---
title: 安装内容创作工具
description: 本文将介绍如何下载并安装用于 Git 和编辑标记文件所需的客户端工具。
author: bryanla
ms.author: bryanla
manager: mbaldwin
ms.date: 01/04/2018
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.custom: external-contributor-guide
ms.openlocfilehash: 62c4b234f23b470ffea33cacdfc469fbd7e526bd
ms.sourcegitcommit: dd1b4e915f4996ac029d2a0704ced785438d3484
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/23/2018
---
# <a name="install-content-authoring-tools"></a>安装内容创作工具

本文介绍以交互方式安装 Git 客户端工具和 Visual Studio Code 的相关步骤。
> [!div class="checklist"]
> * 安装 [Git for Windows](https://git-scm.com/download/win)
> * 安装 [Visual Studio Code](https://code.visualstudio.com/)

>[!IMPORTANT]
> 如果只对文章进行次要更改，则不需要完成本文中的步骤，可以直接继续完成[次要/间歇更改工作流](light-workflow.md)。
>
> 建议主要参与者完成这些步骤，以便你能够使用[主要/持续更改的工作流](full-workflow.md)。 即使具有针对主存储库的写入权限，也强烈建议（同时本指南假定）为存储库创建分支并克隆存储库，以便具有读/写权限在分支中存储建议的更改。

## <a name="install-git-client-tools-on-windows"></a>在 Windows 上安装 Git 客户端工具

 安装最新版本的[软件自由保护组织的 Git 客户端工具](https://git-scm.com/download/)。 安装包括 Git 版本控制系统，以及用于与本地 Git 存储库进行交互的命令行应用 Git Bash。

如果希望使用图形用户界面 (GUI) 而不是命令行界面 (CLI)，请参阅[软件自由保护组织提供的 GUI 客户端页面](https://git-scm.com/downloads/guis)、[GitHub 的 GitHub Desktop](https://desktop.github.com/) 或 [Visual Studio Code](https://www.visualstudio.com/products/code-vs.aspx)，获取一些热门选择。

按照说明，对选定的客户端进行安装和配置。

在下一篇文章中，你将[设置本地 Git 存储库](get-started-setup-local.md)。

   下面提供了更多的 Git 资源：[Git 术语](https://help.github.com/articles/github-glossary) | [Git 基础知识](https://git-scm.com/book/en/v2/Getting-Started-Git-Basics) | [学习 Git 和 GitHub](https://help.github.com/articles/good-resources-for-learning-git-and-github/)

## <a name="understand-markdown-editors"></a>了解 Markdown 编辑器

Markdown 是一种轻量级标记语言，既易于阅读也易于理解。 因此，Markdown 已迅速成为行业标准。 要在 Markdown 中撰写文章，建议首先下载并安装 Markdown 编辑器。  [Visual Studio Code](https://code.visualstudio.com/) 是用于在 Microsoft 中编辑 Markdown 的首选工具。 [Atom](https://atom.io) 是另一个用于编辑 Markdown 的常用工具。

Markdown 文本将保存为扩展名为 .md 的文件。

有关如何使用 Markdown 进行编写的其他详细信息（包括 Markdown 基础知识和 OPS 自定义 Markdown 扩展支持的功能），稍后在[如何使用 Markdown](how-to-write-use-markdown.md) 一文中有所介绍。

## <a name="visual-studio-code"></a>Visual Studio Code

[Visual Studio Code](https://code.visualstudio.com/) 也称为 VS Code，是一种轻型编辑器，适用于 Windows、Linux 和 Mac。 它包括 Git 集成和扩展支持。

下载并安装 [VS Code](https://code.visualstudio.com/)。 VS Code 主页应正确检测操作系统。

- [Windows](https://code.visualstudio.com/docs/setup/windows)
- [Mac](https://code.visualstudio.com/docs/setup/mac)
- [Linux](https://code.visualstudio.com/docs/setup/linux)

> [!TIP]
> 若要启动 VS Code 和打开当前文件夹，请运行命令行中的 `code .` 命令或 bash shell。 如果当前文件夹是本地 Git 存储库的一部分，github 集成将在 Visual Studio Code 中自动显示。

## <a name="next-steps"></a>后续步骤

现在可以开始[设置本地 Git 存储库](get-started-setup-local.md)了。
