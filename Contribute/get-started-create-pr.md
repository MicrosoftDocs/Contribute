---
title: Create a pull request
description: This article helps you complete creating a PR after you have pushed your commits.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
author: v-ashwinik
ms.author: v-ashwinik
ms.date: 06/09/2021
---

# Create a pull request

You create a pull request (PR) after you've updated or added your content. This step is required for getting your changes published. You'll commit and push the changes from Visual Studio Code and continue to GitHub to complete the creation of the pull request.

[!INCLUDE[Contribute create pull request](~/guide/help-content/includes/proc-contribute-create-pr.md)]

## Pull request processing

[!INCLUDE[Contribute pull request processing](~/guide/help-content/includes/contribute-pull-request-processing.md)]

## Update the pull request

After all PR processing is completed, you should review the results (PR comments, preview URLs, and validation) to determine if more changes are required before you sign-off for merging. If a PR reviewer has reviewed your pull request, they can also provide feedback through comments if there are outstanding issues/questions to be resolved before merge.

### To update the PR

When you're making changes, you almost always have to add commits to the PR:

* To address any rendering issues.
* To address feedback from peer reviewers.
* To address feedback from PR reviewers (certain repositories).

[!INCLUDE[Contribute update pull request](~/guide/help-content/includes/proc-contribute-update-pr.md)]

Each time you add a commit to the same working branch in your GitHub fork, the commit is automatically added to the PR. And the publishing system automatically reruns the builds.

## Sign-off and merge pull request

[!INCLUDE[Contribute pull request publishing](~/guide/help-content/includes/contribute-pull-request-publishing.md)]

### Automated labels

[!INCLUDE[Contribute how to pull requests apex automation](./includes/contribute-how-to-pull-requests-apex-automation.md)]

When the pull request is free of errors and signed off, your changes are merged back into the parent branch and the pull request is closed.

### Merge the PR

Typically, when your PR is ready to go, you get it reviewed before it's merged. Ask for a review from a team member who is familiar with the docs editing process for your repository. Continue to merge the PR when the reviewer approves the PR.

1. Use the repository-specific method for getting a PR merged. For example:

   * In the Azure repository, add a PR comment *#sign-off*.
   * In the .NET and ASP.NET repositories, select the **Squash and merge** button.

   After the PR is merged, your changes will be included in the next publish.

2. After the next publish, go to the production URL for the article you changed, and verify that your changes are live.

## Next steps

That's it! You've made a contribution to docs.microsoft.com content!

* To learn more about Markdown and Markdown extensions, continue to the [Markdown reference](markdown-reference.md) article.
