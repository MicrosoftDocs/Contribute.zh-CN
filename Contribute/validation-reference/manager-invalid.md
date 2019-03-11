---
title: manager-invalid
description: 有关 Docs 生成问题 manager-invalid 的解释和解决方法
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 3/1/2019
ms.prod: non-product-specific
ms.openlocfilehash: 7eac188b16b402767bbec551a6dec8b5877680af
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/05/2019
ms.locfileid: "57427170"
---
# <a name="manager-invalid"></a>manager-invalid

**即将推出！**

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>建议

`Invalid value for manager: '{value}' is not a valid Microsoft alias.`

一些内容组需要 `manager` 属性来标识创建者的管理员。

## <a name="resolution"></a>解决方法

`manager` 的值必须是各 Microsoft 员工有效别名。 验证创建者的管理员别名并更新值。

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
