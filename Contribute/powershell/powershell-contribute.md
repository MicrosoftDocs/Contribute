---
title: Contribute to the PowerShell docs repositories
description: This article of the repositories that make up the PowerShell documentation.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
author: sdwheeler
ms.author: sewhee
ms.date: 10/09/2019
---
# Contributing to PowerShell Documentation

Thank you for your interest in PowerShell documentation!

This document covers the process for contributing to the articles and code samples that are hosted
on the PowerShell documentation site. Contributions may be as simple as typo corrections or as
complex as new articles.

The PowerShell documentation site is built from multiple repositories containing one or more
docsets:

- [PowerShell concepts & cmdlet reference][psdocs]
- PowerShell SDK code samples - private repository containing the samples used in the SDK articles
- [PowerShell .NET SDK reference](/dotnet/api/?view=pscore-6.2.0) - private repository contents
  generated from PowerShell source code

Issues for all this content are tracked in the [PowerShell-Docs][docsrepo] repository.

## Repository Structure

The PowerShell-Docs repository consists of three docsets that are published to
[Microsoft Docs][psdocs]. The docsets are contained in the following folders:

- [/reference/][ref] - contains the PowerShell cmdlet reference for the cmdlets that ship in
  PowerShell. The reference is collected in versions folders (3.0, 4.0, 5.0, 5.1, 6, and 7). This
  docset does not contain the reference for the modules that ship in Windows or other Microsoft
  products.
- [/reference/docs-conceptual][conceptual] - contains the PowerShell conceptual documentation. This
  include setup instructions, sample scripts, how-to topics, and more.
- [/developer/][SDK] - contains the PowerShell SDK conceptual documentation.

<!--link refs-->
[psdocs]: https://docs.microsoft.com/powershell
[docsrepo]: https://github.com/MicrosoftDocs/PowerShell-Docs
[ref]: https://github.com/MicrosoftDocs/PowerShell-Docs/tree/staging/reference
[conceptual]: https://github.com/MicrosoftDocs/PowerShell-Docs/tree/staging/reference/docs-conceptual
[SDK]: https://github.com/MicrosoftDocs/PowerShell-Docs/tree/staging/developer
