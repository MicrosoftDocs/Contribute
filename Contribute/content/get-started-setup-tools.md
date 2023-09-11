---
title: Install content-authoring tools
description: This article helps you download and install the client tools you'll need for using Git and editing Markdown files to edit documentation on Microsoft Learn.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
author: jasonwhowell
ms.author: jasonh
ms.date: 09/11/2023
---

# Install content-authoring tools

This article describes how to install the recommended tools you need to make efficient in-depth or large contributions to Microsoft Learn. Examples of major updates include:

- Lengthy revisions to multiple articles
- Any work with a table of contents besides adding a new article
- Work for which you'd want to use all the available custom extensions

> [!IMPORTANT]
> If you're making only minor changes, you *don't* need to complete the steps in this article. See [Edit in the browser](how-to-write-quick-edits.md) to learn how to make quick edits without installing any tools.

Contributors who'll be making major changes are encouraged to complete these steps. Even if you have write permissions in the main repository, *we highly recommend (and this guide assumes) that you fork and clone the repository* so that you have read/write permissions to store your proposed changes in your fork.

In this article, you'll:

> [!div class="checklist"]
> * Install [Git](https://git-scm.com/)
> * Install [Visual Studio Code](https://code.visualstudio.com/)
> * Install the [Learn Authoring Pack](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack)

::: zone pivot="windows-os-pivot-selection"

## Install Git client tools for Windows

This installation includes the Git version control system and Git Bash, the command-line app that you use to interact with your local Git repository.

1. Download [Git for Windows](https://git-scm.com/download/win).

1. Run the downloaded executable (.EXE) file and follow the prompts to install. Select **Next** at each prompt to accept all default settings.

1. Select a code editor, when prompted. The default code editor is Vim.

1. Select **Finish** to complete the installation.

After installing Git for Windows, configure your Git name and your email address, and then install Visual Studio Code, as described below.

::: zone-end

::: zone pivot="mac-os-pivot-selection"

## Install Git client tools for Mac and Linux

- Git for Mac is provided as part of the Xcode Command Line Tools. Simply run `git` from the command line. You will be prompted to install the command line tools if needed. You can also download [Git for Mac](https://git-scm.com/download/mac) from the Software Freedom Conservancy.
- [Git for Linux and Unix](https://git-scm.com/download/linux)

Follow the instructions for your chosen client for installation and configuration.

::: zone-end

## Install Visual Studio Code

[Visual Studio Code](https://code.visualstudio.com/) is a lightweight editor that works on Windows, Linux, and Mac. It includes Git integration and support for extensions.

> [!TIP]
> To launch VS Code and open the current folder, run the command `code .` in the command line or bash shell. If the current folder is part of a local git repo, the GitHub integration appears in Visual Studio Code automatically.

Download and install Visual Studio Code for your operating system:

- [Windows](https://code.visualstudio.com/). The VS Code home page should detect your operating system correctly.
- [Mac](https://code.visualstudio.com/docs/setup/mac)
- [Linux](https://code.visualstudio.com/docs/setup/linux)

During installation, accept all default settings.

## Install Visual Studio Code extensions

[!INCLUDE[Install Visual Studio Code extension](~/guide/help-content/includes/proc-contribute-install-vscode-extensions.md)]

### Install Learn Authoring Pack

The Learn Authoring Pack for Visual Studio Code includes basic Markdown authoring assistance, page previews, support for Markdown templates, markdownlint, and Code Spell Checker. These features ease and streamline the contribution process. As such, we consider the Learn Authoring Pack a **required** extension for contributors.

To install the Learn Authoring Pack, choose **Install** from the [Learn Authoring Pack page](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack) in the VS Code Marketplace.

To use the Learn Authoring Pack functionality, press Alt+M in Visual Studio Code. To configure a toolbar to show the functions available, edit the Visual Studio Code settings (Control+comma), and add user setting `"markdown.showToolbar": true`.

For more information, see [Learn Authoring Pack for Visual Studio Code](how-to-write-docs-auth-pack.md).

## Understand Markdown editors

Markdown is a lightweight markup language used to author the content. [Visual Studio Code](https://code.visualstudio.com/) is the preferred tool for editing Markdown at Microsoft. Other Markdown editing tools are available. The [Markdown Reference](markdown-reference.md) article covers Markdown basics and the features supported by Open Publishing Services custom Markdown extensions.

## Next steps

Now you're ready to [Set up a local Git repository](get-started-setup-local.md).
