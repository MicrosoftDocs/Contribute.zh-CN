---
title: author-missing
description: 有关 Docs 生成问题 author-missin 的解释和解决方案。
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: c10bf7936968f876d983c77e64c2a8cb809baae2
ms.sourcegitcommit: dd751d0cb5b11f81a64ef62f3c83fd17cc5f0541
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/03/2019
ms.locfileid: "70236318"
---
# <a name="author-missing"></a>author-missing

## <a name="warning"></a>警告

`Missing attribute: author. Add the current author's GitHub ID.`

`author` 属性通过 GitHub ID 标识文章的作者。 

## <a name="resolution"></a>解决方法

请将当前作者的 GitHub ID 添加到 YML 标头：

```yml
---
author: meganbradley
ms.author: mbradley
---
```

注意，如果所有权发生变更，则应该是此文章的当前作者，而不是原作者  。

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
