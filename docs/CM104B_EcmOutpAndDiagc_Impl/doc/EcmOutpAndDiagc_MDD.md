---
layout: default
title: EcmOutpAndDiagc_MDD
nav_order: 2
parent: Component Implementation
---
{% raw %}
**Module Design Document**

**For**

**EcmOutpAndDiagc**

**Feb 07, 2018**

**Prepared By:**

**Shruthi Raghavan,**

**Nexteer Automotive,**

**Saginaw, MI, USA  
<u>Change History</u>**

|                                                          |                  |             |             |
|--------------------------------------|--------------|----------|-----------|
| **Description**                                          | **Author**       | **Version** | **Date**    |
| Initial Version                                          | Shruthi Raghavan | 1.0         | 15-Nov-2017 |
| Removed local constant that was removed from NonRte file | Shruthi Raghavan | 2.0         | 07-Feb-2018 |

**  
**

**<u>Table of Contents</u>**

[1 Introduction [4](#introduction)](#introduction)

[1.1 Purpose [4](#purpose)](#purpose)

[2 EcmOutpAndDiagc & High-Level Description
[5](#ecmoutpanddiagc-high-level-description)](#ecmoutpanddiagc-high-level-description)

[3 Design details of software module
[6](#design-details-of-software-module)](#design-details-of-software-module)

[3.1 Graphical representation of EcmOutpAndDiagc
[6](#graphical-representation-of-ecmoutpanddiagc)](#graphical-representation-of-ecmoutpanddiagc)

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

[5.1.1 Init: EcmOutpAndDiagcInit1
[8](#init-ecmoutpanddiagcinit1)](#init-ecmoutpanddiagcinit1)

[5.1.1.1 Design Rationale [8](#design-rationale)](#design-rationale)

[5.1.2 Init: EcmOutpAndDiagcInit3
[8](#init-ecmoutpanddiagcinit3)](#init-ecmoutpanddiagcinit3)

[5.1.2.1 Design Rationale [8](#design-rationale-1)](#design-rationale-1)

[5.1.3 Periodic [8](#periodic)](#periodic)

[5.2 Server Runables [8](#server-runables)](#server-runables)

[5.2.1 CtrlErrOut_Oper [8](#ctrlerrout_oper)](#ctrlerrout_oper)

[5.2.1.1 Design Rationale [8](#design-rationale-2)](#design-rationale-2)

[5.3 Interrupt Functions
[8](#interrupt-functions)](#interrupt-functions)

[5.4 Module Internal (Local) Functions
[8](#module-internal-local-functions)](#module-internal-local-functions)

[5.4.1 Local Function \#1 [8](#local-function-1)](#local-function-1)

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

Module Design Document for Implementation of EcmOutpAndDiagc design for
P1Mc processor based projects.

# EcmOutpAndDiagc & High-Level Description

Refer FDD.

# Design details of software module

## Graphical representation of EcmOutpAndDiagc

> <img
> src="ElectricPowerSteering_RH850_FORD_T3T6_website/docs/CM104B_EcmOutpAndDiagc_Impl/doc/mediax/media/image1.png"
> style="width:3.4326in;height:1.96148in" />

## Data Flow Diagram

### Component level DFD

> Refer FDD

### Function level DFD

> Refer FDD

# Constant Data Dictionary

## Program (fixed) Constants

### Embedded Constants

#### Local Constants

| Constant Name                         | Resolution | Units | Value       |
|---------------------------------------|------------|-------|-------------|
| ECMERROUTZPINSTSREGMASK_CNT_U32       | 1          | Cnt   | 0x80000000U |
| ECMERROUTZPINCOMPERRMASK_CNT_U32      | 1          | Cnt   | 0x40000000U |
| ERROUTPCLRINVLDREGCMPWBITMASK_CNT_U32 | 1          | Cnt   | 0x00010000U |
| ECMCOMPERRBITMASK_CNT_U32             | 1          | Cnt   | 0x10000000U |
|                                       |            |       |             |
| FLASHAPPLCMDIFECMERRMASK_CNT_U32      | 1          | Cnt   | 0x00080000U |
| NROFCOMPERRSRCSETATMPTS_CNT_U08       | 1          | Cnt   | 3U          |
| FEINTRPTREQFLGBITMASK_CNT_U32         | 1          | Cnt   | 0x00001000U |
| FEINTRPTEVESRCECMBITMASK_CNT_U32      | 1          | Cnt   | 0x00000002U |
| ECMERRSETTRIGREGSTSCLRMASK_CNT_U32    | 1          | Cnt   | 0x40000000U |

# Software Component Implementation

## Sub-Module Functions

## Init: EcmOutpAndDiagcInit1

## Design Rationale

> None

## Init: EcmOutpAndDiagcInit3

## Design Rationale

> None

## Periodic

> None

## Server Runables 

## CtrlErrOut_Oper

## Design Rationale

The TrigReg1 enumeration type is given the type qualifier of
EcmOutpAndDiagc so it is not generated in the RTE headers. The header in
the include folder contains the typedef for this enum because it is not
expected to be needed outside the context of this component (or server
runnable call).

## Interrupt Functions

> None

## Module Internal (Local) Functions

## Local Function \#1

|                      |     |      |     |     |
|----------------------|-----|------|-----|-----|
| **Function Name**    | \-  | Type | Min | Max |
| **Arguments Passed** | \-  | \-   | \-  | \-  |
| **Return Value**     | \-  | \-   | \-  | \-  |

## GLOBAL Function/Macro Definitions

None

# Known Limitations with Design

None.

# UNIT TEST CONSIDERATION

> Register file definitions are in the P1Xc/include folder of AR202A
> since this component is designed for P1X-c micro.

####### Abbreviations and Acronyms

| **Abbreviation or Acronym** | **Description**     |
|-----------------------------|---------------------|
| EI                          | Exception Interrupt |
|                             |                     |

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

| **Ref. \#** | **Title**                                                                                                                                                           | **Version**                 |
|-------|---------------------------------------------|--------------------|
| 1           | AUTOSAR Specification of Memory Mapping                                                                                                                             | v1.3.0 R4.0 Rev 2           |
| 2           | MDD Guideline                                                                                                                                                       | EA4 01.00.01                |
| 3           | [Software Naming Conventions.doc](http://misagweb01.nexteer.com/eRoomReq/Files/erooms8/NextGeneration/0_fc55f/Software%20Naming%20Conventions%2003x(In%20Work).doc) | 1.02                        |
| 4           | Software Design and Coding Standards.doc                                                                                                                            | 2.01                        |
| 5           | FDD : CM104B_EcmOutpAndDiagc_Design                                                                                                                                 | See Synergy Subproject Ver. |

{% endraw %}