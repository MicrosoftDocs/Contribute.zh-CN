---
title: OPS 和 docs.microsoft.com 的 Markdown 引用
description: OPS 平台指南，介绍 Markdown 和 DocFX Flavored Markdown (DFM) 扩展。
author: meganbradley
ms.author: mbradley
manager: jemash
ms.date: 05/18/2018
ms.topic: contributor-guide
ms.prod: non-product-specific
audience: internal,external
ms.openlocfilehash: 64921bacf48e638221048db4b24e1a941f1d2777
ms.sourcegitcommit: 44eb4f5ee65c1848d7f36fca107b296eb7687397
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/13/2018
ms.locfileid: "51609536"
---
# <a name="markdown-reference-for-ops"></a>OPS 的 Markdown 引用

Markdown 是一种轻型标记语言，采用纯文本格式语法。 Open Publishing Services (OPS) 支持 Markdown 的 CommonMark 标准，以及一些旨在为 docs.microsoft.com 提供更丰富内容的自定义 Markdown 扩展。 本文介绍在 OPS 中为 docs.microsoft.com 使用 Markdown 的字母顺序引用。

可以使用任何文本编辑器创作 Markdown。 对于可同时插入标准 Markdown 语法和自定义 OPS 扩展的编辑器，建议使用已安装 [ 创作包](https://aka.ms/DocsAuthoringPack)的 [VS Code](https://code.visualstudio.com/)。

OPS 已为所有新存储库对 Markdig 进行标准化，且旧存储库将迁移到 Markdig。 可在 [https://babelmark.github.io/](https://babelmark.github.io/) 测试 Markdig 与其他引擎中的 Markdown 渲染效果。

## <a name="alerts-note-tip-important-caution-warning"></a>警报（备注、提示、重要提示、提醒、警告）

警报特定于 OPS 的 Markdown 扩展，用于创建在 docs.microsoft.com 上呈现的块引用，其中包含指示内容重要性的颜色和图标。 支持以下警报类型：

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
> 用户即使略读也应注意到的信息。

> [!TIP]
> 帮助用户取得更佳成果的可选信息。

> [!IMPORTANT]
> 用户成功必需的基本信息。

> [!CAUTION]
> 操作可能造成的消极后果。

> [!WARNING]
> 操作必然造成的危险后果。

## <a name="code-snippets"></a>代码片段

可在 Markdown 文件中嵌入代码片段：

```markdown
[!code-<language>[<name>](<codepath><queryoption><queryoptionvalue> "<title>")]
```

## <a name="headings"></a>标题

OPS 支持 6 级 Markdown 标题：

```markdown
# This is a first level heading (H1)

## This is a second level heading (H2)

...

###### This is a sixth level heading (H6)
```

- 最后一个 `#` 和标题文本之间必须有空格。
- 每个 Markdown 文件必须有，且仅有一个 H1。
- H1 必须是 YML 元数据块之后的文件中的第一个内容。
- H2 将自动显示在已发布文件右侧的导航菜单中。 而后的低级标题则不会显示，因此策略性地使用 H2 可帮助读者进行内容导航。
- 不建议使用 HTML 标题（如 `<h1>`），它们在某些情况下会导致出现生成警告。
- 可通过[书签](#bookmark-links)链接到文件中的各个标题。

## <a name="html"></a>HTML

虽然 Markdown 支持内联式 HTML，但不建议通过 OPS 发布 HTML，除了数量有限的一系列值以外，其他值会导致生成错误或警告。 <!--For more information, see HTML Whitelist. // do we want to add the whitelist? -->

## <a name="images"></a>图像

用于包含图像的语法是：

```markdown
![[alt text]](<folderPath>)

Example:
![alt text for image](../images/Introduction.png)
```

其中 `alt text` 是图像的简短说明，`<folder path>` 是图像的相对路径。 视觉障碍用户的屏幕阅读器需采用替换文字。 如果出现图像无法呈现的站点 bug，替换文字也非常有用。

图像应存储于文档集内的 `/media` 文件夹中。 默认支持以下文件类型的图像：

- .jpg
- .png

可通过将其他图像类型作为资源添加到文档集的 docfx.json文件中 <!--add link to reference when available-->，添加对它们的支持。

## <a name="links"></a>链接

大多数情况下，OPS 使用指向其他文件和页面的标准 Markdown 链接。 以下各小节将介绍各链接类型。

> [!TIP]
> 适用于 VS Code 的 Docs 创作包有助于正确插入相关链接和书签，免去了寻找路径的麻烦！

> [!IMPORTANT]
> 请勿在 Microsoft 站点链接中添加区域设置代码（如 zh-cn）。 硬编码的区域设置代码会导致本地化内容无法呈现，这对采用其他区域设置的用户而言是糟糕的客户体验，并将产生高昂的本地化成本。 复制浏览器中的 URL 时，默认包括区域设置代码，因此在创建链接时，需手动将其删除。 例如，使用：
>
> `[Microsoft](https://www.microsoft.com)`
>
> Not：
>
> `[Microsoft](https://www.microsoft.com/en-us/)`

### <a name="relative-links-to-files-in-the-same-doc-set"></a>同一文档集中的文件的相对链接

相对路径是指相对于当前文件的目标文件路径。 在 OPS 中，可使用相对路径链接到同一文档集中的其他文件。 相对路径的语法如下：

```markdown
[link text](../../folder/filename.md)
```

其中，`../` 指示层次结构中的上一层级。

- 相对路径将在生成过程中解析，包括删除 .md 扩展名。
- 可使用“../”链接到父文件夹中的文件，但该文件必须位于同一文档集。 不能使用“../”链接到其他文档集文件夹中的文件。
- OPS 还支持以“~”开头的特殊形式的相对路径（例如，~/foo/bar.md）。 此语法表示相对于文档集根文件夹的文件。 此类路径也将在生成过程中进行验证和解析。

> [!IMPORTANT]
> 包括相对路径中的文件扩展名。 生成可验证该相对路径的目标文件是否存在。 如果相对路径不包括文件扩展名，生成很可能会报告断开的链接警告。 例如，使用：
>
> `[link text](../../folder/filename.md)`
>
> Not：
>
> `[link text](../../folder/filename)`

### <a name="absolute-links-to-other-files-in-ops"></a>OPS 中其他文件的绝对链接

```markdown
[Azure and Linux](/articles/virtual-machines/linux/overview)
```

请勿包括文件扩展名 (.md)。 这将链接到 Azure“文章”文档集外的 Linux 概述文件。

### <a name="links-to-external-sites"></a>外部站点链接

```markdown
[Microsoft](https://www.microsoft.com)
```

其他网页基于 URL 的链接（必须包括 https://）。

### <a name="bookmark-links"></a>书签链接

同一存储库中其他文件标题的书签链接：

```markdown
[Managed Disks](../../linux/overview.md#managed-disks)
```

当前文件标题的书签链接：

```markdown
[Managed Disks](#managed-disks)
```

使用哈希标记，后跟标题文字（需删除标点符号，并用短划线替换空格）。

### <a name="explicit-anchor-links"></a>显式定位标记链接

使用 `<a>` HTML 标记的显式定位标记链接并非必需，也不推荐使用，但在中心和登录页面中除外。 在常规 Markdown 文件中使用上述书签。 对于中心和登录页面，使用如下所示的定位标记：

`## <a id="AnchorText"> </a>Header text` 或 `## <a name="AnchorText"> </a>Header text`

若要链接到显式定位标记，请使用以下语法：

```markdown
To go to a section on the same page:
[text](#AnchorText)

To go to a section on another page.
[text](FileName.md#AnchorText)
```

### <a name="xref-cross-reference-links"></a>XREF（交叉引用）链接

若要链接到当前文档集或其他文档集中自动生成的 API 参考页，请使用具有唯一 ID (UID) 的 XREF 链接。

> [!NOTE]
> 若要引用其他文档集中的 API 参考页，需要在 `docfx.json` 文件中添加 `xrefService` 配置。
> ```
> "build": {
>   ...
>   "xrefService": [ "https://xref.docs.microsoft.com/query?uid={uid}" ]
> }
> ```

UID 等同于完全限定的类名称和成员名称。 如果在 UID 后面添加 *，该链接则表示重载页面，而不是特定 API。 例如，使用 `List<T>.BinarySearch*` 链接到 BinarySearch 方法页，而不是链接到特定重载（如 `List<T>.BinarySearch(T, IComparer<T>)`）。

可使用下列某一语法：

- 自动链接：`<xref:UID> or <xref:UID?displayProperty=nameWithType>`

  可选的 `displayProperty` 查询参数生成完全限定的链接文本。 默认情况下，链接文本仅显示成员名称或类型名称。

- Markdown 链接：`[link text](xref:UID)`
  
  用于自定义显示的链接文本。

示例：

- `<xref:System.String>` 呈现为“String”。
- `<xref:System.String?displayProperty=nameWithType>` 呈现为“System.String”。
- `[String class](xref:System.String)` 呈现为“String 类”。

暂无法轻松查找 UID。 <!-- ? -->查找 API UID 的最佳方法是，查看要链接到的 API 页面的源，并查找 ms.assetid 值。 源中不显示各个重载值。 今后，我们将努力开发更优质的系统。

如果 UID 包含特殊字符 \`、\# 或 \*，必须对 UID 值执行 HTML 编码，分别编码为 `%60`、`%23` 和 `%2A`。 虽然有时会发现括号也被编码，但对此并不作要求。

示例：

- System.Threading.Tasks.Task\`1 变为 `System.Threading.Tasks.Task%601`
- System.Exception.\#ctor 变为 `System.Exception.%23ctor`
- System.Lazy\`1.\#ctor(System.Threading.LazyThreadSafetyMode) 变为 `System.Lazy%601.%23ctor%28System.Threading.LazyThreadSafetyMode%29`

<!-- leave out of Contributor Guide for now
Using XREF may require some configuration. For more information, see XREF Service.
-->

## <a name="lists-numbered-bulleted-checklist"></a>列表（带编号、显示项目符号、清单）

### <a name="numbered-list"></a>编号列表

若要创建编号列表，可全部使用 1，它们将在发布时呈现为有序列表。 为提高源可读性，可增加列表。

请勿在列表中使用字母，也勿使用嵌套列表。 通过 OPS 发布时，它们无法正确呈现。 使用编号的嵌套列表在发布时将呈现为小写字母。 例如：

```markdown
1. This is
1. a parent numbered list
   1. and this is
   1. a nested numbered list
1. (fin)
```

这将呈现为：

1. 这是
1. 一个父级编号列表
   1. 而这是
   1. 一个嵌套编号列表
1. (fin)

### <a name="bulleted-list"></a>项目符号列表

若要创建项目符号列表，请使用 `-`，其后每行开头跟一个空格：

```markdown
- This is
- a parent bulleted list
  - and this is
  - a nested bulleted list
- All done!
```

这将呈现为：

- 这是
- 一个父级项目符号列表
  - 而这是
  - 一个嵌套项目符号列表
- 全部完成！

### <a name="checklist"></a>清单

清单仅可通过自定义 Markdown 扩展在 docs.microsoft.com 上使用：

```markdown
> [!div class="checklist"]
> * List item 1
> * List item 2
> * List item 3
```

此示例在 docs.microsoft.com 上呈现为：

> [!div class="checklist"]
> * 列表项目 1
> * 列表项目 2
> * 列表项目 3

在文章开头或结尾使用清单，总结“将要学习的内容”或“所学内容”。 请勿在整篇文章中添加随机清单。
<!-- is this guidance still accurate? -->

## <a name="next-step-action"></a>下一步操作

可使用自定义扩展在 docs.microsoft.com（仅限用于此站点）页面上添加下一步操作按钮。

语法如下所示：

```markdown
> [!div class="nextstepaction"]
> [button text](link to topic)
```

例如：

```markdown
> [!div class="nextstepaction"]
> [Learn about basic style](style-quick-start.md)
```

这将呈现为：

> [!div class="nextstepaction"]
> [了解基本样式](style-quick-start.md)

可在下一步操作中使用任何受支持的链接，包括指向其他网页的 Markdown 链接。 在大多数情况下，下一操作链接是同一文档集中另一个文件的相对链接。

## <a name="section-definition"></a>节定义

<!-- more info about this would be helpful! -->可能需要定义节。 这种语法最常用于代码表。
请参阅以下示例：

````
> [!div class="tabbedCodeSnippets" data-resources="OutlookServices.Calendar"]
> ```cs
> <cs code text>
> ```
> ```javascript
> <js code text>
> ```
````

前面的块引用 Markdown 文本将呈现为：
> [!div class="tabbedCodeSnippets" data-resources="OutlookServices.Calendar"]
> ```cs
> <cs code text>
> ```
> ```javascript
> <js code text>
> ```

## <a name="selectors"></a>选择器

<!-- could be more clear! -->要连接同一文章的不同页面，可使用选择器。 如此，读者即可在这些页面之间切换。

> [!NOTE]
> 此扩展在 docs.microsoft.com 和 MSDN 中的作用不同。 <!-- should we keep info about MSDN? If so say how they differ?-->

### <a name="single-selector"></a>单一选择器

```
> [!div class="op_single_selector"]
> - [Universal Windows](how-to-write-use-markdown.md)
> - [Windows Phone](how-to-write-use-markdown.md)
> - [iOS](how-to-write-use-markdown.md)
> - [Android](how-to-write-use-markdown.md)
> - [Kindle](how-to-write-use-markdown.md)
> - [Baidu](how-to-write-use-markdown.md)
> - [Xamarin.iOS](how-to-write-use-markdown.md)
> - [Xamarin.Android](how-to-write-use-markdown.md)
```

... 将呈现为：

> [!div class="op_single_selector"]
> - [通用 Windows](how-to-write-use-markdown.md)
> - [Windows Phone](how-to-write-use-markdown.md)
> - [iOS](how-to-write-use-markdown.md)
> - [Android](how-to-write-use-markdown.md)
> - [Kindle](how-to-write-use-markdown.md)
> - [百度](how-to-write-use-markdown.md)
> - [Xamarin.iOS](how-to-write-use-markdown.md)
> - [Xamarin.Android](how-to-write-use-markdown.md)

### <a name="multi-selector"></a>多重选择器

```
> [!div class="op_multi_selector" title1="Platform" title2="Backend"]
> - [(iOS | .NET)](how-to-write-workflows-major.md)
> - [(iOS | JavaScript)](how-to-write-workflows-major.md)
> - [(Windows universal C# | .NET)](how-to-write-workflows-major.md)
> - [(Windows universal C# | Javascript)](how-to-write-workflows-major.md)
> - [(Windows Phone | .NET)](how-to-write-workflows-major.md)
> - [(Windows Phone | Javascript)](how-to-write-workflows-major.md)
> - [(Android | .NET)](how-to-write-workflows-major.md)
> - [(Android | Javascript)](how-to-write-workflows-major.md)
> - [(Xamarin iOS | Javascript)](how-to-write-workflows-major.md)
> - [(Xamarin Android | Javascript)](how-to-write-workflows-major.md)
```

... 将呈现为：

> [!div class="op_multi_selector" title1="Platform" title2="Backend"]
> - [(iOS | .NET)](how-to-write-workflows-major.md)
> - [(iOS | JavaScript)](how-to-write-workflows-major.md)
> - [(Windows 通用 C# | .NET)](how-to-write-workflows-major.md)
> - [(Windows 通用 C# | Javascript)](how-to-write-workflows-major.md)
> - [(Windows Phone | .NET)](how-to-write-workflows-major.md)
> - [(Windows Phone | Javascript)](how-to-write-workflows-major.md)
> - [(Android | .NET)](how-to-write-workflows-major.md)
> - [(Android | Javascript)](how-to-write-workflows-major.md)
> - [(Xamarin iOS | Javascript)](how-to-write-workflows-major.md)
> - [(Xamarin Android | Javascript)](how-to-write-workflows-major.md)

<!-- uncomment and link when Cory's topic is live
## Tabbed content

Tabs are a Markdown extension for docs.microsoft.com that allow us to present different versions of content, such as procedural steps to accomplish the same task on different platforms, in a tabbed format.

Because the syntax and requirements for tabbed content are fairly complex, they are documented separately in Tabbed Content.
-->

## <a name="tables"></a>表格

使用 Markdown 创建表的最简单方法是借助垂直线和行。 若要创建带标头的标准表格，请在第一行后使用虚线：

```markdown
|This is   |a simple   |table header|
|----------|-----------|------------|
|table     |data       |here        |
|it doesn't|actually   |have to line up nicely!|
```

这将呈现为：

|这是   |简单的   |表格标头|
|----------|-----------|------------|
|表格     |数据       |此处        |
|它不需要|确实   |完美对齐！||

此外，还可创建不含标头的表格。 例如，创建多列列表：

```markdown
|   |   |
| - | - |
| This | table |
| has no | header |
```

这将呈现为如下所示：

|   |   |
| - | - |
| 此 | 表格 |
| 没有 | 标头 |

可使用冒号来对齐列：

```markdown
|                  |
|------------------|
|    right aligned:|
|:left aligned     |
|:centered        :|
```

呈现为：

|                  |
|------------------|
|    右对齐:|
|:左对齐     |
|:居中:|

> [!TIP]
> 使用 VS Code 的 Docs 创作扩展，可轻松添加基本 Markdown 表格！
>
> 此外，还可使用[联机表格生成器](http://www.tablesgenerator.com/markdown_tables)。

### <a name="mx-tdbreakall"></a>mx-tdBreakAll

> [!IMPORTANT]
> 这仅在 docs.microsoft.com 站点上可用。

如果使用 Markdown 创建表，表可能会扩展到右侧导航栏，导致表不可读。 要解决此问题，请允许文档呈现时根据需要对表格换行。 只需使用自定义类 `[!div class="mx-tdBreakAll"]` 即可实现表格换行。

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

### <a name="mx-tdcol2breakall"></a>mx-tdCol2BreakAll

> [!IMPORTANT]
> 这仅在 docs.microsoft.com 站点上可用。

有时，表中第二列里的字数可能过长。 要确保它们能正确换行，可使用 `div` 包装语法应用 `mx-tdCol2BreakAll` 类，其操作方法如前面所述。

### <a name="html-tables"></a>HTML 表

不建议将 HTML 表用于 docs.microsoft.com。 它们在源中无法为人所理解，而这是 Markdown 的关键原则。

<!--If you use HTML tables and your Markdown is not being rendered between the two tables, you need to add a closing `br` tag after the closing `table` tag.

![break HTML tables](media/break-tables.png)
-->

## <a name="videos"></a>视频

### <a name="embedding-videos-into-a-markdown-page"></a>将视频嵌入 Markdown 页面

目前，OPS 支持以下 3 个站点中发布的视频：

- YouTube
- Channel 9
- Microsoft 自己的“One Playe”系统

可使用以下语法嵌入视频，然后 OPS 将呈现它。

```markdown
> [!VIDEO <embedded_video_link>]
```

示例：

```markdown
> [!VIDEO https://channel9.msdn.com/Series/Youve-Got-Key-Values-A-Redis-Jump-Start/03/player]

> [!VIDEO https://www.youtube.com/embed/iAtwVM-Z7rY]

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS]
```

... 将显示为：

```html
<iframe src="https://channel9.msdn.com/Series/Youve-Got-Key-Values-A-Redis-Jump-Start/03/player" width="640" height="320" allowFullScreen="true" frameBorder="0"></iframe>

<iframe src="https://www.youtube-nocookie.com/embed/iAtwVM-Z7rY" width="640" height="320" allowFullScreen="true" frameBorder="0"></iframe>
<iframe src="https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS" width="640" height="320" allowFullScreen="true" frameBorder="0"></iframe>
```

在已发布页面上，它将显示为如下形式：

> [!VIDEO https://channel9.msdn.com/Series/Youve-Got-Key-Values-A-Redis-Jump-Start/03/player]

> [!VIDEO https://www.youtube.com/embed/iAtwVM-Z7rY]

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS]

> [!IMPORTANT]
> CH9 视频 URL 应以 `https` 开头并以 `/player` 结尾。 否则将嵌入整个页面，而不是只嵌入视频。

### <a name="uploading-new-videos"></a>上传新视频

应按照以下流程上传任何新视频：

1. 加入 IDWEB 上的 docs_video_users 组。
1. 转到 https://aka.ms/VideoUploadRequest 并填写视频的详细信息。 需填写以下内容（请注意各项内容均非公开所见）：
    1. 视频标题。
    1. 与视频相关的产品/服务列表。
    1. 承载该视频的目标页面或文档集（如果尚无页面）。
    1. 视频 MP4 文件的链接（如果没有用于放置该文件的位置，可暂时将其放于此处：`\\scratch2\scratch\apex`）。 MP4 文件应为 720p 或更高。
    1. 视频说明。
1. 提交（保存）该项。
1. 视频将在两个工作日内上传。 嵌入所需的链接将放置于工作项内，并将在解析后返回给你。
1. 获取视频链接后，关闭工作项。
1. 然后，可使用以下语法，将视频链接添加到文章中：

   ```markdown
   > [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS]
   ```
