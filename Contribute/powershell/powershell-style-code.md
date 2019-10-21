---
title: 有关编写脚本示例的特定指南
description: 本文介绍有关设置 PowerShell 代码示例格式的特定规则。 这适用于包含示例的概念性文章以及 cmdlet 引用。
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
author: sdwheeler
ms.author: sewhee
ms.date: 10/09/2019
ms.openlocfilehash: f036ece21d139df0be1d677dc536023910c9d20b
ms.sourcegitcommit: ca84e542b081e145052f38967e826f6ef25da1b2
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/12/2019
ms.locfileid: "72290256"
---
# <a name="formatting-code-samples"></a><span data-ttu-id="d9626-104">设置代码示例的格式</span><span class="sxs-lookup"><span data-stu-id="d9626-104">Formatting code samples</span></span>

<span data-ttu-id="d9626-105">随着时间的推移，现有文档已使用多种样式，并且格式设置规则已多次更改。</span><span class="sxs-lookup"><span data-stu-id="d9626-105">The existing documentation has used multiple styles, over time, and the formatting rules have changed multiple times.</span></span> <span data-ttu-id="d9626-106">我们正在尝试在文档中创建样式一致的 PowerShell 代码块和输出。</span><span class="sxs-lookup"><span data-stu-id="d9626-106">We are trying to establish a consistent style for PowerShell code blocks and output in our documentation.</span></span>

<span data-ttu-id="d9626-107">Markdown 支持两种不同的代码样式：</span><span class="sxs-lookup"><span data-stu-id="d9626-107">Markdown supports two different code styles:</span></span>

