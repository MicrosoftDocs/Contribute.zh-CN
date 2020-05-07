---
title: 参与 .NET 文档存储库撰写
description: 本文档介绍参与组成 .NET 文档的存储库中文章和代码示例撰写的过程。
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
ms.date: 11/07/2018
ms.openlocfilehash: d97d72e8458a53ab11b01cbd4bb5df3b8458b048
ms.sourcegitcommit: cfba5ad25b898bfed76046126ce8ff4871910701
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/04/2020
ms.locfileid: "81784315"
---
# <a name="learn-how-to-contribute-to-the-net-docs-repositories"></a>了解如何参与 .NET 文档存储库撰写

感谢你有兴趣参与 .NET 文档撰写！

本文档介绍参与托管在 [.NET 文档站点](https://docs.microsoft.com/dotnet)上的文章和代码示例撰写的过程。 参与供稿可能像更正拼写错误一样简单，也可能像撰写新文章一样复杂。

.NET 文档站点根据多个存储库生成：

- [.NET 概念性文章](https://github.com/dotnet/docs)
- [代码示例和代码片段](https://github.com/dotnet/samples)
- [.NET Standard、.NET Core、.NET Framework API 参考](https://github.com/dotnet/dotnet-api-docs)
- [.NET Compiler Platform SDK 参考](https://github.com/dotnet/roslyn-api-docs)
- [ML.NET API 参考](https://github.com/dotnet/ml-api-docs)

在 [dotnet/docs](https://github.com/dotnet/docs/issues) 存储库中跟踪所有上述存储库的问题。

## <a name="guidelines-for-contributions"></a>参与原则

感谢社区参与文档撰写。以下列表显示部分参与 .NET 文档撰写时应记住的指导规则：

- 请**勿**向我们提出大量拉取请求。 相反，提出问题并发起讨论，在我们认同这一方向后你再投入大量的时间。
- 请**务必**遵循这些说明以及[语音语调](dotnet-voice-tone.md)准则。
- 请**务必**使用[模板](dotnet-style-guide.md)文件，作为工作的出发点。
- 处理文章前，请**务必**在分支上创建单独的分支。
- 请**务必**遵循 [GitHub 流工作流](https://guides.github.com/introduction/flow/)。
- 请**务必**频繁发布有关参与的博客和推文（或者诸如此类）！

遵循这些指南可确保你和我们都能获得更好的体验。

## <a name="make-a-contribution-to-net-docs"></a>参与 .NET 文档撰写

**步骤 1：** 对于小更改，请跳过此步骤。 如果有兴趣编写新内容或仔细修订现有内容，请创建描述你想做的事情的[问题](https://github.com/dotnet/docs/issues)。

“Docs”文件夹中的内容组织成部分，在目录 (TOC) 中进行反映。 定义主题在 TOC 中所处的位置。 获取有关建议的反馈。

-或-

你还可以从现有问题中选择，欢迎参与社区讨论。 [适用于 .NET 社区参与者的项目](https://github.com/dotnet/docs/projects/35)列出了适用于社区参与者的诸多问题。 根据你的兴趣和承诺级别，可以从以下类别的问题中进行选择：

- **维护**。 此类别包括相当简单的参与，例如，修复断裂或错误的链接，添加缺少的代码示例或解决受限内容问题。 在某些情况下，这些问题可能涉及大量文件。 届时，你应在开始前告知我们想要处理的内容。 在问题上添加注释，以告知我们你正在处理。

- **内容更新**。 鉴于文档集的巨大性，内容很容易过时，需要修订。 此外，出于各种原因，部分内容发生重复，甚至出现一式三份现象。 更新内容涉及确保各个主题为最新，或修订特色区域中的内容以消除重复，以及确保所有独特的内容均保存在较小文档集中。

- **新内容创作**。 如果有兴趣创作自己的主题，这些问题列出了我们要向文档集添加的主题。 不过，请在处理某主题前，告知我们。 如果有兴趣编写此处未列出的主题，请创建一个问题。

此外，还可查看[未决问题](https://github.com/dotnet/docs/issues)列表，并自愿处理感兴趣的主题。 我们使用 [up-for-grabs](https://github.com/dotnet/docs/labels/up-for-grabs) 标签标记针对社区参与标识的问题。 这些通常需要最小上下文，并且非常适合首发问题。 我们鼓励社区中有经验的参与者查看感兴趣的任何问题。 如果找到问题，请添加评论，询问其是否未结。

选择要处理的任务后，请按照[入门](../get-started-setup-github.md)指南操作，创建 GitHub 帐户并设置环境。

**步骤 2：** 根据需要，创建 `/dotnet/docs`、`dotnet/samples`、`dotnet/dotnet-api-docs`、`dotnet/roslyn-api-docs` 或 `dotnet/ml-api-docs` 存储库的分支，并针对更改创建分支。

对于小更改，请在参与者指南的[主页](../index.md#quick-edits-to-existing-documents)中查看在 GitHub 中编辑的说明。

**步骤 3：** 在此新分支上进行更改。

如果它是新主题，则可以使用此[模板文件](dotnet-style-guide.md)，作为起始点。 它包含编写准则，并且还解释每篇文章需要的元数据（例如，作者信息）。

导航到对应针对步骤 1 中的文章确定的目录位置的文件夹。 该文件夹包含针对该部分中所有文章的 Markdown 文件。 如有必要，新建一个文件夹，放置存储内容的文件。 该部分的主要文章称为 index.md。 对于映像和其他静态资源，请在包含文章的文件夹中创建称为“media”的子文件夹（如果尚不存在）。 在“media”文件夹内，创建具有文章名称的子文件夹（索引文件除外）。 如有关[示例](#contributing-to-samples)的部分中所述，代码示例应位于 `dotnet/samples` 存储库中。

请务必遵循适当的 Markdown 语法。 有关常见示例，请参阅[模板和标记速查表](dotnet-style-guide.md)。

## <a name="example-structure"></a>示例结构

    docs
      /about
      /core
        /porting
          porting-overview.md
          /media
            /porting-overview
                portability_report.png

**步骤 4：** 从分支向主分支提交拉取请求 (PR)。

> [!IMPORTANT]
> 任何 .NET 文档存储库中的[评论自动化](../how-to-write-workflows-major.md#review-and-sign-off)功能均暂不可用。 .NET 文档团队成员将评审和合并 PR。

每个 PR 通常一次只处理一个问题。 PR 可修改一个或多个文件。 如果要处理不同文件上的多个修复，首选单独的 PR。 如果要创建示例以及更新标记，则需要为示例创建单独的 PR。

如果 PR 可修复现有问题，请在提交消息或 PR 说明中添加 `Fixes #Issue_Number` 关键字。 如此，PR 合并时，问题将自动关闭。 有关详细信息，请参阅[通过提交消息关闭问题](https://help.github.com/articles/closing-issues-via-commit-messages/)。

.NET 团队将评审 PR 并告知你是否存在必需的其他任何更新/更改，以进行审批。

**步骤 5：** 与团队讨论时，对分支进行任何必需的更新。

反馈应用后且更改得到审批后，维护程序会将 PR 合并为主分支。

我们将定期从主分支将所有提交推送到实时分支，然后便能够在 https://docs.microsoft.com/dotnet/ 实时查看你的参与。 通常我们会在工作周期间每日发布。 发布可能因维护活动延迟数天。

## <a name="contributing-to-samples"></a>参与撰写示例

[dotnet/示例](https://github.com/dotnet/samples)存储库包含属于 .NET 文档下的任何主题的所有代码示例。 存在组织成子文件夹的多个不同项目。 这些子文件夹的组织方式类似于 .NET 文档的组织方式。

我们对存在于存储库中的代码进行以下区分：

- 示例：读者可以下载并运行示例。 所有示例都应是完整的应用程序或库。 如果示例创建库，该库应包括单元测试或允许读者运行代码的应用程序。 它们通常使用多种技术、功能或工具包。 每个示例的 readme.md 文件都将引用文章，使你能够深入了解每个示例中涉及的概念。
- 代码片段：说明较小概念或任务。 它们进行编译但不打算成为完整的应用程序。 它们应正常运行，但不是典型方案的示例应用程序。 相反，它们旨在尽可能小，以说明单个概念或功能。 这些应只是一个屏幕的代码。

所有代码均位于 [dotnet/示例](https://github.com/dotnet/samples)存储库中。 我们正在努力构建一个模型，其中示例文件夹结构匹配文档文件夹结构。 所遵循的标准有：

- 顶层“snippets”文件夹包含小型、重点示例的代码片段。
- API 引用示例位于遵循此模式的文件夹中：snippets/\<>/api/\<namespace>/\<apiname>。
- 其他顶层文件夹与文档存储库中的顶层文件夹匹配。 例如，文档存储库包含“machine-learning/tutorials”文件夹，并且机器学习教程的示例位于“samples/machine-learning/tutorials”文件夹中。

此外，核心和标准文件夹下的所有示例都应在 .NET Core 支持的所有平台上生成并运行。 CI 生成系统将强制执行该操作。 顶层“framework”文件夹包含仅在 Windows 上生成和验证的示例。

示例项目应在针对给定示例可能的最广泛的一组平台上生成和运行。 实际上，这表示在可能的位置生成基于 .NET Core 的控制台应用程序。 特定于 Web 或 UI 框架的示例应根据需要添加这些工具。 示例有 Web 应用程序、移动应用、WPF 或 WinForms 应用等。

我们正在努力实现适用于所有代码的 CI 系统。 当对示例进行任何更新时，请确保每个更新都属于可生成项目。 理想情况下，还可添加针对示例正确性的测试。

创建的每个完整示例都应包含 readme.md 文件。 此文件应包含有关示例的简短说明（一到两个段落）。 Readme.md 应告知读者通过浏览此示例，可以学到什么内容。 此外，readme.md 文件还应包含一个链接，指向 [.NET 文档站点](https://docs.microsoft.com/dotnet/welcome)上的实时文档。 若要确定存储库中给定文件映射到该站点的位置，请将存储库路径中的 `/docs` 替换为 `https://docs.microsoft.com/dotnet`。

此外，主题还将包含指向该示例的链接。 直接链接到 GitHub 上的示例文件夹。

### <a name="writing-a-new-snippet-or-sample"></a>编写新的代码片段或示例

1. 示例必须属于可生成项目的一部分。 如果可能，应在 .NET Core 支持的所有平台上生成项目。 此情况的例外是演示平台特定功能或平台特定工具的示例。

2. 示例应符合 [corefx 编码样式](https://github.com/dotnet/corefx/blob/master/Documentation/coding-guidelines/coding-style.md)，以保持一致性。

    - 此外，演示不需要初始化新对象的内容时，我们首选 `static` 方法，而不是实例方法。

3. 示例应包括适当的异常处理。 它应处理可能在示例的上下文中引发的所有异常。 例如，当输入字符串以参数形式传递给方法时，调用 [Console.ReadLine](https://docs.microsoft.com/dotnet/api/system.console.readline) 方法以检索用户输入的示例应使用适当的异常处理。 同样，如果示例需要方法调用失败，则必须处理导致的异常。 请始终处理方法引发的特定异常，而不是基类异常，例如 [Exception](https://docs.microsoft.com/dotnet/api/system.exception) 或 [SystemException](https://docs.microsoft.com/dotnet/api/system.systemexception)。

4. 如果示例生成独立包，除示例所用的任何运行时外，还必须包含 CI 生成系统所用的运行时：
    - `win7-x64`
    - `win8-x64`
    - `win81-x64`
    - `ubuntu.16.04-x64`

我们将提供一个 CI 系统，以暂时生成这些项目。

创建示例：

1. 提交[问题](https://github.com/dotnet/docs/issues)，或向正在处理的现有问题添加注释。
2. 编写解释示例中演示的概念的主题（例如：`docs/standard/linq/where-clause.md`）。
3. 编写示例（例如：`WhereClause-Sample1.cs`）。
4. 使用调用示例的主要入口点创建 Program.cs。 如果已有一个，则添加对示例的调用：

    ```csharp
    public class Program
    {
        public void Main(string[] args)
        {
            WhereClause1.QuerySyntaxExample();

            // Add the method syntax as an example.
            WhereClause1.MethodSyntaxExample();
        }
    }
    ```

使用 .NET Core CLI 生成任何 .NET Core 代码片段或示例，可与 [.NET Core SDK](https://www.microsoft.com/net/download) 一起安装。 生成并运行示例：

1. 转到示例文件夹和生成，查看其中的错误：

    ```console
    dotnet build
    ```
2. 运行示例：

    ```console
    dotnet run
    ```

3. 向示例的根目录添加 readme.md。

   这应包括代码的简短说明，并使用户参考引用该示例的文章。

备注除外，所有示例均通过 .NET Core 支持的任何平台上的命令行生成。 有一些特定于 Visual Studio 的示例，需要 Visual Studio 2017 或更高版本。 此外，部分示例还展示了平台特定的功能，并且需要特定的平台。 其他示例和代码片段需要 .NET Framework，且将在 Windows 平台上运行，需要适用于目标 Framework 版本的开发人员工具包。

## <a name="the-c-interactive-experience"></a>C# 交互式体验

文章中包括的所有示例均使用[语言标记](../code-in-docs.md)指示源语言。 采用 C# 的短代码示例可使用 `csharp-interactive` 语言标记指定在浏览器中运行的 C# 示例。 （内联代码示例使用 `csharp-interactive` 标记，对于源中包括的代码示例，请使用 `code-csharp-interactive` 标记。）这些代码示例在文中显示一个代码窗口和一个输出窗口。 输出窗口显示用户运行示例后，执行交互式代码的任何输出。

C# 交互式体验改变了我们使用示例的方式。 访问者可运行示例，查看结果。 有许多因素有助于确定示例或对应的文本是否应包括输出的相关信息。

### <a name="when-to-display-the-expected-output-without-running-the-sample"></a>何时显示预期输出，而无需运行示例

- 针对初学者的文章应提供输出，以便读者可将其工作的输出与预期答案进行比较。
- 其中的输出对主题至关重要的示例应显示该输出。 例如，有关格式化文本的文章应显示格式，而无需运行示例。
- 如果示例和预期输出均简短，请考虑显示输出。 可节省一些时间。
- 介绍当前区域性或固定区域性如何影响输出的文章应介绍预期输出。 交互式 REPL（读取–求值–打印循环）在基于 Linux 的主机上运行。 默认区域性和固定区域性在不同的操作系统和计算机上可生成不同的输出。 文章应说明 Windows、Linux 和 Mac 系统中的输出。

### <a name="when-to-exclude-expected-output-from-the-sample"></a>何时从示例中排除预期输出

- 其中的示例生成较大输出的文章不应在注释中包括该内容。 示例运行后，它将使代码难以理解。
- 其中的示例演示主题的文章，但输出对理解该文章不甚重要。 例如，运行 LINQ 查询以说明查询语法的代码，然后该代码显示输出集合中的每个项。

> [!NOTE]
> 你可能已注意到，部分主题当前不遵循此处指定的所有准则。 我们正在努力实现整个网站中的一致性。 查看我们目前正在针对该特定目标跟踪的[未决问题](https://github.com/dotnet/docs/issues?q=is%3Aopen+is%3Aissue+label%3A%22%3Abookmark_tabs%3A+Information+Architecture%22)列表。

### <a name="contributing-to-international-content"></a>参与全球内容   

当前不接受参与机器翻译 (MT) 内容。 为了提高 MT 内容的质量，我们进行了转换，现使用神经 MT 引擎。 我们接受并鼓励参与人工翻译 (HT) 内容，该内容用来训练神经 MT 引擎。 随着时间的推移，对 HT 内容的参与将提高 HT 和 MT 这两者的质量。 MT 主题将包含一条免责声明，其中指出主题的一部分可能是机器翻译，而由于已禁止编辑，因此将不显示“编辑”按钮。   

## <a name="contributor-license-agreement"></a>参与者许可协议

在合并 PR 前，必须先签署 [.NET Foundation 参与许可协议 (CLA)](https://cla.dotnetfoundation.org)。 这是针对 .NET Foundation 中的项目的一次性要求。 可在 Wikipedia 上了解有关[参与许可协议 (CLA)](http://en.wikipedia.org/wiki/Contributor_License_Agreement) 的详细信息。

协议：[net-foundation-contribution-license-agreement.pdf](https://github.com/dotnet/home/blob/master/guidance/net-foundation-contribution-license-agreement.pdf)

无需提前签署协议。 可以照常克隆 PR、创建 PR 分支或提交 PR。 创建 PR 时，由 CLA 机器人进行分类。 如果更改较小（例如，修复拼写错误），则 PR 将标记为 `cla-not-required`。 否则，它将被分类为 `cla-required`。 签署 CLA 后，当前和将来的所有拉取请求都将被标记为 `cla-signed`。
