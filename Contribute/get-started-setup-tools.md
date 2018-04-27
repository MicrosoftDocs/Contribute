---
title: Install content authoring tools
description: This article helps you download and install the client tools you will need for Git and editing markdown files.
author: bryanla
ms.author: bryanla
manager: mbaldwin
ms.date: 01/04/2018
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.custom: external-contributor-guide
---
# Install content authoring tools

This article describes the steps to interactively install Git client tools and Visual Studio Code.
> [!div class="checklist"]
> * Install [Git for Windows](https://git-scm.com/download/win)
> * Install [Visual Studio Code](https://code.visualstudio.com/)

>[!IMPORTANT]
> If you're making only minor changes to an article, you *do not* need to complete the steps in this article and can continue directly to the [quick changes workflow](index.md#quick-edits-to-existing-documents).
>
> Major contributors are encouraged to complete these steps, which enable you to use the [major/long-running changes workflow](how-to-write-workflows-major.md). Even if you have write permissions in the main repository, *we highly recommend (and this guide assumes) that you fork and clone the repository*, so that you have read/write permissions to store your proposed changes in your fork.

## Install Git client tools on Windows

 Install the latest version of [Software Freedom Conservancy's Git client tools](https://git-scm.com/download/). The install includes the Git version control system and Git Bash, the command-line app that you use to interact with your local Git repository.

If you prefer a graphical user interface (GUI) over a command-line interface (CLI), see [Software Freedom Conservancy's available GUI Clients page](https://git-scm.com/downloads/guis), [GitHub's GitHub Desktop](https://desktop.github.com/), or [Visual Studio Code](https://www.visualstudio.com/products/code-vs.aspx) for some popular options.

Follow the instructions for your chosen client for installation and configuration.

In the next article, you will [Set up a local Git repository](get-started-setup-local.md).

   Additional Git resources are available here: [Git terminology](https://help.github.com/articles/github-glossary) | [Git basics](https://git-scm.com/book/en/v2/Getting-Started-Git-Basics) | [Learning Git and GitHub](https://help.github.com/articles/good-resources-for-learning-git-and-github/)

## Understand Markdown editors

Markdown is a lightweight markup language that is both easy to read and easy to learn. Therefore, it has rapidly become an industry standard. To write articles in Markdown, we recommend that you first download and install a Markdown editor.  [Visual Studio Code](https://code.visualstudio.com/) is the preferred tool for editing Markdown at Microsoft. [Atom](https://atom.io) is another popular tool for editing Markdown.

Markdown text is saved into files with .md extension.

Additional details on how to write with Markdown, including Markdown basics and the features supported by OPS custom Markdown extensions, are covered later in the [How to use Markdown](how-to-write-use-markdown.md) article.

## Visual Studio Code

[Visual Studio Code](https://code.visualstudio.com/), also known as VS Code, is a lightweight editor that works on Windows, Linux, and Mac. It includes git integration, and support for extensions.

Download and install [VS Code](https://code.visualstudio.com/). The VS Code home page should detect your operating system correctly.

- [Windows](https://code.visualstudio.com/docs/setup/windows)
- [Mac](https://code.visualstudio.com/docs/setup/mac)
- [Linux](https://code.visualstudio.com/docs/setup/linux)

> [!TIP]
> To launch VS Code and open the current folder, run the command `code .` in the command line or bash shell. If the current folder is part of a local git repo, the github integration appears in Visual Studio Code automatically.

## Next steps

Now you are ready to [Set up a local Git repository](get-started-setup-local.md).
