---
title: h1-no-space
description: Explanation and resolution for Docs build issue no-space-in-h1.
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
---
# h1-no-space

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## Suggestion

`A space is required after the hash (#) in H1.`

H1 refers to the first heading in a Markdown file. When published to docs.microsoft.com, the H1 shows at the top of the page in a large font. An H1 is created by beginning a line with a single hash (#) followed by a space, then the heading text. Without the space after the hash, Docs will not recognize an H1.

## Resolution

To fix this error, add a space after the hash in your H1.

```markdown
---
author: meganbradley
ms.author: mbradley
---
# This is an H1
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]