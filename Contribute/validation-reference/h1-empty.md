---
title: h1-empty
description: 有关 Docs 生成问题 h1-empty 的解释和解决方法。
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 11/25/2019
ms.prod: non-product-specific
ms.openlocfilehash: d0b3ab2206d66ff68a967d7868353b5b399da80a
ms.sourcegitcommit: 423d9b8145a11426c91f45510b2d77319838eb27
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2019
ms.locfileid: "74528794"
---
# <a name="h1-empty"></a>h1-empty

## <a name="warning"></a>警告

`H1 is required. Add content to your top-level heading.`

H1 是指 Markdown 文件中的第一个标题。 发布到 docs.microsoft.com 时，H1 以大字体显示在页面顶部。 H1 的创建方式为，以包含一个井号 (#) 的行开头，后跟空格，然后是标题文本。

## <a name="resolution"></a>解决方法

若要解决此问题，请确保 H1 包含内容，而不仅仅只包含井号。

不好：

```markdown
---
author: meganbradley
ms.author: mbradley
---
#
This is not an H1
```

好：

```markdown
---
author: meganbradley
ms.author: mbradley
---
# This is an H1
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
