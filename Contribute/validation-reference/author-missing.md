---
title: author-missing
description: 有关 Docs 生成问题 author-missin 的解释和解决方案。
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: 33d704d64f4a3a1d96792bb01b403aefb3143eb8
ms.sourcegitcommit: 1311ccbbf38312bfe6947082870bc9e90d38c986
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/11/2019
ms.locfileid: "67791506"
---
# <a name="author-missing"></a>author-missing

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>建议

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
