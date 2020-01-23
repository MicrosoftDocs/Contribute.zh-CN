---
title: 如何使用 Markdown 撰写 Docs
description: 本文提供用于撰写 docs.microsoft.com 文章的 Markdown 语言的基础知识和参考信息。
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
ms.date: 03/26/2019
ms.openlocfilehash: 086972acaef9647709fbe43f07c07abde71c7d9f
ms.sourcegitcommit: fd92198ec2d0ce2d6687b6f1521a82b3fefc60e0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/16/2020
ms.locfileid: "76111066"
---
# <a name="how-to-use-markdown-for-writing-docs"></a><span data-ttu-id="92e55-103">如何使用 Markdown 撰写 Docs</span><span class="sxs-lookup"><span data-stu-id="92e55-103">How to use Markdown for writing Docs</span></span>

<span data-ttu-id="92e55-104">[Docs.microsoft.com](https://docs.microsoft.com) 文章采用名为 [Markdown](https://daringfireball.net/projects/markdown/) 的轻型标记语言撰写，这种语言可读性强且简单易学。</span><span class="sxs-lookup"><span data-stu-id="92e55-104">[Docs.microsoft.com](https://docs.microsoft.com) articles are written in a lightweight markup language called [Markdown](https://daringfireball.net/projects/markdown/), which is both easy to read and easy to learn.</span></span> <span data-ttu-id="92e55-105">正因为如此，Markdown 已迅速成为行业标准。</span><span class="sxs-lookup"><span data-stu-id="92e55-105">Because of this, it has quickly become an industry standard.</span></span> <span data-ttu-id="92e55-106">Docs 站点使用 Markdown 的 [Markdig 风格](#markdown-flavor)。</span><span class="sxs-lookup"><span data-stu-id="92e55-106">The docs site uses the [Markdig flavor](#markdown-flavor) of Markdown.</span></span>


## <a name="markdown-basics"></a><span data-ttu-id="92e55-107">Markdown 基础知识</span><span class="sxs-lookup"><span data-stu-id="92e55-107">Markdown basics</span></span>

### <a name="headings"></a><span data-ttu-id="92e55-108">标题</span><span class="sxs-lookup"><span data-stu-id="92e55-108">Headings</span></span>

<span data-ttu-id="92e55-109">要创建标题，请使用井号标记 (#)，如下所示：</span><span class="sxs-lookup"><span data-stu-id="92e55-109">To create a heading, you use a hash mark (#), as follows:</span></span>

```md
# This is heading 1
## This is heading 2
### This is heading 3
#### This is heading 4
```

<span data-ttu-id="92e55-110">应使用 atx 样式完成标题，即在行的开头使用 1-6 个哈希字符 (#) 指示标题，对应 HTML 标题级别 H1 到 H6。</span><span class="sxs-lookup"><span data-stu-id="92e55-110">Headings should be done using atx-style, that is, use 1-6 hash characters (#) at the start of the line to indicate a heading, corresponding to HTML headings levels H1 through H6.</span></span> <span data-ttu-id="92e55-111">上述示例使用的是一级到四级的标题。</span><span class="sxs-lookup"><span data-stu-id="92e55-111">Examples of first- through fourth-level headers are used above.</span></span>

<span data-ttu-id="92e55-112">主题中只能有一个一级标题 (H1)，将显示为页面内标题  。</span><span class="sxs-lookup"><span data-stu-id="92e55-112">There **must** be only one first-level heading (H1) in your topic, which will be displayed as the on-page title.</span></span>

<span data-ttu-id="92e55-113">如果标题以 `#` 字符结尾，则需要在末尾添加额外的 `#` 字符，使标题正确呈现。</span><span class="sxs-lookup"><span data-stu-id="92e55-113">If your heading finishes with a `#` character, you need to add an extra `#` character in the end in order for the title to render correctly.</span></span> <span data-ttu-id="92e55-114">例如，`# Async Programming in F# #`。</span><span class="sxs-lookup"><span data-stu-id="92e55-114">For example, `# Async Programming in F# #`.</span></span>

<span data-ttu-id="92e55-115">二级标题将生成页面内 TOC，在页面内标题下方的“本文内容”中显示。</span><span class="sxs-lookup"><span data-stu-id="92e55-115">Second-level headings will generate the on-page TOC that appears in the "In this article" section underneath the on-page title.</span></span>

### <a name="bold-and-italic-text"></a><span data-ttu-id="92e55-116">粗体和斜体文本</span><span class="sxs-lookup"><span data-stu-id="92e55-116">Bold and italic text</span></span>

<span data-ttu-id="92e55-117">要将文本设置为粗体格式，请用两个星号括住文本  ：</span><span class="sxs-lookup"><span data-stu-id="92e55-117">To format text as **bold**, you enclose it in two asterisks:</span></span>

```md
This text is **bold**.
```

<span data-ttu-id="92e55-118">要将文本设置为斜体格式，请用一个星号括住文本  ：</span><span class="sxs-lookup"><span data-stu-id="92e55-118">To format text as *italic*, you enclose it in a single asterisk:</span></span>

```md
This text is *italic*.
```

<span data-ttu-id="92e55-119">要将文本同时设置为粗体和斜体格式，请用三个星号括住文本：</span><span class="sxs-lookup"><span data-stu-id="92e55-119">To format text as both ***bold and italic***, you enclose it in three asterisks:</span></span>

```md
This is text is both ***bold and italic***.
```

### <a name="blockquotes"></a><span data-ttu-id="92e55-120">块引用</span><span class="sxs-lookup"><span data-stu-id="92e55-120">Blockquotes</span></span>

<span data-ttu-id="92e55-121">块引用使用 `>` 字符创建：</span><span class="sxs-lookup"><span data-stu-id="92e55-121">Blockquotes are created using the `>` character:</span></span>

```md
> The drought had lasted now for ten million years, and the reign of the terrible lizards had long since ended. Here on the Equator, in the continent which would one day be known as Africa, the battle for existence had reached a new climax of ferocity, and the victor was not yet in sight. In this barren and desiccated land, only the small or the swift or the fierce could flourish, or even hope to survive.
```

<span data-ttu-id="92e55-122">上述示例的呈现如下所示：</span><span class="sxs-lookup"><span data-stu-id="92e55-122">The preceding example renders as follows:</span></span>

> <span data-ttu-id="92e55-123">干旱迄今为止已持续一千万年，恐怖蜥蜴的统治时代早已结束。</span><span class="sxs-lookup"><span data-stu-id="92e55-123">The drought had lasted now for ten million years, and the reign of the terrible lizards had long since ended.</span></span> <span data-ttu-id="92e55-124">赤道上，在将有一天会以“非洲”闻名的大陆上，生存的战斗已经达到新一轮残暴的高潮，胜负未分。</span><span class="sxs-lookup"><span data-stu-id="92e55-124">Here on the Equator, in the continent which would one day be known as Africa, the battle for existence had reached a new climax of ferocity, and the victor was not yet in sight.</span></span> <span data-ttu-id="92e55-125">在这片贫瘠、干枯的土地上，只有体型较小或动作迅捷或凶猛的物种才能繁荣，乃至于有希望幸存。</span><span class="sxs-lookup"><span data-stu-id="92e55-125">In this barren and desiccated land, only the small or the swift or the fierce could flourish, or even hope to survive.</span></span>

### <a name="lists"></a><span data-ttu-id="92e55-126">列表</span><span class="sxs-lookup"><span data-stu-id="92e55-126">Lists</span></span>

#### <a name="unordered-list"></a><span data-ttu-id="92e55-127">无序列表</span><span class="sxs-lookup"><span data-stu-id="92e55-127">Unordered list</span></span>

<span data-ttu-id="92e55-128">要为无序列表/项目符号列表设置格式，可以使用星号或短划线。</span><span class="sxs-lookup"><span data-stu-id="92e55-128">To format an unordered/bulleted list, you can use either asterisks or dashes.</span></span> <span data-ttu-id="92e55-129">例如，以下 Markdown：</span><span class="sxs-lookup"><span data-stu-id="92e55-129">For example, the following Markdown:</span></span>

```md
- List item 1
- List item 2
- List item 3
```

<span data-ttu-id="92e55-130">将显示为：</span><span class="sxs-lookup"><span data-stu-id="92e55-130">will be rendered as:</span></span>

- <span data-ttu-id="92e55-131">List item 1</span><span class="sxs-lookup"><span data-stu-id="92e55-131">List item 1</span></span>
- <span data-ttu-id="92e55-132">List item 2</span><span class="sxs-lookup"><span data-stu-id="92e55-132">List item 2</span></span>
- <span data-ttu-id="92e55-133">List item 3</span><span class="sxs-lookup"><span data-stu-id="92e55-133">List item 3</span></span>

<span data-ttu-id="92e55-134">要将一个列表嵌套在另一个列表中，请缩进子列表项。</span><span class="sxs-lookup"><span data-stu-id="92e55-134">To nest a list within another list, indent the child list items.</span></span> <span data-ttu-id="92e55-135">例如，以下 Markdown：</span><span class="sxs-lookup"><span data-stu-id="92e55-135">For example, the following Markdown:</span></span>

```md
- List item 1
  - List item A
  - List item B
- List item 2
```

<span data-ttu-id="92e55-136">将显示为：</span><span class="sxs-lookup"><span data-stu-id="92e55-136">will be rendered as:</span></span>

- <span data-ttu-id="92e55-137">List item 1</span><span class="sxs-lookup"><span data-stu-id="92e55-137">List item 1</span></span>
  - <span data-ttu-id="92e55-138">List item A</span><span class="sxs-lookup"><span data-stu-id="92e55-138">List item A</span></span>
  - <span data-ttu-id="92e55-139">List item B</span><span class="sxs-lookup"><span data-stu-id="92e55-139">List item B</span></span>
- <span data-ttu-id="92e55-140">List item 2</span><span class="sxs-lookup"><span data-stu-id="92e55-140">List item 2</span></span>

#### <a name="ordered-list"></a><span data-ttu-id="92e55-141">有序列表</span><span class="sxs-lookup"><span data-stu-id="92e55-141">Ordered list</span></span>

<span data-ttu-id="92e55-142">要设置有序/分阶段列表的格式，可以使用相应的编号。</span><span class="sxs-lookup"><span data-stu-id="92e55-142">To format an ordered/stepwise list, you use corresponding numbers.</span></span> <span data-ttu-id="92e55-143">例如，以下 Markdown：</span><span class="sxs-lookup"><span data-stu-id="92e55-143">For example, the following Markdown:</span></span>

```md
1. First instruction
1. Second instruction
1. Third instruction
```

<span data-ttu-id="92e55-144">将显示为：</span><span class="sxs-lookup"><span data-stu-id="92e55-144">will be rendered as:</span></span>

1. <span data-ttu-id="92e55-145">First instruction</span><span class="sxs-lookup"><span data-stu-id="92e55-145">First instruction</span></span>
2. <span data-ttu-id="92e55-146">Second instruction</span><span class="sxs-lookup"><span data-stu-id="92e55-146">Second instruction</span></span>
3. <span data-ttu-id="92e55-147">Third instruction</span><span class="sxs-lookup"><span data-stu-id="92e55-147">Third instruction</span></span>

<span data-ttu-id="92e55-148">要将一个列表嵌套在另一个列表中，请缩进子列表项。</span><span class="sxs-lookup"><span data-stu-id="92e55-148">To nest a list within another list, indent the child list items.</span></span> <span data-ttu-id="92e55-149">例如，以下 Markdown：</span><span class="sxs-lookup"><span data-stu-id="92e55-149">For example, the following Markdown:</span></span>

```md
1. First instruction
   1. Sub-instruction
   1. Sub-instruction
1. Second instruction
```

<span data-ttu-id="92e55-150">将显示为：</span><span class="sxs-lookup"><span data-stu-id="92e55-150">will be rendered as:</span></span>

1. <span data-ttu-id="92e55-151">First instruction</span><span class="sxs-lookup"><span data-stu-id="92e55-151">First instruction</span></span>
   1. <span data-ttu-id="92e55-152">Sub-instruction</span><span class="sxs-lookup"><span data-stu-id="92e55-152">Sub-instruction</span></span>
   2. <span data-ttu-id="92e55-153">Sub-instruction</span><span class="sxs-lookup"><span data-stu-id="92e55-153">Sub-instruction</span></span>
2. <span data-ttu-id="92e55-154">Second instruction</span><span class="sxs-lookup"><span data-stu-id="92e55-154">Second instruction</span></span>

<span data-ttu-id="92e55-155">注意：我们对所有条目</span><span class="sxs-lookup"><span data-stu-id="92e55-155">Note that we use '1.'</span></span> <span data-ttu-id="92e55-156">均使用“1.”。</span><span class="sxs-lookup"><span data-stu-id="92e55-156">for all entries.</span></span> <span data-ttu-id="92e55-157">当后续更新包括新步骤或要删除现有步骤时，这样更易于评审差异。</span><span class="sxs-lookup"><span data-stu-id="92e55-157">It makes diffs easier to review when later updates include new steps or remove existing steps.</span></span>

### <a name="tables"></a><span data-ttu-id="92e55-158">表格</span><span class="sxs-lookup"><span data-stu-id="92e55-158">Tables</span></span>

<span data-ttu-id="92e55-159">表格不属于核心 Markdown 规范，但是它们受 GFM 支持。</span><span class="sxs-lookup"><span data-stu-id="92e55-159">Tables are not part of the core Markdown specification, but GFM supports them.</span></span> <span data-ttu-id="92e55-160">可以使用竖线 (|) 和连字符 (-) 字符创建表格。</span><span class="sxs-lookup"><span data-stu-id="92e55-160">You can create tables by using the pipe (|) and hyphen (-) characters.</span></span> <span data-ttu-id="92e55-161">连字符用于创建每列的标题，而竖线用于分隔每列。</span><span class="sxs-lookup"><span data-stu-id="92e55-161">Hyphens create each column's header, while pipes separate each column.</span></span> <span data-ttu-id="92e55-162">请在表格前面加入一个空行，使它能够正确显示。</span><span class="sxs-lookup"><span data-stu-id="92e55-162">Include a blank line before your table so it's rendered correctly.</span></span>

<span data-ttu-id="92e55-163">例如，以下 Markdown：</span><span class="sxs-lookup"><span data-stu-id="92e55-163">For example, the following Markdown:</span></span>

```md
| Fun                  | With                 | Tables          |
| :------------------- | -------------------: |:---------------:|
| left-aligned column  | right-aligned column | centered column |
| $100                 | $100                 | $100            |
| $10                  | $10                  | $10             |
| $1                   | $1                   | $1              |
```

<span data-ttu-id="92e55-164">将显示为：</span><span class="sxs-lookup"><span data-stu-id="92e55-164">Will be rendered as:</span></span>

| <span data-ttu-id="92e55-165">Fun</span><span class="sxs-lookup"><span data-stu-id="92e55-165">Fun</span></span>                  | <span data-ttu-id="92e55-166">With</span><span class="sxs-lookup"><span data-stu-id="92e55-166">With</span></span>                 | <span data-ttu-id="92e55-167">Tables</span><span class="sxs-lookup"><span data-stu-id="92e55-167">Tables</span></span>          |
| :------------------- | -------------------: |:---------------:|
| <span data-ttu-id="92e55-168">left-aligned column</span><span class="sxs-lookup"><span data-stu-id="92e55-168">left-aligned column</span></span>  | <span data-ttu-id="92e55-169">right-aligned column</span><span class="sxs-lookup"><span data-stu-id="92e55-169">right-aligned column</span></span> | <span data-ttu-id="92e55-170">centered column</span><span class="sxs-lookup"><span data-stu-id="92e55-170">centered column</span></span> |
| <span data-ttu-id="92e55-171">$100</span><span class="sxs-lookup"><span data-stu-id="92e55-171">$100</span></span>                 | <span data-ttu-id="92e55-172">$100</span><span class="sxs-lookup"><span data-stu-id="92e55-172">$100</span></span>                 | <span data-ttu-id="92e55-173">$100</span><span class="sxs-lookup"><span data-stu-id="92e55-173">$100</span></span>            |
| <span data-ttu-id="92e55-174">$10</span><span class="sxs-lookup"><span data-stu-id="92e55-174">$10</span></span>                  | <span data-ttu-id="92e55-175">$10</span><span class="sxs-lookup"><span data-stu-id="92e55-175">$10</span></span>                  | <span data-ttu-id="92e55-176">$10</span><span class="sxs-lookup"><span data-stu-id="92e55-176">$10</span></span>             |
| <span data-ttu-id="92e55-177">$1</span><span class="sxs-lookup"><span data-stu-id="92e55-177">$1</span></span>                   | <span data-ttu-id="92e55-178">$1</span><span class="sxs-lookup"><span data-stu-id="92e55-178">$1</span></span>                   | <span data-ttu-id="92e55-179">$1</span><span class="sxs-lookup"><span data-stu-id="92e55-179">$1</span></span>              |

<span data-ttu-id="92e55-180">有关创建表格的详细信息，请参阅：</span><span class="sxs-lookup"><span data-stu-id="92e55-180">For more information on creating tables, see:</span></span>

- <span data-ttu-id="92e55-181">GitHub 的[使用表格整理信息](https://help.github.com/articles/organizing-information-with-tables/)。</span><span class="sxs-lookup"><span data-stu-id="92e55-181">GitHub's [Organizing information with tables](https://help.github.com/articles/organizing-information-with-tables/).</span></span>
- <span data-ttu-id="92e55-182">[Markdown 表格生成器](https://www.tablesgenerator.com/markdown_tables) Web 应用。</span><span class="sxs-lookup"><span data-stu-id="92e55-182">The [Markdown Tables Generator](https://www.tablesgenerator.com/markdown_tables) web app.</span></span>
- <span data-ttu-id="92e55-183">[Adam Pritchard 的 Markdown 备忘单](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#wiki-tables)。</span><span class="sxs-lookup"><span data-stu-id="92e55-183">[Adam Pritchard's Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#wiki-tables).</span></span>
- <span data-ttu-id="92e55-184">[Michel Fortin 的 Markdown Extra](https://michelf.ca/projects/php-markdown/extra/#table)。</span><span class="sxs-lookup"><span data-stu-id="92e55-184">[Michel Fortin's Markdown Extra](https://michelf.ca/projects/php-markdown/extra/#table).</span></span>
- <span data-ttu-id="92e55-185">[将 HTML 表转换为 Markdown 格式](https://jmalarcon.github.io/markdowntables/)。</span><span class="sxs-lookup"><span data-stu-id="92e55-185">[Convert HTML tables to Markdown](https://jmalarcon.github.io/markdowntables/).</span></span>

### <a name="links"></a><span data-ttu-id="92e55-186">链接</span><span class="sxs-lookup"><span data-stu-id="92e55-186">Links</span></span>

<span data-ttu-id="92e55-187">Markdown 的内联链接语法由两部分组成：`[link text]` 部分，这是要创建为超链接的文本；后跟 `(file-name.md)` 部分，这是要链接到的 URL 或者文件名：</span><span class="sxs-lookup"><span data-stu-id="92e55-187">The Markdown syntax for an inline link consists of the `[link text]` portion, which is the text that will be hyperlinked, followed by the `(file-name.md)` portion, which is the URL or file name that's being linked to:</span></span>

 `[link text](file-name.md)`

<span data-ttu-id="92e55-188">有关链接的详细信息，请参阅：</span><span class="sxs-lookup"><span data-stu-id="92e55-188">For more information on linking, see:</span></span>

- <span data-ttu-id="92e55-189">[Markdown 语法指南](https://daringfireball.net/projects/markdown/syntax#link)，详细了解 Markdown 的基本链接支持相关信息。</span><span class="sxs-lookup"><span data-stu-id="92e55-189">The [Markdown syntax guide](https://daringfireball.net/projects/markdown/syntax#link) for details on Markdown's base linking support.</span></span>
- <span data-ttu-id="92e55-190">参阅本指南的[链接](how-to-write-links.md)部分，深入了解 Markdig 提供的其他链接语法。</span><span class="sxs-lookup"><span data-stu-id="92e55-190">The [Links](how-to-write-links.md) section of this guide for details on the additional linking syntax that Markdig provides.</span></span>

### <a name="code-snippets"></a><span data-ttu-id="92e55-191">代码片段</span><span class="sxs-lookup"><span data-stu-id="92e55-191">Code snippets</span></span>

<span data-ttu-id="92e55-192">Markdown 不仅支持将代码片段内联在某个句子中，还支持将它作为单独的“隔离”块放置在两个句子之间。</span><span class="sxs-lookup"><span data-stu-id="92e55-192">Markdown supports the placement of code snippets both inline in a sentence and as a separate "fenced" block between sentences.</span></span> <span data-ttu-id="92e55-193">有关详细信息，请参阅：</span><span class="sxs-lookup"><span data-stu-id="92e55-193">For details, see:</span></span>

- [<span data-ttu-id="92e55-194">Markdown 代码块本机支持</span><span class="sxs-lookup"><span data-stu-id="92e55-194">Markdown's native support for code blocks</span></span>](https://daringfireball.net/projects/markdown/syntax#precode)
- [<span data-ttu-id="92e55-195">针对代码隔离和语法高亮显示的 GFM 支持</span><span class="sxs-lookup"><span data-stu-id="92e55-195">GFM support for code fencing and syntax highlighting</span></span>](https://help.github.com/articles/creating-and-highlighting-code-blocks/)

<span data-ttu-id="92e55-196">借助隔离代码块，可以轻松实现代码片段的语法高亮显示。</span><span class="sxs-lookup"><span data-stu-id="92e55-196">Fenced code blocks are an easy way to enable syntax highlighting for your code snippets.</span></span> <span data-ttu-id="92e55-197">隔离代码块的一般格式为：</span><span class="sxs-lookup"><span data-stu-id="92e55-197">The general format for fenced code blocks is:</span></span>

    ```alias
    ...
    your code goes in here
    ...
    ```

<span data-ttu-id="92e55-198">开头的三个撇号 (\`) 字符后面的别名定义要使用的语法高亮显示。</span><span class="sxs-lookup"><span data-stu-id="92e55-198">The alias after the initial three backtick (\`) characters defines the syntax highlighting to be used.</span></span> <span data-ttu-id="92e55-199">下面列出了 Docs 内容中常用的编程语言以及匹配的标签：</span><span class="sxs-lookup"><span data-stu-id="92e55-199">The following is a list of commonly used programming languages in Docs content and the matching label:</span></span>

<span data-ttu-id="92e55-200">这些语言支持友好名称并且大多数都可以突出显示语言。</span><span class="sxs-lookup"><span data-stu-id="92e55-200">These languages have friendly name support and most have language highlighting.</span></span>

|<span data-ttu-id="92e55-201">名称</span><span class="sxs-lookup"><span data-stu-id="92e55-201">Name</span></span>|<span data-ttu-id="92e55-202">Markdown 标签</span><span class="sxs-lookup"><span data-stu-id="92e55-202">Markdown Label</span></span>|
|-----|-------|
|<span data-ttu-id="92e55-203">.NET 控制台</span><span class="sxs-lookup"><span data-stu-id="92e55-203">.NET Console</span></span>|<span data-ttu-id="92e55-204">dotnetcli</span><span class="sxs-lookup"><span data-stu-id="92e55-204">dotnetcli</span></span>|
|<span data-ttu-id="92e55-205">ASP.NET (C#)</span><span class="sxs-lookup"><span data-stu-id="92e55-205">ASP.NET (C#)</span></span>|<span data-ttu-id="92e55-206">aspx-csharp</span><span class="sxs-lookup"><span data-stu-id="92e55-206">aspx-csharp</span></span>|
|<span data-ttu-id="92e55-207">ASP.NET (VB)</span><span class="sxs-lookup"><span data-stu-id="92e55-207">ASP.NET (VB)</span></span>|<span data-ttu-id="92e55-208">aspx-vb</span><span class="sxs-lookup"><span data-stu-id="92e55-208">aspx-vb</span></span>|
|<span data-ttu-id="92e55-209">AzCopy</span><span class="sxs-lookup"><span data-stu-id="92e55-209">AzCopy</span></span>|<span data-ttu-id="92e55-210">azcopy</span><span class="sxs-lookup"><span data-stu-id="92e55-210">azcopy</span></span>|
|<span data-ttu-id="92e55-211">Azure CLI</span><span class="sxs-lookup"><span data-stu-id="92e55-211">Azure CLI</span></span>|<span data-ttu-id="92e55-212">azurecli</span><span class="sxs-lookup"><span data-stu-id="92e55-212">azurecli</span></span>|
|<span data-ttu-id="92e55-213">Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="92e55-213">Azure PowerShell</span></span>|<span data-ttu-id="92e55-214">azurepowershell</span><span class="sxs-lookup"><span data-stu-id="92e55-214">azurepowershell</span></span>|
|<span data-ttu-id="92e55-215">Bash</span><span class="sxs-lookup"><span data-stu-id="92e55-215">Bash</span></span>|<span data-ttu-id="92e55-216">bash</span><span class="sxs-lookup"><span data-stu-id="92e55-216">bash</span></span>|
|<span data-ttu-id="92e55-217">C++</span><span class="sxs-lookup"><span data-stu-id="92e55-217">C++</span></span>|<span data-ttu-id="92e55-218">cpp</span><span class="sxs-lookup"><span data-stu-id="92e55-218">cpp</span></span>|
|<span data-ttu-id="92e55-219">C++/CX</span><span class="sxs-lookup"><span data-stu-id="92e55-219">C++/CX</span></span>|<span data-ttu-id="92e55-220">cppcx</span><span class="sxs-lookup"><span data-stu-id="92e55-220">cppcx</span></span>|
|<span data-ttu-id="92e55-221">C++/WinRT</span><span class="sxs-lookup"><span data-stu-id="92e55-221">C++/WinRT</span></span>|<span data-ttu-id="92e55-222">cppwinrt</span><span class="sxs-lookup"><span data-stu-id="92e55-222">cppwinrt</span></span>|
|<span data-ttu-id="92e55-223">C#</span><span class="sxs-lookup"><span data-stu-id="92e55-223">C#</span></span>|<span data-ttu-id="92e55-224">csharp</span><span class="sxs-lookup"><span data-stu-id="92e55-224">csharp</span></span>|
|<span data-ttu-id="92e55-225">浏览器中的 C#</span><span class="sxs-lookup"><span data-stu-id="92e55-225">C# in browser</span></span>|<span data-ttu-id="92e55-226">csharp-interactive</span><span class="sxs-lookup"><span data-stu-id="92e55-226">csharp-interactive</span></span>|
|<span data-ttu-id="92e55-227">控制台</span><span class="sxs-lookup"><span data-stu-id="92e55-227">Console</span></span>|<span data-ttu-id="92e55-228">console</span><span class="sxs-lookup"><span data-stu-id="92e55-228">console</span></span>|
|<span data-ttu-id="92e55-229">CSHTML</span><span class="sxs-lookup"><span data-stu-id="92e55-229">CSHTML</span></span>|<span data-ttu-id="92e55-230">cshtml</span><span class="sxs-lookup"><span data-stu-id="92e55-230">cshtml</span></span>|
|<span data-ttu-id="92e55-231">DAX</span><span class="sxs-lookup"><span data-stu-id="92e55-231">DAX</span></span>|<span data-ttu-id="92e55-232">dax</span><span class="sxs-lookup"><span data-stu-id="92e55-232">dax</span></span>|
|<span data-ttu-id="92e55-233">Docker</span><span class="sxs-lookup"><span data-stu-id="92e55-233">Docker</span></span>|<span data-ttu-id="92e55-234">dockerfile</span><span class="sxs-lookup"><span data-stu-id="92e55-234">dockerfile</span></span>|
|<span data-ttu-id="92e55-235">F#</span><span class="sxs-lookup"><span data-stu-id="92e55-235">F#</span></span>|<span data-ttu-id="92e55-236">fsharp</span><span class="sxs-lookup"><span data-stu-id="92e55-236">fsharp</span></span>|
|<span data-ttu-id="92e55-237">Go</span><span class="sxs-lookup"><span data-stu-id="92e55-237">Go</span></span>|<span data-ttu-id="92e55-238">go</span><span class="sxs-lookup"><span data-stu-id="92e55-238">go</span></span>|
|<span data-ttu-id="92e55-239">HTML</span><span class="sxs-lookup"><span data-stu-id="92e55-239">HTML</span></span>|<span data-ttu-id="92e55-240">html</span><span class="sxs-lookup"><span data-stu-id="92e55-240">html</span></span>|
|<span data-ttu-id="92e55-241">HTTP</span><span class="sxs-lookup"><span data-stu-id="92e55-241">HTTP</span></span>|<span data-ttu-id="92e55-242">http</span><span class="sxs-lookup"><span data-stu-id="92e55-242">http</span></span>|
|<span data-ttu-id="92e55-243">Java</span><span class="sxs-lookup"><span data-stu-id="92e55-243">Java</span></span>|<span data-ttu-id="92e55-244">java</span><span class="sxs-lookup"><span data-stu-id="92e55-244">java</span></span>|
|<span data-ttu-id="92e55-245">JavaScript</span><span class="sxs-lookup"><span data-stu-id="92e55-245">JavaScript</span></span>|<span data-ttu-id="92e55-246">javascript</span><span class="sxs-lookup"><span data-stu-id="92e55-246">javascript</span></span>|
|<span data-ttu-id="92e55-247">JSON</span><span class="sxs-lookup"><span data-stu-id="92e55-247">JSON</span></span>|<span data-ttu-id="92e55-248">json</span><span class="sxs-lookup"><span data-stu-id="92e55-248">json</span></span>|
|<span data-ttu-id="92e55-249">Kusto 查询语言</span><span class="sxs-lookup"><span data-stu-id="92e55-249">Kusto Query Language</span></span>|<span data-ttu-id="92e55-250">kusto</span><span class="sxs-lookup"><span data-stu-id="92e55-250">kusto</span></span>|
|<span data-ttu-id="92e55-251">Markdown</span><span class="sxs-lookup"><span data-stu-id="92e55-251">Markdown</span></span>|<span data-ttu-id="92e55-252">md</span><span class="sxs-lookup"><span data-stu-id="92e55-252">md</span></span>|
|<span data-ttu-id="92e55-253">Objective-C</span><span class="sxs-lookup"><span data-stu-id="92e55-253">Objective-C</span></span>|<span data-ttu-id="92e55-254">objc</span><span class="sxs-lookup"><span data-stu-id="92e55-254">objc</span></span>|
|<span data-ttu-id="92e55-255">OData</span><span class="sxs-lookup"><span data-stu-id="92e55-255">OData</span></span>|<span data-ttu-id="92e55-256">odata</span><span class="sxs-lookup"><span data-stu-id="92e55-256">odata</span></span>|
|<span data-ttu-id="92e55-257">PHP</span><span class="sxs-lookup"><span data-stu-id="92e55-257">PHP</span></span>|<span data-ttu-id="92e55-258">php</span><span class="sxs-lookup"><span data-stu-id="92e55-258">php</span></span>|
|<span data-ttu-id="92e55-259">protobuf</span><span class="sxs-lookup"><span data-stu-id="92e55-259">protobuf</span></span>|<span data-ttu-id="92e55-260">protobuf</span><span class="sxs-lookup"><span data-stu-id="92e55-260">protobuf</span></span>|
|<span data-ttu-id="92e55-261">PowerApps（小数点分隔符）</span><span class="sxs-lookup"><span data-stu-id="92e55-261">PowerApps (dot decimal separator)</span></span>|<span data-ttu-id="92e55-262">powerapps-dot</span><span class="sxs-lookup"><span data-stu-id="92e55-262">powerapps-dot</span></span>|
|<span data-ttu-id="92e55-263">PowerApps（逗号分隔符）</span><span class="sxs-lookup"><span data-stu-id="92e55-263">PowerApps (comma decimal separator)</span></span>|<span data-ttu-id="92e55-264">powerapps-comma</span><span class="sxs-lookup"><span data-stu-id="92e55-264">powerapps-comma</span></span>|
|<span data-ttu-id="92e55-265">PowerShell</span><span class="sxs-lookup"><span data-stu-id="92e55-265">PowerShell</span></span>|<span data-ttu-id="92e55-266">powershell</span><span class="sxs-lookup"><span data-stu-id="92e55-266">powershell</span></span>|
|<span data-ttu-id="92e55-267">Python</span><span class="sxs-lookup"><span data-stu-id="92e55-267">Python</span></span>|<span data-ttu-id="92e55-268">python</span><span class="sxs-lookup"><span data-stu-id="92e55-268">python</span></span>|
|<span data-ttu-id="92e55-269">Q#</span><span class="sxs-lookup"><span data-stu-id="92e55-269">Q#</span></span>|<span data-ttu-id="92e55-270">qsharp</span><span class="sxs-lookup"><span data-stu-id="92e55-270">qsharp</span></span>|
|<span data-ttu-id="92e55-271">R</span><span class="sxs-lookup"><span data-stu-id="92e55-271">R</span></span>|<span data-ttu-id="92e55-272">r</span><span class="sxs-lookup"><span data-stu-id="92e55-272">r</span></span>|
|<span data-ttu-id="92e55-273">Ruby</span><span class="sxs-lookup"><span data-stu-id="92e55-273">Ruby</span></span>|<span data-ttu-id="92e55-274">ruby</span><span class="sxs-lookup"><span data-stu-id="92e55-274">ruby</span></span>|
|<span data-ttu-id="92e55-275">SQL</span><span class="sxs-lookup"><span data-stu-id="92e55-275">SQL</span></span>|<span data-ttu-id="92e55-276">sql</span><span class="sxs-lookup"><span data-stu-id="92e55-276">sql</span></span>|
|<span data-ttu-id="92e55-277">Swift</span><span class="sxs-lookup"><span data-stu-id="92e55-277">Swift</span></span>|<span data-ttu-id="92e55-278">swift</span><span class="sxs-lookup"><span data-stu-id="92e55-278">swift</span></span>|
|<span data-ttu-id="92e55-279">TypeScript</span><span class="sxs-lookup"><span data-stu-id="92e55-279">TypeScript</span></span>|<span data-ttu-id="92e55-280">typescript</span><span class="sxs-lookup"><span data-stu-id="92e55-280">typescript</span></span>|
|<span data-ttu-id="92e55-281">VB</span><span class="sxs-lookup"><span data-stu-id="92e55-281">VB</span></span>|<span data-ttu-id="92e55-282">vb</span><span class="sxs-lookup"><span data-stu-id="92e55-282">vb</span></span>|
|<span data-ttu-id="92e55-283">XAML</span><span class="sxs-lookup"><span data-stu-id="92e55-283">XAML</span></span>|<span data-ttu-id="92e55-284">xaml</span><span class="sxs-lookup"><span data-stu-id="92e55-284">xaml</span></span>|
|<span data-ttu-id="92e55-285">XML</span><span class="sxs-lookup"><span data-stu-id="92e55-285">XML</span></span>|<span data-ttu-id="92e55-286">xml</span><span class="sxs-lookup"><span data-stu-id="92e55-286">xml</span></span>|

<span data-ttu-id="92e55-287">`csharp-interactive` 名称指定 C# 语言，以及从浏览器中运行示例的能力。</span><span class="sxs-lookup"><span data-stu-id="92e55-287">The `csharp-interactive` name specifies the C# language, and the ability to run the samples from the browser.</span></span> <span data-ttu-id="92e55-288">这些代码片段在 Docker 容器中进行编译和执行，并且该程序执行的结果在用户浏览器窗口中显示。</span><span class="sxs-lookup"><span data-stu-id="92e55-288">These snippets are compiled and executed in a Docker container, and the results of that program execution are displayed in the user's browser window.</span></span>

#### <a name="example-c"></a><span data-ttu-id="92e55-289">示例：C\#</span><span class="sxs-lookup"><span data-stu-id="92e55-289">Example: C\#</span></span>

<span data-ttu-id="92e55-290">__Markdown__</span><span class="sxs-lookup"><span data-stu-id="92e55-290">__Markdown__</span></span>

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

<span data-ttu-id="92e55-291">__呈现__</span><span class="sxs-lookup"><span data-stu-id="92e55-291">__Render__</span></span>

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

#### <a name="example-sql"></a><span data-ttu-id="92e55-292">示例：SQL</span><span class="sxs-lookup"><span data-stu-id="92e55-292">Example: SQL</span></span>

<span data-ttu-id="92e55-293">__Markdown__</span><span class="sxs-lookup"><span data-stu-id="92e55-293">__Markdown__</span></span>

    ```sql
    CREATE TABLE T1 (
      c1 int PRIMARY KEY,
      c2 varchar(50) SPARSE NULL
    );
    ```

<span data-ttu-id="92e55-294">__呈现__</span><span class="sxs-lookup"><span data-stu-id="92e55-294">__Render__</span></span>

```sql
CREATE TABLE T1 (
  c1 int PRIMARY KEY,
  c2 varchar(50) SPARSE NULL
);
```

## <a name="docs-custom-markdown-extensions"></a><span data-ttu-id="92e55-295">Docs 自定义 Markdown 扩展</span><span class="sxs-lookup"><span data-stu-id="92e55-295">Docs custom Markdown extensions</span></span>

> [!NOTE]
> <span data-ttu-id="92e55-296">Docs.Microsoft.com (Docs) 可实现 Markdown Markdig 分析程序，它与 GitHub 风格的 Markdown (GFM) 高度兼容。</span><span class="sxs-lookup"><span data-stu-id="92e55-296">Docs.Microsoft.com (Docs) implements a Markdig Parser for Markdown, which is highly compatible with GitHub Flavored Markdown (GFM).</span></span> <span data-ttu-id="92e55-297">Markdig 通过 Markdown 扩展添加一些功能。</span><span class="sxs-lookup"><span data-stu-id="92e55-297">Markdig adds some functionality through Markdown extensions.</span></span> <span data-ttu-id="92e55-298">就这一点而言，本指南从完整的《OPS 创作指南》中选用了几篇文章，以供参考。</span><span class="sxs-lookup"><span data-stu-id="92e55-298">As such, selected articles from the full OPS Authoring Guide are included in this guide for reference.</span></span> <span data-ttu-id="92e55-299">（例如，请参阅目录中的“Markdig 和 Markdown 扩展”以及“代码片段”。）</span><span class="sxs-lookup"><span data-stu-id="92e55-299">(For example, see "Markdig and Markdown extensions" and "Code snippets" in the table of contents.)</span></span>

<span data-ttu-id="92e55-300">Doc 文章使用 GFM 完成大多文章的格式设置，如段落、链接、列表和标题。</span><span class="sxs-lookup"><span data-stu-id="92e55-300">Docs articles use GFM for most article formatting, such as paragraphs, links, lists, and headings.</span></span> <span data-ttu-id="92e55-301">要想实现更丰富的格式设置功能，文章可以使用 Markdig 功能，例如：</span><span class="sxs-lookup"><span data-stu-id="92e55-301">For richer formatting, articles can use Markdig features such as:</span></span>

- <span data-ttu-id="92e55-302">备注块</span><span class="sxs-lookup"><span data-stu-id="92e55-302">Note blocks</span></span>
- <span data-ttu-id="92e55-303">包含文件</span><span class="sxs-lookup"><span data-stu-id="92e55-303">Include files</span></span>
- <span data-ttu-id="92e55-304">选择器</span><span class="sxs-lookup"><span data-stu-id="92e55-304">Selectors</span></span>
- <span data-ttu-id="92e55-305">嵌入视频</span><span class="sxs-lookup"><span data-stu-id="92e55-305">Embedded videos</span></span>
- <span data-ttu-id="92e55-306">代码片段/示例</span><span class="sxs-lookup"><span data-stu-id="92e55-306">Code snippets/samples</span></span>

<span data-ttu-id="92e55-307">如需完整列表，请参阅目录中的“Markdig 和 Markdown 扩展”以及“代码片段”。</span><span class="sxs-lookup"><span data-stu-id="92e55-307">For the complete list, refer to "Markdig and Markdown extensions" and "Code snippets" in the table of contents.</span></span>

### <a name="note-blocks"></a><span data-ttu-id="92e55-308">备注块</span><span class="sxs-lookup"><span data-stu-id="92e55-308">Note blocks</span></span>

<span data-ttu-id="92e55-309">可以从 4 种类型的备注块中进行选择来吸引对特定内容的注意：</span><span class="sxs-lookup"><span data-stu-id="92e55-309">You can choose from four types of note blocks to draw attention to specific content:</span></span>

- <span data-ttu-id="92e55-310">NOTE</span><span class="sxs-lookup"><span data-stu-id="92e55-310">NOTE</span></span>
- <span data-ttu-id="92e55-311">WARNING</span><span class="sxs-lookup"><span data-stu-id="92e55-311">WARNING</span></span>
- <span data-ttu-id="92e55-312">TIP</span><span class="sxs-lookup"><span data-stu-id="92e55-312">TIP</span></span>
- <span data-ttu-id="92e55-313">IMPORTANT</span><span class="sxs-lookup"><span data-stu-id="92e55-313">IMPORTANT</span></span>

<span data-ttu-id="92e55-314">总之，应谨慎使用备注块，因为它们可能会造成干扰。</span><span class="sxs-lookup"><span data-stu-id="92e55-314">In general, note blocks should be used sparingly because they can be disruptive.</span></span> <span data-ttu-id="92e55-315">尽管备注块也支持代码块、图像、列表以及链接，但最好尽量保持备注块简单明了。</span><span class="sxs-lookup"><span data-stu-id="92e55-315">Although they also support code blocks, images, lists, and links, try to keep your note blocks simple and straightforward.</span></span>

<span data-ttu-id="92e55-316">示例：</span><span class="sxs-lookup"><span data-stu-id="92e55-316">Examples:</span></span>

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

<span data-ttu-id="92e55-317">这些警报在 docs.microsoft.com 上如下所示：</span><span class="sxs-lookup"><span data-stu-id="92e55-317">These alerts look like this on docs.microsoft.com:</span></span>

![展示上一示例中的警报在使用不同图标和颜色的 Docs 页面发布版中的显示情况](media/alerts-rendering.png)

### <a name="include-files"></a><span data-ttu-id="92e55-319">包含文件</span><span class="sxs-lookup"><span data-stu-id="92e55-319">Include files</span></span>

<span data-ttu-id="92e55-320">如果有需要加入文章文件中的可重用的文本或图像文件，可以通过 Markdig 文件的包含文件功能使用对“包含”文件的引用。</span><span class="sxs-lookup"><span data-stu-id="92e55-320">When you have reusable text or image files that need to be included in article files, you can use a reference to the "include" file via the Markdig file include feature.</span></span> <span data-ttu-id="92e55-321">此功能指示 OPS 在创建时将该文件加入文章文件中，使它成为已发布文章的一部分。</span><span class="sxs-lookup"><span data-stu-id="92e55-321">This feature instructs OPS to include the file in your article file at build time, making it part of your published article.</span></span> <span data-ttu-id="92e55-322">有 3 种类型的包含引用可帮助你重用内容：</span><span class="sxs-lookup"><span data-stu-id="92e55-322">Three types of include references are available to help you reuse content:</span></span>

- <span data-ttu-id="92e55-323">内联：重用内联在其他句子中的常用文本片段。</span><span class="sxs-lookup"><span data-stu-id="92e55-323">Inline: Reuse a common text snippet inline with within another sentence.</span></span>
- <span data-ttu-id="92e55-324">块：将整个 Markdown 文件作为一个块重用，嵌套在文章的某一部分中。</span><span class="sxs-lookup"><span data-stu-id="92e55-324">Block: Reuse an entire Markdown file as a block, nested within a section of an article.</span></span>
- <span data-ttu-id="92e55-325">图像：此方法可以在 Doc 中实现标准图像加入。</span><span class="sxs-lookup"><span data-stu-id="92e55-325">Image: This is how standard image inclusion is implemented in Docs.</span></span>

<span data-ttu-id="92e55-326">“内联”和“块”包含文件是简单的 Markdown (.md) 文件。</span><span class="sxs-lookup"><span data-stu-id="92e55-326">An inline or block include file is just a simple Markdown (.md) file.</span></span> <span data-ttu-id="92e55-327">它可以包含任何有效的 Markdown。</span><span class="sxs-lookup"><span data-stu-id="92e55-327">It can contain any valid Markdown.</span></span> <span data-ttu-id="92e55-328">所有包含 Markdown 文件都应置于存储库根目录的[常用 `/includes` 子目录](git-github-fundamentals.md#includes-subdirectory) 中。</span><span class="sxs-lookup"><span data-stu-id="92e55-328">All include Markdown files should be placed in a [common `/includes` subdirectory](git-github-fundamentals.md#includes-subdirectory), in the root of the repository.</span></span> <span data-ttu-id="92e55-329">发布文章时，加入的文件会无缝集成到其中。</span><span class="sxs-lookup"><span data-stu-id="92e55-329">When the article is published, the included file is seamlessly integrated into it.</span></span>

<span data-ttu-id="92e55-330">包含文件的要求和注意事项如下：</span><span class="sxs-lookup"><span data-stu-id="92e55-330">Here are requirements and considerations for include files:</span></span>

- <span data-ttu-id="92e55-331">每当需要在多篇文章中显示相同的文本时，均可使用包含功能文件。</span><span class="sxs-lookup"><span data-stu-id="92e55-331">Use an include file whenever you need the same text to appear in multiple articles.</span></span>
- <span data-ttu-id="92e55-332">块包含文件适用于大篇幅内容，比如一个或者两个段落、共享过程或者共享章节。</span><span class="sxs-lookup"><span data-stu-id="92e55-332">Use a block include reference for significant amounts of content--a paragraph or two, a shared procedure, or a shared section.</span></span> <span data-ttu-id="92e55-333">请勿将它们用于小于一个句子的内容。</span><span class="sxs-lookup"><span data-stu-id="92e55-333">Do not use them for anything smaller than a sentence.</span></span>
- <span data-ttu-id="92e55-334">包含文件不会在文章的 GitHub 渲染视图中显示，因为它们依赖于 Markdig 扩展。</span><span class="sxs-lookup"><span data-stu-id="92e55-334">Include references won't be rendered in the GitHub rendered view of your article, because they rely on Markdig extensions.</span></span> <span data-ttu-id="92e55-335">它们在发布后才会显示。</span><span class="sxs-lookup"><span data-stu-id="92e55-335">They'll be rendered only after publication.</span></span>
- <span data-ttu-id="92e55-336">确保包含文件中的所有文本都是完整的句子或者段落，并且与引用该包含文件的文章的前后文没有关联。</span><span class="sxs-lookup"><span data-stu-id="92e55-336">Ensure that all the text in an include file is written in complete sentences or phrases that do not depend on preceding text or following text in the article that references the include file.</span></span> <span data-ttu-id="92e55-337">如果不遵循此指导原则，则会在文章中创建无法转换的字符串，进而破坏本地化体验。</span><span class="sxs-lookup"><span data-stu-id="92e55-337">Ignoring this guidance creates an untranslatable string in the article that breaks the localized experience.</span></span>
- <span data-ttu-id="92e55-338">请勿在其他包含文件中嵌入包含引用。</span><span class="sxs-lookup"><span data-stu-id="92e55-338">Don't embed include references within other include files.</span></span> <span data-ttu-id="92e55-339">不支持此操作。</span><span class="sxs-lookup"><span data-stu-id="92e55-339">They are not supported.</span></span>
- <span data-ttu-id="92e55-340">将媒体文件置于特定于包含文件子目录的媒体文件夹中，例如，`<repo>`/includes/媒体文件夹。</span><span class="sxs-lookup"><span data-stu-id="92e55-340">Place media files in a media folder that's specific to the include subdirectory--for instance, the `<repo>`/includes/media folder.</span></span> <span data-ttu-id="92e55-341">媒体目录不应在根目录中包含任何图片。</span><span class="sxs-lookup"><span data-stu-id="92e55-341">The media directory should not contain any images in its root.</span></span> <span data-ttu-id="92e55-342">如果包含文件中没有图像，则不需要相应的媒体目录。</span><span class="sxs-lookup"><span data-stu-id="92e55-342">If the include file does not have images, a corresponding media directory is not required.</span></span>
- <span data-ttu-id="92e55-343">对于常规文章，请勿在各包含文件之间共享媒体。</span><span class="sxs-lookup"><span data-stu-id="92e55-343">As with regular articles, don't share media between include files.</span></span> <span data-ttu-id="92e55-344">对于每个包含文件和文章，请使用具有唯一名称的单独文件。</span><span class="sxs-lookup"><span data-stu-id="92e55-344">Use a separate file with a unique name for each include file and article.</span></span> <span data-ttu-id="92e55-345">将媒体文件存储在与包含文件关联的媒体文件夹中。</span><span class="sxs-lookup"><span data-stu-id="92e55-345">Store the media file in the media folder that's associated with the include file.</span></span>
- <span data-ttu-id="92e55-346">请勿将包含文件用作文章的唯一内容。</span><span class="sxs-lookup"><span data-stu-id="92e55-346">Don't use an include file as the only content of an article.</span></span>  <span data-ttu-id="92e55-347">包含文件主要用作文章其余内容的补充内容。</span><span class="sxs-lookup"><span data-stu-id="92e55-347">Include files are meant to be supplemental to the content in the rest of the article.</span></span>

<span data-ttu-id="92e55-348">示例：</span><span class="sxs-lookup"><span data-stu-id="92e55-348">Example:</span></span>

```md
[!INCLUDE[sample include file](../includes/sampleinclude.md)]
```

### <a name="selectors"></a><span data-ttu-id="92e55-349">选择器</span><span class="sxs-lookup"><span data-stu-id="92e55-349">Selectors</span></span>

<span data-ttu-id="92e55-350">当你创作具有多种风格的同一篇技术文章时，请在文章中使用选择器，从而跨技术或平台解决实现上的差异。</span><span class="sxs-lookup"><span data-stu-id="92e55-350">Use selectors in technical articles when you author multiple flavors of the same article, to  address differences in implementation across technologies or platforms.</span></span> <span data-ttu-id="92e55-351">通常，这最适用于开发人员的移动平台内容。</span><span class="sxs-lookup"><span data-stu-id="92e55-351">This is typically most applicable to our mobile platform content for developers.</span></span> <span data-ttu-id="92e55-352">Markdig 中目前有两种类型的选择器，单选择器和多选择器。</span><span class="sxs-lookup"><span data-stu-id="92e55-352">There are currently two different types of selectors in Markdig, a single selector and a multi-selector.</span></span>

<span data-ttu-id="92e55-353">由于选择的每篇文章中都会出现相同的选择器 Markdown，因此建议将文章的选择器放在包含文件中。</span><span class="sxs-lookup"><span data-stu-id="92e55-353">Because the same selector Markdown goes in each article in the selection, we recommend placing the selector for your article in an include file.</span></span> <span data-ttu-id="92e55-354">然后，可以在使用相同选择器的所有文章中引用该包含文件。</span><span class="sxs-lookup"><span data-stu-id="92e55-354">Then you can reference that include file in all your articles that use the same selector.</span></span>

<span data-ttu-id="92e55-355">下面展示了一个示例选择器：</span><span class="sxs-lookup"><span data-stu-id="92e55-355">The following shows an example selector:</span></span>

```md
> [!div class="op_single_selector"]
- [macOS](../docs/core/tutorials/using-on-macos.md)
- [Windows](../docs/core/tutorials/with-visual-studio.md)
```

<span data-ttu-id="92e55-356">可在 [Azure 文档](https://docs.microsoft.com/azure/expressroute/expressroute-howto-circuit-classic)中查看有效的选择器示例。</span><span class="sxs-lookup"><span data-stu-id="92e55-356">You can see an example of selectors in action at the [Azure docs](https://docs.microsoft.com/azure/expressroute/expressroute-howto-circuit-classic).</span></span>

### <a name="code-include-references"></a><span data-ttu-id="92e55-357">代码包含引用</span><span class="sxs-lookup"><span data-stu-id="92e55-357">Code include references</span></span>

<span data-ttu-id="92e55-358">通过 Docs 代码片段 Markdown 扩展，可在文章中嵌入代码示例，并使用语言特定的语法着色来呈现它们。</span><span class="sxs-lookup"><span data-stu-id="92e55-358">The Docs code snippet Markdown extension allows you to embed code samples in your articles and render them with language-specific syntax coloring.</span></span> <span data-ttu-id="92e55-359">你可包含来自当前存储库中的代码，也可包含来自其他存储库中的代码。</span><span class="sxs-lookup"><span data-stu-id="92e55-359">You can include code from either the current repository or another repository.</span></span> <span data-ttu-id="92e55-360">下面的说明概述了如何将此功能与 [docs.microsoft.com 创作包](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack)一起使用。</span><span class="sxs-lookup"><span data-stu-id="92e55-360">The instructions below provides an overview of how to use the feature with the [docs.microsoft.com Authoring Pack](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack).</span></span> <span data-ttu-id="92e55-361">在 Visual Studio Code 中，可打开“预览”来预览代码片段  。</span><span class="sxs-lookup"><span data-stu-id="92e55-361">In Visual Studio Code, you can preview the code snippets by opening **Preview**.</span></span> <span data-ttu-id="92e55-362">预览中不可使用突出显示和交互功能。</span><span class="sxs-lookup"><span data-stu-id="92e55-362">Highlighting and interactivity are not available in preview.</span></span>

> [!NOTE]
> <span data-ttu-id="92e55-363">此扩展不支持内联包含代码内容 - 这是通过标准的 triple-tick Markdown 约定实现的。</span><span class="sxs-lookup"><span data-stu-id="92e55-363">The extension does not support including code content within it inline – this is to be done through the standard triple-tick Markdown convention.</span></span>

#### <a name="code-from-current-repository"></a><span data-ttu-id="92e55-364">来自当前存储库的代码</span><span class="sxs-lookup"><span data-stu-id="92e55-364">Code from current repository</span></span>

1. <span data-ttu-id="92e55-365">在 Visual Studio Code 中，单击 Alt + M 或 Option + M，再选择“片段”   。</span><span class="sxs-lookup"><span data-stu-id="92e55-365">In Visual Studio Code, click **Alt + M** or **Option + M** and select Snippet.</span></span>
2. <span data-ttu-id="92e55-366">选择片段后，系统将提示你进行完全搜索、范围搜索或跨存储库引用。</span><span class="sxs-lookup"><span data-stu-id="92e55-366">Once Snippet is selected, you will be prompted for Full Search, Scoped Search or Cross-Repository Reference.</span></span> <span data-ttu-id="92e55-367">要在本地搜索，请选择“完整本地搜索”。</span><span class="sxs-lookup"><span data-stu-id="92e55-367">To search locally, select Full Local Search.</span></span>
3. <span data-ttu-id="92e55-368">要查找文件，请输入搜索词。</span><span class="sxs-lookup"><span data-stu-id="92e55-368">Enter a search term to find the file.</span></span> <span data-ttu-id="92e55-369">找到文件后，将其选中。</span><span class="sxs-lookup"><span data-stu-id="92e55-369">Once you’ve found the file, select the file.</span></span>
4. <span data-ttu-id="92e55-370">接下来，选择一个选项来确定应在片段中包含哪些代码行。</span><span class="sxs-lookup"><span data-stu-id="92e55-370">Next, select an option to determine which line(s) of code should be included in the snippet.</span></span> <span data-ttu-id="92e55-371">选项包括：“ID”、“范围”和“无”    。</span><span class="sxs-lookup"><span data-stu-id="92e55-371">The options are: **ID**, **Range** and **None**.</span></span>
5. <span data-ttu-id="92e55-372">根据在步骤 4 中选择的设置，必要时提供一个值。</span><span class="sxs-lookup"><span data-stu-id="92e55-372">Based on your selection from Step 4, provide a value if necessary.</span></span>

<span data-ttu-id="92e55-373">显示整个代码文件：</span><span class="sxs-lookup"><span data-stu-id="92e55-373">Display entire code file:</span></span>

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs":::
```

<span data-ttu-id="92e55-374">通过指定行号来显示代码文件的一部分：</span><span class="sxs-lookup"><span data-stu-id="92e55-374">Display part of a code file by specifying line numbers:</span></span>

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" range="2-24,26":::
```

<span data-ttu-id="92e55-375">按片段名称显示代码文件的一部分：</span><span class="sxs-lookup"><span data-stu-id="92e55-375">Display part of a code file by a snippet name:</span></span>

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" id="snippet_Create":::
```

#### <a name="code-from-another-repository"></a><span data-ttu-id="92e55-376">来自其他存储库的代码</span><span class="sxs-lookup"><span data-stu-id="92e55-376">Code from another repository</span></span>

1. <span data-ttu-id="92e55-377">在 Visual Studio Code 中，单击 Alt + M 或 Option + M，再选择“片段”   。</span><span class="sxs-lookup"><span data-stu-id="92e55-377">In Visual Studio Code, click **Alt + M** or **Option + M** and select Snippet.</span></span>
2. <span data-ttu-id="92e55-378">选择片段后，系统将提示你进行完全搜索、范围搜索或跨存储库引用。</span><span class="sxs-lookup"><span data-stu-id="92e55-378">Once Snippet is selected, you will be prompted for Full Search, Scoped Search or Cross-Repository Reference.</span></span> <span data-ttu-id="92e55-379">要跨存储库进行搜索，请选择“跨存储库引用”。</span><span class="sxs-lookup"><span data-stu-id="92e55-379">To search across repositories, select Cross-Repository Reference.</span></span>
3. <span data-ttu-id="92e55-380">将显示 .openpublishing.publish.config.json 中的存储库供你选择  。</span><span class="sxs-lookup"><span data-stu-id="92e55-380">You will be given a selection of repositories that are in *.openpublishing.publish.config.json*.</span></span> <span data-ttu-id="92e55-381">选择存储库。</span><span class="sxs-lookup"><span data-stu-id="92e55-381">Select a repository.</span></span>
3. <span data-ttu-id="92e55-382">要查找文件，请输入搜索词。</span><span class="sxs-lookup"><span data-stu-id="92e55-382">Enter a search term to find the file.</span></span> <span data-ttu-id="92e55-383">找到文件后，将其选中。</span><span class="sxs-lookup"><span data-stu-id="92e55-383">Once you’ve found the file, select the file.</span></span>
4. <span data-ttu-id="92e55-384">接下来，选择一个选项来确定应在片段中包含哪些代码行。</span><span class="sxs-lookup"><span data-stu-id="92e55-384">Next, select an option to determine which line(s) of code should be included in the snippet.</span></span> <span data-ttu-id="92e55-385">选项包括：“ID”、“范围”和“无”    。</span><span class="sxs-lookup"><span data-stu-id="92e55-385">The options are: **ID**, **Range** and **None**.</span></span>
5. <span data-ttu-id="92e55-386">根据在步骤 5 中选择的设置，必要时提供一个值。</span><span class="sxs-lookup"><span data-stu-id="92e55-386">Based on your selection from Step 5, provide a value if necessary.</span></span>

<span data-ttu-id="92e55-387">你的片段引用将如下所示：</span><span class="sxs-lookup"><span data-stu-id="92e55-387">Your snippet reference will look like this:</span></span>

```markdown
:::code language="csharp" source="~/samples-durable-functions/samples/csx/shared/Location.csx" highlight="2,5":::
```

#### <a name="path-to-code-file"></a><span data-ttu-id="92e55-388">代码文件路径</span><span class="sxs-lookup"><span data-stu-id="92e55-388">Path to code file</span></span>

<span data-ttu-id="92e55-389">示例：</span><span class="sxs-lookup"><span data-stu-id="92e55-389">Example:</span></span>

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" range="2-24,26":::
```

<span data-ttu-id="92e55-390">本示例摘自 ASP.NET 文档存储库，[aspnetcore/data/ef-mvc/crud.md](https://github.com/aspnet/Docs/blob/master/aspnetcore/data/ef-mvc/crud.md) 文章文件。</span><span class="sxs-lookup"><span data-stu-id="92e55-390">The example is from the ASP.NET docs repo, [aspnetcore/data/ef-mvc/crud.md](https://github.com/aspnet/Docs/blob/master/aspnetcore/data/ef-mvc/crud.md) article file.</span></span> <span data-ttu-id="92e55-391">此代码文件通过同一存储库中的 [aspnetcore/data/ef-mvc/intro/samples/cu/Controllers/StudentsController.cs](https://github.com/aspnet/Docs/blob/master/aspnetcore/data/ef-mvc/intro/samples/cu/Controllers/StudentsController.cs) 相对路径进行引用。</span><span class="sxs-lookup"><span data-stu-id="92e55-391">The code file is referenced by a relative path to [aspnetcore/data/ef-mvc/intro/samples/cu/Controllers/StudentsController.cs](https://github.com/aspnet/Docs/blob/master/aspnetcore/data/ef-mvc/intro/samples/cu/Controllers/StudentsController.cs) in the same repository.</span></span>

#### <a name="selected-line-numbers"></a><span data-ttu-id="92e55-392">选定行号</span><span class="sxs-lookup"><span data-stu-id="92e55-392">Selected line numbers</span></span>

<span data-ttu-id="92e55-393">示例：</span><span class="sxs-lookup"><span data-stu-id="92e55-393">Example:</span></span>

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" range="2-24,26":::
```

<span data-ttu-id="92e55-394">此示例仅显示了 StudentController.cs 代码文件中的第 2-24 行和第 26 行  。</span><span class="sxs-lookup"><span data-stu-id="92e55-394">This example displays only lines 2-24 and 26 of the *StudentController.cs* code file.</span></span>

<span data-ttu-id="92e55-395">更倾向于代码段而不是硬编码的行号，如下一节中所述。</span><span class="sxs-lookup"><span data-stu-id="92e55-395">Prefer snippets over hard-coded line numbers, as explained in the next section.</span></span>

#### <a name="named-snippet"></a><span data-ttu-id="92e55-396">命名的代码段</span><span class="sxs-lookup"><span data-stu-id="92e55-396">Named snippet</span></span>

<span data-ttu-id="92e55-397">示例：</span><span class="sxs-lookup"><span data-stu-id="92e55-397">Example:</span></span>

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" id="snippet_Create":::
```

<span data-ttu-id="92e55-398">仅在名称中使用字母和下划线。</span><span class="sxs-lookup"><span data-stu-id="92e55-398">Use only letters and underscores for the name.</span></span>

<span data-ttu-id="92e55-399">本示例显示代码文件的 `snippet_Create` 部分。</span><span class="sxs-lookup"><span data-stu-id="92e55-399">The example displays the `snippet_Create` section of the code file.</span></span> <span data-ttu-id="92e55-400">本示例中的代码文件具有名为 `snippet_Create` 的 C# 区域：</span><span class="sxs-lookup"><span data-stu-id="92e55-400">The code file for this example has a C# region named `snippet_Create`:</span></span>

```cs
// code excluded from the snippet
// <snippet_Create>
// code included in the snippet
// </snippet_Create>
// code excluded from the snippet
```

<span data-ttu-id="92e55-401">在可能的情况下，请参考命名的部分，而不是指定行号。</span><span class="sxs-lookup"><span data-stu-id="92e55-401">Whenever you can, refer to a named section rather than specifying line numbers.</span></span> <span data-ttu-id="92e55-402">行号引用不太稳妥，因为在更改行号时，代码文件不可避免地会发生更改。</span><span class="sxs-lookup"><span data-stu-id="92e55-402">Line number references are brittle because code files inevitably change in ways that make line numbers change.</span></span>
<span data-ttu-id="92e55-403">不一定会收到此类更改的通知。</span><span class="sxs-lookup"><span data-stu-id="92e55-403">You don't necessarily get notified of such changes.</span></span> <span data-ttu-id="92e55-404">最终，文章开始显示错误行，并且你完全不知道发生的任何变更。</span><span class="sxs-lookup"><span data-stu-id="92e55-404">Your article eventually starts showing the wrong lines and you have no clue anything has changed.</span></span>

#### <a name="highlighting-selected-lines"></a><span data-ttu-id="92e55-405">突出显示选定行</span><span class="sxs-lookup"><span data-stu-id="92e55-405">Highlighting selected lines</span></span>

<span data-ttu-id="92e55-406">示例：</span><span class="sxs-lookup"><span data-stu-id="92e55-406">Example:</span></span>

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" range="2-24,26" highlight="2,5":::
```

<span data-ttu-id="92e55-407">本示例突出显示第 2 行和第 5 行，从显示的代码段开头开始计数。</span><span class="sxs-lookup"><span data-stu-id="92e55-407">The example highlights lines 2 and 5, counting from the start of the displayed snippet.</span></span> <span data-ttu-id="92e55-408">（要突出显示的行号并不从代码文件的开头开始计数。）也就是说，代码文件的第 3 行和第 6 行会突出显示。</span><span class="sxs-lookup"><span data-stu-id="92e55-408">(Line numbers to highlight don't count from the start of the code file.) In other words, lines 3 and 6 of the code file are highlighted.</span></span>

#### <a name="interactive-code-snippets"></a><span data-ttu-id="92e55-409">交互式代码片段</span><span class="sxs-lookup"><span data-stu-id="92e55-409">Interactive code snippets</span></span>

<span data-ttu-id="92e55-410">可以为通过引用包含的代码段启用交互模式。</span><span class="sxs-lookup"><span data-stu-id="92e55-410">You can enable interactive mode for code snippets included by reference.</span></span> <span data-ttu-id="92e55-411">示例如下：</span><span class="sxs-lookup"><span data-stu-id="92e55-411">Here are examples:</span></span>

```markdown
:::code language="powershell" source="PowerShell.ps1" interactive="cloudshell-powershell":::
```

```markdown
:::code language="bash" source="Bash.sh" interactive="cloudshell-bash":::
```

<span data-ttu-id="92e55-412">要为特定代码块启用此功能，请使用 `interactive` 属性。</span><span class="sxs-lookup"><span data-stu-id="92e55-412">To turn on this feature for a particular code block, use the `interactive` attribute.</span></span> <span data-ttu-id="92e55-413">可用的属性值如下：</span><span class="sxs-lookup"><span data-stu-id="92e55-413">The available attribute values are:</span></span>

- <span data-ttu-id="92e55-414">`cloudshell-powershell` - 启用 Azure PowerShell Cloud Shell，如前例所示</span><span class="sxs-lookup"><span data-stu-id="92e55-414">`cloudshell-powershell` - Enables the Azure PowerShell Cloud Shell, as in the preceding example</span></span>
- <span data-ttu-id="92e55-415">`cloudshell-bash` - 启用 Azure Cloud Shell</span><span class="sxs-lookup"><span data-stu-id="92e55-415">`cloudshell-bash` - Enables the Azure Cloud Shell</span></span>
- <span data-ttu-id="92e55-416">`try-dotnet` - 启用 Try .NET</span><span class="sxs-lookup"><span data-stu-id="92e55-416">`try-dotnet` - Enables Try .NET</span></span>
- <span data-ttu-id="92e55-417">`try-dotnet-class` - 使用类基架启用 Try .NET</span><span class="sxs-lookup"><span data-stu-id="92e55-417">`try-dotnet-class` - Enables Try .NET with class scaffolding</span></span>
- <span data-ttu-id="92e55-418">`try-dotnet-method` - 使用方法基架启用 Try .NET</span><span class="sxs-lookup"><span data-stu-id="92e55-418">`try-dotnet-method` - Enables Try .NET with method scaffolding</span></span>

<span data-ttu-id="92e55-419">存在兼容的 `language` 和 `interactive` 对。</span><span class="sxs-lookup"><span data-stu-id="92e55-419">There are pairs of `language` and `interactive` that are compatible.</span></span> <span data-ttu-id="92e55-420">例如，如果 `interactive` 是 `try-dotnet`，则语言必须是 `csharp`。</span><span class="sxs-lookup"><span data-stu-id="92e55-420">For example, if `interactive` is `try-dotnet`, the language must be `csharp`.</span></span> <span data-ttu-id="92e55-421">同样，`cloudshell-powershell` 仅适用于`powershell`，而 `cloudshell-bash` 仅使用 `bash` 作为语言。</span><span class="sxs-lookup"><span data-stu-id="92e55-421">Similarly, `cloudshell-powershell` would only work with `powershell` and `cloudshell-bash` would work only with `bash` as the language.</span></span>

<span data-ttu-id="92e55-422">对于 Azure Cloud Shell 和 PowerShell Cloud Shell，用户可以只针对自己的 Azure 帐户运行命令。</span><span class="sxs-lookup"><span data-stu-id="92e55-422">For the Azure Cloud Shell and PowerShell Cloud Shell, users can run commands against only their own Azure account.</span></span>

<span data-ttu-id="92e55-423">通过 [Try .NET](https://github.com/dotnet/try) 可在浏览器中实现 .NET 代码 (C#) 的交互式执行。</span><span class="sxs-lookup"><span data-stu-id="92e55-423">[Try .NET](https://github.com/dotnet/try) enables interactive execution of .NET code (C#) in the browser.</span></span> <span data-ttu-id="92e55-424">对于 Try .NET，有三个选项可实现交互：`try-dotnet`、`try-dotnet-class` 和 `try-dotnet-method`。</span><span class="sxs-lookup"><span data-stu-id="92e55-424">For Try .NET, there are three options for interactivity: `try-dotnet`, `try-dotnet-class`, and `try-dotnet-method`.</span></span> <span data-ttu-id="92e55-425">无需在代码片段中进行额外配置即可使用这些选项。</span><span class="sxs-lookup"><span data-stu-id="92e55-425">Use of these options require no additional configuration within the code snippet.</span></span> <span data-ttu-id="92e55-426">当前默认可用的命名空间包括：</span><span class="sxs-lookup"><span data-stu-id="92e55-426">The namespaces currently available by default are:</span></span>

- <span data-ttu-id="92e55-427">System</span><span class="sxs-lookup"><span data-stu-id="92e55-427">System</span></span>
- <span data-ttu-id="92e55-428">System.Linq</span><span class="sxs-lookup"><span data-stu-id="92e55-428">System.Linq</span></span>
- <span data-ttu-id="92e55-429">System.Collections.Generic</span><span class="sxs-lookup"><span data-stu-id="92e55-429">System.Collections.Generic</span></span>
- <span data-ttu-id="92e55-430">System.Text</span><span class="sxs-lookup"><span data-stu-id="92e55-430">System.Text</span></span>
- <span data-ttu-id="92e55-431">System.Globalization</span><span class="sxs-lookup"><span data-stu-id="92e55-431">System.Globalization</span></span>
- <span data-ttu-id="92e55-432">System.Text.RegularExpressions</span><span class="sxs-lookup"><span data-stu-id="92e55-432">System.Text.RegularExpressions</span></span>

<span data-ttu-id="92e55-433">用户可通过 `try-dotnet` 属性值在浏览器中运行 C# 代码，而无需将该代码包装在任何自定义代码中。</span><span class="sxs-lookup"><span data-stu-id="92e55-433">The `try-dotnet` attribute value enables users to run C# code in the browser without the need to wrap the code in any custom code.</span></span>

<span data-ttu-id="92e55-434">示例：</span><span class="sxs-lookup"><span data-stu-id="92e55-434">Example:</span></span>

```md
:::code language="csharp" source="relative/path/source.cs" interactive="try-dotnet":::
```

<span data-ttu-id="92e55-435">`try-dotnet-class` 值将类级别基架应用于传递到交互式组件的代码。</span><span class="sxs-lookup"><span data-stu-id="92e55-435">The `try-dotnet-class` value applies class-level scaffolding to the code passed to the interactive component.</span></span>

```md
:::code language="csharp" source="relative/path/source.cs" id="snippet-tag" interactive="try-dotnet-class":::
```

<span data-ttu-id="92e55-436">示例：</span><span class="sxs-lookup"><span data-stu-id="92e55-436">Example:</span></span>

<span data-ttu-id="92e55-437">未应用类基架的代码片段</span><span class="sxs-lookup"><span data-stu-id="92e55-437">Code Snippet without Class Scaffolding Applied</span></span>

```md
public static void Main()
    {  
        // Specify the data source.  
        int[] scores = new int[] { 97, 92, 81, 60 };        // Define the query expression.

        IEnumerable<int> scoreQuery =
            from score in scores  
            where score > 80  
            select score;

        // Execute the query.  
        foreach (int i in scoreQuery)
        {  
            Console.Write(i + " ");
        }
    }  
}
```

<span data-ttu-id="92e55-438">应用了类基架的代码片段</span><span class="sxs-lookup"><span data-stu-id="92e55-438">Code Snippet with Class Scaffolding Applied</span></span>

```md
class NameOfClass {

   public static void Main()
    {
        // Specify the data source.
        int[] scores = new int[] { 97, 92, 81, 60 };

        // Define the query expression.
        IEnumerable<int> scoreQuery =
            from score in scores
            where score > 80
            select score;

        // Execute the query.
        foreach (int i in scoreQuery)
        {
            Console.Write(i + " ");
        }
    }  
}
```

<span data-ttu-id="92e55-439">`try-dotnet-method` 值将方法级别基架应用于传递到交互式组件的代码。</span><span class="sxs-lookup"><span data-stu-id="92e55-439">The `try-dotnet-method` value applies method-level scaffolding to the code passed to the interactive component.</span></span>

```md
:::code language="csharp" source="relative/path/source.cs" id="snippet-tag" interactive="try-dotnet-method":::
```

<span data-ttu-id="92e55-440">示例：</span><span class="sxs-lookup"><span data-stu-id="92e55-440">Example:</span></span>

<span data-ttu-id="92e55-441">未应用方法基架的代码片段</span><span class="sxs-lookup"><span data-stu-id="92e55-441">Code Snippet without Method Scaffolding Applied</span></span>

```md
/*Print some string in C#*/

Console.WriteLine("Hello C#.);
```

<span data-ttu-id="92e55-442">应用了方法基架的代码片段</span><span class="sxs-lookup"><span data-stu-id="92e55-442">Code Snippet with Method Scaffolding Applied</span></span>

```md
public static void Main(string args[]) {

/*Print some string in C#*/

Console.WriteLine("Hello C#.);
}
```

#### <a name="snippet-syntax-reference"></a><span data-ttu-id="92e55-443">片段语法引用</span><span class="sxs-lookup"><span data-stu-id="92e55-443">Snippet syntax reference</span></span>

<span data-ttu-id="92e55-444">通过使用指定的代码语言，可引用存储库中存储的代码片段。</span><span class="sxs-lookup"><span data-stu-id="92e55-444">You can reference code snippets stored in your repo by using the specified code language.</span></span> <span data-ttu-id="92e55-445">指定代码路径的内容将扩展并包含到你的文件中。</span><span class="sxs-lookup"><span data-stu-id="92e55-445">The content of the specified code path will be expanded and included in your file.</span></span>

<span data-ttu-id="92e55-446">代码片段的文件夹结构不受限制。</span><span class="sxs-lookup"><span data-stu-id="92e55-446">There aren't restrictions on the folder structure of code snippets.</span></span> <span data-ttu-id="92e55-447">可将代码片段当作普通源代码进行管理。</span><span class="sxs-lookup"><span data-stu-id="92e55-447">You can manage the code snippets as normal source code.</span></span>

<span data-ttu-id="92e55-448">语法：</span><span class="sxs-lookup"><span data-stu-id="92e55-448">Syntax:</span></span>

```md
:::code language="<language>" source="<path>" <attribute>="<attribute-value>":::
```

> [!IMPORTANT]
> <span data-ttu-id="92e55-449">此语法是块 Markdown 扩展。</span><span class="sxs-lookup"><span data-stu-id="92e55-449">This syntax is a block Markdown extension.</span></span> <span data-ttu-id="92e55-450">必须在自己的行中使用它。</span><span class="sxs-lookup"><span data-stu-id="92e55-450">It must be used on its own line.</span></span>

- <span data-ttu-id="92e55-451">`<language>`（可选） </span><span class="sxs-lookup"><span data-stu-id="92e55-451">`<language>` (*optional*)</span></span>
  - <span data-ttu-id="92e55-452">代码片段的语言。</span><span class="sxs-lookup"><span data-stu-id="92e55-452">Language of the code snippet.</span></span> <span data-ttu-id="92e55-453">有关详细信息，请参阅本文后面的[支持的语言](#supported-languages)部分。</span><span class="sxs-lookup"><span data-stu-id="92e55-453">For more information, see the [Supported languages](#supported-languages) section later in this article.</span></span>

- <span data-ttu-id="92e55-454">`<path>`（必需） </span><span class="sxs-lookup"><span data-stu-id="92e55-454">`<path>` (*mandatory*)</span></span>
  - <span data-ttu-id="92e55-455">文件系统中的相对路径，指示将引用的代码片段文件。</span><span class="sxs-lookup"><span data-stu-id="92e55-455">Relative path in the file system that indicates the code snippet file to reference.</span></span>

- <span data-ttu-id="92e55-456">`<attribute>` 和 `<attribute-value>`（可选） </span><span class="sxs-lookup"><span data-stu-id="92e55-456">`<attribute>` and `<attribute-value>` (*optional*)</span></span>
  - <span data-ttu-id="92e55-457">配合使用以指定如何从文件中检索代码：</span><span class="sxs-lookup"><span data-stu-id="92e55-457">Used together to specify how the code should be retrieved from the file:</span></span>
    - <span data-ttu-id="92e55-458">`range`：`1,3-5` 行的范围。</span><span class="sxs-lookup"><span data-stu-id="92e55-458">`range`: `1,3-5` A range of lines.</span></span> <span data-ttu-id="92e55-459">此示例包含第 1、3、4 和 5 行。</span><span class="sxs-lookup"><span data-stu-id="92e55-459">This example includes lines 1, 3, 4, and 5.</span></span>
    - <span data-ttu-id="92e55-460">`id`：`snippet_Create`：需要从代码文件中插入的片段的 ID。</span><span class="sxs-lookup"><span data-stu-id="92e55-460">`id`: `snippet_Create` The ID of the snippet that needs to be inserted from the code file.</span></span> <span data-ttu-id="92e55-461">该值不能与范围共存。</span><span class="sxs-lookup"><span data-stu-id="92e55-461">This value cannot co-exist with range.</span></span>
    - <span data-ttu-id="92e55-462">`highlight`：`2-4,6`：需要在生成的代码片段中突出显示的范围和/或行数。</span><span class="sxs-lookup"><span data-stu-id="92e55-462">`highlight`: `2-4,6` Range and/or numbers of lines that need to be highlighted in the generated code snippet.</span></span> <span data-ttu-id="92e55-463">编号是与代码片段本身相对的，不与导入的范围相对。</span><span class="sxs-lookup"><span data-stu-id="92e55-463">The numbering is relative to the code snippet itself, not the imported range.</span></span>
    - <span data-ttu-id="92e55-464">`interactive`：`cloudshell-powershell`、`cloudshell-bash`、`try-dotnet`、`try-dotnet-class`、`try-dotnet-method` 字符串值确定启用了哪些类型的交互。</span><span class="sxs-lookup"><span data-stu-id="92e55-464">`interactive`: `cloudshell-powershell`, `cloudshell-bash`, `try-dotnet`, `try-dotnet-class`, `try-dotnet-method` String value determines what kinds of interactivity are enabled.</span></span>

#### <a name="supported-languages"></a><span data-ttu-id="92e55-465">支持的语言</span><span class="sxs-lookup"><span data-stu-id="92e55-465">Supported languages</span></span>

|<span data-ttu-id="92e55-466">名称</span><span class="sxs-lookup"><span data-stu-id="92e55-466">Name</span></span>|<span data-ttu-id="92e55-467">Markdown 标签</span><span class="sxs-lookup"><span data-stu-id="92e55-467">Markdown label</span></span>|
|-----|-------|
|<span data-ttu-id="92e55-468">.NET Core CLI</span><span class="sxs-lookup"><span data-stu-id="92e55-468">.NET Core CLI</span></span>|`dotnetcli`|
|<span data-ttu-id="92e55-469">结合使用 ASP.NET 和 C#</span><span class="sxs-lookup"><span data-stu-id="92e55-469">ASP.NET with C#</span></span>|`aspx-csharp`|
|<span data-ttu-id="92e55-470">结合使用 ASP.NET 和 VB</span><span class="sxs-lookup"><span data-stu-id="92e55-470">ASP.NET with VB</span></span>|`aspx-vb`|
|<span data-ttu-id="92e55-471">Azure CLI</span><span class="sxs-lookup"><span data-stu-id="92e55-471">Azure CLI</span></span>|`azurecli`|
|<span data-ttu-id="92e55-472">浏览器中的 Azure CLI</span><span class="sxs-lookup"><span data-stu-id="92e55-472">Azure CLI in browser</span></span>|`azurecli-interactive`|
|<span data-ttu-id="92e55-473">浏览器中的 Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="92e55-473">Azure PowerShell in browser</span></span>|`azurepowershell-interactive`|
|<span data-ttu-id="92e55-474">AzCopy</span><span class="sxs-lookup"><span data-stu-id="92e55-474">AzCopy</span></span>|`azcopy`|
|<span data-ttu-id="92e55-475">Bash</span><span class="sxs-lookup"><span data-stu-id="92e55-475">Bash</span></span>|`bash`|
|<span data-ttu-id="92e55-476">C++</span><span class="sxs-lookup"><span data-stu-id="92e55-476">C++</span></span>|`cpp`|
|<span data-ttu-id="92e55-477">C#</span><span class="sxs-lookup"><span data-stu-id="92e55-477">C#</span></span>|`csharp`|
|<span data-ttu-id="92e55-478">浏览器中的 C#</span><span class="sxs-lookup"><span data-stu-id="92e55-478">C# in browser</span></span>|`csharp-interactive`|
|<span data-ttu-id="92e55-479">控制台</span><span class="sxs-lookup"><span data-stu-id="92e55-479">Console</span></span>|`console`|
|<span data-ttu-id="92e55-480">CSHTML</span><span class="sxs-lookup"><span data-stu-id="92e55-480">CSHTML</span></span>|`cshtml`|
|<span data-ttu-id="92e55-481">DAX</span><span class="sxs-lookup"><span data-stu-id="92e55-481">DAX</span></span>|`dax`|
|<span data-ttu-id="92e55-482">Docker</span><span class="sxs-lookup"><span data-stu-id="92e55-482">Docker</span></span>|`Dockerfile`|
|<span data-ttu-id="92e55-483">F#</span><span class="sxs-lookup"><span data-stu-id="92e55-483">F#</span></span>|`fsharp`|
|<span data-ttu-id="92e55-484">HTML</span><span class="sxs-lookup"><span data-stu-id="92e55-484">HTML</span></span>|`html`|
|<span data-ttu-id="92e55-485">Java</span><span class="sxs-lookup"><span data-stu-id="92e55-485">Java</span></span>|`java`|
|<span data-ttu-id="92e55-486">JavaScript</span><span class="sxs-lookup"><span data-stu-id="92e55-486">JavaScript</span></span>|`javascript`|
|<span data-ttu-id="92e55-487">JSON</span><span class="sxs-lookup"><span data-stu-id="92e55-487">JSON</span></span>|`json`|
|<span data-ttu-id="92e55-488">Kusto 查询语言</span><span class="sxs-lookup"><span data-stu-id="92e55-488">Kusto Query Language</span></span>|`kusto`|
|<span data-ttu-id="92e55-489">Markdown</span><span class="sxs-lookup"><span data-stu-id="92e55-489">Markdown</span></span>|`md`|
|<span data-ttu-id="92e55-490">Objective-C</span><span class="sxs-lookup"><span data-stu-id="92e55-490">Objective-C</span></span>|`objc`|
|<span data-ttu-id="92e55-491">PHP</span><span class="sxs-lookup"><span data-stu-id="92e55-491">PHP</span></span>|`php`|
|<span data-ttu-id="92e55-492">PowerShell</span><span class="sxs-lookup"><span data-stu-id="92e55-492">PowerShell</span></span>|`powershell`|
|<span data-ttu-id="92e55-493">Power Query M</span><span class="sxs-lookup"><span data-stu-id="92e55-493">Power Query M</span></span>|`powerquery-m`|
|<span data-ttu-id="92e55-494">protobuf</span><span class="sxs-lookup"><span data-stu-id="92e55-494">protobuf</span></span>|`protobuf`|
|<span data-ttu-id="92e55-495">Python</span><span class="sxs-lookup"><span data-stu-id="92e55-495">Python</span></span>|`python`|
|<span data-ttu-id="92e55-496">Ruby</span><span class="sxs-lookup"><span data-stu-id="92e55-496">Ruby</span></span>|`ruby`|
|<span data-ttu-id="92e55-497">SQL</span><span class="sxs-lookup"><span data-stu-id="92e55-497">SQL</span></span>|`sql`|
|<span data-ttu-id="92e55-498">Swift</span><span class="sxs-lookup"><span data-stu-id="92e55-498">Swift</span></span>|`swift`|
|<span data-ttu-id="92e55-499">VB</span><span class="sxs-lookup"><span data-stu-id="92e55-499">VB</span></span>|`vb`|
|<span data-ttu-id="92e55-500">XAML</span><span class="sxs-lookup"><span data-stu-id="92e55-500">XAML</span></span>|`xaml`|
|<span data-ttu-id="92e55-501">XML</span><span class="sxs-lookup"><span data-stu-id="92e55-501">XML</span></span>|`xml`|
|<span data-ttu-id="92e55-502">YAML</span><span class="sxs-lookup"><span data-stu-id="92e55-502">YAML</span></span>|`yml`|

#### <a name="code-extensions"></a><span data-ttu-id="92e55-503">代码扩展</span><span class="sxs-lookup"><span data-stu-id="92e55-503">Code extensions</span></span>

|<span data-ttu-id="92e55-504">名称</span><span class="sxs-lookup"><span data-stu-id="92e55-504">Name</span></span>|<span data-ttu-id="92e55-505">Markdown 标签</span><span class="sxs-lookup"><span data-stu-id="92e55-505">Markdown label</span></span>|<span data-ttu-id="92e55-506">文件扩展</span><span class="sxs-lookup"><span data-stu-id="92e55-506">File extension</span></span>|
|-----|-------|-----|
|<span data-ttu-id="92e55-507">C#</span><span class="sxs-lookup"><span data-stu-id="92e55-507">C#</span></span>|<span data-ttu-id="92e55-508">csharp</span><span class="sxs-lookup"><span data-stu-id="92e55-508">csharp</span></span>|<span data-ttu-id="92e55-509">.cs、.csx</span><span class="sxs-lookup"><span data-stu-id="92e55-509">.cs, .csx</span></span>|
|<span data-ttu-id="92e55-510">C++</span><span class="sxs-lookup"><span data-stu-id="92e55-510">C++</span></span>|<span data-ttu-id="92e55-511">cpp</span><span class="sxs-lookup"><span data-stu-id="92e55-511">cpp</span></span>|<span data-ttu-id="92e55-512">.cpp、.h</span><span class="sxs-lookup"><span data-stu-id="92e55-512">.cpp, .h</span></span>|
|<span data-ttu-id="92e55-513">F#</span><span class="sxs-lookup"><span data-stu-id="92e55-513">F#</span></span>|<span data-ttu-id="92e55-514">fsharp</span><span class="sxs-lookup"><span data-stu-id="92e55-514">fsharp</span></span>|<span data-ttu-id="92e55-515">.fs</span><span class="sxs-lookup"><span data-stu-id="92e55-515">.fs</span></span>|
|<span data-ttu-id="92e55-516">Java</span><span class="sxs-lookup"><span data-stu-id="92e55-516">Java</span></span>|<span data-ttu-id="92e55-517">java</span><span class="sxs-lookup"><span data-stu-id="92e55-517">java</span></span>|<span data-ttu-id="92e55-518">.java</span><span class="sxs-lookup"><span data-stu-id="92e55-518">.java</span></span>|
|<span data-ttu-id="92e55-519">JavaScript</span><span class="sxs-lookup"><span data-stu-id="92e55-519">JavaScript</span></span>|<span data-ttu-id="92e55-520">javascript</span><span class="sxs-lookup"><span data-stu-id="92e55-520">javascript</span></span>|<span data-ttu-id="92e55-521">.js</span><span class="sxs-lookup"><span data-stu-id="92e55-521">.js</span></span>|
|<span data-ttu-id="92e55-522">Python</span><span class="sxs-lookup"><span data-stu-id="92e55-522">Python</span></span>|<span data-ttu-id="92e55-523">python</span><span class="sxs-lookup"><span data-stu-id="92e55-523">python</span></span>|<span data-ttu-id="92e55-524">.py</span><span class="sxs-lookup"><span data-stu-id="92e55-524">.py</span></span>|
|<span data-ttu-id="92e55-525">SQL</span><span class="sxs-lookup"><span data-stu-id="92e55-525">SQL</span></span>|<span data-ttu-id="92e55-526">sql</span><span class="sxs-lookup"><span data-stu-id="92e55-526">sql</span></span>|<span data-ttu-id="92e55-527">.sql</span><span class="sxs-lookup"><span data-stu-id="92e55-527">.sql</span></span>|
|<span data-ttu-id="92e55-528">VB</span><span class="sxs-lookup"><span data-stu-id="92e55-528">VB</span></span>|<span data-ttu-id="92e55-529">vb</span><span class="sxs-lookup"><span data-stu-id="92e55-529">vb</span></span>|<span data-ttu-id="92e55-530">.vb</span><span class="sxs-lookup"><span data-stu-id="92e55-530">.vb</span></span>|
|<span data-ttu-id="92e55-531">XAML</span><span class="sxs-lookup"><span data-stu-id="92e55-531">XAML</span></span>|<span data-ttu-id="92e55-532">xaml</span><span class="sxs-lookup"><span data-stu-id="92e55-532">xaml</span></span>|<span data-ttu-id="92e55-533">.xaml</span><span class="sxs-lookup"><span data-stu-id="92e55-533">.xaml</span></span>|
|<span data-ttu-id="92e55-534">XML</span><span class="sxs-lookup"><span data-stu-id="92e55-534">XML</span></span>|<span data-ttu-id="92e55-535">xml</span><span class="sxs-lookup"><span data-stu-id="92e55-535">xml</span></span>|<span data-ttu-id="92e55-536">.xml</span><span class="sxs-lookup"><span data-stu-id="92e55-536">.xml</span></span>|

## <a name="gotchas-and-troubleshooting"></a><span data-ttu-id="92e55-537">难题和故障排除</span><span class="sxs-lookup"><span data-stu-id="92e55-537">Gotchas and troubleshooting</span></span>

### <a name="alt-text"></a><span data-ttu-id="92e55-538">替换文字</span><span class="sxs-lookup"><span data-stu-id="92e55-538">Alt text</span></span>

<span data-ttu-id="92e55-539">无法正确显示带下划线的替换文字。</span><span class="sxs-lookup"><span data-stu-id="92e55-539">Alt text that contains underscores won't be rendered properly.</span></span> <span data-ttu-id="92e55-540">例如，与使用以下下划线相比：</span><span class="sxs-lookup"><span data-stu-id="92e55-540">For example, instead of using this:</span></span>

```md
![ADextension_2FA_Configure_Step4](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

<span data-ttu-id="92e55-541">转义下划线，如下所示：</span><span class="sxs-lookup"><span data-stu-id="92e55-541">Escape the underscores like this:</span></span>

```md
![ADextension\_2FA\_Configure\_Step4](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

### <a name="apostrophes-and-quotation-marks"></a><span data-ttu-id="92e55-542">撇号和引号</span><span class="sxs-lookup"><span data-stu-id="92e55-542">Apostrophes and quotation marks</span></span>

<span data-ttu-id="92e55-543">如果将文本从 Word 复制到 Markdown 编辑器，文本可能包含“弯”撇号或弯引号。</span><span class="sxs-lookup"><span data-stu-id="92e55-543">If you copy from Word into a Markdown editor, the text might contain "smart" (curly) apostrophes or quotation marks.</span></span> <span data-ttu-id="92e55-544">需要将这些内容编码或更改为基本撇号或单引号。</span><span class="sxs-lookup"><span data-stu-id="92e55-544">These need to be encoded or changed to basic apostrophes or quotation marks.</span></span> <span data-ttu-id="92e55-545">否则，发布文件时，最终将得到：Itâ€™s</span><span class="sxs-lookup"><span data-stu-id="92e55-545">Otherwise, you end up with things like this when the file is published: Itâ€™s</span></span>

<span data-ttu-id="92e55-546">下面是关于这些“弯”版本标点符号的编码：</span><span class="sxs-lookup"><span data-stu-id="92e55-546">Here are the encodings for the "smart" versions of these punctuation marks:</span></span>

- <span data-ttu-id="92e55-547">左（开）引号：`&#8220;`</span><span class="sxs-lookup"><span data-stu-id="92e55-547">Left (opening) quotation mark: `&#8220;`</span></span>
- <span data-ttu-id="92e55-548">右（闭）引号：`&#8221;`</span><span class="sxs-lookup"><span data-stu-id="92e55-548">Right (closing) quotation mark: `&#8221;`</span></span>
- <span data-ttu-id="92e55-549">右单（闭）引号/撇号：`&#8217;`</span><span class="sxs-lookup"><span data-stu-id="92e55-549">Right (closing) single quotation mark or apostrophe: `&#8217;`</span></span>
- <span data-ttu-id="92e55-550">左单（开）引号（很少使用）：`&#8216;`</span><span class="sxs-lookup"><span data-stu-id="92e55-550">Left (opening) single quotation mark (rarely used): `&#8216;`</span></span>

### <a name="angle-brackets"></a><span data-ttu-id="92e55-551">尖括号</span><span class="sxs-lookup"><span data-stu-id="92e55-551">Angle brackets</span></span>

<span data-ttu-id="92e55-552">通常使用尖括号来表示占位符。</span><span class="sxs-lookup"><span data-stu-id="92e55-552">It is common to use angle brackets to denote a placeholder.</span></span> <span data-ttu-id="92e55-553">在文本（而不是代码）中执行此操作时，必须对尖括号进行编码。</span><span class="sxs-lookup"><span data-stu-id="92e55-553">When you do this in text (not code), you must encode the angle brackets.</span></span> <span data-ttu-id="92e55-554">否则，Markdown 会认为它们是一个 HTML 标记。</span><span class="sxs-lookup"><span data-stu-id="92e55-554">Otherwise, Markdown thinks that they're intended to be an HTML tag.</span></span>

<span data-ttu-id="92e55-555">例如，将 `<script name>` 编码为 `&lt;script name&gt;`</span><span class="sxs-lookup"><span data-stu-id="92e55-555">For example, encode `<script name>` as `&lt;script name&gt;`</span></span>

## <a name="markdown-flavor"></a><span data-ttu-id="92e55-556">Markdown 风格</span><span class="sxs-lookup"><span data-stu-id="92e55-556">Markdown flavor</span></span>

<span data-ttu-id="92e55-557">docs.microsoft.com 网站后端支持通过 [Markdig](https://github.com/lunet-io/markdig) 分析引擎进行分析的与 [CommonMark](https://commonmark.org/) 兼容的 Markdown。</span><span class="sxs-lookup"><span data-stu-id="92e55-557">The docs.microsoft.com site backend supports [CommonMark](https://commonmark.org/) compliant Markdown parsed through the [Markdig](https://github.com/lunet-io/markdig) parsing engine.</span></span> <span data-ttu-id="92e55-558">Markdown 风格大多与 [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/) 兼容，因为大多数 docs 存储在 GitHub 中，并可以在 GitHub 中进行编辑。</span><span class="sxs-lookup"><span data-stu-id="92e55-558">This markdown flavor is mostly compatible with [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/), as most docs are stored in GitHub and can be edited there.</span></span> <span data-ttu-id="92e55-559">通过 Markdown 扩展添加一些功能。</span><span class="sxs-lookup"><span data-stu-id="92e55-559">Additional functionality is added through Markdown extensions.</span></span>

## <a name="see-also"></a><span data-ttu-id="92e55-560">另请参阅：</span><span class="sxs-lookup"><span data-stu-id="92e55-560">See also:</span></span>

### <a name="markdown-resources"></a><span data-ttu-id="92e55-561">Markdown 资源</span><span class="sxs-lookup"><span data-stu-id="92e55-561">Markdown resources</span></span>

- [<span data-ttu-id="92e55-562">Markdown 简介</span><span class="sxs-lookup"><span data-stu-id="92e55-562">Introduction to Markdown</span></span>](https://daringfireball.net/projects/markdown/syntax)
- [<span data-ttu-id="92e55-563">Docs Markdown 备忘单</span><span class="sxs-lookup"><span data-stu-id="92e55-563">Docs Markdown cheat sheet</span></span>](./media/documents/markdown-cheatsheet.pdf?raw=true)
- [<span data-ttu-id="92e55-564">GitHub 的 Markdown 基础知识</span><span class="sxs-lookup"><span data-stu-id="92e55-564">GitHub's Markdown Basics</span></span>](https://help.github.com/articles/markdown-basics/)
- [<span data-ttu-id="92e55-565">Markdown 指南</span><span class="sxs-lookup"><span data-stu-id="92e55-565">The Markdown Guide</span></span>](https://www.markdownguide.org/)
