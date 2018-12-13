---
title: unit-not-in-module
description: Explanation and resolution for Docs build issue unit-not-in-module.
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
---
# unit-not-in-module
<!-- error code tentatively drafted based on Yun's doc - may need to change doc and file name later! -->

## Error

`Unit {file name} must belong to a Module.`

The unit UID does not appear in the module's index.

## Resolution

Verify that the unit YML files are using the exact same UIDs as what's in the module index.yml. Usually, it's been worded slightly differently, like `learn-pr.sample-module.1-first-unit`, when it needs to be `learn.sample-module.1-first-unit`.

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](../includes/validation-reference-help.md)]
