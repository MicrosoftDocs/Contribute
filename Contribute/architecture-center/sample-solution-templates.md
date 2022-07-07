---
title: Markdown and YML templates for example workloads
description: These are the markdown and YML templates for an example workload architecture.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
author: EdPrice-MSFT
ms.author: edprice
ms.date: 07/08/2022
---

# Markdown and YML templates for example workloads

Alternatively, you can email us a Word document of your architecture, using the Example Workload Word template. Send the draft of your article to [AACProposals@microsoft.com](mailto:AACProposals@microsoft.com). The Word template is coming soon.

Use these Markdown and YML templates to create an example workload architecture.

Each article must have two files: YML and MD.

## YML file

Name this file *\<example-workload>.yml*:

```yml
### YamlMime:Architecture
metadata:
  title: <Article title, which becomes the title metadata>
  titleSuffix: Azure Architecture Center
  description: <Write a 100-160 character description that ends with a period and starts with a verb. This becomes the browse card description.>
  author: <Your GitHub username>
  ms.date: <Publish or major update date - mm/dd/yyyy>
  ms.topic: conceptual
  ms.service: architecture-center
  ms.subservice: example-scenario
azureCategories:
  - <Include at least one category, such as ai-machine-learning, analytics, compute, containers, databases, devops, hybrid, identity, integration, iot, networking, security, storage, and web>
  - <There can be more than one category>
products:
  - <Choose 1-5 products, such as azure-active-directory, azure-app-service, azure-arc, azure-cosmos-db, azure-data-factory, azure-data-lake, azure-devops, azure-event-hubs, azure-firewall, azure-functions, azure-hdinsight, azure-iot, azure-sql-database, azure-storage, and azure-virtual-machines. If your product is not included here, inquire with our AAC team.>
  - <Second product. Include 1-5 products--no more than 5!>
name: <The H1 title is a phrase with a present tense verb that describes the scenario (no gerunds, "-ing" verbs). Example: "Use Azure monitoring to integrate security components">
summary: <Write a summary. Can be same as description.>
thumbnailUrl: /azure/architecture/browse/thumbs/<browse-png-filename>.png
content: |
  [!include[](<sample-solution>-content.md)]
```

Notes:

