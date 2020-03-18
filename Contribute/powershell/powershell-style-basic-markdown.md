---
title: 适用于 PowerShell 文章的模板和速查表
description: 本文包含一个便捷的模板，可用于针对 PowerShell 文档创建新文章
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
author: sdwheeler
ms.author: sewhee
ms.date: 10/09/2019
ms.openlocfilehash: 073a44240b1aa4baa9e655dab069097d21cdd66d
ms.sourcegitcommit: 804a99b89785e5c8f056a9da3f0fbde9f0a56a51
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/05/2020
ms.locfileid: "78331920"
---
# <a name="markdown-style-guide-for-powershell-docs"></a><span data-ttu-id="8fdad-103">PowerShell-Docs 的 Markdown 风格指南</span><span class="sxs-lookup"><span data-stu-id="8fdad-103">Markdown style guide for PowerShell-Docs</span></span>

<span data-ttu-id="8fdad-104">本文提供一些特定于 PowerShell-Docs 内容的风格指南。</span><span class="sxs-lookup"><span data-stu-id="8fdad-104">This article provides some style guidance specific to the PowerShell-Docs content.</span></span>

<span data-ttu-id="8fdad-105">有关其他写作风格指南，请参阅 [Microsoft 风格指南](https://docs.microsoft.com/style-guide/welcome/)。</span><span class="sxs-lookup"><span data-stu-id="8fdad-105">For other writing style guidance, see the [Microsoft Style Guide](https://docs.microsoft.com/style-guide/welcome/).</span></span>

## <a name="metadata"></a><span data-ttu-id="8fdad-106">元数据</span><span class="sxs-lookup"><span data-stu-id="8fdad-106">Metadata</span></span>

<span data-ttu-id="8fdad-107">此模板包含 Markdown 语法的示例，以及有关设置元数据的指南。</span><span class="sxs-lookup"><span data-stu-id="8fdad-107">This template contains examples of Markdown syntax, as well as guidance on setting the metadata.</span></span>
<span data-ttu-id="8fdad-108">创建 Markdown 文件时，应将包括的模板复制到新文件，按如下所示填充元数据，并将上面的 H1 标题设为文章的标题。</span><span class="sxs-lookup"><span data-stu-id="8fdad-108">When creating a Markdown file, you should copy the included template to a new file, fill out the metadata as specified below, and set the H1 heading above to the title of the article.</span></span>

<span data-ttu-id="8fdad-109">所需的元数据块位于以下示例元数据块中：</span><span class="sxs-lookup"><span data-stu-id="8fdad-109">The required metadata block is in the following sample metadata block:</span></span>

```md
---
author: [GITHUB USERNAME]
description: [usually a summary of your first paragraph. It gets displayed in search results, and can help drive the correct traffic if well written.]
ms.date: [CREATION/UPDATE DATE - mm/dd/yyyy]
title: [ARTICLE TITLE]
---
# The H1 should not be the same as the title, but should describe the article contents
```

- <span data-ttu-id="8fdad-110">冒号 (:) 和元数据元素值之间必须有空格  。</span><span class="sxs-lookup"><span data-stu-id="8fdad-110">You **must** have a space between the colon (:) and the value for a metadata element.</span></span>
- <span data-ttu-id="8fdad-111">值（例如，标题）中的冒号可中断元数据分析器。</span><span class="sxs-lookup"><span data-stu-id="8fdad-111">Colons in a value (for example, a title) break the metadata parser.</span></span> <span data-ttu-id="8fdad-112">在此情况下，使用双引号将标题括起来（例如，`title: "Writing .NET Core console apps: An advanced step-by-step guide"`）。</span><span class="sxs-lookup"><span data-stu-id="8fdad-112">In this case, surround the title with double quotes (for example, `title: "Writing .NET Core console apps: An advanced step-by-step guide"`).</span></span>
- <span data-ttu-id="8fdad-113">**作者**：“作者”字段应包含作者的 GitHub 用户名  。</span><span class="sxs-lookup"><span data-stu-id="8fdad-113">**author**: The author field should contain the **GitHub username** of the author.</span></span>
- <span data-ttu-id="8fdad-114">**说明**：概括文章的内容。</span><span class="sxs-lookup"><span data-stu-id="8fdad-114">**description**: Summarizes the content of the article.</span></span> <span data-ttu-id="8fdad-115">它通常在搜索结果页中显示，并且不用于搜索排名。</span><span class="sxs-lookup"><span data-stu-id="8fdad-115">It's usually shown in the search results page, but it isn't used for search ranking.</span></span> <span data-ttu-id="8fdad-116">它的长度应为 115-145 个字符（含空格）。</span><span class="sxs-lookup"><span data-stu-id="8fdad-116">Its length should be 115-145 characters including spaces.</span></span>
- <span data-ttu-id="8fdad-117">**ms.date**：上一次重要更新的日期。</span><span class="sxs-lookup"><span data-stu-id="8fdad-117">**ms.date**: The date of the last significant update.</span></span> <span data-ttu-id="8fdad-118">如果已评审和更新整篇文章，请在现有文章中更新此内容。</span><span class="sxs-lookup"><span data-stu-id="8fdad-118">Update this on existing articles if you reviewed and updated the entire article.</span></span> <span data-ttu-id="8fdad-119">不保证更新拼写错误或类似的小修复。</span><span class="sxs-lookup"><span data-stu-id="8fdad-119">Small fixes, such as typos or similar don't warrant an update.</span></span>
- <span data-ttu-id="8fdad-120">**标题**：在搜索引擎结果中显示。</span><span class="sxs-lookup"><span data-stu-id="8fdad-120">**title**: Appears in search engine results.</span></span> <span data-ttu-id="8fdad-121">该标题不应与 H1 标题中的标题相同，并且所含字符不应超过 60 个。</span><span class="sxs-lookup"><span data-stu-id="8fdad-121">The title shouldn't be identical to the title in your H1 heading, and it should contain 60 characters or fewer.</span></span>

<span data-ttu-id="8fdad-122">其他元数据附加于每篇文章，但我们通常在文件夹级别应用大多数元数据值，如 docfx.json 中所示  。</span><span class="sxs-lookup"><span data-stu-id="8fdad-122">Other metadata is attached to each article, but we typically apply most metadata values at the folder level, specified in **docfx.json**.</span></span>

## <a name="product-terminology"></a><span data-ttu-id="8fdad-123">产品术语</span><span class="sxs-lookup"><span data-stu-id="8fdad-123">Product Terminology</span></span>

<span data-ttu-id="8fdad-124">PowerShell 有多个变体。</span><span class="sxs-lookup"><span data-stu-id="8fdad-124">There are several variants of PowerShell.</span></span> <span data-ttu-id="8fdad-125">此表定义用于讨论 PowerShell 的一些不同术语。</span><span class="sxs-lookup"><span data-stu-id="8fdad-125">This table defines some of the different terms used to discuss PowerShell.</span></span>

- <span data-ttu-id="8fdad-126">PowerShell - 这是默认值  。</span><span class="sxs-lookup"><span data-stu-id="8fdad-126">**PowerShell** - This is the default.</span></span> <span data-ttu-id="8fdad-127">PowerShell 是我们提供的产品。</span><span class="sxs-lookup"><span data-stu-id="8fdad-127">PowerShell is the product we ship.</span></span> <span data-ttu-id="8fdad-128">术语 PowerShell 可用于描述任何版本的产品。</span><span class="sxs-lookup"><span data-stu-id="8fdad-128">The term PowerShell can be used to describe any edition of the product.</span></span>
- <span data-ttu-id="8fdad-129">PowerShell Core - 基于 .NET Core 公共语言运行时 (CoreCLR) 构建的 PowerShell，适用于任何受支持的平台  。</span><span class="sxs-lookup"><span data-stu-id="8fdad-129">**PowerShell Core** - PowerShell built on .NET Core Common Language Runtime (CoreCLR) for any of the supported platforms.</span></span>
- <span data-ttu-id="8fdad-130">Windows PowerShell - 基于 .NET Framework 公共语言运行时 (CLR) 构建的 PowerShell  。</span><span class="sxs-lookup"><span data-stu-id="8fdad-130">**Windows PowerShell** - PowerShell built on .NET Framework Common Language Runtime (CLR).</span></span> <span data-ttu-id="8fdad-131">Windows PowerShell 仅在 Windows 上提供，需要完整的 .Net Framework CLR。</span><span class="sxs-lookup"><span data-stu-id="8fdad-131">Windows PowerShell ships only on Windows and requires the full .Net Framework CLR.</span></span>

<span data-ttu-id="8fdad-132">通常，可将文档中对“Windows PowerShell”的引用更改为“PowerShell”。</span><span class="sxs-lookup"><span data-stu-id="8fdad-132">In general, references to "Windows PowerShell" in documentation can be changed to "PowerShell".</span></span>
<span data-ttu-id="8fdad-133">讨论特定于 Windows 的技术时，不应更改“Windows PowerShell”  。</span><span class="sxs-lookup"><span data-stu-id="8fdad-133">"Windows PowerShell" should **not** be changed when Windows-specific technology is being discussed.</span></span>

## <a name="basic-markdown-gfm-and-special-characters"></a><span data-ttu-id="8fdad-134">基本 Markdown、GFM 和特殊字符</span><span class="sxs-lookup"><span data-stu-id="8fdad-134">Basic Markdown, GFM, and special characters</span></span>

<span data-ttu-id="8fdad-135">可在 [Markdown 引用](../markdown-reference.md)一文中了解 Markdown、GitHub Flavored Markdown (GFM) 和 OPS 特定扩展的基础知识。</span><span class="sxs-lookup"><span data-stu-id="8fdad-135">You can learn the basics of Markdown, GitHub Flavored Markdown (GFM), and OPS specific extensions in the [Markdown reference](../markdown-reference.md) article.</span></span>

<span data-ttu-id="8fdad-136">Markdown 使用特殊字符（例如，\*、\` 和 \#）进行格式设置。</span><span class="sxs-lookup"><span data-stu-id="8fdad-136">Markdown uses special characters such as \*, \`, and \# for formatting.</span></span> <span data-ttu-id="8fdad-137">如果要在内容中包括其中一个字符，必须执行以下两项操作之一：</span><span class="sxs-lookup"><span data-stu-id="8fdad-137">If you wish to include one of these characters in your content, you must do one of two things:</span></span>

- <span data-ttu-id="8fdad-138">在特殊字符前面放一个反斜杠，进行“转义”（例如 `\*` 表示 \*）。</span><span class="sxs-lookup"><span data-stu-id="8fdad-138">Put a backslash before the special character to "escape" it (for example, `\*` for a \*)</span></span>
- <span data-ttu-id="8fdad-139">对字符使用 [HTML 实体代码](http://www.ascii.cl/htmlcodes.htm)（例如，`&#42;` 表示 &#42;）。</span><span class="sxs-lookup"><span data-stu-id="8fdad-139">Use the [HTML entity code](http://www.ascii.cl/htmlcodes.htm) for the character (for example, `&#42;` for a &#42;).</span></span>
- <span data-ttu-id="8fdad-140">Markdown 文件应使用纯 ASCII 文本或 UTF-8 编码。</span><span class="sxs-lookup"><span data-stu-id="8fdad-140">Markdown files should use plain ASCII text or UTF-8 encoding.</span></span> <span data-ttu-id="8fdad-141">但是，应避免使用多字节 UTF-8 字符。</span><span class="sxs-lookup"><span data-stu-id="8fdad-141">However, avoid using multi-byte UTF-8 characters.</span></span> <span data-ttu-id="8fdad-142">而应使用 HTML 实体。</span><span class="sxs-lookup"><span data-stu-id="8fdad-142">Instead use an HTML entity.</span></span> <span data-ttu-id="8fdad-143">例如，版权符号应使用 `&copy;`。</span><span class="sxs-lookup"><span data-stu-id="8fdad-143">For example, for the copyright symbols use `&copy;`.</span></span>
  <span data-ttu-id="8fdad-144">其呈现为：“&copy;”。</span><span class="sxs-lookup"><span data-stu-id="8fdad-144">It is rendered as: "&copy;".</span></span>

## <a name="hyperlinks"></a><span data-ttu-id="8fdad-145">超链接</span><span class="sxs-lookup"><span data-stu-id="8fdad-145">Hyperlinks</span></span>

- <span data-ttu-id="8fdad-146">避免使用裸 URL。</span><span class="sxs-lookup"><span data-stu-id="8fdad-146">Avoid using bare URLs.</span></span> <span data-ttu-id="8fdad-147">链接应使用 Markdown 语法 `[friendlyname](url-or-path)`</span><span class="sxs-lookup"><span data-stu-id="8fdad-147">Links should use Markdown syntax `[friendlyname](url-or-path)`</span></span>
- <span data-ttu-id="8fdad-148">链接必须具有易记名称，通常是链接主题的标题</span><span class="sxs-lookup"><span data-stu-id="8fdad-148">Links must have a friendly name, usually the title of the linked topic</span></span>
- <span data-ttu-id="8fdad-149">底部“相关链接”部分中的所有项都应采用超链接形式。</span><span class="sxs-lookup"><span data-stu-id="8fdad-149">All items in the "related links" section at the bottom should be hyperlinked.</span></span>
- <span data-ttu-id="8fdad-150">链接到 docs.microsoft.com 上托管的其他内容时，请使用相对链接  。</span><span class="sxs-lookup"><span data-stu-id="8fdad-150">Use relative links when linking to other content that is hosted on **docs.microsoft.com**.</span></span>
- <span data-ttu-id="8fdad-151">请勿在超链接的括号内使用反引号、粗体或其他标记。</span><span class="sxs-lookup"><span data-stu-id="8fdad-151">Do not use backticks, bold, or other markup inside the brackets of a hyperlink.</span></span>

<span data-ttu-id="8fdad-152">有关链接的详细信息，请参阅[在文档中使用链接](../how-to-write-links.md)。</span><span class="sxs-lookup"><span data-stu-id="8fdad-152">For more detailed information about linking, see [Using links in documentation](../how-to-write-links.md).</span></span>

## <a name="filenames"></a><span data-ttu-id="8fdad-153">文件名</span><span class="sxs-lookup"><span data-stu-id="8fdad-153">Filenames</span></span>

<span data-ttu-id="8fdad-154">文件名采用以下规则：</span><span class="sxs-lookup"><span data-stu-id="8fdad-154">Filenames use the following rules:</span></span>

- <span data-ttu-id="8fdad-155">只能包含字母、数字和连字符。</span><span class="sxs-lookup"><span data-stu-id="8fdad-155">Contain only letters, numbers, and hyphens.</span></span>
- <span data-ttu-id="8fdad-156">不使用空格或标点符号字符。</span><span class="sxs-lookup"><span data-stu-id="8fdad-156">No spaces or punctuation characters.</span></span> <span data-ttu-id="8fdad-157">使用连字符分隔文件名中的单词和数字。</span><span class="sxs-lookup"><span data-stu-id="8fdad-157">Use the hyphens to separate words and numbers in the file name.</span></span>
- <span data-ttu-id="8fdad-158">使用特定的行为动词，如开发、购买、构建和故障排除。</span><span class="sxs-lookup"><span data-stu-id="8fdad-158">Use action verbs that are specific, such as develop, buy, build, troubleshoot.</span></span> <span data-ttu-id="8fdad-159">不使用后缀是 ing 的单词。</span><span class="sxs-lookup"><span data-stu-id="8fdad-159">No -ing words.</span></span>
- <span data-ttu-id="8fdad-160">不使用小词汇 - 不包含 a、and、the、in 或 or 等。</span><span class="sxs-lookup"><span data-stu-id="8fdad-160">No small words - don't include a, and, the, in, or, etc.</span></span>
- <span data-ttu-id="8fdad-161">必须在 Markdown 中且使用 .md 文件扩展名。</span><span class="sxs-lookup"><span data-stu-id="8fdad-161">Must be in Markdown and use the .md file extension.</span></span>
- <span data-ttu-id="8fdad-162">使文件名尽量简短，且适当合理。</span><span class="sxs-lookup"><span data-stu-id="8fdad-162">Keep file names reasonably short.</span></span> <span data-ttu-id="8fdad-163">此名称会包含在文章的 URL 中。</span><span class="sxs-lookup"><span data-stu-id="8fdad-163">They are part of the URL for your articles.</span></span>

## <a name="blank-lines-spaces-and-tabs"></a><span data-ttu-id="8fdad-164">空行、空格和制表符</span><span class="sxs-lookup"><span data-stu-id="8fdad-164">Blank lines, spaces, and tabs</span></span>

<span data-ttu-id="8fdad-165">删除重复的空行。</span><span class="sxs-lookup"><span data-stu-id="8fdad-165">Remove duplicate blank lines.</span></span> <span data-ttu-id="8fdad-166">在 HTML 中，多个空行呈现为单个空行，因此没有必要使用多个空行。</span><span class="sxs-lookup"><span data-stu-id="8fdad-166">Multiple blank lines render as a single blank line in HTML so there is not purpose for multiple blank lines.</span></span>

<span data-ttu-id="8fdad-167">在 Markdown 中，空行还表示代码块结束。</span><span class="sxs-lookup"><span data-stu-id="8fdad-167">Blank lines also signal the end of a block in Markdown.</span></span> <span data-ttu-id="8fdad-168">不同类型的 Markdown 代码块之间应存在空白（例如，段落与列表或标头之间）。</span><span class="sxs-lookup"><span data-stu-id="8fdad-168">There should be a single blank between Markdown blocks of different types (for example, between a paragraph and a list or header).</span></span>

> [!NOTE]
> <span data-ttu-id="8fdad-169">间距在 Markdown 中非常重要。</span><span class="sxs-lookup"><span data-stu-id="8fdad-169">Spacing is significant in Markdown.</span></span> <span data-ttu-id="8fdad-170">应始终使用空格，而非硬制表符。</span><span class="sxs-lookup"><span data-stu-id="8fdad-170">Always uses spaces instead of hard tabs.</span></span> <span data-ttu-id="8fdad-171">应删除行末尾多余的空格。</span><span class="sxs-lookup"><span data-stu-id="8fdad-171">Remove extra spaces at the end of lines.</span></span>

## <a name="titles-and-headings"></a><span data-ttu-id="8fdad-172">各级标题</span><span class="sxs-lookup"><span data-stu-id="8fdad-172">Titles and headings</span></span>

<span data-ttu-id="8fdad-173">应只使用 [ATX 标题][atx]（# 样式，而非 `=` 或 `-` 样式标头）。</span><span class="sxs-lookup"><span data-stu-id="8fdad-173">Only use [ATX headings][atx] (# style, as opposed to `=` or `-` style headers).</span></span>

- <span data-ttu-id="8fdad-174">句子大小写的使用 - 仅正确的名词和标题或标头的第一个字母应采用大写形式</span><span class="sxs-lookup"><span data-stu-id="8fdad-174">Use sentence case - only proper nouns and the first letter of a title or header should be capitalized</span></span>
- <span data-ttu-id="8fdad-175">在 `#` 与标题的第一个字母之间必须有一个空格</span><span class="sxs-lookup"><span data-stu-id="8fdad-175">There must be a single space between the `#` and the first letter of the heading</span></span>
- <span data-ttu-id="8fdad-176">标题应由一个空行包围</span><span class="sxs-lookup"><span data-stu-id="8fdad-176">Headings should be surrounded by a single blank line</span></span>
- <span data-ttu-id="8fdad-177">每个文档只有一个 H1</span><span class="sxs-lookup"><span data-stu-id="8fdad-177">Only one H1 per document</span></span>
- <span data-ttu-id="8fdad-178">标头级别应逐个增加，不得跳过级别</span><span class="sxs-lookup"><span data-stu-id="8fdad-178">Header levels should increment by one - do not skip levels</span></span>
- <span data-ttu-id="8fdad-179">请勿在标头中使用反引号、粗体或其他标记</span><span class="sxs-lookup"><span data-stu-id="8fdad-179">Do not use backticks, bold, or other markup in headers</span></span>

> [!CAUTION]
> <span data-ttu-id="8fdad-180">[PlatyPS][platyPS] 为 cmdlet 引用强制执行的架构需要特定的 H2 和 H3 标头。</span><span class="sxs-lookup"><span data-stu-id="8fdad-180">The schema enforced by [PlatyPS][platyPS] for cmdlet reference requires specific H2 and H3 headers.</span></span> <span data-ttu-id="8fdad-181">添加或删除标头可能会中断生成。</span><span class="sxs-lookup"><span data-stu-id="8fdad-181">Adding or removing headers can break the build.</span></span> <span data-ttu-id="8fdad-182">有关详细信息，请参阅 [cmdlet 引用风格指南](powershell-style-reference.md)。</span><span class="sxs-lookup"><span data-stu-id="8fdad-182">For more information, see the [cmdlet reference style guide](powershell-style-reference.md).</span></span>

## <a name="limit-line-length-to-100-characters"></a><span data-ttu-id="8fdad-183">将行长度限制为 100 个字符</span><span class="sxs-lookup"><span data-stu-id="8fdad-183">Limit line length to 100 characters</span></span>

<span data-ttu-id="8fdad-184">这简化了差异和历史记录的命令行输出。</span><span class="sxs-lookup"><span data-stu-id="8fdad-184">This simplifies the command-line output of diffs and history.</span></span>

<span data-ttu-id="8fdad-185">此规则并不能针对 PowerShell-Docs 中的大部分现有内容强制执行，但随着时间的推移，我们正朝着这个方向努力。</span><span class="sxs-lookup"><span data-stu-id="8fdad-185">This rule was not in force for much of the existing content in PowerShell-Docs, but we are working towards it over time.</span></span> <span data-ttu-id="8fdad-186">如需帮助，请随时联系。借助 Visual Studio Code (VSCode) 中的[重排扩展][reflow]，可轻松地将段落的格式重新设置为此限制。</span><span class="sxs-lookup"><span data-stu-id="8fdad-186">Feel free to help out. The [reflow extension][reflow] in Visual Studio Code (VSCode) makes it easy to reformat paragraphs to this limit.</span></span>

## <a name="lists"></a><span data-ttu-id="8fdad-187">列表</span><span class="sxs-lookup"><span data-stu-id="8fdad-187">Lists</span></span>

<span data-ttu-id="8fdad-188">如果列表包含多个句子或段落，请考虑使用子标头，而非列表。</span><span class="sxs-lookup"><span data-stu-id="8fdad-188">If your list contains multiple sentences or paragraphs, consider using a sub-level header rather than a list.</span></span>

<span data-ttu-id="8fdad-189">列表应由一个空行包围。</span><span class="sxs-lookup"><span data-stu-id="8fdad-189">List should be surrounded by a single blank line.</span></span>

### <a name="unordered-lists"></a><span data-ttu-id="8fdad-190">未排序列表</span><span class="sxs-lookup"><span data-stu-id="8fdad-190">Unordered lists</span></span>

<span data-ttu-id="8fdad-191">请勿以句点结束列表项，除非包含多个句子。</span><span class="sxs-lookup"><span data-stu-id="8fdad-191">Do not end list items with a period unless they contain multiple sentences.</span></span> <span data-ttu-id="8fdad-192">对于列表项项目符号，使用连字符 (`-`)。</span><span class="sxs-lookup"><span data-stu-id="8fdad-192">Use the hyphen character (`-`) for list item bullets.</span></span> <span data-ttu-id="8fdad-193">这样可避免与使用星号 [`*`] 的粗体或斜体标记混淆。</span><span class="sxs-lookup"><span data-stu-id="8fdad-193">This avoids confusion with bold or italic markup that uses the asterisk [`*`].</span></span> <span data-ttu-id="8fdad-194">要在项目符号项下包含段落或其他元素，请插入换行符并缩进，使其与项目符号后的第一个字符对齐。</span><span class="sxs-lookup"><span data-stu-id="8fdad-194">To include a paragraph or other elements under a bullet item, insert a line break and align indentation with the first character after the bullet.</span></span>

<span data-ttu-id="8fdad-195">例如：</span><span class="sxs-lookup"><span data-stu-id="8fdad-195">For example:</span></span>

```markdown
This is a list that contain sub-elements under a bullet item.

- First bullet item

  Sentence explaining the first bullet.

  - Sub-bullet item

    Sentence explaining the sub-bullet.

- Second bullet item
- Third bullet item
```

<span data-ttu-id="8fdad-196">这是一个项目符号项下包含子元素的列表。</span><span class="sxs-lookup"><span data-stu-id="8fdad-196">This is a list that contains sub-elements under a bullet item.</span></span>

- <span data-ttu-id="8fdad-197">第一个项目符号项</span><span class="sxs-lookup"><span data-stu-id="8fdad-197">First bullet item</span></span>

  <span data-ttu-id="8fdad-198">用于解释第一个项目符号的句子。</span><span class="sxs-lookup"><span data-stu-id="8fdad-198">Sentence explaining the first bullet.</span></span>

  - <span data-ttu-id="8fdad-199">子项目符号项</span><span class="sxs-lookup"><span data-stu-id="8fdad-199">Sub-bullet item</span></span>

    <span data-ttu-id="8fdad-200">用于解释子项目符号的句子。</span><span class="sxs-lookup"><span data-stu-id="8fdad-200">Sentence explaining the sub-bullet.</span></span>

- <span data-ttu-id="8fdad-201">第二个项目符号项</span><span class="sxs-lookup"><span data-stu-id="8fdad-201">Second bullet item</span></span>
- <span data-ttu-id="8fdad-202">第三个项目符号项</span><span class="sxs-lookup"><span data-stu-id="8fdad-202">Third bullet item</span></span>

### <a name="ordered-lists"></a><span data-ttu-id="8fdad-203">已排序列表</span><span class="sxs-lookup"><span data-stu-id="8fdad-203">Ordered lists</span></span>

<span data-ttu-id="8fdad-204">要在编号项下包含段落或其他元素，请进行缩进，使其与项目编号后的第一个字符对齐。</span><span class="sxs-lookup"><span data-stu-id="8fdad-204">To include a paragraph or other elements under a numbered item, align indentation with the first character after the item number.</span></span>

```markdown
1. For the first element, insert a single space after the 1. Long sentences should be
   wrapped to the next line and must line up with the first character after the numbered
   list marker.

   To include a second element (like this one), insert a line break after the first
   and align indentations. The indentation of the second element must line up with
   the first character after the numbered list marker. For single digit items, like
   this one, you indent to column 4. For double digits items, for example item number
   10, you indent to column 5.

1. The next numbered item starts here.
```

<span data-ttu-id="8fdad-205">获取此输出：</span><span class="sxs-lookup"><span data-stu-id="8fdad-205">to get this output:</span></span>

> 1. <span data-ttu-id="8fdad-206">对于第一个元素，在 1 之后插入一个空格。</span><span class="sxs-lookup"><span data-stu-id="8fdad-206">For the first element, insert a single space after the 1.</span></span> <span data-ttu-id="8fdad-207">长句应换到下一行，并且必须与编号列表标记后面的第一个字符对齐。</span><span class="sxs-lookup"><span data-stu-id="8fdad-207">Long sentences should be wrapped to the next line and must line up with the first character after the numbered list marker.</span></span>
>
>    <span data-ttu-id="8fdad-208">要包含第二个元素（如下所示），请在第一个元素后面插入换行符，并缩进以使之对齐。</span><span class="sxs-lookup"><span data-stu-id="8fdad-208">To include a second element (like this one), insert a line break after the first and align indentations.</span></span> <span data-ttu-id="8fdad-209">第二个元素缩进后，必须与编号列表标记后面的第一个字符对齐。</span><span class="sxs-lookup"><span data-stu-id="8fdad-209">The indentation of the second element must line up with the first character after the numbered list marker.</span></span> <span data-ttu-id="8fdad-210">对于一位数的项（如下所示），缩进到第 4 列。</span><span class="sxs-lookup"><span data-stu-id="8fdad-210">For single digit items, like this one, you indent to column 4.</span></span> <span data-ttu-id="8fdad-211">对于两位数的项，例如项编号 10，缩进到第 5 列。</span><span class="sxs-lookup"><span data-stu-id="8fdad-211">For double digits items, for example item number 10, you indent to column 5.</span></span>
>
> 1. <span data-ttu-id="8fdad-212">下一个编号项从此处开始。</span><span class="sxs-lookup"><span data-stu-id="8fdad-212">The next numbered item starts here.</span></span>

<span data-ttu-id="8fdad-213">以编号形式列出的所有项都应使用数字 `1.`，而不是逐项递增。</span><span class="sxs-lookup"><span data-stu-id="8fdad-213">All items in a numbered listed should use the number `1.` instead of incrementing for each item.</span></span>
<span data-ttu-id="8fdad-214">Markdown 呈现会自动递增该值。</span><span class="sxs-lookup"><span data-stu-id="8fdad-214">Markdown rendering increments the value automatically.</span></span> <span data-ttu-id="8fdad-215">这样可以更轻松地对项进行重新排序，并标准化从属内容的缩进。</span><span class="sxs-lookup"><span data-stu-id="8fdad-215">This makes reordering items easier and standardizes the indentation of subordinate content.</span></span>

## <a name="formatting-command-syntax-elements"></a><span data-ttu-id="8fdad-216">设置命令语法元素的格式</span><span class="sxs-lookup"><span data-stu-id="8fdad-216">Formatting command syntax elements</span></span>

- <span data-ttu-id="8fdad-217">PowerShell cmdlet 名称采用[帕斯卡拼写法][pascal-case]。</span><span class="sxs-lookup"><span data-stu-id="8fdad-217">PowerShell cmdlet names are [Pascal Cased][pascal-case].</span></span> <span data-ttu-id="8fdad-218">谓词通过连字符与名词分隔。</span><span class="sxs-lookup"><span data-stu-id="8fdad-218">Verbs are separated from nouns by a hyphen.</span></span> <span data-ttu-id="8fdad-219">对于 cmdlet 和参数，始终使用帕斯卡拼写法下的全名。</span><span class="sxs-lookup"><span data-stu-id="8fdad-219">Always use the full Pascal Case name for cmdlets and parameters.</span></span> <span data-ttu-id="8fdad-220">应避免使用别名，除非专门讨论别名。</span><span class="sxs-lookup"><span data-stu-id="8fdad-220">Avoid using aliases unless you are specifically talking about an alias.</span></span>

- <span data-ttu-id="8fdad-221">在段落中，语言关键字、cmdlet 名称和变量引用应由反引号 (`` ` ``) 字符引起来。</span><span class="sxs-lookup"><span data-stu-id="8fdad-221">Within a paragraph, language keywords, cmdlet names, and variable references should be wrapped in backtick (`` ` ``) characters.</span></span> <span data-ttu-id="8fdad-222">属性名、参数名和类名应采用粗体  。</span><span class="sxs-lookup"><span data-stu-id="8fdad-222">Property, parameter, and class names should be **bold**.</span></span>

  <span data-ttu-id="8fdad-223">例如：</span><span class="sxs-lookup"><span data-stu-id="8fdad-223">For example:</span></span>

  ~~~markdown
  The following code assigns the output of `Get-ChildItem` to the `$files` variable.

  ```powershell
  $files = Get-ChildItem C:\Windows
  ```
  ~~~

- <span data-ttu-id="8fdad-224">按名称引用参数时，该名称应采用粗体  。</span><span class="sxs-lookup"><span data-stu-id="8fdad-224">When referring to a parameter by name, the name should be **bold**.</span></span> <span data-ttu-id="8fdad-225">演示使用带有连字符前缀的参数时，应使用反引号将参数引起来。</span><span class="sxs-lookup"><span data-stu-id="8fdad-225">When illustrating the use of a parameter with the hyphen prefix, the parameter should be wrapped in backticks.</span></span> <span data-ttu-id="8fdad-226">例如：</span><span class="sxs-lookup"><span data-stu-id="8fdad-226">For example:</span></span>

  ```markdown
  The parameter's name is **Name**, but it is typed as `-Name` when used on the command
  line as a parameter.
  ```

- <span data-ttu-id="8fdad-227">引用 EXE、脚本等外部命令时，命令名称应采用粗体，全部小写（如果位于句子开头，则为大写），并包含相应的文件扩展名。</span><span class="sxs-lookup"><span data-stu-id="8fdad-227">When referring to external commands (EXEs, scripts, etc.), the command name should be bold, all lowercase (or capitalized if at the beginning of a sentence), and include the appropriate file extension.</span></span> <span data-ttu-id="8fdad-228">例如：</span><span class="sxs-lookup"><span data-stu-id="8fdad-228">For example:</span></span>

  ```markdown
  For example, on Windows systems, you can use the `net start` and `net stop` commands
  to start and stop a service. **Sc.exe** is another service control tool for Windows.
  That name does not fit into the naming pattern for the **net.exe** service commands.
  ```

- <span data-ttu-id="8fdad-229">演示外部命令的示例用法时，示例应由反引号引起来。</span><span class="sxs-lookup"><span data-stu-id="8fdad-229">When showing example usage of an external command, the example should be wrapped in backticks.</span></span>
  <span data-ttu-id="8fdad-230">如果与别名存在名称冲突，则必须在命令示例中包含文件扩展名。</span><span class="sxs-lookup"><span data-stu-id="8fdad-230">When there is a name collision with an alias you must include the file extension in the command example.</span></span> <span data-ttu-id="8fdad-231">例如：</span><span class="sxs-lookup"><span data-stu-id="8fdad-231">For example:</span></span>

  ```markdown
  To start the spooler service on a remote computer named DC01, you type `sc.exe \\DC01 start spooler`.
  ```

- <span data-ttu-id="8fdad-232">编写概念性文章（而非引用内容）时，cmdlet 名称的第一个实例应超链接到 cmdlet 文档中。</span><span class="sxs-lookup"><span data-stu-id="8fdad-232">When writing a conceptual article (as opposed to reference content), the first instance of a cmdlet name should be hyperlinked to the cmdlet documentation.</span></span> <span data-ttu-id="8fdad-233">请勿在超链接的括号内使用反引号、粗体或其他标记。</span><span class="sxs-lookup"><span data-stu-id="8fdad-233">Do not use backticks, bold, or other markup inside the brackets of a hyperlink.</span></span>

  <span data-ttu-id="8fdad-234">例如：</span><span class="sxs-lookup"><span data-stu-id="8fdad-234">For example:</span></span>

  ```markdown
  This [Write-Host](/powershell/module/Microsoft.PowerShell.Utility/Write-Host) cmdlet
  uses the **Object** parameter to ...
  ```

  <span data-ttu-id="8fdad-235">有关详细信息，请参阅风格指南的[超链接](#hyperlinks)部分。</span><span class="sxs-lookup"><span data-stu-id="8fdad-235">For more information, see [Hyperlinks](#hyperlinks) section of the Style Guide.</span></span>

## <a name="images"></a><span data-ttu-id="8fdad-236">图像</span><span class="sxs-lookup"><span data-stu-id="8fdad-236">Images</span></span>

<span data-ttu-id="8fdad-237">用于包含图像的语法是：</span><span class="sxs-lookup"><span data-stu-id="8fdad-237">The syntax to include an image is:</span></span>

```Syntax
![[alt text]](<folderPath>)
```

<span data-ttu-id="8fdad-238">示例：</span><span class="sxs-lookup"><span data-stu-id="8fdad-238">Example:</span></span>

```markdown
![Introduction](./media/overview/Introduction.png)
```

<span data-ttu-id="8fdad-239">其中 `alt text` 是图像的简短说明，`<folder path>` 是图像的相对路径。</span><span class="sxs-lookup"><span data-stu-id="8fdad-239">Where `alt text` is a brief description of the image and `<folder path>` is a relative path to the image.</span></span> <span data-ttu-id="8fdad-240">视觉障碍用户的屏幕阅读器需采用替换文字。</span><span class="sxs-lookup"><span data-stu-id="8fdad-240">Alternate text is required for screen readers for the visually impaired.</span></span> <span data-ttu-id="8fdad-241">如果存在无法呈现图像的网站 bug，这也非常有用。</span><span class="sxs-lookup"><span data-stu-id="8fdad-241">It is also useful in case there is a site bug where the image cannot be rendered.</span></span>

<span data-ttu-id="8fdad-242">在包含文章的文件夹中，图像应存储在 `media/<article-name>` 文件夹中。</span><span class="sxs-lookup"><span data-stu-id="8fdad-242">Images should be stored in a `media/<article-name>` folder within the folder containing your article.</span></span> <span data-ttu-id="8fdad-243">不同的文章不应共享图像。</span><span class="sxs-lookup"><span data-stu-id="8fdad-243">Images should not be shared between articles.</span></span> <span data-ttu-id="8fdad-244">在 `media` 文件夹下创建与文章的文件名相匹配的文件夹。</span><span class="sxs-lookup"><span data-stu-id="8fdad-244">Create a folder that matches the filename of your article under the `media` folder.</span></span> <span data-ttu-id="8fdad-245">将该文章的图像复制到该新文件夹。</span><span class="sxs-lookup"><span data-stu-id="8fdad-245">Copy the images for that article to that new folder.</span></span> <span data-ttu-id="8fdad-246">如果多个文章使用一个图像，则每个图像文件夹都必须具有该图像文件的副本。</span><span class="sxs-lookup"><span data-stu-id="8fdad-246">If an image is used by multiple articles, each image folder must have a copy of that image file.</span></span> <span data-ttu-id="8fdad-247">这种做法可防止更改一篇文章的图像影响到另一篇文章。</span><span class="sxs-lookup"><span data-stu-id="8fdad-247">This practice prevents a change to an image in one article affecting another article.</span></span>

<span data-ttu-id="8fdad-248">在某些情况下，需要在多篇文章中共享图像，如徽标和图标。</span><span class="sxs-lookup"><span data-stu-id="8fdad-248">In some cases, you want to share images, like logos and icons, across multiple articles.</span></span> <span data-ttu-id="8fdad-249">这些图像存储在存储库根目录的 `/media/shared` 文件夹中。</span><span class="sxs-lookup"><span data-stu-id="8fdad-249">These images are stored in the `/media/shared` folder at the root of the repository.</span></span>

<span data-ttu-id="8fdad-250">支持下列图像文件类型：*.png"、*.gif"、*.jpeg"、*.jpg"、\*.svg</span><span class="sxs-lookup"><span data-stu-id="8fdad-250">The following image file types are supported: \*.png", \*.gif", \*.jpeg", \*.jpg", \*.svg</span></span>

<!-- External URLs -->
[platyPS]: https://github.com/PowerShell/platyPS
[markdig]: https://github.com/lunet-io/markdig
[CommonMark]: https://spec.commonmark.org/
[atx]: https://github.github.com/gfm/#atx-headings
[pascal-case]: https://en.wikipedia.org/wiki/PascalCase
[reflow]: https://marketplace.visualstudio.com/items?itemName=marvhen.reflow-markdown
