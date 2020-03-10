---
title: .NET docs pull request review process
description: The .NET docs do not have the PR merger webhooks enabled. This article describes the PR process for those repositories
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
ms.date: 01/04/2019
---
# Pull request review process for the .NET docs repositories

Many repositories don't have PR Merger webhooks enabled, which automatically merges minor PRs. This article describes
the PR review process for those repositories. The PR review process was designed
with these goals:

1. Publish high-quality content from our team, product team members, and community members.
1. Provide timely, actionable feedback to authors in a consistent manner.
1. Facilitate discussion between authors and reviewers.

The processes continue to evolve as teams innovate, and as the platform matures.

## Reviewers

One of the content team members reviews every PR. Content team members may request a review from the specific product team members to verify technical accuracy. The content team uses GitHub's Code Ownership feature to automatically request reviews from content team members. As part of this process, a reviewer may tag other team members to review internal PRs. Team members see requested reviews from team members and community members in the same queue.

Community members can review PRs and provide feedback as well. However, at least one member of the core content team must approve any PR before it is merged.

## Review process

Reviews follow one of the three paths based on the PR:

- **Small PRs** - Small PRs are single bug fix: typos, broken links, small code changes, or similar changes.
- **Major contributions** - Major contributions are significant edits to an existing article, new articles, or edits to a number of articles.
- **Work in progress** - Authors can request an in-progress review by opening a PR with the "[WIP]" tag in the title. The "WIP" tag stands for "Work in Progress." 

The processing used by the Contributor License Agreement (CLA) bot is a good guideline for the distinction between "small" and "large" contributions. PRs that do not require the CLA to be signed are likely "small." PRs that do require the CLA are likely "large."

### Small PRs

The changes in small PRs are reviewed for accuracy, and checked using the build on the review site. Because they are small, these PRs do not trigger a review of the entire article. 

Reviewers may notice other small changes that would improve an article. If those changes are also small, suggest them as review comments. If the suggested changes would trigger a larger review, open an issue and address those later. 

### Larger changes

Larger PRs undergo a more thorough review. The following are all checked:

- Sample code must be included in the PR, in source and as a downloadable zip file.
- Sample code compiles and runs correctly.
- The article clearly describes the goals for the reader, and those goals are met.
- The article meets [style and grammar guidelines](dotnet-style-guide.md) and follows our [voice and tone principles](dotnet-voice-tone.md).
- All links should resolve correctly.

Content team members will review the PR, and submit the review with comments. If only minor changes are requested, team members may "approve" the PR with the feedback. The author can then address the feedback and merge the PR. Most reviews will request changes and when those changes are made, the reviewer will review again.

If the edits require a technical review, the content team reviewer will request a review from the appropriate product team member.

### Review "WIP" pull requests

New authors may want feedback earlier in the process. They can open a PR adding the "[WIP]" label to the title. In a comment, they can request an early review.

These early reviews are not as thorough as a full PR review. The content team will comment, but will not "approve" or "request changes" using GitHub's review feature. These early reviews focus on the structure of the article: the outline, the overall content, and the samples. These reviews do not include a thorough check for grammar and correct links.

## Respond to reviews

The author updates the PR to respond to comments marking each addressed comment with the "+1" reaction to indicate it was addressed. If the author disagrees with the comment, or addresses the comment in a different, the author adds a comment explaining their change.

The author @-mentions the original reviewer in a comment to request a new review. 

## Response time expectations

Content team members will typically review new PRs in under two business days. If it takes longer to review, one of the team members will add a comment to acknowledge the PR and set expectations.

Once a review has been submitted, authors should try to respond to comments in a week or less. Volunteers may not be able to meet these expectations because of other commitments. In those cases, team members ask if the community author will update the PR. If not, the team member updates and merges the PR for them.
