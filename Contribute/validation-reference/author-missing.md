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

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## Suggestion

`Missing attribute: author. Add the current author's GitHub ID.`

The `author` attribute identifies the author of the article by GitHub ID. 

## Resolution

Add the current author's GitHub ID to the YML header:

```yml
---
author: meganbradley
ms.author: mbradley
---
```

Note that this should be the *current* owner of the article, not the original author if ownership has changed.

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
