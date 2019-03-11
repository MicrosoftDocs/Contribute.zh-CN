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
# <a name="snippet-not-found"></a>snippet-not-found

## <a name="warning"></a>警告

`Code snippet '{snippet path}' not found.`

指定的路径不存在代码片段引用，或者该路径在当前文件中不可用。

## <a name="resolution"></a>解决方法

[!INCLUDE [docs-authoring-pack](includes/docs-authoring-pack.md)]

确保片段路径正确。 如果片段存储在当前存储库之外，请确保存储库配置为依赖存储库。 有关更多信息，请参阅 Microsoft 内部[代码片段文章](https://review.docs.microsoft.com/en-us/help/contribute/code-in-docs?branch=master)。

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
