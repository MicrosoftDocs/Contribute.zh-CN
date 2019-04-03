---
title: ms-prod-service-mismatch
description: 有关 Docs 生成问题 ms-prod-service-mismatch 的解释和解决方案
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: a8d1698a4842ace0e5dd07db170f40a310c666a6
ms.sourcegitcommit: 8e897e90268a8a87dc4b97d7c28d22ed5950c8d9
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/29/2019
ms.locfileid: "58636784"
---
# <a name="ms-prod-service-mismatch"></a><span data-ttu-id="43bc8-103">ms-prod-service-mismatch</span><span class="sxs-lookup"><span data-stu-id="43bc8-103">ms-prod-service-mismatch</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="43bc8-104">建议</span><span class="sxs-lookup"><span data-stu-id="43bc8-104">Suggestion</span></span>

`Invalid attribute pair: ms.prod and ms.subservice. You can only pair ms.prod with ms.technology.`

`Invalid attribute pair: ms.service and ms.technology. You can only pair ms.service with ms.subservice.`

<span data-ttu-id="43bc8-105">请使用 `ms.prod` 指定本地产品；`ms.service` 用于云服务。</span><span class="sxs-lookup"><span data-stu-id="43bc8-105">Use `ms.prod` to specify on-premises products; `ms.service` for cloud services.</span></span> <span data-ttu-id="43bc8-106">若要指定有关 `ms.prod` 更详细的信息，可以选择指定 `ms.technology`。</span><span class="sxs-lookup"><span data-stu-id="43bc8-106">To specify more detailed information about `ms.prod`, you can optionally specify `ms.technology`.</span></span> <span data-ttu-id="43bc8-107">若要指定有关 `ms.service` 更详细的信息，可以指定 `ms.subservice`。</span><span class="sxs-lookup"><span data-stu-id="43bc8-107">To specify more detailed information about `ms.service`, you can specify `ms.subservice`.</span></span> <span data-ttu-id="43bc8-108">不能将 `ms.prod` 与 `ms.subservice` 一起使用，也不能将 `ms.service` 与 `ms.technology` 一起使用。</span><span class="sxs-lookup"><span data-stu-id="43bc8-108">You can't use `ms.prod` with `ms.subservice` or `ms.service` with `ms.technology`.</span></span>

## <a name="resolution"></a><span data-ttu-id="43bc8-109">解决方法</span><span class="sxs-lookup"><span data-stu-id="43bc8-109">Resolution</span></span>

<span data-ttu-id="43bc8-110">首先，请验证是否已为文章选择了正确的父属性（`ms.prod` 或 `ms.service`）。</span><span class="sxs-lookup"><span data-stu-id="43bc8-110">First, verify that you have selected the correct parent attribute (`ms.prod` or `ms.service`) for your article.</span></span> <span data-ttu-id="43bc8-111">然后，添加具有有效成对值的相应子字段。</span><span class="sxs-lookup"><span data-stu-id="43bc8-111">Then, add the appropriate child field with a valid paired value.</span></span> <span data-ttu-id="43bc8-112">删除所有额外字段。</span><span class="sxs-lookup"><span data-stu-id="43bc8-112">Remove any extra fields.</span></span>

<span data-ttu-id="43bc8-113">可以在[此 Microsoft 内部网站](https://docsmetadatatool.azurewebsites.net/allowlists)上找到有效值。</span><span class="sxs-lookup"><span data-stu-id="43bc8-113">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
