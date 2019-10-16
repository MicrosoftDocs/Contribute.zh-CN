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
# <a name="using-links-in-documentation"></a><span data-ttu-id="74884-103">在文档中使用链接</span><span class="sxs-lookup"><span data-stu-id="74884-103">Using links in documentation</span></span>
<span data-ttu-id="74884-104">本文介绍如何使用 docs.microsoft.com 上托管页面的超链接。</span><span class="sxs-lookup"><span data-stu-id="74884-104">This article describes how to use hyperlinks from pages hosted at docs.microsoft.com.</span></span> <span data-ttu-id="74884-105">通过几种不同的约定，便可轻松地将链接添加到 markdown。</span><span class="sxs-lookup"><span data-stu-id="74884-105">Links are easy to add into markdown with a few varying conventions.</span></span> <span data-ttu-id="74884-106">链接将用户指向相同页面中的内容、其他相邻页面或外部站点和 URL。</span><span class="sxs-lookup"><span data-stu-id="74884-106">Links point users to content in the same page, point off into other neighboring pages, or point to external sites and URLs.</span></span>

<span data-ttu-id="74884-107">docs.microsoft.com 站点后端使用开放发布服务 (OPS)，支持通过 [Markdig](https://github.com/lunet-io/markdig) 分析引擎分析的 [CommonMark](https://commonmark.org/) 兼容 Markdown。</span><span class="sxs-lookup"><span data-stu-id="74884-107">The docs.microsoft.com site backend uses Open Publishing Services (OPS) which supports [CommonMark](https://commonmark.org/) compliant markdown parsed through the [Markdig](https://github.com/lunet-io/markdig) parsing engine.</span></span> <span data-ttu-id="74884-108">Markdown 风格大多与 [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/) 兼容，因为大多数 docs 存储在 GitHub 中，并可以在 GitHub 中进行编辑。</span><span class="sxs-lookup"><span data-stu-id="74884-108">This markdown flavor is mostly compatible with [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/), as most docs are stored in GitHub and can be edited there.</span></span> <span data-ttu-id="74884-109">通过 Markdown 扩展添加一些功能。</span><span class="sxs-lookup"><span data-stu-id="74884-109">Additional functionality is added through Markdown extensions.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="74884-110">只要目标支持（绝大多数都应支持），所有链接均必须是安全的（`https` 与 `http`）。</span><span class="sxs-lookup"><span data-stu-id="74884-110">All links must be secure (`https` vs `http`) whenever the target supports it (which the vast majority should).</span></span>

## <a name="link-text"></a><span data-ttu-id="74884-111">链接文本</span><span class="sxs-lookup"><span data-stu-id="74884-111">Link text</span></span>

<span data-ttu-id="74884-112">链接文本中使用的关键字应反映相关内容。</span><span class="sxs-lookup"><span data-stu-id="74884-112">The words that you include in link text should be friendly.</span></span> <span data-ttu-id="74884-113">换言之，它们应为一般中文关键字或所链接到的页面的标题。</span><span class="sxs-lookup"><span data-stu-id="74884-113">In other words, they should be normal English words or the title of the page that you're linking to.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="74884-114">请勿使用“单击此处”。</span><span class="sxs-lookup"><span data-stu-id="74884-114">Do not use "click here."</span></span> <span data-ttu-id="74884-115">这不利于搜索引擎优化，也不能充分地描述目标网页。</span><span class="sxs-lookup"><span data-stu-id="74884-115">It's bad for search engine optimization, and doesn't adequately describe the target.</span></span>

<span data-ttu-id="74884-116">**正确：**</span><span class="sxs-lookup"><span data-stu-id="74884-116">**Correct:**</span></span>

- `For more information, see the [contributor guide index](https://github.com/Azure/azure-content/blob/master/contributor-guide/contributor-guide-index.md).`

- `For more details, see the [SET TRANSACTION ISOLATION LEVEL](https://msdn.microsoft.com/library/ms173763.aspx) reference.`

<span data-ttu-id="74884-117">**不正确：**</span><span class="sxs-lookup"><span data-stu-id="74884-117">**Incorrect:**</span></span>

- `For more details, see [https://msdn.microsoft.com/library/ms173763.aspx](https://msdn.microsoft.com/library/ms173763.aspx).`

- `For more information, click [here](https://github.com/Azure/azure-content/blob/master/contributor-guide/contributor-guide-index.md).`

## <a name="links-from-one-article-to-another"></a><span data-ttu-id="74884-118">从一篇文章链接到另一篇文章</span><span class="sxs-lookup"><span data-stu-id="74884-118">Links from one article to another</span></span>

<span data-ttu-id="74884-119">要在同一 docset 中创建从一篇 Docs 技术文章到另一篇 Docs 技术文章的内联链接，请使用以下链接语法：</span><span class="sxs-lookup"><span data-stu-id="74884-119">To create an inline link from a Docs technical article to another Docs technical article within the same docset, use the following link syntax:</span></span>

- <span data-ttu-id="74884-120">目录中的一篇文章链接到同一目录中的另一篇文章：</span><span class="sxs-lookup"><span data-stu-id="74884-120">An article in a directory links to another article in the same directory:</span></span>

  `[link text](article-name.md)`

- <span data-ttu-id="74884-121">子目录中的一篇文章链接到根目录中的一篇文章：</span><span class="sxs-lookup"><span data-stu-id="74884-121">An article links from a subdirectory to an article in the root directory:</span></span>

  `[link text](../article-name.md)`

- <span data-ttu-id="74884-122">根目录中的一篇文章链接到子目录中的一篇文章：</span><span class="sxs-lookup"><span data-stu-id="74884-122">An article in the root directory links to an article in a subdirectory:</span></span>

  `[link text](./directory/article-name.md)`

- <span data-ttu-id="74884-123">子目录中的一篇文章链接到另一个子目录中的一篇文章：</span><span class="sxs-lookup"><span data-stu-id="74884-123">An article in a subdirectory links to an article in another subdirectory:</span></span>

  `[link text](../directory/article-name.md)`

- <span data-ttu-id="74884-124">跨 docset 链接的文章（即使在同一存储库中）： `[link text](./directory/article-name)`</span><span class="sxs-lookup"><span data-stu-id="74884-124">An article linking across docsets (even if in the same repository):  `[link text](./directory/article-name)`</span></span>

> [!IMPORTANT]
> <span data-ttu-id="74884-125">上述示例中均未在链接中使用 `~/`。</span><span class="sxs-lookup"><span data-stu-id="74884-125">None of the above examples use the `~/` as part of the link.</span></span> <span data-ttu-id="74884-126">如果要链接到存储库的根路径，请以 `/` 开头。</span><span class="sxs-lookup"><span data-stu-id="74884-126">If you are linking to a path at the root of the repository, start with the `/`.</span></span> <span data-ttu-id="74884-127">如果包含 `~/`，当在 GitHub 上导航源存储库时会生成无效的链接。</span><span class="sxs-lookup"><span data-stu-id="74884-127">Including the `~/` produces invalid links when navigating the source repositories on GitHub.</span></span> <span data-ttu-id="74884-128">使路径以 `/` 开头便可有效解决此问题。</span><span class="sxs-lookup"><span data-stu-id="74884-128">Starting the path with `/` resolves correctly.</span></span>

## <a name="links-to-anchors"></a><span data-ttu-id="74884-129">链接到锚点</span><span class="sxs-lookup"><span data-stu-id="74884-129">Links to anchors</span></span>

<span data-ttu-id="74884-130">不必创建锚点。</span><span class="sxs-lookup"><span data-stu-id="74884-130">You do not have to create anchors.</span></span> <span data-ttu-id="74884-131">它们在发布时会自动生成，用于所有 H2 标题。</span><span class="sxs-lookup"><span data-stu-id="74884-131">They're automatically generated at publishing time for all H2 headings.</span></span> <span data-ttu-id="74884-132">只需要创建到 H2 部分的链接。</span><span class="sxs-lookup"><span data-stu-id="74884-132">The only thing you have to do is create links to the H2 sections.</span></span>

- <span data-ttu-id="74884-133">链接到同一篇文章中的标题：</span><span class="sxs-lookup"><span data-stu-id="74884-133">To link to a heading within the same article:</span></span>

  `[link](#the-text-of-the-H2-section-separated-by-hyphens)`
  `[Create cache](#create-cache)`

- <span data-ttu-id="74884-134">链接到同一子目录中另一篇文章中的锚点：</span><span class="sxs-lookup"><span data-stu-id="74884-134">To link to an anchor in another article in the same subdirectory:</span></span>

  `[link text](article-name.md#anchor-name)`
  `[Configure your profile](media-services-create-account.md#configure-your-profile)`

- <span data-ttu-id="74884-135">链接到另一个服务子目录中的锚点：</span><span class="sxs-lookup"><span data-stu-id="74884-135">To link to an anchor in another service subdirectory:</span></span>

  `[link text](../directory/article-name.md#anchor-name)`
  `[Configure your profile](../directory/media-services-create-account.md#configure-your-profile)`

## <a name="links-from-includes"></a><span data-ttu-id="74884-136">从包含文件链接</span><span class="sxs-lookup"><span data-stu-id="74884-136">Links from includes</span></span>

<span data-ttu-id="74884-137">包含文件位于另一个目录中，因此，必须使用较长的相对路径。</span><span class="sxs-lookup"><span data-stu-id="74884-137">Because include files are located in another directory, you must use longer relative paths.</span></span> <span data-ttu-id="74884-138">若要从包含文件链接到某一篇文章，请使用以下格式：</span><span class="sxs-lookup"><span data-stu-id="74884-138">To link to an article from an include file, use this format:</span></span>

   ```markdown
   [link text](../articles/folder/article-name.md)
   ```

## <a name="links-in-selectors"></a><span data-ttu-id="74884-139">选择器中的链接</span><span class="sxs-lookup"><span data-stu-id="74884-139">Links in selectors</span></span>

<span data-ttu-id="74884-140">选择器是导航组件，以下拉列表的形式在文档文章中显示。</span><span class="sxs-lookup"><span data-stu-id="74884-140">A selector is a navigation component that appears in a docs article as a drop-down list.</span></span> <span data-ttu-id="74884-141">当读者选择下拉列表中的值时，浏览器将打开所选文章。</span><span class="sxs-lookup"><span data-stu-id="74884-141">When a reader selects a value in the drop-down, the browser opens the selected article.</span></span> <span data-ttu-id="74884-142">通常情况下，选择器列表包含密切相关文章的链接，例如，多种编程语言中的相同主题，或密切相关的文章系列。</span><span class="sxs-lookup"><span data-stu-id="74884-142">Typically the selector list contains links to closely related articles, for example the same subject matter in multiple programming languages or a closely related series of articles.</span></span> 

<span data-ttu-id="74884-143">如果你的选择器嵌入在包含文件中，则使用以下链接结构：</span><span class="sxs-lookup"><span data-stu-id="74884-143">If you have selectors that are embedded in an include, use the following link structure:</span></span>

   ```markdown
   > [AZURE.SELECTOR-LIST (Dropdown1 | Dropdown2 )]
   - [(Text1 | Example1 )](../articles/folder/article-name1.md)
   - [(Text1 | Example2 )](../articles/folder/article-name2.md)
   - [(Text2 | Example3 )](../articles/folder/article-name3.md)
   - [(Text2 | Example4 )](../articles/folder/article-name4.md) -->
   ```

## <a name="reference-style-links"></a><span data-ttu-id="74884-144">引用样式链接</span><span class="sxs-lookup"><span data-stu-id="74884-144">Reference-style links</span></span>

<span data-ttu-id="74884-145">可以使用引用样式链接使源内容更易于读取。</span><span class="sxs-lookup"><span data-stu-id="74884-145">You can use reference-style links to make your source content easier to read.</span></span> <span data-ttu-id="74884-146">引用样式链接使用简化的语法替代内联链接语法，以便将长 URL 移动到文章末尾。</span><span class="sxs-lookup"><span data-stu-id="74884-146">Reference-style links replace inline link syntax with simplified syntax that allows you to move the long URLs to the end of the article.</span></span> <span data-ttu-id="74884-147">下面是 [Daring Fireball](https://daringfireball.net/projects/markdown/) 的示例：</span><span class="sxs-lookup"><span data-stu-id="74884-147">Here's [Daring Fireball](https://daringfireball.net/projects/markdown/) 's example:</span></span>

<span data-ttu-id="74884-148">内联文本：</span><span class="sxs-lookup"><span data-stu-id="74884-148">Inline text:</span></span>

   ```markdown
   I get 10 times more traffic from [Google][1] than from [Yahoo][2] or [MSN][3].
   ```

<span data-ttu-id="74884-149">文章末尾部分的链接引用：</span><span class="sxs-lookup"><span data-stu-id="74884-149">Link references at the end of the article:</span></span>

   ```markdown
   <!--Reference links in article-->
   [1]: http://google.com/
   [2]: http://search.yahoo.com/
   [3]: http://search.msn.com/
   ```
   
<span data-ttu-id="74884-150">请务必在链接前的冒号后加入空格。</span><span class="sxs-lookup"><span data-stu-id="74884-150">Make sure that you include the space after the colon, before the link.</span></span> <span data-ttu-id="74884-151">链接到其他技术文章时，如果忘记加入空格，链接会在发布文章中被破坏。</span><span class="sxs-lookup"><span data-stu-id="74884-151">When you link to other technical articles, if you forget to include the space, the link will be broken in the published article.</span></span>

## <a name="links-to-pages-that-are-not-part-of-the-technical-documentation-set"></a><span data-ttu-id="74884-152">链接到不属于技术文档集的页面</span><span class="sxs-lookup"><span data-stu-id="74884-152">Links to pages that are not part of the technical documentation set</span></span>

<span data-ttu-id="74884-153">若要链接到另一个 Microsoft 属性（例如定价页、SLA 页或其他非文档文章的页面），请使用绝对 URL，但要忽略区域设置。</span><span class="sxs-lookup"><span data-stu-id="74884-153">To link to a page on another Microsoft property (such as a pricing page, SLA page, or anything else that is not a documentation article), use an absolute URL, but omit the locale.</span></span> <span data-ttu-id="74884-154">这样做是为了使链接在 GitHub 和显示链接的网站上正常工作：</span><span class="sxs-lookup"><span data-stu-id="74884-154">The goal here is that links work in GitHub and on the rendered site:</span></span>

   ```markdown
   [link text](https://azure.microsoft.com/pricing/details/virtual-machines/)
   ```
   
## <a name="links-to-third-party-sites"></a><span data-ttu-id="74884-155">指向第三方网站的链接</span><span class="sxs-lookup"><span data-stu-id="74884-155">Links to third-party sites</span></span>

<span data-ttu-id="74884-156">为了实现最佳用户体验，最好尽量减少将用户定向到另一个网站的次数。</span><span class="sxs-lookup"><span data-stu-id="74884-156">The best user experience minimizes sending users to another site.</span></span> <span data-ttu-id="74884-157">因此，如果确实需要，可在以下信息基础上实现到第三方网站的任何链接：</span><span class="sxs-lookup"><span data-stu-id="74884-157">So base any links to third-party sites, which we do sometimes need, on this info:</span></span>

- <span data-ttu-id="74884-158">**责任性**：当要共享的信息是第三方信息时，链接到第三方内容。</span><span class="sxs-lookup"><span data-stu-id="74884-158">**Accountability**: Link to third-party content when it's the third-party's information to share.</span></span> <span data-ttu-id="74884-159">例如，告知用户如何使用 Android 开发人员工具并不是 Microsoft 的职责，此类信息可以通过 Google 获取。</span><span class="sxs-lookup"><span data-stu-id="74884-159">For example, it's not Microsoft's place to tell people how to use Android developer tools--that is Google's story to tell.</span></span> <span data-ttu-id="74884-160">如有需要，我们可以介绍如何将 Android 开发人员工具与  Azure 结合使用，但对于如何使用该工具，应向 Google 寻求帮助。</span><span class="sxs-lookup"><span data-stu-id="74884-160">If we need to, we can explain how to use Android developer tools *with* Azure, but Google should tell the story of how to use their tools.</span></span>
- <span data-ttu-id="74884-161">**PM 签名**：请求 Microsoft 在第三方内容上签名。</span><span class="sxs-lookup"><span data-stu-id="74884-161">**PM signoff**: Request that Microsoft sign off on third-party content.</span></span> <span data-ttu-id="74884-162">链接到此内容即表明我们信任此内容，并且有责任和义务让用户按说明操作。</span><span class="sxs-lookup"><span data-stu-id="74884-162">By linking to it, we are saying something about our trust in it and our obligation if people follow the instructions.</span></span>
- <span data-ttu-id="74884-163">**新鲜度评审**：确保第三方信息仍为最新、正确且相关的版本，并确保链接未经任何更改。</span><span class="sxs-lookup"><span data-stu-id="74884-163">**Freshness reviews**: Make sure that the third-party info is still current, correct, and relevant, and that the link hasn’t changed.</span></span>
- <span data-ttu-id="74884-164">**跳转提醒**：确保用户知道他们即将转到另一个网站。</span><span class="sxs-lookup"><span data-stu-id="74884-164">**Offsite**: Make users aware that they are going to another site.</span></span> <span data-ttu-id="74884-165">如果上下文未明确指出这一点，请添加一个限定性句子。</span><span class="sxs-lookup"><span data-stu-id="74884-165">If the context does not make that clear, add a qualifying phrase.</span></span> <span data-ttu-id="74884-166">例如：“先决条件包括 Android 开发人员工具，你可以在 Android Studio 网站上进行下载。”</span><span class="sxs-lookup"><span data-stu-id="74884-166">For example: “Prerequisites include the Android Developer Tools, which you can download on the Android Studio site.”</span></span>
- <span data-ttu-id="74884-167">**后续步骤**：在“后续步骤”部分，最好添加一个指向类似于 MVP 博客等内容的链接。</span><span class="sxs-lookup"><span data-stu-id="74884-167">**Next steps**: It’s fine to add a link to, say, an MVP blog in a "Next steps" section.</span></span> <span data-ttu-id="74884-168">再次提醒，请务必使用户了解他们会离开当前网站。</span><span class="sxs-lookup"><span data-stu-id="74884-168">Again, just make sure that users understand they’ll be leaving the site.</span></span>
- <span data-ttu-id="74884-169">**合法性**：合法遵守每个 ms.com 页面页脚“使用条款”  中的“链接到第三方网站”  规定。</span><span class="sxs-lookup"><span data-stu-id="74884-169">**Legal**: We are covered legally under **Links to Third Party Sites** in the **Terms of Use** footer on every ms.com page.</span></span>

## <a name="links-to-msdn-or-technet"></a><span data-ttu-id="74884-170">链接到 MSDN 或 TechNet</span><span class="sxs-lookup"><span data-stu-id="74884-170">Links to MSDN or TechNet</span></span>

<span data-ttu-id="74884-171">如果需要链接到 MSDN 或 TechNet，请使用主题的完整链接，并从链接中删除“en-us”语言区域设置。</span><span class="sxs-lookup"><span data-stu-id="74884-171">When you need to link to MSDN or TechNet, use the full link to the topic, and remove the "en-us" language locale from the link.</span></span>

## <a name="links-to-azure-powershell-reference-content"></a><span data-ttu-id="74884-172">链接到 Azure PowerShell 引用内容</span><span class="sxs-lookup"><span data-stu-id="74884-172">Links to Azure PowerShell reference content</span></span>

<span data-ttu-id="74884-173">自 2016 年 11 月以来，Azure PowerShell 引用内容已经经历了若干次变更。</span><span class="sxs-lookup"><span data-stu-id="74884-173">The Azure PowerShell reference content has been through several changes since November 2016.</span></span> <span data-ttu-id="74884-174">使用以下准则从 docs.microsoft.com 的其他文章链接到此内容。</span><span class="sxs-lookup"><span data-stu-id="74884-174">Use the following guidelines for linking to this content from other articles on docs.microsoft.com.</span></span>

<span data-ttu-id="74884-175">URL 结构：</span><span class="sxs-lookup"><span data-stu-id="74884-175">Structure of the URL:</span></span>

* <span data-ttu-id="74884-176">对于 cmdlet：</span><span class="sxs-lookup"><span data-stu-id="74884-176">For cmdlets:</span></span>
  - `/powershell/module/<module-name>/<cmdlet-name>[?view=<moniker-name>]`
* <span data-ttu-id="74884-177">对于概念主题：</span><span class="sxs-lookup"><span data-stu-id="74884-177">For conceptual topics:</span></span>
  - `/powershell/azure/<topic-file-name>[?view=<moniker-name>]`
  - `/powershell/azure/<service-name>/<topic-file-name>[?view=<moniker-name>]`

<span data-ttu-id="74884-178">`<moniker-name>` 部分是可选的。</span><span class="sxs-lookup"><span data-stu-id="74884-178">The `<moniker-name>` portion is optional.</span></span> <span data-ttu-id="74884-179">如果省略这一部分，会将用户定向到最新版本的内容。</span><span class="sxs-lookup"><span data-stu-id="74884-179">If it's omitted, you will be directed to the latest version of the content.</span></span> <span data-ttu-id="74884-180">`<service-name>` 部分是以下基 URL 中显示的其中一个示例：</span><span class="sxs-lookup"><span data-stu-id="74884-180">The `<service-name>` portion is one of the examples shown in the following base URLs:</span></span>

- <span data-ttu-id="74884-181">Azure PowerShell (AzureRM) 内容：[https://docs.microsoft.com/powershell/azure/](https://docs.microsoft.com/powershell/azure/)</span><span class="sxs-lookup"><span data-stu-id="74884-181">Azure PowerShell (AzureRM) content: [https://docs.microsoft.com/powershell/azure/](https://docs.microsoft.com/powershell/azure/)</span></span>
- <span data-ttu-id="74884-182">Azure PowerShell (ASM) 内容：[https://docs.microsoft.com/powershell/azure/_servicemanagement_](https://docs.microsoft.com/powershell/azure/servicemanagement)</span><span class="sxs-lookup"><span data-stu-id="74884-182">Azure PowerShell (ASM) content: [https://docs.microsoft.com/powershell/azure/_servicemanagement_](https://docs.microsoft.com/powershell/azure/servicemanagement)</span></span>
- <span data-ttu-id="74884-183">Azure Active Directory (AzureAD) PowerShell 内容：[https://docs.microsoft.com/powershell/azure/_active-directory_](https://docs.microsoft.com/powershell/azure/active-directory)</span><span class="sxs-lookup"><span data-stu-id="74884-183">Azure Active Directory (AzureAD) PowerShell content: [https://docs.microsoft.com/powershell/azure/_active-directory_](https://docs.microsoft.com/powershell/azure/active-directory)</span></span>
- <span data-ttu-id="74884-184">Azure Service Fabric PowerShell：[https://docs.microsoft.com/powershell/azure/_service-fabric_](https://docs.microsoft.com/powershell/azure/service-fabric)</span><span class="sxs-lookup"><span data-stu-id="74884-184">Azure Service Fabric PowerShell: [https://docs.microsoft.com/powershell/azure/_service-fabric_](https://docs.microsoft.com/powershell/azure/service-fabric)</span></span>
- <span data-ttu-id="74884-185">Azure 信息保护 PowerShell：[https://docs.microsoft.com/powershell/azure/_aip_](https://docs.microsoft.com/powershell/azure/aip)</span><span class="sxs-lookup"><span data-stu-id="74884-185">Azure Information Protection PowerShell: [https://docs.microsoft.com/powershell/azure/_aip_](https://docs.microsoft.com/powershell/azure/aip)</span></span>
- <span data-ttu-id="74884-186">Azure 弹性数据库作业 PowerShell：[https://docs.microsoft.com/powershell/azure/_elasticdbjobs_](https://docs.microsoft.com/powershell/azure/elasticdbjobs)</span><span class="sxs-lookup"><span data-stu-id="74884-186">Azure Elastic DB Jobs PowerShell: [https://docs.microsoft.com/powershell/azure/_elasticdbjobs_](https://docs.microsoft.com/powershell/azure/elasticdbjobs)</span></span>

<span data-ttu-id="74884-187">在使用这些 URL 时，会将用户重定向到最新版本的内容。</span><span class="sxs-lookup"><span data-stu-id="74884-187">When you use these URLs, you will be redirected to the latest version of the content.</span></span> <span data-ttu-id="74884-188">这样就不必指定版本名字对象。</span><span class="sxs-lookup"><span data-stu-id="74884-188">This way, you don't have to specify a version moniker.</span></span> <span data-ttu-id="74884-189">并且不会有指向版本更改时必须进行更新的概念内容的链接。</span><span class="sxs-lookup"><span data-stu-id="74884-189">And you won't have links to conceptual content that must be updated when the version changes.</span></span>

<span data-ttu-id="74884-190">若要创建正确的链接，可以在浏览器中找到要链接的页面并复制 URL。</span><span class="sxs-lookup"><span data-stu-id="74884-190">To create the correct link, find the page that you want to link to in your browser, and copy the URL.</span></span>
<span data-ttu-id="74884-191">然后，删除 `https://docs.microsoft.com` 和区域设置信息。</span><span class="sxs-lookup"><span data-stu-id="74884-191">Then, remove  `https://docs.microsoft.com` and the locale info.</span></span>

<span data-ttu-id="74884-192">从 TOC 进行链接时，必须使用完整的 URL（不包含区域设置信息）。</span><span class="sxs-lookup"><span data-stu-id="74884-192">When you're linking from a TOC, you must use the full URL without the locale information.</span></span>

<span data-ttu-id="74884-193">示例 Markdown：</span><span class="sxs-lookup"><span data-stu-id="74884-193">Example markdown:</span></span>

```markdown
[Get-AzureRmResourceGroup](/powershell/module/azurerm.resources/get-azurermresourcegroup)
[Get-AzureRmResourceGroup](/powershell/module/azurerm.resources/get-azurermresourcegroup?view=azurermps-4.1.0)
[New-AzureVM](/powershell/module/azure/new-azurevm?view=azuresmps-4.0.0)
[New-AzureRmVM](/powershell/module/azurerm.compute/new-azurermvm)
[Install Azure PowerShell for Service Management](/powershell/azure/servicemanagement/install-azurerm-ps)
[Install Azure PowerShell](/powershell/azure/install-azurerm-ps)
```
