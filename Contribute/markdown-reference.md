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
# <a name="docs-markdown-reference"></a><span data-ttu-id="c5497-103">Docs Markdown 引用</span><span class="sxs-lookup"><span data-stu-id="c5497-103">Docs Markdown reference</span></span>

<span data-ttu-id="c5497-104">本文按字母顺序提供有关对 docs.microsoft.com (Docs) 编写 Markdown 的引用。</span><span class="sxs-lookup"><span data-stu-id="c5497-104">This article provides an alphabetical reference for writing Markdown for docs.microsoft.com (Docs).</span></span>

<span data-ttu-id="c5497-105">[Markdown](https://daringfireball.net/projects/markdown/) 是一种轻型标记语言，采用纯文本格式语法。</span><span class="sxs-lookup"><span data-stu-id="c5497-105">[Markdown](https://daringfireball.net/projects/markdown/) is a lightweight markup language with plain text formatting syntax.</span></span> <span data-ttu-id="c5497-106">Docs 支持已通过 [Markdig](https://github.com/lunet-io/markdig) 分析引擎进行分析且与 [CommonMark](https://commonmark.org/) 兼容的 Markdown。</span><span class="sxs-lookup"><span data-stu-id="c5497-106">Docs supports [CommonMark](https://commonmark.org/) compliant Markdown parsed through the [Markdig](https://github.com/lunet-io/markdig) parsing engine.</span></span> <span data-ttu-id="c5497-107">Docs 还支持在 Docs 网站上提供更丰富内容的自定义 Markdown 扩展。</span><span class="sxs-lookup"><span data-stu-id="c5497-107">Docs also supports custom Markdown extensions that provide richer content on the Docs site.</span></span>

<span data-ttu-id="c5497-108">可使用任何文本编辑器来编写 Markdown，但建议结合使用 [Visual Studio Code](https://code.visualstudio.com/) 和 [Docs 创作包](https://aka.ms/DocsAuthoringPack)。</span><span class="sxs-lookup"><span data-stu-id="c5497-108">You can use any text editor to write Markdown, but we recommend [Visual Studio Code](https://code.visualstudio.com/) with the [Docs Authoring Pack](https://aka.ms/DocsAuthoringPack).</span></span> <span data-ttu-id="c5497-109">Docs 创作包提供编辑工具和预览功能，让你能够查看文章呈现在 Docs 上时的外观。</span><span class="sxs-lookup"><span data-stu-id="c5497-109">The Docs Authoring Pack provides editing tools and preview functionality that lets you see what your articles will look like when rendered on Docs.</span></span>

## <a name="alerts-note-tip-important-caution-warning"></a><span data-ttu-id="c5497-110">警报（备注、提示、重要提示、提醒、警告）</span><span class="sxs-lookup"><span data-stu-id="c5497-110">Alerts (Note, Tip, Important, Caution, Warning)</span></span>

<span data-ttu-id="c5497-111">警报是用于创建块引用的 Markdown 扩展，这些块引用与指示内容重要性的颜色和图标共同呈现在 docs.microsoft.com 上。</span><span class="sxs-lookup"><span data-stu-id="c5497-111">Alerts are a Markdown extension to create block quotes that render on docs.microsoft.com with colors and icons that indicate the significance of the content.</span></span> <span data-ttu-id="c5497-112">支持以下警报类型：</span><span class="sxs-lookup"><span data-stu-id="c5497-112">The following alert types are supported:</span></span>

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

<span data-ttu-id="c5497-113">这些警报在 docs.microsoft.com 上如下所示：</span><span class="sxs-lookup"><span data-stu-id="c5497-113">These alerts look like this on docs.microsoft.com:</span></span>

> [!NOTE]
> <span data-ttu-id="c5497-114">Information the user should notice even if skimming.</span><span class="sxs-lookup"><span data-stu-id="c5497-114">Information the user should notice even if skimming.</span></span>

> [!TIP]
> <span data-ttu-id="c5497-115">Optional information to help a user be more successful.</span><span class="sxs-lookup"><span data-stu-id="c5497-115">Optional information to help a user be more successful.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c5497-116">Essential information required for user success.</span><span class="sxs-lookup"><span data-stu-id="c5497-116">Essential information required for user success.</span></span>

> [!CAUTION]
> <span data-ttu-id="c5497-117">Negative potential consequences of an action.</span><span class="sxs-lookup"><span data-stu-id="c5497-117">Negative potential consequences of an action.</span></span>

> [!WARNING]
> <span data-ttu-id="c5497-118">Dangerous certain consequences of an action.</span><span class="sxs-lookup"><span data-stu-id="c5497-118">Dangerous certain consequences of an action.</span></span>

### <a name="angle-brackets"></a><span data-ttu-id="c5497-119">尖括号</span><span class="sxs-lookup"><span data-stu-id="c5497-119">Angle brackets</span></span>

<span data-ttu-id="c5497-120">如果在文件中的文本里使用尖括号（例如要表示占位符），则需要对尖括号手动编码。</span><span class="sxs-lookup"><span data-stu-id="c5497-120">If you use angle brackets in text in your file--for example, to denote a placeholder--you need to manually encode the angle brackets.</span></span> <span data-ttu-id="c5497-121">否则，Markdown 会认为它们是一个 HTML 标记。</span><span class="sxs-lookup"><span data-stu-id="c5497-121">Otherwise, Markdown thinks that they're intended to be an HTML tag.</span></span>

<span data-ttu-id="c5497-122">例如，将 `<script name>` 编码为 `&lt;script name&gt;` 或 `\<script name>`。</span><span class="sxs-lookup"><span data-stu-id="c5497-122">For example, encode `<script name>` as `&lt;script name&gt;` or `\<script name>`.</span></span>

<span data-ttu-id="c5497-123">尖括号无需在格式为内联代码的文本中或在代码块中进行转义。</span><span class="sxs-lookup"><span data-stu-id="c5497-123">Angle brackets don't have to be escaped in text formatted as inline code or in code blocks.</span></span>

## <a name="apostrophes-and-quotation-marks"></a><span data-ttu-id="c5497-124">撇号和引号</span><span class="sxs-lookup"><span data-stu-id="c5497-124">Apostrophes and quotation marks</span></span>

<span data-ttu-id="c5497-125">如果将文本从 Word 复制到 Markdown 编辑器，文本可能包含“弯”撇号或弯引号。</span><span class="sxs-lookup"><span data-stu-id="c5497-125">If you copy from Word into a Markdown editor, the text might contain "smart" (curly) apostrophes or quotation marks.</span></span> <span data-ttu-id="c5497-126">需要将这些内容编码或更改为基本撇号或单引号。</span><span class="sxs-lookup"><span data-stu-id="c5497-126">These need to be encoded or changed to basic apostrophes or quotation marks.</span></span> <span data-ttu-id="c5497-127">否则，发布文件时，最终将得到：Itâ€™s</span><span class="sxs-lookup"><span data-stu-id="c5497-127">Otherwise, you end up with things like this when the file is published: Itâ€™s</span></span>

<span data-ttu-id="c5497-128">下面是关于这些“弯”版本标点符号的编码：</span><span class="sxs-lookup"><span data-stu-id="c5497-128">Here are the encodings for the "smart" versions of these punctuation marks:</span></span>

- <span data-ttu-id="c5497-129">左（开）引号：`&#8220;`</span><span class="sxs-lookup"><span data-stu-id="c5497-129">Left (opening) quotation mark: `&#8220;`</span></span>
- <span data-ttu-id="c5497-130">右（闭）引号：`&#8221;`</span><span class="sxs-lookup"><span data-stu-id="c5497-130">Right (closing) quotation mark: `&#8221;`</span></span>
- <span data-ttu-id="c5497-131">右单（闭）引号/撇号：`&#8217;`</span><span class="sxs-lookup"><span data-stu-id="c5497-131">Right (closing) single quotation mark or apostrophe: `&#8217;`</span></span>
- <span data-ttu-id="c5497-132">左单（开）引号（很少使用）：`&#8216;`</span><span class="sxs-lookup"><span data-stu-id="c5497-132">Left (opening) single quotation mark (rarely used): `&#8216;`</span></span>

## <a name="blockquotes"></a><span data-ttu-id="c5497-133">块引用</span><span class="sxs-lookup"><span data-stu-id="c5497-133">Blockquotes</span></span>

<span data-ttu-id="c5497-134">块引用使用 `>` 字符创建：</span><span class="sxs-lookup"><span data-stu-id="c5497-134">Blockquotes are created using the `>` character:</span></span>

```md
> This is a blockquote. It is usually rendered indented and with a different background color.
```

<span data-ttu-id="c5497-135">上述示例的呈现如下所示：</span><span class="sxs-lookup"><span data-stu-id="c5497-135">The preceding example renders as follows:</span></span>

> <span data-ttu-id="c5497-136">这是一个块引用。</span><span class="sxs-lookup"><span data-stu-id="c5497-136">This is a blockquote.</span></span> <span data-ttu-id="c5497-137">它通常以缩进格式呈现，并且具有不同的背景色。</span><span class="sxs-lookup"><span data-stu-id="c5497-137">It is usually rendered indented and with a different background color.</span></span>

## <a name="bold-and-italic-text"></a><span data-ttu-id="c5497-138">粗体和斜体文本</span><span class="sxs-lookup"><span data-stu-id="c5497-138">Bold and italic text</span></span>

<span data-ttu-id="c5497-139">要将文本设置为粗体格式，请用两个星号括住文本  ：</span><span class="sxs-lookup"><span data-stu-id="c5497-139">To format text as **bold**, enclose it in two asterisks:</span></span>

```markdown
This text is **bold**.
```

<span data-ttu-id="c5497-140">要将文本设置为斜体格式，请用一个星号括住文本  ：</span><span class="sxs-lookup"><span data-stu-id="c5497-140">To format text as *italic*, enclose it in a single asterisk:</span></span>

```markdown
This text is *italic*.
```

<span data-ttu-id="c5497-141">要将文本同时设置为粗体和斜体格式，请用三个星号括住文本：</span><span class="sxs-lookup"><span data-stu-id="c5497-141">To format text as both ***bold and italic***, enclose it in three asterisks:</span></span>

```markdown
This text is both ***bold and italic***.
```

## <a name="code-snippets"></a><span data-ttu-id="c5497-142">代码片段</span><span class="sxs-lookup"><span data-stu-id="c5497-142">Code snippets</span></span>

<span data-ttu-id="c5497-143">Docs Markdown 不仅支持将代码片段内联在某个句子中，还支持将它作为单独的“隔离”块放置在两个句子之间。</span><span class="sxs-lookup"><span data-stu-id="c5497-143">Docs Markdown supports the placement of code snippets both inline in a sentence and as a separate "fenced" block between sentences.</span></span> <span data-ttu-id="c5497-144">有关详细信息，请参阅[如何将代码添加到文档](code-in-docs.md)。</span><span class="sxs-lookup"><span data-stu-id="c5497-144">For more information, see [How to add code to docs](code-in-docs.md).</span></span>

## <a name="columns"></a><span data-ttu-id="c5497-145">列</span><span class="sxs-lookup"><span data-stu-id="c5497-145">Columns</span></span>

<span data-ttu-id="c5497-146">通过名为“列”的 Markdown 扩展，Docs 作者可添加基于列的内容布局，这些布局比基本 Markdown 表更灵活、功能更强大，而基本 Markdown 表只适用于真正的表格数据  。</span><span class="sxs-lookup"><span data-stu-id="c5497-146">The **columns** Markdown extension gives Docs authors the ability to add column-based content layouts that are more flexible and powerful than basic Markdown tables, which are only suited for true tabular data.</span></span> <span data-ttu-id="c5497-147">最多可添加 4 列，并需使用可选的 `span` 属性来合并两个或更多列。</span><span class="sxs-lookup"><span data-stu-id="c5497-147">You can add up to four columns, and use the optional `span` attribute to merge two or more columns.</span></span>

<span data-ttu-id="c5497-148">列的语法如下所示：</span><span class="sxs-lookup"><span data-stu-id="c5497-148">The syntax for columns is as follows:</span></span>

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

<span data-ttu-id="c5497-149">列应仅包含基本的 Markdown（包括图像）。</span><span class="sxs-lookup"><span data-stu-id="c5497-149">Columns should only contain basic Markdown, including images.</span></span> <span data-ttu-id="c5497-150">不应包含标题、表、选项卡和其他复杂结构。</span><span class="sxs-lookup"><span data-stu-id="c5497-150">Headings, tables, tabs, and other complex structures shouldn't be included.</span></span> <span data-ttu-id="c5497-151">行不能包含列中没有的任何内容。</span><span class="sxs-lookup"><span data-stu-id="c5497-151">A row can't have any content outside of column.</span></span>

<span data-ttu-id="c5497-152">例如，以下 Markdown 创建了一个跨两个列宽的列和一个标准（无 `span`）列：</span><span class="sxs-lookup"><span data-stu-id="c5497-152">For example, the following Markdown creates one column that spans two column widths, and one standard (no `span`) column:</span></span>

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

<span data-ttu-id="c5497-153">这将呈现为：</span><span class="sxs-lookup"><span data-stu-id="c5497-153">This renders as follows:</span></span>

:::row:::
   :::column span="2":::
      <span data-ttu-id="c5497-154">这是包含大量文本的跨两列的列  。</span><span class="sxs-lookup"><span data-stu-id="c5497-154">**This is a 2-span column with lots of text.**</span></span>

      <span data-ttu-id="c5497-155">Lorem ipsum dolor sit amet, consectetur adipiscing elit.</span><span class="sxs-lookup"><span data-stu-id="c5497-155">Lorem ipsum dolor sit amet, consectetur adipiscing elit.</span></span> <span data-ttu-id="c5497-156">Donec vestibulum mollis nunc ornare commodo.</span><span class="sxs-lookup"><span data-stu-id="c5497-156">Donec vestibulum mollis nunc ornare commodo.</span></span> <span data-ttu-id="c5497-157">Nullam ac metus imperdiet, rutrum justo vel, vulputate leo.</span><span class="sxs-lookup"><span data-stu-id="c5497-157">Nullam ac metus imperdiet, rutrum justo vel, vulputate leo.</span></span> <span data-ttu-id="c5497-158">Donec rutrum non eros eget consectetur.</span><span class="sxs-lookup"><span data-stu-id="c5497-158">Donec rutrum non eros eget consectetur.</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="c5497-159">这是包含图像的单个列  。</span><span class="sxs-lookup"><span data-stu-id="c5497-159">**This is a single-span column with an image in it.**</span></span>

      ![Doc.U.Ment](media/markdown-reference/document.png)
   :::column-end:::
:::row-end:::

## <a name="headings"></a><span data-ttu-id="c5497-161">标题</span><span class="sxs-lookup"><span data-stu-id="c5497-161">Headings</span></span>

<span data-ttu-id="c5497-162">Docs 支持六个级别的 Markdown 标题：</span><span class="sxs-lookup"><span data-stu-id="c5497-162">Docs supports six levels of Markdown headings:</span></span>

```markdown
# This is a first level heading (H1)

## This is a second level heading (H2)

...

###### This is a sixth level heading (H6)
```

- <span data-ttu-id="c5497-163">最后一个 `#` 和标题文本之间必须有空格。</span><span class="sxs-lookup"><span data-stu-id="c5497-163">There must be a space between the last `#` and heading text.</span></span>
- <span data-ttu-id="c5497-164">每个 Markdown 文件必须有且仅有一个 H1 标题。</span><span class="sxs-lookup"><span data-stu-id="c5497-164">Each Markdown file must have one and only one H1 heading.</span></span>
- <span data-ttu-id="c5497-165">H1 标题必须是 YML 元数据块之后的文件中的第一个内容。</span><span class="sxs-lookup"><span data-stu-id="c5497-165">The H1 heading must be the first content in the file after the YML metadata block.</span></span>
- <span data-ttu-id="c5497-166">H2 标题将自动显示在已发布文件右侧的导航菜单中。</span><span class="sxs-lookup"><span data-stu-id="c5497-166">H2 headings automatically appear in the right-hand navigating menu of the published file.</span></span> <span data-ttu-id="c5497-167">而后的低级标题则不会显示，因此策略性地使用 H2 可帮助读者进行内容导航。</span><span class="sxs-lookup"><span data-stu-id="c5497-167">Lower-level headings don't appear, so use H2s strategically to help readers navigate your content.</span></span>
- <span data-ttu-id="c5497-168">不建议使用 HTML 标题（如 `<h1>`），它们在某些情况下会导致出现生成警告。</span><span class="sxs-lookup"><span data-stu-id="c5497-168">HTML headings, such as `<h1>`, aren't recommended, and in some cases will cause build warnings.</span></span>
- <span data-ttu-id="c5497-169">可通过[书签链接](how-to-write-links.md#links-to-anchors)链接到文件中的各个标题。</span><span class="sxs-lookup"><span data-stu-id="c5497-169">You can link to individual headings in a file via [bookmark links](how-to-write-links.md#links-to-anchors).</span></span>

## <a name="html"></a><span data-ttu-id="c5497-170">HTML</span><span class="sxs-lookup"><span data-stu-id="c5497-170">HTML</span></span>

<span data-ttu-id="c5497-171">虽然 Markdown 支持内联式 HTML，但不建议使用 HTML 将内容发布到 Docs，除了数量有限的一系列值以外，其他值会导致生成错误或警告。</span><span class="sxs-lookup"><span data-stu-id="c5497-171">Although Markdown supports inline HTML, HTML isn't recommended for publishing to Docs, and except for a limited list of values will cause build errors or warnings.</span></span> 

## <a name="images"></a><span data-ttu-id="c5497-172">图像</span><span class="sxs-lookup"><span data-stu-id="c5497-172">Images</span></span>

<span data-ttu-id="c5497-173">默认支持以下文件类型的图像：</span><span class="sxs-lookup"><span data-stu-id="c5497-173">The following file types are supported by default for images:</span></span>

- <span data-ttu-id="c5497-174">.jpg</span><span class="sxs-lookup"><span data-stu-id="c5497-174">.jpg</span></span>
- <span data-ttu-id="c5497-175">.png</span><span class="sxs-lookup"><span data-stu-id="c5497-175">.png</span></span>

### <a name="standard-conceptual-images-default-markdown"></a><span data-ttu-id="c5497-176">标准概念图像（默认 Markdown）</span><span class="sxs-lookup"><span data-stu-id="c5497-176">Standard conceptual images (default Markdown)</span></span>

<span data-ttu-id="c5497-177">用于嵌入图像的基本 Markdown 语法为：</span><span class="sxs-lookup"><span data-stu-id="c5497-177">The basic Markdown syntax to embed an image is:</span></span>

```Markdown
![<alt text>](<folderPath>)

Example:
![alt text for image](../images/Introduction.png)
```

<span data-ttu-id="c5497-178">其中 `<alt text>` 是图像的简短说明，`<folder path>` 是图像的相对路径。</span><span class="sxs-lookup"><span data-stu-id="c5497-178">Where `<alt text>` is a brief description of the image and `<folder path>` is a relative path to the image.</span></span> <span data-ttu-id="c5497-179">视觉障碍用户的屏幕阅读器需采用替换文字。</span><span class="sxs-lookup"><span data-stu-id="c5497-179">Alternate text is required for screen readers for the visually impaired.</span></span> <span data-ttu-id="c5497-180">如果出现图像无法呈现的站点 bug，替换文字也非常有用。</span><span class="sxs-lookup"><span data-stu-id="c5497-180">It's also useful if there's a site bug where the image can't render.</span></span>

<span data-ttu-id="c5497-181">无法正确呈现替换文字的下划线，除非使用反斜杠 (`\_`) 作为其前缀来将它进行转义。</span><span class="sxs-lookup"><span data-stu-id="c5497-181">Underscores in alt text aren't rendered properly unless you escape them by prefixing them with a backslash (`\_`).</span></span> <span data-ttu-id="c5497-182">但是，请勿复制用作替换文字的文件名。</span><span class="sxs-lookup"><span data-stu-id="c5497-182">However, don't copy file names for use as alt text.</span></span> <span data-ttu-id="c5497-183">例如，不应编写以下内容：</span><span class="sxs-lookup"><span data-stu-id="c5497-183">For example, instead of this:</span></span>

```markdown
![ADextension_2FA_Configure_Step4](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

<span data-ttu-id="c5497-184">应编写以下内容：</span><span class="sxs-lookup"><span data-stu-id="c5497-184">Write this:</span></span>

```markdown
![Active Directory extension for two-factor authentication, step 4: Configure](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

### <a name="standard-conceptual-images-docs-markdown"></a><span data-ttu-id="c5497-185">标准概念图像（Docs Markdown）</span><span class="sxs-lookup"><span data-stu-id="c5497-185">Standard conceptual images (Docs Markdown)</span></span>

<span data-ttu-id="c5497-186">Docs 自定义 `:::image:::` 扩展支持标准图像、复杂图像和图标。</span><span class="sxs-lookup"><span data-stu-id="c5497-186">The Docs custom `:::image:::` extension supports standard images, complex images, and icons.</span></span>

<span data-ttu-id="c5497-187">对于标准图像，旧的 Markdown 语法仍可用，但推荐使用新的扩展，因为它支持更强大的功能，例如指定与父主题不同的本地化范围。</span><span class="sxs-lookup"><span data-stu-id="c5497-187">For standard images, the older Markdown syntax will still work, but the new extension is recommended because it supports more powerful functionality, such as specifying a localization scope that's different from the parent topic.</span></span> <span data-ttu-id="c5497-188">将来还会提供其他高级功能（例如从共享图像库中选择，而不是指定本地图像）。</span><span class="sxs-lookup"><span data-stu-id="c5497-188">Other advanced functionality, such as selecting from the shared image gallery instead of specifying a local image, will be available in the future.</span></span> <span data-ttu-id="c5497-189">新语法如下所示：</span><span class="sxs-lookup"><span data-stu-id="c5497-189">The new syntax is as follows:</span></span>

```Markdown
:::image type="content" source="<folderPath>" alt-text="<alt text>":::
```

<span data-ttu-id="c5497-190">如果 `type="content"`（默认值），则 `source` 和 `alt-text` 都是必需的。</span><span class="sxs-lookup"><span data-stu-id="c5497-190">If `type="content"` (the default), both `source` and `alt-text` are required.</span></span>

### <a name="complex-images-with-long-descriptions"></a><span data-ttu-id="c5497-191">带有详细说明的复杂图像</span><span class="sxs-lookup"><span data-stu-id="c5497-191">Complex images with long descriptions</span></span>

<span data-ttu-id="c5497-192">还可使用此扩展添加带有详细说明的图像，该图像由屏幕阅读器读取，而不是直观呈现在已发布的页面上。</span><span class="sxs-lookup"><span data-stu-id="c5497-192">You can also use this extension to add an image with a long description that is read by screen readers but not rendered visually on the published page.</span></span> <span data-ttu-id="c5497-193">详细说明是复杂图像（如图形）的可访问性要求。</span><span class="sxs-lookup"><span data-stu-id="c5497-193">Long descriptions are an accessibility requirement for complex images, such as graphs.</span></span> <span data-ttu-id="c5497-194">语法如下所示：</span><span class="sxs-lookup"><span data-stu-id="c5497-194">The syntax is the following:</span></span>

```Markdown
:::image type="complex" source="<folderPath>" alt-text="<alt text>":::
   <long description here>
:::image-end:::
```

<span data-ttu-id="c5497-195">如果 `type="complex"`，则 `source`、`alt-text`、详细说明和 `:::image-end:::` 标记都是必需的。</span><span class="sxs-lookup"><span data-stu-id="c5497-195">If `type="complex"`, `source`, `alt-text`, a long description, and the `:::image-end:::` tag are all required.</span></span>

### <a name="specifying-loc-scope"></a><span data-ttu-id="c5497-196">指定本地化范围</span><span class="sxs-lookup"><span data-stu-id="c5497-196">Specifying loc-scope</span></span>

<span data-ttu-id="c5497-197">有时，图像的本地化范围不同于包含该图像的文章或模块的本地化范围。</span><span class="sxs-lookup"><span data-stu-id="c5497-197">Sometimes the localization scope for an image is different from that of the article or module that contains it.</span></span> <span data-ttu-id="c5497-198">这可能会导致全局体验不佳：例如，产品的屏幕截图被意外本地化为该产品不能使用的语言。</span><span class="sxs-lookup"><span data-stu-id="c5497-198">This can cause a bad global experience: for example, if a screenshot of a product is accidentally localized into a language the product isn't available in.</span></span> <span data-ttu-id="c5497-199">为防止出现此情况，可在类型为 `content` 和 `complex` 的图像中指定可选的 `loc-scope` 属性。</span><span class="sxs-lookup"><span data-stu-id="c5497-199">To prevent this, you can specify the optional `loc-scope` attribute in images of types `content` and `complex`.</span></span>

### <a name="icons"></a><span data-ttu-id="c5497-200">图标</span><span class="sxs-lookup"><span data-stu-id="c5497-200">Icons</span></span>

<span data-ttu-id="c5497-201">图像扩展支持图标（装饰性图像），且不得包含替换文字。</span><span class="sxs-lookup"><span data-stu-id="c5497-201">The image extension supports icons, which are decorative images and should not have alt text.</span></span> <span data-ttu-id="c5497-202">图标的语法如下：</span><span class="sxs-lookup"><span data-stu-id="c5497-202">The syntax for icons is:</span></span>

```Markdown
:::image type="icon" source="<folderPath>":::
```

<span data-ttu-id="c5497-203">如果 `type="icon"`，仅应指定 `source`。</span><span class="sxs-lookup"><span data-stu-id="c5497-203">If `type="icon"`, only `source` should be specified.</span></span>

## <a name="included-markdown-files"></a><span data-ttu-id="c5497-204">包含的 Markdown 文件</span><span class="sxs-lookup"><span data-stu-id="c5497-204">Included Markdown files</span></span>

<span data-ttu-id="c5497-205">如果需要在多篇文章中重复使用 Markdown 文件，可使用包含文件。</span><span class="sxs-lookup"><span data-stu-id="c5497-205">Where markdown files need to be repeated in multiple articles, you can use an include file.</span></span> <span data-ttu-id="c5497-206">包含功能可指示 Docs 在生成时将引用替换为包含文件的内容。</span><span class="sxs-lookup"><span data-stu-id="c5497-206">The includes feature instructs Docs to replace the reference with the contents of the include file at build time.</span></span> <span data-ttu-id="c5497-207">可通过以下方式使用包含文件：</span><span class="sxs-lookup"><span data-stu-id="c5497-207">You can use includes in the following ways:</span></span>

- <span data-ttu-id="c5497-208">内联：重用内联在某句子中的常用文本片段。</span><span class="sxs-lookup"><span data-stu-id="c5497-208">Inline: Reuse a common text snippet inline with within a sentence.</span></span>
- <span data-ttu-id="c5497-209">块：将整个 Markdown 文件作为一个块重用，嵌套在文章的某一部分中。</span><span class="sxs-lookup"><span data-stu-id="c5497-209">Block: Reuse an entire Markdown file as a block, nested within a section of an article.</span></span>

<span data-ttu-id="c5497-210">“内联”和“块”包含文件是 Markdown (.md) 文件。</span><span class="sxs-lookup"><span data-stu-id="c5497-210">An inline or block include file is a Markdown (.md) file.</span></span> <span data-ttu-id="c5497-211">它可以包含任何有效的 Markdown。</span><span class="sxs-lookup"><span data-stu-id="c5497-211">It can contain any valid Markdown.</span></span> <span data-ttu-id="c5497-212">包含文件通常位于存储库根目录中的公共包含子目录中  。</span><span class="sxs-lookup"><span data-stu-id="c5497-212">Include files are typically located in a common *includes* subdirectory, in the root of the repository.</span></span> <span data-ttu-id="c5497-213">发布文章时，加入的文件会无缝集成到其中。</span><span class="sxs-lookup"><span data-stu-id="c5497-213">When the article is published, the included file is seamlessly integrated into it.</span></span>

### <a name="includes-syntax"></a><span data-ttu-id="c5497-214">包含文件语法</span><span class="sxs-lookup"><span data-stu-id="c5497-214">Includes syntax</span></span>

<span data-ttu-id="c5497-215">块包含文件位于其自己的行上：</span><span class="sxs-lookup"><span data-stu-id="c5497-215">Block include is on its own line:</span></span>

```markdown
[!INCLUDE [<title>](<filepath>)]
```

<span data-ttu-id="c5497-216">内联包含文件位于行中：</span><span class="sxs-lookup"><span data-stu-id="c5497-216">Inline include is within a line:</span></span>

```markdown
Text before [!INCLUDE [<title>](<filepath>)] and after.
```

<span data-ttu-id="c5497-217">其中，`<title>` 是文件名，`<filepath>` 是该文件的相对路径。</span><span class="sxs-lookup"><span data-stu-id="c5497-217">Where `<title>` is the name of the file and `<filepath>` is the relative path to the file.</span></span> <span data-ttu-id="c5497-218">`INCLUDE` 必须大写，并且 `<title>` 前必须有一个空格。</span><span class="sxs-lookup"><span data-stu-id="c5497-218">`INCLUDE` must be capitalized and there must be a space before the `<title>`.</span></span>

<span data-ttu-id="c5497-219">包含文件的要求和注意事项如下：</span><span class="sxs-lookup"><span data-stu-id="c5497-219">Here are requirements and considerations for include files:</span></span>

- <span data-ttu-id="c5497-220">块包含文件用于大篇幅内容，比如一个或者两个段落、共享过程或者共享章节。</span><span class="sxs-lookup"><span data-stu-id="c5497-220">Use block includes for significant amounts of content--a paragraph or two, a shared procedure, or a shared section.</span></span> <span data-ttu-id="c5497-221">请勿将它们用于小于一个句子的内容。</span><span class="sxs-lookup"><span data-stu-id="c5497-221">Do not use them for anything smaller than a sentence.</span></span>
- <span data-ttu-id="c5497-222">包含文件不会在文章的 GitHub 呈现视图中显示，因为它们依赖于 Docs 扩展。</span><span class="sxs-lookup"><span data-stu-id="c5497-222">Includes won't be rendered in the GitHub rendered view of your article, because they rely on Docs extensions.</span></span> <span data-ttu-id="c5497-223">它们在发布后才会显示。</span><span class="sxs-lookup"><span data-stu-id="c5497-223">They'll be rendered only after publication.</span></span>
- <span data-ttu-id="c5497-224">确保包含文件中的所有文本都是完整的句子或者段落，并且与引用该包含文件的文章的前后文没有关联。</span><span class="sxs-lookup"><span data-stu-id="c5497-224">Ensure that all the text in an include file is written in complete sentences or phrases that do not depend on preceding text or following text in the article that references the include.</span></span> <span data-ttu-id="c5497-225">如果不遵循此指导原则，则会在文章中创建无法转换的字符串。</span><span class="sxs-lookup"><span data-stu-id="c5497-225">Ignoring this guidance creates an untranslatable string in the article.</span></span>
- <span data-ttu-id="c5497-226">请勿在其他包含文件中嵌入包含文件。</span><span class="sxs-lookup"><span data-stu-id="c5497-226">Don't embed include files within other include files.</span></span>
- <span data-ttu-id="c5497-227">将媒体文件放在特定于包含文件子目录的媒体文件夹中，例如 `<repo>`/includes/media 文件夹  。</span><span class="sxs-lookup"><span data-stu-id="c5497-227">Place media files in a media folder that's specific to the include subdirectory--for instance, the `<repo>`*/includes/media* folder.</span></span> <span data-ttu-id="c5497-228">媒体目录不应在根目录中包含任何图像  。</span><span class="sxs-lookup"><span data-stu-id="c5497-228">The *media* directory should not contain any images in its root.</span></span> <span data-ttu-id="c5497-229">如果包含文件不包含图像，则不需要相应的媒体目录  。</span><span class="sxs-lookup"><span data-stu-id="c5497-229">If the include does not have images, a corresponding *media* directory is not required.</span></span>
- <span data-ttu-id="c5497-230">对于常规文章，请勿在各包含文件之间共享媒体。</span><span class="sxs-lookup"><span data-stu-id="c5497-230">As with regular articles, don't share media between include files.</span></span> <span data-ttu-id="c5497-231">对于每个包含文件和文章，请使用具有唯一名称的单独文件。</span><span class="sxs-lookup"><span data-stu-id="c5497-231">Use a separate file with a unique name for each include and article.</span></span> <span data-ttu-id="c5497-232">将媒体文件存储在与包含文件关联的媒体文件夹中。</span><span class="sxs-lookup"><span data-stu-id="c5497-232">Store the media file in the media folder that's associated with the include.</span></span>
- <span data-ttu-id="c5497-233">请勿将包含文件用作文章的唯一内容。</span><span class="sxs-lookup"><span data-stu-id="c5497-233">Don't use an include as the only content of an article.</span></span>  <span data-ttu-id="c5497-234">包含文件主要用作文章其余内容的补充内容。</span><span class="sxs-lookup"><span data-stu-id="c5497-234">Includes are meant to be supplemental to the content in the rest of the article.</span></span>

## <a name="links"></a><span data-ttu-id="c5497-235">链接</span><span class="sxs-lookup"><span data-stu-id="c5497-235">Links</span></span>

<span data-ttu-id="c5497-236">要了解链接的语法，请参阅[在文档中使用链接](how-to-write-links.md)。</span><span class="sxs-lookup"><span data-stu-id="c5497-236">For information on syntax for links, see [Use links in documentation](how-to-write-links.md).</span></span>

## <a name="lists-numbered-bulleted-checklist"></a><span data-ttu-id="c5497-237">列表（带编号、显示项目符号、清单）</span><span class="sxs-lookup"><span data-stu-id="c5497-237">Lists (Numbered, Bulleted, Checklist)</span></span>

### <a name="numbered-list"></a><span data-ttu-id="c5497-238">编号列表</span><span class="sxs-lookup"><span data-stu-id="c5497-238">Numbered list</span></span>

<span data-ttu-id="c5497-239">要创建编号列表，可全部使用 1。</span><span class="sxs-lookup"><span data-stu-id="c5497-239">To create a numbered list, you can use all 1s.</span></span> <span data-ttu-id="c5497-240">发布后，这些编号会按升序顺序呈现为顺序列表。</span><span class="sxs-lookup"><span data-stu-id="c5497-240">The numbers are rendered in ascending order as a sequential list when published.</span></span> <span data-ttu-id="c5497-241">为提高源可读性，可手动增加列表。</span><span class="sxs-lookup"><span data-stu-id="c5497-241">For increased source readability, you can increment your lists manually.</span></span>

<span data-ttu-id="c5497-242">请勿在列表中使用字母，也勿使用嵌套列表。</span><span class="sxs-lookup"><span data-stu-id="c5497-242">Don't use letters in lists, including nested lists.</span></span> <span data-ttu-id="c5497-243">发布到 Docs 时，它们无法正确呈现。使用编号的嵌套列表在发布时将呈现为小写字母。</span><span class="sxs-lookup"><span data-stu-id="c5497-243">They don't render correctly when published to Docs. Nested lists using numbers will render as lowercase letters when published.</span></span> <span data-ttu-id="c5497-244">例如：</span><span class="sxs-lookup"><span data-stu-id="c5497-244">For example:</span></span>

```markdown
1. This is
1. a parent numbered list
   1. and this is
   1. a nested numbered list
1. (fin)
```

<span data-ttu-id="c5497-245">这将呈现为：</span><span class="sxs-lookup"><span data-stu-id="c5497-245">This renders as follows:</span></span>

1. <span data-ttu-id="c5497-246">This is</span><span class="sxs-lookup"><span data-stu-id="c5497-246">This is</span></span>
1. <span data-ttu-id="c5497-247">a parent numbered list</span><span class="sxs-lookup"><span data-stu-id="c5497-247">a parent numbered list</span></span>
   1. <span data-ttu-id="c5497-248">and this is</span><span class="sxs-lookup"><span data-stu-id="c5497-248">and this is</span></span>
   1. <span data-ttu-id="c5497-249">a nested numbered list</span><span class="sxs-lookup"><span data-stu-id="c5497-249">a nested numbered list</span></span>
1. <span data-ttu-id="c5497-250">(fin)</span><span class="sxs-lookup"><span data-stu-id="c5497-250">(fin)</span></span>

### <a name="bulleted-list"></a><span data-ttu-id="c5497-251">项目符号列表</span><span class="sxs-lookup"><span data-stu-id="c5497-251">Bulleted list</span></span>

<span data-ttu-id="c5497-252">若要创建项目符号列表，请使用 `-` 或 `*`，其后每行开头跟一个空格：</span><span class="sxs-lookup"><span data-stu-id="c5497-252">To create a bulleted list, use `-` or `*` followed by a space at the beginning of each line:</span></span>

```markdown
- This is
- a parent bulleted list
  - and this is
  - a nested bulleted list
- All done!
```

<span data-ttu-id="c5497-253">这将呈现为：</span><span class="sxs-lookup"><span data-stu-id="c5497-253">This renders as follows:</span></span>

- <span data-ttu-id="c5497-254">This is</span><span class="sxs-lookup"><span data-stu-id="c5497-254">This is</span></span>
- <span data-ttu-id="c5497-255">a parent bulleted list</span><span class="sxs-lookup"><span data-stu-id="c5497-255">a parent bulleted list</span></span>
  - <span data-ttu-id="c5497-256">and this is</span><span class="sxs-lookup"><span data-stu-id="c5497-256">and this is</span></span>
  - <span data-ttu-id="c5497-257">a nested bulleted list</span><span class="sxs-lookup"><span data-stu-id="c5497-257">a nested bulleted list</span></span>
- <span data-ttu-id="c5497-258">All done!</span><span class="sxs-lookup"><span data-stu-id="c5497-258">All done!</span></span>

<span data-ttu-id="c5497-259">无论使用哪种语法（`-` 或 `*`），都请在一篇文章中始终使用它。</span><span class="sxs-lookup"><span data-stu-id="c5497-259">Whichever syntax you use, `-` or `*`, use it consistently within an article.</span></span>

### <a name="checklist"></a><span data-ttu-id="c5497-260">清单</span><span class="sxs-lookup"><span data-stu-id="c5497-260">Checklist</span></span>

<span data-ttu-id="c5497-261">清单仅可通过自定义 Markdown 扩展在 Docs 上使用：</span><span class="sxs-lookup"><span data-stu-id="c5497-261">Checklists are available for use on Docs via a custom Markdown extension:</span></span>

```markdown
> [!div class="checklist"]
> * List item 1
> * List item 2
> * List item 3
```

<span data-ttu-id="c5497-262">此示例在 Docs 上呈现为：</span><span class="sxs-lookup"><span data-stu-id="c5497-262">This example renders on Docs like this:</span></span>

> [!div class="checklist"]
> * <span data-ttu-id="c5497-263">List item 1</span><span class="sxs-lookup"><span data-stu-id="c5497-263">List item 1</span></span>
> * <span data-ttu-id="c5497-264">List item 2</span><span class="sxs-lookup"><span data-stu-id="c5497-264">List item 2</span></span>
> * <span data-ttu-id="c5497-265">List item 3</span><span class="sxs-lookup"><span data-stu-id="c5497-265">List item 3</span></span>

<span data-ttu-id="c5497-266">在文章开头或结尾使用清单，总结“将要学习的内容”或“所学内容”。</span><span class="sxs-lookup"><span data-stu-id="c5497-266">Use checklists at the beginning or end of an article to summarize "What will you learn" or "What have you learned" content.</span></span> <span data-ttu-id="c5497-267">请勿在整篇文章中添加随机清单。</span><span class="sxs-lookup"><span data-stu-id="c5497-267">Do not add random checklists throughout your articles.</span></span>

## <a name="next-step-action"></a><span data-ttu-id="c5497-268">下一步操作</span><span class="sxs-lookup"><span data-stu-id="c5497-268">Next step action</span></span>

<span data-ttu-id="c5497-269">可使用自定义扩展向 Docs 页面添加下一步操作按钮。</span><span class="sxs-lookup"><span data-stu-id="c5497-269">You can use a custom extension to add a next step action button to Docs pages.</span></span>

<span data-ttu-id="c5497-270">语法如下所示：</span><span class="sxs-lookup"><span data-stu-id="c5497-270">The syntax is as follows:</span></span>

```markdown
> [!div class="nextstepaction"]
> [button text](link to topic)
```

<span data-ttu-id="c5497-271">例如：</span><span class="sxs-lookup"><span data-stu-id="c5497-271">For example:</span></span>

```markdown
> [!div class="nextstepaction"]
> [Learn about adding code to articles](code-in-docs.md)
```

<span data-ttu-id="c5497-272">这将呈现为：</span><span class="sxs-lookup"><span data-stu-id="c5497-272">This renders as follows:</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="c5497-273">了解如何向文章添加代码</span><span class="sxs-lookup"><span data-stu-id="c5497-273">Learn about adding code to articles</span></span>](code-in-docs.md)

<span data-ttu-id="c5497-274">可在下一步操作中使用任何受支持的链接，包括指向其他网页的 Markdown 链接。</span><span class="sxs-lookup"><span data-stu-id="c5497-274">You can use any supported link in a next step action, including a Markdown link to another web page.</span></span> <span data-ttu-id="c5497-275">在大多数情况下，下一操作链接是同一文档集中另一个文件的相对链接。</span><span class="sxs-lookup"><span data-stu-id="c5497-275">In most cases, the next action link will be a relative link to another file in the same docset.</span></span>

## <a name="non-localized-strings"></a><span data-ttu-id="c5497-276">非本地化字符串</span><span class="sxs-lookup"><span data-stu-id="c5497-276">Non-localized strings</span></span>

<span data-ttu-id="c5497-277">可使用自定义 `no-loc` Markdown 扩展来标识你希望在本地化过程中忽略的内容中的字符串。</span><span class="sxs-lookup"><span data-stu-id="c5497-277">You can use the custom `no-loc` Markdown extension to identify strings of content that you would like the localization process to ignore.</span></span>

<span data-ttu-id="c5497-278">所有调用的字符串都将区分大小写；即字符串必须完全匹配，才能在本地化过程中被忽略。</span><span class="sxs-lookup"><span data-stu-id="c5497-278">All strings called out will be case-sensitive; that is, the string must match exactly to be ignored for localization.</span></span>

<span data-ttu-id="c5497-279">若要将单个字符串标记为不可本地化，请使用以下语法：</span><span class="sxs-lookup"><span data-stu-id="c5497-279">To mark an individual string as non-localizable, use this syntax:</span></span>

```markdown
:::no-loc text="String":::
```

<span data-ttu-id="c5497-280">例如，在以下示例中，本地化过程中只会忽略 `Document` 的单个实例：</span><span class="sxs-lookup"><span data-stu-id="c5497-280">For example, in the following, only the single instance of `Document` will be ignored during the localization process:</span></span>

```markdown
# Heading 1 of the Document

Markdown content within the :::no-loc text="Document":::.  The are multiple instances of Document, document, and documents.
```

> [!NOTE]
> <span data-ttu-id="c5497-281">使用 `\` 转义特殊字符：</span><span class="sxs-lookup"><span data-stu-id="c5497-281">Use `\` to escape special characters:</span></span>
> ```markdown
> Lorem :::no-loc text="Find a \"Quotation\""::: Ipsum.
> ```

<span data-ttu-id="c5497-282">还可以使用 YAML 标头中的元数据将当前 Markdown 文件中字符串的所有实例标记为不可本地化：</span><span class="sxs-lookup"><span data-stu-id="c5497-282">You can also use metadata in the YAML header to mark all instances of a string within the current Markdown file as non-localizable:</span></span>

```yml
author: cillroy
no-loc: [Global, Strings, to be, Ignored]
```

> [!NOTE]
> <span data-ttu-id="c5497-283">在 docfx.json 文件中，不支持将不可本地化的元数据作为全局元数据  。</span><span class="sxs-lookup"><span data-stu-id="c5497-283">The no-loc metadata is not supported as global metadata in *docfx.json* file.</span></span> <span data-ttu-id="c5497-284">本地化管道不会读取 docfx.json 文件，因此必须将不可本地化的元数据添加到每个单独的源文件中  。</span><span class="sxs-lookup"><span data-stu-id="c5497-284">The localization pipeline doesn't read the *docfx.json* file, so the no-loc metadata must be added into each individual source file.</span></span>

<span data-ttu-id="c5497-285">在下示例中，本地化过程中将同时忽略元数据 `title` 和 Markdown 标头中的 `Document` 一词。</span><span class="sxs-lookup"><span data-stu-id="c5497-285">In the following example, both in the metadata `title` and the Markdown header the word `Document` will be ignored during the localization process.</span></span>

<span data-ttu-id="c5497-286">在元数据 `description` 和 Markdown 主要内容中，会对 `document` 一词进行本地化，因此该词没有以大写的 `D` 开头。</span><span class="sxs-lookup"><span data-stu-id="c5497-286">In the metadata `description` and the Markdown main content the word `document` is localized, because it does not start with a capital `D`.</span></span>

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

## <a name="selectors"></a><span data-ttu-id="c5497-287">选择器</span><span class="sxs-lookup"><span data-stu-id="c5497-287">Selectors</span></span>

<span data-ttu-id="c5497-288">选择器是 UI 元素，用户可用它在同一篇文章的多种风格之间切换。</span><span class="sxs-lookup"><span data-stu-id="c5497-288">Selectors are UI elements that let the user switch between multiple flavors of the same article.</span></span> <span data-ttu-id="c5497-289">它们在某些文档集中用来解决跨技术或平台实现的差异。</span><span class="sxs-lookup"><span data-stu-id="c5497-289">They are used in some doc sets to address differences in implementation across technologies or platforms.</span></span> <span data-ttu-id="c5497-290">选择器通常最适用于开发人员的移动平台内容。</span><span class="sxs-lookup"><span data-stu-id="c5497-290">Selectors are typically most applicable to our mobile platform content for developers.</span></span>

<span data-ttu-id="c5497-291">由于使用选择器的每个文章文件中都会出现相同的选择器 Markdown，因此建议将文章的选择器放在包含文件中。</span><span class="sxs-lookup"><span data-stu-id="c5497-291">Because the same selector Markdown goes in each article file that uses the selector, we recommend placing the selector for your article in an include file.</span></span> <span data-ttu-id="c5497-292">然后，可以在使用相同选择器的所有文章文件中引用该包含文件。</span><span class="sxs-lookup"><span data-stu-id="c5497-292">Then you can reference that include file in all your article files that use the same selector.</span></span>

<span data-ttu-id="c5497-293">有两种类型的选择器：单选择器和多选择器。</span><span class="sxs-lookup"><span data-stu-id="c5497-293">There are two types of selectors: a single selector and a multi-selector.</span></span>

### <a name="single-selector"></a><span data-ttu-id="c5497-294">单一选择器</span><span class="sxs-lookup"><span data-stu-id="c5497-294">Single selector</span></span>

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

<span data-ttu-id="c5497-295">... 将呈现为：</span><span class="sxs-lookup"><span data-stu-id="c5497-295">... will be rendered like this:</span></span>

> [!div class="op_single_selector"]
> - [Universal Windows](how-to-write-links.md)
> - [Windows Phone](how-to-write-links.md)
> - [iOS](how-to-write-links.md)
> - [Android](how-to-write-links.md)
> - [Kindle](how-to-write-links.md)
> - [Baidu](how-to-write-links.md)
> - [Xamarin.iOS](how-to-write-links.md)
> - [Xamarin.Android](how-to-write-links.md)

### <a name="multi-selector"></a><span data-ttu-id="c5497-304">多重选择器</span><span class="sxs-lookup"><span data-stu-id="c5497-304">Multi-selector</span></span>

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

<span data-ttu-id="c5497-305">... 将呈现为：</span><span class="sxs-lookup"><span data-stu-id="c5497-305">... will be rendered like this:</span></span>

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

## <a name="subscript-and-superscript"></a><span data-ttu-id="c5497-318">下标和上标</span><span class="sxs-lookup"><span data-stu-id="c5497-318">Subscript and superscript</span></span>

<span data-ttu-id="c5497-319">应仅在要求技术准确性时使用下标或上标，例如在写数学公式时。</span><span class="sxs-lookup"><span data-stu-id="c5497-319">You should only use subscript or superscript when necessary for technical accuracy, such as when writing about mathematical formulas.</span></span> <span data-ttu-id="c5497-320">不要将它们用于非标准样式，如脚注。</span><span class="sxs-lookup"><span data-stu-id="c5497-320">Don't use them for non-standard styles, such as footnotes.</span></span>

<span data-ttu-id="c5497-321">对于下标和上标，请使用 HTML：</span><span class="sxs-lookup"><span data-stu-id="c5497-321">For both subscript and superscript, use HTML:</span></span>

```html
Hello <sub>This is subscript!</sub>
```

<span data-ttu-id="c5497-322">这将呈现为：</span><span class="sxs-lookup"><span data-stu-id="c5497-322">This renders as follows:</span></span>

<span data-ttu-id="c5497-323">Hello <sub>This is subscript!</sub></span><span class="sxs-lookup"><span data-stu-id="c5497-323">Hello <sub>This is subscript!</sub></span></span>

```html
Goodbye <sup>This is superscript!</sup>
```

<span data-ttu-id="c5497-324">这将呈现为：</span><span class="sxs-lookup"><span data-stu-id="c5497-324">This renders as follows:</span></span>

<span data-ttu-id="c5497-325">Goodbye <sup>This is superscript!</sup></span><span class="sxs-lookup"><span data-stu-id="c5497-325">Goodbye <sup>This is superscript!</sup></span></span>

## <a name="tables"></a><span data-ttu-id="c5497-326">表</span><span class="sxs-lookup"><span data-stu-id="c5497-326">Tables</span></span>

<span data-ttu-id="c5497-327">使用 Markdown 创建表的最简单方法是借助垂直线和行。</span><span class="sxs-lookup"><span data-stu-id="c5497-327">The simplest way to create a table in Markdown is to use pipes and lines.</span></span> <span data-ttu-id="c5497-328">若要创建带标头的标准表格，请在第一行后使用虚线：</span><span class="sxs-lookup"><span data-stu-id="c5497-328">To create a standard table with a header, follow the first line with dashed line:</span></span>

```markdown
|This is   |a simple   |table header|
|----------|-----------|------------|
|table     |data       |here        |
|it doesn't|actually   |have to line up nicely!|
```

<span data-ttu-id="c5497-329">这将呈现为：</span><span class="sxs-lookup"><span data-stu-id="c5497-329">This renders as follows:</span></span>

|<span data-ttu-id="c5497-330">This is</span><span class="sxs-lookup"><span data-stu-id="c5497-330">This is</span></span>   |<span data-ttu-id="c5497-331">a simple</span><span class="sxs-lookup"><span data-stu-id="c5497-331">a simple</span></span>   |<span data-ttu-id="c5497-332">table header</span><span class="sxs-lookup"><span data-stu-id="c5497-332">table header</span></span>|
|----------|-----------|------------|
|<span data-ttu-id="c5497-333">table</span><span class="sxs-lookup"><span data-stu-id="c5497-333">table</span></span>     |<span data-ttu-id="c5497-334">data</span><span class="sxs-lookup"><span data-stu-id="c5497-334">data</span></span>       |<span data-ttu-id="c5497-335">here</span><span class="sxs-lookup"><span data-stu-id="c5497-335">here</span></span>        |
|<span data-ttu-id="c5497-336">it doesn't</span><span class="sxs-lookup"><span data-stu-id="c5497-336">it doesn't</span></span>|<span data-ttu-id="c5497-337">actually</span><span class="sxs-lookup"><span data-stu-id="c5497-337">actually</span></span>   |<span data-ttu-id="c5497-338">have to line up nicely!</span><span class="sxs-lookup"><span data-stu-id="c5497-338">have to line up nicely!</span></span>||

<span data-ttu-id="c5497-339">可使用冒号来对齐列：</span><span class="sxs-lookup"><span data-stu-id="c5497-339">You can align the columns by using colons:</span></span>

```markdown
| Fun                  | With                 | Tables          |
| :------------------- | -------------------: |:---------------:|
| left-aligned column  | right-aligned column | centered column |
| $100                 | $100                 | $100            |
| $10                  | $10                  | $10             |
| $1                   | $1                   | $1              |
```

<span data-ttu-id="c5497-340">呈现为：</span><span class="sxs-lookup"><span data-stu-id="c5497-340">Renders as follows:</span></span>

| <span data-ttu-id="c5497-341">Fun</span><span class="sxs-lookup"><span data-stu-id="c5497-341">Fun</span></span>                  | <span data-ttu-id="c5497-342">With</span><span class="sxs-lookup"><span data-stu-id="c5497-342">With</span></span>                 | <span data-ttu-id="c5497-343">Tables</span><span class="sxs-lookup"><span data-stu-id="c5497-343">Tables</span></span>          |
| :------------------- | -------------------: |:---------------:|
| <span data-ttu-id="c5497-344">left-aligned column</span><span class="sxs-lookup"><span data-stu-id="c5497-344">left-aligned column</span></span>  | <span data-ttu-id="c5497-345">right-aligned column</span><span class="sxs-lookup"><span data-stu-id="c5497-345">right-aligned column</span></span> | <span data-ttu-id="c5497-346">centered column</span><span class="sxs-lookup"><span data-stu-id="c5497-346">centered column</span></span> |
| <span data-ttu-id="c5497-347">$100</span><span class="sxs-lookup"><span data-stu-id="c5497-347">$100</span></span>                 | <span data-ttu-id="c5497-348">$100</span><span class="sxs-lookup"><span data-stu-id="c5497-348">$100</span></span>                 | <span data-ttu-id="c5497-349">$100</span><span class="sxs-lookup"><span data-stu-id="c5497-349">$100</span></span>            |
| <span data-ttu-id="c5497-350">$10</span><span class="sxs-lookup"><span data-stu-id="c5497-350">$10</span></span>                  | <span data-ttu-id="c5497-351">$10</span><span class="sxs-lookup"><span data-stu-id="c5497-351">$10</span></span>                  | <span data-ttu-id="c5497-352">$10</span><span class="sxs-lookup"><span data-stu-id="c5497-352">$10</span></span>             |
| <span data-ttu-id="c5497-353">$1</span><span class="sxs-lookup"><span data-stu-id="c5497-353">$1</span></span>                   | <span data-ttu-id="c5497-354">$1</span><span class="sxs-lookup"><span data-stu-id="c5497-354">$1</span></span>                   | <span data-ttu-id="c5497-355">$1</span><span class="sxs-lookup"><span data-stu-id="c5497-355">$1</span></span>              |

> [!TIP]
> <span data-ttu-id="c5497-356">使用 VS Code 的 Docs 创作扩展，可轻松添加基本 Markdown 表格！</span><span class="sxs-lookup"><span data-stu-id="c5497-356">The Docs Authoring Extension for VS Code makes it easy to add basic Markdown tables!</span></span>
>
> <span data-ttu-id="c5497-357">此外，还可使用[联机表格生成器](http://www.tablesgenerator.com/markdown_tables)。</span><span class="sxs-lookup"><span data-stu-id="c5497-357">You can also use an [online table generator](http://www.tablesgenerator.com/markdown_tables).</span></span>

### <a name="line-breaks-within-words-in-any-table-cell"></a><span data-ttu-id="c5497-358">任何表格单元格中单词内的换行符</span><span class="sxs-lookup"><span data-stu-id="c5497-358">Line breaks within words in any table cell</span></span>

<span data-ttu-id="c5497-359">Markdown 中较长的单词可能会扩展到右侧导航栏，导致表不可读。</span><span class="sxs-lookup"><span data-stu-id="c5497-359">Long words in a Markdown table might make the table expand to the right navigation and become unreadable.</span></span> <span data-ttu-id="c5497-360">可通过允许 Docs 渲染，必要时自动在单词内插入换行符来解决此问题。</span><span class="sxs-lookup"><span data-stu-id="c5497-360">You can solve that by allowing Docs rendering to automatically insert line breaks within words when needed.</span></span> <span data-ttu-id="c5497-361">只需使用自定义类 `[!div class="mx-tdBreakAll"]` 即可实现表格换行。</span><span class="sxs-lookup"><span data-stu-id="c5497-361">Just wrap up the table with the custom class `[!div class="mx-tdBreakAll"]`.</span></span>

<span data-ttu-id="c5497-362">下面是一个 3 行表格的 Markdown 示例，它通过使用类名为 `mx-tdBreakAll` 的 `div` 实现表格换行。</span><span class="sxs-lookup"><span data-stu-id="c5497-362">Here is a Markdown sample of a table with three rows that will be wrapped by a `div` with the class name `mx-tdBreakAll`.</span></span>

```markdown
> [!div class="mx-tdBreakAll"]
> |Name|Syntax|Mandatory for silent installation?|Description|
> |-------------|----------|---------|---------|
> |Quiet|/quiet|Yes|Runs the installer, displaying no UI and no prompts.|
> |NoRestart|/norestart|No|Suppresses any attempts to restart. By default, the UI will prompt before restart.|
> |Help|/help|No|Provides help and quick reference. Displays the correct use of the setup command, including a list of all options and behaviors.|
```

<span data-ttu-id="c5497-363">它将以如下形式呈现：</span><span class="sxs-lookup"><span data-stu-id="c5497-363">It will be rendered like this:</span></span>

> [!div class="mx-tdBreakAll"]
> |<span data-ttu-id="c5497-364">名称</span><span class="sxs-lookup"><span data-stu-id="c5497-364">Name</span></span>|<span data-ttu-id="c5497-365">语法</span><span class="sxs-lookup"><span data-stu-id="c5497-365">Syntax</span></span>|<span data-ttu-id="c5497-366">是否是无提示安装所必需的？</span><span class="sxs-lookup"><span data-stu-id="c5497-366">Mandatory for silent installation?</span></span>|<span data-ttu-id="c5497-367">说明</span><span class="sxs-lookup"><span data-stu-id="c5497-367">Description</span></span>|
> |-------------|----------|---------|---------|
> |<span data-ttu-id="c5497-368">Quiet</span><span class="sxs-lookup"><span data-stu-id="c5497-368">Quiet</span></span>|<span data-ttu-id="c5497-369">/quiet</span><span class="sxs-lookup"><span data-stu-id="c5497-369">/quiet</span></span>|<span data-ttu-id="c5497-370">是</span><span class="sxs-lookup"><span data-stu-id="c5497-370">Yes</span></span>|<span data-ttu-id="c5497-371">在不显示 UI 且无提示的情况下运行安装程序。</span><span class="sxs-lookup"><span data-stu-id="c5497-371">Runs the installer, displaying no UI and no prompts.</span></span>|
> |<span data-ttu-id="c5497-372">NoRestart</span><span class="sxs-lookup"><span data-stu-id="c5497-372">NoRestart</span></span>|<span data-ttu-id="c5497-373">/norestart</span><span class="sxs-lookup"><span data-stu-id="c5497-373">/norestart</span></span>|<span data-ttu-id="c5497-374">否</span><span class="sxs-lookup"><span data-stu-id="c5497-374">No</span></span>|<span data-ttu-id="c5497-375">禁止所有重启尝试。</span><span class="sxs-lookup"><span data-stu-id="c5497-375">Suppresses any attempts to restart.</span></span> <span data-ttu-id="c5497-376">重启前将默认提示 UI。</span><span class="sxs-lookup"><span data-stu-id="c5497-376">By default, the UI will prompt before restart.</span></span>|
> |<span data-ttu-id="c5497-377">Help</span><span class="sxs-lookup"><span data-stu-id="c5497-377">Help</span></span>|<span data-ttu-id="c5497-378">/help</span><span class="sxs-lookup"><span data-stu-id="c5497-378">/help</span></span>|<span data-ttu-id="c5497-379">否</span><span class="sxs-lookup"><span data-stu-id="c5497-379">No</span></span>|<span data-ttu-id="c5497-380">提供帮助和快速引用。</span><span class="sxs-lookup"><span data-stu-id="c5497-380">Provides help and quick reference.</span></span> <span data-ttu-id="c5497-381">显示安装命令的正确使用方法，包括一个显示全部选项和行为的列表。</span><span class="sxs-lookup"><span data-stu-id="c5497-381">Displays the correct use of the setup command, including a list of all options and behaviors.</span></span>|

### <a name="line-breaks-within-words-in-second-column-table-cells"></a><span data-ttu-id="c5497-382">第二列表格单元格中单词内的换行符</span><span class="sxs-lookup"><span data-stu-id="c5497-382">Line breaks within words in second column table cells</span></span>

<span data-ttu-id="c5497-383">你可能只希望换行符自动插入到表格第二列中的单词内。</span><span class="sxs-lookup"><span data-stu-id="c5497-383">You might want line breaks to be automatically inserted within words only in the second column of a table.</span></span> <span data-ttu-id="c5497-384">若要限制在第二列换行，请按前述所示使用 `div` 包装语法来应用类 `mx-tdCol2BreakAll`。</span><span class="sxs-lookup"><span data-stu-id="c5497-384">To limit the breaks to the second column, apply the class `mx-tdCol2BreakAll` by using the `div` wrapper syntax as shown earlier.</span></span>

### <a name="html-tables"></a><span data-ttu-id="c5497-385">HTML 表</span><span class="sxs-lookup"><span data-stu-id="c5497-385">HTML Tables</span></span>

<span data-ttu-id="c5497-386">不建议将 HTML 表用于 docs.microsoft.com。</span><span class="sxs-lookup"><span data-stu-id="c5497-386">HTML tables aren't recommended for docs.microsoft.com.</span></span> <span data-ttu-id="c5497-387">它们在源中无法为人所理解，而这是 Markdown 的关键原则。</span><span class="sxs-lookup"><span data-stu-id="c5497-387">They aren't human readable in the source - which is a key principle of Markdown.</span></span>
