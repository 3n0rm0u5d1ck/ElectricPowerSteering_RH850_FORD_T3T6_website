---
layout: default
title: MotAg6Meas_MDD
nav_order: 2
parent: Component Implementation
---
{% raw %}
**Module Design Document**

**For**

**MotAg6Meas**

**Oct 16, 2017**

**Prepared By:**

**Shruthi Raghavan,**

**Nexteer Automotive,**

**Saginaw, MI, USA**

**<u>Change History</u>**

|                                                            |                  |             |             |
|------------------------------------------|-------------|--------|----------|
| **Description**                                            | **Author**       | **Version** | **Date**    |
| Initial Version                                            | Shruthi Raghavan | 1           | 31-Jul-2017 |
| Updated graphical representation to show input name change | Shruthi Raghavan | 2           | 16-Oct-2017 |

**  
**

**<u>Table of Contents</u>**

[1 Introduction [5](#introduction)](#introduction)

[1.1 Purpose [5](#purpose)](#purpose)

[2 MotAg6Meas & High-Level Description
[6](#motag6meas-high-level-description)](#motag6meas-high-level-description)

[3 Design details of software module
[7](#design-details-of-software-module)](#design-details-of-software-module)

[3.1 Graphical representation of MotAg6Meas
[7](#graphical-representation-of-motag6meas)](#graphical-representation-of-motag6meas)

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

[5.1.1 Init: MotAg6MeasInit1
[9](#init-motag6measinit1)](#init-motag6measinit1)

[5.1.1.1 Design Rationale [9](#design-rationale)](#design-rationale)

[5.1.2 Per: MotAg6MeasPer1
[9](#per-motag6measper1)](#per-motag6measper1)

[5.1.2.1 Design Rationale [9](#design-rationale-1)](#design-rationale-1)

[5.1.3 Per: MotAg6MeasPer2
[9](#per-motag6measper2)](#per-motag6measper2)

[5.1.3.1 Design Rationale [9](#design-rationale-2)](#design-rationale-2)

[5.1.4 Per: MotAg6MeasPer3
[9](#per-motag6measper3)](#per-motag6measper3)

[5.1.4.1 Design Rationale [9](#design-rationale-3)](#design-rationale-3)

[5.2 Server Runables [9](#server-runables)](#server-runables)

[5.2.1 MotAg6EolPrmRead [9](#motag6eolprmread)](#motag6eolprmread)

[5.2.1.1 Design Rationale [9](#design-rationale-4)](#design-rationale-4)

[5.2.2 MotAg6EolPrmWr [9](#motag6eolprmwr)](#motag6eolprmwr)

[5.2.2.1 Design Rationale [9](#design-rationale-5)](#design-rationale-5)

[5.3 Module Internal (Local) Functions
[9](#module-internal-local-functions)](#module-internal-local-functions)

[5.3.1 Local Function \#1 [9](#local-function-1)](#local-function-1)

[5.4 GLOBAL Function/Macro Definitions
[10](#_Toc489445812)](#_Toc489445812)

[5.4.1 GLOBAL Function \#1 [10](#global-function-1)](#global-function-1)

[5.4.1.1 Design Rationale
[10](#design-rationale-6)](#design-rationale-6)

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

Module design document for MotAg6Meas

# MotAg6Meas & High-Level Description

*MotAg6Meas funtion shall compute motor angle from Sine and Cosine ADC
signals.*

# Design details of software module

## Graphical representation of MotAg6Meas

> <img
> src="ElectricPowerSteering_RH850_FORD_T3T6_website/docs/ES243A_MotAg6Meas_Impl/doc/mediax/media/image2.png"
> style="width:3.31147in;height:4.79433in" />

## Data Flow Diagram

### Component level DFD

### Function level DFD

# Constant Data Dictionary

## Program (fixed) Constants

### Embedded Constants

#### Local Constants

| Constant Name            | Resolution | Units | Value |
|--------------------------|------------|-------|-------|
| ADCLORNGFAILDBIT_CNT_U08 | 1          | Cnt   | 0U    |
| ADCHIRNGFAILDBIT_CNT_U08 | 1          | Cnt   | 1U    |

# Software Component Implementation

## Sub-Module Functions

## Init: MotAg6MeasInit1

> Refer FDD simulink model for design details.

## Design Rationale

> ‘LpFil Init’ block in the FDD does not use ‘FilLpInit’ library block
> due to a design limitation with the Library block (see ‘Known
> limitations with design’). However, code has no such limitation, so
> the code uses ‘FilLpInit’ block instead of initializing the gain using
> ‘FilLpUpdGain’ block first and then updating the state variable
> values.

## Per: MotAg6MeasPer1

> Refer FDD simulink model for design details.

## Design Rationale

> Rollover on Rte_Pim_MotAg6PrevRollgCntr is intentional, as it is used
> to reset the rolling counter back to zero when it reaches its max
> value of 255. The functionality remains the same as in the FDD.

## Per: MotAg6MeasPer2

## Design Rationale

> Refer FDD simulink model for design details.

## Per: MotAg6MeasPer3

## Design Rationale

> Refer FDD simulink model for design details.

## Server Runables 

## MotAg6EolPrmRead

## Design Rationale

## MotAg6EolPrmWr

## Design Rationale

## Module Internal (Local) Functions

## Local Function \#1

|                      |      |      |     |     |
|----------------------|------|------|-----|-----|
| **Function Name**    | N/A  | Type | Min | Max |
| **Arguments Passed** | None | \-   | \-  | \-  |
| **Return Value**     | N/A  | \-   | \-  | \-  |

## GLOBAL Function/Macro Definitions

## GLOBAL Function \#1

|                      |       |      |     |     |
|----------------------|-------|------|-----|-----|
| **Function Name**    | N/A   | Type | Min | Max |
| **Arguments Passed** | Nones | \-   | \-  | \-  |
| **Return Value**     | N/A   | \-   | \-  | \-  |

## Design Rationale

> N/A

# Known Limitations with Design

1.  The model does not use ‘FilLpInit’ because that library block cannot
    accept a variable as input for initialization of the state variable.
    So they initialize the gain first in the model using ‘FilLpUpdGain’
    and then initialize the state variable with the required
    non-constant input value to the sub-block.

2.  The model uses SCAGCON_ULS_F32 in simulation only blocks but lists
    this in the Data dictionary m file. However, this isnt required for
    implementation.

# UNIT TEST CONSIDERATION

> Some overflows are intentional. This is indicated as such in the code
> using comments.

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

| **Ref. \#** | **Title**                                                                                                                                                                                                                             | **Version**       |
|-------|-------------------------------------------------|-----------------|
| 1           | AUTOSAR Specification of Memory Mapping (Link:[AUTOSAR_SWS_MemoryMapping.pdf](https://www.autosar.org/fileadmin/files/standards/classic/4-0/software-architecture/implementation-integration/standard/AUTOSAR_SWS_MemoryMapping.pdf)) | v1.4.0 R4.0 Rev 3 |
| 2           | MDD Guideline                                                                                                                                                                                                                         | EA4 01.00.01      |
| 3           | EA4 [Software Naming Conventions.doc](http://misagweb01.nexteer.com/eRoomReq/Files/erooms8/NextGeneration/0_fc55f/Software%20Naming%20Conventions%2003x(In%20Work).doc)                                                               | 01.01.00          |
| 4           | [Software Design and Coding Standards.doc](http://eroom1.nexteer.com/eRoomReq/Files/erooms8/NextGeneration/0_1a67a9/Software%20Design%20and%20Coding%20Standards.doc)                                                                 | 2.1               |

{% endraw %}