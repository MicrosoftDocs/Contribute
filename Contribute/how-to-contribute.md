---
title: How to contribute to docs.microsoft.com
description: This article describe different ways you can contribute content to docs.microsoft.com.
author: billwagner
ms.author: wiwagn
manager: wpickett
ms.date: 01/17/2018
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.custom: external-contributor-guide
---
# How to contribute to docs.microsoft.com

There are several ways to participate in improving the content that makes up [docs.microsoft.com](https://docs.microsoft.com):

- You can [create issues](#create-issues) to recommend new articles, or improve existing articles.
- You can [quickly edit](#quick-edits) articles to make small changes in the GitHub online editor.
- You can [review drafts of new articles](#review-new-articles) to ensure quality and technical accuracy.
- You can [create new articles](#create-new-articles) for topics when you want to help drive the content story.
- You can [update](#update-samples) or [create](#create-samples) samples to improve the code samples that reinforce important concepts.

In this article, you'll learn the different ways to contribute, see how to accomplish each of those tasks, and find pointers to more information about each of those tasks.

Our public repositories are hosted on [GitHub](https://wwww.GitHub.com).  You will need to create an account on GitHub to participate in our documentation repositories.

You'll also need a text editor to update the documents. We recommend [Visual Studio Code](https://www.visualstudio.com/code). You should have a basic understanding of [Markdown](https://daringfireball.net/projects/markdown/syntax) syntax.

If you are adding or modifying samples, you'll need a development environment. We recommend [Visual Studio](https://www.visualstudio.com) on PC and Mac, or [Visual Studio Code](https://www.visualstudio.com/code) on all platforms.

## Create issues

If you find omissions or inaccuracies in a article, create an issue against that article. The easiest way to find the right location is to click the "Edit" button in your browser, which will take you to the article source in the correct public GitHub repository. From there, you can retrieve the URL for the source of the article from your address bar. Click "Create Issue" to make a new issue on the article.

> [!NOTE]
> If you find issues you can fix with small edits, such as typing mistakes or grammar issues, you can save yourself and us time by [submitting the fix](#quick-edits) using the browser to edit the source.

Most of our public repos contain templates for new issues that will guide you to provide the information needed to fix the issue.

You can also contribute new issues where you can't find the information you need. The process is the same: create a new issue on one of the public docs repositories. Tell us what you were searching for, what you wanted to do, and why the articles you found did not help the way you expected.

## Review new articles

If you are working on new, possibly CTP or beta, software, we are likely building the docs as you are exploring the technology. You can find the in-process docs in our public repositories. If you have comments, you can help us make them better before they are released.

New articles are reviewed in public, using the [GitHub flow](https://guides.github.com/introduction/flow/) process. Look at any of our docs repositories, and check the open pull requests (PRs). We welcome comments and reviews on any open pull requests. That helps us publish better content on our first release, rather than waiting for feedback after going live.

We are looking for ways to improve technical accuracy, clarity of the descriptions, and grammatical accuracy.

## Quick edits

Quick edits are a way to make small fixes using the browser based editor. If you find small spelling or grammar errors, or mis-named APIs, you can skip creating an issue by making the edit and submitting a PR.

On any article, click the "Edit" button (usually toward the top right-hand side of the page), make your edits, and click "Submit PR" at the bottom of the page. We'll review the PR, and merge it as we do our daily PR review.

## Create new articles

If there are concepts you are passionate about, and want to explain to others, you can create the articles and submit a PR.

Creating new articles is time-consuming, and we value your time and contributions. We want to be involved early in the process to ensure you're following our guidelines and style from the beginning. We recommend the following steps:

1. [Create an issue](#create-issues) describing what's missing and how you'd address it.
1. Comment on the issue, telling us you'd like to work on it, and suggesting an outline and abstract for the article.
1. We'll respond with suggestions. These may include links to related articles, suggestions for samples, or how the article will be organized.
1. Once we agree on the outline, fork the repository, and start working.
1. Early in the process, open a PR, with "[WIP]" at the beginning of the title.
1. One of the core contributors will give you initial feedback.
1. Keep writing, @-mention the person who reviewed the first draft when you're ready for more feedback.
1. Remove the "[WIP]" when you're ready for final review.
1. Respond to the feedback
1. The core contributors will merge your PR.

There are a couple points worth expanding on from that list. In general, we're following the [GitHub flow](https://guides.github.com/introduction/flow/) process to review content as early as possible. That way, we agree on where an article should go in the table of contents, what benefit the reader will get from the new article, and the scope of any samples you'll create. We can make any necessary course corrections early, before you've invested significant time writing.

## Update samples

Some samples may have originally been written several releases ago, using practices no long recommended. You may want to help us update those samples. Or, you may find that a simple variable name change could increase the clarity of an explanation.

The sample code displayed with each article are part of programs that are built and often tested under our CI system.

To make small updates, you find the source in the appropriate repository, make the code change in the browser and submit a PR. Our CI system will build the changes, and we'll merge the PR when it finishes.

For larger scale changes fork the repository and make the changes in your favorite development environment. Make sure you add some tests to ensure that your changes work as you intended. Submit a PR, and we'll review it.

With all code changes, follow the existing code conventions for the sample code you are modifying. Our samples repositories coding standards will mirror those of the corresponding product teams. Check each repository for specific guidance.

> [!NOTE]
> We're working toward following this guidance ourselves. Some of the samples predate our current standards ane have not been updated yet. We are working toward a goal of all running sample code being displayed from working, tested, samples.

## Create samples

You can also create new samples that demonstrate concepts or scenarios. Any samples must be accompanied by a article that explains the key information from the sample.

If your new sample complements an existing article, add a reference to the sample in that article. If not, work with us to [write the article](#create-new-articles) that accompanies the sample.

In all cases, our sample code follows the coding conventions used by the related product teams. One exception is that we are more likely to use explicitly typed varables over implicitly typed (declared with `var`) for clarity when those declarations are included in the article.

Follow the sample process outlined in the earlier section for [new articles](#create-new-articles) so that we can review the code early in the development process.
