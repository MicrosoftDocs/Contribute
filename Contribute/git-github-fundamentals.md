---
title: Git and GitHub essentials for Documentation
description: This article explains an overview of Git,  GitHub repository, and how content is organized, and naming conventions used for docs.microsoft.com.
ms.date: 06/30/2017
---
# Git and GitHub essentials for Docs

## Overview

As a contributor to Docs content, you will interact with multiple tools and processes. You'll work in parallel with other contributors on the same project, potentially the exact same content, even at the same time. This is all enabled through Git and GitHub software.

Git is an open-source version control system. It facilitates this type of project collaboration through *distributed version control* of files that live in *repositories*. In essence, Git makes it possible to integrate streams of work done by multiple contributors over time, for a given repository.

GitHub is a web-based hosting service for Git repositories, such as those used to store [docs.microsoft.com](https://docs.microsoft.com) content. For any project, GitHub hosts the main repository, from which contributors can make copies for their own work.

## Git

If you're familiar with centralized version control systems (such as Team Foundation Server, SharePoint, or Visual SourceSafe), you will notice that Git has a unique contribution workflow and terminology to support its distributed model. For instance, there is no file locking that is normally associated with check-out/check-in operations. As a matter of fact, Git is concerned about changes at an even finer level, comparing files byte by byte.

Git also uses a tiered structure to store and manage content for a project:

- *Repository*: Also known as a *repo*, this is the highest unit of storage. A repository contains one or more branches.
- *Branch*: A unit of storage that contains the files and  folders that make up a project's content set. Branches separate streams of work (typically referred to as versions). Contributions are always made and scoped to a specific branch. All repositories contain a default branch (typically named "master") and one or more branches that are destined to be merged back into the master branch. The master branch serves as the current version and "single source of truth" for the project. It's the parent from which all other branches in the repository are created.

Contributors interact with Git to update and manipulate repositories at both the local and GitHub levels:

- Locally through tools such as the Git Bash console, which supports Git commands for managing local repositories and communicating with GitHub repositories.
- Via [www.github.com](https://www.github.com), which integrates Git to manage the reconciliation of contributions that flow back into the main repository.

## GitHub

> [!NOTE]
> Although Docs guidance is based on using GitHub, some teams use Visual Studio Team Services to host Git repositories. The Visual Studio Team Explorer client provides a GUI for interacting with Team Services repositories, as an alternative to using Git commands through a command line.
> </br>
> Also, many of the following guidelines were developed as best practices from years of experience in hosting Azure service content in GitHub. They might be required in some Docs repositories.

All workflows begin and end at the GitHub level, where the main repository for any Docs project is stored. The copies that contributors create for their own use are distributed across multiple computers. These copies are eventually reconciled back into the project's main GitHub repository.

### Directory organization

As mentioned earlier, a project's default/master branch serves as the current version of content for the project. The content in the master branch--and branches created from it--is loosely aligned with the organization of the articles on the corresponding Docs pages. Subdirectories are used for separation of like content (such as services), media content (such as image files), and "include" files (which enable reuse of content).

You can typically find a main `articles` directory off the root of the repository. The articles directory contains a set of subdirectories. Articles in the subdirectories are formatted as Markdown files that use an *.md* extension. Some repositories that support multiple services use a generic `/articles` subdirectory, such as the [https://github.com/MicrosoftDocs/Azure-Docs](https://github.com/MicrosoftDocs/Azure-Docs) repository. Others might use a service-specific name, such as the [https://github.com/MicrosoftDocs/IntuneDocs](https://github.com/MicrosoftDocs/IntuneDocs) repository, which uses `/IntuneDocs`.

Within the root of this directory, you can find general articles that relate to the overall service or product. And typically, you can then find another series of subdirectories that match the features/services or common scenarios. For instance, Azure "virtual machine" articles are in the `/virtual-machines` subdirectory, and Intune "understand and explore" articles are in the `/understand-explore` subdirectory.

### Media subdirectory

Each article directory contains a `/media` subdirectory for corresponding media files. Media files contain images used by articles that have image references.

### Includes subdirectory

Whenever we have reusable content that is shared across two or more articles, it is placed in an `/includes` subdirectory off the main `articles` directory. In a Markdown file that uses the include file, a corresponding "include" Markdown extension is placed in the location where the include file needs to be referenced.

See [How to use Markdown: Includes](how-to-write-use-markdown.md#includes) for additional guidance.

### Markdown file template

For convenience, the root directory of each repository typically contains a Markdown template file named `template.md`. You can use this template file as a "starter file" if you need to create a new article for submission to the repository. The file contains:

- A **metadata header** at the top of the file, delineated by two, 3-hyphen lines. It contains the various tags used for tracking information related to the article. Article metadata enables certain functionality, such as author attribution, contributor attribution, breadcrumbs, and article descriptions. It also includes SEO optimizations and reporting processes that Microsoft uses to evaluate the performance of the content. So the metadata is important!
- A **metadata section** that describes the various metadata tags and values. If you're unsure of the values to use for the metadata section, you can leave them blank or comment them with a leading hashtag (#), and they will be reviewed/completed by the pull request reviewer for the repository.
- Various **examples of using Markdown** to format the elements of an article.
- General **instructions on the use of Markdown extensions**, which you can use for various types of alerts.
- Examples of **embedding video** by using an iframe.
- General **instructions on the use of docs.microsoft.com extensions**, which you can use for special controls such as buttons and selectors.

## Pull requests

A *pull request* provides a convenient way for a contributor to propose a set of changes that will be applied to the default branch. The changes (also known as *commits*) are stored in a contributor's branch, so GitHub can first model the impact of *merging* them into the default branch. A pull request also serves as a mechanism to provide the contributor with feedback from a build/validation process, the pull request reviewer, to resolve potential issues or questions before the changes are merged into the default branch.

There are two ways to contribute by pull request, depending on the size of changes that you want to propose. We will cover this in detail later, in the [GitHub workflow](how-to-write-workflows-major.md) section of this guide.

<!---- Reference links for Docs landing pages, associated GitHub repositories, and related Forums matrix. ------------------>
<!---- PLEASE INSERT URLS IN ASCENDING SORT ORDER, AND REMOVE LOCALE SEGMENT FROM URLS (that is, en-us) FOR LOCALIZED FORUMS! -->
<!---- NOTE: these links are saved for future use in another/new article; no longer used above in this article --->
[Visual-Studio-Page]:(https://docs.microsoft.com/en-us/visualstudio/index)
[Visual-Studio-Repo-Internal]:(https://github.com/Microsoft/vsdocs)
[Visual-Studio-Repo-External]:(https://github.com/Microsoft/visualstudio-docs)
[Visual-Studio-SO]: (https://stackoverflow.com/search?q=Visual+Studio+2017)
[Dotnet-Page]: https://docs.microsoft.com/dotnet
[Dotnet-Core-Page]: https://docs.microsoft.com/dotnet/articles/welcome
[Dotnet-Core-Repo]: https://github.com/dotnet/docs
[EM-ATA-Land]: https://docs.microsoft.com/advanced-threat-analytics/
[EM-ATA-Repo]: https://github.com/Microsoft/ATADocs
[EM-AzureAD-Land]: https://docs.microsoft.com/active-directory/
[EM-AzureAD-Repo]: https://github.com/Azure/azure-content/tree/master/articles/active-directory/
[EM-AzureRMS-Land]: https://docs.microsoft.com/rights-management/
[EM-AzureRMS-Repo]: https://github.com/Microsoft/Azure-RMSDocs
[EM-Intune-Land]: https://docs.microsoft.com/intune/
[EM-Intune-Repo]: https://github.com/microsoft/intuneDocs
[EM-Land-Page]: https://docs.microsoft.com/enterprise-mobility/
[EM-Land-Repo]: https://github.com/Microsoft/EMDocs/
[EM-MFA-Land]: https://docs.microsoft.com/multi-factor-authentication/
[EM-MFA-Repo]: https://github.com/Azure/azure-content/tree/master/articles/multi-factor-authentication
[EM-MIM-Land]: https://docs.microsoft.com/microsoft-identity-manager/
[EM-MIM-Repo]: https://github.com/Microsoft/MIMDocs
[EM-RemoteApp-Land]: https://docs.microsoft.com/en-us/remoteapp/
[EM-RemoteApp-Repo]: https://github.com/Azure/azure-content/tree/master/articles/remoteapp
[Forum-MSDN-ATA]: https://social.technet.microsoft.com/Forums/en-US/home?forum=mata
[Forum-MSDN-AzureAD]: https://social.msdn.microsoft.com/Forums/en-US/home?forum=WindowsAzureAD
[Forum-MSDN-AzureRMS]: https://social.technet.microsoft.com/Forums/en-US/home?forum=rmsapps%2Crmscloud&filter=alltypes&sort=lastpostdesc
[Forum-MSDN-EM]: https://social.technet.microsoft.com/Forums/en-US/home?sort=relevancedesc&brandIgnore=True&searchTerm=Enterprise+Mobility
[Forum-MSDN-Intune]: https://social.technet.microsoft.com/Forums/en-us/home?category=microsoftintune
[Forum-MSDN-Main]: https://social.msdn.microsoft.com/Forums/home
[Forum-MSDN-MFA]: https://social.msdn.microsoft.com/Forums/en-US/home?forum=windowsazureactiveauthentication
[Forum-MSDN-MIM]: https://social.technet.microsoft.com/Forums/en-US/home?category=identitymanagement
[Forum-MSDN-RemoteApp]: https://social.technet.microsoft.com/Forums/en-US/home?filter=alltypes&brandIgnore=True&sort=relevancedesc&searchTerm=Azure+Remote+or+RemoteApp
[Forum-SO-AzureAD]: https://stackoverflow.com/questions/tagged/azure-active-directory
[Forum-SO-AzureRMS]: https://stackoverflow.com/questions/tagged/rights-management
[Forum-SO-Dotnet]: https://stackoverflow.com/questions/tagged/.net
[Forum-SO-Dotnet-Core]: https://stackoverflow.com/questions/tagged/.net-core
[Forum-SO-Main]: https://stackoverflow.com/tags
[Forum-SO-Intune]: https://stackoverflow.com/questions/tagged/intune
[Forum-SO-MFA]: https://stackoverflow.com/search?q=%5Bazure%5D+multi-factor
[Forum-SO-MIM]: https://stackoverflow.com/search?q=Microsoft+Identity+Manager
[Forum-SO-RemoteApp]: https://stackoverflow.com/questions/tagged/remoteapp
[Forum-TechNet-Main]: https://social.technet.microsoft.com/Forums/home
[Forum-Yammer-AzureRMS]: https://www.yammer.com/AskIPTeam
[Forum-Yammer-Main]: https://www.yammer.com/
