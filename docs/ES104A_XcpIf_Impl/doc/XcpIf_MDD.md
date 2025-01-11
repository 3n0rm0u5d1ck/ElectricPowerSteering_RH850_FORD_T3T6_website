---
layout: default
title: XcpIf_MDD
nav_order: 3
parent: Component Implementation
---
{% raw %}
**Module Design Document**

**For**

**XCP Interface (XcpIf)**

**VERSION:** **4.0**

**DATE:** **12-Feb-2018**

**Prepared By:**

**Kevin Smith**

**EPS Software,**

**Nexteer Automotive,**

**Saginaw, MI, USA**

**  
Location:** The official version of this document is stored in the
Nexteer Configuration Management System.

**Revision History**

|             |                                            |            |             |           |                 |
|-----|-------------------|-------------------|--------|-----------|-----------|
| **Sl. No.** | **Description**                            | **Author** | **Version** | **Date**  | **Approved By** |
| 1           | Initial Version                            | K. Smith   | 1.0         | 16-Jun-15 |                 |
| 2           | Updates for anomaly EA4#6672               | K. Smith   | 2.0         | 29-Aug-16 |                 |
| 3           | Updates for change request EA4#8215        | K. Smith   | 3.0         | 03-Mar-17 |                 |
| 4           | Updates for CR EA4#20563 anomaly EA4#20564 | K. Smith   | 4.0         | 12-Feb-18 |                 |

**<u>  
Table of Contents</u>**

1 Abbrevations And Acronyms 5

2 References 6

3 XCP Interface & High-Level Description 7

4 Design details of software module 8

4.1 Graphical representation of XCP Interface 8

4.2 Data Flow Diagram 8

4.2.1 Module level DFD 8

4.2.2 Sub-Module level DFD 8

4.3 COMPONENT FLOW DIAGRAM 8

5 Variable Data Dictionary 9

5.1 User defined typedef definition/declaration 9

5.2 Variable definition for enumerated types 9

6 Constant Data Dictionary 10

6.1 Program(fixed) Constants 10

6.1.1 Embedded Constants 10

6.1.1.1 Local 10

6.1.1.2 Global 10

6.1.2 Module specific Lookup Tables Constants 10

7 Software Module Implementation 11

7.1 Sub-Module Functions 11

7.2 Initialization Functions 11

7.2.1 CDD_XcpIfInit1 11

7.2.1.1 Design Rationale 11

7.2.1.2 Store Module Inputs to Local copies 11

7.2.1.3 (Processing of function)……… 11

7.2.1.4 Store Local copy of outputs into Module Outputs 11

7.3 PERIODIC FUNCTIONS 11

7.3.1 CDD_XcpIfPer1 11

7.3.1.1 Design Rationale 11

7.3.1.2 Store Module Inputs to Local copies 11

7.3.1.3 (Processing of function)……… 12

7.3.1.4 Store Local copy of outputs into Module Outputs 12

7.3.2 Xcp2msDaq 12

7.3.2.1 Design Rationale 12

7.3.2.2 Store Module Inputs to Local copies 12

7.3.2.3 (Processing of function)……… 12

7.3.2.4 Store Local copy of outputs into Module Outputs 12

7.4 Non PERIODIC FUNCTIONS 12

7.5 Interrupt Functions 12

7.6 Serial Communication Functions 13

7.7 Local Function/Macro Definitions 13

7.8 GLObAL Function/Macro Definitions 14

7.8.1 ApplXcpGetTimestamp 14

7.8.1.1 Description 14

7.8.2 ApplXcpGetPointer 14

7.8.2.1 Description 14

7.8.3 ApplXcpCalibrationWrite 15

7.8.3.1 Description 15

7.8.4 ApplXcpWrCmn 16

7.8.4.1 Description 16

7.8.5 ApplXcpCalibrationRead 16

7.8.5.1 Description 16

7.8.6 ApplXcpCheckWriteAccess 17

7.8.6.1 Description 17

7.8.7 ApplXcpCheckReadAccess 17

7.8.7.1 Description 17

7.8.8 ApplXcpCheckDAQAccess 18

