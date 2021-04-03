---
title: 库存可见性加载项
description: 本主题介绍如何为 Dynamics 365 Supply Chain Management 安装和配置库存可见性加载项。
author: sherry-zheng
manager: tfehr
ms.date: 10/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-10-26
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 4e588be2ac5aae395ca66e3c9a743a67d71db7c0
ms.sourcegitcommit: a3052f76ad71894dbef66566c07c6e2c31505870
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/10/2021
ms.locfileid: "5574214"
---
# <a name="inventory-visibility-add-in"></a><span data-ttu-id="89818-103">库存可见性加载项</span><span class="sxs-lookup"><span data-stu-id="89818-103">Inventory Visibility Add-in</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

<span data-ttu-id="89818-104">库存可见性加载项是一项独立且高度可扩展的微服务，可实现实时现有库存跟踪，并提供库存可见性的全局视图。</span><span class="sxs-lookup"><span data-stu-id="89818-104">The Inventory Visibility Add-in is an independent and highly scalable microservice that enables real-time on-hand inventory tracking, thus providing a global view of inventory visibility.</span></span>

<span data-ttu-id="89818-105">通过低级别 SQL 集成，准实时地将与现有库存相关的所有信息导出到服务中。</span><span class="sxs-lookup"><span data-stu-id="89818-105">All information that relates to on-hand inventory is exported to the service in near real-time through low-level SQL integration.</span></span> <span data-ttu-id="89818-106">外部系统通过 RESTful API 访问服务，以查询有关给定维度集的现有信息，从而检索可用现有位置的列表。</span><span class="sxs-lookup"><span data-stu-id="89818-106">External systems access the service through RESTful APIs to query on-hand information on given sets of dimensions, thus retrieving a list of available on-hand positions.</span></span>

<span data-ttu-id="89818-107">库存可见性是基于 Microsoft Dataverse 生成的微服务，这意味着您可以通过生成 Power Apps 和应用 Power BI 来扩展它，从而提供自定义功能以满足您的业务需求。</span><span class="sxs-lookup"><span data-stu-id="89818-107">Inventory Visibility is a microservice built on Microsoft Dataverse, which means you can extend it by building Power Apps and applying Power BI to provide customized functionality to meet your business requirements.</span></span> <span data-ttu-id="89818-108">也可以升级索引以进行库存查询。</span><span class="sxs-lookup"><span data-stu-id="89818-108">It is also possible to upgrade the index to do inventory queries.</span></span>

<span data-ttu-id="89818-109">库存可见性提供配置选项，使其可以与多个第三方系统集成。</span><span class="sxs-lookup"><span data-stu-id="89818-109">Inventory Visibility provides configuration options that let it integrate with multiple third-party systems.</span></span> <span data-ttu-id="89818-110">它支持标准化的库存维度、自定义的可扩展性以及标准化的可配置的计算数量。</span><span class="sxs-lookup"><span data-stu-id="89818-110">It supports the standardized inventory dimension, customized extensibility, and standardized, configurable calculated quantities.</span></span>

<span data-ttu-id="89818-111">本主题介绍如何为 Dynamics 365 Supply Chain Management 安装和配置库存可见性加载项，以及如何使用其应用程序编程接口 (API)。</span><span class="sxs-lookup"><span data-stu-id="89818-111">This topic describes how to install and configure the Inventory Visibility Add-in for Dynamics 365 Supply Chain Management, and how to use its application programming interface (API).</span></span>

## <a name="install-the-inventory-visibility-add-in"></a><span data-ttu-id="89818-112">安装库存可见性加载项</span><span class="sxs-lookup"><span data-stu-id="89818-112">Install the Inventory Visibility Add-in</span></span>

<span data-ttu-id="89818-113">您需要使用 Microsoft Dynamics Lifecycle Services (LCS) 安装库存可见性加载项。</span><span class="sxs-lookup"><span data-stu-id="89818-113">You need to install the Inventory Visibility Add-in using Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="89818-114">LCS 是一个协作门户，可提供环境和一组定期更新的服务，以帮助您管理 Dynamics 365 Finance and Operations 应用的应用程序生命周期。</span><span class="sxs-lookup"><span data-stu-id="89818-114">LCS is a collaboration portal that provides an environment and a set of regularly updated services that help you manage the application lifecycle of your Dynamics 365 Finance and Operations apps.</span></span>

<span data-ttu-id="89818-115">有关详细信息，请参阅 [Lifecycle Services 资源](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/lcs)。</span><span class="sxs-lookup"><span data-stu-id="89818-115">For more information, see [Lifecycle Services resources](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/lcs).</span></span>

### <a name="prerequisites"></a><span data-ttu-id="89818-116">先决条件</span><span class="sxs-lookup"><span data-stu-id="89818-116">Prerequisites</span></span>

<span data-ttu-id="89818-117">在安装库存可见性加载项之前，您必须执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="89818-117">Before you install the Inventory Visibility Add-in, you must do the following:</span></span>

