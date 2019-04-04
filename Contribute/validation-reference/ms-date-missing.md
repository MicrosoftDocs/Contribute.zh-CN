---
title: ms-date-missing
description: 有关 Docs 生成问题 ms-date-missing 的解释和解决方案
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: ae2a28993671255a9ffd4503eebdbee404e52373
ms.sourcegitcommit: 8e897e90268a8a87dc4b97d7c28d22ed5950c8d9
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/29/2019
ms.locfileid: "58637267"
---
# <a name="ms-date-missing"></a>ms-date-missing

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>建议

`Missing attribute: ms.date. A freshness date is required for this content. Add a date in format MM/DD/YYYY.`

某些内容组需要使用 `ms.date` 来指示“新鲜度” - 即上次审阅文章的相关性、准确性、正确的屏幕截图和工作链接的具体时间。 该日期与文章发布的最后日期不同，如果未显式指定 `ms.date`，则会在页面上显示该日期。

## <a name="resolution"></a>解决方法

确认文章是否是最新的，且没有损坏的内容，再添加 MM/DD/YYYY 格式的有效日期：

```yml
---
ms.date: 02/19/2019
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
