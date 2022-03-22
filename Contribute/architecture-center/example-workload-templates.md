---
title: Markdown and YML templates for example workloads
description: These are the markdown and YML templates for an example workload, previously called an example scenario or sample solution.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
author: EdPrice-MSFT
ms.author: edprice
ms.date: 03/23/2022
---

# Markdown and YML templates for example workloads

Use these Markdown and YML templates to create an example workload, previously called an example scenario or sample solution.

Each article must have two files.

## YML file

Name this file *\<sample-solution>.yml*:

```yml
### YamlMime:Architecture
metadata:
  title: <Article title, which becomes the title metadata>
  titleSuffix: Azure Architecture
  description: <Write a 100-160 character description that ends with a period and ideally starts with a call to action. This becomes the browse card description (at http://aka.ms/Architectures).>
  author: <contributor's GitHub username. If no GitHub account, use EdPrice-MSFT>
  ms.author: <contributor's Microsoft alias. If no alias, use edprice.>
  ms.date: <publish or major update date - mm/dd/yyyy>
  ms.topic: conceptual
  ms.service: architecture-center
  ms.subservice: example-scenario
azureCategories:
  - <choose at least one category, such as ai-machine-learning, analytics, compute, containers, databases, devops, hybrid, identity, integration, internet-of-things, media, migration, mixed-reality, mobile, networking, security, storage, web>
  - <there can be more than one category>
products:
  - <Choose 1-5 products in the format of azure-[productname], such as azure-active-directory or azure-kubernetes-service. To see all of the current products, go to the architecture browse page (http://aka.ms/Architectures)>
  - <1-5 products--no more than 5!>
name: <The H1 title is a noun phrase that describes the scenario. Example: "Insurance claim image classification on Azure">
summary: <Write a summary. Can be the same as the description.>
thumbnailUrl: /azure/architecture/browse/thumbs/<browse-png-filename>.png
content: |
  [!include[](<sample-solution>-content.md)]
```

Notes:

