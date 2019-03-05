---
title: yaml-header-invalid
description: Explanation and resolution for Docs build issue yaml-header-invalid
author: meganbradley
ms.author: mbradley # Microsoft employees only
ms.topic: error-reference
ms.date: 2/26/2019
ms.prod: non-product-specific
---
# yaml-header-invalid

## Warning

`Invalid YAML header: Improper use of a colon in a metadata entry.`

Usually this means an unquoted metadata value in a YAML header includes a colon or another special character. It can also mean that a space is missing after the colon in a key/value pair.

## Resolution

Review your YAML header. Look for the following mistakes.

Colon in unquoted value:

```yml
---
title: Common mistake: I included a colon in my unquoted value.
---
```

Change to:

```yml
---
title: 'Common mistake: I included a colon in my unquoted value.'
---
```

No space after colon in key/value pair:

```yml
---
title:I omitted a space.
---
```

Change to:

```yml
---
title: I omitted a space.
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
