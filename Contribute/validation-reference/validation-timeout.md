---
title: validation-timeout
description: 有关 Docs 生成问题 validation-timeout 的解释和解决方法
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 6/5/2019
ms.prod: non-product-specific
ms.openlocfilehash: f75f005ce9ab0cf332667d5c8b7778ba4ef35a0a
ms.sourcegitcommit: 254c804bb0b451c262745fe8d87e2e8f9196440c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/05/2019
ms.locfileid: "73592539"
---
# <a name="validation-timeout"></a><span data-ttu-id="31b1d-103">validation-timeout</span><span class="sxs-lookup"><span data-stu-id="31b1d-103">validation-timeout</span></span>

## <a name="warning"></a><span data-ttu-id="31b1d-104">警告</span><span class="sxs-lookup"><span data-stu-id="31b1d-104">Warning</span></span>

`The call to the validation service timed out and validation was not completed. This happens when there's an issue with the service and continuing to retry the call could cause build delays. You might have content issues that were not reported. To retry validation, close and re-open your PR, or force a full build of your branch via https://ops.microsoft.com. Note that forcing a full build requires admin permissions to the repo. If you don’t know who your repo admin is, or if you continue to see this message after a forced build, file an issue via https://SiteHelp.`

<span data-ttu-id="31b1d-105">有时，验证服务中的暂时性问题（例如，服务器处于错误状态）会阻止 Docs 生成成功调用该服务。</span><span class="sxs-lookup"><span data-stu-id="31b1d-105">Sometimes transient issues in the validation service, such as a server in a bad state, prevent Docs Build from successfully calling the service.</span></span> <span data-ttu-id="31b1d-106">多次尝试后，调用超时并取消验证，以避免生成延迟和阻塞生成管道。</span><span class="sxs-lookup"><span data-stu-id="31b1d-106">After several tries, the call times out and validation is canceled to avoid build delays and clogging the build pipeline.</span></span>

## <a name="resolution"></a><span data-ttu-id="31b1d-107">解决方法</span><span class="sxs-lookup"><span data-stu-id="31b1d-107">Resolution</span></span>

<span data-ttu-id="31b1d-108">请尝试关闭再重新打开 PR，或者通过 [Docs 门户](https://ops.microsoft.com/#/)强制进行完全生成。</span><span class="sxs-lookup"><span data-stu-id="31b1d-108">Try closing and re-opening your PR, or forcing a full build via [Docs Portal](https://ops.microsoft.com/#/).</span></span> <span data-ttu-id="31b1d-109">通常会在初始重试后清理服务问题本身。</span><span class="sxs-lookup"><span data-stu-id="31b1d-109">Often service issues clear themselves up after the initial retry.</span></span>

<span data-ttu-id="31b1d-110">请注意，只有存储库管理员才可通过 Docs 门户强制进行生成。</span><span class="sxs-lookup"><span data-stu-id="31b1d-110">Note that you must be a repo admin to force a build via Docs Portal.</span></span> <span data-ttu-id="31b1d-111">如果你不知道谁是存储库管理员，或者你在强制生成后仍然收到此消息，则请通过 [https://SiteHelp](https://SiteHelp) 提出问题（针对 Microsoft 员工），或者在 PR 中通过 @ 提及文章作者来获取帮助（针对外部参与者）。</span><span class="sxs-lookup"><span data-stu-id="31b1d-111">If you don't know who your repo admin is, or if you continue to get this message after a forced build, file an issue via [https://SiteHelp](https://SiteHelp) if you're a Microsoft employee, or @ mention the author of an article in your PR for assistance if you're an external contributor.</span></span>

<span data-ttu-id="31b1d-112">如果你是存储库管理员，则可如下强制进行完全生成：</span><span class="sxs-lookup"><span data-stu-id="31b1d-112">If you're a repo admin, you can force a full build as follows:</span></span>

1. <span data-ttu-id="31b1d-113">转到 [Docs 门户](https://ops.microsoft.com/#/)并登录。</span><span class="sxs-lookup"><span data-stu-id="31b1d-113">Go to [Docs Portal](https://ops.microsoft.com/#/) and sign in.</span></span>
1. <span data-ttu-id="31b1d-114">在左上角搜索找到你的存储库，然后选中它。</span><span class="sxs-lookup"><span data-stu-id="31b1d-114">Find your repo by searching in the upper left corner, and select it.</span></span>

   <span data-ttu-id="31b1d-115">:::image type="content" source="media/find-repo.png" alt-text="通过“Docs 门户”搜索框查找你的存储库":::</span><span class="sxs-lookup"><span data-stu-id="31b1d-115">:::image type="content" source="media/find-repo.png" alt-text="find your repo via the Docs Portal search box":::</span></span>
1. <span data-ttu-id="31b1d-116">在“生成历史记录”选项卡中，单击“+手动发布”。</span><span class="sxs-lookup"><span data-stu-id="31b1d-116">On the **Build History** tab, click **+ Manual Publish**.</span></span>
1. <span data-ttu-id="31b1d-117">选择收到警告的分支，例如主分支。</span><span class="sxs-lookup"><span data-stu-id="31b1d-117">Select the branch that's getting the Warning, such as master.</span></span>
1. <span data-ttu-id="31b1d-118">对于目标，请保留默认设置，即“Docs 网站”。</span><span class="sxs-lookup"><span data-stu-id="31b1d-118">For target, keep the default, **Docs Site**.</span></span>
1. <span data-ttu-id="31b1d-119">选中“强制发布”复选框。</span><span class="sxs-lookup"><span data-stu-id="31b1d-119">Check the **Force Publish** checkbox.</span></span>
1. <span data-ttu-id="31b1d-120">单击“发布”。</span><span class="sxs-lookup"><span data-stu-id="31b1d-120">Click **Publish**.</span></span>

   <span data-ttu-id="31b1d-121">:::image type="content" source="media/force-build.png" alt-text="强制完全生成的步骤":::</span><span class="sxs-lookup"><span data-stu-id="31b1d-121">:::image type="content" source="media/force-build.png" alt-text="steps to force a full build":::</span></span>

<span data-ttu-id="31b1d-122">这将在分支上强制进行完全生成。</span><span class="sxs-lookup"><span data-stu-id="31b1d-122">This will force a full build on the branch.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
