---
title: block-section-invalid
description: Explanation and resolution for Docs build issue block-section-invalid
author: meganbradley
ms.author: mbradley # Microsoft employees only
ms.topic: error-reference
ms.date: 09/10/2019
ms.prod: non-product-specific
---
# block-section-invalid

## Warning

`Invalid syntax for alert, div, or video. The text will be rendered as a block quote.`

Several Docs Markdown extensions begin with the string `> [!`. A space is required between `>` and `[`, and there must be a closing `]`. If the syntax is incorrect, the text will be rendered as a block quote.

## Resolution

[!INCLUDE [docs-authoring-pack](includes/docs-authoring-pack.md)]

Ensure the syntax is correct for the extension you're using:

```markdown

Alerts:

> [!NOTE]
> Information the user should notice even if skimming.

> [!TIP]
> Optional information to help a user be more successful.

> [!IMPORTANT]
> Essential information required for user success.

> [!CAUTION]
> Negative potential consequences of an action.

> [!WARNING]
> Dangerous certain consequences of an action.

Videos:

> [!VIDEO https://channel9.msdn.com/Series/Youve-Got-Key-Values-A-Redis-Jump-Start/03/player]

> [!VIDEO https://www.youtube.com/embed/iAtwVM-Z7rY]

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS]

Sections (div):

> [!div class="class"]

```


<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
