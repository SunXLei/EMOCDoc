---
weight: 1
bookFlatSection: false
title: "Tournament Selection"
BookToC: false
---
# Tournament Selection

*File position: **/EMOC/src/operator/tournament_selection.h** and **/EMOC/src/operator/tournament_selection.cpp***

<style>
    .emoc_doc_table_title{
        background-color:#F0F7FA;
    }
    .emoc_doc_table_content{
        background-color:#FFFFFF;
        width:100%;
    }
</style>

There are three tournament selection variants in EMOC：

- [Individual* TournamentByRank(Individual* ind1, Individual* ind2)]({{< relref "#TournamentByRank" >}})

- [Individual* TournamentByFitness(Individual* ind1, Individual* ind2, int greater_is_better = 0)]({{< relref "#TournamentByFitness" >}})

- [Individual* TournamentByCustom(Individual* ind1, double ind1_prop, Individual* ind2, double ind2_prop, int greater_is_better = 0)]({{< relref "#TournamentByCustom" >}})


<div id="TournamentByRank">

{{< hint warning>}}
**Individual\* TournamentByRank(Individual\* ind1, Individual\* ind2)**

{{< /hint >}}

</div>

Use the non-dominated sorting results (i.e., the `rank_` variable of `Individual` object) to complete the tournament selection.

<table class="emoc_doc_table" style="overflow-x: hidden">
    <tbody >
    <tr>
        <td rowspan="2" ALIGN="left" VALIGN="top"  class="emoc_doc_table_title"><strong class="wuhu">Parameter:</strong></td>
    </tr>
    <tr >
        <td class="emoc_doc_table_content">
           <strong>ind1: <i>Individual*, default=None</i></strong><br/>&nbsp &nbsp The pointer to the first individual which will participate the tournament selection.<div style="line-height:75%;"><br></div>
            <strong>ind2: <i>Individual*, default=None</i></strong><br/>&nbsp &nbsp The pointer to the second individual which will participate the tournament selection.
        </td>
    </tr>
    <tr class="emoc_doc_table_title">
        <td rowspan="2" ALIGN="left" VALIGN="top"  class="emoc_doc_table_title"><strong class="wuhu">Returns:</strong></td>
    </tr>
    <tr >
        <td class="emoc_doc_table_content">
            <strong>winner: <i>Individual*</i></strong><br/>&nbsp &nbsp The pointer to the individual which win the tournament.
        </td>
    </tr>
    </tbody>
</table>



<div id="TournamentByFitness">

{{< hint warning>}}
**Individual\* TournamentByFitness(Individual\* ind1, Individual\* ind2, int greater_is_better = 0)**

{{< /hint >}}

</div>

Use the the `fitness_` variable of `Individual` object to complete the tournament selection.

<table class="emoc_doc_table" style="overflow-x: hidden">
    <tbody >
    <tr>
        <td rowspan="2" ALIGN="left" VALIGN="top"  class="emoc_doc_table_title"><strong class="wuhu">Parameter:</strong></td>
    </tr>
    <tr >
        <td class="emoc_doc_table_content">
           <strong>ind1: <i>Individual*, default=None</i></strong><br/>&nbsp &nbsp The pointer to the first individual which will participate the tournament selection.<div style="line-height:75%;"><br></div>
           <strong>ind2: <i>Individual*, default=None</i></strong><br/>&nbsp &nbsp The pointer to the second individual which will participate the tournament selection.<div style="line-height:75%;"><br></div>
           <strong>greater_is_better: <i>int, default=0</i></strong><br/>&nbsp &nbsp Whether the larger fitness the better. By default it's the smaller the better.
        </td>
    </tr>
    <tr class="emoc_doc_table_title">
        <td rowspan="2" ALIGN="left" VALIGN="top"  class="emoc_doc_table_title"><strong class="wuhu">Returns:</strong></td>
    </tr>
    <tr >
        <td class="emoc_doc_table_content">
            <strong>winner: <i>Individual*</i></strong><br/>&nbsp &nbsp The pointer to the individual which win the tournament.
        </td>
    </tr>
    </tbody>
</table>



<div id="TournamentByCustom">

{{< hint warning>}}
**Individual\* TournamentByCustom(Individual\* ind1, double ind1_prop, Individual\* ind2, double ind2_prop, int greater_is_better = 0)**

{{< /hint >}}

</div>

Use the the custom properties of `Individual` object to complete the tournament selection.

<table class="emoc_doc_table" style="overflow-x: hidden">
    <tbody >
    <tr>
        <td rowspan="2" ALIGN="left" VALIGN="top"  class="emoc_doc_table_title"><strong class="wuhu">Parameter:</strong></td>
    </tr>
    <tr >
        <td class="emoc_doc_table_content">
           <strong>ind1: <i>Individual*, default=None</i></strong><br/>&nbsp &nbsp The pointer to the first individual which will participate the tournament selection.<div style="line-height:75%;"><br></div>
           <strong>ind1_prop: <i>double, default=None</i></strong><br/>&nbsp &nbsp The custom property of the first individual<div style="line-height:75%;"><br></div>
           <strong>ind2: <i>Individual*, default=None</i></strong><br/>&nbsp &nbsp The pointer to the second individual which will participate the tournament selection.<div style="line-height:75%;"><br></div>
           <strong>ind2_prop: <i>double, default=None</i></strong><br/>&nbsp &nbsp The custom property of the second individual<div style="line-height:75%;"><br></div>
           <strong>greater_is_better: <i>int, default=0</i></strong><br/>&nbsp &nbsp Whether the larger fitness the better. By default it's the smaller the better.
        </td>
    </tr>
    <tr class="emoc_doc_table_title">
        <td rowspan="2" ALIGN="left" VALIGN="top"  class="emoc_doc_table_title"><strong class="wuhu">Returns:</strong></td>
    </tr>
    <tr >
        <td class="emoc_doc_table_content">
            <strong>winner: <i>Individual*</i></strong><br/>&nbsp &nbsp The pointer to the individual which win the tournament.
        </td>
    </tr>
    </tbody>
</table>

