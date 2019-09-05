---
title: ms-service-missing
description: 有关 Docs 生成问题 ms-service-missing 的解释和解决方案
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/2/2019
ms.prod: non-product-specific
ms.openlocfilehash: b50d9d6f57c953569a4e5dd873961b8c511a8bb1
ms.sourcegitcommit: dd751d0cb5b11f81a64ef62f3c83fd17cc5f0541
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/03/2019
ms.locfileid: "70236502"
---
# <a name="ms-service-missing"></a><span data-ttu-id="227f4-103">ms-service-missing</span><span class="sxs-lookup"><span data-stu-id="227f4-103">ms-service-missing</span></span>

## <a name="warning"></a><span data-ttu-id="227f4-104">警告</span><span class="sxs-lookup"><span data-stu-id="227f4-104">Warning</span></span>

`Missing attribute: ms.service. If you specify ms.subservice, you must also specify ms.service.`

<span data-ttu-id="227f4-105">请使用 `ms.service` 指定云服务。</span><span class="sxs-lookup"><span data-stu-id="227f4-105">Use `ms.service` to specify cloud services.</span></span> <span data-ttu-id="227f4-106">若要指定有关 `ms.service` 更详细的信息，可以选择指定 `ms.subservice`，但如果指定 `ms.subservice`，则必须同时指定 `ms.service`。</span><span class="sxs-lookup"><span data-stu-id="227f4-106">To specify more detailed information about `ms.service`, you can optionally specify `ms.subservice`, but if you specify `ms.subservice`, you must also specify `ms.service`.</span></span> <span data-ttu-id="227f4-107">`ms.service` 和 `ms.subservice` 的值必须是有效对。</span><span class="sxs-lookup"><span data-stu-id="227f4-107">The values for `ms.service` and `ms.subservice` must be a valid pair.</span></span>

## <a name="resolution"></a><span data-ttu-id="227f4-108">解决方法</span><span class="sxs-lookup"><span data-stu-id="227f4-108">Resolution</span></span>

<span data-ttu-id="227f4-109">请确认所指定的 `ms.subservice` 值对于文章正确无误。</span><span class="sxs-lookup"><span data-stu-id="227f4-109">Confirm that the `ms.subservice` value you've specified is correct for your article.</span></span> <span data-ttu-id="227f4-110">然后添加适当的 `ms.service` 值，该值是 `ms.subservice` 的有效父级。</span><span class="sxs-lookup"><span data-stu-id="227f4-110">Then add the appropriate `ms.service` value that is a valid parent for the `ms.subservice`.</span></span>

<span data-ttu-id="227f4-111">可以在[此 Microsoft 内部网站](https://docsmetadatatool.azurewebsites.net/allowlists)上找到有效值。</span><span class="sxs-lookup"><span data-stu-id="227f4-111">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span> <span data-ttu-id="227f4-112">要请求新值，请按照[此过程](https://review.docs.microsoft.com/help/contribute/metadata-changes?branch=master)操作。</span><span class="sxs-lookup"><span data-stu-id="227f4-112">To request new values, follow [this process](https://review.docs.microsoft.com/help/contribute/metadata-changes?branch=master).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
