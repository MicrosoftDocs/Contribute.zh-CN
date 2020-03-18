---
title: 排序所选内容 - Docs 创作包
description: 了解如何使用 Docs 创作包 Visual Studio Code 扩展中的“排序所选内”容功能。
author: IEvangelist
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.date: 03/03/2020
ms.author: dapine
ms.openlocfilehash: b4bd1761dc1bd9326275f011bb1935f6b695404d
ms.sourcegitcommit: dbc2c48194e29bfa0c88d33f50f94b9ee26be2da
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/05/2020
ms.locfileid: "78336741"
---
# <a name="sort-selection"></a><span data-ttu-id="73c06-103">排序所选内容</span><span class="sxs-lookup"><span data-stu-id="73c06-103">Sort selection</span></span>

[!INCLUDE [markdown-extension](includes/markdown-extension.md)]

## <a name="summary"></a><span data-ttu-id="73c06-104">摘要</span><span class="sxs-lookup"><span data-stu-id="73c06-104">Summary</span></span>

<span data-ttu-id="73c06-105">在 Markdown (\*.md) 文件中，进行选择后，现有两个排序上下文菜单项  。</span><span class="sxs-lookup"><span data-stu-id="73c06-105">In a Markdown (*\*.md*) file, when you've made a selection - two sorting context menu items are now available.</span></span> <span data-ttu-id="73c06-106">右键单击所选内容可打开上下文菜单。</span><span class="sxs-lookup"><span data-stu-id="73c06-106">Right-click on the selected text to open the context menu.</span></span> <span data-ttu-id="73c06-107">你将看到类似以下菜单项的内容：</span><span class="sxs-lookup"><span data-stu-id="73c06-107">You will see something similar to the following menu items:</span></span>

:::image type="content" source="media/sort-selection-menu.png" alt-text="排序所选内容上下文菜单":::

> [!TIP]
> <span data-ttu-id="73c06-109">排序上下文菜单项将隐藏，直到 Visual Studio Code 文本编辑器中出现有效的选定内容。</span><span class="sxs-lookup"><span data-stu-id="73c06-109">The sorting context menu items are hidden until there is a valid selection in the Visual Studio Code text editor.</span></span>

## <a name="sort-selection-ascending-a-to-z"></a><span data-ttu-id="73c06-110">按升序对所选内容进行排序（A 到 Z）</span><span class="sxs-lookup"><span data-stu-id="73c06-110">Sort selection ascending (A to Z)</span></span>

<span data-ttu-id="73c06-111">选择“按升序对所选内容进行排序 (A 到 Z)”选项会按字母顺序从 A 到 Z（升序）对整个所选内容进行排序  。</span><span class="sxs-lookup"><span data-stu-id="73c06-111">Selecting the **Sort selection ascending (A to Z)** option will sort the entire selection ascending, alphabetically from A to Z.</span></span>

## <a name="sort-selection-descending-z-to-a"></a><span data-ttu-id="73c06-112">按降序对所选内容进行排序（Z 到 A）</span><span class="sxs-lookup"><span data-stu-id="73c06-112">Sort selection descending (Z to A)</span></span>

<span data-ttu-id="73c06-113">选择“按降序对所选内容进行排序 (Z 到 A)”选项会按字母顺序从 Z 到 A（降序）对整个所选内容进行排序  。</span><span class="sxs-lookup"><span data-stu-id="73c06-113">Selecting the **Sort selection descending (Z to A)** option will sort the entire selection ascending, alphabetically from Z to A.</span></span>

## <a name="considerations"></a><span data-ttu-id="73c06-114">注意事项</span><span class="sxs-lookup"><span data-stu-id="73c06-114">Considerations</span></span>

<span data-ttu-id="73c06-115">基本排序机制使用自然语言排序  。</span><span class="sxs-lookup"><span data-stu-id="73c06-115">The underlying sorting mechanism uses *natural language* sorting.</span></span> <span data-ttu-id="73c06-116">这使得它比标准排序的功能更强大且更全面。</span><span class="sxs-lookup"><span data-stu-id="73c06-116">This makes it more powerful and comprehensive than standard sorting.</span></span> <span data-ttu-id="73c06-117">请考虑下列表：</span><span class="sxs-lookup"><span data-stu-id="73c06-117">Consider the following table:</span></span>

```markdown
| Column1 | Column2                                |
|---------|----------------------------------------|
| 1       | Number 1                               |
| Aa      | The first letter in the alphabet       |
| Ab      | The first letter in the alphabet       |
| C       | The a letter after A in the alphabet   |
| M       | Somewhere in the middle?               |
| 2       | Number 2                               |
| X       | The alphabet letter is towards the end |
| Z       | The last letter in the alphabet        |
| 11      | Number 11                              |
```

<span data-ttu-id="73c06-118">如果不使用自然语言排序，`Column1` 的顺序将为 1、11、2 等，但如果它知道 11 大于 2，则会形成以下升序顺序：</span><span class="sxs-lookup"><span data-stu-id="73c06-118">Without natural language sorting, the order for `Column1` would have been 1, 11, 2, etc. but instead it understands that 11 is greater than 2 - resulting in the following ascending order:</span></span>

```markdown
| Column1 | Column2                                |
|---------|----------------------------------------|
| 1       | Number 1                               |
| 2       | Number 2                               |
| 11      | Number 11                              |
| Aa      | The first letter in the alphabet       |
| Ab      | The first letter in the alphabet       |
| C       | The a letter after A in the alphabet   |
| M       | Somewhere in the middle?               |
| X       | The alphabet letter is towards the end |
| Z       | The last letter in the alphabet        |
```

## <a name="in-action"></a><span data-ttu-id="73c06-119">操作过程</span><span class="sxs-lookup"><span data-stu-id="73c06-119">In action</span></span>

<span data-ttu-id="73c06-120">下面是此功能的简短演示。</span><span class="sxs-lookup"><span data-stu-id="73c06-120">Below is a brief demonstration of this feature.</span></span>

<span data-ttu-id="73c06-121">[![排序所选内容演示](media/sort-selection.gif)](media/sort-selection.gif#lightbox)</span><span class="sxs-lookup"><span data-stu-id="73c06-121">[![Sort selection demo](media/sort-selection.gif)](media/sort-selection.gif#lightbox)</span></span>
