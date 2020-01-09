---
title: 提交拉取请求
description: 本文介绍用于确保你撰写的内容可以合并的 PR 过程和最佳做法。
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
author: sdwheeler
ms.author: sewhee
ms.date: 10/09/2019
ms.openlocfilehash: 156b5ec7b77bba5cf0a0ef2756ed8b64c21a8342
ms.sourcegitcommit: a812d716b31084926b886b93923f9b84c9b23429
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/18/2019
ms.locfileid: "75188218"
---
# <a name="best-practices-for-pull-requests"></a><span data-ttu-id="b920e-103">拉取请求的最佳做法</span><span class="sxs-lookup"><span data-stu-id="b920e-103">Best Practices for Pull requests</span></span>

<span data-ttu-id="b920e-104">若要发布内容更改，需要从分支提交拉取请求。</span><span class="sxs-lookup"><span data-stu-id="b920e-104">To publish changes to content, you submit a pull request from your fork.</span></span> <span data-ttu-id="b920e-105">合并之前，必须评审每一个拉取请求。</span><span class="sxs-lookup"><span data-stu-id="b920e-105">Every pull request has to be reviewed before it can be merged.</span></span>

## <a name="target-the-correct-branch"></a><span data-ttu-id="b920e-106">确定正确的分支</span><span class="sxs-lookup"><span data-stu-id="b920e-106">Target the correct branch</span></span>

<span data-ttu-id="b920e-107">应对 `staging` 分支进行所有更改。</span><span class="sxs-lookup"><span data-stu-id="b920e-107">All changes should be made to the `staging` branch.</span></span> <span data-ttu-id="b920e-108">不得对 `live` 分支进行更改。</span><span class="sxs-lookup"><span data-stu-id="b920e-108">Changes should never be targeted at the `live` branch.</span></span> <span data-ttu-id="b920e-109">在 `staging` 分支中进行的更改将合并到 `live`，这将覆盖对 `live` 进行的任何更改。</span><span class="sxs-lookup"><span data-stu-id="b920e-109">Changes made in the `staging` branch get merged into `live` so any changes made to `live` are overwritten.</span></span>

<span data-ttu-id="b920e-110">如果要提交的文档更改仅适用于 PowerShell 的未发布版本，请检查是否存在该版本的发布分支。</span><span class="sxs-lookup"><span data-stu-id="b920e-110">If you are submitting a change to documentation that only applies to an unreleased version of PowerShell, check to see if there is a release branch for that version.</span></span> <span data-ttu-id="b920e-111">适用于特定未来版本的所有更改都应针对发布分支。</span><span class="sxs-lookup"><span data-stu-id="b920e-111">All changes that apply to a specific, future version should be targeted at the release branch.</span></span> <span data-ttu-id="b920e-112">版本分支具有以下名称模式：`release-<version>`。</span><span class="sxs-lookup"><span data-stu-id="b920e-112">Release branches have the following name pattern: `release-<version>`.</span></span>

## <a name="make-the-pull-request-queue-work-better-for-everyone"></a><span data-ttu-id="b920e-113">提高每个人的拉取请求队列工作效率</span><span class="sxs-lookup"><span data-stu-id="b920e-113">Make the pull request queue work better for everyone</span></span>

<span data-ttu-id="b920e-114">拉取请求队列中存在两种基本情况：</span><span class="sxs-lookup"><span data-stu-id="b920e-114">There are two basic realities in the PR queue:</span></span>

- <span data-ttu-id="b920e-115">对于范围较小并且与更改相关的的拉取请求，所需的评审时间较短。</span><span class="sxs-lookup"><span data-stu-id="b920e-115">Pull requests that are small in scope and relate changes take less time to review.</span></span>
- <span data-ttu-id="b920e-116">对于范围较大或包含不相关更改的拉取请求，所需的评审时间较长。</span><span class="sxs-lookup"><span data-stu-id="b920e-116">Pull requests that are large in scope or that contain unrelated changes take more time to review.</span></span>

