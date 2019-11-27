---
title: h1-not-first
description: 有关 Docs 生成问题 h1-not-first 的解释和解决方法
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 11/25/2019
ms.prod: non-product-specific
ms.openlocfilehash: 09b91577f4c87125a92c0c116bc07bc7206c6833
ms.sourcegitcommit: 423d9b8145a11426c91f45510b2d77319838eb27
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2019
ms.locfileid: "74528909"
---
# <a name="h1-not-first"></a>h1-not-first

## <a name="warning"></a>警告

`Markdown content is not allowed before H1.`

在 Markdown 文件中，只有 YAML 元数据标头可以位于 H1 之前。 例如，如果想要在文章顶部添加注释或图像，则必须将其放置在 H1 之后。 不允许以下操作：

```markdown
---
# This is the YAML metadata header
author: meganbradley
---
> [!NOTE]
> You can't do this.

# This is the H1
```

请改为执行此操作：

```markdown
---
# This is the YAML metadata header
author: meganbradley
---
# This is the H1

> [!NOTE]
> This is OK.
```

造成此问题的另一个常见原因是 YAML 标头之前的 [字节顺序标记 (BOM)](http://www.websina.com/bugzero/kb/unicode-bom.html)。 向存储库提交内容时，有时候编码问题会引入这些标记。 它们会在 GitHub 中导致糟糕的呈现效果，应将它们删除。

## <a name="resolution"></a>解决方法

删除 H1 之前除 YAML 元数据标头以外的任何内容。

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
