---
title: hard-coded-locale
description: 有关 Docs 生成问题 hard-coded-locale 的解释和解决方法。
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 10/18/2019
ms.prod: non-product-specific
ms.openlocfilehash: 1ab511398cbd622906ccb0a67e2b24968ee29374
ms.sourcegitcommit: 55624c641bea5367bcfa08655c085bc950e8beae
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/30/2019
ms.locfileid: "73166825"
---
# <a name="hard-coded-locale"></a>hard-coded-locale

> [!IMPORTANT]
> 此规则最初作为“建议”启用，以便内容团队有时间衡量影响并制定清理其存储库的计划。 **它将于 2019 年 12 月 20 日提升为“警告”** 。

## <a name="suggestion"></a>建议

`Link '{URL}' contains locale code '{code}'. For localizability, remove '{code}' from links to most Microsoft sites.`

区域设置代码（例如 `en-us`）不应包含在指向某些 Microsoft 站点的链接中。 如果在英语内容的链接中包含区域设置代码，它也将包含在本地化链接中，这会导致糟糕的本地化体验。 例如，如果德语本地化内容中的链接包含 `en-us`，则德语客户会发现即使有德语版本，自己也被链接到了英文文章。

以下站点适用于此验证：

- azure.microsoft.com
- docs.microsoft.com
- msdn.microsoft.com（不包括 social.msdn.com，它需要区域设置来确保链接到正确的论坛）
- technet.microsoft.com

## <a name="resolution"></a>解决方法

从 Microsoft 站点的链接中删除区域设置代码。 下面是一个示例。

之前：

`https://docs.microsoft.com/en-us/vsts/load-test/app-service-web-app-performance-test`

之后：

`https://docs.microsoft.com/vsts/load-test/app-service-web-app-performance-test`

> [!TIP]
> 适用于 VS Code 的 Docs Markdown 扩展包括 Microsoft 链接的清理脚本。 脚本会检查存储库中所有指向 Microsoft 网站的链接，确保它们以 `https` 而非 `http` 开头，并且不包含区域设置代码，如 `en-us`。 要运行脚本，请执行以下操作：
>
> 1. 安装适用于 VS Code 的 [Docs Markdown](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown) 扩展。
> 1. 单击 Alt+M，打开“Markdown”菜单。
> 1. 选择“清理”，然后选择“Microsoft 链接”   。

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
