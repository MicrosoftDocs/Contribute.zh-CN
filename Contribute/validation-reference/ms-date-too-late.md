---
title: ms-date-too-late
description: 有关 Docs 生成问题 ms-date-too-late 的解释和解决方案
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: 863b13e55c2aaa2057920e3bd77ec75ab5945277
ms.sourcegitcommit: 203ca15fda2d217f082c74ec648c1f1db323f9f1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/04/2019
ms.locfileid: "55713099"
---
# <a name="ms-date-too-late"></a><span data-ttu-id="d119b-103">ms-date-too-late</span><span class="sxs-lookup"><span data-stu-id="d119b-103">ms-date-too-late</span></span>

<span data-ttu-id="d119b-104">**即将推出！**</span><span class="sxs-lookup"><span data-stu-id="d119b-104">**Coming soon!**</span></span>

## <a name="warning"></a><span data-ttu-id="d119b-105">警告</span><span class="sxs-lookup"><span data-stu-id="d119b-105">Warning</span></span>

`Invalid value for ms.date. The freshness date can't be more than five days in the future.`

<span data-ttu-id="d119b-106">`ms.date` 属性用于指示“新鲜度” - 即上次审阅文章的相关性、准确性、正确的屏幕截图和工作链接的具体时间。</span><span class="sxs-lookup"><span data-stu-id="d119b-106">The `ms.date` attribute is used to indicate "freshness" - that is, when the article was last reviewed for relevance, accuracy, correct screen shots, and working links.</span></span> <span data-ttu-id="d119b-107">因此，该日期不能使用将来的时间！</span><span class="sxs-lookup"><span data-stu-id="d119b-107">Therefore, it can't be in the future!</span></span> <span data-ttu-id="d119b-108">允许指定五天来作为发布时间，例如，在冻结内容进行 QA 以准备重大事件时。</span><span class="sxs-lookup"><span data-stu-id="d119b-108">Five days are allowed to account for release time, such as when content is frozen for QA in preparation for a major event.</span></span>

## <a name="resolution"></a><span data-ttu-id="d119b-109">解决方法</span><span class="sxs-lookup"><span data-stu-id="d119b-109">Resolution</span></span>

<span data-ttu-id="d119b-110">请将 `ms.date` 指定为从今天起不超过五天的某个时间，格式为 MM/DD/YYYY。</span><span class="sxs-lookup"><span data-stu-id="d119b-110">Specify an `ms.date` no more than five days from today, in format MM/DD/YYYY.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
