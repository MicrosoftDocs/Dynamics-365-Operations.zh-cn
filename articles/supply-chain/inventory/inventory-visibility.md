---
title: 库存可见性加载项
description: 本主题介绍如何为 Dynamics 365 Supply Chain Management 安装和配置库存可见性加载项。
author: chuzheng
manager: tfehr
ms.date: 10/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-10-26
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 2976153a6a7e4b4130e8f7673ed128945aeabf65
ms.sourcegitcommit: 03c2e1717b31e4c17ee7bb9004d2ba8cf379a036
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "4625057"
---
# <a name="inventory-visibility-add-in"></a><span data-ttu-id="75300-103">库存可见性加载项</span><span class="sxs-lookup"><span data-stu-id="75300-103">Inventory Visibility Add-in</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="75300-104">库存可见性加载项是一项独立且高度可扩展的微服务，可实现实时现有库存跟踪，并提供库存可见性的全局视图。</span><span class="sxs-lookup"><span data-stu-id="75300-104">The Inventory Visibility Add-in is an independent and highly scalable microservice that enables real-time on-hand inventory tracking, thus providing a global view of inventory visibility.</span></span>

<span data-ttu-id="75300-105">通过低级别 SQL 集成，准实时地将与现有库存相关的所有信息导出到服务中。</span><span class="sxs-lookup"><span data-stu-id="75300-105">All information that relates to on-hand inventory is exported to the service in near real-time through low-level SQL integration.</span></span> <span data-ttu-id="75300-106">外部系统通过 RESTful API 访问服务，以查询有关给定维度集的现有信息，从而检索可用现有位置的列表。</span><span class="sxs-lookup"><span data-stu-id="75300-106">External systems access the service through RESTful APIs to query on-hand information on given sets of dimensions, thus retrieving a list of available on-hand positions.</span></span>

<span data-ttu-id="75300-107">库存可见性是基于 Common Data Service 生成的微服务，这意味着您可以通过生成 Power Apps 和应用 Power BI 来扩展它，从而提供自定义功能以满足您的业务需求。</span><span class="sxs-lookup"><span data-stu-id="75300-107">Inventory Visibility is a microservice built on the Common Data Service, which means you can extend it by building Power Apps and applying Power BI to provide customized functionality to meet your business requirements.</span></span> <span data-ttu-id="75300-108">也可以升级索引以进行库存查询。</span><span class="sxs-lookup"><span data-stu-id="75300-108">It is also possible to upgrade the index to do inventory queries.</span></span>

<span data-ttu-id="75300-109">库存可见性提供配置选项，使其可以与多个第三方系统集成。</span><span class="sxs-lookup"><span data-stu-id="75300-109">Inventory Visibility provides configuration options that let it integrate with multiple third-party systems.</span></span> <span data-ttu-id="75300-110">它支持标准化的库存维度、自定义的可扩展性以及标准化的可配置的计算数量。</span><span class="sxs-lookup"><span data-stu-id="75300-110">It supports the standardized inventory dimension, customized extensibility, and standardized, configurable calculated quantities.</span></span>

<span data-ttu-id="75300-111">本主题介绍如何为 Dynamics 365 Supply Chain Management 安装和配置库存可见性加载项，以及如何使用其应用程序编程接口 (API)。</span><span class="sxs-lookup"><span data-stu-id="75300-111">This topic describes how to install and configure the Inventory Visibility Add-in for Dynamics 365 Supply Chain Management, and how to use its application programming interface (API).</span></span>

## <a name="install-the-inventory-visibility-add-in"></a><span data-ttu-id="75300-112">安装库存可见性加载项</span><span class="sxs-lookup"><span data-stu-id="75300-112">Install the Inventory Visibility Add-in</span></span>

<span data-ttu-id="75300-113">您需要使用 Microsoft Dynamics Lifecycle Services (LCS) 安装库存可见性加载项。</span><span class="sxs-lookup"><span data-stu-id="75300-113">You need to install the Inventory Visibility Add-in using Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="75300-114">LCS 是一个协作门户，可提供环境和一组定期更新的服务，以帮助您管理 Dynamics 365 Finance and Operations 应用的应用程序生命周期。</span><span class="sxs-lookup"><span data-stu-id="75300-114">LCS is a collaboration portal that provides an environment and a set of regularly updated services that help you manage the application lifecycle of your Dynamics 365 Finance and Operations apps.</span></span>

<span data-ttu-id="75300-115">有关详细信息，请参阅 [Lifecycle Services 资源](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/lcs)。</span><span class="sxs-lookup"><span data-stu-id="75300-115">For more information, see [Lifecycle Services resources](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/lcs).</span></span>

### <a name="prerequisites"></a><span data-ttu-id="75300-116">先决条件</span><span class="sxs-lookup"><span data-stu-id="75300-116">Prerequisites</span></span>

<span data-ttu-id="75300-117">在安装库存可见性加载项之前，您必须执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="75300-117">Before you install the Inventory Visibility Add-in, you must do the following:</span></span>

- <span data-ttu-id="75300-118">获取至少部署了一个环境的 LCS 实施项目。</span><span class="sxs-lookup"><span data-stu-id="75300-118">Obtain an LCS implementation project with at least one environment deployed.</span></span>
- <span data-ttu-id="75300-119">在 LCS 中为您的产品/服务生成测试密钥。</span><span class="sxs-lookup"><span data-stu-id="75300-119">Generate the beta keys for your offering in LCS.</span></span>
- <span data-ttu-id="75300-120">在 LCS 中为您的用户启用产品/服务的测试密钥。</span><span class="sxs-lookup"><span data-stu-id="75300-120">Enable the beta keys for your offering for your user in LCS.</span></span>
- <span data-ttu-id="75300-121">请与 Microsoft 库存可见性产品团队联系，并提供要在其中部署库存可见性加载项的环境 ID。</span><span class="sxs-lookup"><span data-stu-id="75300-121">Contact the Microsoft Inventory Visibility product team and provide an environment ID where you want to deploy the Inventory Visibility Add-in.</span></span>

