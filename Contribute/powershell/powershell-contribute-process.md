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
# <a name="process-for-contributing-to-powershell-docs"></a>参与 PowerShell 文档撰写的过程

感谢社区参与文档撰写。以下列表显示参与 PowerShell 文档撰写时应记住的指导规则：

- 请**勿**向我们提出大量拉取请求。 相反，提出问题并发起讨论，在我们认同这一方向后你再投入大量的时间。
- 请务必按以下说明及[代码](powershell-style-code.md)与[引用](powershell-style-reference.md)风格指南操作  。
- 请**务必**使用[模板](powershell-style-basic-markdown.md)文件，作为工作的出发点。
- 处理文章前，请**务必**在分支上创建单独的分支。
- 请**务必**遵循 [GitHub 流工作流](../how-to-write-workflows-major.md)。
- 请**务必**频繁发布有关参与的博客和推文（或者诸如此类）！

遵循这些指南可确保你和我们都能获得更好的体验。

## <a name="make-a-contribution-to-powershell-docs"></a>参与 PowerShell 文档撰写

可从现有[问题](https://github.com/MicrosoftDocs/PowerShell-Docs/issues/new/choose)中进行选择。
根据你的兴趣和承诺级别，工作量分为以下类别：

- **小更改**。 对于小更改，请在参与者指南的[主页](../index.md#quick-edits-to-existing-documents)中查看在 GitHub 中编辑的说明。 小更改包括：

  - 修复各种拼写错误
  - 改进语法或格式
  - 次要技术或事实编辑

- **维护**。 此类别包括相当简单的参与，例如，修复断裂或错误的链接，添加缺少的代码示例或解决受限内容问题。 在某些情况下，这些问题可能涉及大量文件。 届时，你应在开始前告知我们想要处理的内容。 在问题上添加注释，以告知我们你正在处理。

- **内容更新**。 鉴于文档集的巨大性，内容很容易过时，需要修订。 此外，出于各种原因，部分内容发生重复，甚至出现一式三份现象。 更新内容涉及确保各个主题为最新，或修订特色区域中的内容以消除重复，以及确保所有独特的内容均保存在较小文档集中。

- **新内容创作**。 如果有兴趣创作自己的主题，这些问题列出了我们要向文档集添加的主题。 不过，请在处理某主题前，告知我们。 如果有兴趣编写此处未列出的主题，请创建一个问题。

选择要处理的任务后，请按照[入门](../get-started-setup-github.md)指南操作，创建 GitHub 帐户并设置环境。

### <a name="making-large-changes"></a>进行大更改

**步骤 1：** 如果想要编写新内容或彻底修订现有内容，请创建描述你想做的事情的问题。

**步骤 2：** 对 `MicrosoftDocs/PowerShell-Docs` 存储库创建分支，并为所做的更改创建工作分支。

**步骤 3：** 在此新分支上进行更改。

如果是一个新的主题，请使用[风格指南](powershell-style-basic-markdown.md)中的模板作为起点。 风格指南包含编写准则，并且解释了每篇文章需要的元数据。

导航到对应针对步骤 1 中的文章确定的目录位置的文件夹。
该文件夹包含针对该部分中所有文章的 Markdown 文件。 如有必要，新建一个文件夹，放置存储内容的文件。 该部分的主要文章称为 index.md  。
对于映像和其他静态资源，请在包含文章的文件夹中创建称为“media”的子文件夹（如果尚不存在）  。 在“media”文件夹内，创建具有文章名称的子文件夹（索引文件除外）  。

请务必遵循适当的 Markdown 语法。 有关详细说明和示例，请参阅[风格指南](powershell-style-basic-markdown.md)。

**示例结构**

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

**步骤 4：** 从工作分支向暂存分支提交拉取请求 (PR)  。

通常，PR 一次只处理一个问题。 PR 可修改一个或多个文件。 如果要处理不同文件上的多个修复，首选单独的 PR。

如果 PR 可修复现有问题，请在提交消息或 PR 说明中添加 `Fixes #Issue_Number` 关键字。 如此，PR 合并时，问题将自动关闭。 有关详细信息，请参阅[通过提交消息关闭问题](https://help.github.com/articles/closing-issues-via-commit-messages/)。

PowerShell 团队会评审 PR，并告知你是否需要进行其他任何更改以获得批准。

**步骤 5：** 与团队讨论时，对分支进行任何必需的更新。

PR 获得批准后，维护人员会将 PR 合并到暂存分支中  。 我们会定期将所有提交从暂存分支推送到生效分支   。 撰写内容生效后，可在 [PowerShell 文档网站](https://docs.microsoft.com/PowerShell/)中查看。 通常，我们会在一个工作周内发布两到三次。

## <a name="contributor-license-agreement"></a>参与者许可协议

在合并 PR 前，必须先签署[参与撰写许可协议 (CLA)](https://cla.opensource.microsoft.com/MicrosoftDocs/PowerShell-Docs)。 每次参与撰写我们的文档时，都需要签署。

无需提前签署协议。 可以照常克隆 PR、创建 PR 分支或提交 PR。
创建 PR 时，由 CLA 机器人进行分类。 如果更改较小（例如，修复拼写错误），则 PR 将标记为 `cla-not-required`。 否则，它将被分类为 `cla-required`。 签署 CLA 后，当前和将来的所有拉取请求都将被标记为 `cla-signed`。
