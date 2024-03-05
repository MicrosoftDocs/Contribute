---
title: "How to refer to .NET in docs"
description: "Learn how to refer to .NET Framework, .NET Core, .NET 5, and later versions in docs."
ms.topic: contributor-guide
ms.service: learn
ms.custom: external-contributor-guide
ms.date: 01/28/2021
---
# How to refer to .NET in docs

This article is mostly concerned with naming for .NET Core and .NET 5 and later versions. For .NET Framework, it should be referred to as ".NET Framework" and not "the .NET Framework".

## Recommended terminology

**In doc title and first heading (h1):**

- ".NET" (without mention of 5 or Core)

**First reference in article text:**

- ".NET" for docs about Core/5+ that present it to people new to .NET.
- ".NET 5 (and .NET Core) and later versions" if needed to emphasize Core/5+ as a specific .NET implementation.

**Subsequent references:**

- ".NET" for docs that present Core/5+ to people new to .NET or where the reference to Core/5+ is clear in context.
- ".NET 5 and later versions" where necessary to differentiate Core/5+ from other .NET implementations.

**Notes:**

- Other options we considered:
  - ".NET 5 (and .NET Core 2.1/3.1) and later versions" – the Core version numbers seem unnecessary and make the phrase longer than it needs to be.
  - ".NET 5 and later versions (formerly known as .NET Core)" -- could lead to confusion in that "5 and later" seems to exclude 2.1-3.1.
  - ".NET 5 and later versions (including .NET Core 2.1-3.1)" – similar issue in that 2.1-3.1 sounds they should be among the "later versions"
  - ".NET 5+" is a shorter alternative to ".NET 5 and later versions", but there are concerns that it would not be universally understood.
- ".NET 5 and later versions" will remain an accurate description after version 6 and later versions are released. But eventually ".NET" will be understood to mean 5+ and we may be able to eliminate "5 and later versions" in some contexts.

## Examples

### [Changes that affect compatibility](/dotnet/core/compatibility/)

| Before .NET 5 | Current recommendation |
| --- | --- |
| Throughout its history, .NET has attempted to maintain a high level of compatibility from version to version and across flavors of .NET. This continues to be true for .NET Core. Although .NET Core can be considered as a new technology that is independent of the .NET Framework, two major factors limit the ability of .NET Core to diverge from .NET Framework: | Throughout its history, .NET has attempted to maintain a high level of compatibility from version to version and across implementations of .NET. Although .NET 5 (and .NET Core) and later versions can be considered as a new technology compared to .NET Framework, two major factors limit the ability of this implementation of .NET to diverge from .NET Framework: |
| .NET Standard library projects allow developers to create libraries that target common APIs shared by .NET Core and .NET Framework | .NET Standard library projects allow developers to create libraries that target common APIs shared by .NET Framework and .NET 5 (and .NET Core) and later versions. |
| This article is not a complete list of breaking changes between .NET Framework and .NET Core. | This article is not a complete list of breaking changes in .NET 5 (and .NET Core) and later versions, compared to .NET Framework. |
| The following APIs will always throw a `PlatformNotSupportedException` on .NET Core. | The following APIs will always throw a `PlatformNotSupportedException` on .NET 5 (and .NET Core) and later versions. |

### [Install .NET on Windows](/dotnet/core/install/windows)

| Before .NET 5 | Current recommendation |
| --- | --- |
| Title/h1: Install .NET Core on Windows | Title/h1: Install .NET on Windows |
| In this article, you'll learn how to install .NET Core on Windows. .NET Core is made up of the runtime and the SDK. The runtime is used to run a .NET Core app and may or may not be included with the app. The SDK is used to create .NET Core apps and libraries. The .NET Core runtime is always installed with the SDK. | In this article, you'll learn how to install .NET 5 (and .NET Core) and later versions on Windows. .NET is made up of the runtime and the SDK. The runtime is used to run a .NET app and may or may not be included with the app. The SDK is used to create .NET apps and libraries. The .NET runtime is always installed with the SDK. |

### [How to check that .NET is already installed](/dotnet/core/install/how-to-detect-installed-versions)

