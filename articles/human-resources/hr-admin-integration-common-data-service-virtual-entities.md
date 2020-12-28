---
title: 配置 Common Data Service 虚拟实体
description: 本主题介绍了如何为 Dynamics 365 Human Resources 配置虚拟实体。 生成和更新现有虚拟实体，并分析生成的实体和可用实体。
author: andreabichsel
manager: tfehr
ms.date: 11/02/2020
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
ms.openlocfilehash: 2b590faeab600d04c9d5303693ec1e9ac682250d
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645593"
---
# <a name="configure-common-data-service-virtual-entities"></a><span data-ttu-id="c9342-104">配置 Common Data Service 虚拟实体</span><span class="sxs-lookup"><span data-stu-id="c9342-104">Configure Common Data Service virtual entities</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="c9342-105">Dynamics 365 Human Resources 是 Common Data Service 中的虚拟数据源。</span><span class="sxs-lookup"><span data-stu-id="c9342-105">Dynamics 365 Human Resources is a virtual data source in Common Data Service.</span></span> <span data-ttu-id="c9342-106">它提供 Common Data Service 和 Microsoft Power Platform 中的完全创建、读取、更新和删除 (CRUD) 操作。</span><span class="sxs-lookup"><span data-stu-id="c9342-106">It provides full create, read, update, and delete (CRUD) operations from Common Data Service and Microsoft Power Platform.</span></span> <span data-ttu-id="c9342-107">虚拟实体的数据未存储在 Common Data Service 中，但存储在应用程序数据库中。</span><span class="sxs-lookup"><span data-stu-id="c9342-107">The data for virtual entities isn't stored in Common Data Service, but in the application database.</span></span> 

<span data-ttu-id="c9342-108">若要从 Common Data Service 中对 Human Resources 实体启用 CRUD 操作，您必须将这些实体用作 Common Data Service 中的虚拟实体。</span><span class="sxs-lookup"><span data-stu-id="c9342-108">To enable CRUD operations on Human Resources entities from Common Data Service, you must make the entities available as virtual entities in Common Data Service.</span></span> <span data-ttu-id="c9342-109">这使您可以从 Common Data Service 和 Microsoft Power Platform 中对 Human Resources 中的数据执行 CRUD 操作。</span><span class="sxs-lookup"><span data-stu-id="c9342-109">This lets you perform CRUD operations from Common Data Service and Microsoft Power Platform on data that's in Human Resources.</span></span> <span data-ttu-id="c9342-110">这些操作还支持对 Human Resources 进行完整业务逻辑验证，以确保将数据写入实体时的数据完整性。</span><span class="sxs-lookup"><span data-stu-id="c9342-110">The operations also support the full business logic validations of Human Resources to ensure data integrity when writing data to the entities.</span></span>

## <a name="available-virtual-entities-for-human-resources"></a><span data-ttu-id="c9342-111">Human Resources 的可用虚拟实体</span><span class="sxs-lookup"><span data-stu-id="c9342-111">Available virtual entities for Human Resources</span></span>

<span data-ttu-id="c9342-112">Human Resources 中的所有 Open Data Protocol (OData) 实体都可用作 Common Data Service 中的虚拟实体。</span><span class="sxs-lookup"><span data-stu-id="c9342-112">All Open Data Protocol (OData) entities in Human Resources are available as virtual entities in Common Data Service.</span></span> <span data-ttu-id="c9342-113">它们在 Power Platform 中也可用。</span><span class="sxs-lookup"><span data-stu-id="c9342-113">They're also available in Power Platform.</span></span> <span data-ttu-id="c9342-114">您现在可以直接使用具有完全 CRUD 功能的 Human Resources 中的数据构建应用和体验，而无需将数据复制或同步到 Common Data Service。</span><span class="sxs-lookup"><span data-stu-id="c9342-114">You can now build apps and experiences with data directly from Human Resources with full CRUD capability, without copying or synchronizing data to Common Data Service.</span></span> <span data-ttu-id="c9342-115">您可以使用 Power Apps 门户来构建面向外部的网站，以为 Human Resources 中的业务流程启用协作方案。</span><span class="sxs-lookup"><span data-stu-id="c9342-115">You can use Power Apps portals to build external-facing websites that enable collaboration scenarios for business processes in Human Resources.</span></span>