7.8.8.1 Description 18

7.8.9 ApplXcpSetCalPage 19

7.8.9.1 Description 19

7.8.10 ApplXcpGetCalPage 20

7.8.10.1 Description 20

7.8.11 ApplXcpCopyCalPage 21

7.8.11.1 Description 21

7.8.12 ApplXcpUserService 22

7.8.12.1 Description 22

7.8.13 ApplXcpOpenCmdIf 23

7.8.13.1 Description 23

7.8.14 NONTRUSTED_NtWrapS_Rte_Call_CopyCalPageReq_Oper 24

7.8.14.1 Description 24

7.8.15 NONTRUSTED_NtWrapS_Rte_Call_SetCalPageReq_Oper 24

7.8.15.1 Description 24

7.9 TRANSIENT FUNCTIONS 25

8 Unit Test Considerations 26

9 Known Limitations With Design 27

10 Appendix 28

# Abbrevations And Acronyms

| Abbreviation | Description                             |
|--------------|-----------------------------------------|
| DFD          | Design functional diagram               |
| MDD          | Module design Document                  |
|              | \<ADD more to the table if applicable\> |
|              |                                         |

# References

This section lists the title & version of all the documents that are
referred for development of this document

| Sr. No. | Title                           | Version       |
|---------|---------------------------------|---------------|
| \<1\>   | \<MDD Guidelines\>              | 4.0.0         |
| \<2\>   | \<Software Naming Conventions\> | 4.0.0         |
| \<3\>   | \<Coding standards\>            | 4.0.0         |
| \<4\>   | \<FDD \>                        | Not available |
|         | \<Add if more available\>       |               |

# XCP Interface & High-Level Description

XCP Interface provides multiple functions that allow XCP end users and
tools to interface with software components contained in the
application.

# Design details of software module

## Graphical representation of XCP Interface

*None*

## Data Flow Diagram

*None*

## Module level DFD

*None*

## Sub-Module level DFD

*None*

## COMPONENT FLOW DIAGRAM

*None*

# Variable Data Dictionary

## User defined typedef definition/declaration 

<table>
<colgroup>
<col style="width: 34%" />
<col style="width: 31%" />
<col style="width: 11%" />
<col style="width: 11%" />
<col style="width: 11%" />
</colgroup>
<thead>
<tr class="header">
<th>Typedef Name</th>
<th>Element Name</th>
<th>User Defined Type</th>
<th><p>Legal Range</p>
<p>(min)</p></th>
<th><p>Legal Range</p>
<p>(max)</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

## Variable definition for enumerated types

| Enum Name | Element Name | Value |
|-----------|--------------|-------|
|           |              |       |

# Constant Data Dictionary

## Program(fixed) Constants

## Embedded Constants

## Local

| Constant Name | Resolution | Units | Value |
|---------------|------------|-------|-------|
|               |            |       |       |

## Global

| Constant Name             |
|---------------------------|
| XcpEventChannel_2ms_DAQ_2 |

## Module specific Lookup Tables Constants

| Constant Name | Resolution | Value | Software Segment |
|---------------|------------|-------|------------------|
|               |            |       |                  |

# Software Module Implementation

## Sub-Module Functions

*None*

## Initialization Functions

## CDD_XcpIfInit1

## Design Rationale

*This function is called at init to enable or disable XCP access.*

## Store Module Inputs to Local copies

*None*

## (Processing of function)………

## Store Local copy of outputs into Module Outputs

*None*

## PERIODIC FUNCTIONS 

## CDD_XcpIfPer1

## Design Rationale

*This function is called every 100ms to enable or disable* *XCP access.*

## Store Module Inputs to Local copies

*None*

## (Processing of function)………

## Store Local copy of outputs into Module Outputs

*None*

## Xcp2msDaq

## Design Rationale

*This function is called every 2ms for executing the XcpEvent functions
for the 2ms DAQ.*

## Store Module Inputs to Local copies

*None*

## (Processing of function)………

![](ElectricPowerSteering_RH850_FORD_T3T6_website/docs/ES104A_XcpIf_Impl/doc/mediax/media/image2.emf)

