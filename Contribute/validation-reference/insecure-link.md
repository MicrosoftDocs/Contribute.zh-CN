---
title: insecure-link
description: 有关 Docs 生成问题 insecure-link 的解释和解决方法
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 10/1/2019
ms.prod: non-product-specific
ms.openlocfilehash: c22404e624ae85369d7b0b95f44e37d51f847368
ms.sourcegitcommit: ab31cbb17c64a06cab4ffb37b157fd812417a499
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/18/2019
ms.locfileid: "72587681"
---
# <a name="insecure-link"></a>insecure-link

> [!IMPORTANT]
> 此规则最初作为“建议”启用，以便内容团队有时间衡量影响并制定清理其存储库的计划。 **它将于 2019 年 12 月 20 日提升为“警告”** 。

## <a name="suggestion"></a>建议

`Link '{URL}' is insecure. Links to Microsoft sites must use 'https' instead of 'http'.`

此消息表示你使用的是具有 `http` 的显式 Markdown 链接，或者使用原始 URL，如 `www.microsoft.com`。 原始 URL 在发布到 Docs 时会转换为不安全的链接，因此不应使用。

## <a name="resolution"></a>解决方法

应将所有 URL 更改为使用 `https` 而非 `http` 的 Microsoft 网站。

如果链接是原始 URL，请将其更改为以 `https` 开头的显式 Markdown 链接。

> [!TIP]
> 适用于 VS Code 的 Docs Markdown 扩展包括 Microsoft 链接的清理脚本。 脚本会检查存储库中所有指向 Microsoft 网站的链接，确保它们以 `https` 而非 `http` 开头，并且不包含区域设置代码，如 `en-us`。 要运行脚本，请执行以下操作：
>
> 1. 安装适用于 VS Code 的 [Docs Markdown](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown) 扩展。
> 1. 单击 Alt+M，打开“Markdown”菜单。
> 1. 选择“清理”，然后选择“Microsoft 链接”   。

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
