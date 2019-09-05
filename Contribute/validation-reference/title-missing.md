---
title: title-missing
description: 有关 Docs 生成问题 title-missing 的解释和解决方案
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/6/2019
ms.prod: non-product-specific
ms.openlocfilehash: cfe942be4285bb22f5fa08fa882077ea790fd2c4
ms.sourcegitcommit: dd751d0cb5b11f81a64ef62f3c83fd17cc5f0541
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/03/2019
ms.locfileid: "70236569"
---
# <a name="title-missing"></a><span data-ttu-id="69de8-103">title-missing</span><span class="sxs-lookup"><span data-stu-id="69de8-103">title-missing</span></span>

## <a name="warning"></a><span data-ttu-id="69de8-104">警告</span><span class="sxs-lookup"><span data-stu-id="69de8-104">Warning</span></span>

`Missing attribute: title. Add a title string (19 - 59 characters) to show in search engine results.`

## <a name="resolution"></a><span data-ttu-id="69de8-105">解决方法</span><span class="sxs-lookup"><span data-stu-id="69de8-105">Resolution</span></span>

<span data-ttu-id="69de8-106">请添加标题字符串以在搜索结果中显示。</span><span class="sxs-lookup"><span data-stu-id="69de8-106">Add a title string to show in search results.</span></span> <span data-ttu-id="69de8-107">通常，标题应介于 19 到 59 个字符之间，应与文章的 H1 区分开来，并且应包含相关的品牌词。</span><span class="sxs-lookup"><span data-stu-id="69de8-107">In general, titles should be between 19 and 59 characters, should be distinct from the H1 of the article, and should include relevant branding words.</span></span> <span data-ttu-id="69de8-108">不得在标题中包含“ | Microsoft Docs”字样 - 该字样由 Docs 自动添加；如果显式添加此项，则请忽略它。</span><span class="sxs-lookup"><span data-stu-id="69de8-108">You shouldn't include " | Microsoft Docs" in your title - this is added automatically by Docs, and is ignored if you add it explicitly.</span></span> <span data-ttu-id="69de8-109">如果想要向内容集中的所有标题添加其他品牌（例如“ - Azure”），请全局设置 `titleSuffix` 元数据值，或者对文件夹设置此值。</span><span class="sxs-lookup"><span data-stu-id="69de8-109">If you want to add additional branding, such as " - Azure", to all titles in a content set, set the `titleSuffix` metadata value globally or for a folder.</span></span>

<span data-ttu-id="69de8-110">你可以在 [https://moz.com/learn/seo/title-tag](https://moz.com/learn/seo/title-tag) 上预览标题在 Google 中的显示效果。</span><span class="sxs-lookup"><span data-stu-id="69de8-110">You can preview how your title will look in Google on [https://moz.com/learn/seo/title-tag](https://moz.com/learn/seo/title-tag).</span></span>

<span data-ttu-id="69de8-111">如果你是 Microsoft 员工，请参阅内部“参与者指南”中的 [SEO 基本信息](https://review.docs.microsoft.com/en-us/help/contribute/contribute-how-to-write-seo-basics?branch=master)，了解有关正确标题和搜索引擎优化 (SEO) 的更多信息。</span><span class="sxs-lookup"><span data-stu-id="69de8-111">If you're a Microsoft employee, see [SEO Basics](https://review.docs.microsoft.com/en-us/help/contribute/contribute-how-to-write-seo-basics?branch=master) in the internal Contributor Guide for more information about good titles and search engine optimization (SEO).</span></span>

[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
