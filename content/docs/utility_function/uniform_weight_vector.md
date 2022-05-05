---
weight: 2
bookFlatSection: false
title: "Uniform Weight Vector Generation"
BookToC: false
---
# Uniform Weight Vector Generation

*File position: **/EMOC/src/core/uniform_point.h** and **/EMOC/src/core/uniform_point.cpp***

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
**double\*\* UniformPoint(int num, int\* weight_num, int obj_num)**

{{< /hint >}}

</div>

Generate uniform weight vectors.

<table class="emoc_doc_table" style="overflow-x: hidden">
    <tbody >
    <tr>
        <td rowspan="2" ALIGN="left" VALIGN="top"  class="emoc_doc_table_title"><strong class="wuhu">Parameter:</strong></td>
    </tr>
    <tr >
        <td class="emoc_doc_table_content">
           <strong>num: <i>int, default=None</i></strong><br/>&nbsp &nbsp Number of uniform weight vectors want to generate.<div style="line-height:75%;"><br></div>
            <strong>weight_num: <i>int*, default=None</i></strong><br/>&nbsp &nbsp The real number of generated weight vectors.<div style="line-height:75%;"><br></div>
            <strong>obj_num: <i>int, default=None</i></strong><br/>&nbsp &nbsp The dimension of generated weight vectors.
        </td>
    </tr>
    <tr class="emoc_doc_table_title">
        <td rowspan="2" ALIGN="left" VALIGN="top"  class="emoc_doc_table_title"><strong class="wuhu">Returns:</strong></td>
    </tr>
    <tr >
        <td class="emoc_doc_table_content">
            <strong>lambda: <i>double**</i></strong><br/>&nbsp &nbsp Generated uniform weight vectors. It's a 2D array of double with the size <i>weight_num</i> X <i>obj_num</i>.
        </td>
    </tr>
    </tbody>
</table>

