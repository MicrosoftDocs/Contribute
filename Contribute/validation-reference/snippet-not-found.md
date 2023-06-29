---
title: snippet-not-found
description: Explanation and resolution for Docs build issue snippet-not-found
author: meganbradley
ms.author: mbradley # Microsoft employees only
ms.topic: error-reference
ms.date: 2/26/2019
ms.prod: non-product-specific
---
# snippet-not-found

## Warning

`Code snippet '{snippet path}' not found.`

The code snippet references doesn't exist at the specified path, or the path isn't available from the current file.

## Resolution

[!INCLUDE [docs-authoring-pack](includes/docs-authoring-pack.md)]

Ensure that your snippet path is correct. If the snippet is stored outside the current repo, make sure the repo is configured ase a dependent repo. For more information, see the Microsoft-internal [code snippet article](https://review.learn.microsoft.com/en-us/help/contribute/code-in-docs?branch=main).

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
