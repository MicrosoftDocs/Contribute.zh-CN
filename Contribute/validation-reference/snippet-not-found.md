---
title: snippet-not-found
description: 有关 Docs 生成问题 snippet-not-found 的解释和解决方法
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/26/2019
ms.prod: non-product-specific
ms.openlocfilehash: 82fc2926f5bc2ec01577670b066b88fb59d7ea11
ms.sourcegitcommit: 89eb357721b26710e00d9b8fdab3e7628c34bdb6
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/06/2019
ms.locfileid: "57459087"
---
# <a name="snippet-not-found"></a><span data-ttu-id="c29ed-103">snippet-not-found</span><span class="sxs-lookup"><span data-stu-id="c29ed-103">snippet-not-found</span></span>

## <a name="warning"></a><span data-ttu-id="c29ed-104">警告</span><span class="sxs-lookup"><span data-stu-id="c29ed-104">Warning</span></span>

`Code snippet '{snippet path}' not found.`

<span data-ttu-id="c29ed-105">指定的路径不存在代码片段引用，或者该路径在当前文件中不可用。</span><span class="sxs-lookup"><span data-stu-id="c29ed-105">The code snippet references doesn't exist at the specified path, or the path isn't available from the current file.</span></span>

## <a name="resolution"></a><span data-ttu-id="c29ed-106">解决方法</span><span class="sxs-lookup"><span data-stu-id="c29ed-106">Resolution</span></span>

[!INCLUDE [docs-authoring-pack](includes/docs-authoring-pack.md)]

<span data-ttu-id="c29ed-107">确保片段路径正确。</span><span class="sxs-lookup"><span data-stu-id="c29ed-107">Ensure that your snippet path is correct.</span></span> <span data-ttu-id="c29ed-108">如果片段存储在当前存储库之外，请确保存储库配置为依赖存储库。</span><span class="sxs-lookup"><span data-stu-id="c29ed-108">If the snippet is stored outside the current repo, make sure the repo is configured ase a dependent repo.</span></span> <span data-ttu-id="c29ed-109">有关更多信息，请参阅 Microsoft 内部[代码片段文章](https://review.docs.microsoft.com/en-us/help/contribute/code-in-docs?branch=master)。</span><span class="sxs-lookup"><span data-stu-id="c29ed-109">For more information, see the Microsoft-internal [code snippet article](https://review.docs.microsoft.com/en-us/help/contribute/code-in-docs?branch=master).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
