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
# <a name="sort-redirects"></a>排序重定向

[!INCLUDE [markdown-extension](includes/markdown-extension.md)]

## <a name="summary"></a>总结

随着 docs.microsoft.com 文档集的变化，最终将删除一些 Markdown 文件。 删除 Markdown 文件后，我们需要提供重定向，以便通过重定向正确解析对已删除文章的任何引用。 重定向在 .openpublishing.redirection.json 文件中指定。

1. 打开“命令面板”，按 <kbd>F1</kbd>（或 macOS 上的 <kbd>⇧⌘P</kbd>）
1. 类型：Docs:对主重定向文件进行排序
1. 选择要执行的命令
1. 查看对 .openpublishing.redirection.json 文件的更改

## <a name="considerations"></a>考虑事项

“菊花链”的概念与最初设计 .openpublishing.redirection.json 文件的方式相关。 随着时间的推移，作为重定向添加的文件最终会过时。 这会出现在以下情况：删除文件 A 后需要重定向到文件 B，然后删除文件 B，再重定向到文件 C。理想情况下，两个条目都会指向 C - 因此 A 重定向到 C，而 B 保持不变。 这是一个很小的性能提升，并且此功能正在积极开发中。

## <a name="in-action"></a>操作过程

下面是此功能的简短演示。

[![排序重定向演示](media/sort-redirect.gif)](media/sort-redirect.gif#lightbox)
