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
        ---
        ```cs
        System.Console.WriteLine("Hello");
        System.Console.WriteLine("World");
        ```

        Output:
        ---
        ```
        Hello
        World
        ```
        **Note:** The `World` will have a newline at the end as well.

    === "Variables"

        input:
        ---
        ```cs
        // Any Variable That Has a .ToString
        int x = 2;
        System.Console.WriteLine("Hello " + x);
        ```

        Output:
        ---
        ```
        Hello
        World
        ```
        **Note:** The `World` will have a newline at the end as well.

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

<!-- ## Example -->
<!-- ???+ tip "Other Names"
    **NOTE:** Previously called ___
    **NOTE:** Commonly called ___                              -->
<!-- ???+ danger "Danger"-->
<!-- ???+ warning "Deprecations"-->
<!-- ***Simple Definition:*** -->
<!-- - Thing 1 -->
<!-- ***Simple Why:*** -->
<!-- - Thing 1 -->
<!-- < Diagram / Picture of what it does pragmatically >       -->
<!-- ??? example "How"
    === "GUI"
    === "CLI"
    === "API" -->
<!-- ???+ tip "Related Information & Links"
    | *Topic & Link*           | *Why*                           |
    | ------------------------ | ------------------------------- |
    | [[PARENT]]               | Subject Parent                  |
    | [[ARTICLE]]              | Article                         |
    | [Community Reference]()  | StackOverflow Detailing Concept |
    | [Documentation]()        | Official Documentation          |
    | [CLI Reference]()        | CLI Reference                   |
    | [API Reference]()        | API Reference                   | -->
<!-- ???+ info "Extended Definition" -->
<!-- Extra Notes: -->

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
