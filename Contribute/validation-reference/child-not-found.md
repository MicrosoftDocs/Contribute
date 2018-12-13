---
title: #error-code
description: Explanation and resolution for Docs build issue #error-code
author: {github-id}
ms.author: {ms-alias} # Microsoft employees only
ms.topic: error-reference
ms.date: {@date}
ms.prod: non-product-specific
---
# child-not-found
<!-- error code tentatively drafted based on Yun's doc - may need to change doc and file name later! -->

## Error

`Children Uid(s) {UID(s)} can't be found.`

## Resolution

Verify that the unit YML files are using the exact same UIDs as what's in the module index.yml. Usually, it's been worded slightly differently, like `learn-pr.sample-module.1-first-unit`, when it needs to be `learn.sample-module.1-first-unit`.

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](../includes/validation-reference-help.md)]