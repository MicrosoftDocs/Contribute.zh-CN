---
title: Git 和 GitHub 的文档概要
description: 本文概述了 Git、GitHub 存储库、组织内容的方式和用于 docs.microsoft.com 的命名约定。
author: bryanla
ms.author: bryanla
manager: mbaldwin
ms.date: 06/30/2017
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.custom: external-contributor-guide
ms.openlocfilehash: 5f7f90b69953e23833906202c739d2168b139d7e
ms.sourcegitcommit: e046e7aad8ed22bffe5380d63a9d40f0baeecc57
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/22/2018
---
# <a name="git-and-github-essentials-for-docs"></a>Git 和 GitHub 的 Docs 概要

## <a name="overview"></a>概述

作为 Docs 内容的参与者，你将与多个工具和进程进行交互。 你将与其他参与者并行处理同一项目，可能是完全相同的内容，甚至在同一时间。 这一切都可以通过 Git 和 GitHub 软件实现。

Git 是一个开源版本控制系统。 它通过存储库中文件的分布式版本控制来促进这种类型的项目协作。 实质上，Git 可以为给定的存储库整合多个参与者持续完成的工作流。

GitHub 是 Git 存储库基于 Web 的托管服务，例如用于存储 [docs.microsoft.com](https://docs.microsoft.com) 内容的托管服务。 对于任何项目，GitHub 托管主存储库，其中，参与者可为自己的工作创建副本。

## <a name="git"></a>Git

如果熟悉集中式版本控制系统（如 Team Foundation Server、SharePoint 或 Visual SourceSafe），你会注意到，Git 有一个用于支持其分布式模型的独特参与工作流程和术语。 例如，没有通常与签出/签入操作相关联的文件锁定。 事实上，Git 关心的是更精细粒度级别的更改，以逐字节比较文件。

Git 还使用分层结构来存储和管理项目的内容：

- *存储库 (Repository)*：英文缩写为“repo”，它是最大的存储单元。 存储库包括一个或多个分支。
- *分支*：一个存储单元，包含构成项目内容集的文件和文件夹。 分支分隔工作流（通常称为版本）。 始终提供发布内容并将范围限定为特定分支。 所有存储库都包含一个默认分支（通常命名为“主”分支）和一个或多个注定要并入主分支的其他分支。 主分支充当项目的当前版本和“单一事实来源”。 它是创建存储库中其他所有分支所依据的父级。

参与者与 Git 进行交互，更新和处理本地和 GitHub 级别的存储库：

- 在本地，通过 Git Bash 控制台等工具，可支持用于管理本地存储库并与 GitHub 存储库进行通信的 Git 命令
- 通过集成 Git 的 [www.github.com](https://www.github.com) 来管理流回主存储库的参与协调

## <a name="github"></a>GitHub

> [!NOTE]
> 尽管 Docs 指南基于 GitHub 的使用而制定，但有些团队使用 Visual Studio Team Service 来托管 Git 存储库。 Visual Studio 团队资源管理器客户端提供用于与 Team Services 存储库进行交互的 GUI，作为通过命令行使用 Git 命令的替代方法。
> </br>
> 此外，根据在 GitHub 中托管 Azure 服务内容的多年经验，以下许多指南都被开发为最佳做法。 某些 Docs 存储库可能需要它们。

所有工作流在 GitHub 级别开始和结束，期间存储任何 Docs 项目的主存储库。 参与者为自行使用而创建的副本将分散在多台计算机中。 这些副本将最终协调回项目的主 GitHub 存储库。

### <a name="directory-organization"></a>目录组织

如前所述，项目的默认/主分支用作项目的当前内容版本。 主分支（以及从主分支创建的分支）中的内容与相应 Docs 页面上文章的组织大体一致。 子目录用于分离类似内容（如服务）、媒体内容（如图像文件）和“包括”文件（使内容可重复使用）。

通常情况下，可在存储库的根目录处找到主要的 `articles` 目录。 文章目录包含一组子目录。 子目录中的文章格式为使用 .md 扩展名的 Markdown 文件。 一些支持多项服务的存储库（如 [https://github.com/microsoft/Azure-Docs](https://github.com/microsoft/Azure-Docs) 存储库）使用通用 `/articles` 子目录。 另一些存储库可能会使用服务专用名称，如使用 `/IntuneDocs` 的 [https://github.com/microsoft/IntuneDocs](https://github.com/microsoft/IntuneDocs) 存储库。

在此目录的根目录中，可以找到与整体服务或产品相关的一般性文章。 通常情况下，接下来可以找到其他系列的子目录，这些子目录与功能/服务或常见方案相匹配。 例如，Azure“虚拟机”文章在 `/virtual-machines` 子目录中，Intune“了解与探索”文章在 `/understand-explore` 子目录中。

### <a name="media-subdirectory"></a>媒体子目录

每个文章目录均包含对应媒体文件的 `/media` 子目录。 媒体文件包含引用图像的文章所使用的图像。

### <a name="includes-subdirectory"></a>包括子目录

只要在两个或多个文章间有共享的可重用内容，就可将其放入主`articles`目录的 `/includes` 子目录中。 在使用包含文件的 Markdown 文件中，相应的“include”Markdown 扩展名放置在需要引用包含文件的位置。

请参阅[如何使用 Markdown：包含](how-to-write-use-markdown.md#includes)以获得更多指导。

### <a name="markdown-file-template"></a>Markdown 文件模板

为方便起见，每个存储库的子目录通常包含名为 `template.md` 的 Markdown 模板文件。 如果需要创建新文章（用于提交到存储库），可使用此模板文件作为“起始文件”。 文件包含：

- 文件顶部的元数据标头，由 2 个 3 条连字符分隔。 它包含用于跟踪文章相关信息的各种标记。 文章元数据支持某些功能，如作者属性、参与者属性、痕迹导航和文章描述。 它还包括 SEO 优化和报告流程，Microsoft 用其来评估内容表现。 因此，元数据非常重要！
- 元数据部分介绍各种元数据标记和值。 如果不确定对元数据部分使用哪些值，可以将其留空，或使用前导井号标签 (#) 进行注释，然后由存储库拉取请求的审阅者审阅/完成它们。
- 对文章元素进行格式设置的各种 Markdown 使用示例。
- 常规 Markdown 扩展名使用说明，可用于各种警报类型。
- 使用 iframe 的嵌入视频示例。
- docs.microsoft.com 扩展的一般性使用说明，可用于特殊控件（如按钮和选择器）。

## <a name="pull-requests"></a>拉取请求

拉取请求为参与者提供了一种便捷方式，用于将建议的一组更改应用到默认分支。 更改（也称为提交）存储在参与者的分支中，因此 GitHub 可以首先创建将更改合并到默认分支的影响的模型。 拉取请求也是一种机制，用于向参与者提供来自生成/验证过程、拉取请求审阅者的反馈，以便在将更改合并到默认分支之前，解决潜在的问题或疑问。

通过拉取请求参与有两种方式，具体取决于要建议的更改大小。 这部分内容稍后在本指南的 [GitHub 工作流](how-to-write-workflows-major.md)部分中进行详细介绍。

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
