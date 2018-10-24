---
author: meganbradley
ms.author: mbradley
ms.openlocfilehash: fa048980afcf3c50f7d990f9c88064df6ee5ebb5
ms.sourcegitcommit: 6f1997864c000a9cd25fb9171a8f8fdb8b5b5ece
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/11/2018
ms.locfileid: "49084439"
---
# <a name="docs-pr-validation-service"></a>Docs PR 验证服务

Docs PR 验证服务是一个 GitHub 应用，用于对 PR 中的文件执行验证规则。

在存储库上启用验证服务后，将看到以下行为：

1. 提交 PR。
1. 在指示 PR 状态的 GitHub 注释中，将看到存储库上已启用“检查”状态。 请注意，本示例启用了两个检查，“提交验证”和“OpenPublishing.Build”：

   ![部分检查失败](media/validation-failed.png)

   即使提交验证失败，版本也可以通过。

1. 单击“详细信息”以了解更多信息。
1. 在“详细信息”页面上，将看到所有失败的验证检查，以及有关如何解决问题的信息：

   ![验证消息](media/validation-details.png)

有关服务中当前验证的列表，请参阅本文左侧的 TOC。