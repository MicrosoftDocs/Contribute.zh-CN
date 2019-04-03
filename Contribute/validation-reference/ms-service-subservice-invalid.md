---
title: ms-service-and-subservice-invalid
description: 有关 Docs 生成问题 ms-service-and-subservice-invalid 的解释和解决方案
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: 3f165d16eed7e937c7db912a9c5e0ee0809e3031
ms.sourcegitcommit: 8e897e90268a8a87dc4b97d7c28d22ed5950c8d9
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/29/2019
ms.locfileid: "58637290"
---
# <a name="ms-service-and-subservice-invalid"></a><span data-ttu-id="0aed7-103">ms-service-and-subservice-invalid</span><span class="sxs-lookup"><span data-stu-id="0aed7-103">ms-service-and-subservice-invalid</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="0aed7-104">建议</span><span class="sxs-lookup"><span data-stu-id="0aed7-104">Suggestion</span></span>

`Invalid value for ms.service: '{value}'.`

`Invalid value for ms.subservice: '{value}' is not valid with ms.service value '{value}'.`

<span data-ttu-id="0aed7-105">请使用 `ms.service` 指定云服务。</span><span class="sxs-lookup"><span data-stu-id="0aed7-105">Use `ms.service` to specify cloud services.</span></span> <span data-ttu-id="0aed7-106">若要指定有关 `ms.service` 更详细的信息，可以选择指定 `ms.subservice`。</span><span class="sxs-lookup"><span data-stu-id="0aed7-106">To specify more detailed information about `ms.service`, you can optionally specify `ms.subservice`.</span></span> <span data-ttu-id="0aed7-107">`ms.service` 和 `ms.subservice` 的值必须是有效对。</span><span class="sxs-lookup"><span data-stu-id="0aed7-107">The values for `ms.service` and `ms.subservice` must be a valid pair.</span></span> <span data-ttu-id="0aed7-108">`ms.service` 值无效，或 `ms.subservice` 值与 `ms.service` 不是有效对。</span><span class="sxs-lookup"><span data-stu-id="0aed7-108">Either your `ms.service` value is invalid, or your `ms.subservice` value is not a valid pair with your `ms.service`.</span></span>

## <a name="resolution"></a><span data-ttu-id="0aed7-109">解决方法</span><span class="sxs-lookup"><span data-stu-id="0aed7-109">Resolution</span></span>

<span data-ttu-id="0aed7-110">请确认文章的 `ms.service` 值正确无误。</span><span class="sxs-lookup"><span data-stu-id="0aed7-110">Confirm that your `ms.service` value is correct for your article.</span></span> <span data-ttu-id="0aed7-111">然后选择有效的 `ms.subservice` 值。</span><span class="sxs-lookup"><span data-stu-id="0aed7-111">Then choose a valid `ms.subservice` value.</span></span>

<span data-ttu-id="0aed7-112">可以在[此 Microsoft 内部网站](https://docsmetadatatool.azurewebsites.net/allowlists)上找到有效值。</span><span class="sxs-lookup"><span data-stu-id="0aed7-112">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
