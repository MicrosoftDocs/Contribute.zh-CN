---
title: 如何在文档中使用链接
description: 本文指导如何在 docs.microsoft.com 中创建内容链接。
author: bryanla
ms.author: bryanla
manager: mbaldwin
ms.date: 06/29/2017
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.custom: external-contributor-guide
ms.openlocfilehash: 1699e57ac6a4dc4c5a1ef099ea183b3cbc6307cd
ms.sourcegitcommit: de6e6b6ca641fdd5b30eb46deee9ac3a500089ef
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/26/2018
---
# <a name="using-links-in-documentation"></a><span data-ttu-id="90865-103">在文档中使用链接</span><span class="sxs-lookup"><span data-stu-id="90865-103">Using links in documentation</span></span>
<span data-ttu-id="90865-104">本文介绍如何使用 docs.microsoft.com 上托管页面的超链接。通过几种不同的约定，便可轻松地将链接添加到 markdown。</span><span class="sxs-lookup"><span data-stu-id="90865-104">This article describes how to use hyperlinks from pages hosted at docs.microsoft.com. Links are easy to add into markdown with a few varying conventions.</span></span> <span data-ttu-id="90865-105">链接将用户指向相同页面中的内容、其他相邻页面或外部站点和 URL。</span><span class="sxs-lookup"><span data-stu-id="90865-105">Links point users to content in the same page, point off into other neighboring pages, or point to external sites and URLs.</span></span>

<span data-ttu-id="90865-106">docs.microsoft.com 站点后端使用实现 DocFX Flavored Markdown (DFM) 的公开发布服务 (OPS)。</span><span class="sxs-lookup"><span data-stu-id="90865-106">The docs.microsoft.com site backend uses Open Publishing Services (OPS) which implements DocFX Flavored Markdown (DFM).</span></span> <span data-ttu-id="90865-107">DFM 与 GitHub Flavored Markdown (GFM) 高度兼容，并且 DFM 通过 Markdown 扩展添加了附加功能。</span><span class="sxs-lookup"><span data-stu-id="90865-107">DFM is highly compatible with GitHub Flavored Markdown (GFM), and DFM adds additional functionality through Markdown extensions.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="90865-108">只要目标支持（绝大多数都应支持），所有链接均必须是安全的（`https` 与 `http`）。</span><span class="sxs-lookup"><span data-stu-id="90865-108">All links must be secure (`https` vs `http`) whenever the target supports it (which the vast majority should).</span></span>

## <a name="link-text"></a><span data-ttu-id="90865-109">链接文本</span><span class="sxs-lookup"><span data-stu-id="90865-109">Link text</span></span>

<span data-ttu-id="90865-110">链接文本中使用的关键字应反映相关内容。</span><span class="sxs-lookup"><span data-stu-id="90865-110">The words that you include in link text should be friendly.</span></span> <span data-ttu-id="90865-111">换言之，它们应为一般中文关键字或所链接到的页面的标题。</span><span class="sxs-lookup"><span data-stu-id="90865-111">In other words, they should be normal English words or the title of the page that you're linking to.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="90865-112">请勿使用“单击此处”。</span><span class="sxs-lookup"><span data-stu-id="90865-112">Do not use "click here."</span></span> <span data-ttu-id="90865-113">这不利于 SEO，也不能充分地描述目标网页。</span><span class="sxs-lookup"><span data-stu-id="90865-113">It's bad for SEO and doesn't adequately describe the target.</span></span>

<span data-ttu-id="90865-114">**正确：**</span><span class="sxs-lookup"><span data-stu-id="90865-114">**Correct:**</span></span>

- `For more information, see the [contributor guide index](https://github.com/Azure/azure-content/blob/master/contributor-guide/contributor-guide-index.md).`

- `For more details, see the [SET TRANSACTION ISOLATION LEVEL](https://msdn.microsoft.com/library/ms173763.aspx) reference.`

<span data-ttu-id="90865-115">**不正确：**</span><span class="sxs-lookup"><span data-stu-id="90865-115">**Incorrect:**</span></span>

- `For more details, see [https://msdn.microsoft.com/library/ms173763.aspx](https://msdn.microsoft.com/library/ms173763.aspx).`

