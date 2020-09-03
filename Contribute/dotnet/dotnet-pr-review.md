---
title: .NET docs 拉取请求评审流程
description: .NET docs 未启用 PR 合并 Webhook。 本文介绍这些存储库的 PR 流程
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
ms.date: 06/24/2020
ms.openlocfilehash: b2c0cbb0ed72948ba49a7456e16df5659057f5e6
ms.sourcegitcommit: 56505b3f7e670f6387d2c919f0326e9f4c571c8a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/31/2020
ms.locfileid: "89201118"
---
# <a name="pull-request-review-process-for-the-net-docs-repositories"></a><span data-ttu-id="eeea9-104">.NET docs 存储库的拉取请求评审流程</span><span class="sxs-lookup"><span data-stu-id="eeea9-104">Pull request review process for the .NET docs repositories</span></span>

<span data-ttu-id="eeea9-105">某些存储库（包括 .NET 存储库）没有启用“PR 合并”web 挂钩，这会自动合并次要 PR。</span><span class="sxs-lookup"><span data-stu-id="eeea9-105">Some repositories, including the .NET repositories, don't have the "PR Merger" web hook enabled, which automatically merges minor PRs.</span></span> <span data-ttu-id="eeea9-106">本文介绍这些存储库的 PR 评审流程。</span><span class="sxs-lookup"><span data-stu-id="eeea9-106">This article describes the PR review process for those repositories.</span></span> <span data-ttu-id="eeea9-107">PR 评审流程的设计目标是：</span><span class="sxs-lookup"><span data-stu-id="eeea9-107">The PR review process was designed with these goals:</span></span>

- <span data-ttu-id="eeea9-108">发布来自团队、产品团队成员和社区成员的高质量内容。</span><span class="sxs-lookup"><span data-stu-id="eeea9-108">Publish high-quality content from our team, product team members, and community members.</span></span>
- <span data-ttu-id="eeea9-109">以一致的方式向作者提供及时、可操作的反馈。</span><span class="sxs-lookup"><span data-stu-id="eeea9-109">Provide timely, actionable feedback to authors in a consistent manner.</span></span>
- <span data-ttu-id="eeea9-110">促进作者和审阅者之间的讨论。</span><span class="sxs-lookup"><span data-stu-id="eeea9-110">Facilitate discussion between authors and reviewers.</span></span>

<span data-ttu-id="eeea9-111">随着团队的不断创新和平台的日趋成熟，这些流程也会逐步改进。</span><span class="sxs-lookup"><span data-stu-id="eeea9-111">The processes continue to evolve as teams innovate and as the platform matures.</span></span>

## <a name="reviewers"></a><span data-ttu-id="eeea9-112">审阅者</span><span class="sxs-lookup"><span data-stu-id="eeea9-112">Reviewers</span></span>

<span data-ttu-id="eeea9-113">内容团队成员中的一员评审每个 PR。</span><span class="sxs-lookup"><span data-stu-id="eeea9-113">One of the content team members reviews every PR.</span></span> <span data-ttu-id="eeea9-114">内容团队成员可以请求特定产品团队成员进行评审，以验证技术准确性。</span><span class="sxs-lookup"><span data-stu-id="eeea9-114">Content team members may request a review from the specific product team members to verify technical accuracy.</span></span> <span data-ttu-id="eeea9-115">内容团队使用 GitHub 的代码所有权功能自动请求内容团队成员进行评审。</span><span class="sxs-lookup"><span data-stu-id="eeea9-115">The content team uses GitHub's Code Ownership feature to automatically request reviews from content team members.</span></span> <span data-ttu-id="eeea9-116">作为该流程的一部分，审阅者可以标记其他团队成员来评审内部 PR。</span><span class="sxs-lookup"><span data-stu-id="eeea9-116">As part of this process, a reviewer may tag other team members to review internal PRs.</span></span> <span data-ttu-id="eeea9-117">团队成员查看来自同一队列中的团队成员和社区成员的评审请求。</span><span class="sxs-lookup"><span data-stu-id="eeea9-117">Team members see requested reviews from team members and community members in the same queue.</span></span>

<span data-ttu-id="eeea9-118">社区成员也可以评审 PR 并提供反馈。</span><span class="sxs-lookup"><span data-stu-id="eeea9-118">Community members can review PRs and provide feedback as well.</span></span> <span data-ttu-id="eeea9-119">不过，核心内容团队中必须至少有一个成员批准任何 PR，才能合并 PR。</span><span class="sxs-lookup"><span data-stu-id="eeea9-119">However, at least one member of the core content team must approve any PR before it is merged.</span></span>