- <span data-ttu-id="d9626-108">代码范围（内联）- 由单个反引号 (`` ` ``) 字符标记。</span><span class="sxs-lookup"><span data-stu-id="d9626-108">Code spans (inline) - marked by a single backtick (`` ` ``) character.</span></span> <span data-ttu-id="d9626-109">在段落中以内联方式使用，而不是作为独立的块使用。</span><span class="sxs-lookup"><span data-stu-id="d9626-109">Used inline in a paragraph rather than as a standalone block.</span></span> <span data-ttu-id="d9626-110">最常用于 cmdlet 名称。</span><span class="sxs-lookup"><span data-stu-id="d9626-110">Most commonly used around cmdlet names.</span></span> <span data-ttu-id="d9626-111">请参阅[设置命令语法元素的格式](powershell-style-basic-markdown.md#formatting-command-syntax-elements)。</span><span class="sxs-lookup"><span data-stu-id="d9626-111">See [Formatting command syntax elements](powershell-style-basic-markdown.md#formatting-command-syntax-elements).</span></span>
- <span data-ttu-id="d9626-112">代码块 - 由三个反引号 (`` ``` ``) 字符串引起来的多行代码块。</span><span class="sxs-lookup"><span data-stu-id="d9626-112">Code blocks - a multi-line block surrounded by triple-backtick (`` ``` ``) strings.</span></span>

## <a name="using-code-blocks"></a><span data-ttu-id="d9626-113">使用代码块</span><span class="sxs-lookup"><span data-stu-id="d9626-113">Using code blocks</span></span>

<span data-ttu-id="d9626-114">Markdown 允许以缩进方式表示代码块，但这种模式可能会出现问题，应避免使用此模式。</span><span class="sxs-lookup"><span data-stu-id="d9626-114">Markdown allows for indentation to signify a code block, but this pattern can be problematic and should be avoided.</span></span> <span data-ttu-id="d9626-115">所有代码块都应包含在代码隔离区中。</span><span class="sxs-lookup"><span data-stu-id="d9626-115">All code blocks should be contained in a code fence.</span></span> <span data-ttu-id="d9626-116">代码隔离区是由三个反引号 (`` ``` ``) 字符串引起来的代码块。</span><span class="sxs-lookup"><span data-stu-id="d9626-116">A code fence is a block of code surrounded by triple-backtick (`` ``` ``) strings.</span></span> <span data-ttu-id="d9626-117">代码隔离区标记必须位于代码示例前后其自己的行上。</span><span class="sxs-lookup"><span data-stu-id="d9626-117">The code fence markers must be on their own line before and after the code sample.</span></span> <span data-ttu-id="d9626-118">代码块开头的标记可能具有可选的语言标签。</span><span class="sxs-lookup"><span data-stu-id="d9626-118">The marker at the start of the code block may have an optional language label.</span></span> <span data-ttu-id="d9626-119">Microsoft 的开放发布系统 (OPS) 使用语言标签来支持语法突出显示功能。</span><span class="sxs-lookup"><span data-stu-id="d9626-119">Microsoft's Open Publishing System (OPS) uses the language label to support the syntax highlighting feature.</span></span>

<span data-ttu-id="d9626-120">OPS 还添加了可将代码块的内容复制到剪贴板的“复制”按钮  。</span><span class="sxs-lookup"><span data-stu-id="d9626-120">OPS also adds a **Copy** button that copies the contents of the code block to the clipboard.</span></span> <span data-ttu-id="d9626-121">这样，你就可以将代码快速粘贴到脚本中，以测试代码示例。</span><span class="sxs-lookup"><span data-stu-id="d9626-121">This allows you to quickly paste the code into a script for testing the code example.</span></span> <span data-ttu-id="d9626-122">但是，并非文档中的所有示例都应该以这种方式运行。</span><span class="sxs-lookup"><span data-stu-id="d9626-122">However, not all examples in our documentation are intended to be run that way.</span></span> <span data-ttu-id="d9626-123">一些代码块可能是 PowerShell 概念的简单说明或语法的抽象表示形式。</span><span class="sxs-lookup"><span data-stu-id="d9626-123">Some code blocks may be a simple illustration of a PowerShell concept or an abstract representation of syntax.</span></span>

<span data-ttu-id="d9626-124">文档中使用两种类型的代码块：</span><span class="sxs-lookup"><span data-stu-id="d9626-124">There are two types code blocks used in our documentation:</span></span>

1. <span data-ttu-id="d9626-125">演示示例</span><span class="sxs-lookup"><span data-stu-id="d9626-125">Illustrative examples</span></span>
2. <span data-ttu-id="d9626-126">可执行示例</span><span class="sxs-lookup"><span data-stu-id="d9626-126">Executable examples</span></span>

## <a name="formatting-illustrative-examples"></a><span data-ttu-id="d9626-127">设置演示示例的格式</span><span class="sxs-lookup"><span data-stu-id="d9626-127">Formatting illustrative examples</span></span>

<span data-ttu-id="d9626-128">演示示例用于解释 PowerShell 概念。</span><span class="sxs-lookup"><span data-stu-id="d9626-128">Illustrative examples are used to explain a PowerShell concept.</span></span> <span data-ttu-id="d9626-129">不应将其复制到剪贴板来执行。</span><span class="sxs-lookup"><span data-stu-id="d9626-129">They are not meant to be copied to the clipboard for execution.</span></span> <span data-ttu-id="d9626-130">这些示例最常用于易于键入的简单示例。</span><span class="sxs-lookup"><span data-stu-id="d9626-130">These are most commonly used for simple examples that are easy to type.</span></span>
<span data-ttu-id="d9626-131">它们还用于演示命令语法的语法示例。</span><span class="sxs-lookup"><span data-stu-id="d9626-131">They are also used for syntax examples where you are illustrating the syntax of a command.</span></span>

<span data-ttu-id="d9626-132">演示示例使用“裸”代码隔离区来标记代码块的开头和结尾。</span><span class="sxs-lookup"><span data-stu-id="d9626-132">Illustrative examples use a "naked" code fence to mark the beginning and end of the code block.</span></span> <span data-ttu-id="d9626-133">代码块可能包含所演示命令的示例输出。</span><span class="sxs-lookup"><span data-stu-id="d9626-133">The code block may contain example output from the command being illustrated.</span></span>

### <a name="syntax-block"></a><span data-ttu-id="d9626-134">语法块</span><span class="sxs-lookup"><span data-stu-id="d9626-134">Syntax block</span></span>

<span data-ttu-id="d9626-135">此示例演示 `Get-Command` cmdlet 所有可能的参数。</span><span class="sxs-lookup"><span data-stu-id="d9626-135">This example illustrates all the possible parameters of the `Get-Command` cmdlet.</span></span>

~~~markdown
```
Get-Command [-Verb <String[]>] [-Noun <String[]>] [-Module <String[]>]
  [-FullyQualifiedModule <ModuleSpecification[]>] [-TotalCount <Int32>] [-Syntax] [-ShowCommandInfo]
  [[-ArgumentList] <Object[]>] [-All] [-ListImported] [-ParameterName <String[]>]
  [-ParameterType <PSTypeName[]>] [<CommonParameters>]
```
~~~

<span data-ttu-id="d9626-136">此示例以通用术语描述 `for` 语句：</span><span class="sxs-lookup"><span data-stu-id="d9626-136">This example describes the `for` statement in generalized terms:</span></span>

~~~markdown
```
for (<init>; <condition>; <repeat>)
{<statement list>}
```
~~~

### <a name="simple-illustration-example"></a><span data-ttu-id="d9626-137">简单的演示示例</span><span class="sxs-lookup"><span data-stu-id="d9626-137">Simple illustration example</span></span>

<span data-ttu-id="d9626-138">以下示例演示 PowerShell 比较运算符：</span><span class="sxs-lookup"><span data-stu-id="d9626-138">Here is an example illustrating PowerShell comparison operators:</span></span>

~~~markdown
```
PS> 2 -eq 2
True

PS> 2 -eq 3
False

PS>  1,2,3 -eq 2
2

PS> "abc" -eq "abc"
True

PS> "abc" -eq "abc", "def"
False

PS> "abc", "def" -eq "abc"
abc
```
~~~

<span data-ttu-id="d9626-139">请注意，此示例提供简化的 PowerShell 提示，并显示生成的输出。</span><span class="sxs-lookup"><span data-stu-id="d9626-139">Note that this example has the simplified PowerShell prompt and shows the resulting output.</span></span> <span data-ttu-id="d9626-140">在这种情况下，我们不希望读者复制并运行此示例。</span><span class="sxs-lookup"><span data-stu-id="d9626-140">In this case, we don't intend the reader to copy and run this example.</span></span>

## <a name="formatting-executable-examples"></a><span data-ttu-id="d9626-141">设置可执行示例的格式</span><span class="sxs-lookup"><span data-stu-id="d9626-141">Formatting executable examples</span></span>

<span data-ttu-id="d9626-142">更复杂的示例或应该便于复制和执行的示例应使用以下块样式标记：</span><span class="sxs-lookup"><span data-stu-id="d9626-142">More complex examples or examples that are intended to be useful to copy and execute should use the following block-style markup:</span></span>

~~~markdown
```powershell
<PowerShell code goes here>
```
~~~

<span data-ttu-id="d9626-143">PowerShell 命令显示的输出应包含在 Output 代码块中，以防止语法突出显示  。</span><span class="sxs-lookup"><span data-stu-id="d9626-143">The output displayed by PowerShell commands should be enclosed in an **Output** code block to prevent syntax highlighting.</span></span> <span data-ttu-id="d9626-144">例如：</span><span class="sxs-lookup"><span data-stu-id="d9626-144">For example:</span></span>

~~~markdown
```powershell
Get-Command -Module Microsoft.PowerShell.Security
```

```Output
CommandType  Name                        Version    Source
-----------  ----                        -------    ------
Cmdlet       ConvertFrom-SecureString    3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       ConvertTo-SecureString      3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       Get-Acl                     3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       Get-AuthenticodeSignature   3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       Get-CmsMessage              3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       Get-Credential              3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       Get-ExecutionPolicy         3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       Get-PfxCertificate          3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       New-FileCatalog             3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       Protect-CmsMessage          3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       Set-Acl                     3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       Set-AuthenticodeSignature   3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       Set-ExecutionPolicy         3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       Test-FileCatalog            3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       Unprotect-CmsMessage        3.0.0.0    Microsoft.PowerShell.Security
```
~~~

<span data-ttu-id="d9626-145">Output 代码标签不是语法突出显示系统支持的一种正式“语言”  。</span><span class="sxs-lookup"><span data-stu-id="d9626-145">The **Output** code label is not an official "language" supported by the syntax highlighting system.</span></span>
<span data-ttu-id="d9626-146">但是，此标签非常有用，因为 OPS 会将“Output”标签添加到网页上的代码框中。</span><span class="sxs-lookup"><span data-stu-id="d9626-146">However, this label is useful because OPS adds the "Output" label to the code box on the web page.</span></span>
<span data-ttu-id="d9626-147">此“Output”代码框不会突出显示语法。</span><span class="sxs-lookup"><span data-stu-id="d9626-147">And this "Output" code box has no syntax highlighting.</span></span>

## <a name="coding-style-rules"></a><span data-ttu-id="d9626-148">编码样式规则</span><span class="sxs-lookup"><span data-stu-id="d9626-148">Coding style rules</span></span>

### <a name="avoid-line-continuation-in-code-samples"></a><span data-ttu-id="d9626-149">避免在代码示例中出现行继续符</span><span class="sxs-lookup"><span data-stu-id="d9626-149">Avoid line continuation in code samples</span></span>

<span data-ttu-id="d9626-150">避免在 PowerShell 代码示例中使用行继续符 (`` ` ``)。</span><span class="sxs-lookup"><span data-stu-id="d9626-150">Avoid using line continuation characters (`` ` ``) in PowerShell code examples.</span></span> <span data-ttu-id="d9626-151">如果行尾出现多余的空格，则很难看到行继续符，并且可能会引发问题。</span><span class="sxs-lookup"><span data-stu-id="d9626-151">These are hard to see and can cause problems if there are extra spaces at the end of the line.</span></span>

- <span data-ttu-id="d9626-152">使用 PowerShell 展开来缩短包含大量参数的 cmdlet 的行长度。</span><span class="sxs-lookup"><span data-stu-id="d9626-152">Use PowerShell splatting to reduce line length for cmdlets that have a lot of parameters.</span></span>
- <span data-ttu-id="d9626-153">利用 PowerShell 的自然换行机会，如竖线 (`|`) 字符、左大括号、圆括号和方括号之后。</span><span class="sxs-lookup"><span data-stu-id="d9626-153">Take advantage of PowerShell's natural line break opportunities, like after pipe (`|`) characters, opening braces, parentheses, and brackets.</span></span>

### <a name="avoid-using-powershell-prompts-in-examples"></a><span data-ttu-id="d9626-154">避免在示例中使用 PowerShell 提示</span><span class="sxs-lookup"><span data-stu-id="d9626-154">Avoid using PowerShell prompts in examples</span></span>

<span data-ttu-id="d9626-155">不建议使用提示字符串，应该将其限制在旨在说明命令行用法的方案。</span><span class="sxs-lookup"><span data-stu-id="d9626-155">Use of the prompt string is discouraged and should be limited to scenarios that are meant to illustrate command line usage.</span></span> <span data-ttu-id="d9626-156">如果示例演示改变提示的命令，或显示的路径对所演示的方案非常重要时，则需要提示。</span><span class="sxs-lookup"><span data-stu-id="d9626-156">Prompts are required for examples that illustrate commands that alter the prompt or when the path displayed is significant to the scenario being illustrated.</span></span>

- <span data-ttu-id="d9626-157">PowerShell 提示应只用于演示示例。</span><span class="sxs-lookup"><span data-stu-id="d9626-157">PowerShell prompts should only be used in illustrative examples.</span></span> <span data-ttu-id="d9626-158">对于其中大多数示例，提示字符串应为 `PS>`。</span><span class="sxs-lookup"><span data-stu-id="d9626-158">For most of these examples, the prompt string should be "`PS>`".</span></span> <span data-ttu-id="d9626-159">此提示与特定于 OS 的指示器无关。</span><span class="sxs-lookup"><span data-stu-id="d9626-159">This prompt is independent of OS-specific indicators.</span></span>
- <span data-ttu-id="d9626-160">提示不应用于可执行示例  。</span><span class="sxs-lookup"><span data-stu-id="d9626-160">Prompts should **NOT** be used in executable examples.</span></span>

<span data-ttu-id="d9626-161">下面的示例演示使用注册表提供程序时提示的变化。</span><span class="sxs-lookup"><span data-stu-id="d9626-161">The following example illustrates how the prompt changes when using the Registry provider.</span></span>

```powershell
PS C:\> cd HKCU:\System\
PS HKCU:\System\> dir

    Hive: HKEY_CURRENT_USER\System

Name                   Property
----                   --------
CurrentControlSet
GameConfigStore        GameDVR_Enabled                       : 1
                       GameDVR_FSEBehaviorMode               : 2
                       Win32_AutoGameModeDefaultProfile      : {2, 0, 1, 0...}
                       Win32_GameModeRelatedProcesses        : {1, 0, 1, 0...}
                       GameDVR_HonorUserFSEBehaviorMode      : 0
                       GameDVR_DXGIHonorFSEWindowsCompatible : 0
```

### <a name="do-not-use-aliases-in-examples"></a><span data-ttu-id="d9626-162">请勿在示例中使用别名</span><span class="sxs-lookup"><span data-stu-id="d9626-162">Do not use aliases in examples</span></span>

<span data-ttu-id="d9626-163">应始终使用所有 cmdlet 和参数的全名，除非专门讨论别名。</span><span class="sxs-lookup"><span data-stu-id="d9626-163">You should always use the full name of all cmdlets and parameters unless you are specifically talking about the alias.</span></span> <span data-ttu-id="d9626-164">Cmdlet 和参数名称必须使用代码中定义的正确帕斯卡拼写法。</span><span class="sxs-lookup"><span data-stu-id="d9626-164">Cmdlet and parameter names must use the proper Pascal-case spelling defined in the code.</span></span>

### <a name="using-parameters-in-examples"></a><span data-ttu-id="d9626-165">在示例中使用参数</span><span class="sxs-lookup"><span data-stu-id="d9626-165">Using parameters in examples</span></span>

<span data-ttu-id="d9626-166">避免使用位置参数。</span><span class="sxs-lookup"><span data-stu-id="d9626-166">Avoid using positional parameters.</span></span> <span data-ttu-id="d9626-167">通常，即使是位置参数，也应始终在示例中包含参数名称。</span><span class="sxs-lookup"><span data-stu-id="d9626-167">In general, you should use always include the parameter name in an example, even if the parameter positional.</span></span> <span data-ttu-id="d9626-168">这样可减少在示例中产生混淆的可能性。</span><span class="sxs-lookup"><span data-stu-id="d9626-168">This reduces the chance of confusion in your examples.</span></span>
