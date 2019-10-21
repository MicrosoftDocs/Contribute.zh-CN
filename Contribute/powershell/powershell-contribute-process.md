---
title: 参与 PowerShell 文档存储库撰写的过程
description: 本文简要介绍如何参与 PowerShell 文档存储库撰写。 本文将介绍所用的存储库，整理内容的流程和用于管理代码示例和其他资产的策略。
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
author: sdwheeler
ms.author: sewhee
ms.date: 10/07/2019
ms.openlocfilehash: 9802942dccbfad2cb860739ffba4b30d2b0af0c9
ms.sourcegitcommit: ca84e542b081e145052f38967e826f6ef25da1b2
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/12/2019
ms.locfileid: "72290187"
---
# <a name="process-for-contributing-to-powershell-docs"></a><span data-ttu-id="89f65-104">参与 PowerShell 文档撰写的过程</span><span class="sxs-lookup"><span data-stu-id="89f65-104">Process for contributing to PowerShell docs</span></span>

<span data-ttu-id="89f65-105">感谢社区参与文档撰写。以下列表显示参与 PowerShell 文档撰写时应记住的指导规则：</span><span class="sxs-lookup"><span data-stu-id="89f65-105">We appreciate community contributions to docs. The following list shows some guiding rules that you should keep in mind when you're contributing to the PowerShell documentation:</span></span>

- <span data-ttu-id="89f65-106">请**勿**向我们提出大量拉取请求。</span><span class="sxs-lookup"><span data-stu-id="89f65-106">**DON'T** surprise us with large pull requests.</span></span> <span data-ttu-id="89f65-107">相反，提出问题并发起讨论，在我们认同这一方向后你再投入大量的时间。</span><span class="sxs-lookup"><span data-stu-id="89f65-107">Instead, file an issue and start a discussion so we can agree on a direction before you invest a large amount of time.</span></span>
- <span data-ttu-id="89f65-108">请务必按以下说明及[代码](powershell-style-code.md)与[引用](powershell-style-reference.md)风格指南操作  。</span><span class="sxs-lookup"><span data-stu-id="89f65-108">**DO** follow these instructions and the [code](powershell-style-code.md) and [reference](powershell-style-reference.md) style guides..</span></span>
- <span data-ttu-id="89f65-109">请**务必**使用[模板](powershell-style-basic-markdown.md)文件，作为工作的出发点。</span><span class="sxs-lookup"><span data-stu-id="89f65-109">**DO** use the [template](powershell-style-basic-markdown.md) file as the starting point of your work.</span></span>
- <span data-ttu-id="89f65-110">处理文章前，请**务必**在分支上创建单独的分支。</span><span class="sxs-lookup"><span data-stu-id="89f65-110">**DO** create a separate branch on your fork before working on the articles.</span></span>
- <span data-ttu-id="89f65-111">请**务必**遵循 [GitHub 流工作流](../how-to-write-workflows-major.md)。</span><span class="sxs-lookup"><span data-stu-id="89f65-111">**DO** follow the [GitHub Flow workflow](../how-to-write-workflows-major.md).</span></span>
- <span data-ttu-id="89f65-112">请**务必**频繁发布有关参与的博客和推文（或者诸如此类）！</span><span class="sxs-lookup"><span data-stu-id="89f65-112">**DO** blog and tweet (or whatever) about your contributions, frequently!</span></span>

<span data-ttu-id="89f65-113">遵循这些指南可确保你和我们都能获得更好的体验。</span><span class="sxs-lookup"><span data-stu-id="89f65-113">Following these guidelines ensures a better experience for you and for us.</span></span>

## <a name="make-a-contribution-to-powershell-docs"></a><span data-ttu-id="89f65-114">参与 PowerShell 文档撰写</span><span class="sxs-lookup"><span data-stu-id="89f65-114">Make a contribution to PowerShell docs</span></span>

