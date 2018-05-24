---
title: 用于 VS Code 的 Docs 创作包
description: 本文介绍了 VS Code 的扩展包，用于辅助 docs.microsoft.com 的 Markdown 创作。
author: meganbradley
ms.author: mbradley
manager: jemash
ms.date: 04/06/2018
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.custom: external-contributor-guide
ms.openlocfilehash: d0d61db2faf88598ecd2c800fb5fbe8df8ec44f5
ms.sourcegitcommit: e046e7aad8ed22bffe5380d63a9d40f0baeecc57
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/22/2018
---
# <a name="docs-authoring-pack-for-vs-code"></a>用于 VS Code 的 Docs 创作包

Docs 创作包是 VS Code 扩展的集合，用于辅助 docs.microsoft.com 的 Markdown 创作。此包[可在 VS Code Marketplace 中获得](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack)，包含以下扩展：

- **DocFx：** 提供特定于 docs.microsoft.com 的 Markdown 预览。 有关详细信息，请参阅 [DocFx](https://marketplace.visualstudio.com/items?itemName=ms-docfx.DocFX)。
- **markdownlint：** David Anson 推出的一种非常受欢迎的 Markdown Linter，可帮助确保 Markdown 遵循最佳做法。 有关详细信息，请参阅 [markdownlint](https://marketplace.visualstudio.com/items?itemName=DavidAnson.vscode-markdownlint)。
- **Docs Markdown：** 为公开发布系统(OPS) 中的 docs.microsoft.com 内容提供 Markdown 创作帮助，包括基本的 Markdown 支持和对 OPS 中自定义 Markdown 语法的支持。 此主题的其余部分介绍了 Docs Markdown 扩展。

## <a name="prerequisites-and-assumptions"></a>前提条件和假设

要使用 Docs Markdown 扩展正确插入相关链接、图像和其他嵌入内容，则必须将 VS Code 工作区的范围限定于克隆 OPS 存储库的根路径。

扩展支持的一些语法（如警报和片段）是 OPS 的自定义 Markdown，除非已通过 OPS 发布，否则将无法正确呈现。

## <a name="how-to-use-the-docs-markdown-extension"></a>如何使用 Docs Markdown 扩展

要访问 Docs Markdown 菜单，请键入 `ALT+M`。 可以单击或使用向上/向下箭头选择想要的功能，或通过键入来启用筛选，当想要的功能在菜单中突出显示时，点击 `ENTER`。 以下是可用的功能：

|功能     |命令             |说明           |
|-------------|--------------------|----------------------|
|粗体         |`formatBold`        |格式文本为粗体。|
|斜体       |`formatItalic`      |格式文本为斜体。|
|代码         |`formatCode`        |如果选择一行或不到一行，则将文本格式设置为 `inline code`。<br><br>如果选择多行，则将这些行的格式设置为隔离代码块，并允许选择 OPS 支持的编程语言。|
|警报        |`insertAlert`       |插入备注、重要说明、警告或提示。<br><br>从菜单选择警报，然后选择警报类型。 如果之前已选择文本，则所选警报语法将包围该文本。 如果没有选择任何文本，则使用占位符文本添加新的警报。|
|编号列表|`insertNumberedList` |插入新的编号列表。<br><br> 如果已选择多行，则每行都是列表项。 请注意，编号列表在 Markdown 中全显示为 1，但在 docs.microsoft.com 上则显示为序号，如果是嵌套列表，则显示为字母。 要创建嵌套编号列表，请在父列表中制表。|
|项目符号列表|`insertBulletedList` |插入新的项目符号列表。|
|表格        |`insertTable`        |插入 Markdown 表格结构。<br><br>在选择表格命令后，请按列:行（例如 3:4）的格式，指定列数和行数。 请注意，通过此扩展指定的列数的最大值为 5。由于考虑到可读性，因此建议采用该最大值。|
|链接         |`selectLinkType`      |插入链接。 选择此命令时，将出现以下子菜单。<br><br>`External`：通过 URI 链接到网页。 必须包含“http”或“https”。<br>`Internal`：将相关链接插入到相同存储库中的其他文件。 选择此选项后，在命令窗口键入，以按名称筛选文件，然后选择所需文件。 <br>`Bookmark in this file`：从当前文件的标题列表中进行选择，插入正确的格式书签。<br>`Bookmark in another file`：首先，按文件名称筛选并选择要链接到的文件，然后在已选定的文件中选择合适的标题。|
|图像        |`insertImage`     |键入（辅助功能需要的）替换文字并选中该文字，然后调用此命令来筛选存储库中支持的图像文件列表，选择所需图像文件。 如果在调用此命令时未选中替换文字，则在可以选择图像文件之前，会收到相关提示。|
|包括      |`insertInclude`   |查找要嵌入到当前文件的文件。|
|片段      |`insertSnippet`   |在存储库中查找代码片段以嵌入到当前文件。|
|视频        |`insertVideo`     |添加嵌入视频。|
|预览      |`previewTopic`    |使用 DocFX 扩展预览并行窗口中的活动主题。  如果未安装 DocFX 扩展或已安装但处于禁用状态，则不会呈现主题。


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

## <a name="how-to-show-the-legacy-gauntlet-toolbar"></a>如何显示旧的“Gauntlet”工具栏

名为“Gauntlet”的扩展代码的前用户会注意到，安装 Docs Markdown 扩展时，在 VS Code 窗口的底部不再显示创作工具栏。 这是因为工具栏占据了 VS Code 状态栏的大量空间并且不遵循扩展 UX 的最佳做法，因此在新扩展中将其弃用。 但是，可以通过更新 VS Code settings.json 文件来选择性地显示工具栏，如下所示：

1. 在 VS Code 中，转到文件 ->引用 ->设置 (`CTRL+Comma`)。
1. 选择“用户设置”，更改所有 VS Code 工作区的设置，或选择“工作区设置”，更改当前工作的相关设置。
1. 在“默认设置”窗格中，找到“Docs 创作扩展配置”，并选择所需设置旁的铅笔图标。 下一步，系统会提示选择 `true` 或 `false`。 作出选择后，VS Code 会自动将此值添加到 settings.json 文件中，并且会提示重新加载窗口以使更改生效。

## <a name="known-issues"></a>已知问题

- DocFX 预览：在 MacOS 和 Linux 上，DocFX 预览不能正确启动预览（这些平台的预览默认为 VS Code Markdown 预览）。
- DocFx 预览：在所有平台上，指向 API 的 xref（交叉引用）链接等某些语法在预览中无法正确呈现，有时还会留下空白内容。
- 外部书签：在 Linux 上会显示文件列表，但不显示可供选择的标题。
- 包括：在 Linux 上会显示文件列表，但选择后不添加任何链接。
