---
title: 提交拉取请求
description: 本文介绍用于确保你撰写的内容可以合并的 PR 过程和最佳做法。
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
author: sdwheeler
ms.author: sewhee
ms.date: 10/09/2019
ms.openlocfilehash: 156b5ec7b77bba5cf0a0ef2756ed8b64c21a8342
ms.sourcegitcommit: a812d716b31084926b886b93923f9b84c9b23429
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/18/2019
ms.locfileid: "75188218"
---
# <a name="best-practices-for-pull-requests"></a>拉取请求的最佳做法

若要发布内容更改，需要从分支提交拉取请求。 合并之前，必须评审每一个拉取请求。

## <a name="target-the-correct-branch"></a>确定正确的分支

应对 `staging` 分支进行所有更改。 不得对 `live` 分支进行更改。 在 `staging` 分支中进行的更改将合并到 `live`，这将覆盖对 `live` 进行的任何更改。

如果要提交的文档更改仅适用于 PowerShell 的未发布版本，请检查是否存在该版本的发布分支。 适用于特定未来版本的所有更改都应针对发布分支。 版本分支具有以下名称模式：`release-<version>`。

## <a name="make-the-pull-request-queue-work-better-for-everyone"></a>提高每个人的拉取请求队列工作效率

拉取请求队列中存在两种基本情况：

- 对于范围较小并且与更改相关的的拉取请求，所需的评审时间较短。
- 对于范围较大或包含不相关更改的拉取请求，所需的评审时间较长。

### <a name="avoid-branches-that-update-large-numbers-of-files"></a>避免有更新大量文件的分支

将对现有文章的次要更新与新文章的次要更新或主要改写区分开。 在独立的工作分支中处理这些更改。

批量更改会导致 PR 涉及大量已更改文件。 请将 PR 限制为最多 50 个已更改文件。 大型 PR 难以评审，并且更容易包含错误。

### <a name="renaming-or-deleting-files"></a>重命名或删除文件

重命名或删除文件时，请避免将这些更改与添加的内容或更新混合。
请在单独的 PR 中处理这些更改，该 PR 将合并于相关更新的 PR 之后。 例如，先更新重定向文件，再在删除文章前验证重定向是否有效。

必须更新链接到重命名文件的所有文件。 包括任何 TOC 文件。 还必须在存储库根目录中的主重定向文件 (`.openpublishing.redirection.json`) 中添加重定向条目。

## <a name="docs-pr-validation-service"></a>Docs PR 验证服务

Docs PR 验证服务是一个 GitHub 应用，用于对 PR 中的文件执行验证规则。

将出现以下行为：

1. 提交 PR。
1. 在指示 PR 状态的 GitHub 注释中，将看到存储库上已启用“检查”状态。 请注意，本示例启用了两个检查，“提交验证”和“OpenPublishing.Build”：

   ![部分检查失败](media/powershell-pull-requests/validation-failed.png)

   即使提交验证失败，版本也可以通过。

1. 单击“详细信息”以了解更多信息  。
1. 在“详细信息”页面上，将看到所有失败的验证检查，以及有关如何解决问题的信息。
1. 验证成功时，将向 PR 添加以下注释：

   ![生成验证](media/powershell-pull-requests/build-validation.png)

外部（非 Microsoft）参与者无权访问详细的生成报表或预览链接。

### <a name="build-warnings"></a>生成警告

通常，应修复所有生成错误、警告和建议。 但是，可忽略一些警告。

以下警告可忽略：

- > 找不到 `<version>/<modulepath>/About/About.md` 的服务名称

- > 具有以下名称的元数据不允许在 Yaml 标头中设置，也不允许在 docfx.json 中设置为文件级元数据或全局元数据：`locale`。 它们由 Docs 平台生成，因此，将忽略在这 3 个位置设置的值。 请从所有 3 个位置删除它们，以解决此警告。
