---
weight: 3
bookFlatSection: false
title: "Differential Evolution"
BookToC: false
---
# Differential Evolution

*File position: **/EMOC/src/operator/de.h** and **/EMOC/src/operator/de.cpp***

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
**void DE(Individual \*parent1, Individual \*parent2, Individual \*parent3, Individual \*offspring,  std::vector\<double\>& lower_bound, std::vector\<double\>& upper_bound, CrossoverParameter& cross_para)**

{{< /hint >}}

</div>

Do the differential evolution on `parent1` , `parent2` and `parent3`, the results are stored in `offspring`.

<table class="emoc_doc_table" style="overflow-x: hidden">
    <tbody >
    <tr>
        <td rowspan="2" ALIGN="left" VALIGN="top"  class="emoc_doc_table_title"><strong class="wuhu">Parameter:</strong></td>
    </tr>
    <tr >
        <td class="emoc_doc_table_content">
           <strong>parent1: <i>Individual*, default=None</i></strong><br/>&nbsp &nbsp The pointer to the first parent individual to do differential evolution.<div style="line-height:75%;"><br></div>
            <strong>parent2: <i>Individual*, default=None</i></strong><br/>&nbsp &nbsp The pointer to the second parent individual to do differential evolution.<div style="line-height:75%;"><br></div>
            <strong>parent3: <i>Individual*, default=None</i></strong><br/>&nbsp &nbsp The pointer to the third parent individual to do differential evolution.<div style="line-height:75%;"><br></div>
            <strong>offspring: <i>Individual*, default=None</i></strong><br/>&nbsp &nbsp The pointer to the offspring individual of differential evolution results. The memory of the offspring need to be allocated outside the function.<div style="line-height:75%;"><br></div>
            <strong>lower_bound: <i>std::vector&ltdouble&gt, default=None</i></strong><br/>&nbsp &nbsp The lower boundary of decision variables.<div style="line-height:75%;"><br></div>
            <strong>upper_bound: <i>std::vector&ltdouble&gt, default=None</i></strong><br/>&nbsp &nbsp The upper boundary of decision variables.<div style="line-height:75%;"><br></div>
            <strong>cross_para: <i>CrossoverParameter, default=None</i></strong><br/>&nbsp &nbsp The parameter of this crossover. The type <i>CrossoverParameter</i> is just a simple structure which has three member variables (i.e., the crossover probability, the distribution index1 and the distribution index2).
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

