---
title: Markdown and YML templates for Architecture Guides
description: Get Markdown and YML templates for Architecture Guides, which are articles that don't follow any of the other established AAC templates.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: internal-contributor-guide
author: EdPrice-MSFT
ms.author: edprice
ms.date: 07/08/2022
---

# Markdown and YML templates for Architecture Guides

Use these Markdown and YML templates to create AAC Architecture Guide articles. The only required sections for Architecture Guides are the correct metadata blocks and the H2 sections at the end of the articles: Contributors, Next steps, and Related resources.

## Standard Markdown format for Architecture Guides

The standard Architecture Guide format is a single Markdown file with a metadata block at the beginning of the file.

For Architecture Guides, leave out the `titleSuffix` metadata, because it populates globally as `Azure Architecture Center`. The `ms.subservice` metadata value should be `azure-guide`.

```markdown
---
title: <Article title, which becomes the title metadata>
description: <Write a 100-160 character description that ends with a period and starts with a verb. This becomes the browse card description.>
author: <Your GitHub username>
ms.date: <Publish or major update date - mm/dd/yyyy>
ms.topic: conceptual
ms.service: architecture-center
ms.subservice: azure-guide
categories:
  - <Include at least one category, such as ai-machine-learning, analytics, compute, containers, databases, devops, hybrid, identity, integration, iot, networking, security, storage, and web>
  - <There can be more than one category>
  products:
  - <Choose 1-5 products, such as azure-active-directory, azure-app-service, azure-arc, azure-cosmos-db, azure-data-factory, azure-data-lake, azure-devops, azure-event-hubs, azure-firewall, azure-functions, azure-hdinsight, azure-iot, azure-sql-database, azure-storage, and azure-virtual-machines. If your product is not included here, inquire with our AAC team.>
  - <1-5 products>
  - <1-5 products>
ms.custom: fcp
---

# H1 title

There are no further content requirements for Architecture Guides, except to include the last few sections at the end, and to follow all general Azure Architecture Center content requirements.

The Architecture Guide template requires the following sections at the end of the article:
  
## Contributors

> (Expected, but this section is optional if all the contributors would prefer to not include it)

> Start with the explanation text (same for every article), in italics. Then include the "Principal authors" list and the "Additional contributors" list (if there are additional contributors) (all in plain text, not italics or bold). Link each contributor's name to the person's LinkedIn profile. After the name, place a pipe symbol ("|") with spaces, and then enter the person's title. We don't include the person's company, MVP status, or links to additional profiles. Implement this format:

*This article is maintained by Microsoft. It was originally written by the following contributors.*

Principal authors: > Only the primary authors. List them alphabetically, by last name. Use this format: Fname Lname. If the article gets rewritten, keep the original authors and add in the new one(s).

 * [Author 1 Name](http://linkedin.com/ProfileURL) | (Title, such as "Cloud Solution Architect")
 * [Author 2 Name](http://linkedin.com/ProfileURL) | (Title, such as "Cloud Solution Architect")
 * > Continue for each primary author (even if there are 10 of them).

Other contributors: > Include contributing (but not primary) authors, major editors (not minor edits), and technical reviewers. List them alphabetically, by last name. Use this format: Fname Lname. It's okay to add in newer contributors.

 * [Contributor 1 Name](http://linkedin.com/ProfileURL) | (Title, such as "Cloud Solution Architect")
 * [Contributor 2 Name](http://linkedin.com/ProfileURL) | (Title, such as "Cloud Solution Architect")

## Next steps

- Bulleted list of third-party and other Docs and Microsoft links.
- Links shouldn't include en-us locale unless they don't work without it.
- Docs links should be site-relative, for example (/azure/feature/article-name).
- Don't include trailing slash in any links.

## Related resources

- Links to related Azure Architecture Center articles.
- Links should be relative, for example (../../solution-ideas/articles/article-name.yml).

```

## Browse format for Architecture Guides

Browse format articles must have at least four files:

