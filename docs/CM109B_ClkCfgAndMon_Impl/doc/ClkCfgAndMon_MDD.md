---
layout: default
title: ClkCfgAndMon_MDD
nav_order: 2
parent: Component Implementation
---
{% raw %}
**Module Design Document**

**For**

**ClkCfgAndMon**

**21-Nov-2017**

**Prepared By:**

**Shruthi Raghavan,**

**Nexteer Automotive,**

**Saginaw, MI, USA  
<u>Change History</u>**

|                 |                  |             |             |
|-----------------|------------------|-------------|-------------|
| **Description** | **Author**       | **Version** | **Date**    |
| Initial Version | Shruthi Raghavan | 1.0         | 21-Nov-2017 |

**  
**

**<u>Table of Contents</u>**

[1 Introduction [4](#introduction)](#introduction)

[1.1 Purpose [4](#purpose)](#purpose)

[2 ClkCfgAndMon & High-Level Description
[5](#clkcfgandmon-high-level-description)](#clkcfgandmon-high-level-description)

[3 Design details of software module
[6](#design-details-of-software-module)](#design-details-of-software-module)

[3.1 Graphical representation of \<Component Name\>
[6](#graphical-representation-of-component-name)](#graphical-representation-of-component-name)

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

[5.1.1 Init: ClkCfgAndMonInit0
[8](#init-clkcfgandmoninit0)](#init-clkcfgandmoninit0)

[5.1.1.1 Design Rationale [8](#design-rationale)](#design-rationale)

[5.1.2 Periodic [8](#periodic)](#periodic)

[5.2 Server Runables [8](#server-runables)](#server-runables)

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

Module Design Document for CM109B (ClkCfgAndMon) Implementation. See
design for details.

# ClkCfgAndMon & High-Level Description

Refer FDD document.

# Design details of software module

## Graphical representation of \<Component Name\>

> <img
> src="ElectricPowerSteering_RH850_FORD_T3T6_website/docs/CM109B_ClkCfgAndMon_Impl/doc/mediax/media/image1.png"
> style="width:2.66855in;height:1.52629in" />

## Data Flow Diagram

### Component level DFD

> Refer FDD

### Function level DFD

> Refer FDD

# Constant Data Dictionary

## Program (fixed) Constants

### Embedded Constants

#### Local Constants

| Constant Name | Resolution | Units | Value |
|---------------|------------|-------|-------|
| \-            | \-         | \-    | \-    |

# Software Component Implementation

## Sub-Module Functions

## Init: ClkCfgAndMonInit0

## Design Rationale

*Non-RTE Init implemented as per FDD document directions.*

## Init: ClkCfgAndMonInit1

## Design Rationale

RTE Init for MemMap – Empty.

## Periodic

> None

## Server Runables 

> None

## Interrupt Functions

> None

## Module Internal (Local) Functions

|                      |     |      |     |     |
|----------------------|-----|------|-----|-----|
| **Function Name**    | \-  | Type | Min | Max |
| **Arguments Passed** | \-  | \-   | \-  | \-  |

## GLOBAL Function/Macro Definitions

None

# Known Limitations with Design

> None.

# UNIT TEST CONSIDERATION

> Register file definitions are in the P1Xc/include folder of AR202A
> since this component is designed for P1X-c micro.

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

| **\#** | **Title**                                                                                                                                                           | **Version**                    |
|----|------------------------------------------------|---------------------|
| 1      | AUTOSAR Specification of Memory Mapping                                                                                                                             | See Process 04.04.02           |
| 2      | MDD Guideline                                                                                                                                                       | See Process 04.04.02           |
| 3      | [Software Naming Conventions.doc](http://misagweb01.nexteer.com/eRoomReq/Files/erooms8/NextGeneration/0_fc55f/Software%20Naming%20Conventions%2003x(In%20Work).doc) | See Process 04.04.02           |
| 4      | Software Design and Coding Standards.doc                                                                                                                            | See Process 04.04.02           |
| 5      | FDD : CM109B_ClkCfgAndMon_Design                                                                                                                                    | See Synergy Subproject Version |

{% endraw %}