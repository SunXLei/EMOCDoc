---
weight: 1
bookFlatSection: false
title: "Non-dominated Sorting"
BookToC: false
---
# Non-dominated Sorting

*File position: **/EMOC/src/core/nd_sort.h** and **/EMOC/src/core/nd_sort.cpp***

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
**void NonDominatedSort(Individual \*\*pop, int pop_num, int obj_num, bool is_consider_cons = false)**

{{< /hint >}}

</div>

Do the non-dominated sorting on current population `pop`. The results are stored in the `rank_` variable of each individual in the population.

<table class="emoc_doc_table" style="overflow-x: hidden">
    <tbody >
    <tr>
        <td rowspan="2" ALIGN="left" VALIGN="top"  class="emoc_doc_table_title"><strong class="wuhu">Parameter:</strong></td>
    </tr>
    <tr >
        <td class="emoc_doc_table_content">
           <strong>pop: <i>Individual**, default=None</i></strong><br/>&nbsp &nbsp The population which need to be initialized. It's an array of <i>Individual*</i> where each <i>Individual*</i> is a pointer to a individual in the population.<div style="line-height:75%;"><br></div>
            <strong>pop_num: <i>int, default=None</i></strong><br/>&nbsp &nbsp The size of the given population.<div style="line-height:75%;"><br></div>
            <strong>obj_num: <i>int, default=None</i></strong><br/>&nbsp &nbsp The number of objectives.<div style="line-height:75%;"><br></div>
            <strong>is_consider_cons: <i>bool, default=false</i></strong><br/>&nbsp &nbsp Whether to consider the constraints of individual in the sorting.
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

