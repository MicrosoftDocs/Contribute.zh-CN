---
title: 如何使用 Markdown 撰写 Docs
description: 本文提供用于撰写 docs.microsoft.com 文章的 Markdown 语言的基础知识和参考信息。
ms.date: 07/13/2017
ms.openlocfilehash: ef75ffd59b75db5757822642f651d863906cf14c
ms.sourcegitcommit: 18c271ebec920bb976a4bc901f4ab8c1d36b02fa
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/19/2018
ms.locfileid: "53615826"
---
# <a name="how-to-use-markdown-for-writing-docs"></a><span data-ttu-id="aa313-103">如何使用 Markdown 撰写 Docs</span><span class="sxs-lookup"><span data-stu-id="aa313-103">How to use Markdown for writing Docs</span></span>

<span data-ttu-id="aa313-104">[Docs.microsoft.com](http://docs.microsoft.com) 文章采用名为 [Markdown](https://daringfireball.net/projects/markdown/) 的轻型标记语言撰写，这种语言可读性强且简单易学。</span><span class="sxs-lookup"><span data-stu-id="aa313-104">[Docs.microsoft.com](http://docs.microsoft.com) articles are written in a lightweight markup language called [Markdown](https://daringfireball.net/projects/markdown/), which is both easy to read and easy to learn.</span></span> <span data-ttu-id="aa313-105">正因为如此，Markdown 已迅速成为行业标准。</span><span class="sxs-lookup"><span data-stu-id="aa313-105">Because of this, it has quickly become an industry standard.</span></span>

<span data-ttu-id="aa313-106">由于 Doc 内容存储在 GitHub 中，因此可以使用 Markdown 超集（称为 [GitHub 风格的 Markdown (GFM)](https://help.github.com/categories/writing-on-github/)），它为常用格式需求提供了附加功能。</span><span class="sxs-lookup"><span data-stu-id="aa313-106">Since Docs content is stored in GitHub, it can use a superset of Markdown called [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/), which provides additional functionality for common formatting needs.</span></span> <span data-ttu-id="aa313-107">此外， Open Publishing Services (OPS) 还将实现 Markdig Markdown 分析程序。</span><span class="sxs-lookup"><span data-stu-id="aa313-107">Additionally, Open Publishing Services (OPS) implements Markdig Markdown Parser.</span></span> <span data-ttu-id="aa313-108">Markdig 与 GFM 高度兼容，并添加了实现 Docs 特定功能的功能。</span><span class="sxs-lookup"><span data-stu-id="aa313-108">Markdig is highly compatible with GFM, adding functionality to enable Docs-specific features.</span></span>

* <span data-ttu-id="aa313-109">Markdig 是一种适用于 .NET 的 Markdown 分析程序，它运行快速、功能强大且兼容 CommonMark。</span><span class="sxs-lookup"><span data-stu-id="aa313-109">Markdig is a fast, powerful, CommonMark compliant, extensible Markdown processor for .NET.</span></span>
* https://github.com/lunet-io/markdig
* <span data-ttu-id="aa313-110">更好的社区支持</span><span class="sxs-lookup"><span data-stu-id="aa313-110">Better community support</span></span>
* <span data-ttu-id="aa313-111">更好的标准支持</span><span class="sxs-lookup"><span data-stu-id="aa313-111">Better standards support</span></span>

## <a name="markdown-basics"></a><span data-ttu-id="aa313-112">Markdown 基础知识</span><span class="sxs-lookup"><span data-stu-id="aa313-112">Markdown basics</span></span>

### <a name="headings"></a><span data-ttu-id="aa313-113">标题</span><span class="sxs-lookup"><span data-stu-id="aa313-113">Headings</span></span>

<span data-ttu-id="aa313-114">要创建标题，请使用井号标记 (#)，如下所示：</span><span class="sxs-lookup"><span data-stu-id="aa313-114">To create a heading, you use a hash mark (#), as follows:</span></span>

```markdown
# This is heading 1
## This is heading 2
### This is heading 3
#### This is heading 4
```

<span data-ttu-id="aa313-115">应使用 atx 样式完成标题，即在行的开头使用 1-6 个哈希字符 (#) 指示标题，对应 HTML 标题级别 H1 到 H6。</span><span class="sxs-lookup"><span data-stu-id="aa313-115">Headings should be done using atx-style, that is, use 1-6 hash characters (#) at the start of the line to indicate a heading, corresponding to HTML headings levels H1 through H6.</span></span> <span data-ttu-id="aa313-116">上述示例使用的是一级到四级的标题。</span><span class="sxs-lookup"><span data-stu-id="aa313-116">Examples of first- through fourth-level headers are used above.</span></span>

<span data-ttu-id="aa313-117">主题中只能有一个一级标题 (H1)，将显示为页面内标题。</span><span class="sxs-lookup"><span data-stu-id="aa313-117">There **must** be only one first-level heading (H1) in your topic, which will be displayed as the on-page title.</span></span>

<span data-ttu-id="aa313-118">如果标题以 `#` 字符结尾，则需要在末尾添加额外的 `#` 字符，使标题正确呈现。</span><span class="sxs-lookup"><span data-stu-id="aa313-118">If your heading finishes with a `#` character, you need to add an extra `#` character in the end in order for the title to render correctly.</span></span> <span data-ttu-id="aa313-119">例如，`# Async Programming in F# #`。</span><span class="sxs-lookup"><span data-stu-id="aa313-119">For example, `# Async Programming in F# #`.</span></span>

<span data-ttu-id="aa313-120">二级标题将生成页面内 TOC，在页面内标题下方的“本文内容”中显示。</span><span class="sxs-lookup"><span data-stu-id="aa313-120">Second-level headings will generate the on-page TOC that appears in the "In this article" section underneath the on-page title.</span></span>

### <a name="bold-and-italic-text"></a><span data-ttu-id="aa313-121">粗体和斜体文本</span><span class="sxs-lookup"><span data-stu-id="aa313-121">Bold and italic text</span></span>

<span data-ttu-id="aa313-122">要将文本设置为粗体格式，请用两个星号括住文本：</span><span class="sxs-lookup"><span data-stu-id="aa313-122">To format text as **bold**, you enclose it in two asterisks:</span></span>

```markdown
This text is **bold**.
```

<span data-ttu-id="aa313-123">要将文本设置为斜体格式，请用一个星号括住文本：</span><span class="sxs-lookup"><span data-stu-id="aa313-123">To format text as *italic*, you enclose it in a single asterisk:</span></span>

```markdown
This text is *italic*.
```

<span data-ttu-id="aa313-124">要将文本同时设置为粗体和斜体格式，请用三个星号括住文本：</span><span class="sxs-lookup"><span data-stu-id="aa313-124">To format text as both ***bold and italic***, you enclose it in three asterisks:</span></span>

```markdown
This is text is both ***bold and italic***.
```

### <a name="blockquotes"></a><span data-ttu-id="aa313-125">块引用</span><span class="sxs-lookup"><span data-stu-id="aa313-125">Blockquotes</span></span>

<span data-ttu-id="aa313-126">块引用使用 `>` 字符创建：</span><span class="sxs-lookup"><span data-stu-id="aa313-126">Blockquotes are created using the `>` character:</span></span>

```markdown
> The drought had lasted now for ten million years, and the reign of the terrible lizards had long since ended. Here on the Equator, in the continent which would one day be known as Africa, the battle for existence had reached a new climax of ferocity, and the victor was not yet in sight. In this barren and desiccated land, only the small or the swift or the fierce could flourish, or even hope to survive.
```

<span data-ttu-id="aa313-127">上述示例的呈现如下所示：</span><span class="sxs-lookup"><span data-stu-id="aa313-127">The preceding example renders as follows:</span></span>

> <span data-ttu-id="aa313-128">干旱迄今为止已持续一千万年，恐怖蜥蜴的统治时代早已结束。</span><span class="sxs-lookup"><span data-stu-id="aa313-128">The drought had lasted now for ten million years, and the reign of the terrible lizards had long since ended.</span></span> <span data-ttu-id="aa313-129">赤道上，在将有一天会以“非洲”闻名的大陆上，生存的战斗已经达到新一轮残暴的高潮，胜负未分。</span><span class="sxs-lookup"><span data-stu-id="aa313-129">Here on the Equator, in the continent which would one day be known as Africa, the battle for existence had reached a new climax of ferocity, and the victor was not yet in sight.</span></span> <span data-ttu-id="aa313-130">在这片贫瘠、干枯的土地上，只有体型较小或动作迅捷或凶猛的物种才能繁荣，乃至于有希望幸存。</span><span class="sxs-lookup"><span data-stu-id="aa313-130">In this barren and desiccated land, only the small or the swift or the fierce could flourish, or even hope to survive.</span></span>

### <a name="lists"></a><span data-ttu-id="aa313-131">列表</span><span class="sxs-lookup"><span data-stu-id="aa313-131">Lists</span></span>

#### <a name="unordered-list"></a><span data-ttu-id="aa313-132">无序列表</span><span class="sxs-lookup"><span data-stu-id="aa313-132">Unordered list</span></span>

<span data-ttu-id="aa313-133">要为无序列表/项目符号列表设置格式，可以使用星号或短划线。</span><span class="sxs-lookup"><span data-stu-id="aa313-133">To format an unordered/bulleted list, you can use either asterisks or dashes.</span></span> <span data-ttu-id="aa313-134">例如，以下 Markdown：</span><span class="sxs-lookup"><span data-stu-id="aa313-134">For example, the following Markdown:</span></span>

```markdown
- List item 1
- List item 2
- List item 3
```

<span data-ttu-id="aa313-135">将显示为：</span><span class="sxs-lookup"><span data-stu-id="aa313-135">will be rendered as:</span></span>

- <span data-ttu-id="aa313-136">列表项目 1</span><span class="sxs-lookup"><span data-stu-id="aa313-136">List item 1</span></span>
- <span data-ttu-id="aa313-137">列表项目 2</span><span class="sxs-lookup"><span data-stu-id="aa313-137">List item 2</span></span>
- <span data-ttu-id="aa313-138">列表项目 3</span><span class="sxs-lookup"><span data-stu-id="aa313-138">List item 3</span></span>

<span data-ttu-id="aa313-139">要将一个列表嵌套在另一个列表中，请缩进子列表项。</span><span class="sxs-lookup"><span data-stu-id="aa313-139">To nest a list within another list, indent the child list items.</span></span> <span data-ttu-id="aa313-140">例如，以下 Markdown：</span><span class="sxs-lookup"><span data-stu-id="aa313-140">For example, the following Markdown:</span></span>

```markdown
- List item 1
  - List item A
  - List item B
- List item 2
```

<span data-ttu-id="aa313-141">将显示为：</span><span class="sxs-lookup"><span data-stu-id="aa313-141">will be rendered as:</span></span>

- <span data-ttu-id="aa313-142">列表项目 1</span><span class="sxs-lookup"><span data-stu-id="aa313-142">List item 1</span></span>
  - <span data-ttu-id="aa313-143">列表项目 A</span><span class="sxs-lookup"><span data-stu-id="aa313-143">List item A</span></span>
  - <span data-ttu-id="aa313-144">列表项目 B</span><span class="sxs-lookup"><span data-stu-id="aa313-144">List item B</span></span>
- <span data-ttu-id="aa313-145">列表项目 2</span><span class="sxs-lookup"><span data-stu-id="aa313-145">List item 2</span></span>

#### <a name="ordered-list"></a><span data-ttu-id="aa313-146">有序列表</span><span class="sxs-lookup"><span data-stu-id="aa313-146">Ordered list</span></span>

<span data-ttu-id="aa313-147">要设置有序/分阶段列表的格式，可以使用相应的编号。</span><span class="sxs-lookup"><span data-stu-id="aa313-147">To format an ordered/stepwise list, you use corresponding numbers.</span></span> <span data-ttu-id="aa313-148">例如，以下 Markdown：</span><span class="sxs-lookup"><span data-stu-id="aa313-148">For example, the following Markdown:</span></span>

```markdown
1. First instruction
1. Second instruction
1. Third instruction
```

<span data-ttu-id="aa313-149">将显示为：</span><span class="sxs-lookup"><span data-stu-id="aa313-149">will be rendered as:</span></span>

1. <span data-ttu-id="aa313-150">第一个说明</span><span class="sxs-lookup"><span data-stu-id="aa313-150">First instruction</span></span>
2. <span data-ttu-id="aa313-151">第二个说明</span><span class="sxs-lookup"><span data-stu-id="aa313-151">Second instruction</span></span>
3. <span data-ttu-id="aa313-152">第三个说明</span><span class="sxs-lookup"><span data-stu-id="aa313-152">Third instruction</span></span>

<span data-ttu-id="aa313-153">要将一个列表嵌套在另一个列表中，请缩进子列表项。</span><span class="sxs-lookup"><span data-stu-id="aa313-153">To nest a list within another list, indent the child list items.</span></span> <span data-ttu-id="aa313-154">例如，以下 Markdown：</span><span class="sxs-lookup"><span data-stu-id="aa313-154">For example, the following Markdown:</span></span>

```markdown
1. First instruction
   1. Sub-instruction
   1. Sub-instruction
1. Second instruction
```

<span data-ttu-id="aa313-155">将显示为：</span><span class="sxs-lookup"><span data-stu-id="aa313-155">will be rendered as:</span></span>

1. <span data-ttu-id="aa313-156">第一个说明</span><span class="sxs-lookup"><span data-stu-id="aa313-156">First instruction</span></span>
   1. <span data-ttu-id="aa313-157">辅助说明</span><span class="sxs-lookup"><span data-stu-id="aa313-157">Sub-instruction</span></span>
   2. <span data-ttu-id="aa313-158">辅助说明</span><span class="sxs-lookup"><span data-stu-id="aa313-158">Sub-instruction</span></span>
2. <span data-ttu-id="aa313-159">第二个说明</span><span class="sxs-lookup"><span data-stu-id="aa313-159">Second instruction</span></span>

<span data-ttu-id="aa313-160">注意：我们对所有条目</span><span class="sxs-lookup"><span data-stu-id="aa313-160">Note that we use '1.'</span></span> <span data-ttu-id="aa313-161">均使用“1.”。</span><span class="sxs-lookup"><span data-stu-id="aa313-161">for all entries.</span></span> <span data-ttu-id="aa313-162">当后续更新包括新步骤或要删除现有步骤时，这样更易于评审差异。</span><span class="sxs-lookup"><span data-stu-id="aa313-162">It makes diffs easier to review when later updates include new steps or remove existing steps.</span></span>

### <a name="tables"></a><span data-ttu-id="aa313-163">表格</span><span class="sxs-lookup"><span data-stu-id="aa313-163">Tables</span></span>

<span data-ttu-id="aa313-164">表格不属于核心 Markdown 规范，但是它们受 GFM 支持。</span><span class="sxs-lookup"><span data-stu-id="aa313-164">Tables are not part of the core Markdown specification, but GFM supports them.</span></span> <span data-ttu-id="aa313-165">可以使用竖线 (|) 和连字符 (-) 字符创建表格。</span><span class="sxs-lookup"><span data-stu-id="aa313-165">You can create tables by using the pipe (|) and hyphen (-) characters.</span></span> <span data-ttu-id="aa313-166">连字符用于创建每列的标题，而竖线用于分隔每列。</span><span class="sxs-lookup"><span data-stu-id="aa313-166">Hyphens create each column's header, while pipes separate each column.</span></span> <span data-ttu-id="aa313-167">请在表格前面加入一个空行，使它能够正确显示。</span><span class="sxs-lookup"><span data-stu-id="aa313-167">Include a blank line before your table so it's rendered correctly.</span></span>

<span data-ttu-id="aa313-168">例如，以下 Markdown：</span><span class="sxs-lookup"><span data-stu-id="aa313-168">For example, the following Markdown:</span></span>

```markdown
| Fun                  | With                 | Tables          |
| :------------------- | -------------------: |:---------------:|
| left-aligned column  | right-aligned column | centered column |
| $100                 | $100                 | $100            |
| $10                  | $10                  | $10             |
| $1                   | $1                   | $1              |
```

<span data-ttu-id="aa313-169">将显示为：</span><span class="sxs-lookup"><span data-stu-id="aa313-169">will be rendered as:</span></span>

| <span data-ttu-id="aa313-170">趣</span><span class="sxs-lookup"><span data-stu-id="aa313-170">Fun</span></span>                  | <span data-ttu-id="aa313-171">含</span><span class="sxs-lookup"><span data-stu-id="aa313-171">With</span></span>                 | <span data-ttu-id="aa313-172">表格</span><span class="sxs-lookup"><span data-stu-id="aa313-172">Tables</span></span>          |
| :------------------- | -------------------: |:---------------:|
| <span data-ttu-id="aa313-173">左对齐列</span><span class="sxs-lookup"><span data-stu-id="aa313-173">left-aligned column</span></span>  | <span data-ttu-id="aa313-174">右对齐列</span><span class="sxs-lookup"><span data-stu-id="aa313-174">right-aligned column</span></span> | <span data-ttu-id="aa313-175">居中列</span><span class="sxs-lookup"><span data-stu-id="aa313-175">centered column</span></span> |
| <span data-ttu-id="aa313-176">$100</span><span class="sxs-lookup"><span data-stu-id="aa313-176">$100</span></span>                 | <span data-ttu-id="aa313-177">$100</span><span class="sxs-lookup"><span data-stu-id="aa313-177">$100</span></span>                 | <span data-ttu-id="aa313-178">$100</span><span class="sxs-lookup"><span data-stu-id="aa313-178">$100</span></span>            |
| <span data-ttu-id="aa313-179">$10</span><span class="sxs-lookup"><span data-stu-id="aa313-179">$10</span></span>                  | <span data-ttu-id="aa313-180">$10</span><span class="sxs-lookup"><span data-stu-id="aa313-180">$10</span></span>                  | <span data-ttu-id="aa313-181">$10</span><span class="sxs-lookup"><span data-stu-id="aa313-181">$10</span></span>             |
| <span data-ttu-id="aa313-182">$1</span><span class="sxs-lookup"><span data-stu-id="aa313-182">$1</span></span>                   | <span data-ttu-id="aa313-183">$1</span><span class="sxs-lookup"><span data-stu-id="aa313-183">$1</span></span>                   | <span data-ttu-id="aa313-184">$1</span><span class="sxs-lookup"><span data-stu-id="aa313-184">$1</span></span>              |

<span data-ttu-id="aa313-185">有关创建表格的详细信息，请参阅：</span><span class="sxs-lookup"><span data-stu-id="aa313-185">For more information on creating tables, see:</span></span>

- <span data-ttu-id="aa313-186">Markdig [表格换行功能](#table-wrapping)，有助于设置宽表格的格式。</span><span class="sxs-lookup"><span data-stu-id="aa313-186">The Markdig [table wrapping feature](#table-wrapping), which can help with formatting of wide tables.</span></span>
- <span data-ttu-id="aa313-187">GitHub 的[使用表格整理信息](https://help.github.com/articles/organizing-information-with-tables/)。</span><span class="sxs-lookup"><span data-stu-id="aa313-187">GitHub's [Organizing information with tables](https://help.github.com/articles/organizing-information-with-tables/).</span></span>
- <span data-ttu-id="aa313-188">[Markdown 表格生成器](https://www.tablesgenerator.com/markdown_tables) Web 应用。</span><span class="sxs-lookup"><span data-stu-id="aa313-188">The [Markdown Tables Generator](https://www.tablesgenerator.com/markdown_tables) web app.</span></span>
- <span data-ttu-id="aa313-189">[Adam Pritchard 的 Markdown 备忘单](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#wiki-tables)。</span><span class="sxs-lookup"><span data-stu-id="aa313-189">[Adam Pritchard's Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#wiki-tables).</span></span>
- <span data-ttu-id="aa313-190">[Michel Fortin 的 Markdown Extra](https://michelf.ca/projects/php-markdown/extra/#table)。</span><span class="sxs-lookup"><span data-stu-id="aa313-190">[Michel Fortin's Markdown Extra](https://michelf.ca/projects/php-markdown/extra/#table).</span></span>
- <span data-ttu-id="aa313-191">[将 HTML 表转换为 Markdown 格式](https://jmalarcon.github.io/markdowntables/)。</span><span class="sxs-lookup"><span data-stu-id="aa313-191">[Convert HTML tables to Markdown](https://jmalarcon.github.io/markdowntables/).</span></span>

### <a name="links"></a><span data-ttu-id="aa313-192">链接</span><span class="sxs-lookup"><span data-stu-id="aa313-192">Links</span></span>

<span data-ttu-id="aa313-193">Markdown 的内联链接语法由两部分组成：`[link text]` 部分，这是要创建为超链接的文本；后跟 `(file-name.md)` 部分，这是要链接到的 URL 或者文件名：</span><span class="sxs-lookup"><span data-stu-id="aa313-193">The Markdown syntax for an inline link consists of the `[link text]` portion, which is the text that will be hyperlinked, followed by the `(file-name.md)` portion, which is the URL or file name that's being linked to:</span></span>

 `[link text](file-name.md)`

<span data-ttu-id="aa313-194">有关链接的详细信息，请参阅：</span><span class="sxs-lookup"><span data-stu-id="aa313-194">For more information on linking, see:</span></span>

- <span data-ttu-id="aa313-195">[Markdown 语法指南](https://daringfireball.net/projects/markdown/syntax#link)，详细了解 Markdown 的基本链接支持相关信息。</span><span class="sxs-lookup"><span data-stu-id="aa313-195">The [Markdown syntax guide](https://daringfireball.net/projects/markdown/syntax#link) for details on Markdown's base linking support.</span></span>
- <span data-ttu-id="aa313-196">参阅本指南的[链接](how-to-write-links.md)部分，深入了解 Markdig 提供的其他链接语法。</span><span class="sxs-lookup"><span data-stu-id="aa313-196">The [Links](how-to-write-links.md) section of this guide for details on the additional linking syntax that Markdig provides.</span></span>

### <a name="code-snippets"></a><span data-ttu-id="aa313-197">代码片段</span><span class="sxs-lookup"><span data-stu-id="aa313-197">Code snippets</span></span>

<span data-ttu-id="aa313-198">Markdown 不仅支持将代码片段内联在某个句子中，还支持将它作为单独的“隔离”块放置在两个句子之间。</span><span class="sxs-lookup"><span data-stu-id="aa313-198">Markdown supports the placement of code snippets both inline in a sentence and as a separate "fenced" block between sentences.</span></span> <span data-ttu-id="aa313-199">有关详细信息，请参阅：</span><span class="sxs-lookup"><span data-stu-id="aa313-199">For details, see:</span></span>

- [<span data-ttu-id="aa313-200">Markdown 代码块本机支持</span><span class="sxs-lookup"><span data-stu-id="aa313-200">Markdown's native support for code blocks</span></span>](https://daringfireball.net/projects/markdown/syntax#precode)
- [<span data-ttu-id="aa313-201">针对代码隔离和语法高亮显示的 GFM 支持</span><span class="sxs-lookup"><span data-stu-id="aa313-201">GFM support for code fencing and syntax highlighting</span></span>](https://help.github.com/articles/creating-and-highlighting-code-blocks/)

<span data-ttu-id="aa313-202">借助隔离代码块，可以轻松实现代码片段的语法高亮显示。</span><span class="sxs-lookup"><span data-stu-id="aa313-202">Fenced code blocks are an easy way to enable syntax highlighting for your code snippets.</span></span> <span data-ttu-id="aa313-203">隔离代码块的一般格式为：</span><span class="sxs-lookup"><span data-stu-id="aa313-203">The general format for fenced code blocks is:</span></span>

    ```alias
    ...
    your code goes in here
    ...
    ```

<span data-ttu-id="aa313-204">开头的三个撇号 (\`) 字符后面的别名定义要使用的语法高亮显示。</span><span class="sxs-lookup"><span data-stu-id="aa313-204">The alias after the initial three backtick (\`) characters defines the syntax highlighting to be used.</span></span> <span data-ttu-id="aa313-205">下面列出了 Docs 内容中常用的编程语言以及匹配的标签：</span><span class="sxs-lookup"><span data-stu-id="aa313-205">The following is a list of commonly used programming languages in Docs content and the matching label:</span></span>

<span data-ttu-id="aa313-206">这些语言支持友好名称并且大多数都可以突出显示语言。</span><span class="sxs-lookup"><span data-stu-id="aa313-206">These languages have friendly name support and most have language highlighting.</span></span>

|<span data-ttu-id="aa313-207">名称</span><span class="sxs-lookup"><span data-stu-id="aa313-207">Name</span></span>|<span data-ttu-id="aa313-208">Markdown 标签</span><span class="sxs-lookup"><span data-stu-id="aa313-208">Markdown Label</span></span>|
|-----|-------|
|<span data-ttu-id="aa313-209">.NET 控制台</span><span class="sxs-lookup"><span data-stu-id="aa313-209">.NET Console</span></span>|<span data-ttu-id="aa313-210">dotnetcli</span><span class="sxs-lookup"><span data-stu-id="aa313-210">dotnetcli</span></span>|
|<span data-ttu-id="aa313-211">ASP.NET (C#)</span><span class="sxs-lookup"><span data-stu-id="aa313-211">ASP.NET (C#)</span></span>|<span data-ttu-id="aa313-212">aspx-csharp</span><span class="sxs-lookup"><span data-stu-id="aa313-212">aspx-csharp</span></span>|
|<span data-ttu-id="aa313-213">ASP.NET (VB)</span><span class="sxs-lookup"><span data-stu-id="aa313-213">ASP.NET (VB)</span></span>|<span data-ttu-id="aa313-214">aspx-vb</span><span class="sxs-lookup"><span data-stu-id="aa313-214">aspx-vb</span></span>|
|<span data-ttu-id="aa313-215">AzCopy</span><span class="sxs-lookup"><span data-stu-id="aa313-215">AzCopy</span></span>|<span data-ttu-id="aa313-216">azcopy</span><span class="sxs-lookup"><span data-stu-id="aa313-216">azcopy</span></span>|
|<span data-ttu-id="aa313-217">Azure CLI</span><span class="sxs-lookup"><span data-stu-id="aa313-217">Azure CLI</span></span>|<span data-ttu-id="aa313-218">azurecli</span><span class="sxs-lookup"><span data-stu-id="aa313-218">azurecli</span></span>|
|<span data-ttu-id="aa313-219">Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="aa313-219">Azure PowerShell</span></span>|<span data-ttu-id="aa313-220">azurepowershell</span><span class="sxs-lookup"><span data-stu-id="aa313-220">azurepowershell</span></span>|
|<span data-ttu-id="aa313-221">C++</span><span class="sxs-lookup"><span data-stu-id="aa313-221">C++</span></span>|<span data-ttu-id="aa313-222">cpp</span><span class="sxs-lookup"><span data-stu-id="aa313-222">cpp</span></span>|
|<span data-ttu-id="aa313-223">C++/CX</span><span class="sxs-lookup"><span data-stu-id="aa313-223">C++/CX</span></span>|<span data-ttu-id="aa313-224">cppcx</span><span class="sxs-lookup"><span data-stu-id="aa313-224">cppcx</span></span>|
|<span data-ttu-id="aa313-225">C++/WinRT</span><span class="sxs-lookup"><span data-stu-id="aa313-225">C++/WinRT</span></span>|<span data-ttu-id="aa313-226">cppwinrt</span><span class="sxs-lookup"><span data-stu-id="aa313-226">cppwinrt</span></span>|
|<span data-ttu-id="aa313-227">C#</span><span class="sxs-lookup"><span data-stu-id="aa313-227">C#</span></span>|<span data-ttu-id="aa313-228">csharp</span><span class="sxs-lookup"><span data-stu-id="aa313-228">csharp</span></span>|
|<span data-ttu-id="aa313-229">浏览器中的 C#</span><span class="sxs-lookup"><span data-stu-id="aa313-229">C# in browser</span></span>|<span data-ttu-id="aa313-230">csharp-interactive</span><span class="sxs-lookup"><span data-stu-id="aa313-230">csharp-interactive</span></span>|
|<span data-ttu-id="aa313-231">控制台</span><span class="sxs-lookup"><span data-stu-id="aa313-231">Console</span></span>|<span data-ttu-id="aa313-232">console</span><span class="sxs-lookup"><span data-stu-id="aa313-232">console</span></span>|
|<span data-ttu-id="aa313-233">CSHTML</span><span class="sxs-lookup"><span data-stu-id="aa313-233">CSHTML</span></span>|<span data-ttu-id="aa313-234">cshtml</span><span class="sxs-lookup"><span data-stu-id="aa313-234">cshtml</span></span>|
|<span data-ttu-id="aa313-235">DAX</span><span class="sxs-lookup"><span data-stu-id="aa313-235">DAX</span></span>|<span data-ttu-id="aa313-236">dax</span><span class="sxs-lookup"><span data-stu-id="aa313-236">dax</span></span>|
|<span data-ttu-id="aa313-237">F#</span><span class="sxs-lookup"><span data-stu-id="aa313-237">F#</span></span>|<span data-ttu-id="aa313-238">fsharp</span><span class="sxs-lookup"><span data-stu-id="aa313-238">fsharp</span></span>|
|<span data-ttu-id="aa313-239">Go</span><span class="sxs-lookup"><span data-stu-id="aa313-239">Go</span></span>|<span data-ttu-id="aa313-240">go</span><span class="sxs-lookup"><span data-stu-id="aa313-240">go</span></span>|
|<span data-ttu-id="aa313-241">HTML</span><span class="sxs-lookup"><span data-stu-id="aa313-241">HTML</span></span>|<span data-ttu-id="aa313-242">html</span><span class="sxs-lookup"><span data-stu-id="aa313-242">html</span></span>|
|<span data-ttu-id="aa313-243">HTTP</span><span class="sxs-lookup"><span data-stu-id="aa313-243">HTTP</span></span>|<span data-ttu-id="aa313-244">http</span><span class="sxs-lookup"><span data-stu-id="aa313-244">http</span></span>|
|<span data-ttu-id="aa313-245">Java</span><span class="sxs-lookup"><span data-stu-id="aa313-245">Java</span></span>|<span data-ttu-id="aa313-246">java</span><span class="sxs-lookup"><span data-stu-id="aa313-246">java</span></span>|
|<span data-ttu-id="aa313-247">JavaScript</span><span class="sxs-lookup"><span data-stu-id="aa313-247">JavaScript</span></span>|<span data-ttu-id="aa313-248">javascript</span><span class="sxs-lookup"><span data-stu-id="aa313-248">javascript</span></span>|
|<span data-ttu-id="aa313-249">JSON</span><span class="sxs-lookup"><span data-stu-id="aa313-249">JSON</span></span>|<span data-ttu-id="aa313-250">json</span><span class="sxs-lookup"><span data-stu-id="aa313-250">json</span></span>|
|<span data-ttu-id="aa313-251">Markdown</span><span class="sxs-lookup"><span data-stu-id="aa313-251">Markdown</span></span>|<span data-ttu-id="aa313-252">md</span><span class="sxs-lookup"><span data-stu-id="aa313-252">md</span></span>|
|<span data-ttu-id="aa313-253">NodeJS</span><span class="sxs-lookup"><span data-stu-id="aa313-253">NodeJS</span></span>|<span data-ttu-id="aa313-254">nodejs</span><span class="sxs-lookup"><span data-stu-id="aa313-254">nodejs</span></span>|
|<span data-ttu-id="aa313-255">Objective-C</span><span class="sxs-lookup"><span data-stu-id="aa313-255">Objective-C</span></span>|<span data-ttu-id="aa313-256">objc</span><span class="sxs-lookup"><span data-stu-id="aa313-256">objc</span></span>|
|<span data-ttu-id="aa313-257">OData</span><span class="sxs-lookup"><span data-stu-id="aa313-257">OData</span></span>|<span data-ttu-id="aa313-258">odata</span><span class="sxs-lookup"><span data-stu-id="aa313-258">odata</span></span>|
|<span data-ttu-id="aa313-259">PHP</span><span class="sxs-lookup"><span data-stu-id="aa313-259">PHP</span></span>|<span data-ttu-id="aa313-260">php</span><span class="sxs-lookup"><span data-stu-id="aa313-260">php</span></span>|
|<span data-ttu-id="aa313-261">PowerApps（小数点分隔符）</span><span class="sxs-lookup"><span data-stu-id="aa313-261">PowerApps (dot decimal separator)</span></span>|<span data-ttu-id="aa313-262">powerapps-dot</span><span class="sxs-lookup"><span data-stu-id="aa313-262">powerapps-dot</span></span>|
|<span data-ttu-id="aa313-263">PowerApps（逗号分隔符）</span><span class="sxs-lookup"><span data-stu-id="aa313-263">PowerApps (comma decimal separator)</span></span>|<span data-ttu-id="aa313-264">powerapps-comma</span><span class="sxs-lookup"><span data-stu-id="aa313-264">powerapps-comma</span></span>|
|<span data-ttu-id="aa313-265">PowerShell</span><span class="sxs-lookup"><span data-stu-id="aa313-265">PowerShell</span></span>|<span data-ttu-id="aa313-266">powershell</span><span class="sxs-lookup"><span data-stu-id="aa313-266">powershell</span></span>|
|<span data-ttu-id="aa313-267">Python</span><span class="sxs-lookup"><span data-stu-id="aa313-267">Python</span></span>|<span data-ttu-id="aa313-268">python</span><span class="sxs-lookup"><span data-stu-id="aa313-268">python</span></span>|
|<span data-ttu-id="aa313-269">Q#</span><span class="sxs-lookup"><span data-stu-id="aa313-269">Q#</span></span>|<span data-ttu-id="aa313-270">qsharp</span><span class="sxs-lookup"><span data-stu-id="aa313-270">qsharp</span></span>|
|<span data-ttu-id="aa313-271">R</span><span class="sxs-lookup"><span data-stu-id="aa313-271">R</span></span>|<span data-ttu-id="aa313-272">r</span><span class="sxs-lookup"><span data-stu-id="aa313-272">r</span></span>|
|<span data-ttu-id="aa313-273">Ruby</span><span class="sxs-lookup"><span data-stu-id="aa313-273">Ruby</span></span>|<span data-ttu-id="aa313-274">ruby</span><span class="sxs-lookup"><span data-stu-id="aa313-274">ruby</span></span>|
|<span data-ttu-id="aa313-275">SQL</span><span class="sxs-lookup"><span data-stu-id="aa313-275">SQL</span></span>|<span data-ttu-id="aa313-276">sql</span><span class="sxs-lookup"><span data-stu-id="aa313-276">sql</span></span>|
|<span data-ttu-id="aa313-277">Swift</span><span class="sxs-lookup"><span data-stu-id="aa313-277">Swift</span></span>|<span data-ttu-id="aa313-278">swift</span><span class="sxs-lookup"><span data-stu-id="aa313-278">swift</span></span>|
|<span data-ttu-id="aa313-279">TypeScript</span><span class="sxs-lookup"><span data-stu-id="aa313-279">TypeScript</span></span>|<span data-ttu-id="aa313-280">typescript</span><span class="sxs-lookup"><span data-stu-id="aa313-280">typescript</span></span>|
|<span data-ttu-id="aa313-281">VB</span><span class="sxs-lookup"><span data-stu-id="aa313-281">VB</span></span>|<span data-ttu-id="aa313-282">vb</span><span class="sxs-lookup"><span data-stu-id="aa313-282">vb</span></span>|
|<span data-ttu-id="aa313-283">VSTS CLI</span><span class="sxs-lookup"><span data-stu-id="aa313-283">VSTS CLI</span></span>|<span data-ttu-id="aa313-284">vstscli</span><span class="sxs-lookup"><span data-stu-id="aa313-284">vstscli</span></span>|
|<span data-ttu-id="aa313-285">XAML</span><span class="sxs-lookup"><span data-stu-id="aa313-285">XAML</span></span>|<span data-ttu-id="aa313-286">xaml</span><span class="sxs-lookup"><span data-stu-id="aa313-286">xaml</span></span>|
|<span data-ttu-id="aa313-287">XML</span><span class="sxs-lookup"><span data-stu-id="aa313-287">XML</span></span>|<span data-ttu-id="aa313-288">xml</span><span class="sxs-lookup"><span data-stu-id="aa313-288">xml</span></span>|

<span data-ttu-id="aa313-289">`csharp-interactive` 名称指定 C# 语言，以及从浏览器中运行示例的能力。</span><span class="sxs-lookup"><span data-stu-id="aa313-289">The `csharp-interactive` name specifies the C# language, and the ability to run the samples from the browser.</span></span> <span data-ttu-id="aa313-290">这些代码片段在 Docker 容器中进行编译和执行，并且该程序执行的结果在用户浏览器窗口中显示。</span><span class="sxs-lookup"><span data-stu-id="aa313-290">These snippets are compiled and executed in a Docker container, and the results of that program execution are displayed in the user's browser window.</span></span>

#### <a name="example-c"></a><span data-ttu-id="aa313-291">示例：C\#</span><span class="sxs-lookup"><span data-stu-id="aa313-291">Example: C\#</span></span>

<span data-ttu-id="aa313-292">__Markdown__</span><span class="sxs-lookup"><span data-stu-id="aa313-292">__Markdown__</span></span>

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

<span data-ttu-id="aa313-293">__呈现__</span><span class="sxs-lookup"><span data-stu-id="aa313-293">__Render__</span></span>

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

#### <a name="example-sql"></a><span data-ttu-id="aa313-294">示例：SQL</span><span class="sxs-lookup"><span data-stu-id="aa313-294">Example: SQL</span></span>

<span data-ttu-id="aa313-295">__Markdown__</span><span class="sxs-lookup"><span data-stu-id="aa313-295">__Markdown__</span></span>

    ```sql
    CREATE TABLE T1 (
      c1 int PRIMARY KEY,
      c2 varchar(50) SPARSE NULL
    );
    ```

<span data-ttu-id="aa313-296">__呈现__</span><span class="sxs-lookup"><span data-stu-id="aa313-296">__Render__</span></span>

```sql
CREATE TABLE T1 (
  c1 int PRIMARY KEY,
  c2 varchar(50) SPARSE NULL
);
```

## <a name="ops-custom-markdown-extensions"></a><span data-ttu-id="aa313-297">OPS 自定义 Markdown 扩展</span><span class="sxs-lookup"><span data-stu-id="aa313-297">OPS custom Markdown extensions</span></span>

> [!NOTE]
> <span data-ttu-id="aa313-298">Open Publishing Services(OPS) 可实现 Markdown Markdig 分析程序，它与 GitHub 风格的 Markdown (GFM) 高度兼容。</span><span class="sxs-lookup"><span data-stu-id="aa313-298">Open Publishing Services (OPS) implements a Markdig Parser for Markdown, which is highly compatible with GitHub Flavored Markdown (GFM).</span></span> <span data-ttu-id="aa313-299">Markdig 通过 Markdown 扩展添加一些功能。</span><span class="sxs-lookup"><span data-stu-id="aa313-299">Markdig adds some functionality through Markdown extensions.</span></span> <span data-ttu-id="aa313-300">就这一点而言，本指南从完整的《OPS 创作指南》中选用了几篇文章，以供参考。</span><span class="sxs-lookup"><span data-stu-id="aa313-300">As such, selected articles from the full OPS Authoring Guide are included in this guide for reference.</span></span> <span data-ttu-id="aa313-301">（例如，请参阅目录中的“Markdig 和 Markdown 扩展”以及“代码片段”。）</span><span class="sxs-lookup"><span data-stu-id="aa313-301">(For example, see "Markdig and Markdown extensions" and "Code snippets" in the table of contents.)</span></span>

<span data-ttu-id="aa313-302">Doc 文章使用 GFM 完成大多文章的格式设置，如段落、链接、列表和标题。</span><span class="sxs-lookup"><span data-stu-id="aa313-302">Docs articles use GFM for most article formatting, such as paragraphs, links, lists, and headings.</span></span> <span data-ttu-id="aa313-303">要想实现更丰富的格式设置功能，文章可以使用 Markdig 功能，例如：</span><span class="sxs-lookup"><span data-stu-id="aa313-303">For richer formatting, articles can use Markdig features such as:</span></span>

- <span data-ttu-id="aa313-304">备注块</span><span class="sxs-lookup"><span data-stu-id="aa313-304">Note blocks</span></span>
- <span data-ttu-id="aa313-305">包含文件</span><span class="sxs-lookup"><span data-stu-id="aa313-305">Include files</span></span>
- <span data-ttu-id="aa313-306">选择器</span><span class="sxs-lookup"><span data-stu-id="aa313-306">Selectors</span></span>
- <span data-ttu-id="aa313-307">嵌入视频</span><span class="sxs-lookup"><span data-stu-id="aa313-307">Embedded videos</span></span>
- <span data-ttu-id="aa313-308">代码片段/示例</span><span class="sxs-lookup"><span data-stu-id="aa313-308">Code snippets/samples</span></span>

<span data-ttu-id="aa313-309">如需完整列表，请参阅目录中的“Markdig 和 Markdown 扩展”以及“代码片段”。</span><span class="sxs-lookup"><span data-stu-id="aa313-309">For the complete list, refer to "Markdig and Markdown extensions" and "Code snippets" in the table of contents.</span></span>

### <a name="note-blocks"></a><span data-ttu-id="aa313-310">备注块</span><span class="sxs-lookup"><span data-stu-id="aa313-310">Note blocks</span></span>

<span data-ttu-id="aa313-311">可以从 4 种类型的备注块中进行选择来吸引对特定内容的注意：</span><span class="sxs-lookup"><span data-stu-id="aa313-311">You can choose from four types of note blocks to draw attention to specific content:</span></span>

- <span data-ttu-id="aa313-312">注意</span><span class="sxs-lookup"><span data-stu-id="aa313-312">NOTE</span></span>
- <span data-ttu-id="aa313-313">警告</span><span class="sxs-lookup"><span data-stu-id="aa313-313">WARNING</span></span>
- <span data-ttu-id="aa313-314">提示</span><span class="sxs-lookup"><span data-stu-id="aa313-314">TIP</span></span>
- <span data-ttu-id="aa313-315">重要说明</span><span class="sxs-lookup"><span data-stu-id="aa313-315">IMPORTANT</span></span>

<span data-ttu-id="aa313-316">总之，应谨慎使用备注块，因为它们可能会造成干扰。</span><span class="sxs-lookup"><span data-stu-id="aa313-316">In general, note blocks should be used sparingly because they can be disruptive.</span></span> <span data-ttu-id="aa313-317">尽管备注块也支持代码块、图像、列表以及链接，但最好尽量保持备注块简单明了。</span><span class="sxs-lookup"><span data-stu-id="aa313-317">Although they also support code blocks, images, lists, and links, try to keep your note blocks simple and straightforward.</span></span>

<span data-ttu-id="aa313-318">示例：</span><span class="sxs-lookup"><span data-stu-id="aa313-318">Examples:</span></span>

```markdown
> [!NOTE]
> This is a NOTE

> [!WARNING]
> This is a WARNING

> [!TIP]
> This is a TIP

> [!IMPORTANT]
> This is IMPORTANT
```

<span data-ttu-id="aa313-319">这些呈现结果如下：</span><span class="sxs-lookup"><span data-stu-id="aa313-319">These render as follows:</span></span>

> [!NOTE]
> <span data-ttu-id="aa313-320">这是一条备注</span><span class="sxs-lookup"><span data-stu-id="aa313-320">This is a NOTE</span></span>

> [!WARNING]
> <span data-ttu-id="aa313-321">这是一条警告</span><span class="sxs-lookup"><span data-stu-id="aa313-321">This is a WARNING</span></span>

> [!TIP]
> <span data-ttu-id="aa313-322">这是一条提示</span><span class="sxs-lookup"><span data-stu-id="aa313-322">This is a TIP</span></span>

> [!IMPORTANT]
> <span data-ttu-id="aa313-323">这是一条重要提示</span><span class="sxs-lookup"><span data-stu-id="aa313-323">This is IMPORTANT</span></span>

### <a name="include-files"></a><span data-ttu-id="aa313-324">包含文件</span><span class="sxs-lookup"><span data-stu-id="aa313-324">Include files</span></span>

<span data-ttu-id="aa313-325">如果有需要加入文章文件中的可重用的文本或图像文件，可以通过 Markdig 文件的包含文件功能使用对“包含”文件的引用。</span><span class="sxs-lookup"><span data-stu-id="aa313-325">When you have reusable text or image files that need to be included in article files, you can use a reference to the "include" file via the Markdig file include feature.</span></span> <span data-ttu-id="aa313-326">此功能指示 OPS 在创建时将该文件加入文章文件中，使它成为已发布文章的一部分。</span><span class="sxs-lookup"><span data-stu-id="aa313-326">This feature instructs OPS to include the file in your article file at build time, making it part of your published article.</span></span> <span data-ttu-id="aa313-327">有 3 种类型的包含引用可帮助你重用内容：</span><span class="sxs-lookup"><span data-stu-id="aa313-327">Three types of include references are available to help you reuse content:</span></span>

- <span data-ttu-id="aa313-328">内联：重用内联在其他句子中的常用文本片段。</span><span class="sxs-lookup"><span data-stu-id="aa313-328">Inline: Reuse a common text snippet inline with within another sentence.</span></span>
- <span data-ttu-id="aa313-329">块：将整个 Markdown 文件作为一个块重用，嵌套在文章的某一部分中。</span><span class="sxs-lookup"><span data-stu-id="aa313-329">Block: Reuse an entire Markdown file as a block, nested within a section of an article.</span></span>
- <span data-ttu-id="aa313-330">图像：此方法可以在 Doc 中实现标准图像加入。</span><span class="sxs-lookup"><span data-stu-id="aa313-330">Image: This is how standard image inclusion is implemented in Docs.</span></span>

<span data-ttu-id="aa313-331">“内联”和“块”包含文件是简单的 Markdown (.md) 文件。</span><span class="sxs-lookup"><span data-stu-id="aa313-331">An inline or block include file is just a simple Markdown (.md) file.</span></span> <span data-ttu-id="aa313-332">它可以包含任何有效的 Markdown。</span><span class="sxs-lookup"><span data-stu-id="aa313-332">It can contain any valid Markdown.</span></span> <span data-ttu-id="aa313-333">所有包含 Markdown 文件都应置于存储库根目录的[常用 `/includes` 子目录](git-github-fundamentals.md#includes-subdirectory) 中。</span><span class="sxs-lookup"><span data-stu-id="aa313-333">All include Markdown files should be placed in a [common `/includes` subdirectory](git-github-fundamentals.md#includes-subdirectory), in the root of the repository.</span></span> <span data-ttu-id="aa313-334">发布文章时，加入的文件会无缝集成到其中。</span><span class="sxs-lookup"><span data-stu-id="aa313-334">When the article is published, the included file is seamlessly integrated into it.</span></span>

<span data-ttu-id="aa313-335">包含文件的要求和注意事项如下：</span><span class="sxs-lookup"><span data-stu-id="aa313-335">Here are requirements and considerations for include files:</span></span>

- <span data-ttu-id="aa313-336">每当需要在多篇文章中显示相同的文本时，均可使用包含功能文件。</span><span class="sxs-lookup"><span data-stu-id="aa313-336">Use an include file whenever you need the same text to appear in multiple articles.</span></span>
- <span data-ttu-id="aa313-337">块包含文件适用于大篇幅内容，比如一个或者两个段落、共享过程或者共享章节。</span><span class="sxs-lookup"><span data-stu-id="aa313-337">Use a block include reference for significant amounts of content--a paragraph or two, a shared procedure, or a shared section.</span></span> <span data-ttu-id="aa313-338">请勿将它们用于小于一个句子的内容。</span><span class="sxs-lookup"><span data-stu-id="aa313-338">Do not use them for anything smaller than a sentence.</span></span>
- <span data-ttu-id="aa313-339">包含文件不会在文章的 GitHub 渲染视图中显示，因为它们依赖于 Markdig 扩展。</span><span class="sxs-lookup"><span data-stu-id="aa313-339">Include references won't be rendered in the GitHub rendered view of your article, because they rely on Markdig extensions.</span></span> <span data-ttu-id="aa313-340">它们在发布后才会显示。</span><span class="sxs-lookup"><span data-stu-id="aa313-340">They'll be rendered only after publication.</span></span>
- <span data-ttu-id="aa313-341">确保包含文件中的所有文本都是完整的句子或者段落，并且与引用该包含文件的文章的前后文没有关联。</span><span class="sxs-lookup"><span data-stu-id="aa313-341">Ensure that all the text in an include file is written in complete sentences or phrases that do not depend on preceding text or following text in the article that references the include file.</span></span> <span data-ttu-id="aa313-342">如果不遵循此指导原则，则会在文章中创建无法转换的字符串，进而破坏本地化体验。</span><span class="sxs-lookup"><span data-stu-id="aa313-342">Ignoring this guidance creates an untranslatable string in the article that breaks the localized experience.</span></span>
- <span data-ttu-id="aa313-343">请勿在其他包含文件中嵌入包含引用。</span><span class="sxs-lookup"><span data-stu-id="aa313-343">Don't embed include references within other include files.</span></span> <span data-ttu-id="aa313-344">不支持此操作。</span><span class="sxs-lookup"><span data-stu-id="aa313-344">They are not supported.</span></span>
- <span data-ttu-id="aa313-345">将媒体文件置于特定于包含文件子目录的媒体文件夹中，例如，`<repo>`/includes/媒体文件夹。</span><span class="sxs-lookup"><span data-stu-id="aa313-345">Place media files in a media folder that's specific to the include subdirectory--for instance, the `<repo>`/includes/media folder.</span></span> <span data-ttu-id="aa313-346">媒体目录不应在根目录中包含任何图片。</span><span class="sxs-lookup"><span data-stu-id="aa313-346">The media directory should not contain any images in its root.</span></span> <span data-ttu-id="aa313-347">如果包含文件中没有图像，则不需要相应的媒体目录。</span><span class="sxs-lookup"><span data-stu-id="aa313-347">If the include file does not have images, a corresponding media directory is not required.</span></span>
- <span data-ttu-id="aa313-348">对于常规文章，请勿在各包含文件之间共享媒体。</span><span class="sxs-lookup"><span data-stu-id="aa313-348">As with regular articles, don't share media between include files.</span></span> <span data-ttu-id="aa313-349">对于每个包含文件和文章，请使用具有唯一名称的单独文件。</span><span class="sxs-lookup"><span data-stu-id="aa313-349">Use a separate file with a unique name for each include file and article.</span></span> <span data-ttu-id="aa313-350">将媒体文件存储在与包含文件关联的媒体文件夹中。</span><span class="sxs-lookup"><span data-stu-id="aa313-350">Store the media file in the media folder that's associated with the include file.</span></span>
- <span data-ttu-id="aa313-351">请勿将包含文件用作文章的唯一内容。</span><span class="sxs-lookup"><span data-stu-id="aa313-351">Don't use an include file as the only content of an article.</span></span>  <span data-ttu-id="aa313-352">包含文件主要用作文章其余内容的补充内容。</span><span class="sxs-lookup"><span data-stu-id="aa313-352">Include files are meant to be supplemental to the content in the rest of the article.</span></span>

<span data-ttu-id="aa313-353">示例：</span><span class="sxs-lookup"><span data-stu-id="aa313-353">Example:</span></span>

```markdown
[!INCLUDE[sample include file](../includes/sampleinclude.md)]
```

### <a name="selectors"></a><span data-ttu-id="aa313-354">选择器</span><span class="sxs-lookup"><span data-stu-id="aa313-354">Selectors</span></span>

<span data-ttu-id="aa313-355">当你创作具有多种风格的同一篇技术文章时，请在文章中使用选择器，从而跨技术或平台解决实现上的差异。</span><span class="sxs-lookup"><span data-stu-id="aa313-355">Use selectors in technical articles when you author multiple flavors of the same article, to  address differences in implementation across technologies or platforms.</span></span> <span data-ttu-id="aa313-356">通常，这最适用于开发人员的移动平台内容。</span><span class="sxs-lookup"><span data-stu-id="aa313-356">This is typically most applicable to our mobile platform content for developers.</span></span> <span data-ttu-id="aa313-357">Markdig 中目前有两种类型的选择器，单选择器和多选择器。</span><span class="sxs-lookup"><span data-stu-id="aa313-357">There are currently two different types of selectors in Markdig, a single selector and a multi-selector.</span></span>

<span data-ttu-id="aa313-358">由于选择的每篇文章中都会出现相同的选择器 Markdown，因此建议将文章的选择器放在包含文件中。</span><span class="sxs-lookup"><span data-stu-id="aa313-358">Because the same selector Markdown goes in each article in the selection, we recommend placing the selector for your article in an include file.</span></span> <span data-ttu-id="aa313-359">然后，可以在使用相同选择器的所有文章中引用该包含文件。</span><span class="sxs-lookup"><span data-stu-id="aa313-359">Then you can reference that include file in all your articles that use the same selector.</span></span>

<span data-ttu-id="aa313-360">下面展示了一个示例选择器：</span><span class="sxs-lookup"><span data-stu-id="aa313-360">The following shows an example selector:</span></span>

```markdown
> [!div class="op_single_selector"]
- [macOS](../docs/core/tutorials/using-on-macos.md)
- [Windows](../docs/core/tutorials/with-visual-studio.md)
```

<span data-ttu-id="aa313-361">可在 [Azure 文档](https://docs.microsoft.com/azure/expressroute/expressroute-howto-circuit-classic)中查看有效的选择器示例。</span><span class="sxs-lookup"><span data-stu-id="aa313-361">You can see an example of selectors in action at the [Azure docs](https://docs.microsoft.com/azure/expressroute/expressroute-howto-circuit-classic).</span></span>

### <a name="code-include-references"></a><span data-ttu-id="aa313-362">代码包含引用</span><span class="sxs-lookup"><span data-stu-id="aa313-362">Code include references</span></span>

<span data-ttu-id="aa313-363">Markdig 支持通过代码片段扩展以一种高级方式将代码加入文章中。</span><span class="sxs-lookup"><span data-stu-id="aa313-363">Markdig supports advanced inclusion of code in an article, via its code snippet extension.</span></span> <span data-ttu-id="aa313-364">它提供了一种高级的呈现方式，这种方式基于 GFM 功能（例如编程语言选择和语法着色）以及以下一些出色的功能生成：</span><span class="sxs-lookup"><span data-stu-id="aa313-364">It provides advanced rendering that builds on GFM features such as programming language selection and syntax coloring, plus nice features such as:</span></span>

- <span data-ttu-id="aa313-365">通过外部存储库加入集中式代码示例/片段。</span><span class="sxs-lookup"><span data-stu-id="aa313-365">Inclusion of centralized code samples/snippets from an external repository.</span></span>
- <span data-ttu-id="aa313-366">选项卡式 UI，可采用不同语言显示多个版本的代码示例。</span><span class="sxs-lookup"><span data-stu-id="aa313-366">Tabbed UI to show multiple versions of code samples in different languages.</span></span>

## <a name="gotchas-and-troubleshooting"></a><span data-ttu-id="aa313-367">难题和故障排除</span><span class="sxs-lookup"><span data-stu-id="aa313-367">Gotchas and troubleshooting</span></span>

### <a name="alt-text"></a><span data-ttu-id="aa313-368">替换文字</span><span class="sxs-lookup"><span data-stu-id="aa313-368">Alt text</span></span>

<span data-ttu-id="aa313-369">无法正确显示带下划线的替换文字。</span><span class="sxs-lookup"><span data-stu-id="aa313-369">Alt text that contains underscores won't be rendered properly.</span></span> <span data-ttu-id="aa313-370">例如，与使用以下下划线相比：</span><span class="sxs-lookup"><span data-stu-id="aa313-370">For example, instead of using this:</span></span>

```markdown
![ADextension_2FA_Configure_Step4](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

<span data-ttu-id="aa313-371">转义下划线，如下所示：</span><span class="sxs-lookup"><span data-stu-id="aa313-371">Escape the underscores like this:</span></span>

```markdown
![ADextension\_2FA\_Configure\_Step4](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

### <a name="apostrophes-and-quotation-marks"></a><span data-ttu-id="aa313-372">撇号和引号</span><span class="sxs-lookup"><span data-stu-id="aa313-372">Apostrophes and quotation marks</span></span>

<span data-ttu-id="aa313-373">如果将文本从 Word 复制到 Markdown 编辑器，文本可能包含“弯”撇号或弯引号。</span><span class="sxs-lookup"><span data-stu-id="aa313-373">If you copy from Word into a Markdown editor, the text might contain "smart" (curly) apostrophes or quotation marks.</span></span> <span data-ttu-id="aa313-374">需要将这些内容编码或更改为基本撇号或单引号。</span><span class="sxs-lookup"><span data-stu-id="aa313-374">These need to be encoded or changed to basic apostrophes or quotation marks.</span></span> <span data-ttu-id="aa313-375">否则，发布文件时，最终将得到：Itâ€™s</span><span class="sxs-lookup"><span data-stu-id="aa313-375">Otherwise, you end up with things like this when the file is published: Itâ€™s</span></span>

<span data-ttu-id="aa313-376">下面是关于这些“弯”版本标点符号的编码：</span><span class="sxs-lookup"><span data-stu-id="aa313-376">Here are the encodings for the "smart" versions of these punctuation marks:</span></span>

- <span data-ttu-id="aa313-377">左（开）引号：`&#8220;`</span><span class="sxs-lookup"><span data-stu-id="aa313-377">Left (opening) quotation mark: `&#8220;`</span></span>
- <span data-ttu-id="aa313-378">右（闭）引号：`&#8221;`</span><span class="sxs-lookup"><span data-stu-id="aa313-378">Right (closing) quotation mark: `&#8221;`</span></span>
- <span data-ttu-id="aa313-379">右单（闭）引号/撇号：`&#8217;`</span><span class="sxs-lookup"><span data-stu-id="aa313-379">Right (closing) single quotation mark or apostrophe: `&#8217;`</span></span>
- <span data-ttu-id="aa313-380">左单（开）引号（很少使用）：`&#8216;`</span><span class="sxs-lookup"><span data-stu-id="aa313-380">Left (opening) single quotation mark (rarely used): `&#8216;`</span></span>

### <a name="angle-brackets"></a><span data-ttu-id="aa313-381">尖括号</span><span class="sxs-lookup"><span data-stu-id="aa313-381">Angle brackets</span></span>

<span data-ttu-id="aa313-382">通常使用尖括号来表示占位符。</span><span class="sxs-lookup"><span data-stu-id="aa313-382">It is common to use angle brackets to denote a placeholder.</span></span> <span data-ttu-id="aa313-383">在文本（而不是代码）中执行此操作时，必须对尖括号进行编码。</span><span class="sxs-lookup"><span data-stu-id="aa313-383">When you do this in text (not code), you must encode the angle brackets.</span></span> <span data-ttu-id="aa313-384">否则，Markdown 会认为它们是一个 HTML 标记。</span><span class="sxs-lookup"><span data-stu-id="aa313-384">Otherwise, Markdown thinks that they're intended to be an HTML tag.</span></span>

<span data-ttu-id="aa313-385">例如，将 `<script name>` 编码为 `&lt;script name&gt;`</span><span class="sxs-lookup"><span data-stu-id="aa313-385">For example, encode `<script name>` as `&lt;script name&gt;`</span></span>

## <a name="see-also"></a><span data-ttu-id="aa313-386">另请参阅：</span><span class="sxs-lookup"><span data-stu-id="aa313-386">See also:</span></span>

### <a name="markdown-resources"></a><span data-ttu-id="aa313-387">Markdown 资源</span><span class="sxs-lookup"><span data-stu-id="aa313-387">Markdown resources</span></span>

- [<span data-ttu-id="aa313-388">Markdown 简介</span><span class="sxs-lookup"><span data-stu-id="aa313-388">Introduction to Markdown</span></span>](https://daringfireball.net/projects/markdown/syntax)
- [<span data-ttu-id="aa313-389">Docs Markdown 备忘单</span><span class="sxs-lookup"><span data-stu-id="aa313-389">Docs Markdown cheat sheet</span></span>](./media/documents/markdown-cheatsheet.pdf?raw=true)
- [<span data-ttu-id="aa313-390">GitHub 的 Markdown 基础知识</span><span class="sxs-lookup"><span data-stu-id="aa313-390">GitHub's Markdown Basics</span></span>](https://help.github.com/articles/markdown-basics/)
- [<span data-ttu-id="aa313-391">Markdown 指南</span><span class="sxs-lookup"><span data-stu-id="aa313-391">The Markdown Guide</span></span>](https://www.markdownguide.org/)
