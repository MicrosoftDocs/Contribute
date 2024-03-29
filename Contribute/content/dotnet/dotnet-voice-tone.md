---
title: Voice and tone guidelines for .NET docs contributions
description: Learn our voice and tone guidelines through examples of our styles compared to examples that don't follow our guidelines.
ms.topic: contributor-guide
ms.service: learn
ms.custom: external-contributor-guide
ms.date: 11/07/2018
---
# Voice and tone guidelines

A wide variety of people including IT Pros and developers read the .NET docs both to learn .NET and to use it in their regular work. Your goal is to create great documentation that helps the reader on their journey. Our guidelines help with that. Our style guide contains the following recommendations:

## Use a conversational tone

The following paragraph is written in a conversational style. The one that follows it is in a more academic style.

### Appropriate style

We want our documentation to have a conversational tone. You should feel as though you are having a conversation with the author as you read any of our tutorials or explanations. For you, the experience should be informal, conversational, and informative. Readers should feel as though they are listening to the author explain the concepts to them.

### Inappropriate style

One might see the contrast between a conversational style and the style one finds with more academic treatments of technical topics. Those resources are very useful, but the authors have written those articles in a very different style than our documentation. When one reads an academic journal, one finds a very different tone and a very different style of writing. One feels that they are reading a dry account of a very dry topic.  

## Write in second person

The following paragraph uses second person. The one that follows it uses third person. Please write in second person.

### Appropriate style

Write your articles as though you are speaking directly to the reader. Use second person often (as in these two sentences). 2nd person doesn't always mean using the word 'you'. Write directly to the reader. Write imperative sentences. Tell your reader what you want them to learn.

### Inappropriate style

An author could also choose to write in third person. In that model, an author must find some pronoun or noun to use when referring to the reader. A reader might often find this third person style less engaging and less enjoyable to read.

## Use active voice

Write your articles in active voice. Active voice means that the subject of the sentence performs the action (verb) of that sentence. It contrasts with passive voice, where the sentence is arranged
such that the subject of the sentence is acted upon. Contrast these two examples:

>The compiler transformed source code into an executable.

>The source code was transformed into an executable by the compiler.

The first sentence uses active voice. The second sentence was written in passive voice. (Those two sentences provide another example of each style).

We recommend active voice because it is more readable. Passive voice can be more difficult to read.

## Write for readers who may have a limited vocabulary

You are reaching an international audience with your articles. Many of your readers are not native English speakers and may not have the English vocabulary you have.

However, you are still writing for technical professionals. You can assume that your readers have programming knowledge and the specific vocabulary for programming terms. Object Oriented Programming, Class and Object, Function and Method are familiar terms. However, not everyone reading your articles has a formal computer science degree. Terms like 'idempotent' probably need to be defined if you use it, for example:

> The `Close()` method is idempotent, meaning that you can call it multiple times and the effect is the same as if you called it once.

## Avoid future tense

In some non-English languages the concept of future tense is not the same as English. Using future tense can make your documents harder to read. Additionally, when using the future tense, the obvious question is when. So if you say 'Learning PowerShell will be good for you" - the obvious question for the reader is when will it be good? Instead, just say "Learning PowerShell is good for you".

## What is it - so what?

Whenever you introduce a new concept to the reader, define the concept and only then explain why it's useful. It's important for reader to understand what something is before they can understand the benefits (or otherwise).
