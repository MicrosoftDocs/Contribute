---
title: ms-prod-service-mismatch
description: Explanation and resolution for Docs build issue ms-prod-service-mismatch
author: meganbradley
ms.author: mbradley # Microsoft employees only
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
---
# ms-prod-service-mismatch

**Coming soon!**

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## Suggestion

`Invalid attribute pair: ms.prod and ms.subservice. You can only pair ms.prod with ms.technology.`

`Invalid attribute pair: ms.service and ms.technology. You can only pair ms.service with ms.subservice.`

Use `ms.prod` to specify on-premises products; `ms.service` for cloud services. To specify more detailed information about `ms.prod`, you can optionally specify `ms.technology`. To specify more detailed information about `ms.service`, you can specify `ms.subservice`. You can't use `ms.prod` with `ms.subservice` or `ms.service` with `ms.technology`.

## Resolution

First, verify that you have selected the correct parent attribute (`ms.prod` or `ms.service`) for your article. Then, add the appropriate child field with a valid paired value. Remove any extra fields.

Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
