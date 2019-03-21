---
title: ms-prod-missing
description: 有关 Docs 生成问题 ms-prod-missing 的解释和解决方案
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/2/2019
ms.prod: non-product-specific
ms.openlocfilehash: 2578ab47dab315a446529d24357e9489d7fd0bad
ms.sourcegitcommit: 42e5a6ae071826afc2a32a9b7150ca113b39afdf
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/19/2019
ms.locfileid: "57987689"
---
# <a name="ms-prod-missing"></a><span data-ttu-id="2eaa8-103">ms-prod-missing</span><span class="sxs-lookup"><span data-stu-id="2eaa8-103">ms-prod-missing</span></span>

<span data-ttu-id="2eaa8-104">**即将推出！**</span><span class="sxs-lookup"><span data-stu-id="2eaa8-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="2eaa8-105">建议</span><span class="sxs-lookup"><span data-stu-id="2eaa8-105">Suggestion</span></span>

`Missing attribute: ms.prod. If you specify ms.technology, you must also specify ms.prod.`

<span data-ttu-id="2eaa8-106">请使用 `ms.prod` 指定本地产品。</span><span class="sxs-lookup"><span data-stu-id="2eaa8-106">Use `ms.prod` to specify on-premises products.</span></span> <span data-ttu-id="2eaa8-107">若要指定有关 `ms.prod` 更详细的信息，可以选择指定 `ms.technology`，但如果指定 `ms.technology`，则必须同时指定 `ms.prod`。</span><span class="sxs-lookup"><span data-stu-id="2eaa8-107">To specify more detailed information about `ms.prod`, you can optionally specify `ms.technology`, but if you specify `ms.technology`, you must also specify `ms.prod`.</span></span> <span data-ttu-id="2eaa8-108">`ms.prod` 和 `ms.technology` 的值必须是有效对。</span><span class="sxs-lookup"><span data-stu-id="2eaa8-108">The values for `ms.prod` and `ms.technology` must be a valid pair.</span></span>

## <a name="resolution"></a><span data-ttu-id="2eaa8-109">解决方法</span><span class="sxs-lookup"><span data-stu-id="2eaa8-109">Resolution</span></span>

<span data-ttu-id="2eaa8-110">请确认所指定的 `ms.technology` 值对于文章正确无误。</span><span class="sxs-lookup"><span data-stu-id="2eaa8-110">Confirm that the `ms.technology` value you've specified is correct for your article.</span></span> <span data-ttu-id="2eaa8-111">然后添加适当的 `ms.prod` 值，该值是 `ms.technology` 的有效父级。</span><span class="sxs-lookup"><span data-stu-id="2eaa8-111">Then add the appropriate `ms.prod` value that is a valid parent for the `ms.technology`.</span></span>

<span data-ttu-id="2eaa8-112">可以在[此 Microsoft 内部网站](https://docsmetadatatool.azurewebsites.net/allowlists)上找到有效值。</span><span class="sxs-lookup"><span data-stu-id="2eaa8-112">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
