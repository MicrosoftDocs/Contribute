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

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## Suggestion

`H1 is required. Use a single hash (#) followed by a space to create your top-level heading.`

H1 refers to the first heading in a Markdown file. When published to learn.microsoft.com, the H1 shows at the top of the page in a large font. An H1 is created by beginning a line with a single hash (#) followed by a space, then the heading text.

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
> This rule does not apply to included files. If you get H1 results on included files, you most likely need to move your included files into an `includes` folder. The `includes` folder can be at any level in the file path. Based on the path, Docs build will recognize the file as an included file and H1 validations won't run.
>
> A common cause of missing H1s in parent files is misuse of included files: the H1 is in the included file, not in the parent file. This isn't allowed, because using an H1 in an included file either means there are duplicate H1s in parent files or the included file is used only once. H1s should be unique within a content set and included files should only be used to share content among multiple files. If you get `h1-missing` results because the H1 is in an included file, the solution is to move the H1 - and all the included content if the included file is used only once - into the parent file. For more information about included files in Docs, see the Microsoft-internal article [Include reusable content in articles](https://review.learn.microsoft.com/en-us/help/contribute/includes-best-practices?branch=main).

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
