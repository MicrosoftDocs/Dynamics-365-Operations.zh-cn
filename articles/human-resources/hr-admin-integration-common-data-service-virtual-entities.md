---
title: 配置 Common Data Service 虚拟实体
description: 本主题介绍了如何为 Dynamics 365 Human Resources 配置虚拟实体。 生成和更新现有虚拟实体，并分析生成的实体和可用实体。
author: andreabichsel
manager: tfehr
ms.date: 10/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: CDSIntegrationAdministration
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-10-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0d6f79ea569a7a9b0d25e73e8666bf9ba19095d0
ms.sourcegitcommit: a8665c47696028d371cdc4671db1fd8fcf9e1088
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/21/2020
ms.locfileid: "4058146"
---
# <a name="configure-common-data-service-virtual-entities"></a><span data-ttu-id="8e32e-104">配置 Common Data Service 虚拟实体</span><span class="sxs-lookup"><span data-stu-id="8e32e-104">Configure Common Data Service virtual entities</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="8e32e-105">Dynamics 365 Human Resources 是 Common Data Service 中的虚拟数据源。</span><span class="sxs-lookup"><span data-stu-id="8e32e-105">Dynamics 365 Human Resources is a virtual data source in Common Data Service.</span></span> <span data-ttu-id="8e32e-106">它提供 Common Data Service 和 Microsoft Power Platform 中的完全创建、读取、更新和删除 (CRUD) 操作。</span><span class="sxs-lookup"><span data-stu-id="8e32e-106">It provides full create, read, update, and delete (CRUD) operations from Common Data Service and Microsoft Power Platform.</span></span> <span data-ttu-id="8e32e-107">虚拟实体的数据未存储在 Common Data Service 中，但存储在应用程序数据库中。</span><span class="sxs-lookup"><span data-stu-id="8e32e-107">The data for virtual entities isn't stored in Common Data Service, but in the application database.</span></span> 

<span data-ttu-id="8e32e-108">若要从 Common Data Service 中对 Human Resources 实体启用 CRUD 操作，您必须将这些实体用作 Common Data Service 中的虚拟实体。</span><span class="sxs-lookup"><span data-stu-id="8e32e-108">To enable CRUD operations on Human Resources entities from Common Data Service, you must make the entities available as virtual entities in Common Data Service.</span></span> <span data-ttu-id="8e32e-109">这使您可以从 Common Data Service 和 Microsoft Power Platform 中对 Human Resources 中的数据执行 CRUD 操作。</span><span class="sxs-lookup"><span data-stu-id="8e32e-109">This lets you perform CRUD operations from Common Data Service and Microsoft Power Platform on data that's in Human Resources.</span></span> <span data-ttu-id="8e32e-110">这些操作还支持对 Human Resources 进行完整业务逻辑验证，以确保将数据写入实体时的数据完整性。</span><span class="sxs-lookup"><span data-stu-id="8e32e-110">The operations also support the full business logic validations of Human Resources to ensure data integrity when writing data to the entities.</span></span>

## <a name="available-virtual-entities-for-human-resources"></a><span data-ttu-id="8e32e-111">Human Resources 的可用虚拟实体</span><span class="sxs-lookup"><span data-stu-id="8e32e-111">Available virtual entities for Human Resources</span></span>

<span data-ttu-id="8e32e-112">Human Resources 中的所有 Open Data Protocol (OData) 实体都可用作 Common Data Service 中的虚拟实体。</span><span class="sxs-lookup"><span data-stu-id="8e32e-112">All Open Data Protocol (OData) entities in Human Resources are available as virtual entities in Common Data Service.</span></span> <span data-ttu-id="8e32e-113">它们在 Power Platform 中也可用。</span><span class="sxs-lookup"><span data-stu-id="8e32e-113">They're also available in Power Platform.</span></span> <span data-ttu-id="8e32e-114">您现在可以直接使用具有完全 CRUD 功能的 Human Resources 中的数据构建应用和体验，而无需将数据复制或同步到 Common Data Service。</span><span class="sxs-lookup"><span data-stu-id="8e32e-114">You can now build apps and experiences with data directly from Human Resources with full CRUD capability, without copying or synchronizing data to Common Data Service.</span></span> <span data-ttu-id="8e32e-115">您可以使用 Power Apps 门户来构建面向外部的网站，以为 Human Resources 中的业务流程启用协作方案。</span><span class="sxs-lookup"><span data-stu-id="8e32e-115">You can use Power Apps portals to build external-facing websites that enable collaboration scenarios for business processes in Human Resources.</span></span>

