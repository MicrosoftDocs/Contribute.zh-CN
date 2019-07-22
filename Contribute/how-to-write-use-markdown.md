---
title: 如何使用 Markdown 撰写 Docs
description: 本文提供用于撰写 docs.microsoft.com 文章的 Markdown 语言的基础知识和参考信息。
ms.date: 03/26/2019
ms.openlocfilehash: 9fcd76e6103761465815784e4bf24e7042fb9f34
ms.sourcegitcommit: 5f7212a091e9fc4e9cd1320fdfa8efaff51384c7
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/29/2019
ms.locfileid: "66373109"
---
# <a name="how-to-use-markdown-for-writing-docs"></a><span data-ttu-id="3ec80-103">如何使用 Markdown 撰写 Docs</span><span class="sxs-lookup"><span data-stu-id="3ec80-103">How to use Markdown for writing Docs</span></span>

<span data-ttu-id="3ec80-104">[Docs.microsoft.com](http://docs.microsoft.com) 文章采用名为 [Markdown](https://daringfireball.net/projects/markdown/) 的轻型标记语言撰写，这种语言可读性强且简单易学。</span><span class="sxs-lookup"><span data-stu-id="3ec80-104">[Docs.microsoft.com](http://docs.microsoft.com) articles are written in a lightweight markup language called [Markdown](https://daringfireball.net/projects/markdown/), which is both easy to read and easy to learn.</span></span> <span data-ttu-id="3ec80-105">正因为如此，Markdown 已迅速成为行业标准。</span><span class="sxs-lookup"><span data-stu-id="3ec80-105">Because of this, it has quickly become an industry standard.</span></span> <span data-ttu-id="3ec80-106">Docs 站点使用 Markdown 的 [Markdig 风格](#markdown-flavor)。</span><span class="sxs-lookup"><span data-stu-id="3ec80-106">The docs site uses the [Markdig flavor](#markdown-flavor) of Markdown.</span></span>


## <a name="markdown-basics"></a><span data-ttu-id="3ec80-107">Markdown 基础知识</span><span class="sxs-lookup"><span data-stu-id="3ec80-107">Markdown basics</span></span>

### <a name="headings"></a><span data-ttu-id="3ec80-108">标题</span><span class="sxs-lookup"><span data-stu-id="3ec80-108">Headings</span></span>

<span data-ttu-id="3ec80-109">要创建标题，请使用井号标记 (#)，如下所示：</span><span class="sxs-lookup"><span data-stu-id="3ec80-109">To create a heading, you use a hash mark (#), as follows:</span></span>

```markdown
# This is heading 1
## This is heading 2
### This is heading 3
#### This is heading 4
```

<span data-ttu-id="3ec80-110">应使用 atx 样式完成标题，即在行的开头使用 1-6 个哈希字符 (#) 指示标题，对应 HTML 标题级别 H1 到 H6。</span><span class="sxs-lookup"><span data-stu-id="3ec80-110">Headings should be done using atx-style, that is, use 1-6 hash characters (#) at the start of the line to indicate a heading, corresponding to HTML headings levels H1 through H6.</span></span> <span data-ttu-id="3ec80-111">上述示例使用的是一级到四级的标题。</span><span class="sxs-lookup"><span data-stu-id="3ec80-111">Examples of first- through fourth-level headers are used above.</span></span>

<span data-ttu-id="3ec80-112">主题中只能有一个一级标题 (H1)，将显示为页面内标题  。</span><span class="sxs-lookup"><span data-stu-id="3ec80-112">There **must** be only one first-level heading (H1) in your topic, which will be displayed as the on-page title.</span></span>

<span data-ttu-id="3ec80-113">如果标题以 `#` 字符结尾，则需要在末尾添加额外的 `#` 字符，使标题正确呈现。</span><span class="sxs-lookup"><span data-stu-id="3ec80-113">If your heading finishes with a `#` character, you need to add an extra `#` character in the end in order for the title to render correctly.</span></span> <span data-ttu-id="3ec80-114">例如，`# Async Programming in F# #`。</span><span class="sxs-lookup"><span data-stu-id="3ec80-114">For example, `# Async Programming in F# #`.</span></span>

<span data-ttu-id="3ec80-115">二级标题将生成页面内 TOC，在页面内标题下方的“本文内容”中显示。</span><span class="sxs-lookup"><span data-stu-id="3ec80-115">Second-level headings will generate the on-page TOC that appears in the "In this article" section underneath the on-page title.</span></span>

### <a name="bold-and-italic-text"></a><span data-ttu-id="3ec80-116">粗体和斜体文本</span><span class="sxs-lookup"><span data-stu-id="3ec80-116">Bold and italic text</span></span>

<span data-ttu-id="3ec80-117">要将文本设置为粗体格式，请用两个星号括住文本  ：</span><span class="sxs-lookup"><span data-stu-id="3ec80-117">To format text as **bold**, you enclose it in two asterisks:</span></span>

```markdown
This text is **bold**.
```

<span data-ttu-id="3ec80-118">要将文本设置为斜体格式，请用一个星号括住文本  ：</span><span class="sxs-lookup"><span data-stu-id="3ec80-118">To format text as *italic*, you enclose it in a single asterisk:</span></span>

```markdown
This text is *italic*.
```

<span data-ttu-id="3ec80-119">要将文本同时设置为粗体和斜体格式，请用三个星号括住文本：</span><span class="sxs-lookup"><span data-stu-id="3ec80-119">To format text as both ***bold and italic***, you enclose it in three asterisks:</span></span>

```markdown
This is text is both ***bold and italic***.
```

### <a name="blockquotes"></a><span data-ttu-id="3ec80-120">块引用</span><span class="sxs-lookup"><span data-stu-id="3ec80-120">Blockquotes</span></span>

<span data-ttu-id="3ec80-121">块引用使用 `>` 字符创建：</span><span class="sxs-lookup"><span data-stu-id="3ec80-121">Blockquotes are created using the `>` character:</span></span>

```markdown
> The drought had lasted now for ten million years, and the reign of the terrible lizards had long since ended. Here on the Equator, in the continent which would one day be known as Africa, the battle for existence had reached a new climax of ferocity, and the victor was not yet in sight. In this barren and desiccated land, only the small or the swift or the fierce could flourish, or even hope to survive.
```

<span data-ttu-id="3ec80-122">上述示例的呈现如下所示：</span><span class="sxs-lookup"><span data-stu-id="3ec80-122">The preceding example renders as follows:</span></span>

> <span data-ttu-id="3ec80-123">干旱迄今为止已持续一千万年，恐怖蜥蜴的统治时代早已结束。</span><span class="sxs-lookup"><span data-stu-id="3ec80-123">The drought had lasted now for ten million years, and the reign of the terrible lizards had long since ended.</span></span> <span data-ttu-id="3ec80-124">赤道上，在将有一天会以“非洲”闻名的大陆上，生存的战斗已经达到新一轮残暴的高潮，胜负未分。</span><span class="sxs-lookup"><span data-stu-id="3ec80-124">Here on the Equator, in the continent which would one day be known as Africa, the battle for existence had reached a new climax of ferocity, and the victor was not yet in sight.</span></span> <span data-ttu-id="3ec80-125">在这片贫瘠、干枯的土地上，只有体型较小或动作迅捷或凶猛的物种才能繁荣，乃至于有希望幸存。</span><span class="sxs-lookup"><span data-stu-id="3ec80-125">In this barren and desiccated land, only the small or the swift or the fierce could flourish, or even hope to survive.</span></span>

### <a name="lists"></a><span data-ttu-id="3ec80-126">列表</span><span class="sxs-lookup"><span data-stu-id="3ec80-126">Lists</span></span>

#### <a name="unordered-list"></a><span data-ttu-id="3ec80-127">无序列表</span><span class="sxs-lookup"><span data-stu-id="3ec80-127">Unordered list</span></span>

<span data-ttu-id="3ec80-128">要为无序列表/项目符号列表设置格式，可以使用星号或短划线。</span><span class="sxs-lookup"><span data-stu-id="3ec80-128">To format an unordered/bulleted list, you can use either asterisks or dashes.</span></span> <span data-ttu-id="3ec80-129">例如，以下 Markdown：</span><span class="sxs-lookup"><span data-stu-id="3ec80-129">For example, the following Markdown:</span></span>

```markdown
- List item 1
- List item 2
- List item 3
```

<span data-ttu-id="3ec80-130">将显示为：</span><span class="sxs-lookup"><span data-stu-id="3ec80-130">will be rendered as:</span></span>

- <span data-ttu-id="3ec80-131">List item 1</span><span class="sxs-lookup"><span data-stu-id="3ec80-131">List item 1</span></span>
- <span data-ttu-id="3ec80-132">List item 2</span><span class="sxs-lookup"><span data-stu-id="3ec80-132">List item 2</span></span>
- <span data-ttu-id="3ec80-133">List item 3</span><span class="sxs-lookup"><span data-stu-id="3ec80-133">List item 3</span></span>

<span data-ttu-id="3ec80-134">要将一个列表嵌套在另一个列表中，请缩进子列表项。</span><span class="sxs-lookup"><span data-stu-id="3ec80-134">To nest a list within another list, indent the child list items.</span></span> <span data-ttu-id="3ec80-135">例如，以下 Markdown：</span><span class="sxs-lookup"><span data-stu-id="3ec80-135">For example, the following Markdown:</span></span>

```markdown
- List item 1
  - List item A
  - List item B
- List item 2
```

<span data-ttu-id="3ec80-136">将显示为：</span><span class="sxs-lookup"><span data-stu-id="3ec80-136">will be rendered as:</span></span>

- <span data-ttu-id="3ec80-137">List item 1</span><span class="sxs-lookup"><span data-stu-id="3ec80-137">List item 1</span></span>
  - <span data-ttu-id="3ec80-138">List item A</span><span class="sxs-lookup"><span data-stu-id="3ec80-138">List item A</span></span>
  - <span data-ttu-id="3ec80-139">List item B</span><span class="sxs-lookup"><span data-stu-id="3ec80-139">List item B</span></span>
- <span data-ttu-id="3ec80-140">List item 2</span><span class="sxs-lookup"><span data-stu-id="3ec80-140">List item 2</span></span>

#### <a name="ordered-list"></a><span data-ttu-id="3ec80-141">有序列表</span><span class="sxs-lookup"><span data-stu-id="3ec80-141">Ordered list</span></span>

<span data-ttu-id="3ec80-142">要设置有序/分阶段列表的格式，可以使用相应的编号。</span><span class="sxs-lookup"><span data-stu-id="3ec80-142">To format an ordered/stepwise list, you use corresponding numbers.</span></span> <span data-ttu-id="3ec80-143">例如，以下 Markdown：</span><span class="sxs-lookup"><span data-stu-id="3ec80-143">For example, the following Markdown:</span></span>

```markdown
1. First instruction
1. Second instruction
1. Third instruction
```

<span data-ttu-id="3ec80-144">将显示为：</span><span class="sxs-lookup"><span data-stu-id="3ec80-144">will be rendered as:</span></span>

1. <span data-ttu-id="3ec80-145">First instruction</span><span class="sxs-lookup"><span data-stu-id="3ec80-145">First instruction</span></span>
2. <span data-ttu-id="3ec80-146">Second instruction</span><span class="sxs-lookup"><span data-stu-id="3ec80-146">Second instruction</span></span>
3. <span data-ttu-id="3ec80-147">Third instruction</span><span class="sxs-lookup"><span data-stu-id="3ec80-147">Third instruction</span></span>

<span data-ttu-id="3ec80-148">要将一个列表嵌套在另一个列表中，请缩进子列表项。</span><span class="sxs-lookup"><span data-stu-id="3ec80-148">To nest a list within another list, indent the child list items.</span></span> <span data-ttu-id="3ec80-149">例如，以下 Markdown：</span><span class="sxs-lookup"><span data-stu-id="3ec80-149">For example, the following Markdown:</span></span>

```markdown
1. First instruction
   1. Sub-instruction
   1. Sub-instruction
1. Second instruction
```

<span data-ttu-id="3ec80-150">将显示为：</span><span class="sxs-lookup"><span data-stu-id="3ec80-150">will be rendered as:</span></span>

1. <span data-ttu-id="3ec80-151">First instruction</span><span class="sxs-lookup"><span data-stu-id="3ec80-151">First instruction</span></span>
   1. <span data-ttu-id="3ec80-152">Sub-instruction</span><span class="sxs-lookup"><span data-stu-id="3ec80-152">Sub-instruction</span></span>
   2. <span data-ttu-id="3ec80-153">Sub-instruction</span><span class="sxs-lookup"><span data-stu-id="3ec80-153">Sub-instruction</span></span>
2. <span data-ttu-id="3ec80-154">Second instruction</span><span class="sxs-lookup"><span data-stu-id="3ec80-154">Second instruction</span></span>

<span data-ttu-id="3ec80-155">注意：我们对所有条目</span><span class="sxs-lookup"><span data-stu-id="3ec80-155">Note that we use '1.'</span></span> <span data-ttu-id="3ec80-156">均使用“1.”。</span><span class="sxs-lookup"><span data-stu-id="3ec80-156">for all entries.</span></span> <span data-ttu-id="3ec80-157">当后续更新包括新步骤或要删除现有步骤时，这样更易于评审差异。</span><span class="sxs-lookup"><span data-stu-id="3ec80-157">It makes diffs easier to review when later updates include new steps or remove existing steps.</span></span>

### <a name="tables"></a><span data-ttu-id="3ec80-158">表格</span><span class="sxs-lookup"><span data-stu-id="3ec80-158">Tables</span></span>

<span data-ttu-id="3ec80-159">表格不属于核心 Markdown 规范，但是它们受 GFM 支持。</span><span class="sxs-lookup"><span data-stu-id="3ec80-159">Tables are not part of the core Markdown specification, but GFM supports them.</span></span> <span data-ttu-id="3ec80-160">可以使用竖线 (|) 和连字符 (-) 字符创建表格。</span><span class="sxs-lookup"><span data-stu-id="3ec80-160">You can create tables by using the pipe (|) and hyphen (-) characters.</span></span> <span data-ttu-id="3ec80-161">连字符用于创建每列的标题，而竖线用于分隔每列。</span><span class="sxs-lookup"><span data-stu-id="3ec80-161">Hyphens create each column's header, while pipes separate each column.</span></span> <span data-ttu-id="3ec80-162">请在表格前面加入一个空行，使它能够正确显示。</span><span class="sxs-lookup"><span data-stu-id="3ec80-162">Include a blank line before your table so it's rendered correctly.</span></span>

<span data-ttu-id="3ec80-163">例如，以下 Markdown：</span><span class="sxs-lookup"><span data-stu-id="3ec80-163">For example, the following Markdown:</span></span>

```markdown
| Fun                  | With                 | Tables          |
| :------------------- | -------------------: |:---------------:|
| left-aligned column  | right-aligned column | centered column |
| $100                 | $100                 | $100            |
| $10                  | $10                  | $10             |
| $1                   | $1                   | $1              |
```

<span data-ttu-id="3ec80-164">将显示为：</span><span class="sxs-lookup"><span data-stu-id="3ec80-164">Will be rendered as:</span></span>

| <span data-ttu-id="3ec80-165">Fun</span><span class="sxs-lookup"><span data-stu-id="3ec80-165">Fun</span></span>                  | <span data-ttu-id="3ec80-166">With</span><span class="sxs-lookup"><span data-stu-id="3ec80-166">With</span></span>                 | <span data-ttu-id="3ec80-167">Tables</span><span class="sxs-lookup"><span data-stu-id="3ec80-167">Tables</span></span>          |
| :------------------- | -------------------: |:---------------:|
| <span data-ttu-id="3ec80-168">left-aligned column</span><span class="sxs-lookup"><span data-stu-id="3ec80-168">left-aligned column</span></span>  | <span data-ttu-id="3ec80-169">right-aligned column</span><span class="sxs-lookup"><span data-stu-id="3ec80-169">right-aligned column</span></span> | <span data-ttu-id="3ec80-170">centered column</span><span class="sxs-lookup"><span data-stu-id="3ec80-170">centered column</span></span> |
| <span data-ttu-id="3ec80-171">$100</span><span class="sxs-lookup"><span data-stu-id="3ec80-171">$100</span></span>                 | <span data-ttu-id="3ec80-172">$100</span><span class="sxs-lookup"><span data-stu-id="3ec80-172">$100</span></span>                 | <span data-ttu-id="3ec80-173">$100</span><span class="sxs-lookup"><span data-stu-id="3ec80-173">$100</span></span>            |
| <span data-ttu-id="3ec80-174">$10</span><span class="sxs-lookup"><span data-stu-id="3ec80-174">$10</span></span>                  | <span data-ttu-id="3ec80-175">$10</span><span class="sxs-lookup"><span data-stu-id="3ec80-175">$10</span></span>                  | <span data-ttu-id="3ec80-176">$10</span><span class="sxs-lookup"><span data-stu-id="3ec80-176">$10</span></span>             |
| <span data-ttu-id="3ec80-177">$1</span><span class="sxs-lookup"><span data-stu-id="3ec80-177">$1</span></span>                   | <span data-ttu-id="3ec80-178">$1</span><span class="sxs-lookup"><span data-stu-id="3ec80-178">$1</span></span>                   | <span data-ttu-id="3ec80-179">$1</span><span class="sxs-lookup"><span data-stu-id="3ec80-179">$1</span></span>              |

<span data-ttu-id="3ec80-180">有关创建表格的详细信息，请参阅：</span><span class="sxs-lookup"><span data-stu-id="3ec80-180">For more information on creating tables, see:</span></span>

- <span data-ttu-id="3ec80-181">GitHub 的[使用表格整理信息](https://help.github.com/articles/organizing-information-with-tables/)。</span><span class="sxs-lookup"><span data-stu-id="3ec80-181">GitHub's [Organizing information with tables](https://help.github.com/articles/organizing-information-with-tables/).</span></span>
- <span data-ttu-id="3ec80-182">[Markdown 表格生成器](https://www.tablesgenerator.com/markdown_tables) Web 应用。</span><span class="sxs-lookup"><span data-stu-id="3ec80-182">The [Markdown Tables Generator](https://www.tablesgenerator.com/markdown_tables) web app.</span></span>
- <span data-ttu-id="3ec80-183">[Adam Pritchard 的 Markdown 备忘单](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#wiki-tables)。</span><span class="sxs-lookup"><span data-stu-id="3ec80-183">[Adam Pritchard's Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#wiki-tables).</span></span>
- <span data-ttu-id="3ec80-184">[Michel Fortin 的 Markdown Extra](https://michelf.ca/projects/php-markdown/extra/#table)。</span><span class="sxs-lookup"><span data-stu-id="3ec80-184">[Michel Fortin's Markdown Extra](https://michelf.ca/projects/php-markdown/extra/#table).</span></span>
- <span data-ttu-id="3ec80-185">[将 HTML 表转换为 Markdown 格式](https://jmalarcon.github.io/markdowntables/)。</span><span class="sxs-lookup"><span data-stu-id="3ec80-185">[Convert HTML tables to Markdown](https://jmalarcon.github.io/markdowntables/).</span></span>

### <a name="links"></a><span data-ttu-id="3ec80-186">链接</span><span class="sxs-lookup"><span data-stu-id="3ec80-186">Links</span></span>

<span data-ttu-id="3ec80-187">Markdown 的内联链接语法由两部分组成：`[link text]` 部分，这是要创建为超链接的文本；后跟 `(file-name.md)` 部分，这是要链接到的 URL 或者文件名：</span><span class="sxs-lookup"><span data-stu-id="3ec80-187">The Markdown syntax for an inline link consists of the `[link text]` portion, which is the text that will be hyperlinked, followed by the `(file-name.md)` portion, which is the URL or file name that's being linked to:</span></span>

 `[link text](file-name.md)`

<span data-ttu-id="3ec80-188">有关链接的详细信息，请参阅：</span><span class="sxs-lookup"><span data-stu-id="3ec80-188">For more information on linking, see:</span></span>

- <span data-ttu-id="3ec80-189">[Markdown 语法指南](https://daringfireball.net/projects/markdown/syntax#link)，详细了解 Markdown 的基本链接支持相关信息。</span><span class="sxs-lookup"><span data-stu-id="3ec80-189">The [Markdown syntax guide](https://daringfireball.net/projects/markdown/syntax#link) for details on Markdown's base linking support.</span></span>
- <span data-ttu-id="3ec80-190">参阅本指南的[链接](how-to-write-links.md)部分，深入了解 Markdig 提供的其他链接语法。</span><span class="sxs-lookup"><span data-stu-id="3ec80-190">The [Links](how-to-write-links.md) section of this guide for details on the additional linking syntax that Markdig provides.</span></span>

### <a name="code-snippets"></a><span data-ttu-id="3ec80-191">代码片段</span><span class="sxs-lookup"><span data-stu-id="3ec80-191">Code snippets</span></span>

<span data-ttu-id="3ec80-192">Markdown 不仅支持将代码片段内联在某个句子中，还支持将它作为单独的“隔离”块放置在两个句子之间。</span><span class="sxs-lookup"><span data-stu-id="3ec80-192">Markdown supports the placement of code snippets both inline in a sentence and as a separate "fenced" block between sentences.</span></span> <span data-ttu-id="3ec80-193">有关详细信息，请参阅：</span><span class="sxs-lookup"><span data-stu-id="3ec80-193">For details, see:</span></span>

- [<span data-ttu-id="3ec80-194">Markdown 代码块本机支持</span><span class="sxs-lookup"><span data-stu-id="3ec80-194">Markdown's native support for code blocks</span></span>](https://daringfireball.net/projects/markdown/syntax#precode)
- [<span data-ttu-id="3ec80-195">针对代码隔离和语法高亮显示的 GFM 支持</span><span class="sxs-lookup"><span data-stu-id="3ec80-195">GFM support for code fencing and syntax highlighting</span></span>](https://help.github.com/articles/creating-and-highlighting-code-blocks/)

<span data-ttu-id="3ec80-196">借助隔离代码块，可以轻松实现代码片段的语法高亮显示。</span><span class="sxs-lookup"><span data-stu-id="3ec80-196">Fenced code blocks are an easy way to enable syntax highlighting for your code snippets.</span></span> <span data-ttu-id="3ec80-197">隔离代码块的一般格式为：</span><span class="sxs-lookup"><span data-stu-id="3ec80-197">The general format for fenced code blocks is:</span></span>

    ```alias
    ...
    your code goes in here
    ...
    ```

<span data-ttu-id="3ec80-198">开头的三个撇号 (\`) 字符后面的别名定义要使用的语法高亮显示。</span><span class="sxs-lookup"><span data-stu-id="3ec80-198">The alias after the initial three backtick (\`) characters defines the syntax highlighting to be used.</span></span> <span data-ttu-id="3ec80-199">下面列出了 Docs 内容中常用的编程语言以及匹配的标签：</span><span class="sxs-lookup"><span data-stu-id="3ec80-199">The following is a list of commonly used programming languages in Docs content and the matching label:</span></span>

<span data-ttu-id="3ec80-200">这些语言支持友好名称并且大多数都可以突出显示语言。</span><span class="sxs-lookup"><span data-stu-id="3ec80-200">These languages have friendly name support and most have language highlighting.</span></span>

|<span data-ttu-id="3ec80-201">名称</span><span class="sxs-lookup"><span data-stu-id="3ec80-201">Name</span></span>|<span data-ttu-id="3ec80-202">Markdown 标签</span><span class="sxs-lookup"><span data-stu-id="3ec80-202">Markdown Label</span></span>|
|-----|-------|
|<span data-ttu-id="3ec80-203">.NET 控制台</span><span class="sxs-lookup"><span data-stu-id="3ec80-203">.NET Console</span></span>|<span data-ttu-id="3ec80-204">dotnetcli</span><span class="sxs-lookup"><span data-stu-id="3ec80-204">dotnetcli</span></span>|
|<span data-ttu-id="3ec80-205">ASP.NET (C#)</span><span class="sxs-lookup"><span data-stu-id="3ec80-205">ASP.NET (C#)</span></span>|<span data-ttu-id="3ec80-206">aspx-csharp</span><span class="sxs-lookup"><span data-stu-id="3ec80-206">aspx-csharp</span></span>|
|<span data-ttu-id="3ec80-207">ASP.NET (VB)</span><span class="sxs-lookup"><span data-stu-id="3ec80-207">ASP.NET (VB)</span></span>|<span data-ttu-id="3ec80-208">aspx-vb</span><span class="sxs-lookup"><span data-stu-id="3ec80-208">aspx-vb</span></span>|
|<span data-ttu-id="3ec80-209">AzCopy</span><span class="sxs-lookup"><span data-stu-id="3ec80-209">AzCopy</span></span>|<span data-ttu-id="3ec80-210">azcopy</span><span class="sxs-lookup"><span data-stu-id="3ec80-210">azcopy</span></span>|
|<span data-ttu-id="3ec80-211">Azure CLI</span><span class="sxs-lookup"><span data-stu-id="3ec80-211">Azure CLI</span></span>|<span data-ttu-id="3ec80-212">azurecli</span><span class="sxs-lookup"><span data-stu-id="3ec80-212">azurecli</span></span>|
|<span data-ttu-id="3ec80-213">Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="3ec80-213">Azure PowerShell</span></span>|<span data-ttu-id="3ec80-214">azurepowershell</span><span class="sxs-lookup"><span data-stu-id="3ec80-214">azurepowershell</span></span>|
|<span data-ttu-id="3ec80-215">Bash</span><span class="sxs-lookup"><span data-stu-id="3ec80-215">Bash</span></span>|<span data-ttu-id="3ec80-216">bash</span><span class="sxs-lookup"><span data-stu-id="3ec80-216">bash</span></span>|
|<span data-ttu-id="3ec80-217">C++</span><span class="sxs-lookup"><span data-stu-id="3ec80-217">C++</span></span>|<span data-ttu-id="3ec80-218">cpp</span><span class="sxs-lookup"><span data-stu-id="3ec80-218">cpp</span></span>|
|<span data-ttu-id="3ec80-219">C++/CX</span><span class="sxs-lookup"><span data-stu-id="3ec80-219">C++/CX</span></span>|<span data-ttu-id="3ec80-220">cppcx</span><span class="sxs-lookup"><span data-stu-id="3ec80-220">cppcx</span></span>|
|<span data-ttu-id="3ec80-221">C++/WinRT</span><span class="sxs-lookup"><span data-stu-id="3ec80-221">C++/WinRT</span></span>|<span data-ttu-id="3ec80-222">cppwinrt</span><span class="sxs-lookup"><span data-stu-id="3ec80-222">cppwinrt</span></span>|
|<span data-ttu-id="3ec80-223">C#</span><span class="sxs-lookup"><span data-stu-id="3ec80-223">C#</span></span>|<span data-ttu-id="3ec80-224">csharp</span><span class="sxs-lookup"><span data-stu-id="3ec80-224">csharp</span></span>|
|<span data-ttu-id="3ec80-225">浏览器中的 C#</span><span class="sxs-lookup"><span data-stu-id="3ec80-225">C# in browser</span></span>|<span data-ttu-id="3ec80-226">csharp-interactive</span><span class="sxs-lookup"><span data-stu-id="3ec80-226">csharp-interactive</span></span>|
|<span data-ttu-id="3ec80-227">控制台</span><span class="sxs-lookup"><span data-stu-id="3ec80-227">Console</span></span>|<span data-ttu-id="3ec80-228">console</span><span class="sxs-lookup"><span data-stu-id="3ec80-228">console</span></span>|
|<span data-ttu-id="3ec80-229">CSHTML</span><span class="sxs-lookup"><span data-stu-id="3ec80-229">CSHTML</span></span>|<span data-ttu-id="3ec80-230">cshtml</span><span class="sxs-lookup"><span data-stu-id="3ec80-230">cshtml</span></span>|
|<span data-ttu-id="3ec80-231">DAX</span><span class="sxs-lookup"><span data-stu-id="3ec80-231">DAX</span></span>|<span data-ttu-id="3ec80-232">dax</span><span class="sxs-lookup"><span data-stu-id="3ec80-232">dax</span></span>|
|<span data-ttu-id="3ec80-233">Docker</span><span class="sxs-lookup"><span data-stu-id="3ec80-233">Docker</span></span>|<span data-ttu-id="3ec80-234">dockerfile</span><span class="sxs-lookup"><span data-stu-id="3ec80-234">dockerfile</span></span>|
|<span data-ttu-id="3ec80-235">F#</span><span class="sxs-lookup"><span data-stu-id="3ec80-235">F#</span></span>|<span data-ttu-id="3ec80-236">fsharp</span><span class="sxs-lookup"><span data-stu-id="3ec80-236">fsharp</span></span>|
|<span data-ttu-id="3ec80-237">Go</span><span class="sxs-lookup"><span data-stu-id="3ec80-237">Go</span></span>|<span data-ttu-id="3ec80-238">go</span><span class="sxs-lookup"><span data-stu-id="3ec80-238">go</span></span>|
|<span data-ttu-id="3ec80-239">HTML</span><span class="sxs-lookup"><span data-stu-id="3ec80-239">HTML</span></span>|<span data-ttu-id="3ec80-240">html</span><span class="sxs-lookup"><span data-stu-id="3ec80-240">html</span></span>|
|<span data-ttu-id="3ec80-241">HTTP</span><span class="sxs-lookup"><span data-stu-id="3ec80-241">HTTP</span></span>|<span data-ttu-id="3ec80-242">http</span><span class="sxs-lookup"><span data-stu-id="3ec80-242">http</span></span>|
|<span data-ttu-id="3ec80-243">Java</span><span class="sxs-lookup"><span data-stu-id="3ec80-243">Java</span></span>|<span data-ttu-id="3ec80-244">java</span><span class="sxs-lookup"><span data-stu-id="3ec80-244">java</span></span>|
|<span data-ttu-id="3ec80-245">JavaScript</span><span class="sxs-lookup"><span data-stu-id="3ec80-245">JavaScript</span></span>|<span data-ttu-id="3ec80-246">javascript</span><span class="sxs-lookup"><span data-stu-id="3ec80-246">javascript</span></span>|
|<span data-ttu-id="3ec80-247">JSON</span><span class="sxs-lookup"><span data-stu-id="3ec80-247">JSON</span></span>|<span data-ttu-id="3ec80-248">json</span><span class="sxs-lookup"><span data-stu-id="3ec80-248">json</span></span>|
|<span data-ttu-id="3ec80-249">Kusto 查询语言</span><span class="sxs-lookup"><span data-stu-id="3ec80-249">Kusto Query Language</span></span>|<span data-ttu-id="3ec80-250">kusto</span><span class="sxs-lookup"><span data-stu-id="3ec80-250">kusto</span></span>|
|<span data-ttu-id="3ec80-251">Markdown</span><span class="sxs-lookup"><span data-stu-id="3ec80-251">Markdown</span></span>|<span data-ttu-id="3ec80-252">md</span><span class="sxs-lookup"><span data-stu-id="3ec80-252">md</span></span>|
|<span data-ttu-id="3ec80-253">Objective-C</span><span class="sxs-lookup"><span data-stu-id="3ec80-253">Objective-C</span></span>|<span data-ttu-id="3ec80-254">objc</span><span class="sxs-lookup"><span data-stu-id="3ec80-254">objc</span></span>|
|<span data-ttu-id="3ec80-255">OData</span><span class="sxs-lookup"><span data-stu-id="3ec80-255">OData</span></span>|<span data-ttu-id="3ec80-256">odata</span><span class="sxs-lookup"><span data-stu-id="3ec80-256">odata</span></span>|
|<span data-ttu-id="3ec80-257">PHP</span><span class="sxs-lookup"><span data-stu-id="3ec80-257">PHP</span></span>|<span data-ttu-id="3ec80-258">php</span><span class="sxs-lookup"><span data-stu-id="3ec80-258">php</span></span>|
|<span data-ttu-id="3ec80-259">PowerApps（小数点分隔符）</span><span class="sxs-lookup"><span data-stu-id="3ec80-259">PowerApps (dot decimal separator)</span></span>|<span data-ttu-id="3ec80-260">powerapps-dot</span><span class="sxs-lookup"><span data-stu-id="3ec80-260">powerapps-dot</span></span>|
|<span data-ttu-id="3ec80-261">PowerApps（逗号分隔符）</span><span class="sxs-lookup"><span data-stu-id="3ec80-261">PowerApps (comma decimal separator)</span></span>|<span data-ttu-id="3ec80-262">powerapps-comma</span><span class="sxs-lookup"><span data-stu-id="3ec80-262">powerapps-comma</span></span>|
|<span data-ttu-id="3ec80-263">PowerShell</span><span class="sxs-lookup"><span data-stu-id="3ec80-263">PowerShell</span></span>|<span data-ttu-id="3ec80-264">powershell</span><span class="sxs-lookup"><span data-stu-id="3ec80-264">powershell</span></span>|
|<span data-ttu-id="3ec80-265">Python</span><span class="sxs-lookup"><span data-stu-id="3ec80-265">Python</span></span>|<span data-ttu-id="3ec80-266">python</span><span class="sxs-lookup"><span data-stu-id="3ec80-266">python</span></span>|
|<span data-ttu-id="3ec80-267">Q#</span><span class="sxs-lookup"><span data-stu-id="3ec80-267">Q#</span></span>|<span data-ttu-id="3ec80-268">qsharp</span><span class="sxs-lookup"><span data-stu-id="3ec80-268">qsharp</span></span>|
|<span data-ttu-id="3ec80-269">R</span><span class="sxs-lookup"><span data-stu-id="3ec80-269">R</span></span>|<span data-ttu-id="3ec80-270">r</span><span class="sxs-lookup"><span data-stu-id="3ec80-270">r</span></span>|
|<span data-ttu-id="3ec80-271">Ruby</span><span class="sxs-lookup"><span data-stu-id="3ec80-271">Ruby</span></span>|<span data-ttu-id="3ec80-272">ruby</span><span class="sxs-lookup"><span data-stu-id="3ec80-272">ruby</span></span>|
|<span data-ttu-id="3ec80-273">SQL</span><span class="sxs-lookup"><span data-stu-id="3ec80-273">SQL</span></span>|<span data-ttu-id="3ec80-274">sql</span><span class="sxs-lookup"><span data-stu-id="3ec80-274">sql</span></span>|
|<span data-ttu-id="3ec80-275">Swift</span><span class="sxs-lookup"><span data-stu-id="3ec80-275">Swift</span></span>|<span data-ttu-id="3ec80-276">swift</span><span class="sxs-lookup"><span data-stu-id="3ec80-276">swift</span></span>|
|<span data-ttu-id="3ec80-277">TypeScript</span><span class="sxs-lookup"><span data-stu-id="3ec80-277">TypeScript</span></span>|<span data-ttu-id="3ec80-278">typescript</span><span class="sxs-lookup"><span data-stu-id="3ec80-278">typescript</span></span>|
|<span data-ttu-id="3ec80-279">VB</span><span class="sxs-lookup"><span data-stu-id="3ec80-279">VB</span></span>|<span data-ttu-id="3ec80-280">vb</span><span class="sxs-lookup"><span data-stu-id="3ec80-280">vb</span></span>|
|<span data-ttu-id="3ec80-281">XAML</span><span class="sxs-lookup"><span data-stu-id="3ec80-281">XAML</span></span>|<span data-ttu-id="3ec80-282">xaml</span><span class="sxs-lookup"><span data-stu-id="3ec80-282">xaml</span></span>|
|<span data-ttu-id="3ec80-283">XML</span><span class="sxs-lookup"><span data-stu-id="3ec80-283">XML</span></span>|<span data-ttu-id="3ec80-284">xml</span><span class="sxs-lookup"><span data-stu-id="3ec80-284">xml</span></span>|

<span data-ttu-id="3ec80-285">`csharp-interactive` 名称指定 C# 语言，以及从浏览器中运行示例的能力。</span><span class="sxs-lookup"><span data-stu-id="3ec80-285">The `csharp-interactive` name specifies the C# language, and the ability to run the samples from the browser.</span></span> <span data-ttu-id="3ec80-286">这些代码片段在 Docker 容器中进行编译和执行，并且该程序执行的结果在用户浏览器窗口中显示。</span><span class="sxs-lookup"><span data-stu-id="3ec80-286">These snippets are compiled and executed in a Docker container, and the results of that program execution are displayed in the user's browser window.</span></span>

#### <a name="example-c"></a><span data-ttu-id="3ec80-287">示例：C\#</span><span class="sxs-lookup"><span data-stu-id="3ec80-287">Example: C\#</span></span>

<span data-ttu-id="3ec80-288">__Markdown__</span><span class="sxs-lookup"><span data-stu-id="3ec80-288">__Markdown__</span></span>

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

<span data-ttu-id="3ec80-289">__呈现__</span><span class="sxs-lookup"><span data-stu-id="3ec80-289">__Render__</span></span>

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

#### <a name="example-sql"></a><span data-ttu-id="3ec80-290">示例：SQL</span><span class="sxs-lookup"><span data-stu-id="3ec80-290">Example: SQL</span></span>

<span data-ttu-id="3ec80-291">__Markdown__</span><span class="sxs-lookup"><span data-stu-id="3ec80-291">__Markdown__</span></span>

    ```sql
    CREATE TABLE T1 (
      c1 int PRIMARY KEY,
      c2 varchar(50) SPARSE NULL
    );
    ```

<span data-ttu-id="3ec80-292">__呈现__</span><span class="sxs-lookup"><span data-stu-id="3ec80-292">__Render__</span></span>

```sql
CREATE TABLE T1 (
  c1 int PRIMARY KEY,
  c2 varchar(50) SPARSE NULL
);
```

## <a name="ops-custom-markdown-extensions"></a><span data-ttu-id="3ec80-293">OPS 自定义 Markdown 扩展</span><span class="sxs-lookup"><span data-stu-id="3ec80-293">OPS custom Markdown extensions</span></span>

> [!NOTE]
> <span data-ttu-id="3ec80-294">Open Publishing Services(OPS) 可实现 Markdown Markdig 分析程序，它与 GitHub 风格的 Markdown (GFM) 高度兼容。</span><span class="sxs-lookup"><span data-stu-id="3ec80-294">Open Publishing Services (OPS) implements a Markdig Parser for Markdown, which is highly compatible with GitHub Flavored Markdown (GFM).</span></span> <span data-ttu-id="3ec80-295">Markdig 通过 Markdown 扩展添加一些功能。</span><span class="sxs-lookup"><span data-stu-id="3ec80-295">Markdig adds some functionality through Markdown extensions.</span></span> <span data-ttu-id="3ec80-296">就这一点而言，本指南从完整的《OPS 创作指南》中选用了几篇文章，以供参考。</span><span class="sxs-lookup"><span data-stu-id="3ec80-296">As such, selected articles from the full OPS Authoring Guide are included in this guide for reference.</span></span> <span data-ttu-id="3ec80-297">（例如，请参阅目录中的“Markdig 和 Markdown 扩展”以及“代码片段”。）</span><span class="sxs-lookup"><span data-stu-id="3ec80-297">(For example, see "Markdig and Markdown extensions" and "Code snippets" in the table of contents.)</span></span>

<span data-ttu-id="3ec80-298">Doc 文章使用 GFM 完成大多文章的格式设置，如段落、链接、列表和标题。</span><span class="sxs-lookup"><span data-stu-id="3ec80-298">Docs articles use GFM for most article formatting, such as paragraphs, links, lists, and headings.</span></span> <span data-ttu-id="3ec80-299">要想实现更丰富的格式设置功能，文章可以使用 Markdig 功能，例如：</span><span class="sxs-lookup"><span data-stu-id="3ec80-299">For richer formatting, articles can use Markdig features such as:</span></span>

- <span data-ttu-id="3ec80-300">备注块</span><span class="sxs-lookup"><span data-stu-id="3ec80-300">Note blocks</span></span>
- <span data-ttu-id="3ec80-301">包含文件</span><span class="sxs-lookup"><span data-stu-id="3ec80-301">Include files</span></span>
- <span data-ttu-id="3ec80-302">选择器</span><span class="sxs-lookup"><span data-stu-id="3ec80-302">Selectors</span></span>
- <span data-ttu-id="3ec80-303">嵌入视频</span><span class="sxs-lookup"><span data-stu-id="3ec80-303">Embedded videos</span></span>
- <span data-ttu-id="3ec80-304">代码片段/示例</span><span class="sxs-lookup"><span data-stu-id="3ec80-304">Code snippets/samples</span></span>

<span data-ttu-id="3ec80-305">如需完整列表，请参阅目录中的“Markdig 和 Markdown 扩展”以及“代码片段”。</span><span class="sxs-lookup"><span data-stu-id="3ec80-305">For the complete list, refer to "Markdig and Markdown extensions" and "Code snippets" in the table of contents.</span></span>

### <a name="note-blocks"></a><span data-ttu-id="3ec80-306">备注块</span><span class="sxs-lookup"><span data-stu-id="3ec80-306">Note blocks</span></span>

<span data-ttu-id="3ec80-307">可以从 4 种类型的备注块中进行选择来吸引对特定内容的注意：</span><span class="sxs-lookup"><span data-stu-id="3ec80-307">You can choose from four types of note blocks to draw attention to specific content:</span></span>

- <span data-ttu-id="3ec80-308">NOTE</span><span class="sxs-lookup"><span data-stu-id="3ec80-308">NOTE</span></span>
- <span data-ttu-id="3ec80-309">WARNING</span><span class="sxs-lookup"><span data-stu-id="3ec80-309">WARNING</span></span>
- <span data-ttu-id="3ec80-310">TIP</span><span class="sxs-lookup"><span data-stu-id="3ec80-310">TIP</span></span>
- <span data-ttu-id="3ec80-311">IMPORTANT</span><span class="sxs-lookup"><span data-stu-id="3ec80-311">IMPORTANT</span></span>

<span data-ttu-id="3ec80-312">总之，应谨慎使用备注块，因为它们可能会造成干扰。</span><span class="sxs-lookup"><span data-stu-id="3ec80-312">In general, note blocks should be used sparingly because they can be disruptive.</span></span> <span data-ttu-id="3ec80-313">尽管备注块也支持代码块、图像、列表以及链接，但最好尽量保持备注块简单明了。</span><span class="sxs-lookup"><span data-stu-id="3ec80-313">Although they also support code blocks, images, lists, and links, try to keep your note blocks simple and straightforward.</span></span>

<span data-ttu-id="3ec80-314">示例：</span><span class="sxs-lookup"><span data-stu-id="3ec80-314">Examples:</span></span>

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

<span data-ttu-id="3ec80-315">这些呈现结果如下：</span><span class="sxs-lookup"><span data-stu-id="3ec80-315">These render as follows:</span></span>

> [!NOTE]
> <span data-ttu-id="3ec80-316">This is a NOTE</span><span class="sxs-lookup"><span data-stu-id="3ec80-316">This is a NOTE</span></span>

> [!WARNING]
> <span data-ttu-id="3ec80-317">This is a WARNING</span><span class="sxs-lookup"><span data-stu-id="3ec80-317">This is a WARNING</span></span>

> [!TIP]
> <span data-ttu-id="3ec80-318">This is a TIP</span><span class="sxs-lookup"><span data-stu-id="3ec80-318">This is a TIP</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3ec80-319">This is IMPORTANT</span><span class="sxs-lookup"><span data-stu-id="3ec80-319">This is IMPORTANT</span></span>

### <a name="include-files"></a><span data-ttu-id="3ec80-320">包含文件</span><span class="sxs-lookup"><span data-stu-id="3ec80-320">Include files</span></span>

<span data-ttu-id="3ec80-321">如果有需要加入文章文件中的可重用的文本或图像文件，可以通过 Markdig 文件的包含文件功能使用对“包含”文件的引用。</span><span class="sxs-lookup"><span data-stu-id="3ec80-321">When you have reusable text or image files that need to be included in article files, you can use a reference to the "include" file via the Markdig file include feature.</span></span> <span data-ttu-id="3ec80-322">此功能指示 OPS 在创建时将该文件加入文章文件中，使它成为已发布文章的一部分。</span><span class="sxs-lookup"><span data-stu-id="3ec80-322">This feature instructs OPS to include the file in your article file at build time, making it part of your published article.</span></span> <span data-ttu-id="3ec80-323">有 3 种类型的包含引用可帮助你重用内容：</span><span class="sxs-lookup"><span data-stu-id="3ec80-323">Three types of include references are available to help you reuse content:</span></span>

- <span data-ttu-id="3ec80-324">内联：重用内联在其他句子中的常用文本片段。</span><span class="sxs-lookup"><span data-stu-id="3ec80-324">Inline: Reuse a common text snippet inline with within another sentence.</span></span>
- <span data-ttu-id="3ec80-325">块：将整个 Markdown 文件作为一个块重用，嵌套在文章的某一部分中。</span><span class="sxs-lookup"><span data-stu-id="3ec80-325">Block: Reuse an entire Markdown file as a block, nested within a section of an article.</span></span>
- <span data-ttu-id="3ec80-326">图像：此方法可以在 Doc 中实现标准图像加入。</span><span class="sxs-lookup"><span data-stu-id="3ec80-326">Image: This is how standard image inclusion is implemented in Docs.</span></span>

<span data-ttu-id="3ec80-327">“内联”和“块”包含文件是简单的 Markdown (.md) 文件。</span><span class="sxs-lookup"><span data-stu-id="3ec80-327">An inline or block include file is just a simple Markdown (.md) file.</span></span> <span data-ttu-id="3ec80-328">它可以包含任何有效的 Markdown。</span><span class="sxs-lookup"><span data-stu-id="3ec80-328">It can contain any valid Markdown.</span></span> <span data-ttu-id="3ec80-329">所有包含 Markdown 文件都应置于存储库根目录的[常用 `/includes` 子目录](git-github-fundamentals.md#includes-subdirectory) 中。</span><span class="sxs-lookup"><span data-stu-id="3ec80-329">All include Markdown files should be placed in a [common `/includes` subdirectory](git-github-fundamentals.md#includes-subdirectory), in the root of the repository.</span></span> <span data-ttu-id="3ec80-330">发布文章时，加入的文件会无缝集成到其中。</span><span class="sxs-lookup"><span data-stu-id="3ec80-330">When the article is published, the included file is seamlessly integrated into it.</span></span>

<span data-ttu-id="3ec80-331">包含文件的要求和注意事项如下：</span><span class="sxs-lookup"><span data-stu-id="3ec80-331">Here are requirements and considerations for include files:</span></span>

- <span data-ttu-id="3ec80-332">每当需要在多篇文章中显示相同的文本时，均可使用包含功能文件。</span><span class="sxs-lookup"><span data-stu-id="3ec80-332">Use an include file whenever you need the same text to appear in multiple articles.</span></span>
- <span data-ttu-id="3ec80-333">块包含文件适用于大篇幅内容，比如一个或者两个段落、共享过程或者共享章节。</span><span class="sxs-lookup"><span data-stu-id="3ec80-333">Use a block include reference for significant amounts of content--a paragraph or two, a shared procedure, or a shared section.</span></span> <span data-ttu-id="3ec80-334">请勿将它们用于小于一个句子的内容。</span><span class="sxs-lookup"><span data-stu-id="3ec80-334">Do not use them for anything smaller than a sentence.</span></span>
- <span data-ttu-id="3ec80-335">包含文件不会在文章的 GitHub 渲染视图中显示，因为它们依赖于 Markdig 扩展。</span><span class="sxs-lookup"><span data-stu-id="3ec80-335">Include references won't be rendered in the GitHub rendered view of your article, because they rely on Markdig extensions.</span></span> <span data-ttu-id="3ec80-336">它们在发布后才会显示。</span><span class="sxs-lookup"><span data-stu-id="3ec80-336">They'll be rendered only after publication.</span></span>
- <span data-ttu-id="3ec80-337">确保包含文件中的所有文本都是完整的句子或者段落，并且与引用该包含文件的文章的前后文没有关联。</span><span class="sxs-lookup"><span data-stu-id="3ec80-337">Ensure that all the text in an include file is written in complete sentences or phrases that do not depend on preceding text or following text in the article that references the include file.</span></span> <span data-ttu-id="3ec80-338">如果不遵循此指导原则，则会在文章中创建无法转换的字符串，进而破坏本地化体验。</span><span class="sxs-lookup"><span data-stu-id="3ec80-338">Ignoring this guidance creates an untranslatable string in the article that breaks the localized experience.</span></span>
- <span data-ttu-id="3ec80-339">请勿在其他包含文件中嵌入包含引用。</span><span class="sxs-lookup"><span data-stu-id="3ec80-339">Don't embed include references within other include files.</span></span> <span data-ttu-id="3ec80-340">不支持此操作。</span><span class="sxs-lookup"><span data-stu-id="3ec80-340">They are not supported.</span></span>
- <span data-ttu-id="3ec80-341">将媒体文件置于特定于包含文件子目录的媒体文件夹中，例如，`<repo>`/includes/媒体文件夹。</span><span class="sxs-lookup"><span data-stu-id="3ec80-341">Place media files in a media folder that's specific to the include subdirectory--for instance, the `<repo>`/includes/media folder.</span></span> <span data-ttu-id="3ec80-342">媒体目录不应在根目录中包含任何图片。</span><span class="sxs-lookup"><span data-stu-id="3ec80-342">The media directory should not contain any images in its root.</span></span> <span data-ttu-id="3ec80-343">如果包含文件中没有图像，则不需要相应的媒体目录。</span><span class="sxs-lookup"><span data-stu-id="3ec80-343">If the include file does not have images, a corresponding media directory is not required.</span></span>
- <span data-ttu-id="3ec80-344">对于常规文章，请勿在各包含文件之间共享媒体。</span><span class="sxs-lookup"><span data-stu-id="3ec80-344">As with regular articles, don't share media between include files.</span></span> <span data-ttu-id="3ec80-345">对于每个包含文件和文章，请使用具有唯一名称的单独文件。</span><span class="sxs-lookup"><span data-stu-id="3ec80-345">Use a separate file with a unique name for each include file and article.</span></span> <span data-ttu-id="3ec80-346">将媒体文件存储在与包含文件关联的媒体文件夹中。</span><span class="sxs-lookup"><span data-stu-id="3ec80-346">Store the media file in the media folder that's associated with the include file.</span></span>
- <span data-ttu-id="3ec80-347">请勿将包含文件用作文章的唯一内容。</span><span class="sxs-lookup"><span data-stu-id="3ec80-347">Don't use an include file as the only content of an article.</span></span>  <span data-ttu-id="3ec80-348">包含文件主要用作文章其余内容的补充内容。</span><span class="sxs-lookup"><span data-stu-id="3ec80-348">Include files are meant to be supplemental to the content in the rest of the article.</span></span>

<span data-ttu-id="3ec80-349">示例：</span><span class="sxs-lookup"><span data-stu-id="3ec80-349">Example:</span></span>

```markdown
[!INCLUDE[sample include file](../includes/sampleinclude.md)]
```

### <a name="selectors"></a><span data-ttu-id="3ec80-350">选择器</span><span class="sxs-lookup"><span data-stu-id="3ec80-350">Selectors</span></span>

<span data-ttu-id="3ec80-351">当你创作具有多种风格的同一篇技术文章时，请在文章中使用选择器，从而跨技术或平台解决实现上的差异。</span><span class="sxs-lookup"><span data-stu-id="3ec80-351">Use selectors in technical articles when you author multiple flavors of the same article, to  address differences in implementation across technologies or platforms.</span></span> <span data-ttu-id="3ec80-352">通常，这最适用于开发人员的移动平台内容。</span><span class="sxs-lookup"><span data-stu-id="3ec80-352">This is typically most applicable to our mobile platform content for developers.</span></span> <span data-ttu-id="3ec80-353">Markdig 中目前有两种类型的选择器，单选择器和多选择器。</span><span class="sxs-lookup"><span data-stu-id="3ec80-353">There are currently two different types of selectors in Markdig, a single selector and a multi-selector.</span></span>

<span data-ttu-id="3ec80-354">由于选择的每篇文章中都会出现相同的选择器 Markdown，因此建议将文章的选择器放在包含文件中。</span><span class="sxs-lookup"><span data-stu-id="3ec80-354">Because the same selector Markdown goes in each article in the selection, we recommend placing the selector for your article in an include file.</span></span> <span data-ttu-id="3ec80-355">然后，可以在使用相同选择器的所有文章中引用该包含文件。</span><span class="sxs-lookup"><span data-stu-id="3ec80-355">Then you can reference that include file in all your articles that use the same selector.</span></span>

<span data-ttu-id="3ec80-356">下面展示了一个示例选择器：</span><span class="sxs-lookup"><span data-stu-id="3ec80-356">The following shows an example selector:</span></span>

```markdown
> [!div class="op_single_selector"]
- [macOS](../docs/core/tutorials/using-on-macos.md)
- [Windows](../docs/core/tutorials/with-visual-studio.md)
```

<span data-ttu-id="3ec80-357">可在 [Azure 文档](https://docs.microsoft.com/azure/expressroute/expressroute-howto-circuit-classic)中查看有效的选择器示例。</span><span class="sxs-lookup"><span data-stu-id="3ec80-357">You can see an example of selectors in action at the [Azure docs](https://docs.microsoft.com/azure/expressroute/expressroute-howto-circuit-classic).</span></span>

### <a name="code-include-references"></a><span data-ttu-id="3ec80-358">代码包含引用</span><span class="sxs-lookup"><span data-stu-id="3ec80-358">Code include references</span></span>

<span data-ttu-id="3ec80-359">Markdig 支持通过代码片段扩展以一种高级方式将代码加入文章中。</span><span class="sxs-lookup"><span data-stu-id="3ec80-359">Markdig supports advanced inclusion of code in an article, via its code snippet extension.</span></span> <span data-ttu-id="3ec80-360">它提供了一种高级的呈现方式，这种方式基于 GFM 功能（例如编程语言选择和语法着色）以及以下一些出色的功能生成：</span><span class="sxs-lookup"><span data-stu-id="3ec80-360">It provides advanced rendering that builds on GFM features such as programming language selection and syntax coloring, plus nice features such as:</span></span>

- <span data-ttu-id="3ec80-361">通过外部存储库加入集中式代码示例/片段。</span><span class="sxs-lookup"><span data-stu-id="3ec80-361">Inclusion of centralized code samples/snippets from an external repository.</span></span>
- <span data-ttu-id="3ec80-362">选项卡式 UI，可采用不同语言显示多个版本的代码示例。</span><span class="sxs-lookup"><span data-stu-id="3ec80-362">Tabbed UI to show multiple versions of code samples in different languages.</span></span>

## <a name="gotchas-and-troubleshooting"></a><span data-ttu-id="3ec80-363">难题和故障排除</span><span class="sxs-lookup"><span data-stu-id="3ec80-363">Gotchas and troubleshooting</span></span>

### <a name="alt-text"></a><span data-ttu-id="3ec80-364">替换文字</span><span class="sxs-lookup"><span data-stu-id="3ec80-364">Alt text</span></span>

<span data-ttu-id="3ec80-365">无法正确显示带下划线的替换文字。</span><span class="sxs-lookup"><span data-stu-id="3ec80-365">Alt text that contains underscores won't be rendered properly.</span></span> <span data-ttu-id="3ec80-366">例如，与使用以下下划线相比：</span><span class="sxs-lookup"><span data-stu-id="3ec80-366">For example, instead of using this:</span></span>

```markdown
![ADextension_2FA_Configure_Step4](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

<span data-ttu-id="3ec80-367">转义下划线，如下所示：</span><span class="sxs-lookup"><span data-stu-id="3ec80-367">Escape the underscores like this:</span></span>

```markdown
![ADextension\_2FA\_Configure\_Step4](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

### <a name="apostrophes-and-quotation-marks"></a><span data-ttu-id="3ec80-368">撇号和引号</span><span class="sxs-lookup"><span data-stu-id="3ec80-368">Apostrophes and quotation marks</span></span>

<span data-ttu-id="3ec80-369">如果将文本从 Word 复制到 Markdown 编辑器，文本可能包含“弯”撇号或弯引号。</span><span class="sxs-lookup"><span data-stu-id="3ec80-369">If you copy from Word into a Markdown editor, the text might contain "smart" (curly) apostrophes or quotation marks.</span></span> <span data-ttu-id="3ec80-370">需要将这些内容编码或更改为基本撇号或单引号。</span><span class="sxs-lookup"><span data-stu-id="3ec80-370">These need to be encoded or changed to basic apostrophes or quotation marks.</span></span> <span data-ttu-id="3ec80-371">否则，发布文件时，最终将得到：Itâ€™s</span><span class="sxs-lookup"><span data-stu-id="3ec80-371">Otherwise, you end up with things like this when the file is published: Itâ€™s</span></span>

<span data-ttu-id="3ec80-372">下面是关于这些“弯”版本标点符号的编码：</span><span class="sxs-lookup"><span data-stu-id="3ec80-372">Here are the encodings for the "smart" versions of these punctuation marks:</span></span>

- <span data-ttu-id="3ec80-373">左（开）引号：`&#8220;`</span><span class="sxs-lookup"><span data-stu-id="3ec80-373">Left (opening) quotation mark: `&#8220;`</span></span>
- <span data-ttu-id="3ec80-374">右（闭）引号：`&#8221;`</span><span class="sxs-lookup"><span data-stu-id="3ec80-374">Right (closing) quotation mark: `&#8221;`</span></span>
- <span data-ttu-id="3ec80-375">右单（闭）引号/撇号：`&#8217;`</span><span class="sxs-lookup"><span data-stu-id="3ec80-375">Right (closing) single quotation mark or apostrophe: `&#8217;`</span></span>
- <span data-ttu-id="3ec80-376">左单（开）引号（很少使用）：`&#8216;`</span><span class="sxs-lookup"><span data-stu-id="3ec80-376">Left (opening) single quotation mark (rarely used): `&#8216;`</span></span>

### <a name="angle-brackets"></a><span data-ttu-id="3ec80-377">尖括号</span><span class="sxs-lookup"><span data-stu-id="3ec80-377">Angle brackets</span></span>

<span data-ttu-id="3ec80-378">通常使用尖括号来表示占位符。</span><span class="sxs-lookup"><span data-stu-id="3ec80-378">It is common to use angle brackets to denote a placeholder.</span></span> <span data-ttu-id="3ec80-379">在文本（而不是代码）中执行此操作时，必须对尖括号进行编码。</span><span class="sxs-lookup"><span data-stu-id="3ec80-379">When you do this in text (not code), you must encode the angle brackets.</span></span> <span data-ttu-id="3ec80-380">否则，Markdown 会认为它们是一个 HTML 标记。</span><span class="sxs-lookup"><span data-stu-id="3ec80-380">Otherwise, Markdown thinks that they're intended to be an HTML tag.</span></span>

<span data-ttu-id="3ec80-381">例如，将 `<script name>` 编码为 `&lt;script name&gt;`</span><span class="sxs-lookup"><span data-stu-id="3ec80-381">For example, encode `<script name>` as `&lt;script name&gt;`</span></span>

## <a name="markdown-flavor"></a><span data-ttu-id="3ec80-382">Markdown 风格</span><span class="sxs-lookup"><span data-stu-id="3ec80-382">Markdown flavor</span></span>

<span data-ttu-id="3ec80-383">docs.microsoft.com 站点后端使用开放发布服务 (OPS)，支持通过 [Markdig](https://github.com/lunet-io/markdig) 分析引擎分析的 [CommonMark](https://commonmark.org/) 兼容 Markdown。</span><span class="sxs-lookup"><span data-stu-id="3ec80-383">The docs.microsoft.com site backend uses Open Publishing Services (OPS) which supports [CommonMark](https://commonmark.org/) compliant markdown parsed through the [Markdig](https://github.com/lunet-io/markdig) parsing engine.</span></span> <span data-ttu-id="3ec80-384">Markdown 风格大多与 [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/) 兼容，因为大多数 docs 存储在 GitHub 中，并可以在 GitHub 中进行编辑。</span><span class="sxs-lookup"><span data-stu-id="3ec80-384">This markdown flavor is mostly compatible with [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/), as most docs are stored in GitHub and can be edited there.</span></span> <span data-ttu-id="3ec80-385">通过 Markdown 扩展添加一些功能。</span><span class="sxs-lookup"><span data-stu-id="3ec80-385">Additional functionality is added through Markdown extensions.</span></span>

## <a name="see-also"></a><span data-ttu-id="3ec80-386">另请参阅：</span><span class="sxs-lookup"><span data-stu-id="3ec80-386">See also:</span></span>

### <a name="markdown-resources"></a><span data-ttu-id="3ec80-387">Markdown 资源</span><span class="sxs-lookup"><span data-stu-id="3ec80-387">Markdown resources</span></span>

- [<span data-ttu-id="3ec80-388">Markdown 简介</span><span class="sxs-lookup"><span data-stu-id="3ec80-388">Introduction to Markdown</span></span>](https://daringfireball.net/projects/markdown/syntax)
- [<span data-ttu-id="3ec80-389">Docs Markdown 备忘单</span><span class="sxs-lookup"><span data-stu-id="3ec80-389">Docs Markdown cheat sheet</span></span>](./media/documents/markdown-cheatsheet.pdf?raw=true)
- [<span data-ttu-id="3ec80-390">GitHub 的 Markdown 基础知识</span><span class="sxs-lookup"><span data-stu-id="3ec80-390">GitHub's Markdown Basics</span></span>](https://help.github.com/articles/markdown-basics/)
- [<span data-ttu-id="3ec80-391">Markdown 指南</span><span class="sxs-lookup"><span data-stu-id="3ec80-391">The Markdown Guide</span></span>](https://www.markdownguide.org/)
