---
title: Dev lang completion - Learn Authoring Pack
description: Learn how dev lang completion assists contributors in the Learn Authoring Pack, Visual Studio Code extension.
author: scottaddie
ms.service: learn
ms.topic: contributor-guide
ms.date: 03/03/2020
ms.author: scaddie
---

# Dev lang completion

[!INCLUDE [markdown-extension](includes/markdown-extension.md)]

## Summary

Contributors need assistance determining the valid language identifiers (dev langs) that can follow triple-backticks (code fence openings) in a Markdown file. Unfortunately, build-time validation of dev langs doesn't exist. The result is disparate representations of a single language within the same conceptual docset.

Consider C# as an example. Contributors have used `c#`, `C#`, `cs`, `csharp`, and others as dev lang representations of the language. Which of the preceding representations is correct?

The *Dev lang completion* feature dispels the confusion by displaying a list of known dev langs. Upon selecting a dev lang name from IntelliSense:

* The code fence is closed.
* The caret is positioned in the code fence.

## Preferences

It's not possible to disable this feature. The following settings are available:

* [Display commonly used dev langs](#display-commonly-used-dev-langs)
* [Display all known dev langs](#display-all-known-dev-langs)

### Display commonly used dev langs

Only a subset of the valid dev langs will be used in a single docset. To enhance the user experience:

1. In Visual Studio Code, open the docset to the root directory.
1. Select **File** > **Preferences** > **Settings** and filter by *Learn Markdown Extension*.
1. Click the **Edit in settings.json** link in the **Markdown: Docset Languages** section.
1. Add the following `markdown.docsetLanguages` property to the *settings.json* file:

    ```json
    {
        "markdown.docsetLanguages": [

        ]
    }
    ```

1. Position your caret in the property's empty array, and activate IntelliSense (via <kbd>Ctrl</kbd> + <kbd>Space</kbd>). A list of known dev lang names appears.
1. Add dev lang names to the array until you're satisfied with the list. For example, the following list will display four dev lang names to the user after typing triple-ticks:

    ```json
    {
        "markdown.docsetLanguages": [
            ".NET Core CLI",
            "C#",
            "Markdown",
            "YAML"
        ]
    }
    ```

1. Save your changes to the *settings.json* file.

> [!WARNING]
> An empty `markdown.docsetLanguages` array causes all known dev langs to display.

### Display all known dev langs

By default, all known dev lang names are displayed in IntelliSense. This setting overrides the `markdown.docsetLanguages` property described in [Display commonly used dev langs](#display-commonly-used-dev-langs).

To change this setting:

1. Select **File** > **Preferences** > **Settings** and filter by *Learn Markdown Extension*.
1. Toggle the setting in the **Markdown: All Available Languages** section.

## In action

Below is a brief demonstration of this feature:

[![Dev lang completion](media/dev-lang-completion.gif)](media/dev-lang-completion.gif#lightbox)
