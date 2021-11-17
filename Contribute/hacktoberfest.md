---
title: Hacktoberfest and Microsoft Docs
description: Learn how to discover which Docs repositories participate in Hacktoberfest, how to contribute, and what you can expect as a contributor.

author: IEvangelist
ms.author: dapine
ms.date: 09/10/2021
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
---
# Hacktoberfest and Microsoft Docs

Test

Hacktoberfest is an annual worldwide event held during the month of October. The event encourages open source developers to contribute to repositories through pull requests (PR). GitHub hosts many Microsoft Docs open source repositories, all of which contribute to the [docs.microsoft.com](https://docs.microsoft.com) content. Some of the repositories actively participate in the Hacktoberfest event. In this article, you'll learn how to discover which repos are accepting PRs, and what you can expect as a contributor.

## Find a repo

To discover if a Docs repo is participating in Hacktoberfest, you'll see the **hacktoberfest** topic on the project.

:::image type="content" source="media/hacktoberfest/github-topic.png" lightbox="media/hacktoberfest/github-topic.png" alt-text="GitHub .NET docs repository with hacktoberfest topic.":::

To filter all Microsoft Docs and .NET repos that have the **hacktoberfest** topic, see [GitHub Topics: Hacktoberfest](https://github.com/topics/hacktoberfest?q=org%3AMicrosoftDocs+org%3Adotnet).

Alternatively, a repository may choose to use the `Hacktoberfest` label instead. This label is convenient for filtering issues. For more information, see [Filtering issues and pull requests by labels](https://docs.github.com/github/administering-a-repository/finding-information-in-a-repository/filtering-issues-and-pull-requests-by-labels).

## Contribute

To contribute to an open source Docs repo, you must first configure your account to contribute to Microsoft Docs. If you have never completed this process, start by [signing up for a GitHub account](./get-started-setup-github.md).

Once your account is configured, start by reading through and adhering to the _CONTRIBUTING.md_ file at the root of the repository you want to contribute to. These files serve as a guide when contributing. Here are a few example contributor guides from some popular Docs repos:

- [Contribute to the .NET docs repositories](dotnet/dotnet-contribute.md)
- [Contribute to Microsoft Azure documentation](https://github.com/MicrosoftDocs/azure-docs/blob/master/CONTRIBUTING.md)

In addition to the contributing Markdown file, if a repository has a *CODE_OF_CONDUCT.md* file, it's a requirement to adhere to the expected behavior in the community. Again, here are a few common examples:

- [.NET Docs: Code of Conduct](https://github.com/dotnet/docs/blob/main/CODE_OF_CONDUCT.md)
- [Azure Docs: Code of Conduct](https://github.com/MicrosoftDocs/azure-docs/blob/master/CODE_OF_CONDUCT.md)

### Choose an issue

To find an issue to work on in a participating repository, filter the issues for either the `up-for-grabs` or `help-wanted` GitHub labels. While you can address other issues, it's easier to focus on issues that have a well-defined scope and are self-contained. In addition to the Docs repos, you can use the following sites for beginners:

- [Awesome for beginners](https://github.com/mungell/awesome-for-beginners)
- [Up for grabs](https://up-for-grabs.net)
- [First timers only](https://www.firsttimersonly.com)

For more information, see [Hacktoberfest: Beginners](https://hacktoberfest.digitalocean.com/resources/beginners).

### Quality expectations

To have a successful contribution to an open source Docs repository, [create a meaningful and impactful PR](#open-a-pr). The following examples from the official Hacktoberfest site are considered ***low-quality contributions***:

- PRs that are automated (for example, scripted opening PRs to remove whitespace, fix typos, or optimize images).
- PRs that are disruptive (for example, taking someone else's branch or commits and making a PR).
- PRs that are regarded by a project maintainer as a hindrance vs. helping.
- A submission that's clearly an attempt to simply +1 your PR count for October.

Finally, one PR to fix a typo is fine, but five PRs to remove a stray whitespace are not.

For more information, see [Hacktoberfest: Quality standards](https://hacktoberfest.digitalocean.com/resources/qualitystandards).

### Open a PR

A *PR* provides a convenient way for a contributor to propose a set of changes. When opening a PR, specify in the original comment that it's intended to contribute to *hacktoberfest*. Successful PRs have these common characteristics:

- The PR adds value.
- The contributor is receptive to feedback.
- The intended changes are well articulated.
- The changes are related to an existing issue.

If you're proposing a PR without a corresponding issue, create an issue first. For more information, see [GitHub: About pull requests](https://docs.github.com/github/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/about-pull-requests).

## See also

- [GitHub account setup](get-started-setup-github.md)
- [Git and GitHub essentials for Docs](git-github-fundamentals.md)
- [Official Hacktoberfest site](https://hacktoberfest.digitalocean.com)