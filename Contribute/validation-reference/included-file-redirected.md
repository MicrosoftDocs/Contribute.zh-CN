---
title: included-file-redirected
description: 有关 Docs 生成问题 included-file-redirected 的解释和解决方法
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 3/1/2019
ms.prod: non-product-specific
ms.openlocfilehash: 8a40f04fe1a7e7f19ab9ee7ce684684184aa4dc7
ms.sourcegitcommit: 89eb357721b26710e00d9b8fdab3e7628c34bdb6
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/06/2019
ms.locfileid: "57459064"
---
# <a name="included-file-redirected"></a><span data-ttu-id="54200-103">included-file-redirected</span><span class="sxs-lookup"><span data-stu-id="54200-103">included-file-redirected</span></span>

## <a name="warning"></a><span data-ttu-id="54200-104">警告</span><span class="sxs-lookup"><span data-stu-id="54200-104">Warning</span></span>

`Included file '{include path}' is redirected to '{target file path}'. Only include files that are not redirected and that are located in an includes folder.`

## <a name="resolution"></a><span data-ttu-id="54200-105">解决方法</span><span class="sxs-lookup"><span data-stu-id="54200-105">Resolution</span></span>

<span data-ttu-id="54200-106">重构内容，确保不包含重定向的文件。</span><span class="sxs-lookup"><span data-stu-id="54200-106">Restructure your content so you aren't including a redirected file.</span></span> <span data-ttu-id="54200-107">例如，创建一个新文件以包含或删除包含的引用并链接到内容或将其写入内联。</span><span class="sxs-lookup"><span data-stu-id="54200-107">For example, create a new file to include or remove the included reference and link to content or write it inline.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
