---
title: 参与 .NET 文档存储库撰写
description: 本文档介绍参与组成 .NET 文档的存储库中文章和代码示例撰写的过程。
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
ms.date: 05/14/2020
ms.openlocfilehash: d1631f34ef9a3ceb10178792842421376fea97b0
ms.sourcegitcommit: 3774d06ddc1f92b2bdb4c1d8babbd18357229298
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/28/2020
ms.locfileid: "87264800"
---
# <a name="learn-how-to-contribute-to-the-net-docs-repositories"></a><span data-ttu-id="80446-103">了解如何参与 .NET 文档存储库撰写</span><span class="sxs-lookup"><span data-stu-id="80446-103">Learn how to contribute to the .NET docs repositories</span></span>

<span data-ttu-id="80446-104">感谢你有兴趣参与 .NET 文档撰写！</span><span class="sxs-lookup"><span data-stu-id="80446-104">Thank you for your interest in contributing to the .NET documentation!</span></span>

<span data-ttu-id="80446-105">本文档介绍参与托管在 [.NET 文档站点](https://docs.microsoft.com/dotnet)上的文章和代码示例撰写的过程。</span><span class="sxs-lookup"><span data-stu-id="80446-105">This document covers the process for contributing to the articles and code samples that are hosted on the [.NET documentation site](https://docs.microsoft.com/dotnet).</span></span> <span data-ttu-id="80446-106">参与供稿可能像更正拼写错误一样简单，也可能像撰写新文章一样复杂。</span><span class="sxs-lookup"><span data-stu-id="80446-106">Contributions may be as simple as typo corrections or as complex as new articles.</span></span>

<span data-ttu-id="80446-107">.NET 文档站点根据多个存储库生成：</span><span class="sxs-lookup"><span data-stu-id="80446-107">The .NET documentation site is built from multiple repositories:</span></span>

- [<span data-ttu-id="80446-108">.NET 概念文章和代码片段</span><span class="sxs-lookup"><span data-stu-id="80446-108">.NET conceptual articles and code snippets</span></span>](https://github.com/dotnet/docs)
- [<span data-ttu-id="80446-109">代码示例和代码片段</span><span class="sxs-lookup"><span data-stu-id="80446-109">Code samples and snippets</span></span>](https://github.com/dotnet/samples)
- [<span data-ttu-id="80446-110">.NET Standard、.NET Core、.NET Framework API 参考</span><span class="sxs-lookup"><span data-stu-id="80446-110">.NET Standard, .NET Core, .NET Framework API reference</span></span>](https://github.com/dotnet/dotnet-api-docs)
- [<span data-ttu-id="80446-111">.NET Compiler Platform SDK 参考</span><span class="sxs-lookup"><span data-stu-id="80446-111">.NET Compiler Platform SDK reference</span></span>](https://github.com/dotnet/roslyn-api-docs)
- [<span data-ttu-id="80446-112">ML.NET API 参考</span><span class="sxs-lookup"><span data-stu-id="80446-112">ML.NET API reference</span></span>](https://github.com/dotnet/ml-api-docs)

<span data-ttu-id="80446-113">在 [dotnet/docs](https://github.com/dotnet/docs/issues) 存储库中跟踪所有上述存储库的问题。</span><span class="sxs-lookup"><span data-stu-id="80446-113">Issues for all these repositories are tracked in the [dotnet/docs](https://github.com/dotnet/docs/issues) repository.</span></span>

## <a name="guidelines-for-contributions"></a><span data-ttu-id="80446-114">参与原则</span><span class="sxs-lookup"><span data-stu-id="80446-114">Guidelines for contributions</span></span>

<span data-ttu-id="80446-115">感谢社区参与文档撰写。以下列表显示你参与 .NET 文档撰写时需要记住的指导规则：</span><span class="sxs-lookup"><span data-stu-id="80446-115">We appreciate community contributions to docs. The following list shows some guiding rules to keep in mind when you're contributing to the .NET documentation:</span></span>

- <span data-ttu-id="80446-116">请**勿**向我们提出大量拉取请求。</span><span class="sxs-lookup"><span data-stu-id="80446-116">**DON'T** surprise us with large pull requests.</span></span> <span data-ttu-id="80446-117">相反，提出问题并发起讨论，在我们认同这一方向后你再投入大量的时间。</span><span class="sxs-lookup"><span data-stu-id="80446-117">Instead, file an issue and start a discussion so we can agree on a direction before you invest a large amount of time.</span></span>
- <span data-ttu-id="80446-118">请**务必**遵循这些说明以及[语音语调](dotnet-voice-tone.md)准则。</span><span class="sxs-lookup"><span data-stu-id="80446-118">**DO** follow these instructions and [voice and tone](dotnet-voice-tone.md) guidelines.</span></span>
- <span data-ttu-id="80446-119">请**务必**使用[模板](dotnet-style-guide.md)文件，作为工作的出发点。</span><span class="sxs-lookup"><span data-stu-id="80446-119">**DO** use the [template](dotnet-style-guide.md) file as the starting point of your work.</span></span>
- <span data-ttu-id="80446-120">处理文章前，请**务必**在分支上创建单独的分支。</span><span class="sxs-lookup"><span data-stu-id="80446-120">**DO** create a separate branch on your fork before working on the articles.</span></span>
- <span data-ttu-id="80446-121">请务必遵循 [GitHub 流](https://guides.github.com/introduction/flow/)。</span><span class="sxs-lookup"><span data-stu-id="80446-121">**DO** follow the [GitHub flow](https://guides.github.com/introduction/flow/).</span></span>
- <span data-ttu-id="80446-122">如果你愿意的话，请发布有关参与的博客和推文（或者诸如此类）！</span><span class="sxs-lookup"><span data-stu-id="80446-122">**DO** blog and tweet (or whatever) about your contributions if you like!</span></span>

<span data-ttu-id="80446-123">遵循这些指南可确保你和我们都能获得更好的体验。</span><span class="sxs-lookup"><span data-stu-id="80446-123">Following these guidelines will ensure a better experience for you and for us.</span></span>

## <a name="make-a-contribution-to-net-docs"></a><span data-ttu-id="80446-124">参与 .NET 文档撰写</span><span class="sxs-lookup"><span data-stu-id="80446-124">Make a contribution to .NET docs</span></span>

<span data-ttu-id="80446-125">**步骤 1：** 如果有兴趣编写新内容或仔细修订现有内容，请创建描述你想做的事情的[问题](https://github.com/dotnet/docs/issues)。</span><span class="sxs-lookup"><span data-stu-id="80446-125">**Step 1:** If you're interested in writing new content or in thoroughly revising existing content, open an [issue](https://github.com/dotnet/docs/issues) describing what you want to do.</span></span> <span data-ttu-id="80446-126">“Docs”文件夹中的内容组织成部分，在目录 (TOC) 中进行反映。</span><span class="sxs-lookup"><span data-stu-id="80446-126">The content inside the **docs** folder is organized into sections that are reflected in the Table of Contents (TOC).</span></span> <span data-ttu-id="80446-127">定义主题在 TOC 中所处的位置。</span><span class="sxs-lookup"><span data-stu-id="80446-127">Define where the topic will be located in the TOC.</span></span> <span data-ttu-id="80446-128">获取有关建议的反馈。</span><span class="sxs-lookup"><span data-stu-id="80446-128">Get feedback on your proposal.</span></span>

<span data-ttu-id="80446-129">-或-</span><span class="sxs-lookup"><span data-stu-id="80446-129">-or-</span></span>

<span data-ttu-id="80446-130">选择现有问题并解决该问题。</span><span class="sxs-lookup"><span data-stu-id="80446-130">Choose an existing issue and address it.</span></span> <span data-ttu-id="80446-131">可查看[未解决问题](https://github.com/dotnet/docs/issues)列表，并自愿处理感兴趣的主题：</span><span class="sxs-lookup"><span data-stu-id="80446-131">You can look at our [open issues](https://github.com/dotnet/docs/issues) list and volunteer to work on the ones you're interested in:</span></span>

- <span data-ttu-id="80446-132">对于好的优先问题，通过 [good-first-issue](https://github.com/dotnet/docs/labels/good-first-issue) 标签进行筛选。</span><span class="sxs-lookup"><span data-stu-id="80446-132">Filter by the [good-first-issue](https://github.com/dotnet/docs/labels/good-first-issue) label for, well, good first issues.</span></span>
- <span data-ttu-id="80446-133">对于适合社区参与的问题，通过 [up-for-grabs](https://github.com/dotnet/docs/labels/up-for-grabs) 标签进行筛选。</span><span class="sxs-lookup"><span data-stu-id="80446-133">Filter by the [up-for-grabs](https://github.com/dotnet/docs/labels/up-for-grabs) label for issues appropriate for community contribution.</span></span> <span data-ttu-id="80446-134">这些问题通常需要的上下文很少。</span><span class="sxs-lookup"><span data-stu-id="80446-134">These issues usually require minimal context.</span></span>
- <span data-ttu-id="80446-135">经验丰富的参与者可以处理任何感兴趣的问题。</span><span class="sxs-lookup"><span data-stu-id="80446-135">Experienced contributors can tackle any issues of interest.</span></span>

<span data-ttu-id="80446-136">当你找到要处理的问题时，可以添加评论，询问是否未解决。</span><span class="sxs-lookup"><span data-stu-id="80446-136">When you find an issue to work on, add a comment to ask if it's open.</span></span>

<span data-ttu-id="80446-137">选择要处理的任务后，请按照[入门](../get-started-setup-github.md)指南操作，创建 GitHub 帐户并设置环境。</span><span class="sxs-lookup"><span data-stu-id="80446-137">Once you've picked a task to work on, follow the [get started](../get-started-setup-github.md) guide to create a GitHub account and set up your environment.</span></span>

<span data-ttu-id="80446-138">**步骤 2：** 根据需要，创建 `/dotnet/docs`、`dotnet/samples`、`dotnet/dotnet-api-docs`、`dotnet/roslyn-api-docs` 或 `dotnet/ml-api-docs` 存储库的分支，并针对更改创建分支。</span><span class="sxs-lookup"><span data-stu-id="80446-138">**Step 2:** Fork the `/dotnet/docs`, `dotnet/samples`, `dotnet/dotnet-api-docs`, `dotnet/roslyn-api-docs`, or `dotnet/ml-api-docs` repos as needed and create a branch for your changes.</span></span>

<span data-ttu-id="80446-139">对于小更改，请在参与者指南的[主页](../index.md#quick-edits-to-existing-documents)中查看在 GitHub 中编辑的说明。</span><span class="sxs-lookup"><span data-stu-id="80446-139">For small changes, see the instructions on editing in GitHub on the [home page](../index.md#quick-edits-to-existing-documents) of the contributor guide.</span></span>

<span data-ttu-id="80446-140">**步骤 3：** 在此新分支上进行更改。</span><span class="sxs-lookup"><span data-stu-id="80446-140">**Step 3:** Make the changes on this new branch.</span></span>

<span data-ttu-id="80446-141">如果它是新主题，则可以使用此[模板文件](dotnet-style-guide.md)，作为起始点。</span><span class="sxs-lookup"><span data-stu-id="80446-141">If it's a new topic, you can use this [template file](dotnet-style-guide.md) as your starting point.</span></span> <span data-ttu-id="80446-142">它包含编写准则，并且还解释每篇文章需要的元数据（例如，作者信息）。</span><span class="sxs-lookup"><span data-stu-id="80446-142">It contains the writing guidelines and also explains the metadata required for each article, such as author information.</span></span> <span data-ttu-id="80446-143">要详细了解 docs.microsoft.com 站点中使用的 Markdown 语法，请参阅 [Markdown 参考](../markdown-reference.md)。</span><span class="sxs-lookup"><span data-stu-id="80446-143">For more information on the Markdown syntax used in the docs.microsoft.com site, see [Markdown reference](../markdown-reference.md).</span></span>

<span data-ttu-id="80446-144">导航到对应针对步骤 1 中的文章确定的目录位置的文件夹。</span><span class="sxs-lookup"><span data-stu-id="80446-144">Navigate to the folder that corresponds to the TOC location determined for your article in step 1.</span></span> <span data-ttu-id="80446-145">该文件夹包含针对该部分中所有文章的 Markdown 文件。</span><span class="sxs-lookup"><span data-stu-id="80446-145">That folder contains the Markdown files for all articles in that section.</span></span> <span data-ttu-id="80446-146">如有必要，新建一个文件夹，放置存储内容的文件。</span><span class="sxs-lookup"><span data-stu-id="80446-146">If necessary, create a new folder to place the files for your content.</span></span> <span data-ttu-id="80446-147">该部分的主要文章称为 index.md。</span><span class="sxs-lookup"><span data-stu-id="80446-147">The main article for that section is called *index.md*.</span></span>

<span data-ttu-id="80446-148">对于映像和其他静态资源，请在包含文章的文件夹中创建称为“media”的子文件夹（如果尚不存在）。</span><span class="sxs-lookup"><span data-stu-id="80446-148">For images and other static resources, create a subfolder called **media** inside the folder that contains your article, if it doesn't already exist.</span></span> <span data-ttu-id="80446-149">在“media”文件夹内，创建具有文章名称的子文件夹（索引文件除外）。</span><span class="sxs-lookup"><span data-stu-id="80446-149">Inside the **media** folder, create a subfolder with the article name (except for the index file).</span></span>

<span data-ttu-id="80446-150">对于代码片段，请在包含你的文章的文件夹中创建一个名为“snippets”的子文件夹（如果尚不存在） 。</span><span class="sxs-lookup"><span data-stu-id="80446-150">For **code snippets**, create a subfolder called **snippets** inside the folder that contains your article, if it doesn't already exist.</span></span> <span data-ttu-id="80446-151">在“代码片段”文件夹中，创建包含文章名称的子文件夹。</span><span class="sxs-lookup"><span data-stu-id="80446-151">Inside the **snippets** folder, create a subfolder with the article name.</span></span> <span data-ttu-id="80446-152">在大多数情况下，你将具有全部三种主要的 .NET 语言（C#、F# 和 Visual Basic）的代码片段。</span><span class="sxs-lookup"><span data-stu-id="80446-152">In most cases, you'll have code snippets for all three of the main .NET languages, C#, F#, and Visual Basic.</span></span> <span data-ttu-id="80446-153">在此情况下，请为三个项目中的每一个分别创建名为“csharp”、“fsharp”和“vb”的子文件夹  。</span><span class="sxs-lookup"><span data-stu-id="80446-153">In that case, create subfolders named **csharp**, **fsharp**, and **vb** for each of the three projects.</span></span> <span data-ttu-id="80446-154">如果要在 [docs/csharp](https://github.com/dotnet/docs/tree/master/docs/csharp)、[docs/fsharp](https://github.com/dotnet/docs/tree/master/docs/fsharp) 或 [docs/visual-basic](https://github.com/dotnet/docs/tree/master/docs/visual-basic) 文件夹下为一篇文章创建代码片段，此代码片段只能采用一种语言，你才能忽略语言子文件夹。</span><span class="sxs-lookup"><span data-stu-id="80446-154">If you're creating a snippet for an article under the [docs/csharp](https://github.com/dotnet/docs/tree/master/docs/csharp), [docs/fsharp](https://github.com/dotnet/docs/tree/master/docs/fsharp), or [docs/visual-basic](https://github.com/dotnet/docs/tree/master/docs/visual-basic) folders, the snippet will only be in one language so you can omit the language subfolder.</span></span>

<span data-ttu-id="80446-155">代码片段很小，侧重于展示文章中所述概念的代码的示例。</span><span class="sxs-lookup"><span data-stu-id="80446-155">Code snippets are small, focused examples of code that demonstrate the concepts covered in an article.</span></span> <span data-ttu-id="80446-156">用于下载和查看的更大型程序应放置在 [dotnet/samples](https://github.com/dotnet/samples) 存储库中。</span><span class="sxs-lookup"><span data-stu-id="80446-156">Larger programs intended for download and exploration should be located in the [dotnet/samples](https://github.com/dotnet/samples) repository.</span></span> <span data-ttu-id="80446-157">所有示例都在[参与撰写示例](#contribute-to-samples)部分中有所介绍。</span><span class="sxs-lookup"><span data-stu-id="80446-157">Full samples are covered in the section on [Contributing to samples](#contribute-to-samples).</span></span>

## <a name="example-folder-structure"></a><span data-ttu-id="80446-158">文件夹结构示例</span><span class="sxs-lookup"><span data-stu-id="80446-158">Example folder structure</span></span>

```
docs
  /about
  /core
    /porting
      porting-overview.md
      /media
        /porting-overview
          portability_report.png
      /snippets
        /porting-overview
          /csharp
            porting.csproj
            porting-overview.cs
            Program.cs
          /fsharp
            porting.fsproj
            porting-overview.fs
            Program.fs
          /vb
            porting.vbproj
            porting-overview.vb
            Program.vb
```

<span data-ttu-id="80446-159">上面所示结构包含一张图像 portability_report.png，还有三个包含代码片段的代码项目，它们都包含在 porting-overview.md 文章中。</span><span class="sxs-lookup"><span data-stu-id="80446-159">The structure shown above includes one image, *portability_report.png*, and three code projects that include **code snippets** that are included in the *porting-overview.md* article.</span></span> <span data-ttu-id="80446-160">在所接受的备用结构中，每种语言都有一个项目，其中包含该文件夹中所有文章的所有片段。</span><span class="sxs-lookup"><span data-stu-id="80446-160">An accepted alternative structure contains one project per language that contains all snippets for all articles in that folder.</span></span> <span data-ttu-id="80446-161">这一备用结构已在语言参考区域中使用，因为用非常小的片段来展示语言语法。</span><span class="sxs-lookup"><span data-stu-id="80446-161">This alternative has been used in the language reference areas because of very small snippets to demonstrate language syntax.</span></span> <span data-ttu-id="80446-162">建议不要在其他区域中使用此结构。</span><span class="sxs-lookup"><span data-stu-id="80446-162">It is discouraged in other areas.</span></span>

<span data-ttu-id="80446-163">由于历史原因，很多包含的片段存储在 dotnet/docs 存储库的 /samples 文件夹下 。</span><span class="sxs-lookup"><span data-stu-id="80446-163">For historical reasons, many of the included snippets are stored under the */samples* folder in the *dotnet/docs* repository.</span></span> <span data-ttu-id="80446-164">如果要对某篇文章进行重大更改，应将这些片段移到新的结构。</span><span class="sxs-lookup"><span data-stu-id="80446-164">If you're making major changes to an article, those snippets should be moved to the new structure.</span></span> <span data-ttu-id="80446-165">如果是细小改动，则不要移动片段。</span><span class="sxs-lookup"><span data-stu-id="80446-165">Do not move snippets for small changes.</span></span>

<span data-ttu-id="80446-166">**步骤 4：** 从分支向主分支提交拉取请求 (PR)。</span><span class="sxs-lookup"><span data-stu-id="80446-166">**Step 4:** Submit a Pull Request (PR) from your branch to the master branch.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="80446-167">任何 .NET 文档存储库中的[评论自动化](../how-to-write-workflows-major.md#review-and-sign-off)功能均暂不可用。</span><span class="sxs-lookup"><span data-stu-id="80446-167">The [comment automation](../how-to-write-workflows-major.md#review-and-sign-off) functionality is not available on any of the .NET docs repositories at this time.</span></span> <span data-ttu-id="80446-168">.NET 文档团队成员将评审和合并 PR。</span><span class="sxs-lookup"><span data-stu-id="80446-168">Members of the .NET docs team will review and merge your PR.</span></span>

<span data-ttu-id="80446-169">每个 PR 通常一次只处理一个问题。</span><span class="sxs-lookup"><span data-stu-id="80446-169">Each PR should usually address one issue at a time.</span></span> <span data-ttu-id="80446-170">PR 可修改一个或多个文件。</span><span class="sxs-lookup"><span data-stu-id="80446-170">The PR can modify one or multiple files.</span></span> <span data-ttu-id="80446-171">如果要处理不同文件上的多个修复，首选单独的 PR。</span><span class="sxs-lookup"><span data-stu-id="80446-171">If you're addressing multiple fixes on different files, separate PRs are preferred.</span></span> <span data-ttu-id="80446-172">如果要创建示例以及更新标记，则需要为示例创建单独的 PR。</span><span class="sxs-lookup"><span data-stu-id="80446-172">If you're creating samples as well as updating markdown, you'll need to create a separate PR for samples.</span></span>

<span data-ttu-id="80446-173">如果 PR 可修复现有问题，请在提交消息或 PR 说明中添加 `Fixes #Issue_Number` 关键字。</span><span class="sxs-lookup"><span data-stu-id="80446-173">If your PR fixes an existing issue, add the `Fixes #Issue_Number` keyword to the commit message or PR description.</span></span> <span data-ttu-id="80446-174">如此，PR 合并时，问题将自动关闭。</span><span class="sxs-lookup"><span data-stu-id="80446-174">That way, the issue is automatically closed when the PR is merged.</span></span> <span data-ttu-id="80446-175">有关详细信息，请参阅[通过提交消息关闭问题](https://help.github.com/articles/closing-issues-via-commit-messages/)。</span><span class="sxs-lookup"><span data-stu-id="80446-175">For more information, see [Closing issues via commit messages](https://help.github.com/articles/closing-issues-via-commit-messages/).</span></span>

<span data-ttu-id="80446-176">.NET 团队将评审 PR 并告知你是否存在必需的其他任何更新/更改，以进行审批。</span><span class="sxs-lookup"><span data-stu-id="80446-176">The .NET team will review your PR and let you know if there are any other updates/changes necessary in order to approve it.</span></span>

<span data-ttu-id="80446-177">**步骤 5：** 与团队讨论时，对分支进行任何必需的更新。</span><span class="sxs-lookup"><span data-stu-id="80446-177">**Step 5:** Make any necessary updates to your branch as discussed with the team.</span></span>

<span data-ttu-id="80446-178">反馈应用后且更改得到审批后，维护程序会将 PR 合并为主分支。</span><span class="sxs-lookup"><span data-stu-id="80446-178">The maintainers will merge your PR into the master branch once feedback has been applied and your change is approved.</span></span>

<span data-ttu-id="80446-179">我们将定期从主分支将所有提交推送到实时分支，然后便能够在 https://docs.microsoft.com/dotnet/ 实时查看你的参与。</span><span class="sxs-lookup"><span data-stu-id="80446-179">We regularly push all commits from master branch into the live branch and then you'll be able to see your contribution live at https://docs.microsoft.com/dotnet/.</span></span> <span data-ttu-id="80446-180">通常我们会在工作周期间每日发布。</span><span class="sxs-lookup"><span data-stu-id="80446-180">We typically publish daily during the work week.</span></span>

## <a name="contribute-to-samples"></a><span data-ttu-id="80446-181">参与示例撰写</span><span class="sxs-lookup"><span data-stu-id="80446-181">Contribute to samples</span></span>

<span data-ttu-id="80446-182">我们对支持我们内容的代码进行了以下区分：</span><span class="sxs-lookup"><span data-stu-id="80446-182">We make the following distinction for code that supports our content:</span></span>

- <span data-ttu-id="80446-183">示例：读者可以下载并运行示例。</span><span class="sxs-lookup"><span data-stu-id="80446-183">Samples: readers can download and run the samples.</span></span> <span data-ttu-id="80446-184">所有示例都应是完整的应用程序或库。</span><span class="sxs-lookup"><span data-stu-id="80446-184">All samples should be complete applications or libraries.</span></span> <span data-ttu-id="80446-185">如果示例创建库，该库应包括单元测试或允许读者运行代码的应用程序。</span><span class="sxs-lookup"><span data-stu-id="80446-185">Where the sample creates a library, it should include unit tests or an application that lets readers run the code.</span></span> <span data-ttu-id="80446-186">它们通常使用多种技术、功能或工具包。</span><span class="sxs-lookup"><span data-stu-id="80446-186">They often use more than one technology, feature, or toolkit.</span></span> <span data-ttu-id="80446-187">每个示例的 readme.md 文件都将引用文章，使你能够深入了解每个示例中涉及的概念。</span><span class="sxs-lookup"><span data-stu-id="80446-187">The readme.md file for each sample will refer to the article so that you can read more about the concepts covered in each sample.</span></span>
- <span data-ttu-id="80446-188">代码片段：说明较小概念或任务。</span><span class="sxs-lookup"><span data-stu-id="80446-188">Snippets: illustrate a smaller concept or task.</span></span> <span data-ttu-id="80446-189">它们进行编译但不打算成为完整的应用程序。</span><span class="sxs-lookup"><span data-stu-id="80446-189">They compile but they are not intended to be complete applications.</span></span> <span data-ttu-id="80446-190">它们应正常运行，但不是典型方案的示例应用程序。</span><span class="sxs-lookup"><span data-stu-id="80446-190">They should run correctly, but aren't an example application for a typical scenario.</span></span> <span data-ttu-id="80446-191">相反，它们旨在尽可能小，以说明单个概念或功能。</span><span class="sxs-lookup"><span data-stu-id="80446-191">Instead, they are designed to be as small as possible to illustrate a single concept or feature.</span></span> <span data-ttu-id="80446-192">这些应只是一个屏幕的代码。</span><span class="sxs-lookup"><span data-stu-id="80446-192">These should be no more than a single screen of code.</span></span>

<span data-ttu-id="80446-193">示例存储在 [dotnet/samples](https://github.com/dotnet/samples) 存储库中。</span><span class="sxs-lookup"><span data-stu-id="80446-193">Samples are stored in the [dotnet/samples](https://github.com/dotnet/samples) repository.</span></span> <span data-ttu-id="80446-194">我们正在努力构建一个模型，其中示例文件夹结构匹配文档文件夹结构。</span><span class="sxs-lookup"><span data-stu-id="80446-194">We are working toward a model where our samples folder structure matches our docs folder structure.</span></span> <span data-ttu-id="80446-195">所遵循的标准有：</span><span class="sxs-lookup"><span data-stu-id="80446-195">Standards that we follow are:</span></span>

- <span data-ttu-id="80446-196">顶层文件夹与 docs 存储库中的顶层文件夹相匹配。</span><span class="sxs-lookup"><span data-stu-id="80446-196">Top-level folders match the top level folders in the *docs* repository.</span></span> <span data-ttu-id="80446-197">例如，文档存储库包含“machine-learning/tutorials”文件夹，并且机器学习教程的示例位于“samples/machine-learning/tutorials”文件夹中 。</span><span class="sxs-lookup"><span data-stu-id="80446-197">For example, the docs repository has a *machine-learning/tutorials* folder, and the samples for machine learning tutorials are in the *samples/machine-learning/tutorials* folder.</span></span>

<span data-ttu-id="80446-198">此外，核心和标准文件夹下的所有示例都应在 .NET Core 支持的所有平台上生成并运行 。</span><span class="sxs-lookup"><span data-stu-id="80446-198">In addition, all samples under the *core* and *standard* folders should build and run on all platforms supported by .NET Core.</span></span> <span data-ttu-id="80446-199">CI 生成系统将强制执行该操作。</span><span class="sxs-lookup"><span data-stu-id="80446-199">Our CI build system will enforce that.</span></span> <span data-ttu-id="80446-200">顶层“framework”文件夹包含仅在 Windows 上生成和验证的示例。</span><span class="sxs-lookup"><span data-stu-id="80446-200">The top level *framework* folder contains samples that are only built and validated on Windows.</span></span>

<span data-ttu-id="80446-201">示例项目应在针对给定示例可能的最广泛的一组平台上生成和运行。</span><span class="sxs-lookup"><span data-stu-id="80446-201">Sample projects should build and run on the widest set of platforms possible for the given sample.</span></span> <span data-ttu-id="80446-202">实际上，这表示在可能的位置生成基于 .NET Core 的控制台应用程序。</span><span class="sxs-lookup"><span data-stu-id="80446-202">In practice, that means building .NET Core-based console applications where possible.</span></span> <span data-ttu-id="80446-203">特定于 Web 或 UI 框架的示例应根据需要添加这些工具。</span><span class="sxs-lookup"><span data-stu-id="80446-203">Samples that are specific to the web or a UI framework should add those tools as needed.</span></span> <span data-ttu-id="80446-204">示例有 Web 应用程序、移动应用、WPF 或 WinForms 应用等。</span><span class="sxs-lookup"><span data-stu-id="80446-204">Examples include web applications, mobile apps, WPF or WinForms apps, and so on.</span></span>

<span data-ttu-id="80446-205">我们正在努力实现适用于所有代码的 CI 系统。</span><span class="sxs-lookup"><span data-stu-id="80446-205">We are working toward having a CI system in place for all code.</span></span> <span data-ttu-id="80446-206">当对示例进行任何更新时，请确保每个更新都属于可生成项目。</span><span class="sxs-lookup"><span data-stu-id="80446-206">When you make any updates to samples, make sure each update is part of a buildable project.</span></span> <span data-ttu-id="80446-207">理想情况下，还可添加针对示例正确性的测试。</span><span class="sxs-lookup"><span data-stu-id="80446-207">Ideally, add tests for correctness on samples as well.</span></span>

<span data-ttu-id="80446-208">创建的每个完整示例都应包含 readme.md 文件。</span><span class="sxs-lookup"><span data-stu-id="80446-208">Each complete sample that you create should contain a *readme.md* file.</span></span> <span data-ttu-id="80446-209">此文件应包含有关示例的简短说明（一到两个段落）。</span><span class="sxs-lookup"><span data-stu-id="80446-209">This file should contain a short description of the sample (one or two paragraphs).</span></span> <span data-ttu-id="80446-210">Readme.md 应告知读者通过浏览此示例，可以学到什么内容。</span><span class="sxs-lookup"><span data-stu-id="80446-210">Your *readme.md* should tell readers what they will learn by exploring this sample.</span></span> <span data-ttu-id="80446-211">此外，readme.md 文件还应包含一个链接，指向 [.NET 文档站点](https://docs.microsoft.com/dotnet/welcome)上的实时文档。</span><span class="sxs-lookup"><span data-stu-id="80446-211">The *readme.md* file should also contain a link to the live document on the [.NET documentation site](https://docs.microsoft.com/dotnet/welcome).</span></span> <span data-ttu-id="80446-212">若要确定存储库中给定文件映射到该站点的位置，请将存储库路径中的 `/docs` 替换为 `https://docs.microsoft.com/dotnet`。</span><span class="sxs-lookup"><span data-stu-id="80446-212">To determine where a given file in the repository maps to that site, replace `/docs` in the repository path with `https://docs.microsoft.com/dotnet`.</span></span>

<span data-ttu-id="80446-213">此外，主题还将包含指向该示例的链接。</span><span class="sxs-lookup"><span data-stu-id="80446-213">Your topic will also contain links to the sample.</span></span> <span data-ttu-id="80446-214">直接链接到 GitHub 上的示例文件夹。</span><span class="sxs-lookup"><span data-stu-id="80446-214">Link directly to the sample's folder on GitHub.</span></span>

### <a name="write-a-new-sample"></a><span data-ttu-id="80446-215">编写新示例</span><span class="sxs-lookup"><span data-stu-id="80446-215">Write a new sample</span></span>

<span data-ttu-id="80446-216">示例是可供下载的完整程序和库。</span><span class="sxs-lookup"><span data-stu-id="80446-216">Samples are full programs and libraries meant for download.</span></span> <span data-ttu-id="80446-217">它们的范围可能很小，但以一种用户能自行浏览和试验的方式对概念进行了展示。</span><span class="sxs-lookup"><span data-stu-id="80446-217">They may be small in scope, but they demonstrate concepts in a manner that enables people to explore and experiment on their own.</span></span> <span data-ttu-id="80446-218">示例指南确保读者可下载和浏览。</span><span class="sxs-lookup"><span data-stu-id="80446-218">The guidelines for samples ensure readers can download and explore.</span></span> <span data-ttu-id="80446-219">请查看[并行 LINQ (PLINQ)](https://github.com/dotnet/samples/tree/master/csharp/parallel/PLINQ) 示例，它们是每份指南中的例子。</span><span class="sxs-lookup"><span data-stu-id="80446-219">Examine the [Parallel LINQ (PLINQ)](https://github.com/dotnet/samples/tree/master/csharp/parallel/PLINQ) samples as an example of each of the guidelines.</span></span>

1. <span data-ttu-id="80446-220">示例必须属于可生成项目的一部分。</span><span class="sxs-lookup"><span data-stu-id="80446-220">Your sample **must be part of a buildable project**.</span></span> <span data-ttu-id="80446-221">如果可能，应在 .NET Core 支持的所有平台上生成项目。</span><span class="sxs-lookup"><span data-stu-id="80446-221">Where possible, the projects should build on all platforms supported by .NET Core.</span></span> <span data-ttu-id="80446-222">此情况的例外是演示平台特定功能或平台特定工具的示例。</span><span class="sxs-lookup"><span data-stu-id="80446-222">Exceptions to this are samples that demonstrate a platform specific feature or platform specific tool.</span></span>

2. <span data-ttu-id="80446-223">示例应符合 [corefx 编码样式](https://github.com/dotnet/corefx/blob/master/Documentation/coding-guidelines/coding-style.md)，以保持一致性。</span><span class="sxs-lookup"><span data-stu-id="80446-223">Your sample should conform to the [corefx coding style](https://github.com/dotnet/corefx/blob/master/Documentation/coding-guidelines/coding-style.md) to maintain consistency.</span></span>

   <span data-ttu-id="80446-224">此外，演示不需要初始化新对象的内容时，我们首选 `static` 方法，而不是实例方法。</span><span class="sxs-lookup"><span data-stu-id="80446-224">Additionally, we prefer the use of `static` methods rather than instance methods when demonstrating something that doesn't require instantiating a new object.</span></span>

3. <span data-ttu-id="80446-225">示例应包括适当的异常处理。</span><span class="sxs-lookup"><span data-stu-id="80446-225">Your sample should include **appropriate exception handling**.</span></span> <span data-ttu-id="80446-226">它应处理可能在示例的上下文中引发的所有异常。</span><span class="sxs-lookup"><span data-stu-id="80446-226">It should handle all exceptions that are likely to be thrown in the context of the sample.</span></span> <span data-ttu-id="80446-227">例如，当输入字符串以参数形式传递给方法时，调用 [Console.ReadLine](https://docs.microsoft.com/dotnet/api/system.console.readline) 方法以检索用户输入的示例应使用适当的异常处理。</span><span class="sxs-lookup"><span data-stu-id="80446-227">For example, a sample that calls the [Console.ReadLine](https://docs.microsoft.com/dotnet/api/system.console.readline) method to retrieve user input should use appropriate exception handling when the input string is passed as an argument to a method.</span></span> <span data-ttu-id="80446-228">同样，如果示例需要方法调用失败，则必须处理导致的异常。</span><span class="sxs-lookup"><span data-stu-id="80446-228">Similarly, if your sample expects a method call to fail, the resulting exception must be handled.</span></span> <span data-ttu-id="80446-229">请始终处理方法引发的特定异常，而不是基类异常，例如 [Exception](https://docs.microsoft.com/dotnet/api/system.exception) 或 [SystemException](https://docs.microsoft.com/dotnet/api/system.systemexception)。</span><span class="sxs-lookup"><span data-stu-id="80446-229">Always handle the specific exceptions thrown by the method, rather than base class exceptions such as [Exception](https://docs.microsoft.com/dotnet/api/system.exception) or [SystemException](https://docs.microsoft.com/dotnet/api/system.systemexception).</span></span>

4. <span data-ttu-id="80446-230">如果示例生成独立包，除示例所用的任何运行时外，还必须包含 CI 生成系统所用的运行时：</span><span class="sxs-lookup"><span data-stu-id="80446-230">If your sample builds a standalone package, you must include the runtimes used by our CI build system, in addition to any runtimes used by your sample:</span></span>
    - `win7-x64`
    - `win8-x64`
    - `win81-x64`
    - `ubuntu.16.04-x64`

<span data-ttu-id="80446-231">我们将提供一个 CI 系统，以暂时生成这些项目。</span><span class="sxs-lookup"><span data-stu-id="80446-231">We will have a CI system in place to build these projects shortly.</span></span>

<span data-ttu-id="80446-232">创建示例：</span><span class="sxs-lookup"><span data-stu-id="80446-232">To create a sample:</span></span>

1. <span data-ttu-id="80446-233">提交[问题](https://github.com/dotnet/docs/issues)，或向正在处理的现有问题添加注释。</span><span class="sxs-lookup"><span data-stu-id="80446-233">File an [issue](https://github.com/dotnet/docs/issues) or add a comment to an existing one that you are working on it.</span></span>
2. <span data-ttu-id="80446-234">编写解释示例中演示的概念的主题（例如：`docs/standard/linq/where-clause.md`）。</span><span class="sxs-lookup"><span data-stu-id="80446-234">Write the topic that explains the concepts demonstrated in your sample (example: `docs/standard/linq/where-clause.md`).</span></span>
3. <span data-ttu-id="80446-235">编写示例（例如：`WhereClause-Sample1.cs`）。</span><span class="sxs-lookup"><span data-stu-id="80446-235">Write your sample (example: `WhereClause-Sample1.cs`).</span></span>
4. <span data-ttu-id="80446-236">使用调用示例的主要入口点创建 Program.cs。</span><span class="sxs-lookup"><span data-stu-id="80446-236">Create a Program.cs with a Main entry point that calls your samples.</span></span> <span data-ttu-id="80446-237">如果已有一个，则添加对示例的调用：</span><span class="sxs-lookup"><span data-stu-id="80446-237">If there is already one there, add the call to your sample:</span></span>

    ```csharp
    public class Program
    {
        public void Main(string[] args)
        {
            WhereClause1.QuerySyntaxExample();

            // Add the method syntax as an example.
            WhereClause1.MethodSyntaxExample();
        }
    }
    ```

<span data-ttu-id="80446-238">使用 .NET Core CLI 生成任何 .NET Core 代码片段或示例，可与 [.NET Core SDK](https://www.microsoft.com/net/download) 一起安装。</span><span class="sxs-lookup"><span data-stu-id="80446-238">You build any .NET Core snippet or sample using the .NET Core CLI, which can be installed with [the .NET Core SDK](https://www.microsoft.com/net/download).</span></span> <span data-ttu-id="80446-239">生成并运行示例：</span><span class="sxs-lookup"><span data-stu-id="80446-239">To build and run your sample:</span></span>

1. <span data-ttu-id="80446-240">转到示例文件夹和生成，查看其中的错误：</span><span class="sxs-lookup"><span data-stu-id="80446-240">Go to the sample folder and build to check for errors:</span></span>

    ```console
    dotnet build
    ```
2. <span data-ttu-id="80446-241">运行示例：</span><span class="sxs-lookup"><span data-stu-id="80446-241">Run your sample:</span></span>

    ```console
    dotnet run
    ```

3. <span data-ttu-id="80446-242">向示例的根目录添加 readme.md。</span><span class="sxs-lookup"><span data-stu-id="80446-242">Add a readme.md to the root directory of your sample.</span></span>

   <span data-ttu-id="80446-243">这应包括代码的简短说明，并使用户参考引用该示例的文章。</span><span class="sxs-lookup"><span data-stu-id="80446-243">This should include a brief description of the code, and refer people to the article that references the sample.</span></span> <span data-ttu-id="80446-244">readme.md 的顶端必须具有[示例浏览器](https://docs.microsoft.com/samples)所需的元数据。</span><span class="sxs-lookup"><span data-stu-id="80446-244">The top of the *readme.md* must have the metadata required for the [samples browser](https://docs.microsoft.com/samples).</span></span> <span data-ttu-id="80446-245">头信息块应包含以下字段：</span><span class="sxs-lookup"><span data-stu-id="80446-245">The header block should contain the following fields:</span></span>

   ```yml
   ---
   name: "really cool sample"
   description: "Learn everything about this really cool sample."
   page_type: sample
   languages:
     - csharp
     - fsharp
     - vbnet
   products:
     - dotnet-core
     - dotnet
     - dotnet-standard
     - aspnet
     - aspnet-core
     - ef-core
   ---
   ```

   - <span data-ttu-id="80446-246">`languages` 集合应只包含可用于你的示例的语言。</span><span class="sxs-lookup"><span data-stu-id="80446-246">The `languages` collection should include only those languages available for your sample.</span></span>
   - <span data-ttu-id="80446-247">`products` 集合应只包括与你的示例相关的产品。</span><span class="sxs-lookup"><span data-stu-id="80446-247">The `products` collection should include only those products relevant to your sample.</span></span>

<span data-ttu-id="80446-248">备注除外，所有示例均通过 .NET Core 支持的任何平台上的命令行生成。</span><span class="sxs-lookup"><span data-stu-id="80446-248">Except where noted, all samples build from the command line on any platform supported by .NET Core.</span></span> <span data-ttu-id="80446-249">有一些特定于 Visual Studio 的示例，需要 Visual Studio 2017 或更高版本。</span><span class="sxs-lookup"><span data-stu-id="80446-249">There are a few samples that are specific to Visual Studio and require Visual Studio 2017 or later.</span></span> <span data-ttu-id="80446-250">此外，部分示例还展示了平台特定的功能，并且需要特定的平台。</span><span class="sxs-lookup"><span data-stu-id="80446-250">In addition, some samples show platform specific features and will require a specific platform.</span></span> <span data-ttu-id="80446-251">其他示例和代码片段需要 .NET Framework，且将在 Windows 平台上运行，需要适用于目标 Framework 版本的开发人员工具包。</span><span class="sxs-lookup"><span data-stu-id="80446-251">Other samples and snippets require the .NET Framework and will run on Windows platforms, and will need the Developer Pack for the target Framework version.</span></span>

## <a name="the-c-interactive-experience"></a><span data-ttu-id="80446-252">C# 交互式体验</span><span class="sxs-lookup"><span data-stu-id="80446-252">The C# interactive experience</span></span>

<span data-ttu-id="80446-253">文章中包括的所有示例均使用[语言标记](../code-in-docs.md)指示源语言。</span><span class="sxs-lookup"><span data-stu-id="80446-253">All samples included in an article use a [language tag](../code-in-docs.md) to indicate the source language.</span></span> <span data-ttu-id="80446-254">采用 C# 的短代码示例可使用 `csharp-interactive` 语言标记指定在浏览器中运行的 C# 示例。</span><span class="sxs-lookup"><span data-stu-id="80446-254">Short code samples in C# can use the `csharp-interactive` language tag to specify a C# sample that runs in the browser.</span></span> <span data-ttu-id="80446-255">（内联代码示例使用 `csharp-interactive` 标记，对于源中包括的代码示例，请使用 `code-csharp-interactive` 标记。）这些代码示例在文中显示一个代码窗口和一个输出窗口。</span><span class="sxs-lookup"><span data-stu-id="80446-255">(Inline code samples use the `csharp-interactive` tag, for snippets included from source, use the `code-csharp-interactive` tag.) These code samples display a code window and an output window in the article.</span></span> <span data-ttu-id="80446-256">输出窗口显示用户运行示例后，执行交互式代码的任何输出。</span><span class="sxs-lookup"><span data-stu-id="80446-256">The output window displays any output from executing the interactive code once the user has run the sample.</span></span>

<span data-ttu-id="80446-257">C# 交互式体验改变了我们使用示例的方式。</span><span class="sxs-lookup"><span data-stu-id="80446-257">The C# interactive experience changes how we work with samples.</span></span> <span data-ttu-id="80446-258">访问者可运行示例，查看结果。</span><span class="sxs-lookup"><span data-stu-id="80446-258">Visitors can run the sample to see the results.</span></span> <span data-ttu-id="80446-259">有许多因素有助于确定示例或对应的文本是否应包括输出的相关信息。</span><span class="sxs-lookup"><span data-stu-id="80446-259">A number of factors help determine if the sample or corresponding text should include information about the output.</span></span>

### <a name="when-to-display-the-expected-output-without-running-the-sample"></a><span data-ttu-id="80446-260">何时显示预期输出，而无需运行示例</span><span class="sxs-lookup"><span data-stu-id="80446-260">When to display the expected output without running the sample</span></span>

- <span data-ttu-id="80446-261">针对初学者的文章应提供输出，以便读者可将其工作的输出与预期答案进行比较。</span><span class="sxs-lookup"><span data-stu-id="80446-261">Articles intended for beginners should provide output so that readers can compare the output of their work with the expected answer.</span></span>
- <span data-ttu-id="80446-262">其中的输出对主题至关重要的示例应显示该输出。</span><span class="sxs-lookup"><span data-stu-id="80446-262">Samples where the output is integral to the topic should display that output.</span></span> <span data-ttu-id="80446-263">例如，有关格式化文本的文章应显示格式，而无需运行示例。</span><span class="sxs-lookup"><span data-stu-id="80446-263">For example, articles on formatted text should show the text format without running the sample.</span></span>
- <span data-ttu-id="80446-264">如果示例和预期输出均简短，请考虑显示输出。</span><span class="sxs-lookup"><span data-stu-id="80446-264">When both the sample and the expected output is short, consider showing the output.</span></span> <span data-ttu-id="80446-265">可节省一些时间。</span><span class="sxs-lookup"><span data-stu-id="80446-265">It saves a bit of time.</span></span>
- <span data-ttu-id="80446-266">介绍当前区域性或固定区域性如何影响输出的文章应介绍预期输出。</span><span class="sxs-lookup"><span data-stu-id="80446-266">Articles explaining how current culture or invariant culture affect output should explain the expected output.</span></span> <span data-ttu-id="80446-267">交互式 REPL（读取–求值–打印循环）在基于 Linux 的主机上运行。</span><span class="sxs-lookup"><span data-stu-id="80446-267">The interactive REPL (Read Evaluate Print Loop) runs on a Linux-based host.</span></span> <span data-ttu-id="80446-268">默认区域性和固定区域性在不同的操作系统和计算机上可生成不同的输出。</span><span class="sxs-lookup"><span data-stu-id="80446-268">The default culture, and the invariant culture produce different output on different operating systems and machines.</span></span> <span data-ttu-id="80446-269">文章应说明 Windows、Linux 和 Mac 系统中的输出。</span><span class="sxs-lookup"><span data-stu-id="80446-269">The article should explain the output in Windows, Linux, and Mac systems.</span></span>

### <a name="when-to-exclude-expected-output-from-the-sample"></a><span data-ttu-id="80446-270">何时从示例中排除预期输出</span><span class="sxs-lookup"><span data-stu-id="80446-270">When to exclude expected output from the sample</span></span>

- <span data-ttu-id="80446-271">其中的示例生成较大输出的文章不应在注释中包括该内容。</span><span class="sxs-lookup"><span data-stu-id="80446-271">Articles where the sample generates a larger output should not include that in comments.</span></span> <span data-ttu-id="80446-272">示例运行后，它将使代码难以理解。</span><span class="sxs-lookup"><span data-stu-id="80446-272">It obscures the code once the sample has been run.</span></span>
- <span data-ttu-id="80446-273">其中的示例演示主题的文章，但输出对理解该文章不甚重要。</span><span class="sxs-lookup"><span data-stu-id="80446-273">Articles where the sample demonstrates a topic, but the output isn't integral to understanding it.</span></span> <span data-ttu-id="80446-274">例如，运行 LINQ 查询以说明查询语法的代码，然后该代码显示输出集合中的每个项。</span><span class="sxs-lookup"><span data-stu-id="80446-274">For example, code that runs a LINQ query to explain query syntax and then display every item in the output collection.</span></span>

> [!NOTE]
> <span data-ttu-id="80446-275">你可能已注意到，部分主题当前不遵循此处指定的所有准则。</span><span class="sxs-lookup"><span data-stu-id="80446-275">You might notice that some of the topics are not currently following all the guidelines specified here.</span></span> <span data-ttu-id="80446-276">我们正在努力实现整个网站中的一致性。</span><span class="sxs-lookup"><span data-stu-id="80446-276">We're working towards achieving consistency throughout the site.</span></span> <span data-ttu-id="80446-277">查看我们目前正在针对该特定目标跟踪的[未决问题](https://github.com/dotnet/docs/issues?q=is%3Aopen+is%3Aissue+label%3A%22%3Abookmark_tabs%3A+Information+Architecture%22)列表。</span><span class="sxs-lookup"><span data-stu-id="80446-277">Check the list of [open issues](https://github.com/dotnet/docs/issues?q=is%3Aopen+is%3Aissue+label%3A%22%3Abookmark_tabs%3A+Information+Architecture%22) we're currently tracking for that specific goal.</span></span>

### <a name="contributing-to-international-content"></a><span data-ttu-id="80446-278">参与全球内容</span><span class="sxs-lookup"><span data-stu-id="80446-278">Contributing to International content</span></span>

<span data-ttu-id="80446-279">当前不接受参与机器翻译 (MT) 内容。</span><span class="sxs-lookup"><span data-stu-id="80446-279">Contributions for Machine Translated (MT) content are currently not accepted.</span></span> <span data-ttu-id="80446-280">为了提高 MT 内容的质量，我们进行了转换，现使用神经 MT 引擎。</span><span class="sxs-lookup"><span data-stu-id="80446-280">In an effort to improve the quality of MT content, we've transitioned to a Neural MT engine.</span></span> <span data-ttu-id="80446-281">我们接受并鼓励参与人工翻译 (HT) 内容，该内容用来训练神经 MT 引擎。</span><span class="sxs-lookup"><span data-stu-id="80446-281">We accept and encourage contributions for Human Translated (HT) content, which is used to train the Neural MT engine.</span></span> <span data-ttu-id="80446-282">随着时间的推移，对 HT 内容的参与将提高 HT 和 MT 这两者的质量。</span><span class="sxs-lookup"><span data-stu-id="80446-282">So over time, contributions to HT content will improve the quality of both HT and MT.</span></span> <span data-ttu-id="80446-283">MT 主题将包含一条免责声明，其中指出主题的一部分可能是机器翻译，而由于已禁止编辑，因此将不显示“编辑”按钮。</span><span class="sxs-lookup"><span data-stu-id="80446-283">MT topics will have a disclaimer stating that part of the topic may be MT, and the **Edit** button won't be displayed, as editing is disabled.</span></span>

## <a name="contributor-license-agreement"></a><span data-ttu-id="80446-284">参与者许可协议</span><span class="sxs-lookup"><span data-stu-id="80446-284">Contributor license agreement</span></span>

<span data-ttu-id="80446-285">在合并 PR 前，必须先签署 [.NET Foundation 参与许可协议 (CLA)](https://cla.dotnetfoundation.org)。</span><span class="sxs-lookup"><span data-stu-id="80446-285">You must sign the [.NET Foundation Contribution License Agreement (CLA)](https://cla.dotnetfoundation.org) before your PR is merged.</span></span> <span data-ttu-id="80446-286">这是针对 .NET Foundation 中的项目的一次性要求。</span><span class="sxs-lookup"><span data-stu-id="80446-286">This is a one-time requirement for projects in the .NET Foundation.</span></span> <span data-ttu-id="80446-287">可在 Wikipedia 上了解有关[参与许可协议 (CLA)](http://en.wikipedia.org/wiki/Contributor_License_Agreement) 的详细信息。</span><span class="sxs-lookup"><span data-stu-id="80446-287">You can read more about [Contribution License Agreements (CLA)](http://en.wikipedia.org/wiki/Contributor_License_Agreement) on Wikipedia.</span></span>

<span data-ttu-id="80446-288">协议：[net-foundation-contribution-license-agreement.pdf](https://github.com/dotnet/home/blob/master/guidance/net-foundation-contribution-license-agreement.pdf)</span><span class="sxs-lookup"><span data-stu-id="80446-288">The agreement: [net-foundation-contribution-license-agreement.pdf](https://github.com/dotnet/home/blob/master/guidance/net-foundation-contribution-license-agreement.pdf)</span></span>

<span data-ttu-id="80446-289">无需提前签署协议。</span><span class="sxs-lookup"><span data-stu-id="80446-289">You don't have to sign the agreement up-front.</span></span> <span data-ttu-id="80446-290">可以照常克隆 PR、创建 PR 分支或提交 PR。</span><span class="sxs-lookup"><span data-stu-id="80446-290">You can clone, fork, and submit your PR as usual.</span></span> <span data-ttu-id="80446-291">创建 PR 时，由 CLA 机器人进行分类。</span><span class="sxs-lookup"><span data-stu-id="80446-291">When your PR is created, it is classified by a CLA bot.</span></span> <span data-ttu-id="80446-292">如果更改较小（例如，修复拼写错误），则 PR 将标记为 `cla-not-required`。</span><span class="sxs-lookup"><span data-stu-id="80446-292">If the change is small (for example, you fixed a typo), then the PR is labeled with `cla-not-required`.</span></span> <span data-ttu-id="80446-293">否则，它将被分类为 `cla-required`。</span><span class="sxs-lookup"><span data-stu-id="80446-293">Otherwise, it's classified as `cla-required`.</span></span> <span data-ttu-id="80446-294">签署 CLA 后，当前和将来的所有拉取请求都将被标记为 `cla-signed`。</span><span class="sxs-lookup"><span data-stu-id="80446-294">Once you signed the CLA, the current and all future pull requests are labeled as `cla-signed`.</span></span>
