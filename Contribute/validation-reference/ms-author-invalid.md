---
title: ms-author-invalid
description: 有关 Docs 生成问题 ms-author-invalid 的解释和解决方法
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 9/27/2019
ms.prod: non-product-specific
ms.openlocfilehash: b3100b4a304356aee3c50f805628890b8c738fe1
ms.sourcegitcommit: d2f5b68b6a6d1ac902dba5063482ff5955a5b1f7
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/28/2019
ms.locfileid: "71481699"
---
# <a name="ms-author-invalid"></a><span data-ttu-id="d57eb-103">ms-author-invalid</span><span class="sxs-lookup"><span data-stu-id="d57eb-103">ms-author-invalid</span></span>

## <a name="warning"></a><span data-ttu-id="d57eb-104">警告</span><span class="sxs-lookup"><span data-stu-id="d57eb-104">Warning</span></span>

`Invalid value for ms.author: '{value}' is not a valid Microsoft alias, or is not an allowed distribution list.`

## <a name="resolution"></a><span data-ttu-id="d57eb-105">解决方法</span><span class="sxs-lookup"><span data-stu-id="d57eb-105">Resolution</span></span>

<span data-ttu-id="d57eb-106">验证 `ms.author` 值是当前作者的 Microsoft 有效别名。</span><span class="sxs-lookup"><span data-stu-id="d57eb-106">Verify that the `ms.author` value is the current author's valid Microsoft alias.</span></span> <span data-ttu-id="d57eb-107">建议指定的作者为全职员工或团队通讯组列表 (DL)，而不是短期供应商。</span><span class="sxs-lookup"><span data-stu-id="d57eb-107">We recommend that the designated author be a full-time employee or team distrubution list (DL), rather than a short-term vendor.</span></span> <span data-ttu-id="d57eb-108">如果别名是 DL，还必须位于 `ms.author` 允许列表中。</span><span class="sxs-lookup"><span data-stu-id="d57eb-108">If the alias is a DL, it must also be on the `ms.author` allow list.</span></span>

<span data-ttu-id="d57eb-109">可以在 [Microsoft 内部网站](https://docsmetadatatool.azurewebsites.net/allowlists)上找到 `ms.author` DL 的有效值。</span><span class="sxs-lookup"><span data-stu-id="d57eb-109">Valid values for `ms.author` DLs can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
