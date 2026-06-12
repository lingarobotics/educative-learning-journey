# Day 03 Summary

## Date

2026-06-11

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

## Concept 01 - DecimalFormat and Output Formatting (Session 1)

### What I Learned

The `DecimalFormat` class allows precise control over how numeric values are displayed. Patterns can determine decimal places, percentages, currency symbols, leading zeros, and optional digits.

### Related Artifacts

* Transcript Discussion
* AI Verification

### Key Understanding

Formatting changes presentation only. The underlying numeric value remains unchanged.

---

## Concept 02 - ParseInt and Number Bases (Session 2)

### What I Learned

`Integer.parseInt()` converts a string into an integer. The second parameter can specify the number base (radix).

Examples:

* Base 10 → normal decimal interpretation
* Base 16 → hexadecimal interpretation

### Related Artifacts

* Transcript Discussion
* AI Verification

### Key Understanding

The radix determines how Java interprets the digits contained in the string.

---

## Concept 03 - Escape Sequences and Special Characters (Session 2)

### What I Learned

Escape sequences allow special characters to be represented inside strings.

Examples:

* `\"`
* `\\`
* `\t`
* `\n`

### Related Artifacts

* Challenge2
* Transcript Discussion

### Key Understanding

A backslash begins an escape sequence, allowing characters that otherwise have special meaning to appear inside string literals.

---

## Concept 04 - Scanner Delimiters and "\s" (Session 2)

### What I Learned

Scanner delimiters can be specified using regular expressions. `\\s` represents whitespace characters.

### Related Artifacts

* Challenge3 Discussion

### Key Understanding

