---
title: 开发语言完成 - Docs 创作包
description: 了解开发语言完成功能如何在 Docs 创作包 Visual Studio Code 扩展中为参与者提供帮助。
author: scottaddie
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.date: 03/03/2020
ms.author: scaddie
ms.openlocfilehash: f81dc2315dc09256639c98ed72484517ff2c6ff3
ms.sourcegitcommit: cfba5ad25b898bfed76046126ce8ff4871910701
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/04/2020
ms.locfileid: "78336787"
---
# <a name="dev-lang-completion"></a><span data-ttu-id="b0ffc-103">开发语言完成</span><span class="sxs-lookup"><span data-stu-id="b0ffc-103">Dev lang completion</span></span>

[!INCLUDE [markdown-extension](includes/markdown-extension.md)]

## <a name="summary"></a><span data-ttu-id="b0ffc-104">总结</span><span class="sxs-lookup"><span data-stu-id="b0ffc-104">Summary</span></span>

<span data-ttu-id="b0ffc-105">在确定 Markdown 文件中可跟在三个反引号（代码隔离开头）后面的有效语言标识符（开发语言）时，参与者需要帮助。</span><span class="sxs-lookup"><span data-stu-id="b0ffc-105">Contributors need assistance determining the valid language identifiers (dev langs) that can follow triple-backticks (code fence openings) in a Markdown file.</span></span> <span data-ttu-id="b0ffc-106">遗憾的是，没有提供开发语言的生成时验证。</span><span class="sxs-lookup"><span data-stu-id="b0ffc-106">Unfortunately, build-time validation of dev langs doesn't exist.</span></span> <span data-ttu-id="b0ffc-107">这就使得同一概念文档集中的单个语言有不同的表示形式。</span><span class="sxs-lookup"><span data-stu-id="b0ffc-107">The result is disparate representations of a single language within the same conceptual docset.</span></span>

<span data-ttu-id="b0ffc-108">以 C# 为例。</span><span class="sxs-lookup"><span data-stu-id="b0ffc-108">Consider C# as an example.</span></span> <span data-ttu-id="b0ffc-109">参与者使用了 `c#`、`C#`、`cs`、`csharp` 和其他语言作为该语言的开发语言表示形式。</span><span class="sxs-lookup"><span data-stu-id="b0ffc-109">Contributors have used `c#`, `C#`, `cs`, `csharp`, and others as dev lang representations of the language.</span></span> <span data-ttu-id="b0ffc-110">而在上述表示形式中，哪一种是正确的？</span><span class="sxs-lookup"><span data-stu-id="b0ffc-110">Which of the preceding representations is correct?</span></span>

<span data-ttu-id="b0ffc-111">“开发语言完成”功能通过显示已知开发语言的列表来避免产生混淆。</span><span class="sxs-lookup"><span data-stu-id="b0ffc-111">The *Dev lang completion* feature dispels the confusion by displaying a list of known dev langs.</span></span> <span data-ttu-id="b0ffc-112">从 IntelliSense 中选择一个开发语言名称后：</span><span class="sxs-lookup"><span data-stu-id="b0ffc-112">Upon selecting a dev lang name from IntelliSense:</span></span>

* <span data-ttu-id="b0ffc-113">代码隔离会关闭。</span><span class="sxs-lookup"><span data-stu-id="b0ffc-113">The code fence is closed.</span></span>
* <span data-ttu-id="b0ffc-114">插入符号位于代码隔离中。</span><span class="sxs-lookup"><span data-stu-id="b0ffc-114">The caret is positioned in the code fence.</span></span>

## <a name="preferences"></a><span data-ttu-id="b0ffc-115">首选项</span><span class="sxs-lookup"><span data-stu-id="b0ffc-115">Preferences</span></span>

<span data-ttu-id="b0ffc-116">无法禁用此功能。</span><span class="sxs-lookup"><span data-stu-id="b0ffc-116">It's not possible to disable this feature.</span></span> <span data-ttu-id="b0ffc-117">可用设置如下：</span><span class="sxs-lookup"><span data-stu-id="b0ffc-117">The following settings are available:</span></span>

