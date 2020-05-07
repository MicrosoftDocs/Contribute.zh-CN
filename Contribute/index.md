---
title: Microsoft Docs 参与者指南概述
description: 本文介绍如何为 Microsoft 文档站点 docs.microsoft.com 贡献内容。
author: billwagner
ms.author: wiwagn
ms.date: 02/19/2019
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
ms.openlocfilehash: 95dadff41bb31e0b34ee34f85ae47708297954f1
ms.sourcegitcommit: cfba5ad25b898bfed76046126ce8ff4871910701
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/04/2020
ms.locfileid: "81784283"
---
# <a name="microsoft-docs-contributor-guide-overview"></a>Microsoft Docs 参与者指南概述

欢迎查看 [docs.microsoft.com](https://docs.microsoft.com) (Docs) 参与者指南！

一些 Microsoft 文档集是托管在 GitHub 上的开源资源。 并非所有文档集都是完全开放的资源，但许多文档集有面向公众的存储库，你可在其中通过拉取请求提交更改建议。 这种开源方法简化了产品工程师、内容团队和客户之间的沟通流程，提高了效率，并实现了其他优势：

- 开源存储库以公开方式计划，通过反馈得知哪些文档的需求量最大。
- 开源存储库以公开方式评审，以便针对首个版本发布最具帮助意义的内容。
- 开源存储库以公开方式更新，让我们能够更加方便地持续改进内容。

[docs.microsoft.com](https://docs.microsoft.com) 上的用户体验直接集成 [GitHub](https://github.com) 工作流，操作更简单。 你可以从[编辑正在查看的文档](#quick-edits-to-existing-documents)开始， 也可以通过[审查新主题](#review-open-prs)或[创建质量问题](#create-quality-issues)来提供帮助。

> [!IMPORTANT]
> 发布到 docs.microsoft.com 的所有存储库均遵循 [Microsoft 开放源代码行为准则](https://opensource.microsoft.com/codeofconduct/)或 [.NET 基础行为准则](https://dotnetfoundation.org/code-of-conduct)。 有关详细信息，请参阅[行为准则常见问题解答](https://opensource.microsoft.com/codeofconduct/faq/)。 或如有任何疑问或意见，请联系 [opencode@microsoft.com](mailto:opencode@microsoft.com) 或 [conduct@dotnetfoundation.org](mailto:conduct@dotnetfoundation.org)。<br>
>
> [docs.microsoft.com 使用条款](https://docs.microsoft.com/legal/termsofuse)适用于对公共存储库中文档和代码示例所做的小修订和澄清。 如果你不是 Microsoft 的员工，那么新内容或重大更改会在拉取请求中生成一条评论，要求你在线提交一份贡献许可协议 (CLA)。 在我们评审或接受拉取请求之前，需要你填写这份在线表单。

## <a name="quick-edits-to-existing-documents"></a>对现有文档进行快速编辑

快速编辑可简化报告并修复文档中的小错误和遗漏的过程。 尽管我们做出了各种各样的努力，我们发布的文档中仍可能出现小的语法错误和拼写错误。 你可以通过创建问题来报告错误，但更加快捷和简单的做法是通过创建拉取请求来解决问题（如果创建拉取请求的选项可用）。

1. 你可以在浏览器中直接编辑某些文档页面的内容。 如果是这样，便会看到如下所示的“编辑”按钮。 单击“编辑”（或等效的本地化名称）按钮将转到 GitHub 上的源文件。 如果未显示“编辑”按钮（铅笔图标，不包含文本），则意味着无法更改文档页。

   ![“编辑”链接的位置](./media/index/edit-article.png)

2. 接下来，单击铅笔图标来编辑文章，如下所示。 如果铅笔图标呈灰显，则你需要登录到 GitHub 帐户，或者创建一个新帐户。 

   ![铅笔图标的位置](./media/index/edit-icon.png)


3. 在 Web 编辑器中进行更改。 这是使用称为“拉取请求”的操作来完成的。

4. 做出更改后，滚动到页面底部。 为拉取请求输入标题和描述，并单击“建议文件更改”（Propose file change），如下图所示：

   ![建议文件更改](./media/index/submit-pull-request.png)

5. 你已经提出更改，现在需要请求存储库的所有者将更改“拉取”到其存储库。 这是使用称为“拉取请求”的操作完成的。 单击上图中的“建议文件更改”时，你应该会进入一个如下图所示的新页面：

   ![创建拉取请求](media/index/create-pull-request.png)

   单击“创建拉取请求”（Create pull request），为拉取请求输入标题（以及可选的描述），然后再次单击“创建拉取请求”。 （如果不熟悉 GitHub，请参阅[关于拉取请求](https://help.github.com/en/articles/about-pull-requests)，了解详细信息。）

6. 就这么简单！ 内容团队成员将评审并合并你的拉取请求。 如果你进行了更大范围的更改，可能会收到一些请求更改的反馈。

GitHub 编辑界面会根据你在存储库上的权限做出响应。 前面的图片适用于那些对目标存储库没有写入权限的参与者。 GitHub 会在你的帐户中自动创建目标存储库的一个分叉 (fork)。 如果你有目标存储库的写入访问权限，GitHub 将在目标存储库中创建一个新分支 (branch)。 分支名称采用 **\<GitHubId\>-patch-n** 形式，使用的是你的 GitHub ID 和此修改分支的数字标识符。

我们使用拉取请求进行所有更改，即使更改来自于拥有写入权限的参与者，也不例外。 大多数存储库都保护 `master` 分支。这样一来，必须将更新提交为拉取请求。

浏览器内编辑体验最适合进行细微或不频繁的更改。 如果你想贡献大量内容，或者使用高级 Git 功能（例如分支管理或高级合并冲突解决），则需要为[存储库创建分叉，以便在本地工作](how-to-write-workflows-major.md)。

> [!NOTE]
> 如果可用，你可以编辑一篇文章的任何语言版本，而且根据编辑的类型将出现以下情况：
> 1. 任何经过批准的语言更改也将用于帮助改进我们的机器翻译引擎
> 2. 任何显著修改文章内容的编辑都将在内部进行处理，以便针对同一文章的英语版本提交更改，从而在获得批准后，将编辑内容本地化为其他语言。
> 你建议的改进不仅会给你自己语言的文章带来正面影响，还会影响其他所有可用语言。

## <a name="review-open-prs"></a>评审待定的拉取请求

在新主题发布之前，你可以通过检查当前待定的拉取请求来阅读它们。 评审的过程遵循 [GitHub 工作流](https://guides.github.com/introduction/flow/)。 你可以在公开存储库中看到建议的更新或新文章。 审阅这些内容并添加备注。 请随意查看我们的文档存储库，并在你感兴趣的领域里查看待定的拉取请求。 针对更新建议的社区反馈有益于整个社区。

## <a name="create-quality-issues"></a>创建质量问题

我们的文档需要持续完善。 高质量的问题反馈有助于我们将精力集中在社区的首要问题上。 你提供的信息越详尽，问题反馈就越有帮助。 告诉我们你想获取的信息。 告诉我们你所用的搜索词。 如果你不知从哪里入手，告诉我们你希望如何开始探索不熟悉的技术。

许多 Microsoft 文档页的底部都有“反馈”部分，可以单击此部分来提供“产品反馈”或“内容反馈”，以跟踪相应文章的具体问题。

问题反馈可以开启关于所需内容的对话。 内容团队将对这些问题反馈作出回应，同时针对我们可以添加哪些内容表明自己的想法，并征求你的意见。 当我们创建草稿时，会请求你[对拉取请求进行评审](#review-open-prs)。

## <a name="get-more-involved"></a>更多地参与

其他主题将帮助你高效地开始为 Microsoft Docs 贡献内容。它们介绍了如何使用 GitHub 存储库、Markdown 工具和 Microsoft Docs 平台中的扩展。
