---
title: 如何在文档中使用链接
description: 本文指导如何在 docs.microsoft.com 中创建内容链接。
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
author: gewarren
ms.author: gewarren
ms.date: 03/31/2020
ms.openlocfilehash: 94ba4cefd9aff70b38502aa397a3761127c8089f
ms.sourcegitcommit: 9852045bac75fd5d90c0ffc88d2a17dd45ba015f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/19/2020
ms.locfileid: "85107105"
---
# <a name="use-links-in-documentation"></a>在文档中使用链接

本文介绍如何使用 docs.microsoft.com 上托管页面的超链接。 通过几种不同的约定，便可轻松地将链接添加到 markdown。 链接将用户指向相同页面中的内容、其他相邻页面或外部站点和 URL。

docs.microsoft.com 站点后端使用开放发布服务 (OPS)，支持通过 [Markdig][] 分析引擎分析的 [CommonMark][] 兼容 Markdown。 Markdown 风格大多与 [GitHub Flavored Markdown (GFM)][GFM] 兼容，因为大多数 docs 存储在 GitHub 中，并可以在 GitHub 中进行编辑。 通过 Markdown 扩展添加一些功能。

> [!IMPORTANT]
> 只要目标支持（绝大多数都应支持），所有链接均必须是安全的（`https` 与 `http`）。

## <a name="link-text"></a>链接文本

链接文本中使用的关键字应反映相关内容。 换言之，它们应为一般中文关键字或所链接到的页面的标题。

> [!IMPORTANT]
> 请勿使用“单击此处”。 这不利于搜索引擎优化，也不能充分地描述目标网页。

**正确：**

- `For more information, see the [contributor guide index](https://github.com/Azure/azure-content/blob/master/contributor-guide/contributor-guide-index.md).`

- `For more details, see the [SET TRANSACTION ISOLATION LEVEL](https://docs.microsoft.com/sql/t-sql/statements/set-transaction-isolation-level-transact-sql) reference.`

**不正确：**

- `For more details, see [https://msdn.microsoft.com/library/ms173763.aspx](https://msdn.microsoft.com/library/ms173763.aspx).`

- `For more information, click [here](https://github.com/Azure/azure-content/blob/master/contributor-guide/contributor-guide-index.md).`

## <a name="links-from-one-article-to-another"></a>从一篇文章链接到另一篇文章

发布系统支持两种类型的超链接：URL 和文件链接**** ****。

URL 链接可以是相对于 docs.microsoft.com 根的 URL 路径，也可以是包含完整 URL 语法（例如 `https://github.com/MicrosoftDocs/PowerShell-Docs`）的绝对 URL。

- 链接到当前 docset 之外的内容时，或在 docset 中的自动生成的参考和概念文章之间链接时，请使用 URL 链接__。
- 创建相对链接的最简单方法是从浏览器复制 URL，然后从粘贴到 Markdown 中的值中删除 `https://docs.microsoft.com/en-us`。
   - 请勿在 Microsoft 属性的 URL 中包括区域设置（例如，从 URL 中删除“/en-us”）。

文件链接用于在 docset 中从一篇文章链接到另一篇文章。

- 所有文件路径都使用正斜杠 (`/`) 字符，而不是反斜杠字符。
- 一篇文章链接到同一目录中的另一篇文章：

  `[link text](article-name.md)`

- 一篇文章链接到当前目录的父目录中的一篇文章：

  `[link text](../article-name.md)`

- 一篇文章链接到当前目录的子目录中的一篇文章：

  `[link text](directory/article-name.md)`

- 一篇文章链接到当前目录的父目录的子目录中的一篇文章：

  `[link text](../directory/article-name.md)`

> [!NOTE]
> 上述示例中均未在链接中使用 `~/`。 若要链接到以存储库根目录开头的绝对路径，请启用包含 `/` 的链接。 如果包含 `~/`，当在 GitHub 上导航源存储库时会生成无效的链接。 使路径以 `/` 开头便可有效解决此问题。

### <a name="structure-of-links-on-docsmicrosoftcom"></a>docs.microsoft.com 上链接的结构

docs.microsoft.com 上发布的内容具有以下 URL 结构：

```
https://docs.microsoft.com/<locale>/<product-service>/[<feature-service>]/[<subfolder>]/<topic>[?view=<view-name>]
```

示例：

```
https://docs.microsoft.com/en-us/azure/load-balancer/load-balancer-overview
https://docs.microsoft.com/en-us/powershell/azure/overview?view=azurermps-5.1.1
```

