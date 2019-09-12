---
title: internal-bookmark-not-found
description: 有关 Docs 生成问题 internal-bookmark-not-found 的解释和解决方法
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 9/10/2019
ms.prod: non-product-specific
ms.openlocfilehash: 53b98f8da199e3495cc00b2388d983191268eee6
ms.sourcegitcommit: 89147521f0aa3b39e7ddf390136b09a43d95c416
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/10/2019
ms.locfileid: "70856211"
---
# <a name="bookmark-not-found"></a><span data-ttu-id="68b06-103">bookmark-not-found</span><span class="sxs-lookup"><span data-stu-id="68b06-103">bookmark-not-found</span></span>

## <a name="warning"></a><span data-ttu-id="68b06-104">警告</span><span class="sxs-lookup"><span data-stu-id="68b06-104">Warning</span></span>

`Cannot find bookmark '{bookmark-id}' in '{parent-file}'.`

<span data-ttu-id="68b06-105">想要链接到当前文件或其他文件中不存在的标题。</span><span class="sxs-lookup"><span data-stu-id="68b06-105">You're trying to link to a heading in the current file or another file that doesn't exist.</span></span>

## <a name="resolution"></a><span data-ttu-id="68b06-106">解决方法</span><span class="sxs-lookup"><span data-stu-id="68b06-106">Resolution</span></span>

[!INCLUDE [docs-authoring-pack](includes/docs-authoring-pack.md)]

<span data-ttu-id="68b06-107">验证你想要链接到的标题并更新链接。</span><span class="sxs-lookup"><span data-stu-id="68b06-107">Verify the heading you want to link to and update the link.</span></span>

<span data-ttu-id="68b06-108">若要链接到当前文章中的某个部分，请使用一个井号，后跟标题内容。</span><span class="sxs-lookup"><span data-stu-id="68b06-108">To link to a section in the current article, use a hash symbol, followed by the words of the heading.</span></span> <span data-ttu-id="68b06-109">删除标题中的标点符号并将空格替换为短划线。</span><span class="sxs-lookup"><span data-stu-id="68b06-109">Remove punctuation from the heading and replace spaces with dashes.</span></span> <span data-ttu-id="68b06-110">下面是一个示例：</span><span class="sxs-lookup"><span data-stu-id="68b06-110">The following is an example:</span></span>

```markdown
[Managed Disks](#managed-disks)
```

<span data-ttu-id="68b06-111">若要链接到另一个文件中的标题，请使用指向该文件的相对链接，后面跟有一个哈希符号和标题的文字。</span><span class="sxs-lookup"><span data-stu-id="68b06-111">To link to a heading in another file, use a relative link to that file, followed by a hash symbol and the words of the heading.</span></span> <span data-ttu-id="68b06-112">删除标题中的标点符号并将空格替换为短划线。</span><span class="sxs-lookup"><span data-stu-id="68b06-112">Remove punctuation from the heading and replace spaces with dashes.</span></span> <span data-ttu-id="68b06-113">下面是一个示例：</span><span class="sxs-lookup"><span data-stu-id="68b06-113">The following is an example:</span></span>

```markdown
See [the Resolution section in h1-empty](h1-empty.md#resolution).
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
