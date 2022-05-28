---
title: Set up a local Git repository
description: This article provides guidance to create your local Git repository and contribute to documentation, including the forking and cloning process.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
author: jasonwhowell
ms.author: jasonh
ms.date: 05/28/2022
---

# Set up a local Git repository

This article describes the steps to set up a Git repository on your local device, with the intent to contribute to Microsoft documentation. Contributors may use a locally cloned repository to add new articles, do major edits on existing articles, change artwork, and more.

Follow these one-time setup activities to start contributing:

> [!div class="checklist"]
> * Determine the Microsoft repository
> * Fork the Microsoft repository to your GitHub account
> * Choose a location on your device to clone your fork
> * Clone your fork to your local device
> * Configure the Microsoft repository as the remote upstream

> [!IMPORTANT]
> If you're making only minor changes to an article, you *do not* need to complete the steps in this article. You can continue directly to the [quick changes workflow](index.md#quick-edits-to-documentation).

## Overview

To contribute to Microsoft's documentation you must fork the appropriate repository into your own GitHub account. A fork provides an isolated space allowing you to have read and write permissions for your proposed changes. You can make and edit files locally by cloning your fork. After you save your changes locally you then push them to your fork. Once your changes are complete, you use pull requests to merge changes into the Microsoft documentation repository.

:::image type="content" source="media/contribute-get-started-setup-local/repository-initial-setup.svg" alt-text="The Microsoft contributing workflow setup as outlined in this guide." lightbox="media/contribute-get-started-setup-local/repository-initial-setup.svg" border="false":::

### Terminology

Before you start, here are a few important terms and Git actions that will be used in this guide. In addition, the diagram above might help provide further understanding of how these terms relate.

| Name | Description |
|--|--|
| Microsoft/Source Repository | This is the source repository that Microsoft maintains publicly on GitHub. You do not have write permissions to this repository. |
| Fork | This is a copy of a main repository that provides an isolated space for you to make changes. In our case, "your fork" refers to your copy of the Microsoft repository. You have full control over this repository. |
| Clone | This is a local copy of a repository. In our case this is a local copy of your fork stored on Github. |
| Fetch Upstream | This keeps your fork up-to-date with the source or upstream repository. This is a one way action that pulls all changes from the upstream repository, in our case the Microsoft repository, into your forked or cloned repository. |
| Pull Request | A request to merge changes from your fork into the upstream repository, in our case the Microsoft repository. |
| Push | Uploads all changes from the cloned repository into the forked repository. |
| Pull | Downloads all changes from the forked repository into the cloned repository. |

