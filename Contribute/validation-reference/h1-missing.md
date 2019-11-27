---
title: h1-missing
description: 有关 Docs 生成问题 issue h1-missing 的解释和解决方法。
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 11/25/2019
ms.prod: non-product-specific
ms.openlocfilehash: 1ff29a06b5a8d53d0152329807acc416463f4fe2
ms.sourcegitcommit: 423d9b8145a11426c91f45510b2d77319838eb27
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2019
ms.locfileid: "74528861"
---
# <a name="h1-missing"></a><span data-ttu-id="b920a-103">h1-missing</span><span class="sxs-lookup"><span data-stu-id="b920a-103">h1-missing</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="b920a-104">建议</span><span class="sxs-lookup"><span data-stu-id="b920a-104">Suggestion</span></span>

`H1 is required. Use a single hash (#) followed by a space to create your top-level heading.`

<span data-ttu-id="b920a-105">H1 是指 Markdown 文件中的第一个标题。</span><span class="sxs-lookup"><span data-stu-id="b920a-105">H1 refers to the first heading in a Markdown file.</span></span> <span data-ttu-id="b920a-106">发布到 docs.microsoft.com 时，H1 以大字体显示在页面顶部。</span><span class="sxs-lookup"><span data-stu-id="b920a-106">When published to docs.microsoft.com, the H1 shows at the top of the page in a large font.</span></span> <span data-ttu-id="b920a-107">H1 的创建方式为，以包含一个井号 (#) 的行开头，后跟空格，然后是标题文本。</span><span class="sxs-lookup"><span data-stu-id="b920a-107">An H1 is created by beginning a line with a single hash (#) followed by a space, then the heading text.</span></span>

## <a name="resolution"></a><span data-ttu-id="b920a-108">解决方法</span><span class="sxs-lookup"><span data-stu-id="b920a-108">Resolution</span></span>

<span data-ttu-id="b920a-109">若要解决此问题，请将 H1 添加为文件中 YML 元数据块后的第一项内容：</span><span class="sxs-lookup"><span data-stu-id="b920a-109">To fix this issue, add an H1 as the first content after the YML metadata block in your file:</span></span>

```markdown
---
author: meganbradley
ms.author: mbradley
---
# This is an H1
```

> [!NOTE]
> <span data-ttu-id="b920a-110">此规则不适用于包含的文件。</span><span class="sxs-lookup"><span data-stu-id="b920a-110">This rule does not apply to included files.</span></span> <span data-ttu-id="b920a-111">如果在包含的文件中收到 H1 结果，则很可能需要将包含的文件移动到 `includes` 文件夹。</span><span class="sxs-lookup"><span data-stu-id="b920a-111">If you get H1 results on included files, you most likely need to move your included files into an `includes` folder.</span></span> <span data-ttu-id="b920a-112">`includes` 文件夹可以是文件路径中的任何级别。</span><span class="sxs-lookup"><span data-stu-id="b920a-112">The `includes` folder can be at any level in the file path.</span></span> <span data-ttu-id="b920a-113">根据路径，Docs 生成会将该文件识别为包含文件，并且不会运行 H1 验证。</span><span class="sxs-lookup"><span data-stu-id="b920a-113">Based on the path, Docs build will recognize the file as an included file and H1 validations won't run.</span></span>
>
> <span data-ttu-id="b920a-114">父文件中缺少 H1 的常见原因是误用了包含的文件：H1 在包含的文件中，而不在父文件中。</span><span class="sxs-lookup"><span data-stu-id="b920a-114">A common cause of missing H1s in parent files is misuse of included files: the H1 is in the included file, not in the parent file.</span></span> <span data-ttu-id="b920a-115">不允许这样做，因为在包含的文件中使用 H1 要么意味着父文件中存在重复的 H1，要么包含的文件仅使用了一次。</span><span class="sxs-lookup"><span data-stu-id="b920a-115">This isn't allowed, because using an H1 in an included file either means there are duplicate H1s in parent files or the included file is used only once.</span></span> <span data-ttu-id="b920a-116">H1 在内容集中应唯一，并且包含的文件仅应用于在多个文件之间共享内容。</span><span class="sxs-lookup"><span data-stu-id="b920a-116">H1s should be unique within a content set and included files should only be used to share content among multiple files.</span></span> <span data-ttu-id="b920a-117">如果由于 H1 在包含的文件中而获得 `h1-missing` 结果，则解决方案是将 H1 和所有包含的内容（如果包含的文件仅使用一次）移动到父文件中。</span><span class="sxs-lookup"><span data-stu-id="b920a-117">If you get `h1-missing` results because the H1 is in an included file, the solution is to move the H1 - and all the included content if the included file is used only once - into the parent file.</span></span> <span data-ttu-id="b920a-118">有关 Docs 中包含的文件的详细信息，请参阅 Microsoft 内部文章[在文章中包含可重用的内容](https://review.docs.microsoft.com/en-us/help/contribute/includes-best-practices?branch=master)。</span><span class="sxs-lookup"><span data-stu-id="b920a-118">For more information about included files in Docs, see the Microsoft-internal article [Include reusable content in articles](https://review.docs.microsoft.com/en-us/help/contribute/includes-best-practices?branch=master).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
