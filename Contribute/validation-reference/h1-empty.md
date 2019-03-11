---
title: h1-empty
description: 有关 Docs 生成问题 h1-empty 的解释和解决方法。
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: bb07235f7cd1ba6d45418c48a4190255bdd9a428
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/05/2019
ms.locfileid: "57427173"
---
# <a name="h1-empty"></a><span data-ttu-id="8a4ff-103">h1-empty</span><span class="sxs-lookup"><span data-stu-id="8a4ff-103">h1-empty</span></span>

## <a name="warning"></a><span data-ttu-id="8a4ff-104">警告</span><span class="sxs-lookup"><span data-stu-id="8a4ff-104">Warning</span></span>

`H1 is required. Add content to your top-level heading.`

<span data-ttu-id="8a4ff-105">H1 是指 Markdown 文件中的第一个标题。</span><span class="sxs-lookup"><span data-stu-id="8a4ff-105">H1 refers to the first heading in a Markdown file.</span></span> <span data-ttu-id="8a4ff-106">发布到 docs.microsoft.com 时，H1 以大字体显示在页面顶部。</span><span class="sxs-lookup"><span data-stu-id="8a4ff-106">When published to docs.microsoft.com, the H1 shows at the top of the page in a large font.</span></span> <span data-ttu-id="8a4ff-107">H1 的创建方式为，以包含一个井号 (#) 的行开头，后跟空格，然后是标题文本。</span><span class="sxs-lookup"><span data-stu-id="8a4ff-107">An H1 is created by beginning a line with a single hash (#) followed by a space, then the heading text.</span></span>

## <a name="resolution"></a><span data-ttu-id="8a4ff-108">解决方法</span><span class="sxs-lookup"><span data-stu-id="8a4ff-108">Resolution</span></span>

<span data-ttu-id="8a4ff-109">若要解决此问题，请确保 H1 包含内容，而不仅仅只包含井号。</span><span class="sxs-lookup"><span data-stu-id="8a4ff-109">To fix this issue, make sure your H1 includes content, not just a hash.</span></span>

<span data-ttu-id="8a4ff-110">不好：</span><span class="sxs-lookup"><span data-stu-id="8a4ff-110">Bad:</span></span>

```markdown
---
author: meganbradley
ms.author: mbradley
---
#
This is not an H1
```

<span data-ttu-id="8a4ff-111">好：</span><span class="sxs-lookup"><span data-stu-id="8a4ff-111">Good:</span></span>

```markdown
---
author: meganbradley
ms.author: mbradley
---
# This is an H1
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]