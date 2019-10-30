---
title: validation-timeout
description: Explanation and resolution for Docs build issue validation-timeout
author: meganbradley
ms.author: mbradley # Microsoft employees only
ms.topic: error-reference
ms.date: 6/5/2019
ms.prod: non-product-specific
---
# validation-timeout

## Warning

`The call to the validation service timed out and validation was not completed. This happens when there's an issue with the service and continuing to retry the call could cause build delays. You might have content issues that were not reported. To retry validation, close and re-open your PR, or rebuild your branch via Docs Portal (requires admin permissions). If you need admin help or if you continue to see this message, file an issue via https://SiteHelp.`

Sometimes transient issues in the validation service, such as a server in a bad state, prevent Docs Build from successfully calling the service. After several tries, the call times out and validation is canceled to avoid build delays and clogging the build pipeline.

## Resolution

Try closing and re-opening your PR, or forcing a full build via [Docs Portal](https://ops.microsoft.com/#/). Often service issues clear themselves up after the initial retry. 

Note that you must be a repo admin to access the repo via Docs Portal. If you don't know who your repo admin is, or if you continue to get this message after a forced build, file an issue via [https://SiteHelp](https://SiteHelp) if you're a Microsoft employee, or @ mention the author of an article in your PR for assistance if you're an external contributor.

If you're a repo admin, you can force a full build as follows:

1. Go to [Docs Portal](https://ops.microsoft.com/#/) and sign in.
1. Find your repo by searching in the upper left corner, and select it.
1. On the **Build History** tab, click **+ Manual Publish***.
1. Select the branch that's getting the Warning, such as Master.
1. For target, keep the default, **Docs site**.
1. Check the **Force Publish** checkbox.
1. Click **Publish**.

This will force a full build on the branch.

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
