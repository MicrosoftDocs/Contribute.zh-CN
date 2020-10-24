---
title: 参与 .NET 文档存储库中的 .NET 代码分析规则的文档撰写
description: 本文档介绍参与 .NET 文档存储库中的 .NET 代码分析规则的文章和代码示例撰写的过程。
author: mavasani
ms.author: mavasani
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
ms.date: 10/09/2020
ms.openlocfilehash: 27ae1a31c55c41aa1c97bf1f88dbf28bec35a80a
ms.sourcegitcommit: f1535713b66ff9b840f1138583746bc2bf182b4f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/12/2020
ms.locfileid: "91957039"
---
# <a name="contribute-docs-for-net-code-analysis-rules-to-the-net-docs-repository"></a>参与 .NET 文档存储库中的 .NET 代码分析规则的文档撰写

.NET Compiler Platform (Roslyn) 分析器会检查 C# 或 Visual Basic 代码的代码质量和代码样式问题。 从 .NET 5.0 开始，这些分析器[包含在 .NET SDK 中](/dotnet/fundamentals/code-analysis/overview)。

- [代码质量分析（“CAxxxx”规则）](/dotnet/fundamentals/code-analysis/overview#code-quality-analysis)：
  - 在 `dotnet/roslyn-analyzers` 存储库中已在[此处](https://github.com/dotnet/roslyn-analyzers/tree/master/src/NetAnalyzers)实现。
  - 在 `dotnet/docs` 存储库中已在[此处](https://github.com/dotnet/docs/blob/master/docs/fundamentals/code-analysis/quality-rules)记录。 请参阅[参与“CAxxxx”规则的文档撰写](#contribute-docs-for-caxxxx-rules)。
- [代码样式分析（“IDExxxx”规则）](/dotnet/fundamentals/code-analysis/overview#code-style-analysis)：
  - 在 `dotnet/roslyn` 存储库中已在[此处](https://github.com/dotnet/roslyn/tree/master/src/Analyzers)实现。
  - 在 `dotnet/docs` 存储库中已在[此处](https://github.com/dotnet/docs/blob/master/docs/fundamentals/code-analysis/style-rules)记录。 请参阅[参与“IDExxxx”规则的文档撰写](#contribute-docs-for-idexxxx-rules)。

## <a name="contribute-docs-for-caxxxx-rules"></a>参与“CAxxxx”规则的文档撰写

请按照以下步骤参与 [dotnet/docs](https://github.com/dotnet/docs) 存储库中的代码质量分析规则的文档撰写：

1. 确定 `Rule ID` 和 `Category`：确保你知道需要记录“CAxxxx”规则 ID 和规则的类别。 这表示 CA 分析器已合并到 [dotnet/roslyn-analyzers](https://github.com/dotnet/roslyn-analyzers) 存储库或开放的 PR 具有已批准的 ID 和已分配给规则的类别。
2. 添加规则文档：
   1. 在[根](https://github.com/dotnet/docs/blob/master/docs/fundamentals/code-analysis/quality-rules)文件夹下克隆现有的 CA 规则文件（如 `ca1000.md`），然后对其重命名。
   2. 适当地更新文件的内容。
3. 将规则的条目添加到以下表：
   - 在规则类别列表下的[目录](https://github.com/dotnet/docs/blob/master/docs/fundamentals/toc.yml)文件中。 例如，对于具有 `Performance` 类别的 CA 规则，搜索文件中的术语 `- name: Performance rules` 并将条目添加到列表中。 如果都不存在，请在 `- name: Code quality rules` 下创建新类别列表。
   - 在[顶级规则索引](https://github.com/dotnet/docs/blob/master/docs/fundamentals/code-analysis/quality-rules/index.md)文件中。
   - 在基于 `category` 的规则索引文件中：
     1. 在[根](https://github.com/dotnet/docs/blob/master/docs/fundamentals/code-analysis/quality-rules)文件夹下标识基于类别的索引文件。 例如，对于具有 `Performance` 类别的 CA 规则，此文件名为 `performance-warnings.md`。 如果都不存在，请通过克隆现有索引文件来创建基于类别的新索引文件。
     2. 在此文件中添加规则 ID 的条目。

> [!TIP]
> 执行 `dotnet/docs` 存储库中的存储库搜索以查找已知的现有 CA 规则 ID 来标识可能需要更新的位置。 有关示例，请参阅 <https://github.com/dotnet/docs/search?q=CA2000>。

## <a name="contribute-docs-for-idexxxx-rules"></a>参与“IDExxxx”规则的文档撰写

请按照以下步骤参与 [dotnet/docs](https://github.com/dotnet/docs) 存储库中的代码样式分析规则的文档撰写：

1. 确定 `Rule ID` 和代码样式选项（如果有）：确保你知道需要记录“IDExxxx”规则 ID 和规则的代码样式选项。 这表示 IDE 分析器已合并到 [dotnet/roslyn](https://github.com/dotnet/roslyn) 存储库或开放的 PR 具有已批准的 ID 和已分配给规则的代码样式选项。
2. 确定规则 `subcategory`：IDE 规则具有类别 `Style`。 通过阅读[代码样式规则](/dotnet/fundamentals/code-analysis/style-rules/index)的简介部分来标识规则子类别。 大多数 IDE 代码样式规则位于 `Language` 子类别下面。
3. 确定规则 `preference group`：通过通读[此处](/dotnet/fundamentals/code-analysis/style-rules/language-rules#net-style-rules)的首选项标头来标识规则的 `preference group`。
   - 如果规则具有关联的已知代码样式选项，则首选项组将与代码样式选项声明中指定的 `OptionGroup` 匹配。
   - 否则，请确定规则是否属于现有首选组或是否需要新的首选组。
4. 添加规则文档：
   1. 在[根](https://github.com/dotnet/docs/blob/master/docs/fundamentals/code-analysis/style-rules)文件夹下克隆现有的 IDE 规则文件（如 `ide0011.md`），然后对其重命名。
   2. 适当地更新文件的内容。
5. 将 IDE 规则和/或代码样式选项的条目添加到以下表：
   - 在规则的子类别和首选项列表下的[目录](https://github.com/dotnet/docs/blob/master/docs/fundamentals/toc.yml)文件中。 例如，对于具有 `Language` 子类别和 `Modifier preferences` 组的 IDE 代码样式规则，搜索文件中的术语 `- name: Language rules` 和子节点 `- name: Modifier preferences` 并将条目添加到列表中。 如果子类别下的子类别列表或首选项列表都不存在，请在 `- name: Code style rules` 下创建新列表。
   - 在[基于代码样式选项的索引](https://github.com/dotnet/docs/blob/master/docs/fundamentals/code-analysis/style-rules/language-rules.md)文件中。
   - 在[基于规则 ID 的索引](https://github.com/dotnet/docs/blob/master/docs/fundamentals/code-analysis/style-rules/index.md)文件中。
   - 在基于 `preferences group` 的规则索引文件中：
     1. 在[根](https://github.com/dotnet/docs/blob/master/docs/fundamentals/code-analysis/style-rules)文件夹下标识基于首选项组的索引文件。 例如，对于 `Modifier preferences` 的 IDE 规则，此文件名为 `modifier-preferences.md`。 如果都不存在，请通过克隆现有索引文件来创建基于首选项组的新索引文件。
     2. 在此文件中添加规则 ID 的条目。

> [!TIP]
> 执行 `dotnet/docs` 存储库中的存储库搜索，查找已知的现有 IDE 规则和/或代码样式选项，以便标识可能需要更新的位置。 有关示例，请参阅 <https://github.com/dotnet/docs/search?q=IDE0011> 和 <https://github.com/dotnet/docs/search?q=csharp_prefer_braces>。

## <a name="see-also"></a>另请参阅

- [参与 .NET 文档存储库撰写](dotnet-contribute.md)