- `For more information, click [here](https://github.com/Azure/azure-content/blob/master/contributor-guide/contributor-guide-index.md).`

## <a name="links-from-one-article-to-another"></a><span data-ttu-id="90865-116">从一篇文章链接到另一篇文章</span><span class="sxs-lookup"><span data-stu-id="90865-116">Links from one article to another</span></span>

<span data-ttu-id="90865-117">要在同一 docset 中创建从一篇 Docs 技术文章到另一篇 Docs 技术文章的内联链接，请使用以下链接语法：</span><span class="sxs-lookup"><span data-stu-id="90865-117">To create an inline link from a Docs technical article to another Docs technical article within the same docset, use the following link syntax:</span></span>

- <span data-ttu-id="90865-118">目录中的一篇文章链接到同一目录中的另一篇文章：</span><span class="sxs-lookup"><span data-stu-id="90865-118">An article in a directory links to another article in the same directory:</span></span>

  `[link text](article-name.md)`

- <span data-ttu-id="90865-119">子目录中的一篇文章链接到根目录中的一篇文章：</span><span class="sxs-lookup"><span data-stu-id="90865-119">An article links from a subdirectory to an article in the root directory:</span></span>

  `[link text](../article-name.md)`

- <span data-ttu-id="90865-120">根目录中的一篇文章链接到子目录中的一篇文章：</span><span class="sxs-lookup"><span data-stu-id="90865-120">An article in the root directory links to an article in a subdirectory:</span></span>

  `[link text](./directory/article-name.md)`

- <span data-ttu-id="90865-121">子目录中的一篇文章链接到另一个子目录中的一篇文章：</span><span class="sxs-lookup"><span data-stu-id="90865-121">An article in a subdirectory links to an article in another subdirectory:</span></span>

  `[link text](../directory/article-name.md)`

- <span data-ttu-id="90865-122">跨 docset 链接的文章（即使在同一存储库中）：`[link text](./directory/article-name)`</span><span class="sxs-lookup"><span data-stu-id="90865-122">An article linking across docsets (even if in the same repository): `[link text](./directory/article-name)`</span></span>
  
## <a name="links-to-anchors"></a><span data-ttu-id="90865-123">链接到锚点</span><span class="sxs-lookup"><span data-stu-id="90865-123">Links to anchors</span></span>

<span data-ttu-id="90865-124">不必创建锚点。</span><span class="sxs-lookup"><span data-stu-id="90865-124">You do not have to create anchors.</span></span> <span data-ttu-id="90865-125">它们在发布时会自动生成，用于所有 H2 标题。</span><span class="sxs-lookup"><span data-stu-id="90865-125">They're automatically generated at publishing time for all H2 headings.</span></span> <span data-ttu-id="90865-126">只需要创建到 H2 部分的链接。</span><span class="sxs-lookup"><span data-stu-id="90865-126">The only thing you have to do is create links to the H2 sections.</span></span>

- <span data-ttu-id="90865-127">链接到同一篇文章中的标题：</span><span class="sxs-lookup"><span data-stu-id="90865-127">To link to a heading within the same article:</span></span>

  `[link](#the-text-of-the-H2-section-separated-by-hyphens)`
  `[Create cache](#create-cache)`

- <span data-ttu-id="90865-128">链接到同一子目录中另一篇文章中的锚点：</span><span class="sxs-lookup"><span data-stu-id="90865-128">To link to an anchor in another article in the same subdirectory:</span></span>

  `[link text](article-name.md#anchor-name)`
  `[Configure your profile](media-services-create-account.md#configure-your-profile)`

- <span data-ttu-id="90865-129">链接到另一个服务子目录中的锚点：</span><span class="sxs-lookup"><span data-stu-id="90865-129">To link to an anchor in another service subdirectory:</span></span>

  `[link text](../directory/article-name.md#anchor-name)`
  `[Configure your profile](../directory/media-services-create-account.md#configure-your-profile)`

## <a name="links-from-includes"></a><span data-ttu-id="90865-130">从包含文件链接</span><span class="sxs-lookup"><span data-stu-id="90865-130">Links from includes</span></span>

