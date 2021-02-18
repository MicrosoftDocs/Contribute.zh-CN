---
title: 标签、项目和里程碑路线图
description: 本文介绍了如何在 dotnet/docs 存储库中使用标签、项目和里程碑。
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
ms.date: 02/10/2021
ms.openlocfilehash: e053f09f7502cbe6f711488959de910298d3a456
ms.sourcegitcommit: f9a92d1cc70e46fae100dbc698e1d2196e0df7c6
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/13/2021
ms.locfileid: "100335732"
---
# <a name="labels-projects-and-milestones-roadmap"></a>标签、项目和里程碑路线图

.NET 文档团队广泛使用 [ GitHub 标签](https://github.com/dotnet/docs/labels)来组织工作。 通过筛选标签的组合，我们可以快速关注 [.NET 文档网站](https://docs.microsoft.com/dotnet)上我们所需的部分。 例如，我们可以通过查询 [is:issue is:open label:"dotnet-architecture/prod"](https://github.com/dotnet/docs/labels/dotnet-architecture%2Fprod) 筛选出有关体系结构指南的所有待解决问题。

我们使用 [GitHub 项目](https://github.com/dotnet/docs/projects)来组织冲刺 (sprint) 和其他以目标为导向的长篇故事。 我们还使用 [GitHub 里程碑](https://github.com/dotnet/docs/milestones)来跟踪工作。 最好考虑用于规划的项目（问题）和用于工作的里程碑（拉取请求）。

此路线图说明了我们使用这些组织工具的方式，并提供了用于查找感兴趣内容的便捷筛选器的链接。

## <a name="labels"></a>标签

如果这你是首次体验参与 [dotnet/docs](https://github.com/dotnet/docs)，请从[容易作答](https://github.com/dotnet/docs/labels/up-for-grabs)的问题开始。 这些问题针对的范围更加集中。 从此类问题入手是完成首次参与的好方式。 从“容易作答”视图中，你可以进一步根据区域和优先级筛选问题。 我们已使用 [good-first-issue](https://github.com/dotnet/docs/labels/good-first-issue) 标签标识出适合新手回答的问题，以便于你完成首次小小的参与。

我们使用标签以多种不同方式来分类问题：

- [.NET 指南](#find-issues-for-a-single-net-guide)和[指南章节](#find-issues-for-one-section-of-a-guide)。
- [目标版本](#releases)
- [Priority](#priority)

你可以合并每组（指南、版本、优先级）中的标签，以缩小关注范围，查找你想要解决的问题。

### <a name="find-issues-for-a-single-net-guide"></a>查找单个 .NET 指南的问题

我们针对各个体系结构电子书以及各个 .NET 指南使用标签。 所有电子书都注明了 [dotnet-architecture/prod](https://github.com/dotnet/docs/labels/dotnet-architecture%2Fprod) 标签。 每本书都具有以 `/tech` 结尾的唯一标签。

每个 .NET 指南都带有 [`/prod`](https://github.com/dotnet/docs/labels?q=prod) 后缀和蓝灰色背景。 以下是针对各个 .NET 指南筛选出的当前问题。

- [.NET 指南 - `dotnet/prod`](https://github.com/dotnet/docs/labels/dotnet%2Fprod)
- [.NET 基础指南（以前称为 .NET Standard 指南）- `dotnet-fundamentals/prod`](https://github.com/dotnet/docs/labels/dotnet-fundamentals%2Fprod)
- [.NET 基础指南（以前称为 .NET Core 指南）- `dotnet-core/prod`](https://github.com/dotnet/docs/labels/dotnet-core%2Fprod)
- [.NET Framework 指南 - `dotnet-framework/prod`](https://github.com/dotnet/docs/labels/dotnet-framework%2Fprod)
- [API 参考 - `dotnet-api/prod`](https://github.com/dotnet/docs/labels/dotnet-api%2Fprod)
- [C# 指南 - `dotnet-csharp/prod`](https://github.com/dotnet/docs/labels/dotnet-csharp%2Fprod)
- [F# 指南 - `dotnet-fsharp/prod`](https://github.com/dotnet/docs/labels/dotnet-fsharp%2Fprod)
- [Visual Basic 指南 - `dotnet-visualbasic/prod](https://github.com/dotnet/docs/labels/dotnet-visualbasic%2Fprod)
- [ML.NET 指南 - `dotnet-ml/prod`](https://github.com/dotnet/docs/labels/dotnet-ml%2Fprod)
- [Azure .NET SDK - `azure-dotnet/prod`](https://github.com/dotnet/docs/labels/azure-dotnet%2Fprod)
- [.NET for Apache Spark 指南 - `dotnet-spark/prod`](https://github.com/dotnet/docs/labels/dotnet-spark%2Fprod)
- [.NET 桌面指南 - `dotnet-desktop/prod`](https://github.com/dotnet/docs/labels/dotnet-desktop%2Fprod)

为跨存储库的区域定义了其他产品标签。

#### <a name="find-issues-for-one-section-of-a-guide"></a>查找指南某个部分的问题

.NET 指南范围较大，因此，这些标签按指南章节对范围做了进一步限制。 每个 .NET 指南子区域都带有 [`/tech`](https://github.com/dotnet/docs/labels?q=tech) 后缀和浅蓝色背景。 其中许多标签适用于多个指南，而有些标签仅适用于一个指南。 基于区域筛选后，添加其中一种标签，进一步限制问题的范围。

### <a name="releases"></a>版本

![：checkered_flag：版本：深黄色](./media/labels-projects/release.png "版本标签的前缀")

针对特定版本标记的问题使用 [`:checkered_flag: Release:`](https://github.com/dotnet/docs/labels?q=%3Acheckered_flag%3A+Release) 前缀标注，并具有深黄色背景。

### <a name="priority"></a>优先级

优先级标签由 `Pri` 及其后面的单个数字构成。 数字越小表示优先级越高：

- Pri0 - 严重优先级

  安全性问题或合规性所需的法律要求。 应放下所有其他方面来修复。
  
- Pri1 - 高优先级

  常见方案的要素。 或者高访问量文章上的明显错误。 在 P2 或 P3 起作用之前执行。
  
- Pri2 - 中优先级

  有助于常见方案，但不阻止。  快速简单地执行，或者在解决同一篇文章中 P1 问题时修复。
  
- Pri3 - 低优先级

  有助于边缘案例、常见案例的普通矫正、低访问量文章或弃用的技术。 不值得花费时间，但可供争取社区参与。 如果 P3 问题两个月后仍未解决，可关闭。

### <a name="what-about-the-other-labels"></a>其他标签呢

内容团队还使用了许多其他标签来管理各种问题分类。 如果你不属于内容团队，则可以忽略其他这些标签。

## <a name="projects"></a>项目

项目用于规划目的，在这种情况下，设置优先级的工作是通过看板自动完成的。 项目应仅包含 GitHub 问题，而不应包含拉取请求。 项目不同于里程碑，因为里程碑只包含拉取请求。

我们通过两种方式使用项目：

- `Month YYYY` 项目类型：这些是每月工作计划的看板。
  - 示例：[2020 年 7 月](https://github.com/dotnet/docs/projects/103)、[2020 年 8 月](https://github.com/dotnet/docs/projects/117)等。
- 长时间运行的长篇故事：这些用于在工作持续几个月的情况下组织以目标为导向的任务。
  - 示例：[.NET 5 Wave - 重组](https://github.com/dotnet/docs/projects/105)、[.NET 语言 (.NET 5 Wave)](https://github.com/dotnet/docs/projects/106) 等。

## <a name="milestones"></a>里程碑

里程碑通常遵循项目 `Month YYYY` 的相同命名约定，但不同于项目。 我们使用里程碑来跟踪已完成的工作。 里程碑应不包含问题（可能的工作），但仅包含拉取请求。 当前里程碑将自动应用于新的拉取请求。
