---
title: author-missing
description: Explanation and resolution for Docs build issue author-missing.
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
---
# author-missing

## Warning

`Author metadata is required.`

The `author` attribute identifies the author of the article by GitHub ID.

## Resolution

Add the author's GitHub ID to the YML header:

```markdown
---
author: meganbradley
ms.author: mbradley
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](../includes/validation-reference-help.md)]