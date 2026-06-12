# Day 02 Summary

## Date

2026-06-10

---

# Learning Context

This repository follows an AI-assisted learning approach.

AI is used as a support system for:

* Concept clarification
* Doubt resolution
* Guided questioning
* Knowledge verification
* Learning reinforcement

The concepts learned, doubts asked, and discussions documented below represent the actual learning process followed during this session.

---

# Concepts Learned

## Concept 01 - Strings and the Class Scanner (Session 1)

### What I Learned

Scanner reads all input as text first. Methods such as `nextInt()` and `nextDouble()` convert the text into numeric values. I learned the difference between `next()` and `nextLine()`, how Scanner extracts tokens, and how delimiters separate tokens.

I also learned that Scanner can process both keyboard input and String objects using the same abstraction.

### Related Artifacts

* Transcript Discussion
* AI Verification

### Key Understanding

Scanner is an abstraction over parsing. It handles tokenization, delimiter processing, and type conversion so that developers do not repeatedly implement those operations themselves.

---

## Concept 02 - Processing a String Using Scanner (Session 1)

### What I Learned

Scanner can be constructed using a String instead of `System.in`.

```java
Scanner scan = new Scanner(data);
```

This allows the same parsing behavior to be applied to existing String data.

### Related Artifacts

* Transcript Discussion
* AI Verification

### Key Understanding

The source of data can change while the Scanner interface remains the same. This is an example of abstraction and reusable API design.

---

## Concept 03 - The Class LocalTime (Session 1)

### What I Learned

I learned how to create LocalTime objects using:

```java
LocalTime.now();
```

I learned about:

* Import statements
* Packages
* `toString()`
* `getHour()`
* `getMinute()`
* `getSecond()`
* `equals()`
* `compareTo()`
* `isBefore()`
* `isAfter()`

### Related Artifacts

* Transcript Discussion
* AI Verification

### Key Understanding

A LocalTime object stores state and provides behavior. It represents a snapshot of time and contains methods to display and compare time values.

---

## Concept 04 - The Class BigDecimal (Session 2)

### What I Learned

BigDecimal exists to perform precise decimal arithmetic and avoid errors caused by binary floating-point representation.

I learned:

* Why doubles are unsuitable for monetary calculations
* Why BigDecimal values should be created from Strings
* `nextBigDecimal()`
* `add()`
* `subtract()`
* `multiply()`
* `divide()`
* Immutability
* Differences between `equals()` and `compareTo()`

### Related Artifacts

* Transcript Discussion
* ProblemSolved.java
* AI Verification

### Key Understanding

Correct business logic can still produce incorrect results if the underlying data representation is wrong. Choosing the correct data type is an engineering decision.

---

## Concept 05 - More Apples by the Box Using BigDecimal (Session 2)

### What I Learned

I revisited the apples problem using BigDecimal arithmetic instead of double primitives.

The business logic remained unchanged:

```text
Cost of apples individually
-
Cost of box
=
Savings
```

Only the numeric representation changed.

### Related Artifacts

* ProblemSolved.java
* Transcript Discussion

### Key Understanding

Many software bugs originate from representation errors rather than incorrect formulas or business logic.

---

# Doubts Asked To AI

## Doubt 01

### My Question

If `nextLine()` reads a line, how can multiple lines be read?

### AI Explanation

Each call to `nextLine()` reads one line only. Multiple calls are needed to read multiple lines. Loops can be used when the number of lines is unknown.

### Final Understanding

`nextLine()` reads until the next Enter key. One call corresponds to one line.

---

## Doubt 02

### My Question

Why can Scanner process a String object when the data is already stored in a variable?

### AI Explanation

Scanner provides tokenization, delimiter handling, and type conversion that would otherwise need to be implemented manually.

### Final Understanding

Scanner exists as an abstraction layer over parsing operations regardless of where the data originates.

---

# Questions AI Asked Me

## Question 01

### AI Question

Why might engineers choose `|` instead of `,` as a delimiter in structured data?

