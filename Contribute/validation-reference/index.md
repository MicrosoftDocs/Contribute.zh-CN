---
author: meganbradley
ms.author: mbradley
ms.openlocfilehash: fa048980afcf3c50f7d990f9c88064df6ee5ebb5
ms.sourcegitcommit: 6f1997864c000a9cd25fb9171a8f8fdb8b5b5ece
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/11/2018
ms.locfileid: "49084439"
---
# <a name="docs-pr-validation-service"></a><span data-ttu-id="6abfe-101">Docs PR 验证服务</span><span class="sxs-lookup"><span data-stu-id="6abfe-101">Docs PR validation service</span></span>

<span data-ttu-id="6abfe-102">Docs PR 验证服务是一个 GitHub 应用，用于对 PR 中的文件执行验证规则。</span><span class="sxs-lookup"><span data-stu-id="6abfe-102">The Docs PR validation service is a GitHub app that runs validation rules on the files in a PR.</span></span>

<span data-ttu-id="6abfe-103">在存储库上启用验证服务后，将看到以下行为：</span><span class="sxs-lookup"><span data-stu-id="6abfe-103">When the validation service is enabled on a repo, you'll see the following behavior:</span></span>

1. <span data-ttu-id="6abfe-104">提交 PR。</span><span class="sxs-lookup"><span data-stu-id="6abfe-104">You submit a PR.</span></span>
1. <span data-ttu-id="6abfe-105">在指示 PR 状态的 GitHub 注释中，将看到存储库上已启用“检查”状态。</span><span class="sxs-lookup"><span data-stu-id="6abfe-105">In the GitHub comment that indicates the status of your PR, you'll see the status of "checks" enabled on the repo.</span></span> <span data-ttu-id="6abfe-106">请注意，本示例启用了两个检查，“提交验证”和“OpenPublishing.Build”：</span><span class="sxs-lookup"><span data-stu-id="6abfe-106">Note that in this example, there are two checks enabled, "Commit Validation" and "OpenPublishing.Build":</span></span>

   ![部分检查失败](media/validation-failed.png)

   <span data-ttu-id="6abfe-108">即使提交验证失败，版本也可以通过。</span><span class="sxs-lookup"><span data-stu-id="6abfe-108">Build can pass even if commit validation fails.</span></span>

1. <span data-ttu-id="6abfe-109">单击“详细信息”以了解更多信息。</span><span class="sxs-lookup"><span data-stu-id="6abfe-109">Click **Details** for more information.</span></span>
1. <span data-ttu-id="6abfe-110">在“详细信息”页面上，将看到所有失败的验证检查，以及有关如何解决问题的信息：</span><span class="sxs-lookup"><span data-stu-id="6abfe-110">On the Details page, you'll see all the validation checks that failed, with information about how to fix the issues:</span></span>

   ![验证消息](media/validation-details.png)

<span data-ttu-id="6abfe-112">有关服务中当前验证的列表，请参阅本文左侧的 TOC。</span><span class="sxs-lookup"><span data-stu-id="6abfe-112">See the left-hand TOC of this article for the list of validations currently in the service.</span></span>