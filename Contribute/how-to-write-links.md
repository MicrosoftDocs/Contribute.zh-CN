---
title: 如何在文档中使用链接
description: 本文指导如何在 docs.microsoft.com 中创建内容链接。
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
author: gewarren
ms.author: gewarren
ms.date: 10/31/2018
ms.openlocfilehash: 69371cd201d156b2d0ce5e3e38527d77baca5a8a
ms.sourcegitcommit: ca84e542b081e145052f38967e826f6ef25da1b2
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/12/2019
ms.locfileid: "72288570"
---
# <a name="using-links-in-documentation"></a>在文档中使用链接
本文介绍如何使用 docs.microsoft.com 上托管页面的超链接。 通过几种不同的约定，便可轻松地将链接添加到 markdown。 链接将用户指向相同页面中的内容、其他相邻页面或外部站点和 URL。

docs.microsoft.com 站点后端使用开放发布服务 (OPS)，支持通过 [Markdig](https://github.com/lunet-io/markdig) 分析引擎分析的 [CommonMark](https://commonmark.org/) 兼容 Markdown。 Markdown 风格大多与 [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/) 兼容，因为大多数 docs 存储在 GitHub 中，并可以在 GitHub 中进行编辑。 通过 Markdown 扩展添加一些功能。

> [!IMPORTANT]
> 只要目标支持（绝大多数都应支持），所有链接均必须是安全的（`https` 与 `http`）。

## <a name="link-text"></a>链接文本

链接文本中使用的关键字应反映相关内容。 换言之，它们应为一般中文关键字或所链接到的页面的标题。

> [!IMPORTANT]
> 请勿使用“单击此处”。 这不利于搜索引擎优化，也不能充分地描述目标网页。

**正确：**

- `For more information, see the [contributor guide index](https://github.com/Azure/azure-content/blob/master/contributor-guide/contributor-guide-index.md).`

- `For more details, see the [SET TRANSACTION ISOLATION LEVEL](https://msdn.microsoft.com/library/ms173763.aspx) reference.`

**不正确：**

- `For more details, see [https://msdn.microsoft.com/library/ms173763.aspx](https://msdn.microsoft.com/library/ms173763.aspx).`

- `For more information, click [here](https://github.com/Azure/azure-content/blob/master/contributor-guide/contributor-guide-index.md).`

## <a name="links-from-one-article-to-another"></a>从一篇文章链接到另一篇文章

要在同一 docset 中创建从一篇 Docs 技术文章到另一篇 Docs 技术文章的内联链接，请使用以下链接语法：

- 目录中的一篇文章链接到同一目录中的另一篇文章：

  `[link text](article-name.md)`

- 子目录中的一篇文章链接到根目录中的一篇文章：

  `[link text](../article-name.md)`

- 根目录中的一篇文章链接到子目录中的一篇文章：

  `[link text](./directory/article-name.md)`

- 子目录中的一篇文章链接到另一个子目录中的一篇文章：

  `[link text](../directory/article-name.md)`

- 跨 docset 链接的文章（即使在同一存储库中）： `[link text](./directory/article-name)`

> [!IMPORTANT]
> 上述示例中均未在链接中使用 `~/`。 如果要链接到存储库的根路径，请以 `/` 开头。 如果包含 `~/`，当在 GitHub 上导航源存储库时会生成无效的链接。 使路径以 `/` 开头便可有效解决此问题。

## <a name="links-to-anchors"></a>链接到锚点

不必创建锚点。 它们在发布时会自动生成，用于所有 H2 标题。 只需要创建到 H2 部分的链接。

- 链接到同一篇文章中的标题：

  `[link](#the-text-of-the-H2-section-separated-by-hyphens)`
  `[Create cache](#create-cache)`

- 链接到同一子目录中另一篇文章中的锚点：

  `[link text](article-name.md#anchor-name)`
  `[Configure your profile](media-services-create-account.md#configure-your-profile)`

- 链接到另一个服务子目录中的锚点：

  `[link text](../directory/article-name.md#anchor-name)`
  `[Configure your profile](../directory/media-services-create-account.md#configure-your-profile)`

## <a name="links-from-includes"></a>从包含文件链接

包含文件位于另一个目录中，因此，必须使用较长的相对路径。 若要从包含文件链接到某一篇文章，请使用以下格式：

   ```markdown
   [link text](../articles/folder/article-name.md)
   ```

## <a name="links-in-selectors"></a>选择器中的链接

选择器是导航组件，以下拉列表的形式在文档文章中显示。 当读者选择下拉列表中的值时，浏览器将打开所选文章。 通常情况下，选择器列表包含密切相关文章的链接，例如，多种编程语言中的相同主题，或密切相关的文章系列。 

如果你的选择器嵌入在包含文件中，则使用以下链接结构：

   ```markdown
   > [AZURE.SELECTOR-LIST (Dropdown1 | Dropdown2 )]
   - [(Text1 | Example1 )](../articles/folder/article-name1.md)
   - [(Text1 | Example2 )](../articles/folder/article-name2.md)
   - [(Text2 | Example3 )](../articles/folder/article-name3.md)
   - [(Text2 | Example4 )](../articles/folder/article-name4.md) -->
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

- **责任性**：当要共享的信息是第三方信息时，链接到第三方内容。 例如，告知用户如何使用 Android 开发人员工具并不是 Microsoft 的职责，此类信息可以通过 Google 获取。 如有需要，我们可以介绍如何将 Android 开发人员工具与  Azure 结合使用，但对于如何使用该工具，应向 Google 寻求帮助。
- **PM 签名**：请求 Microsoft 在第三方内容上签名。 链接到此内容即表明我们信任此内容，并且有责任和义务让用户按说明操作。
- **新鲜度评审**：确保第三方信息仍为最新、正确且相关的版本，并确保链接未经任何更改。
- **跳转提醒**：确保用户知道他们即将转到另一个网站。 如果上下文未明确指出这一点，请添加一个限定性句子。 例如：“先决条件包括 Android 开发人员工具，你可以在 Android Studio 网站上进行下载。”
- **后续步骤**：在“后续步骤”部分，最好添加一个指向类似于 MVP 博客等内容的链接。 再次提醒，请务必使用户了解他们会离开当前网站。
- **合法性**：合法遵守每个 ms.com 页面页脚“使用条款”  中的“链接到第三方网站”  规定。

## <a name="links-to-msdn-or-technet"></a>链接到 MSDN 或 TechNet

如果需要链接到 MSDN 或 TechNet，请使用主题的完整链接，并从链接中删除“en-us”语言区域设置。

## <a name="links-to-azure-powershell-reference-content"></a>链接到 Azure PowerShell 引用内容

自 2016 年 11 月以来，Azure PowerShell 引用内容已经经历了若干次变更。 使用以下准则从 docs.microsoft.com 的其他文章链接到此内容。

URL 结构：

* 对于 cmdlet：
  - `/powershell/module/<module-name>/<cmdlet-name>[?view=<moniker-name>]`
* 对于概念主题：
  - `/powershell/azure/<topic-file-name>[?view=<moniker-name>]`
  - `/powershell/azure/<service-name>/<topic-file-name>[?view=<moniker-name>]`

`<moniker-name>` 部分是可选的。 如果省略这一部分，会将用户定向到最新版本的内容。 `<service-name>` 部分是以下基 URL 中显示的其中一个示例：

- Azure PowerShell (AzureRM) 内容：[https://docs.microsoft.com/powershell/azure/](https://docs.microsoft.com/powershell/azure/)
- Azure PowerShell (ASM) 内容：[https://docs.microsoft.com/powershell/azure/_servicemanagement_](https://docs.microsoft.com/powershell/azure/servicemanagement)
- Azure Active Directory (AzureAD) PowerShell 内容：[https://docs.microsoft.com/powershell/azure/_active-directory_](https://docs.microsoft.com/powershell/azure/active-directory)
- Azure Service Fabric PowerShell：[https://docs.microsoft.com/powershell/azure/_service-fabric_](https://docs.microsoft.com/powershell/azure/service-fabric)
- Azure 信息保护 PowerShell：[https://docs.microsoft.com/powershell/azure/_aip_](https://docs.microsoft.com/powershell/azure/aip)
- Azure 弹性数据库作业 PowerShell：[https://docs.microsoft.com/powershell/azure/_elasticdbjobs_](https://docs.microsoft.com/powershell/azure/elasticdbjobs)

在使用这些 URL 时，会将用户重定向到最新版本的内容。 这样就不必指定版本名字对象。 并且不会有指向版本更改时必须进行更新的概念内容的链接。

若要创建正确的链接，可以在浏览器中找到要链接的页面并复制 URL。
然后，删除 `https://docs.microsoft.com` 和区域设置信息。

从 TOC 进行链接时，必须使用完整的 URL（不包含区域设置信息）。

示例 Markdown：

```markdown
[Get-AzureRmResourceGroup](/powershell/module/azurerm.resources/get-azurermresourcegroup)
[Get-AzureRmResourceGroup](/powershell/module/azurerm.resources/get-azurermresourcegroup?view=azurermps-4.1.0)
[New-AzureVM](/powershell/module/azure/new-azurevm?view=azuresmps-4.0.0)
[New-AzureRmVM](/powershell/module/azurerm.compute/new-azurermvm)
[Install Azure PowerShell for Service Management](/powershell/azure/servicemanagement/install-azurerm-ps)
[Install Azure PowerShell](/powershell/azure/install-azurerm-ps)
```
