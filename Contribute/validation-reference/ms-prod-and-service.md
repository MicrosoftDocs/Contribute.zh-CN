---
title: ms-prod-and-service
description: 有关 Docs 生成问题 ms-prod-and-service 的解释和解决方案
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: 25a5d2be7d6aad175d746e49e064728020a8ac93
ms.sourcegitcommit: dd751d0cb5b11f81a64ef62f3c83fd17cc5f0541
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/03/2019
ms.locfileid: "70236351"
---
# <a name="ms-prod-and-service"></a>ms-prod-and-service

## <a name="warning"></a>警告
https://review.docs.microsoft.com/en-us/help/contribute/metadata-changes?branch=master `Both ms.prod and ms.service can't be specified. Use ms.prod for on-premise products, or ms.service for cloud services.`

## <a name="resolution"></a>解决方法

`ms.prod` 或 `ms.service` 是必需的，但它们不能同时存在：`ms.prod` 用于本地产品；`ms.service` 用于云服务。 请确定哪个适合你的文章，验证该值正确无误，并删除另一个字段。

可以在[此 Microsoft 内部网站](https://docsmetadatatool.azurewebsites.net/allowlists)上找到有效值。 要请求新值，请按照[此过程](https://review.docs.microsoft.com/en-us/help/contribute/metadata-changes?branch=master)操作。

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
