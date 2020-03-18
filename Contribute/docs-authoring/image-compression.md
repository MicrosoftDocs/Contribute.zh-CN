---
title: 图像压缩 - Docs 创作包
description: 了解如何在 Docs 创作包 Visual Studio Code 扩展中压缩图像。
author: IEvangelist
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.date: 03/03/2020
ms.author: dapine
ms.openlocfilehash: 4b93ac23b83128d5b9125297879d008e9300509c
ms.sourcegitcommit: dbc2c48194e29bfa0c88d33f50f94b9ee26be2da
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/05/2020
ms.locfileid: "78336649"
---
# <a name="image-compression"></a><span data-ttu-id="84021-103">图像压缩</span><span class="sxs-lookup"><span data-stu-id="84021-103">Image compression</span></span>

[!INCLUDE [markdown-extension](includes/image-extension.md)]

## <a name="summary"></a><span data-ttu-id="84021-104">摘要</span><span class="sxs-lookup"><span data-stu-id="84021-104">Summary</span></span>

<span data-ttu-id="84021-105">所有文档均通过 Web 提供，PDF 版的文档除外。提供静态内容时，最好尽可能减少通过网络发送的字节数。</span><span class="sxs-lookup"><span data-stu-id="84021-105">All documentation is provided via the web, with the exception of PDF versions of docs. When serving static content, it is best to minimize the number of bytes sent over the wire.</span></span> <span data-ttu-id="84021-106">实现此目的的一种方法是压缩静态图像。</span><span class="sxs-lookup"><span data-stu-id="84021-106">One way to do that is to compress images at rest.</span></span>

<span data-ttu-id="84021-107">Docs 创作包扩展包括图像压缩上下文菜单项。</span><span class="sxs-lookup"><span data-stu-id="84021-107">The Docs Authoring Pack extension includes image compression context menu items.</span></span> <span data-ttu-id="84021-108">支持以下图像类型/扩展：</span><span class="sxs-lookup"><span data-stu-id="84021-108">The following image types / extensions are supported:</span></span>

* <span data-ttu-id="84021-109">\*.png </span><span class="sxs-lookup"><span data-stu-id="84021-109">*\*.png*</span></span>
* <span data-ttu-id="84021-110">\*.jpg </span><span class="sxs-lookup"><span data-stu-id="84021-110">*\*.jpg*</span></span>
* <span data-ttu-id="84021-111">\*.jpeg </span><span class="sxs-lookup"><span data-stu-id="84021-111">*\*.jpeg*</span></span>
* <span data-ttu-id="84021-112">\*.gif </span><span class="sxs-lookup"><span data-stu-id="84021-112">*\*.gif*</span></span>
* <span data-ttu-id="84021-113">\*.svg </span><span class="sxs-lookup"><span data-stu-id="84021-113">*\*.svg*</span></span>
* <span data-ttu-id="84021-114">\*.webp </span><span class="sxs-lookup"><span data-stu-id="84021-114">*\*.webp*</span></span>

<span data-ttu-id="84021-115">使用无损图像压缩算法（如果适用）。</span><span class="sxs-lookup"><span data-stu-id="84021-115">The lossless image compression algorithms are used, where applicable.</span></span>

## <a name="compress-image"></a><span data-ttu-id="84021-116">压缩图像</span><span class="sxs-lookup"><span data-stu-id="84021-116">Compress image</span></span>

<span data-ttu-id="84021-117">从“资源管理器”导航窗格右键单击图像文件，然后选择“压缩图像”选项   。</span><span class="sxs-lookup"><span data-stu-id="84021-117">From the **Explorer** navigation pane, right-click on an image file - then select the **Compress image** option.</span></span> <span data-ttu-id="84021-118">随即会压缩该图像。</span><span class="sxs-lookup"><span data-stu-id="84021-118">The image is then compressed.</span></span>

## <a name="compress-images-in-folder"></a><span data-ttu-id="84021-119">压缩文件夹中的图像</span><span class="sxs-lookup"><span data-stu-id="84021-119">Compress images in folder</span></span>

<span data-ttu-id="84021-120">从“资源管理器”导航窗格右键单击包含图像的文件夹，然后选择“压缩文件夹中的图像”选项   。</span><span class="sxs-lookup"><span data-stu-id="84021-120">From the **Explorer** navigation pane, right-click on a folder containing images - then select the **Compress images in folder** option.</span></span> <span data-ttu-id="84021-121">随即会压缩文件夹中的所有图像。</span><span class="sxs-lookup"><span data-stu-id="84021-121">All images in the folder are compressed.</span></span>

## <a name="considerations"></a><span data-ttu-id="84021-122">考虑事项</span><span class="sxs-lookup"><span data-stu-id="84021-122">Considerations</span></span>

<span data-ttu-id="84021-123">大分辨率图像的大小会隐式调整。</span><span class="sxs-lookup"><span data-stu-id="84021-123">Large resolution images are implicitly resized.</span></span> <span data-ttu-id="84021-124">最大尺寸基于平台建议的最大宽度 `1,200px`。</span><span class="sxs-lookup"><span data-stu-id="84021-124">The maximum dimensions are based on the platform suggested max width of `1,200px`.</span></span> <span data-ttu-id="84021-125">仅当图像大于建议大小时，才使用最大尺寸，而且在自动调整大小时，图像将保持纵横比不变。</span><span class="sxs-lookup"><span data-stu-id="84021-125">The max is only used when images are larger than they are recommended to be, and they will maintain the aspect ratio when automatically resized.</span></span>

## <a name="preferences"></a><span data-ttu-id="84021-126">首选项</span><span class="sxs-lookup"><span data-stu-id="84021-126">Preferences</span></span>

<span data-ttu-id="84021-127">最大尺寸是可配置的，但默认的最大宽度为 `1200` 像素。</span><span class="sxs-lookup"><span data-stu-id="84021-127">The maximum dimensions are configurable, but a default max width of `1200` pixels exists.</span></span> <span data-ttu-id="84021-128">要配置最大尺寸，请选择“文件”->“首选项”->“设置”，并通过 `"Docs Image Extension"` 进行筛选  。</span><span class="sxs-lookup"><span data-stu-id="84021-128">To configure the max dimensions, select **File -> Preferences -> Settings** and filter by `"Docs Image Extension"`.</span></span>

:::image type="content" source="media/configure-image-compression.png" alt-text="配置图像压缩":::

> [!NOTE]
> <span data-ttu-id="84021-130">如果最大宽度或最大高度为值 `0`，则会忽略分辨率方差   。</span><span class="sxs-lookup"><span data-stu-id="84021-130">A value of `0` in either the **Max Width** or **Max Height** will simply ignore resolution variances.</span></span>

## <a name="in-action"></a><span data-ttu-id="84021-131">操作过程</span><span class="sxs-lookup"><span data-stu-id="84021-131">In action</span></span>

<span data-ttu-id="84021-132">下面是此功能的简短演示。</span><span class="sxs-lookup"><span data-stu-id="84021-132">Below is a brief demonstration of this feature.</span></span>

<span data-ttu-id="84021-133">[![压缩图像演示](media/compress-image.gif)](media/compress-image.gif#lightbox)</span><span class="sxs-lookup"><span data-stu-id="84021-133">[![Compress image demo](media/compress-image.gif)](media/compress-image.gif#lightbox)</span></span>
