---
title: ms-prod-and-technology-invalid
description: 有关 Docs 生成问题 ms-prod-and-technology-invalid 的解释和解决方案
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: 20706a44da0320c1a3fc85592a4636efba364dc7
ms.sourcegitcommit: 42e5a6ae071826afc2a32a9b7150ca113b39afdf
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/19/2019
ms.locfileid: "57987574"
---
# <a name="ms-prod-and-technology-invalid"></a><span data-ttu-id="eed9d-103">ms-prod-and-technology-invalid</span><span class="sxs-lookup"><span data-stu-id="eed9d-103">ms-prod-and-technology-invalid</span></span>

<span data-ttu-id="eed9d-104">**即将推出！**</span><span class="sxs-lookup"><span data-stu-id="eed9d-104">**Coming soon!**</span></span>

## <a name="warning"></a><span data-ttu-id="eed9d-105">警告</span><span class="sxs-lookup"><span data-stu-id="eed9d-105">Warning</span></span>

`Invalid value for ms.prod: '{value}'.`

`Invalid value for ms.technology: '{value}' is not valid with ms.prod value '{value}'.`

<span data-ttu-id="eed9d-106">请使用 `ms.prod` 指定本地产品。</span><span class="sxs-lookup"><span data-stu-id="eed9d-106">Use `ms.prod` to specify on-premises products.</span></span> <span data-ttu-id="eed9d-107">若要指定有关 `ms.prod` 更详细的信息，可以选择指定 `ms.technology`。</span><span class="sxs-lookup"><span data-stu-id="eed9d-107">To specify more detailed information about `ms.prod`, you can optionally specify `ms.technology`.</span></span> <span data-ttu-id="eed9d-108">`ms.prod` 和 `ms.technology` 的值必须是有效对。</span><span class="sxs-lookup"><span data-stu-id="eed9d-108">The values for `ms.prod` and `ms.technology` must be a valid pair.</span></span> <span data-ttu-id="eed9d-109">`ms.prod` 值无效，或 `ms.technology` 值与 `ms.prod` 不是有效对。</span><span class="sxs-lookup"><span data-stu-id="eed9d-109">Either your `ms.prod` value is invalid, or your `ms.technology` value is not a valid pair with your `ms.prod`.</span></span>

## <a name="resolution"></a><span data-ttu-id="eed9d-110">解决方法</span><span class="sxs-lookup"><span data-stu-id="eed9d-110">Resolution</span></span>

<span data-ttu-id="eed9d-111">请确认文章的 `ms.prod` 值正确无误。</span><span class="sxs-lookup"><span data-stu-id="eed9d-111">Confirm that your `ms.prod` value is correct for your article.</span></span> <span data-ttu-id="eed9d-112">然后选择有效的 `ms.technology` 值。</span><span class="sxs-lookup"><span data-stu-id="eed9d-112">Then choose a valid `ms.technology` value.</span></span>

<span data-ttu-id="eed9d-113">可以在[此 Microsoft 内部网站](https://docsmetadatatool.azurewebsites.net/allowlists)上找到有效值。</span><span class="sxs-lookup"><span data-stu-id="eed9d-113">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
