---
title: multiple-values
description: 有关 Docs 生成问题 multiple-values 的解释和解决办法
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/19/2019
ms.prod: non-product-specific
ms.openlocfilehash: 8cee25b07e5bd1e019f8d270888eff73292d8e7c
ms.sourcegitcommit: ae71ca811c143deb6214147c7eea8704444a6093
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/21/2019
ms.locfileid: "56465107"
---
# <a name="multiple-values"></a><span data-ttu-id="2dd7f-103">multiple-values</span><span class="sxs-lookup"><span data-stu-id="2dd7f-103">multiple-values</span></span>

<span data-ttu-id="2dd7f-104">**即将推出！**</span><span class="sxs-lookup"><span data-stu-id="2dd7f-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="2dd7f-105">建议</span><span class="sxs-lookup"><span data-stu-id="2dd7f-105">Suggestion</span></span>

`Single-valued attribute {attribute} has multiple values. Remove additional values.`

<span data-ttu-id="2dd7f-106">为只允许一个值的属性指定了多个值。</span><span class="sxs-lookup"><span data-stu-id="2dd7f-106">You specified more than one value for an attribute that is ony allowed one value.</span></span>

`Single-valued attribute {attribute} is in multi-valued array format. Change to scalar format.`

<span data-ttu-id="2dd7f-107">必须以单值（标量）YML 格式指定不允许有多个值的属性。</span><span class="sxs-lookup"><span data-stu-id="2dd7f-107">Attributes that aren't allowed to have more than one value must be specified in the single-valued (scalar) YML format.</span></span>

## <a name="resolution"></a><span data-ttu-id="2dd7f-108">解决方法</span><span class="sxs-lookup"><span data-stu-id="2dd7f-108">Resolution</span></span>

<span data-ttu-id="2dd7f-109">只要多值数组用于单值属性，无论数组中有多个值还是一个值，都会收到此建议。</span><span class="sxs-lookup"><span data-stu-id="2dd7f-109">You get this Suggestion any time a multi-valued array is used for a single-valued attribute, either with multiple values or a single value in the array.</span></span>

<span data-ttu-id="2dd7f-110">YML 支持以下多值属性（如 `ms.custom`）数组格式：</span><span class="sxs-lookup"><span data-stu-id="2dd7f-110">YML supports the following array formats for multi-valued attributes, such as `ms.custom`:</span></span>

```yml
---
# comma-separated bracketed list:
ms.custom: [WIP, generated-via-CI]

# each value on its own line:
ms.custom:
  - WIP
  - generated-via-CI
---
```

<span data-ttu-id="2dd7f-111">这些格式对单值属性（如 `author`）无效。</span><span class="sxs-lookup"><span data-stu-id="2dd7f-111">These formats aren't valid for single-valued attributes, such as `author`.</span></span>

<span data-ttu-id="2dd7f-112">如果指定了多个值，请检查指定的值，并确定哪个是正确的。</span><span class="sxs-lookup"><span data-stu-id="2dd7f-112">If you specified multiple values, review the specified values and determine which is correct.</span></span> <span data-ttu-id="2dd7f-113">删除其他值，并在同一行中指定一个不带括号的值作为属性，如下所示：</span><span class="sxs-lookup"><span data-stu-id="2dd7f-113">Remove other values and specify the single value on the same line as the attribute with no brackets, as follows:</span></span>

```yml
---
author: meganbradley
---
```

<span data-ttu-id="2dd7f-114">如果有单值数组，请将它更改为上面的标量格式。</span><span class="sxs-lookup"><span data-stu-id="2dd7f-114">If you have a single-valued array, change it to the scalar format above.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
