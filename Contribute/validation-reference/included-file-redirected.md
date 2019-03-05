---
title: included-file-redirected
description: Explanation and resolution for Docs build issue included-file-redirected
author: meganbradley
ms.author: mbradley # Microsoft employees only
ms.topic: error-reference
ms.date: 3/1/2019
ms.prod: non-product-specific
---
# included-file-redirected

## Warning

`Included file '{include path}' is redirected to '{target file path}'. Only include files that are not redirected and that are located in an includes folder.`

## Resolution

Restructure your content so you aren't including a redirected file. For example, create a new file to include or remove the included reference and link to content or write it inline.

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