- `<locale>` - 标识文章的语言（例如 en-us 或 de-de）
- `<product-service>` - 产品或服务的名称（例如 powershell、dotnet 或 azure）
- `[<feature-service>]` -（可选）产品功能或子服务的名称（例如 csharp 或 load-balancer）
- `[<subfolder>]` -（可选）功能中子文件夹的名称
- `<topic>` - 主题的文章文件的名称（例如 load-balancer-overview 或 overview）
- `[?view=\<view-name>]` -（可选）具有多个可用版本的内容的版本选择器使用的视图名称（例如 azps-3.5.0）

> [!TIP]
> 大多数情况下，同一 docset 中的文章具有相同的 `<product-service>` URL 片段__。 例如：
> - 相同 docset
>   - `https://docs.microsoft.com/dotnet/core/get-started`
>   - `https://docs.microsoft.com/dotnet/framework/install`
> - 不同 docset
>   - `https://docs.microsoft.com/dotnet/core/get-started`
>   - `https://docs.microsoft.com/visualstudio/whats-new`

## <a name="bookmark-links"></a>书签链接

对于当前文件中标题的书签链接，请使用哈希符号，后跟标题的小写字词**。 删除标题中的标点符号并将空格替换为短划线：

```markdown
[Managed Disks](#managed-disks)
```

若要链接到另一篇文章中的某个书签标题，请使用文件相对或站点相对链接以及井号，后跟标题内容。 删除标题中的标点符号并将空格替换为短划线：

```markdown
[Managed Disks](../../linux/overview.md#managed-disks)
```

还可以从 URL 复制书签链接。 若要查找 URL，请将鼠标悬停在 docs.microsoft.com 上的标题行上。 应该会看到一个链接图标出现：

![文章标题中的链接图标](media/how-to-write-links/bookmark-link.png)

单击链接图标，然后从 URL 复制书签定位文本（即哈希后的部分）。

> [!NOTE]
> Docs Extension 也有帮助创建链接的工具。

### <a name="explicit-anchor-links"></a>显式定位标记链接

