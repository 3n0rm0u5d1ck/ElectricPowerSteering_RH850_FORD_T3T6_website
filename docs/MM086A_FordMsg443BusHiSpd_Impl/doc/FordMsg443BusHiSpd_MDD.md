---
layout: default
title: FordMsg443BusHiSpd_MDD
nav_order: 2
parent: Component Implementation
---
{% raw %}
**Module Design Document**

**For**

**FordMsg443BusHiSpd**

**June 19, 20158**

**Prepared For:**

**Software Engineering**

**Nexteer Automotive,**

**Saginaw, MI, USA**

**Prepared By:**

**Nexteer ISC,**

**Bengaluru, INDIA.**

**<u>Change History</u>**

|                 |             |         |             |
|-----------------|-------------|---------|-------------|
| Description     | Author      | Version | Date        |
| Initial Version | Nexteer ISC | 1.0     | 23-Apr-2018 |

**<u>Table of Contents</u>**

[1 Introduction [6](#introduction)](#introduction)

[1.1 Purpose [6](#purpose)](#purpose)

[2 FordMsg443BusHiSpd & High-Level Description
[7](#fordmsg443bushispd-high-level-description)](#fordmsg443bushispd-high-level-description)

[3 Design details of software module
[8](#design-details-of-software-module)](#design-details-of-software-module)

[3.1 Graphical representation of FordMsg443BusHiSpd
[8](#graphical-representation-of-fordmsg443bushispd)](#graphical-representation-of-fordmsg443bushispd)

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

[5.1.1 Init: FordMsg443BusHiSpdInit1
[10](#init-fordmsg443bushispdinit1)](#init-fordmsg443bushispdinit1)

[5.1.1.1 Design Rationale [10](#design-rationale)](#design-rationale)

[5.1.1.2 Module Outputs [10](#module-outputs)](#module-outputs)

[5.1.2 Per: FordMsg443BusHiSpdPer1
[10](#per-fordmsg443bushispdper1)](#per-fordmsg443bushispdper1)

[5.1.2.1 Design Rationale
[10](#design-rationale-1)](#design-rationale-1)

[5.1.2.2 Store Module Inputs to Local copies
[10](#store-module-inputs-to-local-copies)](#store-module-inputs-to-local-copies)

[5.1.2.3 Processing of function)………
[10](#processing-of-function)](#processing-of-function)

[5.1.2.4 Store Local copy of outputs into Module Outputs
[10](#store-local-copy-of-outputs-into-module-outputs)](#store-local-copy-of-outputs-into-module-outputs)

[5.2 Server Runnables [10](#server-runnables)](#server-runnables)

[5.2.1 ComIPduCallout_TrailerInfo_FD1
[10](#comipducallout_trailerinfo_fd1)](#comipducallout_trailerinfo_fd1)

[5.2.1.1 Design Rationale
[10](#design-rationale-2)](#design-rationale-2)

[5.2.1.2 (Processing of function)
[10](#processing-of-function-1)](#processing-of-function-1)

[5.2.2 ComTimeoutNotification_TrlrLampCnnct_B_Actl
[10](#comtimeoutnotification_trlrlampcnnct_b_actl)](#comtimeoutnotification_trlrlampcnnct_b_actl)

[5.2.2.1 Design Rationale
[10](#design-rationale-3)](#design-rationale-3)

[5.2.2.2 (Processing of function)
[10](#processing-of-function-2)](#processing-of-function-2)

[5.3 Interrupt Functions
[11](#interrupt-functions)](#interrupt-functions)

[5.4 Module Internal (Local) Functions
[11](#module-internal-local-functions)](#module-internal-local-functions)

[5.4.1 Local Function \#1 [11](#local-function-1)](#local-function-1)

[5.4.1.1 Design Rationale
[11](#design-rationale-4)](#design-rationale-4)

[5.4.1.2 Processing [11](#processing)](#processing)

[5.4.2 Local Function \#2 [11](#local-function-2)](#local-function-2)

[5.4.2.1 Design Rationale
[11](#design-rationale-5)](#design-rationale-5)

[5.4.2.2 Processing [11](#processing-1)](#processing-1)

[5.4.3 Local Function \#3 [12](#local-function-3)](#local-function-3)

[5.4.3.1 Design Rationale
[12](#design-rationale-6)](#design-rationale-6)

[5.4.3.2 Processing [12](#processing-2)](#processing-2)

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

MDD for FordMsg443BusHiSpd

# FordMsg443BusHiSpd & High-Level Description

Please refer FDD.

# Design details of software module

## Graphical representation of FordMsg443BusHiSpd

<img
src="ElectricPowerSteering_RH850_FORD_T3T6_website/docs/MM086A_FordMsg443BusHiSpd_Impl/doc/mediax/media/image1.png"
style="width:4.4625in;height:3in" />

## Data Flow Diagram

### Component level DFD

Please refer FDD.

### Function level DFD

Please refer FDD.

# Constant Data Dictionary

## Program (fixed) Constants

### Embedded Constants

#### Local Constants

| Constant Name                        | Resolution | Units | Value |
|--------------------------------------|------------|-------|-------|
| Please refer Data Dictionary .m file | --         | --    | --    |

# Software Component Implementation

## Sub-Module Functions

### 5.1.1 Init: FordMsg443BusHiSpdInit1 [init-fordmsg443bushispdinit1]

## Design Rationale

None

## Module Outputs

None

### 5.1.2 Per: FordMsg443BusHiSpdPer1 [per-fordmsg443bushispdper1]

## 5.1.2.1 Design Rationale [design-rationale-1]

None

## 5.1.2.2 Store Module Inputs to Local copies [store-module-inputs-to-local-copies]

None

## 5.1.2.3 Processing of function)……… [processing-of-function]

None

## 5.1.2.4 Store Local copy of outputs into Module Outputs [store-local-copy-of-outputs-into-module-outputs]

None

## Server Runnables 

### 5.2.1 ComIPduCallout_TrailerInfo_FD1 [comipducallout_trailerinfo_fd1]

## 5.2.1.1 Design Rationale [design-rationale-2]

None

## 5.2.1.2 (Processing of function) [processing-of-function-1]

None

### 5.2.2 ComTimeoutNotification_TrlrLampCnnct_B_Actl [comtimeoutnotification_trlrlampcnnct_b_actl]

## 5.2.2.1 Design Rationale [design-rationale-3]

None

## 5.2.2.2 (Processing of function) [processing-of-function-2]

None

## Interrupt Functions

None

## Module Internal (Local) Functions

## Local Function \#1

| **Function Name**    | CalSeln                        | Type   | Min | Max    |
|----------------------|--------------------------------|--------|-----|--------|
| **Arguments Passed** | FordEpsLifeCycMod_Cnt_T_u08    | Uint8  | 0U  | 1U     |
| **Return Value**     | BusHiSpdMissThd_MilliSec_T_u16 | Uint16 | 0U  | 65535U |

## Design Rationale

## Processing

Please refer to the below path in the FDD model.

MM086A_FordMsg443BusHiSpd/FordMsg443BusHiSpd/FordMsg443BusHiSpdPer1/CalSeln

## Local Function \#2

| **Function Name**    | MissMsgDtrm                             | Type                      | Min   | Max    |
|----------|-----------------------------|-----------------|---------|---------|
| **Arguments Passed** | MissingMsgDiagEna_Cnt_T_logl            | boolean                   | FALSE | TRUE   |
|                      | ClrDiagcFlgProxyEna_Cnt_T_logl          | boolean                   | FALSE | TRUE   |
|                      | BusHiSpdMissThd_MilliSec_T_u16          | Uint16                    | 0U    | 65535U |
|                      | \*FordVehTrlrLampCnctnStsRaw_Cnt_T_enum | Ford_TrlrLampCnnct_B_Actl | FALSE | TRUE   |
| **Return Value**     | None                                    |                           |       |        |

## Design Rationale

## Processing

Please refer to the below path in the FDD model.

MM086A_FordMsg443BusHiSpd/FordMsg443BusHiSpd/FordMsg443BusHiSpdPer1/MissMsgDetermination

## Local Function \#3

| **Function Name**    | MsgPrsnt                                | Type                      | Min   | Max  |
|----------|-----------------------------|-----------------|---------|---------|
| **Arguments Passed** | MissingMsgDiagEna_Cnt_T_logl            | boolean                   | FALSE | TRUE |
|                      | ClrDiagcFlgProxyEna_Cnt_T_logl          | boolean                   | FALSE | TRUE |
|                      | \*FordVehTrlrLampCnctnStsRaw_Cnt_T_enum | Ford_TrlrLampCnnct_B_Actl | FALSE | TRUE |
| **Return Value**     | None                                    |                           |       |      |

## Design Rationale

## Processing

Please refer to the below path in the FDD model.

MM086A_FordMsg443BusHiSpd/FordMsg443BusHiSpd/FordMsg443BusHiSpdPer1/Msg_Present

## GLOBAL Function/Macro Definitions

None

# Known Limitations with Design

> None.

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

| **Ref. \#** | **Title**                                                                                                                                                             | **Version**                     |
|-------|-------------------------------------------------|-----------------|
| 1           | AUTOSAR Specification of Memory Mapping (Link:[AUTOSAR_SWS_MemoryMapping.pdf](http://www.autosar.org/download/R4.0/AUTOSAR_SWS_MemoryMapping.pdf))                    | v1.3.0 R4.0 Rev 2               |
| 2           | MDD Guideline                                                                                                                                                         | EA4 01.00.00                    |
| 3           | [Software Naming Conventions.doc](http://misagweb01.nexteer.com/eRoomReq/Files/erooms8/NextGeneration/0_fc55f/Software%20Naming%20Conventions%2003x(In%20Work).doc)   | 1.0                             |
| 4           | [Software Design and Coding Standards.doc](http://eroom1.nexteer.com/eRoomReq/Files/erooms8/NextGeneration/0_1a67a9/Software%20Design%20and%20Coding%20Standards.doc) | 2.1                             |
| 5           | FDD: MM086A\_ FordMsg443BusHiSpd_Design                                                                                                                               | See Synergy sub project version |

{% endraw %}