---
title: author-missing
description: 有关 Docs 生成问题 author-missin 的解释和解决方案。
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: 89725dcfbd4ec266071c45a003748021b480bbc2
ms.sourcegitcommit: f374ad2607360f46d88982b4b7ecc63d3ab08235
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/20/2019
ms.locfileid: "56431521"
---
# <a name="author-missing"></a>author-missing

**即将推出！**

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>建议

`Missing attribute: author. Add a valid GitHub ID.`

`author` 属性通过 GitHub ID 标识文章的作者。 

## <a name="resolution"></a>解决方法

请将作者的 GitHub ID 添加到 YML 标头：

```yml
---
author: meganbradley
ms.author: mbradley
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]