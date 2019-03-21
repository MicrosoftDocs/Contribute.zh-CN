---
title: ms-service-and-subservice-invalid
description: 有关 Docs 生成问题 ms-service-and-subservice-invalid 的解释和解决方案
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: 7dee18e7b902b660a8071bcb4a0dee21c19f4f7f
ms.sourcegitcommit: 42e5a6ae071826afc2a32a9b7150ca113b39afdf
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/19/2019
ms.locfileid: "57987629"
---
# <a name="ms-service-and-subservice-invalid"></a><span data-ttu-id="bf2de-103">ms-service-and-subservice-invalid</span><span class="sxs-lookup"><span data-stu-id="bf2de-103">ms-service-and-subservice-invalid</span></span>

<span data-ttu-id="bf2de-104">**即将推出！**</span><span class="sxs-lookup"><span data-stu-id="bf2de-104">**Coming soon!**</span></span>

## <a name="warning"></a><span data-ttu-id="bf2de-105">警告</span><span class="sxs-lookup"><span data-stu-id="bf2de-105">Warning</span></span>

`Invalid value for ms.service: '{value}'.`

`Invalid value for ms.subservice: '{value}' is not valid with ms.service value '{value}'.`

<span data-ttu-id="bf2de-106">请使用 `ms.service` 指定云服务。</span><span class="sxs-lookup"><span data-stu-id="bf2de-106">Use `ms.service` to specify cloud services.</span></span> <span data-ttu-id="bf2de-107">若要指定有关 `ms.service` 更详细的信息，可以选择指定 `ms.subservice`。</span><span class="sxs-lookup"><span data-stu-id="bf2de-107">To specify more detailed information about `ms.service`, you can optionally specify `ms.subservice`.</span></span> <span data-ttu-id="bf2de-108">`ms.service` 和 `ms.subservice` 的值必须是有效对。</span><span class="sxs-lookup"><span data-stu-id="bf2de-108">The values for `ms.service` and `ms.subservice` must be a valid pair.</span></span> <span data-ttu-id="bf2de-109">`ms.service` 值无效，或 `ms.subservice` 值与 `ms.service` 不是有效对。</span><span class="sxs-lookup"><span data-stu-id="bf2de-109">Either your `ms.service` value is invalid, or your `ms.subservice` value is not a valid pair with your `ms.service`.</span></span>

## <a name="resolution"></a><span data-ttu-id="bf2de-110">解决方法</span><span class="sxs-lookup"><span data-stu-id="bf2de-110">Resolution</span></span>

<span data-ttu-id="bf2de-111">请确认文章的 `ms.service` 值正确无误。</span><span class="sxs-lookup"><span data-stu-id="bf2de-111">Confirm that your `ms.service` value is correct for your article.</span></span> <span data-ttu-id="bf2de-112">然后选择有效的 `ms.subservice` 值。</span><span class="sxs-lookup"><span data-stu-id="bf2de-112">Then choose a valid `ms.subservice` value.</span></span>

<span data-ttu-id="bf2de-113">可以在[此 Microsoft 内部网站](https://docsmetadatatool.azurewebsites.net/allowlists)上找到有效值。</span><span class="sxs-lookup"><span data-stu-id="bf2de-113">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
