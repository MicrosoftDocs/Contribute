---
title: Git and GitHub essentials for Microsoft Learn documentation
description: This article defines key terms, provides an overview of Git and GitHub repositories, and explains how content is organized for Microsoft Learn documentation.
author: carlyrevier
ms.author: cahublou
ms.topic: contributor-guide
ms.service: learn
ms.custom: external-contributor-guide
ms.date: 01/25/2024
---

# Git and GitHub essentials for Microsoft Learn documentation

## Overview

As a contributor to Microsoft Learn documentation, you'll interact with multiple tools and processes. You'll work in parallel with other contributors on the same project, potentially the exact same content, even at the same time. This is all enabled through Git and GitHub software.

Git is an open-source version control system. It facilitates this type of project collaboration through *distributed version control* of files that live in *repositories*. In essence, Git makes it possible to integrate streams of work done by multiple contributors over time, for a given repository.

GitHub is a web-based hosting service for Git repositories, such as those used to store [Microsoft Learn](/) content. For any project, GitHub hosts the main repository, from which contributors can make copies for their own work.

This article defines key terms that are part of the Microsoft Learn workflow. It also provides an overview of Git and GitHub repositories, and explains how content is organized for Microsoft technical documentation.

## Branch

Branches separate streams of work (typically referred to as versions). Contributions are always made and scoped to a specific branch.

Isolating related changes to a specific branch allows you to control and introduce those changes independently. In reality, depending on the type of work you do, you can easily end up with several working branches in your repository. It's not uncommon to be working on multiple branches at the same time, each representing a different project.

All repositories contain a default branch (typically named "main") and one or more work-in-progress branches (which we call working branches) that have not yet been integrated into the default branch. The default branch serves as the current version and "single source of truth" for the project. It's the parent from which all other branches in the repository are created.

Every time you introduce a new set of logically related changes, it’s a best practice to create a working branch to manage your changes. We don't recommend making changes to the default branch directly.

## Fork

This term is normally used as a noun when referring to a copy of a main GitHub repository. In practice, a fork is just another repository. But it's special in the sense that GitHub maintains a connection back to the main/parent repository. This term is sometimes used as a verb, as in "You must fork the repository first."

## Git

If you're familiar with centralized version control systems (such as Team Foundation Server, SharePoint, or Visual SourceSafe), you'll notice that Git has a unique contribution workflow and terminology to support its distributed model. For instance, there's no file locking that's normally associated with check-out/check-in operations. Instead, Git is concerned about changes at an even finer level, comparing files byte by byte.

Git also uses a tiered structure to store and manage content for a project:

- *Repository*: Also known as a *repo*, this is the highest unit of storage. A repository contains one or more branches.
- *Branch*: A unit of storage that contains the files and folders that make up a project's content set. For more on branches, see the [Branch](#branch) section of this article.

Contributors interact with Git to update and manipulate repositories at both the local and GitHub levels:

