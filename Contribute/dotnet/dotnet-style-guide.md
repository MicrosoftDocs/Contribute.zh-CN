---
title: 适用于 .NET 文章的模板和速查表
description: 本文包含一个便捷的模板，可用于针对 .NET 文档存储库创建新文章
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
ms.date: 11/07/2018
ms.openlocfilehash: 15288ccb1831e994fd078f47788ad4c2f502775c
ms.sourcegitcommit: 92d06515af1d9d0e5abf632fc3b6425c487174d5
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/21/2020
ms.locfileid: "90837203"
---
# <a name="metadata-and-markdown-template-for-net-docs"></a>适用于 .NET 文档的元数据和 Markdown 模板

此 dotnet/docs 模板包含 Markdown 语法的示例，以及有关设置元数据的指导。

创建 Markdown 文件时，需要将包括的模板复制到新文件，按如下所示填充元数据，并将上面的 H1 标题设为文章的标题。

## <a name="metadata"></a>元数据

所需的元数据块位于以下示例元数据块中：

```markdown
---
title: [ARTICLE TITLE]
description: [usually a summary of your first paragraph. It gets displayed in search results, and can help drive the correct traffic if well written.]
author: [GITHUB USERNAME]
ms.date: [CREATION/UPDATE DATE - mm/dd/yyyy]
---
# The H1 should not be the same as the title, but should describe the article contents
```

- 冒号 (:) 和元数据元素值之间必须有空格。
- 值（例如，标题）中的冒号可中断元数据分析器。 在此情况下，使用双引号将标题括起来（例如，`title: "Writing .NET Core console apps: An advanced step-by-step guide"`）。
- **标题**：在搜索引擎结果中显示。 该标题不应与 H1 标题中的标题相同，并且应包含不超过 60 个字符。
- **说明**：概括文章的内容。 它通常在搜索结果页中显示，并且不用于搜索排名。 它的长度应为 115-145 个字符（含空格）。
- **作者**：“作者”字段应包含作者的 GitHub 用户名。
- **ms.date**：上一次重要更新的日期。 如果已评审和更新整篇文章，请在现有文章中更新此内容。 不保证更新拼写错误或类似的小修复。

其他元数据附加于每篇文章，但我们通常在文件夹级别应用大多数元数据值，如 docfx.json 中所示。

## <a name="basic-markdown-gfm-and-special-characters"></a>基本 Markdown、GFM 和特殊字符

可在 [Markdown 引用](../markdown-reference.md)一文中了解 Markdown、GitHub Flavored Markdown (GFM) 和 OPS 特定扩展的基础知识。

Markdown 使用特殊字符（例如，\*、\` 和 \#）进行格式设置。 如果要在内容中包括其中一个字符，必须执行以下两项操作之一：

- 在特殊字符前面放一个反斜杠，进行“转义”（例如 `\*` 表示 \*）。
- 对字符使用 [HTML 实体代码](http://www.ascii.cl/htmlcodes.htm)（例如，`&#42;` 表示 &#42;）。

## <a name="file-names"></a>文件名

文件名使用以下规则：

* 仅包含小写字母、数字和连字符。
* 不使用空格或标点符号字符。 使用连字符分隔文件名中的单词和数字。
* 使用特定的行为动词，如开发、购买、构建和故障排除。 不使用后缀是 ing 的单词。
* 不使用小词汇 - 不包含 a、and、the、in 或 or 等。
* 必须在 Markdown 中且使用 .md 文件扩展名。
* 使文件名尽量简短，且适当合理。 此名称会包含在文章的 URL 中。

## <a name="headings"></a>标题

使用句式大写。 始终大写标题的第一个字词。

## <a name="text-styling"></a>文本样式

*斜体*\
用于文件、文件夹、路径（对于较长项，拆分成其自己的行）、新术语。

**粗体**\
用于 UI 元素。

`Code`\
用于内联代码、语言关键字、NuGet 包名称、命令行命令、数据库表和列名称，以及不希望可单击的 URL。

## <a name="links"></a>链接

请参阅有关[链接](../how-to-write-links.md)的一般性文章，了解有关定位标记、内部链接、其他文档链接、代码包含和外部链接的信息。

.NET 文档团队使用以下约定：

