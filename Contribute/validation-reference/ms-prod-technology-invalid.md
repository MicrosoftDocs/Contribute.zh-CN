---
title: ms-prod-and-technology-invalid
description: 有关 Docs 生成问题 ms-prod-and-technology-invalid 的解释和解决方案
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: 20706a44da0320c1a3fc85592a4636efba364dc7
ms.sourcegitcommit: 42e5a6ae071826afc2a32a9b7150ca113b39afdf
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/19/2019
ms.locfileid: "57987574"
---
# <a name="ms-prod-and-technology-invalid"></a>ms-prod-and-technology-invalid

**即将推出！**

## <a name="warning"></a>警告

`Invalid value for ms.prod: '{value}'.`

`Invalid value for ms.technology: '{value}' is not valid with ms.prod value '{value}'.`

请使用 `ms.prod` 指定本地产品。 若要指定有关 `ms.prod` 更详细的信息，可以选择指定 `ms.technology`。 `ms.prod` 和 `ms.technology` 的值必须是有效对。 `ms.prod` 值无效，或 `ms.technology` 值与 `ms.prod` 不是有效对。

## <a name="resolution"></a>解决方法

请确认文章的 `ms.prod` 值正确无误。 然后选择有效的 `ms.technology` 值。

可以在[此 Microsoft 内部网站](https://docsmetadatatool.azurewebsites.net/allowlists)上找到有效值。

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
