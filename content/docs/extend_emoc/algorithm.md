---
weight: 2
bookFlatSection: false
title: "Algorithm"
---

# Add New Algorithms in EMOC

Adding a new algorithm is very similar to adding a new problem. We will take NSGA2 as an example (for simplicity, some details are omitted, users can check the complete source code themselves).



## Create the Declaration

 First, let's go to the directory **'/src/algorithm/'**, make a new directory **'/nsga2'** and create a header file **'nsga2.h'** in it. We make the declaration about class `NSGA2` which inherits from class  `Algorithm` in **'nsga2.h'**:

```c++
#pragma once
#include "core/individual.h"
#include "algorithm/algorithm.h"
#include "problem/problem.h"

#include <vector>

namespace emoc {

	class NSGA2 : public Algorithm
	{
	public:
		NSGA2(int thread_id);
		virtual ~NSGA2();
		
		void Solve();

	private:
		void Initialization();
		void Crossover(Individual **parent_pop, Individual **offspring_pop);
		void EnvironmentalSelection(Individual **parent_pop, Individual **mixed_pop);
	};

}
```

There are three public functions and several private functions in the class. The most important function is `Solve()` which is a virtual function inherit from parent class `Algorithm`. We need to implement the details of algorithm in that function and EMOC will call `Solve()` to optimize the problem.



## Create the Definition

After declaring the class `NSGA2`, the **'nsga2.cpp'** file should be created in the same directory.  The definition in **'nsga2.cpp'** is shown below:

```c++
#include "algorithm/nsga2/nsga2.h"

#include <vector>
#include <algorithm>
#include <iostream>

#include "core/macro.h"
#include "core/global.h"
#include "core/nd_sort.h"
#include "core/tournament_selection.h"
#include "operator/polynomial_mutation.h"
#include "operator/sbx.h"
#include "random/random.h"

namespace emoc {

	NSGA2::NSGA2(int thread_id) :Algorithm(thread_id)
	{

	}

	NSGA2::~NSGA2()
	{

	}

	void NSGA2::Solve()
	{
		Initialization();
		while (!IsTermination())
		{
			// generate offspring population
			Crossover(g_GlobalSettings->parent_population_.data(), g_GlobalSettings->offspring_population_.data());
			PolynomialMutation(g_GlobalSettings->offspring_population_.data(), 2 * (real_popnum_ / 2), g_GlobalSettings);
            
            // evaluate the offspring population
			EvaluatePop(g_GlobalSettings->offspring_population_.data(), 2 * (real_popnum_ / 2));
            
            // merge the parent popualtion and offspring population
			MergePopulation(g_GlobalSettings->parent_population_.data(), real_popnum_, g_GlobalSettings->offspring_population_.data(),
				2 * (real_popnum_ / 2), g_GlobalSettings->mixed_population_.data());
			
			// select next generation's population
			EnvironmentalSelection(g_GlobalSettings->parent_population_.data(), g_GlobalSettings->mixed_population_.data());
		}
	}
}
```

In constructor, the only thing we do is calling the `Algorithm's` constructor to initialize some variables.

In deconstructor, there is nothing to release for `NSGA2`.

In function `Solve()`, we use some self-defined functions and common utility functions to complete the optimization process.



## Register into EMOC

The register of a new algorithm is very straightforward with the aid of macro `EMOC_REGIST_ALGORITHM`. Go to the file **'/src/algorithm/algorithm_head_collect.h'** and add the new header **'nsga2.h'** first.

```c++
// algorithm_head_collect.h

#pragma once

...

// include the new algorithm header file
#include "algorithm/nsga2/nsga2.h"
```

And then, open the file **'/src/algorithm/algorithm_head_collect.cpp'**, add the macro call.

```c++
// algorithm_head_collect.cpp

#include "algorithm/algorithm_head_collect.h"

#include "core/macro.h"
#include "algorithm/algorithm_factory.h"

namespace emoc {

    ...
        
	// Register new algorithm
	EMOC_REGIST_ALGORITHM(Multiobjective, Dominance Based, NSGA2);
    
}
```

The macro `EMOC_REGIST_ALGORITHM` accept three parameters:

- **Algorithm property:** Multiobjective / Singleobjective to declare the property of this algorithm.
- **Algorithm category:** Custom category name (can be any valid string).
- **Algorithm name:** The name string of algorithm, must be the same with class name.

After registering and rebuilding, the new algorithm can be directly used in EMOC with algorithm name.



For deep understand of the structure of EMOC, please go through the section [Core Class]({{< ref "/docs/core_class/overview" >}})