---
title: Requirements Engineering
description: Requirements Engineering
class: gaia
_class:
  - lead
  - invert
style: |
    #img-right{
      float: right;
    }
    img[alt~="center"] {
      display: block;
      margin: 0 auto;
    }
    table {
        border-collapse: collapse;
        font-size: 30px;
      }
    table, th,tr, td {
         border: none!important; 
          vertical-align: middle;
      }
size: 16:9
paginate: true
_paginate: false
marp: true
math: true
---

# Requirements Engineering

    Course Code: ELEE1149 
    
    Course Name: Software Engineering

    Credits: 15

    Module Leader: Seb Blair BEng(H) PGCAP MIET MIHEEM FHEA

---

## Topics Covered

<p></p>
<p></p>
<p></p>
<p></p>

- Functional and non-functional requirements
- Requirements engineering processes

<p></p>
<p></p>
<p></p>
<p></p>

Question: What is a requirement in software engineering?

---

## What is a requirement?

- It may range from a high-level abstract statement of a service or of a system constraint to a detailed mathematical functional specification.
  
- This is inevitable as requirements may serve a dual function
  - May be the basis for a bid for a contract - therefore must be open to interpretation;
  - May be the basis for the contract itself - therefore must be defined in detail;
  - Both these statements may be called requirements.
  
- Requirements engineering
  - The process of establishing the services that a customer requires from a system and the constraints under which it operates and is developed.

--- 

## Types of Requirements

- User (customer) requirements
  - Statements in natural language plus diagrams of the services the system provides and its operational constraints. Written for customers.
  
- System requirements
  - A structured document setting out detailed descriptions of the system’s functions, services and operational constraints. Defines what should be implemented so may be part of a contract between client and contractor.

---

## User and System Requirements Example

**User Requirements Definition**

  **1.** The Mentcare system shall generate monthly reports showing the cost of drugs prescribed by each clinic during that month.

**System Requirements Specification**
   
   **1.1** On the last working day of each month, a summary of the drugs prescribed, their cost and the prescribing clinis shall be generated.
  **1.2** The system shall geneate the report for emailing after 1730 for each clinic on the last working day of the month.
  **1.3** A report shall be created for each clinic and shall list the individual drug names, the total number of prescriptions, the number of doses prescribed and the total cost of the prescribed drugs
...

---

## Readers of different types of requirements specification

![h:500 center](../../figures/usersystemrequirements.png)

---

## System Stakeholders

- Any person or organization who is affected by the system in some way and so who has a legitimate interest
- Stakeholder types
  - End users
  - System managers
  - System owners
  - External stakeholders

Question: Who are the stakeholders in the Mentcare system?


---

## Stakeholders in the Mentcare system

- Patients whose information is recorded in the system.
- Doctors who are responsible for assessing and treating patients.
- Nurses who coordinate the consultations with doctors and administer some treatments.
- Medical receptionists who manage patients’ appointments.
- IT staff who are responsible for installing and maintaining the system.
- A medical ethics manager who must ensure that the system meets current ethical guidelines for patient care.
- Health care managers who obtain management information from the system.
- Medical records staff who are responsible for ensuring that system information can be maintained and preserved, and that record keeping procedures have been properly implemented.

---

## Agile methods and requirements

- Many agile methods argue that producing detailed system requirements is a waste of time as requirements change so quickly. - Therefore, the requirements document is always out of date.

- Agile methods usually use incremental requirements engineering and may express requirements as ‘user stories’ (discussed last week).

- This is practical for business systems but problematic for systems that require pre-delivery analysis (e.g. critical systems) or systems developed by several teams.

---

## Functional and non-Fucntional Requirements

<details>
<summary>What do you think we mean by functional and non-functional requirements?</summary> 
<p> </p>

- Functional requirements
  - Statements of services the system should provide, how the system should react to particular inputs and how the system should behave in particular situations.
  - May state what the system should not do.
- Non-functional requirements
  - Constraints on the services or functions offered by the system such as timing constraints, constraints on the development process, standards, etc.
  - Often applied to the system as a whole rather than individual features or services.
  
</details>

---

## Functional Requirements

- Describe functionality or system services.
- Depend on the type of software, expected users and the type of system where the software is used.
- Functional user requirements may be high-level statements of what the system should do.
- Functional system requirements should describe the system services in detail.



---

## Mentacare system: Functional Requirements

<details>
<summary>What are the functional requirements for Mentcare system?</summary>

<p></p>

- A user shall be able to search the appointments lists for all clinics.
- The system shall generate each day, for each clinic, a list of patients who are expected to attend appointments that day. 
- Each staff member using the system shall be uniquely identified by his or her 8-digit employee number. 

