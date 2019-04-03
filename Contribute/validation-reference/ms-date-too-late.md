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
# <a name="ms-date-too-late"></a>ms-date-too-late

## <a name="warning"></a>警告

`Invalid value for ms.date. The freshness date can't be more than five days in the future.`

`ms.date` 属性用于指示“新鲜度” - 即上次审阅文章的相关性、准确性、正确的屏幕截图和工作链接的具体时间。 因此，该日期不能使用将来的时间！ 允许指定五天来作为发布时间，例如，在冻结内容进行 QA 以准备重大事件时。

## <a name="resolution"></a>解决方法

将 `ms.date` 指定为距今天不超过五天的日期，格式为 MM/DD/YYYY：

```yml
---
ms.date: 02/19/2019
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
