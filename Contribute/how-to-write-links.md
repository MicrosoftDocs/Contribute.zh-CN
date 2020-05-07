---
title: 如何在文档中使用链接
description: 本文指导如何在 docs.microsoft.com 中创建内容链接。
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
author: gewarren
ms.author: gewarren
ms.date: 03/31/2020
ms.openlocfilehash: ca29d4b9e81f8af3b680367b210bd1734860687d
ms.sourcegitcommit: cfba5ad25b898bfed76046126ce8ff4871910701
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/04/2020
ms.locfileid: "80624747"
---
# <a name="use-links-in-documentation"></a><span data-ttu-id="aa2ea-103">在文档中使用链接</span><span class="sxs-lookup"><span data-stu-id="aa2ea-103">Use links in documentation</span></span>

<span data-ttu-id="aa2ea-104">本文介绍如何使用 docs.microsoft.com 上托管页面的超链接。</span><span class="sxs-lookup"><span data-stu-id="aa2ea-104">This article describes how to use hyperlinks from pages hosted at docs.microsoft.com.</span></span> <span data-ttu-id="aa2ea-105">通过几种不同的约定，便可轻松地将链接添加到 markdown。</span><span class="sxs-lookup"><span data-stu-id="aa2ea-105">Links are easy to add into markdown with a few varying conventions.</span></span> <span data-ttu-id="aa2ea-106">链接将用户指向相同页面中的内容、其他相邻页面或外部站点和 URL。</span><span class="sxs-lookup"><span data-stu-id="aa2ea-106">Links point users to content in the same page, in other neighboring pages, or on external sites and URLs.</span></span>

<span data-ttu-id="aa2ea-107">docs.microsoft.com 站点后端使用开放发布服务 (OPS)，支持通过 [Markdig][] 分析引擎分析的 [CommonMark][] 兼容 Markdown。</span><span class="sxs-lookup"><span data-stu-id="aa2ea-107">The docs.microsoft.com site backend uses Open Publishing Services (OPS), which supports [CommonMark][]-compliant markdown parsed through the [Markdig][] parsing engine.</span></span> <span data-ttu-id="aa2ea-108">Markdown 风格大多与 [GitHub Flavored Markdown (GFM)][GFM] 兼容，因为大多数 docs 存储在 GitHub 中，并可以在 GitHub 中进行编辑。</span><span class="sxs-lookup"><span data-stu-id="aa2ea-108">This markdown flavor is mostly compatible with [GitHub Flavored Markdown (GFM)][GFM], as most docs are stored in GitHub and can be edited there.</span></span> <span data-ttu-id="aa2ea-109">通过 Markdown 扩展添加一些功能。</span><span class="sxs-lookup"><span data-stu-id="aa2ea-109">Additional functionality is added through Markdown extensions.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="aa2ea-110">只要目标支持（绝大多数都应支持），所有链接均必须是安全的（`https` 与 `http`）。</span><span class="sxs-lookup"><span data-stu-id="aa2ea-110">All links must be secure (`https` vs `http`) whenever the target supports it (which the vast majority should).</span></span>

## <a name="link-text"></a><span data-ttu-id="aa2ea-111">链接文本</span><span class="sxs-lookup"><span data-stu-id="aa2ea-111">Link text</span></span>

<span data-ttu-id="aa2ea-112">链接文本中使用的关键字应反映相关内容。</span><span class="sxs-lookup"><span data-stu-id="aa2ea-112">The words that you include in link text should be friendly.</span></span> <span data-ttu-id="aa2ea-113">换言之，它们应为一般中文关键字或所链接到的页面的标题。</span><span class="sxs-lookup"><span data-stu-id="aa2ea-113">In other words, they should be normal English words or the title of the page that you're linking to.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="aa2ea-114">请勿使用“单击此处”。</span><span class="sxs-lookup"><span data-stu-id="aa2ea-114">Do not use "click here."</span></span> <span data-ttu-id="aa2ea-115">这不利于搜索引擎优化，也不能充分地描述目标网页。</span><span class="sxs-lookup"><span data-stu-id="aa2ea-115">It's bad for search engine optimization and doesn't adequately describe the target.</span></span>

<span data-ttu-id="aa2ea-116">**正确：**</span><span class="sxs-lookup"><span data-stu-id="aa2ea-116">**Correct:**</span></span>

- `For more information, see the [contributor guide index](https://github.com/Azure/azure-content/blob/master/contributor-guide/contributor-guide-index.md).`

- `For more details, see the [SET TRANSACTION ISOLATION LEVEL](https://docs.microsoft.com/sql/t-sql/statements/set-transaction-isolation-level-transact-sql) reference.`

<span data-ttu-id="aa2ea-117">**不正确：**</span><span class="sxs-lookup"><span data-stu-id="aa2ea-117">**Incorrect:**</span></span>

- `For more details, see [https://msdn.microsoft.com/library/ms173763.aspx](https://msdn.microsoft.com/library/ms173763.aspx).`

- `For more information, click [here](https://github.com/Azure/azure-content/blob/master/contributor-guide/contributor-guide-index.md).`

## <a name="links-from-one-article-to-another"></a><span data-ttu-id="aa2ea-118">从一篇文章链接到另一篇文章</span><span class="sxs-lookup"><span data-stu-id="aa2ea-118">Links from one article to another</span></span>

<span data-ttu-id="aa2ea-119">发布系统支持两种类型的超链接：URL 和文件链接   。</span><span class="sxs-lookup"><span data-stu-id="aa2ea-119">There are two types of hyperlinks supported by the publishing system: **URLs** and **file links**.</span></span>

<span data-ttu-id="aa2ea-120">URL 链接可以是相对于 docs.microsoft.com 根的 URL 路径，也可以是包含完整 URL 语法（例如 `https://github.com/MicrosoftDocs/PowerShell-Docs`）的绝对 URL。</span><span class="sxs-lookup"><span data-stu-id="aa2ea-120">A URL link can be a URL path that is relative to the root of docs.microsoft.com, or an absolute URL that includes the full URL syntax (for example, `https://github.com/MicrosoftDocs/PowerShell-Docs`).</span></span>

