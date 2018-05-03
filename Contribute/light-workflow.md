---
title: 次要更改或间歇更改的 GitHub 参与工作流
description: 本文介绍如何使用“次要”参与者工作流参与 docs.microsoft.com 文章的供稿。
author: bryanla
ms.author: bryanla
manager: mbaldwin
ms.date: 10/06/2017
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.custom: external-contributor-guide
ms.openlocfilehash: 8bde44d502e1942b0870df9dd546a97705c2bb4f
ms.sourcegitcommit: de6e6b6ca641fdd5b30eb46deee9ac3a500089ef
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/28/2018
---
# <a name="github-contribution-workflow-for-minor-or-infrequent-changes"></a><span data-ttu-id="39ce1-103">次要更改或间歇更改的 GitHub 参与工作流</span><span class="sxs-lookup"><span data-stu-id="39ce1-103">GitHub contribution workflow for minor or infrequent changes</span></span>

> [!IMPORTANT]
> <span data-ttu-id="39ce1-104">发布到 docs.microsoft.com 的所有存储库均遵循 [Microsoft 开放源代码行为准则](https://opensource.microsoft.com/codeofconduct/)或 [.NET 基础行为准则](https://dotnetfoundation.org/code-of-conduct)。</span><span class="sxs-lookup"><span data-stu-id="39ce1-104">All repositories that publish to docs.microsoft.com have adopted either the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/) or the [.NET Foundation Code of Conduct](https://dotnetfoundation.org/code-of-conduct).</span></span> <span data-ttu-id="39ce1-105">有关详细信息，请参阅[行为准则常见问题解答](https://opensource.microsoft.com/codeofconduct/faq/)。</span><span class="sxs-lookup"><span data-stu-id="39ce1-105">For more information, see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/).</span></span> <span data-ttu-id="39ce1-106">或如有任何疑问或意见，请联系 [opencode@microsoft.com](mailto:opencode@microsoft.com) 或 [conduct@dotnetfoundation.org](mailto:conduct@dotnetfoundation.org)。</span><span class="sxs-lookup"><span data-stu-id="39ce1-106">Or contact [opencode@microsoft.com](mailto:opencode@microsoft.com), or [conduct@dotnetfoundation.org](mailto:conduct@dotnetfoundation.org) with any questions or comments.</span></span><br>
>
> <span data-ttu-id="39ce1-107">[docs.microsoft.com 使用条款](https://docs.microsoft.com/legal/termsofuse)涵盖公共存储库中对文档和代码示例所做的轻微更正和澄清。</span><span class="sxs-lookup"><span data-stu-id="39ce1-107">Minor corrections or clarifications to documentation and code examples in public repositories are covered by the [docs.microsoft.com Terms of Use](https://docs.microsoft.com/legal/termsofuse).</span></span> <span data-ttu-id="39ce1-108">如果你不是 Microsoft 的员工，那么新更改或重大更改会在拉取请求中生成一条注释，要求提交一份在线参与许可协议 (CLA)。</span><span class="sxs-lookup"><span data-stu-id="39ce1-108">New or significant changes will generate a comment in the pull request, asking you to submit an online Contribution License Agreement (CLA) if you are not an employee of Microsoft.</span></span> <span data-ttu-id="39ce1-109">在我们接受拉取请求之前，需要你填写这份在线表单。</span><span class="sxs-lookup"><span data-stu-id="39ce1-109">We need you to complete the online form before we can accept your pull request.</span></span>

## <a name="overview"></a><span data-ttu-id="39ce1-110">概述</span><span class="sxs-lookup"><span data-stu-id="39ce1-110">Overview</span></span>

<span data-ttu-id="39ce1-111">通过使用 GitHub 基于 Web 的 Markdown 编辑器，此工作流适用于执行次要更改或间歇更改的情况。</span><span class="sxs-lookup"><span data-stu-id="39ce1-111">This workflow is suitable for making minor or infrequent changes, by using GitHub's web-based Markdown editor.</span></span> <span data-ttu-id="39ce1-112">GitHub 编辑器对于可执行的操作存在限制，因为 UI 并非支持所有 Git 操作和创作方案。</span><span class="sxs-lookup"><span data-stu-id="39ce1-112">The GitHub editor is limited in terms of what you can do, because the UI does not support all Git operations and authoring scenarios.</span></span> <span data-ttu-id="39ce1-113">如果你需要大篇幅供稿，或者需要对高级 Git 功能的支持（例如分支管理、高级合并冲突解决），请参阅[主要或持续更改的工作流](full-workflow.md)。</span><span class="sxs-lookup"><span data-stu-id="39ce1-113">If you need to make large contributions, or you need support for advanced Git features (such as branch management or advanced merge conflict resolution), refer to the [major or long-running changes workflow](full-workflow.md).</span></span>

## <a name="procedure-for-using-the-github-editor-to-propose-your-changes"></a><span data-ttu-id="39ce1-114">使用 GitHub 编辑器建议更改的步骤</span><span class="sxs-lookup"><span data-stu-id="39ce1-114">Procedure for using the GitHub editor to propose your changes</span></span>

1. <span data-ttu-id="39ce1-115">浏览到文章对应的 GitHub 存储库和 Markdown 文件。</span><span class="sxs-lookup"><span data-stu-id="39ce1-115">Browse to the article's corresponding GitHub repository and Markdown file.</span></span> <span data-ttu-id="39ce1-116">可以使用以下方法之一：</span><span class="sxs-lookup"><span data-stu-id="39ce1-116">You can use either of the following methods:</span></span>

   - <span data-ttu-id="39ce1-117">通过浏览相关 GitHub 存储库中的 Markdown 文件找到文章。</span><span class="sxs-lookup"><span data-stu-id="39ce1-117">Find the article by browsing through the Markdown files in the related GitHub repository.</span></span>
   - <span data-ttu-id="39ce1-118">转到 [docs.microsoft.com](https://docs.microsoft.com/) 上的文章，选择右上角的“编辑”链接。</span><span class="sxs-lookup"><span data-stu-id="39ce1-118">Go to the article on [docs.microsoft.com](https://docs.microsoft.com/) and select the **Edit** link in the upper-right corner of the page.</span></span>

     ![“编辑”链接的位置](./media/light-workflow/contributetogit.png)

2. <span data-ttu-id="39ce1-120">选择“编辑此文件”铅笔图标，进入编辑模式：</span><span class="sxs-lookup"><span data-stu-id="39ce1-120">Select the **Edit this file** pencil icon to go into edit mode:</span></span>

    ![铅笔图标的位置](./media/light-workflow/editicon.png)

3. <span data-ttu-id="39ce1-122">使用“编辑文件”选项卡上的 Markdown 进行更改，并在“预览更改”选项卡上预览所做的更改。编辑器的使用相当简单，不过，如果你需要帮助，请参阅以下指南：</span><span class="sxs-lookup"><span data-stu-id="39ce1-122">Make changes by using Markdown on the **Edit file** tab, and preview your changes on the **Preview changes** tab. Using the editor is fairly straightforward, but if you need assistance, see the following guides:</span></span>

   - [<span data-ttu-id="39ce1-123">如何使用 Markdown</span><span class="sxs-lookup"><span data-stu-id="39ce1-123">How to use Markdown</span></span>](how-to-write-use-markdown.md)
   - [<span data-ttu-id="39ce1-124">在 GitHub 上创建文件</span><span class="sxs-lookup"><span data-stu-id="39ce1-124">Creating files on GitHub</span></span>](https://github.com/blog/1327-creating-files-on-github)
   - [<span data-ttu-id="39ce1-125">将文件上传到存储库</span><span class="sxs-lookup"><span data-stu-id="39ce1-125">Upload files to your repositories</span></span>](https://github.com/blog/2105-upload-files-to-your-repositories)

4. <span data-ttu-id="39ce1-126">滚动到页面底部，会看到下列任一项内容：</span><span class="sxs-lookup"><span data-stu-id="39ce1-126">Scroll to the bottom of the page, where you see one of the following:</span></span>

   - <span data-ttu-id="39ce1-127">**建议文件更改**：如果对存储库具有只读访问权限，则显示此内容，例如[在另一个用户的存储库中编辑文件](https://help.github.com/articles/editing-files-in-another-user-s-repository/)。</span><span class="sxs-lookup"><span data-stu-id="39ce1-127">**Propose file change**: Appears when you have read-only access to the repository, such as [editing files in another user's repository](https://help.github.com/articles/editing-files-in-another-user-s-repository/).</span></span> <span data-ttu-id="39ce1-128">在这种情况下，GitHub 会在存储库的分支中创建一个“修补”分支（如果不存在分支，则会自动创建一个）。</span><span class="sxs-lookup"><span data-stu-id="39ce1-128">In this case, GitHub will create a "patch" branch in your fork of the repository (and automatically create a fork if it doesn't exist).</span></span> <span data-ttu-id="39ce1-129">选择“建议文件更改”后，可以看到“比较更改”页，可以在其中验证更改。</span><span class="sxs-lookup"><span data-stu-id="39ce1-129">After you select **Propose file change**, a **Comparing changes** page appears so you can verify your changes.</span></span> <span data-ttu-id="39ce1-130">然后选择“创建拉取请求”按钮，将更改提交到拉取请求队列，并继续执行[下一部分](#pull-request-processing)。</span><span class="sxs-lookup"><span data-stu-id="39ce1-130">Then select the **Create pull request** button to submit your changes to the pull request queue, and proceed to the [next section](#pull-request-processing).</span></span>

   - <span data-ttu-id="39ce1-131">**提交更改**：如果对存储库具有写入权限（例如[在自己的存储库中编辑文件](https://help.github.com/articles/editing-files-in-your-repository/)），则显示此内容。</span><span class="sxs-lookup"><span data-stu-id="39ce1-131">**Commit changes**: Appears when you have write permissions to a repository, such as [editing files in your own repository](https://help.github.com/articles/editing-files-in-your-repository/).</span></span> <span data-ttu-id="39ce1-132">在这种情况下，GitHub 提供两个选项用于保存更改：</span><span class="sxs-lookup"><span data-stu-id="39ce1-132">In this case, GitHub gives you two options for saving your changes:</span></span>

     - <span data-ttu-id="39ce1-133">“直接提交到 `<branch-name>` 分支”，其中 `<branch-name>` 是在选择“编辑”按钮时你所在分支的名称。</span><span class="sxs-lookup"><span data-stu-id="39ce1-133">**Commit directly to the `<branch-name>` branch**, where `<branch-name>` is the name of the branch that you were on when you selected the **Edit** button.</span></span> <span data-ttu-id="39ce1-134">这可以将你的更改直接应用到分支，而无需使用拉取请求。</span><span class="sxs-lookup"><span data-stu-id="39ce1-134">This applies your changes directly to the branch instead of using a pull request.</span></span> <span data-ttu-id="39ce1-135">至此，已完成提交！</span><span class="sxs-lookup"><span data-stu-id="39ce1-135">At this point, you're finished!</span></span>

     - <span data-ttu-id="39ce1-136">“为此提交创建一个新分支，并启动拉取请求”，它会提示使用一个默认名称来创建新分支。</span><span class="sxs-lookup"><span data-stu-id="39ce1-136">**Create a new branch for this commit and start a pull request**, which prompts you with a default name to create a new branch.</span></span> <span data-ttu-id="39ce1-137">选择“建议文件更改”后，可以看到“比较更改”页，可以在其中验证更改。</span><span class="sxs-lookup"><span data-stu-id="39ce1-137">After you select **Propose file change**, a **Comparing changes** page appears so you can verify your changes.</span></span> <span data-ttu-id="39ce1-138">然后选择“创建拉取请求”按钮，将更改提交到拉取请求队列，并继续执行[下一部分](#pull-request-processing)。</span><span class="sxs-lookup"><span data-stu-id="39ce1-138">Then select the **Create pull request** button to submit your changes to the pull request queue, and proceed to the [next section](#pull-request-processing).</span></span>

[!INCLUDE[contribute-how-to-write-workflows-pull-request-processing](includes/contribute-how-to-write-workflows-pull-request-processing.md)]

## <a name="next-steps"></a><span data-ttu-id="39ce1-139">后续步骤</span><span class="sxs-lookup"><span data-stu-id="39ce1-139">Next steps</span></span>

- <span data-ttu-id="39ce1-140">继续查看“撰写要领”文章，了解 Markdown 和 Markdown 扩展语法等的详细信息。</span><span class="sxs-lookup"><span data-stu-id="39ce1-140">Continue to the "Writing essentials" articles to learn more about Markdown, Markdown extensions syntax, and more.</span></span>
