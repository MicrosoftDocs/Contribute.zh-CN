---
title: manager-missing
description: 有关 Docs 生成问题 issue manager-missing 的解释和解决方法
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 3/1/2019
ms.prod: non-product-specific
ms.openlocfilehash: af23f2cab1fd948b4192bc0b598543ad15013ae0
ms.sourcegitcommit: 8e897e90268a8a87dc4b97d7c28d22ed5950c8d9
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/29/2019
ms.locfileid: "58637244"
---
# <a name="manager-missing"></a><span data-ttu-id="9019d-103">manager-missing</span><span class="sxs-lookup"><span data-stu-id="9019d-103">manager-missing</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="9019d-104">建议</span><span class="sxs-lookup"><span data-stu-id="9019d-104">Suggestion</span></span>

`Missing attribute: manager. Add a valid Microsoft alias for the author's manager.`

<span data-ttu-id="9019d-105">一些内容组需要 `manager` 属性来标识创建者的管理员。</span><span class="sxs-lookup"><span data-stu-id="9019d-105">Some content groups require the `manager` attribute to identify the author's manager.</span></span>

## <a name="resolution"></a><span data-ttu-id="9019d-106">解决方法</span><span class="sxs-lookup"><span data-stu-id="9019d-106">Resolution</span></span>

<span data-ttu-id="9019d-107">请为 `manager` 添加有效的 Microsoft 别名：</span><span class="sxs-lookup"><span data-stu-id="9019d-107">Add a valid Microsoft alias for `manager`:</span></span>

```yml
---
ms.author: mbradley
manager: jemash
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
