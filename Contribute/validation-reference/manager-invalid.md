---
title: manager-invalid
description: 有关 Docs 生成问题 manager-invalid 的解释和解决方法
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 3/1/2019
ms.prod: non-product-specific
ms.openlocfilehash: 44174bde29b63bffe709596f9c2d6be994f252a3
ms.sourcegitcommit: 8e897e90268a8a87dc4b97d7c28d22ed5950c8d9
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/29/2019
ms.locfileid: "58637221"
---
# <a name="manager-invalid"></a><span data-ttu-id="2221d-103">manager-invalid</span><span class="sxs-lookup"><span data-stu-id="2221d-103">manager-invalid</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="2221d-104">建议</span><span class="sxs-lookup"><span data-stu-id="2221d-104">Suggestion</span></span>

`Invalid value for manager: '{value}' is not a valid Microsoft alias.`

<span data-ttu-id="2221d-105">一些内容组需要 `manager` 属性来标识创建者的管理员。</span><span class="sxs-lookup"><span data-stu-id="2221d-105">Some content groups require the `manager` attribute to identify the author's manager.</span></span>

## <a name="resolution"></a><span data-ttu-id="2221d-106">解决方法</span><span class="sxs-lookup"><span data-stu-id="2221d-106">Resolution</span></span>

<span data-ttu-id="2221d-107">`manager` 的值必须是各 Microsoft 员工有效别名。</span><span class="sxs-lookup"><span data-stu-id="2221d-107">The value of `manager` must be a valid alias for an individual Microsoft employee.</span></span> <span data-ttu-id="2221d-108">验证创建者的管理员别名并更新值。</span><span class="sxs-lookup"><span data-stu-id="2221d-108">Verify the author's manager's alias and update the value.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
