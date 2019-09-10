---
title: multiple-h1
description: Explanation and resolution for Docs build issue multiple-h1.
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
---
# multiple-h1

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## Suggestion

`Multiple H1s are not allowed. You can only have one top-level heading.`

H1 refers to the first heading in a Markdown file. When published to docs.microsoft.com, the H1 shows at the top of the page in a large font. An H1 is created by beginning a line with a single hash (#) followed by a space, then the heading text. You can only have one H1 in each file.

## Resolution

To fix this issue, change the heading level of subsequent H1s to H2 (`##`), or otherwise reorganize your file. Note that skipping heading levels, such as following H1 with H3, is not allowed.

```markdown
---
author: meganbradley
ms.author: mbradley
---
# This is an H1

Some content...

## This is an H2
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]