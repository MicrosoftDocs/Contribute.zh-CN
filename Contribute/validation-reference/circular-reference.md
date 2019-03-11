---
title: circular-reference
description: 有关 Docs 生成问题 circular-reference 的解释和解决方法
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/26/2019
ms.prod: non-product-specific
ms.openlocfilehash: 4600465cf940efa82c61bcbac4a1d912c16e6903
ms.sourcegitcommit: 89eb357721b26710e00d9b8fdab3e7628c34bdb6
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/06/2019
ms.locfileid: "57459202"
---
# <a name="circular-reference"></a>circular-reference

## <a name="error"></a>错误

`Files '{file name 1}' and '{file name 2}' reference each other.`

例如，这可能是链接到当前文件的包含文件，也可能是指向已重定向到当前文件的文件的链接。

## <a name="resolution"></a>解决方法

查看文件中的链接并进行必要的编辑，确保没有文件链接到或包含自身。

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
