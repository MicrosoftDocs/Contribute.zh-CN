---
title: h1-missing
description: 有关 Docs 生成问题 issue h1-missing 的解释和解决方法。
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: c920cc0f12a9fac41b640957d45452a7958d4b07
ms.sourcegitcommit: 89eb357721b26710e00d9b8fdab3e7628c34bdb6
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/06/2019
ms.locfileid: "57459110"
---
# <a name="h1-missing"></a><span data-ttu-id="3925b-103">h1-missing</span><span class="sxs-lookup"><span data-stu-id="3925b-103">h1-missing</span></span>

## <a name="warning"></a><span data-ttu-id="3925b-104">警告</span><span class="sxs-lookup"><span data-stu-id="3925b-104">Warning</span></span>

`H1 is required. Use a single hash (#) followed by a space to create your top-level heading.`

<span data-ttu-id="3925b-105">H1 是指 Markdown 文件中的第一个标题。</span><span class="sxs-lookup"><span data-stu-id="3925b-105">H1 refers to the first heading in a Markdown file.</span></span> <span data-ttu-id="3925b-106">发布到 docs.microsoft.com 时，H1 以大字体显示在页面顶部。</span><span class="sxs-lookup"><span data-stu-id="3925b-106">When published to docs.microsoft.com, the H1 shows at the top of the page in a large font.</span></span> <span data-ttu-id="3925b-107">H1 的创建方式为，以包含一个井号 (#) 的行开头，后跟空格，然后是标题文本。</span><span class="sxs-lookup"><span data-stu-id="3925b-107">An H1 is created by beginning a line with a single hash (#) followed by a space, then the heading text.</span></span>

## <a name="resolution"></a><span data-ttu-id="3925b-108">解决方法</span><span class="sxs-lookup"><span data-stu-id="3925b-108">Resolution</span></span>

<span data-ttu-id="3925b-109">若要解决此问题，请将 H1 添加为文件中 YML 元数据块后的第一项内容：</span><span class="sxs-lookup"><span data-stu-id="3925b-109">To fix this issue, add an H1 as the first content after the YML metadata block in your file:</span></span>

```markdown
---
author: meganbradley
ms.author: mbradley
---
# This is an H1
```

> [!NOTE]
> <span data-ttu-id="3925b-110">此规则不适用于包含的文件。</span><span class="sxs-lookup"><span data-stu-id="3925b-110">This rule does not apply to included files.</span></span> <span data-ttu-id="3925b-111">如果在包含的文件中收到 H1 警告，则很可能需要将包含的文件移动到 `includes` 文件夹。</span><span class="sxs-lookup"><span data-stu-id="3925b-111">If you get H1 warnings on included files, you most likely need to move your included files into an `includes` folder.</span></span> <span data-ttu-id="3925b-112">`includes` 文件夹可以是文件路径中的任何级别。</span><span class="sxs-lookup"><span data-stu-id="3925b-112">The `includes` folder can be at any level in the file path.</span></span> <span data-ttu-id="3925b-113">根据路径，Docs 生成会将该文件识别为包含文件，并且不会运行 H1 验证。</span><span class="sxs-lookup"><span data-stu-id="3925b-113">Based on the path, Docs build will recognize the file as an included file and H1 validations won't run.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]