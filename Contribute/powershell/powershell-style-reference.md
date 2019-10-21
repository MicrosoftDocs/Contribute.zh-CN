---
title: 有关编写 cmdlet 引用的特定指南
description: 本文介绍有关设置 PowerShell 代码示例格式的特定规则。 这适用于包含示例的概念性文章以及 cmdlet 引用。
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
author: sdwheeler
ms.author: sewhee
ms.date: 10/09/2019
ms.openlocfilehash: 793a3c02ae0edf192416ae514585d5161e8c1f98
ms.sourcegitcommit: ca84e542b081e145052f38967e826f6ef25da1b2
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/12/2019
ms.locfileid: "72290279"
---
# <a name="updating-reference-articles"></a><span data-ttu-id="d74f9-104">更新引用文章</span><span class="sxs-lookup"><span data-stu-id="d74f9-104">Updating reference articles</span></span>

<span data-ttu-id="d74f9-105">Cmdlet 引用文章具有特定的结构。</span><span class="sxs-lookup"><span data-stu-id="d74f9-105">Cmdlet reference articles have a specific structure.</span></span> <span data-ttu-id="d74f9-106">此结构由 PlatyPS 定义[][]。</span><span class="sxs-lookup"><span data-stu-id="d74f9-106">This structure is defined by [PlatyPS][].</span></span>
<span data-ttu-id="d74f9-107">PlatyPS 工具用于生成 PowerShell 模块的 cmdlet 帮助。</span><span class="sxs-lookup"><span data-stu-id="d74f9-107">PlatyPS is the tool we use to generate cmdlet help for PowerShell modules.</span></span> <span data-ttu-id="d74f9-108">PlatyPS 为 cmdlet 创建基础 Markdown 文件。</span><span class="sxs-lookup"><span data-stu-id="d74f9-108">PlatyPS creates the base Markdown file for a cmdlet.</span></span> <span data-ttu-id="d74f9-109">编辑 Markdown 文件后，使用 PlatyPS 创建 `Get-Help` cmdlet 使用的 MAML 帮助文件。</span><span class="sxs-lookup"><span data-stu-id="d74f9-109">After editing the Markdown files, PlatyPS is used create the MAML help files used by the `Get-Help` cmdlet.</span></span>

<span data-ttu-id="d74f9-110">PlatyPS 具有用于 cmdlet 引用的硬编码架构，并且已写入代码中。</span><span class="sxs-lookup"><span data-stu-id="d74f9-110">PlatyPS has a hard-coded schema for cmdlet reference that is written into the code.</span></span> <span data-ttu-id="d74f9-111">[platyPS.schema.md][] 文档尝试描述此结构。</span><span class="sxs-lookup"><span data-stu-id="d74f9-111">The [platyPS.schema.md][] document attempts to describe this structure.</span></span> <span data-ttu-id="d74f9-112">架构冲突会导致生成错误，必须先修复这些错误然后才能接受你撰写的内容。</span><span class="sxs-lookup"><span data-stu-id="d74f9-112">Schema violations cause build errors that must be fixed before we can accept your contribution.</span></span>

## <a name="general-guidelines"></a><span data-ttu-id="d74f9-113">一般性指导</span><span class="sxs-lookup"><span data-stu-id="d74f9-113">General guidelines</span></span>

