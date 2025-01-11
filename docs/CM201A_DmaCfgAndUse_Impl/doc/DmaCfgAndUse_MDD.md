---
layout: default
title: DmaCfgAndUse_MDD
nav_order: 2
parent: Component Implementation
---
{% raw %}
**Module Design Document**

**For**

**DmaCfgAndUse**

**October 4, 2017**

**Prepared For:**

**Software Engineering**

**Nexteer Automotive,**

**Saginaw, MI, USA**

**Prepared By:**

**Software Group,**

**Nexteer Automotive,**

**Saginaw, MI, USA  
<u>Change History</u>**

|                                         |                  |             |                  |
|---------------------------|------------------|--------------|--------------|
| **Description**                         | **Author**       | **Version** | **Date**         |
| Initial Version                         | Krzysztof Byrski | 1           | 11-July-2017     |
| Changed value of register DTFR1 to 0x87 | Krzysztof Byrski | 2           | 8-September-2017 |
| Removed constant DTFR9ERR_CNT_U32       | Krzysztof Byrski | 3           | 4-October-2017   |

**  
**

<span id="_Toc492549846" class="anchor"></span><u>Table of Contents</u>

[Table of Contents [3](#_Toc492549846)](#_Toc492549846)

[1 Introduction [4](#introduction)](#introduction)

[1.1 Purpose [4](#purpose)](#purpose)

[1.2 Scope [4](#scope)](#scope)

[2 DmaCfgAndUse & High-Level Description
[5](#dmacfganduse-high-level-description)](#dmacfganduse-high-level-description)

[3 Design details of software module
[6](#design-details-of-software-module)](#design-details-of-software-module)

[3.1 Graphical representation of DmaCfgAndUse
[6](#graphical-representation-of-dmacfganduse)](#graphical-representation-of-dmacfganduse)

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

[5.1.1 Init: DmaCfgAndUseInit1
[8](#init-dmacfganduseinit1)](#init-dmacfganduseinit1)

[5.1.2 Per: DmaCfgAndUsePer1
[8](#per-dmacfganduseper1)](#per-dmacfganduseper1)

[5.2 Server Runables [8](#server-runables)](#server-runables)

[5.2.1 DmaEna2MilliSecToMotCtrlTrf_Oper
[8](#dmaena2millisectomotctrltrf_oper)](#dmaena2millisectomotctrltrf_oper)

[5.2.2 DmaWaitForMotCtrlTo2MilliSecTrf_Oper
[8](#dmawaitformotctrlto2millisectrf_oper)](#dmawaitformotctrlto2millisectrf_oper)

[5.2.3 InjDmaErr [9](#injdmaerr)](#injdmaerr)

[5.2.4 InjMcuDiagcErr [9](#injmcudiagcerr)](#injmcudiagcerr)

[5.3 Interrupt Functions
[9](#interrupt-functions)](#interrupt-functions)

[5.4 Module Internal (Local) Functions
[9](#module-internal-local-functions)](#module-internal-local-functions)

[5.5 GLOBAL Function/Macro Definitions
[9](#global-functionmacro-definitions)](#global-functionmacro-definitions)

[5.5.1 GLOBAL Function \#1 [9](#global-function-1)](#global-function-1)

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

Module Design Document for CM201A_DmaCfgAndUse.

## Scope

The following definitions are used throughout this document:

-   **<u>Shall</u>**: indicates a mandatory requirement without
    exception in compliance.

-   **<u>Should</u>**: indicates a mandatory requirement; exceptions
    allowed only with documented justification.

-   **<u>May</u>**: indicates an optional action.

# DmaCfgAndUse & High-Level Description

Refer FDD

# Design details of software module

## Graphical representation of DmaCfgAndUse

<img
src="ElectricPowerSteering_RH850_FORD_T3T6_website/docs/CM201A_DmaCfgAndUse_Impl/doc/mediax/media/image1.png"
style="width:6.01042in;height:2.89583in" />

## Data Flow Diagram

Refer FDD

### Component level DFD

None

### Function level DFD

None

# Constant Data Dictionary

## Program (fixed) Constants

### Embedded Constants

#### Local Constants

| Constant Name                     | Resolution | Units       | Value      |
|-----------------------------------|------------|-------------|------------|
| DMACFGANDUSE_MAXWAIT_MICROSEC_U32 | 1          | Microsecond | 400        |
| DM01CM_CNT_U32                    | 1          | Cnt         | 0x0000200C |
| DTC1_CNT_U32                      | 1          | Cnt         | 0x00000003 |
| DTCT1_CNT_U32                     | 1          | Cnt         | 0x04006611 |
| DRTC1_CNT_U32                     | 1          | Cnt         | 0x00000003 |
| DTCC1_CNT_U32                     | 1          | Cnt         | 0x00000000 |
| DTFR1_CNT_U32                     | 1          | Cnt         | 0x00000087 |
| DM11CM_CNT_U32                    | 1          | Cnt         | 0x00002016 |
| DTCT9_CNT_U32                     | 1          | Cnt         | 0x04000611 |
| DTCC9_CNT_U32                     | 1          | Cnt         | 0x00000000 |
| DTFR9_CNT_U32                     | 1          | Cnt         | 0x00000069 |
| DM16CM_CNT_U32                    | 1          | Cnt         | 0x00002012 |
| DTC14_CNT_U32                     | 1          | Cnt         | 0x00000003 |
| DTCT14_CNT_U32                    | 1          | Cnt         | 0x041D0611 |
| DRTC14_CNT_U32                    | 1          | Cnt         | 0x00000003 |
| DTCC14_CNT_U32                    | 1          | Cnt         | 0x00000000 |
| DTFR14_CNT_U32                    | 1          | Cnt         | 0x00000093 |
| DM17CM_CNT_U32                    | 1          | Cnt         | 0x00002016 |
| DTCT15_CNT_U32                    | 1          | Cnt         | 0x00002611 |
| DTCC15_CNT_U32                    | 1          | Cnt         | 0x00000000 |
| DTFR15_CNT_U32                    | 1          | Cnt         | 0x00000000 |
|                                   |            |             |            |
| UNDEFDAR_CNT_U32                  | 1          | Cnt         | 0xFEBFFFFC |
| TRFSIZE_CNT_U32                   | 1          | Cnt         | 16         |

# Software Component Implementation

## Sub-Module Functions

The sub-module functions are grouped based on similar functionality that
needs to be executed in a given “State” of the system (refer States and
Modes). For a given module, the MDD will identify the type and number of
sub-modules required. The sub-module types are described below.

### Init: DmaCfgAndUseInit1

#### Design Rationale

Refer FDD

#### Module Outputs

Refer FDD

### Per: DmaCfgAndUsePer1

#### Design Rationale

#### Store Module Inputs to Local copies

Refer FDD

#### (Processing of function)………

Refer FDD

#### Store Local copy of outputs into Module Outputs

Refer FDD

## Server Runables 

### DmaEna2MilliSecToMotCtrlTrf_Oper

#### Design Rationale

Refer FDD

####  (Processing of function)………

Refer FDD

### DmaWaitForMotCtrlTo2MilliSecTrf_Oper

#### Design Rationale

Refer FDD

####  (Processing of function)………

Refer FDD

### InjDmaErr

#### Design Rationale

Refer FDD

####  (Processing of function)………

Refer FDD

### InjMcuDiagcErr

#### Design Rationale

Refer FDD

####  (Processing of function)………

Refer FDD

## Interrupt Functions

None

## Module Internal (Local) Functions

None

## GLOBAL Function/Macro Definitions

### GLOBAL Function \#1

|                      |            |      |     |     |
|----------------------|------------|------|-----|-----|
| **Function Name**    | DmaRegInin | Type | Min | Max |
| **Arguments Passed** | None       |      |     |     |
| **Return Value**     | N/A        |      |     |     |

#### Design Rationale

Trusted function that performs all register initialization from the
“CM201A_DmaCfgAndUse_PeripheralCfg.xlsx” spreadsheet in the FDD. The
DMnnCM channel master registers can be written only in supervisor mode.
After the Channel master register for a given channel has been written,
the selected Processor Element can write to that channel’s registers in
user mode. However, for simplicity, all DMA register initialization is
being done in one trusted function.

#### Processing

Refer FDD

# Known Limitations with Design

None

# UNIT TEST CONSIDERATION

None

# Abbreviations and Acronyms

| **Abbreviation or Acronym** | **Description** |
|-----------------------------|-----------------|
| \-                          | \-              |

# Glossary

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

# References

| **Ref. \#** | **Title**                                                                                                                                          | **Version**                     |
|-------|-------------------------------------------------|-----------------|
| 1           | AUTOSAR Specification of Memory Mapping (Link:[AUTOSAR_SWS_MemoryMapping.pdf](http://www.autosar.org/download/R4.0/AUTOSAR_SWS_MemoryMapping.pdf)) | v1.3.0 R4.0 Rev 2               |
| 2           | MDD Guideline                                                                                                                                      | 01.00.01                        |
| 3           | Software Naming Conventions                                                                                                                        | 01.01.00                        |
| 4           | Software Design and Coding Standards                                                                                                               | 2.1                             |
| 5           | CM201A_DmaCfgAndUse_Design                                                                                                                         | See Synergy Sub Project Version |

{% endraw %}