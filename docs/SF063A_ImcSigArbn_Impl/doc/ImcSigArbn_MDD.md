---
layout: default
title: ImcSigArbn_MDD
nav_order: 2
parent: Component Implementation
---
{% raw %}
**Module Design Document**

**For**

**ImcSigArbn**

**May 11, 2017**

**Prepared By:**

**Krishna Anne,**

**Nexteer Automotive,**

**Saginaw, MI, USA  
<u>Change History</u>**

|                                                 |                  |             |            |
|------------------------|---------------------|--------------|--------------|
| **Description**                                 | **Author**       | **Version** | **Date**   |
| Initial Version                                 | Shruthi Raghavan | 1.0         | 02/02/2017 |
| Fix for Issues in using Return value of ImcData | Krishna Anne     | 2.0         | 05/11/2017 |

**  
**

<u>Table of Contents</u>1 Introduction 4

1.1 Purpose 4

2 ImcSigArbn & High-Level Description 5

3 Design details of software module 6

3.1 Graphical representation of ImcSigArbn 6

3.2 Data Flow Diagram 6

3.2.1 Component level DFD 6

3.2.2 Function level DFD 6

4 Constant Data Dictionary 7

4.1 Program (fixed) Constants 7

4.1.1 Embedded Constants 7

5 Software Component Implementation 8

5.1 Sub-Module Functions 8

5.1.1 Init: ImcSigArbnInit1 8

5.1.1.1 Design Rationale 8

5.1.2 Per: ImcSigArbnPer1 8

5.1.2.1 Design Rationale 8

5.1.3 Per: ImcSigArbnPer2 8

5.1.3.1 Design Rationale 8

5.2 Server Runnables 8

5.3 Interrupt Functions 8

5.4 Module Internal (Local) Functions 8

5.4.1 Local Function \#1 8

5.4.1.1 Design Rationale 9

5.5 GLOBAL Function/Macro Definitions 9

6 Known Limitations with Design 10

7 UNIT TEST CONSIDERATION 11

Appendix A Abbreviations and Acronyms 12

Appendix B Glossary 13

Appendix C References 14

# Introduction

## Purpose

> Module design document for ImcSigArbn SF063A to refer for design
> rationale, unit test considerations and implementation details.

# ImcSigArbn & High-Level Description

> This function shall define the requirements for sharing signals. It
> shall serve as a single function of contact to obtain information from
> the other controller in a dual ECU structure. It shall define
> requirements for arbitration of signals and integrator states to
> ensure performance.

# Design details of software module

## Graphical representation of ImcSigArbn

> <img
> src="ElectricPowerSteering_RH850_FORD_T3T6_website/docs/SF063A_ImcSigArbn_Impl/doc/mediax/media/image1.png"
> style="width:4.03435in;height:6.72391in" />

## Data Flow Diagram

### Component level DFD

Refer FDD Simulink model.

### Function level DFD

Refer FDD Simulink Model

# Constant Data Dictionary

## Program (fixed) Constants

### Embedded Constants

#### Local Constants

| Constant Name            | Resolution | Units | Value |
|--------------------------|------------|-------|-------|
| Refer to DataDict.m file |            |       |       |

# Software Component Implementation

## Sub-Module Functions

## Init: ImcSigArbnInit1

## Design Rationale

> Refer FDD Simulink model

## Per: ImcSigArbnPer1

## Design Rationale

> Refer FDD Simulink model  
> The implementation of ElapsedTime block was optimized in the code to
> avoid a couple of Boolean operations and additional temporary
> variables. The functionality was verified in peer review with design
> owner as well.

## Per: ImcSigArbnPer2

## Design Rationale

> Refer FDD Simulink model  
> The implementation of ElapsedTime block was optimized in the code to
> avoid a couple of Boolean operations and additional temporary
> variables. The functionality was verified in peer review with design
> owner as well.

## Server Runnables

None

## Interrupt Functions

> None

## Module Internal (Local) Functions

## Local Function \#1

