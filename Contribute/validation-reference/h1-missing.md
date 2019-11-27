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
# <a name="h1-missing"></a>h1-missing

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>建议

`H1 is required. Use a single hash (#) followed by a space to create your top-level heading.`

H1 是指 Markdown 文件中的第一个标题。 发布到 docs.microsoft.com 时，H1 以大字体显示在页面顶部。 H1 的创建方式为，以包含一个井号 (#) 的行开头，后跟空格，然后是标题文本。

## <a name="resolution"></a>解决方法

若要解决此问题，请将 H1 添加为文件中 YML 元数据块后的第一项内容：

```markdown
---
author: meganbradley
ms.author: mbradley
---
# This is an H1
```

> [!NOTE]
> 此规则不适用于包含的文件。 如果在包含的文件中收到 H1 结果，则很可能需要将包含的文件移动到 `includes` 文件夹。 `includes` 文件夹可以是文件路径中的任何级别。 根据路径，Docs 生成会将该文件识别为包含文件，并且不会运行 H1 验证。
>
> 父文件中缺少 H1 的常见原因是误用了包含的文件：H1 在包含的文件中，而不在父文件中。 不允许这样做，因为在包含的文件中使用 H1 要么意味着父文件中存在重复的 H1，要么包含的文件仅使用了一次。 H1 在内容集中应唯一，并且包含的文件仅应用于在多个文件之间共享内容。 如果由于 H1 在包含的文件中而获得 `h1-missing` 结果，则解决方案是将 H1 和所有包含的内容（如果包含的文件仅使用一次）移动到父文件中。 有关 Docs 中包含的文件的详细信息，请参阅 Microsoft 内部文章[在文章中包含可重用的内容](https://review.docs.microsoft.com/en-us/help/contribute/includes-best-practices?branch=master)。

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
