---
title: Create a pull request in GitHub
description: Learn how to create a pull request in GitHub so your updates to Microsoft Learn documentation can be reviewed and published on Microsoft Learn.
author: carlyrevier
ms.author: cahublou
ms.topic: contributor-guide
ms.service: learn
ms.custom: external-contributor-guide
ms.date: 01/25/2024
---

# Create a pull request in GitHub

After you've updated or added your content, it's time to create a pull request (PR). This step is required for getting your changes published. For more background on PRs, see [Git and GitHub fundamentals](git-github-fundamentals.md#pull-requests).

## Prerequisites

- Identify the GitHub repo that stores the documentation you want to edit.
- [Create a GitHub account](index.md#create-a-github-account), if you don't have one.
- [Install Git and Markdown tools](get-started-setup-tools.md).
- [Set up a local Git repository](get-started-setup-local.md).
- [Make changes in your local clone](how-to-write-major-edits.md)
- [Review Git and GitHub fundamentals](git-github-fundamentals.md) (optional).

## Open a PR

1. In your browser, navigate to GitHub.

1. In the top-right, select your profile, and then select **Your repositories**.

1. Look for the repository in which you just made changes. If there's more than one, select the repository for the MicrosoftDocs upstream repository (for example, *MicrosoftDocs/azure-docs*).

1. Select the **Pull requests** tab at the top of the page.

1. If you see a green **Compare & pull request** button, select that button.

:::image type="content" source="media/create-pull-request/create-pr-compare.png" alt-text="Screenshot of the compare and pull request button in GitHub.":::

1. If you don't see the button, open a new PR manually:
    1. Select the green **New pull request** button.
    1. On the Comparing changes page, make sure the **head repository:** drop-down is set to your fork (for example, *your-github-id/azure-docs*).
    1. Change the **compare:** drop-down to your working branch.
    1. Review the changes that appear. If you don't see your changes, make sure you're comparing the correct branches.

1. On the **Open a pull request** page, verify that:

   - The **base repository:** matches the upstream repository (for example, *MicrosoftDocs/azure-docs*).
   - The **base:** branch is set to the default branch (most likely named *main*) in the upstream repository. All your changes will be merged to the upstream branch.
   - The number of commits and files changed is what you expect.

:::image type="content" source="media/create-pull-request/comparing-changes.png" alt-text="Screenshot of the Comparing changes screen in GitHub.":::

1. Your first commit message on your branch becomes the default PR title. If you want, edit the title to make it more appropriate for a PR (for example: Update prerequisites list).

1. Add an optional description. A description helps reviewers understand the purpose of your PR. For example, you can describe the problem you're trying to solve or the reason you're making the change.

1. Select **Create pull request**. The new PR is linked to your working branch in your fork. Until the PR is merged, any new commits you push to the same working branch in your fork are automatically included in the PR.

## Next steps

You've now created your PR, but you haven't submitted it yet. Now you're ready to [process your pull request](process-pull-request.md) to make sure it gets reviewed and merged into the default branch.