<span data-ttu-id="8e32e-116">您可以查看在环境中启用的虚拟实体列表，然后开始使用 **Dynamics 365 HR 虚拟实体** 解决方案的 [Power Apps](https://make.powerapps.com) 中的实体。</span><span class="sxs-lookup"><span data-stu-id="8e32e-116">You can view the list of virtual entities enabled in the environment, and begin working with the entities in [Power Apps](https://make.powerapps.com), in the **Dynamics 365 HR Virtual Entities** solution.</span></span>

![Power Apps 中的 Dynamics 365 HR 虚拟实体](./media/hr-admin-integration-virtual-entities-power-apps.jpg)

## <a name="virtual-entities-versus-natural-entities"></a><span data-ttu-id="8e32e-118">虚拟实体与自然实体</span><span class="sxs-lookup"><span data-stu-id="8e32e-118">Virtual entities versus natural entities</span></span>

<span data-ttu-id="8e32e-119">Human Resources 的虚拟实体与为 Human Resources 创建的 Common Data Service 自然实体不同。</span><span class="sxs-lookup"><span data-stu-id="8e32e-119">Virtual entities for Human Resources aren't the same as the natural Common Data Service entities created for Human Resources.</span></span> <span data-ttu-id="8e32e-120">Human Resources 的自然实体单独生成，并在 Common Data Service 的 HCM 通用解决方案中维护。</span><span class="sxs-lookup"><span data-stu-id="8e32e-120">The natural entities for Human Resources are generated separately and maintained in the HCM Common solution in Common Data Service.</span></span> <span data-ttu-id="8e32e-121">对于自然实体，数据存储在 Common Data Service 中并且需要与 Human Resources 应用程序数据库同步。</span><span class="sxs-lookup"><span data-stu-id="8e32e-121">With natural entities, the data is stored in Common Data Service and requires synchronization with the Human Resources application database.</span></span>

> [!NOTE]
> <span data-ttu-id="8e32e-122">有关 Human Resources 的 Common Data Service 自然实体列表，请参阅 [Common Data Service 实体](https://docs.microsoft.com/dynamics365/human-resources/hr-developer-entities)。</span><span class="sxs-lookup"><span data-stu-id="8e32e-122">For a list of the natural Common Data Service entities for Human Resources, see [Common Data Service entities](https://docs.microsoft.com/dynamics365/human-resources/hr-developer-entities).</span></span>

## <a name="setup"></a><span data-ttu-id="8e32e-123">设置</span><span class="sxs-lookup"><span data-stu-id="8e32e-123">Setup</span></span>

<span data-ttu-id="8e32e-124">请按照以下设置步骤在您的环境中启用虚拟实体。</span><span class="sxs-lookup"><span data-stu-id="8e32e-124">Follow these setup steps to enable virtual entities in your environment.</span></span> 

### <a name="register-the-app-in-microsoft-azure"></a><span data-ttu-id="8e32e-125">在 Microsoft Azure 中注册应用</span><span class="sxs-lookup"><span data-stu-id="8e32e-125">Register the app in Microsoft Azure</span></span>

<span data-ttu-id="8e32e-126">首先，您需要在 Azure 门户中注册应用，以便 Microsoft 标识平台可以为应用和用户提供身份验证和授权服务。</span><span class="sxs-lookup"><span data-stu-id="8e32e-126">First, you need to register the app in the Azure portal so the Microsoft identity platform can provide authentication and authorization services for the app and users.</span></span> <span data-ttu-id="8e32e-127">有关在 Azure 中注册应用的详细信息，请参阅[快速入门：向 Microsoft 标识平台注册应用程序](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app)。</span><span class="sxs-lookup"><span data-stu-id="8e32e-127">For more information about registering apps in Azure, see [Quickstart: Register an application with the Microsoft identity platform](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app).</span></span>

1. <span data-ttu-id="8e32e-128">打开 [Microsoft Azure 门户](https://portal.azure.com)。</span><span class="sxs-lookup"><span data-stu-id="8e32e-128">Open the [Microsoft Azure portal](https://portal.azure.com).</span></span>

2. <span data-ttu-id="8e32e-129">在 Azure 服务中，选择 **应用注册** 。</span><span class="sxs-lookup"><span data-stu-id="8e32e-129">In the Azure services list, select **App registrations**.</span></span>

3. <span data-ttu-id="8e32e-130">选择 **新注册** 。</span><span class="sxs-lookup"><span data-stu-id="8e32e-130">Select **New registration**.</span></span>

4. <span data-ttu-id="8e32e-131">在 **名称** 字段中，输入应用的描述性名称。</span><span class="sxs-lookup"><span data-stu-id="8e32e-131">In the **Name** field, enter a descriptive name for the app.</span></span> <span data-ttu-id="8e32e-132">例如， **Dynamics 365 Human Resources 虚拟实体** 。</span><span class="sxs-lookup"><span data-stu-id="8e32e-132">For example, **Dynamics 365 Human Resources Virtual Entities**.</span></span>

5. <span data-ttu-id="8e32e-133">在 **重定向 URI** 字段中，输入 Human Resources 实例的命名空间 URL。</span><span class="sxs-lookup"><span data-stu-id="8e32e-133">In the **Redirect URI** field, enter the namespace URL of your instance of Human Resources.</span></span>

6. <span data-ttu-id="8e32e-134">选择 **注册** 。</span><span class="sxs-lookup"><span data-stu-id="8e32e-134">Select **Register**.</span></span>

7. <span data-ttu-id="8e32e-135">注册完成后，Azure 门户显示应用注册的 **概述** 窗格，其中包括其 **应用程序（客户端）ID** 。</span><span class="sxs-lookup"><span data-stu-id="8e32e-135">When registration completes, the Azure portal displays the app registration's **Overview** pane, which includes its **Application (client) ID**.</span></span> <span data-ttu-id="8e32e-136">此时，请记下 **应用程序（客户端）ID** 。</span><span class="sxs-lookup"><span data-stu-id="8e32e-136">Take note of the **Application (client) ID** at this time.</span></span> <span data-ttu-id="8e32e-137">您将在[配置虚拟实体数据源](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source)时输入此信息。</span><span class="sxs-lookup"><span data-stu-id="8e32e-137">You'll enter this information when you [Configure the virtual entity data source](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source).</span></span>

8. <span data-ttu-id="8e32e-138">在左侧导航窗格中，选择 **证书和密码** 。</span><span class="sxs-lookup"><span data-stu-id="8e32e-138">In the left navigation pane, select **Certificates and secrets**.</span></span>

9. <span data-ttu-id="8e32e-139">在页面的 **客户端密码** 部分中，选择 **新客户端密码** 。</span><span class="sxs-lookup"><span data-stu-id="8e32e-139">In the **Client secrets** section of the page, select **New client secret**.</span></span>

10. <span data-ttu-id="8e32e-140">提供描述，选择持续时间，然后选择 **添加** 。</span><span class="sxs-lookup"><span data-stu-id="8e32e-140">Provide a description, select a duration, and select **Add**.</span></span>

11. <span data-ttu-id="8e32e-141">记录密码的值。</span><span class="sxs-lookup"><span data-stu-id="8e32e-141">Record the secret's value.</span></span> <span data-ttu-id="8e32e-142">您将在[配置虚拟实体数据源](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source)时输入此信息。</span><span class="sxs-lookup"><span data-stu-id="8e32e-142">You'll enter this information when you [Configure the virtual entity data source](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source).</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="8e32e-143">请确保此时记下密码的值。</span><span class="sxs-lookup"><span data-stu-id="8e32e-143">Be sure to take note of the secret's value at this time.</span></span> <span data-ttu-id="8e32e-144">离开此页面后，密码将不再显示。</span><span class="sxs-lookup"><span data-stu-id="8e32e-144">The secret is never displayed again after you leave this page.</span></span>

### <a name="install-the-dynamics-365-hr-virtual-entity-app"></a><span data-ttu-id="8e32e-145">安装 Dynamics 365 HR Virtual Entity 应用</span><span class="sxs-lookup"><span data-stu-id="8e32e-145">Install the Dynamics 365 HR Virtual Entity app</span></span>

<span data-ttu-id="8e32e-146">在您的 Power Apps 环境中安装 Dynamics 365 HR Virtual Entity 应用以将虚拟实体解决方案包部署到 Common Data Service。</span><span class="sxs-lookup"><span data-stu-id="8e32e-146">Install the Dynamics 365 HR Virtual Entity app in your Power Apps environment to deploy the virtual entity solution package to Common Data Service.</span></span>

1. <span data-ttu-id="8e32e-147">打开 [Power Platform 管理中心](https://admin.powerplatform.microsoft.com)。</span><span class="sxs-lookup"><span data-stu-id="8e32e-147">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="8e32e-148">在 **环境** 列表中，选择与您的 Human Resources 实例关联的 Power Apps 环境。</span><span class="sxs-lookup"><span data-stu-id="8e32e-148">In the **Environments** list, select the Power Apps environment associated with your Human Resources instance.</span></span>

3. <span data-ttu-id="8e32e-149">在页面的 **资源** 部分中，选择 **Dynamics 365 应用** 。</span><span class="sxs-lookup"><span data-stu-id="8e32e-149">In the **Resources** section of the page, select **Dynamics 365 apps**.</span></span>

4. <span data-ttu-id="8e32e-150">选择 **安装应用** 操作。</span><span class="sxs-lookup"><span data-stu-id="8e32e-150">Select the **Install app** action.</span></span>

5. <span data-ttu-id="8e32e-151">选择 **Dynamics 365 HR Virtual Entity** ，然后选择 **下一步** 。</span><span class="sxs-lookup"><span data-stu-id="8e32e-151">Select **Dynamics 365 HR Virtual Entity** , and select **Next**.</span></span>

6. <span data-ttu-id="8e32e-152">审查并标记以同意服务条款。</span><span class="sxs-lookup"><span data-stu-id="8e32e-152">Review and mark to agree to the terms of service.</span></span>

7. <span data-ttu-id="8e32e-153">选择 **安装** 。</span><span class="sxs-lookup"><span data-stu-id="8e32e-153">Select **Install**.</span></span>

<span data-ttu-id="8e32e-154">安装需要几分钟时间。</span><span class="sxs-lookup"><span data-stu-id="8e32e-154">The install takes a few minutes.</span></span> <span data-ttu-id="8e32e-155">完成后，请继续执行后续步骤。</span><span class="sxs-lookup"><span data-stu-id="8e32e-155">When it completes, continue to the next steps.</span></span>

![从 Power Platform 管理中心安装 Dynamics 365 HR Virtual Entity 应用](./media/hr-admin-integration-virtual-entities-power-platform-install.jpg)

### <a name="configure-the-virtual-entity-data-source"></a><span data-ttu-id="8e32e-157">配置虚拟实体数据源</span><span class="sxs-lookup"><span data-stu-id="8e32e-157">Configure the virtual entity data source</span></span> 

<span data-ttu-id="8e32e-158">下一步是在 Power Apps 环境中配置虚拟实体数据源。</span><span class="sxs-lookup"><span data-stu-id="8e32e-158">The next step is to configure the virtual entity data source in the Power Apps environment.</span></span> 

1. <span data-ttu-id="8e32e-159">打开 [Power Platform 管理中心](https://admin.powerplatform.microsoft.com)。</span><span class="sxs-lookup"><span data-stu-id="8e32e-159">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="8e32e-160">在 **环境** 列表中，选择与您的 Human Resources 实例关联的 Power Apps 环境。</span><span class="sxs-lookup"><span data-stu-id="8e32e-160">In the **Environments** list, select the Power Apps environment associated with your Human Resources instance.</span></span>

3. <span data-ttu-id="8e32e-161">在页面的 **详细信息** 部分中选择 **环境 URL** 。</span><span class="sxs-lookup"><span data-stu-id="8e32e-161">Select the **Environment URL** in the **Details** section of the page.</span></span>

4. <span data-ttu-id="8e32e-162">在 **解决方案运行状况中心** 中，选择应用程序页面右上角的 **高级查找** 图标。</span><span class="sxs-lookup"><span data-stu-id="8e32e-162">In the **Solution Health Hub** , select the **Advanced Find** icon in the top right of the application page.</span></span>

5. <span data-ttu-id="8e32e-163">在 **高级查找** 页面上的 **查找** 下拉列表中，选择 **Finance and Operations 虚拟数据源配置** 。</span><span class="sxs-lookup"><span data-stu-id="8e32e-163">On the **Advanced Find** page, in the **Look for** dropdown list, select **Finance and Operations Virtual Data Source Configurations**.</span></span>

6. <span data-ttu-id="8e32e-164">选择 **结果** 。</span><span class="sxs-lookup"><span data-stu-id="8e32e-164">Select **Results**.</span></span>

7. <span data-ttu-id="8e32e-165">选择 **Microsoft HR 数据源** 记录。</span><span class="sxs-lookup"><span data-stu-id="8e32e-165">Select the **Microsoft HR Data Source** record.</span></span>

8. <span data-ttu-id="8e32e-166">输入数据源配置所需的信息。</span><span class="sxs-lookup"><span data-stu-id="8e32e-166">Enter the required information for the data source configuration.</span></span>

   - <span data-ttu-id="8e32e-167">**目标 URL** ：Human Resources 命名空间的 URL。</span><span class="sxs-lookup"><span data-stu-id="8e32e-167">**Target URL** : The URL of your Human Resources namespace.</span></span>
   - <span data-ttu-id="8e32e-168">**租户 ID** ：Azure Active Directory (Azure AD) 租户 ID。</span><span class="sxs-lookup"><span data-stu-id="8e32e-168">**Tenant ID** : The Azure Active Directory (Azure AD) tenant ID.</span></span>
   - <span data-ttu-id="8e32e-169">**AAD 应用程序 ID** ：为在 Microsoft Azure 门户中注册的应用程序创建的应用程序（客户端）ID。</span><span class="sxs-lookup"><span data-stu-id="8e32e-169">**AAD Application ID** : The application (client) ID created for the application registered in the Microsoft Azure portal.</span></span> <span data-ttu-id="8e32e-170">您在步骤[在 Microsoft Azure 中注册应用](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure)的早期阶段就收到了此信息。</span><span class="sxs-lookup"><span data-stu-id="8e32e-170">You received this information earlier during the step [Register the app in Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span></span>
   - <span data-ttu-id="8e32e-171">**AAD 应用程序密码** ：为在 Microsoft Azure 门户中注册的应用程序创建的客户端密码。</span><span class="sxs-lookup"><span data-stu-id="8e32e-171">**AAD Application Secret** : The client secret created for the application registered in the Microsoft Azure portal.</span></span> <span data-ttu-id="8e32e-172">您在步骤[在 Microsoft Azure 中注册应用](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure)的早期阶段就收到了此信息。</span><span class="sxs-lookup"><span data-stu-id="8e32e-172">You received this information earlier during the step [Register the app in Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span></span>

9. <span data-ttu-id="8e32e-173">选择 **保存并关闭** 。</span><span class="sxs-lookup"><span data-stu-id="8e32e-173">Select **Save & Close**.</span></span>

   ![Microsoft HR 数据源](./media/hr-admin-integration-virtual-entities-hr-data-source.jpg)

### <a name="grant-app-permissions-in-human-resources"></a><span data-ttu-id="8e32e-175">在 Human Resources 中授予应用权限</span><span class="sxs-lookup"><span data-stu-id="8e32e-175">Grant app permissions in Human Resources</span></span>

<span data-ttu-id="8e32e-176">在 Human Resources 中为两个 Azure AD 应用程序授予权限：</span><span class="sxs-lookup"><span data-stu-id="8e32e-176">Grant permissions for the two Azure AD applications in Human Resources:</span></span>

- <span data-ttu-id="8e32e-177">在 Microsoft Azure 门户中为您的租户创建的应用</span><span class="sxs-lookup"><span data-stu-id="8e32e-177">The app created for your tenant in the Microsoft Azure portal</span></span>
- <span data-ttu-id="8e32e-178">在 Power Apps 环境中安装的 Dynamics 365 HR Virtual Entity 应用</span><span class="sxs-lookup"><span data-stu-id="8e32e-178">The Dynamics 365 HR Virtual Entity app installed in the Power Apps environment</span></span> 

1. <span data-ttu-id="8e32e-179">在 Human Resources 中，打开 **Azure Active Directory 应用程序** 页面。</span><span class="sxs-lookup"><span data-stu-id="8e32e-179">In Human Resources, open the **Azure Active Directory applications** page.</span></span>

2. <span data-ttu-id="8e32e-180">选择 **新建** 以创建新的应用程序记录：</span><span class="sxs-lookup"><span data-stu-id="8e32e-180">Select **New** to create a new application record:</span></span>

    - <span data-ttu-id="8e32e-181">在 **客户端 ID** 字段中，输入您在 Microsoft Azure 门户中注册的应用的客户端 ID。</span><span class="sxs-lookup"><span data-stu-id="8e32e-181">In the **Client ID** field, enter the client ID of the app you registered in the Microsoft Azure portal.</span></span>
    - <span data-ttu-id="8e32e-182">在 **名称** 字段中，输入您在 Microsoft Azure 门户中注册的应用的名称。</span><span class="sxs-lookup"><span data-stu-id="8e32e-182">In the **Name** field, enter the name of the app you registered in the Microsoft Azure portal.</span></span>
    - <span data-ttu-id="8e32e-183">在 **用户 ID** 字段中，在 Human Resources 和 Power Apps 环境中选择具有管理员权限的用户的用户 ID。</span><span class="sxs-lookup"><span data-stu-id="8e32e-183">In the **User ID** field, select the user ID of a user with admin permissions in Human Resources and the Power Apps environment.</span></span>

3. <span data-ttu-id="8e32e-184">选择 **新建** 以创建第二个应用程序记录：</span><span class="sxs-lookup"><span data-stu-id="8e32e-184">Select **New** to create a second application record:</span></span>

    - <span data-ttu-id="8e32e-185">**客户端 ID** ：f9be0c49-aa22-4ec6-911a-c5da515226ff</span><span class="sxs-lookup"><span data-stu-id="8e32e-185">**Client Id** : f9be0c49-aa22-4ec6-911a-c5da515226ff</span></span>
    - <span data-ttu-id="8e32e-186">**名称** ：Dynamics 365 HR Virtual Entity</span><span class="sxs-lookup"><span data-stu-id="8e32e-186">**Name** : Dynamics 365 HR Virtual Entity</span></span>
    - <span data-ttu-id="8e32e-187">在 **用户 ID** 字段中，在 Human Resources 和 Power Apps 环境中选择具有管理员权限的用户的用户 ID。</span><span class="sxs-lookup"><span data-stu-id="8e32e-187">In the **User ID** field, select the user ID of a user with admin permissions in Human Resources and the Power Apps environment.</span></span>

## <a name="generate-virtual-entities"></a><span data-ttu-id="8e32e-188">生成虚拟实体</span><span class="sxs-lookup"><span data-stu-id="8e32e-188">Generate virtual entities</span></span>

<span data-ttu-id="8e32e-189">设置完成后，您可以选择要在 Common Data Service 实例中生成和启用的虚拟实体。</span><span class="sxs-lookup"><span data-stu-id="8e32e-189">When setup completes, you can select the virtual entities you want to generate and enable in your Common Data Service instance.</span></span>

1. <span data-ttu-id="8e32e-190">在 Human Resources 中，打开 **Common Data Service (CDS) 集成** 页面。</span><span class="sxs-lookup"><span data-stu-id="8e32e-190">In Human Resources, open the **Common Data Service (CDS) integration** page.</span></span>

2. <span data-ttu-id="8e32e-191">选择 **虚拟实体** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="8e32e-191">Select the **Virtual entities** tab.</span></span>

> [!NOTE]
> <span data-ttu-id="8e32e-192">在完成所有所需的设置后， **启用虚拟实体** 切换将自动设置为 **是** 。</span><span class="sxs-lookup"><span data-stu-id="8e32e-192">The **Enable the virtual entity** toggle will be set to **Yes** automatically when all required setup has been completed.</span></span> <span data-ttu-id="8e32e-193">如果切换设置为 **否** ，请查看本文档前面部分中的步骤，以确保完成所有先决条件设置。</span><span class="sxs-lookup"><span data-stu-id="8e32e-193">If the toggle is set to **No** , review the steps in previous sections of this document to ensure all prerequisite setup is completed.</span></span>

3. <span data-ttu-id="8e32e-194">选择要在 Common Data Service 中生成的一个或多个实体。</span><span class="sxs-lookup"><span data-stu-id="8e32e-194">Select the entity or entities you want to generate in Common Data Service.</span></span>

4. <span data-ttu-id="8e32e-195">选择 **生成/刷新** 。</span><span class="sxs-lookup"><span data-stu-id="8e32e-195">Select **Generate/refresh**.</span></span>

![Common Data Service 集成](./media/hr-admin-integration-common-data-service-integration.jpg)

## <a name="check-entity-generation-status"></a><span data-ttu-id="8e32e-197">检查实体生成状态</span><span class="sxs-lookup"><span data-stu-id="8e32e-197">Check entity generation status</span></span>

<span data-ttu-id="8e32e-198">虚拟实体通过异步后台进程在 Common Data Service 中生成。</span><span class="sxs-lookup"><span data-stu-id="8e32e-198">Virtual entities are generated in Common Data Service through an asynchronous background process.</span></span> <span data-ttu-id="8e32e-199">有关进程的更新显示在操作中心中。</span><span class="sxs-lookup"><span data-stu-id="8e32e-199">Updates on the process display in the action center.</span></span> <span data-ttu-id="8e32e-200">有关进程的详细信息（包括错误日志）显示在 **进程自动化** 页面中。</span><span class="sxs-lookup"><span data-stu-id="8e32e-200">Details on the process, including error logs, appear in the **Process automations** page.</span></span>

1. <span data-ttu-id="8e32e-201">在 Human Resources 中，打开 **进程自动化** 页面。</span><span class="sxs-lookup"><span data-stu-id="8e32e-201">In Human Resources, open the **Process automations** page.</span></span>

2. <span data-ttu-id="8e32e-202">选择 **后台进程** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="8e32e-202">Select the **Background processes** tab.</span></span>

3. <span data-ttu-id="8e32e-203">选择 **虚拟实体轮询异步操作后台进程** 。</span><span class="sxs-lookup"><span data-stu-id="8e32e-203">Select **Virtual entity poll async operation background process**.</span></span>

4. <span data-ttu-id="8e32e-204">选择 **查看最新结果** 。</span><span class="sxs-lookup"><span data-stu-id="8e32e-204">Select **View most recent results**.</span></span>

<span data-ttu-id="8e32e-205">滑出窗格将显示该进程的最新执行结果。</span><span class="sxs-lookup"><span data-stu-id="8e32e-205">The slideout pane displays the most recent execution results for the process.</span></span> <span data-ttu-id="8e32e-206">您可以查看进程的日志，包括从 Common Data Service 返回的任何错误。</span><span class="sxs-lookup"><span data-stu-id="8e32e-206">You can view the log for the process, including any errors returned from Common Data Service.</span></span>

## <a name="see-also"></a><span data-ttu-id="8e32e-207">请参阅</span><span class="sxs-lookup"><span data-stu-id="8e32e-207">See also</span></span>

[<span data-ttu-id="8e32e-208">什么是 Common Data Service？</span><span class="sxs-lookup"><span data-stu-id="8e32e-208">What is Common Data Service?</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro)<br>
[<span data-ttu-id="8e32e-209">实体概述</span><span class="sxs-lookup"><span data-stu-id="8e32e-209">Entity overview</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/entity-overview)<br>
[<span data-ttu-id="8e32e-210">实体关系概述</span><span class="sxs-lookup"><span data-stu-id="8e32e-210">Entity relationships overview</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/relationships-overview)<br>
[<span data-ttu-id="8e32e-211">创建和编辑包含来自外部数据源的数据的虚拟实体</span><span class="sxs-lookup"><span data-stu-id="8e32e-211">Create and edit virtual entities that contain data from an external data source</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/create-edit-virtual-entities)<br>
[<span data-ttu-id="8e32e-212">什么是 Power Apps 门户？</span><span class="sxs-lookup"><span data-stu-id="8e32e-212">What is Power Apps portals?</span></span>](https://docs.microsoft.com/powerapps/maker/portals/overview)<br>
[<span data-ttu-id="8e32e-213">在 Power Apps 中创建应用概述</span><span class="sxs-lookup"><span data-stu-id="8e32e-213">Overview of creating apps in Power Apps</span></span>](https://docs.microsoft.com/powerapps/maker/)
