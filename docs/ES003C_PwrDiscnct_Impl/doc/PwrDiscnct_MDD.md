---
layout: default
title: PwrDiscnct_MDD
nav_order: 2
parent: Component Implementation
---
{% raw %}
**Module Design Document**

**For**

**PwrDiscnct**

**JulAug 204, 2017**

**Prepared For:**

**Software Engineering**

**Nexteer Automotive,**

**Saginaw, MI, USA**

**Prepared By:**

**Krishna Anne**

**Software Group,**

**Nexteer Automotive,**

**<u>Saginaw, MI, USAChange</u>** History

|                                                                 |              |             |             |
|-------------------------------------|----------------|---------|-----------|
| **Description**                                                 | **Author**   | **Version** | **Date**    |
| Initial Version                                                 | Krishna Anne | 1.0         | 20-Jul-2017 |
| Range of NTC042ParmByte_Cnt_T_u08 is changed in local functions | Krishna Anne | 2.0         | 04-Aug-2017 |

<u>Table of Contents</u>

[1 Introduction 5](#introduction)

[1.1 Purpose 5](#purpose)

[2 HwTq0Meas & High-Level Description
6](#hwtq0meas-high-level-description)

[3 Design details of software module
7](#design-details-of-software-module)

[3.1 Graphical representation of HwTq0Meas
7](#graphical-representation-of-hwtq0meas)

[3.2 Data Flow Diagram 7](#data-flow-diagram)

[3.2.1 Component level DFD 7](#component-level-dfd)

[3.2.2 Function level DFD 7](#function-level-dfd)

[4 Constant Data Dictionary 8](#constant-data-dictionary)

[4.1 Program (fixed) Constants 8](#program-fixed-constants)

[4.1.1 Embedded Constants 8](#embedded-constants)

[5 Software Component Implementation
9](#software-component-implementation)

[5.1 Sub-Module Functions 9](#sub-module-functions)

[5.1.1 Init: HwTq0MeasInit1 9](#init-hwtq0measinit1)

[5.1.1.1 Design Rationale 9](#design-rationale)

[5.1.1.2 Module Outputs 9](#module-outputs)

[5.1.2 Per: HwTq0MeasPer1 9](#per-hwtq0measper1)

[5.1.2.1 Design Rationale 9](#design-rationale-1)

[5.1.2.2 Store Module Inputs to Local copies
9](#store-module-inputs-to-local-copies)

[5.1.2.3 (Processing of function)……… 9](#processing-of-function)

[5.1.2.4 Store Local copy of outputs into Module Outputs
9](#store-local-copy-of-outputs-into-module-outputs)

[5.1.3 Per: HwTq0MeasPer2 9](#__RefHeading___Toc438496780)

[5.1.3.1 Design Rationale 9](#__RefHeading___Toc438496781)

[5.1.3.2 Store Module Inputs to Local copies
10](#__RefHeading___Toc438496782)

[5.1.3.3 (Processing of function)……… 10](#__RefHeading___Toc438496783)

[5.1.3.4 Store Local copy of outputs into Module Outputs
10](#__RefHeading___Toc438496784)

[5.2 Server Runables 10](#server-runables)

[5.2.1 HwTq0MeasHwTq0AutTrim_oper 10](#__RefHeading___Toc438496786)

[5.2.1.1 Design Rationale 10](#__RefHeading___Toc438496787)

[5.2.1.2 (Processing of function)……… 10](#__RefHeading___Toc438496788)

[5.2.2 HwTq0MeasHwTq0ClrTrim_Oper 10](#__RefHeading___Toc438496789)

[5.2.2.1 Design Rationale 10](#__RefHeading___Toc438496790)

[5.2.2.2 (Processing of function)……… 10](#__RefHeading___Toc438496791)

[5.2.3 HwTq0MeasHwTq0ReadTrim_Oper 10](#__RefHeading___Toc438496792)

[5.2.3.1 Design Rationale 10](#__RefHeading___Toc438496793)

[5.2.3.2 (Processing of function)……… 10](#__RefHeading___Toc438496794)

[5.2.4 HwTq0MeasHwTq0TrimPrfmdSts_Oper 11](#__RefHeading___Toc438496795)

[5.2.4.1 Design Rationale 11](#__RefHeading___Toc438496796)

[5.2.4.2 (Processing of function)……… 11](#__RefHeading___Toc438496797)

[5.2.5 HwTq0MeasHwTq0WrTrim_Oper 11](#__RefHeading___Toc438496798)

[5.2.5.1 Design Rationale 11](#__RefHeading___Toc438496799)

[5.2.5.2 (Processing of function)……… 11](#__RefHeading___Toc438496800)

[5.2.6 HwTq0MeasTrigStrt_Oper 11](#__RefHeading___Toc438496801)

[5.2.6.1 Design Rationale 11](#__RefHeading___Toc438496802)

[5.2.6.2 (Processing of function)……… 11](#__RefHeading___Toc438496803)

[5.3 Interrupt Functions 11](#interrupt-functions)

[5.4 Module Internal (Local) Functions
11](#module-internal-local-functions)

[5.4.1 Local Function \#1 11](#local-function-1)

[5.4.1.1 Design Rationale 11](#design-rationale-2)

[5.4.2 Local Function \#2 12](#__RefHeading___Toc438496808)

[5.4.2.1 Design Rationale 12](#__RefHeading___Toc438496809)

[5.5 GLOBAL Function/Macro Definitions
12](#global-functionmacro-definitions)

[6 Known Limitations with Design 13](#known-limitations-with-design)

[7 UNIT TEST CONSIDERATION 14](#unit-test-consideration)

[Appendix A Abbreviations and Acronyms 15](#abbreviations-and-acronyms)

[Appendix B Glossary 16](#glossary)

[Appendix C References 18](#references)

# Introduction

## Purpose

Module design document for PwrDiscnct.

#  HwTq0Meas & High-Level Description

# Design details of software module

## Graphical representation of HwTq0Meas

<img
src="ElectricPowerSteering_RH850_FORD_T3T6_website/docs/ES003C_PwrDiscnct_Impl/doc/mediax/media/image1.png"
style="width:4.10486in;height:5.39514in" />

## Data Flow Diagram

### Component level DFD

N/A

### Function level DFD

N/A

# Constant Data Dictionary

## Program (fixed) Constants

### Embedded Constants

#### Local Constants

|                   |            |       |       |
|-------------------|------------|-------|-------|
| Constant Name     | Resolution | Units | Value |
| TESTNORES_CNT_U08 | 1          | Cnt   | 0U    |
| TESTPASSD_CNT_U08 | 1          | Cnt   | 1U    |
| TESTFAILD_CNT_U08 | 1          | Cnt   | 2U    |

Note : These local constants are used in place of SIGQLFR_NORES (0U),
SIGQLFR_PASSD (1U) and SIGQLFR_FAILD (2U) that are used by FDD because
the datatype SigQlfr1 is not necessary for this purpose as well as it
not possible to get them defined from RTE when no client call that uses
this datatype as one of its arguments is defined by current design.

# Software Component Implementation

## Sub-Module Functions

## Init: HwTq0MeasInit1

## Design Rationale

## Module Outputs

*Refer to FDD*

###  [section]

## Per: HwTq0MeasPer1

## Design Rationale

*None*

## Store Module Inputs to Local copies

*Refer to FDD*

## (Processing of function)………

*Refer to FDD*

## Store Local copy of outputs into Module Outputs

*Refer to FDD*

## Server Runables 

## Interrupt Functions

*None*

## Module Internal (Local) Functions

## Local Function \#1

|                      |                              |         |          |         |
|--------------|------------------------------|----------|----------|----------|
| **Function Name**    | VerifyDiscOpen               | Type    | Min      | Max     |
| **Arguments Passed** | BattVltg_Volt_T_f32          | float32 | 0.0F     | 40.0F   |
|                      | BattVltgSwd1_Volt_T_f32      | float32 | 0.0F     | 40.0F   |
|                      | \*NTC042ParmByte_Cnt_T_u08   | uint08  | 0U       | 55U     |
|                      | PwrDiscnctSwtDiag_Volt_T_f32 | float32 | 0.0F     | 40.0F   |
|                      | ChrgPmpDiag_Volt_T_f32       | float32 | 0.0F     | 40.0F   |
|                      | MotVelMrf_MotRadPerSec_T_f32 | float32 | -1350.0F | 1350.0F |
|                      | \*ErrAccOutp_Cnt_T_u16       | uint16  | 0U       | 65535U  |
| **Return Value**     | N/A                          | N/A     | N/A      | N/A     |

## Design Rationale

Path in FDD :
ES003C_PwrDiscnct/PwrDiscnct/PwrDiscnctPer1/WarmInit/Operate/OPEN&CLOSE/VERIFYDISCOPEN.

## Local Function \#2

|                      |                              |         |      |        |
|----------------------|------------------------------|---------|------|--------|
| **Function Name**    | VerifyClose                  | Type    | Min  | Max    |
| **Arguments Passed** | BattVltg_Volt_T_f32          | float32 | 0.0F | 40.0F  |
|                      | BattVltgSwd1_Volt_T_f32      | float32 | 0.0F | 40.0F  |
|                      | \*NTC042ParmByte_Cnt_T_u08   | uint08  | 0U   | 55U    |
|                      | PwrDiscnctSwtDiag_Volt_T_f32 | float32 | 0.0F | 40.0F  |
|                      | \*ErrAccOutp_Cnt_T_u16       | uint16  | 0U   | 65535U |
| **Return Value**     | N/A                          | N/A     | N/A  | N/A    |

## Design Rationale

Path in FDD :
ES003C_PwrDiscnct/PwrDiscnct/PwrDiscnctPer1/WarmInit/Operate/OPEN&CLOSE/VERIFYCLOSE.

## Local Function \#3

|                      |                              |         |      |       |
|----------------------|------------------------------|---------|------|-------|
| **Function Name**    | InitialDiag                  | Type    | Min  | Max   |
| **Arguments Passed** | BattVltg_Volt_T_f32          | float32 | 0.0F | 40.0F |
|                      | BattVltgSwd1_Volt_T_f32      | float32 | 0.0F | 40.0F |
|                      | \*NTC042ParmByte_Cnt_T_u08   | uint08  | 0U   | 55U   |
|                      | PwrDiscnctSwtDiag_Volt_T_f32 | float32 | 0.0F | 40.0F |
|                      | ChrgPmpDiag_Volt_T_f32       | float32 | 0.0F | 40.0F |
| **Return Value**     | N/A                          | N/A     | N/A  | N/A   |

## Design Rationale

Path in FDD :
ES003C_PwrDiscnct/PwrDiscnct/PwrDiscnctPer1/WarmInit/Operate/OPEN&CLOSE/VERIFYDISCOPEN/InitialDiag.

## Local Function \#4

|                      |                                |         |       |       |
|--------------|------------------------------|----------|----------|----------|
| **Function Name**    | PwrDiscnctDiag                 | Type    | Min   | Max   |
| **Arguments Passed** | BattVltg_Volt_T_f32            | float32 | 0.0F  | 40.0F |
|                      | ChrgMinDelta_Volt_T_f32        | float32 | 0.0F  | 40.0F |
|                      | BattVltgAdcFaild_Cnt_T_logl    | boolean | FALSE | TRUE  |
|                      | ChrgPmpDiagAdcFaild_Cnt_T_logl | boolean | FALSE | TRUE  |
|                      | ChrgPmpDiag_Volt_T_f32         | float32 | 0.0F  | 40.0F |
| **Return Value**     | N/A                            | N/A     | N/A   | N/A   |

## Design Rationale

Path in FDD : Path in FDD :
ES003C_PwrDiscnct/PwrDiscnct/PwrDiscnctPer1/WarmInit/Operate/RUNTIMEDIAG/PwrDiscnctDiagnostic.

## GLOBAL Function/Macro Definitions

None

# Known Limitations with Design

Please see not in section 4.1.1.1 w.r.t SigQlfr1 enumeration’s
non-usage.

# UNIT TEST CONSIDERATION

Please see not in section 4.1.1.1 w.r.t SigQlfr1 enumeration’s
non-usage.

####### Abbreviations and Acronyms

| **Abbreviation or Acronym** | **Description**           |
|-----------------------------|---------------------------|
| DFD                         | Design functional diagram |
| MDD                         | Module design Document    |

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

| **Ref. \#** | **Title**                                                                                                                                                             | **Version**                    |
|-------|-------------------------------------------------|-----------------|
| 1           | AUTOSAR Specification of Memory Mapping (Link:[AUTOSAR_SWS_MemoryMapping.pdf](http://www.autosar.org/download/R4.0/AUTOSAR_SWS_MemoryMapping.pdf))                    | v1.3.0 R4.0 Rev 2              |
| 2           | MDD Guideline                                                                                                                                                         | EA4 01.00.00                   |
| 3           | [Software Naming Conventions.doc](http://misagweb01.nexteer.com/eRoomReq/Files/erooms8/NextGeneration/0_fc55f/Software%20Naming%20Conventions%2003x(In%20Work).doc)   | 1.0                            |
| 4           | [Software Design and Coding Standards.doc](http://eroom1.nexteer.com/eRoomReq/Files/erooms8/NextGeneration/0_1a67a9/Software%20Design%20and%20Coding%20Standards.doc) | 2.1                            |
| 5           | FDD – ES003C PwrDiscnct                                                                                                                                               | See Synergy subproject version |

{% endraw %}