- <span data-ttu-id="aa2ea-121">链接到当前 docset 之外的内容时，或在 docset 中的自动生成的参考和概念文章之间链接时，请使用 URL 链接  。</span><span class="sxs-lookup"><span data-stu-id="aa2ea-121">Use URL links when linking to content outside of the current _docset_ or between autogenerated reference and conceptual articles within the docset.</span></span>
- <span data-ttu-id="aa2ea-122">创建相对链接的最简单方法是从浏览器复制 URL，然后从粘贴到 Markdown 中的值中删除 `https://docs.microsoft.com/en-us`。</span><span class="sxs-lookup"><span data-stu-id="aa2ea-122">The simplest way to create a relative link is to copy the URL from your browser, then remove `https://docs.microsoft.com/en-us` from the value you paste into markdown.</span></span>
   - <span data-ttu-id="aa2ea-123">请勿在 Microsoft 属性的 URL 中包括区域设置（例如，从 URL 中删除“/en-us”）。</span><span class="sxs-lookup"><span data-stu-id="aa2ea-123">Do not include locales in URLs for Microsoft properties (for example, remove "/en-us" from the URL).</span></span>

<span data-ttu-id="aa2ea-124">文件链接用于在 docset 中从一篇文章链接到另一篇文章。</span><span class="sxs-lookup"><span data-stu-id="aa2ea-124">A file link is used to link from one article to another within the docset.</span></span>

- <span data-ttu-id="aa2ea-125">所有文件路径都使用正斜杠 (`/`) 字符，而不是反斜杠字符。</span><span class="sxs-lookup"><span data-stu-id="aa2ea-125">All file paths use forward-slash (`/`) characters instead of back-slash characters.</span></span>
- <span data-ttu-id="aa2ea-126">一篇文章链接到同一目录中的另一篇文章：</span><span class="sxs-lookup"><span data-stu-id="aa2ea-126">An article links to another article in the same directory:</span></span>

  `[link text](article-name.md)`

- <span data-ttu-id="aa2ea-127">一篇文章链接到当前目录的父目录中的一篇文章：</span><span class="sxs-lookup"><span data-stu-id="aa2ea-127">An article links to an article in the parent directory of the current directory:</span></span>

  `[link text](../article-name.md)`

- <span data-ttu-id="aa2ea-128">一篇文章链接到当前目录的子目录中的一篇文章：</span><span class="sxs-lookup"><span data-stu-id="aa2ea-128">An article links to an article in a subdirectory of the current directory:</span></span>

  `[link text](directory/article-name.md)`

- <span data-ttu-id="aa2ea-129">一篇文章链接到当前目录的父目录的子目录中的一篇文章：</span><span class="sxs-lookup"><span data-stu-id="aa2ea-129">An article links to an article in a subdirectory of the parent directory of the current directory:</span></span>

  `[link text](../directory/article-name.md)`

> [!NOTE]
> <span data-ttu-id="aa2ea-130">上述示例中均未在链接中使用 `~/`。</span><span class="sxs-lookup"><span data-stu-id="aa2ea-130">None of the previous examples use the `~/` as part of the link.</span></span> <span data-ttu-id="aa2ea-131">若要链接到以存储库根目录开头的绝对路径，请启用包含 `/` 的链接。</span><span class="sxs-lookup"><span data-stu-id="aa2ea-131">To link to an absolute path that begins at the root of the repository, start the link with `/`.</span></span> <span data-ttu-id="aa2ea-132">如果包含 `~/`，当在 GitHub 上导航源存储库时会生成无效的链接。</span><span class="sxs-lookup"><span data-stu-id="aa2ea-132">Including the `~/` produces invalid links when navigating the source repositories on GitHub.</span></span> <span data-ttu-id="aa2ea-133">使路径以 `/` 开头便可有效解决此问题。</span><span class="sxs-lookup"><span data-stu-id="aa2ea-133">Starting the path with `/` resolves correctly.</span></span>

### <a name="structure-of-links-on-docsmicrosoftcom"></a><span data-ttu-id="aa2ea-134">docs.microsoft.com 上链接的结构</span><span class="sxs-lookup"><span data-stu-id="aa2ea-134">Structure of links on docs.microsoft.com</span></span>

<span data-ttu-id="aa2ea-135">docs.microsoft.com 上发布的内容具有以下 URL 结构：</span><span class="sxs-lookup"><span data-stu-id="aa2ea-135">Content published on docs.microsoft.com has the following URL structure:</span></span>

```
https://docs.microsoft.com/<locale>/<product-service>/[<feature-service>]/[<subfolder>]/<topic>[?view=<view-name>]
```

<span data-ttu-id="aa2ea-136">示例：</span><span class="sxs-lookup"><span data-stu-id="aa2ea-136">Examples:</span></span>

```
https://docs.microsoft.com/en-us/azure/load-balancer/load-balancer-overview
https://docs.microsoft.com/en-us/powershell/azure/overview?view=azurermps-5.1.1
```

- <span data-ttu-id="aa2ea-137">`<locale>` - 标识文章的语言（例如 en-us 或 de-de）</span><span class="sxs-lookup"><span data-stu-id="aa2ea-137">`<locale>` - identifies the language of the article (example: en-us or de-de)</span></span>
- <span data-ttu-id="aa2ea-138">`<product-service>` - 产品或服务的名称（例如 powershell、dotnet 或 azure）</span><span class="sxs-lookup"><span data-stu-id="aa2ea-138">`<product-service>` - the name of the product or service (example: powershell, dotnet, or azure)</span></span>
- <span data-ttu-id="aa2ea-139">`[<feature-service>]` -（可选）产品功能或子服务的名称（例如 csharp 或 load-balancer）</span><span class="sxs-lookup"><span data-stu-id="aa2ea-139">`[<feature-service>]` - (optional) the name of the product's feature or subservice (example: csharp or load-balancer)</span></span>
- <span data-ttu-id="aa2ea-140">`[<subfolder>]` -（可选）功能中子文件夹的名称</span><span class="sxs-lookup"><span data-stu-id="aa2ea-140">`[<subfolder>]` - (optional) the name of a subfolder within a feature</span></span>
- <span data-ttu-id="aa2ea-141">`<topic>` - 主题的文章文件的名称（例如 load-balancer-overview 或 overview）</span><span class="sxs-lookup"><span data-stu-id="aa2ea-141">`<topic>` - the name of the article file for the topic (example: load-balancer-overview or overview)</span></span>
- <span data-ttu-id="aa2ea-142">`[?view=\<view-name>]` -（可选）具有多个可用版本的内容的版本选择器使用的视图名称（例如 azps-3.5.0）</span><span class="sxs-lookup"><span data-stu-id="aa2ea-142">`[?view=\<view-name>]` - (optional) the view name used by the version selector for content that has multiple versions available (example: azps-3.5.0)</span></span>

