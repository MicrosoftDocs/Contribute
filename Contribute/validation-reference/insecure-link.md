---
title: insecure-link
description: Explanation and resolution for Docs build issue insecure-link
author: meganbradley
ms.author: mbradley # Microsoft employees only
ms.topic: error-reference
ms.date: 10/1/2019
ms.prod: non-product-specific
---
# insecure-link

> [!IMPORTANT]
> This rule was initially enabled as a "Suggestion" to give content teams time to gauge impact and develop a plan to clean up their repos. **It will be elevated to a "Warning" on 12/20/2019**.

## Suggestion

`Link '{URL}' is insecure. Links to Microsoft sites must use 'https' instead of 'http'.`

This message means that you either used an explicit Markdown link with `http` or you used a raw URL, such as `www.microsoft.com`. Raw URLs are converted to insecure links when published to Docs, and should not be used.

## Resolution

Change all URLs to Microsoft sites to use `https` instead of `http`.

If your link is a raw URL, change it to an explicit Markdown link beginning with `https`.

> [!TIP]
> The Docs Markdown extension for VS Code includes a cleanup script for Microsoft links. The script checks all links to Microsoft sites in a repo to ensure that they begin with `https` instead of `http` and don't contain locale codes, such as `en-us`. To run the script:
>
> 1. Install the [Docs Markdown](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown) extension for VS Code.
> 1. Click alt + M to open the Markdown menu.
> 1. Select **Cleanup**, then **Microsoft links**.

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
