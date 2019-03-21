---
title: ms-service-missing
description: 有关 Docs 生成问题 ms-service-missing 的解释和解决方案
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/2/2019
ms.prod: non-product-specific
ms.openlocfilehash: 7c5860d9ef50598ad5b3e9546100af0ba436e69f
ms.sourcegitcommit: 42e5a6ae071826afc2a32a9b7150ca113b39afdf
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/19/2019
ms.locfileid: "57987712"
---
# <a name="ms-service-missing"></a>ms-service-missing

**即将推出！**

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>建议

`Missing attribute: ms.service. If you specify ms.subservice, you must also specify ms.service.`

请使用 `ms.service` 指定云服务。 若要指定有关 `ms.service` 更详细的信息，可以选择指定 `ms.subservice`，但如果指定 `ms.subservice`，则必须同时指定 `ms.service`。 `ms.service` 和 `ms.subservice` 的值必须是有效对。

## <a name="resolution"></a>解决方法

请确认所指定的 `ms.subservice` 值对于文章正确无误。 然后添加适当的 `ms.service` 值，该值是 `ms.subservice` 的有效父级。

可以在[此 Microsoft 内部网站](https://docsmetadatatool.azurewebsites.net/allowlists)上找到有效值。

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
