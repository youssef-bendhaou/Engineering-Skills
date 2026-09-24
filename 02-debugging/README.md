# Debugging

## What is it?

Debugging is the process of **finding and fixing a problem** in a software or hardware system.

The goal is to find the **root cause**, not only fix the visible error.

## Basic Process

```text
Problem
   ↓
Observe
   ↓
Find possible causes
   ↓
Test
   ↓
Find the root cause
   ↓
Fix
   ↓
Verify
```

## Example

Problem:

> STM32 does not receive UART data.

Possible causes:

* Wrong baud rate
* Wrong GPIO configuration
* Wiring problem
* UART configuration problem
* Software problem

Instead of changing everything, test each possibility step by step.

## Useful Tools

* Debugger
* UART logs
* Multimeter
* Oscilloscope
* Logic analyzer
* GDB

## Key Idea

> **Do not guess. Observe, test and verify.**