- Locally through tools such as the Git Bash console, which supports Git commands for managing local repositories and communicating with GitHub repositories.
- Via [www.github.com](https://www.github.com), which integrates Git to manage the reconciliation of contributions that flow back into the main repository.

## GitHub

> [!NOTE]
> Although the documentation guidance is based on using GitHub, some teams use Visual Studio Team Services to host Git repositories. The Visual Studio Team Explorer client provides a GUI for interacting with Team Services repositories, as an alternative to using Git commands through a command line.
> </br>
> Also, many of the following guidelines were developed as best practices from years of experience in hosting Azure service content in GitHub. They might be required in some Microsoft Learn repositories.

All workflows begin and end at the GitHub level, where the main repository for any documentation project is stored. The copies that contributors create for their own use are distributed across multiple computers. These copies are eventually reconciled back into the project's main GitHub repository.

### Directory organization

A project's default branch serves as the current version of content for the project. The content in the default branch--and branches created from it--is loosely aligned with the organization of the articles on the corresponding Microsoft Learn pages. Subdirectories are used to separate like articles (such as services), media content (such as image files), and "include" files (which enable reuse of content).

#### Articles subdirectory

You can typically find a main `articles` directory off the root of the repository. The `articles` directory contains a set of subdirectories Articles in the subdirectories are formatted as Markdown files that use an *.md* extension. Some repositories that support multiple services use a
generic `/articles` subdirectory, such as the [Azure-Docs](https://github.com/MicrosoftDocs/Azure-Docs) repository. Others might use a
service-specific name, such as the [IntuneDocs](https://github.com/MicrosoftDocs/IntuneDocs) repository, which uses `/IntuneDocs`.

Within the root of this directory, you can find general articles that relate to the overall service or product. And typically, you can then find another series of subdirectories that match the features/services or common scenarios. For instance, Azure "virtual machine" articles are in the `/virtual-machines` subdirectory, and Intune "understand and explore" articles are in the `/understand-explore` subdirectory.

#### Media subdirectory

Each article directory contains a `/media` subdirectory for corresponding media files. Media files contain images used by articles that have image references.

#### Includes subdirectory

Whenever we have reusable content that is shared across two or more articles, it is placed in an `/includes` subdirectory off the main `articles` directory. In a Markdown file that uses the include file, a corresponding "include" Markdown extension is placed in the location where the include file needs to be referenced.

See [Markdown reference: Includes](markdown-reference.md#included-markdown-files) for additional guidance.

### Markdown file template

For convenience, the root directory of each repository typically contains a Markdown template file named `template.md`. You can use this template file as a "starter file" if you need to create a new article for submission to the repository. The file contains:

- A **metadata header** at the top of the file, delineated by two, 3-hyphen lines. It contains the various tags used for tracking information related to the article. Article metadata enables certain functionality, such as author attribution, contributor attribution, breadcrumbs, and article descriptions. It also includes SEO optimizations and reporting processes that Microsoft uses to evaluate the performance of the content. So the metadata is important!
- A **metadata section** that describes the various metadata tags and values. If you're unsure of the values to use for the metadata section, you can leave them blank or comment them with a leading hashtag (#), and they will be reviewed/completed by the pull request reviewer for the repository.
- Various **examples of using Markdown** to format the elements of an article.
- General **instructions on the use of Markdown extensions**, which you can use for various types of alerts.
- Examples of **embedding video** by using an iframe.
- General **instructions on the use of Microsoft technical documentation extensions**, which you can use for special controls such as buttons and selectors.

## Origin

This term is the name assigned to the connection between your local repository and the repository from which it was cloned. In the Microsoft Learn workflow, the origin represents the connection to your fork. This term is sometimes used as a moniker for the origin repository itself, as in "Remember to push your changes to the origin."

## Pull requests

A *pull request* (PR) is a request for a content owner to pull your changes into the official source. A PR enables GitHub's collaboration model by asking for the changes (also known as *commits*) from your working branch to be pulled and merged into another branch. In most cases, that other branch is the default branch in the main repository.

A PR also serves as a mechanism to provide the contributor with feedback from Microsoft Learn's validation processes and the PR reviewer to resolve issues or questions before the changes are merged into the default branch.

## Remote

A *remote* is a named connection to a remote repository, such as the "origin" or "upstream" remote. Git refers to this as a remote because it's used to reference a repository that's hosted on another computer. In the Microsoft Learn workflow, a remote is always a GitHub repository.

## Upstream

Like the origin remote, *upstream* is a named connection to another repository. In the Microsoft Learn workflow, the upstream represents the connection between your local repository and the main repository from which your fork was created. This term is sometimes used as a moniker for the upstream repository itself, as in "Remember to pull the latest changes from the upstream."

## Learn more

If you're unfamiliar with Git or GitHub, these resources can help you learn, be productive, or answer questions.

### Git source-control resources

- [Pro Git e-book (web)](https://go.microsoft.com/fwlink/?linkid=853940): A thorough Git reference, in HTML format.
- [Pro Git e-book (PDF)](https://progit2.s3.amazonaws.com/en/2016-03-22-f3531/progit-en.1084.pdf): Same as the preceding link, in PDF form.
- [Learn Git course from Codecademy](https://www.codecademy.com/learn/learn-git)
- [Try Git course from Code School on Pluralsight](https://www.pluralsight.com/courses/code-school-git-real)

### GitHub resources

- [GitHub Hello World quickstart exercise](https://docs.github.com/get-started/quickstart/hello-world): Online tutorial that exposes you to the basics of Git using GitHub.
- [GitHub Guides](https://guides.github.com/): The home of GitHub documentation.
- [GitHub learning resources](https://help.github.com/articles/git-and-github-learning-resources/): Other useful GitHub resources.
- [Glossary](https://help.github.com/articles/github-glossary): A handy glossary of Git and GitHub terms.
- [GitHub student developer pack](https://education.github.com/pack): Free access to the best developer tools for students.

## FAQs

### What's Git?

Git helps keep track of changes when many people work on computer code together. It's like a time machine for code, so you can see what changed and go back if needed.

### Why use Git?

It's great for teamwork. Git makes it easy for lots of people to work on the same project without messing up each other's work. It also helps to fix mistakes easily.

### How does Git work?

Git stores all the versions of a project's code. When you make changes, Git takes a picture (like a snapshot) of what's different. You can make different versions at the same time without a problem.

### What are branches in Git?

Branches are like different paths in a project. They let people work on new things without changing the main project. Later, they can bring these changes back into the main project.

### What is a commit in Git?

A commit is like a save point. It's a way to record changes you made. Each commit has a unique ID and a note about what was changed.

### What is GitHub?

GitHub is a website where you can store your Git projects. It's like a big hub for sharing and working together on code with others. It also helps in keeping track of who changed what.

### How is GitHub different from Git?

Git is the tool for tracking changes, while GitHub is the place to store your projects and work together. GitHub uses Git to do its magic.

### Is GitHub free?

Yes, for projects everyone can see. But for private projects (only you and your team), you might need to pay. They offer different plans with extra features.

### What are pull requests in GitHub?

Pull requests are like asking to put your changes into the main project. People can review and discuss the changes before they're added.

### How safe is GitHub?

GitHub takes good care of security. They use special codes and rules to make sure only the right people can access and change your code. You can also add extra security layers like two-factor authentication for more safety.
