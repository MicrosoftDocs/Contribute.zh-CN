---
title: no-space-in-h1
description: 有关 Docs 生成问题 no-space-in-h1 的解释和解决方法。
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: 8c719a89e6373fb960f216a5b4ec01c6d1739a28
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/05/2019
ms.locfileid: "57427228"
---
# <a name="no-space-in-h1"></a><span data-ttu-id="2dcd2-103">no-space-in-h1</span><span class="sxs-lookup"><span data-stu-id="2dcd2-103">no-space-in-h1</span></span>

## <a name="warning"></a><span data-ttu-id="2dcd2-104">警告</span><span class="sxs-lookup"><span data-stu-id="2dcd2-104">Warning</span></span>

`A space is required after the hash (#) in H1.`

<span data-ttu-id="2dcd2-105">H1 是指 Markdown 文件中的第一个标题。</span><span class="sxs-lookup"><span data-stu-id="2dcd2-105">H1 refers to the first heading in a Markdown file.</span></span> <span data-ttu-id="2dcd2-106">发布到 docs.microsoft.com 时，H1 以大字体显示在页面顶部。</span><span class="sxs-lookup"><span data-stu-id="2dcd2-106">When published to docs.microsoft.com, the H1 shows at the top of the page in a large font.</span></span> <span data-ttu-id="2dcd2-107">H1 的创建方式为，以包含一个井号 (#) 的行开头，后跟空格，然后是标题文本。</span><span class="sxs-lookup"><span data-stu-id="2dcd2-107">An H1 is created by beginning a line with a single hash (#) followed by a space, then the heading text.</span></span> <span data-ttu-id="2dcd2-108">如果井号后面没有空格，Docs 不会识别 H1。</span><span class="sxs-lookup"><span data-stu-id="2dcd2-108">Without the space after the hash, Docs will not recognize an H1.</span></span>

## <a name="resolution"></a><span data-ttu-id="2dcd2-109">解决方法</span><span class="sxs-lookup"><span data-stu-id="2dcd2-109">Resolution</span></span>

<span data-ttu-id="2dcd2-110">若要解决此错误，请在 H1 中的井号后添加空格。</span><span class="sxs-lookup"><span data-stu-id="2dcd2-110">To fix this error, add a space after the hash in your H1.</span></span>

```markdown
---
author: meganbradley
ms.author: mbradley
---
# This is an H1
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]