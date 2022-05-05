---
weight: 8
bookFlatSection: false
title: "Python DLL"
---
# Python Dynamic Link Library

<style>
    .emoc_doc_table_title{
        background-color:#F0F7FA;
    }
    .emoc_doc_table_content{
        background-color:#FFFFFF;
        width:100%;
    }
</style>

In [Quick Start]({{< ref "/docs/quickstart/use_emoc_in_python" >}}) section, we give a brief introduction on how to use EMOC in python language. Basically speaking, several fundamental classes are exported into python. So the users can utilize these classes to define their own problem and solve it with available algorithms in EMOC.  

In this section, we will give the detailed definition of these exported classes to help users understand the python dynamic link library of EMOC.



## Exported Classes

### Problem

This class is basically the same as original class in C++ except some member variable names.

{{< hint info>}}
**class Problem(int dec_num, int obj_num)**

{{< /hint >}}

The parent class of all test problems in EMOC. The custom problem in python need to inherit form this class.

<table class="emoc_doc_table" style="overflow-x: hidden;">
    <tbody>
    <tr>
        <td rowspan="2" ALIGN="left" VALIGN="top"  class="emoc_doc_table_title"><strong class="wuhu">Parameter:</strong></td>
    </tr>
    <tr>
        <td class="emoc_doc_table_content" >
            <strong>dec_num: <i>int, default=None</i></strong><br/>&nbsp &nbsp The number of decision variables setting for the problem.<div style="line-height:75%;"><br></div>
            <strong>obj_num: <i>int, default=None</i></strong><br/>&nbsp &nbsp The number of objective functions setting for the problem.<br/>
        </td>
    </tr>
    <tr class="emoc_doc_table_title">
        <td rowspan="2" ALIGN="left" VALIGN="top"  class="emoc_doc_table_title"><strong class="wuhu">Member variables:</strong></td>
    </tr>
    <tr >
        <td class="emoc_doc_table_content">
            <strong><i>(public)</i> dec_num: <i>int</i></strong><br/>&nbsp &nbsp The number of decision variables set by users. It is equal to the given dec_num. <div style="line-height:75%;"><br></div>
            <strong><i>(public)</i> obj_num: <i>int</i></strong><br/>&nbsp &nbsp The number of objective functions set by users. It is equal to the given obj_num.<div style="line-height:75%;"><br></div>
            <strong><i>(public)</i> lower_bound: <i>std::vector&ltdouble&gt</i></strong><br/>&nbsp &nbsp The lower bound of each decision variable. The size of this <i>std::vector</i> is dec_num.<div style="line-height:75%;"><br></div>
            <strong><i>(public)</i> upper_bound: <i>std::vector&ltdouble&gt</i></strong><br/>&nbsp &nbsp The upper bound of each decision variable. The size of this <i>std::vector</i> is dec_num.
        </td>
	</tr>
</tbody>
</table>



<br/>

**Public Member Functions:**

- [void CalObj(Individual\* ind)]({{< relref "#CalObj" >}})

<div id="CalObj">

{{< hint warning>}}
**void CalObj(Individual\* ind)**


{{< /hint >}}

</div>

Calculate the objective function values.

This function is a pure virtual function which must be implemented in custom problem in python.

<table class="emoc_doc_table" style="overflow-x: hidden">
    <tbody >
    <tr>
        <td rowspan="2" ALIGN="left" VALIGN="top"  class="emoc_doc_table_title"><strong class="wuhu">Parameter:</strong></td>
    </tr>
    <tr >
        <td class="emoc_doc_table_content">
            <strong>ind: <i>Individual*, default=None</i></strong><br/>&nbsp &nbsp Pointer to the individual which need to calculate the objectives.
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

<br/>

### Individual

This class is basically the same as original class in C++ except some member variable names.

{{< hint info>}}
**class Individual(int dec_num, int obj_num)**

{{< /hint >}}

The class for each individual in the population.

