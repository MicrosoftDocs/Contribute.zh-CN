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
# <a name="labels-projects-and-milestones-roadmap"></a><span data-ttu-id="72161-103">标签、项目和里程碑路线图</span><span class="sxs-lookup"><span data-stu-id="72161-103">Labels, projects, and milestones roadmap</span></span>

<span data-ttu-id="72161-104">.NET 文档团队广泛使用 [ GitHub 标签](https://github.com/dotnet/docs/labels)来组织工作。</span><span class="sxs-lookup"><span data-stu-id="72161-104">The .NET docs team makes extensive use of [GitHub labels](https://github.com/dotnet/docs/labels) to organize our work.</span></span> <span data-ttu-id="72161-105">通过筛选标签的组合，我们可以快速关注 [.NET 文档网站](https://docs.microsoft.com/dotnet)上我们所需的部分。</span><span class="sxs-lookup"><span data-stu-id="72161-105">By filtering on combinations of labels, we can quickly focus on sections of interest on the [.NET docs website](https://docs.microsoft.com/dotnet).</span></span> <span data-ttu-id="72161-106">例如，我们可以筛选到 `P1` 通过查询 [is:issue is:open label:":books:Area - .NET Architecture Guide"](https://github.com/dotnet/docs/issues?q=is%3Aissue+is%3Aopen+label%3A%22%3Abooks%3A+Area+-+.NET+Architecture+Guide%22) 发出的所有开放优先级。</span><span class="sxs-lookup"><span data-stu-id="72161-106">For example, we could filter to all of the open priority one `P1` issues with a query to [is:issue is:open label:":books: Area - .NET Architecture Guide"](https://github.com/dotnet/docs/issues?q=is%3Aissue+is%3Aopen+label%3A%22%3Abooks%3A+Area+-+.NET+Architecture+Guide%22).</span></span>

<span data-ttu-id="72161-107">我们使用 [GitHub 项目](https://github.com/dotnet/docs/projects)来组织冲刺 (sprint) 和其他以目标为导向的长篇故事。</span><span class="sxs-lookup"><span data-stu-id="72161-107">We use [GitHub projects](https://github.com/dotnet/docs/projects) to organize sprints and other goal-oriented epics.</span></span> <span data-ttu-id="72161-108">我们还使用 [GitHub 里程碑](https://github.com/dotnet/docs/milestones)来跟踪工作。</span><span class="sxs-lookup"><span data-stu-id="72161-108">We also use [GitHub milestones](https://github.com/dotnet/docs/milestones) to track work.</span></span> <span data-ttu-id="72161-109">最好考虑用于规划的项目（问题）和用于工作的里程碑（拉取请求）。</span><span class="sxs-lookup"><span data-stu-id="72161-109">It is best to think of projects for planning (issues), and milestones for work (pull requests).</span></span>

<span data-ttu-id="72161-110">此路线图说明了我们使用这些组织工具的方式，并提供了用于查找感兴趣内容的便捷筛选器的链接。</span><span class="sxs-lookup"><span data-stu-id="72161-110">This roadmap explains how we use these organizational tools and has links to handy filters we use to find areas of interest.</span></span>

## <a name="labels"></a><span data-ttu-id="72161-111">标签</span><span class="sxs-lookup"><span data-stu-id="72161-111">Labels</span></span>

<span data-ttu-id="72161-112">如果这你是首次体验参与 [dotnet/docs](https://github.com/dotnet/docs)，请从[容易作答](https://github.com/dotnet/docs/labels/up-for-grabs)的问题开始。</span><span class="sxs-lookup"><span data-stu-id="72161-112">If this is your first experience contributing to [dotnet/docs](https://github.com/dotnet/docs), start with the [up-for-grabs](https://github.com/dotnet/docs/labels/up-for-grabs) issues.</span></span> <span data-ttu-id="72161-113">这些问题针对的范围更加集中。</span><span class="sxs-lookup"><span data-stu-id="72161-113">These are issues that have a more focused scope.</span></span> <span data-ttu-id="72161-114">从此类问题入手是完成首次参与的好方式。</span><span class="sxs-lookup"><span data-stu-id="72161-114">They are a great way to make your first contribution.</span></span> <span data-ttu-id="72161-115">从“容易作答”视图中，你可以进一步根据区域和优先级筛选问题。</span><span class="sxs-lookup"><span data-stu-id="72161-115">From the up-for-grabs view, you can further filter issues based on areas and priority.</span></span> <span data-ttu-id="72161-116">我们已使用 [good-first-issue](https://github.com/dotnet/docs/labels/good-first-issue) 标签标识出适合新手回答的问题，以便于你完成首次小小的参与。</span><span class="sxs-lookup"><span data-stu-id="72161-116">We've identified good issues for beginners with the [good-first-issue](https://github.com/dotnet/docs/labels/good-first-issue) if you want to try a smaller first contribution.</span></span>

<span data-ttu-id="72161-117">我们使用标签以多种不同方式来分类问题：</span><span class="sxs-lookup"><span data-stu-id="72161-117">We use labels to classify issues in many different ways:</span></span>

- <span data-ttu-id="72161-118">[.NET 指南](#find-a-single-net-guide)和[指南章节](#search-one-section-of-a-guide)。</span><span class="sxs-lookup"><span data-stu-id="72161-118">[.NET Guides](#find-a-single-net-guide) and [sections of a guide](#search-one-section-of-a-guide).</span></span>
- [<span data-ttu-id="72161-119">目标版本</span><span class="sxs-lookup"><span data-stu-id="72161-119">Target release</span></span>](#releases)
- [<span data-ttu-id="72161-120">Priority</span><span class="sxs-lookup"><span data-stu-id="72161-120">Priority</span></span>](#priority)

<span data-ttu-id="72161-121">你可以合并每组（指南、版本、优先级）中的标签，以缩小关注范围，查找你想要解决的问题。</span><span class="sxs-lookup"><span data-stu-id="72161-121">You can combine a label from each set (guide, release, priority) to create a narrow focus to find issues you want to work on.</span></span>

### <a name="find-a-single-net-guide"></a><span data-ttu-id="72161-122">查找单个 .NET 指南</span><span class="sxs-lookup"><span data-stu-id="72161-122">Find a single .NET guide</span></span>

<span data-ttu-id="72161-123">我们针对各个体系结构电子书以及各个 .NET 指南使用标签。</span><span class="sxs-lookup"><span data-stu-id="72161-123">We use labels for each of the architecture e-books and for each .NET Guide.</span></span>

<span data-ttu-id="72161-124">![:book: guide on light green background](./media/labels-projects/guide.png "体系结构指南标签的前缀")</span><span class="sxs-lookup"><span data-stu-id="72161-124">![:book: guide on light green background](./media/labels-projects/guide.png "Prefix for architecture guide labels")</span></span>

<span data-ttu-id="72161-125">体系结构电子书标有 `:book: guide` 前缀，并且使用浅绿色背景。</span><span class="sxs-lookup"><span data-stu-id="72161-125">Architecture e-books are noted with the `:book: guide` prefix and have a light green background.</span></span> <span data-ttu-id="72161-126">这些是长格式区域，其中包含推荐的体系结构。</span><span class="sxs-lookup"><span data-stu-id="72161-126">These are the long-form areas that cover recommended architecture.</span></span> <span data-ttu-id="72161-127">以下是针对各个 .NET 体系结构指南筛选出的当前问题。</span><span class="sxs-lookup"><span data-stu-id="72161-127">Here are current issues filtered for each of the .NET architecture guides.</span></span>

- [<span data-ttu-id="72161-128">ASP.NET Core Web 应用</span><span class="sxs-lookup"><span data-stu-id="72161-128">ASP.NET Core web apps</span></span>](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20ASP.NET%20Core%20web%20apps)
- [<span data-ttu-id="72161-129">Blazor</span><span class="sxs-lookup"><span data-stu-id="72161-129">Blazor</span></span>](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Blazor)
- [<span data-ttu-id="72161-130">云本机</span><span class="sxs-lookup"><span data-stu-id="72161-130">Cloud Native</span></span>](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Cloud%20Native)
- [<span data-ttu-id="72161-131">Docker 生命周期</span><span class="sxs-lookup"><span data-stu-id="72161-131">Docker lifecycle</span></span>](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Docker%20lifecycle)
- [<span data-ttu-id="72161-132">gRPC</span><span class="sxs-lookup"><span data-stu-id="72161-132">gRPC</span></span>](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20gRPC)
- [<span data-ttu-id="72161-133">通过 Windows 容器实现现代化</span><span class="sxs-lookup"><span data-stu-id="72161-133">Modernizing w/ Windows containers</span></span>](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Modernizing%20w%2F%20Windows%20containers)
- [<span data-ttu-id="72161-134">.NET 微服务</span><span class="sxs-lookup"><span data-stu-id="72161-134">.NET Microservices</span></span>](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20.NET%20Microservices)
- [<span data-ttu-id="72161-135">无服务器应用</span><span class="sxs-lookup"><span data-stu-id="72161-135">Serverless apps</span></span>](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Serverless%20apps)

<span data-ttu-id="72161-136">此标签样式也适用于 [Framework 设计准则](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Framework%20Design%20Guidelines)。</span><span class="sxs-lookup"><span data-stu-id="72161-136">This label style is also applied to the [Framework design guidelines](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Framework%20Design%20Guidelines).</span></span> <span data-ttu-id="72161-137">此区域使用相同的标签设计，但不建议对它执行社区拉取请求。</span><span class="sxs-lookup"><span data-stu-id="72161-137">This area has the same label design, but community PRs are discouraged.</span></span> <span data-ttu-id="72161-138">此为经许可后转载的材料，请勿进行编辑。</span><span class="sxs-lookup"><span data-stu-id="72161-138">This is material reprinted with permission and should not be edited.</span></span>

<span data-ttu-id="72161-139">![：书籍：深蓝色背景上的区域](./media/labels-projects/area.png ".NET 指南区域标签的前缀")</span><span class="sxs-lookup"><span data-stu-id="72161-139">![:books: Area on dark blue background](./media/labels-projects/area.png "Prefix for .NET Guide area labels")</span></span>

<span data-ttu-id="72161-140">每个 .NET 指南都标有 `:books: Area` 前缀，并且使用深蓝色背景。</span><span class="sxs-lookup"><span data-stu-id="72161-140">Each .NET Guide is noted with the `:books: Area` prefix and has a dark blue background.</span></span> <span data-ttu-id="72161-141">以下是针对各个 .NET 指南筛选出的当前问题。</span><span class="sxs-lookup"><span data-stu-id="72161-141">Here are current issues filtered for each of the .NET guides.</span></span>

- [<span data-ttu-id="72161-142">API 参考</span><span class="sxs-lookup"><span data-stu-id="72161-142">API Reference</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20API%20Reference)
- [<span data-ttu-id="72161-143">Azure .NET SDK</span><span class="sxs-lookup"><span data-stu-id="72161-143">Azure .NET SDK</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20Azure%20.NET%20SDk)
- [<span data-ttu-id="72161-144">C# 指南</span><span class="sxs-lookup"><span data-stu-id="72161-144">C# Guide</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20C%23%20Guide)
- [<span data-ttu-id="72161-145">桌面指南</span><span class="sxs-lookup"><span data-stu-id="72161-145">Desktop Guide</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20Desktop%20Guide)
- [<span data-ttu-id="72161-146">F# 指南</span><span class="sxs-lookup"><span data-stu-id="72161-146">F# Guide</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20F%23%20Guide)
- [<span data-ttu-id="72161-147">ML.NET 指南</span><span class="sxs-lookup"><span data-stu-id="72161-147">ML.NET Guide</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20ML.NET%20Guide)
- <span data-ttu-id="72161-148">[.NET 体系结构指南](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20Architecture%20Guide) - 可以删除</span><span class="sxs-lookup"><span data-stu-id="72161-148">[.NET Architecture Guide](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20Architecture%20Guide) - Could be removed</span></span>
- [<span data-ttu-id="72161-149">.NET Core 指南</span><span class="sxs-lookup"><span data-stu-id="72161-149">.NET Core Guide</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20Core%20Guide)
- [<span data-ttu-id="72161-150">.NET for Apache Spark 指南</span><span class="sxs-lookup"><span data-stu-id="72161-150">.NET for Apache Spark Guide</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20for%20Apache%20Spark%20Guide)
- [<span data-ttu-id="72161-151">.NET Framework 指南</span><span class="sxs-lookup"><span data-stu-id="72161-151">.NET Framework Guide</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20Framework%20Guide)
- [<span data-ttu-id="72161-152">.NET 指南</span><span class="sxs-lookup"><span data-stu-id="72161-152">.NET Guide</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20Guide)
- <span data-ttu-id="72161-153">[Roslyn API 参考](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20Roslyn%20API%20Reference) - 可以删除。</span><span class="sxs-lookup"><span data-stu-id="72161-153">[Roslyn API Reference](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20Roslyn%20API%20Reference) - could be removed.</span></span>
- [<span data-ttu-id="72161-154">Visual Basic 指南</span><span class="sxs-lookup"><span data-stu-id="72161-154">Visual Basic Guide</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20Visual%20Basic%20Guide)

#### <a name="search-one-section-of-a-guide"></a><span data-ttu-id="72161-155">搜索指南的某个章节</span><span class="sxs-lookup"><span data-stu-id="72161-155">Search one section of a guide</span></span>

<span data-ttu-id="72161-156">![：card_file_box：中蓝色背景上的区域](./media/labels-projects/technology.png ".NET 指南子区域标签的前缀")</span><span class="sxs-lookup"><span data-stu-id="72161-156">![:card_file_box: Area on medium blue background](./media/labels-projects/technology.png "Prefix for .NET Guide sub-area labels")</span></span>

<span data-ttu-id="72161-157">.NET 指南范围较大，因此，这些标签按指南章节对范围做了进一步限制。</span><span class="sxs-lookup"><span data-stu-id="72161-157">The .NET guides are large, so these labels further limit the scope by a section of a guide.</span></span> <span data-ttu-id="72161-158">每个 .NET 指南的子区域都标有 `:card_file_box: Technology` 前缀，并且使用中蓝色背景。</span><span class="sxs-lookup"><span data-stu-id="72161-158">Each .NET Guide subarea is noted with the `:card_file_box: Technology` prefix and has a medium blue background.</span></span> <span data-ttu-id="72161-159">其中许多标签适用于多个指南，而有些标签仅适用于一个指南。</span><span class="sxs-lookup"><span data-stu-id="72161-159">Many of these labels apply to multiple guides, while others are in only one guide.</span></span> <span data-ttu-id="72161-160">基于区域筛选后，添加其中一种标签，进一步限制问题的范围。</span><span class="sxs-lookup"><span data-stu-id="72161-160">After filtering on an area, add one of these labels to further limit the scope of issues.</span></span>

- <span data-ttu-id="72161-161">AppCompat</span><span class="sxs-lookup"><span data-stu-id="72161-161">AppCompat</span></span>
- <span data-ttu-id="72161-162">异步任务</span><span class="sxs-lookup"><span data-stu-id="72161-162">Async Task</span></span>
- <span data-ttu-id="72161-163">C# 高级概念</span><span class="sxs-lookup"><span data-stu-id="72161-163">C# Advanced concepts</span></span>
- <span data-ttu-id="72161-164">C# 编译器</span><span class="sxs-lookup"><span data-stu-id="72161-164">C# compiler</span></span>
- <span data-ttu-id="72161-165">C# 基础知识</span><span class="sxs-lookup"><span data-stu-id="72161-165">C# Fundamentals</span></span>
- <span data-ttu-id="72161-166">C# 入门</span><span class="sxs-lookup"><span data-stu-id="72161-166">C# Get Started</span></span>
- <span data-ttu-id="72161-167">C# 语言参考</span><span class="sxs-lookup"><span data-stu-id="72161-167">C# Language Reference</span></span>
- <span data-ttu-id="72161-168">C# Null 安全性</span><span class="sxs-lookup"><span data-stu-id="72161-168">C# Null safety</span></span>
- <span data-ttu-id="72161-169">C# 新增功能</span><span class="sxs-lookup"><span data-stu-id="72161-169">C# What's new</span></span>
- <span data-ttu-id="72161-170">CLI</span><span class="sxs-lookup"><span data-stu-id="72161-170">CLI</span></span>
- <span data-ttu-id="72161-171">数据访问</span><span class="sxs-lookup"><span data-stu-id="72161-171">Data Access</span></span>
- <span data-ttu-id="72161-172">Docker</span><span class="sxs-lookup"><span data-stu-id="72161-172">Docker</span></span>
- <span data-ttu-id="72161-173">安装程序</span><span class="sxs-lookup"><span data-stu-id="72161-173">Installers</span></span>
- <span data-ttu-id="72161-174">LINQ</span><span class="sxs-lookup"><span data-stu-id="72161-174">LINQ</span></span>
- <span data-ttu-id="72161-175">NCL</span><span class="sxs-lookup"><span data-stu-id="72161-175">NCL</span></span>
- <span data-ttu-id="72161-176">.NET Standard</span><span class="sxs-lookup"><span data-stu-id="72161-176">.NET Standard</span></span>
- <span data-ttu-id="72161-177">Roslyn API</span><span class="sxs-lookup"><span data-stu-id="72161-177">Roslyn APIs</span></span>
- <span data-ttu-id="72161-178">安全性</span><span class="sxs-lookup"><span data-stu-id="72161-178">Security</span></span>
- <span data-ttu-id="72161-179">WCF</span><span class="sxs-lookup"><span data-stu-id="72161-179">WCF</span></span>
- <span data-ttu-id="72161-180">WF</span><span class="sxs-lookup"><span data-stu-id="72161-180">WF</span></span>
- <span data-ttu-id="72161-181">WIF</span><span class="sxs-lookup"><span data-stu-id="72161-181">WIF</span></span>
- <span data-ttu-id="72161-182">WinForms</span><span class="sxs-lookup"><span data-stu-id="72161-182">WinForms</span></span>
- <span data-ttu-id="72161-183">WPF</span><span class="sxs-lookup"><span data-stu-id="72161-183">WPF</span></span>

### <a name="releases"></a><span data-ttu-id="72161-184">版本</span><span class="sxs-lookup"><span data-stu-id="72161-184">Releases</span></span>

<span data-ttu-id="72161-185">![：checkered_flag：版本：深黄色](./media/labels-projects/release.png "版本标签的前缀")</span><span class="sxs-lookup"><span data-stu-id="72161-185">![:checkered_flag: Release: on dark yellow](./media/labels-projects/release.png "Prefix for release labels")</span></span>

<span data-ttu-id="72161-186">针对特定版本标记的问题标有 `:checkered_flag: Release:` 前缀，并且使用深黄色背景。</span><span class="sxs-lookup"><span data-stu-id="72161-186">Issues tagged for a specific release are noted with the `:checkered_flag: Release:` prefix and have a dark yellow background.</span></span>

- <span data-ttu-id="72161-187">.NET Core 2.2</span><span class="sxs-lookup"><span data-stu-id="72161-187">.NET Core 2.2</span></span>
- <span data-ttu-id="72161-188">.NET Core 3.0</span><span class="sxs-lookup"><span data-stu-id="72161-188">.NET Core 3.0</span></span>
- <span data-ttu-id="72161-189">.NET Framework 4.8</span><span class="sxs-lookup"><span data-stu-id="72161-189">.NET Framework 4.8</span></span>
- <span data-ttu-id="72161-190">.NET 5</span><span class="sxs-lookup"><span data-stu-id="72161-190">.NET 5</span></span>

### <a name="priority"></a><span data-ttu-id="72161-191">优先级</span><span class="sxs-lookup"><span data-stu-id="72161-191">Priority</span></span>

<span data-ttu-id="72161-192">优先级标签由 `P` 及其后面的单个数字构成。</span><span class="sxs-lookup"><span data-stu-id="72161-192">Priority labels are all `P` followed by a single digit.</span></span> <span data-ttu-id="72161-193">数字越小表示优先级越高：</span><span class="sxs-lookup"><span data-stu-id="72161-193">Lower numbers are higher priority:</span></span>

- <span data-ttu-id="72161-194">P0 - 严重优先级</span><span class="sxs-lookup"><span data-stu-id="72161-194">P0 - Critical priority</span></span>

  <span data-ttu-id="72161-195">安全性问题或合规性所需的法律要求。</span><span class="sxs-lookup"><span data-stu-id="72161-195">Security issue or legally required for compliance.</span></span> <span data-ttu-id="72161-196">应放下所有其他方面来修复。</span><span class="sxs-lookup"><span data-stu-id="72161-196">We drop everything else to fix.</span></span>
  
- <span data-ttu-id="72161-197">P1 - 高优先级</span><span class="sxs-lookup"><span data-stu-id="72161-197">P1 - High priority</span></span>

  <span data-ttu-id="72161-198">常见方案的要素。</span><span class="sxs-lookup"><span data-stu-id="72161-198">Essential for common scenarios.</span></span> <span data-ttu-id="72161-199">或者高访问量文章上的明显错误。</span><span class="sxs-lookup"><span data-stu-id="72161-199">Or highly visible error on high page view article.</span></span> <span data-ttu-id="72161-200">在 P2 或 P3 起作用之前执行。</span><span class="sxs-lookup"><span data-stu-id="72161-200">We do these before P2 or P3 work.</span></span>
  
- <span data-ttu-id="72161-201">P2 - 中优先级</span><span class="sxs-lookup"><span data-stu-id="72161-201">P2 - Medium priority</span></span>

  <span data-ttu-id="72161-202">有助于常见方案，但不阻止。</span><span class="sxs-lookup"><span data-stu-id="72161-202">Helpful for common scenarios but not blocking.</span></span>  <span data-ttu-id="72161-203">快速简单地执行，或者在解决同一篇文章中 P1 问题时修复。</span><span class="sxs-lookup"><span data-stu-id="72161-203">We do these if quick and easy, or fit them in while addressing a P1 issue in the same article.</span></span>
  
- <span data-ttu-id="72161-204">P3 - 低优先级</span><span class="sxs-lookup"><span data-stu-id="72161-204">P3 - Low priority</span></span>

  <span data-ttu-id="72161-205">有助于边缘案例、常见案例的普通矫正、低访问量文章或弃用的技术。</span><span class="sxs-lookup"><span data-stu-id="72161-205">Helpful for edge cases, trivial corrections for common scenarios, low page view article, or deprecated technology.</span></span> <span data-ttu-id="72161-206">不值得花费时间，但可供争取社区参与。</span><span class="sxs-lookup"><span data-stu-id="72161-206">Not worth our time but up for grabs for community contribution.</span></span> <span data-ttu-id="72161-207">如果 P3 问题两个月后仍未解决，可关闭。</span><span class="sxs-lookup"><span data-stu-id="72161-207">A P3 issue may be closed if not addressed after two months.</span></span>

### <a name="what-about-the-other-labels"></a><span data-ttu-id="72161-208">其他标签呢</span><span class="sxs-lookup"><span data-stu-id="72161-208">What about the other labels</span></span>

<span data-ttu-id="72161-209">内容团队还使用了许多其他标签来管理各种问题分类。</span><span class="sxs-lookup"><span data-stu-id="72161-209">There are many other labels used by the content teams to manage different classifications of issues.</span></span> <span data-ttu-id="72161-210">如果你不属于内容团队，则可以忽略其他这些标签。</span><span class="sxs-lookup"><span data-stu-id="72161-210">If you're not on the content team, you can ignore these other labels.</span></span>

## <a name="projects"></a><span data-ttu-id="72161-211">项目</span><span class="sxs-lookup"><span data-stu-id="72161-211">Projects</span></span>

<span data-ttu-id="72161-212">项目用于规划目的，在这种情况下，设置优先级的工作是通过看板自动完成的。</span><span class="sxs-lookup"><span data-stu-id="72161-212">Projects are intended for planning purposes, where prioritized work is automated through a Kanban board.</span></span> <span data-ttu-id="72161-213">项目应仅包含 GitHub 问题，而不应包含拉取请求。</span><span class="sxs-lookup"><span data-stu-id="72161-213">Projects should only ever contain GitHub issues, _not_ pull requests.</span></span> <span data-ttu-id="72161-214">项目不同于里程碑，因为里程碑只包含拉取请求。</span><span class="sxs-lookup"><span data-stu-id="72161-214">Projects differ from milestones, in that milestones only contain pull requests.</span></span>

<span data-ttu-id="72161-215">我们通过两种方式使用项目：</span><span class="sxs-lookup"><span data-stu-id="72161-215">We use projects in two ways:</span></span>

- <span data-ttu-id="72161-216">`Month YYYY` 项目类型：这些是每月工作计划的看板。</span><span class="sxs-lookup"><span data-stu-id="72161-216">`Month YYYY` project types: These are Kanban boards for each month's working plan.</span></span>
  - <span data-ttu-id="72161-217">示例：[2020 年 7 月](https://github.com/dotnet/docs/projects/103)、[2020 年 8 月](https://github.com/dotnet/docs/projects/117)等。</span><span class="sxs-lookup"><span data-stu-id="72161-217">Examples, [July 2020](https://github.com/dotnet/docs/projects/103), [August 2020](https://github.com/dotnet/docs/projects/117), and so on.</span></span>
- <span data-ttu-id="72161-218">长时间运行的长篇故事：这些用于在工作持续几个月的情况下组织以目标为导向的任务。</span><span class="sxs-lookup"><span data-stu-id="72161-218">Long-running epics: These are used to organize tasks toward a goal when the work will occur over several months.</span></span>
  - <span data-ttu-id="72161-219">示例：[.NET 5 Wave - 重组](https://github.com/dotnet/docs/projects/105)、[.NET 语言 (.NET 5 Wave)](https://github.com/dotnet/docs/projects/106) 等。</span><span class="sxs-lookup"><span data-stu-id="72161-219">Examples: [.NET 5 Wave - Reorganization](https://github.com/dotnet/docs/projects/105), [.NET Languages (.NET 5 wave) ](https://github.com/dotnet/docs/projects/106), and so on.</span></span>

## <a name="milestones"></a><span data-ttu-id="72161-220">里程碑</span><span class="sxs-lookup"><span data-stu-id="72161-220">Milestones</span></span>

<span data-ttu-id="72161-221">里程碑通常遵循项目 `Month YYYY` 的相同命名约定，但不同于项目。</span><span class="sxs-lookup"><span data-stu-id="72161-221">Milestones typically follow the same naming convention of projects `Month YYYY`, but they're different from projects.</span></span> <span data-ttu-id="72161-222">我们使用里程碑来跟踪已完成的工作。</span><span class="sxs-lookup"><span data-stu-id="72161-222">We use milestones to track completed work.</span></span> <span data-ttu-id="72161-223">里程碑应不包含问题（可能的工作），但仅包含拉取请求。</span><span class="sxs-lookup"><span data-stu-id="72161-223">Milestones should _not_ contain issues (potential work), but rather exclusively contain pull requests.</span></span> <span data-ttu-id="72161-224">当前里程碑将自动应用于新的拉取请求。</span><span class="sxs-lookup"><span data-stu-id="72161-224">The current milestone is automatically applied to new pull requests.</span></span>
