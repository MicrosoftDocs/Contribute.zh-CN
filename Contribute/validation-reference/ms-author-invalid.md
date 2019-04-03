---
title: ms-author-invalid
description: 有关 Docs 生成问题 ms-author-invalid 的解释和解决方法
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/28/2019
ms.prod: non-product-specific
ms.openlocfilehash: 6d6c77b9b378865913e2055abf2b64ccba8ca482
ms.sourcegitcommit: 8e897e90268a8a87dc4b97d7c28d22ed5950c8d9
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/29/2019
ms.locfileid: "58636715"
---
# <a name="ms-author-invalid"></a><span data-ttu-id="bef81-103">ms-author-invalid</span><span class="sxs-lookup"><span data-stu-id="bef81-103">ms-author-invalid</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="bef81-104">建议</span><span class="sxs-lookup"><span data-stu-id="bef81-104">Suggestion</span></span>

`Invalid value for ms.author: '{value}' is not a valid Microsoft alias, or is not an allowed distribution list.`

## <a name="resolution"></a><span data-ttu-id="bef81-105">解决方法</span><span class="sxs-lookup"><span data-stu-id="bef81-105">Resolution</span></span>

<span data-ttu-id="bef81-106">验证 `ms.author` 值是有效的 Microsoft 别名。</span><span class="sxs-lookup"><span data-stu-id="bef81-106">Verify that the `ms.author` value is a valid Microsoft alias.</span></span> <span data-ttu-id="bef81-107">如果别名是通讯组列表，还必须位于允许列表中。</span><span class="sxs-lookup"><span data-stu-id="bef81-107">If the alias is a distribution list, it must also be on the allow list.</span></span>

<span data-ttu-id="bef81-108">可以在[此 Microsoft 内部网站](https://docsmetadatatool.azurewebsites.net/allowlists)上找到 DL 的有效值。</span><span class="sxs-lookup"><span data-stu-id="bef81-108">Valid values for DLs can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
