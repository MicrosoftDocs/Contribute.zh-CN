---
title: deprecated-attribute
description: 有关 Docs 生成问题 deprecated-attribute 的解释和解决办法
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/1/2019
ms.prod: non-product-specific
ms.openlocfilehash: 564bd35c418fb9def6bf20240fca64265a477f46
ms.sourcegitcommit: 42e5a6ae071826afc2a32a9b7150ca113b39afdf
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/19/2019
ms.locfileid: "57987781"
---
# <a name="deprecated-attribute"></a><span data-ttu-id="fcda4-103">deprecated-attribute</span><span class="sxs-lookup"><span data-stu-id="fcda4-103">deprecated-attribute</span></span>

<span data-ttu-id="fcda4-104">**即将推出！**</span><span class="sxs-lookup"><span data-stu-id="fcda4-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="fcda4-105">建议</span><span class="sxs-lookup"><span data-stu-id="fcda4-105">Suggestion</span></span>

`Deprecated attribute: ms.component. Use ms.subservice instead.`

<span data-ttu-id="fcda4-106">请使用 `ms.service` 指定云服务。</span><span class="sxs-lookup"><span data-stu-id="fcda4-106">Use `ms.service` to specify cloud services.</span></span> <span data-ttu-id="fcda4-107">若要指定有关 `ms.service` 更详细的信息，可以选择指定 `ms.subservice`。</span><span class="sxs-lookup"><span data-stu-id="fcda4-107">To specify more detailed information about `ms.service`, you can optionally specify `ms.subservice`.</span></span> <span data-ttu-id="fcda4-108">请勿使用 `ms.component`；它已针对此内容弃用。</span><span class="sxs-lookup"><span data-stu-id="fcda4-108">Don't use `ms.component`; it's deprecated for this content.</span></span>

## <a name="resolution"></a><span data-ttu-id="fcda4-109">解决方法</span><span class="sxs-lookup"><span data-stu-id="fcda4-109">Resolution</span></span>

<span data-ttu-id="fcda4-110">请确认文章的 `ms.service` 值正确无误。</span><span class="sxs-lookup"><span data-stu-id="fcda4-110">Confirm that your `ms.service` value is correct for your article.</span></span> <span data-ttu-id="fcda4-111">然后选择有效的 `ms.subservice` 值。</span><span class="sxs-lookup"><span data-stu-id="fcda4-111">Then choose a valid `ms.subservice` value.</span></span>

<span data-ttu-id="fcda4-112">可以在[此 Microsoft 内部网站](https://docsmetadatatool.azurewebsites.net/allowlists)上找到有效值。</span><span class="sxs-lookup"><span data-stu-id="fcda4-112">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
