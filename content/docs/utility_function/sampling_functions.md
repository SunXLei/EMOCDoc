---
weight: 4
bookFlatSection: false
title: "Sampling Functions"
BookToC: true
---
# Sampling Functions

<style>
    .emoc_doc_table_title{
        background-color:#F0F7FA;
    }
    .emoc_doc_table_content{
        background-color:#FFFFFF;
        width:100%;
    }
</style>

## Random Number Generation

*File position: **/EMOC/vendor/random.h** and **/EMOC/vendor/random.cpp***

Random number generation is a basic function for evolutionary algorithm, EMOC provides several random number related functions as below:

- [double randomperc()]({{< relref "#randomperc" >}})
- [int rnd(int low, int high)]({{< relref "#rnd" >}})
- [double rndreal(double low, double high)]({{< relref "#rndreal" >}})

<div id="randomperc">

{{< hint warning>}}
**double randomperc()**

{{< /hint >}}

</div>

Fetch a single random number between 0.0 and 1.0.

<table class="emoc_doc_table" style="overflow-x: hidden">
    <tbody >
    <tr>
        <td rowspan="2" ALIGN="left" VALIGN="top"  class="emoc_doc_table_title"><strong class="wuhu">Parameter:</strong></td>
    </tr>
    <tr >
        <td class="emoc_doc_table_content">
            <strong>void</strong>
        </td>
    </tr>
    <tr class="emoc_doc_table_title">
        <td rowspan="2" ALIGN="left" VALIGN="top"  class="emoc_doc_table_title"><strong class="wuhu">Returns:</strong></td>
    </tr>
    <tr >
        <td class="emoc_doc_table_content">
              <strong>rand: <i>double</i></strong><br/>&nbsp &nbsp A random number between 0.0 and 1.0.
        </td>
    </tr>
    </tbody>
</table>

<div id="rnd">

{{< hint warning>}}
**int rnd(int low, int high)**

{{< /hint >}}

</div>

Return a random integer between `low` and `high`.

<table class="emoc_doc_table" style="overflow-x: hidden">
    <tbody >
    <tr>
        <td rowspan="2" ALIGN="left" VALIGN="top"  class="emoc_doc_table_title"><strong class="wuhu">Parameter:</strong></td>
    </tr>
    <tr >
        <td class="emoc_doc_table_content">
           <strong>low: <i>int, default=None</i></strong><br/>&nbsp &nbsp Lower boundary of random integer.<div style="line-height:75%;"><br></div>
           <strong>high: <i>int, default=None</i></strong><br/>&nbsp &nbsp Upper boundary of random integer.
        </td>
    </tr>
    <tr class="emoc_doc_table_title">
        <td rowspan="2" ALIGN="left" VALIGN="top"  class="emoc_doc_table_title"><strong class="wuhu">Returns:</strong></td>
    </tr>
    <tr >
        <td class="emoc_doc_table_content">
            <strong>rand: <i>double</i></strong><br/>&nbsp &nbsp A random integer between low and high.
        </td>
    </tr>
    </tbody>
</table>



<div id="rndreal">

{{< hint warning>}}
**double rndreal(double low, double high)**

{{< /hint >}}

</div>

Return a random real number between `low` and `high`.

<table class="emoc_doc_table" style="overflow-x: hidden">
    <tbody >
    <tr>
        <td rowspan="2" ALIGN="left" VALIGN="top"  class="emoc_doc_table_title"><strong class="wuhu">Parameter:</strong></td>
    </tr>
    <tr >
        <td class="emoc_doc_table_content">
           <strong>low: <i>double, default=None</i></strong><br/>&nbsp &nbsp Lower boundary of random double.<div style="line-height:75%;"><br></div>
           <strong>high: <i>double, default=None</i></strong><br/>&nbsp &nbsp Upper boundary of random double.
        </td>
    </tr>
    <tr class="emoc_doc_table_title">
        <td rowspan="2" ALIGN="left" VALIGN="top"  class="emoc_doc_table_title"><strong class="wuhu">Returns:</strong></td>
    </tr>
    <tr >
        <td class="emoc_doc_table_content">
            <strong>rand: <i>double</i></strong><br/>&nbsp &nbsp A random double between low and high.
        </td>
    </tr>
    </tbody>
</table>





## Sampling from Distribution

