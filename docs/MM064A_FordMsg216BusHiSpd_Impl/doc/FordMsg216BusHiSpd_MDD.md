---
layout: default
title: FordMsg216BusHiSpd_MDD
nav_order: 2
parent: Component Implementation
---
{% raw %}
**Module Design Document**

**For**

**FordMsg216BusHiSpd**

**27-Apr-2018**

**Prepared For:**

**Software Engineering**

**Nexteer Automotive,**

**Saginaw, MI, USA**

**Prepared By:**

**TATA ELXSI,**

**INDIA**

**<u>Change History</u>**

|                 |            |             |             |
|-----------------|------------|-------------|-------------|
| **Description** | **Author** | **Version** | **Date**    |
| Initial version | TATA ELXSI | 1           | 27-Apr-2018 |

**  
**

<span id="_Toc512865019" class="anchor"></span><u>Table of Contents</u>

[Table of Contents [3](#_Toc512865019)](#_Toc512865019)

[1 Introduction [5](#introduction)](#introduction)

[1.1 Purpose [5](#purpose)](#purpose)

[1.2 Scope [5](#scope)](#scope)

[2 FordMsg216BusHiSpd & High-Level Description
[6](#fordmsg216bushispd-high-level-description)](#fordmsg216bushispd-high-level-description)

[3 Design details of software module
[7](#design-details-of-software-module)](#design-details-of-software-module)

[3.1 Graphical representation of FordMsg216BusHiSpd
[7](#graphical-representation-of-fordmsg216bushispd)](#graphical-representation-of-fordmsg216bushispd)

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

[5.1.1 Init: FordMsg216BusHiSpdInit1
[9](#init-fordmsg216bushispdinit1)](#init-fordmsg216bushispdinit1)

[5.1.2 Per: FordMsg216BusHiSpdPer1
[9](#per-fordmsg216bushispdper1)](#per-fordmsg216bushispdper1)

[5.2 Server Runnable [9](#server-runnable)](#server-runnable)

[5.3 Interrupt Functions
[9](#interrupt-functions)](#interrupt-functions)

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

[5.4.7 Local Function \#7 [13](#local-function-7)](#local-function-7)

[5.4.7.1 Design Rationale
[13](#design-rationale-10)](#design-rationale-10)

[5.4.7.2 Processing [13](#processing-6)](#processing-6)

[5.4.8 Local Function \#8 [14](#local-function-8)](#local-function-8)

[5.4.8.1 Design Rationale
[14](#design-rationale-11)](#design-rationale-11)

[5.4.8.2 Processing [14](#processing-7)](#processing-7)

[5.4.9 Local Function \#9 [14](#local-function-9)](#local-function-9)

[5.4.9.1 Design Rationale
[15](#design-rationale-12)](#design-rationale-12)

[5.4.9.2 Processing [15](#processing-8)](#processing-8)

[5.4.10 Local Function \#10
[15](#local-function-10)](#local-function-10)

[5.4.10.1 Design Rationale
[15](#design-rationale-13)](#design-rationale-13)

[5.4.10.2 Processing [15](#processing-9)](#processing-9)

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

Module Design Document for MM064A_FordMsg216BusHiSpd_Impl.

## Scope

The following definitions are used throughout this document:

-   **<u>Shall</u>**: indicates a mandatory requirement without
    exception in compliance.

-   **<u>Should</u>**: indicates a mandatory requirement; exceptions
    allowed only with documented justification.

-   **<u>May</u>**: indicates an optional action.

# FordMsg216BusHiSpd & High-Level Description

The purpose of the Ford Message 216 Bus High Speed function is to
provide the Electric Power Steering system with signal values for the
Trailer Back Up Assist, Torque Steer Compensation, and Brake Oscillation
Reduction functions from CAN. The Ford Message216 function will perform
the missing message diagnostic as well as provide a validity signal for
the received message.

# Design details of software module

## Graphical representation of FordMsg216BusHiSpd

<img
src="ElectricPowerSteering_RH850_FORD_T3T6_website/docs/MM064A_FordMsg216BusHiSpd_Impl/doc/mediax/media/image1.png"
style="width:5.61458in;height:5.45833in" />

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

| Constant Name   | Resolution | Units | Value |
|-----------------|------------|-------|-------|
| Please Refer DD | NA         | NA    | NA    |

# Software Component Implementation

## Sub-Module Functions

The sub-module functions are grouped based on similar functionality that
needs to be executed in a given “State” of the system (refer States and
Modes). For a given module, the MDD will identify the type and number of
sub-modules required. The sub-module types are described below.

### Init: FordMsg216BusHiSpdInit1

#### Design Rationale

Refer FDD

#### Module Outputs

Refer FDD

### Per: FordMsg216BusHiSpdPer1

#### Design Rationale

Refer FDD

#### Store Module Inputs to Local copies

Refer FDD

#### (Processing of function) ………

Refer FDD

#### Store Local copy of outputs into Module Outputs

Refer FDD

## Server Runnable

### ComIPduCallout_WheelData_FD1

## 5.2.1.1 Design Rationale [design-rationale-2]

None

## 5.2.1.2 Processing of function [processing-of-function-1]

None

### ComTimeoutNotification_WhlDirFl_D_Actl

## 5.2.2.1 Design Rationale [design-rationale-3]

None

## 5.2.2.2 Processing of function [processing-of-function-2]

None

## Interrupt Functions

None

## Module Internal (Local) Functions

## Local Function \#1

| **Function Name** | DiagEna                           | Type    | Min | Max  |
|-------------------|-----------------------------------|---------|-----|------|
| Arguments Passed  | FordTqSteerCmpEnad_Cnt_T_logl     | boolean | 0U  | 1U   |
|                   | FordBrkOscnRednEnad_Cnt_T_logl    | boolean | 0U  | 1U   |
|                   | FordTrlrBackUpAssiEnad_Cnt_T_logl | boolean | 0U  | 1U   |
|                   | ClrDiagcFlgProxy_Cnt_T_u08        | uint8   | 0U  | 255U |
|                   | FordCanDtcInhb_Cnt_T_logl         | boolean | 0U  | 1U   |
|                   | \*MissMsgDiagEna_Cnt_T_logl       | boolean | 0U  | 1U   |
|                   | \*ClrDiagcFlgProxyEna_Cnt_logl    | boolean | 0U  | 1U   |
| Return Value      |                                   |         |     |      |

## Design Rationale

## Processing

Please refer to the below path in the FDD model.

MM064A_FordMsg216BusHiSpd_SIL/FordMsg216BusHiSpd/FordMsg216BusHiSpdPer1/DiagEna

## Local Function \#2

| **Function Name** | MissMsg                                 | Type    | Min | Max  |
|------------|---------------------------------|---------|---------|----------|
| Arguments Passed  | FordEpsLifeCycMod_Cnt_T_u08             | uint8   | 0   | 255U |
|                   | MissMsgDiagEna_Cnt_T_logl               | boolean | 0U  | 1U   |
|                   | ClrDiagcFlgProxyEna_Cnt_logl            | boolean | 0U  | 1U   |
|                   | \*FordVehFrntLeWhlDirRaw_Cnt_T_enum     | Enum    | 0U  | 3U   |
|                   | \*FordVehFrntRiWhlDirRaw_Cnt_T_enum     | Enum    | 0U  | 3U   |
|                   | \*FordVehReLeWhlDirRaw_Cnt_T_enum       | Enum    | 0U  | 3U   |
|                   | \*FordVehReRiWhlDirRaw_Cnt_T_enum       | Enum    | 0   | 3U   |
|                   | \*FordVehFrntLeWhlRollgCntr_Cnt_T_u08   | uint8   | 0   | 255U |
|                   | \*FordVehFrntRiWhlRollgCntr_Cnt_T_u08   | uint8   | 0   | 255U |
|                   | \*FordVehReLeWhlRollgCntr_Cnt_T_u08     | uint8   | 0   | 255U |
|                   | \*FordVehReRiWhlRollgCntr_Cnt_T_u08     | uint8   | 0   | 255U |
|                   | \*FordVehFrntLeWhlCntrDirVld_Cnt_T_logl | boolean | 0U  | 1U   |
|                   | \*FordVehFrntRiWhlCntrDirVld_Cnt_T_logl | boolean | 0U  | 1U   |
|                   | \*FordVehReLeWhlCntrDirVld_Cnt_T_logl   | boolean | 0U  | 1U   |
|                   | \*FordVehReRiWhlCntrDirVld_Cnt_T_logl   | boolean | 0U  | 1U   |
| Return Value      |                                         |         |     |      |

## Design Rationale

## Processing

Please refer to the below path in the FDD model.

MM064A_FordMsg216BusHiSpd_SIL/FordMsg216BusHiSpd/FordMsg216BusHiSpdPer1/FordMsg064MsgMiss

## Local Function \#3

| **Function Name** | MissMsgNtcFail               | Type    | Min | Max   |
|-------------------|------------------------------|---------|-----|-------|
| Arguments Passed  | MissMsgDiagEna_Cnt_T_logl    | boolean | 0U  | 1U    |
|                   | ClrDiagcFlgProxyEna_Cnt_logl | boolean | 0U  | 1U    |
|                   | BusHiSpdMissTiThd_Cnt_T_u16  | unit16  | 0   | 65535 |
| Return Value      |                              |         |     |       |

## Design Rationale

## Processing

Please refer to the below path in the FDD model.

MM064A_FordMsg216BusHiSpd/FordMsg216BusHiSpd/FordMsg216BusHiSpdPer1/FordMsg064MsgMiss

## Local Function \#4

| **Function Name** | MissMsgOutpProcg                        | Type    | Min | Max |
|----------|-------------------------------------|--------|---------|----------|
| Arguments Passed  | \*FordVehFrntLeWhlCntrDirVld_Cnt_T_logl | boolean | 0U  | 1U  |
|                   | \*FordVehFrntRiWhlCntrDirVld_Cnt_T_logl | boolean | 0U  | 1U  |
|                   | \*FordVehReLeWhlCntrDirVld_Cnt_T_logl   | boolean | 0U  | 1U  |
|                   | \*FordVehReRiWhlCntrDirVld_Cnt_T_logl   | boolean | 0U  | 1U  |
| Return Value      |                                         |         |     |     |

## Design Rationale

## Processing

Please refer to the below path in the FDD model.

MM064A_FordMsg216BusHiSpd/FordMsg216BusHiSpd/FordMsg216BusHiSpdPer1/FordMsg064MsgMiss

## Local Function \#5

| **Function Name** | MsgPrsnt                                | Type    | Min | Max  |
|-----------|-----------------------------|--------------|--------|-----------|
| Arguments Passed  | Ford_WhlDirFl_D_Actl_Cnt_T_enum         | Enum    | 0U  | 3U   |
|                   | Ford_WhlDirFr_D_Actl_Cnt_T_enum         | Enum    | 0U  | 3U   |
|                   | Ford_WhlDirRl_D_Actl_Cnt_T_enum         | Enum    | 0U  | 3U   |
|                   | Ford_WhlDirRr_D_Actl_Cnt_T_enum         | Enum    | 0U  | 3U   |
|                   | Ford_WhlRotatFl_No_Cnt_Cnt_T_u08        | uint8   | 0   | 255U |
|                   | Ford_WhlRotatFr_No_Cnt_Cnt_T_u08        | uint8   | 0   | 255U |
|                   | Ford_WhlRotatRl_No_Cnt_Cnt_T_u08        | uint8   | 0   | 255U |
|                   | Ford_WhlRotatRr_No_Cnt_Cnt_T_u08        | uint8   | 0   | 255U |
|                   | MissMsgDiagEna_Cnt_T_logl               | boolean | 0U  | 1U   |
|                   | ClrDiagcFlgProxyEna_Cnt_logl            | boolean | 0U  | 1U   |
|                   | \*FordVehFrntLeWhlDirRaw_Cnt_T_enum     | Enum    | 0U  | 3U   |
|                   | \*FordVehFrntRiWhlDirRaw_Cnt_T_enum     | Enum    | 0U  | 3U   |
|                   | \*FordVehReLeWhlDirRaw_Cnt_T_enum       | Enum    | 0U  | 3U   |
|                   | \*FordVehReRiWhlDirRaw_Cnt_T_enum       | Enum    | 0U  | 3U   |
|                   | \*FordVehFrntLeWhlRollgCntr_Cnt_T_u08   | uint8   | 0   | 255U |
|                   | \*FordVehFrntRiWhlRollgCntr_Cnt_T_u08   | uint8   | 0   | 255U |
|                   | \*FordVehReLeWhlRollgCntr_Cnt_T_u08     | uint8   | 0   | 255U |
|                   | \*FordVehReRiWhlRollgCntr_Cnt_T_u0,     | uint8   | 0   | 255U |
|                   | \*FordVehFrntLeWhlCntrDirVld_Cnt_T_logl | boolean | 0U  | 1U   |
|                   | \*FordVehFrntRiWhlCntrDirVld_Cnt_T_logl | boolean | 0U  | 1U   |
|                   | \*FordVehReLeWhlCntrDirVld_Cnt_T_logl   | boolean | 0U  | 1U   |
|                   | \*FordVehReRiWhlCntrDirVld_Cnt_T_logl)  | boolean | 0U  | 1U   |
| Return Value      |                                         |         |     |      |

## Design Rationale

## Processing

Please refer to the below path in the FDD model.

MM064A_FordMsg216BusHiSpd/FordMsg216BusHiSpd/FordMsg216BusHiSpdPer1/Msg_Prsnt

## Local Function \#6

| **Function Name** | MissMsgNtcPass               | Type    | Min | Max |
|-------------------|------------------------------|---------|-----|-----|
| Arguments Passed  | MissMsgDiagEna_Cnt_T_logl    | boolean | 0U  | 1U  |
|                   | ClrDiagcFlgProxyEna_Cnt_logl | boolean | 0U  | 1U  |
| Return Value      |                              |         |     |     |

## Design Rationale

## Processing

Please refer to the below path in the FDD model.

MM064A_FordMsg216BusHiSpd/FordMsg216BusHiSpd/FordMsg216BusHiSpdPer1/Msg_Prsnt

## Local Function \#7

| **Function Name** | FordVehWhlDirRawProcg               | Type    | Min | Max |
|-------------------|-------------------------------------|---------|-----|-----|
| Arguments Passed  | Ford_WhlDir_D_Actl                  | Enum    | 0U  | 3U  |
|                   | \*FordVehWhlDirRaw_Cnt_T_enum       | Enum    | 0U  | 3U  |
|                   | \*FordVehWhlDirRawVldFlg_Cnt_T_logl | boolean | 0U  | 1U  |
| Return Value      |                                     |         |     |     |

## Design Rationale

## Processing

Please refer to the below path in the FDD model.

MM064A_FordMsg216BusHiSpd/FordMsg216BusHiSpd/FordMsg216BusHiSpdPer1/Msg_Prsnt/OutputProcessing

## Local Function \#8

| **Function Name** | VldElpdTi                                        | Type    | Min | Max        |
|----------|-------------------------------------|--------|--------|-----------|
| Arguments Passed  | CntrDirVldRefTi_Cnt_T_u32                        | Uint32  | 0   | 4294967295 |
|                   | FordMsg216BusHiSpdWhlCntrDirTiThd_MilliSec_T_u16 | Uint16  | 0   | 65535      |
|                   | \* WhlCntrDirVldElpdTi_Cnt_T_logl                | boolean | 0U  | 1U         |
| Return Value      |                                                  |         |     |            |

## Design Rationale

## Processing

Please refer to the below path in the FDD model.

MM064A_FordMsg216BusHiSpd/FordMsg216BusHiSpd/FordMsg216BusHiSpdPer1/Msg_Prsnt/OutputProcessing/VldElpdTi

## Local Function \#9

| **Function Name** | ChkElpdTiFrnt                             | Type    | Min | Max |
|----------|-------------------------------------|--------|---------|----------|
| Arguments Passed  | FordVehFrntLeWhlCntrDirVldFlg_Cnt_T_logl  | boolean | 0U  | 1U  |
|                   | FordVehFrntRiWhlCntrDirVldFlg_Cnt_T_log   | boolean | 0U  | 1U  |
|                   | FrntLeWhlCntrDirVldPassdElpdTi_Cnt_T_logl | boolean | 0U  | 1U  |
|                   | FrntLeWhlCntrDirVldFaildElpdTi_Cnt_T_logl | boolean | 0U  | 1U  |
|                   | FrntRiWhlCntrDirVldPassdElpdTi_Cnt_T_logl | boolean | 0U  | 1U  |
|                   | FrntRiWhlCntrDirVldFaildElpdTi_Cnt_T_logl | boolean | 0U  | 1U  |
|                   | \*FordVehFrntLeWhlCntrDirVld_Cnt_T_logl   | boolean | 0U  | 1U  |
|                   | \*FordVehFrntRiWhlCntrDirVld_Cnt_T_logl   | boolean | 0U  | 1U  |
| Return Value      |                                           |         |     |     |

## Design Rationale

## Processing

Please refer to the below path in the FDD
model.MM064A_FordMsg216BusHiSpd_SIL/FordMsg216BusHiSpd/FordMsg216BusHiSpdPer1/Msg_Prsnt/OutputProcessing/ChkElpdTi

## Local Function \#10

| **Function Name** | ChkElpdTiRear                           | Type    | Min | Max |
|----------|-------------------------------------|--------|---------|----------|
| Arguments Passed  | FordVehReLeWhlCntrDirVldFlg_Cnt_T_logl  | boolean | 0U  | 1U  |
|                   | FordVehReRiWhlCntrDirVldFlg_Cnt_T_logl  | boolean | 0U  | 1U  |
|                   | ReLeWhlCntrDirVldPassdElpdTi_Cnt_T_logl | boolean | 0U  | 1U  |
|                   | ReLeWhlCntrDirVldFaildElpdTi_Cnt_T_logl | boolean | 0U  | 1U  |
|                   | ReRiWhlCntrDirVldPassdElpdTi_Cnt_T_logl | boolean | 0U  | 1U  |
|                   | ReRiWhlCntrDirVldFaildElpdTi_Cnt_T_logl | boolean | 0U  | 1U  |
|                   | \*FordVehReLeWhlCntrDirVld_Cnt_T_logl   | boolean | 0U  | 1U  |
|                   | \*FordVehReRiWhlCntrDirVld_Cnt_T_logl   | boolean | 0U  | 1U  |
| Return Value      |                                         |         |     |     |

## Design Rationale

## Processing

Please refer to the below path in the FDD
model.MM064A_FordMsg216BusHiSpd_SIL/FordMsg216BusHiSpd/FordMsg216BusHiSpdPer1/Msg_Prsnt/OutputProcessing/ChkElpdTi

## GLOBAL Function/Macro Definitions

None

# Known Limitations with Design

None

# UNIT TEST CONSIDERATION

None

# Abbreviations and Acronyms

| **Abbreviation or Acronym** | **Description**                              |
|------------------------|------------------------------------------------|
| FDD                         | Functional Design Document. (See references) |

# Glossary

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

# References

| Ref. \# | Title                                                                        | Version                        |
|-------|----------------------------------------|-------------------------|
| 1       | AUTOSAR Specification of Memory Mapping (Link:AUTOSAR_SWS_MemoryMapping.pdf) | v1.3.0 R4.0 Rev 2              |
| 2       | MDD Guideline                                                                | EA4 01.02                      |
| 3       | Software Naming Conventions.doc                                              | EA4 01.02                      |
| 4       | Software Design and Coding Standards.doc                                     | EA4 2.01                       |
| 5       | FDD: MM064A_FordMsg216BusHiSpd_Design                                        | See Synergy subproject version |

{% endraw %}