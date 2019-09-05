---
title: ms-prod-or-service-missing
description: 有关 Docs 生成问题 ms-prod-or-service-missing 的解释和解决方案
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/20/2018
ms.prod: non-product-specific
ms.openlocfilehash: 93351fa343603a0b9d60e4b3e3ae41ce90d9912e
ms.sourcegitcommit: dd751d0cb5b11f81a64ef62f3c83fd17cc5f0541
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/03/2019
ms.locfileid: "70236291"
---
# <a name="ms-prod-or-service-missing"></a><span data-ttu-id="05cfe-103">ms-prod-or-service-missing</span><span class="sxs-lookup"><span data-stu-id="05cfe-103">ms-prod-or-service-missing</span></span>

## <a name="warning"></a><span data-ttu-id="05cfe-104">警告</span><span class="sxs-lookup"><span data-stu-id="05cfe-104">Warning</span></span>

`Missing attribute: either ms.prod or ms.service is required. Use ms.prod for on-premise products, or ms.service for cloud services.`

## <a name="resolution"></a><span data-ttu-id="05cfe-105">解决方法</span><span class="sxs-lookup"><span data-stu-id="05cfe-105">Resolution</span></span>

<span data-ttu-id="05cfe-106">`ms.prod` 或 `ms.service` 是必需的，但它们不能同时存在：`ms.prod` 用于本地产品；`ms.service` 用于云服务。</span><span class="sxs-lookup"><span data-stu-id="05cfe-106">Either `ms.prod` or `ms.service` is required, and they can't both be present: `ms.prod` is used for on-premises products; `ms.service` is used for cloud services.</span></span> <span data-ttu-id="05cfe-107">请确定哪个适合你的文章，验证该值正确无误，并删除另一个字段。</span><span class="sxs-lookup"><span data-stu-id="05cfe-107">Determine which is appropriate for your article, verify that the value is correct, and remove the other field.</span></span>

<span data-ttu-id="05cfe-108">可以在[此 Microsoft 内部网站](https://docsmetadatatool.azurewebsites.net/allowlists)上找到有效值。</span><span class="sxs-lookup"><span data-stu-id="05cfe-108">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span> <span data-ttu-id="05cfe-109">要请求新值，请按照[此过程](https://review.docs.microsoft.com/help/contribute/metadata-changes?branch=master)操作。</span><span class="sxs-lookup"><span data-stu-id="05cfe-109">To request new values, follow [this process](https://review.docs.microsoft.com/help/contribute/metadata-changes?branch=master).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
