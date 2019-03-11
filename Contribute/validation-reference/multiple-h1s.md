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
# <a name="multiple-h1"></a><span data-ttu-id="99a90-103">multiple-h1</span><span class="sxs-lookup"><span data-stu-id="99a90-103">multiple-h1</span></span>

## <a name="warning"></a><span data-ttu-id="99a90-104">警告</span><span class="sxs-lookup"><span data-stu-id="99a90-104">Warning</span></span>

`Multiple H1s are not allowed. You can only have one top-level heading.`

<span data-ttu-id="99a90-105">H1 是指 Markdown 文件中的第一个标题。</span><span class="sxs-lookup"><span data-stu-id="99a90-105">H1 refers to the first heading in a Markdown file.</span></span> <span data-ttu-id="99a90-106">发布到 docs.microsoft.com 时，H1 以大字体显示在页面顶部。</span><span class="sxs-lookup"><span data-stu-id="99a90-106">When published to docs.microsoft.com, the H1 shows at the top of the page in a large font.</span></span> <span data-ttu-id="99a90-107">H1 的创建方式为，以包含一个井号 (#) 的行开头，后跟空格，然后是标题文本。</span><span class="sxs-lookup"><span data-stu-id="99a90-107">An H1 is created by beginning a line with a single hash (#) followed by a space, then the heading text.</span></span> <span data-ttu-id="99a90-108">一个文件中只能有一个 H1。</span><span class="sxs-lookup"><span data-stu-id="99a90-108">You can only have one H1 in each file.</span></span>

## <a name="resolution"></a><span data-ttu-id="99a90-109">解决方法</span><span class="sxs-lookup"><span data-stu-id="99a90-109">Resolution</span></span>

<span data-ttu-id="99a90-110">若要解决此问题，请将后续 H1s 的标题级别更改为 H2 (`##`)，否则请重新组织文件。</span><span class="sxs-lookup"><span data-stu-id="99a90-110">To fix this issue, change the heading level of subsequent H1s to H2 (`##`), or otherwise reorganize your file.</span></span> <span data-ttu-id="99a90-111">请注意，不允许跳过标题级别，如 H1 之后为 H3。</span><span class="sxs-lookup"><span data-stu-id="99a90-111">Note that skipping heading levels, such as following H1 with H3, is not allowed.</span></span>

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