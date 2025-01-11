---
layout: default
title: HwTq8Meas_IntegrationManual
nav_order: 1
parent: Component Implementation
---
{% raw %}
**Integration Manual**

**For**

**HwTq8Meas**

**VERSION: 1.0**

**DATE: 11-Jul-2017**

**Prepared By:**

**Software Group,**

**Nexteer Automotive,**

**Saginaw, MI, USA**

**Location:** The official version of this document is stored in the
Nexteer Configuration Management System.

**Revision History**

|             |                 |              |             |             |
|-------------|-----------------|--------------|-------------|-------------|
| **Sl. No.** | **Description** | **Author**   | **Version** | **Date**    |
| 1           | Initial version | Krishna Anne | 1.0         | 11-Jul-2017 |

Table of Contents

[1 Abbrevations And Acronyms 5](#abbrevations-and-acronyms)

[2 References 6](#references)

[3 Dependencies 7](#dependencies)

[3.1 SWCs 7](#swcs)

[3.2 Global Functions(Non RTE) to be provided to Integration Project
7](#global-functionsnon-rte-to-be-provided-to-integration-project)

[4 Configuration REQUIREMeNTS 8](#configuration-requirements)

[4.1 Build Time Config 8](#build-time-config)

[4.2 Configuration Files to be provided by Integration Project
8](#configuration-files-to-be-provided-by-integration-project)

[4.3 Da Vinci Parameter Configuration Changes
8](#da-vinci-parameter-configuration-changes)

[4.4 DaVinci Interrupt Configuration Changes
8](#davinci-interrupt-configuration-changes)

[4.5 Manual Configuration Changes 8](#manual-configuration-changes)

[5 Integration DATAFLOW REQUIREMENTS
9](#integration-dataflow-requirements)

[5.1 Required Global Data Inputs 9](#required-global-data-inputs)

[5.2 Required Global Data Outputs 9](#required-global-data-outputs)

[5.3 Specific Include Path present 9](#specific-include-path-present)

[6 Runnable Scheduling 10](#runnable-scheduling)

[7 Memory Map REQUIREMENTS 11](#memory-map-requirements)

[7.1 Mapping 11](#mapping)

[7.2 Usage 11](#usage)

[7.3 NvM Blocks 11](#nvm-blocks)

[8 Compiler Settings 12](#compiler-settings)

[8.1 Preprocessor MACRO 12](#preprocessor-macro)

[8.2 Optimization Settings 12](#optimization-settings)

[9 Appendix 13](#appendix)

# Abbrevations And Acronyms

|                  |                            |
|------------------|----------------------------|
| **Abbreviation** | **Description**            |
| DFD              | Design functional diagram  |
| MDD              | Module design Document     |
| FDD              | Functional Design Document |
|                  |                            |
|                  |                            |

# References

This section lists the title & version of all the documents that are
referred for development of this document

|             |                             |                                |
|-------------|-----------------------------|--------------------------------|
| **Sr. No.** | **Title**                   | **Version**                    |
| 1           | FDD – CM650A HwTq8Meas      | See Synergy subproject version |
| 2           | Software Naming Conventions | Process 04.02.00               |
| 3           | Software Coding Standards   | Process 04.02.00               |

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

None

# Configuration REQUIREMeNTS

## Build Time Config

|               |                                                      |     |
|---------------|------------------------------------------------------|-----|
| **Modules**   | **Notes**                                            |     |
| **FLTINJENA** | Set to STD_ON if want to turn on the fault injection |     |

## Configuration Files to be provided by Integration Project

CDD_HwTq8Meas_Cfg.h

*Note: Temporarily this file can be copied from the contract folder.
Later revision will have the Davinci configuration parameter to generate
the file.*

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

Refer DataDict.m file

## Required Global Data Outputs

Refer DataDict.m file

## Specific Include Path present

Yes

# Runnable Scheduling 

This section specifies the required runnable scheduling.

|                    |                             |                |
|--------------------|-----------------------------|----------------|
| **Init**           | **Scheduling Requirements** | **Trigger**    |
| **HwTq8MeasInit1** | **None**                    | **RTE (Init)** |

|                            |                             |                  |
|----------------------------|------------------------------|---------------|
| **Runnable**               | **Scheduling Requirements** | **Trigger**      |
| **HwTq8MeasPer1**          | **None**                    | **RTE (2 ms)**   |
| **HwTq8MeasPer2**          | **None**                    | **RTE (100 ms)** |
| **HwTq8AutTrim_Oper**      | **None**                    | **On event**     |
| **HwTq8ClrTrim_Oper**      | **None**                    | **On event**     |
| **HwTq8ReadTrim_Oper**     | **None**                    | **On event**     |
| **HwTq8TrimPrfmdSts_Oper** | **None**                    | **On event**     |
| **HwTq8WrTrim_Oper**       | **None**                    | **On event**     |
| **HwTq8MeasTrigStrt_Oper** | **None**                    | **On event**     |

# Memory Map REQUIREMENTS

## Mapping

|                    |              |           |
|--------------------|--------------|-----------|
| **Memory Section** | **Contents** | **Notes** |
| **None**           |              |           |
|                    |              |           |

\* Each …START_SEC… constant is terminated by a …STOP_SEC… constant as
specified in the AUTOSAR Memory Mapping requirements.

## Usage

|             |         |         |
|-------------|---------|---------|
| **Feature** | **RAM** | **ROM** |
| **None**    |         |         |

Table 1: ARM Cortex R4 Memory Usage

## NvM Blocks

\*See DataDict.m

# Compiler Settings

##  Preprocessor MACRO

None

## Optimization Settings

None

# Appendix

*Port Configuration SENT0SPCO output:*

*Port (that’s needs to be configured as SENT0SPCO) should be initialized
as input DIO with level high.*

*The client call IoHwAb_SetFctPrphlHwTq8_Oper will reset the pin to
output alternate mode for SENT0SPCO.*

{% endraw %}