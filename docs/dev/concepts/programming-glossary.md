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
        int i = 5;      // int = type
        string s = "hi" // string = type
        ```

---------------------------------------------------------

## Common Data Types
***Simple Definition:***

- Most languages have these date types (non-exhaustive):

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
        int i = 5;      // i = variable
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
        const int Months = 12;  // Months are unchanging
        const double PI = 3.14; // Pi is unchanging
        ```

---------------------------------------------------------

## Escape Characters
***Simple Definition:***

- An **Escape Character** is a special character or action [represented by a symbol.](https://learn.microsoft.com/en-us/dotnet/csharp/programming-guide/strings/)
- Each language and tool has different ways of expressing the special characters.

***Simple Why:***

- How does one represent a new line or the same quote character that closes the string?

???+ example "Examples"
    === "C#"

        Input:
        ```cs
        Console.WriteLine("Hello\nWorld")
        ```

        Output:
        ```
        Hello
        World
        ```

        ---

        Input:
        ```cs
        Console.WriteLine("\"Yay!\"")
        ```

        Output:
        ```
        "Yay!"
        ```

---------------------------------------------------------

## Common Escape Characters
***Simple Definition:***

- Most languages use [C Styled Escape Characters](https://en.wikipedia.org/wiki/Escape_sequences_in_C)

This list is non-exhaustive:

| *Type*       | *What*                           |
| -------------------: | ------------------------------- |
| `\n` | New Line                                          |
| `\r` | Carriage Return (MacOS New Line / Windows `\r\n` New Line) |
| `\t` | Horizontal Tab                                    |
| `\v` | [Vertical Tab](https://stackoverflow.com/questions/3380538/what-is-a-vertical-tab) |
| `\b` | Backspace                                         |
| `\0` | Null Character                                    |
| `\\` | Literal \                                         |
| `\'` | Literal '                                         |
| `\"` | Literal "                                         |

---------------------------------------------------------

## Generics
***Simple Definition:***

- If the language supports it, allows the user to choose the data type instead of the method.
- This is [common for comparing objects or for collections](https://www.tutorialsteacher.com/csharp/csharp-collection), but [can also be for methods.](https://www.programiz.com/csharp-programming/generics)
- Sometimes [generics types can be constrained from any type to specific types.](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/keywords/where-generic-type-constraint)

***Simple Why:***

- Allows compile time checks & optimization.
- Allows for reuseable code.
- Eliminates boxing for languages the implicitly cast.

???+ example "Examples"
    === "C#"

        ```cs
        var myIntList = new List<int>();
        myIntList.Add(10);
        myIntList.Add("String");     // Error: string != int

        var myStringList = new List<string>();
        myStringList.Add("String");
        myStringList.Add(10);        // Error: int != string
        ```

---------------------------------------------------------

## Stack & Heap

***Simple What:***

- How data is held in memory and used when running.
- This is a complex subject that will vary by every programming & OS implementation.

***Simple Why:***

- The way many popular languages split variable scope and object persistent.
- Stack variables are faster to add and remove, where as heap variables are global and shareable.
- [Better explained here.](https://www.alexhyett.com/stack-vs-heap-memory/)

I'll leave it to the professionals to explain this:

<iframe width="560" height="315" src="https://www.youtube.com/embed/5OJRqkYbK-4?si=qNpAhmm8z2o2MOpw" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

---------------------------------------------------------

## Type Casting / Type Conversion

***Simple What:***

- Depending on language, implicitly or explicitly converts one type to another.
- For instance, a `int` will usually automatically "widen" to a double.

***Simple Why:***

- Sometimes you need to have a different type from data that already exists.

???+ example "Examples"
    === "C#"

        Implicit:

        ```cs
        int myInt = 9;
        double myDouble = myInt; // Now we have a 9 of type double!
        ```

        Explicit:

        ```cs
        double myDouble = 9.78;
        int myInt = (int) myDouble;    // Notice how we define (int) since we may lose data.
        Console.WriteLine(myDouble);   // Outputs 9.78
        Console.WriteLine(myInt);      // Outputs 9 (!)
        ```

        There are other ways to do these conversions, but these are the most common ways when people say "Type Casting"

---------------------------------------------------------

## Modulus

***Simple What:***

- Common way of getting remainder of number after division, represented by symbol `%`.

***Simple Why:***

- Good for launching "Once every `n` times" operations.
- Good for determining even & odd.
- Good way to create chance system in combination with a random function.

![[image-20230930165909.png]]{width=700, align=}

???+ example "Examples"
    === "C#"

        Basic example:

        ```cs
        int timeOne   = 23 % 12; // 11
        int timeTwo   = 24 % 12; // 0
        int timeThree = 25 % 12; // 1
        ```

        Even or Odd:

        ```cs
        if (num % 2 == 0) {
            // even
        }
        ```

---------------------------------------------------------

## Compound Assignment Operators

***Simple What:***

- Operators like `+=`, `-=`, and even `=>`.
- [Learn about what each one does here.](https://www.tutorialspoint.com/compound-assignment-operators-in-chash)

***Simple Why:***

- Makes reading code *sometimes* more elegant. This is an audience question.

---------------------------------------------------------

## Increment / Decrement

***Simple What:***

- Add or subtracts (or otherwise moves up/down) a variable.
- [Depending on language, `++i` and `i++` have slightly different meaning.](https://stackoverflow.com/questions/24901/is-there-a-performance-difference-between-i-and-i-in-c/9519095#9519095)
    - If its a presentation that also impacts the variable, [it will make a difference.](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/operators/arithmetic-operators)
    - **Note:** Common premature optimization, [the compiler / language fixes performance / doesn't matter.](https://stackoverflow.com/questions/467322/is-there-any-performance-difference-between-i-and-i-in-c)

***Simple Why:***

- Easy way to move up and down a number.
- Useful during `for loops` or iterations.

???+ example "Examples"
    === "C#"

        Basic example:

        ```cs
        int i = 1;
        i++;       // i = 2
        ```

        Order difference example:

        ```cs
        int i = 1;
        Console.WriteLine(i++); // "1"; i = 2
        ```

        ```cs
        int i = 1;
        Console.WriteLine(++i); // "2"; i = 2
        ```

## Dictionary / Map / Key Value Collection

***Simple What:***

- Many names to describe a collection of keys and values, usually modifiable.
- Formally defined as an [Associative Array](https://en.wikipedia.org/wiki/Associative_array).
- A Hash Map / Hash Table is an *implementation* of the underlying key sorting algorithm.
    - **NOTE:** Many languages have different underlying algorithms that [fulfill the same purpose](https://stackoverflow.com/questions/301371/why-is-dictionary-preferred-over-hashtable-in-c).

***Simple Why:***

- Lots of things need a unique identifier with information under it.
    - For instance, a student (who has a unique ID) and their overall grades.

???+ example "Examples"
    === "C#"

        C# has [a `Hashtable` and a ***preferred*** generic-capable `Dictionary`.](https://stackoverflow.com/questions/301371/why-is-dictionary-preferred-over-hashtable-in-c)

        Dictionary accepts nearly any type for both `<Key, Value>`.

        Student example:

        ```cs
        using System.Collections.Generic;

        var grades = new Dictionary<string, List<int>>();
        grades.Add("Ed",       new List<int> {93, 87, 98, 95, 10});
        grades.Add("Deadbeef", new List<int> {80, 83, 82, 88, 85});
        grades.Add("Cafe",     new List<int> {84, 96, 73, 85, 79});
        ```

        You may also [initialize it with data a few different ways.](https://learn.microsoft.com/en-us/dotnet/csharp/programming-guide/classes-and-structs/how-to-initialize-a-dictionary-with-a-collection-initializer)

        ```cs
        var grades = new Dictionary<string, List<int>>
        {
            {"Ed",         new List<int> {93, 87, 98, 95, 10}},
            {"Deadbeef",   new List<int> {80, 83, 82, 88, 85}}
        };
        // ... You can still add them later normally
        grades.Add("Cafe", new List<int> {84, 96, 73, 85, 79});
        ```

---------------------------------------------------------

## Stateful / Stateless Code

***Simple What:***

- **Stateful** code stores information about itself that can be recalled later.
- **Stateless** code works regardless and consistently without memory of the past.
- Good [answers here](https://stackoverflow.com/questions/5329618/stateless-vs-stateful).

***Simple Why:***

- This is the nature of code. Either it is or isn't.
- Stateless code is [usually preferred because it enables more consistent and parallel code.](https://stackoverflow.com/questions/844536/advantages-of-stateless-programming).
- State is almost always unavoidable however, or preferred!

???+ example "Examples"
    === "C#"

    Stateless:

    ```cs
    void addTwo(int a, int b)
    {
        int statelessNumber = a + b;
        Console.WriteLine(statelessNumber);
    };

    addTwo(1, 2);
    ```

    Stateful:

    ```cs
    int statefulNumber;

    void addMore(int a)
    {
        statefulNumber = statefulNumber + a;
        Console.WriteLine(statefulNumber);
    }

    addMore(5);
    addMore(5);
    ```


    ![[image-20231001141656.png]]{width=400, align=}


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

##