</details>

---

## Requirements Imprecision

- Problems arise when functional requirements are not precisely stated.
- Ambiguous requirements may be interpreted in different ways by developers and users.
- Consider the term ‘search’ in the first requirement on the previous slide
  - User intention – search for a patient name across all appointments in all clinics;
  - Developer interpretation – search for a patient name in an individual clinic. User chooses clinic then search.

---

## Requirements completeness and consistency

- In principle, requirements should be both complete and consistent.
  
- Complete
  - They should include descriptions of all facilities required.

- Consistent
  - There should be no conflicts or contradictions in the descriptions of the system facilities.

- In practice, because of system and environmental complexity, it is not always possible to produce a complete and consistent requirements document.

---

## Non-functional Requirements

- Define system properties and constraints e.g. reliability, response time and storage requirements. Constraints are I/O device capability, system representations, etc.

- Non-functional requirements can also be specified referring to  a particular IDE, programming language or development method.

- Non-functional requirements may be more critical than functional requirements. If these are not met, the system may be useless.

---

## Types of Non-functional Requirement

![bg right:65% 80%](../../figures/nonfunctionalgraph.svg)

---

## Non-functional requirements implementation

- Non-functional requirements may affect the overall architecture of a system rather than the individual components. 
  - For example, to ensure that performance requirements are met, you may have to organize the system to minimize communications between components.

- A single non-functional requirement, such as a security requirement, may generate several related functional requirements that define system services that are required. 
  - It may also generate requirements that restrict existing requirements. 

---

## Non-functional Classifications

- Product requirements
  - Requirements which specify that the delivered product must behave in a particular way e.g. execution speed, reliability, etc

- Organisational requirements
  - Requirements which are a consequence of organisational policies and procedures e.g. process standards used, implementation requirements, etc.

- External requirements
  - Requirements which arise from factors which are external to the system and its development process e.g. interoperability requirements, legislative requirements, etc.

---

## Examples of non-functional requirements in the Mentcare system


**Product requirement**
The Mentcare system shall be available to all clinics during normal working hours (Mon–Fri, 0830–17.30). Downtime within normal working hours shall not exceed five seconds in any one day.

**Organizational requirement**
Users of the Mentcare system shall authenticate themselves using their health authority identity card.

**External requirement**
The system shall implement patient privacy provisions as set out in HStan-03-2022-priv. 

---

## Goals and Requirements

- Non-functional requirements may be very difficult to state precisely and imprecise requirements may be difficult to verify. 

- Goal
  - A general intention of the user such as ease of use. They are usually quite general and vague (not easily measurable)

- Verifiable non-functional requirement
  - A statement using some measure that can be objectively tested.

- Goals are helpful to developers as they convey the intentions of the system users.

---

## Usability Requirements
- The system should be easy to use by medical staff and should be organized in such a way that user errors are minimized. (Goal, too general)

- Medical staff shall be able to use all the system functions after four hours of training. After this training, the average number of errors made by experienced users shall not exceed two per hour of system use. (Testable non-functional requirement, more specific and measurable)

---

## Metrics for specifying non-functional requirements

<table align=center >
    <tr>
        <td>
        Property
        </td>
        <td>
        Measure
        </td>
    </tr>
    <tr>
        <td>
        Speed
        </td>
        <td>
            <ul>
                <li> Processed transactions/second 
                <li> User/event response time 
                <li> screen refresh time
            </ul>
        </td>
    </tr>
     <tr>
        <td>
        Size
        </td>
        <td>
            <ul>
                <li> MBytes
                <li> Amount of RAM 
            </ul>
        </td>
    </tr>
    <tr>
        <td>
        Ease of Use
        </td>
        <td>
            <ul>
                <li> Training Time
                <li> Number of frames per second 
            </ul>
        </td>
    </tr>
    <tr>
        <td>
        Reliability
        </td>
        <td>
            <ul>
                <li> Mean time to failure
                <li>Probability of unavailability
                <li>Rate of failure occurrence
                <li>Availability
            </ul>
        </td>
    </tr>
    <tr>
        <td>
        Robustness
        </td>
        <td>
            <ul>
                <li> Time to restart after failure
                <li>Percentage of events causing failure
                <li>Probability of data corruption on failure
            </ul>
        </td>
    </tr>
    <tr>
        <td>
        Portability
        </td>
        <td>
            <ul>
                <li> Percentage of target dependent statements
                <li>Number of target systems
            </ul>
        </td>
    </tr>
</table>
