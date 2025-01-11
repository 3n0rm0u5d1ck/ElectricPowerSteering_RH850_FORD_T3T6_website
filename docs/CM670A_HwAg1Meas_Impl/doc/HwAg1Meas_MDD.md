---
layout: default
title: HwAg1Meas_MDD
nav_order: 2
parent: Component Implementation
---
{% raw %}
**Module Design Document**

**For**

**HwAg1Meas**

**14-Aug-2017**

**Prepared For:**

**Software Engineering**

**Nexteer Automotive,**

**Saginaw, MI, USA**

**Prepared By:**

**Software Engineering,**

**Nexteer Automotive,**

**Saginaw, MI, USA**

**  
<u>Change History</u>**

|                                                                       |                    |             |              |
|------------------------|---------------------|--------------|--------------|
| **Description**                                                       | **Author**         | **Version** | **Date**     |
| Initial Version                                                       | Selva Sengottaiyan | 1.0         | 21-July-2015 |
| Updated to v1.2.0 of the FDD                                          | Selva Sengottaiyan | 2.0         | 11-Sep-2015  |
| Updated to v1.4.0 of the FDD                                          | Selva Sengottaiyan | 3.0         | 23-Dec-2015  |
| Updated to v1.11.0 of the FDD                                         | Ramachandran       | 4.0         | 21-Jun-2016  |
| Updated for v2.1.0                                                    | KK                 | 5.0         | 11-Apr-2017  |
| Updated server runnable names to match DataDict.m and updated graphic | Brionna Spencer    | 6.0         | 14-Aug-2017  |

**  
**

<u>Table of Contents</u>

1 Introduction 5

1.1 Purpose 5

1.2 Scope 5

2 HwAg1Meas High-Level Description 6

3 Design details of software module 7

3.1 Graphical representation of HwAg1Meas 7

3.2 Data Flow Diagram 7

3.2.1 Component level DFD 7

3.2.2 Function level DFD 7

4 Constant Data Dictionary 8

4.1 Program (fixed) Constants 8

4.1.1 Embedded Constants 8

5 Software Component Implementation 9

5.1 Sub-Module Functions 9

5.1.1 Init: HwAg1MeasInit1 9

5.1.1.1 Design Rationale 9

5.1.2 Per: HwAg1MeasPer1 9

5.1.2.1 Design Rationale 9

5.1.3 Per: HwAg1MeasPer2 9

5.1.3.1 Design Rationale 9

5.1.4 Per: HwAg1MeasPer3 9

5.1.4.1 Design Rationale 9

5.1.5 Per: HwAg1MeasPer4 9

5.1.5.1 Design Rationale 9

5.1.6 Per: HwAg1MeasPer5 9

5.1.6.1 Design Rationale 9

5.2 Server Runnables 10

5.2.1 HwAg1AutTrim 10

5.2.1.1 Design Rationale 10

5.2.2 HwAg1ClrLtch 10

5.2.2.1 Design Rationale 10

5.2.3 HwAg1ClrTrim 10

5.2.3.1 Design Rationale 10

5.2.4 HwAg1ReadTrim 10

5.2.4.1 Design Rationale 10

5.2.5 HwAg1TrimPrfmdSts 10

5.2.5.1 Design Rationale 10

5.2.6 HwAg1WrTrim 10

5.2.6.1 Design Rationale 10

5.3 Interrupt Functions 10

5.4 Module Internal (Local) Functions 11

5.4.1 Local Function \#1 11

5.4.1.1 Design Rationale 11

5.4.2 Local Function \#2 11

5.4.2.1 Design Rationale 11

5.4.3 Local Function \#3 11

5.4.3.1 Design Rationale 11

6 Known Limitations with Design 12

7 UNIT TEST CONSIDERATION 13

Appendix A Abbreviations and Acronyms 14

Appendix B Glossary 15

Appendix C References 16

# Introduction

## Purpose

Refer to FDD.

## Scope

# HwAg1Meas High-Level Description

Refer to FDD

# Design details of software module

## Graphical representation of HwAg1Meas

<img
src="ElectricPowerSteering_RH850_FORD_T3T6_website/docs/CM670A_HwAg1Meas_Impl/doc/mediax/media/image1.png"
style="width:3.80333in;height:4.55in" />

## Data Flow Diagram

### Component level DFD

Refer to FDD

### Function level DFD

Refer to FDD

# Constant Data Dictionary

## Program (fixed) Constants

### Embedded Constants

#### Local Constants

| Constant Name               | Resolution | Units    | Value        |
|-----------------------------|------------|----------|--------------|
| MAXWAITININ_MICROSEC_U32    | 1          | MicroSec | 2U           |
| DATAAVLMAXWAIT_MICROSEC_U32 | 1          | MicroSec | 300U         |
| COMSTSMAXWAIT_MICROSEC_U32  | 1          | MicroSec | 5U           |
| PRTCLFLTMASK_CNT_U32        | 1          | Cnt      | 0xFEU        |
| SNSRIDMASK_CNT_U08          | 1          | Cnt      | 0x00FU       |
| MSGSTSMASK_CNT_U08          | 1          | Cnt      | 0x01U        |
| COMSTSMASK_CNT_U32          | 1          | Cnt      | 0x30000000UL |
| DATAMASK_CNT_U16            | 1          | Cnt      | 0xFFF0U      |

