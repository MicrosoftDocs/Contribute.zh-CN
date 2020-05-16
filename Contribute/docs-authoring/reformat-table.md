---
title: 重新设置 Markdown 表的格式 - Docs 创作包
description: 了解如何使用 Docs 创作包 Visual Studio Code 扩展中的各种 Markdown 表格式设置功能。
author: IEvangelist
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.date: 03/03/2020
ms.author: dapine
ms.openlocfilehash: 07c95f2a0d24a49f59eaffe1bec64ee872530c2f
ms.sourcegitcommit: cfba5ad25b898bfed76046126ce8ff4871910701
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/04/2020
ms.locfileid: "78336764"
---
# <a name="reformat-markdown-tables"></a>重新设置 Markdown 表的格式

[!INCLUDE [markdown-extension](includes/markdown-extension.md)]

## <a name="summary"></a>摘要

在 Markdown (\*.md) 文件中，选择一个完整的表时，现有两个表格式设置上下文菜单项  。 右键单击所选的 Markdown 表可打开上下文菜单。 你将看到类似以下菜单项的内容：

:::image type="content" source="media/reformat-table-menu.png" alt-text="重新设置表上下文菜单的格式":::

> [!TIP]
> 选择多个表时，不可使用此功能，它仅用于单个 Markdown 表  。 必须选择整个表，包括所需结果的标题。

## <a name="consolidate-selected-table"></a>合并所选表

选择“合并所选表”选项将折叠表标题以及每个值的两侧仅有一个空格的内容  。

## <a name="evenly-distribute-selected-table"></a>平均分布所选表

选择“平均分布所选表”选项将计算每列的最长值，并使用空格相应地平均分布所有其他值  。

## <a name="considerations"></a>考虑事项

此功能不会影响表的呈现，但将有助于提高表的可读性，从而更易于维护。 重新设置表格式的功能将保持列对齐方式不变。

请考虑下列表：

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

“平均分布”后：

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

“合并”后：

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

## <a name="in-action"></a>操作过程

下面是此功能的简短演示。

[![重新设置表格式演示](media/reformat-table.gif)](media/reformat-table.gif#lightbox)
