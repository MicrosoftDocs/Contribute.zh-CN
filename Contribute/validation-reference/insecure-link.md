---
title: insecure-link
description: 有关 Docs 生成问题 insecure-link 的解释和解决方法
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 10/1/2019
ms.prod: non-product-specific
ms.openlocfilehash: 4735d47cdf2029d2c613c9b333a393c7d978c58e
ms.sourcegitcommit: 423d9b8145a11426c91f45510b2d77319838eb27
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2019
ms.locfileid: "74528850"
---
# <a name="insecure-link"></a><span data-ttu-id="ad00b-103">insecure-link</span><span class="sxs-lookup"><span data-stu-id="ad00b-103">insecure-link</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ad00b-104">此规则最初作为“建议”启用，以便内容团队有时间衡量影响并制定清理其存储库的计划。</span><span class="sxs-lookup"><span data-stu-id="ad00b-104">This rule was initially enabled as a "Suggestion" to give content teams time to gauge impact and develop a plan to clean up their repos.</span></span> <span data-ttu-id="ad00b-105">**它将于 2019 年 12 月 20 日提升为“警告”** 。</span><span class="sxs-lookup"><span data-stu-id="ad00b-105">**It will be elevated to a "Warning" on 12/20/2019**.</span></span>

## <a name="suggestion"></a><span data-ttu-id="ad00b-106">建议</span><span class="sxs-lookup"><span data-stu-id="ad00b-106">Suggestion</span></span>

`Link '{URL}' is insecure. Links to Microsoft sites must use 'https' instead of 'http'.`

<span data-ttu-id="ad00b-107">此消息表示你使用的是具有 `http` 的显式 Markdown 链接，或者使用原始 URL，如 `www.microsoft.com`。</span><span class="sxs-lookup"><span data-stu-id="ad00b-107">This message means that you either used an explicit Markdown link with `http` or you used a raw URL, such as `www.microsoft.com`.</span></span> <span data-ttu-id="ad00b-108">原始 URL 在发布到 Docs 时会转换为不安全的链接，因此不应使用。</span><span class="sxs-lookup"><span data-stu-id="ad00b-108">Raw URLs are converted to insecure links when published to Docs, and should not be used.</span></span>

## <a name="resolution"></a><span data-ttu-id="ad00b-109">解决方法</span><span class="sxs-lookup"><span data-stu-id="ad00b-109">Resolution</span></span>

<span data-ttu-id="ad00b-110">应将所有 URL 更改为使用 `https` 而非 `http` 的 Microsoft 网站。</span><span class="sxs-lookup"><span data-stu-id="ad00b-110">Change all URLs to Microsoft sites to use `https` instead of `http`.</span></span>

<span data-ttu-id="ad00b-111">如果链接是原始 URL，请将其更改为以 `https` 开头的显式 Markdown 链接，例如：</span><span class="sxs-lookup"><span data-stu-id="ad00b-111">If your link is a raw URL, change it to an explicit Markdown link beginning with `https`, such as:</span></span>

```md
`[www.microsoft.com](https://www.microsoft.com)`.
```

> [!TIP]
> <span data-ttu-id="ad00b-112">适用于 VS Code 的 Docs Markdown 扩展包括 Microsoft 链接的清理脚本。</span><span class="sxs-lookup"><span data-stu-id="ad00b-112">The Docs Markdown extension for VS Code includes a cleanup script for Microsoft links.</span></span> <span data-ttu-id="ad00b-113">脚本会检查存储库中所有指向 Microsoft 网站的链接，确保它们以 `https` 而非 `http` 开头，并且不包含区域设置代码，如 `en-us`。</span><span class="sxs-lookup"><span data-stu-id="ad00b-113">The script checks all links to Microsoft sites in a repo to ensure that they begin with `https` instead of `http` and don't contain locale codes, such as `en-us`.</span></span> <span data-ttu-id="ad00b-114">要运行脚本，请执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="ad00b-114">To run the script:</span></span>
>
> 1. <span data-ttu-id="ad00b-115">安装适用于 VS Code 的 [Docs Markdown](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown) 扩展。</span><span class="sxs-lookup"><span data-stu-id="ad00b-115">Install the [Docs Markdown](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown) extension for VS Code.</span></span>
> 1. <span data-ttu-id="ad00b-116">单击 Alt+M，打开“Markdown”菜单。</span><span class="sxs-lookup"><span data-stu-id="ad00b-116">Click alt + M to open the Markdown menu.</span></span>
> 1. <span data-ttu-id="ad00b-117">选择“清理”，然后选择“Microsoft 链接”   。</span><span class="sxs-lookup"><span data-stu-id="ad00b-117">Select **Cleanup**, then **Microsoft links**.</span></span>

<span data-ttu-id="ad00b-118">在某些情况下，可能需要记录不是可单击链接的 web 地址，如完全限定的域名。</span><span class="sxs-lookup"><span data-stu-id="ad00b-118">In some cases, you might need to document web addresses, such as fully-qualified domain names, that aren't meant to be clickable links.</span></span> <span data-ttu-id="ad00b-119">应以内联代码的形式为其设置样式，例如：</span><span class="sxs-lookup"><span data-stu-id="ad00b-119">These should be styled as inline code, such as:</span></span>

```md
`www.microsoft.com:90`
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