## <a name="review-process"></a><span data-ttu-id="eeea9-120">评审流程</span><span class="sxs-lookup"><span data-stu-id="eeea9-120">Review process</span></span>

<span data-ttu-id="eeea9-121">根据不同的 PR，评审遵循下面的三种方法之一：</span><span class="sxs-lookup"><span data-stu-id="eeea9-121">Reviews follow one of the three paths based on the PR:</span></span>

- <span data-ttu-id="eeea9-122">**小型 PR**：小型 PR 是单个 bug 修复，包括拼写错误、链接断开、小型代码更改或类似的更改。</span><span class="sxs-lookup"><span data-stu-id="eeea9-122">**Small PRs** - Small PRs are single bug fix: typos, broken links, small code changes, or similar changes.</span></span>
- <span data-ttu-id="eeea9-123">**主要发布内容**：主要发布内容是对现有文章、新文章的重要编辑，或对大量文章的编辑。</span><span class="sxs-lookup"><span data-stu-id="eeea9-123">**Major contributions** - Major contributions are significant edits to an existing article, new articles, or edits to a number of articles.</span></span>
- <span data-ttu-id="eeea9-124">正在进行的工作 - 作者可以通过打开草稿拉取请求来创建标记为“尚未准备好进行评审”的 PR。</span><span class="sxs-lookup"><span data-stu-id="eeea9-124">**Work in progress** - Authors can can create a PR that is marked as not ready for review yet by opening a *draft* pull request.</span></span>

<span data-ttu-id="eeea9-125">若要明确“小型”和“大型”贡献内容之间的区别，可以将参与者许可证协议 (CLA) 自动程序使用的过程作为一个良好的指导准则。</span><span class="sxs-lookup"><span data-stu-id="eeea9-125">The processing used by the Contributor License Agreement (CLA) bot is a good guideline for the distinction between "small" and "large" contributions.</span></span> <span data-ttu-id="eeea9-126">不需要进行 CLA 签名的 PR 可能属于“小型”发布内容。</span><span class="sxs-lookup"><span data-stu-id="eeea9-126">PRs that do not require the CLA to be signed are likely "small."</span></span> <span data-ttu-id="eeea9-127">需要 CLA 的 PR可能是“大型”发布内容。</span><span class="sxs-lookup"><span data-stu-id="eeea9-127">PRs that do require the CLA are likely "large."</span></span>

### <a name="small-prs"></a><span data-ttu-id="eeea9-128">小型 PR</span><span class="sxs-lookup"><span data-stu-id="eeea9-128">Small PRs</span></span>

<span data-ttu-id="eeea9-129">评审小型 PR 中的更改是否符合准确性，并使用评审网站上的内部版本进行检查。</span><span class="sxs-lookup"><span data-stu-id="eeea9-129">The changes in small PRs are reviewed for accuracy and checked using the build on the review site.</span></span> <span data-ttu-id="eeea9-130">由于它们是小型发布内容，这些 PR 不会触发对整篇文章的评审。</span><span class="sxs-lookup"><span data-stu-id="eeea9-130">Because they are small, these PRs do not trigger a review of the entire article.</span></span> 

<span data-ttu-id="eeea9-131">审阅者可能会注意到其他一些可以改进文章的小更改。</span><span class="sxs-lookup"><span data-stu-id="eeea9-131">Reviewers may notice other small changes that would improve an article.</span></span> <span data-ttu-id="eeea9-132">如果这些更改的范围也很小，建议将它们作为评审评论。</span><span class="sxs-lookup"><span data-stu-id="eeea9-132">If those changes are also small, suggest them as review comments.</span></span> <span data-ttu-id="eeea9-133">如果建议的更改将触发更大范围的评审，则将其作为待解决问题并稍后进行解决。</span><span class="sxs-lookup"><span data-stu-id="eeea9-133">If the suggested changes would trigger a larger review, open an issue and address those later.</span></span> 

### <a name="larger-changes"></a><span data-ttu-id="eeea9-134">较大更改</span><span class="sxs-lookup"><span data-stu-id="eeea9-134">Larger changes</span></span>

<span data-ttu-id="eeea9-135">较大型 PR 会进行更全面的评审。</span><span class="sxs-lookup"><span data-stu-id="eeea9-135">Larger PRs undergo a more thorough review.</span></span> <span data-ttu-id="eeea9-136">以下是所有检查的内容：</span><span class="sxs-lookup"><span data-stu-id="eeea9-136">The following are all checked:</span></span>

