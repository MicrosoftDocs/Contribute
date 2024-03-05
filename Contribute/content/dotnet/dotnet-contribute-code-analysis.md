---
title: Contribute docs for .NET code analysis rules to the .NET docs repository
description: This article describes the process for contributing to the articles and code samples for .NET code analysis rules in the .NET docs repository.
author: mavasani
ms.author: mavasani
ms.topic: contributor-guide
ms.service: learn
ms.custom: external-contributor-guide
ms.date: 10/09/2020
---
# Contribute docs for .NET code analysis rules to the .NET docs repository

.NET compiler platform (Roslyn) analyzers inspect your C# or Visual Basic code for code quality and code style issues. Starting in .NET 5.0, these analyzers are [included with the .NET SDK](/dotnet/fundamentals/code-analysis/overview).

- [Code quality analysis ("CAxxxx" rules)](/dotnet/fundamentals/code-analysis/overview#code-quality-analysis):
  - Implemented [here](https://github.com/dotnet/roslyn-analyzers/tree/main/src/NetAnalyzers) in `dotnet/roslyn-analyzers` repo.
  - Documented [here](https://github.com/dotnet/docs/blob/main/docs/fundamentals/code-analysis/quality-rules) in the `dotnet/docs` repo. See [Contribute docs for 'CAxxxx' rules](#contribute-docs-for-caxxxx-rules).
- [Code style analysis ("IDExxxx" rules)](/dotnet/fundamentals/code-analysis/overview#code-style-analysis):
  - Implemented [here](https://github.com/dotnet/roslyn/tree/main/src/Analyzers) in `dotnet/roslyn` repo.
  - Documented [here](https://github.com/dotnet/docs/blob/main/docs/fundamentals/code-analysis/style-rules) in the `dotnet/docs` repo. See [Contribute docs for 'IDExxxx' rules](#contribute-docs-for-idexxxx-rules).

## Contribute docs for 'CAxxxx' rules

Please follow the following steps to contribute documentation for code quality analysis rules to the [dotnet/docs](https://github.com/dotnet/docs) repo:

1. Determine `Rule ID` and `Category`: Ensure that you know the 'CAxxxx' rule ID and category for the rule to be documented. This means either your CA analyzer has been merged into [dotnet/roslyn-analyzers](https://github.com/dotnet/roslyn-analyzers) repo or you have an open PR with an approved ID and category that has been assigned to the rule.
2. Add rule doc:
   1. Clone an existing CA rule file under [root](https://github.com/dotnet/docs/blob/main/docs/fundamentals/code-analysis/quality-rules) folder, say `ca1000.md`, and rename it.
   2. Update the content of the file appropriately.
3. Add an entry for the rule to following tables:
   - In [table of contents](https://github.com/dotnet/docs/blob/main/docs/fundamentals/toc.yml) file under the rule category list. For example, for a CA rule with `Performance` category, search for the term `- name: Performance rules` in the file and add an entry to the list. If none exists, create a new category list under `- name: Code quality rules`.
   - In [top-level rule index](https://github.com/dotnet/docs/blob/main/docs/fundamentals/code-analysis/quality-rules/index.md) file.
   - In `category` based rule index file:
     1. Identify the category based index file under [root](https://github.com/dotnet/docs/blob/main/docs/fundamentals/code-analysis/quality-rules) folder. For example, for a CA rule with `Performance` category, this file is named `performance-warnings.md`. If none exists, create a new category based index file by cloning an existing one.
     2. Add an entry for the rule ID in this file.

> [!TIP]
> Perform a repo search in the `dotnet/docs` repo for a known, existing CA rule ID to identify potential places that might need an update. For example, see <https://github.com/dotnet/docs/search?q=CA2000>.

## Contribute docs for 'IDExxxx' rules

Please follow the following steps to contribute documentation for code style analysis rules to the [dotnet/docs](https://github.com/dotnet/docs) repo:

1. Determine `Rule ID` and code style options, if any: Ensure that you know the 'IDExxxx' rule ID and code style options for the rule to be documented. This means either the IDE analyzer has been merged into the [dotnet/roslyn](https://github.com/dotnet/roslyn) repo or you have an open PR with an approved ID and code style options that have been assigned to the rule.
2. Determine rule `subcategory`: IDE rules have category `Style`. Identify the rule subcategory by reading through the introductory section of [Code style rules](/dotnet/fundamentals/code-analysis/style-rules/index). Most of the IDE code style rules are under the `Language` subcategory.
3. Determine rule `preference group`: Identify the `preference group` for the rule by reading through the preferences headers [here](/dotnet/fundamentals/code-analysis/style-rules/language-rules#net-style-rules).
   - If the rule has known, associated code style option(s), the preferences group will match the `OptionGroup` specified in the code style option declaration.
   - Otherwise, determine if the rule belongs to an existing preference group or needs a new preference group.
4. Add rule doc:
   1. Clone an existing IDE rule file under [root](https://github.com/dotnet/docs/blob/main/docs/fundamentals/code-analysis/style-rules) folder, say `ide0011.md`, and rename it.
   2. Update the content of the file appropriately.
5. Add an entry for the IDE rule and/or code style option(s) to the following tables:
   - In [table of contents](https://github.com/dotnet/docs/blob/main/docs/fundamentals/toc.yml) file under the rule's sub-category and preferences list. For example, for an IDE code style rule with `Language` subcategory and `Modifier preferences` group, search for the term `- name: Language rules` and a child node `- name: Modifier preferences` in the file and add an entry to the list. If either the subcategory list or the preferences list under the subcategory does not exist, create a new one under `- name: Code style rules`.
   - In the [code style option-based index](https://github.com/dotnet/docs/blob/main/docs/fundamentals/code-analysis/style-rules/language-rules.md) file.
   - In the [rule ID-based index](https://github.com/dotnet/docs/blob/main/docs/fundamentals/code-analysis/style-rules/index.md) file.
   - In `preferences group` based rule index file:
     1. Identify the preferences group based index file under [root](https://github.com/dotnet/docs/blob/main/docs/fundamentals/code-analysis/style-rules) folder. For example, for an IDE rule for `Modifier preferences`, this file is named `modifier-preferences.md`. If none exists, create a new preferences group based index file by cloning an existing one.
     2. Add an entry for the rule ID in this file.

> [!TIP]
> Perform a repo search in the `dotnet/docs` repo, for a known, existing IDE rule and/or code style option(s) to identify potential places that might need an update. For example, see <https://github.com/dotnet/docs/search?q=IDE0011> and <https://github.com/dotnet/docs/search?q=csharp_prefer_braces>.

## See also

- [Contribute to the .NET docs repositories](dotnet-contribute.md)
