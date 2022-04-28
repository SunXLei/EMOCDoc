---
weight: 4
bookFlatSection: false
title: "Algorithm"
BookToC: false
---

# Algorithm Class

*File position: **/EMOC/src/algorithm/algorithm.h** and **/EMOC/src/algorithm/algorithm.cpp***

{{< hint info>}}
**class Algorithm(int thread_id)**

{{< /hint >}}

The parent class of all algorithms in EMOC.  It provides some useful functions for subclasses such as population evaluation and copy.

<style>
    .emoc_doc_table_title{
        background-color:#F0F7FA;
    }
    .emoc_doc_table_content{
        background-color:#FFFFFF;
        width:100%;
    }
</style>

<table class="emoc_doc_table" style="overflow-x: hidden;">
    <tbody>
    <tr>
        <td rowspan="2" ALIGN="left" VALIGN="top"  class="emoc_doc_table_title"><strong class="wuhu">Parameter:</strong></td>
    </tr>
    <tr>
        <td class="emoc_doc_table_content" >
            <strong>thread_id: <i>int, default=0</i></strong><br/>&nbsp &nbsp Index of current thread index. EMOC reserved an array of <i>Global</i> objects. Each object is owned by an unique thread. This index is used to refer to the correpsonding <i>Global</i> object for algorithm class to get some current run's settings easily.
        </td>
    </tr>
    <tr class="emoc_doc_table_title">
        <td rowspan="2" ALIGN="left" VALIGN="top"  class="emoc_doc_table_title"><strong class="wuhu">Member variables:</strong></td>
    </tr>
    <tr >
        <td class="emoc_doc_table_content">
            <strong><i>(protected)</i> g_GlobalSettings: <i>Global*</i></strong><br/>&nbsp &nbsp The pointer to the <i>Global</i> object set according to thread_id. It is used to retrieve the parameter settings directly in algorithm implementations when necessary.<div style="line-height:75%;"><br></div>
            <strong><i>(protected)</i> thread_id_: <i>int</i></strong><br/>&nbsp &nbsp The index of current thread. It is equal to the given thread_id_.<div style="line-height:75%;"><br></div>
            <strong><i>(protected)</i> real_popnum_: <i>int</i></strong><br/>&nbsp &nbsp The size of the optimized population. Note that the population size may not eaqual to the setting number when using decomposition based algorithms. <div style="line-height:75%;"><br></div>
            <strong><i>(protected)</i> runtime_: <i>double</i></strong><br/>&nbsp &nbsp Total time for the algorithm to optimize the problem.
        </td>
    </tr>
    </tbody>
</table>

<br/>

**Public Methods:**

- [void Solve()]({{< relref "#Solve" >}})
- [void PrintPop()]({{< relref "#PrintPop" >}})
- [int GetRealPopNum()]({{< relref "#GetRealPopNum" >}})
- [double GetRuntime()]({{< relref "#GetRuntime" >}})

<div id="Solve">

{{< hint warning>}}
**void Solve()**

{{< /hint >}}

</div>

Optimization process of the algorithm.

It is a pure virtual function which must be implemented in subclass.

<table class="emoc_doc_table" style="overflow-x: hidden">
    <tbody>
    <tr>
        <td rowspan="2" ALIGN="left" VALIGN="top"  class="emoc_doc_table_title"><strong class="wuhu">Parameter:</strong></td>
    </tr>
    <tr>
        <td class="emoc_doc_table_content" >
            <strong>void</strong>
        </td>
    </tr>
    <tr class="emoc_doc_table_title">
        <td rowspan="2" ALIGN="left" VALIGN="top"  class="emoc_doc_table_title"><strong class="wuhu">Returns:</strong></td>
    </tr>
    <tr >
        <td class="emoc_doc_table_content">
            <strong>void</strong>
        </td>
    </tr>
    </tbody>
</table>



<div id="PrintPop">

{{< hint warning>}}
**void PrintPop()**

{{< /hint >}}

</div>

Display the population information in the screen.

<table class="emoc_doc_table" style="overflow-x: hidden">
    <tbody >
    <tr>
        <td rowspan="2" ALIGN="left" VALIGN="top"  class="emoc_doc_table_title"><strong class="wuhu">Parameter:</strong></td>
    </tr>
    <tr >
        <td class="emoc_doc_table_content">
            <strong>void</strong>
        </td>
    </tr>
    <tr class="emoc_doc_table_title">
        <td rowspan="2" ALIGN="left" VALIGN="top"  class="emoc_doc_table_title"><strong class="wuhu">Returns:</strong></td>
    </tr>
    <tr >
        <td class="emoc_doc_table_content">
			<strong>void</strong>
        </td>
    </tr>
    </tbody>
</table>



<div id="GetRealPopNum">

{{< hint warning>}}
**int GetRealPopNum()**

{{< /hint >}}

</div>

Get the real size of population.

