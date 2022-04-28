---
weight: 2
bookFlatSection: false
title: "Individual"
BookToC: false
---

# Individual Class


*File position: **/EMOC/src/core/individual.h** and **/EMOC/src/core/individual.cpp***

{{< hint info>}}
**class Individual(int dec_num, int obj_num)**

{{< /hint >}}

The class for each individual in the population.

<style>
    .emoc_doc_table_title{
        background-color:#F0F7FA;
    }
    .emoc_doc_table_content{
        background-color:#FFFFFF;
        width:100%;
    }
</style>

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
            <strong><i>(public)</i> dec_: <i>std::vector&ltdouble&gt</i></strong><br/>&nbsp &nbsp Decision variables of this individual. The size of this <i>std::vector</i> is dec_num. <div style="line-height:75%;"><br></div>
            <strong><i>(public)</i> obj_: <i>std::vector&ltdouble&gt</i></strong><br/>&nbsp &nbsp Objectives of this individual. The size of this <i>std::vector</i> is obj_num.<div style="line-height:75%;"><br></div>
            <strong><i>(public)</i> con_: <i>std::vector&ltdouble&gt</i></strong><br/>&nbsp &nbsp Constraints of this individual. The size of this <i>std::vector</i> is obj_num.<div style="line-height:75%;"><br></div>
            <strong><i>(public)</i> fitness_: <i>double</i></strong><br/>&nbsp &nbsp The fitness of this individual.<div style="line-height:75%;"><br></div>
            <strong><i>(public)</i> rank_: <i>int</i></strong><br/>&nbsp &nbsp The rank index of this individual in the non-dominated sort (NDS) results of current population. <i>Rank 0</i> represents the first front in NDS.
        </td>
    </tr>
    </tbody>
</table>

