---
title: Programming Glossary
description: Glossary of Programming
date: 2023-09-23
hide:
  - footer
---

<!--------------------------------------------------------------->

# Programming Glossary
Terminology, Lingo, and Clarification for Programming.

---------------------------------------------------------

## Programming Language

***Simple Definition:***

- A human interface that controls computers, usually textual and with formal rules.

???+ info "Extended Definition"
    ***What:***

    - Depends on [who you're asking][planguage01]!

[planguage01]: https://en.wikipedia.org/wiki/Programming_language

---------------------------------------------------------

## Compiler

***Simple Definition:***

- A program that commonly converts code to other code (usually lower).
- Sometimes refers to linking, optimizing, and other add-on features.

---------------------------------------------------------

## Syntax
***Simple Definition:***

- The set of rules for character arrangement [to make a valid statement in a language][syntax-01].

[syntax-01]: https://www.educative.io/blog/what-is-syntax-in-programming

---------------------------------------------------------

## Semantics
***Simple Definition:***

- The meaning of the code written.
- Something like `1 + 1` and `add(1, 1)` are semantically identical.

---------------------------------------------------------

## Types
***Simple Definition:***

- A **Data Type** (or **Type**) is a classification of data which tells a language how to handle it.

***Simple Why:***

- Its creates formal logic, optimization opportunities, and easier to check code.
- Learn more about why to use [types here.](https://pavelfokin.dev/blog/why-do-programming-languages-have-types/)

???+ example "Examples"
    === "C#"

        Input:
        ```cs
        int i = 5; // int = type
        string s = "hi" // string = type
        ```

---------------------------------------------------------

## Common Data Types
***Simple Definition:***

- Most languages have a these date types (non-exhaustive):

| *Type*       | *What*                           |
| -------------------: | ------------------------------- |
| `Integers`           | -2, -1, 0, 1, 2 [(Read More)](https://en.wikipedia.org/wiki/Integer).                               |
| `Floating Point`     | -2.2, -1.0, 0.0, 1.3E-12, 2E9 [(Read More)](https://academind.com/tutorials/floating-point-precision-and-arithmetic).                               |
| `Boolean`            | false, true [(Read More)](https://stackoverflow.com/questions/5189072/does-true-equal-to-1-and-false-equal-to-0).                               |
| `Char`               | a, A, b, !, 😃 [(Read More)](https://stackoverflow.com/questions/20825275/why-would-you-use-char-as-opposed-to-string).                               |
| `Null`               | `Null`, sometimes `Undefined` or `Empty` [(Read More)](https://stackoverflow.com/questions/2627076/when-should-one-use-nullable-types-in-c)                               |
| `Enum`               | `#!c {LOW = 1, MEDIUM = 2, HIGH = 3}` [(Read More)](https://www.w3schools.com/c/c_enums.php)                               |
| `Array`              | `#!python ["ford", "toyota", "dodge"]` [(Read More)](https://www.kodeclik.com/python-array-vs-list/)                               |
| `Record` / `Struct`  | `#!csharp {string firstName, string lastName, int birthYear}` [(Read More)](https://stackoverflow.com/questions/521298/when-should-i-use-a-struct-rather-than-a-class-in-c)                               |

- Depending on language or library, they also may support these (and many more):

| *Type*       | *What*                           |
| -------------------: | ------------------------------- |
| `String`             | `Hello`, `A sentence`, `forty-two` [(Read More)](https://stackoverflow.com/questions/25633944/string-is-value-type-or-reference-type) |
| `Time`               | 23:00:00.000UTC [(Read More)](https://stackoverflow.com/questions/798121/date-vs-datetime)   |
| `Date`               | 2023-09-27 [(Read More)](https://stackoverflow.com/questions/798121/date-vs-datetime) |

---------------------------------------------------------

## Variable
***Simple Definition:***

- A **Variable** is named symbol that (may) contain data.

***Simple Why:***

- It allows for reuse of code and easier comprehension of our code.

???+ example "Examples"
    === "C#"

        Input:
        ```cs
        int i = 5; // i = variable
        string s = "hi" // s = variable
        ```

---------------------------------------------------------

## Literal
***Simple Definition:***

- A **Literal** is a value that is literally itself.
    - Such as `#!csharp "Words"`, or `#!csharp 12`, or `#!csharp false`
    - Good explanation and examples of literal vs non-literal [here.](https://stackoverflow.com/questions/485119/what-does-the-word-literal-mean/485142#485142)

***Simple Why:***

- Most languages have compile time advantages for values that won't change.

???+ example "Examples"
    === "C#"

        Input:
        ```cs
        int i = 5; // 5 = literal
        string s = "hi" // "hi" = literal
        ```

---------------------------------------------------------

## Constant
***Simple Definition:***

- A **Constant** is a **Literal** represented [as a variable.](https://stackoverflow.com/questions/44767354/confusion-between-constants-and-literals/58033459#58033459)

***Simple Why:***

- Most languages have compile time advantages for values that won't change.
- Descriptively tells programmers that this value is immutable.

???+ example "Examples"
    === "C#"

        Input:
        ```cs
        const int Months = 12; // Months are unchanging
        const double PI = 3.14; // Pi is unchanging
        ```

<!-- --------------------------------------------------------- -->

<!--
## Example
???+ tip "Other Names"
    **NOTE:** Previously called ___
    **NOTE:** Commonly called ___
???+ danger "Danger"
???+ warning "Deprecations"
***Simple Definition:***
- Thing 1
***Simple Why:***
- Thing 1
< Diagram / Picture of what it does pragmatically >
??? example "How"
    === "GUI"
    === "CLI"
    === "API"
???+ tip "Related Information & Links"
    | *Topic & Link*           | *Why*                           |
    | ------------------------ | ------------------------------- |
    | [[PARENT]]               | Subject Parent                  |
    | [[ARTICLE]]              | Article                         |
    | [Community Reference]()  | StackOverflow Detailing Concept |
    | [Documentation]()        | Official Documentation          |
    | [CLI Reference]()        | CLI Reference                   |
    | [API Reference]()        | API Reference                   |
???+ info "Extended Definition"
Extra Notes:
-->

<!--------------------------------------------------------------->

<!-- <style>
    .md-footer__link--prev {
        display: none
    }
    .md-footer__link--next {
        display: none
    }
</style> -->

<!--------------------------------------------------------------->

<!-- TO-DO List -->
