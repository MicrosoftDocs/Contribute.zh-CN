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
# <a name="install-content-authoring-tools"></a><span data-ttu-id="9d33b-103">安装内容创作工具</span><span class="sxs-lookup"><span data-stu-id="9d33b-103">Install content authoring tools</span></span>

<span data-ttu-id="9d33b-104">本文介绍以交互方式安装 Git 客户端工具和 Visual Studio Code 的相关步骤。</span><span class="sxs-lookup"><span data-stu-id="9d33b-104">This article describes the steps to interactively install Git client tools and Visual Studio Code.</span></span>
> [!div class="checklist"]
> * <span data-ttu-id="9d33b-105">安装 [Git for Windows](https://git-scm.com/download/win)</span><span class="sxs-lookup"><span data-stu-id="9d33b-105">Install [Git for Windows](https://git-scm.com/download/win)</span></span>
> * <span data-ttu-id="9d33b-106">安装 [Visual Studio Code](https://code.visualstudio.com/)</span><span class="sxs-lookup"><span data-stu-id="9d33b-106">Install [Visual Studio Code](https://code.visualstudio.com/)</span></span>

>[!IMPORTANT]
> <span data-ttu-id="9d33b-107">如果只对文章进行次要更改，则不需要完成本文中的步骤，可以直接继续完成[次要/间歇更改工作流](light-workflow.md)。</span><span class="sxs-lookup"><span data-stu-id="9d33b-107">If you're making only minor changes to an article, you *do not* need to complete the steps in this article and can continue directly to the [minor/infrequent changes workflow](light-workflow.md).</span></span>
>
> <span data-ttu-id="9d33b-108">建议主要参与者完成这些步骤，以便你能够使用[主要/持续更改的工作流](full-workflow.md)。</span><span class="sxs-lookup"><span data-stu-id="9d33b-108">Major contributors are encouraged to complete these steps, which enable you to use the [major/long-running changes workflow](full-workflow.md).</span></span> <span data-ttu-id="9d33b-109">即使具有针对主存储库的写入权限，也强烈建议（同时本指南假定）为存储库创建分支并克隆存储库，以便具有读/写权限在分支中存储建议的更改。</span><span class="sxs-lookup"><span data-stu-id="9d33b-109">Even if you have write permissions in the main repository, *we highly recommend (and this guide assumes) that you fork and clone the repository*, so that you have read/write permissions to store your proposed changes in your fork.</span></span>

## <a name="install-git-client-tools-on-windows"></a><span data-ttu-id="9d33b-110">在 Windows 上安装 Git 客户端工具</span><span class="sxs-lookup"><span data-stu-id="9d33b-110">Install Git client tools on Windows</span></span>

 <span data-ttu-id="9d33b-111">安装最新版本的[软件自由保护组织的 Git 客户端工具](https://git-scm.com/download/)。</span><span class="sxs-lookup"><span data-stu-id="9d33b-111">Install the latest version of [Software Freedom Conservancy's Git client tools](https://git-scm.com/download/).</span></span> <span data-ttu-id="9d33b-112">安装包括 Git 版本控制系统，以及用于与本地 Git 存储库进行交互的命令行应用 Git Bash。</span><span class="sxs-lookup"><span data-stu-id="9d33b-112">The install includes the Git version control system and Git Bash, the command-line app that you use to interact with your local Git repository.</span></span>

<span data-ttu-id="9d33b-113">如果希望使用图形用户界面 (GUI) 而不是命令行界面 (CLI)，请参阅[软件自由保护组织提供的 GUI 客户端页面](https://git-scm.com/downloads/guis)、[GitHub 的 GitHub Desktop](https://desktop.github.com/) 或 [Visual Studio Code](https://www.visualstudio.com/products/code-vs.aspx)，获取一些热门选择。</span><span class="sxs-lookup"><span data-stu-id="9d33b-113">If you prefer a graphical user interface (GUI) over a command-line interface (CLI), see [Software Freedom Conservancy's available GUI Clients page](https://git-scm.com/downloads/guis), [GitHub's GitHub Desktop](https://desktop.github.com/), or [Visual Studio Code](https://www.visualstudio.com/products/code-vs.aspx) for some popular options.</span></span>

<span data-ttu-id="9d33b-114">按照说明，对选定的客户端进行安装和配置。</span><span class="sxs-lookup"><span data-stu-id="9d33b-114">Follow the instructions for your chosen client for installation and configuration.</span></span>

<span data-ttu-id="9d33b-115">在下一篇文章中，你将[设置本地 Git 存储库](get-started-setup-local.md)。</span><span class="sxs-lookup"><span data-stu-id="9d33b-115">In the next article, you will [Set up a local Git repository](get-started-setup-local.md).</span></span>

   <span data-ttu-id="9d33b-116">下面提供了更多的 Git 资源：[Git 术语](https://help.github.com/articles/github-glossary) | [Git 基础知识](https://git-scm.com/book/en/v2/Getting-Started-Git-Basics) | [学习 Git 和 GitHub](https://help.github.com/articles/good-resources-for-learning-git-and-github/)</span><span class="sxs-lookup"><span data-stu-id="9d33b-116">Additional Git resources are available here: [Git terminology](https://help.github.com/articles/github-glossary) | [Git basics](https://git-scm.com/book/en/v2/Getting-Started-Git-Basics) | [Learning Git and GitHub](https://help.github.com/articles/good-resources-for-learning-git-and-github/)</span></span>

## <a name="understand-markdown-editors"></a><span data-ttu-id="9d33b-117">了解 Markdown 编辑器</span><span class="sxs-lookup"><span data-stu-id="9d33b-117">Understand Markdown editors</span></span>

<span data-ttu-id="9d33b-118">Markdown 是一种轻量级标记语言，既易于阅读也易于理解。</span><span class="sxs-lookup"><span data-stu-id="9d33b-118">Markdown is a lightweight markup language that is both easy to read and easy to learn.</span></span> <span data-ttu-id="9d33b-119">因此，Markdown 已迅速成为行业标准。</span><span class="sxs-lookup"><span data-stu-id="9d33b-119">Therefore, it has rapidly become an industry standard.</span></span> <span data-ttu-id="9d33b-120">要在 Markdown 中撰写文章，建议首先下载并安装 Markdown 编辑器。</span><span class="sxs-lookup"><span data-stu-id="9d33b-120">To write articles in Markdown, we recommend that you first download and install a Markdown editor.</span></span>  <span data-ttu-id="9d33b-121">[Visual Studio Code](https://code.visualstudio.com/) 是用于在 Microsoft 中编辑 Markdown 的首选工具。</span><span class="sxs-lookup"><span data-stu-id="9d33b-121">[Visual Studio Code](https://code.visualstudio.com/) is the preferred tool for editing Markdown at Microsoft.</span></span> <span data-ttu-id="9d33b-122">[Atom](https://atom.io) 是另一个用于编辑 Markdown 的常用工具。</span><span class="sxs-lookup"><span data-stu-id="9d33b-122">[Atom](https://atom.io) is another popular tool for editing Markdown.</span></span>

<span data-ttu-id="9d33b-123">Markdown 文本将保存为扩展名为 .md 的文件。</span><span class="sxs-lookup"><span data-stu-id="9d33b-123">Markdown text is saved into files with .md extension.</span></span>

<span data-ttu-id="9d33b-124">有关如何使用 Markdown 进行编写的其他详细信息（包括 Markdown 基础知识和 OPS 自定义 Markdown 扩展支持的功能），稍后在[如何使用 Markdown](how-to-write-use-markdown.md) 一文中有所介绍。</span><span class="sxs-lookup"><span data-stu-id="9d33b-124">Additional details on how to write with Markdown, including Markdown basics and the features supported by OPS custom Markdown extensions, are covered later in the [How to use Markdown](how-to-write-use-markdown.md) article.</span></span>

## <a name="visual-studio-code"></a><span data-ttu-id="9d33b-125">Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="9d33b-125">Visual Studio Code</span></span>

<span data-ttu-id="9d33b-126">[Visual Studio Code](https://code.visualstudio.com/) 也称为 VS Code，是一种轻型编辑器，适用于 Windows、Linux 和 Mac。</span><span class="sxs-lookup"><span data-stu-id="9d33b-126">[Visual Studio Code](https://code.visualstudio.com/), also known as VS Code, is a lightweight editor that works on Windows, Linux, and Mac.</span></span> <span data-ttu-id="9d33b-127">它包括 Git 集成和扩展支持。</span><span class="sxs-lookup"><span data-stu-id="9d33b-127">It includes git integration, and support for extensions.</span></span>

<span data-ttu-id="9d33b-128">下载并安装 [VS Code](https://code.visualstudio.com/)。</span><span class="sxs-lookup"><span data-stu-id="9d33b-128">Download and install [VS Code](https://code.visualstudio.com/).</span></span> <span data-ttu-id="9d33b-129">VS Code 主页应正确检测操作系统。</span><span class="sxs-lookup"><span data-stu-id="9d33b-129">The VS Code home page should detect your operating system correctly.</span></span>

- [<span data-ttu-id="9d33b-130">Windows</span><span class="sxs-lookup"><span data-stu-id="9d33b-130">Windows</span></span>](https://code.visualstudio.com/docs/setup/windows)
- [<span data-ttu-id="9d33b-131">Mac</span><span class="sxs-lookup"><span data-stu-id="9d33b-131">Mac</span></span>](https://code.visualstudio.com/docs/setup/mac)
- [<span data-ttu-id="9d33b-132">Linux</span><span class="sxs-lookup"><span data-stu-id="9d33b-132">Linux</span></span>](https://code.visualstudio.com/docs/setup/linux)

> [!TIP]
> <span data-ttu-id="9d33b-133">若要启动 VS Code 和打开当前文件夹，请运行命令行中的 `code .` 命令或 bash shell。</span><span class="sxs-lookup"><span data-stu-id="9d33b-133">To launch VS Code and open the current folder, run the command `code .` in the command line or bash shell.</span></span> <span data-ttu-id="9d33b-134">如果当前文件夹是本地 Git 存储库的一部分，github 集成将在 Visual Studio Code 中自动显示。</span><span class="sxs-lookup"><span data-stu-id="9d33b-134">If the current folder is part of a local git repo, the github integration appears in Visual Studio Code automatically.</span></span>

## <a name="next-steps"></a><span data-ttu-id="9d33b-135">后续步骤</span><span class="sxs-lookup"><span data-stu-id="9d33b-135">Next steps</span></span>

<span data-ttu-id="9d33b-136">现在可以开始[设置本地 Git 存储库](get-started-setup-local.md)了。</span><span class="sxs-lookup"><span data-stu-id="9d33b-136">Now you are ready to [Set up a local Git repository](get-started-setup-local.md).</span></span>
