---
title: 适用于 Visual Studio Code 的 Docs 创作包
description: 本文介绍了 Visual Studio Code 的扩展包，用于辅助 docs.microsoft.com 的 Markdown 创作。
author: meganbradley
ms.author: mbradley
ms.date: 10/22/2018
ms.openlocfilehash: 00afafbbf16096ac6433c0ab276578d8d9084b51
ms.sourcegitcommit: d3c7b49dc854dae8da9cd49da8ac4035789a5010
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/23/2018
ms.locfileid: "49805645"
---
# <a name="docs-authoring-pack-for-vs-code"></a>用于 VS Code 的 Docs 创作包

Docs 创作包是 Visual Studio Code 扩展集合，用于辅助 docs.microsoft.com 的 Markdown 创作。 此包[可在 VS Code Marketplace 中获得](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack)，包含以下扩展：

- [markdownlint](https://marketplace.visualstudio.com/items?itemName=DavidAnson.vscode-markdownlint)：David Anson 推出的一种非常受欢迎的 Markdown Linter，可帮助确保 Markdown 遵循最佳做法。
- [代码拼写检查器](https://marketplace.visualstudio.com/items?itemName=streetsidesoftware.code-spell-checker)：Street Side Software 推出的完全脱机的拼写检查器。
- [Docs 预览](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-preview)：使用 docs.microsoft.com CSS 进行更准确的 Markdown 预览，包括自定义 Markdown。
- [Docs Markdown](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown)：为公开发布系统 (OPS) 中的 docs.microsoft.com 内容提供 Markdown 创作帮助，包括基本的 Markdown 支持和对 OPS 中自定义 Markdown 语法的支持。 此主题的其余部分介绍了 Docs Markdown 扩展。
- [Docs 文章模板](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-article-templates)：允许用户将 Markdown 框架内容应用于新文件。

## <a name="prerequisites-and-assumptions"></a>前提条件和假设

要使用 Docs Markdown 扩展正确插入相关链接、图像和其他嵌入内容，则必须将 VS Code 工作区的范围限定于克隆公开发布系统 (OPS) 存储库的根路径。

扩展支持的一些语法（如警报和片段）是 OPS 的自定义 Markdown，除非已通过 OPS 发布，否则将无法正确呈现。

## <a name="how-to-use-the-docs-markdown-extension"></a>如何使用 Docs Markdown 扩展

要访问 Docs Markdown 菜单，请键入 `ALT+M`。 可以单击或使用向上/向下箭头选择想要的功能，或通过键入来启用筛选，当想要的功能在菜单中突出显示时，点击 `ENTER`。 以下是可用的功能：

|功能     |说明           |
|-------------|----------------------|
|预览      |使用 Docs 预览扩展预览并行窗口中的活动主题。 此选项仅在安装 Docs 预览后可用。|
|粗体         |格式文本为粗体。|
|斜体       |格式文本为斜体。|
|代码         |如果选择一行或不到一行，则将文本格式设置为 `inline code`。<br><br>如果选择多行，则将这些行的格式设置为隔离代码块，并允许选择 OPS 支持的编程语言。|
|警报        |插入备注、重要说明、警告或提示。<br><br>从菜单选择警报，然后选择警报类型。 如果之前已选择文本，则所选警报语法将包围该文本。 如果没有选择任何文本，则使用占位符文本添加新的警报。|
|编号列表|插入新的编号列表。<br><br> 如果已选择多行，则每行都是列表项。 请注意，编号列表在 Markdown 中全显示为 1，但在 docs.microsoft.com 上则显示为序号，如果是嵌套列表，则显示为字母。 要创建嵌套编号列表，请在父列表中制表。|
|项目符号列表|插入新的项目符号列表。|
|表格        |插入 Markdown 表格结构。<br><br>在选择表格命令后，请按列:行（例如 3:4）的格式，指定列数和行数。 请注意，通过此扩展指定的列数的最大值为 5。由于考虑到可读性，因此建议采用该最大值。|
|链接到存储库中的文件|将相关链接插入到当前存储库中的其他文件。 选择此选项后，在命令窗口键入，以按名称筛选文件，然后选择所需文件。 如果之前选择了文本，它将成为链接文本。 否则，会将目标文件的 H1 用作链接文本。|
|链接到网页    |将链接插入到网页。 选择此选项后，将 URI 粘贴或键入到命令窗口。 `https://` 是必需的。 如果之前选择了文本，它将成为链接文本。 否则，将此 URI 用作链接文本。|
|链接到标题     |链接到当前文件中的书签或存储库中其他文件中的书签。<br>`Bookmark in this file`：从当前文件的标题列表中进行选择，插入正确的格式书签。<br>`Bookmark in another file`：首先，按文件名称筛选并选择要链接到的文件，然后在已选定的文件中选择合适的标题。|
|图像        |键入（辅助功能需要的）替换文字并选中该文字，然后调用此命令来筛选存储库中支持的图像文件列表，选择所需图像文件。 如果在调用此命令时未选中替换文字，则在可以选择图像文件之前，会收到相关提示。|
|包括      |查找要嵌入到当前文件的文件。|
|片段      |在存储库中查找代码片段以嵌入到当前文件。|
|视频        |添加嵌入视频。|
|模板     |创建新文件并应用 Markdown 模板。 有关详细信息，请参阅下面的[模板](#how-to-use-docs-templates)。|

## <a name="how-to-assign-keyboard-shortcuts"></a>如何分配键盘快捷方式

1. 依次键入 `CTRL+K` 和 `CTRL+S`，打开键盘快捷方式列表。
1. 搜索要创建自定义键绑定的命令，如 `formatBold`。
1. 鼠标悬停在该行上时，单击命令名称旁边出现的加号。
1. 在显示新的输入框后，键入想要绑定到特定命令的键盘快捷方式。 例如，要将常见快捷方式用于加粗操作，则键入 `ctrl+b`。
1. 在键绑定中插入 `when` 子句是个不错的主意，这样在 Markdown 以外的文件中就无法使用该快捷方式。 为此，请打开 keybindings.json，在命令名称下方插入以下行（请确保在行之间添加逗号）：
   
    `"when": "editorTextFocus && editorLangId == 'markdown'"`

    自定义键绑定完成后，在 keybindings.json 中看起来应如下所示：

    ```json
    // Place your key bindings in this file to overwrite the defaults
    [
        {
            "key": "ctrl+b",
            "command": "formatBold",
            "when": "editorTextFocus && editorLangId == 'markdown'"
        }
    ]
    ```

1. 保存 keybindings.json。

请参阅 VS Code docs 中的[键绑定](https://code.visualstudio.com/docs/getstarted/keybindings)，获取详细信息。

## <a name="how-to-show-the-legacy-toolbar"></a>如何显示旧工具栏

使用此扩展的预发布版本的用户会注意到，安装 Docs Markdown 扩展时，在 VS Code 窗口的底部不再显示创作工具栏。 这是因为工具栏占据了 VS Code 状态栏的大量空间并且不遵循扩展 UX 的最佳做法，因此在新扩展中将其弃用。 但是，可以通过更新 VS Code settings.json 文件来选择性地显示工具栏，如下所示：

1. 在 VS Code 中，转到文件 ->引用 ->设置 (`CTRL+Comma`)。
1. 选择“用户设置”，更改所有 VS Code 工作区的设置，或选择“工作区设置”，更改当前工作的相关设置。
1. 在“默认设置”窗格中，找到“Docs 创作扩展配置”，并选择所需设置旁的铅笔图标。 下一步，系统会提示选择 `true` 或 `false`。 作出选择后，VS Code 会自动将此值添加到 settings.json 文件中，并且会提示重新加载窗口以使更改生效。

## <a name="how-to-use-docs-templates"></a>如何使用 Docs 模板

使用 Docs 文章模板扩展，VS Code 中的编写者可以从集中存储中提取 Markdown 模板并将其应用到文件。 模板可帮助确保文章中包含所需的元数据、遵循内容标准等。 在公共 GitHub 存储库中，模板作为 Markdown 文件进行管理。

### <a name="to-apply-a-template-in-vs-code"></a>在 VS Code 中应用模板

1. 如果没有安装 Docs Markdown，请点击 F1 打开命令面板，开始键入“template”进行筛选，然后单击“`Docs: Template`”。 如果安装了 Docs Markdown，则可以使用命令面板，也可以单击“`Alt+M`”以显示 Docs Markdown QuickPick 菜单，然后从列表中选择“`Template`”。
1. 从显示的列表中选择所需的模板。

### <a name="to-add-your-github-id-andor-microsoft-alias-to-your-vs-code-settings"></a>将 GitHub ID 和/或 Microsoft 别名添加到 VS Code 设置中

Templates 扩展支持三个动态元数据字段：author、ms.author 和 ms.date。 这意味着，如果模板创建者在 Markdown 模板的元数据标头中使用这些字段，则在应用模板时，它们将在你的文件中自动填充，如下所示：

|元数据  |值|
|----------|---------------|
|author    |你的 GitHub ID（如果在 VS Code 设置文件中指定）。|
|ms.author |你的 Microsoft 别名（如果在 VS Code 设置文件中指定）。 如果你不是 Microsoft 员工，请不要指定该字段。|
|ms.date   |Docs 支持格式的当前日期，MM/DD/YYYY。 请注意，如果之后更新文件，则不会自动更新日期。 必须手动更新 ms.date 值以指示 docs.microsoft.com 站点上的最新发布日期。|

### <a name="to-set-author-github-id-andor-msauthor-microsoft-alias"></a>设置创建者 (GitHub ID) 和/或 ms.author（Microsoft 别名）

1. 在 VS Code 中，转到文件 ->引用 ->设置 (`CTRL+Comma`)。
1. 选择“用户设置”，更改所有 VS Code 工作区的设置，或选择“工作区设置”，更改当前工作区的相关设置。
1. 在左侧的“默认设置”窗格中，找到“Docs 文章模板扩展配置”，单击所需设置旁边的铅笔图标，然后单击“设置”中的“替换”。
1. “用户设置”窗格将并排打开，底部附带一个新条目。
1. 根据需要，添加 GitHub ID 或 Microsoft 电子邮件别名，然后保存该文件。
1. 可能需要关闭并重启 VS Code 才能使更改生效。
1. 现在，在应用使用动态字段的模板时，你的 GitHub ID 和/或 Microsoft 别名自动填充到元数据标头中。
