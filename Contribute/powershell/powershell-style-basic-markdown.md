---
title: Template and cheatsheet for PowerShell articles
description: This article contains a handy template you can use to create new articles for the PowerShell docs
ms.date: 10/09/2019
---
# Markdown style guide for PowerShell-Docs

This article provides some style guidance specific to the PowerShell-Docs content.

For other writing style guidance, see the [Microsoft Style Guide](https://docs.microsoft.com/style-guide/welcome/).

## Metadata

This template contains examples of Markdown syntax, as well as guidance on setting the metadata.
When creating a Markdown file, you should copy the included template to a new file, fill out the
metadata as specified below, and set the H1 heading above to the title of the article.

The required metadata block is in the following sample metadata block:

```md
---
author: [GITHUB USERNAME]
description: [usually a summary of your first paragraph. It gets displayed in search results, and can help drive the correct traffic if well written.]
ms.date: [CREATION/UPDATE DATE - mm/dd/yyyy]
title: [ARTICLE TITLE]
---
# The H1 should not be the same as the title, but should describe the article contents
```

- You **must** have a space between the colon (:) and the value for a metadata element.
- Colons in a value (for example, a title) break the metadata parser. In this case, surround the
  title with double quotes (for example,
  `title: "Writing .NET Core console apps: An advanced step-by-step guide"`).
- **author**: The author field should contain the **GitHub username** of the author.
- **description**: Summarizes the content of the article. It's usually shown in the search results
  page, but it isn't used for search ranking. Its length should be 115-145 characters including
  spaces.
- **ms.date**: The date of the last significant update. Update this on existing articles if you
  reviewed and updated the entire article. Small fixes, such as typos or similar don't warrant an
  update.
- **title**: Appears in search engine results. The title shouldn't be identical to the title in your
  H1 heading, and it should contain 60 characters or fewer.

Other metadata is attached to each article, but we typically apply most metadata values at the
folder level, specified in **docfx.json**.

## Product Terminology

There are several variants of PowerShell. This table defines some of the different terms used to
discuss PowerShell.

- **PowerShell** - This is the default. PowerShell is the product we ship. The term PowerShell can
  be used to describe any edition of the product.
- **PowerShell Core** - PowerShell built on .NET Core Common Language Runtime (CoreCLR) for any of
  the supported platforms.
- **Windows PowerShell** - PowerShell built on .NET Framework Common Language Runtime (CLR). Windows
  PowerShell ships only on Windows and requires the full .Net Framework CLR.

In general, references to "Windows PowerShell" in documentation can be changed to "PowerShell".
"Windows PowerShell" should **not** be changed when Windows-specific technology is being discussed.

## Basic Markdown, GFM, and special characters

You can learn the basics of Markdown, GitHub Flavored Markdown (GFM), and OPS specific extensions in
the general articles on [Markdown](../how-to-write-use-markdown.md) and
[Markdown reference](../markdown-reference.md).

Markdown uses special characters such as \*, \`, and \# for formatting. If you wish to include one
of these characters in your content, you must do one of two things:

- Put a backslash before the special character to "escape" it (for example, `\*` for a \*)
- Use the [HTML entity code](http://www.ascii.cl/htmlcodes.htm) for the character (for example,
  `&#42;` for a &#42;).
- Markdown files should use plain ASCII text or UTF-8 encoding. However, avoid using multi-byte
  UTF-8 characters. Instead use an HTML entity. For example, for the copyright symbols use `&copy;`.
  It is rendered as: "&copy;".

## Hyperlinks

- Avoid using bare URLs. Links should use Markdown syntax `[friendlyname](url-or-path)`
- Links must have a friendly name, usually the title of the linked topic
- All items in the "related links" section at the bottom should be hyperlinked.
- Use relative links when linking to other content that is hosted on **docs.microsoft.com**.
- Do not use backticks, bold, or other markup inside the brackets of a hyperlink.

For more detailed information about linking, see [Using links in documentation](../how-to-write-links.md).

## Filenames

Filenames use the following rules:

- Contain only letters, numbers, and hyphens.
- No spaces or punctuation characters. Use the hyphens to separate words and numbers in the file
  name.
- Use action verbs that are specific, such as develop, buy, build, troubleshoot. No -ing words.
- No small words - don't include a, and, the, in, or, etc.
- Must be in Markdown and use the .md file extension.
- Keep file names reasonably short. They are part of the URL for your articles.

## Blank lines, spaces, and tabs

Remove duplicate blank lines. Multiple blank lines render as a single blank line in HTML so there is
not purpose for multiple blank lines.

Blank lines also signal the end of a block in Markdown. There should be a single blank between
Markdown blocks of different types (for example, between a paragraph and a list or header).

> [!NOTE]
> Spacing is significant in Markdown. Always uses spaces instead of hard tabs. Remove
> extra spaces at the end of lines.

## Titles and headings

Only use [ATX headings][atx] (# style, as opposed to `=` or `-` style headers).

- Use sentence case - only proper nouns and the first letter of a title or header should be
  capitalized
- There must be a single space between the `#` and the first letter of the heading
- Headings should be surrounded by a single blank line
- Only one H1 per document
- Header levels should increment by one - do not skip levels
- Do not use backticks, bold, or other markup in headers

> [!CAUTION]
> The schema enforced by [PlatyPS][platyPS] for cmdlet reference requires specific H2 and H3
> headers. Adding or removing headers can break the build. For more information, see the
> [cmdlet reference style guide](powershell-style-reference.md).

## Limit line length to 100 characters

This simplifies the command-line output of diffs and history.

This rule was not in force for much of the existing content in PowerShell-Docs, but we are working
towards it over time. Feel free to help out. The [reflow extension][reflow] in Visual Studio Code
(VSCode) makes it easy to reformat paragraphs to this limit.

## Lists

If your list contains multiple sentences or paragraphs, consider using a sub-level header rather
than a list.

List should be surrounded by a single blank line.

### Unordered lists

Do not end list items with a period unless they contain multiple sentences. Use the hyphen character
(`-`) for list item bullets. This avoids confusion with bold or italic markup that uses the asterisk
[`*`]. To include a paragraph or other elements under a bullet item, insert a line break and align
indentation with the first character after the bullet.

For example:

```markdown
This is a list that contain sub-elements under a bullet item.

- First bullet item

  Sentence explaining the first bullet.

  - Sub-bullet item

    Sentence explaining the sub-bullet.

- Second bullet item
- Third bullet item
```

This is a list that contains sub-elements under a bullet item.

- First bullet item

  Sentence explaining the first bullet.

  - Sub-bullet item

    Sentence explaining the sub-bullet.

- Second bullet item
- Third bullet item

### Ordered lists

To include a paragraph or other elements under a numbered item, align indentation with the first
character after the item number.

```markdown
1. For the first element, insert a single space after the 1. Long sentences should be
   wrapped to the next line and must line up with the first character after the numbered
   list marker.

   To include a second element (like this one), insert a line break after the first
   and align indentations. The indentation of the second element must line up with
   the first character after the numbered list marker. For single digit items, like
   this one, you indent to column 4. For double digits items, for example item number
   10, you indent to column 5.

1. The next numbered item starts here.
```

to get this output:

> 1. For the first element, insert a single space after the 1. Long sentences should be
>    wrapped to the next line and must line up with the first character after the numbered
>    list marker.
>
>    To include a second element (like this one), insert a line break after the first
>    and align indentations. The indentation of the second element must line up with
>    the first character after the numbered list marker. For single digit items, like
>    this one, you indent to column 4. For double digits items, for example item number
>    10, you indent to column 5.
>
> 1. The next numbered item starts here.

All items in a numbered listed should use the number `1.` instead of incrementing for each item.
Markdown rendering increments the value automatically. This makes reordering items easier and
standardizes the indentation of subordinate content.

## Formatting command syntax elements

- PowerShell cmdlet names are [Pascal Cased][pascal-case]. Verbs are separated from nouns by a
  hyphen. Always use the full Pascal Case name for cmdlets and parameters. Avoid using aliases
  unless you are specifically talking about an alias.

- Within a paragraph, language keywords, cmdlet names, and variable references should be wrapped in
  backtick (`` ` ``) characters. Property, parameter, and class names should be **bold**.

  For example:

  ~~~markdown
  The following code assigns the output of `Get-ChildItem` to the `$files` variable.

  ```powershell
  $files = Get-ChildItem C:\Windows
  ```
  ~~~

- When referring to a parameter by name, the name should be **bold**. When illustrating the use of
  a parameter with the hyphen prefix, the parameter should be wrapped in backticks. For example:

  ```markdown
  The parameter's name is **Name**, but it is typed as `-Name` when used on the command
  line as a parameter.
  ```

- When referring to external commands (EXEs, scripts, etc.), the command name should be bold, all
  lowercase (or capitalized if at the beginning of a sentence), and include the appropriate file
  extension. For example:

  ```markdown
  For example, on Windows systems, you can use the `net start` and `net stop` commands
  to start and stop a service. **Sc.exe** is another service control tool for Windows.
  That name does not fit into the naming pattern for the **net.exe** service commands.
  ```

- When showing example usage of an external command, the example should be wrapped in backticks.
  When there is a name collision with an alias you must include the file extension in the command
  example. For example:

  ```markdown
  To start the spooler service on a remote computer named DC01, you type `sc.exe \\DC01 start spooler`.
  ```

- When writing a conceptual article (as opposed to reference content), the first instance of a
  cmdlet name should be hyperlinked to the cmdlet documentation. Do not use backticks, bold, or
  other markup inside the brackets of a hyperlink.

  For example:

  ```markdown
  This [Write-Host](/powershell/module/Microsoft.PowerShell.Utility/Write-Host) cmdlet
  uses the **Object** parameter to ...
  ```

  For more information, see [Hyperlinks](#hyperlinks) section of the Style Guide.

## Images

The syntax to include an image is:

```Syntax
![[alt text]](<folderPath>)
```

Example:

```markdown
![Introduction](./media/overview/Introduction.png)
```

Where `alt text` is a brief description of the image and `<folder path>` is a relative path to the
image. Alternate text is required for screen readers for the visually impaired. It is also useful in
case there is a site bug where the image cannot be rendered.

Images should be stored in a `media/<article-name>` folder within the folder containing your
article. Images should not be shared between articles. Create a folder that matches the filename of
your article under the `media` folder. Copy the images for that article to that new folder. If an
image is used by multiple articles, each image folder must have a copy of that image file. This
practice prevents a change to an image in one article affecting another article.

In some cases, you want to share images, like logos and icons, across multiple articles. These
images are stored in the `/media/shared` folder at the root of the repository.

The following image file types are supported: *.png", *.gif", *.jpeg", *.jpg", *.svg

<!-- External URLs -->
[platyPS]: https://github.com/PowerShell/platyPS
[markdig]: https://github.com/lunet-io/markdig
[CommonMark]: https://spec.commonmark.org/
[atx]: https://github.github.com/gfm/#atx-headings
[pascal-case]: https://en.wikipedia.org/wiki/PascalCase
[reflow]: https://marketplace.visualstudio.com/items?itemName=marvhen.reflow-markdown
