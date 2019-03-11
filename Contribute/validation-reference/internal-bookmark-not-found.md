---
title: internal-bookmark-not-found
description: 有关 Docs 生成问题 internal-bookmark-not-found 的解释和解决方法
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/28/2019
ms.prod: non-product-specific
ms.openlocfilehash: 9073603d4e745db2f49b57a8901e00a03d8f570f
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/05/2019
ms.locfileid: "57427225"
---
# <a name="internal-bookmark-not-found"></a>internal-bookmark-not-found

**即将推出！**

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>建议

`Current file doesn't contain a bookmark named '{bookmark}'.`

想要链接到当前不存在的文件中的标题。

## <a name="resolution"></a>解决方法

[!INCLUDE [docs-authoring-pack](includes/docs-authoring-pack.md)]

验证你想要链接到的标题并更新链接。

若要链接到当前文章中的某个部分，请使用一个井号，后跟标题内容。 删除标题中的标点符号并将空格替换为短划线。 下面是一个示例：

```markdown
[Managed Disks](#managed-disks)
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
