---
title: ms-author-missing
description: 有关 Docs 生成问题 ms-author-missing 的解释和解决方案
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/20/2018
ms.prod: non-product-specific
ms.openlocfilehash: 6b313bd6b168b913d82721607126fcd4e6255009
ms.sourcegitcommit: 57eb071bdc55ef71fa3f8ac979326c3f8fbe9c45
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/10/2019
ms.locfileid: "72246251"
---
# <a name="ms-author-missing"></a><span data-ttu-id="35f6d-103">ms-author-missing</span><span class="sxs-lookup"><span data-stu-id="35f6d-103">ms-author-missing</span></span>

## <a name="warning"></a><span data-ttu-id="35f6d-104">警告</span><span class="sxs-lookup"><span data-stu-id="35f6d-104">Warning</span></span>

`Missing attribute: ms.author. Add the current author's Microsoft alias.`

## <a name="resolution"></a><span data-ttu-id="35f6d-105">解决方法</span><span class="sxs-lookup"><span data-stu-id="35f6d-105">Resolution</span></span>

<span data-ttu-id="35f6d-106">对于 `ms.author`，添加当前作者的 Microsoft 别名。</span><span class="sxs-lookup"><span data-stu-id="35f6d-106">Add the current author's Microsoft alias for `ms.author`.</span></span> <span data-ttu-id="35f6d-107">注意，如果所有权发生变更，则应该是此文章的当前作者，而不是原作者  。</span><span class="sxs-lookup"><span data-stu-id="35f6d-107">Note that this should be the *current* owner of the article, not the original author if ownership has changed.</span></span> <span data-ttu-id="35f6d-108">建议指定的作者为全职员工或团队通讯组列表 (DL)，而不是短期供应商。</span><span class="sxs-lookup"><span data-stu-id="35f6d-108">We recommend that the designated author be a full-time employee or team distribution list (DL), rather than a short-term vendor.</span></span> 

<span data-ttu-id="35f6d-109">如果别名是 DL，还必须位于 `ms.author` 允许列表中。</span><span class="sxs-lookup"><span data-stu-id="35f6d-109">If the alias is a DL, it must also be on the `ms.author` allow list.</span></span>

<span data-ttu-id="35f6d-110">可以在 [Microsoft 内部网站](https://docsmetadatatool.azurewebsites.net/allowlists)上找到 `ms.author` DL 的有效值。</span><span class="sxs-lookup"><span data-stu-id="35f6d-110">Valid values for `ms.author` DLs can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
