---
title: validation-timeout
description: 有关 Docs 生成问题 validation-timeout 的解释和解决方法
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 6/5/2019
ms.prod: non-product-specific
ms.openlocfilehash: 018634b1c5fba0848fb36a70d81c46be9acf2ecd
ms.sourcegitcommit: 1e53d17639277bebd89b2e7cabeb45bdad526354
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/12/2019
ms.locfileid: "67024201"
---
# <a name="validation-timeout"></a>validation-timeout

## <a name="warning"></a>警告

`The call to the validation service timed out and validation was not completed. This happens when there's an issue with the service and continuing to retry the call could cause build delays. You might have content issues that were not reported. To retry validation, close and open your PR. If you continue to see this message, file an issue via https://SiteHelp.`

有时，验证服务中的暂时性问题（例如，服务器处于错误状态）会阻止 Docs 生成成功调用该服务。 尝试三次之后，调用超时并取消验证，以避免生成延迟和阻塞生成管道。

## <a name="resolution"></a>解决方法

尝试关闭并重新打开你的 PR，或重新运行手动生成（仅限存储库管理员）。 通常会在初始重试后清理服务问题本身。 如果仍收到消息，Microsoft 员工请通过 [https://SiteHelp](https://SiteHelp) 提出问题，外部参与者在 PR 中 @ 提及文章的作者以获取帮助。

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