- <span data-ttu-id="89818-118">获取至少部署了一个环境的 LCS 实施项目。</span><span class="sxs-lookup"><span data-stu-id="89818-118">Obtain an LCS implementation project with at least one environment deployed.</span></span>
- <span data-ttu-id="89818-119">确保[加载项概述](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md)中提供的设置加载项的先决条件已经满足。</span><span class="sxs-lookup"><span data-stu-id="89818-119">Make sure that the prerequisites for setting up add-ins provided in the [Add-ins overview](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md) have been completed.</span></span> <span data-ttu-id="89818-120">库存可见性不需要双写入链接。</span><span class="sxs-lookup"><span data-stu-id="89818-120">Inventory Visibility doesn't require dual-write linking.</span></span>
- <span data-ttu-id="89818-121">请通过 [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) 与库存可见性团队联系，获取以下三个必需文件：</span><span class="sxs-lookup"><span data-stu-id="89818-121">Contact the Inventory Visibility Team at [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) to get the following three required files:</span></span>

    - `Inventory Visibility Dataverse Solution.zip`
    - `Inventory Visibility Configuration Trigger.zip`
    - <span data-ttu-id="89818-122">`Inventory Visibility Integration.zip`（如果您运行的 Supply Chain Management 的版本早于版本 10.0.18）</span><span class="sxs-lookup"><span data-stu-id="89818-122">`Inventory Visibility Integration.zip` (if the version of Supply Chain Management that you're running is earlier than version 10.0.18)</span></span>

> [!NOTE]
> <span data-ttu-id="89818-123">目前支持的国家和地区包括加拿大、美国和欧盟 (EU)。</span><span class="sxs-lookup"><span data-stu-id="89818-123">The currently supported countries and regions include Canada, the United States, and the European Union (EU).</span></span>

<span data-ttu-id="89818-124">如果您对这些先决条件有任何疑问，请与库存可视性产品团队联系。</span><span class="sxs-lookup"><span data-stu-id="89818-124">If you have any questions about these prerequisites, please contact the Inventory Visibility product team.</span></span>

### <a name="set-up-dataverse"></a><a name="setup-microsoft-dataverse"></a><span data-ttu-id="89818-125">设置 Dataverse</span><span class="sxs-lookup"><span data-stu-id="89818-125">Set up Dataverse</span></span>

<span data-ttu-id="89818-126">请按照下列步骤设置 Dataverse。</span><span class="sxs-lookup"><span data-stu-id="89818-126">Follow these steps to set up Dataverse.</span></span>

1. <span data-ttu-id="89818-127">向您的租户添加服务原则：</span><span class="sxs-lookup"><span data-stu-id="89818-127">Add a service principle to your tenant:</span></span>

    1. <span data-ttu-id="89818-128">如[安装 Azure Active Directory PowerShell for Graph](https://docs.microsoft.com/powershell/azure/active-directory/install-adv2) 中所述安装 Azure AD PowerShell 模块 v2。</span><span class="sxs-lookup"><span data-stu-id="89818-128">Install Azure AD PowerShell Module v2 as described in [Install Azure Active Directory PowerShell for Graph](https://docs.microsoft.com/powershell/azure/active-directory/install-adv2).</span></span>
    1. <span data-ttu-id="89818-129">运行以下 PowerShell 命令。</span><span class="sxs-lookup"><span data-stu-id="89818-129">Run the following PowerShell command.</span></span>

        ```powershell
        Connect-AzureAD # (open a sign in window and sign in as a tenant user)

        New-AzureADServicePrincipal -AppId "3022308a-b9bd-4a18-b8ac-2ddedb2075e1" -DisplayName "d365-scm-inventoryservice"
        ```

1. <span data-ttu-id="89818-130">在 Dataverse 中为库存可见性创建应用程序用户：</span><span class="sxs-lookup"><span data-stu-id="89818-130">Create an application user for Inventory Visibility in Dataverse:</span></span>

    1. <span data-ttu-id="89818-131">打开您的 Dataverse 环境的 URL。</span><span class="sxs-lookup"><span data-stu-id="89818-131">Open the URL of your Dataverse environment.</span></span>
    1. <span data-ttu-id="89818-132">转到 **高级设置 \> 系统 \> 安全 \> 用户**，创建应用程序用户。</span><span class="sxs-lookup"><span data-stu-id="89818-132">Go to **Advanced Setting \> System \> Security \> Users**, and create an application user.</span></span> <span data-ttu-id="89818-133">使用视图菜单将页面视图更改为 **应用程序用户**。</span><span class="sxs-lookup"><span data-stu-id="89818-133">Use the view menu to change the page view to **Application Users**.</span></span>
    1. <span data-ttu-id="89818-134">选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="89818-134">Select **New**.</span></span> <span data-ttu-id="89818-135">将应用程序 ID 设置为 *3022308a-b9bd-4a18-b8ac-2ddedb2075e1*。</span><span class="sxs-lookup"><span data-stu-id="89818-135">Set the application ID to *3022308a-b9bd-4a18-b8ac-2ddedb2075e1*.</span></span> <span data-ttu-id="89818-136">（保存更改后，对象 ID 将自动加载。）您可以自定义名称。</span><span class="sxs-lookup"><span data-stu-id="89818-136">(The object ID will automatically be loaded when you save your changes.) You can customize the name.</span></span> <span data-ttu-id="89818-137">例如，您可以将其更改为 *库存可见性*。</span><span class="sxs-lookup"><span data-stu-id="89818-137">For example, you can change it to *Inventory Visibility*.</span></span> <span data-ttu-id="89818-138">当您完成时，选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="89818-138">When you've finished, select **Save**.</span></span>
    1. <span data-ttu-id="89818-139">选择 **分配角色**，然后选择 **系统管理员**。</span><span class="sxs-lookup"><span data-stu-id="89818-139">Select **Assign Role**, and then select **System Administrator**.</span></span> <span data-ttu-id="89818-140">如果有一个名为 **Common Data Service 用户** 的角色，也选择它。</span><span class="sxs-lookup"><span data-stu-id="89818-140">If there is a role that is named **Common Data Service User**, select it too.</span></span>

    <span data-ttu-id="89818-141">有关详细信息，请参阅[创建应用程序用户](https://docs.microsoft.com/power-platform/admin/create-users-assign-online-security-roles#create-an-application-user)。</span><span class="sxs-lookup"><span data-stu-id="89818-141">For more information, see [Create an application user](https://docs.microsoft.com/power-platform/admin/create-users-assign-online-security-roles#create-an-application-user).</span></span>

1. <span data-ttu-id="89818-142">导入 `Inventory Visibility Dataverse Solution.zip` 文件，其中包括与 Dataverse 配置相关的实体和 Power Apps：</span><span class="sxs-lookup"><span data-stu-id="89818-142">Import the `Inventory Visibility Dataverse Solution.zip` file, which includes Dataverse configuration related entities and Power Apps:</span></span>

    1. <span data-ttu-id="89818-143">转到 **解决方案** 页。</span><span class="sxs-lookup"><span data-stu-id="89818-143">Go to the **Solutions** page.</span></span>
    1. <span data-ttu-id="89818-144">选择 **导入**。</span><span class="sxs-lookup"><span data-stu-id="89818-144">Select **Import**.</span></span>

1. <span data-ttu-id="89818-145">导入配置升级触发流：</span><span class="sxs-lookup"><span data-stu-id="89818-145">Import the configuration upgrade trigger flow:</span></span>

    1. <span data-ttu-id="89818-146">转到 Microsoft Flow 页。</span><span class="sxs-lookup"><span data-stu-id="89818-146">Go to the Microsoft Flow page.</span></span>
    1. <span data-ttu-id="89818-147">确保存在名为 *Dataverse (旧版)* 的连接。</span><span class="sxs-lookup"><span data-stu-id="89818-147">Make sure that the connection that is named *Dataverse (legacy)* exists.</span></span> <span data-ttu-id="89818-148">（如果不存在，请创建。）</span><span class="sxs-lookup"><span data-stu-id="89818-148">(If it doesn't exist, create it.)</span></span>
    1. <span data-ttu-id="89818-149">导入 `Inventory Visibility Configuration Trigger.zip` 文件。</span><span class="sxs-lookup"><span data-stu-id="89818-149">Import the `Inventory Visibility Configuration Trigger.zip` file.</span></span> <span data-ttu-id="89818-150">导入后，触发器将出现在 **我的流** 下。</span><span class="sxs-lookup"><span data-stu-id="89818-150">After it's imported, the trigger will appear under **My flows**.</span></span>
    1. <span data-ttu-id="89818-151">根据环境信息初始化以下四个变量：</span><span class="sxs-lookup"><span data-stu-id="89818-151">Initialize the following four variables, based on the environment information:</span></span>

        - <span data-ttu-id="89818-152">Azure 租户 ID</span><span class="sxs-lookup"><span data-stu-id="89818-152">Azure Tenant ID</span></span>
        - <span data-ttu-id="89818-153">Azure 应用程序客户端 ID</span><span class="sxs-lookup"><span data-stu-id="89818-153">Azure Application Client ID</span></span>
        - <span data-ttu-id="89818-154">Azure 应用程序客户端密码</span><span class="sxs-lookup"><span data-stu-id="89818-154">Azure Application Client Secret</span></span>
        - <span data-ttu-id="89818-155">库存可见性终结点</span><span class="sxs-lookup"><span data-stu-id="89818-155">Inventory Visibility Endpoint</span></span>

            <span data-ttu-id="89818-156">有关此变量的详细信息，请参阅本主题后面的[设置库存可见性集成](#setup-inventory-visibility-integration)一节。</span><span class="sxs-lookup"><span data-stu-id="89818-156">For more information about this variable, see the [Set up Inventory Visibility integration](#setup-inventory-visibility-integration) section later in this topic.</span></span>

        <span data-ttu-id="89818-157">![配置触发器](media/configuration-trigger.png "配置触发器")</span><span class="sxs-lookup"><span data-stu-id="89818-157">![Configuration trigger](media/configuration-trigger.png "Configuration trigger")</span></span>

    1. <span data-ttu-id="89818-158">选择 **打开**。</span><span class="sxs-lookup"><span data-stu-id="89818-158">Select **Turn on**.</span></span>

### <a name="install-the-add-in"></a><a name="install-add-in"></a><span data-ttu-id="89818-159">安装加载项</span><span class="sxs-lookup"><span data-stu-id="89818-159">Install the add-in</span></span>

<span data-ttu-id="89818-160">若要安装库存可见性加载项，请执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="89818-160">To install the Inventory Visibility Add-in, do the following:</span></span>

1. <span data-ttu-id="89818-161">登录到 [Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index) 门户。</span><span class="sxs-lookup"><span data-stu-id="89818-161">Sign in to the [Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index) portal.</span></span>
1. <span data-ttu-id="89818-162">在主页上，选择在其中部署环境的项目。</span><span class="sxs-lookup"><span data-stu-id="89818-162">On the home page, select the project where your environment is deployed.</span></span>
1. <span data-ttu-id="89818-163">在项目页面上，选择要在其中安装加载项的环境。</span><span class="sxs-lookup"><span data-stu-id="89818-163">On the project page, select the environment where you want to install the add-in.</span></span>
1. <span data-ttu-id="89818-164">在环境页上，向下滚动，直到看到 **Power Platform 集成** 部分中的 **环境加载项** 部分，您可以在其中找到 Dataverse 环境名称。</span><span class="sxs-lookup"><span data-stu-id="89818-164">On the environment page, scroll down until you see the **Environment add-ins** section in the **Power Platform integration** section, where you can find the Dataverse environment name.</span></span>
1. <span data-ttu-id="89818-165">在 **环境加载项** 部分中，选择 **安装新加载项**。</span><span class="sxs-lookup"><span data-stu-id="89818-165">In the **Environment add-ins** section, select **Install a new add-in**.</span></span>

    <span data-ttu-id="89818-166">![LCS 中的环境页面](media/inventory-visibility-environment.png "LCS 中的环境页面")</span><span class="sxs-lookup"><span data-stu-id="89818-166">![The environment page in LCS](media/inventory-visibility-environment.png "The environment page in LCS")</span></span>

1. <span data-ttu-id="89818-167">选择 **安装新加载项** 链接。</span><span class="sxs-lookup"><span data-stu-id="89818-167">Select the **Install a new add-in** link.</span></span> <span data-ttu-id="89818-168">将打开可用加载项的列表。</span><span class="sxs-lookup"><span data-stu-id="89818-168">A list of available add-ins opens.</span></span>
1. <span data-ttu-id="89818-169">在列表中选择 **库存可见性**。</span><span class="sxs-lookup"><span data-stu-id="89818-169">Select **Inventory Visibility** in the list.</span></span>
1. <span data-ttu-id="89818-170">为您的环境输入以下字段的值：</span><span class="sxs-lookup"><span data-stu-id="89818-170">Enter values for the following fields for your environment:</span></span>

    - <span data-ttu-id="89818-171">**AAD 应用程序（客户端）ID**</span><span class="sxs-lookup"><span data-stu-id="89818-171">**AAD application (client) ID**</span></span>
    - <span data-ttu-id="89818-172">**AAD 租户 ID**</span><span class="sxs-lookup"><span data-stu-id="89818-172">**AAD tenant ID**</span></span>

    <span data-ttu-id="89818-173">![加载项设置页面](media/inventory-visibility-setup.png "加载项设置页面")</span><span class="sxs-lookup"><span data-stu-id="89818-173">![Add in setup page](media/inventory-visibility-setup.png "Add-in setup page")</span></span>

1. <span data-ttu-id="89818-174">通过选中 **条款和条件** 复选框同意条款和条件。</span><span class="sxs-lookup"><span data-stu-id="89818-174">Agree to the terms and condition by selecting the **Terms and conditions** check box.</span></span>
1. <span data-ttu-id="89818-175">选择 **安装**。</span><span class="sxs-lookup"><span data-stu-id="89818-175">Select **Install**.</span></span> <span data-ttu-id="89818-176">加载项的状态将显示为 **正在安装**。</span><span class="sxs-lookup"><span data-stu-id="89818-176">The status of the add-in will show as **Installing**.</span></span> <span data-ttu-id="89818-177">完成后，刷新页面以查看状态更改为 **已安装**。</span><span class="sxs-lookup"><span data-stu-id="89818-177">When it's done, refresh the page to see the status change to **Installed**.</span></span>

### <a name="uninstall-the-add-in"></a><a name="uninstall-add-in"></a><span data-ttu-id="89818-178">卸载加载项</span><span class="sxs-lookup"><span data-stu-id="89818-178">Uninstall the add-in</span></span>

<span data-ttu-id="89818-179">若要卸载加载项，请选择 **卸载**。</span><span class="sxs-lookup"><span data-stu-id="89818-179">To uninstall the add-in, select **Uninstall**.</span></span> <span data-ttu-id="89818-180">刷新 LCS 时，库存可见性加载项将被删除。</span><span class="sxs-lookup"><span data-stu-id="89818-180">When you refresh LCS, the Inventory Visibility Add-in will be removed.</span></span> <span data-ttu-id="89818-181">卸载流程将删除加载项注册，还将启动作业以清理存储在服务中的所有业务数据。</span><span class="sxs-lookup"><span data-stu-id="89818-181">The uninstall process removes the add-in registration and also starts a job to clean up all the business data that is stored in the service.</span></span>

## <a name="consume-on-hand-inventory-data-from-supply-chain-management"></a><span data-ttu-id="89818-182">使用 Supply Chain Management 中的现有库存量数据</span><span class="sxs-lookup"><span data-stu-id="89818-182">Consume on-hand inventory data from Supply Chain Management</span></span>

### <a name="deploy-the-inventory-visibility-integration-package"></a><a name="deploy-inventory-visibility-package"></a><span data-ttu-id="89818-183">部署库存可见性集成包</span><span class="sxs-lookup"><span data-stu-id="89818-183">Deploy the Inventory Visibility integration package</span></span>

<span data-ttu-id="89818-184">如果您运行的是 Supply Chain Management 版本 10.0.17 或更早版本，请通过 [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) 与库存可见性当班支持团队联系获取包文件。</span><span class="sxs-lookup"><span data-stu-id="89818-184">If you're running Supply Chain Management version 10.0.17 or earlier, contact the Inventory Visibility on-board support team at [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) to get the package file.</span></span> <span data-ttu-id="89818-185">然后在 LCS 中部署包。</span><span class="sxs-lookup"><span data-stu-id="89818-185">Then deploy the package in LCS.</span></span>

> [!NOTE]
> <span data-ttu-id="89818-186">如果在部署过程中发生版本不匹配错误，则必须手动将 X++ 项目导入到您的开发环境。</span><span class="sxs-lookup"><span data-stu-id="89818-186">If a version mismatch error occurs during deployment, you must manually import the X++ project into your development environment.</span></span> <span data-ttu-id="89818-187">然后在您的开发环境中创建可部署包，并在您的生产环境中部署。</span><span class="sxs-lookup"><span data-stu-id="89818-187">Then create the deployable package in your development environment, and deploy it in your production environment.</span></span>
> 
> <span data-ttu-id="89818-188">此代码包含在 Supply Chain Management 版本 10.0.18 中。</span><span class="sxs-lookup"><span data-stu-id="89818-188">The code is included with Supply Chain Management version 10.0.18.</span></span> <span data-ttu-id="89818-189">如果您运行的是该版本或更高版本，则不需要进行部署。</span><span class="sxs-lookup"><span data-stu-id="89818-189">If you're running that version or later, deployment isn't required.</span></span>

<span data-ttu-id="89818-190">确保在您的 Supply Chain Management 环境中启用了以下功能。</span><span class="sxs-lookup"><span data-stu-id="89818-190">Make sure that the following features are turned on in your Supply Chain Management environment.</span></span> <span data-ttu-id="89818-191">（默认情况下，它们是打开的。）</span><span class="sxs-lookup"><span data-stu-id="89818-191">(By default, they are turned on.)</span></span>

| <span data-ttu-id="89818-192">功能描述</span><span class="sxs-lookup"><span data-stu-id="89818-192">Feature description</span></span> | <span data-ttu-id="89818-193">代码版本</span><span class="sxs-lookup"><span data-stu-id="89818-193">Code version</span></span> | <span data-ttu-id="89818-194">切换类</span><span class="sxs-lookup"><span data-stu-id="89818-194">Toggle class</span></span> |
|---|---|---|
| <span data-ttu-id="89818-195">在 InventSum 表上启用或禁用使用库存维度</span><span class="sxs-lookup"><span data-stu-id="89818-195">Enable or disable using inventory dimensions on InventSum table</span></span> | <span data-ttu-id="89818-196">10.0.11</span><span class="sxs-lookup"><span data-stu-id="89818-196">10.0.11</span></span> | <span data-ttu-id="89818-197">InventUseDimOfInventSumToggle</span><span class="sxs-lookup"><span data-stu-id="89818-197">InventUseDimOfInventSumToggle</span></span> |
| <span data-ttu-id="89818-198">在 InventSumDelta 表上启用或禁用使用库存维度</span><span class="sxs-lookup"><span data-stu-id="89818-198">Enable or disable using inventory dimensions on InventSumDelta table</span></span> | <span data-ttu-id="89818-199">10.0.12</span><span class="sxs-lookup"><span data-stu-id="89818-199">10.0.12</span></span> | <span data-ttu-id="89818-200">InventUseDimOfInventSumDeltaToggle</span><span class="sxs-lookup"><span data-stu-id="89818-200">InventUseDimOfInventSumDeltaToggle</span></span> |

### <a name="set-up-inventory-visibility-integration"></a><a name="setup-inventory-visibility-integration"></a><span data-ttu-id="89818-201">设置库存可见性集成</span><span class="sxs-lookup"><span data-stu-id="89818-201">Set up Inventory Visibility integration</span></span>

1. <span data-ttu-id="89818-202">在 Supply Chain Management 中，打开 **[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** 工作区，然后打开 **库存可见性集成** 功能。</span><span class="sxs-lookup"><span data-stu-id="89818-202">In Supply Chain Management, open the **[Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** workspace, and turn on the **Inventory Visibility Integration** feature.</span></span>
1. <span data-ttu-id="89818-203">转到 **库存管理 \> 设置 \> 库存可见性集成参数**，输入要运行“库存可见性”的环境的 URL。</span><span class="sxs-lookup"><span data-stu-id="89818-203">Go to **Inventory Management \> Set up \> Inventory Visibility Integration parameters**, and enter the URL of the environment where you're running Inventory Visibility.</span></span>

    <span data-ttu-id="89818-204">找到您的 LCS 环境的 Azure 区域，然后输入 URL。</span><span class="sxs-lookup"><span data-stu-id="89818-204">Find your LCS environment's Azure region, and then enter the URL.</span></span> <span data-ttu-id="89818-205">URL 具有以下形式：</span><span class="sxs-lookup"><span data-stu-id="89818-205">The URL has the following form:</span></span>

    `https://inventoryservice.<RegionShortName>-il301.gateway.prod.island.powerapps.com/`

    <span data-ttu-id="89818-206">例如，如果您在欧洲，您的环境将具有以下 URL 之一：</span><span class="sxs-lookup"><span data-stu-id="89818-206">For example, if you're in Europe, your environment will have one of the following URLs:</span></span>

    - `https://inventoryservice.neu-il301.gateway.prod.island.powerapps.com/`
    - `https://inventoryservice.weu-il301.gateway.prod.island.powerapps.com/`

    <span data-ttu-id="89818-207">以下区域当前可用。</span><span class="sxs-lookup"><span data-stu-id="89818-207">The following regions are currently available.</span></span>

    | <span data-ttu-id="89818-208">Azure 区域</span><span class="sxs-lookup"><span data-stu-id="89818-208">Azure region</span></span> | <span data-ttu-id="89818-209">区域短名称</span><span class="sxs-lookup"><span data-stu-id="89818-209">Region short name</span></span> |
    |---|---|
    | <span data-ttu-id="89818-210">澳大利亚东部</span><span class="sxs-lookup"><span data-stu-id="89818-210">Australia east</span></span> | <span data-ttu-id="89818-211">eau</span><span class="sxs-lookup"><span data-stu-id="89818-211">eau</span></span> |
    | <span data-ttu-id="89818-212">澳大利亚东南部</span><span class="sxs-lookup"><span data-stu-id="89818-212">Australia southeast</span></span> | <span data-ttu-id="89818-213">seau</span><span class="sxs-lookup"><span data-stu-id="89818-213">seau</span></span> |
    | <span data-ttu-id="89818-214">加拿大中部</span><span class="sxs-lookup"><span data-stu-id="89818-214">Canada central</span></span> | <span data-ttu-id="89818-215">cca</span><span class="sxs-lookup"><span data-stu-id="89818-215">cca</span></span> |
    | <span data-ttu-id="89818-216">加拿大东部</span><span class="sxs-lookup"><span data-stu-id="89818-216">Canada east</span></span> | <span data-ttu-id="89818-217">eca</span><span class="sxs-lookup"><span data-stu-id="89818-217">eca</span></span> |
    | <span data-ttu-id="89818-218">欧洲北部</span><span class="sxs-lookup"><span data-stu-id="89818-218">North Europe</span></span> | <span data-ttu-id="89818-219">neu</span><span class="sxs-lookup"><span data-stu-id="89818-219">neu</span></span> |
    | <span data-ttu-id="89818-220">西欧</span><span class="sxs-lookup"><span data-stu-id="89818-220">West Europe</span></span> | <span data-ttu-id="89818-221">weu</span><span class="sxs-lookup"><span data-stu-id="89818-221">weu</span></span> |
    | <span data-ttu-id="89818-222">美国东部</span><span class="sxs-lookup"><span data-stu-id="89818-222">East US</span></span> | <span data-ttu-id="89818-223">eus</span><span class="sxs-lookup"><span data-stu-id="89818-223">eus</span></span> |
    | <span data-ttu-id="89818-224">美国西部</span><span class="sxs-lookup"><span data-stu-id="89818-224">West US</span></span> | <span data-ttu-id="89818-225">wus</span><span class="sxs-lookup"><span data-stu-id="89818-225">wus</span></span> |

1. <span data-ttu-id="89818-226">转到 **库存管理 \> 定期 \> 库存可见性集成**，启用作业。</span><span class="sxs-lookup"><span data-stu-id="89818-226">Go to **Inventory Management \> Periodic \> Inventory Visibility Integration**, and enable the job.</span></span> <span data-ttu-id="89818-227">现在，来自 Supply Chain Management 的所有库存更改事件都将发布到库存可见性。</span><span class="sxs-lookup"><span data-stu-id="89818-227">All inventory change events from Supply Chain Management will now be posted to Inventory Visibility.</span></span>

## <a name="the-inventory-visibility-add-in-public-api"></a><a name="inventory-visibility-public-api"></a><span data-ttu-id="89818-228">库存可见性加载项公共 API</span><span class="sxs-lookup"><span data-stu-id="89818-228">The Inventory Visibility Add-in public API</span></span>

<span data-ttu-id="89818-229">库存可见性加载项的公共 REST API 为集成提供几个特定终结点。</span><span class="sxs-lookup"><span data-stu-id="89818-229">The public REST API of the Inventory Visibility Add-in presents several specific endpoints for integration.</span></span> <span data-ttu-id="89818-230">它支持三种主要交互类型：</span><span class="sxs-lookup"><span data-stu-id="89818-230">It supports three main interaction types:</span></span>

- <span data-ttu-id="89818-231">从外部系统发布对加载项的现有库存量更改</span><span class="sxs-lookup"><span data-stu-id="89818-231">Posting on-hand inventory changes to the add-in from an external system</span></span>
- <span data-ttu-id="89818-232">从外部系统查询当前的现有数量</span><span class="sxs-lookup"><span data-stu-id="89818-232">Querying current on-hand quantities from an external system</span></span>
- <span data-ttu-id="89818-233">自动与 Supply Chain Management 现有库存量同步</span><span class="sxs-lookup"><span data-stu-id="89818-233">Automatic synchronization with Supply Chain Management on-hand inventory</span></span>

<span data-ttu-id="89818-234">自动同步不是公共 API 的一部分。</span><span class="sxs-lookup"><span data-stu-id="89818-234">Automatic synchronization isn't part of the public API.</span></span> <span data-ttu-id="89818-235">而会在启用了库存可见性加载项的环境的后台处理。</span><span class="sxs-lookup"><span data-stu-id="89818-235">Instead, it's handled in the background for environments where the Inventory Visibility Add-in is enabled.</span></span>

### <a name="authentication"></a><a name="inventory-visibility-authentication"></a><span data-ttu-id="89818-236">身份验证</span><span class="sxs-lookup"><span data-stu-id="89818-236">Authentication</span></span>

<span data-ttu-id="89818-237">平台安全令牌用于调用库存可见性加载项。</span><span class="sxs-lookup"><span data-stu-id="89818-237">The platform security token is used to call the Inventory Visibility Add-in.</span></span> <span data-ttu-id="89818-238">因此，您必须使用Azure AD 应用程序生成 *Azure Active Directory (Azure AD) 令牌*。</span><span class="sxs-lookup"><span data-stu-id="89818-238">Therefore, you must generate an *Azure Active Directory (Azure AD) token* by using your Azure AD application.</span></span> <span data-ttu-id="89818-239">然后，必须使用 Azure AD 令牌从安全服务获取 *访问令牌*。</span><span class="sxs-lookup"><span data-stu-id="89818-239">You must then use the Azure AD token to get the *access token* from the security service.</span></span>

<span data-ttu-id="89818-240">通过执行以下操作获取安全服务令牌：</span><span class="sxs-lookup"><span data-stu-id="89818-240">Get a security service token by doing the following:</span></span>

1. <span data-ttu-id="89818-241">登录到 Azure 门户，使用它为您的 Supply Chain Management 应用程序查找 `clientId` 和 `clientSecret`。</span><span class="sxs-lookup"><span data-stu-id="89818-241">Sign in to Azure portal and use it to find the `clientId` and `clientSecret` for your Supply Chain Management application.</span></span>
1. <span data-ttu-id="89818-242">通过提交包含以下属性的 HTTP 请求来获取 Azure Active Directory 令牌 (`aadToken`)：</span><span class="sxs-lookup"><span data-stu-id="89818-242">Fetch an Azure Active Directory token (`aadToken`) by submitting an HTTP request with the following properties:</span></span>
    - <span data-ttu-id="89818-243">**URL** - `https://login.microsoftonline.com/${aadTenantId}/oauth2/token`</span><span class="sxs-lookup"><span data-stu-id="89818-243">**URL** - `https://login.microsoftonline.com/${aadTenantId}/oauth2/token`</span></span>
    - <span data-ttu-id="89818-244">**方法** - `GET`</span><span class="sxs-lookup"><span data-stu-id="89818-244">**Method** - `GET`</span></span>
    - <span data-ttu-id="89818-245">**正文内容（窗体数据）**：</span><span class="sxs-lookup"><span data-stu-id="89818-245">**Body content (form data)**:</span></span>

        | <span data-ttu-id="89818-246">键</span><span class="sxs-lookup"><span data-stu-id="89818-246">key</span></span> | <span data-ttu-id="89818-247">值</span><span class="sxs-lookup"><span data-stu-id="89818-247">value</span></span> |
        | --- | --- |
        | <span data-ttu-id="89818-248">client_id</span><span class="sxs-lookup"><span data-stu-id="89818-248">client_id</span></span> | <span data-ttu-id="89818-249">${aadAppId}</span><span class="sxs-lookup"><span data-stu-id="89818-249">${aadAppId}</span></span> |
        | <span data-ttu-id="89818-250">client_secret</span><span class="sxs-lookup"><span data-stu-id="89818-250">client_secret</span></span> | <span data-ttu-id="89818-251">${aadAppSecret}</span><span class="sxs-lookup"><span data-stu-id="89818-251">${aadAppSecret}</span></span> |
        | <span data-ttu-id="89818-252">grant_type</span><span class="sxs-lookup"><span data-stu-id="89818-252">grant_type</span></span> | <span data-ttu-id="89818-253">client_credentials</span><span class="sxs-lookup"><span data-stu-id="89818-253">client_credentials</span></span> |
        | <span data-ttu-id="89818-254">resource</span><span class="sxs-lookup"><span data-stu-id="89818-254">resource</span></span> | <span data-ttu-id="89818-255">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span><span class="sxs-lookup"><span data-stu-id="89818-255">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span></span> |
1. <span data-ttu-id="89818-256">您应该会在响应中收到一个 `aadToken`，类似于以下示例。</span><span class="sxs-lookup"><span data-stu-id="89818-256">You should receive an `aadToken` in response, which resembles the following example.</span></span>

    ```json
    {
    "token_type": "Bearer",
    "expires_in": "3599",
    "ext_expires_in": "3599",
    "expires_on": "1610466645",
    "not_before": "1610462745",
    "resource": "0cdb527f-a8d1-4bf8-9436-b352c68682b2",
    "access_token": "eyJ0eX...8WQ"
    }
    ```

1. <span data-ttu-id="89818-257">创建一个类似于以下请求的 JSON 请求：</span><span class="sxs-lookup"><span data-stu-id="89818-257">Formulate a JSON request that resembles the following:</span></span>

    ```json
    {
        "grant_type": "client_credentials",
        "client_assertion_type":"aad_app",
        "client_assertion": "{Your_AADToken}",
        "scope":"https://inventoryservice.operations365.dynamics.com/.default",
        "context": "5dbf6cc8-255e-4de2-8a25-2101cd5649b4",
        "context_type": "finops-env"
    }
    ```

    <span data-ttu-id="89818-258">其中：</span><span class="sxs-lookup"><span data-stu-id="89818-258">Where:</span></span>
    - <span data-ttu-id="89818-259">`client_assertion` 值必须是您在上一步中收到的 `aadToken`。</span><span class="sxs-lookup"><span data-stu-id="89818-259">The `client_assertion` value must be the `aadToken` you received in the previous step.</span></span>
    - <span data-ttu-id="89818-260">`context` 值必须是要在其中部署加载项的环境 ID。</span><span class="sxs-lookup"><span data-stu-id="89818-260">The `context` value must be the environment ID where you want to deploy the add-in.</span></span>
    - <span data-ttu-id="89818-261">如示例中所示设置所有其他值。</span><span class="sxs-lookup"><span data-stu-id="89818-261">Set all of other values as shown in the example.</span></span>

1. <span data-ttu-id="89818-262">提交包含以下属性的 HTTP 请求：</span><span class="sxs-lookup"><span data-stu-id="89818-262">Submit an HTTP request with the following properties:</span></span>
    - <span data-ttu-id="89818-263">**URL** - `https://securityservice.operations365.dynamics.com/token`</span><span class="sxs-lookup"><span data-stu-id="89818-263">**URL** - `https://securityservice.operations365.dynamics.com/token`</span></span>
    - <span data-ttu-id="89818-264">**方法** - `POST`</span><span class="sxs-lookup"><span data-stu-id="89818-264">**Method** - `POST`</span></span>
    - <span data-ttu-id="89818-265">**HTTP 标题** - 包含 API 版本（键为 `Api-Version`，值为 `1.0`）</span><span class="sxs-lookup"><span data-stu-id="89818-265">**HTTP header** - Include the API version (key is `Api-Version` and value is `1.0`)</span></span>
    - <span data-ttu-id="89818-266">**正文内容** - 包括您在上一步中创建的 JSON 请求。</span><span class="sxs-lookup"><span data-stu-id="89818-266">**Body content** - Include the JSON request that you created in the previous step.</span></span>

1. <span data-ttu-id="89818-267">您将获得 `access_token` 作为回应。</span><span class="sxs-lookup"><span data-stu-id="89818-267">You will get an `access_token` in response.</span></span> <span data-ttu-id="89818-268">您需要使用它作为持有者令牌来调用库存可见性 API。</span><span class="sxs-lookup"><span data-stu-id="89818-268">This is what you need as a bearer token to call the Inventory Visibility API.</span></span> <span data-ttu-id="89818-269">下面是一个示例。</span><span class="sxs-lookup"><span data-stu-id="89818-269">Here is an example.</span></span>

    ```json
    {
        "access_token": "{Returned_Token}",
        "token_type": "bearer",
        "expires_in": 1200
    }
    ```

### <a name="configure-the-inventory-visibility-api"></a><a name="inventory-visibility-configuration"></a><span data-ttu-id="89818-270">配置库存可见性 API</span><span class="sxs-lookup"><span data-stu-id="89818-270">Configure the Inventory Visibility API</span></span>

<span data-ttu-id="89818-271">使用该服务之前，必须完成以下子部分中所述的配置。</span><span class="sxs-lookup"><span data-stu-id="89818-271">Before using the service, you must complete the configurations described in the following subsections.</span></span> <span data-ttu-id="89818-272">配置因您的环境的详细信息而异。</span><span class="sxs-lookup"><span data-stu-id="89818-272">The configuration may vary based on the details of your environment.</span></span> <span data-ttu-id="89818-273">它主要包括四个部分：</span><span class="sxs-lookup"><span data-stu-id="89818-273">It primarily includes four parts:</span></span>

- [<span data-ttu-id="89818-274">分区</span><span class="sxs-lookup"><span data-stu-id="89818-274">Partitioning</span></span>](#partitioning)
- [<span data-ttu-id="89818-275">维度配置</span><span class="sxs-lookup"><span data-stu-id="89818-275">Dimension configurations</span></span>](#dimension-configurations)
- [<span data-ttu-id="89818-276">正在索引</span><span class="sxs-lookup"><span data-stu-id="89818-276">Indexing</span></span>](#indexing)
- [<span data-ttu-id="89818-277">自定义度量</span><span class="sxs-lookup"><span data-stu-id="89818-277">Custom measurement</span></span>](#custom-measurement)

#### <a name="partitioning"></a><span data-ttu-id="89818-278">分区</span><span class="sxs-lookup"><span data-stu-id="89818-278">Partitioning</span></span>

<span data-ttu-id="89818-279">分区会显著影响库存可见性 API 的性能。</span><span class="sxs-lookup"><span data-stu-id="89818-279">Partitioning can significantly influence the performance of the Inventory Visibility API.</span></span> <span data-ttu-id="89818-280">最好定义一个方案，允许将数据进行小规模分组，同时仍然允许有意义的数据查询。</span><span class="sxs-lookup"><span data-stu-id="89818-280">It's a good idea to define a scheme that allows for small groupings of data while still allowing for meaningful data queries.</span></span>

<span data-ttu-id="89818-281">`organizationId`（Supply Chain Management 中的 `dataAreaId`）将始终是分区的一部分，并且默认情况下，库存可见性按维度（*站点 + 库位*）设置为分区。</span><span class="sxs-lookup"><span data-stu-id="89818-281">The `organizationId` (`dataAreaId` in Supply Chain Management) will always be part of the partitioning, and by default Inventory Visibility is set to partition by dimensions as *Site + Location*.</span></span> <span data-ttu-id="89818-282">这意味着必须始终使用在筛选器上定义的这些维度来查询服务。</span><span class="sxs-lookup"><span data-stu-id="89818-282">This means that the service must always be queried with these dimensions defined on the filters.</span></span>

> [!NOTE]
> <span data-ttu-id="89818-283">*站点* 和 *库位* 是库存可见性中的两个常规默认维度。</span><span class="sxs-lookup"><span data-stu-id="89818-283">*Site* and *Location* are two general default dimensions in Inventory Visibility.</span></span> <span data-ttu-id="89818-284">在 Supply Chain Management 中，这些维度称为 *站点* (`InventSiteId`) 和 *仓库* (`InventLocationId`)</span><span class="sxs-lookup"><span data-stu-id="89818-284">In Supply Chain Management, those dimensions are called *Site* (`InventSiteId`) and *Warehouse* (`InventLocationId`)</span></span>

### <a name="dimension-configurations"></a><span data-ttu-id="89818-285">维度配置</span><span class="sxs-lookup"><span data-stu-id="89818-285">Dimension configurations</span></span>

<span data-ttu-id="89818-286">库存可见性将提供常规默认维度的列表，以启用多源系统集成。</span><span class="sxs-lookup"><span data-stu-id="89818-286">Inventory Visibility will provide a list of general default dimensions to enable the multiple source system integration.</span></span>

<span data-ttu-id="89818-287">下表列出了库存维度，它们将是库存可见性中的默认维度名称。</span><span class="sxs-lookup"><span data-stu-id="89818-287">The following table lists the inventory dimensions that will be the default dimension names in Inventory Visibility.</span></span>

| <span data-ttu-id="89818-288">维度类型</span><span class="sxs-lookup"><span data-stu-id="89818-288">Dimension type</span></span> | <span data-ttu-id="89818-289">维度名称</span><span class="sxs-lookup"><span data-stu-id="89818-289">Dimension name</span></span> |
|---|---|
| <span data-ttu-id="89818-290">产品</span><span class="sxs-lookup"><span data-stu-id="89818-290">Product</span></span> | `ColorId` |
| <span data-ttu-id="89818-291">产品</span><span class="sxs-lookup"><span data-stu-id="89818-291">Product</span></span> | `SizeId` |
| <span data-ttu-id="89818-292">产品</span><span class="sxs-lookup"><span data-stu-id="89818-292">Product</span></span> | `StyleId` |
| <span data-ttu-id="89818-293">产品</span><span class="sxs-lookup"><span data-stu-id="89818-293">Product</span></span> | `ConfigId` |
| <span data-ttu-id="89818-294">跟踪</span><span class="sxs-lookup"><span data-stu-id="89818-294">Tracking</span></span> | `BatchId` |
| <span data-ttu-id="89818-295">跟踪</span><span class="sxs-lookup"><span data-stu-id="89818-295">Tracking</span></span> | `SerialId` |
| <span data-ttu-id="89818-296">库位</span><span class="sxs-lookup"><span data-stu-id="89818-296">Location</span></span> | `LocationId` |
| <span data-ttu-id="89818-297">库位</span><span class="sxs-lookup"><span data-stu-id="89818-297">Location</span></span> | `SiteId` |
| <span data-ttu-id="89818-298">库存状态</span><span class="sxs-lookup"><span data-stu-id="89818-298">Inventory Status</span></span> | `StatusId` |
| <span data-ttu-id="89818-299">仓库特定</span><span class="sxs-lookup"><span data-stu-id="89818-299">Warehouse Specific</span></span> | `WMSLocationId` |
| <span data-ttu-id="89818-300">仓库特定</span><span class="sxs-lookup"><span data-stu-id="89818-300">Warehouse Specific</span></span> | `WMSPalletId` |
| <span data-ttu-id="89818-301">仓库特定</span><span class="sxs-lookup"><span data-stu-id="89818-301">Warehouse Specific</span></span> | `LicensePlateId` |

> [!NOTE]
> <span data-ttu-id="89818-302">上表中列出的维度类型仅供参考。</span><span class="sxs-lookup"><span data-stu-id="89818-302">The dimension type listed in the previous table is for reference only.</span></span> <span data-ttu-id="89818-303">您无需在库存可见性中定义维度类型。</span><span class="sxs-lookup"><span data-stu-id="89818-303">You don't need to define the dimension type in Inventory Visibility.</span></span>

<span data-ttu-id="89818-304">如果自定义维度已存在，并且在由库存可见性使用时需要流入默认值，可以在库存可见性中配置 **自定义维度** 名称。</span><span class="sxs-lookup"><span data-stu-id="89818-304">If a custom dimension exists and needs to flow to a default value when consumed by Inventory Visibility, you can configure the **Custom dimension** name in Inventory Visibility.</span></span>

<span data-ttu-id="89818-305">外部系统通过 RESTful API 访问库存可见性，这些 API 可以查询给定维度集上的现有信息。</span><span class="sxs-lookup"><span data-stu-id="89818-305">External systems access Inventory Visibility through RESTful APIs that enable on-hand information on given sets of dimensions to be queried.</span></span> <span data-ttu-id="89818-306">对于集成，库存可见性使您能够在库存可见性中将 *外部通道数据源* 以及来源维度配置为 *目标维度*。</span><span class="sxs-lookup"><span data-stu-id="89818-306">For the integration, Inventory Visibility enables you to configure the *external channel data source* and the source dimension to the *target dimensions* in Inventory Visibility.</span></span>

<span data-ttu-id="89818-307">目标维度应为以下维度之一：</span><span class="sxs-lookup"><span data-stu-id="89818-307">The target dimensions should be one of the following:</span></span>

- <span data-ttu-id="89818-308">库存可见性中的默认维度</span><span class="sxs-lookup"><span data-stu-id="89818-308">Default dimensions in Inventory Visibility</span></span>
- <span data-ttu-id="89818-309">自定义维度</span><span class="sxs-lookup"><span data-stu-id="89818-309">Custom dimensions</span></span>

<span data-ttu-id="89818-310">维度配置的目的是标准化维度查询和维度发布事件的多系统集成。</span><span class="sxs-lookup"><span data-stu-id="89818-310">The purpose of dimension configuration is to standardize the multi-system integration for the query on dimensions and the posting event with dimensions.</span></span>

#### <a name="indexing"></a><span data-ttu-id="89818-311">正在索引</span><span class="sxs-lookup"><span data-stu-id="89818-311">Indexing</span></span>

<span data-ttu-id="89818-312">在大多数情况下，库存现有查询不仅会处于最高的“总计”级别，而且您可能希望查看基于库存维度汇总的结果。</span><span class="sxs-lookup"><span data-stu-id="89818-312">Most of the time, the inventory on-hand query will not only be on the highest "total" level, but you may want to see results aggregated based on the inventory dimensions.</span></span>

<span data-ttu-id="89818-313">库存可视性通过允许您设置基于维度或维度组合的索引来提供灵活性。</span><span class="sxs-lookup"><span data-stu-id="89818-313">Inventory Visibility provides flexibility by allowing you to set up the indexes, which are based on the dimension or the combination of the dimensions.</span></span>

> [!NOTE]
> <span data-ttu-id="89818-314">当前，您最多只能配置五个索引。</span><span class="sxs-lookup"><span data-stu-id="89818-314">Currently, you can only configure indexes to a maximum of five.</span></span> <span data-ttu-id="89818-315">您需要在实施之前仔细考虑将使用哪个维度或维度组合，以确保它可以满足您的业务需求。</span><span class="sxs-lookup"><span data-stu-id="89818-315">You need to carefully consider which dimension or dimension combination you will use before the implementation to ensure that it will meet your business needs.</span></span> <span data-ttu-id="89818-316">例如，如果要查询产品，如下所示：</span><span class="sxs-lookup"><span data-stu-id="89818-316">For example, if you want to query products as follows:</span></span>

- <span data-ttu-id="89818-317">按 *颜色* 和 *尺寸* 维度查询汇总的现有产品。</span><span class="sxs-lookup"><span data-stu-id="89818-317">Query the aggregated product on-hand by the *Color* and *Size* dimensions.</span></span>
- <span data-ttu-id="89818-318">在某些情况下，您只想查询全部产品。</span><span class="sxs-lookup"><span data-stu-id="89818-318">In some cases, you just want to query on the product in total.</span></span>

<span data-ttu-id="89818-319">您将有两个定义如下的索引：</span><span class="sxs-lookup"><span data-stu-id="89818-319">You would have two indexes defined as the following:</span></span>

- `["ColorId", "SizeId"]`
- `[]`

<span data-ttu-id="89818-320">空括号将基于分区内的产品 ID 进行汇总。</span><span class="sxs-lookup"><span data-stu-id="89818-320">The empty bracket will aggregate based on the product ID within the partition.</span></span>

<span data-ttu-id="89818-321">索引定义如何基于 `groupBy` 查询设置对结果进行分组。</span><span class="sxs-lookup"><span data-stu-id="89818-321">The indexing defines how you can group your results based on the `groupBy` query setting.</span></span> <span data-ttu-id="89818-322">在这种情况下，如果您未定义任何 `groupBy` 值，您将按 `productid` 获得总计。</span><span class="sxs-lookup"><span data-stu-id="89818-322">In this case if you don't define any `groupBy` values, you'll get totals by `productid`.</span></span> <span data-ttu-id="89818-323">否则，如果您将 `groupBy` 定义为 `groupBy=ColorId&groupBy=SizeId`，将基于系统中的不同颜色和尺寸组合返回多行。</span><span class="sxs-lookup"><span data-stu-id="89818-323">Otherwise, if you define `groupBy` as `groupBy=ColorId&groupBy=SizeId`, you'll get multiple lines returned, based on the different color and size combinations in the system.</span></span>

<span data-ttu-id="89818-324">您可以将查询条件放入请求正文中。</span><span class="sxs-lookup"><span data-stu-id="89818-324">You can put your query criteria in the request body.</span></span>

<span data-ttu-id="89818-325">下面是有关具有颜色和尺寸组合的产品的示例查询。</span><span class="sxs-lookup"><span data-stu-id="89818-325">Here is a sample query on the product with color and size combination.</span></span>

```json
{
    "filters": {
        "OrganizationId": ["usmf"],
        "ProductId": ["MyProduct"],
        "LocationId": ["21"],
        "SiteId": ["2"],
        "ColorId": ["Red"]
    },
    "groupByValues": [
        "SizeId",
        "ColorId"
    ],
    "returnNegative": true
}
```

#### <a name="custom-measurement"></a><span data-ttu-id="89818-326">自定义度量</span><span class="sxs-lookup"><span data-stu-id="89818-326">Custom measurement</span></span>

<span data-ttu-id="89818-327">默认度量数量将链接到 Supply Chain Management。</span><span class="sxs-lookup"><span data-stu-id="89818-327">The default measurement quantities are linked to Supply Chain Management.</span></span> <span data-ttu-id="89818-328">但是，您可能需要有由默认度量的组合组成的数量。</span><span class="sxs-lookup"><span data-stu-id="89818-328">However, you may want to have a quantity that is made up of a combination of the default measurements.</span></span> <span data-ttu-id="89818-329">为此，您可以配置自定义数量，它们将添加到现有查询的输出中。</span><span class="sxs-lookup"><span data-stu-id="89818-329">To do this, you can have a configuration of custom quantities, which will be added to the output of the on-hand queries.</span></span>

<span data-ttu-id="89818-330">该功能仅允许您定义一组要添加的度量，和/或一组要减去的度量，以便形成自定义度量。</span><span class="sxs-lookup"><span data-stu-id="89818-330">The functionality simply allows you to define a set of measures that will be added, and/or a set of measures that will be subtracted, in order to form the custom measurement.</span></span>

<span data-ttu-id="89818-331">例如，在以下查询条件下，您将自定义度量数量配置为由消耗系统消耗的 `MyCustomAvailableforReservation`。</span><span class="sxs-lookup"><span data-stu-id="89818-331">For example, with the following query condition, you will configure the custom measurement quantity as `MyCustomAvailableforReservation` to be consumed by the consumption system.</span></span>

```json
[
    {
        "productId": "MyProduct",
        "dimensions": {
            "colorid": "Red"
        },
        "quantities": {
            "mypos": {
                "outbound": 20.0,
                "inbound": 80.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "exterchannel": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            }
        }
    }
]

```



| <span data-ttu-id="89818-332">消耗系统</span><span class="sxs-lookup"><span data-stu-id="89818-332">Consumption system</span></span> | <span data-ttu-id="89818-333">计算的度量</span><span class="sxs-lookup"><span data-stu-id="89818-333">Calculated measurers</span></span> | <span data-ttu-id="89818-334">数据源</span><span class="sxs-lookup"><span data-stu-id="89818-334">Data source</span></span> | <span data-ttu-id="89818-335">修饰符</span><span class="sxs-lookup"><span data-stu-id="89818-335">Modifier</span></span> | <span data-ttu-id="89818-336">修饰符计算类型</span><span class="sxs-lookup"><span data-stu-id="89818-336">Modifier calculation type</span></span> |
|---|---|---|---|---|
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `availphysical` | <span data-ttu-id="89818-337">增加额</span><span class="sxs-lookup"><span data-stu-id="89818-337">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedintotal` | <span data-ttu-id="89818-338">增加额</span><span class="sxs-lookup"><span data-stu-id="89818-338">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedreserved` | <span data-ttu-id="89818-339">减</span><span class="sxs-lookup"><span data-stu-id="89818-339">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `inbound` | <span data-ttu-id="89818-340">增加额</span><span class="sxs-lookup"><span data-stu-id="89818-340">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `outbound` | <span data-ttu-id="89818-341">减</span><span class="sxs-lookup"><span data-stu-id="89818-341">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `received` | <span data-ttu-id="89818-342">增加额</span><span class="sxs-lookup"><span data-stu-id="89818-342">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `scheduled` | <span data-ttu-id="89818-343">增加额</span><span class="sxs-lookup"><span data-stu-id="89818-343">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `issued` | <span data-ttu-id="89818-344">减</span><span class="sxs-lookup"><span data-stu-id="89818-344">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `reserved` | <span data-ttu-id="89818-345">减</span><span class="sxs-lookup"><span data-stu-id="89818-345">Subtraction</span></span> |

<span data-ttu-id="89818-346">这样，对自定义度量数量的查询将返回以下输出。</span><span class="sxs-lookup"><span data-stu-id="89818-346">With that, the query on the custom measurement quantity will return the following output.</span></span>

```json
[
    {
        "productId": "MyProduct",
        "dimensions": {
            "colorid": "Red"
        },
        "quantities": {
            "mypos": {
                "outbound": 20.0,
                "inbound": 80.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "exterchannel": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            },
            "CustomChannel": {
                "MyCustomAvailableforReservation": 220.0
            }
        }
    }
]
```

<span data-ttu-id="89818-347">`MyCustomAvailableforReservation` 输出基于自定义度量中的计算设置，如下所示：</span><span class="sxs-lookup"><span data-stu-id="89818-347">The `MyCustomAvailableforReservation` output is based on the calculation setting in the custom measurements as:</span></span>  
 <span data-ttu-id="89818-348">*100 + 50 + 80 + 90 + 30 &ndash; 10 &ndash; 20 &ndash; 60 &ndash; 40 = 220*</span><span class="sxs-lookup"><span data-stu-id="89818-348">*100 + 50 + 80 + 90 + 30 &ndash; 10 &ndash; 20 &ndash; 60 &ndash; 40 = 220*</span></span>

### <a name="posting-on-hand-changes"></a><span data-ttu-id="89818-349">发布现有更改</span><span class="sxs-lookup"><span data-stu-id="89818-349">Posting on-hand changes</span></span>

<span data-ttu-id="89818-350">该事件将发布到的确切 URL 将取决于您的地理区域。</span><span class="sxs-lookup"><span data-stu-id="89818-350">The exact URL that the event will be posted to will depend on your geographical region.</span></span> <span data-ttu-id="89818-351">它将采用以下形式：</span><span class="sxs-lookup"><span data-stu-id="89818-351">It will take the form:</span></span>

`https://{serviceURL}/api/environment/{environmentId}/onhand`

<span data-ttu-id="89818-352">经过身份验证后，此 URL 可以与 HTTP `POST` 方法一起使用以将现有更改事件发送到服务。</span><span class="sxs-lookup"><span data-stu-id="89818-352">When authenticated, this URL can be used along with the HTTP `POST` method to send on-hand change events to the service.</span></span>

<span data-ttu-id="89818-353">特殊标题用于通过 HTTP 请求与 Dynamics 365 服务通信，表示数据链接到的 Supply Chain Management 实例的环境 ID。</span><span class="sxs-lookup"><span data-stu-id="89818-353">A special header is used for communicating with Dynamics 365 services through HTTP requests, denoting the environment ID of the Supply Chain Management instance the data is linked to.</span></span> <span data-ttu-id="89818-354">例如:</span><span class="sxs-lookup"><span data-stu-id="89818-354">For example:</span></span>

`x-ms-environment-id: 2db79622-f97a-4d64-9844-d12efed41796`

#### <a name="posting-on-hand-changes-query-example-1"></a><span data-ttu-id="89818-355">发布现有更改查询示例 1</span><span class="sxs-lookup"><span data-stu-id="89818-355">Posting on-hand changes query example 1</span></span>

<span data-ttu-id="89818-356">本示例显示将在 Power Apps 中设置维度配置的场景。</span><span class="sxs-lookup"><span data-stu-id="89818-356">This example shows a scenario where you will set up the dimension configuration in Power Apps.</span></span>

<span data-ttu-id="89818-357">使用以下查询在以 Power Apps 中配置维度映射：</span><span class="sxs-lookup"><span data-stu-id="89818-357">Use the following query to configure the dimension mapping in Power Apps:</span></span>

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

<span data-ttu-id="89818-358">现在，您可以指定 `dimensionDataSource` 并在查询中使用自定义维度。</span><span class="sxs-lookup"><span data-stu-id="89818-358">Now you can specify the `dimensionDataSource` and use custom dimensions in your queries.</span></span> <span data-ttu-id="89818-359">系统会自动将自定义维度转换为基本维度。</span><span class="sxs-lookup"><span data-stu-id="89818-359">The system will automatically convert custom dimensions to base dimensions.</span></span>

```json
{
    "id": "demo-test-00007",
    "organizationId": "usmf",
    "productId": "MyProduct",
    "quantities": {
        "pos": {
            "Outbound": 1
        }
    },
    "dimensionDataSource": "pos",
    "dimensions": {
        "PosSizeId": "Large",
        "PosColorId": "Red",
        "PosSiteId": "2",
        "PosLocationId": "21"
    }
}
```

#### <a name="posting-on-hand-changes-query-example-2"></a><span data-ttu-id="89818-360">发布现有更改查询示例 2</span><span class="sxs-lookup"><span data-stu-id="89818-360">Posting on-hand changes query example 2</span></span>

<span data-ttu-id="89818-361">本示例显示不在 Power Apps 中为维度配置设置映射，因此发布还应该使用基本维度的场景。</span><span class="sxs-lookup"><span data-stu-id="89818-361">This example shows a scenario where no mappings are set up for the dimension configuration in Power Apps, so the posting should also use the base dimensions.</span></span> <span data-ttu-id="89818-362">当 `dimensionDataSource` 字段为 null、空或空白时，所有维度都必须是基本维度。</span><span class="sxs-lookup"><span data-stu-id="89818-362">All dimensions must be base dimensions when the `dimensionDataSource` field is null, empty, or whitespace.</span></span>

```json
{
    "id": "demo-test-00007",
    "organizationId": "usmf",
    "productId": "MyProduct",
    "quantities": {
        "pos": {
            "Outbound": 1
        }
    },
    "dimensions": {
        "SizeId": "Large",
        "ColorId": "Red",
        "SiteId": "2",
        "LocationId": "21"
    }
}
```

#### <a name="json-document-field-properties"></a><span data-ttu-id="89818-363">JSON 文档字段属性</span><span class="sxs-lookup"><span data-stu-id="89818-363">JSON document field properties</span></span>

<span data-ttu-id="89818-364">先前提供的 JSON 查询示例中的字段具有下表中列出的属性。</span><span class="sxs-lookup"><span data-stu-id="89818-364">The fields from the JSON query examples provided previously have the properties listed in the following table.</span></span>

| <span data-ttu-id="89818-365">字段 ID</span><span class="sxs-lookup"><span data-stu-id="89818-365">Field ID</span></span> | <span data-ttu-id="89818-366">说明</span><span class="sxs-lookup"><span data-stu-id="89818-366">Description</span></span> |
|---|---|
| `id` | <span data-ttu-id="89818-367">特定更改事件的唯一 ID。</span><span class="sxs-lookup"><span data-stu-id="89818-367">A unique ID for the specific change event.</span></span> <span data-ttu-id="89818-368">此 ID 用于确保如果在发布过程中与服务的通信失败，重新提交事件不会导致同一事件在系统中计入两次。</span><span class="sxs-lookup"><span data-stu-id="89818-368">This ID is used to ensure that if communication with the service fails during posting, resubmitting the event would not result in the same event being counted twice in the system.</span></span> |
| `organizationId` | <span data-ttu-id="89818-369">链接到事件的组织的标识符。</span><span class="sxs-lookup"><span data-stu-id="89818-369">The identifier of the organization linked to the event.</span></span> <span data-ttu-id="89818-370">这将映射到 Supply Chain Management 组织或数据区域 ID。</span><span class="sxs-lookup"><span data-stu-id="89818-370">This maps to Supply Chain Management organizations or data area IDs.</span></span> |
| `productId` | <span data-ttu-id="89818-371">所讨论的订单的标识符。</span><span class="sxs-lookup"><span data-stu-id="89818-371">The identifier of the product in question.</span></span> |
| `quantity` | <span data-ttu-id="89818-372">需要更改现有量所依据的数量。</span><span class="sxs-lookup"><span data-stu-id="89818-372">The quantity by which the on-hand needs to be changed.</span></span> <span data-ttu-id="89818-373">例如，如果将 10 个新的百吉饼添加到货位上，该值将为 10。</span><span class="sxs-lookup"><span data-stu-id="89818-373">If, for instance, 10 new bagels were added to a shelf, this value would be 10.</span></span> <span data-ttu-id="89818-374">然后，如果将 3 个百吉饼从货位中下架或出售，则该值将为 -3。</span><span class="sxs-lookup"><span data-stu-id="89818-374">If 3 bagels were then removed from the shelf or sold, this value would be -3.</span></span> |
| `dimensionDataSource` | <span data-ttu-id="89818-375">在发布更改事件和查询中使用的维度的数据源。</span><span class="sxs-lookup"><span data-stu-id="89818-375">The data source of the dimensions used in the posting change event and query.</span></span> <span data-ttu-id="89818-376">如果指定数据源，您可以使用来自指定数据源的自定义维度。</span><span class="sxs-lookup"><span data-stu-id="89818-376">If you specify the data source, you can use the custom dimensions from the specified data source.</span></span> <span data-ttu-id="89818-377">使用维度配置，库存可见性可以将自定义维度映射到常规默认维度。</span><span class="sxs-lookup"><span data-stu-id="89818-377">With the dimension configuration, Inventory Visibility can map the custom dimensions to the general default dimensions.</span></span> <span data-ttu-id="89818-378">如果未指定 `dimensionDataSource`，只能在查询中使用常规默认维度。</span><span class="sxs-lookup"><span data-stu-id="89818-378">If the `dimensionDataSource` is not specified, you can only use the general default dimensions in your queries.</span></span>   |
| `dimensions` | <span data-ttu-id="89818-379">键/值对的动态包。</span><span class="sxs-lookup"><span data-stu-id="89818-379">A dynamic bag of key/value pairs.</span></span> <span data-ttu-id="89818-380">这些将映射到 Supply Chain Management 中的某些维度，但是您也可以添加自定义维度（例如 *源*），这可以表示事件是来自 Supply Chain Management 还是外部系统。</span><span class="sxs-lookup"><span data-stu-id="89818-380">These will map to some of the dimensions in Supply Chain Management, but you could also add custom dimensions (like *Source*) that may denote if the event was coming from Supply Chain Management or an external system.</span></span> |

### <a name="querying-current-on-hand"></a><span data-ttu-id="89818-381">查询当前现有量</span><span class="sxs-lookup"><span data-stu-id="89818-381">Querying current on-hand</span></span>

<span data-ttu-id="89818-382">用于查询当前现有量的终结点将具有类似的 URL：</span><span class="sxs-lookup"><span data-stu-id="89818-382">The endpoint for querying the current on-hand will have a similar URL:</span></span>

`https://{serviceURL}/api/environment/{environmentId}/onhand/indexquery`

<span data-ttu-id="89818-383">将使用 HTTP `POST` 方法查询它。</span><span class="sxs-lookup"><span data-stu-id="89818-383">It will be queried with the HTTP `POST` method.</span></span>

#### <a name="current-on-hand-query-example-1"></a><span data-ttu-id="89818-384">当前现有查询示例 1</span><span class="sxs-lookup"><span data-stu-id="89818-384">Current on-hand query example 1</span></span>

<span data-ttu-id="89818-385">本示例显示已在 Power Apps 中完成维度配置的场景。</span><span class="sxs-lookup"><span data-stu-id="89818-385">This example shows a scenario where you have already completed the dimension configuration in Power Apps.</span></span>

<span data-ttu-id="89818-386">使用以下查询在以 Power Apps 中配置维度映射：</span><span class="sxs-lookup"><span data-stu-id="89818-386">Use the following query to configure the dimension mapping in Power Apps:</span></span>

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

<span data-ttu-id="89818-387">现在，您可以指定 `dimensionDataSource` 并在查询中使用自定义维度。</span><span class="sxs-lookup"><span data-stu-id="89818-387">Now you can specify the `dimensionDataSource` and use custom dimensions in your queries.</span></span> <span data-ttu-id="89818-388">系统会自动将自定义维度转换为基本维度。</span><span class="sxs-lookup"><span data-stu-id="89818-388">The system will automatically convert custom dimensions to base dimensions.</span></span> <span data-ttu-id="89818-389">您可以在 `filters` 中指定 `DimensionDataSource`，并在 `filters` 和 `groupByValues` 中指定自定义维度。</span><span class="sxs-lookup"><span data-stu-id="89818-389">You can specify the `DimensionDataSource` in `filters` and specify custom dimensions in both `filters` and `groupByValues`.</span></span> <span data-ttu-id="89818-390">系统会自动将自定义维度转换为基本维度。</span><span class="sxs-lookup"><span data-stu-id="89818-390">The system will automatically convert custom dimensions to base dimensions.</span></span>

```json
{
    "filters": {
        "OrganizationId": ["usmf"],
        "ProductId": ["MyProduct"],
        "DimensionDataSource": ["Pos"],
        "PosLocationId": ["21"],
        "PosSiteId": ["2"],
        "PosColorId": ["Red"]
    },
    "groupByValues": [
        "PosSizeId",
        "PosColorId"
    ],
    "returnNegative": true
}
```

#### <a name="current-on-hand-query-example-2"></a><span data-ttu-id="89818-391">当前现有查询示例 2</span><span class="sxs-lookup"><span data-stu-id="89818-391">Current on-hand query example 2</span></span>

<span data-ttu-id="89818-392">本示例显示不在 Power Apps 中为维度配置设置映射，因此发布还应该使用基本维度的场景。</span><span class="sxs-lookup"><span data-stu-id="89818-392">This example shows a scenario where no mappings are set up for the dimension configuration in Power Apps, so the posting should also use the base dimensions.</span></span> <span data-ttu-id="89818-393">当在 `filters` 下 `dimensionDataSource` 字段为 null、空或空白时，所有维度都必须是基本维度。</span><span class="sxs-lookup"><span data-stu-id="89818-393">All dimensions must be base dimensions when the `dimensionDataSource` field, under `filters` is null, empty, or whitespace.</span></span>

```json
{
    "filters": {
        "OrganizationId": ["usmf"],
        "ProductId": ["MyProduct"],
        "LocationId": ["21"],
        "SiteId": ["2"],
        "ColorId": ["Red"]
    },
    "groupByValues": [
        "SizeId",
        "ColorId"
    ],
    "returnNegative": true
}
```

#### <a name="example-return-result"></a><span data-ttu-id="89818-394">返回结果示例</span><span class="sxs-lookup"><span data-stu-id="89818-394">Example return result</span></span>

<span data-ttu-id="89818-395">前面示例中显示的查询可能返回如下结果。</span><span class="sxs-lookup"><span data-stu-id="89818-395">The queries shown in the previous examples could return a result like this.</span></span>

```json
[
    {
        "productId": "MyProduct",
        "dimensions": {
            "colorid": "Red"
        },
        "quantities": {
            "mypos": {
                "outbound": 20.0,
                "inbound": 80.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "exterchannel": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            },
            "CustomChannel": {
                "MyCustomAvailableforReservation": 220.0
            }
        }
    }
]
```

<span data-ttu-id="89818-396">请注意，数量字段将构造为度量及其相关值的字典。</span><span class="sxs-lookup"><span data-stu-id="89818-396">Note that the quantities fields are structured as a dictionary of measures and their associated values.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
