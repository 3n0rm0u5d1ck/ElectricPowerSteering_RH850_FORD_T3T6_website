---
layout: default
title: FordMsg077BusHiSpd_MDD
nav_order: 2
parent: Component Implementation
---
{% raw %}
**Module Design Document**

**For**

**FordMsg077BusHiSpd**

**02-May-2018**

**Prepared For:**

**Software Engineering**

**Nexteer Automotive,**

**Saginaw, MI, USA**

**Prepared By:**

**TATA ELXSI,**

**INDIA**

**<u>Change History</u>**

|             |                 |                        |             |             |
|--------|--------------------------|------------------|--------|--------------|
| **Sl. No.** | **Description** | **Author**             | **Version** | **Date**    |
| 1           | Initial version | Shishir Holenarasipura | 1.0         | 02-May-2018 |

**  
**

<span id="_Toc513218329" class="anchor"></span><u>Table of Contents</u>

[Table of Contents [3](#_Toc513218329)](#_Toc513218329)

[1 Introduction [6](#introduction)](#introduction)

[1.1 Purpose [6](#purpose)](#purpose)

[1.2 Scope [6](#scope)](#scope)

[2 FordMsg077BusHiSpd & High-Level Description
[7](#fordmsg077bushispd-high-level-description)](#fordmsg077bushispd-high-level-description)

[3 Design details of software module
[8](#design-details-of-software-module)](#design-details-of-software-module)

[3.1 Graphical representation of FordMsg077BusHiSpd
[8](#graphical-representation-of-fordmsg077bushispd)](#graphical-representation-of-fordmsg077bushispd)

[3.2 Data Flow Diagram [9](#data-flow-diagram)](#data-flow-diagram)

[3.2.1 Component level DFD
[9](#component-level-dfd)](#component-level-dfd)

[3.2.2 Function level DFD [9](#function-level-dfd)](#function-level-dfd)

[4 Constant Data Dictionary
[10](#constant-data-dictionary)](#constant-data-dictionary)

[4.1 Program (fixed) Constants
[10](#program-fixed-constants)](#program-fixed-constants)

[4.1.1 Embedded Constants
[10](#embedded-constants)](#embedded-constants)

[5 Software Component Implementation
[11](#software-component-implementation)](#software-component-implementation)

[5.1 Sub-Module Functions
[11](#sub-module-functions)](#sub-module-functions)

[5.1.1 Init: FordMsg077BusHiSpdInit1
[11](#init-fordmsg077bushispdinit1)](#init-fordmsg077bushispdinit1)

[5.1.2 Per: FordMsg077BusHiSpdPer1
[11](#per-fordmsg077bushispdper1)](#per-fordmsg077bushispdper1)

[5.2 Server Runnables [11](#server-runnables)](#server-runnables)

[5.2.1 ComIPduCallout_BrakeSnData_3_FD1
[11](#comipducallout_brakesndata_3_fd1)](#comipducallout_brakesndata_3_fd1)

[5.2.1.1 Design Rationale
[11](#design-rationale-2)](#design-rationale-2)

[5.2.1.2 Processing of function
[11](#processing-of-function-1)](#processing-of-function-1)

[5.2.2 ComTimeoutNotification_VehLatComp_A_Actl
[11](#comtimeoutnotification_vehlatcomp_a_actl)](#comtimeoutnotification_vehlatcomp_a_actl)

[5.2.2.1 Design Rationale
[11](#design-rationale-3)](#design-rationale-3)

[5.2.2.2 Processing of function
[11](#processing-of-function-2)](#processing-of-function-2)

[5.3 Interrupt Functions
[12](#interrupt-functions)](#interrupt-functions)

[5.4 Module Internal (Local) Functions
[12](#module-internal-local-functions)](#module-internal-local-functions)

[5.4.1 Local Function \#1 [12](#local-function-1)](#local-function-1)

[5.4.1.1 Design Rationale
[12](#design-rationale-4)](#design-rationale-4)

[5.4.1.2 Processing [12](#processing)](#processing)

[5.4.2 Local Function \#2 [12](#local-function-2)](#local-function-2)

[5.4.2.1 Design Rationale
[13](#design-rationale-5)](#design-rationale-5)

[5.4.2.2 Processing [13](#processing-1)](#processing-1)

[5.4.3 Local Function \#3 [13](#local-function-3)](#local-function-3)

[5.4.3.1 Design Rationale
[13](#design-rationale-6)](#design-rationale-6)

[5.4.3.2 Processing [13](#processing-2)](#processing-2)

[5.4.4 Local Function \#4 [14](#local-function-4)](#local-function-4)

[5.4.5 Design Rationale [14](#design-rationale-7)](#design-rationale-7)

[5.4.5.1 Processing [14](#processing-3)](#processing-3)

[5.4.6 Local Function \#5 [15](#local-function-5)](#local-function-5)

[5.4.6.1 Design Rationale
[15](#design-rationale-8)](#design-rationale-8)

[5.4.6.2 Processing [15](#processing-4)](#processing-4)

[5.4.7 Local Function \#6 [15](#local-function-6)](#local-function-6)

[5.4.7.1 Design Rationale
[15](#design-rationale-9)](#design-rationale-9)

[5.4.7.2 Processing [15](#processing-5)](#processing-5)

[5.4.8 Local Function \#7 [15](#local-function-7)](#local-function-7)

[5.4.8.1 Design Rationale
[16](#design-rationale-10)](#design-rationale-10)

[5.4.8.2 Processing [16](#processing-6)](#processing-6)

[5.4.9 Local Function \#8 [16](#local-function-8)](#local-function-8)

[5.4.9.1 Design Rationale
[16](#design-rationale-11)](#design-rationale-11)

[5.4.9.2 Processing [16](#processing-7)](#processing-7)

[5.4.10 Local Function \#9 [16](#local-function-9)](#local-function-9)

[5.4.10.1 Design Rationale
[16](#design-rationale-12)](#design-rationale-12)

[5.4.10.2 Processing [16](#processing-8)](#processing-8)

[5.4.11 Local Function \#10
[17](#local-function-10)](#local-function-10)

[5.4.11.1 Design Rationale
[17](#design-rationale-13)](#design-rationale-13)

[5.4.11.2 Processing [17](#processing-9)](#processing-9)

[5.4.12 Local Function \#11
[17](#local-function-11)](#local-function-11)

[5.4.12.1 Design Rationale
[17](#design-rationale-14)](#design-rationale-14)

[5.4.12.2 Processing [17](#processing-10)](#processing-10)

[5.4.13 Local Function \#12
[17](#local-function-12)](#local-function-12)

[5.4.13.1 Design Rationale
[18](#design-rationale-15)](#design-rationale-15)

[5.4.13.2 Processing [18](#processing-11)](#processing-11)

[5.4.14 Local Function \#13
[18](#local-function-13)](#local-function-13)

[5.4.14.1 Design Rationale
[18](#design-rationale-16)](#design-rationale-16)

[5.4.14.2 Processing [18](#processing-12)](#processing-12)

[5.4.15 Local Function \#14
[18](#local-function-14)](#local-function-14)

[5.4.15.1 Design Rationale
[18](#design-rationale-17)](#design-rationale-17)

[5.4.15.2 Processing [19](#processing-13)](#processing-13)

[5.4.16 Local Function \#15
[19](#local-function-15)](#local-function-15)

[5.4.16.1 Design Rationale
[19](#design-rationale-18)](#design-rationale-18)

[5.4.16.2 Processing [19](#processing-14)](#processing-14)

[5.4.17 Local Function \#16
[19](#local-function-16)](#local-function-16)

[5.4.17.1 Design Rationale
[19](#design-rationale-19)](#design-rationale-19)

[5.4.17.2 Processing [19](#processing-15)](#processing-15)

[5.4.18 Local Function \#17
[19](#local-function-17)](#local-function-17)

[5.4.18.1 Design Rationale
[20](#design-rationale-20)](#design-rationale-20)

[5.4.18.2 Processing [20](#processing-16)](#processing-16)

[5.4.19 Local Function \#18
[20](#local-function-18)](#local-function-18)

[5.4.19.1 Design Rationale
[20](#design-rationale-21)](#design-rationale-21)

[5.4.19.2 Processing [20](#processing-17)](#processing-17)

[5.5 GLOBAL Function/Macro Definitions
[20](#global-functionmacro-definitions)](#global-functionmacro-definitions)

[6 Known Limitations with Design
[21](#known-limitations-with-design)](#known-limitations-with-design)

[7 UNIT TEST CONSIDERATION
[22](#unit-test-consideration)](#unit-test-consideration)

[Appendix A Abbreviations and Acronyms
[23](#abbreviations-and-acronyms)](#abbreviations-and-acronyms)

[Appendix B Glossary [24](#glossary)](#glossary)

[Appendix C References [25](#references)](#references)

# Introduction

## Purpose

Module Design Document for MM124A_FordMsg077BusHiSpd_Impl.

## Scope

The following definitions are used throughout this document:

-   **<u>Shall</u>**: indicates a mandatory requirement without
    exception in compliance.

-   **<u>Should</u>**: indicates a mandatory requirement; exceptions
    allowed only with documented justification.

-   **<u>May</u>**: indicates an optional action.

# FordMsg077BusHiSpd & High-Level Description

Refer the FDD.

# Design details of software module

## Graphical representation of FordMsg077BusHiSpd

<img
src="ElectricPowerSteering_RH850_FORD_T3T6_website/docs/MM124A_FordMsg077BusHiSpd_Impl/doc/mediax/media/image1.png"
style="width:4.02083in;height:7.88331in" />

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

### Init: FordMsg077BusHiSpdInit1

#### Design Rationale

Refer FDD

#### Module Outputs

Refer FDD

### Per: FordMsg077BusHiSpdPer1

#### Design Rationale

Refer FDD

#### Store Module Inputs to Local copies

Refer FDD

#### (Processing of function)………

Refer FDD

#### Store Local copy of outputs into Module Outputs

Refer FDD

## Server Runnables 

### ComIPduCallout_BrakeSnData_3_FD1

## 5.2.1.1 Design Rationale [design-rationale-2]

None

## 5.2.1.2 Processing of function [processing-of-function-1]

None

###  ComTimeoutNotification_VehLatComp_A_Actl

## 5.2.2.1 Design Rationale [design-rationale-3]

None

## 5.2.2.2 Processing of function [processing-of-function-2]

None

## Interrupt Functions

None

## Module Internal (Local) Functions

## Local Function \#1

|                      |                                            |         |     |     |
|------------|-------------------------------|---------|-----------|----------|
| **Function Name**    | DiagEna                                    | Type    | Min | Max |
| **Arguments Passed** | FordTqSteerCmpEnad_Cnt_T_logl              | boolean | 0U  | 1U  |
|                      | FordBrkOscnRednEnad_Cnt_T_logl             | boolean | 0U  | 1U  |
|                      | FordLaneKeepAssiEnad_Cnt_T_logl            | boolean | 0U  | 1U  |
|                      | FordTrfcJamAssiEnad_Cnt_T_logl             | boolean | 0U  | 1U  |
|                      | FordLaneCentrAssiEnad_Cnt_T_logl           | boolean | 0U  | 1U  |
|                      | FordPullDriftCmpEnad_Cnt_T_logl            | boolean | 0U  | 1U  |
|                      | FordTrlrBackUpAssiEnad_Cnt_T_logl          | boolean | 0U  | 1U  |
|                      | FordEvasSteerAssiEnad_Cnt_T_logl           | boolean | 0U  | 1U  |
|                      | FordCanDtcInhb_Cnt_T_logl                  | boolean | 0U  | 1U  |
|                      | FordClrDiagcFlgProxy_Cnt_T_logl            | boolean | 0U  | 1U  |
|                      | \*MissMsgDiagEna_Cnt_T_logl                | boolean | 0U  | 1U  |
|                      | \* FordVehLatACmpdInvldDiagEna_Cnt_T_logl  | boolean | 0U  | 1U  |
|                      | \*FordVehLgtACmpdInvldDiagEna_Cnt_T_logl   | boolean | 0U  | 1U  |
|                      | \*FordVehSpdOverGndInvldDiagEna_Cnt_T_logl | boolean | 0U  | 1U  |
| **Return Value**     | NA                                         |         |     |     |

## Design Rationale

None

## Processing

Please refer to the below path in the FDD model.

MM124A_FordMsg077BusHiSpd/FordMsg077BusHiSpd/FordMsg077BusHiSpdPer1/DiagEna

##  Local Function \#2

|                      |                                              |        |     |       |
|----------|--------------------------------------|--------|-------|----------|
| **Function Name**    | CalSeln                                      | Type   | Min | Max   |
| **Arguments Passed** | FordEpsLifeCycMod_Cnt_T_u08                  | uint8  | 0U  | 1U    |
|                      | \*BusHiSpdMissThd_MilliSec_T_u16             | uint16 | 0U  | 6000U |
|                      | \*BusHiSpdLatACmpdInvldThd_MilliSec_T_u16    | uint16 | 0U  | 6000U |
|                      | \*BusHiSpdLgtACmpdInvldThd_MilliSec_T_u16    | uint16 | 0U  | 6000U |
|                      | \*BusHiSpdYawRateCmpdInvldThd_MilliSec_T_u16 | uint16 | 0U  | 6000U |
|                      | \*BusHiSpdOverGndInvldThd_MilliSec_T_u16     | uint16 | 0U  | 6000U |
| **Return Value**     | NA                                           |        |     |       |

## Design Rationale

None

## Processing

Please refer to the below path in the FDD model.

MM124A_FordMsg077BusHiSpd/FordMsg077BusHiSpd/FordMsg077BusHiSpdPer1/CalSeln

##  Local Function \#3

|                      |                                    |         |       |          |
|-----------|--------------------------------|---------|----------|-----------|
| **Function Name**    | MissMsg                            | Type    | Min   | Max      |
| **Arguments Passed** | MissMsgDiagEna_Cnt_T_logl          | boolean | 0U    | 1U       |
|                      | BusHiSpdMissTiThd_MilliSec_T_u16   | uint16  | 0U    | 6000U    |
|                      | \*FordVehLatACmpdRaw_Cnt_T_u16     | uint16  | 0U    | 1023U    |
|                      | \*FordVehLatACmpd_Cnt_T_f32        | float32 | -17.9 | 17.835   |
|                      | \*FordVehLatACmpdVld_Cnt_T_logl    | boolean | 0U    | 1U       |
|                      | \*FordVehLgtACmpdRaw_Cnt_T_u16     | uint16  | 0U    | 1023     |
|                      | \*FordVehLgtACmpd_Cnt_T_f32        | float32 | -17.9 | 17.835   |
|                      | \*FordVehLgtACmpdVld_Cnt_T_logl    | boolean | 0U    | 1U       |
|                      | \*FordVehYawRateCmpdRaw_Cnt_T_u16  | uint16  | 0U    | 4095     |
|                      | \*FordVehYawRateCmpd_Cnt_T_f32     | float32 | -75   | 74.92659 |
|                      | \*FordVehYawRateCmpdVld_Cnt_T_logl | boolean | 0U    | 1U       |
|                      | \*FordVehSpdOverGndRaw_Cnt_T_u16   | uint16  | 0U    | 65535    |
|                      | \*FordVehSpdOverGnd_Kph_T_f32      | float32 | 0     | 655.33   |
|                      | \*FordVehSpdOverGndVld_Cnt_T_logl  | boolean | 0U    | 1U       |
| **Return Value**     | NA                                 |         |       |          |

## Design Rationale

None

## Processing

Please refer to the below path in the FDD model.

MM124A_FordMsg077BusHiSpd/FordMsg077BusHiSpd/FordMsg077BusHiSpdPer1/MissingMsgDetermination

## Local Function \#4

|                      |                                    |                         |       |          |
|---------|-----------------------------|-------------------|-------|---------|
| **Function Name**    | OutProcg                           | Type                    | Min   | Max      |
| **Arguments Passed** | Ford_VehLatComp_A_Actl_Cnt_T_enum  | Ford_VehLatComp_A_Actl  | 0U    | 1023U    |
|                      | Ford_VehLongComp_A_Actl_Cnt_T_enum | Ford_VehLongComp_A_Actl | 0U    | 1023U    |
|                      | Ford_VehYawComp_W_Actl_Cnt_T_enum  | Ford_VehYawComp_W_Actl  | 0U    | 4095U    |
|                      | Ford_VehOverGnd_V_Est_Cnt_T_enum   | Ford_VehOverGnd_V_Est   | 0U    | 65535U   |
|                      | \*FordVehLatACmpdRaw_Cnt_T_u16     | uint16                  | 0U    | 1023U    |
|                      | \*FordVehLatACmpd_Cnt_T_f32        | float32                 | -17.9 | 17.835   |
|                      | \*FordVehLatACmpdVld_Cnt_T_logl    | boolean                 | 0U    | 1U       |
|                      | \*FordVehLgtACmpdRaw_Cnt_T_u16     | uint16                  | 0U    | 1023U    |
|                      | \*FordVehLgtACmpd_Cnt_T_f32        | float32                 | -17.9 | 17.835   |
|                      | \*FordVehLgtACmpdVld_Cnt_T_logl    | boolean                 | 0U    | 1U       |
|                      | \*FordVehYawRateCmpdRaw_Cnt_T_u16  | uint16                  | 0U    | 4095U    |
|                      | \*FordVehYawRateCmpd_Cnt_T_f32     | float32                 | -75   | 74.92659 |
|                      | \*FordVehYawRateCmpdVld_Cnt_T_logl | boolean                 | 0U    | 1U       |
|                      | \*FordVehSpdOverGndRaw_Cnt_T_u16   | uint16                  | 0U    | 65535U   |
|                      | \*FordVehSpdOverGnd_Kph_T_f32      | float32                 | 0     | 655.35   |
|                      | \*FordVehSpdOverGndVld_Cnt_T_logl  | boolean                 | 0U    | 1U       |
|                      | \*FordVehLatACmpdVldInp_Cnt_T_logl | boolean                 | 0U    | 1U       |
|                      | \*FordVehLgtACmpdInp_Cnt_T_logl    | boolean                 | 0U    | 1U       |
|                      | \*FordVehYawRateCmpdInp_Cnt_T_logl | boolean                 | 0U    | 1U       |
|                      | \*FordVehSpdOverGndInp_Cnt_T_logl  | boolean                 | 0U    | 1U       |
| **Return Value**     | NA                                 |                         |       |          |

## Design Rationale

None

## Processing

Please refer to the below path in the FDD model.

MM124A_FordMsg077BusHiSpd/FordMsg077BusHiSpd/FordMsg077BusHiSpdPer1/MsgProcessing/OutputProcessing

## Local Function \#5

|                      |                                       |         |     |     |
|------------|-------------------------------|---------|-----------|-----------|
| **Function Name**    | VldElpdTi                             | Type    | Min | Max |
| **Arguments Passed** | \*VehLatVldElpdTi_Cnt_T_logl          | boolean | 0U  | 1U  |
|                      | \*VehLatInvldElpdTi_Cnt_T_logl        | boolean | 0U  | 1U  |
|                      | \*VehLgtVldElpdTi_Cnt_T_logl          | boolean | 0U  | 1U  |
|                      | \*VehLgtInvldElpdTi_Cnt_T_logl        | boolean | 0U  | 1U  |
|                      | \*VehYawRateVldElpdTi_Cnt_T_logl      | boolean | 0U  | 1U  |
|                      | \*VehYawRateInvldElpdTi_Cnt_T_logl    | boolean | 0U  | 1U  |
|                      | \*VehSpdOverGndVldElpdTi_Cnt_T_logl   | boolean | 0U  | 1U  |
|                      | \*VehSpdOverGndInvldElpdTi_Cnt_T_logl | boolean | 0U  | 1U  |
| **Return Value**     | NA                                    |         |     |     |

## Design Rationale

None

## Processing

Please refer to the below path in the FDD model.

MM124A_FordMsg077BusHiSpd/FordMsg077BusHiSpd/FordMsg077BusHiSpdPer1/MsgProcessing/OutputProcessing/VldElpdTi

## Local Function \#6

|                      |                                |         |     |     |
|----------------------|--------------------------------|---------|-----|-----|
| **Function Name**    | VehLatVldElpdTi                | Type    | Min | Max |
| **Arguments Passed** | \*VehLatVldElpdTi_Cnt_T_logl   | boolean | 0U  | 1U  |
|                      | \*VehLatInvldElpdTi_Cnt_T_logl | boolean | 0U  | 1U  |
| **Return Value**     | NA                             |         |     |     |

## Design Rationale

None

## Processing

Please refer to the below path in the FDD model.

MM124A_FordMsg077BusHiSpd/FordMsg077BusHiSpd/FordMsg077BusHiSpdPer1/MsgProcessing/OutputProcessing/VldElpdTi

## Local Function \#7

|                      |                                |         |     |     |
|----------------------|--------------------------------|---------|-----|-----|
| **Function Name**    | VehLgtVldElpdTi                | Type    | Min | Max |
| **Arguments Passed** | \*VehLgtVldElpdTi_Cnt_T_logl   | boolean | 0U  | 1U  |
|                      | \*VehLgtInvldElpdTi_Cnt_T_logl | boolean | 0U  | 1U  |
| **Return Value**     | NA                             |         |     |     |

## Design Rationale

None

## Processing

Please refer to the below path in the FDD model.

MM124A_FordMsg077BusHiSpd/FordMsg077BusHiSpd/FordMsg077BusHiSpdPer1/MsgProcessing/OutputProcessing/VldElpdTi

## Local Function \#8

|                      |                                    |         |     |     |
|------------|-------------------------------|---------|-----------|-----------|
| **Function Name**    | VehYawRateVldElpdTi                | Type    | Min | Max |
| **Arguments Passed** | \*VehYawRateVldElpdTi_Cnt_T_logl   | boolean | 0U  | 1U  |
|                      | \*VehYawRateInvldElpdTi_Cnt_T_logl | boolean | 0U  | 1U  |
| **Return Value**     | NA                                 |         |     |     |

## Design Rationale

None

## Processing

Please refer to the below path in the FDD model.

MM124A_FordMsg077BusHiSpd/FordMsg077BusHiSpd/FordMsg077BusHiSpdPer1/MsgProcessing/OutputProcessing/VldElpdTi

## Local Function \#9

|                      |                                       |         |     |     |
|------------|-------------------------------|---------|-----------|-----------|
| **Function Name**    | VehSpdOverGndVldElpdTi                | Type    | Min | Max |
| **Arguments Passed** | \*VehSpdOverGndVldElpdTi_Cnt_T_logl   | boolean | 0U  | 1U  |
|                      | \*VehSpdOverGndInvldElpdTi_Cnt_T_logl | boolean | 0U  | 1U  |
| **Return Value**     | NA                                    |         |     |     |

## Design Rationale

None

## Processing

Please refer to the below path in the FDD model.

MM124A_FordMsg077BusHiSpd/FordMsg077BusHiSpd/FordMsg077BusHiSpdPer1/MsgProcessing/OutputProcessing/VldElpdTi

##  Local Function \#10

|                      |                                  |         |     |     |
|----------------------|----------------------------------|---------|-----|-----|
| **Function Name**    | VehLatAVld                       | Type    | Min | Max |
| **Arguments Passed** | FordVehLatACmpdVldInp_Cnt_T_logl | boolean | 0U  | 1U  |
|                      | VehLatVldElpdTi_Cnt_T_logl       | boolean | 0U  | 1U  |
|                      | VehLatInvldElpdTi_Cnt_T_logl     | boolean | 0U  | 1U  |
|                      | \*FordVehLatACmpdVld_Cnt_T_logl  | boolean | 0U  | 1U  |
| **Return Value**     | NA                               |         |     |     |

## Design Rationale

None

## Processing

Please refer to the below path in the FDD model.

MM124A_FordMsg077BusHiSpd/FordMsg077BusHiSpd/FordMsg077BusHiSpdPer1/MsgProcessing/OutputProcessing/ChkElpdTi

## Local Function \#11

|                      |                                 |         |     |     |
|----------------------|---------------------------------|---------|-----|-----|
| **Function Name**    | VehLgtAVld                      | Type    | Min | Max |
| **Arguments Passed** | FordVehLgtACmpdInp_Cnt_T_logl   | boolean | 0U  | 1U  |
|                      | VehLgtVldElpdTi_Cnt_T_logl      | boolean | 0U  | 1U  |
|                      | VehLgtInvldElpdTi_Cnt_T_logl    | boolean | 0U  | 1U  |
|                      | \*FordVehLgtACmpdVld_Cnt_T_logl | boolean | 0U  | 1U  |
| **Return Value**     | NA                              |         |     |     |

## Design Rationale

None

## Processing

Please refer to the below path in the FDD model.

MM124A_FordMsg077BusHiSpd/FordMsg077BusHiSpd/FordMsg077BusHiSpdPer1/MsgProcessing/OutputProcessing/ChkElpdTi

## Local Function \#12

|                      |                                    |         |     |     |
|------------|---------------------------------|---------|----------|----------|
| **Function Name**    | VehYawRateVld                      | Type    | Min | Max |
| **Arguments Passed** | FordVehYawRateCmpdInp_Cnt_T_logl   | boolean | 0U  | 1U  |
|                      | VehYawRateVldElpdTi_Cnt_T_logl     | boolean | 0U  | 1U  |
|                      | VehYawRateInvldElpdTi_Cnt_T_logl   | boolean | 0U  | 1U  |
|                      | \*FordVehYawRateCmpdVld_Cnt_T_logl | boolean | 0U  | 1U  |
| **Return Value**     | NA                                 |         |     |     |

## Design Rationale

None

## Processing

Please refer to the below path in the FDD model.

MM124A_FordMsg077BusHiSpd/FordMsg077BusHiSpd/FordMsg077BusHiSpdPer1/MsgProcessing/OutputProcessing/ChkElpdTi

## Local Function \#13

|                      |                                     |         |     |     |
|------------|---------------------------------|---------|----------|----------|
| **Function Name**    | VehSpdOverGndVld                    | Type    | Min | Max |
| **Arguments Passed** | FordVehSpdOverGndInp_Cnt_T_logl     | boolean | 0U  | 1U  |
|                      | VehSpdOverGndVldElpdTi_Cnt_T_logl   | boolean | 0U  | 1U  |
|                      | VehSpdOverGndInvldElpdTi_Cnt_T_logl | boolean | 0U  | 1U  |
|                      | \*FordVehSpdOverGndVld_Cnt_T_logl   | boolean | 0U  | 1U  |
| **Return Value**     | NA                                  |         |     |     |

## Design Rationale

None

## Processing

Please refer to the below path in the FDD model.

MM124A_FordMsg077BusHiSpd/FordMsg077BusHiSpd/FordMsg077BusHiSpdPer1/MsgProcessing/OutputProcessing/ChkElpdTi

## Local Function \#14

|                      |                                       |         |     |        |
|------------|---------------------------------|---------|----------|----------|
| **Function Name**    | MissMsgNtcPass                        | Type    | Min | Max    |
| **Arguments Passed** | MissMsgDiagEna_Cnt_T_logl             | boolean | 0U  | 1U     |
|                      | FordVehYawRateCmpdInp_Cnt_T_logl      | boolean | 0U  | 1U     |
|                      | BusHiSpdYawRateCmpdInvldThd_Cnt_T_u16 | uint16  | 0U  | 65535U |
|                      | FordEvasSteerAssiEnad_Cnt_T_logl      | boolean | 0U  | 1U     |
| **Return Value**     | NA                                    |         |     |        |

## Design Rationale

None

## Processing

Please refer to the below path in the FDD model.

MM124A_FordMsg077BusHiSpd/FordMsg077BusHiSpd/FordMsg077BusHiSpdPer1/MsgProcessing/MissMsgNtcPass

## Local Function \#15

|                      |                                        |         |     |        |
|------------|---------------------------------|---------|----------|----------|
| **Function Name**    | FordVehLgtACmpdInvldNtc                | Type    | Min | Max    |
| **Arguments Passed** | FordVehLgtACmpdInvldDiagEna_Cnt_T_logl | boolean | 0U  | 1U     |
|                      | FordVehLgtACmpdInp_Cnt_T_logl          | boolean | 0U  | 1U     |
|                      | BusHiSpdLgtACmpdInvldThd_Cnt_T_u16     | uint16  | 0U  | 65535U |
| **Return Value**     | NA                                     |         |     |        |

## Design Rationale

None

## Processing

Please refer to the below path in the FDD model.

MM124A_FordMsg077BusHiSpd/FordMsg077BusHiSpd/FordMsg077BusHiSpdPer1/MsgProcessing/FordVehLgtACmpdInvldNtc

## Local Function \#16

|                      |                                        |         |     |        |
|------------|---------------------------------|---------|----------|----------|
| **Function Name**    | FordVehLatACmpdInvldDiagEnaPass        | Type    | Min | Max    |
| **Arguments Passed** | FordVehLatACmpdInvldDiagEna_Cnt_T_logl | boolean | 0U  | 1U     |
|                      | FordVehLatACmpdVldInp_Cnt_T_logl       | boolean | 0U  | 1U     |
|                      | BusHiSpdLatACmpdInvldThd_Cnt_T_u16     | uint16  | 0U  | 65535U |
| **Return Value**     | NA                                     |         |     |        |

## Design Rationale

None

## Processing

Please refer to the below path in the FDD model.

MM124A_FordMsg077BusHiSpd/FordMsg077BusHiSpd/FordMsg077BusHiSpdPer1/MsgProcessing/FordVehLatACmpdInvldDiagEnaPass

## Local Function \#17

|                      |                                          |         |     |        |
|------------|---------------------------------|---------|----------|----------|
| **Function Name**    | FordVehSpdOverGndInvldNtc                | Type    | Min | Max    |
| **Arguments Passed** | FordVehSpdOverGndInvldDiagEna_Cnt_T_logl | boolean | 0U  | 1U     |
|                      | BusHiSpdOverGndInvldThd_Cnt_T_u16        | uint16  | 0U  | 65535U |
|                      | FordVehSpdOverGndInp_Cnt_T_logl          | boolean | 0U  | 1U     |
| **Return Value**     | NA                                       |         |     |        |

## Design Rationale

None

## Processing

Please refer to the below path in the FDD model.

MM124A_FordMsg077BusHiSpd/FordMsg077BusHiSpd/FordMsg077BusHiSpdPer1/MsgProcessing/FordVehSpdOverGndInvldNtc

## Local Function \#18

|                      |                 |         |     |     |
|----------------------|-----------------|---------|-----|-----|
| **Function Name**    | IsFeatActv      | Type    | Min | Max |
| **Arguments Passed** | Enad_Cnt_T_logl | boolean | 0U  | 1U  |
| **Return Value**     | NA              |         |     |     |

## Design Rationale

None

## Processing

Please refer to the below path in the FDD model.

MM124A_FordMsg077BusHiSpd/FordMsg077BusHiSpd/FordMsg077BusHiSpdPer1/DiagEna

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