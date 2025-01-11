---
layout: default
title: FordSysSt_MDD
nav_order: 2
parent: Component Implementation
---
{% raw %}
**Module Design Document**

**For**

**FordSysSt**

**04-Dec-2017**

**Prepared For:**

**Software Engineering**

**Nexteer Automotive,**

**Saginaw, MI, USA**

**Prepared By:**

**Shawn Penning,**

**Nexteer Automotive,**

**Saginaw, MI, USA  
<u>Change History</u>**

|                 |               |             |             |
|-----------------|---------------|-------------|-------------|
| **Description** | **Author**    | **Version** | **Date**    |
| Initial Version | Shawn Penning | 1           | 04-Dec-2017 |

**  
**

<u>Table of Contents</u>

[1 Introduction [6](#introduction)](#introduction)

[1.1 Purpose [6](#purpose)](#purpose)

[1.2 Scope [6](#scope)](#scope)

[2 FordSysSt & High-Level Description
[7](#fordsysst-high-level-description)](#fordsysst-high-level-description)

[3 Design details of software module
[8](#design-details-of-software-module)](#design-details-of-software-module)

[3.1 Graphical representation of FordSysSt
[8](#graphical-representation-of-fordsysst)](#graphical-representation-of-fordsysst)

[3.2 Data Flow Diagram [8](#data-flow-diagram)](#data-flow-diagram)

[3.2.1 Component level DFD
[8](#component-level-dfd)](#component-level-dfd)

[3.2.2 Function level DFD [8](#function-level-dfd)](#function-level-dfd)

[4 Constant Data Dictionary
[9](#constant-data-dictionary)](#constant-data-dictionary)

[4.1 Program (fixed) Constants
[9](#program-fixed-constants)](#program-fixed-constants)

[4.1.1 Embedded Constants [9](#embedded-constants)](#embedded-constants)

[5 Software Component Implementation
[10](#software-component-implementation)](#software-component-implementation)

[5.1 Sub-Module Functions
[10](#sub-module-functions)](#sub-module-functions)

[5.1.1 Init: FordSysStInit1 [10](#init-init1)](#init-init1)

[5.1.1.1 Design Rationale [10](#design-rationale)](#design-rationale)

[5.1.1.2 Module Outputs [10](#module-outputs)](#module-outputs)

[5.1.2 Per: FordSysStPer1 [10](#per-per1)](#per-per1)

[5.1.2.1 Design Rationale
[10](#design-rationale-1)](#design-rationale-1)

[5.1.2.2 Store Module Inputs to Local copies
[10](#store-module-inputs-to-local-copies)](#store-module-inputs-to-local-copies)

[5.1.2.3 (Processing of function)
[10](#processing-of-function)](#processing-of-function)

[5.1.2.4 Store Local copy of outputs into Module Outputs
[10](#store-local-copy-of-outputs-into-module-outputs)](#store-local-copy-of-outputs-into-module-outputs)

[5.2 Server Runnables [10](#server-runnables)](#server-runnables)

[5.3 Interrupt Functions
[10](#interrupt-functions)](#interrupt-functions)

[5.4 Module Internal (Local) Functions
[10](#module-internal-local-functions)](#module-internal-local-functions)

[5.4.1 Local Function \#1 [10](#local-function-1)](#local-function-1)

[5.4.1.1 Design Rationale
[10](#design-rationale-2)](#design-rationale-2)

[5.4.1.2 Processing [11](#processing)](#processing)

[5.4.2 Local Function \#2 [11](#local-function-2)](#local-function-2)

[5.4.2.1 Design Rationale
[11](#design-rationale-3)](#design-rationale-3)

[5.4.2.2 Processing [11](#processing-1)](#processing-1)

[5.4.3 Local Function \#3 [11](#local-function-3)](#local-function-3)

[5.4.3.1 Design Rationale
[11](#design-rationale-4)](#design-rationale-4)

[5.4.3.2 Processing [11](#processing-2)](#processing-2)

[5.4.4 Local Function \#4 [11](#local-function-4)](#local-function-4)

[5.4.4.1 Design Rationale
[11](#design-rationale-5)](#design-rationale-5)

[5.4.4.2 Processing [11](#processing-3)](#processing-3)

[5.4.5 Local Function \#5 [11](#local-function-5)](#local-function-5)

[5.4.5.1 Design Rationale
[12](#design-rationale-6)](#design-rationale-6)

[5.4.5.2 Processing [12](#processing-4)](#processing-4)

[5.4.6 Local Function \#6 [12](#local-function-6)](#local-function-6)

[5.4.6.1 Design Rationale
[12](#design-rationale-7)](#design-rationale-7)

[5.4.6.2 Processing [12](#processing-5)](#processing-5)

[5.4.7 Local Function \#7 [12](#local-function-7)](#local-function-7)

[5.4.7.1 Design Rationale
[13](#design-rationale-8)](#design-rationale-8)

[5.4.7.2 Processing [13](#processing-6)](#processing-6)

[5.4.8 Local Function \#8 [13](#local-function-8)](#local-function-8)

[5.4.9 Design Rationale [13](#design-rationale-9)](#design-rationale-9)

[5.4.9.1 Processing [13](#processing-7)](#processing-7)

[5.4.10 Local Function \#9 [13](#local-function-9)](#local-function-9)

[5.4.11 Design Rationale
[13](#design-rationale-10)](#design-rationale-10)

[5.4.11.1 Processing [13](#processing-8)](#processing-8)

[5.4.12 Local Function \#10
[13](#local-function-10)](#local-function-10)

[5.4.12.1 Design Rationale
[13](#design-rationale-11)](#design-rationale-11)

[5.4.12.2 Processing [14](#processing-9)](#processing-9)

[5.4.13 Local Function \#11
[14](#local-function-11)](#local-function-11)

[5.4.14 Design Rationale
[14](#design-rationale-12)](#design-rationale-12)

[5.4.14.1 Processing [14](#processing-10)](#processing-10)

[5.4.15 Local Function \#12
[14](#local-function-12)](#local-function-12)

[5.4.16 Design Rationale
[14](#design-rationale-13)](#design-rationale-13)

[5.4.16.1 Processing [14](#processing-11)](#processing-11)

[5.4.17 Local Function \#13
[14](#local-function-13)](#local-function-13)

[5.4.18 Design Rationale
[14](#design-rationale-14)](#design-rationale-14)

[5.4.18.1 Processing [14](#processing-12)](#processing-12)

[5.5 GLOBAL Function/Macro Definitions
[14](#global-functionmacro-definitions)](#global-functionmacro-definitions)

[6 Known Limitations with Design
[16](#known-limitations-with-design)](#known-limitations-with-design)

[7 UNIT TEST CONSIDERATION
[17](#unit-test-consideration)](#unit-test-consideration)

[Appendix A Abbreviations and Acronyms
[18](#abbreviations-and-acronyms)](#abbreviations-and-acronyms)

[Appendix B Glossary [19](#glossary)](#glossary)

[Appendix C References [20](#references)](#references)

# Introduction

## Purpose

## Scope

# FordSysSt & High-Level Description

Ford System State will handle internal states and failure modes, and
output the current state to the bus.

# Design details of software module

## Graphical representation of FordSysSt

<img
src="ElectricPowerSteering_RH850_FORD_T3T6_website/docs/CF052A_FordSysSt_Impl/doc/mediax/media/image1.png"
style="width:5.02569in;height:5.24375in" />

## Data Flow Diagram

Refer FDD

### Component level DFD

Refer FDD

### Function level DFD

Refer FDD

# Constant Data Dictionary

## Program (fixed) Constants

### Embedded Constants

#### Local Constants

| Constant Name | Resolution | Units | Value |
|---------------|------------|-------|-------|
| Refer .m file |            |       |       |

# Software Component Implementation

## Sub-Module Functions

### Init: Init1

## Design Rationale

*None*

## Module Outputs

*None*

### Per: Per1

## Design Rationale

*None*

## Store Module Inputs to Local copies

*Refer FDD*

## (Processing of function)

*Refer FDD*

## Store Local copy of outputs into Module Outputs

*Refer FDD*

## Server Runnables 

*None*

## Interrupt Functions

*None*

## Module Internal (Local) Functions

## Local Function \#1

|                      |                             |                 |       |      |
|--------------|-------------------------------|-----------|---------|---------|
| **Function Name**    | ChkLvngWarmInit             | Type            | Min   | Max  |
| **Arguments Passed** | FordSysSt_Cnt_T_enum        | SysSt1          | 0U    | 3U   |
|                      | FordLoaSt_Cnt_T_enum        | LoaSt1          | 0U    | 5U   |
|                      | SysStWrmIninCmpl_Cnt_T_logl | Boolean         | FALSE | TRUE |
|                      | FordVltgOperSt_Cnt_T_enum   | FordVltgOperSt1 | 0U    | 6U   |
|                      | FordEpsSysSt_Cnt_T_enum     | FordEpsSysSt1   | 0U    | 8U   |
|                      | OperScaFctr_Cnt_T_f32       | float32         | 0.1   | 1    |
|                      | OperRampRate_Cnt_T_f32      | float32         | 0.1   | 1000 |
| **Return Value**     | none                        |                 |       |      |

## Design Rationale

None

## Processing

Check the conditions for leaving ChkLvngWarmInit.

## Local Function \#2

|                      |                         |               |     |     |
|----------------------|-------------------------|---------------|-----|-----|
| **Function Name**    | ChkLvngLimpHome         | Type          | Min | Max |
| **Arguments Passed** | FordLoaSt_Cnt_T_enum    | LoaSt1        | 0U  | 3U  |
|                      | FordEpsSysSt_Cnt_T_enum | FordEpsSysSt1 | 0U  | 8U  |
| **Return Value**     | none                    |               |     |     |

## Design Rationale

None

## Processing

## Local Function \#3

|                      |                         |               |     |     |
|----------------------|-------------------------|---------------|-----|-----|
| **Function Name**    | ChkLvngLimpAside        | Type          | Min | Max |
| **Arguments Passed** | FordLoaSt_Cnt_T_enum    | LoaSt1        | 0U  | 3U  |
|                      | FordEpsSysSt_Cnt_T_enum | FordEpsSysSt1 | 0U  | 8U  |
| **Return Value**     | none                    |               |     |     |

## Design Rationale

None

## Processing

Check the condtions for leaving LimpAside for another substate of
EPSSystemFailure.

## Local Function \#4

|                      |                         |               |     |     |
|----------------------|-------------------------|---------------|-----|-----|
| **Function Name**    | ChkLvngRampOut          | Type          | Min | Max |
| **Arguments Passed** | FordLoaSt_Cnt_T_enum    | LoaSt1        | 0U  | 3U  |
|                      | FordEpsSysSt_Cnt_T_enum | FordEpsSysSt1 | 0U  | 8U  |
| **Return Value**     | none                    |               |     |     |

## Design Rationale

None

## Processing

Check the condtions for leaving RampOut for another substate of
EPSSystemFailure.

## Local Function \#5

|                      |                              |                     |       |         |
|-------------|------------------------------|--------------|--------|--------|
| **Function Name**    | ChkLvngEpsNormOperLimAssi    | Type                | Min   | Max     |
| **Arguments Passed** | LoaSt_Cnt_T_enum             | LoaSt1              | 0U    | 3U      |
|                      | FordVltgOperSt_Cnt_T_enum    | FordVltgOperSt1     | 0U    | 6U      |
|                      | SysSt_Cnt_T_enum             | SysSt1              | 0U    | 3U      |
|                      | FordVehSpdVld_Cnt_T_logl     | boolean             | FALSE | TRUE    |
|                      | FordVehSpd_Cnt_T_f32         | float32             | 0.0F  | 511.0F  |
|                      | FordVehPwrpkTqSts_Cnt_T_enum | Ford_PwPckTq_D_Stat | 0U    | 3U      |
|                      | NtcQlfr_Cnt_T_enum           | SigQlfr1            | 0U    | 2U      |
|                      | FordEpsSysSt_Cnt_T_enum      | FordEpsSysSt1       | 0U    | 8U      |
|                      | OperScaFctr_Cnt_T_f32        | float32             | 0.0F  | 1.0F    |
|                      | OperRampRate_Cnt_T_f32       | float32             | 0.0F  | 1000.0F |
| **Return Value**     | none                         |                     |       |         |

## Design Rationale

None

## Processing

Check the conditions for leaving EpsNormOper--\>LimAssi.

## Local Function \#6

|                      |                              |                     |       |        |
|-------------|------------------------------|--------------|--------|--------|
| **Function Name**    | ChkLvngEpsNormOperFullAssi   | Type                | Min   | Max    |
| **Arguments Passed** | FordLoaSt_Cnt_T_enum         | LoaSt1              | 0U    | 3U     |
|                      | FordVltgOperSt_Cnt_T_enum    | FordVltgOperSt1     | 0U    | 6U     |
|                      | FordSysSt_Cnt_T_enum         | SysSt1              | 0U    | 3U     |
|                      | FordVehSpdVld_Cnt_T_logl     | boolean             | FALSE | TRUE   |
|                      | FordVehSpd_Cnt_T_f32         | float32             | 0.0F  | 511.0F |
|                      | FordVehPwrpkTqSts_Cnt_T_enum | Ford_PwPckTq_D_Stat | 0U    | 3U     |
|                      | NtcQlfr_Cnt_T_enum           | SigQlfr1            | 0U    | 2U     |
| **Return Value**     | none                         |                     |       |        |

## Design Rationale

None

## Processing

Check the conditions for leaving EpsNormOper--\>FullAssist.

## Local Function \#7

|                      |           |      |     |     |
|----------------------|-----------|------|-----|-----|
| **Function Name**    | PowerDown | Type | Min | Max |
| **Arguments Passed** | None      |      |     |     |
| **Return Value**     |           |      |     |     |

## Design Rationale

None

## Processing

Set FordEpsSystemSt to PowerDown

## Local Function \#8

|                      |          |      |     |     |
|----------------------|----------|------|-----|-----|
| **Function Name**    | WarmInit | Type | Min | Max |
| **Arguments Passed** | None     |      |     |     |
| **Return Value**     |          |      |     |     |

## Design Rationale

None

## Processing

Set WarmInit conditions.

## Local Function \#9

|                      |                  |      |     |     |
|----------------------|------------------|------|-----|-----|
| **Function Name**    | EpsSystemFailure | Type | Min | Max |
| **Arguments Passed** | None             |      |     |     |
| **Return Value**     |                  |      |     |     |

## Design Rationale

None

## Processing

Set EpsSystemFailure variables common to the entire block.

## Local Function \#10

|                      |                              |                     |       |        |
|-------------|------------------------------|--------------|--------|--------|
| **Function Name**    | EpsSystemFailureExitCheck    | Type                | Min   | Max    |
| **Arguments Passed** | FordSysSt_Cnt_T_enum         | SysSt1              | 0U    | 3U     |
|                      | FordVehSpd_Cnt_T_f32         | float32             | 0.0F  | 511.0F |
|                      | FordVehSpdVld_Cnt_T_logl     | boolean             | FALSE | TRUE   |
|                      | FordVehPwrpkTqSts_Cnt_T_enum | Ford_PwPckTq_D_Stat | 0U    | 3U     |
|                      | NtcQlfr_Cnt_T_enum           | SigQlfr1            | 0U    | 2U     |
| **Return Value**     |                              | boolean             | FALSE | TRUE   |

## Design Rationale

None

## Processing

Called whenever FordEpsSysSt is already in an EpsSystemFailure state.

## Local Function \#11

|                      |           |      |     |     |
|----------------------|-----------|------|-----|-----|
| **Function Name**    | LimAssist | Type | Min | Max |
| **Arguments Passed** | None      |      |     |     |
| **Return Value**     |           |      |     |     |

## Design Rationale

None

## Processing

Set LimAssist conditions.

## Local Function \#12

|                      |            |      |     |     |
|----------------------|------------|------|-----|-----|
| **Function Name**    | FullAssist | Type | Min | Max |
| **Arguments Passed** | None       |      |     |     |
| **Return Value**     |            |      |     |     |

## Design Rationale

None

## Processing

Set FullAssist conditions.

## Local Function \#13

|                      |          |      |     |     |
|----------------------|----------|------|-----|-----|
| **Function Name**    | ShutDown | Type | Min | Max |
| **Arguments Passed** | None     |      |     |     |
| **Return Value**     |          |      |     |     |

## Design Rationale

None

## Processing

Set ShutDown conditions.

## GLOBAL Function/Macro Definitions

None

# Known Limitations with Design

None

# UNIT TEST CONSIDERATION

None

####### Abbreviations and Acronyms

| **Abbreviation or Acronym** | **Description** |
|-----------------------------|-----------------|
|                             |                 |
|                             |                 |

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

| **Ref. \#** | **Title**                                                                                                                                                                                                                | **Version**                    |
|-------|-------------------------------------------------|-----------------|
| 1           | [AUTOSAR Specification of Memory Mapping](http://www.autosar.org/fileadmin/files/standards/classic/4-0/software-architecture/implementation-integration/standard/AUTOSAR_SWS_MemoryMapping.pdf?_sm_au_=iVVkW148vj2N42wj) | v1.3.0 R4.0 Rev 2              |
| 2           | MDD Guideline                                                                                                                                                                                                            | EA4 01.00.00                   |
| 3           | EA4 Software Naming Conventions                                                                                                                                                                                          | 01.01.00                       |
| 4           | Software Design and Coding Standards                                                                                                                                                                                     | 2.1                            |
| 5           | FDD – CF052A FordSysSt                                                                                                                                                                                                   | See Synergy subproject version |

{% endraw %}