### <a name="avoid-branches-that-update-large-numbers-of-files"></a><span data-ttu-id="b920e-117">避免有更新大量文件的分支</span><span class="sxs-lookup"><span data-stu-id="b920e-117">Avoid branches that update large numbers of files</span></span>

<span data-ttu-id="b920e-118">将对现有文章的次要更新与新文章的次要更新或主要改写区分开。</span><span class="sxs-lookup"><span data-stu-id="b920e-118">Separate minor updates to existing articles from new articles or major rewrites.</span></span> <span data-ttu-id="b920e-119">在独立的工作分支中处理这些更改。</span><span class="sxs-lookup"><span data-stu-id="b920e-119">Work on these changes in separate working branches.</span></span>

<span data-ttu-id="b920e-120">批量更改会导致 PR 涉及大量已更改文件。</span><span class="sxs-lookup"><span data-stu-id="b920e-120">Bulk changes drive PRs with large numbers of changed files.</span></span> <span data-ttu-id="b920e-121">请将 PR 限制为最多 50 个已更改文件。</span><span class="sxs-lookup"><span data-stu-id="b920e-121">Limit your PRs to a maximum of 50 changed files.</span></span> <span data-ttu-id="b920e-122">大型 PR 难以评审，并且更容易包含错误。</span><span class="sxs-lookup"><span data-stu-id="b920e-122">Large PRs are difficult to review and are more prone to contain errors.</span></span>

### <a name="renaming-or-deleting-files"></a><span data-ttu-id="b920e-123">重命名或删除文件</span><span class="sxs-lookup"><span data-stu-id="b920e-123">Renaming or deleting files</span></span>

<span data-ttu-id="b920e-124">重命名或删除文件时，请避免将这些更改与添加的内容或更新混合。</span><span class="sxs-lookup"><span data-stu-id="b920e-124">When you rename or delete files, avoid mixing these changes with content additions or updates.</span></span>
<span data-ttu-id="b920e-125">请在单独的 PR 中处理这些更改，该 PR 将合并于相关更新的 PR 之后。</span><span class="sxs-lookup"><span data-stu-id="b920e-125">Handle these changes in a separate PR that gets merged after the PR for related updates.</span></span> <span data-ttu-id="b920e-126">例如，先更新重定向文件，再在删除文章前验证重定向是否有效。</span><span class="sxs-lookup"><span data-stu-id="b920e-126">For example, update the redirects file and verify the redirect is working before deleting an article.</span></span>

<span data-ttu-id="b920e-127">必须更新链接到重命名文件的所有文件。</span><span class="sxs-lookup"><span data-stu-id="b920e-127">You must update all files that link to the renamed file.</span></span> <span data-ttu-id="b920e-128">包括任何 TOC 文件。</span><span class="sxs-lookup"><span data-stu-id="b920e-128">This includes any TOC files.</span></span> <span data-ttu-id="b920e-129">还必须在存储库根目录中的主重定向文件 (`.openpublishing.redirection.json`) 中添加重定向条目。</span><span class="sxs-lookup"><span data-stu-id="b920e-129">You must also add redirection entries in the master redirection file (`.openpublishing.redirection.json`) in the root of the repository.</span></span>

## <a name="docs-pr-validation-service"></a><span data-ttu-id="b920e-130">Docs PR 验证服务</span><span class="sxs-lookup"><span data-stu-id="b920e-130">Docs PR validation service</span></span>

<span data-ttu-id="b920e-131">Docs PR 验证服务是一个 GitHub 应用，用于对 PR 中的文件执行验证规则。</span><span class="sxs-lookup"><span data-stu-id="b920e-131">The Docs PR validation service is a GitHub app that runs validation rules on the files in a PR.</span></span>

<span data-ttu-id="b920e-132">将出现以下行为：</span><span class="sxs-lookup"><span data-stu-id="b920e-132">You'll see the following behavior:</span></span>

