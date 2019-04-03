---
author: meganbradley
ms.author: mbradley
ms.date: 03/29/2019
ms.openlocfilehash: a3b383021046412620c616882b19cb06f4dc59f8
ms.sourcegitcommit: af37d44eb67daa2841959817cd205ec95db18cec
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/29/2019
ms.locfileid: "58653542"
---
# <a name="locale-specific-links"></a>特定于区域设置的链接

区域设置代码（例如 `en-us`）不应包含在指向某些 Microsoft 站点的链接中。 如果在英语内容的链接中包含区域设置代码，它也将包含在本地化链接中，这会导致糟糕的本地化体验。 例如，如果德语本地化内容中的链接包含 `en-us`，则德语客户会发现即使有德语版本，自己也被链接到了英文文章。

从 Microsoft 站点的链接中删除区域设置代码。 下面是一个示例。

之前：

`https://docs.microsoft.com/en-us/vsts/load-test/app-service-web-app-performance-test`

之后：

`https://docs.microsoft.com/vsts/load-test/app-service-web-app-performance-test`

以下站点适用于此验证：

- azure.microsoft.com
- docs.microsoft.com
- msdn.microsoft.com
- technet.microsoft.com