<table class="emoc_doc_table" style="overflow-x: hidden">
    <tbody >
    <tr>
        <td rowspan="2" ALIGN="left" VALIGN="top"  class="emoc_doc_table_title"><strong class="wuhu">Parameter:</strong></td>
    </tr>
    <tr >
        <td class="emoc_doc_table_content">
            <strong>void</strong>
        </td>
    </tr>
    <tr class="emoc_doc_table_title">
        <td rowspan="2" ALIGN="left" VALIGN="top"  class="emoc_doc_table_title"><strong class="wuhu">Returns:</strong></td>
    </tr>
    <tr >
        <td class="emoc_doc_table_content">
			<strong>real_popnum_: <i>int</i></strong><br/>&nbsp &nbsp The size of the current population.
        </td>
    </tr>
    </tbody>
</table>



<div id="GetRuntime">

{{< hint warning>}}
**double GetRuntime()**

{{< /hint >}}

</div>

Get the runtime of current run.

<table class="emoc_doc_table" style="overflow-x: hidden">
    <tbody >
    <tr>
        <td rowspan="2" ALIGN="left" VALIGN="top"  class="emoc_doc_table_title"><strong class="wuhu">Parameter:</strong></td>
    </tr>
    <tr >
        <td class="emoc_doc_table_content">
            <strong>void</strong>
        </td>
    </tr>
    <tr class="emoc_doc_table_title">
        <td rowspan="2" ALIGN="left" VALIGN="top"  class="emoc_doc_table_title"><strong class="wuhu">Returns:</strong></td>
    </tr>
    <tr >
        <td class="emoc_doc_table_content">
			<strong>runtime_: <i>double</i></strong><br/>&nbsp &nbsp Total time for the algorithm to optimize the problem.
        </td>
    </tr>
    </tbody>
</table>



<br/>

**Protected Methods:**

- [bool IsTermination()]({{< relref "#IsTermination" >}})
- [void EvaluateInd(Individual *ind)]({{< relref "#EvaluateInd" >}})
- [void EvaluatePop(Individual **pop, int pop_num)]({{< relref "#EvaluatePop" >}})
- [void SwapIndividual(Individual* ind1, Individual* ind2)]({{< relref "#SwapIndividual" >}})
- [void CopyIndividual(Individual* ind_src, Individual* ind_dest)]({{< relref "#CopyIndividual" >}})
- [int MergePopulation(Individual** pop_src1, int pop_num1, Individual** pop_src2, int pop_num2, Individual** pop_dest)]({{< relref "#MergePopulation" >}})

<div id="IsTermination">

{{< hint warning>}}
**bool IsTermination()**

{{< /hint >}}

</div>

Get the execution state of current run.

<table class="emoc_doc_table" style="overflow-x: hidden">
    <tbody >
    <tr>
        <td rowspan="2" ALIGN="left" VALIGN="top"  class="emoc_doc_table_title"><strong class="wuhu">Parameter:</strong></td>
    </tr>
    <tr >
        <td class="emoc_doc_table_content">
            <strong>void</strong>
        </td>
    </tr>
    <tr class="emoc_doc_table_title">
        <td rowspan="2" ALIGN="left" VALIGN="top"  class="emoc_doc_table_title"><strong class="wuhu">Returns:</strong></td>
    </tr>
    <tr >
        <td class="emoc_doc_table_content">
			<strong>is_terminated: <i>bool</i></strong><br/>&nbsp &nbsp Whether the execution is terminated.
        </td>
    </tr>
    </tbody>
</table>



<div id="EvaluateInd">

{{< hint warning>}}
**void EvaluateInd(Individual\* ind)**

{{< /hint >}}

</div>

Evaluate the given individual.

<table class="emoc_doc_table" style="overflow-x: hidden">
    <tbody >
    <tr>
        <td rowspan="2" ALIGN="left" VALIGN="top"  class="emoc_doc_table_title"><strong class="wuhu">Parameter:</strong></td>
    </tr>
    <tr >
        <td class="emoc_doc_table_content">
            <strong>ind: <i>Individual *, default=None</i></strong><br/>&nbsp &nbsp The pointer to the individual which need to be evaluated.
        </td>
    </tr>
    <tr class="emoc_doc_table_title">
        <td rowspan="2" ALIGN="left" VALIGN="top"  class="emoc_doc_table_title"><strong class="wuhu">Returns:</strong></td>
    </tr>
    <tr >
        <td class="emoc_doc_table_content">
            <strong>void</strong>
        </td>
    </tr>
    </tbody>
</table>





<div id="EvaluatePop">

{{< hint warning>}}
**void EvaluatePop(Individual\*\* pop, int pop_num)**

{{< /hint >}}

</div>

Evaluate the given population

<table class="emoc_doc_table" style="overflow-x: hidden">
    <tbody >
    <tr>
        <td rowspan="2" ALIGN="left" VALIGN="top"  class="emoc_doc_table_title"><strong class="wuhu">Parameter:</strong></td>
    </tr>
    <tr >
        <td class="emoc_doc_table_content">
            <strong>pop: <i>Individual**, default=None</i></strong><br/>&nbsp &nbsp The population which need to be evaluated. It's an array of <i>Individual*</i> where each <i>Individual*</i> is a pointer to a individual in the population.<div style="line-height:75%;"><br></div>
			<strong>pop_num: <i>int, default=None</i></strong><br/>&nbsp &nbsp The size of the given population.
        </td>
    </tr>
    <tr class="emoc_doc_table_title">
        <td rowspan="2" ALIGN="left" VALIGN="top"  class="emoc_doc_table_title"><strong class="wuhu">Returns:</strong></td>
    </tr>
    <tr >
        <td class="emoc_doc_table_content">
            <strong>void</strong>
        </td>
    </tr>
    </tbody>
