---
title: manager-invalid
description: 有关 Docs 生成问题 manager-invalid 的解释和解决方法
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 3/1/2019
ms.prod: non-product-specific
ms.openlocfilehash: 7eac188b16b402767bbec551a6dec8b5877680af
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/05/2019
ms.locfileid: "57427170"
---
# <a name="manager-invalid"></a><span data-ttu-id="3091e-103">manager-invalid</span><span class="sxs-lookup"><span data-stu-id="3091e-103">manager-invalid</span></span>

<span data-ttu-id="3091e-104">**即将推出！**</span><span class="sxs-lookup"><span data-stu-id="3091e-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="3091e-105">建议</span><span class="sxs-lookup"><span data-stu-id="3091e-105">Suggestion</span></span>

`Invalid value for manager: '{value}' is not a valid Microsoft alias.`

<span data-ttu-id="3091e-106">一些内容组需要 `manager` 属性来标识创建者的管理员。</span><span class="sxs-lookup"><span data-stu-id="3091e-106">Some content groups require the `manager` attribute to identify the author's manager.</span></span>

## <a name="resolution"></a><span data-ttu-id="3091e-107">解决方法</span><span class="sxs-lookup"><span data-stu-id="3091e-107">Resolution</span></span>

<span data-ttu-id="3091e-108">`manager` 的值必须是各 Microsoft 员工有效别名。</span><span class="sxs-lookup"><span data-stu-id="3091e-108">The value of `manager` must be a valid alias for an individual Microsoft employee.</span></span> <span data-ttu-id="3091e-109">验证创建者的管理员别名并更新值。</span><span class="sxs-lookup"><span data-stu-id="3091e-109">Verify the author's manager's alias and update the value.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