- 在大多数情况下，我们使用相对链接，并且不鼓励在链接中使用 `~/` GitHub 上的源进行解析。 然而，每当我们链接到独立存储库中的文件时，都会使用 `~/` 字符提供路径。 因为独立存储库中的文件位于 GitHub 中的不同位置，因此使用相对链接无法正确解析，无论其编写方式如何。
- C# 语言规范和 Visual Basic 语言规范通过来自语言存储库中的源，包括在 .NET 文档中。 Markdown 源托管于 [csharplang](https://github.com/dotnet/csharplang) 和 [vblang](https://github.com/dotnet/vblang) 存储库中。

规范的链接必须指向其中包括这些规范的源目录。 对于 C#，它是 ~/_csharplang/spec，而对于 VB，它是 ~/_vblang/spec如下例所示 ：

```markdown
[C# Query Expressions](~/_csharplang/spec/expressions.md#query-expressions)
```

### <a name="links-to-apis"></a>链接到 API

生成系统具有一些扩展，使我们能够链接到 .NET API，而无需使用外部链接。 可以使用下列语法之一：

1. 自动链接：`<xref:UID>` 或 `<xref:UID?displayProperty=nameWithType>`

   `displayProperty` 查询参数生成完全限定的链接文本。 默认情况下，链接文本仅显示成员名称或类型名称。

2. Markdown 链接：`[link text](xref:UID)`

   用于自定义显示的链接文本。

示例：

