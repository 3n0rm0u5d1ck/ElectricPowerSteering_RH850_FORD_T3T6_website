---
layout: default
title: FordMsg213BusHiSpd_MDD
nav_order: 2
parent: Component Implementation
---
{% raw %}
**Module Design Document**

**For**

**FordMsg213BusHiSpd**

**17-Apr-2018**

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
| 1           | Initial version | TATA ELXSI | 1           | 17-Apr-2018 |

**  
**

<span id="_Toc512327695" class="anchor"></span><u>Table of Contents</u>

[Table of Contents [3](#_Toc512327695)](#_Toc512327695)

[1 Introduction [5](#introduction)](#introduction)

[1.1 Purpose [5](#purpose)](#purpose)

[1.2 Scope [5](#scope)](#scope)

[2 FordMsg213BusHiSpd & High-Level Description
[6](#fordmsg213bushispd-high-level-description)](#fordmsg213bushispd-high-level-description)

[3 Design details of software module
[7](#design-details-of-software-module)](#design-details-of-software-module)

[3.1 Graphical representation of FordMsg213BusHiSpd
[7](#graphical-representation-of-fordmsg213bushispd)](#graphical-representation-of-fordmsg213bushispd)

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

[5.1.1 Init: FordMsg213BusHiSpdInit1
[9](#init-fordmsg213bushispdinit1)](#init-fordmsg213bushispdinit1)

[5.1.2 Per: FordMsg213BusHiSpdPer1
[9](#per-fordmsg213bushispdper1)](#per-fordmsg213bushispdper1)

[5.2 Server Runnables [9](#server-runnables)](#server-runnables)

[5.2.1 ComIPduCallout_DesiredTorqBrk_FD1
[9](#comipducallout_desiredtorqbrk_fd1)](#comipducallout_desiredtorqbrk_fd1)

[5.2.1.1 Design Rationale [9](#design-rationale-2)](#design-rationale-2)

[5.2.1.2 Processing of function
[9](#processing-of-function-1)](#processing-of-function-1)

[5.2.2 ComTimeoutNotification_CmbbDeny_B_ActlBrk
[9](#comtimeoutnotification_cmbbdeny_b_actlbrk)](#comtimeoutnotification_cmbbdeny_b_actlbrk)

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
[10](#design-rationale-5)](#design-rationale-5)

[5.4.2.2 Processing [11](#processing-1)](#processing-1)

[5.4.3 Local Function \#3 [11](#local-function-3)](#local-function-3)

[5.4.3.1 Design Rationale
[11](#design-rationale-6)](#design-rationale-6)

[5.4.3.2 Processing [11](#processing-2)](#processing-2)

[5.4.4 Local Function \#4 [11](#local-function-4)](#local-function-4)

[5.4.4.1 Design Rationale
[11](#design-rationale-7)](#design-rationale-7)

[5.4.4.2 Processing [11](#processing-3)](#processing-3)

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

Module Design Document for MM063A_FordMsg213BusHiSpd_Impl.

## Scope

The following definitions are used throughout this document:

-   **<u>Shall</u>**: indicates a mandatory requirement without
    exception in compliance.

-   **<u>Should</u>**: indicates a mandatory requirement; exceptions
    allowed only with documented justification.

-   **<u>May</u>**: indicates an optional action.

# FordMsg213BusHiSpd & High-Level Description

The purpose of the Ford Message 213 Bus High Speed function is to
provide the Electric Power Steering system with signal values for the
Brake Oscillation Reduction, Lane Detection Warning, LKA, Traffic Jam
Assist and Lane Center Assist functions from CAN. The Ford Message 213
function will perform the missing message and signal invalid diagnostics
as well as provide a validity flag for the signal values and received
message.

# Design details of software module

## Graphical representation of FordMsg213BusHiSpd

<img
src="ElectricPowerSteering_RH850_FORD_T3T6_website/docs/MM063A_FordMsg213BusHiSpd_Impl/doc/mediax/media/image1.jpeg"
style="width:5.73958in;height:4.91667in"
alt="C:\Users\guru.s\Desktop\MM063A\MM063A.JPG" />

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

| Constant Name                       | Resolution       | Units          | Value  |
|--------------------------------|--------------|---------------|------------|
| ABSACTVMAX_CNT_U08                  | Single Precision | Cnt            | 1U     |
| ABSACTVMIN_CNT_U08                  | Single Precision | Cnt            | 0U     |
| BUSHISPDFIXDTITHD_MILLISEC_U16      | Single Precision | MilliSec       | 5000U  |
| CLLSNMTGTNBYBRKGDENDMAX_CNT_U08     | Single Precision | Cnt            | 1U     |
| CLLSNMTGTNBYBRKGDENDMIN_CNT_U08     | Single Precision | Cnt            | 0U     |
| CLLSNMTGTNBYBRKGDISADMAX_CNT_U08    | Single Precision | Cnt            | 1U     |
| CLLSNMTGTNBYBRKGDISADMIN_CNT_U08    | Single Precision | Cnt            | 0U     |
| CNVMILLISECTOCNT_CNTPERMILLISEC_U16 | Single Precision | CntPerMilliSec | 10U    |
| DEBSTEP_CNT_U16                     | Single Precision | Cnt            | 65535U |
| ESCACTVMAX_CNT_U08                  | Single Precision | Cnt            | 1U     |
| ESCACTVMIN_CNT_U08                  | Single Precision | Cnt            | 0U     |
| MODSEL_CNT_U08                      | Single Precision | Cnt            | 1U     |

# Software Component Implementation

## Sub-Module Functions

The sub-module functions are grouped based on similar functionality that
needs to be executed in a given “State” of the system (refer States and
Modes). For a given module, the MDD will identify the type and number of
sub-modules required. The sub-module types are described below.

### Init: FordMsg213BusHiSpdInit1

#### Design Rationale

Refer FDD

#### Module Outputs

Refer FDD

### Per: FordMsg213BusHiSpdPer1

#### Design Rationale

Refer FDD

#### Store Module Inputs to Local copies

Refer FDD

#### (Processing of function) ………

Refer FDD

#### Store Local copy of outputs into Module Outputs

Refer FDD

## Server Runnables 

### ComIPduCallout_DesiredTorqBrk_FD1

## 5.2.1.1 Design Rationale [design-rationale-2]

None

## 5.2.1.2 Processing of function [processing-of-function-1]

None

### ComTimeoutNotification_CmbbDeny_B_ActlBrk

## 5.2.2.1 Design Rationale [design-rationale-3]

None

## 5.2.2.2 Processing of function [processing-of-function-2]

None

## Interrupt Functions

None

## Module Internal (Local) Functions

## Local Function \#1

|                      |                                  |         |     |     |
|----------------------|----------------------------------|---------|-----|-----|
| **Function Name**    | NtcEnab                          | Type    | Min | Max |
| **Arguments Passed** | FordEvasSteerAssiEnad_Cnt_T_logl | boolean | 0U  | 1U  |
|                      | FordBrkOscnRednEnad_Cnt_T_logl   | boolean | 0U  | 1U  |
|                      | FordLaneDetnWarnEnad_Cnt_T_logl  | boolean | 0U  | 1U  |
|                      | FordLkaEnad_Cnt_T_logl           | boolean | 0U  | 1U  |
|                      | FordTrfcJamAssiEnad_Cnt_T_logl   | boolean | 0U  | 1U  |
|                      | FordLaneCentrAssiEnad_Cnt_T_logl | boolean | 0U  | 1U  |
|                      | ClrDiagcFlgProxy_Cnt_T_u08       | uint8   | 0U  | 1U  |
|                      | FordCanDtcInhb_Cnt_T_logl        | boolean | 0U  | 1U  |
|                      | \*DiagEna_Cnt_T_logl             | boolean | 0U  | 1U  |
|                      | \*ClrDiagcFlgProxyEna_Cnt_T_logl | boolean | 0U  | 1U  |
| **Return Value**     | NA                               |         |     |     |

## Design Rationale

None

## Processing

Please refer to the below path in the FDD model.

MM063A_FordMsg213BusHiSpd/FordMsg213BusHiSpd/FordMsg213BusHiSpdPer1/NtcEnab

##  Local Function \#2

|                      |                                  |         |     |       |
|-----------|-------------------------------|---------|--------|--------------|
| **Function Name**    | CalSeln                          | Type    | Min | Max   |
| **Arguments Passed** | FordEpsLifeCycMod_Cnt_T_u08      | uint8   | 0U  | 1U    |
|                      | FordEvasSteerAssiEnad_Cnt_T_logl | boolean | 0U  | 1U    |
| **Return Value**     | BusHiSpdMissThd_Cnt_T_u16        | uint16  | 0U  | 6000U |

## Design Rationale

None

## Processing

Please refer to the below path in the FDD model.

MM063A_FordMsg213BusHiSpd/FordMsg213BusHiSpd/FordMsg213BusHiSpdPer1/CalSeln

##  Local Function \#3

|                      |                               |         |     |     |
|----------------------|-------------------------------|---------|-----|-----|
| **Function Name**    | AbsEscStsVldChk               | Type    | Min | Max |
| **Arguments Passed** | NA                            |         |     |     |
| **Return Value**     | AbsEscStsVldElpdTi_Cnt_T_logl | boolean | 0U  | 1U  |

## Design Rationale

None

## Processing

Please refer to the below path in the FDD model.

MM063A_FordMsg213BusHiSpd/FordMsg213BusHiSpd/FordMsg213BusHiSpdPer1/MissingMsgFailed

###  Local Function \#4

|                      |                               |         |     |     |
|----------------------|-------------------------------|---------|-----|-----|
| **Function Name**    | VldElpdTi                     | Type    | Min | Max |
| **Arguments Passed** | NA                            |         |     |     |
| **Return Value**     | AbsEscStsVldElpdTi_Cnt_T_logl | boolean | 0U  | 1U  |

## Design Rationale

None

## Processing

Please refer to the below path in the FDD model.

MM063A_FordMsg213BusHiSpd/FordMsg213BusHiSpd/FordMsg213BusHiSpdPer1/MissingMsgPassed/VldElpdTi

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
| 2       | MDD Guideline                                                                | EA4 01.00                      |
| 3       | Software Naming Conventions.doc                                              | EA4 01.02                      |
| 4       | Software Design and Coding Standards.doc                                     | EA4 2.01                       |
| 5       | FDD: MM063A_FordMsg213BusHiSpd_Design                                        | See Synergy subproject version |

{% endraw %}