---
title: external-bookmark-not-found
description: Explanation and resolution for Docs build issue external-bookmark-not-found
author: meganbradley
ms.author: mbradley # Microsoft employees only
ms.topic: error-reference
ms.date: 2/26/2019
ms.prod: non-product-specific
---
# external-bookmark-not-found

## Warning

`File '{file name}' doesn't contain a bookmark named '{bookmark text}'.`

You're trying to link to a heading in another file that doesn't exist.

## Resolution

[!INCLUDE [docs-authoring-pack](includes/docs-authoring-pack.md)]

Review the file you're linking to and update your bookmark link to point to a valid section in the file.

To link to a section heading in another article, use the file-relative or site-relative link plus a hash symbol, followed by the words of the heading. Remove punctuation from the heading and replace spaces with dashes. The following is an example:

```markdown
[Managed Disks](../../linux/overview.md#managed-disks)
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
