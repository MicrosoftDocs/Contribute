---
title: h1-missing
description: Explanation and resolution for Docs build issue h1-missing.
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
---
# h1-missing

## Warning

`H1 is required. Use a single hash (#) followed by a space to create your top-level heading.`

H1 refers to the first heading in a Markdown file. When published to docs.microsoft.com, the H1 shows at the top of the page in a large font. An H1 is created by beginning a line with a single hash (#) followed by a space, then the heading text.

## Resolution

To fix this issue, add an H1 as the first content after the YML metadata block in your file:

```markdown
---
author: meganbradley
ms.author: mbradley
---
# This is an H1
```

> [!NOTE]
> This rule does not apply to included files. If you get H1 warnings on included files, you most likely need to move your included files into an `includes` folder. The `includes` folder can be at any level in the file path. Based on the path, Docs build will recognize t he file as an included file and H1 validations won't run.

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]