<span data-ttu-id="90865-131">包含文件位于另一个目录中，因此，必须使用较长的相对路径。</span><span class="sxs-lookup"><span data-stu-id="90865-131">Because include files are located in another directory, you must use longer relative paths.</span></span> <span data-ttu-id="90865-132">若要从包含文件链接到某一篇文章，请使用以下格式：</span><span class="sxs-lookup"><span data-stu-id="90865-132">To link to an article from an include file, use this format:</span></span>

    [link text](../articles/folder/article-name.md)

## <a name="links-in-selectors"></a><span data-ttu-id="90865-133">选择器中的链接</span><span class="sxs-lookup"><span data-stu-id="90865-133">Links in selectors</span></span>

<span data-ttu-id="90865-134">如果你的选择器嵌入在包含文件中（如同 Azure 文档团队处理的那样），则使用以下链接结构：</span><span class="sxs-lookup"><span data-stu-id="90865-134">If you have selectors that are embedded in an include--as does the Azure documentation team--use the following link structure:</span></span>

    > <span data-ttu-id="90865-135">[AZURE.SELECTOR-LIST (Dropdown1 | Dropdown2 )]</span><span class="sxs-lookup"><span data-stu-id="90865-135">[AZURE.SELECTOR-LIST (Dropdown1 | Dropdown2 )]</span></span>
    - [<span data-ttu-id="90865-136">(Text1 | Example1 )</span><span class="sxs-lookup"><span data-stu-id="90865-136">(Text1 | Example1 )</span></span>](../articles/folder/article-name1.md)
    - [<span data-ttu-id="90865-137">(Text1 | Example2 )</span><span class="sxs-lookup"><span data-stu-id="90865-137">(Text1 | Example2 )</span></span>](../articles/folder/article-name2.md)
    - [<span data-ttu-id="90865-138">(Text2 | Example3 )</span><span class="sxs-lookup"><span data-stu-id="90865-138">(Text2 | Example3 )</span></span>](../articles/folder/article-name3.md)
    - <span data-ttu-id="90865-139">[(Text2 | Example4 )](../articles/folder/article-name4.md) --></span><span class="sxs-lookup"><span data-stu-id="90865-139">[(Text2 | Example4 )](../articles/folder/article-name4.md) --></span></span>

## <a name="reference-style-links"></a><span data-ttu-id="90865-140">引用样式链接</span><span class="sxs-lookup"><span data-stu-id="90865-140">Reference-style links</span></span>

