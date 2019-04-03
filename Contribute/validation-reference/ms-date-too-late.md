---
title: ms-date-too-late
description: 有关 Docs 生成问题 ms-date-too-late 的解释和解决方案
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: 4cb5da1da2fee59302791e729e5fcfb8e84170e5
ms.sourcegitcommit: 8e897e90268a8a87dc4b97d7c28d22ed5950c8d9
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/29/2019
ms.locfileid: "58637382"
---
# <a name="ms-date-too-late"></a><span data-ttu-id="c79d2-103">ms-date-too-late</span><span class="sxs-lookup"><span data-stu-id="c79d2-103">ms-date-too-late</span></span>

## <a name="warning"></a><span data-ttu-id="c79d2-104">警告</span><span class="sxs-lookup"><span data-stu-id="c79d2-104">Warning</span></span>

`Invalid value for ms.date. The freshness date can't be more than five days in the future.`

<span data-ttu-id="c79d2-105">`ms.date` 属性用于指示“新鲜度” - 即上次审阅文章的相关性、准确性、正确的屏幕截图和工作链接的具体时间。</span><span class="sxs-lookup"><span data-stu-id="c79d2-105">The `ms.date` attribute is used to indicate "freshness" - that is, when the article was last reviewed for relevance, accuracy, correct screen shots, and working links.</span></span> <span data-ttu-id="c79d2-106">因此，该日期不能使用将来的时间！</span><span class="sxs-lookup"><span data-stu-id="c79d2-106">Therefore, it can't be in the future!</span></span> <span data-ttu-id="c79d2-107">允许指定五天来作为发布时间，例如，在冻结内容进行 QA 以准备重大事件时。</span><span class="sxs-lookup"><span data-stu-id="c79d2-107">Five days are allowed to account for release time, such as when content is frozen for QA in preparation for a major event.</span></span>

## <a name="resolution"></a><span data-ttu-id="c79d2-108">解决方法</span><span class="sxs-lookup"><span data-stu-id="c79d2-108">Resolution</span></span>

<span data-ttu-id="c79d2-109">将 `ms.date` 指定为距今天不超过五天的日期，格式为 MM/DD/YYYY：</span><span class="sxs-lookup"><span data-stu-id="c79d2-109">Specify an `ms.date` no more than five days from today, in format MM/DD/YYYY:</span></span>

```yml
---
ms.date: 02/19/2019
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
