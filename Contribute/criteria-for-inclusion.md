---
title: Criteria for inclusion into the External contributors guide
description: This article outlines the inclusion criteria for docs.microsoft.com external contributors guide topics 
author: jralexander
ms.author: johalex
manager: wpickett
ms.date: 05/31/2018
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.custom: external-contributor-guide
---
# Criteria for inclusion into the External contributor's guide

In an ideal Open Source project, our external contributor guide would be the same document as the internal contributor guide: the goals, processes, and tools used by external contributors would be the same as those used by internal contributors. In reality, some guidance is internal only. This article explains those situations where guidance must be internal only.

The decision process is that any guidance **does** belong in the external contributor guide, unless there is a clear reason to exclude it. That ensures that we have guidance in place for any potential contribution from the commuunity. If we don’t provide the guidance, we’ll be correcting people without having set expectations properly.

The general rule is that the contributor's guide is for everyone that contributes, except under these situations:

- Content for [external products and tools](#external-products).
- Specific guidance about [an internal tool](#internal-tools).
- Writing for [unreleased and unannounced products](#unlreleased-products).
- [Administrative tasks](#administrative-tasks).

In addition to the above rules, there are tasks and processes that are far more likely to be done by members of the content teams than our partner teams or external contributors. That fact leads to organizing the external guide around [the most common external tasks](#common-external-tasks).

## External products

There are tools that are necessary for content creation, but are another team's or company's responsibility. For example, we won't include dcoumentation on using GitHub, but will point to the GitHub guides for specific tasks. We won't provide complete documentation on Markdown, but we will point to other resources for that infomration. We won't document Visual Studio Code, but will point to Visual Studio Code documentation. We will, however, document the docs authoring pack extension.

## Internal tools

The content teams make use of many tools and processes that are not available to external contributors. Some are part of the adminstrative process around repositories and document sets, others are part of the authoring process, and others are part of the review and approval process. The Acrolinx extension is one such tool. Other policies are internal only, such as the rules governing policheck. The processes used for publishing or configuring builds are internal. Finally, some tools are not yet ready to be released for external contributors. Topics related to these tools are not included in any external facing guidance.

## Unreleased products

Teams work in private repositories to enable work on products or releases that have not been announced yet (among other reasons). The external contributor guide does not include resources or information on working in private repositories. It does not include information on coordinating branches between private and public repositories.

## Administrative tasks
 
==> John

Non content
Infrastructure tasks

consider limiting administrative tasks (bread crumbs, hub pages, and so on....) Product renaming likely fits here.

## Common external tasks

 ==> Tom

The goals for the ToC organization for external contributors differ from internal ToC goals. For external contributors:

* It's more important that the ToC not look intimidatingly large, either at first glance or when drilling down to a particular task. Fewer ToC nodes is generally better except for a "Reference" area.
* If they come to the guide looking for how to do a particular task, they should be able to find one entry to one article at or near the top ToC level. If the task is presented as needing a collection of 6 articles to learn how to accomplish, the potential contributor may be dissuaded from trying.

### Preliminary ToC organization plan

* Introduction
* Communicate with the docs team<sup>1</sup>
* How to make simple changes<sup>2</sup>
* How to make complex changes<sup>3</sup>
* Create a new article<sup>4</sup>
* FAQ<sup>5</sup>
* Reference and Resources
  * Text formatting [article from internal guide]
  * Add code to articles [article from internal guide]
  * Add art to articles [ToC node from internal guide]
  * Add links to articles [article from internal guide]
  * Add alerts to articles [article from internal guide]
  * Add lists and bullets to articles [article from internal guide]
  * TOC management [article from internal guide]
  * Repository-specific guidance [ToC node from internal guide]
  * Pull Request review process [ToC node from internal guide]
  * [include here relevant nodes under Resources node in internal guide]<sup>6</sup>
  
<sup>1</sup> Leaf node, goes to an article about how and where to create GitHub issues to report problems, propose changes, propose new content, and so forth.

<sup>2</sup> Leaf node, goes to an article about browser workflow, with embedded video at the top.

<sup>3</sup> Leaf node, goes to a how-to article about local clone editing workflow. Gives in one article everything from set up to responding to PR feedback: Install Git, VS Code, Docs Authoring pack, fork and clone, find the file, create a working branch, stage and commit changes, push to remote, create PR, respond to feedback.

<sup>4</sup> Non-leaf node, OK to have a collection of articles here because it would be expected that there's much more to learn if you're creating something from scratch. Contains an overview article plus each of the article-type how-tos under Create content / Write in the internal ToC.

<sup>5</sup> Quick answers to common questions, such as -- CLA, getting credit for contributions, 

<sup>6</sup> If we kept separate nodes for Reference and Resources, people would not find some things due to looking in the wrong place.  For example, you might expect to find the Style Guide link under Reference, but it's under Resources.


