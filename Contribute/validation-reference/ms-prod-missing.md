---
title: ms-prod-missing
description: Explanation and resolution for Docs build issue ms-prod-missing
author: meganbradley
ms.author: mbradley # Microsoft employees only
ms.topic: error-reference
ms.date: 2/2/2019
ms.prod: non-product-specific
---
# ms-prod-missing

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## Suggestion

`Missing attribute: ms.prod. If you specify ms.technology, you must also specify ms.prod.`

Use `ms.prod` to specify on-premises products. To specify more detailed information about `ms.prod`, you can optionally specify `ms.technology`, but if you specify `ms.technology`, you must also specify `ms.prod`. The values for `ms.prod` and `ms.technology` must be a valid pair.

## Resolution

Confirm that the `ms.technology` value you've specified is correct for your article. Then add the appropriate `ms.prod` value that is a valid parent for the `ms.technology`.

Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists). To request new values, follow [this process](https://review.docs.microsoft.com/help/contribute/metadata-changes?branch=master).

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
