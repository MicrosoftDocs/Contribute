---
title: title-missing
description: Explanation and resolution for Docs build issue title-missing
author: meganbradley
ms.author: mbradley # Microsoft employees only
ms.topic: error-reference
ms.date: 2/6/2019
ms.prod: non-product-specific
---
# title-missing

## Warning

`Missing attribute: title. Add a title string (19 - 59 characters) to show in search engine results.`

## Resolution

Add a title string to show in search results. In general, titles should be between 19 and 59 characters, should be distinct from the H1 of the article, and should include relevant branding words. You shouldn't include " | Microsoft Docs" in your title - this is added automatically by Docs, and is ignored if you add it explicitly. If you want to add additional branding, such as " - Azure", to all titles in a content set, set the `titleSuffix` metadata value globally or for a folder.

You can preview how your title will look in Google on [https://moz.com/learn/seo/title-tag](https://moz.com/learn/seo/title-tag).

If you're a Microsoft employee, see [SEO Basics](https://review.docs.microsoft.com/en-us/help/contribute/contribute-how-to-write-seo-basics?branch=master) in the internal Contributor Guide for more information about good titles and search engine optimization (SEO).

[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
