---
title: System Modelling Part 2
description: System Modelling Part 2
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

# System Modelling Part 2

    Course Code: ELEE1149 
    
    Course Name: Software Engineering

    Credits: 15

    Module Leader: Seb Blair BEng(H) PGCAP MIET MIHEEM FHEA

---

## Topics Covered

- Behavioral models

- Model-driven engineering

---

## Behavioral models

- **Behavioral models** are models of the dynamic behavior of a system as it is executing. They show what happens or what is supposed to happen when a system responds to a stimulus from its environment. 

- You can think of these stimuli as being of two types:
  - **Data** Some data arrives that has to be processed by the system.
  - **Events** Some event happens that triggers system processing. Events may have associated data, although this is not always the case.

---


## Data-driven modeling

- Many business systems are data-processing systems that are primarily driven by data. They are controlled by the data input to the system, with relatively little external event processing. 

- Data-driven models show the sequence of actions involved in processing input data and generating an associated output. 

- They are particularly useful during the analysis of requirements as they can be used to show end-to-end processing in a system. 

- To show the sequence of processing in a system, we can use two types of diagrams, you can choose which one to use, you do not need both
  - **Activity diagrams** – also called Data Flow Diagrams (DFDs) – highlight the operations or activities
  - **Sequence diagrams** – highlight objects in a system


---

## An activity model of the insulin pump’s operation 

![bg right:50% 50% horizontal](../../figures/InsulinPump_act1.svg)
![bg right:50% 80% horizontal](../../figures/InsulinPump_act2.svg)

---

## DFDs vs. Sequence diagrams

- Sequence diagrams can be used to model interaction (we have seen that in the previous lecture), but if we draw this so that messages are only sent from left to right, then they show the sequential data processing in the system

- Sequence diagrams highlight objects in the systems, whereas DFDs highlight the operations or activities

- In practice, non-experts seem to find DFD more intuitive, but engineers prefer sequence diagrams

---

## Order Processing Sequence Diagram

![](../../figures/OrderProcessingSeqDia.svg)

<!--
https://kroki.io/mermaid/svg/eNptkLEOgyAURfd-xRttGn_AgaFputrEtItxIPC0pIgWwe-vQrFoZSDk3vsOcAd8W1QML4I2mrYHmBZlptNws5o96YB5XQuGOjhipAZ3TbdtjJSQU6456gyuQkqhkuMa5EwnuVOaEh9_UCn4FNjmz5Y3aKIBQryUQTn6GdEp6F4V3PsZAAltO6uM53Dcktb40kGHanVBEDMo6BheFJGWoai9wva9FN-vhcDcxuJMNFT8n_ZrJBL3-v4AfASNJg==
-->


---

## Event-driven modelling

- Real-time systems are often event-driven, with minimal data processing. For example, a landline phone switching system responds to events such as ‘receiver off hook’ by generating a dial tone. 

- **Event-driven modelling** shows how a system responds to external and internal events. 

- It assumes that a system has a finite number of states and that events (stimuli) may cause a transition from one state to another

- Event-driven modelling is used extensively when designing and documenting real time systems

---

## State machine models

- UML supports event-driven modelling using state diagrams which are based on state charts.

- State diagrams show system states and events that cause transitions from one state to another.  They do not show the flow of data within the system

- A **state machine** models the behaviour of the system in response to external and internal events.

- State machine models show system states as nodes and events as arcs between these nodes. When an event occurs, the system moves from one state to another.

- **State chart diagram**s are an integral part of the UML and are used to represent state machine models.

---

## A State machine model of a microwave

- This simple microwave model has a switch to select full or half power, a numeric keypad to input the cooking time, a start/stop button and an alphanumeric display

- The sequence of actions in using the microwave are as follows:
  - Select the power level (half or full power)
  - Input the cooking time using the numeric keypad
  - Press Start and the food is cooked for a given time

- For safety reasons, the oven should not operate when the door is opened, and, on completion of cooking, a buzzer is sounded. The oven has a simple display that is used to display various alerts and warning messages

---


## State Machine Model

- In UML state chart diagrams, rounded rectangles represent systems states

- They may include a brief description (following “do”) of the actions taken in that state

- The labelled arrows represent stimuli that force a transition from one state to another

- Start and end can be indicated using filled circles as in activity diagrams

---

## State Diagram of Microwave

