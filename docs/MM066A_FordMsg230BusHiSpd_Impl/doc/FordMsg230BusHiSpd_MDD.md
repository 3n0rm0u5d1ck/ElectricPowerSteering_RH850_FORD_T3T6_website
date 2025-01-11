---
layout: default
title: FordMsg230BusHiSpd_MDD
nav_order: 2
parent: Component Implementation
---
{% raw %}
**Module Design Document**

**For**

**FordMsg230BusHiSpd**

**03-Apr-2018**

**Prepared For:**

**Software Engineering**

**Nexteer Automotive,**

**Saginaw, MI, USA**

**Prepared By:**

**Tata Elxsi,**

**Trivandrum, INDIA  
<u>Change History</u>**

|                 |        |         |             |
|-----------------|--------|---------|-------------|
| Description     | Author | Version | Date        |
| Initial Version | TATA   | 1.0     | 03-Apr-2018 |

**  
**

**<u>Table of Contents</u>**

[1 Introduction [5](#introduction)](#introduction)

[MDD for FordMsg230BusHiSpd
[5](#mdd-for-fordmsg230bushispd)](#mdd-for-fordmsg230bushispd)

[2 FordMsg230BusHiSpd & High-Level Description
[6](#fordmsg230bushispd-high-level-description)](#fordmsg230bushispd-high-level-description)

[3 Design details of software module
[7](#design-details-of-software-module)](#design-details-of-software-module)

[3.1 Graphical representation of FordMsg230BusHiSpd
[7](#graphical-representation-of-fordmsg230bushispd)](#graphical-representation-of-fordmsg230bushispd)

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

[5.1.1 Init: FordMsg230BusHiSpdInit1
[9](#init-fordmsg230bushispdinit1)](#init-fordmsg230bushispdinit1)

[5.1.2 Per: FordMsg230BusHiSpdPer1
[9](#per-fordmsg230bushispdper1)](#per-fordmsg230bushispdper1)

[5.2 Server Runnables [9](#server-runnables)](#server-runnables)

[5.2.1 ComIPduCallout_BrakeSysFeatures_HS2
[9](#comipducallout-_transgeardata_fd1)](#comipducallout-_transgeardata_fd1)

[5.2.2 ComTimeoutNotification_Veh_V_ActlBrk
[9](#comtimeoutnotification-_gearlvrpos_d_actl)](#comtimeoutnotification-_gearlvrpos_d_actl)

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
[12](#design-rationale-8)](#design-rationale-8)

[5.4.5.2 Processing [12](#processing-4)](#processing-4)

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

##  MDD for FordMsg230BusHiSpd [mdd-for-fordmsg230bushispd]

# FordMsg230BusHiSpd & High-Level Description

Please refer FDD.

# Design details of software module

## Graphical representation of FordMsg230BusHiSpd

<img
src="ElectricPowerSteering_RH850_FORD_T3T6_website/docs/MM066A_FordMsg230BusHiSpd_Impl/doc/mediax/media/image1.png"
style="width:5.625in;height:3.80208in" />

## Data Flow Diagram

### Component level DFD

Please refer FDD.

### Function level DFD

Please refer FDD.

# Constant Data Dictionary

## Program (fixed) Constants

### Embedded Constants

#### Local Constants

| Constant Name                        | Resolution | Units | Value |
|--------------------------------------|------------|-------|-------|
| Please refer Data Dictionary .m file | NA         | NA    | NA    |

# Software Component Implementation

## Sub-Module Functions

### 5.1.1 Init: FordMsg230BusHiSpdInit1 [init-fordmsg230bushispdinit1]

#### Design Rationale

None

#### Module Outputs

None

### 5.1.2 Per: FordMsg230BusHiSpdPer1 [per-fordmsg230bushispdper1]

#### 5.1.2.1 Design Rationale [design-rationale-1]

None

#### 5.1.2.2 Store Module Inputs to Local copies [store-module-inputs-to-local-copies]

None

#### 5.1.2.3 Processing of function) [processing-of-function]

None

#### 5.1.2.4 Store Local copy of outputs into Module Outputs [store-local-copy-of-outputs-into-module-outputs]

None

## Server Runnables 

### 5.2.1 ComIPduCallout \_TransGearData_FD1 [comipducallout-_transgeardata_fd1]

#### 5.2.1.1 Design Rationale [design-rationale-2]

None

#### 5.2.1.2 (Processing of function) [processing-of-function-1]

None

### 5.2.2 ComTimeoutNotification \_GearLvrPos_D_Actl [comtimeoutnotification-_gearlvrpos_d_actl]

#### 5.2.2.1 Design Rationale [design-rationale-3]

None

#### 5.2.2.2 (Processing of function) [processing-of-function-2]

None

## Interrupt Functions

None

## Module Internal (Local) Functions

## Local Function \#1

| **Function Name** | DiagEna                           | Type    | Min | Max  |
|-------------------|-----------------------------------|---------|-----|------|
| Arguments Passed  | FordTrlrBackupAssiEnad_Cnt_T_logl | boolean | 0U  | 1U   |
|                   | FordCanDtcInhb_Cnt_T_logl         | boolean | 0U  | 1U   |
|                   | ClrDiagcFlgProxy_Cnt_T_u08        | uint8   | 0U  | 255U |
|                   | \*MissMsgDiagEna_Cnt_T_logl       | boolean | 0U  | 1U   |
|                   | \*ClrDiagcFlgProxyEna_Cnt_log     | boolean | 0U  | 1U   |
| Return Value      |                                   |         |     |      |

## Design Rationale

## Processing

Please refer to the below path in the FDD model.

MM066A_FordMsg230BusHiSpd/FordMsg230BusHiSpd/FordMsg230BusHiSpdPer1/DiagEnab

## Local Function \#2

| **Function Name** | MissMsg                               | Type                   | Min | Max    |
|----------|----------------------------|------------------|--------|---------|
| Arguments Passed  | BusHiSpdMissThd_Cnt_T_u16             | unit16                 | 0U  | 65535U |
|                   | MissMsgDiagEna_Cnt_T_logl             | boolean                | 0U  | 1U     |
|                   | ClrDiagcFlgProxyEna_Cnt_logl          | boolean                | 0U  | 1U     |
|                   | \*FordVehGearLvrPosnVldInt_Cnt_T_logl | boolean                | 0U  | 1U     |
|                   | \*FordVehGearLvrPosn_Cnt_T_enum       | Ford_GearLvrPos_D_Actl | 0U  | 15U    |
| Return Value      | None                                  |                        |     |        |

## Design Rationale

## Processing

Please refer to the below path in the FDD model.

MM066A_FordMsg230BusHiSpd/FordMsg230BusHiSpd/FordMsg230BusHiSpdPer1/MsgMiss

## Local Function \#3

| **Function Name** | MsgPrsnt                            | Type    | Min | Max    |
|----------|---------------------------|----------------------|-------|--------|
| Arguments Passed  | MissMsgDiagEna_Cnt_T_logl           | boolean | 0U  | 1U     |
|                   | BusHiSpdInvldThd_Cnt_T_u16          | uint16  | 0U  | 65535U |
|                   | FordVehGearLvrPosnVldFlg_Cnt_T_logl | boolean | 0U  | 1U     |
|                   | ClrDiagcFlgProxyEna_Cnt_logl        | boolean | 0U  | 1U     |
| Return Value      | None                                |         |     |        |

## Design Rationale

## Processing

Please refer to the below path in the FDD model.

MM066A_FordMsg230BusHiSpd/FordMsg230BusHiSpd/FordMsg230BusHiSpdPer1/MsgPrsnt

## Local Function \#4

| **Function Name** | OutpProcg                             | Type                   | Min | Max |
|----------|--------------------------------|------------------|-------|-------|
| Arguments Passed  | Ford_GearLvrPos_D_Actl_Cnt_T_enum     | Ford_GearLvrPos_D_Actl | 0U  | 15U |
|                   | \*FordVehGearLvrPosn_Cnt_T_enum       | Ford_GearLvrPos_D_Actl | 0U  | 15U |
|                   | \*FordVehGearLvrPosnVldInt_Cnt_T_logl | boolean                | 0U  | 1U  |
|                   | \*FordVehGearLvrPosnVldFlg_Cnt_T_logl | boolean                | 0U  | 1U  |
| Return Value      | None                                  |                        |     |     |

## Design Rationale

## Processing

Please refer to the below path in the FDD model.

MM066A_FordMsg230BusHiSpd/FordMsg230BusHiSpd/FordMsg230BusHiSpdPer1/MsgPrsnt/OutpProcg

## Local Function \#5

| **Function Name** | ElpdTi                   | Type    | Min | Max |
|-------------------|--------------------------|---------|-----|-----|
| Arguments Passed  | \*VldElpdTi_Cnt_T_logl   | boolean | 0U  | 1U  |
|                   | \*InvldElpdTi_Cnt_T_logl | boolean | 0U  | 1U  |
| Return Value      | None                     |         |     |     |

## Design Rationale

## Processing

Please refer to the below path in the FDD model.

MM066A_FordMsg230BusHiSpd/FordMsg230BusHiSpd/FordMsg230BusHiSpdPer1/MsgPrsnt/OutpProcg

/VldElpdTi

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

| Ref. \# | Title                                                                        | Version                        |
|-------|----------------------------------------|-------------------------|
| 1       | AUTOSAR Specification of Memory Mapping (Link:AUTOSAR_SWS_MemoryMapping.pdf) | v1.3.0 R4.0 Rev 2              |
| 2       | MDD Guideline                                                                | EA4 01.00                      |
| 3       | Software Naming Conventions.doc                                              | EA4 01.02                      |
| 4       | Software Design and Coding Standards.doc                                     | EA4 2.01                       |
| 5       | FDD: MM077A_FordMsg415BusHiSpd_Design                                        | See Synergy subproject version |

{% endraw %}