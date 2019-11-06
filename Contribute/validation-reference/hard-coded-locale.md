---
title: hard-coded-locale
description: 有关 Docs 生成问题 hard-coded-locale 的解释和解决方法。
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 10/18/2019
ms.prod: non-product-specific
ms.openlocfilehash: 1ab511398cbd622906ccb0a67e2b24968ee29374
ms.sourcegitcommit: 55624c641bea5367bcfa08655c085bc950e8beae
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/30/2019
ms.locfileid: "73166825"
---
# <a name="hard-coded-locale"></a><span data-ttu-id="3dfb6-103">hard-coded-locale</span><span class="sxs-lookup"><span data-stu-id="3dfb6-103">hard-coded-locale</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3dfb6-104">此规则最初作为“建议”启用，以便内容团队有时间衡量影响并制定清理其存储库的计划。</span><span class="sxs-lookup"><span data-stu-id="3dfb6-104">This rule was initially enabled as a "Suggestion" to give content teams time to gauge impact and develop a plan to clean up their repos.</span></span> <span data-ttu-id="3dfb6-105">**它将于 2019 年 12 月 20 日提升为“警告”** 。</span><span class="sxs-lookup"><span data-stu-id="3dfb6-105">**It will be elevated to a "Warning" on 12/20/2019**.</span></span>

## <a name="suggestion"></a><span data-ttu-id="3dfb6-106">建议</span><span class="sxs-lookup"><span data-stu-id="3dfb6-106">Suggestion</span></span>

`Link '{URL}' contains locale code '{code}'. For localizability, remove '{code}' from links to most Microsoft sites.`

<span data-ttu-id="3dfb6-107">区域设置代码（例如 `en-us`）不应包含在指向某些 Microsoft 站点的链接中。</span><span class="sxs-lookup"><span data-stu-id="3dfb6-107">Locale codes, such as `en-us`, should not be included in links to certain Microsoft sites.</span></span> <span data-ttu-id="3dfb6-108">如果在英语内容的链接中包含区域设置代码，它也将包含在本地化链接中，这会导致糟糕的本地化体验。</span><span class="sxs-lookup"><span data-stu-id="3dfb6-108">If you include a locale code in a link in English content, it will also be included in localized links, which leads to a bad localized experience.</span></span> <span data-ttu-id="3dfb6-109">例如，如果德语本地化内容中的链接包含 `en-us`，则德语客户会发现即使有德语版本，自己也被链接到了英文文章。</span><span class="sxs-lookup"><span data-stu-id="3dfb6-109">For example, if a link in German localized content includes `en-us`, German customers will find themselves linking to the English article, even if a German version is available.</span></span>

<span data-ttu-id="3dfb6-110">以下站点适用于此验证：</span><span class="sxs-lookup"><span data-stu-id="3dfb6-110">The following sites are in scope for this validation:</span></span>

- <span data-ttu-id="3dfb6-111">azure.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="3dfb6-111">azure.microsoft.com</span></span>
- <span data-ttu-id="3dfb6-112">docs.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="3dfb6-112">docs.microsoft.com</span></span>
- <span data-ttu-id="3dfb6-113">msdn.microsoft.com（不包括 social.msdn.com，它需要区域设置来确保链接到正确的论坛）</span><span class="sxs-lookup"><span data-stu-id="3dfb6-113">msdn.microsoft.com (excluding social.msdn.com, which needs locale to ensure the correct forum is linked to)</span></span>
- <span data-ttu-id="3dfb6-114">technet.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="3dfb6-114">technet.microsoft.com</span></span>

## <a name="resolution"></a><span data-ttu-id="3dfb6-115">解决方法</span><span class="sxs-lookup"><span data-stu-id="3dfb6-115">Resolution</span></span>

<span data-ttu-id="3dfb6-116">从 Microsoft 站点的链接中删除区域设置代码。</span><span class="sxs-lookup"><span data-stu-id="3dfb6-116">Remove locale codes from links to Microsoft sites.</span></span> <span data-ttu-id="3dfb6-117">下面是一个示例。</span><span class="sxs-lookup"><span data-stu-id="3dfb6-117">The following is an example.</span></span>

<span data-ttu-id="3dfb6-118">之前：</span><span class="sxs-lookup"><span data-stu-id="3dfb6-118">Before:</span></span>

`https://docs.microsoft.com/en-us/vsts/load-test/app-service-web-app-performance-test`

<span data-ttu-id="3dfb6-119">之后：</span><span class="sxs-lookup"><span data-stu-id="3dfb6-119">After:</span></span>

`https://docs.microsoft.com/vsts/load-test/app-service-web-app-performance-test`

> [!TIP]
> <span data-ttu-id="3dfb6-120">适用于 VS Code 的 Docs Markdown 扩展包括 Microsoft 链接的清理脚本。</span><span class="sxs-lookup"><span data-stu-id="3dfb6-120">The Docs Markdown extension for VS Code includes a cleanup script for Microsoft links.</span></span> <span data-ttu-id="3dfb6-121">脚本会检查存储库中所有指向 Microsoft 网站的链接，确保它们以 `https` 而非 `http` 开头，并且不包含区域设置代码，如 `en-us`。</span><span class="sxs-lookup"><span data-stu-id="3dfb6-121">The script checks all links to Microsoft sites in a repo to ensure that they begin with `https` instead of `http` and don't contain locale codes, such as `en-us`.</span></span> <span data-ttu-id="3dfb6-122">要运行脚本，请执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="3dfb6-122">To run the script:</span></span>
>
> 1. <span data-ttu-id="3dfb6-123">安装适用于 VS Code 的 [Docs Markdown](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown) 扩展。</span><span class="sxs-lookup"><span data-stu-id="3dfb6-123">Install the [Docs Markdown](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown) extension for VS Code.</span></span>
> 1. <span data-ttu-id="3dfb6-124">单击 Alt+M，打开“Markdown”菜单。</span><span class="sxs-lookup"><span data-stu-id="3dfb6-124">Click alt + M to open the Markdown menu.</span></span>
> 1. <span data-ttu-id="3dfb6-125">选择“清理”，然后选择“Microsoft 链接”   。</span><span class="sxs-lookup"><span data-stu-id="3dfb6-125">Select **Cleanup**, then **Microsoft links**.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
