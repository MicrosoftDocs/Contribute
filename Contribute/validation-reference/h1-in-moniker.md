---
title: h1-in-moniker
description: Explanation and resolution for Docs build issue h1-in-moniker.
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 11/25/2019
ms.prod: non-product-specific
---
# h1-in-moniker

## Warning

`H1s are not allowed in moniker sections. Each article should have one and only one H1.`

H1 refers to the first heading in a Markdown file. When published to docs.microsoft.com, the H1 shows at the top of the page in a large font. An H1 is created by beginning a line with a single hash (#) followed by a space, then the heading text. You can only have one H1 in each file. H1s aren't allowed in moniker sections, because H1s in monikers can easily cause duplicate or missing H1s depending on how versioning is configured.

You might also get this message if a moniker section contains a line of equals signs making a double underline, like this: `=======`. This is an alternative Markdown syntax for an H1. It's also commonly seen in merge conflicts:

```markdown
<<<<<<< HEAD
...
=======
...
>>>>>>> 1d82c7efe18f86136247fb366df5030843199c19
```

## Resolution

To fix this issue, remove H1s from all moniker sections, and make sure the H1 at the top of the article is appropriate for all moniker sections. Note that skipping heading levels, such as following H1 with H3, isn't allowed.

If an H1 in a moniker section is actually a double underline (`=======`), remove it or replace it with a hashtag heading, such as `##`, as appropriate. If the double underline is part of a merge conflict, make sure to also remove the merge conflict beginning and ending markers and the obsolete text.

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
