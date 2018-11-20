---
title: 安装内容创作工具
description: 本文将介绍如何下载并安装用于 Git 和编辑标记文件所需的客户端工具。
author: jasonwhowell
ms.author: jasonh
manager: kfile
ms.date: 04/30/2018
ms.openlocfilehash: 715634a9a2342311eb1d358cb8379f90a7074d80
ms.sourcegitcommit: 44eb4f5ee65c1848d7f36fca107b296eb7687397
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/13/2018
ms.locfileid: "51609375"
---
# <a name="install-content-authoring-tools"></a><span data-ttu-id="72eba-103">安装内容创作工具</span><span class="sxs-lookup"><span data-stu-id="72eba-103">Install content authoring tools</span></span>

<span data-ttu-id="72eba-104">本文介绍以交互方式安装 Git 客户端工具和 Visual Studio Code 的相关步骤。</span><span class="sxs-lookup"><span data-stu-id="72eba-104">This article describes the steps to interactively install Git client tools and Visual Studio Code.</span></span>
> [!div class="checklist"]
> * <span data-ttu-id="72eba-105">安装 [Git](https://git-scm.com/)</span><span class="sxs-lookup"><span data-stu-id="72eba-105">Install [Git](https://git-scm.com/)</span></span>
> * <span data-ttu-id="72eba-106">安装 [Visual Studio Code](https://code.visualstudio.com/)</span><span class="sxs-lookup"><span data-stu-id="72eba-106">Install [Visual Studio Code](https://code.visualstudio.com/)</span></span>
> * <span data-ttu-id="72eba-107">安装 [Docs 创作包](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack)</span><span class="sxs-lookup"><span data-stu-id="72eba-107">Install [Docs Authoring Pack](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack)</span></span>

>[!IMPORTANT]
> <span data-ttu-id="72eba-108">如果只对文章进行小的更改，则*不*需要完成本文中的步骤，可以直接继续进行[快速更改工作流](index.md#quick-edits-to-existing-documents)。</span><span class="sxs-lookup"><span data-stu-id="72eba-108">If you're making only minor changes to an article, you *do not* need to complete the steps in this article and can continue directly to the [quick changes workflow](index.md#quick-edits-to-existing-documents).</span></span>
>
> <span data-ttu-id="72eba-109">建议主要参与者完成这些步骤，以便你能够使用[主要/持续更改的工作流](how-to-write-workflows-major.md)。</span><span class="sxs-lookup"><span data-stu-id="72eba-109">Major contributors are encouraged to complete these steps, which enable you to use the [major/long-running changes workflow](how-to-write-workflows-major.md).</span></span> <span data-ttu-id="72eba-110">即使具有针对主存储库的写入权限，也强烈建议（同时本指南假定）为存储库创建分支并克隆存储库，以便具有读/写权限在分支中存储建议的更改。</span><span class="sxs-lookup"><span data-stu-id="72eba-110">Even if you have write permissions in the main repository, *we highly recommend (and this guide assumes) that you fork and clone the repository*, so that you have read/write permissions to store your proposed changes in your fork.</span></span>

## <a name="install-git-client-tools"></a><span data-ttu-id="72eba-111">安装 Git 客户端工具</span><span class="sxs-lookup"><span data-stu-id="72eba-111">Install Git client tools</span></span> 

 <span data-ttu-id="72eba-112">为你的平台安装最新版本的[软件自由保护组织的 Git 客户端工具](https://git-scm.com/download/)。</span><span class="sxs-lookup"><span data-stu-id="72eba-112">Install the latest version of [Software Freedom Conservancy's Git client tools](https://git-scm.com/download/) for your platform.</span></span> 

* <span data-ttu-id="72eba-113">[Git for Windows](https://git-scm.com/download/win)。</span><span class="sxs-lookup"><span data-stu-id="72eba-113">[Git for Windows](https://git-scm.com/download/win).</span></span> <span data-ttu-id="72eba-114">此安装包括 Git 版本控制系统，以及用于与本地 Git 存储库进行交互的命令行应用 Git Bash。</span><span class="sxs-lookup"><span data-stu-id="72eba-114">This install includes the Git version control system and Git Bash, the command-line app that you use to interact with your local Git repository.</span></span>
* <span data-ttu-id="72eba-115">Git for Mac 作为 Xcode 命令行工具的一部分提供。</span><span class="sxs-lookup"><span data-stu-id="72eba-115">Git for Mac is provided as part of the Xcode Command Line Tools.</span></span> <span data-ttu-id="72eba-116">只需从命令行运行 `git`。</span><span class="sxs-lookup"><span data-stu-id="72eba-116">Simply run `git` from the command line.</span></span> <span data-ttu-id="72eba-117">系统将提示你安装命令行工具（如有必要）。</span><span class="sxs-lookup"><span data-stu-id="72eba-117">You will be prompted to install the command line tools if needed.</span></span> <span data-ttu-id="72eba-118">你也可以从软件自由保护组织中下载 [Git for Mac](https://git-scm.com/download/mac)。</span><span class="sxs-lookup"><span data-stu-id="72eba-118">You can also download [Git for Mac](https://git-scm.com/download/mac) from the Software Freedom Conservancy.</span></span>
* [<span data-ttu-id="72eba-119">Git for Linux 和 Git for Unix</span><span class="sxs-lookup"><span data-stu-id="72eba-119">Git for Linux and Unix</span></span>](https://git-scm.com/download/linux)

<span data-ttu-id="72eba-120">如果希望使用图形用户界面 (GUI) 而不是命令行界面 (CLI)，请参阅[软件自由保护组织提供的 GUI 客户端页面](https://git-scm.com/downloads/guis)、[GitHub 的 GitHub Desktop](https://desktop.github.com/) 或 [Visual Studio Code](https://www.visualstudio.com/products/code-vs.aspx)，获取一些热门选择。</span><span class="sxs-lookup"><span data-stu-id="72eba-120">If you prefer a graphical user interface (GUI) over a command-line interface (CLI), see [Software Freedom Conservancy's available GUI Clients page](https://git-scm.com/downloads/guis), [GitHub's GitHub Desktop](https://desktop.github.com/), or [Visual Studio Code](https://www.visualstudio.com/products/code-vs.aspx) for some popular options.</span></span>

<span data-ttu-id="72eba-121">按照说明，对选定的客户端进行安装和配置。</span><span class="sxs-lookup"><span data-stu-id="72eba-121">Follow the instructions for your chosen client for installation and configuration.</span></span>

<span data-ttu-id="72eba-122">在下一篇文章中，你将[设置本地 Git 存储库](get-started-setup-local.md)。</span><span class="sxs-lookup"><span data-stu-id="72eba-122">In the next article, you will [Set up a local Git repository](get-started-setup-local.md).</span></span>

   <span data-ttu-id="72eba-123">下面提供了更多的 Git 资源：[Git 术语](https://help.github.com/articles/github-glossary) | [Git 基础知识](https://git-scm.com/book/en/v2/Getting-Started-Git-Basics) | [学习 Git 和 GitHub](https://help.github.com/articles/good-resources-for-learning-git-and-github/)</span><span class="sxs-lookup"><span data-stu-id="72eba-123">Additional Git resources are available here: [Git terminology](https://help.github.com/articles/github-glossary) | [Git basics](https://git-scm.com/book/en/v2/Getting-Started-Git-Basics) | [Learning Git and GitHub](https://help.github.com/articles/good-resources-for-learning-git-and-github/)</span></span>

## <a name="understand-markdown-editors"></a><span data-ttu-id="72eba-124">了解 Markdown 编辑器</span><span class="sxs-lookup"><span data-stu-id="72eba-124">Understand Markdown editors</span></span>

<span data-ttu-id="72eba-125">Markdown 是一种轻量级标记语言，既易于阅读也易于理解。</span><span class="sxs-lookup"><span data-stu-id="72eba-125">Markdown is a lightweight markup language that is both easy to read and easy to learn.</span></span> <span data-ttu-id="72eba-126">因此，Markdown 已迅速成为行业标准。</span><span class="sxs-lookup"><span data-stu-id="72eba-126">Therefore, it has rapidly become an industry standard.</span></span> <span data-ttu-id="72eba-127">要在 Markdown 中撰写文章，建议首先下载并安装 Markdown 编辑器。</span><span class="sxs-lookup"><span data-stu-id="72eba-127">To write articles in Markdown, we recommend that you first download and install a Markdown editor.</span></span>  <span data-ttu-id="72eba-128">[Visual Studio Code](https://code.visualstudio.com/) 是用于在 Microsoft 中编辑 Markdown 的首选工具。</span><span class="sxs-lookup"><span data-stu-id="72eba-128">[Visual Studio Code](https://code.visualstudio.com/) is the preferred tool for editing Markdown at Microsoft.</span></span> <span data-ttu-id="72eba-129">[Atom](https://atom.io) 是另一个用于编辑 Markdown 的常用工具。</span><span class="sxs-lookup"><span data-stu-id="72eba-129">[Atom](https://atom.io) is another popular tool for editing Markdown.</span></span>

<span data-ttu-id="72eba-130">Markdown 文本将保存为扩展名为 .md 的文件。</span><span class="sxs-lookup"><span data-stu-id="72eba-130">Markdown text is saved into files with .md extension.</span></span>

<span data-ttu-id="72eba-131">有关如何使用 Markdown 进行编写的其他详细信息（包括 Markdown 基础知识和 Open Publishing Services (OPS) 自定义 Markdown 扩展支持的功能），请参阅[如何使用 Markdown 撰写文档](how-to-write-use-markdown.md)和 [OPS 的 Markdown 引用](markdown-reference.md)文章。</span><span class="sxs-lookup"><span data-stu-id="72eba-131">Additional details on how to write with Markdown, including Markdown basics and the features supported by Open Publishing Services (OPS) custom Markdown extensions, are covered in the [How to use Markdown for writing Docs](how-to-write-use-markdown.md) and [Markdown Reference for OPS](markdown-reference.md) articles.</span></span>

## <a name="visual-studio-code"></a><span data-ttu-id="72eba-132">Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="72eba-132">Visual Studio Code</span></span>

<span data-ttu-id="72eba-133">[Visual Studio Code](https://code.visualstudio.com/) 也称为 VS Code，是一种轻型编辑器，适用于 Windows、Linux 和 Mac。</span><span class="sxs-lookup"><span data-stu-id="72eba-133">[Visual Studio Code](https://code.visualstudio.com/), also known as VS Code, is a lightweight editor that works on Windows, Linux, and Mac.</span></span> <span data-ttu-id="72eba-134">它包括 Git 集成和扩展支持。</span><span class="sxs-lookup"><span data-stu-id="72eba-134">It includes git integration, and support for extensions.</span></span>

<span data-ttu-id="72eba-135">下载并安装 [VS Code](https://code.visualstudio.com/)。</span><span class="sxs-lookup"><span data-stu-id="72eba-135">Download and install [VS Code](https://code.visualstudio.com/).</span></span> <span data-ttu-id="72eba-136">VS Code 主页应正确检测操作系统。</span><span class="sxs-lookup"><span data-stu-id="72eba-136">The VS Code home page should detect your operating system correctly.</span></span>

- [<span data-ttu-id="72eba-137">Windows</span><span class="sxs-lookup"><span data-stu-id="72eba-137">Windows</span></span>](https://code.visualstudio.com/docs/setup/windows)
- [<span data-ttu-id="72eba-138">Mac</span><span class="sxs-lookup"><span data-stu-id="72eba-138">Mac</span></span>](https://code.visualstudio.com/docs/setup/mac)
- [<span data-ttu-id="72eba-139">Linux</span><span class="sxs-lookup"><span data-stu-id="72eba-139">Linux</span></span>](https://code.visualstudio.com/docs/setup/linux)

> [!TIP]
> <span data-ttu-id="72eba-140">若要启动 VS Code 和打开当前文件夹，请运行命令行中的 `code .` 命令或 bash shell。</span><span class="sxs-lookup"><span data-stu-id="72eba-140">To launch VS Code and open the current folder, run the command `code .` in the command line or bash shell.</span></span> <span data-ttu-id="72eba-141">如果当前文件夹是本地 Git 存储库的一部分，GitHub 集成将在 Visual Studio Code 中自动显示。</span><span class="sxs-lookup"><span data-stu-id="72eba-141">If the current folder is part of a local git repo, the GitHub integration appears in Visual Studio Code automatically.</span></span>

## <a name="docs-authoring-pack"></a><span data-ttu-id="72eba-142">Docs 创作包</span><span class="sxs-lookup"><span data-stu-id="72eba-142">Docs Authoring Pack</span></span>
<span data-ttu-id="72eba-143">安装 Visual Studio Code Docs 创作包。</span><span class="sxs-lookup"><span data-stu-id="72eba-143">Install the Docs Authoring Pack for Visual Studio Code.</span></span> <span data-ttu-id="72eba-144">这组扩展包括在编写 Markdown 时提供帮助的基本创作协助，以及一个预览功能，方便用户看到 docs.microsoft.com 网站风格的 Markdown 外观。</span><span class="sxs-lookup"><span data-stu-id="72eba-144">This set of extensions includes basic authoring assistance for help when writing Markdown, and a preview feature, so that you can see what the Markdown looks like in the style of the docs.microsoft.com site.</span></span>

   <span data-ttu-id="72eba-145">访问此[市场页](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack)，并选择“安装”，或者在 VS Code 窗口的扩展列表中搜索 `docsmsft.docs-authoring-pack`。</span><span class="sxs-lookup"><span data-stu-id="72eba-145">Visit this [marketplace page](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack) and select **Install**, or search for `docsmsft.docs-authoring-pack` in your extensions list in the VS Code window.</span></span> 

   <span data-ttu-id="72eba-146">可以通过在 VS Code 中按 Alt+M 键来访问 Docs 创作包。</span><span class="sxs-lookup"><span data-stu-id="72eba-146">The Docs Authoring Pack is accessible by pressing Alt+M inside of VS Code.</span></span> <span data-ttu-id="72eba-147">工具栏默认隐藏，但可以显示。</span><span class="sxs-lookup"><span data-stu-id="72eba-147">The toolbar is hidden by default but can be shown.</span></span> <span data-ttu-id="72eba-148">编辑 VS Code 设置（Ctrl+逗号），并添加用户设置 `"markdown.showToolbar": true` 来显示工具栏。</span><span class="sxs-lookup"><span data-stu-id="72eba-148">Edit the VS Code settings (Control+comma) and adding user setting `"markdown.showToolbar": true` to show the toolbar.</span></span>

   <span data-ttu-id="72eba-149">有关详细信息，请参阅 [Docs 创作包](how-to-write-docs-auth-pack.md)页面。</span><span class="sxs-lookup"><span data-stu-id="72eba-149">For more information, see the [Docs Authoring Pack](how-to-write-docs-auth-pack.md) page.</span></span>


## <a name="next-steps"></a><span data-ttu-id="72eba-150">后续步骤</span><span class="sxs-lookup"><span data-stu-id="72eba-150">Next steps</span></span>

<span data-ttu-id="72eba-151">现在可以开始[设置本地 Git 存储库](get-started-setup-local.md)了。</span><span class="sxs-lookup"><span data-stu-id="72eba-151">Now you are ready to [Set up a local Git repository](get-started-setup-local.md).</span></span>
