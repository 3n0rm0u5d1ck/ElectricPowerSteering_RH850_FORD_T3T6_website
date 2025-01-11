---
layout: default
title: FordMsg2FDBusHiSpd_MDD
nav_order: 2
parent: Component Implementation
---
{% raw %}
**Module Design Document**

**For**

**FordMsg2FDBusHiSpd**

**24-Apr-2018**

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
| Initial Version | Mrudula Paturi | 1       | 24-Apr-2018 |

**  
**

**<u>Table of Contents</u>**

[1 Introduction [5](#introduction)](#introduction)

[MDD for FordMsg2FDBusHiSpd
[5](#mdd-for-fordmsg2fdbushispd)](#mdd-for-fordmsg2fdbushispd)

[2 FordMsg2FDBusHiSpd & High-Level Description
[6](#fordmsg2fdbushispd-high-level-description)](#fordmsg2fdbushispd-high-level-description)

[3 Design details of software module
[7](#design-details-of-software-module)](#design-details-of-software-module)

[3.1 Graphical representation of FordMsg2FDBusHiSpd
[7](#graphical-representation-of-fordmsg2fdbushispd)](#graphical-representation-of-fordmsg2fdbushispd)

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

[5.1.1 Init: FordMsg2FDBusHiSpdInit1
[9](#init-fordmsg2fdbushispdinit1)](#init-fordmsg2fdbushispdinit1)

[5.1.2 Per: FordMsg2FDBusHiSpdPer1
[9](#per-fordmsg2fdbushispdper1)](#per-fordmsg2fdbushispdper1)

[5.2 Server Runnables [9](#server-runnables)](#server-runnables)

[5.2.1 ComIPduCallout_Mc_Send_Signlas_2_FD1
[9](#comipducallout_mc_send_signlas_2_fd1)](#comipducallout_mc_send_signlas_2_fd1)

[5.2.2 ComTimeoutNotification_EsaOn_B_Rq
[9](#comtimeoutnotification_esaon_b_rq)](#comtimeoutnotification_esaon_b_rq)

[5.3 Interrupt Functions
[10](#interrupt-functions)](#interrupt-functions)

[5.4 Module Internal (Local) Functions
[10](#module-internal-local-functions)](#module-internal-local-functions)

[5.4.1 DiagEna [10](#_Toc510547745)](#_Toc510547745)

[5.4.1.1 Design Rationale
[10](#design-rationale-4)](#design-rationale-4)

[5.4.1.2 Processing [10](#processing)](#processing)

[5.4.2 MsgMiss [10](#_Toc510547748)](#_Toc510547748)

[5.4.2.1 Design Rationale
[11](#design-rationale-5)](#design-rationale-5)

[5.4.2.2 Processing [11](#processing-1)](#processing-1)

[5.4.3 Enabled [11](#_Toc499562923)](#_Toc499562923)

[5.4.3.1 Design Rationale
[11](#design-rationale-6)](#design-rationale-6)

[5.4.3.2 Processing [11](#processing-2)](#processing-2)

[5.4.4 MsgPrsnt [11](#_Toc510547754)](#_Toc510547754)

[5.4.4.1 Design Rationale
[12](#design-rationale-7)](#design-rationale-7)

[5.4.4.2 Processing [12](#_Toc499562928)](#_Toc499562928)

[5.5 GLOBAL Function/Macro Definitions
[13](#_Toc510547760)](#_Toc510547760)

[6 Known Limitations with Design
[14](#known-limitations-with-design)](#known-limitations-with-design)

[7 UNIT TEST CONSIDERATION
[15](#unit-test-consideration)](#unit-test-consideration)

[Appendix A Abbreviations and Acronyms
[16](#_Toc510547763)](#_Toc510547763)

[Appendix B Glossary [17](#glossary)](#glossary)

[Appendix C References [18](#references)](#references)

# Introduction

##  MDD for FordMsg2FDBusHiSpd [mdd-for-fordmsg2fdbushispd]

# FordMsg2FDBusHiSpd & High-Level Description

Please refer FDD.

# Design details of software module

## Graphical representation of FordMsg2FDBusHiSpd

<img
src="ElectricPowerSteering_RH850_FORD_T3T6_website/docs/MM134A_FordMsg2FDBusHiSpd_Impl/doc/mediax/media/image1.png"
style="width:6.9in;height:3.47014in" />

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

### 5.1.1 Init: FordMsg2FDBusHiSpdInit1 [init-fordmsg2fdbushispdinit1]

#### Design Rationale

None

#### Module Outputs

None

### 5.1.2 Per: FordMsg2FDBusHiSpdPer1 [per-fordmsg2fdbushispdper1]

#### 5.1.2.1 Design Rationale [design-rationale-1]

None

#### 5.1.2.2 Store Module Inputs to Local copies [store-module-inputs-to-local-copies]

None

#### 5.1.2.3 Processing of function [processing-of-function]

None

#### 5.1.2.4 Store Local copy of outputs into Module Outputs [store-local-copy-of-outputs-into-module-outputs]

None

## Server Runnables 

### 5.2.1 ComIPduCallout_Mc_Send_Signlas_2_FD1 [comipducallout_mc_send_signlas_2_fd1]

#### 5.2.1.1 Design Rationale [design-rationale-2]

None

#### 5.2.1.2 (Processing of function) [processing-of-function-1]

None

### 5.2.2 ComTimeoutNotification_EsaOn_B_Rq [comtimeoutnotification_esaon_b_rq]

#### 5.2.2.1 Design Rationale [design-rationale-3]

None

#### 5.2.2.2 (Processing of function) [processing-of-function-2]

None

## Interrupt Functions

None

## Module Internal (Local) Functions

## DiagEna

| **Function Name** | DiagEna                          | Type    | Min | Max |
|-------------------|----------------------------------|---------|-----|-----|
| Arguments Passed  | FordEvasSteerAssiEnad_Cnt_T_logl | boolean | 0U  | 1U  |
|                   | FordCanDtcInhb_Cnt_T_logl        | boolean | 0U  | 1U  |
| Return Value      |                                  | boolean |     |     |

#### 5.4.1.1 Design Rationale [design-rationale-4]

Refer FDD

#### 5.4.1.2 Processing [processing]

Refer FDD

## MsgMiss

<table>
<colgroup>
<col style="width: 12%" />
<col style="width: 40%" />
<col style="width: 24%" />
<col style="width: 10%" />
<col style="width: 11%" />
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
<td>FordEpsLifeCycMod_Cnt_T_u08</td>
<td>Uint8</td>
<td>0U</td>
<td>1U</td>
</tr>
<tr class="even">
<td>DiagEna_Cnt_T_logl</td>
<td>boolean</td>
<td>0U</td>
<td>1U</td>
</tr>
<tr class="odd">
<td>ClrDiagcFlgProxy_Cnt_T_u08</td>
<td>Uint8</td>
<td>0U</td>
<td>1U</td>
</tr>
<tr class="even">
<td>Return Value</td>
<td></td>
<td><p>Boolean</p>
<p>Uint8</p></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

#### 5.4.2.1 Design Rationale [design-rationale-5]

Refer FDD

#### 5.4.2.2 Processing [processing-1]

<span id="_Toc499562923" class="anchor"></span>Refer FDD

## Enabled

| **Function Name** | Enabled                     | Type  | Min | Max |
|-------------------|-----------------------------|-------|-----|-----|
| Arguments Passed  | FordEpsLifeCycMod_Cnt_T_u08 | Uint8 | 0U  | 1U  |
| Return Value      | None                        |       |     |     |

#### 5.4.3.1 Design Rationale [design-rationale-6]

Refer FDD

#### 5.4.3.2 Processing [processing-2]

Refer FDD

## MsgPrsnt

<table>
<colgroup>
<col style="width: 12%" />
<col style="width: 47%" />
<col style="width: 22%" />
<col style="width: 8%" />
<col style="width: 9%" />
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
<td rowspan="3">Arguments Passed</td>
<td>DiagEna_Cnt_T_logl</td>
<td>boolean</td>
<td>0U</td>
<td>1U</td>
</tr>
<tr class="even">
<td>ClrDiagcFlgProxy_Cnt_T_u08</td>
<td>Uint8</td>
<td>0U</td>
<td>1U</td>
</tr>
<tr class="odd">
<td>Ford_EsaOn_B_Rq_Cnt_T_enum</td>
<td>Ford_EsaOn_B_Rq</td>
<td>0U</td>
<td>1U</td>
</tr>
<tr class="even">
<td>Return Value</td>
<td></td>
<td><p>Boolean</p>
<p>Uint8</p></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

#### 5.4.4.1 Design Rationale [design-rationale-7]

<span id="_Toc499562928" class="anchor"></span>Refer FDD

#### 5.4.4.2 Processing [processing-3]

<span id="_Toc510547760" class="anchor"></span>Refer FDD

## GLOBAL Function/Macro Definitions

None

# Known Limitations with Design

The output signal FordVehEvasSteerAssiReq is of type enum in DataDict.m
file but it is clarified to be uint8 as per the Architecture team. Same
with the associated PIM FordVehEvasSteerAssiReqPrev which is clarified
to be uint8.

# UNIT TEST CONSIDERATION

<span id="_Toc510547763" class="anchor"></span>The output signal
FordVehEvasSteerAssiReq is of type enum in DataDict.m file but it is
clarified to be uint8 as per the Architecture team. Same with the
associated PIM FordVehEvasSteerAssiReqPrev which is clarified to be
uint8.

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
| 5       | FDD: MM134A\_ FordMsg2FDBusHiSpd \_Design                                    | See Synergy subproject version |

{% endraw %}