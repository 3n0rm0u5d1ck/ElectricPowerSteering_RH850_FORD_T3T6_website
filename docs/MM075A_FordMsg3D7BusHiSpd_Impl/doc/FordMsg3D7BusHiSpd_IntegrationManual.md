---
layout: default
title: FordMsg3D7BusHiSpd_IntegrationManual
nav_order: 1
parent: Component Implementation
---
{% raw %}
**Integration Manual**

**For**

**FordMsg3D7BusHiSpd**

**VERSION: 1.0**

**DATE: 24-Apr-2018**

**Prepared By:**

**Software Group,**

**Nexteer Automotive,**

**Saginaw, MI, USA**

**Location:** The official version of this document is stored in the
Nexteer Configuration Management System.

**Revision History**

|             |                 |            |             |             |
|-------------|-----------------|------------|-------------|-------------|
| **Sl. No.** | **Description** | **Author** | **Version** | **Date**    |
| 1           | Initial version | MP         | 1.0         | 24-Apr-2018 |

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
7](#__RefHeading___Toc510535448)

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
|                  |                           |
|                  |                           |

# References

This section lists the title & version of all the documents that are
referred for development of this document

|             |                                       |                                 |
|----------|----------------------------------------------|-----------------|
| **Sr. No.** | **Title**                             | **Version**                     |
| 1           | FDD: MM075A_FordMsg3D7BusHiSpd_Design | See Synergy Sub Project Version |
| 2           | Software Naming Conventions           | 1.02                            |
| 3           | Software Design and Coding Standards  | 2.01                            |

# Dependencies

## SWCs

|            |                      |
|------------|----------------------|
| **Module** | **Required Feature** |
| **None**   |                      |

Note : Referencing the external components should be avoided in most
cases. Only in unavoidable circumstance external components should be
referred. Developer should track the references.

## Global Functions(Non RTE) to be provided to Integration Project

ComIPduCallout_Steer_Assist_Data_FD1

ComTimeoutNotification_EsaEnbl_D2_Rq

# Configuration REQUIREMeNTS

## Build Time Config

|             |           |     |
|-------------|-----------|-----|
| **Modules** | **Notes** |     |
| **None**    |           |     |

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

# Integration DATAFLOW REQUIREMENTS

## Required Global Data Inputs

Refer DataDict.m file in the FDD

## Required Global Data Outputs

Refer DataDict.m file in the FDD

## Specific Include Path present

No

# Runnable Scheduling 

This section specifies the required runnable scheduling.

|                             |                             |             |
|-----------------------------|-----------------------------|-------------|
| **Init**                    | **Scheduling Requirements** | **Trigger** |
| **FordMsg3D7BusHiSpdInit1** | None                        | RTE (Init)  |

|                            |                             |             |
|----------------------------|-----------------------------|-------------|
| **Runnable**               | **Scheduling Requirements** | **Trigger** |
| **FordMsg3D7BusHiSpdPer1** | None                        | RTE (10 ms) |

|                                          |                             |                                                                 |
|----------------------------|------------------|---------------------------|
| **Srv Runnable**                         | **Scheduling Requirements** | **Trigger**                                                     |
| **ComIPduCallout_Steer_Assist_Data_FD1** | None                        | On invocation of ComIPduCallout_Steer_Assist_Data_FD1 (NON-RTE) |

<table>
<colgroup>
<col style="width: 39%" />
<col style="width: 21%" />
<col style="width: 38%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Srv Runnable</strong></td>
<td><strong>Scheduling Requirements</strong></td>
<td><strong>Trigger</strong></td>
</tr>
<tr class="even">
<td><strong>ComTimeoutNotification_EsaEnbl_D2_Rq</strong></td>
<td>None</td>
<td><p>On invocation of</p>
<p>ComTimeoutNotification_EsaEnbl_D2_Rq (NON-RTE)</p></td>
</tr>
</tbody>
</table>

# Memory Map REQUIREMENTS

## Mapping

|                                       |              |           |
|---------------------------------------|--------------|-----------|
| **Memory Section**                    | **Contents** | **Notes** |
| **None**                              |              |           |
| **FordMsg3D7BusHiSpd_START_SEC_CODE** |              |           |

\* Each …START_SEC… constant is terminated by a …STOP_SEC… constant as
specified in the AUTOSAR Memory Mapping requirements.

## Usage

|             |         |         |
|-------------|---------|---------|
| **Feature** | **RAM** | **ROM** |
| **None**    |         |         |

Table 1: ARM Cortex R4 Memory Usage

## NvM Blocks

**None**

# Compiler Settings

##  Preprocessor MACRO

None.

## Optimization Settings

None.

# Appendix

None.

{% endraw %}