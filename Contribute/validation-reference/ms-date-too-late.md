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
# <a name="ms-date-too-late"></a>ms-date-too-late

**即将推出！**

## <a name="warning"></a>警告

`Invalid value for ms.date. The freshness date can't be more than five days in the future.`

`ms.date` 属性用于指示“新鲜度” - 即上次审阅文章的相关性、准确性、正确的屏幕截图和工作链接的具体时间。 因此，该日期不能使用将来的时间！ 允许指定五天来作为发布时间，例如，在冻结内容进行 QA 以准备重大事件时。

## <a name="resolution"></a>解决方法

请将 `ms.date` 指定为从今天起不超过五天的某个时间，格式为 MM/DD/YYYY。

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
