---
title: 适用于 PowerShell 文章的模板和速查表
description: 本文包含一个便捷的模板，可用于针对 PowerShell 文档创建新文章
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
author: sdwheeler
ms.author: sewhee
ms.date: 10/09/2019
ms.openlocfilehash: e7ee9295794adfde78a2d500f0de3309dd3c821a
ms.sourcegitcommit: ca84e542b081e145052f38967e826f6ef25da1b2
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/12/2019
ms.locfileid: "72290348"
---
# <a name="markdown-style-guide-for-powershell-docs"></a>PowerShell-Docs 的 Markdown 风格指南

本文提供一些特定于 PowerShell-Docs 内容的风格指南。

有关其他写作风格指南，请参阅 [Microsoft 风格指南](https://docs.microsoft.com/style-guide/welcome/)。

## <a name="metadata"></a>元数据

此模板包含 Markdown 语法的示例，以及有关设置元数据的指南。
创建 Markdown 文件时，应将包括的模板复制到新文件，按如下所示填充元数据，并将上面的 H1 标题设为文章的标题。

所需的元数据块位于以下示例元数据块中：

```md
---
author: [GITHUB USERNAME]
description: [usually a summary of your first paragraph. It gets displayed in search results, and can help drive the correct traffic if well written.]
ms.date: [CREATION/UPDATE DATE - mm/dd/yyyy]
title: [ARTICLE TITLE]
---
# The H1 should not be the same as the title, but should describe the article contents
```

- 冒号 (:) 和元数据元素值之间必须有空格  。
- 值（例如，标题）中的冒号可中断元数据分析器。 在此情况下，使用双引号将标题括起来（例如，`title: "Writing .NET Core console apps: An advanced step-by-step guide"`）。
- **作者**：“作者”字段应包含作者的 GitHub 用户名  。
- **说明**：概括文章的内容。 它通常在搜索结果页中显示，并且不用于搜索排名。 它的长度应为 115-145 个字符（含空格）。
- **ms.date**：上一次重要更新的日期。 如果已评审和更新整篇文章，请在现有文章中更新此内容。 不保证更新拼写错误或类似的小修复。
- **标题**：在搜索引擎结果中显示。 该标题不应与 H1 标题中的标题相同，并且所含字符不应超过 60 个。

其他元数据附加于每篇文章，但我们通常在文件夹级别应用大多数元数据值，如 docfx.json 中所示  。

## <a name="product-terminology"></a>产品术语

PowerShell 有多个变体。 此表定义用于讨论 PowerShell 的一些不同术语。

- PowerShell - 这是默认值  。 PowerShell 是我们提供的产品。 术语 PowerShell 可用于描述任何版本的产品。
- PowerShell Core - 基于 .NET Core 公共语言运行时 (CoreCLR) 构建的 PowerShell，适用于任何受支持的平台  。
- Windows PowerShell - 基于 .NET Framework 公共语言运行时 (CLR) 构建的 PowerShell  。 Windows PowerShell 仅在 Windows 上提供，需要完整的 .Net Framework CLR。

通常，可将文档中对“Windows PowerShell”的引用更改为“PowerShell”。
讨论特定于 Windows 的技术时，不应更改“Windows PowerShell”  。

## <a name="basic-markdown-gfm-and-special-characters"></a>基本 Markdown、GFM 和特殊字符

可在有关 [Markdown](../how-to-write-use-markdown.md) 和 [Markdown 参考](../markdown-reference.md)的一般性文章中了解 Markdown、GitHub Flavored Markdown (GFM) 和 OPS 特定扩展的基础知识。

Markdown 使用特殊字符（例如，\*、\` 和 \#）进行格式设置。 如果要在内容中包括其中一个字符，必须执行以下两项操作之一：

- 在特殊字符前面放一个反斜杠，进行“转义”（例如 `\*` 表示 \*）。
- 对字符使用 [HTML 实体代码](http://www.ascii.cl/htmlcodes.htm)（例如，`&#42;` 表示 &#42;）。
- Markdown 文件应使用纯 ASCII 文本或 UTF-8 编码。 但是，应避免使用多字节 UTF-8 字符。 而应使用 HTML 实体。 例如，版权符号应使用 `&copy;`。
  其呈现为：“&copy;”。

## <a name="hyperlinks"></a>超链接

- 避免使用裸 URL。 链接应使用 Markdown 语法 `[friendlyname](url-or-path)`
- 链接必须具有易记名称，通常是链接主题的标题
- 底部“相关链接”部分中的所有项都应采用超链接形式。
- 链接到 docs.microsoft.com 上托管的其他内容时，请使用相对链接  。
- 请勿在超链接的括号内使用反引号、粗体或其他标记。

有关链接的详细信息，请参阅[在文档中使用链接](../how-to-write-links.md)。

## <a name="filenames"></a>文件名

文件名采用以下规则：

- 只能包含字母、数字和连字符。
- 不使用空格或标点符号字符。 使用连字符分隔文件名中的单词和数字。
- 使用特定的行为动词，如开发、购买、构建和故障排除。 不使用后缀是 ing 的单词。
- 不使用小词汇 - 不包含 a、and、the、in 或 or 等。
- 必须在 Markdown 中且使用 .md 文件扩展名。
- 使文件名尽量简短，且适当合理。 此名称会包含在文章的 URL 中。

## <a name="blank-lines-spaces-and-tabs"></a>空行、空格和制表符

删除重复的空行。 在 HTML 中，多个空行呈现为单个空行，因此没有必要使用多个空行。

在 Markdown 中，空行还表示代码块结束。 不同类型的 Markdown 代码块之间应存在空白（例如，段落与列表或标头之间）。

> [!NOTE]
> 间距在 Markdown 中非常重要。 应始终使用空格，而非硬制表符。 应删除行末尾多余的空格。

## <a name="titles-and-headings"></a>各级标题

应只使用 [ATX 标题][atx]（# 样式，而非 `=` 或 `-` 样式标头）。

- 句子大小写的使用 - 仅正确的名词和标题或标头的第一个字母应采用大写形式
- 在 `#` 与标题的第一个字母之间必须有一个空格
- 标题应由一个空行包围
- 每个文档只有一个 H1
- 标头级别应逐个增加，不得跳过级别
- 请勿在标头中使用反引号、粗体或其他标记

> [!CAUTION]
> [PlatyPS][platyPS] 为 cmdlet 引用强制执行的架构需要特定的 H2 和 H3 标头。 添加或删除标头可能会中断生成。 有关详细信息，请参阅 [cmdlet 引用风格指南](powershell-style-reference.md)。

## <a name="limit-line-length-to-100-characters"></a>将行长度限制为 100 个字符

这简化了差异和历史记录的命令行输出。

此规则并不能针对 PowerShell-Docs 中的大部分现有内容强制执行，但随着时间的推移，我们正朝着这个方向努力。 如需帮助，请随时联系。借助 Visual Studio Code (VSCode) 中的[重排扩展][reflow]，可轻松地将段落的格式重新设置为此限制。

## <a name="lists"></a>列表

如果列表包含多个句子或段落，请考虑使用子标头，而非列表。

列表应由一个空行包围。

### <a name="unordered-lists"></a>未排序列表

请勿以句点结束列表项，除非包含多个句子。 对于列表项项目符号，使用连字符 (`-`)。 这样可避免与使用星号 [`*`] 的粗体或斜体标记混淆。 要在项目符号项下包含段落或其他元素，请插入换行符并缩进，使其与项目符号后的第一个字符对齐。

例如：

```markdown
This is a list that contain sub-elements under a bullet item.

- First bullet item

  Sentence explaining the first bullet.

  - Sub-bullet item

    Sentence explaining the sub-bullet.

- Second bullet item
- Third bullet item
```

这是一个项目符号项下包含子元素的列表。

- 第一个项目符号项

  用于解释第一个项目符号的句子。

  - 子项目符号项

    用于解释子项目符号的句子。

- 第二个项目符号项
- 第三个项目符号项

### <a name="ordered-lists"></a>已排序列表

要在编号项下包含段落或其他元素，请进行缩进，使其与项目编号后的第一个字符对齐。

```markdown
1. For the first element, insert a single space after the 1. Long sentences should be
   wrapped to the next line and must line up with the first character after the numbered
   list marker.

   To include a second element (like this one), insert a line break after the first
   and align indentations. The indentation of the second element must line up with
   the first character after the numbered list marker. For single digit items, like
   this one, you indent to column 4. For double digits items, for example item number
   10, you indent to column 5.

1. The next numbered item starts here.
```

获取此输出：

> 1. 对于第一个元素，在 1 之后插入一个空格。 长句应换到下一行，并且必须与编号列表标记后面的第一个字符对齐。
>
>    要包含第二个元素（如下所示），请在第一个元素后面插入换行符，并缩进以使之对齐。 第二个元素缩进后，必须与编号列表标记后面的第一个字符对齐。 对于一位数的项（如下所示），缩进到第 4 列。 对于两位数的项，例如项编号 10，缩进到第 5 列。
>
> 1. 下一个编号项从此处开始。

以编号形式列出的所有项都应使用数字 `1.`，而不是逐项递增。
Markdown 呈现会自动递增该值。 这样可以更轻松地对项进行重新排序，并标准化从属内容的缩进。

## <a name="formatting-command-syntax-elements"></a>设置命令语法元素的格式

- PowerShell cmdlet 名称采用[帕斯卡拼写法][pascal-case]。 谓词通过连字符与名词分隔。 对于 cmdlet 和参数，始终使用帕斯卡拼写法下的全名。 应避免使用别名，除非专门讨论别名。

- 在段落中，语言关键字、cmdlet 名称和变量引用应由反引号 (`` ` ``) 字符引起来。 属性名、参数名和类名应采用粗体  。

  例如：

  ~~~markdown
  The following code assigns the output of `Get-ChildItem` to the `$files` variable.

  ```powershell
  $files = Get-ChildItem C:\Windows
  ```
  ~~~

- 按名称引用参数时，该名称应采用粗体  。 演示使用带有连字符前缀的参数时，应使用反引号将参数引起来。 例如：

  ```markdown
  The parameter's name is **Name**, but it is typed as `-Name` when used on the command
  line as a parameter.
  ```

- 引用 EXE、脚本等外部命令时，命令名称应采用粗体，全部小写（如果位于句子开头，则为大写），并包含相应的文件扩展名。 例如：

  ```markdown
  For example, on Windows systems, you can use the `net start` and `net stop` commands
  to start and stop a service. **Sc.exe** is another service control tool for Windows.
  That name does not fit into the naming pattern for the **net.exe** service commands.
  ```

- 演示外部命令的示例用法时，示例应由反引号引起来。
  如果与别名存在名称冲突，则必须在命令示例中包含文件扩展名。 例如：

  ```markdown
  To start the spooler service on a remote computer named DC01, you type `sc.exe \\DC01 start spooler`.
  ```

- 编写概念性文章（而非引用内容）时，cmdlet 名称的第一个实例应超链接到 cmdlet 文档中。 请勿在超链接的括号内使用反引号、粗体或其他标记。

  例如：

  ```markdown
  This [Write-Host](/powershell/module/Microsoft.PowerShell.Utility/Write-Host) cmdlet
  uses the **Object** parameter to ...
  ```

  有关详细信息，请参阅风格指南的[超链接](#hyperlinks)部分。

## <a name="images"></a>图像

用于包含图像的语法是：

```Syntax
![[alt text]](<folderPath>)
```

示例：

```markdown
![Introduction](./media/overview/Introduction.png)
```

其中 `alt text` 是图像的简短说明，`<folder path>` 是图像的相对路径。 视觉障碍用户的屏幕阅读器需采用替换文字。 如果存在无法呈现图像的网站 bug，这也非常有用。

在包含文章的文件夹中，图像应存储在 `media/<article-name>` 文件夹中。 不同的文章不应共享图像。 在 `media` 文件夹下创建与文章的文件名相匹配的文件夹。 将该文章的图像复制到该新文件夹。 如果多个文章使用一个图像，则每个图像文件夹都必须具有该图像文件的副本。 这种做法可防止更改一篇文章的图像影响到另一篇文章。

在某些情况下，需要在多篇文章中共享图像，如徽标和图标。 这些图像存储在存储库根目录的 `/media/shared` 文件夹中。

支持下列图像文件类型：*.png"、*.gif"、*.jpeg"、*.jpg"、*.svg

<!-- External URLs -->
[platyPS]: https://github.com/PowerShell/platyPS
[markdig]: https://github.com/lunet-io/markdig
[CommonMark]: https://spec.commonmark.org/
[atx]: https://github.github.com/gfm/#atx-headings
[pascal-case]: https://en.wikipedia.org/wiki/PascalCase
[reflow]: https://marketplace.visualstudio.com/items?itemName=marvhen.reflow-markdown
