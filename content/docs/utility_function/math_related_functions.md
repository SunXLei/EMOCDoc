---
weight: 5
bookFlatSection: false
title: "Math Related Functions"
BookToC: false
---
# Math Related Functions

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

In EMOC, some mathematic operations are also provided for convenience:

- [int Combination(int n, int k)]({{< relref "#Combination" >}})

- [double CalculateCos(double *a, double *b, int dimension)]({{< relref "#CalculateCos" >}})

- [double CalculateSin(double *a, double *b, int dimension)]({{< relref "#CalculateSin" >}})

- [double CalculateNorm(double *vector, int dimension)]({{< relref "#CalculateNorm" >}})

- [double CalculateDotProduct(double *vector1, double *vector2, int dimension)]({{< relref "#CalculateDotProduct" >}})

- [double CalEuclidianDistance(double* a, double* b, int dimension)]({{< relref "#CalEuclidianDistance" >}})

- [double CalPerpendicularDistance(double* a, double* b, int dimension)]({{< relref "#CalPerpendicularDistance" >}})

  



<div id="Combination">

{{< hint warning>}}
**int Combination(int n, int k)**

{{< /hint >}}

</div>

Return the combination number with the given parameters.

<table class="emoc_doc_table" style="overflow-x: hidden">
    <tbody >
    <tr>
        <td rowspan="2" ALIGN="left" VALIGN="top"  class="emoc_doc_table_title"><strong class="wuhu">Parameter:</strong></td>
    </tr>
    <tr >
        <td class="emoc_doc_table_content">
           <strong>n: <i>int, default=None</i></strong><br/>&nbsp &nbsp The number of total things.<div style="line-height:75%;"><br></div>
            <strong>k: <i>int, default=None</i></strong><br/>&nbsp &nbsp The number of things taken from the total <i>n</i> things.
        </td>
    </tr>
    <tr class="emoc_doc_table_title">
        <td rowspan="2" ALIGN="left" VALIGN="top"  class="emoc_doc_table_title"><strong class="wuhu">Returns:</strong></td>
    </tr>
    <tr >
        <td class="emoc_doc_table_content">
            <strong>combination: <i>double</i></strong><br/>&nbsp &nbsp Combination number.
        </td>
    </tr>
    </tbody>
</table>

<div id = "CalculateCos">

{{< hint warning>}}
**double CalculateCos(double \*a, double \*b, int dimension)**

{{< /hint >}}

</div>

Calculate the cosine value between two vectors.

<table class="emoc_doc_table" style="overflow-x: hidden">
    <tbody >
    <tr>
        <td rowspan="2" ALIGN="left" VALIGN="top"  class="emoc_doc_table_title"><strong class="wuhu">Parameter:</strong></td>
    </tr>
    <tr >
        <td class="emoc_doc_table_content">
           <strong>a: <i>double*, default=None</i></strong><br/>&nbsp &nbsp The first vector. It's a 1D array of double.<div style="line-height:75%;"><br></div>
           <strong>b: <i>double*, default=None</i></strong><br/>&nbsp &nbsp The second vector. It's a 1D array of double.<div style="line-height:75%;"><br></div>
           <strong>dimension: <i>int, default=None</i></strong><br/>&nbsp &nbsp The dimension of given vectors.
        </td>
    </tr>
    <tr class="emoc_doc_table_title">
        <td rowspan="2" ALIGN="left" VALIGN="top"  class="emoc_doc_table_title"><strong class="wuhu">Returns:</strong></td>
    </tr>
    <tr >
        <td class="emoc_doc_table_content">
            <strong>cos: <i>double</i></strong><br/>&nbsp &nbsp Cosine value between vector <i>a</i> and vector <i>b</i>.
        </td>
    </tr>
    </tbody>
</table>



<div id = "CalculateSin">

{{< hint warning>}}
**double CalculateSin(double \*a, double \*b, int dimension)**

{{< /hint >}}

</div>

Calculate the sine value between two vectors.

<table class="emoc_doc_table" style="overflow-x: hidden">
    <tbody >
    <tr>
        <td rowspan="2" ALIGN="left" VALIGN="top"  class="emoc_doc_table_title"><strong class="wuhu">Parameter:</strong></td>
    </tr>
    <tr >
        <td class="emoc_doc_table_content">
           <strong>a: <i>double*, default=None</i></strong><br/>&nbsp &nbsp The first vector. It's a 1D array of double.<div style="line-height:75%;"><br></div>
           <strong>b: <i>double*, default=None</i></strong><br/>&nbsp &nbsp The second vector. It's a 1D array of double.<div style="line-height:75%;"><br></div>
           <strong>dimension: <i>int, default=None</i></strong><br/>&nbsp &nbsp The dimension of given vectors.
        </td>
    </tr>
    <tr class="emoc_doc_table_title">
        <td rowspan="2" ALIGN="left" VALIGN="top"  class="emoc_doc_table_title"><strong class="wuhu">Returns:</strong></td>
    </tr>
    <tr >
        <td class="emoc_doc_table_content">
            <strong>sin: <i>double</i></strong><br/>&nbsp &nbsp Sine value between vector <i>a</i> and vector <i>b</i>.
        </td>
    </tr>
    </tbody>
</table>



<div id = "CalculateCos">

<div id = "CalculateNorm">

{{< hint warning>}}
**double CalculateNorm(double \*vector, int dimension)**

{{< /hint >}}

</div>

Calculate the norm of given vector.

