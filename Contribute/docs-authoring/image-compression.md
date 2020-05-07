---
title: 图像压缩 - Docs 创作包
description: 了解如何在 Docs 创作包 Visual Studio Code 扩展中压缩图像。
author: IEvangelist
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.date: 03/03/2020
ms.author: dapine
ms.openlocfilehash: 4b93ac23b83128d5b9125297879d008e9300509c
ms.sourcegitcommit: cfba5ad25b898bfed76046126ce8ff4871910701
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/04/2020
ms.locfileid: "78336649"
---
# <a name="image-compression"></a>图像压缩

[!INCLUDE [markdown-extension](includes/image-extension.md)]

## <a name="summary"></a>总结

所有文档均通过 Web 提供，PDF 版的文档除外。提供静态内容时，最好尽可能减少通过网络发送的字节数。 实现此目的的一种方法是压缩静态图像。

Docs 创作包扩展包括图像压缩上下文菜单项。 支持以下图像类型/扩展：

* \*.png
* \*.jpg
* \*.jpeg
* \*.gif
* \*.svg
* \*.webp

使用无损图像压缩算法（如果适用）。

## <a name="compress-image"></a>压缩图像

从“资源管理器”导航窗格右键单击图像文件，然后选择“压缩图像”选项。 随即会压缩该图像。

## <a name="compress-images-in-folder"></a>压缩文件夹中的图像

从“资源管理器”导航窗格右键单击包含图像的文件夹，然后选择“压缩文件夹中的图像”选项。 随即会压缩文件夹中的所有图像。

## <a name="considerations"></a>考虑事项

大分辨率图像的大小会隐式调整。 最大尺寸基于平台建议的最大宽度 `1,200px`。 仅当图像大于建议大小时，才使用最大尺寸，而且在自动调整大小时，图像将保持纵横比不变。

## <a name="preferences"></a>首选项

最大尺寸是可配置的，但默认的最大宽度为 `1200` 像素。 要配置最大尺寸，请选择“文件”->“首选项”->“设置”，并通过 `"Docs Image Extension"` 进行筛选。

:::image type="content" source="media/configure-image-compression.png" alt-text="配置图像压缩":::

> [!NOTE]
> 如果最大宽度或最大高度为值 `0`，则会忽略分辨率方差。

## <a name="in-action"></a>操作过程

下面是此功能的简短演示。

[![压缩图像演示](media/compress-image.gif)](media/compress-image.gif#lightbox)