Because Java treats `\` as an escape character, `\\` is required to represent a literal backslash inside a string.

---

## Concept 05 - Classes as Blueprints and Objects as Instances (Session 3)

### What I Learned

A class acts as a blueprint that describes data and behavior. Objects are created at runtime from that blueprint using the `new` operator.

### Related Artifacts

* Greeter Class Discussion
* Transcript Discussion

### Key Understanding

Classes define structure, while objects contain actual allocated memory and data.

---

## Concept 06 - Instance Variables and Object State (Session 3)

### What I Learned

Instance variables belong to objects. Every object receives its own copy of instance variables when instantiated.

### Related Artifacts

* Greeter Discussion
* AI Verification

### Key Understanding

Three objects mean three separate sets of instance variables.

---

## Concept 07 - Constructors (Session 3)

### What I Learned

Constructors initialize newly created objects. Constructors can be default or parameterized and may contain additional logic beyond simple assignments.

### Related Artifacts

* Greeter Constructor Discussion

### Key Understanding

Object memory allocation is performed by `new`, while constructors initialize that allocated memory.

---

## Concept 08 - Parameters vs Arguments (Session 3)

### What I Learned

Parameters are variables declared in method or constructor headers. Arguments are values supplied during method invocation.

### Related Artifacts

* Constructor Discussion
* AI Verification

### Key Understanding

Parameters receive arguments and behave as local variables during execution.

---

## Concept 09 - Encapsulation, Getters, and Setters (Session 3)

### What I Learned

Getters provide controlled read access. Setters provide controlled write access. Encapsulation protects object consistency and validity.

### Related Artifacts

* Backend Workflow Discussion
* AI Verification

### Key Understanding

Getters and setters are not merely syntax; they represent controlled access to object state.

---

## Concept 10 - Local Variables (Session 3)

### What I Learned

Local variables exist only while a method executes. They are temporary working variables and disappear when the method ends.

### Related Artifacts

* changeGreeting Discussion

### Key Understanding

Instance variables belong to objects, while local variables belong to method execution.

---

## Concept 11 - Designing Classes (Session 3)

### What I Learned

Class design begins with identifying data fields, behaviors, method signatures, and usage patterns before implementation.

### Related Artifacts

* Name Class Design Discussion

### Key Understanding

Professional design focuses on behavior and interface before implementation details.

---

## Concept 12 - Implementing Classes (Session 3)

### What I Learned

Methods can call other methods within the same class to avoid duplication and improve maintainability.

### Related Artifacts

* Name Class Implementation Discussion

### Key Understanding

Logic should be centralized and reused rather than duplicated.

---

## Concept 13 - Passing Arguments (Session 3)

### What I Learned

Java always uses call-by-value.

* Primitive types pass copies of values.
* Objects pass copies of references.

### Related Artifacts

* Name Class Discussion
* AI Verification

### Key Understanding

Methods can modify an object's state through a copied reference but cannot replace the caller's reference variable.

---

## Concept 14 - Class Design Tradeoffs (Session 4)

### What I Learned

Different implementations can provide identical behavior while using different amounts of memory and computation.

### Related Artifacts

* Square
* Square2
* Square3

### Key Understanding

Software engineering often involves choosing between memory usage and computation cost.

---

# Doubts Asked To AI

## Doubt 01

### My Question

Why did my string trimming solution fail even though it looked identical to the platform solution?

### AI Explanation

The trimmed value was assigned to `output`, but the next statement converted the original untrimmed `input` to uppercase, discarding the trimmed result.

### Final Understanding

The second assignment unintentionally replaced the previously trimmed value.

---

## Doubt 02

### My Question

Why use `\\s` instead of `" "` as a Scanner delimiter?

### AI Explanation

`\\s` is a regular expression representing whitespace and requires escaping because Java treats backslashes specially.

### Final Understanding

The double backslash allows Java to produce a single backslash for the regex engine.

---

## Doubt 03

### My Question

Can constructors perform logic beyond assigning instance variables?

### AI Explanation

Yes. Constructors can validate input, initialize dependent fields, create objects, compute values, and establish invariants.

### Final Understanding

Constructors are initialization workflows, not merely assignment blocks.

---

## Doubt 04

### My Question

If Java copies references, how can methods modify objects?

### AI Explanation

A copied reference still points to the same object, allowing the method to modify that object's data.

### Final Understanding

Java copies the reference value, not the object itself.

---

# Questions AI Asked Me

## Question 01

### AI Question

After reassigning a Greeter reference to a new object, what happens to the original object?

### My Answer

A new object with its own instance variables is created.

### My Reasoning

The reference is redirected to the newly created object.

### Final Outcome

Partially Correct

### Correct Understanding

A new object is created and the reference variable now points to it. The original object becomes eligible for garbage collection if no references remain.

---

## Question 02

### AI Question

Identify the instance variable, local variable, and parameter in the `changeUsername` example.

### My Answer

username, oldUsername, newUsername

### My Reasoning

I recognized the three variable types involved.

### Final Outcome

Partially Correct

### Correct Understanding

* Instance Variable → username
* Local Variable → oldUsername
* Formal Parameter → newUsername

---

## Question 03

### AI Question

After calling `doubleValue(x)` where `x = 10`, what are the values of `x` and `number`?

### My Answer

10, 20

### My Reasoning

The method modifies the copied value.

### Final Outcome

Correct

### Correct Understanding

Primitive values are passed by value, so only the copied variable changes.

---

## Question 04

### AI Question

For a frequently displayed XP value that changes rarely, would you compute or store it?

### My Answer

Store

### My Reasoning

The value is read frequently but updated infrequently.

### Final Outcome

Correct

### Correct Understanding

Frequent reads and infrequent writes often justify storing computed values.

---

# Learning Artifacts

## Artifact 01

Type:

Debugging Case

Title:

String Trim and Uppercase Bug

Purpose:

Understanding variable reassignment and data flow.

Concepts Used:

* String Manipulation
* Variables
* Assignment

---

## Artifact 02

Type:

Discussion

Title:

Backend Usage of Getters and Setters

Purpose:

Mapping object-oriented concepts to real backend request flows.

Concepts Used:

* Encapsulation
* Getters
* Setters

---

## Artifact 03

Type:

Discussion

Title:

Memory vs Computation Tradeoffs

Purpose:

Comparing alternative class implementations.

Concepts Used:

* Design Tradeoffs
* Performance
* Encapsulation

---

# Engineering Intuition Developed

## Insight 01

Classes are blueprints, but object memory is allocated only when `new` executes.

---

## Insight 02

The same interface can support multiple implementations with different performance and memory characteristics.

---

# Learning Insights

## Most Important Concept Today

Passing Arguments

Reason:

It clarified the distinction between object mutation and reference reassignment.

---

## Most Valuable Doubt

Constructor Responsibilities

Reason:

It expanded understanding beyond simple field assignment.

---

## Most Valuable Question Asked By AI

XP Storage Tradeoff

Reason:

It connected a simple class example to real software architecture decisions.

---

## Concepts Requiring Revision

* Method Scope
* Reference Reassignment vs Object Mutation
* Class Design Tradeoffs

---

# End of Day Reflection

Today's learning shifted from using classes to understanding how classes are designed and implemented. The distinction between instance variables, local variables, parameters, and object references became much clearer. The most valuable realization was that Java always uses call-by-value, even for objects. Another important insight was seeing how different implementations can provide identical behavior while making different memory and computation tradeoffs. The class design discussions felt much closer to real software engineering than pure Java syntax.

---

# Navigation

## Concepts

* DecimalFormat
* parseInt
* Escape Sequences
* Scanner Delimiters
* Classes and Objects
* Instance Variables
* Constructors
* Parameters and Arguments
* Encapsulation
* Local Variables
* Class Design
* Class Implementation
* Passing Arguments
* Design Tradeoffs

## Learning Artifacts

* String Trim Debugging
* Backend Getter/Setter Discussion
* Square Class Tradeoff Discussion

## Doubts Discussed

* String Trimming Bug
* Scanner Delimiters
* Constructor Responsibilities
* Object References

## AI Verification Questions

* Reference Reassignment
* Variable Classification
* Call By Value
* Memory vs Computation Tradeoff
