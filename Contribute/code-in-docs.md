---
title: 如何在文档中包含代码
description: 了解如何在发布到 docs.microsoft.com 的文章中包含代码元素和代码段。
author: tdykstra
ms.author: tdykstra
ms.date: 03/03/2020
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.custom: external-contributor-guide
ms.openlocfilehash: b33333a49df11f0234193ca84fc2c3accdb6894d
ms.sourcegitcommit: f1535713b66ff9b840f1138583746bc2bf182b4f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/12/2020
ms.locfileid: "91953641"
---
# <a name="how-to-include-code-in-docs"></a>如何在文档中包含代码

可以通过以下几种方法在发布到 docs.microsoft.com 的文章中包含代码：

* 一行中的单个元素（单词）。

  以下是 `code` 样式的示例。

  在文本中引用附近代码块中的命名参数和变量时，使用代码格式。 代码格式也可用于属性、方法、类和语言关键字。 有关详细信息，请参阅本文后面的[代码元素](#code-elements)。

* 文章 Markdown 文件中的代码块。

  ```markdown
      ```csharp
      public static void Log(string message)
      {
          _logger.LogInformation(message);
      }
      ```
  ```

  不能通过引用代码文件来显示代码时，使用内联代码块。 有关详细信息，请参阅本文后面的[代码块](#inline-code-blocks)。

* 通过引用本地存储库中的代码文件的代码块。

  ```markdown
  :::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" range="2-24,26":::
  ```

  有关详细信息，请参阅本文后面的[存储库内的片段引用](#in-repo-snippet-references)。

* 通过引用另一存储库中的代码文件的代码块。

  ```markdown
  :::code language="csharp" source="~/samples-durable-functions/samples/csx/shared/Location.csx" highlight="2,5":::
  ```
  
  有关详细信息，请参阅本文后面的[存储库外的片段引用](#out-of-repo-snippet-references)。
  
* 允许用户在浏览器中执行代码的代码块。

   ```markdown
  :::code source="PowerShell.ps1" interactive="cloudshell-powershell":::
  ```

  有关详细信息，请参阅本文后面的[交互式代码片段](#interactive-code-snippets)。

除了解释包含代码的每种方法的 Markdown 之外，本文还提供了一些[适用于所有代码块的一般指南](#code-blocks)。

## <a name="code-elements"></a>代码元素

“代码元素”指的是编程语言关键字、类名、属性名称等。 什么内容可以称为代码，并不总是显而易见。 例如，NuGet 包名称应被视为代码。 如有疑问，请参阅[文本格式设置准则](text-formatting-guidelines.md)。

### <a name="inline-code-style"></a>内联代码样式

若要在文章文本中包含代码元素，请使用反斜线 (\`) 将其包住，表示代码样式。
内联代码样式不得使用三个反引号格式。

|Markdown |呈现 |
|---------|---------|
|默认情况下，实体框架将名为 \`Id\` 或 \`ClassnameID\` 的属性解释为主键。|默认情况下，实体框架将名为 `Id` 或 `ClassnameID` 的属性解释为主键。|

在本地化文章（翻译成其他语言）时，不会翻译代码样式的文本。 如果要在不使用代码样式的情况下防止本地化，请参阅[非本地化字符串](markdown-reference.md#non-localized-strings)。

### <a name="bold-style"></a>粗体样式

一些较旧的风格指南为内联代码指定粗体格式。 当代码样式太过突兀以致于影响可读性时，可以选择使用粗体。 例如，主要包含代码元素的 Markdown 表格如果全部应用代码样式，可能看起来杂乱。 如果选择使用粗体样式，请使用[非本地化字符串语法](markdown-reference.md#non-localized-strings)以确保代码未本地化。

### <a name="links"></a>链接

在某些上下文中，指向参考文档的链接可能比代码格式更有帮助。 如果使用链接，请勿将代码格式应用于链接文本。 将链接设置为代码会掩盖文本是链接的事实。

如果使用链接，并且之后在相同的上下文中引用同一元素，请对后面的实例应用代码格式而非链接。

### <a name="placeholders"></a>占位符

如果希望用户使用其自己的值替换一段显示的代码，请使用由尖括号或大括号标记的占位符文本。 例如：`az group delete -n <ResourceGroupName>`。 说明在替换实值时必须删除尖括号或大括号。

## <a name="code-blocks"></a>代码块

用于将代码包含在文档中的语法取决于代码所在的位置：

* [在文章的 Markdown 文件中](#inline-code-blocks)
* [在同一个存储库的代码文件中](#in-repo-snippet-references)
* [在不同存储库的代码文件中](#out-of-repo-snippet-references)

下面是适用于所有三种类型代码块的指导原则：

* [自动执行代码验证。](#code-validation)
* [突出显示关键代码行。](#highlighting)
* [避免水平滚动条。](#horizontal-scroll-bars)

### <a name="screenshots"></a>屏幕截图

上一部分中列出的所有方法均可生成可用的代码块：

* 可从中进行复制和粘贴。
* 可通过搜索引擎将其编入索引。
* 屏幕阅读器可访问这些代码块。

这只是建议不要将 IDE 屏幕截图作为在文章中包含代码的方法的一些原因。 仅当显示 IDE 本身的相关信息（如 IntelliSense）时，才将 IDE 屏幕截图用于代码。 请勿仅将屏幕截图用于显示着色和突出显示。

### <a name="code-validation"></a>代码验证

一些存储库已经实现了自动编译所有示例代码以检查错误的过程。 .NET 存储库已实现此过程。 有关详细信息，请参阅 .NET 存储库中的[参与](https://github.com/dotnet/docs/blob/master/CONTRIBUTING.md)。

如果要包含其他存储库中的代码块，请与所有者共同制定代码维护策略，以便在提供代码使用的新版本的库时，你包含的代码不会中断或过期。

### <a name="highlighting"></a>突出显示

代码段通常包含提供上下文所需的更多代码。 在代码段中突出显示所关注的关键行时，它有助于提高可读性，如本例所示：

![突出显示的代码示例](media/code-in-docs/highlighted-code.png)

将代码包含在文章的 Markdown 文件中时，将无法突出显示代码。 它只适用于通过引用代码文件包含的代码段。

### <a name="horizontal-scroll-bars"></a>水平滚动条

分解较长的行，以避免水平滚动条。 代码块上的滚动条为阅读代码带来困难。 在更长的代码块上尤其会出现此问题，在其中可能无法看到滚动条和同时想要读取的行。

要尽量使代码块上的水平滚动条保持最小，一种很好的做法是分解超过 85 个字符的代码行。 但请记住，滚动条存在与否不是衡量可读性的唯一标准。 如果在不到 85 个字符时换行，会影响可读性或复制粘贴的便捷性，因此请随意超过 85 个字符。

## <a name="inline-code-blocks"></a>内联代码块

仅当不能通过引用代码文件来显示代码时，才使用内联代码块。 与代码文件（完整项目的一部分）相比，内联代码通常更难测试且更难保持最新。  并且内联代码可能忽略可帮助开发人员理解和使用代码的上下文。 这些注意事项主要适用于编程语言。 内联代码块还可用于输出和输入（如 JSON）、查询语言（如 SQL）和脚本语言（如 PowerShell）。
  
可以通过以下两种方法在文章文件中指出文本的一部分是一个代码块：使用三个反斜杠 (\`\`\`) 将其隔开或缩进。 隔离是首选方法，因为它允许指定语言。 避免使用缩进，因为这样极易出错，并且当其他编写者需要编辑你的文章时，可能很难理解你的意图。

语言指示紧跟开头的三个反斜杠后，如以下示例所示：

Markdown：

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

呈现：

```json
{
    "aggregator": {
        "batchSize": 1000,
        "flushTimeout": "00:00:30"
    }
}
```

有关可以用作语言指示的值的信息，请参阅[语言名称和别名](http://highlightjs.readthedocs.io/en/latest/css-classes-reference.html#language-names-and-aliases)。

如果在三个反引号 (\`\`\`) 后面使用不受支持的语言或环境单词，该单词会显示在呈现页面上的代码部分标题栏中。 请尽量在内联代码块中使用语言或环境指示。

> [!NOTE]
> 如果复制粘贴 Word 文档中的代码，请确保它没有对代码无效的“弯引号”（如 `“` 和 `’`）。 如果有，请将其改为常规引号（`'` 和 `"`）。 或者，使用 Docs 创作包 - [智能引号替换功能](docs-authoring/smart-quote-replacement.md)。

## <a name="in-repo-snippet-references"></a>存储库内的代码段引用

要在文档中包含用于编程语言的代码片段，首选方法是引用代码文件。 借助此方法，你可以突出显示几行代码，并在 GitHub 上提供更广泛的代码片段上下文供开发人员使用。 可手动使用三冒号格式 (:\:\:) 或在 Visual Studio Code 中借助 [docs.microsoft.com 创作包](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack)来包含代码。

1. 在 Visual Studio Code 中，单击 Alt + M 或 Option + M，再选择“片段”<kbd></kbd><kbd></kbd>。
2. 选择片段后，系统将提示你进行完全搜索、范围搜索或跨存储库引用。 要在本地搜索，请选择“完整搜索”。
3. 要查找文件，请输入搜索词。 找到文件后，将其选中。
4. 接下来，选择一个选项来确定应在片段中包含哪些代码行。 选项包括：“ID”、“范围”和“无”。
5. 根据在步骤 4 中选择的设置，必要时提供一个值。

显示整个代码文件：

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs":::
```

通过指定行号来显示代码文件的一部分：

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" range="2-24,26":::
```

通过指定一个代码段名称来显示代码文件的一部分：

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" id="snippet_Create":::
```

以下部分说明了这些示例：

* [使用代码文件的相对路径](#path-to-code-file)
* [只包括选定行号](#selected-line-numbers)
* [参考命名的代码段](#named-snippet)
* [突出显示选定行](#highlighting-selected-lines)

有关详细信息，请查看本文后面的[片段语法引用](#snippet-syntax-reference)。

### <a name="path-to-code-file"></a>代码文件路径

示例：

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" range="2-24,26":::
```

本示例摘自 ASP.NET 文档存储库，[aspnetcore/data/ef-mvc/crud.md](https://github.com/aspnet/Docs/blob/master/aspnetcore/data/ef-mvc/crud.md) 文章文件。 此代码文件通过同一存储库中的 [aspnetcore/data/ef-mvc/intro/samples/cu/Controllers/StudentsController.cs](https://github.com/aspnet/Docs/blob/master/aspnetcore/data/ef-mvc/intro/samples/cu/Controllers/StudentsController.cs) 相对路径进行引用。

### <a name="selected-line-numbers"></a>选定行号

示例：

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" range="2-24,26":::
```

此示例仅显示了 StudentController.cs 代码文件中的第 2-24 行和第 26 行。

更倾向于命名的代码片段而不是硬编码的行号，如下一部分所述。

### <a name="named-snippet"></a>命名的代码段

示例：

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" id="snippet_Create":::
```

仅在名称中使用字母和下划线。

本示例显示代码文件的 `snippet_Create` 部分。 本示例的代码文件在 C# 代码中注释中带有代码片段标记：

```cs
// code excluded from the snippet
// <snippet_Create>
// code included in the snippet
// </snippet_Create>
// code excluded from the snippet
```

在可能的情况下，请参考命名的部分，而不是指定行号。 行号引用不太稳妥，因为在更改行号时，代码文件不可避免地会发生更改。
不一定会收到此类更改的通知。 最终，文章开始显示错误行，并且你完全不知道发生的任何变更。

### <a name="highlighting-selected-lines"></a>突出显示选定行

示例：

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" range="2-24,26" highlight="2,5":::
```

本示例突出显示第 2 行和第 5 行，从显示的代码段开头开始计数。 要突出显示的行号并不从代码文件的开头开始计数。 也就是说，代码文件的第 3 行和第 6 行会突出显示。

## <a name="out-of-repo-snippet-references"></a>存储库外的代码段引用

如果要引用的代码文件在另一个存储库中，请将代码储存库设置为“从属存储库”。 在执行此操作时，请为它指定一个名称。 然后，该名称会作为一个文件夹名称用于代码引用。

例如，文档存储库是 Azure/azure-docs，代码存储库是 Azure/azure-functions-durable-extension。

在 azure-docs 的根文件夹中，在 .openpublishing.publish.config.json 中添加以下部分：

```json
    {
      "path_to_root": "samples-durable-functions",
      "url": "https://github.com/Azure/azure-functions-durable-extension",
      "branch": "master",
      "branch_mapping": {}
    },
```

现在，当你引用 sample-durable-functions（如同它是 azure-docs 中的一个文件夹）时，你实际上引用的是 azure-functions-durable-extension 存储库中的根文件夹。

可手动使用三冒号格式 (:\:\:) 或在 Visual Studio Code 中借助 [docs.microsoft.com 创作包](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack)来包含代码。

1. 在 Visual Studio Code 中，单击 Alt + M 或 Option + M，再选择“片段”<kbd></kbd><kbd></kbd>。
2. 选择片段后，系统将提示你进行完全搜索、范围搜索或跨存储库引用。 要跨存储库进行搜索，请选择“跨存储库引用”。
3. 将显示 .openpublishing.publish.config.json 中的存储库供你选择。 选择存储库。
4. 要查找文件，请输入搜索词。 找到文件后，将其选中。
5. 接下来，选择一个选项来确定应在片段中包含哪些代码行。 选项包括：“ID”、“范围”和“无”。
6. 根据在步骤 5 中选择的设置，提供一个值。

你的片段引用将如下所示：

```markdown
:::code language="csharp" source="~/samples-durable-functions/samples/csx/shared/Location.csx" highlight="2,5":::
```

在 azure-functions-durable-extension 存储库中，该代码文件位于 samples/csx/shared 文件夹中。 [如前](#highlighting-selected-lines)所述，突出显示的行号对应于代码片段的开头而非文件的开头。

> [!NOTE]
> 分配给从属存储库的名称对应于主存储库的根目录，但波形符 (~) 是指文档集的根目录。 文档集根目录由 .openpublishing.publish.config.json 中的 `build_source_folder` 确定。 上一示例中代码片段的路径可在 azure-docs 存储库中使用，因为 `build_source_folder` 指的是存储库根目录 (`.`)。 如果 `build_source_folder` 为 `articles`，则路径将以 `~/../samples-durable-functions` 而非 `~/samples-durable-functions` 开头。

## <a name="interactive-code-snippets"></a>交互式代码片段

### <a name="inline-interactive-code-blocks"></a>内联交互式代码块

对于以下语言，可以在浏览器窗口中执行代码段：

* Azure Cloud Shell
* Azure PowerShell Cloud Shell
* C# REPL

启用交互模式后，呈现的代码框会出现“尝试”或“运行”按钮。 例如：

```markdown
    ```azurepowershell-interactive
    New-AzResourceGroup -Name myResourceGroup -Location westeurope
    ```
```

呈现为：

```azurepowershell-interactive
New-AzResourceGroup -Name myResourceGroup -Location westeurope
```

要为特定代码块启用此功能，请使用特殊的语言标识符。 可用选项包括：

* `azurepowershell-interactive` - 启用 Azure PowerShell Cloud Shell，如前例所示
* `azurecli-interactive` - 启用 Azure Cloud Shell
* `csharp-interactive` - 启用 C# REPL

对于 Azure Cloud Shell 和 PowerShell Cloud Shell，用户可以只针对自己的 Azure 帐户运行命令。

### <a name="code-snippets-included-by-reference"></a>通过引用包含的代码片段

可以为通过引用包含的代码段启用交互模式。 示例如下：

```markdown
:::code source="PowerShell.ps1" interactive="cloudshell-powershell":::
```

```markdown
:::code source="Bash.sh" interactive="cloudshell-bash":::
```

要为特定代码块启用此功能，请使用 `interactive` 属性。 可用的属性值如下：

* `cloudshell-powershell` - 启用 Azure PowerShell Cloud Shell，如前例所示
* `cloudshell-bash` - 启用 Azure Cloud Shell
* `try-dotnet` - 启用 .NET Interactive
* `try-dotnet-class` - 使用类基架启用 .NET Interactive
* `try-dotnet-method` - 使用方法基架启用 .NET Interactive

对于 Azure Cloud Shell 和 PowerShell Cloud Shell，用户只能针对自己的 Azure 帐户运行命令。

对于 .NET Interactive 体验，代码块的内容取决于三种基架体验中所选的体验：

* 无基架 (`try-dotnet`)：代码块应表示完整的程序文本。 例如，`dotnet new console` 生成的 Program.cs 文件将有效。 这些最适用于显示整个小程序，包括所需的 `using` 指令。 此时不支持顶级语句。
* 方法基架 (`try-dotnet-method`)：代码块应表示控制台应用程序中的 `Main` 方法的内容。 你可以假设由 `dotnet new console` 模板添加的 `using` 指令。 此设置最适用于演示一个功能的短代码段。
* 类基架 (`try-dotnet-class`)：代码块应将具有 `Main` 方法的类表示为程序入口点。 这些可用于显示类的成员如何交互。

## <a name="snippet-syntax-reference"></a>片段语法引用

语法：

```md
:::code language="<language>" source="<path>" <attribute>="<attribute-value>":::
```

> [!IMPORTANT]
> 此语法是块 Markdown 扩展。 必须在自己的行中使用它。

* `<language>`（可选）
  * 代码片段的语言。 有关详细信息，请参阅本文后面的[支持的语言](#supported-languages)部分。

* `<path>`（必需）
  * 文件系统中的相对路径，指示将引用的代码片段文件。

* `<attribute>` 和 `<attribute-value>`（可选）**

  配合使用以指定如何从文件中检索代码以及如何显示代码：

  * `range`：`1,3-5` 行的范围。 此示例包含第 1、3、4 和 5 行。
  * `id`：`snippet_Create`：需要从代码文件中插入的片段的 ID。 该值不能与范围共存。
  * `highlight`：`2-4,6`：需要在生成的代码片段中突出显示的范围和/或行数。 该编号对应于显示的行数（由范围或 ID 指定）而非文件。
  * `interactive`：`cloudshell-powershell`、`cloudshell-bash`、`try-dotnet`、`try-dotnet-class`、`try-dotnet-method` 字符串值确定启用了哪些类型的交互。
  * 有关按语言在代码片段源文件中呈现标记名称的详细信息，请参阅 [DocFX 准则](https://dotnet.github.io/docfx/spec/docfx_flavored_markdown.html#tag-name-representation-in-code-snippet-source-file)。

## <a name="supported-languages"></a>支持的语言

[Docs 创作包](how-to-write-docs-auth-pack.md)包含一项功能，可对代码隔离块的可用语言标识符提供语句完成和验证功能。

### <a name="fenced-code-blocks"></a>隔离代码块

| 名称                           | 有效别名                                                                  |
|--------------------------------|--------------------------------------------------------------------------------|
| .NET Core CLI                  | `dotnetcli`                                                                    |
| 1C                             | `1c`                                                                           |
| ABNF                           | `abnf`                                                                         |
| 访问日志                    | `accesslog`                                                                    |
| Ada                            | `ada`                                                                          |
| ARM assembler                  | `armasm`、`arm`                                                                |
| AVR assembler                  | `avrasm`                                                                       |
| ActionScript                   | `actionscript`, `as`                                                           |
| Alan                           | `alan`、`i`                                                                    |
| AngelScript                    | `angelscript`, `asc`                                                           |
| ANTLR                          | `antlr`                                                                        |
| Apache                         | `apache`, `apacheconf`                                                         |
| AppleScript                    | `applescript`, `osascript`                                                     |
| 街机游戏                         | `arcade`                                                                       |
| AsciiDoc                       | `asciidoc`, `adoc`                                                             |
| AspectJ                        | `aspectj`                                                                      |
| ASPX                           | `aspx`                                                                         |
| ASP.NET (C#)                   | `aspx-csharp`                                                                  |
| ASP.NET (VB)                   | `aspx-vb`                                                                      |
| AutoHotkey                     | `autohotkey`                                                                   |
| AutoIt                         | `autoit`                                                                       |
| Awk                            | `awk`, `mawk`, `nawk`, `gawk`                                                  |
| Axapta                         | `axapta`                                                                       |
| AzCopy                         | `azcopy`                                                                       |
| Azure CLI                      | `azurecli`                                                                     |
| Azure CLI (Interactive)        | `azurecli-interactive`                                                         |
| Azure Powershell               | `azurepowershell`                                                              |
| Azure Powershell (Interactive) | `azurepowershell-interactive`                                                  |
| Bash                           | `bash`, `sh`, `zsh`                                                            |
| 基本                          | `basic`                                                                        |
| BNF                            | `bnf`                                                                          |
| C                              | `c`                                                                            |
| C#                             | `csharp`、`cs`                                                                 |
| C# (Interactive)               | `csharp-interactive`                                                           |
| C++                            | `cpp`, `c`, `cc`, `h`, `c++`, `h++`, `hpp`                                     |
| C++/CX                         | `cppcx`                                                                        |
| C++/WinRT                      | `cppwinrt`                                                                     |
| C/AL                           | `cal`                                                                          |
| Cache Object Script            | `cos`, `cls`                                                                   |
| CMake                          | `cmake`, `cmake.in`                                                            |
| Coq                            | `coq`                                                                          |
| CSP                            | `csp`                                                                          |
| CSS                            | `css`                                                                          |
| Cap'n Proto                    | `capnproto`, `capnp`                                                           |
| Clojure                        | `clojure`, `clj`                                                               |
| CoffeeScript                   | `coffeescript`, `coffee`, `cson`, `iced`                                       |
| Crmsh                          | `crmsh`, `crm`, `pcmk`                                                         |
| Crystal                        | `crystal`, `cr`                                                                |
| Cypher (Neo4j)                 | `cypher`                                                                       |
| D                              | `d`                                                                            |
| DAX Power BI                   | `dax`                                                                          |
| DNS Zone file                  | `dns`, `zone`, `bind`                                                          |
| DOS                            | `dos`, `bat`, `cmd`                                                            |
| Dart                           | `dart`                                                                         |
| Delphi                         | `delphi`, `dpr`, `dfm`, `pas`, `pascal`, `freepascal`, `lazarus`, `lpr`, `lfm` |
| 差异                           | `diff`, `patch`                                                                |
| Django                         | `django`, `jinja`                                                              |
| Dockerfile                     | `dockerfile`、`docker`                                                         |
| dsconfig                       | `dsconfig`                                                                     |
| DTS (Device Tree)              | `dts`                                                                          |
| Dust                           | `dust`, `dst`                                                                  |
| Dylan                          | `dylan`                                                                        |
| EBNF                           | `ebnf`                                                                         |
| Elixir                         | `elixir`                                                                       |
| Elm                            | `elm`                                                                          |
| Erlang                         | `erlang`, `erl`                                                                |
| Excel                          | `excel`, `xls`, `xlsx`                                                         |
| Extempore                      | `extempore`, `xtlang`, `xtm`                                                   |
| F#                             | `fsharp`, `fs`                                                                 |
| FIX                            | `fix`                                                                          |
| Fortran                        | `fortran`, `f90`, `f95`                                                        |
| G-Code                         | `gcode`, `nc`                                                                  |
| Gams                           | `gams`, `gms`                                                                  |
| GAUSS                          | `gauss`, `gss`                                                                 |
| GDScript                       | `godot`, `gdscript`                                                            |
| Gherkin                        | `gherkin`                                                                      |
| GN for Ninja                   | `gn`、`gni`                                                                    |
| Go                             | `go`, `golang`                                                                 |
| Golo                           | `golo`, `gololang`                                                             |
| Gradle                         | `gradle`                                                                       |
| Groovy                         | `groovy`                                                                       |
| HTML                           | `html`, `xhtml`                                                                |
| HTTP                           | `http`, `https`                                                                |
| Haml                           | `haml`                                                                         |
| 把手                     | `handlebars`, `hbs`, `html.hbs`, `html.handlebars`                             |
| Haskell                        | `haskell`, `hs`                                                                |
| Haxe                           | `haxe`, `hx`                                                                   |
| Hy                             | `hy`, `hylang`                                                                 |
| Ini                            | `ini`                                                                          |
| Inform7                        | `inform7`, `i7`                                                                |
| IRPF90                         | `irpf90`                                                                       |
| JSON                           | `json`                                                                         |
| Java                           | `java`, `jsp`                                                                  |
| JavaScript                     | `javascript`, `js`, `jsx`                                                      |
| Kotlin                         | `kotlin`、`kt`                                                                 |
| Kusto                          | `kusto`                                                                        |
| 叶                           | `leaf`                                                                         |
| 套索                          | `lasso`, `ls`, `lassoscript`                                                   |
| Less                           | `less`                                                                         |
| LDIF                           | `ldif`                                                                         |
| Lisp                           | `lisp`                                                                         |
| LiveCode Server                | `livecodeserver`                                                               |
| LiveScript                     | `livescript`, `ls`                                                             |
| Lua                            | `lua`                                                                          |
| 生成文件                       | `makefile`, `mk`, `mak`                                                        |
| Markdown                       | `markdown`, `md`, `mkdown`, `mkd`                                              |
| Mathematica                    | `mathematica`, `mma`, `wl`                                                     |
| Matlab                         | `matlab`                                                                       |
| Maxima                         | `maxima`                                                                       |
| Maya Embedded Language         | `mel`                                                                          |
| Mercury                        | `mercury`                                                                      |
| mIRC Scripting Language        | `mirc`, `mrc`                                                                  |
| Mizar                          | `mizar`                                                                        |
| 托管对象格式          | `mof`                                                                          |
| Mojolicious                    | `mojolicious`                                                                  |
| Monkey                         | `monkey`                                                                       |
| Moonscript                     | `moonscript`、`moon`                                                           |
| MS Graph (Interactive)         | `msgraph-interactive`                                                          |
| N1QL                           | `n1ql`                                                                         |
| NSIS                           | `nsis`                                                                         |
| Nginx                          | `nginx`、`nginxconf`                                                           |
| Nimrod                         | `nimrod`, `nim`                                                                |
| Nix                            | `nix`                                                                          |
| OCaml                          | `ocaml`, `ml`                                                                  |
| Objective C                    | `objectivec`, `mm`, `objc`, `obj-c`                                            |
| OpenGL Shading Language        | `glsl`                                                                         |
| OpenSCAD                       | `openscad`, `scad`                                                             |
| Oracle Rules Language          | `ruleslanguage`                                                                |
| Oxygene                        | `oxygene`                                                                      |
| PF                             | `pf`, `pf.conf`                                                                |
| PHP                            | `php`, `php3`, `php4`, `php5`, `php6`                                          |
| Parser3                        | `parser3`                                                                      |
| Perl                           | `perl`, `pl`, `pm`                                                             |
| Plaintext no highlight         | `plaintext`                                                                    |
| Pony                           | `pony`                                                                         |
| PostgreSQL & PL/pgSQL          | `pgsql`, `postgres`, `postgresql`                                              |
| PowerShell                     | `powershell`, `ps`                                                             |
| PowerShell (Interactive)       | `powershell-interactive`                                                       |
| Processing                     | `processing`                                                                   |
| Prolog                         | `prolog`                                                                       |
| 属性                     | `properties`                                                                   |
| 协议缓冲区               | `protobuf`                                                                     |
| Puppet                         | `puppet`, `pp`                                                                 |
| Python                         | `python`, `py`, `gyp`                                                          |
| Python profiler results        | `profile`                                                                      |
| Q#                             | `qsharp`                                                                       |
| Q                              | `k`、`kdb`                                                                     |
| QML                            | `qml`                                                                          |
| R                              | `r`                                                                            |
| Razor CSHTML                   | `cshtml`, `razor`, `razor-cshtml`                                              |
| ReasonML                       | `reasonml`, `re`                                                               |
| RenderMan RIB                  | `rib`                                                                          |
| RenderMan RSL                  | `rsl`                                                                          |
| Roboconf                       | `graph`、`instances`                                                           |
| Robot Framework                | `robot`, `rf`                                                                  |
| RPM spec files                 | `rpm-specfile`, `rpm`, `spec`, `rpm-spec`, `specfile`                          |
| Ruby                           | `ruby`, `rb`, `gemspec`, `podspec`, `thor`, `irb`                              |
| Rust                           | `rust`、`rs`                                                                   |
| SAS                            | `SAS`, `sas`                                                                   |
| SCSS                           | `scss`                                                                         |
| SQL                            | `sql`                                                                          |
| STEP Part 21                   | `p21`, `step`, `stp`                                                           |
| Scala                          | `scala`                                                                        |
| Scheme                         | `scheme`                                                                       |
| Scilab                         | `scilab`, `sci`                                                                |
| Shape Expressions              | `shexc`                                                                        |
| Shell                          | `shell`, `console`                                                             |
| Smali                          | `smali`                                                                        |
| Smalltalk                      | `smalltalk`, `st`                                                              |
| Solidity                       | `solidity`, `sol`                                                              |
| Stan                           | `stan`                                                                         |
| Stata                          | `stata`                                                                        |
| Structured Text                | `iecst`, `scl`, `stl`, `structured-text`                                       |
| 触笔                         | `stylus`, `styl`                                                               |
| SubUnit                        | `subunit`                                                                      |
| Supercollider                  | `supercollider`, `sc`                                                          |
| Swift                          | `swift`                                                                        |
| Tcl                            | `tcl`, `tk`                                                                    |
| Terraform (HCL)                | `terraform`, `tf`, `hcl`                                                       |
| Test Anything Protocol         | `tap`                                                                          |
| TeX                            | `tex`                                                                          |
| Thrift                         | `thrift`                                                                       |
| TOML                           | `toml`                                                                         |
| TP                             | `tp`                                                                           |
| Twig                           | `twig`、`craftcms`                                                             |
| TypeScript                     | `typescript`, `ts`                                                             |
| VB.NET                         | `vbnet`, `vb`                                                                  |
| VBScript                       | `vbscript`, `vbs`                                                              |
| VHDL                           | `vhdl`                                                                         |
| Vala                           | `vala`                                                                         |
| Verilog                        | `verilog`, `v`                                                                 |
| Vim Script                     | `vim`                                                                          |
| X++                            | `xpp`                                                                          |
| x86 Assembly                   | `x86asm`                                                                       |
| XL                             | `xl`, `tao`                                                                    |
| XQuery                         | `xquery`, `xpath`, `xq`                                                        |
| XAML                           | `xaml`                                                                         |
| XML                            | `xml`, `xhtml`, `rss`, `atom`, `xjb`, `xsd`, `xsl`, `plist`                    |
| YAML                           | `yml`, `yaml`                                                                  |
| Zephir                         | `zephir`, `zep`                                                                |

> [!TIP]
> 当多个别名可用时，Docs 创作包的[开发语言完成功能](docs-authoring/dev-lang-completion.md)使用第一个有效别名。

## <a name="next-steps"></a>后续步骤

要了解内容类型（代码除外）的文本格式设置，请参阅[文本格式设置准则](text-formatting-guidelines.md)。
