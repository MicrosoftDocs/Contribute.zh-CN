---
title: 如何在文档中引用 .NET
description: 了解如何在文档中引用 .NET Core、.NET 5 及更高版本。
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
ms.date: 01/28/2021
ms.openlocfilehash: 102c782215ea6daa033b4fa4e996d89cf587c86b
ms.sourcegitcommit: ac9c26c336b6886b6970e8d85b1e79faad0db4b8
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/02/2021
ms.locfileid: "99477320"
---
# <a name="how-to-refer-to-net-in-docs"></a>如何在文档中引用 .NET

## <a name="recommended-terminology"></a>建议的术语

**在文档标题和第一个标题 (h1) 中：**

- “.NET”（不提及 5 或 Core）

**文章文本中的第一个引用：**

- “.NET”，用于有关 Core/5+ 的文档，这些文档向 .NET 的新用户提供。
- “.NET 5（和 .NET Core）及更高版本”，如果需要强调 Core/5+ 是特定的 .NET 实现。

**后续引用：**

- “.NET”，用于向 .NET 新用户提供 Core/5+ 或上下文中对 Core/5+ 的引用清晰的情况。
- “.NET 5 和更高版本”，用于需要将 Core/5+ 与其他 .NET 实现区分开的情况。

**注意：**

- 我们考虑的其他选项：
  - “.NET 5（和 .NET Core 2.1/3.1）以及更高版本”- Core 版本号似乎没有必要，它使短语的长度超过必要的长度。
  - “.NET 5 和更高版本（以前称为 .NET Core）”--可能导致理解混淆，因为“5 和更高版本”似乎不包括 2.1-3.1。
  - “.NET 5 和更高版本（包括 .NET Core 2.1-3.1）” - 类似问题，因为 2.1-3.1 听起来应该在“更高版本”中
  - “.NET 5+”是“.NET 5 和更高版本”的较短的替代表达，但有人担心并非所有人都能理解这种表达。
- 版本 6 和更高版本发布后，“.NET 5 和更高版本”仍将是准确的表述。 但最终人们会理解“.NET”表示 5+，我们也许可以在某些上下文中移除“5 和更高版本”。

## <a name="examples"></a>示例

### <a name="changes-that-affect-compatibility"></a>[会影响兼容性的变更](/dotnet/core/compatibility/)

| 在 .NET 5 前 | 当前建议 |
| --- | --- |
| 在 .NET 的整个历史记录中，它都尝试在版本之间以及 .NET 各个风格之间保持高级别的兼容性。 .NET Core 将继续坚守这个准则。 尽管可以将 .NET Core 视为独立于 .NET Framework 的新技术，但下面的两个因素使 .NET Core 无法脱离 .NET Framework： | 在 .NET 的整个历史记录中，它都尝试在版本之间以及 .NET 各个实现之间保持高级别的兼容性。 与 .NET Framework 相比，尽管可以将 .NET 5（和 .NET Core）以及更高版本视为一种新技术，但下面的两个因素使 .NET 的此种实现无法脱离 .NET Framework： |
| .NET Standard 库项目允许开发人员创建面向 .NET Core 和 .NET Framework 共享的通用 API 的库 | .NET Standard 库项目允许开发人员创建面向 .NET 5（和 .NET Core）以及更高版本和 .NET Framework 共享的通用 API 的库。 |
| 本文不是 .NET Framework 与 .NET Core 之间的中断性变更的完整列表。 | 与 .NET Framework 相比，本文不是 .NET 5（和 .NET Core）及更高版本中的中断性变更的完整列表。 |
| 以下 API 将始终对 .NET Core 引发 `PlatformNotSupportedException`。 | 以下 API 将始终对 .NET 5（和 .NET Core）及更高版本引发 `PlatformNotSupportedException`。 |

### <a name="install-net-on-windows"></a>[在 Windows 上安装 .NET](/dotnet/core/install/windows)

| 在 .NET 5 前 | 当前建议 |
| --- | --- |
| Title/h1：在 Windows 上安装 .NET Core | Title/h1：在 Windows 上安装 .NET |
| 在本文中，你将了解如何在 Windows 上安装 .NET Core。 .NET Core 由运行时和 SDK 组成。 运行时用于运行 .NET Core 应用，应用可能包含也可能不包含它。 SDK 用于创建 .NET Core 应用和库。 .NET Core 运行时始终随 SDK 一起安装。 | 本文介绍如何在 Windows 上安装 .NET 5（和 .NET Core）及更高版本。 .NET 由运行时和 SDK 组成。 运行时用于运行 .NET 应用，应用可能包含也可能不包含它。 SDK 用于创建 .NET 应用和库。 .NET 运行时始终随 SDK 一起安装。 |

### <a name="how-to-check-that-net-is-already-installed"></a>[如何检查是否已安装 .NET](/dotnet/core/install/how-to-detect-installed-versions)

