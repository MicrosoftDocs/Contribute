Comment automation enables read-level users (users who don't have write permissions in a repo) to perform a write-level action, by assigning the appropriate label to a pull request. If you are working in a repository where comment automation has been implemented, use the hashtag comments listed in the following table to assign labels, change labels, or close a pull request. Microsoft employees will also be notified via e-mail for review and sign-off of public repository PRs, whenever changes are proposed to articles for which you are the author.


| Hashtag comment | What it does | Repo availability |
| --- | --- | --- |
| #sign-off |When the author of an article types the **#sign-off** comment in the comment stream, the **ready-to-merge** label is assigned. This label lets the reviewers in the repo know when a pull request is ready for review/merge. |Public and private |
| #sign-off |If a contributor who is *not* the listed author tries to sign off on a public pull request by using the **#sign-off** comment, a message is written to the pull request indicating that only the author can assign the label. |Public |
| #hold-off |Authors can type **#hold-off** in a PR comment to remove the **ready-to-merge** label--in case they change their mind or make a mistake. In the private repo, this assigns the **do-not-merge** label. |Public and private |
| #please-close |Authors can type **#please-close** in the comment stream to close the pull request if they decide not to have the changes merged. |Public |
