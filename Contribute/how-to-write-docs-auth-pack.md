---
title: Docs Authoring Pack for VS Code
description: This article describes the VS Code extension pack to facilitate Markdown authoring for docs.microsoft.com.
author: meganbradley
ms.author: mbradley
manager: jemash
ms.date: 04/06/2018
---
# Docs Authoring Pack for VS Code

The Docs Authoring Pack is a collection of VS Code extensions to aid with Markdown authoring for docs.microsoft.com. The pack is [available in the VS Code Marketplace](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack) and contains the following extensions:

- [markdownlint](https://marketplace.visualstudio.com/items?itemName=DavidAnson.vscode-markdownlint): A popular Markdown linter by David Anson to help ensure your Markdown follows best practices.
- [Code Spell Checker](https://marketplace.visualstudio.com/items?itemName=streetsidesoftware.code-spell-checker): A fully offline spell checker by Street Side Software.
- [Docs Preview](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-preview): Uses the docs.microsoft.com CSS for more accurate Markdown preview, including custom Markdown.
- [Docs Markdown](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown): Provides Markdown authoring assistance for docs.microsoft.com content in the Open Publishing System (OPS), including basic Markdown support and support for custom Markdown syntax in OPS. The rest of this topic describes the Docs Markdown extension.
- [Docs Article Templates](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-article-templates): Allows users to apply Markdown skeleton content to new files.

## Prerequisites and assumptions

To accurately insert relative links, images, and other embedded content with the Docs Markdown extension, you must have your VS Code workspace scoped to the root of your cloned Open Publishing System (OPS) repo.

Some syntax supported by the extension, such as alerts and snippets, are custom Markdown for OPS, and will not render correctly unless published via OPS.

## How to use the Docs Markdown extension

To access the Docs Markdown menu, type `ALT+M`. You can click or use up/down arrows to select the function you want, or type to start filtering, then hit `ENTER` when the function you want is highlighted in the menu. The following are available:

|Function     |Description           |
|-------------|----------------------|
|Preview      |Preview the active topic in a side-by-side window using the Docs Preview extension. This option is only available if Docs Preview is installed.|
|Bold         |Formats text **bold**.|
|Italic       |Formats text *italic*.|
|Code         |If one line or less is selected, formats text as `inline code`.<br><br>If multiple lines are selected, formats them as a fenced code block, and allows you to optionally select a programming language supported by OPS.|
|Alert        |Inserts a Note, Important, Warning, or Tip.<br><br>Select Alert from the menu, then select the alert type. If you have previously selected text, it will be surrounded with the selected alert syntax. If no text is selected, a new alert will be added with placeholder text.|
|Numbered list|Inserts a new numbered list.<br><br> If multiple lines are selected, each will be a list item. Note that numbered lists show in the Markdown as all 1s, but will render on docs.microsoft.com as sequential numbers or, for nested lists, letters. To create a nested numbered list, tab from within the parent list.|
|Bulleted list|Inserts a new bulleted list.|
|Table        |Inserts a Markdown table structure.<br><br>After you select the table command, specify the number of columns and rows in the format columns:rows, such as 3:4. Note that the maximum number of columns you can specify via this extension is 5, which is the recommended maximum for readability.|
|Link to file in repo|Inserts a relative link to another file in the current repo. After selecting this option, type in the command window to filter files by name, then select the file you want. If you have previously selected text, it will become the link text. Otherwise, the H1 of the target file will be used as link text.|
|Link to web page    |Inserts a link to a web page. After selecting this option, paste or type the URI into the command window. `https://` is required. If you have previously selected text, it will become the link text. Otherwise, the URI will be used as link text.|
|Link to heading     |Links to a bookmark in the current file or another file in the repo.<br>`Bookmark in this file`: Choose from a list of headings in the current file to insert a properly formatted bookmark.<br>`Bookmark in another file`: First, filter by file name and select the file to link to, then choose the appropriate heading within the selected file.|
|Image        |Type alternate text (required for accessibility) and select it, then call this command to filter the list of supported image files in the repo and select the one you want. If you haven't selected alt text when you call this command, you will be prompted for it before you can select an image file.|
|Include      |Find a file to embed in the current file.|
|Snippet      |Find a code snippet in the repo to embed in the current file.|
|Video        |Add an embedded video.|
|Template     |Create a new file and apply a Markdown template. See [Templates](#how-to-use-docs-templates), below, for more information.|

## How to assign keyboard shortcuts

1. Type `CTRL+K` then `CTRL+S` to open the Keyboard Shortcuts list.
1. Search for the command, such as `formatBold`, for which you want to create a custom keybinding.
1. Click the plus that appears near the command name when you mouse over the line.
1. After a new input box is visible, type the keyboard shortcut you want to bind to that particular command. For example, to use the common shortcut for bold, type `ctrl+b`.
1. It's a good idea to insert a `when` clause into your keybinding, so it won't be available in files other than Markdown. To do this, open *keybindings.json* and insert the following line below the command name (be sure to add a comma between lines):
   
    `"when": "editorTextFocus && editorLangId == 'markdown'"`

    Your completed custom keybinding should look like this in keybindings.json:

    ```json
    // Place your key bindings in this file to overwrite the defaults
    [
        {
            "key": "ctrl+b",
            "command": "formatBold",
            "when": "editorTextFocus && editorLangId == 'markdown'"
        }
    ]
    ```

1. Save keybindings.json.

See [Keybindings](https://code.visualstudio.com/docs/getstarted/keybindings) in the VS Code docs for more information.

## How to show the legacy toolbar

Users of the pre-release version of the extension will notice that the authoring toolbar no longer appears at the bottom of the VS Code window when the Docs Markdown Extension is installed. This is because the toolbar took up a lot of space on the VS Code status bar and did not follow best practices for extension UX, so it is deprecated in the new extension. However, you can optionally show the toolbar by updating your VS Code settings.json file as follows:

1. In VS Code, go to File -> Preferences -> Settings (`CTRL+Comma`).
1. Select User Settings to change the settings for all VS Code workspaces, or  Workspace Settings to change them for just the current workspace.
1. In the Default Settings pane, find Docs Authoring Extension Configuration, and select the pencil icon next to the desired setting. Next, you will be prompted to select either `true` or `false`. Once you've made your selection, VS Code will automatically add the value to the settings.json file and you will be prompted to reload the window for the changes to take effect.

## How to use Docs templates

The Docs Article Templates extension lets writers in VS Code pull a Markdown template from a centralized store and apply it to a file. Templates can help ensure that required metadata is included in articles, that content standards are followed, and so on. Templates are managed as Markdown files in a public GitHub repository.

### To apply a template in VS Code

1. Ensure the Docs Article Templates extension is installed and enabled.
1. If you don't have the Docs Markdown extension installed, hit F1 to open the command palette, start typing "template" to filter, then click `Docs: Template`. If you do have Docs Markdown installed, you can use either the command palette or click `Alt+M` to bring up the Docs Markdown QuickPick menu, then select `Template` from the list.
1. Select the desired template from the list that appears.

### To add your GitHub ID and/or Microsoft alias to your VS Code settings

The Templates extension supports three dynamic metadata fields: author, ms.author, and ms.date. That means that if a template creator uses these fields in the metadata header of a Markdown template, they will be auto-populated in your file when you apply the template, as follows:

|Field     |Value|
|----------|-----|
|author    |Your GitHub alias, if specified in your VS Code settings file.|
|ms.author |Your Microsoft alias, if specified in your VS Code settings file. If you are not a Microsoft employee, leave this unspecified.|
|ms.date   |The current date in the Docs-supported format, MM/DD/YYYY. Note that the date is not automatically updated if you subsequently update the file - you must update this manually to indicate the article freshness date.|

### To set author and/or ms.author

1. In VS Code, go to File -> Preferences -> Settings (`CTRL+Comma`).
1. Select User Settings to change the settings for all VS Code workspaces, or Workspace Settings to change them for just the current workspace.
1. In the Default Settings pane on the left, find Docs Article Templates Extension Configuration, click the pencil icon next to the desired setting, then click Replace in Settings.
1. The User Settings pane will open side-by-side, with a new entry at the bottom.
1. Add your GitHub ID or Microsoft email alias, as appropriate, and save the file.
1. You might need to close and restart VS Code for the changes to take effect.
1. Now, when you apply a template that uses dynamic fields, your GitHub ID and/or Microsoft alias will be auto-populated in the metadata header.
