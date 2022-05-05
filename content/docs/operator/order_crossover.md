---
weight: 5
bookFlatSection: false
title: "Order Crossover"
BookToC: false
---
# Order Crossover

*File position: **/EMOC/src/operator/order_crossover.h** and **/EMOC/src/operator/order_crossover.cpp***

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
**void OrderCrossover(Individual \*parent1, Individual \*parent2, Individual \*offspring1, Individual \*offspring2)**

{{< /hint >}}

</div>

Do the order crossover on `parent1` and `parent2`, the results are stored in `offspring1` and `offspring2`. Note this crossover is for permutation encoding problems.

<table class="emoc_doc_table" style="overflow-x: hidden">
    <tbody >
    <tr>
        <td rowspan="2" ALIGN="left" VALIGN="top"  class="emoc_doc_table_title"><strong class="wuhu">Parameter:</strong></td>
    </tr>
    <tr >
        <td class="emoc_doc_table_content">
           <strong>parent1: <i>Individual*, default=None</i></strong><br/>&nbsp &nbsp The pointer to the first parent individual to do order crossover.<div style="line-height:75%;"><br></div>
            <strong>parent2: <i>Individual*, default=None</i></strong><br/>&nbsp &nbsp The pointer to the second parent individual to do order crossover.<div style="line-height:75%;"><br></div>
            <strong>offspring1: <i>Individual*, default=None</i></strong><br/>&nbsp &nbsp The pointer to the first offspring individual of order crossover results. The memory of the offspring need to be allocated outside the function.<div style="line-height:75%;"><br></div>
            <strong>offspring2: <i>Individual*, default=None</i></strong><br/>&nbsp &nbsp The pointer to the second offspring individual of order crossover results. The memory of the offspring need to be allocated outside the function.
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

