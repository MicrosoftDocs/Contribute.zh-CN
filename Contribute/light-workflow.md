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
# <a name="github-contribution-workflow-for-minor-or-infrequent-changes"></a>次要更改或间歇更改的 GitHub 参与工作流

> [!IMPORTANT]
> 发布到 docs.microsoft.com 的所有存储库均遵循 [Microsoft 开放源代码行为准则](https://opensource.microsoft.com/codeofconduct/)或 [.NET 基础行为准则](https://dotnetfoundation.org/code-of-conduct)。 有关详细信息，请参阅[行为准则常见问题解答](https://opensource.microsoft.com/codeofconduct/faq/)。 或如有任何疑问或意见，请联系 [opencode@microsoft.com](mailto:opencode@microsoft.com) 或 [conduct@dotnetfoundation.org](mailto:conduct@dotnetfoundation.org)。<br>
>
> [docs.microsoft.com 使用条款](https://docs.microsoft.com/legal/termsofuse)涵盖公共存储库中对文档和代码示例所做的轻微更正和澄清。 如果你不是 Microsoft 的员工，那么新更改或重大更改会在拉取请求中生成一条注释，要求提交一份在线参与许可协议 (CLA)。 在我们接受拉取请求之前，需要你填写这份在线表单。

## <a name="overview"></a>概述

通过使用 GitHub 基于 Web 的 Markdown 编辑器，此工作流适用于执行次要更改或间歇更改的情况。 GitHub 编辑器对于可执行的操作存在限制，因为 UI 并非支持所有 Git 操作和创作方案。 如果你需要大篇幅供稿，或者需要对高级 Git 功能的支持（例如分支管理、高级合并冲突解决），请参阅[主要或持续更改的工作流](full-workflow.md)。

## <a name="procedure-for-using-the-github-editor-to-propose-your-changes"></a>使用 GitHub 编辑器建议更改的步骤

1. 浏览到文章对应的 GitHub 存储库和 Markdown 文件。 可以使用以下方法之一：

   - 通过浏览相关 GitHub 存储库中的 Markdown 文件找到文章。
   - 转到 [docs.microsoft.com](https://docs.microsoft.com/) 上的文章，选择右上角的“编辑”链接。

     ![“编辑”链接的位置](./media/light-workflow/contributetogit.png)

2. 选择“编辑此文件”铅笔图标，进入编辑模式：

    ![铅笔图标的位置](./media/light-workflow/editicon.png)

3. 使用“编辑文件”选项卡上的 Markdown 进行更改，并在“预览更改”选项卡上预览所做的更改。编辑器的使用相当简单，不过，如果你需要帮助，请参阅以下指南：

   - [如何使用 Markdown](how-to-write-use-markdown.md)
   - [在 GitHub 上创建文件](https://github.com/blog/1327-creating-files-on-github)
   - [将文件上传到存储库](https://github.com/blog/2105-upload-files-to-your-repositories)

4. 滚动到页面底部，会看到下列任一项内容：

   - **建议文件更改**：如果对存储库具有只读访问权限，则显示此内容，例如[在另一个用户的存储库中编辑文件](https://help.github.com/articles/editing-files-in-another-user-s-repository/)。 在这种情况下，GitHub 会在存储库的分支中创建一个“修补”分支（如果不存在分支，则会自动创建一个）。 选择“建议文件更改”后，可以看到“比较更改”页，可以在其中验证更改。 然后选择“创建拉取请求”按钮，将更改提交到拉取请求队列，并继续执行[下一部分](#pull-request-processing)。

   - **提交更改**：如果对存储库具有写入权限（例如[在自己的存储库中编辑文件](https://help.github.com/articles/editing-files-in-your-repository/)），则显示此内容。 在这种情况下，GitHub 提供两个选项用于保存更改：

     - “直接提交到 `<branch-name>` 分支”，其中 `<branch-name>` 是在选择“编辑”按钮时你所在分支的名称。 这可以将你的更改直接应用到分支，而无需使用拉取请求。 至此，已完成提交！

     - “为此提交创建一个新分支，并启动拉取请求”，它会提示使用一个默认名称来创建新分支。 选择“建议文件更改”后，可以看到“比较更改”页，可以在其中验证更改。 然后选择“创建拉取请求”按钮，将更改提交到拉取请求队列，并继续执行[下一部分](#pull-request-processing)。

[!INCLUDE[contribute-how-to-write-workflows-pull-request-processing](includes/contribute-how-to-write-workflows-pull-request-processing.md)]

## <a name="next-steps"></a>后续步骤

- 继续查看“撰写要领”文章，了解 Markdown 和 Markdown 扩展语法等的详细信息。
