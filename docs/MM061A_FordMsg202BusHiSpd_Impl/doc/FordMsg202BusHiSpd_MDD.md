---
layout: default
title: FordMsg202BusHiSpd_MDD
nav_order: 2
parent: Component Implementation
---
{% raw %}
**Module Design Document**

**For**

**FordMsg202BusHiSpd**

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
| 1           | Initial Version | TATA       | 1.0         | 20-Dec-2017 |

**<u>Table of Contents</u>**

[1 Introduction [5](#introduction)](#introduction)

[1.1 Purpose [5](#purpose)](#purpose)

[2 FordMsg202BusHiSpd & High-Level Description
[6](#fordmsg202bushispd-high-level-description)](#fordmsg202bushispd-high-level-description)

[3 Design details of software module
[7](#design-details-of-software-module)](#design-details-of-software-module)

[3.1 Graphical representation of FordMsg202BusHiSpd
[7](#graphical-representation-of-fordmsg202bushispd)](#graphical-representation-of-fordmsg202bushispd)

[3.2 Data Flow Diagram [7](#data-flow-diagram)](#data-flow-diagram)

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

[5.1.1 Init: FordMsg202BusHiSpdInit1
[9](#init-fordmsg202bushispdinit1)](#init-fordmsg202bushispdinit1)

[5.1.1.1 Design Rationale [9](#design-rationale)](#design-rationale)

[5.1.1.2 Module Outputs [9](#module-outputs)](#module-outputs)

[5.1.2 Per: FordMsg202BusHiSpdPer
[9](#per-fordmsg202bushispdper)](#per-fordmsg202bushispdper)

[5.1.2.4 Store Local copy of outputs into Module Outputs
[9](#store-local-copy-of-outputs-into-module-outputs)](#store-local-copy-of-outputs-into-module-outputs)

[5.2 Server Runnables [9](#server-runnables)](#server-runnables)

[5.2.1 ComIPduCallout_EngVehicleSpThrottle2_HS2
[9](#comipducallout_engvehiclespthrottle2_hs2)](#comipducallout_engvehiclespthrottle2_hs2)

[5.2.2 ComTimeoutNotification_Ford_VehVActlEng_D_Qf
[9](#comtimeoutnotification_ford_vehvactleng_d_qf)](#comtimeoutnotification_ford_vehvactleng_d_qf)

[5.3 Interrupt Functions
[10](#interrupt-functions)](#interrupt-functions)

[5.4 Module Internal (Local) Functions
[10](#module-internal-local-functions)](#module-internal-local-functions)

[5.4.1 Local Function \#1 [10](#local-function-1)](#local-function-1)

[5.4.2 Local Function \#2 [10](#local-function-2)](#local-function-2)

[5.4.3 Local Function \#3 [11](#local-function-3)](#local-function-3)

[5.4.4 Local Function \#4 [11](#local-function-4)](#local-function-4)

[5.4.5 Local Function \#5 [13](#local-function-5)](#local-function-5)

[5.4.6 Local Function \#6 [13](#local-function-6)](#local-function-6)

[5.5 GLOBAL Function/Macro Definitions
[14](#global-functionmacro-definitions)](#global-functionmacro-definitions)

[6 Known Limitations with Design
[15](#known-limitations-with-design)](#known-limitations-with-design)

[7 UNIT TEST CONSIDERATION
[16](#unit-test-consideration)](#unit-test-consideration)

[Appendix A Abbreviations and Acronyms
[17](#abbreviations-and-acronyms)](#abbreviations-and-acronyms)

[Appendix B Glossary [18](#glossary)](#glossary)

[Appendix C References [19](#references)](#references)

# Introduction

## Purpose

MDD for FordMsg202BusHiSpd

# FordMsg202BusHiSpd & High-Level Description

Please refer FDD.

# Design details of software module

## Graphical representation of FordMsg202BusHiSpd

<img
src="ElectricPowerSteering_RH850_FORD_T3T6_website/docs/MM061A_FordMsg202BusHiSpd_Impl/doc/mediax/media/image1.png"
style="width:3.58333in;height:5.70833in" />

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

###  Init: FordMsg202BusHiSpdInit1

### 5.1.1.1 Design Rationale [design-rationale]

None

### 5.1.1.2 Module Outputs [module-outputs]

None

### 5.1.2 Per: FordMsg202BusHiSpdPer [per-fordmsg202bushispdper]

#### 5.1.2.1 Design Rationale [design-rationale-1]

None

#### 5.1.2.2 Store Module Inputs to Local copies [store-module-inputs-to-local-copies]

None

#### 5.1.2.3 Processing of function [processing-of-function]

None

### 5.1.2.4 Store Local copy of outputs into Module Outputs [store-local-copy-of-outputs-into-module-outputs]

None

## Server Runnables 

### 5.2.1 ComIPduCallout_EngVehicleSpThrottle2_HS2 [comipducallout_engvehiclespthrottle2_hs2]

#### 5.2.1.1 Design Rationale [design-rationale-2]

None

#### 5.2.1.2 Processing of function [processing-of-function-1]

None

### 5.2.2 ComTimeoutNotification_Ford_VehVActlEng_D_Qf [comtimeoutnotification_ford_vehvactleng_d_qf]

#### 5.2.2.1 Design Rationale [design-rationale-3]

None

#### 5.2.2.2 Processing of function [processing-of-function-2]

None

## Interrupt Functions

None

## Module Internal (Local) Functions

##  Local Function \#1

|                      |                                      |         |       |      |
|------------|------------------------------|---------|-----------|-----------|
| **Function Name**    | DiagEna                              | Type    | Min   | Max  |
| **Arguments Passed** | ClrDiagcFlgProxy_Cnt_T_u08           | uint8   | 0U    | 1U   |
|                      | FordAbsPrsnt_Cnt_T_u08               | uint8   | 0U    | 1U   |
|                      | FordTqSteerCmpEnad_Cnt_T_u08         | uint8   | 0U    | 1U   |
|                      | FordMissMsgDiagcInhb_Cnt_T_u08       | uint8   | 0U    | 1U   |
|                      | FordMfgDiagcInhb_Cnt_T_u08           | uint8   | 0U    | 1U   |
|                      | FordCanDtcInhb_Cnt_T_u08             | uint8   | 0U    | 1U   |
|                      | FordBrkOscnRednEnad_Cnt_T_u08        | uint8   | 0U    | 1U   |
|                      | FordTrlrBackupAssiEnad_Cnt_T_u08     | uint8   | 0U    | 1U   |
|                      | FordInvldMsgDiagcInhb_Cnt_T_u08      | uint8   | 0U    | 1U   |
|                      | \* MissMsgNtcFail_Cnt_T_logl         | boolean | False | True |
|                      | \* MissMsgNtcPass_Cnt_T_logl         | boolean | False | True |
|                      | \* InvldMsgQlyFacDiagEna_Cnt_T_logl  | boolean | False | True |
|                      | \* InvldMsgGearRevDiagEna_Cnt_T_logl | boolean | False | True |
| **Return Value**     | NA                                   | NA      | NA    | NA   |

#### Design Rationale

None

#### Processing

Please refer to the below path in the FDD model.

MM061A_FordMsg202BusHiSpd/FordMsg202BusHiSpd/FordMsg202BusHiSpdPer1/DiagEna

##  Local Function \#2

|                      |                                               |        |     |       |
|-----------|-----------------------------------|--------|----------|---------|
| **Function Name**    | CalSeln                                       | Type   | Min | Max   |
| **Arguments Passed** | FordEpsLifeCycMod_Cnt_T_u08                   | uint8  | 0U  | 1U    |
|                      | FordAbsPrsnt_Cnt_T_u08                        | uint8  | 0U  | 1U    |
|                      | \* BusHiSpdMissMsgFaildThd_Cnt_T_u16          | uint16 | 0U  | 6000U |
|                      | \* BusHiSpdGearRvStsInvldFaildThd_Cnt_T_u16   | uint16 | 0U  | 6000U |
|                      | \*BusHiSpdQlyFacEngModInvldFaildThd_Cnt_T_u16 | uint16 | 0U  | 6000U |
| **Return Value**     | NA                                            | NA     | NA  | NA    |

#### Design Rationale

None

#### Processing

Please refer to the below path in the FDD model.

MM061A_FordMsg202BusHiSpd/FordMsg202BusHiSpd/FordMsg202BusHiSpdPer1/CalSeln

##  Local Function \#3

|                      |                                           |         |       |      |
|-----------|-------------------------------------|---------|---------|---------|
| **Function Name**    | VldFalse                                  | Type    | Min   | Max  |
| **Arguments Passed** | \*FordVehGearRvsStsVld_Cnt_T_logl         | boolean | False | True |
|                      | \* FordVehSpdEngModlVld_Cnt_T_logl        | boolean | False | True |
|                      | \* FordVehSpdEngModLoQlyVld_Cnt_T_logl    | boolean | False | True |
|                      | \* FordVehTrlrBackupAssiAvlVld_Cnt_T_logl | boolean | False | True |
| **Return Value**     | NA                                        | NA      | NA    | NA   |

#### Design Rationale

None

#### Processing

Please refer to the below path in the FDD model.

MM061A_FordMsg202BusHiSpd/FordMsg202BusHiSpd/FordMsg202BusHiSpdPer1/FordMsg202MsgMiss/VldFalse

### 5.4.4 Local Function \#4 [local-function-4]

|                      |                                           |                               |       |         |
|---------|--------------------------|--------------------------|------|-------|
| **Function Name**    | SigProcg                                  | Type                          | Min   | Max     |
| **Arguments Passed** | Ford_GearRvrse_D_Actl1_Cnt_T_enum         | enum.Ford_GearRvrse_D_Actl    | 0U    | 7U      |
|                      | Ford_Veh_V_ActlEng_Cnt_T_u16              | uint16                        | 0U    | 65535U  |
|                      | Ford_VehVActlEng_D_Qf1_Cnt_T_enum         | enum.Ford_VehVActlEng_D_Qf    | 0U    | 3U      |
|                      | Ford_VehVActlEng_No_Cnt_Cnt_T_u08         | uint8                         | 0U    | 15U     |
|                      | Ford_VehVActlEng_No_Cs_Cnt_T_u08          | uint8                         | 0U    | 255U    |
|                      | Ford_VehVTrlrAid_B_Avail1_Cnt_T_enum      | enum.Ford_VehVTrlrAid_B_Avail | False | True    |
|                      | \* FordVehGearRvsStsRaw_Cnt_T_u08         | uint8                         | 0U    | 7U      |
|                      | \* FordVehGearRvsSts_Cnt_T_enum           | enum.Ford_GearRvrse_D_Actl    | 0U    | 7U      |
|                      | \* FordVehGearRvsStsVld_Cnt_T_logl        | boolean                       | False | True    |
|                      | \* FordVehSpdEngModlRaw_Cnt_T_u16         | uint16                        | 0U    | 65535U  |
|                      | \* FordVehSpdEngModl_Kph_T_f32            | Float32                       | 0F    | 655.35F |
|                      | \* FordVehSpdQlyFacEngModl_Cnt_T_enum     | enum.Ford_VehVActlEng_D_Qf    | 0U    | 3U      |
|                      | \* FordVehSpdCntrEngModl_Cnt_T_u08        | uint8                         | 0U    | 15U     |
|                      | \* FordVehSpdChksEngModl_Cnt_T_u08        | uint8                         | 0U    | 255U    |
|                      | \* FordVehSpdEngModlVld_Cnt_T_logl        | boolean                       | False | True    |
|                      | \* FordVehSpdEngModLoQlyVld_Cnt_T_logl    | boolean                       | False | True    |
|                      | \* FordVehTrlrAidAvlRaw_Cnt_T_u08         | uint8                         | 0U    | 1U      |
|                      | \* FordVehTrlrAidAvl_Cnt_T_enum           | enum.Ford_VehVTrlrAid_B_Avail | False | True    |
|                      | \* FordVehTrlrBackupAssiAvlVld_Cnt_T_logl | boolean                       | False | True    |
|                      | \*FordVehGearRvsStsVldFlg_Cnt_T_logl      | boolean                       | False | True    |
|                      | \* FordVehSpdEngModlVldFlg_Cnt_T_logl     | boolean                       | False | True    |
| **Return Value**     | NA                                        | NA                            | NA    | NA      |

#### 5.4.4.1 Design Rationale [design-rationale-7]

None

#### 5.4.4.1 Processing [processing-3]

Please refer to the below path in the FDD model.

MM061A_FordMsg202BusHiSpd/FordMsg202BusHiSpd/FordMsg202BusHiSpdPer1/FordMsg202MsgPrsnt/SignalProcessing

### 5.4.5 Local Function \#5 [local-function-5]

|                      |                                                |         |       |      |
|-----------|-------------------------------------|---------|---------|---------|
| **Function Name**    | VldElpdTi                                      | Type    | Min   | Max  |
| **Arguments Passed** | \*GearRvsStsVldElpdTi_Cnt_T_logl               | boolean | False | True |
|                      | \*GearRvsStsInvldElpdTi_Cnt_T_logl             | boolean | False | True |
|                      | \*SpdEngModLoQlyVldElpdTi_Cnt_T_logl           | boolean | False | True |
|                      | \*SpdEngModLoQlyInvldElpdTi_Cnt_T_logl         | boolean | False | True |
|                      | \*FordVehTrlrBackupAssiAvlVldElpdTi_Cnt_T_logl | boolean | False | True |
|                      | \*EngModlInvldElpdTi_Cnt_T_logl                | boolean | False | True |
| **Return Value**     | NA                                             | NA      | NA    | NA   |

#### 5.4.5.1 Design Rationale [design-rationale-8]

None

#### 5.4.5.2 Processing [processing-4]

Please refer to the below path in the FDD model.

MM061A_FordMsg202BusHiSpd/FordMsg202BusHiSpd/FordMsg202BusHiSpdPer1/FordMsg202MsgPrsnt/SignalProcessing/VldElpdTi

### 5.4.6 Local Function \#6 [local-function-6]

|                      |                                              |         |       |      |
|-----------|-------------------------------------|---------|---------|---------|
| **Function Name**    | VldChk                                       | Type    | Min   | Max  |
| **Arguments Passed** | FordVehGearRvsStsVldFlg_Cnt_T_logl           | boolean | False | True |
|                      | FordVehSpdEngModLoQlyVldFlg_Cnt_T_logl       | boolean | False | True |
|                      | FordVehSpdEngModlVldFlg_Cnt_T_logl           | boolean | False | True |
|                      | FordVehTrlrBackupAssiAvlVldElpdTi_Cnt_T_logl | boolean | False | True |
|                      | GearRvsStsVldElpdTi_Cnt_T_logl               | boolean | False | True |
|                      | GearRvsStsInvldElpdTi_Cnt_T_logl             | boolean | False | True |
|                      | SpdEngModLoQlyVldElpdTi_Cnt_T_logl           | boolean | False | True |
|                      | SpdEngModLoQlyInvldElpdTi_Cnt_T_logl         | boolean | False | True |
|                      | EngModlInvldElpdTi_Cnt_T_logl                | boolean | False | True |
|                      | \* FordVehGearRvsStsVld_Cnt_T_logl           | boolean | False | True |
|                      | \* FordVehSpdEngModLoQlyVld_Cnt_T_logl       | boolean | False | True |
|                      | \* FordVehTrlrBackupAssiAvlVld_Cnt_T_logl    | boolean | False | True |
|                      | \* FordVehSpdEngModlVld_Cnt_T_logl           | boolean | False | True |
| **Return Value**     | NA                                           | NA      | NA    | NA   |

#### 5.4.6.1 Design Rationale [design-rationale-9]

None

#### 5.4.6.2 Processing [processing-5]

Please refer to the below path in the FDD model.

MM061A_FordMsg202BusHiSpd/FordMsg202BusHiSpd/FordMsg202BusHiSpdPer1/FordMsg202MsgPrsnt/SignalProcessing/VldChk

## GLOBAL Function/Macro Definitions

None

# Known Limitations with Design

1.  In the following path,

MM061A_FordMsg202BusHiSpd/FordMsg202BusHiSpd/FordMsg202BusHiSpdPer1/FordMsg202MsgPrsnt/SignalProcessing/VldChk/SpdEngModlInvld/FordVehSpdEngModlVldFalse

MM061A_FordMsg202BusHiSpd/FordMsg202BusHiSpd/FordMsg202BusHiSpdPer1/FordMsg202MsgPrsnt/SignalProcessing/VldChk/SpdEngModlInvld/SpdEngModlVldPrevious

The port name used within the FordVehSpdEngModlVldFalse and
SpdEngModlVldPrevious subsystems do not match with the merge block
output names.

1.  In below path

MM061A_FordMsg202BusHiSpd/FordMsg202BusHiSpd/FordMsg202BusHiSpdPer1/FordMsg202MsgPrsnt/FordVehGearRvsStsinvld/FordVehGearRvsStsinvldFaild

Type casting required for CNVMILLISECTOCNT_CNTPERMILLISEC_U16 and
BusHiSpdGearRvStsInvldFaildThd as per logic.

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
| 5           | FDD: MM061A_FordMsg202BusHiSpd_Design_2.1.0                                                                                                                           | See Synergy sub project version |

{% endraw %}