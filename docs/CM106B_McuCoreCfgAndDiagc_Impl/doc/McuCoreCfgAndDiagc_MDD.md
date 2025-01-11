---
layout: default
title: McuCoreCfgAndDiagc_MDD
nav_order: 2
parent: Component Implementation
---
{% raw %}
**Module Design Document**

**For**

**McuCoreCfgAndDiagc**

**08-Nov-2017**

**Prepared By:**

**Shruthi Raghavan,**

**Nexteer Automotive,**

**Saginaw, MI, USA  
<u>Change History</u>**

|                 |                  |             |             |
|-----------------|------------------|-------------|-------------|
| **Description** | **Author**       | **Version** | **Date**    |
| Initial Version | Shruthi Raghavan | 1.0         | 08-Nov-2017 |

**  
**

**<u>Table of Contents</u>**

[1 Introduction [4](#introduction)](#introduction)

[1.1 Purpose [4](#purpose)](#purpose)

[2 McuCoreCfgAndDiagc & High-Level Description
[5](#mcucorecfganddiagc-high-level-description)](#mcucorecfganddiagc-high-level-description)

[3 Design details of software module
[6](#design-details-of-software-module)](#design-details-of-software-module)

[3.1 Graphical representation of McuCoreCfgAndDiagc
[6](#graphical-representation-of-mcucorecfganddiagc)](#graphical-representation-of-mcucorecfganddiagc)

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

[5.1.1 Init: McuCoreCfgAndDiagcInit1
[8](#init-mcucorecfganddiagcinit1)](#init-mcucorecfganddiagcinit1)

[5.1.1.1 Design Rationale [8](#design-rationale)](#design-rationale)

[5.1.2 Init: McuCoreCfgAndDiagcInit2
[8](#init-mcucorecfganddiagcinit2)](#init-mcucorecfganddiagcinit2)

[5.1.2.1 Design Rationale [8](#design-rationale-1)](#design-rationale-1)

[5.1.3 Per: \<Component Name\>\_Per\<n\>
[8](#per-component-name_pern)](#per-component-name_pern)

[5.1.3.1 Design Rationale [8](#design-rationale-2)](#design-rationale-2)

[5.2 Server Runables [8](#server-runables)](#server-runables)

[5.2.1 \<Server Runable Name\>
[8](#server-runable-name)](#server-runable-name)

[5.2.1.1 Design Rationale [8](#design-rationale-3)](#design-rationale-3)

[5.3 Interrupt Functions
[8](#interrupt-functions)](#interrupt-functions)

[5.3.1 Interrupt Function Name
[8](#interrupt-function-name)](#interrupt-function-name)

[5.3.1.1 Design Rationale [8](#design-rationale-4)](#design-rationale-4)

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

Module design document for McuCoreCfgAndDiagc SWC.

# McuCoreCfgAndDiagc & High-Level Description

Refer FDD description.

# Design details of software module

## Graphical representation of McuCoreCfgAndDiagc

> <img
> src="ElectricPowerSteering_RH850_FORD_T3T6_website/docs/CM106B_McuCoreCfgAndDiagc_Impl/doc/mediax/media/image1.png"
> style="width:2.13322in;height:1.90081in" />

## Data Flow Diagram

### Component level DFD

> Refer FDD

### Function level DFD

> Refer FDD

# Constant Data Dictionary

## Program (fixed) Constants

### Embedded Constants

#### Local Constants

| Constant Name                     | Resolution | Units | Value       |
|-----------------------------------|------------|-------|-------------|
| FIEBISTCTRLCIRCTRFERRMASK_CNT_U32 | 1          | Cnt   | 0x00080000U |

# Software Component Implementation

## Sub-Module Functions

## Init: McuCoreCfgAndDiagcInit1

## Design Rationale

None

## Init: McuCoreCfgAndDiagcInit2

## Design Rationale

Empty RTE Init function for software memory map.

## Per: \<Component Name\>\_Per\<n\>

## Design Rationale

N/A

## Server Runables 

## \<Server Runable Name\>

## Design Rationale

N/A

## Interrupt Functions

## Interrupt Function Name

> None.

## Design Rationale

N/A

## Module Internal (Local) Functions

> None

## GLOBAL Function/Macro Definitions

> None

# Known Limitations with Design

None.

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

| **Ref. \#** | **Title**                                     | **Version**                    |
|-------|--------------------------------------------|----------------------|
| 1           | AUTOSAR Specification of Memory Mapping       | v1.3.0 R4.0 Rev 2              |
| 2           | MDD Guideline EA4 01.00.01.docx               | EA4 01.00.01                   |
| 3           | EA4 Software Naming Conventions 01.01.00.docx | 01.01.00                       |
| 4           | Software Design and Coding Standards 2.1.doc  | 2.1                            |
| 5           | FDD : CM106B_McuCoreCfgAndDiagc_Design        | See Synergy Subproject Version |

{% endraw %}