* Make sure you copy the main diagram image into the "/azure/architecture/browse/thumbs" folder.
* Update the YML file with the new thumbnail path for the thumbnailUrl field.
* In the TOC file [https://github.com/MicrosoftDocs/architecture-center/blob/main/docs/toc.yml](https://github.com/MicrosoftDocs/architecture-center-pr/blob/main/docs/toc.yml), add a link to this new YML file. Place the link in one of the Azure categories (such as "AI + Machine Learning"), under its "Architectures" section. We list the Architectures alphabetically.

## MD file

Name this file *\<sample-solution>-content.md* (do not use acronyms or capitals in the filename):

```markdown

> Introductory section - no heading
>   In this section, include 1-2 sentences to briefly explain this architecture. 
>   The full scenario info will go in the "Scenario details" section, which is below the "Alternatives" header, and above the "Considerations" header. That includes the "Potential use cases" H3 section, which goes under the "Scenario details" section.

## Architecture

> Architecture diagram goes here. Use the following format:

![Diagram of the <solution name> architecture.](./images/<file-name>.png)

> Under the architecture diagram, include this sentence and a link to the Visio file or the PowerPoint file: 

*Download a [Visio file](https://arch-center.azureedge.net/[file-name].vsdx) of this architecture.*

> Note that you must send the Visio or PowerPoint file to the AAC contact.

### Dataflow

> An alternate title for this sub-section is "Workflow" (if data isn't really involved).
> In this section, include a numbered list that annotates/describes the dataflow or workflow through the solution. Explain what each step does. Start from the user or external data source, and then follow the flow through the rest of the solution (as shown in the diagram).

The following workflow (or dataflow) corresponds to the above diagram:
1. Admin 1 adds, updates, or deletes an entry in Admin 1's fork of the Microsoft 365 config file.
2. Admin 1 commits and syncs the changes to Admin 1's forked repository.
3. Admin 1 creates a pull request (PR) to merge the changes to the main repository.
4. The build pipeline runs on the PR.

### Components

> A bullet list of components in the architecture (including all relevant Azure services) with links to the product service pages on Azure.com.

> Why is each component there?
> What does it do and why was it necessary?
> Link the name of the service (via embedded link) to the service's product service page. Be sure to exclude the localization part of the URL (such as "en-US/").

- Examples: 
  - [Azure App Service](https://azure.microsoft.com/services/app-service)
  - [Azure Bot Service](https://azure.microsoft.com/services/bot-service)
  - [Azure Cognitive Services Language Understanding](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service)
  - [Azure Cognitive Services Speech Services](https://azure.microsoft.com/services/cognitive-services/speech-services)
  - [Azure SQL Database](https://azure.microsoft.com/services/sql-database)
  - [Azure Monitor](https://azure.microsoft.com/services/monitor): Application Insights is a feature of Azure Monitor.
  - [Resource Groups][resource-groups] is a logical container for Azure resources.  We use resource groups to organize everything related to this project in the Azure console.

### Alternatives

> Use this section to talk about alternative Azure services or architectures that you might consider for this solution. Include the reasons why you might choose these alternatives.

> What alternative technologies were considered and why didn't we use them?

## Scenario details

> This should be an explanation of the business problem and why this scenario was built to solve it.
>   What prompted them to solve the problem?
>   What services were used in building out this solution?
>   What does this example scenario show? What are the customer's goals?
> What were the benefits of implementing the solution?

### Potential use cases

> What industry is the customer in? Use the following industry keywords, when possible, to get the article into the proper search and filter results: retail, finance, manufacturing, healthcare, government, energy, telecommunications, education, automotive, nonprofit, game, media (media and entertainment), travel (includes hospitality, like restaurants), facilities (includes real estate), aircraft (includes aerospace and satellites), agriculture, and sports. 
>   Are there any other use cases or industries where this would be a fit?
>   How similar or different are they to what's in this article?

## Considerations

> REQUIRED STATEMENT: Include the following statement to introduce this section:

These considerations implement the pillars of the Azure Well-Architected Framework, which is a set of guiding tenets that can be used to improve the quality of a workload. For more information, see [Microsoft Azure Well-Architected Framework](/azure/architecture/framework).

> Are there any lessons learned from running this that would be helpful for new customers?  What went wrong when building it out?  What went right?
> How do I need to think about managing, maintaining, and monitoring this long term?

> REQUIREMENTS: 
>   You must include the "Cost optimization" section. 
>   You must include at least two of the other H3 sub-sections/pillars: Reliability, Security, Operational excellence, and Performance efficiency.

### Reliability

> REQUIRED STATEMENT: If using this section, include the following statement to introduce the section:

Reliability ensures your application can meet the commitments you make to your customers. For more information, see [Overview of the reliability pillar](/azure/architecture/framework/resiliency/overview)."

> This section includes resiliency and availability considerations. They can also be H4 headers in this section, if you think they should be separated.
> Are there any key resiliency and reliability considerations (past the typical)?

### Security

> REQUIRED STATEMENT: If using this section, include the following statement to introduce the section:

Security provides assurances against deliberate attacks and the abuse of your valuable data and systems. For more information, see [Overview of the security pillar](/azure/architecture/framework/security/overview).

> This section includes identity and data sovereignty considerations.
> Are there any security considerations (past the typical) that I should know about this?

### Cost optimization

> REQUIRED: This section is required.

> REQUIRED STATEMENT: Include the following statement to introduce the section:

Cost optimization is about looking at ways to reduce unnecessary expenses and improve operational efficiencies. For more information, see [Overview of the cost optimization pillar](/azure/architecture/framework/cost/overview).

> How much will this cost to run? See if you can answer this without dollar amounts.
> Are there ways I could save cost?
> If it scales linearly, than we should break it down by cost/unit. If it does not, why?
> What are the components that make up the cost?
> How does scale affect the cost?

> Link to the pricing calculator (https://azure.microsoft.com/pricing/calculator) with all of the components in the architecture included.
> If it makes sense, include small/medium/large configurations. Describe what needs to be changed as you move to larger sizes.

### Operational excellence

> REQUIRED STATEMENT: If using this section, include the following statement to introduce the section:

Operational excellence covers the operations processes that deploy an application and keep it running in production. For more information, see [Overview of the operational excellence pillar](/azure/architecture/framework/devops/overview).

> This includes DevOps, monitoring, and diagnostics considerations.
> How do I need to think about operating this solution?

### Performance efficiency

> REQUIRED STATEMENT: If using this section, include the following statement to introduce the section:

Performance efficiency is the ability of your workload to scale to meet the demands placed on it by users in an efficient manner. For more information, see [Performance efficiency pillar overview](/azure/architecture/framework/scalability/overview).

> This includes scalability considerations.
> Are there any key performance considerations (past the typical)?
> Are there any size considerations around this specific solution? What scale does this work at? At what point do things break or not make sense for this architecture?

## Deploy this scenario

> (Optional, but greatly encouraged)

> Is there an example deployment that can show me this in action?  What would I need to change to run this in production?

## Contributors

> Start with the explanation text (same for every section), in italics. Then include the "Principal authors" list and the "Other contributors" list, if there are additional contributors (all in plain text, not italics or bold). We include all the contributors in these lists, regardless of what company they work for. Link each contributor's name to the person's LinkedIn profile. After the name, place a pipe symbol ("|") with spaces, and then enter the person's title. We don't include the person's company, MVP status, or links to additional profiles. Implement this format:

*This article is maintained by Microsoft. It was originally written by the following contributors.* 

Principal authors: > Only the primary authors. Listed alphabetically by last name. Use this format: Fname Lname. If the article gets rewritten, keep the original authors and add in the new one(s).

 - [Author 1 Name](http://linkedin.com/ProfileURL) | (Title, such as "Cloud Solution Architect")
 - [Author 2 Name](http://linkedin.com/ProfileURL) | (Title, such as "Cloud Solution Architect")
 - > Continue for each primary author (even if there are 10 of them).

Other contributors: > Include contributing (but not primary) authors, major editors (not minor edits), and technical reviewers. Listed alphabetically by last name. Use this format: Fname Lname. It's okay to add in newer contributors.

 - [Contributor 1 Name](http://linkedin.com/ProfileURL) | (Title, such as "Cloud Solution Architect")
 - [Contributor 2 Name](http://linkedin.com/ProfileURL) | (Title, such as "Cloud Solution Architect")
 - > Continue for each additional contributor (even if there are 10 of them).
 
*To see non-public LinkedIn profiles, sign in to LinkedIn.*

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

> Link to articles in the AAC repo. The links should be relative, such as (../../solution-ideas/articles/<article-name>.yml).

Examples:
  - [Artificial intelligence (AI) - Architectural overview](/azure/architecture/data-guide/big-data/ai-overview)
  - [Choosing a Microsoft cognitive services technology](/azure/architecture/data-guide/technology-choices/cognitive-services)
  - [Chatbot for hotel reservations](/azure/architecture/example-scenario/ai/commerce-chatbot)
  - [Build an enterprise-grade conversational bot](/azure/architecture/reference-architectures/ai/conversational-bot)
  - [Speech-to-text conversion](/azure/architecture/reference-architectures/ai/speech-ai-ingestion)

```
