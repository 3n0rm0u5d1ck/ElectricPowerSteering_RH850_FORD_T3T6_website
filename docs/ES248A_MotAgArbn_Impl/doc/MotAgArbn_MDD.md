---
layout: default
title: MotAgArbn_MDD
nav_order: 2
parent: Component Implementation
---
{% raw %}
**Module Design Document**

**For**

**MotAgArbn**

**Sep** **29, 2017**

**Prepared By:**

**Shruthi Raghavan,**

**Nexteer Automotive,**

**Saginaw, MI, USA**

**<u>Change History</u>**

|                                                                                                |                  |             |             |
|------------------------------------------|-------------|--------|----------|
| **Description**                                                                                | **Author**       | **Version** | **Date**    |
| Initial Version                                                                                | SB               | 1.0         | 05-Aug-2015 |
| Updated per design vers. 1.2.0                                                                 | ML               | 2.0         | 15-Feb-2017 |
| Updated to remove the constants that have been renamed and added to DataDict.m file in design. | Shruthi Raghavan | 3.0         | 29-Sep-2017 |

**  
**

<u>Table of Contents</u>[1 Introduction
[4](#introduction)](#introduction)

[Purpose [4](#purpose)](#purpose)

[1.1 [4](#section-1)](#section-1)

[2 MotAgArbn & High-Level Description
[5](#motagarbn-high-level-description)](#motagarbn-high-level-description)

[3 Design details of software module
[6](#design-details-of-software-module)](#design-details-of-software-module)

[3.1 Graphical representation of MotAgArbn
[6](#graphical-representation-of-motagarbn)](#graphical-representation-of-motagarbn)

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

[5.1.1 Init: MotAgArbnInit1
[8](#init-motagarbninit1)](#init-motagarbninit1)

[5.1.1.1 Design Rationale [8](#design-rationale)](#design-rationale)

[5.1.1.2 Module Outputs [8](#module-outputs)](#module-outputs)

[5.1.2 Per: MotAgArbnPer1 [8](#per-motagarbnper1)](#per-motagarbnper1)

[5.1.2.1 Design Rationale [8](#design-rationale-1)](#design-rationale-1)

[5.2 Server Runables [8](#server-runables)](#server-runables)

[5.3 Interrupt Functions
[8](#interrupt-functions)](#interrupt-functions)

[5.4 Module Internal (Local) Functions
[8](#module-internal-local-functions)](#module-internal-local-functions)

[5.4.1 Local Function \#1 [8](#local-function-1)](#local-function-1)

[5.4.1.1 Design Rationale [8](#design-rationale-2)](#design-rationale-2)

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

## 

## 

Module design document for MotAgArbn

# MotAgArbn & High-Level Description

*Refer FDD.*

# Design details of software module

## Graphical representation of MotAgArbn 

<img
src="ElectricPowerSteering_RH850_FORD_T3T6_website/docs/ES248A_MotAgArbn_Impl/doc/mediax/media/image1.png"
style="width:1.875in;height:1.61458in" />

## Data Flow Diagram

Refer FDD

### Component level DFD

Refer FDD

### Function level DFD

Refer FDD

# Constant Data Dictionary

## Program (fixed) Constants

### Embedded Constants

#### Local Constants

| Constant Name | Resolution | Units | Value |
|---------------|------------|-------|-------|
| Refer .m file |            |       |       |
|               |            |       |       |
|               |            |       |       |

# Software Component Implementation

## Sub-Module Functions

## Init: MotAgArbnInit1

## Design Rationale

Init1 function is created so that it will allow a RTE model to be
created in the AUTOSAR tools which allows Per-Instance Memory and
calibration definition needs. The initialization function is doing
nothing

## Module Outputs

*None*

## Per: MotAgArbnPer1

## Design Rationale

*None*

## Server Runables 

None

## Interrupt Functions

*None*

## Module Internal (Local) Functions

## Local Function \#1

|                      |                            |          |               |               |
|--------------|------------------------------|---------|-----------|-----------|
| **Function Name**    | SigAvlyChk                 | Type     | Min           | Max           |
| **Arguments Passed** | SigCorrChk_Cnt_T_u08       | uint8    | 0U            | 2U            |
|                      | SigRollgCntr_Cnt_T_u08     | uint8    | 0U            | 255U          |
|                      | SigQlfr_Cnt_T_enum         | SigQlfr1 | SIGQLFR_NORES | SIGQLFR_FAILD |
|                      | \* PrevRollgCntr_Cnt_T_u08 | uint8    | 0U            | 255U          |
|                      | \* StallCnt_Cnt_T_u08      | uint8    | 0U            | 10U           |
| **Return Value**     | SigAvl_Cnt_T_lgc           | boolean  | FALSE         | TRUE          |

## Design Rationale

None

## GLOBAL Function/Macro Definitions

None

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

| **Ref. \#** | **Title**                                                                                                                                                               | **Version**                    |
|-------|-------------------------------------------------|-----------------|
| 1           | AUTOSAR Specification of Memory Mapping                                                                                                                                 | v1.3.0 R4.0 Rev 2              |
| 2           | MDD Guideline                                                                                                                                                           | EA4 01.00.01                   |
| 3           | EA4 [Software Naming Conventions.doc](http://misagweb01.nexteer.com/eRoomReq/Files/erooms8/NextGeneration/0_fc55f/Software%20Naming%20Conventions%2003x(In%20Work).doc) | EA4 01.01.00                   |
| 4           | [Software Design and Coding Standards.doc](http://eroom1.nexteer.com/eRoomReq/Files/erooms8/NextGeneration/0_1a67a9/Software%20Design%20and%20Coding%20Standards.doc)   | 2.1                            |
| 5           | FDD – ES248A_MotAgArbn_Design                                                                                                                                           | See Synergy Subproject verison |

{% endraw %}