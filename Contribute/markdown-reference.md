---
title: Markdown reference for docs.microsoft.com
description: Learn the Markdown features and syntax used in the Microsoft Docs platform.
author: meganbradley
ms.author: mbradley
ms.date: 05/18/2018
ms.topic: contributor-guide
ms.prod: non-product-specific
---

# Markdown Reference

Markdown is a lightweight markup language with plain text formatting syntax. The Docs platform supports the CommonMark standard for Markdown, plus some custom Markdown extensions designed to provide richer content on docs.microsoft.com. This article provides an alphabetical reference for using Markdown for docs.microsoft.com.

You can use any text editor to author Markdown. For an editor that facilitates inserting both standard Markdown syntax and custom Docs extensions, we recommend [VS Code](https://code.visualstudio.com/) with the [Docs Authoring Pack](https://aka.ms/DocsAuthoringPack) installed.

Docs uses the Markdig Markdown engine. You can test the rendering of Markdown in Markdig vs. other engines at [https://babelmark.github.io/](https://babelmark.github.io/).

## Alerts (Note, Tip, Important, Caution, Warning)

Alerts are a Docs Markdown extension to create block quotes that render on docs.microsoft.com with colors and icons that indicate the significance of the content. The following alert types are supported:

```markdown
> [!NOTE]
> Information the user should notice even if skimming.

> [!TIP]
> Optional information to help a user be more successful.

> [!IMPORTANT]
> Essential information required for user success.

> [!CAUTION]
> Negative potential consequences of an action.

> [!WARNING]
> Dangerous certain consequences of an action.
```

These alerts look like this on docs.microsoft.com:

> [!NOTE]
> Information the user should notice even if skimming.

> [!TIP]
> Optional information to help a user be more successful.

> [!IMPORTANT]
> Essential information required for user success.

> [!CAUTION]
> Negative potential consequences of an action.

> [!WARNING]
> Dangerous certain consequences of an action.

## Code snippets

You can embed code snippets in your Markdown files:

```markdown
[!code-<language>[<name>](<codepath><queryoption><queryoptionvalue> "<title>")]
```

## Headings

Docs supports six levels of Markdown headings:

```markdown
# This is a first level heading (H1)

## This is a second level heading (H2)

...

###### This is a sixth level heading (H6)
```

- There must be a space between the last `#` and heading text.
- Each Markdown file must have one and only one H1.
- The H1 must be the first content in the file after the YML metadata block.
- H2s automatically appear in the right-hand navigating menu of the published file. Lower-level headings do not, so use H2s strategically to help readers navigate your content.
- HMTL headings, such as `<h1>`, are not recommended and in some cases will cause build warnings.
- You can link to individual headings in a file via [bookmarks](#bookmark-links).

## HTML

Although Markdown supports inline HTML, HTML is not recommended for publishing to Docs, and except for a limited list of values will cause build errors or warnings.

## Images

The syntax to include an image is:

```markdown
![[alt text]](<folderPath>)

Example:
![alt text for image](../images/Introduction.png)
```

Where `alt text` is a brief description of the image and `<folder path>` is a relative path to the image. Alternate text is required for screen readers for the visually impaired. It is also useful if there is a site bug where the image cannot render.

Images should be stored in a `/media` folder within your doc set. The following file types are supported by default for images:

- .jpg
- .png

You can add support for other image types by adding them as resources to the docfx.json file<!--add link to reference when available--> for your doc set.

## Links

In most cases, Docs uses standard Markdown links to other files and pages. The types of links are described in subsections below.

> [!TIP]
> The Docs Authoring Pack for VS Code can help insert relative links and bookmarks correctly without the tedium of figuring out the paths!

> [!IMPORTANT]
> Do not include locale codes, such as en-us, in your links to Microsoft sites. Hard-coded locale codes prevent localized content from rendering, which is a bad customer experience for users in other locales and incurs significant localization costs. When you copy a URL from a browser, the locale code is included by default, so you need to manually delete it when you create your link. For example, use:
>
> `[Microsoft](https://www.microsoft.com)`
>
> Not:
>
> `[Microsoft](https://www.microsoft.com/en-us/)`

### Relative links to files in the same doc set

A relative path is the path to the target file relative to the current file. In Docs, you can use a relative path to link to another file within the same doc set. The syntax for a relative path is as follows:

```markdown
[link text](../../folder/filename.md)
```

Where `../` indicates one level above in the hierarchy.

- The relative path will be resolved during the build, including removal of the .md extension.
- You can use "../" to link to a file in the parent folder, but that file has to be in the same doc set. You cannot use "../" to link to a file in another doc set folder.
- Docs also supports a special form of relative path that starts with "~" (for example, ~/foo/bar.md). This syntax indicates a file relative to the root folder of a doc set. This kind of path is also validated and resolved during the build.

> [!IMPORTANT]
> Include the file extension in the relative path. Build validates the existence of the target file of that relative path. If relative path does not include file extension, it is likely build will report a warning of broken link. For example, use:
>
> `[link text](../../folder/filename.md)`
>
> Not:
>
> `[link text](../../folder/filename)`

### Site relative links to other files on Docs

```markdown
[Azure and Linux](/articles/virtual-machines/linux/overview)
```

Do not include the file extension (.md). This links to the Linux overview file from outside the Azure "articles" doc set.

### Links to external sites

```markdown
[Microsoft](https://www.microsoft.com)
```

URL-based link to another web page (must include https://).

### Bookmark links

Bookmark link to a heading in another file in the same repo:

```markdown
[Managed Disks](../../linux/overview.md#managed-disks)
```

Bookmark link to a heading in the current file:

```markdown
[Managed Disks](#managed-disks)
```

Use a hash tag followed by the words of the heading with punctuation removed and spaces replaced with dashes.

### Explicit anchor links

Explicit anchor links using the `<a>` HTML tag are **not required or recommended** except in hub and landing pages. Use bookmarks as described above in general Markdown files. For hub and landing pages, use anchors as follows:

`## <a id="AnchorText"> </a>Header text` or `## <a name="AnchorText"> </a>Header text`

To link to explicit anchors, use the following syntax:

```markdown
To go to a section on the same page:
[text](#AnchorText)

To go to a section on another page.
[text](FileName.md#AnchorText)
```

### XREF (cross reference) links

To link to auto-generated API references pages in the current doc set or other doc sets, use XREF links with the unique ID (UID).

> [!NOTE]
> To reference API reference pages in other doc sets, you need to add `xrefService` configuration in `docfx.json` file.
> ```
> "build": {
>   ...
>   "xrefService": [ "https://xref.docs.microsoft.com/query?uid={uid}" ]
> }
> ```

The UID equates to the fully qualified class and member name. If you add a * after the UID, the link then represents the overload page and not a specific API. For example, use `List<T>.BinarySearch*` to link to the BinarySearch Method page instead of linking to a specific overload such as `List<T>.BinarySearch(T, IComparer<T>)`.

You can use one of the following syntaxes:

- Auto-link: `<xref:UID> or <xref:UID?displayProperty=nameWithType>`

  The optional `displayProperty` query parameter produces a fully qualified link text. By default, link text shows only the member or type name.

- Markdown link: `[link text](xref:UID)`
  
  Use when you want to customize the link text displayed.

Examples:

- `<xref:System.String>` renders as "String".
- `<xref:System.String?displayProperty=nameWithType>` renders as "System.String".
- `[String class](xref:System.String)` renders as "String class".

Right now, there is no easy way to find the UIDs. <!-- ? -->The best way to find the UID for an API is to view the source for the API page you want to link to and find the ms.assetid value. Individual overload values are not shown in the source. We're working on having a better system in the future.

When the UID contains the special characters \`, \#, or \*, the UID value needs to be HTML encoded as `%60`, `%23`, and `%2A`, respectively. You'll sometimes see parentheses encoded but it's not a requirement.

Examples:

- System.Threading.Tasks.Task\`1 becomes `System.Threading.Tasks.Task%601`
- System.Exception.\#ctor becomes `System.Exception.%23ctor`
- System.Lazy\`1.\#ctor(System.Threading.LazyThreadSafetyMode) becomes  `System.Lazy%601.%23ctor%28System.Threading.LazyThreadSafetyMode%29`

<!-- leave out of Contributor Guide for now
Using XREF may require some configuration. For more information, see XREF Service.
-->

## Lists (Numbered, Bulleted, Checklist)

### Numbered list

To create a numbered list, you can use all 1s, which are rendered as a sequential list when published. For increased source readability, you can increment your lists.

Do not use letters in lists, including nested lists. They do not render correctly when published to Docs. Nested lists using numbers will render as lowercase letters when published. For example:

```markdown
1. This is
1. a parent numbered list
   1. and this is
   1. a nested numbered list
1. (fin)
```

This renders as follows:

1. This is
1. a parent numbered list
   1. and this is
   1. a nested numbered list
1. (fin)

### Bulleted list

To create a bulleted list, use `-` followed by a space at the beginning of each line:

```markdown
- This is
- a parent bulleted list
  - and this is
  - a nested bulleted list
- All done!
```

This renders as follows:

- This is
- a parent bulleted list
  - and this is
  - a nested bulleted list
- All done!

### Checklist

Checklists are available for use on docs.microsoft.com (only) via a custom Markdown extension:

```markdown
> [!div class="checklist"]
> * List item 1
> * List item 2
> * List item 3
```

This example renders on docs.microsoft.com like this:

> [!div class="checklist"]
> * List item 1
> * List item 2
> * List item 3

Use checklists at the beginning or end of an article to summarize "What will you learn" or "What have you learned" content. Do not add random checklists throughout your articles.
<!-- is this guidance still accurate? -->

## Next step action

You can use a custom extension to add a next step action button to pages on docs.microsoft.com (only).

The syntax is as follows:

```markdown
> [!div class="nextstepaction"]
> [button text](link to topic)
```

For example:

```markdown
> [!div class="nextstepaction"]
> [Learn about basic style](style-quick-start.md)
```

This renders as follows:

> [!div class="nextstepaction"]
> [Learn about basic style](style-quick-start.md)

You can use any supported link in a next step action, including a Markdown link to another web page. In most cases, the next action link will be a relative link to another file in the same doc set.

## Section definition

<!-- more info about this would be helpful! -->
You might need to define a section. This syntax is mostly used for code tables.
See the following example:

````
> [!div class="tabbedCodeSnippets" data-resources="OutlookServices.Calendar"]
> ```cs
> <cs code text>
> ```
> ```javascript
> <js code text>
> ```
````

The preceding blockquote Markdown text will be rendered as:
> [!div class="tabbedCodeSnippets" data-resources="OutlookServices.Calendar"]
> ```cs
> <cs code text>
> ```
> ```javascript
> <js code text>
> ```

## Selectors

<!-- could be more clear! -->
You can use a selector when you want to connect different pages for the same article. Readers can then switch between those pages.

> [!NOTE]
> This extension works differently between docs.microsoft.com and MSDN. <!-- should we keep info about MSDN? If so say how they differ?-->

### Single selector

```
> [!div class="op_single_selector"]
> - [Universal Windows](how-to-write-use-markdown.md)
> - [Windows Phone](how-to-write-use-markdown.md)
> - [iOS](how-to-write-use-markdown.md)
> - [Android](how-to-write-use-markdown.md)
> - [Kindle](how-to-write-use-markdown.md)
> - [Baidu](how-to-write-use-markdown.md)
> - [Xamarin.iOS](how-to-write-use-markdown.md)
> - [Xamarin.Android](how-to-write-use-markdown.md)
```

... will be rendered like this:

> [!div class="op_single_selector"]
> - [Universal Windows](how-to-write-use-markdown.md)
> - [Windows Phone](how-to-write-use-markdown.md)
> - [iOS](how-to-write-use-markdown.md)
> - [Android](how-to-write-use-markdown.md)
> - [Kindle](how-to-write-use-markdown.md)
> - [Baidu](how-to-write-use-markdown.md)
> - [Xamarin.iOS](how-to-write-use-markdown.md)
> - [Xamarin.Android](how-to-write-use-markdown.md)

### Multi-selector

```
> [!div class="op_multi_selector" title1="Platform" title2="Backend"]
> - [(iOS | .NET)](how-to-write-workflows-major.md)
> - [(iOS | JavaScript)](how-to-write-workflows-major.md)
> - [(Windows universal C# | .NET)](how-to-write-workflows-major.md)
> - [(Windows universal C# | Javascript)](how-to-write-workflows-major.md)
> - [(Windows Phone | .NET)](how-to-write-workflows-major.md)
> - [(Windows Phone | Javascript)](how-to-write-workflows-major.md)
> - [(Android | .NET)](how-to-write-workflows-major.md)
> - [(Android | Javascript)](how-to-write-workflows-major.md)
> - [(Xamarin iOS | Javascript)](how-to-write-workflows-major.md)
> - [(Xamarin Android | Javascript)](how-to-write-workflows-major.md)
```

... will be rendered like this:

> [!div class="op_multi_selector" title1="Platform" title2="Backend"]
> - [(iOS | .NET)](how-to-write-workflows-major.md)
> - [(iOS | JavaScript)](how-to-write-workflows-major.md)
> - [(Windows universal C# | .NET)](how-to-write-workflows-major.md)
> - [(Windows universal C# | Javascript)](how-to-write-workflows-major.md)
> - [(Windows Phone | .NET)](how-to-write-workflows-major.md)
> - [(Windows Phone | Javascript)](how-to-write-workflows-major.md)
> - [(Android | .NET)](how-to-write-workflows-major.md)
> - [(Android | Javascript)](how-to-write-workflows-major.md)
> - [(Xamarin iOS | Javascript)](how-to-write-workflows-major.md)
> - [(Xamarin Android | Javascript)](how-to-write-workflows-major.md)

## Tables

The simplest way to create a table in Markdown is to use pipes and lines. To create a standard table with a header, follow the first line with dashed line:

```markdown
|This is   |a simple   |table header|
|----------|-----------|------------|
|table     |data       |here        |
|it doesn't|actually   |have to line up nicely!|
```

This renders as follows:

|This is   |a simple   |table header|
|----------|-----------|------------|
|table     |data       |here        |
|it doesn't|actually   |have to line up nicely!||

You can also create a table without a header. For example, to create a multiple-column list:

```markdown
|   |   |
| - | - |
| This | table |
| has no | header |
```

This renders like this:

|   |   |
| - | - |
| This | table |
| has no | header |

You can align the columns by using colons:

```markdown
|                  |
|------------------|
|    right aligned:|
|:left aligned     |
|:centered        :|
```

Renders as follows:

|                  |
|------------------|
|    right aligned:|
|:left aligned     |
|:centered        :|

> [!TIP]
> The Docs Authoring Extension for VS Code makes it easy to add basic Markdown tables!
>
> You can also use an [online table generator](http://www.tablesgenerator.com/markdown_tables).

### mx-tdBreakAll

> [!IMPORTANT]
> This only works on the docs.microsoft.com site.

If you create a table in Markdown, the table might expand to the right navigation and become unreadable. You can solve that by allowing Docs rendering to break the table when needed. Just wrap up the table with the custom class `[!div class="mx-tdBreakAll"]`.

Here is a Markdown sample of a table with three rows that will be wrapped by a `div` with the class name `mx-tdBreakAll`.

```markdown
> [!div class="mx-tdBreakAll"]
> |Name|Syntax|Mandatory for silent installation?|Description|
> |-------------|----------|---------|---------|
> |Quiet|/quiet|Yes|Runs the installer, displaying no UI and no prompts.|
> |NoRestart|/norestart|No|Suppresses any attempts to restart. By default, the UI will prompt before restart.|
> |Help|/help|No|Provides help and quick reference. Displays the correct use of the setup command, including a list of all options and behaviors.|
```

It will be rendered like this:

> [!div class="mx-tdBreakAll"]
> |Name|Syntax|Mandatory for silent installation?|Description|
> |-------------|----------|---------|---------|
> |Quiet|/quiet|Yes|Runs the installer, displaying no UI and no prompts.|
> |NoRestart|/norestart|No|Suppresses any attempts to restart. By default, the UI will prompt before restart.|
> |Help|/help|No|Provides help and quick reference. Displays the correct use of the setup command, including a list of all options and behaviors.|

### mx-tdCol2BreakAll

> [!IMPORTANT]
> This only works on the docs.microsoft.com site.

From time to time, you might have very long words in the second column of a table. To ensure they are broken apart nicely, you can apply the class `mx-tdCol2BreakAll` by using the `div` wrapper syntax as shown earlier.

### HTML Tables

HTML tables are not recommended for docs.microsoft.com. They are not human readable in the source - which is a key principle of Markdown.

<!--If you use HTML tables and your Markdown is not being rendered between the two tables, you need to add a closing `br` tag after the closing `table` tag.

![break HTML tables](media/break-tables.png)
-->

## Videos

### Embedding videos into a Markdown page

Currently, Docs can support videos published to one of three locations:

- YouTube
- Channel 9
- Microsoft's own 'One Player' system

You can embed a video with the following syntax, and Docs will render it.

```markdown
> [!VIDEO <embedded_video_link>]
```

Example:

```markdown
> [!VIDEO https://channel9.msdn.com/Series/Youve-Got-Key-Values-A-Redis-Jump-Start/03/player]

> [!VIDEO https://www.youtube.com/embed/iAtwVM-Z7rY]

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS]
```

... will be rendered as:

```html
<iframe src="https://channel9.msdn.com/Series/Youve-Got-Key-Values-A-Redis-Jump-Start/03/player" width="640" height="320" allowFullScreen="true" frameBorder="0"></iframe>

<iframe src="https://www.youtube-nocookie.com/embed/iAtwVM-Z7rY" width="640" height="320" allowFullScreen="true" frameBorder="0"></iframe>
<iframe src="https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS" width="640" height="320" allowFullScreen="true" frameBorder="0"></iframe>
```

And it will be displayed like this on published pages:

> [!VIDEO https://channel9.msdn.com/Series/Youve-Got-Key-Values-A-Redis-Jump-Start/03/player]

> [!VIDEO https://www.youtube.com/embed/iAtwVM-Z7rY]

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS]

> [!IMPORTANT]
> The CH9 video URL should start with `https` and end with `/player`. Otherwise, it will embed the whole page instead of the video only.

### Uploading new videos

Any new videos should be uploaded using the following process:

1. Join the **docs_video_users** group on IDWEB.
1. Go to https://aka.ms/VideoUploadRequest and fill in the details for your video. You will need (note that none of these items will be visible to the public):
    1. A title for your video.
    1. A list of products/services that your video is related to.
    1. The target page or (if you don’t have the page yet) doc set that your video will be hosted on.
    1. A link to the MP4 file for your video (if you don’t have a location to put the file, you can put it here temporarily:   `\\scratch2\scratch\apex`). MP4 files should be 720p or higher.
    1. A description of the video.
1. Submit (save) that item.
1. Within two business days, the video will get uploaded. The link you need for embedding will be placed into the work item, and it will be resolved *back to you*.
1. Once you have grabbed the video link, close the work item.
1. The video link can then be added to your post, using this syntax:

   ```markdown
   > [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS]
   ```
