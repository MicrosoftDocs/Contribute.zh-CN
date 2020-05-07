---
title: 元数据更新 - Docs 创作包
description: 了解如何从 Docs 创作包 Visual Studio Code 扩展中更新元数据。
author: IEvangelist
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.date: 03/03/2020
ms.author: dapine
ms.openlocfilehash: 391ea6c523d1f1b82b21883cea5e3428e86633e9
ms.sourcegitcommit: cfba5ad25b898bfed76046126ce8ff4871910701
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/04/2020
ms.locfileid: "78336626"
---
# <a name="update-metadata"></a><span data-ttu-id="92ccc-103">更新元数据</span><span class="sxs-lookup"><span data-stu-id="92ccc-103">Update metadata</span></span>

[!INCLUDE [markdown-extension](includes/markdown-extension.md)]

## <a name="summary"></a><span data-ttu-id="92ccc-104">摘要</span><span class="sxs-lookup"><span data-stu-id="92ccc-104">Summary</span></span>

<span data-ttu-id="92ccc-105">在 Markdown ( *.md) 文件中，有两个特定于元数据的上下文菜单项\** 。</span><span class="sxs-lookup"><span data-stu-id="92ccc-105">In a Markdown (*\*.md*) file, there are two contextual menu items specific to metadata.</span></span> <span data-ttu-id="92ccc-106">右键单击文本编辑器中的任意位置时，会看到类似以下菜单项的内容：</span><span class="sxs-lookup"><span data-stu-id="92ccc-106">When you right-click anywhere in the text editor, you will see something similar to the following menu items:</span></span>

:::image type="content" source="media/update-metadata-menu.png" alt-text="更新元数据上下文菜单":::

## <a name="update-msdate-metadata-value"></a><span data-ttu-id="92ccc-108">更新 `ms.date` 元数据值</span><span class="sxs-lookup"><span data-stu-id="92ccc-108">Update `ms.date` metadata value</span></span>

<span data-ttu-id="92ccc-109">选择“更新  **元数据值”选项会将当前的 Markdown 文件 `ms.date` 值设为当天的日期**`ms.date`。</span><span class="sxs-lookup"><span data-stu-id="92ccc-109">Selecting the **Update `ms.date` Metadata Value** option will set the current Markdown files `ms.date` value to today's date.</span></span> <span data-ttu-id="92ccc-110">如果文档不包含 `ms.date` 元数据字段，则不执行任何操作。</span><span class="sxs-lookup"><span data-stu-id="92ccc-110">If the document does not have an `ms.date` metadata field, no action is taken.</span></span>

## <a name="update-implicit-metadata-values"></a><span data-ttu-id="92ccc-111">更新隐式元数据值</span><span class="sxs-lookup"><span data-stu-id="92ccc-111">Update implicit metadata values</span></span>

<span data-ttu-id="92ccc-112">选择“更新隐式元数据值”选项将查找并替换可能隐式指定的所有可能的元数据值  。</span><span class="sxs-lookup"><span data-stu-id="92ccc-112">Selecting the **Update implicit metadata values** option will find and replace all possible metadata values that could be implicitly specified.</span></span> <span data-ttu-id="92ccc-113">元数据值是在  *节点下的 docfx.json 文件中隐式指定的*`build/fileMetadata`。</span><span class="sxs-lookup"><span data-stu-id="92ccc-113">Metadata values are implicitly specified in the *docfx.json* file, under the `build/fileMetadata` node.</span></span> <span data-ttu-id="92ccc-114">`fileMetadata` 节点中的每个键值对均表示元数据默认值。</span><span class="sxs-lookup"><span data-stu-id="92ccc-114">Each key value pair in the `fileMetadata` node represents metadata defaults.</span></span> <span data-ttu-id="92ccc-115">例如，top-level/sub-folder 目录中忽略 *元数据值的 Markdown 文件可能会隐式指定要在* 节点中使用的默认值`ms.author``fileMetadata`。</span><span class="sxs-lookup"><span data-stu-id="92ccc-115">For example, a Markdown file in the *top-level/sub-folder* directory that omits the `ms.author` metadata value could implicitly specify a default value to use in the `fileMetadata` node.</span></span>

```json
{
    "build": {
        "fileMetadata": {
            "ms.author": {
                "top-level/sub-folder/**/**.md": "dapine"
            }
        }
    }
}
```

<span data-ttu-id="92ccc-116">在此情况下，所有 Markdown 文件都将隐式采用 `ms.author: dapine` 元数据值。</span><span class="sxs-lookup"><span data-stu-id="92ccc-116">In this case, all Markdown files would implicitly take on the `ms.author: dapine` metadata value.</span></span> <span data-ttu-id="92ccc-117">此功能用于在 docfx.json 文件中找到的这些隐式设置  。</span><span class="sxs-lookup"><span data-stu-id="92ccc-117">The feature acts on these implicit settings found in the *docfx.json* file.</span></span> <span data-ttu-id="92ccc-118">如果 Markdown 文件包含的元数据值被显式设为除隐式值以外的值，则会覆盖这些值。</span><span class="sxs-lookup"><span data-stu-id="92ccc-118">If a Markdown file contains metadata with values that are explicitly set to something other than the implicit values, they are overridden.</span></span>

<span data-ttu-id="92ccc-119">请考虑使用以下 Markdown 文件元数据，该 Markdown 文件位于 top-level/sub-folder/includes/example.md 中  ：</span><span class="sxs-lookup"><span data-stu-id="92ccc-119">Consider the following Markdown file metadata, where this Markdown file resides in **top-level/sub-folder/includes/example.md**:</span></span>

```markdown
---
ms.author: someone-else
---

# Content
```

<span data-ttu-id="92ccc-120">如果在此文件上执行了“更新隐式元数据值”选项，则元数据值上方的假设的 docfx.json 内容将更新为   `ms.author: dapine`。</span><span class="sxs-lookup"><span data-stu-id="92ccc-120">If the **Update implicit metadata values** option was executed on this file, with the assumed *docfx.json* content from above the metadata value would be updated to `ms.author: dapine`.</span></span>

```markdown
---
ms.author: dapine
---

# Content
```

## <a name="in-action"></a><span data-ttu-id="92ccc-121">操作过程</span><span class="sxs-lookup"><span data-stu-id="92ccc-121">In action</span></span>

<span data-ttu-id="92ccc-122">下面是此功能的简短演示。</span><span class="sxs-lookup"><span data-stu-id="92ccc-122">Below is a brief demonstration of this feature.</span></span>

<span data-ttu-id="92ccc-123">[![更新元数据演示](media/update-metadata.gif)](media/update-metadata.gif#lightbox)</span><span class="sxs-lookup"><span data-stu-id="92ccc-123">[![Update metadata demo](media/update-metadata.gif)](media/update-metadata.gif#lightbox)</span></span>
