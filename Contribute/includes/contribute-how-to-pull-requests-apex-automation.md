Comment automation enables read-level users (users who don't have write permissions in a repo) to perform a write-level action, by assigning the appropriate label to a pull request (PR). If you are working in a repository where comment automation has been implemented, use the **hashtag comments** listed in the following table to assign labels, change labels, or close a PR. Microsoft employees will also be notified via e-mail for review and sign-off of public repository PRs, whenever changes are proposed to articles for which you are the author.

| Hashtag comment | What it does | Repo availability |
| --- | --- | --- |
| `#sign-off` | Automatically assigns the **ready-to-merge** label to let the reviewers in the repo know the PR is ready for review/merge. <br/><br/> If you are <em>not</em> the listed author and try to sign off on a public repo PR using the <code>#sign-off</code> comment, the PR is updated to indicate that only the author can assign the label. | Public and private |
| `#hold-off` | Removes the **ready-to-merge** label in case you change your mind or make a mistake. In the private repo, this assigns the **do-not-merge** label. | Public and private |
| `#please-close` | Closes the PR if you decide not to have the changes merged. | Public and private |
| `#please-open` | Reopens a closed PR or issue. | Public and private |
| `#label:"custom label text"` | Adds a custom label up to 200 characters (shorter recommended). | Public and private |
| `#assign:<GitHub account>` | Adds a GitHub account to **Assignees** in the PR or issue. The account must be a valid contributor in the repo. | Public and private |
| `#reassign:<Github account>` | Removes all current assignees and adds a GitHub account to **Assignees** in the PR or issue. The account must be a valid contributor in the repo. | Public and private |
| `#assign-reviewer:<GitHub account>` | Adds a GitHub account to **Reviewers** in the PR. The account must be a valid contributor in the repo. | Public and private |
| `#unassign-reviewer:<GitHub account>` | Removes a GitHub account from **Reviewers** in the PR. | Public and private |
