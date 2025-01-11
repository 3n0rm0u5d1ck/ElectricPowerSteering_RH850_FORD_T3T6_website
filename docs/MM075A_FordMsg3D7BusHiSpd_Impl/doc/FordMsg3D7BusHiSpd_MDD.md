---
layout: default
title: FordMsg3D7BusHiSpd_MDD
nav_order: 2
parent: Component Implementation
---
{% raw %}
**Module Design Document**

**For**

**FordMsg3D7BusHiSpd**

**19-Apr-2018**

**Prepared For:**

**Software Engineering**

**Nexteer Automotive,**

**Saginaw, MI, USA**

**Prepared By:**

**Software Group,**

**Nexteer Automotive,**

**Saginaw, MI, USA  
<u>Change History</u>**

|                 |                |         |             |
|-----------------|----------------|---------|-------------|
| Description     | Author         | Version | Date        |
| Initial Version | Mrudula Paturi | 1       | 19-Apr-2018 |

**  
**

**<u>Table of Contents</u>**

[1 Introduction [5](#introduction)](#introduction)

[MDD for FordMsg3D7BusHiSpd
[5](#mdd-for-fordmsg3d7bushispd)](#mdd-for-fordmsg3d7bushispd)

[2 FordMsg3D7BusHiSpd & High-Level Description
[6](#fordmsg3d7bushispd-high-level-description)](#fordmsg3d7bushispd-high-level-description)

[3 Design details of software module
[7](#design-details-of-software-module)](#design-details-of-software-module)

[3.1 Graphical representation of FordMsg3D7BusHiSpd
[7](#graphical-representation-of-fordmsg3d7bushispd)](#graphical-representation-of-fordmsg3d7bushispd)

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

[5.1.1 Init: FordMsg3D7BusHiSpdInit1
[9](#init-fordmsg3d7bushispdinit1)](#init-fordmsg3d7bushispdinit1)

[5.1.2 Per: FordMsg3D7BusHiSpdPer1
[9](#per-fordmsg3d7bushispdper1)](#per-fordmsg3d7bushispdper1)

[5.2 Server Runnables [9](#server-runnables)](#server-runnables)

[5.2.1 ComIPduCallout_Steer_Assist_Data_FD1
[9](#comipducallout_steer_assist_data_fd1)](#comipducallout_steer_assist_data_fd1)

[5.2.2 ComTimeoutNotification_EsaOn_B_Rq
[9](#comtimeoutnotification_esaenbl_d2_rq)](#comtimeoutnotification_esaenbl_d2_rq)

[5.3 Interrupt Functions
[10](#interrupt-functions)](#interrupt-functions)

[5.4 Module Internal (Local) Functions
[10](#module-internal-local-functions)](#module-internal-local-functions)

[5.4.1 NtcEnab [10](#_Toc510547745)](#_Toc510547745)

[5.4.1.1 Design Rationale
[10](#design-rationale-4)](#design-rationale-4)

[5.4.1.2 Processing [10](#processing)](#processing)

[5.4.2 MsgMiss [10](#_Toc510547748)](#_Toc510547748)

[5.4.2.1 Design Rationale
[11](#design-rationale-5)](#design-rationale-5)

[5.4.2.2 Processing [11](#processing-1)](#processing-1)

[5.4.3 OutpProcd [11](#_Toc510547751)](#_Toc510547751)

[5.4.3.1 Design Rationale
[11](#design-rationale-6)](#design-rationale-6)

[5.4.3.2 Processing [11](#processing-2)](#processing-2)

[5.4.4 VldElpdTi [11](#_Toc510547754)](#_Toc510547754)

[5.4.4.1 Design Rationale
[11](#design-rationale-7)](#design-rationale-7)

[5.4.4.2 Processing [11](#processing-3)](#processing-3)

[5.4.5 FirstTran [12](#_Toc510547757)](#_Toc510547757)

[5.4.5.1 Design Rationale
[12](#design-rationale-8)](#design-rationale-8)

[5.4.5.2 Processing [12](#processing-4)](#processing-4)

[5.4.6 ChkElpdTi [12](#_Toc510547757)](#_Toc510547757)

[5.4.6.1 Design Rationale
[12](#design-rationale-8)](#design-rationale-8)

[5.4.6.2 Processing [12](#processing-4)](#processing-4)

[5.4.7 Enabled [12](#_Toc510547757)](#_Toc510547757)

[5.4.7.1 Design Rationale
[12](#design-rationale-8)](#design-rationale-8)

[5.4.7.2 Processing [12](#processing-4)](#processing-4)

[5.4.8 EnabledTwo [12](#_Toc510547757)](#_Toc510547757)

[5.4.8.1 Design Rationale
[12](#design-rationale-8)](#design-rationale-8)

[5.4.8.2 Processing [12](#processing-4)](#processing-4)

[5.5 GLOBAL Function/Macro Definitions [12](#chkelpdti)](#chkelpdti)

[6 Known Limitations with Design
[13](#known-limitations-with-design)](#known-limitations-with-design)

[7 UNIT TEST CONSIDERATION
[14](#unit-test-consideration)](#unit-test-consideration)

[Appendix A Abbreviations and Acronyms
[15](#_Toc510547763)](#_Toc510547763)

[Appendix B Glossary [16](#glossary)](#glossary)

[Appendix C References [17](#references)](#references)

# Introduction

##  MDD for FordMsg3D7BusHiSpd [mdd-for-fordmsg3d7bushispd]

# FordMsg3D7BusHiSpd & High-Level Description

Please refer FDD.

# Design details of software module

## Graphical representation of FordMsg3D7BusHiSpd

<img
src="ElectricPowerSteering_RH850_FORD_T3T6_website/docs/MM075A_FordMsg3D7BusHiSpd_Impl/doc/mediax/media/image1.png"
style="width:6.9in;height:6.65347in" />

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

### 5.1.1 Init: FordMsg3D7BusHiSpdInit1 [init-fordmsg3d7bushispdinit1]

#### Design Rationale

None

#### Module Outputs

None

### 5.1.2 Per: FordMsg3D7BusHiSpdPer1 [per-fordmsg3d7bushispdper1]

#### 5.1.2.1 Design Rationale [design-rationale-1]

None

#### 5.1.2.2 Store Module Inputs to Local copies [store-module-inputs-to-local-copies]

None

#### 5.1.2.3 Processing of function [processing-of-function]

None

#### 5.1.2.4 Store Local copy of outputs into Module Outputs [store-local-copy-of-outputs-into-module-outputs]

None

## Server Runnables 

### 5.2.1 ComIPduCallout_Steer_Assist_Data_FD1 [comipducallout_steer_assist_data_fd1]

#### 5.2.1.1 Design Rationale [design-rationale-2]

None

#### 5.2.1.2 (Processing of function) [processing-of-function-1]

None

### 5.2.2 ComTimeoutNotification_EsaEnbl_D2_Rq [comtimeoutnotification_esaenbl_d2_rq]

#### 5.2.2.1 Design Rationale [design-rationale-3]

None

#### 5.2.2.2 (Processing of function) [processing-of-function-2]

None

## Interrupt Functions

None

## Module Internal (Local) Functions

### NtcEnab

| **Function Name** | NtcEnab                          | Type    | Min | Max |
|-------------------|----------------------------------|---------|-----|-----|
| Arguments Passed  | FordEvasSteerAssiEnad_Cnt_T_logl | boolean | 0U  | 1U  |
|                   | FordCanDtcInhb_Cnt_T_logl        | boolean | 0U  | 1U  |
|                   | ClrDiagcFlgProxy_Cnt_T_u08       | uint8   | 0U  | 1U  |
| Return Value      |                                  | boolean |     |     |

#### Design Rationale

Refer FDD

#### Processing

Refer FDD

### MsgMiss

<table>
<colgroup>
<col style="width: 12%" />
<col style="width: 56%" />
<col style="width: 14%" />
<col style="width: 7%" />
<col style="width: 9%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Function Name</strong></th>
<th>MsgMiss</th>
<th>Type</th>
<th>Min</th>
<th>Max</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td rowspan="3">Arguments Passed</td>
<td>DiagEna_Cnt_T_logl</td>
<td>boolean</td>
<td>0U</td>
<td>1U</td>
</tr>
<tr class="even">
<td>BusHiSpdMissThd_Cnt_T_u16</td>
<td>Uint16</td>
<td>0U</td>
<td>6000U</td>
</tr>
<tr class="odd">
<td>ClrDiagcFlgProxyEna_Cnt_T_logl</td>
<td>boolean</td>
<td>0U</td>
<td>1U</td>
</tr>
<tr class="even">
<td>Return Value</td>
<td></td>
<td><p>Boolean</p>
<p>Uint8</p>
<p>Uint16</p></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

#### Design Rationale

Refer FDD

#### Processing

Refer FDD

### OutpProcd

<table>
<colgroup>
<col style="width: 12%" />
<col style="width: 56%" />
<col style="width: 15%" />
<col style="width: 6%" />
<col style="width: 8%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Function Name</strong></th>
<th>MsgPrsnt</th>
<th>Type</th>
<th>Min</th>
<th>Max</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td rowspan="8">Arguments Passed</td>
<td>Ford_EsaEnbl_D2_Rq_Cnt_T_enum</td>
<td>enum</td>
<td>0U</td>
<td>3U</td>
</tr>
<tr class="even">
<td>Ford_CmbbObjClass_D_Stat_Cnt_T_enum</td>
<td>enum</td>
<td>0U</td>
<td>15U</td>
</tr>
<tr class="odd">
<td>Ford_CmbbObjConfdnc_D_Stat_Cnt_T_enum</td>
<td>enum</td>
<td>0U</td>
<td>3U</td>
</tr>
<tr class="even">
<td>Ford_CmbbObjDistLong_L_Actl_Cnt_T_u16</td>
<td>Uint16</td>
<td>0U</td>
<td>1023U</td>
</tr>
<tr class="odd">
<td>Ford_CmbbObjDistLat_L_Actl_Cnt_T_u16</td>
<td>Uint16</td>
<td>0U</td>
<td>511U</td>
</tr>
<tr class="even">
<td>Ford_CmbbObjRelLong_V_Actl_Cnt_T_u16</td>
<td>Uint16</td>
<td>0U</td>
<td>1023U</td>
</tr>
<tr class="odd">
<td>Ford_CmbbObjRelLat_V_Actl_Cnt_T_u16</td>
<td>Uint16</td>
<td>0U</td>
<td>511U</td>
</tr>
<tr class="even">
<td>Ford_CmbbObjColl_T_Actl_Cnt_T_u08</td>
<td>Uint8</td>
<td>0U</td>
<td>127U</td>
</tr>
<tr class="odd">
<td>Return Value</td>
<td></td>
<td><p>Boolean</p>
<p>Uint8</p>
<p>Uint16</p></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

#### Design Rationale

Refer FDD

#### Processing

Refer FDD

### VldElpdTi

| **Function Name** | VldElpdTi          | Type    | Min | Max |
|-------------------|--------------------|---------|-----|-----|
| Arguments Passed  | No input arguments |         |     |     |
| Return Value      |                    | Boolean |     |     |

#### Design Rationale

Refer FDD

#### Processing

Refer FDD

### FirstTran

| **Function Name** | FirstTran            | Type    | Min | Max |
|-------------------|----------------------|---------|-----|-----|
| Arguments Passed  | VldChkFlg_Cnt_T_logl | boolean | 0U  | 1U  |
| Return Value      |                      | boolean |     |     |

#### Design Rationale

Refer FDD

#### Processing

Refer FDD

### ChkElpdTi

| **Function Name** | ChkElpdTi                                         | Type    | Min | Max |
|----------|------------------------------------|--------------|-------|-------|
| Arguments Passed  | VldChkFlg_Cnt_T_logl                              | boolean | 0U  | 1U  |
|                   | ImgProcrModlAVldPassdElpdTi_Cnt_T_logl            | boolean | 0U  | 1U  |
|                   | FordVehCllsnMtgtnByBrkgLgtDstRawInp_Cnt_T_logl    | boolean | 0U  | 1U  |
|                   | LgtDstRawVldFaildElpdTi_Cnt_T_logl                | boolean | 0U  | 1U  |
|                   | FordVehCllsnMtgtnByBrkgLatDstRawInp_Cnt_T_logl    | boolean | 0U  | 1U  |
|                   | LatDstRawVldFaildElpdTi_Cnt_T_logl                | boolean | 0U  | 1U  |
|                   | FordVehCllsnMtgtnByBrkgRelLgtVelRawInp_Cnt_T_logl | boolean | 0U  | 1U  |
|                   | RelLgtVelRawVldFaildElpdTi_Cnt_T_logl             | boolean | 0U  | 1U  |
|                   | FordVehCllsnMtgtnByBrkgRelLatVelRawInp_Cnt_T_logl | boolean | 0U  | 1U  |
|                   | RelLatVelRawVldFaildElpdTi_Cnt_T_logl             | boolean | 0U  | 1U  |
|                   | FordVehCllsnMtgtnByBrkgTiToCllsnRawInp_Cnt_T_logl | boolean | 0U  | 1U  |
|                   | TiToCllsnRawVldFaildElpdTi_Cnt_T_logl             | boolean | 0U  | 1U  |
| Return Value      |                                                   | boolean |     |     |

#### Design Rationale

Refer FDD

#### Processing

Refer FDD

### Enad

| **Function Name** | Enabled                                        | Type    | Min | Max   |
|----------|----------------------------------|---------------|-------|--------|
| Arguments Passed  | FordVehCllsnMtgtnByBrkgLgtDstRawInp_Cnt_T_logl | boolean | 0U  | 1U    |
|                   | BusHiSpdLgtDstInvldThd_Cnt_T_u16               | Uint16  | 0U  | 6000U |
|                   | BusHiSpdLatDstInvldThd_Cnt_T_u16               | Uint16  | 0U  | 6000U |
|                   | FordVehCllsnMtgtnByBrkgLatDstRawInp_Cnt_T_logl | boolean | 0U  | 1U    |
| Return Value      | None                                           |         |     |       |

#### Design Rationale

Refer FDD

#### Processing

Refer FDD

### Enad2

| **Function Name** | ElpdTi                                            | Type    | Min | Max   |
|----------|------------------------------------|--------------|-------|-------|
| Arguments Passed  | FordVehCllsnMtgtnByBrkgRelLgtVelRawInp_Cnt_T_logl | boolean | 0U  | 1U    |
|                   | FordVehCllsnMtgtnByBrkgRelLatVelRawInp_Cnt_T_logl | boolean | 0U  | 1U    |
|                   | FordVehCllsnMtgtnByBrkgTiToCllsnRawInp_Cnt_T_logl | boolean | 0U  | 1U    |
|                   | BusHiSpdRelLgtVelInvldThd_Cnt_T_u16               | Uint16  | 0U  | 6000U |
|                   | BusHiSpdRelLatVelInvldThd_Cnt_T_u16               | Uint16  | 0U  | 6000U |
|                   | BusHiSpdTiToCllsnInvldThd_Cnt_T_u16               | boolean | 0U  | 1U    |
| Return Value      | None                                              |         |     |       |

#### Design Rationale

Refer FDD

#### Processing

Refer FDD

## GLOBAL Function/Macro Definitions

None

# Known Limitations with Design

1.  The datatypes of the following outputs and PIMs have been changed to
    uint8 as per clarification by the Architect.

> FordVehCllsnMtgtnByBrkgObjDataConfLvlRaw_Cnt_T_u08
>
> FordVehCllsnMtgtnByBrkgObjTypClassnRaw_Cnt_T_u08
>
> FordVehEvasSteerAssiEnadReqRaw_Cnt_T_u08
>
> Rte_Pim_FordVehCllsnMtgtnByBrkgObjDataConfLvlRawPrev
>
> Rte_Pim_FordVehCllsnMtgtnByBrkgObjTypClassnRawPrev
>
> Rte_Pim_FordVehEvasSteerAssiEnadReqRawPrev
>
> 2\) FORDVEHCLLSNMTGTNBYBRKGTITOCLLSNRAWTHD_CNT_U16 is of type uint8
> but wrongly named as U16. This was changed in the code to
> FORDVEHCLLSNMTGTNBYBRKGTITOCLLSNRAWTHD_CNT_U08.

# UNIT TEST CONSIDERATION

1.  <span id="_Toc510547763" class="anchor"></span>The datatypes of the
    following outputs and PIMs have been changed to uint8 from enum as
    per clarification by the Architect.

> FordVehCllsnMtgtnByBrkgObjDataConfLvlRaw_Cnt_T_u08
>
> FordVehCllsnMtgtnByBrkgObjTypClassnRaw_Cnt_T_u08
>
> FordVehEvasSteerAssiEnadReqRaw_Cnt_T_u08
>
> Rte_Pim_FordVehCllsnMtgtnByBrkgObjDataConfLvlRawPrev
>
> Rte_Pim_FordVehCllsnMtgtnByBrkgObjTypClassnRawPrev
>
> Rte_Pim_FordVehEvasSteerAssiEnadReqRawPrev

1.  FORDVEHCLLSNMTGTNBYBRKGTITOCLLSNRAWTHD_CNT_U16 is of type uint8 but
    wrongly named as U16. This was changed in the code to
    FORDVEHCLLSNMTGTNBYBRKGTITOCLLSNRAWTHD_CNT_U08.

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

| Ref. \# | Title                                                                        | Version                        |
|-------|----------------------------------------|-------------------------|
| 1       | AUTOSAR Specification of Memory Mapping (Link:AUTOSAR_SWS_MemoryMapping.pdf) | v1.3.0 R4.0 Rev 2              |
| 2       | MDD Guideline                                                                | EA4 01.00                      |
| 3       | Software Naming Conventions.doc                                              | EA4 01.02                      |
| 4       | Software Design and Coding Standards.doc                                     | EA4 2.01                       |
| 5       | FDD: MM075A_FordMsg3D7BusHiSpd_Design                                        | See Synergy subproject version |

{% endraw %}