- A YML file that has the metadata and article H1 title.
- The *-content.md* file that has the article content.
- One or more architectural diagrams, in PNG or SVG format, in the article.
- A browse thumbnail graphic uploaded to the */docs/browser/thumbs/* directory of the AAC repository.

### YML file

Name the YML file *\<architecture-guide>.yml*.

For Architecture Guides, leave out the `titleSuffix` metadata, because it populates globally as `Azure Architecture Center`. The `ms.subservice` metadata value should be `azure-guide`.

```yml
### YamlMime:Architecture
metadata:
  title: <Article title, which becomes the title metadata>
  description: <Write a 100-160 character description that ends with a period and starts with a call to action. This becomes the browse card description.>
  author: <Your GitHub username>
  ms.date: <Publish or major update date - mm/dd/yyyy>
  ms.topic: conceptual
  ms.service: architecture-center
  ms.subservice: azure-guide
azureCategories:
  - <Include at least one category, such as ai-machine-learning, analytics, compute, containers, databases, devops, hybrid, identity, integration, iot, networking, security, storage, and web>
  - <There can be more than one category>
products:
  - <Choose 1-5 products, such as azure-active-directory, azure-app-service, azure-arc, azure-cosmos-db, azure-data-factory, azure-data-lake, azure-devops, azure-event-hubs, azure-firewall, azure-functions, azure-hdinsight, azure-iot, azure-sql-database, azure-storage, and azure-virtual-machines. If your product is not included here, inquire with our AAC team.>
  - <1-5 products>
  - <1-5 products>
name: <The H1 title is a phrase with a present tense verb that describes the scenario (no gerunds, "-ing" verbs). Example: "Use Azure monitoring to integrate security components">
summary: <Write a summary. Can be same as description.>
thumbnailUrl: /azure/architecture/browse/thumbs/<browse-png-filename>.png
content: |
  [!include[](<guide>-content.md)]
```

Notes:

* Make sure you copy the main diagram image into the "/azure/architecture/browse/thumbs" folder.
* Update the YML file with the new thumbnail path for the thumbnailUrl field.
* In the TOC file [https://github.com/MicrosoftDocs/architecture-center/blob/main/docs/toc.yml](https://github.com/MicrosoftDocs/architecture-center-pr/blob/main/docs/toc.yml), add a link to this new YML file. Place the link in one of the Azure categories (such as "AI + Machine Learning"), under its "Guides" section. We list the Architecture Guides in the logical order of workflow. We group similar articles in a topic node, under the "Guides" section of that category.

### Markdown file

Name the corresponding content Markdown file *\<architecture-guide>-content.md*.

Don't enter the H1 title in this MD file, but as the **name** value in the corresponding YML file.

```markdown

Architecture Guides don't have specific content guidelines (except for the three sections at the end), but they should fulfill all the general AAC content requirements.

## Architecture

> Architecture diagram goes here. Use the following format:

![Diagram of the <solution name> architecture.](./images/<file-name>.png)

> Under the architecture diagram, include this sentence and a link to the Visio file or the PowerPoint file: 

*Download a [Visio file](https://arch-center.azureedge.net/DiagramName.vsdx) of this architecture.*

- A numbered or bulleted list describing the architecture usually follows the diagram.
- However, the Architecture Guide template doesn't require a section named Architecture, nor a bulleted or numbered list.

The Architecture Guide template requires the following sections at the end of the article:
  
## Contributors
  
> Start with the explanation text (same for every article), in italics. Then include the "Principal authors" list and the "Additional contributors" list (if there are additional contributors). Link each contributor's name to the person's LinkedIn profile. After the name, place a pipe symbol ("|") with spaces, and then enter the person's title. We don't include the person's company, MVP status, or links to additional profiles. Implement this format:

*This article is maintained by Microsoft. It was originally written by the following contributors.*

**Principal authors:** > Only the primary authors. List them alphabetically, by last name. Use this format: Fname Lname. If the article gets rewritten, keep the original authors and add in the new one(s).

 * [Author 1 Name](http://linkedin.com/ProfileURL) | (Title, such as "Cloud Solution Architect")
 * [Author 2 Name](http://linkedin.com/ProfileURL) | (Title, such as "Cloud Solution Architect")
 * > Continue for each primary author (even if there are 10 of them).

**Other contributors:** > Include contributing (but not primary) authors, major editors (not minor edits), and technical reviewers. List them alphabetically, by last name. Use this format: Fname Lname. It's okay to add in newer contributors.

 * [Contributor 1 Name](http://linkedin.com/ProfileURL) | (Title, such as "Cloud Solution Architect")
 * [Contributor 2 Name](http://linkedin.com/ProfileURL) | (Title, such as "Cloud Solution Architect")
  
 *To see non-public LinkedIn profiles, sign in to LinkedIn.*

## Next steps

- Bulleted list of third-party and other Docs and Microsoft links.
- Links shouldn't include "en-us" locale unless they don't work without it.
- Documentation links should be relative, such as (/azure/feature/article-name).
- Don't include a trailing slash in any links.

Examples:
* [Azure Kubernetes Service (AKS) documentation](/azure/aks)
* [Azure Machine Learning documentation](/azure/machine-learning)
  
## Related resources

> Link to articles in the AAC repo. The links should be relative, such as (../../solution-ideas/articles/<article-name>.yml).
  
Examples:
  - [Artificial intelligence (AI) - Architectural overview](/azure/architecture/data-guide/big-data/ai-overview)
  - [Choosing a Microsoft cognitive services technology](/azure/architecture/data-guide/technology-choices/cognitive-services)
  - [Chatbot for hotel reservations](/azure/architecture/example-scenario/ai/commerce-chatbot)
  - [Build an enterprise-grade conversational bot](/azure/architecture/reference-architectures/ai/conversational-bot)

```
