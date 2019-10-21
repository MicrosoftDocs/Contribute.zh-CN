---
title: hard-coded-locale
description: 有关 Docs 生成问题 hard-coded-locale 的解释和解决方法。
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: eb9ae17673b3da5f921139d88cc9af469423c9c3
ms.sourcegitcommit: d357977935b432381f3df6297164417ed59ab434
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/14/2019
ms.locfileid: "72310334"
---
# <a name="hard-coded-locale"></a><span data-ttu-id="aafd9-103">hard-coded-locale</span><span class="sxs-lookup"><span data-stu-id="aafd9-103">hard-coded-locale</span></span>

## <a name="warning"></a><span data-ttu-id="aafd9-104">警告</span><span class="sxs-lookup"><span data-stu-id="aafd9-104">Warning</span></span>

`Link '{URL}' contains locale code '{code}'. For localizability, remove '{code}' from links to Microsoft sites.`

<span data-ttu-id="aafd9-105">区域设置代码（例如 `en-us`）不应包含在指向某些 Microsoft 站点的链接中。</span><span class="sxs-lookup"><span data-stu-id="aafd9-105">Locale codes, such as `en-us`, should not be included in links to certain Microsoft sites.</span></span> <span data-ttu-id="aafd9-106">如果在英语内容的链接中包含区域设置代码，它也将包含在本地化链接中，这会导致糟糕的本地化体验。</span><span class="sxs-lookup"><span data-stu-id="aafd9-106">If you include a locale code in a link in English content, it will also be included in localized links, which leads to a bad localized experience.</span></span> <span data-ttu-id="aafd9-107">例如，如果德语本地化内容中的链接包含 `en-us`，则德语客户会发现即使有德语版本，自己也被链接到了英文文章。</span><span class="sxs-lookup"><span data-stu-id="aafd9-107">For example, if a link in German localized content includes `en-us`, German customers will find themselves linking to the English article, even if a German version is available.</span></span>

<span data-ttu-id="aafd9-108">以下站点适用于此验证：</span><span class="sxs-lookup"><span data-stu-id="aafd9-108">The following sites are in scope for this validation:</span></span>

- <span data-ttu-id="aafd9-109">azure.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="aafd9-109">azure.microsoft.com</span></span>
- <span data-ttu-id="aafd9-110">docs.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="aafd9-110">docs.microsoft.com</span></span>
- <span data-ttu-id="aafd9-111">msdn.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="aafd9-111">msdn.microsoft.com</span></span>
- <span data-ttu-id="aafd9-112">technet.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="aafd9-112">technet.microsoft.com</span></span>

## <a name="resolution"></a><span data-ttu-id="aafd9-113">解决方法</span><span class="sxs-lookup"><span data-stu-id="aafd9-113">Resolution</span></span>

<span data-ttu-id="aafd9-114">从 Microsoft 站点的链接中删除区域设置代码。</span><span class="sxs-lookup"><span data-stu-id="aafd9-114">Remove locale codes from links to Microsoft sites.</span></span> <span data-ttu-id="aafd9-115">下面是一个示例。</span><span class="sxs-lookup"><span data-stu-id="aafd9-115">The following is an example.</span></span>

<span data-ttu-id="aafd9-116">之前：</span><span class="sxs-lookup"><span data-stu-id="aafd9-116">Before:</span></span>

`https://docs.microsoft.com/en-us/vsts/load-test/app-service-web-app-performance-test`

<span data-ttu-id="aafd9-117">之后：</span><span class="sxs-lookup"><span data-stu-id="aafd9-117">After:</span></span>

`https://docs.microsoft.com/vsts/load-test/app-service-web-app-performance-test`

> [!TIP]
> <span data-ttu-id="aafd9-118">适用于 VS Code 的 Docs Markdown 扩展包括 Microsoft 链接的清理脚本。</span><span class="sxs-lookup"><span data-stu-id="aafd9-118">The Docs Markdown extension for VS Code includes a cleanup script for Microsoft links.</span></span> <span data-ttu-id="aafd9-119">脚本会检查存储库中所有指向 Microsoft 网站的链接，确保它们以 `https` 而非 `http` 开头，并且不包含区域设置代码，如 `en-us`。</span><span class="sxs-lookup"><span data-stu-id="aafd9-119">The script checks all links to Microsoft sites in a repo to ensure that they begin with `https` instead of `http` and don't contain locale codes, such as `en-us`.</span></span> <span data-ttu-id="aafd9-120">要运行脚本，请执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="aafd9-120">To run the script:</span></span>
>
> 1. <span data-ttu-id="aafd9-121">安装适用于 VS Code 的 [Docs Markdown](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown) 扩展。</span><span class="sxs-lookup"><span data-stu-id="aafd9-121">Install the [Docs Markdown](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown) extension for VS Code.</span></span>
> 1. <span data-ttu-id="aafd9-122">单击 Alt+M，打开“Markdown”菜单。</span><span class="sxs-lookup"><span data-stu-id="aafd9-122">Click alt + M to open the Markdown menu.</span></span>
> 1. <span data-ttu-id="aafd9-123">选择“清理”，然后选择“Microsoft 链接”   。</span><span class="sxs-lookup"><span data-stu-id="aafd9-123">Select **Cleanup**, then **Microsoft links**.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]