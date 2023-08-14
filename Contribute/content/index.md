---
title: Microsoft Learn documentation contributor guide overview
description: The guide describes how you can contribute to technical documentation on Microsoft Learn.
author: carlyrevier
ms.author: cahublou
ms.date: 05/11/2022
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
---

# Microsoft Learn documentation contributor guide overview

Welcome to the Microsoft Learn documentation contributor guide!

Sharing your expertise with others on Microsoft Learn helps everyone achieve more. Use the information in this guide to publish a new article to Microsoft Learn or make updates to an existing published article.

Several of the Microsoft documentation sets are open source and hosted on GitHub. Not all document sets are completely open source, but many have public-facing repos where you can suggest changes via pull requests (PR). This open-source approach streamlines and improves communication between product engineers, content teams, and customers, and it has other advantages:

- Open-source repos _plan in the open_ to get feedback on what docs are most needed.
- Open-source repos _review in the open_ to publish the most helpful content on our first release.
- Open-source repos _update in the open_ to make it easier to continuously improve the content.

The user experience on Microsoft Learn integrates [GitHub](https://github.com) workflows directly to make it even easier. Start by [editing the document you're viewing](#quick-edits-to-documentation). Or help by [reviewing new topics](#review-open-prs) or [creating quality issues](#create-quality-issues).

> [!IMPORTANT]
> All repositories that publish to Microsoft Learn have adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/) or the [.NET Foundation Code of Conduct](https://dotnetfoundation.org/code-of-conduct). For more information, see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/). Contact [opencode@microsoft.com](mailto:opencode@microsoft.com) or [conduct@dotnetfoundation.org](mailto:conduct@dotnetfoundation.org) with any questions or comments.<br>
>
> Minor corrections or clarifications to documentation and code examples in public repositories are covered by the [learn.microsoft.com Terms of Use](/legal/termsofuse). New or significant changes generate a comment in the PR, asking you to submit an online Contribution License Agreement (CLA) if you're not a Microsoft employee. We need you to complete the online form before we can review or accept your PR.

## Quick edits to documentation making changes

Quick edits streamline the process to report and fix small errors and omissions in documentation. Despite all efforts, small grammar and spelling errors _do_ make their way into our published documents. While you can create issues to report mistakes, it's faster and easier to create a PR to fix the issue, when the option is available.

1. _Some_ docs pages allow you to edit content directly in the browser. If so, you'll see an **Edit** button like the one shown below. Choosing the **Edit** (or equivalently localized) button takes you to the source file on GitHub.

   :::image type="content" source="media/index/edit-article.png" alt-text="Location of the edit article link.":::

   If the **Edit** button isn't present, it means the content isn't open to public contributions.  Some pages are generated (for example, from inline documentation in code) and must be edited in the project they belong to.

2. Select the pencil icon to edit the article. If the pencil icon is grayed out, you need to either log in to your GitHub account or create a new account.

   :::image type="content" source="media/index/edit-icon.png" alt-text="Location of the fork and edit pencil icon.":::

3. Edit the file in the web editor. Choose the **Preview** tab to check the formatting of your changes.

4. When you're finished editing, scroll to the bottom of the page. In the **Propose changes** area, enter a title and optionally a description for your changes. The title will be the first line of the commit message. Select **Propose changes** to create a new branch in your fork and commit your changes:

   :::image type="content" source="media/index/commit-changes.png" alt-text="Propose and commit file changes.":::
   
5. Now that you've proposed and committed your changes, you need to ask the owners of the repository to "pull" your changes into their repository. This is done using something called a "pull request" (PR). When you select **Propose changes**, a new page similar to the following is displayed:

   :::image type="content" source="media/index/create-pull-request.png" alt-text="Compare changes and create pull request.":::

   Select **Create pull request**. Next, enter a title and a description for the PR, and then select **Create pull request**. If you're new to GitHub, see [About pull requests](https://docs.github.com/articles/using-pull-requests) for more information.

6. That's it! Content team members will review your PR and merge it when it's approved. You may get feedback requesting changes.

The GitHub editing UI responds to your permissions on the repository. The preceding images are for contributors who don't have write permissions to the target repository. GitHub automatically creates a fork of the target repository in your account. The newly created fork name has the form **`GitHubUsername`/`RepositoryName`** by default. If you have write access to the target repository, such as your fork, GitHub creates a new branch in the target repository. The branch name has the default form **patch-`n`**, using a numeric identifier for the patch branch.

We use PRs for all changes, even for contributors who have write access. Most repositories protect the default branch so that updates must be submitted as PRs.

The in-browser editing experience is best for minor or infrequent changes. If you make large contributions or use advanced Git features (such as branch management or advanced merge conflict resolution), you need to [fork the repo and work locally](how-to-write-workflows-major.md).

[!INCLUDE [note-docsitelocfeedback](../includes/note-docsitelocfeedback.md)]

## Review open PRs

You can read new topics before they're published by checking the open PR queue. Reviews follow the [GitHub flow](https://guides.github.com/introduction/flow/) process. You can see proposed updates or new articles in public repositories. Review them and add your comments. Look at any of our Microsoft Learn repositories, and check the open PRs for areas that interest you. Community feedback on proposed updates helps the entire community.

## Create quality issues

Our docs are a continuous work in progress. Good issues help us focus our efforts on the highest priorities for the community. The more detail you can provide, the more helpful the issue. Tell us what information you sought. Tell us the search terms you used. If you can't get started, tell us how you want to start exploring unfamiliar technology.

Many of Microsoft's documentation pages have a **Feedback** section at the bottom of the page where you can choose to leave **Product feedback** or **Content feedback** to track issues that are specific to that article.

Issues start the conversation about what's needed. The content team will respond to these issues with ideas for what we can add, and ask for your opinions. When we create a draft, we'll ask you to [review the PR](#review-open-prs).

## Get more involved

Other topics in this guide help you get started productively contributing to Microsoft Learn. They explain working with GitHub repositories, Markdown tools, and extensions used in the Microsoft Learn content.
