---
title: insecure-link
description: 有关 Docs 生成问题 insecure-link 的解释和解决方法
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 10/1/2019
ms.prod: non-product-specific
ms.openlocfilehash: b97d4c4a0f61e5f3448331a56fe4bde442ff1cca
ms.sourcegitcommit: 0cb0177c209abab1a72af4f411ef527fa5cf10f9
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/16/2019
ms.locfileid: "72379508"
---
# <a name="insecure-link"></a><span data-ttu-id="a7189-103">insecure-link</span><span class="sxs-lookup"><span data-stu-id="a7189-103">insecure-link</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="a7189-104">建议</span><span class="sxs-lookup"><span data-stu-id="a7189-104">Suggestion</span></span>

`Link '{URL}' is insecure. Links to Microsoft sites must use 'https' instead of 'http'.`

<span data-ttu-id="a7189-105">此消息表示你使用的是具有 `http` 的显式 Markdown 链接，或者使用原始 URL，如 `www.microsoft.com`。</span><span class="sxs-lookup"><span data-stu-id="a7189-105">This message means that you either used an explicit Markdown link with `http` or you used a raw URL, such as `www.microsoft.com`.</span></span> <span data-ttu-id="a7189-106">原始 URL 在发布到 Docs 时会转换为不安全的链接，因此不应使用。</span><span class="sxs-lookup"><span data-stu-id="a7189-106">Raw URLs are converted to insecure links when published to Docs, and should not be used.</span></span>

## <a name="resolution"></a><span data-ttu-id="a7189-107">解决方法</span><span class="sxs-lookup"><span data-stu-id="a7189-107">Resolution</span></span>

<span data-ttu-id="a7189-108">应将所有 URL 更改为使用 `https` 而非 `http` 的 Microsoft 网站。</span><span class="sxs-lookup"><span data-stu-id="a7189-108">Change all URLs to Microsoft sites to use `https` instead of `http`.</span></span>

<span data-ttu-id="a7189-109">如果链接是原始 URL，请将其更改为以 `https` 开头的显式 Markdown 链接。</span><span class="sxs-lookup"><span data-stu-id="a7189-109">If your link is a raw URL, change it to an explicit Markdown link beginning with `https`.</span></span>

> [!TIP]
> <span data-ttu-id="a7189-110">适用于 VS Code 的 Docs Markdown 扩展包括 Microsoft 链接的清理脚本。</span><span class="sxs-lookup"><span data-stu-id="a7189-110">The Docs Markdown extension for VS Code includes a cleanup script for Microsoft links.</span></span> <span data-ttu-id="a7189-111">脚本会检查存储库中所有指向 Microsoft 网站的链接，确保它们以 `https` 而非 `http` 开头，并且不包含区域设置代码，如 `en-us`。</span><span class="sxs-lookup"><span data-stu-id="a7189-111">The script checks all links to Microsoft sites in a repo to ensure that they begin with `https` instead of `http` and don't contain locale codes, such as `en-us`.</span></span> <span data-ttu-id="a7189-112">要运行脚本，请执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="a7189-112">To run the script:</span></span>
>
> 1. <span data-ttu-id="a7189-113">安装适用于 VS Code 的 [Docs Markdown](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown) 扩展。</span><span class="sxs-lookup"><span data-stu-id="a7189-113">Install the [Docs Markdown](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown) extension for VS Code.</span></span>
> 1. <span data-ttu-id="a7189-114">单击 Alt+M，打开“Markdown”菜单。</span><span class="sxs-lookup"><span data-stu-id="a7189-114">Click alt + M to open the Markdown menu.</span></span>
> 1. <span data-ttu-id="a7189-115">选择“清理”，然后选择“Microsoft 链接”   。</span><span class="sxs-lookup"><span data-stu-id="a7189-115">Select **Cleanup**, then **Microsoft links**.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