* [<span data-ttu-id="b0ffc-118">显示常用的开发语言</span><span class="sxs-lookup"><span data-stu-id="b0ffc-118">Display commonly used dev langs</span></span>](#display-commonly-used-dev-langs)
* [<span data-ttu-id="b0ffc-119">显示所有已知的开发语言</span><span class="sxs-lookup"><span data-stu-id="b0ffc-119">Display all known dev langs</span></span>](#display-all-known-dev-langs)

### <a name="display-commonly-used-dev-langs"></a><span data-ttu-id="b0ffc-120">显示常用的开发语言</span><span class="sxs-lookup"><span data-stu-id="b0ffc-120">Display commonly used dev langs</span></span>

<span data-ttu-id="b0ffc-121">只在单个文档集中使用一部分有效的开发语言。</span><span class="sxs-lookup"><span data-stu-id="b0ffc-121">Only a subset of the valid dev langs will be used in a single docset.</span></span> <span data-ttu-id="b0ffc-122">要增强用户体验，请执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="b0ffc-122">To enhance the user experience:</span></span>

1. <span data-ttu-id="b0ffc-123">在 Visual Studio Code 中，打开根目录中的文档集。</span><span class="sxs-lookup"><span data-stu-id="b0ffc-123">In Visual Studio Code, open the docset to the root directory.</span></span>
1. <span data-ttu-id="b0ffc-124">选择“文件” > “首选项” > “设置”，通过 Docs Markdown 扩展进行筛选。</span><span class="sxs-lookup"><span data-stu-id="b0ffc-124">Select **File** > **Preferences** > **Settings** and filter by *Docs Markdown Extension*.</span></span>
1. <span data-ttu-id="b0ffc-125">单击“Markdown: 文档集语言”部分中的“在 settings.json 中编辑”链接。</span><span class="sxs-lookup"><span data-stu-id="b0ffc-125">Click the **Edit in settings.json** link in the **Markdown: Docset Languages** section.</span></span>
1. <span data-ttu-id="b0ffc-126">将以下 `markdown.docsetLanguages` 属性添加到 settings.json 文件中：</span><span class="sxs-lookup"><span data-stu-id="b0ffc-126">Add the following `markdown.docsetLanguages` property to the *settings.json* file:</span></span>

    ```json
    {
        "markdown.docsetLanguages": [

        ]
    }
    ```

1. <span data-ttu-id="b0ffc-127">将插入符号放在属性的空数组中，再通过 <kbd>Ctrl</kbd> + <kbd></kbd> 激活 IntelliSense。</span><span class="sxs-lookup"><span data-stu-id="b0ffc-127">Position your caret in the property's empty array, and activate IntelliSense (via <kbd>Ctrl</kbd> + <kbd>Space</kbd>).</span></span> <span data-ttu-id="b0ffc-128">这将显示已知开发语言名称的列表。</span><span class="sxs-lookup"><span data-stu-id="b0ffc-128">A list of known dev lang names appears.</span></span>
1. <span data-ttu-id="b0ffc-129">将开发语言名称添加到数组中，直到对该列表满意为止。</span><span class="sxs-lookup"><span data-stu-id="b0ffc-129">Add dev lang names to the array until you're satisfied with the list.</span></span> <span data-ttu-id="b0ffc-130">例如，键入三个引号后，以下列表将向用户显示 4 个开发语言名称：</span><span class="sxs-lookup"><span data-stu-id="b0ffc-130">For example, the following list will display four dev lang names to the user after typing triple-ticks:</span></span>

    ```json
    {
        "markdown.docsetLanguages": [
            ".NET Core CLI",
            "C#",
            "Markdown",
            "YAML"
        ]
    }
    ```

1. <span data-ttu-id="b0ffc-131">将更改保存到 settings.json 文件。</span><span class="sxs-lookup"><span data-stu-id="b0ffc-131">Save your changes to the *settings.json* file.</span></span>

> [!WARNING]
> <span data-ttu-id="b0ffc-132">如果 `markdown.docsetLanguages` 数组为空，则显示所有已知的开发语言。</span><span class="sxs-lookup"><span data-stu-id="b0ffc-132">An empty `markdown.docsetLanguages` array causes all known dev langs to display.</span></span>

### <a name="display-all-known-dev-langs"></a><span data-ttu-id="b0ffc-133">显示所有已知的开发语言</span><span class="sxs-lookup"><span data-stu-id="b0ffc-133">Display all known dev langs</span></span>

<span data-ttu-id="b0ffc-134">默认情况下，所有已知的开发语言名称都显示在 IntelliSense 中。</span><span class="sxs-lookup"><span data-stu-id="b0ffc-134">By default, all known dev lang names are displayed in IntelliSense.</span></span> <span data-ttu-id="b0ffc-135">此设置将替代[显示常用的开发语言](#display-commonly-used-dev-langs)中所述的 `markdown.docsetLanguages` 属性。</span><span class="sxs-lookup"><span data-stu-id="b0ffc-135">This setting overrides the `markdown.docsetLanguages` property described in [Display commonly used dev langs](#display-commonly-used-dev-langs).</span></span>

<span data-ttu-id="b0ffc-136">要更改此设置，请执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="b0ffc-136">To change this setting:</span></span>

1. <span data-ttu-id="b0ffc-137">选择“文件” > “首选项” > “设置”，通过 Docs Markdown 扩展进行筛选。</span><span class="sxs-lookup"><span data-stu-id="b0ffc-137">Select **File** > **Preferences** > **Settings** and filter by *Docs Markdown Extension*.</span></span>
1. <span data-ttu-id="b0ffc-138">切换“Markdown: 所有可用语言”部分中的设置。</span><span class="sxs-lookup"><span data-stu-id="b0ffc-138">Toggle the setting in the **Markdown: All Available Languages** section.</span></span>

## <a name="in-action"></a><span data-ttu-id="b0ffc-139">操作过程</span><span class="sxs-lookup"><span data-stu-id="b0ffc-139">In action</span></span>

<span data-ttu-id="b0ffc-140">下面是此功能的简短演示：</span><span class="sxs-lookup"><span data-stu-id="b0ffc-140">Below is a brief demonstration of this feature:</span></span>

<span data-ttu-id="b0ffc-141">[![开发语言完成](media/dev-lang-completion.gif)](media/dev-lang-completion.gif#lightbox)</span><span class="sxs-lookup"><span data-stu-id="b0ffc-141">[![Dev lang completion](media/dev-lang-completion.gif)](media/dev-lang-completion.gif#lightbox)</span></span>