- <span data-ttu-id="eeea9-137">示例代码必须作为一个可下载的 zip 文件包含在源的 PR 中。</span><span class="sxs-lookup"><span data-stu-id="eeea9-137">Sample code must be included in the PR, in source and as a downloadable zip file.</span></span>
- <span data-ttu-id="eeea9-138">示例代码可正常编译和运行。</span><span class="sxs-lookup"><span data-stu-id="eeea9-138">Sample code compiles and runs correctly.</span></span>
- <span data-ttu-id="eeea9-139">文章明确描述了读者目标，并实现了这些目标。</span><span class="sxs-lookup"><span data-stu-id="eeea9-139">The article clearly describes the goals for the reader, and those goals are met.</span></span>
- <span data-ttu-id="eeea9-140">本文符合[样式和语法指南](dotnet-style-guide.md)，并遵循[语音和语调原则](dotnet-voice-tone.md)。</span><span class="sxs-lookup"><span data-stu-id="eeea9-140">The article meets [style and grammar guidelines](dotnet-style-guide.md) and follows our [voice and tone principles](dotnet-voice-tone.md).</span></span>
- <span data-ttu-id="eeea9-141">所有链接都应正确解析。</span><span class="sxs-lookup"><span data-stu-id="eeea9-141">All links should resolve correctly.</span></span>

<span data-ttu-id="eeea9-142">内容团队成员将评审 PR，并提交评审评论。</span><span class="sxs-lookup"><span data-stu-id="eeea9-142">Content team members will review the PR and submit the review with comments.</span></span> <span data-ttu-id="eeea9-143">如果只请求小幅更改，团队成员可以通过反馈来“批准”PR。</span><span class="sxs-lookup"><span data-stu-id="eeea9-143">If only minor changes are requested, team members may "approve" the PR with the feedback.</span></span> <span data-ttu-id="eeea9-144">然后，作者可以处理反馈并合并 PR。</span><span class="sxs-lookup"><span data-stu-id="eeea9-144">The author can then address the feedback and merge the PR.</span></span> <span data-ttu-id="eeea9-145">大多数评审会请求更改，在完成这些更改后，审阅者将再次进行评审。</span><span class="sxs-lookup"><span data-stu-id="eeea9-145">Most reviews will request changes and when those changes are made, the reviewer will review again.</span></span>

<span data-ttu-id="eeea9-146">如果编辑需要技术评审，内容团队审阅者将请求相应的产品团队成员进行评审。</span><span class="sxs-lookup"><span data-stu-id="eeea9-146">If the edits require a technical review, the content team reviewer will request a review from the appropriate product team member.</span></span>

### <a name="review-draft-pull-requests"></a><span data-ttu-id="eeea9-147">评审草稿拉取请求</span><span class="sxs-lookup"><span data-stu-id="eeea9-147">Review draft pull requests</span></span>

<span data-ttu-id="eeea9-148">你可能希望在此过程初期获得反馈。</span><span class="sxs-lookup"><span data-stu-id="eeea9-148">You may want feedback earlier in the process.</span></span> <span data-ttu-id="eeea9-149">打开草稿 PR 并添加请求之前评审的评论。</span><span class="sxs-lookup"><span data-stu-id="eeea9-149">Open a draft PR and add a comment that requests an early review.</span></span> <span data-ttu-id="eeea9-150">这些早期评审重点关注文章的结构：大纲、整体内容和示例。</span><span class="sxs-lookup"><span data-stu-id="eeea9-150">These early reviews focus on the structure of the article: the outline, the overall content, and the samples.</span></span> <span data-ttu-id="eeea9-151">这些评审不包括对语法和正确链接的全面检查。</span><span class="sxs-lookup"><span data-stu-id="eeea9-151">These reviews do not include a thorough check for grammar and correct links.</span></span>

## <a name="explain-suggestions"></a><span data-ttu-id="eeea9-152">解释建议</span><span class="sxs-lookup"><span data-stu-id="eeea9-152">Explain suggestions</span></span>