> [!TIP]
> <span data-ttu-id="aa2ea-143">大多数情况下，同一 docset 中的文章具有相同的 `<product-service>` URL 片段  。</span><span class="sxs-lookup"><span data-stu-id="aa2ea-143">In most cases, articles in the same _docset_ have the same `<product-service>` URL fragment.</span></span> <span data-ttu-id="aa2ea-144">例如：</span><span class="sxs-lookup"><span data-stu-id="aa2ea-144">For example:</span></span>
> - <span data-ttu-id="aa2ea-145">相同 docset</span><span class="sxs-lookup"><span data-stu-id="aa2ea-145">Same docset</span></span>
>   - `https://docs.microsoft.com/dotnet/core/get-started`
>   - `https://docs.microsoft.com/dotnet/framework/install`
> - <span data-ttu-id="aa2ea-146">不同 docset</span><span class="sxs-lookup"><span data-stu-id="aa2ea-146">Different docset</span></span>
>   - `https://docs.microsoft.com/dotnet/core/get-started`
>   - `https://docs.microsoft.com/visualstudio/whats-new`

## <a name="bookmark-links"></a><span data-ttu-id="aa2ea-147">书签链接</span><span class="sxs-lookup"><span data-stu-id="aa2ea-147">Bookmark links</span></span>

<span data-ttu-id="aa2ea-148">对于当前文件中标题的书签链接，请使用哈希符号，后跟标题的小写字词  。</span><span class="sxs-lookup"><span data-stu-id="aa2ea-148">For a bookmark link to a heading in the *current* file, use a hash symbol followed by the lowercase words of the heading.</span></span> <span data-ttu-id="aa2ea-149">删除标题中的标点符号并将空格替换为短划线：</span><span class="sxs-lookup"><span data-stu-id="aa2ea-149">Remove punctuation from the heading and replace spaces with dashes:</span></span>

```markdown
[Managed Disks](#managed-disks)
```

<span data-ttu-id="aa2ea-150">若要链接到另一篇文章中的某个书签标题，请使用文件相对或站点相对链接以及井号，后跟标题内容。</span><span class="sxs-lookup"><span data-stu-id="aa2ea-150">To link to a bookmark heading in another article, use the file-relative or site-relative link plus a hash symbol, followed by the words of the heading.</span></span> <span data-ttu-id="aa2ea-151">删除标题中的标点符号并将空格替换为短划线：</span><span class="sxs-lookup"><span data-stu-id="aa2ea-151">Remove punctuation from the heading and replace spaces with dashes:</span></span>

```markdown
[Managed Disks](../../linux/overview.md#managed-disks)
```

<span data-ttu-id="aa2ea-152">还可以从 URL 复制书签链接。</span><span class="sxs-lookup"><span data-stu-id="aa2ea-152">You can also copy the bookmark link from the URL.</span></span> <span data-ttu-id="aa2ea-153">若要查找 URL，请将鼠标悬停在 docs.microsoft.com 上的标题行上。</span><span class="sxs-lookup"><span data-stu-id="aa2ea-153">To find the URL, hover your mouse over the heading line on docs.microsoft.com.</span></span> <span data-ttu-id="aa2ea-154">应该会看到一个链接图标出现：</span><span class="sxs-lookup"><span data-stu-id="aa2ea-154">You should see a link icon appear:</span></span>

![文章标题中的链接图标](media/how-to-write-links/bookmark-link.png)

<span data-ttu-id="aa2ea-156">单击链接图标，然后从 URL 复制书签定位文本（即哈希后的部分）。</span><span class="sxs-lookup"><span data-stu-id="aa2ea-156">Click the link icon and then copy the bookmark anchor text from the URL (that is, the part after the hash).</span></span>

> [!NOTE]
> <span data-ttu-id="aa2ea-157">Docs Extension 也有帮助创建链接的工具。</span><span class="sxs-lookup"><span data-stu-id="aa2ea-157">The Docs Extension also has tools to help create links.</span></span>

### <a name="explicit-anchor-links"></a><span data-ttu-id="aa2ea-158">显式定位标记链接</span><span class="sxs-lookup"><span data-stu-id="aa2ea-158">Explicit anchor links</span></span>

<span data-ttu-id="aa2ea-159">使用 `<a>` HTML 标记添加显式定位标记链接并非必需，也不推荐使用，但在中心和登录页面中除外。</span><span class="sxs-lookup"><span data-stu-id="aa2ea-159">Adding explicit anchor links using the `<a>` HTML tag isn't required or recommended, except in hub and landing pages.</span></span> <span data-ttu-id="aa2ea-160">请改为使用自动生成的书签，如[书签链接](#bookmark-links)中所述。</span><span class="sxs-lookup"><span data-stu-id="aa2ea-160">Instead, use the auto-generated bookmarks as described in [bookmark links](#bookmark-links).</span></span> <span data-ttu-id="aa2ea-161">对于中心和登录页面，声明如下所示的定位标记：</span><span class="sxs-lookup"><span data-stu-id="aa2ea-161">For hub and landing pages, declare anchors as follows:</span></span>

```markdown
## <a id="anchortext" />Header text
```

<span data-ttu-id="aa2ea-162">或</span><span class="sxs-lookup"><span data-stu-id="aa2ea-162">or</span></span>

```markdown
## <a name="anchortext" />Header text
```

<span data-ttu-id="aa2ea-163">以下链接到定位标记：</span><span class="sxs-lookup"><span data-stu-id="aa2ea-163">And the following to link to the anchor:</span></span>

```markdown
To go to a section on the same page:
[text](#anchortext)

To go to a section on another page.
[text](filename.md#anchortext)
```

> [!NOTE]
> <span data-ttu-id="aa2ea-164">定位文本必须始终为小写，且不包含空格。</span><span class="sxs-lookup"><span data-stu-id="aa2ea-164">Anchor text must always be lowercase and not contain spaces.</span></span>

