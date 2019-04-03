---
title: deprecated-attribute
description: 有关 Docs 生成问题 deprecated-attribute 的解释和解决办法
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/1/2019
ms.prod: non-product-specific
ms.openlocfilehash: 113ca759af1765a2a51cadc721fa59743b699475
ms.sourcegitcommit: 8e897e90268a8a87dc4b97d7c28d22ed5950c8d9
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/29/2019
ms.locfileid: "58636876"
---
# <a name="deprecated-attribute"></a><span data-ttu-id="d4d5e-103">deprecated-attribute</span><span class="sxs-lookup"><span data-stu-id="d4d5e-103">deprecated-attribute</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="d4d5e-104">建议</span><span class="sxs-lookup"><span data-stu-id="d4d5e-104">Suggestion</span></span>

`Deprecated attribute: ms.component. Use ms.subservice instead.`

<span data-ttu-id="d4d5e-105">请使用 `ms.service` 指定云服务。</span><span class="sxs-lookup"><span data-stu-id="d4d5e-105">Use `ms.service` to specify cloud services.</span></span> <span data-ttu-id="d4d5e-106">若要指定有关 `ms.service` 更详细的信息，可以选择指定 `ms.subservice`。</span><span class="sxs-lookup"><span data-stu-id="d4d5e-106">To specify more detailed information about `ms.service`, you can optionally specify `ms.subservice`.</span></span> <span data-ttu-id="d4d5e-107">请勿使用 `ms.component`；它已针对此内容弃用。</span><span class="sxs-lookup"><span data-stu-id="d4d5e-107">Don't use `ms.component`; it's deprecated for this content.</span></span>

## <a name="resolution"></a><span data-ttu-id="d4d5e-108">解决方法</span><span class="sxs-lookup"><span data-stu-id="d4d5e-108">Resolution</span></span>

<span data-ttu-id="d4d5e-109">请确认文章的 `ms.service` 值正确无误。</span><span class="sxs-lookup"><span data-stu-id="d4d5e-109">Confirm that your `ms.service` value is correct for your article.</span></span> <span data-ttu-id="d4d5e-110">然后选择有效的 `ms.subservice` 值。</span><span class="sxs-lookup"><span data-stu-id="d4d5e-110">Then choose a valid `ms.subservice` value.</span></span>

<span data-ttu-id="d4d5e-111">可以在[此 Microsoft 内部网站](https://docsmetadatatool.azurewebsites.net/allowlists)上找到有效值。</span><span class="sxs-lookup"><span data-stu-id="d4d5e-111">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
