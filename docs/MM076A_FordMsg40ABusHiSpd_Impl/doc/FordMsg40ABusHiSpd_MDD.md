---
layout: default
title: FordMsg40ABusHiSpd_MDD
nav_order: 2
parent: Component Implementation
---
{% raw %}
**Module Design Document**

**For**

**FordMsg40ABusHiSpd**

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
| 1           | Initial Version | TATA       | 1.0         | 11-Dec-2017 |

**<u>Table of Contents</u>**

[1 Introduction [4](#introduction)](#introduction)

[1.1 Purpose [4](#purpose)](#purpose)

[2 FordMsg40ABusHiSpd & High-Level Description
[5](#fordmsg40abushispd-high-level-description)](#fordmsg40abushispd-high-level-description)

[3 Design details of software module
[6](#design-details-of-software-module)](#design-details-of-software-module)

[3.1 Graphical representation of FordMsg40ABusHiSpd
[6](#graphical-representation-of-fordmsg40abushispd)](#graphical-representation-of-fordmsg40abushispd)

[3.2 Data Flow Diagram [6](#data-flow-diagram)](#data-flow-diagram)

[Component level DFD [6](#component-level-dfd)](#component-level-dfd)

[Function level DFD [6](#function-level-dfd)](#function-level-dfd)

[4 Constant Data Dictionary
[7](#constant-data-dictionary)](#constant-data-dictionary)

[4.1 Program (fixed) Constants
[7](#program-fixed-constants)](#program-fixed-constants)

[Embedded Constants [7](#embedded-constants)](#embedded-constants)

[5 Software Component Implementation
[8](#software-component-implementation)](#software-component-implementation)

[5.1 Sub-Module Functions
[8](#sub-module-functions)](#sub-module-functions)

[5.1.1 Init: FordMsg40ABusHiSpdInit1
[8](#init-fordmsg40abushispdinit1)](#init-fordmsg40abushispdinit1)

[5.1.2 Per: FordMsg40ABusHiSpdPer1
[8](#per-fordmsg40abushispdper1)](#per-fordmsg40abushispdper1)

[5.2 Server Runnables [8](#server-runnables)](#server-runnables)

[5.2.1 ComIPduCallout_GGCC_Config_Mgmt_ID_1_HS2
[8](#comipducallout_ggcc_config_mgmt_id_1_hs2)](#comipducallout_ggcc_config_mgmt_id_1_hs2)

[5.2.2 ComTimeoutNotification_VehicleGGCCData
[8](#comtimeoutnotification_vehicleggccdata)](#comtimeoutnotification_vehicleggccdata)

[5.3 Interrupt Functions
[9](#interrupt-functions)](#interrupt-functions)

[5.4 Module Internal (Local) Functions
[9](#module-internal-local-functions)](#module-internal-local-functions)

[5.4.1 Local Function \#1 [9](#local-function-1)](#local-function-1)

[5.4.2 Local Function \#2 [9](#local-function-2)](#local-function-2)

[5.4.3 Local Function \#3 [10](#local-function-3)](#local-function-3)

[5.4.4 Local Function \#4 [10](#local-function-4)](#local-function-4)

[5.5 GLOBAL Function/Macro Definitions
[11](#global-functionmacro-definitions)](#global-functionmacro-definitions)

[6 Known Limitations with Design
[12](#known-limitations-with-design)](#known-limitations-with-design)

[7 UNIT TEST CONSIDERATION
[13](#unit-test-consideration)](#unit-test-consideration)

[Appendix A Abbreviations and Acronyms
[14](#abbreviations-and-acronyms)](#abbreviations-and-acronyms)

[Appendix B Glossary [15](#glossary)](#glossary)

[Appendix C References [16](#references)](#references)

# Introduction

## Purpose

MDD for FordMsg40ABusHiSpd

# FordMsg40ABusHiSpd & High-Level Description

Please refer FDD.

# Design details of software module

## Graphical representation of FordMsg40ABusHiSpd

<img
src="ElectricPowerSteering_RH850_FORD_T3T6_website/docs/MM076A_FordMsg40ABusHiSpd_Impl/doc/mediax/media/image1.png"
style="width:3.19792in;height:4.125in" />

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
| IDX2_CNT_U08                         | Uint8      | Cnt   | 2U    |
| IDX3_CNT_U08                         | Uint8      | Cnt   | 3U    |
| IDX4_CNT_U08                         | Uint8      | Cnt   | 4U    |
| IDX5_CNT_U08                         | Uint8      | Cnt   | 5U    |
| IDX6_CNT_U08                         | Uint8      | Cnt   | 6U    |
| IDX7_CNT_U08                         | Uint8      | Cnt   | 7U    |
| IDX8_CNT_U08                         | Uint8      | Cnt   | 8U    |
| IDX9_CNT_U08                         | Uint8      | Cnt   | 9U    |
| IDX10_CNT_U08                        | Uint8      | Cnt   | 10U   |
| IDX11_CNT_U08                        | Uint8      | Cnt   | 11U   |
| IDX12_CNT_U08                        | Uint8      | Cnt   | 12U   |
| IDX13_CNT_U08                        | Uint8      | Cnt   | 13U   |
| IDX14_CNT_U08                        | Uint8      | Cnt   | 14U   |
| IDX15_CNT_U08                        | Uint8      | Cnt   | 15U   |
| IDX16_CNT_U08                        | Uint8      | Cnt   | 16U   |
| IDX17_CNT_U08                        | Uint8      | Cnt   | 17U   |

# Software Component Implementation

## Sub-Module Functions

### 5.1.1 Init: FordMsg40ABusHiSpdInit1

#### 5.1.1.1 Design Rationale [design-rationale]

> None

#### 5.1.1.2 Module Outputs [module-outputs]

> None

### 5.1.2 Per: FordMsg40ABusHiSpdPer1

#### 5.1.2.1 Design Rationale [design-rationale-1]

None

#### 5.1.2.2 Store Module Inputs to Local copies [store-module-inputs-to-local-copies]

None

#### 5.1.2.3 Processing of function [processing-of-function]

None

#### 5.1.2.4 Store Local copy of outputs into Module Outputs [store-local-copy-of-outputs-into-module-outputs]

None

## Server Runnables 

### 5.2.1 ComIPduCallout_GGCC_Config_Mgmt_ID_1_HS2

#### 5.2.1.1 Design Rationale [design-rationale-2]

None

#### 5.2.1.2 Processing of function [processing-of-function-1]

None

### 5.2.2 ComTimeoutNotification_VehicleGGCCData

#### 5.2.2.1 Design Rationale [design-rationale-3]

None

#### 5.2.2.2 Processing of function [processing-of-function-2]

None

## Interrupt Functions

None

## Module Internal (Local) Functions

##  Local Function \#1

|                      |                                |         |       |      |
|----------------------|--------------------------------|---------|-------|------|
| **Function Name**    | DiagEna                        | Type    | Min   | Max  |
| **Arguments Passed** | FordCanDtcInhb_Cnt_T_u08       | uint8   | 0U    | 1U   |
|                      | ClrDiagcFlgProxy_Cnt_T_u08     | uint8   | 0U    | 1U   |
|                      | FordMissMsgDiagcInhb_Cnt_T_u08 | uint8   | 0U    | 1U   |
|                      | FordMfgDiagcInhb_Cnt_T_u08     | uint8   | 0U    | 1U   |
| **Return Value**     | MissMsgDiagEna_Cnt_T_logl      | boolean | FALSE | TRUE |

#### Design Rationale

None

#### Processing

Please refer to the below path in the FDD model.

MM076A_FordMsg40ABusHiSpd/FordMsg40ABusHiSpd/FordMsg40ABusHiSpdPer1/DiagEna

##  Local Function \#2

|                      |                                     |         |       |               |
|-----------|----------------------------------|--------|---------|------------|
| **Function Name**    | MissMsgFaild                        | Type    | Min   | Max           |
| **Arguments Passed** | MissMsgDiagEna_Cnt_T_logl           | boolean | FALSE | TRUE          |
|                      | BusHiSpdMissTiThdval_MilliSec_T_u16 | uint16  | 0U    | 6000U         |
|                      | \* FordVehGlbRealTi_Sec_T_f32       | float32 | 0.1F  | 429496729\.5F |
|                      | \* FordVehIdnNr_Cnt_T_u08           | uint8   | 0U    | 255U          |
|                      | \* FordVehTireCircum_MilliMtr_T_f32 | float32 | 0.0F  | 65535.0F      |
| **Return Value**     | NA                                  | NA      | NA    | NA            |

#### Design Rationale

None

#### Processing

Please refer to the below path in the FDD model.

MM076A_FordMsg40ABusHiSpd/FordMsg40ABusHiSpd/FordMsg40ABusHiSpdPer1/MissMsgFaild

##  Local Function \#3

|                      |                                     |         |       |               |
|-----------|--------------------------------|---------|--------|--------------|
| **Function Name**    | MissMsgPassd                        | Type    | Min   | Max           |
| **Arguments Passed** | MissMsgDiagEna_Cnt_T_logl           | boolean | FALSE | TRUE          |
|                      | \* Ford_VehGGCCData_Cnt_T_u08       | uint8   | 0U    | 255U          |
|                      | \* FordVehGlbRealTi_Sec_T_f32       | float32 | 0.1F  | 429496729\.5F |
|                      | \* FordVehIdnNr_Cnt_T_u08           | uint8   | 0U    | 255U          |
|                      | \* FordVehTireCircum_MilliMtr_T_f32 | float32 | 0.0F  | 65535.0F      |
| **Return Value**     | NA                                  | NA      | NA    | NA            |

#### Design Rationale

None

#### Processing

Please refer to the below path in the FDD model.

MM076A_FordMsg40ABusHiSpd/FordMsg40ABusHiSpd/FordMsg40ABusHiSpdPer1/MissMsgPassd

###  Local Function \#4

|                      |                                  |         |      |               |
|-----------|--------------------------------|---------|--------|--------------|
| **Function Name**    | OutpProc                         | Type    | Min  | Max           |
| **Arguments Passed** | Ford_VehGGCCData_Cnt_T_u08       | uint8   | 0U   | 255U          |
|                      | VehGlbCfgByte1_Cnt_T_u08         | uint8   | 0U   | 255U          |
|                      | VehGlbCfgByte2_Cnt_T_u08         | uint8   | 0U   | 255U          |
|                      | FordVehGlbRealTi_Sec_T_f32       | float32 | 0.1F | 429496729\.5F |
|                      | FordVehIdnNr_Cnt_T_u08           | uint8   | 0U   | 255U          |
|                      | FordVehTireCircum_MilliMtr_T_f32 | float32 | 0.0F | 65535.0F      |
| **Return Value**     | NA                               | NA      | NA   | NA            |

#### Design Rationale

None

#### Processing

Please refer to the below path in the FDD model.

MM076A_FordMsg40ABusHiSpd/FordMsg40ABusHiSpd/FordMsg40ABusHiSpdPer1/MissMsgPassd/OutpProc

## GLOBAL Function/Macro Definitions

None

# Known Limitations with Design

In model FordVehGlbRealTiPrev(PIM) value is assigned to
FordVehGlbRealTi(Output). But both signal minimum value is not matching
in the datadictionary.

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
| 5           | FDD: MM076A\_ FordMsg40ABusHiSpd \_Design                                                                                                                             | See Synergy sub project version |

{% endraw %}