---
title: multiple-h1
description: 有关 Docs 生成问题 multiple-h1 的解释和解决方法。
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: 55ce6260cb4d1e09f63e0540528576ed3fa165f8
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/05/2019
ms.locfileid: "57427237"
---
# <a name="multiple-h1"></a>multiple-h1

## <a name="warning"></a>警告

`Multiple H1s are not allowed. You can only have one top-level heading.`

H1 是指 Markdown 文件中的第一个标题。 发布到 docs.microsoft.com 时，H1 以大字体显示在页面顶部。 H1 的创建方式为，以包含一个井号 (#) 的行开头，后跟空格，然后是标题文本。 一个文件中只能有一个 H1。

## <a name="resolution"></a>解决方法

若要解决此问题，请将后续 H1s 的标题级别更改为 H2 (`##`)，否则请重新组织文件。 请注意，不允许跳过标题级别，如 H1 之后为 H3。

```markdown
---
author: meganbradley
ms.author: mbradley
---
# This is an H1

Some content...

## This is an H2
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]