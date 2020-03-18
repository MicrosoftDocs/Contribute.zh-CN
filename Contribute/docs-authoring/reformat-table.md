---
title: 重新设置 Markdown 表的格式 - Docs 创作包
description: 了解如何使用 Docs 创作包 Visual Studio Code 扩展中的各种 Markdown 表格式设置功能。
author: IEvangelist
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.date: 03/03/2020
ms.author: dapine
ms.openlocfilehash: 07c95f2a0d24a49f59eaffe1bec64ee872530c2f
ms.sourcegitcommit: dbc2c48194e29bfa0c88d33f50f94b9ee26be2da
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/05/2020
ms.locfileid: "78336764"
---
# <a name="reformat-markdown-tables"></a><span data-ttu-id="52bc1-103">重新设置 Markdown 表的格式</span><span class="sxs-lookup"><span data-stu-id="52bc1-103">Reformat Markdown tables</span></span>

[!INCLUDE [markdown-extension](includes/markdown-extension.md)]

## <a name="summary"></a><span data-ttu-id="52bc1-104">摘要</span><span class="sxs-lookup"><span data-stu-id="52bc1-104">Summary</span></span>

<span data-ttu-id="52bc1-105">在 Markdown (\*.md) 文件中，选择一个完整的表时，现有两个表格式设置上下文菜单项  。</span><span class="sxs-lookup"><span data-stu-id="52bc1-105">In a Markdown (*\*.md*) file, when you select a complete table - two table formatting context menu items are now available.</span></span> <span data-ttu-id="52bc1-106">右键单击所选的 Markdown 表可打开上下文菜单。</span><span class="sxs-lookup"><span data-stu-id="52bc1-106">Right-click on the selected Markdown table to open the context menu.</span></span> <span data-ttu-id="52bc1-107">你将看到类似以下菜单项的内容：</span><span class="sxs-lookup"><span data-stu-id="52bc1-107">You will see something similar to the following menu items:</span></span>

:::image type="content" source="media/reformat-table-menu.png" alt-text="重新设置表上下文菜单的格式":::

> [!TIP]
> <span data-ttu-id="52bc1-109">选择多个表时，不可使用此功能，它仅用于单个 Markdown 表  。</span><span class="sxs-lookup"><span data-stu-id="52bc1-109">This feature **does not** work with multiple table selections, but rather is intended for a single Markdown table.</span></span> <span data-ttu-id="52bc1-110">必须选择整个表，包括所需结果的标题。</span><span class="sxs-lookup"><span data-stu-id="52bc1-110">You must select the entire table, including headings for desired results.</span></span>

## <a name="consolidate-selected-table"></a><span data-ttu-id="52bc1-111">合并所选表</span><span class="sxs-lookup"><span data-stu-id="52bc1-111">Consolidate selected table</span></span>

<span data-ttu-id="52bc1-112">选择“合并所选表”选项将折叠表标题以及每个值的两侧仅有一个空格的内容  。</span><span class="sxs-lookup"><span data-stu-id="52bc1-112">Selecting the **Consolidate selected table** option will collapse the table headings and contents with only a single space on either side of each value.</span></span>

## <a name="evenly-distribute-selected-table"></a><span data-ttu-id="52bc1-113">平均分布所选表</span><span class="sxs-lookup"><span data-stu-id="52bc1-113">Evenly distribute selected table</span></span>

<span data-ttu-id="52bc1-114">选择“平均分布所选表”选项将计算每列的最长值，并使用空格相应地平均分布所有其他值  。</span><span class="sxs-lookup"><span data-stu-id="52bc1-114">Selecting the **Evenly distribute selected table** option will calculate the longest value in each column and evenly distribute all the other values accordingly with space.</span></span>

## <a name="considerations"></a><span data-ttu-id="52bc1-115">注意事项</span><span class="sxs-lookup"><span data-stu-id="52bc1-115">Considerations</span></span>

<span data-ttu-id="52bc1-116">此功能不会影响表的呈现，但将有助于提高表的可读性，从而更易于维护。</span><span class="sxs-lookup"><span data-stu-id="52bc1-116">The feature will not impact the rendering of the table, but it will help to improve the readability of the table - thus making more maintainable.</span></span> <span data-ttu-id="52bc1-117">重新设置表格式的功能将保持列对齐方式不变。</span><span class="sxs-lookup"><span data-stu-id="52bc1-117">The reformatting table feature will keep column alignment intact.</span></span>

<span data-ttu-id="52bc1-118">请考虑下列表：</span><span class="sxs-lookup"><span data-stu-id="52bc1-118">Consider the following table:</span></span>

```markdown
| Column1 | This is a long column name | Column3 |  |
|--:|---------|:--:|:----|
||         |  |         |
|     |  |         |   a value      |
||         |         |         |
|     |         | This is a long value |       but why? |
|     |         |         |         |
|     |                                           |         | Here is something |
|  |         |   |         |
```

<span data-ttu-id="52bc1-119">“平均分布”后：</span><span class="sxs-lookup"><span data-stu-id="52bc1-119">After being "evenly distributed":</span></span>

```markdown
| Column1 | This is a long column name | Column3              |                   |
|--------:|----------------------------|:--------------------:|:------------------|
|         |                            |                      |                   |
|         |                            |                      | a value           |
|         |                            |                      |                   |
|         |                            | This is a long value | but why?          |
|         |                            |                      |                   |
|         |                            |                      | Here is something |
|         |                            |                      |                   |
```

<span data-ttu-id="52bc1-120">“合并”后：</span><span class="sxs-lookup"><span data-stu-id="52bc1-120">After being "consolidated":</span></span>

```markdown
| Column1 | This is a long column name | Column3 |  |
|-:|--|:-:|:-|
|  |  |  |  |
|  |  |  | a value |
|  |  |  |  |
|  |  | This is a long value | but why? |
|  |  |  |  |
|  |  |  | Here is something |
|  |  |  |  |
```

## <a name="in-action"></a><span data-ttu-id="52bc1-121">操作过程</span><span class="sxs-lookup"><span data-stu-id="52bc1-121">In action</span></span>

<span data-ttu-id="52bc1-122">下面是此功能的简短演示。</span><span class="sxs-lookup"><span data-stu-id="52bc1-122">Below is a brief demonstration of this feature.</span></span>

<span data-ttu-id="52bc1-123">[![重新设置表格式演示](media/reformat-table.gif)](media/reformat-table.gif#lightbox)</span><span class="sxs-lookup"><span data-stu-id="52bc1-123">[![Reformat table demo](media/reformat-table.gif)](media/reformat-table.gif#lightbox)</span></span>
