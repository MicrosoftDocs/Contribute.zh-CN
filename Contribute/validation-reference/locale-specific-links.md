---
author: meganbradley
ms.author: mbradley
ms.date: 03/29/2019
title: 特定于区域设置的链接
ms.openlocfilehash: f42a26da45b48972bfc595cb26c67ab0acfe8603
ms.sourcegitcommit: 1e53d17639277bebd89b2e7cabeb45bdad526354
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/12/2019
ms.locfileid: "66841250"
---
# <a name="locale-specific-links"></a><span data-ttu-id="39831-102">特定于区域设置的链接</span><span class="sxs-lookup"><span data-stu-id="39831-102">Locale-specific links</span></span>

<span data-ttu-id="39831-103">区域设置代码（例如 `en-us`）不应包含在指向某些 Microsoft 站点的链接中。</span><span class="sxs-lookup"><span data-stu-id="39831-103">Locale codes, such as `en-us`, should not be included in links to certain Microsoft sites.</span></span> <span data-ttu-id="39831-104">如果在英语内容的链接中包含区域设置代码，它也将包含在本地化链接中，这会导致糟糕的本地化体验。</span><span class="sxs-lookup"><span data-stu-id="39831-104">If you include a locale code in a link in English content, it will also be included in localized links, which leads to a bad localized experience.</span></span> <span data-ttu-id="39831-105">例如，如果德语本地化内容中的链接包含 `en-us`，则德语客户会发现即使有德语版本，自己也被链接到了英文文章。</span><span class="sxs-lookup"><span data-stu-id="39831-105">For example, if a link in German localized content includes `en-us`, German customers will find themselves linking to the English article, even if a German version is available.</span></span>

<span data-ttu-id="39831-106">从 Microsoft 站点的链接中删除区域设置代码。</span><span class="sxs-lookup"><span data-stu-id="39831-106">Remove locale codes from links to Microsoft sites.</span></span> <span data-ttu-id="39831-107">下面是一个示例。</span><span class="sxs-lookup"><span data-stu-id="39831-107">The following is an example.</span></span>

<span data-ttu-id="39831-108">之前：</span><span class="sxs-lookup"><span data-stu-id="39831-108">Before:</span></span>

`https://docs.microsoft.com/en-us/vsts/load-test/app-service-web-app-performance-test`

<span data-ttu-id="39831-109">之后：</span><span class="sxs-lookup"><span data-stu-id="39831-109">After:</span></span>

`https://docs.microsoft.com/vsts/load-test/app-service-web-app-performance-test`

<span data-ttu-id="39831-110">以下站点适用于此验证：</span><span class="sxs-lookup"><span data-stu-id="39831-110">The following sites are in scope for this validation:</span></span>

- <span data-ttu-id="39831-111">azure.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="39831-111">azure.microsoft.com</span></span>
- <span data-ttu-id="39831-112">docs.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="39831-112">docs.microsoft.com</span></span>
- <span data-ttu-id="39831-113">msdn.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="39831-113">msdn.microsoft.com</span></span>
- <span data-ttu-id="39831-114">technet.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="39831-114">technet.microsoft.com</span></span>