<span data-ttu-id="75300-122">如果您对这些先决条件有任何疑问，请与库存可视性产品团队联系。</span><span class="sxs-lookup"><span data-stu-id="75300-122">If you have any questions about these prerequisites, please contact the Inventory Visibility product team.</span></span>

### <a name="install-the-add-in"></a><a name="install-add-in"></a><span data-ttu-id="75300-123">安装加载项</span><span class="sxs-lookup"><span data-stu-id="75300-123">Install the add-in</span></span>

<span data-ttu-id="75300-124">若要安装库存可见性加载项，请执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="75300-124">To install the Inventory Visibility Add-in, do the following:</span></span>

1. <span data-ttu-id="75300-125">登录到 [Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index) 门户。</span><span class="sxs-lookup"><span data-stu-id="75300-125">Sign in to the [Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index) portal.</span></span>
1. <span data-ttu-id="75300-126">在主页上，选择在其中部署环境的项目。</span><span class="sxs-lookup"><span data-stu-id="75300-126">On the home page, select the project where your environment is deployed.</span></span>
1. <span data-ttu-id="75300-127">在项目页面上，选择要在其中安装加载项的环境。</span><span class="sxs-lookup"><span data-stu-id="75300-127">On the project page, select the environment where you want to install the add-in.</span></span>
1. <span data-ttu-id="75300-128">在环境页面上，向下滚动，直到看到 **环境加载项** 部分。</span><span class="sxs-lookup"><span data-stu-id="75300-128">On the environment page, scroll down until you see the **Environment add-ins** section.</span></span> <span data-ttu-id="75300-129">如果看不到该部分，请确保已完全处理必备的测试密钥。</span><span class="sxs-lookup"><span data-stu-id="75300-129">If the section isn't visible, make sure the prerequisite beta keys have been fully processed.</span></span>
1. <span data-ttu-id="75300-130">在 **环境加载项** 部分中，选择 **安装新加载项**。</span><span class="sxs-lookup"><span data-stu-id="75300-130">In the **Environment add-ins** section, select **Install a new add-in**.</span></span>
    <span data-ttu-id="75300-131">![LCS 中的环境页面](media/inventory-visibility-environment.png "LCS 中的环境页面")</span><span class="sxs-lookup"><span data-stu-id="75300-131">![The environment page in LCS](media/inventory-visibility-environment.png "The environment page in LCS")</span></span>
1. <span data-ttu-id="75300-132">选择 **安装新加载项** 链接。</span><span class="sxs-lookup"><span data-stu-id="75300-132">Select the **Install a new add-in** link.</span></span> <span data-ttu-id="75300-133">将打开可用加载项的列表。</span><span class="sxs-lookup"><span data-stu-id="75300-133">A list of available add-ins opens.</span></span>
1. <span data-ttu-id="75300-134">从列表中选择 **库存服务**。</span><span class="sxs-lookup"><span data-stu-id="75300-134">Select **Inventory service** from the list.</span></span> <span data-ttu-id="75300-135">（请注意，这现在可能作为 **Dynamics 365 Supply Chain Management 的库存可见性加载项** 列出。）</span><span class="sxs-lookup"><span data-stu-id="75300-135">(Note, this may now be listed as **Inventory Visibility Add-in for Dynamics 365 Supply Chain Management**.)</span></span>
1. <span data-ttu-id="75300-136">为您的环境输入以下字段的值：</span><span class="sxs-lookup"><span data-stu-id="75300-136">Enter values for the following fields for your environment:</span></span>

    - <span data-ttu-id="75300-137">**AAD 应用程序 ID**</span><span class="sxs-lookup"><span data-stu-id="75300-137">**AAD application ID**</span></span>
    - <span data-ttu-id="75300-138">**AAD 租户 ID**</span><span class="sxs-lookup"><span data-stu-id="75300-138">**AAD tenant ID**</span></span>

    <span data-ttu-id="75300-139">![加载项设置页面](media/inventory-visibility-setup.png "加载项设置页面")</span><span class="sxs-lookup"><span data-stu-id="75300-139">![Add in setup page](media/inventory-visibility-setup.png "Add-in setup page")</span></span>

1. <span data-ttu-id="75300-140">通过选中 **条款和条件** 复选框同意条款和条件。</span><span class="sxs-lookup"><span data-stu-id="75300-140">Agree to the terms and condition by selecting the **Terms and conditions** check box.</span></span>
1. <span data-ttu-id="75300-141">选择 **安装**。</span><span class="sxs-lookup"><span data-stu-id="75300-141">Select **Install**.</span></span> <span data-ttu-id="75300-142">加载项的状态将显示为 **正在安装**。</span><span class="sxs-lookup"><span data-stu-id="75300-142">The status of the add-in will show as **Installing**.</span></span> <span data-ttu-id="75300-143">完成后，刷新页面以查看状态更改为 **已安装**。</span><span class="sxs-lookup"><span data-stu-id="75300-143">When it's done, refresh the page to see the status change to **Installed**.</span></span>

### <a name="get-a-security-service-token"></a><span data-ttu-id="75300-144">获取安全服务令牌</span><span class="sxs-lookup"><span data-stu-id="75300-144">Get a security service token</span></span>

<span data-ttu-id="75300-145">若要获取安全服务令牌，请执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="75300-145">To get a security service token, do the following:</span></span>

