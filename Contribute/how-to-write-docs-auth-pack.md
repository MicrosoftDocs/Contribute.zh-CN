---
title: 适用于 Visual Studio Code 的 Docs 创作包
description: 本文介绍了 Visual Studio Code 的扩展包，用于辅助 docs.microsoft.com 的 Markdown 创作。
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
author: meganbradley
ms.author: mbradley
ms.date: 03/05/2020
ms.openlocfilehash: 5bbf51af52069d5636715ffb2bd3f59bf459d5b9
ms.sourcegitcommit: cfba5ad25b898bfed76046126ce8ff4871910701
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/04/2020
ms.locfileid: "78336397"
---
# <a name="docs-authoring-pack-for-vs-code"></a>用于 VS Code 的 Docs 创作包

Docs 创作包是 VS Code 扩展的集合，用于辅助 docs.microsoft.com 的 Markdown 创作。 此包[可在 VS Code Marketplace 中获得](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack)，包含以下扩展：

> [!div class="checklist"]
> * [Docs Markdown](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown)：为 docs.microsoft.com (Docs) 内容提供 Markdown 创作帮助，包括基本的 Markdown 支持和对 Docs 中自定义 Markdown 语法的支持，例如警报、代码片段和非本地化文本。 现在还包括一些基本 YAML 创作帮助，例如插入 TOC 条目。
> * [markdownlint](https://marketplace.visualstudio.com/items?itemName=DavidAnson.vscode-markdownlint)：David Anson 推出的一种非常受欢迎的 Markdown Linter，可帮助确保 Markdown 有效。
> * [代码拼写检查器](https://marketplace.visualstudio.com/items?itemName=streetsidesoftware.code-spell-checker)：Street Side Software 推出的完全脱机的拼写检查器。
> * [Docs 预览](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-preview)：使用 docs.microsoft.com CSS 可进行更准确的 Markdown 预览，包括自定义 Markdown。
> * [Docs 文章模板](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-article-templates)：允许用户搭建 Learn 模块基架以及将 Markdown 框架内容应用于新文件。
> * [Docs YAML](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-yaml)：提供 Docs YAML 架构验证和自动完成。
> * [Docs 图像](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-images):提供图像压缩和重新调整文件夹和单个文件大小的功能，为 docs.microsoft.com 的作者提供帮助。

## <a name="prerequisites-and-assumptions"></a>前提条件和假设

要使用 Docs Markdown 扩展插入相关链接、图像和其他嵌入内容，必须将 VS Code 工作区的范围限定于所克隆的公开发布系统 (OPS) 存储库的根路径。 例如，如果已将文档存储库克隆到 `C:\git\SomeDocsRepo\`，请在 VS Code 中打开该文件夹或子文件夹：选择“文件” > “打开文件夹”菜单，或使用命令行中的 `code C:\git\SomeDocsRepo\`。

扩展支持的一些语法（如警报和片段）是 OPS 的自定义 Markdown。 除非已通过 OPS 发布，否则将无法正确呈现自定义 Markdown。

## <a name="how-to-use-the-docs-markdown-extension"></a>如何使用 Docs Markdown 扩展

要访问 Docs Markdown 菜单，请键入 <kbd>ALT+M</kbd>。 可单击或使用上下箭头来选择所需的命令。 或者，可键入内容以开始筛选，然后当你所需的功能在菜单中突出显示时按 <kbd>Enter</kbd>。

请参阅 [Docs Markdown 自述文件](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown)以获取最新的命令列表。

## <a name="how-to-generate-a-master-redirect-file"></a>如何生成主重定向文件

Docs Markdown 扩展包括一个脚本，用于基于单个文件中的 `redirect_url` 元数据生成或更新存储库的主重定向文件。 此脚本可检查存储库中每个 Markdown 文件是否具有 `redirect_url`、将重定向元数据添加到存储库的主重定向文件 (.openpublishing.redirection.json)，还可将已重定向的文件移至存储库以外的文件夹。 要运行脚本，请执行以下操作：

1. 选择 <kbd>F1</kbd> 打开 VS Code 命令面板。
2. 开始键入“Docs:生成…”
3. 选择命令 `Docs: Generate master redirection file`。
4. 该脚本完成运行后，重定向结果将显示在 VS Code 输出窗格中，并且已删除的 Markdown 文件将添加到默认路径下的 Docs Authoring\redirects 文件夹中。
5. 查看结果。 如果结果与预期一样，请提交拉取请求以更新存储库。

## <a name="how-to-assign-keyboard-shortcuts"></a>如何分配键盘快捷方式

1. 依次键入 <kbd>Ctrl+K</kbd> 和 <kbd>Ctrl+S</kbd>，打开键盘快捷方式列表。
1. 搜索要创建自定义键绑定的命令，例如 `formatBold`。
1. 鼠标悬停在该行上时，单击命令名称旁边出现的加号。
1. 在显示新的输入框后，键入想要绑定到特定命令的键盘快捷方式。 例如，要将常见快捷方式用于加粗操作，则键入 <kbd>Ctrl+B</kbd>。
1. 在键绑定中插入 `when` 子句是个不错的主意，这样便无法在 Markdown 以外的文件中使用该快捷方式。 为此，请打开 keybindings.json，在命令名称下方插入以下行（请确保在行之间添加逗号）：

    `"when": "editorTextFocus && editorLangId == 'markdown'"`

    自定义键绑定完成后，在 keybindings.json 中看起来应如下所示：

    ```json
    [
        {
            "key": "ctrl+b",
            "command": "formatBold",
            "when": "editorTextFocus && editorLangId == 'markdown'"
        }
    ]
    ```

    > [!TIP]
    > 将键绑定放在此文件中以覆盖默认值

1. 保存 keybindings.json。

有关键绑定的详细信息，请参阅 [VS Code 文档](https://code.visualstudio.com/docs/getstarted/keybindings)。

## <a name="how-to-show-the-legacy-gauntlet-toolbar"></a>如何显示旧的“Gauntlet”工具栏

名为“Gauntlet”的扩展代码的前用户会注意到，安装 Docs Markdown 扩展时，在 VS Code 窗口的底部不再显示创作工具栏。 这是因为工具栏占据了 VS Code 状态栏的大量空间，而且未遵循扩展 UX 的最佳做法，因此在新扩展中被弃用。 但是，可以通过更新 VS Code settings.json 文件来选择性地显示工具栏，如下所示：

1. 在 VS Code 中，转到“文件” > “首选项” > “设置”，或者选择 <kbd>Ctrl+,</kbd>。
1. 选择“用户设置”，更改所有 VS Code 工作区的设置，或选择“工作区设置”，更改当前工作区的相关设置。
1. 选择“扩展” > “Docs Markdown 扩展配置”，然后选择“在底部状态栏中显示旧工具栏”。

   ![在 VS Code 中显示旧工具栏设置](docs-authoring/media/show-gauntlet-bar.png)

做出选择后，VS Code 会更新 settings.json 文件。 系统将提示你重新加载窗口，以使更改生效。

添加到扩展的更新的命令在工具栏中不可用。

## <a name="how-to-use-docs-templates"></a>如何使用 Docs 模板

使用 Docs 文章模板扩展，VS Code 中的编写者可以从集中存储中提取 Markdown 模板并将其应用到文件。 模板可帮助确保文章中包含所需的元数据、遵循内容标准等。 在公共 GitHub 存储库中，模板作为 Markdown 文件进行管理。

### <a name="to-apply-a-template-in-vs-code"></a>在 VS Code 中应用模板

1. 请确保已安装和启用 Docs 文章模板扩展。
1. 如果没有安装 Docs Markdown 扩展，请单击 <kbd>F1</kbd> 打开命令面板，开始键入“template”进行筛选，然后单击 `Docs: Template`。 如果安装了 Docs Markdown，则可以使用命令面板，也可以单击 <kbd>Alt+M</kbd> 以显示 Docs Markdown QuickPick 菜单，然后从列表中选择 `Template`。
1. 从显示的列表中选择所需的模板。

### <a name="to-add-your-github-id-andor-microsoft-alias-to-your-vs-code-settings"></a>将 GitHub ID 和/或 Microsoft 别名添加到 VS Code 设置中

Templates 扩展支持三个动态元数据字段：author、ms.author 和 ms.date。 这意味着，如果模板创建者在 Markdown 模板的元数据标头中使用这些字段，则在应用模板时，它们将在你的文件中自动填充，如下所示：

| 元数据字段 | 值 |
|--|--|
| `author` | 你的 GitHub 别名（如果在 VS Code 设置文件中指定）。 |
| `ms.author` | 你的 Microsoft 别名（如果在 VS Code 设置文件中指定）。 如果你不是 Microsoft 员工，请不要指定该字段。 |
| `ms.date` | 采用 Docs 支持的格式 (`MM/DD/YYYY`) 的当前日期。 如果之后更新文件，则不会自动更新日期 - 必须手动更新。 此字段用于表示“文章新鲜度”。 |

### <a name="to-set-author-andor-msauthor"></a>设置 author 和/或 ms.author

1. 在 VS Code 中，转到“文件” > “首选项” > “设置”，或者选择 <kbd>Ctrl+,</kbd>。
1. 选择“用户设置”，更改所有 VS Code 工作区的设置，或选择“工作区设置”，更改当前工作区的相关设置。
1. 在左侧的“默认设置”窗格中，找到“Docs 文章模板扩展配置”，单击所需设置旁边的铅笔图标，然后单击“设置”中的“替换”。
1. “用户设置”窗格将并排打开，底部附带一个新条目。
1. 根据需要，添加 GitHub ID 或 Microsoft 电子邮件别名，然后保存该文件。
1. 可能需要关闭并重启 VS Code 才能使更改生效。
1. 现在，在应用使用动态字段的模板时，你的 GitHub ID 和/或 Microsoft 别名自动填充到元数据标头中。

### <a name="to-make-a-new-template-available-in-vs-code"></a>生成可在 VS Code 中使用的新模板

1. 将模板起草为 Markdown 文件。
1. 将拉取请求提交到 [MicrosoftDocs/content-templates](https://github.com/MicrosoftDocs/content-templates) 存储库的模板文件夹中。

docs.microsoft.com 团队会查看你的模板，并在该模板符合 docs.microsoft.com 风格指南的情况下合并 PR。 合并后，该模板将可供 Docs 文章模板扩展的所有用户使用。

## <a name="demo-several-features"></a>演示多种功能

下面是一个简短的视频，演示了 Docs 创作包的以下功能：

* **YAML 文件**
  * 支持“Docs:链接到存储库中的文件”
* **Markdown 文件**
  * 更新“ms.date”元数据值上下文菜单选项
  * 代码自动完成支持代码隔离语言标识符
  * 无法识别的代码隔离语言标识符警告/自动更正支持
  * 按升序对所选内容进行排序（A 到 Z）
  * 按降序对所选内容进行排序（Z 到 A）

> [!VIDEO https://www.youtube.com/embed/6zfbBRdjlw8]

## <a name="contribution-expectations"></a>参与预期

Docs 创作包扩展是开放源代码，供具有 GitHub 帐户的任何人参与。 有一个专门的 Microsoft 内部团队积极处理此项目。 该团队会监视问题和拉取请求。 服务级别协议 (SLA) 问题目前一周解决，且目前有望一周内审阅拉取请求。 该团队正在努力实现自动化，以缩短这一周转时间。

## <a name="next-steps"></a>后续步骤

了解 Docs 创作包 Visual Studio Code 扩展中可用的各种功能。

* [开发语言完成](docs-authoring/dev-lang-completion.md)
* [图像压缩](docs-authoring/image-compression.md)
* [元数据更新](docs-authoring/metadata-updates.md)
* [重新设置表格式](docs-authoring/reformat-table.md)
* [智能引号替换](docs-authoring/smart-quote-replacement.md)
* [排序重定向](docs-authoring/sort-redirects.md)
* [排序所选内容](docs-authoring/sort-selection.md)
