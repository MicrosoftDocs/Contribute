---
title: multiple-values
description: Explanation and resolution for Docs build issue multiple-values
author: meganbradley
ms.author: mbradley # Microsoft employees only
ms.topic: error-reference
ms.date: 2/19/2019
ms.prod: non-product-specific
---
# multiple-values

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## Suggestion

`Single-valued attribute {attribute} has multiple values. Remove additional values.`

You specified more than one value for an attribute that is ony allowed one value.

## Resolution

Review the specified values and determine which is correct. Specify the single value on the same line as the attribute with no brackets, as follows:

```yml
---
author: meganbradley
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
