---
layout: default
title: FordMsg414BusHiSpd_MDD
nav_order: 2
parent: Component Implementation
---
{% raw %}
**Module Design Document**

**For**

**FordMsg414BusHiSpd**

**4-Apr-2018**

**Prepared For:**

**Software Engineering**

**Nexteer Automotive,**

**Saginaw, MI, USA**

**Prepared By:**

**Tata Elxsi,**

**Trivandrum, INDIA**

**<u>Change History</u>**

|             |                                                     |                        |             |             |
|---------|--------------------|----------------------|----------|-------------|
| **Sl. No.** | **Description**                                     | **Author**             | **Version** | **Date**    |
| 1           | Initial Version                                     | TATA                   | 1.0         | 23-Nov-2017 |
| 2           | Implemented FDD version 2.0.0                       | TATA                   | 2.0         | 05-Jan-2018 |
| 3           | Updated graphical representation and local function | Shishir Holenarasipura | 3.0         | 4-Apr-2018  |

<u>Table of Contents</u>

[1 Introduction 6](#introduction)

[1.1 Purpose 6](#purpose)

[2 FordMsg414BusHiSpd & High-Level Description
7](#fordmsg414bushispd-high-level-description)

[3 Design details of software module
8](#design-details-of-software-module)

[3.1 Graphical representation of FordMsg414BusHiSpd
8](#graphical-representation-of-fordmsg414bushispd)

[3.2 Data Flow Diagram 8](#data-flow-diagram)

[Component level DFD 8](#component-level-dfd)

[Function level DFD 8](#function-level-dfd)

[4 Constant Data Dictionary 9](#constant-data-dictionary)

[4.1 Program (fixed) Constants 9](#program-fixed-constants)

[Embedded Constants 9](#embedded-constants)

[5 Software Component Implementation
10](#software-component-implementation)

[5.1 Sub-Module Functions 10](#sub-module-functions)

[5.1.1 Init: FordMsg414BusHiSpdInit1 10](#init-fordmsg414bushispdinit1)

[5.1.1.1 Design Rationale 10](#design-rationale)

[5.1.1.2 Module Outputs 10](#module-outputs)

[5.1.2 Per: FordMsg414BusHiSpdPer1 10](#per-fordmsg414bushispdper1)

[5.1.2.1 Design Rationale 10](#design-rationale-1)

[5.1.2.2 Store Module Inputs to Local copies
10](#store-module-inputs-to-local-copies)

[5.1.2.3 Processing of function 10](#processing-of-function)

[5.1.2.4 Store Local copy of outputs into Module Outputs
10](#store-local-copy-of-outputs-into-module-outputs)

[5.2 Server Runnables 10](#server-runnables)

[5.2.1 ComIPduCallout_BrakeSnData_6_HS2
10](#comipducallout_brakesndata_6_fd1)

[5.2.1.1 Design Rationale 10](#design-rationale-2)

[5.2.1.2 Processing of function 10](#processing-of-function-1)

[5.2.2 ComTimeoutNotification_Ford_StePinOffst_D_Stat
10](#comtimeoutnotification_ford_stepinoffst_d_stat)

[5.2.2.1 Design Rationale 10](#design-rationale-3)

[5.2.2.2 Processing of function 10](#processing-of-function-2)

[5.3 Interrupt Functions 11](#interrupt-functions)

[5.4 Module Internal (Local) Functions
11](#module-internal-local-functions)

[5.4.1 Local Function \#1 11](#local-function-1)

[5.4.1.1 Design Rationale 11](#design-rationale-4)

[5.4.1.2 Processing 11](#processing)

[5.4.2 Local Function \#2 11](#_Toc510619941)

[5.4.2.1 Design Rationale 12](#_Toc510619942)

[5.4.2.2 Processing 12](#_Toc510619943)

[5.5 GLOBAL Function/Macro Definitions 12](#_Toc497138900)

[6 Known Limitations with Design 13](#known-limitations-with-design)

[7 UNIT TEST CONSIDERATION 14](#unit-test-consideration)

[Appendix A Abbreviations and Acronyms 15](#abbreviations-and-acronyms)

[Appendix B Glossary 16](#glossary)

[Appendix C References 17](#references)

# Introduction

## Purpose

MDD for FordMsg414BusHiSpd

# FordMsg414BusHiSpd & High-Level Description

Please refer FDD.

# Design details of software module

## Graphical representation of FordMsg414BusHiSpd

<img
src="ElectricPowerSteering_RH850_FORD_T3T6_website/docs/MM070A_FordMsg414BusHiSpd_Impl/doc/mediax/media/image2.png"
style="width:5.20833in;height:4.88542in" />

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

# Software Component Implementation

## Sub-Module Functions

### 5.1.1 Init: FordMsg414BusHiSpdInit1

### 5.1.1.1 Design Rationale

> None

### 5.1.1.2 Module Outputs

> None

### 5.1.2 Per: FordMsg414BusHiSpdPer1

## 5.1.2.1 Design Rationale [design-rationale-1]

> None

## 5.1.2.2 Store Module Inputs to Local copies [store-module-inputs-to-local-copies]

> None

## 5.1.2.3 Processing of function [processing-of-function]

> None

## 5.1.2.4 Store Local copy of outputs into Module Outputs [store-local-copy-of-outputs-into-module-outputs]

> None

## Server Runnables 

### 5.2.1 ComIPduCallout_BrakeSnData_6_FD1

## 5.2.1.1 Design Rationale [design-rationale-2]

None

## 5.2.1.2 Processing of function [processing-of-function-1]

None

### 5.2.2 ComTimeoutNotification_Ford_StePinOffst_D_Stat

## 5.2.2.1 Design Rationale [design-rationale-3]

None

## 5.2.2.2 Processing of function [processing-of-function-2]

None

## Interrupt Functions

None

## Module Internal (Local) Functions

##  Local Function \#1

|                      |                                          |                         |       |        |
|----------|------------------------------|------------------|-------|--------|
| **Function Name**    | FordVehSteerPinionOffsVldCovn            | Type                    | Min   | Max    |
| **Arguments Passed** | FordVehSteerPinionAgOffsRaw_Cnt_T_u16    | uint16                  | 0U    | 65535U |
|                      | FordVehSteerPinionOffsSts_Cnt_T_enum     | Ford_StePinOffst_D_Stat | OU    | 3U     |
|                      | FordVehSteerPinionOffsCnt_Cnt_T_u08      | uint8                   | 0U    | 15U    |
|                      | FordVehSteerPinionOffsChks_Cnt_T_u08     | uint8                   | 0U    | 255U   |
|                      | CalcFordVehSteerPinionOffsChks_Cnt_T_u08 | uint8                   | 0U    | 255U   |
|                      | \*CntrVldChkFlg_Cnt_T_log1               | boolean                 | FALSE | TRUE   |
|                      | \*ChksVldChkFlg_Cnt_T_logl               | boolean                 | FALSE | TRUE   |
| **Return Value**     | VldChkFlg_Cnt_T_logl                     | boolean                 | FALSE | TRUE   |

## Design Rationale

None

## Processing

Please refer to the below path in the FDD model.

MM070A_FordMsg414BusHiSpd/FordMsg414BusHiSpd/FordMsg414BusHiSpdPer1/MsgPrsnt/SigProcg/FordVehSteerPinionOffsVldCovn

##  Local Function \#2

|                      |                                   |         |       |      |
|----------|------------------------------|------------------|-------|--------|
| **Function Name**    | VldElpdTi                         | Type    | Min   | Max  |
| **Arguments Passed** | \*AgOffsVldPassdElpdTi_Cnt_T_logl | boolean | FALSE | TRUE |
|                      | \*AgOffsVldFaildElpdTi_Cnt_T_logl | boolean | FALSE | TRUE |
|                      | \*ChksVldFaildElpdTi_Cnt_T_logl   | boolean | FALSE | TRUE |
| **Return Value**     | void                              |         |       |      |

## Design Rationale

None

## Processing

Please refer to the below path in the FDD model.

MM070A_FordMsg414BusHiSpd/FordMsg414BusHiSpd/FordMsg414BusHiSpdPer1/MsgPrsnt/SigProcg/VldElpdTi

<span id="_Toc497138900" class="anchor"></span> GLOBAL Function/Macro
Definitions

None

# Known Limitations with Design

1.  

None.

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

|         |                                                                              |                                |     |
|-------|----------------------------------------|----------|-----------------|
|         |                                                                              |                                |     |
|         |                                                                              |                                |     |
|         |                                                                              |                                |     |
|         |                                                                              |                                |     |
|         |                                                                              |                                |     |
| Ref. \# | Title                                                                        | Version                        |     |
| 1       | AUTOSAR Specification of Memory Mapping (Link:AUTOSAR_SWS_MemoryMapping.pdf) | v1.3.0 R4.0 Rev 2              |     |
| 2       | MDD Guideline                                                                | EA4 01.00                      |     |
| 3       | Software Naming Conventions.doc                                              | EA4 01.02                      |     |
| 4       | Software Design and Coding Standards.doc                                     | EA4 2.01                       |     |
| 5       | MM070A_FordMsg414BusHiSpd_Design                                             | See Synergy subproject version |     |

{% endraw %}