---
title: docs.microsoft.com 的 Markdown 引用
description: 了解 Microsoft Docs 平台中使用的 Markdown 功能和语法。
author: meganbradley
ms.author: mbradley
ms.date: 05/18/2018
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
ms.openlocfilehash: a5ff6c5122a08d2b611fd6b0344a6f5740d93928
ms.sourcegitcommit: 254c804bb0b451c262745fe8d87e2e8f9196440c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/05/2019
ms.locfileid: "73592571"
---
# <a name="markdown-reference"></a><span data-ttu-id="9f84c-103">Markdown 引用</span><span class="sxs-lookup"><span data-stu-id="9f84c-103">Markdown Reference</span></span>

<span data-ttu-id="9f84c-104">Markdown 是一种轻型标记语言，采用纯文本格式语法。</span><span class="sxs-lookup"><span data-stu-id="9f84c-104">Markdown is a lightweight markup language with plain text formatting syntax.</span></span> <span data-ttu-id="9f84c-105">Docs 平台支持 Markdown 的 CommonMark 标准，以及一些旨在为 docs.microsoft.com 提供更丰富内容的自定义 Markdown 扩展。</span><span class="sxs-lookup"><span data-stu-id="9f84c-105">The Docs platform supports the CommonMark standard for Markdown, plus some custom Markdown extensions designed to provide richer content on docs.microsoft.com.</span></span> <span data-ttu-id="9f84c-106">本文针对 docs.microsoft.com 的 Markdown 使用，介绍其字母顺序引用。</span><span class="sxs-lookup"><span data-stu-id="9f84c-106">This article provides an alphabetical reference for using Markdown for docs.microsoft.com.</span></span>

