---
title: ms-date-invalid
description: Explanation and resolution for Docs build issue ms-date-invalid
author: meganbradley
ms.author: mbradley # Microsoft employees only
ms.topic: error-reference
ms.date: 09/10/2019
ms.prod: non-product-specific
---
# ms-date-invalid

## Warning

`Invalid value for ms.date: '{value}'. Must be a date in format MM/DD/YYYY, no more than 30 days from today.`

## Resolution

Confirm that the article is up-to-date with no broken content, then add a valid date in the format MM/DD/YYYY:

```yml
---
ms.date: 02/19/2019
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