<table>
<colgroup>
<col style="width: 15%" />
<col style="width: 24%" />
<col style="width: 11%" />
<col style="width: 24%" />
<col style="width: 23%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Function Name</strong></td>
<td>CalcImcSigOffs</td>
<td>Type</td>
<td>Min</td>
<td>Max</td>
</tr>
<tr class="even">
<td><strong>Arguments Passed</strong></td>
<td>ImcSigArbnEna_Cnt_T_logl</td>
<td>Boolean</td>
<td>0</td>
<td>1</td>
</tr>
<tr class="odd">
<td></td>
<td>InpSig_Uls_T_f32</td>
<td>Float32</td>
<td>-32767.5</td>
<td>32767.5</td>
</tr>
<tr class="even">
<td></td>
<td>ImcSig_Uls_T_f32</td>
<td>Float32</td>
<td>-32767.5</td>
<td>32767.5</td>
</tr>
<tr class="odd">
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td>*SigLpFil_Uls_T_str</td>
<td>FilLpRec1</td>
<td>[struct ('FilSt’, -32767.5,<br />
'FilGain', 0. 062831853000000)]</td>
<td>[struct('FilSt', 32767.5,<br />
'FilGain', 0. 998132557254885)]</td>
</tr>
<tr class="odd">
<td></td>
<td>*OutSigPrev_Uls_T_f32</td>
<td>Float32</td>
<td>-32767.5</td>
<td>32767.5</td>
</tr>
<tr class="even">
<td></td>
<td>ImcSigArbnSigOffsLim_Uls_T_f32</td>
<td>Float32</td>
<td>0</td>
<td>32767.5</td>
</tr>
<tr class="odd">
<td></td>
<td>Sts_Cnt_T_enum</td>
<td>ImcArbnRxSts1</td>
<td>IMCARBNRXSTS_NODATA</td>
<td>IMCARBNRXSTS_INVLD</td>
</tr>
<tr class="even">
<td></td>
<td>Rtn_Cnt_T_enum</td>
<td>Std_ReturnType</td>
<td>E_NOT_OK</td>
<td>E_OK</td>
</tr>
<tr class="odd">
<td><strong>Return Value</strong></td>
<td>OutSigPrev_Uls_T_f32</td>
<td>Float32</td>
<td>-32767.5</td>
<td>32767.5</td>
</tr>
</tbody>
</table>

## Design Rationale

All the ImcSigArbn\_\* functions in the Per2 inside ‘Calc Offs Corrn
10ms Periodic’ block of FDD do the same function with different cals,
pims and input signals. So they were all clubbed into single function.

## Local Function \#1

|                      |                |         |     |            |
|----------------------|----------------|---------|-----|------------|
| **Function Name**    | CalcImcSigOffs | Type    | Min | Max        |
| **Arguments Passed** | SetArbnNtc     | float32 | 0   | 4294967296 |
| **Return Value**     | NA             | NA      | NA  | NA         |

## Design Rationale

To handle cyclomatic complexity.

## GLOBAL Function/Macro Definitions

> None

# Known Limitations with Design

1.  Filter ranges given in design are full range of float for state
    variable and \[0,max_float32\] for gain – this has to be fixed in
    next version. For now, the ranges are given in the unit test
    considerations after calculating from the code. These values can be
    used instead.

2.  The value of calculated float32 offset signals are limited to
    \[-cal, cal\] and then later checked for absolute value being
    greater than or equal to the same cal. This was verified by
    component owner as not the design intent & one of these places, the
    cal used has to change.

3.  The input signal PosnTrakgIntgtrSt1 has a range of \[-2864,2864\]
    according to the DataDict.m file. If its IMC counterpart
    ImcPosnTrakgIntgtrSt1 read in Per2 has the same range
    \[-2864,2864\], the algorithm inside the
    ImcSigArbn_PosnTrakgIntglSt1 will only give output
    PosnTrakgIntgtrSt1Offs values

> **\[Refer: SF063A_ImcSigArbn/ImcSigArbn/ImcSigArbnPer2/Calculate Offs
> Corrn 10 ms Periodic /ImcSigArbn_PosnTrakgIntglSt1/Do arbitration\]  
> **in the range \[-2864,2864\]. However, the limit used on this value
> is a calibration ImcSigArbnPosnTrakg1ArbnOffsLim whose range is
> \[0,32767.5\], max is much larger than the actual maximum that can be
> taken by this variable. Also, the output limits on the
> PosnTrakgIntgtrSt1Offs output is \[-32767.5,32767.5\], which needs to
> change.

