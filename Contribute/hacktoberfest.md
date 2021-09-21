---
title: Hacktoberfest and Microsoft docs
description: Learn how to discover which docs repositories participate in Hacktoberfest, how to contribute, and what you can expect as a contributor.
author: IEvangelist
ms.author: dapine
ms.date: 09/10/2021
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
---

# Hacktoberfest and Microsoft docs

Hacktoberfest is an annual world-wide event that drives open source contributions through the month of October. During the month, open source developers are encouraged to contribute to repositories through pull requests (PRs). There are many Microsoft docs open source repositories on GitHub, all of which contribute to the [docs.microsoft.com](https://docs.microsoft.com) content. Some of the repositories actively participate in the Hacktoberfest event. In this article you'll learn how to discover which repos are accepting pull requests, and what you can expect as a contributor.

## Discoverability

To discover if a docs repo is participating in Hacktoberfest, you will see the **hacktoberfest** topic on the project.

:::image type="content" source="media/hacktoberfest/github-topic.png" lightbox="media/hacktoberfest/github-topic.png" alt-text="GitHub .NET docs repository with hacktoberfest topic.":::

To filter all Microsoft docs and .NET repos that have the **hacktoberfest** topic see, [GitHub Topics: Hacktoberfest](https://github.com/topics/hacktoberfest?q=org%3AMicrosoftDocs+org%3Adotnet).

Alternatively, a repository may choose to use the `Hacktoberfest` label instead. This is convenient for filtering issues with &mdash; for more information see, [Filtering issues and pull requests by labels](https://docs.github.com/github/administering-a-repository/finding-information-in-a-repository/filtering-issues-and-pull-requests-by-labels).

## Contribute

To contribute to an open source docs repo, always start by reading through and adhering to the _CONTRIBUTING.md_ file at the root of the repository. These files serve as a guide when making contributions. Here are a few example contributing guides from some popular docs repos:

- [Contribute to the .NET docs repositories](dotnet/dotnet-contribute.md)
- [Contribute to Microsoft Azure documentation](https://github.com/MicrosoftDocs/azure-docs/blob/master/CONTRIBUTING.md)

In addition to the contributing markdown file, if a repository has a *CODE_OF_CONDUCT.md* file &mdash; it is a requirement to adhere to the expected behavior in the community. Again, here are a few common examples:

- [.NET Docs: Code of Conduct](https://github.com/dotnet/docs/blob/main/CODE_OF_CONDUCT.md)
- [Azure Docs: Code of Conduct](https://github.com/MicrosoftDocs/azure-docs/blob/master/CODE_OF_CONDUCT.md)

### Choose an issue

To find an issue to work on in a participating repository, filter the issues with either `up-for-grabs` or `help-wanted` GitHub labels. While other issues can be addressed, it's easier to focus on issues that have a well-defined scope and are self-contained. In addition to the docs repos, you can use the following sites for beginners:

- [Awesome for beginners](https://github.com/mungell/awesome-for-beginners)
- [Up for grabs](https://up-for-grabs.net)
- [First timers only](https://www.firsttimersonly.com)

For more information, see [Hacktoberfest: Beginners](https://hacktoberfest.digitalocean.com/resources/beginners).

### Quality expectations

To have a successful contribution to an open source docs repository, be sure to make a meaningful and impactful [pull request](#make-a-pull-request). The following examples, provided from the official Hacktoberfest site, are considered ***low quality contributions***:


- Pull requests that are automated (e.g. scripted opening pull requests to remove whitespace / fix typos / optimize images).

- Pull requests that are disruptive (e.g. taking someone else's branch/commits and making a pull request).

- Pull requests that are regarded by a project maintainer as a hindrance vs. helping.
- Something that's clearly an attempt to simply +1 your pull request count for October.
- Last but not least, one pull request to fix a typo is fine, but 5 pull requests to remove a stray whitespace is not.

For more information, see [Hacktoberfest: Quality standards](https://hacktoberfest.digitalocean.com/resources/quality-standards).

### Make a pull request

A *pull request* provides a convenient way for a contributor to propose a set of changes. When authoring a pull request, please be specific that it is intended to contribute to *hacktoberfest*. Successful pull requests have these common characteristics:

- The pull request adds value.
- The contributor is receptive to feedback.
- The intended changes are well articulated.
- The changes are related to an existing issue.

If you're proposing a pull request without a corresponding issue, please create an issue first. For more information, see [GitHub: About pull requests](https://docs.github.com/github/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/about-pull-requests).

## See also

- [GitHub account setup](get-started-setup-github.md)
- [Git and GitHub essentials for Docs](git-github-fundamentals.md)
- [Official Hacktoberfest site](https://hacktoberfest.digitalocean.com)
