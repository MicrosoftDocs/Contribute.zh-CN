---
ms.openlocfilehash: fa7cd177f6c4a3c4862677dbfa89f63a91e7f464
ms.sourcegitcommit: 42e5a6ae071826afc2a32a9b7150ca113b39afdf
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/19/2019
ms.locfileid: "57987804"
---
# <a name="tabbed-conceptual"></a><span data-ttu-id="3f09a-101">选项卡式概念</span><span class="sxs-lookup"><span data-stu-id="3f09a-101">Tabbed conceptual</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3f09a-102">选项卡式概念语法已弃用，不得添加新选项卡。</span><span class="sxs-lookup"><span data-stu-id="3f09a-102">The tabbed conceptual syntax has been deprecated and new tabs should not be added.</span></span> <span data-ttu-id="3f09a-103">本文中描述的验证适用于已获准使用选项卡式概念（在出现可用的替换功能之前）的内容集。</span><span class="sxs-lookup"><span data-stu-id="3f09a-103">The validations described in this article apply to content sets that have been approved to use tabbed conceptual until replacement functionality is available.</span></span>

## <a name="tab-syntax"></a><span data-ttu-id="3f09a-104">选项卡语法</span><span class="sxs-lookup"><span data-stu-id="3f09a-104">Tab syntax</span></span>

<span data-ttu-id="3f09a-105">选项卡的语法如下所示：</span><span class="sxs-lookup"><span data-stu-id="3f09a-105">The syntax for tabs is as follows:</span></span>

<span data-ttu-id="3f09a-106">单级别选项卡：</span><span class="sxs-lookup"><span data-stu-id="3f09a-106">Single level tab:</span></span>

`# [Tab Display Name](#tab/tab-id)`

<span data-ttu-id="3f09a-107">可选依赖选项卡：</span><span class="sxs-lookup"><span data-stu-id="3f09a-107">Optional dependent tab:</span></span>

`# [Tab Display Name](#tab/tab-id/tab-condition)`

<span data-ttu-id="3f09a-108">具有两个选项卡和选项卡组终止符 (---) 的单级别选项卡分区示例：</span><span class="sxs-lookup"><span data-stu-id="3f09a-108">Example of a single-level tab section with two tabs and the tab group terminator (---):</span></span>

```markdown
# [Linux](#tab/linux)

Content for Linux...

# [Windows](#tab/windows)

Content for Windows...

---
```

<span data-ttu-id="3f09a-109">可选择选项卡中是否包含辅助选项卡或依赖选项卡。</span><span class="sxs-lookup"><span data-stu-id="3f09a-109">Tabs can optionally contain secondary tabs, or dependency tabs.</span></span> <span data-ttu-id="3f09a-110">如果包含，则选项卡将依赖于另一组选项卡的选择。</span><span class="sxs-lookup"><span data-stu-id="3f09a-110">This makes tabs dependent on the selection in another set of tabs.</span></span> <span data-ttu-id="3f09a-111">示例如下：</span><span class="sxs-lookup"><span data-stu-id="3f09a-111">Here's an example:</span></span>

```markdown
# [Azure CLI](#tab/azure-cli/linux)

Azure CLI content for Linux...

# [Azure CLI](#tab/azure-cli/windows)

Azure CLI content for Windows...

# [PowerShell](#tab/azure-powershell/linux)

PowerShell content for Linux...

# [PowerShell](#tab/azure-powershell/windows)

PowerShell content for Windows...

---
```

<span data-ttu-id="3f09a-112">以下验证适用于选项卡语法：</span><span class="sxs-lookup"><span data-stu-id="3f09a-112">The following validations apply to tab syntax:</span></span>

- <span data-ttu-id="3f09a-113">选项卡语法必须正确。</span><span class="sxs-lookup"><span data-stu-id="3f09a-113">Tab syntax must be correct.</span></span>
- <span data-ttu-id="3f09a-114">必须在先前的选项卡组中定义依赖选项卡。</span><span class="sxs-lookup"><span data-stu-id="3f09a-114">Dependent tabs must have been defined in a previous tab group.</span></span>
- <span data-ttu-id="3f09a-115">只允许一个级别的依赖项。</span><span class="sxs-lookup"><span data-stu-id="3f09a-115">Only one level of dependency is allowed.</span></span>
- <span data-ttu-id="3f09a-116">允许的选项卡数量不得少于 2 个。</span><span class="sxs-lookup"><span data-stu-id="3f09a-116">No fewer than two tabs are allowed.</span></span>
- <span data-ttu-id="3f09a-117">允许的选项卡数量不得超过 4 个。</span><span class="sxs-lookup"><span data-stu-id="3f09a-117">No more than four tabs are allowed.</span></span>
- <span data-ttu-id="3f09a-118">必须批准选项卡。</span><span class="sxs-lookup"><span data-stu-id="3f09a-118">Tabs must be approved.</span></span>
- <span data-ttu-id="3f09a-119">选项卡/ID 对必须有效。</span><span class="sxs-lookup"><span data-stu-id="3f09a-119">Tab/ID pairs must be valid.</span></span>
- <span data-ttu-id="3f09a-120">一个选项卡组中不能多次使用同一选项卡 ID。</span><span class="sxs-lookup"><span data-stu-id="3f09a-120">Cannot have the same tab ID multiple times in one tab group.</span></span>

