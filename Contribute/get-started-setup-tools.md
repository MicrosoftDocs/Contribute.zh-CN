---
title: 安装内容创作工具
description: 本文将介绍如何下载并安装用于 Git 和编辑标记文件所需的客户端工具。
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
author: jasonwhowell
ms.author: jasonh
ms.date: 04/30/2018
ms.openlocfilehash: 24d47c4e094c318be75a27dbaaec11d8ead94452
ms.sourcegitcommit: ca84e542b081e145052f38967e826f6ef25da1b2
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/12/2019
ms.locfileid: "72288549"
---
# <a name="install-content-authoring-tools"></a>安装内容创作工具

本文介绍以交互方式安装 Git 客户端工具和 Visual Studio Code 的相关步骤。
> [!div class="checklist"]
> * 安装 [Git](https://git-scm.com/)
> * 安装 [Visual Studio Code](https://code.visualstudio.com/)
> * 安装 [Docs 创作包](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack)

>[!IMPORTANT]
> 如果只对文章进行小的更改，则*不*需要完成本文中的步骤，可以直接继续进行[快速更改工作流](index.md#quick-edits-to-existing-documents)。
>
> 建议主要参与者完成这些步骤，以便你能够使用[主要/持续更改的工作流](how-to-write-workflows-major.md)。 即使具有针对主存储库的写入权限，也强烈建议（同时本指南假定）为存储库创建分支并克隆存储库  ，以便具有读/写权限在分支中存储建议的更改。

## <a name="install-git-client-tools"></a>安装 Git 客户端工具 

 为你的平台安装最新版本的[软件自由保护组织的 Git 客户端工具](https://git-scm.com/download/)。 

* [Git for Windows](https://git-scm.com/download/win)。 此安装包括 Git 版本控制系统，以及用于与本地 Git 存储库进行交互的命令行应用 Git Bash。
* Git for Mac 作为 Xcode 命令行工具的一部分提供。 只需从命令行运行 `git`。 系统将提示你安装命令行工具（如有必要）。 你也可以从软件自由保护组织中下载 [Git for Mac](https://git-scm.com/download/mac)。
* [Git for Linux 和 Git for Unix](https://git-scm.com/download/linux)

如果希望使用图形用户界面 (GUI) 而不是命令行界面 (CLI)，请参阅[软件自由保护组织提供的 GUI 客户端页面](https://git-scm.com/downloads/guis)、[GitHub 的 GitHub Desktop](https://desktop.github.com/) 或 [Visual Studio Code](https://www.visualstudio.com/products/code-vs.aspx)，获取一些热门选择。

按照说明，对选定的客户端进行安装和配置。

在下一篇文章中，你将[设置本地 Git 存储库](get-started-setup-local.md)。

   其他 Git 资源可在此处找到：[Git terminology](https://help.github.com/articles/github-glossary)（Git 术语） | [Git 基本信息](https://git-scm.com/book/en/v2/Getting-Started-Git-Basics) | [了解 Git 和 GitHub](https://help.github.com/articles/good-resources-for-learning-git-and-github/)

## <a name="understand-markdown-editors"></a>了解 Markdown 编辑器

Markdown 是一种轻量级标记语言，既易于阅读也易于理解。 因此，Markdown 已迅速成为行业标准。 要在 Markdown 中撰写文章，建议首先下载并安装 Markdown 编辑器。  [Visual Studio Code](https://code.visualstudio.com/) 是用于在 Microsoft 中编辑 Markdown 的首选工具。 [Atom](https://atom.io) 是另一个用于编辑 Markdown 的常用工具。

Markdown 文本将保存为扩展名为 .md 的文件。

有关如何使用 Markdown 进行编写的其他详细信息（包括 Markdown 基础知识和 Open Publishing Services (OPS) 自定义 Markdown 扩展支持的功能），请参阅[如何使用 Markdown 撰写文档](how-to-write-use-markdown.md)和 [OPS 的 Markdown 引用](markdown-reference.md)文章。

## <a name="visual-studio-code"></a>Visual Studio Code

[Visual Studio Code](https://code.visualstudio.com/) 也称为 VS Code，是一种轻型编辑器，适用于 Windows、Linux 和 Mac。 它包括 Git 集成和扩展支持。

下载并安装 [VS Code](https://code.visualstudio.com/)。 VS Code 主页应正确检测操作系统。

- [Windows](https://code.visualstudio.com/docs/setup/windows)
- [Mac](https://code.visualstudio.com/docs/setup/mac)
- [Linux](https://code.visualstudio.com/docs/setup/linux)

> [!TIP]
> 若要启动 VS Code 和打开当前文件夹，请运行命令行中的 `code .` 命令或 bash shell。 如果当前文件夹是本地 Git 存储库的一部分，GitHub 集成将在 Visual Studio Code 中自动显示。

## <a name="docs-authoring-pack"></a>Docs 创作包
安装 Visual Studio Code Docs 创作包。 这组扩展包括在编写 Markdown 时提供帮助的基本创作协助，以及一个预览功能，方便用户看到 docs.microsoft.com 网站风格的 Markdown 外观。

   访问此[市场页](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack)，并选择“安装”  ，或者在 VS Code 窗口的扩展列表中搜索 `docsmsft.docs-authoring-pack`。 

   可以通过在 VS Code 中按 Alt+M 键来访问 Docs 创作包。 工具栏默认隐藏，但可以显示。 编辑 VS Code 设置（Ctrl+逗号），并添加用户设置 `"markdown.showToolbar": true` 来显示工具栏。

   有关详细信息，请参阅 [Docs 创作包](how-to-write-docs-auth-pack.md)页面。


## <a name="next-steps"></a>后续步骤

现在可以开始[设置本地 Git 存储库](get-started-setup-local.md)了。
