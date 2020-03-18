---
title: 开发语言完成 - Docs 创作包
description: 了解开发语言完成功能如何在 Docs 创作包 Visual Studio Code 扩展中为参与者提供帮助。
author: scottaddie
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.date: 03/03/2020
ms.author: scaddie
ms.openlocfilehash: f81dc2315dc09256639c98ed72484517ff2c6ff3
ms.sourcegitcommit: dbc2c48194e29bfa0c88d33f50f94b9ee26be2da
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/05/2020
ms.locfileid: "78336787"
---
# <a name="dev-lang-completion"></a>开发语言完成

[!INCLUDE [markdown-extension](includes/markdown-extension.md)]

## <a name="summary"></a>摘要

在确定 Markdown 文件中可跟在三个反引号（代码隔离开头）后面的有效语言标识符（开发语言）时，参与者需要帮助。 遗憾的是，没有提供开发语言的生成时验证。 这就使得同一概念文档集中的单个语言有不同的表示形式。

以 C# 为例。 参与者使用了 `c#`、`C#`、`cs`、`csharp` 和其他语言作为该语言的开发语言表示形式。 而在上述表示形式中，哪一种是正确的？

“开发语言完成”功能通过显示已知开发语言的列表来避免产生混淆  。 从 IntelliSense 中选择一个开发语言名称后：

* 代码隔离会关闭。
* 插入符号位于代码隔离中。

## <a name="preferences"></a>首选项

无法禁用此功能。 可用设置如下：

* [显示常用的开发语言](#display-commonly-used-dev-langs)
* [显示所有已知的开发语言](#display-all-known-dev-langs)

### <a name="display-commonly-used-dev-langs"></a>显示常用的开发语言

只在单个文档集中使用一部分有效的开发语言。 要增强用户体验，请执行以下操作：

1. 在 Visual Studio Code 中，打开根目录中的文档集。
1. 选择“文件” > “首选项” > “设置”，通过 Docs Markdown 扩展进行筛选     。
1. 单击“Markdown: 文档集语言”部分中的   “在 settings.json 中编辑”链接。
1. 将以下 `markdown.docsetLanguages` 属性添加到 settings.json 文件中  ：

    ```json
    {
        "markdown.docsetLanguages": [

        ]
    }
    ```

1. 将插入符号放在属性的空数组中，再通过 <kbd>Ctrl</kbd> + <kbd></kbd> 激活 IntelliSense。 这将显示已知开发语言名称的列表。
1. 将开发语言名称添加到数组中，直到对该列表满意为止。 例如，键入三个引号后，以下列表将向用户显示 4 个开发语言名称：

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

1. 将更改保存到 settings.json 文件  。

> [!WARNING]
> 如果 `markdown.docsetLanguages` 数组为空，则显示所有已知的开发语言。

### <a name="display-all-known-dev-langs"></a>显示所有已知的开发语言

默认情况下，所有已知的开发语言名称都显示在 IntelliSense 中。 此设置将替代[显示常用的开发语言](#display-commonly-used-dev-langs)中所述的 `markdown.docsetLanguages` 属性。

要更改此设置，请执行以下操作：

1. 选择“文件” > “首选项” > “设置”，通过 Docs Markdown 扩展进行筛选     。
1. 切换“Markdown: 所有可用语言”部分中的  设置。

## <a name="in-action"></a>操作过程

下面是此功能的简短演示：

[![开发语言完成](media/dev-lang-completion.gif)](media/dev-lang-completion.gif#lightbox)
