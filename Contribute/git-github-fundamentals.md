---
title: Git 和 GitHub 的文档概要
description: 本文概述了 Git、GitHub 存储库、组织内容的方式和用于 docs.microsoft.com 的命名约定。
ms.date: 06/30/2017
ms.openlocfilehash: 05c758845007f859382014166e88fd9614cdb873
ms.sourcegitcommit: d3c7b49dc854dae8da9cd49da8ac4035789a5010
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/23/2018
ms.locfileid: "49805691"
---
# <a name="git-and-github-essentials-for-docs"></a><span data-ttu-id="f4c28-103">Git 和 GitHub 的 Docs 概要</span><span class="sxs-lookup"><span data-stu-id="f4c28-103">Git and GitHub essentials for Docs</span></span>

## <a name="overview"></a><span data-ttu-id="f4c28-104">概述</span><span class="sxs-lookup"><span data-stu-id="f4c28-104">Overview</span></span>

<span data-ttu-id="f4c28-105">作为 Docs 内容的参与者，你将与多个工具和进程进行交互。</span><span class="sxs-lookup"><span data-stu-id="f4c28-105">As a contributor to Docs content, you will interact with multiple tools and processes.</span></span> <span data-ttu-id="f4c28-106">你将与其他参与者并行处理同一项目，可能是完全相同的内容，甚至在同一时间。</span><span class="sxs-lookup"><span data-stu-id="f4c28-106">You'll work in parallel with other contributors on the same project, potentially the exact same content, even at the same time.</span></span> <span data-ttu-id="f4c28-107">这一切都可以通过 Git 和 GitHub 软件实现。</span><span class="sxs-lookup"><span data-stu-id="f4c28-107">This is all enabled through Git and GitHub software.</span></span>

<span data-ttu-id="f4c28-108">Git 是一个开源版本控制系统。</span><span class="sxs-lookup"><span data-stu-id="f4c28-108">Git is an open-source version control system.</span></span> <span data-ttu-id="f4c28-109">它通过存储库中文件的分布式版本控制来促进这种类型的项目协作。</span><span class="sxs-lookup"><span data-stu-id="f4c28-109">It facilitates this type of project collaboration through *distributed version control* of files that live in *repositories*.</span></span> <span data-ttu-id="f4c28-110">实质上，Git 可以为给定的存储库整合多个参与者持续完成的工作流。</span><span class="sxs-lookup"><span data-stu-id="f4c28-110">In essence, Git makes it possible to integrate streams of work done by multiple contributors over time, for a given repository.</span></span>

