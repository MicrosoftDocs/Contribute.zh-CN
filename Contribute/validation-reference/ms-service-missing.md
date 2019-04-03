---
title: ms-service-missing
description: 有关 Docs 生成问题 ms-service-missing 的解释和解决方案
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/2/2019
ms.prod: non-product-specific
ms.openlocfilehash: 17e2e272e3a21e14e038e27ff68866afe28bee60
ms.sourcegitcommit: 8e897e90268a8a87dc4b97d7c28d22ed5950c8d9
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/29/2019
ms.locfileid: "58636692"
---
# <a name="ms-service-missing"></a><span data-ttu-id="16c30-103">ms-service-missing</span><span class="sxs-lookup"><span data-stu-id="16c30-103">ms-service-missing</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="16c30-104">建议</span><span class="sxs-lookup"><span data-stu-id="16c30-104">Suggestion</span></span>

`Missing attribute: ms.service. If you specify ms.subservice, you must also specify ms.service.`

<span data-ttu-id="16c30-105">请使用 `ms.service` 指定云服务。</span><span class="sxs-lookup"><span data-stu-id="16c30-105">Use `ms.service` to specify cloud services.</span></span> <span data-ttu-id="16c30-106">若要指定有关 `ms.service` 更详细的信息，可以选择指定 `ms.subservice`，但如果指定 `ms.subservice`，则必须同时指定 `ms.service`。</span><span class="sxs-lookup"><span data-stu-id="16c30-106">To specify more detailed information about `ms.service`, you can optionally specify `ms.subservice`, but if you specify `ms.subservice`, you must also specify `ms.service`.</span></span> <span data-ttu-id="16c30-107">`ms.service` 和 `ms.subservice` 的值必须是有效对。</span><span class="sxs-lookup"><span data-stu-id="16c30-107">The values for `ms.service` and `ms.subservice` must be a valid pair.</span></span>

## <a name="resolution"></a><span data-ttu-id="16c30-108">解决方法</span><span class="sxs-lookup"><span data-stu-id="16c30-108">Resolution</span></span>

<span data-ttu-id="16c30-109">请确认所指定的 `ms.subservice` 值对于文章正确无误。</span><span class="sxs-lookup"><span data-stu-id="16c30-109">Confirm that the `ms.subservice` value you've specified is correct for your article.</span></span> <span data-ttu-id="16c30-110">然后添加适当的 `ms.service` 值，该值是 `ms.subservice` 的有效父级。</span><span class="sxs-lookup"><span data-stu-id="16c30-110">Then add the appropriate `ms.service` value that is a valid parent for the `ms.subservice`.</span></span>

<span data-ttu-id="16c30-111">可以在[此 Microsoft 内部网站](https://docsmetadatatool.azurewebsites.net/allowlists)上找到有效值。</span><span class="sxs-lookup"><span data-stu-id="16c30-111">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
