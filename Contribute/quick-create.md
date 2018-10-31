---
title: 快速入门：在 Azure Key Vault 中设置和检索机密 | Microsoft Docs
description: 快速入门：在 Azure Key Vault 中设置和检索机密
services: key-vault
author: syntaxc4
manager: erifkin
ms.date: 07/24/2018
ms.author: cfowler
zone_pivot_groups: keyvault-languages
ROBOTS: NOINDEX, NOFOLLOW
ms.openlocfilehash: 497631fe46ac4e2c9c495a609547753a84d662bf
ms.sourcegitcommit: d3c7b49dc854dae8da9cd49da8ac4035789a5010
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/23/2018
ms.locfileid: "49805720"
---
# <a name="quickstart-set-and-retrieve-a-secret-from-azure-key-vault"></a><span data-ttu-id="92434-103">快速入门：在 Azure Key Vault 中设置和检索机密</span><span class="sxs-lookup"><span data-stu-id="92434-103">Quickstart: Set and retrieve a secret from Azure Key Vault</span></span>

<span data-ttu-id="92434-104">本快速入门介绍如何在 Key Vault 中存储机密，以及如何使用 Web 应用来检索它。</span><span class="sxs-lookup"><span data-stu-id="92434-104">This quickstart shows you how to store a secret in Key Vault and how to retrieve it using a Web app.</span></span> <span data-ttu-id="92434-105">若要查看机密值，必须在 Azure 上运行此应用。</span><span class="sxs-lookup"><span data-stu-id="92434-105">To see the secret value you would have to run this on Azure.</span></span> <span data-ttu-id="92434-106">本快速入门使用 Node.js 和托管服务标识 (MSI)。</span><span class="sxs-lookup"><span data-stu-id="92434-106">The quickstart uses Node.js and Managed service identities (MSIs).</span></span>

