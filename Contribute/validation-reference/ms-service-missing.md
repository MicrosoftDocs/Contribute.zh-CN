---
title: ms-service-missing
description: 有关 Docs 生成问题 ms-service-missing 的解释和解决方案
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/2/2019
ms.prod: non-product-specific
ms.openlocfilehash: b50d9d6f57c953569a4e5dd873961b8c511a8bb1
ms.sourcegitcommit: dd751d0cb5b11f81a64ef62f3c83fd17cc5f0541
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/03/2019
ms.locfileid: "70236502"
---
# <a name="ms-service-missing"></a>ms-service-missing

## <a name="warning"></a>警告

`Missing attribute: ms.service. If you specify ms.subservice, you must also specify ms.service.`

请使用 `ms.service` 指定云服务。 若要指定有关 `ms.service` 更详细的信息，可以选择指定 `ms.subservice`，但如果指定 `ms.subservice`，则必须同时指定 `ms.service`。 `ms.service` 和 `ms.subservice` 的值必须是有效对。

## <a name="resolution"></a>解决方法

请确认所指定的 `ms.subservice` 值对于文章正确无误。 然后添加适当的 `ms.service` 值，该值是 `ms.subservice` 的有效父级。

可以在[此 Microsoft 内部网站](https://docsmetadatatool.azurewebsites.net/allowlists)上找到有效值。 要请求新值，请按照[此过程](https://review.docs.microsoft.com/help/contribute/metadata-changes?branch=master)操作。

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