<span data-ttu-id="eeea9-153">通过 GitHub，可以在类型为 `suggestion`、显示为差异且可通过单击按钮合并的三重反引号块中输入注释。</span><span class="sxs-lookup"><span data-stu-id="eeea9-153">GitHub lets you enter comments in triple-back-tick blocks of type `suggestion` that are displayed as a diff and can be merged by clicking a button.</span></span> <span data-ttu-id="eeea9-154">在短行上，GitHub 会很好地突出显示所做的更改。</span><span class="sxs-lookup"><span data-stu-id="eeea9-154">On short lines, GitHub does a good job of highlighting the changes.</span></span> <span data-ttu-id="eeea9-155">在较长的行（如一行文本中的长段）上，GitHub 不会突出显示所做的更改。</span><span class="sxs-lookup"><span data-stu-id="eeea9-155">On longer lines, such as a long paragraph in one line of text, GitHub doesn't highlight the changes.</span></span> <span data-ttu-id="eeea9-156">为长行输入建议时，请注意是否已明确突出显示所做的更改。</span><span class="sxs-lookup"><span data-stu-id="eeea9-156">When entering a suggestion for a long line, notice whether your changes are clearly highlighted.</span></span> <span data-ttu-id="eeea9-157">如果未突出显示所做的更改，请在说明所做更改的建议块外添加注释。</span><span class="sxs-lookup"><span data-stu-id="eeea9-157">If the changes aren't highlighted, include comments outside the suggestion block explaining what you changed.</span></span> <span data-ttu-id="eeea9-158">如果没有说明，则后面的审阅者或 PR 作者通常需要花费很长时间来确定所做的更改。</span><span class="sxs-lookup"><span data-stu-id="eeea9-158">Without an explanation it's often time-consuming for subsequent reviewers or the PR author to figure out what the changes are.</span></span>

## <a name="respond-to-reviews"></a><span data-ttu-id="eeea9-159">对评审的响应</span><span class="sxs-lookup"><span data-stu-id="eeea9-159">Respond to reviews</span></span>

<span data-ttu-id="eeea9-160">作者更新 PR 以响应评论，用“+1”回应，标记每个已处理的评论，表明它已得到处理。</span><span class="sxs-lookup"><span data-stu-id="eeea9-160">The author updates the PR to respond to comments and marks each addressed comment with the "+1" reaction to indicate it was addressed.</span></span> <span data-ttu-id="eeea9-161">如果作者不同意评论内容，或者在其他 PR 中处理评论，他会添加评论来解释这些变更。</span><span class="sxs-lookup"><span data-stu-id="eeea9-161">If the author disagrees with the comment, or addresses the comment in a different PR, the author adds a comment explaining their change.</span></span>

<span data-ttu-id="eeea9-162">作者会在评论中 @-mentions 初始审阅者，请求重新评审。</span><span class="sxs-lookup"><span data-stu-id="eeea9-162">The author @-mentions the original reviewer in a comment to request a new review.</span></span> 

## <a name="response-time-expectations"></a><span data-ttu-id="eeea9-163">预期响应时间</span><span class="sxs-lookup"><span data-stu-id="eeea9-163">Response time expectations</span></span>

<span data-ttu-id="eeea9-164">内容团队成员通常会在两个工作日内评审新 PR。</span><span class="sxs-lookup"><span data-stu-id="eeea9-164">Content team members will typically review new PRs in under two business days.</span></span> <span data-ttu-id="eeea9-165">如果需要更长时间进行评审，团队成员中的一员会添加评论来确认 PR 并设置期望时间。</span><span class="sxs-lookup"><span data-stu-id="eeea9-165">If it takes longer to review, one of the team members will add a comment to acknowledge the PR and set expectations.</span></span>

<span data-ttu-id="eeea9-166">提交了评审后，作者应尝试在一周或更短时间内回复评论。</span><span class="sxs-lookup"><span data-stu-id="eeea9-166">Once a review has been submitted, authors should try to respond to comments in a week or less.</span></span> <span data-ttu-id="eeea9-167">志愿者可能无法满足以上要求，因为他们还有其他事项安排。</span><span class="sxs-lookup"><span data-stu-id="eeea9-167">Volunteers may not be able to meet these expectations because of other commitments.</span></span> <span data-ttu-id="eeea9-168">在这些情况下，团队成员会询问社区作者是否会更新 PR。</span><span class="sxs-lookup"><span data-stu-id="eeea9-168">In those cases, team members ask if the community author will update the PR.</span></span> <span data-ttu-id="eeea9-169">如果不进行更新，团队成员将为其更新和合并 PR。</span><span class="sxs-lookup"><span data-stu-id="eeea9-169">If not, the team member updates and merges the PR for them.</span></span>