## <a name="xref-cross-reference-links"></a><span data-ttu-id="aa2ea-165">XRef（交叉引用）链接</span><span class="sxs-lookup"><span data-stu-id="aa2ea-165">XRef (cross reference) links</span></span>

<span data-ttu-id="aa2ea-166">XRef 链接是链接到 API 的推荐方式，因为它们在生成时经过验证。</span><span class="sxs-lookup"><span data-stu-id="aa2ea-166">XRef links are the recommended way to link to APIs, because they're validated at build time.</span></span> <span data-ttu-id="aa2ea-167">若要链接到当前文档集或其他文档集中自动生成的 API 参考页，请使用具有类型或成员的唯一 ID ([UID](#determine-the-uid)) 的 XRef 链接。</span><span class="sxs-lookup"><span data-stu-id="aa2ea-167">To link to auto-generated API reference pages in the current docset or other docsets, use XRef links with the unique ID ([UID](#determine-the-uid)) of the type or member.</span></span>

> [!TIP]
> <span data-ttu-id="aa2ea-168">可以使用[ VS Code 的 Docs Markdown 扩展][docsextension]（Docs Authoring Pack 的一部分）插入[.NET API 浏览器][]中显示的 .NET XRref 链接。</span><span class="sxs-lookup"><span data-stu-id="aa2ea-168">You can use the [Docs Markdown extension for VS Code][docsextension] (part of the Docs Authoring Pack) to insert .NET XRref links that are surfaced in the [.NET API Browser][].</span></span>

<span data-ttu-id="aa2ea-169">通过在 [.NET API 浏览器][]或 [Windows UWP][] 搜索框中键入其所有或部分全名，检查要链接到的 API 是否位于 [docs.microsoft.com][docs] 上。</span><span class="sxs-lookup"><span data-stu-id="aa2ea-169">Check if the API you want to link to is on [docs.microsoft.com][docs] by typing all or some of its full name in the [.NET API browser][] or [Windows UWP][] search box.</span></span> <span data-ttu-id="aa2ea-170">如果未显示任何结果，则该类型尚不在 docs.microsoft.com 上。</span><span class="sxs-lookup"><span data-stu-id="aa2ea-170">If you don't see any results displayed, the type isn't yet on docs.microsoft.com.</span></span>

<span data-ttu-id="aa2ea-171">可使用下列某一语法：</span><span class="sxs-lookup"><span data-stu-id="aa2ea-171">You can use one of the following syntaxes:</span></span>

- <span data-ttu-id="aa2ea-172">自动链接：</span><span class="sxs-lookup"><span data-stu-id="aa2ea-172">Auto-links:</span></span>

   ```markdown
   <xref:UID>
   <xref:UID?displayProperty=nameWithType>
   ```

   <span data-ttu-id="aa2ea-173">默认情况下，链接文本仅显示成员名称或类型名称。</span><span class="sxs-lookup"><span data-stu-id="aa2ea-173">By default, link text shows only the member or type name.</span></span> <span data-ttu-id="aa2ea-174">可选 `displayProperty=nameWithType` 查询参数生成完全限定的链接文本，即类型 namespace.type，以及类型成员（包括枚举类型成员）type.member   。</span><span class="sxs-lookup"><span data-stu-id="aa2ea-174">The optional `displayProperty=nameWithType` query parameter produces fully qualified link text, that is, **namespace.type** for types, and **type.member** for type members, including enumeration type members.</span></span>

- <span data-ttu-id="aa2ea-175">Markdown 样式链接：</span><span class="sxs-lookup"><span data-stu-id="aa2ea-175">Markdown-style links:</span></span>

   ```markdown
   [link text](xref:UID)
   ```

   <span data-ttu-id="aa2ea-176">如果要自定义显示的链接文本，请使用适用于 XRef 的 Markdown 样式链接。</span><span class="sxs-lookup"><span data-stu-id="aa2ea-176">Use Markdown-style links for XRef when you want to customize the link text that's displayed.</span></span>

<span data-ttu-id="aa2ea-177">示例：</span><span class="sxs-lookup"><span data-stu-id="aa2ea-177">Examples:</span></span>

- <span data-ttu-id="aa2ea-178">\<xref:System.String> 显示为 <xref:System.String> </span><span class="sxs-lookup"><span data-stu-id="aa2ea-178">**\<xref:System.String>** displays as <xref:System.String></span></span>

- <span data-ttu-id="aa2ea-179">\<xref:System.String?displayProperty=nameWithType> 显示为 <xref:System.String?displayProperty=nameWithType> </span><span class="sxs-lookup"><span data-stu-id="aa2ea-179">**\<xref:System.String?displayProperty=nameWithType>** displays as <xref:System.String?displayProperty=nameWithType></span></span>

- <span data-ttu-id="aa2ea-180">\[String class](xref:System.String) 显示为 [String class](xref:System.String)  。</span><span class="sxs-lookup"><span data-stu-id="aa2ea-180">**\[String class](xref:System.String)** displays as [String class](xref:System.String).</span></span>

<span data-ttu-id="aa2ea-181">`displayProperty=fullName` 查询参数的工作方式与类的 `displayProperty=nameWithType` 相同。</span><span class="sxs-lookup"><span data-stu-id="aa2ea-181">The `displayProperty=fullName` query parameter works the same way as `displayProperty=nameWithType` for classes.</span></span> <span data-ttu-id="aa2ea-182">也就是说，链接文本将成为 namespace.classname  。</span><span class="sxs-lookup"><span data-stu-id="aa2ea-182">That is, the link text becomes **namespace.classname**.</span></span> <span data-ttu-id="aa2ea-183">但是，对于成员，链接文本显示为 namespace.classname.membername，这可能不可取  。</span><span class="sxs-lookup"><span data-stu-id="aa2ea-183">However, for members, the link text displays as **namespace.classname.membername**, which may be undesirable.</span></span>

> [!NOTE]
> <span data-ttu-id="aa2ea-184">UID 是区分大小写的。</span><span class="sxs-lookup"><span data-stu-id="aa2ea-184">UIDs are case sensitive.</span></span> <span data-ttu-id="aa2ea-185">例如，`<xref:System.Object>` 会正确解析，但 `<xref:system.object>` 不会正确解析。</span><span class="sxs-lookup"><span data-stu-id="aa2ea-185">For example, `<xref:System.Object>` resolves correctly but `<xref:system.object>` does not.</span></span>

