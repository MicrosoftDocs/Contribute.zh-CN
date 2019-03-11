---
title: external-bookmark-not-found
description: 有关 Docs 生成问题 external-bookmark-not-found 的解释和解决方法
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/26/2019
ms.prod: non-product-specific
ms.openlocfilehash: b533a463ac38d6445ab84c74bf14b2065a0a63f3
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/05/2019
ms.locfileid: "57427182"
---
# <a name="external-bookmark-not-found"></a><span data-ttu-id="c6a01-103">external-bookmark-not-found</span><span class="sxs-lookup"><span data-stu-id="c6a01-103">external-bookmark-not-found</span></span>

## <a name="warning"></a><span data-ttu-id="c6a01-104">警告</span><span class="sxs-lookup"><span data-stu-id="c6a01-104">Warning</span></span>

`File '{file name}' doesn't contain a bookmark named '{bookmark text}'.`

<span data-ttu-id="c6a01-105">想要链接到另一个不存在的文件中的标题。</span><span class="sxs-lookup"><span data-stu-id="c6a01-105">You're trying to link to a heading in another file that doesn't exist.</span></span>

## <a name="resolution"></a><span data-ttu-id="c6a01-106">解决方法</span><span class="sxs-lookup"><span data-stu-id="c6a01-106">Resolution</span></span>

[!INCLUDE [docs-authoring-pack](includes/docs-authoring-pack.md)]

<span data-ttu-id="c6a01-107">查看要链接到的文件并更新书签链接以指向文件中的有效部分。</span><span class="sxs-lookup"><span data-stu-id="c6a01-107">Review the file you're linking to and update your bookmark link to point to a valid section in the file.</span></span>

<span data-ttu-id="c6a01-108">若要链接到另一篇文章中的某个部分标题，请使用文件相对或站点相对链接以及井号，后跟标题内容。</span><span class="sxs-lookup"><span data-stu-id="c6a01-108">To link to a section heading in another article, use the file-relative or site-relative link plus a hash symbol, followed by the words of the heading.</span></span> <span data-ttu-id="c6a01-109">删除标题中的标点符号并将空格替换为短划线。</span><span class="sxs-lookup"><span data-stu-id="c6a01-109">Remove punctuation from the heading and replace spaces with dashes.</span></span> <span data-ttu-id="c6a01-110">下面是一个示例：</span><span class="sxs-lookup"><span data-stu-id="c6a01-110">The following is an example:</span></span>

```markdown
[Managed Disks](../../linux/overview.md#managed-disks)
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