*File position: **/EMOC/src/core/utility.h** and **/EMOC/src/core/utility.cpp***

There are also some sampling function for different distribution:

- [double CauchyRandom(double location, double scale)]({{< relref "#CauchyRandom" >}})

- [double BetaRandom(double a, double b)]({{< relref "#BetaRandom" >}})

- [double GaussianRandom(double mean, double stdev)]({{< relref "#GaussianRandom" >}})

<div id="CauchyRandom">

{{< hint warning>}}
**double CauchyRandom(double location, double scale)**

{{< /hint >}}

</div>

Return a sample value subject to Cauchy distribution.

<table class="emoc_doc_table" style="overflow-x: hidden">
    <tbody >
    <tr>
        <td rowspan="2" ALIGN="left" VALIGN="top"  class="emoc_doc_table_title"><strong class="wuhu">Parameter:</strong></td>
    </tr>
    <tr >
        <td class="emoc_doc_table_content">
           <strong>location: <i>double, default=None</i></strong><br/>&nbsp &nbsp The location parameter of Cauchy distribution.<div style="line-height:75%;"><br></div>
           <strong>scale: <i>double, default=None</i></strong><br/>&nbsp &nbsp The scale parameter of Cauchy distribution.
        </td>
    </tr>
    <tr class="emoc_doc_table_title">
        <td rowspan="2" ALIGN="left" VALIGN="top"  class="emoc_doc_table_title"><strong class="wuhu">Returns:</strong></td>
    </tr>
    <tr >
        <td class="emoc_doc_table_content">
            <strong>sample: <i>double</i></strong><br/>&nbsp &nbsp A random sample from Cauchy distribution.
        </td>
    </tr>
    </tbody>
</table>



<div id="BetaRandom">

{{< hint warning>}}
**double BetaRandom(double a, double b)**

{{< /hint >}}

</div>

Return a sample value subject to Beta distribution.

<table class="emoc_doc_table" style="overflow-x: hidden">
    <tbody >
    <tr>
        <td rowspan="2" ALIGN="left" VALIGN="top"  class="emoc_doc_table_title"><strong class="wuhu">Parameter:</strong></td>
    </tr>
    <tr >
        <td class="emoc_doc_table_content">
           <strong>a: <i>double, default=None</i></strong><br/>&nbsp &nbsp The alpha parameter of Beta distribution.<div style="line-height:75%;"><br></div>
           <strong>b: <i>double, default=None</i></strong><br/>&nbsp &nbsp The beta parameter of Beta distribution.
        </td>
    </tr>
    <tr class="emoc_doc_table_title">
        <td rowspan="2" ALIGN="left" VALIGN="top"  class="emoc_doc_table_title"><strong class="wuhu">Returns:</strong></td>
    </tr>
    <tr >
        <td class="emoc_doc_table_content">
            <strong>sample: <i>double</i></strong><br/>&nbsp &nbsp A random sample from Beta distribution.
        </td>
    </tr>
    </tbody>
</table>



<div id="GaussianRandom">

{{< hint warning>}}
**double GaussianRandom(double mean, double stdev)**

{{< /hint >}}

</div>

Return a sample value subject to Gaussian distribution.

<table class="emoc_doc_table" style="overflow-x: hidden">
    <tbody >
    <tr>
        <td rowspan="2" ALIGN="left" VALIGN="top"  class="emoc_doc_table_title"><strong class="wuhu">Parameter:</strong></td>
    </tr>
    <tr >
        <td class="emoc_doc_table_content">
           <strong>mean: <i>double, default=None</i></strong><br/>&nbsp &nbsp The mean parameter of Gaussian distribution.<div style="line-height:75%;"><br></div>
           <strong>stdev: <i>double, default=None</i></strong><br/>&nbsp &nbsp The standard deviation parameter of Gaussian distribution.
        </td>
    </tr>
    <tr class="emoc_doc_table_title">
        <td rowspan="2" ALIGN="left" VALIGN="top"  class="emoc_doc_table_title"><strong class="wuhu">Returns:</strong></td>
    </tr>
    <tr >
        <td class="emoc_doc_table_content">
            <strong>sample: <i>double</i></strong><br/>&nbsp &nbsp A random sample from Gaussian distribution.
        </td>
    </tr>
    </tbody>
</table>