### <a name="xref-build-warnings-and-incremental-builds"></a><span data-ttu-id="aa2ea-186">XRef 生成警告和增量生成</span><span class="sxs-lookup"><span data-stu-id="aa2ea-186">XRef build warnings and incremental builds</span></span>

<span data-ttu-id="aa2ea-187">增量生成仅生成已更改或受更改影响的文件。</span><span class="sxs-lookup"><span data-stu-id="aa2ea-187">An incremental build only builds files that have changed or been affected by a change.</span></span> <span data-ttu-id="aa2ea-188">如果你看到有关无效 XREF 链接的生成警告，但该链接实际上有效，这可能是因为生成是增量的。</span><span class="sxs-lookup"><span data-stu-id="aa2ea-188">If you see a build warning about an invalid XREF link, but the link is actually valid, this could be because the build was incremental.</span></span> <span data-ttu-id="aa2ea-189">导致警告的文件未更改，因此未生成该文件，过去的警告被重播。</span><span class="sxs-lookup"><span data-stu-id="aa2ea-189">The file causing the warning didn't change, so it wasn't built and past warnings were replayed.</span></span> <span data-ttu-id="aa2ea-190">文件更改或你触发完整生成（你可以在 ops.microsoft.com 上启动完整生成）时，警告将消失。</span><span class="sxs-lookup"><span data-stu-id="aa2ea-190">The warning will disappear when the file changes or if you trigger a full build (you can start a full build on ops.microsoft.com).</span></span> <span data-ttu-id="aa2ea-191">这是增量生成的一个缺点，因为 DocFX 无法检测到 XREF 服务中的数据更新。</span><span class="sxs-lookup"><span data-stu-id="aa2ea-191">This is a drawback to incremental builds, because DocFX can't detect a data update inside the XREF service.</span></span>

### <a name="determine-the-uid"></a><span data-ttu-id="aa2ea-192">确定 UID</span><span class="sxs-lookup"><span data-stu-id="aa2ea-192">Determine the UID</span></span>

<span data-ttu-id="aa2ea-193">UID 通常是完全限定的类或成员名称。</span><span class="sxs-lookup"><span data-stu-id="aa2ea-193">The UID is usually the fully qualified class or member name.</span></span> <span data-ttu-id="aa2ea-194">确定 UID 的方法至少有两种：</span><span class="sxs-lookup"><span data-stu-id="aa2ea-194">There are at least two ways to determine the UID:</span></span>

- <span data-ttu-id="aa2ea-195">右键单击某一类型或成员的 [Docs][docs] 页，选择“查看源”，然后复制 ms.assetid 的“内容”值    ：</span><span class="sxs-lookup"><span data-stu-id="aa2ea-195">Right-click on the [Docs][docs] page for a type or member, select **View source**, and then copy the **content** value for **ms.assetid**:</span></span>

  ![网页源中的 ms.assetid](media/how-to-write-links/ms-assetid.png)

- <span data-ttu-id="aa2ea-197">通过将类型的部分或全部名称追加到 URL 中，使用[自动完成网站][]。</span><span class="sxs-lookup"><span data-stu-id="aa2ea-197">Use the [autocomplete site][] by appending some or all of the name of the type to the URL.</span></span> <span data-ttu-id="aa2ea-198">例如，在浏览器的地址栏中输入 `https://xref.docs.microsoft.com/autocomplete?text=Writeline` 会显示所有类型和方法，这些类型和方法的名称中包含 Writeline 及其 UID  。</span><span class="sxs-lookup"><span data-stu-id="aa2ea-198">For example, entering `https://xref.docs.microsoft.com/autocomplete?text=Writeline` in the address bar of your browser displays all the types and methods that contain **Writeline** in their name, along with their UID.</span></span>

#### <a name="verify-the-uid"></a><span data-ttu-id="aa2ea-199">验证 UID</span><span class="sxs-lookup"><span data-stu-id="aa2ea-199">Verify the UID</span></span>

<span data-ttu-id="aa2ea-200">若要测试你是否具有正确的 UID，请将以下 URL 中的 System.String 替换为你的 UID，然后将其粘贴到浏览器的地址栏中  ：</span><span class="sxs-lookup"><span data-stu-id="aa2ea-200">To test if you have the correct UID, replace **System.String** in the following URL with your UID, and then paste it into the address bar of a browser:</span></span>

`https://xref.docs.microsoft.com/query?uid=System.String`

> [!TIP]
> <span data-ttu-id="aa2ea-201">URL 中的 UID 区分大小写，如果要检查方法重载 UID，则不要在参数类型之间包含空格。</span><span class="sxs-lookup"><span data-stu-id="aa2ea-201">The UID in the URL is case-sensitive, and if you're checking a method overload UID, don't include spaces between the parameter types.</span></span>

<span data-ttu-id="aa2ea-202">如果看到以下类似内容，则你具有正确的 UID：</span><span class="sxs-lookup"><span data-stu-id="aa2ea-202">If you see something like the following, you have the correct UID:</span></span>

```text
[{"uid":"System.String","name":"String","fullName":"System.String","href":"https://docs.microsoft.com/dotnet/api/system.string","tags":",/dotnet,netframework-4.5.1,netframework-4.5.2,netframework-4.5,...xamarinmac-3.0,public,","vendor":null,"hash":null,"commentId":"T:System.String","nameWithType":"System.String"},{"uid":"System.String","name":"String","fullName":"System.String","href":"https://docs.microsoft.com/dotnet/api/system.string","tags":",/dotnet,netframework-4.5.1,netframework-4.5.2,netframework-4.5,netframework-4.6,netframework-4.6.1,...,xamarinmac-3.0,public,","vendor":null,"hash":null,"commentId":"T:System.String","nameWithType":"System.String"}]
```

<span data-ttu-id="aa2ea-203">如果只是看到页面上显示 `[]` ，则 UID 错误。</span><span class="sxs-lookup"><span data-stu-id="aa2ea-203">If you just see `[]` displayed on the page, you have the wrong UID.</span></span>

