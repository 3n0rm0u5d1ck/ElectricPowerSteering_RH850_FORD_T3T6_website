---
layout: default
title: FordMsg215BusHiSpd_MDD
nav_order: 2
parent: Component Implementation
---
{% raw %}
**Module Design Document**

**For**

**FordMsg215BusHiSpd**

**Prepared For:**

**,**

**Prepared By:**

**TATA ELXSI,**

**INDIA**

**<u>Change History</u>**

|                 |            |             |             |
|-----------------|------------|-------------|-------------|
| **Description** | **Author** | **Version** | **Date**    |
| Initial version | TATA ELXSI | 1           | 03-Apr-2018 |

**  
**

<span id="_Toc510547254" class="anchor"></span><u>Table of Contents</u>

[Table of Contents [3](#_Toc510547254)](#_Toc510547254)

[1 Introduction [4](#introduction)](#introduction)

[1.1 Purpose [4](#purpose)](#purpose)

[1.2 Scope [4](#scope)](#scope)

[2 FordMsg215BusHiSpd & High-Level Description
[5](#fordmsg215bushispd-high-level-description)](#fordmsg215bushispd-high-level-description)

[3 Design details of software module
[6](#design-details-of-software-module)](#design-details-of-software-module)

[3.1 Graphical representation of FordMsg215BusHiSpd
[6](#graphical-representation-of-fordmsg215bushispd)](#graphical-representation-of-fordmsg215bushispd)

[3.2 Data Flow Diagram [6](#data-flow-diagram)](#data-flow-diagram)

[3.2.1 Component level DFD
[6](#component-level-dfd)](#component-level-dfd)

[3.2.2 Function level DFD [6](#function-level-dfd)](#function-level-dfd)

[4 Constant Data Dictionary
[7](#constant-data-dictionary)](#constant-data-dictionary)

[4.1 Program (fixed) Constants
[7](#program-fixed-constants)](#program-fixed-constants)

[4.1.1 Embedded Constants [7](#embedded-constants)](#embedded-constants)

[5 Software Component Implementation
[8](#software-component-implementation)](#software-component-implementation)

[5.1 Sub-Module Functions
[8](#sub-module-functions)](#sub-module-functions)

[5.1.1 Init: FordMsg215BusHiSpdInit1 [8](#init-init1)](#init-init1)

[5.1.2 Per: FordMsg215BusHiSpdPer1 [8](#per-per1)](#per-per1)

[5.2 Server Runables [8](#server-runnables)](#server-runnables)

[5.3 Interrupt Functions
[8](#interrupt-functions)](#interrupt-functions)

[5.4 Module Internal (Local) Functions
[8](#module-internal-local-functions)](#module-internal-local-functions)

[5.5 GLOBAL Function/Macro Definitions
[8](#global-functionmacro-definitions)](#global-functionmacro-definitions)

[6 Known Limitations with Design
[9](#known-limitations-with-design)](#known-limitations-with-design)

[7 UNIT TEST CONSIDERATION
[10](#unit-test-consideration)](#unit-test-consideration)

[Appendix A Abbreviations and Acronyms
[11](#abbreviations-and-acronyms)](#abbreviations-and-acronyms)

[Appendix B Glossary [12](#glossary)](#glossary)

[Appendix C References [13](#references)](#references)

# Introduction

## Purpose

Module Design Document for MM057A_FordMsg215BusHiSpd_Impl.

## Scope

The following definitions are used throughout this document:

-   **<u>Shall</u>**: indicates a mandatory requirement without
    exception in compliance.

-   **<u>Should</u>**: indicates a mandatory requirement; exceptions
    allowed only with documented justification.

-   **<u>May</u>**: indicates an optional action.

# FordMsg215BusHiSpd & High-Level Description

The purpose of the Ford Message 215 Bus High Speed function is to
provide the Electric Power Steering system with trailer Back up Assist
and Gear Lever Position signals from CAN. The Ford Message 215 function
will perform the missing message and signal invalid diagnostics as well
as provide a validity signal for the signal values and received message.

# Design details of software module

## Graphical representation of FordMsg215BusHiSpd

<img
src="ElectricPowerSteering_RH850_FORD_T3T6_website/docs/MM057A_FordMsg215BusHiSpd_Impl/doc/mediax/media/image1.png"
style="width:4.625in;height:3.52083in" />

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

### Init: Init1

#### Design Rationale

Refer FDD

#### Module Outputs

Refer FDD

### Per: Per1

#### Design Rationale

Refer FDD

#### Store Module Inputs to Local copies

Refer FDD

#### (Processing of function) ………

Refer FDD

#### Store Local copy of outputs into Module Outputs

Refer FDD

## Server Runnables

### ComIPduCallout_APIM_Send_Signals_2_FD1

## 5.2.1.1 Design Rationale [design-rationale-2]

None

## 5.2.1.2 Processing of function [processing-of-function-1]

None

### ComTimeoutNotification_TrlrAidMde_D_Rq

## 5.2.2.1 Design Rationale [design-rationale-3]

None

## 5.2.2.2 Processing of function [processing-of-function-2]

None

## Interrupt Functions

None

## Module Internal (Local) Functions

## Local Function \#1

| **Function Name** | MsgMiss                            | Type                 | Min | Max |
|------------|---------------------------|-----------------|---------|---------|
| Arguments Passed  | DiagEna_Cnt_T_logl                 | boolean              | 0U  | 1U  |
|                   | FordEpsLifeCycMod_Cnt_T_u08        | uint8                | 0U  | 1U  |
|                   | ClrDiagcFlgProxy_Cnt_T_u08         | uint8                | 0U  | 1U  |
|                   | FordVehTrlrAidModReqVld_Cnt_T_logl | boolean              | 0U  | 1U  |
|                   | FordVehTrlrAidModReq_Cnt_T_enum    | Ford_TrlrAidMde_D_Rq | 0U  | 3U  |
| Return Value      |                                    |                      |     |     |

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
| 5       | FDD: MM057A_FordMsg215BusHiSpd_Design                                        | See Synergy subproject version |

{% endraw %}