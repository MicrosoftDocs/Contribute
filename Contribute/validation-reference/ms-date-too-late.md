---
title: ms-date-too-late
description: Explanation and resolution for Docs build issue ms-date-too-late
author: meganbradley
ms.author: mbradley # Microsoft employees only
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
---
# ms-date-too-late

## Warning

`Invalid value for ms.date. The freshness date can't be more than 5 days in the future.`

The `ms.date` attribute is used to indicate "freshness" - that is, when the article was last reviewed for relevance, accuracy, correct screen shots, and working links. Therefore, it can't be in the future! Five days are allowed to account for release time, such as when content is frozen for QA in preparation for a major event.

## Resolution

Specify an `ms.date` no more than five days from today, in format MM/DD/YYYY.

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
