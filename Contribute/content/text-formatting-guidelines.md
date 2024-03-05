---
title: Text formatting guidelines
description: Learn when to use bold, italics, code, and other text styles in articles published on Microsoft Learn.
author: tdykstra
ms.author: tdykstra
ms.date: 11/09/2021
ms.service: learn
ms.topic: contributor-guide
ms.custom: external-contributor-guide
---

# Text formatting guidelines

Consistent and appropriate use of bold, italic, and code style for text elements improves
readability and helps avoid misunderstandings.

## Bold

Use bold for UI elements, such as menu selections, dialog box names, and input field names.

### Examples

* **This**: In **Solution Explorer**, right-click the project node, and then select **Add > New Item**.
* **Not this**: In Solution Explorer, right-click the project node, and then select Add > New Item.
* **Not this**: In *Solution Explorer*, right-click the project node, and then select *Add > New Item*.

## Italics

Use italics for:

* Introducing new terms along with a definition or explanation.
* File names, folder names, paths.
* User input.

### Examples

* **This**: In App Service, an app runs in an *App Service plan*. An App Service plan defines a set of compute resources for a web app to run on.
* **Not this**: In App Service, an app runs in an "App Service plan." An App Service plan defines a set of compute resources for a web app to run on.
* **This**: Replace the code in *HttpTriggerCSharp.cs* with the following code.
* **Not this**: Replace the code in `HttpTriggerCSharp.cs` with the following code.
* **This**: Enter *ContosoUniversity* for the **Name**, and then select **Add**.
* **Not this**: Enter "ContosoUniversity" for the **Name**, and then select **Add**.

## Code style

Use code style for:

* Code elements, such as method names, property names, and language keywords.
* SQL commands
* NuGet package names
* Command-line commands\*
* Database table and column names
* Resource names that should not be localized (such as virtual machine names)
* URLs that you don't want to be clickable

**Why?** Older style guides specify bold for many of these text elements. However, most articles are
localized, and code style tells the translator to leave that part of the text untranslated.

