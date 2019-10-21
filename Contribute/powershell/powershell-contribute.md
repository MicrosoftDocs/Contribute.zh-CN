---
title: 参与 PowerShell 文档存储库撰写
description: 本文介绍组成 PowerShell 文档的存储库。
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
author: sdwheeler
ms.author: sewhee
ms.date: 10/09/2019
ms.openlocfilehash: 6b975c085aa42846be9951a77d3fdebbd5fb17a1
ms.sourcegitcommit: ca84e542b081e145052f38967e826f6ef25da1b2
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/12/2019
ms.locfileid: "72290164"
---
# <a name="contributing-to-powershell-documentation"></a><span data-ttu-id="ce9c8-103">参与 PowerShell 文档撰写</span><span class="sxs-lookup"><span data-stu-id="ce9c8-103">Contributing to PowerShell Documentation</span></span>

<span data-ttu-id="ce9c8-104">感谢你对 PowerShell 文档的关注！</span><span class="sxs-lookup"><span data-stu-id="ce9c8-104">Thank you for your interest in PowerShell documentation!</span></span>

<span data-ttu-id="ce9c8-105">本文档介绍参与托管在 PowerShell 文档网站上的文章和代码示例撰写的过程。</span><span class="sxs-lookup"><span data-stu-id="ce9c8-105">This document covers the process for contributing to the articles and code samples that are hosted on the PowerShell documentation site.</span></span> <span data-ttu-id="ce9c8-106">参与供稿可能像更正拼写错误一样简单，也可能像撰写新文章一样复杂。</span><span class="sxs-lookup"><span data-stu-id="ce9c8-106">Contributions may be as simple as typo corrections or as complex as new articles.</span></span>

<span data-ttu-id="ce9c8-107">PowerShell 文档网站是从包含一个或多个 docset 的多个存储库生成的：</span><span class="sxs-lookup"><span data-stu-id="ce9c8-107">The PowerShell documentation site is built from multiple repositories containing one or more docsets:</span></span>

- <span data-ttu-id="ce9c8-108">[PowerShell 概念和 cmdlet 引用][psdocs]</span><span class="sxs-lookup"><span data-stu-id="ce9c8-108">[PowerShell concepts & cmdlet reference][psdocs]</span></span>
- <span data-ttu-id="ce9c8-109">PowerShell SDK 代码示例 - 包含 SDK 文章中使用的示例的专用存储库</span><span class="sxs-lookup"><span data-stu-id="ce9c8-109">PowerShell SDK code samples - private repository containing the samples used in the SDK articles</span></span>
- <span data-ttu-id="ce9c8-110">[PowerShell .NET SDK 引用](/dotnet/api/?view=pscore-6.2.0) - 从 PowerShell 源代码生成的专用存储库内容</span><span class="sxs-lookup"><span data-stu-id="ce9c8-110">[PowerShell .NET SDK reference](/dotnet/api/?view=pscore-6.2.0) - private repository contents generated from PowerShell source code</span></span>

<span data-ttu-id="ce9c8-111">所有这些内容的问题都在 [PowerShell-Docs][docsrepo] 存储库中进行跟踪。</span><span class="sxs-lookup"><span data-stu-id="ce9c8-111">Issues for all this content are tracked in the [PowerShell-Docs][docsrepo] repository.</span></span>

## <a name="repository-structure"></a><span data-ttu-id="ce9c8-112">存储库结构</span><span class="sxs-lookup"><span data-stu-id="ce9c8-112">Repository Structure</span></span>

<span data-ttu-id="ce9c8-113">PowerShell-Docs 存储库由三个发布到 [Microsoft Docs][psdocs] 的 docset 组成。docset 包含在以下文件夹中：</span><span class="sxs-lookup"><span data-stu-id="ce9c8-113">The PowerShell-Docs repository consists of three docsets that are published to [Microsoft Docs][psdocs]. The docsets are contained in the following folders:</span></span>

- <span data-ttu-id="ce9c8-114">[/reference/][ref] - 包含 PowerShell cmdlet 引用，适用于 PowerShell 中提供的 cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ce9c8-114">[/reference/][ref] - contains the PowerShell cmdlet reference for the cmdlets that ship in PowerShell.</span></span> <span data-ttu-id="ce9c8-115">引用收集于版本文件夹中（3.0、4.0、5.0、5.1、6 和 7）。</span><span class="sxs-lookup"><span data-stu-id="ce9c8-115">The reference is collected in versions folders (3.0, 4.0, 5.0, 5.1, 6, and 7).</span></span> <span data-ttu-id="ce9c8-116">此 docset 不包含适用于 Windows 或其他 Microsoft 产品中提供的模块的引用。</span><span class="sxs-lookup"><span data-stu-id="ce9c8-116">This docset does not contain the reference for the modules that ship in Windows or other Microsoft products.</span></span>
- <span data-ttu-id="ce9c8-117">[/reference/docs-conceptual][conceptual] - 包含 PowerShell 概念性文档。</span><span class="sxs-lookup"><span data-stu-id="ce9c8-117">[/reference/docs-conceptual][conceptual] - contains the PowerShell conceptual documentation.</span></span> <span data-ttu-id="ce9c8-118">其中包括安装说明、示例脚本、操作方法主题等。</span><span class="sxs-lookup"><span data-stu-id="ce9c8-118">This include setup instructions, sample scripts, how-to topics, and more.</span></span>
- <span data-ttu-id="ce9c8-119">[/developer/][SDK] - 包含 PowerShell SDK 概念性文档。</span><span class="sxs-lookup"><span data-stu-id="ce9c8-119">[/developer/][SDK] - contains the PowerShell SDK conceptual documentation.</span></span>

<!--link refs-->
[psdocs]: https://docs.microsoft.com/powershell
[docsrepo]: https://github.com/MicrosoftDocs/PowerShell-Docs
[ref]: https://github.com/MicrosoftDocs/PowerShell-Docs/tree/staging/reference
[conceptual]: https://github.com/MicrosoftDocs/PowerShell-Docs/tree/staging/reference/docs-conceptual
[SDK]: https://github.com/MicrosoftDocs/PowerShell-Docs/tree/staging/developer