## Store Local copy of outputs into Module Outputs

*None*

## Non PERIODIC FUNCTIONS 

*None*

## Interrupt Functions

*None*

## Serial Communication Functions

*None*

## Local Function/Macro Definitions

None

## GLObAL Function/Macro Definitions

## ApplXcpGetTimestamp

|                      |                     |                     |                 |                 |
|-------------|----------------------------|--------------|---------|---------|
| **Function Name**    | ApplXcpGetTimestamp | Type                | Min             | Max             |
| **Arguments Passed** | None                |                     |                 |                 |
|                      |                     |                     |                 |                 |
| **Return Value**     | Timestamp_Cnt_T_u32 | XcpDaqTimestampType | See description | See description |

## Description

This function returns the timestamp that is based on a reference timer.
The range of return values vary depending on the configuration of the
Xcp Component. The data type can range from a full range of a uint8 to a
uint32 value.

![](ElectricPowerSteering_RH850_FORD_T3T6_website/docs/ES104A_XcpIf_Impl/doc/mediax/media/image3.emf)

## ApplXcpGetPointer

|                      |                   |            |     |            |
|----------------------|-------------------|------------|-----|------------|
| **Function Name**    | ApplXcpGetPointer | Type       | Min | Max        |
| **Arguments Passed** | addr_ext          | vuint8     | 0   | 255        |
|                      | addr              | vuint32    | 1   | 4294967295 |
| **Return Value**     | RtnAddr_Cnt_T_u32 | MTABYTEPTR | 1   | 4294967295 |

## Description

This function takes the extension and address of and returns the
physical address of the item.

![](ElectricPowerSteering_RH850_FORD_T3T6_website/docs/ES104A_XcpIf_Impl/doc/mediax/media/image4.emf)

## ApplXcpCalibrationWrite

|                      |                         |            |     |            |
|----------------------|-------------------------|------------|-----|------------|
| **Function Name**    | ApplXcpCalibrationWrite | Type       | Min | Max        |
| **Arguments Passed** | addr                    | MTABYTEPTR | 1   | 4294967295 |
|                      | size                    | Vuint8     | 0   | 255        |
|                      | data                    | BYTEPTR    | 1   | 4294967295 |
| **Return Value**     | XCP_CMD_OK              | Uint8      | 0   | 0          |

## Description

This function calls the common XCP writing function. For this deisgn,
the function call will be translated into a trusted function call.

![](ElectricPowerSteering_RH850_FORD_T3T6_website/docs/ES104A_XcpIf_Impl/doc/mediax/media/image5.emf)

## ApplXcpWrCmn

|                      |              |            |     |            |
|----------------------|--------------|------------|-----|------------|
| **Function Name**    | ApplXcpWrCmn | Type       | Min | Max        |
| **Arguments Passed** | addr         | MTABYTEPTR | 1   | 4294967295 |
|                      | size         | Vuint8     | 0   | 255        |
|                      | data         | BYTEPTR    | 1   | 4294967295 |
| **Return Value**     | XCP_CMD_OK   | Uint8      | 0   | 0          |

## Description

This function writes the data passed in by the XCP user to the
designated address.

![](ElectricPowerSteering_RH850_FORD_T3T6_website/docs/ES104A_XcpIf_Impl/doc/mediax/media/image6.emf)

## ApplXcpCalibrationRead

|                      |                        |            |     |            |
|----------------------|------------------------|------------|-----|------------|
| **Function Name**    | ApplXcpCalibrationRead | Type       | Min | Max        |
| **Arguments Passed** | addr                   | MTABYTEPTR | 1   | 4294967295 |
|                      | size                   | Vuint8     | 0   | 255        |
|                      | data                   | BYTEPTR    | 1   | 4294967295 |
| **Return Value**     | XCP_CMD_OK             | Uint8      | 0   | 0          |

## Description

This function reads the data in the designated address and returns it to
the XCP user.

![](ElectricPowerSteering_RH850_FORD_T3T6_website/docs/ES104A_XcpIf_Impl/doc/mediax/media/image7.emf)

##  ApplXcpCheckWriteAccess

