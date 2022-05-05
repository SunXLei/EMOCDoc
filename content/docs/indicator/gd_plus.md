---
weight: 2
bookFlatSection: false
title: "Generational Distance Plus"
BookToC: false
---
# Generational Distance Plus

*File position: **/EMOC/src/metric/gd_plus.h** and **/EMOC/src/metric/gd_plus.cpp***

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
**double CalculateGDPlus(Individual\*\* pop, int pop_num, int obj_num, double\*\* pf_data, int pf_size)**

{{< /hint >}}

</div>

Calculate the generational distance plus value of current population `pop` based on the pareto front data `pf_data`. 

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
            <strong>pf_data: <i>double**, default=None</i></strong><br/>&nbsp &nbsp The pareto front data. It's a 2D array of double (pf_size X obj_num).<div style="line-height:75%;"><br></div>
            <strong>pf_size: <i>int, default=None</i></strong><br/>&nbsp &nbsp The size of the pareto front <i>pf_data</i>.
        </td>
    </tr>
    <tr class="emoc_doc_table_title">
        <td rowspan="2" ALIGN="left" VALIGN="top"  class="emoc_doc_table_title"><strong class="wuhu">Returns:</strong></td>
    </tr>
    <tr >
        <td class="emoc_doc_table_content">
            <strong>gdplus_value: <i>double</i></strong><br/>&nbsp &nbsp Generational distance plus value of current population <i>pop</i>.
        </td>
    </tr>
    </tbody>
</table>

