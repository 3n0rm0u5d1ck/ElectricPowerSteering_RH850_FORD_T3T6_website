---
layout: default
title: FordMsg083BusHiSpd_MDD
nav_order: 2
parent: Component Implementation
---
{% raw %}
**Module Design Document**

**For**

**FordMsg083BusHiSpd**

**Prepared For:**

**,**

**Prepared By:**

**TATA ELXSI,**

**INDIA**

**<u>Change History</u>**

|                 |            |             |             |
|-----------------|------------|-------------|-------------|
| **Description** | **Author** | **Version** | **Date**    |
| Initial version | TATA ELXSI | 1           | 17-Apr-2018 |

**  
**

<span id="_Toc511984787" class="anchor"></span><u>Table of Contents</u>

[Table of Contents [4](#_Toc511984787)](#_Toc511984787)

[1 Introduction [6](#introduction)](#introduction)

[1.1 Purpose [6](#purpose)](#purpose)

[2 FordMsg083BusHiSpd& High-Level Description
[7](#fordmsg083bushispd-high-level-description)](#fordmsg083bushispd-high-level-description)

[3 Design details of software module
[8](#design-details-of-software-module)](#design-details-of-software-module)

[3.1 Graphical representation of FordMsg083BusHiSpd
[8](#graphical-representation-of-fordmsg083bushispd)](#graphical-representation-of-fordmsg083bushispd)

[3.2 Data Flow Diagram [8](#data-flow-diagram)](#data-flow-diagram)

[3.2.1 Component level DFD
[8](#component-level-dfd)](#component-level-dfd)

[3.2.2 Function level DFD [8](#function-level-dfd)](#function-level-dfd)

[4 Constant Data Dictionary
[9](#constant-data-dictionary)](#constant-data-dictionary)

[4.1 Program (fixed) Constants
[9](#program-fixed-constants)](#program-fixed-constants)

[4.1.1 Embedded Constants [9](#embedded-constants)](#embedded-constants)

[5 Software Component Implementation
[10](#software-component-implementation)](#software-component-implementation)

[5.1 Sub-Module Functions
[10](#sub-module-functions)](#sub-module-functions)

[5.1.1 Init: FordMsg083BusHiSpdInit1
[10](#init-fordmsg083bushispdinit1)](#init-fordmsg083bushispdinit1)

[5.1.2 Per: FordMsg083BusHiSpdPer1
[10](#per-fordmsg083bushispdper1)](#per-fordmsg083bushispdper1)

[5.2 Server Runnables [10](#server-runnables)](#server-runnables)

[5.2.1 ComIPduCallout_Steering_Data_FD1
[10](#comipducallout_steering_data_fd1)](#comipducallout_steering_data_fd1)

[5.2.1.1 Design Rationale
[10](#design-rationale-2)](#design-rationale-2)

[5.2.1.2 Processing of function
[10](#processing-of-function-1)](#processing-of-function-1)

[5.2.2 ComTimeoutNotification_TurnLghtSwtch_D_Stat
[10](#comtimeoutnotification_turnlghtswtch_d_stat)](#comtimeoutnotification_turnlghtswtch_d_stat)

[5.2.2.1 Design Rationale
[10](#design-rationale-3)](#design-rationale-3)

[5.2.2.2 Processing of function
[10](#processing-of-function-2)](#processing-of-function-2)

[5.3 Interrupt Functions
[11](#interrupt-functions)](#interrupt-functions)

[5.4 Module Internal (Local) Functions
[12](#module-internal-local-functions)](#module-internal-local-functions)

[5.4.1 Local Function \#1 [12](#local-function-1)](#local-function-1)

[5.4.1.1 Design Rationale
[12](#design-rationale-4)](#design-rationale-4)

[5.4.1.2 Processing [12](#processing)](#processing)

[5.4.2 Local Function \#2 [12](#local-function-2)](#local-function-2)

[5.4.2.1 Design Rationale
[12](#design-rationale-5)](#design-rationale-5)

[5.4.2.2 Processing [12](#processing-1)](#processing-1)

[5.4.3 Local Function \#3 [12](#local-function-3)](#local-function-3)

[5.4.3.1 Design Rationale
[13](#design-rationale-6)](#design-rationale-6)

[5.4.3.2 Processing [13](#processing-2)](#processing-2)

[5.4.4 Local Function \#4 [13](#local-function-4)](#local-function-4)

[5.4.4.1 Design Rationale
[13](#design-rationale-7)](#design-rationale-7)

[5.4.4.2 Processing [13](#processing-3)](#processing-3)

[5.4.5 Local Function \#5 [13](#local-function-5)](#local-function-5)

[5.4.5.1 Design Rationale
[13](#design-rationale-8)](#design-rationale-8)

[5.4.5.2 Processing [13](#processing-4)](#processing-4)

[5.5 GLOBAL Function/Macro Definitions
[14](#global-functionmacro-definitions)](#global-functionmacro-definitions)

[6 Known Limitations with Design
[15](#known-limitations-with-design)](#known-limitations-with-design)

[7 UNIT TEST CONSIDERATION
[16](#unit-test-consideration)](#unit-test-consideration)

[Appendix A Abbreviations and Acronyms
[17](#_Toc511984830)](#_Toc511984830)

[Appendix B Glossary [18](#glossary)](#glossary)

[Appendix C References [19](#references)](#references)

# Introduction

## Purpose

Module Design Document for MM054A_FordMsg083BusHiSpd_Impl.

# FordMsg083BusHiSpd& High-Level Description

The purpose of the Ford Message 083 Bus High Speed function is to
provide the Electric Power Steering system with signal values for the
Lane Detection Warning function from CAN. The Ford Message 083 function
will perform the missing message diagnostics as well as provide a
validity flag for the signal values and received message. Detailed
requirements have implemented the Ford DBC file for guidance.

# Design details of software module

## Graphical representation of FordMsg083BusHiSpd

<img
src="ElectricPowerSteering_RH850_FORD_T3T6_website/docs/MM054A_FordMsg083BusHiSpd_Impl/doc/mediax/media/image1.png"
style="width:5.72917in;height:3.75in" />

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

| Constant Name                       | Resolution       | Units          | Value |
|------------------------------------------|-----------|--------------|-------|
| BUSHISPDFIXDTITHD_MILLISEC_U16      | Single precision | MilliSec       | 5000  |
| CNVMILLISECTOCNT_CNTPERMILLISEC_U16 | Single precision | CntPerMilliSec | 10    |
| DEBSTEP_CNT_U16                     | Single precision | Cnt            | 65535 |
| MODSEL_CNT_U08                      | Single precision | Cnt            | 1     |

# Software Component Implementation

## Sub-Module Functions

The sub-module functions are grouped based on similar functionality that
needs to be executed in a given “State” of the system (refer States and
Modes). For a given module, the MDD will identify the type and number of
sub-modules required. The sub-module types are described below.

### Init: FordMsg083BusHiSpdInit1

#### Design Rationale

Refer FDD

#### Module Outputs

Refer FDD

### Per: FordMsg083BusHiSpdPer1

#### Design Rationale

Refer FDD

#### Store Module Inputs to Local copies

Refer FDD

#### (Processing of function)

Refer FDD

#### Store Local copy of outputs into Module Outputs

Refer FDD

## Server Runnables

### ComIPduCallout_Steering_Data_FD1

## 5.2.1.1 Design Rationale [design-rationale-2]

None

## 5.2.1.2 Processing of function [processing-of-function-1]

None

### ComTimeoutNotification_TurnLghtSwtch_D_Stat

## 5.2.2.1 Design Rationale [design-rationale-3]

None

## 5.2.2.2 Processing of function [processing-of-function-2]

None

## Interrupt Functions

None

## Module Internal (Local) Functions

## Local Function \#1

| **Function Name** | DiagEna                         | Type    | Min | Max |
|-------------------|---------------------------------|---------|-----|-----|
| Arguments Passed  | FordLaneDetnWarnEnad_Cnt_T_logl | boolean | 0U  | 1U  |
|                   | FordCanDtcInhb_Cnt_T_logl       | boolean | 0U  | 1U  |
|                   | ClrDiagcFlgProxy_Cnt_T_u08      | Uint8   | 0U  | 1U  |
|                   | DiagEna_Cnt_T_logl              | boolean | 0U  | 1U  |
|                   | ClrDiagcFlgProxyEna_Cnt_T_logl  | boolean | 0U  | 1U  |
| Return Value      |                                 |         |     |     |

## Design Rationale

## Processing

Please refer to the below path in the FDD model.

MM054A_FordMsg083BusHiSpd/FordMsg083BusHiSpd/FordMsg083BusHiSpdPer1/DiagEna

## Local Function \#2

| **Function Name** | CalSeln                     | Type   | Min | Max   |
|-------------------|-----------------------------|--------|-----|-------|
| Arguments Passed  | FordEpsLifeCycMod_Cnt_T_u08 | Uint8  | 0U  | 1U    |
| Return Value      | BusHiSpdMissThd_Cnt_T_u16   | Uint16 | 0U  | 6000U |

## Design Rationale

## Processing

Please refer to the below path in the FDD model.

MM054A_FordMsg083BusHiSpd/FordMsg083BusHiSpd/FordMsg083BusHiSpdPer1/CalSeln

## Local Function \#3

| **Function Name** | MsgMiss                            | Type    | Min | Max   |
|-------------------|------------------------------------|---------|-----|-------|
| Arguments Passed  | BusHiSpdMissThd_Cnt_T_u16          | Uint16  | 0U  | 6000U |
|                   | DiagEna_Cnt_T_logl                 | boolean | 0U  | 1U    |
|                   | ClrDiagcFlgProxyEna_Cnt_T_logl     | boolean | 0U  | 1U    |
|                   | FordVehTurnSigVld_Cnt_T_logl       | boolean | 0U  | 1U    |
|                   | FordVehTurnSigSwtStsRaw_Cnt_T_enum | Enum    | 0U  | 3U    |
| Return Value      |                                    |         |     |       |

## Design Rationale

## Processing

Please refer to the below path in the FDD model.

MM054A_FordMsg083BusHiSpd/FordMsg083BusHiSpd/FordMsg083BusHiSpdPer1/FordMsg083MsgMiss

## Local Function \#4

| **Function Name** | MsgPrsnt                       | Type    | Min | Max |
|-------------------|--------------------------------|---------|-----|-----|
| Arguments Passed  | DiagEna_Cnt_T_logl             | boolean | 0U  | 1U  |
|                   | ClrDiagcFlgProxyEna_Cnt_T_logl | boolean | 0U  | 1U  |
| Return Value      |                                |         |     |     |

## Design Rationale

## Processing

Please refer to the below path in the FDD model.

MM054A_FordMsg083BusHiSpd/FordMsg083BusHiSpd/FordMsg083BusHiSpdPer1/FordMsg083MsgPrsnt

## Local Function \#5

| **Function Name** | OutpProcg                             | Type    | Min | Max |
|------------|------------------------------|---------------|--------|---------|
| Arguments Passed  | Ford_TurnLghtSwtch_D_Stat1_Cnt_T_enum | Enum    | 0U  | 3U  |
|                   | FordVehTurnSigVld_Cnt_T_logl          | boolean | 0U  | 1U  |
|                   | FordVehTurnSigSwtStsRaw_Cnt_T_enum    | Enum    | 0U  | 3U  |
| Return Value      |                                       |         |     |     |

## Design Rationale

## Processing

Please refer to the below path in the FDD model.

MM054A_FordMsg083BusHiSpd/FordMsg083BusHiSpd/FordMsg083BusHiSpdPer1/FordMsg083MsgPrsnt/OutputProcessing

## GLOBAL Function/Macro Definitions

None

# Known Limitations with Design

Return type and arguments for Non RTE Srv Runnables do not match with
data dictionary. This is due to the limitations of FDD tools.

# UNIT TEST CONSIDERATION

<span id="_Toc511984830" class="anchor"></span>Return type and arguments
for Non RTE Srv Runnables do not match with data dictionary. This is due
to the limitations of FDD tools.

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
| 5       | MM054A_FordMsg083BusHiSpd_Design                                             | See Synergy subproject version |

{% endraw %}