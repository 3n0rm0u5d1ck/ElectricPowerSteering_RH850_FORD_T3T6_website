---
layout: default
title: HwTq10Meas_MDD
nav_order: 2
parent: Component Implementation
---
{% raw %}
**Module Design Document**

**For**

**HwTq10Meas**

**12-Jan-2018**

**Prepared By:**

**Software Engineering,**

**Nexteer Automotive,**

**Saginaw, MI, USA**

**  
<u>Change History</u>**

|                 |               |             |             |
|-----------------|---------------|-------------|-------------|
| **Description** | **Author**    | **Version** | **Date**    |
| Initial Version | Pratik Jadhav | 1.0         | 12-Jan-2018 |

**  
**

<u>Table of Contents</u>

[1 Introduction [5](#introduction)](#introduction)

[1.1 Purpose [5](#purpose)](#purpose)

[1.2 Scope [5](#scope)](#scope)

[2 HwTq10Meas High-Level Description
[6](#hwtq10meas-high-level-description)](#hwtq10meas-high-level-description)

[3 Design details of software module
[7](#design-details-of-software-module)](#design-details-of-software-module)

[3.1 Graphical representation of HwTq10Meas
[7](#_Toc498603134)](#_Toc498603134)

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

[5.1.1 Init: HwTq10MeasInit1
[9](#init-hwtq10measinit1)](#init-hwtq10measinit1)

[5.1.1.1 Design Rationale [9](#design-rationale)](#design-rationale)

[5.1.2 Per: HwTq10MeasPer1
[9](#per-hwtq10measper1)](#per-hwtq10measper1)

[5.1.2.1 Design Rationale [9](#design-rationale-1)](#design-rationale-1)

[5.1.3 Per: HwTq10MeasPer2
[9](#per-hwtq10measper2)](#per-hwtq10measper2)

[5.1.3.1 Design Rationale [9](#design-rationale-2)](#design-rationale-2)

[5.2 Server Runnables [10](#server-runnables)](#server-runnables)

[5.2.1 HwTq10MeasHwTq10AutTrim
[10](#hwtq10meashwtq10auttrim)](#hwtq10meashwtq10auttrim)

[5.2.1.1 Design Rationale
[10](#design-rationale-3)](#design-rationale-3)

[5.2.2 HwTq10MeasHwTq10ClrTrim
[10](#hwtq10meashwtq10clrtrim)](#hwtq10meashwtq10clrtrim)

[5.2.2.1 Design Rationale
[10](#design-rationale-4)](#design-rationale-4)

[5.2.3 HwTq10MeasHwTq10ReadTrim
[10](#hwtq10meashwtq10readtrim)](#hwtq10meashwtq10readtrim)

[5.2.3.1 Design Rationale
[10](#design-rationale-5)](#design-rationale-5)

[5.2.4 HwTq10MeasHwTq10TrimPrfmdSts
[10](#hwtq10meashwtq10trimprfmdsts)](#hwtq10meashwtq10trimprfmdsts)

[5.2.4.1 Design Rationale
[10](#design-rationale-6)](#design-rationale-6)

[5.2.5 HwTq10MeasHwTq10WrTrim
[10](#hwtq10meashwtq10wrtrim)](#hwtq10meashwtq10wrtrim)

[5.2.5.1 Design Rationale
[10](#design-rationale-7)](#design-rationale-7)

[5.3 Interrupt Functions
[10](#interrupt-functions)](#interrupt-functions)

[5.4 Module Internal (Local) Functions
[11](#module-internal-local-functions)](#module-internal-local-functions)

[5.4.1 Local Function \#1 [11](#local-function-1)](#local-function-1)

[5.4.1.1 Design Rationale
[11](#design-rationale-8)](#design-rationale-8)

[5.4.2 Local Function \#2 [11](#local-function-2)](#local-function-2)

[5.4.2.1 Design Rationale
[11](#design-rationale-9)](#design-rationale-9)

[5.4.3 Local Function \#3 [11](#local-function-3)](#local-function-3)

[5.4.3.1 Design Rationale
[11](#design-rationale-10)](#design-rationale-10)

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

Refer to FDD.

## Scope

# HwTq10Meas High-Level Description

Refer to FDD

# Design details of software module

## Graphical representation of HwTq10Meas

<img
src="ElectricPowerSteering_RH850_FORD_T3T6_website/docs/ES225A_HwTq10Meas_Impl/doc/mediax/media/image1.png"
style="width:5.26042in;height:3.13542in" />

## Data Flow Diagram

### Component level DFD

Refer to FDD

### Function level DFD

Refer to FDD

# Constant Data Dictionary

## Program (fixed) Constants

### Embedded Constants

#### Local Constants

| Constant Name      | Resolution | Units | Value |
|--------------------|------------|-------|-------|
| CRCTBLSIZE_CNT_U08 | 1          | Cnt   | 16U   |
|                    |            |       |       |

*\* Refer to FDD for other constant definitions*

# Software Component Implementation

## Sub-Module Functions

## Init: HwTq10MeasInit1

## Design Rationale

None

## Per: HwTq10MeasPer1

## Design Rationale

Clear local buffer in the below path of the model has not been
implemented, because it’s not required.

Path : ES225A_HwTq10Meas/HwTq10Meas/HwTq10MeasPer1/Raw Data
Processing/Clear Local Buffer

## Per: HwTq10MeasPer2

## Design Rationale

None

## Server Runnables 

## HwTq10MeasHwTq10AutTrim

## Design Rationale

None

## HwTq10MeasHwTq10ClrTrim

## Design Rationale

None

## HwTq10MeasHwTq10ReadTrim

## Design Rationale

None

## HwTq10MeasHwTq10TrimPrfmdSts

## Design Rationale

None

## HwTq10MeasHwTq10WrTrim

## Design Rationale

None

## Interrupt Functions

None

## Module Internal (Local) Functions

### Local Function \#1

|                      |                      |       |     |     |
|----------------------|----------------------|-------|-----|-----|
| **Function Name**    | StuckNoDataSeln      | Type  | Min | Max |
| **Arguments Passed** | NA                   | N/A   | N/A | N/A |
| **Return Value**     | MissMsgEna_Uls_T_u08 | uint8 | 0   | 1   |

## Design Rationale

This function is split from Per1 to reduce path count and cyclomatic
complexity.

## Local Function \#2

|                      |                   |         |      |            |
|----------------------|-------------------|---------|------|------------|
| **Function Name**    | RngChk            | Type    | Min  | Max        |
| **Arguments Passed** | Temp_Cnt_T_u32    | uint32  | 0    | 4294967295 |
| **Return Value**     | RngChk_Cnt_T_logl | boolean | TRUE | FALSE      |

## Design Rationale

This function is split from Per1 to reduce path count and cyclomatic
complexity.

## Local Function \#3

|                      |                           |        |     |     |
|----------------------|---------------------------|--------|-----|-----|
| **Function Name**    | CrcChk                    | Type   | Min | Max |
| **Arguments Passed** | CalcdCrc_Cnt_T_u16        | uint16 | 0   | 15  |
| **Arguments Passed** | AntcptdCrc_Cnt_T_u16      | uint16 | 0   | 15  |
| **Return Value**     | CRCFaildPrmByte_Cnt_T_u08 | uint8  | 0   | 1   |

## Design Rationale

This function is split from Per1 to reduce path count and cyclomatic
complexity.

# Known Limitations with Design

> None.

# UNIT TEST CONSIDERATION

1.  Clear local buffer in the below path of the model has not been
    implemented, because it’s not required. Path :
    ES225A_HwTq10Meas/HwTq10Meas/HwTq10MeasPer1/Raw Data
    Processing/Clear Local Buffer

####### Abbreviations and Acronyms

| **Abbreviation or Acronym** | **Description**        |
|-----------------------------|------------------------|
| MDD                         | Module Design Document |
| DFD                         | Data Flow Diagram      |

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

|     |     |     |
|-----|-----|-----|
|     |     |     |
|     |     |     |

####### References

| **Ref. \#** | **Title**                               | **Version**                     |
|-------|-------------------------------------------------|-----------------|
| 1           | AUTOSAR Specification of Memory Mapping | v1.3.0 R4.0 Rev 2               |
| 2           | MDD Guideline                           | EA4 01.00.01                    |
| 3           | EA4 Software Naming Conventions         | 01.01.00                        |
| 4           | Software Design and Coding Standards    | 2.1                             |
| 5           | FDD – ES225A_HwTq10Meas_Design          | See Synergy sub project version |

{% endraw %}