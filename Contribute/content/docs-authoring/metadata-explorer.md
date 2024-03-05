---
title: Metadata explorer - Learn Authoring Pack
description: Learn about the Metadata explorer, included with the Learn Authoring Pack Visual Studio Code extension.
author: gewarren
ms.author: gewarren
ms.service: learn
ms.topic: contributor-guide
ms.date: 06/10/2021
feedback_product_url: https://github.com/microsoft/vscode-docs-authoring/issues
---

# Metadata explorer

[!INCLUDE [markdown-extension](includes/markdown-extension.md)]

## Summary

The Metadata explorer appears automatically in the Explorer sidebar of Visual Studio Code when you open a Learn Markdown file. It has two main sections: [required metadata](../metadata.md#required-metadata) and [optional metadata](../metadata.md#optional-metadata).

:::image type="content" source="media/metadata-explorer.PNG" alt-text="Metadata explorer in Visual Studio Code":::

## Metadata sources

The Metadata explorer shows metadata from three sources: the YAML front matter of the Markdown file that's open in the editor, and the `fileMetadata` and `globalMetadata` sections of the docset's *docfx.json* file. Icons help to quickly identify the source of the displayed metadata. If your article is missing any required metadata, that metadata key appears with a warning icon.

| Icon | Metadata source |
| - | - |
| :::image type="content" source="media/markdown-icon.png" alt-text="Markdown icon"::: | YAML front matter of active Markdown file |
| :::image type="content" source="media/json-icon.png" alt-text="Json icon"::: | [`fileMetadata` section](https://github.com/dotnet/docs/blob/d34042d234a90d74df1baee17f664f89d5abd67f/docfx.json#L147) of *docfx.json* file |
| :::image type="content" source="media/globe-icon.png" alt-text="Globe icon"::: | [`globalMetadata` section](https://github.com/dotnet/docs/blob/d34042d234a90d74df1baee17f664f89d5abd67f/docfx.json#L111) of *docfx.json* file |
| :::image type="content" source="media/warning-icon.png" alt-text="Warning icon"::: | This required metadata is *missing completely* |

## Precedence

The Metadata explorer only shows unique metadata keys. If more than one value can apply for the same key, the explorer uses the same precedence settings as DocFx does. The order of precedence in decreasing priority is:

1. YAML front matter
1. `fileMetadata`
1. `globalMetadata`

If multiple folder-based glob patterns apply to a single article, the entry that appears last in the *docfx.json* file is selected. For example, consider the file at *C:/docs/csharp/reference/keywords.md* and the following entries in the *docfx.json* file:

```json
"ms.topic": {
  "csharp/**/*.md": "conceptual",
  "csharp/reference/*.md": "language-reference"
}
```

In this case, while both glob patterns include the path to the file, the second value of `language-reference` is selected.

## Tooltip

You can hover over a value to see an expanded display in the tooltip. This is especially useful for keys that have multiple values in an array. The information also includes the [source](#metadata-sources) of the metadata.

:::image type="content" source="media/metadata-hover.PNG" alt-text="Tooltip for metadata value in Metadata explorer.":::

## Refresh

If you have auto-save disabled in Visual Studio Code, the Metadata explorer refreshes automatically when you save your Markdown file. If you have auto-save enabled, you can refresh the displayed metadata by clicking the **Refresh** button at the top of the explorer.

When you open a different Markdown file, the explorer refreshes automatically.

## See also

- [Metadata](../metadata.md)
