---
title: ms-author-invalid
description: Explanation and resolution for Docs build issue ms-author-invalid
author: meganbradley
ms.author: mbradley # Microsoft employees only
ms.topic: error-reference
ms.date: 9/27/2019
ms.prod: non-product-specific
---
# ms-author-invalid

## Warning

`Invalid value for ms.author: '{value}' is not a valid Microsoft alias, or is not an allowed distribution list.`

## Resolution

Verify that the `ms.author` value is the current author's valid Microsoft alias. We recommend that the designated author be a full-time employee or team distrubution list (DL), rather than a short-term vendor. If the alias is a DL, it must also be on the `ms.author` allow list.

Valid values for `ms.author` DLs can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