Along with the terminology outlined above, it might be helpful to reference the [Git and GitHub fundamentals](./git-github-fundamentals.md) along with the terminology section of the [GitHub contribution workflow](./how-to-write-workflows-major.md#terminology). Don't stress over knowing all of the terminologies right away; instead, use the above table as a reference, as needed, when going through this guide.

## Determine the Microsoft repository

To start you need to determine what Microsoft repository you want to edit. Documentation hosted at [docs.microsoft.com](https://docs.microsoft.com) resides in several different repositories on [GitHub](https://github.com). It may not be immediately clear which Microsoft repository is used for maintaining an article. Furthermore, it may not be clear where an article is stored in a repository.

1. To determine which Microsoft repository contains the article you want to edit, visit the article on [docs.microsoft.com](https://docs.microsoft.com).

    > [!NOTE]
    > If you're a Microsoft employee or vendor, before you edit the article, append `review.` to the beginning of the URL. This action lets you use the private repository, **windows-docs-pr**. For more information, see the [internal contributor guide](https://review.docs.microsoft.com/help/get-started/edit-article-in-github?branch=main).

2. Then select the **Pencil** icon at the upper right of the article.

   :::image type="content" source="media/index/edit-article.png" alt-text="Select the Pencil icon, Edit This Document, to determine the repository and file location." border="false":::

   If the pencil icon isn't present, the content might not be open to public contributions. Some pages are generated (for example, from inline documentation in code) and must be edited in the project they belong to. This isn't always the case and you might be able to find the documentation by searching the [Microsoft Docs Organization on GitHub](https://github.com/MicrosoftDocs).

   > [!TIP]
   > View the page source in your browser, and look for the following metadata: `original_content_git_url`. This path always points to the source markdown file for the article.

3. The **Pencil** icon takes you to the GitHub location for the corresponding article in the appropriate repository. GitHub displays the repository name at the top left of the page.

   :::image type="content" source="media/contribute-get-started-setup-local/public-repo.png" alt-text="The repository name is listed at the top left of the GitHub page.":::

   For example, these popular repositories are available for public contributions:
   * Azure Documentation [https://github.com/MicrosoftDocs/azure-docs](https://github.com/MicrosoftDocs/azure-docs)
   * SQL Server Documentation [https://github.com/MicrosoftDocs/sql-docs](https://github.com/MicrosoftDocs/sql-docs)
   * Visual Studio Documentation [https://github.com/MicrosoftDocs/visualstudio-docs](https://github.com/MicrosoftDocs/visualstudio-docs)
   * .NET Documentation [https://github.com/dotnet/docs](https://github.com/dotnet/docs)
   * Azure .NET SDK Documentation [https://github.com/azure/azure-docs-sdk-dotnet](https://github.com/azure/azure-docs-sdk-dotnet)
   * Microsoft Endpoint Configuration Manager Documentation [https://github.com/MicrosoftDocs/memdocs](https://github.com/MicrosoftDocs/memdocs)

## Fork the Microsoft repository to your GitHub account

After determining the Microsoft repository, use the GitHub website to create a fork of the Microsoft repository. The newly created fork will be held in your GitHub account and changes are isolated from the Microsoft repository.

A fork is required since all documentation repositories provide read-only access. To propose changes, you must submit a [pull request](git-github-fundamentals.md#pull-requests) from your fork into the Microsoft repository. To facilitate this process, you first need your own copy of the repository, in which you have write access. A GitHub *fork* serves that purpose.

1. Go to the Microsoft repository's GitHub page and select the **Fork** button at the upper right.

   :::image type="content" source="media/contribute-get-started-setup-local/fork-location.png" alt-text="Select Fork at the upper right of the repository on GitHub.":::

2. You will be taken to a page for creating a new fork. The fork destination should be automatically set to your GitHub account. If you belong to multiple organizations you will be able to change the destination account, choose the account that fits best. Generally the default settings work fine, but feel free to customize the provided fields. Once you are satisfied with your choices, select **Create fork**.

   :::image type="content" source="media/contribute-get-started-setup-local/create-fork.png" alt-text="Create a new fork page.":::

   A copy of the Microsoft repository will be created within the account you selected, this will be your fork.

## Choose a location on your device to clone your fork

Now that you have created a fork of the Microsoft repository, you must clone your fork locally. Some of the documentation repositories can be large; for example, `azure-docs` is up to 25 GB. Make sure to choose a location with available disk space for cloning the forked repository.

When cloning a repository, Git will automatically create a new directory, with the forked repository's name,  within your current directory. If you are working on multiple documentation repositories it may be helpful to store them together. For example, you may want to clone the `azure-docs`, `sql-docs`, and `visualstudio-docs` using a directory path such as `C:/Users/<Username>/Documents/Docs/<Repo-Name>`. Each repository is stored separately in its own directory (`<Repo-Name>`), but together under the same parent directory (`Docs`).

> [!TIP]
> [Windows Terminal](/windows/terminal/) with [PowerShell](/powershell/) supports a nearly identical command experience to that of Git Bash. You can even run Git Bash inside Windows Terminal.

1. Launch Git Bash

   :::image type="content" source="media/contribute-get-started-setup-local/gitbash-start.png" alt-text="Launch Git Bash from Windows search.":::

   The default path that Git Bash starts in is the home directory (`~`) or `/c/Users/<Username>` on Windows. To determine the current directory, type `pwd`.

2. Change directory (`cd`) to the directory that you want to create your parent directory in. Note that Git Bash uses the Linux convention of forward-slashes instead of back-slashes for directory paths.

   > [!IMPORTANT]
   > Avoid choosing a local directory path that is nested inside of another Git repository. While it is acceptable to store the cloned repositories adjacent to each other, nesting repositories inside one another causes errors for the Git file tracking.

   Consider a root directory:

   ```bash
   cd C:/
   ```

   Consider a directory in your user profile directory:

   ```bash
   cd ~/Documents
   ```

3. Make a new directory (`mkdir`) for storing all of your cloned repositories. Choose a parent directory name that is easy for you to remember and type.

   ```bash
   mkdir "Docs"
   ```

4. Finally, change directory to the newly created directory. For example, if you used `Docs` as the directory name:

   ```bash
   cd Docs/
   ```

   This will be the parent directory where you clone and store all of your documentation repositories. In total the path (`pwd`) will be something like: `/c/Users/<Username>/Documents/Docs`.

## Clone your fork to your local device

To clone your fork, run the **clone** command which downloads a copy of your forked repository into a new directory on the local disk. A new directory, with the forked repository's name, is made within the current directory. It may take a few minutes, depending on the repository size, to download. You can explore the directory to see the structure once it is finished.

1. Run the **clone** command by providing the forked repository URL.

   > [!Tip]
   > You can get your fork's GitHub URL for the clone command from the **Code** button in the GitHub UI:
   >
   > :::image type="content" source="media/contribute-get-started-setup-local/github-code-button.svg" alt-text="GitHub Code button." border="false":::

   Be sure to specify the URL to your fork during the cloning process, not the Microsoft repository from which you created the fork. Otherwise, you cannot contribute changes.

   ```bash
   git clone https://github.com/<Username>/<Repo-Name>.git
   ```

2. To begin executing Git commands and working with your cloned fork, change your current working directory to it.

   ```bash
   cd <Repo-Name>/
   ```

## Configure the Microsoft repository as the remote upstream

If you are working on more substantial changes that span a larger period of time, you might want to keep your fork up-to-date with the Microsoft repository's changes. To do this set up a read-only remote connection to the Microsoft repository, sometimes referred to as the **upstream** repository. You use the upstream repository to keep your locally cloned repository up-to-date with the latest changes from the upstream repository. The **remote** command is used to set the upstream repository. While the **fetch** command pulls changes from the upstream repository into the cloned repository.

1. Make sure your current working directory is the cloned repository. For example, running the `pwd` command should output:

   ```bash
   /c/Users/<Username>/Documents/Docs/<Repo-Name>
   ```

   If your current working directory is not the cloned repository, change directory (`cd`) to it. You can also test if you are in a repository by running `git status`.

2. Add the Microsoft repository as an upstream repository.

   ```bash
   git remote add upstream https://github.com/MicrosoftDocs/<Repo-Name>.git
   ```

3. Validate that the remote URLs are correct.

   ```bash
   git remote -v
   ```

   The **origin** URL entires should be your fork URL, while the **upstream** URL entires should be the source Microsoft repository URL.

   ```output
   origin  https://github.com/<Username>/<Repo-Name>.git (fetch)
   origin  https://github.com/<Username>/<Repo-Name>.git (push)
   upstream        https://github.com/MicrosoftDocs/<Repo-Name>.git (fetch)
   upstream        https://github.com/MicrosoftDocs/<Repo-Name>.git (push)
   ```

   `<Username>` will be your GitHub username, or the GitHub account/organization you chose when forking the Microsoft repository. `<Repo-Name>` will be the respective fork and Microsoft repository name. The Microsoft repository name and your fork repository name may be different depending on your choices when forking.

4. If you made a mistake, you can remove the remote upstream value.

   ```bash
   git remote remove upstream
   ```

5. Once your upstream repository is correctly configured you can fetch changes from the upstream repository at any time.

   ```bash
   git fetch upstream
   ```

## Next steps

In this step you set up set up a local Git repository. In the next step you will learn more about adding and updating content.

> [!div class="nextstepaction"]
> [GitHub contribution workflow](how-to-write-workflows-major.md)
