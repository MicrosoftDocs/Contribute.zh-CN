---
title: yaml-header-invalid
description: 有关 Docs 生成问题 yaml-header-invalid 的解释和解决方法
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/26/2019
ms.prod: non-product-specific
ms.openlocfilehash: 62b3b2c2aa47525cae5dd5c0955eb88463124359
ms.sourcegitcommit: 89eb357721b26710e00d9b8fdab3e7628c34bdb6
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/06/2019
ms.locfileid: "57459018"
---
# <a name="yaml-header-invalid"></a>yaml-header-invalid

## <a name="warning"></a>警告

`Invalid YAML header: Improper use of a colon in a metadata entry.`

这通常意味着 YAML 标头中未加引号的元数据值包含冒号或其他特殊字符。 它还可能意味着键/值对中的冒号后缺少空格。

## <a name="resolution"></a>解决方法

审阅 YAML 标头。 查找以下错误。

未加引号的值中的冒号：

```yml
---
title: Common mistake: I included a colon in my unquoted value.
---
```

更改为：

```yml
---
title: 'Common mistake: I included a colon in my unquoted value.'
---
```

键/值对中的冒号后没有空格：

```yml
---
title:I omitted a space.
---
```

更改为：

```yml
---
title: I omitted a space.
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
