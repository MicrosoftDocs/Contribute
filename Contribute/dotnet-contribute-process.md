---
title: Contribution process for .NET docs repositories
description: This article provides a brief introduction to contributing to the .NET docs repositories. You'll learn the repositories used, the process for organizing content, and the policies for managing code samples and other assets.
ms.date: 11/07/2018
---
# Process for contributing to .NET docs

We appreciate community contributions to docs. The following list shows some guiding rules that you should keep in mind when you're contributing to the .NET documentation:

- **DON'T** surprise us with large pull requests. Instead, file an issue and start a discussion so we can agree on a direction before you invest a large amount of time.
- **DO** follow these instructions and [voice and tone](dotnet-voice-tone.md) guidelines.
- **DO** use the [template](dotnet-style-guide.md) file as the starting point of your work.
- **DO** create a separate branch on your fork before working on the articles.
- **DO** follow the [GitHub Flow workflow](https://guides.github.com/introduction/flow/).
- **DO** blog and tweet (or whatever) about your contributions, frequently!

Following these guidelines will ensure a better experience for you and for us.

## Make a contribution to .NET docs

**Step 1:** Skip this step for small changes. If you're interested in writing new content or in thoroughly revising existing content, open an [issue](https://github.com/dotnet/docs/issues) describing what you want to do.

The content inside the **docs** folder is organized into sections that are reflected in the Table of Contents (TOC). Define where the topic will be located in the TOC. Get feedback on your proposal.

-or-

You can also choose from existing issues for which community contributions are welcome. [Projects for .NET Community contributors](https://github.com/dotnet/docs/projects/35) lists many of the issues that are available for community contributors. Depending on your interests and level of commitment, you can choose from issues in the following categories:

- **Maintenance**. This category includes fairly simple contributions, such as fixing broken or incorrect links, adding missing code examples, or addressing limited content issues. In some cases, these issues may concern large numbers of files. In that case, you should let us know what you'd like to work on before you begin. Add a comment on the issue to tell us that you are working on it.

- **Content updates**. Given the enormity of the doc set, content easily becomes outdated and requires revision. In addition, for a variety of reason, some content has been duplicated or even triplicated. Updating content involves making sure that individual topics are current or revising content in a feature area to eliminate duplication and ensure that all unique content is preserved in the smaller documentation set.

- **New content authoring**. If you're interested in authoring your own topic, these issues list topics that we know we'd like to add to our doc set. Let us know before you begin working on a topic, though. If you're interested in writing a topic that isn't listed here, open an issue.

You can also look at our [open issues](https://github.com/dotnet/docs/issues) list and volunteer to work on the ones you're interested in. We use the [up-for-grabs](https://github.com/dotnet/docs/labels/up-for-grabs) label to tag issues identified for community contribution. These usually require minimal context and are well-suited for first issues. We encourage experienced contributors in our community to look at any issues of interest. When you find one, add a comment to ask if it's open.

Once you've picked a task to work on, follow the [get started](get-started-setup-github.md) guide to create a GitHub account and setup your environment.

**Step 2:** Fork the `/dotnet/docs`, `dotnet/samples`, `dotnet/dotnet-api-docs`, `dotnet/roslyn-api-docs`, or `dotnet/ml-api-docs` repos as needed and create a branch for your changes.

For small changes, see the instructions on editing in GitHub on the [home page](index.md#quick-edits-to-existing-documents) of the contributor guide.

**Step 3:** Make the changes on this new branch.

If it's a new topic, you can use this [template file](dotnet-style-guide.md) as your starting point. It contains the writing guidelines and also explains the metadata required for each article, such as author information.

Navigate to the folder that corresponds to the TOC location determined for your article in step 1. That folder contains the Markdown files for all articles in that section. If necessary, create a new folder to place the files for your content. The main article for that section is called *index.md*. For images and other static resources, create a subfolder called **media** inside the folder that contains your article, if it doesn't already exist. Inside the **media** folder, create a subfolder with the article name (except for the index file). Sample code should be in the `dotnet/samples` repo, as described in the section on [samples](#contributing-to-samples).

Be sure to follow the proper Markdown syntax. For examples of common , see the [template and markdown cheatsheet](dotnet-style-guide.md).

## Example structure

    docs
      /about
      /core
        /porting
          porting-overview.md
          /media
            /porting-overview
                portability_report.png

**Step 4:** Submit a Pull Request (PR) from your branch to the master branch.

> [!IMPORTANT]
> The [comment automation](how-to-write-workflows-major.md#review-and-sign-off) functionality is not available on any of the .NET docs repositories at this time. Members of the .NET docs team will review and merge your PR.

Each PR should usually address one issue at a time. The PR can modify one or multiple files. If you're addressing multiple fixes on different files, separate PRs are preferred. If you are creating samples as well as updating markdown, you'll need to create a separate PR for samples.

If your PR fixes an existing issue, add the `Fixes #Issue_Number` keyword to the commit message or PR description. That way, the issue is automatically closed when the PR is merged. For more information, see [Closing issues via commit messages](https://help.github.com/articles/closing-issues-via-commit-messages/).

The .NET team will review your PR and let you know if there are any other updates/changes necessary in order to approve it.

**Step 5:** Make any necessary updates to your branch as discussed with the team.

The maintainers will merge your PR into the master branch once feedback has been applied and your change is approved.

We regularly push all commits from master branch into the live branch and then you'll be able to see your contribution live at https://docs.microsoft.com/dotnet/. We typically publish daily during the work week. Maintenance activities may delay publishing for a few days.

## Contributing to samples

The [dotnet/samples](https://github.com/dotnet/samples) repo contains all the sample code that is part of any topic under the .NET documentation. There are several different projects that are organized in sub-folders. These sub-folders are organized similarly to the organization of the docs for .NET.

We make the following distinction for code that exists in our repository:

- Samples: readers can download and run the samples. All samples should be complete applications or libraries. Where the sample creates a library, it should include unit tests or an application that lets readers run the code. They often use more than one technology, feature, or toolkit. The readme.md file for each sample will refer to the article so that you can read more about the concepts covered in each sample.
- Snippets: illustrate a smaller concept or task. They compile but they are not intended to be complete applications. They should run correctly, but aren't an example application for a typical scenario. Instead, they are designed to be as small as possible to illustrate a single concept or feature. These should be no more than a single screen of code.

Code all lives in the [dotnet/samples](https://github.com/dotnet/samples) repository. We are working toward a model where our samples folder structure matches our docs folder structure. Standards that we follow are:

- The top level *snippets* folder contains snippets for small, focused samples.
- API reference samples are placed in a folder following this pattern: *snippets/\<language>/api/\<namespace>/\<apiname>*.
- Other top-level folders match the top level folders in the *docs* repository. For example, the docs repository has a *machine-learning/tutorials* folder, and the samples for machine learning tutorials are in the *samples/machine-learning/tutorials* folder.

In addition, all samples under the *core* and *standard* folders should build and run on all platforms supported by .NET Core. Our CI build system will enforce that. The top level *framework* folder contains samples that are only built and validated on Windows.

Sample projects should build and run on the widest set of platforms possible for the given sample. In practice, that means building .NET Core-based console applications where possible. Samples that are specific to the web or a UI framework should add those tools as needed. Examples include web applications, mobile apps, WPF or WinForms apps, and so on.

We are working toward having a CI system in place for all code. When you make any updates to samples, make sure each update is part of a buildable project. Ideally, add tests for correctness on samples as well.

Each complete sample that you create should contain a *readme.md* file. This file should contain a short description of the sample (one or two paragraphs). Your *readme.md* should tell readers what they will learn by exploring this sample. The *readme.md* file should also contain a link to the live document on the [.NET documentation site](https://docs.microsoft.com/dotnet/welcome). To determine where a given file in the repository maps to that site, replace `/docs` in the repository path with `http://docs.microsoft.com/dotnet`.

Your topic will also contain links to the sample. Link directly to the sample's folder on GitHub.

### Writing a new snippet or sample

1. Your sample **must be part of a buildable project**. Where possible, the projects should build on all platforms supported by .NET Core. Exceptions to this are samples that demonstrate a platform specific feature or platform specific tool.

2. Your sample should conform to the [corefx coding style](https://github.com/dotnet/corefx/blob/master/Documentation/coding-guidelines/coding-style.md) to maintain consistency.

	- Additionally, we prefer the use of `static` methods rather than instance methods when demonstrating something that doesn't require instantiating a new object.

3. Your sample should include **appropriate exception handling**. It should handle all exceptions that are likely to be thrown in the context of the sample. For example, a sample that calls the [Console.ReadLine](https://docs.microsoft.com/dotnet/api/system.console.readline) method to retrieve user input should use appropriate exception handling when the input string is passed as an argument to a method. Similarly, if your sample expects a method call to fail, the resulting exception must be handled. Always handle the specific exceptions thrown by the method, rather than base class exceptions such as [Exception](https://docs.microsoft.com/dotnet/api/system.exception) or [SystemException](https://docs.microsoft.com/dotnet/api/system.systemexception).

4. If your sample builds a standalone package, you must include the runtimes used by our CI build system, in addition to any runtimes used by your sample:
    - `win7-x64`
    - `win8-x64`
    - `win81-x64`
    - `ubuntu.16.04-x64`

We will have a CI system in place to build these projects shortly.

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

    ```console
    dotnet build
    ```
2. Run your sample:

    ```console
    dotnet run
    ```

3. Add a readme.md to the root directory of your sample. 

   This should include a brief description of the code, and refer people to the article that references the sample.

Except where noted, all samples build from the command line on any platform supported by .NET Core. There are a few samples that are specific to Visual Studio and require Visual Studio 2017 or later. In addition, some samples show platform specific features and will require a specific platform. Other samples and snippets require the .NET Framework and will run on Windows platforms, and will need the Developer Pack for the target Framework version.

## The C# interactive experience

All samples included in an article use a [language tag](how-to-write-markdown.md#code-snippets) to indicate the source language. Short code samples in C# can use the `csharp-interactive` language tag to specify a C# sample that runs in the browser. (Inline code samples use the `csharp-interactive` tag, for snippets included from source, use the `code-csharp-interactive` tag.) These code samples display a code window and an output window in the article. The output window displays any output from executing the interactive code once the user has run the sample.

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

## Contributor license agreement

You must sign the [.NET Foundation Contribution License Agreement (CLA)](https://cla.dotnetfoundation.org) before your PR is merged. This is a one-time requirement for projects in the .NET Foundation. You can read more about [Contribution License Agreements (CLA)](http://en.wikipedia.org/wiki/Contributor_License_Agreement) on Wikipedia.

The agreement: [net-foundation-contribution-license-agreement.pdf](https://github.com/dotnet/home/blob/master/guidance/net-foundation-contribution-license-agreement.pdf)

You don't have to sign the agreement up-front. You can clone, fork, and submit your PR as usual. When your PR is created, it is classified by a CLA bot. If the change is small (for example, you fixed a typo), then the PR is labeled with `cla-not-required`. Otherwise, it's classified as `cla-required`. Once you signed the CLA, the current and all future pull requests are labeled as `cla-signed`.