Code style can be *inline* (surrounded by \`) or *fenced* code blocks (surrounded by \`\`\`) that
span multiple lines. Put longer code snippets and paths in fenced code blocks.

\* In command-line commands, use forward slashes in file paths if they're supported on all platforms. Use backslashes to illustrate commands that run on Windows, when only backslashes are supported. For example, forward slashes work on the .NET CLI on all platforms, so you would use `dotnet build foldername/filename.csproj` rather than `dotnet build foldername\filename.csproj`.

### Examples using inline styles

* **This**: By default, the Entity Framework interprets a property that's named `Id` or `ClassnameID` as the primary key.
* **Not this**: By default, the Entity Framework interprets a property that's named *Id* or *ClassnameID* as the primary key.
* **This**: The `Microsoft.EntityFrameworkCore` package provides runtime support for EF Core.
* **Not this**: The *Microsoft.EntityFrameworkCore* package provides runtime support for EF Core.

### Examples of fenced code blocks

* **This**: No commands are sent to the database by statements that just change an `IQueryable`, such as the following code:

  ```markdown
      ```csharp
      var students = context.Students.Where(s => s.LastName == "Davolio")
      ```
  ```

* **Not this**: No commands are sent to the database by statements that just change an **IQueryable**, such as **var students = context.Students.Where(s => s.LastName == "Davolio")**.

* **This**: For example, to run the `Get-ServiceLog.ps1` script in the `C:\Scripts` directory, type:

  ```markdown
      ```powershell
      C:\Scripts\Get-ServiceLog.ps1
      ```
  ```

* **Not this**: For example, to run the **Get-ServiceLog.ps1** script in the **C:\Scripts** directory, type: "C:\Scripts\Get-ServiceLog.ps1."

* **All** fenced code blocks must have an approved language tag. For a list of support language tags, see [How to include code in docs](./code-in-docs.md#supported-languages).

## Placeholders

If you want the user to replace part of an input string with their own values, use placeholder text marked off by angle brackets (less than  `<` and greater than `>` characters). 

**Option 1:** Use code-styling to surround the placeholder word or the encompassing phrase. For example, you can use single backticks \` for inline-code formatting for a single phrase, or triple-ticks \`\`\` for code-fenced formatting.

```markdown
`az group delete -n <ResourceGroupName>`
```

Rendered as:
> `az group delete -n <ResourceGroupName>`

or

**Option 2:** Use a backslash character `\` to escape the angle bracket characters in Markdown, such as `\<` and `\>`. While only the first escape on the left angle bracket `\<` is required, escaping the closing bracket `\>` works too for consistency. The rendered HTML doesn't show the escape character to the reader:

```markdown
az group delete -n \<ResourceGroupName\>
```

Rendered as:
>  az group delete -n \<ResourceGroupName\>


**Inform the reader about the placeholder**: In the text preceding such placeholder examples, explain to the reader that the text in brackets must be removed and substituted with real values. We recommend the use of italics for user input. You can format italics within angle bracketed inline code:

> In the following example, replace the placeholder text *`<ResourceGroupName>`* with your own resource group name.

> [!CAUTION]
> The Microsoft Learn site does not render \<placeholder\> text that uses angle brackets in cases where the brackets are not escaped properly or the text is not code-formatted. The Microsoft Learn build process interprets the \<placeholder\> phrase as an HTML tag that could be dangerous to the reader's browser, and flags it as a *disallowed-html-tag*. You'll see a suggestion in the build report, and the placeholder word isn't rendered in the Microsoft Learn page output when that happens.
>  
> To avoid content loss on placeholders, use `code` formatting or  escape characters (`\<` `\>`)  as described previously.

We discourage using curly braces { } as syntactical placeholders. Readers can confuse curly brace placeholders with the same notation used in:

* Replaceable text
* Format strings
* String interpolation
* Text templates
* Similar programming constructs

**Casing and spacing**: You can separate placeholder names with hyphens ("kebab case") or with underscores, or you can do it by using Pascal case. Kebab case might generate syntax errors, and underscores could conflict with underlining. All-caps can conflict with named constants in many languages, though it may also draw attention to the placeholder name.

> *`<Resource-Group-Name>`* or *`<ResourceGroupName>`*

## Headings and link text

Don't apply an inline style such as italics or bold to headings or hyperlink text.

**Why?**

People rely on standard hyperlink text to identify text elements as clickable links. Styling a link
as italics, for example, can obscure the fact that the text is a link. Headings have their own styles
and mixing other styles in them looks bad.

### Examples of headings and link text

* **This**: The *function.json* file is generated by the NuGet package [Microsoft.NET.Sdk.Functions](https://www.nuget.org/packages/Microsoft.NET.Sdk.Functions).
* **Not this**: The *function.json* file is generated by the NuGet package [*Microsoft.NET.Sdk.Functions*](https://www.nuget.org/packages/Microsoft.NET.Sdk.Functions).

* **This**:

  ```markdown
  ### The Microsoft.NET.Sdk.Functions package
  ```

* **Not this**:

  ```markdown
  ### The *Microsoft.NET.Sdk.Functions* package
  ```

## Keys and keyboard shortcuts

When referring to keys or key combinations, follow these conventions:

* Capitalize the first letter of key names.
* Surround the key names with `<kbd>` and `</kbd>` HTML tags.
* Use "+" to join keys that the user selects at the same time.

### Examples of keys and keyboard shortcuts

* **This**: Select <kbd>Alt</kbd>+<kbd>Ctrl</kbd>+<kbd>S</kbd>.
* **Not this**: Press **ALT+CTRL+S**.
* **Not this**: Hit `ALT+CTRL+S`.

## Exceptions

Style guidelines aren't rigid rules. In contexts where they harm readability, do something
different. For example, an HTML table with mostly code elements might look too busy with code
styling everywhere. You might choose bold styling in that context.

If you choose an alternate text style where code is normally called for, make sure it's okay for the text
to be translated in localized versions of the article. Code is the only style that automatically
prevents translation. For scenarios where you want to prevent localization without using code style, see [Non-localized strings](markdown-reference.md#non-localized-strings).
