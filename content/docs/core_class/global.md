---
weight: 5
bookFlatSection: false
title: "Global"
BookToC: false
---

# Global Class

*File position: **/EMOC/src/core/global.h** and **/EMOC/src/core/global.cpp***

{{< hint info>}}
**class Global(const char\* algorithm_name, const char\* problem_name, int population_num, int dec_num, int obj_num, int max_evaluation, int thread_id, int output_interval, int run_id = 0)**

{{< /hint >}}

`Global` class represents an execution entity of EMOC which basically is a specified algorithm optimized a certain problem with pre-defined parameters. It holds all the relevant datas such as the pointer to algorithm, the pointer to problem, optimization settings and the population.

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
            <strong>algorithm_name: <i>const char*, default=None</i></strong><br/>&nbsp &nbsp The name of the specified algorithm.<div style="line-height:75%;"><br></div>
            <strong>problem_name: <i>const char*, default=None</i></strong><br/>&nbsp &nbsp The name of the specified problem.<div style="line-height:75%;"><br></div>
            <strong>population_num: <i>int, default=None</i></strong><br/>&nbsp &nbsp The number of population size.<div style="line-height:75%;"><br></div>
            <strong>dec_num: <i>int, default=None</i></strong><br/>&nbsp &nbsp The number of the decision variables for problem settings.<div style="line-height:75%;"><br></div>
            <strong>obj_num: <i>int, default=None</i></strong><br/>&nbsp &nbsp The number of objective functions for problem settings.<div style="line-height:75%;"><br></div>
            <strong>max_evaluation: <i>int, default=None</i></strong><br/>&nbsp &nbsp The max evaluation times for current run.<div style="line-height:75%;"><br></div>
            <strong>thread_id: <i>int, default=None</i></strong><br/>&nbsp &nbsp The index of used thread. If there is no multi-thread enabled, 0 will be used. <div style="line-height:75%;"><br></div>
            <strong>output_interval: <i>int, default=None</i></strong><br/>&nbsp &nbsp The interval of population saving in generation.<div style="line-height:75%;"><br></div>
            <strong>run_id: <i>int, default=0</i></strong><br/>&nbsp &nbsp The index of current run. This is for multiple runs with same parameter settings, starting from 0.<div style="line-height:75%;"><br></div>
        </td>
    </tr>
    <tr class="emoc_doc_table_title">
        <td rowspan="2" ALIGN="left" VALIGN="top"  class="emoc_doc_table_title"><strong class="wuhu">Member variables:</strong></td>
    </tr>
    <tr >
        <td class="emoc_doc_table_content">
            <strong><i>(public)</i> dec_num_: <i>int</i></strong><br/>&nbsp &nbsp The number of the decision variables. It is equal to the given dec_num.<div style="line-height:75%;"><br></div>
            <strong><i>(public)</i> obj_num_: <i>int</i></strong><br/>&nbsp &nbsp The number of objectives. It is equal to the given obj_num.<div style="line-height:75%;"><br></div>
            <strong><i>(public)</i> population_num_: <i>int</i></strong><br/>&nbsp &nbsp The number of population size.  It is equal to the given population_num.<div style="line-height:75%;"><br></div>
            <strong><i>(public)</i> max_evaluation_: <i>int</i></strong><br/>&nbsp &nbsp The max evaluation times. It is equal to the given max_evaluation.<div style="line-height:75%;"><br></div>
            <strong><i>(public)</i> output_interval_: <i>int</i></strong><br/>&nbsp &nbsp The interval of population saving in generation. It is equal to the given output_interval.<div style="line-height:75%;"><br></div>
            <strong><i>(public)</i> algorithm_name_: <i>std::string</i></strong><br/>&nbsp &nbsp The name of the specified algorithm. It is equal to the given algorithm_name.<div style="line-height:75%;"><br></div>
            <strong><i>(public)</i> problem_name_: <i>std::string</i></strong><br/>&nbsp &nbsp The name of the specified problem. It is equal to the given problem_name.<div style="line-height:75%;"><br></div>
            <strong><i>(public)</i> iteration_num_: <i>int</i></strong><br/>&nbsp &nbsp The iteration index. It is updated by the algorithm in it's optimization loop.<div style="line-height:75%;"><br></div>
            <strong><i>(public)</i> current_evaluation_: <i>int</i></strong><br/>&nbsp &nbsp Current evaluation times. It is updated when the individual is evaluated.<div style="line-height:75%;"><br></div>
            <strong><i>(public)</i> algorithm_: <i>Algorithm*</i></strong><br/>&nbsp &nbsp Pointer to the current run's algorithm object.<div style="line-height:75%;"><br></div>
            <strong><i>(public)</i> problem_: <i>Problem*</i></strong><br/>&nbsp &nbsp Pointer to the current run's problem object.<div style="line-height:75%;"><br></div>
            <strong><i>(public)</i> dec_lower_bound_: <i>std::vector&ltdouble&gt</i></strong><br/>&nbsp &nbsp Lower bound for each decision variables.<div style="line-height:75%;"><br></div>
            <strong><i>(public)</i> dec_upper_bound_: <i>std::vector&ltdouble&gt</i></strong><br/>&nbsp &nbsp Upper bound for each decision variables.<div style="line-height:75%;"><br></div>
            <strong><i>(public)</i> parent_population_: <i>std::vector&ltIndividual*&gt</i></strong><br/>&nbsp &nbsp The parent population of current run.<div style="line-height:75%;"><br></div>
            <strong><i>(public)</i> offspring_population_: <i>std::vector&ltIndividual*&gt</i></strong><br/>&nbsp &nbsp The offspring population of current run.<div style="line-height:75%;"><br></div>
            <strong><i>(public)</i> mixed_population_: <i>std::vector&ltIndividual*&gt</i></strong><br/>&nbsp &nbsp The mixed population of current run. It is usually used to do some merge work.<div style="line-height:75%;"><br></div>
        </td>
    </tr>
    </tbody>
