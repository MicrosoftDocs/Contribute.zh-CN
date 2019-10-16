---
title: 适用于 .NET 文章的模板和速查表
description: 本文包含一个便捷的模板，可用于针对 .NET 文档存储库创建新文章
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
ms.date: 11/07/2018
ms.openlocfilehash: 998ebf90c8a162451dd4ca2e7c8a55833ed9d408
ms.sourcegitcommit: ca84e542b081e145052f38967e826f6ef25da1b2
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/12/2019
ms.locfileid: "72288379"
---
# <a name="metadata-and-markdown-template-for-net-docs"></a><span data-ttu-id="7bf15-103">适用于 .NET 文档的元数据和 Markdown 模板</span><span class="sxs-lookup"><span data-stu-id="7bf15-103">Metadata and Markdown template for .NET docs</span></span>

<span data-ttu-id="7bf15-104">此 dotnet/docs 模板包含 Markdown 语法的示例，以及有关设置元数据的指导。</span><span class="sxs-lookup"><span data-stu-id="7bf15-104">This dotnet/docs template contains examples of Markdown syntax, as well as guidance on setting the metadata.</span></span>

<span data-ttu-id="7bf15-105">创建 Markdown 文件时，应将包括的模板复制到新文件，按如下所示填充元数据，并将上面的 H1 标题设为文章的标题。</span><span class="sxs-lookup"><span data-stu-id="7bf15-105">When creating a Markdown file, you should copy the included template to a new file, fill out the metadata as specified below, and set the H1 heading above to the title of the article.</span></span>

## <a name="metadata"></a><span data-ttu-id="7bf15-106">元数据</span><span class="sxs-lookup"><span data-stu-id="7bf15-106">Metadata</span></span>

<span data-ttu-id="7bf15-107">所需的元数据块位于以下示例元数据块中：</span><span class="sxs-lookup"><span data-stu-id="7bf15-107">The required metadata block is in the following sample metadata block:</span></span>

```markdown
---
title: [ARTICLE TITLE]
description: [usually a summary of your first paragraph. It gets displayed in search results, and can help drive the correct traffic if well written.]
author: [GITHUB USERNAME]
ms.date: [CREATION/UPDATE DATE - mm/dd/yyyy]
---
# The H1 should not be the same as the title, but should describe the article contents
```

- <span data-ttu-id="7bf15-108">冒号 (:) 和元数据元素值之间必须有空格  。</span><span class="sxs-lookup"><span data-stu-id="7bf15-108">You **must** have a space between the colon (:) and the value for a metadata element.</span></span>
- <span data-ttu-id="7bf15-109">值（例如，标题）中的冒号可中断元数据分析器。</span><span class="sxs-lookup"><span data-stu-id="7bf15-109">Colons in a value (for example, a title) break the metadata parser.</span></span> <span data-ttu-id="7bf15-110">在此情况下，使用双引号将标题括起来（例如，`title: "Writing .NET Core console apps: An advanced step-by-step guide"`）。</span><span class="sxs-lookup"><span data-stu-id="7bf15-110">In this case, surround the title with double quotes (for example, `title: "Writing .NET Core console apps: An advanced step-by-step guide"`).</span></span>
- <span data-ttu-id="7bf15-111">**标题**：在搜索引擎结果中显示。</span><span class="sxs-lookup"><span data-stu-id="7bf15-111">**title**: Appears in search engine results.</span></span> <span data-ttu-id="7bf15-112">该标题不应与 H1 标题中的标题相同，并且应包含不超过 60 个字符。</span><span class="sxs-lookup"><span data-stu-id="7bf15-112">The title shouldn't be identical to the title in your H1 heading, and it should contain 60 characters or less.</span></span>
- <span data-ttu-id="7bf15-113">**说明**：概括文章的内容。</span><span class="sxs-lookup"><span data-stu-id="7bf15-113">**description**: Summarizes the content of the article.</span></span> <span data-ttu-id="7bf15-114">它通常在搜索结果页中显示，并且不用于搜索排名。</span><span class="sxs-lookup"><span data-stu-id="7bf15-114">It's usually shown in the search results page, but it isn't used for search ranking.</span></span> <span data-ttu-id="7bf15-115">它的长度应为 115-145 个字符（含空格）。</span><span class="sxs-lookup"><span data-stu-id="7bf15-115">Its length should be 115-145 characters including spaces.</span></span>
- <span data-ttu-id="7bf15-116">**作者**：“作者”字段应包含作者的 GitHub 用户名  。</span><span class="sxs-lookup"><span data-stu-id="7bf15-116">**author**: The author field should contain the **GitHub username** of the author.</span></span>
- <span data-ttu-id="7bf15-117">**ms.date**：上一次重要更新的日期。</span><span class="sxs-lookup"><span data-stu-id="7bf15-117">**ms.date**: The date of the last significant update.</span></span> <span data-ttu-id="7bf15-118">如果已评审和更新整篇文章，请在现有文章中更新此内容。</span><span class="sxs-lookup"><span data-stu-id="7bf15-118">Update this on existing articles if you reviewed and updated the entire article.</span></span> <span data-ttu-id="7bf15-119">不保证更新拼写错误或类似的小修复。</span><span class="sxs-lookup"><span data-stu-id="7bf15-119">Small fixes, such as typos or similar do not warrant an update.</span></span>

<span data-ttu-id="7bf15-120">其他元数据附加于每篇文章，但我们通常在文件夹级别应用大多数元数据值，如 docfx.json 中所示  。</span><span class="sxs-lookup"><span data-stu-id="7bf15-120">Other metadata is attached to each article, but we typically apply most metadata values at the folder level, specified in **docfx.json**.</span></span>

