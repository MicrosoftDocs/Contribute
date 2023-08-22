---
title: Microsoft Learn contributor guide overview
description: The contributor guide describes how you can contribute to technical documentation and other content experiences on Microsoft Learn.
author: carlyrevier
ms.author: cahublou
ms.date: 08/14/2023
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
---

# Microsoft Learn contributor guide overview

Welcome to the Microsoft Learn contributor guide!

Microsoft Learn hosts all documentation for Microsoft products and technologies. Sharing your expertise with others on Microsoft Learn helps everyone achieve more. Use the information in this guide to publish a new article to Microsoft Learn or make updates to an existing published article.

Several of the Microsoft documentation sets are open source and hosted on GitHub. Not all document sets are completely open source, but many have public-facing repos where you can suggest changes via pull requests (PR). This open-source approach streamlines and improves communication between product engineers, content teams, and customers, and it has other advantages:

- Open-source repos _plan in the open_ to get feedback on what docs are most needed.
- Open-source repos _review in the open_ to publish the most helpful content on our first release.
- Open-source repos _update in the open_ to make it easier to continuously improve the content.

The user experience on Microsoft Learn integrates [GitHub](https://github.com) workflows directly to make it even easier. Start by [editing the document you're viewing](#quick-edits-to-documentation). Or help by [reviewing new topics](#review-open-prs) or [creating quality issues](#create-quality-issues).

> [!IMPORTANT]
> All repositories that publish to Microsoft Learn have adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/) or the [.NET Foundation Code of Conduct](https://dotnetfoundation.org/code-of-conduct). For more information, see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/). Contact [opencode@microsoft.com](mailto:opencode@microsoft.com) or [conduct@dotnetfoundation.org](mailto:conduct@dotnetfoundation.org) with any questions or comments.<br>
>
> Minor corrections or clarifications to documentation and code examples in public repositories are covered by the [learn.microsoft.com Terms of Use](/legal/termsofuse). New or significant changes generate a comment in the PR, asking you to submit an online Contribution License Agreement (CLA) if you're not a Microsoft employee. We need you to complete the online form before we can review or accept your PR.

## Quick edits to documentation

Quick edits streamline the process to report and fix small errors and omissions in documentation. Despite all efforts, small grammar and spelling errors _do_ make their way into our published documents. While you can create issues to report mistakes, it's faster and easier to create a PR to fix the issue, when the option is available.

1. You need a GitHub account to contribute. If you already have an account, make sure you're signed in. If you don't have a GitHub account, navigate to [https://github.com/join](https://github.com/join) for a fast and free sign-up process.

1. Navigate to the documentation you wish to edit. _Some_ docs pages allow you to edit content directly in the browser. If so, you'll see an **Edit** pencil icon like the one shown below. Choosing the **Edit** pencil icon takes you to the source file on GitHub.

   :::image type="content" source="media/index/edit-article.png" alt-text="Screenshot of an Azure documentation article showing the edit pencil icon.":::

   If the **Edit** button isn't present, it means the content isn't open to public contributions. Some pages are generated (for example, from inline documentation in code) and must be edited in the project they belong to.

1. Select the pencil icon at the top of the GitHub file page. If the pencil icon is grayed out or doesn't display, you need to log in to your GitHub account.

   :::image type="content" source="media/index/edit-icon.png" alt-text="Screenshot of the Azure article within GitHub,showing the edit pencil icon.":::

    At the top of the article is the article's metadata. Metadata is applied to articles for reporting, discoverability via search, and driving aspects of the site experience. If you're making minor updates to a published article, you probably won't need to change the metadata.

1. If it's your first time working in this repository, you'll be prompted to fork the repo before you propose changes. Select **Fork this repository** to continue.

1. Edit the file in the web editor. Choose the **Preview** tab in the toolbar to check the formatting of your changes.

1. When you're finished editing, select the **Commit changes** or **Propose changes** button, usually at the top-right of the screen. 

1. Enter a commit message. The commit message becomes the title of your PR and should be a brief summary of your changes (for example, "Fix spelling and grammar errors"). Optionally, add an **Extended description** to give more details about your changes. Select **Propose changes**:

   :::image type="content" source="media/index/commit-changes.png" alt-text="Screenshot of the propose changes pop-up.":::

1. Now that you've proposed and committed your changes, you need to ask the owners of the repository to "pull" your changes into their repository. This is done using a [pull request](https://docs.github.com/articles/using-pull-requests)(PR). When you select **Propose changes**, you'll see a page like this:

   :::image type="content" source="media/index/create-pull-request.png" alt-text="Screenshot of the comparing changes screen.":::

   Select **compare across forks** and make sure your branch configuration looks like that shown above. Your PR should propose changes from your fork and branch (represented by the two items on the right side of the arrow) into the MicrosoftDocs repo's fork and `main` branch (represented by the two items on the left side of the arrow). You may have to select the dropdown boxes to adjust the repo and branch names.

   Review your changes, and then select **Create pull request**.

1. On the **Open a pull request** page, preview your PR. You can change the title or description fields if needed. When you're ready, select **Create pull request**. This action opens your PR.

1. If everything looks good and you're done editing, add a comment that reads `#sign-off`. This alerts the PR review team that your PR is ready to be reviewed.

    :::image type="content" source="media/index/sign-off.png" alt-text="Screenshot of the GitHub comment box within a PR with a comment reading #sign-off.":::

1. That's it! Content team members will review your PR and merge it when it's approved. You may get feedback requesting changes.

The GitHub editing UI responds to your permissions on the repository. The preceding images are for contributors who don't have write permissions to the target repository. GitHub automatically creates a fork of the target repository in your account. The newly created fork name has the form **`GitHubUsername`/`RepositoryName`** by default. If you have write access to the target repository, such as your fork, GitHub creates a new branch in the target repository. The branch name has the default form **patch-`n`**, using a numeric identifier for the patch branch.

We use PRs for all changes, even for contributors who have write access. Most repositories protect the default branch so that updates must be submitted as PRs.

The in-browser editing experience is best for minor or infrequent changes. If you make large contributions or use advanced Git features (such as branch management or advanced merge conflict resolution), you need to [fork the repo and work locally](how-to-write-workflows-major.md).

[!INCLUDE [note-docsitelocfeedback](../includes/note-docsitelocfeedback.md)]

## Review open PRs in GitHub

You can read new topics before they're published by checking the open PR queue in GitHub. Reviews follow the [GitHub flow](https://guides.github.com/introduction/flow/) process. You can see proposed updates or new articles in public repositories. Review them and add your comments. Look at any of our [Microsoft Learn repositories](https://github.com/orgs/MicrosoftDocs/repositories), and check the open PRs for areas that interest you. Community feedback on proposed updates helps the entire community.

## Create GitHub issues

Our docs are a continuous work in progress. Good GitHub issues help us focus our efforts on the highest priorities for the community. The more detail you can provide, the more helpful the issue. Tell us what information you sought. Tell us the search terms you used. If you can't get started, tell us how you want to start exploring unfamiliar technology.

Many of Microsoft's documentation pages have a **Feedback** section at the bottom of the page where you can choose to leave product feedback (**This product** link) or content feedback (**This page** link) to track issues that are specific to that article. Both of these options require you to log in to GitHub or some other system. To leave anonymous feedback, use the **Feedback** thumbs-up icon that appears in the top-right corner of each article, beneath the title.

Issues start the conversation about what's needed. The content team will respond to these issues with ideas for what we can add and ask for your opinions. When we create a draft, we'll ask you to [review the PR](#review-open-prs).

## Get more involved

Other topics in this guide help you get started productively contributing to Microsoft Learn. They explain working with GitHub repositories, Markdown tools, and extensions used in Microsoft Learn content.
