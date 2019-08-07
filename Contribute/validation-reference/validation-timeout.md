---
title: validation-timeout
description: 有关 Docs 生成问题 validation-timeout 的解释和解决方法
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 6/5/2019
ms.prod: non-product-specific
ms.openlocfilehash: bb58c472371c429002cf5b35b7d6157ffb28b5cd
ms.sourcegitcommit: 495d49f10df51a8897687940aa653e906c48c2a0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/06/2019
ms.locfileid: "68817415"
---
# <a name="validation-timeout"></a><span data-ttu-id="a5fcf-103">validation-timeout</span><span class="sxs-lookup"><span data-stu-id="a5fcf-103">validation-timeout</span></span>

## <a name="warning"></a><span data-ttu-id="a5fcf-104">警告</span><span class="sxs-lookup"><span data-stu-id="a5fcf-104">Warning</span></span>

`The call to the validation service timed out and validation was not completed. This happens when there's an issue with the service and continuing to retry the call could cause build delays. You might have content issues that were not reported. To retry validation, close and re-open your PR, or rebuild your branch via Docs Portal (requires admin permissions). If you need admin help or if you continue to see this message, file an issue via https://SiteHelp.`

<span data-ttu-id="a5fcf-105">有时，验证服务中的暂时性问题（例如，服务器处于错误状态）会阻止 Docs 生成成功调用该服务。</span><span class="sxs-lookup"><span data-stu-id="a5fcf-105">Sometimes transient issues in the validation service, such as a server in a bad state, prevent Docs Build from successfully calling the service.</span></span> <span data-ttu-id="a5fcf-106">多次尝试后，调用超时并取消验证，以避免生成延迟和阻塞生成管道。</span><span class="sxs-lookup"><span data-stu-id="a5fcf-106">After several tries, the call times out and validation is canceled to avoid build delays and clogging the build pipeline.</span></span>

## <a name="resolution"></a><span data-ttu-id="a5fcf-107">解决方法</span><span class="sxs-lookup"><span data-stu-id="a5fcf-107">Resolution</span></span>

<span data-ttu-id="a5fcf-108">请尝试关闭再重新打开拉取请求 (PR)，或通过 Docs 门户重新运行手动生成（仅限存储库管理员）。</span><span class="sxs-lookup"><span data-stu-id="a5fcf-108">Try closing and re-opening your PR, or re-running a manual build via Docs Portal (repo admins only).</span></span> <span data-ttu-id="a5fcf-109">通常会在初始重试后清理服务问题本身。</span><span class="sxs-lookup"><span data-stu-id="a5fcf-109">Often service issues clear themselves up after the initial retry.</span></span> <span data-ttu-id="a5fcf-110">如需管理员提供帮助或者仍然收到此消息，请通过 [https://SiteHelp](https://SiteHelp) 提出问题（针对 Microsoft 员工），或者在 PR 中通过 @ 提及文章作者来获取帮助（针对外部参与者）。</span><span class="sxs-lookup"><span data-stu-id="a5fcf-110">If you need help from an admin or if you continue to get this message, file an issue via [https://SiteHelp](https://SiteHelp) if you're a Microsoft employee, or @ mention the author of an article in your PR for assistance if you're an external contributor.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