## <a name="basic-markdown-gfm-and-special-characters"></a><span data-ttu-id="7bf15-121">基本 Markdown、GFM 和特殊字符</span><span class="sxs-lookup"><span data-stu-id="7bf15-121">Basic Markdown, GFM, and special characters</span></span>

<span data-ttu-id="7bf15-122">可在有关 [Markdown](how-to-write-use-markdown.md) 和 [Markdown 参考](markdown-reference.md)的一般性文章中了解 Markdown、GitHub Flavored Markdown (GFM) 和 OPS 特定扩展的基础知识。</span><span class="sxs-lookup"><span data-stu-id="7bf15-122">You can learn the basics of Markdown, GitHub Flavored Markdown (GFM), and OPS specific extensions in the general articles on [Markdown](how-to-write-use-markdown.md) and [Markdown reference](markdown-reference.md).</span></span>

<span data-ttu-id="7bf15-123">Markdown 使用特殊字符（例如，\*、\` 和 \#）进行格式设置。</span><span class="sxs-lookup"><span data-stu-id="7bf15-123">Markdown uses special characters such as \*, \`, and \# for formatting.</span></span> <span data-ttu-id="7bf15-124">如果要在内容中包括其中一个字符，必须执行以下两项操作之一：</span><span class="sxs-lookup"><span data-stu-id="7bf15-124">If you wish to include one of these characters in your content, you must do one of two things:</span></span>

- <span data-ttu-id="7bf15-125">在特殊字符前面放一个反斜杠，进行“转义”（例如 `\*` 表示 \*）。</span><span class="sxs-lookup"><span data-stu-id="7bf15-125">Put a backslash before the special character to "escape" it (for example, `\*` for a \*)</span></span>
- <span data-ttu-id="7bf15-126">对字符使用 [HTML 实体代码](http://www.ascii.cl/htmlcodes.htm)（例如，`&#42;` 表示 &#42;）。</span><span class="sxs-lookup"><span data-stu-id="7bf15-126">Use the [HTML entity code](http://www.ascii.cl/htmlcodes.htm) for the character (for example, `&#42;` for a &#42;).</span></span>

## <a name="file-names"></a><span data-ttu-id="7bf15-127">文件名</span><span class="sxs-lookup"><span data-stu-id="7bf15-127">File names</span></span>

<span data-ttu-id="7bf15-128">文件名使用以下规则：</span><span class="sxs-lookup"><span data-stu-id="7bf15-128">File names use the following rules:</span></span>

* <span data-ttu-id="7bf15-129">仅包含小写字母、数字和连字符。</span><span class="sxs-lookup"><span data-stu-id="7bf15-129">Contain only lowercase letters, numbers, and hyphens.</span></span>
* <span data-ttu-id="7bf15-130">不使用空格或标点符号字符。</span><span class="sxs-lookup"><span data-stu-id="7bf15-130">No spaces or punctuation characters.</span></span> <span data-ttu-id="7bf15-131">使用连字符分隔文件名中的单词和数字。</span><span class="sxs-lookup"><span data-stu-id="7bf15-131">Use the hyphens to separate words and numbers in the file name.</span></span>
* <span data-ttu-id="7bf15-132">使用特定的行为动词，如开发、购买、构建和故障排除。</span><span class="sxs-lookup"><span data-stu-id="7bf15-132">Use action verbs that are specific, such as develop, buy, build, troubleshoot.</span></span> <span data-ttu-id="7bf15-133">不使用后缀是 ing 的单词。</span><span class="sxs-lookup"><span data-stu-id="7bf15-133">No -ing words.</span></span>
* <span data-ttu-id="7bf15-134">不使用小词汇 - 不包含 a、and、the、in 或 or 等。</span><span class="sxs-lookup"><span data-stu-id="7bf15-134">No small words - don't include a, and, the, in, or, etc.</span></span>
* <span data-ttu-id="7bf15-135">必须在 Markdown 中且使用 .md 文件扩展名。</span><span class="sxs-lookup"><span data-stu-id="7bf15-135">Must be in Markdown and use the .md file extension.</span></span>
* <span data-ttu-id="7bf15-136">使文件名尽量简短，且适当合理。</span><span class="sxs-lookup"><span data-stu-id="7bf15-136">Keep file names reasonably short.</span></span> <span data-ttu-id="7bf15-137">此名称会包含在文章的 URL 中。</span><span class="sxs-lookup"><span data-stu-id="7bf15-137">They are part of the URL for your articles.</span></span>

## <a name="headings"></a><span data-ttu-id="7bf15-138">标题</span><span class="sxs-lookup"><span data-stu-id="7bf15-138">Headings</span></span>

<span data-ttu-id="7bf15-139">使用句式大写。</span><span class="sxs-lookup"><span data-stu-id="7bf15-139">Use sentence-style capitalization.</span></span> <span data-ttu-id="7bf15-140">始终大写标题的第一个字词。</span><span class="sxs-lookup"><span data-stu-id="7bf15-140">Always capitalize the first word of a heading.</span></span>

## <a name="text-styling"></a><span data-ttu-id="7bf15-141">文本样式</span><span class="sxs-lookup"><span data-stu-id="7bf15-141">Text styling</span></span>

