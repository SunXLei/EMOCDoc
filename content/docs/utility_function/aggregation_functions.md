---
weight: 3
bookFlatSection: false
title: "Aggregation Functions"
BookToC: false
---
# Aggregation Functions

*File position: **/EMOC/src/core/utility.h** and **/EMOC/src/core/utility.cpp***

<style>
    .emoc_doc_table_title{
        background-color:#F0F7FA;
    }
    .emoc_doc_table_content{
        background-color:#FFFFFF;
        width:100%;
    }
</style>

There are several aggregation functions for decomposition:

- [double CalWeightedSum(Individual *ind, double *weight_vector, double *ideal_point, int obj_num)]({{< relref "#CalWeightedSum" >}})

- [double CalInverseChebycheff(Individual *ind, double *weight_vector, double *ideal_point, int obj_num)]({{< relref "#CalInverseChebycheff" >}})

- [double CalPBI(Individual *ind, double *weight_vector, double *ideal_point, int obj_num, double theta)]({{< relref "#CalPBI" >}})

<div id="CalWeightedSum">

{{< hint warning>}}
**double CalWeightedSum(Individual \*ind, double \*weight_vector, double \*ideal_point, int obj_num)**

{{< /hint >}}

</div>

Use weighted sum method  to decompose the individual `ind` based on weight vector `weight_vector`.

<table class="emoc_doc_table" style="overflow-x: hidden">
    <tbody >
    <tr>
        <td rowspan="2" ALIGN="left" VALIGN="top"  class="emoc_doc_table_title"><strong class="wuhu">Parameter:</strong></td>
    </tr>
    <tr >
        <td class="emoc_doc_table_content">
           <strong>ind: <i>Individual*, default=None</i></strong><br/>&nbsp &nbsp The pointer to the individual which will be decomposed.<div style="line-height:75%;"><br></div>
           <strong>weight_vector: <i>double*, default=None</i></strong><br/>&nbsp &nbsp The weight vector for decomposition. It's a 1D array of double.<div style="line-height:75%;"><br></div>
           <strong>obj_num: <i>int, default=None</i></strong><br/>&nbsp &nbsp The number of objectives.
        </td>
    </tr>
    <tr class="emoc_doc_table_title">
        <td rowspan="2" ALIGN="left" VALIGN="top"  class="emoc_doc_table_title"><strong class="wuhu">Returns:</strong></td>
    </tr>
    <tr >
        <td class="emoc_doc_table_content">
            <strong>weighted_sum: <i>double</i></strong><br/>&nbsp &nbsp The decomposition value with the weighted sum method.
        </td>
    </tr>
    </tbody>
</table>



<div id="CalInverseChebycheff">

{{< hint warning>}}
**double CalInverseChebycheff(Individual \*ind, double \*weight_vector, double \*ideal_point, int obj_num)**

{{< /hint >}}

</div>

Use inverse chebycheff method to decompose the individual `ind` based on weight vector `weight_vector`.

<table class="emoc_doc_table" style="overflow-x: hidden">
    <tbody >
    <tr>
        <td rowspan="2" ALIGN="left" VALIGN="top"  class="emoc_doc_table_title"><strong class="wuhu">Parameter:</strong></td>
    </tr>
    <tr >
        <td class="emoc_doc_table_content">
           <strong>ind: <i>Individual*, default=None</i></strong><br/>&nbsp &nbsp The pointer to the individual which will be decomposed.<div style="line-height:75%;"><br></div>
           <strong>weight_vector: <i>double*, default=None</i></strong><br/>&nbsp &nbsp The weight vector for decomposition. It's a 1D array of double.<div style="line-height:75%;"><br></div>
           <strong>ideal_point: <i>double*, default=None</i></strong><br/>&nbsp &nbsp The ideal point of current population. It's a 1D array of double.<div style="line-height:75%;"><br></div>
           <strong>obj_num: <i>int, default=None</i></strong><br/>&nbsp &nbsp The number of objectives.
        </td>
    </tr>
    <tr class="emoc_doc_table_title">
        <td rowspan="2" ALIGN="left" VALIGN="top"  class="emoc_doc_table_title"><strong class="wuhu">Returns:</strong></td>
    </tr>
    <tr >
        <td class="emoc_doc_table_content">
            <strong>inverse_chebycheff: <i>double</i></strong><br/>&nbsp &nbsp The decomposition value with the inverse chebycheff method.
        </td>
    </tr>
    </tbody>
</table>



<div id="CalPBI">

{{< hint warning>}}
**double CalPBI(Individual \*ind, double \*weight_vector, double \*ideal_point, int obj_num, double theta)**

{{< /hint >}}

</div>

Use penalty-based boundary intersection method to decompose the individual `ind` based on weight vector `weight_vector`.

<table class="emoc_doc_table" style="overflow-x: hidden">
    <tbody >
    <tr>
        <td rowspan="2" ALIGN="left" VALIGN="top"  class="emoc_doc_table_title"><strong class="wuhu">Parameter:</strong></td>
    </tr>
    <tr >
        <td class="emoc_doc_table_content">
           <strong>ind: <i>Individual*, default=None</i></strong><br/>&nbsp &nbsp The pointer to the individual which will be decomposed.<div style="line-height:75%;"><br></div>
           <strong>weight_vector: <i>double*, default=None</i></strong><br/>&nbsp &nbsp The weight vector for decomposition. It's a 1D array of double.<div style="line-height:75%;"><br></div>
           <strong>ideal_point: <i>double*, default=None</i></strong><br/>&nbsp &nbsp The ideal point of current population. It's a 1D array of double.<div style="line-height:75%;"><br></div>
           <strong>obj_num: <i>int, default=None</i></strong><br/>&nbsp &nbsp The number of objectives.<div style="line-height:75%;"><br></div>
           <strong>theta: <i>double, default=None</i></strong><br/>&nbsp &nbsp The parameter of penalty-based boundary intersection method.
        </td>
    </tr>
    <tr class="emoc_doc_table_title">
        <td rowspan="2" ALIGN="left" VALIGN="top"  class="emoc_doc_table_title"><strong class="wuhu">Returns:</strong></td>
    </tr>
    <tr >
        <td class="emoc_doc_table_content">
            <strong>pbi: <i>double</i></strong><br/>&nbsp &nbsp The decomposition value with the penalty-based boundary intersection method.
        </td>
    </tr>
    </tbody>
</table>

