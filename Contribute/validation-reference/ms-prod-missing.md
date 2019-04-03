---
title: ms-prod-missing
description: 有关 Docs 生成问题 ms-prod-missing 的解释和解决方案
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/2/2019
ms.prod: non-product-specific
ms.openlocfilehash: 9b3f209ca2300735210490ffd58c3ac423c44fef
ms.sourcegitcommit: 8e897e90268a8a87dc4b97d7c28d22ed5950c8d9
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/29/2019
ms.locfileid: "58636761"
---
# <a name="ms-prod-missing"></a>ms-prod-missing

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>建议

`Missing attribute: ms.prod. If you specify ms.technology, you must also specify ms.prod.`

请使用 `ms.prod` 指定本地产品。 若要指定有关 `ms.prod` 更详细的信息，可以选择指定 `ms.technology`，但如果指定 `ms.technology`，则必须同时指定 `ms.prod`。 `ms.prod` 和 `ms.technology` 的值必须是有效对。

## <a name="resolution"></a>解决方法

请确认所指定的 `ms.technology` 值对于文章正确无误。 然后添加适当的 `ms.prod` 值，该值是 `ms.technology` 的有效父级。

可以在[此 Microsoft 内部网站](https://docsmetadatatool.azurewebsites.net/allowlists)上找到有效值。

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
