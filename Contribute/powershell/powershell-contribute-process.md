---
title: Contribution process for PowerShell docs repositories
description: This article provides a brief introduction to contributing to the PowerShell docs repositories. You'll learn the repositories used, the process for organizing content, and the policies for managing code samples and other assets.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
author: sdwheeler
ms.author: sewhee
ms.date: 10/07/2019
---
# Process for contributing to PowerShell docs

We appreciate community contributions to docs. The following list shows some guiding rules that you
should keep in mind when you're contributing to the PowerShell documentation:

- **DON'T** surprise us with large pull requests. Instead, file an issue and start a discussion so
  we can agree on a direction before you invest a large amount of time.
- **DO** follow these instructions and the [code](powershell-style-code.md) and
  [reference](powershell-style-reference.md) style guides..
- **DO** use the [template](powershell-style-basic-markdown.md) file as the starting point of your
  work.
- **DO** create a separate branch on your fork before working on the articles.
- **DO** follow the [GitHub Flow workflow](../how-to-write-workflows-major.md).
- **DO** blog and tweet (or whatever) about your contributions, frequently!

Following these guidelines ensures a better experience for you and for us.

## Make a contribution to PowerShell docs

You can choose from existing [issues](https://github.com/MicrosoftDocs/PowerShell-Docs/issues/new/choose).
Depending on your interests and level of commitment, the efforts fall into the following categories:

- **Small changes**. For small changes, see the instructions on editing in GitHub on the
  [home page](../index.md#quick-edits-to-existing-documents) of the contributor guide. Small changes
  include:

  - Fixing typos and spelling errors
  - Improving grammar or formatting
  - Minor technical or factual edits

- **Maintenance**. This category includes fairly simple contributions, such as fixing broken or
  incorrect links, adding missing code examples, or addressing limited content issues. In some
  cases, these issues may concern large numbers of files. In that case, you should let us know what
  you'd like to work on before you begin. Add a comment on the issue to tell us that you are working
  on it.

- **Content updates**. Given the enormity of the doc set, content easily becomes outdated and
  requires revision. In addition, for a variety of reason, some content has been duplicated or even
  triplicated. Updating content involves making sure that individual topics are current or revising
  content in a feature area to eliminate duplication and ensure that all unique content is preserved
  in the smaller documentation set.

- **New content authoring**. If you're interested in authoring your own topic, these issues list
  topics that we know we'd like to add to our doc set. Let us know before you begin working on a
  topic, though. If you're interested in writing a topic that isn't listed here, open an issue.

Once you've picked a task to work on, follow the [get started](../get-started-setup-github.md) guide
to create a GitHub account and setup your environment.

### Making large changes

**Step 1:** If you're interested in writing new content or in thoroughly revising existing content,
open an issue describing what you want to do.

**Step 2:** Fork the `MicrosoftDocs/PowerShell-Docs` repository and create a working branch for your
changes.

**Step 3:** Make the changes in this new branch.

If it's a new topic, use the template in the [style guide](powershell-style-basic-markdown.md) as
your starting point. The style guide contains the writing guidelines and explains the metadata
required for each article.

Navigate to the folder that corresponds to the TOC location determined for your article in step 1.
That folder contains the Markdown files for all articles in that section. If necessary, create a new
folder to place the files for your content. The main article for that section is called *index.md*.
For images and other static resources, create a subfolder called **media** inside the folder that
contains your article, if it doesn't already exist. Inside the **media** folder, create a subfolder
with the article name (except for the index file).

Be sure to follow the proper Markdown syntax. Please read the
[style guide](powershell-style-basic-markdown.md) for detailed instructions and examples.

**Example structure**

```
reference
  /docs-conceptual
    /learn
      /remoting
        managing-remote-sessions.md
        /images
          /managing-remote-sessions
            sesssion-list.png
```

**Step 4:** Submit a Pull Request (PR) from your working branch to the *staging* branch.

Normally, a PR should address one issue at a time. The PR can modify one or multiple files. If
you're addressing multiple fixes on different files, separate PRs are preferred.

If your PR fixes an existing issue, add the `Fixes #Issue_Number` keyword to the commit message or
PR description. That way, the issue is automatically closed when the PR is merged. For more
information, see
[Closing issues via commit messages](https://help.github.com/articles/closing-issues-via-commit-messages/).

The PowerShell team reviews your PR and lets you know if there are any other changes necessary in
order to approve it.

**Step 5:** Make any necessary updates to your branch as discussed with the team.

Once the PR is approved, the maintainers merge your PR into the *staging* branch. We periodically
push all commits from *staging* branch into the *live* branch. Once your contribution is live, you
can see it in the [PowerShell docs site](https://learn.microsoft.com/PowerShell/). Typically, we
publish a two to three times during the work week.

## Contributor license agreement

You must sign the [Contribution License Agreement (CLA)](https://cla.opensource.microsoft.com/MicrosoftDocs/PowerShell-Docs)
before your PR is merged. This is a one-time requirement when contributing to our documentation.

You don't have to sign the agreement up-front. You can clone, fork, and submit your PR as usual.
When your PR is created, it is classified by a CLA bot. If the change is small (for example, you
fixed a typo), then the PR is labeled with `cla-not-required`. Otherwise, it's classified as
`cla-required`. Once you signed the CLA, the current and all future pull requests are labeled as
`cla-signed`.
