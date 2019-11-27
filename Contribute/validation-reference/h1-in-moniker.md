---
title: h1-in-moniker
description: 有关 Docs 生成问题 h1-in-moniker 的解释和解决方法。
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 11/25/2019
ms.prod: non-product-specific
ms.openlocfilehash: f22ce2c9e2a014e4d8bf0ae9b61fa48b11d8c9a1
ms.sourcegitcommit: 423d9b8145a11426c91f45510b2d77319838eb27
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2019
ms.locfileid: "74528835"
---
# <a name="h1-in-moniker"></a><span data-ttu-id="e1d62-103">h1-in-moniker</span><span class="sxs-lookup"><span data-stu-id="e1d62-103">h1-in-moniker</span></span>

## <a name="warning"></a><span data-ttu-id="e1d62-104">警告</span><span class="sxs-lookup"><span data-stu-id="e1d62-104">Warning</span></span>

`H1s are not allowed in moniker sections. Each article should have one and only one H1.`

<span data-ttu-id="e1d62-105">H1 是指 Markdown 文件中的第一个标题。</span><span class="sxs-lookup"><span data-stu-id="e1d62-105">H1 refers to the first heading in a Markdown file.</span></span> <span data-ttu-id="e1d62-106">发布到 docs.microsoft.com 时，H1 以大字体显示在页面顶部。</span><span class="sxs-lookup"><span data-stu-id="e1d62-106">When published to docs.microsoft.com, the H1 shows at the top of the page in a large font.</span></span> <span data-ttu-id="e1d62-107">H1 的创建方式为，以包含一个井号 (#) 的行开头，后跟空格，然后是标题文本。</span><span class="sxs-lookup"><span data-stu-id="e1d62-107">An H1 is created by beginning a line with a single hash (#) followed by a space, then the heading text.</span></span> <span data-ttu-id="e1d62-108">一个文件中只能有一个 H1。</span><span class="sxs-lookup"><span data-stu-id="e1d62-108">You can only have one H1 in each file.</span></span> <span data-ttu-id="e1d62-109">H1s 不允许用于名字对象部分，因为根据版本的配置，名字对象中的 H1s 易导致 H1s 重复或缺失。</span><span class="sxs-lookup"><span data-stu-id="e1d62-109">H1s aren't allowed in moniker sections, because H1s in monikers can easily cause duplicate or missing H1s depending on how versioning is configured.</span></span>

<span data-ttu-id="e1d62-110">如果名字对象部分包含一行等于号，形成双下划线（如 `=======`），也可能会收到此消息。</span><span class="sxs-lookup"><span data-stu-id="e1d62-110">You might also get this message if a moniker section contains a line of equals signs making a double underline, like this: `=======`.</span></span> <span data-ttu-id="e1d62-111">这是 H1 的替代 Markdown 语法。</span><span class="sxs-lookup"><span data-stu-id="e1d62-111">This is an alternative Markdown syntax for an H1.</span></span> <span data-ttu-id="e1d62-112">这种情况也通常出现在合并冲突中：</span><span class="sxs-lookup"><span data-stu-id="e1d62-112">It's also commonly seen in merge conflicts:</span></span>

```markdown
<<<<<<< HEAD
...
=======
...
>>>>>>> 1d82c7efe18f86136247fb366df5030843199c19
```

## <a name="resolution"></a><span data-ttu-id="e1d62-113">解决方法</span><span class="sxs-lookup"><span data-stu-id="e1d62-113">Resolution</span></span>

<span data-ttu-id="e1d62-114">要解决此问题，请删除所有名字对象部分中的 H1s，并确保文章顶部的 H1 适用于所有名字对象部分。</span><span class="sxs-lookup"><span data-stu-id="e1d62-114">To fix this issue, remove H1s from all moniker sections, and make sure the H1 at the top of the article is appropriate for all moniker sections.</span></span> <span data-ttu-id="e1d62-115">请注意，不允许跳过标题级别，如 H1 之后为 H3。</span><span class="sxs-lookup"><span data-stu-id="e1d62-115">Note that skipping heading levels, such as following H1 with H3, isn't allowed.</span></span>

<span data-ttu-id="e1d62-116">如果名字对象部分中的 H1 确实是双下划线 (`=======`)，请将其删除，或根据需要将其替换为井号标签标题，如 `##`。</span><span class="sxs-lookup"><span data-stu-id="e1d62-116">If an H1 in a moniker section is actually a double underline (`=======`), remove it or replace it with a hashtag heading, such as `##`, as appropriate.</span></span> <span data-ttu-id="e1d62-117">如果双下划线属于合并冲突，请确保同时删除合并冲突的开始和结束标记及已过时的文本。</span><span class="sxs-lookup"><span data-stu-id="e1d62-117">If the double underline is part of a merge conflict, make sure to also remove the merge conflict beginning and ending markers and the obsolete text.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
