---
layout: default
title: FordMsg5B5BusHiSpd_MDD
nav_order: 2
parent: Component Implementation
---
{% raw %}
**Module Design Document**

**For**

**FordMsg5B5BusHiSpd**

006-Apr-2018

**Prepared For:**

Software Engineering

Nexteer Automotive**,**

Saginaw, MI, USA

**Prepared By:**

**Tata Elxsi,**

**Trivandrum, INDIA**

**<u>Change History</u>**

|             |                                          |            |             |             |
|---------|---------------------|---------------------|----------|-------------|
| **Sl. No.** | **Description**                          | **Author** | **Version** | **Date**    |
| 1           | Initial Version                          | TATA       | 1.0         | 21-Nov-2017 |
| 2           | Updated DaVinci graphical representation | TATA       | 2.0         | 06-APR-2018 |

**<u>Table of Contents</u>**

[1 Introduction 4](#introduction)

[MDD for FordMsg5B5BusHiSpd 4](#mdd-for-fordmsg5b5bushispd)

[2 FordMsg5B5BusHiSpd & High-Level Description
5](#fordmsg5b5bushispd-high-level-description)

[3 Design details of software module
6](#design-details-of-software-module)

[3.1 Graphical representation of FordMsg5B5BusHiSpd
6](#graphical-representation-of-fordmsg5b5bushispd)

[3.2 Data Flow Diagram 6](#data-flow-diagram)

[3.2.1 Component level DFD 6](#component-level-dfd)

[3.2.2 Function level DFD 6](#function-level-dfd)

[4 Constant Data Dictionary 7](#constant-data-dictionary)

[4.1 Program (fixed) Constants 7](#program-fixed-constants)

[4.1.1 Embedded Constants 7](#embedded-constants)

[5 Software Component Implementation
8](#software-component-implementation)

[5.1 Sub-Module Functions 8](#sub-module-functions)

[5.1.1 Init: FordMsg5B5BusHiSpdInit1 8](#init-fordmsg5b5bushispdinit1)

[5.1.2 Per: FordMsg5B5BusHiSpdPer1 8](#per-fordmsg5b5bushispdper1)

[5.2 Server Runnables 8](#server-runnables)

[5.3 Interrupt Functions 8](#interrupt-functions)

[5.4 Module Internal (Local) Functions
8](#module-internal-local-functions)

[5.5 GLOBAL Function/Macro Definitions
8](#global-functionmacro-definitions)

[6 Known Limitations with Design 9](#known-limitations-with-design)

[7 UNIT TEST CONSIDERATION 10](#unit-test-consideration)

[Appendix A Abbreviations and Acronyms 11](#__RefHeading___Toc511813662)

[Appendix B Glossary 12](#glossary)

[Appendix C References 13](#references)

# Introduction

##  MDD for FordMsg5B5BusHiSpd [mdd-for-fordmsg5b5bushispd]

# FordMsg5B5BusHiSpd & High-Level Description

Please refer FDD.

# Design details of software module

## Graphical representation of FordMsg5B5BusHiSpd

<img
src="ElectricPowerSteering_RH850_FORD_T3T6_website/docs/MM519A_FordMsg5B5BusHiSpd_Impl/doc/mediax/media/image2.png"
style="width:3.5625in;height:3.84375in" />

## Data Flow Diagram

### Component level DFD

Please refer FDD.

### Function level DFD

Please refer FDD.

# Constant Data Dictionary

## Program (fixed) Constants

### Embedded Constants

#### Local Constants

|                                      |            |       |       |
|--------------------------------------|------------|-------|-------|
| Constant Name                        | Resolution | Units | Value |
| Please refer Data Dictionary .m file | NA         | NA    | NA    |

# Software Component Implementation

## Sub-Module Functions

### 5.1.1 Init: FordMsg5B5BusHiSpdInit1 [init-fordmsg5b5bushispdinit1]

#### Design Rationale

None

#### Module Outputs

None

### 5.1.2 Per: FordMsg5B5BusHiSpdPer1 [per-fordmsg5b5bushispdper1]

#### 5.1.2.1 Design Rationale [design-rationale-1]

None

#### 5.1.2.2 Store Module Inputs to Local copies [store-module-inputs-to-local-copies]

None

#### 5.1.2.3 Processing of function) [processing-of-function]

None

#### 5.1.2.4 Store Local copy of outputs into Module Outputs [store-local-copy-of-outputs-into-module-outputs]

None

## Server Runnables 

None

## Interrupt Functions

None

## Module Internal (Local) Functions

None

## GLOBAL Function/Macro Definitions

None

# Known Limitations with Design

> The limits for all outputs in FDD v3.0.0 uses same Min and Max values
> which will cause PIL test coverage issue due to limit function.

# UNIT TEST CONSIDERATION

> The limits for all outputs in FDD v3.0.0 uses same Min and Max values
> which will cause PIL test coverage issue due to limit function.

<span id="__RefHeading___Toc511813662"
class="anchor"></span>Abbreviations and Acronyms

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

|         |                                                                              |                                |
|-------|----------------------------------------|-------------------------|
| Ref. \# | Title                                                                        | Version                        |
| 1       | AUTOSAR Specification of Memory Mapping (Link:AUTOSAR_SWS_MemoryMapping.pdf) | v1.3.0 R4.0 Rev 2              |
| 2       | MDD Guideline                                                                | EA4 01.00                      |
| 3       | Software Naming Conventions.doc                                              | EA4 01.02                      |
| 4       | Software Design and Coding Standards.doc                                     | EA4 2.01                       |
| 5       | FDD: MM519A_FordMsg5B5BusHiSpd_Design                                        | See Synergy subproject version |

{% endraw %}