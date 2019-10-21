---
title: h1-in-moniker
description: 有关 Docs 生成问题 h1-in-moniker 的解释和解决方法。
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 10/09/2019
ms.prod: non-product-specific
ms.openlocfilehash: 3730385cfaf86c3a2a6165f1958d644e71ad7b56
ms.sourcegitcommit: 57eb071bdc55ef71fa3f8ac979326c3f8fbe9c45
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/10/2019
ms.locfileid: "72246351"
---
# <a name="h1-in-moniker"></a>h1-in-moniker

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>建议

`H1s are not allowed in moniker sections. Each article should have one and only one H1.`

H1 是指 Markdown 文件中的第一个标题。 发布到 docs.microsoft.com 时，H1 以大字体显示在页面顶部。 H1 的创建方式为，以包含一个井号 (#) 的行开头，后跟空格，然后是标题文本。 一个文件中只能有一个 H1。 H1s 不允许用于名字对象部分，因为根据版本的配置，名字对象中的 H1s 易导致 H1s 重复或缺失。

如果名字对象部分包含一行等于号，形成双下划线（如 `=======`），也可能会收到此消息。 这是 H1 的替代 Markdown 语法。 这种情况也通常出现在合并冲突中：

```markdown
<<<<<<< HEAD
...
=======
...
>>>>>>> 1d82c7efe18f86136247fb366df5030843199c19
```

## <a name="resolution"></a>解决方法

要解决此问题，请删除所有名字对象部分中的 H1s，并确保文章顶部的 H1 适用于所有名字对象部分。 请注意，不允许跳过标题级别，如 H1 之后为 H3。

如果名字对象部分中的 H1 确实是双下划线 (`=======`)，请将其删除，或根据需要将其替换为井号标签标题，如 `##`。 如果双下划线属于合并冲突，请确保同时删除合并冲突的开始和结束标记及已过时的文本。

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
