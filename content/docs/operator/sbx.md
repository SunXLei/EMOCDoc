---
weight: 2
bookFlatSection: false
title: "Simulated Binary Crossover"
BookToC: false
---
# Simulated Binary Crossover

*File position: **/EMOC/src/operator/sbx.h** and **/EMOC/src/operator/sbx.cpp***

<style>
    .emoc_doc_table_title{
        background-color:#F0F7FA;
    }
    .emoc_doc_table_content{
        background-color:#FFFFFF;
        width:100%;
    }
</style>

<div>
{{< hint warning>}}
**void SBX(Individual\* parent1, Individual\* parent2, Individual\* offspring1, Individual\* offspring2, std::vector\<double\>& lower_bound, std::vector\<double\>& upper_bound, CrossoverParameter& cross_para)**

{{< /hint >}}

</div>

Do the simulated binary crossover based on `parent1` and `parent2`, the results are stored in `offspring1` and `offspring2`.

<table class="emoc_doc_table" style="overflow-x: hidden">
    <tbody >
    <tr>
        <td rowspan="2" ALIGN="left" VALIGN="top"  class="emoc_doc_table_title"><strong class="wuhu">Parameter:</strong></td>
    </tr>
    <tr >
        <td class="emoc_doc_table_content">
           <strong>parent1: <i>Individual*, default=None</i></strong><br/>&nbsp &nbsp The pointer to the first parent individual to do simulated binary crossover.<div style="line-height:75%;"><br></div>
            <strong>parent2: <i>Individual*, default=None</i></strong><br/>&nbsp &nbsp The pointer to the second parent individual to do simulated binary crossover.<div style="line-height:75%;"><br></div>
            <strong>offspring1: <i>Individual*, default=None</i></strong><br/>&nbsp &nbsp The pointer to the first offspring individual of simulated crossover results. The memory of the offspring need to be allocated outside the function.<div style="line-height:75%;"><br></div>
            <strong>offspring2: <i>Individual*, default=None</i></strong><br/>&nbsp &nbsp The pointer to the second offspring individual of simulated crossover results. The memory of the offspring need to be allocated outside the function.<div style="line-height:75%;"><br></div>
            <strong>lower_bound: <i>std::vector&ltdouble&gt, default=None</i></strong><br/>&nbsp &nbsp The lower boundary of decision variables.<div style="line-height:75%;"><br></div>
            <strong>upper_bound: <i>std::vector&ltdouble&gt, default=None</i></strong><br/>&nbsp &nbsp The upper boundary of decision variables.<div style="line-height:75%;"><br></div>
            <strong>cross_para: <i>CrossoverParameter, default=None</i></strong><br/>&nbsp &nbsp The parameter of this crossover. The type <i>CrossoverParameter</i> is just a simple structure which has three member variables (i.e., the crossover probability, the distribution index1 and the distribution index2)
        </td>
    </tr>
    <tr class="emoc_doc_table_title">
        <td rowspan="2" ALIGN="left" VALIGN="top"  class="emoc_doc_table_title"><strong class="wuhu">Returns:</strong></td>
    </tr>
    <tr >
        <td class="emoc_doc_table_content">
            <strong>void</strong><br/>
        </td>
    </tr>
    </tbody>
</table>

