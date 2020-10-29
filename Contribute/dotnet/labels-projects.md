---
title: 标签、项目和里程碑路线图
description: 本文介绍了如何在 dotnet/docs 存储库中使用标签、项目和里程碑。
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
ms.date: 08/06/2020
ms.openlocfilehash: 059ed8297956589a281cf11e4f7244e972565160
ms.sourcegitcommit: 11228bd1d3dc1496820355096453f1eb2d28b33e
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/24/2020
ms.locfileid: "92523461"
---
# <a name="labels-projects-and-milestones-roadmap"></a>标签、项目和里程碑路线图

.NET 文档团队广泛使用 [ GitHub 标签](https://github.com/dotnet/docs/labels)来组织工作。 通过筛选标签的组合，我们可以快速关注 [.NET 文档网站](https://docs.microsoft.com/dotnet)上我们所需的部分。 例如，我们可以筛选到 `P1` 通过查询 [is:issue is:open label:":books:Area - .NET Architecture Guide"](https://github.com/dotnet/docs/issues?q=is%3Aissue+is%3Aopen+label%3A%22%3Abooks%3A+Area+-+.NET+Architecture+Guide%22) 发出的所有开放优先级。

我们使用 [GitHub 项目](https://github.com/dotnet/docs/projects)来组织冲刺 (sprint) 和其他以目标为导向的长篇故事。 我们还使用 [GitHub 里程碑](https://github.com/dotnet/docs/milestones)来跟踪工作。 最好考虑用于规划的项目（问题）和用于工作的里程碑（拉取请求）。

此路线图说明了我们使用这些组织工具的方式，并提供了用于查找感兴趣内容的便捷筛选器的链接。

## <a name="labels"></a>标签

如果这你是首次体验参与 [dotnet/docs](https://github.com/dotnet/docs)，请从[容易作答](https://github.com/dotnet/docs/labels/up-for-grabs)的问题开始。 这些问题针对的范围更加集中。 从此类问题入手是完成首次参与的好方式。 从“容易作答”视图中，你可以进一步根据区域和优先级筛选问题。 我们已使用 [good-first-issue](https://github.com/dotnet/docs/labels/good-first-issue) 标签标识出适合新手回答的问题，以便于你完成首次小小的参与。

我们使用标签以多种不同方式来分类问题：

- [.NET 指南](#find-a-single-net-guide)和[指南章节](#search-one-section-of-a-guide)。
- [目标版本](#releases)
- [Priority](#priority)

你可以合并每组（指南、版本、优先级）中的标签，以缩小关注范围，查找你想要解决的问题。

### <a name="find-a-single-net-guide"></a>查找单个 .NET 指南

我们针对各个体系结构电子书以及各个 .NET 指南使用标签。

![:book: guide on light green background](./media/labels-projects/guide.png "体系结构指南标签的前缀")

体系结构电子书标有 `:book: guide` 前缀，并且使用浅绿色背景。 这些是长格式区域，其中包含推荐的体系结构。 以下是针对各个 .NET 体系结构指南筛选出的当前问题。

- [ASP.NET Core Web 应用](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20ASP.NET%20Core%20web%20apps)
- [Blazor](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Blazor)
- [云本机](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Cloud%20Native)
- [Docker 生命周期](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Docker%20lifecycle)
- [gRPC](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20gRPC)
- [通过 Windows 容器实现现代化](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Modernizing%20w%2F%20Windows%20containers)
- [.NET 微服务](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20.NET%20Microservices)
- [无服务器应用](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Serverless%20apps)

此标签样式也适用于 [Framework 设计准则](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Framework%20Design%20Guidelines)。 此区域使用相同的标签设计，但不建议对它执行社区拉取请求。 此为经许可后转载的材料，请勿进行编辑。

![：书籍：深蓝色背景上的区域](./media/labels-projects/area.png ".NET 指南区域标签的前缀")

每个 .NET 指南都标有 `:books: Area` 前缀，并且使用深蓝色背景。 以下是针对各个 .NET 指南筛选出的当前问题。

- [API 参考](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20API%20Reference)
- [Azure .NET SDK](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20Azure%20.NET%20SDk)
- [C# 指南](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20C%23%20Guide)
- [桌面指南](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20Desktop%20Guide)
- [F# 指南](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20F%23%20Guide)
- [ML.NET 指南](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20ML.NET%20Guide)
- [.NET 体系结构指南](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20Architecture%20Guide) - 可以删除
- [.NET Core 指南](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20Core%20Guide)
- [.NET for Apache Spark 指南](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20for%20Apache%20Spark%20Guide)
- [.NET Framework 指南](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20Framework%20Guide)
- [.NET 指南](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20Guide)
- [Roslyn API 参考](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20Roslyn%20API%20Reference) - 可以删除。
- [Visual Basic 指南](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20Visual%20Basic%20Guide)

#### <a name="search-one-section-of-a-guide"></a>搜索指南的某个章节

![：card_file_box：中蓝色背景上的区域](./media/labels-projects/technology.png ".NET 指南子区域标签的前缀")

.NET 指南范围较大，因此，这些标签按指南章节对范围做了进一步限制。 每个 .NET 指南的子区域都标有 `:card_file_box: Technology` 前缀，并且使用中蓝色背景。 其中许多标签适用于多个指南，而有些标签仅适用于一个指南。 基于区域筛选后，添加其中一种标签，进一步限制问题的范围。

- AppCompat
- 异步任务
- C# 高级概念
- C# 编译器
- C# 基础知识
- C# 入门
- C# 语言参考
- C# Null 安全性
- C# 新增功能
- CLI
- 数据访问
- Docker
- 安装程序
- LINQ
- NCL
- .NET Standard
- Roslyn API
- 安全性
- WCF
- WF
- WIF
- WinForms
- WPF

### <a name="releases"></a>版本

![：checkered_flag：版本：深黄色](./media/labels-projects/release.png "版本标签的前缀")

针对特定版本标记的问题标有 `:checkered_flag: Release:` 前缀，并且使用深黄色背景。

- .NET Core 2.2
- .NET Core 3.0
- .NET Framework 4.8
- .NET 5

### <a name="priority"></a>优先级

优先级标签由 `P` 及其后面的单个数字构成。 数字越小表示优先级越高：

- P0 - 严重优先级

  安全性问题或合规性所需的法律要求。 应放下所有其他方面来修复。
  
- P1 - 高优先级

  常见方案的要素。 或者高访问量文章上的明显错误。 在 P2 或 P3 起作用之前执行。
  
- P2 - 中优先级

  有助于常见方案，但不阻止。  快速简单地执行，或者在解决同一篇文章中 P1 问题时修复。
  
- P3 - 低优先级

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
