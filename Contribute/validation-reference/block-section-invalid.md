---
title: block-section-invalid
description: 有关 Docs 生成问题 block-section-invalid 的解释和解决方法
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 09/10/2019
ms.prod: non-product-specific
ms.openlocfilehash: 500527c7371dd9d4966460b3eafe0a44874fc4eb
ms.sourcegitcommit: 89147521f0aa3b39e7ddf390136b09a43d95c416
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/10/2019
ms.locfileid: "70848529"
---
# <a name="block-section-invalid"></a><span data-ttu-id="8763b-103">block-section-invalid</span><span class="sxs-lookup"><span data-stu-id="8763b-103">block-section-invalid</span></span>

## <a name="warning"></a><span data-ttu-id="8763b-104">警告</span><span class="sxs-lookup"><span data-stu-id="8763b-104">Warning</span></span>

`Invalid syntax for alert, div, or video. The text will be rendered as a block quote.`

<span data-ttu-id="8763b-105">若干 Docs Markdown 扩展以 `> [!` 开头。</span><span class="sxs-lookup"><span data-stu-id="8763b-105">Several Docs Markdown extensions begin with the string `> [!`.</span></span> <span data-ttu-id="8763b-106">`>` 与 `[` 之间需要空格，并且必须有一个结束 `]`。</span><span class="sxs-lookup"><span data-stu-id="8763b-106">A space is required between `>` and `[`, and there must be a closing `]`.</span></span> <span data-ttu-id="8763b-107">如果语法不正确，则文本将呈现为块引用。</span><span class="sxs-lookup"><span data-stu-id="8763b-107">If the syntax is incorrect, the text will be rendered as a block quote.</span></span>

## <a name="resolution"></a><span data-ttu-id="8763b-108">解决方法</span><span class="sxs-lookup"><span data-stu-id="8763b-108">Resolution</span></span>

[!INCLUDE [docs-authoring-pack](includes/docs-authoring-pack.md)]

<span data-ttu-id="8763b-109">确保所使用扩展的语法正确：</span><span class="sxs-lookup"><span data-stu-id="8763b-109">Ensure the syntax is correct for the extension you're using:</span></span>

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
