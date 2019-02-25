---
title: deprecated-attribute
description: 有关 Docs 生成问题 deprecated-attribute 的解释和解决办法
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/1/2019
ms.prod: non-product-specific
ms.openlocfilehash: 4f9ddc611d401bc7003e1b7d378517d5e374da87
ms.sourcegitcommit: a2c8317ccf8b56371773c84f4960a44787ce8666
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2019
ms.locfileid: "56322668"
---
# <a name="deprecated-attribute"></a>deprecated-attribute

**即将推出！**

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>建议

`Deprecated attribute: ms.component. Use ms.subservice instead.`

请使用 `ms.service` 指定云服务。 若要指定有关 `ms.service` 更详细的信息，可以选择指定 `ms.subservice`。 请勿使用 `ms.component`；它已针对此内容弃用。

## <a name="resolution"></a>解决方法

请确认文章的 `ms.service` 值正确无误。 然后选择有效的 `ms.subservice` 值。

可以在[此 Microsoft 内部网站](https://docsmetadatatool.azurewebsites.net/whitelists)上找到有效值。

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
