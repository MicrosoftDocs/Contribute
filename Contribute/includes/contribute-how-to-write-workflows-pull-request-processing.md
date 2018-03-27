## Pull request processing

The previous section walked you through the process of submitting proposed changes, by bundling them in a new pull request (PR) that is added to the destination repository's PR queue. A pull request enables GitHub's collaboration model, by asking for the changes from your working branch to be pulled and merged into another branch. In most cases, that other branch is the default/master branch in the main repository.

### Validation

Before your pull request can be merged into its destination branch, it might be required to pass through one or more PR validation processes. Validation processes can vary depending on the scope of proposed changes and the rules of the destination repository. After your pull request is submitted, you can expect one or more of the following to happen:

- **Mergeability**: A baseline GitHub mergeability test occurs first, to verify whether the proposed changes in your branch are in conflict with the destination branch. If the pull request indicates that this test failed, you must reconcile the content that is causing the merge conflict before processing can continue.
- **CLA**: If you are contributing to a public repository and are not a Microsoft employee, depending on the magnitude of the proposed changes, you might be asked to complete a short Contribution License Agreement (CLA) the first time you submit a pull request to that repository. After the CLA step is cleared, your pull request is processed.
- **Labeling**: Labels are automatically applied to your pull request, to indicate the state of your pull request as it passes through the validation workflow. For instance, new pull requests might automatically receive the "do-not-merge" label, indicating that the pull request has not yet completed the validation, review, and sign-off steps.
- **Validation and build**: Automated checks verify whether your changes pass validation tests. The validation tests might yield warnings or errors, requiring you to make changes to one or more files in your pull request before it can be merged. The validation test results are added as a comment in your pull request for your review, and they might be sent to you in e-mail.
- **Staging**: The article pages affected by your changes are automatically deployed to a staging environment for review upon successful validation and build. Preview URLs appear in a PR comment.
- **Auto-merge**: The pull request might be automatically merged, if it passes validation testing and certain criteria. In this case, you don't need to take any further action.

### Review and sign-off

After all PR processing is completed, you should review the results (PR comments, preview URLs, etc.) to determine if additional changes to its files are required before you sign off for merging. If a PR reviewer has reviewed your pull request, they can also provide feedback via comments if there are outstanding issues/questions to be resolved prior to merge.

[!INCLUDE[contribute-how-to-pull-requests-apex-automation.md](contribute-how-to-pull-requests-apex-automation.md)]

When the pull request is issue-free and signed off, your changes are merged back into the parent branch and the pull request is closed.

### Publishing

Remember, your pull request has to be merged by a PR reviewer before the changes can be included in the next scheduled publishing run. Pull requests are normally reviewed/merged in the order of submission. If your pull request requires merging for a specific publishing run, you will need to work with your PR reviewer ahead of time to ensure that merging happens prior to publishing.

After your contributions are approved and merged, the docs.microsoft.com publishing process picks them up. Depending on the team that manages the repository you are contributing to, publishing times can vary. Articles published under the following paths are normally deployed at approximately 10:30 AM and 3:30 PM Pacific Time, Monday-Friday:

- https://docs.microsoft.com/azure/
- https://docs.microsoft.com/aspnet/
- https://docs.microsoft.com/dotnet/
- https://docs.microsoft.com/enterprise-mobility-security

It can take up to 45 minutes for articles to appear online after publishing. After your article is published, you can verify your changes at the appropriate URL: `https://docs.microsoft.com/<path-to-your-article-without-the-md-extension>`.
