---
layout: default
title: Uart0CfgAndUse_MDD
nav_order: 2
parent: Component Implementation
---
{% raw %}
**Module Design Document**

**For**

**Uart0CfgAndUse**

**Jan 11, 2018**

**Prepared For:**

**Software Engineering**

**Nexteer Automotive,**

**Saginaw, MI, USA**

**Prepared By:**

**Software Group,**

**Nexteer Automotive,**

**Saginaw, MI, USA  
<u>Change History</u>**

|                                           |                  |             |              |
|---------------------------|------------------|--------------|--------------|
| **Description**                           | **Author**       | **Version** | **Date**     |
| Initial Version                           | Krzysztof Byrski | 1           | 08-June-2017 |
| Updated the local functions and constants | Avinash James    | 2           | 11-Jan-2018  |

**  
**

<u>Table of Contents</u>1 Introduction 4

1.1 Purpose 4

1.2 Scope 4

2 Uart0CfgAndUse & High-Level Description 5

3 Design details of software module 6

3.1 Graphical representation of Uart0CfgAndUse 6

3.2 Data Flow Diagram 6

3.2.1 Component level DFD 6

3.2.2 Function level DFD 6

4 Constant Data Dictionary 7

4.1 Program (fixed) Constants 7

4.1.1 Embedded Constants 7

5 Software Component Implementation 8

5.1 Sub-Module Functions 8

5.1.1 Init: Uart0CfgAndUseInit1 8

5.1.2 Per: Uart0CfgAndUsePer1 8

5.1.3 Per: Uart0CfgAndUsePer2 8

5.1.4 Per: Uart0CfgAndUsePer3 8

5.1.5 Per: Uart0CfgAndUsePer4 9

5.2 Server Runables 9

5.3 Interrupt Functions 9

5.4 Module Internal (Local) Functions 9

5.4.1 RollOverAdd 9

5.4.2 UpdDtsTxReg 10

5.4.3 UpdDtsRxReg 10

5.5 GLOBAL Function/Macro Definitions 10

6 Known Limitations with Design 11

7 UNIT TEST CONSIDERATION 12

Appendix A Abbreviations and Acronyms 13

Appendix B Glossary 14

Appendix C References 15

# Introduction

## Purpose

Module Design Document for CM760A_Uart0CfgAndUse.

## Scope

The following definitions are used throughout this document:

-   **<u>Shall</u>**: indicates a mandatory requirement without
    exception in compliance.

-   **<u>Should</u>**: indicates a mandatory requirement; exceptions
    allowed only with documented justification.

-   **<u>May</u>**: indicates an optional action.

# Uart0CfgAndUse & High-Level Description

Refer FDD.

# Design details of software module

## Graphical representation of Uart0CfgAndUse

<img
src="ElectricPowerSteering_RH850_FORD_T3T6_website/docs/CM760A_Uart0CfgAndUse_Impl/doc/mediax/media/image1.png"
style="width:2.05208in;height:1.40625in" />

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

| Constant Name                 | Resolution | Units | Value      |
|-------------------------------|------------|-------|------------|
| ROLLGCNTCHK_CNT_U08           | 1          | Cnt   | 255        |
| DATABYTE0_CNT_U08             | 1          | Cnt   | 0          |
| DATABYTE1_CNT_U08             | 1          | Cnt   | 1          |
| DATABYTE2_CNT_U08             | 1          | Cnt   | 2          |
| DATABYTE3_CNT_U08             | 1          | Cnt   | 3          |
| DATABYTE4_CNT_U08             | 1          | Cnt   | 4          |
| DATABYTE5_CNT_U08             | 1          | Cnt   | 5          |
| DATABYTE6_CNT_U08             | 1          | Cnt   | 6          |
| DATABYTE7_CNT_U08             | 1          | Cnt   | 7          |
| DATABYTE8_CNT_U08             | 1          | Cnt   | 8          |
| MASKLOWR16BITOFUINT32_CNT_U16 | 1          | Cnt   | 65535      |
|                               |            |       |            |
| MAXSIGGROUPFORTX_CNT_U08      | 1          | Cnt   | 9          |
| TWO_CNT_U08                   | 1          | Cnt   | 2          |
| UART0RXMAXBUFSIZE_CNT_U08     | 1          | Cnt   | 144        |
| UART0TXBUFSIZE_CNT_U08        | 1          | Cnt   | 80         |
| RLN30LBRP01BRP_CNT_U08        | 1          | Cnt   | 4          |
| DTS101CM_CNT_U32              | 1          | Cnt   | 0x20120000 |
| DTS100CM_CNT_U32              | 1          | Cnt   | 0x200E0000 |
| DTTCT101_CNT_U32              | 1          | Cnt   | 256        |
| DTTC100_CNT_U32               | 1          | Cnt   | 9438624    |
| DTTCT100_CNT_U32              | 1          | Cnt   | 6720       |
| DTRTC100_CNT_U32              | 1          | Cnt   | 9438624    |