<span data-ttu-id="7bf15-142">斜体：用于文件、文件夹、路径（对于较长项，拆分成其自己的行）、新术语  。</span><span class="sxs-lookup"><span data-stu-id="7bf15-142">*Italics* Use for files, folders, paths (for long items, split onto their own line), new terms.</span></span>

<span data-ttu-id="7bf15-143">粗体：用于 UI 元素  。</span><span class="sxs-lookup"><span data-stu-id="7bf15-143">**Bold** Use for UI elements.</span></span>

<span data-ttu-id="7bf15-144">`Code` 用于内联代码、语言关键字、NuGet 包名称、命令行命令、数据库表和列名称，以及不希望可单击的 URL。</span><span class="sxs-lookup"><span data-stu-id="7bf15-144">`Code` Use for inline code, language keywords, NuGet package names, command-line commands, database table and column names, and URLs that you don't want to be clickable.</span></span>

## <a name="links"></a><span data-ttu-id="7bf15-145">链接</span><span class="sxs-lookup"><span data-stu-id="7bf15-145">Links</span></span>

<span data-ttu-id="7bf15-146">请参阅有关[链接](how-to-write-links.md)的一般性文章，了解有关定位标记、内部链接、其他文档链接、代码包含和外部链接的信息。</span><span class="sxs-lookup"><span data-stu-id="7bf15-146">See the general article on [Links](how-to-write-links.md) for information about anchors, internal links, links to other documents, code includes, and external links.</span></span>

<span data-ttu-id="7bf15-147">.NET 文档团队使用以下约定：</span><span class="sxs-lookup"><span data-stu-id="7bf15-147">The .NET docs team uses the following conventions:</span></span>

- <span data-ttu-id="7bf15-148">在大多数情况下，我们使用相对链接，并且不鼓励在链接中使用 `~/` GitHub 上的源进行解析。</span><span class="sxs-lookup"><span data-stu-id="7bf15-148">In most cases, we use the relative links and discourage the use of `~/` in links because relative links resolve in the source on GitHub.</span></span> <span data-ttu-id="7bf15-149">然而，每当我们链接到独立存储库中的文件时，都将使用 `~/` 字符提供路径。</span><span class="sxs-lookup"><span data-stu-id="7bf15-149">However, whenever we link to a file in a dependent repo, we'll use the `~/` character to provide the path.</span></span> <span data-ttu-id="7bf15-150">因为独立存储库中的文件位于 GitHub 中的不同位置，因此使用相对链接无法正确解析，无论其编写方式如何。</span><span class="sxs-lookup"><span data-stu-id="7bf15-150">Because the files in the dependent repo are in a different location in GitHub the links won't resolve correctly with relative links regardless of how they were written.</span></span>
- <span data-ttu-id="7bf15-151">C# 语言规范和 Visual Basic 语言规范通过来自语言存储库中的源，包括在 .NET 文档中。</span><span class="sxs-lookup"><span data-stu-id="7bf15-151">The C# language specification and the Visual Basic language specification are included in the .NET docs by including the source from the language repositories.</span></span> <span data-ttu-id="7bf15-152">Markdown 源托管于 [csharplang](https://github.com/dotnet/csharplang) 和 [vblang](https://github.com/dotnet/vblang) 存储库中。</span><span class="sxs-lookup"><span data-stu-id="7bf15-152">The markdown sources are managed in the [csharplang](https://github.com/dotnet/csharplang) and [vblang](https://github.com/dotnet/vblang) repositories.</span></span>

<span data-ttu-id="7bf15-153">规范的链接必须指向其中包括这些规范的源目录。</span><span class="sxs-lookup"><span data-stu-id="7bf15-153">Links to the spec must point to the source directories where those specs are included.</span></span> <span data-ttu-id="7bf15-154">对于 C#，它是 ~/_csharplang/spec，而对于 VB，它是 ~/_vblang/spec如下例所示   ：</span><span class="sxs-lookup"><span data-stu-id="7bf15-154">For C#, it's **~/_csharplang/spec** and for VB, it's **~/_vblang/spec**, as in the following example:</span></span>

```markdown
[C# Query Expressions](~/_csharplang/spec/expressions.md#query-expressions)
```

### <a name="links-to-apis"></a><span data-ttu-id="7bf15-155">链接到 API</span><span class="sxs-lookup"><span data-stu-id="7bf15-155">Links to APIs</span></span>

<span data-ttu-id="7bf15-156">生成系统具有一些扩展，使我们能够链接到 .NET API，而无需使用外部链接。</span><span class="sxs-lookup"><span data-stu-id="7bf15-156">The build system has some extensions that allow us to link to .NET APIs without having to use external links.</span></span> <span data-ttu-id="7bf15-157">可以使用下列语法之一：</span><span class="sxs-lookup"><span data-stu-id="7bf15-157">You use one of the following syntax:</span></span>

1. <span data-ttu-id="7bf15-158">自动链接：`<xref:UID>` 或 `<xref:UID?displayProperty=nameWithType>`</span><span class="sxs-lookup"><span data-stu-id="7bf15-158">Auto-link: `<xref:UID>` or `<xref:UID?displayProperty=nameWithType>`</span></span>

   <span data-ttu-id="7bf15-159">`displayProperty` 查询参数生成完全限定的链接文本。</span><span class="sxs-lookup"><span data-stu-id="7bf15-159">The `displayProperty` query parameter produces a fully qualified link text.</span></span> <span data-ttu-id="7bf15-160">默认情况下，链接文本仅显示成员名称或类型名称。</span><span class="sxs-lookup"><span data-stu-id="7bf15-160">By default, link text shows only the member or type name.</span></span>

