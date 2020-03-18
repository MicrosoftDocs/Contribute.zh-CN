---
title: docs.microsoft.com 的 Markdown 引用
description: 了解 Microsoft Docs 平台中使用的 Markdown 功能和语法。
author: meganbradley
ms.author: mbradley
ms.date: 01/30/2020
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
ms.openlocfilehash: 14cc9f0912149eb342c97d0dd7d2776bd54c84e7
ms.sourcegitcommit: 804a99b89785e5c8f056a9da3f0fbde9f0a56a51
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/05/2020
ms.locfileid: "78331945"
---
# <a name="docs-markdown-reference"></a>Docs Markdown 引用

本文按字母顺序提供有关对 docs.microsoft.com (Docs) 编写 Markdown 的引用。

[Markdown](https://daringfireball.net/projects/markdown/) 是一种轻型标记语言，采用纯文本格式语法。 Docs 支持已通过 [Markdig](https://github.com/lunet-io/markdig) 分析引擎进行分析且与 [CommonMark](https://commonmark.org/) 兼容的 Markdown。 Docs 还支持在 Docs 网站上提供更丰富内容的自定义 Markdown 扩展。

可使用任何文本编辑器来编写 Markdown，但建议结合使用 [Visual Studio Code](https://code.visualstudio.com/) 和 [Docs 创作包](https://aka.ms/DocsAuthoringPack)。 Docs 创作包提供编辑工具和预览功能，让你能够查看文章呈现在 Docs 上时的外观。

## <a name="alerts-note-tip-important-caution-warning"></a>警报（备注、提示、重要提示、提醒、警告）

警报是用于创建块引用的 Markdown 扩展，这些块引用与指示内容重要性的颜色和图标共同呈现在 docs.microsoft.com 上。 支持以下警报类型：

```markdown
> [!NOTE]
> Information the user should notice even if skimming.

> [!TIP]
> Optional information to help a user be more successful.

> [!IMPORTANT]
> Essential information required for user success.

> [!CAUTION]
> Negative potential consequences of an action.

> [!WARNING]
> Dangerous certain consequences of an action.
```

这些警报在 docs.microsoft.com 上如下所示：

> [!NOTE]
> Information the user should notice even if skimming.

> [!TIP]
> Optional information to help a user be more successful.

> [!IMPORTANT]
> Essential information required for user success.

> [!CAUTION]
> Negative potential consequences of an action.

> [!WARNING]
> Dangerous certain consequences of an action.

### <a name="angle-brackets"></a>尖括号

如果在文件中的文本里使用尖括号（例如要表示占位符），则需要对尖括号手动编码。 否则，Markdown 会认为它们是一个 HTML 标记。

例如，将 `<script name>` 编码为 `&lt;script name&gt;` 或 `\<script name>`。

尖括号无需在格式为内联代码的文本中或在代码块中进行转义。

## <a name="apostrophes-and-quotation-marks"></a>撇号和引号

如果将文本从 Word 复制到 Markdown 编辑器，文本可能包含“弯”撇号或弯引号。 需要将这些内容编码或更改为基本撇号或单引号。 否则，发布文件时，最终将得到：Itâ€™s

下面是关于这些“弯”版本标点符号的编码：

- 左（开）引号：`&#8220;`
- 右（闭）引号：`&#8221;`
- 右单（闭）引号/撇号：`&#8217;`
- 左单（开）引号（很少使用）：`&#8216;`

## <a name="blockquotes"></a>块引用

块引用使用 `>` 字符创建：

```md
> This is a blockquote. It is usually rendered indented and with a different background color.
```

上述示例的呈现如下所示：

> 这是一个块引用。 它通常以缩进格式呈现，并且具有不同的背景色。

## <a name="bold-and-italic-text"></a>粗体和斜体文本

要将文本设置为粗体格式，请用两个星号括住文本  ：

```markdown
This text is **bold**.
```

要将文本设置为斜体格式，请用一个星号括住文本  ：

```markdown
This text is *italic*.
```

要将文本同时设置为粗体和斜体格式，请用三个星号括住文本：

```markdown
This text is both ***bold and italic***.
```

## <a name="code-snippets"></a>代码片段

Docs Markdown 不仅支持将代码片段内联在某个句子中，还支持将它作为单独的“隔离”块放置在两个句子之间。 有关详细信息，请参阅[如何将代码添加到文档](code-in-docs.md)。

## <a name="columns"></a>列

通过名为“列”的 Markdown 扩展，Docs 作者可添加基于列的内容布局，这些布局比基本 Markdown 表更灵活、功能更强大，而基本 Markdown 表只适用于真正的表格数据  。 最多可添加 4 列，并需使用可选的 `span` 属性来合并两个或更多列。

列的语法如下所示：

```markdown
:::row:::
   :::column span="":::
      Content...
   :::column-end:::
   :::column span="":::
      More content...
   :::column-end:::
:::row-end:::
```

列应仅包含基本的 Markdown（包括图像）。 不应包含标题、表、选项卡和其他复杂结构。 行不能包含列中没有的任何内容。

例如，以下 Markdown 创建了一个跨两个列宽的列和一个标准（无 `span`）列：

```markdown
:::row:::
   :::column span="2":::
      **This is a 2-span column with lots of text.**

      Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec vestibulum mollis nunc
      ornare commodo. Nullam ac metus imperdiet, rutrum justo vel, vulputate leo. Donec
      rutrum non eros eget consectetur.
   :::column-end:::
   :::column span="":::
      **This is a single-span column with an image in it.**

      ![Doc.U.Ment](media/markdown-reference/document.png)
   :::column-end:::
:::row-end:::
```

这将呈现为：

:::row:::
   :::column span="2":::
      这是包含大量文本的跨两列的列  。

      Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec vestibulum mollis nunc ornare commodo. Nullam ac metus imperdiet, rutrum justo vel, vulputate leo. Donec rutrum non eros eget consectetur.
   :::column-end:::
   :::column span="":::
      这是包含图像的单个列  。

      ![Doc.U.Ment](media/markdown-reference/document.png)
   :::column-end:::
:::row-end:::

## <a name="headings"></a>标题

Docs 支持六个级别的 Markdown 标题：

```markdown
# This is a first level heading (H1)

## This is a second level heading (H2)

...

###### This is a sixth level heading (H6)
```

- 最后一个 `#` 和标题文本之间必须有空格。
- 每个 Markdown 文件必须有且仅有一个 H1 标题。
- H1 标题必须是 YML 元数据块之后的文件中的第一个内容。
- H2 标题将自动显示在已发布文件右侧的导航菜单中。 而后的低级标题则不会显示，因此策略性地使用 H2 可帮助读者进行内容导航。
- 不建议使用 HTML 标题（如 `<h1>`），它们在某些情况下会导致出现生成警告。
- 可通过[书签链接](how-to-write-links.md#links-to-anchors)链接到文件中的各个标题。

## <a name="html"></a>HTML

虽然 Markdown 支持内联式 HTML，但不建议使用 HTML 将内容发布到 Docs，除了数量有限的一系列值以外，其他值会导致生成错误或警告。 

## <a name="images"></a>图像

默认支持以下文件类型的图像：

- .jpg
- .png

### <a name="standard-conceptual-images-default-markdown"></a>标准概念图像（默认 Markdown）

用于嵌入图像的基本 Markdown 语法为：

```Markdown
![<alt text>](<folderPath>)

Example:
![alt text for image](../images/Introduction.png)
```

其中 `<alt text>` 是图像的简短说明，`<folder path>` 是图像的相对路径。 视觉障碍用户的屏幕阅读器需采用替换文字。 如果出现图像无法呈现的站点 bug，替换文字也非常有用。

无法正确呈现替换文字的下划线，除非使用反斜杠 (`\_`) 作为其前缀来将它进行转义。 但是，请勿复制用作替换文字的文件名。 例如，不应编写以下内容：

```markdown
![ADextension_2FA_Configure_Step4](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

应编写以下内容：

```markdown
![Active Directory extension for two-factor authentication, step 4: Configure](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

### <a name="standard-conceptual-images-docs-markdown"></a>标准概念图像（Docs Markdown）

Docs 自定义 `:::image:::` 扩展支持标准图像、复杂图像和图标。

对于标准图像，旧的 Markdown 语法仍可用，但推荐使用新的扩展，因为它支持更强大的功能，例如指定与父主题不同的本地化范围。 将来还会提供其他高级功能（例如从共享图像库中选择，而不是指定本地图像）。 新语法如下所示：

```Markdown
:::image type="content" source="<folderPath>" alt-text="<alt text>":::
```

如果 `type="content"`（默认值），则 `source` 和 `alt-text` 都是必需的。

### <a name="complex-images-with-long-descriptions"></a>带有详细说明的复杂图像

还可使用此扩展添加带有详细说明的图像，该图像由屏幕阅读器读取，而不是直观呈现在已发布的页面上。 详细说明是复杂图像（如图形）的可访问性要求。 语法如下所示：

```Markdown
:::image type="complex" source="<folderPath>" alt-text="<alt text>":::
   <long description here>
:::image-end:::
```

如果 `type="complex"`，则 `source`、`alt-text`、详细说明和 `:::image-end:::` 标记都是必需的。

### <a name="specifying-loc-scope"></a>指定本地化范围

有时，图像的本地化范围不同于包含该图像的文章或模块的本地化范围。 这可能会导致全局体验不佳：例如，产品的屏幕截图被意外本地化为该产品不能使用的语言。 为防止出现此情况，可在类型为 `content` 和 `complex` 的图像中指定可选的 `loc-scope` 属性。

### <a name="icons"></a>图标

图像扩展支持图标（装饰性图像），且不得包含替换文字。 图标的语法如下：

```Markdown
:::image type="icon" source="<folderPath>":::
```

如果 `type="icon"`，仅应指定 `source`。

## <a name="included-markdown-files"></a>包含的 Markdown 文件

如果需要在多篇文章中重复使用 Markdown 文件，可使用包含文件。 包含功能可指示 Docs 在生成时将引用替换为包含文件的内容。 可通过以下方式使用包含文件：

- 内联：重用内联在某句子中的常用文本片段。
- 块：将整个 Markdown 文件作为一个块重用，嵌套在文章的某一部分中。

“内联”和“块”包含文件是 Markdown (.md) 文件。 它可以包含任何有效的 Markdown。 包含文件通常位于存储库根目录中的公共包含子目录中  。 发布文章时，加入的文件会无缝集成到其中。

### <a name="includes-syntax"></a>包含文件语法

块包含文件位于其自己的行上：

```markdown
[!INCLUDE [<title>](<filepath>)]
```

内联包含文件位于行中：

```markdown
Text before [!INCLUDE [<title>](<filepath>)] and after.
```

其中，`<title>` 是文件名，`<filepath>` 是该文件的相对路径。 `INCLUDE` 必须大写，并且 `<title>` 前必须有一个空格。

包含文件的要求和注意事项如下：

- 块包含文件用于大篇幅内容，比如一个或者两个段落、共享过程或者共享章节。 请勿将它们用于小于一个句子的内容。
- 包含文件不会在文章的 GitHub 呈现视图中显示，因为它们依赖于 Docs 扩展。 它们在发布后才会显示。
- 确保包含文件中的所有文本都是完整的句子或者段落，并且与引用该包含文件的文章的前后文没有关联。 如果不遵循此指导原则，则会在文章中创建无法转换的字符串。
- 请勿在其他包含文件中嵌入包含文件。
- 将媒体文件放在特定于包含文件子目录的媒体文件夹中，例如 `<repo>`/includes/media 文件夹  。 媒体目录不应在根目录中包含任何图像  。 如果包含文件不包含图像，则不需要相应的媒体目录  。
- 对于常规文章，请勿在各包含文件之间共享媒体。 对于每个包含文件和文章，请使用具有唯一名称的单独文件。 将媒体文件存储在与包含文件关联的媒体文件夹中。
- 请勿将包含文件用作文章的唯一内容。  包含文件主要用作文章其余内容的补充内容。

## <a name="links"></a>链接

要了解链接的语法，请参阅[在文档中使用链接](how-to-write-links.md)。

## <a name="lists-numbered-bulleted-checklist"></a>列表（带编号、显示项目符号、清单）

### <a name="numbered-list"></a>编号列表

要创建编号列表，可全部使用 1。 发布后，这些编号会按升序顺序呈现为顺序列表。 为提高源可读性，可手动增加列表。

请勿在列表中使用字母，也勿使用嵌套列表。 发布到 Docs 时，它们无法正确呈现。使用编号的嵌套列表在发布时将呈现为小写字母。 例如：

```markdown
1. This is
1. a parent numbered list
   1. and this is
   1. a nested numbered list
1. (fin)
```

这将呈现为：

1. This is
1. a parent numbered list
   1. and this is
   1. a nested numbered list
1. (fin)

### <a name="bulleted-list"></a>项目符号列表

若要创建项目符号列表，请使用 `-` 或 `*`，其后每行开头跟一个空格：

```markdown
- This is
- a parent bulleted list
  - and this is
  - a nested bulleted list
- All done!
```

这将呈现为：

- This is
- a parent bulleted list
  - and this is
  - a nested bulleted list
- All done!

无论使用哪种语法（`-` 或 `*`），都请在一篇文章中始终使用它。

### <a name="checklist"></a>清单

清单仅可通过自定义 Markdown 扩展在 Docs 上使用：

```markdown
> [!div class="checklist"]
> * List item 1
> * List item 2
> * List item 3
```

此示例在 Docs 上呈现为：

> [!div class="checklist"]
> * List item 1
> * List item 2
> * List item 3

在文章开头或结尾使用清单，总结“将要学习的内容”或“所学内容”。 请勿在整篇文章中添加随机清单。

## <a name="next-step-action"></a>下一步操作

可使用自定义扩展向 Docs 页面添加下一步操作按钮。

语法如下所示：

```markdown
> [!div class="nextstepaction"]
> [button text](link to topic)
```

例如：

```markdown
> [!div class="nextstepaction"]
> [Learn about adding code to articles](code-in-docs.md)
```

这将呈现为：

> [!div class="nextstepaction"]
> [了解如何向文章添加代码](code-in-docs.md)

可在下一步操作中使用任何受支持的链接，包括指向其他网页的 Markdown 链接。 在大多数情况下，下一操作链接是同一文档集中另一个文件的相对链接。

## <a name="non-localized-strings"></a>非本地化字符串

可使用自定义 `no-loc` Markdown 扩展来标识你希望在本地化过程中忽略的内容中的字符串。

所有调用的字符串都将区分大小写；即字符串必须完全匹配，才能在本地化过程中被忽略。

若要将单个字符串标记为不可本地化，请使用以下语法：

```markdown
:::no-loc text="String":::
```

例如，在以下示例中，本地化过程中只会忽略 `Document` 的单个实例：

```markdown
# Heading 1 of the Document

Markdown content within the :::no-loc text="Document":::.  The are multiple instances of Document, document, and documents.
```

> [!NOTE]
> 使用 `\` 转义特殊字符：
> ```markdown
> Lorem :::no-loc text="Find a \"Quotation\""::: Ipsum.
> ```

还可以使用 YAML 标头中的元数据将当前 Markdown 文件中字符串的所有实例标记为不可本地化：

```yml
author: cillroy
no-loc: [Global, Strings, to be, Ignored]
```

> [!NOTE]
> 在 docfx.json 文件中，不支持将不可本地化的元数据作为全局元数据  。 本地化管道不会读取 docfx.json 文件，因此必须将不可本地化的元数据添加到每个单独的源文件中  。

在下示例中，本地化过程中将同时忽略元数据 `title` 和 Markdown 标头中的 `Document` 一词。

在元数据 `description` 和 Markdown 主要内容中，会对 `document` 一词进行本地化，因此该词没有以大写的 `D` 开头。

```markdown
---
title: Title of the Document
author: author-name
description: Description for the document
no-loc: [Title, Document]
---
# Heading 1 of the Document

Markdown content within the document.
```

<!-- commenting out for now because no one knows what this means
## Section definition

You might need to define a section. This syntax is mostly used for code tables.
See the following example:

````
> [!div class="tabbedCodeSnippets" data-resources="OutlookServices.Calendar"]
> ```cs
> <cs code text>
> ```
> ```javascript
> <js code text>
> ```
````

The preceding blockquote Markdown text will be rendered as:
> [!div class="tabbedCodeSnippets" data-resources="OutlookServices.Calendar"]
> ```cs
> <cs code text>
> ```
> ```javascript
> <js code text>
> ```
-->

## <a name="selectors"></a>选择器

选择器是 UI 元素，用户可用它在同一篇文章的多种风格之间切换。 它们在某些文档集中用来解决跨技术或平台实现的差异。 选择器通常最适用于开发人员的移动平台内容。

由于使用选择器的每个文章文件中都会出现相同的选择器 Markdown，因此建议将文章的选择器放在包含文件中。 然后，可以在使用相同选择器的所有文章文件中引用该包含文件。

有两种类型的选择器：单选择器和多选择器。

### <a name="single-selector"></a>单一选择器

```markdown
> [!div class="op_single_selector"]
> - [Universal Windows](../articles/notification-hubs-windows-store-dotnet-get-started/)
> - [Windows Phone](../articles/notification-hubs-windows-phone-get-started/)
> - [iOS](../articles/notification-hubs-ios-get-started/)
> - [Android](../articles/notification-hubs-android-get-started/)
> - [Kindle](../articles/notification-hubs-kindle-get-started/)
> - [Baidu](../articles/notification-hubs-baidu-get-started/)
> - [Xamarin.iOS](../articles/partner-xamarin-notification-hubs-ios-get-started/)
> - [Xamarin.Android](../articles/partner-xamarin-notification-hubs-android-get-started/)
```

... 将呈现为：

> [!div class="op_single_selector"]
> - [Universal Windows](how-to-write-links.md)
> - [Windows Phone](how-to-write-links.md)
> - [iOS](how-to-write-links.md)
> - [Android](how-to-write-links.md)
> - [Kindle](how-to-write-links.md)
> - [Baidu](how-to-write-links.md)
> - [Xamarin.iOS](how-to-write-links.md)
> - [Xamarin.Android](how-to-write-links.md)

### <a name="multi-selector"></a>多重选择器

```markdown
> [!div class="op_multi_selector" title1="Platform" title2="Backend"]
> - [(iOS | .NET)](./mobile-services-dotnet-backend-ios-get-started-push.md)
> - [(iOS | JavaScript)](./mobile-services-javascript-backend-ios-get-started-push.md)
> - [(Windows universal C# | .NET)](./mobile-services-dotnet-backend-windows-universal-dotnet-get-started-push.md)
> - [(Windows universal C# | Javascript)](./mobile-services-javascript-backend-windows-universal-dotnet-get-started-push.md)
> - [(Windows Phone | .NET)](./mobile-services-dotnet-backend-windows-phone-get-started-push.md)
> - [(Windows Phone | Javascript)](./mobile-services-javascript-backend-windows-phone-get-started-push.md)
> - [(Android | .NET)](./mobile-services-dotnet-backend-android-get-started-push.md)
> - [(Android | Javascript)](./mobile-services-javascript-backend-android-get-started-push.md)
> - [(Xamarin iOS | Javascript)](./partner-xamarin-mobile-services-ios-get-started-push.md)
> - [(Xamarin Android | Javascript)](./partner-xamarin-mobile-services-android-get-started-push.md)
```

... 将呈现为：

> [!div class="op_multi_selector" title1="平台" title2="后端"]
> - [(iOS | .NET)](how-to-write-links.md)
> - [(iOS | JavaScript)](how-to-write-links.md)
> - [(Windows universal C# | .NET)](how-to-write-links.md)
> - [(Windows universal C# | Javascript)](how-to-write-links.md)
> - [(Windows Phone | .NET)](how-to-write-links.md)
> - [(Windows Phone | Javascript)](how-to-write-links.md)
> - [(Android | .NET)](how-to-write-links.md)
> - [(Android | Javascript)](how-to-write-links.md)
> - [(Xamarin iOS | Javascript)](how-to-write-links.md)
> - [(Xamarin Android | Javascript)](how-to-write-links.md)

## <a name="subscript-and-superscript"></a>下标和上标

应仅在要求技术准确性时使用下标或上标，例如在写数学公式时。 不要将它们用于非标准样式，如脚注。

对于下标和上标，请使用 HTML：

```html
Hello <sub>This is subscript!</sub>
```

这将呈现为：

Hello <sub>This is subscript!</sub>

```html
Goodbye <sup>This is superscript!</sup>
```

这将呈现为：

Goodbye <sup>This is superscript!</sup>

## <a name="tables"></a>表

使用 Markdown 创建表的最简单方法是借助垂直线和行。 若要创建带标头的标准表格，请在第一行后使用虚线：

```markdown
|This is   |a simple   |table header|
|----------|-----------|------------|
|table     |data       |here        |
|it doesn't|actually   |have to line up nicely!|
```

这将呈现为：

|This is   |a simple   |table header|
|----------|-----------|------------|
|table     |data       |here        |
|it doesn't|actually   |have to line up nicely!||

可使用冒号来对齐列：

```markdown
| Fun                  | With                 | Tables          |
| :------------------- | -------------------: |:---------------:|
| left-aligned column  | right-aligned column | centered column |
| $100                 | $100                 | $100            |
| $10                  | $10                  | $10             |
| $1                   | $1                   | $1              |
```

呈现为：

| Fun                  | With                 | Tables          |
| :------------------- | -------------------: |:---------------:|
| left-aligned column  | right-aligned column | centered column |
| $100                 | $100                 | $100            |
| $10                  | $10                  | $10             |
| $1                   | $1                   | $1              |

> [!TIP]
> 使用 VS Code 的 Docs 创作扩展，可轻松添加基本 Markdown 表格！
>
> 此外，还可使用[联机表格生成器](http://www.tablesgenerator.com/markdown_tables)。

### <a name="line-breaks-within-words-in-any-table-cell"></a>任何表格单元格中单词内的换行符

Markdown 中较长的单词可能会扩展到右侧导航栏，导致表不可读。 可通过允许 Docs 渲染，必要时自动在单词内插入换行符来解决此问题。 只需使用自定义类 `[!div class="mx-tdBreakAll"]` 即可实现表格换行。

下面是一个 3 行表格的 Markdown 示例，它通过使用类名为 `mx-tdBreakAll` 的 `div` 实现表格换行。

```markdown
> [!div class="mx-tdBreakAll"]
> |Name|Syntax|Mandatory for silent installation?|Description|
> |-------------|----------|---------|---------|
> |Quiet|/quiet|Yes|Runs the installer, displaying no UI and no prompts.|
> |NoRestart|/norestart|No|Suppresses any attempts to restart. By default, the UI will prompt before restart.|
> |Help|/help|No|Provides help and quick reference. Displays the correct use of the setup command, including a list of all options and behaviors.|
```

它将以如下形式呈现：

> [!div class="mx-tdBreakAll"]
> |名称|语法|是否是无提示安装所必需的？|说明|
> |-------------|----------|---------|---------|
> |Quiet|/quiet|是|在不显示 UI 且无提示的情况下运行安装程序。|
> |NoRestart|/norestart|否|禁止所有重启尝试。 重启前将默认提示 UI。|
> |Help|/help|否|提供帮助和快速引用。 显示安装命令的正确使用方法，包括一个显示全部选项和行为的列表。|

### <a name="line-breaks-within-words-in-second-column-table-cells"></a>第二列表格单元格中单词内的换行符

你可能只希望换行符自动插入到表格第二列中的单词内。 若要限制在第二列换行，请按前述所示使用 `div` 包装语法来应用类 `mx-tdCol2BreakAll`。

### <a name="html-tables"></a>HTML 表

不建议将 HTML 表用于 docs.microsoft.com。 它们在源中无法为人所理解，而这是 Markdown 的关键原则。
