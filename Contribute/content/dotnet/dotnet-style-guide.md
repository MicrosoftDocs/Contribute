---
title: Template and cheatsheet for .NET articles
description: This article contains a handy template you can use to create new articles for the .NET docs repositories
ms.topic: contributor-guide
ms.service: learn
ms.custom: external-contributor-guide
ms.date: 11/07/2018
---
# Metadata and Markdown template for .NET docs

This dotnet/docs template contains examples of Markdown syntax and guidance on setting the metadata.

When creating a Markdown file, copy the included template to a new file, fill out the metadata as specified below, and set the H1 heading above to the title of the article.

## Metadata

The required metadata block is in the following sample metadata block:

```markdown
---
title: [ARTICLE TITLE]
description: [usually a summary of your first paragraph. It gets displayed in search results, and can help drive the correct traffic if well written.]
author: [GITHUB USERNAME]
ms.date: [CREATION/UPDATE DATE - mm/dd/yyyy]
---
# The H1 should not be the same as the title, but should describe the article contents
```

- You **must** have a space between the colon (:) and the value for a metadata element.
- Colons in a value (for example, a title) break the metadata parser. In this case, surround the title with double quotes (for example, `title: "Writing .NET Core console apps: An advanced step-by-step guide"`).
- **title**: Appears in search engine results. The title shouldn't be identical to the title in your H1 heading, and it should contain 60 characters or less.
- **description**: Summarizes the content of the article. It's usually shown in the search results page, but it isn't used for search ranking. Its length should be 115-145 characters including spaces.
- **author**: The author field should contain the **GitHub username** of the author.
- **ms.date**: The date of the last significant update. Update this on existing articles if you reviewed and updated the entire article. Small fixes, such as typos or similar do not warrant an update.

Other metadata is attached to each article, but we typically apply most metadata values at the folder level, specified in **docfx.json**.

## Basic Markdown, GFM, and special characters

You can learn the basics of Markdown, GitHub Flavored Markdown (GFM), and OPS-specific extensions in the [Markdown reference](../markdown-reference.md) article.

Markdown uses special characters such as \*, \`, and \# for formatting. If you wish to include one of these characters in your content, you must do one of two things:

- Put a backslash before the special character to "escape" it (for example, `\*` for a \*).
- Use the [HTML entity code](http://www.ascii.cl/htmlcodes.htm) for the character (for example, `&#42;` for a &#42;).

## File names

File names use the following rules:

* Contain only lowercase letters, numbers, and hyphens.
* No spaces or punctuation characters. Use the hyphens to separate words and numbers in the file name.
* Use action verbs that are specific, such as develop, buy, build, troubleshoot. No -ing words.
* No small words - don't include a, and, the, in, or, etc.
* Must be in Markdown and use the .md file extension.
* Keep file names reasonably short. They are part of the URL for your articles.

## Headings

Use sentence-style capitalization. Always capitalize the first word of a heading.

## Text styling

*Italics*\
Use for files, folders, paths (for long items, split onto their own line), new terms.

**Bold**\
Use for UI elements.

`Code`\
Use for inline code, language keywords, NuGet package names, command-line commands, database table and column names, and URLs that you don't want to be clickable.

## Links

See the general article on [Links](../how-to-write-links.md) for information about anchors, internal links, links to other documents, code includes, and external links.

The .NET docs team uses the following conventions:

- In most cases, we use the relative links and discourage the use of `~/` in links because relative links resolve in the source on GitHub. However, whenever we link to a file in a dependent repo, we use the `~/` character to provide the path. Because the files in the dependent repo are in a different location in GitHub the links won't resolve correctly with relative links regardless of how they were written.
- The C# language specification and the Visual Basic language specification are included in the .NET docs by including the source from the language repositories. The markdown sources are managed in the [csharplang](https://github.com/dotnet/csharplang) and [vblang](https://github.com/dotnet/vblang) repositories.

Links to the spec must point to the source directories where those specs are included. For C#, it's **~/_csharplang/spec** and for VB, it's **~/_vblang/spec**, as in the following example:

```markdown
[C# Query Expressions](~/_csharplang/spec/expressions.md#query-expressions)
```

### Links to APIs

The build system has some extensions that allow us to link to .NET APIs without having to use external links. You use one of the following syntax:

1. Auto-link: `<xref:UID>` or `<xref:UID?displayProperty=nameWithType>`

   The `displayProperty` query parameter produces a fully qualified link text. By default, link text shows only the member or type name.

2. Markdown link: `[link text](xref:UID)`

   Use when you want to customize the link text displayed.

Examples:

- `<xref:System.String>` renders as [String](/dotnet/api/system.string)
- `<xref:System.String?displayProperty=nameWithType>` renders as [System.String](/dotnet/api/system.string)
- `[String class](xref:System.String)` renders as [String class](/dotnet/api/system.string)

