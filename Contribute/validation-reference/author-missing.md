---
title: author-missing
description: 有关 Docs 生成问题 author-missin 的解释和解决方案。
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: 6c7306cf674a345b25d3e05c4e00662623c44469
ms.sourcegitcommit: 8e897e90268a8a87dc4b97d7c28d22ed5950c8d9
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/29/2019
ms.locfileid: "58637428"
---
# <a name="author-missing"></a><span data-ttu-id="920c4-103">author-missing</span><span class="sxs-lookup"><span data-stu-id="920c4-103">author-missing</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="920c4-104">建议</span><span class="sxs-lookup"><span data-stu-id="920c4-104">Suggestion</span></span>

`Missing attribute: author. Add a valid GitHub ID.`

<span data-ttu-id="920c4-105">`author` 属性通过 GitHub ID 标识文章的作者。</span><span class="sxs-lookup"><span data-stu-id="920c4-105">The `author` attribute identifies the author of the article by GitHub ID.</span></span> 

## <a name="resolution"></a><span data-ttu-id="920c4-106">解决方法</span><span class="sxs-lookup"><span data-stu-id="920c4-106">Resolution</span></span>

<span data-ttu-id="920c4-107">请将作者的 GitHub ID 添加到 YML 标头：</span><span class="sxs-lookup"><span data-stu-id="920c4-107">Add the author's GitHub ID to the YML header:</span></span>

```yml
---
author: meganbradley
ms.author: mbradley
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]