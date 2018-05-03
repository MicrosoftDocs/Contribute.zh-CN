---
title: 如何使用 Markdown 撰写 Docs
description: 本文提供用于撰写 docs.microsoft.com 文章的 Markdown 语言的基础知识和参考信息。
author: bryanla
ms.author: bryanla
manager: mbaldwin
ms.date: 07/13/2017
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.custom: external-contributor-guide
ms.openlocfilehash: 96d00abc052c3b23ca62201dccdbe590a927e72d
ms.sourcegitcommit: de6e6b6ca641fdd5b30eb46deee9ac3a500089ef
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/26/2018
---
# <a name="how-to-use-markdown-for-writing-docs"></a><span data-ttu-id="b9976-103">如何使用 Markdown 撰写 Docs</span><span class="sxs-lookup"><span data-stu-id="b9976-103">How to use Markdown for writing Docs</span></span>

<span data-ttu-id="b9976-104">Docs.microsoft.com 文章均采用一种称为 [Markdown](https://daringfireball.net/projects/markdown/) 的轻量级标记语言编写，这种语言易读且易学。</span><span class="sxs-lookup"><span data-stu-id="b9976-104">Docs.microsoft.com articles are written in a lightweight markup language called [Markdown](https://daringfireball.net/projects/markdown/), which is both easy to read and easy to learn.</span></span> <span data-ttu-id="b9976-105">正因为如此，Markdown 已迅速成为行业标准。</span><span class="sxs-lookup"><span data-stu-id="b9976-105">Because of this, it has quickly become an industry standard.</span></span>

<span data-ttu-id="b9976-106">由于 Doc 内容存储在 GitHub 中，因此可以使用 Markdown 超集（称为 [ GitHub 风格的 Markdown (GFM)](https://help.github.com/categories/writing-on-github/)），它为常用格式需求提供了附加功能。</span><span class="sxs-lookup"><span data-stu-id="b9976-106">Because Docs content is stored in GitHub, it can use a superset of Markdown called [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/), which provides additional functionality for common formatting needs.</span></span> <span data-ttu-id="b9976-107">此外， Open Publishing Services (OPS) 还将实现 DocFX 风格的 Markdown (DFM)。</span><span class="sxs-lookup"><span data-stu-id="b9976-107">Additionally, Open Publishing Services (OPS) implements DocFX Flavored Markdown (DFM).</span></span> <span data-ttu-id="b9976-108">DFM 与 GitHub 风格的 Markdown (GFM) 高度兼容，并添加了实现 Docs 特定功能的功能。</span><span class="sxs-lookup"><span data-stu-id="b9976-108">DFM is highly compatible with GitHub Flavored Markdown (GFM), adding functionality to enable Docs-specific features.</span></span>

## <a name="markdown-basics"></a><span data-ttu-id="b9976-109">Markdown 基础知识</span><span class="sxs-lookup"><span data-stu-id="b9976-109">Markdown basics</span></span>

### <a name="headings"></a><span data-ttu-id="b9976-110">标题</span><span class="sxs-lookup"><span data-stu-id="b9976-110">Headings</span></span>

<span data-ttu-id="b9976-111">要创建标题，请使用井号标记 (#)，如下所示：</span><span class="sxs-lookup"><span data-stu-id="b9976-111">To create a heading, you use a hash mark (#), as follows:</span></span>

```markdown
    # This is heading 1
    ## This is heading 2
    ### This is heading 3
    #### This is heading 4
```

### <a name="bold-and-italic-text"></a><span data-ttu-id="b9976-112">粗体和斜体文本</span><span class="sxs-lookup"><span data-stu-id="b9976-112">Bold and italic text</span></span>

<span data-ttu-id="b9976-113">要将文本设置为粗体格式，请用两个星号括住文本：</span><span class="sxs-lookup"><span data-stu-id="b9976-113">To format text as **bold**, you enclose it in two asterisks:</span></span>

```markdown
    This text is **bold**.
```

<span data-ttu-id="b9976-114">要将文本设置为斜体格式，请用一个星号括住文本：</span><span class="sxs-lookup"><span data-stu-id="b9976-114">To format text as *italic*, you enclose it in a single asterisk:</span></span>

```markdown
    This text is *italic*.
```

<span data-ttu-id="b9976-115">要将文本同时设置为粗体和斜体格式，请用三个星号括住文本：</span><span class="sxs-lookup"><span data-stu-id="b9976-115">To format text as both ***bold and italic***, you enclose it in three asterisks:</span></span>

```markdown
    This is text is both ***bold and italic***.
```

### <a name="lists"></a><span data-ttu-id="b9976-116">列表</span><span class="sxs-lookup"><span data-stu-id="b9976-116">Lists</span></span>

#### <a name="unordered-list"></a><span data-ttu-id="b9976-117">无序列表</span><span class="sxs-lookup"><span data-stu-id="b9976-117">Unordered list</span></span>

<span data-ttu-id="b9976-118">要为无序列表/项目符号列表设置格式，可以使用星号或短划线。</span><span class="sxs-lookup"><span data-stu-id="b9976-118">To format an unordered/bulleted list, you can use either asterisks or dashes.</span></span> <span data-ttu-id="b9976-119">例如，以下 Markdown：</span><span class="sxs-lookup"><span data-stu-id="b9976-119">For example, the following Markdown:</span></span>

```markdown
- List item 1
- List item 2
- List item 3
```

<span data-ttu-id="b9976-120">将显示为：</span><span class="sxs-lookup"><span data-stu-id="b9976-120">will be rendered as:</span></span>

- <span data-ttu-id="b9976-121">列表项目 1</span><span class="sxs-lookup"><span data-stu-id="b9976-121">List item 1</span></span>
- <span data-ttu-id="b9976-122">列表项目 2</span><span class="sxs-lookup"><span data-stu-id="b9976-122">List item 2</span></span>
- <span data-ttu-id="b9976-123">列表项目 3</span><span class="sxs-lookup"><span data-stu-id="b9976-123">List item 3</span></span>

<span data-ttu-id="b9976-124">要将一个列表嵌套在另一个列表中，请缩进子列表项。</span><span class="sxs-lookup"><span data-stu-id="b9976-124">To nest a list within another list, indent the child list items.</span></span> <span data-ttu-id="b9976-125">例如，以下 Markdown：</span><span class="sxs-lookup"><span data-stu-id="b9976-125">For example, the following Markdown:</span></span>

```markdown
- List item 1
  - List item A
  - List item B
- List item 2
```

<span data-ttu-id="b9976-126">将显示为：</span><span class="sxs-lookup"><span data-stu-id="b9976-126">will be rendered as:</span></span>

- <span data-ttu-id="b9976-127">列表项目 1</span><span class="sxs-lookup"><span data-stu-id="b9976-127">List item 1</span></span>
  - <span data-ttu-id="b9976-128">列表项目 A</span><span class="sxs-lookup"><span data-stu-id="b9976-128">List item A</span></span>
  - <span data-ttu-id="b9976-129">列表项目 B</span><span class="sxs-lookup"><span data-stu-id="b9976-129">List item B</span></span>
- <span data-ttu-id="b9976-130">列表项目 2</span><span class="sxs-lookup"><span data-stu-id="b9976-130">List item 2</span></span>

#### <a name="ordered-list"></a><span data-ttu-id="b9976-131">有序列表</span><span class="sxs-lookup"><span data-stu-id="b9976-131">Ordered list</span></span>

<span data-ttu-id="b9976-132">要设置有序/分阶段列表的格式，可以使用相应的编号。</span><span class="sxs-lookup"><span data-stu-id="b9976-132">To format an ordered/stepwise list, you use corresponding numbers.</span></span> <span data-ttu-id="b9976-133">例如，以下 Markdown：</span><span class="sxs-lookup"><span data-stu-id="b9976-133">For example, the following Markdown:</span></span>

```markdown
1. First instruction
2. Second instruction
3. Third instruction
```

<span data-ttu-id="b9976-134">将显示为：</span><span class="sxs-lookup"><span data-stu-id="b9976-134">will be rendered as:</span></span>

1. <span data-ttu-id="b9976-135">第一个说明</span><span class="sxs-lookup"><span data-stu-id="b9976-135">First instruction</span></span>
2. <span data-ttu-id="b9976-136">第二个说明</span><span class="sxs-lookup"><span data-stu-id="b9976-136">Second instruction</span></span>
3. <span data-ttu-id="b9976-137">第三个说明</span><span class="sxs-lookup"><span data-stu-id="b9976-137">Third instruction</span></span>

<span data-ttu-id="b9976-138">要将一个列表嵌套在另一个列表中，请缩进子列表项。</span><span class="sxs-lookup"><span data-stu-id="b9976-138">To nest a list within another list, indent the child list items.</span></span> <span data-ttu-id="b9976-139">例如，以下 Markdown：</span><span class="sxs-lookup"><span data-stu-id="b9976-139">For example, the following Markdown:</span></span>

```markdown
1. First instruction
    1. Sub-instruction
    2. Sub-instruction
2. Second instruction
```

<span data-ttu-id="b9976-140">将显示为：</span><span class="sxs-lookup"><span data-stu-id="b9976-140">will be rendered as:</span></span>

1. <span data-ttu-id="b9976-141">第一个说明</span><span class="sxs-lookup"><span data-stu-id="b9976-141">First instruction</span></span>
    1. <span data-ttu-id="b9976-142">辅助说明</span><span class="sxs-lookup"><span data-stu-id="b9976-142">Sub-instruction</span></span>
    2. <span data-ttu-id="b9976-143">辅助说明</span><span class="sxs-lookup"><span data-stu-id="b9976-143">Sub-instruction</span></span>
2. <span data-ttu-id="b9976-144">第二个说明</span><span class="sxs-lookup"><span data-stu-id="b9976-144">Second instruction</span></span>

### <a name="tables"></a><span data-ttu-id="b9976-145">表格</span><span class="sxs-lookup"><span data-stu-id="b9976-145">Tables</span></span>

<span data-ttu-id="b9976-146">表格不属于核心 Markdown 规范，但是它们受 GFM 支持。</span><span class="sxs-lookup"><span data-stu-id="b9976-146">Tables are not part of the core Markdown specification, but GFM supports them.</span></span> <span data-ttu-id="b9976-147">可以使用竖线 (|) 和连字符 (-) 字符创建表格。</span><span class="sxs-lookup"><span data-stu-id="b9976-147">You can create tables by using the pipe (|) and hyphen (-) characters.</span></span> <span data-ttu-id="b9976-148">连字符用于创建每列的标题，而竖线用于分隔每列。</span><span class="sxs-lookup"><span data-stu-id="b9976-148">Hyphens create each column's header, while pipes separate each column.</span></span> <span data-ttu-id="b9976-149">请在表格前面加入一个空行，使它能够正确显示。</span><span class="sxs-lookup"><span data-stu-id="b9976-149">Include a blank line before your table so it's rendered correctly.</span></span>

<span data-ttu-id="b9976-150">例如，以下 Markdown：</span><span class="sxs-lookup"><span data-stu-id="b9976-150">For example, the following Markdown:</span></span>

```markdown
| Fun                  | With                 | Tables          |
| :------------------- | -------------------: |:---------------:|
| left-aligned column  | right-aligned column | centered column |
| $100                 | $100                 | $100            |
| $10                  | $10                  | $10             |
| $1                   | $1                   | $1              |
```

<span data-ttu-id="b9976-151">将显示为：</span><span class="sxs-lookup"><span data-stu-id="b9976-151">will be rendered as:</span></span>

| <span data-ttu-id="b9976-152">趣</span><span class="sxs-lookup"><span data-stu-id="b9976-152">Fun</span></span>                  | <span data-ttu-id="b9976-153">含</span><span class="sxs-lookup"><span data-stu-id="b9976-153">With</span></span>                 | <span data-ttu-id="b9976-154">表格</span><span class="sxs-lookup"><span data-stu-id="b9976-154">Tables</span></span>          |
| :------------------- | -------------------: |:---------------:|
| <span data-ttu-id="b9976-155">左对齐列</span><span class="sxs-lookup"><span data-stu-id="b9976-155">left-aligned column</span></span>  | <span data-ttu-id="b9976-156">右对齐列</span><span class="sxs-lookup"><span data-stu-id="b9976-156">right-aligned column</span></span> | <span data-ttu-id="b9976-157">居中列</span><span class="sxs-lookup"><span data-stu-id="b9976-157">centered column</span></span> |
| <span data-ttu-id="b9976-158">$100</span><span class="sxs-lookup"><span data-stu-id="b9976-158">$100</span></span>                 | <span data-ttu-id="b9976-159">$100</span><span class="sxs-lookup"><span data-stu-id="b9976-159">$100</span></span>                 | <span data-ttu-id="b9976-160">$100</span><span class="sxs-lookup"><span data-stu-id="b9976-160">$100</span></span>            |
| <span data-ttu-id="b9976-161">$10</span><span class="sxs-lookup"><span data-stu-id="b9976-161">$10</span></span>                  | <span data-ttu-id="b9976-162">$10</span><span class="sxs-lookup"><span data-stu-id="b9976-162">$10</span></span>                  | <span data-ttu-id="b9976-163">$10</span><span class="sxs-lookup"><span data-stu-id="b9976-163">$10</span></span>             |
| <span data-ttu-id="b9976-164">$1</span><span class="sxs-lookup"><span data-stu-id="b9976-164">$1</span></span>                   | <span data-ttu-id="b9976-165">$1</span><span class="sxs-lookup"><span data-stu-id="b9976-165">$1</span></span>                   | <span data-ttu-id="b9976-166">$1</span><span class="sxs-lookup"><span data-stu-id="b9976-166">$1</span></span>              |

<span data-ttu-id="b9976-167">有关创建表格的详细信息，请参阅：</span><span class="sxs-lookup"><span data-stu-id="b9976-167">For more information on creating tables, see:</span></span>

- <span data-ttu-id="b9976-168">DFM [表格换行功能](#table-wrapping)，有助于设置宽表格的格式</span><span class="sxs-lookup"><span data-stu-id="b9976-168">The DFM [table wrapping feature](#table-wrapping), which can help with formatting of wide tables</span></span>
- <span data-ttu-id="b9976-169">GitHub 的[使用表格整理信息](https://help.github.com/articles/organizing-information-with-tables/)</span><span class="sxs-lookup"><span data-stu-id="b9976-169">GitHub's [Organizing information with tables](https://help.github.com/articles/organizing-information-with-tables/)</span></span>
- <span data-ttu-id="b9976-170">[Markdown 表格生成器](https://www.tablesgenerator.com/markdown_tables) Web 应用</span><span class="sxs-lookup"><span data-stu-id="b9976-170">The [Markdown Tables Generator](https://www.tablesgenerator.com/markdown_tables) web app</span></span>
- [<span data-ttu-id="b9976-171">Adam Pritchard 的 Markdown 备忘单</span><span class="sxs-lookup"><span data-stu-id="b9976-171">Adam Pritchard's Markdown Cheatsheet</span></span>](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#wiki-tables)
- [<span data-ttu-id="b9976-172">Michel Fortin 的 Markdown Extra</span><span class="sxs-lookup"><span data-stu-id="b9976-172">Michel Fortin's Markdown Extra</span></span>](https://michelf.ca/projects/php-markdown/extra/#table)
- [<span data-ttu-id="b9976-173">将 HTML 表转换为 Markdown 格式</span><span class="sxs-lookup"><span data-stu-id="b9976-173">Convert HTML tables to Markdown</span></span>](https://jmalarcon.github.io/markdowntables/)

### <a name="links"></a><span data-ttu-id="b9976-174">链接</span><span class="sxs-lookup"><span data-stu-id="b9976-174">Links</span></span>

<span data-ttu-id="b9976-175">Markdown 的内联链接语法由两部分组成：`[link text]` 部分，这是要创建为超链接的文本；后跟 `(file-name.md)` 部分，这是要链接到的 URL 或者文件名：</span><span class="sxs-lookup"><span data-stu-id="b9976-175">The Markdown syntax for an inline link consists of the `[link text]` portion, which is the text that will be hyperlinked, followed by the `(file-name.md)` portion, which is the URL or file name that's being linked to:</span></span>

 `[link text](file-name.md)`

<span data-ttu-id="b9976-176">有关链接的详细信息，请参阅：</span><span class="sxs-lookup"><span data-stu-id="b9976-176">For more information on linking, see:</span></span>

- <span data-ttu-id="b9976-177">[Markdown 语法指南](https://daringfireball.net/projects/markdown/syntax#link)，详细了解 Markdown 的基本链接支持相关信息。</span><span class="sxs-lookup"><span data-stu-id="b9976-177">The [Markdown syntax guide](https://daringfireball.net/projects/markdown/syntax#link) for details on Markdown's base linking support.</span></span>
- <span data-ttu-id="b9976-178">本指南的[链接](how-to-write-links.md)部分，了解 DFM 提供的其他链接语法的详细信息。</span><span class="sxs-lookup"><span data-stu-id="b9976-178">The [Links](how-to-write-links.md) section of this guide for details on additional linking syntax that DFM provides.</span></span>

### <a name="code-snippets"></a><span data-ttu-id="b9976-179">代码片段</span><span class="sxs-lookup"><span data-stu-id="b9976-179">Code snippets</span></span>

<span data-ttu-id="b9976-180">Markdown 不仅支持将代码片段内联在某个句子中，还支持将它作为单独的“隔离”块放置在两个句子之间。</span><span class="sxs-lookup"><span data-stu-id="b9976-180">Markdown supports the placement of code snippets both inline in a sentence and as a separate "fenced" block between sentences.</span></span> <span data-ttu-id="b9976-181">有关详细信息，请参阅：</span><span class="sxs-lookup"><span data-stu-id="b9976-181">For details, see:</span></span>

- [<span data-ttu-id="b9976-182">Markdown 代码块本机支持</span><span class="sxs-lookup"><span data-stu-id="b9976-182">Markdown's native support for code blocks</span></span>](https://daringfireball.net/projects/markdown/syntax#precode)
- [<span data-ttu-id="b9976-183">针对代码隔离和语法高亮显示的 GFM 支持</span><span class="sxs-lookup"><span data-stu-id="b9976-183">GFM support for code fencing and syntax highlighting</span></span>](https://help.github.com/articles/creating-and-highlighting-code-blocks/)

<span data-ttu-id="b9976-184">借助隔离代码块，可以轻松实现代码片段的语法高亮显示。</span><span class="sxs-lookup"><span data-stu-id="b9976-184">Fenced code blocks are an easy way to enable syntax highlighting for your code snippets.</span></span> <span data-ttu-id="b9976-185">隔离代码块的一般格式为：</span><span class="sxs-lookup"><span data-stu-id="b9976-185">The general format for fenced code blocks is:</span></span>

    ```alias
    ...
    your code goes in here
    ...
    ```

<span data-ttu-id="b9976-186">开头的三个撇号 (\`) 字符后面的别名定义要使用的语法高亮显示。</span><span class="sxs-lookup"><span data-stu-id="b9976-186">The alias after the initial three backtick (\`) characters defines the syntax highlighting to be used.</span></span> <span data-ttu-id="b9976-187">下面列出了 Docs 内容中常用的编程语言以及匹配的标签：</span><span class="sxs-lookup"><span data-stu-id="b9976-187">The following is a list of commonly used programming languages in Docs content and the matching label:</span></span>

<span data-ttu-id="b9976-188">这些语言支持友好名称并且大多数都可以突出显示语言。</span><span class="sxs-lookup"><span data-stu-id="b9976-188">These languages have friendly name support and most have language highlighting.</span></span>

|<span data-ttu-id="b9976-189">名称</span><span class="sxs-lookup"><span data-stu-id="b9976-189">Name</span></span>|<span data-ttu-id="b9976-190">Markdown 标签</span><span class="sxs-lookup"><span data-stu-id="b9976-190">Markdown Label</span></span>|
|-----|-------|
|<span data-ttu-id="b9976-191">.NET 控制台</span><span class="sxs-lookup"><span data-stu-id="b9976-191">.NET Console</span></span>|<span data-ttu-id="b9976-192">dotnetcli</span><span class="sxs-lookup"><span data-stu-id="b9976-192">dotnetcli</span></span>|
|<span data-ttu-id="b9976-193">ASP.NET (C#)</span><span class="sxs-lookup"><span data-stu-id="b9976-193">ASP.NET (C#)</span></span>|<span data-ttu-id="b9976-194">aspx-csharp</span><span class="sxs-lookup"><span data-stu-id="b9976-194">aspx-csharp</span></span>|
|<span data-ttu-id="b9976-195">ASP.NET (VB)</span><span class="sxs-lookup"><span data-stu-id="b9976-195">ASP.NET (VB)</span></span>|<span data-ttu-id="b9976-196">aspx-vb</span><span class="sxs-lookup"><span data-stu-id="b9976-196">aspx-vb</span></span>|
|<span data-ttu-id="b9976-197">AzCopy</span><span class="sxs-lookup"><span data-stu-id="b9976-197">AzCopy</span></span>|<span data-ttu-id="b9976-198">azcopy</span><span class="sxs-lookup"><span data-stu-id="b9976-198">azcopy</span></span>|
|<span data-ttu-id="b9976-199">Azure CLI</span><span class="sxs-lookup"><span data-stu-id="b9976-199">Azure CLI</span></span>|<span data-ttu-id="b9976-200">azurecli</span><span class="sxs-lookup"><span data-stu-id="b9976-200">azurecli</span></span>|
|<span data-ttu-id="b9976-201">Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="b9976-201">Azure PowerShell</span></span>|<span data-ttu-id="b9976-202">azurepowershell</span><span class="sxs-lookup"><span data-stu-id="b9976-202">azurepowershell</span></span>|
|<span data-ttu-id="b9976-203">C++</span><span class="sxs-lookup"><span data-stu-id="b9976-203">C++</span></span>|<span data-ttu-id="b9976-204">cpp</span><span class="sxs-lookup"><span data-stu-id="b9976-204">cpp</span></span>|
|<span data-ttu-id="b9976-205">C++/CX</span><span class="sxs-lookup"><span data-stu-id="b9976-205">C++/CX</span></span>|<span data-ttu-id="b9976-206">cppcx</span><span class="sxs-lookup"><span data-stu-id="b9976-206">cppcx</span></span>|
|<span data-ttu-id="b9976-207">C++/WinRT</span><span class="sxs-lookup"><span data-stu-id="b9976-207">C++/WinRT</span></span>|<span data-ttu-id="b9976-208">cppwinrt</span><span class="sxs-lookup"><span data-stu-id="b9976-208">cppwinrt</span></span>|
|<span data-ttu-id="b9976-209">C#</span><span class="sxs-lookup"><span data-stu-id="b9976-209">C#</span></span>|<span data-ttu-id="b9976-210">csharp</span><span class="sxs-lookup"><span data-stu-id="b9976-210">csharp</span></span>|
|<span data-ttu-id="b9976-211">CSHTML</span><span class="sxs-lookup"><span data-stu-id="b9976-211">CSHTML</span></span>|<span data-ttu-id="b9976-212">cshtml</span><span class="sxs-lookup"><span data-stu-id="b9976-212">cshtml</span></span>|
|<span data-ttu-id="b9976-213">DAX</span><span class="sxs-lookup"><span data-stu-id="b9976-213">DAX</span></span>|<span data-ttu-id="b9976-214">dax</span><span class="sxs-lookup"><span data-stu-id="b9976-214">dax</span></span>|
|<span data-ttu-id="b9976-215">F#</span><span class="sxs-lookup"><span data-stu-id="b9976-215">F#</span></span>|<span data-ttu-id="b9976-216">fsharp</span><span class="sxs-lookup"><span data-stu-id="b9976-216">fsharp</span></span>|
|<span data-ttu-id="b9976-217">Go</span><span class="sxs-lookup"><span data-stu-id="b9976-217">Go</span></span>|<span data-ttu-id="b9976-218">go</span><span class="sxs-lookup"><span data-stu-id="b9976-218">go</span></span>|
|<span data-ttu-id="b9976-219">HTML</span><span class="sxs-lookup"><span data-stu-id="b9976-219">HTML</span></span>|<span data-ttu-id="b9976-220">html</span><span class="sxs-lookup"><span data-stu-id="b9976-220">html</span></span>|
|<span data-ttu-id="b9976-221">HTTP</span><span class="sxs-lookup"><span data-stu-id="b9976-221">HTTP</span></span>|<span data-ttu-id="b9976-222">http</span><span class="sxs-lookup"><span data-stu-id="b9976-222">http</span></span>|
|<span data-ttu-id="b9976-223">Java</span><span class="sxs-lookup"><span data-stu-id="b9976-223">Java</span></span>|<span data-ttu-id="b9976-224">java</span><span class="sxs-lookup"><span data-stu-id="b9976-224">java</span></span>|
|<span data-ttu-id="b9976-225">JavaScript</span><span class="sxs-lookup"><span data-stu-id="b9976-225">JavaScript</span></span>|<span data-ttu-id="b9976-226">javascript</span><span class="sxs-lookup"><span data-stu-id="b9976-226">javascript</span></span>|
|<span data-ttu-id="b9976-227">JSON</span><span class="sxs-lookup"><span data-stu-id="b9976-227">JSON</span></span>|<span data-ttu-id="b9976-228">json</span><span class="sxs-lookup"><span data-stu-id="b9976-228">json</span></span>|
|<span data-ttu-id="b9976-229">Markdown</span><span class="sxs-lookup"><span data-stu-id="b9976-229">Markdown</span></span>|<span data-ttu-id="b9976-230">md</span><span class="sxs-lookup"><span data-stu-id="b9976-230">md</span></span>|
|<span data-ttu-id="b9976-231">NodeJS</span><span class="sxs-lookup"><span data-stu-id="b9976-231">NodeJS</span></span>|<span data-ttu-id="b9976-232">nodejs</span><span class="sxs-lookup"><span data-stu-id="b9976-232">nodejs</span></span>|
|<span data-ttu-id="b9976-233">Objective-C</span><span class="sxs-lookup"><span data-stu-id="b9976-233">Objective-C</span></span>|<span data-ttu-id="b9976-234">objc</span><span class="sxs-lookup"><span data-stu-id="b9976-234">objc</span></span>|
|<span data-ttu-id="b9976-235">OData</span><span class="sxs-lookup"><span data-stu-id="b9976-235">OData</span></span>|<span data-ttu-id="b9976-236">odata</span><span class="sxs-lookup"><span data-stu-id="b9976-236">odata</span></span>|
|<span data-ttu-id="b9976-237">PHP</span><span class="sxs-lookup"><span data-stu-id="b9976-237">PHP</span></span>|<span data-ttu-id="b9976-238">php</span><span class="sxs-lookup"><span data-stu-id="b9976-238">php</span></span>|
|<span data-ttu-id="b9976-239">Power Apps Formula</span><span class="sxs-lookup"><span data-stu-id="b9976-239">Power Apps Formula</span></span>|<span data-ttu-id="b9976-240">powerappsfl</span><span class="sxs-lookup"><span data-stu-id="b9976-240">powerappsfl</span></span>|
|<span data-ttu-id="b9976-241">PowerShell</span><span class="sxs-lookup"><span data-stu-id="b9976-241">PowerShell</span></span>|<span data-ttu-id="b9976-242">powershell</span><span class="sxs-lookup"><span data-stu-id="b9976-242">powershell</span></span>|
|<span data-ttu-id="b9976-243">Python</span><span class="sxs-lookup"><span data-stu-id="b9976-243">Python</span></span>|<span data-ttu-id="b9976-244">python</span><span class="sxs-lookup"><span data-stu-id="b9976-244">python</span></span>|
|<span data-ttu-id="b9976-245">Q#</span><span class="sxs-lookup"><span data-stu-id="b9976-245">Q#</span></span>|<span data-ttu-id="b9976-246">qsharp</span><span class="sxs-lookup"><span data-stu-id="b9976-246">qsharp</span></span>|
|<span data-ttu-id="b9976-247">Ruby</span><span class="sxs-lookup"><span data-stu-id="b9976-247">Ruby</span></span>|<span data-ttu-id="b9976-248">ruby</span><span class="sxs-lookup"><span data-stu-id="b9976-248">ruby</span></span>|
|<span data-ttu-id="b9976-249">SQL</span><span class="sxs-lookup"><span data-stu-id="b9976-249">SQL</span></span>|<span data-ttu-id="b9976-250">sql</span><span class="sxs-lookup"><span data-stu-id="b9976-250">sql</span></span>|
|<span data-ttu-id="b9976-251">Swift</span><span class="sxs-lookup"><span data-stu-id="b9976-251">Swift</span></span>|<span data-ttu-id="b9976-252">swift</span><span class="sxs-lookup"><span data-stu-id="b9976-252">swift</span></span>|
|<span data-ttu-id="b9976-253">TypeScript</span><span class="sxs-lookup"><span data-stu-id="b9976-253">TypeScript</span></span>|<span data-ttu-id="b9976-254">typescript</span><span class="sxs-lookup"><span data-stu-id="b9976-254">typescript</span></span>|
|<span data-ttu-id="b9976-255">VB</span><span class="sxs-lookup"><span data-stu-id="b9976-255">VB</span></span>|<span data-ttu-id="b9976-256">vb</span><span class="sxs-lookup"><span data-stu-id="b9976-256">vb</span></span>|
|<span data-ttu-id="b9976-257">VSTS CLI</span><span class="sxs-lookup"><span data-stu-id="b9976-257">VSTS CLI</span></span>|<span data-ttu-id="b9976-258">vstscli</span><span class="sxs-lookup"><span data-stu-id="b9976-258">vstscli</span></span>|
|<span data-ttu-id="b9976-259">XAML</span><span class="sxs-lookup"><span data-stu-id="b9976-259">XAML</span></span>|<span data-ttu-id="b9976-260">xaml</span><span class="sxs-lookup"><span data-stu-id="b9976-260">xaml</span></span>|
|<span data-ttu-id="b9976-261">XML</span><span class="sxs-lookup"><span data-stu-id="b9976-261">XML</span></span>|<span data-ttu-id="b9976-262">xml</span><span class="sxs-lookup"><span data-stu-id="b9976-262">xml</span></span>|

#### <a name="example-c"></a><span data-ttu-id="b9976-263">示例：C\#</span><span class="sxs-lookup"><span data-stu-id="b9976-263">Example: C\#</span></span>

<span data-ttu-id="b9976-264">__Markdown__</span><span class="sxs-lookup"><span data-stu-id="b9976-264">__Markdown__</span></span>

    ```csharp
    // Hello1.cs
    public class Hello1
    {
        public static void Main()
        {
            System.Console.WriteLine("Hello, World!");
        }
    }
    ```

<span data-ttu-id="b9976-265">__呈现__</span><span class="sxs-lookup"><span data-stu-id="b9976-265">__Render__</span></span>

```csharp
// Hello1.cs
public class Hello1
{
    public static void Main()
    {
        System.Console.WriteLine("Hello, World!");
    }
}
```

#### <a name="example-sql"></a><span data-ttu-id="b9976-266">示例：SQL</span><span class="sxs-lookup"><span data-stu-id="b9976-266">Example: SQL</span></span>

<span data-ttu-id="b9976-267">__Markdown__</span><span class="sxs-lookup"><span data-stu-id="b9976-267">__Markdown__</span></span>

    ```sql
    CREATE TABLE T1 (
      c1 int PRIMARY KEY,
      c2 varchar(50) SPARSE NULL
    );
    ```

<span data-ttu-id="b9976-268">__呈现__</span><span class="sxs-lookup"><span data-stu-id="b9976-268">__Render__</span></span>

```sql
CREATE TABLE T1 (
  c1 int PRIMARY KEY,
  c2 varchar(50) SPARSE NULL
);
```

## <a name="ops-custom-markdown-extensions"></a><span data-ttu-id="b9976-269">OPS 自定义 Markdown 扩展</span><span class="sxs-lookup"><span data-stu-id="b9976-269">OPS custom Markdown extensions</span></span>

> [!NOTE]
> <span data-ttu-id="b9976-270">Open Publishing Services(OPS) 可实现 DocFX 风格的 Markdown (DFM)，它与 GitHub 风格的 Markdown (GFM) 高度兼容。</span><span class="sxs-lookup"><span data-stu-id="b9976-270">Open Publishing Services (OPS) implements DocFX Flavored Markdown (DFM), which is highly compatible with GitHub Flavored Markdown (GFM).</span></span> <span data-ttu-id="b9976-271">DFM 通过 Markdown 扩展添加一些功能。</span><span class="sxs-lookup"><span data-stu-id="b9976-271">DFM adds some functionality through Markdown extensions.</span></span> <span data-ttu-id="b9976-272">就这一点而言，本指南从完整的《OPS 创作指南》中选用了几篇文章，以供参考。</span><span class="sxs-lookup"><span data-stu-id="b9976-272">As such, selected articles from the full OPS Authoring Guide are included in this guide for reference.</span></span> <span data-ttu-id="b9976-273">（例如，请参阅目录中的“DFM 和 Markdown 扩展”以及“代码片段”。）</span><span class="sxs-lookup"><span data-stu-id="b9976-273">(For example, see "DFM and Markdown extensions" and "Code snippets" in the table of contents.)</span></span>

<span data-ttu-id="b9976-274">Doc 文章使用 GFM 完成大多文章的格式设置，如段落、链接、列表和标题。</span><span class="sxs-lookup"><span data-stu-id="b9976-274">Docs articles use GFM for most article formatting, such as paragraphs, links, lists, and headings.</span></span> <span data-ttu-id="b9976-275">要想实现更丰富的格式设置功能，文章可以使用 DFM 功能，例如：</span><span class="sxs-lookup"><span data-stu-id="b9976-275">For richer formatting, articles can use DFM features such as:</span></span>

- <span data-ttu-id="b9976-276">备注块</span><span class="sxs-lookup"><span data-stu-id="b9976-276">Note blocks</span></span>
- <span data-ttu-id="b9976-277">包含文件</span><span class="sxs-lookup"><span data-stu-id="b9976-277">Includes</span></span>
- <span data-ttu-id="b9976-278">选择器</span><span class="sxs-lookup"><span data-stu-id="b9976-278">Selectors</span></span>
- <span data-ttu-id="b9976-279">嵌入视频</span><span class="sxs-lookup"><span data-stu-id="b9976-279">Embedded videos</span></span>
- <span data-ttu-id="b9976-280">代码片段/示例</span><span class="sxs-lookup"><span data-stu-id="b9976-280">Code snippets/samples</span></span>

<span data-ttu-id="b9976-281">如需完整列表，请参阅目录中的“DFM 和 Markdown 扩展”以及“代码片段”。</span><span class="sxs-lookup"><span data-stu-id="b9976-281">For the complete list, refer to "DFM and Markdown extensions" and "Code snippets" in the table of contents.</span></span>

### <a name="note-blocks"></a><span data-ttu-id="b9976-282">备注块</span><span class="sxs-lookup"><span data-stu-id="b9976-282">Note blocks</span></span>

<span data-ttu-id="b9976-283">可以从 4 种类型的备注块中进行选择来吸引对特定内容的注意：</span><span class="sxs-lookup"><span data-stu-id="b9976-283">You can choose from four types of note blocks to draw attention to specific content:</span></span>

- <span data-ttu-id="b9976-284">注意</span><span class="sxs-lookup"><span data-stu-id="b9976-284">NOTE</span></span>
- <span data-ttu-id="b9976-285">警告</span><span class="sxs-lookup"><span data-stu-id="b9976-285">WARNING</span></span>
- <span data-ttu-id="b9976-286">提示</span><span class="sxs-lookup"><span data-stu-id="b9976-286">TIP</span></span>
- <span data-ttu-id="b9976-287">重要说明</span><span class="sxs-lookup"><span data-stu-id="b9976-287">IMPORTANT</span></span>

<span data-ttu-id="b9976-288">总之，应谨慎使用备注块，因为它们可能会造成干扰。</span><span class="sxs-lookup"><span data-stu-id="b9976-288">In general, note blocks should be used sparingly because they can be disruptive.</span></span> <span data-ttu-id="b9976-289">尽管备注块也支持代码块、图像、列表以及链接，但最好尽量保持备注块简单明了。</span><span class="sxs-lookup"><span data-stu-id="b9976-289">Although they also support code blocks, images, lists, and links, try to keep your note blocks simple and straightforward.</span></span>

### <a name="includes"></a><span data-ttu-id="b9976-290">包含文件</span><span class="sxs-lookup"><span data-stu-id="b9976-290">Includes</span></span>

<span data-ttu-id="b9976-291">如果有需要加入文章文件中的可重用的文本或图像文件，可以通过 DFM 文件的包含文件功能使用对“包含”文件的引用。</span><span class="sxs-lookup"><span data-stu-id="b9976-291">When you have reusable text or image files that need to be included in article files, you can use a reference to the "include" file via the DFM file include feature.</span></span> <span data-ttu-id="b9976-292">此功能指示 OPS 在创建时将该文件加入文章文件中，使它成为已发布文章的一部分。</span><span class="sxs-lookup"><span data-stu-id="b9976-292">This feature instructs OPS to include the file in your article file at build time, making it part of your published article.</span></span> <span data-ttu-id="b9976-293">有 3 种类型的包含功能可帮助你重用内容：</span><span class="sxs-lookup"><span data-stu-id="b9976-293">Three types of includes are available to help you reuse content:</span></span>

- <span data-ttu-id="b9976-294">内联：重用内联在其他句子中的常用文本片段。</span><span class="sxs-lookup"><span data-stu-id="b9976-294">Inline: Reuse a common text snippet inline with within another sentence.</span></span>
- <span data-ttu-id="b9976-295">块：将整个 Markdown 文件作为一个块来重用，嵌套在文章的某一部分中。</span><span class="sxs-lookup"><span data-stu-id="b9976-295">Block: Reuse an entire Markdown file as a block, nested within a section of an article.</span></span>
- <span data-ttu-id="b9976-296">图像：此方法可以在 Doc 中实现标准图像加入。</span><span class="sxs-lookup"><span data-stu-id="b9976-296">Image: This is how standard image inclusion is implemented in Docs.</span></span>

<span data-ttu-id="b9976-297">“内联”和“块”包含文件是简单的 Markdown (.md) 文件。</span><span class="sxs-lookup"><span data-stu-id="b9976-297">An inline or block include is just a simple Markdown (.md) file.</span></span> <span data-ttu-id="b9976-298">它可以包含任何有效的 Markdown。</span><span class="sxs-lookup"><span data-stu-id="b9976-298">It can contain any valid Markdown.</span></span> <span data-ttu-id="b9976-299">所有包含 Markdown 文件都应置于存储库根目录的[常用 `/includes` 子目录](git-github-fundamentals.md#includes-subdirectory) 中。</span><span class="sxs-lookup"><span data-stu-id="b9976-299">All include Markdown files should be placed in a [common `/includes` subdirectory](git-github-fundamentals.md#includes-subdirectory), in the root of the repository.</span></span> <span data-ttu-id="b9976-300">发布文章时，加入的文件会无缝集成到其中。</span><span class="sxs-lookup"><span data-stu-id="b9976-300">When the article is published, the included file is seamlessly integrated into it.</span></span>

<span data-ttu-id="b9976-301">包含文件的要求和注意事项如下：</span><span class="sxs-lookup"><span data-stu-id="b9976-301">Here are requirements and considerations for includes:</span></span>

- <span data-ttu-id="b9976-302">无论何时需要使相同的文本显示在多篇文章中，均可使用包含功能。</span><span class="sxs-lookup"><span data-stu-id="b9976-302">Use includes whenever you need the same text to appear in multiple articles.</span></span>
- <span data-ttu-id="b9976-303">块包含文件用于大篇幅内容，比如一个或者两个段落、共享过程或者共享章节。</span><span class="sxs-lookup"><span data-stu-id="b9976-303">Use block includes for significant amounts of content--a paragraph or two, a shared procedure, or a shared section.</span></span> <span data-ttu-id="b9976-304">请勿将它们用于小于一个句子的内容。</span><span class="sxs-lookup"><span data-stu-id="b9976-304">Do not use them for anything smaller than a sentence.</span></span>
- <span data-ttu-id="b9976-305">包含文件不会在你文章的 GitHub 渲染视图中显示，因为它们依赖于 DFM 扩展。</span><span class="sxs-lookup"><span data-stu-id="b9976-305">Includes won't be rendered in the GitHub rendered view of your article, because they rely on DFM extensions.</span></span> <span data-ttu-id="b9976-306">它们在发布后才会显示。</span><span class="sxs-lookup"><span data-stu-id="b9976-306">They'll be rendered only after publication.</span></span>
- <span data-ttu-id="b9976-307">确保包含文件中的所有文本都是完整的句子或者段落，并且与引用包含文件的文章的前后文没有关联。</span><span class="sxs-lookup"><span data-stu-id="b9976-307">Ensure that all the text in an include is written in complete sentences or phrases that do not depend on preceding text or following text in the article that references the include.</span></span> <span data-ttu-id="b9976-308">如果不遵循此指导原则，则会在文章中创建无法转换的字符串，进而破坏本地化体验。</span><span class="sxs-lookup"><span data-stu-id="b9976-308">Ignoring this guidance creates an untranslatable string in the article that breaks the localized experience.</span></span>
- <span data-ttu-id="b9976-309">请勿将包含文件嵌入其他包含文件中。</span><span class="sxs-lookup"><span data-stu-id="b9976-309">Don't embed includes within other includes.</span></span> <span data-ttu-id="b9976-310">不支持此操作。</span><span class="sxs-lookup"><span data-stu-id="b9976-310">They are not supported.</span></span>
- <span data-ttu-id="b9976-311">将媒体文件置于特定于包含文件子目录的媒体文件夹中，例如，`<repo>`/includes/媒体文件夹。</span><span class="sxs-lookup"><span data-stu-id="b9976-311">Place media files in a media folder that's specific to the include subdirectory--for instance, the `<repo>`/includes/media folder.</span></span> <span data-ttu-id="b9976-312">媒体目录不应在根目录中包含任何图片。</span><span class="sxs-lookup"><span data-stu-id="b9976-312">The media directory should not contain any images in its root.</span></span> <span data-ttu-id="b9976-313">如果包含文件不包含图像，则不需要相应的媒体目录。</span><span class="sxs-lookup"><span data-stu-id="b9976-313">If the include does not have images, a corresponding media directory is not required.</span></span>
- <span data-ttu-id="b9976-314">对于常规文章，请勿在各包含文件之间共享媒体。</span><span class="sxs-lookup"><span data-stu-id="b9976-314">As with regular articles, don't share media between include files.</span></span> <span data-ttu-id="b9976-315">对于每个包含文件和文章，请使用具有唯一名称的单独文件。</span><span class="sxs-lookup"><span data-stu-id="b9976-315">Use a separate file with a unique name for each include and article.</span></span> <span data-ttu-id="b9976-316">将媒体文件存储在与包含文件关联的媒体文件夹中。</span><span class="sxs-lookup"><span data-stu-id="b9976-316">Store the media file in the media folder that's associated with the include.</span></span>
- <span data-ttu-id="b9976-317">请勿将包含文件用作文章的唯一内容。</span><span class="sxs-lookup"><span data-stu-id="b9976-317">Don't use an include as the only content of an article.</span></span>  <span data-ttu-id="b9976-318">包含文件主要用作文章其余内容的补充内容。</span><span class="sxs-lookup"><span data-stu-id="b9976-318">Includes are meant to be supplemental to the content in the rest of the article.</span></span>

### <a name="selectors"></a><span data-ttu-id="b9976-319">选择器</span><span class="sxs-lookup"><span data-stu-id="b9976-319">Selectors</span></span>

<span data-ttu-id="b9976-320">当你创作具有多种风格的同一篇技术文章时，请在文章中使用选择器，从而跨技术或平台解决实现上的差异。</span><span class="sxs-lookup"><span data-stu-id="b9976-320">Use selectors in technical articles when you author multiple flavors of the same article, to address differences in implementation across technologies or platforms.</span></span> <span data-ttu-id="b9976-321">通常，这最适用于开发人员的移动平台内容。</span><span class="sxs-lookup"><span data-stu-id="b9976-321">This is typically most applicable to our mobile platform content for developers.</span></span> <span data-ttu-id="b9976-322">DFM 中目前有两种类型的选择器，单选择器和多选择器。</span><span class="sxs-lookup"><span data-stu-id="b9976-322">There are currently two different types of selectors in DFM, a single selector and a multi-selector.</span></span>

<span data-ttu-id="b9976-323">由于选择的每篇文章中都会出现相同的选择器 Markdown，因此建议将文章的选择器放在一个包含文件中。</span><span class="sxs-lookup"><span data-stu-id="b9976-323">Because the same selector Markdown goes in each article in the selection, we recommend placing the selector for your article in an include.</span></span> <span data-ttu-id="b9976-324">然后，可以在使用相同选择器的所有文章中引用该包含文件。</span><span class="sxs-lookup"><span data-stu-id="b9976-324">Then you can reference that include in all your articles that use the same selector.</span></span>

### <a name="code-snippets"></a><span data-ttu-id="b9976-325">代码片段</span><span class="sxs-lookup"><span data-stu-id="b9976-325">Code snippets</span></span>

<span data-ttu-id="b9976-326">DFM 支持通过代码片段扩展以一种高级方式将代码加入文章中。</span><span class="sxs-lookup"><span data-stu-id="b9976-326">DFM supports advanced inclusion of code in an article, via its code snippet extension.</span></span> <span data-ttu-id="b9976-327">它提供了一种高级的呈现方式，这种方式基于 GFM 功能（例如编程语言选择和语法着色）以及以下一些出色的功能生成：</span><span class="sxs-lookup"><span data-stu-id="b9976-327">It provides advanced rendering that builds on GFM features such as programming language selection and syntax coloring, plus nice features such as:</span></span>

- <span data-ttu-id="b9976-328">通过外部存储库加入集中式代码示例/片段。</span><span class="sxs-lookup"><span data-stu-id="b9976-328">Inclusion of centralized code samples/snippets from an external repository.</span></span>
- <span data-ttu-id="b9976-329">选项卡式 UI，可采用不同语言显示多个版本的代码示例。</span><span class="sxs-lookup"><span data-stu-id="b9976-329">Tabbed UI to show multiple versions of code samples in different languages.</span></span>

## <a name="gotchas-and-troubleshooting"></a><span data-ttu-id="b9976-330">难题和故障排除</span><span class="sxs-lookup"><span data-stu-id="b9976-330">Gotchas and troubleshooting</span></span>

### <a name="alt-text"></a><span data-ttu-id="b9976-331">替换文字</span><span class="sxs-lookup"><span data-stu-id="b9976-331">Alt text</span></span>

<span data-ttu-id="b9976-332">无法正确显示带下划线的替换文字。</span><span class="sxs-lookup"><span data-stu-id="b9976-332">Alt text that contains underscores won't be rendered properly.</span></span> <span data-ttu-id="b9976-333">例如，与使用以下下划线相比：</span><span class="sxs-lookup"><span data-stu-id="b9976-333">For example, instead of using this:</span></span>

```markdown
![ADextension_2FA_Configure_Step4] (./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

<span data-ttu-id="b9976-334">转义下划线，如下所示：</span><span class="sxs-lookup"><span data-stu-id="b9976-334">Escape the underscores like this:</span></span>

```markdown
![ADextension\_2FA\_Configure\_Step4] (./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

### <a name="apostrophes-and-quotation-marks"></a><span data-ttu-id="b9976-335">撇号和引号</span><span class="sxs-lookup"><span data-stu-id="b9976-335">Apostrophes and quotation marks</span></span>

<span data-ttu-id="b9976-336">如果将文本从 Word 复制到 Markdown 编辑器，文本可能包含“弯”撇号或弯引号。</span><span class="sxs-lookup"><span data-stu-id="b9976-336">If you copy from Word into a Markdown editor, the text might contain "smart" (curly) apostrophes or quotation marks.</span></span> <span data-ttu-id="b9976-337">需要将这些内容编码或更改为基本撇号或单引号。</span><span class="sxs-lookup"><span data-stu-id="b9976-337">These need to be encoded or changed to basic apostrophes or quotation marks.</span></span> <span data-ttu-id="b9976-338">否则，在发布文件时，最终将得到：Itâ€™s</span><span class="sxs-lookup"><span data-stu-id="b9976-338">Otherwise, you end up with things like this when the file is published: Itâ€™s</span></span>

<span data-ttu-id="b9976-339">下面是关于这些“弯”版本标点符号的编码：</span><span class="sxs-lookup"><span data-stu-id="b9976-339">Here are the encodings for the "smart" versions of these punctuation marks:</span></span>

- <span data-ttu-id="b9976-340">左（开）引号：`&#8220;`</span><span class="sxs-lookup"><span data-stu-id="b9976-340">Left (opening) quotation mark: `&#8220;`</span></span>
- <span data-ttu-id="b9976-341">右（闭）引号：`&#8221;`</span><span class="sxs-lookup"><span data-stu-id="b9976-341">Right (closing) quotation mark: `&#8221;`</span></span>
- <span data-ttu-id="b9976-342">右单（闭）引号/撇号：`&#8217;`</span><span class="sxs-lookup"><span data-stu-id="b9976-342">Right (closing) single quotation mark or apostrophe: `&#8217;`</span></span>
- <span data-ttu-id="b9976-343">左单（开）引号（很少使用）：`&#8216;`</span><span class="sxs-lookup"><span data-stu-id="b9976-343">Left (opening) single quotation mark (rarely used): `&#8216;`</span></span>

### <a name="angle-brackets"></a><span data-ttu-id="b9976-344">尖括号</span><span class="sxs-lookup"><span data-stu-id="b9976-344">Angle brackets</span></span>

<span data-ttu-id="b9976-345">如果在文件中的文本（不是代码）里使用尖括号（例如要表示占位符），则需要对尖括号手动编码。</span><span class="sxs-lookup"><span data-stu-id="b9976-345">If you use angle brackets in text (not code) in your file--for example, to denote a placeholder--you need to manually encode the angle brackets.</span></span> <span data-ttu-id="b9976-346">否则，Markdown 会认为它们是一个 HTML 标记。</span><span class="sxs-lookup"><span data-stu-id="b9976-346">Otherwise, Markdown thinks that they're intended to be an HTML tag.</span></span>

<span data-ttu-id="b9976-347">例如，将 `<script name>` 编码为 `&lt;script name&gt;`</span><span class="sxs-lookup"><span data-stu-id="b9976-347">For example, encode `<script name>` as `&lt;script name&gt;`</span></span>

## <a name="see-also"></a><span data-ttu-id="b9976-348">另请参阅</span><span class="sxs-lookup"><span data-stu-id="b9976-348">See also</span></span>

### <a name="markdown-resources"></a><span data-ttu-id="b9976-349">Markdown 资源</span><span class="sxs-lookup"><span data-stu-id="b9976-349">Markdown resources</span></span>

- [<span data-ttu-id="b9976-350">Markdown 简介</span><span class="sxs-lookup"><span data-stu-id="b9976-350">Introduction to Markdown</span></span>](https://daringfireball.net/projects/markdown/syntax)
- [<span data-ttu-id="b9976-351">Docs Markdown 备忘单</span><span class="sxs-lookup"><span data-stu-id="b9976-351">Docs Markdown cheat sheet</span></span>](./media/documents/markdown-cheatsheet.pdf?raw=true)
- [<span data-ttu-id="b9976-352">GitHub 的 Markdown 基础知识</span><span class="sxs-lookup"><span data-stu-id="b9976-352">GitHub's Markdown Basics</span></span>](https://help.github.com/articles/markdown-basics/)
