---
title: ms-date-invalid
description: 有关 Docs 生成问题 ms-date-invalid 的解释和解决方案
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: e960bc2d8e9013e480f2bb391cdfa0c1da043b8b
ms.sourcegitcommit: f374ad2607360f46d88982b4b7ecc63d3ab08235
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/20/2019
ms.locfileid: "56431498"
---
# <a name="ms-date-invalid"></a><span data-ttu-id="0ec81-103">ms-date-invalid</span><span class="sxs-lookup"><span data-stu-id="0ec81-103">ms-date-invalid</span></span>

<span data-ttu-id="0ec81-104">**即将推出！**</span><span class="sxs-lookup"><span data-stu-id="0ec81-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="0ec81-105">建议</span><span class="sxs-lookup"><span data-stu-id="0ec81-105">Suggestion</span></span>

`Invalid value for ms.date: '{value}'. Must be a date in format MM/DD/YYYY.`

## <a name="resolution"></a><span data-ttu-id="0ec81-106">解决方法</span><span class="sxs-lookup"><span data-stu-id="0ec81-106">Resolution</span></span>

<span data-ttu-id="0ec81-107">确认文章是否是最新的，且没有损坏的内容，再添加 MM/DD/YYYY 格式的有效日期：</span><span class="sxs-lookup"><span data-stu-id="0ec81-107">Confirm that the article is up-to-date with no broken content, then add a valid date in the format MM/DD/YYYY:</span></span>

```yml
---
ms.date: 02/19/2019
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