</table>





<div id="SwapIndividual">

{{< hint warning>}}
**void SwapIndividual(Individual\* ind1, Individual\* ind2)**

{{< /hint >}}

</div>

Swap the two given individual.

<table class="emoc_doc_table" style="overflow-x: hidden">
    <tbody >
    <tr>
        <td rowspan="2" ALIGN="left" VALIGN="top"  class="emoc_doc_table_title"><strong class="wuhu">Parameter:</strong></td>
    </tr>
    <tr >
        <td class="emoc_doc_table_content">
            <strong>ind1: <i>Individual*, default=None</i></strong><br/>&nbsp &nbsp Pointer to the first individual.<div style="line-height:75%;"><br></div>
			<strong>ind2: <i>Individual*, default=None</i></strong><br/>&nbsp &nbsp Pointer to the second individual.
        </td>
    </tr>
    <tr class="emoc_doc_table_title">
        <td rowspan="2" ALIGN="left" VALIGN="top"  class="emoc_doc_table_title"><strong class="wuhu">Returns:</strong></td>
    </tr>
    <tr >
        <td class="emoc_doc_table_content">
			<strong>void</strong>
        </td>
    </tr>
    </tbody>
</table>



<div id="CopyIndividual">

{{< hint warning>}}
**void CopyIndividual(Individual\* ind_src, Individual\* ind_dest)**

{{< /hint >}}

</div>

Copy the individual `ind_src` to the indvidual `ind_dest`.

<table class="emoc_doc_table" style="overflow-x: hidden">
    <tbody >
    <tr>
        <td rowspan="2" ALIGN="left" VALIGN="top"  class="emoc_doc_table_title"><strong class="wuhu">Parameter:</strong></td>
    </tr>
    <tr >
        <td class="emoc_doc_table_content">
           <strong>ind_src: <i>Individual*, default=None</i></strong><br/>&nbsp &nbsp Pointer to the source individual.<div style="line-height:75%;"><br></div>
			<strong>ind_dest: <i>Individual*, default=None</i></strong><br/>&nbsp &nbsp Pointer to the destination individual.
        </td>
    </tr>
    <tr class="emoc_doc_table_title">
        <td rowspan="2" ALIGN="left" VALIGN="top"  class="emoc_doc_table_title"><strong class="wuhu">Returns:</strong></td>
    </tr>
    <tr >
        <td class="emoc_doc_table_content">
			<strong>void</strong>
        </td>
    </tr>
    </tbody>
</table>





<div id="MergePopulation">

{{< hint warning>}}
**int MergePopulation(Individual\*\* pop_src1, int pop_num1, Individual\*\* pop_src2, int pop_num2, Individual\*\* pop_dest)**

{{< /hint >}}

</div>

Get the runtime of current run.

<table class="emoc_doc_table" style="overflow-x: hidden">
    <tbody >
    <tr>
        <td rowspan="2" ALIGN="left" VALIGN="top"  class="emoc_doc_table_title"><strong class="wuhu">Parameter:</strong></td>
    </tr>
    <tr >
        <td class="emoc_doc_table_content">
           <strong>pop_src1: <i>Individual**, default=None</i></strong><br/>&nbsp &nbsp First source population. It's an array of <i>Individual*</i> where each <i>Individual*</i> is a pointer to a individual in the population.<div style="line-height:75%;"><br></div>
           <strong>pop_num1: <i>int, default=None</i></strong><br/>&nbsp &nbsp Size of the first source population.<div style="line-height:75%;"><br></div>
           <strong>pop_src2: <i>Individual**, default=None</i></strong><br/>&nbsp &nbsp Second source population. It's an array of <i>Individual*</i> where each <i>Individual*</i> is a pointer to a individual in the population.<div style="line-height:75%;"><br></div>
           <strong>pop_num2: <i>int, default=None</i></strong><br/>&nbsp &nbsp Size of the second source population.<div style="line-height:75%;"><br></div>
           <strong>pop_dest: <i>Individual**, default=None</i></strong><br/>&nbsp &nbsp Destination population. It's an array of <i>Individual*</i> where each <i>Individual*</i> is a pointer to a individual in the population.<div style="line-height:75%;"><br></div>
        </td>
    </tr>
    <tr class="emoc_doc_table_title">
        <td rowspan="2" ALIGN="left" VALIGN="top"  class="emoc_doc_table_title"><strong class="wuhu">Returns:</strong></td>
    </tr>
    <tr >
        <td class="emoc_doc_table_content">
			<strong>mixed_popnum: <i>int</i></strong><br/>&nbsp &nbsp Size of the mixed population. 
        </td>
    </tr>
    </tbody>
</table>











