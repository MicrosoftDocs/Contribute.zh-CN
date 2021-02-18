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
# <a name="labels-projects-and-milestones-roadmap"></a><span data-ttu-id="444de-103">标签、项目和里程碑路线图</span><span class="sxs-lookup"><span data-stu-id="444de-103">Labels, projects, and milestones roadmap</span></span>

<span data-ttu-id="444de-104">.NET 文档团队广泛使用 [ GitHub 标签](https://github.com/dotnet/docs/labels)来组织工作。</span><span class="sxs-lookup"><span data-stu-id="444de-104">The .NET docs team makes extensive use of [GitHub labels](https://github.com/dotnet/docs/labels) to organize our work.</span></span> <span data-ttu-id="444de-105">通过筛选标签的组合，我们可以快速关注 [.NET 文档网站](https://docs.microsoft.com/dotnet)上我们所需的部分。</span><span class="sxs-lookup"><span data-stu-id="444de-105">By filtering on combinations of labels, we can quickly focus on sections of interest on the [.NET docs website](https://docs.microsoft.com/dotnet).</span></span> <span data-ttu-id="444de-106">例如，我们可以通过查询 [is:issue is:open label:"dotnet-architecture/prod"](https://github.com/dotnet/docs/labels/dotnet-architecture%2Fprod) 筛选出有关体系结构指南的所有待解决问题。</span><span class="sxs-lookup"><span data-stu-id="444de-106">For example, we could filter to all of the open issues on the architecture guides with a query to [is:issue is:open label:"dotnet-architecture/prod"](https://github.com/dotnet/docs/labels/dotnet-architecture%2Fprod).</span></span>

<span data-ttu-id="444de-107">我们使用 [GitHub 项目](https://github.com/dotnet/docs/projects)来组织冲刺 (sprint) 和其他以目标为导向的长篇故事。</span><span class="sxs-lookup"><span data-stu-id="444de-107">We use [GitHub projects](https://github.com/dotnet/docs/projects) to organize sprints and other goal-oriented epics.</span></span> <span data-ttu-id="444de-108">我们还使用 [GitHub 里程碑](https://github.com/dotnet/docs/milestones)来跟踪工作。</span><span class="sxs-lookup"><span data-stu-id="444de-108">We also use [GitHub milestones](https://github.com/dotnet/docs/milestones) to track work.</span></span> <span data-ttu-id="444de-109">最好考虑用于规划的项目（问题）和用于工作的里程碑（拉取请求）。</span><span class="sxs-lookup"><span data-stu-id="444de-109">It is best to think of projects for planning (issues), and milestones for work (pull requests).</span></span>

<span data-ttu-id="444de-110">此路线图说明了我们使用这些组织工具的方式，并提供了用于查找感兴趣内容的便捷筛选器的链接。</span><span class="sxs-lookup"><span data-stu-id="444de-110">This roadmap explains how we use these organizational tools and has links to handy filters we use to find areas of interest.</span></span>

## <a name="labels"></a><span data-ttu-id="444de-111">标签</span><span class="sxs-lookup"><span data-stu-id="444de-111">Labels</span></span>

<span data-ttu-id="444de-112">如果这你是首次体验参与 [dotnet/docs](https://github.com/dotnet/docs)，请从[容易作答](https://github.com/dotnet/docs/labels/up-for-grabs)的问题开始。</span><span class="sxs-lookup"><span data-stu-id="444de-112">If this is your first experience contributing to [dotnet/docs](https://github.com/dotnet/docs), start with the [up-for-grabs](https://github.com/dotnet/docs/labels/up-for-grabs) issues.</span></span> <span data-ttu-id="444de-113">这些问题针对的范围更加集中。</span><span class="sxs-lookup"><span data-stu-id="444de-113">These are issues that have a more focused scope.</span></span> <span data-ttu-id="444de-114">从此类问题入手是完成首次参与的好方式。</span><span class="sxs-lookup"><span data-stu-id="444de-114">They are a great way to make your first contribution.</span></span> <span data-ttu-id="444de-115">从“容易作答”视图中，你可以进一步根据区域和优先级筛选问题。</span><span class="sxs-lookup"><span data-stu-id="444de-115">From the up-for-grabs view, you can further filter issues based on areas and priority.</span></span> <span data-ttu-id="444de-116">我们已使用 [good-first-issue](https://github.com/dotnet/docs/labels/good-first-issue) 标签标识出适合新手回答的问题，以便于你完成首次小小的参与。</span><span class="sxs-lookup"><span data-stu-id="444de-116">We've identified good issues for beginners with the [good-first-issue](https://github.com/dotnet/docs/labels/good-first-issue) if you want to try a smaller first contribution.</span></span>

<span data-ttu-id="444de-117">我们使用标签以多种不同方式来分类问题：</span><span class="sxs-lookup"><span data-stu-id="444de-117">We use labels to classify issues in many different ways:</span></span>

- <span data-ttu-id="444de-118">[.NET 指南](#find-issues-for-a-single-net-guide)和[指南章节](#find-issues-for-one-section-of-a-guide)。</span><span class="sxs-lookup"><span data-stu-id="444de-118">[.NET Guides](#find-issues-for-a-single-net-guide) and [sections of a guide](#find-issues-for-one-section-of-a-guide).</span></span>
- [<span data-ttu-id="444de-119">目标版本</span><span class="sxs-lookup"><span data-stu-id="444de-119">Target release</span></span>](#releases)
- [<span data-ttu-id="444de-120">Priority</span><span class="sxs-lookup"><span data-stu-id="444de-120">Priority</span></span>](#priority)

<span data-ttu-id="444de-121">你可以合并每组（指南、版本、优先级）中的标签，以缩小关注范围，查找你想要解决的问题。</span><span class="sxs-lookup"><span data-stu-id="444de-121">You can combine a label from each set (guide, release, priority) to create a narrow focus to find issues you want to work on.</span></span>

### <a name="find-issues-for-a-single-net-guide"></a><span data-ttu-id="444de-122">查找单个 .NET 指南的问题</span><span class="sxs-lookup"><span data-stu-id="444de-122">Find issues for a single .NET guide</span></span>

<span data-ttu-id="444de-123">我们针对各个体系结构电子书以及各个 .NET 指南使用标签。</span><span class="sxs-lookup"><span data-stu-id="444de-123">We use labels for each of the architecture e-books and for each .NET Guide.</span></span> <span data-ttu-id="444de-124">所有电子书都注明了 [dotnet-architecture/prod](https://github.com/dotnet/docs/labels/dotnet-architecture%2Fprod) 标签。</span><span class="sxs-lookup"><span data-stu-id="444de-124">All ebooks are noted with the [dotnet-architecture/prod](https://github.com/dotnet/docs/labels/dotnet-architecture%2Fprod) label.</span></span> <span data-ttu-id="444de-125">每本书都具有以 `/tech` 结尾的唯一标签。</span><span class="sxs-lookup"><span data-stu-id="444de-125">Each book has a unique label that ends with `/tech`.</span></span>

<span data-ttu-id="444de-126">每个 .NET 指南都带有 [`/prod`](https://github.com/dotnet/docs/labels?q=prod) 后缀和蓝灰色背景。</span><span class="sxs-lookup"><span data-stu-id="444de-126">Each .NET Guide is noted with the [`/prod`](https://github.com/dotnet/docs/labels?q=prod) suffix and has a blue-gray background.</span></span> <span data-ttu-id="444de-127">以下是针对各个 .NET 指南筛选出的当前问题。</span><span class="sxs-lookup"><span data-stu-id="444de-127">Here are current issues filtered for each of the .NET guides.</span></span>

- [<span data-ttu-id="444de-128">.NET 指南 - `dotnet/prod`</span><span class="sxs-lookup"><span data-stu-id="444de-128">.NET Guide - `dotnet/prod`</span></span>](https://github.com/dotnet/docs/labels/dotnet%2Fprod)
- [<span data-ttu-id="444de-129">.NET 基础指南（以前称为 .NET Standard 指南）- `dotnet-fundamentals/prod`</span><span class="sxs-lookup"><span data-stu-id="444de-129">.NET Fundamentals Guide (formerly .NET Standard Guide) - `dotnet-fundamentals/prod`</span></span>](https://github.com/dotnet/docs/labels/dotnet-fundamentals%2Fprod)
- [<span data-ttu-id="444de-130">.NET 基础指南（以前称为 .NET Core 指南）- `dotnet-core/prod`</span><span class="sxs-lookup"><span data-stu-id="444de-130">.NET Fundamentals Guide (formerly .NET Core Guide) - `dotnet-core/prod`</span></span>](https://github.com/dotnet/docs/labels/dotnet-core%2Fprod)
- [<span data-ttu-id="444de-131">.NET Framework 指南 - `dotnet-framework/prod`</span><span class="sxs-lookup"><span data-stu-id="444de-131">.NET Framework Guide - `dotnet-framework/prod`</span></span>](https://github.com/dotnet/docs/labels/dotnet-framework%2Fprod)
- [<span data-ttu-id="444de-132">API 参考 - `dotnet-api/prod`</span><span class="sxs-lookup"><span data-stu-id="444de-132">API Reference - `dotnet-api/prod`</span></span>](https://github.com/dotnet/docs/labels/dotnet-api%2Fprod)
- [<span data-ttu-id="444de-133">C# 指南 - `dotnet-csharp/prod`</span><span class="sxs-lookup"><span data-stu-id="444de-133">C# Guide - `dotnet-csharp/prod`</span></span>](https://github.com/dotnet/docs/labels/dotnet-csharp%2Fprod)
- [<span data-ttu-id="444de-134">F# 指南 - `dotnet-fsharp/prod`</span><span class="sxs-lookup"><span data-stu-id="444de-134">F# Guide- `dotnet-fsharp/prod`</span></span>](https://github.com/dotnet/docs/labels/dotnet-fsharp%2Fprod)
- [<span data-ttu-id="444de-135">Visual Basic 指南 - \`dotnet-visualbasic/prod</span><span class="sxs-lookup"><span data-stu-id="444de-135">Visual Basic Guide - \`dotnet-visualbasic/prod</span></span>](https://github.com/dotnet/docs/labels/dotnet-visualbasic%2Fprod)
- [<span data-ttu-id="444de-136">ML.NET 指南 - `dotnet-ml/prod`</span><span class="sxs-lookup"><span data-stu-id="444de-136">ML.NET Guide - `dotnet-ml/prod`</span></span>](https://github.com/dotnet/docs/labels/dotnet-ml%2Fprod)
- [<span data-ttu-id="444de-137">Azure .NET SDK - `azure-dotnet/prod`</span><span class="sxs-lookup"><span data-stu-id="444de-137">Azure .NET SDK - `azure-dotnet/prod`</span></span>](https://github.com/dotnet/docs/labels/azure-dotnet%2Fprod)
- [<span data-ttu-id="444de-138">.NET for Apache Spark 指南 - `dotnet-spark/prod`</span><span class="sxs-lookup"><span data-stu-id="444de-138">.NET for Apache Spark Guide - `dotnet-spark/prod`</span></span>](https://github.com/dotnet/docs/labels/dotnet-spark%2Fprod)
- [<span data-ttu-id="444de-139">.NET 桌面指南 - `dotnet-desktop/prod`</span><span class="sxs-lookup"><span data-stu-id="444de-139">.NET Desktop Guide - `dotnet-desktop/prod`</span></span>](https://github.com/dotnet/docs/labels/dotnet-desktop%2Fprod)

<span data-ttu-id="444de-140">为跨存储库的区域定义了其他产品标签。</span><span class="sxs-lookup"><span data-stu-id="444de-140">Other product labels are defined for areas that cross repositories.</span></span>

#### <a name="find-issues-for-one-section-of-a-guide"></a><span data-ttu-id="444de-141">查找指南某个部分的问题</span><span class="sxs-lookup"><span data-stu-id="444de-141">Find issues for one section of a guide</span></span>

<span data-ttu-id="444de-142">.NET 指南范围较大，因此，这些标签按指南章节对范围做了进一步限制。</span><span class="sxs-lookup"><span data-stu-id="444de-142">The .NET guides are large, so these labels further limit the scope by a section of a guide.</span></span> <span data-ttu-id="444de-143">每个 .NET 指南子区域都带有 [`/tech`](https://github.com/dotnet/docs/labels?q=tech) 后缀和浅蓝色背景。</span><span class="sxs-lookup"><span data-stu-id="444de-143">Each .NET Guide subarea is noted with the [`/tech`](https://github.com/dotnet/docs/labels?q=tech) suffix and has a light blue background.</span></span> <span data-ttu-id="444de-144">其中许多标签适用于多个指南，而有些标签仅适用于一个指南。</span><span class="sxs-lookup"><span data-stu-id="444de-144">Many of these labels apply to multiple guides, while others are in only one guide.</span></span> <span data-ttu-id="444de-145">基于区域筛选后，添加其中一种标签，进一步限制问题的范围。</span><span class="sxs-lookup"><span data-stu-id="444de-145">After filtering on an area, add one of these labels to further limit the scope of issues.</span></span>

### <a name="releases"></a><span data-ttu-id="444de-146">版本</span><span class="sxs-lookup"><span data-stu-id="444de-146">Releases</span></span>

<span data-ttu-id="444de-147">![：checkered_flag：版本：深黄色](./media/labels-projects/release.png "版本标签的前缀")</span><span class="sxs-lookup"><span data-stu-id="444de-147">![:checkered_flag: Release: on dark yellow](./media/labels-projects/release.png "Prefix for release labels")</span></span>

<span data-ttu-id="444de-148">针对特定版本标记的问题使用 [`:checkered_flag: Release:`](https://github.com/dotnet/docs/labels?q=%3Acheckered_flag%3A+Release) 前缀标注，并具有深黄色背景。</span><span class="sxs-lookup"><span data-stu-id="444de-148">Issues tagged for a specific release are noted with the [`:checkered_flag: Release:`](https://github.com/dotnet/docs/labels?q=%3Acheckered_flag%3A+Release) prefix and have a dark yellow background.</span></span>

### <a name="priority"></a><span data-ttu-id="444de-149">优先级</span><span class="sxs-lookup"><span data-stu-id="444de-149">Priority</span></span>

<span data-ttu-id="444de-150">优先级标签由 `Pri` 及其后面的单个数字构成。</span><span class="sxs-lookup"><span data-stu-id="444de-150">Priority labels are all `Pri` followed by a single digit.</span></span> <span data-ttu-id="444de-151">数字越小表示优先级越高：</span><span class="sxs-lookup"><span data-stu-id="444de-151">Lower numbers are higher priority:</span></span>

- <span data-ttu-id="444de-152">Pri0 - 严重优先级</span><span class="sxs-lookup"><span data-stu-id="444de-152">Pri0 - Critical priority</span></span>

  <span data-ttu-id="444de-153">安全性问题或合规性所需的法律要求。</span><span class="sxs-lookup"><span data-stu-id="444de-153">Security issue or legally required for compliance.</span></span> <span data-ttu-id="444de-154">应放下所有其他方面来修复。</span><span class="sxs-lookup"><span data-stu-id="444de-154">We drop everything else to fix.</span></span>
  
- <span data-ttu-id="444de-155">Pri1 - 高优先级</span><span class="sxs-lookup"><span data-stu-id="444de-155">Pri1 - High priority</span></span>

  <span data-ttu-id="444de-156">常见方案的要素。</span><span class="sxs-lookup"><span data-stu-id="444de-156">Essential for common scenarios.</span></span> <span data-ttu-id="444de-157">或者高访问量文章上的明显错误。</span><span class="sxs-lookup"><span data-stu-id="444de-157">Or highly visible error on high page view article.</span></span> <span data-ttu-id="444de-158">在 P2 或 P3 起作用之前执行。</span><span class="sxs-lookup"><span data-stu-id="444de-158">We do these before P2 or P3 work.</span></span>
  
- <span data-ttu-id="444de-159">Pri2 - 中优先级</span><span class="sxs-lookup"><span data-stu-id="444de-159">Pri2 - Medium priority</span></span>

  <span data-ttu-id="444de-160">有助于常见方案，但不阻止。</span><span class="sxs-lookup"><span data-stu-id="444de-160">Helpful for common scenarios but not blocking.</span></span>  <span data-ttu-id="444de-161">快速简单地执行，或者在解决同一篇文章中 P1 问题时修复。</span><span class="sxs-lookup"><span data-stu-id="444de-161">We do these if quick and easy, or fit them in while addressing a P1 issue in the same article.</span></span>
  
- <span data-ttu-id="444de-162">Pri3 - 低优先级</span><span class="sxs-lookup"><span data-stu-id="444de-162">Pri3 - Low priority</span></span>

  <span data-ttu-id="444de-163">有助于边缘案例、常见案例的普通矫正、低访问量文章或弃用的技术。</span><span class="sxs-lookup"><span data-stu-id="444de-163">Helpful for edge cases, trivial corrections for common scenarios, low page view article, or deprecated technology.</span></span> <span data-ttu-id="444de-164">不值得花费时间，但可供争取社区参与。</span><span class="sxs-lookup"><span data-stu-id="444de-164">Not worth our time but up for grabs for community contribution.</span></span> <span data-ttu-id="444de-165">如果 P3 问题两个月后仍未解决，可关闭。</span><span class="sxs-lookup"><span data-stu-id="444de-165">A P3 issue may be closed if not addressed after two months.</span></span>

### <a name="what-about-the-other-labels"></a><span data-ttu-id="444de-166">其他标签呢</span><span class="sxs-lookup"><span data-stu-id="444de-166">What about the other labels</span></span>

<span data-ttu-id="444de-167">内容团队还使用了许多其他标签来管理各种问题分类。</span><span class="sxs-lookup"><span data-stu-id="444de-167">There are many other labels used by the content teams to manage different classifications of issues.</span></span> <span data-ttu-id="444de-168">如果你不属于内容团队，则可以忽略其他这些标签。</span><span class="sxs-lookup"><span data-stu-id="444de-168">If you're not on the content team, you can ignore these other labels.</span></span>

## <a name="projects"></a><span data-ttu-id="444de-169">项目</span><span class="sxs-lookup"><span data-stu-id="444de-169">Projects</span></span>

<span data-ttu-id="444de-170">项目用于规划目的，在这种情况下，设置优先级的工作是通过看板自动完成的。</span><span class="sxs-lookup"><span data-stu-id="444de-170">Projects are intended for planning purposes, where prioritized work is automated through a Kanban board.</span></span> <span data-ttu-id="444de-171">项目应仅包含 GitHub 问题，而不应包含拉取请求。</span><span class="sxs-lookup"><span data-stu-id="444de-171">Projects should only ever contain GitHub issues, _not_ pull requests.</span></span> <span data-ttu-id="444de-172">项目不同于里程碑，因为里程碑只包含拉取请求。</span><span class="sxs-lookup"><span data-stu-id="444de-172">Projects differ from milestones, in that milestones only contain pull requests.</span></span>

<span data-ttu-id="444de-173">我们通过两种方式使用项目：</span><span class="sxs-lookup"><span data-stu-id="444de-173">We use projects in two ways:</span></span>

- <span data-ttu-id="444de-174">`Month YYYY` 项目类型：这些是每月工作计划的看板。</span><span class="sxs-lookup"><span data-stu-id="444de-174">`Month YYYY` project types: These are Kanban boards for each month's working plan.</span></span>
  - <span data-ttu-id="444de-175">示例：[2020 年 7 月](https://github.com/dotnet/docs/projects/103)、[2020 年 8 月](https://github.com/dotnet/docs/projects/117)等。</span><span class="sxs-lookup"><span data-stu-id="444de-175">Examples, [July 2020](https://github.com/dotnet/docs/projects/103), [August 2020](https://github.com/dotnet/docs/projects/117), and so on.</span></span>
- <span data-ttu-id="444de-176">长时间运行的长篇故事：这些用于在工作持续几个月的情况下组织以目标为导向的任务。</span><span class="sxs-lookup"><span data-stu-id="444de-176">Long-running epics: These are used to organize tasks toward a goal when the work will occur over several months.</span></span>
  - <span data-ttu-id="444de-177">示例：[.NET 5 Wave - 重组](https://github.com/dotnet/docs/projects/105)、[.NET 语言 (.NET 5 Wave)](https://github.com/dotnet/docs/projects/106) 等。</span><span class="sxs-lookup"><span data-stu-id="444de-177">Examples: [.NET 5 Wave - Reorganization](https://github.com/dotnet/docs/projects/105), [.NET Languages (.NET 5 wave) ](https://github.com/dotnet/docs/projects/106), and so on.</span></span>

## <a name="milestones"></a><span data-ttu-id="444de-178">里程碑</span><span class="sxs-lookup"><span data-stu-id="444de-178">Milestones</span></span>

<span data-ttu-id="444de-179">里程碑通常遵循项目 `Month YYYY` 的相同命名约定，但不同于项目。</span><span class="sxs-lookup"><span data-stu-id="444de-179">Milestones typically follow the same naming convention of projects `Month YYYY`, but they're different from projects.</span></span> <span data-ttu-id="444de-180">我们使用里程碑来跟踪已完成的工作。</span><span class="sxs-lookup"><span data-stu-id="444de-180">We use milestones to track completed work.</span></span> <span data-ttu-id="444de-181">里程碑应不包含问题（可能的工作），但仅包含拉取请求。</span><span class="sxs-lookup"><span data-stu-id="444de-181">Milestones should _not_ contain issues (potential work), but rather exclusively contain pull requests.</span></span> <span data-ttu-id="444de-182">当前里程碑将自动应用于新的拉取请求。</span><span class="sxs-lookup"><span data-stu-id="444de-182">The current milestone is automatically applied to new pull requests.</span></span>