* Make sure you copy the main diagram image into the "/azure/architecture/browse/thumbs" folder.
* Update the YML file with the new thumbnail path for the thumbnailUrl field. This is necessary for a thumbnail to appear in the https://aka.ms/Architectures browse experience.
* In the TOC file (https://github.com/MicrosoftDocs/architecture-center-pr/blob/main/docs/toc.yml), add a link to this new YML file. Place the link in one of the Azure categories (such as "AI + Machine Learning"), under its "Architectures" section. We list the Architectures and Solution ideas alphabetically.

## MD file

Name this file *\<sample-solution-content>.md*:

```markdown
> The H1 title is a noun phrase that describes the scenario. Don't enter it here, but as the **name** value in the corresponding YAML file.

Introductory section - no heading

> This should be an introduction of the business problem and why this scenario was built to solve it.
>> What prompted them to solve the problem?
>> What services were used in building out this solution?
>> What does this example workload show? What are the customer's goals?

> What were the benefits of implementing the solution described below?

## Potential use cases

> What industry/industries is the customer in? 
> Are there any other use cases or industries where this would be a fit?
> How similar or different are they to what's in this article? 
> Use the following format:

These other use cases have similar design patterns:

- <List of example use cases>

## Architecture

> Architecture diagram goes here

> Under the architecture diagram, include this sentence and a link to the Visio file or the PowerPoint file: 

_Download a [Visio file](https://arch-center.azureedge.net/[filename].vsdx) of this architecture._

### Dataflow

> An alternate title for this sub-section is "Workflow" (if data isn't really involved).
> In this section, include a bulleted list or a numbered list (if there are corresponding numbers in the diagram) that annotates/describes the dataflow or workflow through the solution. 
> Explain what each step does. Start from the user or external data source, and then follow the flow through the rest of the solution (as shown in the diagram).

Examples:
1. Admin 1 adds, updates, or deletes an entry in Admin 1's fork of the Microsoft 365 config file.
2. Admin 1 commits and syncs the changes to Admin 1's forked repository.
3. Admin 1 creates a pull request (PR) to merge the changes to the main repository.
4. The build pipeline runs on the PR.

### Components

> A bulleted list of components in the architecture (including all relevant Azure services) with links to the Azure.com product service pages.

> Why is each component there?
> What does it do and why was it necessary?
> Link the name of the service (via embedded link) to the service's product service page, on Azure.com. Be sure to exclude the localization part of the URL (such as "en-US/").

- Examples: 
  - [Azure App Service](https://azure.microsoft.com/services/app-service)
  - [Azure Bot Service](https://azure.microsoft.com/services/bot-service)
  - [Azure Cognitive Services Language Understanding](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service)
  - [Azure Cognitive Services Speech Services](https://azure.microsoft.com/services/cognitive-services/speech-services)
  - [Azure SQL Database](https://azure.microsoft.com/services/sql-database)
  - [Azure Monitor](https://azure.microsoft.com/services/monitor): Application Insights is a feature of Azure Monitor.
  - [Resource Groups][resource-groups] is a logical container for Azure resources.  We use resource groups to organize everything related to this project in the Azure console.

### Alternatives

> Use this section to talk about alternative Azure services or architectures that you might consider for this solution. Include the reasons why you might choose these alternatives. Readers find this valuable because they want to know what other services or technologies they can use as part of this architecture.

> What alternative technologies were considered and why didn't we use them?

## Considerations

> Include a statement to introduce this section, like this:
> "These considerations implement the pillars of the Azure Well-Architected Framework, which is a set of guiding tenets that can be used to improve the quality of a workload. For more information, see [Microsoft Azure Well-Architected Framework](/azure/architecture/framework)."

> Are there any lessons learned from running this that would be helpful for new customers?  What went wrong when building it out?  What went right?
> How do I need to think about managing, maintaining, and monitoring this long term?
> REQUIREMENT: Note that you must have "Cost optimization" and at least two of the other H3 sub-sections/pillars.

### Reliability

> This includes resiliency and availability.
> Are there any key resiliency and reliability considerations (past the typical)?
> Include a link to the [Overview of the reliability pillar](/azure/architecture/framework/resiliency/overview).

### Security

> This includes identity and data sovereignty.
> Are there any security considerations (past the typical) that I should know about this? 
> Include a link to the [Overview of the operational excellence pillar](/azure/architecture/framework/devops/overview).

### Cost optimization

> REQUIRED: This section is required. Cost is of the utmost importance to our readers.

> How much will this cost to run? See if you can answer this without dollar amounts. (We link to the pricing calculator, so that we don't have to update the article.)
> Are there ways I could reduce the cost?
> If it scales linearly, than we should break it down by cost/unit. If it does not, why?
> What are the components that make up the cost?
> How does scale affect the cost?
> Include a link to the [Overview of the cost optimization pillar](/azure/architecture/framework/cost/overview).

> Link to the pricing calculator with all of the components in the architecture included, even if they're a $0 or $1 usage.
> If it makes sense, include small/medium/large configurations. Describe what needs to be changed as you move to larger sizes.

### Operational excellence

> This includes DevOps, monitoring, and diagnostics.
> How do I need to think about operating this solution?
> Include a link to the [Overview of the operational excellence pillar](/azure/architecture/framework/devops/overview).

### Performance efficiency

> This includes scalability.
> Are there any key performance considerations (past the typical)?
> Are there any size considerations around this specific solution? What scale does this work at? At what point do things break or not make sense for this architecture?
> Include a link to the [Performance efficiency pillar overview](/azure/architecture/framework/scalability/overview).

## Deploy this scenario

> (Optional, but greatly encouraged)

> Is there an example deployment that can show me this in action?  What would I need to change to run this in production?

## Contributors

> (Expected, but this section is optional if the principal authors would prefer to not include it)

> Start with the explanation text (same for every article), in italics. This makes it clear that Microsoft takes responsibility for the article (not the one contributor). 
> Then include the "Pricipal authors" list and the "Additional contributors" list (if there are additional contributors). Link each contributor's name to the person's LinkedIn profile. After the name, place a pipe symbol ("|") with spaces, and then enter the person's title. 
> We don't include the person's company, MVP status, or links to additional profiles (to minimize edits/updates).  
> Implement this format:

_This article is being updated and maintained by Microsoft. It was originally written by the following contributors._

**Principal authors:** > Only the primary authors. Listed alphabetically by last name. Use this format: Fname Lname. If the article gets rewritten, keep the original authors and add in the new one(s).

 * [Author 1 Name](http://linkedin.com/ProfileURL) | [Title, such as "Cloud Solution Architect"]
 * [Author 2 Name](http://linkedin.com/ProfileURL) | [Title, such as "Cloud Solution Architect"]
 * > Continue for each primary author (even if there are 10 of them).

**Additional contributors:** > Include contributing (but not primary) authors, major editors (not minor edits), and technical reviewers. Listed alphabetically by last name. Use this format: Fname Lname. It's okay to add in newer contributors.

 * [Contributor 1 Name](http://linkedin.com/ProfileURL) | [Title, such as "Cloud Solution Architect"]
 * [Contributor 2 Name](http://linkedin.com/ProfileURL) | [Title, such as "Cloud Solution Architect"]
 * > Continue for each additional contributor (even if there are 10 of them).

## Next steps

> Link to Docs and Learn articles, along with any third-party documentation.
> Where should I go next if I want to start building this?
> Are there any relevant case studies or customers doing something similar?
> Is there any other documentation that might be useful? Are there product documents that go into more detail on specific technologies that are not already linked?

Examples:
* [Azure Kubernetes Service (AKS) documentation](/azure/aks)
* [Azure Machine Learning documentation](/azure/machine-learning)
* [What are Azure Cognitive Services?](/azure/cognitive-services/what-are-cognitive-services)
* [What is Language Understanding (LUIS)?](/azure/cognitive-services/luis/what-is-luis)
* [What is the Speech service?](/azure/cognitive-services/speech-service/overview)
* [What is Azure Active Directory B2C?](/azure/active-directory-b2c/overview)
* [Introduction to Bot Framework Composer](/composer/introduction)
* [What is Application Insights](/azure/azure-monitor/app/app-insights-overview)
 
## Related resources

> Use "Related resources" for related architecture guides and architectures (content on the Azure Architecture Center).

Examples:
  - [Artificial intelligence (AI) - Architectural overview](/azure/architecture/data-guide/big-data/ai-overview)
  - [Choosing a Microsoft cognitive services technology](/azure/architecture/data-guide/technology-choices/cognitive-services)
  - [Chatbot for hotel reservations](/azure/architecture/example-scenario/ai/commerce-chatbot)
  - [Build an enterprise-grade conversational bot](/azure/architecture/reference-architectures/ai/conversational-bot)
  - [Speech-to-text conversion](/azure/architecture/reference-architectures/ai/speech-ai-ingestion)

```