<span data-ttu-id="c9342-116">您可以查看在环境中启用的虚拟实体列表，然后开始使用 **Dynamics 365 HR 虚拟实体** 解决方案的 [Power Apps](https://make.powerapps.com) 中的实体。</span><span class="sxs-lookup"><span data-stu-id="c9342-116">You can view the list of virtual entities enabled in the environment, and begin working with the entities in [Power Apps](https://make.powerapps.com), in the **Dynamics 365 HR Virtual Entities** solution.</span></span>

![Power Apps 中的 Dynamics 365 HR 虚拟实体](./media/hr-admin-integration-virtual-entities-power-apps.jpg)

## <a name="virtual-entities-versus-natural-entities"></a><span data-ttu-id="c9342-118">虚拟实体与自然实体</span><span class="sxs-lookup"><span data-stu-id="c9342-118">Virtual entities versus natural entities</span></span>

<span data-ttu-id="c9342-119">Human Resources 的虚拟实体与为 Human Resources 创建的 Common Data Service 自然实体不同。</span><span class="sxs-lookup"><span data-stu-id="c9342-119">Virtual entities for Human Resources aren't the same as the natural Common Data Service entities created for Human Resources.</span></span> <span data-ttu-id="c9342-120">Human Resources 的自然实体单独生成，并在 Common Data Service 的 HCM 通用解决方案中维护。</span><span class="sxs-lookup"><span data-stu-id="c9342-120">The natural entities for Human Resources are generated separately and maintained in the HCM Common solution in Common Data Service.</span></span> <span data-ttu-id="c9342-121">对于自然实体，数据存储在 Common Data Service 中并且需要与 Human Resources 应用程序数据库同步。</span><span class="sxs-lookup"><span data-stu-id="c9342-121">With natural entities, the data is stored in Common Data Service and requires synchronization with the Human Resources application database.</span></span>

> [!NOTE]
> <span data-ttu-id="c9342-122">有关 Human Resources 的 Common Data Service 自然实体列表，请参阅 [Common Data Service 实体](https://docs.microsoft.com/dynamics365/human-resources/hr-developer-entities)。</span><span class="sxs-lookup"><span data-stu-id="c9342-122">For a list of the natural Common Data Service entities for Human Resources, see [Common Data Service entities](https://docs.microsoft.com/dynamics365/human-resources/hr-developer-entities).</span></span>

## <a name="setup"></a><span data-ttu-id="c9342-123">设置</span><span class="sxs-lookup"><span data-stu-id="c9342-123">Setup</span></span>

<span data-ttu-id="c9342-124">请按照以下设置步骤在您的环境中启用虚拟实体。</span><span class="sxs-lookup"><span data-stu-id="c9342-124">Follow these setup steps to enable virtual entities in your environment.</span></span>

### <a name="enable-virtual-entities-in-human-resources"></a><span data-ttu-id="c9342-125">在 Human Resources 中启用虚拟实体</span><span class="sxs-lookup"><span data-stu-id="c9342-125">Enable virtual entities in Human Resources</span></span>

<span data-ttu-id="c9342-126">首先，您必须在 **功能管理** 工作区中启用虚拟实体。</span><span class="sxs-lookup"><span data-stu-id="c9342-126">First, you must enable virtual entities in the **Feature management** workspace.</span></span>

1. <span data-ttu-id="c9342-127">在 Human Resources 中，选择 **系统管理**。</span><span class="sxs-lookup"><span data-stu-id="c9342-127">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="c9342-128">选择 **功能管理** 磁贴。</span><span class="sxs-lookup"><span data-stu-id="c9342-128">Select the **Feature management** tile.</span></span>

3. <span data-ttu-id="c9342-129">选择 **HR/CDS 中的虚拟实体支持**，然后选择 **启用**。</span><span class="sxs-lookup"><span data-stu-id="c9342-129">Select **Virtual Entity support in HR/CDS**, and then select **Enable**.</span></span>

<span data-ttu-id="c9342-130">有关启用和禁用功能的详细信息，请参阅[管理功能](hr-admin-manage-features.md)。</span><span class="sxs-lookup"><span data-stu-id="c9342-130">For more information about enabling and disabling features, see [Manage features](hr-admin-manage-features.md).</span></span>

### <a name="register-the-app-in-microsoft-azure"></a><span data-ttu-id="c9342-131">在 Microsoft Azure 中注册应用</span><span class="sxs-lookup"><span data-stu-id="c9342-131">Register the app in Microsoft Azure</span></span>

<span data-ttu-id="c9342-132">您必须在 Azure 门户中注册 Human Resources 实例，以便 Microsoft 标识平台可以为应用和用户提供身份验证和授权服务。</span><span class="sxs-lookup"><span data-stu-id="c9342-132">You must register your Human Resources instance in the Azure portal so the Microsoft identity platform can provide authentication and authorization services for the app and users.</span></span> <span data-ttu-id="c9342-133">有关在 Azure 中注册应用的详细信息，请参阅[快速入门：向 Microsoft 标识平台注册应用程序](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app)。</span><span class="sxs-lookup"><span data-stu-id="c9342-133">For more information about registering apps in Azure, see [Quickstart: Register an application with the Microsoft identity platform](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app).</span></span>

1. <span data-ttu-id="c9342-134">打开 [Microsoft Azure 门户](https://portal.azure.com)。</span><span class="sxs-lookup"><span data-stu-id="c9342-134">Open the [Microsoft Azure portal](https://portal.azure.com).</span></span>

2. <span data-ttu-id="c9342-135">在 Azure 服务中，选择 **应用注册**。</span><span class="sxs-lookup"><span data-stu-id="c9342-135">In the Azure services list, select **App registrations**.</span></span>

3. <span data-ttu-id="c9342-136">选择 **新注册**。</span><span class="sxs-lookup"><span data-stu-id="c9342-136">Select **New registration**.</span></span>

4. <span data-ttu-id="c9342-137">在 **名称** 字段中，输入应用的描述性名称。</span><span class="sxs-lookup"><span data-stu-id="c9342-137">In the **Name** field, enter a descriptive name for the app.</span></span> <span data-ttu-id="c9342-138">例如，**Dynamics 365 Human Resources 虚拟实体**。</span><span class="sxs-lookup"><span data-stu-id="c9342-138">For example, **Dynamics 365 Human Resources Virtual Entities**.</span></span>

5. <span data-ttu-id="c9342-139">在 **重定向 URI** 字段中，输入 Human Resources 实例的命名空间 URL。</span><span class="sxs-lookup"><span data-stu-id="c9342-139">In the **Redirect URI** field, enter the namespace URL of your instance of Human Resources.</span></span>

6. <span data-ttu-id="c9342-140">选择 **注册**。</span><span class="sxs-lookup"><span data-stu-id="c9342-140">Select **Register**.</span></span>

7. <span data-ttu-id="c9342-141">注册完成后，Azure 门户显示应用注册的 **概述** 窗格，其中包括其 **应用程序（客户端）ID**。</span><span class="sxs-lookup"><span data-stu-id="c9342-141">When registration completes, the Azure portal displays the app registration's **Overview** pane, which includes its **Application (client) ID**.</span></span> <span data-ttu-id="c9342-142">此时，请记下 **应用程序（客户端）ID**。</span><span class="sxs-lookup"><span data-stu-id="c9342-142">Take note of the **Application (client) ID** at this time.</span></span> <span data-ttu-id="c9342-143">您将在[配置虚拟实体数据源](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source)时输入此信息。</span><span class="sxs-lookup"><span data-stu-id="c9342-143">You'll enter this information when you [Configure the virtual entity data source](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source).</span></span>

8. <span data-ttu-id="c9342-144">在左侧导航窗格中，选择 **证书和密码**。</span><span class="sxs-lookup"><span data-stu-id="c9342-144">In the left navigation pane, select **Certificates and secrets**.</span></span>

9. <span data-ttu-id="c9342-145">在页面的 **客户端密码** 部分中，选择 **新客户端密码**。</span><span class="sxs-lookup"><span data-stu-id="c9342-145">In the **Client secrets** section of the page, select **New client secret**.</span></span>

10. <span data-ttu-id="c9342-146">提供描述，选择持续时间，然后选择 **添加**。</span><span class="sxs-lookup"><span data-stu-id="c9342-146">Provide a description, select a duration, and select **Add**.</span></span>

11. <span data-ttu-id="c9342-147">记录密码的值。</span><span class="sxs-lookup"><span data-stu-id="c9342-147">Record the secret's value.</span></span> <span data-ttu-id="c9342-148">您将在[配置虚拟实体数据源](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source)时输入此信息。</span><span class="sxs-lookup"><span data-stu-id="c9342-148">You'll enter this information when you [Configure the virtual entity data source](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source).</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="c9342-149">请确保此时记下密码的值。</span><span class="sxs-lookup"><span data-stu-id="c9342-149">Be sure to take note of the secret's value at this time.</span></span> <span data-ttu-id="c9342-150">离开此页面后，密码将不再显示。</span><span class="sxs-lookup"><span data-stu-id="c9342-150">The secret is never displayed again after you leave this page.</span></span>

### <a name="install-the-dynamics-365-hr-virtual-entity-app"></a><span data-ttu-id="c9342-151">安装 Dynamics 365 HR Virtual Entity 应用</span><span class="sxs-lookup"><span data-stu-id="c9342-151">Install the Dynamics 365 HR Virtual Entity app</span></span>

<span data-ttu-id="c9342-152">在您的 Power Apps 环境中安装 Dynamics 365 HR Virtual Entity 应用以将虚拟实体解决方案包部署到 Common Data Service。</span><span class="sxs-lookup"><span data-stu-id="c9342-152">Install the Dynamics 365 HR Virtual Entity app in your Power Apps environment to deploy the virtual entity solution package to Common Data Service.</span></span>

1. <span data-ttu-id="c9342-153">打开 [Power Platform 管理中心](https://admin.powerplatform.microsoft.com)。</span><span class="sxs-lookup"><span data-stu-id="c9342-153">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="c9342-154">在 **环境** 列表中，选择与您的 Human Resources 实例关联的 Power Apps 环境。</span><span class="sxs-lookup"><span data-stu-id="c9342-154">In the **Environments** list, select the Power Apps environment associated with your Human Resources instance.</span></span>

3. <span data-ttu-id="c9342-155">在页面的 **资源** 部分中，选择 **Dynamics 365 应用**。</span><span class="sxs-lookup"><span data-stu-id="c9342-155">In the **Resources** section of the page, select **Dynamics 365 apps**.</span></span>

4. <span data-ttu-id="c9342-156">选择 **安装应用** 操作。</span><span class="sxs-lookup"><span data-stu-id="c9342-156">Select the **Install app** action.</span></span>

5. <span data-ttu-id="c9342-157">选择 **Dynamics 365 HR Virtual Entity**，然后选择 **下一步**。</span><span class="sxs-lookup"><span data-stu-id="c9342-157">Select **Dynamics 365 HR Virtual Entity**, and select **Next**.</span></span>

6. <span data-ttu-id="c9342-158">审查并标记以同意服务条款。</span><span class="sxs-lookup"><span data-stu-id="c9342-158">Review and mark to agree to the terms of service.</span></span>

7. <span data-ttu-id="c9342-159">选择 **安装**。</span><span class="sxs-lookup"><span data-stu-id="c9342-159">Select **Install**.</span></span>

<span data-ttu-id="c9342-160">安装需要几分钟时间。</span><span class="sxs-lookup"><span data-stu-id="c9342-160">The install takes a few minutes.</span></span> <span data-ttu-id="c9342-161">完成后，请继续执行后续步骤。</span><span class="sxs-lookup"><span data-stu-id="c9342-161">When it completes, continue to the next steps.</span></span>

![从 Power Platform 管理中心安装 Dynamics 365 HR Virtual Entity 应用](./media/hr-admin-integration-virtual-entities-power-platform-install.jpg)

### <a name="configure-the-virtual-entity-data-source"></a><span data-ttu-id="c9342-163">配置虚拟实体数据源</span><span class="sxs-lookup"><span data-stu-id="c9342-163">Configure the virtual entity data source</span></span> 

<span data-ttu-id="c9342-164">下一步是在 Power Apps 环境中配置虚拟实体数据源。</span><span class="sxs-lookup"><span data-stu-id="c9342-164">The next step is to configure the virtual entity data source in the Power Apps environment.</span></span> 

1. <span data-ttu-id="c9342-165">打开 [Power Platform 管理中心](https://admin.powerplatform.microsoft.com)。</span><span class="sxs-lookup"><span data-stu-id="c9342-165">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="c9342-166">在 **环境** 列表中，选择与您的 Human Resources 实例关联的 Power Apps 环境。</span><span class="sxs-lookup"><span data-stu-id="c9342-166">In the **Environments** list, select the Power Apps environment associated with your Human Resources instance.</span></span>

3. <span data-ttu-id="c9342-167">在页面的 **详细信息** 部分中选择 **环境 URL**。</span><span class="sxs-lookup"><span data-stu-id="c9342-167">Select the **Environment URL** in the **Details** section of the page.</span></span>

4. <span data-ttu-id="c9342-168">在 **解决方案运行状况中心** 中，选择应用程序页面右上角的 **高级查找** 图标。</span><span class="sxs-lookup"><span data-stu-id="c9342-168">In the **Solution Health Hub**, select the **Advanced Find** icon in the top right of the application page.</span></span>

5. <span data-ttu-id="c9342-169">在 **高级查找** 页面上的 **查找** 下拉列表中，选择 **Finance and Operations 虚拟数据源配置**。</span><span class="sxs-lookup"><span data-stu-id="c9342-169">On the **Advanced Find** page, in the **Look for** dropdown list, select **Finance and Operations Virtual Data Source Configurations**.</span></span>

6. <span data-ttu-id="c9342-170">选择 **结果**。</span><span class="sxs-lookup"><span data-stu-id="c9342-170">Select **Results**.</span></span>

7. <span data-ttu-id="c9342-171">选择 **Microsoft HR 数据源** 记录。</span><span class="sxs-lookup"><span data-stu-id="c9342-171">Select the **Microsoft HR Data Source** record.</span></span>

8. <span data-ttu-id="c9342-172">输入数据源配置所需的信息：</span><span class="sxs-lookup"><span data-stu-id="c9342-172">Enter the required information for the data source configuration:</span></span>

   - <span data-ttu-id="c9342-173">**目标 URL**：Human Resources 命名空间的 URL。</span><span class="sxs-lookup"><span data-stu-id="c9342-173">**Target URL**: The URL of your Human Resources namespace.</span></span> <span data-ttu-id="c9342-174">目标 URL 的格式为：</span><span class="sxs-lookup"><span data-stu-id="c9342-174">The format of the target URL is:</span></span>
     
     <span data-ttu-id="c9342-175">https://\<hostname\>.hr.talent.dynamics.com/namespaces/\<namespaceID\>/</span><span class="sxs-lookup"><span data-stu-id="c9342-175">https://\<hostname\>.hr.talent.dynamics.com/namespaces/\<namespaceID\>/</span></span>

     <span data-ttu-id="c9342-176">例如:</span><span class="sxs-lookup"><span data-stu-id="c9342-176">For example:</span></span>
     
     `https://aos.rts-sf-5ea54e35c68-westus2.hr.talent.dynamics.com/namespaces/49d24c565-8f4d-4891-b174-bf83d948ed0c/`

     >[!NOTE]
     ><span data-ttu-id="c9342-177">确保在 URL 的结尾包括“**/**”字符，以避免收到错误。</span><span class="sxs-lookup"><span data-stu-id="c9342-177">Be sure to include the "**/**" character at the end of the URL to avoid receiving an error.</span></span>

   - <span data-ttu-id="c9342-178">**租户 ID**：Azure Active Directory (Azure AD) 租户 ID。</span><span class="sxs-lookup"><span data-stu-id="c9342-178">**Tenant ID**: The Azure Active Directory (Azure AD) tenant ID.</span></span>

   - <span data-ttu-id="c9342-179">**AAD 应用程序 ID**：为在 Microsoft Azure 门户中注册的应用程序创建的应用程序（客户端）ID。</span><span class="sxs-lookup"><span data-stu-id="c9342-179">**AAD Application ID**: The application (client) ID created for the application registered in the Microsoft Azure portal.</span></span> <span data-ttu-id="c9342-180">您在步骤[在 Microsoft Azure 中注册应用](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure)的早期阶段就收到了此信息。</span><span class="sxs-lookup"><span data-stu-id="c9342-180">You received this information earlier during the step [Register the app in Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span></span>

   - <span data-ttu-id="c9342-181">**AAD 应用程序密码**：为在 Microsoft Azure 门户中注册的应用程序创建的客户端密码。</span><span class="sxs-lookup"><span data-stu-id="c9342-181">**AAD Application Secret**: The client secret created for the application registered in the Microsoft Azure portal.</span></span> <span data-ttu-id="c9342-182">您在步骤[在 Microsoft Azure 中注册应用](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure)的早期阶段就收到了此信息。</span><span class="sxs-lookup"><span data-stu-id="c9342-182">You received this information earlier during the step [Register the app in Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span></span>

   ![Microsoft HR 数据源](./media/hr-admin-integration-virtual-entities-hr-data-source.jpg)

9. <span data-ttu-id="c9342-184">选择 **保存并关闭**。</span><span class="sxs-lookup"><span data-stu-id="c9342-184">Select **Save & Close**.</span></span>

### <a name="grant-app-permissions-in-human-resources"></a><span data-ttu-id="c9342-185">在 Human Resources 中授予应用权限</span><span class="sxs-lookup"><span data-stu-id="c9342-185">Grant app permissions in Human Resources</span></span>

<span data-ttu-id="c9342-186">在 Human Resources 中为两个 Azure AD 应用程序授予权限：</span><span class="sxs-lookup"><span data-stu-id="c9342-186">Grant permissions for the two Azure AD applications in Human Resources:</span></span>

- <span data-ttu-id="c9342-187">在 Microsoft Azure 门户中为您的租户创建的应用</span><span class="sxs-lookup"><span data-stu-id="c9342-187">The app created for your tenant in the Microsoft Azure portal</span></span>
- <span data-ttu-id="c9342-188">在 Power Apps 环境中安装的 Dynamics 365 HR Virtual Entity 应用</span><span class="sxs-lookup"><span data-stu-id="c9342-188">The Dynamics 365 HR Virtual Entity app installed in the Power Apps environment</span></span> 

1. <span data-ttu-id="c9342-189">在 Human Resources 中，打开 **Azure Active Directory 应用程序** 页面。</span><span class="sxs-lookup"><span data-stu-id="c9342-189">In Human Resources, open the **Azure Active Directory applications** page.</span></span>

2. <span data-ttu-id="c9342-190">选择 **新建** 以创建新的应用程序记录：</span><span class="sxs-lookup"><span data-stu-id="c9342-190">Select **New** to create a new application record:</span></span>

    - <span data-ttu-id="c9342-191">在 **客户端 ID** 字段中，输入您在 Microsoft Azure 门户中注册的应用的客户端 ID。</span><span class="sxs-lookup"><span data-stu-id="c9342-191">In the **Client ID** field, enter the client ID of the app you registered in the Microsoft Azure portal.</span></span>
    - <span data-ttu-id="c9342-192">在 **名称** 字段中，输入您在 Microsoft Azure 门户中注册的应用的名称。</span><span class="sxs-lookup"><span data-stu-id="c9342-192">In the **Name** field, enter the name of the app you registered in the Microsoft Azure portal.</span></span>
    - <span data-ttu-id="c9342-193">在 **用户 ID** 字段中，在 Human Resources 和 Power Apps 环境中选择具有管理员权限的用户的用户 ID。</span><span class="sxs-lookup"><span data-stu-id="c9342-193">In the **User ID** field, select the user ID of a user with admin permissions in Human Resources and the Power Apps environment.</span></span>

3. <span data-ttu-id="c9342-194">选择 **新建** 以创建第二个应用程序记录：</span><span class="sxs-lookup"><span data-stu-id="c9342-194">Select **New** to create a second application record:</span></span>

    - <span data-ttu-id="c9342-195">**客户端 ID**：f9be0c49-aa22-4ec6-911a-c5da515226ff</span><span class="sxs-lookup"><span data-stu-id="c9342-195">**Client Id**: f9be0c49-aa22-4ec6-911a-c5da515226ff</span></span>
    - <span data-ttu-id="c9342-196">**名称**：Dynamics 365 HR Virtual Entity</span><span class="sxs-lookup"><span data-stu-id="c9342-196">**Name**: Dynamics 365 HR Virtual Entity</span></span>
    - <span data-ttu-id="c9342-197">在 **用户 ID** 字段中，在 Human Resources 和 Power Apps 环境中选择具有管理员权限的用户的用户 ID。</span><span class="sxs-lookup"><span data-stu-id="c9342-197">In the **User ID** field, select the user ID of a user with admin permissions in Human Resources and the Power Apps environment.</span></span>

## <a name="generate-virtual-entities"></a><span data-ttu-id="c9342-198">生成虚拟实体</span><span class="sxs-lookup"><span data-stu-id="c9342-198">Generate virtual entities</span></span>

<span data-ttu-id="c9342-199">设置完成后，您可以选择要在 Common Data Service 实例中生成和启用的虚拟实体。</span><span class="sxs-lookup"><span data-stu-id="c9342-199">When setup completes, you can select the virtual entities you want to generate and enable in your Common Data Service instance.</span></span>

1. <span data-ttu-id="c9342-200">在 Human Resources 中，打开 **Common Data Service (CDS) 集成** 页面。</span><span class="sxs-lookup"><span data-stu-id="c9342-200">In Human Resources, open the **Common Data Service (CDS) integration** page.</span></span>

2. <span data-ttu-id="c9342-201">选择 **虚拟实体** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="c9342-201">Select the **Virtual entities** tab.</span></span>

> [!NOTE]
> <span data-ttu-id="c9342-202">在完成所有所需的设置后，**启用虚拟实体** 切换将自动设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="c9342-202">The **Enable the virtual entity** toggle will be set to **Yes** automatically when all required setup has been completed.</span></span> <span data-ttu-id="c9342-203">如果切换设置为 **否**，请查看本文档前面部分中的步骤，以确保完成所有先决条件设置。</span><span class="sxs-lookup"><span data-stu-id="c9342-203">If the toggle is set to **No**, review the steps in previous sections of this document to ensure all prerequisite setup is completed.</span></span>

3. <span data-ttu-id="c9342-204">选择要在 Common Data Service 中生成的一个或多个实体。</span><span class="sxs-lookup"><span data-stu-id="c9342-204">Select the entity or entities you want to generate in Common Data Service.</span></span>

4. <span data-ttu-id="c9342-205">选择 **生成/刷新**。</span><span class="sxs-lookup"><span data-stu-id="c9342-205">Select **Generate/refresh**.</span></span>

![Common Data Service 集成](./media/hr-admin-integration-common-data-service-integration.jpg)

## <a name="check-entity-generation-status"></a><span data-ttu-id="c9342-207">检查实体生成状态</span><span class="sxs-lookup"><span data-stu-id="c9342-207">Check entity generation status</span></span>

<span data-ttu-id="c9342-208">虚拟实体通过异步后台进程在 Common Data Service 中生成。</span><span class="sxs-lookup"><span data-stu-id="c9342-208">Virtual entities are generated in Common Data Service through an asynchronous background process.</span></span> <span data-ttu-id="c9342-209">有关进程的更新显示在操作中心中。</span><span class="sxs-lookup"><span data-stu-id="c9342-209">Updates on the process display in the action center.</span></span> <span data-ttu-id="c9342-210">有关进程的详细信息（包括错误日志）显示在 **进程自动化** 页面中。</span><span class="sxs-lookup"><span data-stu-id="c9342-210">Details on the process, including error logs, appear in the **Process automations** page.</span></span>

1. <span data-ttu-id="c9342-211">在 Human Resources 中，打开 **进程自动化** 页面。</span><span class="sxs-lookup"><span data-stu-id="c9342-211">In Human Resources, open the **Process automations** page.</span></span>

2. <span data-ttu-id="c9342-212">选择 **后台进程** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="c9342-212">Select the **Background processes** tab.</span></span>

3. <span data-ttu-id="c9342-213">选择 **虚拟实体轮询异步操作后台进程**。</span><span class="sxs-lookup"><span data-stu-id="c9342-213">Select **Virtual entity poll async operation background process**.</span></span>

4. <span data-ttu-id="c9342-214">选择 **查看最新结果**。</span><span class="sxs-lookup"><span data-stu-id="c9342-214">Select **View most recent results**.</span></span>

<span data-ttu-id="c9342-215">滑出窗格将显示该进程的最新执行结果。</span><span class="sxs-lookup"><span data-stu-id="c9342-215">The slideout pane displays the most recent execution results for the process.</span></span> <span data-ttu-id="c9342-216">您可以查看进程的日志，包括从 Common Data Service 返回的任何错误。</span><span class="sxs-lookup"><span data-stu-id="c9342-216">You can view the log for the process, including any errors returned from Common Data Service.</span></span>

## <a name="see-also"></a><span data-ttu-id="c9342-217">请参阅</span><span class="sxs-lookup"><span data-stu-id="c9342-217">See also</span></span>

[<span data-ttu-id="c9342-218">什么是 Common Data Service？</span><span class="sxs-lookup"><span data-stu-id="c9342-218">What is Common Data Service?</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro)<br>
[<span data-ttu-id="c9342-219">实体概述</span><span class="sxs-lookup"><span data-stu-id="c9342-219">Entity overview</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/entity-overview)<br>
[<span data-ttu-id="c9342-220">实体关系概述</span><span class="sxs-lookup"><span data-stu-id="c9342-220">Entity relationships overview</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/relationships-overview)<br>
[<span data-ttu-id="c9342-221">创建和编辑包含来自外部数据源的数据的虚拟实体</span><span class="sxs-lookup"><span data-stu-id="c9342-221">Create and edit virtual entities that contain data from an external data source</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/create-edit-virtual-entities)<br>
[<span data-ttu-id="c9342-222">什么是 Power Apps 门户？</span><span class="sxs-lookup"><span data-stu-id="c9342-222">What is Power Apps portals?</span></span>](https://docs.microsoft.com/powerapps/maker/portals/overview)<br>
[<span data-ttu-id="c9342-223">在 Power Apps 中创建应用概述</span><span class="sxs-lookup"><span data-stu-id="c9342-223">Overview of creating apps in Power Apps</span></span>](https://docs.microsoft.com/powerapps/maker/)