<table class="emoc_doc_table" style="overflow-x: hidden">
    <tbody>
    <tr>
        <td rowspan="2" ALIGN="left" VALIGN="top"  class="emoc_doc_table_title"><strong class="wuhu">Parameter:</strong></td>
    </tr>
    <tr>
        <td class="emoc_doc_table_content" >
            <strong>dec_num: <i>int, default=None</i></strong><br/>&nbsp &nbsp The number of decision variables.<div style="line-height:75%;"><br></div>
            <strong>obj_num: <i>int, default=None</i></strong><br/>&nbsp &nbsp The number of objectives.<br/>
        </td>
    </tr>
    <tr class="emoc_doc_table_title">
        <td rowspan="2" ALIGN="left" VALIGN="top"  class="emoc_doc_table_title"><strong class="wuhu">Member variables:</strong></td>
    </tr>
    <tr >
        <td class="emoc_doc_table_content">
            <strong><i>(public)</i> dec: <i>std::vector&ltdouble&gt</i></strong><br/>&nbsp &nbsp Decision variables of this individual. The size of this <i>std::vector</i> is dec_num. <div style="line-height:75%;"><br></div>
            <strong><i>(public)</i> obj: <i>std::vector&ltdouble&gt</i></strong><br/>&nbsp &nbsp Objectives of this individual. The size of this <i>std::vector</i> is obj_num.
        </td>
    </tr>
    </tbody>
</table>

<br/>

### EMOCManager

{{< hint info>}}
**class EMOCManager()**

{{< /hint >}}

`EMOCManager` is the manager class of EMOC which controls the execution of EMOC. Most original member variables in C++ definition are omitted. Because they are not needed in python.

<table class="emoc_doc_table" style="overflow-x: hidden;">
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
        <td rowspan="2" ALIGN="left" VALIGN="top"  class="emoc_doc_table_title"><strong class="wuhu">Member variables:</strong></td>
    </tr>       
	<tr >
    	<td class="emoc_doc_table_content">
        	<strong>void</strong>
        </td>
	</tr>
</tbody>
</table>





<br/>

**Public Methods:**

- [void Run()]({{< relref "#Run" >}})
- [void SetTaskParameters(const EMOCParameters& para)]({{< relref "#SetTaskParameters" >}})
- [EMOCGeneralResult GetPythonResult()]({{< relref "#EMOCGeneralResult " >}})





<div id="Run">

{{< hint warning>}}
**void Run()**

{{< /hint >}}

</div>

Start this optimization with current parameters.

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



<div id="SetTaskParameters">

{{< hint warning>}}
**void SetTaskParameters(const EMOCParameters& para)**

{{< /hint >}}

</div>

Set the parameters of this execution

<table class="emoc_doc_table" style="overflow-x: hidden">
    <tbody>
    <tr>
        <td rowspan="2" ALIGN="left" VALIGN="top"  class="emoc_doc_table_title"><strong class="wuhu">Parameter:</strong></td>
    </tr>
    <tr>
        <td class="emoc_doc_table_content" >
            <strong>para: <i>const EMOCParameters&, default=None</i></strong><br/>&nbsp &nbsp Parameters of this run.
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



<div id="GetPythonResult">

{{< hint warning>}}
**EMOCGeneralResult GetPythonResult()**

{{< /hint >}}

</div>

Get the optimization results of this run.

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
            <strong>result: <i>EMOCGeneralResult</i></strong><br/>&nbsp &nbsp Optimization results of this run.
        </td>
    </tr>
    </tbody>
</table>











<br/>

### EMOCParameters

{{< hint info>}}
**class EMOCParameters()**

{{< /hint >}}

`EMOCParameters` is a simple structure consists of basic parameter settings variables and two public interface for configuring custom problem and initial population

<table class="emoc_doc_table" style="overflow-x: hidden;">
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
        <td rowspan="2" ALIGN="left" VALIGN="top"  class="emoc_doc_table_title"><strong class="wuhu">Member variables:</strong></td>
    </tr>
    <tr >
        <td class="emoc_doc_table_content">
            <strong><i>(public)</i> algorithm_name: <i>string</i></strong><br/>&nbsp &nbsp Algorithm name. <div style="line-height:75%;"><br></div>
            <strong><i>(public)</i> problem_name: <i>string</i></strong><br/>&nbsp &nbsp Problem name. <div style="line-height:75%;"><br></div>
            <strong><i>(public)</i> population_num: <i>int</i></strong><br/>&nbsp &nbsp The size of population. <div style="line-height:75%;"><br></div>
            <strong><i>(public)</i> decision_num: <i>int</i></strong><br/>&nbsp &nbsp The number of decision variables. <div style="line-height:75%;"><br></div>
            <strong><i>(public)</i> objective_num: <i>int</i></strong><br/>&nbsp &nbsp The number of objectives. <div style="line-height:75%;"><br></div>
            <strong><i>(public)</i> max_evaluation: <i>int</i></strong><br/>&nbsp &nbsp The max evaluation times of this optimization. <div style="line-height:75%;"><br></div>
            <strong><i>(public)</i> output_interval: <i>int</i></strong><br/>&nbsp &nbsp Save interval in generation.
        </td>
    </tr>
    </tbody>
