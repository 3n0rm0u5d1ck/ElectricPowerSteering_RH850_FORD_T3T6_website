---
layout: default
title: HwTqArbn_MDD
nav_order: 3
parent: Component Implementation
---
{% raw %}
**Module Design Document**

**For**

**HwTqArbn**

**Feb 21, 2017**

**Prepared For:**

**Software Engineering**

**Nexteer Automotive,**

**Saginaw, MI, USA**

**Prepared By:**

**Matthew Leser,**

**Nexteer Automotive,**

**Saginaw, MI, USA**

**<u>Change History</u>**

|                 |            |             |             |
|-----------------|------------|-------------|-------------|
| **Description** | **Author** | **Version** | **Date**    |
| Initial Version | ML         | 1.0         | 21-Feb-2017 |

**  
**

**<u>Table of Contents</u>**

[1 Introduction [6](#introduction)](#introduction)

[1.1 Purpose [6](#purpose)](#purpose)

[1.2 Scope [6](#scope)](#scope)

[2 HwTqArbn & High-Level Description
[7](#hwtqarbn-high-level-description)](#hwtqarbn-high-level-description)

[3 Design details of software module
[8](#design-details-of-software-module)](#design-details-of-software-module)

[3.1 Graphical representation of HwTqArbn
[8](#graphical-representation-of-hwtqarbn)](#graphical-representation-of-hwtqarbn)

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

[5.1.1 Init: HwTqArbnInit1
[10](#init-hwtqarbninit1)](#init-hwtqarbninit1)

[5.1.1.1 Design Rationale [10](#design-rationale)](#design-rationale)

[5.1.1.2 Module Outputs [10](#module-outputs)](#module-outputs)

[5.1.2 Per: HwTqArbnPer1 [10](#per-hwtqarbnper1)](#per-hwtqarbnper1)

[5.1.2.1 Design Rationale
[10](#design-rationale-1)](#design-rationale-1)

[5.1.2.2 (Processing of function)………
[10](#processing-of-function)](#processing-of-function)

[5.2 Server Runables [10](#server-runables)](#server-runables)

[5.3 Interrupt Functions
[10](#interrupt-functions)](#interrupt-functions)

[5.4 Module Internal (Local) Functions
[10](#module-internal-local-functions)](#module-internal-local-functions)

[5.4.1 Local Function \#1 [10](#local-function-1)](#local-function-1)

[5.4.1.1 Design Rationale
[10](#design-rationale-2)](#design-rationale-2)

[5.4.1.2 Processing [10](#processing)](#processing)

[5.4.2 Local Function \#2 [11](#local-function-2)](#local-function-2)

[5.4.2.1 Design Rationale
[11](#design-rationale-3)](#design-rationale-3)

[5.4.2.2 Processing [11](#processing-1)](#processing-1)

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

## Scope

# HwTqArbn & High-Level Description

*Refer FDD.*

# Design details of software module

*\<The Data Flow Diagrams should be created in the absence of this
representation with the FDD.\>*

## Graphical representation of HwTqArbn 

<img
src="ElectricPowerSteering_RH850_FORD_T3T6_website/docs/ES228C_HwTqArbn_Impl/doc/mediax/media/image1.png"
style="width:2.16091in;height:3.03542in" />

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

| Constant Name    | Resolution | Units | Value |
|------------------|------------|-------|-------|
| BITMASKA_ULS_U08 | 1          | Cnt   | 0x01  |
| BITMASKB_ULS_U08 | 1          | Cnt   | 0x02  |
| BITMASKC_CNT_U08 | 1          | Cnt   | 0x04  |
| BITMASKD_CNT_U08 | 1          | Cnt   | 0x08  |

# Software Component Implementation

## Sub-Module Functions

## Init: HwTqArbnInit1

## Design Rationale

Init1 function is created so that it will allow a RTE model to be
created in the AUTOSAR tools which allows Per-Instance Memory and
calibration definition needs. The initialization function is doing
nothing

## Module Outputs

*None*

## Per: HwTqArbnPer1

## Design Rationale

*None*

##  (Processing of function)………

*Refer FDD*

## Server Runables 

None

## Interrupt Functions

*None*

## Module Internal (Local) Functions

## Local Function \#1

|                      |                           |          |               |               |
|--------------|------------------------------|---------|-----------|-----------|
| **Function Name**    | HwTqSigAvl                | Type     | Min           | Max           |
| **Arguments Passed** | HwTqRollgCntr_Cnt_T_u08   | uint8    | 0             | 255           |
|                      | HwTqQlfr_Cnt_T_enum       | SigQlfr1 | SIGQLFR_NORES | SIGQLFR_FAILD |
|                      | CorrlSig_Cnt_T_logl       | boolean  | FALSE         | TRUE          |
|                      | \*RollgCntrPrev_Cnt_T_u08 | uint8    | 0             | 255           |
|                      | \*StallCntr_Cnt_T_u08     | uint8    | 0             | 255           |
| **Return Value**     | HwTqArbnAvl_Cnt_T_logl    | boolean  | FALSE         | TRUE          |

## Design Rationale

None

## Processing

None

## Local Function \#2

|                      |                                |         |       |      |
|----------------------|--------------------------------|---------|-------|------|
| **Function Name**    | HwTqContrbn                    | Type    | Min   | Max  |
| **Arguments Passed** | HwTqAvl_Cnt_T_logl             | boolean | FALSE | TRUE |
|                      | HwTqContrbn_HwNwtMtr_T_f32     | float32 | 0     | 10   |
|                      | \*HwTqNumCntrbn_HwNwtMtr_T_f32 | float32 | -40   | 40   |
|                      | \*HwTqDenomCntrbn_Uls_T_f32    | float32 | 0     | 4    |
| **Return Value**     | None                           |         |       |      |

## Design Rationale

None

## Processing

None

## GLOBAL Function/Macro Definitions

None

# Known Limitations with Design

None

# UNIT TEST CONSIDERATION

None

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

| **Ref. \#** | **Title**                                                                                                                                                             | **Version**                    |
|-------|-------------------------------------------------|-----------------|
| 1           | AUTOSAR Specification of Memory Mapping (Link:[AUTOSAR_SWS_MemoryMapping.pdf](http://www.autosar.org/download/R4.0/AUTOSAR_SWS_MemoryMapping.pdf))                    | v1.3.0 R4.0 Rev 2              |
| 2           | MDD Guideline                                                                                                                                                         | EA4 01.00.00                   |
| 3           | [Software Naming Conventions.doc](http://misagweb01.nexteer.com/eRoomReq/Files/erooms8/NextGeneration/0_fc55f/Software%20Naming%20Conventions%2003x(In%20Work).doc)   | 2.0                            |
| 4           | [Software Design and Coding Standards.doc](http://eroom1.nexteer.com/eRoomReq/Files/erooms8/NextGeneration/0_1a67a9/Software%20Design%20and%20Coding%20Standards.doc) | 2.1                            |
| 5           | FDD – ES228C_HwTqArbn_Design                                                                                                                                          | See Synergy Subproject verison |

{% endraw %}