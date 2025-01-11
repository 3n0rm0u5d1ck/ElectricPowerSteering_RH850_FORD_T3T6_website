---
layout: default
title: FordMsg217BusHiSpd_MDD
nav_order: 2
parent: Component Implementation
---
{% raw %}
**Module Design Document**

**For**

**FordMsg217BusHiSpd**

**June 19, 20157**

**Prepared For:**

**Software Engineering**

**Nexteer Automotive,**

**Saginaw, MI, USA**

**Prepared By:**

**Tata Elxsi,**

**Trivandrum, INDIA**

**<u>Change History</u>**

|             |                 |            |             |             |
|-------------|-----------------|------------|-------------|-------------|
| **Sl. No.** | **Description** | **Author** | **Version** | **Date**    |
| 1           | Initial Version | TATA       | 1.0         | 29-Nov-2017 |

**<u>Table of Contents</u>**

[1 Introduction [5](#introduction)](#introduction)

[1.1 Purpose [5](#purpose)](#purpose)

[2 FordMsg217BusHiSpd & High-Level Description
[6](#fordmsg217bushispd-high-level-description)](#fordmsg217bushispd-high-level-description)

[3 Design details of software module
[7](#design-details-of-software-module)](#design-details-of-software-module)

[3.1 Graphical representation of FordMsg217BusHiSpd
[7](#graphical-representation-of-fordmsg217bushispd)](#graphical-representation-of-fordmsg217bushispd)

[3.2 Data Flow Diagram [7](#data-flow-diagram)](#data-flow-diagram)

[Component level DFD [7](#component-level-dfd)](#component-level-dfd)

[Function level DFD [7](#function-level-dfd)](#function-level-dfd)

[4 Constant Data Dictionary
[8](#constant-data-dictionary)](#constant-data-dictionary)

[4.1 Program (fixed) Constants
[8](#program-fixed-constants)](#program-fixed-constants)

[Embedded Constants [8](#embedded-constants)](#embedded-constants)

[5 Software Component Implementation
[9](#software-component-implementation)](#software-component-implementation)

[5.1 Sub-Module Functions
[9](#sub-module-functions)](#sub-module-functions)

[5.1.1 Init: FordMsg217BusHiSpdInit1
[9](#init-fordmsg217bushispdinit1)](#init-fordmsg217bushispdinit1)

[5.1.1.1 Design Rationale [9](#design-rationale)](#design-rationale)

[5.1.1.2 Module Outputs [9](#module-outputs)](#module-outputs)

[5.1.2 Per: FordMsg217BusHiSpdPer1
[9](#per-fordmsg217bushispdper1)](#per-fordmsg217bushispdper1)

[5.1.2.1 Design Rationale [9](#design-rationale-1)](#design-rationale-1)

[5.1.2.2 Store Module Inputs to Local copies
[9](#store-module-inputs-to-local-copies)](#store-module-inputs-to-local-copies)

[5.1.2.3 Processing of function
[9](#processing-of-function)](#processing-of-function)

[5.1.2.4 Store Local copy of outputs into Module Outputs
[9](#store-local-copy-of-outputs-into-module-outputs)](#store-local-copy-of-outputs-into-module-outputs)

[5.2 Server Runnables [9](#server-runnables)](#server-runnables)

[5.2.1 ComIPduCallout_BrakeSysFeatures_3_HS2_Oper
[9](#comipducallout_brakesysfeatures_3_hs2_oper)](#comipducallout_brakesysfeatures_3_hs2_oper)

[5.2.1.1 Design Rationale [9](#design-rationale-2)](#design-rationale-2)

[5.2.1.2 Processing of function
[9](#processing-of-function-1)](#processing-of-function-1)

[5.2.2 ComTimeoutNotification_SelDrvMdeChassis2_D_Rq_Oper
[9](#comtimeoutnotification_seldrvmdechassis2_d_rq_oper)](#comtimeoutnotification_seldrvmdechassis2_d_rq_oper)

[5.2.2.1 Design Rationale [9](#design-rationale-3)](#design-rationale-3)

[5.2.2.2 Processing of function
[9](#processing-of-function-2)](#processing-of-function-2)

[5.3 Interrupt Functions
[10](#interrupt-functions)](#interrupt-functions)

[5.4 Module Internal (Local) Functions
[10](#module-internal-local-functions)](#module-internal-local-functions)

[5.4.1 Local Function \#1 [10](#local-function-1)](#local-function-1)

[5.4.1.1 Design Rationale
[10](#design-rationale-4)](#design-rationale-4)

[5.4.1.2 Processing [10](#processing)](#processing)

[5.4.2 Local Function \#2 [10](#local-function-2)](#local-function-2)

[5.4.2.1 Design Rationale
[11](#design-rationale-5)](#design-rationale-5)

[5.4.2.2 Processing [11](#processing-1)](#processing-1)

[5.4.3 Local Function \#3 [11](#local-function-3)](#local-function-3)

[5.4.3.1 Design Rationale
[11](#design-rationale-6)](#design-rationale-6)

[5.4.3.2 Processing [11](#processing-2)](#processing-2)

[5.4.4 Local Function \#4 [11](#local-function-4)](#local-function-4)

[5.4.4.1 Design Rationale
[12](#design-rationale-7)](#design-rationale-7)

[5.4.4.2 Processing [12](#processing-3)](#processing-3)

[5.4.5 Local Function \#5 [12](#local-function-5)](#local-function-5)

[5.4.5.1 Design Rationale
[13](#design-rationale-8)](#design-rationale-8)

[5.4.5.2 Processing [13](#processing-4)](#processing-4)

[5.4.6 Local Function \#6 [13](#local-function-6)](#local-function-6)

[5.4.6.1 Design Rationale
[13](#design-rationale-9)](#design-rationale-9)

[5.4.6.2 Processing [13](#processing-5)](#processing-5)

[5.4.7 Local Function \#7 [14](#local-function-7)](#local-function-7)

[5.4.7.1 Design Rationale
[14](#design-rationale-10)](#design-rationale-10)

[5.4.7.2 Processing [14](#processing-6)](#processing-6)

[5.4.8 Local Function \#8 [14](#local-function-8)](#local-function-8)

[5.4.8.1 Design Rationale
[14](#design-rationale-11)](#design-rationale-11)

[5.4.8.2 Processing [14](#processing-7)](#processing-7)

[5.5 GLOBAL Function/Macro Definitions
[15](#global-functionmacro-definitions)](#global-functionmacro-definitions)

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

MDD for FordMsg217BusHiSpd

# FordMsg217BusHiSpd & High-Level Description

Please refer FDD.

# Design details of software module

## Graphical representation of FordMsg217BusHiSpd

<img
src="ElectricPowerSteering_RH850_FORD_T3T6_website/docs/MM065A_FordMsg217BusHiSpd_Impl/doc/mediax/media/image1.png"
style="width:4in;height:5.95833in" />

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

### 5.1.1 Init: FordMsg217BusHiSpdInit1

### 5.1.1.1 Design Rationale

> None

### 5.1.1.2 Module Outputs

> None

### 5.1.2 Per: FordMsg217BusHiSpdPer1

## 5.1.2.1 Design Rationale [design-rationale-1]

> None

## 5.1.2.2 Store Module Inputs to Local copies [store-module-inputs-to-local-copies]

> None

## 5.1.2.3 Processing of function [processing-of-function]

> None

## 5.1.2.4 Store Local copy of outputs into Module Outputs [store-local-copy-of-outputs-into-module-outputs]

> None

## Server Runnables 

### 5.2.1 ComIPduCallout_BrakeSysFeatures_3_HS2_Oper

## 5.2.1.1 Design Rationale [design-rationale-2]

None

## 5.2.1.2 Processing of function [processing-of-function-1]

None

### 5.2.2 ComTimeoutNotification_SelDrvMdeChassis2_D_Rq_Oper

## 5.2.2.1 Design Rationale [design-rationale-3]

None

## 5.2.2.2 Processing of function [processing-of-function-2]

None

## Interrupt Functions

None

## Module Internal (Local) Functions

##  Local Function \#1

|                      |                                  |         |       |      |
|------------|------------------------------|---------|-----------|-----------|
| **Function Name**    | DiagEna                          | Type    | Min   | Max  |
| **Arguments Passed** | FordMissMsgDiagcInhb_Cnt_T_u08   | uint8   | 0U    | 1U   |
|                      | FordInvldMsgDiagcInhb_Cnt_T_u08  | uint8   | 0U    | 1U   |
|                      | ClrDiagcFlgProxy_Cnt_T_u08       | uint8   | 0U    | 1U   |
|                      | FordMfgDiagcInhb_Cnt_T_u08       | uint8   | 0U    | 1U   |
|                      | FordCanDtcInhb_Cnt_T_u08         | uint8   | 0U    | 1U   |
|                      | FordAbsPrsnt_Cnt_T_u08           | uint8   | 0U    | 1U   |
|                      | FordActvNiblCtrlEnad_Cnt_T_u08   | uint8   | 0U    | 1U   |
|                      | FordBrkOscnRednEnad_Cnt_T_u08    | uint8   | 0U    | 1U   |
|                      | FordTqSteerCmpEnad_Cnt_T_u08     | uint8   | 0U    | 1U   |
|                      | FordTrlrBackupAssiEnad_Cnt_T_u08 | uint8   | 0U    | 1U   |
|                      | \*MissMsgDiagEna_Cnt_T_logl      | boolean | FALSE | TRUE |
|                      | \*FrntWhlSpdDiagEna_Cnt_T_logl   | boolean | FALSE | TRUE |
|                      | \*ReWhlSpdDiagEna_Cnt_T_logl     | boolean | FALSE | TRUE |
| **Return Value**     | NA                               | NA      | NA    | NA   |

## Design Rationale

None

## Processing

Please refer to the below path in the FDD model.

MM065A_FordMsg217BusHiSpd/FordMsg217BusHiSpd/FordMsg217BusHiSpdPer1/DiagEna

##  Local Function \#2

|                      |                                                   |        |     |       |
|-----------|-----------------------------------|--------|----------|---------|
| **Function Name**    | CalSeln                                           | Type   | Min | Max   |
| **Arguments Passed** | FordEpsLifeCycMod_Cnt_T_u08                       | uint8  | 0U  | 1U    |
|                      | BusHiSpdMissMsgFaildThd_MilliSec_T_u16p0          | uint16 | 0U  | 6000U |
|                      | \*FrntLeWhlBusHiSpdInvldFaildThd_MilliSec_T_u16p0 | uint16 | 0U  | 6000U |
|                      | \*FrntRiWhlBusHiSpdInvldFaildThd_MilliSec_T_u16p0 | uint16 | 0U  | 6000U |
|                      | \*ReLeWhlBusHiSpdInvldFaildThd_MilliSec_T_u16p0   | uint16 | 0U  | 6000U |
|                      | \*ReRiWhlBusHiSpdInvldFaildThd_MilliSec_T_u16p0   | uint16 | 0U  | 6000U |
| **Return Value**     | NA                                                | NA     | NA  | NA    |

## Design Rationale

None

## Processing

Please refer to the below path in the FDD model.

MM065A_FordMsg217BusHiSpd/FordMsg217BusHiSpd/FordMsg217BusHiSpdPer1/CalSeln

##  Local Function \#3

|                      |                                     |         |       |      |
|-----------|-------------------------------------|---------|---------|---------|
| **Function Name**    | VldFalse                            | Type    | Min   | Max  |
| **Arguments Passed** | \*FordVehFrntLeWhlSpdVld_Cnt_T_logl | boolean | FALSE | TRUE |
|                      | \*FordVehFrntRiWhlSpdVld_Cnt_T_logl | boolean | FALSE | TRUE |
|                      | \*FordVehReLeWhlSpdVld_Cnt_T_logl   | boolean | FALSE | TRUE |
|                      | \*FordVehReRiWhlSpdVld_Cnt_T_logl   | boolean | FALSE | TRUE |
| **Return Value**     | NA                                  | NA      | NA    | NA   |

## Design Rationale

None

## Processing

Please refer to the below path in the FDD model.

MM065A_FordMsg217BusHiSpd/FordMsg217BusHiSpd/FordMsg217BusHiSpdPer1/FordMsg217MsgMiss/VldFalse

###  Local Function \#4

|                      |                                        |         |       |         |
|-----------|-------------------------------------|---------|---------|---------|
| **Function Name**    | SigProc                                | Type    | Min   | Max     |
| **Arguments Passed** | Ford_WhlFl_W_Meas_Cnt_T_u16            | uint16  | 0U    | 32767U  |
|                      | Ford_WhlFr_W_Meas_Cnt_T_u16            | uint16  | 0U    | 32767U  |
|                      | Ford_WhlRl_W_Meas_Cnt_T_u16            | uint16  | 0U    | 32767U  |
|                      | Ford_WhlRr_W_Meas_Cnt_T_u16            | uint16  | 0U    | 32767U  |
|                      | \*FordVehFrntLeWhlSpdRaw_Cnt_T_u16     | uint16  | 0U    | 32767U  |
|                      | \*FordVehFrntLeWhlSpd_RadPerSec_T_f32  | float32 | 0.0F  | 327.67F |
|                      | \*FordVehFrntRiWhlSpdRaw_Cnt_T_u16     | uint16  | 0U    | 32767U  |
|                      | \*FordVehFrntRiWhlSpd_RadPerSec_T_f32  | float32 | 0.0F  | 327.67F |
|                      | \*FordVehReLeWhlSpdRaw_Cnt_T_u16       | uint16  | 0U    | 32767U  |
|                      | \*FordVehReLeWhlSpd_RadPerSec_T_f32    | float32 | 0.0F  | 327.67F |
|                      | \*FordVehReRiWhlSpdRaw_Cnt_T_u16       | uint16  | 0U    | 32767U  |
|                      | \*FordVehReRiWhlSpd_RadPerSec_T_f32    | float32 | 0.0F  | 327.67F |
|                      | \*FordVehFrntLeWhlSpdVld_Cnt_T_logl    | boolean | FALSE | TRUE    |
|                      | \*FordVehFrntRiWhlSpdVld_Cnt_T_logl    | boolean | FALSE | TRUE    |
|                      | \*FordVehReLeWhlSpdVld_Cnt_T_logl      | boolean | FALSE | TRUE    |
|                      | \*FordVehReRiWhlSpdVld_Cnt_T_logl      | boolean | FALSE | TRUE    |
|                      | \*FordVehFrntRiWhlSpdVldInp_Cnt_T_logl | boolean | FALSE | TRUE    |
|                      | \*FordVehFrntLeWhlSpdVldInp_Cnt_T_logl | boolean | FALSE | TRUE    |
|                      | \*FordVehReRiWhlSpdVldInp_Cnt_T_logl   | boolean | FALSE | TRUE    |
|                      | \*FordVehReLeWhlSpdVldInp_Cnt_T_logl   | boolean | FALSE | TRUE    |
| **Return Value**     | NA                                     | NA      | NA    | NA      |

## Design Rationale

None

## Processing

Please refer to the below path in the FDD model.

MM065A_FordMsg217BusHiSpd/FordMsg217BusHiSpd/FordMsg217BusHiSpdPer1/FordMsg217MsgPrsnt/SignalProcessing

###  Local Function \#5

|                      |                                     |         |       |      |
|-----------|-------------------------------------|---------|---------|---------|
| **Function Name**    | VldChk                              | Type    | Min   | Max  |
| **Arguments Passed** | FordVehFrntLeWhlSpd_Cnt_T_logl      | boolean | FALSE | TRUE |
|                      | FordVehFrntRiWhlSpd_Cnt_T_logl      | boolean | FALSE | TRUE |
|                      | FordVehReLeWhlSpd_Cnt_T_logl        | boolean | FALSE | TRUE |
|                      | FordVehReRiWhlSpd_Cnt_T_logl        | boolean | FALSE | TRUE |
|                      | \*FordVehFrntLeWhlSpdVld_Cnt_T_logl | boolean | FALSE | TRUE |
|                      | \*FordVehFrntRiWhlSpdVld_Cnt_T_logl | boolean | FALSE | TRUE |
|                      | \*FordVehReLeWhlSpdVld_Cnt_T_logl   | boolean | FALSE | TRUE |
|                      | \*FordVehReRiWhlSpdVld_Cnt_T_logl   | boolean | FALSE | TRUE |
| **Return Value**     | NA                                  | NA      | NA    | NA   |

## Design Rationale

None

## Processing

Please refer to the below path in the FDD model.

MM065A_FordMsg217BusHiSpd/FordMsg217BusHiSpd/FordMsg217BusHiSpdPer1/FordMsg217MsgPrsnt/SignalProcessing/VldChk

###  Local Function \#6

|                      |                                                 |         |       |       |
|-----------|-------------------------------------|---------|---------|---------|
| **Function Name**    | FrntWhlSpdDiagEnaChk                            | Type    | Min   | Max   |
| **Arguments Passed** | FrntWhlSpdDiagEna_Cnt_T_logl                    | boolean | FALSE | TRUE  |
|                      | FrntLeWhlBusHiSpdInvldFaildThd_MilliSec_T_u16p0 | uint16  | 0U    | 6000U |
|                      | FrntRiWhlBusHiSpdInvldFaildThd_MilliSec_T_u16p0 | uint16  | 0U    | 6000U |
|                      | FordVehFrntLeWhlSpdVldInp_Cnt_T_logl            | boolean | FALSE | TRUE  |
|                      | FordVehFrntRiWhlSpdVldInp_Cnt_T_logl            | boolean | FALSE | TRUE  |
| **Return Value**     | NA                                              | NA      | NA    | NA    |

## Design Rationale

None

## Processing

Please refer to the below path in the FDD model.

MM065A_FordMsg217BusHiSpd/FordMsg217BusHiSpd/FordMsg217BusHiSpdPer1/FordMsg217MsgPrsnt/FordVehFrntWhlSpdInvldSts

MM065A_FordMsg217BusHiSpd/FordMsg217BusHiSpd/FordMsg217BusHiSpdPer1/FordMsg217MsgPrsnt/FordVehFrntWhlSpdInvldNtcReset

###  Local Function \#7

|                      |                                               |         |       |       |
|-----------|-------------------------------------|---------|---------|---------|
| **Function Name**    | ReWhlSpdDiagEnaChk                            | Type    | Min   | Max   |
| **Arguments Passed** | ReWhlSpdDiagEna_Cnt_T_logl                    | boolean | FALSE | TRUE  |
|                      | ReLeWhlBusHiSpdInvldFaildThd_MilliSec_T_u16p0 | uint16  | 0U    | 6000U |
|                      | ReRiWhlBusHiSpdInvldFaildThd_MilliSec_T_u16p0 | uint16  | 0U    | 6000U |
|                      | FordVehReLeWhlSpdVldInp_Cnt_T_logl            | boolean | FALSE | TRUE  |
|                      | FordVehReRiWhlSpdVldInp_Cnt_T_logl            | boolean | FALSE | TRUE  |
| **Return Value**     | NA                                            | NA      | NA    | NA    |

## Design Rationale

None

## Processing

Please refer to the below path in the FDD model.

MM065A_FordMsg217BusHiSpd/FordMsg217BusHiSpd/FordMsg217BusHiSpdPer1/FordMsg217MsgPrsnt/FordVehReWhlSpdInvldSts

MM065A_FordMsg217BusHiSpd/FordMsg217BusHiSpd/FordMsg217BusHiSpdPer1/FordMsg217MsgPrsnt/FordVehReWhlSpdInvldNtcReset

###  Local Function \#8

|                      |                           |         |       |      |
|----------------------|---------------------------|---------|-------|------|
| **Function Name**    | MissMsgDiagEnaChk         | Type    | Min   | Max  |
| **Arguments Passed** | MissMsgDiagEna_Cnt_T_logl | boolean | FALSE | TRUE |
| **Return Value**     | NA                        | NA      | NA    | NA   |

## Design Rationale

None

## Processing

Please refer to the below path in the FDD model.

MM065A_FordMsg217BusHiSpd/FordMsg217BusHiSpd/FordMsg217BusHiSpdPer1/FordMsg217MsgPrsnt/FordMsg217MissMsgPass

MM065A_FordMsg217BusHiSpd/FordMsg217BusHiSpd/FordMsg217BusHiSpdPer1/FordMsg217MsgPrsnt/Reset

## GLOBAL Function/Macro Definitions

None

# Known Limitations with Design

1.  In the following path,

> MM065A_FordMsg217BusHiSpd/FordMsg217BusHiSpd/FordMsg217BusHiSpdPer1/FordMsg217MsgPrsnt
>
> Ford Vehicle Front Left Wheel Speed Valid (FordVehFrntLeWhlSpdVld) and
> Ford Vehicle Front Right Wheel Speed (FordVehFrntRiWhlSpdVld) signals
> are cross coupled.

1.  In the path,

MM065A_FordMsg217BusHiSpd/FordMsg217BusHiSpd/FordMsg217BusHiSpdPer1/FordMsg217MsgPrsnt/FordVehReWhlSpdInvldSts/ReRiWhlSpdInvldFail

There is a mismatch between the logic inside ReRiWhlSpdInvldFail
subsystem and its input port name.

1.  In the following path,

MM065A_FordMsg217BusHiSpd/FordMsg217BusHiSpd/FordMsg217BusHiSpdPer1/FordMsg217MsgMiss/VldFalse/ReLeWhlSpdVld
Previous

MM065A_FordMsg217BusHiSpd/FordMsg217BusHiSpd/FordMsg217BusHiSpdPer1/FordMsg217MsgMiss/VldFalse/ReRiWhlSpdVld
Previous

The port name used within the ReLeWhlSpdVld Previous and ReRiWhlSpdVld
Previous subsystems do not match with the merge block output names.

1.  In the following path,

MM065A_FordMsg217BusHiSpd/FordMsg217BusHiSpd/FordMsg217BusHiSpdPer1/CalSeln/FixdTi

uint32 constant value(BUSHISPDFIXDTITHD_MILLISEC_U32) is assigned to
uint16 signals.

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
| 5           | FDD: MM065A_FordMsg217BusHiSpd_Design                                                                                                                                 | See Synergy sub project version |

{% endraw %}