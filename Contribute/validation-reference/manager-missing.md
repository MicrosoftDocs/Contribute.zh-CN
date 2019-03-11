---
title: manager-missing
description: 有关 Docs 生成问题 issue manager-missing 的解释和解决方法
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 3/1/2019
ms.prod: non-product-specific
ms.openlocfilehash: 16da241a21d400d5a5dfb101e247e55d95567485
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/05/2019
ms.locfileid: "57427224"
---
# <a name="manager-missing"></a><span data-ttu-id="a4355-103">manager-missing</span><span class="sxs-lookup"><span data-stu-id="a4355-103">manager-missing</span></span>

<span data-ttu-id="a4355-104">**即将推出！**</span><span class="sxs-lookup"><span data-stu-id="a4355-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="a4355-105">建议</span><span class="sxs-lookup"><span data-stu-id="a4355-105">Suggestion</span></span>

`Missing attribute: manager. Add a valid Microsoft alias for the author's manager.`

<span data-ttu-id="a4355-106">一些内容组需要 `manager` 属性来标识创建者的管理员。</span><span class="sxs-lookup"><span data-stu-id="a4355-106">Some content groups require the `manager` attribute to identify the author's manager.</span></span>

## <a name="resolution"></a><span data-ttu-id="a4355-107">解决方法</span><span class="sxs-lookup"><span data-stu-id="a4355-107">Resolution</span></span>

<span data-ttu-id="a4355-108">请为 `manager` 添加有效的 Microsoft 别名：</span><span class="sxs-lookup"><span data-stu-id="a4355-108">Add a valid Microsoft alias for `manager`:</span></span>

```yml
---
ms.author: mbradley
manager: jemash
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
