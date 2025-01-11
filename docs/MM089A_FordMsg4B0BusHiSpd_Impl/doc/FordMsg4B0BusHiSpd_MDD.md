---
layout: default
title: FordMsg4B0BusHiSpd_MDD
nav_order: 2
parent: Component Implementation
---
{% raw %}
**Module Design Document**

**For**

**FordMsg4B0BusHiSpd**

**Prepared For:**

**,**

**Prepared By:**

**TATA ELXSI,**

**INDIA**

**  
<u>Change History</u>**

|                 |            |             |             |
|-----------------|------------|-------------|-------------|
| **Description** | **Author** | **Version** | **Date**    |
| Initial version | TATA ELXSI | 1           | 17-Apr-2018 |

**  
**

<span id="_Toc511761596" class="anchor"></span><u>Table of Contents</u>

[Table of Contents [3](#_Toc511761596)](#_Toc511761596)

[1 Introduction [5](#introduction)](#introduction)

[1.1 Purpose [5](#purpose)](#purpose)

[1.2 Scope [5](#scope)](#scope)

[2 FordMsg4B0BusHiSpd & High-Level Description
[6](#fordmsg4b0bushispd-high-level-description)](#fordmsg4b0bushispd-high-level-description)

[3 Design details of software module
[7](#design-details-of-software-module)](#design-details-of-software-module)

[3.1 Graphical representation of FordMsg4B0BusHiSpd
[7](#graphical-representation-of-fordmsg4b0bushispd)](#graphical-representation-of-fordmsg4b0bushispd)

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

[5.1.1 Init: FordMsg4B0BusHiSpdInit1
[9](#init-fordmsg4b0bushispdinit1)](#init-fordmsg4b0bushispdinit1)

[5.1.2 Per: FordMsg4B0BusHiSpdPer1
[9](#per-fordmsg4b0bushispdper1)](#per-fordmsg4b0bushispdper1)

[5.2 Server Runables [9](#server-runnables)](#server-runnables)

[5.3 Interrupt Functions
[9](#interrupt-functions)](#interrupt-functions)

[5.4 Module Internal (Local) Functions
[9](#module-internal-local-functions)](#module-internal-local-functions)

[5.4.1 Local Function \#1 [9](#local-function-1)](#local-function-1)

[5.4.1.1 Design Rationale
[10](#design-rationale-4)](#design-rationale-4)

[5.4.1.2 Processing [10](#processing)](#processing)

[5.4.2 Local Function \#2 [10](#local-function-2)](#local-function-2)

[5.4.2.1 Design Rationale
[10](#design-rationale-5)](#design-rationale-5)

[5.4.2.2 Processing [10](#processing-1)](#processing-1)

[5.4.3 Local Function \#3 [10](#local-function-3)](#local-function-3)

[5.4.3.1 Design Rationale
[11](#design-rationale-6)](#design-rationale-6)

[5.4.3.2 Processing [11](#processing-2)](#processing-2)

[5.4.4 Local Function \#4 [11](#local-function-4)](#local-function-4)

[5.4.4.1 Design Rationale
[11](#design-rationale-7)](#design-rationale-7)

[5.4.4.2 Processing [11](#processing-3)](#processing-3)

[5.4.5 Local Function \#5 [11](#local-function-5)](#local-function-5)

[5.4.5.1 Design Rationale
[11](#design-rationale-8)](#design-rationale-8)

[5.4.5.2 Processing [11](#processing-4)](#processing-4)

[5.4.6 Local Function \#6 [12](#local-function-6)](#local-function-6)

[5.4.6.1 Design Rationale
[12](#design-rationale-9)](#design-rationale-9)

[5.4.6.2 Processing [12](#processing-5)](#processing-5)

[5.4.7 Local Function \#7 [12](#local-function-7)](#local-function-7)

[5.4.7.1 Design Rationale
[12](#design-rationale-10)](#design-rationale-10)

[5.4.7.2 Processing [12](#processing-6)](#processing-6)

[5.5 GLOBAL Function/Macro Definitions
[12](#global-functionmacro-definitions)](#global-functionmacro-definitions)

[6 Known Limitations with Design
[13](#known-limitations-with-design)](#known-limitations-with-design)

[7 UNIT TEST CONSIDERATION
[14](#unit-test-consideration)](#unit-test-consideration)

[Appendix A Abbreviations and Acronyms
[15](#abbreviations-and-acronyms)](#abbreviations-and-acronyms)

[Appendix B Glossary [16](#glossary)](#glossary)

[Appendix C References [17](#references)](#references)

# Introduction

## Purpose

Module Design Document for MM089A_FordMsg4B0BusHiSpd_Impl.

## Scope

The following definitions are used throughout this document:

-   **<u>Shall</u>**: indicates a mandatory requirement without
    exception in compliance.

-   **<u>Should</u>**: indicates a mandatory requirement; exceptions
    allowed only with documented justification.

-   **<u>May</u>**: indicates an optional action.

# FordMsg4B0BusHiSpd & High-Level Description

The purpose of the Ford Message 4B0 Bus High Speed function is to
provide the Electric Power Steering system with signal values for the
Torque Steer Compensation, Brake Oscillation Reduction, Lane Detection
Warning, LKA, Traffic Jam Assist, Lane Center Assist, and Evasive Steer
Assist functions from CAN. The Ford Message 4B0 function will perform
the missing message and signal invalid diagnostics as well as provide a
validity flag for the signal values and received message.

# Design details of software module

## Graphical representation of FordMsg4B0BusHiSpd

<img
src="ElectricPowerSteering_RH850_FORD_T3T6_website/docs/MM089A_FordMsg4B0BusHiSpd_Impl/doc/mediax/media/image1.png"
style="width:4.25in;height:5.29167in" />

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

| Constant Name                        | Resolution | Units | Value |
|--------------------------------------|------------|-------|-------|
| Please refer Data Dictionary .m file | NA         | NA    | NA    |

# Software Component Implementation

## Sub-Module Functions

The sub-module functions are grouped based on similar functionality that
needs to be executed in a given “State” of the system (refer States and
Modes). For a given module, the MDD will identify the type and number of
sub-modules required. The sub-module types are described below.

### Init: FordMsg4B0BusHiSpdInit1

#### Design Rationale

Refer FDD

#### Module Outputs

Refer FDD

### Per: FordMsg4B0BusHiSpdPer1

#### Design Rationale

Refer FDD

#### Store Module Inputs to Local copies

Refer FDD

#### (Processing of function)………

Refer FDD

#### Store Local copy of outputs into Module Outputs

Refer FDD

## Server Runnables

### ComIPduCallout_ABS_BrkBst_Data_FD1

## 5.2.1.1 Design Rationale [design-rationale-2]

None

## 5.2.1.2 Processing of function [processing-of-function-1]

None

### ComTimeoutNotification_YawStabilityIndex

## 5.2.2.1 Design Rationale [design-rationale-3]

None

## 5.2.2.2 Processing of function [processing-of-function-2]

None

## Interrupt Functions

None

## Module Internal (Local) Functions

## Local Function \#1

| **Function Name** | SetNTC                           | Type    | Min | Max |
|-------------------|----------------------------------|---------|-----|-----|
| Arguments Passed  | FordTqSteerCmpEnad_Cnt_T_logl    | boolean | 0U  | 1U  |
|                   | FordBrkOscnRednEnad_Cnt_T_logl   | boolean | 0U  | 1U  |
|                   | LaneDetnWarnEnad_Cnt_T_logl      | boolean | 0U  | 1U  |
|                   | LaneKeepAssiEnad_Cnt_T_logl      | boolean | 0U  | 1U  |
|                   | ClrDiagcFlgProxyEna_Cnt_log      | boolean | 0U  | 1U  |
|                   | TrfcJamAssiEnad_Cnt_T_logl       | boolean | 0U  | 1U  |
|                   | FordLaneCentrAssiEnad_Cnt_T_logl | boolean | 0U  | 1U  |
|                   | FordEvasSteerAssiEnad_Cnt_T_logl | boolean | 0U  | 1U  |
|                   | FordCanDtcInhb_Cnt_T_logl        | boolean | 0U  | 1U  |
|                   | FordEpsLifeCycMod_Cnt_T_u08      | uint8   | 0U  | 1U  |
|                   | ClrDiagcFlgProxy_Cnt_T_u08       | boolean | 0U  | 1U  |
|                   | FordVehYawStabyRaw_Cnt_T_enum    | boolean | 0U  | 1U  |
| Return Value      |                                  |         |     |     |

## Design Rationale

## Processing

Please refer to the below path in the FDD model.

MM089A_FordMsg4B0BusHiSpd/FordMsg4B0BusHiSpd/FordMsg4B0BusHiSpdPer1

## Local Function \#2

| **Function Name** | SetNTC_0x18D                   | Type    | Min | Max         |
|------------|---------------------------|---------------|---------|------------|
| Arguments Passed  | FeatCdn_Cnt_T_logl             | boolean | 0U  | 1U          |
|                   | CanDtcInhbEna_Cnt_T_logl       | boolean | 0U  | 1U          |
|                   | MsgMissNtcDiagcTiThd_Cnt_T_u32 | uint32  | 0U  | 4294967295U |
| Return Value      |                                |         |     |             |

## Design Rationale

## Processing

Please refer to the below path in the FDD model.

MM089A_FordMsg4B0BusHiSpd/FordMsg4B0BusHiSpd/FordMsg4B0BusHiSpdPer1/SetNTC

## Local Function \#3

| **Function Name** | SetNTC_0x18E                  | Type    | Min | Max         |
|------------|---------------------------|---------------|---------|------------|
| Arguments Passed  | FeatCdn_Cnt_T_logl            | boolean | 0U  | 1U          |
|                   | CanDtcInhbEna_Cnt_T_logl      | boolean | 0U  | 1U          |
|                   | MsgFltNtcDiagcTiThd_Cnt_T_u32 | uint32  | 0U  | 4294967295U |
|                   | FordVehYawStabyRaw_Cnt_T_enum | Enum    | 0U  | 511U        |
| Return Value      |                               |         |     |             |

## Design Rationale

## Processing

Please refer to the below path in the FDD model.

MM089A_FordMsg4B0BusHiSpd
/FordMsg4B0BusHiSpd/FordMsg4B0BusHiSpdPer1/SetNTC

## Local Function \#4

| **Function Name** | MsgVldChk            | Type    | Min | Max |
|-------------------|----------------------|---------|-----|-----|
| Arguments Passed  | MsgVld_Cnt_T_logl    | boolean | 0U  | 1U  |
| Return Value      | MsgVldFlg_Cnt_T_logl | boolean | 0U  | 1U  |

## Design Rationale

## Processing

Please refer to the below path in the FDD model.

MM089A_FordMsg4B0BusHiSpd/FordMsg4B0BusHiSpd/FordMsg4B0BusHiSpdPer1/SetNTC

## Local Function \#5

| **Function Name** | MsgMissChk              | Type    | Min | Max |
|-------------------|-------------------------|---------|-----|-----|
| Arguments Passed  | None                    |         |     |     |
| Return Value      | MsgNotRxdFlg_Cnt_T_logl | boolean | 0U  | 1U  |

## Design Rationale

## Processing

Please refer to the below path in the FDD model.

MM089A_FordMsg4B0BusHiSpd/FordMsg4B0BusHiSpd/FordMsg4B0BusHiSpdPer1/SetNTC

## Local Function \#6

| **Function Name** | MsgNoDataExistChk             | Type    | Min | Max  |
|-------------------|-------------------------------|---------|-----|------|
| Arguments Passed  | FordVehYawStabyRaw_Cnt_T_enum | Enum    | 0U  | Enum |
| Return Value      | MsgNoDataExistFlg_Cnt_T_logl  | boolean | 0U  | 1U   |

## Design Rationale

## Processing

Please refer to the below path in the FDD model.

MM089A_FordMsg4B0BusHiSpd/FordMsg4B0BusHiSpd/FordMsg4B0BusHiSpdPer1/SetNTC

## Local Function \#7

| **Function Name** | MsgFltChk                     | Type    | Min | Max  |
|-------------------|-------------------------------|---------|-----|------|
| Arguments Passed  | FordVehYawStabyRaw_Cnt_T_enum | Enum    | 0U  | Enum |
| Return Value      | MsgFltFlg_Cnt_T_logl          | boolean | 0U  | 1U   |

## Design Rationale

## Processing

Please refer to the below path in the FDD model.

MM089A_FordMsg4B0BusHiSpd/FordMsg4B0BusHiSpd/FordMsg4B0BusHiSpdPer1/SetNTC

## GLOBAL Function/Macro Definitions

None

# Known Limitations with Design

None.

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
| 5       | FDD: MM089A_FordMsg4B0BusHiSpd_Design                                        | See Synergy subproject version |

{% endraw %}