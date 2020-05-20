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
# <a name="update-metadata"></a>更新元数据

[!INCLUDE [markdown-extension](includes/markdown-extension.md)]

## <a name="summary"></a>摘要

在 Markdown (\*.md) 文件中，有两个特定于元数据的上下文菜单项。 右键单击文本编辑器中的任意位置时，会看到类似以下菜单项的内容：

:::image type="content" source="media/update-metadata-menu.png" alt-text="更新元数据上下文菜单":::

## <a name="update-msdate-metadata-value"></a>更新 `ms.date` 元数据值

选择“更新 `ms.date` 元数据值”选项会将当前的 Markdown 文件 `ms.date` 值设为当天的日期。 如果文档不包含 `ms.date` 元数据字段，则不执行任何操作。

## <a name="update-implicit-metadata-values"></a>更新隐式元数据值

选择“更新隐式元数据值”选项将查找并替换可能隐式指定的所有可能的元数据值  。 元数据值是在 `build/fileMetadata` 节点下的 docfx.json 文件中隐式指定的。 `fileMetadata` 节点中的每个键值对均表示元数据默认值。 例如，top-level/sub-folder 目录中忽略 `ms.author` 元数据值的 Markdown 文件可能会隐式指定要在 `fileMetadata` 节点中使用的默认值。

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

在此情况下，所有 Markdown 文件都将隐式采用 `ms.author: dapine` 元数据值。 此功能用于在 docfx.json 文件中找到的这些隐式设置  。 如果 Markdown 文件包含的元数据值被显式设为除隐式值以外的值，则会覆盖这些值。

请考虑使用以下 Markdown 文件元数据，该 Markdown 文件位于 top-level/sub-folder/includes/example.md 中  ：

```markdown
---
ms.author: someone-else
---

# Content
```

如果在此文件上执行了“更新隐式元数据值”选项，则元数据值上方的假设的 docfx.json 内容将更新为 `ms.author: dapine`。

```markdown
---
ms.author: dapine
---

# Content
```

## <a name="in-action"></a>操作过程

下面是此功能的简短演示。

[![更新元数据演示](media/update-metadata.gif)](media/update-metadata.gif#lightbox)
