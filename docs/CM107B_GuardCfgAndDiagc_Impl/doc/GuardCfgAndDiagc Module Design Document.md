---
layout: default
title: GuardCfgAndDiagc Module Design Document
nav_order: 2
parent: Component Implementation
---
{% raw %}
**Module Design Document**

**For**

**GuardCfgAndDiagc**

**Nov 12 , 2017**

**Prepared For:**

**Software Engineering**

**Nexteer Automotive,**

**Saginaw, MI, USA**

**Prepared By:**

**Software Group,**

**Nexteer Automotive,**

**Saginaw, MI, USA  
<u>Change History</u>**

|                 |               |             |          |
|-----------------|---------------|-------------|----------|
| **Description** | **Author**    | **Version** | **Date** |
| Initial Version | Avinash James | 1.0         | 11/12/17 |
|                 |               |             |          |

**  
**

**<u>Table of Contents</u>**

[1 Introduction [5](#introduction)](#introduction)

[1.1 Purpose [5](#purpose)](#purpose)

[1.2 Scope [5](#scope)](#scope)

[2 GuardCfgAndDiagc & High-Level Description
[6](#guardcfganddiagc-high-level-description)](#guardcfganddiagc-high-level-description)

[3 Design details of software module
[7](#design-details-of-software-module)](#design-details-of-software-module)

[3.1 Graphical representation of GuardCfgAndDiagc
[7](#graphical-representation-of-guardcfganddiagc)](#graphical-representation-of-guardcfganddiagc)

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

[5.1.1 Init: GuardCfgAndDiagcInit1
[9](#init-guardcfganddiagcinit1)](#init-guardcfganddiagcinit1)

[5.1.1.1 Design Rationale [9](#design-rationale)](#design-rationale)

[5.1.1.2 Module Outputs [9](#module-outputs)](#module-outputs)

[5.1.2 Init: GuardCfgAndDiagcInit2
[9](#init-guardcfganddiagcinit2)](#init-guardcfganddiagcinit2)

[5.1.2.1 Design Rationale [9](#design-rationale-1)](#design-rationale-1)

[5.1.2.2 Module Outputs [9](#module-outputs-1)](#module-outputs-1)

[5.1.3 Per: None [9](#per-none)](#per-none)

[5.2 Server Runables [9](#server-runables)](#server-runables)

[5.3 Interrupt Functions
[9](#interrupt-functions)](#interrupt-functions)

[5.4 Module Internal (Local) Functions
[9](#module-internal-local-functions)](#module-internal-local-functions)

[5.4.1 PegInin [9](#peginin)](#peginin)

[5.4.1.1 Design Rationale [9](#design-rationale-2)](#design-rationale-2)

[5.4.1.2 Processing [9](#processing)](#processing)

[5.4.2 PbgInin [10](#pbginin)](#pbginin)

[5.4.2.1 Design Rationale
[10](#design-rationale-3)](#design-rationale-3)

[5.4.2.2 Processing [10](#processing-1)](#processing-1)

[5.4.3 FrGuardInin [10](#_Toc498278450)](#_Toc498278450)

[5.4.3.1 Design Rationale
[10](#design-rationale-4)](#design-rationale-4)

[5.4.3.2 Processing [10](#processing-2)](#processing-2)

[5.4.4 GlbRamGuardInin [10](#glbramguardinin)](#glbramguardinin)

[5.4.4.1 Design Rationale
[10](#design-rationale-5)](#design-rationale-5)

[5.4.4.2 Processing [10](#processing-3)](#processing-3)

[5.5 GLOBAL Function/Macro Definitions
[10](#global-functionmacro-definitions)](#global-functionmacro-definitions)

[5.5.1 GLOBAL Function \#1 [10](#global-function-1)](#global-function-1)

[5.5.1.1 Design Rationale
[11](#design-rationale-6)](#design-rationale-6)

[5.5.1.2 Processing [11](#processing-4)](#processing-4)

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

## Scope

The following definitions are used throughout this document:

-   **<u>Shall</u>**: indicates a mandatory requirement without
    exception in compliance.

-   **<u>Should</u>**: indicates a mandatory requirement; exceptions
    allowed only with documented justification.

-   **<u>May</u>**: indicates an optional action.

# GuardCfgAndDiagc & High-Level Description

*See FDD*

# Design details of software module

## Graphical representation of GuardCfgAndDiagc

<img
src="ElectricPowerSteering_RH850_FORD_T3T6_website/docs/CM107B_GuardCfgAndDiagc_Impl/doc/mediax/media/image1.jpg"
style="width:2.40833in;height:1.475in" />

## Data Flow Diagram

### Component level DFD

*See FDD*

### Function level DFD

*See FDD*

# Constant Data Dictionary

## Program (fixed) Constants

### Embedded Constants

#### Local Constants

| Constant Name                       | Resolution | Units      | Value            |
|---------------------------------|---------------|-----------|-------------|
| **PROTNLOCKENA_CNT_U32**            | **1**      | **uint32** | **0x80000000UL** |
| **GLBRAMGUARDENA_CNT_U32**          | **1**      | **uint32** | **0x40000000UL** |
| **GLBRAMGUARDRSTVAL_CNT_U32**       | **1**      | **uint32** | **0x07FFFE10UL** |
| **GLBRAMGUARD0BASADRREG_CNT_U32**   | **1**      | **uint32** | **0x00027E00UL** |
| **GLBRAMGUARD0VALADRREG_CNT_U32**   | **1**      | **uint32** | **0x00000000UL** |
| **SPID0_CNT_U32**                   | **1**      | **uint32** | **0x00000001UL** |
| **SPID1_CNT_U32**                   | **1**      | **uint32** | **0x00000002UL** |
| **SPID2_CNT_U32**                   | **1**      | **uint32** | **0x00000004UL** |
| **SPID3_CNT_U32**                   | **1**      | **uint32** | **0x00000008UL** |
| **SPID4_CNT_U32**                   | **1**      | **uint32** | **0x00000010UL** |
| **SPID5_CNT_U32**                   | **1**      | **uint32** | **0x00000020UL** |
| **SPID6_CNT_U32**                   | **1**      | **uint32** | **0x00000040UL** |
| **SPID7_CNT_U32**                   | **1**      | **uint32** | **0x00000080UL** |
| **ALLSPIDDI_CNT_U32**               | **1**      | **uint32** | **0x00000000UL** |
| **HISPDBUSGUARDREADENAPE1_CNT_U32** | **1**      | **uint32** | **0x0605FE1BUL** |
| **HISPDBUSGUARDWRENAPE1_CNT_U32**   | **1**      | **uint32** | **0x0605FE17UL** |
| **PBGREADENAPE1_CNT_U32**           | **1**      | **uint32** | **0x0605FE1BUL** |
| **PBGWRENAPE1_CNT_U32**             | **1**      | **uint32** | **0x0605FE17UL** |
| **PBGREADENAPE1ANDPE4_CNT_U32**     | **1**      | **uint32** | **0x0625FE1BUL** |
| **PBGWRENAPE1ANDPE4_CNT_U32**       | **1**      | **uint32** | **0x0625FE17UL** |
| **PBGREADALLPEDI_CNT_U32**          | **1**      | **uint32** | **0x0601FE1BUL** |
| **PBGWRALLPEDI_CNT_U32**            | **1**      | **uint32** | **0x0601FE17UL** |

# Software Component Implementation

## Sub-Module Functions

### Init: GuardCfgAndDiagcInit1

## Design Rationale

*Non-RTE function for Guard configuration initialization of PEG, IPG,
GRG,HBG and PBG so that guard protection can be initialized and enabled
before the RTE is started*

## Module Outputs

*Configuration registers for PEG, IPG,GRG,HRG and PBG*

### Init: GuardCfgAndDiagcInit2

## Design Rationale

*RTE Empty function for purposes of memory mapping*

*See FDD for more.*

## Module Outputs

*None*

## Per: None

## Server Runables 

*None*

## Interrupt Functions

*None*

## Module Internal (Local) Functions

### PegInin

|                      |         |      |     |     |
|----------------------|---------|------|-----|-----|
| **Function Name**    | PegInin | Type | Min | Max |
| **Arguments Passed** | None    | \-   | \-  | \-  |
| **Return Value**     | None    | \-   | \-  | \-  |

## Design Rationale

Sub function to set Peg Register configuration.

## Processing

None

### PbgInin

|                      |         |      |     |     |
|----------------------|---------|------|-----|-----|
| **Function Name**    | PbgInin | Type | Min | Max |
| **Arguments Passed** | None    | \-   | \-  | \-  |
| **Return Value**     | None    | \-   | \-  | \-  |

## Design Rationale

Sub function to set PBG Register configuration.

## Processing

None

### HiSpdBusGuardInin

|                      |                   |      |     |     |
|----------------------|-------------------|------|-----|-----|
| **Function Name**    | HiSpdBusGuardInin | Type | Min | Max |
| **Arguments Passed** | None              | \-   | \-  | \-  |
| **Return Value**     | None              | \-   | \-  | \-  |

## Design Rationale

Sub function to set HBG Register configuration.

## Processing

None

### GlbRamGuardInin

|                      |                 |      |     |     |
|----------------------|-----------------|------|-----|-----|
| **Function Name**    | GlbRamGuardInin | Type | Min | Max |
| **Arguments Passed** | None            | \-   | \-  | \-  |
| **Return Value**     | None            | \-   | \-  | \-  |

## Design Rationale

Sub function to set GRG Register configuration.

## Processing

None

## GLOBAL Function/Macro Definitions

## GLOBAL Function \#1

|                      |     |      |     |     |
|----------------------|-----|------|-----|-----|
| **Function Name**    |     | Type | Min | Max |
| **Arguments Passed** |     |      |     |     |
|                      |     |      |     |     |
| **Return Value**     |     |      |     |     |

## Design Rationale

## Processing

# Known Limitations with Design

None

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

| **Ref. \#** | **Title**                                                                                                                                                             | **Version**       |
|-------|-------------------------------------------------|-----------------|
| 1           | AUTOSAR Specification of Memory Mapping (Link:[AUTOSAR_SWS_MemoryMapping.pdf](http://www.autosar.org/download/R4.0/AUTOSAR_SWS_MemoryMapping.pdf))                    | v1.3.0 R4.0 Rev 2 |
| 2           | MDD Guideline                                                                                                                                                         | EA4 01.00.01      |
| 3           | [Software Naming Conventions.doc](http://misagweb01.nexteer.com/eRoomReq/Files/erooms8/NextGeneration/0_fc55f/Software%20Naming%20Conventions%2003x(In%20Work).doc)   | 2.0               |
| 4           | [Software Design and Coding Standards.doc](http://eroom1.nexteer.com/eRoomReq/Files/erooms8/NextGeneration/0_1a67a9/Software%20Design%20and%20Coding%20Standards.doc) | 2.1               |

{% endraw %}