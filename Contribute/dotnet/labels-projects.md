---
title: 标签和项目路线图
description: 本文介绍了如何在 dotnet/docs 存储库中使用标签和项目。
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
ms.date: 03/24/2020
ms.openlocfilehash: 0dcac28db04378730b186c0f23064c1433d9f80e
ms.sourcegitcommit: bf2f4c7d9050b480d4db306df19d4c9f8714eff0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/07/2020
ms.locfileid: "80760367"
---
# <a name="labels-and-projects-roadmap"></a>标签和项目路线图

.NET 文档团队广泛使用 [ GitHub 标签](https://github.com/dotnet/docs/labels)来组织工作。 通过筛选标签的组合，我们可以快速关注 [.NET 文档网站](https://docs.microsoft.com/dotnet)上我们所需的部分。

我们还使用 [GitHub 项目](https://github.com/dotnet/docs/projects)来组织冲刺 (sprint) 和其他以目标为导向的长篇故事。

此路线图解释了我们如何使用这些组织工具，并提供一个用于查找所需领域的简便筛选器的链接。

## <a name="labels"></a>标签

如果这是你第一次体验参与[ dotnet/docs](https://github.com/dotnet/docs)，请从[ up-for-grabs ](https://github.com/dotnet/docs/labels/up-for-grabs)问题开始。 这些问题具有更集中的范围。 它们是你第一次参与的好方式。 从 up-for-grabs 视图中，你可以根据领域和优先级进一步筛选问题。 如果你第一次想尝试较小的参与，我们已经通过 [good-first-issue](https://github.com/dotnet/docs/labels/good-first-issue) 为初学者确定了好问题。

我们使用标签以许多不同的方式对问题进行分类：

- [.NET 指南](#find-a-single-net-guide)和[指南章节](#search-one-section-of-a-guide)。
- [目标版本](#releases)
- [优先级](#priority)

可以组合每个集合（指南、版本、优先级）的标签，以创建较小范围的重点来查找要处理的问题。

### <a name="find-a-single-net-guide"></a>查找单个 .NET 指南

我们将标签用于每个体系结构电子书和每个 .NET 指南。

![：书籍：浅绿色背景上的指南](./media/labels-projects/guide.png "体系结构指南标签的前缀")

体系结构电子书使用 `:book: guide` 前缀进行标注，并且具有浅绿色背景。 这些是涵盖推荐体系结构的长格式区域。 以下是针对每个 .NET 体系结构指南筛选的当前问题。

- [ASP.NET Core Web 应用](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20ASP.NET%20Core%20web%20apps)
- [Blazor](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Blazor)
- [云本机](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Cloud%20Native)
- [Docker 生命周期](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Docker%20lifecycle)
- [gRPC](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20gRPC)
- [通过 Windows 容器实现现代化](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Modernizing%20w%2F%20Windows%20containers)
- [.NET 微服务](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20.NET%20Microservices)
- [无服务器应用](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Serverless%20apps)

此标签样式也适用于[框架设计准则](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Framework%20Design%20Guidelines)。 此区域具有相同的标签设计，但不建议使用社区 PR。 这是经许可转载的材料，不应进行编辑。

![：书籍：深蓝色背景上的区域](./media/labels-projects/area.png ".NET 指南区域标签的前缀")

每个 .NET 指南都使用 `:books: Area` 前缀进行标注，并且具有深蓝色背景。 以下是针对每个 .NET 指南筛选的当前问题。

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

#### <a name="search-one-section-of-a-guide"></a>搜索指南的一个部分

![：card_file_box：中蓝色背景上的区域](./media/labels-projects/technology.png ".NET 指南子区域标签的前缀")

.NET 指南涵盖很多内容，因此这些标签会进一步限制指南的一个部分的范围。 每个 .NET 指南子区域都使用 `:card_file_box: Technology` 前缀进行标注，并且具有中蓝色背景。 其中许多标签适用于多个指南，而其他标签只位于一个指南中。 筛选区域后，添加其中一个标签以进一步限制问题的范围。

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

针对特定版本标记的问题使用 `:checkered_flag: Release:` 前缀标注，并具有深黄色背景。

- .NET Core 2.2
- .NET Core 3.0
- .NET Framework 4.8
- .NET 5

### <a name="priority"></a>优先级

优先级标签全部为 `P`，后跟单个数字。 较小的数字表示较高的优先级：

- P0
- P1
- P2
- P3

### <a name="what-about-the-other-labels"></a>其他标签呢？

内容团队还使用许多其他标签来管理问题的不同分类。 如果你不属于内容团队，则可以忽略这些其他标签。

## <a name="projects"></a>项目

我们通过两种方式使用项目：

- Month YYYY 项目类型：这些是每月工作计划的 Scrum 板。
- 长时间运行的长篇故事：这些用于在工作持续几个月的情况下组织以目标为导向的任务。