# Software Component Implementation

## Sub-Module Functions

The sub-module functions are grouped based on similar functionality that
needs to be executed in a given “State” of the system (refer States and
Modes). For a given module, the MDD will identify the type and number of
sub-modules required. The sub-module types are described below.

### Init: Init1

#### Design Rationale

Refer FDD

#### Module Outputs

Refer FDD

### Per: Per1

#### Design Rationale

Refer FDD

#### Store Module Inputs to Local copies

Refer FDD

#### (Processing of function)………

Refer FDD

#### Store Local copy of outputs into Module Outputs

Refer FDD

### Per: Per2

#### Design Rationale

Refer FDD

#### Store Module Inputs to Local copies

Refer FDD

#### (Processing of function)………

Refer FDD

#### Store Local copy of outputs into Module Outputs

Refer FDD

### Per: Per3

#### Design Rationale

Refer FDD

#### Store Module Inputs to Local copies

Refer FDD

#### (Processing of function)………

Refer FDD

#### Store Local copy of outputs into Module Outputs

Refer FDD

### Per: Per4

#### Design Rationale

Refer FDD

#### Store Module Inputs to Local copies

Refer FDD

#### (Processing of function)………

Refer FDD

#### Store Local copy of outputs into Module Outputs

Refer FDD

## Server Runables 

None

## Interrupt Functions

None

## Module Internal (Local) Functions

### RollOverAdd

|                      |                  |       |     |     |
|----------------------|------------------|-------|-----|-----|
| **Function Name**    | RollOverAdd      | Type  | Min | Max |
| **Arguments Passed** | Input1_Cnt_T_u08 | uint8 | 0   | 255 |
|                      | Input2_Cnt_T_u08 | uint8 | 0   | 255 |
| **Return Value**     | Output_Cnt_T_u08 | uint8 | 0   | 143 |

#### Design Rationale

Refer FDD

#### Processing

Refer FDD

### UpdDtsTxReg

|                      |                      |       |     |     |
|----------------------|----------------------|-------|-----|-----|
| **Function Name**    | UpdDtsTxReg          | Type  | Min | Max |
| **Arguments Passed** | Uart0GlbTx_Cnt_T_u08 | uint8 | 0   | 72  |
| **Return Value**     | None                 | \-    | \-  | \-  |

#### Design Rationale

Refer FDD

#### Processing

Refer FDD

### Uart1Diagc

|                      |                 |       |     |     |
|----------------------|-----------------|-------|-----|-----|
| **Function Name**    | Uart1Diagc      | Type  | Min | Max |
| **Arguments Passed** | Uart1RxDataCntr | uint8 | 0   | 255 |
| **Return Value**     | None            | \-    | \-  | \-  |

#### Design Rationale

Refer Uart1RxDataCntr block in FDD

#### Processing

Refer FDD

## GLOBAL Function/Macro Definitions

None

# Known Limitations with Design

The client call SetRxSigGroup has one argument Buf which is listed as
Output in the design but implemented correctly as Input. This is an
update to AR350A and is not done as of today.

The component makes use of static component level variables which are
needed for the special DMA mapping .

# UNIT TEST CONSIDERATION

Code prover flags out of bound array access as it considers range of the
index variable outside the array bounds. But this has been functionally
checked to be within the limits.

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
| 2           | MDD Guideline                                                                                                                                      | EA4 01.00.01                    |
| 3           | Software Naming Conventions                                                                                                                        | 01.01.00                        |
| 4           | Software Design and Coding Standards                                                                                                               | 2.1                             |
| 5           | CM760A_Uart0CfgAndUse_Design                                                                                                                       | See Synergy Sub Project Version |

{% endraw %}