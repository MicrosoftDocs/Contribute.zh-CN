---
title: 排序所选内容 - Docs 创作包
description: 了解如何使用 Docs 创作包 Visual Studio Code 扩展中的“排序所选内”容功能。
author: IEvangelist
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.date: 03/03/2020
ms.author: dapine
ms.openlocfilehash: b4bd1761dc1bd9326275f011bb1935f6b695404d
ms.sourcegitcommit: cfba5ad25b898bfed76046126ce8ff4871910701
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/04/2020
ms.locfileid: "78336741"
---
# <a name="sort-selection"></a>排序所选内容

[!INCLUDE [markdown-extension](includes/markdown-extension.md)]

## <a name="summary"></a>摘要

在 Markdown (\*.md) 文件中，进行选择后，现有两个排序上下文菜单项。 右键单击所选内容可打开上下文菜单。 你将看到类似以下菜单项的内容：

:::image type="content" source="media/sort-selection-menu.png" alt-text="排序所选内容上下文菜单":::

> [!TIP]
> 排序上下文菜单项将隐藏，直到 Visual Studio Code 文本编辑器中出现有效的选定内容。

## <a name="sort-selection-ascending-a-to-z"></a>按升序对所选内容进行排序（A 到 Z）

选择“按升序对所选内容进行排序 (A 到 Z)”选项会按字母顺序从 A 到 Z（升序）对整个所选内容进行排序  。

## <a name="sort-selection-descending-z-to-a"></a>按降序对所选内容进行排序（Z 到 A）

选择“按降序对所选内容进行排序 (Z 到 A)”选项会按字母顺序从 Z 到 A（降序）对整个所选内容进行排序  。

## <a name="considerations"></a>考虑事项

基本排序机制使用自然语言排序  。 这使得它比标准排序的功能更强大且更全面。 请考虑下列表：

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

如果不使用自然语言排序，`Column1` 的顺序将为 1、11、2 等，但如果它知道 11 大于 2，则会形成以下升序顺序：

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

## <a name="in-action"></a>操作过程

下面是此功能的简短演示。

[![排序所选内容演示](media/sort-selection.gif)](media/sort-selection.gif#lightbox)