<table class="emoc_doc_table" style="overflow-x: hidden">
    <tbody >
    <tr>
        <td rowspan="2" ALIGN="left" VALIGN="top"  class="emoc_doc_table_title"><strong class="wuhu">Parameter:</strong></td>
    </tr>
    <tr >
        <td class="emoc_doc_table_content">
           <strong>vector: <i>double*, default=None</i></strong><br/>&nbsp &nbsp The pointer to given vector. It's a 1D array of double.<div style="line-height:75%;"><br></div>
           <strong>dimension: <i>int, default=None</i></strong><br/>&nbsp &nbsp The dimension of given vector.
        </td>
    </tr>
    <tr class="emoc_doc_table_title">
        <td rowspan="2" ALIGN="left" VALIGN="top"  class="emoc_doc_table_title"><strong class="wuhu">Returns:</strong></td>
    </tr>
    <tr >
        <td class="emoc_doc_table_content">
            <strong>norm: <i>double</i></strong><br/>&nbsp &nbsp The norm of given vector.
        </td>
    </tr>
    </tbody>
</table>



<div id = "CalculateDotProduct">

{{< hint warning>}}
**double CalculateDotProduct(double \*vector1, double \*vector2, int dimension)**

{{< /hint >}}

</div>

Calculate the dot product between two vectors.

<table class="emoc_doc_table" style="overflow-x: hidden">
    <tbody >
    <tr>
        <td rowspan="2" ALIGN="left" VALIGN="top"  class="emoc_doc_table_title"><strong class="wuhu">Parameter:</strong></td>
    </tr>
    <tr >
        <td class="emoc_doc_table_content">
           <strong>vector1: <i>double*, default=None</i></strong><br/>&nbsp &nbsp The first vector. It's a 1D array of double.<div style="line-height:75%;"><br></div>
           <strong>vector2: <i>double*, default=None</i></strong><br/>&nbsp &nbsp The second vector. It's a 1D array of double.<div style="line-height:75%;"><br></div>
           <strong>dimension: <i>int, default=None</i></strong><br/>&nbsp &nbsp The dimension of given vectors.
        </td>
    </tr>
    <tr class="emoc_doc_table_title">
        <td rowspan="2" ALIGN="left" VALIGN="top"  class="emoc_doc_table_title"><strong class="wuhu">Returns:</strong></td>
    </tr>
    <tr >
        <td class="emoc_doc_table_content">
            <strong>sin: <i>double</i></strong><br/>&nbsp &nbsp Dot product between the two given vectors.
        </td>
    </tr>
    </tbody>
</table>



<div id = "CalEuclidianDistance">

{{< hint warning>}}
**double CalEuclidianDistance(double\* a, double\* b, int dimension)**

{{< /hint >}}

</div>

Calculate the euclidian distance between two vectors.

<table class="emoc_doc_table" style="overflow-x: hidden">
    <tbody >
    <tr>
        <td rowspan="2" ALIGN="left" VALIGN="top"  class="emoc_doc_table_title"><strong class="wuhu">Parameter:</strong></td>
    </tr>
    <tr >
        <td class="emoc_doc_table_content">
           <strong>a: <i>double*, default=None</i></strong><br/>&nbsp &nbsp The first vector. It's a 1D array of double.<div style="line-height:75%;"><br></div>
           <strong>b: <i>double*, default=None</i></strong><br/>&nbsp &nbsp The second vector. It's a 1D array of double.<div style="line-height:75%;"><br></div>
           <strong>dimension: <i>int, default=None</i></strong><br/>&nbsp &nbsp The dimension of given vectors.
        </td>
    </tr>
    <tr class="emoc_doc_table_title">
        <td rowspan="2" ALIGN="left" VALIGN="top"  class="emoc_doc_table_title"><strong class="wuhu">Returns:</strong></td>
    </tr>
    <tr >
        <td class="emoc_doc_table_content">
            <strong>distance: <i>double</i></strong><br/>&nbsp &nbsp The euclidian distance between two vectors.
        </td>
    </tr>
    </tbody>
</table>



<div id = "CalPerpendicularDistance">

{{< hint warning>}}
**double CalPerpendicularDistance(double\* a, double\* b, int dimension)**

{{< /hint >}}

</div>

Calculate the perpendicular distance between two vectors.

<table class="emoc_doc_table" style="overflow-x: hidden">
    <tbody >
    <tr>
        <td rowspan="2" ALIGN="left" VALIGN="top"  class="emoc_doc_table_title"><strong class="wuhu">Parameter:</strong></td>
    </tr>
    <tr >
        <td class="emoc_doc_table_content">
           <strong>a: <i>double*, default=None</i></strong><br/>&nbsp &nbsp The first vector. It's a 1D array of double.<div style="line-height:75%;"><br></div>
           <strong>b: <i>double*, default=None</i></strong><br/>&nbsp &nbsp The second vector. It's a 1D array of double.<div style="line-height:75%;"><br></div>
           <strong>dimension: <i>int, default=None</i></strong><br/>&nbsp &nbsp The dimension of given vectors.
        </td>
    </tr>
    <tr class="emoc_doc_table_title">
        <td rowspan="2" ALIGN="left" VALIGN="top"  class="emoc_doc_table_title"><strong class="wuhu">Returns:</strong></td>
    </tr>
    <tr >
        <td class="emoc_doc_table_content">
            <strong>perpendicular: <i>double</i></strong><br/>&nbsp &nbsp The euclidian distance between two vectors.
        </td>
    </tr>
    </tbody>
</table>

