---
title: ms-date-missing
description: Explanation and resolution for Docs build issue ms-date-missing
author: meganbradley
ms.author: mbradley # Microsoft employees only
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
---
# ms-date-missing

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## Suggestion

`Missing attribute: ms.date. A freshness date is required for this content. Add a date in format MM/DD/YYYY.`

Some content groups require `ms.date` to indicate "freshness" - that is, when the article was last reviewed for relevance, accuracy, correct screen shots, and working links. This is not the same as the last date the article was *published*, which will show on the page if `ms.date` is not explicitly specified.

## Resolution

Confirm that the article is up-to-date with no broken content, then add a valid date in the format MM/DD/YYYY:

```yml
---
ms.date: 02/19/2019
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