- `<xref:System.String>` 呈现为 [String](https://docs.microsoft.com/dotnet/api/system.string)
- `<xref:System.String?displayProperty=nameWithType>` 呈现为 [System.String](https://docs.microsoft.com/dotnet/api/system.string)
- `[String class](xref:System.String)` 呈现为 [String 类](https://docs.microsoft.com/dotnet/api/system.string)

若要详细了解如何使用此表示法，请参阅[使用交叉引用](https://dotnet.github.io/docfx/tutorial/links_and_cross_references.html#using-cross-reference)。

某些 UID 包含特殊字符 \`、\# 或 \*，需要对 UID 值执行 HTML 编码，分别编码为 `%60`、`%23` 和 `%2A`。 虽然有时会发现括号也被编码，但对此并不作要求。

示例：

- System.Threading.Tasks.Task\`1 变为 `System.Threading.Tasks.Task%601`
- System.Exception.\#ctor 变为 `System.Exception.%23ctor`
- System.Lazy\`1.\#ctor(System.Threading.LazyThreadSafetyMode) 变为 `System.Lazy%601.%23ctor%28System.Threading.LazyThreadSafetyMode%29`

可以在 `https://xref.docs.microsoft.com/autocomplete` 中查找类型的 UID、成员重载列表或特定的重载成员。 查询字符串 `?text=*\<type-member-name>*` 可标识要查看其 UID 的类型或成员。 例如，`https://xref.docs.microsoft.com/autocomplete?text=string.format` 将检索 [String.Format](https://docs.microsoft.com/dotnet/api/system.string.format) 重载。 该工具可在 UID 的任意部分中搜索提供的 `text` 查询参数。 例如，可以搜索成员名称 (ToString)、部分成员名称 (ToStri)、类型和成员名称 (Double.ToString) 等。

如果在 UID 后面添加 \*（或 `%2A`），该链接则表示重载页面，而不是特定 API。 例如，若要通过一般方式链接到 [List\<T>.BinarySearch 方法](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1.binarysearch)页面，而不是通过 [List\<T>.BinarySearch(T, IComparer\<T>)](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1.binarysearch#System_Collections_Generic_List_1_BinarySearch__0_) 等特定重载，可以使用它。 此外，如果未重载成员，还可以使用 \* 链接到成员页，这可消除在 UID 中包括参数列表的需求。

若要链接到特定的方法重载，必须包括每个方法参数的完全限定的类型名称。 例如，\<xref:System.DateTime.ToString> 链接到无参数 [DateTime.ToString](https://docs.microsoft.com/dotnet/api/system.datetime.tostring#System_DateTime_ToString) 方法，而 \<xref:System.DateTime.ToString(System.String,System.IFormatProvider)> 链接到 [DateTime.ToString(String,IFormatProvider)](https://docs.microsoft.com/dotnet/api/system.datetime.tostring#System_DateTime_ToString_System_String_System_IFormatProvider_) 方法。

若要链接到泛型类型（例如 [System.Collections.Generic.List\<T>](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1)），可使用 \` (`%60`) 字符，其后紧跟泛型类型参数的数量。 例如，`<xref:System.Nullable%601>` 可链接到 [System.Nullable\<T>](https://docs.microsoft.com/dotnet/api/system.nullable-1) 类型，而 `<xref:System.Func%602>` 可链接到 [System.Func\<T,TResult>](https://docs.microsoft.com/dotnet/api/system.func-2) 委托。

## <a name="code"></a>代码

包括代码的最佳方式是包括工作示例中的代码片段。 请遵循[参与 .NET](dotnet-contribute.md#contribute-to-samples) 一文中的说明，创建示例。 包含来自完整程序的代码片段可确保所有代码通过持续集成 (CI) 系统运行。 然而，如果需要显示导致编译时或运行时错误的内容，可以使用内联代码块。

有关在文档中显示代码的 Markdown 语法的信息，请参阅[如何在文档中包含代码](../code-in-docs.md)。

## <a name="images"></a>图像

### <a name="static-image-or-animated-gif"></a>静态图像或动态 GIF

```markdown
![this is the alt text](../images/Logo_DotNet.png)
```

### <a name="linked-image"></a>链接图像

```markdown
[![alt text for linked image](../images/Logo_DotNet.png)](https://dot.net)
```

## <a name="videos"></a>视频

目前，可使用以下语法，同时嵌入 Channel 9 和 YouTube 视频：

### <a name="channel-9"></a>Channel 9

```markdown
> [!VIDEO <channel9_video_link>]
```

若要获取视频的正确 URL，请选择视频框架下方的“嵌入”，然后复制 `<iframe>` 元素中的 URL。 例如：

```markdown
> [!VIDEO https://channel9.msdn.com/Blogs/dotnet/NET-Core-20-Released/player]
```

### <a name="youtube"></a>YouTube

若要获取视频的正确 URL，右键单击视频，选择“复制嵌入代码”，然后复制 `<iframe>` 元素中的 URL。

```markdown
> [!VIDEO <youtube_video_link>]
```

例如：

```markdown
> [!VIDEO https://www.youtube.com/embed/Q2mMbjw6cLA]
```

## <a name="docsmicrosoft-extensions"></a>docs.microsoft 扩展

docs.microsoft 可提供 GitHub Flavored Markdown 的一些额外扩展。

### <a name="checked-lists"></a>核对清单

自定义样式适用于列表。 可呈现带绿色复选标记的列表。

```markdown
> [!div class="checklist"]
> * How to create a .NET Core app
> * How to add a reference to the Microsoft.XmlSerializer.Generator package
> * How to edit your MyApp.csproj to add dependencies
> * How to add a class and an XmlSerializer
> * How to build and run the application
```

这将呈现为：

> [!div class="checklist"]
> * 如何创建 .NET Core 应用
> * 如何添加 Microsoft.XmlSerializer.Generator 包引用
> * 如何编辑 MyApp.csproj，以添加依赖项
> * 如何添加类和 XmlSerializer
> * 如何生成并运行应用程序

可在 [.NET Core 文档](https://docs.microsoft.com/dotnet/core/additional-tools/xml-serializer-generator)中查看有效的核对清单示例。

### <a name="buttons"></a>按钮

按钮链接：

```markdown
> [!div class="button"]
> [button links](dotnet-contribute.md)
```

这将呈现为：

> [!div class="button"]
> [按钮链接](dotnet-contribute.md)

可在 [Visual Studio 文档](https://docs.microsoft.com/visualstudio/install/install-visual-studio#step-2---download-visual-studio)中查看有效的按钮示例。

### <a name="step-by-steps"></a>分步操作

```markdown
>[!div class="step-by-step"]
> [Pre](../docs/csharp/expression-trees-interpreting.md)
> [Next](../docs/csharp/expression-trees-translating.md)
```

可在 [C# 指南](https://docs.microsoft.com/dotnet/csharp/tour-of-csharp/program-structure)中查看有效的分步操作示例。
