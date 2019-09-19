---
title: h1-not-first
description: 有关 Docs 生成问题 h1-not-first 的解释和解决方法
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 09/10/2019
ms.prod: non-product-specific
ms.openlocfilehash: c5e2eeeb5c464cd2923e23110cdab9a83324e53e
ms.sourcegitcommit: 89ec9772d9cc8281c633833c6fa51f629e9cd566
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/11/2019
ms.locfileid: "70895453"
---
# <a name="h1-not-first"></a><span data-ttu-id="0f38b-103">h1-not-first</span><span class="sxs-lookup"><span data-stu-id="0f38b-103">h1-not-first</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="0f38b-104">建议</span><span class="sxs-lookup"><span data-stu-id="0f38b-104">Suggestion</span></span>

`Markdown content is not allowed before H1.`

<span data-ttu-id="0f38b-105">在 Markdown 文件中，只有 YAML 元数据标头可以位于 H1 之前。</span><span class="sxs-lookup"><span data-stu-id="0f38b-105">Only the YAML metadata header can come before the H1 in a Markdown file.</span></span> <span data-ttu-id="0f38b-106">例如，如果想要在文章顶部添加注释或图像，则必须将其放置在 H1 之后。</span><span class="sxs-lookup"><span data-stu-id="0f38b-106">For example, if you want to add a note or an image at the top of the article, it must come after H1.</span></span> <span data-ttu-id="0f38b-107">不允许以下操作：</span><span class="sxs-lookup"><span data-stu-id="0f38b-107">The following is not allowed:</span></span>

```markdown
---
# This is the YAML metadata header
author: meganbradley
---
> [!NOTE]
> You can't do this.

# This is the H1
```

<span data-ttu-id="0f38b-108">请改为执行此操作：</span><span class="sxs-lookup"><span data-stu-id="0f38b-108">Do this instead:</span></span>

```markdown
---
# This is the YAML metadata header
author: meganbradley
---
# This is the H1

> [!NOTE]
> This is OK.
```

<span data-ttu-id="0f38b-109">造成此问题的另一个常见原因是 YAML 标头之前的 [字节顺序标记 (BOM)](http://www.websina.com/bugzero/kb/unicode-bom.html)。</span><span class="sxs-lookup"><span data-stu-id="0f38b-109">Another common cause of this issue is [byte order marks (BOMs)](http://www.websina.com/bugzero/kb/unicode-bom.html) before the YAML header.</span></span> <span data-ttu-id="0f38b-110">向存储库提交内容时，有时候编码问题会引入这些标记。</span><span class="sxs-lookup"><span data-stu-id="0f38b-110">These are sometimes introduced by encoding issues when committing content to repos.</span></span> <span data-ttu-id="0f38b-111">它们会在 GitHub 中导致糟糕的呈现效果，应将它们删除。</span><span class="sxs-lookup"><span data-stu-id="0f38b-111">They result in bad rendering in GitHub and should be removed.</span></span>

## <a name="resolution"></a><span data-ttu-id="0f38b-112">解决方法</span><span class="sxs-lookup"><span data-stu-id="0f38b-112">Resolution</span></span>

<span data-ttu-id="0f38b-113">删除 H1 之前除 YAML 元数据标头以外的任何内容。</span><span class="sxs-lookup"><span data-stu-id="0f38b-113">Remove any content other than the YAML metadata header from before the H1.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