</table>

<br/>

**Public Methods:**

- [void SetProblem(Problem\* problem)]({{< relref "#SetProblem" >}})
- [void SetInitialPop(std::vector\<std::vector\<double\>\> initial_pop)]({{< relref "#SetInitialPop" >}})



<div id="SetProblem">

{{< hint warning>}}
**void SetProblem(Problem\* problem)**

{{< /hint >}}

</div>

Set the custom problem.

<table class="emoc_doc_table" style="overflow-x: hidden">
    <tbody>
    <tr>
        <td rowspan="2" ALIGN="left" VALIGN="top"  class="emoc_doc_table_title"><strong class="wuhu">Parameter:</strong></td>
    </tr>
    <tr>
        <td class="emoc_doc_table_content" >
            <strong>problem: <i>Problem*, default=None</i></strong><br/>&nbsp &nbsp Pointer to the custom problem. This can be an problem object in python.
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



<div id="SetInitialPop">

{{< hint warning>}}
**void SetInitialPop(std::vector\<std::vector\<double\>\> initial_pop)**

{{< /hint >}}

</div>

Set the custom initial population.

<table class="emoc_doc_table" style="overflow-x: hidden">
    <tbody>
    <tr>
        <td rowspan="2" ALIGN="left" VALIGN="top"  class="emoc_doc_table_title"><strong class="wuhu">Parameter:</strong></td>
    </tr>
    <tr>
        <td class="emoc_doc_table_content" >
            <strong>initial_pop: <i>std::vector&ltstd::vector&ltdouble&gt&gt, default=None</i></strong><br/>&nbsp &nbsp The custom initial population. It's basically a 2D array of double. Each row is the decision variables of an individual.
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









<br/>

### EMOCGeneralResult

{{< hint info>}}
**class EMOCGeneralResult()**

{{< /hint >}}

The class for the optimization results which can get by `EMOCManager::GetResult()`.

<table class="emoc_doc_table" style="overflow-x: hidden;">
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
        <td rowspan="2" ALIGN="left" VALIGN="top"  class="emoc_doc_table_title"><strong class="wuhu">Member variables:</strong></td>
    </tr>
    <tr >
        <td class="emoc_doc_table_content">
            <strong><i>(public)</i> igd: <i>double</i></strong><br/>&nbsp &nbsp IGD value of this optimization. This is only valid in multi-objective optimization problem. <div style="line-height:75%;"><br></div>
            <strong><i>(public)</i> gd: <i>double</i></strong><br/>&nbsp &nbsp GD value of this optimization. This is only valid in multi-objective optimization problem.<div style="line-height:75%;"><br></div>
            <strong><i>(public)</i> hv: <i>double</i></strong><br/>&nbsp &nbsp HV value of this optimization. This is only valid in multi-objective optimization problem.<div style="line-height:75%;"><br></div>
            <strong><i>(public)</i> spacing: <i>double</i></strong><br/>&nbsp &nbsp Spacing value of this optimization. This is only valid in multi-objective optimization problem.<div style="line-height:75%;"><br></div>
            <strong><i>(public)</i> igdplus: <i>double</i></strong><br/>&nbsp &nbsp IGD Plus value of this optimization. This is only valid in multi-objective optimization problem.<div style="line-height:75%;"><br></div>
            <strong><i>(public)</i> gdplus: <i>double</i></strong><br/>&nbsp &nbsp GD Plus value of this optimization. This is only valid in multi-objective optimization problem.<div style="line-height:75%;"><br></div>
            <strong><i>(public)</i> best_value: <i>double</i></strong><br/>&nbsp &nbsp Best found value. This is only valid in single-objective optimization problem. <div style="line-height:75%;"><br></div>
            <strong><i>(public)</i> runtime: <i>double</i></strong><br/>&nbsp &nbsp The run time of this run. <div style="line-height:75%;"><br></div>
            <strong><i>(public)</i> pop_num: <i>int</i></strong><br/>&nbsp &nbsp The size of the final population. <div style="line-height:75%;"><br></div>
            <strong><i>(public)</i> pop_decs: <i>2D list</i></strong><br/>&nbsp &nbsp Decision variables of final population. <div style="line-height:75%;"><br></div>
            <strong><i>(public)</i> pop_objs: <i>2D list</i></strong><br/>&nbsp &nbsp Objectives of final population.
        </td>
    </tr>
    </tbody>
</table>