---
layout: default
title: FordMsg3CABusHiSpd_MDD
nav_order: 2
parent: Component Implementation
---
{% raw %}
**Module Design Document**

**For**

**FordMsg3CABusHiSpd**

**04-May-2018**

**Prepared For:**

**Software Engineering**

**Nexteer Automotive,**

**Saginaw, MI, USA**

**Prepared By:**

**TATA ELXSI,**

**INDIA**

**<u>Change History</u>**

|             |                                                                         |                        |             |             |
|--------|---------------------------|---------------|---------|--------------|
| **Sl. No.** | **Description**                                                         | **Author**             | **Version** | **Date**    |
| 1           | Initial version                                                         | TATA ELXSI             | 1.0         | 22-Apr-2018 |
| 2           | Changed local function OutpProcg arguments to match with implementation | Shishir Holenarasipura | 2.0         | 04-May-2018 |

**  
**

<span id="_Toc512160234" class="anchor"></span><u>Table of Contents</u>

[Table of Contents [3](#_Toc512160234)](#_Toc512160234)

[1 Introduction [5](#introduction)](#introduction)

[1.1 Purpose [5](#purpose)](#purpose)

[1.2 Scope [5](#scope)](#scope)

[2 FordMsg3CABusHiSpd & High-Level Description
[6](#fordmsg3cabushispd-high-level-description)](#fordmsg3cabushispd-high-level-description)

[3 Design details of software module
[7](#design-details-of-software-module)](#design-details-of-software-module)

[3.1 Graphical representation of FordMsg3CABusHiSpd
[7](#graphical-representation-of-fordmsg3cabushispd)](#graphical-representation-of-fordmsg3cabushispd)

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

[5.1.1 Init: FordMsg3CABusHiSpdInit1
[9](#init-fordmsg3cabushispdinit1)](#init-fordmsg3cabushispdinit1)

[5.1.2 Per: FordMsg3CABusHiSpdPer1
[9](#per-fordmsg3cabushispdper1)](#per-fordmsg3cabushispdper1)

[5.2 Server Runables [9](#server-runnables)](#server-runnables)

[5.3 Interrupt Functions
[9](#comipducallout_lane_assist_data1_fd1)](#comipducallout_lane_assist_data1_fd1)

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
[10](#design-rationale-6)](#design-rationale-6)

[5.4.3.2 Processing [11](#processing-2)](#processing-2)

[5.4.4 Local Function \#4 [11](#_Toc512160263)](#_Toc512160263)

[5.4.4.1 Design Rationale [11](#_Toc512160264)](#_Toc512160264)

[5.4.4.2 Processing [11](#_Toc512160265)](#_Toc512160265)

[5.4.5 Local Function \#5 [11](#local-function-5)](#local-function-5)

[5.4.5.1 Design Rationale
[11](#design-rationale-7)](#design-rationale-7)

[5.4.5.2 Processing [11](#processing-3)](#processing-3)

[5.4.6 Local Function \#6 [11](#local-function-6)](#local-function-6)

[5.4.7 Design Rationale [12](#design-rationale-8)](#design-rationale-8)

[5.4.7.1 Processing [12](#processing-4)](#processing-4)

[5.4.7 Local Function \#7 [12](#local-function-7)](#local-function-7)

[5.4.7.1 Design Rationale
[13](#design-rationale-9)](#design-rationale-9)

[5.4.7.2 Processing [13](#processing-5)](#processing-5)

[5.4.8 Local Function \#8 [13](#local-function-8)](#local-function-8)

[5.4.8.1 Design Rationale
[13](#design-rationale-10)](#design-rationale-10)

[5.4.8.2 Processing [13](#processing-6)](#processing-6)

[5.4.9 Local Function \#9 [13](#local-function-9)](#local-function-9)

[5.4.9.1 Design Rationale
[14](#design-rationale-11)](#design-rationale-11)

[5.4.9.2 Processing [14](#processing-7)](#processing-7)

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

Module Design Document for MM073A_FordMsg3CABusHiSpd_Impl.

## Scope

The following definitions are used throughout this document:

-   **<u>Shall</u>**: indicates a mandatory requirement without
    exception in compliance.

-   **<u>Should</u>**: indicates a mandatory requirement; exceptions
    allowed only with documented justification.

-   **<u>May</u>**: indicates an optional action.

# FordMsg3CABusHiSpd & High-Level Description

The purpose of the Ford Message 3CA Bus High Speed function is to
provide the Electric Power Steering system with signal values for Lane
Detection Warning and Lane Keep Assist functions form CAN. The Ford
Message 3CA function will perform the missing message and signal invalid
diagnostics as well as provide a validity signal for the signal values
and received message.

# Design details of software module

## Graphical representation of FordMsg3CABusHiSpd

<img
src="ElectricPowerSteering_RH850_FORD_T3T6_website/docs/MM073A_FordMsg3CABusHiSpd_Impl/doc/mediax/media/image1.png"
style="width:6.14583in;height:5.42708in" />

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

| Constant Name               | Resolution | Units | Value |
|-----------------------------|------------|-------|-------|
| Refer .m file for constants |            |       |       |

# Software Component Implementation

## Sub-Module Functions

The sub-module functions are grouped based on similar functionality that
needs to be executed in a given “State” of the system (refer States and
Modes). For a given module, the MDD will identify the type and number of
sub-modules required. The sub-module types are described below.

### Init: FordMsg3CABusHiSpdInit1

#### Design Rationale

Refer FDD

#### Module Outputs

Refer FDD

### Per: FordMsg3CABusHiSpdPer1

#### Design Rationale

Refer FDD

#### Store Module Inputs to Local copies

Refer FDD

#### (Processing of function)………

Refer FDD

#### Store Local copy of outputs into Module Outputs

Refer FDD

## Server Runnables 

### ComIPduCallout_Lane_Assist_Data1_FD1

## 5.2.1.1 Design Rationale [design-rationale-2]

None

## 5.2.1.2 Processing of function [processing-of-function-1]

None

###  ComTimeoutNotification_LaCurvature_No_Calc

## 5.2.2.1 Design Rationale [design-rationale-3]

None

## 5.2.2.2 Processing of function [processing-of-function-2]

None

## Interrupt Functions

None

## Module Internal (Local) Functions

## Local Function \#1

|                      |                                      |         |     |     |
|------------|------------------------------|---------|-----------|-----------|
| **Function Name**    | DiagEna                              | Type    | Min | Max |
| **Arguments Passed** | FordLaneDetnWarnEnad_Cnt_T_logl      | boolean | 0U  | 1U  |
|                      | FordLaneKeepAssiEnad_Cnt_T_logl      | boolean | 0U  | 1U  |
|                      | ClrDiagcFlgProxy_Cnt_T_u08           | uint8   | 0U  | 1U  |
|                      | FordCanDtcInhb_Cnt_T_logl            | boolean | 0U  | 1U  |
|                      | \*MissMsgDiagEna_Cnt_T_logl          | boolean | 0U  | 1U  |
|                      | \*ClrDiagcFlgProxyDiagEna_Cnt_T_logl | boolean | 0U  | 1U  |
|                      | \*InvldDiagEna_Cnt_T_logl            | boolean | 0U  | 1U  |
| **Return Value**     | NA                                   |         |     |     |

## Design Rationale

None

## Processing

Please refer to the below path in the FDD model.

MM073A_FordMsg3CABusHiSpd/FordMsg3CABusHiSpd/FordMsg3CABusHiSpdPer1/DiagEna

##  Local Function \#2

|                      |                                                      |        |     |       |
|----------|--------------------------------------|--------|-------|----------|
| **Function Name**    | CalSeln                                              | Type   | Min | Max   |
| **Arguments Passed** | FordEpsLifeCycMod_Cnt_T_u08                          | uint8  | 0U  | 1U    |
|                      | \*BusHiSpdMissTiThd_MilliSec_T_u16                   | uint16 | 0U  | 6000U |
|                      | \*BusHiSpdLaneKeepSysReqdAgInvldTiThd_MilliSec_T_u16 | uint16 | 0U  | 6000U |
|                      | \*BusHiSpdLaneKeepSysCrvInvldTiThd_MilliSec_T_u16    | uint16 | 0U  | 6000U |
| **Return Value**     | NA                                                   |        |     |       |

## Design Rationale

None

## Processing

Please refer to the below path in the FDD model.

MM073A_FordMsg3CABusHiSpd/FordMsg3CABusHiSpd/FordMsg3CABusHiSpdPer1/CalSeln

##  Local Function \#3

|                      |                                  |         |     |       |
|-----------|--------------------------------|---------|----------|-----------|
| **Function Name**    | MissMsgDiagEnaChk                | Type    | Min | Max   |
| **Arguments Passed** | MissMsgDiagEna_Cnt_T_logl        | boolean | 0U  | 1U    |
|                      | BusHiSpdMissTiThd_MilliSec_T_u16 | uint16  | 0U  | 6000U |
| **Return Value**     | NA                               |         |     |       |

## Design Rationale

None

## Processing

Please refer to the below path in the FDD model.

MM073A_FordMsg3CABusHiSpd/FordMsg3CABusHiSpd/FordMsg3CABusHiSpdPer1/MsgMiss/MissMsgNtcFail,
MM073A_FordMsg3CABusHiSpd/FordMsg3CABusHiSpd/FordMsg3CABusHiSpdPer1/MsgMiss/MissNtcPassTmrRst

## Local Function \#5

|                      |                                                    |         |     |       |
|-----------|-------------------------------------|--------|---------|---------|
| **Function Name**    | FordVehPrpnWhlTqSigInvldNtc                        | Type    | Min | Max   |
| **Arguments Passed** | BusHiSpdLaneKeepSysCrvInvldTiThd_MilliSec_T_u16    | uint16  | 0U  | 6000U |
|                      | LaneKeepSysCrvtRawVldInp_Cnt_T_logl                | boolean | 0U  | 1U    |
|                      | BusHiSpdLaneKeepSysReqdAgInvldTiThd_MilliSec_T_u16 | uint16  | 0U  | 6000U |
|                      | LaneKeepSysReqdAgRawVldInp_Cnt_T_logl              | boolean | 0U  | 1U    |
| **Return Value**     | NA                                                 |         |     |       |

## Design Rationale

None

## Processing

Please refer to the below path in the FDD model.

MM073A_FordMsg3CABusHiSpd/FordMsg3CABusHiSpd/FordMsg3CABusHiSpdPer1/MsgPrsnt/FordVehPrpnWhlTqSigInvldNtc

##  Local Function \#6

|                      |                                              |                          |           |          |
|---------|------------------------------|------------------|--------|--------|
| **Function Name**    | OutpProcg                                    | Type                     | Min       | Max      |
| **Arguments Passed** | Ford_LaCurvature_No_Calc_Cnt_T_enum          | Ford_LaCurvature_No_Calc | 0U        | 4095U    |
|                      | Ford_LaRampType_B_Req_Cnt_T_enum             | Ford_LaRampType_B_Req    | 0U        | 1U       |
|                      | Ford_LaRefAng_No_Req_Cnt_T_enum              | Ford_LaRefAng_No_Req     | 0U        | 4095U    |
|                      | Ford_LdwActvIntns_D_Req_Cnt_T_enum           | Ford_LdwActvIntns_D_Req  | 0U        | 3U       |
|                      | Ford_LdwActvStats_D_Req_Cnt_T_enum           | Ford_LdwActvStats_D_Req  | 0U        | 7U       |
|                      | Ford_LkaActvStats_D2_Req_Cnt_T_enum          | Ford_LkaActvStats_D2_Req | 0U        | 7U       |
|                      | \*FordVehLaneKeepSysCrvtRaw_Cnt_T_u16        | uint16                   | 0U        | 4095U    |
|                      | \*FordVehLaneKeepSysCrvt_IvsMtr_T_f32        | float32                  | -0.01024F | 0.01023F |
|                      | \*FordVehLaneKeepSysRampTyp_Cnt_T_u08        | uint8                    | 0U        | 1U       |
|                      | \*FordVehLaneKeepSysReqdAgRaw_Cnt_T_u16      | uint16                   | 0U        | 4095U    |
|                      | \*FordVehLaneKeepSysReqdAg_MilliRad_T_f32    | float32                  | -102.4F   | 102.3F   |
|                      | \*FordVehLaneDetnWarnInten_Cnt_T_u08         | uint8                    | 0U        | 3U       |
|                      | \*FordVehLaneDetnWarnSts_Cnt_T_u08           | uint8                    | 0U        | 7U       |
|                      | \*FordVehLaneKeepSysSts_Cnt_T_u08            | uint8                    | 0U        | 7U       |
|                      | \*FordVehLaneAssiImgProcgModlAVld_Cnt_T_logl | boolean                  | 0U        | 1U       |
|                      | \*LaneKeepSysCrvtRawVldInp_Cnt_T_logl        | boolean                  | 0U        | 1U       |
|                      | \*LaneKeepSysReqdAgRawVldInp_Cnt_T_logl      | boolean                  | 0U        | 1U       |
| **Return Value**     | NA                                           |                          |           |          |

## Design Rationale

None

## Processing

Please refer to the below path in the FDD model.

MM073A_FordMsg3CABusHiSpd/FordMsg3CABusHiSpd/FordMsg3CABusHiSpdPer1/MsgPrsnt/OutputProcg

###  Local Function \#7

|                      |                                         |         |     |       |
|------------|-------------------------------|---------|-----------|-----------|
| **Function Name**    | VldProcg                                | Type    | Min | Max   |
| **Arguments Passed** | FordVehLaneKeepSysCrvtRaw_Cnt_T_u16     | uint16  | 0U  | 4095U |
|                      | FordVehLaneKeepSysReqdAgRaw_Cnt_T_u16   | uint16  | 0U  | 4095U |
|                      | \*LaneKeepSysCrvtRawVldInp_Cnt_T_logl   | boolean | 0U  | 1U    |
|                      | \*LaneKeepSysReqdAgRawVldInp_Cnt_T_logl | boolean | 0U  | 1U    |
|                      | \*LaneKeepSysVldInp_Cnt_T_logl          | boolean | 0U  | 1U    |
| **Return Value**     | NA                                      |         |     |       |

## Design Rationale

None

## Processing

Please refer to the below path in the FDD model.

MM073A_FordMsg3CABusHiSpd/FordMsg3CABusHiSpd/FordMsg3CABusHiSpdPer1/MsgPrsnt/OutputProcg/VldProcg

##  Local Function \#8

|                      |                                |         |     |     |
|----------------------|--------------------------------|---------|-----|-----|
| **Function Name**    | VldElpdTi                      | Type    | Min | Max |
| **Arguments Passed** | \*VldElpdTi_Cnt_T_logl         | boolean | 0U  | 1U  |
|                      | \*InvldCrvtElpdTi_Cnt_T_logl   | boolean | 0U  | 1U  |
|                      | \*InvldReqdAgElpdTi_Cnt_T_logl | boolean | 0U  | 1U  |
| **Return Value**     | NA                             |         |     |     |

## Design Rationale

None

## Processing

Please refer to the below path in the FDD model.

MM073A_FordMsg3CABusHiSpd/FordMsg3CABusHiSpd/FordMsg3CABusHiSpdPer1/MsgPrsnt/OutputProcg/VldElpdTi

##  Local Function \#9

|                      |                                              |         |     |     |
|------------|---------------------------------|---------|----------|----------|
| **Function Name**    | ChkElpdTi                                    | Type    | Min | Max |
| **Arguments Passed** | VldElpdTi_Cnt_T_logl                         | boolean | 0U  | 1U  |
|                      | InvldCrvtElpdTi_Cnt_T_logl                   | boolean | 0U  | 1U  |
|                      | InvldReqdAgElpdTi_Cnt_T_logl                 | boolean | 0U  | 1U  |
|                      | LaneKeepSysVldInp_Cnt_T_logl                 | boolean | 0U  | 1U  |
|                      | LaneKeepSysCrvtRawVldInp_Cnt_T_logl          | boolean | 0U  | 1U  |
|                      | LaneKeepSysReqdAgRawVldInp_Cnt_T_logl        | boolean | 0U  | 1U  |
|                      | \*FordVehLaneAssiImgProcgModlAVld_Cnt_T_logl | boolean | 0U  | 1U  |
| **Return Value**     | NA                                           |         |     |     |

## Design Rationale

None

## Processing

Please refer to the below path in the FDD model.

MM073A_FordMsg3CABusHiSpd/FordMsg3CABusHiSpd/FordMsg3CABusHiSpdPer1/MsgPrsnt/OutputProcg/ChkElpdTi

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
| 5       | FDD: MM073A_FordMsg3CABusHiSpd_Design                                        | See Synergy subproject version |

{% endraw %}