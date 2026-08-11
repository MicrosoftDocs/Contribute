---
title: Contributor License Agreement
description: Learn when external contributors are asked to complete the Microsoft Contributor License Agreement for Microsoft Learn documentation pull requests.
author: cahublou
ms.author: cahublou
ms.date: 08/11/2026
ms.topic: contributor-guide
ms.service: learn
ms.custom: external-contributor-guide
---

# Contributor License Agreement

Microsoft welcomes contributions from the community to Microsoft Learn
documentation repositories on GitHub. If you open a pull request (PR) to a
public Microsoft Learn repository and you aren't a Microsoft employee, you
might be asked to complete the Microsoft Contributor License Agreement (CLA).

The CLA is a short, one-time step that helps Microsoft process community
contributions. It's part of the PR validation workflow for public repositories.
After the CLA step is cleared, your PR continues through the rest of the
validation and review process.

## When you're asked to complete the CLA

You might be asked to complete the CLA the first time you submit a substantial
PR to a public Microsoft Learn repository. Whether the CLA check appears can
depend on the amount of change in the PR.

Microsoft employees don't need to complete this step for Microsoft Learn
documentation contributions.

If your PR requires a CLA, GitHub shows a License/CLA check on the PR. When the
check is queued or waiting, the PR can't finish processing until the CLA step is
complete.

## How the CLA flow works

The CLA flow happens in the GitHub PR conversation. You don't need to leave the
PR or start over.

1. Open your PR in GitHub.
1. Review the checks and comments on the PR.
1. If the License/CLA check is queued, follow the CLA-bot instructions in the
   PR conversation.
1. Comment on the PR with the appropriate CLA-bot command.
1. Wait for the License/CLA check to update.

After the check clears, the PR continues through the normal Microsoft Learn PR
workflow, such as labeling, validation, build, staging, review, and possible
merge.

## Sign as an individual or a company

The CLA can be completed for an individual or for a company. Choose the option
that matches how you're contributing.

To agree on behalf of yourself as an individual, comment on the PR with:

```markdown
@microsoft-github-policy-service agree
```

To agree on behalf of a company, comment on the PR with:

```markdown
@microsoft-github-policy-service agree company="your company"
```

After the CLA is completed for the same individual or company, it shouldn't need
to be completed again for future Microsoft Learn documentation PRs from that
same legal entity.

## If your contribution status changes

If you need to revoke a previous CLA agreement because your company or
contribution status changed, comment on the PR with:

```markdown
@microsoft-github-policy-service terminate
```

If the CLA check doesn't update after you follow the PR instructions, wait a
short time and refresh the PR. The rest of the PR checks can continue only after
the CLA step clears.
