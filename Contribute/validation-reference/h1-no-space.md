---
title: h1-no-space
description: 有关 Docs 生成问题 h1-no-space 的解释和解决方法。
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: 7dd6a3d5cfc6def000d5bf7a5bf7810a16625cae
ms.sourcegitcommit: 89147521f0aa3b39e7ddf390136b09a43d95c416
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/10/2019
ms.locfileid: "70856234"
---
# <a name="h1-no-space"></a><span data-ttu-id="cf55e-103">h1-no-space</span><span class="sxs-lookup"><span data-stu-id="cf55e-103">h1-no-space</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="cf55e-104">建议</span><span class="sxs-lookup"><span data-stu-id="cf55e-104">Suggestion</span></span>

`A space is required after the hash (#) in H1.`

<span data-ttu-id="cf55e-105">H1 是指 Markdown 文件中的第一个标题。</span><span class="sxs-lookup"><span data-stu-id="cf55e-105">H1 refers to the first heading in a Markdown file.</span></span> <span data-ttu-id="cf55e-106">发布到 docs.microsoft.com 时，H1 以大字体显示在页面顶部。</span><span class="sxs-lookup"><span data-stu-id="cf55e-106">When published to docs.microsoft.com, the H1 shows at the top of the page in a large font.</span></span> <span data-ttu-id="cf55e-107">H1 的创建方式为，以包含一个井号 (#) 的行开头，后跟空格，然后是标题文本。</span><span class="sxs-lookup"><span data-stu-id="cf55e-107">An H1 is created by beginning a line with a single hash (#) followed by a space, then the heading text.</span></span> <span data-ttu-id="cf55e-108">如果井号后面没有空格，Docs 不会识别 H1。</span><span class="sxs-lookup"><span data-stu-id="cf55e-108">Without the space after the hash, Docs will not recognize an H1.</span></span>

## <a name="resolution"></a><span data-ttu-id="cf55e-109">解决方法</span><span class="sxs-lookup"><span data-stu-id="cf55e-109">Resolution</span></span>

<span data-ttu-id="cf55e-110">若要解决此错误，请在 H1 中的井号后添加空格。</span><span class="sxs-lookup"><span data-stu-id="cf55e-110">To fix this error, add a space after the hash in your H1.</span></span>

```markdown
---
author: meganbradley
ms.author: mbradley
---
# This is an H1
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
