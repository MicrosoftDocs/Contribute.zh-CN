---
title: ms-prod-missing
description: 有关 Docs 生成问题 ms-prod-missing 的解释和解决方案
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/2/2019
ms.prod: non-product-specific
ms.openlocfilehash: ee29396a20345f6884a5bbc94aa25f48dafaff52
ms.sourcegitcommit: 203ca15fda2d217f082c74ec648c1f1db323f9f1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/04/2019
ms.locfileid: "55713214"
---
# <a name="ms-prod-missing"></a><span data-ttu-id="6ba83-103">ms-prod-missing</span><span class="sxs-lookup"><span data-stu-id="6ba83-103">ms-prod-missing</span></span>

<span data-ttu-id="6ba83-104">**即将推出！**</span><span class="sxs-lookup"><span data-stu-id="6ba83-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="6ba83-105">建议</span><span class="sxs-lookup"><span data-stu-id="6ba83-105">Suggestion</span></span>

`Missing attribute: ms.prod. If you specify ms.technology, you must also specify ms.prod.`

<span data-ttu-id="6ba83-106">请使用 `ms.prod` 指定本地产品。</span><span class="sxs-lookup"><span data-stu-id="6ba83-106">Use `ms.prod` to specify on-premises products.</span></span> <span data-ttu-id="6ba83-107">若要指定有关 `ms.prod` 更详细的信息，可以选择指定 `ms.technology`，但如果指定 `ms.technology`，则必须同时指定 `ms.prod`。</span><span class="sxs-lookup"><span data-stu-id="6ba83-107">To specify more detailed information about `ms.prod`, you can optionally specify `ms.technology`, but if you specify `ms.technology`, you must also specify `ms.prod`.</span></span> <span data-ttu-id="6ba83-108">`ms.prod` 和 `ms.technology` 的值必须是有效对。</span><span class="sxs-lookup"><span data-stu-id="6ba83-108">The values for `ms.prod` and `ms.technology` must be a valid pair.</span></span>

## <a name="resolution"></a><span data-ttu-id="6ba83-109">解决方法</span><span class="sxs-lookup"><span data-stu-id="6ba83-109">Resolution</span></span>

<span data-ttu-id="6ba83-110">请确认所指定的 `ms.technology` 值对于文章正确无误。</span><span class="sxs-lookup"><span data-stu-id="6ba83-110">Confirm that the `ms.technology` value you've specified is correct for your article.</span></span> <span data-ttu-id="6ba83-111">然后添加适当的 `ms.prod` 值，该值是 `ms.technology` 的有效父级。</span><span class="sxs-lookup"><span data-stu-id="6ba83-111">Then add the appropriate `ms.prod` value that is a valid parent for the `ms.technology`.</span></span>

<span data-ttu-id="6ba83-112">可以在[此 Microsoft 内部网站](https://docsmetadatatool.azurewebsites.net/whitelists)上找到有效值。</span><span class="sxs-lookup"><span data-stu-id="6ba83-112">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/whitelists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
