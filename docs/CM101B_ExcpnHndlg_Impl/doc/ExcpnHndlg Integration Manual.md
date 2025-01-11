---
layout: default
title: ExcpnHndlg Integration Manual
nav_order: 1
parent: Component Implementation
---
{% raw %}
**Integration Manual**

**For**

**ExcpnHndlg**

**VERSION: 1**

**DATE: 12/11/17**

**Prepared By:**

**Software Group,**

**Nexteer Automotive,**

**Saginaw, MI, USA**

**Location:** The official version of this document is stored in the
Nexteer Configuration Management System.

**Revision History**

|            |                 |               |             |          |
|------------|-----------------|---------------|-------------|----------|
| **Sl.No.** | **Description** | **Author**    | **Version** | **Date** |
| 1          | Initial version | Avinash James | 1.0         | 12/11/17 |
|            |                 |               |             |          |

Table of Contents

[1 Abbrevations And Acronyms 4](#abbrevations-and-acronyms)

[2 References 5](#references)

[3 Dependencies 6](#dependencies)

[3.1 SWCs 6](#swcs)

[3.2 Global Functions(Non RTE) to be provided to Integration Project
6](#global-functionsnon-rte-to-be-provided-to-integration-project)

[4 Configuration REQUIREMeNTS 8](#configuration-requirements)

[4.1 Build Time Config 8](#build-time-config)

[4.2 Configuration Files to be provided by Integration Project
8](#configuration-files-to-be-provided-by-integration-project)

[4.3 Da Vinci Parameter Configuration Changes
8](#da-vinci-parameter-configuration-changes)

[4.4 DaVinci Interrupt Configuration Changes
8](#__RefHeading___Toc500849256)

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

|                  |                 |
|------------------|-----------------|
| **Abbreviation** | **Description** |
|                  |                 |
|                  |                 |
|                  |                 |

# References

This section lists the title & version of all the documents that are
referred for development of this document

|             |                                      |                                       |
|---------|---------------------------|------------------------------------|
| **Sr. No.** | **Title**                            | **Version**                           |
| 1           | FDD : CM101B\_ ExcpnHndlg_Design     | See Synergy sub project version       |
| 2           | EA4 Software Naming Conventions      | Software Engineering Process 04.04.02 |
| 3           | Software Design and Coding Standards | Software Engineering Process 04.04.02 |

# Dependencies

## SWCs

|            |                      |
|------------|----------------------|
| **Module** | **Required Feature** |
|            |                      |

Note : Referencing the external components should be avoided in most
cases. Only in unavoidable circumstance external components should be
referred. Developer should track the references.

## Global Functions(Non RTE) to be provided to Integration Project

**SetMcuDiagcIdnData** – Non-Rte Server Interface (called as needed)

**GetMcuDiagcIdnData** – Non-Rte Server Interface (called as needed)

**SysErrIrq/Patched_SysErrIrq** – Interrupt Handler Routine (triggered
by Interrupt)

**FpuErrIrq/Patched_FpuErrIrq** – Interrupt Handler Routine (triggered
by Interrupt)

**AlgnErrIrq** – Interrupt Handler Routine (triggered by Interrupt)

**ResdOperIrq** – Interrupt Handler Routine (triggered by Interrupt)

**ExcpnHndlgInit1** – Non-RTE initialization function (called during
startup before RTE is initialized)

**FeNmiPegErr** – Callout function for interrupt response handling (to
be called by FENMI Interrupt handler)

**FeNmiDmaTrfErr** – Callout function for interrupt response handling
(to be called by FENMI Interrupt handler)

**FeNmiEcmMstChkrErr**– Callout function for interrupt response handling
(to be called by FENMI Interrupt handler)

**FeNmiWdgErr**– Callout function for interrupt response handling (to be
called by FENMI Interrupt handler)

**ProcUkwnExcpnErr** – Callout function for OS error response handling
(to be called by OS error handler)

**ProcMpuExcpnErr** – Callout function for OS error response handling
(to be called by OS error handler)

**ProcPrvlgdInstrExcpnErr** – Callout function for OS error response
handling (to be called by OS error handler)

**ProcPrmntOsErr** – Callout function for OS error response handling (to
be called by OS error handler)

**ProcNonCritOsErr** – Callout function for OS error response handling
(to be called by OS error handler)

**ChkForStrtUpTest_Oper** – (called as needed from both RTE and non-RTE
context))

**FeNmiClkMonr0RtLowrLimFlt** – Callout function responding to Clock
Monitor 0 Runtime Lower Limit Failure(to be called by FENMI Interrupt
handler)

**FeNmiClkMonr0RtErr** – Callout function responding to Clock Monitor 0
Runtime Failure (to be called by FENMI Interrupt handler)

**FeNmiClkMonr1RtErr** – Callout function responding to Clock Monitor 1
Runtime Failure (to be called by FENMI Interrupt handler)

**FeNmiClkMonr2RtErr** – Callout function responding to Clock Monitor 2
Runtime Failure (to be called by FENMI Interrupt handler)

**FeNmiClkMonr3RtErr** – Callout function responding to Clock Monitor 3
Runtime Failure (to be called by FENMI Interrupt handler)

**FeNmiClkMonr5RtErr** – Callout function responding to Clock Monitor 5
Runtime Failure (to be called by FENMI Interrupt handler)

**FeNmiModErrDbgActv** – Callout function responding to Debug mode
active failure (to be called by FENMI Interrupt handler)

**FeNmiModErrProgmModActv** – Callout function responding to Programming
mode active failure (to be called by FENMI Interrupt handler)

**FeNmiModErrUsrModInactv** – Callout function responding to user mode
being inactive failure (to be called by FENMI Interrupt handler)

**FeNmiModErrTestModActv** – Callout function responding to Test mode
active failure (to be called by FENMI Interrupt handler)

**FeNmiBusBrdgErr** – Callout function responding to Bus Bridge error
(to be called by FENMI Interrupt handler)

**FeNmiBusSngBitEccErr** – Callout function Single bit ECC error on the
data bus (to be called by FENMI Interrupt handler)

**FeNmiCodFlsEccAdrOvfErr** – Callout function code flash ecc address
overflow error (to be called by FENMI Interrupt handler)

**FeNmiCodFlsIllglAcsBySysBus** – Callout function responding to illegal
access of code flash by the system bus (to be called by FENMI Interrupt
handler)

**FeNmiDmaIllglAcsErr** – Callout function responding to illegal access
by the DMA (to be called by FENMI Interrupt handler)

**FeNmiDmaLockStepErrOrGblRamWrBufErr** – Callout function responding to
Dma lock step error or Global RAM write buffer error (to be called by
FENMI Interrupt handler)

**FeNmiDtsRamDblBitEccErr** – Callout function responding to Dts Ram ECC
double bit failure (to be called by FENMI Interrupt handler)

**FeNmiFlsSeqErr** – Callout function responding to flash sequencer
failure (to be called by FENMI Interrupt handler)

**FeNmiGblRamIllglAcsByProcr** – Callout function responding to illegal
access of global RAM by processor (to be called by FENMI Interrupt
handler)

**FeNmiGblRamIllglAcsBySysBus** – Callout function responding to global
RAM illegal access by system bus (to be called by FENMI Interrupt
handler)

**FeNmiPrphlRamEccAdrOvfErr** – Callout function responding to
peripheral RAM ECC address overflow error (to be called by FENMI
Interrupt handler)

**FeNmiGlbRamEccAdrOvfErr** – Callout function responding to global ram
ecc address overflow error (to be called by FENMI Interrupt handler)

**FeNmiGtmRamDblBitEccErr** – Callout function responding to GTM RAM ecc
double bit error (to be called by FENMI Interrupt handler)

**FeNmiLclRamEccAdrOvfErr** – Callout function responding to local RAM
ecc address overflow error (to be called by FENMI Interrupt handler)

**FeNmiProcrLockStepErr** – Callout function responding to processor
lockstep error (to be called by FENMI Interrupt handler)

**FeNmiResdAreaIllglAcsByHiSpdBus** – Callout function responding to
Reserved area illegal access by High Speed bus (to be called by FENMI
Interrupt handler)

**Note:- The configuration for the Non RTE server runnables for the
FENMI handler is done in the MCU component as per the error source
configuration list available in CM104B Design.**

**The OS errors are configured in the OS component. OS document shall
explain the configuration of the OS related errors**

# Configuration REQUIREMeNTS

## Build Time Config

|             |           |     |
|-------------|-----------|-----|
| **Modules** | **Notes** |     |
|             |           |     |

## Configuration Files to be provided by Integration Project

N/A

## Da Vinci Parameter Configuration Changes

<table>
<colgroup>
<col style="width: 34%" />
<col style="width: 49%" />
<col style="width: 15%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Parameter</strong></td>
<td><strong>Notes</strong></td>
<td><strong>SWC</strong></td>
</tr>
<tr class="even">
<td><strong>/Nexteer/ExcpnHndlg/<br />
ExcpnHndlgCfg/WdgMCfgStr</strong></td>
<td><p>WdgMConfig structure name. For OS Gen 7 or later, set this to
WdgMConfig_Mode0_Core&lt;n&gt;</p>
<p>Otherwise Set it to WdgMConfig_Mode0<br />
Name to be given by integrator based on the definition in WdgM_PBcfg.h
file from Vector</p></td>
<td>ExcpnHndlg</td>
</tr>
</tbody>
</table>

## DaVinci Interrupt Configuration Changes

|                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------|------------------------------------------------|
| **ISR Name**          | **Notes**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| **Patched_SysErrIrq** | The ExcpnHndlg module implements an interrupt that needs a patch for a hardware problem that exists on the P1M hardware (see Renesas Technical Update TN-RH8-S001A/E). Nexteer has created the appropriate workaround that subsequently calls the normal interrupt handler code. Therefore, when configuring the SysErrIrq interrupt in the O/S the interrupt handler name should be configured to the Nexteer code with the workaround (“Patched_SysErrIrq”) instead of directly referencing the normal interrupt handler code. |
| **Patched_FpuErrIrq** | The ExcpnHndlg module implements an interrupt that needs a patch for a hardware problem that exists on the P1M hardware (see Renesas Technical Update TN-RH8-S001A/E). Nexteer has created the appropriate workaround that subsequently calls the normal interrupt handler code. Therefore, when configuring the FpuErrIrq interrupt in the O/S the interrupt handler name should be configured to the Nexteer code with the workaround (“Patched_FpuErrIrq”) instead of directly referencing the normal interrupt handler code. |

## Manual Configuration Changes

|              |           |         |
|--------------|-----------|---------|
| **Constant** | **Notes** | **SWC** |
| **None**     |           |         |

# Integration DATAFLOW REQUIREMENTS

## Required Global Data Inputs

Refer FDD

## Required Global Data Outputs

Refer FDD

## Specific Include Path present

Yes

# Runnable Scheduling 

> API usage and scheduling of BSW components expected to be captured at
> a project architectural level and is beyond the scope of this
> document. Third party documentation can be referenced as needed.

|                         |                                                             |                    |
|------------------|----------------------------------------|---------------|
| **Init**                | **Scheduling Requirements**                                 | **Trigger**        |
| **ExcpnHndlgInit1**     | Pre-RTE initializaton                                       | Once at init       |
| **ExcpnHndlgInit2**     | After diagnostic manager is initialized and NTCs can be set | RTE initialization |
| **ChkForStrtUpTest**    | None                                                        | On invocation      |
| **GetMcuDiagcSpplData** | None                                                        | On invocation      |

|                    |                             |             |
|--------------------|-----------------------------|-------------|
| **Runnable**       | **Scheduling Requirements** | **Trigger** |
| **ExcpnHndlgPer1** |                             | 2ms         |

**.**

# Memory Map REQUIREMENTS

## Mapping

|                                           |                           |                                                                                                         |
|----------------------------------|--------------------|-------------------|
| **Memory Section**                        | **Contents**              | **Notes**                                                                                               |
| **GlobalShared_START_SEC_VAR_CLEARED_16** | ExcpnHndlgOsErrCod_C      | Used for memory mapping the variable to global shared                                                   |
| **BackUpRam_START_SEC_VAR_CLEARED_32**    | 1KB of back up RAM memory | Need the array of 1KB of uint32 to be mapped to this section( address range 0xFEBF_FC00 to 0xFEBF_FFFF) |

> \* Each …START_SEC… constant is terminated by a …STOP_SEC… constant as
> specified in the AUTOSAR Memory Mapping requirements.

## Usage

|             |         |         |
|-------------|---------|---------|
| **Feature** | **RAM** | **ROM** |
| **None**    |         |         |

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