### <a name="percent-encoding-of-urls"></a><span data-ttu-id="aa2ea-204">URL 的百分数编码</span><span class="sxs-lookup"><span data-stu-id="aa2ea-204">Percent-encoding of URLs</span></span>

<span data-ttu-id="aa2ea-205">UID 中的特殊字符需要进行 HTML 编码，如下所示：</span><span class="sxs-lookup"><span data-stu-id="aa2ea-205">Special characters in the UID need to be HTML encoded as follows:</span></span>

| <span data-ttu-id="aa2ea-206">字符</span><span class="sxs-lookup"><span data-stu-id="aa2ea-206">Character</span></span> | <span data-ttu-id="aa2ea-207">HTML 编码</span><span class="sxs-lookup"><span data-stu-id="aa2ea-207">HTML encoding</span></span> |
| --------- | ------------- |
| `` ` ``   | <span data-ttu-id="aa2ea-208">%60</span><span class="sxs-lookup"><span data-stu-id="aa2ea-208">%60</span></span>           |
| `#`       | <span data-ttu-id="aa2ea-209">%23</span><span class="sxs-lookup"><span data-stu-id="aa2ea-209">%23</span></span>           |
| `*`       | <span data-ttu-id="aa2ea-210">%2A</span><span class="sxs-lookup"><span data-stu-id="aa2ea-210">%2A</span></span>           |

