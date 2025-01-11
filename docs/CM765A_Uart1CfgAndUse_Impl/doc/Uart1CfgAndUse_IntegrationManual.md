---
layout: default
title: Uart1CfgAndUse_IntegrationManual
nav_order: 1
parent: Component Implementation
---
{% raw %}
**Integration Manual**

**For**

**Uart1CfgAndUse**

**VERSION: 1.0**

**DATE: 15-June-2017**

**Prepared By:**

**Software Group,**

**Nexteer Automotive,**

**Saginaw, MI, USA**

**Location:** The official version of this document is stored in the
Nexteer Configuration Management System.

**Revision History**

|             |                 |                  |             |              |
|-------------|-----------------|------------------|-------------|--------------|
| **Sl. No.** | **Description** | **Author**       | **Version** | **Date**     |
| 1           | Initial version | Krzysztof Byrski | 1.0         | 15-June-2017 |

Table of Contents

[1 Abbrevations And Acronyms 4](#abbrevations-and-acronyms)

[2 References 5](#references)

[3 Dependencies 6](#dependencies)

[3.1 SWCs 6](#swcs)

[3.2 Global Functions(Non RTE) to be provided to Integration Project
6](#global-functionsnon-rte-to-be-provided-to-integration-project)

[4 Configuration REQUIREMeNTS 7](#configuration-requirements)

[4.1 Build Time Config 7](#build-time-config)

[4.2 Configuration Files to be provided by Integration Project
7](#configuration-files-to-be-provided-by-integration-project)

[4.3 Da Vinci Parameter Configuration Changes
7](#da-vinci-parameter-configuration-changes)

[4.4 DaVinci Interrupt Configuration Changes
7](#__RefHeading___Toc484677598)

[4.5 Manual Configuration Changes 7](#manual-configuration-changes)

[5 Integration DATAFLOW REQUIREMENTS
8](#integration-dataflow-requirements)

[5.1 Required Global Data Inputs 8](#required-global-data-inputs)

[5.2 Required Global Data Outputs 8](#required-global-data-outputs)

[5.3 Specific Include Path present 8](#specific-include-path-present)

[6 Runnable Scheduling 9](#runnable-scheduling)

[7 Memory Map REQUIREMENTS 10](#memory-map-requirements)

[7.1 Mapping 10](#mapping)

[7.2 Usage 10](#usage)

[7.3 NvM Blocks 10](#nvm-blocks)

[8 Compiler Settings 11](#compiler-settings)

[8.1 Preprocessor MACRO 11](#preprocessor-macro)

[8.2 Optimization Settings 11](#optimization-settings)

[9 Appendix 12](#appendix)

# Abbrevations And Acronyms

|                  |                           |
|------------------|---------------------------|
| **Abbreviation** | **Description**           |
| DFD              | Design functional diagram |
| MDD              | Module design Document    |

# References

This section lists the title & version of all the documents that are
referred for development of this document

|             |                                      |                                 |
|----------|----------------------------------------------|-----------------|
| **Sr. No.** | **Title**                            | **Version**                     |
| 1           | EA4 Software Naming Conventions      | 01.01.00                        |
| 2           | Software Design and Coding Standards | 2.1                             |
| 3           | CM765A_Uart1CfgAndUse_Design         | See Synergy Sub Project Version |

# Dependencies

## SWCs

|                    |                                      |
|--------------------|--------------------------------------|
| **Module**         | **Required Feature**                 |
| **AR350A ImcArbn** | All the IMC signal group definitions |

Note : Referencing the external components should be avoided in most
cases. Only in unavoidable circumstance external components should be
referred. Developer should track the references.

## Global Functions(Non RTE) to be provided to Integration Project

Uart1CfgAndUseInin - To be defined as a trusted function as the DTS
Channel master registers need to be configured in the supervisor mode.

# Configuration REQUIREMeNTS

## Build Time Config

|                                              |                      |     |
|----------------------------------------------|----------------------|-----|
| **Modules**                                  | **Notes**            |     |
| **IMCARBN_NROF2MILLISECRATEGROUP_CNT_U08**   | Takes unsigned value |     |
| **IMCARBN_NROF10MILLISECRATEGROUP_CNT_U08**  | Takes unsigned value |     |
| **IMCARBN_NROF100MILLISECRATEGROUP_CNT_U08** | Takes unsigned value |     |

## Configuration Files to be provided by Integration Project

None

## Da Vinci Parameter Configuration Changes

|               |           |         |
|---------------|-----------|---------|
| **Parameter** | **Notes** | **SWC** |
| **None**      |           |         |

## DaVinci Interrupt Configuration Changes

|              |            |                         |           |
|--------------|------------|-------------------------|-----------|
| **ISR Name** | **VIM \#** | **Priority Dependency** | **Notes** |
| **None**     |            |                         |           |

## Manual Configuration Changes

|              |           |         |
|--------------|-----------|---------|
| **Constant** | **Notes** | **SWC** |
| **None**     |           |         |

## EXCLUSIVE AREAS

<table>
<colgroup>
<col style="width: 39%" />
<col style="width: 47%" />
<col style="width: 12%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Exclusive Area</strong></td>
<td><strong>Notes</strong></td>
<td><strong>SWC</strong></td>
</tr>
<tr class="even">
<td><strong>ExclsvAr1Uart1DrvrTxRxBuf</strong></td>
<td><p>Exclusive area needs to protect access to Transmit and Receive
buffers from asynchronous updates by server runnables and periodic
updates by tasks.</p>
<p>Integrator needs to verify if client calls to server runnables can
interrupt periodics and set up exclusive area to properly protect
access. If exclusive area is needed, at minimum it must disable OS Task
scheduling (It is assumed that all clients call occurs in OS
Tasks).</p></td>
<td></td>
</tr>
</tbody>
</table>

# Integration DATAFLOW REQUIREMENTS

## Required Global Data Inputs

None

## Required Global Data Outputs

None

## Specific Include Path present

Yes

# Runnable Scheduling 

This section specifies the required runnable scheduling.

|                         |                             |             |
|-------------------------|-----------------------------|-------------|
| **Init**                | **Scheduling Requirements** | **Trigger** |
| **Uart1CfgAndUseInit1** | None                        | RTE(Init)   |

|                        |                             |             |
|------------------------|-----------------------------|-------------|
| **Runnable**           | **Scheduling Requirements** | **Trigger** |
| **Uart1CfgAndUsePer1** | None                        | RTE(2ms)    |
| **Uart1CfgAndUsePer2** | None                        | RTE(2ms)    |
| **Uart1CfgAndUsePer3** | None                        | RTE(10ms)   |
| **Uart1CfgAndUsePer4** | None                        | RTE(100ms)  |

**.**

# Memory Map REQUIREMENTS

## Mapping

|                                                        |              |           |
|-----------------------------------------|----------------|----------------|
| **Memory Section**                                     | **Contents** | **Notes** |
| **CDD_Uart1CfgAndUse_START_SEC_CODE**                  | Functions    |           |
| **CDD_Uart1CfgAndUse_START_SEC_VAR_INIT_128**          | Tx Buffer    |           |
| **CDD_Uart1CfgAndUse_DmaWrite_START_SEC_VAR_INIT_128** | Rx Buffer    |           |

\* Each …START_SEC… constant is terminated by a …STOP_SEC… constant as
specified in the AUTOSAR Memory Mapping requirements.

## Usage

|             |         |         |
|-------------|---------|---------|
| **Feature** | **RAM** | **ROM** |
| **None**    |         |         |

Table 1: ARM Cortex R4 Memory Usage

## NvM Blocks

None

# Compiler Settings

##  Preprocessor MACRO

None

## Optimization Settings

None

# Appendix

Header file “CDD_Uart1CfgAndUse.h” shall be included inside
Rte_UserTypes.h which will provide typedef Ary1D_u8_2048_Uart1CfgAndUse.

{% endraw %}