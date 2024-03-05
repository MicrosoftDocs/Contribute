---
title: Labels, projects, and milestones roadmap
description: This article explains how labels, projects, and milestones are used in the dotnet/docs repository.
ms.topic: contributor-guide
ms.service: learn
ms.custom: external-contributor-guide
ms.date: 02/10/2021
---

# Labels, projects, and milestones roadmap

The .NET docs team makes extensive use of [GitHub labels](https://github.com/dotnet/docs/labels) to organize our work. By filtering on combinations of labels, we can quickly focus on sections of interest on the [.NET docs website](/dotnet). For example, we could filter to all of the open issues on the architecture guides with a query to [is:issue is:open label:"dotnet-architecture/prod"](https://github.com/dotnet/docs/labels/dotnet-architecture%2Fprod).

We use [GitHub projects](https://github.com/dotnet/docs/projects) to organize sprints and other goal-oriented epics. We also use [GitHub milestones](https://github.com/dotnet/docs/milestones) to track work. It is best to think of projects for planning (issues), and milestones for work (pull requests).

This roadmap explains how we use these organizational tools and has links to handy filters we use to find areas of interest.

## Labels

If this is your first experience contributing to [dotnet/docs](https://github.com/dotnet/docs), start with the [up-for-grabs](https://github.com/dotnet/docs/labels/up-for-grabs) issues. These are issues that have a more focused scope. They are a great way to make your first contribution. From the up-for-grabs view, you can further filter issues based on areas and priority. We've identified good issues for beginners with the [good-first-issue](https://github.com/dotnet/docs/labels/good-first-issue) if you want to try a smaller first contribution.

We use labels to classify issues in many different ways:

- [.NET Guides](#find-issues-for-a-single-net-guide) and [sections of a guide](#find-issues-for-one-section-of-a-guide).
- [Target release](#releases)
- [Priority](#priority)

You can combine a label from each set (guide, release, priority) to create a narrow focus to find issues you want to work on.

### Find issues for a single .NET guide

We use labels for each of the architecture e-books and for each .NET Guide. All ebooks are noted with the [dotnet-architecture/prod](https://github.com/dotnet/docs/labels/dotnet-architecture%2Fprod) label. Each book has a unique label that ends with `/tech`.

Each .NET Guide is noted with the [`/prod`](https://github.com/dotnet/docs/labels?q=prod) suffix and has a blue-gray background. Here are current issues filtered for each of the .NET guides.

- [.NET Guide - `dotnet/prod`](https://github.com/dotnet/docs/labels/dotnet%2Fprod)
- [.NET Fundamentals Guide (formerly .NET Standard Guide) - `dotnet-fundamentals/prod`](https://github.com/dotnet/docs/labels/dotnet-fundamentals%2Fprod)
- [.NET Fundamentals Guide (formerly .NET Core Guide) - `dotnet-core/prod`](https://github.com/dotnet/docs/labels/dotnet-core%2Fprod)
- [.NET Framework Guide - `dotnet-framework/prod`](https://github.com/dotnet/docs/labels/dotnet-framework%2Fprod)
- [API Reference - `dotnet-api/prod`](https://github.com/dotnet/docs/labels/dotnet-api%2Fprod)
- [C# Guide - `dotnet-csharp/prod`](https://github.com/dotnet/docs/labels/dotnet-csharp%2Fprod)
- [F# Guide- `dotnet-fsharp/prod`](https://github.com/dotnet/docs/labels/dotnet-fsharp%2Fprod)
- [Visual Basic Guide - `dotnet-visualbasic/prod](https://github.com/dotnet/docs/labels/dotnet-visualbasic%2Fprod)
- [ML.NET Guide - `dotnet-ml/prod`](https://github.com/dotnet/docs/labels/dotnet-ml%2Fprod)
- [Azure .NET SDK - `azure-dotnet/prod`](https://github.com/dotnet/docs/labels/azure-dotnet%2Fprod)
- [.NET for Apache Spark Guide - `dotnet-spark/prod`](https://github.com/dotnet/docs/labels/dotnet-spark%2Fprod)
- [.NET Desktop Guide - `dotnet-desktop/prod`](https://github.com/dotnet/docs/labels/dotnet-desktop%2Fprod)

Other product labels are defined for areas that cross repositories.

#### Find issues for one section of a guide

The .NET guides are large, so these labels further limit the scope by a section of a guide. Each .NET Guide subarea is noted with the [`/tech`](https://github.com/dotnet/docs/labels?q=tech) suffix and has a light blue background. Many of these labels apply to multiple guides, while others are in only one guide. After filtering on an area, add one of these labels to further limit the scope of issues.

### Releases

![:checkered_flag: Release: on dark yellow](./media/labels-projects/release.png "Prefix for release labels")

Issues tagged for a specific release are noted with the [`:checkered_flag: Release:`](https://github.com/dotnet/docs/labels?q=%3Acheckered_flag%3A+Release) prefix and have a dark yellow background.

### Priority

Priority labels are all `Pri` followed by a single digit. Lower numbers are higher priority:

- Pri0 - Critical priority

  Security issue or legally required for compliance. We drop everything else to fix.
  
- Pri1 - High priority

  Essential for common scenarios. Or highly visible error on high page view article. We do these before P2 or P3 work.
  
- Pri2 - Medium priority

  Helpful for common scenarios but not blocking.  We do these if quick and easy, or fit them in while addressing a P1 issue in the same article.
  
- Pri3 - Low priority

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
