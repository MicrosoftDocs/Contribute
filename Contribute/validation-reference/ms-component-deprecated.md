---
title: ms-component-deprecated
description: Explanation and resolution for Docs build issue ms-component-deprecated
author: meganbradley
ms.author: mbradley # Microsoft employees only
ms.topic: error-reference
ms.date: 2/1/2019
ms.prod: non-product-specific
---
# ms-component-deprecated

[!INCLUDE [suggestion-note](../../../../Contribute/Contribute/validation-reference/includes/suggestion-note.md)]

## Suggestion

`Deprecated attribute: ms.component. Use ms.subservice instead.`

Use `ms.service` to specify cloud services. To specify more detailed information about `ms.service`, you can optionally specify `ms.subservice`. Don't use `ms.component`; it's deprecated for this content.

## Resolution

Confirm that your `ms.service` value is correct for your article. Then choose a valid `ms.subservice` value.

Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/whitelists).

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
