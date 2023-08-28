
---
title: Overview
description: Overview of .NET
---

![[dotnet-logo.png]]{width=75, align=right, align=right}
# .NET

Microsoft's official framework for languages targeting the CIL specification.

.NET compiles C# (and others) to IL, links to included .NET Libraries, and runs via JIT compilation.

![[dotnet-compilation.png]]{width=520}

.NET ships with a large amount of libraries that are heavily associated with C# (Although usable in other CIL languages)

![[dotnet-diagram.png]]{width=720}

<!----------------------------------------------------------------------------->

## **Links**
External information regarding **.NET**:

| *Info*        | *Link*                              | *Note*                                            |
| ------------- | ----------------------------------- | ------------------------------------------------- |
| Documentation | [Framework][Doc] / [Core][DocAlt]   |                                                   |
| Download      | [Framework][Down] / [Core][DownAlt] | Many ways to install, exercise selective caution! |
| License       | [Framework][Lic] / [Core][LicAlt]   | Framework requires special consideration.         |
| Project Home  | [Framework][Proj] / [Core][ProjAlt] |                                                   |

[Down]:     https://dotnet.microsoft.com/en-us/download/dotnet-framework
[Doc]:      https://dotnet.microsoft.com/en-us/download/dotnet-framework
[Lic]:      https://www.microsoft.com/web/webpi/eula/net_library_eula_enu.htm
[Proj]:     https://github.com/microsoft/referencesource

[DownAlt]:  https://dotnet.microsoft.com/en-us/download
[DocAlt]:   https://dotnet.microsoft.com/en-us/download
[LicAlt]:   https://github.com/dotnet/core/blob/main/LICENSE.TXT
[ProjAlt]:  https://github.com/dotnet/core/

<!----------------------------------------------------------------------------->

### ***Nice to Know***
Information that will greatly help in understanding all things .NET:

| *Topic*             | *Link* |
| ------------------- | ------ |
| What is a Compiler? |        |
| What is a Library?  |        |
| What is a Runtime?  |        |

<!----------------------------------------------------------------------------->

### ***Getting Started***
Common day-to-day tasks, problems, and procedures:

| *Topic*               | *Link* |
| --------------------- | ------ |
| Install Visual Studio |        |

<!----------------------------------------------------------------------------->

### ***Deep Dive***
Specific information that isn't as common:

| *Topic*                         | *Link*                                     |
| ------------------------------- | ------------------------------------------ |
| Common Terms & Definitions      | [[.NET-Glossary]]                 |
|                                 |                                            |

<!----------------------------------------------------------------------------->

### ***Common Questions***
Questions you may have:

| *Question*                   | *Answer*                             |
| ---------------------------- | ------------------------------------ |
| .NET Framework vs. .NET Core | [Answer](#net-framework-vs-net-core) |

### **.NET Framework vs .NET Core**

.NET started as ***.NET Framework***, as a Windows only framework.

.NET was completely rewritten to ***.NET Core***, a cross-platform framework.

Quite a few things changed or didn't survive (i.e. ***ASP.NET WebForms***).

![[dotnet-framework-vs-core.png]]{width=520}

To help transition, a lot of things have a old (Framework) and new (Core) syntax.

<!----------------------------------------------------------------------------->

### ***Related***
Topics related to .NET:

| *Topic & Link*                               | *Why*                   |
| -------------------------------------------- | ----------------------- |
| [Visual Studio](Visual-Studio.md) | Primary Dev Tool for C# |

<!----------------------------------------------------------------------------->
