---
weight: 1
bookFlatSection: false
title: "Problem"
---

# Add New Problems in EMOC

Due to the simple structure of EMOC, it is straightforward to add a new problem in EMOC. This needs three steps as below. We will take the test problem ZDT1 as an example.



## Create the Declaration

First, we need to create a header file to make a declaration of ZDT1. Although there is no strict position request. We recommend to go to the directory **'/src/problem/'**, make a new directory **'/zdt'** and create a header file **'zdt.h'** in it.

![image-20220423160828910](../../../images/problem_headerfile_pos.png)

In **'zdt.h'**, we declare the class `ZDT1` which inherits from class  `Problem`:

```c++
#pragma once
#include "core/individual.h"
#include "problem/problem.h"

namespace emoc {
    
	class ZDT1 :public Problem
	{
	public:
		ZDT1(int dec_num, int obj_num);
		virtual ~ZDT1();

		void CalObj(Individual* ind);
	};
    
}
```

The structure of `ZDT1` is very simple, just a constructor, a deconstructor and a virtual function `CalObj(Individual* ind)` inherit from parent class `Problem`. In each evaluation, EMOC will call the `CalObj` function to calculate the objective value. 



## Create the Definition

After declaring the class `ZDT1`, the **'zdt.cpp'** file needs to be created in the same directory.  In **'zdt.cpp'**, we define the three functions which declared in **'zdt.h'**:

```c++
#include "problem/zdt/zdt.h"

#include <cmath>

#include "core/macro.h"
#include "core/global.h"

namespace emoc {
    
	ZDT1::ZDT1(int dec_num, int obj_num) :Problem(dec_num, obj_num)
	{
		for (int i = 0; i < dec_num; ++i)
		{
			lower_bound_[i] = 0.0;
			upper_bound_[i] = 1.0;
		}
	}

	ZDT1::~ZDT1()
	{

	}

	void ZDT1::CalObj(Individual* ind)
	{
		double f1 = 0, f2 = 0;
		double g = 0, h = 0;

		f1 = ind->dec_[0];
		for (int i = 1; i < dec_num_; i++)
		{
			g += ind->dec_[i];
		}

		g = 1 + g * 9.0 / (dec_num_ - 1);
		h = 1 - sqrt((double)(f1 / g));
		f2 = g * h;

		ind->obj_[0] = f1;
		ind->obj_[1] = f2;
	}
    
}
```

In the constructor, it needs to call the `Problem's` constructor first to set the variable `dec_num_`, `obj_num_` of `Problem` class and allocate some memories. In addition to this, the decision bound should be set by `lower_bound_` and `upper_bound_`.

In the deconstructor, we do nothing because there is no extra memories managed by class `ZDT1`.

In `CalObj(Individual* ind)`, calculating the objective value based on the decision variable `ind->dec_` and set the result to `ind->obj_`.

## Register into EMOC

Once the declaration and definition has been completed, we need to register the new problem into EMOC. The macro `EMOC_REGIST_PROBLEM` is provided to simplify the process.

First go to the file **'/src/problem/problem_head_collect.h'**, add the new header **'zdt.h'**.

```c++
// problem_head_collect.h

#pragma once

...
    
// include the new problem header file
#include "problem/zdt/zdt.h"
```

And then, open the file **'/src/problem/problem_head_collect.cpp'**, add the macro call.

```c++
// problem_head_collect.cpp

#include "problem/problem_head_collect.h"

#include "core/macro.h"
#include "problem/problem_factory.h"

namespace emoc {
	
    ...
    
	// register new problem
	EMOC_REGIST_PROBLEM(Multiobjective, ZDT Series, ZDT1);

}
```

The macro `EMOC_REGIST_PROBLEM` accept three parameters:

- **Problem property:** Multiobjective / Singleobjective to declare the property of this problem.
- **Problem category:** Custom category name (can be any valid string).
- **Problem name:** The name string of problem, must be the same with class name.

After registering and rebuilding, the new problem can be directly used in EMOC with problem name.



For deep understand of the structure of EMOC, please go through the section [Core Class]({{< ref "/docs/core_class/overview" >}})

