<span data-ttu-id="90865-141">可以使用引用样式链接使源内容更易于读取。</span><span class="sxs-lookup"><span data-stu-id="90865-141">You can use reference-style links to make your source content easier to read.</span></span> <span data-ttu-id="90865-142">引用样式链接使用简化的语法替代内联链接语法，以便将长 URL 移动到文章末尾。</span><span class="sxs-lookup"><span data-stu-id="90865-142">Reference-style links replace inline link syntax with simplified syntax that allows you to move the long URLs to the end of the article.</span></span> <span data-ttu-id="90865-143">下面是 [Daring Fireball](https://daringfireball.net/projects/markdown/) 的示例：</span><span class="sxs-lookup"><span data-stu-id="90865-143">Here's [Daring Fireball](https://daringfireball.net/projects/markdown/) 's example:</span></span>

<span data-ttu-id="90865-144">内联文本：</span><span class="sxs-lookup"><span data-stu-id="90865-144">Inline text:</span></span>

    I get 10 times more traffic from [Google][1] than from [Yahoo][2] or [MSN][3].

<span data-ttu-id="90865-145">文章末尾部分的链接引用：</span><span class="sxs-lookup"><span data-stu-id="90865-145">Link references at the end of the article:</span></span>

    <!--Reference links in article-->
    [1]: http://google.com/
    [2]: http://search.yahoo.com/
    [3]: http://search.msn.com/

<span data-ttu-id="90865-146">请务必在链接前的冒号后加入空格。</span><span class="sxs-lookup"><span data-stu-id="90865-146">Make sure that you include the space after the colon, before the link.</span></span> <span data-ttu-id="90865-147">链接到其他技术文章时，如果忘记加入空格，链接会在发布文章中被破坏。</span><span class="sxs-lookup"><span data-stu-id="90865-147">When you link to other technical articles, if you forget to include the space, the link will be broken in the published article.</span></span>

## <a name="links-to-pages-that-are-not-part-of-the-technical-documentation-set"></a><span data-ttu-id="90865-148">链接到不属于技术文档集的页面</span><span class="sxs-lookup"><span data-stu-id="90865-148">Links to pages that are not part of the technical documentation set</span></span>

<span data-ttu-id="90865-149">若要链接到另一个 Microsoft 属性（例如定价页、SLA 页或其他非文档文章的页面），请使用绝对 URL，但要忽略区域设置。</span><span class="sxs-lookup"><span data-stu-id="90865-149">To link to a page on another Microsoft property (such as a pricing page, SLA page, or anything else that is not a documentation article), use an absolute URL, but omit the locale.</span></span> <span data-ttu-id="90865-150">这样做是为了使链接在 GitHub 和显示链接的网站上正常工作：</span><span class="sxs-lookup"><span data-stu-id="90865-150">The goal here is that links work in GitHub and on the rendered site:</span></span>

    [link text](https://azure.microsoft.com/pricing/details/virtual-machines/)

## <a name="links-to-third-party-sites"></a><span data-ttu-id="90865-151">指向第三方网站的链接</span><span class="sxs-lookup"><span data-stu-id="90865-151">Links to third-party sites</span></span>

<span data-ttu-id="90865-152">为了实现最佳用户体验，最好尽量减少将用户定向到另一个网站的次数。</span><span class="sxs-lookup"><span data-stu-id="90865-152">The best user experience minimizes sending users to another site.</span></span> <span data-ttu-id="90865-153">因此，如果确实需要，可在以下信息基础上实现到第三方网站的任何链接：</span><span class="sxs-lookup"><span data-stu-id="90865-153">So base any links to third-party sites, which we do sometimes need, on this info:</span></span>

- <span data-ttu-id="90865-154">**责任性**：当要共享的信息是第三方信息时，链接到第三方内容。</span><span class="sxs-lookup"><span data-stu-id="90865-154">**Accountability**: Link to third-party content when it's the third-party's information to share.</span></span> <span data-ttu-id="90865-155">例如，告知用户如何使用 Android 开发人员工具并不是 Microsoft 的职责，此类信息可以通过 Google 获取。</span><span class="sxs-lookup"><span data-stu-id="90865-155">For example, it's not Microsoft's place to tell people how to use Android developer tools--that is Google's story to tell.</span></span> <span data-ttu-id="90865-156">如有需要，我们可以介绍如何将 Android 开发人员工具与 Azure 结合使用，但对于如何使用该工具，应向 Google 寻求帮助。</span><span class="sxs-lookup"><span data-stu-id="90865-156">If we need to, we can explain how to use Android developer tools *with* Azure, but Google should tell the story of how to use their tools.</span></span>
- <span data-ttu-id="90865-157">**PM 签名**：请求 Microsoft 在第三方内容上签名。</span><span class="sxs-lookup"><span data-stu-id="90865-157">**PM signoff**: Request that Microsoft sign off on third-party content.</span></span> <span data-ttu-id="90865-158">链接到此内容即表明我们信任此内容，并且有责任和义务让用户按说明操作。</span><span class="sxs-lookup"><span data-stu-id="90865-158">By linking to it, we are saying something about our trust in it and our obligation if people follow the instructions.</span></span>
- <span data-ttu-id="90865-159">**适时检查更新**：确保第三方信息保持持续适用性、正确性和相关性，并确保链接未经任何更改。</span><span class="sxs-lookup"><span data-stu-id="90865-159">**Freshness reviews**: Make sure that the third-party info is still current, correct, and relevant, and that the link hasn’t changed.</span></span>
- <span data-ttu-id="90865-160">**跳转提醒**：确保用户知道他们即将转到另一个网站。</span><span class="sxs-lookup"><span data-stu-id="90865-160">**Offsite**: Make users aware that they are going to another site.</span></span> <span data-ttu-id="90865-161">如果上下文未明确指出这一点，请添加一个限定性句子。</span><span class="sxs-lookup"><span data-stu-id="90865-161">If the context does not make that clear, add a qualifying phrase.</span></span> <span data-ttu-id="90865-162">例如，“先决条件包括 Android 开发人员工具，你可以在 Android Studio 网站上进行下载”。</span><span class="sxs-lookup"><span data-stu-id="90865-162">For example: “Prerequisites include the Android Developer Tools, which you can download on the Android Studio site.”</span></span>
- <span data-ttu-id="90865-163">**后续步骤**：在“后续步骤”部分，最好添加一个指向类似于 MVP 博客等内容的链接。</span><span class="sxs-lookup"><span data-stu-id="90865-163">**Next steps**: It’s fine to add a link to, say, an MVP blog in a "Next steps" section.</span></span> <span data-ttu-id="90865-164">再次提醒，请务必使用户了解他们会离开当前网站。</span><span class="sxs-lookup"><span data-stu-id="90865-164">Again, just make sure that users understand they’ll be leaving the site.</span></span>
- <span data-ttu-id="90865-165">**合法性**：合法遵守每个 ms.com 页面页脚的使用条款中“链接到第三方网站”的规定。</span><span class="sxs-lookup"><span data-stu-id="90865-165">**Legal**: We are covered legally under **Links to Third Party Sites** in the **Terms of Use** footer on every ms.com page.</span></span>

## <a name="links-to-msdn-or-technet"></a><span data-ttu-id="90865-166">链接到 MSDN 或 TechNet</span><span class="sxs-lookup"><span data-stu-id="90865-166">Links to MSDN or TechNet</span></span>

<span data-ttu-id="90865-167">如果需要链接到 MSDN 或 TechNet，请使用主题的完整链接，并从链接中删除“en-us”语言区域设置。</span><span class="sxs-lookup"><span data-stu-id="90865-167">When you need to link to MSDN or TechNet, use the full link to the topic, and remove the "en-us" language locale from the link.</span></span>

## <a name="links-to-azure-powershell-reference-content"></a><span data-ttu-id="90865-168">链接到 Azure PowerShell 引用内容</span><span class="sxs-lookup"><span data-stu-id="90865-168">Links to Azure PowerShell reference content</span></span>

<span data-ttu-id="90865-169">自 2016 年 11 月以来，Azure PowerShell 引用内容已经经历了若干次变更。</span><span class="sxs-lookup"><span data-stu-id="90865-169">The Azure PowerShell reference content has been through several changes since November 2016.</span></span> <span data-ttu-id="90865-170">使用以下准则从 docs.microsoft.com 的其他文章链接到此内容。</span><span class="sxs-lookup"><span data-stu-id="90865-170">Use the following guidelines for linking to this content from other articles on docs.microsoft.com.</span></span>

<span data-ttu-id="90865-171">URL 结构：</span><span class="sxs-lookup"><span data-stu-id="90865-171">Structure of the URL:</span></span>

* <span data-ttu-id="90865-172">对于 cmdlet：</span><span class="sxs-lookup"><span data-stu-id="90865-172">For cmdlets:</span></span>
  - `/powershell/module/<module-name>/<cmdlet-name>[?view=<moniker-name>]`
* <span data-ttu-id="90865-173">对于概念主题：</span><span class="sxs-lookup"><span data-stu-id="90865-173">For conceptual topics:</span></span>
  - `/powershell/azure/<topic-file-name>[?view=<moniker-name>]`
  - `/powershell/azure/<service-name>/<topic-file-name>[?view=<moniker-name>]`

<span data-ttu-id="90865-174">&lt;moniker-name&gt; 部分是可选的。</span><span class="sxs-lookup"><span data-stu-id="90865-174">The &lt;moniker-name&gt; portion is optional.</span></span> <span data-ttu-id="90865-175">如果省略这一部分，会将用户定向到最新版本的内容。</span><span class="sxs-lookup"><span data-stu-id="90865-175">If it's omitted, you will be directed to the latest version of the content.</span></span> <span data-ttu-id="90865-176">&lt;service-name&gt; 部分是以下基 URL 中显示的其中一个示例：</span><span class="sxs-lookup"><span data-stu-id="90865-176">The &lt;service-name&gt; portion is one of the examples shown in the following base URLs:</span></span>

- <span data-ttu-id="90865-177">Azure PowerShell (AzureRM) 内容：https://docs.microsoft.com/powershell/azure/</span><span class="sxs-lookup"><span data-stu-id="90865-177">Azure PowerShell (AzureRM) content: https://docs.microsoft.com/powershell/azure/</span></span>
- <span data-ttu-id="90865-178">Azure PowerShell (ASM) 内容：https://docs.microsoft.com/powershell/azure/_servicemanagement_</span><span class="sxs-lookup"><span data-stu-id="90865-178">Azure PowerShell (ASM) content: https://docs.microsoft.com/powershell/azure/_servicemanagement_</span></span>
- <span data-ttu-id="90865-179">Azure Active Directory (AzureAD) PowerShell 内容：https://docs.microsoft.com/powershell/azure/_active-directory_</span><span class="sxs-lookup"><span data-stu-id="90865-179">Azure Active Directory (AzureAD) PowerShell content: https://docs.microsoft.com/powershell/azure/_active-directory_</span></span>
- <span data-ttu-id="90865-180">Azure Service Fabric PowerShell：https://docs.microsoft.com/powershell/azure/_service-fabric_</span><span class="sxs-lookup"><span data-stu-id="90865-180">Azure Service Fabric PowerShell: https://docs.microsoft.com/powershell/azure/_service-fabric_</span></span>
- <span data-ttu-id="90865-181">Azure 信息保护 PowerShell：https://docs.microsoft.com/powershell/azure/_aip_</span><span class="sxs-lookup"><span data-stu-id="90865-181">Azure Information Protection PowerShell: https://docs.microsoft.com/powershell/azure/_aip_</span></span>
- <span data-ttu-id="90865-182">Azure 弹性数据库作业 PowerShell：https://docs.microsoft.com/powershell/azure/_elasticdbjobs_</span><span class="sxs-lookup"><span data-stu-id="90865-182">Azure Elastic DB Jobs PowerShell: https://docs.microsoft.com/powershell/azure/_elasticdbjobs_</span></span>

<span data-ttu-id="90865-183">在使用这些 URL 时，会将用户重定向到最新版本的内容。</span><span class="sxs-lookup"><span data-stu-id="90865-183">When you use these URLs, you will be redirected to the latest version of the content.</span></span> <span data-ttu-id="90865-184">这样就不必指定版本名字对象。</span><span class="sxs-lookup"><span data-stu-id="90865-184">This way, you don't have to specify a version moniker.</span></span> <span data-ttu-id="90865-185">并且不会有指向版本更改时必须进行更新的概念内容的链接。</span><span class="sxs-lookup"><span data-stu-id="90865-185">And you won't have links to conceptual content that must be updated when the version changes.</span></span>

<span data-ttu-id="90865-186">若要创建正确的链接，可以在浏览器中找到要链接的页面并复制 URL。</span><span class="sxs-lookup"><span data-stu-id="90865-186">To create the correct link, find the page that you want to link to in your browser, and copy the URL.</span></span>
<span data-ttu-id="90865-187">然后，删除“https://docs.microsoft.com”和区域设置信息。</span><span class="sxs-lookup"><span data-stu-id="90865-187">Then, remove "https://docs.microsoft.com" and the locale info.</span></span>

<span data-ttu-id="90865-188">从 TOC 进行链接时，必须使用完整的 URL（不包含区域设置信息）。</span><span class="sxs-lookup"><span data-stu-id="90865-188">When you're linking from a TOC, you must use the full URL without the locale information.</span></span>

<span data-ttu-id="90865-189">示例 Markdown：</span><span class="sxs-lookup"><span data-stu-id="90865-189">Example markdown:</span></span>

```markdown
[Get-AzureRmResourceGroup](/powershell/module/azurerm.resources/get-azurermresourcegroup)
[Get-AzureRmResourceGroup](/powershell/module/azurerm.resources/get-azurermresourcegroup?view=azurermps-4.1.0)
[New-AzureVM](/powershell/module/azure/new-azurevm?view=azuresmps-4.0.0)
[New-AzureRmVM](/powershell/module/azurerm.compute/new-azurermvm)
[Install Azure PowerShell for Service Management](/powershell/azure/servicemanagement/install-azurerm-ps)
[Install Azure PowerShell](/powershell/azure/install-azurerm-ps)
```
