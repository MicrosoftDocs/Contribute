---
title: ms-service-and-subservice-invalid
description: Explanation and resolution for Docs build issue ms-service-and-subservice-invalid
author: meganbradley
ms.author: mbradley # Microsoft employees only
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
---
# ms-service-and-subservice-invalid

## Warning

`Invalid value for ms.service: '{value}'.`

`Invalid value for ms.subservice: '{value}' is not valid with ms.service value '{value}'.`

Use `ms.service` to specify cloud services. To specify more detailed information about `ms.service`, you can optionally specify `ms.subservice`. The values for `ms.service` and `ms.subservice` must be a valid pair. Either your `ms.service` value is invalid, or your `ms.subservice` value is not a valid pair with your `ms.service`.

## Resolution

Confirm that your `ms.service` value is correct for your article. Then choose a valid `ms.subservice` value.

Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists). To request new values, follow [this process](https://review.learn.microsoft.com/help/contribute/metadata-changes?branch=main).

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
