---
title: 从 Jupyter 笔记本获取内容 - Docs 创作包
description: 了解如何使用 Docs 创作包（Visual Studio Code 扩展）将 Jupyter 笔记本中的内容插入并更新到你的文档中。
author: sdgilley
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.date: 01/19/2021
ms.author: sgilley
ms.openlocfilehash: c2b21d260c9e3bd90fbffed9a28afbebd76e2831
ms.sourcegitcommit: f174f438ad2cdb7f2acc5acc73bf5389074c44c5
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/26/2021
ms.locfileid: "98811964"
---
# <a name="insert-and-update-content-from-a-jupyter-notebook"></a><span data-ttu-id="688d1-103">从 Jupyter 笔记本插入并更新内容</span><span class="sxs-lookup"><span data-stu-id="688d1-103">Insert and update content from a Jupyter notebook</span></span>

[!INCLUDE [markdown-extension](includes/markdown-extension.md)]

> [!IMPORTANT]
> <span data-ttu-id="688d1-104">从 Jupyter 笔记本进行插入和更新的功能当前不适用于 Mac。</span><span class="sxs-lookup"><span data-stu-id="688d1-104">Insert and update from a Jupyter notebook functionality does not currently work on a Mac.</span></span>

## <a name="summary"></a><span data-ttu-id="688d1-105">总结</span><span class="sxs-lookup"><span data-stu-id="688d1-105">Summary</span></span>

<span data-ttu-id="688d1-106">Jupyter 笔记本是在 Python 领域创建和共享代码的标准交互方式。</span><span class="sxs-lookup"><span data-stu-id="688d1-106">Jupyter Notebooks are a standard interactive way of creating and sharing code in the Python world.</span></span>  <span data-ttu-id="688d1-107">笔记本包含 Python 代码、Markdown 和（可选）代码输出的组合。</span><span class="sxs-lookup"><span data-stu-id="688d1-107">The notebook contains a combination of Python code, markdown, and optionally output from the code.</span></span>


<span data-ttu-id="688d1-108">Docs 创作包扩展包括将静态 Markdown 版本的 Jupyter 笔记本置于文档中的功能：</span><span class="sxs-lookup"><span data-stu-id="688d1-108">The Docs Authoring Pack extension includes functionality to put a static markdown version of a Jupyter notebook into your document:</span></span>

<span data-ttu-id="688d1-109">Docs:插入 Jupyter 笔记本：输入笔记本的 URL。</span><span class="sxs-lookup"><span data-stu-id="688d1-109">**Docs: Insert Jupyter notebook**: Enter the URL of the notebook.</span></span> <span data-ttu-id="688d1-110">Markdown 版本的笔记本将被添加到文档中光标所在的位置。</span><span class="sxs-lookup"><span data-stu-id="688d1-110">A markdown version of the notebook is added to the document at the position of your cursor.</span></span> <span data-ttu-id="688d1-111">请勿修改开始或结束标记；下一个函数将使用它来更新笔记本。</span><span class="sxs-lookup"><span data-stu-id="688d1-111">Do not modify the start or end tags; it's what the next function uses to update the notebook.</span></span>

<span data-ttu-id="688d1-112">Docs:更新 Jupyter 笔记本：此函数将在开始和结束之间使用最新版本替换之前插入的笔记本内容。</span><span class="sxs-lookup"><span data-stu-id="688d1-112">**Docs: Update Jupyter notebook**: This function will replace the previously inserted notebook content between start and end with the latest version.</span></span> <span data-ttu-id="688d1-113">不需要输入 URL，它就记录在开始标记中。</span><span class="sxs-lookup"><span data-stu-id="688d1-113">No need to enter the URL, it's recorded in the start tag.</span></span>  <span data-ttu-id="688d1-114">更新功能假设文档中只有一个笔记本。</span><span class="sxs-lookup"><span data-stu-id="688d1-114">Update functionality assumes there is a single notebook in the document.</span></span>  <span data-ttu-id="688d1-115">请勿将多个笔记本添加到一个文档中。</span><span class="sxs-lookup"><span data-stu-id="688d1-115">Don't add multiple notebooks to a single document.</span></span>

