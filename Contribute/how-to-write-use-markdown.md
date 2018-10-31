---
title: 如何使用 Markdown 撰写 Docs
description: 本文提供用于撰写 docs.microsoft.com 文章的 Markdown 语言的基础知识和参考信息。
ms.date: 07/13/2017
ms.openlocfilehash: 6bb8a1fa20957512addb07dda0e68abec4b0a83f
ms.sourcegitcommit: d3c7b49dc854dae8da9cd49da8ac4035789a5010
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/23/2018
ms.locfileid: "49805714"
---
# <a name="how-to-use-markdown-for-writing-docs"></a>如何使用 Markdown 撰写 Docs

[Docs.microsoft.com](http://docs.microsoft.com) 文章采用名为 [Markdown](https://daringfireball.net/projects/markdown/) 的轻型标记语言撰写，这种语言可读性强且简单易学。 正因为如此，Markdown 已迅速成为行业标准。

由于 Doc 内容存储在 GitHub 中，因此可以使用 Markdown 超集（称为 [GitHub 风格的 Markdown (GFM)](https://help.github.com/categories/writing-on-github/)），它为常用格式需求提供了附加功能。 此外， Open Publishing Services (OPS) 还将实现 Markdig Markdown 分析程序。 Markdig 与 GFM 高度兼容，并添加了实现 Docs 特定功能的功能。

* Markdig 是一种适用于 .NET 的 Markdown 分析程序，它运行快速、功能强大且兼容 CommonMark。
* https://github.com/lunet-io/markdig
* 更好的社区支持
* 更好的标准支持

## <a name="markdown-basics"></a>Markdown 基础知识

### <a name="headings"></a>标题

要创建标题，请使用井号标记 (#)，如下所示：

```markdown
# This is heading 1
## This is heading 2
### This is heading 3
#### This is heading 4
```

### <a name="bold-and-italic-text"></a>粗体和斜体文本

要将文本设置为粗体格式，请用两个星号括住文本：

```markdown
This text is **bold**.
```

要将文本设置为斜体格式，请用一个星号括住文本：

```markdown
This text is *italic*.
```

要将文本同时设置为粗体和斜体格式，请用三个星号括住文本：

```markdown
This is text is both ***bold and italic***.
```

### <a name="lists"></a>列表

#### <a name="unordered-list"></a>无序列表

要为无序列表/项目符号列表设置格式，可以使用星号或短划线。 例如，以下 Markdown：

```markdown
- List item 1
- List item 2
- List item 3
```

将显示为：

- 列表项目 1
- 列表项目 2
- 列表项目 3

要将一个列表嵌套在另一个列表中，请缩进子列表项。 例如，以下 Markdown：

```markdown
- List item 1
  - List item A
  - List item B
- List item 2
```

将显示为：

- 列表项目 1
  - 列表项目 A
  - 列表项目 B
- 列表项目 2

#### <a name="ordered-list"></a>有序列表

要设置有序/分阶段列表的格式，可以使用相应的编号。 例如，以下 Markdown：

```markdown
1. First instruction
2. Second instruction
3. Third instruction
```

将显示为：

1. 第一个说明
2. 第二个说明
3. 第三个说明

要将一个列表嵌套在另一个列表中，请缩进子列表项。 例如，以下 Markdown：

```markdown
1. First instruction
   1. Sub-instruction
   2. Sub-instruction
2. Second instruction
```

将显示为：

1. 第一个说明
   1. 辅助说明
   2. 辅助说明
2. 第二个说明

### <a name="tables"></a>表格

表格不属于核心 Markdown 规范，但是它们受 GFM 支持。 可以使用竖线 (|) 和连字符 (-) 字符创建表格。 连字符用于创建每列的标题，而竖线用于分隔每列。 请在表格前面加入一个空行，使它能够正确显示。

例如，以下 Markdown：

```markdown
| Fun                  | With                 | Tables          |
| :------------------- | -------------------: |:---------------:|
| left-aligned column  | right-aligned column | centered column |
| $100                 | $100                 | $100            |
| $10                  | $10                  | $10             |
| $1                   | $1                   | $1              |
```

将显示为：

| 趣                  | 含                 | 表格          |
| :------------------- | -------------------: |:---------------:|
| 左对齐列  | 右对齐列 | 居中列 |
| $100                 | $100                 | $100            |
| $10                  | $10                  | $10             |
| $1                   | $1                   | $1              |

有关创建表格的详细信息，请参阅：

- Markdig [表格换行功能](#table-wrapping)，有助于设置宽表格的格式。
- GitHub 的[使用表格整理信息](https://help.github.com/articles/organizing-information-with-tables/)。
- [Markdown 表格生成器](https://www.tablesgenerator.com/markdown_tables) Web 应用。
- [Adam Pritchard 的 Markdown 备忘单](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#wiki-tables)。
- [Michel Fortin 的 Markdown Extra](https://michelf.ca/projects/php-markdown/extra/#table)。
- [将 HTML 表转换为 Markdown 格式](https://jmalarcon.github.io/markdowntables/)。

### <a name="links"></a>链接

Markdown 的内联链接语法由两部分组成：`[link text]` 部分，这是要创建为超链接的文本；后跟 `(file-name.md)` 部分，这是要链接到的 URL 或者文件名：

 `[link text](file-name.md)`

有关链接的详细信息，请参阅：

- [Markdown 语法指南](https://daringfireball.net/projects/markdown/syntax#link)，详细了解 Markdown 的基本链接支持相关信息。
- 参阅本指南的[链接](how-to-write-links.md)部分，深入了解 Markdig 提供的其他链接语法。

### <a name="code-snippets"></a>代码片段

Markdown 不仅支持将代码片段内联在某个句子中，还支持将它作为单独的“隔离”块放置在两个句子之间。 有关详细信息，请参阅：

- [Markdown 代码块本机支持](https://daringfireball.net/projects/markdown/syntax#precode)
- [针对代码隔离和语法高亮显示的 GFM 支持](https://help.github.com/articles/creating-and-highlighting-code-blocks/)

借助隔离代码块，可以轻松实现代码片段的语法高亮显示。 隔离代码块的一般格式为：

    ```alias
    ...
    your code goes in here
    ...
    ```

开头的三个撇号 (`) 字符后面的别名定义要使用的语法高亮显示。 下面列出了 Docs 内容中常用的编程语言以及匹配的标签：

这些语言支持友好名称并且大多数都可以突出显示语言。

|名称|Markdown 标签|
|-----|-------|
|.NET 控制台|dotnetcli|
|ASP.NET (C#)|aspx-csharp|
|ASP.NET (VB)|aspx-vb|
|AzCopy|azcopy|
|Azure CLI|azurecli|
|Azure PowerShell|azurepowershell|
|C++|cpp|
|C++/CX|cppcx|
|C++/WinRT|cppwinrt|
|C#|csharp|
|CSHTML|cshtml|
|DAX|dax|
|F#|fsharp|
|Go|go|
|HTML|html|
|HTTP|http|
|Java|java|
|JavaScript|javascript|
|JSON|json|
|Markdown|md|
|NodeJS|nodejs|
|Objective-C|objc|
|OData|odata|
|PHP|php|
|Power Apps Formula|powerappsfl|
|PowerShell|powershell|
|Python|python|
|Q#|qsharp|
|R|r|
|Ruby|ruby|
|SQL|sql|
|Swift|swift|
|TypeScript|typescript|
|VB|vb|
|VSTS CLI|vstscli|
|XAML|xaml|
|XML|xml|

#### <a name="example-c"></a>示例：C\#

__Markdown__

    ```csharp
    // Hello1.cs
    public class Hello1
    {
        public static void Main()
        {
            System.Console.WriteLine("Hello, World!");
        }
    }
    ```

__呈现__

```csharp
// Hello1.cs
public class Hello1
{
    public static void Main()
    {
        System.Console.WriteLine("Hello, World!");
    }
}
```

#### <a name="example-sql"></a>示例：SQL

__Markdown__

    ```sql
    CREATE TABLE T1 (
      c1 int PRIMARY KEY,
      c2 varchar(50) SPARSE NULL
    );
    ```

__呈现__

```sql
CREATE TABLE T1 (
  c1 int PRIMARY KEY,
  c2 varchar(50) SPARSE NULL
);
```

## <a name="ops-custom-markdown-extensions"></a>OPS 自定义 Markdown 扩展

> [!NOTE]
> Open Publishing Services(OPS) 可实现 Markdown Markdig 分析程序，它与 GitHub 风格的 Markdown (GFM) 高度兼容。 Markdig 通过 Markdown 扩展添加一些功能。 就这一点而言，本指南从完整的《OPS 创作指南》中选用了几篇文章，以供参考。 （例如，请参阅目录中的“Markdig 和 Markdown 扩展”以及“代码片段”。）

Doc 文章使用 GFM 完成大多文章的格式设置，如段落、链接、列表和标题。 要想实现更丰富的格式设置功能，文章可以使用 Markdig 功能，例如：

- 备注块
- 包含文件
- 选择器
- 嵌入视频
- 代码片段/示例

如需完整列表，请参阅目录中的“Markdig 和 Markdown 扩展”以及“代码片段”。

### <a name="note-blocks"></a>备注块

可以从 4 种类型的备注块中进行选择来吸引对特定内容的注意：

- 注意
- 警告
- 提示
- 重要说明

总之，应谨慎使用备注块，因为它们可能会造成干扰。 尽管备注块也支持代码块、图像、列表以及链接，但最好尽量保持备注块简单明了。

### <a name="includes"></a>包含文件

如果有需要加入文章文件中的可重用的文本或图像文件，可以通过 Markdig 文件的包含文件功能使用对“包含”文件的引用。 此功能指示 OPS 在创建时将该文件加入文章文件中，使它成为已发布文章的一部分。 有 3 种类型的包含功能可帮助你重用内容：

- 内联：重用内联在其他句子中的常用文本片段。
- 块：将整个 Markdown 文件作为一个块来重用，嵌套在文章的某一部分中。
- 图像：此方法可以在 Doc 中实现标准图像加入。

“内联”和“块”包含文件是简单的 Markdown (.md) 文件。 它可以包含任何有效的 Markdown。 所有包含 Markdown 文件都应置于存储库根目录的[常用 `/includes` 子目录](git-github-fundamentals.md#includes-subdirectory) 中。 发布文章时，加入的文件会无缝集成到其中。

包含文件的要求和注意事项如下：

- 无论何时需要使相同的文本显示在多篇文章中，均可使用包含功能。
- 块包含文件用于大篇幅内容，比如一个或者两个段落、共享过程或者共享章节。 请勿将它们用于小于一个句子的内容。
- 包含文件不会在你文章的 GitHub 渲染视图中显示，因为它们依赖于 Markdig 扩展。 它们在发布后才会显示。
- 确保包含文件中的所有文本都是完整的句子或者段落，并且与引用包含文件的文章的前后文没有关联。 如果不遵循此指导原则，则会在文章中创建无法转换的字符串，进而破坏本地化体验。
- 请勿将包含文件嵌入其他包含文件中。 不支持此操作。
- 将媒体文件置于特定于包含文件子目录的媒体文件夹中，例如，`<repo>`/includes/媒体文件夹。 媒体目录不应在根目录中包含任何图片。 如果包含文件不包含图像，则不需要相应的媒体目录。
- 对于常规文章，请勿在各包含文件之间共享媒体。 对于每个包含文件和文章，请使用具有唯一名称的单独文件。 将媒体文件存储在与包含文件关联的媒体文件夹中。
- 请勿将包含文件用作文章的唯一内容。  包含文件主要用作文章其余内容的补充内容。

### <a name="selectors"></a>选择器

当你创作具有多种风格的同一篇技术文章时，请在文章中使用选择器，从而跨技术或平台解决实现上的差异。 通常，这最适用于开发人员的移动平台内容。 Markdig 中目前有两种类型的选择器，单选择器和多选择器。

由于选择的每篇文章中都会出现相同的选择器 Markdown，因此建议将文章的选择器放在一个包含文件中。 然后，可以在使用相同选择器的所有文章中引用该包含文件。

### <a name="code-snippets"></a>代码片段

Markdig 支持通过代码片段扩展以一种高级方式将代码加入文章中。 它提供了一种高级的呈现方式，这种方式基于 GFM 功能（例如编程语言选择和语法着色）以及以下一些出色的功能生成：

- 通过外部存储库加入集中式代码示例/片段。
- 选项卡式 UI，可采用不同语言显示多个版本的代码示例。

## <a name="gotchas-and-troubleshooting"></a>难题和故障排除

### <a name="alt-text"></a>替换文字

无法正确显示带下划线的替换文字。 例如，与使用以下下划线相比：

```markdown
![ADextension_2FA_Configure_Step4](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

转义下划线，如下所示：

```markdown
![ADextension\_2FA\_Configure\_Step4](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

### <a name="apostrophes-and-quotation-marks"></a>撇号和引号

如果将文本从 Word 复制到 Markdown 编辑器，文本可能包含“弯”撇号或弯引号。 需要将这些内容编码或更改为基本撇号或单引号。
否则，在发布文件时，最终将得到：Itâ€™s

下面是关于这些“弯”版本标点符号的编码：

- 左（开）引号：`&#8220;`
- 右（闭）引号：`&#8221;`
- 右单（闭）引号/撇号：`&#8217;`
- 左单（开）引号（很少使用）：`&#8216;`

### <a name="angle-brackets"></a>尖括号

通常使用尖括号来表示占位符。 在文本（而不是代码）中执行此操作时，必须对尖括号进行编码。 否则，Markdown 会认为它们是一个 HTML 标记。

例如，将 `<script name>` 编码为 `&lt;script name&gt;`

## <a name="see-also"></a>另请参阅：

### <a name="markdown-resources"></a>Markdown 资源

- [Markdown 简介](https://daringfireball.net/projects/markdown/syntax)
- [Docs Markdown 备忘单](./media/documents/markdown-cheatsheet.pdf?raw=true)
- [GitHub 的 Markdown 基础知识](https://help.github.com/articles/markdown-basics/)
- [Markdown 指南](https://www.markdownguide.org/)
