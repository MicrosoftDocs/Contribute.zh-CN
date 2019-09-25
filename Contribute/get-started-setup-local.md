---
title: 设置本地 Git 存储库
description: 本文介绍创建本地 Git 存储库和提供文档的指南，包括创建分支和克隆过程。
author: jasonwhowell
ms.author: jasonh
ms.date: 01/18/2018
ms.openlocfilehash: 285c25fe0e5df067ceeaa5a42da1bad5533d2c84
ms.sourcegitcommit: 7e73bef8bcdca39fd54cd79fbe8cb22da5566411
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2019
ms.locfileid: "71247394"
---
# <a name="set-up-git-repository-locally-for-documentation"></a>设置本地 Git 文档存储库

本文介绍在本地计算机上设置 Git 存储库的步骤，旨在为 Microsoft 文档提供帮助。 参与者可以使用本地克隆的存储库来添加新项目，对现有文章进行主要编辑或更改图片。

运行这些一次性设置活动即可开始参与其中：
> [!div class="checklist"]
> * 确定相应的存储库
> * 对 GitHub 帐户创建存储库分支
> * 为克隆文件选择一个本地文件夹
> * 将存储库克隆到本地计算机
> * 配置上游远程值

> [!IMPORTANT]
> 如果要对文章进行次要更改，无需完成本文中的相关步骤  。 可直接转到[快速更改工作流](index.md#quick-edits-to-existing-documents)。
>

## <a name="overview"></a>概述

要为 Microsoft 文档站点供稿，可以通过克隆相应的文档存储库在本地创建和编辑 Markdown 文件。 Microsoft 要求你在自己的 GitHub 帐户创建相应的存储库分支，以便在其中具有读/写权限来存储建议的更改。 然后，使用拉取请求将更改合并到只读的中央共享存储库。

![GitHub 三角形](./media/git-and-github-initial-setup.png)

如果你刚接触 GitHub，请观看以下视频，了解创建分支和克隆过程的概念性概述：

>[!VIDEO https://channel9.msdn.com/Blogs/CoolMoose/Git-Repository-Setup/player]

## <a name="determine-the-repository"></a>确定存储库

在 [docs.microsoft.com](https://docs.microsoft.com) 上托管的文档驻留在 [github.com](https://www.github.com) 上的多个不同存储库中。

1. 如果不确定要使用的存储库，请使用 Web 浏览器访问 [docs.microsoft.com](https://docs.microsoft.com) 上的文章。 选择文章右上方的“编辑”  链接（铅笔图标）。

   ![单击“编辑”来确定存储库和文件位置。](media/index/edit-article.png)

2. 该链接会将你带到 github.com 位置，以获取相应存储库中对应的 Markdown 文件。 请注意用于查看存储库名称的 URL。

   ![请注意用于确定存储库位置的 URL。](media/public-repo.png)

   例如，这些常用的存储库可用于下列公开发表的内容：
   - Azure 文档 [https://github.com/MicrosoftDocs/azure-docs](https://github.com/MicrosoftDocs/azure-docs)
   - SQL Server 文档 [https://github.com/MicrosoftDocs/sql-docs](https://github.com/MicrosoftDocs/sql-docs)
   - Visual Studio 文档 [https://github.com/MicrosoftDocs/visualstudio-docs](https://github.com/MicrosoftDocs/visualstudio-docs)
   - .NET 文档 [https://github.com/dotnet/docs](https://github.com/dotnet/docs)
   - Azure .Net SDK 文档 [https://github.com/azure/azure-docs-sdk-dotnet](https://github.com/azure/azure-docs-sdk-dotnet)
   - ConfigMgr 文档 [https://github.com/MicrosoftDocs/SCCMdocs](https://github.com/MicrosoftDocs/SCCMdocs/)

## <a name="fork-the-repository"></a>为存储库创建分支
使用合适的存储库，通过 GitHub 网站，将存储库的一个分支创建到自己的 GitHub 帐户中。

由于所有主文档存储库均提供只读访问权限，因此需具备个人分支。 要进行更改，必须将[拉取请求](git-github-fundamentals.md#pull-requests)从自己的分支提交到存储库。 为推进此过程，首先需要自己拥有一个存储库副本并对其具有写入权限。 GitHub 分支就很适合该用途  。

1. 转到主存储库的 GitHub 页面，然后单击右上角的“创建分支”按钮  。

   ![GitHub 个人资料示例](./media/contribute-get-started-setup-local/fork.png)

2. 如果出现提示，请选择 GitHub 帐户磁贴作为创建分支的目标位置。 此提示在 GitHub 帐户中创建存储库的副本，也就是分支。

## <a name="choose-a-local-folder"></a>选择本地文件夹
将存储库的副本保存在本地文件夹中。 有些存储库可能会很大；例如，azure-docs，最高可达 5 GB。 选择具有可用磁盘空间的位置。

1. 所选的文件夹名称应便于记忆和键入。 例如，将根文件夹设为 `C:\docs\` 或在用户配置文件目录 `~/Documents/docs/` 中创建文件夹

   > [!IMPORTANT]
   > 避免选择嵌套在另一个 git 存储库文件夹位置内的本地文件夹路径。 尽管可以将 git 克隆文件夹存储在另一个文件夹旁边，但将 git 文件夹嵌套在另一个文件夹内会导致文件跟踪错误。

2. 启动 Git Bash

   ![启动 Git Bash](./media/contribute-get-started-setup-local/gitbash-start.png)

   Git Bash 启动的默认位置通常都在主目录 (~) 或在 Windows OS 上的 `/c/users/<Windows-user-account>/`。

   要确定当前目录，请在 $ 提示符处键入 `pwd`。 

3. 将目录更改为创建用于在本地托管存储库的的文件夹。 请注意，Git Bash 的文件夹路径使用正斜杠的 Linux 约定，而不是反斜杠。

   例如，`cd /c/docs/ ` 或 `cd ~/Documents/docs/`

## <a name="create-a-local-clone"></a>创建本地克隆

使用 Git Bash，准备运行 clone 命令，将存储库（分支）副本下载到当前目录上的设备  。 

### <a name="authenticate-by-using-git-credential-manager"></a>使用 Git 凭据管理器进行身份验证
如果安装了适用于 Windows 的 Git 的最新版本并接受了默认安装，则默认启用 Git 凭据管理器。 Git 凭据管理器使身份验证更加简便，因为在使用 GitHub 重新建立经过身份验证的连接和远程时，不需要撤回个人访问令牌。

1. 通过提供存储库名称来运行 clone 命令  。 克隆在本地计算机上下载（克隆）分支存储库。 

    > [!Tip]
    > 可以通过 GitHub UI 中的“克隆或下载”按钮获取分支的克隆命令的 GitHub URL  ：
    >
    > ![克隆或下载](./media/contribute-get-started-setup-local/clone-or-download.png)

    确保在克隆期间指定分支的路径，而不是在其中创建分支的主存储库  。 否则，无法提供更改。 通过个人 GitHub 用户帐户引用分支，例如 `github.com/<github-username>/<repo>`。

    ```bash
    git clone https://github.com/<github-username>/<repo>.git
    ```

    克隆命令应类似于以下示例：

    ```bash
    git clone https://github.com/smithj/azure-docs.git
    ```

2. 在系统提示时输入 GitHub 凭据。

    ![GitHub 登录](./media/contribute-get-started-setup-local/github-login.png)

3. 在系统提示时输入双因素身份验证代码。

    ![GitHub 双因素身份验证](./media/contribute-get-started-setup-local/github-2fa.png)

    > [!Note]
    > 凭据将进行保存并用于对未来的 GitHub 请求进行身份验证。 每台计算机仅需执行此身份验证一次。 

4. 克隆命令运行分支的存储库文件副本并将其下载到本地磁盘上的新文件夹中。 在当前文件夹中创建新的文件夹。 这可能需要花费几分钟，具体取决于存储库大小。 可以浏览文件夹，查看完成后的结构。

## <a name="configure-remote-upstream"></a>配置远程上游
克隆存储库后，为名为“上游”的主存储库设置只读的远程连接  。 利用此上游 URL，使本地存储库与其他人所做的最新更改保持同步。 git remote 命令用于设值配置值  。 使用 fetch 命令从上游存储库刷新分支信息  。

1. 如果使用的是 Git 凭据管理器，请使用以下命令  。 替换 \<repo\> 和 \<organization\> 占位符。
   ```bash
   cd <repo>
   git remote add upstream https://github.com/<organization>/<repo>.git
   git fetch upstream
   ```

2. 查看配置值并确认 URL 是正确的。 确保“源”URL 指向个人分支  。 确保“上游”URL 指向主存储库，例如 MicrosoftDocs 或 Azure  。 
   ```bash
   git remote -v 
   ```

   显示远程输出示例。 名为 MyGitAccount 的虚构 git 帐户配置了个人访问令牌来访问存储库 azure-docs：
   ```output
   origin  https://github.com/MyGitAccount/azure-docs.git (fetch)
   origin  https://github.com/MyGitAccount/azure-docs.git(push)
   upstream        https://github.com/MicrosoftDocs/azure-docs.git (fetch)
   upstream        https://github.com/MicrosoftDocs/azure-docs.git (push)
   ```

3. 如果出错，可以删除远程值。 要删除上游值，请运行命令 `git remote remove upstream`。

## <a name="next-steps"></a>后续步骤
- 了解有关添加和更新内容的详细信息，请继续访问 [GitHub 参与工作流](how-to-write-workflows-major.md)。