## <a name="in-action"></a><span data-ttu-id="688d1-116">操作过程</span><span class="sxs-lookup"><span data-stu-id="688d1-116">In action</span></span>

<span data-ttu-id="688d1-117">下面是此功能的简短演示。</span><span class="sxs-lookup"><span data-stu-id="688d1-117">Below is a brief demonstration of this feature.</span></span>

<span data-ttu-id="688d1-118">[![插入 Jupyter 笔记本](media/insertnotebook.gif)](media/insertnotebook.gif#lightbox)</span><span class="sxs-lookup"><span data-stu-id="688d1-118">[![Insert Jupyter notebook](media/insertnotebook.gif)](media/insertnotebook.gif#lightbox)</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="688d1-119">疑难解答</span><span class="sxs-lookup"><span data-stu-id="688d1-119">Troubleshooting</span></span>

> [!IMPORTANT]
> <span data-ttu-id="688d1-120">从 Jupyter 笔记本进行插入和更新的功能当前不适用于 Mac。</span><span class="sxs-lookup"><span data-stu-id="688d1-120">Insert and update from a Jupyter notebook functionality does not currently work on a Mac.</span></span>

<span data-ttu-id="688d1-121">这些函数需要在计算机上安装 Python、`jupyter`和 `nbconvert`。</span><span class="sxs-lookup"><span data-stu-id="688d1-121">These functions need Python, `jupyter`, and `nbconvert` installed on your machine.</span></span>

<span data-ttu-id="688d1-122">若要查看是否已安装 Python，请打开 VS Code 终端并运行以下命令：</span><span class="sxs-lookup"><span data-stu-id="688d1-122">To see if Python is installed, open a VS Code terminal and run:</span></span>

* <span data-ttu-id="688d1-123">Windows - `where python`。</span><span class="sxs-lookup"><span data-stu-id="688d1-123">Windows - `where python`</span></span>
* <span data-ttu-id="688d1-124">Linux/Mac - `which python`</span><span class="sxs-lookup"><span data-stu-id="688d1-124">Linux/Mac - `which python`</span></span>

<span data-ttu-id="688d1-125">如果返回的是一个或多个路径，则 Python 已安装。</span><span class="sxs-lookup"><span data-stu-id="688d1-125">If the return is one or more paths, Python is installed.</span></span>  <span data-ttu-id="688d1-126">否则，请立即[安装 Python](https://www.python.org/downloads/)。</span><span class="sxs-lookup"><span data-stu-id="688d1-126">If not, [install Python](https://www.python.org/downloads/) now.</span></span>

<span data-ttu-id="688d1-127">接下来，确保已安装 `jupyter`：</span><span class="sxs-lookup"><span data-stu-id="688d1-127">Next make sure `jupyter` is installed:</span></span>

* <span data-ttu-id="688d1-128">Windows - `where jupyter`。</span><span class="sxs-lookup"><span data-stu-id="688d1-128">Windows - `where jupyter`</span></span>
* <span data-ttu-id="688d1-129">Linux/Mac - `which jupyter`</span><span class="sxs-lookup"><span data-stu-id="688d1-129">Linux/Mac - `which jupyter`</span></span>

<span data-ttu-id="688d1-130">如果未返回路径，请安装 `jupyter`：</span><span class="sxs-lookup"><span data-stu-id="688d1-130">If a path is not returned, install `jupyter`:</span></span>

```bash
pip install --upgrade jupyter
```

<span data-ttu-id="688d1-131">在安装 Python 和 `jupyter` 后，请安装 `nbconvert`：</span><span class="sxs-lookup"><span data-stu-id="688d1-131">Once both Python and `jupyter` are installed, install `nbconvert`:</span></span>

```bash
pip install --upgrade nbconvert
```
