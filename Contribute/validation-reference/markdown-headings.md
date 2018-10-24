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
# <a name="markdown-headings"></a><span data-ttu-id="1f860-103">Markdown 标题</span><span class="sxs-lookup"><span data-stu-id="1f860-103">Markdown headings</span></span>

<span data-ttu-id="1f860-104">OPS Markdown 文件中的标题适用的验证要求如下。</span><span class="sxs-lookup"><span data-stu-id="1f860-104">The following validation requirements apply to headings in OPS Markdown files.</span></span>

## <a name="h1"></a><span data-ttu-id="1f860-105">H1</span><span class="sxs-lookup"><span data-stu-id="1f860-105">H1</span></span>

<span data-ttu-id="1f860-106">`H1` 是指 Markdown 文件中的第一个标题。</span><span class="sxs-lookup"><span data-stu-id="1f860-106">`H1` refers to the first heading in a Markdown file.</span></span> <span data-ttu-id="1f860-107">发布到 docs.microsoft.com 时，H1 以大字体显示在页面顶部。</span><span class="sxs-lookup"><span data-stu-id="1f860-107">When published to docs.microsoft.com, the H1 shows at the top of the page in a large font.</span></span>

<span data-ttu-id="1f860-108">H1 的创建方式为，以包含单个哈希 (`#`) 的行开头，后跟空格，然后是标题文本。</span><span class="sxs-lookup"><span data-stu-id="1f860-108">An H1 is created by beginning a line with a single hash (`#`) followed by a space, then the heading text.</span></span> <span data-ttu-id="1f860-109">例如，本文的 H1 是：</span><span class="sxs-lookup"><span data-stu-id="1f860-109">For example, the H1 of this article is:</span></span>

```md
# Markdown headings
```

<span data-ttu-id="1f860-110">H1 标题适用的规则如下：</span><span class="sxs-lookup"><span data-stu-id="1f860-110">The following rules apply to H1 headings:</span></span>

- <span data-ttu-id="1f860-111">H1 必须存在于文件中。</span><span class="sxs-lookup"><span data-stu-id="1f860-111">An H1 must be present in the file.</span></span>
- <span data-ttu-id="1f860-112">H1 只能有一个。</span><span class="sxs-lookup"><span data-stu-id="1f860-112">There can only be one H1.</span></span>
- <span data-ttu-id="1f860-113">H1 必须有内容。</span><span class="sxs-lookup"><span data-stu-id="1f860-113">The H1 must have content.</span></span>

  ```markdown
  # 
  This is not allowed.
  ```
- <span data-ttu-id="1f860-114">`#` 和 H1 内容之间必须有空格。</span><span class="sxs-lookup"><span data-stu-id="1f860-114">There must be a space between the `#` and the H1 content.</span></span> <span data-ttu-id="1f860-115">没有空格的 H1 不会在已发布页面上呈现为标题。</span><span class="sxs-lookup"><span data-stu-id="1f860-115">An H1 with no space doesn't render as a heading on the published page.</span></span>

  ```markdown
  #This looks bad on the site.
  ```
- <span data-ttu-id="1f860-116">H1 必须是 YML 元数据标头之后的文件中的第一个内容。</span><span class="sxs-lookup"><span data-stu-id="1f860-116">The H1 must be the first content in the file after the YML metadata header.</span></span> <span data-ttu-id="1f860-117">在 YML 标头的末尾和 H1 之间不允许使用文本或图像等内容。</span><span class="sxs-lookup"><span data-stu-id="1f860-117">No content, such as text or images, is allowed between the end of the YML header and the H1.</span></span>

  ```markdown
  ---
  ... YML would go here
  ---
  ![cheerful image](not-allowed.jpg)
  # This cheer is not allowed
  ```
- <span data-ttu-id="1f860-118">不应使用第一级标题的 HTML 元素 `<h1>`。</span><span class="sxs-lookup"><span data-stu-id="1f860-118">The HTML element for first-level headings, `<h1>`, should not be used.</span></span> <span data-ttu-id="1f860-119">使用 Markdown 语法 (`# `)。</span><span class="sxs-lookup"><span data-stu-id="1f860-119">Use the Markdown syntax (`# `).</span></span>
- <span data-ttu-id="1f860-120">H1 的长度不应超过 100 个字符。</span><span class="sxs-lookup"><span data-stu-id="1f860-120">The H1 should be no more than 100 characters long.</span></span> <span data-ttu-id="1f860-121">这是风格指南。</span><span class="sxs-lookup"><span data-stu-id="1f860-121">This is a style guideline.</span></span>

## <a name="h2---h6"></a><span data-ttu-id="1f860-122">H2 - H6</span><span class="sxs-lookup"><span data-stu-id="1f860-122">H2 - H6</span></span>

<span data-ttu-id="1f860-123">在 OPS 中允许 H2 (`## `) 至 H6 (`###### `)。</span><span class="sxs-lookup"><span data-stu-id="1f860-123">H2 (`## `) through H6 (`###### `) are allowed in OPS.</span></span> <span data-ttu-id="1f860-124">使用 Markdown 标头而不是 HTML (`<h2>` - `<h6>`) 来创建标题。</span><span class="sxs-lookup"><span data-stu-id="1f860-124">Use the Markdown headers, not the HTML (`<h2>` - `<h6>`), to create headings.</span></span>
