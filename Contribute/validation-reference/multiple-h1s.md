---
title: multiple-h1s
description: 有关 Docs 生成问题 multiple-h1s 的解释和解决方法。
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 11/25/2019
ms.prod: non-product-specific
ms.openlocfilehash: e2912066895494e221181f2de2bb117ff9ed1636
ms.sourcegitcommit: 423d9b8145a11426c91f45510b2d77319838eb27
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2019
ms.locfileid: "74528939"
---
# <a name="multiple-h1s"></a>multiple-h1s

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>建议

`Multiple H1s are not allowed. You can only have one top-level heading.`

H1 是指 Markdown 文件中的第一个标题。 发布到 docs.microsoft.com 时，H1 以大字体显示在页面顶部。 H1 的创建方式为，以包含一个井号 (#) 的行开头，后跟空格，然后是标题文本。 一个文件中只能有一个 H1。

如果文章包含一行等于号，形成双下划线（如 `=======`），也可能会收到此消息。 这是 H1 的替代 Markdown 语法。 这种情况也通常出现在合并冲突中：

```markdown
<<<<<<< HEAD
...
=======
...
>>>>>>> 1d82c7efe18f86136247fb366df5030843199c19
```

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

如果另一个 H1 确实是双下划线 (`=======`)，请将其删除，或根据需要将其替换为井号标签标题，如 `##`。 如果双下划线属于合并冲突，请确保同时删除合并冲突的开始和结束标记及已过时的文本。

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
