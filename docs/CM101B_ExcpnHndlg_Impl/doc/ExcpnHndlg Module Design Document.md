---
layout: default
title: ExcpnHndlg Module Design Document
nav_order: 2
parent: Component Implementation
---
{% raw %}
**Module Design Document**

**For**

**ExcpnHndlg**

**Mar 11, 2018**

**Prepared By:**

**Software Group,**

**Nexteer Automotive,**

**Saginaw, MI, USA  
<u>Change History</u>**

|                         |               |             |             |
|-------------------------|---------------|-------------|-------------|
| **Description**         | **Author**    | **Version** | **Date**    |
| Initial Version         | Avinash James | 1.0         | 11-Dec-2017 |
| Updated local constants | Avinash James | 2.0         | 11-Mar-2018 |

**  
**

<u>Table of Contents</u>

[1 Introduction [4](#introduction)](#introduction)

[1.1.1 Purpose [4](#purpose)](#purpose)

[2 ExcpnHndlg & High-Level Description
[5](#excpnhndlg-high-level-description)](#excpnhndlg-high-level-description)

[3 Design details of software module
[6](#design-details-of-software-module)](#design-details-of-software-module)

[3.1.1 Graphical representation of ExcpnHndlg
[6](#graphical-representation-of-excpnhndlg)](#graphical-representation-of-excpnhndlg)

[3.1.2 Data Flow Diagram [6](#data-flow-diagram)](#data-flow-diagram)

[3.1.3 Component level DFD
[6](#component-level-dfd)](#component-level-dfd)

[3.1.4 Function level DFD [6](#function-level-dfd)](#function-level-dfd)

[4 Constant Data Dictionary
[7](#constant-data-dictionary)](#constant-data-dictionary)

[4.1.1 Program (fixed) Constants
[7](#program-fixed-constants)](#program-fixed-constants)

[4.1.2 Embedded Constants [7](#embedded-constants)](#embedded-constants)

[5 Software Component Implementation
[11](#software-component-implementation)](#software-component-implementation)

[5.1.1 Sub-Module Functions
[11](#sub-module-functions)](#sub-module-functions)

[5.1.2 Per: ExcpnHndlgPer1
[11](#per-excpnhndlgper1)](#per-excpnhndlgper1)

[5.1.3 Server Runables [11](#server-runables)](#server-runables)

[5.1.4 Interrupt Functions
[17](#interrupt-functions)](#interrupt-functions)

[5.1.5 Module Internal (Local) Functions
[17](#module-internal-local-functions)](#module-internal-local-functions)

[5.1.6 GLOBAL Function/Macro Definitions
[18](#global-functionmacro-definitions)](#global-functionmacro-definitions)

[5.1.7 GLOBAL Function \#1 [18](#global-function-1)](#global-function-1)

[5.1.8 Design Rationale
[18](#design-rationale-46)](#design-rationale-46)

[5.1.9 processing [18](#processing-1)](#processing-1)

[6 Known Limitations with Design
[19](#known-limitations-with-design)](#known-limitations-with-design)

[7 UNIT TEST CONSIDERATION
[20](#unit-test-consideration)](#unit-test-consideration)

[Appendix A Abbreviations and Acronyms
[21](#abbreviations-and-acronyms)](#abbreviations-and-acronyms)

[Appendix B Glossary [22](#glossary)](#glossary)

[Appendix C References [23](#references)](#references)

# Introduction

## Purpose

This document details the design in the FDD and also lists out any
deviations which were made from the design for the implementation due to
any constraints in development. ExcpnHndlg MDD describes the exception
handling / reset cause determination for microcontroller diagnostics

# ExcpnHndlg & High-Level Description

Refer FDD

# Design details of software module

## Graphical representation of ExcpnHndlg

## Data Flow Diagram

<img
src="ElectricPowerSteering_RH850_FORD_T3T6_website/docs/CM101B_ExcpnHndlg_Impl/doc/mediax/media/image1.png"
style="width:2.91667in;height:1.83333in" />

### Component level DFD

**N/A**

### Function level DFD

**N/A**

# Constant Data Dictionary

## Program (fixed) Constants

### Embedded Constants

#### Local Constants

| Constant Name                         | Resolution | Units  | Value                   |
|---------------------------|-------------|----------|-----------------------|
| FPCFGININVAL_CNT_T_U32                | 1          | Counts | 0x0000001CU             |
| FPCFGREGID_CNT_S32                    | 1          | Counts | 10                      |
| FPCFGSELNID_CNT_S32                   | 1          | Counts | 0                       |
| REGFEPCREGID_CNT_S32                  | 1          | Counts | 2                       |
| REGFEPCSELNID_CNT_S32                 | 1          | Counts | 0                       |
| MEAREGID_CNT_S32                      | 1          | Counts | 6                       |
| MEASELNID_CNT_S32                     | 1          | Counts | 2                       |
| FPSRREGID_CNT_S32                     | 1          | Counts | 6                       |
| FPSRSELNID_CNT_S32                    | 1          | Counts | 0                       |
| FPEPCREGID_CNT_S32                    | 1          | Counts | 7                       |
| FPEPCSELNID_CNT_S32                   | 1          | Counts | 0                       |
| MEIREGID_CNT_S32                      | 1          | Counts | 8                       |
| MEISELNID_CNT_S32                     | 1          | Counts | 2                       |
| FEICREGID_CNT_S32                     | 1          | Counts | 14                      |
| FEICSELNID_CNT_S32                    | 1          | Counts | 0                       |
| FPUINVLDOPERSTSBIT_CNT_U32            | 1          | Counts | ((uint32)(0x00004000U)) |
| FPUDIVBYZEROSTSBIT_CNT_U32            | 1          | Counts | ((uint32)(0x00002000U)) |
| FPUOVFSTSBIT_CNT_U32                  | 1          | Counts | ((uint32)(0x00001000U)) |
| MEMERRINFOREADWRBIT_CNT_U32           | 1          | Counts | ((uint32)(0x00000001U)) |
| SEGVPGFMASK_CNT_U16                   | 1          | Counts | ((uint16)(0x0200U))     |
| SEGVCRFMASK_CNT_U16                   | 1          | Counts | ((uint16)(0x0100U))     |
| SEGTCMFMASK_CNT_U16                   | 1          | Counts | ((uint16)(0x0040U))     |
| SEGROMFMASK_CNT_U16                   | 1          | Counts | ((uint16)(0x0020U))     |
| SEGVCIFMASK_CNT_U16                   | 1          | Counts | ((uint16)(0x0010U))     |
| HISPDBUSRESDAREAUPPRADR_CNT_U32       | 1          | Counts | ((uint32)(0XF2FFFFFFU)) |
| HISPDBUSRESDAREALOWRADR_CNT_U32       | 1          | Counts | ((uint32)(0x10000000U)) |
| IPGREGAREAUPPRADR_CNT_U32             | 1          | Counts | ((uint32)(0XFFFEE000U)) |
| IPGREGAREALOWRADR_CNT_U08             | 1          | Counts | ((uint32)(0xFFFEE024U)) |
| SEGREGAREAUPPRADR_CNT_U32             | 1          | Counts | ((uint32)(0xFFFEE98BU)) |
| SEGREGAREALOWRADR_CNT_U08             | 1          | Counts | ((uint32)(0xFFFEE980U)) |
| PRPHLRESDAREALOWRADR_CNT_U08          | 1          | Counts | ((uint32)(0xFF000000U)) |
| CODFLSINSTRFETCHERRFEICREGVAL         | 1          | Counts | ((uint32)0x11U)         |
|                                       |            |        |                         |
| CODFLSECCDBLBITORADRPARERR_CNT_U08    | 1          | Counts | ((uint8)2U)             |
| CODFLSSEQERR_CNT_U08                  | 1          | Counts | ((uint8)4U)             |
| MEMBISTSTRTUPTESTFAILR_CNT_U08        | 1          | Counts | 1U                      |
| LCLRAMECCDBLBIT_CNT_U08               | 1          | Counts | ((uint8)2U)             |
| GBLRAMECCDBLBIT_CNT_U08               | 1          | Counts | ((uint8)4U)             |
| GTMRAMRAMECCDBLBIT_CNT_U08            | 1          | Counts | ((uint8)8U)             |
| INVLDRAMAREA_CNT_U08                  | 1          | Counts | ((uint8)128U)           |
| LCLRAMECCADROVFFLT_CNT_U08            | 1          | Counts | ((uint8)1U)             |
| GLBRAMECCADROVFFLT_CNT_U08            | 1          | Counts | ((uint8)2U)             |
| CODFLSECCADROVFFLT_CNT_U08            | 1          | Counts | ((uint8)4U)             |
| FRRAMECCOVFFLT_CNT_U08                | 1          | Counts | ((uint8)8U)             |
| CSIHRAMECCOVFFLT_CNT_U08              | 1          | Counts | ((uint8)16U)            |
| CANRAMECCOVFFLT_CNT_U08               | 1          | Counts | ((uint8)32U)            |
| GTMRAMECCOVFFLT_CNT_U08               | 1          | Counts | ((uint8)64U)            |
| GBLRAMILLGLACSBYPROCRFLT_CNT_U08      | 1          | Counts | ((uint8)1U)             |
| CODFLSILLGLACSBYSYSBUSFLT_CNT_U08     | 1          | Counts | ((uint8)2U)             |
| GBLRAMILLGLACSBYSYSBUS_CNT_U08        | 1          | Counts | ((uint8)4U)             |
| RESDAREAILLGLACSBYHISPDBUS_CNT_U08    | 1          | Counts | ((uint8)8U)             |
| DTSDBLBIT_CNT_U08                     | 1          | Counts | ((uint8)2U)             |
| BISTCODECCFAILR_CNT_U08               | 1          | Counts | ((uint8)1U)             |
| BISTNOTCMPL_CNT_U08                   | 1          | Counts | ((uint8)2U)             |
| LOGLBISTSTRTUPTESTFAILR_CNT_U08       | 1          | Counts | ((uint8)4U)             |
| FACIRSTTRFERR_CNT_U08                 | 1          | Counts | ((uint8)128U)           |
| LOCKSTEPCOMP_CNT_U08                  | 1          | Counts | ((uint8)1U)             |
| PROCLOCKSTEPRTERR_CNT_U08             | 1          | Counts | ((uint8)2U)             |
| DMALOCKSTEPRTORGBLRAMWRBUFERR_CNT_U08 | 1          | Counts | ((uint8)4U)             |
| ALGNWR_CNT_U08                        | 1          | Counts | ((uint8)8U)             |
| ALGNREAD_CNT_U08                      | 1          | Counts | ((uint8)16U)            |
| RESDOPER_CNT_U08                      | 1          | Counts | ((uint8)32U)            |
| CODFLSINSTRFETCH_CNT_U08              | 1          | Counts | ((uint8)64U)            |
| NONCODFLSINSTRFETCH_CNT_U08           | 1          | Counts | ((uint8)128U)           |
| CLKMONR0RTFLT_CNT_U08                 | 1          | Counts | ((uint8)1U)             |
| CLKMONR1RTFLT_CNT_U08                 | 1          | Counts | ((uint8)2U)             |
| CLKMONR2RTFLT_CNT_U08                 | 1          | Counts | ((uint8)4U)             |
| CLKMONR3RTFLT_CNT_U08                 | 1          | Counts | ((uint8)8U)             |
| CLKMONR5RTFLT_CNT_U08                 | 1          | Counts | ((uint8)32U)            |
| MODERRUSRMODINACTV_CNT_U08            | 1          | Counts | ((uint8)1U)             |
| MODERRPROGMMODACTV_CNT_U08            | 1          | Counts | ((uint8)2U)             |
| MODERRDBGACTV_CNT_U08                 | 1          | Counts | ((uint8)4U)             |
| MODERRTESTMODACTV_CNT_U08             | 1          | Counts | ((uint8)8U)             |
| DATAANDINSTRPROTNERR_CNT_U08          | 1          | Counts | ((uint8)1U)             |
| PRVLGDINSTREXCPN_CNT_U08              | 1          | Counts | ((uint8)2U)             |
| ECMMSTCHKRSTRTUPTESTFAILR_CNT_U08     | 1          | Counts | ((uint8)1U)             |
|                                       |            |        |                         |
| ECMCONFIGOUTPCTRLFLT_CNT_U08          | 1          | Counts | ((uint8)4U)             |
| EIINTRPTSTRTUPTESTFAILR_CNT_U08       | 1          | Counts | ((uint8)8U)             |
|                                       |            |        |                         |
| ECMMSTCHKROUTPCTRLFAILR_CNT_U08       | 1          | Counts | ((uint8)32U)            |
|                                       |            |        |                         |
| ECMRTMSTCHKRCOMPFLT_CNT_U08           | 1          | Counts | ((uint8)128U)           |
| FPUINVLDOPEREXCPN_CNT_U08             | 1          | Counts | ((uint8)2U)             |
| FPUDIVBYZEROEXCPN_CNT_U08             | 1          | Counts | ((uint8)4U)             |
| FPUOVFEXCPN_CNT_U08                   | 1          | Counts | ((uint8)8U)             |
| FPUUKWNEXCPN_CNT_U08                  | 1          | Counts | ((uint8)16U)            |
| UKWNECMRST_CNT_U08                    | 1          | Counts | ((uint8)1U)             |
| UKWNRST_CNT_U08                       | 1          | Counts | ((uint8)2U)             |
| FLSBTLDRPREOSSRTUPEXCPN_CNT_U08       | 1          | Counts | ((uint8)4U)             |
| STRTUPRSTINFOFAILD_CNT_U08            | 1          | Counts | ((uint8)8U)             |
| UKWNSWRST_CNT_U08                     | 1          | Counts | ((uint8)16U)            |
| PROGFLOW_CNT_U08                      | 1          | Counts | ((uint8)1U)             |
| DEADLINEMONR_CNT_U08                  | 1          | Counts | ((uint8)2U)             |
| ALVMONR_CNT_U08                       | 1          | Counts | ((uint8)4U)             |
| WDGTOUT_CNT_U08                       | 1          | Counts | ((uint8)1U)             |
| PBGGUARDWRERR_CNT_U08                 | 1          | Counts | ((uint8)1U)             |
| IPGRTFLT_CNT_U08                      | 1          | Counts | ((uint8)2U)             |
| PBGGUARDREADERR_CNT_U08               | 1          | Counts | ((uint8)4U)             |
| HISPDBUSGUARDERR_CNT_U08              | 1          | Counts | ((uint8)8U)             |
| CODFLSGUARDERR_CNT_U08                | 1          | Counts | ((uint8)16U)            |
| GBLRAMGUARDERR_CNT_U08                | 1          | Counts | ((uint8)32U)            |
| PEGERR_CNT_U08                        | 1          | Counts | ((uint8)64U)            |
| SYSERRGENREGWRINUSRMODE_CNT_U08       | 1          | Counts | ((uint8)1U)             |
| IPGPROTNREGWRINUSRMODE_CNT_U08        | 1          | Counts | ((uint8)2U)             |
| DBGRST_CNT_U08                        | 1          | Counts | ((uint8)1U)             |
| OSCRITFLT_CNT_U08                     | 1          | Counts | ((uint8)1U)             |
| UKWNEXCPN_CNT_U08                     | 1          | Counts | ((uint8)2U)             |
| DMATRFERR_CNT_U08                     | 1          | Counts | ((uint8)1U)             |
| DMAREGACSPROTCNERR_CNT_U08            | 1          | Counts | ((uint8)2U)             |
| PRPHLBUSADRDATAECCFLT_CNT_U08         | 1          | Counts | ((uint8)1U)             |
| PRPHLUMAPDAREAACS_CNT_U08             | 1          | Counts | ((uint8)2U)             |
| HISPDBUSUMAPDAREAACS_CNT_U08          | 1          | Counts | ((uint8)4U)             |
| BUSBRDGARBNERR_CNT_U08                | 1          | Counts | ((uint8)8U)             |
| BUSSNGBITECCERR_CNT_U08               | 1          | Counts | ((uint8)16U)            |
| INTCVMOVERVLTGMONR_CNT_U08            | 1          | Counts | ((uint8)1U)             |
| INTCVMUNDERVLTGMONR_CNT_U08           | 1          | Counts | ((uint8)2U)             |
| EXTVLTGMONRFLT_CNT_U08                | 1          | Counts | ((uint8)128U)           |
| UPPR16BITMASK_CNT_U32                 | 1          | Counts | ((uint32)(0xFFFF0000U)) |
| LOWR16BITMASK_CNT_U32                 | 1          | Counts | ((uint32)(0x0000FFFFU)) |
| FPCFGININVAL_CNT_T_U32                | 1          | Counts | ((uint32)0x0000001CU)   |
| MAXBACKUPRAMSIZE_CNT_U16              | 1          | Counts | ((uint16)1024U)         |

# Software Component Implementation

## Sub-Module Functions

#### Init: ExcpnHndlgInit1

##### **Design Rationale**

*Non-RTE function because it needs to be called before the OS is
started - so that floating point exceptions can be enabled before
anything uses floating point*

##### **Module Outputs**

*None*

#### Init: ExcpnHndlgInit2

##### **Design Rationale**

*RTE function to initialize all the NTCs to pass*

##### **Module Outputs**

*None*

## Per: ExcpnHndlgPer1

#### Design Rationale

*RTE Periodic function called every 2 ms to check for OS errors*

#### Store Module Inputs to Local copies

*Refer MDD*

####  (Processing of function)………

*Triggered on Timing Event every 2ms*

#### Store Local copy of outputs into Module Outputs

*None*

## Server Runables 

#### ChkForStrtUpTest

#####  **Design Rationale**

*Refer FDD*

#####   **Processing of function**

*Refer FDD*

#### FeNmiClkMonr0RtErr 

##### **Design Rationale**

*Refer FDD*

#####  **Processing of function**

*Refer FDD*

#### FeNmiClkMonr1RtErr

##### **Design Rationale**

*Refer FDD*

#####  **Processing of function**

*Refer FDD*

#### FeNmiClkMonr2RtErr

##### **Design Rationale**

*Refer FDD*

#####  **Processing of function**

*Refer FDD*

#### FeNmiClkMonr3RtErr

##### **Design Rationale**

*Refer FDD*

#####  **Processing of function**

*Refer FDD*

#### FeNmiClkMonr5RtErr

##### **Design Rationale**

*Refer FDD*

#####  **Processing of function**

*Refer FDD*

#### FeNmiModErrDbgActv

##### **Design Rationale**

*Refer FDD*

#####  **Processing of function**

*Refer FDD*

##### FeNmiModErrProgmModActv

##### **Design Rationale**

*Refer FDD*

#####  **Processing of function**

*Refer FDD*

#### FeNmiModErrUsrModInactv

##### **Design Rationale**

*Refer FDD*

#####  **Processing of function**

*Refer FDD*

#### FeNmiModErrTestModActv

##### **Design Rationale**

*Refer FDD*

#####  **Processing of function**

*Refer FDD*

#### FeNmiBusBrdgErr

##### **Design Rationale**

*Refer FDD*

#####  **Processing of function**

*Refer FDD*

#### FeNmiBusSngBitEccErr

##### **Design Rationale**

*Refer FDD*

#####  **Processing of function**

*Refer FDD*

#### FeNmiCodFlsEccAdrOvfErr

##### **Design Rationale**

*Refer FDD*

#####  **Processing of function**

*Refer FDD*

#### FeNmiCodFlsIllglAcsBySysBus

##### **Design Rationale**

*Refer FDD*

#####  **Processing of function**

*Refer FDD*

#### FeNmiDmaIllglAcsErr

##### **Design Rationale**

*Refer FDD*

#####  **Processing of function**

*Refer FDD*

#### FeNmiDmaLockStepErrOrGblRamWrBufErr

##### **Design Rationale**

*Refer FDD*

#####  **Processing of function**

*Refer FDD*

#### FeNmiDmaTrfErr

##### **Design Rationale**

*Refer FDD*

#####  **Processing of function**

*Refer FDD*

#### FeNmiDtsRamDblBitEccErr

##### **Design Rationale**

*Refer FDD*

#####  **Processing of function**

*Refer FDD*

#### FeNmiEcmMstChkrErr

##### **Design Rationale**

*Refer FDD*

#####  **Processing of function**

*Refer FDD*

#### FeNmiFlsSeqErr

##### **Design Rationale**

*Refer FDD*

#####  **Processing of function**

*Refer FDD*

#### FeNmiGblRamIllglAcsByProcr

##### **Design Rationale**

*Refer FDD*

#####  **Processing of function**

*Refer FDD*

#### FeNmiGblRamIllglAcsBySysBus

##### **Design Rationale**

*Refer FDD*

#####  **Processing of function**

*Refer FDD*

#### FeNmiPrphlRamEccAdrOvfErr

##### **Design Rationale**

*Refer FDD*

#####  **Processing of function**

*Refer FDD*

#### FeNmiGlbRamEccAdrOvfErr

##### **Design Rationale**

*Refer FDD*

#####  **Processing of function**

*Refer FDD*

#### FeNmiGtmRamDblBitEccErr

##### **Design Rationale**

*Refer FDD*

#####  **Processing of function**

*Refer FDD*

#### FeNmiLclRamEccAdrOvfErr

##### **Design Rationale**

*Refer FDD*

#####  **Processing of function**

*Refer FDD*

#### FeNmiPegErr

##### **Design Rationale**

*Refer FDD*

#####  **Processing of function**

*Refer FDD*

#### FeNmiProcrLockStepErr

##### **Design Rationale**

*Refer FDD*

#####  **Processing of function**

*Refer FDD*

#### FeNmiResdAreaIllglAcsByHiSpdBus

##### **Design Rationale**

*Refer FDD*

#####  **Processing of function**

*Refer FDD*

#### FeNmiWdgErr

##### **Design Rationale**

*Refer FDD*

#####  **Processing of function**

*Refer FDD*

#### ProcUkwnExcpnErr

##### **Design Rationale**

*Refer FDD*

#####  **Processing of function**

*Refer FDD*

#### ProcMpuExcpnErr

##### **Design Rationale**

*Refer FDD*

#####  **Processing of function**

*Refer FDD*

#### ProcPrvlgdInstrExcpnErr

##### **Design Rationale**

*Refer FDD*

#####  **Processing of function**

*Refer FDD*

#### ProcPrmntOsErr

##### **Design Rationale**

*Refer FDD*

#####  **Processing of function**

*Refer FDD*

#### ProcNonCritOsErr

##### **Design Rationale**

*Refer FDD*

#####  **Processing of function**

*Refer FDD*

#### GetMcuDiagcIdnData

##### **Design Rationale**

*Refer FDD*

#####  **Processing of function**

*Refer FDD*

#### SetMcuDiagcIdnData

##### **Design Rationale**

*Refer FDD*

#####  **Processing of function**

*Refer FDD*

## Interrupt Functions

#### AlgnErrIrq 

##### **Design Rationale**

*Refer FDD*

#####  **Processing of function**

*Refer FDD*

#### FpuErrIrq 

##### **Design Rationale**

*Refer FDD*

#####  **Processing of function**

*Refer FDD*

#### SysErrIrq

##### **Design Rationale**

*Refer FDD*

#####  **Processing of function**

*Refer FDD*

#### ResdOperIrq

##### **Design Rationale**

*Refer FDD*

#####  **Processing of function**

*Refer FDD*

## Module Internal (Local) Functions

#### ProcStrtUpOrSwRst 

|                      |                   |      |     |     |
|----------------------|-------------------|------|-----|-----|
| **Function Name**    | ProcStrtUpOrSwRst | Type | Min | Max |
| **Arguments Passed** | None              |      |     |     |
|                      |                   |      |     |     |
| **Return Value**     | NA                |      |     |     |

##### **Design Rationale**

*Refer FDD*

#####  **Processing of function**

*Refer FDD*

#### McuDiagcRstChk 

|                      |                          |           |             |             |
|--------------|------------------------------|----------|----------|----------|
| **Function Name**    | McuDiagcRstChk           | Type      | Min         | Max         |
| **Arguments Passed** | RstInfo_Cnt_T_enum       | McuDiagc1 | Refer FDD\* | Refer FDD\* |
|                      |                          |           |             |             |
| **Return Value**     | McuDiagcRstChk_Cnt_T_lgc | Boolean   | FALSE       | TRUE        |

##### **Design Rationale**

*Checks if the reset cause is power on/Flash Progamming /Hard Reset
/Soft Reset.*

##### **Processing**

Refer the FDD

## GLOBAL Function/Macro Definitions

\<If these are numerous and defined in a separate source file then
reference the source file only.\>

## GLOBAL Function \#1

|                      |                                                    |                               |                               |                               |
|--------------|------------------------------|----------|----------|----------|
| **Function Name**    | (Exact name used)                                  | Type                          | Min                           | Max                           |
| **Arguments Passed** | (if none, write None)                              | \<Refer MDD guidelines\[1\]\> | \<Refer MDD guidelines\[1\]\> | \<Refer MDD guidelines\[1\]\> |
|                      | (Insert more rows for additional passed arguments) |                               |                               |                               |
| **Return Value**     | (if no value returned, write N/A)                  |                               |                               |                               |

## Design Rationale

## processing

(Place flowchart/design for local function)

# Known Limitations with Design

None

# UNIT TEST CONSIDERATION

The PIMs listed in the Data dictionary file BackUpRam and
ExcpnHndlgOsErrCod are non RTE PIMS which need special memory mapping
and are not generated through RTE. Hence use the component level
variable name as used in the component for these PIMs

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

| **Ref. \#** | **Title**                                                                                                                                                             | **Version**                    |
|-------|--------------------------------------------|----------------------|
| 1           | AUTOSAR Specification of Memory Mapping (Link:[AUTOSAR_SWS_MemoryMapping.pdf](http://www.autosar.org/download/R4.0/AUTOSAR_SWS_MemoryMapping.pdf))                    | v1.3.0 R4.0 Rev 2              |
| 2           | MDD Guideline                                                                                                                                                         | Process 04.04.02               |
| 3           | [Software Naming Conventions.doc](http://misagweb01.nexteer.com/eRoomReq/Files/erooms8/NextGeneration/0_fc55f/Software%20Naming%20Conventions%2003x(In%20Work).doc)   | Process 04.04.02               |
| 4           | [Software Design and Coding Standards.doc](http://eroom1.nexteer.com/eRoomReq/Files/erooms8/NextGeneration/0_1a67a9/Software%20Design%20and%20Coding%20Standards.doc) | Process 04.04.02               |
| 5           | FDD (CM101B_ExcpnHndlg_Design)                                                                                                                                        | See Synergy Subproject version |

{% endraw %}