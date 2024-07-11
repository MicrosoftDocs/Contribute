---
title: Process a pull request
description: This article explains what happens after you open a pull request in GitHub for your contribution to Microsoft Learn.
author: carlyrevier
ms.author: cahublou
ms.topic: contributor-guide
ms.service: learn
ms.custom: external-contributor-guide
ms.date: 01/25/2024
---

# Process a pull request

After you've opened a pull request (PR), the PR undergoes a set of checks and reviews to ensure your proposed changes can be merged. For more background on PRs, see [Git and GitHub fundamentals](git-github-fundamentals.md#pull-requests).

## Validation

Before your PR can be merged into its destination branch, it might be required to pass through one or more PR-validation processes. After you select **Create pull request**, GitHub runs the validations configured for your repository. When the validation process finishes, the results appear in the PR.

Validation processes vary depending on the scope of proposed changes and the rules of the destination repository. After you submit your PR, you can expect one or more of the following to happen:

- **Mergeability**: A baseline GitHub mergeability test occurs first to verify whether the proposed changes in your branch conflict with the destination branch. If the PR indicates this test failed, you must reconcile the content that is causing the merge conflict before processing can continue.
- **Contribution License Agreement (CLA)**: As a non-Microsoft contributor, if you're contributing to a public repository, you might be asked to complete a short CLA the first time you submit a PR to that repository. After the CLA step is cleared, your PR is processed.
- **Labeling**: Labels are automatically applied to your PR to indicate the state of your PR as it passes through the validation workflow. For instance, new PRs might automatically receive the "do-not-merge" label, indicating that the PR hasn't yet completed the validation, review, and sign-off steps.
- **Validation and build**: Automated checks verify whether your changes pass validation tests. The validation tests might yield warnings or errors, requiring you to edit one or more files in your PR before it can be merged. The validation test results are added as a comment in your PR for your review, and they might be sent to you in e-mail.
- **Staging**: Upon successful validation and build, the articles you changed are automatically deployed to a staging environment for review. Preview URLs appear in a PR comment.
- **Auto-merge**: The PR might be automatically merged if it passes validation testing and certain criteria. In this case, you don't need to do anything else.

## Review and address feedback

After all PR processing is complete, you should review the results (for example, PR comments, build results). Determine if you need to make more changes before you sign off for merging. You may need to change your content for any of the following reasons:

- PR comments from reviewers. If a PR reviewer has reviewed your PR, they can provide feedback via comments if there are outstanding issues or questions to be resolved before merge.
- Feedback from peer reviewers.
- Formatting fixes due to rendering issues.
- Validation errors or warnings.
- Merge conflicts.

If you need to make changes, you can edit your content directly in the PR, or you can return to VS Code to make your changes. When you're finished, commit your changes to your working branch. The PR is automatically updated with your changes.

Each time you add a commit to the same working branch, the commit is added automatically to the PR. With each commit, the publishing system reruns the validation and review processes automatically.

## Sign-off and comment automation

When you've addressed all feedback and validation errors, and you're ready for your changes to be merged, it's time to sign off on your PR by creating a new comment that reads `#sign-off`. You must enter the `#sign-off` comment to merge your changes. Even if all reviews and validation checks pass, you're responsible for using this comment to tell the PR reviewers and repo admins that your changes are ready for merging. 

When the reviewers determine that your PR is issue-free and signed off, your changes are merged into the default branch and the PR is closed.

Comment automation enables users who don't have write permissions in a repo to complete a write-level action by assigning the appropriate label to a PR. If you're working in a repo where comment automation has been implemented, use the **hashtag comments** listed in the following table to assign labels, change labels, or close a PR. Microsoft authors will also be notified via e-mail for review and sign-off whenever changes are proposed to their articles.

| Hashtag comment | What it does |
| --- | --- | --- |
| `#sign-off` | Automatically assigns the **ready-to-merge** label to let the reviewers in the repo know the PR is ready for review/merge. <br/><br/> If you're <em>not</em> the listed author and try to sign off on a public-repo PR using the <code>#sign-off</code> comment, the PR is updated to indicate that only the author can assign the label. |
| `#hold-off` | Removes the **ready-to-merge** label in case you change your mind or make a mistake. In the private repo, this assigns the **do-not-merge** label. |
| `#please-close` | Closes the PR if you decide not to have the changes merged. |
| `#please-open` | Reopens a closed PR or issue. |

## Publishing

Your PR has to be merged by a PR reviewer before the changes can be included in the next scheduled publishing run. Normally, PRs are reviewed and merged in the order of submission.

After your contributions are approved and merged, the publishing process picks them up. Depending on the team that manages the repository you’re contributing to, publishing times can vary, but they typically occur at least once every weekday. It can take up to 45 minutes for articles to appear online after publishing.

Once your changes are published, they go live on Microsoft Learn for others to start learning from!

## Next steps

That's it! You've made a contribution to Microsoft Learn content!