## <a name="approved-tabs"></a><span data-ttu-id="3f09a-121">已批准的选项卡</span><span class="sxs-lookup"><span data-stu-id="3f09a-121">Approved tabs</span></span>

<span data-ttu-id="3f09a-122">已批准以下选项卡名称/选项卡 ID 对。</span><span class="sxs-lookup"><span data-stu-id="3f09a-122">The following tab name/tab ID pairs are approved.</span></span> <span data-ttu-id="3f09a-123">依赖选项卡 ID 未配对，但根据选项卡 ID 列，其必定有效。</span><span class="sxs-lookup"><span data-stu-id="3f09a-123">Dependent tab IDs are not paired but must be valid per the Tab ID column.</span></span> <span data-ttu-id="3f09a-124">这些值区分大小写</span><span class="sxs-lookup"><span data-stu-id="3f09a-124">The values are case-sensitive</span></span>

|<span data-ttu-id="3f09a-125">选项卡名称</span><span class="sxs-lookup"><span data-stu-id="3f09a-125">Tab name</span></span>              |<span data-ttu-id="3f09a-126">选项卡 ID</span><span class="sxs-lookup"><span data-stu-id="3f09a-126">Tab ID</span></span>            |
|----------------------|------------------|
|`[.NET]`              |`(#tab/dotnet)`   |
|`[.NET Core 1.x]`     |`(#tab/netcore1x)`|
|`[.NET Core 2.x]`     |`(#tab/netcore2x)`|
|`[.NET Core 2.0]`     |`(#tab/netcore20)`|
|`[.NET Core 2.1]`     |`(#tab/netcore21)`|
|`[.NET Core 2.2]`     |`(#tab/netcore22)`|
|`[.NET Core 3.x]`     |`(#tab/netcore3x)`|
|`[.NET Core 3.0]`     |`(#tab/netcore30)`|
|`[.NET Core CLI]`     |`(#tab/netcore-cli)`|
|`[Azure CLI]`         |`(#tab/azure-cli)`|
|`[Android]`           |`(#tab/android)`  |
|`[Browser]`           |`(#tab/browser)`  |
|`[C#]`                |`(#tab/csharp)`   |
|`[C# Script]`         |`(#tab/csharp-script)`|
|`[CentOS]`            |`(#tab/centos)`|
|`[Command Line]`      |`(#tab/command-line)`|
|`[Debian]`            |`(#tab/debian)`|
|`[Docker Hub]`        |`(#tab/docker-hub)`|
|`[F#]`                |`(#tab/fsharp)`|
|`[Fedora]`            |`(#tab/fedora)`|
|`[iOS]`               |`(#tab/ios)`      |
|`[Java]`              |`(#tab/java)`|
|`[JavaScript]`        |`(#tab/javascript)`|
|`[Linux]`             |`(#tab/linux)`    |
|`[macOS]`             |`(#tab/macos)`    |
|`[Managed Kubernetes]`|`(#tab/kubernetes-managed)`|
|`[Maven]`             |`(#tab/maven)`|
|`[Mint]`              |`(#tab/mint)`|
|`[Node.js]`           |`(#tab/nodejs)`|
|`[npm]`               |`(#tab/npm)` |
|`[NuGet]`             |`(#tab/nuget)`|
|`[openSUSE]`          |`(#tab/opensuse)`|
|`[Other]`             |`(#tab/other)` |
|`[Oracle Linux]`      |`(#tab/oracle-linux)`|
|`[Package Manager]`   |`(#tab/package-manager)` |
|`[PEAR]`              |`(#tab/pear)`|
|`[pip]`               |`(#tab/pip)`|
|`[Portal]`            |`(#tab/azure-portal)`    |
|`[PowerShell]`        |`(#tab/azure-powershell)`|
|`[Private Registry]`  |`(#tab/private-registry)`|
|`[Python]`            |`(#tab/python)`|
|`[Resource Manager Template]`|`(#tab/azure-resource-manager)`|
|`[RHEL]`              |`(#tab/rhel)`|
|`[RubyGems]`          |`(#tab/rubygems)`|
|`[SQL Server]`        |`(#tab/sql-server)`|
|`[SQLite]`            |`(#tab/sqlite)`|
|`[TypeScript]`        |`(#tab/typescript)`|
|`[Visual Basic]`      |`(#tab/vb)` |
|`[Visual Studio]`     |`(#tab/visual-studio)`|
|`[Visual Studio 15.6 and earlier]`|`(#tab/vs156)`|
|`[Visual Studio 15.7 and later]`  |`(#tab/vs157)`|
|`[Visual Studio Code]`            |`(#tab/visual-studio-code)`|
|`[Visual Studio for Mac]`         |`(#tab/visual-studio-mac)`|
|`[Ubuntu]`                        |`(#tab/ubuntu)`|
|`[Unmanaged Kubernetes]`          |`(#tab/kubernetes-unmanaged)`|
|`[Windows]`   |`(#tab/windows)`   |