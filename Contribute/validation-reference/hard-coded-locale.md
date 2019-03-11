---
title: hard-coded-locale
description: 有关 Docs 生成问题 hard-coded-locale 的解释和解决方法。
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: 1862014076fa4cbff18535095b244e8f94a17b0f
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/05/2019
ms.locfileid: "57427172"
---
# <a name="hard-coded-locale"></a><span data-ttu-id="5b27b-103">hard-coded-locale</span><span class="sxs-lookup"><span data-stu-id="5b27b-103">hard-coded-locale</span></span>

## <a name="warning"></a><span data-ttu-id="5b27b-104">警告</span><span class="sxs-lookup"><span data-stu-id="5b27b-104">Warning</span></span>

`Link {URL} contains locale code {code}. For localizability, remove {code} from links to Microsoft sites.`

<span data-ttu-id="5b27b-105">区域设置代码（例如 `en-us`）不应包含在指向某些 Microsoft 站点的链接中。</span><span class="sxs-lookup"><span data-stu-id="5b27b-105">Locale codes, such as `en-us`, should not be included in links to certain Microsoft sites.</span></span> <span data-ttu-id="5b27b-106">如果在英语内容的链接中包含区域设置代码，它也将包含在本地化链接中，这会导致糟糕的本地化体验。</span><span class="sxs-lookup"><span data-stu-id="5b27b-106">If you include a locale code in a link in English content, it will also be included in localized links, which leads to a bad localized experience.</span></span> <span data-ttu-id="5b27b-107">例如，如果德语本地化内容中的链接包含 `en-us`，则德语客户会发现即使有德语版本，自己也被链接到了英文文章。</span><span class="sxs-lookup"><span data-stu-id="5b27b-107">For example, if a link in German localized content includes `en-us`, German customers will find themselves linking to the English article, even if a German version is available.</span></span>

<span data-ttu-id="5b27b-108">以下站点适用于此验证：</span><span class="sxs-lookup"><span data-stu-id="5b27b-108">The following sites are in scope for this validation:</span></span>

- <span data-ttu-id="5b27b-109">azure.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="5b27b-109">azure.microsoft.com</span></span>
- <span data-ttu-id="5b27b-110">docs.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="5b27b-110">docs.microsoft.com</span></span>
- <span data-ttu-id="5b27b-111">msdn.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="5b27b-111">msdn.microsoft.com</span></span>
- <span data-ttu-id="5b27b-112">technet.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="5b27b-112">technet.microsoft.com</span></span>

## <a name="resolution"></a><span data-ttu-id="5b27b-113">解决方法</span><span class="sxs-lookup"><span data-stu-id="5b27b-113">Resolution</span></span>

<span data-ttu-id="5b27b-114">从 Microsoft 站点的链接中删除区域设置代码。</span><span class="sxs-lookup"><span data-stu-id="5b27b-114">Remove locale codes from links to Microsoft sites.</span></span> <span data-ttu-id="5b27b-115">下面是一个示例。</span><span class="sxs-lookup"><span data-stu-id="5b27b-115">The following is an example.</span></span>

<span data-ttu-id="5b27b-116">之前：</span><span class="sxs-lookup"><span data-stu-id="5b27b-116">Before:</span></span>

`https://docs.microsoft.com/en-us/vsts/load-test/app-service-web-app-performance-test`

<span data-ttu-id="5b27b-117">之后：</span><span class="sxs-lookup"><span data-stu-id="5b27b-117">After:</span></span>

`https://docs.microsoft.com/vsts/load-test/app-service-web-app-performance-test`

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]