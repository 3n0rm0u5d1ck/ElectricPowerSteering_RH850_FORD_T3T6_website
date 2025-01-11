---
layout: default
title: DampgPahSum_MDD
nav_order: 2
parent: Component Implementation
---
{% raw %}
**Module Design Document**

**For**

**DampgPahSum**

**July 07, 2015**

**Prepared For:**

**Software Engineering**

**Nexteer Automotive,**

**Saginaw, MI, USA**

**Prepared By:**

**Nick Saxton,**

**Nexteer Automotive,**

**<u>Saginaw, MI, USAChange</u>** History

|                 |            |             |             |
|-----------------|------------|-------------|-------------|
| **Description** | **Author** | **Version** | **Date**    |
| Initial Version | N. Saxton  | 1.00.00     | 07-Jul-2015 |

**<u>Table of Contents</u>**

[1 DampgPahSum & High-Level Description
4](#dampgpahsum-high-level-description)

[2 Design details of software module
5](#design-details-of-software-module)

[2.1 Graphical representation of DampgPahSum
5](#graphical-representation-of-dampgpahsum)

[2.2 Data Flow Diagram 5](#data-flow-diagram)

[2.2.1 Component level DFD 5](#component-level-dfd)

[2.2.2 Function level DFD 5](#function-level-dfd)

[3 Constant Data Dictionary 6](#constant-data-dictionary)

[3.1 Program (fixed) Constants 6](#program-fixed-constants)

[3.1.1 Embedded Constants 6](#embedded-constants)

[4 Software Component Implementation
7](#software-component-implementation)

[4.1.1 Sub-Module Functions 7](#sub-module-functions)

[4.1.2 Interrupt Service Routines 7](#interrupt-service-routines)

[4.1.3 Server Runnable Functions 7](#server-runnable-functions)

[4.1.4 Module Internal (Local) Functions
7](#module-internal-local-functions)

[4.1.5 Transition Functions 7](#transition-functions)

[5 Known Limitations with Design 8](#known-limitations-with-design)

[6 UNIT TEST CONSIDERATION 9](#unit-test-consideration)

[Appendix A Abbreviations and Acronyms 10](#abbreviations-and-acronyms)

[Appendix B Glossary 11](#glossary)

[Appendix C References 13](#references)

# DampgPahSum & High-Level Description

This function calculates the damping command by taking the difference of
the base damping and inertia compensation and is intended for use in
programs that do not require the extra features of SF035A.

# Design details of software module

## Graphical representation of DampgPahSum

<img
src="ElectricPowerSteering_RH850_FORD_T3T6_website/docs/SF035B_DampgPahSum_Impl/doc/mediax/media/image1.png"
style="width:2.96667in;height:1.05833in" />

## Data Flow Diagram

### Component level DFD

N/A

### Function level DFD

N/A

# Constant Data Dictionary

## Program (fixed) Constants

### Embedded Constants

#### Local Constants

None

# Software Component Implementation

### Sub-Module Functions

#### Initialization sub-module {\_Init()}

None

#### Periodic sub-module {\_Per()}

##### DampgPahSumPer1

###### Design Rationale

Refer to FDD

###### Store module inputs to local copies

Refer to FDD

###### (Processing of function)……

Refer to FDD

###### Store local copy of outputs into module outputs

Refer FDD

### Interrupt Service Routines

None

### Server Runnable Functions

None

### Module Internal (Local) Functions

None

### Transition Functions

None

# Known Limitations with Design

None

# UNIT TEST CONSIDERATION

None

####### Abbreviations and Acronyms

None

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
|-------|-------------------------------------------------|-----------------|
| 1           | AUTOSAR Specification of Memory Mapping (Link:[AUTOSAR_SWS_MemoryMapping.pdf](http://www.autosar.org/download/R4.0/AUTOSAR_SWS_MemoryMapping.pdf))                    | v1.3.0 R4.0 Rev 2              |
| 2           | MDD Guideline                                                                                                                                                         | EA4 01.00.00                   |
| 3           | [Software Naming Conventions.doc](http://misagweb01.nexteer.com/eRoomReq/Files/erooms8/NextGeneration/0_fc55f/Software%20Naming%20Conventions%2003x(In%20Work).doc)   | 2.0                            |
| 4           | [Software Design and Coding Standards.doc](http://eroom1.nexteer.com/eRoomReq/Files/erooms8/NextGeneration/0_1a67a9/Software%20Design%20and%20Coding%20Standards.doc) | 2.1                            |
| 5           | FDD – SF035B Damping Path Summation                                                                                                                                   | See Synergy subproject version |

{% endraw %}