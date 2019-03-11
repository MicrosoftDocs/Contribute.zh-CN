---
title: block-section-invalid
description: 有关 Docs 生成问题 block-section-invalid 的解释和解决方法
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/28/2019
ms.prod: non-product-specific
ms.openlocfilehash: 257b963ae37f5a8f0edc2fbca6186ab0f258cfc0
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/05/2019
ms.locfileid: "57427236"
---
# <a name="block-section-invalid"></a>block-section-invalid

## <a name="warning"></a>警告

`Invalid syntax for alert, div, or video. The text will be rendered as a block quote.`

若干 Docs Markdown 扩展以 `> [!` 开头。 `>` 与 `[` 之间需要空格，并且必须有一个结束 `]`。 如果语法不正确，则文本将呈现为块引用。

## <a name="resolution"></a>解决方法

[!INCLUDE [docs-authoring-pack](includes/docs-authoring-pack.md)]

确保所使用扩展的语法正确：

```markdown

Alerts:

> [!NOTE]
> Information the user should notice even if skimming.

> [!TIP]
> Optional information to help a user be more successful.

> [!IMPORTANT]
> Essential information required for user success.

> [!CAUTION]
> Negative potential consequences of an action.

> [!WARNING]
> Dangerous certain consequences of an action.

Videos:

> [!VIDEO https://channel9.msdn.com/Series/Youve-Got-Key-Values-A-Redis-Jump-Start/03/player]

> [!VIDEO https://www.youtube.com/embed/iAtwVM-Z7rY]

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS]

Sections (div):

> [!div class="class"]

```


<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
