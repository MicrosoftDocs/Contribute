---
title: Metadata for Microsoft Learn documentation
description: Learn about the required and optional metadata for Microsoft Learn documentation.
author: sarah-barrett
ms.author: sabarret
ms.reviewer: jasonh
ms.date: 10/13/2021
ms.topic: contributor-guide
ms.service: learn
ms.custom: external-contributor-guide
---

# Metadata for Microsoft Learn documentation

Metadata can be applied in the article (in the YAML front matter) or globally in the *docfx.json* file for the repo. If you're making an edit to an existing article, you probably won't have to change any metadata. However, if you're adding a new article, there are certain required metadata attributes that you'll need to include in the YAML front matter of the file.

Here's an example of metadata applied in the YAML front matter of a Markdown article:

```md
---
title:                     # the article title to show on the browser tab
description:               # 115 - 145 character description to show in search results
author: {github-id}        # the author's GitHub ID - will be auto-populated if set in settings.json
ms.author: {ms-alias}      # the author's Microsoft alias (if applicable) - will be auto-populated if set in settings.json
ms.date: {@date}           # the date - will be auto-populated when template is first applied
ms.topic: getting-started  # the type of article
---
# Heading 1 <!-- the article title to show on the web page -->
```

## Required metadata

The following table shows the required metadata attributes. If you omit any of these, you'll likely get a validation error during build.

| Field | Value | Why? |
| ----- | ----- | ---- |
| <code>author</code> | The author's GitHub account ID. | Identifies the author by GitHub ID in case there are questions about or problems with the content. In some cases, GitHub automation might notify the author of activity involving the file. |
| <code>description</code> |  A summary of the content. 75-300 characters. | Used in site search. Sometimes used on a search engine results page for improved SEO. |
| <code>ms.author</code> |The author's Microsoft alias, *without* "@microsoft.com". If you aren't a Microsoft employee, find a suitable Microsoft employee to use in this field. | Identifies the article's owner. The owner is responsible for decisions about the content of the article, and for the article's reporting and BI. |
| <code>ms.date</code> | A date in the format MM/DD/YYYY. | Displayed on the published page to indicate the last time the article was substantially edited or guaranteed fresh. The date is entered without time and is interpreted as 0:00 and in the UTC time zone. The date displayed to users is converted to their time zone. |
| <code>ms.service</code>  |The primary Microsoft offering the content is about.| Identifies Microsoft offering.<br/><br/>|
| <code>ms.topic</code>  | Usually one of the following values:<br/><br/><code>article</code>, <code>conceptual</code>, <code>contributor-guide</code>, <code>overview</code>, <code>quickstart</code>, <code>reference</code>, <code>sample</code>, <code>tutorial</code>. | Identifies the type of content for reporting purposes. |
| <code>title</code> | The page title. | This is the page title that's displayed on the browser tab. It's the most important metadata for SEO. |

Attributes are case-sensitive. Enter them exactly as listed, and use a colon and a space between the attributes and the value. If an attribute value includes a colon (:), a hash (#), or any other special character, you must enclose it either single (') or double (") quotes. For example:

```md
---
title: 'Quickstart: How to use hashtags (#) to make a point on the internet'
---
# Heading 1 <!-- the article title to show on the web page -->
```