*\* Refer to FDD for other constant definitions*

# Software Component Implementation

## Sub-Module Functions

## Init: HwAg1MeasInit1

## Design Rationale

None

## Per: HwAg1MeasPer1

## Design Rationale

None

## Per: HwAg1MeasPer2

## Design Rationale

None

## Per: HwAg1MeasPer3

## Design Rationale

None

## Per: HwAg1MeasPer4

## Design Rationale

None

## Per: HwAg1MeasPer5

## Design Rationale

The implementation brings in the block “HwAg1Final” inside the True
Condition of the “finalAbsAg” as the other error condition will just
retain the previous value and rolling counter will not change. It saves
extra instructions in the implementation to the match the FDD. Final
Functionality is still the same.

## Server Runnables 

## HwAg1AutTrim

## Design Rationale

None

## HwAg1ClrLtch

## Design Rationale

None

## HwAg1ClrTrim

## Design Rationale

None

## HwAg1ReadTrim

## Design Rationale

None

## HwAg1TrimPrfmdSts

## Design Rationale

None

## HwAg1WrTrim

## Design Rationale

None

## Interrupt Functions

None

## Module Internal (Local) Functions

### Local Function \#1

|                      |                      |         |      |     |
|----------------------|----------------------|---------|------|-----|
| **Function Name**    | CalcHwAgIdx          | Type    | Min  | Max |
| **Arguments Passed** | HwAgStep_HwDeg_T_f32 | float32 | -900 | 900 |
| **Return Value**     | Index_Cnt_T_u08      | uint16  | 0    | 22  |

## Design Rationale

The implementation deviates from the FDD block “Intpn” block. The
implementation finds the minimum of absolute values of the difference
between HwAg1Step with all the values from the Calibration table and
find the index associated with minimum value of the difference in the
calibration table.

## Local Function \#2

|                      |                             |      |     |     |
|----------------------|-----------------------------|------|-----|-----|
| **Function Name**    | ReadRegister                | Type | Min | Max |
| **Arguments Passed** | RegisterDummyRead_Cnt_T_u32 | N/A  | N/A | N/A |
| **Return Value**     | RegisterDummyRead_Cnt_T_u32 | N/A  | N/A | N/A |

## Design Rationale

This function can be used both for read-and-use and for
read-and-discard.

## Local Function \#3

|                      |                     |          |               |               |
|--------------|-------------------------|----------|-------------|-----------|
| **Function Name**    | UpdtLthOnValChng    | Type     | Min           | Max           |
| **Arguments Passed** | SigQlfrIfNtc_T_enum | SigQlfr1 | SIGQLFR_NORES | SIGQLFR_FAILD |
| **Return Value**     | NA                  | N/A      | N/A           | N/A           |

## Design Rationale

This function is split from Per4 to reduce path count and cyclomatic
complexity.

Path in Model: CM670A_HwAg1Meas/HwAg1Meas/HwAg1MeasPer4/HwAgRead/Update
Latch on value change

# Known Limitations with Design

None

# UNIT TEST CONSIDERATION

-   Roll Over is intentional for

    -   \*Rte_Pim_HwAg1Snsr0ComStsErrCntr()

    -   \*Rte_Pim_HwAg1Snsr0IdErrCntr()

    -   \*Rte_Pim_HwAg1Snsr0IntSnsrErrCntr()

    -   \*Rte_Pim_HwAg1Snsr0NoMsgErrCntr()

    -   \*Rte_Pim_HwAg1Snsr1ComStsErrCntr()

    -   \*Rte_Pim_HwAg1Snsr1IdErrCntr()

    -   \*Rte_Pim_HwAg1Snsr1IntSnsrErrCntr()

    -   \*Rte_Pim_HwAg1Snsr1NoMsgErrCntr()

    -   (\*Rte_Pim_HwAg1PrevRollCnt).

-   Thus, counter acts in circular

####### Abbreviations and Acronyms

| **Abbreviation or Acronym** | **Description**        |
|-----------------------------|------------------------|
| MDD                         | Module Design Document |
| DFD                         | Data Flow Diagram      |

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

|     |     |     |
|-----|-----|-----|
|     |     |     |
|     |     |     |

####### References

| **Ref. \#** | **Title**                               | **Version**                     |
|-------|-------------------------------------------------|-----------------|
| 1           | AUTOSAR Specification of Memory Mapping | v1.3.0 R4.0 Rev 2               |
| 2           | MDD Guideline                           | EA4 01.00.01                    |
| 3           | EA4 Software Naming Conventions         | 01.01.00                        |
| 4           | Software Design and Coding Standards    | 2.1                             |
| 5           | FDD - CM670A_HwAg1Meas_Design           | See Synergy sub project version |

{% endraw %}