|                      |                         |            |     |            |
|----------------------|-------------------------|------------|-----|------------|
| **Function Name**    | ApplXcpCheckWriteAccess | Type       | Min | Max        |
| **Arguments Passed** | addr                    | MTABYTEPTR | 1   | 4294967295 |
|                      | Size_Cnt_T_u08          | Vuint8     | 0   | 255        |
| **Return Value**     | XCP_CMD_OK              | Uint8      | 0   | 0          |

## Description

This function checks access for XCP writes. Since the functions in
tuning selection management handle the presmissions for writes, this
function shall always return a positive response.

![](ElectricPowerSteering_RH850_FORD_T3T6_website/docs/ES104A_XcpIf_Impl/doc/mediax/media/image8.emf)

## ApplXcpCheckReadAccess

|                      |                        |            |     |            |
|----------------------|------------------------|------------|-----|------------|
| **Function Name**    | ApplXcpCheckReadAccess | Type       | Min | Max        |
| **Arguments Passed** | addr                   | MTABYTEPTR | 1   | 4294967295 |
|                      | Size_Cnt_T_u08         | Vuint8     | 0   | 255        |
| **Return Value**     | XCP_CMD_OK             | Uint8      | 0   | 0          |

## Description

This function checks access for XCP reads. Since the functions in tuning
selection management handle the presmissions for reads, this function
shall always return a positive response.

![](ElectricPowerSteering_RH850_FORD_T3T6_website/docs/ES104A_XcpIf_Impl/doc/mediax/media/image8.emf)

## ApplXcpCheckDAQAccess

|                      |                       |            |     |            |
|----------------------|-----------------------|------------|-----|------------|
| **Function Name**    | ApplXcpCheckDAQAccess | Type       | Min | Max        |
| **Arguments Passed** | addr                  | MTABYTEPTR | 1   | 4294967295 |
|                      | Size_Cnt_T_u08        | Vuint8     | 0   | 255        |
| **Return Value**     | XCP_CMD_OK            | Uint8      | 0   | 0          |

## Description

This function checks access for XCP DAQ access. Since all reads are
allowed, this function will also always return a positive response.

![](ElectricPowerSteering_RH850_FORD_T3T6_website/docs/ES104A_XcpIf_Impl/doc/mediax/media/image8.emf)

## ApplXcpSetCalPage

|                      |                   |        |     |      |
|----------------------|-------------------|--------|-----|------|
| **Function Name**    | ApplXcpSetCalPage | Type   | Min | Max  |
| **Arguments Passed** | Seg_Cnt_T_u08     | Vuint8 | 0   | 255  |
|                      | Page_Cnt_T_u08    | Vuint8 | 0   | 255  |
|                      | Mod_Cnt_T_u08     | Vuint8 | 0   | 255  |
| **Return Value**     | Rtn_Cnt_T_u08     | Uint8  | 0   | 0x28 |

## Description

This function sets the calibration page access. It directly calls the
functions used in tuning selection management.

![](ElectricPowerSteering_RH850_FORD_T3T6_website/docs/ES104A_XcpIf_Impl/doc/mediax/media/image9.emf)

## ApplXcpGetCalPage

|                      |                   |        |     |      |
|----------------------|-------------------|--------|-----|------|
| **Function Name**    | ApplXcpGetCalPage | Type   | Min | Max  |
| **Arguments Passed** | Seg_Cnt_T_u08     | Vuint8 | 0   | 255  |
|                      | Mod_Cnt_T_u08     | Vuint8 | 0   | 255  |
| **Return Value**     | Rtn_Cnt_T_u08     | Uint8  | 0   | 0x28 |

## Description

This function sets the calibration page access. It directly calls the
functions used in tuning selection management.

![](ElectricPowerSteering_RH850_FORD_T3T6_website/docs/ES104A_XcpIf_Impl/doc/mediax/media/image10.emf)

## ApplXcpCopyCalPage

