---
title: ms-service-and-subservice-invalid
description: 有关 Docs 生成问题 ms-service-and-subservice-invalid 的解释和解决方案
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: a6059d592212b271780344a086ee68c7133e15cd
ms.sourcegitcommit: dd751d0cb5b11f81a64ef62f3c83fd17cc5f0541
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/03/2019
ms.locfileid: "70236525"
---
# <a name="ms-service-and-subservice-invalid"></a>ms-service-and-subservice-invalid

## <a name="warning"></a>警告

`Invalid value for ms.service: '{value}'.`

`Invalid value for ms.subservice: '{value}' is not valid with ms.service value '{value}'.`

请使用 `ms.service` 指定云服务。 若要指定有关 `ms.service` 更详细的信息，可以选择指定 `ms.subservice`。 `ms.service` 和 `ms.subservice` 的值必须是有效对。 `ms.service` 值无效，或 `ms.subservice` 值与 `ms.service` 不是有效对。

## <a name="resolution"></a>解决方法

请确认文章的 `ms.service` 值正确无误。 然后选择有效的 `ms.subservice` 值。

可以在[此 Microsoft 内部网站](https://docsmetadatatool.azurewebsites.net/allowlists)上找到有效值。 要请求新值，请按照[此过程](https://review.docs.microsoft.com/help/contribute/metadata-changes?branch=master)操作。

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
