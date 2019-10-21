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
# <a name="formatting-code-samples"></a>设置代码示例的格式

随着时间的推移，现有文档已使用多种样式，并且格式设置规则已多次更改。 我们正在尝试在文档中创建样式一致的 PowerShell 代码块和输出。

Markdown 支持两种不同的代码样式：

- 代码范围（内联）- 由单个反引号 (`` ` ``) 字符标记。 在段落中以内联方式使用，而不是作为独立的块使用。 最常用于 cmdlet 名称。 请参阅[设置命令语法元素的格式](powershell-style-basic-markdown.md#formatting-command-syntax-elements)。
- 代码块 - 由三个反引号 (`` ``` ``) 字符串引起来的多行代码块。

## <a name="using-code-blocks"></a>使用代码块

Markdown 允许以缩进方式表示代码块，但这种模式可能会出现问题，应避免使用此模式。 所有代码块都应包含在代码隔离区中。 代码隔离区是由三个反引号 (`` ``` ``) 字符串引起来的代码块。 代码隔离区标记必须位于代码示例前后其自己的行上。 代码块开头的标记可能具有可选的语言标签。 Microsoft 的开放发布系统 (OPS) 使用语言标签来支持语法突出显示功能。

OPS 还添加了可将代码块的内容复制到剪贴板的“复制”按钮  。 这样，你就可以将代码快速粘贴到脚本中，以测试代码示例。 但是，并非文档中的所有示例都应该以这种方式运行。 一些代码块可能是 PowerShell 概念的简单说明或语法的抽象表示形式。

文档中使用两种类型的代码块：

1. 演示示例
2. 可执行示例

## <a name="formatting-illustrative-examples"></a>设置演示示例的格式

演示示例用于解释 PowerShell 概念。 不应将其复制到剪贴板来执行。 这些示例最常用于易于键入的简单示例。
它们还用于演示命令语法的语法示例。

演示示例使用“裸”代码隔离区来标记代码块的开头和结尾。 代码块可能包含所演示命令的示例输出。

### <a name="syntax-block"></a>语法块

此示例演示 `Get-Command` cmdlet 所有可能的参数。

~~~markdown
```
Get-Command [-Verb <String[]>] [-Noun <String[]>] [-Module <String[]>]
  [-FullyQualifiedModule <ModuleSpecification[]>] [-TotalCount <Int32>] [-Syntax] [-ShowCommandInfo]
  [[-ArgumentList] <Object[]>] [-All] [-ListImported] [-ParameterName <String[]>]
  [-ParameterType <PSTypeName[]>] [<CommonParameters>]
```
~~~

此示例以通用术语描述 `for` 语句：

~~~markdown
```
for (<init>; <condition>; <repeat>)
{<statement list>}
```
~~~

### <a name="simple-illustration-example"></a>简单的演示示例

以下示例演示 PowerShell 比较运算符：

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

请注意，此示例提供简化的 PowerShell 提示，并显示生成的输出。 在这种情况下，我们不希望读者复制并运行此示例。

## <a name="formatting-executable-examples"></a>设置可执行示例的格式

更复杂的示例或应该便于复制和执行的示例应使用以下块样式标记：

~~~markdown
```powershell
<PowerShell code goes here>
```
~~~

PowerShell 命令显示的输出应包含在 Output 代码块中，以防止语法突出显示  。 例如：

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

Output 代码标签不是语法突出显示系统支持的一种正式“语言”  。
但是，此标签非常有用，因为 OPS 会将“Output”标签添加到网页上的代码框中。
此“Output”代码框不会突出显示语法。

## <a name="coding-style-rules"></a>编码样式规则

### <a name="avoid-line-continuation-in-code-samples"></a>避免在代码示例中出现行继续符

避免在 PowerShell 代码示例中使用行继续符 (`` ` ``)。 如果行尾出现多余的空格，则很难看到行继续符，并且可能会引发问题。

- 使用 PowerShell 展开来缩短包含大量参数的 cmdlet 的行长度。
- 利用 PowerShell 的自然换行机会，如竖线 (`|`) 字符、左大括号、圆括号和方括号之后。

### <a name="avoid-using-powershell-prompts-in-examples"></a>避免在示例中使用 PowerShell 提示

不建议使用提示字符串，应该将其限制在旨在说明命令行用法的方案。 如果示例演示改变提示的命令，或显示的路径对所演示的方案非常重要时，则需要提示。

- PowerShell 提示应只用于演示示例。 对于其中大多数示例，提示字符串应为 `PS>`。 此提示与特定于 OS 的指示器无关。
- 提示不应用于可执行示例  。

下面的示例演示使用注册表提供程序时提示的变化。

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

### <a name="do-not-use-aliases-in-examples"></a>请勿在示例中使用别名

应始终使用所有 cmdlet 和参数的全名，除非专门讨论别名。 Cmdlet 和参数名称必须使用代码中定义的正确帕斯卡拼写法。

### <a name="using-parameters-in-examples"></a>在示例中使用参数

避免使用位置参数。 通常，即使是位置参数，也应始终在示例中包含参数名称。 这样可减少在示例中产生混淆的可能性。
