---
title: h1-not-first
description: Explanation and resolution for Docs build issue h1-not-first
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 09/10/2019
ms.prod: non-product-specific
---
# h1-not-first

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## Suggestion

`Markdown content is not allowed before H1.`

Only the YAML metadata header can come before the H1 in a Markdown file. For example, if you want to add a note or an image at the top of the article, it must come after H1. The following is not allowed:

```markdown
---
# This is the YAML metadata header
author: meganbradley
---
> [!NOTE]
> You can't do this.

# This is the H1
```

Do this instead:

```markdown
---
# This is the YAML metadata header
author: meganbradley
---
# This is the H1

> [!NOTE]
> This is OK.
```

Another common cause of this issue is [byte order marks (BOMs)](http://www.websina.com/bugzero/kb/unicode-bom.html) before the YAML header. These are sometimes introduced by encoding issues when committing content to repos. They result in bad rendering in GitHub and should be removed.

## Resolution

Remove any content other than the YAML metadata header from before the H1.

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
