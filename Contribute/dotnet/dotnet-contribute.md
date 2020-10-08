---
title: Contribute to the .NET docs repositories
description: This article describes the process for contributing to the articles and code samples in the repositories that make up the .NET documentation.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
ms.date: 05/14/2020
---
# Learn how to contribute to the .NET docs repositories

Thank you for your interest in contributing to the .NET documentation!

This document covers the process for contributing to the articles and code samples that are hosted on the [.NET documentation site](https://docs.microsoft.com/dotnet). Contributions may be as simple as typo corrections or as complex as new articles.

The .NET documentation site is built from multiple repositories:

- [.NET conceptual articles and code snippets](https://github.com/dotnet/docs)
- [Code samples and snippets](https://github.com/dotnet/samples)
- [.NET Standard, .NET Core, .NET Framework API reference](https://github.com/dotnet/dotnet-api-docs)
- [.NET Compiler Platform SDK reference](https://github.com/dotnet/roslyn-api-docs)
- [ML.NET API reference](https://github.com/dotnet/ml-api-docs)

Issues for all these repositories are tracked in the [dotnet/docs](https://github.com/dotnet/docs/issues) repository.

## Guidelines for contributions

We appreciate community contributions to docs. The following list shows some guiding rules to keep in mind when you're contributing to the .NET documentation:

- **DON'T** surprise us with large pull requests. Instead, file an issue and start a discussion so we can agree on a direction before you invest a large amount of time.
- **DO** follow these instructions and [voice and tone](dotnet-voice-tone.md) guidelines.
- **DO** use the [template](dotnet-style-guide.md) file as the starting point of your work.
- **DO** create a separate branch on your fork before working on the articles.
- **DO** follow the [GitHub flow](https://guides.github.com/introduction/flow/).
- **DO** blog and tweet (or whatever) about your contributions if you like!

Following these guidelines will ensure a better experience for you and for us.

## Make a contribution to .NET docs

**Step 1:** If you're interested in writing new content or in thoroughly revising existing content, open an [issue](https://github.com/dotnet/docs/issues) describing what you want to do. The content inside the **docs** folder is organized into sections that are reflected in the Table of Contents (TOC). Define where the topic will be located in the TOC. Get feedback on your proposal.

-or-

Choose an existing issue and address it. You can look at our [open issues](https://github.com/dotnet/docs/issues) list and volunteer to work on the ones you're interested in:

- Filter by the [good-first-issue](https://github.com/dotnet/docs/labels/good-first-issue) label for, well, good first issues.
- Filter by the [up-for-grabs](https://github.com/dotnet/docs/labels/up-for-grabs) label for issues appropriate for community contribution. These issues usually require minimal context.
- Experienced contributors can tackle any issues of interest.

When you find an issue to work on, add a comment to ask if it's open.

Once you've picked a task to work on, follow the [get started](../get-started-setup-github.md) guide to create a GitHub account and set up your environment.

**Step 2:** Fork the `/dotnet/docs`, `dotnet/samples`, `dotnet/dotnet-api-docs`, `dotnet/roslyn-api-docs`, or `dotnet/ml-api-docs` repos as needed and create a branch for your changes.

For small changes, see the instructions on editing in GitHub on the [home page](../index.md#quick-edits-to-existing-documents) of the contributor guide.

**Step 3:** Make the changes on this new branch.

If it's a new topic, you can use this [template file](dotnet-style-guide.md) as your starting point. It contains the writing guidelines and also explains the metadata required for each article, such as author information. For more information on the Markdown syntax used in the docs.microsoft.com site, see [Markdown reference](../markdown-reference.md).

Navigate to the folder that corresponds to the TOC location determined for your article in step 1. That folder contains the Markdown files for all articles in that section. If necessary, create a new folder to place the files for your content. The main article for that section is called *index.md*.

For images and other static resources, create a subfolder called **media** inside the folder that contains your article, if it doesn't already exist. Inside the **media** folder, create a subfolder with the article name (except for the index file).

For **code snippets**, create a subfolder called **snippets** inside the folder that contains your article, if it doesn't already exist. Inside the **snippets** folder, create a subfolder with the article name. In most cases, you'll have code snippets for all three of the main .NET languages, C#, F#, and Visual Basic. In that case, create subfolders named **csharp**, **fsharp**, and **vb** for each of the three projects. If you're creating a snippet for an article under the [docs/csharp](https://github.com/dotnet/docs/tree/master/docs/csharp), [docs/fsharp](https://github.com/dotnet/docs/tree/master/docs/fsharp), or [docs/visual-basic](https://github.com/dotnet/docs/tree/master/docs/visual-basic) folders, the snippet will only be in one language so you can omit the language subfolder.

Code snippets are small, focused examples of code that demonstrate the concepts covered in an article. Larger programs intended for download and exploration should be located in the [dotnet/samples](https://github.com/dotnet/samples) repository. Full samples are covered in the section on [Contributing to samples](#contribute-to-samples).

### Contribute .NET analyzer docs

.NET compiler platform (Roslyn) analyzers inspect your C# or Visual Basic code for code quality and code style issues. Starting in .NET 5.0, these analyzers are [included with the .NET SDK](/dotnet/fundamentals/code-analysis/overview).

- [Code quality analysis ("CAxxxx" rules)](/dotnet/fundamentals/code-analysis/overview#code-quality-analysis):
  - Implemented [here](https://github.com/dotnet/roslyn-analyzers/tree/master/src/NetAnalyzers) in `dotnet/roslyn-analyzers` repo.
  - Documented [here](https://github.com/dotnet/docs/blob/master/docs/fundamentals/code-analysis/quality-rules) in the `dotnet/docs` repo. See [Contribute docs for 'CAxxxx' rules](#contribute-docs-for-caxxxx-rules).
- [Code style analysis ("IDExxxx" rules)](/dotnet/fundamentals/code-analysis/overview#code-style-analysis):
  - Implemented [here](https://github.com/dotnet/roslyn/tree/master/src/Analyzers) in `dotnet/roslyn` repo.
  - Documented [here](https://github.com/dotnet/docs/blob/master/docs/fundamentals/code-analysis/style-rules) in the `dotnet/docs` repo. See [Contribute docs for 'IDExxxx' rules](#contribute-docs-for-idexxxx-rules).

#### Contribute docs for 'CAxxxx' rules

Please follow the following steps to contribute documentation for code quality analysis rules to the [dotnet/docs](https://github.com/dotnet/docs) repo:

1. Determine `Rule ID` and `Category`: Ensure that you know the 'CAxxxx' rule ID and category for the rule to be documented. This means either your CA analyzer has been merged into [dotnet/roslyn-analyzers](https://github.com/dotnet/roslyn-analyzers) repo or you have an open PR with an approved ID and category that has been assigned to the rule.
2. Add an entry for the rule to following tables:
  1. In [table of contents](https://github.com/dotnet/docs/blob/master/docs/fundamentals/toc.yml) file under the rule category list. For example, for a CA rule with `Performance` category, search for the term `- name: Performance rules` in the file and add an entry to the list. If none exists, create a new category list under `- name: Code quality rules`.
  2. In [top-level rule index](https://github.com/dotnet/docs/blob/master/docs/fundamentals/code-analysis/quality-rules/index.md) file.
  3. In `category` based rule index file:
    1. Identify the category based index file under [root](https://github.com/dotnet/docs/blob/master/docs/fundamentals/code-analysis/quality-rules) folder. For example, for a CA rule with `Performance` category, this file is named `performance-warnings.md`. If none exists, create a new category based index file by cloning an existing one.
    2. Add an entry for the rule ID in this file.
3. Add rule doc:
  1. Clone an existing CA rule file under [root](https://github.com/dotnet/docs/blob/master/docs/fundamentals/code-analysis/quality-rules) folder, say `ca1000.md`, and rename it.
  2. Update the content of the file appropriately.

> [!TIP]
> Perform a repo search in the `dotnet/docs` repo for a known, existing CA rule ID to identify potential places that might need an update. For example, see <https://github.com/dotnet/docs/search?q=CA2000>.

#### Contribute docs for 'IDExxxx' rules

Please follow the following steps to contribute documentation for code style analysis rules to the [dotnet/docs](https://github.com/dotnet/docs) repo:

1. Determine `Rule ID` and code style options, if any: Ensure that you know the 'IDExxxx' rule ID and code style options for the rule to be documented. This means either the IDE analyzer has been merged into the [dotnet/roslyn](https://github.com/dotnet/roslyn) repo or you have an open PR with an approved ID and code style options that have been assigned to the rule.
2. Determine rule `subcategory`: IDE rules have category `Style`. Identify the rule subcategory by reading through the introductory section of [Code style rules](/dotnet/fundamentals/code-analysis/style-rules/index). Most of the IDE code style rules are under the `Language` subcategory.
3. Determine rule `preference group`: Identify the `preference group` for the rule by reading through the preferences headers [here](/dotnet/fundamentals/code-analysis/style-rules/language-rules#net-style-rules).
  - If the rule has known, associated code style option(s), the preferences group will match the `OptionGroup` specified in the code style option declaration.
  - Otherwise, determine if the rule belongs to an existing preference group or needs a new preference group.
4. Add an entry for the IDE rule and/or code style option(s) to the following tables:
  1. In [table of contents](https://github.com/dotnet/docs/blob/master/docs/fundamentals/toc.yml) file under the rule's sub-category and preferences list. For example, for an IDE code style rule with `Language` subcategory and `Modifier preferences` group, search for the term `- name: Language rules` and a child node `- name: Modifier preferences` in the file and add an entry to the list. If either the subcategory list or the preferences list under the subcategory does not exist, create a new one under `- name: Code style rules`.
  2. In the [code style option-based index](https://github.com/dotnet/docs/blob/master/docs/fundamentals/code-analysis/style-rules/language-rules.md) file.
  3. In the [rule ID-based index](https://github.com/dotnet/docs/blob/master/docs/fundamentals/code-analysis/style-rules/index.md) file.
  4. In `preferences group` based rule index file:
    1. Identify the preferences group based index file under [root](https://github.com/dotnet/docs/blob/master/docs/fundamentals/code-analysis/style-rules) folder. For example, for an IDE rule for `Modifier preferences`, this file is named `modifier-preferences.md`. If none exists, create a new preferences group based index file by cloning an existing one.
    2. Add an entry for the rule ID in this file.
5. Add rule doc:
  1. Clone an existing IDE rule file under [root](https://github.com/dotnet/docs/blob/master/docs/fundamentals/code-analysis/style-rules) folder, say `ide0011.md`, and rename it.
  2. Update the content of the file appropriately.

> [!TIP]
> Perform a repo search in the `dotnet/docs` repo, for a known, existing IDE rule and/or code style option(s) to identify potential places that might need an update. For example, see <https://github.com/dotnet/docs/search?q=IDE0011> and <https://github.com/dotnet/docs/search?q=csharp_prefer_braces>.

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
```

> [!NOTE]
> The language folders under snippets are not needed in the language guide area, where only one language is assumed.

The structure shown above includes one image, *portability_report.png*, and three code projects that include **code snippets** that are included in the *porting-overview.md* article. An accepted alternative structure contains one project per language that contains all snippets for all articles in that folder. This alternative has been used in the language reference areas because of very small snippets to demonstrate language syntax. It is discouraged in other areas.

For historical reasons, many of the included snippets are stored under the */samples* folder in the *dotnet/docs* repository. If you're making major changes to an article, those snippets should be moved to the new structure. Do not move snippets for small changes.

**Step 4:** Submit a Pull Request (PR) from your branch to the master branch.

> [!IMPORTANT]
> The [comment automation](../how-to-write-workflows-major.md#review-and-sign-off) functionality is not available on any of the .NET docs repositories at this time. Members of the .NET docs team will review and merge your PR.

Each PR should usually address one issue at a time. The PR can modify one or multiple files. If you're addressing multiple fixes on different files, separate PRs are preferred. If you're creating samples as well as updating markdown, you'll need to create a separate PR for samples.

If your PR fixes an existing issue, add the `Fixes #Issue_Number` keyword to the commit message or PR description. That way, the issue is automatically closed when the PR is merged. For more information, see [Closing issues via commit messages](https://help.github.com/articles/closing-issues-via-commit-messages/).

The .NET team will review your PR and let you know if there are any other updates/changes necessary in order to approve it.

**Step 5:** Make any necessary updates to your branch as discussed with the team.

The maintainers will merge your PR into the master branch once feedback has been applied and your change is approved.

We regularly push all commits from master branch into the live branch and then you'll be able to see your contribution live at https://docs.microsoft.com/dotnet/. We typically publish daily during the work week.

## Contribute to samples

We make the following distinction for code that supports our content:

- Samples: readers can download and run the samples. All samples should be complete applications or libraries. Where the sample creates a library, it should include unit tests or an application that lets readers run the code. They often use more than one technology, feature, or toolkit. The readme.md file for each sample will refer to the article so that you can read more about the concepts covered in each sample.
- Snippets: illustrate a smaller concept or task. They compile but they are not intended to be complete applications. They should run correctly, but aren't an example application for a typical scenario. Instead, they are designed to be as small as possible to illustrate a single concept or feature. These should be no more than a single screen of code.

Samples are stored in the [dotnet/samples](https://github.com/dotnet/samples) repository. We are working toward a model where our samples folder structure matches our docs folder structure. Standards that we follow are:

- Top-level folders match the top level folders in the *docs* repository. For example, the docs repository has a *machine-learning/tutorials* folder, and the samples for machine learning tutorials are in the *samples/machine-learning/tutorials* folder.

In addition, all samples under the *core* and *standard* folders should build and run on all platforms supported by .NET Core. Our CI build system will enforce that. The top level *framework* folder contains samples that are only built and validated on Windows.

Sample projects should build and run on the widest set of platforms possible for the given sample. In practice, that means building .NET Core-based console applications where possible. Samples that are specific to the web or a UI framework should add those tools as needed. Examples include web applications, mobile apps, WPF or WinForms apps, and so on.

We are working toward having a CI system in place for all code. When you make any updates to samples, make sure each update is part of a buildable project. Ideally, add tests for correctness on samples as well.

Each complete sample that you create should contain a *readme.md* file. This file should contain a short description of the sample (one or two paragraphs). Your *readme.md* should tell readers what they will learn by exploring this sample. The *readme.md* file should also contain a link to the live document on the [.NET documentation site](https://docs.microsoft.com/dotnet/welcome). To determine where a given file in the repository maps to that site, replace `/docs` in the repository path with `https://docs.microsoft.com/dotnet`.

Your topic will also contain links to the sample. Link directly to the sample's folder on GitHub.

### Write a new sample

Samples are full programs and libraries meant for download. They may be small in scope, but they demonstrate concepts in a manner that enables people to explore and experiment on their own. The guidelines for samples ensure readers can download and explore. Examine the [Parallel LINQ (PLINQ)](https://github.com/dotnet/samples/tree/master/csharp/parallel/PLINQ) samples as an example of each of the guidelines.

1. Your sample **must be part of a buildable project**. Where possible, the projects should build on all platforms supported by .NET Core. Exceptions to this are samples that demonstrate a platform specific feature or platform specific tool.

2. Your sample should conform to the [corefx coding style](https://github.com/dotnet/corefx/blob/master/Documentation/coding-guidelines/coding-style.md) to maintain consistency.

   Additionally, we prefer the use of `static` methods rather than instance methods when demonstrating something that doesn't require instantiating a new object.

3. Your sample should include **appropriate exception handling**. It should handle all exceptions that are likely to be thrown in the context of the sample. For example, a sample that calls the [Console.ReadLine](https://docs.microsoft.com/dotnet/api/system.console.readline) method to retrieve user input should use appropriate exception handling when the input string is passed as an argument to a method. Similarly, if your sample expects a method call to fail, the resulting exception must be handled. Always handle the specific exceptions thrown by the method, rather than base class exceptions such as [Exception](https://docs.microsoft.com/dotnet/api/system.exception) or [SystemException](https://docs.microsoft.com/dotnet/api/system.systemexception).

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

You build any .NET Core snippet or sample using the .NET Core CLI, which can be installed with [the .NET Core SDK](https://www.microsoft.com/net/download). To build and run your sample:

1. Go to the sample folder and build to check for errors:

    ```dotnetcli
    dotnet build
    ```

2. Run your sample:

    ```dotnetcli
    dotnet run
    ```

3. Add a readme.md to the root directory of your sample.

   This should include a brief description of the code, and refer people to the article that references the sample. The top of the *readme.md* must have the metadata required for the [samples browser](https://docs.microsoft.com/samples). The header block should contain the following fields:

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

Except where noted, all samples build from the command line on any platform supported by .NET Core. There are a few samples that are specific to Visual Studio and require Visual Studio 2017 or later. In addition, some samples show platform specific features and will require a specific platform. Other samples and snippets require the .NET Framework and will run on Windows platforms, and will need the Developer Pack for the target Framework version.

## The C# interactive experience

All samples included in an article use a [language tag](../code-in-docs.md) to indicate the source language. Short code samples in C# can use the `csharp-interactive` language tag to specify a C# sample that runs in the browser. (Inline code samples use the `csharp-interactive` tag, for snippets included from source, use the `code-csharp-interactive` tag.) These code samples display a code window and an output window in the article. The output window displays any output from executing the interactive code once the user has run the sample.

The C# interactive experience changes how we work with samples. Visitors can run the sample to see the results. A number of factors help determine if the sample or corresponding text should include information about the output.

### When to display the expected output without running the sample

- Articles intended for beginners should provide output so that readers can compare the output of their work with the expected answer.
- Samples where the output is integral to the topic should display that output. For example, articles on formatted text should show the text format without running the sample.
- When both the sample and the expected output is short, consider showing the output. It saves a bit of time.
- Articles explaining how current culture or invariant culture affect output should explain the expected output. The interactive REPL (Read Evaluate Print Loop) runs on a Linux-based host. The default culture, and the invariant culture produce different output on different operating systems and machines. The article should explain the output in Windows, Linux, and Mac systems.

### When to exclude expected output from the sample

- Articles where the sample generates a larger output should not include that in comments. It obscures the code once the sample has been run.
- Articles where the sample demonstrates a topic, but the output isn't integral to understanding it. For example, code that runs a LINQ query to explain query syntax and then display every item in the output collection.

> [!NOTE]
> You might notice that some of the topics are not currently following all the guidelines specified here. We're working towards achieving consistency throughout the site. Check the list of [open issues](https://github.com/dotnet/docs/issues?q=is%3Aopen+is%3Aissue+label%3A%22%3Abookmark_tabs%3A+Information+Architecture%22) we're currently tracking for that specific goal.

### Contributing to International content

Contributions for Machine Translated (MT) content are currently not accepted. In an effort to improve the quality of MT content, we've transitioned to a Neural MT engine. We accept and encourage contributions for Human Translated (HT) content, which is used to train the Neural MT engine. So over time, contributions to HT content will improve the quality of both HT and MT. MT topics will have a disclaimer stating that part of the topic may be MT, and the **Edit** button won't be displayed, as editing is disabled.

## Contributor license agreement

You must sign the [.NET Foundation Contribution License Agreement (CLA)](https://cla.dotnetfoundation.org) before your PR is merged. This is a one-time requirement for projects in the .NET Foundation. You can read more about [Contribution License Agreements (CLA)](http://en.wikipedia.org/wiki/Contributor_License_Agreement) on Wikipedia.

The agreement: [net-foundation-contribution-license-agreement.pdf](https://github.com/dotnet/home/blob/master/guidance/net-foundation-contribution-license-agreement.pdf)

You don't have to sign the agreement up-front. You can clone, fork, and submit your PR as usual. When your PR is created, it is classified by a CLA bot. If the change is small (for example, you fixed a typo), then the PR is labeled with `cla-not-required`. Otherwise, it's classified as `cla-required`. Once you signed the CLA, the current and all future pull requests are labeled as `cla-signed`.