|                      |                    |        |     |      |
|----------------------|--------------------|--------|-----|------|
| **Function Name**    | ApplXcpCopyCalPage | Type   | Min | Max  |
| **Arguments Passed** | SrcSeg_Cnt_T_u08   | Vuint8 | 0   | 255  |
|                      | SrcPage_Cnt_T_u08  | Vuint8 | 0   | 255  |
|                      | DestSeg_Cnt_T_u08  | Vuint8 | 0   | 255  |
|                      | DestPage_Cnt_T_u08 | Vuint8 | 0   | 255  |
| **Return Value**     | XCP_CMD_OK         | Uint8  | 0   | 0x28 |

## Description

This function sets the calibration page access. It directly calls the
functions used in tuning selection management.

![](ElectricPowerSteering_RH850_FORD_T3T6_website/docs/ES104A_XcpIf_Impl/doc/mediax/media/image11.emf)

## ApplXcpUserService

|                      |                    |         |     |            |
|----------------------|--------------------|---------|-----|------------|
| **Function Name**    | ApplXcpUserService | Type    | Min | Max        |
| **Arguments Passed** | pCmd               | BYTEPTR | 0   | 4294967295 |
| **Return Value**     | XCP_CMD_OK         | Uint8   | 0   | 0x3        |

## Description

This function handles user service requests.

![](ElectricPowerSteering_RH850_FORD_T3T6_website/docs/ES104A_XcpIf_Impl/doc/mediax/media/image12.emf)

## ApplXcpOpenCmdIf

|                      |                  |         |     |            |
|----------------------|------------------|---------|-----|------------|
| **Function Name**    | ApplXcpOpenCmdIf | Type    | Min | Max        |
| **Arguments Passed** | pCmd             | BYTEPTR | 0   | 4294967295 |
|                      | pRes             | BYTEPTR | 0   | 4294967295 |
|                      | pLength          | BYTEPTR | 0   | 4294967295 |
| **Return Value**     | XCP_CMD_OK       | Uint8   | 0   | 0x3        |

## Description

This function handles XCP service requests that are not supported by the
driver but defined by the XCP protocol specification.

![](ElectricPowerSteering_RH850_FORD_T3T6_website/docs/ES104A_XcpIf_Impl/doc/mediax/media/image13.emf)

## NONTRUSTED_NtWrapS_Rte_Call_CopyCalPageReq_Oper

|                      |                                                 |                                    |     |       |
|--------|------------------------------|---------------------|-----|---------|
| **Function Name**    | NONTRUSTED_NtWrapS_Rte_Call_CopyCalPageReq_Oper | Type                               | Min | Max   |
| **Arguments Passed** | FunctionIndex                                   | NonTrustedFunctionIndexType        | 0   | 65535 |
|                      | FunctionParams                                  | NonTrustedFunctionParameterRefType | N/A | N/A   |
| **Return Value**     | N/A                                             | N/A                                | N/A | N/A   |

## Description

![](ElectricPowerSteering_RH850_FORD_T3T6_website/docs/ES104A_XcpIf_Impl/doc/mediax/media/image14.emf)

## NONTRUSTED_NtWrapS_Rte_Call_SetCalPageReq_Oper

|                      |                                                |                                    |     |       |
|--------|------------------------------|----------------------|-----|---------|
| **Function Name**    | NONTRUSTED_NtWrapS_Rte_Call_SetCalPageReq_Oper | Type                               | Min | Max   |
| **Arguments Passed** | FunctionIndex                                  | NonTrustedFunctionIndexType        | 0   | 65535 |
|                      | FunctionParams                                 | NonTrustedFunctionParameterRefType | N/A | N/A   |
| **Return Value**     | N/A                                            | N/A                                | N/A | N/A   |

## Description

![](ElectricPowerSteering_RH850_FORD_T3T6_website/docs/ES104A_XcpIf_Impl/doc/mediax/media/image15.emf)

## TRANSIENT FUNCTIONS 

*None*

# Unit Test Considerations

-   The value datatype of XcpDaqTimestampType can be uint8, uint16, or
    uint32 depending on the configuration of XCP. Unit testing shall
    test full ranges for all three types to ensure proper functionality.

# Known Limitations With Design

-   There are no protections in this design for executing on NULL_PTRs

# Appendix

*None*

{% endraw %}