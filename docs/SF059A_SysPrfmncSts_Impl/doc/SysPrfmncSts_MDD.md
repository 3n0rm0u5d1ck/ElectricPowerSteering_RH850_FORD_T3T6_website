---
layout: default
title: SysPrfmncSts_MDD
nav_order: 2
parent: Component Implementation
---
{% raw %}
**Module Design Document**

**For**

**SysPrfmncSts**

**Jan 19, 2017**

**Prepared For:**

**Software Engineering**

**Nexteer Automotive,**

**Saginaw, MI, USA**

**Prepared By:**

**SW Component group,**

**Nexteer Automotive,**

**Saginaw, MI, USA  
<u>Change History</u>**

|                 |              |             |             |
|-----------------|--------------|-------------|-------------|
| **Description** | **Author**   | **Version** | **Date**    |
| Initial Version | Krishna Anne | 1.0         | 20-Jan-2017 |

**  
**

**<u>Table of Contents</u>**

[1 Introduction [4](#introduction)](#introduction)

[2 SysPrfmncSts & High-Level Description
[5](#sysprfmncsts-high-level-description)](#sysprfmncsts-high-level-description)

[3 Design details of software module
[6](#design-details-of-software-module)](#design-details-of-software-module)

[3.1 Graphical representation of SysPrfmncSts
[6](#graphical-representation-of-sysprfmncsts)](#graphical-representation-of-sysprfmncsts)

[3.2 Data Flow Diagram [6](#data-flow-diagram)](#data-flow-diagram)

[4 Constant Data Dictionary
[7](#constant-data-dictionary)](#constant-data-dictionary)

[4.1 Program (fixed) Constants
[7](#program-fixed-constants)](#program-fixed-constants)

[4.1.1 Embedded Constants [7](#embedded-constants)](#embedded-constants)

[5 Software Component Implementation
[8](#software-component-implementation)](#software-component-implementation)

[5.1 Sub-Module Functions
[8](#sub-module-functions)](#sub-module-functions)

[5.1.1 Init: SysPrfmncStsInit1
[8](#init-sysprfmncstsinit1)](#init-sysprfmncstsinit1)

[5.1.1.1 Design Rationale [8](#design-rationale)](#design-rationale)

[5.1.1.2 Module Outputs [8](#module-outputs)](#module-outputs)

[5.1.2 Per: SysPrfmncStsPer1
[8](#per-sysprfmncstsper1)](#per-sysprfmncstsper1)

[5.1.2.1 Design Rationale [8](#design-rationale-1)](#design-rationale-1)

[5.1.2.2 Store Module Inputs to Local copies
[8](#store-module-inputs-to-local-copies)](#store-module-inputs-to-local-copies)

[5.2 Server Runables [8](#server-runables)](#server-runables)

[5.3 Interrupt Functions
[8](#interrupt-functions)](#interrupt-functions)

[5.4 Module Internal (Local) Functions
[8](#module-internal-local-functions)](#module-internal-local-functions)

[5.4.1 Local Function \#1 [8](#local-function-1)](#local-function-1)

[5.4.1.1 Design Rationale [9](#design-rationale-2)](#design-rationale-2)

[5.4.1.2 Processing [9](#processing)](#processing)

[5.4.2 Local Function \#2 [9](#local-function-2)](#local-function-2)

[5.4.2.1 Design Rationale [9](#design-rationale-3)](#design-rationale-3)

[5.4.2.2 Processing [9](#processing-1)](#processing-1)

[6 Known Limitations with Design
[10](#known-limitations-with-design)](#known-limitations-with-design)

[7 UNIT TEST CONSIDERATION
[11](#unit-test-consideration)](#unit-test-consideration)

[Appendix A Abbreviations and Acronyms
[12](#abbreviations-and-acronyms)](#abbreviations-and-acronyms)

[Appendix B Glossary [13](#glossary)](#glossary)

[Appendix C References [14](#references)](#references)

# Introduction

Please refer the Design Subproject.

# SysPrfmncSts & High-Level Description

Please refer the Design Subproject.

# Design details of software module

Please refer the Design Subproject.

## Graphical representation of SysPrfmncSts

<img
src="ElectricPowerSteering_RH850_FORD_T3T6_website/docs/SF059A_SysPrfmncSts_Impl/doc/mediax/media/image1.png"
style="width:3.77917in;height:5.47222in" />

## Data Flow Diagram

Please refer the Design Subproject.

# Constant Data Dictionary

## Program (fixed) Constants

### Embedded Constants

#### Local Constants

| Constant Name                                      | Resolution | Units | Value |
|---------------------------------|---------------|-----------|-------------|
| Please refer the .m file in the design Subproject. | NA         | NA    | NA    |

# Software Component Implementation

## Sub-Module Functions

None

## Init: SysPrfmncStsInit1

## Design Rationale

None

## Module Outputs

None

## Per: SysPrfmncStsPer1

## Design Rationale

None

## Store Module Inputs to Local copies

None

## Server Runables 

None

## Interrupt Functions

None

## Module Internal (Local) Functions

## Local Function \#1

|                      |                                             |         |      |        |
|---------------|--------------------------------|---------|---------|---------|
| **Function Name**    | PrfmncSysSt1                                | Type    | Min  | Max    |
| **Arguments Passed** | SysSt_Val_Cnt_T_enum                        | SysSt1  | 0U   | 3U     |
|                      | ThermDutyCycProtnTDptLim_MotNwtMtr_T_f32    | float32 | 0.0F | 8.8F   |
|                      | ThermDutyCycProtnLoadDptLim_MotNwtMtr_T_f32 | float32 | 0.0F | 8.8F   |
|                      | StallMotTqLim_MotNwtMtr_T_f32               | float32 | 0.0F | 8.8F   |
|                      | \*SysPrfmncSt_Cnt_T_u16                     | uint16  | 0U   | 36702U |
| **Return Value**     | NA                                          | NA      | NA   | NA     |

## Design Rationale

None

## Processing

Please refer below path in FDD.

*SF059A_SysPrfmncSts/SysPrfmncSts/SysPrfmncStsPer1/PrfmncSysSt*

## Local Function \#2

|                      |                                    |         |        |        |
|---------------|--------------------------------|---------|---------|---------|
| **Function Name**    | PrfmncSysSt2                       | Type    | Min    | Max    |
| **Arguments Passed** | DutyCycThermProtnMaxOutp_Uls_T_u16 | uint16  | 0U     | 200U   |
|                      | EcuTFild_DegCgrd_T_f32             | float32 | -50.0F | 50.0F  |
|                      | LoaSt_Val_Cnt_T_enum               | LoaSt1  | 0U     | 5U     |
|                      | VehSpdVld_Cnt_T_logl               | Boolean | FALSE  | TRUE   |
|                      | \*SysPrfmncSt_Cnt_T_u16            | uint16  | 0U     | 36702U |
| **Return Value**     | NA                                 | NA      | NA     | NA     |

## Design Rationale

None

## Processing

Please refer below path in FDD.

*SF059A_SysPrfmncSts/SysPrfmncSts/SysPrfmncStsPer1/PrfmncSysSt*

# Known Limitations with Design

NTC definitions are missed in the .m file of the design. FDD owner
agreed to include them in the next revision.

Anomaly EA4#9446 is raised.

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
| 5           | FDD : SF059A_SysPrfmncSts_Design                                                                                                                                      | See synergy sub-project version |

{% endraw %}