---
title: SEO quick reference guide
description: Explore this SEO quick reference guide with writing tips to improve on-page search engine optimization. Make your online content more discoverable by search engines and LLMs.
author: ps0394
ms.author: paulsanders
ms.date: 12/04/2023
ms.topic: contributor-guide
ms.service: learn
ms.custom: external-contributor-guide
---

# SEO quick reference guide

Use these search engine optimization (SEO) tips as a quick reference to the basics of on-page SEO for contributors to Microsoft Learn. This guide can be an effective tool in optimizing your content once you've done your keyword research and aligned your content with user intent. Adhering to these SEO best practices can improve your overall content quality and discoverability by users, search engines, and large language models (LLMs).

## Search results: main elements

- [**Meta title:**](#meta-titles) The meta title is entered in the YAML header in a Markdown document (or between the head tags in HTML). It's displayed on the search engine results page (SERP) and browser tab. It's the title that describes the entire page. It has the greatest impact on search rank and click-through rate (CTR). The meta title isn't the same as the main heading (H1) on the page.
- [**URL:**](#optimized-url) Once chosen, the URL shouldn't be changed because it affects tracking. Changing the URL could send conflicting signals to search engines. The URL should be concise and specific to aid search engines and improve user experience.
- [**Meta description:**](#meta-description) The meta description is also entered in the YAML header in a Markdown document (or between the head tags in HTML). It's displayed in the SERPs below the URL and meta title. This short block of text gives users a preview of what your pages is about. It has a positive impact on CTR and should be a summary that entices users to click.

## View meta title and description in Visual Studio Code

The [Learn Authoring Pack](/contribute/content/get-started-setup-tools?pivots=windows-os-pivot-selection#install-learn-authoring-pack) for Visual Studio Code includes a Search Results Preview to help verify that your title and description are helpful to users when returned in search results. Access the Command Palette with **ALT + M** and select **Search Results Preview**.

## SEO best practices

- **Keyword placement**: Use the primary keyword near the beginning of the meta title, meta description, H1, introduction, H2s, and image text whenever possible.
- **Use terms that address intent.**
- **Be specific.** Use exact terms for products, features, errors, etc., that are likely to match queries put into search engines. Don't use acronyms, unless widely known, such as DNS.

## Meta titles

The meta title should be clear and concise, and it should include the primary keyword. For example, for a tutorial on Python programming, a suitable meta title could be "Python Mastery: A Comprehensive Guide for Beginners." This title not only includes the primary keyword "Python" but also provides a glimpse into the content focus. It should also:

- **Be the right length.** For optimal SEO, write the title so that the entire title is 30-65 characters long. The entire title is: Meta title + meta titleSuffix + suffix "| Microsoft Learn." (Some teams use titleSuffix metadata to add the product name. If your team doesn't use titleSuffix then add the product brand name into the meta title.)
- **Be written in title case.** This means to capitalize every word except for small words such as "a, an, the, of," etc.
- **Show enough information** for users to determine relevance.
- **Describe a specific scenario or benefit.**

## Optimized URL

The page URL displays in the search result and contributes to rank and relevance.

- Follow the URL convention for your site.
- Should be 75 characters max using lowercase letters, numbers, and hyphens.
- Use key terms from the meta title and H1.

## Meta description

The meta description allows search engines and users to understand the page content.

- Should be between 120 and 165 characters, including spaces.
- Describes the specific scenario and/or benefit of the article.
- Entices users to click through to the page.

## Main heading (H1)

The H1 heading is the main heading at the top of an article. The H1 is the second-most important text string for search rank and relevance. There's only one H1 per article. H1 isn't the same as the [meta title](#meta-titles).

It’s ok to copy the meta title, but, when possible, make it more unique and specific. At a minimum, repeat key terms.

## Sub-headings (H2-H3)

H2s divide the primary sections on a page, making it easy for users and search engines to understand the content on the page. Search engines often display H2s as additional links below the metadata description on the SERP. Make them specific and descriptive of a section’s content. Avoid writing one- or two-word headings. Use a heading hierarchy (H2-H3) without skipping a level.

## Image filenames and alt text

Image filenames and alt text can get a page-one result in the image carousel, even if your article isn’t on page one of search otherwise. Although image alt text is primarily an accessibility feature, you can include your primary keyword in the description if it makes sense. Here are some best practices for images and alt text when used in articles:

- **Alt text:** Describe the image in simple language. Use at least 40 characters but no more than 150 characters. Alt text is important because it helps search engines understand the image and increases accessibility for users. Don't include language like “image of.”
- **Image filename:** Use letters, numbers, and hyphens only to a maximum of 80 characters, including spaces. Describe the image and include your primary keyword if it makes sense.
