# Information Filtering

## 1. Definition

**Information Filtering** is the ability to identify, select and verify the information that is relevant to a specific technical problem.

Engineers often have access to a large amount of information:

* Datasheets
* Reference manuals
* Application notes
* Technical documentation
* GitHub repositories
* Forums
* Error messages
* Logs
* Tutorials
* Technical articles

The challenge is not only finding information, but determining **which information is useful and reliable**.

---

## 2. Why Is It Important?

When solving an engineering problem, searching without a clear method can lead to:

* Too much irrelevant information
* Conflicting answers
* Outdated information
* Incorrect assumptions
* Time wasted on unnecessary research

Information Filtering helps reduce this problem by focusing the search on the information that can actually help solve the problem.

---

## 3. The Information Filtering Process

A simple approach is:

```text id="5kt2e7"
Technical Problem
       ↓
Define What I Need
       ↓
Identify Keywords
       ↓
Search Information
       ↓
Filter Results
       ↓
Check Reliability
       ↓
Compare Information
       ↓
Apply
       ↓
Verify
```

---

## 4. Step 1 — Define the Problem

Before searching, clearly describe the problem.

Bad approach:

> "QNX problem"

Better approach:

> "QNX process terminates unexpectedly after receiving a specific command."

A precise problem leads to a more precise search.

---

## 5. Step 2 — Identify Keywords

Extract the important technical terms from the problem.

For example:

```text id="q6ksn6"
Problem:
QNX process terminates unexpectedly

Keywords:

QNX
process
termination
crash
SIGSEGV
process monitoring
restart
```

These keywords can then be used to search technical documentation.

---

## 6. Step 3 — Search Multiple Sources

Different sources can provide different types of information.

### Official Documentation

Useful for:

* Technical specifications
* APIs
* Configuration
* Supported features
* Official behavior

### Datasheets / Reference Manuals

Useful for:

* Hardware specifications
* Registers
* Electrical characteristics
* Timing
* Peripheral configuration

### GitHub

Useful for:

* Practical examples
* Source code
* Project structures
* Implementation ideas

### Forums / Communities

Useful for:

* Real-world problems
* Debugging experiences
* Unusual errors

However, information from forums should be verified before being used as a technical reference.

---

## 7. Step 4 — Filter the Results

Not every search result is useful.

A result can be evaluated using questions such as:

```text id="mlkr2v"
Is it related to my problem?
        ↓
Is it technically relevant?
        ↓
Is it recent enough?
        ↓
Is the source reliable?
        ↓
Does it match my hardware/software version?
        ↓
Can I verify the information?
```

---

## 8. Step 5 — Check the Source

The reliability of information depends on its source.

A useful hierarchy can be:

```text id="gnzwfv"
Manufacturer Documentation
        ↓
Official Technical Documentation
        ↓
Application Notes
        ↓
Official Examples
        ↓
Well-documented Projects
        ↓
Technical Communities
        ↓
Random Online Content
```

This does not mean that community information is always wrong.

It means that **important technical information should be verified using reliable sources**.

---

## 9. Step 6 — Check the Context

Technical information can be correct but still not apply to your situation.

For example:

```text id="1p75zj"
Information found online

       ↓

Different MCU?
Different QNX version?
Different hardware?
Different compiler?
Different configuration?
Different protocol version?

       ↓

May not apply directly
```

Before using information, check whether the context matches your system.

---

## 10. Example — Debugging a QNX Problem

Imagine that a QNX process crashes.

A search might return:

```text id="p0x3hz"
Result 1 → QNX official documentation
Result 2 → GitHub project
Result 3 → Stack Overflow
Result 4 → Random blog
Result 5 → Old forum post
```

Instead of using the first result, evaluate them.

### Official documentation

Can explain the expected behavior of the QNX mechanism.

### GitHub

Can provide a practical implementation example.

### Stack Overflow

Can provide useful debugging experience.

### Random blog

May contain useful information, but should be verified.

### Old forum post

May describe an older version or configuration.

The objective is to **combine useful information while verifying it against reliable documentation**.

---

## 11. Example — Datasheet Research

Suppose I need to configure an STM32 peripheral.

I may find information in:

```text id="85cxbl"
Google Search
     ↓
STM32 Datasheet
     ↓
Reference Manual
     ↓
Application Note
     ↓
GitHub Example
     ↓
Forum Discussion
```

The information should then be filtered and compared.

For example:

```text id="q6z7yt"
Question:
Which pins can be used?

       ↓

Datasheet
       +
Reference Manual
       +
Board configuration

       ↓

Verified configuration
```

---

## 12. Search vs Information Filtering

These two skills are different.

### Searching

Finding information.

```text
"What is this error?"
```

### Filtering

Determining which information is useful.

```text
"Which explanation applies to my system?"
```

### Engineering Approach

```text id="5zh1b0"
Search
  ↓
Collect
  ↓
Filter
  ↓
Verify
  ↓
Understand
  ↓
Apply
```

---

## 13. Common Mistakes

### Using the first search result

The first result is not necessarily the best technical source.

### Copying code without understanding it

A code example may work in a different environment but fail in your system.

### Ignoring software or hardware versions

An API or configuration can change between versions.

### Trusting a single source

Important information should be cross-checked when possible.

### Searching without defining the problem

A vague problem usually produces a large amount of irrelevant information.

---

## 14. Practical Checklist

Before using information found online, ask:

```text
[ ] What exactly am I trying to solve?
[ ] What information do I need?
[ ] Is the source reliable?
[ ] Is the information relevant to my system?
[ ] Does the hardware/software version match?
[ ] Can I verify the information?
[ ] Do I understand the information?
[ ] Can I test it?
```

---

## 15. Key Takeaways

* Define the problem before searching.
* Use precise technical keywords.
* Do not assume that every search result is relevant.
* Prefer reliable technical sources.
* Check hardware and software versions.
* Compare information when necessary.
* Understand information before applying it.
* Verify the final result experimentally.

> **Finding information is easy. Finding the right information is an engineering skill.**
