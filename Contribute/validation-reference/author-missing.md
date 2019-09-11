---
title: author-missing
description: 有关 Docs 生成问题 author-missin 的解释和解决方案。
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 09/10/2019
ms.prod: non-product-specific
ms.openlocfilehash: 904ec2ad495945d882e581a240f6a72ca650c37e
ms.sourcegitcommit: 89147521f0aa3b39e7ddf390136b09a43d95c416
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/10/2019
ms.locfileid: "70848584"
---
# <a name="author-missing"></a><span data-ttu-id="c97cc-103">author-missing</span><span class="sxs-lookup"><span data-stu-id="c97cc-103">author-missing</span></span>

## <a name="warning"></a><span data-ttu-id="c97cc-104">警告</span><span class="sxs-lookup"><span data-stu-id="c97cc-104">Warning</span></span>

`Missing attribute: author. Add the current author's GitHub ID.`

<span data-ttu-id="c97cc-105">`author` 属性通过 GitHub ID 标识文章的作者。</span><span class="sxs-lookup"><span data-stu-id="c97cc-105">The `author` attribute identifies the author of the article by GitHub ID.</span></span> 

## <a name="resolution"></a><span data-ttu-id="c97cc-106">解决方法</span><span class="sxs-lookup"><span data-stu-id="c97cc-106">Resolution</span></span>

<span data-ttu-id="c97cc-107">请将当前作者的 GitHub ID 添加到 YML 标头：</span><span class="sxs-lookup"><span data-stu-id="c97cc-107">Add the current author's GitHub ID to the YML header:</span></span>

```yml
---
author: meganbradley
ms.author: mbradley
---
```

<span data-ttu-id="c97cc-108">注意，如果所有权发生变更，则应该是此文章的当前作者，而不是原作者  。</span><span class="sxs-lookup"><span data-stu-id="c97cc-108">Note that this should be the *current* owner of the article, not the original author if ownership has changed.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