### My Answer

Commas may naturally appear inside values such as prices or text. The pipe character is less likely to appear in the actual data.

### My Reasoning

Using commas can cause incorrect token separation when the data itself contains commas.

### Final Outcome

* Correct

### Correct Understanding

Delimiters should be chosen so they rarely appear inside valid data values.

---

## Question 02

### AI Question

Why might Java provide `isBefore()` and `isAfter()` when `compareTo()` already exists?

### My Answer

`compareTo()` provides positive and negative values, but `isBefore()` and `isAfter()` communicate intent more clearly and improve readability.

### My Reasoning

Developers can understand the purpose immediately without remembering comparison rules.

### Final Outcome

* Correct

### Correct Understanding

APIs often provide higher-level methods to improve readability, maintenance, and code intent.

---

## Question 03

### AI Question

Why would banks insist on BigDecimal even if each transaction error is extremely small?

### My Answer

Tiny errors become significant when repeated across many transactions and many users.

### My Reasoning

Accumulated rounding errors can eventually become financially meaningful.

### Final Outcome

* Correct

### Correct Understanding

Financial systems prioritize correctness because small errors can compound into large discrepancies.

---

# Learning Artifacts

## Artifact 01

Type:

Discussion

Title:

Scanner as an Abstraction

Purpose:

Understanding tokenization, delimiter handling, and type conversion.

Concepts Used:

* Scanner
* Tokens
* Delimiters
* Parsing

---

## Artifact 02

Type:

Discussion

Title:

LocalTime and Time Comparison

Purpose:

Understanding object behavior, snapshots of time, and comparison methods.

Concepts Used:

* LocalTime
* compareTo
* isBefore
* isAfter

---

## Artifact 03

Type:

Program

File:

ProblemSolved.java

Purpose:

Demonstrates precise monetary calculations using BigDecimal.

Concepts Used:

* BigDecimal
* multiply
* subtract
* nextBigDecimal

---

# Engineering Intuition Developed

## Insight 01

Libraries often exist to reduce programmer complexity rather than machine complexity. Scanner, LocalTime, and BigDecimal all encapsulate recurring work behind reusable abstractions.

---

## Insight 02

Choosing the correct data representation is often more important than changing the business logic. Correct formulas can still produce incorrect outcomes when the representation is inappropriate.

---

# Learning Insights

## Most Important Concept Today

BigDecimal

Reason:

It demonstrated how representation choices directly affect correctness in real-world systems such as banking and finance.

---

## Most Valuable Doubt

Why Scanner can process a String even when the data is already stored.

Reason:

The discussion revealed that Scanner is fundamentally a parsing abstraction rather than an input-only utility.

---

## Most Valuable Question Asked By AI

Why would banks insist on BigDecimal despite tiny transaction errors?

Reason:

It connected language features to large-scale real-world systems and financial correctness.

---

## Concepts Requiring Revision

* BigDecimal immutability
* BigDecimal equals vs compareTo behavior

---

# End of Day Reflection

Today reinforced the importance of abstraction and data representation.

Scanner helped me understand parsing and tokenization beyond keyboard input. LocalTime showed how objects combine state and behavior while providing meaningful APIs. BigDecimal was the strongest concept because it demonstrated how representation errors can affect correctness even when the logic is mathematically correct.

The session was lighter than planned because of environmental issues affecting focus, but the concepts learned were valuable and connected strongly to real-world software engineering concerns.

---

# Navigation

## Concepts

* Strings and the Class Scanner
* Processing a String Using Scanner
* The Class LocalTime
* The Class BigDecimal
* More Apples by the Box Using BigDecimal

## Learning Artifacts

* ProblemSolved.java
* Scanner Discussion
* LocalTime Discussion
* BigDecimal Discussion

## Doubts Discussed

* Reading multiple lines using Scanner
* Why Scanner can process String objects

## AI Verification Questions

* Delimiter selection and data contracts
* Time comparison readability
* BigDecimal and financial correctness