For more information about using this notation, see [Using cross reference](https://dotnet.github.io/docfx/tutorial/links_and_cross_references.html#using-cross-reference).

Some UIDs contain the special characters \`, \# or \*, the UID value needs to be HTML encoded as `%60`, `%23` and `%2A` respectively. You'll sometimes see parentheses encoded but it's not a requirement.

Examples:

- System.Threading.Tasks.Task\`1 becomes `System.Threading.Tasks.Task%601`
- System.Exception.\#ctor becomes `System.Exception.%23ctor`
- System.Lazy\`1.\#ctor(System.Threading.LazyThreadSafetyMode) becomes  `System.Lazy%601.%23ctor%28System.Threading.LazyThreadSafetyMode%29`

You can find the UIDs of types, a member overload list, or a particular overloaded member from `https://xref.learn.microsoft.com/autocomplete`. The query string `?text=*\<type-member-name>*` identifies the type or member whose UIDs you'd like to see. For example, `https://xref.learn.microsoft.com/autocomplete?text=string.format` retrieves the [String.Format](/dotnet/api/system.string.format) overloads. The tool searches for the provided `text` query parameter in any part of the UID. For example, you can search for member name (ToString), partial member name (ToStri), type and member name (Double.ToString), etc.

If you add a \* (or `%2A`) after the UID, the link then represents the overload page and not a specific API. For example, you can use that when you want to link to the [List\<T>.BinarySearch Method](/dotnet/api/system.collections.generic.list-1.binarysearch) page in a generic way instead of a specific overload such as [List\<T>.BinarySearch(T, IComparer\<T>)](/dotnet/api/system.collections.generic.list-1.binarysearch#System_Collections_Generic_List_1_BinarySearch__0_). You can also use \* to link to a member page when the member is not overloaded; this saves you from having to include the parameter list in the UID.

To link to a specific method overload, you must include the fully qualified type name of each of the method's parameters. For example, \<xref:System.DateTime.ToString> links to the parameterless [DateTime.ToString](/dotnet/api/system.datetime.tostring#System_DateTime_ToString) method, while \<xref:System.DateTime.ToString(System.String,System.IFormatProvider)> links to the  [DateTime.ToString(String,IFormatProvider)](/dotnet/api/system.datetime.tostring#System_DateTime_ToString_System_String_System_IFormatProvider_) method.

To link to a generic type, such as [System.Collections.Generic.List\<T>](/dotnet/api/system.collections.generic.list-1), you use the \` (`%60`) character followed by the number of generic type parameters. For example, `<xref:System.Nullable%601>` links to the [System.Nullable\<T>](/dotnet/api/system.nullable-1) type, while `<xref:System.Func%602>` links to the [System.Func\<T,TResult>](/dotnet/api/system.func-2) delegate.

## Code

The best way to include code is to include snippets from a working sample. Create your sample following the instructions in the [contributing to .NET](dotnet-contribute.md#contribute-to-samples) article. Including snippets from full programs ensures that all code runs through our Continuous Integration (CI)
system. However, if you need to show something that causes compile time or
runtime errors, you can use inline code blocks.

For information about the Markdown syntax for showing code in docs, see [How to include code in docs](../code-in-docs.md).

## Images

### Static image or animated GIF

```markdown
![this is the alt text](../images/Logo_DotNet.png)
```

### Linked image

```markdown
[![alt text for linked image](../images/Logo_DotNet.png)](https://dot.net)
```

## Videos

You can embed YouTube videos in a Markdown file. To get the video's correct URL, right-click on the video, select **Copy Embed Code**, and copy the URL from the `<iframe>` element.

```markdown
> [!VIDEO <youtube_video_link>]
```

For example:

```markdown
> [!VIDEO https://www.youtube.com/embed/Q2mMbjw6cLA]
```

## learn.microsoft extensions

learn.microsoft provides a few additional extensions to GitHub Flavored Markdown.

### Checked lists

A custom style is available for lists. You can render lists with green check marks.

```markdown
> [!div class="checklist"]
> * How to create a .NET Core app
> * How to add a reference to the Microsoft.XmlSerializer.Generator package
> * How to edit your MyApp.csproj to add dependencies
> * How to add a class and an XmlSerializer
> * How to build and run the application
```

This renders as:

> [!div class="checklist"]
> * How to create a .NET Core app
> * How to add a reference to the Microsoft.XmlSerializer.Generator package
> * How to edit your MyApp.csproj to add dependencies
> * How to add a class and an XmlSerializer
> * How to build and run the application

You can see an example of checked lists in action in the [.NET Core docs](/dotnet/core/additional-tools/xml-serializer-generator).

### Buttons

Button links:

```markdown
> [!div class="button"]
> [button links](dotnet-contribute.md)
```

This renders as:

> [!div class="button"]
> [button links](dotnet-contribute.md)

You can see an example of buttons in action in the [Visual Studio docs](/visualstudio/install/install-visual-studio#step-2---download-visual-studio).

### Step-by-steps

```markdown
>[!div class="step-by-step"]
> [Pre](../docs/csharp/expression-trees-interpreting.md)
> [Next](../docs/csharp/expression-trees-translating.md)
```

You can see an example of step-by-steps in action at the [C# Guide](/dotnet/csharp/tour-of-csharp/program-structure).
