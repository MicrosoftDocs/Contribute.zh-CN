---
title: 排序重定向 - Docs 创作包
description: 了解如何使用 Docs 创作包 Visual Studio Code 扩展排序重定向。
author: IEvangelist
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.date: 03/03/2020
ms.author: dapine
ms.openlocfilehash: 4924c631c8720743c283083e53b3a1e9af86b00a
ms.sourcegitcommit: cfba5ad25b898bfed76046126ce8ff4871910701
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/04/2020
ms.locfileid: "78336672"
---
# <a name="sort-redirects"></a><span data-ttu-id="c0a68-103">排序重定向</span><span class="sxs-lookup"><span data-stu-id="c0a68-103">Sort redirects</span></span>

[!INCLUDE [markdown-extension](includes/markdown-extension.md)]

## <a name="summary"></a><span data-ttu-id="c0a68-104">总结</span><span class="sxs-lookup"><span data-stu-id="c0a68-104">Summary</span></span>

<span data-ttu-id="c0a68-105">随着 docs.microsoft.com 文档集的变化，最终将删除一些 Markdown 文件。</span><span class="sxs-lookup"><span data-stu-id="c0a68-105">With the evolution of a docs.microsoft.com docset, some Markdown files eventually will be deleted.</span></span> <span data-ttu-id="c0a68-106">删除 Markdown 文件后，我们需要提供重定向，以便通过重定向正确解析对已删除文章的任何引用。</span><span class="sxs-lookup"><span data-stu-id="c0a68-106">When a Markdown file is deleted, we're required to provide a redirect so that any reference to the deleted article is properly resolved via the redirect.</span></span> <span data-ttu-id="c0a68-107">重定向在 .openpublishing.redirection.json 文件中指定。</span><span class="sxs-lookup"><span data-stu-id="c0a68-107">Redirections are specified in the *.openpublishing.redirection.json* file.</span></span>

1. <span data-ttu-id="c0a68-108">打开“命令面板”，按 <kbd>F1</kbd>（或 macOS 上的 <kbd>⇧⌘P</kbd>）</span><span class="sxs-lookup"><span data-stu-id="c0a68-108">Open the Command Palette, press <kbd>F1</kbd> (or <kbd>⇧⌘P</kbd> on macOS)</span></span>
1. <span data-ttu-id="c0a68-109">类型：Docs:对主重定向文件进行排序</span><span class="sxs-lookup"><span data-stu-id="c0a68-109">Type: **Docs: Sort master redirection file**</span></span>
1. <span data-ttu-id="c0a68-110">选择要执行的命令</span><span class="sxs-lookup"><span data-stu-id="c0a68-110">Select the command to execute it</span></span>
1. <span data-ttu-id="c0a68-111">查看对 .openpublishing.redirection.json 文件的更改</span><span class="sxs-lookup"><span data-stu-id="c0a68-111">Observe changes to *.openpublishing.redirection.json* file</span></span>

## <a name="considerations"></a><span data-ttu-id="c0a68-112">考虑事项</span><span class="sxs-lookup"><span data-stu-id="c0a68-112">Considerations</span></span>

<span data-ttu-id="c0a68-113">“菊花链”的概念与最初设计 .openpublishing.redirection.json 文件的方式相关。</span><span class="sxs-lookup"><span data-stu-id="c0a68-113">The concept of "daisy chaining" exists with how the *.openpublishing.redirection.json* file was originally designed.</span></span> <span data-ttu-id="c0a68-114">随着时间的推移，作为重定向添加的文件最终会过时。</span><span class="sxs-lookup"><span data-stu-id="c0a68-114">Over time, files added as a redirect will eventually become stale.</span></span> <span data-ttu-id="c0a68-115">这会出现在以下情况：删除文件 A 后需要重定向到文件 B，然后删除文件 B，再重定向到文件 C。理想情况下，两个条目都会指向 C - 因此 A 重定向到 C，而 B 保持不变。</span><span class="sxs-lookup"><span data-stu-id="c0a68-115">This happens when file A is deleted and needs a redirect to file B, then later file B is deleted and then redirects to file C. Ideally, both entries would point to C - so that A redirects to C, and B remains the same.</span></span> <span data-ttu-id="c0a68-116">这是一个很小的性能提升，并且此功能正在积极开发中。</span><span class="sxs-lookup"><span data-stu-id="c0a68-116">This is a minor performance gain, and the feature is actively being worked on.</span></span>

## <a name="in-action"></a><span data-ttu-id="c0a68-117">操作过程</span><span class="sxs-lookup"><span data-stu-id="c0a68-117">In action</span></span>

<span data-ttu-id="c0a68-118">下面是此功能的简短演示。</span><span class="sxs-lookup"><span data-stu-id="c0a68-118">Below is a brief demonstration of this feature.</span></span>

<span data-ttu-id="c0a68-119">[![排序重定向演示](media/sort-redirect.gif)](media/sort-redirect.gif#lightbox)</span><span class="sxs-lookup"><span data-stu-id="c0a68-119">[![Sort redirects demo](media/sort-redirect.gif)](media/sort-redirect.gif#lightbox)</span></span>
