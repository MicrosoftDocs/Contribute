---
title: Metadata for docs.microsoft.com
description: Learn about the required and optional metadata for Microsoft documentation.
author: sarah-barrett
ms.author: sabarret
ms.reviewer: jasonh
ms.date: 06/08/2021
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
---

# Metadata for docs

At Microsoft, we use metadata on Docs for reporting, discoverability of the content via search, and to drive aspects of the site experience. Metadata can be applied in the article (in the YAML front matter) or globally in the *docfx.json* file for the repo.

If you're making an edit to an existing article, you probably won't have to change any metadata. However, if you're adding a new article, there are certain required metadata values that you'll need to include in the YAML front matter of the file.

## Required metadata

The following table shows the required metadata keys. If you omit any of these, you'll likely get a validation error during build.

| Field | Value | Why? |
| ----- | ----- | ---- |
| `author` | The author's GitHub account ID. | Identifies the author by GitHub ID in case there are questions about or problems with the content. In some cases, GitHub automation might notify the author of activity involving the file. |
| `description` |  A summary of the content. 75-300 characters. | Used in site search. Sometimes used on a search engine results page for improved SEO. |
| `ms.author` | The author's Microsoft alias, *without* "@microsoft.com". If you aren't a Microsoft employee, find a suitable Microsoft employee to use in this field. | Identifies the article's owner. The owner is responsible for decisions about the content of the article, and for the article's reporting and BI. |
| `ms.date` | A date in the format MM/DD/YYYY. | Displayed on the published page to indicate the last time the article was substantially edited or guaranteed fresh. The date is entered without time and is interpreted as 0:00 and in the UTC time zone. The date displayed to users is converted to their time zone. |
| `ms.service` *or* <br/>`ms.prod` | The service or product identifier. Use one or the other, never both. This value is often set globally in the *docfx.json* file. | Used for issue triage and reporting. <br/><br/>Generally, use `ms.service` for cloud applications and use `ms.prod` for on-premises servers and applications.|
| `ms.topic`  | Usually one of the following values:<br/><br/>`article`, `conceptual`, `contributor-guide`, `interactive-tutorial`, `overview`, `quickstart`, `reference`, `sample`, `tutorial`. | Identifies the type of content for reporting purposes. |
| `title` | The page title. | It's the most important metadata for SEO. |

## Optional metadata

In addition to the required metadata, there are many optional metadata keys you can specify. The following table shows some of the optional metadata keys.

| Field | Value | Why? |
| ----- | ----- | ---- |
| `ms.custom` | **For writer or team use only.**<br/><br/>Commonly used for tracking specific docs or sets of content in telemetry tools. It's a single string value, and it's up to the consuming tool to parse it. Example: `ms.custom: "experiment1, content_reporting, all_uwp_docs, CI_Id=101022"`<br/><br/>**Character limit: The maximum string value length is 125 characters**. | `ms.custom` is a custom field that writers can use to track special projects or a subset of content. |
| `ms.reviewer` | The Microsoft alias of a person that reviews the content.| |
| `ms.subservice` | The more granular service to which the content belongs. Only use `ms.subservice` if you're also using `ms.service` | `ms.subservice` by itself isn't valid metadata. The author must associate it with a parent `ms.service` value. This attribute is a way to drill down further in reporting for a given `ms.service`. |
| `ms.technology` | The technology to which the content belongs. Only use `ms.technology` if you're also using `ms.prod`. |`ms.technology` by itself isn't valid metadata. The author must associate it with a parent `ms.prod` value. This attribute is a way to drill down further in reporting for a given `ms.prod`. |
| `ROBOTS` | `NOINDEX`, `UNFOLLOW` | Use ROBOTS in your metadata section to prevent the build and publishing process from showing content on search pages. When you want to use `ROBOTS` (and yes, it's all capitalized, even though other metadata tags aren't):<br>- Add `ROBOTS: NOINDEX` to your metadata section.<br>- `NOINDEX` causes the asset to not show up in search results.<br>- Use `NOFOLLOW` only when you archive an entire content set. |
| `no-loc` | A list of words in the article that should never be translated (localized). | Use this metadata to prevent "overlocalization". |