> [!div class="checklist"]
> * <span data-ttu-id="92434-107">创建 Key Vault。</span><span class="sxs-lookup"><span data-stu-id="92434-107">Create a Key Vault.</span></span>
> * <span data-ttu-id="92434-108">在 Key Vault 中存储机密。</span><span class="sxs-lookup"><span data-stu-id="92434-108">Store a secret in the Key Vault.</span></span>
> * <span data-ttu-id="92434-109">从 Key Vault 检索机密。</span><span class="sxs-lookup"><span data-stu-id="92434-109">Retrieve a secret from Key Vault.</span></span>
> * <span data-ttu-id="92434-110">创建 Azure Web 应用程序。</span><span class="sxs-lookup"><span data-stu-id="92434-110">Create an Azure Web Application.</span></span>
> * <span data-ttu-id="92434-111">[启用托管服务标识](https://docs.microsoft.com/azure/active-directory/managed-service-identity/overview)。</span><span class="sxs-lookup"><span data-stu-id="92434-111">[Enable managed service identities](https://docs.microsoft.com/azure/active-directory/managed-service-identity/overview).</span></span>
> * <span data-ttu-id="92434-112">授予所需的权限，让 Web 应用程序从 Key Vault 读取数据。</span><span class="sxs-lookup"><span data-stu-id="92434-112">Grant the required permissions for the web application to read data from Key vault.</span></span>

<span data-ttu-id="92434-113">在继续操作之前，请确保熟悉[基本概念](https://docs.microsoft.com/azure/key-vault/key-vault-whatis#basic-concepts)。</span><span class="sxs-lookup"><span data-stu-id="92434-113">Before you proceed make sure that you are familiar with the [basic concepts](https://docs.microsoft.com/azure/key-vault/key-vault-whatis#basic-concepts).</span></span>

> [!NOTE]
> <span data-ttu-id="92434-114">若要理解为什么以下教程是最佳做法，我们需要了解一些概念。</span><span class="sxs-lookup"><span data-stu-id="92434-114">To understand why the below tutorial is the best practice we need to understand a few concepts.</span></span> <span data-ttu-id="92434-115">Key Vault 是一个以编程方式存储机密的中央存储库。</span><span class="sxs-lookup"><span data-stu-id="92434-115">Key Vault is a central repository to store secrets programmatically.</span></span> <span data-ttu-id="92434-116">但要这样做，应用程序/用户需要首先向 Key Vault 进行身份验证，即提供机密。</span><span class="sxs-lookup"><span data-stu-id="92434-116">But to do so applications / users need to first authenticate to Key Vault i.e. present a secret.</span></span> <span data-ttu-id="92434-117">为了遵循安全最佳做法，第一个机密也需要定期轮换。</span><span class="sxs-lookup"><span data-stu-id="92434-117">To follow security best practices this first secret needs to be rotated periodically as well.</span></span> <span data-ttu-id="92434-118">但是，使用 [托管服务标识](https://docs.microsoft.com/azure/active-directory/managed-service-identity/overview)，在 Azure 中运行的应用程序将获得由 Azure 自动管理的标识。</span><span class="sxs-lookup"><span data-stu-id="92434-118">But with [Managed Service Identity](https://docs.microsoft.com/azure/active-directory/managed-service-identity/overview), applications that run in Azure are given an identity which is automatically managed by Azure.</span></span> <span data-ttu-id="92434-119">这有助于解决机密采用问题，其中用户/应用程序可以遵循最佳做法，而不必担心轮换第一个机密</span><span class="sxs-lookup"><span data-stu-id="92434-119">This helps solve the **Secret Introduction Problem** where users / applications can follow best practices and not have to worry about rotating the first secret</span></span>

## <a name="prerequisites"></a><span data-ttu-id="92434-120">先决条件</span><span class="sxs-lookup"><span data-stu-id="92434-120">Prerequisites</span></span>

::: zone pivot="nodejs"
* [<span data-ttu-id="92434-121">Node JS</span><span class="sxs-lookup"><span data-stu-id="92434-121">Node JS</span></span>](https://nodejs.org/en/)
::: zone-end
::: zone pivot="dotnet"
* <span data-ttu-id="92434-122">[Visual Studio 2017 版本 15.7.3 或更高版本](https://www.microsoft.com/net/download/windows)，其中包含以下工作负载：</span><span class="sxs-lookup"><span data-stu-id="92434-122">[Visual Studio 2017 version 15.7.3 or later](https://www.microsoft.com/net/download/windows) with the following workloads:</span></span>
  * <span data-ttu-id="92434-123">ASP.NET 和 Web 开发</span><span class="sxs-lookup"><span data-stu-id="92434-123">ASP.NET and web development</span></span>
  * <span data-ttu-id="92434-124">.NET Core 跨平台开发</span><span class="sxs-lookup"><span data-stu-id="92434-124">.NET Core cross-platform development</span></span>
* [<span data-ttu-id="92434-125">.NET Core 2.1 SDK 或更高版本</span><span class="sxs-lookup"><span data-stu-id="92434-125">.NET Core 2.1 SDK or later</span></span>](https://www.microsoft.com/net/download/windows)
::: zone-end
* <span data-ttu-id="92434-126">Git（[下载](https://git-scm.com/downloads)）。</span><span class="sxs-lookup"><span data-stu-id="92434-126">Git ([download](https://git-scm.com/downloads)).</span></span>
* <span data-ttu-id="92434-127">Azure 订阅。</span><span class="sxs-lookup"><span data-stu-id="92434-127">An Azure subscription.</span></span> <span data-ttu-id="92434-128">如果没有 Azure 订阅，请在开始之前创建一个[免费帐户](https://azure.microsoft.com/free/?WT.mc_id=A261C142F)。</span><span class="sxs-lookup"><span data-stu-id="92434-128">If you don't have an Azure subscription, create a [free account](https://azure.microsoft.com/free/?WT.mc_id=A261C142F) before you begin.</span></span>
* <span data-ttu-id="92434-129">[Azure CLI](https://docs.microsoft.com/cli/azure/install-azure-cli?view=azure-cli-latest) 版本 2.0.4 或更高版本。</span><span class="sxs-lookup"><span data-stu-id="92434-129">[Azure CLI](https://docs.microsoft.com/cli/azure/install-azure-cli?view=azure-cli-latest) version 2.0.4 or later.</span></span> <span data-ttu-id="92434-130">适用于 Windows、Mac 和 Linux。</span><span class="sxs-lookup"><span data-stu-id="92434-130">This is available for Windows, Mac, and Linux.</span></span>

## <a name="login-to-azure"></a><span data-ttu-id="92434-131">登录到 Azure</span><span class="sxs-lookup"><span data-stu-id="92434-131">Login to Azure</span></span>

<span data-ttu-id="92434-132">若要使用 CLI 登录到 Azure，可以键入：</span><span class="sxs-lookup"><span data-stu-id="92434-132">To log in to Azure using the CLI, you can type:</span></span>

```azurecli
az login
```

## <a name="create-resource-group"></a><span data-ttu-id="92434-133">创建资源组</span><span class="sxs-lookup"><span data-stu-id="92434-133">Create resource group</span></span>

<span data-ttu-id="92434-134">运行 [az group create](/cli/azure/group#az-group-create) 命令，以创建资源组。</span><span class="sxs-lookup"><span data-stu-id="92434-134">Create a resource group with the [az group create](/cli/azure/group#az-group-create) command.</span></span> <span data-ttu-id="92434-135">Azure 资源组是逻辑容器，可在其中部署和管理 Azure 资源。</span><span class="sxs-lookup"><span data-stu-id="92434-135">An Azure resource group is a logical container into which Azure resources are deployed and managed.</span></span>

<span data-ttu-id="92434-136">请选择一个资源组名称，然后将其填充在占位符中。</span><span class="sxs-lookup"><span data-stu-id="92434-136">Please select a Resource Group name and fill in the placeholder.</span></span>
<span data-ttu-id="92434-137">以下示例在 eastus 位置创建名为 <YourResourceGroupName> 的资源组。</span><span class="sxs-lookup"><span data-stu-id="92434-137">The following example creates a resource group named *<YourResourceGroupName>* in the *eastus* location.</span></span>

```azurecli
# To list locations: az account list-locations --output table
az group create --name "<YourResourceGroupName>" --location "East US"
```

<span data-ttu-id="92434-138">刚刚创建的资源组将在整篇教程中使用。</span><span class="sxs-lookup"><span data-stu-id="92434-138">The resource group you just created is used throughout this tutorial.</span></span>

## <a name="create-an-azure-key-vault"></a><span data-ttu-id="92434-139">创建 Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="92434-139">Create an Azure Key Vault</span></span>

<span data-ttu-id="92434-140">接下来，在上一步创建的资源组中创建 Key Vault。</span><span class="sxs-lookup"><span data-stu-id="92434-140">Next you create a Key Vault using the resource group created in the previous step.</span></span> <span data-ttu-id="92434-141">尽管本文中使用“ContosoKeyVault”作为 Key Vault 的名称，但你必须使用唯一名称。</span><span class="sxs-lookup"><span data-stu-id="92434-141">Although “ContosoKeyVault” is used as the name for the Key Vault throughout this article, you have to use a unique name.</span></span> <span data-ttu-id="92434-142">提供以下信息：</span><span class="sxs-lookup"><span data-stu-id="92434-142">Provide the following information:</span></span>

* <span data-ttu-id="92434-143">保管库名称 - 在此处选择一个 Key Vault 名称。</span><span class="sxs-lookup"><span data-stu-id="92434-143">Vault name - **Select a Key Vault Name here**.</span></span>
* <span data-ttu-id="92434-144">资源组名称 - 在此处选择一个资源组名称。</span><span class="sxs-lookup"><span data-stu-id="92434-144">Resource group name - **Select a Resource Group Name here**.</span></span>
* <span data-ttu-id="92434-145">位置 -“美国东部”。</span><span class="sxs-lookup"><span data-stu-id="92434-145">The location - **East US**.</span></span>

```azurecli
az keyvault create --name "<YourKeyVaultName>" --resource-group "<YourResourceGroupName>" --location "East US"
```

<span data-ttu-id="92434-146">目前，只有你的 Azure 帐户才有权对这个新保管库执行任何操作。</span><span class="sxs-lookup"><span data-stu-id="92434-146">At this point, your Azure account is the only one authorized to perform any operations on this new vault.</span></span>

## <a name="add-a-secret-to-key-vault"></a><span data-ttu-id="92434-147">向 Key Vault 添加机密</span><span class="sxs-lookup"><span data-stu-id="92434-147">Add a secret to key vault</span></span>

<span data-ttu-id="92434-148">我们将添加机密以帮助说明这是如何工作的。</span><span class="sxs-lookup"><span data-stu-id="92434-148">We're adding a secret to help illustrate how this works.</span></span> <span data-ttu-id="92434-149">可以存储需要安全保存但同时也可供应用程序使用的 SQL 连接字符串或其他任何信息。</span><span class="sxs-lookup"><span data-stu-id="92434-149">You could be storing a SQL connection string or any other information that you need to keep securely but make available to your application.</span></span> <span data-ttu-id="92434-150">在本教程中，密码名为 AppSecret，将在其中存储 MySecret 的值。</span><span class="sxs-lookup"><span data-stu-id="92434-150">In this tutorial, the password will be called **AppSecret** and will store the value of **MySecret** in it.</span></span>

<span data-ttu-id="92434-151">键入以下命令，在 Key Vault 中创建名为 AppSecret 的机密，用于存储 MySecret 值：</span><span class="sxs-lookup"><span data-stu-id="92434-151">Type the commands below to create a secret in Key Vault called **AppSecret** that will store the value **MySecret**:</span></span>

```azurecli
az keyvault secret set --vault-name "<YourKeyVaultName>" --name "AppSecret" --value "MySecret"
```

<span data-ttu-id="92434-152">若要查看机密中包含的纯文本形式的值，请执行以下命令：</span><span class="sxs-lookup"><span data-stu-id="92434-152">To view the value contained in the secret as plain text:</span></span>

```azurecli
az keyvault secret show --name "AppSecret" --vault-name "<YourKeyVaultName>"
```

<span data-ttu-id="92434-153">此命令显示机密信息，包括 URI。</span><span class="sxs-lookup"><span data-stu-id="92434-153">This command shows the secret information including the URI.</span></span> <span data-ttu-id="92434-154">完成这些步骤后，Azure Key Vault 中应会出现某个机密的 URI。</span><span class="sxs-lookup"><span data-stu-id="92434-154">After completing these steps, you should have a URI to a secret in an Azure Key Vault.</span></span> <span data-ttu-id="92434-155">请记下此信息。</span><span class="sxs-lookup"><span data-stu-id="92434-155">Write this information down.</span></span> <span data-ttu-id="92434-156">后面的步骤需要用到。</span><span class="sxs-lookup"><span data-stu-id="92434-156">You need it in a later step.</span></span>

## <a name="clone-the-repo"></a><span data-ttu-id="92434-157">克隆存储库</span><span class="sxs-lookup"><span data-stu-id="92434-157">Clone the Repo</span></span>

<span data-ttu-id="92434-158">运行以下命令，以便克隆存储库，为你创建一个用于编辑源的本地副本：</span><span class="sxs-lookup"><span data-stu-id="92434-158">Clone the repo in order to make a local copy for you to edit the source by running the following command:</span></span>

```bash
git clone https://github.com/Azure-Samples/key-vault-node-quickstart.git
```

::: zone pivot="nodejs"

## <a name="install-dependencies"></a><span data-ttu-id="92434-159">安装依赖项</span><span class="sxs-lookup"><span data-stu-id="92434-159">Install dependencies</span></span>

<span data-ttu-id="92434-160">在这里，我们安装依赖项。</span><span class="sxs-lookup"><span data-stu-id="92434-160">Here we install the dependencies.</span></span> <span data-ttu-id="92434-161">运行以下命令：</span><span class="sxs-lookup"><span data-stu-id="92434-161">Run the following commands:</span></span>

    cd key-vault-node-quickstart
    npm install

<span data-ttu-id="92434-162">此项目使用 2 个节点模块：</span><span class="sxs-lookup"><span data-stu-id="92434-162">This project used 2 node modules:</span></span>

* [<span data-ttu-id="92434-163">ms-rest-azure</span><span class="sxs-lookup"><span data-stu-id="92434-163">ms-rest-azure</span></span>](https://www.npmjs.com/package/ms-rest-azure) 
* [<span data-ttu-id="92434-164">azure-keyvault</span><span class="sxs-lookup"><span data-stu-id="92434-164">azure-keyvault</span></span>](https://www.npmjs.com/package/azure-keyvault)

## <a name="publish-the-web-application-to-azure"></a><span data-ttu-id="92434-165">将 Web 应用程序发布到 Azure</span><span class="sxs-lookup"><span data-stu-id="92434-165">Publish the web application to Azure</span></span>

<span data-ttu-id="92434-166">将应用程序发布到 Azure 需执行以下几个步骤。</span><span class="sxs-lookup"><span data-stu-id="92434-166">Below are the few steps we need to do to publish the application to Azure.</span></span>

* <span data-ttu-id="92434-167">第一步是创建 [Azure 应用服务](https://azure.microsoft.com/services/app-service/)计划。</span><span class="sxs-lookup"><span data-stu-id="92434-167">The 1st step is to create a [Azure App Service](https://azure.microsoft.com/services/app-service/) Plan.</span></span> <span data-ttu-id="92434-168">可以在此计划中存储多个 Web 应用。</span><span class="sxs-lookup"><span data-stu-id="92434-168">You can store multiple web apps in this plan.</span></span>

    ```azurecli
    az appservice plan create --name myAppServicePlan --resource-group myResourceGroup
    ```
* <span data-ttu-id="92434-169">接下来创建 Web 应用。</span><span class="sxs-lookup"><span data-stu-id="92434-169">Next we create a web app.</span></span> <span data-ttu-id="92434-170">在以下示例中，将 <app_name> 替换为全局唯一的应用名称（有效字符为 a-z、0-9 和 -）。</span><span class="sxs-lookup"><span data-stu-id="92434-170">In the following example, replace <app_name> with a globally unique app name (valid characters are a-z, 0-9, and -).</span></span> <span data-ttu-id="92434-171">运行时设置为 NODE|6.9。</span><span class="sxs-lookup"><span data-stu-id="92434-171">The runtime is set to NODE|6.9.</span></span> <span data-ttu-id="92434-172">若要查看所有受支持的运行时，请运行 `az webapp list-runtimes`</span><span class="sxs-lookup"><span data-stu-id="92434-172">To see all supported runtimes, run `az webapp list-runtimes`</span></span>

    ```azurecli
    az webapp create --resource-group myResourceGroup --plan myAppServicePlan --name <app_name> --runtime "NODE|6.9" --deployment-local-git
    ```

    <span data-ttu-id="92434-173">创建 Web 应用后，Azure CLI 会显示类似于以下示例的输出：</span><span class="sxs-lookup"><span data-stu-id="92434-173">When the web app has been created, the Azure CLI shows output similar to the following example:</span></span>

    ```json
    {
      "availabilityState": "Normal",
      "clientAffinityEnabled": true,
      "clientCertEnabled": false,
      "cloningInfo": null,
      "containerSize": 0,
      "dailyMemoryTimeQuota": 0,
      "defaultHostName": "<app_name>.azurewebsites.net",
      "enabled": true,
      "deploymentLocalGitUrl": "https://<username>@<app_name>.scm.azurewebsites.net/<app_name>.git"
      < JSON data removed for brevity. >
    }
    ```
    <span data-ttu-id="92434-174">浏览到新建的 Web 应用，此时会看到正在运行的 Web 应用。</span><span class="sxs-lookup"><span data-stu-id="92434-174">Browse to your newly created web app and you should see a functioning web app.</span></span> <span data-ttu-id="92434-175">将 <app_name> 替换为唯一的应用名称。</span><span class="sxs-lookup"><span data-stu-id="92434-175">Replace <app_name> with a unique app name.</span></span>

    ```text
    http://<app name>.azurewebsites.net
    ```
    <span data-ttu-id="92434-176">以上命令也创建一个支持 Git 的应用，该应用可以用来将内容从本地 Git 部署到 Azure。</span><span class="sxs-lookup"><span data-stu-id="92434-176">The above command also creates a Git-enabled app which allows you to deploy to azure from your local git.</span></span> 
    <span data-ttu-id="92434-177">本地 Git 配置了 URL“https://<username>@<app_name>.scm.azurewebsites.net/<app_name>.git”</span><span class="sxs-lookup"><span data-stu-id="92434-177">Local git is configured with url of 'https://<username>@<app_name>.scm.azurewebsites.net/<app_name>.git'</span></span>

* <span data-ttu-id="92434-178">创建部署用户：在完成上一命令以后，可以向本地 Git 存储库添加 Azure 远程功能。</span><span class="sxs-lookup"><span data-stu-id="92434-178">Create a deployment user After the previous command is completed you can add add an Azure remote to your local Git repository.</span></span> <span data-ttu-id="92434-179">使用从“启用应用的 Git”中获取的 Git 远程 URL 替换 <url>。</span><span class="sxs-lookup"><span data-stu-id="92434-179">Replace <url> with the URL of the Git remote that you got from Enable Git for your app.</span></span>

    ```bash
    git remote add azure <url>
    ```
    
::: zone-end

::: zone pivot="dotnet"
## <a name="open-and-edit-the-solution"></a><span data-ttu-id="92434-180">打开并编辑解决方案</span><span class="sxs-lookup"><span data-stu-id="92434-180">Open and edit the solution</span></span>

<span data-ttu-id="92434-181">编辑 program.cs 文件，以便使用特定的 Key Vault 名称运行示例：</span><span class="sxs-lookup"><span data-stu-id="92434-181">Edit the program.cs file to run the sample with your specific key vault name:</span></span>

1. <span data-ttu-id="92434-182">浏览到 key-vault-dotnet-core-quickstart 文件夹。</span><span class="sxs-lookup"><span data-stu-id="92434-182">Browse to the folder key-vault-dotnet-core-quickstart.</span></span>
2. <span data-ttu-id="92434-183">在 Visual Studio 2017 中打开 key-vault-dotnet-core-quickstart.sln 文件。</span><span class="sxs-lookup"><span data-stu-id="92434-183">Open the key-vault-dotnet-core-quickstart.sln file in Visual Studio 2017.</span></span>
3. <span data-ttu-id="92434-184">打开 Program.cs 文件，将占位符 YourKeyVaultName 更新为以前创建的 Key Vault 的名称。</span><span class="sxs-lookup"><span data-stu-id="92434-184">Open the Program.cs file and update the placeholder *YourKeyVaultName* with the name of your key vault that you created earlier.</span></span>

<span data-ttu-id="92434-185">此解决方案使用 [AppAuthentication](https://www.nuget.org/packages/Microsoft.Azure.Services.AppAuthentication) 和 [KeyVault](https://www.nuget.org/packages/Microsoft.Azure.KeyVault) NuGet 库。</span><span class="sxs-lookup"><span data-stu-id="92434-185">This solution uses [AppAuthentication](https://www.nuget.org/packages/Microsoft.Azure.Services.AppAuthentication) and [KeyVault](https://www.nuget.org/packages/Microsoft.Azure.KeyVault) NuGet libraries.</span></span>

## <a name="run-the-app"></a><span data-ttu-id="92434-186">运行应用</span><span class="sxs-lookup"><span data-stu-id="92434-186">Run the app</span></span>

<span data-ttu-id="92434-187">在 Visual Studio 2017 的主菜单中，选择“调试” > “开始执行(不调试)”。</span><span class="sxs-lookup"><span data-stu-id="92434-187">From the main menu of Visual Studio 2017, select **Debug** > **Start** without debugging.</span></span> <span data-ttu-id="92434-188">显示浏览器时，导航到“关于”页。</span><span class="sxs-lookup"><span data-stu-id="92434-188">When the browser appears, go to the **About** page.</span></span> <span data-ttu-id="92434-189">此时将显示 AppSecret 的值。</span><span class="sxs-lookup"><span data-stu-id="92434-189">The value for **AppSecret** is displayed.</span></span>

## <a name="publish-the-web-application-to-azure"></a><span data-ttu-id="92434-190">将 Web 应用程序发布到 Azure</span><span class="sxs-lookup"><span data-stu-id="92434-190">Publish the web application to Azure</span></span>

<span data-ttu-id="92434-191">我们要将此应用发布到 Azure，看其是否可以作为 Web 应用运行，并看我们能否提取机密值：</span><span class="sxs-lookup"><span data-stu-id="92434-191">Publish this app to Azure to see it live as a web app, and to see that you can fetch the secret value:</span></span>

1. <span data-ttu-id="92434-192">在 Visual Studio 中选择 key-vault-dotnet-core-quickstart 项目。</span><span class="sxs-lookup"><span data-stu-id="92434-192">In Visual Studio, select the **key-vault-dotnet-core-quickstart** project.</span></span>
2. <span data-ttu-id="92434-193">选择“发布” > “开始”。</span><span class="sxs-lookup"><span data-stu-id="92434-193">Select **Publish** > **Start**.</span></span>
3. <span data-ttu-id="92434-194">创建新的“应用服务”，然后选择“发布”。</span><span class="sxs-lookup"><span data-stu-id="92434-194">Create a new **App Service**, and then select **Publish**.</span></span>
4. <span data-ttu-id="92434-195">将应用名称更改为“keyvaultdotnetcorequickstart”。</span><span class="sxs-lookup"><span data-stu-id="92434-195">Change the app name to **keyvaultdotnetcorequickstart**.</span></span>
5. <span data-ttu-id="92434-196">选择“创建”。</span><span class="sxs-lookup"><span data-stu-id="92434-196">Select **Create**.</span></span>

>[!VIDEO https://sec.ch9.ms/ch9/e93d/a6ac417f-2e63-4125-a37a-8f34bf0fe93d/KeyVault_high.mp4]
::: zone-end

## <a name="enable-managed-service-identities"></a><span data-ttu-id="92434-197">启用托管服务标识</span><span class="sxs-lookup"><span data-stu-id="92434-197">Enable managed service identities</span></span>

<span data-ttu-id="92434-198">虽然 Azure Key Vault 可用于安全存储凭据以及其他密钥和机密，但代码需要通过 Azure Key Vault 的身份验证才能检索它们。</span><span class="sxs-lookup"><span data-stu-id="92434-198">Azure Key Vault provides a way to securely store credentials and other keys and secrets, but your code needs to authenticate to Azure Key Vault to retrieve them.</span></span> <span data-ttu-id="92434-199">托管服务标识为 Azure 服务提供了 Azure Active Directory (Azure AD) 中的自动托管标识，巧妙地解决了这个问题。</span><span class="sxs-lookup"><span data-stu-id="92434-199">Managed Service Identity makes this easier by giving Azure services an automatically managed identity in Azure Active Directory (Azure AD).</span></span> <span data-ttu-id="92434-200">此标识可用于通过支持 Azure AD 身份验证的任何服务（包括 Key Vault）的身份验证，这样就无需在代码中插入任何凭据了。</span><span class="sxs-lookup"><span data-stu-id="92434-200">You can use this identity to authenticate to any service that supports Azure AD authentication, including Key Vault, without having any credentials in your code.</span></span>

1. <span data-ttu-id="92434-201">返回 Azure CLI。</span><span class="sxs-lookup"><span data-stu-id="92434-201">Return to the Azure CLI.</span></span>
2. <span data-ttu-id="92434-202">运行 assign-identity 命令，为此应用程序创建标识：</span><span class="sxs-lookup"><span data-stu-id="92434-202">Run the assign-identity command to create the identity for this application:</span></span>

   ```azurecli
   az webapp identity assign --name "keyvaultdotnetcorequickstart" --resource-group "<YourResourceGroupName>"
   ```

>[!NOTE]
><span data-ttu-id="92434-203">此过程中的命令等同于转到门户并在 Web 应用程序属性中将“托管服务标识”切换为“打开”。</span><span class="sxs-lookup"><span data-stu-id="92434-203">The command in this procedure is the equivalent of going to the portal and switching **Managed service identity** to **On** in the web application properties.</span></span>

## <a name="assign-permissions-to-your-application-to-read-secrets-from-key-vault"></a><span data-ttu-id="92434-204">为应用程序分配从 Key Vault 读取机密的权限</span><span class="sxs-lookup"><span data-stu-id="92434-204">Assign permissions to your application to read secrets from Key Vault</span></span>

<span data-ttu-id="92434-205">请记下将应用程序发布到 Azure 时的输出。</span><span class="sxs-lookup"><span data-stu-id="92434-205">Make a note of the output when you publish the application to Azure.</span></span> <span data-ttu-id="92434-206">它应该采用以下格式：</span><span class="sxs-lookup"><span data-stu-id="92434-206">It should be of the format:</span></span>

```json
        {
          "principalId": "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx",
          "tenantId": "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx",
          "type": "SystemAssigned"
        }
```

<span data-ttu-id="92434-207">然后，使用 Key Vault 名称和 PrincipalId 值运行以下命令：</span><span class="sxs-lookup"><span data-stu-id="92434-207">Then, run this command by using the name of your key vault and the value of **PrincipalId**:</span></span>

```azurecli
az keyvault set-policy --name '<YourKeyVaultName>' --object-id <PrincipalId> --secret-permissions get
```

::: zone pivot="nodejs"
## <a name="deploy-the-node-app-to-azure-and-retrieve-the-secret-value"></a><span data-ttu-id="92434-208">将 Node 应用部署到 Azure，然后检索机密值</span><span class="sxs-lookup"><span data-stu-id="92434-208">Deploy the Node App to Azure and retrieve the secret value</span></span>

<span data-ttu-id="92434-209">现在，一切都已设置好。</span><span class="sxs-lookup"><span data-stu-id="92434-209">Now that everything is set.</span></span> <span data-ttu-id="92434-210">运行以下命令，将应用部署到 Azure</span><span class="sxs-lookup"><span data-stu-id="92434-210">Run the following command to deploy the app to Azure</span></span>

```bash
git push azure master
```

<span data-ttu-id="92434-211">然后，在浏览 https://<app_name>.azurewebsites.net 时，即可看到机密值。</span><span class="sxs-lookup"><span data-stu-id="92434-211">After this when you browse https://<app_name>.azurewebsites.net you can see the secret value.</span></span>
<span data-ttu-id="92434-212">请确保已将名称 <YourKeyVaultName> 替换为你的保管库名称</span><span class="sxs-lookup"><span data-stu-id="92434-212">Make sure that you replaced the name <YourKeyVaultName> with your vault name</span></span>

::: zone-end

::: zone pivot="dotnet"
<span data-ttu-id="92434-213">现在运行应用程序时，应该会看到检索到的机密值。</span><span class="sxs-lookup"><span data-stu-id="92434-213">Now when you run the application, you should see your secret value retrieved.</span></span>
::: zone-end

## <a name="next-steps"></a><span data-ttu-id="92434-214">后续步骤</span><span class="sxs-lookup"><span data-stu-id="92434-214">Next steps</span></span>

::: zone pivot="nodejs"
* [<span data-ttu-id="92434-215">Azure Key Vault 主页</span><span class="sxs-lookup"><span data-stu-id="92434-215">Azure Key Vault Home Page</span></span>](https://azure.microsoft.com/services/key-vault/)
* [<span data-ttu-id="92434-216">Azure Key Vault 文档</span><span class="sxs-lookup"><span data-stu-id="92434-216">Azure Key Vault Documentation</span></span>](https://docs.microsoft.com/azure/key-vault/)
* [<span data-ttu-id="92434-217">用于 Node 的 Azure SDK</span><span class="sxs-lookup"><span data-stu-id="92434-217">Azure SDK For Node</span></span>](https://docs.microsoft.com/javascript/api/overview/azure/key-vault)
* [<span data-ttu-id="92434-218">Azure REST API 参考</span><span class="sxs-lookup"><span data-stu-id="92434-218">Azure REST API Reference</span></span>](https://docs.microsoft.com/rest/api/keyvault/)
::: zone-end

::: zone pivot="dotnet"
* [<span data-ttu-id="92434-219">Azure Key Vault 主页</span><span class="sxs-lookup"><span data-stu-id="92434-219">Azure Key Vault home page</span></span>](https://azure.microsoft.com/services/key-vault/)
* [<span data-ttu-id="92434-220">Azure Key Vault 文档</span><span class="sxs-lookup"><span data-stu-id="92434-220">Azure Key Vault documentation</span></span>](https://docs.microsoft.com/azure/key-vault/)
* [<span data-ttu-id="92434-221">用于 .NET 的 Azure SDK</span><span class="sxs-lookup"><span data-stu-id="92434-221">Azure SDK For .NET</span></span>](https://github.com/Azure/azure-sdk-for-net)
* [<span data-ttu-id="92434-222">Azure REST API 参考</span><span class="sxs-lookup"><span data-stu-id="92434-222">Azure REST API reference</span></span>](https://docs.microsoft.com/rest/api/keyvault/)
::: zone-end
