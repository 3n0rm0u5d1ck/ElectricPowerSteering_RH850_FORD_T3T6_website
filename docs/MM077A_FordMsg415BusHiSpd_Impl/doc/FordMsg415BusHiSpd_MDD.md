---
layout: default
title: FordMsg415BusHiSpd_MDD
nav_order: 2
parent: Component Implementation
---
{% raw %}
**Module Design Document**

**For**

**FordMsg415BusHiSpd**

**June 19, 20157**

**Prepared For:**

**Software Engineering**

**Nexteer Automotive,**

**Saginaw, MI, USA**

**Prepared By:**

**Tata Elxsi,**

**Trivandrum, INDIA**

**<u>Change History</u>**

|                 |        |         |             |
|-----------------|--------|---------|-------------|
| Description     | Author | Version | Date        |
| Initial Version | TATA   | 1.0     | 23-Nov-2017 |

**<u>Table of Contents</u>**

[1 Introduction [5](#introduction)](#introduction)

[1.1 Purpose [5](#purpose)](#purpose)

[2 FordMsg415BusHiSpd & High-Level Description
[6](#fordmsg415bushispd-high-level-description)](#fordmsg415bushispd-high-level-description)

[3 Design details of software module
[7](#design-details-of-software-module)](#design-details-of-software-module)

[3.1 Graphical representation of FordMsg415BusHiSpd
[7](#graphical-representation-of-fordmsg415bushispd)](#graphical-representation-of-fordmsg415bushispd)

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

[5.1.1 Init: FordMsg415BusHiSpdInit1
[9](#init-fordmsg415bushispdinit1)](#init-fordmsg415bushispdinit1)

[5.1.1.1 Design Rationale [9](#design-rationale)](#design-rationale)

[5.1.1.2 Module Outputs [9](#module-outputs)](#module-outputs)

[5.1.2 Per: FordMsg415BusHiSpdPer1
[9](#per-fordmsg415bushispdper1)](#per-fordmsg415bushispdper1)

[5.1.2.1 Design Rationale [9](#design-rationale-1)](#design-rationale-1)

[5.1.2.2 Store Module Inputs to Local copies
[9](#store-module-inputs-to-local-copies)](#store-module-inputs-to-local-copies)

[5.1.2.3 Processing of function)
[9](#processing-of-function)](#processing-of-function)

[5.1.2.4 Store Local copy of outputs into Module Outputs
[9](#store-local-copy-of-outputs-into-module-outputs)](#store-local-copy-of-outputs-into-module-outputs)

[5.2 Server Runnables [9](#server-runnables)](#server-runnables)

[5.2.1 ComIPduCallout_BrakeSysFeatures_HS2
[9](#comipducallout_brakesysfeatures_hs2)](#comipducallout_brakesysfeatures_hs2)

[5.2.1.1 Design Rationale [9](#design-rationale-2)](#design-rationale-2)

[5.2.1.2 (Processing of function)
[9](#processing-of-function-1)](#processing-of-function-1)

[5.2.2 ComTimeoutNotification_Veh_V_ActlBrk
[9](#comtimeoutnotification_veh_v_actlbrk)](#comtimeoutnotification_veh_v_actlbrk)

[5.2.2.1 Design Rationale [9](#design-rationale-3)](#design-rationale-3)

[5.2.2.2 (Processing of function)
[9](#processing-of-function-2)](#processing-of-function-2)

[5.3 Interrupt Functions
[10](#interrupt-functions)](#interrupt-functions)

[5.4 Module Internal (Local) Functions
[10](#module-internal-local-functions)](#module-internal-local-functions)

[5.4.1 Local Function \#1 [10](#local-function-1)](#local-function-1)

[5.4.1.1 Design Rationale
[10](#design-rationale-4)](#design-rationale-4)

[5.4.1.2 Processing [10](#processing)](#processing)

[5.4.2 Local Function \#2 [10](#local-function-2)](#local-function-2)

[5.4.2.1 Design Rationale
[11](#design-rationale-5)](#design-rationale-5)

[5.4.2.2 Processing [11](#processing-1)](#processing-1)

[5.4.3 Local Function \#3 [11](#local-function-3)](#local-function-3)

[5.4.3.1 Design Rationale
[12](#design-rationale-6)](#design-rationale-6)

[5.4.3.2 Processing [12](#processing-2)](#processing-2)

[5.4.4 Local Function \#4 [12](#local-function-4)](#local-function-4)

[5.4.4.1 Design Rationale
[12](#design-rationale-7)](#design-rationale-7)

[5.4.4.2 Processing [12](#processing-3)](#processing-3)

[5.4.5 Local Function \#5 [12](#local-function-5)](#local-function-5)

[5.4.5.1 Design Rationale
[13](#design-rationale-8)](#design-rationale-8)

[5.4.5.2 Processing [13](#processing-4)](#processing-4)

[5.4.6 Local Function \#6 [13](#local-function-6)](#local-function-6)

[5.4.6.1 Design Rationale
[13](#design-rationale-9)](#design-rationale-9)

[5.4.6.2 Processing [13](#processing-5)](#processing-5)

[5.4.7 Local Function \#7 [13](#local-function-7)](#local-function-7)

[5.4.7.1 Design Rationale
[14](#design-rationale-10)](#design-rationale-10)

[5.4.7.2 Processing [14](#processing-6)](#processing-6)

[5.4.8 Local Function \#8 [14](#local-function-8)](#local-function-8)

[5.4.8.1 Design Rationale
[14](#design-rationale-11)](#design-rationale-11)

[5.4.8.2 Processing [14](#processing-7)](#processing-7)

[5.4.9 Local Function \#9 [14](#local-function-9)](#local-function-9)

[5.4.9.1 Design Rationale
[14](#design-rationale-12)](#design-rationale-12)

[5.4.9.2 Processing [14](#processing-8)](#processing-8)

[5.5 GLOBAL Function/Macro Definitions
[14](#global-functionmacro-definitions)](#global-functionmacro-definitions)

[6 Known Limitations with Design
[15](#known-limitations-with-design)](#known-limitations-with-design)

[7 UNIT TEST CONSIDERATION
[16](#unit-test-consideration)](#unit-test-consideration)

[Appendix A Abbreviations and Acronyms
[17](#abbreviations-and-acronyms)](#abbreviations-and-acronyms)

[Appendix B Glossary [18](#glossary)](#glossary)

[Appendix C References [19](#references)](#references)

# Introduction

## Purpose

MDD for FordMsg415BusHiSpd

# FordMsg415BusHiSpd & High-Level Description

Please refer FDD.

# Design details of software module

## Graphical representation of FordMsg415BusHiSpd

<img
src="ElectricPowerSteering_RH850_FORD_T3T6_website/docs/MM077A_FordMsg415BusHiSpd_Impl/doc/mediax/media/image1.png"
style="width:4.17708in;height:5.65625in" />

## Data Flow Diagram

### Component level DFD

Please refer FDD.

### Function level DFD

Please refer FDD.

# Constant Data Dictionary

## Program (fixed) Constants

### Embedded Constants

#### Local Constants

| Constant Name                        | Resolution | Units | Value |
|--------------------------------------|------------|-------|-------|
| Please refer Data Dictionary .m file | NA         | NA    | NA    |

# Software Component Implementation

## Sub-Module Functions

### 5.1.1 Init: FordMsg415BusHiSpdInit1 [init-fordmsg415bushispdinit1]

## Design Rationale

None

## Module Outputs

None

### 5.1.2 Per: FordMsg415BusHiSpdPer1 [per-fordmsg415bushispdper1]

## 5.1.2.1 Design Rationale [design-rationale-1]

None

## 5.1.2.2 Store Module Inputs to Local copies [store-module-inputs-to-local-copies]

None

## 5.1.2.3 Processing of function) [processing-of-function]

None

## 5.1.2.4 Store Local copy of outputs into Module Outputs [store-local-copy-of-outputs-into-module-outputs]

None

## Server Runnables 

### 5.2.1 ComIPduCallout_BrakeSysFeatures_HS2 [comipducallout_brakesysfeatures_hs2]

## 5.2.1.1 Design Rationale [design-rationale-2]

None

## 5.2.1.2 (Processing of function) [processing-of-function-1]

None

### 5.2.2 ComTimeoutNotification_Veh_V_ActlBrk [comtimeoutnotification_veh_v_actlbrk]

## 5.2.2.1 Design Rationale [design-rationale-3]

None

## 5.2.2.2 (Processing of function) [processing-of-function-2]

None

## Interrupt Functions

None

## Module Internal (Local) Functions

## Local Function \#1

| **Function Name**    | NtcEnab                          | Type    | Min   | Max  |
|----------|-----------------------------|----------------|---------|---------|
| **Arguments Passed** | FordMfgDiagcInhb_Cnt_T_u08       | Uint8   | 0U    | 1U   |
|                      | FordCanDtcInhb_Cnt_T_u08         | Uint8   | 0U    | 1U   |
|                      | FordAbsPrsnt_Cnt_T_u08           | Uint8   | 0U    | 1U   |
|                      | ClrDiagcFlgProxy_Cnt_T_u08       | Uint8   | 0U    | 1U   |
|                      | FordMissMsgDiagcInhb_Cnt_T_u08   | Uint8   | 0U    | 1U   |
|                      | FordTrlrBackupAssiEnad_Cnt_T_u08 | Uint8   | 0U    | 1U   |
|                      | FordInvldMsgDiagcInhb_Cnt_T_u08  | Uint8   | 0U    | 1U   |
|                      | \*MissMsgDiagEna_Cnt_T_logl      | Boolean | FALSE | TRUE |
|                      | \*InvldMsgDiagEna_Cnt_T_logl     | Boolean | FALSE | TRUE |
| **Return Value**     | None                             |         |       |      |

## Design Rationale

## Processing

Please refer to the below path in the FDD model.

MM077A_FordMsg415BusHiSpd/FordMsg415BusHiSpd/FordMsg415BusHiSpdPer1/NtcEnab

## Local Function \#2

| **Function Name**    | MissMsgFaild                                    | Type                     | Min   | Max     |
|----------|-----------------------------|----------------|---------|---------|
| **Arguments Passed** | MissMsgDiagEna_Cnt_T_logl                       | Boolean                  | FALSE | TRUE    |
|                      | BusHiSpdMissThd_Cnt_T_u16                       | Uint16                   | 0U    | 6000U   |
|                      | \*FordVehSpdBrkModlRawVal_Cnt_T_u16             | Uint16                   | 0U    | 65535U  |
|                      | \*FordVehSpdBrkModlVal_Kph_T_f32                | Float32                  | 0.0F  | 655.35F |
|                      | \*FordVehSpdQlyFacBrkModlVal_Cnt_T_enum         | Ford_VehVActlBrk_D_Qf1   | 0U    | 3U      |
|                      | \*FordVehSpdCntrBrkModlVal_Cnt_T_u08            | Uint8                    | 0U    | 15U     |
|                      | \*FordVehSpdChksBrkModlVal_Cnt_T_u08            | Uint8                    | 0U    | 255U    |
|                      | \*FordVehLoSpdMtnCtrlBrkSprtStsRawVal_Cnt_T_u08 | Uint8                    | 0U    | 8U      |
|                      | \*FordVehLoSpdMtnCtrlBrkSprtStsVal_Cnt_T_enum   | Ford_LsmcBrkDecel_D_Stat | 0U    | 7U      |
|                      | \*FordVehLoSpdMtnCtrlBrkSprtVldVal_Cnt_T_logl   | Boolean                  | FALSE | TRUE    |
|                      | \*FordVehSpdBrkModlLoQlyVldVal_Cnt_T_logl       | Boolean                  | FALSE | TRUE    |
|                      | \*FordVehSpdBrkModlVldVal_Cnt_T_logl            | Boolean                  | FALSE | TRUE    |
| **Return Value**     | None                                            |                          |       |         |

## Design Rationale

## Processing

Please refer to the below path in the FDD model.

MM077A_FordMsg415BusHiSpd/FordMsg415BusHiSpd/FordMsg415BusHiSpdPer1/MissMsgFaild

## Local Function \#3

| **Function Name**    | MissMsgPassd                                    | Type                     | Min   | Max     |
|---------|---------------------------------|----------------|-------|--------|
| **Arguments Passed** | MissMsgDiagEna_Cnt_T_logl                       | Boolean                  | FALSE | TRUE    |
|                      | Ford_Veh_V_ActlBrk_Cnt_T_u16                    | Uint16                   | 0U    | 65535U  |
|                      | Ford_VehVActlBrk_D_Qf1_Cnt_T_enum               | Ford_VehVActlBrk_D_Qf1   | 0U    | 3U      |
|                      | Ford_VehVActlBrk_No_Cnt_Cnt_T_u08               | Uint8                    | 0U    | 15U     |
|                      | Ford_VehVActlBrk_No_Cs_Cnt_T_u08                | Uint8                    | 0U    | 255U    |
|                      | InvldMsgDiagEna_Cnt_T_logl                      | Boolean                  | FALSE | TRUE    |
|                      | BusHiSpdQlyFacBrkModlInvldThd_Cnt_T_u16         | Uint16                   | 0U    | 6000U   |
|                      | BusHiSpdCntrBrkModlInvldThd_Cnt_T_u16           | Uint16                   | 0U    | 6000U   |
|                      | BusHiSpdChksBrkModlInvld_Cnt_T_u16              | Uint16                   | 0U    | 65535U  |
|                      | Ford_LsmcBrkDecel_D_Stat1_Cnt_T_enum            | Ford_LsmcBrkDecel_D_Stat | 0U    | 7U      |
|                      | \*FordVehSpdBrkModlRawVal_Cnt_T_u16             | Uint16                   | 0U    | 65535U  |
|                      | \*FordVehSpdBrkModlVal_Kph_T_f32                | Float32                  | 0.0F  | 655.35F |
|                      | \*FordVehSpdQlyFacBrkModlVal_Cnt_T_enum         | Ford_VehVActlBrk_D_Qf1   | 0U    | 3U      |
|                      | \*FordVehSpdCntrBrkModlVal_Cnt_T_u08            | Uint8                    | 0U    | 15U     |
|                      | \*FordVehSpdChksBrkModlVal_Cnt_T_u08            | Uint8                    | 0U    | 255U    |
|                      | \*FordVehLoSpdMtnCtrlBrkSprtStsRawVal_Cnt_T_u08 | Uint8                    | 0U    | 8U      |
|                      | \*FordVehLoSpdMtnCtrlBrkSprtStsVal_Cnt_T_enum   | Ford_LsmcBrkDecel_D_Stat | 0U    | 7U      |
|                      | \*FordVehLoSpdMtnCtrlBrkSprtVldVal_Cnt_T_logl   | Boolean                  | FALSE | TRUE    |
|                      | \*FordVehSpdBrkModlLoQlyVldVal_Cnt_T_logl       | Boolean                  | FALSE | TRUE    |
|                      | \*FordVehSpdBrkModlVldVal_Cnt_T_logl            | Boolean                  | FALSE | TRUE    |
| **Return Value**     | None                                            |                          |       |         |

## Design Rationale

## Processing

Please refer to the below path in the FDD model.

MM077A_FordMsg415BusHiSpd/FordMsg415BusHiSpd/FordMsg415BusHiSpdPer1/MissMsgPassd

## Local Function \#4

| **Function Name**    | SigProcg                                        | Type                     | Min   | Max     |
|---------|---------------------------------|----------------|-------|--------|
| **Arguments Passed** | Ford_Veh_V_ActlBrkValue_Cnt_T_u16               | Uint16                   | 0U    | 65535U  |
|                      | Ford_VehVActlBrk_D_Qf1Value_Cnt_T_enum          | Ford_VehVActlBrk_D_Qf1   | 0U    | 3U      |
|                      | Ford_VehVActlBrk_No_CntValue_Cnt_T_u08          | Uint8                    | 0U    | 15U     |
|                      | Ford_VehVActlBrk_No_CsValue_Cnt_T_u08           | Uint8                    | 0U    | 255U    |
|                      | Ford_LsmcBrkDecel_D_Stat1Value_Cnt_T_enum       | Ford_LsmcBrkDecel_D_Stat | 0U    | 7U      |
|                      | FordVehSpdBrkModlRawValue_Cnt_T_u16             | Uint16                   | 0U    | 65535U  |
|                      | FordVehSpdBrkModlValue_Kph_T_f32                | Float32                  | 0.0F  | 655.35F |
|                      | FordVehSpdQlyFacBrkModlValue_Cnt_T_enum         | Ford_VehVActlBrk_D_Qf1   | 0U    | 3U      |
|                      | FordVehSpdCntrBrkModlValue_Cnt_T_u08            | Uint8                    | 0U    | 15U     |
|                      | FordVehSpdChksBrkModlValue_Cnt_T_u08            | Uint8                    | 0U    | 255U    |
|                      | FordVehLoSpdMtnCtrlBrkSprtStsRawValue_Cnt_T_u08 | Uint8                    | 0U    | 8U      |
|                      | FordVehLoSpdMtnCtrlBrkSprtStsValue_Cnt_T_enum   | Ford_LsmcBrkDecel_D_Stat | 0U    | 7U      |
|                      | \*QlyFacBrkModlVldFlg_Cnt_T_logl                | Boolean                  | FALSE | TRUE    |
|                      | \*CntrBrkModlVldFlg_Cnt_T_logl                  | Boolean                  | FALSE | TRUE    |
|                      | \*ChksBrkModlVldFlg_Cnt_T_logl                  | Boolean                  | FALSE | TRUE    |
|                      | \*VldChkFlg_Cnt_T_logl                          | Boolean                  | FALSE | TRUE    |
| **Return Value**     | None                                            |                          |       |         |

## Design Rationale

## Processing

Please refer to the below path in the FDD model.

MM077A_FordMsg415BusHiSpd/FordMsg415BusHiSpd/FordMsg415BusHiSpdPer1/MissMsgPassd/OutpProcg/SigProcg

## Local Function \#5

| **Function Name**    | VldElpdTi                                | Type    | Min   | Max  |
|---------|---------------------------------|----------------|-------|--------|
| **Arguments Passed** | \* BrkModlVldPassdElpdTi_Cnt_T_logl      | Boolean | FALSE | TRUE |
|                      | \* BrkModlVldFaildElpdTi_Cnt_T_logl      | Boolean | FALSE | TRUE |
|                      | \* BrkModlLoQlyVldPassdElpdTi_Cnt_T_logl | Boolean | FALSE | TRUE |
|                      | \* BrkModlLoQlyVldFaildElpdTi_Cnt_T_logl | Boolean | FALSE | TRUE |
|                      | \* BrkSprtVldPassdElpdTi_Cnt_T_logl      | Boolean | FALSE | TRUE |
| **Return Value**     | None                                     |         |       |      |

## Design Rationale

## Processing

Please refer to the below path in the FDD model.

MM077A_FordMsg415BusHiSpd/FordMsg415BusHiSpd/FordMsg415BusHiSpdPer1/MissMsgPassd/OutpProcg/VldElpdTi

## Local Function \#6

| **Function Name**    | ChkElpdTi                                       | Type    | Min   | Max  |
|---------|---------------------------------|----------------|-------|--------|
| **Arguments Passed** | VldChkFlg_Cnt_T_logl                            | Boolean | FALSE | TRUE |
|                      | BrkModlVldPassdElpdTi_Cnt_T_logl                | Boolean | FALSE | TRUE |
|                      | BrkModlLoQlyVldPassdElpdTi_Cnt_T_logl           | Boolean | FALSE | TRUE |
|                      | BrkModlVldFaildElpdTi_Cnt_T_logl                | Boolean | FALSE | TRUE |
|                      | BrkModlLoQlyVldFaildElpdTi_Cnt_T_logl           | Boolean | FALSE | TRUE |
|                      | BrkSprtVldPassdElpdTi_Cnt_T_logl                | Boolean | FALSE | TRUE |
|                      | \*FordVehSpdBrkModlVldValue_Cnt_T_logl          | Boolean | FALSE | TRUE |
|                      | \*FordVehSpdBrkModlLoQlyVldValue_Cnt_T_logl     | Boolean | FALSE | TRUE |
|                      | \*FordVehLoSpdMtnCtrlBrkSprtVldValue_Cnt_T_logl | Boolean | FALSE | TRUE |
| **Return Value**     | None                                            |         |       |      |

## Design Rationale

## Processing

Please refer to the below path in the FDD model.

MM077A_FordMsg415BusHiSpd/FordMsg415BusHiSpd/FordMsg415BusHiSpdPer1/MissMsgPassd/OutpProcg/ChkElpdTi

## Local Function \#7

| **Function Name**    | Ntc0x166SetRst                               | Type    | Min   | Max   |
|---------|---------------------------------|----------------|-------|--------|
| **Arguments Passed** | QlyFacBrkModlVldFlg_Cnt_T_logl               | Boolean | FALSE | TRUE  |
|                      | BusHiSpdQlyFacBrkModlInvldThdValue_Cnt_T_u16 | Uint16  | 0U    | 6000U |
| **Return Value**     | None                                         |         |       |       |

## Design Rationale

## Processing

Please refer to the below path in the FDD model.

MM077A_FordMsg415BusHiSpd/FordMsg415BusHiSpd/FordMsg415BusHiSpdPer1/MissMsgPassd/InvldNtcPass/Ntc0x166_Set_Reset

## Local Function \#8

| **Function Name**    | Ntc0x167SetRst                             | Type    | Min   | Max   |
|---------|---------------------------------|----------------|-------|--------|
| **Arguments Passed** | CntrBrkModlVldFlg_Cnt_T_logl               | Boolean | FALSE | TRUE  |
|                      | BusHiSpdCntrBrkModlInvldThdValue_Cnt_T_u16 | Uint16  | 0U    | 6000U |
| **Return Value**     | None                                       |         |       |       |

## Design Rationale

## Processing

Please refer to the below path in the FDD model.

MM077A_FordMsg415BusHiSpd/FordMsg415BusHiSpd/FordMsg415BusHiSpdPer1/MissMsgPassd/InvldNtcPass/Ntc0x167_Set_Reset

## Local Function \#9

| **Function Name**    | Ntc0x168SetRst                          | Type    | Min   | Max    |
|---------|---------------------------------|----------------|-------|--------|
| **Arguments Passed** | ChksBrkModlVldFlg_Cnt_T_logl            | Boolean | FALSE | TRUE   |
|                      | BusHiSpdChksBrkModlInvldValue_Cnt_T_u16 | Uint16  | 0U    | 65535U |
| **Return Value**     | None                                    |         |       |        |

## Design Rationale

## Processing

Please refer to the below path in the FDD model.

MM077A_FordMsg415BusHiSpd/FordMsg415BusHiSpd/FordMsg415BusHiSpdPer1/MissMsgPassd/InvldNtcPass/Ntc0x168_Set_Reset

## GLOBAL Function/Macro Definitions

None

# Known Limitations with Design

1.  In model, ClrDiagcFlgProxyPrev(boolean) is compared with
    ClrDiagcFlgProxy(uint8 signal) which is logically wrong. So, change
    the data type of ClrDiagcFlgProxyPrev to uint8. Please refer MM065A
    Data dictionary for the same.

2.  The range of the input signal Ford_Veh_V_ActlBrk is 0 to 65535. We
    are
    (MM077A_FordMsg415BusHiSpd_SIL/FordMsg415BusHiSpd/FordMsg415BusHiSpdPer1/MissMsgPassd/OutpProcg/SigProcg/CalcVehSpdChksBrkModlCnvn)
    rightshifting the value of the input signal with RISHIFT_CNT_U16 and
    Masking the value of the input signal with EIGHTBITMASK_CNT_U16.
    Then we add the ouptuts of the each operation. If the output value
    of the rightshift operation and bitmasking operation is greater than
    range of UINT8, then overflow occurs.

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
| 5           | FDD: MM077A_FordMsg415BusHiSpd_Design                                                                                                                                 | See Synergy sub project version |

{% endraw %}