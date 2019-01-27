---
title: Microsoft Docs 参与者指南概述
description: 本文介绍为 Microsoft 文档站点 docs.microsoft.com 供稿的方式。
author: billwagner
ms.author: wiwagn
manager: wpickett
ms.date: 04/17/2018
ms.openlocfilehash: dab2de80654fb55382b2ca7c9f78df36df9971dc
ms.sourcegitcommit: 44eb4f5ee65c1848d7f36fca107b296eb7687397
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/13/2018
ms.locfileid: "51609352"
---
# <a name="microsoft-docs-contributor-guide-overview"></a>Microsoft Docs 参与者指南概述

欢迎查看 [docs.microsoft.com](https://docs.microsoft.com) (Docs) 参与者指南！

我们的一些文档集是开放源代码，托管在 GitHub 上。 Microsoft 的更多团队一直在采用这种模式。 即使文档集不完全开放源代码，也有面向公众的存储库，其中用户受邀发出拉取请求。 这种模式简化并改善了产品工程师、内容团队和我们的客户之间的通信。 开放式工作有以下几点好处：

- 开放源代码存储库以公开方式计划，获取如下反馈：哪些文档是最需要的。
- 开放源代码存储库以公开方式评审，在我们首个版本中发布最具帮助意义的内容。
- 开放源代码存储库以公开方式更新，持续改进内容变得更加方便。

[docs.microsoft.com](https://docs.microsoft.com) 上的用户体验直接集成 [GitHub](https://github.com) 工作流，操作更简单。 可以从[编辑正在查看的文档](#quick-edits-to-existing-documents)开始。 或者，通过[查看新主题](#review-open-prs)或[创建质量问题](#create-quality-issues)来获取帮助。

> [!IMPORTANT]
> 发布到 docs.microsoft.com 的所有存储库均遵循 [Microsoft 开放源代码行为准则](https://opensource.microsoft.com/codeofconduct/)或 [.NET 基础行为准则](https://dotnetfoundation.org/code-of-conduct)。 有关详细信息，请参阅[行为准则常见问题解答](https://opensource.microsoft.com/codeofconduct/faq/)。 或如有任何疑问或意见，请联系 [opencode@microsoft.com](mailto:opencode@microsoft.com) 或 [conduct@dotnetfoundation.org](mailto:conduct@dotnetfoundation.org)。<br>
>
> [docs.microsoft.com 使用条款](https://docs.microsoft.com/legal/termsofuse)涵盖公共存储库中对文档和代码示例所做的轻微更正和澄清。 如果你不是 Microsoft 的员工，那么新更改或重大更改会在拉取请求中发送一条备注，要求提交一份在线贡献许可协议 (CLA)。 在我们评审或接受拉取请求之前，需要你填写这份在线表单。

## <a name="quick-edits-to-existing-documents"></a>对现有文档进行快速编辑

快速编辑可简化报告和修复文档中的小错误和遗漏的过程。 尽管做出了各种各样的努力，但在我们发布的文档中仍会遇到小的语法错误和拼写错误。 虽然可以创建问题来报告错误，但创建拉取请求 (PR) 来解决此问题速度更快，也更简便。 几乎每一篇文章都显示一个“编辑”按钮，如下图所示。 单击“编辑”（或等效的本地化名称）按钮将转到 GitHub 上的源文件。

![“编辑”链接的位置](./media/index/edit-article.png)

接下来，单击“铅笔”图标（如下图所示）编辑文章。

![铅笔图标的位置](./media/index/editicon.png)

> [!NOTE]
> 如果铅笔图标显示为灰色，需要登录到 GitHub 帐户，或者创建一个新帐户。

在 Web 编辑器中进行更改。 可以单击“预览更改”选项卡来检查更改的格式。

做出更改后，滚动到页面底部。 为 PR 输入标题和描述，并单击“建议文件更改”，如下图所示：

![建议更改](./media/index/submit-pull-request.png)

既然已提出更改，则需要请求存储库的所有者将更改“拉取”到其存储库中。 这是使用称为“拉取请求”的操作完成的。 单击上图中的“建议文件更改”时，应该会进入一个如下图所示的新页面：

![创建拉取请求](media/index/create-pull-request.png)

单击“创建拉取请求”，为拉取请求输入标题（以及可选的描述），然后再次单击“创建拉取请求”。

就这么简单！ 内容团队成员将评审并合并你的 PR。 如果进行了更大范围的更改，可能会收到一些请求更改的反馈。

GitHub 编辑 UI 会响应你在存储库上的权限。 前面的图像对于那些对目标存储库没有写入权限的参与者来说是准确的。 GitHub 会在帐户中自动创建目标存储库的一个分支。 如果你对目标存储库具有写入访问权限，GitHub 将在目标存储库中创建一个新分支。 分支名称采用 \<GitHubId\>-patch-n 形式，使用的是你的 GitHub ID 和修补程序分支的数字标识符。

我们使用 PR 进行所有更改，即使对于具有写入访问权限的参与者也是如此。 大多数存储库都会为 `master` 分支提供保护，使更新必须作为 PR 提交。

浏览器内编辑体验最适合进行细微或不频繁的更改。 如果大篇幅供稿，或者使用高级 Git 功能（例如分支管理或高级合并冲突解决），需要[在本地创建存储库和工作分支](how-to-write-workflows-major.md)。

> [!NOTE]
> 如果启用，则可以使用任何语言编辑文章，并根据编辑类型执行以下操作：
> 1. 任何经过批准的语言更改也将有助于改进我们的机器翻译引擎
> 2. 任何显着修改文章内容的编辑都将在内部进行处理，以提交对英语版本的同一文章的更改，从而在获得批准后，以所有语言对文章进行本地化。
> 因此，你建议的改进不仅会正面地影响你自己语言的文章，还会影响所有可用语言。

## <a name="review-open-prs"></a>评审开放式 PR

在新主题发布之前，可以通过检查当前开放式 PR 来读取新主题。 按照 [GitHub 流](https://guides.github.com/introduction/flow/)过程进行评审。 可以在公共存储库中看到建议的更新或新文章。 审阅这些文章并添加备注。 查看任意文档存储库，并检查感兴趣领域的开放式拉取请求 (PR)。 针对建议更新的社区反馈可以为整个社区提供帮助。

## <a name="create-quality-issues"></a>创建质量问题

我们的文档是一项持续进行的工作。 高质量的问题有助于我们将精力集中在社区的首要问题上。 提供的信息越详尽，问题就越有帮助。 告诉我们你所找寻的信息。 告诉我们你所用的搜索词。 如果开始使用存在困难，告诉我们你希望如何开始探索不熟悉的技术。

问题会就所需的内容展开对话。 内容团队将对这些问题作出回应，同时提议我们可以添加的内容，并征求你的意见。 当我们创建草稿时，会要求你[对 PR 进行评审](#review-open-prs)。

## <a name="get-more-involved"></a>参与更多内容

其他主题将帮助你高效地开始对 Microsoft Docs 进行供稿。它们介绍了如何利用在 Microsoft Docs 平台中使用的 GitHub 存储库、Markdown 工具和扩展。