1. <span data-ttu-id="b920e-133">提交 PR。</span><span class="sxs-lookup"><span data-stu-id="b920e-133">You submit a PR.</span></span>
1. <span data-ttu-id="b920e-134">在指示 PR 状态的 GitHub 注释中，将看到存储库上已启用“检查”状态。</span><span class="sxs-lookup"><span data-stu-id="b920e-134">In the GitHub comment that indicates the status of your PR, you'll see the status of "checks" enabled on the repo.</span></span> <span data-ttu-id="b920e-135">请注意，本示例启用了两个检查，“提交验证”和“OpenPublishing.Build”：</span><span class="sxs-lookup"><span data-stu-id="b920e-135">Note that in this example, there are two checks enabled, "Commit Validation" and "OpenPublishing.Build":</span></span>

   ![部分检查失败](media/powershell-pull-requests/validation-failed.png)

   <span data-ttu-id="b920e-137">即使提交验证失败，版本也可以通过。</span><span class="sxs-lookup"><span data-stu-id="b920e-137">Build can pass even if commit validation fails.</span></span>

1. <span data-ttu-id="b920e-138">单击“详细信息”以了解更多信息  。</span><span class="sxs-lookup"><span data-stu-id="b920e-138">Click **Details** for more information.</span></span>
1. <span data-ttu-id="b920e-139">在“详细信息”页面上，将看到所有失败的验证检查，以及有关如何解决问题的信息。</span><span class="sxs-lookup"><span data-stu-id="b920e-139">On the Details page, you'll see all the validation checks that failed, with information about how to fix the issues.</span></span>
1. <span data-ttu-id="b920e-140">验证成功时，将向 PR 添加以下注释：</span><span class="sxs-lookup"><span data-stu-id="b920e-140">When validation succeeds, the following comment is added to the PR:</span></span>

   ![生成验证](media/powershell-pull-requests/build-validation.png)

<span data-ttu-id="b920e-142">外部（非 Microsoft）参与者无权访问详细的生成报表或预览链接。</span><span class="sxs-lookup"><span data-stu-id="b920e-142">If you are an external (non-Microsoft) contributor you do not have access to the detailed build reports or preview links.</span></span>

### <a name="build-warnings"></a><span data-ttu-id="b920e-143">生成警告</span><span class="sxs-lookup"><span data-stu-id="b920e-143">Build warnings</span></span>

<span data-ttu-id="b920e-144">通常，应修复所有生成错误、警告和建议。</span><span class="sxs-lookup"><span data-stu-id="b920e-144">Normally you should fix all build errors, warnings, and suggestions.</span></span> <span data-ttu-id="b920e-145">但是，可忽略一些警告。</span><span class="sxs-lookup"><span data-stu-id="b920e-145">However, there are some warnings that can be ignored.</span></span>

<span data-ttu-id="b920e-146">以下警告可忽略：</span><span class="sxs-lookup"><span data-stu-id="b920e-146">The following warnings can be ignored:</span></span>

- > <span data-ttu-id="b920e-147">找不到 `<version>/<modulepath>/About/About.md` 的服务名称</span><span class="sxs-lookup"><span data-stu-id="b920e-147">Can't find service name for `<version>/<modulepath>/About/About.md`</span></span>

- > <span data-ttu-id="b920e-148">具有以下名称的元数据不允许在 Yaml 标头中设置，也不允许在 docfx.json 中设置为文件级元数据或全局元数据：`locale`。</span><span class="sxs-lookup"><span data-stu-id="b920e-148">Metadata with following name(s) are not allowed to be set in Yaml header, or as file level metadata in docfx.json, or as global metadata in docfx.json: `locale`.</span></span> <span data-ttu-id="b920e-149">它们由 Docs 平台生成，因此，将忽略在这 3 个位置设置的值。</span><span class="sxs-lookup"><span data-stu-id="b920e-149">They are generated by Docs platform, so the values set in these 3 places will be ignored.</span></span> <span data-ttu-id="b920e-150">请从所有 3 个位置删除它们，以解决此警告。</span><span class="sxs-lookup"><span data-stu-id="b920e-150">Please remove them from all 3 places to resolve the warning.</span></span>
