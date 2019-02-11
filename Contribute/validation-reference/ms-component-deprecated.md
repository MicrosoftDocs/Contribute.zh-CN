---
title: ms-component-deprecated
description: 有关 Docs 生成问题 ms-component-deprecated 的解释和解决方案
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/1/2019
ms.prod: non-product-specific
ms.openlocfilehash: 4f89571e2d4c50439806fb26b9967a4b7588f4a9
ms.sourcegitcommit: 203ca15fda2d217f082c74ec648c1f1db323f9f1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/04/2019
ms.locfileid: "55713145"
---
# <a name="ms-component-deprecated"></a><span data-ttu-id="4af0b-103">ms-component-deprecated</span><span class="sxs-lookup"><span data-stu-id="4af0b-103">ms-component-deprecated</span></span>

<span data-ttu-id="4af0b-104">**即将推出！**</span><span class="sxs-lookup"><span data-stu-id="4af0b-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="4af0b-105">建议</span><span class="sxs-lookup"><span data-stu-id="4af0b-105">Suggestion</span></span>

`Deprecated attribute: ms.component. Use ms.subservice instead.`

<span data-ttu-id="4af0b-106">请使用 `ms.service` 指定云服务。</span><span class="sxs-lookup"><span data-stu-id="4af0b-106">Use `ms.service` to specify cloud services.</span></span> <span data-ttu-id="4af0b-107">若要指定有关 `ms.service` 更详细的信息，可以选择指定 `ms.subservice`。</span><span class="sxs-lookup"><span data-stu-id="4af0b-107">To specify more detailed information about `ms.service`, you can optionally specify `ms.subservice`.</span></span> <span data-ttu-id="4af0b-108">请勿使用 `ms.component`；它已针对此内容弃用。</span><span class="sxs-lookup"><span data-stu-id="4af0b-108">Don't use `ms.component`; it's deprecated for this content.</span></span>

## <a name="resolution"></a><span data-ttu-id="4af0b-109">解决方法</span><span class="sxs-lookup"><span data-stu-id="4af0b-109">Resolution</span></span>

<span data-ttu-id="4af0b-110">请确认文章的 `ms.service` 值正确无误。</span><span class="sxs-lookup"><span data-stu-id="4af0b-110">Confirm that your `ms.service` value is correct for your article.</span></span> <span data-ttu-id="4af0b-111">然后选择有效的 `ms.subservice` 值。</span><span class="sxs-lookup"><span data-stu-id="4af0b-111">Then choose a valid `ms.subservice` value.</span></span>

<span data-ttu-id="4af0b-112">可以在[此 Microsoft 内部网站](https://docsmetadatatool.azurewebsites.net/whitelists)上找到有效值。</span><span class="sxs-lookup"><span data-stu-id="4af0b-112">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/whitelists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
