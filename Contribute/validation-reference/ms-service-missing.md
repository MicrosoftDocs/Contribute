---
title: ms-service-missing
description: Explanation and resolution for Docs build issue ms-service-missing
author: meganbradley
ms.author: mbradley # Microsoft employees only
ms.topic: error-reference
ms.date: 2/2/2019
ms.prod: non-product-specific
---
# ms-service-missing

## Warning

`Missing attribute: ms.service. If you specify ms.subservice, you must also specify ms.service.`

Use `ms.service` to specify cloud services. To specify more detailed information about `ms.service`, you can optionally specify `ms.subservice`, but if you specify `ms.subservice`, you must also specify `ms.service`. The values for `ms.service` and `ms.subservice` must be a valid pair.

## Resolution

Confirm that the `ms.subservice` value you've specified is correct for your article. Then add the appropriate `ms.service` value that is a valid parent for the `ms.subservice`.

Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists). To request new values, follow [this process](https://review.learn.microsoft.com/help/contribute/metadata-changes?branch=main).

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
