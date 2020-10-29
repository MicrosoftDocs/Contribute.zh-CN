---
title: 主要或持续更改的 GitHub 参与工作流
description: 本文介绍如何使用“主要”参与者工作流参与 docs.microsoft.com 文章的供稿。
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
ms.date: 08/30/2017
ms.openlocfilehash: 0661191c64d2f8aa29973e96e98445d070424beb
ms.sourcegitcommit: 344c3c74c317350a00f91e3e7019a545d5c3c5a2
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/27/2020
ms.locfileid: "92689311"
---
# <a name="github-contribution-workflow-for-major-or-long-running-changes"></a><span data-ttu-id="b07de-103">主要或持续更改的 GitHub 参与工作流</span><span class="sxs-lookup"><span data-stu-id="b07de-103">GitHub contribution workflow for major or long-running changes</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b07de-104">发布到 docs.microsoft.com 的所有存储库均遵循 [Microsoft 开放源代码行为准则](https://opensource.microsoft.com/codeofconduct/)或 [.NET 基础行为准则](https://dotnetfoundation.org/code-of-conduct)。</span><span class="sxs-lookup"><span data-stu-id="b07de-104">All repositories that publish to docs.microsoft.com have adopted either the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/) or the [.NET Foundation Code of Conduct](https://dotnetfoundation.org/code-of-conduct).</span></span> <span data-ttu-id="b07de-105">有关详细信息，请参阅[行为准则常见问题解答](https://opensource.microsoft.com/codeofconduct/faq/)。</span><span class="sxs-lookup"><span data-stu-id="b07de-105">For more information, see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/).</span></span> <span data-ttu-id="b07de-106">或如有任何疑问或意见，请联系 [opencode@microsoft.com](mailto:opencode@microsoft.com) 或 [conduct@dotnetfoundation.org](mailto:conduct@dotnetfoundation.org)。</span><span class="sxs-lookup"><span data-stu-id="b07de-106">Or contact [opencode@microsoft.com](mailto:opencode@microsoft.com), or [conduct@dotnetfoundation.org](mailto:conduct@dotnetfoundation.org) with any questions or comments.</span></span><br>
>
> <span data-ttu-id="b07de-107">[docs.microsoft.com 使用条款](https://docs.microsoft.com/legal/termsofuse)适用于对公共存储库中文档和代码示例所做的小修订和澄清。</span><span class="sxs-lookup"><span data-stu-id="b07de-107">Minor corrections or clarifications to documentation and code examples in public repositories are covered by the [docs.microsoft.com Terms of Use](https://docs.microsoft.com/legal/termsofuse).</span></span> <span data-ttu-id="b07de-108">如果你不是 Microsoft 的员工，那么新更改或重大更改会在拉取请求中生成一条注释，要求提交一份在线参与许可协议 (CLA)。</span><span class="sxs-lookup"><span data-stu-id="b07de-108">New or significant changes will generate a comment in the pull request, asking you to submit an online Contribution License Agreement (CLA) if you are not an employee of Microsoft.</span></span> <span data-ttu-id="b07de-109">在合并拉取请求之前，你需要填写这份在线表单。</span><span class="sxs-lookup"><span data-stu-id="b07de-109">You will need to complete the online form before your pull request can be merged.</span></span>

## <a name="overview"></a><span data-ttu-id="b07de-110">概述</span><span class="sxs-lookup"><span data-stu-id="b07de-110">Overview</span></span>

<span data-ttu-id="b07de-111">此工作流适合需要进行主要更改的参与者，或者是向存储库频繁供稿的参与者。</span><span class="sxs-lookup"><span data-stu-id="b07de-111">This workflow is suitable for a contributor who needs to make a major change or will be a frequent contributor to a repository.</span></span> <span data-ttu-id="b07de-112">频繁供稿的参与者通常会执行不断进行的（即持续）更改（这些更改经过多个构建/验证/暂存周期或跨越多天），然后进行拉取请求签核和合并。</span><span class="sxs-lookup"><span data-stu-id="b07de-112">Frequent contributors typically have ongoing (long-running) changes, which go through multiple build/validation/staging cycles or span multiple days before pull request sign-off and merge.</span></span>

<span data-ttu-id="b07de-113">这些类型的参与示例包括：</span><span class="sxs-lookup"><span data-stu-id="b07de-113">Examples of these types of contributions include:</span></span>

[!INCLUDE[contribute-major-changes-change-definition](includes/contribute-how-to-write-workflows-major-change-definition.md)]

### <a name="terminology"></a><span data-ttu-id="b07de-114">术语</span><span class="sxs-lookup"><span data-stu-id="b07de-114">Terminology</span></span>

<span data-ttu-id="b07de-115">在开始之前，让我们回顾一下在此工作流中使用的 Git/GitHub 术语和名字对象。</span><span class="sxs-lookup"><span data-stu-id="b07de-115">Before you start, let's review some of the Git/GitHub terms and monikers used in this workflow.</span></span> <span data-ttu-id="b07de-116">不用着急去熟悉它。</span><span class="sxs-lookup"><span data-stu-id="b07de-116">Don't worry about understanding them now.</span></span> <span data-ttu-id="b07de-117">只要知道你将对此有所了解，并且在需要验证某个定义时，可以回顾参考本节。</span><span class="sxs-lookup"><span data-stu-id="b07de-117">Just know that you will be learning about them, and you can refer back to this section when you need to verify a definition.</span></span>

| <span data-ttu-id="b07de-118">名称</span><span class="sxs-lookup"><span data-stu-id="b07de-118">Name</span></span> | <span data-ttu-id="b07de-119">说明</span><span class="sxs-lookup"><span data-stu-id="b07de-119">Description</span></span> |
|-----------|-------------|
|<span data-ttu-id="b07de-120">分支</span><span class="sxs-lookup"><span data-stu-id="b07de-120">fork</span></span>|<span data-ttu-id="b07de-121">在表示主 GitHub 存储库的副本时，通常用作名词。</span><span class="sxs-lookup"><span data-stu-id="b07de-121">Normally used as a noun, when referring to a copy of a main GitHub repository.</span></span> <span data-ttu-id="b07de-122">实际上，分支只是另一个存储库。</span><span class="sxs-lookup"><span data-stu-id="b07de-122">In practice, a fork is just another repository.</span></span> <span data-ttu-id="b07de-123">但是，从某种意义上来说，GitHub 维护至主/父存储库的连接。</span><span class="sxs-lookup"><span data-stu-id="b07de-123">But it's special in the sense that GitHub maintains a connection back to the main/parent repository.</span></span> <span data-ttu-id="b07de-124">它有时用作动词，如“必须首先为存储库创建分支”。</span><span class="sxs-lookup"><span data-stu-id="b07de-124">It's sometimes used as a verb, as in "You must fork the repository first."</span></span>|
|<span data-ttu-id="b07de-125">远程</span><span class="sxs-lookup"><span data-stu-id="b07de-125">remote</span></span>|<span data-ttu-id="b07de-126">到远程存储库的命名连接，例如“源”或“上游”远程。</span><span class="sxs-lookup"><span data-stu-id="b07de-126">A named connection to a remote repository, such as the "origin" or "upstream" remote.</span></span> <span data-ttu-id="b07de-127">Git 称之为“远程源”，因为它们可用于引用托管在另一台计算机上的存储库。</span><span class="sxs-lookup"><span data-stu-id="b07de-127">Git refers to this as remote because it is used to reference a repository that's hosted on another computer.</span></span> <span data-ttu-id="b07de-128">在此工作流中，远程始终是一个 GitHub 存储库。</span><span class="sxs-lookup"><span data-stu-id="b07de-128">In this workflow, a remote is always a GitHub repository.</span></span>|
|<span data-ttu-id="b07de-129">源</span><span class="sxs-lookup"><span data-stu-id="b07de-129">origin</span></span>|<span data-ttu-id="b07de-130">分配给本地存储库与在其中进行克隆的源存储库之间的连接的名称。</span><span class="sxs-lookup"><span data-stu-id="b07de-130">The name assigned to the connection between your local repository and the repository from which it was cloned.</span></span> <span data-ttu-id="b07de-131">在此工作流中，源表示与分支的连接。</span><span class="sxs-lookup"><span data-stu-id="b07de-131">In this workflow, origin represents the connection to your fork.</span></span> <span data-ttu-id="b07de-132">它有时用作源存储库本身的一个名字对象，如“请务必将更改推送到源”。</span><span class="sxs-lookup"><span data-stu-id="b07de-132">It's sometimes used as a moniker for the origin repository itself, as in "Remember to push your changes to origin."</span></span>|
|<span data-ttu-id="b07de-133">上游</span><span class="sxs-lookup"><span data-stu-id="b07de-133">upstream</span></span>|<span data-ttu-id="b07de-134">与源远程一样，上游是与另一个存储库的命名连接。</span><span class="sxs-lookup"><span data-stu-id="b07de-134">Like the origin remote, upstream is a named connection to another repository.</span></span> <span data-ttu-id="b07de-135">在此工作流中，上游表示本地存储库与在其中创建分支的主存储库之间的连接。</span><span class="sxs-lookup"><span data-stu-id="b07de-135">In this workflow, upstream represents the connection between your local repository and the main repository, from which your fork was created.</span></span> <span data-ttu-id="b07de-136">它有时用作上游存储库本身的一个名字对象，如“请务必从上游拉取更改”。</span><span class="sxs-lookup"><span data-stu-id="b07de-136">It's sometimes used as a moniker for the upstream repository itself, as in "Remember to pull the changes from upstream."</span></span>|

## <a name="workflow"></a><span data-ttu-id="b07de-137">工作流</span><span class="sxs-lookup"><span data-stu-id="b07de-137">Workflow</span></span>

>[!IMPORTANT]
> <span data-ttu-id="b07de-138">如果尚未完成这些步骤，则必须在[设置](get-started-setup-github.md)部分完成。</span><span class="sxs-lookup"><span data-stu-id="b07de-138">If you haven't already, you must complete the steps in the [Setup](get-started-setup-github.md) section.</span></span> <span data-ttu-id="b07de-139">本节内容指导你完成设置 GitHub 帐户、安装 Git Bash 和 Markdown 编辑器、创建分支，并设置本地存储库。</span><span class="sxs-lookup"><span data-stu-id="b07de-139">This section walks you through setting up your GitHub account, installing Git Bash and a Markdown editor, creating a fork, and setting up your local repository.</span></span> <span data-ttu-id="b07de-140">如果你不熟悉 Git 和 GitHub 概念（如存储库或分支），请首先回顾一下 [Git 和 GitHub 基础知识](git-github-fundamentals.md)。</span><span class="sxs-lookup"><span data-stu-id="b07de-140">If you are unfamiliar with Git and GitHub concepts such as a repository or branch, please first review [Git and GitHub fundamentals](git-github-fundamentals.md).</span></span>

<span data-ttu-id="b07de-141">在此工作流中，更改在重复循环中传递。</span><span class="sxs-lookup"><span data-stu-id="b07de-141">In this workflow, changes flow in a repetitive cycle.</span></span> <span data-ttu-id="b07de-142">从设备的本地存储库开始，它们会传递回 GitHub 分支，进入主 GitHub 存储库，然后在你合并其他参与者提供的更改时再次回到本地。</span><span class="sxs-lookup"><span data-stu-id="b07de-142">Starting from your device's local repository, they flow back up to your GitHub fork, into the main GitHub repository, and back down locally again as you incorporate changes from other contributors.</span></span>

### <a name="use-github-flow"></a><span data-ttu-id="b07de-143">使用 GitHub 流</span><span class="sxs-lookup"><span data-stu-id="b07de-143">Use GitHub flow</span></span>

<span data-ttu-id="b07de-144">回顾 [Git 和 GitHub 基础知识](git-github-fundamentals.md#git)，Git 存储库包含一个主分支，以及未集成到主分支的任何正在工作的额外分支。</span><span class="sxs-lookup"><span data-stu-id="b07de-144">Recall from [Git and GitHub fundamentals](git-github-fundamentals.md#git) that a Git repository contains a master branch, plus any additional work-in-progress branches that have not been integrated into master.</span></span> <span data-ttu-id="b07de-145">每当要引入一组在逻辑上有关联的更改时，最佳做法是创建一个工作分支，用于通过工作流来管理更改  。</span><span class="sxs-lookup"><span data-stu-id="b07de-145">Whenever you introduce a set of logically related changes, it’s a best practice to create a *working branch* to manage your changes through the workflow.</span></span> <span data-ttu-id="b07de-146">这里之所以将其称为工作分支，是因为它是一个会不断迭代/优化更改直至其可集成回主分支的工作空间。</span><span class="sxs-lookup"><span data-stu-id="b07de-146">We refer to it here as a working branch because it's a workspace to iterate/refine changes, until they can be integrated back into the master branch.</span></span>

<span data-ttu-id="b07de-147">将相关的更改隔离到特定的分支中，可以使你独立地控制和引入这些更改，并将它们定向到发布周期中的特定发布时间。</span><span class="sxs-lookup"><span data-stu-id="b07de-147">Isolating related changes to a specific branch allows you to control and introduce those changes independently, targeting them to a specific release time in the publishing cycle.</span></span> <span data-ttu-id="b07de-148">实际上，根据所执行的工作类型，你可以很容易地实现在存储库中使用多个工作分支。</span><span class="sxs-lookup"><span data-stu-id="b07de-148">In reality, depending on the type of work you do, you can easily end up with several working branches in your repository.</span></span> <span data-ttu-id="b07de-149">同时使用多个分支很常见，每一项工作都代表一个不同的项目。</span><span class="sxs-lookup"><span data-stu-id="b07de-149">It's not uncommon to be working on multiple branches at the same time, each representing a different project.</span></span>

>[!TIP]
><span data-ttu-id="b07de-150">在主分支中进行更改并不是最佳做法  。</span><span class="sxs-lookup"><span data-stu-id="b07de-150">Making your changes in the master branch is *not* a good practice.</span></span> <span data-ttu-id="b07de-151">想象一下，如果你使用主分支为定时功能发布引入一组更改。</span><span class="sxs-lookup"><span data-stu-id="b07de-151">Imagine that you use the master branch to introduce a set of changes for a timed feature release.</span></span> <span data-ttu-id="b07de-152">你已完成更改，并等待发布更改。</span><span class="sxs-lookup"><span data-stu-id="b07de-152">You finish the changes and are waiting to release them.</span></span> <span data-ttu-id="b07de-153">然后，在过渡期间，你收到一个需要修复某些内容的紧急请求，因此你将在主分支中更改一个文件，然后发布该更改。</span><span class="sxs-lookup"><span data-stu-id="b07de-153">Then in the interim, you have an urgent request to fix something, so you make the change to a file in the master branch and then publish the change.</span></span> <span data-ttu-id="b07de-154">在本示例中，你可能无意中发布了修正和更改，而这些内容本应在特定日期发布  。</span><span class="sxs-lookup"><span data-stu-id="b07de-154">In this example, you inadvertently publish both the fix *and* the changes that you were holding for release on a specific date.</span></span>

<span data-ttu-id="b07de-155">现在，让我们在本地存储库中创建一个新的工作分支，以获取你所建议的更改。</span><span class="sxs-lookup"><span data-stu-id="b07de-155">Now let's create a new working branch in your local repository, to capture your proposed changes.</span></span> <span data-ttu-id="b07de-156">如果已设置 Git Bash（请参阅[安装内容创作工具](get-started-setup-tools.md)），则可以创建新的分支，并使用一个命令从克隆的存储库中“签出”该分支：</span><span class="sxs-lookup"><span data-stu-id="b07de-156">If you've setup Git Bash (see [Install content authoring tools](get-started-setup-tools.md)), you can create a new branch and "checkout" that branch with one command from within your cloned repository:</span></span>

````
git checkout -b "branchname"
````

<span data-ttu-id="b07de-157">每个 Git 客户端都不同，因此有关首选客户端，请咨询帮助。</span><span class="sxs-lookup"><span data-stu-id="b07de-157">Each git client is different, so consult the help for your preferred client.</span></span> <span data-ttu-id="b07de-158">你可以在 [GitHub 流](https://guides.github.com/introduction/flow/)上的 GitHub 指南中查看过程概览。</span><span class="sxs-lookup"><span data-stu-id="b07de-158">You can see an overview of the process in the GitHub Guide on [GitHub flow](https://guides.github.com/introduction/flow/).</span></span>

## <a name="making-your-changes"></a><span data-ttu-id="b07de-159">执行更改</span><span class="sxs-lookup"><span data-stu-id="b07de-159">Making your changes</span></span>

<span data-ttu-id="b07de-160">获得了 Microsoft 存储库的副本（“克隆”）并创建了分支后，现在即可随时使用任何文本或 Markdown 编辑器执行可能对社区有益的任何更改（如[安装内容创作工具](get-started-setup-tools.md)页面所述）。</span><span class="sxs-lookup"><span data-stu-id="b07de-160">Now that you have a copy ("clone") of the Microsoft repository and you've created a branch, you're now free to make whatever changes you think would benefit the community using any text or Markdown editor, as outlined on the [Install content authoring tools](get-started-setup-tools.md) page.</span></span>  <span data-ttu-id="b07de-161">可以在本地保存更改，而无需将更改提交到 Microsoft，准备就绪后再提交即可。</span><span class="sxs-lookup"><span data-stu-id="b07de-161">You can save your changes locally without needing to submit them to Microsoft until you're ready.</span></span>

## <a name="saving-changes-to-your-repository"></a><span data-ttu-id="b07de-162">将更改保存到存储库</span><span class="sxs-lookup"><span data-stu-id="b07de-162">Saving changes to your repository</span></span>

<span data-ttu-id="b07de-163">向作者发送更改之前，必须先将更改保存到 Github 存储库。</span><span class="sxs-lookup"><span data-stu-id="b07de-163">Before sending your changes to the author, you must first save them to your Github repository.</span></span>  <span data-ttu-id="b07de-164">同样，尽管所有工具都是不同的，但如果使用的是 Git Bash 命令行，则只需几个简单步骤即可完成此操作。</span><span class="sxs-lookup"><span data-stu-id="b07de-164">Again, while all tools are different, if you're using the Git Bash command line, this can be done in just a few easy steps.</span></span>

<span data-ttu-id="b07de-165">首先，在存储库中，需要暂存所有要提交的更改  。</span><span class="sxs-lookup"><span data-stu-id="b07de-165">First, from within the repository, you need to _stage_ all of your changes to be commmited.</span></span>  <span data-ttu-id="b07de-166">可以通过执行以下命令完成此操作：</span><span class="sxs-lookup"><span data-stu-id="b07de-166">This can be done by executing:</span></span>

````
git add --all
````

<span data-ttu-id="b07de-167">接下来，需要将保存的更改提交到本地存储库。</span><span class="sxs-lookup"><span data-stu-id="b07de-167">Next, you need to commit your saved changes to your local repository.</span></span>  <span data-ttu-id="b07de-168">可以通过运行以下命令在 Git Bash 中完成此操作：</span><span class="sxs-lookup"><span data-stu-id="b07de-168">This can be done in Git Bash by running:</span></span>

````
git commit -m "Short Description of Changes Made"
````

<span data-ttu-id="b07de-169">最后，由于此分支在本地计算机上创建，因此需要使 GitHub.com 帐户中的分支知道此分支的存在。</span><span class="sxs-lookup"><span data-stu-id="b07de-169">Finally, since you created this branch on your local computer, you need to let the fork in your GitHub.com account know about it.</span></span>  <span data-ttu-id="b07de-170">如果使用的是 Git Bash，可通过运行以下命令完成此操作：</span><span class="sxs-lookup"><span data-stu-id="b07de-170">If you're using Git Bash, this can be done by running:</span></span>

````
git push --set-upstream origin <branchname>
````

<span data-ttu-id="b07de-171">大功告成！</span><span class="sxs-lookup"><span data-stu-id="b07de-171">You've done it!</span></span>  <span data-ttu-id="b07de-172">你的代码现在将在 GitHub 存储库中，并可用于创建拉取请求。</span><span class="sxs-lookup"><span data-stu-id="b07de-172">Your code is now up in your GitHub repository and ready for you to create a pull request.</span></span>  

>[!TIP]
> <span data-ttu-id="b07de-173">尽管更改在推送后即会在个人 GitHub 帐户中可见，但不需要立即提交拉取请求。</span><span class="sxs-lookup"><span data-stu-id="b07de-173">Even though your changes become visible in your personal GitHub account when you push them, there is no rule that you need to submit a pull request immediately.</span></span>  <span data-ttu-id="b07de-174">如果想要停止并稍后返回进行其他调整，这完全没问题！</span><span class="sxs-lookup"><span data-stu-id="b07de-174">If you want to come stop and return at a later time to make additional tweaks, that's OK!</span></span>

<span data-ttu-id="b07de-175">需要修复已提交的内容？</span><span class="sxs-lookup"><span data-stu-id="b07de-175">Need to fix something you submitted?</span></span>  <span data-ttu-id="b07de-176">没问题！</span><span class="sxs-lookup"><span data-stu-id="b07de-176">No problem!</span></span>  <span data-ttu-id="b07de-177">只需在同一分支中进行更改，然后重新提交并推送即可（无需对同一分支的后续推送设置上游服务器）。</span><span class="sxs-lookup"><span data-stu-id="b07de-177">Just make your changes in the same branch and then commit and push again (no need to set the upstream server on subsequent pushes of the same branch).</span></span>

## <a name="making-your-next-change"></a><span data-ttu-id="b07de-178">进行下一步更改</span><span class="sxs-lookup"><span data-stu-id="b07de-178">Making your next change</span></span>

<span data-ttu-id="b07de-179">需要执行更多与此分支无关的更改？</span><span class="sxs-lookup"><span data-stu-id="b07de-179">Got more changes you need to make unrelated to this one?</span></span> <span data-ttu-id="b07de-180">切换回主分支，从上游存储库拉取，以确保分支保持最新且签出新分支。</span><span class="sxs-lookup"><span data-stu-id="b07de-180">Switch back to the master branch, pull from the upstream repository to make sure that your fork is up to date, and check out a new branch.</span></span>  <span data-ttu-id="b07de-181">在 Git Bash 中运行以下命令：</span><span class="sxs-lookup"><span data-stu-id="b07de-181">Run the following commands in Git Bash:</span></span>

````
git checkout master
git pull upstream master
git checkout -b "branchname"
````

<span data-ttu-id="b07de-182">现已位于新分支中，你即将成为主要供稿人。</span><span class="sxs-lookup"><span data-stu-id="b07de-182">You're now back in a new branch and you're well on your way to being a master contributer.</span></span>

[!INCLUDE[contribute-how-to-write-workflows-pull-request-processing](includes/contribute-how-to-write-workflows-pull-request-processing.md)]

## <a name="next-steps"></a><span data-ttu-id="b07de-183">后续步骤</span><span class="sxs-lookup"><span data-stu-id="b07de-183">Next steps</span></span>

<span data-ttu-id="b07de-184">就这么简单！</span><span class="sxs-lookup"><span data-stu-id="b07de-184">That's it!</span></span> <span data-ttu-id="b07de-185">你已完成参与 docs.microsoft.com 内容的供稿！</span><span class="sxs-lookup"><span data-stu-id="b07de-185">You've made a contribution to docs.microsoft.com content!</span></span>

- <span data-ttu-id="b07de-186">继续查看 [Markdown 引用](markdown-reference.md)一文，详细了解 Markdown 和 Markdown 扩展语法等主题。</span><span class="sxs-lookup"><span data-stu-id="b07de-186">To learn more about topics such as Markdown and Markdown extensions syntax, continue to the [Markdown reference](markdown-reference.md) article.</span></span>
