---
title: ms-prod-and-service
description: Explanation and resolution for Docs build issue ms-prod-and-service
author: meganbradley
ms.author: mbradley # Microsoft employees only
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
---
# ms-prod-and-service

## Warning

<https://review.learn.microsoft.com/en-us/help/contribute/metadata-changes?branch=main>
`Both ms.prod and ms.service can't be specified. Use ms.prod for on-premise products, or ms.service for cloud services.`

## Resolution

Either `ms.prod` or `ms.service` is required, and they can't both be present: `ms.prod` is used for on-premises products; `ms.service` is used for cloud services. Determine which is appropriate for your article, verify that the value is correct, and remove the other field.

Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists). To request new values, follow [this process](https://review.learn.microsoft.com/en-us/help/contribute/metadata-changes?branch=main).

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
