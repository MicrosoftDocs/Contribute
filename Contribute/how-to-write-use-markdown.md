---
# required metadata

title: How to use Markdown
description: Provides the basics and reference information for the Markdown markup used in Docs articles.
author: bryanla
ms.author: bryanla
manager: mbaldwin
ms.date: 07/13/2017
ms.topic: contributor-guide
ms.prod: n.a
ms.service: n.a
ms.technology: n.a

# optional metadata
#keywords:
#ROBOTS:
audience: external
#ms.devlang:
#ms.reviewer: bryanla
#ms.suite: ems
#ms.tgt_pltfrm:
#ms.custom:

---
# How to use Markdown

Docs.microsoft.com articles are written in a lightweight markup language called [Markdown](https://daringfireball.net/projects/markdown/), which is both easy to read and easy to learn. Because of this, it has quickly become an industry standard.

Because Docs content is stored in GitHub, it can use a superset of Markdown called [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/), which provides additional functionality for common formatting needs. Additionally, Open Publishing Services (OPS) implements DocFX Flavored Markdown (DFM). DFM is highly compatible with GitHub Flavored Markdown (GFM), adding functionality to enable Docs-specific features.

## Markdown basics

### Headings

To create a heading, you use a hash mark (#), as follows:

```markdown
    # This is heading 1
    ## This is heading 2
    ### This is heading 3
    #### This is heading 4
```

### Bold and italic text

To format text as **bold**, you enclose it in two asterisks:

```markdown
    This text is **bold**.
```

To format text as *italic*, you enclose it in a single asterisk:

```markdown
    This text is *italic*.
```

To format text as both ***bold and italic***, you enclose it in three asterisks:

```markdown
    This is text is both ***bold and italic***.
```

### Lists

#### Unordered list

To format an unordered/bulleted list, you can use either asterisks or dashes. For example, the following Markdown:

```markdown
- List item 1
- List item 2
- List item 3
```

will be rendered as:

- List item 1
- List item 2
- List item 3

To nest a list within another list, indent the child list items. For example, the following Markdown:

```markdown
- List item 1
  - List item A
  - List item B
- List item 2
```

will be rendered as:

* List item 1
    * List item A
    * List item B
* List item 2

#### Ordered list

To format an ordered/stepwise list, you use corresponding numbers. For example, the following Markdown:

```markdown
1. First instruction
2. Second instruction
3. Third instruction
```

will be rendered as:

1. First instruction
2. Second instruction
3. Third instruction

To nest a list within another list, indent the child list items. For example, the following Markdown:

```markdown
1. First instruction
    a. Sub-instruction
    b. Sub-instruction

2. Second instruction
```

will be rendered as:

1. First instruction
    a. Sub-instruction
    b. Sub-instruction

2. Second instruction

### Tables

Tables are not part of the core Markdown specification, but GFM supports them. You can create tables by using the pipe (|) and hyphen (-) characters. Hyphens create each column's header, while pipes separate each column. Include a blank line before your table so it's rendered correctly.

For example, the following Markdown:

```markdown
| Fun                  | With                 | Tables          |
| :------------------- | -------------------: |:---------------:|
| left-aligned column  | right-aligned column | centered column |
| $100                 | $100                 | $100            |
| $10                  | $10                  | $10             |
| $1                   | $1                   | $1              |
```

will be rendered as:

| Fun                  | With                 | Tables          |
| :------------------- | -------------------: |:---------------:|
| left-aligned column  | right-aligned column | centered column |
| $100                 | $100                 | $100            |
| $10                  | $10                  | $10             |
| $1                   | $1                   | $1              |

For more information on creating tables, see:

- The DFM [table wrapping feature](#table-wrapping), which can help with formatting of wide tables
- GitHub's [Organizing information with tables](https://help.github.com/articles/organizing-information-with-tables/)
- The [Markdown Tables Generator](https://www.tablesgenerator.com/markdown_tables) web app
- [Adam Pritchard's Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#wiki-tables)
- [Michel Fortin's Markdown Extra](https://michelf.ca/projects/php-markdown/extra/#table)
- [Convert HTML tables to Markdown](https://jmalarcon.github.io/markdowntables/)

### Links

The Markdown syntax for an inline link consists of the `[link text]` portion, which is the text that will be hyperlinked, followed by the `(file-name.md)` portion, which is the URL or file name that's being linked to:

 `[link text](file-name.md)`

For more information on linking, see:

- The [Markdown syntax guide](https://daringfireball.net/projects/markdown/syntax#link) for details on Markdown's base linking support.
- The [Links](how-to-write-links.md) section of this guide for details on additional linking syntax that DFM provides.

### Code snippets

Markdown supports the placement of code snippets both inline in a sentence and as a separate "fenced" block between sentences. For details, see:

- [Markdown's native support for code blocks](https://daringfireball.net/projects/markdown/syntax#precode)
- [GFM support for code fencing and syntax highlighting](https://help.github.com/articles/creating-and-highlighting-code-blocks/)

Fenced code blocks are an easy way to enable syntax highlighting for your code snippets. The general format for fenced code blocks is:

    ```alias
    ...
    your code goes in here
    ...
    ```

The alias after the initial three backtick (`) characters defines the syntax highlighting to be used. The following is a list of commonly used programming languages on the Azure platform and the matching label:

| Language or CLI | Language alias |
| ------- | ------- |
| Azure CLI | azurecli |
| AzCopy | azcopy |
| C++ | cpp |
| C# | csharp |
| F# | fsharp |
| Java | java|
| JavaScript | javascript |
| JSON | json |
| Node.js | nodejs |
| Objective-C | objc |
| PHP | php |
| PowerShell | powershell |
| Python | python |
| Ruby | ruby |
| SQL / T-SQL | sql |
| Swift | swift |
| VB | vb |
| XAML | xaml |
| XML | xml |

For a full list of supported languages, see [Language names and aliases](https://highlightjs.readthedocs.io/en/latest/css-classes-reference.html#language-names-and-aliases).

#### Example: C\#

__Markdown__

    ```csharp
    // Hello1.cs
    public class Hello1
    {
        public static void Main()
        {
            System.Console.WriteLine("Hello, World!");
        }
    }
    ```

__Render__

```csharp
// Hello1.cs
public class Hello1
{
    public static void Main()
    {
        System.Console.WriteLine("Hello, World!");
    }
}
```

#### Example: SQL

__Markdown__

    ```sql
    CREATE TABLE T1 (
      c1 int PRIMARY KEY,
      c2 varchar(50) SPARSE NULL
    );
    ```

__Render__

```sql
CREATE TABLE T1 (
  c1 int PRIMARY KEY,
  c2 varchar(50) SPARSE NULL
);
```

## OPS custom Markdown extensions

> [!NOTE]
> Open Publishing Services (OPS) implements DocFX Flavored Markdown (DFM), which is highly compatible with GitHub Flavored Markdown (GFM). DFM adds some functionality through Markdown extensions. As such, selected articles from the full OPS Authoring Guide are included in this guide for reference. (For example, see "DFM and Markdown extensions" and "Code snippets" in the table of contents.)

Docs articles use GFM for most article formatting, such as paragraphs, links, lists, and headings. For richer formatting, articles can use DFM features such as:

- Note blocks
- Includes
- Selectors
- Embedded videos
- Code snippets/samples

For the complete list, refer to "DFM and Markdown extensions" and "Code snippets" in the table of contents.

### Note blocks

You can choose from four types of note blocks to draw attention to specific content:

- NOTE
- WARNING
- TIP
- IMPORTANT

In general, note blocks should be used sparingly because they can be disruptive. Although they also support code blocks, images, lists, and links, try to keep your note blocks simple and straightforward.

### Includes

When you have reusable text or image files that need to be included in article files, you can use a reference to the "include" file via the DFM file include feature. This feature instructs OPS to include the file in your article file at build time, making it part of your published article. Three types of includes are available to help you reuse content:

- Inline: Reuse a common text snippet inline with within another sentence.
- Block: Reuse an entire Markdown file as a block, nested within a section of an article.
- Image: This is how standard image inclusion is implemented in Docs.

An inline or block include is just a simple Markdown (.md) file. It can contain any valid Markdown. All include Markdown files should be placed in a [common `/includes` subdirectory](git-github-fundamentals.md#includes-subdirectory), in the root of the repository. When the article is published, the included file is seamlessly integrated into it.

Here are requirements and considerations for includes:

- Use includes whenever you need the same text to appear in multiple articles.
- Use block includes for significant amounts of content--a paragraph or two, a shared procedure, or a shared section. Do not use them for anything smaller than a sentence.
- Includes won't be rendered in the GitHub rendered view of your article, because they rely on DFM extensions. They'll be rendered only after publication.
- Ensure that all the text in an include is written in complete sentences or phrases that do not depend on preceding text or following text in the article that references the include. Ignoring this guidance creates an untranslatable string in the article that breaks the localized experience.
- Don't embed includes within other includes. They are not supported.
- Place media files in a media folder that's specific to the include subdirectory--for instance, the `<repo>`/includes/media folder. The media directory should not contain any images in its root. If the include does not have images, a corresponding media directory is not required.
- As with regular articles, don't share media between include files. Use a separate file with a unique name for each include and article. Store the media file in the media folder that's associated with the include.
- Don't use an include as the only content of an article.  Includes are meant to be supplemental to the content in the rest of the article.

### Selectors

Use selectors in technical articles when you author multiple flavors of the same article, to address differences in implementation across technologies or platforms. This is typically most applicable to our mobile platform content for developers. There are currently two different types of selectors in DFM, a single selector and a multi-selector.

Because the same selector Markdown goes in each article in the selection, we recommend placing the selector for your article in an include. Then you can reference that include in all your articles that use the same selector.

### Code snippets

DFM supports advanced inclusion of code in an article, via its code snippet extension. It provides advanced rendering that builds on GFM features such as programming language selection and syntax coloring, plus nice features such as:

- Inclusion of centralized code samples/snippets from an external repository.
- Tabbed UI to show multiple versions of code samples in different languages.

## Gotchas and troubleshooting

### Alt text

Alt text that contains underscores won't be rendered properly. For example, instead of using this:

```markdown
![ADextension_2FA_Configure_Step4] (./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

Escape the underscores like this:

```markdown
![ADextension\_2FA\_Configure\_Step4] (./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

### Apostrophes and quotation marks

If you copy from Word into a Markdown editor, the text might contain "smart" (curly) apostrophes or quotation marks. These need to be encoded or changed to basic apostrophes or quotation marks. Otherwise, you end up with things like this when the file is published: Itâ€™s

Here are the encodings for the "smart" versions of these punctuation marks:

- Left (opening) quotation mark: `&#8220;`
- Right (closing) quotation mark: `&#8221;`
- Right (closing) single quotation mark or apostrophe: `&#8217;`
- Left (opening) single quotation mark (rarely used): `&#8216;`

### Angle brackets

If you use angle brackets in text (not code) in your file--for example, to denote a placeholder--you need to manually encode the angle brackets. Otherwise, Markdown thinks that they're intended to be an HTML tag.

For example, encode `<script name>` as `&lt;script name&gt;`

## See also

### Markdown resources

- [Introduction to Markdown](https://daringfireball.net/projects/markdown/syntax)
- [Docs Markdown cheat sheet](./media/documents/markdown-cheatsheet.pdf?raw=true)
- [GitHub's Markdown Basics](https://help.github.com/articles/markdown-basics/)
