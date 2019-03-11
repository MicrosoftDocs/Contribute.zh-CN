---
title: external-bookmark-not-found
description: 有关 Docs 生成问题 external-bookmark-not-found 的解释和解决方法
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/26/2019
ms.prod: non-product-specific
ms.openlocfilehash: b533a463ac38d6445ab84c74bf14b2065a0a63f3
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/05/2019
ms.locfileid: "57427182"
---
# <a name="external-bookmark-not-found"></a>external-bookmark-not-found

## <a name="warning"></a>警告

`File '{file name}' doesn't contain a bookmark named '{bookmark text}'.`

想要链接到另一个不存在的文件中的标题。

## <a name="resolution"></a>解决方法

[!INCLUDE [docs-authoring-pack](includes/docs-authoring-pack.md)]

查看要链接到的文件并更新书签链接以指向文件中的有效部分。

若要链接到另一篇文章中的某个部分标题，请使用文件相对或站点相对链接以及井号，后跟标题内容。 删除标题中的标点符号并将空格替换为短划线。 下面是一个示例：

```markdown
[Managed Disks](../../linux/overview.md#managed-disks)
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
