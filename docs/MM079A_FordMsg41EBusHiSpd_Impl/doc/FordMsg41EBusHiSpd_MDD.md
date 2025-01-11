---
layout: default
title: FordMsg41EBusHiSpd_MDD
nav_order: 2
parent: Component Implementation
---
{% raw %}
**Module Design Document**

**For**

**FordMsg41EBusHiSpd**

**June 19, 20158**

**Prepared For:**

**Software Engineering**

**Nexteer Automotive,**

**Saginaw, MI, USA**

**Prepared By:**

**Nexteer ISC,**

**Bengaluru, INDIA.**

**<u>Change History</u>**

|             |                                       |             |             |             |
|---------|--------------------|----------------------|----------|-------------|
| **Sl. No.** | **Description**                       | **Author**  | **Version** | **Date**    |
| 1           | Initial Version                       | TATA        | 1.0         | 21-Nov-2017 |
| 2           | Updated based on Model Version V4.0.0 | Nexteer ISC | 2.0         | 23-Apr-2018 |

<u>Table of Contents</u>

[1 Introduction 5](#introduction)

[1.1 Purpose 5](#purpose)

[2 FordMsg41EBusHiSpd & High-Level Description
6](#fordmsg41ebushispd-high-level-description)

[3 Design details of software module
7](#design-details-of-software-module)

[3.1 Graphical representation of FordMsg41EBusHiSpd
7](#graphical-representation-of-fordmsg41ebushispd)

[3.2 Data Flow Diagram 7](#data-flow-diagram)

[3.2.1 Component level DFD 7](#component-level-dfd)

[3.2.2 Function level DFD 7](#function-level-dfd)

[4 Constant Data Dictionary 8](#constant-data-dictionary)

[4.1 Program (fixed) Constants 8](#program-fixed-constants)

[4.1.1 Embedded Constants 8](#embedded-constants)

[5 Software Component Implementation
9](#software-component-implementation)

[5.1 Sub-Module Functions 9](#sub-module-functions)

[5.1.1 Init: FordMsg41EBusHiSpdInit1 9](#init-fordmsg41ebushispdinit1)

[5.1.1.1 Design Rationale 9](#design-rationale)

[5.1.1.2 Module Outputs 9](#module-outputs)

[5.1.2 Per: FordMsg41EBusHiSpdPer1 9](#per-fordmsg41ebushispdper1)

[5.1.2.1 Design Rationale 9](#design-rationale-1)

[5.1.2.2 Store Module Inputs to Local copies
9](#store-module-inputs-to-local-copies)

[5.1.2.3 Processing of function 9](#processing-of-function)

[5.1.2.4 Store Local copy of outputs into Module Outputs
9](#store-local-copy-of-outputs-into-module-outputs)

[5.2 Server Runnables 9](#server-runnables)

[5.2.1 ComIPduCallout_BrakeSysFeatures_3_HS2_Oper
9](#comipducallout_brakesysfeatures_3_hs2_oper)

[5.2.1.1 Design Rationale 9](#design-rationale-2)

[5.2.1.2 (Processing of function) 9](#processing-of-function-1)

[5.2.2 ComTimeoutNotification_SelDrvMdeChassis2_D_Rq_Oper
9](#comtimeoutnotification_seldrvmdechassis2_d_rq_oper)

[5.2.2.1 Design Rationale 9](#design-rationale-3)

[5.2.2.2 (Processing of function) 9](#processing-of-function-2)

[5.3 Interrupt Functions 10](#interrupt-functions)

[5.4 Module Internal (Local) Functions
10](#module-internal-local-functions)

[5.4.1 Local Function \#1 10](#local-function-1)

[5.4.1.1 Design Rationale 10](#design-rationale-4)

[5.4.1.2 Processing 10](#processing)

[5.4.2 Local Function \#2 10](#_Toc512530778)

[5.4.2.1 Design Rationale 11](#_Toc512530779)

[5.4.2.2 Processing 11](#_Toc512530780)

[5.4.3 Local Function \#3 11](#_Toc512530781)

[5.4.3.1 Design Rationale 11](#_Toc512530782)

[5.4.3.2 Processing 11](#_Toc512530783)

[5.4.4 Local Function \#4 11](#_Toc512530784)

[5.4.4.1 Design Rationale 11](#_Toc512530785)

[5.4.4.2 Processing 12](#_Toc512530786)

[5.4.5 Local Function \#5 12](#_Toc512530787)

[5.4.5.1 Design Rationale 12](#_Toc512530788)

[5.4.5.2 Processing 12](#_Toc512530789)

[5.4.6 Local Function \#5 12](#_Toc512530790)

[5.4.6.1 Design Rationale 13](#_Toc512530791)

[5.4.6.2 Processing 13](#_Toc512530792)

[5.4.7 GLOBAL Function/Macro Definitions 13](#_Toc512530869)

[6 Known Limitations with Design 14](#known-limitations-with-design)

[7 UNIT TEST CONSIDERATION 15](#unit-test-consideration)

[Appendix A Abbreviations and Acronyms 16](#abbreviations-and-acronyms)

[Appendix B Glossary 17](#glossary)

[Appendix C References 18](#references)

# Introduction

## Purpose

MDD for FordMsg41EBusHiSpd

# FordMsg41EBusHiSpd & High-Level Description

Please refer FDD.

# Design details of software module

## Graphical representation of FordMsg41EBusHiSpd

<img
src="ElectricPowerSteering_RH850_FORD_T3T6_website/docs/MM079A_FordMsg41EBusHiSpd_Impl/doc/mediax/media/image2.png"
style="width:3.86111in;height:3.04792in" />

## Data Flow Diagram

### Component level DFD

> Please refer FDD.

### Function level DFD

> Please refer FDD.

# Constant Data Dictionary

## Program (fixed) Constants

### Embedded Constants

#### Local Constants

| Constant Name                        | Resolution | Units | Value |
|--------------------------------------|------------|-------|-------|
| Please refer Data Dictionary .m file | NA         | NA    | NA    |

# Software Component Implementation

## Sub-Module Functions

###  Init: FordMsg41EBusHiSpdInit1

### 5.1.1.1 Design Rationale [design-rationale]

> None

### 5.1.1.2 Module Outputs [module-outputs]

> None

### 5.1.2 Per: FordMsg41EBusHiSpdPer1 [per-fordmsg41ebushispdper1]

## 5.1.2.1 Design Rationale [design-rationale-1]

> None

## 5.1.2.2 Store Module Inputs to Local copies [store-module-inputs-to-local-copies]

> None

## 5.1.2.3 Processing of function [processing-of-function]

> None

## 5.1.2.4 Store Local copy of outputs into Module Outputs [store-local-copy-of-outputs-into-module-outputs]

> None

## Server Runnables

###  5.2.1 ComIPduCallout_BrakeSysFeatures_3_HS2_Oper [comipducallout_brakesysfeatures_3_hs2_oper]

## 5.2.1.1 Design Rationale [design-rationale-2]

None

## 5.2.1.2 (Processing of function) [processing-of-function-1]

None

### 5.2.2 ComTimeoutNotification_SelDrvMdeChassis2_D_Rq_Oper [comtimeoutnotification_seldrvmdechassis2_d_rq_oper]

## 5.2.2.1 Design Rationale [design-rationale-3]

None

## 5.2.2.2 (Processing of function) [processing-of-function-2]

None

##  [section]

## Interrupt Functions

None

## Module Internal (Local) Functions

## Local Function \#1

|                      |                                   |         |       |      |
|--------|-------------------------------------------|---------|-------|-------|
| **Function Name**    | DiagEna                           | Type    | Min   | Max  |
| **Arguments Passed** | FordCanDtcInhb_Cnt_T_logl         | boolean | FALSE | TRUE |
|                      |                                   |         |       |      |
|                      | ClrDiagcFlgProxy_Cnt_T_u08        | uint8   | 0U    | 1U   |
|                      | FordSelDrvModEnad_Cnt_T_logl      | boolean | FALSE | TRUE |
|                      |                                   |         |       |      |
|                      |                                   |         |       |      |
|                      | \* DiagEna_Cnt_T_logl             | boolean | FALSE | TRUE |
|                      | \* ClrDiagcFlgProxyEna_Cnt_T_logl | boolean | FALSE | TRUE |
| **Return Value**     | NA                                | NA      | NA    | NA   |

## Design Rationale

None

## Processing

Please refer to the below path in the FDD model.

MM079A_FordMsg41EBusHiSpd/FordMsg41EBusHiSpd/FordMsg41EBusHiSpdPer1/DiagEna

## Local Function \#2

|                      |                                |         |       |        |
|---------|------------------------------------------|---------|-------|-------|
| **Function Name**    | MsgMiss                        | Type    | Min   | Max    |
| **Arguments Passed** | DiagEna_Cnt_T_logl             | boolean | FALSE | TRUE   |
|                      | ClrDiagcFlgProxyEna_Cnt_T_logl | boolean | FALSE | TRUE   |
|                      | BusHiSpdMissMsgThd_Cnt_T_u16   | Uint16  | 0U    | 65535U |
| **Return Value**     | NA                             | NA      | NA    | NA     |

## Design Rationale

None

## Processing

Please refer to the below path in the FDD model.

MM079A_FordMsg41EBusHiSpd_400/FordMsg41EBusHiSpd/FordMsg41EBusHiSpdPer1/Msg_Missing

## Local Function \#3

|                      |                                          |         |       |      |
|---------|------------------------------------------|---------|-------|-------|
| **Function Name**    | ChkElpdTi                                | Type    | Min   | Max  |
| **Arguments Passed** | FordVehSelDrvModChassisVldInp_Cnt_T_logl | boolean | FALSE | TRUE |
|                      | VldElpdTi_Cnt_T_logl                     | boolean | FALSE | TRUE |
|                      | InvldElpdTi_Cnt_T_logl                   | boolean | FALSE | TRUE |
| **Return Value**     | \*FordVehSelDrvModChassisVld_Cnt_T_logl  | boolean | FALSE | TRUE |

## Design Rationale

None

## Processing

Please refer to the below path in the FDD model.

MM079A_FordMsg41EBusHiSpd_400/FordMsg41EBusHiSpd/FordMsg41EBusHiSpdPer1/Msg_Present/OutputProcessing/ChkElpdTi

## Local Function \#4

|                      |                                   |         |       |        |
|---------|------------------------------------------|---------|-------|-------|
| **Function Name**    | FordVehSelDrvModChassisVldInpNtc  | Type    | Min   | Max    |
| **Arguments Passed** | FordVehPenSelDrvModVld_Cnt_T_logl | boolean | FALSE | TRUE   |
|                      | BusHiSpdInvldThd_Cnt_T_u16        | Uint16  | 0U    | 65535U |
| **Return Value**     | NA                                | NA      | NA    | NA     |

## Design Rationale

None

## Processing

Please refer to the below path in the FDD model.

MM079A_FordMsg41EBusHiSpd_400/FordMsg41EBusHiSpd/FordMsg41EBusHiSpdPer1/Msg_Present/OutputProcessing/FordVehPenSelDrvModSelnProcessing

## Local Function \#5

|                      |                                          |         |       |      |
|---------|------------------------------------------|---------|-------|-------|
| **Function Name**    | VldElpdTi                                | Type    | Min   | Max  |
| **Arguments Passed** | FordVehSelDrvModChassisVldInp_Cnt_T_logl | boolean | FALSE | TRUE |
|                      | \*VldElpdTi_Cnt_T_logl                   | boolean | FALSE | TRUE |
|                      | \*InvldElpdTi_Cnt_T_logl                 | boolean | FALSE | TRUE |
|                      | \*FordVehSelDrvModChassisVld_Cnt_T_logl  | boolean | FALSE | TRUE |
| **Return Value**     | NA                                       | NA      | NA    | NA   |

## Design Rationale

None

## Processing

Please refer to the below path in the FDD model.

MM079A_FordMsg41EBusHiSpd_400/FordMsg41EBusHiSpd/FordMsg41EBusHiSpdPer1/Msg_Present/OutputProcessing/VldElpdTi

## Local Function \#6

|                      |                                         |         |       |      |
|---------|------------------------------------------|---------|-------|-------|
| **Function Name**    | CalSeln                                 | Type    | Min   | Max  |
| **Arguments Passed** | FordEpsLifeCycMod_Cnt_T_u08             | Uint8   | 0U    | 1U   |
|                      | \*VldElpdTi_Cnt_T_logl                  | boolean | FALSE | TRUE |
|                      | \*InvldElpdTi_Cnt_T_logl                | boolean | FALSE | TRUE |
|                      | \*FordVehSelDrvModChassisVld_Cnt_T_logl | boolean | FALSE | TRUE |
| **Return Value**     | NA                                      | NA      | NA    | NA   |

## Design Rationale

None

## Processing

Please refer to the below path in the FDD model.

MM079A_FordMsg41EBusHiSpd_400/FordMsg41EBusHiSpd/FordMsg41EBusHiSpdPer1/CalSeln

## 

## 

|     |     |     |     |     |
|-----|-----|-----|-----|-----|
|     |     |     |     |     |
|     |     |     |     |     |
|     |     |     |     |     |
|     |     |     |     |     |
|     |     |     |     |     |
|     |     |     |     |     |

## 

## 

## 

## 

|       |     |     |     |     |
|-------|-----|-----|-----|-----|
|       |     |     |     |     |
|       |     |     |     |     |
|       |     |     |     |     |
|       |     |     |     |     |

## 

## 

## GLOBAL Function/Macro Definitions

None

# Known Limitations with Design

> None.

# UNIT TEST CONSIDERATION

> None.

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

| **Ref. \#** | **Title**                                                                                                                                                             | **Version**                     |
|-------|-------------------------------------------------|-----------------|
| 1           | AUTOSAR Specification of Memory Mapping (Link:[AUTOSAR_SWS_MemoryMapping.pdf](http://www.autosar.org/download/R4.0/AUTOSAR_SWS_MemoryMapping.pdf))                    | v1.3.0 R4.0 Rev 2               |
| 2           | MDD Guideline                                                                                                                                                         | EA4 01.00.00                    |
| 3           | [Software Naming Conventions.doc](http://misagweb01.nexteer.com/eRoomReq/Files/erooms8/NextGeneration/0_fc55f/Software%20Naming%20Conventions%2003x(In%20Work).doc)   | 1.0                             |
| 4           | [Software Design and Coding Standards.doc](http://eroom1.nexteer.com/eRoomReq/Files/erooms8/NextGeneration/0_1a67a9/Software%20Design%20and%20Coding%20Standards.doc) | 2.1                             |
| 5           | FDD: MM079A_FordMsg41EBusHiSpd_Design                                                                                                                                 | See Synergy sub project version |

{% endraw %}