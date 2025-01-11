---
layout: default
title: MotAgSwCal_MDD
nav_order: 2
parent: Component Implementation
---
{% raw %}
**Module Design Document**

**For**

**MotAgSwCal**

**23-AUG-2017**

**Prepared By:**

**Shruthi Raghavan,**

**Nexteer Automotive,**

**Saginaw, MI, USA  
<u>Change History</u>**

|                 |                  |             |             |
|-----------------|------------------|-------------|-------------|
| **Description** | **Author**       | **Version** | **Date**    |
| Initial Version | Shruthi Raghavan | 1.0         | 15-Jul-2015 |

**  
**

**<u>Table of Contents</u>**

[1 Introduction [2](#introduction)](#introduction)

[1.1 Purpose [2](#purpose)](#purpose)

[1.2 Scope [2](#_Toc424732604)](#_Toc424732604)

[2 \<Component Name\> & High-Level Description
[2](#_Toc424732605)](#_Toc424732605)

[3 Design details of software module
[2](#design-details-of-software-module)](#design-details-of-software-module)

[3.1 Graphical representation of \<Component Name\>
[2](#graphical-representation-of-motagswcal)](#graphical-representation-of-motagswcal)

[3.2 Data Flow Diagram [2](#data-flow-diagram)](#data-flow-diagram)

[3.2.1 Component level DFD
[2](#component-level-dfd)](#component-level-dfd)

[3.2.2 Function level DFD [2](#function-level-dfd)](#function-level-dfd)

[4 Constant Data Dictionary
[2](#constant-data-dictionary)](#constant-data-dictionary)

[4.1 Program (fixed) Constants
[2](#program-fixed-constants)](#program-fixed-constants)

[4.1.1 Embedded Constants [2](#embedded-constants)](#embedded-constants)

[5 Software Component Implementation
[2](#software-component-implementation)](#software-component-implementation)

[5.1 Sub-Module Functions
[2](#sub-module-functions)](#sub-module-functions)

[5.1.1 Init: \<ModuleName\>Init\<n\>
[2](#init-motagswcalinit1)](#init-motagswcalinit1)

[5.1.1.1 Design Rationale [2](#design-rationale)](#design-rationale)

[5.1.1.2 Module Outputs [2](#_Toc424732618)](#_Toc424732618)

[5.1.2 Per: \<ModuleName\>\_Per\<n\>
[2](#per-motagswcalper1)](#per-motagswcalper1)

[5.1.2.1 Design Rationale [2](#design-rationale-1)](#design-rationale-1)

[5.1.2.2 Store Module Inputs to Local copies
[2](#_Toc424732621)](#_Toc424732621)

[5.1.2.3 (Processing of function)………
[2](#_Toc424732622)](#_Toc424732622)

[5.1.2.4 Store Local copy of outputs into Module Outputs
[2](#_Toc424732623)](#_Toc424732623)

[5.2 Server Runables [2](#server-runables)](#server-runables)

[5.2.1 \<Server Runable Name\> [2](#swcalgetprm)](#swcalgetprm)

[5.2.1.1 Design Rationale [2](#design-rationale-3)](#design-rationale-3)

[5.2.1.2 (Processing of function)………
[2](#_Toc424732627)](#_Toc424732627)

[5.3 Interrupt Functions
[2](#interrupt-functions)](#interrupt-functions)

[5.3.1 Interrupt Function Name [2](#_Toc424732629)](#_Toc424732629)

[5.3.1.1 Design Rationale [2](#_Toc424732630)](#_Toc424732630)

[5.3.1.2 (Processing of the ISR function)…..
[2](#_Toc424732631)](#_Toc424732631)

[5.4 Module Internal (Local) Functions
[2](#module-internal-local-functions)](#module-internal-local-functions)

[5.4.1 Local Function \#1 [2](#local-function-1)](#local-function-1)

[5.4.1.1 Design Rationale [2](#design-rationale-7)](#design-rationale-7)

[5.4.1.2 Processing [2](#_Toc424732635)](#_Toc424732635)

[5.5 GLOBAL Function/Macro Definitions
[2](#global-functionmacro-definitions)](#global-functionmacro-definitions)

[5.5.1 GLOBAL Function \#1 [2](#global-function-1)](#global-function-1)

[5.5.1.1 Design Rationale
[2](#design-rationale-10)](#design-rationale-10)

[5.5.1.2 processing [2](#_Toc424732639)](#_Toc424732639)

[6 Known Limitations with Design
[2](#known-limitations-with-design)](#known-limitations-with-design)

[7 UNIT TEST CONSIDERATION
[2](#unit-test-consideration)](#unit-test-consideration)

[Appendix A Abbreviations and Acronyms
[2](#abbreviations-and-acronyms)](#abbreviations-and-acronyms)

[Appendix B Glossary [2](#glossary)](#glossary)

[Appendix C References [2](#references)](#references)

# Introduction

## Purpose

Module design document for MotAgSwCal component.

# MotAgSwCal & High-Level Description

> This component is used to determine the calibration parameters of the
> hall sensor based on motor angle data samples. A modulation index
> profile is fenerated based on process parameters and average motor
> angle is calculated and sent out using a client call when the data is
> ready.

# Design details of software module

## Graphical representation of MotAgSwCal

<img
src="ElectricPowerSteering_RH850_FORD_T3T6_website/docs/ES280A_MotAgSwCal_Impl/doc/mediax/media/image1.png"
style="width:2.03307in;height:1.26191in" />

## Data Flow Diagram

### Component level DFD

> Refer FDD Simulink Model

### Function level DFD 

> Refer FDD Simulink Model

# Constant Data Dictionary

## Program (fixed) Constants

### Embedded Constants

#### Local Constants

| Constant Name                    | Resolution | Units      | Value                                                           |
|----------------------|-------------|---------|-----------------------------|
| POSNSTEPSIZEDFT_MOTREVELEC_U0P16 | P16        | MotRevElec | FloatToFixd_u16_f32(0.031250477F,NXTRFIXDPT_FLOATTOP16_ULS_F32) |
| PSBLNROFMOTAGMEAS_CNT_U08        | 1          | Cnt        | 6U                                                              |
| PSBLNROFSINCOSCPT_CNT_U08        | 1          | Cnt        | PSBLNROFMOTAGMEAS_CNT_U08\*2                                    |

# Software Component Implementation

## Sub-Module Functions

## Init: MotAgSwCalInit1

## Design Rationale

None.

## Per: MotAgSwCalPer1

## Design Rationale

None

## Per: MotAgSwCalPer2

## Design Rationale

None

## Server Runables 

## SwCalGetPrm

## Design Rationale

None

## SwCalSetPrm

## Design Rationale

None

## SwCalStop

## Design Rationale

None

## SwCalStrt

## Design Rationale

None

## Interrupt Functions

> None

## Module Internal (Local) Functions

## Local Function \#1

|                      |           |      |     |     |
|----------------------|-----------|------|-----|-----|
| **Function Name**    | RstFctPrm | Type | Min | Max |
| **Arguments Passed** | None      | \-   | \-  | \-  |
| **Return Value**     | N/A       | \-   | \-  | \-  |

## Design Rationale

> None.

## Local Function \#2

|                      |                              |         |      |             |
|---------------|--------------------------------|---------|---------|---------|
| **Function Name**    | CalcMotAgDelta               | Type    | Min  | Max         |
| **Arguments Passed** | CurrMotAgCptVal_Volt_T_f32   | Float32 | 0.0F | 5.0F        |
|                      | \* PrevMotAgCptVal_Cnt_T_u16 | U3p13   | 0.0F | 7.99987792F |
| **Return Value**     | MotAgDelta_Cnt_T_u16         | Uint16  | 0U   | 65535U      |

## Design Rationale

> None.

## Local Function \#3

|                      |                  |      |     |     |
|----------------------|------------------|------|-----|-----|
| **Function Name**    | UpdFaildAdcCntrs | Type | Min | Max |
| **Arguments Passed** | None             | \-   | \-  | \-  |
| **Return Value**     | N/A              | \-   | \-  | \-  |

## Design Rationale

> None.

1.  **Local Function \#4**

|                      |           |      |     |     |
|----------------------|-----------|------|-----|-----|
| **Function Name**    | UpdTiOuts | Type | Min | Max |
| **Arguments Passed** | None      | \-   | \-  | \-  |
| **Return Value**     | N/A       | \-   | \-  | \-  |

1.  **Design Rationale**

> None.

## GLOBAL Function/Macro Definitions

## GLOBAL Function \#1

|                      |     |      |     |     |
|----------------------|-----|------|-----|-----|
| **Function Name**    | \-  | Type | Min | Max |
| **Arguments Passed** | \-  | \-   | \-  | \-  |
| **Return Value**     | \-  | \-   | \-  | \-  |

## Design Rationale

N/A

# Known Limitations with Design

See Continuous Improvement CR EA4#15533

# UNIT TEST CONSIDERATION

> Intentional rollovers and cast overflows are explicitly indicated in
> the code.

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

| **Ref. \#** | **Title**                                                                                                                                                           | **Version**       |
|-------|-------------------------------------------------|-----------------|
| 1           | AUTOSAR Specification of Memory Mapping                                                                                                                             | v1.3.0 R4.0 Rev 2 |
| 2           | MDD Guideline                                                                                                                                                       | EA4 01.00.01      |
| 3           | [Software Naming Conventions.doc](http://misagweb01.nexteer.com/eRoomReq/Files/erooms8/NextGeneration/0_fc55f/Software%20Naming%20Conventions%2003x(In%20Work).doc) | 1.0               |
| 4           | Software Design and Coding Standards.doc                                                                                                                            | 2.1               |

{% endraw %}