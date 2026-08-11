---
title: AI-assisted authoring tools for Microsoft Learn
description: Learn how AI-assisted tools in Visual Studio Code can help you author Microsoft Learn documentation.
ms.topic: contributor-guide
ms.service: learn
ms.custom: external-contributor-guide
author: cahublou
ms.author: cahublou
ms.date: 08/11/2026
---

# AI-assisted authoring tools for Microsoft Learn

AI-assisted authoring tools can help you draft, review, and refine documentation in Visual Studio Code. These tools are optional aids. You can still contribute to Microsoft Learn by using the standard workflow and the [Learn Authoring Pack](how-to-write-docs-auth-pack.md).

This article introduces two AI-assisted tools that might be useful when you work on Microsoft Learn Markdown files:

- Microsoft Learn Authoring Assistant
- GitHub Copilot for Visual Studio Code

Availability and features can vary by account, repository, organization settings, and extension access. If a tool isn't available to you, continue using the Learn Authoring Pack and the guidance in this contributor guide.

## Microsoft Learn Authoring Assistant

Microsoft Learn Authoring Assistant is a Visual Studio Code extension that works with GitHub Copilot Chat to help improve Learn Markdown content. It reviews Markdown files and suggests edits for issues such as grammar, voice, clarity, readability, and Microsoft writing guidance.

Depending on your setup, the Authoring Assistant can show suggested edits in Visual Studio Code so you can review them before making changes. You can accept a suggestion, adjust it manually, or leave your original text unchanged.

The Authoring Assistant is designed to support review, not replace it. Always check suggestions for technical accuracy, context, and the needs of the article's audience.

## GitHub Copilot for documentation

GitHub Copilot for Visual Studio Code can help with documentation authoring by providing writing suggestions and help with code examples as you work. For example, you might use Copilot to brainstorm wording, revise a paragraph, or draft example code that you then test and verify.

Copilot suggestions are AI-generated. Review them carefully before using them in Microsoft Learn content. Make sure any suggested text is accurate, original, appropriate for the article, and aligned with Microsoft Learn style and contribution requirements.

## Use these tools with the Learn Authoring Pack

The Learn Authoring Pack remains the core Visual Studio Code extension pack for Microsoft Learn Markdown authoring. It includes tools for Markdown support, previews, templates, linting, spelling, YAML assistance, and image handling.

Use AI-assisted tools alongside the Learn Authoring Pack when they're available to you. For example, you can use the Learn Authoring Pack to preview and validate Markdown, then use an AI-assisted tool to help refine wording or review style suggestions.

## Install or enable the tools

To use these tools in Visual Studio Code, start with the standard setup for major documentation contributions:

1. Install Visual Studio Code.
1. Install the Learn Authoring Pack.
1. Open the root folder of your cloned documentation repository in Visual Studio Code.

To try Microsoft Learn Authoring Assistant, open the Visual Studio Code Extensions view and search for **Microsoft Learn Authoring Assistant**. If the extension is available to you, install it and follow any sign-in prompts. Some features might require specific account access or GitHub Copilot Chat.

To try GitHub Copilot, make sure GitHub Copilot is enabled for your GitHub account. In Visual Studio Code, open the Extensions view, search for **GitHub Copilot**, and install the extension. If you want Copilot suggestions in Markdown files, check the GitHub Copilot extension settings and enable Markdown support if it isn't already enabled.

## Next steps

- [Install content-authoring tools](get-started-setup-tools.md)
- [Learn Authoring Pack for Visual Studio Code](how-to-write-docs-auth-pack.md)