2. <span data-ttu-id="7bf15-161">Markdown 链接：`[link text](xref:UID)`</span><span class="sxs-lookup"><span data-stu-id="7bf15-161">Markdown link: `[link text](xref:UID)`</span></span>

   <span data-ttu-id="7bf15-162">用于自定义显示的链接文本。</span><span class="sxs-lookup"><span data-stu-id="7bf15-162">Use when you want to customize the link text displayed.</span></span>

<span data-ttu-id="7bf15-163">示例：</span><span class="sxs-lookup"><span data-stu-id="7bf15-163">Examples:</span></span>

- <span data-ttu-id="7bf15-164">`<xref:System.String>` 呈现为 [String](https://docs.microsoft.com/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="7bf15-164">`<xref:System.String>` renders as [String](https://docs.microsoft.com/dotnet/api/system.string)</span></span>
- <span data-ttu-id="7bf15-165">`<xref:System.String?displayProperty=nameWithType>` 呈现为 [System.String](https://docs.microsoft.com/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="7bf15-165">`<xref:System.String?displayProperty=nameWithType>` renders as [System.String](https://docs.microsoft.com/dotnet/api/system.string)</span></span>
- <span data-ttu-id="7bf15-166">`[String class](xref:System.String)` 呈现为 [String 类](https://docs.microsoft.com/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="7bf15-166">`[String class](xref:System.String)` renders as [String class](https://docs.microsoft.com/dotnet/api/system.string)</span></span>

<span data-ttu-id="7bf15-167">若要详细了解如何使用此表示法，请参阅[使用交叉引用](https://dotnet.github.io/docfx/tutorial/links_and_cross_references.html#using-cross-reference)。</span><span class="sxs-lookup"><span data-stu-id="7bf15-167">For more information about using this notation, see [Using cross reference](https://dotnet.github.io/docfx/tutorial/links_and_cross_references.html#using-cross-reference).</span></span>

<span data-ttu-id="7bf15-168">某些 UID 包含特殊字符 \`、\# 或 \*，需要对 UID 值执行 HTML 编码，分别编码为 `%60`、`%23` 和 `%2A`。</span><span class="sxs-lookup"><span data-stu-id="7bf15-168">Some UIDs contain the special characters \`, \# or \*, the UID value needs to be HTML encoded as `%60`, `%23` and `%2A` respectively.</span></span> <span data-ttu-id="7bf15-169">虽然有时会发现括号也被编码，但对此并不作要求。</span><span class="sxs-lookup"><span data-stu-id="7bf15-169">You'll sometimes see parentheses encoded but it's not a requirement.</span></span>

<span data-ttu-id="7bf15-170">示例：</span><span class="sxs-lookup"><span data-stu-id="7bf15-170">Examples:</span></span>

- <span data-ttu-id="7bf15-171">System.Threading.Tasks.Task\`1 变为 `System.Threading.Tasks.Task%601`</span><span class="sxs-lookup"><span data-stu-id="7bf15-171">System.Threading.Tasks.Task\`1 becomes `System.Threading.Tasks.Task%601`</span></span>
- <span data-ttu-id="7bf15-172">System.Exception.\#ctor 变为 `System.Exception.%23ctor`</span><span class="sxs-lookup"><span data-stu-id="7bf15-172">System.Exception.\#ctor becomes `System.Exception.%23ctor`</span></span>
- <span data-ttu-id="7bf15-173">System.Lazy\`1.\#ctor(System.Threading.LazyThreadSafetyMode) 变为 `System.Lazy%601.%23ctor%28System.Threading.LazyThreadSafetyMode%29`</span><span class="sxs-lookup"><span data-stu-id="7bf15-173">System.Lazy\`1.\#ctor(System.Threading.LazyThreadSafetyMode) becomes  `System.Lazy%601.%23ctor%28System.Threading.LazyThreadSafetyMode%29`</span></span>

<span data-ttu-id="7bf15-174">可以在 `https://xref.docs.microsoft.com/autocomplete` 中查找类型的 UID、成员重载列表或特定的重载成员。</span><span class="sxs-lookup"><span data-stu-id="7bf15-174">You can find the UIDs of types, a member overload list, or a particular overloaded member from `https://xref.docs.microsoft.com/autocomplete`.</span></span> <span data-ttu-id="7bf15-175">查询字符串 `?text=*\<type-member-name>*` 可标识要查看其 UID 的类型或成员。</span><span class="sxs-lookup"><span data-stu-id="7bf15-175">The query string `?text=*\<type-member-name>*` identifies the type or member whose UIDs you'd like to see.</span></span> <span data-ttu-id="7bf15-176">例如，`https://xref.docs.microsoft.com/autocomplete?text=string.format` 将检索 [String.Format](https://docs.microsoft.com/dotnet/api/system.string.format) 重载。</span><span class="sxs-lookup"><span data-stu-id="7bf15-176">For example, `https://xref.docs.microsoft.com/autocomplete?text=string.format` retrieves the [String.Format](https://docs.microsoft.com/dotnet/api/system.string.format) overloads.</span></span> <span data-ttu-id="7bf15-177">该工具可在 UID 的任意部分中搜索提供的 `text` 查询参数。</span><span class="sxs-lookup"><span data-stu-id="7bf15-177">The tool searches for the provided `text` query parameter in any part of the UID.</span></span> <span data-ttu-id="7bf15-178">例如，可以搜索成员名称 (ToString)、部分成员名称 (ToStri)、类型和成员名称 (Double.ToString) 等。</span><span class="sxs-lookup"><span data-stu-id="7bf15-178">For example, you can search for member name (ToString), partial member name (ToStri), type and member name (Double.ToString), etc.</span></span>

<span data-ttu-id="7bf15-179">如果在 UID 后面添加 \*（或 `%2A`），该链接则表示重载页面，而不是特定 API。</span><span class="sxs-lookup"><span data-stu-id="7bf15-179">If you add a \* (or `%2A`) after the UID, the link then represents the overload page and not a specific API.</span></span> <span data-ttu-id="7bf15-180">例如，若要通过一般方式链接到 [List\<T>.BinarySearch 方法](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1.binarysearch)页面，而不是通过 [List\<T>.BinarySearch(T, IComparer\<T>)](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1.binarysearch#System_Collections_Generic_List_1_BinarySearch__0_) 等特定重载，可以使用它。</span><span class="sxs-lookup"><span data-stu-id="7bf15-180">For example, you can use that when you want to link to the [List\<T>.BinarySearch Method](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1.binarysearch) page in a generic way instead of a specific overload such as [List\<T>.BinarySearch(T, IComparer\<T>)](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1.binarysearch#System_Collections_Generic_List_1_BinarySearch__0_).</span></span> <span data-ttu-id="7bf15-181">此外，如果未重载成员，还可以使用 \* 链接到成员页，这可消除在 UID 中包括参数列表的需求。</span><span class="sxs-lookup"><span data-stu-id="7bf15-181">You can also use \* to link to a member page when the member is not overloaded; this saves you from having to include the parameter list in the UID.</span></span>

<span data-ttu-id="7bf15-182">若要链接到特定的方法重载，必须包括每个方法参数的完全限定的类型名称。</span><span class="sxs-lookup"><span data-stu-id="7bf15-182">To link to a specific method overload, you must include the fully qualified type name of each of the method's parameters.</span></span> <span data-ttu-id="7bf15-183">例如，\<xref:System.DateTime.ToString> 可链接到无参数的 [DateTime.ToString](https://docs.microsoft.com/dotnet/api/system.datetime.tostring#System_DateTime_ToString) 方法，而 \<xref:System.DateTime.ToString(System.String,System.IFormatProvider)> 可链接到 [DateTime.ToString(String,IFormatProvider)](https://docs.microsoft.com/dotnet/api/system.datetime.tostring#System_DateTime_ToString_System_String_System_IFormatProvider_) 方法。</span><span class="sxs-lookup"><span data-stu-id="7bf15-183">For example, \<xref:System.DateTime.ToString> links to the parameterless [DateTime.ToString](https://docs.microsoft.com/dotnet/api/system.datetime.tostring#System_DateTime_ToString) method, while \<xref:System.DateTime.ToString(System.String,System.IFormatProvider)> links to the  [DateTime.ToString(String,IFormatProvider)](https://docs.microsoft.com/dotnet/api/system.datetime.tostring#System_DateTime_ToString_System_String_System_IFormatProvider_) method.</span></span>

<span data-ttu-id="7bf15-184">若要链接到泛型类型（例如 [System.Collections.Generic.List\<T>](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1)），可使用 \` (`%60`) 字符，其后紧跟泛型类型参数的数量。</span><span class="sxs-lookup"><span data-stu-id="7bf15-184">To link to a generic type, such as [System.Collections.Generic.List\<T>](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1), you use the \` (`%60`) character followed by the number of generic type parameters.</span></span> <span data-ttu-id="7bf15-185">例如，`<xref:System.Nullable%601>` 可链接到 [System.Nullable\<T>](https://docs.microsoft.com/dotnet/api/system.nullable-1) 类型，而 `<xref:System.Func%602>` 可链接到 [System.Func\<T,TResult>](https://docs.microsoft.com/dotnet/api/system.func-2) 委托。</span><span class="sxs-lookup"><span data-stu-id="7bf15-185">For example, `<xref:System.Nullable%601>` links to the [System.Nullable\<T>](https://docs.microsoft.com/dotnet/api/system.nullable-1) type, while `<xref:System.Func%602>` links to the [System.Func\<T,TResult>](https://docs.microsoft.com/dotnet/api/system.func-2) delegate.</span></span>

## <a name="code"></a><span data-ttu-id="7bf15-186">代码</span><span class="sxs-lookup"><span data-stu-id="7bf15-186">Code</span></span>

<span data-ttu-id="7bf15-187">包括代码的最佳方式是包括工作示例中的代码片段。</span><span class="sxs-lookup"><span data-stu-id="7bf15-187">The best way to include code is to include snippets from a working sample.</span></span> <span data-ttu-id="7bf15-188">请遵循[参与 .NET](dotnet-contribute-process.md#contributing-to-samples) 一文中的说明，创建示例。</span><span class="sxs-lookup"><span data-stu-id="7bf15-188">Create your sample following the instructions in the [contributing to .NET](dotnet-contribute-process.md#contributing-to-samples) article.</span></span> <span data-ttu-id="7bf15-189">包括代码的基本规则位于有关[代码](how-to-write-use-markdown.md#code-snippets)的通用指南中。</span><span class="sxs-lookup"><span data-stu-id="7bf15-189">The basic rules for including code are located in the general guidance on [code](how-to-write-use-markdown.md#code-snippets).</span></span>

<span data-ttu-id="7bf15-190">可使用以下语法，包括代码：</span><span class="sxs-lookup"><span data-stu-id="7bf15-190">You can include the code using the following syntax:</span></span>

```markdown
[!code-<language>[<name>](<pathToFile><queryoption><queryoptionvalue>)]
```

* <span data-ttu-id="7bf15-191">`-<language>`（是可选的，但建议采用）  </span><span class="sxs-lookup"><span data-stu-id="7bf15-191">`-<language>` (*optional* but *recommended*)</span></span>
  * <span data-ttu-id="7bf15-192">要引用的代码片段的语言。</span><span class="sxs-lookup"><span data-stu-id="7bf15-192">Language of the code snippet being referenced.</span></span>

* <span data-ttu-id="7bf15-193">`<name>`（可选） </span><span class="sxs-lookup"><span data-stu-id="7bf15-193">`<name>` (*optional*)</span></span>
  * <span data-ttu-id="7bf15-194">代码片段的名称。</span><span class="sxs-lookup"><span data-stu-id="7bf15-194">Name for the code snippet.</span></span> <span data-ttu-id="7bf15-195">这不会对输出 HTML 产生影响，但可用于增强 Markdown 源的可读性。</span><span class="sxs-lookup"><span data-stu-id="7bf15-195">It doesn’t have any impact on the output HTML, but you can use it to improve the readability of your Markdown source.</span></span>

* <span data-ttu-id="7bf15-196">`<pathToFile>`（必需） </span><span class="sxs-lookup"><span data-stu-id="7bf15-196">`<pathToFile>` (*mandatory*)</span></span>
  * <span data-ttu-id="7bf15-197">文件系统中的相对路径，指示将引用的代码片段文件。</span><span class="sxs-lookup"><span data-stu-id="7bf15-197">Relative path in the file system that indicates the code snippet file to reference.</span></span> <span data-ttu-id="7bf15-198">根据组成 .NET 文档集的不同存储库，这可能很复杂。</span><span class="sxs-lookup"><span data-stu-id="7bf15-198">This can be complicated by the different repos that make up the .NET doc set.</span></span> <span data-ttu-id="7bf15-199">.NET 示例位于 dotnet/示例存储库。</span><span class="sxs-lookup"><span data-stu-id="7bf15-199">The .NET samples are in the dotnet/samples repo.</span></span> <span data-ttu-id="7bf15-200">所有代码片段路径都会以 `~/samples` 开头，路径其余部分为该存储库的根目录中的源路径。</span><span class="sxs-lookup"><span data-stu-id="7bf15-200">All snippet paths would start with `~/samples`, the rest of the path being the path to the source from the root of that repo.</span></span>

* <span data-ttu-id="7bf15-201">`<queryoption>`（可选） </span><span class="sxs-lookup"><span data-stu-id="7bf15-201">`<queryoption>` (*optional*)</span></span>
  * <span data-ttu-id="7bf15-202">用于指定如何从文件中检索代码：</span><span class="sxs-lookup"><span data-stu-id="7bf15-202">Used to specify how the code should be retrieved from the file:</span></span>
    * <span data-ttu-id="7bf15-203">`#`：`#{tagname}`（标记名称）或 `#L{startlinenumber}-L{endlinenumber}`（行范围）  。</span><span class="sxs-lookup"><span data-stu-id="7bf15-203">`#`:  `#{tagname}` (tag name) *or* `#L{startlinenumber}-L{endlinenumber}` (line range).</span></span>
    <span data-ttu-id="7bf15-204">不鼓励使用行号，因为它们很脆弱。</span><span class="sxs-lookup"><span data-stu-id="7bf15-204">We discourage the use of line numbers because they are very brittle.</span></span> <span data-ttu-id="7bf15-205">标记名称是引用代码片段的首选方式。</span><span class="sxs-lookup"><span data-stu-id="7bf15-205">Tag name is the preferred way of referencing code snippets.</span></span> <span data-ttu-id="7bf15-206">请使用有意义的标记名称。</span><span class="sxs-lookup"><span data-stu-id="7bf15-206">Use meaningful tag names.</span></span> <span data-ttu-id="7bf15-207">（由于许多代码片段迁移自上一个平台，并且标记具有 `Snippet1`、`Snippet2` 等名称。因此维持此做法要困难得多。）</span><span class="sxs-lookup"><span data-stu-id="7bf15-207">(Many snippets were migrated from a previous platform and the tags have names such as `Snippet1`, `Snippet2` etc. That practice is much harder to maintain.)</span></span>
    * <span data-ttu-id="7bf15-208">`range`：`?range=1,3-5` 行的范围。</span><span class="sxs-lookup"><span data-stu-id="7bf15-208">`range`: `?range=1,3-5` A range of lines.</span></span> <span data-ttu-id="7bf15-209">此示例包含第 1、3、4 和 5 行。</span><span class="sxs-lookup"><span data-stu-id="7bf15-209">This example includes lines 1, 3, 4, and 5.</span></span>

<span data-ttu-id="7bf15-210">建议在可能的情况下使用标记名称。</span><span class="sxs-lookup"><span data-stu-id="7bf15-210">We recommend using the tag name option whenever possible.</span></span> <span data-ttu-id="7bf15-211">标记名称是区域或代码注释的名称，在源代码中以 `Snippettagname` 格式存在。</span><span class="sxs-lookup"><span data-stu-id="7bf15-211">The tag name is the name of a region or of a code comment in the format of `Snippettagname` present in the source code.</span></span> <span data-ttu-id="7bf15-212">以下示例说明如何引用标记名称 `BasicThrow`：</span><span class="sxs-lookup"><span data-stu-id="7bf15-212">The following example shows how to refer to the tag name `BasicThrow`:</span></span>

```markdown
[!code-csharp[csrefKeyword#1](~/samples/snippets/snippets/csharp/language-reference/operators/ConditionalExamples.csConditionalRef)]
```

<span data-ttu-id="7bf15-213">dotnet/示例存储库中源的相对路径遵循 `~/samples` 路径  。</span><span class="sxs-lookup"><span data-stu-id="7bf15-213">The relative path to the source in the **dotnet/samples** repo follows the `~/samples` path.</span></span>

<span data-ttu-id="7bf15-214">并且，可在[此源文件](https://github.com/dotnet/samples/blob/master/snippets/csharp/language-reference/operators/ConditionalExamples.cs)中了解代码片段标记的构成方式。</span><span class="sxs-lookup"><span data-stu-id="7bf15-214">And you can see how the snippet tags are structured in [this source file](https://github.com/dotnet/samples/blob/master/snippets/csharp/language-reference/operators/ConditionalExamples.cs).</span></span> <span data-ttu-id="7bf15-215">有关按语言在代码片段源文件中呈现标记名称的详细信息，请参阅 [DocFX 准则](https://dotnet.github.io/docfx/spec/docfx_flavored_markdown.html#tag-name-representation-in-code-snippet-source-file)。</span><span class="sxs-lookup"><span data-stu-id="7bf15-215">For details about tag name representation in code snippet source files by language, see the [DocFX guidelines](https://dotnet.github.io/docfx/spec/docfx_flavored_markdown.html#tag-name-representation-in-code-snippet-source-file).</span></span>

<span data-ttu-id="7bf15-216">以下示例介绍在所有三种 .NET 语言中包含的代码：</span><span class="sxs-lookup"><span data-stu-id="7bf15-216">The following example shows code included in all three .NET languages:</span></span>

```markdown
[!code-fsharp[ToPigLatin](../../../samples/snippets/fsharp/getting-started/pig-latin.fs#L1-L14)]
 [!code-csharp[ADCreateDomain#2](../../../samples/snippets/csharp/VS_Snippets_CLR/ADCreateDomain/CS/source2.cs#2)]
 [!code-vb[ADCreateDomain#2](../../../samples/snippets/visualbasic/VS_Snippets_CLR/ADCreateDomain/VB/source2.vb#2)]  
```

<span data-ttu-id="7bf15-217">包含来自完整程序的代码片段可确保所有代码通过持续集成 (CI) 系统运行。</span><span class="sxs-lookup"><span data-stu-id="7bf15-217">Including snippets from full programs ensures that all code runs through our Continuous Integration (CI) system.</span></span> <span data-ttu-id="7bf15-218">然而，如果需要显示导致编译时或运行时错误的内容，可以使用内联代码块。</span><span class="sxs-lookup"><span data-stu-id="7bf15-218">However, if you need to show something that causes compile time or runtime errors, you can use inline code blocks.</span></span>

## <a name="images"></a><span data-ttu-id="7bf15-219">图像</span><span class="sxs-lookup"><span data-stu-id="7bf15-219">Images</span></span>

### <a name="static-image-or-animated-gif"></a><span data-ttu-id="7bf15-220">静态图像或动态 GIF</span><span class="sxs-lookup"><span data-stu-id="7bf15-220">Static image or animated GIF</span></span>

```markdown
![this is the alt text](../images/Logo_DotNet.png)
```

### <a name="linked-image"></a><span data-ttu-id="7bf15-221">链接图像</span><span class="sxs-lookup"><span data-stu-id="7bf15-221">Linked image</span></span>

```markdown
[![alt text for linked image](../images/Logo_DotNet.png)](https://dot.net)
```

## <a name="videos"></a><span data-ttu-id="7bf15-222">视频</span><span class="sxs-lookup"><span data-stu-id="7bf15-222">Videos</span></span>

<span data-ttu-id="7bf15-223">目前，可使用以下语法，同时嵌入 Channel 9 和 YouTube 视频：</span><span class="sxs-lookup"><span data-stu-id="7bf15-223">Currently, you can embed both Channel 9 and YouTube videos with the following syntax:</span></span>

### <a name="channel-9"></a><span data-ttu-id="7bf15-224">Channel 9</span><span class="sxs-lookup"><span data-stu-id="7bf15-224">Channel 9</span></span>

```markdown
> [!VIDEO <channel9_video_link>]
```

<span data-ttu-id="7bf15-225">若要获取视频的正确 URL，请选择视频框架下方的“嵌入”，然后复制 `<iframe>` 元素中的 URL  。</span><span class="sxs-lookup"><span data-stu-id="7bf15-225">To get the video's correct URL, select the **Embed** tab below the video frame, and copy the URL from the `<iframe>` element.</span></span> <span data-ttu-id="7bf15-226">例如：</span><span class="sxs-lookup"><span data-stu-id="7bf15-226">For example:</span></span>

```markdown
> [!VIDEO https://channel9.msdn.com/Blogs/dotnet/NET-Core-20-Released/player]
```

### <a name="youtube"></a><span data-ttu-id="7bf15-227">YouTube</span><span class="sxs-lookup"><span data-stu-id="7bf15-227">YouTube</span></span>

<span data-ttu-id="7bf15-228">若要获取视频的正确 URL，右键单击视频，选择“复制嵌入代码”，然后复制 `<iframe>` 元素中的 URL  。</span><span class="sxs-lookup"><span data-stu-id="7bf15-228">To get the video's correct URL, right-click on the video, select **Copy Embed Code**, and copy the URL from the `<iframe>` element.</span></span>

```markdown
> [!VIDEO <youtube_video_link>]
```

<span data-ttu-id="7bf15-229">例如：</span><span class="sxs-lookup"><span data-stu-id="7bf15-229">For example:</span></span>

```markdown
> [!VIDEO https://www.youtube.com/embed/Q2mMbjw6cLA]
```

## <a name="docsmicrosoft-extensions"></a><span data-ttu-id="7bf15-230">docs.microsoft 扩展</span><span class="sxs-lookup"><span data-stu-id="7bf15-230">docs.microsoft extensions</span></span>

<span data-ttu-id="7bf15-231">docs.microsoft 可提供 GitHub Flavored Markdown 的一些额外扩展。</span><span class="sxs-lookup"><span data-stu-id="7bf15-231">docs.microsoft provides a few additional extensions to GitHub Flavored Markdown.</span></span>

### <a name="checked-lists"></a><span data-ttu-id="7bf15-232">核对清单</span><span class="sxs-lookup"><span data-stu-id="7bf15-232">Checked lists</span></span>

<span data-ttu-id="7bf15-233">自定义样式适用于列表。</span><span class="sxs-lookup"><span data-stu-id="7bf15-233">A custom style is available for lists.</span></span> <span data-ttu-id="7bf15-234">可呈现带绿色复选标记的列表。</span><span class="sxs-lookup"><span data-stu-id="7bf15-234">You can render lists with green check marks.</span></span>

```markdown
> [!div class="checklist"]
> * How to create a .NET Core app
> * How to add a reference to the Microsoft.XmlSerializer.Generator package
> * How to edit your MyApp.csproj to add dependencies
> * How to add a class and an XmlSerializer
> * How to build and run the application
```

<span data-ttu-id="7bf15-235">这将呈现为：</span><span class="sxs-lookup"><span data-stu-id="7bf15-235">This renders as:</span></span>

> [!div class="checklist"]
> * <span data-ttu-id="7bf15-236">如何创建 .NET Core 应用</span><span class="sxs-lookup"><span data-stu-id="7bf15-236">How to create a .NET Core app</span></span>
> * <span data-ttu-id="7bf15-237">如何添加 Microsoft.XmlSerializer.Generator 包引用</span><span class="sxs-lookup"><span data-stu-id="7bf15-237">How to add a reference to the Microsoft.XmlSerializer.Generator package</span></span>
> * <span data-ttu-id="7bf15-238">如何编辑 MyApp.csproj，以添加依赖项</span><span class="sxs-lookup"><span data-stu-id="7bf15-238">How to edit your MyApp.csproj to add dependencies</span></span>
> * <span data-ttu-id="7bf15-239">如何添加类和 XmlSerializer</span><span class="sxs-lookup"><span data-stu-id="7bf15-239">How to add a class and an XmlSerializer</span></span>
> * <span data-ttu-id="7bf15-240">如何生成并运行应用程序</span><span class="sxs-lookup"><span data-stu-id="7bf15-240">How to build and run the application</span></span>

<span data-ttu-id="7bf15-241">可在 [.NET Core 文档](https://docs.microsoft.com/dotnet/core/additional-tools/xml-serializer-generator)中查看有效的核对清单示例。</span><span class="sxs-lookup"><span data-stu-id="7bf15-241">You can see an example of checked lists in action in the [.NET Core docs](https://docs.microsoft.com/dotnet/core/additional-tools/xml-serializer-generator).</span></span>

### <a name="buttons"></a><span data-ttu-id="7bf15-242">按钮</span><span class="sxs-lookup"><span data-stu-id="7bf15-242">Buttons</span></span>

<span data-ttu-id="7bf15-243">按钮链接：</span><span class="sxs-lookup"><span data-stu-id="7bf15-243">Button links:</span></span>

```markdown
> [!div class="button"]
> [button links](dotnet-contribute.md)
```

<span data-ttu-id="7bf15-244">这将呈现为：</span><span class="sxs-lookup"><span data-stu-id="7bf15-244">This renders as:</span></span>

> [!div class="button"]
> [<span data-ttu-id="7bf15-245">按钮链接</span><span class="sxs-lookup"><span data-stu-id="7bf15-245">button links</span></span>](dotnet-contribute.md)

<span data-ttu-id="7bf15-246">可在 [Visual Studio 文档](https://docs.microsoft.com/visualstudio/install/install-visual-studio#step-2---download-visual-studio)中查看有效的按钮示例。</span><span class="sxs-lookup"><span data-stu-id="7bf15-246">You can see an example of buttons in action in the [Visual Studio docs](https://docs.microsoft.com/visualstudio/install/install-visual-studio#step-2---download-visual-studio).</span></span>

### <a name="step-by-steps"></a><span data-ttu-id="7bf15-247">分步操作</span><span class="sxs-lookup"><span data-stu-id="7bf15-247">Step-by-steps</span></span>

```markdown
>[!div class="step-by-step"]
> [Pre](../docs/csharp/expression-trees-interpreting.md)
> [Next](../docs/csharp/expression-trees-translating.md)
```

<span data-ttu-id="7bf15-248">可在 [C# 指南](https://docs.microsoft.com/dotnet/csharp/tour-of-csharp/program-structure)中查看有效的分步操作示例。</span><span class="sxs-lookup"><span data-stu-id="7bf15-248">You can see an example of step-by-steps in action at the [C# Guide](https://docs.microsoft.com/dotnet/csharp/tour-of-csharp/program-structure).</span></span>