使用 `<a>` HTML 标记添加显式定位标记链接并非必需，也不推荐使用，但在中心和登录页面中除外。 请改为使用自动生成的书签，如[书签链接](#bookmark-links)中所述。 对于中心和登录页面，声明如下所示的定位标记：

```markdown
## <a id="anchortext" />Header text
```

或

```markdown
## <a name="anchortext" />Header text
```

以下链接到定位标记：

```markdown
To go to a section on the same page:
[text](#anchortext)

To go to a section on another page.
[text](filename.md#anchortext)
```

> [!NOTE]
> 定位文本必须始终为小写，且不包含空格。

## <a name="xref-cross-reference-links"></a>XRef（交叉引用）链接

XRef 链接是链接到 API 的推荐方式，因为它们在生成时经过验证。 若要链接到当前文档集或其他文档集中自动生成的 API 参考页，请使用具有类型或成员的唯一 ID ([UID](#determine-the-uid)) 的 XRef 链接。

> [!TIP]
> 可以使用[ VS Code 的 Docs Markdown 扩展][docsextension]（Docs Authoring Pack 的一部分）插入[.NET API 浏览器][]中显示的 .NET XRref 链接。

通过在 [.NET API 浏览器][]或 [Windows UWP][] 搜索框中键入其所有或部分全名，检查要链接到的 API 是否位于 [docs.microsoft.com][docs] 上。 如果未显示任何结果，则该类型尚不在 docs.microsoft.com 上。

可使用下列某一语法：

- 自动链接：

   ```markdown
   <xref:UID>
   <xref:UID?displayProperty=nameWithType>
   ```

   默认情况下，链接文本仅显示成员名称或类型名称。 可选 `displayProperty=nameWithType` 查询参数生成完全限定的链接文本，即类型 namespace.type，以及类型成员（包括枚举类型成员）type.member**** ****。

- Markdown 样式链接：

   ```markdown
   [link text](xref:UID)
   ```

   如果要自定义显示的链接文本，请使用适用于 XRef 的 Markdown 样式链接。

示例：

- \<xref:System.String> 显示为 <xref:System.String>****

- \<xref:System.String?displayProperty=nameWithType> 显示为 <xref:System.String?displayProperty=nameWithType>****

- \[String class](xref:System.String) 显示为 [String class](xref:System.String)****。

`displayProperty=fullName` 查询参数的工作方式与类的 `displayProperty=nameWithType` 相同。 也就是说，链接文本将成为 namespace.classname****。 但是，对于成员，链接文本显示为 namespace.classname.membername，这可能不可取****。

> [!NOTE]
> UID 是区分大小写的。 例如，`<xref:System.Object>` 会正确解析，但 `<xref:system.object>` 不会正确解析。

### <a name="xref-build-warnings-and-incremental-builds"></a>XRef 生成警告和增量生成

增量生成仅生成已更改或受更改影响的文件。 如果你看到有关无效 XREF 链接的生成警告，但该链接实际上有效，这可能是因为生成是增量的。 导致警告的文件未更改，因此未生成该文件，过去的警告被重播。 文件更改或你触发完整生成（你可以在 ops.microsoft.com 上启动完整生成）时，警告将消失。 这是增量生成的一个缺点，因为 DocFX 无法检测到 XREF 服务中的数据更新。

### <a name="determine-the-uid"></a>确定 UID

UID 通常是完全限定的类或成员名称。 确定 UID 的方法至少有两种：

- 右键单击某一类型或成员的 [Docs][docs] 页，选择“查看源”，然后复制 ms.assetid 的“内容”值**** **** ****：

  ![网页源中的 ms.assetid](media/how-to-write-links/ms-assetid.png)

- 通过将类型的部分或全部名称追加到 URL 中，使用[自动完成网站][]。 例如，在浏览器的地址栏中输入 `https://xref.docs.microsoft.com/autocomplete?text=Writeline` 会显示所有类型和方法，这些类型和方法的名称中包含 Writeline 及其 UID****。

#### <a name="verify-the-uid"></a>验证 UID

若要测试你是否具有正确的 UID，请将以下 URL 中的 System.String 替换为你的 UID，然后将其粘贴到浏览器的地址栏中****：

`https://xref.docs.microsoft.com/query?uid=System.String`

> [!TIP]
> URL 中的 UID 区分大小写，如果要检查方法重载 UID，则不要在参数类型之间包含空格。

如果看到以下类似内容，则你具有正确的 UID：

```text
[{"uid":"System.String","name":"String","fullName":"System.String","href":"https://docs.microsoft.com/dotnet/api/system.string","tags":",/dotnet,netframework-4.5.1,netframework-4.5.2,netframework-4.5,...xamarinmac-3.0,public,","vendor":null,"hash":null,"commentId":"T:System.String","nameWithType":"System.String"},{"uid":"System.String","name":"String","fullName":"System.String","href":"https://docs.microsoft.com/dotnet/api/system.string","tags":",/dotnet,netframework-4.5.1,netframework-4.5.2,netframework-4.5,netframework-4.6,netframework-4.6.1,...,xamarinmac-3.0,public,","vendor":null,"hash":null,"commentId":"T:System.String","nameWithType":"System.String"}]
```

如果只是看到页面上显示 `[]` ，则 UID 错误。

### <a name="percent-encoding-of-urls"></a>URL 的百分数编码

UID 中的特殊字符需要进行 HTML 编码，如下所示：

| 字符 | HTML 编码 |
| --------- | ------------- |
| `` ` ``   | %60           |
| `#`       | %23           |
| `*`       | %2A           |

查看[百分数代码](https://en.wikipedia.org/wiki/Percent-encoding)的完整列表。

编码示例：

- ``System.Threading.Tasks.Task`1`` 编码为 `System.Threading.Tasks.Task%601`（请参阅[泛型类型部分](#generic-types)）

- `System.Exception.#ctor` 编码为 `System.Exception.%23ctor`

- `System.Object.Equals*` 编码为 `System.Object.Equals%2A`

### <a name="generic-types"></a>泛型类型

泛型类型是诸如 `System.Collections.Generic.List<T>` 这样的类型。 如果在[ .NET API 浏览器](https://docs.microsoft.com/dotnet/api/)中浏览到此类型并查看其 URL，你会看到 `<T>` 在 URL 中编写为 `-1`，这实际上表示 **`1**：

`https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1`

要链接到泛型类型（如 List\<T>），请将 \` 反单引号符号编码为 %60，如以下示例中所示**** **** ****：

```markdown
<xref:System.Collections.Generic.List%601>
```

### <a name="methods"></a>方法

若要链接到方法，可以通过在方法名称后添加星号 (`*`) 链接到常规方法页面，或链接到特定重载。 例如，如果要链接到没有特定参数类型的 `<xref:System.Object.Equals%2A?displayProperty=nameWithType>` 方法，请使用“常规”页面。 星号字符编码为 `%2A`。 例如：

`<xref:System.Object.Equals%2a?displayProperty=nameWithType>` 链接到 <xref:System.Object.Equals%2A?displayProperty=nameWithType>

要链接到特定重载，请在方法名称后添加括号，并包含每个参数的完整类型名称。 请勿在类型名称之间放置空格字符，否则链接将无法正常工作。 例如：

`<xref:System.Object.Equals(System.Object,System.Object)?displayProperty=nameWithType>` 链接到 <xref:System.Object.Equals(System.Object,System.Object)?displayProperty=nameWithType>

## <a name="links-from-includes"></a>从包含文件链接

包含文件位于另一个目录中，因此，必须使用较长的相对路径。 若要从包含文件链接到某一篇文章，请使用以下格式：

```markdown
[link text](../articles/folder/article-name.md)
```

> [!TIP]
> 适用于 Visual Studio Code 的 [Docs Authoring Pack](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack) 扩展有助于正确插入相关链接和书签，免去了寻找路径的麻烦。

## <a name="links-in-selectors"></a>选择器中的链接

选择器是导航组件，以下拉列表的形式在文档文章中显示。 当读者选择下拉列表中的值时，浏览器将打开所选文章。 通常情况下，选择器列表包含密切相关文章的链接，例如，多种编程语言中的相同主题，或密切相关的文章系列。

如果你的选择器嵌入在包含文件中，则使用以下链接结构：

   ```markdown
   > [AZURE.SELECTOR-LIST (Dropdown1 | Dropdown2 )]
   - [(Text1 | Example1 )](../articles/folder/article-name1.md)
   - [(Text1 | Example2 )](../articles/folder/article-name2.md)
   - [(Text2 | Example3 )](../articles/folder/article-name3.md)
   - [(Text2 | Example4 )](../articles/folder/article-name4.md)
   ```

## <a name="reference-style-links"></a>引用样式链接

可以使用引用样式链接使源内容更易于读取。 引用样式链接使用简化的语法替代内联链接语法，以便将长 URL 移动到文章末尾。 下面是 [Daring Fireball](https://daringfireball.net/projects/markdown/) 的示例：

内联文本：

   ```markdown
   I get 10 times more traffic from [Google][1] than from [Yahoo][2] or [MSN][3].
   ```

文章末尾部分的链接引用：

   ```markdown
   <!--Reference links in article-->
   [1]: http://google.com/
   [2]: http://search.yahoo.com/
   [3]: http://search.msn.com/
   ```

请务必在链接前的冒号后加入空格。 链接到其他技术文章时，如果忘记加入空格，链接会在发布文章中被破坏。

## <a name="links-to-pages-that-are-not-part-of-the-technical-documentation-set"></a>链接到不属于技术文档集的页面

若要链接到另一个 Microsoft 属性（例如定价页、SLA 页或其他非文档文章的页面），请使用绝对 URL，但要忽略区域设置。 这样做是为了使链接在 GitHub 和显示链接的网站上正常工作：

   ```markdown
   [link text](https://azure.microsoft.com/pricing/details/virtual-machines/)
   ```

## <a name="links-to-third-party-sites"></a>指向第三方网站的链接

为了实现最佳用户体验，最好尽量减少将用户定向到另一个网站的次数。 因此，如果确实需要，可在以下信息基础上实现到第三方网站的任何链接：

- **责任性**：当要共享的信息是第三方信息时，链接到第三方内容。 例如，告知用户如何使用 Android 开发人员工具并不是 Microsoft 的职责，此类信息可以通过 Google 获取。 如有需要，我们可以介绍如何将 Android 开发人员工具与** Azure 结合使用，但对于如何使用该工具，应向 Google 寻求帮助。
- **PM 签名**：请求 Microsoft 在第三方内容上签名。 链接到此内容即表明我们信任此内容，并且有责任和义务让用户按说明操作。
- **新鲜度评审**：确保第三方信息仍为最新、正确且相关的版本，并确保链接未经任何更改。
- **跳转提醒**：确保用户知道他们即将转到另一个网站。 如果上下文未明确指出这一点，请添加一个限定性句子。 例如：“先决条件包括 Android 开发人员工具，你可以在 Android Studio 网站上进行下载。”
- **后续步骤**：在“后续步骤”部分，最好添加一个指向类似于 MVP 博客等内容的链接。 再次提醒，请务必使用户了解他们会离开当前网站。
- **合法性**：合法遵守每个 microsoft.com 页面页脚“使用条款”中的“链接到第三方网站”规定**** ****。

<!-- link references -->
[CommonMark]: https://commonmark.org/
[Markdig]: https://github.com/lunet-io/markdig
[GFM]: https://help.github.com/categories/writing-on-github/
[docs]: https://docs.microsoft.com
[.NET API 浏览器]: https://docs.microsoft.com/dotnet/api/
[Windows UWP]: https://docs.microsoft.com/uwp/api
[docsextension]: https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown
[自动完成网站]: https://xref.docs.microsoft.com/autocomplete?text=