<span data-ttu-id="9f84c-107">可以使用任何文本编辑器创作 Markdown。</span><span class="sxs-lookup"><span data-stu-id="9f84c-107">You can use any text editor to author Markdown.</span></span> <span data-ttu-id="9f84c-108">对于可同时插入标准 Markdown 语法和自定义 Docs 扩展的编辑器，建议使用已安装 [Docs 创作包](https://aka.ms/DocsAuthoringPack)的 [VS Code](https://code.visualstudio.com/)。</span><span class="sxs-lookup"><span data-stu-id="9f84c-108">For an editor that facilitates inserting both standard Markdown syntax and custom Docs extensions, we recommend [VS Code](https://code.visualstudio.com/) with the [Docs Authoring Pack](https://aka.ms/DocsAuthoringPack) installed.</span></span>

<span data-ttu-id="9f84c-109">Docs 使用 Markdig Markdown 引擎。</span><span class="sxs-lookup"><span data-stu-id="9f84c-109">Docs uses the Markdig Markdown engine.</span></span> <span data-ttu-id="9f84c-110">可在 [https://babelmark.github.io/](https://babelmark.github.io/) 测试 Markdig 与其他引擎中的 Markdown 渲染效果。</span><span class="sxs-lookup"><span data-stu-id="9f84c-110">You can test the rendering of Markdown in Markdig vs. other engines at [https://babelmark.github.io/](https://babelmark.github.io/).</span></span>

## <a name="alerts-note-tip-important-caution-warning"></a><span data-ttu-id="9f84c-111">警报（备注、提示、重要提示、提醒、警告）</span><span class="sxs-lookup"><span data-stu-id="9f84c-111">Alerts (Note, Tip, Important, Caution, Warning)</span></span>

<span data-ttu-id="9f84c-112">警报是用于创建块引用 Docs Markdown 扩展，这些块引用与指示内容重要性的颜色和图标共同呈现在 docs.microsoft.com 上。</span><span class="sxs-lookup"><span data-stu-id="9f84c-112">Alerts are a Docs Markdown extension to create block quotes that render on docs.microsoft.com with colors and icons that indicate the significance of the content.</span></span> <span data-ttu-id="9f84c-113">支持以下警报类型：</span><span class="sxs-lookup"><span data-stu-id="9f84c-113">The following alert types are supported:</span></span>

```md
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

<span data-ttu-id="9f84c-114">这些警报在 docs.microsoft.com 上如下所示：</span><span class="sxs-lookup"><span data-stu-id="9f84c-114">These alerts look like this on docs.microsoft.com:</span></span>

![展示上一示例中的警报在使用不同图标和颜色的 Docs 页面发布版中的显示情况](media/alerts-rendering.png)

## <a name="code-snippets"></a><span data-ttu-id="9f84c-116">代码片段</span><span class="sxs-lookup"><span data-stu-id="9f84c-116">Code snippets</span></span>

<span data-ttu-id="9f84c-117">可在 Markdown 文件中嵌入代码片段：</span><span class="sxs-lookup"><span data-stu-id="9f84c-117">You can embed code snippets in your Markdown files:</span></span>

```md
[!code-<language>[<name>](<codepath><queryoption><queryoptionvalue> "<title>")]
```

## <a name="headings"></a><span data-ttu-id="9f84c-118">标题</span><span class="sxs-lookup"><span data-stu-id="9f84c-118">Headings</span></span>

<span data-ttu-id="9f84c-119">Docs 支持六个级别的 Markdown 标题：</span><span class="sxs-lookup"><span data-stu-id="9f84c-119">Docs supports six levels of Markdown headings:</span></span>

```md
# This is a first level heading (H1)

## This is a second level heading (H2)

...

###### This is a sixth level heading (H6)
```

- <span data-ttu-id="9f84c-120">最后一个 `#` 和标题文本之间必须有空格。</span><span class="sxs-lookup"><span data-stu-id="9f84c-120">There must be a space between the last `#` and heading text.</span></span>
- <span data-ttu-id="9f84c-121">每个 Markdown 文件必须有，且仅有一个 H1。</span><span class="sxs-lookup"><span data-stu-id="9f84c-121">Each Markdown file must have one and only one H1.</span></span>
- <span data-ttu-id="9f84c-122">H1 必须是 YML 元数据块之后的文件中的第一个内容。</span><span class="sxs-lookup"><span data-stu-id="9f84c-122">The H1 must be the first content in the file after the YML metadata block.</span></span>
- <span data-ttu-id="9f84c-123">H2 将自动显示在已发布文件右侧的导航菜单中。</span><span class="sxs-lookup"><span data-stu-id="9f84c-123">H2s automatically appear in the right-hand navigating menu of the published file.</span></span> <span data-ttu-id="9f84c-124">而后的低级标题则不会显示，因此策略性地使用 H2 可帮助读者进行内容导航。</span><span class="sxs-lookup"><span data-stu-id="9f84c-124">Lower-level headings do not, so use H2s strategically to help readers navigate your content.</span></span>
- <span data-ttu-id="9f84c-125">不建议使用 HTML 标题（如 `<h1>`），它们在某些情况下会导致出现生成警告。</span><span class="sxs-lookup"><span data-stu-id="9f84c-125">HMTL headings, such as `<h1>`, are not recommended and in some cases will cause build warnings.</span></span>
- <span data-ttu-id="9f84c-126">可通过[书签](#bookmark-links)链接到文件中的各个标题。</span><span class="sxs-lookup"><span data-stu-id="9f84c-126">You can link to individual headings in a file via [bookmarks](#bookmark-links).</span></span>

## <a name="html"></a><span data-ttu-id="9f84c-127">HTML</span><span class="sxs-lookup"><span data-stu-id="9f84c-127">HTML</span></span>

<span data-ttu-id="9f84c-128">虽然 Markdown 支持内联式 HTML，但不建议使用 HTML 将内容发布到 Docs，除了数量有限的一系列值以外，其他值会导致生成错误或警告。</span><span class="sxs-lookup"><span data-stu-id="9f84c-128">Although Markdown supports inline HTML, HTML is not recommended for publishing to Docs, and except for a limited list of values will cause build errors or warnings.</span></span>

## <a name="images"></a><span data-ttu-id="9f84c-129">图像</span><span class="sxs-lookup"><span data-stu-id="9f84c-129">Images</span></span>

<span data-ttu-id="9f84c-130">用于包含图像的语法是：</span><span class="sxs-lookup"><span data-stu-id="9f84c-130">The syntax to include an image is:</span></span>

```md
![[alt text]](<folderPath>)

Example:
![alt text for image](../images/Introduction.png)
```

<span data-ttu-id="9f84c-131">其中 `alt text` 是图像的简短说明，`<folder path>` 是图像的相对路径。</span><span class="sxs-lookup"><span data-stu-id="9f84c-131">Where `alt text` is a brief description of the image and `<folder path>` is a relative path to the image.</span></span> <span data-ttu-id="9f84c-132">视觉障碍用户的屏幕阅读器需采用替换文字。</span><span class="sxs-lookup"><span data-stu-id="9f84c-132">Alternate text is required for screen readers for the visually impaired.</span></span> <span data-ttu-id="9f84c-133">如果出现图像无法呈现的站点 bug，替换文字也非常有用。</span><span class="sxs-lookup"><span data-stu-id="9f84c-133">It is also useful if there is a site bug where the image cannot render.</span></span>

<span data-ttu-id="9f84c-134">图像应存储于文档集内的 `/media` 文件夹中。</span><span class="sxs-lookup"><span data-stu-id="9f84c-134">Images should be stored in a `/media` folder within your doc set.</span></span> <span data-ttu-id="9f84c-135">默认支持以下文件类型的图像：</span><span class="sxs-lookup"><span data-stu-id="9f84c-135">The following file types are supported by default for images:</span></span>

- <span data-ttu-id="9f84c-136">.jpg</span><span class="sxs-lookup"><span data-stu-id="9f84c-136">.jpg</span></span>
- <span data-ttu-id="9f84c-137">.png</span><span class="sxs-lookup"><span data-stu-id="9f84c-137">.png</span></span>

<span data-ttu-id="9f84c-138">可通过将其他图像类型作为资源添加到文档集的 docfx.json文件中，</span><span class="sxs-lookup"><span data-stu-id="9f84c-138">You can add support for other image types by adding them as resources to the docfx.json file</span></span><!--add link to reference when available--> <span data-ttu-id="9f84c-139">添加对它们的支持。</span><span class="sxs-lookup"><span data-stu-id="9f84c-139">for your doc set.</span></span>

## <a name="links"></a><span data-ttu-id="9f84c-140">链接</span><span class="sxs-lookup"><span data-stu-id="9f84c-140">Links</span></span>

<span data-ttu-id="9f84c-141">大多数情况下，Docs 使用指向其他文件和页面的标准 Markdown 链接。</span><span class="sxs-lookup"><span data-stu-id="9f84c-141">In most cases, Docs uses standard Markdown links to other files and pages.</span></span> <span data-ttu-id="9f84c-142">以下各小节将介绍各链接类型。</span><span class="sxs-lookup"><span data-stu-id="9f84c-142">The types of links are described in subsections below.</span></span>

> [!TIP]
> <span data-ttu-id="9f84c-143">适用于 VS Code 的 Docs 创作包有助于正确插入相关链接和书签，免去了寻找路径的麻烦！</span><span class="sxs-lookup"><span data-stu-id="9f84c-143">The Docs Authoring Pack for VS Code can help insert relative links and bookmarks correctly without the tedium of figuring out the paths!</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9f84c-144">请勿在 Microsoft 站点链接中添加区域设置代码（如 zh-cn）。</span><span class="sxs-lookup"><span data-stu-id="9f84c-144">Do not include locale codes, such as en-us, in your links to Microsoft sites.</span></span> <span data-ttu-id="9f84c-145">硬编码的区域设置代码会导致本地化内容无法呈现，这对采用其他区域设置的用户而言是糟糕的客户体验，并将产生高昂的本地化成本。</span><span class="sxs-lookup"><span data-stu-id="9f84c-145">Hard-coded locale codes prevent localized content from rendering, which is a bad customer experience for users in other locales and incurs significant localization costs.</span></span> <span data-ttu-id="9f84c-146">复制浏览器中的 URL 时，默认包括区域设置代码，因此在创建链接时，需手动将其删除。</span><span class="sxs-lookup"><span data-stu-id="9f84c-146">When you copy a URL from a browser, the locale code is included by default, so you need to manually delete it when you create your link.</span></span> <span data-ttu-id="9f84c-147">例如，使用：</span><span class="sxs-lookup"><span data-stu-id="9f84c-147">For example, use:</span></span>
>
> `[Microsoft](https://www.microsoft.com)`
>
> <span data-ttu-id="9f84c-148">而不是：</span><span class="sxs-lookup"><span data-stu-id="9f84c-148">Not:</span></span>
>
> `[Microsoft](https://www.microsoft.com/en-us/)`

### <a name="relative-links-to-files-in-the-same-doc-set"></a><span data-ttu-id="9f84c-149">同一文档集中的文件的相对链接</span><span class="sxs-lookup"><span data-stu-id="9f84c-149">Relative links to files in the same doc set</span></span>

<span data-ttu-id="9f84c-150">相对路径是指相对于当前文件的目标文件路径。</span><span class="sxs-lookup"><span data-stu-id="9f84c-150">A relative path is the path to the target file relative to the current file.</span></span> <span data-ttu-id="9f84c-151">在 Docs 中，可使用相对路径链接到同一文档集中的其他文件。</span><span class="sxs-lookup"><span data-stu-id="9f84c-151">In Docs, you can use a relative path to link to another file within the same doc set.</span></span> <span data-ttu-id="9f84c-152">相对路径的语法如下：</span><span class="sxs-lookup"><span data-stu-id="9f84c-152">The syntax for a relative path is as follows:</span></span>

```md
[link text](../../folder/filename.md)
```

<span data-ttu-id="9f84c-153">其中，`../` 指示层次结构中的上一层级。</span><span class="sxs-lookup"><span data-stu-id="9f84c-153">Where `../` indicates one level above in the hierarchy.</span></span>

- <span data-ttu-id="9f84c-154">相对路径将在生成过程中解析，包括删除 .md 扩展名。</span><span class="sxs-lookup"><span data-stu-id="9f84c-154">The relative path will be resolved during the build, including removal of the .md extension.</span></span>
- <span data-ttu-id="9f84c-155">可使用“../”链接到父文件夹中的文件，但该文件必须位于同一文档集。</span><span class="sxs-lookup"><span data-stu-id="9f84c-155">You can use "../" to link to a file in the parent folder, but that file has to be in the same doc set.</span></span> <span data-ttu-id="9f84c-156">不能使用“../”链接到其他文档集文件夹中的文件。</span><span class="sxs-lookup"><span data-stu-id="9f84c-156">You cannot use "../" to link to a file in another doc set folder.</span></span>
- <span data-ttu-id="9f84c-157">Docs 还支持以“~”开头的特殊形式的相对路径（例如，~/foo/bar.md）。</span><span class="sxs-lookup"><span data-stu-id="9f84c-157">Docs also supports a special form of relative path that starts with "~" (for example, ~/foo/bar.md).</span></span> <span data-ttu-id="9f84c-158">此语法表示相对于文档集根文件夹的文件。</span><span class="sxs-lookup"><span data-stu-id="9f84c-158">This syntax indicates a file relative to the root folder of a doc set.</span></span> <span data-ttu-id="9f84c-159">此类路径也将在生成过程中进行验证和解析。</span><span class="sxs-lookup"><span data-stu-id="9f84c-159">This kind of path is also validated and resolved during the build.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9f84c-160">包括相对路径中的文件扩展名。</span><span class="sxs-lookup"><span data-stu-id="9f84c-160">Include the file extension in the relative path.</span></span> <span data-ttu-id="9f84c-161">生成可验证该相对路径的目标文件是否存在。</span><span class="sxs-lookup"><span data-stu-id="9f84c-161">Build validates the existence of the target file of that relative path.</span></span> <span data-ttu-id="9f84c-162">如果相对路径不包括文件扩展名，生成很可能会报告断开的链接警告。</span><span class="sxs-lookup"><span data-stu-id="9f84c-162">If relative path does not include file extension, it is likely build will report a warning of broken link.</span></span> <span data-ttu-id="9f84c-163">例如，使用：</span><span class="sxs-lookup"><span data-stu-id="9f84c-163">For example, use:</span></span>
>
> `[link text](../../folder/filename.md)`
>
> <span data-ttu-id="9f84c-164">而不是：</span><span class="sxs-lookup"><span data-stu-id="9f84c-164">Not:</span></span>
>
> `[link text](../../folder/filename)`

### <a name="site-relative-links-to-other-files-on-docs"></a><span data-ttu-id="9f84c-165">站点相对链接到 Docs 上的其他文件</span><span class="sxs-lookup"><span data-stu-id="9f84c-165">Site relative links to other files on Docs</span></span>

```md
[Azure and Linux](/articles/virtual-machines/linux/overview)
```

<span data-ttu-id="9f84c-166">请勿包括文件扩展名 (.md)。</span><span class="sxs-lookup"><span data-stu-id="9f84c-166">Do not include the file extension (.md).</span></span> <span data-ttu-id="9f84c-167">这将链接到 Azure“文章”文档集外的 Linux 概述文件。</span><span class="sxs-lookup"><span data-stu-id="9f84c-167">This links to the Linux overview file from outside the Azure "articles" doc set.</span></span>

### <a name="links-to-external-sites"></a><span data-ttu-id="9f84c-168">外部站点链接</span><span class="sxs-lookup"><span data-stu-id="9f84c-168">Links to external sites</span></span>

```md
[Microsoft](https://www.microsoft.com)
```

<span data-ttu-id="9f84c-169">其他网页基于 URL 的链接（必须包括 https://）。</span><span class="sxs-lookup"><span data-stu-id="9f84c-169">URL-based link to another web page (must include https://).</span></span>

### <a name="bookmark-links"></a><span data-ttu-id="9f84c-170">书签链接</span><span class="sxs-lookup"><span data-stu-id="9f84c-170">Bookmark links</span></span>

<span data-ttu-id="9f84c-171">同一存储库中其他文件标题的书签链接。</span><span class="sxs-lookup"><span data-stu-id="9f84c-171">Bookmark link to a heading in another file in the same repo.</span></span> <span data-ttu-id="9f84c-172">例如：</span><span class="sxs-lookup"><span data-stu-id="9f84c-172">For example:</span></span>

```md
[Managed Disks](../../linux/overview.md#managed-disks)
```

<span data-ttu-id="9f84c-173">当前文件标题的书签链接：</span><span class="sxs-lookup"><span data-stu-id="9f84c-173">Bookmark link to a heading in the current file:</span></span>

```md
[Managed Disks](#managed-disks)
```

<span data-ttu-id="9f84c-174">使用哈希标记 `#`，后跟标头的字词。</span><span class="sxs-lookup"><span data-stu-id="9f84c-174">Use a hash mark `#` followed by the words of the heading.</span></span> <span data-ttu-id="9f84c-175">要将标题文本更改为链接文本，请执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="9f84c-175">To change the heading text into link text:</span></span>
- <span data-ttu-id="9f84c-176">使用所有小写字符</span><span class="sxs-lookup"><span data-stu-id="9f84c-176">Use all lowercase characters</span></span>
- <span data-ttu-id="9f84c-177">删除标点</span><span class="sxs-lookup"><span data-stu-id="9f84c-177">Remove punctuation</span></span>
- <span data-ttu-id="9f84c-178">将空格替换为短划线</span><span class="sxs-lookup"><span data-stu-id="9f84c-178">Replace spaces with dashes</span></span>

<span data-ttu-id="9f84c-179">例如，如果标题名称为“2.2 安全问题”，则书签链接文本是“#22-安全-问题”。</span><span class="sxs-lookup"><span data-stu-id="9f84c-179">For example, if the heading name is "2.2 Security concerns", then the bookmark link text will be "#22-security-concerns".</span></span>

### <a name="explicit-anchor-links"></a><span data-ttu-id="9f84c-180">显式定位标记链接</span><span class="sxs-lookup"><span data-stu-id="9f84c-180">Explicit anchor links</span></span>

<span data-ttu-id="9f84c-181">使用 `<a>` HTML 标记的显式定位标记链接并非必需，也不推荐使用，但在中心和登录页面中除外。</span><span class="sxs-lookup"><span data-stu-id="9f84c-181">Explicit anchor links using the `<a>` HTML tag are **not required or recommended** except in hub and landing pages.</span></span> <span data-ttu-id="9f84c-182">在常规 Markdown 文件中使用上述书签。</span><span class="sxs-lookup"><span data-stu-id="9f84c-182">Use bookmarks as described above in general Markdown files.</span></span> <span data-ttu-id="9f84c-183">对于中心和登录页面，使用如下所示的定位标记：</span><span class="sxs-lookup"><span data-stu-id="9f84c-183">For hub and landing pages, use anchors as follows:</span></span>

<span data-ttu-id="9f84c-184">`## <a id="AnchorText"> </a>Header text` 或 `## <a name="AnchorText"> </a>Header text`</span><span class="sxs-lookup"><span data-stu-id="9f84c-184">`## <a id="AnchorText"> </a>Header text` or `## <a name="AnchorText"> </a>Header text`</span></span>

<span data-ttu-id="9f84c-185">若要链接到显式定位标记，请使用以下语法：</span><span class="sxs-lookup"><span data-stu-id="9f84c-185">To link to explicit anchors, use the following syntax:</span></span>

```md
To go to a section on the same page:
[text](#AnchorText)

To go to a section on another page.
[text](FileName.md#AnchorText)
```

### <a name="xref-cross-reference-links"></a><span data-ttu-id="9f84c-186">XREF（交叉引用）链接</span><span class="sxs-lookup"><span data-stu-id="9f84c-186">XREF (cross reference) links</span></span>

<span data-ttu-id="9f84c-187">若要链接到当前文档集或其他文档集中自动生成的 API 参考页，请使用具有唯一 ID (UID) 的 XREF 链接。</span><span class="sxs-lookup"><span data-stu-id="9f84c-187">To link to auto-generated API references pages in the current doc set or other doc sets, use XREF links with the unique ID (UID).</span></span>

> [!NOTE]
> <span data-ttu-id="9f84c-188">若要引用其他文档集中的 API 参考页，需要在 `docfx.json` 文件中添加 `xrefService` 配置。</span><span class="sxs-lookup"><span data-stu-id="9f84c-188">To reference API reference pages in other doc sets, you need to add `xrefService` configuration in `docfx.json` file.</span></span>
> ```
> "build": {
>   ...
>   "xrefService": [ "https://xref.docs.microsoft.com/query?uid={uid}" ]
> }
> ```

<span data-ttu-id="9f84c-189">UID 等同于完全限定的类名称和成员名称。</span><span class="sxs-lookup"><span data-stu-id="9f84c-189">The UID equates to the fully qualified class and member name.</span></span> <span data-ttu-id="9f84c-190">如果在 UID 后面添加 \*，该链接则表示重载页面，而不是特定 API。</span><span class="sxs-lookup"><span data-stu-id="9f84c-190">If you add a \* after the UID, the link then represents the overload page and not a specific API.</span></span> <span data-ttu-id="9f84c-191">例如，使用 `List<T>.BinarySearch*` 链接到 BinarySearch 方法页，而不是链接到特定重载（如 `List<T>.BinarySearch(T, IComparer<T>)`）。</span><span class="sxs-lookup"><span data-stu-id="9f84c-191">For example, use `List<T>.BinarySearch*` to link to the BinarySearch Method page instead of linking to a specific overload such as `List<T>.BinarySearch(T, IComparer<T>)`.</span></span>

<span data-ttu-id="9f84c-192">可使用下列某一语法：</span><span class="sxs-lookup"><span data-stu-id="9f84c-192">You can use one of the following syntaxes:</span></span>

- <span data-ttu-id="9f84c-193">自动链接：`<xref:UID> or <xref:UID?displayProperty=nameWithType>`</span><span class="sxs-lookup"><span data-stu-id="9f84c-193">Auto-link: `<xref:UID> or <xref:UID?displayProperty=nameWithType>`</span></span>

  <span data-ttu-id="9f84c-194">可选的 `displayProperty` 查询参数生成完全限定的链接文本。</span><span class="sxs-lookup"><span data-stu-id="9f84c-194">The optional `displayProperty` query parameter produces a fully qualified link text.</span></span> <span data-ttu-id="9f84c-195">默认情况下，链接文本仅显示成员名称或类型名称。</span><span class="sxs-lookup"><span data-stu-id="9f84c-195">By default, link text shows only the member or type name.</span></span>

- <span data-ttu-id="9f84c-196">Markdown 链接：`[link text](xref:UID)`</span><span class="sxs-lookup"><span data-stu-id="9f84c-196">Markdown link: `[link text](xref:UID)`</span></span>
  
  <span data-ttu-id="9f84c-197">用于自定义显示的链接文本。</span><span class="sxs-lookup"><span data-stu-id="9f84c-197">Use when you want to customize the link text displayed.</span></span>

<span data-ttu-id="9f84c-198">示例：</span><span class="sxs-lookup"><span data-stu-id="9f84c-198">Examples:</span></span>

- <span data-ttu-id="9f84c-199">`<xref:System.String>` 呈现为“String”。</span><span class="sxs-lookup"><span data-stu-id="9f84c-199">`<xref:System.String>` renders as "String".</span></span>
- <span data-ttu-id="9f84c-200">`<xref:System.String?displayProperty=nameWithType>` 呈现为“System.String”。</span><span class="sxs-lookup"><span data-stu-id="9f84c-200">`<xref:System.String?displayProperty=nameWithType>` renders as "System.String".</span></span>
- <span data-ttu-id="9f84c-201">`[String class](xref:System.String)` 呈现为“String 类”。</span><span class="sxs-lookup"><span data-stu-id="9f84c-201">`[String class](xref:System.String)` renders as "String class".</span></span>

<span data-ttu-id="9f84c-202">暂无法轻松查找 UID。</span><span class="sxs-lookup"><span data-stu-id="9f84c-202">Right now, there is no easy way to find the UIDs.</span></span> <!-- ? --><span data-ttu-id="9f84c-203">查找 API UID 的最佳方法是，查看要链接到的 API 页面的源，并查找 ms.assetid 值。</span><span class="sxs-lookup"><span data-stu-id="9f84c-203">The best way to find the UID for an API is to view the source for the API page you want to link to and find the ms.assetid value.</span></span> <span data-ttu-id="9f84c-204">源中不显示各个重载值。</span><span class="sxs-lookup"><span data-stu-id="9f84c-204">Individual overload values are not shown in the source.</span></span> <span data-ttu-id="9f84c-205">今后，我们将努力开发更优质的系统。</span><span class="sxs-lookup"><span data-stu-id="9f84c-205">We're working on having a better system in the future.</span></span>

<span data-ttu-id="9f84c-206">如果 UID 包含特殊字符 \`、\# 或 \*，必须对 UID 值执行 HTML 编码，分别编码为 `%60`、`%23` 和 `%2A`。</span><span class="sxs-lookup"><span data-stu-id="9f84c-206">When the UID contains the special characters \`, \#, or \*, the UID value needs to be HTML encoded as `%60`, `%23`, and `%2A`, respectively.</span></span> <span data-ttu-id="9f84c-207">虽然有时会发现括号也被编码，但对此并不作要求。</span><span class="sxs-lookup"><span data-stu-id="9f84c-207">You'll sometimes see parentheses encoded but it's not a requirement.</span></span>

<span data-ttu-id="9f84c-208">示例：</span><span class="sxs-lookup"><span data-stu-id="9f84c-208">Examples:</span></span>

- <span data-ttu-id="9f84c-209">System.Threading.Tasks.Task\`1 变为 `System.Threading.Tasks.Task%601`</span><span class="sxs-lookup"><span data-stu-id="9f84c-209">System.Threading.Tasks.Task\`1 becomes `System.Threading.Tasks.Task%601`</span></span>
- <span data-ttu-id="9f84c-210">System.Exception.\#ctor 变为 `System.Exception.%23ctor`</span><span class="sxs-lookup"><span data-stu-id="9f84c-210">System.Exception.\#ctor becomes `System.Exception.%23ctor`</span></span>
- <span data-ttu-id="9f84c-211">System.Lazy\`1.\#ctor(System.Threading.LazyThreadSafetyMode) 变为 `System.Lazy%601.%23ctor%28System.Threading.LazyThreadSafetyMode%29`</span><span class="sxs-lookup"><span data-stu-id="9f84c-211">System.Lazy\`1.\#ctor(System.Threading.LazyThreadSafetyMode) becomes  `System.Lazy%601.%23ctor%28System.Threading.LazyThreadSafetyMode%29`</span></span>

<!-- leave out of Contributor Guide for now
Using XREF may require some configuration. For more information, see XREF Service.
-->

## <a name="lists-numbered-bulleted-checklist"></a><span data-ttu-id="9f84c-212">列表（带编号、显示项目符号、清单）</span><span class="sxs-lookup"><span data-stu-id="9f84c-212">Lists (Numbered, Bulleted, Checklist)</span></span>

### <a name="numbered-list"></a><span data-ttu-id="9f84c-213">编号列表</span><span class="sxs-lookup"><span data-stu-id="9f84c-213">Numbered list</span></span>

<span data-ttu-id="9f84c-214">若要创建编号列表，可全部使用 1，它们将在发布时呈现为有序列表。</span><span class="sxs-lookup"><span data-stu-id="9f84c-214">To create a numbered list, you can use all 1s, which are rendered as a sequential list when published.</span></span> <span data-ttu-id="9f84c-215">为提高源可读性，可增加列表。</span><span class="sxs-lookup"><span data-stu-id="9f84c-215">For increased source readability, you can increment your lists.</span></span>

<span data-ttu-id="9f84c-216">请勿在列表中使用字母，也勿使用嵌套列表。</span><span class="sxs-lookup"><span data-stu-id="9f84c-216">Do not use letters in lists, including nested lists.</span></span> <span data-ttu-id="9f84c-217">发布到 Docs 时，它们无法正确呈现。使用编号的嵌套列表在发布时将呈现为小写字母。</span><span class="sxs-lookup"><span data-stu-id="9f84c-217">They do not render correctly when published to Docs. Nested lists using numbers will render as lowercase letters when published.</span></span> <span data-ttu-id="9f84c-218">例如：</span><span class="sxs-lookup"><span data-stu-id="9f84c-218">For example:</span></span>

```md
1. This is
1. a parent numbered list
   1. and this is
   1. a nested numbered list
1. (fin)
```

<span data-ttu-id="9f84c-219">这将呈现为：</span><span class="sxs-lookup"><span data-stu-id="9f84c-219">This renders as follows:</span></span>

1. <span data-ttu-id="9f84c-220">This is</span><span class="sxs-lookup"><span data-stu-id="9f84c-220">This is</span></span>
1. <span data-ttu-id="9f84c-221">a parent numbered list</span><span class="sxs-lookup"><span data-stu-id="9f84c-221">a parent numbered list</span></span>
   1. <span data-ttu-id="9f84c-222">and this is</span><span class="sxs-lookup"><span data-stu-id="9f84c-222">and this is</span></span>
   1. <span data-ttu-id="9f84c-223">a nested numbered list</span><span class="sxs-lookup"><span data-stu-id="9f84c-223">a nested numbered list</span></span>
1. <span data-ttu-id="9f84c-224">(fin)</span><span class="sxs-lookup"><span data-stu-id="9f84c-224">(fin)</span></span>

### <a name="bulleted-list"></a><span data-ttu-id="9f84c-225">项目符号列表</span><span class="sxs-lookup"><span data-stu-id="9f84c-225">Bulleted list</span></span>

<span data-ttu-id="9f84c-226">若要创建项目符号列表，请使用 `-`，其后每行开头跟一个空格：</span><span class="sxs-lookup"><span data-stu-id="9f84c-226">To create a bulleted list, use `-` followed by a space at the beginning of each line:</span></span>

```md
- This is
- a parent bulleted list
  - and this is
  - a nested bulleted list
- All done!
```

<span data-ttu-id="9f84c-227">这将呈现为：</span><span class="sxs-lookup"><span data-stu-id="9f84c-227">This renders as follows:</span></span>

- <span data-ttu-id="9f84c-228">This is</span><span class="sxs-lookup"><span data-stu-id="9f84c-228">This is</span></span>
- <span data-ttu-id="9f84c-229">a parent bulleted list</span><span class="sxs-lookup"><span data-stu-id="9f84c-229">a parent bulleted list</span></span>
  - <span data-ttu-id="9f84c-230">and this is</span><span class="sxs-lookup"><span data-stu-id="9f84c-230">and this is</span></span>
  - <span data-ttu-id="9f84c-231">a nested bulleted list</span><span class="sxs-lookup"><span data-stu-id="9f84c-231">a nested bulleted list</span></span>
- <span data-ttu-id="9f84c-232">All done!</span><span class="sxs-lookup"><span data-stu-id="9f84c-232">All done!</span></span>

### <a name="checklist"></a><span data-ttu-id="9f84c-233">清单</span><span class="sxs-lookup"><span data-stu-id="9f84c-233">Checklist</span></span>

<span data-ttu-id="9f84c-234">清单仅可通过自定义 Markdown 扩展在 docs.microsoft.com 上使用：</span><span class="sxs-lookup"><span data-stu-id="9f84c-234">Checklists are available for use on docs.microsoft.com (only) via a custom Markdown extension:</span></span>

```md
> [!div class="checklist"]
> * List item 1
> * List item 2
> * List item 3
```

<span data-ttu-id="9f84c-235">此示例在 docs.microsoft.com 上呈现为：</span><span class="sxs-lookup"><span data-stu-id="9f84c-235">This example renders on docs.microsoft.com like this:</span></span>

> [!div class="checklist"]
> * <span data-ttu-id="9f84c-236">List item 1</span><span class="sxs-lookup"><span data-stu-id="9f84c-236">List item 1</span></span>
> * <span data-ttu-id="9f84c-237">List item 2</span><span class="sxs-lookup"><span data-stu-id="9f84c-237">List item 2</span></span>
> * <span data-ttu-id="9f84c-238">List item 3</span><span class="sxs-lookup"><span data-stu-id="9f84c-238">List item 3</span></span>

<span data-ttu-id="9f84c-239">在文章开头或结尾使用清单，总结“将要学习的内容”或“所学内容”。</span><span class="sxs-lookup"><span data-stu-id="9f84c-239">Use checklists at the beginning or end of an article to summarize "What will you learn" or "What have you learned" content.</span></span> <span data-ttu-id="9f84c-240">请勿在整篇文章中添加随机清单。</span><span class="sxs-lookup"><span data-stu-id="9f84c-240">Do not add random checklists throughout your articles.</span></span>
<!-- is this guidance still accurate? -->

## <a name="next-step-action"></a><span data-ttu-id="9f84c-241">下一步操作</span><span class="sxs-lookup"><span data-stu-id="9f84c-241">Next step action</span></span>

<span data-ttu-id="9f84c-242">可使用自定义扩展在 docs.microsoft.com（仅限用于此站点）页面上添加下一步操作按钮。</span><span class="sxs-lookup"><span data-stu-id="9f84c-242">You can use a custom extension to add a next step action button to pages on docs.microsoft.com (only).</span></span>

<span data-ttu-id="9f84c-243">语法如下所示：</span><span class="sxs-lookup"><span data-stu-id="9f84c-243">The syntax is as follows:</span></span>

```md
> [!div class="nextstepaction"]
> [button text](link to topic)
```

<span data-ttu-id="9f84c-244">例如：</span><span class="sxs-lookup"><span data-stu-id="9f84c-244">For example:</span></span>

```md
> [!div class="nextstepaction"]
> [Learn about basic style](style-quick-start.md)
```

<span data-ttu-id="9f84c-245">这将呈现为：</span><span class="sxs-lookup"><span data-stu-id="9f84c-245">This renders as follows:</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="9f84c-246">了解基本样式</span><span class="sxs-lookup"><span data-stu-id="9f84c-246">Learn about basic style</span></span>](style-quick-start.md)

<span data-ttu-id="9f84c-247">可在下一步操作中使用任何受支持的链接，包括指向其他网页的 Markdown 链接。</span><span class="sxs-lookup"><span data-stu-id="9f84c-247">You can use any supported link in a next step action, including a Markdown link to another web page.</span></span> <span data-ttu-id="9f84c-248">在大多数情况下，下一操作链接是同一文档集中另一个文件的相对链接。</span><span class="sxs-lookup"><span data-stu-id="9f84c-248">In most cases, the next action link will be a relative link to another file in the same doc set.</span></span>

## <a name="section-definition"></a><span data-ttu-id="9f84c-249">节定义</span><span class="sxs-lookup"><span data-stu-id="9f84c-249">Section definition</span></span>

<!-- more info about this would be helpful! -->
<span data-ttu-id="9f84c-250">可能需要定义节。</span><span class="sxs-lookup"><span data-stu-id="9f84c-250">You might need to define a section.</span></span> <span data-ttu-id="9f84c-251">这种语法最常用于代码表。</span><span class="sxs-lookup"><span data-stu-id="9f84c-251">This syntax is mostly used for code tables.</span></span>
<span data-ttu-id="9f84c-252">请参阅以下示例：</span><span class="sxs-lookup"><span data-stu-id="9f84c-252">See the following example:</span></span>

````
> [!div class="tabbedCodeSnippets" data-resources="OutlookServices.Calendar"]
> ```cs
> <cs code text>
> ```
> ```javascript
> <js code text>
> ```
````

<span data-ttu-id="9f84c-253">前面的块引用 Markdown 文本将呈现为：</span><span class="sxs-lookup"><span data-stu-id="9f84c-253">The preceding blockquote Markdown text will be rendered as:</span></span>
> [!div class="tabbedCodeSnippets" data-resources="OutlookServices.Calendar"]
> ```cs
> <cs code text>
> ```
> ```javascript
> <js code text>
> ```

## <a name="selectors"></a><span data-ttu-id="9f84c-254">选择器</span><span class="sxs-lookup"><span data-stu-id="9f84c-254">Selectors</span></span>

<!-- could be more clear! -->
<span data-ttu-id="9f84c-255">要连接同一文章的不同页面，可使用选择器。</span><span class="sxs-lookup"><span data-stu-id="9f84c-255">You can use a selector when you want to connect different pages for the same article.</span></span> <span data-ttu-id="9f84c-256">如此，读者即可在这些页面之间切换。</span><span class="sxs-lookup"><span data-stu-id="9f84c-256">Readers can then switch between those pages.</span></span>

> [!NOTE]
> <span data-ttu-id="9f84c-257">此扩展在 docs.microsoft.com 和 MSDN 中的作用不同。</span><span class="sxs-lookup"><span data-stu-id="9f84c-257">This extension works differently between docs.microsoft.com and MSDN.</span></span> <!-- should we keep info about MSDN? If so say how they differ?-->

### <a name="single-selector"></a><span data-ttu-id="9f84c-258">单一选择器</span><span class="sxs-lookup"><span data-stu-id="9f84c-258">Single selector</span></span>

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

<span data-ttu-id="9f84c-259">... 将呈现为：</span><span class="sxs-lookup"><span data-stu-id="9f84c-259">... will be rendered like this:</span></span>

> [!div class="op_single_selector"]
> - [Universal Windows](how-to-write-use-markdown.md)
> - [Windows Phone](how-to-write-use-markdown.md)
> - [iOS](how-to-write-use-markdown.md)
> - [Android](how-to-write-use-markdown.md)
> - [Kindle](how-to-write-use-markdown.md)
> - [Baidu](how-to-write-use-markdown.md)
> - [Xamarin.iOS](how-to-write-use-markdown.md)
> - [Xamarin.Android](how-to-write-use-markdown.md)

### <a name="multi-selector"></a><span data-ttu-id="9f84c-268">多重选择器</span><span class="sxs-lookup"><span data-stu-id="9f84c-268">Multi-selector</span></span>

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

<span data-ttu-id="9f84c-269">... 将呈现为：</span><span class="sxs-lookup"><span data-stu-id="9f84c-269">... will be rendered like this:</span></span>

> [!div class="op_multi_selector" title1="平台" title2="后端"]
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

## <a name="tables"></a><span data-ttu-id="9f84c-282">表</span><span class="sxs-lookup"><span data-stu-id="9f84c-282">Tables</span></span>

<span data-ttu-id="9f84c-283">使用 Markdown 创建表的最简单方法是借助垂直线和行。</span><span class="sxs-lookup"><span data-stu-id="9f84c-283">The simplest way to create a table in Markdown is to use pipes and lines.</span></span> <span data-ttu-id="9f84c-284">若要创建带标头的标准表格，请在第一行后使用虚线：</span><span class="sxs-lookup"><span data-stu-id="9f84c-284">To create a standard table with a header, follow the first line with dashed line:</span></span>

```md
|This is   |a simple   |table header|
|----------|-----------|------------|
|table     |data       |here        |
|it doesn't|actually   |have to line up nicely!|
```

<span data-ttu-id="9f84c-285">这将呈现为：</span><span class="sxs-lookup"><span data-stu-id="9f84c-285">This renders as follows:</span></span>

|<span data-ttu-id="9f84c-286">This is</span><span class="sxs-lookup"><span data-stu-id="9f84c-286">This is</span></span>   |<span data-ttu-id="9f84c-287">a simple</span><span class="sxs-lookup"><span data-stu-id="9f84c-287">a simple</span></span>   |<span data-ttu-id="9f84c-288">table header</span><span class="sxs-lookup"><span data-stu-id="9f84c-288">table header</span></span>|
|----------|-----------|------------|
|<span data-ttu-id="9f84c-289">table</span><span class="sxs-lookup"><span data-stu-id="9f84c-289">table</span></span>     |<span data-ttu-id="9f84c-290">data</span><span class="sxs-lookup"><span data-stu-id="9f84c-290">data</span></span>       |<span data-ttu-id="9f84c-291">here</span><span class="sxs-lookup"><span data-stu-id="9f84c-291">here</span></span>        |
|<span data-ttu-id="9f84c-292">it doesn't</span><span class="sxs-lookup"><span data-stu-id="9f84c-292">it doesn't</span></span>|<span data-ttu-id="9f84c-293">actually</span><span class="sxs-lookup"><span data-stu-id="9f84c-293">actually</span></span>   |<span data-ttu-id="9f84c-294">have to line up nicely!</span><span class="sxs-lookup"><span data-stu-id="9f84c-294">have to line up nicely!</span></span>||

<span data-ttu-id="9f84c-295">此外，还可创建不含标头的表格。</span><span class="sxs-lookup"><span data-stu-id="9f84c-295">You can also create a table without a header.</span></span> <span data-ttu-id="9f84c-296">例如，创建多列列表：</span><span class="sxs-lookup"><span data-stu-id="9f84c-296">For example, to create a multiple-column list:</span></span>

```md
|   |   |
| - | - |
| This | table |
| has no | header |
```

<span data-ttu-id="9f84c-297">这将呈现为如下所示：</span><span class="sxs-lookup"><span data-stu-id="9f84c-297">This renders like this:</span></span>

|   |   |
| - | - |
| <span data-ttu-id="9f84c-298">This</span><span class="sxs-lookup"><span data-stu-id="9f84c-298">This</span></span> | <span data-ttu-id="9f84c-299">table</span><span class="sxs-lookup"><span data-stu-id="9f84c-299">table</span></span> |
| <span data-ttu-id="9f84c-300">has no</span><span class="sxs-lookup"><span data-stu-id="9f84c-300">has no</span></span> | <span data-ttu-id="9f84c-301">header</span><span class="sxs-lookup"><span data-stu-id="9f84c-301">header</span></span> |

<span data-ttu-id="9f84c-302">可使用冒号来对齐列：</span><span class="sxs-lookup"><span data-stu-id="9f84c-302">You can align the columns by using colons:</span></span>

```md
|                  |
|------------------|
|    right aligned:|
|:left aligned     |
|:centered        :|
```

<span data-ttu-id="9f84c-303">呈现为：</span><span class="sxs-lookup"><span data-stu-id="9f84c-303">Renders as follows:</span></span>

|                  |
|------------------|
|    <span data-ttu-id="9f84c-304">right aligned:</span><span class="sxs-lookup"><span data-stu-id="9f84c-304">right aligned:</span></span>|
|<span data-ttu-id="9f84c-305">:left aligned</span><span class="sxs-lookup"><span data-stu-id="9f84c-305">:left aligned</span></span>     |
|<span data-ttu-id="9f84c-306">:centered        :</span><span class="sxs-lookup"><span data-stu-id="9f84c-306">:centered        :</span></span>|

> [!TIP]
> <span data-ttu-id="9f84c-307">使用 VS Code 的 Docs 创作扩展，可轻松添加基本 Markdown 表格！</span><span class="sxs-lookup"><span data-stu-id="9f84c-307">The Docs Authoring Extension for VS Code makes it easy to add basic Markdown tables!</span></span>
>
> <span data-ttu-id="9f84c-308">此外，还可使用[联机表格生成器](http://www.tablesgenerator.com/markdown_tables)。</span><span class="sxs-lookup"><span data-stu-id="9f84c-308">You can also use an [online table generator](http://www.tablesgenerator.com/markdown_tables).</span></span>

### <a name="mx-tdbreakall"></a><span data-ttu-id="9f84c-309">mx-tdBreakAll</span><span class="sxs-lookup"><span data-stu-id="9f84c-309">mx-tdBreakAll</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9f84c-310">这仅在 docs.microsoft.com 站点上可用。</span><span class="sxs-lookup"><span data-stu-id="9f84c-310">This only works on the docs.microsoft.com site.</span></span>

<span data-ttu-id="9f84c-311">如果使用 Markdown 创建表，表可能会扩展到右侧导航栏，导致表不可读。</span><span class="sxs-lookup"><span data-stu-id="9f84c-311">If you create a table in Markdown, the table might expand to the right navigation and become unreadable.</span></span> <span data-ttu-id="9f84c-312">要解决此问题，请允许文档呈现时根据需要对表格换行。</span><span class="sxs-lookup"><span data-stu-id="9f84c-312">You can solve that by allowing Docs rendering to break the table when needed.</span></span> <span data-ttu-id="9f84c-313">只需使用自定义类 `[!div class="mx-tdBreakAll"]` 即可实现表格换行。</span><span class="sxs-lookup"><span data-stu-id="9f84c-313">Just wrap up the table with the custom class `[!div class="mx-tdBreakAll"]`.</span></span>

<span data-ttu-id="9f84c-314">下面是一个 3 行表格的 Markdown 示例，它通过使用类名为 `mx-tdBreakAll` 的 `div` 实现表格换行。</span><span class="sxs-lookup"><span data-stu-id="9f84c-314">Here is a Markdown sample of a table with three rows that will be wrapped by a `div` with the class name `mx-tdBreakAll`.</span></span>

```md
> [!div class="mx-tdBreakAll"]
> |Name|Syntax|Mandatory for silent installation?|Description|
> |-------------|----------|---------|---------|
> |Quiet|/quiet|Yes|Runs the installer, displaying no UI and no prompts.|
> |NoRestart|/norestart|No|Suppresses any attempts to restart. By default, the UI will prompt before restart.|
> |Help|/help|No|Provides help and quick reference. Displays the correct use of the setup command, including a list of all options and behaviors.|
```

<span data-ttu-id="9f84c-315">它将以如下形式呈现：</span><span class="sxs-lookup"><span data-stu-id="9f84c-315">It will be rendered like this:</span></span>

> [!div class="mx-tdBreakAll"]
> |<span data-ttu-id="9f84c-316">名称</span><span class="sxs-lookup"><span data-stu-id="9f84c-316">Name</span></span>|<span data-ttu-id="9f84c-317">语法</span><span class="sxs-lookup"><span data-stu-id="9f84c-317">Syntax</span></span>|<span data-ttu-id="9f84c-318">是否是无提示安装所必需的？</span><span class="sxs-lookup"><span data-stu-id="9f84c-318">Mandatory for silent installation?</span></span>|<span data-ttu-id="9f84c-319">说明</span><span class="sxs-lookup"><span data-stu-id="9f84c-319">Description</span></span>|
> |-------------|----------|---------|---------|
> |<span data-ttu-id="9f84c-320">Quiet</span><span class="sxs-lookup"><span data-stu-id="9f84c-320">Quiet</span></span>|<span data-ttu-id="9f84c-321">/quiet</span><span class="sxs-lookup"><span data-stu-id="9f84c-321">/quiet</span></span>|<span data-ttu-id="9f84c-322">是</span><span class="sxs-lookup"><span data-stu-id="9f84c-322">Yes</span></span>|<span data-ttu-id="9f84c-323">在不显示 UI 且无提示的情况下运行安装程序。</span><span class="sxs-lookup"><span data-stu-id="9f84c-323">Runs the installer, displaying no UI and no prompts.</span></span>|
> |<span data-ttu-id="9f84c-324">NoRestart</span><span class="sxs-lookup"><span data-stu-id="9f84c-324">NoRestart</span></span>|<span data-ttu-id="9f84c-325">/norestart</span><span class="sxs-lookup"><span data-stu-id="9f84c-325">/norestart</span></span>|<span data-ttu-id="9f84c-326">否</span><span class="sxs-lookup"><span data-stu-id="9f84c-326">No</span></span>|<span data-ttu-id="9f84c-327">禁止所有重启尝试。</span><span class="sxs-lookup"><span data-stu-id="9f84c-327">Suppresses any attempts to restart.</span></span> <span data-ttu-id="9f84c-328">重启前将默认提示 UI。</span><span class="sxs-lookup"><span data-stu-id="9f84c-328">By default, the UI will prompt before restart.</span></span>|
> |<span data-ttu-id="9f84c-329">Help</span><span class="sxs-lookup"><span data-stu-id="9f84c-329">Help</span></span>|<span data-ttu-id="9f84c-330">/help</span><span class="sxs-lookup"><span data-stu-id="9f84c-330">/help</span></span>|<span data-ttu-id="9f84c-331">否</span><span class="sxs-lookup"><span data-stu-id="9f84c-331">No</span></span>|<span data-ttu-id="9f84c-332">提供帮助和快速引用。</span><span class="sxs-lookup"><span data-stu-id="9f84c-332">Provides help and quick reference.</span></span> <span data-ttu-id="9f84c-333">显示安装命令的正确使用方法，包括一个显示全部选项和行为的列表。</span><span class="sxs-lookup"><span data-stu-id="9f84c-333">Displays the correct use of the setup command, including a list of all options and behaviors.</span></span>|

### <a name="mx-tdcol2breakall"></a><span data-ttu-id="9f84c-334">mx-tdCol2BreakAll</span><span class="sxs-lookup"><span data-stu-id="9f84c-334">mx-tdCol2BreakAll</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9f84c-335">这仅在 docs.microsoft.com 站点上可用。</span><span class="sxs-lookup"><span data-stu-id="9f84c-335">This only works on the docs.microsoft.com site.</span></span>

<span data-ttu-id="9f84c-336">有时，表中第二列里的字数可能过长。</span><span class="sxs-lookup"><span data-stu-id="9f84c-336">From time to time, you might have very long words in the second column of a table.</span></span> <span data-ttu-id="9f84c-337">要确保它们能正确换行，可使用 `div` 包装语法应用 `mx-tdCol2BreakAll` 类，其操作方法如前面所述。</span><span class="sxs-lookup"><span data-stu-id="9f84c-337">To ensure they are broken apart nicely, you can apply the class `mx-tdCol2BreakAll` by using the `div` wrapper syntax as shown earlier.</span></span>

### <a name="html-tables"></a><span data-ttu-id="9f84c-338">HTML 表</span><span class="sxs-lookup"><span data-stu-id="9f84c-338">HTML Tables</span></span>

<span data-ttu-id="9f84c-339">不建议将 HTML 表用于 docs.microsoft.com。</span><span class="sxs-lookup"><span data-stu-id="9f84c-339">HTML tables are not recommended for docs.microsoft.com.</span></span> <span data-ttu-id="9f84c-340">它们在源中无法为人所理解，而这是 Markdown 的关键原则。</span><span class="sxs-lookup"><span data-stu-id="9f84c-340">They are not human readable in the source - which is a key principle of Markdown.</span></span>

<!--If you use HTML tables and your Markdown is not being rendered between the two tables, you need to add a closing `br` tag after the closing `table` tag.

![break HTML tables](media/break-tables.png)
-->

## <a name="videos"></a><span data-ttu-id="9f84c-341">视频</span><span class="sxs-lookup"><span data-stu-id="9f84c-341">Videos</span></span>

### <a name="embedding-videos-into-a-markdown-page"></a><span data-ttu-id="9f84c-342">将视频嵌入 Markdown 页面</span><span class="sxs-lookup"><span data-stu-id="9f84c-342">Embedding videos into a Markdown page</span></span>

<span data-ttu-id="9f84c-343">目前，Docs 支持以下 3 个站点中发布的视频：</span><span class="sxs-lookup"><span data-stu-id="9f84c-343">Currently, Docs can support videos published to one of three locations:</span></span>

- <span data-ttu-id="9f84c-344">YouTube</span><span class="sxs-lookup"><span data-stu-id="9f84c-344">YouTube</span></span>
- <span data-ttu-id="9f84c-345">Channel 9</span><span class="sxs-lookup"><span data-stu-id="9f84c-345">Channel 9</span></span>
- <span data-ttu-id="9f84c-346">Microsoft 自己的“One Playe”系统</span><span class="sxs-lookup"><span data-stu-id="9f84c-346">Microsoft's own 'One Player' system</span></span>

<span data-ttu-id="9f84c-347">可使用以下语法嵌入视频，Docs 随即将其呈现。</span><span class="sxs-lookup"><span data-stu-id="9f84c-347">You can embed a video with the following syntax, and Docs will render it.</span></span>

```md
> [!VIDEO <embedded_video_link>]
```

<span data-ttu-id="9f84c-348">示例：</span><span class="sxs-lookup"><span data-stu-id="9f84c-348">Example:</span></span>

```md
> [!VIDEO https://channel9.msdn.com/Series/Youve-Got-Key-Values-A-Redis-Jump-Start/03/player]

> [!VIDEO https://www.youtube.com/embed/iAtwVM-Z7rY]

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS]
```

<span data-ttu-id="9f84c-349">... 将显示为：</span><span class="sxs-lookup"><span data-stu-id="9f84c-349">... will be rendered as:</span></span>

```html
<iframe src="https://channel9.msdn.com/Series/Youve-Got-Key-Values-A-Redis-Jump-Start/03/player" width="640" height="320" allowFullScreen="true" frameBorder="0"></iframe>

<iframe src="https://www.youtube-nocookie.com/embed/iAtwVM-Z7rY" width="640" height="320" allowFullScreen="true" frameBorder="0"></iframe>
<iframe src="https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS" width="640" height="320" allowFullScreen="true" frameBorder="0"></iframe>
```

<span data-ttu-id="9f84c-350">在已发布页面上，它将显示为如下形式：</span><span class="sxs-lookup"><span data-stu-id="9f84c-350">And it will be displayed like this on published pages:</span></span>

> [!VIDEO https://channel9.msdn.com/Series/Youve-Got-Key-Values-A-Redis-Jump-Start/03/player]

> [!VIDEO https://www.youtube.com/embed/iAtwVM-Z7rY]

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS]

> [!IMPORTANT]
> <span data-ttu-id="9f84c-351">CH9 视频 URL 应以 `https` 开头并以 `/player` 结尾。</span><span class="sxs-lookup"><span data-stu-id="9f84c-351">The CH9 video URL should start with `https` and end with `/player`.</span></span> <span data-ttu-id="9f84c-352">否则将嵌入整个页面，而不是只嵌入视频。</span><span class="sxs-lookup"><span data-stu-id="9f84c-352">Otherwise, it will embed the whole page instead of the video only.</span></span>

### <a name="uploading-new-videos"></a><span data-ttu-id="9f84c-353">上传新视频</span><span class="sxs-lookup"><span data-stu-id="9f84c-353">Uploading new videos</span></span>

<span data-ttu-id="9f84c-354">应按照以下流程上传任何新视频：</span><span class="sxs-lookup"><span data-stu-id="9f84c-354">Any new videos should be uploaded using the following process:</span></span>

1. <span data-ttu-id="9f84c-355">加入 IDWEB 上的 docs_video_users 组。</span><span class="sxs-lookup"><span data-stu-id="9f84c-355">Join the **docs_video_users** group on IDWEB.</span></span>
1. <span data-ttu-id="9f84c-356">转到 https://aka.ms/VideoUploadRequest 并填写视频的详细信息。</span><span class="sxs-lookup"><span data-stu-id="9f84c-356">Go to https://aka.ms/VideoUploadRequest and fill in the details for your video.</span></span> <span data-ttu-id="9f84c-357">需填写以下内容（请注意各项内容均非公开所见）：</span><span class="sxs-lookup"><span data-stu-id="9f84c-357">You will need (note that none of these items will be visible to the public):</span></span>
    1. <span data-ttu-id="9f84c-358">视频标题。</span><span class="sxs-lookup"><span data-stu-id="9f84c-358">A title for your video.</span></span>
    1. <span data-ttu-id="9f84c-359">与视频相关的产品/服务列表。</span><span class="sxs-lookup"><span data-stu-id="9f84c-359">A list of products/services that your video is related to.</span></span>
    1. <span data-ttu-id="9f84c-360">承载该视频的目标页面或文档集（如果尚无页面）。</span><span class="sxs-lookup"><span data-stu-id="9f84c-360">The target page or (if you don’t have the page yet) doc set that your video will be hosted on.</span></span>
    1. <span data-ttu-id="9f84c-361">视频 MP4 文件的链接（如果没有用于放置该文件的位置，可暂时将其放于此处：`\\scratch2\scratch\apex`）。</span><span class="sxs-lookup"><span data-stu-id="9f84c-361">A link to the MP4 file for your video (if you don’t have a location to put the file, you can put it here temporarily:   `\\scratch2\scratch\apex`).</span></span> <span data-ttu-id="9f84c-362">MP4 文件应为 720p 或更高。</span><span class="sxs-lookup"><span data-stu-id="9f84c-362">MP4 files should be 720p or higher.</span></span>
    1. <span data-ttu-id="9f84c-363">视频说明。</span><span class="sxs-lookup"><span data-stu-id="9f84c-363">A description of the video.</span></span>
1. <span data-ttu-id="9f84c-364">提交（保存）该项。</span><span class="sxs-lookup"><span data-stu-id="9f84c-364">Submit (save) that item.</span></span>
1. <span data-ttu-id="9f84c-365">视频将在两个工作日内上传。</span><span class="sxs-lookup"><span data-stu-id="9f84c-365">Within two business days, the video will get uploaded.</span></span> <span data-ttu-id="9f84c-366">嵌入所需的链接将放置于工作项内，并将在解析后返回给你。</span><span class="sxs-lookup"><span data-stu-id="9f84c-366">The link you need for embedding will be placed into the work item, and it will be resolved *back to you*.</span></span>
1. <span data-ttu-id="9f84c-367">获取视频链接后，关闭工作项。</span><span class="sxs-lookup"><span data-stu-id="9f84c-367">Once you have grabbed the video link, close the work item.</span></span>
1. <span data-ttu-id="9f84c-368">然后，可使用以下语法，将视频链接添加到文章中：</span><span class="sxs-lookup"><span data-stu-id="9f84c-368">The video link can then be added to your post, using this syntax:</span></span>

   ```md
   > [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS]
   ```
