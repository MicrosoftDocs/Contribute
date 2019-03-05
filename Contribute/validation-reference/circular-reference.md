---
title: circular-reference
description: Explanation and resolution for Docs build issue circular-reference
author: meganbradley
ms.author: mbradley # Microsoft employees only
ms.topic: error-reference
ms.date: 2/26/2019
ms.prod: non-product-specific
---
# circular-reference

## Error

`Files '{file name 1}' and '{file name 2}' reference each other.`

For example, this might be an included file that links to the current file, or a link to a file that's been redirected to the current file.

## Resolution

Review the links in the files and make necessary edits so no file links to or includes itself.

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
