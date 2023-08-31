---
title: Make major or long-running changes to Microsoft Learn documentation
description: Learn how to use the "major" contributor workflow to make major or long-running contributions to Microsoft Learn documentation.
author: carlyrevier
ms.author: cahublou
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
ms.date: 08/31/2023
---

# Make major or long-running changes to Microsoft Learn documentation

> [!IMPORTANT]
> All repositories that publish to Microsoft Learn have adopted either the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/) or the [.NET Foundation Code of Conduct](https://dotnetfoundation.org/code-of-conduct). For more information, see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/). Or contact [opencode@microsoft.com](mailto:opencode@microsoft.com), or [conduct@dotnetfoundation.org](mailto:conduct@dotnetfoundation.org) with any questions or comments.<br>
>
> Minor corrections or clarifications to documentation and code examples in public repositories are covered by the [learn.microsoft.com Terms of Use](/legal/termsofuse). New or significant changes will generate a comment in the pull request, asking you to submit an online Contribution License Agreement (CLA) if you are not an employee of Microsoft. You will need to complete the online form before your pull request can be merged.

This workflow is suitable for a contributor who needs to make a major change or will be a frequent contributor to a repository. Frequent contributors typically have ongoing (long-running) changes, which go through multiple build/validation/staging cycles or span multiple days before pull request sign-off and merge.

Examples of these types of contributions include:

- **Making a large contribution**. For instance, your contributions (additions, changes, or deletions) might span multiple articles and need to be committed and tested as one unit of work in a single PR.
- **Creating and publishing a new article**, which typically requires a more robust local editor.
- **Adding new images or updating images**, which typically requires you to simultaneously create a new `media` subdirectory, create image files, update image links in articles, and preview Markdown files in a local editor to test image rendering.
- **Updating an article over a period of days before you publish**. In these cases, you typically need to do regular integration of other changes that occur in the default branch. This integration is easier via Git Bash and local editing. You also run the risk of losing your edits if you do this via the GitHub web editor and wait before you commit the changes.
- **Making continual updates to the same article after a PR has been opened**. Though you can use the GitHub web editor for this purpose, you might create multiple outstanding PRs for the same file, which may conflict with one another.

## Prerequisites

- Set up your GitHub account.
- Install Git and Markdown tools.
- Set up a local Git repository.
- Review Git and GitHub fundamentals (optional).

## Terminology

Before you start, let's review some of the Git/GitHub terms and monikers used in this workflow. Don't worry about understanding them now. Just know that you will be learning about them, and you can refer back to this section when you need to verify a definition.

| Name | Description |
|-----------|-------------|
|fork|Normally used as a noun, when referring to a copy of a main GitHub repository. In practice, a fork is just another repository. But it's special in the sense that GitHub maintains a connection back to the main/parent repository. It's sometimes used as a verb, as in "You must fork the repository first."|
|remote|A named connection to a remote repository, such as the "origin" or "upstream" remote. Git refers to this as remote because it is used to reference a repository that's hosted on another computer. In this workflow, a remote is always a GitHub repository.|
|origin|The name assigned to the connection between your local repository and the repository from which it was cloned. In this workflow, origin represents the connection to your fork. It's sometimes used as a moniker for the origin repository itself, as in "Remember to push your changes to origin."|
|upstream|Like the origin remote, upstream is a named connection to another repository. In this workflow, upstream represents the connection between your local repository and the main repository, from which your fork was created. It's sometimes used as a moniker for the upstream repository itself, as in "Remember to pull the changes from upstream."|

## Workflow

In this workflow, changes flow in a repetitive cycle. Starting from your device's local repository, they flow back up to your GitHub fork, into the main GitHub repository, and back down locally again as you incorporate changes from other contributors.

### Create a working branch

Recall from [Git and GitHub fundamentals](git-github-fundamentals.md#git) that a Git repository contains a default branch, plus any additional work-in-progress branches that have not been integrated into the default branch. Whenever you introduce a set of logically related changes, it’s a best practice to create a *working branch* to manage your changes through the workflow. We refer to it here as a working branch because it's a workspace to iterate/refine changes until they can be integrated back into the default branch.

Isolating related changes to a specific branch allows you to control and introduce those changes independently, targeting them to a specific release time in the publishing cycle. In reality, depending on the type of work you do, you can easily end up with several working branches in your repository. It's not uncommon to be working on multiple branches at the same time, each representing a different project.

>[!TIP]
>Making your changes in the default branch is *not* a good practice. Imagine that you use the default branch to introduce a set of changes for a timed feature release. You finish the changes and are waiting to release them. Then in the interim, you have an urgent request to fix something, so you make the change to a file in the default branch and then publish the change. In this example, you inadvertently publish both the fix *and* the changes that you were holding for release on a specific date.

Now let's create a new working branch in your local repository, to capture your proposed changes. If you've set up Git Bash (see [Install content authoring tools](get-started-setup-tools.md)), you can create a new branch and "check out" that branch with one command from within your cloned repository:

````
git checkout -b "branchname"
````

Each git client is different, so consult the help for your preferred client. You can see an overview of the process in the GitHub Guide on [GitHub flow](https://guides.github.com/introduction/flow/).

## Make your changes

Now that you have a copy ("clone") of the Microsoft repository and you've created a branch, you're now free to make whatever changes you think would benefit the community using any text or Markdown editor, as outlined on the [Install content authoring tools](get-started-setup-tools.md) page.  You can save your changes locally without needing to submit them to Microsoft until you're ready.

## Save changes to your repository

Before sending your changes to the author, you must first save them to your Github repository.  Again, while all tools are different, if you're using the Git Bash command line, this can be done in just a few easy steps.

First, from within the repository, you need to _stage_ all of your changes in preparation for the next commit.  This can be done by executing:

````
git add --all
````

Next, you need to commit your saved changes to your local repository.  This can be done in Git Bash by running:

````
git commit -m "Short Description of Changes Made"
````

Finally, since you created this branch on your local computer, you need to let the fork in your GitHub.com account know about it.  If you're using Git Bash, this can be done by running:

````
git push --set-upstream origin <branchname>
````

You've done it!  Your code is now up in your GitHub repository and ready for you to create a pull request.  

>[!TIP]
> Even though your changes become visible in your personal GitHub account when you push them, there is no rule that you need to submit a pull request immediately.  If you want to stop and return at a later time to make additional tweaks, that's OK!

Need to fix something you submitted?  No problem!  Just make your changes in the same branch and then commit and push again (no need to set the upstream server on subsequent pushes of the same branch).

## Make your next change

Got more changes you need to make unrelated to this one? Switch back to the default branch, pull from the upstream repository to make sure that your fork is up to date, and check out a new branch.  Run the following commands in Git Bash:

````
git checkout main
git pull upstream main
git checkout -b "branchname"
````

> [!NOTE]
> The preceding commands assume the repo you're working with has `main` as its default branch. If the first command fails, it's likely that the default branch hasn't been renamed. Replace `main` in the first two commands with `master` to verify this.

You're now back in a new branch, and you're well on your way to being an expert contributor.

## Push changes??

## Next steps

- Learn about [pull request processing](process-pull-request.md), the next step in the contribtuion workflow.
- To learn more about topics such as Markdown and Markdown extensions syntax, review the [Markdown reference](markdown-reference.md).
