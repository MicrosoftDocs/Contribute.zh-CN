---
title: 如何使用 Markdown 撰写 Docs
description: 本文提供用于撰写 docs.microsoft.com 文章的 Markdown 语言的基础知识和参考信息。
ms.date: 07/13/2017
ms.openlocfilehash: dca1ccba2ae4ebd08b6039f5d780e7a7ac92e79f
ms.sourcegitcommit: 92aef5ea8bdd692c5c393d5c8f99b9e4f672ef2b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/19/2018
ms.locfileid: "36238957"
---
# <a name="how-to-use-markdown-for-writing-docs"></a><span data-ttu-id="90e9b-103">如何使用 Markdown 撰写 Docs</span><span class="sxs-lookup"><span data-stu-id="90e9b-103">How to use Markdown for writing Docs</span></span>

<span data-ttu-id="90e9b-104">Docs.microsoft.com 文章均采用一种称为 [Markdown](https://daringfireball.net/projects/markdown/) 的轻量级标记语言编写，这种语言易读且易学。</span><span class="sxs-lookup"><span data-stu-id="90e9b-104">Docs.microsoft.com articles are written in a lightweight markup language called [Markdown](https://daringfireball.net/projects/markdown/), which is both easy to read and easy to learn.</span></span> <span data-ttu-id="90e9b-105">正因为如此，Markdown 已迅速成为行业标准。</span><span class="sxs-lookup"><span data-stu-id="90e9b-105">Because of this, it has quickly become an industry standard.</span></span>

<span data-ttu-id="90e9b-106">由于 Doc 内容存储在 GitHub 中，因此可以使用 Markdown 超集（称为 [ GitHub 风格的 Markdown (GFM)](https://help.github.com/categories/writing-on-github/)），它为常用格式需求提供了附加功能。</span><span class="sxs-lookup"><span data-stu-id="90e9b-106">Because Docs content is stored in GitHub, it can use a superset of Markdown called [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/), which provides additional functionality for common formatting needs.</span></span> <span data-ttu-id="90e9b-107">此外， Open Publishing Services (OPS) 还将实现 Markdig Markdown 分析程序。</span><span class="sxs-lookup"><span data-stu-id="90e9b-107">Additionally, Open Publishing Services (OPS) implements Markdig Markdown Parser.</span></span> <span data-ttu-id="90e9b-108">Markdig 与 GitHub 风格的 Markdown (GFM) 高度兼容，并添加了实现 Docs 特定功能的功能。</span><span class="sxs-lookup"><span data-stu-id="90e9b-108">Markdig is highly compatible with GitHub Flavored Markdown (GFM), adding functionality to enable Docs-specific features.</span></span>

* <span data-ttu-id="90e9b-109">Markdig 是一种适用于 .NET 的 Markdown 分析程序，它运行快速、功能强大且兼容 CommonMark。</span><span class="sxs-lookup"><span data-stu-id="90e9b-109">Markdig is a fast, powerful, CommonMark compliant, extensible Markdown processor for .NET.</span></span>
* https://github.com/lunet-io/markdig
* <span data-ttu-id="90e9b-110">更好的社区支持</span><span class="sxs-lookup"><span data-stu-id="90e9b-110">Better community support</span></span>
* <span data-ttu-id="90e9b-111">更好的标准支持</span><span class="sxs-lookup"><span data-stu-id="90e9b-111">Better standards support</span></span>

## <a name="markdown-basics"></a><span data-ttu-id="90e9b-112">Markdown 基础知识</span><span class="sxs-lookup"><span data-stu-id="90e9b-112">Markdown basics</span></span>

### <a name="headings"></a><span data-ttu-id="90e9b-113">标题</span><span class="sxs-lookup"><span data-stu-id="90e9b-113">Headings</span></span>

<span data-ttu-id="90e9b-114">要创建标题，请使用井号标记 (#)，如下所示：</span><span class="sxs-lookup"><span data-stu-id="90e9b-114">To create a heading, you use a hash mark (#), as follows:</span></span>

```markdown
    # This is heading 1
    ## This is heading 2
    ### This is heading 3
    #### This is heading 4
```

### <a name="bold-and-italic-text"></a><span data-ttu-id="90e9b-115">粗体和斜体文本</span><span class="sxs-lookup"><span data-stu-id="90e9b-115">Bold and italic text</span></span>

<span data-ttu-id="90e9b-116">要将文本设置为粗体格式，请用两个星号括住文本：</span><span class="sxs-lookup"><span data-stu-id="90e9b-116">To format text as **bold**, you enclose it in two asterisks:</span></span>

```markdown
    This text is **bold**.
```

<span data-ttu-id="90e9b-117">要将文本设置为斜体格式，请用一个星号括住文本：</span><span class="sxs-lookup"><span data-stu-id="90e9b-117">To format text as *italic*, you enclose it in a single asterisk:</span></span>

```markdown
    This text is *italic*.
```

<span data-ttu-id="90e9b-118">要将文本同时设置为粗体和斜体格式，请用三个星号括住文本：</span><span class="sxs-lookup"><span data-stu-id="90e9b-118">To format text as both ***bold and italic***, you enclose it in three asterisks:</span></span>

```markdown
    This is text is both ***bold and italic***.
```

### <a name="lists"></a><span data-ttu-id="90e9b-119">列表</span><span class="sxs-lookup"><span data-stu-id="90e9b-119">Lists</span></span>

#### <a name="unordered-list"></a><span data-ttu-id="90e9b-120">无序列表</span><span class="sxs-lookup"><span data-stu-id="90e9b-120">Unordered list</span></span>

<span data-ttu-id="90e9b-121">要为无序列表/项目符号列表设置格式，可以使用星号或短划线。</span><span class="sxs-lookup"><span data-stu-id="90e9b-121">To format an unordered/bulleted list, you can use either asterisks or dashes.</span></span> <span data-ttu-id="90e9b-122">例如，以下 Markdown：</span><span class="sxs-lookup"><span data-stu-id="90e9b-122">For example, the following Markdown:</span></span>

```markdown
- List item 1
- List item 2
- List item 3
```

<span data-ttu-id="90e9b-123">将显示为：</span><span class="sxs-lookup"><span data-stu-id="90e9b-123">will be rendered as:</span></span>

- <span data-ttu-id="90e9b-124">列表项目 1</span><span class="sxs-lookup"><span data-stu-id="90e9b-124">List item 1</span></span>
- <span data-ttu-id="90e9b-125">列表项目 2</span><span class="sxs-lookup"><span data-stu-id="90e9b-125">List item 2</span></span>
- <span data-ttu-id="90e9b-126">列表项目 3</span><span class="sxs-lookup"><span data-stu-id="90e9b-126">List item 3</span></span>

<span data-ttu-id="90e9b-127">要将一个列表嵌套在另一个列表中，请缩进子列表项。</span><span class="sxs-lookup"><span data-stu-id="90e9b-127">To nest a list within another list, indent the child list items.</span></span> <span data-ttu-id="90e9b-128">例如，以下 Markdown：</span><span class="sxs-lookup"><span data-stu-id="90e9b-128">For example, the following Markdown:</span></span>

```markdown
- List item 1
  - List item A
  - List item B
- List item 2
```

<span data-ttu-id="90e9b-129">将显示为：</span><span class="sxs-lookup"><span data-stu-id="90e9b-129">will be rendered as:</span></span>

- <span data-ttu-id="90e9b-130">列表项目 1</span><span class="sxs-lookup"><span data-stu-id="90e9b-130">List item 1</span></span>
  - <span data-ttu-id="90e9b-131">列表项目 A</span><span class="sxs-lookup"><span data-stu-id="90e9b-131">List item A</span></span>
  - <span data-ttu-id="90e9b-132">列表项目 B</span><span class="sxs-lookup"><span data-stu-id="90e9b-132">List item B</span></span>
- <span data-ttu-id="90e9b-133">列表项目 2</span><span class="sxs-lookup"><span data-stu-id="90e9b-133">List item 2</span></span>

#### <a name="ordered-list"></a><span data-ttu-id="90e9b-134">有序列表</span><span class="sxs-lookup"><span data-stu-id="90e9b-134">Ordered list</span></span>

<span data-ttu-id="90e9b-135">要设置有序/分阶段列表的格式，可以使用相应的编号。</span><span class="sxs-lookup"><span data-stu-id="90e9b-135">To format an ordered/stepwise list, you use corresponding numbers.</span></span> <span data-ttu-id="90e9b-136">例如，以下 Markdown：</span><span class="sxs-lookup"><span data-stu-id="90e9b-136">For example, the following Markdown:</span></span>

```markdown
1. First instruction
2. Second instruction
3. Third instruction
```

<span data-ttu-id="90e9b-137">将显示为：</span><span class="sxs-lookup"><span data-stu-id="90e9b-137">will be rendered as:</span></span>

1. <span data-ttu-id="90e9b-138">第一个说明</span><span class="sxs-lookup"><span data-stu-id="90e9b-138">First instruction</span></span>
2. <span data-ttu-id="90e9b-139">第二个说明</span><span class="sxs-lookup"><span data-stu-id="90e9b-139">Second instruction</span></span>
3. <span data-ttu-id="90e9b-140">第三个说明</span><span class="sxs-lookup"><span data-stu-id="90e9b-140">Third instruction</span></span>

<span data-ttu-id="90e9b-141">要将一个列表嵌套在另一个列表中，请缩进子列表项。</span><span class="sxs-lookup"><span data-stu-id="90e9b-141">To nest a list within another list, indent the child list items.</span></span> <span data-ttu-id="90e9b-142">例如，以下 Markdown：</span><span class="sxs-lookup"><span data-stu-id="90e9b-142">For example, the following Markdown:</span></span>

```markdown
1. First instruction
    1. Sub-instruction
    2. Sub-instruction
2. Second instruction
```

<span data-ttu-id="90e9b-143">将显示为：</span><span class="sxs-lookup"><span data-stu-id="90e9b-143">will be rendered as:</span></span>

1. <span data-ttu-id="90e9b-144">第一个说明</span><span class="sxs-lookup"><span data-stu-id="90e9b-144">First instruction</span></span>
    1. <span data-ttu-id="90e9b-145">辅助说明</span><span class="sxs-lookup"><span data-stu-id="90e9b-145">Sub-instruction</span></span>
    2. <span data-ttu-id="90e9b-146">辅助说明</span><span class="sxs-lookup"><span data-stu-id="90e9b-146">Sub-instruction</span></span>
2. <span data-ttu-id="90e9b-147">第二个说明</span><span class="sxs-lookup"><span data-stu-id="90e9b-147">Second instruction</span></span>

### <a name="tables"></a><span data-ttu-id="90e9b-148">表格</span><span class="sxs-lookup"><span data-stu-id="90e9b-148">Tables</span></span>

<span data-ttu-id="90e9b-149">表格不属于核心 Markdown 规范，但是它们受 GFM 支持。</span><span class="sxs-lookup"><span data-stu-id="90e9b-149">Tables are not part of the core Markdown specification, but GFM supports them.</span></span> <span data-ttu-id="90e9b-150">可以使用竖线 (|) 和连字符 (-) 字符创建表格。</span><span class="sxs-lookup"><span data-stu-id="90e9b-150">You can create tables by using the pipe (|) and hyphen (-) characters.</span></span> <span data-ttu-id="90e9b-151">连字符用于创建每列的标题，而竖线用于分隔每列。</span><span class="sxs-lookup"><span data-stu-id="90e9b-151">Hyphens create each column's header, while pipes separate each column.</span></span> <span data-ttu-id="90e9b-152">请在表格前面加入一个空行，使它能够正确显示。</span><span class="sxs-lookup"><span data-stu-id="90e9b-152">Include a blank line before your table so it's rendered correctly.</span></span>

<span data-ttu-id="90e9b-153">例如，以下 Markdown：</span><span class="sxs-lookup"><span data-stu-id="90e9b-153">For example, the following Markdown:</span></span>

```markdown
| Fun                  | With                 | Tables          |
| :------------------- | -------------------: |:---------------:|
| left-aligned column  | right-aligned column | centered column |
| $100                 | $100                 | $100            |
| $10                  | $10                  | $10             |
| $1                   | $1                   | $1              |
```

<span data-ttu-id="90e9b-154">将显示为：</span><span class="sxs-lookup"><span data-stu-id="90e9b-154">will be rendered as:</span></span>

| <span data-ttu-id="90e9b-155">趣</span><span class="sxs-lookup"><span data-stu-id="90e9b-155">Fun</span></span>                  | <span data-ttu-id="90e9b-156">含</span><span class="sxs-lookup"><span data-stu-id="90e9b-156">With</span></span>                 | <span data-ttu-id="90e9b-157">表格</span><span class="sxs-lookup"><span data-stu-id="90e9b-157">Tables</span></span>          |
| :------------------- | -------------------: |:---------------:|
| <span data-ttu-id="90e9b-158">左对齐列</span><span class="sxs-lookup"><span data-stu-id="90e9b-158">left-aligned column</span></span>  | <span data-ttu-id="90e9b-159">右对齐列</span><span class="sxs-lookup"><span data-stu-id="90e9b-159">right-aligned column</span></span> | <span data-ttu-id="90e9b-160">居中列</span><span class="sxs-lookup"><span data-stu-id="90e9b-160">centered column</span></span> |
| <span data-ttu-id="90e9b-161">$100</span><span class="sxs-lookup"><span data-stu-id="90e9b-161">$100</span></span>                 | <span data-ttu-id="90e9b-162">$100</span><span class="sxs-lookup"><span data-stu-id="90e9b-162">$100</span></span>                 | <span data-ttu-id="90e9b-163">$100</span><span class="sxs-lookup"><span data-stu-id="90e9b-163">$100</span></span>            |
| <span data-ttu-id="90e9b-164">$10</span><span class="sxs-lookup"><span data-stu-id="90e9b-164">$10</span></span>                  | <span data-ttu-id="90e9b-165">$10</span><span class="sxs-lookup"><span data-stu-id="90e9b-165">$10</span></span>                  | <span data-ttu-id="90e9b-166">$10</span><span class="sxs-lookup"><span data-stu-id="90e9b-166">$10</span></span>             |
| <span data-ttu-id="90e9b-167">$1</span><span class="sxs-lookup"><span data-stu-id="90e9b-167">$1</span></span>                   | <span data-ttu-id="90e9b-168">$1</span><span class="sxs-lookup"><span data-stu-id="90e9b-168">$1</span></span>                   | <span data-ttu-id="90e9b-169">$1</span><span class="sxs-lookup"><span data-stu-id="90e9b-169">$1</span></span>              |

<span data-ttu-id="90e9b-170">有关创建表格的详细信息，请参阅：</span><span class="sxs-lookup"><span data-stu-id="90e9b-170">For more information on creating tables, see:</span></span>

- <span data-ttu-id="90e9b-171">Markdig [表格换行功能](#table-wrapping)，有助于设置宽表格的格式</span><span class="sxs-lookup"><span data-stu-id="90e9b-171">The Markdig [table wrapping feature](#table-wrapping), which can help with formatting of wide tables</span></span>
- <span data-ttu-id="90e9b-172">GitHub 的[使用表格整理信息](https://help.github.com/articles/organizing-information-with-tables/)</span><span class="sxs-lookup"><span data-stu-id="90e9b-172">GitHub's [Organizing information with tables](https://help.github.com/articles/organizing-information-with-tables/)</span></span>
- <span data-ttu-id="90e9b-173">[Markdown 表格生成器](https://www.tablesgenerator.com/markdown_tables) Web 应用</span><span class="sxs-lookup"><span data-stu-id="90e9b-173">The [Markdown Tables Generator](https://www.tablesgenerator.com/markdown_tables) web app</span></span>
- [<span data-ttu-id="90e9b-174">Adam Pritchard 的 Markdown 备忘单</span><span class="sxs-lookup"><span data-stu-id="90e9b-174">Adam Pritchard's Markdown Cheatsheet</span></span>](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#wiki-tables)
- [<span data-ttu-id="90e9b-175">Michel Fortin 的 Markdown Extra</span><span class="sxs-lookup"><span data-stu-id="90e9b-175">Michel Fortin's Markdown Extra</span></span>](https://michelf.ca/projects/php-markdown/extra/#table)
- [<span data-ttu-id="90e9b-176">将 HTML 表转换为 Markdown 格式</span><span class="sxs-lookup"><span data-stu-id="90e9b-176">Convert HTML tables to Markdown</span></span>](https://jmalarcon.github.io/markdowntables/)

### <a name="links"></a><span data-ttu-id="90e9b-177">链接</span><span class="sxs-lookup"><span data-stu-id="90e9b-177">Links</span></span>

<span data-ttu-id="90e9b-178">Markdown 的内联链接语法由两部分组成：`[link text]` 部分，这是要创建为超链接的文本；后跟 `(file-name.md)` 部分，这是要链接到的 URL 或者文件名：</span><span class="sxs-lookup"><span data-stu-id="90e9b-178">The Markdown syntax for an inline link consists of the `[link text]` portion, which is the text that will be hyperlinked, followed by the `(file-name.md)` portion, which is the URL or file name that's being linked to:</span></span>

 `[link text](file-name.md)`

<span data-ttu-id="90e9b-179">有关链接的详细信息，请参阅：</span><span class="sxs-lookup"><span data-stu-id="90e9b-179">For more information on linking, see:</span></span>

- <span data-ttu-id="90e9b-180">[Markdown 语法指南](https://daringfireball.net/projects/markdown/syntax#link)，详细了解 Markdown 的基本链接支持相关信息。</span><span class="sxs-lookup"><span data-stu-id="90e9b-180">The [Markdown syntax guide](https://daringfireball.net/projects/markdown/syntax#link) for details on Markdown's base linking support.</span></span>
- <span data-ttu-id="90e9b-181">本指南的[链接](how-to-write-links.md)部分，了解 Markdig 提供的其他链接语法的详细信息。</span><span class="sxs-lookup"><span data-stu-id="90e9b-181">The [Links](how-to-write-links.md) section of this guide for details on additional linking syntax that Markdig provides.</span></span>

### <a name="code-snippets"></a><span data-ttu-id="90e9b-182">代码片段</span><span class="sxs-lookup"><span data-stu-id="90e9b-182">Code snippets</span></span>

<span data-ttu-id="90e9b-183">Markdown 不仅支持将代码片段内联在某个句子中，还支持将它作为单独的“隔离”块放置在两个句子之间。</span><span class="sxs-lookup"><span data-stu-id="90e9b-183">Markdown supports the placement of code snippets both inline in a sentence and as a separate "fenced" block between sentences.</span></span> <span data-ttu-id="90e9b-184">有关详细信息，请参阅：</span><span class="sxs-lookup"><span data-stu-id="90e9b-184">For details, see:</span></span>

- [<span data-ttu-id="90e9b-185">Markdown 代码块本机支持</span><span class="sxs-lookup"><span data-stu-id="90e9b-185">Markdown's native support for code blocks</span></span>](https://daringfireball.net/projects/markdown/syntax#precode)
- [<span data-ttu-id="90e9b-186">针对代码隔离和语法高亮显示的 GFM 支持</span><span class="sxs-lookup"><span data-stu-id="90e9b-186">GFM support for code fencing and syntax highlighting</span></span>](https://help.github.com/articles/creating-and-highlighting-code-blocks/)

<span data-ttu-id="90e9b-187">借助隔离代码块，可以轻松实现代码片段的语法高亮显示。</span><span class="sxs-lookup"><span data-stu-id="90e9b-187">Fenced code blocks are an easy way to enable syntax highlighting for your code snippets.</span></span> <span data-ttu-id="90e9b-188">隔离代码块的一般格式为：</span><span class="sxs-lookup"><span data-stu-id="90e9b-188">The general format for fenced code blocks is:</span></span>

    ```alias
    ...
    your code goes in here
    ...
    ```

<span data-ttu-id="90e9b-189">开头的三个撇号 (\`) 字符后面的别名定义要使用的语法高亮显示。</span><span class="sxs-lookup"><span data-stu-id="90e9b-189">The alias after the initial three backtick (\`) characters defines the syntax highlighting to be used.</span></span> <span data-ttu-id="90e9b-190">下面列出了 Docs 内容中常用的编程语言以及匹配的标签：</span><span class="sxs-lookup"><span data-stu-id="90e9b-190">The following is a list of commonly used programming languages in Docs content and the matching label:</span></span>

<span data-ttu-id="90e9b-191">这些语言支持友好名称并且大多数都可以突出显示语言。</span><span class="sxs-lookup"><span data-stu-id="90e9b-191">These languages have friendly name support and most have language highlighting.</span></span>

|<span data-ttu-id="90e9b-192">名称</span><span class="sxs-lookup"><span data-stu-id="90e9b-192">Name</span></span>|<span data-ttu-id="90e9b-193">Markdown 标签</span><span class="sxs-lookup"><span data-stu-id="90e9b-193">Markdown Label</span></span>|
|-----|-------|
|<span data-ttu-id="90e9b-194">.NET 控制台</span><span class="sxs-lookup"><span data-stu-id="90e9b-194">.NET Console</span></span>|<span data-ttu-id="90e9b-195">dotnetcli</span><span class="sxs-lookup"><span data-stu-id="90e9b-195">dotnetcli</span></span>|
|<span data-ttu-id="90e9b-196">ASP.NET (C#)</span><span class="sxs-lookup"><span data-stu-id="90e9b-196">ASP.NET (C#)</span></span>|<span data-ttu-id="90e9b-197">aspx-csharp</span><span class="sxs-lookup"><span data-stu-id="90e9b-197">aspx-csharp</span></span>|
|<span data-ttu-id="90e9b-198">ASP.NET (VB)</span><span class="sxs-lookup"><span data-stu-id="90e9b-198">ASP.NET (VB)</span></span>|<span data-ttu-id="90e9b-199">aspx-vb</span><span class="sxs-lookup"><span data-stu-id="90e9b-199">aspx-vb</span></span>|
|<span data-ttu-id="90e9b-200">AzCopy</span><span class="sxs-lookup"><span data-stu-id="90e9b-200">AzCopy</span></span>|<span data-ttu-id="90e9b-201">azcopy</span><span class="sxs-lookup"><span data-stu-id="90e9b-201">azcopy</span></span>|
|<span data-ttu-id="90e9b-202">Azure CLI</span><span class="sxs-lookup"><span data-stu-id="90e9b-202">Azure CLI</span></span>|<span data-ttu-id="90e9b-203">azurecli</span><span class="sxs-lookup"><span data-stu-id="90e9b-203">azurecli</span></span>|
|<span data-ttu-id="90e9b-204">Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="90e9b-204">Azure PowerShell</span></span>|<span data-ttu-id="90e9b-205">azurepowershell</span><span class="sxs-lookup"><span data-stu-id="90e9b-205">azurepowershell</span></span>|
|<span data-ttu-id="90e9b-206">C++</span><span class="sxs-lookup"><span data-stu-id="90e9b-206">C++</span></span>|<span data-ttu-id="90e9b-207">cpp</span><span class="sxs-lookup"><span data-stu-id="90e9b-207">cpp</span></span>|
|<span data-ttu-id="90e9b-208">C++/CX</span><span class="sxs-lookup"><span data-stu-id="90e9b-208">C++/CX</span></span>|<span data-ttu-id="90e9b-209">cppcx</span><span class="sxs-lookup"><span data-stu-id="90e9b-209">cppcx</span></span>|
|<span data-ttu-id="90e9b-210">C++/WinRT</span><span class="sxs-lookup"><span data-stu-id="90e9b-210">C++/WinRT</span></span>|<span data-ttu-id="90e9b-211">cppwinrt</span><span class="sxs-lookup"><span data-stu-id="90e9b-211">cppwinrt</span></span>|
|<span data-ttu-id="90e9b-212">C#</span><span class="sxs-lookup"><span data-stu-id="90e9b-212">C#</span></span>|<span data-ttu-id="90e9b-213">csharp</span><span class="sxs-lookup"><span data-stu-id="90e9b-213">csharp</span></span>|
|<span data-ttu-id="90e9b-214">CSHTML</span><span class="sxs-lookup"><span data-stu-id="90e9b-214">CSHTML</span></span>|<span data-ttu-id="90e9b-215">cshtml</span><span class="sxs-lookup"><span data-stu-id="90e9b-215">cshtml</span></span>|
|<span data-ttu-id="90e9b-216">DAX</span><span class="sxs-lookup"><span data-stu-id="90e9b-216">DAX</span></span>|<span data-ttu-id="90e9b-217">dax</span><span class="sxs-lookup"><span data-stu-id="90e9b-217">dax</span></span>|
|<span data-ttu-id="90e9b-218">F#</span><span class="sxs-lookup"><span data-stu-id="90e9b-218">F#</span></span>|<span data-ttu-id="90e9b-219">fsharp</span><span class="sxs-lookup"><span data-stu-id="90e9b-219">fsharp</span></span>|
|<span data-ttu-id="90e9b-220">Go</span><span class="sxs-lookup"><span data-stu-id="90e9b-220">Go</span></span>|<span data-ttu-id="90e9b-221">go</span><span class="sxs-lookup"><span data-stu-id="90e9b-221">go</span></span>|
|<span data-ttu-id="90e9b-222">HTML</span><span class="sxs-lookup"><span data-stu-id="90e9b-222">HTML</span></span>|<span data-ttu-id="90e9b-223">html</span><span class="sxs-lookup"><span data-stu-id="90e9b-223">html</span></span>|
|<span data-ttu-id="90e9b-224">HTTP</span><span class="sxs-lookup"><span data-stu-id="90e9b-224">HTTP</span></span>|<span data-ttu-id="90e9b-225">http</span><span class="sxs-lookup"><span data-stu-id="90e9b-225">http</span></span>|
|<span data-ttu-id="90e9b-226">Java</span><span class="sxs-lookup"><span data-stu-id="90e9b-226">Java</span></span>|<span data-ttu-id="90e9b-227">java</span><span class="sxs-lookup"><span data-stu-id="90e9b-227">java</span></span>|
|<span data-ttu-id="90e9b-228">JavaScript</span><span class="sxs-lookup"><span data-stu-id="90e9b-228">JavaScript</span></span>|<span data-ttu-id="90e9b-229">javascript</span><span class="sxs-lookup"><span data-stu-id="90e9b-229">javascript</span></span>|
|<span data-ttu-id="90e9b-230">JSON</span><span class="sxs-lookup"><span data-stu-id="90e9b-230">JSON</span></span>|<span data-ttu-id="90e9b-231">json</span><span class="sxs-lookup"><span data-stu-id="90e9b-231">json</span></span>|
|<span data-ttu-id="90e9b-232">Markdown</span><span class="sxs-lookup"><span data-stu-id="90e9b-232">Markdown</span></span>|<span data-ttu-id="90e9b-233">md</span><span class="sxs-lookup"><span data-stu-id="90e9b-233">md</span></span>|
|<span data-ttu-id="90e9b-234">NodeJS</span><span class="sxs-lookup"><span data-stu-id="90e9b-234">NodeJS</span></span>|<span data-ttu-id="90e9b-235">nodejs</span><span class="sxs-lookup"><span data-stu-id="90e9b-235">nodejs</span></span>|
|<span data-ttu-id="90e9b-236">Objective-C</span><span class="sxs-lookup"><span data-stu-id="90e9b-236">Objective-C</span></span>|<span data-ttu-id="90e9b-237">objc</span><span class="sxs-lookup"><span data-stu-id="90e9b-237">objc</span></span>|
|<span data-ttu-id="90e9b-238">OData</span><span class="sxs-lookup"><span data-stu-id="90e9b-238">OData</span></span>|<span data-ttu-id="90e9b-239">odata</span><span class="sxs-lookup"><span data-stu-id="90e9b-239">odata</span></span>|
|<span data-ttu-id="90e9b-240">PHP</span><span class="sxs-lookup"><span data-stu-id="90e9b-240">PHP</span></span>|<span data-ttu-id="90e9b-241">php</span><span class="sxs-lookup"><span data-stu-id="90e9b-241">php</span></span>|
|<span data-ttu-id="90e9b-242">Power Apps Formula</span><span class="sxs-lookup"><span data-stu-id="90e9b-242">Power Apps Formula</span></span>|<span data-ttu-id="90e9b-243">powerappsfl</span><span class="sxs-lookup"><span data-stu-id="90e9b-243">powerappsfl</span></span>|
|<span data-ttu-id="90e9b-244">PowerShell</span><span class="sxs-lookup"><span data-stu-id="90e9b-244">PowerShell</span></span>|<span data-ttu-id="90e9b-245">powershell</span><span class="sxs-lookup"><span data-stu-id="90e9b-245">powershell</span></span>|
|<span data-ttu-id="90e9b-246">Python</span><span class="sxs-lookup"><span data-stu-id="90e9b-246">Python</span></span>|<span data-ttu-id="90e9b-247">python</span><span class="sxs-lookup"><span data-stu-id="90e9b-247">python</span></span>|
|<span data-ttu-id="90e9b-248">Q#</span><span class="sxs-lookup"><span data-stu-id="90e9b-248">Q#</span></span>|<span data-ttu-id="90e9b-249">qsharp</span><span class="sxs-lookup"><span data-stu-id="90e9b-249">qsharp</span></span>|
|<span data-ttu-id="90e9b-250">Ruby</span><span class="sxs-lookup"><span data-stu-id="90e9b-250">Ruby</span></span>|<span data-ttu-id="90e9b-251">ruby</span><span class="sxs-lookup"><span data-stu-id="90e9b-251">ruby</span></span>|
|<span data-ttu-id="90e9b-252">SQL</span><span class="sxs-lookup"><span data-stu-id="90e9b-252">SQL</span></span>|<span data-ttu-id="90e9b-253">sql</span><span class="sxs-lookup"><span data-stu-id="90e9b-253">sql</span></span>|
|<span data-ttu-id="90e9b-254">Swift</span><span class="sxs-lookup"><span data-stu-id="90e9b-254">Swift</span></span>|<span data-ttu-id="90e9b-255">swift</span><span class="sxs-lookup"><span data-stu-id="90e9b-255">swift</span></span>|
|<span data-ttu-id="90e9b-256">TypeScript</span><span class="sxs-lookup"><span data-stu-id="90e9b-256">TypeScript</span></span>|<span data-ttu-id="90e9b-257">typescript</span><span class="sxs-lookup"><span data-stu-id="90e9b-257">typescript</span></span>|
|<span data-ttu-id="90e9b-258">VB</span><span class="sxs-lookup"><span data-stu-id="90e9b-258">VB</span></span>|<span data-ttu-id="90e9b-259">vb</span><span class="sxs-lookup"><span data-stu-id="90e9b-259">vb</span></span>|
|<span data-ttu-id="90e9b-260">VSTS CLI</span><span class="sxs-lookup"><span data-stu-id="90e9b-260">VSTS CLI</span></span>|<span data-ttu-id="90e9b-261">vstscli</span><span class="sxs-lookup"><span data-stu-id="90e9b-261">vstscli</span></span>|
|<span data-ttu-id="90e9b-262">XAML</span><span class="sxs-lookup"><span data-stu-id="90e9b-262">XAML</span></span>|<span data-ttu-id="90e9b-263">xaml</span><span class="sxs-lookup"><span data-stu-id="90e9b-263">xaml</span></span>|
|<span data-ttu-id="90e9b-264">XML</span><span class="sxs-lookup"><span data-stu-id="90e9b-264">XML</span></span>|<span data-ttu-id="90e9b-265">xml</span><span class="sxs-lookup"><span data-stu-id="90e9b-265">xml</span></span>|

#### <a name="example-c"></a><span data-ttu-id="90e9b-266">示例：C\#</span><span class="sxs-lookup"><span data-stu-id="90e9b-266">Example: C\#</span></span>

<span data-ttu-id="90e9b-267">__Markdown__</span><span class="sxs-lookup"><span data-stu-id="90e9b-267">__Markdown__</span></span>

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

<span data-ttu-id="90e9b-268">__呈现__</span><span class="sxs-lookup"><span data-stu-id="90e9b-268">__Render__</span></span>

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

#### <a name="example-sql"></a><span data-ttu-id="90e9b-269">示例：SQL</span><span class="sxs-lookup"><span data-stu-id="90e9b-269">Example: SQL</span></span>

<span data-ttu-id="90e9b-270">__Markdown__</span><span class="sxs-lookup"><span data-stu-id="90e9b-270">__Markdown__</span></span>

    ```sql
    CREATE TABLE T1 (
      c1 int PRIMARY KEY,
      c2 varchar(50) SPARSE NULL
    );
    ```

<span data-ttu-id="90e9b-271">__呈现__</span><span class="sxs-lookup"><span data-stu-id="90e9b-271">__Render__</span></span>

```sql
CREATE TABLE T1 (
  c1 int PRIMARY KEY,
  c2 varchar(50) SPARSE NULL
);
```

## <a name="ops-custom-markdown-extensions"></a><span data-ttu-id="90e9b-272">OPS 自定义 Markdown 扩展</span><span class="sxs-lookup"><span data-stu-id="90e9b-272">OPS custom Markdown extensions</span></span>

> [!NOTE]
> <span data-ttu-id="90e9b-273">Open Publishing Services(OPS) 可实现 Markdown Markdig 分析程序，它与 GitHub 风格的 Markdown (GFM) 高度兼容。</span><span class="sxs-lookup"><span data-stu-id="90e9b-273">Open Publishing Services (OPS) implements a Markdig Parser for Markdown, which is highly compatible with GitHub Flavored Markdown (GFM).</span></span> <span data-ttu-id="90e9b-274">Markdig 通过 Markdown 扩展添加一些功能。</span><span class="sxs-lookup"><span data-stu-id="90e9b-274">Markdig adds some functionality through Markdown extensions.</span></span> <span data-ttu-id="90e9b-275">就这一点而言，本指南从完整的《OPS 创作指南》中选用了几篇文章，以供参考。</span><span class="sxs-lookup"><span data-stu-id="90e9b-275">As such, selected articles from the full OPS Authoring Guide are included in this guide for reference.</span></span> <span data-ttu-id="90e9b-276">（例如，请参阅目录中的“Markdig 和 Markdown 扩展”以及“代码片段”。）</span><span class="sxs-lookup"><span data-stu-id="90e9b-276">(For example, see "Markdig and Markdown extensions" and "Code snippets" in the table of contents.)</span></span>

<span data-ttu-id="90e9b-277">Doc 文章使用 GFM 完成大多文章的格式设置，如段落、链接、列表和标题。</span><span class="sxs-lookup"><span data-stu-id="90e9b-277">Docs articles use GFM for most article formatting, such as paragraphs, links, lists, and headings.</span></span> <span data-ttu-id="90e9b-278">要想实现更丰富的格式设置功能，文章可以使用 Markdig 功能，例如：</span><span class="sxs-lookup"><span data-stu-id="90e9b-278">For richer formatting, articles can use Markdig features such as:</span></span>

- <span data-ttu-id="90e9b-279">备注块</span><span class="sxs-lookup"><span data-stu-id="90e9b-279">Note blocks</span></span>
- <span data-ttu-id="90e9b-280">包含文件</span><span class="sxs-lookup"><span data-stu-id="90e9b-280">Includes</span></span>
- <span data-ttu-id="90e9b-281">选择器</span><span class="sxs-lookup"><span data-stu-id="90e9b-281">Selectors</span></span>
- <span data-ttu-id="90e9b-282">嵌入视频</span><span class="sxs-lookup"><span data-stu-id="90e9b-282">Embedded videos</span></span>
- <span data-ttu-id="90e9b-283">代码片段/示例</span><span class="sxs-lookup"><span data-stu-id="90e9b-283">Code snippets/samples</span></span>

<span data-ttu-id="90e9b-284">如需完整列表，请参阅目录中的“Markdig 和 Markdown 扩展”以及“代码片段”。</span><span class="sxs-lookup"><span data-stu-id="90e9b-284">For the complete list, refer to "Markdig and Markdown extensions" and "Code snippets" in the table of contents.</span></span>

### <a name="note-blocks"></a><span data-ttu-id="90e9b-285">备注块</span><span class="sxs-lookup"><span data-stu-id="90e9b-285">Note blocks</span></span>

<span data-ttu-id="90e9b-286">可以从 4 种类型的备注块中进行选择来吸引对特定内容的注意：</span><span class="sxs-lookup"><span data-stu-id="90e9b-286">You can choose from four types of note blocks to draw attention to specific content:</span></span>

- <span data-ttu-id="90e9b-287">注意</span><span class="sxs-lookup"><span data-stu-id="90e9b-287">NOTE</span></span>
- <span data-ttu-id="90e9b-288">警告</span><span class="sxs-lookup"><span data-stu-id="90e9b-288">WARNING</span></span>
- <span data-ttu-id="90e9b-289">提示</span><span class="sxs-lookup"><span data-stu-id="90e9b-289">TIP</span></span>
- <span data-ttu-id="90e9b-290">重要说明</span><span class="sxs-lookup"><span data-stu-id="90e9b-290">IMPORTANT</span></span>

<span data-ttu-id="90e9b-291">总之，应谨慎使用备注块，因为它们可能会造成干扰。</span><span class="sxs-lookup"><span data-stu-id="90e9b-291">In general, note blocks should be used sparingly because they can be disruptive.</span></span> <span data-ttu-id="90e9b-292">尽管备注块也支持代码块、图像、列表以及链接，但最好尽量保持备注块简单明了。</span><span class="sxs-lookup"><span data-stu-id="90e9b-292">Although they also support code blocks, images, lists, and links, try to keep your note blocks simple and straightforward.</span></span>

### <a name="includes"></a><span data-ttu-id="90e9b-293">包含文件</span><span class="sxs-lookup"><span data-stu-id="90e9b-293">Includes</span></span>

<span data-ttu-id="90e9b-294">如果有需要加入文章文件中的可重用的文本或图像文件，可以通过 Markdig 文件的包含文件功能使用对“包含”文件的引用。</span><span class="sxs-lookup"><span data-stu-id="90e9b-294">When you have reusable text or image files that need to be included in article files, you can use a reference to the "include" file via the Markdig file include feature.</span></span> <span data-ttu-id="90e9b-295">此功能指示 OPS 在创建时将该文件加入文章文件中，使它成为已发布文章的一部分。</span><span class="sxs-lookup"><span data-stu-id="90e9b-295">This feature instructs OPS to include the file in your article file at build time, making it part of your published article.</span></span> <span data-ttu-id="90e9b-296">有 3 种类型的包含功能可帮助你重用内容：</span><span class="sxs-lookup"><span data-stu-id="90e9b-296">Three types of includes are available to help you reuse content:</span></span>

- <span data-ttu-id="90e9b-297">内联：重用内联在其他句子中的常用文本片段。</span><span class="sxs-lookup"><span data-stu-id="90e9b-297">Inline: Reuse a common text snippet inline with within another sentence.</span></span>
- <span data-ttu-id="90e9b-298">块：将整个 Markdown 文件作为一个块来重用，嵌套在文章的某一部分中。</span><span class="sxs-lookup"><span data-stu-id="90e9b-298">Block: Reuse an entire Markdown file as a block, nested within a section of an article.</span></span>
- <span data-ttu-id="90e9b-299">图像：此方法可以在 Doc 中实现标准图像加入。</span><span class="sxs-lookup"><span data-stu-id="90e9b-299">Image: This is how standard image inclusion is implemented in Docs.</span></span>

<span data-ttu-id="90e9b-300">“内联”和“块”包含文件是简单的 Markdown (.md) 文件。</span><span class="sxs-lookup"><span data-stu-id="90e9b-300">An inline or block include is just a simple Markdown (.md) file.</span></span> <span data-ttu-id="90e9b-301">它可以包含任何有效的 Markdown。</span><span class="sxs-lookup"><span data-stu-id="90e9b-301">It can contain any valid Markdown.</span></span> <span data-ttu-id="90e9b-302">所有包含 Markdown 文件都应置于存储库根目录的[常用 `/includes` 子目录](git-github-fundamentals.md#includes-subdirectory) 中。</span><span class="sxs-lookup"><span data-stu-id="90e9b-302">All include Markdown files should be placed in a [common `/includes` subdirectory](git-github-fundamentals.md#includes-subdirectory), in the root of the repository.</span></span> <span data-ttu-id="90e9b-303">发布文章时，加入的文件会无缝集成到其中。</span><span class="sxs-lookup"><span data-stu-id="90e9b-303">When the article is published, the included file is seamlessly integrated into it.</span></span>

<span data-ttu-id="90e9b-304">包含文件的要求和注意事项如下：</span><span class="sxs-lookup"><span data-stu-id="90e9b-304">Here are requirements and considerations for includes:</span></span>

- <span data-ttu-id="90e9b-305">无论何时需要使相同的文本显示在多篇文章中，均可使用包含功能。</span><span class="sxs-lookup"><span data-stu-id="90e9b-305">Use includes whenever you need the same text to appear in multiple articles.</span></span>
- <span data-ttu-id="90e9b-306">块包含文件用于大篇幅内容，比如一个或者两个段落、共享过程或者共享章节。</span><span class="sxs-lookup"><span data-stu-id="90e9b-306">Use block includes for significant amounts of content--a paragraph or two, a shared procedure, or a shared section.</span></span> <span data-ttu-id="90e9b-307">请勿将它们用于小于一个句子的内容。</span><span class="sxs-lookup"><span data-stu-id="90e9b-307">Do not use them for anything smaller than a sentence.</span></span>
- <span data-ttu-id="90e9b-308">包含文件不会在你文章的 GitHub 渲染视图中显示，因为它们依赖于 Markdig 扩展。</span><span class="sxs-lookup"><span data-stu-id="90e9b-308">Includes won't be rendered in the GitHub rendered view of your article, because they rely on Markdig extensions.</span></span> <span data-ttu-id="90e9b-309">它们在发布后才会显示。</span><span class="sxs-lookup"><span data-stu-id="90e9b-309">They'll be rendered only after publication.</span></span>
- <span data-ttu-id="90e9b-310">确保包含文件中的所有文本都是完整的句子或者段落，并且与引用包含文件的文章的前后文没有关联。</span><span class="sxs-lookup"><span data-stu-id="90e9b-310">Ensure that all the text in an include is written in complete sentences or phrases that do not depend on preceding text or following text in the article that references the include.</span></span> <span data-ttu-id="90e9b-311">如果不遵循此指导原则，则会在文章中创建无法转换的字符串，进而破坏本地化体验。</span><span class="sxs-lookup"><span data-stu-id="90e9b-311">Ignoring this guidance creates an untranslatable string in the article that breaks the localized experience.</span></span>
- <span data-ttu-id="90e9b-312">请勿将包含文件嵌入其他包含文件中。</span><span class="sxs-lookup"><span data-stu-id="90e9b-312">Don't embed includes within other includes.</span></span> <span data-ttu-id="90e9b-313">不支持此操作。</span><span class="sxs-lookup"><span data-stu-id="90e9b-313">They are not supported.</span></span>
- <span data-ttu-id="90e9b-314">将媒体文件置于特定于包含文件子目录的媒体文件夹中，例如，`<repo>`/includes/媒体文件夹。</span><span class="sxs-lookup"><span data-stu-id="90e9b-314">Place media files in a media folder that's specific to the include subdirectory--for instance, the `<repo>`/includes/media folder.</span></span> <span data-ttu-id="90e9b-315">媒体目录不应在根目录中包含任何图片。</span><span class="sxs-lookup"><span data-stu-id="90e9b-315">The media directory should not contain any images in its root.</span></span> <span data-ttu-id="90e9b-316">如果包含文件不包含图像，则不需要相应的媒体目录。</span><span class="sxs-lookup"><span data-stu-id="90e9b-316">If the include does not have images, a corresponding media directory is not required.</span></span>
- <span data-ttu-id="90e9b-317">对于常规文章，请勿在各包含文件之间共享媒体。</span><span class="sxs-lookup"><span data-stu-id="90e9b-317">As with regular articles, don't share media between include files.</span></span> <span data-ttu-id="90e9b-318">对于每个包含文件和文章，请使用具有唯一名称的单独文件。</span><span class="sxs-lookup"><span data-stu-id="90e9b-318">Use a separate file with a unique name for each include and article.</span></span> <span data-ttu-id="90e9b-319">将媒体文件存储在与包含文件关联的媒体文件夹中。</span><span class="sxs-lookup"><span data-stu-id="90e9b-319">Store the media file in the media folder that's associated with the include.</span></span>
- <span data-ttu-id="90e9b-320">请勿将包含文件用作文章的唯一内容。</span><span class="sxs-lookup"><span data-stu-id="90e9b-320">Don't use an include as the only content of an article.</span></span>  <span data-ttu-id="90e9b-321">包含文件主要用作文章其余内容的补充内容。</span><span class="sxs-lookup"><span data-stu-id="90e9b-321">Includes are meant to be supplemental to the content in the rest of the article.</span></span>

### <a name="selectors"></a><span data-ttu-id="90e9b-322">选择器</span><span class="sxs-lookup"><span data-stu-id="90e9b-322">Selectors</span></span>

<span data-ttu-id="90e9b-323">当你创作具有多种风格的同一篇技术文章时，请在文章中使用选择器，从而跨技术或平台解决实现上的差异。</span><span class="sxs-lookup"><span data-stu-id="90e9b-323">Use selectors in technical articles when you author multiple flavors of the same article, to address differences in implementation across technologies or platforms.</span></span> <span data-ttu-id="90e9b-324">通常，这最适用于开发人员的移动平台内容。</span><span class="sxs-lookup"><span data-stu-id="90e9b-324">This is typically most applicable to our mobile platform content for developers.</span></span> <span data-ttu-id="90e9b-325">Markdig 中目前有两种类型的选择器，单选择器和多选择器。</span><span class="sxs-lookup"><span data-stu-id="90e9b-325">There are currently two different types of selectors in Markdig, a single selector and a multi-selector.</span></span>

<span data-ttu-id="90e9b-326">由于选择的每篇文章中都会出现相同的选择器 Markdown，因此建议将文章的选择器放在一个包含文件中。</span><span class="sxs-lookup"><span data-stu-id="90e9b-326">Because the same selector Markdown goes in each article in the selection, we recommend placing the selector for your article in an include.</span></span> <span data-ttu-id="90e9b-327">然后，可以在使用相同选择器的所有文章中引用该包含文件。</span><span class="sxs-lookup"><span data-stu-id="90e9b-327">Then you can reference that include in all your articles that use the same selector.</span></span>

### <a name="code-snippets"></a><span data-ttu-id="90e9b-328">代码片段</span><span class="sxs-lookup"><span data-stu-id="90e9b-328">Code snippets</span></span>

<span data-ttu-id="90e9b-329">Markdig 支持通过代码片段扩展以一种高级方式将代码加入文章中。</span><span class="sxs-lookup"><span data-stu-id="90e9b-329">Markdig supports advanced inclusion of code in an article, via its code snippet extension.</span></span> <span data-ttu-id="90e9b-330">它提供了一种高级的呈现方式，这种方式基于 GFM 功能（例如编程语言选择和语法着色）以及以下一些出色的功能生成：</span><span class="sxs-lookup"><span data-stu-id="90e9b-330">It provides advanced rendering that builds on GFM features such as programming language selection and syntax coloring, plus nice features such as:</span></span>

- <span data-ttu-id="90e9b-331">通过外部存储库加入集中式代码示例/片段。</span><span class="sxs-lookup"><span data-stu-id="90e9b-331">Inclusion of centralized code samples/snippets from an external repository.</span></span>
- <span data-ttu-id="90e9b-332">选项卡式 UI，可采用不同语言显示多个版本的代码示例。</span><span class="sxs-lookup"><span data-stu-id="90e9b-332">Tabbed UI to show multiple versions of code samples in different languages.</span></span>

## <a name="gotchas-and-troubleshooting"></a><span data-ttu-id="90e9b-333">难题和故障排除</span><span class="sxs-lookup"><span data-stu-id="90e9b-333">Gotchas and troubleshooting</span></span>

### <a name="alt-text"></a><span data-ttu-id="90e9b-334">替换文字</span><span class="sxs-lookup"><span data-stu-id="90e9b-334">Alt text</span></span>

<span data-ttu-id="90e9b-335">无法正确显示带下划线的替换文字。</span><span class="sxs-lookup"><span data-stu-id="90e9b-335">Alt text that contains underscores won't be rendered properly.</span></span> <span data-ttu-id="90e9b-336">例如，与使用以下下划线相比：</span><span class="sxs-lookup"><span data-stu-id="90e9b-336">For example, instead of using this:</span></span>

```markdown
![ADextension_2FA_Configure_Step4] (./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

<span data-ttu-id="90e9b-337">转义下划线，如下所示：</span><span class="sxs-lookup"><span data-stu-id="90e9b-337">Escape the underscores like this:</span></span>

```markdown
![ADextension\_2FA\_Configure\_Step4] (./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

### <a name="apostrophes-and-quotation-marks"></a><span data-ttu-id="90e9b-338">撇号和引号</span><span class="sxs-lookup"><span data-stu-id="90e9b-338">Apostrophes and quotation marks</span></span>

<span data-ttu-id="90e9b-339">如果将文本从 Word 复制到 Markdown 编辑器，文本可能包含“弯”撇号或弯引号。</span><span class="sxs-lookup"><span data-stu-id="90e9b-339">If you copy from Word into a Markdown editor, the text might contain "smart" (curly) apostrophes or quotation marks.</span></span> <span data-ttu-id="90e9b-340">需要将这些内容编码或更改为基本撇号或单引号。</span><span class="sxs-lookup"><span data-stu-id="90e9b-340">These need to be encoded or changed to basic apostrophes or quotation marks.</span></span> <span data-ttu-id="90e9b-341">否则，在发布文件时，最终将得到：Itâ€™s</span><span class="sxs-lookup"><span data-stu-id="90e9b-341">Otherwise, you end up with things like this when the file is published: Itâ€™s</span></span>

<span data-ttu-id="90e9b-342">下面是关于这些“弯”版本标点符号的编码：</span><span class="sxs-lookup"><span data-stu-id="90e9b-342">Here are the encodings for the "smart" versions of these punctuation marks:</span></span>

- <span data-ttu-id="90e9b-343">左（开）引号：`&#8220;`</span><span class="sxs-lookup"><span data-stu-id="90e9b-343">Left (opening) quotation mark: `&#8220;`</span></span>
- <span data-ttu-id="90e9b-344">右（闭）引号：`&#8221;`</span><span class="sxs-lookup"><span data-stu-id="90e9b-344">Right (closing) quotation mark: `&#8221;`</span></span>
- <span data-ttu-id="90e9b-345">右单（闭）引号/撇号：`&#8217;`</span><span class="sxs-lookup"><span data-stu-id="90e9b-345">Right (closing) single quotation mark or apostrophe: `&#8217;`</span></span>
- <span data-ttu-id="90e9b-346">左单（开）引号（很少使用）：`&#8216;`</span><span class="sxs-lookup"><span data-stu-id="90e9b-346">Left (opening) single quotation mark (rarely used): `&#8216;`</span></span>

### <a name="angle-brackets"></a><span data-ttu-id="90e9b-347">尖括号</span><span class="sxs-lookup"><span data-stu-id="90e9b-347">Angle brackets</span></span>

<span data-ttu-id="90e9b-348">如果在文件中的文本（不是代码）里使用尖括号（例如要表示占位符），则需要对尖括号手动编码。</span><span class="sxs-lookup"><span data-stu-id="90e9b-348">If you use angle brackets in text (not code) in your file--for example, to denote a placeholder--you need to manually encode the angle brackets.</span></span> <span data-ttu-id="90e9b-349">否则，Markdown 会认为它们是一个 HTML 标记。</span><span class="sxs-lookup"><span data-stu-id="90e9b-349">Otherwise, Markdown thinks that they're intended to be an HTML tag.</span></span>

<span data-ttu-id="90e9b-350">例如，将 `<script name>` 编码为 `&lt;script name&gt;`</span><span class="sxs-lookup"><span data-stu-id="90e9b-350">For example, encode `<script name>` as `&lt;script name&gt;`</span></span>

## <a name="see-also"></a><span data-ttu-id="90e9b-351">另请参阅</span><span class="sxs-lookup"><span data-stu-id="90e9b-351">See also</span></span>

### <a name="markdown-resources"></a><span data-ttu-id="90e9b-352">Markdown 资源</span><span class="sxs-lookup"><span data-stu-id="90e9b-352">Markdown resources</span></span>

- [<span data-ttu-id="90e9b-353">Markdown 简介</span><span class="sxs-lookup"><span data-stu-id="90e9b-353">Introduction to Markdown</span></span>](https://daringfireball.net/projects/markdown/syntax)
- [<span data-ttu-id="90e9b-354">Docs Markdown 备忘单</span><span class="sxs-lookup"><span data-stu-id="90e9b-354">Docs Markdown cheat sheet</span></span>](./media/documents/markdown-cheatsheet.pdf?raw=true)
- [<span data-ttu-id="90e9b-355">GitHub 的 Markdown 基础知识</span><span class="sxs-lookup"><span data-stu-id="90e9b-355">GitHub's Markdown Basics</span></span>](https://help.github.com/articles/markdown-basics/)
