---
layout: default
title: MotRplCoggCmd_MDD
nav_order: 2
parent: Component Implementation
---
{% raw %}
**Module Design Document**

**For**

**MotRplCoggCmd**

**Mar 23, 2017**

**Prepared For:**

**Software Engineering**

**Nexteer Automotive,**

**Saginaw, MI, USA**

**Prepared By:**

**Software** **Engineering**

**Nexteer Automotive,**

**Saginaw, MI, USA  
****<u>Change History</u>**

|             |                                 |                    |             |
|---------------------|---------------------|------------------|-------------|
| **Version** | **Description**                 | **Author**         | **Date**    |
| 1           | Initial Version                 | Selva Sengottaiyan | 09-Feb-2016 |
| 2           | Updated Unit Test consideration | Avinash James      | 23-Mar-2017 |

**  
**

**<u>Table of Contents</u>**

[1 Introduction [5](#introduction)](#introduction)

[2 MotRplCoggCmd & High-Level Description
[6](#motrplcoggcmd-high-level-description)](#motrplcoggcmd-high-level-description)

[3 Design details of software module
[7](#design-details-of-software-module)](#design-details-of-software-module)

[3.1 Graphical representation of MotRplCoggCmd
[7](#graphical-representation-of-motrplcoggcmd)](#graphical-representation-of-motrplcoggcmd)

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

[5.1.1 Init: MotRplCoggCmdInit1
[9](#init-motrplcoggcmdinit1)](#init-motrplcoggcmdinit1)

[5.1.1.1 Design Rationale [9](#design-rationale)](#design-rationale)

[5.1.1.2 Module Outputs [9](#module-outputs)](#module-outputs)

[5.1.2 Per: MotRplCoggCmdPer1
[9](#per-motrplcoggcmdper1)](#per-motrplcoggcmdper1)

[5.1.2.1 Design Rationale [9](#design-rationale-1)](#design-rationale-1)

[5.1.2.2 Store Module Inputs to Local copies
[9](#store-module-inputs-to-local-copies)](#store-module-inputs-to-local-copies)

[5.1.2.3 (Processing of function)………
[9](#processing-of-function)](#processing-of-function)

[5.1.2.4 Store Local copy of outputs into Module Outputs
[9](#store-local-copy-of-outputs-into-module-outputs)](#store-local-copy-of-outputs-into-module-outputs)

[5.2 Server Runables [9](#server-runables)](#server-runables)

[5.2.1 GetMotCoggCmdPrm_Oper
[9](#getmotcoggcmdprm_oper)](#getmotcoggcmdprm_oper)

[5.2.1.1 Design Rationale [9](#design-rationale-2)](#design-rationale-2)

[5.2.1.2 Store Module Inputs to Local copies
[10](#store-module-inputs-to-local-copies-1)](#store-module-inputs-to-local-copies-1)

[5.2.1.3 (Processing of function)………
[10](#processing-of-function-1)](#processing-of-function-1)

[5.2.1.4 Store Local copy of outputs into Module Outputs
[10](#store-local-copy-of-outputs-into-module-outputs-1)](#store-local-copy-of-outputs-into-module-outputs-1)

[5.2.1 SetMotCoggCmdPrm_Oper
[10](#setmotcoggcmdprm_oper)](#setmotcoggcmdprm_oper)

[5.2.1.1 Design Rationale
[10](#design-rationale-3)](#design-rationale-3)

[5.2.1.2 Store Module Inputs to Local copies
[10](#store-module-inputs-to-local-copies-2)](#store-module-inputs-to-local-copies-2)

[5.2.1.3 (Processing of function)………
[10](#processing-of-function-2)](#processing-of-function-2)

[5.2.1.4 Store Local copy of outputs into Module Outputs
[10](#store-local-copy-of-outputs-into-module-outputs-2)](#store-local-copy-of-outputs-into-module-outputs-2)

[5.3 Module Internal (Local) Functions
[10](#module-internal-local-functions)](#module-internal-local-functions)

[5.3.1 Local Function \#1 [10](#local-function-1)](#local-function-1)

[5.3.1.1 Design Rationale
[10](#design-rationale-4)](#design-rationale-4)

[5.3.1.2 Processing [10](#processing)](#processing)

[6 Known Limitations with Design
[11](#known-limitations-with-design)](#known-limitations-with-design)

[7 UNIT TEST CONSIDERATION
[12](#unit-test-consideration)](#unit-test-consideration)

[Appendix A Abbreviations and Acronyms
[13](#abbreviations-and-acronyms)](#abbreviations-and-acronyms)

[Appendix B Glossary [14](#glossary)](#glossary)

[Appendix C References [15](#references)](#references)

# Introduction

Refer the Design Subproject.

# MotRplCoggCmd & High-Level Description

Refer the Design Subproject.

# Design details of software module

## Graphical representation of MotRplCoggCmd

Refer the Design Subproject.

<img
src="ElectricPowerSteering_RH850_FORD_T3T6_website/docs/SF107A_MotRplCoggCmd_Impl/doc/mediax/media/image1.png"
style="width:3.85in;height:1.41667in" />

## Data Flow Diagram

### Component level DFD

### Function level DFD

# Constant Data Dictionary

## Program (fixed) Constants

### Embedded Constants

#### Local Constants

| Constant Name                | Resolution                   | Units                        | Value                        |
|---------------------------------|---------------|-----------|-------------|
| Refer the Design Subproject. | Refer the Design Subproject. | Refer the Design Subproject. | Refer the Design Subproject. |

# Software Component Implementation

\<The detailed design of the function is provided in the FDD. The detail
design shall only be added to the MDD when it is not provided in the FDD
or the FDD is not adequate and clarification is needed.\>

## Sub-Module Functions

The sub-module functions are grouped based on similar functionality that
needs to be executed in a given “State” of the system (refer States and
Modes). For a given module, the MDD will identify the type and number of
sub-modules required. The sub-module types are described below.

*\<(Note: For multiple init or per functions, insert new headers at the
“Header 3” level – subset of “Sub-Module Functions section above” and
follow the same sub-section design shown below . If none required, place
the text “None”))\>*

## Init: MotRplCoggCmdInit1

## Design Rationale

Refer the Design Subproject

## Module Outputs

Refer the Design Subproject

###  [section]

## Per: MotRplCoggCmdPer1

## Design Rationale

Refer the Design Subproject*-* ARCHGLBPRM_ONEOVER2PI constant has been
used from ArchGlbPrm.h file instead of ONEOVER2PI which is defined in
the FDD

## Store Module Inputs to Local copies

Refer the Design Subproject

##  (Processing of function)………

Refer the Design Subproject

## Store Local copy of outputs into Module Outputs

Refer the Design Subproject

## Server Runables 

### GetMotCoggCmdPrm_Oper

## Design Rationale

Refer the Design Subproject

## Store Module Inputs to Local copies

Refer the Design Subproject

##  (Processing of function)………

Refer the Design Subproject

## Store Local copy of outputs into Module Outputs

Refer the Design Subproject

### SetMotCoggCmdPrm_Oper

## Design Rationale

Refer the Design Subproject

## Store Module Inputs to Local copies

Refer the Design Subproject

##  (Processing of function)………

Refer the Design Subproject

## Store Local copy of outputs into Module Outputs

Refer the Design Subproject

## Module Internal (Local) Functions

## Local Function \#1

|                      |                  |         |     |       |
|----------------------|------------------|---------|-----|-------|
| **Function Name**    | SinLookup        | Type    | Min | Max   |
| **Arguments Passed** | Theta_Rad_T_f32  | Float32 | 0   | 2\*PI |
|                      |                  |         |     |       |
| **Return Value**     | Result_Uls_T_f32 | Float32 | 0   | 1     |

## Design Rationale

## Processing

Refer the design

# Known Limitations with Design

None

# UNIT TEST CONSIDERATION

####### Abbreviations and Acronyms

| In the file CDD_MotRplCoggCmd_MotCtrl.c ARCHGLBPRM_ONEOVER2PI constant has been used from ArchGlbPrm.h file instead of ONEOVER2PI which is defined in the FDD. The architecture has changed to include the constant ONEOVER2PI in the architecture global parameter list as ARCHGLBPRM_ONEOVER2PI **Abbreviation or Acronym** | **Description** |
|------------------------|------------------------------------------------|
|                                                                                                                                                                                                                                                                                                                               |                 |
|                                                                                                                                                                                                                                                                                                                               |                 |

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
| 3           | [Software Naming Conventions.doc](http://misagweb01.nexteer.com/eRoomReq/Files/erooms8/NextGeneration/0_fc55f/Software%20Naming%20Conventions%2003x(In%20Work).doc)   | 1.0               |
| 4           | [Software Design and Coding Standards.doc](http://eroom1.nexteer.com/eRoomReq/Files/erooms8/NextGeneration/0_1a67a9/Software%20Design%20and%20Coding%20Standards.doc) | 2.0               |

{% endraw %}