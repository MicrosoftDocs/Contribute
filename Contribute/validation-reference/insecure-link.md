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

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## Suggestion

`Link '{URL}' is insecure. Links to Microsoft sites must use 'https' instead of 'http'.`

## Resolution

Change all URLs to Microsoft sites to use `https` instead of `http`.

> [!TIP]
> The Docs Markdown extension for VS Code includes a cleanup script for Microsoft links. The script checks all links to Microsoft sites in a repo to ensure that they begin with `https` instead of `http` and don't contain locale codes, such as `en-us`. To run the script:
>
> 1. Install the [Docs Markdown](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown) extension for VS Code.
> 1. Click alt + M to open the Markdown menu.
> 1. Select **Cleanup**, then **Microsoft links**.

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
