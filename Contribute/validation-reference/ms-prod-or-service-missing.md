---
title: ms-prod-or-service-missing
description: 有关 Docs 生成问题 ms-prod-or-service-missing 的解释和解决方案
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/20/2018
ms.prod: non-product-specific
ms.openlocfilehash: 6eeb4a95e4d4aeba527b1078bc646fcbc56898a2
ms.sourcegitcommit: 42e5a6ae071826afc2a32a9b7150ca113b39afdf
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/19/2019
ms.locfileid: "57987551"
---
# <a name="ms-prod-or-service-missing"></a><span data-ttu-id="80007-103">ms-prod-or-service-missing</span><span class="sxs-lookup"><span data-stu-id="80007-103">ms-prod-or-service-missing</span></span>

<span data-ttu-id="80007-104">**即将推出！**</span><span class="sxs-lookup"><span data-stu-id="80007-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="80007-105">建议</span><span class="sxs-lookup"><span data-stu-id="80007-105">Suggestion</span></span>

`Missing attribute: either ms.prod or ms.service is required. Use ms.prod for on-premise products, or ms.service for cloud services.`

## <a name="resolution"></a><span data-ttu-id="80007-106">解决方法</span><span class="sxs-lookup"><span data-stu-id="80007-106">Resolution</span></span>

<span data-ttu-id="80007-107">`ms.prod` 或 `ms.service` 是必需的，但它们不能同时存在：`ms.prod` 用于本地产品；`ms.service` 用于云服务。</span><span class="sxs-lookup"><span data-stu-id="80007-107">Either `ms.prod` or `ms.service` is required, and they can't both be present: `ms.prod` is used for on-premises products; `ms.service` is used for cloud services.</span></span> <span data-ttu-id="80007-108">请确定哪个适合你的文章，验证该值正确无误，并删除另一个字段。</span><span class="sxs-lookup"><span data-stu-id="80007-108">Determine which is appropriate for your article, verify that the value is correct, and remove the other field.</span></span>

<span data-ttu-id="80007-109">可以在[此 Microsoft 内部网站](https://docsmetadatatool.azurewebsites.net/allowlists)上找到有效值。</span><span class="sxs-lookup"><span data-stu-id="80007-109">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]