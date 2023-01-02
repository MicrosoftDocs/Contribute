Comment automation enables read-level users (users who don't have write permissions in a repo) to perform a write-level action, by assigning the appropriate label to a pull request. If you are working in a repository where comment automation has been implemented, use the hashtag comments listed in the following table to assign labels, change labels, or close a pull request. Microsoft employees will also be notified via e-mail for review and sign-off of public repository PRs, whenever changes are proposed to articles for which you are the author.

| Hashtag comment | What it does | Repo availability |
| --- | --- | --- |
| `#sign-off` (private repo)| Adds the **ready-to-merge** label to the PR. This label lets the reviewers in the repo know when a PR is ready for review/merge. In private repos, any contributor to the repo can sign off, but it's generally the author of the PR or the owner of the article.| Private |
| `#sign-off` (public repo) | Adds the **ready-to-merge** label to the PR. In public repos, only the listed authors of files in the PR can sign off. If a contributor who *isn't* a listed author tries to sign off, comment automation writes a message to the PR indicating that only the authors can sign off. | Public |
| `#hold-off` | Removes the **ready-to-merge** label. In a private repo, **#hold-off** assigns the **do-not-merge** label. | Public and private |
| `#please-close` | Closes the PR or issue.| Public and private|
| `#please-open` | Reopens a closed PR or issue.|Public and private|
| `#label:"custom label text"` | Adds a custom label up to 200 characters (shorter recommended).| Public and private |
| `#assign:<GitHub account`> | Adds a GitHub account to **Assignees** in the PR or issue. The account must be a valid contributor in the repo.| Public and private |
| `#reassign:<Github account>` |Removes all current assignees and adds a GitHub account to **Assignees** in the PR or issue. The account must be a valid contributor in the repo. | Public and private |
| `#assign-reviewer:<GitHub account>` | Adds a GitHub account to **Reviewers** in the PR. The account must be a valid contributor in the repo.|Public and private|
| `#unassign-reviewer:GitHub account>` |Removes a GitHub account from **Reviewers** in the PR.|Public and private|