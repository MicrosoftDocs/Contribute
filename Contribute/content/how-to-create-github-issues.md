---
title: Create GitHub issues for Microsoft Learn documentation
description: Learn how to create issues in GitHub when you spot errors in Microsoft Learn documentation.
author: carlyrevier
ms.author: cahublou
ms.date: 08/28/2023
ms.topic: contributor-guide
ms.service: learn
ms.custom: external-contributor-guide
---

# Create GitHub issues

This article teaches you how to create a GitHub issue for Microsoft Learn documentation. It also teaches you how to peruse other users' issues and either add your own comments to them or open a pull request (PR) to address them.

Our documentation is a continuous work in progress. Receiving good GitHub issues from contributors helps us focus our efforts on the highest priorities for the community.

Of course, if you know how to fix an issue, we invite you to [make the changes yourself](how-to-write-quick-edits.md), instead of opening an issue.

## Prerequisites

- [Create a GitHub account](index.md#create-a-github-account), if you don't have one.

## Create an issue

1. Navigate to the article you want to comment on.
1. Scroll to the bottom of the article, where you'll see options for submitting feedback on either the topic itself or the product. Select the **This page** link to submit feedback on the topic.

    ![Screenshot of the bottom of an article, showing the feedback options.](media/how-to-create-github-issues/feedback-links.png)

    - Selecting **This product** takes you to a destination (for example, UserVoice, GitHub, an email address) where you can provide feedback on the product itself. This feedback is independent of the content and has no relationship back to the original article.
    - Selecting **This page** opens a new issue for you in the GitHub repository that stores the content for the article you're viewing. This feedback is specific to the content and is tracked as an issue in GitHub. 
    - Selecting **View all page feedback** allows you to see all feedback submitted for the article. Anyone can read the feedback, but you must be signed in to comment or leave feedback.

1. The system opens a new issue for you in the GitHub repository that stores the content for the article you're viewing. Replace the **[Enter feedback here]** placeholder with your feedback, add a title, and select **Submit new issue**. Don't change any content in the **Document Details** section.

    :::image type="content" source="media/how-to-create-github-issues/github-issue.png" alt-text="Screenshot of a new issue in GitHub.":::

    The more detail you can provide, the more helpful the issue. Tell us what information you sought. Tell us the search terms you used. If you can't get started, tell us how you want to start exploring unfamiliar technology.

That's it! Your issue is now added to the Issues queue. Issues start the conversation about what's needed. The content team will respond to these issues with ideas for what we can add and ask for your opinions. When we create a draft, we'll ask you to review the PR.

## Comment on an issue

You can comment on any issue in the repository. You can also add your own comments to an issue you've created.

1. Find the issue you want to comment on. In your browser, navigate to the GitHub repository you want to look at issues for. Choose the **Issues** tab to see the open issues for that repo. If the repo has a lot of issues, use the **Filters** bar to filter by label, author, and more. Or use the **Search** bar to look for specific queries.

    If you're not sure which repo to look at, find one that interests you in our [list of Microsoft Learn repos](https://github.com/orgs/MicrosoftDocs/repositories).

1. Read the issue and any comments that have already been added by others. If you want to add a comment, scroll to the bottom of the issue and enter your comment in the **Leave a comment** box. When you're done, select **Comment**.

    :::image type="content" source="media/how-to-create-github-issues/comment-issue.png" alt-text="Screenshot of a GitHub issue with a comment box at the bottom.":::

## Open a pull request to address issues

As you browse issues, you may find one that you know how to fix. If so, you're welcome to open a PR to address the issue. For more information, see [Edit documentation in the browser](how-to-write-quick-edits.md).

Once you've opened a PR to address the issue, return to the issue and add a comment that links to your PR. This helps us track the issue and the PR together. Use the pound sign (#) followed by the PR number to link to the PR. For example, if your PR number is 4210, you'd enter `#4210` in your comment.

:::image type="content" source="media/how-to-create-github-issues/pr-open-issue.png" alt-text="Screenshot of the GitHub issue comment box with a link to a PR.":::