| 在 .NET 5 前 | 当前建议 |
| --- | --- |
| Title/h1：如何检查是否已安装 .NET Core | Title/h1：如何检查是否已安装 .NET |
| 本文介绍如何检查计算机上安装的 .NET Core 运行时和 SDK 的版本。 如果你拥有一个集成开发环境（如 Visual Studio 或 Visual Studio for Mac），则可能已安装 .NET core。 | 本文介绍如何检查计算机上安装的适用于 .NET 5（和 .NET Core）及更高版本的进行时和 SDK 是什么版本。 如果你拥有一个集成开发环境（如 Visual Studio 或 Visual Studio for Mac），则可能已安装运行时和 SDK。 |

### <a name="tutorial-create-a-net-console-application-using-visual-studio"></a>[教程：使用 Visual Studio 创建 .NET 控制台应用程序](/dotnet/core/tutorials/with-visual-studio)

| 在 .NET 5 前 | 当前建议 |
| --- | --- |
| Title/h1：教程：使用 Visual Studio 创建 .NET Core 控制台应用程序 | Title/h1：教程：使用 Visual Studio 创建 .NET 控制台应用程序 |
| 本教程演示如何在 Visual Studio 2019 中创建和运行 .NET Core 控制台应用程序。 | 本教程演示如何在 Visual Studio 2019 中创建和运行 .NET 控制台应用程序。 |
| 先决条件：安装了具有“.NET Core 跨平台开发”工作负载的 Visual Studio 2019 版本 16.6 或更高版本。 选择此工作负载时，将自动安装 .NET Core 3.1 SDK。 | 先决条件：安装了具有“.NET 跨平台开发”工作负载的 Visual Studio 2019 版本 16.6 或更高版本。 选择此工作负载时，将自动安装 .NET SDK。 |


### <a name="tutorial-create-an-item-template"></a>[教程：创建项模板](/dotnet/core/tutorials/cli-templates-create-item-template)

| 在 .NET 5 前 | 当前建议 |
| --- | --- |
| Title/h1：教程：创建项模板 | Title/h1：教程：创建项模板 |
| 使用 .NET Core，可以创建和部署可生成项目、文件甚至资源的模板。 | 使用 .NET，可以创建和部署可生成项目、文件甚至资源的模板。 |
| 先决条件：.NET Core 2.2 SDK 或更高版本。 | 先决条件：.NET Core 2.2 SDK 或更高版本（包括.NET 5 和更高版本）。 |

### <a name="net-sdk-overview"></a>[.NET SDK 概述](/dotnet/core/sdk)

| 在 .NET 5 前 | 当前建议 |
| --- | --- |
| Title/h1：.NET Core SDK 概述 | Title/h1：.NET SDK 概述 |
| 文本中的“SDK” | 无更改 |

### <a name="net-cli-overview"></a>[.NET CLI 概述](/dotnet/core/tools)

| 在 .NET 5 前 | 当前建议 |
| --- | --- |
| Title/h1：.NET Core CLI 概述 | Title/h1：.NET CLI 概述 |
| .NET Core 命令行接口 (CLI) 工具是用于开发、生成、运行和发布 .NET Core 应用程序的跨平台工具链。 | .NET 命令行接口 (CLI) 工具是用于开发、生成、运行和发布 .NET 应用程序的跨平台工具链。 |

### <a name="net-application-publishing-overview"></a>[.NET 应用程序发布概述](/dotnet/core/deploying/)

| 在 .NET 5 前 | 当前建议 |
| --- | --- |
| Title/h1：.NET Core 应用程序发布概述 | Title/h1：.NET 应用程序发布概述 |
| 可在两种模式下发布使用 .NET Core 创建的应用程序，模式会影响用户运行应用的方式。 | 可在两种模式下发布使用 .NET 5（和 .NET Core）及更高版本创建的应用程序，模式会影响用户运行应用的方式。 |
| 将应用作为独立应用，生成的应用程序将包含 .NET Core 运行时和库，以及该应用程序及其依赖项。 应用程序的用户可以在未安装 .NET Core 运行时的计算机上运行该应用程序。 | 将应用作为独立应用，生成的应用程序将包含 .NET 运行时和库，以及该应用程序及其依赖项。 应用程序的用户可以在未安装 .NET 运行时的计算机上运行该应用程序。 |

### <a name="dotnet-new"></a>[dotnet new](/dotnet/core/tools/dotnet-new)

| 在 .NET 5 前 | 当前建议 |
| --- | --- |
| 本文适用于：✔️ .NET Core 2.1 SDK 和更高版本 | 本文适用于：✔️ .NET Core 2.1 SDK 和更高版本（包括 .NET 5 SDK 和更高版本） |
| **`--dry-run`** 显示有关以下内容的摘要：给定命令运行导致模板创建时发生的情况。 自 .NET Core 2.2 SDK 起可用。 | 无更改（保留“从 .NET Core 2.2 SDK 开始可用”） |

### <a name="applies-to-link-text-in-api-ref-docs"></a>API 参考文档中的“适用于”链接文本

| 在 .NET 5 前 | 当前建议 |
| --- | --- |
| \<exception cref="T:System.PlatformNotSupportedException"\>仅限 .NET Core：在所有情况下\</exception\> | \<exception cref="T:System.PlatformNotSupportedException"\>.NET 5（和 .NET Core）及更高版本：在所有情况下。\</exception\> |
