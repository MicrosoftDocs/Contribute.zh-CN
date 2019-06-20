---
title: validation-timeout
description: 有关 Docs 生成问题 validation-timeout 的解释和解决方法
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 6/5/2019
ms.prod: non-product-specific
ms.openlocfilehash: 00461768491c25b9bafaff6b117a356d9e291e22
ms.sourcegitcommit: 412ce4ab23e758d41947043f1463e96595ba3bfe
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/12/2019
ms.locfileid: "67033289"
---
# <a name="validation-timeout"></a>validation-timeout

## <a name="warning"></a>警告

`The call to the validation service timed out and validation was not completed. This happens when there's an issue with the service and continuing to retry the call could cause build delays. You might have content issues that were not reported. To retry validation, close and re-open your PR, or rebuild your branch via Docs Portal (requires admin permissions). If you need admin help or  If you continue to see this message, file an issue via https://SiteHelp.`

有时，验证服务中的暂时性问题（例如，服务器处于错误状态）会阻止 Docs 生成成功调用该服务。 多次尝试后，调用超时并取消验证，以避免生成延迟和阻塞生成管道。

## <a name="resolution"></a>解决方法

请尝试关闭再重新打开拉取请求 (PR)，或通过 Docs 门户重新运行手动生成（仅限存储库管理员）。 通常会在初始重试后清理服务问题本身。 如需管理员提供帮助或者仍然收到此消息，请通过 [https://SiteHelp](https://SiteHelp) 提出问题（针对 Microsoft 员工），或者在 PR 中通过 @ 提及文章作者来获取帮助（针对外部参与者）。

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
