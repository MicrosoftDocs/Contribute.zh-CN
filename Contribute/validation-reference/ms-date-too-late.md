---
title: ms-date-too-late
description: 有关 Docs 生成问题 ms-date-too-late 的解释和解决方案
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: b38392e9f297e4ee4147ca7fc65f938b5cd53403
ms.sourcegitcommit: f374ad2607360f46d88982b4b7ecc63d3ab08235
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/20/2019
ms.locfileid: "56431475"
---
# <a name="ms-date-too-late"></a><span data-ttu-id="ed473-103">ms-date-too-late</span><span class="sxs-lookup"><span data-stu-id="ed473-103">ms-date-too-late</span></span>

<span data-ttu-id="ed473-104">**即将推出！**</span><span class="sxs-lookup"><span data-stu-id="ed473-104">**Coming soon!**</span></span>

## <a name="warning"></a><span data-ttu-id="ed473-105">警告</span><span class="sxs-lookup"><span data-stu-id="ed473-105">Warning</span></span>

`Invalid value for ms.date. The freshness date can't be more than five days in the future.`

<span data-ttu-id="ed473-106">`ms.date` 属性用于指示“新鲜度” - 即上次审阅文章的相关性、准确性、正确的屏幕截图和工作链接的具体时间。</span><span class="sxs-lookup"><span data-stu-id="ed473-106">The `ms.date` attribute is used to indicate "freshness" - that is, when the article was last reviewed for relevance, accuracy, correct screen shots, and working links.</span></span> <span data-ttu-id="ed473-107">因此，该日期不能使用将来的时间！</span><span class="sxs-lookup"><span data-stu-id="ed473-107">Therefore, it can't be in the future!</span></span> <span data-ttu-id="ed473-108">允许指定五天来作为发布时间，例如，在冻结内容进行 QA 以准备重大事件时。</span><span class="sxs-lookup"><span data-stu-id="ed473-108">Five days are allowed to account for release time, such as when content is frozen for QA in preparation for a major event.</span></span>

## <a name="resolution"></a><span data-ttu-id="ed473-109">解决方法</span><span class="sxs-lookup"><span data-stu-id="ed473-109">Resolution</span></span>

<span data-ttu-id="ed473-110">将 `ms.date` 指定为距今天不超过五天的日期，格式为 MM/DD/YYYY：</span><span class="sxs-lookup"><span data-stu-id="ed473-110">Specify an `ms.date` no more than five days from today, in format MM/DD/YYYY:</span></span>

```yml
---
ms.date: 02/19/2019
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
