# Big Picture Thinking

## 1. Definition

**Big Picture Thinking** is the ability to understand a system as a whole instead of focusing only on one component.

An engineer should understand how the different parts of a system interact, communicate and depend on each other.

The goal is to answer questions such as:

* What is the purpose of the system?
* What are its main components?
* How do the components interact?
* What happens if one component fails?
* How can a change affect the rest of the system?

---

## 2. Why Is It Important?

Modern engineering systems are composed of many interconnected components.

Focusing only on one component can lead to solving a local problem while creating another problem somewhere else.

Big Picture Thinking helps an engineer to:

* Understand system architecture
* Identify dependencies
* Understand interfaces between components
* Analyze the impact of changes
* Find problems at the system level
* Make better technical decisions

---

## 3. From Component to System

An engineer can look at a system at different levels.

```text
Component
    ↓
Subsystem
    ↓
Complete System
    ↓
Final Product
```

For example, in an embedded system:

```text
Sensor
   ↓
Microcontroller
   ↓
Communication
   ↓
Software
   ↓
Actuator
   ↓
Final System
```

Instead of asking only:

> "How does this sensor work?"

we should also ask:

> "What role does this sensor play in the complete system?"

---

## 4. Example — Automotive Embedded System

Consider a simplified automotive system:

```text
        Sensors
           │
           ↓
        ECU / SoC
           │
     ┌─────┴─────┐
     ↓           ↓
   CAN Bus    Software
     │           │
     └─────┬─────┘
           ↓
       Actuators
```

Each component has a specific role, but the complete system depends on the interaction between them.

For example, a problem with a sensor can appear as a software problem because incorrect sensor data is transmitted to the ECU.

Therefore, understanding the complete data flow is important before trying to solve the problem.

---

## 5. A Simple Method

When approaching an unfamiliar system, I can use the following method:

```text
1. Understand the objective
          ↓
2. Identify the main components
          ↓
3. Understand the interfaces
          ↓
4. Understand the data flow
          ↓
5. Identify dependencies
          ↓
6. Identify possible failure points
          ↓
7. Analyze the system as a whole
```

### Questions to ask

**Objective**

* What is the system supposed to do?

**Components**

* What are the main hardware and software elements?

**Interfaces**

* How do they communicate?

**Data Flow**

* Where does the information come from?
* Where does it go?

**Dependencies**

* Which components depend on each other?

**Failures**

* What happens if one component stops working?

---

## 6. Engineering Example

Suppose an STM32 is not receiving data from a sensor.

A local approach would be:

```text
"Check the STM32 code."
```

A Big Picture approach would be:

```text
Sensor
  ↓
Physical Connection
  ↓
Communication Bus
  ↓
STM32 Peripheral
  ↓
Driver
  ↓
Application
```

The problem could come from any of these levels.

Therefore, before changing the code, the engineer should understand the complete communication chain.

---

## 7. Big Picture vs. Detailed Thinking

Big Picture Thinking does not mean ignoring technical details.

Good engineering requires both:

```text
        BIG PICTURE
             ↓
     Understand the system
             ↓
      Identify the problem
             ↓
      Focus on the details
             ↓
       Find the root cause
             ↓
      Return to the system
             ↓
       Verify the solution
```

The engineer moves between **system-level understanding** and **component-level analysis**.

---

## 8. Key Takeaways

* Understand the system before focusing on a component.
* Identify how components interact.
* Follow the data flow.
* Understand dependencies.
* Consider the impact of changes.
* Combine system-level thinking with technical details.

> **A component cannot always be understood correctly without understanding the system around it.**
