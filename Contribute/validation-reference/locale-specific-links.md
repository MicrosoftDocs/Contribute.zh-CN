---
author: meganbradley
ms.author: mbradley
ms.date: 03/29/2019
ms.openlocfilehash: a3b383021046412620c616882b19cb06f4dc59f8
ms.sourcegitcommit: af37d44eb67daa2841959817cd205ec95db18cec
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/29/2019
ms.locfileid: "58653542"
---
# <a name="locale-specific-links"></a><span data-ttu-id="72844-101">特定于区域设置的链接</span><span class="sxs-lookup"><span data-stu-id="72844-101">Locale-specific links</span></span>

<span data-ttu-id="72844-102">区域设置代码（例如 `en-us`）不应包含在指向某些 Microsoft 站点的链接中。</span><span class="sxs-lookup"><span data-stu-id="72844-102">Locale codes, such as `en-us`, should not be included in links to certain Microsoft sites.</span></span> <span data-ttu-id="72844-103">如果在英语内容的链接中包含区域设置代码，它也将包含在本地化链接中，这会导致糟糕的本地化体验。</span><span class="sxs-lookup"><span data-stu-id="72844-103">If you include a locale code in a link in English content, it will also be included in localized links, which leads to a bad localized experience.</span></span> <span data-ttu-id="72844-104">例如，如果德语本地化内容中的链接包含 `en-us`，则德语客户会发现即使有德语版本，自己也被链接到了英文文章。</span><span class="sxs-lookup"><span data-stu-id="72844-104">For example, if a link in German localized content includes `en-us`, German customers will find themselves linking to the English article, even if a German version is available.</span></span>

<span data-ttu-id="72844-105">从 Microsoft 站点的链接中删除区域设置代码。</span><span class="sxs-lookup"><span data-stu-id="72844-105">Remove locale codes from links to Microsoft sites.</span></span> <span data-ttu-id="72844-106">下面是一个示例。</span><span class="sxs-lookup"><span data-stu-id="72844-106">The following is an example.</span></span>

<span data-ttu-id="72844-107">之前：</span><span class="sxs-lookup"><span data-stu-id="72844-107">Before:</span></span>

`https://docs.microsoft.com/en-us/vsts/load-test/app-service-web-app-performance-test`

<span data-ttu-id="72844-108">之后：</span><span class="sxs-lookup"><span data-stu-id="72844-108">After:</span></span>

`https://docs.microsoft.com/vsts/load-test/app-service-web-app-performance-test`

<span data-ttu-id="72844-109">以下站点适用于此验证：</span><span class="sxs-lookup"><span data-stu-id="72844-109">The following sites are in scope for this validation:</span></span>

- <span data-ttu-id="72844-110">azure.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="72844-110">azure.microsoft.com</span></span>
- <span data-ttu-id="72844-111">docs.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="72844-111">docs.microsoft.com</span></span>
- <span data-ttu-id="72844-112">msdn.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="72844-112">msdn.microsoft.com</span></span>
- <span data-ttu-id="72844-113">technet.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="72844-113">technet.microsoft.com</span></span>