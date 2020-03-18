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
# <a name="smart-quote-replacement"></a>智能引号替换

[!INCLUDE [markdown-extension](includes/markdown-extension.md)]

## <a name="summary"></a>摘要

内容开发人员负责编写现代技术和智能功能的一些最先进的特性，但是我们目前的工具更喜欢在 Markdown 中使用“直引号”。 反义词自然为“智能引号”。 在理想排版中，智能引号比较常见，但它不是 Markdown 和呈现的 HTML 中的首选。

例如，在处理 Microsoft Word 文档时，你可能已经注意到，按住 <kbd>Shift</kbd> 并键入 <kbd>"</kbd> 时，Microsoft Word 会快速将 `"` 字符替换为智能引号等效字符 `“`。

| 说明        | Unicode  | 智能引号 | 替换字符 |
|--------------------|----------|-------------|-------------|
| 左双引号  | `\u201c` | `“`         | `"`         |
| 右双引号 | `\u201d` | `”`         | `"`         |
| 左单引号  | `\u2018` | `‘`         | `'`         |
| 右单引号 | `\u2019` | `’`         | `'`         |

在 Markdown (\*.md) 文件中，当你粘贴文本或更新内容时，此功能将主动评估内容并自动替换相应的值  。

> [!NOTE]
> 智能引号替换功能还可替换其他字符，例如但不限于 `©, ™, ®, •`、下标和上标字符。 在粘贴 Word 文档中的文本时，此功能很有用。

## <a name="preferences"></a>首选项

此功能是可选的，但默认为 `true`。 若要启用或关闭此功能，请执行以下操作：

1. 选择“文件” > “首选项” > “设置”，通过 Docs Markdown 扩展进行筛选     。
1. 切换“Markdown: 所有可用语言”部分中的  设置。

## <a name="in-action"></a>操作过程

下面是此功能的简短演示。

[![替换智能引号演示](media/replace-smart-quotes.gif)](media/replace-smart-quotes.gif#lightbox)
