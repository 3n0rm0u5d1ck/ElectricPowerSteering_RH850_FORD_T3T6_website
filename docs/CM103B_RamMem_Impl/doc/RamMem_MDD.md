---
layout: default
title: RamMem_MDD
nav_order: 2
parent: Component Implementation
---
{% raw %}
**Module Design Document**

**For**

**RamMem**

**Oct 23, 2017**

**Prepared By:**

**Shruthi Raghavan,**

**Nexteer Automotive,**

**Saginaw, MI, USA**

**<u>Change History</u>**

|                 |                  |             |             |
|-----------------|------------------|-------------|-------------|
| **Description** | **Author**       | **Version** | **Date**    |
| Initial Version | Shruthi Raghavan | 1.0         | 23-Oct-2017 |

**  
**

**<u>Table of Contents</u>**

[1 Introduction [5](#introduction)](#introduction)

[1.1 Purpose [5](#purpose)](#purpose)

[2 RamMem & High-Level Description
[6](#rammem-high-level-description)](#rammem-high-level-description)

[3 Design details of software module
[7](#design-details-of-software-module)](#design-details-of-software-module)

[3.1 Graphical representation of RamMem
[7](#graphical-representation-of-rammem)](#graphical-representation-of-rammem)

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
[10](#software-component-implementation)](#software-component-implementation)

[5.1 Sub-Module Functions
[10](#sub-module-functions)](#sub-module-functions)

[5.1.1 Init: RamMemInit1 [10](#init-rammeminit1)](#init-rammeminit1)

[5.1.1.1 Design Rationale [10](#design-rationale)](#design-rationale)

[5.1.2 Per: RamMemPer1 [10](#per-rammemper1)](#per-rammemper1)

[5.1.2.1 Design Rationale
[10](#design-rationale-1)](#design-rationale-1)

[5.2 Server Runables [10](#server-runables)](#server-runables)

[5.3 Interrupt Functions
[10](#interrupt-functions)](#interrupt-functions)

[5.3.1 RamMemLclRamSngBitEcc
[10](#rammemlclramsngbitecc)](#rammemlclramsngbitecc)

[5.3.1.1 Design Rationale
[10](#design-rationale-2)](#design-rationale-2)

[5.3.2 RamMemGlbRamSngBitEcc
[10](#rammemglbramsngbitecc)](#rammemglbramsngbitecc)

[5.3.2.1 Design Rationale
[10](#design-rationale-3)](#design-rationale-3)

[5.4 Module Internal (Local) Functions
[10](#module-internal-local-functions)](#module-internal-local-functions)

[5.4.1 Local Function \#1 [10](#local-function-1)](#local-function-1)

[5.4.1.1 Design Rationale
[10](#design-rationale-4)](#design-rationale-4)

[5.4.2 Local Function \#2 [11](#local-function-2)](#local-function-2)

[5.4.2.1 Design Rationale
[11](#design-rationale-5)](#design-rationale-5)

[5.4.3 Local Function \#3 [11](#local-function-3)](#local-function-3)

[5.4.3.1 Design Rationale
[11](#design-rationale-6)](#design-rationale-6)

[5.5 GLOBAL Function/Macro Definitions
[11](#global-functionmacro-definitions)](#global-functionmacro-definitions)

[5.5.1 GLOBAL Function \#1 [11](#global-function-1)](#global-function-1)

[5.5.1.1 Design Rationale
[11](#design-rationale-7)](#design-rationale-7)

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

Module Design Document for Implementation details of RamMem component
from CM103B FDD.

# RamMem & High-Level Description

Diagnostics related to RAM memory - Local, periperal and I-Cache.

# Design details of software module

## Graphical representation of RamMem

<img
src="ElectricPowerSteering_RH850_FORD_T3T6_website/docs/CM103B_RamMem_Impl/doc/mediax/media/image1.png"
style="width:3.16575in;height:1.4098in" />

## Data Flow Diagram

### Component level DFD

> Refer FDD

### Function level DFD

> Refer FDD

# Constant Data Dictionary

## Program (fixed) Constants

### Embedded Constants

#### Local Constants

| Constant Name                             | Resolution | Units | Value       |
|-------------------------------------------|------------|-------|-------------|
| LCLRAMSNGBITCNTRMAX_CNT_U08               | uint8      | Cnt   | 100U        |
| GLBRAMSNGBITCNTRMAX_CNT_U08               | uint8      | Cnt   | 100U        |
| PRPHLRAMSNGBITECCRDACSERRDETD_CNT_U32     | uint32     | Cnt   | 0x00000002U |
| PRPHLRAMSNGBITECCERRADDRSAVED_CNT_U32     | uint32     | Cnt   | 0x00010000U |
| PRPHLRAMSNGBITECCERRDETDFLGCLRMSK_CNT_U32 | uint32     | Cnt   | 0X00000200U |
| PRPHLRAMDBLBITECCRDACSERRDETD_CNT_U32     | uint32     | Cnt   | 0x00000004U |
| PRPHLRAMDBLBITECCERRADDRSAVED_CNT_U32     | uint32     | Cnt   | 0x00020000U |
| PRPHLRAMDBLBITECCERRDETDFLGCLRMSK_CNT_U32 | uint32     | Cnt   | 0X00000400U |
| DTSRAMSNGBITECCRDACSERRDETD_CNT_U32       | uint32     | Cnt   | 0X00008000U |
| DTSRAMSNGBITECCERRADRMSK_CNT_U32          | uint32     | Cnt   | 0X00000FFFU |
| DTSRAMSNGBITECCERRDETDFLGCLRMSK_CNT_U32   | uint32     | Cnt   | 0X00008000U |
| INSTRCACHEBNK0SNGBITECCERRDETD_CNT_U32    | uint32     | Cnt   | 0x00000001U |
| INSTRCACHEBNK1SNGBITECCERRDETD_CNT_U32    | uint32     | Cnt   | 0x00000100U |
| INSTRCACHEBNK0DBLBITECCERRDETD_CNT_U32    | uint32     | Cnt   | 0x00000002U |
| INSTRCACHEBNK1DBLBITECCERRDETD_CNT_U32    | uint32     | Cnt   | 0x00000200U |
| INSTRCACHESNGBITECCFLGCLRMSK_CNT_U32      | uint32     | Cnt   | 0X00000003U |
| INSTRCACHEDBLBITECCFLGCLRMSK_CNT_U32      | uint32     | Cnt   | 0X00000003U |
| INSTRCACHEECCFLTECMCLRMSK_CNT_U32         | uint32     | Cnt   | 0x00040000U |
| CSIHRAMECCDBLBITECMCLRMSK_CNT_U32         | uint32     | Cnt   | 0x00200000U |
| MCANRAMECCDBLBITECMCLRMSK_CNT_U32         | uint32     | Cnt   | 0x00400000U |
| FRRAMECCDBLBITECMCLRMSK_CNT_U32           | uint32     | Cnt   | 0x01000000U |
| GTMRAMECCDBLBITECMCLRMSK_CNT_U32          | uint32     | Cnt   | 0x02000000U |
| DTSRAMECCSNGBITECMCLRMSK_CNT_U32          | uint32     | Cnt   | 0x00000200U |
| CSIHRAMECCSNGBITECMCLRMSK_CNT_U32         | uint32     | Cnt   | 0x00200000U |
| MCANRAMECCSNGBITECMCLRMSK_CNT_U32         | uint32     | Cnt   | 0x00400000U |
| FRRAMECCSNGBITECMCLRMSK_CNT_U32           | uint32     | Cnt   | 0x01000000U |
| GTMRAMECCSNGBITECMCLRMSK_CNT_U32          | uint32     | Cnt   | 0x02000000U |
| LCLRAMECCSNGBITSOFTFLTPRMBYTE_CNT_U08     | uint8      | Cnt   | 0x01U       |
| GLBRAMECCSNGBITSOFTFLTPRMBYTE_CNT_U08     | uint8      | Cnt   | 0x02U       |
| INSTRCACHEECCFLTPRMBYTE_CNT_U08           | uint8      | Cnt   | 0x04U       |
| DTSRAMECCSNGBITFLTPRMBYTE_CNT_U08         | uint8      | Cnt   | 0x08U       |
| MCANRAMECCSNGBITFLTPRMBYTE_CNT_U08        | uint8      | Cnt   | 0x10U       |
| FRRAMECCSNGBITFLTPRMBYTE_CNT_U08          | uint8      | Cnt   | 0x20U       |
| CSIHRAMECCSNGBITFLTPRMBYTE_CNT_U08        | uint8      | Cnt   | 0x40U       |
| GTMRAMECCSNGBITFLTPRMBYTE_CNT_U08         | uint8      | Cnt   | 0x80U       |
| CSIHRAMECCDBLBITFLTPRMBYTE_CNT_U08        | uint8      | Cnt   | 0x02U       |
| MTTCANRAMDBLBITECCERRPRMBYTE_CNT_U08      | uint8      | Cnt   | 0x02U       |
| MCAN0RAMDBLBITECCERRPRMBYTE_CNT_U08       | uint8      | Cnt   | 0x08U       |
| MCAN1RAMDBLBITECCERRPRMBYTE_CNT_U08       | uint8      | Cnt   | 0x20U       |
| FRMRAMDBLBITECCERRPRMBYTE_CNT_U08         | uint8      | Cnt   | 0x02U       |
| FRTBUFADBLBITECCERRPRMBYTE_CNT_U08        | uint8      | Cnt   | 0x08U       |
| FRTBUFBDBLBITECCERRPRMBYTE_CNT_U08        | uint8      | Cnt   | 0x20U       |
| LCLRAMWORDLINERDADROFFS_CNT_U32           | uint32     | Cnt   | 0x00000010U |
| LCLRAMWORDLINEADRMSK_CNT_U32              | uint32     | Cnt   | 0xFFFFFF8FU |
| GLBRAMWORDLINERDADROFFS_CNT_U32           | uint32     | Cnt   | 0x00000008U |
| GLBRAMWORDLINEADRMSK_CNT_U32              | uint32     | Cnt   | 0xFFFFFFC7U |
| LCLRAMECCSEDECMFLGCLRMASK_CNT_U32         | uint32     | Cnt   | 0x00010000U |
| GLBRAMECCSEDECMFLGCLRMASK_CNT_U32         | uint32     | Cnt   | 0x00020000U |
| LCLRAMBASADR_CNT_U32                      | uint32     | Cnt   | 0xFEBE0000U |
| LCLRAMSEDERRBASADRBNK0_CNT_U32            | uint32     | Cnt   | 0xFEBC0000U |
| LCLRAMSEDERRBASADRBNK1_CNT_U32            | uint32     | Cnt   | 0xFEBC0004U |
| LCLRAMSEDERRBASADRBNK2_CNT_U32            | uint32     | Cnt   | 0xFEBC0008U |
| LCLRAMSEDERRBASADRBNK3_CNT_U32            | uint32     | Cnt   | 0xFEBC000CU |
| GLBRAMBASADR_CNT_U32                      | uint32     | Cnt   | 0xFEED8000U |
| GLBRAMSEDERRBASADR_CNT_U32                | uint32     | Cnt   | 0xFEE00000U |
| GLBRAMSEDERRADRSTRT_CNT_U32               | uint32     | Cnt   | 0xFFC64040U |
| LCLRAMBNK0SEDERRADRSTRT_CNT_U32           | uint32     | Cnt   | 0xFFC65460U |
| LCLRAMBNK1SEDERRADRSTRT_CNT_U32           | uint32     | Cnt   | 0xFFC65464U |
| LCLRAMBNK2SEDERRADRSTRT_CNT_U32           | uint32     | Cnt   | 0xFFC65468U |
| LCLRAMBNK3SEDERRADRSTRT_CNT_U32           | uint32     | Cnt   | 0xFFC6546CU |
| SIZEOFRAMSNGBITECCERRADRREG_CNT_U08       | uint8      | Cnt   | 4U          |
| NROFGLBRAMSEDERRADRREG_CNT_U08            | uint8      | Cnt   | 32U         |
| NROFRAMADRINWORDLINE_CNT_U08              | uint8      | Cnt   | 8U          |
| NROFLCLRAMSEGPERBNK_CNT_U08               | uint8      | Cnt   | 8U          |
| NROFLCLRAMMEMBNK_CNT_U08                  | uint8      | Cnt   | 4U          |
| LCLRAMBNKLOGLADROFFS_CNT_U32              | uint32     | Cnt   | 4U          |
| LCLRAMBNK0SNGBITERRMONREGMASK_CNT_U32     | uint32     | Cnt   | 0x11111111U |
| LCLRAMBNK1SNGBITERRMONREGMASK_CNT_U32     | uint32     | Cnt   | 0x22222222U |
| LCLRAMBNK2SNGBITERRMONREGMASK_CNT_U32     | uint32     | Cnt   | 0x44444444U |
| LCLRAMBNK3SNGBITERRMONREGMASK_CNT_U32     | uint32     | Cnt   | 0x88888888U |
| LCLRAMWORDLINERDADROFFS_CNT_U32           | uint32     | Cnt   | 0x00000010U |
| LCLRAMWORDLINEADRMASK_CNT_U32             | uint32     | Cnt   | 0xFFFFFF8FU |
| GLBRAMWORDLINERDADROFFS_CNT_U32           | uint32     | Cnt   | 0x00000008U |
| GLBRAMWORDLINEADRMASK_CNT_U32             | uint32     | Cnt   | 0xFFFFFFC7U |

# Software Component Implementation

## Sub-Module Functions

## Init: RamMemInit1

## Design Rationale

Refer FDD document.

## Per: RamMemPer1

## Design Rationale

Refer FDD document.

## Server Runables 

> None

## Interrupt Functions

## RamMemLclRamSngBitEcc

## Design Rationale

Refer to the FDD document.

## RamMemGlbRamSngBitEcc

## Design Rationale

Refer to the FDD document.

## Module Internal (Local) Functions

## Local Function \#1

|                      |                      |      |     |     |
|----------------------|----------------------|------|-----|-----|
| **Function Name**    | SpiEccErrChkAndHndlg | Type | Min | Max |
| **Arguments Passed** | None                 | \-   | \-  | \-  |
| **Return Value**     | N/A                  | \-   | \-  | \-  |

## Design Rationale

> Handles RAM single and double bit ECC error checking for Spi
> peripheral \[CSIH0-3\].
>
> Called from the periodic runnable RamMemPer1

## Local Function \#2

|                      |                       |      |     |     |
|----------------------|-----------------------|------|-----|-----|
| **Function Name**    | MCanEccErrChkAndHndlg | Type | Min | Max |
| **Arguments Passed** | None                  | \-   | \-  | \-  |
| **Return Value**     | N/A                   | \-   | \-  | \-  |

## Design Rationale

> Handles RAM single and double bit ECC error checking for MCAN
> peripheral \[MTTCAN,MCAN0 and MCAN1\].

Called from the periodic runnable RamMemPer1

## Local Function \#3

|                      |                     |      |     |     |
|----------------------|---------------------|------|-----|-----|
| **Function Name**    | FrEccErrChkAndHndlg | Type | Min | Max |
| **Arguments Passed** | None                | \-   | \-  | \-  |
| **Return Value**     | N/A                 | \-   | \-  | \-  |

## Design Rationale

> Handles RAM single and double bit ECC error checking for FlexRay
> peripheral \[MRAM,TBF A,TBF B\].

Called from the periodic runnable RamMemPer1

1.  **Local Function \#4**

|                      |                         |      |     |     |
|----------------------|-------------------------|------|-----|-----|
| **Function Name**    | GtmRamEccErrChkAndHndlg | Type | Min | Max |
| **Arguments Passed** | None                    | \-   | \-  | \-  |
| **Return Value**     | N/A                     | \-   | \-  | \-  |

1.  **Design Rationale**

> Handles RAM single bit ECC error checking for GTM peripheral..

Called from the periodic runnable RamMemPer1

1.  **Local Function \#4**

|                      |                          |        |     |            |
|----------------------|--------------------------|--------|-----|------------|
| **Function Name**    | RamFailrModClassnChk     | Type   | Min | Max        |
| **Arguments Passed** | LclRamFailrAdr_Cnt_T_u32 | uint32 | 0   | 4294967295 |
|                      | ErrClrMask_Cnt_T_u32     | uint32 | 0   | 4294967295 |
| **Return Value**     | N/A                      | \-     | \-  | \-         |

1.  **Design Rationale**

None

## GLOBAL Function/Macro Definitions

## GLOBAL Function \#1

|                      |       |      |     |     |
|----------------------|-------|------|-----|-----|
| **Function Name**    | None. | Type | Min | Max |
| **Arguments Passed** | \-    | \-   | \-  | \-  |
| **Return Value**     | \-    | \-   | \-  | \-  |

## Design Rationale

> N/A

# Known Limitations with Design

Design updates dRamMemFrRamTmpBufBDblBitEccErrAdr and
dRamMemFrRamTmpBufADblBitEccErrAdr in the wrong places. They should be
intercahnged. Corrected in code.

The NTC parameter bytes are also interchanged for the above.

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

| **Ref. \#** | **Title**                                                                                                                                                           | **Version**                    |
|-------|-------------------------------------------|-----------------------|
| 1           | AUTOSAR Specification of Memory Mapping                                                                                                                             | v1.3.0 R4.0 Rev 2              |
| 2           | MDD Guideline                                                                                                                                                       | EA4 01.00.01                   |
| 3           | [Software Naming Conventions.doc](http://misagweb01.nexteer.com/eRoomReq/Files/erooms8/NextGeneration/0_fc55f/Software%20Naming%20Conventions%2003x(In%20Work).doc) | 01.01.00                       |
| 4           | Software Design and Coding Standards.doc                                                                                                                            | 2.1                            |
| 5           | Functional Design Document: CM103B_RamMem_Design                                                                                                                    | See Synergy SubProject Version |

{% endraw %}