1. <span data-ttu-id="75300-146">获取 `aadToken` 并调用终结点：https://securityservice.operations365.dynamics.com/token。</span><span class="sxs-lookup"><span data-stu-id="75300-146">Get your `aadToken` and call the endpoint: https://securityservice.operations365.dynamics.com/token.</span></span>
1. <span data-ttu-id="75300-147">使用 `aadToken` 替换正文中的 `client_assertion`。</span><span class="sxs-lookup"><span data-stu-id="75300-147">Replace the `client_assertion` in the body with your `aadToken`.</span></span>
1. <span data-ttu-id="75300-148">使用要在其中部署加载项的环境替换正文中的上下文。</span><span class="sxs-lookup"><span data-stu-id="75300-148">Replace the context in the body with the environment where you want to deploy the add-in.</span></span>
1. <span data-ttu-id="75300-149">使用以下项替换正文中的范围：</span><span class="sxs-lookup"><span data-stu-id="75300-149">Replace the scope in the body with the following:</span></span>

    - <span data-ttu-id="75300-150">MCK 的范围 -“https://inventoryservice.operations365.dynamics.cn/.default”</span><span class="sxs-lookup"><span data-stu-id="75300-150">Scope for MCK - "https://inventoryservice.operations365.dynamics.cn/.default"</span></span>  
    <span data-ttu-id="75300-151">（您可以在 `appsettings.mck.json` 中找到 MCK 的 Azure Active Directory 应用程序 ID 和租户 ID。）</span><span class="sxs-lookup"><span data-stu-id="75300-151">(You can find the Azure Active Directory application ID and tenant ID for MCK in `appsettings.mck.json`.)</span></span>
    - <span data-ttu-id="75300-152">PROD 的范围 -“https://inventoryservice.operations365.dynamics.com/.default”</span><span class="sxs-lookup"><span data-stu-id="75300-152">Scope for PROD - "https://inventoryservice.operations365.dynamics.com/.default"</span></span>  
    <span data-ttu-id="75300-153">（您可以在 `appsettings.prod.json` 中找到 PROD 的 Azure Active Directory 应用程序 ID 和租户 ID。）</span><span class="sxs-lookup"><span data-stu-id="75300-153">(You can find the Azure Active Directory application ID and tenant ID for PROD in `appsettings.prod.json`.)</span></span>

    <span data-ttu-id="75300-154">结果应类似于以下示例。</span><span class="sxs-lookup"><span data-stu-id="75300-154">The result should resemble the following example.</span></span>

    ```json
    {
        "grant_type": "client_credentials",
        "client_assertion_type":"aad_app",
        "client_assertion": "{**Your_AADToken**}",
        "scope":"**https://inventoryservice.operations365.dynamics.com/.default**",
        "context": "**5dbf6cc8-255e-4de2-8a25-2101cd5649b4**",
        "context_type": "finops-env"
    }
    ```

1. <span data-ttu-id="75300-155">您将获得 `access_token` 作为回应。</span><span class="sxs-lookup"><span data-stu-id="75300-155">You will get an `access_token` in response.</span></span> <span data-ttu-id="75300-156">您需要使用它作为持有者令牌来调用库存可见性 API。</span><span class="sxs-lookup"><span data-stu-id="75300-156">This is what you need as a bearer token to call the Inventory Visibility API.</span></span> <span data-ttu-id="75300-157">下面是一个示例。</span><span class="sxs-lookup"><span data-stu-id="75300-157">Here is an example.</span></span>

    ```json
    {
        "access_token": "{Returned_Token}",
        "token_type": "bearer",
        "expires_in": 1200
    }
    ```

### <a name="uninstall-the-add-in"></a><span data-ttu-id="75300-158">卸载加载项</span><span class="sxs-lookup"><span data-stu-id="75300-158">Uninstall the add-in</span></span>

<span data-ttu-id="75300-159">若要卸载加载项，请选择 **卸载**。</span><span class="sxs-lookup"><span data-stu-id="75300-159">To uninstall the add-in, select **Uninstall**.</span></span> <span data-ttu-id="75300-160">刷新 LCS，库存可见性加载项将会删除。</span><span class="sxs-lookup"><span data-stu-id="75300-160">Refresh LCS and the Inventory Visibility Add-in will be removed.</span></span> <span data-ttu-id="75300-161">卸载流程将删除加载项注册，还将启动作业以清理存储在服务中的所有业务数据。</span><span class="sxs-lookup"><span data-stu-id="75300-161">The uninstall process will remove the add-in registration and also start a job to clean up all of the business data stored in the service.</span></span>

## <a name="inventory-visibility-add-in-public-api"></a><span data-ttu-id="75300-162">库存可见性加载项公共 API</span><span class="sxs-lookup"><span data-stu-id="75300-162">Inventory Visibility Add-in public API</span></span>

<span data-ttu-id="75300-163">库存可见性加载项的公共 REST API 提供集成的几个特定终结点。</span><span class="sxs-lookup"><span data-stu-id="75300-163">The public REST API of the of the Inventory Visibility Add-in presents several specific endpoints of integration.</span></span> <span data-ttu-id="75300-164">它支持三种主要交互类型：</span><span class="sxs-lookup"><span data-stu-id="75300-164">It supports three main interaction types:</span></span>

- <span data-ttu-id="75300-165">从外部系统发布对加载项的现有更改。</span><span class="sxs-lookup"><span data-stu-id="75300-165">Posting on-hand changes to the add-in from an external system.</span></span>
- <span data-ttu-id="75300-166">从外部系统查询当前的现有数量。</span><span class="sxs-lookup"><span data-stu-id="75300-166">Querying current on-hand quantities from an external system.</span></span>
- <span data-ttu-id="75300-167">自动与现有 Supply Chain Management 同步。</span><span class="sxs-lookup"><span data-stu-id="75300-167">Automatic synchronization with Supply Chain Management on-hand.</span></span>

<span data-ttu-id="75300-168">自动同步不是公共 API 的一部分，而是在启用了库存可见性加载项的环境中在后台处理。</span><span class="sxs-lookup"><span data-stu-id="75300-168">The automatic synchronization isn't part of the public API but is instead handled in the background for environments that have enabled the Inventory Visibility Add-in.</span></span>

### <a name="authentication"></a><span data-ttu-id="75300-169">身份验证</span><span class="sxs-lookup"><span data-stu-id="75300-169">Authentication</span></span>

<span data-ttu-id="75300-170">平台安全令牌用于调用库存可见性加载项，因此您必须使用 Azure Active Directory 应用程序生成 Azure Active Directory 令牌。</span><span class="sxs-lookup"><span data-stu-id="75300-170">The platform security token is used to call the Inventory Visibility Add-in, so you must generate an Azure Active Directory token using your Azure Active Directory application.</span></span>

