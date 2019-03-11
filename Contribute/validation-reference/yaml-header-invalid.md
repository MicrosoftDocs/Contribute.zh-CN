---
title: yaml-header-invalid
description: 有关 Docs 生成问题 yaml-header-invalid 的解释和解决方法
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/26/2019
ms.prod: non-product-specific
ms.openlocfilehash: 62b3b2c2aa47525cae5dd5c0955eb88463124359
ms.sourcegitcommit: 89eb357721b26710e00d9b8fdab3e7628c34bdb6
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/06/2019
ms.locfileid: "57459018"
---
# <a name="yaml-header-invalid"></a><span data-ttu-id="dc820-103">yaml-header-invalid</span><span class="sxs-lookup"><span data-stu-id="dc820-103">yaml-header-invalid</span></span>

## <a name="warning"></a><span data-ttu-id="dc820-104">警告</span><span class="sxs-lookup"><span data-stu-id="dc820-104">Warning</span></span>

`Invalid YAML header: Improper use of a colon in a metadata entry.`

<span data-ttu-id="dc820-105">这通常意味着 YAML 标头中未加引号的元数据值包含冒号或其他特殊字符。</span><span class="sxs-lookup"><span data-stu-id="dc820-105">Usually this means an unquoted metadata value in a YAML header includes a colon or another special character.</span></span> <span data-ttu-id="dc820-106">它还可能意味着键/值对中的冒号后缺少空格。</span><span class="sxs-lookup"><span data-stu-id="dc820-106">It can also mean that a space is missing after the colon in a key/value pair.</span></span>

## <a name="resolution"></a><span data-ttu-id="dc820-107">解决方法</span><span class="sxs-lookup"><span data-stu-id="dc820-107">Resolution</span></span>

<span data-ttu-id="dc820-108">审阅 YAML 标头。</span><span class="sxs-lookup"><span data-stu-id="dc820-108">Review your YAML header.</span></span> <span data-ttu-id="dc820-109">查找以下错误。</span><span class="sxs-lookup"><span data-stu-id="dc820-109">Look for the following mistakes.</span></span>

<span data-ttu-id="dc820-110">未加引号的值中的冒号：</span><span class="sxs-lookup"><span data-stu-id="dc820-110">Colon in unquoted value:</span></span>

```yml
---
title: Common mistake: I included a colon in my unquoted value.
---
```

<span data-ttu-id="dc820-111">更改为：</span><span class="sxs-lookup"><span data-stu-id="dc820-111">Change to:</span></span>

```yml
---
title: 'Common mistake: I included a colon in my unquoted value.'
---
```

<span data-ttu-id="dc820-112">键/值对中的冒号后没有空格：</span><span class="sxs-lookup"><span data-stu-id="dc820-112">No space after colon in key/value pair:</span></span>

```yml
---
title:I omitted a space.
---
```

<span data-ttu-id="dc820-113">更改为：</span><span class="sxs-lookup"><span data-stu-id="dc820-113">Change to:</span></span>

```yml
---
title: I omitted a space.
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
