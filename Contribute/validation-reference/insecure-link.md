---
title: insecure-link
description: 有关 Docs 生成问题 insecure-link 的解释和解决方法
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 10/1/2019
ms.prod: non-product-specific
ms.openlocfilehash: b97d4c4a0f61e5f3448331a56fe4bde442ff1cca
ms.sourcegitcommit: 0cb0177c209abab1a72af4f411ef527fa5cf10f9
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/16/2019
ms.locfileid: "72379508"
---
# <a name="insecure-link"></a>insecure-link

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

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
