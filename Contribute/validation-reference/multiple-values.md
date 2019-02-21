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

**Coming soon!**

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## Suggestion

`Single-valued attribute {attribute} has multiple values. Remove additional values.`

You specified more than one value for an attribute that is ony allowed one value.

`Single-valued attribute {attribute} is in multi-valued array format. Change to scalar format.`

Attributes that aren't allowed to have more than one value must be specified in the single-valued (scalar) YML format.

## Resolution

You get this Suggestion any time a multi-valued array is used for a single-valued attribute, either with multiple values or a single value in the array.

YML supports the following array formats for multi-valued attributes, such as `ms.custom`:

```yml
---
# comma-separated bracketed list:
ms.custom: [WIP, generated-via-CI]

# each value on its own line:
ms.custom:
  - WIP
  - generated-via-CI
---
```

These formats aren't valid for single-valued attributes, such as `author`.

If you specified multiple values, review the specified values and determine which is correct. Remove other values and specify the single value on the same line as the attribute with no brackets, as follows:

```yml
---
author: meganbradley
---
```

If you have a single-valued array, change it to the scalar format above.

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
