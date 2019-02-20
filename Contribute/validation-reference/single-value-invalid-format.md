---
title: single-value-invalid-format
description: Explanation and resolution for Docs build issue single-value-invalid-format
author: meganbradley
ms.author: mbradley # Microsoft employees only
ms.topic: error-reference
ms.date: 2/19/2019
ms.prod: non-product-specific
---
# single-value-invalid-format

**Coming soon!**

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## Suggestion

`Single-valued attribute {attribute} is in multi-valued array format. Change to scalar format.`

Attributes that aren't allowed to have more than one value must be specified in the single-valued (scalar) YML format.

## Resolution

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

These formats aren't valid for single-valued attributes, such as `author`. Use this scalar format instead:

```yml
---
author: meganbradley
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
