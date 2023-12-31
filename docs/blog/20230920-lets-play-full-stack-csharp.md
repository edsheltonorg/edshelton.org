---
# draft: true
title: "Let's Play: Full Stack C# Developer" # Proper Title, Auto Slugged
description: Ed's adventure in learning C# & .NET
authors:
  - ed
date:
  created: 2023-09-20
  # updated:
# readtime: 15
---

<!--------------------------------------------------------------->

A coworker of mine in IT operations is beginning to learn how to program!

We were discussing the most pragmatic ways to become a holistic dev, <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;I didn't have a perfect answer, but I have a gut feeling road maps are great:

![[roadmapsh-backend.png]]{width=700, align=}

So I will begin a quest to "Let's Play" (1) a road maps.
{.annotate}

1. The act of aimlessly narrating something with no end in sight!

Let's 0-to-100 as an aspiring .NET developer, while making our own road map on the way!

<!-- more -->

---------------------------------------------------------

??? info "Article Updates"

    | Date       | What                                          |
    | ---------- | --------------------------------------------- |
    | 2023-09-20 | [Game Plan](#game-plan)                                     |
    | 2023-09-23 | [01. The Adventure Begins](#01-the-adventure-begins) |

---------------------------------------------------------

## Game Plan

I'll be starting from scratch like a beginner would! (1)
{.annotate}

1. I am a systems administrator w/ strong emphasis on PowerShell & Python. I will be dogfooding this strategy to ensure its appropriate for all I recommend it to.

??? abstract "Material & Road Maps"
    I put this material in the basic order I'd be trying to start them.

    Some will lay incomplete before beginning the next one, but I intend to finish all.

    | Material                                                  |
    | --------------------------------------------------------- |
    | [01: Microsoft + FreeCodeCamp Foundational C# Certification](https://www.freecodecamp.org/learn/foundational-c-sharp-with-microsoft) |
    | [02: C# Learning Roadmap](https://github.com/gridlocdev/csharp-learning-roadmap) |
    | [03: Roadmap.sh ASP.NET](https://roadmap.sh/aspnet-core) |
    | [04: Roadmap.sh SQL](https://roadmap.sh/sql) |
    | [05: Roadmap.sh PostgreSQL](https://roadmap.sh/postgresql-dba) |
    | [06: Roadmap.sh MongoDB](https://roadmap.sh/mongodb) |
    | [07: Roadmap.sh Docker](https://roadmap.sh/docker) |
    | [08: Roadmap.sh Kubernetes](https://roadmap.sh/kubernetes) |
    | [09: Roadmap.sh GraphQL](https://roadmap.sh/graphql)
    | [10: Roadmap.sh Frontend](https://roadmap.sh/frontend) |
    | [11: Roadmap.sh UX Design](https://roadmap.sh/ux-design) |
    | [12: Roadmap.sh Design System](https://roadmap.sh/design-system) |
    | [13: Roadmap.sh Javascript](https://roadmap.sh/javascript) |
    | [14: Roadmap.sh Typescript](https://roadmap.sh/typescript) |
    | [15: Roadmap.sh Node.JS](https://roadmap.sh/nodejs) |
    | [16: Roadmap.sh Frontend Performance](https://roadmap.sh/best-practices/frontend-performance) |
    | [17: Roadmap.sh React](https://roadmap.sh/react) |
    | [18: Roadmap.sh React Native](https://roadmap.sh/react-native) |
    | [19: Roadmap.sh Code Review](https://roadmap.sh/best-practices/code-review) |
    | [20: Roadmap.sh QA](https://roadmap.sh/qa) |
    | [21: Roadmap.sh Backend](https://roadmap.sh/backend) |
    | [22: Roadmap.sh Devops](https://roadmap.sh/devops) |
    | [23: Roadmap.sh API Security](https://roadmap.sh/best-practices/api-security) |
    | [24: Roadmap.sh AWS Best Practices](https://roadmap.sh/best-practices/aws) |
    | [25: Roadmap.sh CyberSecurity](https://roadmap.sh/cyber-security) |
    | [26: Roadmap.sh System Design](https://roadmap.sh/system-design) |
    | [27: Roadmap.sh Computer Science](https://roadmap.sh/computer-science) |
    | [28: Roadmap.sh Software Design Architecture](https://roadmap.sh/software-design-architecture) |

[C# Academy](https://www.thecsharpacademy.com) will be used as self guided exams to test comprehension.

If all goes well, the goal is to make my own roadmap.sh style map for you all!

---------------------------------------------------------

## 01. The Adventure Begins

### Beginning as a Beginner

Did you know [99.5%](https://blog.stephsmith.io/learning-to-code-apps/) of people can't program?

![[image-20230923140317.png]]{width=200, align=}

So let's jump into the mind of an anxious beginner:

- Where should I start?
- Should I jump straight into code?
- Maybe setup an IDE or text editor?

Turns out, Microsoft and FreeCodeCamp got together to make an [Intro C# Certification](https://www.freecodecamp.org/learn/foundational-c-sharp-with-microsoft/).

![[image-20230924203825.png]]{width=700, align=}

The first module even has a built-in coding panel, how friendly!

![[image-20230923032354.png]]{width=700, align=}

They get you into action almost right away, while explaining just a little theory.

---

### Gripes & Mindset Fix

This material is (mostly) great! It doesn't treat you like an idiot.

However, one gripe is the occasional use of terms without definition:

![[image-20230923040433.png]]{width=700, align=}

Alluding to untaught subjects both under-explains and over-explains!<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Younger me would panic: **"I've missed something big!"**

I find an effective strategy to stop this anxiety is to just write it down:

![[image-20230923142625.png]]{width=700, align=}

If our source doesn't do a good job answering the question, we'll just google it later!<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;I treat it like patiently asking a question after a lecture.

---------------------------------------------------------

### Cheat Sheets

As a *slightly-more-than-beginner* developer, this exercise is helping me build my site!

Anything I find useful will be added to either of these glossaries:

- [[dotnet-glossary|.NET Glossary]]
- [[programming-glossary|Programming Glossary]]

I highly encourage you to keep a terminology cheat sheet! It helps tremendously.

---------------------------------------------------------

### Rapid Experimenting

God, how lucky are we to be alive in this very moment.

Microsoft made an extension to jupyter notebooks to allow C#, F#, PowerShell, and more!

![[image-20230924204836.png]]{width=700, align=}

I **Highly Recommend** installing it, as it will help you visualize what's going on.

For instance, here's an easy to follow class & object assignment:

![[image-20230924220722.png]]{width=700, align=}

Now check how I can output normally & via Jupyter's variable examination:

![[image-20230924220747.png]]{width=700, align=}

Take note how I didn't have to use any `#!csharp using` statements or boilerplate!

This brings my favorite feature of shell-like languages to C#: ***Organically Messing Around!***

The only thing I see being a thorn is the fact `#!csharp Console.ReadLine()` doesn't work, rather this:

![[image-20230924225444.png]]{width=700, align=}

If I ever decide to teach, I'll have to determine how to address this if it isn't fixed.

---------------------------------------------------------

### Non-Windows People Rejoice

Good news!

VSCode & the official C# Dev Kit extensions work on all major operating systems. (1)
{ .annotate }

1. VS Codium had issues w/ the C# extension for licensing reasons, which is the same general terms as the Visual Studio EULA. This isn't FOSS at all, and you need to be cautious when using for a commercial product!

The C# Dev Kit provides a lot of Visual Studio features to VSCode, like project creation:

![[image-20230928204049.png]]{width=700, align=}

And the Solution Explorer allows adding project files nicely.

![[image-20230928204026.png]]{width=700, align=}

Testing has a nice interface as well!

![[image-20230929203310.png]]{width=300, align=}

.NET Framework stuff is mostly stripped, but that's beyond OK!

Let's see how far we can get w/ VSCode!

---------------------------------------------------------

### VSCode Idiosyncrasies

Oh geez... how will I explain this sanely?

So, the normal debug `launch.json` and the top right debug buttons are controlled separately:

![[image-20230927220554.png]]{width=700, align=}

The top right button is controlled by the (mostly working) C# Dev Kit via the `settings.json` file.

Basically the only annoying thing is the default behavior to use the debug console.<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
It doesn't allow for the `#!csharp Console.ReadLine()` to be input:

![[image-20230928193551.png]]{width=700, align=}

This can be fixed, [however integratedTerminal is tricky to use until they fix it!](https://github.com/microsoft/vscode-dotnettools/issues/82#issuecomment-1739008950)

As such, we'll use our preferred terminal for console apps:

```json title=".vscode/settings.json"
{
    // ...
    "csharp.debug.console": "externalTerminal", // or integratedTerminal when working nicely
    "debug.internalConsoleOptions": "neverOpen",
    "debug.openDebug": "neverOpen",
}
```

Here's the external terminal in action:<br>
**Note:** VSCode doesn't hold the console open, so you can add this code to hold it open:<br> `#!csharp if (System.Diagnostics.Debugger.IsAttached) Console.ReadKey(true);`

![[image-20230928203751.png]]{width=700, align=}

If you don't mind the debug menu focusing (or its fixed), here's the integrated terminal:

![[image-20230928201013.png]]{width=700, align=}

---------------------------------------------------------

### Part 1 Complete!

Wow, that was a lot more comprehensive then I thought!

We are introduced into types and general programming logic.

![[image-20231001104911.png]]{width=700, align=}

It also got pretty deep in `#!csharp Console.WriteLine()` formatting, I learned a few things!

With the projects, they'll let you cheat yourself if you're not careful.

![[image-20231001105315.png]]{width=700, align=}

The projects are done at the skill level they want and are great!

The editor on the side was pretty easy to work with too.

I will say that this is a great interactive way to get someone started from nothing.<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
It will save you time in seeing if someone is serious. Usually they're not!

--------------------------------------------------------

### Part 2

Hey, I'm glad I decided to use VSCode for this in the background.

Our first assignment is to setup VSCode (and will be used all the way to the end).<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
**Note:** The instructions are mostly Windows w/ small mentions of Linux & MacOS.<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
You can easily follow along, but just be aware its not dynamic based off user agent.

![[image-20231001113235.png]]{width=700, align=}

They introduce you to it very nicely as well:

![[image-20231001113830.png]]{width=700, align=}

---------------------------------------------------------

### Learning to Swim

Very shortly into part 2 does it start asking you to RTFM.

This is excellent, they introduce where to look (that is, search engines & M$ docs).

Here's an example:

![[image-20231007102603.png]]{width=700, align=}

I initially searched "Largest" instead of "Larger" and couldn't find anything in the docs.

So I consulted the internet, and StackOverflow introduced `#!csharp Math.Max()`

![[image-20231007103304.png]]{width=700, align=}

I really like that it introduces the main problem solving workflow early to the student.

<!-- --------------------------------------------------------- -->

<!-- OPTIONAL: ???+ bug "Issues And Questions Still Faced"

    | Error / Issue               | Article / Bug Track          |
    | --------------------------- | ---------------------------- |
    |                             | [[Answer#Section]]           | -->

<!-- --------------------------------------------------------- -->

<!-- OPTIONAL: ???+ example "Related Topics"

    | Topic & Link                | Why                          |
    | --------------------------- | ---------------------------- |
    | [[PARENT]]                  | Logical Concept              | -->

<!--------------------------------------------------------------->

<!-- TO-DO List -->
