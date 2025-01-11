---
layout: default
title: FordMsg07EBusHiSpd_MDD
nav_order: 2
parent: Component Implementation
---
{% raw %}
**Module Design Document**

**For**

**FordMsg07EBusHiSpd**

**28-Mar-2018**

**Prepared For:**

**Software Engineering**

**Nexteer Automotive,**

**Saginaw, MI, USA**

**Prepared By:**

**Tata Elxsi,**

**Trivandrum, INDIA**

**<u>Change History</u>**

|                                          |        |         |             |
|------------------------------------------|--------|---------|-------------|
| Description                              | Author | Version | Date        |
| Initial Version                          | TATA   | 1.0     | 21-Nov-2017 |
| Updated DaVinci graphical representation | TATA   | 2.0     | 28-Mar-2018 |

<u>Table of Contents</u>

[1 Introduction 4](#introduction)

[1.1 Purpose 4](#purpose)

[2 FordMsg07EBusHiSpd & High-Level Description
5](#fordmsg07ebushispd-high-level-description)

[3 Design details of software module
6](#design-details-of-software-module)

[3.1 Graphical representation of FordMsg07EBusHiSpd
6](#graphical-representation-of-fordmsg07ebushispd)

[3.2 Data Flow Diagram 6](#data-flow-diagram)

[3.2.1 Component level DFD 6](#component-level-dfd)

[3.2.2 Function level DFD 6](#function-level-dfd)

[4 Constant Data Dictionary 7](#constant-data-dictionary)

[4.1 Program (fixed) Constants 7](#program-fixed-constants)

[4.1.1 Embedded Constants 7](#embedded-constants)

[5 Software Component Implementation
8](#software-component-implementation)

[5.1 Sub-Module Functions 8](#sub-module-functions)

[5.1.1 Init: FordMsg07EBusHiSpdInit1 8](#init-fordmsg07ebushispdinit1)

[5.1.1.1 Design Rationale 8](#design-rationale)

[5.1.1.2 Module Outputs 8](#module-outputs)

[5.1.2 Per: FordMsg07EBusHiSpdPer1 8](#per-fordmsg07ebushispdper1)

[5.1.2.1 Design Rationale 8](#design-rationale-1)

[5.1.2.2 Store Module Inputs to Local copies
8](#store-module-inputs-to-local-copies)

[5.1.2.3 Processing of function)……… 8](#processing-of-function)

[5.1.2.4 Store Local copy of outputs into Module Outputs
8](#store-local-copy-of-outputs-into-module-outputs)

[5.2 Server Runables 8](#server-runnables)

[5.3 Interrupt Functions 8](#interrupt-functions)

[5.4 Module Internal (Local) Functions
8](#module-internal-local-functions)

[5.5 GLOBAL Function/Macro Definitions
8](#global-functionmacro-definitions)

[6 Known Limitations with Design 9](#known-limitations-with-design)

[7 UNIT TEST CONSIDERATION 10](#unit-test-consideration)

[Appendix A Abbreviations and Acronyms 11](#abbreviations-and-acronyms)

[Appendix B Glossary 12](#glossary)

[Appendix C References 13](#references)

# Introduction

## Purpose

MDD for FordMsg07EBusHiSpd

# FordMsg07EBusHiSpd & High-Level Description

Please refer FDD.

# Design details of software module

## Graphical representation of FordMsg07EBusHiSpd

<img
src="ElectricPowerSteering_RH850_FORD_T3T6_website/docs/MM531A_FordMsg07EBusHiSpd_Impl/doc/mediax/media/image2.png"
style="width:4.50069in;height:3.83403in" />

## Data Flow Diagram

### Component level DFD

Please refer FDD.

### Function level DFD

Please refer FDD.

# Constant Data Dictionary

## Program (fixed) Constants

### Embedded Constants

#### Local Constants

|                                      |            |       |       |     |
|--------------------------------------|------------|-------|-------|-----|
|                                      |            |       |       |     |
|                                      |            |       |       |     |
| Constant Name                        | Resolution | Units | Value |     |
| Please refer Data Dictionary .m file | NA         | NA    | NA    |     |

# Software Component Implementation

## Sub-Module Functions

### 5.1.1 Init: FordMsg07EBusHiSpdInit1 [init-fordmsg07ebushispdinit1]

## Design Rationale

None

## Module Outputs

None

### 5.1.2 Per: FordMsg07EBusHiSpdPer1 [per-fordmsg07ebushispdper1]

## 5.1.2.1 Design Rationale [design-rationale-1]

None

## 5.1.2.2 Store Module Inputs to Local copies [store-module-inputs-to-local-copies]

None

## 5.1.2.3 Processing of function)……… [processing-of-function]

None

## 5.1.2.4 Store Local copy of outputs into Module Outputs [store-local-copy-of-outputs-into-module-outputs]

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

|         |                                                                              |                                |
|-------|-------------------------------------------------|-----------------|
|         |                                                                              |                                |
|         |                                                                              |                                |
|         |                                                                              |                                |
|         |                                                                              |                                |
|         |                                                                              |                                |
| Ref. \# | Title                                                                        | Version                        |
| 1       | AUTOSAR Specification of Memory Mapping (Link:AUTOSAR_SWS_MemoryMapping.pdf) | v1.3.0 R4.0 Rev 2              |
| 2       | MDD Guideline                                                                | EA4 01.00                      |
| 3       | Software Naming Conventions.doc                                              | EA4 01.02                      |
| 4       | Software Design and Coding Standards.doc                                     | EA4 2.01                       |
| 5       | FDD: MM531A_FordMsg07EBusHiSpd_Design                                        | See Synergy subproject version |

{% endraw %}