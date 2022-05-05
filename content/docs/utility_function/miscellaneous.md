---
weight: 6
bookFlatSection: false
title: "Miscellaneous"
BookToC: true
---
## Ideal Point and Nadir Point Update

<style>
    .emoc_doc_table_title{
        background-color:#F0F7FA;
    }
    .emoc_doc_table_content{
        background-color:#FFFFFF;
        width:100%;
    }
</style>

*File position: **/EMOC/src/core/utility.h** and **/EMOC/src/core/utility.cpp***

- [void UpdateIdealpoint(Individual *ind, double *ideal_point, int obj_num)]({{< relref "#UpdateIdealpoint" >}})
- [void UpdateNadirpoint(Individual *ind, double *nadir_point, int obj_num)]({{< relref "#UpdateNadirpoint" >}})

<div id="UpdateIdealpoint">

{{< hint warning>}}
**void UpdateIdealpoint(Individual \*ind, double \*ideal_point, int obj_num)**

{{< /hint >}}

</div>

Update the ideal point `ideal_point` with given individual `ind`.

<table class="emoc_doc_table" style="overflow-x: hidden">
    <tbody >
    <tr>
        <td rowspan="2" ALIGN="left" VALIGN="top"  class="emoc_doc_table_title"><strong class="wuhu">Parameter:</strong></td>
    </tr>
    <tr >
        <td class="emoc_doc_table_content">
           <strong>ind: <i>Individual*, default=None</i></strong><br/>&nbsp &nbsp The pointer to the given individual.<div style="line-height:75%;"><br></div>
           <strong>ideal_point: <i>double*, default=None</i></strong><br/>&nbsp &nbsp The pointer to the ideal point which will be updated. It's a 1D array of double.<div style="line-height:75%;"><br></div>
           <strong>obj_num: <i>int, default=None</i></strong><br/>&nbsp &nbsp The number of objectives.
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



<div id="UpdateNadirpoint">

{{< hint warning>}}
**void UpdateNadirpoint(Individual \*ind, double \*nadir_point, int obj_num)**

{{< /hint >}}

</div>

Update the ideal point `nadir_point` with given individual `ind`.

<table class="emoc_doc_table" style="overflow-x: hidden">
    <tbody >
    <tr>
        <td rowspan="2" ALIGN="left" VALIGN="top"  class="emoc_doc_table_title"><strong class="wuhu">Parameter:</strong></td>
    </tr>
    <tr >
        <td class="emoc_doc_table_content">
           <strong>ind: <i>Individual*, default=None</i></strong><br/>&nbsp &nbsp The pointer to the given individual.<div style="line-height:75%;"><br></div>
           <strong>ideal_point: <i>double*, default=None</i></strong><br/>&nbsp &nbsp The pointer to the nadir point which will be updated. It's a 1D array of double.<div style="line-height:75%;"><br></div>
           <strong>obj_num: <i>int, default=None</i></strong><br/>&nbsp &nbsp The number of objectives.
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



## Statistic Test

*File position: **/EMOC/src/core/utility.h** and **/EMOC/src/core/utility.cpp***

- [int RankSumTest(const std::vector\<double\>& array1, const std::vector\<double\>& array2)]({{< relref "#RankSumTest" >}})
- [int SignRankTest(const std::vector\<double\>& array1, const std::vector\<double\>& array2)]({{< relref "#SignRankTest" >}})



<div id="RankSumTest">

{{< hint warning>}}
**int RankSumTest(const std::vector\<double\>& array1, const std::vector\<double\>& array2)**

{{< /hint >}}

</div>

Do the ranksum test between the two given arrays.

<table class="emoc_doc_table" style="overflow-x: hidden">
    <tbody >
    <tr>
        <td rowspan="2" ALIGN="left" VALIGN="top"  class="emoc_doc_table_title"><strong class="wuhu">Parameter:</strong></td>
    </tr>
    <tr >
        <td class="emoc_doc_table_content">
           <strong>array1: <i>std::vector&ltdouble&gt, default=None</i></strong><br/>&nbsp &nbsp The first array which will attend ranksum test.<div style="line-height:75%;"><br></div>
            <strong>array2: <i>std::vector&ltdouble&gt, default=None</i></strong><br/>&nbsp &nbsp The second array which will attend ranksum test.
        </td>
    </tr>
    <tr class="emoc_doc_table_title">
        <td rowspan="2" ALIGN="left" VALIGN="top"  class="emoc_doc_table_title"><strong class="wuhu">Returns:</strong></td>
    </tr>
    <tr >
        <td class="emoc_doc_table_content">
            <strong>res: <i>int</i></strong><br/>&nbsp &nbsp The result of ranksum test. 0 means no significant difference and 1 means has significant difference with 5% significance level.
        </td>
    </tr>
    </tbody>
</table>



<div id="SignRankTest">

{{< hint warning>}}
**int SignRankTest(const std::vector\<double\>& array1, const std::vector\<double\>& array2)**

{{< /hint >}}

</div>

Do the sign rank test between the two given arrays.

<table class="emoc_doc_table" style="overflow-x: hidden">
    <tbody >
    <tr>
        <td rowspan="2" ALIGN="left" VALIGN="top"  class="emoc_doc_table_title"><strong class="wuhu">Parameter:</strong></td>
    </tr>
    <tr >
        <td class="emoc_doc_table_content">
           <strong>array1: <i>std::vector&ltdouble&gt, default=None</i></strong><br/>&nbsp &nbsp The first array which will attend sign rank test.<div style="line-height:75%;"><br></div>
            <strong>array2: <i>std::vector&ltdouble&gt, default=None</i></strong><br/>&nbsp &nbsp The second array which will attend sign rank test.
        </td>
    </tr>
    <tr class="emoc_doc_table_title">
        <td rowspan="2" ALIGN="left" VALIGN="top"  class="emoc_doc_table_title"><strong class="wuhu">Returns:</strong></td>
    </tr>
    <tr >
        <td class="emoc_doc_table_content">
            <strong>res: <i>int</i></strong><br/>&nbsp &nbsp The result of sign rank test. 0 means no significant difference and 1 means has significant difference with 5% significance level.
        </td>
    </tr>
    </tbody>
</table>

