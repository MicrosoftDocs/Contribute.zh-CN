---
title: 自动智能引号替换 - Docs 创作包
description: 了解如何使用 Docs 创作包 Visual Studio Code 扩展自动替换智能引号。
author: IEvangelist
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.date: 03/03/2020
ms.author: dapine
ms.openlocfilehash: 048f244324d7dde540c78e6631ccb5abbed3e431
ms.sourcegitcommit: dbc2c48194e29bfa0c88d33f50f94b9ee26be2da
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/05/2020
ms.locfileid: "78336695"
---
# <a name="smart-quote-replacement"></a><span data-ttu-id="8fe62-103">智能引号替换</span><span class="sxs-lookup"><span data-stu-id="8fe62-103">Smart quote replacement</span></span>

[!INCLUDE [markdown-extension](includes/markdown-extension.md)]

## <a name="summary"></a><span data-ttu-id="8fe62-104">摘要</span><span class="sxs-lookup"><span data-stu-id="8fe62-104">Summary</span></span>

<span data-ttu-id="8fe62-105">内容开发人员负责编写现代技术和智能功能的一些最先进的特性，但是我们目前的工具更喜欢在 Markdown 中使用“直引号”。</span><span class="sxs-lookup"><span data-stu-id="8fe62-105">Content developers are responsible for authoring some of the most advanced features of modern technology and intelligence, yet our tooling today prefers the usage of "dumb quotes" in Markdown.</span></span> <span data-ttu-id="8fe62-106">反义词自然为“智能引号”。</span><span class="sxs-lookup"><span data-stu-id="8fe62-106">The antonym of course being "smart quotes".</span></span> <span data-ttu-id="8fe62-107">在理想排版中，智能引号比较常见，但它不是 Markdown 和呈现的 HTML 中的首选。</span><span class="sxs-lookup"><span data-stu-id="8fe62-107">Smart quotes are common with ideal typographies, but not preferred with Markdown and rendered HTML.</span></span>

<span data-ttu-id="8fe62-108">例如，在处理 Microsoft Word 文档时，你可能已经注意到，按住 <kbd>Shift</kbd> 并键入 <kbd>"</kbd> 时，Microsoft Word 会快速将 `"` 字符替换为智能引号等效字符 `“`。</span><span class="sxs-lookup"><span data-stu-id="8fe62-108">When working on a Microsoft Word document for example, you may have noticed that when you hold the <kbd>Shift</kbd> and type a <kbd>"</kbd> Microsoft Word quickly replaces the `"` character with a smart quote equivalent `“` character.</span></span>

| <span data-ttu-id="8fe62-109">说明</span><span class="sxs-lookup"><span data-stu-id="8fe62-109">Description</span></span>        | <span data-ttu-id="8fe62-110">Unicode</span><span class="sxs-lookup"><span data-stu-id="8fe62-110">Unicode</span></span>  | <span data-ttu-id="8fe62-111">智能引号</span><span class="sxs-lookup"><span data-stu-id="8fe62-111">Smart Quote</span></span> | <span data-ttu-id="8fe62-112">替换字符</span><span class="sxs-lookup"><span data-stu-id="8fe62-112">Replacement</span></span> |
|--------------------|----------|-------------|-------------|
| <span data-ttu-id="8fe62-113">左双引号</span><span class="sxs-lookup"><span data-stu-id="8fe62-113">Double left quote</span></span>  | `\u201c` | `“`         | `"`         |
| <span data-ttu-id="8fe62-114">右双引号</span><span class="sxs-lookup"><span data-stu-id="8fe62-114">Double right quote</span></span> | `\u201d` | `”`         | `"`         |
| <span data-ttu-id="8fe62-115">左单引号</span><span class="sxs-lookup"><span data-stu-id="8fe62-115">Single left quote</span></span>  | `\u2018` | `‘`         | `'`         |
| <span data-ttu-id="8fe62-116">右单引号</span><span class="sxs-lookup"><span data-stu-id="8fe62-116">Single right quote</span></span> | `\u2019` | `’`         | `'`         |

<span data-ttu-id="8fe62-117">在 Markdown (\*.md) 文件中，当你粘贴文本或更新内容时，此功能将主动评估内容并自动替换相应的值  。</span><span class="sxs-lookup"><span data-stu-id="8fe62-117">In a Markdown (*\*.md*) file, when you paste in text or as you update content - this feature will actively evaluate the content and automatically replace values accordingly.</span></span>

> [!NOTE]
> <span data-ttu-id="8fe62-118">智能引号替换功能还可替换其他字符，例如但不限于 `©, ™, ®, •`、下标和上标字符。</span><span class="sxs-lookup"><span data-stu-id="8fe62-118">The smart quote replacement feature also replaces other characters, such as but not limited to; (`©, ™, ®, •`, subscript and superscript characters).</span></span> <span data-ttu-id="8fe62-119">在粘贴 Word 文档中的文本时，此功能很有用。</span><span class="sxs-lookup"><span data-stu-id="8fe62-119">This is useful when pasting text from Word documents.</span></span>

## <a name="preferences"></a><span data-ttu-id="8fe62-120">首选项</span><span class="sxs-lookup"><span data-stu-id="8fe62-120">Preferences</span></span>

<span data-ttu-id="8fe62-121">此功能是可选的，但默认为 `true`。</span><span class="sxs-lookup"><span data-stu-id="8fe62-121">This feature is optional, but defaults to `true`.</span></span> <span data-ttu-id="8fe62-122">若要启用或关闭此功能，请执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="8fe62-122">To toggle this feature on or off:</span></span>

1. <span data-ttu-id="8fe62-123">选择“文件” > “首选项” > “设置”，通过 Docs Markdown 扩展进行筛选     。</span><span class="sxs-lookup"><span data-stu-id="8fe62-123">Select **File** > **Preferences** > **Settings** and filter by *Docs Markdown Extension*.</span></span>
1. <span data-ttu-id="8fe62-124">切换“Markdown: 所有可用语言”部分中的  设置。</span><span class="sxs-lookup"><span data-stu-id="8fe62-124">Toggle the setting in the **Markdown: Replace Smart Quotes** section.</span></span>

## <a name="in-action"></a><span data-ttu-id="8fe62-125">操作过程</span><span class="sxs-lookup"><span data-stu-id="8fe62-125">In action</span></span>

<span data-ttu-id="8fe62-126">下面是此功能的简短演示。</span><span class="sxs-lookup"><span data-stu-id="8fe62-126">Below is a brief demonstration of this feature.</span></span>

<span data-ttu-id="8fe62-127">[![替换智能引号演示](media/replace-smart-quotes.gif)](media/replace-smart-quotes.gif#lightbox)</span><span class="sxs-lookup"><span data-stu-id="8fe62-127">[![Replace smart quotes demo](media/replace-smart-quotes.gif)](media/replace-smart-quotes.gif#lightbox)</span></span>
