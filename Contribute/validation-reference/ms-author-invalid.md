---
title: ms-author-invalid
description: 有关 Docs 生成问题 ms-author-invalid 的解释和解决方法
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 9/27/2019
ms.prod: non-product-specific
ms.openlocfilehash: 615d9f5978893196a24e3a043f3b71a22e1eb353
ms.sourcegitcommit: 57eb071bdc55ef71fa3f8ac979326c3f8fbe9c45
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/10/2019
ms.locfileid: "72246289"
---
# <a name="ms-author-invalid"></a><span data-ttu-id="6f4c1-103">ms-author-invalid</span><span class="sxs-lookup"><span data-stu-id="6f4c1-103">ms-author-invalid</span></span>

## <a name="warning"></a><span data-ttu-id="6f4c1-104">警告</span><span class="sxs-lookup"><span data-stu-id="6f4c1-104">Warning</span></span>

`Invalid value for ms.author: '{value}' is not a valid Microsoft alias, or is not an allowed distribution list.`

## <a name="resolution"></a><span data-ttu-id="6f4c1-105">解决方法</span><span class="sxs-lookup"><span data-stu-id="6f4c1-105">Resolution</span></span>

<span data-ttu-id="6f4c1-106">请使用当前作者的 Microsoft 有效别名更新 `ms.author` 值。</span><span class="sxs-lookup"><span data-stu-id="6f4c1-106">Update the `ms.author` value with the current author's valid Microsoft alias.</span></span> <span data-ttu-id="6f4c1-107">建议指定的作者为全职员工或团队通讯组列表 (DL)，而不是短期供应商。</span><span class="sxs-lookup"><span data-stu-id="6f4c1-107">We recommend that the designated author be a full-time employee or team distribution list (DL), rather than a short-term vendor.</span></span> <span data-ttu-id="6f4c1-108">如果别名是 DL，还必须位于 `ms.author` 允许列表中。</span><span class="sxs-lookup"><span data-stu-id="6f4c1-108">If the alias is a DL, it must also be on the `ms.author` allow list.</span></span>

<span data-ttu-id="6f4c1-109">可以在 [Microsoft 内部网站](https://docsmetadatatool.azurewebsites.net/allowlists)上找到 `ms.author` DL 的有效值。</span><span class="sxs-lookup"><span data-stu-id="6f4c1-109">Valid values for `ms.author` DLs can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
