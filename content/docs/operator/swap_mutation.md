---
weight: 8
bookFlatSection: false
title: "Swap Mutation"
BookToC: false
---
# Swap Mutation

*File position: **/EMOC/src/operator/swap_mutation.h** and **/EMOC/src/operator/swap_mutation.cpp***

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
**void SwapMutation(Individual \*ind, MutationParameter &mutation_para)**

{{< /hint >}}

</div>

Do the swap mutation on `ind`. The mutation results are stored in itself. Note this mutation is for permutation encoding problems.

<table class="emoc_doc_table" style="overflow-x: hidden">
    <tbody >
    <tr>
        <td rowspan="2" ALIGN="left" VALIGN="top"  class="emoc_doc_table_title"><strong class="wuhu">Parameter:</strong></td>
    </tr>
    <tr >
        <td class="emoc_doc_table_content">
            <strong>ind: <i>Individual*, default=None</i></strong><br/>&nbsp &nbsp The pointer to the individual which will do the swap mutation.<div style="line-height:75%;"><br></div>
            <strong>mutation_para: <i>MutationParameter, default=None</i></strong><br/>&nbsp &nbsp The parameter of this mutation. The type <i>MutationParameter</i> is just a simple structure which has three member variables (i.e., the mutation probability, the distribution index1 and the distribution index2).
        </td>
    </tr>
    <tr class="emoc_doc_table_title">
        <td rowspan="2" ALIGN="left" VALIGN="top"  class="emoc_doc_table_title"><strong class="wuhu">Returns:</strong></td>
    </tr>
    <tr >
        <td class="emoc_doc_table_content">
            <strong>void</strong><br/>
        </td>
    </tr>
    </tbody>
</table>