</table>

<br/>

**Public Methods:**

- [void Init()]({{< relref "#Init" >}})

- [void Start()]({{< relref "#Start" >}})

- [void InitializeIndividual(Individual* ind)]({{< relref "#InitializeIndividual" >}})

- [void InitializePopulation(Individual** pop, int pop_num)]({{< relref "#InitializePopulation" >}})

  



<div id="Init">
{{< hint warning>}}
**void Init()**

{{< /hint >}}

</div>

Initialize the `Global` object such as setting the parameters' value and allocating memories.

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



<div id="Start">

{{< hint warning>}}
**void Start()**

{{< /hint >}}

</div>

Start the optimization with current configuration.

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



<div id="InitializeIndividual">

{{< hint warning>}}
**void InitializeIndividual(Individual\* ind)**

{{< /hint >}}

</div>

Initialize the given individual (i.e. set the decision variables with uniform random number in the decision bounds).

<table class="emoc_doc_table" style="overflow-x: hidden">
    <tbody >
    <tr>
        <td rowspan="2" ALIGN="left" VALIGN="top"  class="emoc_doc_table_title"><strong class="wuhu">Parameter:</strong></td>
    </tr>
    <tr >
        <td class="emoc_doc_table_content">
            <strong>ind: <i>Individual *, default=None</i></strong><br/>&nbsp &nbsp The pointer to the individual which need to be initialized.
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



<div id="InitializePopulation">

{{< hint warning>}}
**void InitializePopulation(Individual\*\* pop, int pop_num)**

{{< /hint >}}

</div>

Initialize the given population.

<table class="emoc_doc_table" style="overflow-x: hidden">
    <tbody >
    <tr>
        <td rowspan="2" ALIGN="left" VALIGN="top"  class="emoc_doc_table_title"><strong class="wuhu">Parameter:</strong></td>
    </tr>
    <tr >
        <td class="emoc_doc_table_content">
           <strong>pop: <i>Individual**, default=None</i></strong><br/>&nbsp &nbsp The population which need to be initialized. It's an array of <i>Individual*</i> where each <i>Individual*</i> is a pointer to a individual in the population.<div style="line-height:75%;"><br></div>
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

