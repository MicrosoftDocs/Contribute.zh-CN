---
title: ms-service-missing
description: 有关 Docs 生成问题 ms-service-missing 的解释和解决方案
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/2/2019
ms.prod: non-product-specific
ms.openlocfilehash: 2bc425726f82840565978072b2efdf13a1284ec0
ms.sourcegitcommit: 203ca15fda2d217f082c74ec648c1f1db323f9f1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/04/2019
ms.locfileid: "55713076"
---
# <a name="ms-service-missing"></a><span data-ttu-id="d4534-103">ms-service-missing</span><span class="sxs-lookup"><span data-stu-id="d4534-103">ms-service-missing</span></span>

<span data-ttu-id="d4534-104">**即将推出！**</span><span class="sxs-lookup"><span data-stu-id="d4534-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="d4534-105">建议</span><span class="sxs-lookup"><span data-stu-id="d4534-105">Suggestion</span></span>

`Missing attribute: ms.service. If you specify ms.subservice, you must also specify ms.service.`

<span data-ttu-id="d4534-106">请使用 `ms.service` 指定云服务。</span><span class="sxs-lookup"><span data-stu-id="d4534-106">Use `ms.service` to specify cloud services.</span></span> <span data-ttu-id="d4534-107">若要指定有关 `ms.service` 更详细的信息，可以选择指定 `ms.subservice`，但如果指定 `ms.subservice`，则必须同时指定 `ms.service`。</span><span class="sxs-lookup"><span data-stu-id="d4534-107">To specify more detailed information about `ms.service`, you can optionally specify `ms.subservice`, but if you specify `ms.subservice`, you must also specify `ms.service`.</span></span> <span data-ttu-id="d4534-108">`ms.service` 和 `ms.subservice` 的值必须是有效对。</span><span class="sxs-lookup"><span data-stu-id="d4534-108">The values for `ms.service` and `ms.subservice` must be a valid pair.</span></span>

## <a name="resolution"></a><span data-ttu-id="d4534-109">解决方法</span><span class="sxs-lookup"><span data-stu-id="d4534-109">Resolution</span></span>

<span data-ttu-id="d4534-110">请确认所指定的 `ms.subservice` 值对于文章正确无误。</span><span class="sxs-lookup"><span data-stu-id="d4534-110">Confirm that the `ms.subservice` value you've specified is correct for your article.</span></span> <span data-ttu-id="d4534-111">然后添加适当的 `ms.service` 值，该值是 `ms.subservice` 的有效父级。</span><span class="sxs-lookup"><span data-stu-id="d4534-111">Then add the appropriate `ms.service` value that is a valid parent for the `ms.subservice`.</span></span>

<span data-ttu-id="d4534-112">可以在[此 Microsoft 内部网站](https://docsmetadatatool.azurewebsites.net/whitelists)上找到有效值。</span><span class="sxs-lookup"><span data-stu-id="d4534-112">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/whitelists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
