---
title: ms-author-missing
description: Explanation and resolution for Docs build issue ms-author-missing
author: meganbradley
ms.author: mbradley # Microsoft employees only
ms.topic: error-reference
ms.date: 12/20/2018
ms.prod: non-product-specific
---
# ms-author-missing

## Warning

`Missing attribute: ms.author. Add the current author's Microsoft alias.`

## Resolution

Add the current author's Microsoft alias for `ms.author`. Note that this should be the *current* owner of the article, not the original author if ownership has changed. We recommend that the designated author be a full-time employee or team distribution list (DL), rather than a short-term vendor. 

If the alias is a DL, it must also be on the `ms.author` allow list.

Valid values for `ms.author` DLs can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
