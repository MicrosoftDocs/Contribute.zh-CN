---
title: author-missing
description: 有关 Docs 生成问题 author-missin 的解释和解决方案。
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: cba9788c113101fc93bffa674702b2bed95afbcb
ms.sourcegitcommit: 203ca15fda2d217f082c74ec648c1f1db323f9f1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/04/2019
ms.locfileid: "55713030"
---
# <a name="author-missing"></a><span data-ttu-id="6e52b-103">author-missing</span><span class="sxs-lookup"><span data-stu-id="6e52b-103">author-missing</span></span>

<span data-ttu-id="6e52b-104">**即将推出！**</span><span class="sxs-lookup"><span data-stu-id="6e52b-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="6e52b-105">建议</span><span class="sxs-lookup"><span data-stu-id="6e52b-105">Suggestion</span></span>

`Missing attribute: author. Add a valid GitHub ID.`

<span data-ttu-id="6e52b-106">`author` 属性通过 GitHub ID 标识文章的作者。</span><span class="sxs-lookup"><span data-stu-id="6e52b-106">The `author` attribute identifies the author of the article by GitHub ID.</span></span> 

## <a name="resolution"></a><span data-ttu-id="6e52b-107">解决方法</span><span class="sxs-lookup"><span data-stu-id="6e52b-107">Resolution</span></span>

<span data-ttu-id="6e52b-108">请将作者的 GitHub ID 添加到 YML 标头：</span><span class="sxs-lookup"><span data-stu-id="6e52b-108">Add the author's GitHub ID to the YML header:</span></span>

```markdown
---
author: meganbradley
ms.author: mbradley
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]