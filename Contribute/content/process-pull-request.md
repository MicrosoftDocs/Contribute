---
title: Process a pull request
description: This article explains what happens after you open a pull request in GitHub for your contribution to Microsoft Learn.
author: carlyrevier
ms.author: cahublou
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
ms.date: 08/31/2023
---

# Process a pull request

A pull request (PR) is a request for a content owner to pull your changes into the official source. A PR enables GitHub's collaboration model by asking for the changes from your working branch to be pulled and merged into another branch. In most cases, that other branch is the default branch in the main repository.

## Validation

Before your PR can be merged into its destination branch, it might be required to pass through one or more PR validation processes. Validation processes can vary depending on the scope of proposed changes and the rules of the destination repository. After you submit your PR, you can expect one or more of the following to happen:

- **Mergeability**: A baseline GitHub mergeability test occurs first to verify whether the proposed changes in your branch conflict with the destination branch. If the PR indicates this test failed, you must reconcile the content that is causing the merge conflict before processing can continue.
- **Contribution License Agreement (CLA)**: As a non-Microsoft contributor, if you're contributing to a public repository, you might be asked to complete a short CLA the first time you submit a PR to that repository. After the CLA step is cleared, your PR is processed.
- **Labeling**: Labels are automatically applied to your PR to indicate the state of your PR as it passes through the validation workflow. For instance, new PRs might automatically receive the "do-not-merge" label, indicating that the PR hasn't yet completed the validation, review, and sign-off steps.
- **Validation and build**: Automated checks verify whether your changes pass validation tests. The validation tests might yield warnings or errors, requiring you to edit one or more files in your PR before it can be merged. The validation test results are added as a comment in your PR for your review, and they might be sent to you in e-mail.
- **Staging**: Upon successful validation and build, the articles you changed are automatically deployed to a staging environment for review. Preview URLs appear in a PR comment.
- **Auto-merge**: The PR might be automatically merged if it passes validation testing and certain criteria. In this case, you don't need to do anything else.

## Review and sign-off

After all PR processing is completed, you should review the results (for example, PR comments, preview URLs). Determine if you need to make more changes before you sign off for merging. If a PR reviewer has reviewed your PR, they can also provide feedback via comments if there are outstanding issues or questions to be resolved before merge.

Comment automation enables read-level users (users who don't have write permissions in a repo) to complete a write-level action by assigning the appropriate label to a PR. If you're working in a repo where comment automation has been implemented, use the **hashtag comments** listed in the following table to assign labels, change labels, or close a PR. Microsoft employees will also be notified via e-mail for review and sign-off whenever changes are proposed to articles for which you are the author.

| Hashtag comment | What it does |
| --- | --- | --- |
| `#sign-off` | Automatically assigns the **ready-to-merge** label to let the reviewers in the repo know the PR is ready for review/merge. <br/><br/> If you're <em>not</em> the listed author and try to sign off on a public-repo PR using the <code>#sign-off</code> comment, the PR is updated to indicate that only the author can assign the label. |
| `#hold-off` | Removes the **ready-to-merge** label in case you change your mind or make a mistake. In the private repo, this assigns the **do-not-merge** label. |
| `#please-close` | Closes the PR if you decide not to have the changes merged. |
| `#please-open` | Reopens a closed PR or issue. |
| `#label:"custom label text"` | Adds a custom label up to 200 characters (shorter recommended). |
| `#assign:<GitHub account>` | Adds a GitHub account to **Assignees** in the PR or issue. The account must be a valid contributor in the repo. |
| `#reassign:<Github account>` | Removes all current assignees and adds a GitHub account to **Assignees** in the PR or issue. The account must be a valid contributor in the repo. |
| `#assign-reviewer:<GitHub account>` | Adds a GitHub account to **Reviewers** in the PR. The account must be a valid contributor in the repo. |
| `#unassign-reviewer:<GitHub account>` | Removes a GitHub account from **Reviewers** in the PR. |

When the PR is issue-free and signed off, your changes are merged back into the parent branch and the PR is closed.

## Publishing

Remember, your PR has to be merged by a PR reviewer before the changes can be included in the next scheduled publishing run. Normally, PRs are reviewed and merged in the order of submission. If your PR requires merging for a specific publishing run, you'll need to work with your PR reviewer ahead of time to ensure that merging happens before publishing.

After your contributions are approved and merged, the publishing process picks them up. Publishing times vary depending on the team that manages the repository you're contributing to. Articles published under the following locations are normally deployed at approximately 10:30 AM and 3:30 PM Pacific Time, Monday through Friday:

- [Azure documentation](/azure/)
- [ASP.NET documentation](/aspnet/)
- [.NET documentation](/dotnet/)
- [Enterprise Mobility + Security documentation](/enterprise-mobility-security)

It can take up to 45 minutes for articles to appear online after publishing. After your article is published, you can verify your changes at the appropriate URL: `https://learn.microsoft.com/<path-to-your-article-without-the-md-extension>`.

## Next steps

That's it! You've made a contribution to Microsoft Learn content!
