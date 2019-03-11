---
title: internal-bookmark-not-found
description: 有关 Docs 生成问题 internal-bookmark-not-found 的解释和解决方法
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/28/2019
ms.prod: non-product-specific
ms.openlocfilehash: 9073603d4e745db2f49b57a8901e00a03d8f570f
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/05/2019
ms.locfileid: "57427225"
---
# <a name="internal-bookmark-not-found"></a><span data-ttu-id="c4f2c-103">internal-bookmark-not-found</span><span class="sxs-lookup"><span data-stu-id="c4f2c-103">internal-bookmark-not-found</span></span>

<span data-ttu-id="c4f2c-104">**即将推出！**</span><span class="sxs-lookup"><span data-stu-id="c4f2c-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="c4f2c-105">建议</span><span class="sxs-lookup"><span data-stu-id="c4f2c-105">Suggestion</span></span>

`Current file doesn't contain a bookmark named '{bookmark}'.`

<span data-ttu-id="c4f2c-106">想要链接到当前不存在的文件中的标题。</span><span class="sxs-lookup"><span data-stu-id="c4f2c-106">You're trying to link to a heading in the current file that doesn't exist.</span></span>

## <a name="resolution"></a><span data-ttu-id="c4f2c-107">解决方法</span><span class="sxs-lookup"><span data-stu-id="c4f2c-107">Resolution</span></span>

[!INCLUDE [docs-authoring-pack](includes/docs-authoring-pack.md)]

<span data-ttu-id="c4f2c-108">验证你想要链接到的标题并更新链接。</span><span class="sxs-lookup"><span data-stu-id="c4f2c-108">Verify the heading you want to link to and update the link.</span></span>

<span data-ttu-id="c4f2c-109">若要链接到当前文章中的某个部分，请使用一个井号，后跟标题内容。</span><span class="sxs-lookup"><span data-stu-id="c4f2c-109">To link to a section in the current article, use a hash symbol, followed by the words of the heading.</span></span> <span data-ttu-id="c4f2c-110">删除标题中的标点符号并将空格替换为短划线。</span><span class="sxs-lookup"><span data-stu-id="c4f2c-110">Remove punctuation from the heading and replace spaces with dashes.</span></span> <span data-ttu-id="c4f2c-111">下面是一个示例：</span><span class="sxs-lookup"><span data-stu-id="c4f2c-111">The following is an example:</span></span>

```markdown
[Managed Disks](#managed-disks)
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
