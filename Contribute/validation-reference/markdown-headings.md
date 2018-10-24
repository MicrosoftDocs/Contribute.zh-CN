---
title: Markdown 标题
description: 介绍 Markdown 标题的要求。
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 05/03/2017
ms.openlocfilehash: 18beb815fdf7caad3e8e675e8d79853d8a5688f2
ms.sourcegitcommit: 6f1997864c000a9cd25fb9171a8f8fdb8b5b5ece
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/11/2018
ms.locfileid: "49084420"
---
# <a name="markdown-headings"></a>Markdown 标题

OPS Markdown 文件中的标题适用的验证要求如下。

## <a name="h1"></a>H1

`H1` 是指 Markdown 文件中的第一个标题。 发布到 docs.microsoft.com 时，H1 以大字体显示在页面顶部。

H1 的创建方式为，以包含单个哈希 (`#`) 的行开头，后跟空格，然后是标题文本。 例如，本文的 H1 是：

```md
# Markdown headings
```

H1 标题适用的规则如下：

- H1 必须存在于文件中。
- H1 只能有一个。
- H1 必须有内容。

  ```markdown
  # 
  This is not allowed.
  ```
- `#` 和 H1 内容之间必须有空格。 没有空格的 H1 不会在已发布页面上呈现为标题。

  ```markdown
  #This looks bad on the site.
  ```
- H1 必须是 YML 元数据标头之后的文件中的第一个内容。 在 YML 标头的末尾和 H1 之间不允许使用文本或图像等内容。

  ```markdown
  ---
  ... YML would go here
  ---
  ![cheerful image](not-allowed.jpg)
  # This cheer is not allowed
  ```
- 不应使用第一级标题的 HTML 元素 `<h1>`。 使用 Markdown 语法 (`# `)。
- H1 的长度不应超过 100 个字符。 这是风格指南。

## <a name="h2---h6"></a>H2 - H6

在 OPS 中允许 H2 (`## `) 至 H6 (`###### `)。 使用 Markdown 标头而不是 HTML (`<h2>` - `<h6>`) 来创建标题。
