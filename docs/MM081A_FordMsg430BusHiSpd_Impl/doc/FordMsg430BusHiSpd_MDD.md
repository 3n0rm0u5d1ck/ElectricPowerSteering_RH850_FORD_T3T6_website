---
layout: default
title: FordMsg430BusHiSpd_MDD
nav_order: 2
parent: Component Implementation
---
{% raw %}
**Module Design Document**

**For**

**FordMsg430BusHiSpd**

**June 19, 20158**

**Prepared For:**

**Software Engineering**

**Nexteer Automotive,**

**Saginaw, MI, USA**

**Prepared By:**

**Tata Elxsi,**

**Trivandrum, INDIA**

**<u>Change History</u>**

|                                                     |        |         |             |
|------------------------|---------------------|--------------|--------------|
| Description                                         | Author | Version | Date        |
| Initial Version                                     | TATA   | 1.0     | 04-Dec-2017 |
| Implemented FDD version 2.0.0 and FDD version 2.1.0 | TATA   | 2.0     | 05-Jan-2018 |

<u>Table of Contents</u>

[1 Introduction 5](#introduction)

[1.1 Purpose 5](#purpose)

[2 FordMsg430BusHiSpd & High-Level Description
6](#fordmsg430bushispd-high-level-description)

[3 Design details of software module
7](#design-details-of-software-module)

[3.1 Graphical representation of FordMsg430BusHiSpd
7](#graphical-representation-of-fordmsg430bushispd)

[3.2 Data Flow Diagram 7](#data-flow-diagram)

[3.2.1 Component level DFD 7](#component-level-dfd)

[3.2.2 Function level DFD 7](#function-level-dfd)

[4 Constant Data Dictionary 8](#constant-data-dictionary)

[4.1 Program (fixed) Constants 8](#program-fixed-constants)

[4.1.1 Embedded Constants 8](#embedded-constants)

[5 Software Component Implementation
9](#software-component-implementation)

[5.1 Sub-Module Functions 9](#sub-module-functions)

[5.1.1 Init: FordMsg430BusHiSpdInit1 9](#init-fordmsg430bushispdinit1)

[5.1.1.1 Design Rationale 9](#design-rationale)

[5.1.1.2 Module Outputs 9](#module-outputs)

[5.1.2 Per: FordMsg430BusHiSpdPer1 9](#per-fordmsg430bushispdper1)

[5.1.2.1 Design Rationale 9](#design-rationale-1)

[5.1.2.2 Store Module Inputs to Local copies
9](#store-module-inputs-to-local-copies)

[5.1.2.3 Processing of function) 9](#processing-of-function)

[5.1.2.4 Store Local copy of outputs into Module Outputs
9](#store-local-copy-of-outputs-into-module-outputs)

[5.2 Server Runnables 9](#server-runnables)

[None 9](#_Toc502944345)

[5.3 Interrupt Functions 9](#interrupt-functions)

[5.4 Module Internal (Local) Functions
9](#module-internal-local-functions)

[5.4.1 Local Function \#1 9](#local-function-1)

[5.4.1.1 Design Rationale 10](#design-rationale-2)

[5.4.1.2 Processing 10](#processing)

[5.5 GLOBAL Function/Macro Definitions
10](#global-functionmacro-definitions)

[6 Known Limitations with Design 11](#known-limitations-with-design)

[7 UNIT TEST CONSIDERATION 12](#unit-test-consideration)

[Appendix A Abbreviations and Acronyms 13](#abbreviations-and-acronyms)

[Appendix B Glossary 14](#glossary)

[Appendix C References 15](#references)

3.2.1 Component level DFD 7 3.2.2 Function level DFD 7 4 Constant Data
Dictionary 8 4.1 Program (fixed) Constants 8 4.1.1 Embedded Constants 8
5 Software Component Implementation 9 5.1 Sub-Module Functions 9 5.1.1
Init: FordMsg430BusHiSpdInit1 9 5.1.1.1 Design Rationale 9 5.1.1.2
Module Outputs 9 5.1.2 Per: FordMsg430BusHiSpdPer1 9 5.1.2.1 Design
Rationale 9 5.1.2.2 Store Module Inputs to Local copies 9 5.1.2.3
Processing of function) 9 5.1.2.4 Store Local copy of outputs into
Module Outputs 9 5.2 Server Runnables 9 5.2.1
FordMsg430HiSpdBusClrDiagcSrv 9 5.2.1.1 Design Rationale 9 5.2.1.2
(Processing of function) 9 5.2.2 FordMsg430HiSpdBusSerlComInpDi 9
5.2.2.1 Design Rationale 9 5.2.2.2 (Processing of function) 9 5.3
Interrupt Functions 10 5.4 Module Internal (Local) Functions 10 5.4.1
Local Function \#1 10 5.4.1.1 Design Rationale 10 5.4.1.2 Processing 10
5.4.2 Local Function \#2 10 5.4.2.1 Design Rationale 11 5.4.2.2
Processing 11 5.5 GLOBAL Function/Macro Definitions 11 6 Known
Limitations with Design 12 7 UNIT TEST CONSIDERATION 13 Appendix A
Appendix B

# Introduction

## Purpose

MDD for FordMsg430BusHiSpd

# FordMsg430BusHiSpd & High-Level Description

Please refer FDD.

# Design details of software module

## Graphical representation of FordMsg430BusHiSpd

<img
src="ElectricPowerSteering_RH850_FORD_T3T6_website/docs/MM081A_FordMsg430BusHiSpd_Impl/doc/mediax/media/image2.jpeg"
style="width:5.02083in;height:3.21875in"
alt="C:\Users\ramachandran.mg\Desktop\MM081A.JPG" />

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
| Please refer Data Dictionary .m file | NA         | NA    | NA    |

# Software Component Implementation

## Sub-Module Functions

### 5.1.1 Init: FordMsg430BusHiSpdInit1 [init-fordmsg430bushispdinit1]

## Design Rationale

None

## Module Outputs

None

### 5.1.2 Per: FordMsg430BusHiSpdPer1 [per-fordmsg430bushispdper1]

## 5.1.2.1 Design Rationale [design-rationale-1]

None

## 5.1.2.2 Store Module Inputs to Local copies [store-module-inputs-to-local-copies]

None

## 5.1.2.3 Processing of function) [processing-of-function]

None

## 5.1.2.4 Store Local copy of outputs into Module Outputs [store-local-copy-of-outputs-into-module-outputs]

None

## Server Runnables 

### None [none]

###  [section]

##  [section-1]

##  [section-2]

###  [section-3]

##  [section-4]

##  [section-5]

### 

## Interrupt Functions

None

## Module Internal (Local) Functions

## Local Function \#1

| **Function Name**    | NtcFail                     | Type    |     | Min    |     | Max           |     |
|----------|---------------------------|--|---------------|--|--------|--|---------|
| **Arguments Passed** | MissMsgDiagEna_Cnt_T_logl   | boolean |     | FALSE  |     | TRUE          |     |
|                      | BusHiSpdMissThd_Cnt_T_u16   | uint16  |     | 0U     |     | 6000U         |     |
|                      | \*FordVehOdom_KiloMtr_T_f32 | float32 |     | (0.0F) |     | (16777215.0)F |     |
| **Return Value**     | None                        |         |     |        |     |               |     |
|                      |                             |         |     |        |     |               |     |
|                      |                             |         |     |        |     |               |     |
|                      |                             |         |     |        |     |               |     |
|                      |                             |         |     |        |     |               |     |
|                      |                             |         |     |        |     |               |     |
|                      |                             |         |     |        |     |               |     |
|                      |                             |         |     |        |     |               |     |
|                      |                             |         |     |        |     |               |     |
|                      |                             |         |     |        |     |               |     |
|                      |                             |         |     |        |     |               |     |

## Design Rationale

## Processing

Please refer to the below path in the FDD model.

MM081A_FordMsg430BusHiSpd/FordMsg430BusHiSpd/FordMsg430BusHiSpdPer1/MsgMiss/NtcFail

1.  

|     |     |     |     |     |
|-----|-----|-----|-----|-----|
|     |     |     |     |     |
|     |     |     |     |     |
|     |     |     |     |     |
|     |     |     |     |     |
|     |     |     |     |     |
|     |     |     |     |     |
|     |     |     |     |     |
|     |     |     |     |     |
|     |     |     |     |     |
|     |     |     |     |     |
|     |     |     |     |     |

## 

## 

## 

## GLOBAL Function/Macro Definitions

None

# Known Limitations with Design

1.  Datatype of input variable ClrDiagcFlgProxy is uint8 in the data
    dictionary, but it must be Boolean according to the design in the
    model.

2.  In the below design path,

MM081A_FordMsg430BusHiSpd/FordMsg430BusHiSpd/FordMsg430BusHiSpdPer1

The inputs to merge block are not the same corresponding to the output
signal FordVehOdom.

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
| 5           | FDD: MM077A_FordMsg415BusHiSpd_Design_2.1.0                                                                                                                           | See Synergy sub project version |

{% endraw %}