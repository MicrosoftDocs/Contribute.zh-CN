---
title: multiple-h1
description: 有关 Docs 生成问题 multiple-h1 的解释和解决方法。
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 10/09/2019
ms.prod: non-product-specific
ms.openlocfilehash: c97ae237cd2ce657bd02132af5169cb6544ae306
ms.sourcegitcommit: 57eb071bdc55ef71fa3f8ac979326c3f8fbe9c45
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/10/2019
ms.locfileid: "72246269"
---
# <a name="multiple-h1"></a><span data-ttu-id="ad6d1-103">multiple-h1</span><span class="sxs-lookup"><span data-stu-id="ad6d1-103">multiple-h1</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="ad6d1-104">建议</span><span class="sxs-lookup"><span data-stu-id="ad6d1-104">Suggestion</span></span>

`Multiple H1s are not allowed. You can only have one top-level heading.`

<span data-ttu-id="ad6d1-105">H1 是指 Markdown 文件中的第一个标题。</span><span class="sxs-lookup"><span data-stu-id="ad6d1-105">H1 refers to the first heading in a Markdown file.</span></span> <span data-ttu-id="ad6d1-106">发布到 docs.microsoft.com 时，H1 以大字体显示在页面顶部。</span><span class="sxs-lookup"><span data-stu-id="ad6d1-106">When published to docs.microsoft.com, the H1 shows at the top of the page in a large font.</span></span> <span data-ttu-id="ad6d1-107">H1 的创建方式为，以包含一个井号 (#) 的行开头，后跟空格，然后是标题文本。</span><span class="sxs-lookup"><span data-stu-id="ad6d1-107">An H1 is created by beginning a line with a single hash (#) followed by a space, then the heading text.</span></span> <span data-ttu-id="ad6d1-108">一个文件中只能有一个 H1。</span><span class="sxs-lookup"><span data-stu-id="ad6d1-108">You can only have one H1 in each file.</span></span>

<span data-ttu-id="ad6d1-109">如果文章包含一行等于号，形成双下划线（如 `=======`），也可能会收到此消息。</span><span class="sxs-lookup"><span data-stu-id="ad6d1-109">You might also get this message if your article contains a line of equals signs making a double underline, like this: `=======`.</span></span> <span data-ttu-id="ad6d1-110">这是 H1 的替代 Markdown 语法。</span><span class="sxs-lookup"><span data-stu-id="ad6d1-110">This is an alternative Markdown syntax for an H1.</span></span> <span data-ttu-id="ad6d1-111">这种情况也通常出现在合并冲突中：</span><span class="sxs-lookup"><span data-stu-id="ad6d1-111">It's also commonly seen in merge conflicts:</span></span>

```markdown
<<<<<<< HEAD
...
=======
...
>>>>>>> 1d82c7efe18f86136247fb366df5030843199c19
```

## <a name="resolution"></a><span data-ttu-id="ad6d1-112">解决方法</span><span class="sxs-lookup"><span data-stu-id="ad6d1-112">Resolution</span></span>

<span data-ttu-id="ad6d1-113">若要解决此问题，请将后续 H1s 的标题级别更改为 H2 (`##`)，否则请重新组织文件。</span><span class="sxs-lookup"><span data-stu-id="ad6d1-113">To fix this issue, change the heading level of subsequent H1s to H2 (`##`), or otherwise reorganize your file.</span></span> <span data-ttu-id="ad6d1-114">请注意，不允许跳过标题级别，如 H1 之后为 H3。</span><span class="sxs-lookup"><span data-stu-id="ad6d1-114">Note that skipping heading levels, such as following H1 with H3, isn't allowed.</span></span>

```markdown
---
author: meganbradley
ms.author: mbradley
---
# This is an H1

Some content...

## This is an H2
```

<span data-ttu-id="ad6d1-115">如果另一个 H1 确实是双下划线 (`=======`)，请将其删除，或根据需要将其替换为井号标签标题，如 `##`。</span><span class="sxs-lookup"><span data-stu-id="ad6d1-115">If an additional H1 is actually a double underline (`=======`), remove it or replace it with a hashtag heading, such as `##`, as appropriate.</span></span> <span data-ttu-id="ad6d1-116">如果双下划线属于合并冲突，请确保同时删除合并冲突的开始和结束标记及已过时的文本。</span><span class="sxs-lookup"><span data-stu-id="ad6d1-116">If the double underline is part of a merge conflict, make sure to also remove the merge conflict beginning and ending markers and the obsolete text.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
