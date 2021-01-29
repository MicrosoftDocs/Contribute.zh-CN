---
title: 从 Jupyter 笔记本获取内容 - Docs 创作包
description: 了解如何使用 Docs 创作包（Visual Studio Code 扩展）将 Jupyter 笔记本中的内容插入并更新到你的文档中。
author: sdgilley
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.date: 01/19/2021
ms.author: sgilley
ms.openlocfilehash: c2b21d260c9e3bd90fbffed9a28afbebd76e2831
ms.sourcegitcommit: f174f438ad2cdb7f2acc5acc73bf5389074c44c5
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/26/2021
ms.locfileid: "98811964"
---
# <a name="insert-and-update-content-from-a-jupyter-notebook"></a>从 Jupyter 笔记本插入并更新内容

[!INCLUDE [markdown-extension](includes/markdown-extension.md)]

> [!IMPORTANT]
> 从 Jupyter 笔记本进行插入和更新的功能当前不适用于 Mac。

## <a name="summary"></a>总结

Jupyter 笔记本是在 Python 领域创建和共享代码的标准交互方式。  笔记本包含 Python 代码、Markdown 和（可选）代码输出的组合。


Docs 创作包扩展包括将静态 Markdown 版本的 Jupyter 笔记本置于文档中的功能：

Docs:插入 Jupyter 笔记本：输入笔记本的 URL。 Markdown 版本的笔记本将被添加到文档中光标所在的位置。 请勿修改开始或结束标记；下一个函数将使用它来更新笔记本。

Docs:更新 Jupyter 笔记本：此函数将在开始和结束之间使用最新版本替换之前插入的笔记本内容。 不需要输入 URL，它就记录在开始标记中。  更新功能假设文档中只有一个笔记本。  请勿将多个笔记本添加到一个文档中。

## <a name="in-action"></a>操作过程

下面是此功能的简短演示。

[![插入 Jupyter 笔记本](media/insertnotebook.gif)](media/insertnotebook.gif#lightbox)

## <a name="troubleshooting"></a>疑难解答

> [!IMPORTANT]
> 从 Jupyter 笔记本进行插入和更新的功能当前不适用于 Mac。

这些函数需要在计算机上安装 Python、`jupyter`和 `nbconvert`。

若要查看是否已安装 Python，请打开 VS Code 终端并运行以下命令：

* Windows - `where python`。
* Linux/Mac - `which python`

如果返回的是一个或多个路径，则 Python 已安装。  否则，请立即[安装 Python](https://www.python.org/downloads/)。

接下来，确保已安装 `jupyter`：

* Windows - `where jupyter`。
* Linux/Mac - `which jupyter`

如果未返回路径，请安装 `jupyter`：

```bash
pip install --upgrade jupyter
```

在安装 Python 和 `jupyter` 后，请安装 `nbconvert`：

```bash
pip install --upgrade nbconvert
```
