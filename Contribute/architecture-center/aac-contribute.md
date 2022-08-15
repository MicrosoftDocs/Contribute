---
title: Contribute to the Azure Architecture Center
description: This article describes how to contribute to the Azure Architecture Center.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
author: EdPrice-MSFT
ms.author: edprice
ms.date: 08/16/2022
---

# Azure Architecture Center contributions

You can edit articles or create new articles for the Azure Architecture Center. The Azure Architecture Center (AAC) encourages contributions from the public, through GitHub issues and pull requests (PR). This page covers the general guidelines for contributing content to the Azure Architecture Center.

## Overview

The Azure Architecture Center (AAC) helps customers design, build, and operate solutions on Azure. AAC consists of three main sections of content: [Architecture fundamentals](/azure/architecture/guide), Industry solutions, and Azure categories. 

Some Azure architecture fundamental topics include Architecture styles, Design principles, Technology choices, Best practices, Antipatterns, Responsible engineering, Mission critical applications, Multitenant applications,  Solutions across Microsoft platforms, Third-party scenarios, Azure for AWS professionals, and Azure for Google Cloud professionals, and Cloud Desig Patterns. Some industry solution examples are Retail,  

Some featured industries include Retail, Finance, Healthcare, Government, Manufacturing, Energy, Telecommunications, Automotive, Education, and Nonprofit.

Azure categories include AI + Machine Learning, Analytics, Blockchain + Multiparty Compute, Compute + HPC, Containers, Databases, DataOps, Developer Options (Microservices and Serverless), DevOps, Hybrid + Multicloud, Identity, Integration, Internet of Things, Mainframe + Midrange, Management + Governance, Media, Migration, Mixed Reality, Mobile, Networking, Oracle, SAP, Security, Storage, Virtual Desktop, and Web.

## Submit a new article

You can submit a new article on Azure Architecture Center!

### Base requirements

All new contributions (submitted articles) *must* follow these requirements:

- Cover a gap in existing articles.
- Describe the ideal solution or pathway for a specific scenario.
- Include multiple services and technologies.
- Is a scenario supported by Microsoft.

All contributions *must not have* the following:

- Limited pattern applicability (where fewer than dozens of customers could benefit).
- Incur unreasonable costs for the consumer, unless we specify what type of consumer will benefit from it.

If your solution includes code and/or a deployment, then there are a number of additional requirements.

### Process

1. You (the contributor) must submit a proposed article. Send an email to [AACProposals@microsoft.com](mailto:AACProposals@microsoft.com). Include the following information:
    1. Your name.
    1. The name of your proposed article.
    1. What type of content this should be. Options include an Architecture Guide, a Solution Idea, an Example Workload, or a Reference Architecture.
    1. A brief description of your article.
    1. The category (such as AI/ML, Databases, or Security) and/or the industry (such as Retail, Healthcare, and so on) that this article would fit in (
    1. A draft of your article (and/or your code) if you have it. The most efficient way to do this is to send us a Word doc. This could include a link to an accessible location (like a OneDrive), a blog post or GitHub MD file that the article is based on, and so on.
    1. List the names of all the team members involved in creating this content. Include them in CC on your email.
    
1. We will follow up with you and ask any questions to make sure this isn't repeated content and to sync on the next steps.

1. You (the contributor) submit the draft article. Because we don't have resources to create the draft, you must write the initial draft of the article.

> [!NOTE]
> If this article is an architecture, you must provide a Visio or PowerPoint diagram of the architecture.

1. We will review the draft with you to ensure technical accuracy and technical completeness (it tells the full story).

1. We will edit the article (technical edit and copy edit), edit and refine the diagram, and publish the final article.

## Edit an existing article

You can edit an existing article on Azure Architecture Center if you see a typo, want to add a link, or want to add more details.

### Base requirements

All edits *must* follow these requirements:

- Be technically accurate.
- Provide helpful or valuable information in the context of the article.

All edits *must not have* the following:

- Link to advertise another company's product, unless the company's components are part of the architecture.

### Process

**Setup**. Steps to follow to set up your GitHub account and browser for editing:

1. Set up your GitHub account. See [GitHub account setup](/contribute/get-started-setup-github).

1. To improve your edit experience, install SpineEdit from the [Chrome web store](https://chrome.google.com/webstore/detail/spineedit/llhlgkbkfdfcbjbfnnakfpgmemopbbnf). The extension works in all Chromium-based browsers, including Microsoft Edge.

Learn more about the benefits of [SpineEdit](https://github.com/craigshoemaker/spineedit#introduction). 

**Edit**. Steps to follow to edit a Microsoft Docs article:

1. Click the **Edit This Document** button (the pencil icon in the top right of the article, above the title).
1. After you make your edits, click the **Propose changes** button at the bottom of the page. Then click **Create pull request** on the next page.

A Microsoft employee will review your changes, and our pull request review team will merge and publish your changes.

See [Quick edits to documentation](/contribute/?msclkid=4121f48ad0b311eca160953a4cf93670#quick-edits-to-documentation) for detailed instructions.

## Content templates

* **[Architecture Guide templates](guide-templates.md)**. Architecture Guides are AAC articles that do not have a standard structure in the article, except for three sections at the bottom: Contributors (credits), Next steps (links to other articles and sources), and Related resources (links to other AAC guides and architectures). The content can be high-level conceptual, middle-level process-oriented, or low-level implementation instructions. They follow the requirements of all AAC content, including that they are architectural (connecting multiple technologies and services into one story).

* **[Solution Idea templates](solution-idea-templates.md)**. Solution Ideas are our "small" AAC architectures. They provide brief overviews of solutions that customers can implement using Azure services. Each Solution Idea has an architecture diagram, dataflow, components (a list of the services used), contributor credits, next step links, and related resources (links to related AAC guides and architectures).

* **[Example Workload templates](sample-solution-templates.md)**. Example Workloads are our "medium" AAC architectures. They Example workloads guide customers through the design process of solving specific problems in Azure. They provide actionable architecture guidance based on real customer examples. Their goal is to shorten a customer's learning curve by telling them the story of another customer who has been there before. In addition to the Solution Idea sections, they also include Alternatives (other services that you can plug into the architecture instead), Considerations (which map to our Well Architected principals), and they can optionally include a deployment.
