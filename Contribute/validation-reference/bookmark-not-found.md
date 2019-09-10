---
title: internal-bookmark-not-found
description: Explanation and resolution for Docs build issue internal-bookmark-not-found
author: meganbradley
ms.author: mbradley # Microsoft employees only
ms.topic: error-reference
ms.date: 9/10/2019
ms.prod: non-product-specific
---
# bookmark-not-found

## Warning

`Cannot find bookmark '{bookmark-id}' in '{parent-file}'.`

You're trying to link to a heading in the current file or another file that doesn't exist.

## Resolution

[!INCLUDE [docs-authoring-pack](includes/docs-authoring-pack.md)]

Verify the heading you want to link to and update the link.

To link to a section in the current article, use a hash symbol, followed by the words of the heading. Remove punctuation from the heading and replace spaces with dashes. The following is an example:

```markdown
[Managed Disks](#managed-disks)
```

To link to a heading in another file, use a relative link to that file, followed by a hash symbol and the words of the heading. Remove punctuation from the heading and replace spaces with dashes. The following is an example:

```markdown
See [the Resolution section in h1-empty](h1-empty.md#resolution).
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
