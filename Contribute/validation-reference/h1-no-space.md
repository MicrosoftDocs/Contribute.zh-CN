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
# <a name="h1-no-space"></a><span data-ttu-id="913f1-103">h1-no-space</span><span class="sxs-lookup"><span data-stu-id="913f1-103">h1-no-space</span></span>

## <a name="warning"></a><span data-ttu-id="913f1-104">警告</span><span class="sxs-lookup"><span data-stu-id="913f1-104">Warning</span></span>

`A space is required after the hash (#) in H1.`

<span data-ttu-id="913f1-105">H1 是指 Markdown 文件中的第一个标题。</span><span class="sxs-lookup"><span data-stu-id="913f1-105">H1 refers to the first heading in a Markdown file.</span></span> <span data-ttu-id="913f1-106">发布到 docs.microsoft.com 时，H1 以大字体显示在页面顶部。</span><span class="sxs-lookup"><span data-stu-id="913f1-106">When published to docs.microsoft.com, the H1 shows at the top of the page in a large font.</span></span> <span data-ttu-id="913f1-107">H1 的创建方式为，以包含一个井号 (#) 的行开头，后跟空格，然后是标题文本。</span><span class="sxs-lookup"><span data-stu-id="913f1-107">An H1 is created by beginning a line with a single hash (#) followed by a space, then the heading text.</span></span> <span data-ttu-id="913f1-108">如果井号后面没有空格，Docs 不会识别 H1。</span><span class="sxs-lookup"><span data-stu-id="913f1-108">Without the space after the hash, Docs will not recognize an H1.</span></span>

## <a name="resolution"></a><span data-ttu-id="913f1-109">解决方法</span><span class="sxs-lookup"><span data-stu-id="913f1-109">Resolution</span></span>

<span data-ttu-id="913f1-110">若要解决此错误，请在 H1 中的井号后添加空格。</span><span class="sxs-lookup"><span data-stu-id="913f1-110">To fix this error, add a space after the hash in your H1.</span></span>

```markdown
---
author: meganbradley
ms.author: mbradley
---
# This is an H1
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