- <span data-ttu-id="d74f9-114">请勿删除任何标头结构。</span><span class="sxs-lookup"><span data-stu-id="d74f9-114">Do not remove any of the header structures.</span></span> <span data-ttu-id="d74f9-115">PlatyPS 需要一组特定的标头。</span><span class="sxs-lookup"><span data-stu-id="d74f9-115">PlatyPS expects a specific set of headers.</span></span>
- <span data-ttu-id="d74f9-116">输入类型和输出类型标头必须具有类型   。</span><span class="sxs-lookup"><span data-stu-id="d74f9-116">The **Input type** and **Output type** headers must have a type.</span></span> <span data-ttu-id="d74f9-117">如果 cmdlet 不接受输入或不返回值，则使用“None”值。</span><span class="sxs-lookup"><span data-stu-id="d74f9-117">If the cmdlet does not take input or return a value then use the value "None".</span></span>
- <span data-ttu-id="d74f9-118">仅[示例](#format-for-examples)部分允许使用隔离代码块。</span><span class="sxs-lookup"><span data-stu-id="d74f9-118">Fenced code blocks are only allowed in the [Examples](#format-for-examples) section.</span></span>
- <span data-ttu-id="d74f9-119">任何段落都可使用内联代码范围。</span><span class="sxs-lookup"><span data-stu-id="d74f9-119">Inline code spans can be used in any paragraph.</span></span>

## <a name="formatting-about_-files"></a><span data-ttu-id="d74f9-120">设置 About_ 文件的格式</span><span class="sxs-lookup"><span data-stu-id="d74f9-120">Formatting About_ files</span></span>

<span data-ttu-id="d74f9-121">`About_*` 文件现由 [Pandoc][] 处理，而不是 PlatyPS。</span><span class="sxs-lookup"><span data-stu-id="d74f9-121">`About_*` files are now processed by [Pandoc][], instead of PlatyPS.</span></span> <span data-ttu-id="d74f9-122">`About_*` 文件的格式设置使其在所有版本的 PowerShell 和发布工具中具有最佳兼容性。</span><span class="sxs-lookup"><span data-stu-id="d74f9-122">`About_*` files are formatted for the best compatibility across with all versions of PowerShell and with the publishing tools.</span></span>
<span data-ttu-id="d74f9-123">如果未以存储库维护人员的身份签入，请勿更改 `about_*` 文件的格式。</span><span class="sxs-lookup"><span data-stu-id="d74f9-123">Please do not alter the formatting of `about_*` files without checking in with a repository maintainer.</span></span>

<span data-ttu-id="d74f9-124">基本格式设置指南：</span><span class="sxs-lookup"><span data-stu-id="d74f9-124">Basic formatting guidelines:</span></span>

- <span data-ttu-id="d74f9-125">将行限制为 80 个字符</span><span class="sxs-lookup"><span data-stu-id="d74f9-125">Limit lines to 80 characters</span></span>
- <span data-ttu-id="d74f9-126">将代码块、块引号和表限制为 76 个字符，因为在转换过程中，Pandoc 会将这些内容缩进四个空格</span><span class="sxs-lookup"><span data-stu-id="d74f9-126">Code blocks, block quotes, and tables are limited to 76 characters because Pandoc indents these by four spaces during conversion</span></span>
- <span data-ttu-id="d74f9-127">表需要调整为 76 个字符以内</span><span class="sxs-lookup"><span data-stu-id="d74f9-127">Tables need fit within 76 characters</span></span>
  - <span data-ttu-id="d74f9-128">手动将单元格内容换到多行</span><span class="sxs-lookup"><span data-stu-id="d74f9-128">Manually wrap contents of cells across multiple lines</span></span>
  - <span data-ttu-id="d74f9-129">在每一行上使用开始和结束 `|` 字符</span><span class="sxs-lookup"><span data-stu-id="d74f9-129">Use opening and closing `|` characters on each line</span></span>
  - <span data-ttu-id="d74f9-130">请参阅 [about_Comparison_Operators][about-example] 中的工作示例</span><span class="sxs-lookup"><span data-stu-id="d74f9-130">See a working example in [about_Comparison_Operators][about-example]</span></span>
- <span data-ttu-id="d74f9-131">使用 Pandoc 的特殊字符 `\`、`$`、`` ` `` 和 `<`</span><span class="sxs-lookup"><span data-stu-id="d74f9-131">When using Pandoc's special characters `\`,`$`,`` ` ``, and `<`</span></span>
  - <span data-ttu-id="d74f9-132">在标头中 - 必须使用前导 `\` 字符对这些字符进行转义</span><span class="sxs-lookup"><span data-stu-id="d74f9-132">Within a header - these characters must be escaped using a leading `\` character</span></span>
  - <span data-ttu-id="d74f9-133">在段落中 - 应将这些字符放入代码范围中。</span><span class="sxs-lookup"><span data-stu-id="d74f9-133">Within a paragraph - these characters should be put into code spans.</span></span> <span data-ttu-id="d74f9-134">例如：</span><span class="sxs-lookup"><span data-stu-id="d74f9-134">For example:</span></span>

    ~~~markdown
    ### The purpose of the \$foo variable

    The `$foo` variable is used to store ...
    ~~~

## <a name="format-for-examples"></a><span data-ttu-id="d74f9-135">示例的格式</span><span class="sxs-lookup"><span data-stu-id="d74f9-135">Format for examples</span></span>

<span data-ttu-id="d74f9-136">在 PlatyPS 架构中，EXAMPLES 标头是 H2 标头，每个示例都是 H3 标头  。</span><span class="sxs-lookup"><span data-stu-id="d74f9-136">In the PlatyPS schema, the **EXAMPLES** header is an H2 header and each example is an H3 header.</span></span>

<span data-ttu-id="d74f9-137">在示例中，架构不允许按段落分隔代码块。</span><span class="sxs-lookup"><span data-stu-id="d74f9-137">Within an example, the schema does not allow code blocks to be separated by paragraphs.</span></span> <span data-ttu-id="d74f9-138">有效的架构为：</span><span class="sxs-lookup"><span data-stu-id="d74f9-138">The valid schema is:</span></span>

```
### Example #X title

0 or more paragraphs
1 or more code blocks
0 or more paragraphs.
```

<span data-ttu-id="d74f9-139">为每个示例编号并添加简短标题。</span><span class="sxs-lookup"><span data-stu-id="d74f9-139">Number each example and add a brief title.</span></span>

<span data-ttu-id="d74f9-140">例如：</span><span class="sxs-lookup"><span data-stu-id="d74f9-140">For example:</span></span>

~~~markdown
### Example 1: Get cmdlets, functions, and aliases

This example gets the PowerShell cmdlets, functions, and aliases that are installed on the
computer.

```powershell
Get-Command
```
~~~


[PlatyPS]: https://github.com/powershell/platyps
[platyPS.schema.md]: https://github.com/PowerShell/platyPS/blob/master/platyPS.schema.md
[issue1806]: https://github.com/PowerShell/PowerShell-Docs/issues/1806
[about-example]: https://github.com/MicrosoftDocs/PowerShell-Docs/blob/staging/reference/6/Microsoft.PowerShell.Core/About/about_Comparison_Operators.md
[Pandoc]: https://pandoc.org