1.  The units on the embedded constants INTGTROFFSSATNLOWLIM_ULS_F32 and
    INTGTROFFSSATNUPPRLIM_ULS_F32 need to change if a different set of
    constants are decided to be used for PosnTrakgIntgtrSt1Offs limits

# UNIT TEST CONSIDERATION

In case the m file gives float min/max values as the ranges for the
following PIMs, use the values from this table instead as the range.

| PIM Variables               |                   | Ranges              |                     |
|----------------------|----------------|------------------|------------------|
| Structure Name              | Structure Element | Min                 | Max                 |
| **HwAgLpFil**               | FilSt             | -1440               | 1440                |
|                             | FilGain           | 0\. 062831853000000 | 0\. 998132557254885 |
| **HwAgTarLpFil**            | FilSt             | -1440               | 1440                |
|                             | FilGain           | 0\. 062831853000000 | 0\. 998132557254885 |
| **HwTqLpFil**               | FilSt             | -10                 | 10                  |
|                             | FilGain           | 0\. 062831853000000 | 0\. 998132557254885 |
| **MotVelLpFil**             | FilSt             | -1350               | 1350                |
|                             | FilGain           | 0\. 062831853000000 | 0\. 998132557254885 |
| **PosnServoIntgtrLpFil**    | FilSt             | -32767.5            | 32767.5             |
|                             | FilGain           | 0\. 062831853000000 | 0\. 998132557254885 |
| **PullCmpLongTermCmpLpFil** | FilSt             | -10                 | 10                  |
|                             | FilGain           | 0\. 062831853000000 | 0\. 998132557254885 |
| **PullCmpShoTermCmpLpFil**  | FilSt             | -10                 | 10                  |
|                             | FilGain           | 0\. 062831853000000 | 0\. 998132557254885 |
| **TrakgIntgtrSt1LpFil**     | FilSt             | -2864               | 2864                |
|                             | FilGain           | 0\. 062831853000000 | 0\. 998132557254885 |
| **TrakgIntgtrSt2LpFil**     | FilSt             | -20000              | 20000               |
|                             | FilGain           | 0\. 062831853000000 | 0\. 998132557254885 |
| **VehSpdLpFil**             | FilSt             | 0                   | 511                 |
|                             | FilGain           | 0\. 062831853000000 | 0\. 998132557254885 |

Tolerance of state variables can be assumed to be six significant digits
and for the gains it is 1e-07.

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

<table>
<colgroup>
<col style="width: 8%" />
<col style="width: 46%" />
<col style="width: 44%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Ref. #</strong></th>
<th><strong>Title</strong></th>
<th><strong>Version</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>1</td>
<td>AUTOSAR Specification of Memory Mapping<br />
(Link:<a
href="http://www.autosar.org/download/R4.0/AUTOSAR_SWS_MemoryMapping.pdf">AUTOSAR_SWS_MemoryMapping.pdf</a>)</td>
<td>v1.3.0 R4.0 Rev 2</td>
</tr>
<tr class="even">
<td>2</td>
<td>MDD Guideline</td>
<td>See Software Engineering Process 04.02.01</td>
</tr>
<tr class="odd">
<td>3</td>
<td><a
href="http://misagweb01.nexteer.com/eRoomReq/Files/erooms8/NextGeneration/0_fc55f/Software%20Naming%20Conventions%2003x(In%20Work).doc">Software
Naming Conventions.doc</a></td>
<td>See Software Engineering Process 04.02.01</td>
</tr>
<tr class="even">
<td>4</td>
<td><a
href="http://eroom1.nexteer.com/eRoomReq/Files/erooms8/NextGeneration/0_1a67a9/Software%20Design%20and%20Coding%20Standards.doc">Software
Design and Coding Standards.doc</a></td>
<td>See Software Engineering Process 04.02.01</td>
</tr>
<tr class="odd">
<td>5</td>
<td>SF063A_ImcSigArbn_Design</td>
<td>See Synergy Sub-Project Version</td>
</tr>
</tbody>
</table>

{% endraw %}