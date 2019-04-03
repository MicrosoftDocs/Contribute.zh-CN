---
title: multiple-values
description: 有关 Docs 生成问题 multiple-values 的解释和解决办法
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/19/2019
ms.prod: non-product-specific
ms.openlocfilehash: f8c2825801392e8ff1114e6abd08518a59ee8087
ms.sourcegitcommit: 8e897e90268a8a87dc4b97d7c28d22ed5950c8d9
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/29/2019
ms.locfileid: "58637313"
---
# <a name="multiple-values"></a>multiple-values

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>建议

`Single-valued attribute {attribute} has multiple values. Remove additional values.`

为只允许一个值的属性指定了多个值。

`Single-valued attribute {attribute} is in multi-valued array format. Change to scalar format.`

必须以单值（标量）YML 格式指定不允许有多个值的属性。

## <a name="resolution"></a>解决方法

只要多值数组用于单值属性，无论数组中有多个值还是一个值，都会收到此建议。

YML 支持以下多值属性（如 `ms.custom`）数组格式：

```yml
---
# comma-separated bracketed list:
ms.custom: [WIP, generated-via-CI]

# each value on its own line:
ms.custom:
  - WIP
  - generated-via-CI
---
```

这些格式对单值属性（如 `author`）无效。

如果指定了多个值，请检查指定的值，并确定哪个是正确的。 删除其他值，并在同一行中指定一个不带括号的值作为属性，如下所示：

```yml
---
author: meganbradley
---
```

如果有单值数组，请将它更改为上面的标量格式。

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
