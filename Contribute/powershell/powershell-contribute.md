---
title: Contribute to the PowerShell docs repositories
description: This article of the repositories that make up the PowerShell documentation.
ms.date: 10/09/2019
---
# Contributing to PowerShell Documentation

Thank you for your interest in PowerShell documentation!

This document covers the process for contributing to the articles and code samples that are hosted
on the PowerShell documentation site. Contributions may be as simple as typo corrections or as
complex as new articles.

The PowerShell documentation site is built from multiple repositories containing one or more
docsets:

- [PowerShell conceptual articles](https://github.com/MicrosoftDocs/PowerShell-Docs)
- PowerShell SDK code samples - private repository containing the samples used in the SDK articles
- [PowerShell .NET SDK reference](/dotnet/api/?view=pscore-6.2.0) - private repository contents
  generated from PowerShell source code

Issues for all this content are tracked in the [PowerShell-Docs](https://github.com/MicrosoftDocs/PowerShell-Docs)
repository.

## Repository Structure

The PowerShell-Docs repository consists of three docsets that are published to [Microsoft Docs](https://docs.microsoft.com/powershell). The docsets are contained in the following folders:

- [/reference/](https://docs.microsoft.com/powershell/scripting/) - contains the PowerShell cmdlet
  reference for the cmdlets that ship in PowerShell. The reference is collected in versions folders
  (3.0, 4.0, 5.0, 5.1, 6, and 7). This docset does not contain the reference for the modules that
  ship in Windows or other Microsoft products.
- [/reference/docs-conceptual](https://docs.microsoft.com/powershell/scripting/) - contains the
  PowerShell conceptual documentation. This include setup instructions, sample scripts, how-to
  topics, and more.
- [/developer/](https://docs.microsoft.com/powershell/developer/) - contains the PowerShell SDK
  conceptual documentation.
