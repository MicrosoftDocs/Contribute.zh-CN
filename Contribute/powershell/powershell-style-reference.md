---
title: 有关编写 cmdlet 引用的特定指南
description: 本文介绍有关设置 PowerShell 代码示例格式的特定规则。 这适用于包含示例的概念性文章以及 cmdlet 引用。
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
author: sdwheeler
ms.author: sewhee
ms.date: 10/09/2019
ms.openlocfilehash: 793a3c02ae0edf192416ae514585d5161e8c1f98
ms.sourcegitcommit: ca84e542b081e145052f38967e826f6ef25da1b2
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/12/2019
ms.locfileid: "72290279"
---
# <a name="updating-reference-articles"></a>更新引用文章

Cmdlet 引用文章具有特定的结构。 此结构由 PlatyPS 定义[][]。
PlatyPS 工具用于生成 PowerShell 模块的 cmdlet 帮助。 PlatyPS 为 cmdlet 创建基础 Markdown 文件。 编辑 Markdown 文件后，使用 PlatyPS 创建 `Get-Help` cmdlet 使用的 MAML 帮助文件。

PlatyPS 具有用于 cmdlet 引用的硬编码架构，并且已写入代码中。 [platyPS.schema.md][] 文档尝试描述此结构。 架构冲突会导致生成错误，必须先修复这些错误然后才能接受你撰写的内容。

## <a name="general-guidelines"></a>一般性指导

- 请勿删除任何标头结构。 PlatyPS 需要一组特定的标头。
- 输入类型和输出类型标头必须具有类型   。 如果 cmdlet 不接受输入或不返回值，则使用“None”值。
- 仅[示例](#format-for-examples)部分允许使用隔离代码块。
- 任何段落都可使用内联代码范围。

## <a name="formatting-about_-files"></a>设置 About_ 文件的格式

`About_*` 文件现由 [Pandoc][] 处理，而不是 PlatyPS。 `About_*` 文件的格式设置使其在所有版本的 PowerShell 和发布工具中具有最佳兼容性。
如果未以存储库维护人员的身份签入，请勿更改 `about_*` 文件的格式。

基本格式设置指南：

- 将行限制为 80 个字符
- 将代码块、块引号和表限制为 76 个字符，因为在转换过程中，Pandoc 会将这些内容缩进四个空格
- 表需要调整为 76 个字符以内
  - 手动将单元格内容换到多行
  - 在每一行上使用开始和结束 `|` 字符
  - 请参阅 [about_Comparison_Operators][about-example] 中的工作示例
- 使用 Pandoc 的特殊字符 `\`、`$`、`` ` `` 和 `<`
  - 在标头中 - 必须使用前导 `\` 字符对这些字符进行转义
  - 在段落中 - 应将这些字符放入代码范围中。 例如：

    ~~~markdown
    ### The purpose of the \$foo variable

    The `$foo` variable is used to store ...
    ~~~

## <a name="format-for-examples"></a>示例的格式

在 PlatyPS 架构中，EXAMPLES 标头是 H2 标头，每个示例都是 H3 标头  。

在示例中，架构不允许按段落分隔代码块。 有效的架构为：

```
### Example #X title

0 or more paragraphs
1 or more code blocks
0 or more paragraphs.
```

为每个示例编号并添加简短标题。

例如：

~~~markdown
### Example 1: Get cmdlets, functions, and aliases

This example gets the PowerShell cmdlets, functions, and aliases that are installed on the
computer.

```powershell
Get-Command
```
~~~


[PlatyPS]: https://github.com/powershell/platyps
[platyPS.schema.md]: https://github.com/PowerShell/platyPS/blob/master/platyPS.schema.md
[issue1806]: https://github.com/PowerShell/PowerShell-Docs/issues/1806
[about-example]: https://github.com/MicrosoftDocs/PowerShell-Docs/blob/staging/reference/6/Microsoft.PowerShell.Core/About/about_Comparison_Operators.md
[Pandoc]: https://pandoc.org