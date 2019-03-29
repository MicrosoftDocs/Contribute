---
title: ms-prod-or-service-missing
description: Explanation and resolution for Docs build issue ms-prod-or-service-missing
author: meganbradley
ms.author: mbradley # Microsoft employees only
ms.topic: error-reference
ms.date: 12/20/2018
ms.prod: non-product-specific
---
# ms-prod-or-service-missing

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## Suggestion

`Missing attribute: either ms.prod or ms.service is required. Use ms.prod for on-premise products, or ms.service for cloud services.`

## Resolution

Either `ms.prod` or `ms.service` is required, and they can't both be present: `ms.prod` is used for on-premises products; `ms.service` is used for cloud services. Determine which is appropriate for your article, verify that the value is correct, and remove the other field.

Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]