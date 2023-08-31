---
title: Edit Microsoft Learn documentation in the browser
description: Learn how to edit a Microsoft Learn documentation article in the browser using GitHub.
author: carlyrevier
ms.author: cahublou
ms.date: 08/28/2023
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
---

# Edit Microsoft Learn documentation in the browser

Several of Microsoft's documentation sets are open source and hosted on GitHub. Not all documentation is completely open source, but many have public-facing repositories where you can suggest changes via pull requests (PRs). This open-source approach streamlines and improves communication between product engineers, content teams, and customers.

Quick edits streamline the process to report and fix small errors and omissions in documentation. Despite all efforts, small grammar and spelling errors _do_ make their way into our published documents. While you can create issues to report mistakes, it's faster and easier to create a PR to fix the issue, when the option is available.

We use PRs for all changes, even for contributors who have write access. Most repositories protect the default branch, so updates must be submitted as PRs.

## Prerequisites

- A GitHub account
- Acceptance of the Microsoft Learn CLA and TOU

## Edit a document in the browser

1. Navigate to the documentation you wish to edit. _Some_ docs pages allow you to edit content directly in the browser. If so, you'll see an **Edit** pencil icon like the one shown below. Choosing the **Edit** pencil icon takes you to the source file on GitHub.

   :::image type="content" source="media/how-to-write-quick-edits/edit-article.png" alt-text="Screenshot of an Azure documentation article showing the edit pencil icon.":::

   If the **Edit** button isn't present, it means the content isn't open to public contributions. Some pages are generated (for example, from inline documentation in code) and must be edited in the project they belong to.

1. Select the pencil icon at the top of the GitHub file page. If the pencil icon is grayed out or doesn't display, you need to log in to your GitHub account.

   :::image type="content" source="media/how-to-write-quick-edits/edit-icon.png" alt-text="Screenshot of the Azure article within GitHub,showing the edit pencil icon.":::

    At the top of the article is the article's metadata. Metadata is applied to articles for reporting, discoverability via search, and driving aspects of the site experience. If you're making minor updates to a published article, you probably won't need to change the metadata.

1. If it's your first time working in this repository, you'll be prompted to fork the repo before you propose changes. Select **Fork this repository** to continue.

1. Edit the file in the web editor. Choose the **Preview** tab in the toolbar to check the formatting of your changes.

1. When you're finished editing, select the **Commit changes** or **Propose changes** button, usually at the top-right of the screen.

1. Enter a commit message. The commit message becomes the title of your PR and should be a brief summary of your changes (for example, "Fix spelling and grammar errors"). Optionally, add an **Extended description** to give more details about your changes. Select **Propose changes**:

   :::image type="content" source="media/how-to-write-quick-edits/commit-changes.png" alt-text="Screenshot of the propose changes pop-up.":::

1. Now that you've proposed and committed your changes, you need to ask the owners of the repository to "pull" your changes into their repository. This is done using a [pull request](https://docs.github.com/articles/using-pull-requests)(PR). When you select **Propose changes**, you'll see a page like this:

   :::image type="content" source="media/how-to-write-quick-edits/create-pull-request.png" alt-text="Screenshot of the comparing changes screen.":::

   Select **compare across forks** and make sure your branch configuration looks like that shown above. Your PR should propose changes from your fork and branch (represented by the two items on the right side of the arrow) into the MicrosoftDocs repo's fork and `main` branch (represented by the two items on the left side of the arrow). You may have to select the dropdown boxes to adjust the repo and branch names.

   Review your changes, and then select **Create pull request**.

1. On the **Open a pull request** page, preview your PR. You can change the title or description fields if needed. When you're ready, select **Create pull request**. This action opens your PR.

1. If everything looks good and you're done editing, add a comment that reads `#sign-off`. This alerts the PR review team that your PR is ready to be reviewed.

    :::image type="content" source="media/how-to-write-quick-edits/sign-off.png" alt-text="Screenshot of the GitHub comment box within a PR with a comment reading #sign-off.":::

1. That's it! Content team members will review your PR and merge it when it's approved. You may get feedback requesting changes.

## Limitations

- Most localized documentation doesn't offer the ability to edit or provide feedback through GitHub. To provide feedback on localized content, use the [Provide Feedback](https://aka.ms/provide-feedback) form.
- The in-browser editing experience works best for minor or infrequent changes. If you make large contributions or use advanced Git features (such as branch management or advanced merge conflict resolution), we recommend that you [fork the repo and work locally](how-to-write-workflows-major.md).