<span data-ttu-id="f4c28-111">GitHub 是 Git 存储库基于 Web 的托管服务，例如用于存储 [docs.microsoft.com](https://docs.microsoft.com) 内容的托管服务。</span><span class="sxs-lookup"><span data-stu-id="f4c28-111">GitHub is a web-based hosting service for Git repositories, such as those used to store [docs.microsoft.com](https://docs.microsoft.com) content.</span></span> <span data-ttu-id="f4c28-112">对于任何项目，GitHub 托管主存储库，其中，参与者可为自己的工作创建副本。</span><span class="sxs-lookup"><span data-stu-id="f4c28-112">For any project, GitHub hosts the main repository, from which contributors can make copies for their own work.</span></span>

## <a name="git"></a><span data-ttu-id="f4c28-113">Git</span><span class="sxs-lookup"><span data-stu-id="f4c28-113">Git</span></span>

<span data-ttu-id="f4c28-114">如果熟悉集中式版本控制系统（如 Team Foundation Server、SharePoint 或 Visual SourceSafe），你会注意到，Git 有一个用于支持其分布式模型的独特参与工作流程和术语。</span><span class="sxs-lookup"><span data-stu-id="f4c28-114">If you're familiar with centralized version control systems (such as Team Foundation Server, SharePoint, or Visual SourceSafe), you will notice that Git has a unique contribution workflow and terminology to support its distributed model.</span></span> <span data-ttu-id="f4c28-115">例如，没有通常与签出/签入操作相关联的文件锁定。</span><span class="sxs-lookup"><span data-stu-id="f4c28-115">For instance, there is no file locking that is normally associated with check-out/check-in operations.</span></span> <span data-ttu-id="f4c28-116">事实上，Git 关心的是更精细粒度级别的更改，以逐字节比较文件。</span><span class="sxs-lookup"><span data-stu-id="f4c28-116">As a matter of fact, Git is concerned about changes at an even finer level, comparing files byte by byte.</span></span>

<span data-ttu-id="f4c28-117">Git 还使用分层结构来存储和管理项目的内容：</span><span class="sxs-lookup"><span data-stu-id="f4c28-117">Git also uses a tiered structure to store and manage content for a project:</span></span>

- <span data-ttu-id="f4c28-118">*存储库 (Repository)*：英文缩写为“repo”，它是最大的存储单元。</span><span class="sxs-lookup"><span data-stu-id="f4c28-118">*Repository*: Also known as a *repo*, this is the highest unit of storage.</span></span> <span data-ttu-id="f4c28-119">存储库包括一个或多个分支。</span><span class="sxs-lookup"><span data-stu-id="f4c28-119">A repository contains one or more branches.</span></span>
- <span data-ttu-id="f4c28-120">*分支*：一个存储单元，包含构成项目内容集的文件和文件夹。</span><span class="sxs-lookup"><span data-stu-id="f4c28-120">*Branch*: A unit of storage that contains the files and  folders that make up a project's content set.</span></span> <span data-ttu-id="f4c28-121">分支分隔工作流（通常称为版本）。</span><span class="sxs-lookup"><span data-stu-id="f4c28-121">Branches separate streams of work (typically referred to as versions).</span></span> <span data-ttu-id="f4c28-122">始终提供发布内容并将范围限定为特定分支。</span><span class="sxs-lookup"><span data-stu-id="f4c28-122">Contributions are always made and scoped to a specific branch.</span></span> <span data-ttu-id="f4c28-123">所有存储库都包含一个默认分支（通常命名为“主”分支）和一个或多个注定要并入主分支的其他分支。</span><span class="sxs-lookup"><span data-stu-id="f4c28-123">All repositories contain a default branch (typically named "master") and one or more branches that are destined to be merged back into the master branch.</span></span> <span data-ttu-id="f4c28-124">主分支充当项目的当前版本和“单一事实来源”。</span><span class="sxs-lookup"><span data-stu-id="f4c28-124">The master branch serves as the current version and "single source of truth" for the project.</span></span> <span data-ttu-id="f4c28-125">它是创建存储库中其他所有分支所依据的父级。</span><span class="sxs-lookup"><span data-stu-id="f4c28-125">It's the parent from which all other branches in the repository are created.</span></span>

<span data-ttu-id="f4c28-126">参与者与 Git 进行交互，更新和处理本地和 GitHub 级别的存储库：</span><span class="sxs-lookup"><span data-stu-id="f4c28-126">Contributors interact with Git to update and manipulate repositories at both the local and GitHub levels:</span></span>

- <span data-ttu-id="f4c28-127">在本地，通过 Git Bash 控制台等工具，该工具支持用于管理本地存储库并与 GitHub 存储库进行通信的 Git 命令。</span><span class="sxs-lookup"><span data-stu-id="f4c28-127">Locally through tools such as the Git Bash console, which supports Git commands for managing local repositories and communicating with GitHub repositories.</span></span>
- <span data-ttu-id="f4c28-128">通过 [www.github.com](https://www.github.com) 集成 Git 来管理流回主存储库的参与协调。</span><span class="sxs-lookup"><span data-stu-id="f4c28-128">Via [www.github.com](https://www.github.com), which integrates Git to manage the reconciliation of contributions that flow back into the main repository.</span></span>

## <a name="github"></a><span data-ttu-id="f4c28-129">GitHub</span><span class="sxs-lookup"><span data-stu-id="f4c28-129">GitHub</span></span>

> [!NOTE]
> <span data-ttu-id="f4c28-130">尽管 Docs 指南基于 GitHub 的使用而制定，但有些团队使用 Visual Studio Team Service 来托管 Git 存储库。</span><span class="sxs-lookup"><span data-stu-id="f4c28-130">Although Docs guidance is based on using GitHub, some teams use Visual Studio Team Services to host Git repositories.</span></span> <span data-ttu-id="f4c28-131">Visual Studio 团队资源管理器客户端提供用于与 Team Services 存储库进行交互的 GUI，作为通过命令行使用 Git 命令的替代方法。</span><span class="sxs-lookup"><span data-stu-id="f4c28-131">The Visual Studio Team Explorer client provides a GUI for interacting with Team Services repositories, as an alternative to using Git commands through a command line.</span></span>
> </br>
> <span data-ttu-id="f4c28-132">此外，根据在 GitHub 中托管 Azure 服务内容的多年经验，以下许多指南都被开发为最佳做法。</span><span class="sxs-lookup"><span data-stu-id="f4c28-132">Also, many of the following guidelines were developed as best practices from years of experience in hosting Azure service content in GitHub.</span></span> <span data-ttu-id="f4c28-133">某些 Docs 存储库可能需要它们。</span><span class="sxs-lookup"><span data-stu-id="f4c28-133">They might be required in some Docs repositories.</span></span>

<span data-ttu-id="f4c28-134">所有工作流在 GitHub 级别开始和结束，期间存储任何 Docs 项目的主存储库。</span><span class="sxs-lookup"><span data-stu-id="f4c28-134">All workflows begin and end at the GitHub level, where the main repository for any Docs project is stored.</span></span> <span data-ttu-id="f4c28-135">参与者为自行使用而创建的副本将分散在多台计算机中。</span><span class="sxs-lookup"><span data-stu-id="f4c28-135">The copies that contributors create for their own use are distributed across multiple computers.</span></span> <span data-ttu-id="f4c28-136">这些副本将最终协调回项目的主 GitHub 存储库。</span><span class="sxs-lookup"><span data-stu-id="f4c28-136">These copies are eventually reconciled back into the project's main GitHub repository.</span></span>

### <a name="directory-organization"></a><span data-ttu-id="f4c28-137">目录组织</span><span class="sxs-lookup"><span data-stu-id="f4c28-137">Directory organization</span></span>

<span data-ttu-id="f4c28-138">如前所述，项目的默认/主分支用作项目的当前内容版本。</span><span class="sxs-lookup"><span data-stu-id="f4c28-138">As mentioned earlier, a project's default/master branch serves as the current version of content for the project.</span></span> <span data-ttu-id="f4c28-139">主分支（以及从主分支创建的分支）中的内容与相应 Docs 页面上文章的组织大体一致。</span><span class="sxs-lookup"><span data-stu-id="f4c28-139">The content in the master branch--and branches created from it--is loosely aligned with the organization of the articles on the corresponding Docs pages.</span></span> <span data-ttu-id="f4c28-140">子目录用于分离类似内容（如服务）、媒体内容（如图像文件）和“包括”文件（使内容可重复使用）。</span><span class="sxs-lookup"><span data-stu-id="f4c28-140">Subdirectories are used for separation of like content (such as services), media content (such as image files), and "include" files (which enable reuse of content).</span></span>

<span data-ttu-id="f4c28-141">通常情况下，可在存储库的根目录处找到主要的 `articles` 目录。</span><span class="sxs-lookup"><span data-stu-id="f4c28-141">You can typically find a main `articles` directory off the root of the repository.</span></span> <span data-ttu-id="f4c28-142">文章目录包含一组子目录。</span><span class="sxs-lookup"><span data-stu-id="f4c28-142">The articles directory contains a set of subdirectories.</span></span> <span data-ttu-id="f4c28-143">子目录中的文章格式为使用 .md 扩展名的 Markdown 文件。</span><span class="sxs-lookup"><span data-stu-id="f4c28-143">Articles in the subdirectories are formatted as Markdown files that use an *.md* extension.</span></span> <span data-ttu-id="f4c28-144">一些支持多项服务的存储库（如 [Azure-Docs](https://github.com/MicrosoftDocs/Azure-Docs) 存储库）使用通用 `/articles` 子目录。</span><span class="sxs-lookup"><span data-stu-id="f4c28-144">Some repositories that support multiple services use a generic `/articles` subdirectory, such as the [Azure-Docs](https://github.com/MicrosoftDocs/Azure-Docs) repository.</span></span> <span data-ttu-id="f4c28-145">另一些存储库可能会使用服务专用名称，如使用 `/IntuneDocs` 的 [IntuneDocs](https://github.com/MicrosoftDocs/IntuneDocs) 存储库。</span><span class="sxs-lookup"><span data-stu-id="f4c28-145">Others might use a service-specific name, such as the [IntuneDocs](https://github.com/MicrosoftDocs/IntuneDocs) repository, which uses `/IntuneDocs`.</span></span>

<span data-ttu-id="f4c28-146">在此目录的根目录中，可以找到与整体服务或产品相关的一般性文章。</span><span class="sxs-lookup"><span data-stu-id="f4c28-146">Within the root of this directory, you can find general articles that relate to the overall service or product.</span></span> <span data-ttu-id="f4c28-147">通常情况下，接下来可以找到其他系列的子目录，这些子目录与功能/服务或常见方案相匹配。</span><span class="sxs-lookup"><span data-stu-id="f4c28-147">And typically, you can then find another series of subdirectories that match the features/services or common scenarios.</span></span> <span data-ttu-id="f4c28-148">例如，Azure“虚拟机”文章在 `/virtual-machines` 子目录中，Intune“了解与探索”文章在 `/understand-explore` 子目录中。</span><span class="sxs-lookup"><span data-stu-id="f4c28-148">For instance, Azure "virtual machine" articles are in the `/virtual-machines` subdirectory, and Intune "understand and explore" articles are in the `/understand-explore` subdirectory.</span></span>

### <a name="media-subdirectory"></a><span data-ttu-id="f4c28-149">媒体子目录</span><span class="sxs-lookup"><span data-stu-id="f4c28-149">Media subdirectory</span></span>

<span data-ttu-id="f4c28-150">每个文章目录均包含对应媒体文件的 `/media` 子目录。</span><span class="sxs-lookup"><span data-stu-id="f4c28-150">Each article directory contains a `/media` subdirectory for corresponding media files.</span></span> <span data-ttu-id="f4c28-151">媒体文件包含引用图像的文章所使用的图像。</span><span class="sxs-lookup"><span data-stu-id="f4c28-151">Media files contain images used by articles that have image references.</span></span>

### <a name="includes-subdirectory"></a><span data-ttu-id="f4c28-152">包括子目录</span><span class="sxs-lookup"><span data-stu-id="f4c28-152">Includes subdirectory</span></span>

<span data-ttu-id="f4c28-153">只要在两个或多个文章间有共享的可重用内容，就可将其放入主`articles`目录的 `/includes` 子目录中。</span><span class="sxs-lookup"><span data-stu-id="f4c28-153">Whenever we have reusable content that is shared across two or more articles, it is placed in an `/includes` subdirectory off the main `articles` directory.</span></span> <span data-ttu-id="f4c28-154">在使用包含文件的 Markdown 文件中，相应的“include”Markdown 扩展名放置在需要引用包含文件的位置。</span><span class="sxs-lookup"><span data-stu-id="f4c28-154">In a Markdown file that uses the include file, a corresponding "include" Markdown extension is placed in the location where the include file needs to be referenced.</span></span>

<span data-ttu-id="f4c28-155">请参阅[如何使用 Markdown：包含](how-to-write-use-markdown.md#includes)以获得更多指导。</span><span class="sxs-lookup"><span data-stu-id="f4c28-155">See [How to use Markdown: Includes](how-to-write-use-markdown.md#includes) for additional guidance.</span></span>

### <a name="markdown-file-template"></a><span data-ttu-id="f4c28-156">Markdown 文件模板</span><span class="sxs-lookup"><span data-stu-id="f4c28-156">Markdown file template</span></span>

<span data-ttu-id="f4c28-157">为方便起见，每个存储库的子目录通常包含名为 `template.md` 的 Markdown 模板文件。</span><span class="sxs-lookup"><span data-stu-id="f4c28-157">For convenience, the root directory of each repository typically contains a Markdown template file named `template.md`.</span></span> <span data-ttu-id="f4c28-158">如果需要创建新文章（用于提交到存储库），可使用此模板文件作为“起始文件”。</span><span class="sxs-lookup"><span data-stu-id="f4c28-158">You can use this template file as a "starter file" if you need to create a new article for submission to the repository.</span></span> <span data-ttu-id="f4c28-159">文件包含：</span><span class="sxs-lookup"><span data-stu-id="f4c28-159">The file contains:</span></span>

- <span data-ttu-id="f4c28-160">文件顶部的元数据标头，由 2 个 3 条连字符分隔。</span><span class="sxs-lookup"><span data-stu-id="f4c28-160">A **metadata header** at the top of the file, delineated by two, 3-hyphen lines.</span></span> <span data-ttu-id="f4c28-161">它包含用于跟踪文章相关信息的各种标记。</span><span class="sxs-lookup"><span data-stu-id="f4c28-161">It contains the various tags used for tracking information related to the article.</span></span> <span data-ttu-id="f4c28-162">文章元数据支持某些功能，如作者属性、参与者属性、痕迹导航和文章描述。</span><span class="sxs-lookup"><span data-stu-id="f4c28-162">Article metadata enables certain functionality, such as author attribution, contributor attribution, breadcrumbs, and article descriptions.</span></span> <span data-ttu-id="f4c28-163">它还包括 SEO 优化和报告流程，Microsoft 用其来评估内容表现。</span><span class="sxs-lookup"><span data-stu-id="f4c28-163">It also includes SEO optimizations and reporting processes that Microsoft uses to evaluate the performance of the content.</span></span> <span data-ttu-id="f4c28-164">因此，元数据非常重要！</span><span class="sxs-lookup"><span data-stu-id="f4c28-164">So the metadata is important!</span></span>
- <span data-ttu-id="f4c28-165">元数据部分介绍各种元数据标记和值。</span><span class="sxs-lookup"><span data-stu-id="f4c28-165">A **metadata section** that describes the various metadata tags and values.</span></span> <span data-ttu-id="f4c28-166">如果不确定对元数据部分使用哪些值，可以将其留空，或使用前导井号标签 (#) 进行注释，然后由存储库拉取请求的审阅者审阅/完成它们。</span><span class="sxs-lookup"><span data-stu-id="f4c28-166">If you're unsure of the values to use for the metadata section, you can leave them blank or comment them with a leading hashtag (#), and they will be reviewed/completed by the pull request reviewer for the repository.</span></span>
- <span data-ttu-id="f4c28-167">对文章元素进行格式设置的各种 Markdown 使用示例。</span><span class="sxs-lookup"><span data-stu-id="f4c28-167">Various **examples of using Markdown** to format the elements of an article.</span></span>
- <span data-ttu-id="f4c28-168">常规 Markdown 扩展名使用说明，可用于各种警报类型。</span><span class="sxs-lookup"><span data-stu-id="f4c28-168">General **instructions on the use of Markdown extensions**, which you can use for various types of alerts.</span></span>
- <span data-ttu-id="f4c28-169">使用 iframe 的嵌入视频示例。</span><span class="sxs-lookup"><span data-stu-id="f4c28-169">Examples of **embedding video** by using an iframe.</span></span>
- <span data-ttu-id="f4c28-170">docs.microsoft.com 扩展的一般性使用说明，可用于特殊控件（如按钮和选择器）。</span><span class="sxs-lookup"><span data-stu-id="f4c28-170">General **instructions on the use of docs.microsoft.com extensions**, which you can use for special controls such as buttons and selectors.</span></span>

## <a name="pull-requests"></a><span data-ttu-id="f4c28-171">拉取请求</span><span class="sxs-lookup"><span data-stu-id="f4c28-171">Pull requests</span></span>

<span data-ttu-id="f4c28-172">拉取请求为参与者提供了一种便捷方式，用于将建议的一组更改应用到默认分支。</span><span class="sxs-lookup"><span data-stu-id="f4c28-172">A *pull request* provides a convenient way for a contributor to propose a set of changes that will be applied to the default branch.</span></span> <span data-ttu-id="f4c28-173">更改（也称为提交）存储在参与者的分支中，因此 GitHub 可以首先创建将更改合并到默认分支的影响的模型。</span><span class="sxs-lookup"><span data-stu-id="f4c28-173">The changes (also known as *commits*) are stored in a contributor's branch, so GitHub can first model the impact of *merging* them into the default branch.</span></span> <span data-ttu-id="f4c28-174">拉取请求也是一种机制，用于向参与者提供来自生成/验证过程、拉取请求审阅者的反馈，以便在将更改合并到默认分支之前，解决潜在的问题或疑问。</span><span class="sxs-lookup"><span data-stu-id="f4c28-174">A pull request also serves as a mechanism to provide the contributor with feedback from a build/validation process, the pull request reviewer, to resolve potential issues or questions before the changes are merged into the default branch.</span></span>

<span data-ttu-id="f4c28-175">通过拉取请求参与有两种方式，具体取决于要建议的更改大小。</span><span class="sxs-lookup"><span data-stu-id="f4c28-175">There are two ways to contribute by pull request, depending on the size of changes that you want to propose.</span></span> <span data-ttu-id="f4c28-176">这部分内容稍后在本指南的 [GitHub 工作流](how-to-write-workflows-major.md)部分中进行详细介绍。</span><span class="sxs-lookup"><span data-stu-id="f4c28-176">We will cover this in detail later, in the [GitHub workflow](how-to-write-workflows-major.md) section of this guide.</span></span>

<!---- Reference links for Docs landing pages, associated GitHub repositories, and related Forums matrix. ------------------>
<!---- PLEASE INSERT URLS IN ASCENDING SORT ORDER, AND REMOVE LOCALE SEGMENT FROM URLS (that is, en-us) FOR LOCALIZED FORUMS! -->
<!---- NOTE: these links are saved for future use in another/new article; no longer used above in this article --->
[Visual-Studio-Page]:(https://docs.microsoft.com/en-us/visualstudio/index)
[Visual-Studio-Repo-Internal]:(https://github.com/Microsoft/vsdocs)
[Visual-Studio-Repo-External]:(https://github.com/Microsoft/visualstudio-docs)
[Visual-Studio-SO]: (https://stackoverflow.com/search?q=Visual+Studio+2017)
[Dotnet-Page]: https://docs.microsoft.com/dotnet
[Dotnet-Core-Page]: https://docs.microsoft.com/dotnet/articles/welcome
[Dotnet-Core-Repo]: https://github.com/dotnet/docs
[EM-ATA-Land]: https://docs.microsoft.com/advanced-threat-analytics/
[EM-ATA-Repo]: https://github.com/Microsoft/ATADocs
[EM-AzureAD-Land]: https://docs.microsoft.com/active-directory/
[EM-AzureAD-Repo]: https://github.com/Azure/azure-content/tree/master/articles/active-directory/
[EM-AzureRMS-Land]: https://docs.microsoft.com/rights-management/
[EM-AzureRMS-Repo]: https://github.com/Microsoft/Azure-RMSDocs
[EM-Intune-Land]: https://docs.microsoft.com/intune/
[EM-Intune-Repo]: https://github.com/microsoft/intuneDocs
[EM-Land-Page]: https://docs.microsoft.com/enterprise-mobility/
[EM-Land-Repo]: https://github.com/Microsoft/EMDocs/
[EM-MFA-Land]: https://docs.microsoft.com/multi-factor-authentication/
[EM-MFA-Repo]: https://github.com/Azure/azure-content/tree/master/articles/multi-factor-authentication
[EM-MIM-Land]: https://docs.microsoft.com/microsoft-identity-manager/
[EM-MIM-Repo]: https://github.com/Microsoft/MIMDocs
[EM-RemoteApp-Land]: https://docs.microsoft.com/en-us/remoteapp/
[EM-RemoteApp-Repo]: https://github.com/Azure/azure-content/tree/master/articles/remoteapp
[Forum-MSDN-ATA]: https://social.technet.microsoft.com/Forums/en-US/home?forum=mata
[Forum-MSDN-AzureAD]: https://social.msdn.microsoft.com/Forums/en-US/home?forum=WindowsAzureAD
[Forum-MSDN-AzureRMS]: https://social.technet.microsoft.com/Forums/en-US/home?forum=rmsapps%2Crmscloud&filter=alltypes&sort=lastpostdesc
[Forum-MSDN-EM]: https://social.technet.microsoft.com/Forums/en-US/home?sort=relevancedesc&brandIgnore=True&searchTerm=Enterprise+Mobility
[Forum-MSDN-Intune]: https://social.technet.microsoft.com/Forums/en-us/home?category=microsoftintune
[Forum-MSDN-Main]: https://social.msdn.microsoft.com/Forums/home
[Forum-MSDN-MFA]: https://social.msdn.microsoft.com/Forums/en-US/home?forum=windowsazureactiveauthentication
[Forum-MSDN-MIM]: https://social.technet.microsoft.com/Forums/en-US/home?category=identitymanagement
[Forum-MSDN-RemoteApp]: https://social.technet.microsoft.com/Forums/en-US/home?filter=alltypes&brandIgnore=True&sort=relevancedesc&searchTerm=Azure+Remote+or+RemoteApp
[Forum-SO-AzureAD]: https://stackoverflow.com/questions/tagged/azure-active-directory
[Forum-SO-AzureRMS]: https://stackoverflow.com/questions/tagged/rights-management
[Forum-SO-Dotnet]: https://stackoverflow.com/questions/tagged/.net
[Forum-SO-Dotnet-Core]: https://stackoverflow.com/questions/tagged/.net-core
[Forum-SO-Main]: https://stackoverflow.com/tags
[Forum-SO-Intune]: https://stackoverflow.com/questions/tagged/intune
[Forum-SO-MFA]: https://stackoverflow.com/search?q=%5Bazure%5D+multi-factor
[Forum-SO-MIM]: https://stackoverflow.com/search?q=Microsoft+Identity+Manager
[Forum-SO-RemoteApp]: https://stackoverflow.com/questions/tagged/remoteapp
[Forum-TechNet-Main]: https://social.technet.microsoft.com/Forums/home
[Forum-Yammer-AzureRMS]: https://www.yammer.com/AskIPTeam
[Forum-Yammer-Main]: https://www.yammer.com/
