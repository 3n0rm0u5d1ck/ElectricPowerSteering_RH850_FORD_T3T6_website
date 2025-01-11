---
layout: default
title: GtmCfgAndUse_MDD
nav_order: 2
parent: Component Implementation
---
{% raw %}
**Module Design Document Guidelines**

**GtmCfgAndUse**

**Feb 28, 2018**

**Prepared For:**

**Software Engineering**

**Nexteer Automotive,**

**Saginaw, MI, USA**

**Prepared By:**

**Software Group,**

**Nexteer Automotive,**

**Saginaw, MI, USA  
<u>Change History</u>**

|                                                          |               |             |             |
|-----------------------|-----------------------|------------|---------------|
| **Description**                                          | **Author**    | **Version** | **Date**    |
| Initial version                                          | Avinash James | 1.0         | 13-Sep-2017 |
| Updated local function and added unit test consideration | Avinash James | 2.0         | 28-Feb-2018 |

**<u>  
</u>**

**<u>Table of Contents</u>**

[1 Introduction [5](#introduction)](#introduction)

[1.1 Purpose [5](#purpose)](#purpose)

[1.2 Scope [5](#_Toc495057831)](#_Toc495057831)

[2 Component Name & High Level Description
[6](#component-name-high-level-description)](#component-name-high-level-description)

[3 Design details of software component
[7](#design-details-of-software-component)](#design-details-of-software-component)

[3.1 Graphical Representation
[7](#graphical-representation)](#graphical-representation)

[3.2 Data Flow Diagrams [7](#data-flow-diagrams)](#data-flow-diagrams)

[3.2.1 Component level DFD
[7](#component-level-dfd)](#component-level-dfd)

[3.2.2 Function level DFD [7](#function-level-dfd)](#function-level-dfd)

[4 Constant Data Dictionary
[8](#constant-data-dictionary)](#constant-data-dictionary)

[4.1 Program (fixed) Constants
[8](#program-fixed-constants)](#program-fixed-constants)

[4.1.1 Embedded Constants [8](#embedded-constants)](#embedded-constants)

[5 Software Component Implementation
[9](#software-component-implementation)](#software-component-implementation)

[5.1 Sub-Module Functions
[9](#sub-module-functions)](#sub-module-functions)

[5.1.1 Init: GtmCfgAndUseInit1
[9](#init-gtmcfganduseinit1)](#init-gtmcfganduseinit1)

[5.1.1.1 Design Rationale [9](#design-rationale)](#design-rationale)

[5.1.1.2 Module Outputs [9](#module-outputs)](#module-outputs)

[5.1.2 Per: GtmCfgAndUsePer1
[9](#per-gtmcfganduseper1)](#per-gtmcfganduseper1)

[5.1.2.1 Design Rationale [9](#design-rationale-1)](#design-rationale-1)

[5.1.2.2 Store Module Inputs to Local copies
[9](#store-module-inputs-to-local-copies)](#store-module-inputs-to-local-copies)

[5.1.2.3 (Processing of function)
[9](#processing-of-function)](#processing-of-function)

[5.1.2.4 Store Local copy of outputs into Module Outputs
[9](#store-local-copy-of-outputs-into-module-outputs)](#store-local-copy-of-outputs-into-module-outputs)

[5.1.3 Per: GtmCfgAndUsePer2
[9](#per-gtmcfganduseper2)](#per-gtmcfganduseper2)

[5.1.3.1 Design Rationale [9](#design-rationale-2)](#design-rationale-2)

[5.1.3.2 Store Module Inputs to Local copies
[9](#store-module-inputs-to-local-copies-1)](#store-module-inputs-to-local-copies-1)

[5.1.3.3 (Processing of function)
[9](#processing-of-function-1)](#processing-of-function-1)

[5.1.3.4 Store Local copy of outputs into Module Outputs
[9](#store-local-copy-of-outputs-into-module-outputs-1)](#store-local-copy-of-outputs-into-module-outputs-1)

[5.2 Server Runnable () Functions
[10](#server-runnable-functions)](#server-runnable-functions)

[5.2.1 GtmGetSent0Data_Oper
[10](#gtmgetsent0data_oper)](#gtmgetsent0data_oper)

[5.2.1.1 Design Rationale
[10](#design-rationale-3)](#design-rationale-3)

[5.2.1.2 Store Module Inputs to Local copies
[10](#store-module-inputs-to-local-copies-2)](#store-module-inputs-to-local-copies-2)

[5.2.1.3 (Processing of function)
[10](#processing-of-function-2)](#processing-of-function-2)

[5.2.1.4 Store Local copy of outputs into Module Outputs
[10](#store-local-copy-of-outputs-into-module-outputs-2)](#store-local-copy-of-outputs-into-module-outputs-2)

[5.2.2 GtmGetSent1Data_Oper
[10](#gtmgetsent1data_oper)](#gtmgetsent1data_oper)

[5.2.2.1 Design Rationale
[10](#design-rationale-4)](#design-rationale-4)

[5.2.2.2 Store Module Inputs to Local copies
[10](#store-module-inputs-to-local-copies-3)](#store-module-inputs-to-local-copies-3)

[5.2.2.3 (Processing of function)
[10](#processing-of-function-3)](#processing-of-function-3)

[5.2.2.4 Store Local copy of outputs into Module Outputs
[10](#store-local-copy-of-outputs-into-module-outputs-3)](#store-local-copy-of-outputs-into-module-outputs-3)

[5.3 Interrupt Service Routines
[10](#interrupt-service-routines)](#interrupt-service-routines)

[5.4 Module Internal (Local) Functions
[10](#module-internal-local-functions)](#module-internal-local-functions)

[5.4.1 Local Function \#1 [10](#local-function-1)](#local-function-1)

[5.4.1.1 Description [11](#description)](#description)

[5.4.2 Local Function \#2 [11](#local-function-2)](#local-function-2)

[5.4.2.1 Description [11](#description-1)](#description-1)

[5.4.3 Local Function \#3 [11](#local-function-3)](#local-function-3)

[5.4.3.1 Description [11](#description-2)](#description-2)

[5.4.4 Local Function \#4 [11](#local-function-4)](#local-function-4)

[5.4.4.1 Description [11](#description-3)](#description-3)

[5.4.5 Local Function \#5 [11](#local-function-5)](#local-function-5)

[5.4.5.1 Description [12](#description-4)](#description-4)

[5.4.6 Local Function \#6 [12](#local-function-6)](#local-function-6)

[5.4.6.1 Description [12](#description-5)](#description-5)

[5.4.7 Local Function \#7 [12](#local-function-7)](#local-function-7)

[5.4.7.1 Description [12](#description-6)](#description-6)

[5.4.7.2 Design Rationale
[12](#design-rationale-5)](#design-rationale-5)

[5.5 GLOBAL Function/Macro Definitions
[13](#global-functionmacro-definitions)](#global-functionmacro-definitions)

[6 Known Limitations with Design
[14](#known-limitations-with-design)](#known-limitations-with-design)

[7 UNIT TEST CONSIDERATION
[15](#unit-test-consideration)](#unit-test-consideration)

[Appendix A Abbreviations and Acronyms
[16](#abbreviations-and-acronyms)](#abbreviations-and-acronyms)

[Appendix B Glossary [17](#glossary)](#glossary)

[Appendix C References [18](#references)](#references)

# Introduction

## Purpose

# Component Name & High Level Description

Refer FDD

# Design details of software component

## Graphical Representation

<img
src="ElectricPowerSteering_RH850_FORD_T3T6_website/docs/CM770A_GtmCfgAndUse_Impl/doc/mediax/media/image1.png"
style="width:5.58333in;height:5.575in" /><img
src="ElectricPowerSteering_RH850_FORD_T3T6_website/docs/CM770A_GtmCfgAndUse_Impl/doc/mediax/media/image2.png"
style="width:5.64167in;height:5.68333in" />

## Data Flow Diagrams

Refer FDD

### Component level DFD

### Function level DFD

# Constant Data Dictionary

## Program (fixed) Constants

### Embedded Constants

#### Local Constants

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constant Name</p></th>
<th>Data Type</th>
<th>Value</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>CLRBIT0MASK_CNT_U32</td>
<td>Uint32</td>
<td>((uint32)0xFFFFFFFEU)</td>
</tr>
<tr class="even">
<td>Refer .m file</td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

# Software Component Implementation

## Sub-Module Functions

### Init: GtmCfgAndUseInit1

## Design Rationale

Refer FDD

## Module Outputs

*None*

### Per: GtmCfgAndUsePer1

## Design Rationale

Refer FDD

## Store Module Inputs to Local copies

*None*

## (Processing of function)

*Refer FDD*

## Store Local copy of outputs into Module Outputs

*None*

### Per: GtmCfgAndUsePer2

## Design Rationale

Refer FDD

## Store Module Inputs to Local copies

*None*

## (Processing of function)

*Refer FDD*

## Store Local copy of outputs into Module Outputs

*None*

## Server Runnable () Functions

### GtmGetSent0Data_Oper

## Design Rationale

Refer FDD .

The place where the server runnable gets called should make sure a NULL
pointer is not passed as an argument to the server runnable

## Store Module Inputs to Local copies

*None*

## (Processing of function)

*Refer FDD*

## Store Local copy of outputs into Module Outputs

*None*

### GtmGetSent1Data_Oper

## Design Rationale

Refer FDD

The place where the server runnable gets called should make sure a NULL
pointer is not passed as an argument to the server runnable

## Store Module Inputs to Local copies

*None*

## (Processing of function)

*Refer FDD*

## Store Local copy of outputs into Module Outputs

*None*

## Interrupt Service Routines

*None*

## Module Internal (Local) Functions

## Local Function \#1 

|                      |                            |                  |     |     |
|------------|--------------------------|---------------|----------|----------|
| **Function Name**    | NoTranSysStIsEn            | Type             | Min | Max |
| **Arguments Passed** | MotCurrEolCalSt_Cnt_T_enum | MotCurrEolCalSt2 | 0   | 8   |
|                      | IvtrFetFltPha_Cnt_T_enum   | IvtrFetFltPha1   | 0   | 4   |
| **Return Value**     | N/A                        |                  |     |     |

## Description

See FDD model block:
CM770A_GtmCfgAndUse/GtmCfgAndUse/GtmCfgAndUsePer2/No Transition SysState
= Enable

## Local Function \#2

|                      |            |      |     |     |
|----------------------|------------|------|-----|-----|
| **Function Name**    | TranFromEn | Type | Min | Max |
| **Arguments Passed** | None       |      |     |     |
| **Return Value**     | N/A        |      |     |     |

## Description

See FDD model block:
CM770A_GtmCfgAndUse/GtmCfgAndUse/GtmCfgAndUsePer2/Transition from Enable

## Local Function \#3

|                      |          |      |     |     |
|----------------------|----------|------|-----|-----|
| **Function Name**    | TranToEn | Type | Min | Max |
| **Arguments Passed** | None     |      |     |     |
| **Return Value**     | N/A      |      |     |     |

## Description

See FDD model block:
CM770A_GtmCfgAndUse/GtmCfgAndUse/GtmCfgAndUsePer2/Transition to Enable

## Local Function \#4

|                      |                  |      |     |     |
|----------------------|------------------|------|-----|-----|
| **Function Name**    | NoTranSysStNotEn | Type | Min | Max |
| **Arguments Passed** | None             |      |     |     |
| **Return Value**     | N/A              |      |     |     |

## Description

See FDD model block:
CM770A_GtmCfgAndUse/GtmCfgAndUse/GtmCfgAndUsePer2/No Transition SysState
!= Enable

## Local Function \#5

|                      |                              |      |     |     |
|----------------------|------------------------------|------|-----|-----|
| **Function Name**    | MapFetCtrlSigToGpioAndSetLow | Type | Min | Max |
| **Arguments Passed** | None                         |      |     |     |
| **Return Value**     | N/A                          |      |     |     |

## Description

See FDD model block:
CM770A_GtmCfgAndUse/GtmCfgAndUse/GtmCfgAndUsePer2/Transition from
Enable/Map FET Ctrl Signals to GPIO and Set Low (also same block name in
other model layers)

## Local Function \#6

|                      |               |      |     |     |
|----------------------|---------------|------|-----|-----|
| **Function Name**    | MapPinsToGpio | Type | Min | Max |
| **Arguments Passed** | None          |      |     |     |
| **Return Value**     | N/A           |      |     |     |

## Description

See FDD model block:
CM770A_GtmCfgAndUse/GtmCfgAndUse/GtmCfgAndUsePer2/Transition from
Enable/Map FET Ctrl Signals to GPIO and Set Low/Map Pins to GPIO (also
same block name in other model layers)

## Local Function \#7

|                      |                                              |        |     |        |
|---------------|--------------------------------|---------|---------|---------|
| **Function Name**    | CnvNanoSecToTmrCnt                           | Type   | Min | Max    |
| **Arguments Passed** | Ti_NanoSec_T_u32                             | uint32 | 0   | 100000 |
| **Return Value**     | Timer counts corresponding to the input time | uint32 | 0   | 8000   |

## Description

See FDD model block:
CM770A_GtmCfgAndUse/GtmCfgAndUse/GtmCfgAndUsePer1/UpdatePWMRegisters/RawTime_NanoSec
to RawTimerCount_Cnt Conversion Block

## Design Rationale

Because this function is called by a motor control runnable, it is coded
as an inline function to maximize the chance that the compiler will
inline it, in order to improve runtime efficiency of the motor control
loop.

## Local Function \#8

|                      |                          |                |     |     |
|----------------------|--------------------------|----------------|-----|-----|
| **Function Name**    | ChkForFetFlt             | Type           | Min | Max |
| **Arguments Passed** | IvtrFetFltPha_Cnt_T_enum | IvtrFetFltPha1 | 0   | 4   |
| **Return Value**     | None                     |                |     |     |

## Description

See FDD model block:
CM770A_GtmCfgAndUse/GtmCfgAndUse/GtmCfgAndUsePer2/Check For FET faults

Conversion Block

## GLOBAL Function/Macro Definitions

None

# Known Limitations with Design

None

# UNIT TEST CONSIDERATION

Roll over of the PIM Rte_Pim_MissUpdCntr in the motor control function
is intentional

In the motor control function MissUpdStrtCntr_Cnt_T_u32 and
MissUpdEndCntr_Cnt_T_u32 reads the value from the same register
GTM0ATOM00CN0. Hence during unit testing where these registers are
simulated as variables and doesn’t change during execution, there will
be a coverage issue for achieving the false case for the condition
((MissUpdStrtCntr_Cnt_T_u32 \>= MissUpdEndCntr_Cnt_T_u32) as this will
always be TRUE the way unit testing is done now.

####### Abbreviations and Acronyms

|     |     |     |
|-----|-----|-----|
|     |     |     |
|     |     |     |

####### Glossary

**Note**: Terms and definitions from the source “Nexteer Automotive”
take precedence over all other definitions of the same term. Terms and
definitions from the source “Nexteer Automotive” are formulated from
multiple sources, including the following:

-   ISO 9000

-   ISO/IEC 12207

-   ISO/IEC 15504

-   Automotive SPICE® Process Reference Model (PRM)

-   Automotive SPICE® Process Assessment Model (PAM)

-   ISO/IEC 15288

-   ISO 26262

-   IEEE Standards

-   SWEBOK

-   PMBOK

-   Existing Nexteer Automotive documentation

| **Term** | **Definition**         | **Source** |
|----------|------------------------|------------|
| MDD      | Module Design Document |            |
| DFD      | Data Flow Diagram      |            |

####### References

| **Ref. \#** | **Title**                                                                                                                                                             | **Version**       |
|-------|-------------------------------------------------|-----------------|
| 1           | AUTOSAR Specification of Memory Mapping (Link:[AUTOSAR_SWS_MemoryMapping.pdf](http://www.autosar.org/download/R4.0/AUTOSAR_SWS_MemoryMapping.pdf))                    | v1.3.0 R4.0 Rev 2 |
| 2           | MDD Design Template                                                                                                                                                   | 1.0.1             |
| 3           | [Software Naming Conventions.doc](http://misagweb01.nexteer.com/eRoomReq/Files/erooms8/NextGeneration/0_fc55f/Software%20Naming%20Conventions%2003x(In%20Work).doc)   | 1.0.1             |
| 4           | [Software Design and Coding Standards.doc](http://eroom1.nexteer.com/eRoomReq/Files/erooms8/NextGeneration/0_1a67a9/Software%20Design%20and%20Coding%20Standards.doc) | 2.1               |

{% endraw %}