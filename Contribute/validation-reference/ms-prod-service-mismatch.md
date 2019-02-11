---
title: ms-prod-service-mismatch
description: 有关 Docs 生成问题 ms-prod-service-mismatch 的解释和解决方案
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: 4a3cf8bc5435972f0442ca1d41d4147e1ea00d78
ms.sourcegitcommit: 203ca15fda2d217f082c74ec648c1f1db323f9f1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/04/2019
ms.locfileid: "55713168"
---
# <a name="ms-prod-service-mismatch"></a>ms-prod-service-mismatch

**即将推出！**

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>建议

`Invalid attribute pair: ms.prod and ms.subservice. You can only pair ms.prod with ms.technology.`

`Invalid attribute pair: ms.service and ms.technology. You can only pair ms.service with ms.subservice.`

请使用 `ms.prod` 指定本地产品；`ms.service` 用于云服务。 若要指定有关 `ms.prod` 更详细的信息，可以选择指定 `ms.technology`。 若要指定有关 `ms.service` 更详细的信息，可以指定 `ms.subservice`。 不能将 `ms.prod` 与 `ms.subservice` 一起使用，也不能将 `ms.service` 与 `ms.technology` 一起使用。

## <a name="resolution"></a>解决方法

首先，请验证是否已为文章选择了正确的父属性（`ms.prod` 或 `ms.service`）。 然后，添加具有有效成对值的相应子字段。 删除所有额外字段。

可以在[此 Microsoft 内部网站](https://docsmetadatatool.azurewebsites.net/whitelists)上找到有效值。

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