<span data-ttu-id="75300-171">有关如何获取安全令牌的详细信息，请参阅[安装库存可见性加载项](#install-add-in)。</span><span class="sxs-lookup"><span data-stu-id="75300-171">For more information about how to get the security token, see [Install the Inventory Visibility Add-in](#install-add-in).</span></span>

### <a name="configure-the-inventory-visibility-api"></a><span data-ttu-id="75300-172">配置库存可见性 API</span><span class="sxs-lookup"><span data-stu-id="75300-172">Configure the Inventory Visibility API</span></span>

<span data-ttu-id="75300-173">使用该服务之前，必须完成以下子部分中所述的配置。</span><span class="sxs-lookup"><span data-stu-id="75300-173">Before using the service, you must complete the configurations described in the following subsections.</span></span> <span data-ttu-id="75300-174">配置因您的环境的详细信息而异。</span><span class="sxs-lookup"><span data-stu-id="75300-174">The configuration may vary based on the details of your environment.</span></span> <span data-ttu-id="75300-175">它主要包括四个部分：</span><span class="sxs-lookup"><span data-stu-id="75300-175">It primarily includes four parts:</span></span>

- [<span data-ttu-id="75300-176">分区</span><span class="sxs-lookup"><span data-stu-id="75300-176">Partitioning</span></span>](#partitioning)
- [<span data-ttu-id="75300-177">维度配置</span><span class="sxs-lookup"><span data-stu-id="75300-177">Dimension configurations</span></span>](#dimension-configurations)
- [<span data-ttu-id="75300-178">正在索引</span><span class="sxs-lookup"><span data-stu-id="75300-178">Indexing</span></span>](#indexing)
- [<span data-ttu-id="75300-179">自定义度量</span><span class="sxs-lookup"><span data-stu-id="75300-179">Custom measurement</span></span>](#custom-measurement)

#### <a name="partitioning"></a><span data-ttu-id="75300-180">分区</span><span class="sxs-lookup"><span data-stu-id="75300-180">Partitioning</span></span>

<span data-ttu-id="75300-181">分区会显著影响库存可见性 API 的性能。</span><span class="sxs-lookup"><span data-stu-id="75300-181">Partitioning can significantly influence the performance of the Inventory Visibility API.</span></span> <span data-ttu-id="75300-182">最好定义一个方案，允许将数据进行小规模分组，同时仍然允许有意义的数据查询。</span><span class="sxs-lookup"><span data-stu-id="75300-182">It's a good idea to define a scheme that allows for small groupings of data while still allowing for meaningful data queries.</span></span>

<span data-ttu-id="75300-183">`organizationId`（Supply Chain Management 中的 `dataAreaId`）将始终是分区的一部分，并且默认情况下，库存可见性按维度（*站点 + 库位*）设置为分区。</span><span class="sxs-lookup"><span data-stu-id="75300-183">The `organizationId` (`dataAreaId` in Supply Chain Management) will always be part of the partitioning, and by default Inventory Visibility is set to partition by dimensions as *Site + Location*.</span></span> <span data-ttu-id="75300-184">这意味着必须始终使用在筛选器上定义的这些维度来查询服务。</span><span class="sxs-lookup"><span data-stu-id="75300-184">This means that the service must always be queried with these dimensions defined on the filters.</span></span>

> [!NOTE]
> <span data-ttu-id="75300-185">*站点* 和 *库位* 是库存可见性中的两个常规默认维度。</span><span class="sxs-lookup"><span data-stu-id="75300-185">*Site* and *Location* are two general default dimensions in Inventory Visibility.</span></span> <span data-ttu-id="75300-186">在 Supply Chain Management 中，这些维度称为 *站点* (`InventSiteId`) 和 *仓库* (`InventLocationId`)</span><span class="sxs-lookup"><span data-stu-id="75300-186">In Supply Chain Management, those dimensions are called *Site* (`InventSiteId`) and *Warehouse* (`InventLocationId`)</span></span>

### <a name="dimension-configurations"></a><span data-ttu-id="75300-187">维度配置</span><span class="sxs-lookup"><span data-stu-id="75300-187">Dimension configurations</span></span>

<span data-ttu-id="75300-188">库存可见性将提供常规默认维度的列表，以启用多源系统集成。</span><span class="sxs-lookup"><span data-stu-id="75300-188">Inventory Visibility will provide a list of general default dimensions to enable the multiple source system integration.</span></span>

<span data-ttu-id="75300-189">下表列出了库存维度，它们将是库存可见性中的默认维度名称。</span><span class="sxs-lookup"><span data-stu-id="75300-189">The following table lists the inventory dimensions that will be the default dimension names in Inventory Visibility.</span></span>

| <span data-ttu-id="75300-190">维度类型</span><span class="sxs-lookup"><span data-stu-id="75300-190">Dimension type</span></span> | <span data-ttu-id="75300-191">维度名称</span><span class="sxs-lookup"><span data-stu-id="75300-191">Dimension name</span></span> |
|---|---|
| <span data-ttu-id="75300-192">产品</span><span class="sxs-lookup"><span data-stu-id="75300-192">Product</span></span> | `ColorId` |
| <span data-ttu-id="75300-193">产品</span><span class="sxs-lookup"><span data-stu-id="75300-193">Product</span></span> | `SizeId` |
| <span data-ttu-id="75300-194">产品</span><span class="sxs-lookup"><span data-stu-id="75300-194">Product</span></span> | `StyleId` |
| <span data-ttu-id="75300-195">产品</span><span class="sxs-lookup"><span data-stu-id="75300-195">Product</span></span> | `ConfigId` |
| <span data-ttu-id="75300-196">跟踪</span><span class="sxs-lookup"><span data-stu-id="75300-196">Tracking</span></span> | `BatchId` |
| <span data-ttu-id="75300-197">跟踪</span><span class="sxs-lookup"><span data-stu-id="75300-197">Tracking</span></span> | `SerialId` |
| <span data-ttu-id="75300-198">库位</span><span class="sxs-lookup"><span data-stu-id="75300-198">Location</span></span> | `LocationId` |
| <span data-ttu-id="75300-199">库位</span><span class="sxs-lookup"><span data-stu-id="75300-199">Location</span></span> | `SiteId` |
| <span data-ttu-id="75300-200">库存状态</span><span class="sxs-lookup"><span data-stu-id="75300-200">Inventory Status</span></span> | `StatusId` |
| <span data-ttu-id="75300-201">仓库特定</span><span class="sxs-lookup"><span data-stu-id="75300-201">Warehouse Specific</span></span> | `WMSLocationId` |
| <span data-ttu-id="75300-202">仓库特定</span><span class="sxs-lookup"><span data-stu-id="75300-202">Warehouse Specific</span></span> | `WMSPalletId` |
| <span data-ttu-id="75300-203">仓库特定</span><span class="sxs-lookup"><span data-stu-id="75300-203">Warehouse Specific</span></span> | `LicensePlateId` |

> [!NOTE]
> <span data-ttu-id="75300-204">上表中列出的维度类型仅供参考。</span><span class="sxs-lookup"><span data-stu-id="75300-204">The dimension type listed in the previous table is for reference only.</span></span> <span data-ttu-id="75300-205">您无需在库存可见性中定义维度类型。</span><span class="sxs-lookup"><span data-stu-id="75300-205">You don't need to define the dimension type in Inventory Visibility.</span></span>

<span data-ttu-id="75300-206">如果自定义维度已存在，并且在由库存可见性使用时需要流入默认值，可以在库存可见性中配置 **自定义维度** 名称。</span><span class="sxs-lookup"><span data-stu-id="75300-206">If a custom dimension exists and needs to flow to a default value when consumed by Inventory Visibility, you can configure the **Custom dimension** name in Inventory Visibility.</span></span>

<span data-ttu-id="75300-207">外部系统通过 RESTful API 访问库存可见性，这些 API 可以查询给定维度集上的现有信息。</span><span class="sxs-lookup"><span data-stu-id="75300-207">External systems access Inventory Visibility through RESTful APIs that enable on-hand information on given sets of dimensions to be queried.</span></span> <span data-ttu-id="75300-208">对于集成，库存可见性使您能够在库存可见性中将 *外部通道数据源* 以及来源维度配置为 *目标维度*。</span><span class="sxs-lookup"><span data-stu-id="75300-208">For the integration, Inventory Visibility enables you to configure the *external channel data source* and the source dimension to the *target dimensions* in Inventory Visibility.</span></span>

<span data-ttu-id="75300-209">目标维度应为以下维度之一：</span><span class="sxs-lookup"><span data-stu-id="75300-209">The target dimensions should be one of the following:</span></span>

- <span data-ttu-id="75300-210">库存可见性中的默认维度</span><span class="sxs-lookup"><span data-stu-id="75300-210">Default dimensions in Inventory Visibility</span></span>
- <span data-ttu-id="75300-211">自定义维度</span><span class="sxs-lookup"><span data-stu-id="75300-211">Custom dimensions</span></span>

<span data-ttu-id="75300-212">维度配置的目的是标准化维度查询和维度发布事件的多系统集成。</span><span class="sxs-lookup"><span data-stu-id="75300-212">The purpose of dimension configuration is to standardize the multi-system integration for the query on dimensions and the posting event with dimensions.</span></span>

#### <a name="indexing"></a><span data-ttu-id="75300-213">正在索引</span><span class="sxs-lookup"><span data-stu-id="75300-213">Indexing</span></span>

<span data-ttu-id="75300-214">在大多数情况下，库存现有查询不仅会处于最高的“总计”级别，而且您可能希望查看基于库存维度汇总的结果。</span><span class="sxs-lookup"><span data-stu-id="75300-214">Most of the time, the inventory on-hand query will not only be on the highest "total" level, but you may want to see results aggregated based on the inventory dimensions.</span></span>

<span data-ttu-id="75300-215">库存可视性通过允许您设置基于维度或维度组合的索引来提供灵活性。</span><span class="sxs-lookup"><span data-stu-id="75300-215">Inventory Visibility provides flexibility by allowing you to set up the indexes, which are based on the dimension or the combination of the dimensions.</span></span>

> [!NOTE]
> <span data-ttu-id="75300-216">当前，您最多只能配置五个索引。</span><span class="sxs-lookup"><span data-stu-id="75300-216">Currently, you can only configure indexes to a maximum of five.</span></span> <span data-ttu-id="75300-217">您需要在实施之前仔细考虑将使用哪个维度或维度组合，以确保它可以满足您的业务需求。</span><span class="sxs-lookup"><span data-stu-id="75300-217">You need to carefully consider which dimension or dimension combination you will use before the implementation to ensure that it will meet your business needs.</span></span> <span data-ttu-id="75300-218">例如，如果要查询产品，如下所示：</span><span class="sxs-lookup"><span data-stu-id="75300-218">For example, if you want to query products as follows:</span></span>

- <span data-ttu-id="75300-219">按 *颜色* 和 *尺寸* 维度查询汇总的现有产品。</span><span class="sxs-lookup"><span data-stu-id="75300-219">Query the aggregated product on-hand by the *Color* and *Size* dimensions.</span></span>
- <span data-ttu-id="75300-220">在某些情况下，您只想查询全部产品。</span><span class="sxs-lookup"><span data-stu-id="75300-220">In some cases, you just want to query on the product in total.</span></span>

<span data-ttu-id="75300-221">您将有两个定义如下的索引：</span><span class="sxs-lookup"><span data-stu-id="75300-221">You would have two indexes defined as the following:</span></span>

- `["ColorId", "SizeId"]`
- `[]`

<span data-ttu-id="75300-222">空括号将基于分区内的产品 ID 进行汇总。</span><span class="sxs-lookup"><span data-stu-id="75300-222">The empty bracket will aggregate based on the product ID within the partition.</span></span>

<span data-ttu-id="75300-223">索引定义如何基于 `groupBy` 查询设置对结果进行分组。</span><span class="sxs-lookup"><span data-stu-id="75300-223">The indexing defines how you can group your results based on the `groupBy` query setting.</span></span> <span data-ttu-id="75300-224">在这种情况下，如果您未定义任何 `groupBy` 值，您将按 `productid` 获得总计。</span><span class="sxs-lookup"><span data-stu-id="75300-224">In this case if you don't define any `groupBy` values, you'll get totals by `productid`.</span></span> <span data-ttu-id="75300-225">否则，如果您将 `groupBy` 定义为 `groupBy=ColorId&groupBy=SizeId`，将基于系统中的不同颜色和尺寸组合返回多行。</span><span class="sxs-lookup"><span data-stu-id="75300-225">Otherwise if you define `groupBy` as `groupBy=ColorId&groupBy=SizeId`, you'll get multiple lines returned, based on the different color and size combinations in the system.</span></span>

<span data-ttu-id="75300-226">您可以将查询条件放入请求正文中。</span><span class="sxs-lookup"><span data-stu-id="75300-226">You can put your query criteria in the request body.</span></span>

<span data-ttu-id="75300-227">下面是有关具有颜色和尺寸组合的产品的示例查询。</span><span class="sxs-lookup"><span data-stu-id="75300-227">Here is a sample query on the product with color and size combination.</span></span>

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

#### <a name="custom-measurement"></a><span data-ttu-id="75300-228">自定义度量</span><span class="sxs-lookup"><span data-stu-id="75300-228">Custom measurement</span></span>

<span data-ttu-id="75300-229">默认度量数量将链接到 Supply Chain Management，但是您可能希望拥有由默认度量组合组成的数量。</span><span class="sxs-lookup"><span data-stu-id="75300-229">The default measurement quantities are linked to Supply Chain Management, however you may want to have a quantity that is made up of a combination of the default measurements.</span></span> <span data-ttu-id="75300-230">为此，您可以配置自定义数量，它们将添加到现有查询的输出中。</span><span class="sxs-lookup"><span data-stu-id="75300-230">To do this, you can have a configuration of custom quantities, which will be added to the output of the on-hand queries.</span></span>

<span data-ttu-id="75300-231">该功能仅允许您定义一组要添加的度量，和/或一组要减去的度量，以便形成自定义度量。</span><span class="sxs-lookup"><span data-stu-id="75300-231">The functionality simply allows you to define a set of measures that will be added, and/or a set of measures that will be subtracted, in order to form the custom measurement.</span></span>

<span data-ttu-id="75300-232">例如，在以下查询条件下，您将自定义度量数量配置为由消耗系统消耗的 `MyCustomAvailableforReservation`。</span><span class="sxs-lookup"><span data-stu-id="75300-232">For example, with the following query condition, you will configure the custom measurement quantity as `MyCustomAvailableforReservation` to be consumed by the consumption system.</span></span>

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



| <span data-ttu-id="75300-233">消耗系统</span><span class="sxs-lookup"><span data-stu-id="75300-233">Consumption system</span></span> | <span data-ttu-id="75300-234">计算的度量</span><span class="sxs-lookup"><span data-stu-id="75300-234">Calculated measurers</span></span> | <span data-ttu-id="75300-235">数据源</span><span class="sxs-lookup"><span data-stu-id="75300-235">Data source</span></span> | <span data-ttu-id="75300-236">修饰符</span><span class="sxs-lookup"><span data-stu-id="75300-236">Modifier</span></span> | <span data-ttu-id="75300-237">修饰符计算类型</span><span class="sxs-lookup"><span data-stu-id="75300-237">Modifier calculation type</span></span> |
|---|---|---|---|---|
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `availphysical` | <span data-ttu-id="75300-238">增加额</span><span class="sxs-lookup"><span data-stu-id="75300-238">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedintotal` | <span data-ttu-id="75300-239">增加额</span><span class="sxs-lookup"><span data-stu-id="75300-239">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedreserved` | <span data-ttu-id="75300-240">减</span><span class="sxs-lookup"><span data-stu-id="75300-240">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `inbound` | <span data-ttu-id="75300-241">增加额</span><span class="sxs-lookup"><span data-stu-id="75300-241">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `outbound` | <span data-ttu-id="75300-242">减</span><span class="sxs-lookup"><span data-stu-id="75300-242">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `received` | <span data-ttu-id="75300-243">增加额</span><span class="sxs-lookup"><span data-stu-id="75300-243">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `scheduled` | <span data-ttu-id="75300-244">增加额</span><span class="sxs-lookup"><span data-stu-id="75300-244">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `issued` | <span data-ttu-id="75300-245">减</span><span class="sxs-lookup"><span data-stu-id="75300-245">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `reserved` | <span data-ttu-id="75300-246">减</span><span class="sxs-lookup"><span data-stu-id="75300-246">Subtraction</span></span> |

<span data-ttu-id="75300-247">这样，对自定义度量数量的查询将返回以下输出。</span><span class="sxs-lookup"><span data-stu-id="75300-247">With that, the query on the custom measurement quantity will return the following output.</span></span>

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

<span data-ttu-id="75300-248">`MyCustomAvailableforReservation` 输出基于自定义度量中的计算设置，如下所示：</span><span class="sxs-lookup"><span data-stu-id="75300-248">The `MyCustomAvailableforReservation` output is based on the calculation setting in the custom measurements as:</span></span>  
 <span data-ttu-id="75300-249">*100 + 50 + 80 + 90 + 30 &ndash; 10 &ndash; 20 &ndash; 60 &ndash; 40 = 220*</span><span class="sxs-lookup"><span data-stu-id="75300-249">*100 + 50 + 80 + 90 + 30 &ndash; 10 &ndash; 20 &ndash; 60 &ndash; 40 = 220*</span></span>

### <a name="posting-on-hand-changes"></a><span data-ttu-id="75300-250">发布现有更改</span><span class="sxs-lookup"><span data-stu-id="75300-250">Posting on-hand changes</span></span>

<span data-ttu-id="75300-251">该事件将发布到的确切 URL 将取决于您的地理区域。</span><span class="sxs-lookup"><span data-stu-id="75300-251">The exact URL that the event will be posted to will depend on your geographical region.</span></span> <span data-ttu-id="75300-252">它将采用以下形式：</span><span class="sxs-lookup"><span data-stu-id="75300-252">It will take the form:</span></span>

`https://{serviceURL}/api/environment/{environmentId}/onhand`

<span data-ttu-id="75300-253">经过身份验证后，此 URL 可以与 HTTP `POST` 方法一起使用以将现有更改事件发送到服务。</span><span class="sxs-lookup"><span data-stu-id="75300-253">When authenticated, this URL can be used along with the HTTP `POST` method to send on-hand change events to the service.</span></span>

<span data-ttu-id="75300-254">特殊标题用于通过 HTTP 请求与 Dynamics 365 服务通信，表示数据链接到的 Supply Chain Management 实例的环境 ID。</span><span class="sxs-lookup"><span data-stu-id="75300-254">A special header is used for communicating with Dynamics 365 services through HTTP requests, denoting the environment ID of the Supply Chain Management instance the data is linked to.</span></span> <span data-ttu-id="75300-255">例如:</span><span class="sxs-lookup"><span data-stu-id="75300-255">For example:</span></span>

`x-ms-environment-id: 2db79622-f97a-4d64-9844-d12efed41796`

#### <a name="posting-on-hand-changes-query-example-1"></a><span data-ttu-id="75300-256">发布现有更改查询示例 1</span><span class="sxs-lookup"><span data-stu-id="75300-256">Posting on-hand changes query example 1</span></span>

<span data-ttu-id="75300-257">本示例显示将在 Power Apps 中设置维度配置的场景。</span><span class="sxs-lookup"><span data-stu-id="75300-257">This example shows a scenario where you will set up the dimension configuration in Power Apps.</span></span>

<span data-ttu-id="75300-258">使用以下查询在以 Power Apps 中配置维度映射：</span><span class="sxs-lookup"><span data-stu-id="75300-258">Use the following query to configure the dimension mapping in Power Apps:</span></span>

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

<span data-ttu-id="75300-259">现在，您可以指定 `dimensionDataSource` 并在查询中使用自定义维度。</span><span class="sxs-lookup"><span data-stu-id="75300-259">Now you can specify the `dimensionDataSource` and use custom dimensions in your queries.</span></span> <span data-ttu-id="75300-260">系统会自动将自定义维度转换为基本维度。</span><span class="sxs-lookup"><span data-stu-id="75300-260">The system will automatically convert custom dimensions to base dimensions.</span></span>

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

#### <a name="posting-on-hand-changes-query-example-2"></a><span data-ttu-id="75300-261">发布现有更改查询示例 2</span><span class="sxs-lookup"><span data-stu-id="75300-261">Posting on-hand changes query example 2</span></span>

<span data-ttu-id="75300-262">本示例显示不在 Power Apps 中为维度配置设置映射，因此发布还应该使用基本维度的场景。</span><span class="sxs-lookup"><span data-stu-id="75300-262">This example shows a scenario where no mappings are set up for the dimension configuration in Power Apps, so the posting should also use the base dimensions.</span></span> <span data-ttu-id="75300-263">当 `dimensionDataSource` 字段为 null、空或空白时，所有维度都必须是基本维度。</span><span class="sxs-lookup"><span data-stu-id="75300-263">All dimensions must be base dimensions when the `dimensionDataSource` field is null, empty, or whitespace.</span></span>

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

#### <a name="json-document-field-properties"></a><span data-ttu-id="75300-264">JSON 文档字段属性</span><span class="sxs-lookup"><span data-stu-id="75300-264">JSON document field properties</span></span>

<span data-ttu-id="75300-265">先前提供的 JSON 查询示例中的字段具有下表中列出的属性。</span><span class="sxs-lookup"><span data-stu-id="75300-265">The fields from the JSON query examples provided previously have the properties listed in the following table.</span></span>

| <span data-ttu-id="75300-266">字段 ID</span><span class="sxs-lookup"><span data-stu-id="75300-266">Field ID</span></span> | <span data-ttu-id="75300-267">说明</span><span class="sxs-lookup"><span data-stu-id="75300-267">Description</span></span> |
|---|---|
| `id` | <span data-ttu-id="75300-268">特定更改事件的唯一 ID。</span><span class="sxs-lookup"><span data-stu-id="75300-268">A unique ID for the specific change event.</span></span> <span data-ttu-id="75300-269">此 ID 用于确保如果在发布过程中与服务的通信失败，重新提交事件不会导致同一事件在系统中计入两次。</span><span class="sxs-lookup"><span data-stu-id="75300-269">This ID is used to ensure that if communication with the service fails during posting, resubmitting the event would not result in the same event being counted twice in the system.</span></span> |
| `organizationId` | <span data-ttu-id="75300-270">链接到事件的组织的标识符。</span><span class="sxs-lookup"><span data-stu-id="75300-270">The identifier of the organization linked to the event.</span></span> <span data-ttu-id="75300-271">这将映射到 Supply Chain Management 组织或数据区域 ID。</span><span class="sxs-lookup"><span data-stu-id="75300-271">This maps to Supply Chain Management organizations or data area IDs.</span></span> |
| `productId` | <span data-ttu-id="75300-272">所讨论的订单的标识符。</span><span class="sxs-lookup"><span data-stu-id="75300-272">The identifier of the product in question.</span></span> |
| `quantity` | <span data-ttu-id="75300-273">需要更改现有量所依据的数量。</span><span class="sxs-lookup"><span data-stu-id="75300-273">The quantity by which the on-hand needs to be changed.</span></span> <span data-ttu-id="75300-274">例如，如果将 10 个新的百吉饼添加到货位上，该值将为 10。</span><span class="sxs-lookup"><span data-stu-id="75300-274">If, for instance, 10 new bagels were added to a shelf, this value would be 10.</span></span> <span data-ttu-id="75300-275">然后，如果将 3 个百吉饼从货位中下架或出售，则该值将为 -3。</span><span class="sxs-lookup"><span data-stu-id="75300-275">If 3 bagels were then removed from the shelf or sold, this value would be -3.</span></span> |
| `dimensionDataSource` | <span data-ttu-id="75300-276">在发布更改事件和查询中使用的维度的数据源。</span><span class="sxs-lookup"><span data-stu-id="75300-276">The data source of the dimensions used in the posting change event and query.</span></span> <span data-ttu-id="75300-277">如果指定数据源，您可以使用来自指定数据源的自定义维度。</span><span class="sxs-lookup"><span data-stu-id="75300-277">If you specify the data source, you can use the custom dimensions from the specified data source.</span></span> <span data-ttu-id="75300-278">使用维度配置，库存可见性可以将自定义维度映射到常规默认维度。</span><span class="sxs-lookup"><span data-stu-id="75300-278">With the dimension configuration, Inventory Visibility can map the custom dimensions to the general default dimensions.</span></span> <span data-ttu-id="75300-279">如果未指定 `dimensionDataSource`，只能在查询中使用常规默认维度。</span><span class="sxs-lookup"><span data-stu-id="75300-279">If the `dimensionDataSource` is not specified, you can only use the general default dimensions in your queries.</span></span>   |
| `dimensions` | <span data-ttu-id="75300-280">键/值对的动态包。</span><span class="sxs-lookup"><span data-stu-id="75300-280">A dynamic bag of key/value pairs.</span></span> <span data-ttu-id="75300-281">这些将映射到 Supply Chain Management 中的某些维度，但是您也可以添加自定义维度（例如 *源*），这可以表示事件是来自 Supply Chain Management 还是外部系统。</span><span class="sxs-lookup"><span data-stu-id="75300-281">These will map to some of the dimensions in Supply Chain Management, but you could also add custom dimensions (like *Source*) that may denote if the event was coming from Supply Chain Management or an external system.</span></span> |

### <a name="querying-current-on-hand"></a><span data-ttu-id="75300-282">查询当前现有量</span><span class="sxs-lookup"><span data-stu-id="75300-282">Querying current on-hand</span></span>

<span data-ttu-id="75300-283">用于查询当前现有量的终结点将具有类似的 URL：</span><span class="sxs-lookup"><span data-stu-id="75300-283">The endpoint for querying the current on-hand will have a similar URL:</span></span>

`https://{serviceURL}/api/environment/{environmentId}/onhand/indexquery`

<span data-ttu-id="75300-284">将使用 HTTP `POST` 方法查询它。</span><span class="sxs-lookup"><span data-stu-id="75300-284">It will be queried with the HTTP `POST` method.</span></span>

#### <a name="current-on-hand-query-example-1"></a><span data-ttu-id="75300-285">当前现有查询示例 1</span><span class="sxs-lookup"><span data-stu-id="75300-285">Current on-hand query example 1</span></span>

<span data-ttu-id="75300-286">本示例显示已在 Power Apps 中完成维度配置的场景。</span><span class="sxs-lookup"><span data-stu-id="75300-286">This example shows a scenario where you have already completed the dimension configuration in Power Apps.</span></span>

<span data-ttu-id="75300-287">使用以下查询在以 Power Apps 中配置维度映射：</span><span class="sxs-lookup"><span data-stu-id="75300-287">Use the following query to configure the dimension mapping in Power Apps:</span></span>

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

<span data-ttu-id="75300-288">现在，您可以指定 `dimensionDataSource` 并在查询中使用自定义维度。</span><span class="sxs-lookup"><span data-stu-id="75300-288">Now you can specify the `dimensionDataSource` and use custom dimensions in your queries.</span></span> <span data-ttu-id="75300-289">系统会自动将自定义维度转换为基本维度。</span><span class="sxs-lookup"><span data-stu-id="75300-289">The system will automatically convert custom dimensions to base dimensions.</span></span> <span data-ttu-id="75300-290">您可以在 `filters` 中指定 `DimensionDataSource`，并在 `filters` 和 `groupByValues` 中指定自定义维度。</span><span class="sxs-lookup"><span data-stu-id="75300-290">You can specify the `DimensionDataSource` in `filters` and specify custom dimensions in both `filters` and `groupByValues`.</span></span> <span data-ttu-id="75300-291">系统会自动将自定义维度转换为基本维度。</span><span class="sxs-lookup"><span data-stu-id="75300-291">The system will automatically convert custom dimensions to base dimensions.</span></span>

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

#### <a name="current-on-hand-query-example-2"></a><span data-ttu-id="75300-292">当前现有查询示例 2</span><span class="sxs-lookup"><span data-stu-id="75300-292">Current on-hand query example 2</span></span>

<span data-ttu-id="75300-293">本示例显示不在 Power Apps 中为维度配置设置映射，因此发布还应该使用基本维度的场景。</span><span class="sxs-lookup"><span data-stu-id="75300-293">This example shows a scenario where no mappings are set up for the dimension configuration in Power Apps, so the posting should also use the base dimensions.</span></span> <span data-ttu-id="75300-294">当在 `filters` 下 `dimensionDataSource` 字段为 null、空或空白时，所有维度都必须是基本维度。</span><span class="sxs-lookup"><span data-stu-id="75300-294">All dimensions must be base dimensions when the `dimensionDataSource` field, under `filters` is null, empty, or whitespace.</span></span>

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

#### <a name="example-return-result"></a><span data-ttu-id="75300-295">返回结果示例</span><span class="sxs-lookup"><span data-stu-id="75300-295">Example return result</span></span>

<span data-ttu-id="75300-296">前面示例中显示的查询可能返回如下结果。</span><span class="sxs-lookup"><span data-stu-id="75300-296">The queries shown in the previous examples could return a result like this.</span></span>

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

<span data-ttu-id="75300-297">请注意，数量字段将构造为度量及其相关值的字典。</span><span class="sxs-lookup"><span data-stu-id="75300-297">Note that the quantities fields are structured as a dictionary of measures and their associated values.</span></span>
