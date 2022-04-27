---
weight: 3
bookFlatSection: false
title: "Problem"
BookToC: false
---

# Problem Class

*File position: **/EMOC/src/problem/problem.h** and **/EMOC/src/problem/problem.cpp***

{{< hint info>}}
**class Problem(dec_num, obj_num)**

{{< /hint >}}

The parent class of all test problems in EMOC.

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
            <strong>dec_num:<i>int, default=None</i></strong><br/>&nbsp &nbsp The number of decision variables setting for the problem.<div style="line-height:75%;"><br></div>
            <strong>obj_num:<i>int, default=None</i></strong><br/>&nbsp &nbsp The number of objective functions setting for the problem.<br/>
        </td>
    </tr>
    <tr class="emoc_doc_table_title">
        <td rowspan="2" ALIGN="left" VALIGN="top"  class="emoc_doc_table_title"><strong class="wuhu">Member variables:</strong></td>
    </tr>
    <tr >
        <td class="emoc_doc_table_content">
            <strong><i>(public)</i> dec_num_:<i>int</i></strong><br/>&nbsp &nbsp Decision variables of this individual. The size of this <i>std::vector</i> is dec_num. <div style="line-height:75%;"><br></div>
            <strong><i>(public)</i> obj_num_:<i>int</i></strong><br/>&nbsp &nbsp Objectives of this individual. The size of this <i>std::vector</i> is obj_num.<div style="line-height:75%;"><br></div>
            <strong><i>(public)</i> lower_bound_:<i>std::vector&ltdouble&gt</i></strong><br/>&nbsp &nbsp Constraints of this individual. The size of this <i>std::vector</i> is obj_num.<div style="line-height:75%;"><br></div>
            <strong><i>(public)</i> upper_bound_:<i>std::vector&ltdouble&gt</i></strong><br/>&nbsp &nbsp Constraints of this individual. The size of this <i>std::vector</i> is obj_num.<div style="line-height:75%;"><br></div>
            <strong><i>(public)</i> encoding_:<i>EncodingType</i></strong><br/>&nbsp &nbsp The rank index of this individual in the non-dominated sort (NDS) results of current population. <i>Rank 0</i> represents the first front in NDS.<br/>
        </td>
    </tr>
    </tbody>
</table>

<br/>

**Public Methods:**

- [void CalObj(Individual\* ind)]({{< relref "#CalObj" >}})
- [void CalCon(Individual\* ind)]({{< relref "#CalCon" >}})



<div id="CalObj">

{{< hint warning>}}
**void CalObj(Individual\* ind)**

{{< /hint >}}

</div>

Calculate the objective function values.

<table class="emoc_doc_table" style="overflow-x: hidden">
    <tbody>
    <tr>
        <td rowspan="2" ALIGN="left" VALIGN="top"  class="emoc_doc_table_title"><strong class="wuhu">Parameter:</strong></td>
    </tr>
    <tr>
        <td class="emoc_doc_table_content">
            <strong>ind:<i>Individual*, default=None</i></strong><br/>&nbsp &nbsp Pointer to the individual which need to calculate the objectives.
        </td>
    </tr>
    <tr class="emoc_doc_table_title">
        <td rowspan="2" ALIGN="left" VALIGN="top"  class="emoc_doc_table_title"><strong class="wuhu">Returns:</strong></td>
    </tr>
    <tr >
        <td class="emoc_doc_table_content">
			<br/>
        </td>
    </tr>
    </tbody>
</table>



<div id="CalCon">

{{< hint warning>}}
**void CalCon(Individual\* ind)**

{{< /hint >}}

</div>

Calculate the constraint function values.

<table class="emoc_doc_table" style="overflow-x: hidden">
    <tbody>
    <tr>
        <td rowspan="2" ALIGN="left" VALIGN="top"  class="emoc_doc_table_title"><strong class="wuhu">Parameter:</strong></td>
    </tr>
    <tr>
        <td class="emoc_doc_table_content" >
            <strong>ind:<i>Individual*, default=None</i></strong><br/>&nbsp &nbsp Pointer to the individual which need to calculate the constraints.
        </td>
    </tr>
    <tr class="emoc_doc_table_title">
        <td rowspan="2" ALIGN="left" VALIGN="top"  class="emoc_doc_table_title"><strong class="wuhu">Returns:</strong></td>
    </tr>
    <tr >
        <td class="emoc_doc_table_content">
            <br/>
        </td>
    </tr>
    </tbody>
</table>