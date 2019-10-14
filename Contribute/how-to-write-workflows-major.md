---
title: GitHub contribution workflow for major or long-running changes
description: This article shows you how to use the "major" contributor workflow to make contributions to docs.microsoft.com articles.
ms.date: 08/30/2017
---
# GitHub contribution workflow for major or long-running changes

> [!IMPORTANT]
> All repositories that publish to docs.microsoft.com have adopted either the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/) or the [.NET Foundation Code of Conduct](https://dotnetfoundation.org/code-of-conduct). For more information, see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/). Or contact [opencode@microsoft.com](mailto:opencode@microsoft.com), or [conduct@dotnetfoundation.org](mailto:conduct@dotnetfoundation.org) with any questions or comments.<br>
>
> Minor corrections or clarifications to documentation and code examples in public repositories are covered by the [docs.microsoft.com Terms of Use](https://docs.microsoft.com/legal/termsofuse). New or significant changes will generate a comment in the pull request, asking you to submit an online Contribution License Agreement (CLA) if you are not an employee of Microsoft. You will need to complete the online form before your pull request can be merged.

## Overview

This workflow is suitable for a contributor who needs to make a major change or will be a frequent contributor to a repository. Frequent contributors typically have ongoing (long-running) changes, which go through multiple build/validation/staging cycles or span multiple days before pull request sign-off and merge.

Examples of these types of contributions include:

[!INCLUDE[contribute-major-changes-change-definition](includes/contribute-how-to-write-workflows-major-change-definition.md)]

### Terminology

Before you start, let's review some of the Git/GitHub terms and monikers used in this workflow. Don't worry about understanding them now. Just know that you will be learning about them, and you can refer back to this section when you need to verify a definition.

| Name | Description |
|-----------|-------------|
|fork|Normally used as a noun, when referring to a copy of a main GitHub repository. In practice, a fork is just another repository. But it's special in the sense that GitHub maintains a connection back to the main/parent repository. It's sometimes used as a verb, as in "You must fork the repository first."|
|remote|A named connection to a remote repository, such as the "origin" or "upstream" remote. Git refers to this as remote because it is used to reference a repository that's hosted on another computer. In this workflow, a remote is always a GitHub repository.|
|origin|The name assigned to the connection between your local repository and the repository from which it was cloned. In this workflow, origin represents the connection to your fork. It's sometimes used as a moniker for the origin repository itself, as in "Remember to push your changes to origin."|
|upstream|Like the origin remote, upstream is a named connection to another repository. In this workflow, upstream represents the connection between your local repository and the main repository, from which your fork was created. It's sometimes used as a moniker for the upstream repository itself, as in "Remember to pull the changes from upstream."|

## Workflow

>[!IMPORTANT]
> If you haven't already, you must complete the steps in the [Setup](get-started-setup-github.md) section. This section walks you through setting up your GitHub account, installing Git Bash and a Markdown editor, creating a fork, and setting up your local repository. If you are unfamiliar with Git and GitHub concepts such as a repository or branch, please first review [Git and GitHub fundamentals](git-github-fundamentals.md).

In this workflow, changes flow in a repetitive cycle. Starting from your device's local repository, they flow back up to your GitHub fork, into the main GitHub repository, and back down locally again as you incorporate changes from other contributors.

### Use GitHub flow

Recall from [Git and GitHub fundamentals](git-github-fundamentals.md#git) that a Git repository contains a master branch, plus any additional work-in-progress branches that have not been integrated into master. Whenever you introduce a set of logically related changes, it’s a best practice to create a *working branch* to manage your changes through the workflow. We refer to it here as a working branch because it's a workspace to iterate/refine changes, until they can be integrated back into the master branch.

Isolating related changes to a specific branch allows you to control and introduce those changes independently, targeting them to a specific release time in the publishing cycle. In reality, depending on the type of work you do, you can easily end up with several working branches in your repository. It's not uncommon to be working on multiple branches at the same time, each representing a different project.

>[!TIP]
>Making your changes in the master branch is *not* a good practice. Imagine that you use the master branch to introduce a set of changes for a timed feature release. You finish the changes and are waiting to release them. Then in the interim, you have an urgent request to fix something, so you make the change to a file in the master branch and then publish the change. In this example, you inadvertently publish both the fix *and* the changes that you were holding for release on a specific date.

Now let's create a new working branch in your local repository, to capture your proposed changes. Each git client is different, so consult the help for your preferred client. You can see an overview of the process in the GitHub Guide on [GitHub flow](https://guides.github.com/introduction/flow/).

[!INCLUDE[contribute-how-to-write-workflows-pull-request-processing](includes/contribute-how-to-write-workflows-pull-request-processing.md)]

## Next steps

That's it! You've made a contribution to docs.microsoft.com content!

- To learn more about topics such as Markdown and Markdown extensions syntax, continue to the [Writing essentials](how-to-write-use-markdown.md) article.
