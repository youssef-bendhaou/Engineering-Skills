# Debugging

## 1. Definition

**Debugging** is the process of identifying, analyzing and fixing problems in a software or hardware system.

The objective is not only to fix the visible error, but to identify the **root cause** of the problem.

---

## 2. Why Is Debugging Important?

Engineering systems rarely work perfectly on the first attempt.

A problem can come from different sources:

* Hardware
* Software
* Configuration
* Communication
* Timing
* Memory
* Power supply
* External components

A good debugging approach helps avoid making random changes and allows problems to be solved systematically.

---

## 3. Debugging Mindset

A useful debugging mindset is:

> **Do not guess. Observe, formulate a hypothesis, test it and verify the result.**

Instead of immediately changing the code:

```text
Problem
   ↓
Observation
   ↓
Hypothesis
   ↓
Test
   ↓
Result
   ↓
Root Cause
   ↓
Fix
   ↓
Verification
```

---

## 4. Step-by-Step Debugging Process

### Step 1 — Reproduce the Problem

First, try to reproduce the problem.

Questions:

* Does the problem happen every time?
* Under what conditions does it happen?
* What is the expected behavior?
* What is the actual behavior?

---

### Step 2 — Observe

Collect information before changing anything.

Useful information can include:

* Error messages
* Logs
* Return values
* System behavior
* Sensor values
* Communication data
* Timing information
* CPU or memory usage

The goal is to understand **what is actually happening**.

---

### Step 3 — Form Hypotheses

Based on the observations, identify possible causes.

For example:

```text
Problem:
STM32 does not receive UART data.

Possible causes:

1. Wrong baud rate
2. Incorrect GPIO configuration
3. Wiring problem
4. UART peripheral not initialized
5. Interrupt configuration problem
6. Incorrect software logic
```

---

### Step 4 — Test One Hypothesis

Do not change several things at the same time.

Test one hypothesis at a time.

```text
Hypothesis
    ↓
Test
    ↓
Result
    ↓
Confirmed / Rejected
```

This makes it easier to identify the real cause.

---

### Step 5 — Identify the Root Cause

The **root cause** is the fundamental reason why the problem occurs.

For example:

```text
Symptom:
No UART data

        ↓

Observation:
STM32 is transmitting

        ↓

Test:
Check receiver configuration

        ↓

Finding:
Different baud rates

        ↓

Root Cause:
UART configuration mismatch
```

---

### Step 6 — Apply the Fix

Once the root cause is identified, apply the appropriate correction.

The fix should address the cause rather than only hiding the symptom.

---

### Step 7 — Verify

After applying the fix, verify that:

* The original problem is solved.
* The expected behavior is restored.
* No new problem has been introduced.
* The system still works under different conditions.

---

## 5. Debugging Tools

Different problems require different tools.

### Software

* Debugger
* GDB
* Logs
* `printf`
* Error codes
* Stack traces

### Embedded Systems

* UART
* JTAG / SWD
* Oscilloscope
* Logic analyzer
* Multimeter

### System-Level Debugging

* Process monitoring
* CPU usage
* Memory usage
* System logs
* Network analysis

The tool should be selected according to the problem.

---

## 6. Example — Embedded System

Consider a system where a microcontroller communicates with a peripheral.

```text
Microcontroller
      │
      │ Communication
      ↓
   Peripheral
```

The peripheral does not respond.

Instead of immediately modifying the software, check the system step by step:

```text
1. Power supply
       ↓
2. Physical connection
       ↓
3. Communication signals
       ↓
4. Protocol configuration
       ↓
5. Peripheral configuration
       ↓
6. Software
```

For example, an oscilloscope or logic analyzer can be used to determine whether the expected communication signals are actually present.

---

## 7. Example — QNX

Debugging is also important at the operating-system level.

For example, if a QNX process crashes:

```text
Application
     ↓
Process crashes
     ↓
Observe the behavior
     ↓
Check process status
     ↓
Check logs / error information
     ↓
Identify the cause
     ↓
Restart or fix the process
     ↓
Verify system behavior
```

This is particularly important in systems where different processes have different responsibilities.

---

## 8. Common Debugging Mistakes

### Changing too many things at once

If several changes are made simultaneously, it becomes difficult to know which change solved the problem.

### Assuming the first hypothesis is correct

The first hypothesis is not necessarily the root cause.

### Ignoring hardware

A software problem can sometimes be caused by wiring, power or electrical conditions.

### Not reproducing the problem

If the problem cannot be reproduced, it becomes harder to verify the solution.

### Not verifying the fix

A system that works once after a change is not necessarily fully fixed.

---

## 9. Debugging Principles

```text
Observe before changing
        ↓
Use evidence
        ↓
Form a hypothesis
        ↓
Test systematically
        ↓
Find the root cause
        ↓
Fix
        ↓
Verify
```

### Key principles

* Do not guess when you can measure.
* Change one variable at a time.
* Use evidence to support your hypothesis.
* Separate symptoms from root causes.
* Always verify the final solution.

---

## 10. Key Takeaways

* Debugging is a structured problem-solving process.
* The goal is to find the root cause, not only the visible symptom.
* Observation and measurement are essential.
* Different problems require different debugging tools.
* A good debugging process reduces unnecessary trial and error.

> **Good debugging is not about finding the answer quickly. It is about finding the correct cause systematically.**
