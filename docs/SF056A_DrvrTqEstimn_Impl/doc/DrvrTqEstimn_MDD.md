---
layout: default
title: DrvrTqEstimn_MDD
nav_order: 3
parent: Component Implementation
---
{% raw %}
**Module Design Document**

**For**

**DrvrTqEstimn**

**Feb 2, 2017**

**Prepared For:**

**Software Engineering**

**Nexteer Automotive,**

**Saginaw, MI, USA**

**Prepared By:**

**Matthew Leser**

**Software Engineering**

**Nexteer Automotive,**

**Saginaw, MI, USA**

**  
<u>Change History</u>**

|                 |               |             |             |
|-----------------|---------------|-------------|-------------|
| **Description** | **Author**    | **Version** | **Date**    |
| Initial Version | Matthew Leser | 1.0         | 02-Feb-2017 |

**  
**

<u>Table of Contents</u>

[1 Introduction [4](#introduction)](#introduction)

[1.1 Purpose [4](#purpose)](#purpose)

[2 DrvrTqEstimn & High-Level Description
[5](#drvrtqestimn-high-level-description)](#drvrtqestimn-high-level-description)

[3 Design details of software module
[6](#design-details-of-software-module)](#design-details-of-software-module)

[3.1 Graphical representation of DrvrTqEstimn
[6](#graphical-representation-of-drvrtqestimn)](#graphical-representation-of-drvrtqestimn)

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

[5.1.1 Init: DrvrTqEstimnInit1
[8](#init-drvrtqestimninit1)](#init-drvrtqestimninit1)

[5.1.1.1 Design Rationale [8](#design-rationale)](#design-rationale)

[5.1.1.2 Module Outputs [8](#module-outputs)](#module-outputs)

[5.1.2Per: DrvrTqEstimnPer1
[8](#per-drvrtqestimnper1)](#per-drvrtqestimnper1)

[5.1.1.3 Design Rationale [8](#design-rationale-1)](#design-rationale-1)

[5.1.1.4 Store Module Inputs to Local copies
[8](#store-module-inputs-to-local-copies)](#store-module-inputs-to-local-copies)

[5.1.1.5 (Processing of function)………
[8](#processing-of-function)](#processing-of-function)

[5.1.1.6 Store Local copy of outputs into Module Outputs
[8](#store-local-copy-of-outputs-into-module-outputs)](#store-local-copy-of-outputs-into-module-outputs)

[5.2 Server Runnables [8](#server-runnables)](#server-runnables)

[5.3 Interrupt Functions
[8](#interrupt-functions)](#interrupt-functions)

[5.4 Module Internal (Local) Functions
[8](#module-internal-local-functions)](#module-internal-local-functions)

[5.4.1.1 Design Rationale [8](#design-rationale-2)](#design-rationale-2)

[5.4.1.2 Processing [8](#processing)](#processing)

[5.5 GLOBAL Function/Macro Definitions
[8](#global-functionmacro-definitions)](#global-functionmacro-definitions)

[6 Known Limitations with Design
[10](#known-limitations-with-design)](#known-limitations-with-design)

[7 UNIT TEST CONSIDERATION
[11](#unit-test-consideration)](#unit-test-consideration)

[Appendix A Abbreviations and Acronyms
[12](#abbreviations-and-acronyms)](#abbreviations-and-acronyms)

[Appendix B Glossary [13](#glossary)](#glossary)

[Appendix C References [14](#references)](#references)

# Introduction

## Purpose

MDD for Driver Torque Estimation.

# DrvrTqEstimn & High-Level Description

Please refer FDD.

# Design details of software module

## Graphical representation of DrvrTqEstimn

<img
src="ElectricPowerSteering_RH850_FORD_T3T6_website/docs/SF056A_DrvrTqEstimn_Impl/doc/mediax/media/image1.png"
style="width:1.85168in;height:3.69657in" />

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

### 5.1.1 Init: DrvrTqEstimnInit1 [init-drvrtqestimninit1]

## Design Rationale

None

## Module Outputs

None

### 5.1.2Per: DrvrTqEstimnPer1 [per-drvrtqestimnper1]

## Design Rationale

None

## Store Module Inputs to Local copies

None

##  (Processing of function)………

Please refer FDD

## Store Local copy of outputs into Module Outputs

Please refer FDD

## Server Runnables 

None

## Interrupt Functions

None

## Module Internal (Local) Functions

## Design Rationale

None.

## Processing

None.

## GLOBAL Function/Macro Definitions

None.

# Known Limitations with Design

None.

# UNIT TEST CONSIDERATION

None.

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
| 5           | FDD : SF056A_DrvrTqEstimn_Design                                                                                                                                      | See Synergy Sub-project version |

{% endraw %}