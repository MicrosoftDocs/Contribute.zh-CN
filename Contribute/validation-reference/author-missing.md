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
# <a name="author-missing"></a><span data-ttu-id="1f1ae-103">author-missing</span><span class="sxs-lookup"><span data-stu-id="1f1ae-103">author-missing</span></span>

<span data-ttu-id="1f1ae-104">**即将推出！**</span><span class="sxs-lookup"><span data-stu-id="1f1ae-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="1f1ae-105">建议</span><span class="sxs-lookup"><span data-stu-id="1f1ae-105">Suggestion</span></span>

`Missing attribute: author. Add a valid GitHub ID.`

<span data-ttu-id="1f1ae-106">`author` 属性通过 GitHub ID 标识文章的作者。</span><span class="sxs-lookup"><span data-stu-id="1f1ae-106">The `author` attribute identifies the author of the article by GitHub ID.</span></span> 

## <a name="resolution"></a><span data-ttu-id="1f1ae-107">解决方法</span><span class="sxs-lookup"><span data-stu-id="1f1ae-107">Resolution</span></span>

<span data-ttu-id="1f1ae-108">请将作者的 GitHub ID 添加到 YML 标头：</span><span class="sxs-lookup"><span data-stu-id="1f1ae-108">Add the author's GitHub ID to the YML header:</span></span>

```yml
---
author: meganbradley
ms.author: mbradley
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]