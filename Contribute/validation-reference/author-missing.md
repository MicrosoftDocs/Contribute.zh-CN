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
# <a name="author-missing"></a><span data-ttu-id="5b2e1-103">author-missing</span><span class="sxs-lookup"><span data-stu-id="5b2e1-103">author-missing</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="5b2e1-104">建议</span><span class="sxs-lookup"><span data-stu-id="5b2e1-104">Suggestion</span></span>

`Missing attribute: author. Add the current author's GitHub ID.`

<span data-ttu-id="5b2e1-105">`author` 属性通过 GitHub ID 标识文章的作者。</span><span class="sxs-lookup"><span data-stu-id="5b2e1-105">The `author` attribute identifies the author of the article by GitHub ID.</span></span> 

## <a name="resolution"></a><span data-ttu-id="5b2e1-106">解决方法</span><span class="sxs-lookup"><span data-stu-id="5b2e1-106">Resolution</span></span>

<span data-ttu-id="5b2e1-107">请将当前作者的 GitHub ID 添加到 YML 标头：</span><span class="sxs-lookup"><span data-stu-id="5b2e1-107">Add the current author's GitHub ID to the YML header:</span></span>

```yml
---
author: meganbradley
ms.author: mbradley
---
```

<span data-ttu-id="5b2e1-108">注意，如果所有权发生变更，则应该是此文章的当前作者，而不是原作者  。</span><span class="sxs-lookup"><span data-stu-id="5b2e1-108">Note that this should be the *current* owner of the article, not the original author if ownership has changed.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
