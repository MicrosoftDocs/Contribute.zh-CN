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
# <a name="docs-authoring-pack-for-vs-code"></a><span data-ttu-id="bf082-103">用于 VS Code 的 Docs 创作包</span><span class="sxs-lookup"><span data-stu-id="bf082-103">Docs Authoring Pack for VS Code</span></span>

<span data-ttu-id="bf082-104">Docs 创作包是 VS Code 扩展的集合，用于辅助 docs.microsoft.com 的 Markdown 创作。</span><span class="sxs-lookup"><span data-stu-id="bf082-104">The Docs Authoring Pack is a collection of VS Code extensions to aid with Markdown authoring for docs.microsoft.com.</span></span> <span data-ttu-id="bf082-105">此包[可在 VS Code Marketplace 中获得](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack)，包含以下扩展：</span><span class="sxs-lookup"><span data-stu-id="bf082-105">The pack is [available in the VS Code Marketplace](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack) and contains the following extensions:</span></span>

> [!div class="checklist"]
> * <span data-ttu-id="bf082-106">[Docs Markdown](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown)：为 docs.microsoft.com (Docs) 内容提供 Markdown 创作帮助，包括基本的 Markdown 支持和对 Docs 中自定义 Markdown 语法的支持，例如警报、代码片段和非本地化文本。</span><span class="sxs-lookup"><span data-stu-id="bf082-106">[Docs Markdown](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown): Provides Markdown authoring assistance for docs.microsoft.com (Docs) content, including basic Markdown support and support for custom Markdown syntax in Docs, such as alerts, code snippets, and non-localizable text.</span></span> <span data-ttu-id="bf082-107">现在还包括一些基本 YAML 创作帮助，例如插入 TOC 条目。</span><span class="sxs-lookup"><span data-stu-id="bf082-107">Now also includes some basic YAML authoring assistance, such as inserting TOC entries.</span></span>
> * <span data-ttu-id="bf082-108">[markdownlint](https://marketplace.visualstudio.com/items?itemName=DavidAnson.vscode-markdownlint)：David Anson 推出的一种非常受欢迎的 Markdown Linter，可帮助确保 Markdown 有效。</span><span class="sxs-lookup"><span data-stu-id="bf082-108">[markdownlint](https://marketplace.visualstudio.com/items?itemName=DavidAnson.vscode-markdownlint): A popular Markdown linter by David Anson to help make sure your Markdown is valid.</span></span>
> * <span data-ttu-id="bf082-109">[代码拼写检查器](https://marketplace.visualstudio.com/items?itemName=streetsidesoftware.code-spell-checker)：Street Side Software 推出的完全脱机的拼写检查器。</span><span class="sxs-lookup"><span data-stu-id="bf082-109">[Code Spell Checker](https://marketplace.visualstudio.com/items?itemName=streetsidesoftware.code-spell-checker): A fully offline spell checker by Street Side Software.</span></span>
> * <span data-ttu-id="bf082-110">[Docs 预览](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-preview)：使用 docs.microsoft.com CSS 可进行更准确的 Markdown 预览，包括自定义 Markdown。</span><span class="sxs-lookup"><span data-stu-id="bf082-110">[Docs Preview](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-preview): Uses the docs.microsoft.com CSS for more accurate Markdown preview, including custom Markdown.</span></span>
> * <span data-ttu-id="bf082-111">[Docs 文章模板](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-article-templates)：允许用户搭建 Learn 模块基架以及将 Markdown 框架内容应用于新文件。</span><span class="sxs-lookup"><span data-stu-id="bf082-111">[Docs Article Templates](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-article-templates): Allows users to scaffold Learn modules and apply Markdown skeleton content to new files.</span></span>
> * <span data-ttu-id="bf082-112">[Docs YAML](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-yaml)：提供 Docs YAML 架构验证和自动完成。</span><span class="sxs-lookup"><span data-stu-id="bf082-112">[Docs YAML](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-yaml): Provides Docs YAML schema validation and auto-complete.</span></span>
> * <span data-ttu-id="bf082-113">[Docs 图像](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-images):提供图像压缩和重新调整文件夹和单个文件大小的功能，为 docs.microsoft.com 的作者提供帮助。</span><span class="sxs-lookup"><span data-stu-id="bf082-113">[Docs Images](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-images): Provides image compression and resizing for folders and individual files to help authors of docs.microsoft.com.</span></span>

## <a name="prerequisites-and-assumptions"></a><span data-ttu-id="bf082-114">前提条件和假设</span><span class="sxs-lookup"><span data-stu-id="bf082-114">Prerequisites and assumptions</span></span>

<span data-ttu-id="bf082-115">要使用 Docs Markdown 扩展插入相关链接、图像和其他嵌入内容，必须将 VS Code 工作区的范围限定于所克隆的公开发布系统 (OPS) 存储库的根路径。</span><span class="sxs-lookup"><span data-stu-id="bf082-115">To insert relative links, images, and other embedded content with the Docs Markdown extension, you must have your VS Code workspace scoped to the root of your cloned Open Publishing System (OPS) repo.</span></span> <span data-ttu-id="bf082-116">例如，如果已将文档存储库克隆到 `C:\git\SomeDocsRepo\`，请在 VS Code 中打开该文件夹或子文件夹：选择“文件” > “打开文件夹”菜单，或使用命令行中的 `code C:\git\SomeDocsRepo\`。</span><span class="sxs-lookup"><span data-stu-id="bf082-116">For example, if you have cloned the docs repository to `C:\git\SomeDocsRepo\`, then open that folder or a subfolder in VS Code: **File** > **Open Folder** menu,  or `code C:\git\SomeDocsRepo\` from the command line.</span></span>

<span data-ttu-id="bf082-117">扩展支持的一些语法（如警报和片段）是 OPS 的自定义 Markdown。</span><span class="sxs-lookup"><span data-stu-id="bf082-117">Some syntax supported by the extension, such as alerts and snippets, are custom Markdown for OPS.</span></span> <span data-ttu-id="bf082-118">除非已通过 OPS 发布，否则将无法正确呈现自定义 Markdown。</span><span class="sxs-lookup"><span data-stu-id="bf082-118">Custom Markdown will not render correctly unless published via OPS.</span></span>

## <a name="how-to-use-the-docs-markdown-extension"></a><span data-ttu-id="bf082-119">如何使用 Docs Markdown 扩展</span><span class="sxs-lookup"><span data-stu-id="bf082-119">How to use the Docs Markdown extension</span></span>

<span data-ttu-id="bf082-120">要访问 Docs Markdown 菜单，请键入 <kbd>ALT+M</kbd>。</span><span class="sxs-lookup"><span data-stu-id="bf082-120">To access the **Docs Markdown** menu, type <kbd>ALT+M</kbd>.</span></span> <span data-ttu-id="bf082-121">可单击或使用上下箭头来选择所需的命令。</span><span class="sxs-lookup"><span data-stu-id="bf082-121">You can click or use the up and down arrows to select the command you want.</span></span> <span data-ttu-id="bf082-122">或者，可键入内容以开始筛选，然后当你所需的功能在菜单中突出显示时按 <kbd>Enter</kbd>。</span><span class="sxs-lookup"><span data-stu-id="bf082-122">Or you can type to start filtering, then hit <kbd>ENTER</kbd> when the function you want is highlighted in the menu.</span></span>

<span data-ttu-id="bf082-123">请参阅 [Docs Markdown 自述文件](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown)以获取最新的命令列表。</span><span class="sxs-lookup"><span data-stu-id="bf082-123">See the [Docs Markdown readme](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown) for an up-to-date list of commands.</span></span>

## <a name="how-to-generate-a-master-redirect-file"></a><span data-ttu-id="bf082-124">如何生成主重定向文件</span><span class="sxs-lookup"><span data-stu-id="bf082-124">How to generate a master redirect file</span></span>

<span data-ttu-id="bf082-125">Docs Markdown 扩展包括一个脚本，用于基于单个文件中的 `redirect_url` 元数据生成或更新存储库的主重定向文件。</span><span class="sxs-lookup"><span data-stu-id="bf082-125">The Docs Markdown extension includes a script to generate or update a master redirection file for a repo, based on the `redirect_url` metadata in individual files.</span></span> <span data-ttu-id="bf082-126">此脚本可检查存储库中每个 Markdown 文件是否具有 `redirect_url`、将重定向元数据添加到存储库的主重定向文件 (.openpublishing.redirection.json)，还可将已重定向的文件移至存储库以外的文件夹。</span><span class="sxs-lookup"><span data-stu-id="bf082-126">This script checks every Markdown file in the repo for `redirect_url`, adds the redirection metadata to the master redirection file (*.openpublishing.redirection.json*) for the repo, and moves the redirected files to a folder outside the repo.</span></span> <span data-ttu-id="bf082-127">要运行脚本，请执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="bf082-127">To run the script:</span></span>

1. <span data-ttu-id="bf082-128">选择 <kbd>F1</kbd> 打开 VS Code 命令面板。</span><span class="sxs-lookup"><span data-stu-id="bf082-128">Select <kbd>F1</kbd> to open the VS Code command palette.</span></span>
2. <span data-ttu-id="bf082-129">开始键入“Docs:生成…”</span><span class="sxs-lookup"><span data-stu-id="bf082-129">Start typing "Docs: Generate..."</span></span>
3. <span data-ttu-id="bf082-130">选择命令 `Docs: Generate master redirection file`。</span><span class="sxs-lookup"><span data-stu-id="bf082-130">Select the command `Docs: Generate master redirection file`.</span></span>
4. <span data-ttu-id="bf082-131">该脚本完成运行后，重定向结果将显示在 VS Code 输出窗格中，并且已删除的 Markdown 文件将添加到默认路径下的 Docs Authoring\redirects 文件夹中。</span><span class="sxs-lookup"><span data-stu-id="bf082-131">When the script finishes running, the redirection results will show in the VS Code output pane, and the removed Markdown files will be added to the Docs Authoring\redirects folder under your default path.</span></span>
5. <span data-ttu-id="bf082-132">查看结果。</span><span class="sxs-lookup"><span data-stu-id="bf082-132">Review the results.</span></span> <span data-ttu-id="bf082-133">如果结果与预期一样，请提交拉取请求以更新存储库。</span><span class="sxs-lookup"><span data-stu-id="bf082-133">If they are as expected, submit a pull request to update the repo.</span></span>

## <a name="how-to-assign-keyboard-shortcuts"></a><span data-ttu-id="bf082-134">如何分配键盘快捷方式</span><span class="sxs-lookup"><span data-stu-id="bf082-134">How to assign keyboard shortcuts</span></span>

1. <span data-ttu-id="bf082-135">依次键入 <kbd>Ctrl+K</kbd> 和 <kbd>Ctrl+S</kbd>，打开键盘快捷方式列表。</span><span class="sxs-lookup"><span data-stu-id="bf082-135">Type <kbd>CTRL+K</kbd> then <kbd>Ctrl+S</kbd> to open the **Keyboard Shortcuts** list.</span></span>
1. <span data-ttu-id="bf082-136">搜索要创建自定义键绑定的命令，例如 `formatBold`。</span><span class="sxs-lookup"><span data-stu-id="bf082-136">Search for the command, such as `formatBold`, for which you want to create a custom key binding.</span></span>
1. <span data-ttu-id="bf082-137">鼠标悬停在该行上时，单击命令名称旁边出现的加号。</span><span class="sxs-lookup"><span data-stu-id="bf082-137">Click the plus that appears near the command name when you mouse over the line.</span></span>
1. <span data-ttu-id="bf082-138">在显示新的输入框后，键入想要绑定到特定命令的键盘快捷方式。</span><span class="sxs-lookup"><span data-stu-id="bf082-138">After a new input box is visible, type the keyboard shortcut you want to bind to that particular command.</span></span> <span data-ttu-id="bf082-139">例如，要将常见快捷方式用于加粗操作，则键入 <kbd>Ctrl+B</kbd>。</span><span class="sxs-lookup"><span data-stu-id="bf082-139">For example, to use the common shortcut for bold, type <kbd>Ctrl+B</kbd>.</span></span>
1. <span data-ttu-id="bf082-140">在键绑定中插入 `when` 子句是个不错的主意，这样便无法在 Markdown 以外的文件中使用该快捷方式。</span><span class="sxs-lookup"><span data-stu-id="bf082-140">It's a good idea to insert a `when` clause into your key binding, so it won't be available in files other than Markdown.</span></span> <span data-ttu-id="bf082-141">为此，请打开 keybindings.json，在命令名称下方插入以下行（请确保在行之间添加逗号）：</span><span class="sxs-lookup"><span data-stu-id="bf082-141">To do this, open *keybindings.json* and insert the following line below the command name (be sure to add a comma between lines):</span></span>

    `"when": "editorTextFocus && editorLangId == 'markdown'"`

    <span data-ttu-id="bf082-142">自定义键绑定完成后，在 keybindings.json 中看起来应如下所示：</span><span class="sxs-lookup"><span data-stu-id="bf082-142">Your completed custom key binding should look like this in *keybindings.json*:</span></span>

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
    > <span data-ttu-id="bf082-143">将键绑定放在此文件中以覆盖默认值</span><span class="sxs-lookup"><span data-stu-id="bf082-143">Place your key bindings in this file to overwrite the defaults</span></span>

1. <span data-ttu-id="bf082-144">保存 keybindings.json。</span><span class="sxs-lookup"><span data-stu-id="bf082-144">Save *keybindings.json*.</span></span>

<span data-ttu-id="bf082-145">有关键绑定的详细信息，请参阅 [VS Code 文档](https://code.visualstudio.com/docs/getstarted/keybindings)。</span><span class="sxs-lookup"><span data-stu-id="bf082-145">For more information on key bindings, see the [VS Code docs](https://code.visualstudio.com/docs/getstarted/keybindings).</span></span>

## <a name="how-to-show-the-legacy-gauntlet-toolbar"></a><span data-ttu-id="bf082-146">如何显示旧的“Gauntlet”工具栏</span><span class="sxs-lookup"><span data-stu-id="bf082-146">How to show the legacy "Gauntlet" toolbar</span></span>

<span data-ttu-id="bf082-147">名为“Gauntlet”的扩展代码的前用户会注意到，安装 Docs Markdown 扩展时，在 VS Code 窗口的底部不再显示创作工具栏。</span><span class="sxs-lookup"><span data-stu-id="bf082-147">Former users of the extension code-named "Gauntlet" will notice that the authoring toolbar no longer appears at the bottom of the VS Code window when the Docs Markdown Extension is installed.</span></span> <span data-ttu-id="bf082-148">这是因为工具栏占据了 VS Code 状态栏的大量空间，而且未遵循扩展 UX 的最佳做法，因此在新扩展中被弃用。</span><span class="sxs-lookup"><span data-stu-id="bf082-148">This is because the toolbar took up a large space on the VS Code status bar and did not follow best practices for extension UX, so it is deprecated in the new extension.</span></span> <span data-ttu-id="bf082-149">但是，可以通过更新 VS Code settings.json 文件来选择性地显示工具栏，如下所示：</span><span class="sxs-lookup"><span data-stu-id="bf082-149">However, you can optionally show the toolbar by updating your VS Code settings.json file as follows:</span></span>

1. <span data-ttu-id="bf082-150">在 VS Code 中，转到“文件” > “首选项” > “设置”，或者选择 <kbd>Ctrl+,</kbd>。</span><span class="sxs-lookup"><span data-stu-id="bf082-150">In VS Code, go to **File** > **Preferences** > **Settings** or select <kbd>Ctrl+,</kbd>.</span></span>
1. <span data-ttu-id="bf082-151">选择“用户设置”，更改所有 VS Code 工作区的设置，或选择“工作区设置”，更改当前工作区的相关设置。</span><span class="sxs-lookup"><span data-stu-id="bf082-151">Select **User Settings** to change the settings for all VS Code workspaces or **Workspace Settings** to change them for just the current workspace.</span></span>
1. <span data-ttu-id="bf082-152">选择“扩展” > “Docs Markdown 扩展配置”，然后选择“在底部状态栏中显示旧工具栏”。</span><span class="sxs-lookup"><span data-stu-id="bf082-152">Select **Extensions** > **Docs Markdown Extension Configuration**, and then select **Show the legacy toolbar in the bottom status bar**.</span></span>

   ![在 VS Code 中显示旧工具栏设置](docs-authoring/media/show-gauntlet-bar.png)

<span data-ttu-id="bf082-154">做出选择后，VS Code 会更新 settings.json 文件。</span><span class="sxs-lookup"><span data-stu-id="bf082-154">Once you've made your selection, VS Code updates the *settings.json* file.</span></span> <span data-ttu-id="bf082-155">系统将提示你重新加载窗口，以使更改生效。</span><span class="sxs-lookup"><span data-stu-id="bf082-155">You will then be prompted to reload the window for the changes to take effect.</span></span>

<span data-ttu-id="bf082-156">添加到扩展的更新的命令在工具栏中不可用。</span><span class="sxs-lookup"><span data-stu-id="bf082-156">Newer commands added to the extension will not be available from the toolbar.</span></span>

## <a name="how-to-use-docs-templates"></a><span data-ttu-id="bf082-157">如何使用 Docs 模板</span><span class="sxs-lookup"><span data-stu-id="bf082-157">How to use Docs templates</span></span>

<span data-ttu-id="bf082-158">使用 Docs 文章模板扩展，VS Code 中的编写者可以从集中存储中提取 Markdown 模板并将其应用到文件。</span><span class="sxs-lookup"><span data-stu-id="bf082-158">The Docs Article Templates extension lets writers in VS Code pull a Markdown template from a centralized store and apply it to a file.</span></span> <span data-ttu-id="bf082-159">模板可帮助确保文章中包含所需的元数据、遵循内容标准等。</span><span class="sxs-lookup"><span data-stu-id="bf082-159">Templates can help ensure that required metadata is included in articles, that content standards are followed, and so on.</span></span> <span data-ttu-id="bf082-160">在公共 GitHub 存储库中，模板作为 Markdown 文件进行管理。</span><span class="sxs-lookup"><span data-stu-id="bf082-160">Templates are managed as Markdown files in a public GitHub repository.</span></span>

### <a name="to-apply-a-template-in-vs-code"></a><span data-ttu-id="bf082-161">在 VS Code 中应用模板</span><span class="sxs-lookup"><span data-stu-id="bf082-161">To apply a template in VS Code</span></span>

1. <span data-ttu-id="bf082-162">请确保已安装和启用 Docs 文章模板扩展。</span><span class="sxs-lookup"><span data-stu-id="bf082-162">Ensure the Docs Article Templates extension is installed and enabled.</span></span>
1. <span data-ttu-id="bf082-163">如果没有安装 Docs Markdown 扩展，请单击 <kbd>F1</kbd> 打开命令面板，开始键入“template”进行筛选，然后单击 `Docs: Template`。</span><span class="sxs-lookup"><span data-stu-id="bf082-163">If you don't have the Docs Markdown extension installed, click <kbd>F1</kbd> to open the command palette, start typing "template" to filter, then click `Docs: Template`.</span></span> <span data-ttu-id="bf082-164">如果安装了 Docs Markdown，则可以使用命令面板，也可以单击 <kbd>Alt+M</kbd> 以显示 Docs Markdown QuickPick 菜单，然后从列表中选择 `Template`。</span><span class="sxs-lookup"><span data-stu-id="bf082-164">If you do have Docs Markdown installed, you can use either the command palette or click <kbd>Alt+M</kbd> to bring up the Docs Markdown QuickPick menu, then select `Template` from the list.</span></span>
1. <span data-ttu-id="bf082-165">从显示的列表中选择所需的模板。</span><span class="sxs-lookup"><span data-stu-id="bf082-165">Select the desired template from the list that appears.</span></span>

### <a name="to-add-your-github-id-andor-microsoft-alias-to-your-vs-code-settings"></a><span data-ttu-id="bf082-166">将 GitHub ID 和/或 Microsoft 别名添加到 VS Code 设置中</span><span class="sxs-lookup"><span data-stu-id="bf082-166">To add your GitHub ID and/or Microsoft alias to your VS Code settings</span></span>

<span data-ttu-id="bf082-167">Templates 扩展支持三个动态元数据字段：author、ms.author 和 ms.date。</span><span class="sxs-lookup"><span data-stu-id="bf082-167">The Templates extension supports three dynamic metadata fields: author, ms.author, and ms.date.</span></span> <span data-ttu-id="bf082-168">这意味着，如果模板创建者在 Markdown 模板的元数据标头中使用这些字段，则在应用模板时，它们将在你的文件中自动填充，如下所示：</span><span class="sxs-lookup"><span data-stu-id="bf082-168">That means that if a template creator uses these fields in the metadata header of a Markdown template, they will be auto-populated in your file when you apply the template, as follows:</span></span>

| <span data-ttu-id="bf082-169">元数据字段</span><span class="sxs-lookup"><span data-stu-id="bf082-169">Metadata field</span></span> | <span data-ttu-id="bf082-170">值</span><span class="sxs-lookup"><span data-stu-id="bf082-170">Value</span></span> |
|--|--|
| `author` | <span data-ttu-id="bf082-171">你的 GitHub 别名（如果在 VS Code 设置文件中指定）。</span><span class="sxs-lookup"><span data-stu-id="bf082-171">Your GitHub alias, if specified in your VS Code settings file.</span></span> |
| `ms.author` | <span data-ttu-id="bf082-172">你的 Microsoft 别名（如果在 VS Code 设置文件中指定）。</span><span class="sxs-lookup"><span data-stu-id="bf082-172">Your Microsoft alias, if specified in your VS Code settings file.</span></span> <span data-ttu-id="bf082-173">如果你不是 Microsoft 员工，请不要指定该字段。</span><span class="sxs-lookup"><span data-stu-id="bf082-173">If you are not a Microsoft employee, leave unspecified.</span></span> |
| `ms.date` | <span data-ttu-id="bf082-174">采用 Docs 支持的格式 (`MM/DD/YYYY`) 的当前日期。</span><span class="sxs-lookup"><span data-stu-id="bf082-174">The current date in the Docs-supported format, `MM/DD/YYYY`.</span></span> <span data-ttu-id="bf082-175">如果之后更新文件，则不会自动更新日期 - 必须手动更新。</span><span class="sxs-lookup"><span data-stu-id="bf082-175">The date is not automatically updated if you subsequently update the file - you must update it manually.</span></span> <span data-ttu-id="bf082-176">此字段用于表示“文章新鲜度”。</span><span class="sxs-lookup"><span data-stu-id="bf082-176">This field is used to indicate the "article freshness".</span></span> |

### <a name="to-set-author-andor-msauthor"></a><span data-ttu-id="bf082-177">设置 author 和/或 ms.author</span><span class="sxs-lookup"><span data-stu-id="bf082-177">To set author and/or ms.author</span></span>

1. <span data-ttu-id="bf082-178">在 VS Code 中，转到“文件” > “首选项” > “设置”，或者选择 <kbd>Ctrl+,</kbd>。</span><span class="sxs-lookup"><span data-stu-id="bf082-178">In VS Code, go to **File** > **Preferences** > **Settings** or select <kbd>Ctrl+,</kbd>.</span></span>
1. <span data-ttu-id="bf082-179">选择“用户设置”，更改所有 VS Code 工作区的设置，或选择“工作区设置”，更改当前工作区的相关设置。</span><span class="sxs-lookup"><span data-stu-id="bf082-179">Select **User** settings to change the settings for all VS Code workspaces, or **Workspace** settings to change them for just the current workspace.</span></span>
1. <span data-ttu-id="bf082-180">在左侧的“默认设置”窗格中，找到“Docs 文章模板扩展配置”，单击所需设置旁边的铅笔图标，然后单击“设置”中的“替换”。</span><span class="sxs-lookup"><span data-stu-id="bf082-180">In the Default Settings pane on the left, find **Docs Article Templates Extension Configuration**, click the pencil icon next to the desired setting, then click Replace in Settings.</span></span>
1. <span data-ttu-id="bf082-181">“用户设置”窗格将并排打开，底部附带一个新条目。</span><span class="sxs-lookup"><span data-stu-id="bf082-181">The **User** settings pane will open side by side, with a new entry at the bottom.</span></span>
1. <span data-ttu-id="bf082-182">根据需要，添加 GitHub ID 或 Microsoft 电子邮件别名，然后保存该文件。</span><span class="sxs-lookup"><span data-stu-id="bf082-182">Add your GitHub ID or Microsoft email alias, as appropriate, and save the file.</span></span>
1. <span data-ttu-id="bf082-183">可能需要关闭并重启 VS Code 才能使更改生效。</span><span class="sxs-lookup"><span data-stu-id="bf082-183">You might need to close and restart VS Code for the changes to take effect.</span></span>
1. <span data-ttu-id="bf082-184">现在，在应用使用动态字段的模板时，你的 GitHub ID 和/或 Microsoft 别名自动填充到元数据标头中。</span><span class="sxs-lookup"><span data-stu-id="bf082-184">Now, when you apply a template that uses dynamic fields, your GitHub ID and/or Microsoft alias will be auto-populated in the metadata header.</span></span>

### <a name="to-make-a-new-template-available-in-vs-code"></a><span data-ttu-id="bf082-185">生成可在 VS Code 中使用的新模板</span><span class="sxs-lookup"><span data-stu-id="bf082-185">To make a new template available in VS Code</span></span>

1. <span data-ttu-id="bf082-186">将模板起草为 Markdown 文件。</span><span class="sxs-lookup"><span data-stu-id="bf082-186">Draft your template as a Markdown file.</span></span>
1. <span data-ttu-id="bf082-187">将拉取请求提交到 [MicrosoftDocs/content-templates](https://github.com/MicrosoftDocs/content-templates) 存储库的模板文件夹中。</span><span class="sxs-lookup"><span data-stu-id="bf082-187">Submit a pull request to the templates folder of the [MicrosoftDocs/content-templates](https://github.com/MicrosoftDocs/content-templates) repo.</span></span>

<span data-ttu-id="bf082-188">docs.microsoft.com 团队会查看你的模板，并在该模板符合 docs.microsoft.com 风格指南的情况下合并 PR。</span><span class="sxs-lookup"><span data-stu-id="bf082-188">The docs.microsoft.com team will review your template and merge the PR if it meets docs.microsoft.com style guidelines.</span></span> <span data-ttu-id="bf082-189">合并后，该模板将可供 Docs 文章模板扩展的所有用户使用。</span><span class="sxs-lookup"><span data-stu-id="bf082-189">Once merged, the template will be available to all users of the Docs Article Templates extension.</span></span>

## <a name="demo-several-features"></a><span data-ttu-id="bf082-190">演示多种功能</span><span class="sxs-lookup"><span data-stu-id="bf082-190">Demo several features</span></span>

<span data-ttu-id="bf082-191">下面是一个简短的视频，演示了 Docs 创作包的以下功能：</span><span class="sxs-lookup"><span data-stu-id="bf082-191">Here's a short video that demonstrates the following features of the Docs Authoring Pack:</span></span>

* <span data-ttu-id="bf082-192">**YAML 文件**</span><span class="sxs-lookup"><span data-stu-id="bf082-192">**YAML files**</span></span>
  * <span data-ttu-id="bf082-193">支持“Docs:链接到存储库中的文件”</span><span class="sxs-lookup"><span data-stu-id="bf082-193">Support for "Docs: Link to file in repo"</span></span>
* <span data-ttu-id="bf082-194">**Markdown 文件**</span><span class="sxs-lookup"><span data-stu-id="bf082-194">**Markdown files**</span></span>
  * <span data-ttu-id="bf082-195">更新“ms.date”元数据值上下文菜单选项</span><span class="sxs-lookup"><span data-stu-id="bf082-195">Update "ms.date" Metadata Value context menu option</span></span>
  * <span data-ttu-id="bf082-196">代码自动完成支持代码隔离语言标识符</span><span class="sxs-lookup"><span data-stu-id="bf082-196">Code auto-completion support for code-fence language identifiers</span></span>
  * <span data-ttu-id="bf082-197">无法识别的代码隔离语言标识符警告/自动更正支持</span><span class="sxs-lookup"><span data-stu-id="bf082-197">Unrecognized code-fence language identifier warnings / auto correction support</span></span>
  * <span data-ttu-id="bf082-198">按升序对所选内容进行排序（A 到 Z）</span><span class="sxs-lookup"><span data-stu-id="bf082-198">Sort selection ascending (A to Z)</span></span>
  * <span data-ttu-id="bf082-199">按降序对所选内容进行排序（Z 到 A）</span><span class="sxs-lookup"><span data-stu-id="bf082-199">Sort selection descending (Z to A)</span></span>

> [!VIDEO https://www.youtube.com/embed/6zfbBRdjlw8]

## <a name="contribution-expectations"></a><span data-ttu-id="bf082-200">参与预期</span><span class="sxs-lookup"><span data-stu-id="bf082-200">Contribution expectations</span></span>

<span data-ttu-id="bf082-201">Docs 创作包扩展是开放源代码，供具有 GitHub 帐户的任何人参与。</span><span class="sxs-lookup"><span data-stu-id="bf082-201">The Docs Authoring Pack extension is open source and available for contributions to anyone with a GitHub account.</span></span> <span data-ttu-id="bf082-202">有一个专门的 Microsoft 内部团队积极处理此项目。</span><span class="sxs-lookup"><span data-stu-id="bf082-202">There is a dedicated internal Microsoft team that actively works on this project.</span></span> <span data-ttu-id="bf082-203">该团队会监视问题和拉取请求。</span><span class="sxs-lookup"><span data-stu-id="bf082-203">This team monitors issues and pull requests.</span></span> <span data-ttu-id="bf082-204">服务级别协议 (SLA) 问题目前一周解决，且目前有望一周内审阅拉取请求。</span><span class="sxs-lookup"><span data-stu-id="bf082-204">The service level agreement (SLA) and expectation of getting a pull request reviewed is currently one week.</span></span> <span data-ttu-id="bf082-205">该团队正在努力实现自动化，以缩短这一周转时间。</span><span class="sxs-lookup"><span data-stu-id="bf082-205">The team is undergoing automation efforts to improve this turn around time.</span></span>

## <a name="next-steps"></a><span data-ttu-id="bf082-206">后续步骤</span><span class="sxs-lookup"><span data-stu-id="bf082-206">Next steps</span></span>

<span data-ttu-id="bf082-207">了解 Docs 创作包 Visual Studio Code 扩展中可用的各种功能。</span><span class="sxs-lookup"><span data-stu-id="bf082-207">Explore the various features available in the Docs Authoring Pack, Visual Studio Code extension.</span></span>

* [<span data-ttu-id="bf082-208">开发语言完成</span><span class="sxs-lookup"><span data-stu-id="bf082-208">Dev lang completion</span></span>](docs-authoring/dev-lang-completion.md)
* [<span data-ttu-id="bf082-209">图像压缩</span><span class="sxs-lookup"><span data-stu-id="bf082-209">Image compression</span></span>](docs-authoring/image-compression.md)
* [<span data-ttu-id="bf082-210">元数据更新</span><span class="sxs-lookup"><span data-stu-id="bf082-210">Metadata updates</span></span>](docs-authoring/metadata-updates.md)
* [<span data-ttu-id="bf082-211">重新设置表格式</span><span class="sxs-lookup"><span data-stu-id="bf082-211">Reformat table</span></span>](docs-authoring/reformat-table.md)
* [<span data-ttu-id="bf082-212">智能引号替换</span><span class="sxs-lookup"><span data-stu-id="bf082-212">Smart quote replacement</span></span>](docs-authoring/smart-quote-replacement.md)
* [<span data-ttu-id="bf082-213">排序重定向</span><span class="sxs-lookup"><span data-stu-id="bf082-213">Sort redirects</span></span>](docs-authoring/sort-redirects.md)
* [<span data-ttu-id="bf082-214">排序所选内容</span><span class="sxs-lookup"><span data-stu-id="bf082-214">Sort selection</span></span>](docs-authoring/sort-selection.md)
