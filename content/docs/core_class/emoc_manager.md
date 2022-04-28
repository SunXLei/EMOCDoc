---
weight: 6
bookFlatSection: false
title: "EMOCManager"
BookToC: false
---

# EMOCManager Class

*File position: **/EMOC/src/core/emoc_manager.h** and **/EMOC/src/core/emoc_manager.cpp***

{{< hint info>}}
**class EMOCManager()**

{{< /hint >}}

`EMOCManager` is the manager class of EMOC which controls the command mode and GUI mode. 

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
            <strong>void</strong>
        </td>
    </tr>
    <tr class="emoc_doc_table_title">
        <td rowspan="2" ALIGN="left" VALIGN="top"  class="emoc_doc_table_title"><strong class="wuhu">Member variables:</strong></td>
    </tr>
    <tr >
        <td class="emoc_doc_table_content">
            <strong><i>(private)</i> is_plot_: <i>bool</i></strong><br/>&nbsp &nbsp Whether to activate plot function. <div style="line-height:75%;"><br></div>
            <strong><i>(private)</i> is_gui_: <i>bool</i></strong><br/>&nbsp &nbsp Whether to enable gui mode.<div style="line-height:75%;"><br></div>
            <strong><i>(private)</i> is_experiment_: <i>bool</i></strong><br/>&nbsp &nbsp Whether in experiment module of gui mode.<div style="line-height:75%;"><br></div>
            <strong><i>(private)</i> is_test_pause_: <i>bool</i></strong><br/>&nbsp &nbsp Whether current run is paused in test module of gui mode.<div style="line-height:75%;"><br></div>
            <strong><i>(private)</i> is_test_finish_: <i>bool</i></strong><br/>&nbsp &nbsp Whether current run is finished in test module of gui mode. <div style="line-height:75%;"><br></div>
            <strong><i>(private)</i> is_experiment_pause_: <i>bool</i></strong><br/>&nbsp &nbsp Whether current run is finished in experiment module of gui mode. <div style="line-height:75%;"><br></div>
            <strong><i>(private)</i> is_experiment_finish_: <i>bool</i></strong><br/>&nbsp &nbsp Whether current run is finished in experiment module of gui mode. <div style="line-height:75%;"><br></div>
            <strong><i>(private)</i> g_GlobalSettingsArray: <i>std::vector&ltGlobal*&gt</i></strong><br/>&nbsp &nbsp An array of pointer to <i>Global</i>, it is reserved for different threads. The size of the vector is MAX_THREAD_NUM which is a macro definition in EMOC. By default the value is 128.<div style="line-height:75%;"><br></div>
        </td>
    </tr>
    </tbody>
</table>

**Note: Most of the private member variables can be set or got by the corresponding `Get` and `Set` functions. For more details, please check the source code.**

<br/>

**Public Methods:**

- [static EMOCManager* Instance()]({{< relref "#Instance" >}})
- [void Run()]({{< relref "#Run" >}})
- [void ExperimentModuleRun(std::vector<EMOCParameters> experiment_tasks, int thread_num)]({{< relref "#ExperimentModuleRun" >}})



<div id="Instance">

{{< hint warning>}}
**static EMOCManager\* Instance()**

{{< /hint >}}

</div>

Get the pointer to current EMOCManager object.

In EMOC, the EMOCManager class utilize the singleton design mode. So the object can be retrieved anywhere by `EMOCManager::Instance()` directly.

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
            <strong>s_Instance: <i>EMOCManager*</i></strong><br/>&nbsp &nbsp Pointer to the current EMOCManager object iteself.
			<br/>
        </td>
    </tr>
    </tbody>
</table>



<div id="Run">

{{< hint warning>}}
**void Run()**

{{< /hint >}}

</div>

The run function for command line mode in EMOC.

<table class="emoc_doc_table" style="overflow-x: hidden">
    <tbody>
    <tr>
        <td rowspan="2" ALIGN="left" VALIGN="top"  class="emoc_doc_table_title"><strong class="wuhu">Parameter:</strong></td>
    </tr>
    <tr>
        <td class="emoc_doc_table_content" >
            <strong>void</strong>
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



<div id="ExperimentModuleRun">

{{< hint warning>}}
**void ExperimentModuleRun(std::vector\<EMOCParameters\> experiment_tasks, int thread_num)**

{{< /hint >}}

</div>

The run function for experiment module of gui mode in EMOC.

<table class="emoc_doc_table" style="overflow-x: hidden">
    <tbody >
    <tr>
        <td rowspan="2" ALIGN="left" VALIGN="top"  class="emoc_doc_table_title"><strong class="wuhu">Parameter:</strong></td>
    </tr>
    <tr >
        <td class="emoc_doc_table_content">
            <strong>experiment_tasks: <i>std::vector&ltEMOCParameters&gt, default=None</i></strong><br/>&nbsp &nbsp All EMOC tasks need to be completed which are configured in experiment module of gui mode.<div style="line-height:75%;"><br></div>
            <strong>thread_num: <i>int, default=None</i></strong><br/>&nbsp &nbsp The number of enabled thread.
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

