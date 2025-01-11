---
layout: default
title: HwAgSysArbn_MDD
nav_order: 3
parent: Component Implementation
---
{% raw %}
**Module Design Document**

**For**

**HwAgSysArbn**

**Oct** **31, 2017**

**Prepared By:**

**Matthew Leser,**

**Nexteer Automotive,**

**Saginaw, MI, USA**

**<u>Change History</u>**

|             |                                                    |                                |             |              |
|------|---------------------------------|-----------|----------|-------------|
| **Sl. No.** | **Description**                                    | **Author**                     | **Version** | **Date**     |
| 1           | Initial Version                                    | Sarika Natu(KPIT Technologies) | 1.0         | 07-Sept-2015 |
| 2           | SF045A_HwAgSysArbn_Design version 2 implementation | SB                             | 2.0         | 20-Jun-2016  |
| 3           | Updated to design version 2.2.0                    | TATA                           | 3.0         | 07-Dec-16    |
| 4           | Updated to design version 2.4.0                    | KK                             | 4.0         | 28-Feb-17    |
| 5           | Updated graph and added new function               | ML                             | 5.0         | 19-Jul-2017  |
| 6           | Added new function                                 | ML                             | 6.0         | 11-Oct-2017  |
| 7           | Updated Graph                                      | ML                             | 7.0         | 31-Oct-2017  |

**  
**

<u>Table of Contents</u>

