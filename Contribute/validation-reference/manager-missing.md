---
title: manager-missing
description: Explanation and resolution for Docs build issue manager-missing
author: meganbradley
ms.author: mbradley # Microsoft employees only
ms.topic: error-reference
ms.date: 3/1/2019
ms.prod: non-product-specific
---
# manager-missing

**Coming soon!**

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## Suggestion

`Missing attribute: manager. Add a valid Microsoft alias for the author's manager.`

Some content groups require the `manager` attribute to identify the author's manager.

## Resolution

Add a valid Microsoft alias for `manager`:

```yml
---
ms.author: mbradley
manager: jemash
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
