---
title: 主要或持续更改的 GitHub 参与工作流
description: 本文介绍如何使用“主要”参与者工作流参与 docs.microsoft.com 文章的供稿。
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
ms.date: 08/30/2017
ms.openlocfilehash: 5231b68f04caa94d3ff2ff26afc38e3218ca06b8
ms.sourcegitcommit: 804a99b89785e5c8f056a9da3f0fbde9f0a56a51
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/05/2020
ms.locfileid: "78331897"
---
# <a name="github-contribution-workflow-for-major-or-long-running-changes"></a>主要或持续更改的 GitHub 参与工作流

> [!IMPORTANT]
> 发布到 docs.microsoft.com 的所有存储库均遵循 [Microsoft 开放源代码行为准则](https://opensource.microsoft.com/codeofconduct/)或 [.NET 基础行为准则](https://dotnetfoundation.org/code-of-conduct)。 有关详细信息，请参阅[行为准则常见问题解答](https://opensource.microsoft.com/codeofconduct/faq/)。 或如有任何疑问或意见，请联系 [opencode@microsoft.com](mailto:opencode@microsoft.com) 或 [conduct@dotnetfoundation.org](mailto:conduct@dotnetfoundation.org)。<br>
>
> [docs.microsoft.com 使用条款](https://docs.microsoft.com/legal/termsofuse)适用于对公共存储库中文档和代码示例所做的小修订和澄清。 如果你不是 Microsoft 的员工，那么新更改或重大更改会在拉取请求中生成一条注释，要求提交一份在线参与许可协议 (CLA)。 在合并拉取请求之前，你需要填写这份在线表单。

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

回顾 [Git 和 GitHub 基础知识](git-github-fundamentals.md#git)，Git 存储库包含一个主分支，以及未集成到主分支的任何正在工作的额外分支。 每当要引入一组在逻辑上有关联的更改时，最佳做法是创建一个工作分支，用于通过工作流来管理更改  。 这里之所以将其称为工作分支，是因为它是一个会不断迭代/优化更改直至其可集成回主分支的工作空间。

将相关的更改隔离到特定的分支中，可以使你独立地控制和引入这些更改，并将它们定向到发布周期中的特定发布时间。 实际上，根据所执行的工作类型，你可以很容易地实现在存储库中使用多个工作分支。 同时使用多个分支很常见，每一项工作都代表一个不同的项目。

>[!TIP]
>在主分支中进行更改并不是最佳做法  。 想象一下，如果你使用主分支为定时功能发布引入一组更改。 你已完成更改，并等待发布更改。 然后，在过渡期间，你收到一个需要修复某些内容的紧急请求，因此你将在主分支中更改一个文件，然后发布该更改。 在本示例中，你可能无意中发布了修正和更改，而这些内容本应在特定日期发布  。

现在，让我们在本地存储库中创建一个新的工作分支，以获取你所建议的更改。 如果已设置 Git Bash（请参阅[安装内容创作工具](get-started-setup-tools.md)），则可以创建新的分支，并使用一个命令从克隆的存储库中“签出”该分支：

````
git checkout -b "branchname"
````

每个 Git 客户端都不同，因此有关首选客户端，请咨询帮助。 你可以在 [GitHub 流](https://guides.github.com/introduction/flow/)上的 GitHub 指南中查看过程概览。

## <a name="making-your-changes"></a>执行更改

获得了 Microsoft 存储库的副本（“克隆”）并创建了分支后，现在即可随时使用任何文本或 Markdown 编辑器执行可能对社区有益的任何更改（如[安装内容创作工具](get-started-setup-tools.md)页面所述）。  可以在本地保存更改，而无需将更改提交到 Microsoft，准备就绪后再提交即可。

## <a name="saving-changes-to-your-repository"></a>将更改保存到存储库

向作者发送更改之前，必须先将更改保存到 Github 存储库。  同样，尽管所有工具都是不同的，但如果使用的是 Git Bash 命令行，则只需几个简单步骤即可完成此操作。

首先，在存储库中，需要暂存所有要提交的更改  。  可以通过执行以下命令完成此操作：

````
git add --all
````

接下来，需要将保存的更改提交到本地存储库。  可以通过运行以下命令在 Git Bash 中完成此操作：

````
git commit -m "Short Description of Changes Made"
````

最后，由于此分支在本地计算机上创建，因此需要使 GitHub.com 帐户中的分支知道此分支的存在。  如果使用的是 Git Bash，可通过运行以下命令完成此操作：

````
git push --set-upstream origin <branchname>
````

大功告成！  你的代码现在将在 GitHub 存储库中，并可用于创建拉取请求。  

>[!TIP]
> 尽管更改在推送后即会在个人 GitHub 帐户中可见，但不需要立即提交拉取请求。  如果想要停止并稍后返回进行其他调整，这完全没问题！

需要修复已提交的内容？  没问题！  只需在同一分支中进行更改，然后重新提交并推送即可（无需对同一分支的后续推送设置上游服务器）。

需要执行更多与此分支无关的更改？  切换回主分支并使用 Git Bash 签出其他新分支，此过程非常简单，执行以下命令即可：

````
git checkout master
git checkout -b "branchname"
````

现已位于新分支中，你即将成为主要供稿人。

[!INCLUDE[contribute-how-to-write-workflows-pull-request-processing](includes/contribute-how-to-write-workflows-pull-request-processing.md)]

## <a name="next-steps"></a>后续步骤

就这么简单！ 你已完成参与 docs.microsoft.com 内容的供稿！

- 继续查看 [Markdown 引用](markdown-reference.md)一文，详细了解 Markdown 和 Markdown 扩展语法等主题。
