---
title: .NET Glossary
description: Glossary of .NET
date: 2023-09-23
hide:
  - footer
---

<!--------------------------------------------------------------->

# .NET Glossary
Terminology, Lingo, and Clarification for .NET.

---------------------------------------------------------

## `#!csharp Var` Type / Implicitly Typed Local Variables
***Simple Definition:***

<div class="annotate" markdown>
- Sets the variable type to whatever is first assigned.
</div>

***Simple Why:***

<div class="annotate" markdown>
- `#!csharp var x = new MyLongClassName<int>()` reads better than<br>`#!csharp MyLongClassName<int> x = new MyLongClassName<int>();`.
- Helps decouple design and write code faster at expense of some legibility if not careful.
- Read more [here.](https://stackoverflow.com/questions/4307467/what-does-var-mean-in-c)
</div>

???+ example "How"
    === "Simple"

        Input:

        ```cs
        var x = 1; // These lines are the same
        int x = 1; // These lines are the same

        var x;     // Error: Need to assign type

        var x = 1;
        x = "hi";  // Error: "hi" not an int
        ```

---------------------------------------------------------

## Value Type
***Simple Definition:***

- A **Value Type** is a value that directly holds itself in the variable's memory address.
- In Microsoft's implementation, [most built-in types are primitive.](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types)
    - **NOTE:** Certain uses of value types are treated as references OR converted via "Boxing".
- They are [usually stored on the stack, but this is an implementation detail.](https://learn.microsoft.com/en-us/archive/blogs/ericlippert/the-truth-about-value-types)

***Simple Why:***

- [Space and time efficiency mostly.](https://stackoverflow.com/questions/1932155/why-value-types-are-stored-onto-stacks)

![[image-20230930075842.png]]{width=700, align=}

???+ example "How"
    === "Value Type"

        Follow this code and examine `i`:

        ```cs
        int i = 0;
        Console.WriteLine(i);     // i = 0
        ChangeValue(i);
        Console.WriteLine(i);     // i = 0

        static void ChangeValue(int i)
        {
            i =  2;
            Console.WriteLine(i); // i = 2
        }
        ```

        For extra points, check it out in the debugger.

        ![[image-20230930084354.png]]{width=700, align=}

        Notice how when we get out of scope, it switches back!

        ![[image-20230930084627.png]]{width=700, align=}


## Reference Type
***Simple Definition:***

- A **Reference Type** is a value that is accessed by a different memory address.
- In Microsoft's implementation, [strings and most objects are references.](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types)
    - **NOTE:** Certain uses of value types are treated as references OR converted via "Boxing".
- They are [usually stored on the heap, but this is an implementation detail.](https://learn.microsoft.com/en-us/archive/blogs/ericlippert/the-truth-about-value-types)

***Simple Why:***

- Allows for fancy garbage collection and other cool stuff.
- [Our stack won't blow up trying to load a massive string / object.](https://stackoverflow.com/questions/1825964/c-c-maximum-stack-size-of-program-on-mainstream-oses) It is only [1MB/4MB](https://stackoverflow.com/questions/28656872/why-is-stack-size-in-c-sharp-exactly-1-mb)

![[image-20230930083107.png]]{width=700, align=}

???+ example "How"
    === "Reference Type"

        Objects (like this examples `Student` class) are references:

        ```cs
        Student ed = new Student();
        ed.studentName = "Ed";
        Console.WriteLine(ed.studentName); // Ed
        ChangeReferenceType(ed);
        Console.WriteLine(ed.studentName); // Not Ed

        static void ChangeReferenceType(Student student)
        {
            student.studentName = "Not Ed";
        }

        class Student
        {
            public string studentName;
        }
        ```

    === "Immutable References & `ref`"

        Notice how trying to change just the string doesn't change the object!

        ```cs
        Student ed = new Student();
        ed.studentName = "Ed";
        Console.WriteLine(ed.studentName); // Ed
        ChangeStringReference(ed.studentName);
        Console.WriteLine(ed.studentName); // Ed (!)
        ChangeClassReference(ed);
        Console.WriteLine(ed.studentName); // Not Ed

        static void ChangeStringReference(string studentName)
        {
            studentName = "Not Ed";
        }

        static void ChangeClassReference(Student student)
        {
            student.studentName = "Not Ed";
        }

        class Student
        {
            public string studentName;
        }
        ```

        So what's going on here?

        C# Passes-By-Value (in this case, the memory address). Take a look on why object properties vs strings act different:

        ![[image-20230930101434.png]]{width=700, align=}

        [Read this for more context.](https://www.tutorialsteacher.com/csharp/csharp-value-type-and-reference-type)

        ---

        Here's a simplified version of our reference being Passed-By-Value:

        ```cs
        string s = "hi!";
        Console.WriteLine(s);     // s = "hi!"
        ChangeValue(s);
        Console.WriteLine(s);     // s = "hi!" ...wait, what?

        static void ChangeValue(string s)
        {
            s = "bye!";
            Console.WriteLine(s); // s = "bye!"
        }
        ```

        [**If Absolutely Necessary,** we can resolve this by using `ref` which Passes-By-Reference.](https://stackoverflow.com/questions/1096449/c-sharp-string-reference-type)

        ```cs
        string s = "hi!";
        Console.WriteLine(s);     // s = "hi!"
        ChangeValue(ref s);
        Console.WriteLine(s);     // s = "bye!"

        static void ChangeValue(ref string s)
        {
            s = "bye!";
            Console.WriteLine(s); // s = "bye!"
        }
        ```

        [Or we can defer to using a mutable object, like StringBuilder:](https://www.tutorialsteacher.com/csharp/csharp-stringbuilder)

        ```cs
        using System.Text;

        StringBuilder s = new StringBuilder("hi!");
        Console.WriteLine(s);     // s = "hi!"
        ChangeValue(s);
        Console.WriteLine(s);     // s = "bye!"

        static void ChangeValue(StringBuilder s)
        {
            s.Clear();
            s.Append("bye!");
            Console.WriteLine(s); // s = "bye!"
        }
        ```

        Apologies if I didn't do well explaining this, its fairly nuanced!

        <iframe width="560" height="315" src="https://www.youtube.com/embed/KGFAnwkO0Pk?si=zuyKpp_QfBBm3VrO" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>


## Boxing / Unboxing
***Simple Definition:***

- Conversion of a value type to a reference type.
- This is usually not desired because it [eats extra CPU cycles and creates extra objects in memory.](https://stackoverflow.com/questions/15950692/boxing-and-performance)
- It also avoids compile-time checks, which should be avoided if possible.

***Simple Why:***

- [Early on, it was difficult to avoid passing a value to an `object` parameter or non-generic collection.](https://stackoverflow.com/questions/1040384/why-do-some-languages-need-boxing-and-unboxing)
    - **NOTE:** This has been mostly solved with generics and .NET maturity.

???+ example "How"
    === "Boxing Example"
    When passing values to an object parameter:

    ```csharp
    using System.Collections;

    ArrayList x = new ArrayList();

    int myInt = 10;     // Int
    x.Add(myInt);       // Boxing Int -> Object
    int y = (int) x[0]; // Unboxing Object -> Int Explicitly
    ```

    In our debugger, we can see this the value -> reference -> value nastiness:

    ![[image-20230930135754.png]]{width=700, align=}

---------------------------------------------------------

## Console.WriteLine
***Simple Definition:***

<div class="annotate" markdown>
- Writes to the console & adds a newline.
- Basically `#!csharp Console.Write` with a newline at the end.
{ .annotate }
</div>

***Simple Why:***

<div class="annotate" markdown>
- `#!csharp Console.WriteLine()` beats `#!csharp Console.Write()` as you'll usually want to add a return.
- Allows platform agnostic newlines, since each OS uses different control characters. (1)
</div>

1. MacOS only uses the `return` or `carriage return` character `\r`, Linux only uses the `newline` or `line feed` character `\n`, and Windows uses BOTH `\r\n`.

???+ example "How"
    === "Simple"

        Input:

        ```cs
        System.Console.WriteLine("Hello");
        System.Console.WriteLine("World");
        ```

        Output:

        ```
        Hello
        World
        ```
        **Note:** The `World` will have a newline at the end as well.

    === "Concatenation vs Formatting vs Interpolation"

        There are a few ways to slam variables into a string, you should know all of them!

        All 3 ways deliver this output:

        Output:

        ```
        Ed
        Round 1: 2
        Round 2: 3
        Total: 5
        ```

        ---

        Concatenation:

        ```cs
        string name = "Ed";
        int scoreOne = 2;
        int scoreTwo = 3;
        Console.WriteLine(name + "\nRound 1: " + scoreOne + "\nRound 2: " + scoreTwo + "\nTotal: " + (scoreOne + scoreTwo));
        ```

        Composite Formatting:

        ```cs
        string name = "Ed";
        int scoreOne = 2;
        int scoreTwo = 3;
        Console.WriteLine("{0}\nRound 1: {1}\nRound 2: {2}\nTotal: {3}", name, scoreOne, scoreTwo, (scoreOne + scoreTwo));
        ```

        [String Interpolation:](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/tokens/interpolated)

        ```cs
        string name = "Ed";
        int scoreOne = 2;
        int scoreTwo = 3;
        Console.WriteLine($"{name}\nRound 1: {scoreOne}\nRound 2: {scoreTwo}\nTotal: {scoreOne + scoreTwo}");
        ```

        String interpolation is usually the most expressive & shortest:

        ![[image-20230930160754.png]]{width=700, align=}

        [It also works well with verbatim / raw strings!](https://www.freecodecamp.org/news/new-ish-things-about-c-strings/)

    === "Verbatim & Raw Strings"

        Look, just [click this link](https://www.freecodecamp.org/news/new-ish-things-about-c-strings/) and pay attention to this picture:

        ![[image-20230930162336.png]]{width=700, align=}

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

<!-- --------------------------------------------------------- -->

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
