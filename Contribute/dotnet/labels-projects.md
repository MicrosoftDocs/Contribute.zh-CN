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
# <a name="labels-and-projects-roadmap"></a><span data-ttu-id="4850b-103">标签和项目路线图</span><span class="sxs-lookup"><span data-stu-id="4850b-103">Labels and projects roadmap</span></span>

<span data-ttu-id="4850b-104">.NET 文档团队广泛使用 [ GitHub 标签](https://github.com/dotnet/docs/labels)来组织工作。</span><span class="sxs-lookup"><span data-stu-id="4850b-104">The .NET docs team makes extensive use of [GitHub labels](https://github.com/dotnet/docs/labels) to organize our work.</span></span> <span data-ttu-id="4850b-105">通过筛选标签的组合，我们可以快速关注 [.NET 文档网站](https://docs.microsoft.com/dotnet)上我们所需的部分。</span><span class="sxs-lookup"><span data-stu-id="4850b-105">By filtering on combinations of labels, we can quickly focus on sections of interest on the [.NET docs website](https://docs.microsoft.com/dotnet).</span></span>

<span data-ttu-id="4850b-106">我们还使用 [GitHub 项目](https://github.com/dotnet/docs/projects)来组织冲刺 (sprint) 和其他以目标为导向的长篇故事。</span><span class="sxs-lookup"><span data-stu-id="4850b-106">We also use [GitHub projects](https://github.com/dotnet/docs/projects) to organize sprints and other goal-oriented epics.</span></span>

<span data-ttu-id="4850b-107">此路线图解释了我们如何使用这些组织工具，并提供一个用于查找所需领域的简便筛选器的链接。</span><span class="sxs-lookup"><span data-stu-id="4850b-107">This roadmap explains how we use these organizational tools and has links to handy filters we use to find areas of interest.</span></span>

## <a name="labels"></a><span data-ttu-id="4850b-108">标签</span><span class="sxs-lookup"><span data-stu-id="4850b-108">Labels</span></span>

<span data-ttu-id="4850b-109">如果这是你第一次体验参与[ dotnet/docs](https://github.com/dotnet/docs)，请从[ up-for-grabs ](https://github.com/dotnet/docs/labels/up-for-grabs)问题开始。</span><span class="sxs-lookup"><span data-stu-id="4850b-109">If this is your first experience contributing to [dotnet/docs](https://github.com/dotnet/docs), start with the [up-for-grabs](https://github.com/dotnet/docs/labels/up-for-grabs) issues.</span></span> <span data-ttu-id="4850b-110">这些问题具有更集中的范围。</span><span class="sxs-lookup"><span data-stu-id="4850b-110">These are issues that have a more focused scope.</span></span> <span data-ttu-id="4850b-111">它们是你第一次参与的好方式。</span><span class="sxs-lookup"><span data-stu-id="4850b-111">They are a great way to make your first contribution.</span></span> <span data-ttu-id="4850b-112">从 up-for-grabs 视图中，你可以根据领域和优先级进一步筛选问题。</span><span class="sxs-lookup"><span data-stu-id="4850b-112">From the up-for-grabs view, you can further filter issues based on areas and priority.</span></span> <span data-ttu-id="4850b-113">如果你第一次想尝试较小的参与，我们已经通过 [good-first-issue](https://github.com/dotnet/docs/labels/good-first-issue) 为初学者确定了好问题。</span><span class="sxs-lookup"><span data-stu-id="4850b-113">We've identified good issues for beginners with the [good-first-issue](https://github.com/dotnet/docs/labels/good-first-issue) if you want to try a smaller first contribution.</span></span>

<span data-ttu-id="4850b-114">我们使用标签以许多不同的方式对问题进行分类：</span><span class="sxs-lookup"><span data-stu-id="4850b-114">We use labels to classify issues in many different ways:</span></span>

- <span data-ttu-id="4850b-115">[.NET 指南](#find-a-single-net-guide)和[指南章节](#search-one-section-of-a-guide)。</span><span class="sxs-lookup"><span data-stu-id="4850b-115">[.NET Guides](#find-a-single-net-guide) and [sections of a guide](#search-one-section-of-a-guide).</span></span>
- [<span data-ttu-id="4850b-116">目标版本</span><span class="sxs-lookup"><span data-stu-id="4850b-116">Target release</span></span>](#releases)
- [<span data-ttu-id="4850b-117">优先级</span><span class="sxs-lookup"><span data-stu-id="4850b-117">Priority</span></span>](#priority)

<span data-ttu-id="4850b-118">可以组合每个集合（指南、版本、优先级）的标签，以创建较小范围的重点来查找要处理的问题。</span><span class="sxs-lookup"><span data-stu-id="4850b-118">You can combine a label from each set (guide, release, priority) to create a narrow focus to find issues you want to work on.</span></span>

### <a name="find-a-single-net-guide"></a><span data-ttu-id="4850b-119">查找单个 .NET 指南</span><span class="sxs-lookup"><span data-stu-id="4850b-119">Find a single .NET guide</span></span>

<span data-ttu-id="4850b-120">我们将标签用于每个体系结构电子书和每个 .NET 指南。</span><span class="sxs-lookup"><span data-stu-id="4850b-120">We use labels for each of the architecture e-books and for each .NET Guide.</span></span>

<span data-ttu-id="4850b-121">![：书籍：浅绿色背景上的指南](./media/labels-projects/guide.png "体系结构指南标签的前缀")</span><span class="sxs-lookup"><span data-stu-id="4850b-121">![:book: guide on light green background](./media/labels-projects/guide.png "Prefix for architecture guide labels")</span></span>

<span data-ttu-id="4850b-122">体系结构电子书使用 `:book: guide` 前缀进行标注，并且具有浅绿色背景。</span><span class="sxs-lookup"><span data-stu-id="4850b-122">Architecture e-books are noted with the `:book: guide` prefix and have a light green background.</span></span> <span data-ttu-id="4850b-123">这些是涵盖推荐体系结构的长格式区域。</span><span class="sxs-lookup"><span data-stu-id="4850b-123">These are the long-form areas that cover recommended architecture.</span></span> <span data-ttu-id="4850b-124">以下是针对每个 .NET 体系结构指南筛选的当前问题。</span><span class="sxs-lookup"><span data-stu-id="4850b-124">Here are current issues filtered for each of the .NET architecture guides.</span></span>

- [<span data-ttu-id="4850b-125">ASP.NET Core Web 应用</span><span class="sxs-lookup"><span data-stu-id="4850b-125">ASP.NET Core web apps</span></span>](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20ASP.NET%20Core%20web%20apps)
- [<span data-ttu-id="4850b-126">Blazor</span><span class="sxs-lookup"><span data-stu-id="4850b-126">Blazor</span></span>](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Blazor)
- [<span data-ttu-id="4850b-127">云本机</span><span class="sxs-lookup"><span data-stu-id="4850b-127">Cloud Native</span></span>](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Cloud%20Native)
- [<span data-ttu-id="4850b-128">Docker 生命周期</span><span class="sxs-lookup"><span data-stu-id="4850b-128">Docker lifecycle</span></span>](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Docker%20lifecycle)
- [<span data-ttu-id="4850b-129">gRPC</span><span class="sxs-lookup"><span data-stu-id="4850b-129">gRPC</span></span>](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20gRPC)
- [<span data-ttu-id="4850b-130">通过 Windows 容器实现现代化</span><span class="sxs-lookup"><span data-stu-id="4850b-130">Modernizing w/ Windows containers</span></span>](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Modernizing%20w%2F%20Windows%20containers)
- [<span data-ttu-id="4850b-131">.NET 微服务</span><span class="sxs-lookup"><span data-stu-id="4850b-131">.NET Microservices</span></span>](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20.NET%20Microservices)
- [<span data-ttu-id="4850b-132">无服务器应用</span><span class="sxs-lookup"><span data-stu-id="4850b-132">Serverless apps</span></span>](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Serverless%20apps)

<span data-ttu-id="4850b-133">此标签样式也适用于[框架设计准则](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Framework%20Design%20Guidelines)。</span><span class="sxs-lookup"><span data-stu-id="4850b-133">This label style is also applied to the [Framework design guidelines](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Framework%20Design%20Guidelines).</span></span> <span data-ttu-id="4850b-134">此区域具有相同的标签设计，但不建议使用社区 PR。</span><span class="sxs-lookup"><span data-stu-id="4850b-134">This area has the same label design, but community PRs are discouraged.</span></span> <span data-ttu-id="4850b-135">这是经许可转载的材料，不应进行编辑。</span><span class="sxs-lookup"><span data-stu-id="4850b-135">This is material reprinted with permission and should not be edited.</span></span>

<span data-ttu-id="4850b-136">![：书籍：深蓝色背景上的区域](./media/labels-projects/area.png ".NET 指南区域标签的前缀")</span><span class="sxs-lookup"><span data-stu-id="4850b-136">![:books: Area on dark blue background](./media/labels-projects/area.png "Prefix for .NET Guide area labels")</span></span>

<span data-ttu-id="4850b-137">每个 .NET 指南都使用 `:books: Area` 前缀进行标注，并且具有深蓝色背景。</span><span class="sxs-lookup"><span data-stu-id="4850b-137">Each .NET Guide is noted with the `:books: Area` prefix and has a dark blue background.</span></span> <span data-ttu-id="4850b-138">以下是针对每个 .NET 指南筛选的当前问题。</span><span class="sxs-lookup"><span data-stu-id="4850b-138">Here are current issues filtered for each of the .NET guides.</span></span>

- [<span data-ttu-id="4850b-139">API 参考</span><span class="sxs-lookup"><span data-stu-id="4850b-139">API Reference</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20API%20Reference)
- [<span data-ttu-id="4850b-140">Azure .NET SDK</span><span class="sxs-lookup"><span data-stu-id="4850b-140">Azure .NET SDK</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20Azure%20.NET%20SDk)
- [<span data-ttu-id="4850b-141">C# 指南</span><span class="sxs-lookup"><span data-stu-id="4850b-141">C# Guide</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20C%23%20Guide)
- [<span data-ttu-id="4850b-142">桌面指南</span><span class="sxs-lookup"><span data-stu-id="4850b-142">Desktop Guide</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20Desktop%20Guide)
- [<span data-ttu-id="4850b-143">F# 指南</span><span class="sxs-lookup"><span data-stu-id="4850b-143">F# Guide</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20F%23%20Guide)
- [<span data-ttu-id="4850b-144">ML.NET 指南</span><span class="sxs-lookup"><span data-stu-id="4850b-144">ML.NET Guide</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20ML.NET%20Guide)
- <span data-ttu-id="4850b-145">[.NET 体系结构指南](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20Architecture%20Guide) - 可以删除</span><span class="sxs-lookup"><span data-stu-id="4850b-145">[.NET Architecture Guide](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20Architecture%20Guide) - Could be removed</span></span>
- [<span data-ttu-id="4850b-146">.NET Core 指南</span><span class="sxs-lookup"><span data-stu-id="4850b-146">.NET Core Guide</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20Core%20Guide)
- [<span data-ttu-id="4850b-147">.NET for Apache Spark 指南</span><span class="sxs-lookup"><span data-stu-id="4850b-147">.NET for Apache Spark Guide</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20for%20Apache%20Spark%20Guide)
- [<span data-ttu-id="4850b-148">.NET Framework 指南</span><span class="sxs-lookup"><span data-stu-id="4850b-148">.NET Framework Guide</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20Framework%20Guide)
- [<span data-ttu-id="4850b-149">.NET 指南</span><span class="sxs-lookup"><span data-stu-id="4850b-149">.NET Guide</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20Guide)
- <span data-ttu-id="4850b-150">[Roslyn API 参考](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20Roslyn%20API%20Reference) - 可以删除。</span><span class="sxs-lookup"><span data-stu-id="4850b-150">[Roslyn API Reference](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20Roslyn%20API%20Reference) - could be removed.</span></span>
- [<span data-ttu-id="4850b-151">Visual Basic 指南</span><span class="sxs-lookup"><span data-stu-id="4850b-151">Visual Basic Guide</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20Visual%20Basic%20Guide)

#### <a name="search-one-section-of-a-guide"></a><span data-ttu-id="4850b-152">搜索指南的一个部分</span><span class="sxs-lookup"><span data-stu-id="4850b-152">Search one section of a guide</span></span>

<span data-ttu-id="4850b-153">![：card_file_box：中蓝色背景上的区域](./media/labels-projects/technology.png ".NET 指南子区域标签的前缀")</span><span class="sxs-lookup"><span data-stu-id="4850b-153">![:card_file_box: Area on medium blue background](./media/labels-projects/technology.png "Prefix for .NET Guide sub-area labels")</span></span>

<span data-ttu-id="4850b-154">.NET 指南涵盖很多内容，因此这些标签会进一步限制指南的一个部分的范围。</span><span class="sxs-lookup"><span data-stu-id="4850b-154">The .NET guides are large, so these labels further limit the scope by a section of a guide.</span></span> <span data-ttu-id="4850b-155">每个 .NET 指南子区域都使用 `:card_file_box: Technology` 前缀进行标注，并且具有中蓝色背景。</span><span class="sxs-lookup"><span data-stu-id="4850b-155">Each .NET Guide subarea is noted with the `:card_file_box: Technology` prefix and has a medium blue background.</span></span> <span data-ttu-id="4850b-156">其中许多标签适用于多个指南，而其他标签只位于一个指南中。</span><span class="sxs-lookup"><span data-stu-id="4850b-156">Many of these labels apply to multiple guides, while others are in only one guide.</span></span> <span data-ttu-id="4850b-157">筛选区域后，添加其中一个标签以进一步限制问题的范围。</span><span class="sxs-lookup"><span data-stu-id="4850b-157">After filtering on an area, add one of these labels to further limit the scope of issues.</span></span>

- <span data-ttu-id="4850b-158">AppCompat</span><span class="sxs-lookup"><span data-stu-id="4850b-158">AppCompat</span></span>
- <span data-ttu-id="4850b-159">异步任务</span><span class="sxs-lookup"><span data-stu-id="4850b-159">Async Task</span></span>
- <span data-ttu-id="4850b-160">C# 高级概念</span><span class="sxs-lookup"><span data-stu-id="4850b-160">C# Advanced concepts</span></span>
- <span data-ttu-id="4850b-161">C# 编译器</span><span class="sxs-lookup"><span data-stu-id="4850b-161">C# compiler</span></span>
- <span data-ttu-id="4850b-162">C# 基础知识</span><span class="sxs-lookup"><span data-stu-id="4850b-162">C# Fundamentals</span></span>
- <span data-ttu-id="4850b-163">C# 入门</span><span class="sxs-lookup"><span data-stu-id="4850b-163">C# Get Started</span></span>
- <span data-ttu-id="4850b-164">C# 语言参考</span><span class="sxs-lookup"><span data-stu-id="4850b-164">C# Language Reference</span></span>
- <span data-ttu-id="4850b-165">C# Null 安全性</span><span class="sxs-lookup"><span data-stu-id="4850b-165">C# Null safety</span></span>
- <span data-ttu-id="4850b-166">C# 新增功能</span><span class="sxs-lookup"><span data-stu-id="4850b-166">C# What's new</span></span>
- <span data-ttu-id="4850b-167">CLI</span><span class="sxs-lookup"><span data-stu-id="4850b-167">CLI</span></span>
- <span data-ttu-id="4850b-168">数据访问</span><span class="sxs-lookup"><span data-stu-id="4850b-168">Data Access</span></span>
- <span data-ttu-id="4850b-169">Docker</span><span class="sxs-lookup"><span data-stu-id="4850b-169">Docker</span></span>
- <span data-ttu-id="4850b-170">安装程序</span><span class="sxs-lookup"><span data-stu-id="4850b-170">Installers</span></span>
- <span data-ttu-id="4850b-171">LINQ</span><span class="sxs-lookup"><span data-stu-id="4850b-171">LINQ</span></span>
- <span data-ttu-id="4850b-172">NCL</span><span class="sxs-lookup"><span data-stu-id="4850b-172">NCL</span></span>
- <span data-ttu-id="4850b-173">.NET Standard</span><span class="sxs-lookup"><span data-stu-id="4850b-173">.NET Standard</span></span>
- <span data-ttu-id="4850b-174">Roslyn API</span><span class="sxs-lookup"><span data-stu-id="4850b-174">Roslyn APIs</span></span>
- <span data-ttu-id="4850b-175">安全性</span><span class="sxs-lookup"><span data-stu-id="4850b-175">Security</span></span>
- <span data-ttu-id="4850b-176">WCF</span><span class="sxs-lookup"><span data-stu-id="4850b-176">WCF</span></span>
- <span data-ttu-id="4850b-177">WF</span><span class="sxs-lookup"><span data-stu-id="4850b-177">WF</span></span>
- <span data-ttu-id="4850b-178">WIF</span><span class="sxs-lookup"><span data-stu-id="4850b-178">WIF</span></span>
- <span data-ttu-id="4850b-179">WinForms</span><span class="sxs-lookup"><span data-stu-id="4850b-179">WinForms</span></span>
- <span data-ttu-id="4850b-180">WPF</span><span class="sxs-lookup"><span data-stu-id="4850b-180">WPF</span></span>

### <a name="releases"></a><span data-ttu-id="4850b-181">版本</span><span class="sxs-lookup"><span data-stu-id="4850b-181">Releases</span></span>

<span data-ttu-id="4850b-182">![：checkered_flag：版本：深黄色](./media/labels-projects/release.png "版本标签的前缀")</span><span class="sxs-lookup"><span data-stu-id="4850b-182">![:checkered_flag: Release: on dark yellow](./media/labels-projects/release.png "Prefix for release labels")</span></span>

<span data-ttu-id="4850b-183">针对特定版本标记的问题使用 `:checkered_flag: Release:` 前缀标注，并具有深黄色背景。</span><span class="sxs-lookup"><span data-stu-id="4850b-183">Issues tagged for a specific release are noted with the `:checkered_flag: Release:` prefix and have a dark yellow background.</span></span>

- <span data-ttu-id="4850b-184">.NET Core 2.2</span><span class="sxs-lookup"><span data-stu-id="4850b-184">.NET Core 2.2</span></span>
- <span data-ttu-id="4850b-185">.NET Core 3.0</span><span class="sxs-lookup"><span data-stu-id="4850b-185">.NET Core 3.0</span></span>
- <span data-ttu-id="4850b-186">.NET Framework 4.8</span><span class="sxs-lookup"><span data-stu-id="4850b-186">.NET Framework 4.8</span></span>
- <span data-ttu-id="4850b-187">.NET 5</span><span class="sxs-lookup"><span data-stu-id="4850b-187">.NET 5</span></span>

### <a name="priority"></a><span data-ttu-id="4850b-188">优先级</span><span class="sxs-lookup"><span data-stu-id="4850b-188">Priority</span></span>

<span data-ttu-id="4850b-189">优先级标签全部为 `P`，后跟单个数字。</span><span class="sxs-lookup"><span data-stu-id="4850b-189">Priority labels are all `P` followed by a single digit.</span></span> <span data-ttu-id="4850b-190">较小的数字表示较高的优先级：</span><span class="sxs-lookup"><span data-stu-id="4850b-190">Lower numbers are higher priority:</span></span>

- <span data-ttu-id="4850b-191">P0</span><span class="sxs-lookup"><span data-stu-id="4850b-191">P0</span></span>
- <span data-ttu-id="4850b-192">P1</span><span class="sxs-lookup"><span data-stu-id="4850b-192">P1</span></span>
- <span data-ttu-id="4850b-193">P2</span><span class="sxs-lookup"><span data-stu-id="4850b-193">P2</span></span>
- <span data-ttu-id="4850b-194">P3</span><span class="sxs-lookup"><span data-stu-id="4850b-194">P3</span></span>

### <a name="what-about-the-other-labels"></a><span data-ttu-id="4850b-195">其他标签呢？</span><span class="sxs-lookup"><span data-stu-id="4850b-195">What about the other labels?</span></span>

<span data-ttu-id="4850b-196">内容团队还使用许多其他标签来管理问题的不同分类。</span><span class="sxs-lookup"><span data-stu-id="4850b-196">There are many other labels used by the content teams to manage different classifications of issues.</span></span> <span data-ttu-id="4850b-197">如果你不属于内容团队，则可以忽略这些其他标签。</span><span class="sxs-lookup"><span data-stu-id="4850b-197">If you're not on the content team, you can ignore these other labels.</span></span>

## <a name="projects"></a><span data-ttu-id="4850b-198">项目</span><span class="sxs-lookup"><span data-stu-id="4850b-198">Projects</span></span>

<span data-ttu-id="4850b-199">我们通过两种方式使用项目：</span><span class="sxs-lookup"><span data-stu-id="4850b-199">We use projects in two ways:</span></span>

- <span data-ttu-id="4850b-200">Month YYYY 项目类型：这些是每月工作计划的 Scrum 板。</span><span class="sxs-lookup"><span data-stu-id="4850b-200">Month YYYY project types: These are scrum boards for each month's working plan.</span></span>
- <span data-ttu-id="4850b-201">长时间运行的长篇故事：这些用于在工作持续几个月的情况下组织以目标为导向的任务。</span><span class="sxs-lookup"><span data-stu-id="4850b-201">Long-running epics: These are used to organize tasks toward a goal when the work will occur over several months.</span></span>