![bg right:50% 70%](../../figures/microwaveState.svg)

<!-- 
https://www.plantuml.com/plantuml/uml/RL5DQy904BtlhtXuB4WrGWyUYaBRGoaYpR7sC6u65JO9P6Rr8FxtxYQkJT3JBEzZPjxiGfGQzQKpOianNYOJd0w5xetvUVh5-1MvalBKT0NZX6IO8_VMCXTSzDbecsEvhHjDHFPlcztRiWSsYKHod0tG0QEbjRxqBhxVgzhlzdWZfKtrLLUxJeuLbJm22Lp0fi7Qrj3xquk2e2mQq3PTc3jKtP2WN_6fxJuWrqrjMIJYGTBRmLpCTTr1rWywk1HqrWjwkm6UaTEHyStYdTuBqqNCWgiY_jCV
-->

---

## A State Machine Model 

- The problem with state-driven modelling is that the number of possible states increases rapidly

- For large systems, you need to hide details in the models

- To illustrate this, consider the Operation state from the model on the previous slide, and how it can be expanded on the slide below  

---


## Microwave Oven Operation

![h:500 center](../../figures/microwaveState1.svg.svg)

<!--
https://www.plantuml.com/plantuml/uml/RL5DQy904BtlhtXuB4WrGWyUYaBRGoaYpR7sC6u65JO9P6Rr8FxtxYQkJT3JBEzZPjxiGfGQzQKpOianNYOJd0w5xetvUVh5-1MvalBKT0NZX6IO8_VMCXTSzDbecsEvhHjDHFPlcztRiWSsYKHod0tG0QEbjRxqBhxVgzhlzdWZfKtrLLUxJeuLbJm22Lp0fi7Qrj3xquk2e2mQq3PTc3jKtP2WN_6fxJuWrqrjMIJYGTBRmLpCTTr1rWywk1HqrWjwkm6UaTEHyStYdTuBqqNCWgiY_jCV
-->
---

## States and stimuli for the microwave oven (1) 

<div align=center>

|State|Description|
|---|---|
|Waiting|The oven is waiting for input. The display shows the current time.|
|Half Power|The oven power is set to 300 watts. The display shows ‘Half power’.|
|Full Power|The oven power is set to 600 watts. The display shows ‘Full power’.|
|Set time|The cooking time is set to the user’s input value. The display shows the cooking time selected and is updated as the time is set.|
|Disabled|Oven operation is disabled for safety. Interior oven light is on. Display shows ‘Not ready’.|
|Enabled|Oven operation is enabled. Interior oven light is off. Display shows ‘Ready to cook’.|
|Operation|Oven in operation. Interior oven light is on. Display shows the timer countdown. On completion of cooking, the buzzer is sounded for five seconds. Oven light is on. Display shows ‘Cooking complete’ while buzzer is sounding.|

</div>

---

## States and stimuli for the microwave oven (2) 

<div align=center>

|State|Description|
|---|---|
|Half Power|The user has pressed the half-power button.|
|Full Power|The user has pressed the full-power button.|
|Time|The user has pressed one of the timer buttons.|
|Number|The user has pressed a numeric key.|
|Door open|The oven door switch is not closed.|
|Door Closed|The oven door switch is closed.|
|Start|The user has pressed the Start button.|
|Cancel|The user has pressed the Cancel button.|

</div>

---

## Model-driven engineering (MDE)

- **Model-driven engineering** is an approach to software development where models rather than programs are the principal outputs of the development process. 

- The programs that execute on a hardware/software platform are then generated automatically from the models. 

- Supporters of MDE argue that this raises the level of abstraction in software engineering so that engineers no longer have to be concerned with programming language details or the specifics of execution platforms.

- Questions: 
  - What are the benefits of model-driven engineering? 
  - What are the drawbacks of model-driven engineering? 

---

## Usage of model-driven engineering

- Model-driven engineering is still at an early stage of development, and it is unclear whether it will have a significant effect on software engineering practice. 

- **Pros**
  - Allows systems to be considered at higher levels of abstraction without concern for implementation details
  - Errors are reduced and the design and implementation process is speeded up
  - Generating code automatically means that it is cheaper to adapt systems to new platforms.
- **Cons**
  - Models for abstraction and not necessarily right for implementation.
  - Savings from generating code may be outweighed by the costs of developing translators for new platforms.