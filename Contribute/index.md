---
title: Microsoft Docs contributor guide overview
description: The guide describes how you can contribute to the Microsoft documentation site docs.microsoft.com.
author: bryanla
ms.author: bryanla
manager: mbaldwin
ms.date: 04/17/2018
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.custom: external-contributor-guide
---

# Microsoft Docs contributor guide overview

Welcome to the [docs.microsoft.com](https://docs.microsoft.com) (Docs)
Contributor Guide!

Several of our documentation sets are Open Source, hosted on GitHub. More
teams are adopting this model all the time. We've chosen this model to
streamline and improve communication between the product team engineers,
the content teams, and our customers. Working in the open provides several
advantages:

- We plan in the open to get feedback on what docs are most needed.
- We review in the open to publish the most helpful content on our first release.
- We update in the open to make it easier to continuously improve the content.

The user experience on [docs.microsoft.com](https://docs.microsoft.com) integrates
[GitHub](https://github.com) workflows directly to make it even easier.

> [!IMPORTANT]
> All repositories that publish to docs.microsoft.com have adopted either the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/) or the [.NET Foundation Code of Conduct](https://dotnetfoundation.org/code-of-conduct). For more information, see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/). Or contact [opencode@microsoft.com](mailto:opencode@microsoft.com), or [conduct@dotnetfoundation.org](mailto:conduct@dotnetfoundation.org) with any questions or comments.<br>
>
> Minor corrections or clarifications to documentation and code examples in public repositories are covered by the [docs.microsoft.com Terms of Use](https://docs.microsoft.com/legal/termsofuse). New or significant changes will generate a comment in the pull request, asking you to submit an online Contribution License Agreement (CLA) if you are not an employee of Microsoft. We need you to complete the online form before we can accept your pull request.

## Quick edits to existing documents

Quick edits streamline the process to report and fix small errors and
omissions in documents. Try as we do, small grammar and spelling errors
do make their way into our published documents. While you can create issues
to report this mistakes, you can save both yourself and us time by cretaing
a pull request (PR) to fix the issue. Every article displays an edit button
as shown in the following figure. Clicking this takes you to the source
on GitHub.

![Location of the Edit link](./media/index/edit-article.png)

Next, click the pencil icon, shown in the figure below, to edit the article.

If the pencil icon is grayed out, you need to login to your GitHub account,
or create a new account. Make your changes in the web editor. You can click
the **Preview changes** tab to check formatting of your change.

![Location of the pencil icon](./media/index/editicon.png)

Once you have made your changes, scroll to the bottom of the page. Enter a
title and description for your PR and click **Propose file change**
as shown in the following figure:

![proposing your change](./media/index/submit-pull-request.png)

That's it. Content team members will review and merge your PR.

Some UI elements may be different due to differences in permissions. The
preceding images are accurate for contributors that do not have write
permissions to the target repository. GitHub automatically creates a fork
of the target repository in your account. If you have write access to the
target repository, GitHub creates a new branch in the target repo. The
branch name has the form **<GitHubId>-patch-n** using your GitHub ID,
and a numeric identifier for the patch branch.

We typically use PRs for all changes, even for contributors that have
write access. That facilitates reviews and ensures quality. Most repositories
have the `master` branch protected so that updates must be submitted as PRs.

Use this workflow to make minor or infrequent changes with GitHub's web-based
Markdown editor. If you need to make large contributions, or you need support
for advanced Git features (such as branch management or advanced merge conflict
resolution), refer to the [major or long-running changes workflow](full-workflow.md).

## Review open PRs

If you are working on new, possibly CTP or beta, software, we are likely
building the docs as you are exploring the technology. You can find the
in-process docs in our public repositories. If you have comments, you can
help us make them better before they are released.

New articles are reviewed in public, using the [GitHub flow](https://guides.github.com/introduction/flow/)
process. Look at any of our docs repositories, and check the open pull
requests (PRs). We welcome comments and reviews on any open pull requests.
That helps us publish better content on our first release. We are looking
for ways to improve technical accuracy, clarity of the descriptions, and
grammatical accuracy.

## Create good issues

We've begun integrating GitHub issues as the comment platform for our
existing documents. Good issues help us focus our efforts. The more detail
you can provide, the more helpful the issue. Tell us what information you
were seeking. Tell us the search terms you used.

If you can't get started, tell us how you want to start exploring unfamiliar
technology.

Issues start the conversation about what's needed. The content team will
respond to these issues with ideas for what we can add, and ask for questions
and opinions. When we create adraft, we'll ask you to [review the PR](#review-open-prs).


## Getting more involved

The table of contents to your left is designed to help you get started
and be productive contributing to Microsoft Docs. The introductory
articles provide a quick start for the tasks that are common to any
contribution activity. Later articles are specific to different tasks,
and you should focus on the section that describes the activity that
interests you. Many of the articles can also serve as reference content,
which you might want to save as a favorite/bookmark in your browser. Also
note that there are several links to other sites, which will take you to
pages that are off the docs.microsoft.com domain and outside this guide.
