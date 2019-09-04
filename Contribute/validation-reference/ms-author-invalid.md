---
title: ms-author-invalid
description: 有关 Docs 生成问题 ms-author-invalid 的解释和解决方法
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/28/2019
ms.prod: non-product-specific
ms.openlocfilehash: 25428f93eaa7d36a5bbe35d77434ef33972e8944
ms.sourcegitcommit: dd751d0cb5b11f81a64ef62f3c83fd17cc5f0541
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/03/2019
ms.locfileid: "70236536"
---
# <a name="ms-author-invalid"></a><span data-ttu-id="50e12-103">ms-author-invalid</span><span class="sxs-lookup"><span data-stu-id="50e12-103">ms-author-invalid</span></span>

## <a name="warning"></a><span data-ttu-id="50e12-104">警告</span><span class="sxs-lookup"><span data-stu-id="50e12-104">Warning</span></span>

`Invalid value for ms.author: '{value}' is not a valid Microsoft alias, or is not an allowed distribution list.`

## <a name="resolution"></a><span data-ttu-id="50e12-105">解决方法</span><span class="sxs-lookup"><span data-stu-id="50e12-105">Resolution</span></span>

<span data-ttu-id="50e12-106">验证 `ms.author` 值是当前作者的 Microsoft 有效别名。</span><span class="sxs-lookup"><span data-stu-id="50e12-106">Verify that the `ms.author` value is the current author's valid Microsoft alias.</span></span> <span data-ttu-id="50e12-107">如果别名是通讯组列表，还必须位于允许列表中。</span><span class="sxs-lookup"><span data-stu-id="50e12-107">If the alias is a distribution list, it must also be on the allow list.</span></span>

<span data-ttu-id="50e12-108">可以在[此 Microsoft 内部网站](https://docsmetadatatool.azurewebsites.net/allowlists)上找到 DL 的有效值。</span><span class="sxs-lookup"><span data-stu-id="50e12-108">Valid values for DLs can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
