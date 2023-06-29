---
title: multiple-h1
description: Explanation and resolution for Docs build issue multiple-h1.
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 10/09/2019
ms.prod: non-product-specific
---
# multiple-h1

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## Suggestion

`Multiple H1s are not allowed. You can only have one top-level heading.`

H1 refers to the first heading in a Markdown file. When published to learn.microsoft.com, the H1 shows at the top of the page in a large font. An H1 is created by beginning a line with a single hash (#) followed by a space, then the heading text. You can only have one H1 in each file.

You might also get this message if your article contains a line of equals signs making a double underline, like this: `=======`. This is an alternative Markdown syntax for an H1. It's also commonly seen in merge conflicts:

```markdown
<<<<<<< HEAD
...
=======
...
>>>>>>> 1d82c7efe18f86136247fb366df5030843199c19
```

## Resolution

To fix this issue, change the heading level of subsequent H1s to H2 (`##`), or otherwise reorganize your file. Note that skipping heading levels, such as following H1 with H3, isn't allowed.

```markdown
---
author: meganbradley
ms.author: mbradley
---
# This is an H1

Some content...

## This is an H2
```

If an additional H1 is actually a double underline (`=======`), remove it or replace it with a hashtag heading, such as `##`, as appropriate. If the double underline is part of a merge conflict, make sure to also remove the merge conflict beginning and ending markers and the obsolete text.

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
