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
# <a name="validation-timeout"></a><span data-ttu-id="862d9-103">validation-timeout</span><span class="sxs-lookup"><span data-stu-id="862d9-103">validation-timeout</span></span>

## <a name="warning"></a><span data-ttu-id="862d9-104">警告</span><span class="sxs-lookup"><span data-stu-id="862d9-104">Warning</span></span>

`The call to the validation service timed out and validation was not completed. This happens when there's an issue with the service and continuing to retry the call could cause build delays. You might have content issues that were not reported. To retry validation, close and open your PR. If you continue to see this message, file an issue via https://SiteHelp.`

<span data-ttu-id="862d9-105">有时，验证服务中的暂时性问题（例如，服务器处于错误状态）会阻止 Docs 生成成功调用该服务。</span><span class="sxs-lookup"><span data-stu-id="862d9-105">Sometimes transient issues in the validation service, such as a server in a bad state, prevent Docs Build from successfully calling the service.</span></span> <span data-ttu-id="862d9-106">尝试三次之后，调用超时并取消验证，以避免生成延迟和阻塞生成管道。</span><span class="sxs-lookup"><span data-stu-id="862d9-106">After three tries, the call times out and validation is canceled to avoid build delays and clogging the build pipeline.</span></span>

## <a name="resolution"></a><span data-ttu-id="862d9-107">解决方法</span><span class="sxs-lookup"><span data-stu-id="862d9-107">Resolution</span></span>

<span data-ttu-id="862d9-108">尝试关闭并重新打开你的 PR，或重新运行手动生成（仅限存储库管理员）。</span><span class="sxs-lookup"><span data-stu-id="862d9-108">Try closing and reopening your PR, or re-running a manual build (repo admins only).</span></span> <span data-ttu-id="862d9-109">通常会在初始重试后清理服务问题本身。</span><span class="sxs-lookup"><span data-stu-id="862d9-109">Often service issues clear themselves up after the initial retry.</span></span> <span data-ttu-id="862d9-110">如果仍收到消息，Microsoft 员工请通过 [https://SiteHelp](https://SiteHelp) 提出问题，外部参与者在 PR 中 @ 提及文章的作者以获取帮助。</span><span class="sxs-lookup"><span data-stu-id="862d9-110">If you continue to get the message, file an issue via [https://SiteHelp](https://SiteHelp) if you're a Microsoft employee, or @ mention the author of an article in your PR for assistance if you're an external contributor.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
