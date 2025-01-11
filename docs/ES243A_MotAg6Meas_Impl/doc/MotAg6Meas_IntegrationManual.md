---
layout: default
title: MotAg6Meas_IntegrationManual
nav_order: 1
parent: Component Implementation
---
{% raw %}
**Integration Manual**

**For**

**MotAg6Meas**

**VERSION: 1.0**

**DATE: 31-JUL-2017**

**Prepared By:**

**Shruthi Raghavan,**

**Nexteer Automotive,**

**Saginaw, MI, USA**

**Location:** The official version of this document is stored in the
Nexteer Configuration Management System.

**Revision History**

|            |                 |                  |             |             |
|------------|-----------------|------------------|-------------|-------------|
| **Sl.No.** | **Description** | **Author**       | **Version** | **Date**    |
| 1          | Initial version | Shruthi Raghavan | 1.0         | 31-Jul-2017 |

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
7](#__RefHeading___Toc489206174)

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

|            |                                      |                                       |
|-------|-------------------------------------------------|-----------------|
| **Sl.No.** | **Title**                            | **Version**                           |
| 1          | EA4 Software Naming Conventions      | 01.01.00                              |
| 2          | EA4 Common Naming Conventions        | 01.01.00                              |
| 3          | Software Design and Coding Standards | 2.1                                   |
| 4          | ES243A_MotAg6Meas_Design             | See Synergy design Subproject Version |

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

> MotAg6MeasPer2

# Configuration REQUIREMeNTS

## Build Time Config

|             |           |     |
|-------------|-----------|-----|
| **Modules** | **Notes** |     |
| **None**    |           |     |

## Configuration Files to be provided by Integration Project

> None

## Da Vinci Parameter Configuration Changes

<table>
<colgroup>
<col style="width: 38%" />
<col style="width: 44%" />
<col style="width: 17%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Parameter</strong></td>
<td><strong>Notes</strong></td>
<td><strong>SWC</strong></td>
</tr>
<tr class="even">
<td><p>/Nexteer/MotAg6Meas/</p>
<p>MotAg6MeasGeneral/MotAg6PrtclFlt</p></td>
<td>NTC Number for Protocol Fault in MotAg6Meas component. Range is
NTCNR_0X083 to NTCNR_0X08A</td>
<td><p>ES243A</p>
<p>MotAg6Meas</p></td>
</tr>
</tbody>
</table>

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

Refer FDD DataDict.m file

## Required Global Data Outputs

Refer FDD DataDict.m file

## Specific Include Path present

Yes

# Runnable Scheduling 

This section specifies the required runnable scheduling.

|                     |                             |             |
|---------------------|-----------------------------|-------------|
| **Init**            | **Scheduling Requirements** | **Trigger** |
| **MotAg6MeasInit1** | None                        | RTE (Init)  |

|                      |                             |               |
|----------------------|-----------------------------|---------------|
| **Runnable**         | **Scheduling Requirements** | **Trigger**   |
| **MotAg6MeasPer1**   | None                        | RTE (2ms)     |
| **MotAg6MeasPer3**   | None                        | RTE (4ms)     |
| **MotAg6MeasPer2**   | None                        | ISR(MotCtrl)  |
| **MotAg6EolPrmRead** | None                        | On invocation |
| **MotAg6EolPrmWr**   | None                        | On invocation |

# Memory Map REQUIREMENTS

## Mapping

|                                   |                                                    |           |
|-----------------------------|------------------------------------|-------|
| **Memory Section**                | **Contents**                                       | **Notes** |
| **MotCtrl_START_SEC_CODE**        | Code section for Motor Control scheduled functions |           |
| **CDD_MotAg6Meas_START_SEC_CODE** |                                                    |           |

> \* Each …START_SEC… constant is terminated by a …STOP_SEC… constant as
> specified in the AUTOSAR Memory Mapping requirements.

## Usage

|             |         |         |
|-------------|---------|---------|
| **Feature** | **RAM** | **ROM** |
| **None**    |         |         |

Table 1: ARM Cortex R4 Memory Usage

## NvM Blocks

**MotAg6EolPrm**

**MotAg6StVari**

\*See DataDict.m for details

# Compiler Settings

##  Preprocessor MACRO

None

## Optimization Settings

None

# Appendix

None

{% endraw %}