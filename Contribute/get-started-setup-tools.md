---
title: Install content authoring tools
description: This article helps you download and install the client tools you will need for Git and editing markdown files.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
author: jasonwhowell
ms.author: jasonh
ms.date: 04/30/2018
---
# Install content authoring tools

This article describes the steps to interactively install Git client tools and Visual Studio Code.
> [!div class="checklist"]
> * Install [Git](https://git-scm.com/)
> * Install [Visual Studio Code](https://code.visualstudio.com/)
> * Install [Docs Authoring Pack](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack)

>[!IMPORTANT]
> If you're making only minor changes to an article, you *do not* need to complete the steps in this article and can continue directly to the [quick changes workflow](index.md#quick-edits-to-existing-documents).
>
> Major contributors are encouraged to complete these steps, which enable you to use the [major/long-running changes workflow](how-to-write-workflows-major.md). Even if you have write permissions in the main repository, *we highly recommend (and this guide assumes) that you fork and clone the repository*, so that you have read/write permissions to store your proposed changes in your fork.

## Install Git client tools 

 Install the latest version of [Software Freedom Conservancy's Git client tools](https://git-scm.com/download/) for your platform. 

* [Git for Windows](https://git-scm.com/download/win). This install includes the Git version control system and Git Bash, the command-line app that you use to interact with your local Git repository.
* Git for Mac is provided as part of the Xcode Command Line Tools. Simply run `git` from the command line. You will be prompted to install the command line tools if needed. You can also download [Git for Mac](https://git-scm.com/download/mac) from the Software Freedom Conservancy.
* [Git for Linux and Unix](https://git-scm.com/download/linux)

If you prefer a graphical user interface (GUI) over a command-line interface (CLI), see [Software Freedom Conservancy's available GUI Clients page](https://git-scm.com/downloads/guis), [GitHub's GitHub Desktop](https://desktop.github.com/), or [Visual Studio Code](https://www.visualstudio.com/products/code-vs.aspx) for some popular options.

Follow the instructions for your chosen client for installation and configuration.

In the next article, you will [Set up a local Git repository](get-started-setup-local.md).

   Additional Git resources are available here: [Git terminology](https://help.github.com/articles/github-glossary) | [Git basics](https://git-scm.com/book/en/v2/Getting-Started-Git-Basics) | [Learning Git and GitHub](https://help.github.com/articles/good-resources-for-learning-git-and-github/)

## Understand Markdown editors

Markdown is a lightweight markup language that is both easy to read and easy to learn. Therefore, it has rapidly become an industry standard. To write articles in Markdown, we recommend that you first download and install a Markdown editor.  [Visual Studio Code](https://code.visualstudio.com/) is the preferred tool for editing Markdown at Microsoft. [Atom](https://atom.io) is another popular tool for editing Markdown.

Markdown text is saved into files with .md extension.

Additional details on how to write with Markdown, including Markdown basics and the features supported by Open Publishing Services (OPS) custom Markdown extensions, are covered in the [Markdown Reference](markdown-reference.md) article.

## Visual Studio Code

[Visual Studio Code](https://code.visualstudio.com/), also known as VS Code, is a lightweight editor that works on Windows, Linux, and Mac. It includes git integration, and support for extensions.

Download and install [VS Code](https://code.visualstudio.com/). The VS Code home page should detect your operating system correctly.

- [Windows](https://code.visualstudio.com/docs/setup/windows)
- [Mac](https://code.visualstudio.com/docs/setup/mac)
- [Linux](https://code.visualstudio.com/docs/setup/linux)

> [!TIP]
> To launch VS Code and open the current folder, run the command `code .` in the command line or bash shell. If the current folder is part of a local git repo, the GitHub integration appears in Visual Studio Code automatically.

## Docs Authoring Pack
Install the Docs Authoring Pack for Visual Studio Code. This set of extensions includes basic authoring assistance for help when writing Markdown, and a preview feature, so that you can see what the Markdown looks like in the style of the docs.microsoft.com site.

   Visit this [marketplace page](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack) and select **Install**, or search for `docsmsft.docs-authoring-pack` in your extensions list in the VS Code window. 

   The Docs Authoring Pack is accessible by pressing Alt+M inside of VS Code. The toolbar is hidden by default but can be shown. Edit the VS Code settings (Control+comma) and adding user setting `"markdown.showToolbar": true` to show the toolbar.

   For more information, see the [Docs Authoring Pack](how-to-write-docs-auth-pack.md) page.


## Next steps

Now you are ready to [Set up a local Git repository](get-started-setup-local.md).
