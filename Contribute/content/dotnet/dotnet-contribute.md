---
title: Contribute to the .NET documentation repositories
description: This article describes the process for contributing to the articles and code samples in the repositories that make up the .NET documentation.
ms.topic: contributor-guide
ms.service: learn
ms.custom: external-contributor-guide
ms.date: 04/08/2021
---
# Contribute to the .NET documentation repositories

Thank you for your interest in contributing to the .NET documentation!

This document covers the process for contributing to the articles and code samples that are hosted on the [.NET documentation site](/dotnet). Contributions may be as simple as typo corrections or as complex as new articles.

The .NET documentation site is built from multiple repositories. These are just some of them:

- [.NET conceptual articles and code snippets](https://github.com/dotnet/docs)
- [Code samples and snippets](https://github.com/dotnet/samples)
- [.NET API reference](https://github.com/dotnet/dotnet-api-docs)
- [.NET Compiler Platform SDK reference](https://github.com/dotnet/roslyn-api-docs)
- [ML.NET API reference](https://github.com/dotnet/ml-api-docs)

## Guidelines for contributions

We appreciate community contributions to documentation. The following list shows some guiding rules to keep in mind when you're contributing to .NET documentation:

- **DON'T** surprise us with large pull requests. Instead, file an issue and start a discussion so we can agree on a direction before you invest a large amount of time.
- **DON'T** include sample code inline in an article.
- **DO** use a snippet project with code to be embedded in the article.
- **DO** follow these instructions and [voice and tone](dotnet-voice-tone.md) guidelines.
- **DO** use the [template](dotnet-style-guide.md) file as the starting point of your work.
- **DO** create a separate branch on your fork before working on the articles.
- **DO** follow the [GitHub flow](https://guides.github.com/introduction/flow/).
- **DO** blog and tweet (or whatever) about your contributions if you like!

Following these guidelines will ensure a better experience for you and for us.

## Contribution process

**Step 1:** If you're interested in writing new content or in thoroughly revising existing content, open an [issue](https://github.com/dotnet/docs/issues) describing what you want to do. The content inside the **docs** folder is organized into sections that are reflected in the table of contents (TOC). Define where the topic will be located in the TOC. Get feedback on your proposal.

-or-

Choose an existing issue and address it. You can look at our [open issues](https://github.com/dotnet/docs/issues) list and volunteer to work on the ones you're interested in:

- Filter by the [good-first-issue](https://github.com/dotnet/docs/labels/good-first-issue) label for, well, good first issues.
- Filter by the [up-for-grabs](https://github.com/dotnet/docs/labels/up-for-grabs) label for issues appropriate for community contribution. These issues usually require minimal context.
- Experienced contributors can tackle any issues of interest.

When you find an issue to work on, add a comment to ask if it's open.

Once you've picked a task to work on, [create a GitHub account](../index.md#create-a-github-account) and move on to Step 2.

**Step 2:** Fork the `/dotnet/docs` repo (or whichever repo you're contributing to) as needed and create a branch for your changes.

For small changes, see [Edit in the browser](../how-to-write-quick-edits.md).

**Step 3:** Make the changes on this new branch.

If it's a new topic, you can use this [template file](dotnet-style-guide.md) as your starting point. It contains the writing guidelines and also explains the metadata required for each article, such as author information. For more information on the Markdown syntax used in Microsoft Learn content, see [Markdown reference](../markdown-reference.md).

Navigate to the folder that corresponds to the TOC location determined for your article in Step 1. That folder contains the Markdown files for all articles in that section. If necessary, create a new folder to place the files for your content. The main article for that section is called *index.md*.

For images and other static resources, create a subfolder called **media** inside the folder that contains your article, if it doesn't already exist. Inside the **media** folder, create a subfolder with the article name (except for the index file). For more information about where to place your files, see the [Example folder structure](#example-folder-structure) section.

Don't include code inline in the article, unless you're demonstrating a construct that doesn't compile. Instead, use a **code snippets** project and include the code using the code extension. That ensures that your sample code is validated by our CI system.

For **code snippets**, create a subfolder called **snippets** inside the folder that contains your article, if it doesn't already exist. Inside the **snippets** folder, create a subfolder with the article name. In most cases, you'll have code snippets for all three of the main .NET languages, C#, F#, and Visual Basic. In that case, create subfolders named **csharp**, **fsharp**, and **vb** for each of the three projects. If you're creating a snippet for an article under the [docs/csharp](https://github.com/dotnet/docs/tree/main/docs/csharp), [docs/fsharp](https://github.com/dotnet/docs/tree/main/docs/fsharp), or [docs/visual-basic](https://github.com/dotnet/docs/tree/main/docs/visual-basic) folders, the snippet will only be in one language so you can omit the language subfolder. For more information about where to place your files, see the [Example folder structure](#example-folder-structure) section.

Code snippets are small, focused examples of code that demonstrate the concepts covered in an article. Larger programs intended for download and exploration should be located in the [dotnet/samples](https://github.com/dotnet/samples) repository. Full samples are covered in the section on [Contributing to samples](#contribute-to-samples).

**Step 4:** Submit a pull request (PR) from your branch to the default branch.

> [!IMPORTANT]
> The comment automation functionality is not available on any of the .NET docs repositories at this time. Members of the .NET docs team will review and merge your PR.

Each PR should usually address one issue at a time, unless multiple issues are related to the same PR fix. The PR can modify one or multiple files. If you're addressing multiple fixes on different files, separate PRs are preferred.

If your PR fixes an existing issue, add the `Fixes #Issue_Number` keyword to the PR description. That way, the issue is automatically closed when the PR is merged. For more information, see [Linking a pull request to an issue using a keyword](https://docs.github.com/github/managing-your-work-on-github/linking-a-pull-request-to-an-issue#linking-a-pull-request-to-an-issue-using-a-keyword).

The .NET team will review your PR and let you know if there are any other updates/changes necessary in order to approve it.

**Step 5:** Make any necessary updates to your branch as discussed with the team.

The maintainers will merge your PR into the default branch once feedback has been applied and your change is approved.

We regularly push all commits from default branch into the live branch and then you'll be able to see your contribution live in the [.NET documentation](/dotnet/). We typically publish daily during the work week.

## Example folder structure

```
docs
  /about
  /core
    /porting
      porting-overview.md
      /media
        /porting-overview
          portability_report.png
        /shared ...
      /snippets
        /porting-overview
          /csharp
            porting.csproj
            porting-overview.cs
            Program.cs
          /fsharp
            porting.fsproj
            porting-overview.fs
            Program.fs
          /vb
            porting.vbproj
            porting-overview.vb
            Program.vb
        /shared
          /csharp ...
          /fsharp ...
          /vb ...
```

> [!NOTE]
> The language folders under snippets are not needed in the language guide area, where only one language is assumed. For example, in the C# guide, it's assumed that all snippets are C#.

The structure shown above includes one image, *portability_report.png*, and three code projects that include **code snippets** that are included in the *porting-overview.md* article.

The *snippets/shared* folder is used for snippets that may span multiple articles within the same parent folder, such as the *porting* folder in the previous example. Only use the *shared* folder when you have a specific reason to do so, such as XAML code that's referenced by multiple articles, yet can't compile in the *article-specific* folder.

Media can also be shared across articles when those articles are in the same parent folder, such as the *porting* folder in the previous example. This *shared* folder should be avoided if possible, and only used when it makes sense. For example, it may make sense to share a common loading screen for the app being demonstrated, or share Visual Studio dialogs that are reused across multiple articles.

> [!IMPORTANT]
> For historical reasons, many of the included snippets are stored under the */samples* folder in the *dotnet/docs* repository. If you're making major changes to an article, those snippets should be moved to the new structure. However, don't worry about moving snippets for small changes.

## Contribute to samples

We make the following distinction for code that supports our content:

- Samples: readers can download and run the samples. All samples should be complete applications or libraries. Where the sample creates a library, it should include unit tests or an application that lets readers run the code. They often use more than one technology, feature, or toolkit. The readme.md file for each sample will refer to the article so that you can read more about the concepts covered in each sample.
- Snippets: illustrate a smaller concept or task. They compile but they are not intended to be complete applications. They should run correctly, but aren't an example application for a typical scenario. Instead, they are designed to be as small as possible to illustrate a single concept or feature. These should be no more than a single screen of code.

Samples are stored in the [dotnet/samples](https://github.com/dotnet/samples) repository. We are working toward a model where our samples folder structure matches our docs folder structure. Standards that we follow are:

- Top-level folders match the top level folders in the *docs* repository. For example, the docs repository has a *machine-learning/tutorials* folder, and the samples for machine learning tutorials are in the *samples/machine-learning/tutorials* folder.

In addition, all samples under the *core* and *standard* folders should build and run on all platforms supported by .NET Core. Our CI build system will enforce that. The top level *framework* folder contains samples that are only built and validated on Windows.

Sample projects should build and run on the widest set of platforms possible for the given sample. In practice, that means building .NET Core-based console applications where possible. Samples that are specific to the web or a UI framework should add those tools as needed. Examples include web applications, mobile apps, WPF or WinForms apps, and so on.

We are working toward having a CI system in place for all code. When you make any updates to samples, make sure each update is part of a buildable project. Ideally, add tests for correctness on samples as well.

Each complete sample that you create should contain a *readme.md* file. This file should contain a short description of the sample (one or two paragraphs). Your *readme.md* should tell readers what they will learn by exploring this sample. The *readme.md* file should also contain a link to the live document on the [.NET documentation site](/dotnet/welcome). To determine where a given file in the repository maps to that site, replace `/docs` in the repository path with `https://learn.microsoft.com/dotnet`.

Your topic will also contain links to the sample. Link directly to the sample's folder on GitHub.

### Write a new sample

Samples are full programs and libraries meant for download. They may be small in scope, but they demonstrate concepts in a manner that enables people to explore and experiment on their own. The guidelines for samples ensure readers can download and explore. Examine the [Parallel LINQ (PLINQ)](https://github.com/dotnet/samples/tree/main/csharp/parallel/PLINQ) samples as an example of each of the guidelines.

1. Your sample **must be part of a buildable project**. Where possible, the projects should build on all platforms supported by .NET Core. Exceptions to this are samples that demonstrate a platform specific feature or platform specific tool.

2. Your sample should conform to the [runtime coding style](https://github.com/dotnet/runtime/blob/main/docs/coding-guidelines/coding-style.md) to maintain consistency.

   Additionally, we prefer the use of `static` methods rather than instance methods when demonstrating something that doesn't require instantiating a new object.

3. Your sample should include **appropriate exception handling**. It should handle all exceptions that are likely to be thrown in the context of the sample. For example, a sample that calls the [Console.ReadLine](/dotnet/api/system.console.readline) method to retrieve user input should use appropriate exception handling when the input string is passed as an argument to a method. Similarly, if your sample expects a method call to fail, the resulting exception must be handled. Always handle the specific exceptions thrown by the method, rather than base class exceptions such as [Exception](/dotnet/api/system.exception) or [SystemException](/dotnet/api/system.systemexception).

To create a sample:

1. File an [issue](https://github.com/dotnet/docs/issues) or add a comment to an existing one that you are working on it.
2. Write the topic that explains the concepts demonstrated in your sample (example: `docs/standard/linq/where-clause.md`).
3. Write your sample (example: `WhereClause-Sample1.cs`).
4. Create a Program.cs with a Main entry point that calls your samples. If there is already one there, add the call to your sample:

    ```csharp
    public class Program
    {
        public void Main(string[] args)
        {
            WhereClause1.QuerySyntaxExample();

            // Add the method syntax as an example.
            WhereClause1.MethodSyntaxExample();
        }
    }
    ```

You build any .NET snippet or sample using the .NET CLI, which can be installed with [the .NET SDK](https://www.microsoft.com/net/download). To build and run your sample:

1. Go to the sample folder and build to check for errors:

    ```dotnetcli
    dotnet build
    ```

2. Run your sample:

    ```dotnetcli
    dotnet run
    ```

3. Add a readme.md to the root directory of your sample.

   This should include a brief description of the code, and refer people to the article that references the sample. The top of the *readme.md* must have the metadata required for the [samples browser](/samples). The header block should contain the following fields:

   ```yml
   ---
   name: "really cool sample"
   description: "Learn everything about this really cool sample."
   page_type: sample
   languages:
     - csharp
     - fsharp
     - vbnet
   products:
     - dotnet-core
     - dotnet
     - dotnet-standard
     - aspnet
     - aspnet-core
     - ef-core
   ---
   ```

   - The `languages` collection should include only those languages available for your sample.
   - The `products` collection should include only those products relevant to your sample.

Except where noted, all samples build from the command line on any platform supported by .NET. There are a few samples that are specific to Visual Studio and require Visual Studio 2017 or later. In addition, some samples show platform specific features and will require a specific platform. Other samples and snippets require the .NET Framework and will run on Windows platforms, and will need the Developer Pack for the target Framework version.

## The C# interactive experience

All snippets included in an article use a [language tag](../code-in-docs.md) to indicate the source language. Short code snippets in C# can use the `csharp-interactive` language tag to specify a C# snippet that runs in the browser. (Inline code snippets use the `csharp-interactive` tag, for snippets included from source, use the `code-csharp-interactive` tag.) These code snippets display a **code window** and an **output window** in the article. The **output window** displays any output from executing the interactive code once the user has run the snippet.

The C# interactive experience changes how we work with snippets. Visitors can run the snippet to see the results. A number of factors help determine if the snippet or corresponding text should include information about the output.

### When to display the expected output without running the snippet

- Articles intended for beginners should provide output so that readers can compare the output of their work with the expected answer.
- Snippets where the output is integral to the topic should display that output. For example, articles on formatted text should show the text format without running the snippet.
- When both the snippet and the expected output is short, consider showing the output. It saves a bit of time.
- Articles explaining how current culture or invariant culture affect output should explain the expected output. The interactive REPL (Read Evaluate Print Loop) runs on a Linux-based host. The default culture, and the invariant culture produce different output on different operating systems and machines. The article should explain the output in Windows, Linux, and Mac systems.

### When to exclude expected output from the snippet

- Articles where the snippet generates a larger output should not include that in comments. It obscures the code once the snippet has been run.
- Articles where the snippet demonstrates a topic, but the output isn't integral to understanding it. For example, code that runs a LINQ query to explain query syntax and then display every item in the output collection.

> [!NOTE]
> You might notice that some of the topics are not currently following all the guidelines specified here. We're working towards achieving consistency throughout the site. Check the list of [open issues](https://github.com/dotnet/docs/issues?q=is%3Aopen+is%3Aissue+label%3A%22%3Abookmark_tabs%3A+Information+Architecture%22) we're currently tracking for that specific goal.

### Contributing to non-English content

Contributions for Machine Translated (MT) content are currently not accepted. In an effort to improve the quality of MT content, we've transitioned to a Neural MT engine. We accept and encourage contributions for Human Translated (HT) content, which is used to train the Neural MT engine. So over time, contributions to HT content will improve the quality of both HT and MT. MT topics will have a disclaimer stating that part of the topic may be MT, and the **Edit** button won't be displayed, as editing is disabled.

[!INCLUDE [note-docsitelocfeedback](../../includes/note-docsitelocfeedback.md)]

## Contributor license agreement

You must sign the [.NET Foundation Contribution License Agreement (CLA)](https://cla.dotnetfoundation.org) before your PR is merged. This is a one-time requirement for projects in the .NET Foundation. You can read more about [Contribution License Agreements (CLA)](http://en.wikipedia.org/wiki/Contributor_License_Agreement) on Wikipedia.

The agreement: [.NET Foundation Contributor License Agreement (CLA)](https://github.com/dotnet/home/blob/master/guidance/net-foundation-contribution-license-agreement.pdf)

You don't have to sign the agreement up-front. You can clone, fork, and submit your PR as usual. When your PR is created, it is classified by a CLA bot. If the change is small (for example, you fixed a typo), then the PR is labeled with `cla-not-required`. Otherwise, it's classified as `cla-required`. Once you signed the CLA, the current and all future pull requests are labeled as `cla-signed`.
