---
layout: default
title: FordMsg417BusHiSpd_MDD
nav_order: 2
parent: Component Implementation
---
{% raw %}
**Module Design Document**

**For**

**FordMsg417BusHiSpd**

**Nov 30, 2017**

**Prepared For:**

**Software Engineering**

**Nexteer Automotive,**

**Saginaw, MI, USA**

**Prepared By:**

**Krishna Anne,**

**Nexteer Automotive,**

**Saginaw, MI, USA  
<u>Change History</u>**

|                 |              |             |             |
|-----------------|--------------|-------------|-------------|
| **Description** | **Author**   | **Version** | **Date**    |
| Initial version | Krishna Anne | 1.0         | 30-Nov-2017 |

**  
**

<u>Table of Contents</u>

[1 FordMsg417BusHiSpd High-Level Description
[4](#fordmsg417bushispd-high-level-description)](#fordmsg417bushispd-high-level-description)

[2 Design details of software module
[5](#design-details-of-software-module)](#design-details-of-software-module)

[2.1 Graphical representation of FordMsg417BusHiSpd
[5](#graphical-representation-of-fordmsg417bushispd)](#graphical-representation-of-fordmsg417bushispd)

[2.2 Data Flow Diagram [5](#data-flow-diagram)](#data-flow-diagram)

[2.2.1 Component level DFD
[5](#component-level-dfd)](#component-level-dfd)

[2.2.2 Function level DFD [5](#function-level-dfd)](#function-level-dfd)

[3 Constant Data Dictionary
[6](#constant-data-dictionary)](#constant-data-dictionary)

[3.1 Program (fixed) Constants
[6](#program-fixed-constants)](#program-fixed-constants)

[3.1.1 Embedded Constants [6](#embedded-constants)](#embedded-constants)

[4 Software Component Implementation
[7](#software-component-implementation)](#software-component-implementation)

[4.1 Sub-Module Functions
[7](#sub-module-functions)](#sub-module-functions)

[4.1.1 Init: FordMsg417BusHiSpdInit1
[7](#init-fordmsg417bushispdinit1)](#init-fordmsg417bushispdinit1)

[4.1.1.1 Design Rationale [7](#design-rationale)](#design-rationale)

[4.1.1.2 Module Outputs [7](#module-outputs)](#module-outputs)

[4.1.2 Init: FordMsg417BusHiSpdPer1
[7](#init-fordmsg417bushispdper1)](#init-fordmsg417bushispdper1)

[4.1.2.1 Design Rationale [7](#design-rationale-1)](#design-rationale-1)

[4.1.2.2 Module Outputs [7](#module-outputs-1)](#module-outputs-1)

[4.2 Server Runables [7](#server-runables)](#server-runables)

[4.3 Interrupt Functions
[7](#interrupt-functions)](#interrupt-functions)

[4.3.1 Interrupt Function Name
[7](#interrupt-function-name)](#interrupt-function-name)

[4.4 Module Internal (Local) Functions
[8](#module-internal-local-functions)](#module-internal-local-functions)

[4.4.1 Local Function \#1 [8](#_Toc479765169)](#_Toc479765169)

[4.4.1.1 Design Rationale [8](#_Toc479765170)](#_Toc479765170)

[4.4.1.2 Processing [8](#_Toc479765171)](#_Toc479765171)

[4.5 GLOBAL Function/Macro Definitions
[8](#global-functionmacro-definitions)](#global-functionmacro-definitions)

[5 Known Limitations with Design
[9](#known-limitations-with-design)](#known-limitations-with-design)

[6 UNIT TEST CONSIDERATION
[10](#unit-test-consideration)](#unit-test-consideration)

[Appendix A Abbreviations and Acronyms
[11](#abbreviations-and-acronyms)](#abbreviations-and-acronyms)

[Appendix B Glossary [12](#glossary)](#glossary)

[Appendix C Please references
[13](#please-references)](#please-references)

# FordMsg417BusHiSpd High-Level Description

Please refer FDD

# Design details of software module

Please refer FDD

## Graphical representation of FordMsg417BusHiSpd

<img
src="ElectricPowerSteering_RH850_FORD_T3T6_website/docs/MM518A_FordMsg417BusHiSpd_Impl/doc/mediax/media/image1.jpeg"
style="width:3.29861in;height:2.16389in" alt="MM518" />

## Data Flow Diagram

Please refer FDD

### Component level DFD

Please refer FDD

### Function level DFD

Please refer FDD

# Constant Data Dictionary

## Program (fixed) Constants

### Embedded Constants

#### Local Constants

| Constant Name                      | Resolution | Units | Value |
|------------------------------------|------------|-------|-------|
| Please refer .m file for constants |            |       |       |

# Software Component Implementation

## Sub-Module Functions

## Init: FordMsg417BusHiSpdInit1

## Design Rationale

Please refer FDD

## Module Outputs

None

## Init: FordMsg417BusHiSpdPer1

## Design Rationale

Please refer FDD.

## Module Outputs

None

## Server Runables 

None

## Interrupt Functions

None

## Interrupt Function Name

None

## Module Internal (Local) Functions

None

## GLOBAL Function/Macro Definitions

None

# Known Limitations with Design

None.

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

-   Automotive SPICE® Process Please reference Model (PRM)

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

####### Please references

| **Ref. \#** | **Title**                                                                                                                                                             | **Version**                    |
|-------|-------------------------------------------------|-----------------|
| 1           | AUTOSAR Specification of Memory Mapping (Link:[AUTOSAR_SWS_MemoryMapping.pdf](http://www.autosar.org/download/R4.0/AUTOSAR_SWS_MemoryMapping.pdf))                    | v1.3.0 R4.0 Rev 2              |
| 2           | MDD Guideline                                                                                                                                                         | EA4 01.00.00                   |
| 3           | [Software Naming Conventions.doc](http://misagweb01.nexteer.com/eRoomReq/Files/erooms8/NextGeneration/0_fc55f/Software%20Naming%20Conventions%2003x(In%20Work).doc)   | 2.0                            |
| 4           | [Software Design and Coding Standards.doc](http://eroom1.nexteer.com/eRoomReq/Files/erooms8/NextGeneration/0_1a67a9/Software%20Design%20and%20Coding%20Standards.doc) | 2.1                            |
| 5           | FDD: MM518A_FordMsg417BusHiSpd_Design                                                                                                                                 | See Synergy subproject version |

{% endraw %}