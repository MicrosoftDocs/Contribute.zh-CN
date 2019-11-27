---
title: h1-no-space
description: 有关 Docs 生成问题 h1-no-space 的解释和解决方法。
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 11/25/2019
ms.prod: non-product-specific
ms.openlocfilehash: 7058367a6edd7f663ea42a4fc2e9fafd9cbfb34f
ms.sourcegitcommit: 423d9b8145a11426c91f45510b2d77319838eb27
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2019
ms.locfileid: "74528954"
---
# <a name="h1-no-space"></a>h1-no-space

## <a name="warning"></a>警告

`A space is required after the hash (#) in H1.`

H1 是指 Markdown 文件中的第一个标题。 发布到 docs.microsoft.com 时，H1 以大字体显示在页面顶部。 H1 的创建方式为，以包含一个井号 (#) 的行开头，后跟空格，然后是标题文本。 如果井号后面没有空格，Docs 不会识别 H1。

## <a name="resolution"></a>解决方法

若要解决此错误，请在 H1 中的井号后添加空格。

```markdown
---
author: meganbradley
ms.author: mbradley
---
# This is an H1
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
