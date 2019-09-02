---
title: ms-date-invalid
description: Explanation and resolution for Docs build issue ms-date-invalid
author: meganbradley
ms.author: mbradley # Microsoft employees only
ms.topic: error-reference
ms.date: 01/15/2019
ms.prod: non-product-specific
---
# ms-date-invalid

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## Suggestion

`Invalid value for ms.date: '{value}'. Must be a date in format MM/dd/yyyy.`

## Resolution

Confirm that the article is up-to-date with no broken content, then add a valid date in the format MM/dd/yyyy:

```yml
---
ms.date: 02/19/2019
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