<span data-ttu-id="aa2ea-211">查看[百分数代码](https://en.wikipedia.org/wiki/Percent-encoding)的完整列表。</span><span class="sxs-lookup"><span data-stu-id="aa2ea-211">See a full list of [percent-codes](https://en.wikipedia.org/wiki/Percent-encoding).</span></span>

<span data-ttu-id="aa2ea-212">编码示例：</span><span class="sxs-lookup"><span data-stu-id="aa2ea-212">Encoding examples:</span></span>

- <span data-ttu-id="aa2ea-213">`System.Threading.Tasks.Task``1` 编码为 `System.Threading.Tasks.Task%601`（请参阅[泛型类型部分](#generic-types)）</span><span class="sxs-lookup"><span data-stu-id="aa2ea-213">`System.Threading.Tasks.Task``1` encodes as `System.Threading.Tasks.Task%601` (see the [section on generic types](#generic-types))</span></span>

- <span data-ttu-id="aa2ea-214">`System.Exception.#ctor` 编码为 `System.Exception.%23ctor`</span><span class="sxs-lookup"><span data-stu-id="aa2ea-214">`System.Exception.#ctor` encodes as `System.Exception.%23ctor`</span></span>

- <span data-ttu-id="aa2ea-215">`System.Object.Equals*` 编码为 `System.Object.Equals%2A`</span><span class="sxs-lookup"><span data-stu-id="aa2ea-215">`System.Object.Equals*` encodes as `System.Object.Equals%2A`</span></span>

### <a name="generic-types"></a><span data-ttu-id="aa2ea-216">泛型类型</span><span class="sxs-lookup"><span data-stu-id="aa2ea-216">Generic types</span></span>

<span data-ttu-id="aa2ea-217">泛型类型是诸如 `System.Collections.Generic.List<T>` 这样的类型。</span><span class="sxs-lookup"><span data-stu-id="aa2ea-217">Generic types are those types such as `System.Collections.Generic.List<T>`.</span></span> <span data-ttu-id="aa2ea-218">如果在[ .NET API 浏览器](https://docs.microsoft.com/dotnet/api/)中浏览到此类型并查看其 URL，你会看到 `<T>` 在 URL 中编写为 `-1`，这实际上表示 **\`1**：</span><span class="sxs-lookup"><span data-stu-id="aa2ea-218">If you browse to this type in the [.NET API browser](https://docs.microsoft.com/dotnet/api/) and look at its URL, you see that `<T>` is written as `-1` in the URL, which actually represents **\`1**:</span></span>

`https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1`

<span data-ttu-id="aa2ea-219">若要链接到泛型类型（如 List\<T>），将 \` 反单引号符号编码为 %60，如以下示例中所示    ：</span><span class="sxs-lookup"><span data-stu-id="aa2ea-219">To link to a generic type such as **List\<T>**, encode the **\`** backtick character as **%60**, as shown in the following example:</span></span>

```markdown
<xref:System.Collections.Generic.List%601>
```

### <a name="methods"></a><span data-ttu-id="aa2ea-220">方法</span><span class="sxs-lookup"><span data-stu-id="aa2ea-220">Methods</span></span>

<span data-ttu-id="aa2ea-221">若要链接到方法，可以通过在方法名称后添加星号 (`*`) 链接到常规方法页面，或链接到特定重载。</span><span class="sxs-lookup"><span data-stu-id="aa2ea-221">To link to a method, you can either link to the general method page by adding an asterisk (`*`) after the method name, or to a specific overload.</span></span> <span data-ttu-id="aa2ea-222">例如，如果要链接到没有特定参数类型的 `<xref:System.Object.Equals%2A?displayProperty=nameWithType>` 方法，请使用“常规”页面。</span><span class="sxs-lookup"><span data-stu-id="aa2ea-222">For example, use the general page when you want to link to the `<xref:System.Object.Equals%2A?displayProperty=nameWithType>` method without specific parameter types.</span></span> <span data-ttu-id="aa2ea-223">星号字符编码为 `%2A`。</span><span class="sxs-lookup"><span data-stu-id="aa2ea-223">The asterisk character is encoded as `%2A`.</span></span> <span data-ttu-id="aa2ea-224">例如：</span><span class="sxs-lookup"><span data-stu-id="aa2ea-224">For example:</span></span>

<span data-ttu-id="aa2ea-225">`<xref:System.Object.Equals%2a?displayProperty=nameWithType>` 链接到 <xref:System.Object.Equals%2A?displayProperty=nameWithType></span><span class="sxs-lookup"><span data-stu-id="aa2ea-225">`<xref:System.Object.Equals%2a?displayProperty=nameWithType>` links to <xref:System.Object.Equals%2A?displayProperty=nameWithType></span></span>

<span data-ttu-id="aa2ea-226">要链接到特定重载，请在方法名称后添加括号，并包含每个参数的完整类型名称。</span><span class="sxs-lookup"><span data-stu-id="aa2ea-226">To link to a specific overload, add parenthesis after the method name and include the full type name of each parameter.</span></span> <span data-ttu-id="aa2ea-227">请勿在类型名称之间放置空格字符，否则链接将无法正常工作。</span><span class="sxs-lookup"><span data-stu-id="aa2ea-227">Do not put a space character between the type names or the link won't work.</span></span> <span data-ttu-id="aa2ea-228">例如：</span><span class="sxs-lookup"><span data-stu-id="aa2ea-228">For example:</span></span>

<span data-ttu-id="aa2ea-229">`<xref:System.Object.Equals(System.Object,System.Object)?displayProperty=nameWithType>` 链接到 <xref:System.Object.Equals(System.Object,System.Object)?displayProperty=nameWithType></span><span class="sxs-lookup"><span data-stu-id="aa2ea-229">`<xref:System.Object.Equals(System.Object,System.Object)?displayProperty=nameWithType>` links to <xref:System.Object.Equals(System.Object,System.Object)?displayProperty=nameWithType></span></span>

## <a name="links-from-includes"></a><span data-ttu-id="aa2ea-230">从包含文件链接</span><span class="sxs-lookup"><span data-stu-id="aa2ea-230">Links from includes</span></span>

<span data-ttu-id="aa2ea-231">包含文件位于另一个目录中，因此，必须使用较长的相对路径。</span><span class="sxs-lookup"><span data-stu-id="aa2ea-231">Because include files are located in another directory, you must use longer relative paths.</span></span> <span data-ttu-id="aa2ea-232">若要从包含文件链接到某一篇文章，请使用以下格式：</span><span class="sxs-lookup"><span data-stu-id="aa2ea-232">To link to an article from an include file, use this format:</span></span>

```markdown
[link text](../articles/folder/article-name.md)
```

> [!TIP]
> <span data-ttu-id="aa2ea-233">适用于 Visual Studio Code 的 [Docs Authoring Pack](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack) 扩展有助于正确插入相关链接和书签，免去了寻找路径的麻烦。</span><span class="sxs-lookup"><span data-stu-id="aa2ea-233">The [Docs Authoring Pack](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack) extension for Visual Studio Code helps you insert relative links and bookmarks correctly without the tedium of figuring out paths.</span></span>

## <a name="links-in-selectors"></a><span data-ttu-id="aa2ea-234">选择器中的链接</span><span class="sxs-lookup"><span data-stu-id="aa2ea-234">Links in selectors</span></span>

<span data-ttu-id="aa2ea-235">选择器是导航组件，以下拉列表的形式在文档文章中显示。</span><span class="sxs-lookup"><span data-stu-id="aa2ea-235">A selector is a navigation component that appears in a docs article as a drop-down list.</span></span> <span data-ttu-id="aa2ea-236">当读者选择下拉列表中的值时，浏览器将打开所选文章。</span><span class="sxs-lookup"><span data-stu-id="aa2ea-236">When a reader selects a value in the drop-down, the browser opens the selected article.</span></span> <span data-ttu-id="aa2ea-237">通常情况下，选择器列表包含密切相关文章的链接，例如，多种编程语言中的相同主题，或密切相关的文章系列。</span><span class="sxs-lookup"><span data-stu-id="aa2ea-237">Typically the selector list contains links to closely related articles, for example the same subject matter in multiple programming languages or a closely related series of articles.</span></span>

<span data-ttu-id="aa2ea-238">如果你的选择器嵌入在包含文件中，则使用以下链接结构：</span><span class="sxs-lookup"><span data-stu-id="aa2ea-238">If you have selectors that are embedded in an include, use the following link structure:</span></span>

   ```markdown
   > [AZURE.SELECTOR-LIST (Dropdown1 | Dropdown2 )]
   - [(Text1 | Example1 )](../articles/folder/article-name1.md)
   - [(Text1 | Example2 )](../articles/folder/article-name2.md)
   - [(Text2 | Example3 )](../articles/folder/article-name3.md)
   - [(Text2 | Example4 )](../articles/folder/article-name4.md)
   ```

## <a name="reference-style-links"></a><span data-ttu-id="aa2ea-239">引用样式链接</span><span class="sxs-lookup"><span data-stu-id="aa2ea-239">Reference-style links</span></span>

<span data-ttu-id="aa2ea-240">可以使用引用样式链接使源内容更易于读取。</span><span class="sxs-lookup"><span data-stu-id="aa2ea-240">You can use reference-style links to make your source content easier to read.</span></span> <span data-ttu-id="aa2ea-241">引用样式链接使用简化的语法替代内联链接语法，以便将长 URL 移动到文章末尾。</span><span class="sxs-lookup"><span data-stu-id="aa2ea-241">Reference-style links replace inline link syntax with simplified syntax that allows you to move the long URLs to the end of the article.</span></span> <span data-ttu-id="aa2ea-242">下面是 [Daring Fireball](https://daringfireball.net/projects/markdown/) 的示例：</span><span class="sxs-lookup"><span data-stu-id="aa2ea-242">Here's [Daring Fireball](https://daringfireball.net/projects/markdown/) 's example:</span></span>

<span data-ttu-id="aa2ea-243">内联文本：</span><span class="sxs-lookup"><span data-stu-id="aa2ea-243">Inline text:</span></span>

   ```markdown
   I get 10 times more traffic from [Google][1] than from [Yahoo][2] or [MSN][3].
   ```

<span data-ttu-id="aa2ea-244">文章末尾部分的链接引用：</span><span class="sxs-lookup"><span data-stu-id="aa2ea-244">Link references at the end of the article:</span></span>

   ```markdown
   <!--Reference links in article-->
   [1]: http://google.com/
   [2]: http://search.yahoo.com/
   [3]: http://search.msn.com/
   ```

<span data-ttu-id="aa2ea-245">请务必在链接前的冒号后加入空格。</span><span class="sxs-lookup"><span data-stu-id="aa2ea-245">Make sure that you include the space after the colon, before the link.</span></span> <span data-ttu-id="aa2ea-246">链接到其他技术文章时，如果忘记加入空格，链接会在发布文章中被破坏。</span><span class="sxs-lookup"><span data-stu-id="aa2ea-246">When you link to other technical articles, if you forget to include the space, the link will be broken in the published article.</span></span>

## <a name="links-to-pages-that-are-not-part-of-the-technical-documentation-set"></a><span data-ttu-id="aa2ea-247">链接到不属于技术文档集的页面</span><span class="sxs-lookup"><span data-stu-id="aa2ea-247">Links to pages that are not part of the technical documentation set</span></span>

<span data-ttu-id="aa2ea-248">若要链接到另一个 Microsoft 属性（例如定价页、SLA 页或其他非文档文章的页面），请使用绝对 URL，但要忽略区域设置。</span><span class="sxs-lookup"><span data-stu-id="aa2ea-248">To link to a page on another Microsoft property (such as a pricing page, SLA page, or anything else that is not a documentation article), use an absolute URL, but omit the locale.</span></span> <span data-ttu-id="aa2ea-249">这样做是为了使链接在 GitHub 和显示链接的网站上正常工作：</span><span class="sxs-lookup"><span data-stu-id="aa2ea-249">The goal here is that links work in GitHub and on the rendered site:</span></span>

   ```markdown
   [link text](https://azure.microsoft.com/pricing/details/virtual-machines/)
   ```

## <a name="links-to-third-party-sites"></a><span data-ttu-id="aa2ea-250">指向第三方网站的链接</span><span class="sxs-lookup"><span data-stu-id="aa2ea-250">Links to third-party sites</span></span>

<span data-ttu-id="aa2ea-251">为了实现最佳用户体验，最好尽量减少将用户定向到另一个网站的次数。</span><span class="sxs-lookup"><span data-stu-id="aa2ea-251">The best user experience minimizes sending users to another site.</span></span> <span data-ttu-id="aa2ea-252">因此，如果确实需要，可在以下信息基础上实现到第三方网站的任何链接：</span><span class="sxs-lookup"><span data-stu-id="aa2ea-252">So base any links to third-party sites, which we do sometimes need, on this info:</span></span>

- <span data-ttu-id="aa2ea-253">**责任性**：当要共享的信息是第三方信息时，链接到第三方内容。</span><span class="sxs-lookup"><span data-stu-id="aa2ea-253">**Accountability**: Link to third-party content when it's the third-party's information to share.</span></span> <span data-ttu-id="aa2ea-254">例如，告知用户如何使用 Android 开发人员工具并不是 Microsoft 的职责，此类信息可以通过 Google 获取。</span><span class="sxs-lookup"><span data-stu-id="aa2ea-254">For example, it's not Microsoft's place to tell people how to use Android developer tools--that is Google's story to tell.</span></span> <span data-ttu-id="aa2ea-255">如有需要，我们可以介绍如何将 Android 开发人员工具与  Azure 结合使用，但对于如何使用该工具，应向 Google 寻求帮助。</span><span class="sxs-lookup"><span data-stu-id="aa2ea-255">If we need to, we can explain how to use Android developer tools *with* Azure, but Google should tell the story of how to use their tools.</span></span>
- <span data-ttu-id="aa2ea-256">**PM 签名**：请求 Microsoft 在第三方内容上签名。</span><span class="sxs-lookup"><span data-stu-id="aa2ea-256">**PM signoff**: Request that Microsoft sign off on third-party content.</span></span> <span data-ttu-id="aa2ea-257">链接到此内容即表明我们信任此内容，并且有责任和义务让用户按说明操作。</span><span class="sxs-lookup"><span data-stu-id="aa2ea-257">By linking to it, we are saying something about our trust in it and our obligation if people follow the instructions.</span></span>
- <span data-ttu-id="aa2ea-258">**新鲜度评审**：确保第三方信息仍为最新、正确且相关的版本，并确保链接未经任何更改。</span><span class="sxs-lookup"><span data-stu-id="aa2ea-258">**Freshness reviews**: Make sure that the third-party info is still current, correct, and relevant, and that the link hasn't changed.</span></span>
- <span data-ttu-id="aa2ea-259">**跳转提醒**：确保用户知道他们即将转到另一个网站。</span><span class="sxs-lookup"><span data-stu-id="aa2ea-259">**Offsite**: Make users aware that they are going to another site.</span></span> <span data-ttu-id="aa2ea-260">如果上下文未明确指出这一点，请添加一个限定性句子。</span><span class="sxs-lookup"><span data-stu-id="aa2ea-260">If the context does not make that clear, add a qualifying phrase.</span></span> <span data-ttu-id="aa2ea-261">例如：“先决条件包括 Android 开发人员工具，你可以在 Android Studio 网站上进行下载。”</span><span class="sxs-lookup"><span data-stu-id="aa2ea-261">For example: "Prerequisites include the Android Developer Tools, which you can download on the Android Studio site."</span></span>
- <span data-ttu-id="aa2ea-262">**后续步骤**：在“后续步骤”部分，最好添加一个指向类似于 MVP 博客等内容的链接。</span><span class="sxs-lookup"><span data-stu-id="aa2ea-262">**Next steps**: It's fine to add a link to, say, an MVP blog in a "Next steps" section.</span></span> <span data-ttu-id="aa2ea-263">再次提醒，请务必使用户了解他们会离开当前网站。</span><span class="sxs-lookup"><span data-stu-id="aa2ea-263">Again, just make sure that users understand they'll be leaving the site.</span></span>
- <span data-ttu-id="aa2ea-264">**合法性**：合法遵守每个 microsoft.com 页面页脚“使用条款”中的“链接到第三方网站”规定   。</span><span class="sxs-lookup"><span data-stu-id="aa2ea-264">**Legal**: We are covered legally under **Links to Third Party Sites** in the **Terms of Use** footer on every microsoft.com page.</span></span>

<!-- link references -->
[CommonMark]: https://commonmark.org/
[Markdig]: https://github.com/lunet-io/markdig
[GFM]: https://help.github.com/categories/writing-on-github/
[docs]: https://docs.microsoft.com
[.NET API 浏览器]: https://docs.microsoft.com/dotnet/api/
[.NET API browser]: https://docs.microsoft.com/dotnet/api/
[Windows UWP]: https://docs.microsoft.com/uwp/api
[docsextension]: https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown
[自动完成网站]: https://xref.docs.microsoft.com/autocomplete?text=
[autocomplete site]: https://xref.docs.microsoft.com/autocomplete?text=
