---
layout: default
title: GtmCfgAndUse Integration Manual
nav_order: 1
parent: Component Implementation
---
{% raw %}
**Integration Manual**

**For**

**GtmCfgAndUse**

**VERSION: 1.0**

**DATE: 09-14-2017**

**Prepared By:**

**Avinash James,**

**Nexteer Automotive,**

**Saginaw, MI, USA**

**Location:** The official version of this document is stored in the
Nexteer Configuration Management System.

**Revision History**

|             |                 |               |             |             |
|-------------|-----------------|---------------|-------------|-------------|
| **Sl. No.** | **Description** | **Author**    | **Version** | **Date**    |
| 1           | Initial version | Avinash James | 1.0         | 14-Sep-2017 |

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
7](#__RefHeading___Toc495057626)

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

|                  |                                         |
|------------------|-----------------------------------------|
| **Abbreviation** | **Description**                         |
| DFD              | Design functional diagram               |
| MDD              | Module design Document                  |
|                  | \<ADD more to the table if applicable\> |
|                  |                                         |
|                  |                                         |

# References

|             |                             |                                       |
|----------|----------------------------------------------|-----------------|
| **Sr. No.** | **Title**                   | **Version**                           |
| 1           | MDD Guidelines              | Software Engineering Process 04.04.02 |
| 2           | Software Naming Conventions | Software Engineering Process 04.04.02 |
| 3           | Coding standards            | Software Engineering Process 04.04.02 |
| \<4         | FDD                         | See Synergy Sub projection version    |
|             | \<Add if more available\>   |                                       |

# Dependencies

## SWCs

|                |                                         |
|----------------|-----------------------------------------|
| **Module**     | **Required Feature**                    |
| **ElecGlbPrm** | Global macro defined in the header file |

Note : Referencing the external components should be avoided in most
cases. Only in unavoidable circumstance external components should be
referred. Developer should track the references.

## Global Functions(Non RTE) to be provided to Integration Project

GtmCfgAndUsePer1 – Called from the Motor control ISR

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
|               |           |         |

## DaVinci Interrupt Configuration Changes

|              |            |                         |           |
|--------------|------------|-------------------------|-----------|
| **ISR Name** | **VIM \#** | **Priority Dependency** | **Notes** |
|              |            |                         |           |

## Manual Configuration Changes

|     |           |         |
|-----|-----------|---------|
|     | **Notes** | **SWC** |
|     |           |         |

# Integration DATAFLOW REQUIREMENTS

## Required Global Data Inputs

> See DataDict.m file

## Required Global Data Outputs

> See DataDict.m file

## Specific Include Path present

Yes

# Runnable Scheduling 

This section specifies the required runnable scheduling.

|                       |                             |             |
|-----------------------|-----------------------------|-------------|
| **Init**              | **Scheduling Requirements** | **Trigger** |
| **GtmCfgAndUseInit1** | None                        | RTE Init    |

|                          |                             |                    |
|----------------------------|----------------------------|----------------|
| **Runnable**             | **Scheduling Requirements** | **Trigger**        |
| **GtmCfgAndUsePer1**     | None                        | Motor Control Rate |
| **GtmCfgAndUsePer2**     | None                        | 2 ms               |
| **GtmGetSent0Data_Oper** | None                        | On Invocation      |
| **GtmGetSent1Data_Oper** | None                        | On Invocation      |

# Memory Map REQUIREMENTS

## Mapping

|                                             |              |           |
|---------------------------------------------|--------------|-----------|
| **Memory Section**                          | **Contents** | **Notes** |
| **GtmCfgAndUse_START_SEC_CODE**             |              |           |
| **CDD_GtmCfgAndUse_MotCtrl_START_SEC_CODE** |              |           |

\* Each …START_SEC… constant is terminated by a …STOP_SEC… constant as
specified in the AUTOSAR Memory Mapping requirements.

## Usage

|             |         |         |
|-------------|---------|---------|
| **Feature** | **RAM** | **ROM** |
|             |         |         |

Table 1: ARM Cortex R4 Memory Usage

## NvM Blocks

None

# Compiler Settings

##  Preprocessor MACRO

> None

## Optimization Settings

> None

# Appendix

*None*

{% endraw %}