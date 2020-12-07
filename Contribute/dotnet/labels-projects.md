---
title: Labels, projects, and milestones roadmap
description: This article explains how labels, projects, and milestones are used in the dotnet/docs repository.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
ms.date: 08/06/2020
---

# Labels, projects, and milestones roadmap

The .NET docs team makes extensive use of [GitHub labels](https://github.com/dotnet/docs/labels) to organize our work. By filtering on combinations of labels, we can quickly focus on sections of interest on the [.NET docs website](https://docs.microsoft.com/dotnet). For example, we could filter to all of the open priority one `P1` issues with a query to [is:issue is:open label:":books: Area - .NET Architecture Guide"](https://github.com/dotnet/docs/issues?q=is%3Aissue+is%3Aopen+label%3A%22%3Abooks%3A+Area+-+.NET+Architecture+Guide%22).

We use [GitHub projects](https://github.com/dotnet/docs/projects) to organize sprints and other goal-oriented epics. We also use [GitHub milestones](https://github.com/dotnet/docs/milestones) to track work. It is best to think of projects for planning (issues), and milestones for work (pull requests).

This roadmap explains how we use these organizational tools and has links to handy filters we use to find areas of interest.

## Labels

If this is your first experience contributing to [dotnet/docs](https://github.com/dotnet/docs), start with the [up-for-grabs](https://github.com/dotnet/docs/labels/up-for-grabs) issues. These are issues that have a more focused scope. They are a great way to make your first contribution. From the up-for-grabs view, you can further filter issues based on areas and priority. We've identified good issues for beginners with the [good-first-issue](https://github.com/dotnet/docs/labels/good-first-issue) if you want to try a smaller first contribution.

We use labels to classify issues in many different ways:

- [.NET Guides](#find-a-single-net-guide) and [sections of a guide](#search-one-section-of-a-guide).
- [Target release](#releases)
- [Priority](#priority)

You can combine a label from each set (guide, release, priority) to create a narrow focus to find issues you want to work on.

### Find a single .NET guide

We use labels for each of the architecture e-books and for each .NET Guide.

![:book: guide on light green background](./media/labels-projects/guide.png "Prefix for architecture guide labels")

Architecture e-books are noted with the `:book: guide` prefix and have a light green background. These are the long-form areas that cover recommended architecture. Here are current issues filtered for each of the .NET architecture guides.

- [ASP.NET Core web apps](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20ASP.NET%20Core%20web%20apps)
- [Blazor](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Blazor)
- [Cloud Native](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Cloud%20Native)
- [Docker lifecycle](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Docker%20lifecycle)
- [gRPC](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20gRPC)
- [Modernizing w/ Windows containers](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Modernizing%20w%2F%20Windows%20containers)
- [.NET Microservices](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20.NET%20Microservices)
- [Serverless apps](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Serverless%20apps)

This label style is also applied to the [Framework design guidelines](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Framework%20Design%20Guidelines). This area has the same label design, but community PRs are discouraged. This is material reprinted with permission and should not be edited.

![:books: Area on dark blue background](./media/labels-projects/area.png "Prefix for .NET Guide area labels")

Each .NET Guide is noted with the `:books: Area` prefix and has a dark blue background. Here are current issues filtered for each of the .NET guides.

- [API Reference](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20API%20Reference)
- [Azure .NET SDK](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20Azure%20.NET%20SDk)
- [C# Guide](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20C%23%20Guide)
- [F# Guide](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20F%23%20Guide)
- [ML.NET Guide](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20ML.NET%20Guide)
- [.NET Architecture Guide](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20Architecture%20Guide) - Could be removed
- [.NET Core Guide](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20Core%20Guide)
- [.NET for Apache Spark Guide](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20for%20Apache%20Spark%20Guide)
- [.NET Framework Guide](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20Framework%20Guide)
- [.NET Guide](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20Guide)
- [Roslyn API Reference](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20Roslyn%20API%20Reference) - could be removed.
- [Visual Basic Guide](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20Visual%20Basic%20Guide)

#### Search one section of a guide

![:card_file_box: Area on medium blue background](./media/labels-projects/technology.png "Prefix for .NET Guide sub-area labels")

The .NET guides are large, so these labels further limit the scope by a section of a guide. Each .NET Guide subarea is noted with the `:card_file_box: Technology` prefix and has a medium blue background. Many of these labels apply to multiple guides, while others are in only one guide. After filtering on an area, add one of these labels to further limit the scope of issues.

- AppCompat
- Async Task
- C# Advanced concepts
- C# compiler
- C# Fundamentals
- C# Get Started
- C# Language Reference
- C# Null safety
- C# What's new
- CLI
- Data Access
- Docker
- Installers
- LINQ
- NCL
- .NET Standard
- Roslyn APIs
- Security
- WCF
- WF
- WIF
- WinForms
- WPF

### Releases

![:checkered_flag: Release: on dark yellow](./media/labels-projects/release.png "Prefix for release labels")

Issues tagged for a specific release are noted with the `:checkered_flag: Release:` prefix and have a dark yellow background.

- .NET Core 2.2
- .NET Core 3.0
- .NET Framework 4.8
- .NET 5

### Priority

Priority labels are all `P` followed by a single digit. Lower numbers are higher priority:

- P0 - Critical priority

  Security issue or legally required for compliance. We drop everything else to fix.
  
- P1 - High priority

  Essential for common scenarios. Or highly visible error on high page view article. We do these before P2 or P3 work.
  
- P2 - Medium priority

  Helpful for common scenarios but not blocking.  We do these if quick and easy, or fit them in while addressing a P1 issue in the same article.
  
- P3 - Low priority

  Helpful for edge cases, trivial corrections for common scenarios, low page view article, or deprecated technology. Not worth our time but up for grabs for community contribution. A P3 issue may be closed if not addressed after two months.

### What about the other labels

There are many other labels used by the content teams to manage different classifications of issues. If you're not on the content team, you can ignore these other labels.

## Projects

Projects are intended for planning purposes, where prioritized work is automated through a Kanban board. Projects should only ever contain GitHub issues, _not_ pull requests. Projects differ from milestones, in that milestones only contain pull requests.

We use projects in two ways:

- `Month YYYY` project types: These are Kanban boards for each month's working plan.
  - Examples, [July 2020](https://github.com/dotnet/docs/projects/103), [August 2020](https://github.com/dotnet/docs/projects/117), and so on.
- Long-running epics: These are used to organize tasks toward a goal when the work will occur over several months.
  - Examples: [.NET 5 Wave - Reorganization](https://github.com/dotnet/docs/projects/105), [.NET Languages (.NET 5 wave)
](https://github.com/dotnet/docs/projects/106), and so on.

## Milestones

Milestones typically follow the same naming convention of projects `Month YYYY`, but they're different from projects. We use milestones to track completed work. Milestones should _not_ contain issues (potential work), but rather exclusively contain pull requests. The current milestone is automatically applied to new pull requests.
