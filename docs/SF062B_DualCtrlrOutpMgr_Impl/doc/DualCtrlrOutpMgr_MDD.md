---
layout: default
title: DualCtrlrOutpMgr_MDD
nav_order: 2
parent: Component Implementation
---
{% raw %}
**Module Design Document**

**For**

**DualCtrlrOutpMgr**

**18-Oct-2017**

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
| Initial version | Shawn Penning | 1.0         | 18-Oct-2017 |

**  
**

<u>Table of Contents</u>

[1 DualCtrlrOutpMgr High-Level Description
[4](#dualctrlroutpmgr-high-level-description)](#dualctrlroutpmgr-high-level-description)

[2 Design details of software module
[5](#design-details-of-software-module)](#design-details-of-software-module)

[2.1 Graphical representation of DualCtrlrOutpMgr
[5](#graphical-representation-of-dualctrlroutpmgr)](#graphical-representation-of-dualctrlroutpmgr)

[2.2 Data Flow Diagram [5](#data-flow-diagram)](#data-flow-diagram)

[2.2.1 Component level DFD
[5](#component-level-dfd)](#component-level-dfd)

[2.2.2 Function level DFD [5](#function-level-dfd)](#function-level-dfd)

[3 Constant Data Dictionary
[6](#constant-data-dictionary)](#constant-data-dictionary)

[3.1 Program (fixed) Constants
[6](#program-fixed-constants)](#program-fixed-constants)

[3.1.1 Embedded Constants [6](#embedded-constants)](#embedded-constants)

[4 Software Component Implementation
[7](#software-component-implementation)](#software-component-implementation)

[4.1 Sub-Module Functions
[7](#sub-module-functions)](#sub-module-functions)

[4.1.1 Init: DualCtrlrOutpMgrInit1
[7](#init-dualctrlroutpmgrinit1)](#init-dualctrlroutpmgrinit1)

[4.1.1.1 Design Rationale [7](#design-rationale)](#design-rationale)

[4.1.1.2 Module Outputs [7](#module-outputs)](#module-outputs)

[4.1.2 Init: DualCtrlrOutpMgrPer1
[7](#per1-dualctrlroutpmgrper1)](#per1-dualctrlroutpmgrper1)

[4.1.2.1 Design Rationale [7](#design-rationale-1)](#design-rationale-1)

[4.1.2.2 Module Outputs [7](#module-outputs-1)](#module-outputs-1)

[4.2 Server Runables [7](#server-runables)](#server-runables)

[4.3 Interrupt Functions
[7](#interrupt-functions)](#interrupt-functions)

[4.3.1 Interrupt Function Name
[7](#interrupt-function-name)](#interrupt-function-name)

[4.4 Module Internal (Local) Functions
[8](#module-internal-local-functions)](#module-internal-local-functions)

[4.4.1 Local Function \#1 [8](#local-function-1)](#local-function-1)

[4.4.1.1 Design Rationale [8](#design-rationale-3)](#design-rationale-3)

[4.4.1.2 Processing [8](#processing)](#processing)

[4.5 GLOBAL Function/Macro Definitions
[8](#global-functionmacro-definitions)](#global-functionmacro-definitions)

[5 Known Limitations with Design
[9](#known-limitations-with-design)](#known-limitations-with-design)

[6 UNIT TEST CONSIDERATION
[10](#unit-test-consideration)](#unit-test-consideration)

[Appendix A Abbreviations and Acronyms
[11](#abbreviations-and-acronyms)](#abbreviations-and-acronyms)

[Appendix B Glossary [12](#glossary)](#glossary)

[Appendix C Please references
[13](#please-references)](#please-references)

# DualCtrlrOutpMgr High-Level Description

Refer to FDD

# Design details of software module

Refer to FDD

## Graphical representation of DualCtrlrOutpMgr

<img
src="ElectricPowerSteering_RH850_FORD_T3T6_website/docs/SF062B_DualCtrlrOutpMgr_Impl/doc/mediax/media/image1.png"
style="width:3.53125in;height:4.83333in" />

## Data Flow Diagram

Refer to FDD

### Component level DFD

Refer to FDD

### Function level DFD

Refer to FDD

# Constant Data Dictionary

## Program (fixed) Constants

### Embedded Constants

#### Local Constants

| Constant Name                  | Resolution | Units | Value |
|--------------------------------|------------|-------|-------|
| Refer to .m file for constants |            |       |       |

# Software Component Implementation

## Sub-Module Functions

## Init: DualCtrlrOutpMgrInit1

## Design Rationale

Refer to FDD

## Module Outputs

None

## Per1: DualCtrlrOutpMgrPer1

## Design Rationale

Refer to FDD.

ElapsedTimeFlag function is used to avoid the repetitive code and make
optimization.

## Module Outputs

None

## Per2: DualCtrlrOutpMgrPer2

## Design Rationale

Refer to FDD.

ElapsedTimeFlag function is used to avoid the repetitive code and make
optimization.

## Module Outputs

None

## Server Runables 

None

## Interrupt Functions

None

## Interrupt Function Name

None

## Module Internal (Local) Functions

## Local Function \#1

|                      |                        |         |       |             |
|----------------------|------------------------|---------|-------|-------------|
| **Function Name**    | ElapsedTimeFlag        | Type    | Min   | Max         |
| **Arguments Passed** | PrmTmrThd_Cnt_T_u16    | uint16  | 0U    | 1000        |
|                      | FltStsFlag1_Cnt_T_logl | boolean | FALSE | TRUE        |
|                      | \*PimFlag_Cnt_T_logl   | boolean | FALSE | TRUE        |
|                      | \*PimTmr_Cnt_T_u32     | uint32  | 0U    | 4294967295U |
|                      | PimFlgPrev_Cnt_T_logl  | boolean | FALSE | TRUE        |
|                      | \*OutpFlg_Cnt_T_logl   | boolean | FALSE | TRUE        |
| **Return Value**     | NA                     | NA      | NA    | NA          |

## Design Rationale

Implementation of 'ElapsedTimeX' block (X=1,2,3 etc).

## Processing

Please refer 'ElapsedTimeX' block (X=1,2,3 etc).

## Local Function \#2

|                      |                                      |         |       |      |
|-------------|-----------------------------|----------|----------|-----------|
| **Function Name**    | Andoper                              | Type    | Min   | Max  |
| **Arguments Passed** | ImcDualMotCtrlMtgtnEnaVld_Cnt_T_logl | boolean | FALSE | TRUE |
|                      | ImcDualMotCtrlMtgtnEna_Cnt_T_logl    | boolean | FALSE | TRUE |
| **Return Value**     |                                      | boolean | FALSE | TRUE |

## Design Rationale

Implementation of 'Andoper' block (X=1,2,3 etc).

## Processing

Please refer ‘Andoper' block (X=1,2,3 etc).

## Local Function \#3

|                      |                                  |         |       |      |
|-------------|-----------------------------|----------|----------|-----------|
| **Function Name**    | Decoder                          | Type    | Min   | Max  |
| **Arguments Passed** | MotAndThermProtnLoaMod_Cnt_T_u08 | uint8   | 0U    | 1000 |
| **Return Value**     |                                  | boolean | FALSE | TRUE |

## Design Rationale

Implementation of 'Decoder' block (X=1,2,3 etc).

## Processing

Please refer 'Decoder' block (X=1,2,3 etc).

## GLOBAL Function/Macro Definitions

None

# Known Limitations with Design

None.

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

-   Automotive SPICE® Process Please reference Model (PRM)

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

####### Please references

| **Ref. \#** | **Title**                                                                                                                                                             | **Version**                    |
|-------|-------------------------------------------------|-----------------|
| 1           | AUTOSAR Specification of Memory Mapping (Link:[AUTOSAR_SWS_MemoryMapping.pdf](http://www.autosar.org/download/R4.0/AUTOSAR_SWS_MemoryMapping.pdf))                    | v1.3.0 R4.0 Rev 2              |
| 2           | MDD Guideline                                                                                                                                                         | EA4 01.00.00                   |
| 3           | [Software Naming Conventions.doc](http://misagweb01.nexteer.com/eRoomReq/Files/erooms8/NextGeneration/0_fc55f/Software%20Naming%20Conventions%2003x(In%20Work).doc)   | 2.0                            |
| 4           | [Software Design and Coding Standards.doc](http://eroom1.nexteer.com/eRoomReq/Files/erooms8/NextGeneration/0_1a67a9/Software%20Design%20and%20Coding%20Standards.doc) | 2.1                            |
| 5           | FDD: SF062B_DualCtrlrOutpMgr_Design                                                                                                                                   | See Synergy subproject version |

{% endraw %}