| Before .NET 5 | Current recommendation |
| --- | --- |
| Title/h1: How to check that .NET Core is already installed | Title/h1: How to check that .NET is already installed |
| This article teaches you how to check which versions of the .NET Core runtime and SDK are installed on your computer. .NET core may have already been installed if you have an integrated development environment, such as Visual Studio or Visual Studio for Mac. | This article teaches you how to check which versions of the runtime and SDK for .NET 5 (and .NET Core) and later versions are installed on your computer. The runtime and SDK may have already been installed if you have an integrated development environment, such as Visual Studio or Visual Studio for Mac. |

### [Tutorial: Create a .NET console application using Visual Studio](/dotnet/core/tutorials/with-visual-studio)

| Before .NET 5 | Current recommendation |
| --- | --- |
| Title/h1: Tutorial: Create a .NET Core console application using Visual Studio | Title/h1: Tutorial: Create a .NET console application using Visual Studio |
| This tutorial shows how to create and run a .NET Core console application in Visual Studio 2019. | This tutorial shows how to create and run a .NET console application in Visual Studio 2019. |
| Prerequisites:Visual Studio 2019 version 16.6 or a later version with the .NET Core cross-platform development workload installed. The .NET Core 3.1 SDK is automatically installed when you select this workload. | PrerequisitesVisual Studio 2019 version 16.6 or a later version with the .NET cross-platform development workload installed. The .NET SDK is automatically installed when you select this workload. |


### [Tutorial: Create an item template](/dotnet/core/tutorials/cli-templates-create-item-template)

| Before .NET 5 | Current recommendation |
| --- | --- |
| Title/h1:Tutorial: Create an item template | Title/h1:Tutorial: Create an item template |
| With .NET Core, you can create and deploy templates that generate projects, files, even resources. | With .NET, you can create and deploy templates that generate projects, files, even resources. |
| Prerequisites: .NET Core 2.2 SDK or a later version. | Prerequisites: .NET Core 2.2 SDK or a later version (including .NET 5 and later versions). |

### [.NET SDK overview](/dotnet/core/sdk)

| Before .NET 5 | Current recommendation |
| --- | --- |
| Title/h1: .NET Core SDK overview | Title/h1: .NET SDK overview |
| "the SDK" in the text | no change |

### [.NET CLI overview](/dotnet/core/tools)

| Before .NET 5 | Current recommendation |
| --- | --- |
| Title/h1: .NET Core CLI overview | Title/h1: .NET CLI overview |
| The .NET Core command-line interface (CLI) is a cross-platform toolchain for developing, building, running, and publishing .NET Core applications. | The .NET command-line interface (CLI) is a cross-platform toolchain for developing, building, running, and publishing .NET applications. |

### [.NET application publishing overview](/dotnet/core/deploying/)

| Before .NET 5 | Current recommendation |
| --- | --- |
| Title/h1:.NET Core application publishing overview | Title/h1:.NET application publishing overview |
| Applications you create with .NET Core can be published in two different modes, and the mode affects how a user runs your app. | Applications you create with .NET 5 (and .NET Core) and later versions can be published in two different modes, and the mode affects how a user runs your app. |
| Publishing your app as self-contained produces an application that includes the .NET Core runtime and libraries, and your application and its dependencies. Users of the application can run it on a machine that doesn't have the .NET Core runtime installed. | Publishing your app as self-contained produces an application that includes the .NET runtime and libraries, and your application and its dependencies. Users of the application can run it on a machine that doesn't have the .NET runtime installed. |

### [dotnet new](/dotnet/core/tools/dotnet-new)

| Before .NET 5 | Current recommendation |
| --- | --- |
| **This article applies to:**  ✔️ .NET Core 2.1 SDK and later versions | **This article applies to:**  ✔️ .NET Core 2.1 SDK and later versions (including .NET 5 SDK and later versions) |
| **`--dry-run`** Displays a summary of what would happen if the given command were run if it would result in a template creation. Available since .NET Core 2.2 SDK. | no change (keep "Available since .NET Core 2.2 SDK") |

### "Applies to" link text in API ref docs

| Before .NET 5 | Current recommendation |
| --- | --- |
| \<exception cref="T:System.PlatformNotSupportedException"\>.NET Core only: In all cases\</exception\> | \<exception cref="T:System.PlatformNotSupportedException"\>.NET 5 (and .NET Core) and later versions: In all cases.\</exception\> |
