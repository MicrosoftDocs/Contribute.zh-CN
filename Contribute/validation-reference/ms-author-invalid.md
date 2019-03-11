---
title: ms-author-invalid
description: 有关 Docs 生成问题 ms-author-invalid 的解释和解决方法
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/28/2019
ms.prod: non-product-specific
ms.openlocfilehash: 210ff6a18bd12585c81f461a87238aa8d20c0530
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/05/2019
ms.locfileid: "57427229"
---
# <a name="ms-author-invalid"></a><span data-ttu-id="bf938-103">ms-author-invalid</span><span class="sxs-lookup"><span data-stu-id="bf938-103">ms-author-invalid</span></span>

<span data-ttu-id="bf938-104">**即将推出！**</span><span class="sxs-lookup"><span data-stu-id="bf938-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="bf938-105">建议</span><span class="sxs-lookup"><span data-stu-id="bf938-105">Suggestion</span></span>

`Invalid value for ms.author: '{value}' is not a valid Microsoft alias, or is not a whitelisted distribution list.`

## <a name="resolution"></a><span data-ttu-id="bf938-106">解决方法</span><span class="sxs-lookup"><span data-stu-id="bf938-106">Resolution</span></span>

<span data-ttu-id="bf938-107">验证 `ms.author` 值是有效的 Microsoft 别名。</span><span class="sxs-lookup"><span data-stu-id="bf938-107">Verify that the `ms.author` value is a valid Microsoft alias.</span></span> <span data-ttu-id="bf938-108">如果别名是通讯组列表，它还必须已列入允许列表。</span><span class="sxs-lookup"><span data-stu-id="bf938-108">If the alias is a distribution list, it must also be whitelisted.</span></span>

<span data-ttu-id="bf938-109">可以在[此 Microsoft 内部网站](https://docsmetadatatool.azurewebsites.net/whitelists)上找到有效值。</span><span class="sxs-lookup"><span data-stu-id="bf938-109">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/whitelists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