[1 Design details of software module
[5](#design-details-of-software-module)](#design-details-of-software-module)

[1.1 Graphical representation of HwAgSysArbn
[5](#graphical-representation-of-hwagsysarbn)](#graphical-representation-of-hwagsysarbn)

[1.2 Data Flow Diagram [5](#data-flow-diagram)](#data-flow-diagram)

[1.2.1 Component level DFD
[5](#component-level-dfd)](#component-level-dfd)

[1.2.2 Function level DFD [5](#function-level-dfd)](#function-level-dfd)

[2 Constant Data Dictionary
[6](#constant-data-dictionary)](#constant-data-dictionary)

[2.1 Program (fixed) Constants
[6](#program-fixed-constants)](#program-fixed-constants)

[2.1.1 Embedded Constants [6](#embedded-constants)](#embedded-constants)

[3 Software Component Implementation
[7](#software-component-implementation)](#software-component-implementation)

[3.1 Sub-Module Functions
[7](#sub-module-functions)](#sub-module-functions)

[3.1.1 Init: HwAgSysArbn_Init1
[7](#init-hwagsysarbninit1)](#init-hwagsysarbninit1)

[3.1.1.1 Design Rationale [7](#design-rationale)](#design-rationale)

[3.1.1.2 Module Outputs [7](#module-outputs)](#module-outputs)

[3.1.2 Per: HwAgSysArbn_Per1
[7](#per-hwagsysarbn_per1)](#per-hwagsysarbn_per1)

[3.1.2.1 Design Rationale [7](#design-rationale-1)](#design-rationale-1)

[3.1.2.2 Store Module Inputs to Local copies
[7](#store-module-inputs-to-local-copies)](#store-module-inputs-to-local-copies)

[3.1.2.3 (Processing of function)………
[7](#processing-of-function)](#processing-of-function)

[3.1.2.4 Store Local copy of outputs into Module Outputs
[7](#store-local-copy-of-outputs-into-module-outputs)](#store-local-copy-of-outputs-into-module-outputs)

[3.2 Server Runables [7](#server-runnables)](#server-runnables)

[3.3 Interrupt Functions
[7](#interrupt-functions)](#interrupt-functions)

[3.4 Module Internal (Local) Functions
[7](#module-internal-local-functions)](#module-internal-local-functions)

[3.4.1 Local Function \#1 [7](#_Toc488233003)](#_Toc488233003)

[3.4.1.1 Design Rationale [8](#design-rationale-3)](#design-rationale-3)

[3.4.1.2 Processing [8](#processing-1)](#processing-1)

[3.4.2 Local Function \#2 [8](#local-function-3)](#local-function-3)

[3.4.2.1 Design Rationale [8](#design-rationale-4)](#design-rationale-4)

[3.4.2.2 Processing [8](#processing-2)](#processing-2)

[3.4.3 Local Function \#3 [8](#local-function-4)](#local-function-4)

[3.4.3.1 Design Rationale [8](#design-rationale-5)](#design-rationale-5)

[3.4.3.2 Processing [8](#processing-3)](#processing-3)

[3.5 GLOBAL Function/Macro Definitions
[9](#global-functionmacro-definitions)](#global-functionmacro-definitions)

[4 Known Limitations with Design
[10](#known-limitations-with-design)](#known-limitations-with-design)

[5 UNIT TEST CONSIDERATION
[11](#unit-test-consideration)](#unit-test-consideration)

[Appendix A References [12](#references)](#references)

**HwAgSysArbn & High-Level Description**

The Handwheel angle system arbitration function accepts inputs from the
various angle sources available in the EPS system and selects the angle
source to be used for the system handwheel angle value. It also provides
for compliance compensation of the angle value and determines the angle
value and angle validity to be output on the vehicle data bus.

# Design details of software module

## Graphical representation of HwAgSysArbn

<img
src="ElectricPowerSteering_RH850_FORD_T3T6_website/docs/SF045A_HwAgSysArbn_Impl/doc/mediax/media/image2.png"
style="width:3.05912in;height:4.10473in" />

## Data Flow Diagram

See FDD.

### Component level DFD

See FDD.

### Function level DFD

See FDD.

# Constant Data Dictionary

## Program (fixed) Constants

### Embedded Constants

#### Local Constants

Refer .m file

# Software Component Implementation

## Sub-Module Functions

## Init: HwAgSysArbnInit1

## Design Rationale

*Refer FDD*

## Module Outputs

*Refer FDD*

## Per: HwAgSysArbn_Per1

## Design Rationale

## Store Module Inputs to Local copies

*Refer FDD*

##  (Processing of function)………

*Refer FDD*

## Store Local copy of outputs into Module Outputs

*Refer FDD*

## Server Runnables 

None

## Interrupt Functions

None

## Module Internal (Local) Functions

## Local Function \#1

|                   |                            |         |         |        |
|-------------------|----------------------------|---------|---------|--------|
| **Function Name** | VldtSnsrlsData             | Type    | Min     | Max    |
| Arguments Passed  | HwAgSnsrls_HwDeg_T_f32     | float32 | -1440.0 | 1440.0 |
|                   | HwAgSnsrlsConfIn_Uls_T_f32 | float32 | 0.0     | 1.0    |
| **Return Value**  | HwAgSnsrlsConf_Uls_T_f32   | float32 | 0.0     | 1.0    |

## Design Rationale

Done to reduce Path Count

## Processing

Refer to the Handwheel signal serial communication arbitration
functionality of “VldtSnsrlsData” subsystem in the Simulink model.

## Local Function \#2

|                   |                                    |         |        |       |
|---------------|--------------------------------|---------|---------|---------|
| **Function Name** | HwAgVelSerlCom                     | Type    | Min    | Max   |
| Arguments Passed  | HwAgCorrdConf_Uls_T_f32            | uint8   | 0      | 1     |
|                   | HwAgSnsrlsConf_Uls_T_f32           | uint8   | 0      | 1     |
|                   | HwAgCorrd_HwDeg_T_f32              | float32 | -1440  | 1440  |
|                   | HwAgSnsrls_HwDeg_T_f32             | float32 | -1440  | 1440  |
|                   | HwVel_HwRadPerSec_T_f32            | float32 | -42.0F | 42.0F |
|                   | PinionVelConf_Uls_T_f32            | float32 | 0.0F   | 1.0F  |
|                   | \*HwAgStsToSerlCom_Cnt_T_lgc       | boolean | FALSE  | TRUE  |
|                   | \*HwVelToSerlCom_HwRadPerSec_T_f32 | float32 | -42.0F | 42.0F |
| **Return Value**  | HwAgToSerlCom_HwDeg_T_f32          | float32 | -1440  | 1440  |

## Design Rationale

None

## Processing

Refer to the Handwheel signal serial communication arbitration
functionality of “HwAgVelSerlCom” subsystem in the Simulink model.

## Local Function \#3

|                   |                                |         |          |         |
|---------------|--------------------------------|---------|---------|---------|
| **Function Name** | CalcPinionVel                  | Type    | Min      | Max     |
| Arguments Passed  | HwTq_HwNwtMtr_T_f32            | float32 | -10.0F   | 10.0F   |
|                   | MotVelCrf_MotRadPerSec_T_f32   | float32 | -1350.0F | 1350.0F |
|                   | MotVelVld_Cnt_T_logl           | boolean | FALSE    | TRUE    |
|                   | PinionAgConf_Uls_T_f32         | float32 | 0.0F     | 1.0F    |
|                   | HwAg_HwDeg_T_f32               | float32 | -1440.0F | 1440.0F |
|                   | \* PinionVel_HwRadPerSec_T_f32 | float32 | -42.0F   | 42.0F   |
|                   | \* PinionVelConf_Uls_T_f32     | float32 | 0.0F     | 1.0F    |
| **Return Value**  | HwVel_HwRadPerSec_T_f32        | float32 | -42.0F   | 42.0F   |

## Design Rationale

None

## Processing

Refer to the functionality of “CalcPinionVel” subsystem in the Simulink
model.

## Local Function \#4

|                   |                       |       |     |     |
|-------------------|-----------------------|-------|-----|-----|
| **Function Name** | HwPosnSigLoNTCSet     | Type  | Min | Max |
| Arguments Passed  | HwAgIdptSig_Cnt_T_u08 | uint8 | 0U  | 2U  |
| **Return Value**  | None                  |       |     |     |

## Design Rationale

Done to reduce Path Count.

## Processing

None

## GLOBAL Function/Macro Definitions

None

# Known Limitations with Design

None

# UNIT TEST CONSIDERATION

For the switch case in Per1, the input ‘HwAgIdptSig_Cnt_T_u08’ will need
to go out of range to reach default case.

####### References

| **Ref. \#** | **Title**                                                                                                                                                             | **Version**                    |
|-------|-------------------------------------------------|-----------------|
| 1           | AUTOSAR Specification of Memory Mapping (Link:[AUTOSAR_SWS_MemoryMapping.pdf](http://www.autosar.org/download/R4.0/AUTOSAR_SWS_MemoryMapping.pdf))                    | v1.3.0 R4.0 Rev 2              |
| 2           | MDD Guideline                                                                                                                                                         | Process Release 04.02.01       |
| 3           | [Software Naming Conventions.doc](http://misagweb01.nexteer.com/eRoomReq/Files/erooms8/NextGeneration/0_fc55f/Software%20Naming%20Conventions%2003x(In%20Work).doc)   | 2.0                            |
| 4           | [Software Design and Coding Standards.doc](http://eroom1.nexteer.com/eRoomReq/Files/erooms8/NextGeneration/0_1a67a9/Software%20Design%20and%20Coding%20Standards.doc) | 2.1                            |
| 5           | SF045A_HwAgSysArbn_Design                                                                                                                                             | See Synergy subproject version |

{% endraw %}