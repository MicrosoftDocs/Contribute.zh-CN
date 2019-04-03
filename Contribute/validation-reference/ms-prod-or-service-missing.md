---
title: ms-prod-or-service-missing
description: 有关 Docs 生成问题 ms-prod-or-service-missing 的解释和解决方案
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/20/2018
ms.prod: non-product-specific
ms.openlocfilehash: 8d8d01f95af74009cfa9cb1a57531663df4edf4d
ms.sourcegitcommit: 8e897e90268a8a87dc4b97d7c28d22ed5950c8d9
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/29/2019
ms.locfileid: "58637359"
---
# <a name="ms-prod-or-service-missing"></a><span data-ttu-id="92266-103">ms-prod-or-service-missing</span><span class="sxs-lookup"><span data-stu-id="92266-103">ms-prod-or-service-missing</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="92266-104">建议</span><span class="sxs-lookup"><span data-stu-id="92266-104">Suggestion</span></span>

`Missing attribute: either ms.prod or ms.service is required. Use ms.prod for on-premise products, or ms.service for cloud services.`

## <a name="resolution"></a><span data-ttu-id="92266-105">解决方法</span><span class="sxs-lookup"><span data-stu-id="92266-105">Resolution</span></span>

<span data-ttu-id="92266-106">`ms.prod` 或 `ms.service` 是必需的，但它们不能同时存在：`ms.prod` 用于本地产品；`ms.service` 用于云服务。</span><span class="sxs-lookup"><span data-stu-id="92266-106">Either `ms.prod` or `ms.service` is required, and they can't both be present: `ms.prod` is used for on-premises products; `ms.service` is used for cloud services.</span></span> <span data-ttu-id="92266-107">请确定哪个适合你的文章，验证该值正确无误，并删除另一个字段。</span><span class="sxs-lookup"><span data-stu-id="92266-107">Determine which is appropriate for your article, verify that the value is correct, and remove the other field.</span></span>

<span data-ttu-id="92266-108">可以在[此 Microsoft 内部网站](https://docsmetadatatool.azurewebsites.net/allowlists)上找到有效值。</span><span class="sxs-lookup"><span data-stu-id="92266-108">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]