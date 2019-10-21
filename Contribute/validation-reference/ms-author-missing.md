---
title: ms-author-missing
description: 有关 Docs 生成问题 ms-author-missing 的解释和解决方案
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/20/2018
ms.prod: non-product-specific
ms.openlocfilehash: 6b313bd6b168b913d82721607126fcd4e6255009
ms.sourcegitcommit: 57eb071bdc55ef71fa3f8ac979326c3f8fbe9c45
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/10/2019
ms.locfileid: "72246251"
---
# <a name="ms-author-missing"></a>ms-author-missing

## <a name="warning"></a>警告

`Missing attribute: ms.author. Add the current author's Microsoft alias.`

## <a name="resolution"></a>解决方法

对于 `ms.author`，添加当前作者的 Microsoft 别名。 注意，如果所有权发生变更，则应该是此文章的当前作者，而不是原作者  。 建议指定的作者为全职员工或团队通讯组列表 (DL)，而不是短期供应商。 

如果别名是 DL，还必须位于 `ms.author` 允许列表中。

可以在 [Microsoft 内部网站](https://docsmetadatatool.azurewebsites.net/allowlists)上找到 `ms.author` DL 的有效值。

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
