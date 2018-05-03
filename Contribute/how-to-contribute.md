---
title: 参与 docs.microsoft.com 内容撰写的方式
description: 本文介绍参与 docs.microsoft.com 内容撰写的不同方式。
author: billwagner
ms.author: wiwagn
manager: wpickett
ms.date: 01/17/2018
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.custom: external-contributor-guide
ms.openlocfilehash: bc6f9c314eda5f0d950da049374a7a157f16782a
ms.sourcegitcommit: de6e6b6ca641fdd5b30eb46deee9ac3a500089ef
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/28/2018
---
# <a name="how-to-contribute-to-docsmicrosoftcom"></a><span data-ttu-id="901b9-103">参与 docs.microsoft.com 内容撰写的方式</span><span class="sxs-lookup"><span data-stu-id="901b9-103">How to contribute to docs.microsoft.com</span></span>

<span data-ttu-id="901b9-104">参与改进 [docs.microsoft.com](https://docs.microsoft.com) 内容的方式有数种：</span><span class="sxs-lookup"><span data-stu-id="901b9-104">There are several ways to participate in improving the content that makes up [docs.microsoft.com](https://docs.microsoft.com):</span></span>

- <span data-ttu-id="901b9-105">你可以[创建问题](#create-issues)以推荐新文章，或改进现有文章。</span><span class="sxs-lookup"><span data-stu-id="901b9-105">You can [create issues](#create-issues) to recommend new articles, or improve existing articles.</span></span>
- <span data-ttu-id="901b9-106">你可以[快速编辑](#quick-edits)文章，在 GitHub 在线编辑器中进行较小的更改。</span><span class="sxs-lookup"><span data-stu-id="901b9-106">You can [quickly edit](#quick-edits) articles to make small changes in the GitHub online editor.</span></span>
- <span data-ttu-id="901b9-107">你可以[审查新文章的草稿](#review-new-articles)以确保质量和技术准确性。</span><span class="sxs-lookup"><span data-stu-id="901b9-107">You can [review drafts of new articles](#review-new-articles) to ensure quality and technical accuracy.</span></span>
- <span data-ttu-id="901b9-108">如果你想要帮助推动内容故事时，你可以为主题[创建新文章](#create-new-articles)。</span><span class="sxs-lookup"><span data-stu-id="901b9-108">You can [create new articles](#create-new-articles) for topics when you want to help drive the content story.</span></span>
- <span data-ttu-id="901b9-109">你可以[更新](#update-samples)或[创建](#create-samples)示例，以改进可增强重要概念的代码示例。</span><span class="sxs-lookup"><span data-stu-id="901b9-109">You can [update](#update-samples) or [create](#create-samples) samples to improve the code samples that reinforce important concepts.</span></span>

<span data-ttu-id="901b9-110">在本文中，你将学习不同的参与方式，了解如何完成这些任务，并找到有关每个任务的更多信息的指针。</span><span class="sxs-lookup"><span data-stu-id="901b9-110">In this article, you'll learn the different ways to contribute, see how to accomplish each of those tasks, and find pointers to more information about each of those tasks.</span></span>

<span data-ttu-id="901b9-111">我们的公共存储库托管在 [GitHub](https://wwww.GitHub.com) 上。</span><span class="sxs-lookup"><span data-stu-id="901b9-111">Our public repositories are hosted on [GitHub](https://wwww.GitHub.com).</span></span>  <span data-ttu-id="901b9-112">你需要在 GitHub 上创建一个帐户才能参与我们的文档存储库。</span><span class="sxs-lookup"><span data-stu-id="901b9-112">You will need to create an account on GitHub to participate in our documentation repositories.</span></span>

<span data-ttu-id="901b9-113">你还需要文本编辑器来更新文档。</span><span class="sxs-lookup"><span data-stu-id="901b9-113">You'll also need a text editor to update the documents.</span></span> <span data-ttu-id="901b9-114">建议使用 [Visual Studio Code](https://www.visualstudio.com/code)。</span><span class="sxs-lookup"><span data-stu-id="901b9-114">We recommend [Visual Studio Code](https://www.visualstudio.com/code).</span></span> <span data-ttu-id="901b9-115">你应该对 [Markdown](https://daringfireball.net/projects/markdown/syntax) 语法有基本的了解。</span><span class="sxs-lookup"><span data-stu-id="901b9-115">You should have a basic understanding of [Markdown](https://daringfireball.net/projects/markdown/syntax) syntax.</span></span>

<span data-ttu-id="901b9-116">如果要添加或修改示例，则需要开发环境。</span><span class="sxs-lookup"><span data-stu-id="901b9-116">If you are adding or modifying samples, you'll need a development environment.</span></span> <span data-ttu-id="901b9-117">建议在 PC 和 Mac 上使用 [Visual Studio](https://www.visualstudio.com)，或在所有平台上使用 [Visual Studio Code](https://www.visualstudio.com/code)。</span><span class="sxs-lookup"><span data-stu-id="901b9-117">We recommend [Visual Studio](https://www.visualstudio.com) on PC and Mac, or [Visual Studio Code](https://www.visualstudio.com/code) on all platforms.</span></span>

## <a name="create-issues"></a><span data-ttu-id="901b9-118">创建问题</span><span class="sxs-lookup"><span data-stu-id="901b9-118">Create issues</span></span>

<span data-ttu-id="901b9-119">如果你在文章中发现遗漏或不准确的地方，请针对该文章创建一个问题。</span><span class="sxs-lookup"><span data-stu-id="901b9-119">If you find omissions or inaccuracies in a article, create an issue against that article.</span></span> <span data-ttu-id="901b9-120">找到正确位置最简单的方法是单击浏览器中的“编辑”按钮，该操作将转到正确公共 GitHub 存储库中的文章来源。</span><span class="sxs-lookup"><span data-stu-id="901b9-120">The easiest way to find the right location is to click the "Edit" button in your browser, which will take you to the article source in the correct public GitHub repository.</span></span> <span data-ttu-id="901b9-121">在此处，你可以从地址栏中检索文章来源的 URL。</span><span class="sxs-lookup"><span data-stu-id="901b9-121">From there, you can retrieve the URL for the source of the article from your address bar.</span></span> <span data-ttu-id="901b9-122">单击“创建问题”以针对该文章创建新问题。</span><span class="sxs-lookup"><span data-stu-id="901b9-122">Click "Create Issue" to make a new issue on the article.</span></span>

> [!NOTE]
> <span data-ttu-id="901b9-123">如果发现的问题可以通过小的修改来修复（如输入错误或语法问题），则可以通过使用浏览器[提交修补程序](#quick-edits)来编辑源代码，从而节省你自己和我们的时间。</span><span class="sxs-lookup"><span data-stu-id="901b9-123">If you find issues you can fix with small edits, such as typing mistakes or grammar issues, you can save yourself and us time by [submitting the fix](#quick-edits) using the browser to edit the source.</span></span>

<span data-ttu-id="901b9-124">我们的大部分公共存储库都包含新问题模板，可指导你提供修复问题所需的信息。</span><span class="sxs-lookup"><span data-stu-id="901b9-124">Most of our public repos contain templates for new issues that will guide you to provide the information needed to fix the issue.</span></span>

<span data-ttu-id="901b9-125">如果你找不到所需信息，也可以提出新问题。</span><span class="sxs-lookup"><span data-stu-id="901b9-125">You can also contribute new issues where you can't find the information you need.</span></span> <span data-ttu-id="901b9-126">过程是相同的：针对其中一个公共文档存储库创建新问题。</span><span class="sxs-lookup"><span data-stu-id="901b9-126">The process is the same: create a new issue on one of the public docs repositories.</span></span> <span data-ttu-id="901b9-127">告诉我们你在寻找什么，你想要做什么，以及为什么你找到的文章没有提供你所期望的帮助。</span><span class="sxs-lookup"><span data-stu-id="901b9-127">Tell us what you were searching for, what you wanted to do, and why the articles you found did not help the way you expected.</span></span>

## <a name="review-new-articles"></a><span data-ttu-id="901b9-128">审查新文章</span><span class="sxs-lookup"><span data-stu-id="901b9-128">Review new articles</span></span>

<span data-ttu-id="901b9-129">如果您正在开发新的软件（可能是 CTP 或 beta 版），那么我们可能会在你研发该技术的同时也在编写文档。</span><span class="sxs-lookup"><span data-stu-id="901b9-129">If you are working on new, possibly CTP or beta, software, we are likely building the docs as you are exploring the technology.</span></span> <span data-ttu-id="901b9-130">你可以在公共存储库中查找正在编写的文档。</span><span class="sxs-lookup"><span data-stu-id="901b9-130">You can find the in-process docs in our public repositories.</span></span> <span data-ttu-id="901b9-131">如果你有意见，可以在文档发布之前帮助我们对其进行改进。</span><span class="sxs-lookup"><span data-stu-id="901b9-131">If you have comments, you can help us make them better before they are released.</span></span>

<span data-ttu-id="901b9-132">使用 [GitHub 流](https://guides.github.com/introduction/flow/)流程公开审查新文章。</span><span class="sxs-lookup"><span data-stu-id="901b9-132">New articles are reviewed in public, using the [GitHub flow](https://guides.github.com/introduction/flow/) process.</span></span> <span data-ttu-id="901b9-133">查看任意文档存储库，并检查开放的拉取请求 (PR)。</span><span class="sxs-lookup"><span data-stu-id="901b9-133">Look at any of our docs repositories, and check the open pull requests (PRs).</span></span> <span data-ttu-id="901b9-134">我们欢迎针对开放的拉取请求发表意见和评论。</span><span class="sxs-lookup"><span data-stu-id="901b9-134">We welcome comments and reviews on any open pull requests.</span></span> <span data-ttu-id="901b9-135">这有助于我们在首次发布时就能发布更好的内容，而不是在上线后等待反馈。</span><span class="sxs-lookup"><span data-stu-id="901b9-135">That helps us publish better content on our first release, rather than waiting for feedback after going live.</span></span>

<span data-ttu-id="901b9-136">我们正在寻找提高技术准确性、描述清晰度以及语法准确性的方法。</span><span class="sxs-lookup"><span data-stu-id="901b9-136">We are looking for ways to improve technical accuracy, clarity of the descriptions, and grammatical accuracy.</span></span>

## <a name="quick-edits"></a><span data-ttu-id="901b9-137">快速编辑</span><span class="sxs-lookup"><span data-stu-id="901b9-137">Quick edits</span></span>

<span data-ttu-id="901b9-138">快速编辑是一种使用基于浏览器的编辑器进行细微修复的方法。</span><span class="sxs-lookup"><span data-stu-id="901b9-138">Quick edits are a way to make small fixes using the browser based editor.</span></span> <span data-ttu-id="901b9-139">如果你发现小的拼写或语法错误，或者 API 命名错误，可以通过编辑和提交 PR 来跳过创建问题。</span><span class="sxs-lookup"><span data-stu-id="901b9-139">If you find small spelling or grammar errors, or mis-named APIs, you can skip creating an issue by making the edit and submitting a PR.</span></span>

<span data-ttu-id="901b9-140">对于任何文章，单击“编辑”按钮（通常在页面的右上角），进行编辑，然后单击页面底部的“提交 PR”。</span><span class="sxs-lookup"><span data-stu-id="901b9-140">On any article, click the "Edit" button (usually toward the top right-hand side of the page), make your edits, and click "Submit PR" at the bottom of the page.</span></span> <span data-ttu-id="901b9-141">我们将审查该 PR，并在日常 PR 审查时将其合并。</span><span class="sxs-lookup"><span data-stu-id="901b9-141">We'll review the PR, and merge it as we do our daily PR review.</span></span>

## <a name="create-new-articles"></a><span data-ttu-id="901b9-142">创建新文章</span><span class="sxs-lookup"><span data-stu-id="901b9-142">Create new articles</span></span>

<span data-ttu-id="901b9-143">如果你对某些概念有浓厚的兴趣，并希望向其他人进行解释说明，则可以创建文章并提交 PR。</span><span class="sxs-lookup"><span data-stu-id="901b9-143">If there are concepts you are passionate about, and want to explain to others, you can create the articles and submit a PR.</span></span>

<span data-ttu-id="901b9-144">创建新文章非常耗时，我们珍视你付出的时间和贡献。</span><span class="sxs-lookup"><span data-stu-id="901b9-144">Creating new articles is time-consuming, and we value your time and contributions.</span></span> <span data-ttu-id="901b9-145">我们希望尽早参与该过程，以确保你从一开始就遵循我们的指导准则和风格。</span><span class="sxs-lookup"><span data-stu-id="901b9-145">We want to be involved early in the process to ensure you're following our guidelines and style from the beginning.</span></span> <span data-ttu-id="901b9-146">以下为建议步骤：</span><span class="sxs-lookup"><span data-stu-id="901b9-146">We recommend the following steps:</span></span>

1. <span data-ttu-id="901b9-147">[创建问题](#create-issues)，说明缺少的内容以及你的解决方法。</span><span class="sxs-lookup"><span data-stu-id="901b9-147">[Create an issue](#create-issues) describing what's missing and how you'd address it.</span></span>
1. <span data-ttu-id="901b9-148">对该问题进行评论，告诉我们你希望处理此问题，并给出文章大纲和摘要。</span><span class="sxs-lookup"><span data-stu-id="901b9-148">Comment on the issue, telling us you'd like to work on it, and suggesting an outline and abstract for the article.</span></span>
1. <span data-ttu-id="901b9-149">我们将在回复中提出建议。</span><span class="sxs-lookup"><span data-stu-id="901b9-149">We'll respond with suggestions.</span></span> <span data-ttu-id="901b9-150">这些建议可能包括相关文章的链接、针对示例的建议或文章的组织方式。</span><span class="sxs-lookup"><span data-stu-id="901b9-150">These may include links to related articles, suggestions for samples, or how the article will be organized.</span></span>
1. <span data-ttu-id="901b9-151">一旦我们就大纲达成一致，为存储库创建分支，然后开始工作。</span><span class="sxs-lookup"><span data-stu-id="901b9-151">Once we agree on the outline, fork the repository, and start working.</span></span>
1. <span data-ttu-id="901b9-152">在此过程的早期，打开标题以“[WIP]”开头的 PR。</span><span class="sxs-lookup"><span data-stu-id="901b9-152">Early in the process, open a PR, with "[WIP]" at the beginning of the title.</span></span>
1. <span data-ttu-id="901b9-153">其中一个核心参与者会给你提供初始反馈。</span><span class="sxs-lookup"><span data-stu-id="901b9-153">One of the core contributors will give you initial feedback.</span></span>
1. <span data-ttu-id="901b9-154">继续编写，当你准备好接受更多反馈时，@-mention审核初稿的人。</span><span class="sxs-lookup"><span data-stu-id="901b9-154">Keep writing, @-mention the person who reviewed the first draft when you're ready for more feedback.</span></span>
1. <span data-ttu-id="901b9-155">准备好进行最终审核时，移除“[WIP]”。</span><span class="sxs-lookup"><span data-stu-id="901b9-155">Remove the "[WIP]" when you're ready for final review.</span></span>
1. <span data-ttu-id="901b9-156">回复反馈</span><span class="sxs-lookup"><span data-stu-id="901b9-156">Respond to the feedback</span></span>
1. <span data-ttu-id="901b9-157">核心参与者将合并你的 PR。</span><span class="sxs-lookup"><span data-stu-id="901b9-157">The core contributors will merge your PR.</span></span>

<span data-ttu-id="901b9-158">该列表中有一些点需要进行扩展。</span><span class="sxs-lookup"><span data-stu-id="901b9-158">There are a couple points worth expanding on from that list.</span></span> <span data-ttu-id="901b9-159">一般而言，我们遵循 [GitHub 流](https://guides.github.com/introduction/flow/)流程尽早审核内容。</span><span class="sxs-lookup"><span data-stu-id="901b9-159">In general, we're following the [GitHub flow](https://guides.github.com/introduction/flow/) process to review content as early as possible.</span></span> <span data-ttu-id="901b9-160">这样，我们就可以确定文章应该放在目录的哪个位置，读者将从新文章中收获哪些知识，以及你要创建的示例的范围。</span><span class="sxs-lookup"><span data-stu-id="901b9-160">That way, we agree on where an article should go in the table of contents, what benefit the reader will get from the new article, and the scope of any samples you'll create.</span></span> <span data-ttu-id="901b9-161">在投入大量时间写作之前，我们可以在早期做出任何必要的修正。</span><span class="sxs-lookup"><span data-stu-id="901b9-161">We can make any necessary course corrections early, before you've invested significant time writing.</span></span>

## <a name="update-samples"></a><span data-ttu-id="901b9-162">更新示例</span><span class="sxs-lookup"><span data-stu-id="901b9-162">Update samples</span></span>

<span data-ttu-id="901b9-163">某些示例最初可能是使用不再建议采用的做法在数个版本之前编写的。</span><span class="sxs-lookup"><span data-stu-id="901b9-163">Some samples may have originally been written several releases ago, using practices no long recommended.</span></span> <span data-ttu-id="901b9-164">你希望帮助我们更新这些示例。</span><span class="sxs-lookup"><span data-stu-id="901b9-164">You may want to help us update those samples.</span></span> <span data-ttu-id="901b9-165">或者，你或许发现一个简单的变量名称更改可能会增加解释的清晰度。</span><span class="sxs-lookup"><span data-stu-id="901b9-165">Or, you may find that a simple variable name change could increase the clarity of an explanation.</span></span>

<span data-ttu-id="901b9-166">每篇文章中显示的示例代码都是我们在 CI 系统中构建并经常进行测试的程序的一部分。</span><span class="sxs-lookup"><span data-stu-id="901b9-166">The sample code displayed with each article are part of programs that are built and often tested under our CI system.</span></span>

<span data-ttu-id="901b9-167">要进行细微的更新，你可以在适当的存储库中找到源代码，在浏览器中更改代码并提交 PR。</span><span class="sxs-lookup"><span data-stu-id="901b9-167">To make small updates, you find the source in the appropriate repository, make the code change in the browser and submit a PR.</span></span> <span data-ttu-id="901b9-168">CI 系统将生成这些更改，我们会在 PR 完成时将其合并。</span><span class="sxs-lookup"><span data-stu-id="901b9-168">Our CI system will build the changes, and we'll merge the PR when it finishes.</span></span>

<span data-ttu-id="901b9-169">对于较大规模的更改，请对存储库建立分支，并在喜爱的开发环境中进行更改。</span><span class="sxs-lookup"><span data-stu-id="901b9-169">For larger scale changes fork the repository and make the changes in your favorite development environment.</span></span> <span data-ttu-id="901b9-170">确保添加了一些测试，以保证更改按预期工作。</span><span class="sxs-lookup"><span data-stu-id="901b9-170">Make sure you add some tests to ensure that your changes work as you intended.</span></span> <span data-ttu-id="901b9-171">提交 PR，我们将对其进行审查。</span><span class="sxs-lookup"><span data-stu-id="901b9-171">Submit a PR, and we'll review it.</span></span>

<span data-ttu-id="901b9-172">对于所有代码更改，请遵循你正在修改的示例代码的现有代码约定。</span><span class="sxs-lookup"><span data-stu-id="901b9-172">With all code changes, follow the existing code conventions for the sample code you are modifying.</span></span> <span data-ttu-id="901b9-173">示例存储库编码标准将反映相应产品团队的编码标准。</span><span class="sxs-lookup"><span data-stu-id="901b9-173">Our samples repositories coding standards will mirror those of the corresponding product teams.</span></span> <span data-ttu-id="901b9-174">检查每个存储库以了解具体指导准则。</span><span class="sxs-lookup"><span data-stu-id="901b9-174">Check each repository for specific guidance.</span></span>

> [!NOTE]
> <span data-ttu-id="901b9-175">我们自身正在努力遵循这一指导准则。</span><span class="sxs-lookup"><span data-stu-id="901b9-175">We're working toward following this guidance ourselves.</span></span> <span data-ttu-id="901b9-176">某些示例早于我们的当前标准，因而尚未更新。</span><span class="sxs-lookup"><span data-stu-id="901b9-176">Some of the samples predate our current standards ane have not been updated yet.</span></span> <span data-ttu-id="901b9-177">我们正在努力实现一个目标：所有正在运行的示例代码都通过有效的、测试过的示例显示。</span><span class="sxs-lookup"><span data-stu-id="901b9-177">We are working toward a goal of all running sample code being displayed from working, tested, samples.</span></span>

## <a name="create-samples"></a><span data-ttu-id="901b9-178">创建示例</span><span class="sxs-lookup"><span data-stu-id="901b9-178">Create samples</span></span>

<span data-ttu-id="901b9-179">你还可以创建展示概念或场景的新示例。</span><span class="sxs-lookup"><span data-stu-id="901b9-179">You can also create new samples that demonstrate concepts or scenarios.</span></span> <span data-ttu-id="901b9-180">任何示例必须附上一篇文章，说明示例中的关键信息。</span><span class="sxs-lookup"><span data-stu-id="901b9-180">Any samples must be accompanied by a article that explains the key information from the sample.</span></span>

<span data-ttu-id="901b9-181">如果新示例是对现有文章的补充，请在该文章中添加对该示例的引用。</span><span class="sxs-lookup"><span data-stu-id="901b9-181">If your new sample complements an existing article, add a reference to the sample in that article.</span></span> <span data-ttu-id="901b9-182">如果未添加，请与我们共同编写附带该示例的[文章](#create-new-articles)。</span><span class="sxs-lookup"><span data-stu-id="901b9-182">If not, work with us to [write the article](#create-new-articles) that accompanies the sample.</span></span>

<span data-ttu-id="901b9-183">在所有情况下，示例代码都遵循相关产品团队使用的编码约定。</span><span class="sxs-lookup"><span data-stu-id="901b9-183">In all cases, our sample code follows the coding conventions used by the related product teams.</span></span> <span data-ttu-id="901b9-184">一个例外是，当文章中包含这些声明时，为了清晰起见，我们更倾向于使用显式类型化的变量而不是隐式类型化的变量（通过 `var` 声明）。</span><span class="sxs-lookup"><span data-stu-id="901b9-184">One exception is that we are more likely to use explicitly typed varables over implicitly typed (declared with `var`) for clarity when those declarations are included in the article.</span></span>

<span data-ttu-id="901b9-185">请按照[新文章](#create-new-articles)中前面部分概述的示例流程进行操作，这样我们可以在开发过程的早期审查代码。</span><span class="sxs-lookup"><span data-stu-id="901b9-185">Follow the sample process outlined in the earlier section for [new articles](#create-new-articles) so that we can review the code early in the development process.</span></span>
