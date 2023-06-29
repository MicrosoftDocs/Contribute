---
title: hard-coded-locale
description: Explanation and resolution for Docs build issue hard-coded-locale.
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 10/18/2019
ms.prod: non-product-specific
---
# hard-coded-locale

> [!IMPORTANT]
> This rule was initially enabled as a "Suggestion" to give content teams time to gauge impact and develop a plan to clean up their repos. **It will be elevated to a "Warning" on 12/20/2019**.

## Suggestion

`Link '{URL}' contains locale code '{code}'. For localizability, remove '{code}' from links to most Microsoft sites.`

Locale codes, such as `en-us`, should not be included in links to certain Microsoft sites. If you include a locale code in a link in English content, it will also be included in localized links, which leads to a bad localized experience. For example, if a link in German localized content includes `en-us`, German customers will find themselves linking to the English article, even if a German version is available.

The following sites are in scope for this validation:

- azure.microsoft.com
- learn.microsoft.com
- msdn.microsoft.com (excluding social.msdn.com, which needs locale to ensure the correct forum is linked to)
- technet.microsoft.com

## Resolution

Remove locale codes from links to Microsoft sites. The following is an example.

Before:

`https://learn.microsoft.com/en-us/vsts/load-test/app-service-web-app-performance-test`

After:

`https://learn.microsoft.com/vsts/load-test/app-service-web-app-performance-test`

> [!TIP]
> The Docs Markdown extension for VS Code includes a cleanup script for Microsoft links. The script checks all links to Microsoft sites in a repo to ensure that they begin with `https` instead of `http` and don't contain locale codes, such as `en-us`. To run the script:
>
> 1. Install the [Docs Markdown](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown) extension for VS Code.
> 1. Click alt + M to open the Markdown menu.
> 1. Select **Cleanup**, then **Microsoft links**.

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
