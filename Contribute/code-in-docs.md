---
title: 如何在文档中包含代码
description: 了解如何在发布到 docs.microsoft.com 的文章中包含代码元素和代码段。
author: tdykstra
ms.author: tdykstra
ms.date: 03/03/2020
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.custom: external-contributor-guide
ms.openlocfilehash: 4aa34196f59a69651dd19add35a0351dd9b5d59b
ms.sourcegitcommit: dbc2c48194e29bfa0c88d33f50f94b9ee26be2da
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/05/2020
ms.locfileid: "78336472"
---
# <a name="how-to-include-code-in-docs"></a><span data-ttu-id="f8634-103">如何在文档中包含代码</span><span class="sxs-lookup"><span data-stu-id="f8634-103">How to include code in docs</span></span>

<span data-ttu-id="f8634-104">可以通过以下几种方法在发布到 docs.microsoft.com 的文章中包含代码：</span><span class="sxs-lookup"><span data-stu-id="f8634-104">There are several ways to include code in an article published on docs.microsoft.com:</span></span>

* <span data-ttu-id="f8634-105">一行中的单个元素（单词）。</span><span class="sxs-lookup"><span data-stu-id="f8634-105">Individual elements (words) within a line.</span></span>

  <span data-ttu-id="f8634-106">以下是 `code` 样式的示例。</span><span class="sxs-lookup"><span data-stu-id="f8634-106">Here's an example of `code` style.</span></span>

  <span data-ttu-id="f8634-107">在文本中引用附近代码块中的命名参数和变量时，使用代码格式。</span><span class="sxs-lookup"><span data-stu-id="f8634-107">Use code format when referring to named parameters and variables in a nearby code block in your text.</span></span> <span data-ttu-id="f8634-108">代码格式也可用于属性、方法、类和语言关键字。</span><span class="sxs-lookup"><span data-stu-id="f8634-108">Code format may also be used for properties, methods, classes, and language keywords.</span></span> <span data-ttu-id="f8634-109">有关详细信息，请参阅本文后面的[代码元素](#code-elements)。</span><span class="sxs-lookup"><span data-stu-id="f8634-109">For more information, see [Code elements](#code-elements) later in this article..</span></span>

* <span data-ttu-id="f8634-110">文章 Markdown 文件中的代码块。</span><span class="sxs-lookup"><span data-stu-id="f8634-110">Code blocks in the article Markdown file.</span></span>

  ```markdown
      ```csharp
      public static void Log(string message)
      {
          _logger.LogInformation(message);
      }
      ```
  ```

  <span data-ttu-id="f8634-111">不能通过引用代码文件来显示代码时，使用内联代码块。</span><span class="sxs-lookup"><span data-stu-id="f8634-111">Use inline code blocks when it's impractical to display code by reference to a code file.</span></span> <span data-ttu-id="f8634-112">有关详细信息，请参阅本文后面的[代码块](#inline-code-blocks)。</span><span class="sxs-lookup"><span data-stu-id="f8634-112">For more information, see [Code blocks](#inline-code-blocks) later in this article.</span></span>

* <span data-ttu-id="f8634-113">通过引用本地存储库中的代码文件的代码块。</span><span class="sxs-lookup"><span data-stu-id="f8634-113">Code blocks by reference to a code file in the local repository.</span></span>

  ```markdown
  :::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" range="2-24,26":::
  ```

  <span data-ttu-id="f8634-114">有关详细信息，请参阅本文后面的[存储库内的片段引用](#in-repo-snippet-references)。</span><span class="sxs-lookup"><span data-stu-id="f8634-114">For more information, see [In-repo snippet references](#in-repo-snippet-references) later in this article.</span></span>

* <span data-ttu-id="f8634-115">通过引用另一存储库中的代码文件的代码块。</span><span class="sxs-lookup"><span data-stu-id="f8634-115">Code blocks by reference to a code file in another repository.</span></span>

  ```markdown
  :::code language="csharp" source="~/samples-durable-functions/samples/csx/shared/Location.csx" highlight="2,5":::
  ```
  
  <span data-ttu-id="f8634-116">有关详细信息，请参阅本文后面的[存储库外的片段引用](#out-of-repo-snippet-references)。</span><span class="sxs-lookup"><span data-stu-id="f8634-116">For more information, see [Out-of-repo snippet references](#out-of-repo-snippet-references) later in this article.</span></span>
  
* <span data-ttu-id="f8634-117">允许用户在浏览器中执行代码的代码块。</span><span class="sxs-lookup"><span data-stu-id="f8634-117">Code blocks that let the user execute code in the browser.</span></span>

   ```markdown
  :::code source="PowerShell.ps1" interactive="cloudshell-powershell":::
  ```

  <span data-ttu-id="f8634-118">有关详细信息，请参阅本文后面的[交互式代码片段](#interactive-code-snippets)。</span><span class="sxs-lookup"><span data-stu-id="f8634-118">For more information, see [Interactive code snippets](#interactive-code-snippets) later in this article.</span></span>

<span data-ttu-id="f8634-119">除了解释包含代码的每种方法的 Markdown 之外，本文还提供了一些[适用于所有代码块的一般指南](#code-blocks)。</span><span class="sxs-lookup"><span data-stu-id="f8634-119">Besides explaining the Markdown for each of these ways to include code, the article provides some [general guidance for all code blocks](#code-blocks).</span></span>

## <a name="code-elements"></a><span data-ttu-id="f8634-120">代码元素</span><span class="sxs-lookup"><span data-stu-id="f8634-120">Code elements</span></span>

<span data-ttu-id="f8634-121">“代码元素”指的是编程语言关键字、类名、属性名称等。</span><span class="sxs-lookup"><span data-stu-id="f8634-121">A "code element" is a programming language keyword, class name, property name, and so forth.</span></span> <span data-ttu-id="f8634-122">什么内容可以称为代码，并不总是显而易见。</span><span class="sxs-lookup"><span data-stu-id="f8634-122">It's not always obvious what qualifies as code.</span></span> <span data-ttu-id="f8634-123">例如，NuGet 包名称应被视为代码。</span><span class="sxs-lookup"><span data-stu-id="f8634-123">For example, NuGet package names should be treated as code.</span></span> <span data-ttu-id="f8634-124">如有疑问，请参阅[文本格式设置准则](text-formatting-guidelines.md)。</span><span class="sxs-lookup"><span data-stu-id="f8634-124">When in doubt, see [Text formatting guidelines](text-formatting-guidelines.md).</span></span>

### <a name="inline-code-style"></a><span data-ttu-id="f8634-125">内联代码样式</span><span class="sxs-lookup"><span data-stu-id="f8634-125">Inline code style</span></span>

<span data-ttu-id="f8634-126">若要在文章文本中包含代码元素，请使用反斜线 (\`) 将其包住，表示代码样式。</span><span class="sxs-lookup"><span data-stu-id="f8634-126">To include a code element in article text, surround it with backticks (\`) to indicate code style.</span></span>
<span data-ttu-id="f8634-127">内联代码样式不得使用三个反引号格式。</span><span class="sxs-lookup"><span data-stu-id="f8634-127">Inline code style shouldn't use the triple-backtick format.</span></span>

|<span data-ttu-id="f8634-128">Markdown</span><span class="sxs-lookup"><span data-stu-id="f8634-128">Markdown</span></span> |<span data-ttu-id="f8634-129">呈现</span><span class="sxs-lookup"><span data-stu-id="f8634-129">Rendered</span></span> |
|---------|---------|
|<span data-ttu-id="f8634-130">默认情况下，实体框架将名为 \`Id\` 或 \`ClassnameID\` 的属性解释为主键。</span><span class="sxs-lookup"><span data-stu-id="f8634-130">By default, the Entity Framework interprets a property that's named \`Id\` or \`ClassnameID\` as the primary key.</span></span>|<span data-ttu-id="f8634-131">默认情况下，实体框架将名为 `Id` 或 `ClassnameID` 的属性解释为主键。</span><span class="sxs-lookup"><span data-stu-id="f8634-131">By default, the Entity Framework interprets a property that's named `Id` or `ClassnameID` as the primary key.</span></span>|

<span data-ttu-id="f8634-132">在本地化文章（翻译成其他语言）时，不会翻译代码样式的文本。</span><span class="sxs-lookup"><span data-stu-id="f8634-132">When an article is localized (translated into other languages), text styled as code is left untranslated.</span></span> <span data-ttu-id="f8634-133">如果要在不使用代码样式的情况下防止本地化，请参阅[非本地化字符串](markdown-reference.md#non-localized-strings)。</span><span class="sxs-lookup"><span data-stu-id="f8634-133">If you want to prevent localization without using code style, see [Non-localized strings](markdown-reference.md#non-localized-strings).</span></span>

### <a name="bold-style"></a><span data-ttu-id="f8634-134">粗体样式</span><span class="sxs-lookup"><span data-stu-id="f8634-134">Bold style</span></span>

<span data-ttu-id="f8634-135">一些较旧的风格指南为内联代码指定粗体格式。</span><span class="sxs-lookup"><span data-stu-id="f8634-135">Some older style guides specify bold for inline code.</span></span> <span data-ttu-id="f8634-136">当代码样式太过突兀以致于影响可读性时，可以选择使用粗体。</span><span class="sxs-lookup"><span data-stu-id="f8634-136">Bold is an option when code style is so obtrusive as to compromise readability.</span></span> <span data-ttu-id="f8634-137">例如，主要包含代码元素的 Markdown 表格如果全部应用代码样式，可能看起来杂乱。</span><span class="sxs-lookup"><span data-stu-id="f8634-137">For example, a Markdown table with mostly code elements might look too busy with code styling everywhere.</span></span> <span data-ttu-id="f8634-138">如果选择使用粗体样式，请使用[非本地化字符串语法](markdown-reference.md#non-localized-strings)以确保代码未本地化。</span><span class="sxs-lookup"><span data-stu-id="f8634-138">If you choose to use bold style, use [non-localized strings syntax](markdown-reference.md#non-localized-strings) to make sure that code is not localized.</span></span>

### <a name="links"></a><span data-ttu-id="f8634-139">链接</span><span class="sxs-lookup"><span data-stu-id="f8634-139">Links</span></span>

<span data-ttu-id="f8634-140">在某些上下文中，指向参考文档的链接可能比代码格式更有帮助。</span><span class="sxs-lookup"><span data-stu-id="f8634-140">A link to reference documentation may be more helpful than code format in some contexts.</span></span> <span data-ttu-id="f8634-141">如果使用链接，请勿将代码格式应用于链接文本。</span><span class="sxs-lookup"><span data-stu-id="f8634-141">If you use a link, don't apply code format to the link text.</span></span> <span data-ttu-id="f8634-142">将链接设置为代码会掩盖文本是链接的事实。</span><span class="sxs-lookup"><span data-stu-id="f8634-142">Styling a link as code can obscure the fact that the text is a link.</span></span>

<span data-ttu-id="f8634-143">如果使用链接，并且之后在相同的上下文中引用同一元素，请对后面的实例应用代码格式而非链接。</span><span class="sxs-lookup"><span data-stu-id="f8634-143">If you use a link and refer to the same element later in the same context, make the subsequent instances code format rather than links.</span></span>

### <a name="placeholders"></a><span data-ttu-id="f8634-144">占位符</span><span class="sxs-lookup"><span data-stu-id="f8634-144">Placeholders</span></span>

<span data-ttu-id="f8634-145">如果希望用户使用其自己的值替换一段显示的代码，请使用由尖括号或大括号标记的占位符文本。</span><span class="sxs-lookup"><span data-stu-id="f8634-145">If you want the user to replace a section of displayed code with their own values, use placeholder text marked off by angle brackets or curly braces.</span></span> <span data-ttu-id="f8634-146">例如：`az group delete -n <ResourceGroupName>`。</span><span class="sxs-lookup"><span data-stu-id="f8634-146">For example: `az group delete -n <ResourceGroupName>`.</span></span> <span data-ttu-id="f8634-147">说明在替换实值时必须删除尖括号或大括号。</span><span class="sxs-lookup"><span data-stu-id="f8634-147">Explain that the brackets or braces must be removed when substituting real values.</span></span>

## <a name="code-blocks"></a><span data-ttu-id="f8634-148">代码块</span><span class="sxs-lookup"><span data-stu-id="f8634-148">Code blocks</span></span>

<span data-ttu-id="f8634-149">用于将代码包含在文档中的语法取决于代码所在的位置：</span><span class="sxs-lookup"><span data-stu-id="f8634-149">The syntax for including code in a doc depends on where the code is located:</span></span>

* [<span data-ttu-id="f8634-150">在文章的 Markdown 文件中</span><span class="sxs-lookup"><span data-stu-id="f8634-150">In the article Markdown file</span></span>](#inline-code-blocks)
* [<span data-ttu-id="f8634-151">在同一个存储库的代码文件中</span><span class="sxs-lookup"><span data-stu-id="f8634-151">In a code file in the same repository</span></span>](#in-repo-snippet-references)
* [<span data-ttu-id="f8634-152">在不同存储库的代码文件中</span><span class="sxs-lookup"><span data-stu-id="f8634-152">In a code file in a different repository</span></span>](#out-of-repo-snippet-references)

<span data-ttu-id="f8634-153">下面是适用于所有三种类型代码块的指导原则：</span><span class="sxs-lookup"><span data-stu-id="f8634-153">Following are guidelines that apply to all three types of code blocks:</span></span>

* [<span data-ttu-id="f8634-154">自动执行代码验证。</span><span class="sxs-lookup"><span data-stu-id="f8634-154">Automate code validation.</span></span>](#code-validation)
* [<span data-ttu-id="f8634-155">突出显示关键代码行。</span><span class="sxs-lookup"><span data-stu-id="f8634-155">Highlight key lines of code.</span></span>](#highlighting)
* [<span data-ttu-id="f8634-156">避免水平滚动条。</span><span class="sxs-lookup"><span data-stu-id="f8634-156">Avoid horizontal scroll bars.</span></span>](#horizontal-scroll-bars)

### <a name="screenshots"></a><span data-ttu-id="f8634-157">屏幕截图</span><span class="sxs-lookup"><span data-stu-id="f8634-157">Screenshots</span></span>

<span data-ttu-id="f8634-158">上一部分中列出的所有方法均可生成可用的代码块：</span><span class="sxs-lookup"><span data-stu-id="f8634-158">All of the methods listed in the preceding section result in usable code blocks:</span></span>

* <span data-ttu-id="f8634-159">可从中进行复制和粘贴。</span><span class="sxs-lookup"><span data-stu-id="f8634-159">You can copy and paste from them.</span></span>
* <span data-ttu-id="f8634-160">可通过搜索引擎将其编入索引。</span><span class="sxs-lookup"><span data-stu-id="f8634-160">They're indexed by search engines.</span></span>
* <span data-ttu-id="f8634-161">屏幕阅读器可访问这些代码块。</span><span class="sxs-lookup"><span data-stu-id="f8634-161">They're accessible to screen readers.</span></span>

<span data-ttu-id="f8634-162">这只是建议不要将 IDE 屏幕截图作为在文章中包含代码的方法的一些原因。</span><span class="sxs-lookup"><span data-stu-id="f8634-162">These are just a few of the reasons why IDE screenshots aren't recommended as a method of including code in an article.</span></span> <span data-ttu-id="f8634-163">仅当显示 IDE 本身的相关信息（如 IntelliSense）时，才将 IDE 屏幕截图用于代码。</span><span class="sxs-lookup"><span data-stu-id="f8634-163">Use IDE screenshots for code only if you're showing something about the IDE itself, like IntelliSense.</span></span> <span data-ttu-id="f8634-164">请勿仅将屏幕截图用于显示着色和突出显示。</span><span class="sxs-lookup"><span data-stu-id="f8634-164">Don't use screenshots just to show colorization and highlighting.</span></span>

### <a name="code-validation"></a><span data-ttu-id="f8634-165">代码验证</span><span class="sxs-lookup"><span data-stu-id="f8634-165">Code validation</span></span>

<span data-ttu-id="f8634-166">一些存储库已经实现了自动编译所有示例代码以检查错误的过程。</span><span class="sxs-lookup"><span data-stu-id="f8634-166">Some repositories have implemented processes that automatically compile all sample code to check for errors.</span></span> <span data-ttu-id="f8634-167">.NET 存储库已实现此过程。</span><span class="sxs-lookup"><span data-stu-id="f8634-167">The .NET repository does this.</span></span> <span data-ttu-id="f8634-168">有关详细信息，请参阅 .NET 存储库中的[参与](https://github.com/dotnet/docs/blob/master/CONTRIBUTING.md)。</span><span class="sxs-lookup"><span data-stu-id="f8634-168">For more information, see [Contributing](https://github.com/dotnet/docs/blob/master/CONTRIBUTING.md) in the .NET repository.</span></span>

<span data-ttu-id="f8634-169">如果要包含其他存储库中的代码块，请与所有者共同制定代码维护策略，以便在提供代码使用的新版本的库时，你包含的代码不会中断或过期。</span><span class="sxs-lookup"><span data-stu-id="f8634-169">If you are including code blocks from another repository, work with the owners on a maintenance strategy for the code so that your included code does not break or go out of date as new versions of the libraries the code uses are shipped.</span></span>

### <a name="highlighting"></a><span data-ttu-id="f8634-170">突出显示</span><span class="sxs-lookup"><span data-stu-id="f8634-170">Highlighting</span></span>

<span data-ttu-id="f8634-171">代码段通常包含提供上下文所需的更多代码。</span><span class="sxs-lookup"><span data-stu-id="f8634-171">Snippets typically include more code than necessary in order to provide context.</span></span> <span data-ttu-id="f8634-172">在代码段中突出显示所关注的关键行时，它有助于提高可读性，如本例所示：</span><span class="sxs-lookup"><span data-stu-id="f8634-172">It helps readability when you highlight the key lines that you're focusing on in the snippet, as in this example:</span></span>

![突出显示的代码示例](media/code-in-docs/highlighted-code.png)

<span data-ttu-id="f8634-174">将代码包含在文章的 Markdown 文件中时，将无法突出显示代码。</span><span class="sxs-lookup"><span data-stu-id="f8634-174">You can't highlight code when you include it in the article Markdown file.</span></span> <span data-ttu-id="f8634-175">它只适用于通过引用代码文件包含的代码段。</span><span class="sxs-lookup"><span data-stu-id="f8634-175">It works only for code snippets included by reference to a code file.</span></span>

### <a name="horizontal-scroll-bars"></a><span data-ttu-id="f8634-176">水平滚动条</span><span class="sxs-lookup"><span data-stu-id="f8634-176">Horizontal scroll bars</span></span>

<span data-ttu-id="f8634-177">分解较长的行，以避免水平滚动条。</span><span class="sxs-lookup"><span data-stu-id="f8634-177">Break up long lines to avoid horizontal scroll bars.</span></span> <span data-ttu-id="f8634-178">代码块上的滚动条为阅读代码带来困难。</span><span class="sxs-lookup"><span data-stu-id="f8634-178">Scroll bars on code blocks make code hard to read.</span></span> <span data-ttu-id="f8634-179">在更长的代码块上尤其会出现此问题，在其中可能无法看到滚动条和同时想要读取的行。</span><span class="sxs-lookup"><span data-stu-id="f8634-179">They're especially problematic on longer code blocks, where it may be impossible to see the scroll bar and the line you want to read at the same time.</span></span>

<span data-ttu-id="f8634-180">要尽量使代码块上的水平滚动条保持最小，一种很好的做法是分解超过 85 个字符的代码行。</span><span class="sxs-lookup"><span data-stu-id="f8634-180">A good practice for minimizing horizontal scroll bars on code blocks is to break up code lines longer than 85 characters.</span></span> <span data-ttu-id="f8634-181">但请记住，滚动条存在与否不是衡量可读性的唯一标准。</span><span class="sxs-lookup"><span data-stu-id="f8634-181">But keep in mind that the presence or absence of a scroll bar isn't the only criterion of readability.</span></span> <span data-ttu-id="f8634-182">如果在不到 85 个字符时换行，会影响可读性或复制粘贴的便捷性，因此请随意超过 85 个字符。</span><span class="sxs-lookup"><span data-stu-id="f8634-182">If breaking a line before 85 hurts readability or copy-paste convenience, feel free to go over 85.</span></span>

## <a name="inline-code-blocks"></a><span data-ttu-id="f8634-183">内联代码块</span><span class="sxs-lookup"><span data-stu-id="f8634-183">Inline code blocks</span></span>

<span data-ttu-id="f8634-184">仅当不能通过引用代码文件来显示代码时，才使用内联代码块。</span><span class="sxs-lookup"><span data-stu-id="f8634-184">Use inline code blocks only when it's impractical to display code by reference to a code file.</span></span> <span data-ttu-id="f8634-185">与代码文件（完整项目的一部分）相比，内联代码通常更难测试且更难保持最新。</span><span class="sxs-lookup"><span data-stu-id="f8634-185">Inline code is generally more difficult to test and keep up to date compared to a code file that is part of a complete project.</span></span>  <span data-ttu-id="f8634-186">并且内联代码可能忽略可帮助开发人员理解和使用代码的上下文。</span><span class="sxs-lookup"><span data-stu-id="f8634-186">And inline code may omit context that could help the developer to understand and use the code.</span></span> <span data-ttu-id="f8634-187">这些注意事项主要适用于编程语言。</span><span class="sxs-lookup"><span data-stu-id="f8634-187">These considerations apply mainly to programming languages.</span></span> <span data-ttu-id="f8634-188">内联代码块还可用于输出和输入（如 JSON）、查询语言（如 SQL）和脚本语言（如 PowerShell）。</span><span class="sxs-lookup"><span data-stu-id="f8634-188">Inline code blocks can also be used for outputs and inputs (such as JSON), query languages (such as SQL), and scripting languages (such as PowerShell).</span></span>
  
<span data-ttu-id="f8634-189">可以通过以下两种方法在文章文件中指出文本的一部分是一个代码块：使用三个反斜杠 (\`\`\`) 将其隔开  或缩进。</span><span class="sxs-lookup"><span data-stu-id="f8634-189">There are two ways to indicate a section of text in an article file is a code block: by *fencing* it in triple-backticks (\`\`\`) or by indenting it.</span></span> <span data-ttu-id="f8634-190">隔离是首选方法，因为它允许指定语言。</span><span class="sxs-lookup"><span data-stu-id="f8634-190">Fencing is preferred because it lets you specify the language.</span></span> <span data-ttu-id="f8634-191">避免使用缩进，因为这样极易出错，并且当其他编写者需要编辑你的文章时，可能很难理解你的意图。</span><span class="sxs-lookup"><span data-stu-id="f8634-191">Avoid using indentation because it's too easy to get wrong and it may be hard for another writer to understand your intent when they need to edit your article.</span></span>

<span data-ttu-id="f8634-192">语言指示紧跟开头的三个反斜杠后，如以下示例所示：</span><span class="sxs-lookup"><span data-stu-id="f8634-192">Language indicators are placed immediately after the opening triple-backticks, as in the following example:</span></span>

<span data-ttu-id="f8634-193">Markdown：</span><span class="sxs-lookup"><span data-stu-id="f8634-193">Markdown:</span></span>

```markdown
    ```json
    {
        "aggregator": {
            "batchSize": 1000,
            "flushTimeout": "00:00:30"
        }
    }
    ```
```

<span data-ttu-id="f8634-194">呈现：</span><span class="sxs-lookup"><span data-stu-id="f8634-194">Rendered:</span></span>

```json
{
    "aggregator": {
        "batchSize": 1000,
        "flushTimeout": "00:00:30"
    }
}
```

<span data-ttu-id="f8634-195">有关可以用作语言指示的值的信息，请参阅[语言名称和别名](http://highlightjs.readthedocs.io/en/latest/css-classes-reference.html#language-names-and-aliases)。</span><span class="sxs-lookup"><span data-stu-id="f8634-195">For information about the values you can use as language indicators, see [Language names and aliases](http://highlightjs.readthedocs.io/en/latest/css-classes-reference.html#language-names-and-aliases).</span></span>

<span data-ttu-id="f8634-196">如果在三个反引号 (\`\`\`) 后面使用不受支持的语言或环境单词，该单词会显示在呈现页面上的代码部分标题栏中。</span><span class="sxs-lookup"><span data-stu-id="f8634-196">If you use a language or environment word after the triple-backticks (\`\`\`) that isn't supported, that word appears in the code section title bar on the rendered page.</span></span> <span data-ttu-id="f8634-197">请尽量在内联代码块中使用语言或环境指示。</span><span class="sxs-lookup"><span data-stu-id="f8634-197">Whenever possible, use a language or environment indicator in your inline code blocks.</span></span>

> [!NOTE]
> <span data-ttu-id="f8634-198">如果复制粘贴 Word 文档中的代码，请确保它没有对代码无效的“弯引号”（如 `“` 和 `’`）。</span><span class="sxs-lookup"><span data-stu-id="f8634-198">If you copy and paste code from a Word document, make sure it has no "curly quotes," which aren't valid in code (for example, `“` and `’`).</span></span> <span data-ttu-id="f8634-199">如果有，请将其改为常规引号（`'` 和 `"`）。</span><span class="sxs-lookup"><span data-stu-id="f8634-199">If it does, change them back to normal quotes (`'` and `"`).</span></span> <span data-ttu-id="f8634-200">或者，使用 Docs 创作包 - [智能引号替换功能](docs-authoring/smart-quote-replacement.md)。</span><span class="sxs-lookup"><span data-stu-id="f8634-200">Alternatively, rely on the Docs Authoring Pack, [smart quotes replacement feature](docs-authoring/smart-quote-replacement.md).</span></span>

## <a name="in-repo-snippet-references"></a><span data-ttu-id="f8634-201">存储库内的代码段引用</span><span class="sxs-lookup"><span data-stu-id="f8634-201">In-repo snippet references</span></span>

<span data-ttu-id="f8634-202">要在文档中包含用于编程语言的代码片段，首选方法是引用代码文件。</span><span class="sxs-lookup"><span data-stu-id="f8634-202">The preferred way to include code snippets for programming languages in docs is by reference to a code file.</span></span> <span data-ttu-id="f8634-203">借助此方法，你可以突出显示几行代码，并在 GitHub 上提供更广泛的代码片段上下文供开发人员使用。</span><span class="sxs-lookup"><span data-stu-id="f8634-203">This method gives you the ability to highlight lines of code and makes the wider context of the snippet available on GitHub for developers to use.</span></span> <span data-ttu-id="f8634-204">可手动使用三冒号格式 (:\:\:) 或在 Visual Studio Code 中借助 [docs.microsoft.com 创作包](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack)来包含代码。</span><span class="sxs-lookup"><span data-stu-id="f8634-204">You can include code by using the triple colon format (:\:\:) either manually or in Visual Studio Code with the help of the [docs.microsoft.com Authoring Pack](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack).</span></span>

1. <span data-ttu-id="f8634-205">在 Visual Studio Code 中，单击 Alt + M 或 Option + M，再选择“片段”<kbd></kbd><kbd></kbd>。</span><span class="sxs-lookup"><span data-stu-id="f8634-205">In Visual Studio Code, click <kbd>Alt + M</kbd> or <kbd>Option + M</kbd> and select Snippet.</span></span>
2. <span data-ttu-id="f8634-206">选择片段后，系统将提示你进行完全搜索、范围搜索或跨存储库引用。</span><span class="sxs-lookup"><span data-stu-id="f8634-206">Once Snippet is selected, you will be prompted for Full Search, Scoped Search or Cross-Repository Reference.</span></span> <span data-ttu-id="f8634-207">要在本地搜索，请选择“完整搜索”。</span><span class="sxs-lookup"><span data-stu-id="f8634-207">To search locally, select Full Search.</span></span>
3. <span data-ttu-id="f8634-208">要查找文件，请输入搜索词。</span><span class="sxs-lookup"><span data-stu-id="f8634-208">Enter a search term to find the file.</span></span> <span data-ttu-id="f8634-209">找到文件后，将其选中。</span><span class="sxs-lookup"><span data-stu-id="f8634-209">Once you've found the file, select the file.</span></span>
4. <span data-ttu-id="f8634-210">接下来，选择一个选项来确定应在片段中包含哪些代码行。</span><span class="sxs-lookup"><span data-stu-id="f8634-210">Next, select an option to determine which line(s) of code should be included in the snippet.</span></span> <span data-ttu-id="f8634-211">选项包括：“ID”、“范围”和“无”    。</span><span class="sxs-lookup"><span data-stu-id="f8634-211">The options are: **ID**, **Range** and **None**.</span></span>
5. <span data-ttu-id="f8634-212">根据在步骤 4 中选择的设置，必要时提供一个值。</span><span class="sxs-lookup"><span data-stu-id="f8634-212">Based on your selection from Step 4, provide a value if necessary.</span></span>

<span data-ttu-id="f8634-213">显示整个代码文件：</span><span class="sxs-lookup"><span data-stu-id="f8634-213">Display entire code file:</span></span>

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs":::
```

<span data-ttu-id="f8634-214">通过指定行号来显示代码文件的一部分：</span><span class="sxs-lookup"><span data-stu-id="f8634-214">Display part of a code file by specifying line numbers:</span></span>

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" range="2-24,26":::
```

<span data-ttu-id="f8634-215">通过指定一个代码段名称来显示代码文件的一部分：</span><span class="sxs-lookup"><span data-stu-id="f8634-215">Display part of a code file by specifying a snippet name:</span></span>

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" id="snippet_Create":::
```

<span data-ttu-id="f8634-216">以下部分说明了这些示例：</span><span class="sxs-lookup"><span data-stu-id="f8634-216">The following sections explain these examples:</span></span>

* [<span data-ttu-id="f8634-217">使用代码文件的相对路径</span><span class="sxs-lookup"><span data-stu-id="f8634-217">Use a relative path to the code file</span></span>](#path-to-code-file)
* [<span data-ttu-id="f8634-218">只包括选定行号</span><span class="sxs-lookup"><span data-stu-id="f8634-218">Include only selected line numbers</span></span>](#selected-line-numbers)
* [<span data-ttu-id="f8634-219">参考命名的代码段</span><span class="sxs-lookup"><span data-stu-id="f8634-219">Refer to a named snippet</span></span>](#named-snippet)
* [<span data-ttu-id="f8634-220">突出显示选定行</span><span class="sxs-lookup"><span data-stu-id="f8634-220">Highlight selected lines</span></span>](#highlighting-selected-lines)

<span data-ttu-id="f8634-221">有关详细信息，请查看本文后面的[片段语法引用](#snippet-syntax-reference)。</span><span class="sxs-lookup"><span data-stu-id="f8634-221">For more information, see [Snippet syntax reference](#snippet-syntax-reference) later in this article.</span></span>

### <a name="path-to-code-file"></a><span data-ttu-id="f8634-222">代码文件路径</span><span class="sxs-lookup"><span data-stu-id="f8634-222">Path to code file</span></span>

<span data-ttu-id="f8634-223">示例：</span><span class="sxs-lookup"><span data-stu-id="f8634-223">Example:</span></span>

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" range="2-24,26":::
```

<span data-ttu-id="f8634-224">本示例摘自 ASP.NET 文档存储库，[aspnetcore/data/ef-mvc/crud.md](https://github.com/aspnet/Docs/blob/master/aspnetcore/data/ef-mvc/crud.md) 文章文件。</span><span class="sxs-lookup"><span data-stu-id="f8634-224">The example is from the ASP.NET docs repo, [aspnetcore/data/ef-mvc/crud.md](https://github.com/aspnet/Docs/blob/master/aspnetcore/data/ef-mvc/crud.md) article file.</span></span> <span data-ttu-id="f8634-225">此代码文件通过同一存储库中的 [aspnetcore/data/ef-mvc/intro/samples/cu/Controllers/StudentsController.cs](https://github.com/aspnet/Docs/blob/master/aspnetcore/data/ef-mvc/intro/samples/cu/Controllers/StudentsController.cs) 相对路径进行引用。</span><span class="sxs-lookup"><span data-stu-id="f8634-225">The code file is referenced by a relative path to [aspnetcore/data/ef-mvc/intro/samples/cu/Controllers/StudentsController.cs](https://github.com/aspnet/Docs/blob/master/aspnetcore/data/ef-mvc/intro/samples/cu/Controllers/StudentsController.cs) in the same repository.</span></span>

### <a name="selected-line-numbers"></a><span data-ttu-id="f8634-226">选定行号</span><span class="sxs-lookup"><span data-stu-id="f8634-226">Selected line numbers</span></span>

<span data-ttu-id="f8634-227">示例：</span><span class="sxs-lookup"><span data-stu-id="f8634-227">Example:</span></span>

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" range="2-24,26":::
```

<span data-ttu-id="f8634-228">此示例仅显示了 StudentController.cs 代码文件中的第 2-24 行和第 26 行  。</span><span class="sxs-lookup"><span data-stu-id="f8634-228">This example displays only lines 2-24 and 26 of the *StudentController.cs* code file.</span></span>

<span data-ttu-id="f8634-229">更倾向于命名的代码片段而不是硬编码的行号，如下一部分所述。</span><span class="sxs-lookup"><span data-stu-id="f8634-229">Prefer named snippets over hard-coded line numbers, as explained in the next section.</span></span>

### <a name="named-snippet"></a><span data-ttu-id="f8634-230">命名的代码段</span><span class="sxs-lookup"><span data-stu-id="f8634-230">Named snippet</span></span>

<span data-ttu-id="f8634-231">示例：</span><span class="sxs-lookup"><span data-stu-id="f8634-231">Example:</span></span>

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" id="snippet_Create":::
```

<span data-ttu-id="f8634-232">仅在名称中使用字母和下划线。</span><span class="sxs-lookup"><span data-stu-id="f8634-232">Use only letters and underscores for the name.</span></span>

<span data-ttu-id="f8634-233">本示例显示代码文件的 `snippet_Create` 部分。</span><span class="sxs-lookup"><span data-stu-id="f8634-233">The example displays the `snippet_Create` section of the code file.</span></span> <span data-ttu-id="f8634-234">本示例的代码文件在 C# 代码中注释中带有代码片段标记：</span><span class="sxs-lookup"><span data-stu-id="f8634-234">The code file for this example has snippet tags in comments in the C# code:</span></span>

```cs
// code excluded from the snippet
// <snippet_Create>
// code included in the snippet
// </snippet_Create>
// code excluded from the snippet
```

<span data-ttu-id="f8634-235">在可能的情况下，请参考命名的部分，而不是指定行号。</span><span class="sxs-lookup"><span data-stu-id="f8634-235">Whenever you can, refer to a named section rather than specifying line numbers.</span></span> <span data-ttu-id="f8634-236">行号引用不太稳妥，因为在更改行号时，代码文件不可避免地会发生更改。</span><span class="sxs-lookup"><span data-stu-id="f8634-236">Line number references are brittle because code files inevitably change in ways that make line numbers change.</span></span>
<span data-ttu-id="f8634-237">不一定会收到此类更改的通知。</span><span class="sxs-lookup"><span data-stu-id="f8634-237">You don't necessarily get notified of such changes.</span></span> <span data-ttu-id="f8634-238">最终，文章开始显示错误行，并且你完全不知道发生的任何变更。</span><span class="sxs-lookup"><span data-stu-id="f8634-238">Your article eventually starts showing the wrong lines and you have no clue anything has changed.</span></span>

### <a name="highlighting-selected-lines"></a><span data-ttu-id="f8634-239">突出显示选定行</span><span class="sxs-lookup"><span data-stu-id="f8634-239">Highlighting selected lines</span></span>

<span data-ttu-id="f8634-240">示例：</span><span class="sxs-lookup"><span data-stu-id="f8634-240">Example:</span></span>

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" range="2-24,26" highlight="2,5":::
```

<span data-ttu-id="f8634-241">本示例突出显示第 2 行和第 5 行，从显示的代码段开头开始计数。</span><span class="sxs-lookup"><span data-stu-id="f8634-241">The example highlights lines 2 and 5, counting from the start of the displayed snippet.</span></span> <span data-ttu-id="f8634-242">要突出显示的行号并不从代码文件的开头开始计数。</span><span class="sxs-lookup"><span data-stu-id="f8634-242">Line numbers to highlight don't count from the start of the code file.</span></span> <span data-ttu-id="f8634-243">也就是说，代码文件的第 3 行和第 6 行会突出显示。</span><span class="sxs-lookup"><span data-stu-id="f8634-243">In other words, lines 3 and 6 of the code file are highlighted.</span></span>

## <a name="out-of-repo-snippet-references"></a><span data-ttu-id="f8634-244">存储库外的代码段引用</span><span class="sxs-lookup"><span data-stu-id="f8634-244">Out-of-repo snippet references</span></span>

<span data-ttu-id="f8634-245">如果要引用的代码文件在另一个存储库中，请将代码储存库设置为“从属存储库”  。</span><span class="sxs-lookup"><span data-stu-id="f8634-245">If the code file you want to reference is in a different repository, set up the code repository as a *dependent repository*.</span></span> <span data-ttu-id="f8634-246">在执行此操作时，请为它指定一个名称。</span><span class="sxs-lookup"><span data-stu-id="f8634-246">When you do that, you specify a name for it.</span></span> <span data-ttu-id="f8634-247">然后，该名称会作为一个文件夹名称用于代码引用。</span><span class="sxs-lookup"><span data-stu-id="f8634-247">That name then acts like a folder name for purposes of code references.</span></span>

<span data-ttu-id="f8634-248">例如，文档存储库是 Azure/azure-docs  ，代码存储库是 Azure/azure-functions-durable-extension  。</span><span class="sxs-lookup"><span data-stu-id="f8634-248">For example, the docs repository is *Azure/azure-docs*, and the code repository is *Azure/azure-functions-durable-extension*.</span></span>

<span data-ttu-id="f8634-249">在 azure-docs  的根文件夹中，在 .openpublishing.publish.config.json  中添加以下部分：</span><span class="sxs-lookup"><span data-stu-id="f8634-249">In the root folder of *azure-docs*, add the following section in *.openpublishing.publish.config.json*:</span></span>

```json
    {
      "path_to_root": "samples-durable-functions",
      "url": "https://github.com/Azure/azure-functions-durable-extension",
      "branch": "master",
      "branch_mapping": {}
    },
```

<span data-ttu-id="f8634-250">现在，当你引用 sample-durable-functions（如同它是 azure-docs 中的一个文件夹）时，你实际上引用的是 azure-functions-durable-extension 存储库中的根文件夹    。</span><span class="sxs-lookup"><span data-stu-id="f8634-250">Now when you refer to *samples-durable-functions* as if it were a folder in *azure-docs*, you're actually referring to the root folder in the *azure-functions-durable-extension* repository.</span></span>

<span data-ttu-id="f8634-251">可手动使用三冒号格式 (:\:\:) 或在 Visual Studio Code 中借助 [docs.microsoft.com 创作包](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack)来包含代码。</span><span class="sxs-lookup"><span data-stu-id="f8634-251">You can include code by using the triple colon format (:\:\:) either manually or in Visual Studio Code with the help of the [docs.microsoft.com Authoring Pack](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack).</span></span>

1. <span data-ttu-id="f8634-252">在 Visual Studio Code 中，单击 Alt + M 或 Option + M，再选择“片段”<kbd></kbd><kbd></kbd>。</span><span class="sxs-lookup"><span data-stu-id="f8634-252">In Visual Studio Code, click <kbd>Alt + M</kbd> or <kbd>Option + M</kbd> and select Snippet.</span></span>
2. <span data-ttu-id="f8634-253">选择片段后，系统将提示你进行完全搜索、范围搜索或跨存储库引用。</span><span class="sxs-lookup"><span data-stu-id="f8634-253">Once Snippet is selected, you will be prompted for Full Search, Scoped Search or Cross-Repository Reference.</span></span> <span data-ttu-id="f8634-254">要跨存储库进行搜索，请选择“跨存储库引用”。</span><span class="sxs-lookup"><span data-stu-id="f8634-254">To search across repositories, select Cross-Repository Reference.</span></span>
3. <span data-ttu-id="f8634-255">将显示 .openpublishing.publish.config.json 中的存储库供你选择  。</span><span class="sxs-lookup"><span data-stu-id="f8634-255">You will be given a selection of repositories that are in *.openpublishing.publish.config.json*.</span></span> <span data-ttu-id="f8634-256">选择存储库。</span><span class="sxs-lookup"><span data-stu-id="f8634-256">Select a repository.</span></span>
4. <span data-ttu-id="f8634-257">要查找文件，请输入搜索词。</span><span class="sxs-lookup"><span data-stu-id="f8634-257">Enter a search term to find the file.</span></span> <span data-ttu-id="f8634-258">找到文件后，将其选中。</span><span class="sxs-lookup"><span data-stu-id="f8634-258">Once you've found the file, select the file.</span></span>
5. <span data-ttu-id="f8634-259">接下来，选择一个选项来确定应在片段中包含哪些代码行。</span><span class="sxs-lookup"><span data-stu-id="f8634-259">Next, select an option to determine which line(s) of code should be included in the snippet.</span></span> <span data-ttu-id="f8634-260">选项包括：“ID”、“范围”和“无”    。</span><span class="sxs-lookup"><span data-stu-id="f8634-260">The options are: **ID**, **Range** and **None**.</span></span>
6. <span data-ttu-id="f8634-261">根据在步骤 5 中选择的设置，提供一个值。</span><span class="sxs-lookup"><span data-stu-id="f8634-261">Based on your selection from Step 5, provide a value.</span></span>

<span data-ttu-id="f8634-262">你的片段引用将如下所示：</span><span class="sxs-lookup"><span data-stu-id="f8634-262">Your snippet reference will look like this:</span></span>

```markdown
:::code language="csharp" source="~/samples-durable-functions/samples/csx/shared/Location.csx" highlight="2,5":::
```

<span data-ttu-id="f8634-263">在 azure-functions-durable-extension  存储库中，该代码文件位于 samples/csx/shared  文件夹中。</span><span class="sxs-lookup"><span data-stu-id="f8634-263">In the *azure-functions-durable-extension* repository, that code file is in the *samples/csx/shared* folder.</span></span> <span data-ttu-id="f8634-264">[如前](#highlighting-selected-lines)所述，突出显示的行号对应于代码片段的开头而非文件的开头。</span><span class="sxs-lookup"><span data-stu-id="f8634-264">As noted [earlier](#highlighting-selected-lines), line numbers for highlighting are relative to the start of the snippet rather than the start of the file.</span></span>

> [!NOTE]
> <span data-ttu-id="f8634-265">分配给从属存储库的名称对应于主存储库的根目录，但波形符 (~) 是指文档集的根目录。</span><span class="sxs-lookup"><span data-stu-id="f8634-265">The name you assign to the dependent repository is relative to the root of the main repository, but the tilde (~) refers to the root of the doc set.</span></span> <span data-ttu-id="f8634-266">文档集根目录由 .openpublishing.publish.config.json 中的 `build_source_folder` 确定  。</span><span class="sxs-lookup"><span data-stu-id="f8634-266">The doc set root is determined by `build_source_folder` in *.openpublishing.publish.config.json*.</span></span> <span data-ttu-id="f8634-267">上一示例中代码片段的路径可在 azure-docs 存储库中使用，因为 `build_source_folder` 指的是存储库根目录 (`.`)。</span><span class="sxs-lookup"><span data-stu-id="f8634-267">The path to the snippet in the preceding example works in the azure-docs repo because `build_source_folder` refers to the repo root (`.`).</span></span> <span data-ttu-id="f8634-268">如果 `build_source_folder` 为 `articles`，则路径将以 `~/../samples-durable-functions` 而非 `~/samples-durable-functions` 开头。</span><span class="sxs-lookup"><span data-stu-id="f8634-268">If `build_source_folder` were `articles`, the path would start with `~/../samples-durable-functions` instead of `~/samples-durable-functions`.</span></span>

## <a name="interactive-code-snippets"></a><span data-ttu-id="f8634-269">交互式代码片段</span><span class="sxs-lookup"><span data-stu-id="f8634-269">Interactive code snippets</span></span>

### <a name="inline-interactive-code-blocks"></a><span data-ttu-id="f8634-270">内联交互式代码块</span><span class="sxs-lookup"><span data-stu-id="f8634-270">Inline interactive code blocks</span></span>

<span data-ttu-id="f8634-271">对于以下语言，可以在浏览器窗口中执行代码段：</span><span class="sxs-lookup"><span data-stu-id="f8634-271">For the following languages, code snippets can be made executable in the browser window:</span></span>

* <span data-ttu-id="f8634-272">Azure Cloud Shell</span><span class="sxs-lookup"><span data-stu-id="f8634-272">Azure Cloud Shell</span></span>
* <span data-ttu-id="f8634-273">Azure PowerShell Cloud Shell</span><span class="sxs-lookup"><span data-stu-id="f8634-273">Azure PowerShell Cloud Shell</span></span>
* <span data-ttu-id="f8634-274">C# REPL</span><span class="sxs-lookup"><span data-stu-id="f8634-274">C# REPL</span></span>

<span data-ttu-id="f8634-275">启用交互模式后，呈现的代码框会出现“尝试”  或“运行”  按钮。</span><span class="sxs-lookup"><span data-stu-id="f8634-275">When interactive mode is enabled, the rendered code boxes have a **Try It** or **Run** button.</span></span> <span data-ttu-id="f8634-276">例如：</span><span class="sxs-lookup"><span data-stu-id="f8634-276">For example:</span></span>

```markdown
    ```azurepowershell-interactive
    New-AzResourceGroup -Name myResourceGroup -Location westeurope
    ```
```

<span data-ttu-id="f8634-277">呈现为：</span><span class="sxs-lookup"><span data-stu-id="f8634-277">renders as follows:</span></span>

```azurepowershell-interactive
New-AzResourceGroup -Name myResourceGroup -Location westeurope
```

<span data-ttu-id="f8634-278">要为特定代码块启用此功能，请使用特殊的语言标识符。</span><span class="sxs-lookup"><span data-stu-id="f8634-278">To turn on this feature for a particular code block, use a special language identifier.</span></span> <span data-ttu-id="f8634-279">可用选项包括：</span><span class="sxs-lookup"><span data-stu-id="f8634-279">The available options are:</span></span>

* <span data-ttu-id="f8634-280">`azurepowershell-interactive` - 启用 Azure PowerShell Cloud Shell，如前例所示</span><span class="sxs-lookup"><span data-stu-id="f8634-280">`azurepowershell-interactive` - Enables the Azure PowerShell Cloud Shell, as in the preceding example</span></span>
* <span data-ttu-id="f8634-281">`azurecli-interactive` - 启用 Azure Cloud Shell</span><span class="sxs-lookup"><span data-stu-id="f8634-281">`azurecli-interactive` - Enables the Azure Cloud Shell</span></span>
* <span data-ttu-id="f8634-282">`csharp-interactive` - 启用 C# REPL</span><span class="sxs-lookup"><span data-stu-id="f8634-282">`csharp-interactive` - Enables the C# REPL</span></span>

<span data-ttu-id="f8634-283">对于 Azure Cloud Shell 和 PowerShell Cloud Shell，用户可以只针对自己的 Azure 帐户运行命令。</span><span class="sxs-lookup"><span data-stu-id="f8634-283">For the Azure Cloud Shell and PowerShell Cloud Shell, users can run commands against only their own Azure account.</span></span>

### <a name="code-snippets-included-by-reference"></a><span data-ttu-id="f8634-284">通过引用包含的代码片段</span><span class="sxs-lookup"><span data-stu-id="f8634-284">Code snippets included by reference</span></span>

<span data-ttu-id="f8634-285">可以为通过引用包含的代码段启用交互模式。</span><span class="sxs-lookup"><span data-stu-id="f8634-285">You can enable interactive mode for code snippets included by reference.</span></span> <span data-ttu-id="f8634-286">示例如下：</span><span class="sxs-lookup"><span data-stu-id="f8634-286">Here are examples:</span></span>

```markdown
:::code source="PowerShell.ps1" interactive="cloudshell-powershell":::
```

```markdown
:::code source="Bash.sh" interactive="cloudshell-bash":::
```

<span data-ttu-id="f8634-287">要为特定代码块启用此功能，请使用 `interactive` 属性。</span><span class="sxs-lookup"><span data-stu-id="f8634-287">To turn on this feature for a particular code block, use the `interactive` attribute.</span></span> <span data-ttu-id="f8634-288">可用的属性值如下：</span><span class="sxs-lookup"><span data-stu-id="f8634-288">The available attribute values are:</span></span>

* <span data-ttu-id="f8634-289">`cloudshell-powershell` - 启用 Azure PowerShell Cloud Shell，如前例所示</span><span class="sxs-lookup"><span data-stu-id="f8634-289">`cloudshell-powershell` - Enables the Azure PowerShell Cloud Shell, as in the preceding example</span></span>
* <span data-ttu-id="f8634-290">`cloudshell-bash` - 启用 Azure Cloud Shell</span><span class="sxs-lookup"><span data-stu-id="f8634-290">`cloudshell-bash` - Enables the Azure Cloud Shell</span></span>
* <span data-ttu-id="f8634-291">`try-dotnet` - 启用 Try .NET</span><span class="sxs-lookup"><span data-stu-id="f8634-291">`try-dotnet` - Enables Try .NET</span></span>
* <span data-ttu-id="f8634-292">`try-dotnet-class` - 使用类基架启用 Try .NET</span><span class="sxs-lookup"><span data-stu-id="f8634-292">`try-dotnet-class` - Enables Try .NET with class scaffolding</span></span>
* <span data-ttu-id="f8634-293">`try-dotnet-method` - 使用方法基架启用 Try .NET</span><span class="sxs-lookup"><span data-stu-id="f8634-293">`try-dotnet-method` - Enables Try .NET with method scaffolding</span></span>

<span data-ttu-id="f8634-294">对于 Azure Cloud Shell 和 PowerShell Cloud Shell，用户只能针对自己的 Azure 帐户运行命令。</span><span class="sxs-lookup"><span data-stu-id="f8634-294">For the Azure Cloud Shell and PowerShell Cloud Shell, users can only run commands against their own Azure account.</span></span>

## <a name="snippet-syntax-reference"></a><span data-ttu-id="f8634-295">片段语法引用</span><span class="sxs-lookup"><span data-stu-id="f8634-295">Snippet syntax reference</span></span>

<span data-ttu-id="f8634-296">语法：</span><span class="sxs-lookup"><span data-stu-id="f8634-296">Syntax:</span></span>

```md
:::code language="<language>" source="<path>" <attribute>="<attribute-value>":::
```

> [!IMPORTANT]
> <span data-ttu-id="f8634-297">此语法是块 Markdown 扩展。</span><span class="sxs-lookup"><span data-stu-id="f8634-297">This syntax is a block Markdown extension.</span></span> <span data-ttu-id="f8634-298">必须在自己的行中使用它。</span><span class="sxs-lookup"><span data-stu-id="f8634-298">It must be used on its own line.</span></span>

* <span data-ttu-id="f8634-299">`<language>`（可选） </span><span class="sxs-lookup"><span data-stu-id="f8634-299">`<language>` (*optional*)</span></span>
  * <span data-ttu-id="f8634-300">代码片段的语言。</span><span class="sxs-lookup"><span data-stu-id="f8634-300">Language of the code snippet.</span></span> <span data-ttu-id="f8634-301">有关详细信息，请参阅本文后面的[支持的语言](#supported-languages)部分。</span><span class="sxs-lookup"><span data-stu-id="f8634-301">For more information, see the [Supported languages](#supported-languages) section later in this article.</span></span>

* <span data-ttu-id="f8634-302">`<path>`（必需） </span><span class="sxs-lookup"><span data-stu-id="f8634-302">`<path>` (*mandatory*)</span></span>
  * <span data-ttu-id="f8634-303">文件系统中的相对路径，指示将引用的代码片段文件。</span><span class="sxs-lookup"><span data-stu-id="f8634-303">Relative path in the file system that indicates the code snippet file to reference.</span></span>

* <span data-ttu-id="f8634-304">`<attribute>` 和 `<attribute-value>`（可选） </span><span class="sxs-lookup"><span data-stu-id="f8634-304">`<attribute>` and `<attribute-value>` (*optional*)</span></span>
  * <span data-ttu-id="f8634-305">配合使用以指定如何从文件中检索代码以及如何显示代码：</span><span class="sxs-lookup"><span data-stu-id="f8634-305">Used together to specify how the code should be retrieved from the file and how it should be displayed:</span></span>
    * <span data-ttu-id="f8634-306">`range`：`1,3-5` 行的范围。</span><span class="sxs-lookup"><span data-stu-id="f8634-306">`range`: `1,3-5` A range of lines.</span></span> <span data-ttu-id="f8634-307">此示例包含第 1、3、4 和 5 行。</span><span class="sxs-lookup"><span data-stu-id="f8634-307">This example includes lines 1, 3, 4, and 5.</span></span>
    * <span data-ttu-id="f8634-308">`id`：`snippet_Create`：需要从代码文件中插入的片段的 ID。</span><span class="sxs-lookup"><span data-stu-id="f8634-308">`id`: `snippet_Create` The ID of the snippet that needs to be inserted from the code file.</span></span> <span data-ttu-id="f8634-309">该值不能与范围共存。</span><span class="sxs-lookup"><span data-stu-id="f8634-309">This value cannot co-exist with range.</span></span>
    * <span data-ttu-id="f8634-310">`highlight`：`2-4,6`：需要在生成的代码片段中突出显示的范围和/或行数。</span><span class="sxs-lookup"><span data-stu-id="f8634-310">`highlight`: `2-4,6` Range and/or numbers of lines that need to be highlighted in the generated code snippet.</span></span> <span data-ttu-id="f8634-311">该编号对应于显示的行数（由范围或 ID 指定）而非文件。</span><span class="sxs-lookup"><span data-stu-id="f8634-311">The numbering is relative to the lines displayed (as specified by range or id), not the file.</span></span>
    * <span data-ttu-id="f8634-312">`interactive`：`cloudshell-powershell`、`cloudshell-bash`、`try-dotnet`、`try-dotnet-class`、`try-dotnet-method` 字符串值确定启用了哪些类型的交互。</span><span class="sxs-lookup"><span data-stu-id="f8634-312">`interactive`: `cloudshell-powershell`, `cloudshell-bash`, `try-dotnet`, `try-dotnet-class`, `try-dotnet-method` String value determines what kinds of interactivity are enabled.</span></span>
    * <span data-ttu-id="f8634-313">有关按语言在代码片段源文件中呈现标记名称的详细信息，请参阅 [DocFX 准则](https://dotnet.github.io/docfx/spec/docfx_flavored_markdown.html#tag-name-representation-in-code-snippet-source-file)。</span><span class="sxs-lookup"><span data-stu-id="f8634-313">For details about tag name representation in code snippet source files by language, see the [DocFX guidelines](https://dotnet.github.io/docfx/spec/docfx_flavored_markdown.html#tag-name-representation-in-code-snippet-source-file).</span></span>

## <a name="supported-languages"></a><span data-ttu-id="f8634-314">支持的语言</span><span class="sxs-lookup"><span data-stu-id="f8634-314">Supported languages</span></span>

<span data-ttu-id="f8634-315">[Docs 创作包](how-to-write-docs-auth-pack.md)包含一项功能，可对代码隔离块的可用语言标识符提供语句完成和验证功能。</span><span class="sxs-lookup"><span data-stu-id="f8634-315">The [Docs Authoring Pack](how-to-write-docs-auth-pack.md) includes a feature to provide statement completion and validation of the available language identifiers for code fence blocks.</span></span>

### <a name="fenced-code-blocks"></a><span data-ttu-id="f8634-316">隔离代码块</span><span class="sxs-lookup"><span data-stu-id="f8634-316">Fenced code blocks</span></span>

| <span data-ttu-id="f8634-317">名称</span><span class="sxs-lookup"><span data-stu-id="f8634-317">Name</span></span>                           | <span data-ttu-id="f8634-318">有效别名</span><span class="sxs-lookup"><span data-stu-id="f8634-318">Valid aliases</span></span>                                                                  |
|--------------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="f8634-319">.NET Core CLI</span><span class="sxs-lookup"><span data-stu-id="f8634-319">.NET Core CLI</span></span>                  | `dotnetcli`                                                                    |
| <span data-ttu-id="f8634-320">1C</span><span class="sxs-lookup"><span data-stu-id="f8634-320">1C</span></span>                             | `1c`                                                                           |
| <span data-ttu-id="f8634-321">ABNF</span><span class="sxs-lookup"><span data-stu-id="f8634-321">ABNF</span></span>                           | `abnf`                                                                         |
| <span data-ttu-id="f8634-322">Access logs</span><span class="sxs-lookup"><span data-stu-id="f8634-322">Access logs</span></span>                    | `accesslog`                                                                    |
| <span data-ttu-id="f8634-323">Ada</span><span class="sxs-lookup"><span data-stu-id="f8634-323">Ada</span></span>                            | `ada`                                                                          |
| <span data-ttu-id="f8634-324">ARM assembler</span><span class="sxs-lookup"><span data-stu-id="f8634-324">ARM assembler</span></span>                  | <span data-ttu-id="f8634-325">`armasm`、`arm`</span><span class="sxs-lookup"><span data-stu-id="f8634-325">`armasm`, `arm`</span></span>                                                                |
| <span data-ttu-id="f8634-326">AVR assembler</span><span class="sxs-lookup"><span data-stu-id="f8634-326">AVR assembler</span></span>                  | `avrasm`                                                                       |
| <span data-ttu-id="f8634-327">ActionScript</span><span class="sxs-lookup"><span data-stu-id="f8634-327">ActionScript</span></span>                   | <span data-ttu-id="f8634-328">`actionscript`、`as`</span><span class="sxs-lookup"><span data-stu-id="f8634-328">`actionscript`, `as`</span></span>                                                           |
| <span data-ttu-id="f8634-329">Alan</span><span class="sxs-lookup"><span data-stu-id="f8634-329">Alan</span></span>                           | <span data-ttu-id="f8634-330">`alan`、`i`</span><span class="sxs-lookup"><span data-stu-id="f8634-330">`alan`, `i`</span></span>                                                                    |
| <span data-ttu-id="f8634-331">AngelScript</span><span class="sxs-lookup"><span data-stu-id="f8634-331">AngelScript</span></span>                    | <span data-ttu-id="f8634-332">`angelscript`、`asc`</span><span class="sxs-lookup"><span data-stu-id="f8634-332">`angelscript`, `asc`</span></span>                                                           |
| <span data-ttu-id="f8634-333">ANTLR</span><span class="sxs-lookup"><span data-stu-id="f8634-333">ANTLR</span></span>                          | `antlr`                                                                        |
| <span data-ttu-id="f8634-334">Apache</span><span class="sxs-lookup"><span data-stu-id="f8634-334">Apache</span></span>                         | <span data-ttu-id="f8634-335">`apache`、`apacheconf`</span><span class="sxs-lookup"><span data-stu-id="f8634-335">`apache`, `apacheconf`</span></span>                                                         |
| <span data-ttu-id="f8634-336">AppleScript</span><span class="sxs-lookup"><span data-stu-id="f8634-336">AppleScript</span></span>                    | <span data-ttu-id="f8634-337">`applescript`、`osascript`</span><span class="sxs-lookup"><span data-stu-id="f8634-337">`applescript`, `osascript`</span></span>                                                     |
| <span data-ttu-id="f8634-338">Arcade</span><span class="sxs-lookup"><span data-stu-id="f8634-338">Arcade</span></span>                         | `arcade`                                                                       |
| <span data-ttu-id="f8634-339">AsciiDoc</span><span class="sxs-lookup"><span data-stu-id="f8634-339">AsciiDoc</span></span>                       | <span data-ttu-id="f8634-340">`asciidoc`、`adoc`</span><span class="sxs-lookup"><span data-stu-id="f8634-340">`asciidoc`, `adoc`</span></span>                                                             |
| <span data-ttu-id="f8634-341">AspectJ</span><span class="sxs-lookup"><span data-stu-id="f8634-341">AspectJ</span></span>                        | `aspectj`                                                                      |
| <span data-ttu-id="f8634-342">ASPX</span><span class="sxs-lookup"><span data-stu-id="f8634-342">ASPX</span></span>                           | `aspx`                                                                         |
| <span data-ttu-id="f8634-343">ASP.NET (C#)</span><span class="sxs-lookup"><span data-stu-id="f8634-343">ASP.NET (C#)</span></span>                   | `aspx-csharp`                                                                  |
| <span data-ttu-id="f8634-344">ASP.NET (VB)</span><span class="sxs-lookup"><span data-stu-id="f8634-344">ASP.NET (VB)</span></span>                   | `aspx-vb`                                                                      |
| <span data-ttu-id="f8634-345">AutoHotkey</span><span class="sxs-lookup"><span data-stu-id="f8634-345">AutoHotkey</span></span>                     | `autohotkey`                                                                   |
| <span data-ttu-id="f8634-346">AutoIt</span><span class="sxs-lookup"><span data-stu-id="f8634-346">AutoIt</span></span>                         | `autoit`                                                                       |
| <span data-ttu-id="f8634-347">Awk</span><span class="sxs-lookup"><span data-stu-id="f8634-347">Awk</span></span>                            | <span data-ttu-id="f8634-348">`awk`、`mawk`、`nawk`、`gawk`</span><span class="sxs-lookup"><span data-stu-id="f8634-348">`awk`, `mawk`, `nawk`, `gawk`</span></span>                                                  |
| <span data-ttu-id="f8634-349">Axapta</span><span class="sxs-lookup"><span data-stu-id="f8634-349">Axapta</span></span>                         | `axapta`                                                                       |
| <span data-ttu-id="f8634-350">AzCopy</span><span class="sxs-lookup"><span data-stu-id="f8634-350">AzCopy</span></span>                         | `azcopy`                                                                       |
| <span data-ttu-id="f8634-351">Azure CLI</span><span class="sxs-lookup"><span data-stu-id="f8634-351">Azure CLI</span></span>                      | `azurecli`                                                                     |
| <span data-ttu-id="f8634-352">Azure CLI (Interactive)</span><span class="sxs-lookup"><span data-stu-id="f8634-352">Azure CLI (Interactive)</span></span>        | `azurecli-interactive`                                                         |
| <span data-ttu-id="f8634-353">Azure Powershell</span><span class="sxs-lookup"><span data-stu-id="f8634-353">Azure Powershell</span></span>               | `azurepowershell`                                                              |
| <span data-ttu-id="f8634-354">Azure Powershell (Interactive)</span><span class="sxs-lookup"><span data-stu-id="f8634-354">Azure Powershell (Interactive)</span></span> | `azurepowershell-interactive`                                                  |
| <span data-ttu-id="f8634-355">Bash</span><span class="sxs-lookup"><span data-stu-id="f8634-355">Bash</span></span>                           | <span data-ttu-id="f8634-356">`bash`、`sh`、`zsh`</span><span class="sxs-lookup"><span data-stu-id="f8634-356">`bash`, `sh`, `zsh`</span></span>                                                            |
| <span data-ttu-id="f8634-357">Basic</span><span class="sxs-lookup"><span data-stu-id="f8634-357">Basic</span></span>                          | `basic`                                                                        |
| <span data-ttu-id="f8634-358">BNF</span><span class="sxs-lookup"><span data-stu-id="f8634-358">BNF</span></span>                            | `bnf`                                                                          |
| <span data-ttu-id="f8634-359">C</span><span class="sxs-lookup"><span data-stu-id="f8634-359">C</span></span>                              | `c`                                                                            |
| <span data-ttu-id="f8634-360">C#</span><span class="sxs-lookup"><span data-stu-id="f8634-360">C#</span></span>                             | <span data-ttu-id="f8634-361">`csharp`、`cs`</span><span class="sxs-lookup"><span data-stu-id="f8634-361">`csharp`, `cs`</span></span>                                                                 |
| <span data-ttu-id="f8634-362">C# (Interactive)</span><span class="sxs-lookup"><span data-stu-id="f8634-362">C# (Interactive)</span></span>               | `csharp-interactive`                                                           |
| <span data-ttu-id="f8634-363">C++</span><span class="sxs-lookup"><span data-stu-id="f8634-363">C++</span></span>                            | <span data-ttu-id="f8634-364">`cpp`、`c`、`cc`、`h`、`c++`、`h++`、`hpp`</span><span class="sxs-lookup"><span data-stu-id="f8634-364">`cpp`, `c`, `cc`, `h`, `c++`, `h++`, `hpp`</span></span>                                     |
| <span data-ttu-id="f8634-365">C++/CX</span><span class="sxs-lookup"><span data-stu-id="f8634-365">C++/CX</span></span>                         | `cppcx`                                                                        |
| <span data-ttu-id="f8634-366">C++/WinRT</span><span class="sxs-lookup"><span data-stu-id="f8634-366">C++/WinRT</span></span>                      | `cppwinrt`                                                                     |
| <span data-ttu-id="f8634-367">C/AL</span><span class="sxs-lookup"><span data-stu-id="f8634-367">C/AL</span></span>                           | `cal`                                                                          |
| <span data-ttu-id="f8634-368">Cache Object Script</span><span class="sxs-lookup"><span data-stu-id="f8634-368">Cache Object Script</span></span>            | <span data-ttu-id="f8634-369">`cos`、`cls`</span><span class="sxs-lookup"><span data-stu-id="f8634-369">`cos`, `cls`</span></span>                                                                   |
| <span data-ttu-id="f8634-370">CMake</span><span class="sxs-lookup"><span data-stu-id="f8634-370">CMake</span></span>                          | <span data-ttu-id="f8634-371">`cmake`、`cmake.in`</span><span class="sxs-lookup"><span data-stu-id="f8634-371">`cmake`, `cmake.in`</span></span>                                                            |
| <span data-ttu-id="f8634-372">Coq</span><span class="sxs-lookup"><span data-stu-id="f8634-372">Coq</span></span>                            | `coq`                                                                          |
| <span data-ttu-id="f8634-373">CSP</span><span class="sxs-lookup"><span data-stu-id="f8634-373">CSP</span></span>                            | `csp`                                                                          |
| <span data-ttu-id="f8634-374">CSS</span><span class="sxs-lookup"><span data-stu-id="f8634-374">CSS</span></span>                            | `css`                                                                          |
| <span data-ttu-id="f8634-375">Cap'n Proto</span><span class="sxs-lookup"><span data-stu-id="f8634-375">Cap'n Proto</span></span>                    | <span data-ttu-id="f8634-376">`capnproto`、`capnp`</span><span class="sxs-lookup"><span data-stu-id="f8634-376">`capnproto`, `capnp`</span></span>                                                           |
| <span data-ttu-id="f8634-377">Clojure</span><span class="sxs-lookup"><span data-stu-id="f8634-377">Clojure</span></span>                        | <span data-ttu-id="f8634-378">`clojure`、`clj`</span><span class="sxs-lookup"><span data-stu-id="f8634-378">`clojure`, `clj`</span></span>                                                               |
| <span data-ttu-id="f8634-379">CoffeeScript</span><span class="sxs-lookup"><span data-stu-id="f8634-379">CoffeeScript</span></span>                   | <span data-ttu-id="f8634-380">`coffeescript`、`coffee`、`cson`、`iced`</span><span class="sxs-lookup"><span data-stu-id="f8634-380">`coffeescript`, `coffee`, `cson`, `iced`</span></span>                                       |
| <span data-ttu-id="f8634-381">Crmsh</span><span class="sxs-lookup"><span data-stu-id="f8634-381">Crmsh</span></span>                          | <span data-ttu-id="f8634-382">`crmsh`、`crm`、`pcmk`</span><span class="sxs-lookup"><span data-stu-id="f8634-382">`crmsh`, `crm`, `pcmk`</span></span>                                                         |
| <span data-ttu-id="f8634-383">Crystal</span><span class="sxs-lookup"><span data-stu-id="f8634-383">Crystal</span></span>                        | <span data-ttu-id="f8634-384">`crystal`、`cr`</span><span class="sxs-lookup"><span data-stu-id="f8634-384">`crystal`, `cr`</span></span>                                                                |
| <span data-ttu-id="f8634-385">Cypher (Neo4j)</span><span class="sxs-lookup"><span data-stu-id="f8634-385">Cypher (Neo4j)</span></span>                 | `cypher`                                                                       |
| <span data-ttu-id="f8634-386">D</span><span class="sxs-lookup"><span data-stu-id="f8634-386">D</span></span>                              | `d`                                                                            |
| <span data-ttu-id="f8634-387">DAX Power BI</span><span class="sxs-lookup"><span data-stu-id="f8634-387">DAX Power BI</span></span>                   | `dax`                                                                          |
| <span data-ttu-id="f8634-388">DNS Zone file</span><span class="sxs-lookup"><span data-stu-id="f8634-388">DNS Zone file</span></span>                  | <span data-ttu-id="f8634-389">`dns`、`zone`、`bind`</span><span class="sxs-lookup"><span data-stu-id="f8634-389">`dns`, `zone`, `bind`</span></span>                                                          |
| <span data-ttu-id="f8634-390">DOS</span><span class="sxs-lookup"><span data-stu-id="f8634-390">DOS</span></span>                            | <span data-ttu-id="f8634-391">`dos`、`bat`、`cmd`</span><span class="sxs-lookup"><span data-stu-id="f8634-391">`dos`, `bat`, `cmd`</span></span>                                                            |
| <span data-ttu-id="f8634-392">Dart</span><span class="sxs-lookup"><span data-stu-id="f8634-392">Dart</span></span>                           | `dart`                                                                         |
| <span data-ttu-id="f8634-393">Delphi</span><span class="sxs-lookup"><span data-stu-id="f8634-393">Delphi</span></span>                         | <span data-ttu-id="f8634-394">`delphi`、`dpr`、`dfm`、`pas`、`pascal`、`freepascal`、`lazarus`、`lpr`、`lfm`</span><span class="sxs-lookup"><span data-stu-id="f8634-394">`delphi`, `dpr`, `dfm`, `pas`, `pascal`, `freepascal`, `lazarus`, `lpr`, `lfm`</span></span> |
| <span data-ttu-id="f8634-395">Diff</span><span class="sxs-lookup"><span data-stu-id="f8634-395">Diff</span></span>                           | <span data-ttu-id="f8634-396">`diff`、`patch`</span><span class="sxs-lookup"><span data-stu-id="f8634-396">`diff`, `patch`</span></span>                                                                |
| <span data-ttu-id="f8634-397">Django</span><span class="sxs-lookup"><span data-stu-id="f8634-397">Django</span></span>                         | <span data-ttu-id="f8634-398">`django`、`jinja`</span><span class="sxs-lookup"><span data-stu-id="f8634-398">`django`, `jinja`</span></span>                                                              |
| <span data-ttu-id="f8634-399">Dockerfile</span><span class="sxs-lookup"><span data-stu-id="f8634-399">Dockerfile</span></span>                     | <span data-ttu-id="f8634-400">`dockerfile`、`docker`</span><span class="sxs-lookup"><span data-stu-id="f8634-400">`dockerfile`, `docker`</span></span>                                                         |
| <span data-ttu-id="f8634-401">dsconfig</span><span class="sxs-lookup"><span data-stu-id="f8634-401">dsconfig</span></span>                       | `dsconfig`                                                                     |
| <span data-ttu-id="f8634-402">DTS (Device Tree)</span><span class="sxs-lookup"><span data-stu-id="f8634-402">DTS (Device Tree)</span></span>              | `dts`                                                                          |
| <span data-ttu-id="f8634-403">Dust</span><span class="sxs-lookup"><span data-stu-id="f8634-403">Dust</span></span>                           | <span data-ttu-id="f8634-404">`dust`、`dst`</span><span class="sxs-lookup"><span data-stu-id="f8634-404">`dust`, `dst`</span></span>                                                                  |
| <span data-ttu-id="f8634-405">Dylan</span><span class="sxs-lookup"><span data-stu-id="f8634-405">Dylan</span></span>                          | `dylan`                                                                        |
| <span data-ttu-id="f8634-406">EBNF</span><span class="sxs-lookup"><span data-stu-id="f8634-406">EBNF</span></span>                           | `ebnf`                                                                         |
| <span data-ttu-id="f8634-407">Elixir</span><span class="sxs-lookup"><span data-stu-id="f8634-407">Elixir</span></span>                         | `elixir`                                                                       |
| <span data-ttu-id="f8634-408">Elm</span><span class="sxs-lookup"><span data-stu-id="f8634-408">Elm</span></span>                            | `elm`                                                                          |
| <span data-ttu-id="f8634-409">Erlang</span><span class="sxs-lookup"><span data-stu-id="f8634-409">Erlang</span></span>                         | <span data-ttu-id="f8634-410">`erlang`、`erl`</span><span class="sxs-lookup"><span data-stu-id="f8634-410">`erlang`, `erl`</span></span>                                                                |
| <span data-ttu-id="f8634-411">Excel</span><span class="sxs-lookup"><span data-stu-id="f8634-411">Excel</span></span>                          | <span data-ttu-id="f8634-412">`excel`、`xls`、`xlsx`</span><span class="sxs-lookup"><span data-stu-id="f8634-412">`excel`, `xls`, `xlsx`</span></span>                                                         |
| <span data-ttu-id="f8634-413">Extempore</span><span class="sxs-lookup"><span data-stu-id="f8634-413">Extempore</span></span>                      | <span data-ttu-id="f8634-414">`extempore`、`xtlang`、`xtm`</span><span class="sxs-lookup"><span data-stu-id="f8634-414">`extempore`, `xtlang`, `xtm`</span></span>                                                   |
| <span data-ttu-id="f8634-415">F#</span><span class="sxs-lookup"><span data-stu-id="f8634-415">F#</span></span>                             | <span data-ttu-id="f8634-416">`fsharp`、`fs`</span><span class="sxs-lookup"><span data-stu-id="f8634-416">`fsharp`, `fs`</span></span>                                                                 |
| <span data-ttu-id="f8634-417">FIX</span><span class="sxs-lookup"><span data-stu-id="f8634-417">FIX</span></span>                            | `fix`                                                                          |
| <span data-ttu-id="f8634-418">Fortran</span><span class="sxs-lookup"><span data-stu-id="f8634-418">Fortran</span></span>                        | <span data-ttu-id="f8634-419">`fortran`、`f90`、`f95`</span><span class="sxs-lookup"><span data-stu-id="f8634-419">`fortran`, `f90`, `f95`</span></span>                                                        |
| <span data-ttu-id="f8634-420">G-Code</span><span class="sxs-lookup"><span data-stu-id="f8634-420">G-Code</span></span>                         | <span data-ttu-id="f8634-421">`gcode`、`nc`</span><span class="sxs-lookup"><span data-stu-id="f8634-421">`gcode`, `nc`</span></span>                                                                  |
| <span data-ttu-id="f8634-422">Gams</span><span class="sxs-lookup"><span data-stu-id="f8634-422">Gams</span></span>                           | <span data-ttu-id="f8634-423">`gams`、`gms`</span><span class="sxs-lookup"><span data-stu-id="f8634-423">`gams`, `gms`</span></span>                                                                  |
| <span data-ttu-id="f8634-424">GAUSS</span><span class="sxs-lookup"><span data-stu-id="f8634-424">GAUSS</span></span>                          | <span data-ttu-id="f8634-425">`gauss`、`gss`</span><span class="sxs-lookup"><span data-stu-id="f8634-425">`gauss`, `gss`</span></span>                                                                 |
| <span data-ttu-id="f8634-426">GDScript</span><span class="sxs-lookup"><span data-stu-id="f8634-426">GDScript</span></span>                       | <span data-ttu-id="f8634-427">`godot`、`gdscript`</span><span class="sxs-lookup"><span data-stu-id="f8634-427">`godot`, `gdscript`</span></span>                                                            |
| <span data-ttu-id="f8634-428">Gherkin</span><span class="sxs-lookup"><span data-stu-id="f8634-428">Gherkin</span></span>                        | `gherkin`                                                                      |
| <span data-ttu-id="f8634-429">GN for Ninja</span><span class="sxs-lookup"><span data-stu-id="f8634-429">GN for Ninja</span></span>                   | <span data-ttu-id="f8634-430">`gn`、`gni`</span><span class="sxs-lookup"><span data-stu-id="f8634-430">`gn`, `gni`</span></span>                                                                    |
| <span data-ttu-id="f8634-431">Go</span><span class="sxs-lookup"><span data-stu-id="f8634-431">Go</span></span>                             | <span data-ttu-id="f8634-432">`go`、`golang`</span><span class="sxs-lookup"><span data-stu-id="f8634-432">`go`, `golang`</span></span>                                                                 |
| <span data-ttu-id="f8634-433">Golo</span><span class="sxs-lookup"><span data-stu-id="f8634-433">Golo</span></span>                           | <span data-ttu-id="f8634-434">`golo`、`gololang`</span><span class="sxs-lookup"><span data-stu-id="f8634-434">`golo`, `gololang`</span></span>                                                             |
| <span data-ttu-id="f8634-435">Gradle</span><span class="sxs-lookup"><span data-stu-id="f8634-435">Gradle</span></span>                         | `gradle`                                                                       |
| <span data-ttu-id="f8634-436">Groovy</span><span class="sxs-lookup"><span data-stu-id="f8634-436">Groovy</span></span>                         | `groovy`                                                                       |
| <span data-ttu-id="f8634-437">HTML</span><span class="sxs-lookup"><span data-stu-id="f8634-437">HTML</span></span>                           | <span data-ttu-id="f8634-438">`html`、`xhtml`</span><span class="sxs-lookup"><span data-stu-id="f8634-438">`html`, `xhtml`</span></span>                                                                |
| <span data-ttu-id="f8634-439">HTTP</span><span class="sxs-lookup"><span data-stu-id="f8634-439">HTTP</span></span>                           | <span data-ttu-id="f8634-440">`http`、`https`</span><span class="sxs-lookup"><span data-stu-id="f8634-440">`http`, `https`</span></span>                                                                |
| <span data-ttu-id="f8634-441">Haml</span><span class="sxs-lookup"><span data-stu-id="f8634-441">Haml</span></span>                           | `haml`                                                                         |
| <span data-ttu-id="f8634-442">Handlebars</span><span class="sxs-lookup"><span data-stu-id="f8634-442">Handlebars</span></span>                     | <span data-ttu-id="f8634-443">`handlebars`、`hbs`、`html.hbs`、`html.handlebars`</span><span class="sxs-lookup"><span data-stu-id="f8634-443">`handlebars`, `hbs`, `html.hbs`, `html.handlebars`</span></span>                             |
| <span data-ttu-id="f8634-444">Haskell</span><span class="sxs-lookup"><span data-stu-id="f8634-444">Haskell</span></span>                        | <span data-ttu-id="f8634-445">`haskell`、`hs`</span><span class="sxs-lookup"><span data-stu-id="f8634-445">`haskell`, `hs`</span></span>                                                                |
| <span data-ttu-id="f8634-446">Haxe</span><span class="sxs-lookup"><span data-stu-id="f8634-446">Haxe</span></span>                           | <span data-ttu-id="f8634-447">`haxe`、`hx`</span><span class="sxs-lookup"><span data-stu-id="f8634-447">`haxe`, `hx`</span></span>                                                                   |
| <span data-ttu-id="f8634-448">Hy</span><span class="sxs-lookup"><span data-stu-id="f8634-448">Hy</span></span>                             | <span data-ttu-id="f8634-449">`hy`、`hylang`</span><span class="sxs-lookup"><span data-stu-id="f8634-449">`hy`, `hylang`</span></span>                                                                 |
| <span data-ttu-id="f8634-450">Ini</span><span class="sxs-lookup"><span data-stu-id="f8634-450">Ini</span></span>                            | `ini`                                                                          |
| <span data-ttu-id="f8634-451">Inform7</span><span class="sxs-lookup"><span data-stu-id="f8634-451">Inform7</span></span>                        | <span data-ttu-id="f8634-452">`inform7`、`i7`</span><span class="sxs-lookup"><span data-stu-id="f8634-452">`inform7`, `i7`</span></span>                                                                |
| <span data-ttu-id="f8634-453">IRPF90</span><span class="sxs-lookup"><span data-stu-id="f8634-453">IRPF90</span></span>                         | `irpf90`                                                                       |
| <span data-ttu-id="f8634-454">JSON</span><span class="sxs-lookup"><span data-stu-id="f8634-454">JSON</span></span>                           | `json`                                                                         |
| <span data-ttu-id="f8634-455">Java</span><span class="sxs-lookup"><span data-stu-id="f8634-455">Java</span></span>                           | <span data-ttu-id="f8634-456">`java`、`jsp`</span><span class="sxs-lookup"><span data-stu-id="f8634-456">`java`, `jsp`</span></span>                                                                  |
| <span data-ttu-id="f8634-457">JavaScript</span><span class="sxs-lookup"><span data-stu-id="f8634-457">JavaScript</span></span>                     | <span data-ttu-id="f8634-458">`javascript`、`js`、`jsx`</span><span class="sxs-lookup"><span data-stu-id="f8634-458">`javascript`, `js`, `jsx`</span></span>                                                      |
| <span data-ttu-id="f8634-459">Kotlin</span><span class="sxs-lookup"><span data-stu-id="f8634-459">Kotlin</span></span>                         | <span data-ttu-id="f8634-460">`kotlin`、`kt`</span><span class="sxs-lookup"><span data-stu-id="f8634-460">`kotlin`, `kt`</span></span>                                                                 |
| <span data-ttu-id="f8634-461">Kusto</span><span class="sxs-lookup"><span data-stu-id="f8634-461">Kusto</span></span>                          | `kusto`                                                                        |
| <span data-ttu-id="f8634-462">Leaf</span><span class="sxs-lookup"><span data-stu-id="f8634-462">Leaf</span></span>                           | `leaf`                                                                         |
| <span data-ttu-id="f8634-463">Lasso</span><span class="sxs-lookup"><span data-stu-id="f8634-463">Lasso</span></span>                          | <span data-ttu-id="f8634-464">`lasso`、`ls`、`lassoscript`</span><span class="sxs-lookup"><span data-stu-id="f8634-464">`lasso`, `ls`, `lassoscript`</span></span>                                                   |
| <span data-ttu-id="f8634-465">Less</span><span class="sxs-lookup"><span data-stu-id="f8634-465">Less</span></span>                           | `less`                                                                         |
| <span data-ttu-id="f8634-466">LDIF</span><span class="sxs-lookup"><span data-stu-id="f8634-466">LDIF</span></span>                           | `ldif`                                                                         |
| <span data-ttu-id="f8634-467">Lisp</span><span class="sxs-lookup"><span data-stu-id="f8634-467">Lisp</span></span>                           | `lisp`                                                                         |
| <span data-ttu-id="f8634-468">LiveCode Server</span><span class="sxs-lookup"><span data-stu-id="f8634-468">LiveCode Server</span></span>                | `livecodeserver`                                                               |
| <span data-ttu-id="f8634-469">LiveScript</span><span class="sxs-lookup"><span data-stu-id="f8634-469">LiveScript</span></span>                     | <span data-ttu-id="f8634-470">`livescript`、`ls`</span><span class="sxs-lookup"><span data-stu-id="f8634-470">`livescript`, `ls`</span></span>                                                             |
| <span data-ttu-id="f8634-471">Lua</span><span class="sxs-lookup"><span data-stu-id="f8634-471">Lua</span></span>                            | `lua`                                                                          |
| <span data-ttu-id="f8634-472">Makefile</span><span class="sxs-lookup"><span data-stu-id="f8634-472">Makefile</span></span>                       | <span data-ttu-id="f8634-473">`makefile`、`mk`、`mak`</span><span class="sxs-lookup"><span data-stu-id="f8634-473">`makefile`, `mk`, `mak`</span></span>                                                        |
| <span data-ttu-id="f8634-474">Markdown</span><span class="sxs-lookup"><span data-stu-id="f8634-474">Markdown</span></span>                       | <span data-ttu-id="f8634-475">`markdown`、`md`、`mkdown`、`mkd`</span><span class="sxs-lookup"><span data-stu-id="f8634-475">`markdown`, `md`, `mkdown`, `mkd`</span></span>                                              |
| <span data-ttu-id="f8634-476">Mathematica</span><span class="sxs-lookup"><span data-stu-id="f8634-476">Mathematica</span></span>                    | <span data-ttu-id="f8634-477">`mathematica`、`mma`、`wl`</span><span class="sxs-lookup"><span data-stu-id="f8634-477">`mathematica`, `mma`, `wl`</span></span>                                                     |
| <span data-ttu-id="f8634-478">Matlab</span><span class="sxs-lookup"><span data-stu-id="f8634-478">Matlab</span></span>                         | `matlab`                                                                       |
| <span data-ttu-id="f8634-479">Maxima</span><span class="sxs-lookup"><span data-stu-id="f8634-479">Maxima</span></span>                         | `maxima`                                                                       |
| <span data-ttu-id="f8634-480">Maya Embedded Language</span><span class="sxs-lookup"><span data-stu-id="f8634-480">Maya Embedded Language</span></span>         | `mel`                                                                          |
| <span data-ttu-id="f8634-481">Mercury</span><span class="sxs-lookup"><span data-stu-id="f8634-481">Mercury</span></span>                        | `mercury`                                                                      |
| <span data-ttu-id="f8634-482">mIRC Scripting Language</span><span class="sxs-lookup"><span data-stu-id="f8634-482">mIRC Scripting Language</span></span>        | <span data-ttu-id="f8634-483">`mirc`、`mrc`</span><span class="sxs-lookup"><span data-stu-id="f8634-483">`mirc`, `mrc`</span></span>                                                                  |
| <span data-ttu-id="f8634-484">Mizar</span><span class="sxs-lookup"><span data-stu-id="f8634-484">Mizar</span></span>                          | `mizar`                                                                        |
| <span data-ttu-id="f8634-485">托管对象格式</span><span class="sxs-lookup"><span data-stu-id="f8634-485">Managed Object Format</span></span>          | `mof`                                                                          |
| <span data-ttu-id="f8634-486">Mojolicious</span><span class="sxs-lookup"><span data-stu-id="f8634-486">Mojolicious</span></span>                    | `mojolicious`                                                                  |
| <span data-ttu-id="f8634-487">Monkey</span><span class="sxs-lookup"><span data-stu-id="f8634-487">Monkey</span></span>                         | `monkey`                                                                       |
| <span data-ttu-id="f8634-488">Moonscript</span><span class="sxs-lookup"><span data-stu-id="f8634-488">Moonscript</span></span>                     | <span data-ttu-id="f8634-489">`moonscript`、`moon`</span><span class="sxs-lookup"><span data-stu-id="f8634-489">`moonscript`, `moon`</span></span>                                                           |
| <span data-ttu-id="f8634-490">MS Graph (Interactive)</span><span class="sxs-lookup"><span data-stu-id="f8634-490">MS Graph (Interactive)</span></span>         | `msgraph-interactive`                                                          |
| <span data-ttu-id="f8634-491">N1QL</span><span class="sxs-lookup"><span data-stu-id="f8634-491">N1QL</span></span>                           | `n1ql`                                                                         |
| <span data-ttu-id="f8634-492">NSIS</span><span class="sxs-lookup"><span data-stu-id="f8634-492">NSIS</span></span>                           | `nsis`                                                                         |
| <span data-ttu-id="f8634-493">Nginx</span><span class="sxs-lookup"><span data-stu-id="f8634-493">Nginx</span></span>                          | <span data-ttu-id="f8634-494">`nginx`、`nginxconf`</span><span class="sxs-lookup"><span data-stu-id="f8634-494">`nginx`, `nginxconf`</span></span>                                                           |
| <span data-ttu-id="f8634-495">Nimrod</span><span class="sxs-lookup"><span data-stu-id="f8634-495">Nimrod</span></span>                         | <span data-ttu-id="f8634-496">`nimrod`、`nim`</span><span class="sxs-lookup"><span data-stu-id="f8634-496">`nimrod`, `nim`</span></span>                                                                |
| <span data-ttu-id="f8634-497">Nix</span><span class="sxs-lookup"><span data-stu-id="f8634-497">Nix</span></span>                            | `nix`                                                                          |
| <span data-ttu-id="f8634-498">OCaml</span><span class="sxs-lookup"><span data-stu-id="f8634-498">OCaml</span></span>                          | <span data-ttu-id="f8634-499">`ocaml`、`ml`</span><span class="sxs-lookup"><span data-stu-id="f8634-499">`ocaml`, `ml`</span></span>                                                                  |
| <span data-ttu-id="f8634-500">Objective C</span><span class="sxs-lookup"><span data-stu-id="f8634-500">Objective C</span></span>                    | <span data-ttu-id="f8634-501">`objectivec`、`mm`、`objc`、`obj-c`</span><span class="sxs-lookup"><span data-stu-id="f8634-501">`objectivec`, `mm`, `objc`, `obj-c`</span></span>                                            |
| <span data-ttu-id="f8634-502">OpenGL Shading Language</span><span class="sxs-lookup"><span data-stu-id="f8634-502">OpenGL Shading Language</span></span>        | `glsl`                                                                         |
| <span data-ttu-id="f8634-503">OpenSCAD</span><span class="sxs-lookup"><span data-stu-id="f8634-503">OpenSCAD</span></span>                       | <span data-ttu-id="f8634-504">`openscad`、`scad`</span><span class="sxs-lookup"><span data-stu-id="f8634-504">`openscad`, `scad`</span></span>                                                             |
| <span data-ttu-id="f8634-505">Oracle Rules Language</span><span class="sxs-lookup"><span data-stu-id="f8634-505">Oracle Rules Language</span></span>          | `ruleslanguage`                                                                |
| <span data-ttu-id="f8634-506">Oxygene</span><span class="sxs-lookup"><span data-stu-id="f8634-506">Oxygene</span></span>                        | `oxygene`                                                                      |
| <span data-ttu-id="f8634-507">PF</span><span class="sxs-lookup"><span data-stu-id="f8634-507">PF</span></span>                             | <span data-ttu-id="f8634-508">`pf`、`pf.conf`</span><span class="sxs-lookup"><span data-stu-id="f8634-508">`pf`, `pf.conf`</span></span>                                                                |
| <span data-ttu-id="f8634-509">PHP</span><span class="sxs-lookup"><span data-stu-id="f8634-509">PHP</span></span>                            | <span data-ttu-id="f8634-510">`php`、`php3`、`php4`、`php5`、`php6`</span><span class="sxs-lookup"><span data-stu-id="f8634-510">`php`, `php3`, `php4`, `php5`, `php6`</span></span>                                          |
| <span data-ttu-id="f8634-511">Parser3</span><span class="sxs-lookup"><span data-stu-id="f8634-511">Parser3</span></span>                        | `parser3`                                                                      |
| <span data-ttu-id="f8634-512">Perl</span><span class="sxs-lookup"><span data-stu-id="f8634-512">Perl</span></span>                           | <span data-ttu-id="f8634-513">`perl`、`pl`、`pm`</span><span class="sxs-lookup"><span data-stu-id="f8634-513">`perl`, `pl`, `pm`</span></span>                                                             |
| <span data-ttu-id="f8634-514">Plaintext no highlight</span><span class="sxs-lookup"><span data-stu-id="f8634-514">Plaintext no highlight</span></span>         | `plaintext`                                                                    |
| <span data-ttu-id="f8634-515">Pony</span><span class="sxs-lookup"><span data-stu-id="f8634-515">Pony</span></span>                           | `pony`                                                                         |
| <span data-ttu-id="f8634-516">PostgreSQL & PL/pgSQL</span><span class="sxs-lookup"><span data-stu-id="f8634-516">PostgreSQL & PL/pgSQL</span></span>          | <span data-ttu-id="f8634-517">`pgsql`、`postgres`、`postgresql`</span><span class="sxs-lookup"><span data-stu-id="f8634-517">`pgsql`, `postgres`, `postgresql`</span></span>                                              |
| <span data-ttu-id="f8634-518">PowerShell</span><span class="sxs-lookup"><span data-stu-id="f8634-518">PowerShell</span></span>                     | <span data-ttu-id="f8634-519">`powershell`、`ps`</span><span class="sxs-lookup"><span data-stu-id="f8634-519">`powershell`, `ps`</span></span>                                                             |
| <span data-ttu-id="f8634-520">PowerShell (Interactive)</span><span class="sxs-lookup"><span data-stu-id="f8634-520">PowerShell (Interactive)</span></span>       | `powershell-interactive`                                                       |
| <span data-ttu-id="f8634-521">Processing</span><span class="sxs-lookup"><span data-stu-id="f8634-521">Processing</span></span>                     | `processing`                                                                   |
| <span data-ttu-id="f8634-522">Prolog</span><span class="sxs-lookup"><span data-stu-id="f8634-522">Prolog</span></span>                         | `prolog`                                                                       |
| <span data-ttu-id="f8634-523">属性</span><span class="sxs-lookup"><span data-stu-id="f8634-523">Properties</span></span>                     | `properties`                                                                   |
| <span data-ttu-id="f8634-524">Protocol Buffers</span><span class="sxs-lookup"><span data-stu-id="f8634-524">Protocol Buffers</span></span>               | `protobuf`                                                                     |
| <span data-ttu-id="f8634-525">Puppet</span><span class="sxs-lookup"><span data-stu-id="f8634-525">Puppet</span></span>                         | <span data-ttu-id="f8634-526">`puppet`、`pp`</span><span class="sxs-lookup"><span data-stu-id="f8634-526">`puppet`, `pp`</span></span>                                                                 |
| <span data-ttu-id="f8634-527">Python</span><span class="sxs-lookup"><span data-stu-id="f8634-527">Python</span></span>                         | <span data-ttu-id="f8634-528">`python`、`py`、`gyp`</span><span class="sxs-lookup"><span data-stu-id="f8634-528">`python`, `py`, `gyp`</span></span>                                                          |
| <span data-ttu-id="f8634-529">Python profiler results</span><span class="sxs-lookup"><span data-stu-id="f8634-529">Python profiler results</span></span>        | `profile`                                                                      |
| <span data-ttu-id="f8634-530">Q#</span><span class="sxs-lookup"><span data-stu-id="f8634-530">Q#</span></span>                             | `qsharp`                                                                       |
| <span data-ttu-id="f8634-531">Q</span><span class="sxs-lookup"><span data-stu-id="f8634-531">Q</span></span>                              | <span data-ttu-id="f8634-532">`k`、`kdb`</span><span class="sxs-lookup"><span data-stu-id="f8634-532">`k`, `kdb`</span></span>                                                                     |
| <span data-ttu-id="f8634-533">QML</span><span class="sxs-lookup"><span data-stu-id="f8634-533">QML</span></span>                            | `qml`                                                                          |
| <span data-ttu-id="f8634-534">R</span><span class="sxs-lookup"><span data-stu-id="f8634-534">R</span></span>                              | `r`                                                                            |
| <span data-ttu-id="f8634-535">Razor CSHTML</span><span class="sxs-lookup"><span data-stu-id="f8634-535">Razor CSHTML</span></span>                   | <span data-ttu-id="f8634-536">`cshtml`、`razor`、`razor-cshtml`</span><span class="sxs-lookup"><span data-stu-id="f8634-536">`cshtml`, `razor`, `razor-cshtml`</span></span>                                              |
| <span data-ttu-id="f8634-537">ReasonML</span><span class="sxs-lookup"><span data-stu-id="f8634-537">ReasonML</span></span>                       | <span data-ttu-id="f8634-538">`reasonml`、`re`</span><span class="sxs-lookup"><span data-stu-id="f8634-538">`reasonml`, `re`</span></span>                                                               |
| <span data-ttu-id="f8634-539">RenderMan RIB</span><span class="sxs-lookup"><span data-stu-id="f8634-539">RenderMan RIB</span></span>                  | `rib`                                                                          |
| <span data-ttu-id="f8634-540">RenderMan RSL</span><span class="sxs-lookup"><span data-stu-id="f8634-540">RenderMan RSL</span></span>                  | `rsl`                                                                          |
| <span data-ttu-id="f8634-541">Roboconf</span><span class="sxs-lookup"><span data-stu-id="f8634-541">Roboconf</span></span>                       | <span data-ttu-id="f8634-542">`graph`、`instances`</span><span class="sxs-lookup"><span data-stu-id="f8634-542">`graph`, `instances`</span></span>                                                           |
| <span data-ttu-id="f8634-543">Robot Framework</span><span class="sxs-lookup"><span data-stu-id="f8634-543">Robot Framework</span></span>                | <span data-ttu-id="f8634-544">`robot`、`rf`</span><span class="sxs-lookup"><span data-stu-id="f8634-544">`robot`, `rf`</span></span>                                                                  |
| <span data-ttu-id="f8634-545">RPM spec files</span><span class="sxs-lookup"><span data-stu-id="f8634-545">RPM spec files</span></span>                 | <span data-ttu-id="f8634-546">`rpm-specfile`、`rpm`、`spec`、`rpm-spec`、`specfile`</span><span class="sxs-lookup"><span data-stu-id="f8634-546">`rpm-specfile`, `rpm`, `spec`, `rpm-spec`, `specfile`</span></span>                          |
| <span data-ttu-id="f8634-547">Ruby</span><span class="sxs-lookup"><span data-stu-id="f8634-547">Ruby</span></span>                           | <span data-ttu-id="f8634-548">`ruby`、`rb`、`gemspec`、`podspec`、`thor`、`irb`</span><span class="sxs-lookup"><span data-stu-id="f8634-548">`ruby`, `rb`, `gemspec`, `podspec`, `thor`, `irb`</span></span>                              |
| <span data-ttu-id="f8634-549">Rust</span><span class="sxs-lookup"><span data-stu-id="f8634-549">Rust</span></span>                           | <span data-ttu-id="f8634-550">`rust`、`rs`</span><span class="sxs-lookup"><span data-stu-id="f8634-550">`rust`, `rs`</span></span>                                                                   |
| <span data-ttu-id="f8634-551">SAS</span><span class="sxs-lookup"><span data-stu-id="f8634-551">SAS</span></span>                            | <span data-ttu-id="f8634-552">`SAS`、`sas`</span><span class="sxs-lookup"><span data-stu-id="f8634-552">`SAS`, `sas`</span></span>                                                                   |
| <span data-ttu-id="f8634-553">SCSS</span><span class="sxs-lookup"><span data-stu-id="f8634-553">SCSS</span></span>                           | `scss`                                                                         |
| <span data-ttu-id="f8634-554">SQL</span><span class="sxs-lookup"><span data-stu-id="f8634-554">SQL</span></span>                            | `sql`                                                                          |
| <span data-ttu-id="f8634-555">STEP Part 21</span><span class="sxs-lookup"><span data-stu-id="f8634-555">STEP Part 21</span></span>                   | <span data-ttu-id="f8634-556">`p21`、`step`、`stp`</span><span class="sxs-lookup"><span data-stu-id="f8634-556">`p21`, `step`, `stp`</span></span>                                                           |
| <span data-ttu-id="f8634-557">Scala</span><span class="sxs-lookup"><span data-stu-id="f8634-557">Scala</span></span>                          | `scala`                                                                        |
| <span data-ttu-id="f8634-558">Scheme</span><span class="sxs-lookup"><span data-stu-id="f8634-558">Scheme</span></span>                         | `scheme`                                                                       |
| <span data-ttu-id="f8634-559">Scilab</span><span class="sxs-lookup"><span data-stu-id="f8634-559">Scilab</span></span>                         | <span data-ttu-id="f8634-560">`scilab`、`sci`</span><span class="sxs-lookup"><span data-stu-id="f8634-560">`scilab`, `sci`</span></span>                                                                |
| <span data-ttu-id="f8634-561">Shape Expressions</span><span class="sxs-lookup"><span data-stu-id="f8634-561">Shape Expressions</span></span>              | `shexc`                                                                        |
| <span data-ttu-id="f8634-562">Shell</span><span class="sxs-lookup"><span data-stu-id="f8634-562">Shell</span></span>                          | <span data-ttu-id="f8634-563">`shell`、`console`</span><span class="sxs-lookup"><span data-stu-id="f8634-563">`shell`, `console`</span></span>                                                             |
| <span data-ttu-id="f8634-564">Smali</span><span class="sxs-lookup"><span data-stu-id="f8634-564">Smali</span></span>                          | `smali`                                                                        |
| <span data-ttu-id="f8634-565">Smalltalk</span><span class="sxs-lookup"><span data-stu-id="f8634-565">Smalltalk</span></span>                      | <span data-ttu-id="f8634-566">`smalltalk`、`st`</span><span class="sxs-lookup"><span data-stu-id="f8634-566">`smalltalk`, `st`</span></span>                                                              |
| <span data-ttu-id="f8634-567">Solidity</span><span class="sxs-lookup"><span data-stu-id="f8634-567">Solidity</span></span>                       | <span data-ttu-id="f8634-568">`solidity`、`sol`</span><span class="sxs-lookup"><span data-stu-id="f8634-568">`solidity`, `sol`</span></span>                                                              |
| <span data-ttu-id="f8634-569">Stan</span><span class="sxs-lookup"><span data-stu-id="f8634-569">Stan</span></span>                           | `stan`                                                                         |
| <span data-ttu-id="f8634-570">Stata</span><span class="sxs-lookup"><span data-stu-id="f8634-570">Stata</span></span>                          | `stata`                                                                        |
| <span data-ttu-id="f8634-571">Structured Text</span><span class="sxs-lookup"><span data-stu-id="f8634-571">Structured Text</span></span>                | <span data-ttu-id="f8634-572">`iecst`、`scl`、`stl`、`structured-text`</span><span class="sxs-lookup"><span data-stu-id="f8634-572">`iecst`, `scl`, `stl`, `structured-text`</span></span>                                       |
| <span data-ttu-id="f8634-573">Stylus</span><span class="sxs-lookup"><span data-stu-id="f8634-573">Stylus</span></span>                         | <span data-ttu-id="f8634-574">`stylus`、`styl`</span><span class="sxs-lookup"><span data-stu-id="f8634-574">`stylus`, `styl`</span></span>                                                               |
| <span data-ttu-id="f8634-575">SubUnit</span><span class="sxs-lookup"><span data-stu-id="f8634-575">SubUnit</span></span>                        | `subunit`                                                                      |
| <span data-ttu-id="f8634-576">Supercollider</span><span class="sxs-lookup"><span data-stu-id="f8634-576">Supercollider</span></span>                  | <span data-ttu-id="f8634-577">`supercollider`、`sc`</span><span class="sxs-lookup"><span data-stu-id="f8634-577">`supercollider`, `sc`</span></span>                                                          |
| <span data-ttu-id="f8634-578">Swift</span><span class="sxs-lookup"><span data-stu-id="f8634-578">Swift</span></span>                          | `swift`                                                                        |
| <span data-ttu-id="f8634-579">Tcl</span><span class="sxs-lookup"><span data-stu-id="f8634-579">Tcl</span></span>                            | <span data-ttu-id="f8634-580">`tcl`、`tk`</span><span class="sxs-lookup"><span data-stu-id="f8634-580">`tcl`, `tk`</span></span>                                                                    |
| <span data-ttu-id="f8634-581">Terraform (HCL)</span><span class="sxs-lookup"><span data-stu-id="f8634-581">Terraform (HCL)</span></span>                | <span data-ttu-id="f8634-582">`terraform`、`tf`、`hcl`</span><span class="sxs-lookup"><span data-stu-id="f8634-582">`terraform`, `tf`, `hcl`</span></span>                                                       |
| <span data-ttu-id="f8634-583">Test Anything Protocol</span><span class="sxs-lookup"><span data-stu-id="f8634-583">Test Anything Protocol</span></span>         | `tap`                                                                          |
| <span data-ttu-id="f8634-584">TeX</span><span class="sxs-lookup"><span data-stu-id="f8634-584">TeX</span></span>                            | `tex`                                                                          |
| <span data-ttu-id="f8634-585">Thrift</span><span class="sxs-lookup"><span data-stu-id="f8634-585">Thrift</span></span>                         | `thrift`                                                                       |
| <span data-ttu-id="f8634-586">TOML</span><span class="sxs-lookup"><span data-stu-id="f8634-586">TOML</span></span>                           | `toml`                                                                         |
| <span data-ttu-id="f8634-587">TP</span><span class="sxs-lookup"><span data-stu-id="f8634-587">TP</span></span>                             | `tp`                                                                           |
| <span data-ttu-id="f8634-588">Twig</span><span class="sxs-lookup"><span data-stu-id="f8634-588">Twig</span></span>                           | <span data-ttu-id="f8634-589">`twig`、`craftcms`</span><span class="sxs-lookup"><span data-stu-id="f8634-589">`twig`, `craftcms`</span></span>                                                             |
| <span data-ttu-id="f8634-590">TypeScript</span><span class="sxs-lookup"><span data-stu-id="f8634-590">TypeScript</span></span>                     | <span data-ttu-id="f8634-591">`typescript`、`ts`</span><span class="sxs-lookup"><span data-stu-id="f8634-591">`typescript`, `ts`</span></span>                                                             |
| <span data-ttu-id="f8634-592">VB.NET</span><span class="sxs-lookup"><span data-stu-id="f8634-592">VB.NET</span></span>                         | <span data-ttu-id="f8634-593">`vbnet`、`vb`</span><span class="sxs-lookup"><span data-stu-id="f8634-593">`vbnet`, `vb`</span></span>                                                                  |
| <span data-ttu-id="f8634-594">VBScript</span><span class="sxs-lookup"><span data-stu-id="f8634-594">VBScript</span></span>                       | <span data-ttu-id="f8634-595">`vbscript`、`vbs`</span><span class="sxs-lookup"><span data-stu-id="f8634-595">`vbscript`, `vbs`</span></span>                                                              |
| <span data-ttu-id="f8634-596">VHDL</span><span class="sxs-lookup"><span data-stu-id="f8634-596">VHDL</span></span>                           | `vhdl`                                                                         |
| <span data-ttu-id="f8634-597">Vala</span><span class="sxs-lookup"><span data-stu-id="f8634-597">Vala</span></span>                           | `vala`                                                                         |
| <span data-ttu-id="f8634-598">Verilog</span><span class="sxs-lookup"><span data-stu-id="f8634-598">Verilog</span></span>                        | <span data-ttu-id="f8634-599">`verilog`、`v`</span><span class="sxs-lookup"><span data-stu-id="f8634-599">`verilog`, `v`</span></span>                                                                 |
| <span data-ttu-id="f8634-600">Vim Script</span><span class="sxs-lookup"><span data-stu-id="f8634-600">Vim Script</span></span>                     | `vim`                                                                          |
| <span data-ttu-id="f8634-601">X++</span><span class="sxs-lookup"><span data-stu-id="f8634-601">X++</span></span>                            | `xpp`                                                                          |
| <span data-ttu-id="f8634-602">x86 Assembly</span><span class="sxs-lookup"><span data-stu-id="f8634-602">x86 Assembly</span></span>                   | `x86asm`                                                                       |
| <span data-ttu-id="f8634-603">XL</span><span class="sxs-lookup"><span data-stu-id="f8634-603">XL</span></span>                             | <span data-ttu-id="f8634-604">`xl`、`tao`</span><span class="sxs-lookup"><span data-stu-id="f8634-604">`xl`, `tao`</span></span>                                                                    |
| <span data-ttu-id="f8634-605">XQuery</span><span class="sxs-lookup"><span data-stu-id="f8634-605">XQuery</span></span>                         | <span data-ttu-id="f8634-606">`xquery`、`xpath`、`xq`</span><span class="sxs-lookup"><span data-stu-id="f8634-606">`xquery`, `xpath`, `xq`</span></span>                                                        |
| <span data-ttu-id="f8634-607">XAML</span><span class="sxs-lookup"><span data-stu-id="f8634-607">XAML</span></span>                           | `xaml`                                                                         |
| <span data-ttu-id="f8634-608">XML</span><span class="sxs-lookup"><span data-stu-id="f8634-608">XML</span></span>                            | <span data-ttu-id="f8634-609">`xml`、`xhtml`、`rss`、`atom`、`xjb`、`xsd`、`xsl`、`plist`</span><span class="sxs-lookup"><span data-stu-id="f8634-609">`xml`, `xhtml`, `rss`, `atom`, `xjb`, `xsd`, `xsl`, `plist`</span></span>                    |
| <span data-ttu-id="f8634-610">YAML</span><span class="sxs-lookup"><span data-stu-id="f8634-610">YAML</span></span>                           | <span data-ttu-id="f8634-611">`yml`、`yaml`</span><span class="sxs-lookup"><span data-stu-id="f8634-611">`yml`, `yaml`</span></span>                                                                  |
| <span data-ttu-id="f8634-612">Zephir</span><span class="sxs-lookup"><span data-stu-id="f8634-612">Zephir</span></span>                         | <span data-ttu-id="f8634-613">`zephir`、`zep`</span><span class="sxs-lookup"><span data-stu-id="f8634-613">`zephir`, `zep`</span></span>                                                                |

> [!TIP]
> <span data-ttu-id="f8634-614">当多个别名可用时，Docs 创作包的[开发语言完成功能](docs-authoring/dev-lang-completion.md)使用第一个有效别名。</span><span class="sxs-lookup"><span data-stu-id="f8634-614">The Docs Authoring Pack, [Dev Lang Completion feature](docs-authoring/dev-lang-completion.md) uses the first valid alias when multiple aliases are available.</span></span>

## <a name="next-steps"></a><span data-ttu-id="f8634-615">后续步骤</span><span class="sxs-lookup"><span data-stu-id="f8634-615">Next steps</span></span>

<span data-ttu-id="f8634-616">要了解内容类型（代码除外）的文本格式设置，请参阅[文本格式设置准则](text-formatting-guidelines.md)。</span><span class="sxs-lookup"><span data-stu-id="f8634-616">For information on text formatting for content types other than code, see [Text formatting guidelines](text-formatting-guidelines.md).</span></span>
