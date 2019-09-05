---
title: ms-prod-missing
description: 有关 Docs 生成问题 ms-prod-missing 的解释和解决方案
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/2/2019
ms.prod: non-product-specific
ms.openlocfilehash: 5f0b5964dd66946f87d4535e134905db731743f2
ms.sourcegitcommit: dd751d0cb5b11f81a64ef62f3c83fd17cc5f0541
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/03/2019
ms.locfileid: "70236292"
---
# <a name="ms-prod-missing"></a><span data-ttu-id="b5244-103">ms-prod-missing</span><span class="sxs-lookup"><span data-stu-id="b5244-103">ms-prod-missing</span></span>

## <a name="warning"></a><span data-ttu-id="b5244-104">警告</span><span class="sxs-lookup"><span data-stu-id="b5244-104">Warning</span></span>

`Missing attribute: ms.prod. If you specify ms.technology, you must also specify ms.prod.`

<span data-ttu-id="b5244-105">请使用 `ms.prod` 指定本地产品。</span><span class="sxs-lookup"><span data-stu-id="b5244-105">Use `ms.prod` to specify on-premises products.</span></span> <span data-ttu-id="b5244-106">若要指定有关 `ms.prod` 更详细的信息，可以选择指定 `ms.technology`，但如果指定 `ms.technology`，则必须同时指定 `ms.prod`。</span><span class="sxs-lookup"><span data-stu-id="b5244-106">To specify more detailed information about `ms.prod`, you can optionally specify `ms.technology`, but if you specify `ms.technology`, you must also specify `ms.prod`.</span></span> <span data-ttu-id="b5244-107">`ms.prod` 和 `ms.technology` 的值必须是有效对。</span><span class="sxs-lookup"><span data-stu-id="b5244-107">The values for `ms.prod` and `ms.technology` must be a valid pair.</span></span>

## <a name="resolution"></a><span data-ttu-id="b5244-108">解决方法</span><span class="sxs-lookup"><span data-stu-id="b5244-108">Resolution</span></span>

<span data-ttu-id="b5244-109">请确认所指定的 `ms.technology` 值对于文章正确无误。</span><span class="sxs-lookup"><span data-stu-id="b5244-109">Confirm that the `ms.technology` value you've specified is correct for your article.</span></span> <span data-ttu-id="b5244-110">然后添加适当的 `ms.prod` 值，该值是 `ms.technology` 的有效父级。</span><span class="sxs-lookup"><span data-stu-id="b5244-110">Then add the appropriate `ms.prod` value that is a valid parent for the `ms.technology`.</span></span>

<span data-ttu-id="b5244-111">可以在[此 Microsoft 内部网站](https://docsmetadatatool.azurewebsites.net/allowlists)上找到有效值。</span><span class="sxs-lookup"><span data-stu-id="b5244-111">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span> <span data-ttu-id="b5244-112">要请求新值，请按照[此过程](https://review.docs.microsoft.com/help/contribute/metadata-changes?branch=master)操作。</span><span class="sxs-lookup"><span data-stu-id="b5244-112">To request new values, follow [this process](https://review.docs.microsoft.com/help/contribute/metadata-changes?branch=master).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
