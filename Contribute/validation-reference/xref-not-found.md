---
title: xref-not-found
description: 有关 Docs 生成问题 xref-not-found 的解释和解决方法
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/26/2019
ms.prod: non-product-specific
ms.openlocfilehash: d51eace291bfac179be2701463d113c06627f92f
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/05/2019
ms.locfileid: "57427233"
---
# <a name="xref-not-found"></a>xref-not-found

## <a name="warning"></a>警告

`Cross reference not found: '<xref: {uid}>'.`

`Cross reference not found: '@{uid}'.`

链接到的 UID 不存在或者在存储库中不可用。

## <a name="resolution"></a>解决方法

根据 Microsoft 内部 [Xref 服务](https://review.docs.microsoft.com/en-us/help/onboard/admin/xref-service?branch=master)文档中所述，验证 UID 正确无误并且在存储库中正确配置了 Xref 服务。

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
