---
title: h1-empty
description: Explanation and resolution for Docs build issue h1-empty.
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 11/25/2019
ms.prod: non-product-specific
---
# h1-empty

## Warning

`H1 is required. Add content to your top-level heading.`

H1 refers to the first heading in a Markdown file. When published to docs.microsoft.com, the H1 shows at the top of the page in a large font. An H1 is created by beginning a line with a single hash (#) followed by a space, then the heading text.

## Resolution

To fix this issue, make sure your H1 includes content, not just a hash.

Bad:

```markdown
---
author: meganbradley
ms.author: mbradley
---
#
This is not an H1
```

Good:

```markdown
---
author: meganbradley
ms.author: mbradley
---
# This is an H1
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