<span data-ttu-id="89f65-115">可从现有[问题](https://github.com/MicrosoftDocs/PowerShell-Docs/issues/new/choose)中进行选择。</span><span class="sxs-lookup"><span data-stu-id="89f65-115">You can choose from existing [issues](https://github.com/MicrosoftDocs/PowerShell-Docs/issues/new/choose).</span></span>
<span data-ttu-id="89f65-116">根据你的兴趣和承诺级别，工作量分为以下类别：</span><span class="sxs-lookup"><span data-stu-id="89f65-116">Depending on your interests and level of commitment, the efforts fall into the following categories:</span></span>

- <span data-ttu-id="89f65-117">**小更改**。</span><span class="sxs-lookup"><span data-stu-id="89f65-117">**Small changes**.</span></span> <span data-ttu-id="89f65-118">对于小更改，请在参与者指南的[主页](../index.md#quick-edits-to-existing-documents)中查看在 GitHub 中编辑的说明。</span><span class="sxs-lookup"><span data-stu-id="89f65-118">For small changes, see the instructions on editing in GitHub on the [home page](../index.md#quick-edits-to-existing-documents) of the contributor guide.</span></span> <span data-ttu-id="89f65-119">小更改包括：</span><span class="sxs-lookup"><span data-stu-id="89f65-119">Small changes include:</span></span>

  - <span data-ttu-id="89f65-120">修复各种拼写错误</span><span class="sxs-lookup"><span data-stu-id="89f65-120">Fixing typos and spelling errors</span></span>
  - <span data-ttu-id="89f65-121">改进语法或格式</span><span class="sxs-lookup"><span data-stu-id="89f65-121">Improving grammar or formatting</span></span>
  - <span data-ttu-id="89f65-122">次要技术或事实编辑</span><span class="sxs-lookup"><span data-stu-id="89f65-122">Minor technical or factual edits</span></span>

- <span data-ttu-id="89f65-123">**维护**。</span><span class="sxs-lookup"><span data-stu-id="89f65-123">**Maintenance**.</span></span> <span data-ttu-id="89f65-124">此类别包括相当简单的参与，例如，修复断裂或错误的链接，添加缺少的代码示例或解决受限内容问题。</span><span class="sxs-lookup"><span data-stu-id="89f65-124">This category includes fairly simple contributions, such as fixing broken or incorrect links, adding missing code examples, or addressing limited content issues.</span></span> <span data-ttu-id="89f65-125">在某些情况下，这些问题可能涉及大量文件。</span><span class="sxs-lookup"><span data-stu-id="89f65-125">In some cases, these issues may concern large numbers of files.</span></span> <span data-ttu-id="89f65-126">届时，你应在开始前告知我们想要处理的内容。</span><span class="sxs-lookup"><span data-stu-id="89f65-126">In that case, you should let us know what you'd like to work on before you begin.</span></span> <span data-ttu-id="89f65-127">在问题上添加注释，以告知我们你正在处理。</span><span class="sxs-lookup"><span data-stu-id="89f65-127">Add a comment on the issue to tell us that you are working on it.</span></span>

- <span data-ttu-id="89f65-128">**内容更新**。</span><span class="sxs-lookup"><span data-stu-id="89f65-128">**Content updates**.</span></span> <span data-ttu-id="89f65-129">鉴于文档集的巨大性，内容很容易过时，需要修订。</span><span class="sxs-lookup"><span data-stu-id="89f65-129">Given the enormity of the doc set, content easily becomes outdated and requires revision.</span></span> <span data-ttu-id="89f65-130">此外，出于各种原因，部分内容发生重复，甚至出现一式三份现象。</span><span class="sxs-lookup"><span data-stu-id="89f65-130">In addition, for a variety of reason, some content has been duplicated or even triplicated.</span></span> <span data-ttu-id="89f65-131">更新内容涉及确保各个主题为最新，或修订特色区域中的内容以消除重复，以及确保所有独特的内容均保存在较小文档集中。</span><span class="sxs-lookup"><span data-stu-id="89f65-131">Updating content involves making sure that individual topics are current or revising content in a feature area to eliminate duplication and ensure that all unique content is preserved in the smaller documentation set.</span></span>

- <span data-ttu-id="89f65-132">**新内容创作**。</span><span class="sxs-lookup"><span data-stu-id="89f65-132">**New content authoring**.</span></span> <span data-ttu-id="89f65-133">如果有兴趣创作自己的主题，这些问题列出了我们要向文档集添加的主题。</span><span class="sxs-lookup"><span data-stu-id="89f65-133">If you're interested in authoring your own topic, these issues list topics that we know we'd like to add to our doc set.</span></span> <span data-ttu-id="89f65-134">不过，请在处理某主题前，告知我们。</span><span class="sxs-lookup"><span data-stu-id="89f65-134">Let us know before you begin working on a topic, though.</span></span> <span data-ttu-id="89f65-135">如果有兴趣编写此处未列出的主题，请创建一个问题。</span><span class="sxs-lookup"><span data-stu-id="89f65-135">If you're interested in writing a topic that isn't listed here, open an issue.</span></span>

<span data-ttu-id="89f65-136">选择要处理的任务后，请按照[入门](../get-started-setup-github.md)指南操作，创建 GitHub 帐户并设置环境。</span><span class="sxs-lookup"><span data-stu-id="89f65-136">Once you've picked a task to work on, follow the [get started](../get-started-setup-github.md) guide to create a GitHub account and setup your environment.</span></span>

### <a name="making-large-changes"></a><span data-ttu-id="89f65-137">进行大更改</span><span class="sxs-lookup"><span data-stu-id="89f65-137">Making large changes</span></span>

<span data-ttu-id="89f65-138">**步骤 1：** 如果想要编写新内容或彻底修订现有内容，请创建描述你想做的事情的问题。</span><span class="sxs-lookup"><span data-stu-id="89f65-138">**Step 1:** If you're interested in writing new content or in thoroughly revising existing content, open an issue describing what you want to do.</span></span>

<span data-ttu-id="89f65-139">**步骤 2：** 对 `MicrosoftDocs/PowerShell-Docs` 存储库创建分支，并为所做的更改创建工作分支。</span><span class="sxs-lookup"><span data-stu-id="89f65-139">**Step 2:** Fork the `MicrosoftDocs/PowerShell-Docs` repository and create a working branch for your changes.</span></span>

<span data-ttu-id="89f65-140">**步骤 3：** 在此新分支上进行更改。</span><span class="sxs-lookup"><span data-stu-id="89f65-140">**Step 3:** Make the changes in this new branch.</span></span>

<span data-ttu-id="89f65-141">如果是一个新的主题，请使用[风格指南](powershell-style-basic-markdown.md)中的模板作为起点。</span><span class="sxs-lookup"><span data-stu-id="89f65-141">If it's a new topic, use the template in the [style guide](powershell-style-basic-markdown.md) as your starting point.</span></span> <span data-ttu-id="89f65-142">风格指南包含编写准则，并且解释了每篇文章需要的元数据。</span><span class="sxs-lookup"><span data-stu-id="89f65-142">The style guide contains the writing guidelines and explains the metadata required for each article.</span></span>

<span data-ttu-id="89f65-143">导航到对应针对步骤 1 中的文章确定的目录位置的文件夹。</span><span class="sxs-lookup"><span data-stu-id="89f65-143">Navigate to the folder that corresponds to the TOC location determined for your article in step 1.</span></span>
<span data-ttu-id="89f65-144">该文件夹包含针对该部分中所有文章的 Markdown 文件。</span><span class="sxs-lookup"><span data-stu-id="89f65-144">That folder contains the Markdown files for all articles in that section.</span></span> <span data-ttu-id="89f65-145">如有必要，新建一个文件夹，放置存储内容的文件。</span><span class="sxs-lookup"><span data-stu-id="89f65-145">If necessary, create a new folder to place the files for your content.</span></span> <span data-ttu-id="89f65-146">该部分的主要文章称为 index.md  。</span><span class="sxs-lookup"><span data-stu-id="89f65-146">The main article for that section is called *index.md*.</span></span>
<span data-ttu-id="89f65-147">对于映像和其他静态资源，请在包含文章的文件夹中创建称为“media”的子文件夹（如果尚不存在）  。</span><span class="sxs-lookup"><span data-stu-id="89f65-147">For images and other static resources, create a subfolder called **media** inside the folder that contains your article, if it doesn't already exist.</span></span> <span data-ttu-id="89f65-148">在“media”文件夹内，创建具有文章名称的子文件夹（索引文件除外）  。</span><span class="sxs-lookup"><span data-stu-id="89f65-148">Inside the **media** folder, create a subfolder with the article name (except for the index file).</span></span>

<span data-ttu-id="89f65-149">请务必遵循适当的 Markdown 语法。</span><span class="sxs-lookup"><span data-stu-id="89f65-149">Be sure to follow the proper Markdown syntax.</span></span> <span data-ttu-id="89f65-150">有关详细说明和示例，请参阅[风格指南](powershell-style-basic-markdown.md)。</span><span class="sxs-lookup"><span data-stu-id="89f65-150">Please read the [style guide](powershell-style-basic-markdown.md) for detailed instructions and examples.</span></span>

<span data-ttu-id="89f65-151">**示例结构**</span><span class="sxs-lookup"><span data-stu-id="89f65-151">**Example structure**</span></span>

```
reference
  /docs-conceptual
    /learn
      /remoting
        managing-remote-sessions.md
        /images
          /managing-remote-sessions
            sesssion-list.png
```

<span data-ttu-id="89f65-152">**步骤 4：** 从工作分支向暂存分支提交拉取请求 (PR)  。</span><span class="sxs-lookup"><span data-stu-id="89f65-152">**Step 4:** Submit a Pull Request (PR) from your working branch to the *staging* branch.</span></span>

<span data-ttu-id="89f65-153">通常，PR 一次只处理一个问题。</span><span class="sxs-lookup"><span data-stu-id="89f65-153">Normally, a PR should address one issue at a time.</span></span> <span data-ttu-id="89f65-154">PR 可修改一个或多个文件。</span><span class="sxs-lookup"><span data-stu-id="89f65-154">The PR can modify one or multiple files.</span></span> <span data-ttu-id="89f65-155">如果要处理不同文件上的多个修复，首选单独的 PR。</span><span class="sxs-lookup"><span data-stu-id="89f65-155">If you're addressing multiple fixes on different files, separate PRs are preferred.</span></span>

<span data-ttu-id="89f65-156">如果 PR 可修复现有问题，请在提交消息或 PR 说明中添加 `Fixes #Issue_Number` 关键字。</span><span class="sxs-lookup"><span data-stu-id="89f65-156">If your PR fixes an existing issue, add the `Fixes #Issue_Number` keyword to the commit message or PR description.</span></span> <span data-ttu-id="89f65-157">如此，PR 合并时，问题将自动关闭。</span><span class="sxs-lookup"><span data-stu-id="89f65-157">That way, the issue is automatically closed when the PR is merged.</span></span> <span data-ttu-id="89f65-158">有关详细信息，请参阅[通过提交消息关闭问题](https://help.github.com/articles/closing-issues-via-commit-messages/)。</span><span class="sxs-lookup"><span data-stu-id="89f65-158">For more information, see [Closing issues via commit messages](https://help.github.com/articles/closing-issues-via-commit-messages/).</span></span>

<span data-ttu-id="89f65-159">PowerShell 团队会评审 PR，并告知你是否需要进行其他任何更改以获得批准。</span><span class="sxs-lookup"><span data-stu-id="89f65-159">The PowerShell team reviews your PR and lets you know if there are any other changes necessary in order to approve it.</span></span>

<span data-ttu-id="89f65-160">**步骤 5：** 与团队讨论时，对分支进行任何必需的更新。</span><span class="sxs-lookup"><span data-stu-id="89f65-160">**Step 5:** Make any necessary updates to your branch as discussed with the team.</span></span>

<span data-ttu-id="89f65-161">PR 获得批准后，维护人员会将 PR 合并到暂存分支中  。</span><span class="sxs-lookup"><span data-stu-id="89f65-161">Once the PR is approved, the maintainers merge your PR into the *staging* branch.</span></span> <span data-ttu-id="89f65-162">我们会定期将所有提交从暂存分支推送到生效分支   。</span><span class="sxs-lookup"><span data-stu-id="89f65-162">We periodically push all commits from *staging* branch into the *live* branch.</span></span> <span data-ttu-id="89f65-163">撰写内容生效后，可在 [PowerShell 文档网站](https://docs.microsoft.com/PowerShell/)中查看。</span><span class="sxs-lookup"><span data-stu-id="89f65-163">Once your contribution is live, you can see it in the [PowerShell docs site](https://docs.microsoft.com/PowerShell/).</span></span> <span data-ttu-id="89f65-164">通常，我们会在一个工作周内发布两到三次。</span><span class="sxs-lookup"><span data-stu-id="89f65-164">Typically, we publish a two to three times during the work week.</span></span>

## <a name="contributor-license-agreement"></a><span data-ttu-id="89f65-165">参与者许可协议</span><span class="sxs-lookup"><span data-stu-id="89f65-165">Contributor license agreement</span></span>

<span data-ttu-id="89f65-166">在合并 PR 前，必须先签署[参与撰写许可协议 (CLA)](https://cla.opensource.microsoft.com/MicrosoftDocs/PowerShell-Docs)。</span><span class="sxs-lookup"><span data-stu-id="89f65-166">You must sign the [Contribution License Agreement (CLA)](https://cla.opensource.microsoft.com/MicrosoftDocs/PowerShell-Docs) before your PR is merged.</span></span> <span data-ttu-id="89f65-167">每次参与撰写我们的文档时，都需要签署。</span><span class="sxs-lookup"><span data-stu-id="89f65-167">This is a one-time requirement when contributing to our documentation.</span></span>

<span data-ttu-id="89f65-168">无需提前签署协议。</span><span class="sxs-lookup"><span data-stu-id="89f65-168">You don't have to sign the agreement up-front.</span></span> <span data-ttu-id="89f65-169">可以照常克隆 PR、创建 PR 分支或提交 PR。</span><span class="sxs-lookup"><span data-stu-id="89f65-169">You can clone, fork, and submit your PR as usual.</span></span>
<span data-ttu-id="89f65-170">创建 PR 时，由 CLA 机器人进行分类。</span><span class="sxs-lookup"><span data-stu-id="89f65-170">When your PR is created, it is classified by a CLA bot.</span></span> <span data-ttu-id="89f65-171">如果更改较小（例如，修复拼写错误），则 PR 将标记为 `cla-not-required`。</span><span class="sxs-lookup"><span data-stu-id="89f65-171">If the change is small (for example, you fixed a typo), then the PR is labeled with `cla-not-required`.</span></span> <span data-ttu-id="89f65-172">否则，它将被分类为 `cla-required`。</span><span class="sxs-lookup"><span data-stu-id="89f65-172">Otherwise, it's classified as `cla-required`.</span></span> <span data-ttu-id="89f65-173">签署 CLA 后，当前和将来的所有拉取请求都将被标记为 `cla-signed`。</span><span class="sxs-lookup"><span data-stu-id="89f65-173">Once you signed the CLA, the current and all future pull requests are labeled as `cla-signed`.</span></span>
