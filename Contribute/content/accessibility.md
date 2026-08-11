---
title: Accessibility and alt text
description: Learn how to make Microsoft Learn documentation more accessible with meaningful alt text, links, tables, and visual cues.
author: cahublou
ms.author: cahublou
ms.date: 08/11/2026
ms.service: learn
ms.topic: contributor-guide
ms.custom: external-contributor-guide
---

# Accessibility and alt text

Accessibility helps make Microsoft Learn useful for more readers, including people
who use screen readers or other assistive technology. Small authoring choices can
make an article easier to understand, navigate, and trust.

## Write meaningful alt text

Alternative text, or alt text, describes an image for readers who can't see it.
Screen readers read alt text aloud, so the text should provide information that's
equivalent to the visual element.

Use alt text for images that convey meaning, such as screenshots, diagrams,
charts, and flowcharts. Good alt text:

- Explains the purpose or core idea of the image.
- Is specific to the image and unique within the article.
- Includes important product names, labels, highlighted areas, values, or states.
- Ends with a period so screen readers pause at the end.
- Uses about 40 to 150 characters when possible.

## Avoid redundant or unhelpful alt text

Don't use alt text that only repeats the file name, the surrounding sentence, or
a generic label. Avoid phrases such as "image of" or "graphic of" because screen
readers already announce images.

Use phrases such as "Screenshot of" or "Diagram that shows" when the type of
visual helps readers understand the content.

- **Use**: "Diagram that shows a client sending requests through an API gateway."
- **Avoid**: "Image of API gateway diagram."
- **Avoid**: "api-gateway.png"
- **Avoid**: "Diagram"

## Add long descriptions for complex images

Complex images include architecture diagrams, graphs, decision trees, and process
flowcharts. If the visual includes more information than alt text can cover, use
the Learn `:::image type="complex":::` syntax and add a long description.

The long description should include the important relationships, values, text,
and data that readers need to understand the visual.

## Mark decorative images correctly

Decorative images and icons don't convey information. Don't add alt text to
decorative images. Instead, use the Learn image syntax with `type="icon"` so the
published page uses an empty alt attribute.

## Use descriptive link text

Write link text that describes the destination or action. Descriptive link text
helps readers understand where a link goes without relying on surrounding text.

- **Use**: "Read the Markdown reference."
- **Avoid**: "Click here."
- **Avoid**: "Learn more."

## Make tables accessible

Use simple tables with clear header rows. Avoid merged cells because they can
make relationships between headers and data difficult to follow. If a table
becomes too complex, consider rewriting the information as headings and lists.

## Don't rely on color alone

Color can help draw attention, but it shouldn't be the only signal. Use text,
labels, position, or other descriptions so readers who can't distinguish the
color still understand the meaning.

## Check build warnings

The Microsoft Learn build validates alt text. Missing alt text, duplicate alt
text, and alt text that uses a bad value such as the image file name can cause
warnings. Resolve these warnings before submitting or updating a pull request.
