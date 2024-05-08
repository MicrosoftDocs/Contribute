---
title: Edit Microsoft Learn documentation in the browser
description: Learn how to edit a Microsoft Learn article in the browser using GitHub's user interface and without having to download or install tools.
author: carlyrevier
ms.author: cahublou
ms.date: 02/01/2024
ms.topic: contributor-guide
ms.service: learn
ms.custom: external-contributor-guide
---

# Edit Microsoft Learn documentation in the browser

> [!TIP]
> A self-paced, [step-by-step learning path](/training/modules/contribute-to-docs-browser/?source=recommendations) is available for this topic.

Several of Microsoft's documentation sets are open source and hosted on GitHub. While not all documentation sets are completely open source, many have public-facing repositories where you can suggest changes via pull requests (PRs). This open-source approach streamlines and improves communication between product engineers, content teams, and customers.

Quick edits facilitate the process to report and fix small errors and omissions in documentation. Despite all efforts, small grammar and spelling errors _do_ make their way into our published documents. We appreciate your help in identifying and fixing these issues!

We use PRs for all changes, even for contributors who have write access. Most repositories protect the default branch, so updates must be submitted as PRs.

## Prerequisite

- [Create a GitHub account](index.md#create-a-github-account), if you don't have one.

## Edit a document in the browser

1. Navigate to the documentation you want to edit. _Some_ docs pages allow you to edit content directly in the browser. If so, you'll see an **Edit** pencil icon like the one shown below. Choosing the **Edit** pencil icon takes you to the source file on GitHub.

   :::image type="content" source="media/how-to-write-quick-edits/edit-article.png" alt-text="Screenshot of an Azure documentation article showing the edit pencil icon.":::

   If the **Edit** button isn't present, it means the content isn't open to public contributions. Some pages are generated (for example, from inline documentation in code) and must be edited in the project they belong to.

1. Select the pencil icon at the top of the GitHub file page. If the pencil icon is unavailable (appears dimmed) or doesn't display, you need to log in to your GitHub account.

   :::image type="content" source="media/how-to-write-quick-edits/edit-icon.png" alt-text="Screenshot of the Azure article within GitHub,showing the edit pencil icon.":::

    At the top of the article is the article's metadata. Metadata is applied to articles for reporting, discoverability via search, and driving aspects of the site experience. If you're making minor updates to a published article, you probably won't need to change the metadata.

1. If it's your first time working in this repository, you'll be prompted to fork the repo before you propose changes. Select **Fork this repository** to continue.

1. Edit the file in the web editor. Choose the **Preview** tab on the toolbar to check the formatting of your changes.

1. When you're finished editing, select the **Commit changes** or **Propose changes** button, usually at the top-right of the screen.

1. Enter a commit message. The commit message becomes the title of your PR and should be a brief summary of your changes (for example, "Fix spelling and grammar errors"). Optionally, add an **Extended description** to give more details about your changes. Select **Propose changes**:

   :::image type="content" source="media/how-to-write-quick-edits/commit-changes.png" alt-text="Screenshot of the propose changes pop-up.":::

1. Now that you've proposed and committed your changes, you need to ask the owners of the repository to "pull" your changes into their repository. This is done using a [pull request](https://docs.github.com/articles/using-pull-requests) (PR). When you select **Propose changes**, you'll see a page like this:

   :::image type="content" source="media/how-to-write-quick-edits/create-pull-request.png" alt-text="Screenshot of the comparing changes screen.":::

   Your PR proposes changes from your fork and branch (represented by the two items on the right side of the arrow) into the documentation repo's main fork and `main` branch (represented by the two items on the left side of the arrow).

   Review your changes, and then select **Create pull request**.

1. On the **Open a pull request** page, preview your PR. You can change the title or description fields if needed. When you're ready, select **Create pull request**. This action opens your PR and alerts the article owner that you've proposed a change.

1. That's it! Content team members will review your PR and merge it when it's approved. You may get feedback requesting changes. For more details on processing your PR, see [Process a pull request](process-pull-request.md).

## Limitations

- Most localized (i.e., translated) content doesn't offer the ability to edit through GitHub. However, you can provide feedback on translation quality by selecting the Feedback (thumbs) button at the top of the page and then choosing the **Translation quality** reason. You can also leave more specific feedback on localized content by using the [Provide Feedback](https://aka.ms/provide-feedback) form.
- The in-browser editing experience works best for minor and infrequent changes. If you make large contributions or use advanced Git features (such as branch management or advanced merge conflict resolution), we recommend that you [fork the repo and work locally](how-to-write-workflows-major.md).
