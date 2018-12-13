---
title: hard-coded-locale
description: Explanation and resolution for Docs build issue hard-coded-locale.
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
---
# hard-coded-locale

## Warning

`Link {URL} contains locale code {code}. For localizability, remove {code} from links to Microsoft sites.`

Locale codes, such as `en-us`, should not be included in links to certain Microsoft sites. If you include a locale code in a link in English content, it will also be included in localized links, which leads to a bad localized experience. For example, if a link in German localized content includes `en-us`, German customers will find themselves linking to the English article, even if a German version is available.

The following sites are in scope for this validation:

- azure.microsoft.com
- docs.microsoft.com
- msdn.microsoft.com
- technet.microsoft.com

## Resolution

Remove locale codes from links to Microsoft sites. The following is an example.

Before:

`https://docs.microsoft.com/en-us/vsts/load-test/app-service-web-app-performance-test`

After:

`https://docs.microsoft.com/vsts/load-test/app-service-web-app-performance-test`

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](../includes/validation-reference-help.md)]