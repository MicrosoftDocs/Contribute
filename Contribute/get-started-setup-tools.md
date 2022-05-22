---
title: Install content authoring tools
description: This article helps you download and install the content authoring tools you will need, such as Git and Visual Studio Code.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
author: jasonwhowell
ms.author: jasonh
ms.date: 05/22/2022
---

# Install content authoring tools

This article describes the steps to interactively install content authoring tools like Git and Visual Studio Code.

> [!div class="checklist"]
>
> * Install [Git](https://git-scm.com/)
> * Install [Visual Studio Code](https://code.visualstudio.com/)
> * Install [Docs Authoring Pack](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack)

>[!IMPORTANT]
> If you're making only minor changes to an article, you *do not* need to complete the steps in this article and can continue directly to the [quick changes workflow](index.md#quick-edits-to-documentation).
>
> Contributors who will be making major changes are encouraged to complete these steps, which enable you to use the [major/long-running changes workflow](how-to-write-workflows-major.md). Even if you have write permissions in the main repository, *we highly recommend (and this guide assumes) that you fork and clone the repository* so that you have read/write permissions to store your proposed changes in your fork.

## Install Git

When installing Git, a version control system, on Windows, it includes Git Bash, a command-line application that you can use to run commands and interact with your local Git repository.

> [!TIP]
> If you already have Visual Studio Code installed you can set it as Git's default editor during setup.

### Install Git on Windows

[!INCLUDE[Install Git client tools for Windows](~/guide/help-content/includes/proc-contribute-install-git-client-tools.md)]

### Install Git on Linux and macOS

* Git on macOS is provided as part of the Command Line Tools for Xcode. Simply run `git` from Terminal, and you will be prompted to install the command line tools if needed. You can learn more about installing [Git on macOS](https://git-scm.com/download/mac) from the Software Freedom Conservancy.
* [Git on Linux and Unix](https://git-scm.com/download/linux)

### Configure Git

After installation, Git comes ready-to-go, with the exception of two important configurations. For your changes to be properly tracked and attributed, you must set a local username and email. **Do not skip this step.**

The following commands set the default username and email for every repository on your device, not just Microsoft repositories. For a more detailed guide on configuring Git, see GitHub's [Setting up Git](https://docs.github.com/articles/set-up-git#setting-up-git) documentation.

```bash
git config --global user.name "First Last"
```

```bash
git config --global user.email "email@example.com"
```

Additional Git resources are available here: [GitHub Quickstart](https://docs.github.com/get-started/quickstart) | [Git basics](https://git-scm.com/book/en/v2/) | [Learning Git and GitHub](https://help.github.com/articles/good-resources-for-learning-git-and-github/)

## Install Visual Studio Code

[Visual Studio Code](https://code.visualstudio.com/), also known as VS Code, is a lightweight editor that works on Windows, Linux, and macOS. It includes Git integration, and support for extensions.

> [!TIP]
> To launch VS Code and open the current folder, run the command `code .` in the command line or bash shell. If the current folder is part of a local Git repository, the GitHub integration appears in Visual Studio Code automatically.

### Install Visual Studio Code on Windows, Linux, and macOS

The [VS Code home page](https://code.visualstudio.com/) should detect your operating system automatically. However, for OS specific instructions here are direct links:

* [Windows](https://code.visualstudio.com/docs/setup/windows)
* [macOS](https://code.visualstudio.com/docs/setup/mac)
* [Linux](https://code.visualstudio.com/docs/setup/linux)

## Install Visual Studio Code extensions

[!INCLUDE[Install Visual Studio Code extension](~/guide/help-content/includes/proc-contribute-install-vscode-extensions.md)]

### Install Docs Authoring Pack

> [!IMPORTANT]
> The Docs Authoring Pack for Visual Studio Code includes basic Markdown authoring assistance, page previews, support for Markdown templates, markdownlint, and Code Spell Checker. These features ease and streamline the contributions process. As such, we consider the Docs Authoring Pack a **required** extension for contributors.

To install the Docs Authoring Pack, select **Install** from the [Docs Authoring Pack page](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack) in the Visual Studio Marketplace.

To use the Docs Authoring Pack functionality, press <kbd>Alt</kbd> + <kbd>M</kbd> in Visual Studio Code. For more information, see [Docs Authoring Pack for Visual Studio Code](how-to-write-docs-auth-pack.md).

## Understand Markdown editors

Markdown is a lightweight markup language used to author the content. [Visual Studio Code](https://code.visualstudio.com/) is the preferred tool for editing Markdown at Microsoft. [Atom](https://atom.io) is another popular tool for editing Markdown. Markdown basics and the features supported by Open Publishing Services (OPS) custom Markdown extensions, are covered in the [Markdown Reference](markdown-reference.md) article.

## Next steps

In this step you installed content authoring tools. In the next step, you will setup a local Git repository.

> [!div class="nextstepaction"]
> [Set up a local Git repository](get-started-setup-local.md)
