---
layout: default
title: Adcf0CfgAndUse_MDD
nav_order: 2
parent: Component Implementation
---
{% raw %}
**Module Design Document**

**For**

**Adcf0CfgAndUse**

**May 25, 2017**

**Prepared For:**

**Software Engineering**

**Nexteer Automotive,**

**Saginaw, MI, USA**

**Prepared By:**

**Mateusz Bartocha,**

**Nexteer Automotive,**

**Saginaw, MI, USA  
<u>Change History</u>**

|                 |             |             |             |
|-----------------|-------------|-------------|-------------|
| **Description** | **Author**  | **Version** | **Date**    |
| Initial Version | M. Bartocha | 1.0         | 25-May-2017 |

**  
**

**<u>Table of Contents</u>**

[1 Introduction [4](#introduction)](#introduction)

[2 CM301A_Adcf0CfgAndUse & High-Level Description
[5](#cm301a_adcf0cfganduse-high-level-description)](#cm301a_adcf0cfganduse-high-level-description)

[3 Design details of software module
[6](#design-details-of-software-module)](#design-details-of-software-module)

[3.1 Graphical representation of CM301A_Adcf0CfgAndUse
[6](#_Toc484086655)](#_Toc484086655)

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

[5.1.1 Init: Adcf0CfgAndUse_Init1
[8](#init-adcf0cfganduse_init1)](#init-adcf0cfganduse_init1)

[5.1.1.1 Design Rationale [8](#design-rationale)](#design-rationale)

[5.1.1.2 Module Outputs [8](#module-outputs)](#module-outputs)

[5.1.2 Per: Adcf0CfgAndUse_Per1
[8](#per-adcf0cfganduse_per1)](#per-adcf0cfganduse_per1)

[5.1.2.1 Design Rationale [8](#design-rationale-1)](#design-rationale-1)

[5.1.2.2 Store Module Inputs to Local copies
[8](#store-module-inputs-to-local-copies)](#store-module-inputs-to-local-copies)

[5.1.2.3 (Processing of function)………
[8](#processing-of-function)](#processing-of-function)

[5.1.2.4 Store Local copy of outputs into Module Outputs
[8](#store-local-copy-of-outputs-into-module-outputs)](#store-local-copy-of-outputs-into-module-outputs)

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

*None*

# CM301A_Adcf0CfgAndUse & High-Level Description

*None*

# Design details of software module

## Graphical representation of CM301A_Adcf0CfgAndUse

<img
src="ElectricPowerSteering_RH850_FORD_T3T6_website/docs/CM301A_Adcf0CfgAndUse_Impl/doc/mediax/media/image1.JPG"
style="width:2.44167in;height:1.89167in" />

## Data Flow Diagram

### Component level DFD

### Function level DFD

# Constant Data Dictionary

## Program (fixed) Constants

### Embedded Constants

#### Local Constants

| Constant Name                             | Resolution | Units | Value |
|-------------------------------------------|------------|-------|-------|
| Refer to the DataDictionary of the design |            |       |       |

# Software Component Implementation

*Refer to FDD.*

## Sub-Module Functions

## Init: Adcf0CfgAndUse_Init1

## Design Rationale

*None*

## Module Outputs

*Refer to FDD.*

###  [section]

## Per: Adcf0CfgAndUse_Per1

## Design Rationale

*None*

## Store Module Inputs to Local copies

*Refer to FDD.*

##  (Processing of function)………

*Refer to FDD.*

## Store Local copy of outputs into Module Outputs

*Refer to FDD.*

## Server Runables 

*None*

## Interrupt Functions

*None*

## Module Internal (Local) Functions

*None*

## GLOBAL Function/Macro Definitions

*None*

# Known Limitations with Design

*None*

# UNIT TEST CONSIDERATION

*None*

####### Abbreviations and Acronyms

|     |     |
|-----|-----|
|     |     |
|     |     |

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

| **Ref. \#** | **Title**                                                                                                                                                               | **Version**       |
|-------|-------------------------------------------------|-----------------|
| 1           | AUTOSAR Specification of Memory Mapping                                                                                                                                 | v1.3.0 R4.0 Rev 2 |
| 2           | MDD Guideline                                                                                                                                                           | EA4 01.00.00      |
| 3           | EA4 [Software Naming Conventions.doc](http://misagweb01.nexteer.com/eRoomReq/Files/erooms8/NextGeneration/0_fc55f/Software%20Naming%20Conventions%2003x(In%20Work).doc) | 1.0.0             |
| 4           | Software Design and Coding Standards.doc                                                                                                                                | 2.1               |

{% endraw %}