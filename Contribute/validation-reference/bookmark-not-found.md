---
title: internal-bookmark-not-found
description: 有关 Docs 生成问题 internal-bookmark-not-found 的解释和解决方法
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 9/10/2019
ms.prod: non-product-specific
ms.openlocfilehash: 53b98f8da199e3495cc00b2388d983191268eee6
ms.sourcegitcommit: 89147521f0aa3b39e7ddf390136b09a43d95c416
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/10/2019
ms.locfileid: "70856211"
---
# <a name="bookmark-not-found"></a>bookmark-not-found

## <a name="warning"></a>警告

`Cannot find bookmark '{bookmark-id}' in '{parent-file}'.`

想要链接到当前文件或其他文件中不存在的标题。

## <a name="resolution"></a>解决方法

[!INCLUDE [docs-authoring-pack](includes/docs-authoring-pack.md)]

验证你想要链接到的标题并更新链接。

若要链接到当前文章中的某个部分，请使用一个井号，后跟标题内容。 删除标题中的标点符号并将空格替换为短划线。 下面是一个示例：

```markdown
[Managed Disks](#managed-disks)
```

若要链接到另一个文件中的标题，请使用指向该文件的相对链接，后面跟有一个哈希符号和标题的文字。 删除标题中的标点符号并将空格替换为短划线。 下面是一个示例：

```markdown
See [the Resolution section in h1-empty](h1-empty.md#resolution).
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
