---
title: ms-prod-and-technology-invalid
description: Explanation and resolution for Docs build issue ms-prod-and-technology-invalid
author: meganbradley
ms.author: mbradley # Microsoft employees only
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
---
# ms-prod-and-technology-invalid

**Coming soon!**

## Warning

`Invalid value for ms.prod: '{value}'.`

`Invalid value for ms.technology: '{value}' is not valid with ms.prod value '{value}'.`

Use `ms.prod` to specify on-premises products. To specify more detailed information about `ms.prod`, you can optionally specify `ms.technology`. The values for `ms.prod` and `ms.technology` must be a valid pair. Either your `ms.prod` value is invalid, or your `ms.technology` value is not a valid pair with your `ms.prod`.

## Resolution

Confirm that your `ms.prod` value is correct for your article. Then choose a valid `ms.technology` value.

Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/whitelists).

<!-- Can we link to whitelist externally? -->

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
