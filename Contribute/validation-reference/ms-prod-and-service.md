---
title: ms-prod-and-service
description: 有关 Docs 生成问题 ms-prod-and-service 的解释和解决方案
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: b685144e92485df2dddb9bdda09fea47d75f588f
ms.sourcegitcommit: 42e5a6ae071826afc2a32a9b7150ca113b39afdf
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/19/2019
ms.locfileid: "57987666"
---
# <a name="ms-prod-and-service"></a>ms-prod-and-service

**即将推出！**

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>建议

`Both ms.prod and ms.service can't be specified. Use ms.prod for on-premise products, or ms.service for cloud services.`

## <a name="resolution"></a>解决方法

`ms.prod` 或 `ms.service` 是必需的，但它们不能同时存在：`ms.prod` 用于本地产品；`ms.service` 用于云服务。 请确定哪个适合你的文章，验证该值正确无误，并删除另一个字段。

可以在[此 Microsoft 内部网站](https://docsmetadatatool.azurewebsites.net/allowlists)上找到有效值。

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
