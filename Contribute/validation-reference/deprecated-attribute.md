---
title: deprecated-attribute
description: 有关 Docs 生成问题 deprecated-attribute 的解释和解决办法
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/1/2019
ms.prod: non-product-specific
ms.openlocfilehash: 15d285159b361b7fb9dbc1774e6c4b2f5f5758ed
ms.sourcegitcommit: dd751d0cb5b11f81a64ef62f3c83fd17cc5f0541
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/03/2019
ms.locfileid: "70236239"
---
# <a name="deprecated-attribute"></a>deprecated-attribute

## <a name="warning"></a>警告

`Deprecated attribute: ms.component. Use ms.subservice instead.`

请使用 `ms.service` 指定云服务。 若要指定有关 `ms.service` 更详细的信息，可以选择指定 `ms.subservice`。 请勿使用 `ms.component`；它已针对此内容弃用。

## <a name="resolution"></a>解决方法

请确认文章的 `ms.service` 值正确无误。 然后选择有效的 `ms.subservice` 值。

可以在[此 Microsoft 内部网站](https://docsmetadatatool.azurewebsites.net/allowlists)上找到有效值。

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
