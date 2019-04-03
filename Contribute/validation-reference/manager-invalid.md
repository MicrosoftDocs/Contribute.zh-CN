---
title: manager-invalid
description: 有关 Docs 生成问题 manager-invalid 的解释和解决方法
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 3/1/2019
ms.prod: non-product-specific
ms.openlocfilehash: 44174bde29b63bffe709596f9c2d6be994f252a3
ms.sourcegitcommit: 8e897e90268a8a87dc4b97d7c28d22ed5950c8d9
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/29/2019
ms.locfileid: "58637221"
---
# <a name="manager-invalid"></a>manager-invalid

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>建议

`Invalid value for manager: '{value}' is not a valid Microsoft alias.`

一些内容组需要 `manager` 属性来标识创建者的管理员。

## <a name="resolution"></a>解决方法

`manager` 的值必须是各 Microsoft 员工有效别名。 验证创建者的管理员别名并更新值。

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
