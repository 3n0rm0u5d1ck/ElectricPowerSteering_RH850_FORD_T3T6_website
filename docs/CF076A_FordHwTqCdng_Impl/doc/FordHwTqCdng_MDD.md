---
layout: default
title: FordHwTqCdng_MDD
nav_order: 2
parent: Component Implementation
---
{% raw %}
**Module Design Document**

**For**

**FordHwTqCdng**

**June 19, 20158**

**Prepared For:**

**Software Engineering**

**Nexteer Automotive,**

**Saginaw, MI, USA**

**Prepared By:**

**Tata Elxsi,**

**Trivandrum, INDIA**

**<u>Change History</u>**

|             |                 |            |             |             |
|-------------|-----------------|------------|-------------|-------------|
| **Sl. No.** | **Description** | **Author** | **Version** | **Date**    |
| 1           | Initial Version | TATA       | 1.0         | 11-Jan-2018 |

**<u>Table of Contents</u>**

[1 Introduction [5](#introduction)](#introduction)

[1.1 Purpose [5](#purpose)](#purpose)

[2 FordHwTqCdng & High-Level Description
[6](#_Toc503455916)](#_Toc503455916)

[3 Design details of software module
[7](#design-details-of-software-module)](#design-details-of-software-module)

[3.1 Graphical representation of FordHwTqCdng
[7](#graphical-representation-of-component-name)](#graphical-representation-of-component-name)

[3.2 Data Flow Diagram [7](#data-flow-diagram)](#data-flow-diagram)

[Component level DFD [7](#component-level-dfd)](#component-level-dfd)

[Function level DFD [7](#function-level-dfd)](#function-level-dfd)

[4 Constant Data Dictionary
[8](#constant-data-dictionary)](#constant-data-dictionary)

[4.1 Program (fixed) Constants
[8](#program-fixed-constants)](#program-fixed-constants)

[Embedded Constants [8](#embedded-constants)](#embedded-constants)

[5 Software Component Implementation
[9](#software-component-implementation)](#software-component-implementation)

[5.1 Sub-Module Functions
[9](#sub-module-functions)](#sub-module-functions)

[5.1.1 Init: FordHwTqCdngInit1
[9](#init-component-nameinit1)](#init-component-nameinit1)

[5.1.1.1 Design Rationale [9](#design-rationale)](#design-rationale)

[5.1.1.2 Module Outputs [9](#module-outputs)](#module-outputs)

[5.1.2 Per: FordHwTqCdngPer1
[9](#per-component-nameper1)](#per-component-nameper1)

[5.1.2.1 Design Rationale [9](#design-rationale-1)](#design-rationale-1)

[5.1.2.2 Store Module Inputs to Local copies
[9](#store-module-inputs-to-local-copies)](#store-module-inputs-to-local-copies)

[5.1.2.3 Processing of function
[9](#processing-of-function)](#processing-of-function)

[5.1.2.4 Store Local copy of outputs into Module Outputs
[9](#store-local-copy-of-outputs-into-module-outputs)](#store-local-copy-of-outputs-into-module-outputs)

[5.1.3 Per: FordHwTqCdngPer2
[9](#per-component-nameper2)](#per-component-nameper2)

[5.1.3.1 Design Rationale [9](#design-rationale-2)](#design-rationale-2)

[5.1.3.2 Store Module Inputs to Local copies
[9](#store-module-inputs-to-local-copies-1)](#store-module-inputs-to-local-copies-1)

[5.1.3.3 Processing of function
[9](#processing-of-function-1)](#processing-of-function-1)

[5.1.3.4 Store Local copy of outputs into Module Outputs
[9](#store-local-copy-of-outputs-into-module-outputs-1)](#store-local-copy-of-outputs-into-module-outputs-1)

[5.2 Server Runnables [10](#server-runnables)](#server-runnables)

[5.2.1 Runnable: FIH_Read_EPS_Direct_BC_Torque
[10](#runnable-fih_read_eps_direct_bc_torque)](#runnable-fih_read_eps_direct_bc_torque)

[5.2.1.1 Design Rationale
[10](#design-rationale-3)](#design-rationale-3)

[5.2.1.2 Store Module Inputs to Local copies
[10](#store-module-inputs-to-local-copies-2)](#store-module-inputs-to-local-copies-2)

[5.2.1.3 Processing of function
[10](#processing-of-function-2)](#processing-of-function-2)

[5.2.1.4 Store Local copy of outputs into Module Outputs
[10](#store-local-copy-of-outputs-into-module-outputs-2)](#store-local-copy-of-outputs-into-module-outputs-2)

[5.2.2 Runnable: FIH_Read_EPS_Inverse_BC_Torque
[10](#runnable-fih_read_eps_inverse_bc_torque)](#runnable-fih_read_eps_inverse_bc_torque)

[5.2.2.1 Design Rationale
[10](#design-rationale-4)](#design-rationale-4)

[5.2.2.2 Store Module Inputs to Local copies
[10](#store-module-inputs-to-local-copies-3)](#store-module-inputs-to-local-copies-3)

[5.2.2.3 Processing of function
[10](#processing-of-function-3)](#processing-of-function-3)

[5.2.2.4 Store Local copy of outputs into Module Outputs
[10](#store-local-copy-of-outputs-into-module-outputs-3)](#store-local-copy-of-outputs-into-module-outputs-3)

[5.3 Interrupt Functions
[10](#interrupt-functions)](#interrupt-functions)

[5.4 Module Internal (Local) Functions
[10](#module-internal-local-functions)](#module-internal-local-functions)

[5.5 GLOBAL Function/Macro Definitions
[10](#global-functionmacro-definitions)](#global-functionmacro-definitions)

[6 Known Limitations with Design
[11](#known-limitations-with-design)](#known-limitations-with-design)

[7 UNIT TEST CONSIDERATION
[12](#unit-test-consideration)](#unit-test-consideration)

[Appendix A Abbreviations and Acronyms
[13](#abbreviations-and-acronyms)](#abbreviations-and-acronyms)

[Appendix B Glossary [14](#glossary)](#glossary)

[Appendix C References [15](#references)](#references)

# Introduction

## Purpose

MDD for FordHwTqCdng

# \<Component Name\> & High-Level Description

Please refer FDD.

# Design details of software module

## Graphical representation of \<Component Name\>

<img
src="ElectricPowerSteering_RH850_FORD_T3T6_website/docs/CF076A_FordHwTqCdng_Impl/doc/mediax/media/image1.jpeg"
style="width:4.84375in;height:4.01042in"
alt="C:\Users\ramachandran.mg\Desktop\guru\CF076A_FordHwTqCdng_Impl.JPG" />

## Data Flow Diagram

### Component level DFD

> Please refer FDD.

### Function level DFD

> Please refer FDD.

# Constant Data Dictionary

## Program (fixed) Constants

### Embedded Constants

#### Local Constants

| Constant Name                        | Resolution | Units | Value |
|--------------------------------------|------------|-------|-------|
| Please refer Data Dictionary .m file | NA         | NA    | NA    |

# Software Component Implementation

## Sub-Module Functions

### 5.1.1 Init: \<Component Name\>Init1

### 5.1.1.1 Design Rationale

None

### 5.1.1.2 Module Outputs

None

### 5.1.2 Per: \<Component Name\>Per1

## 5.1.2.1 Design Rationale [design-rationale-1]

None

## 5.1.2.2 Store Module Inputs to Local copies [store-module-inputs-to-local-copies]

None

## 5.1.2.3 Processing of function [processing-of-function]

None

## 5.1.2.4 Store Local copy of outputs into Module Outputs [store-local-copy-of-outputs-into-module-outputs]

> None

### 5.1.3 Per: \<Component Name\>Per2

## 5.1.3.1 Design Rationale [design-rationale-2]

None

## 5.1.3.2 Store Module Inputs to Local copies [store-module-inputs-to-local-copies-1]

None

## 5.1.3.3 Processing of function [processing-of-function-1]

None

## 5.1.3.4 Store Local copy of outputs into Module Outputs [store-local-copy-of-outputs-into-module-outputs-1]

> None

## Server Runnables 

### 5.2.1 Runnable: FIH_Read_EPS_Direct_BC_Torque

## 5.2.1.1 Design Rationale [design-rationale-3]

None

## 5.2.1.2 Store Module Inputs to Local copies [store-module-inputs-to-local-copies-2]

None

## 5.2.1.3 Processing of function [processing-of-function-2]

None

## 5.2.1.4 Store Local copy of outputs into Module Outputs [store-local-copy-of-outputs-into-module-outputs-2]

None

### 5.2.2 Runnable: FIH_Read_EPS_Inverse_BC_Torque

## 5.2.2.1 Design Rationale [design-rationale-4]

None

## 5.2.2.2 Store Module Inputs to Local copies [store-module-inputs-to-local-copies-3]

None

## 5.2.2.3 Processing of function [processing-of-function-3]

None

## 5.2.2.4 Store Local copy of outputs into Module Outputs [store-local-copy-of-outputs-into-module-outputs-3]

None

## Interrupt Functions

None

## Module Internal (Local) Functions

None

## GLOBAL Function/Macro Definitions

None

# Known Limitations with Design

1.  In data dictionary,

Server invocation of *GetRefTmr100MicroSec32bit* is not defined for the
Init runnable (*FordHwTqCdngInit1*).

1.  The RTE server runnables *FIH_Read_EPS_Direct_BC_Torque* and
    *FIH_Read_EPS_Inverse_BC_Torque* are not available in StdDef.dcf and
    Ford_MM_4.arxml

Therefore, these runnables have been implemented as Non-RTE runnables
for the current release.

1.  The sub function *IvsBoostCrv* will be implemented in future.
    Therefore, this sub function is not implemented at the moment.

Note: This has resulted in some Dataflow defects in Polyspace and it
will be resolved once the sub function is implemented in the subsequent
build.

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

| **Ref. \#** | **Title**                                                                                                                                                             | **Version**                     |
|-------|-------------------------------------------------|-----------------|
| 1           | AUTOSAR Specification of Memory Mapping (Link:[AUTOSAR_SWS_MemoryMapping.pdf](http://www.autosar.org/download/R4.0/AUTOSAR_SWS_MemoryMapping.pdf))                    | v1.3.0 R4.0 Rev 2               |
| 2           | MDD Guideline                                                                                                                                                         | EA4 01.00.00                    |
| 3           | [Software Naming Conventions.doc](http://misagweb01.nexteer.com/eRoomReq/Files/erooms8/NextGeneration/0_fc55f/Software%20Naming%20Conventions%2003x(In%20Work).doc)   | 1.0                             |
| 4           | [Software Design and Coding Standards.doc](http://eroom1.nexteer.com/eRoomReq/Files/erooms8/NextGeneration/0_1a67a9/Software%20Design%20and%20Coding%20Standards.doc) | 2.1                             |
| 5           | FDD: CF076A_FordHwTqCdng_Design                                                                                                                                       | See Synergy sub project version |

{% endraw %}