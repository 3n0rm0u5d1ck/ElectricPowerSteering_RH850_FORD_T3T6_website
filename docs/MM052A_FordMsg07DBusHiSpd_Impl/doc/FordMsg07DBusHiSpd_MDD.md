---
layout: default
title: FordMsg07DBusHiSpd_MDD
nav_order: 2
parent: Component Implementation
---
{% raw %}
**Module Design Document**

**For**

**FordMsg07DBusHiSpd**

**18-Apr-2018**

**Prepared For:**

**Software Engineering**

**Nexteer Automotive,**

**Saginaw, MI, USA**

**Prepared By:**

**TATA ELXSI,**

**INDIA**

**  
<u>Change History</u>**

|             |                 |            |             |             |
|-------------|-----------------|------------|-------------|-------------|
| **Sl. No.** | **Description** | **Author** | **Version** | **Date**    |
| 1           | Initial version | TATA ELXSI | 1.0         | 18-Apr-2018 |

**  
**

<span id="_Toc511898817" class="anchor"></span><u>Table of Contents</u>

[Table of Contents [3](#_Toc511898817)](#_Toc511898817)

[1 Introduction [5](#introduction)](#introduction)

[1.1 Purpose [5](#purpose)](#purpose)

[1.2 Scope [5](#scope)](#scope)

[2 FordMsg07DBusHiSpd & High-Level Description
[6](#fordmsg07dbushispd-high-level-description)](#fordmsg07dbushispd-high-level-description)

[3 Design details of software module
[7](#design-details-of-software-module)](#design-details-of-software-module)

[3.1 Graphical representation of FordMsg07DBusHiSpd
[7](#graphical-representation-of-fordmsg07dbushispd)](#graphical-representation-of-fordmsg07dbushispd)

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

[5.1.1 Init: FordMsg07DBusHiSpdInit1
[9](#init-fordmsg07dbushispdinit1)](#init-fordmsg07dbushispdinit1)

[5.1.2 Per: FordMsg07DBusHiSpdPer1
[9](#per-fordmsg07dbushispdper1)](#per-fordmsg07dbushispdper1)

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

[5.4.5.2 Processing [12](#processing-4)](#processing-4)

[5.4.6 Local Function \#6 [12](#local-function-6)](#local-function-6)

[5.4.6.1 Design Rationale
[12](#design-rationale-9)](#design-rationale-9)

[5.4.6.2 Processing [12](#processing-5)](#processing-5)

[5.4.7 Local Function \#7 [12](#local-function-7)](#local-function-7)

[5.4.7.1 Design Rationale
[12](#design-rationale-10)](#design-rationale-10)

[5.4.7.2 Processing [12](#processing-6)](#processing-6)

[5.4.8 Local Function \#8 [12](#_Toc511898858)](#_Toc511898858)

[5.4.8.1 Design Rationale [13](#_Toc511898859)](#_Toc511898859)

[5.4.8.2 Processing [13](#_Toc511898860)](#_Toc511898860)

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

Module Design Document for MM052A_FordMsg07DBusHiSpd_Impl.

## Scope

The following definitions are used throughout this document:

-   **<u>Shall</u>**: indicates a mandatory requirement without
    exception in compliance.

-   **<u>Should</u>**: indicates a mandatory requirement; exceptions
    allowed only with documented justification.

-   **<u>May</u>**: indicates an optional action.

# FordMsg07DBusHiSpd & High-Level Description

The purpose of the Ford Message 07D Bus High Speed function is to
provide the Electric Power Steering system with signal values for the
Brake Oscillation Reduction and Trailer Back Up Assist function from
CAN. The Ford Message 07D function will perform the missing message
diagnostic, signal invalid diagnostic, and provide a validity flag for
the received message and signal values.

# Design details of software module

## Graphical representation of FordMsg07DBusHiSpd

<img
src="ElectricPowerSteering_RH850_FORD_T3T6_website/docs/MM052A_FordMsg07DBusHiSpd_Impl/doc/mediax/media/image1.jpeg"
style="width:5.4375in;height:4.28125in"
alt="C:\Users\guru.s\AppData\Local\Microsoft\Windows\INetCache\Content.Word\MM052A.JPG" />

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

| Constant Name                       | Resolution | Units | Value |
|-------------------------------------|------------|-------|-------|
| Refer data dictionary for constants |            |       |       |

# Software Component Implementation

## Sub-Module Functions

The sub-module functions are grouped based on similar functionality that
needs to be executed in a given “State” of the system (refer States and
Modes). For a given module, the MDD will identify the type and number of
sub-modules required. The sub-module types are described below.

### Init: FordMsg07DBusHiSpdInit1

#### Design Rationale

Refer FDD

#### Module Outputs

Refer FDD

### Per: FordMsg07DBusHiSpdPer1

#### Design Rationale

Refer FDD

#### Store Module Inputs to Local copies

Refer FDD

#### (Processing of function) ………

Refer FDD

#### Store Local copy of outputs into Module Outputs

Refer FDD

## Server Runnables 

### ComIPduCallout_BrakeSnData_4_FD1

## 5.2.1.1 Design Rationale [design-rationale-2]

None

## 5.2.1.2 Processing of function [processing-of-function-1]

None

###  ComTimeoutNotification_BrkTot_Tq_Actl

## 5.2.2.1 Design Rationale [design-rationale-3]

None

## 5.2.2.2 Processing of function [processing-of-function-2]

None

## Interrupt Functions

None

## Module Internal (Local) Functions

## Local Function \#1

|                      |                                       |         |     |     |
|------------|------------------------------|---------|-----------|-----------|
| **Function Name**    | DiagEna                               | Type    | Min | Max |
| **Arguments Passed** | FordBrkOscnRednEnad_Cnt_T_logl        | boolean | 0U  | 1U  |
|                      | FordTrlrBackUpAssiEnad_Cnt_T_logl     | boolean | 0U  | 1U  |
|                      | FordCanDtcInhb_Cnt_T_logl             | boolean | 0U  | 1U  |
|                      | ClrDiagcFlgProxy_Cnt_T_u08            | uint8   | 0U  | 1U  |
|                      | \*MissMsgDiagEna_Cnt_T_logl           | boolean | 0U  | 1U  |
|                      | \*VertACmpdSigInvldDiagEna_Cnt_T_logl | boolean | 0U  | 1U  |
|                      | \*ClrDiagcFlgProxyEna_Cnt_T_logl      | boolean | 0U  | 1U  |
| **Return Value**     | NA                                    |         |     |     |

## Design Rationale

None

## Processing

Please refer to the below path in the FDD model.

MM052A_FordMsg07DBusHiSpd/FordMsg07DBusHiSpd/FordMsg07DBusHiSpdPer1/DiagEna

##  Local Function \#2

|                      |                                                    |        |     |       |
|----------|------------------------------------|---------|-------|-----------|
| **Function Name**    | CalSeln                                            | Type   | Min | Max   |
| **Arguments Passed** | FordEpsLifeCycMod_Cnt_T_u08                        | uint8  | 0U  | 1U    |
|                      | \*BusHiSpdMissThd_MilliSec_T_u16                   | uint16 | 0U  | 6000U |
|                      | \*VehActlTqBrkBusHiSpdInvldFaildThd_MilliSec_T_u16 | uint16 | 0U  | 6000U |
|                      | \*VertACmpdSigBusHiSpdInvldFaildThd_MilliSec_T_u16 | uint16 | 0U  | 6000U |
| **Return Value**     | NA                                                 |        |     |       |

## Design Rationale

None

## Processing

Please refer to the below path in the FDD model.

MM052A_FordMsg07DBusHiSpd/FordMsg07DBusHiSpd/FordMsg07DBusHiSpdPer1/CalSeln

##  Local Function \#3

|                      |                                |         |     |       |
|----------------------|--------------------------------|---------|-----|-------|
| **Function Name**    | NTCFail                        | Type    | Min | Max   |
| **Arguments Passed** | BusHiSpdMissThd_MilliSec_T_u16 | uint16  | 0U  | 6000U |
|                      | MissMsgDiagEna_Cnt_T_logl      | boolean | 0U  | 1U    |
|                      | ClrDiagcFlgProxyEna_Cnt_T_logl | boolean | 0U  | 1U    |
|                      | \*FordVehBrkTqVld_Cnt_T_logl   | boolean | 0U  | 1U    |
|                      | \*FordVehVertAVld_Cnt_T_logl   | boolean | 0U  | 1U    |
| **Return Value**     | NA                             |         |     |       |

## Design Rationale

None

## Processing

Please refer to the below path in the FDD model.

MM052A_FordMsg07DBusHiSpd/FordMsg07DBusHiSpd/FordMsg07DBusHiSpdPer1/FordMsg07DMsgMiss/NTCFail

###  Local Function \#4

|                      |                                |         |     |       |
|----------------------|--------------------------------|---------|-----|-------|
| **Function Name**    | MissMsgNtcFail                 | Type    | Min | Max   |
| **Arguments Passed** | BusHiSpdMissThd_MilliSec_T_u16 | uint16  | 0U  | 6000U |
|                      | MissMsgDiagEna_Cnt_T_logl      | boolean | 0U  | 1U    |
|                      | ClrDiagcFlgProxyEna_Cnt_T_logl | boolean | 0U  | 1U    |
| **Return Value**     | NA                             |         |     |       |

## Design Rationale

None

## Processing

Please refer to the below path in the FDD model.

MM052A_FordMsg07DBusHiSpd/FordMsg07DBusHiSpd/FordMsg07DBusHiSpdPer1/FordMsg07DMsgMiss/NTCFail/MissMsgNtcFail

## Local Function \#5

|                      |                                    |                         |     |       |
|----------|-----------------------------|--------------------|-------|--------|
| **Function Name**    | OutpProcg                          | Type                    | Min | Max   |
| **Arguments Passed** | Ford_BrkTot_Tq_Actl_Cnt_T_enum     | Ford_BrkTot_Tq_Actl     | 0U  | 8191U |
|                      | Ford_VehVertComp_A_Actl_Cnt_T_enum | Ford_VehVertComp_A_Actl | 0U  | 1023U |
|                      | \*FordVehActBrkTqRaw_Cnt_T_u16     | uint16                  | 0U  | 8191U |
|                      | \*FordVehBrkTqVld_Cnt_T_logl       | boolean                 | 0U  | 1U    |
|                      | \*FordVehVertACmpdRaw_Cnt_T_u16    | uint16                  | 0U  | 1023U |
|                      | \*FordVehVertAVld_Cnt_T_logl       | boolean                 | 0U  | 1U    |
|                      | \*FordVehBrkTqVldInp_Cnt_T_logl    | boolean                 | 0U  | 1U    |
|                      | \*FordVehVertAVldInp_Cnt_T_logl    | boolean                 | 0U  | 1U    |
| **Return Value**     | NA                                 |                         |     |       |

## Design Rationale

None

## Processing

Please refer to the below path in the FDD model.

MM052A_FordMsg07DBusHiSpd/FordMsg07DBusHiSpd/FordMsg07DBusHiSpdPer1/FordMsg07DMsgPrsnt/OutputProcessing

## Local Function \#6

|                      |                                                  |         |     |       |
|-----------|-----------------------------------|--------|----------|---------|
| **Function Name**    | FordVehVertACmpdInvldSts                         | Type    | Min | Max   |
| **Arguments Passed** | VertACmpdSigBusHiSpdInvldFaildThd_MilliSec_T_u16 | uint16  | 0U  | 6000U |
|                      | FordVehVertAVldInp_Cnt_T_logl                    | boolean | 0U  | 1U    |
| **Return Value**     | NA                                               |         |     |       |

## Design Rationale

None

## Processing

Please refer to the below path in the FDD model.

MM052A_FordMsg07DBusHiSpd/FordMsg07DBusHiSpd/FordMsg07DBusHiSpdPer1/FordMsg07DMsgPrsnt/FordVehVertACmpdInvldSts

## Local Function \#7

|                      |                                             |         |     |     |
|------------|-------------------------------|---------|-----------|-----------|
| **Function Name**    | ElpdTi                                      | Type    | Min | Max |
| **Arguments Passed** | \*FordVehBrkTqVldElpdTi_Cnt_T_logl          | boolean | 0U  | 1U  |
|                      | \*FordVehBrkTqInvldElpdTi_Cnt_T_logl        | boolean | 0U  | 1U  |
|                      | \*FordVehVertACmpdSigInvldElpdTi_Cnt_T_logl | boolean | 0U  | 1U  |
|                      | \*FordVehVertACmpdSigVldElpdTi_Cnt_T_logl   | boolean | 0U  | 1U  |
| **Return Value**     | NA                                          |         |     |     |

## Design Rationale

None

## Processing

Please refer to the below path in the FDD model.

MM052A_FordMsg07DBusHiSpd/FordMsg07DBusHiSpd/FordMsg07DBusHiSpdPer1/FordMsg07DMsgPrsnt/OutputProcessing/ElpdTi

## GLOBAL Function/Macro Definitions

None

# Known Limitations with Design

1.  In the design path:
    MM052A_FordMsg07DBusHiSpd/FordMsg07DBusHiSpd/FordMsg07DBusHiSpdPer1/FordMsg07DMsgPrsnt/OutputProcessing/FordVehBrkTqVld
    Processing/SetInvld,

The input signal name to the merge block does not match with its output
signal name.

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
| 5       | FDD: MM052A_FordMsg07DBusHiSpd_Design                                        | See Synergy subproject version |

{% endraw %}