---
title: ms-prod-and-technology-invalid
description: 有关 Docs 生成问题 ms-prod-and-technology-invalid 的解释和解决方案
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: 92e8b17c3b5c96d544d12d394534a494ada3b901
ms.sourcegitcommit: 203ca15fda2d217f082c74ec648c1f1db323f9f1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/04/2019
ms.locfileid: "55713260"
---
# <a name="ms-prod-and-technology-invalid"></a>ms-prod-and-technology-invalid

**即将推出！**

## <a name="warning"></a>警告

`Invalid value for ms.prod: '{value}'.`

`Invalid value for ms.technology: '{value}' is not valid with ms.prod value '{value}'.`

请使用 `ms.prod` 指定本地产品。 若要指定有关 `ms.prod` 更详细的信息，可以选择指定 `ms.technology`。 `ms.prod` 和 `ms.technology` 的值必须是有效对。 `ms.prod` 值无效，或 `ms.technology` 值与 `ms.prod` 不是有效对。

## <a name="resolution"></a>解决方法

请确认文章的 `ms.prod` 值正确无误。 然后选择有效的 `ms.technology` 值。

可以在[此 Microsoft 内部网站](https://docsmetadatatool.azurewebsites.net/whitelists)上找到有效值。

<!-- Can we link to whitelist externally? -->

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
