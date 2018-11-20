---
title: 主要或持续更改的 GitHub 参与工作流
description: 本文介绍如何使用“主要”参与者工作流参与 docs.microsoft.com 文章的供稿。
ms.date: 08/30/2017
ms.openlocfilehash: 93e659df4f72c6a272d15fd7487eb3a997bdf3c8
ms.sourcegitcommit: 44eb4f5ee65c1848d7f36fca107b296eb7687397
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/13/2018
ms.locfileid: "51609382"
---
# <a name="github-contribution-workflow-for-major-or-long-running-changes"></a>主要或持续更改的 GitHub 参与工作流

> [!IMPORTANT]
> 发布到 docs.microsoft.com 的所有存储库均遵循 [Microsoft 开放源代码行为准则](https://opensource.microsoft.com/codeofconduct/)或 [.NET 基础行为准则](https://dotnetfoundation.org/code-of-conduct)。 有关详细信息，请参阅[行为准则常见问题解答](https://opensource.microsoft.com/codeofconduct/faq/)。 或如有任何疑问或意见，请联系 [opencode@microsoft.com](mailto:opencode@microsoft.com) 或 [conduct@dotnetfoundation.org](mailto:conduct@dotnetfoundation.org)。<br>
>
> [docs.microsoft.com 使用条款](https://docs.microsoft.com/legal/termsofuse)涵盖公共存储库中对文档和代码示例所做的轻微更正和澄清。 如果你不是 Microsoft 的员工，那么新更改或重大更改会在拉取请求中生成一条注释，要求提交一份在线参与许可协议 (CLA)。 在合并拉取请求之前，你需要填写这份在线表单。

## <a name="overview"></a>概述

此工作流适合需要进行主要更改的参与者，或者是向存储库频繁供稿的参与者。 频繁供稿的参与者通常会执行不断进行的（即持续）更改（这些更改经过多个构建/验证/暂存周期或跨越多天），然后进行拉取请求签核和合并。

这些类型的参与示例包括：

[!INCLUDE[contribute-major-changes-change-definition](includes/contribute-how-to-write-workflows-major-change-definition.md)]

### <a name="terminology"></a>术语

在开始之前，让我们回顾一下在此工作流中使用的 Git/GitHub 术语和名字对象。 不用着急去熟悉它。 只要知道你将对此有所了解，并且在需要验证某个定义时，可以回顾参考本节。

| 名称 | 说明 |
|-----------|-------------|
|分支|在表示主 GitHub 存储库的副本时，通常用作名词。 实际上，分支只是另一个存储库。 但是，从某种意义上来说，GitHub 维护至主/父存储库的连接。 它有时用作动词，如“必须首先为存储库创建分支”。|
|远程|到远程存储库的命名连接，例如“源”或“上游”远程。 Git 称之为“远程源”，因为它们可用于引用托管在另一台计算机上的存储库。 在此工作流中，远程始终是一个 GitHub 存储库。|
|源|分配给本地存储库与在其中进行克隆的源存储库之间的连接的名称。 在此工作流中，源表示与分支的连接。 它有时用作源存储库本身的一个名字对象，如“请务必将更改推送到源”。|
|上游|与源远程一样，上游是与另一个存储库的命名连接。 在此工作流中，上游表示本地存储库与在其中创建分支的主存储库之间的连接。 它有时用作上游存储库本身的一个名字对象，如“请务必从上游拉取更改”。|

## <a name="workflow"></a>工作流

>[!IMPORTANT]
> 如果尚未完成这些步骤，则必须在[设置](get-started-setup-github.md)部分完成。 本节内容指导你完成设置 GitHub 帐户、安装 Git Bash 和 Markdown 编辑器、创建分支，并设置本地存储库。 如果你不熟悉 Git 和 GitHub 概念（如存储库或分支），请首先回顾一下 [Git 和 GitHub 基础知识](git-github-fundamentals.md)。

在此工作流中，更改在重复循环中传递。 从设备的本地存储库开始，它们会传递回 GitHub 分支，进入主 GitHub 存储库，然后在你合并其他参与者提供的更改时再次回到本地。

### <a name="use-github-flow"></a>使用 GitHub 流

回顾 [Git 和 GitHub 基础知识](git-github-fundamentals.md#git)，Git 存储库包含一个主分支，以及未集成到主分支的任何其他正在工作的分支。 每当你引入一组逻辑上关联的更改时，最佳做法是创建一个工作分支，以便通过工作流管理更改。 我们之所以将其称为工作分支，是因为它是一个用于迭代/优化更改的工作空间，直到它们可以被集成回主分支中。

将相关的更改隔离到特定的分支中，可以使你独立地控制和引入这些更改，并将它们定向到发布周期中的特定发布时间。 实际上，根据所执行的工作类型，你可以很容易地实现在存储库中使用多个工作分支。 同时使用多个分支很常见，每一项工作都代表一个不同的项目。

>[!TIP]
>在主分支中进行更改并不是最佳做法。 想象一下，如果你使用主分支为定时功能发布引入一组更改。 你已完成更改，并等待发布更改。 然后，在过渡期间，你收到一个需要修复某些内容的紧急请求，因此你将在主分支中更改一个文件，然后发布该更改。 在本示例中，你可能无意中发布了修正和更改，而这些内容本应在特定日期发布。

现在，让我们在本地存储库中创建一个新的工作分支，以获取你所建议的更改。 每个 Git 客户端都不同，因此有关首选客户端，请咨询帮助。 你可以在 [GitHub 流](https://guides.github.com/introduction/flow/)上的 GitHub 指南中查看过程概览。

[!INCLUDE[contribute-how-to-write-workflows-pull-request-processing](includes/contribute-how-to-write-workflows-pull-request-processing.md)]

## <a name="next-steps"></a>后续步骤

就这么简单！ 你已完成参与 docs.microsoft.com 内容的供稿！

- 继续查看撰写要领部分，了解特定主题（如 Markdown 和 Markdown 扩展语法等）的详细信息。
