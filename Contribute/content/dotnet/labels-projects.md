---
title: Labels, projects, and milestones roadmap
description: This article explains how labels, projects, and milestones are used in the dotnet/docs repository.
ms.topic: contributor-guide
ms.service: learn
ms.custom: external-contributor-guide
ms.date: 06/17/2025
---

# Labels, projects, and milestones roadmap

The .NET docs team makes extensive use of [GitHub labels](https://github.com/dotnet/docs/labels) to organize our work. By filtering on combinations of labels, we can quickly focus on sections of interest on the [.NET docs website](/dotnet). For example, we could filter to all of the open issues on the architecture guides with a query to [is:issue is:open label:"dotnet-architecture/svc"](https://github.com/dotnet/docs/labels/dotnet-architecture%2Fsvc).

We use [GitHub projects](https://github.com/dotnet/docs/projects) to organize sprints and other goal-oriented epics. We also use [GitHub milestones](https://github.com/dotnet/docs/milestones) to track work. It is best to think of projects for planning (issues), and milestones for work (pull requests).

This roadmap explains how we use these organizational tools and has links to handy filters we use to find areas of interest.

## Labels

If this is your first experience contributing to [dotnet/docs](https://github.com/dotnet/docs), start with the [help wanted](https://github.com/dotnet/docs/labels/help%20wanted) issues. These are issues that have a more focused scope. They are a great way to make your first contribution. From the up-for-grabs view, you can further filter issues based on areas and priority. We've identified good issues for beginners with the [good first issue](https://github.com/dotnet/docs/labels/good%20first%20issue) if you want to try a smaller first contribution.

We use labels to classify issues in many different ways:

- [.NET Guides](#find-issues-for-a-single-net-guide) and [sections of a guide](#find-issues-for-one-section-of-a-guide).
- [Target release](#releases)

You can combine a label from each set (guide, release, priority) to create a narrow focus to find issues you want to work on.

### Find issues for a single .NET guide

We use labels for each of the architecture e-books and for each .NET Guide. All ebooks are noted with the [dotnet-architecture/prod](https://github.com/dotnet/docs/labels/dotnet-architecture%2Fprod) label. Each book has a unique label that ends with `/subsvc`.

Each .NET Guide is noted with the [`/svc`](https://github.com/dotnet/docs/labels?q=svc) suffix and has a blue-gray background. Here are current issues filtered for each of the .NET guides.

- [.NET Guide - `dotnet/svc`](https://github.com/dotnet/docs/labels/dotnet%2Fsvc)
- [.NET Fundamentals Guide (formerly .NET Standard Guide) - `dotnet-fundamentals/svc`](https://github.com/dotnet/docs/labels/dotnet-fundamentals%2Fsvc)
- [.NET Fundamentals Guide (formerly .NET Core Guide) - `dotnet-core/svc`](https://github.com/dotnet/docs/labels/dotnet-core%2Fsvc)
- [.NET Framework Guide - `dotnet-framework/svc`](https://github.com/dotnet/docs/labels/dotnet-framework%2Fsvc)
- [API Reference - `dotnet-api/svc`](https://github.com/dotnet/docs/labels/dotnet-api%2Fsvc)
- [C# Guide - `dotnet-csharp/svc`](https://github.com/dotnet/docs/labels/dotnet-csharp%2Fsvc)
- [F# Guide- `dotnet-fsharp/svc`](https://github.com/dotnet/docs/labels/dotnet-fsharp%2Fsvc)
- [Visual Basic Guide - `dotnet-visualbasic/svc`](https://github.com/dotnet/docs/labels/dotnet-visualbasic%2Fsvc)
- [ML.NET Guide - `dotnet-ml/svc`](https://github.com/dotnet/docs/labels/dotnet-ml%2Fsvc)
- [Azure .NET SDK - `dotnet-azure/svc`](https://github.com/dotnet/docs/labels/azure-dotnet%2Fsvc)
- [.NET Desktop Guide - `dotnet-desktop/svc`](https://github.com/dotnet/docs/labels/dotnet-desktop%2Fsvc)

Other product labels are defined for areas that cross repositories.

#### Find issues for one section of a guide

The .NET guides are large, so these labels further limit the scope by a section of a guide. Each .NET Guide subarea is noted with the [`/subsvc`](https://github.com/dotnet/docs/labels?q=subsvc) suffix and has a light blue background. Many of these labels apply to multiple guides, while others are in only one guide. After filtering on an area, add one of these labels to further limit the scope of issues.

### Releases

![:checkered_flag: Release: on dark yellow](./media/labels-projects/release.png "Prefix for release labels")

Issues tagged for a specific release are noted with the [`:checkered_flag: Release:`](https://github.com/dotnet/docs/labels?q=%3Acheckered_flag%3A+Release) prefix and have a dark yellow background.

### What about the other labels

There are many other labels used by the content teams to manage different classifications of issues. If you're not on the content team, you can ignore these other labels.

## Projects

Projects are intended for planning purposes, where prioritized work is automated through a Kanban board. Projects should only ever contain GitHub issues, _not_ pull requests. Projects differ from milestones, in that milestones generally contain pull requests. We watch milestones to make sure pull requests don't get stale.

We use projects in two ways:

- `Month YYYY` project types: These are Kanban boards for each month's working plan.
- Long-running epics: These are used to organize tasks toward a goal when the work will occur over several months.

## Milestones

Milestones typically follow the same naming convention of projects `Month YYYY`, but they're different from projects. We use milestones to track completed work. Milestones should _not_ contain issues (potential work), but rather exclusively contain pull requests. The current milestone is automatically applied to new pull requests.
