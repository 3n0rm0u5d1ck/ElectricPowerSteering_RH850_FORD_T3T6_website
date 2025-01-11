---
layout: default
title: FordMsg3D3BusHiSpd_MDD
nav_order: 2
parent: Component Implementation
---
{% raw %}
**Module Design Document**

**For**

**FordMsg3D3BusHiSpd**

**April 20, 2018**

**Prepared For:**

**Software Engineering**

**Nexteer Automotive,**

**Saginaw, MI, USA**

**Prepared By:**

**TATA ELXSI,**

**INDIA**

**  
<u>Change History</u>**

|                 |            |             |             |
|-----------------|------------|-------------|-------------|
| **Description** | **Author** | **Version** | **Date**    |
| Initial version | TATA ELXSI | 1           | 20-Apr-2018 |

**  
**

<span id="_Toc512268264" class="anchor"></span><u>Table of Contents</u>

[Table of Contents [3](#_Toc512268264)](#_Toc512268264)

[1 Introduction [5](#introduction)](#introduction)

[1.1 Purpose [5](#purpose)](#purpose)

[1.2 Scope [5](#scope)](#scope)

[2 FordMsg3D3BusHiSpd & High-Level Description
[6](#fordmsg3d3bushispd-high-level-description)](#fordmsg3d3bushispd-high-level-description)

[3 Design details of software module
[7](#design-details-of-software-module)](#design-details-of-software-module)

[3.1 Graphical representation of FordMsg3D3BusHiSpd
[7](#graphical-representation-of-fordmsg3d3bushispd)](#graphical-representation-of-fordmsg3d3bushispd)

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

[5.1.1 Init: FordMsg3D3BusHiSpdInit1
[9](#init-fordmsg3d3bushispdinit1)](#init-fordmsg3d3bushispdinit1)

[5.1.2 Per: FordMsg3D3BusHiSpdPer1
[9](#per-fordmsg3d3bushispdper1)](#per-fordmsg3d3bushispdper1)

[5.2 Server Runables [9](#server-runables)](#server-runables)

[5.3 Interrupt Functions
[9](#interrupt-functions)](#interrupt-functions)

[5.4 Module Internal (Local) Functions
[10](#module-internal-local-functions)](#module-internal-local-functions)

[5.4.1 Local Function \#1 [10](#local-function-1)](#local-function-1)

[5.4.1.1 Design Rationale
[10](#design-rationale-2)](#design-rationale-2)

[5.4.1.2 Processing [10](#processing)](#processing)

[5.4.2 Local Function \#2 [10](#local-function-2)](#local-function-2)

[5.4.2.1 Design Rationale
[11](#design-rationale-3)](#design-rationale-3)

[5.4.2.2 Processing [11](#processing-1)](#processing-1)

[5.4.3 Local Function \#3 [11](#local-function-3)](#local-function-3)

[5.4.3.1 Design Rationale
[11](#design-rationale-4)](#design-rationale-4)

[5.4.3.2 Processing [11](#processing-2)](#processing-2)

[5.4.4 Local Function \#4 [11](#local-function-4)](#local-function-4)

[5.4.4.1 Design Rationale
[12](#design-rationale-5)](#design-rationale-5)

[5.4.4.2 Processing [12](#processing-3)](#processing-3)

[5.4.5 Local Function \#5 [13](#local-function-5)](#local-function-5)

[5.4.5.1 Design Rationale
[13](#design-rationale-6)](#design-rationale-6)

[5.4.5.2 Processing [13](#processing-4)](#processing-4)

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

## Purpose

Module Design Document for MM074A_FordMsg3D3BusHiSpd_Impl.

## Scope

The following definitions are used throughout this document:

-   **<u>Shall</u>**: indicates a mandatory requirement without
    exception in compliance.

-   **<u>Should</u>**: indicates a mandatory requirement; exceptions
    allowed only with documented justification.

-   **<u>May</u>**: indicates an optional action.

# FordMsg3D3BusHiSpd & High-Level Description

The purpose of the Ford Message 3D3 Bus High Speed function is to
provide the Electric Power Steering system with signal values for the
Traffic Jam Assist and Lane Center Assist functions from CAN. The Ford
Message 3D3 function will perform the missing message as well as provide
a validity flag for the signal values and received message.

# Design details of software module

## Graphical representation of FordMsg3D3BusHiSpd

<img
src="ElectricPowerSteering_RH850_FORD_T3T6_website/docs/MM074A_FordMsg3D3BusHiSpd_Impl/doc/mediax/media/image1.png"
style="width:3.06335in;height:4.02375in" />

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

### Init: FordMsg3D3BusHiSpdInit1

#### Design Rationale

Refer FDD

#### Module Outputs

Refer FDD

### Per: FordMsg3D3BusHiSpdPer1

#### Design Rationale

Refer FDD

#### Store Module Inputs to Local copies

Refer FDD

#### (Processing of function)………

Refer FDD

#### Store Local copy of outputs into Module Outputs

Refer FDD

## Server Runables

None

## Interrupt Functions

None

## Module Internal (Local) Functions

## Local Function \#1

| **Function Name** | DiagEna                           | Type    | Min | Max  |
|-------------------|-----------------------------------|---------|-----|------|
| Arguments Passed  | FordTrlrBackupAssiEnad_Cnt_T_logl | boolean | 0U  | 1U   |
|                   | FordCanDtcInhb_Cnt_T_logl         | boolean | 0U  | 1U   |
|                   | ClrDiagcFlgProxy_Cnt_T_u08        | uintt8  | 0U  | 255U |
|                   | \*MissMsgDiagEna_Cnt_T_logl       | boolean | 0U  | 1U   |
|                   | \*ClrDiagcFlgProxyEna_Cnt_logl    | boolean | 0U  | 1U   |
| Return Value      |                                   |         |     |      |

## Design Rationale

## Processing

Please refer to the below path in the FDD model.

MM074A_FordMsg3D3BusHiSpd/FordMsg3D3BusHiSpd/FordMsg3D3BusHiSpdPer1

## Local Function \#2

| **Function Name** | MissMsg                                            | Type    | Min        | Max         |
|---------|------------------------------------|--------|---------|-----------|
| Arguments Passed  | FordEpsLifeCycMod_Cnt_T_u08                        | uint8   | 0U         | 255U        |
|                   | MissMsgDiagEna_Cnt_T_logl                          | boolean | 0U         | 1U          |
|                   | ClrDiagcFlgProxyEna_Cnt_logl                       | boolean | 0U         | 1U          |
|                   | \*FordVehLatCtrlRampTyp_Cnt_T_enum                 | Float32 | -.02F      | 0.02094F    |
|                   | \*FordVehLatCtrlPrcsn_Cnt_T_enum                   | Enum    | 0U         | 3U          |
|                   | \*FordVehLatCtrlCrvt_IvsMtr_T_f32                  | Float32 | -.02F      | 0.02094F    |
|                   | \*FordVehLatCtrlCrvtRaw_Cnt_T_u16                  | uint16  | 0U         | 65535U      |
|                   | \*FordVehLatCtrlPah_Rad_T_f32                      | Float32 | -0.5F      | 0.5235F     |
|                   | \*FordVehLatCtrlPahRaw_Cnt_T_u16                   | uint16  | 0U         | 65535U      |
|                   | \*FordVehLatCtrlPahOffs_Mtr_T_f32                  | Float32 | -5.12F     | 5.11F       |
|                   | \*FordVehLatCtrlPahOffsRaw_Cnt_T_u16               | uint16  | 0U         | 65535U      |
|                   | \*FordVehLatCtrlCrvtRate_IvsMtr_T_f32              | Float32 | -0.001024F | 0.00102375F |
|                   | \*FordVehLatCtrlCrvtRateRaw_Cnt_T_u16              | uint16  | 0U         | 65535U      |
|                   | \*FordVehLatCtrlReq_Cnt_T_enum                     | Enum    | 0U         | 7U          |
|                   | \*FordVehLatCtrlRingMax_Cnt_T_u08                  | uint8   | 0U         | 255U        |
|                   | \*FordVehLatCtrlHandsOffDetnTqStimlsReq_Cnt_T_enum | Enum    | 0U         | 1U          |
|                   | \*FordVehLatCtrlImgProcrModlAVld_Cnt_T_u16         | uint16  | 0U         | 65535U      |
| Return Value      |                                                    |         |            |             |

## Design Rationale

## Processing

Please refer to the below path in the FDD model.

MM074A_FordMsg3D3BusHiSpd/FordMsg3D3BusHiSpd/FordMsg3D3BusHiSpdPer1

## Local Function \#3

| **Function Name** | FordMsg3D3MissMsgFail        | Type    | Min | Max   |
|-------------------|------------------------------|---------|-----|-------|
| Arguments Passed  | BusHiSpdMissThd_Cnt_T_u16    | uint16  | 0   | 65535 |
|                   | MissMsgDiagEna_Cnt_T_logl    | boolean | 0U  | 1U    |
|                   | ClrDiagcFlgProxyEna_Cnt_logl | boolean | 0U  | 1U    |
| Return Value      |                              |         |     |       |

## Design Rationale

## Processing

Please refer to the below path in the FDD model.

MM074A_FordMsg3D3BusHiSpd/FordMsg3D3BusHiSpd/FordMsg3D3BusHiSpdPer1/FordMsg3D3MsgMiss

## Local Function \#4

| **Function Name** | MsgPrsnt                                           | Type    | Min        | Max         |
|---------|------------------------------------|--------|---------|-----------|
| Arguments Passed  | Ford_LatCtlRampType_D_Rq_Cnt_enum                  | Enum    | 0U         | 3U          |
|                   | Ford_LatCtlPrecision_D_Rq_Cnt_enum                 | Enum    | 0U         | 3U          |
|                   | Ford_LatCtlCurv_No_Actl_Cnt_T_u16                  | uint16  | 0U         | 65535U      |
|                   | Ford_LatCtlPath_An_Actl_Cnt_T_u16                  | uint16  | 0U         | 65535U      |
|                   | Ford_LatCtlPathOffst_L_Actl_Cnt_T_u16              | uint16  | 0U         | 65535U      |
|                   | Ford_LatCtlCurv_NoRate_Actl_Cnt_T_u16              | uint16  | 0U         | 65535U      |
|                   | Ford_LatCtl_D_Rq_Cnt_T_enum                        | Enum    | 0U         | 7U          |
|                   | Ford_LatCtlRng_L_Max_Cnt_T_u08                     | uint8   | 0U         | 255U        |
|                   | Ford_HandsOffCnfm_B_Rq_Cnt_T_enum                  | Enum    | 0U         | 1U          |
|                   | FordEpsLifeCycMod_Cnt_T_u08                        | uint8   | 0U         | 255U        |
|                   | MissMsgDiagEna_Cnt_T_logl                          | boolean | 0U         | 1U          |
|                   | ClrDiagcFlgProxyEna_Cnt_logl                       | boolean | 0U         | 1U          |
|                   | \*FordVehLatCtrlRampTyp_Cnt_T_enum                 | Float32 | -.02F      | 0.02094F    |
|                   | \*FordVehLatCtrlPrcsn_Cnt_T_enum                   | Enum    | 0U         | 3U          |
|                   | \*FordVehLatCtrlCrvt_IvsMtr_T_f32                  | Float32 | -.02F      | 0.02094F    |
|                   | \*FordVehLatCtrlCrvtRaw_Cnt_T_u16                  | uint16  | 0U         | 65535U      |
|                   | \*FordVehLatCtrlPah_Rad_T_f32                      | Float32 | -0.5F      | 0.5235F     |
|                   | \*FordVehLatCtrlPahRaw_Cnt_T_u16                   | uint16  | 0U         | 65535       |
|                   | \*FordVehLatCtrlPahOffs_Mtr_T_f32                  | Float32 | -5.12F     | 5.11F       |
|                   | \*FordVehLatCtrlPahOffsRaw_Cnt_T_u16               | uint16  | 0U         | 65535U      |
|                   | \*FordVehLatCtrlCrvtRate_IvsMtr_T_f32              | Float32 | -0.001024F | 0.00102375F |
|                   | \*FordVehLatCtrlCrvtRateRaw_Cnt_T_u16              | uint16  | 0U         | 65535U      |
|                   | \*FordVehLatCtrlReq_Cnt_T_enum                     | Enum    | 0U         | 7U          |
|                   | \*FordVehLatCtrlRingMax_Cnt_T_u08                  | uint8   | 0U         | 255U        |
|                   | \*FordVehLatCtrlHandsOffDetnTqStimlsReq_Cnt_T_enum | Enum    | 0U         | 1U          |
|                   | \*FordVehLatCtrlImgProcrModlAVld_Cnt_T_u16         | uint16  | 0U         | 65535U      |
| Return Value      |                                                    |         |            |             |

## Design Rationale

## Processing

Please refer to the below path in the FDD model.

MM074A_FordMsg3D3BusHiSpd/FordMsg3D3BusHiSpd/FordMsg3D3BusHiSpdPer1

## Local Function \#5

| **Function Name** | FordMsg3D3MissMsgPass        | Type    | Min | Max |
|-------------------|------------------------------|---------|-----|-----|
| Arguments Passed  | MissMsgDiagEna_Cnt_T_logl    | boolean | 0U  | 1U  |
|                   | ClrDiagcFlgProxyEna_Cnt_logl | boolean | 0U  | 1U  |
| Return Value      |                              |         |     |     |

## Design Rationale

## Processing

Please refer to the below path in the FDD model.

MM074A_FordMsg3D3BusHiSpd/FordMsg3D3BusHiSpd/FordMsg3D3BusHiSpdPer1/FordMsg3D3MsgMiss

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

| **Ref. \#** | **Title**                                                                                                                                                                                                                             | **Version**                     |
|-------|-------------------------------------------------|-----------------|
| 1           | AUTOSAR Specification of Memory Mapping (Link:[AUTOSAR_SWS_MemoryMapping.pdf](https://www.autosar.org/fileadmin/files/standards/classic/4-0/software-architecture/implementation-integration/standard/AUTOSAR_SWS_MemoryMapping.pdf)) | v1.4.0 R4.0 Rev 3               |
| 2           | MDD Guideline EA4                                                                                                                                                                                                                     | 1.02                            |
| 3           | EA4 Software Naming Conventions                                                                                                                                                                                                       | 1.0.3 draft                     |
| 4           | Software Design and Coding Standards                                                                                                                                                                                                  | 3.0 draft                       |
| 5           | MM074A_FordMsg3D3BusHiSpd_Design                                                                                                                                                                                                      | See Synergy Sub Project Version |

{% endraw %}