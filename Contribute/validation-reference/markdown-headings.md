---
title: Markdown Headings
description: Describes requirements for Markdown headings.
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 05/03/2017
---
# Markdown headings

The following validation requirements apply to headings in OPS Markdown files.

## H1

`H1` refers to the first heading in a Markdown file. When published to docs.microsoft.com, the H1 shows at the top of the page in a large font.

An H1 is created by beginning a line with a single hash (`#`) followed by a space, then the heading text. For example, the H1 of this article is:

```md
# Markdown headings
```

The following rules apply to H1 headings:

- An H1 must be present in the file.
- There can only be one H1.
- The H1 must have content.

  ```markdown
  # 
  This is not allowed.
  ```
- There must be a space between the `#` and the H1 content. An H1 with no space doesn't render as a heading on the published page.

  ```markdown
  #This looks bad on the site.
  ```
- The H1 must be the first content in the file after the YML metadata header. No content, such as text or images, is allowed between the end of the YML header and the H1.

  ```markdown
  ---
  ... YML would go here
  ---
  ![cheerful image](not-allowed.jpg)
  # This cheer is not allowed
  ```
- The HTML element for first-level headings, `<h1>`, should not be used. Use the Markdown syntax (`# `).
- The H1 should be no more than 100 characters long. This is a style guideline.

## H2 - H6

H2 (`## `) through H6 (`###### `) are allowed in OPS. Use the Markdown headers, not the HTML (`<h2>` - `<h6>`), to create headings.
