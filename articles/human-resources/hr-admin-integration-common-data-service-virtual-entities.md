---
title: 配置 Dataverse 虚拟表
description: 本主题介绍如何为 Dynamics 365 Human Resources 配置虚拟表。 生成和更新现有虚拟表，并分析生成的实体和可用表。
author: andreabichsel
manager: tfehr
ms.date: 01/25/2021
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
ms.openlocfilehash: d8780be777c9a204fcb95950f5679a5711aee298
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/17/2021
ms.locfileid: "5465814"
---
# <a name="configure-dataverse-virtual-tables"></a><span data-ttu-id="2de55-104">配置 Dataverse 虚拟表</span><span class="sxs-lookup"><span data-stu-id="2de55-104">Configure Dataverse virtual tables</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="2de55-105">Dynamics 365 Human Resources 是 Microsoft Dataverse 中的虚拟数据源。</span><span class="sxs-lookup"><span data-stu-id="2de55-105">Dynamics 365 Human Resources is a virtual data source in Microsoft Dataverse.</span></span> <span data-ttu-id="2de55-106">它提供 Dataverse 和 Microsoft Power Platform 中的完全创建、读取、更新和删除 (CRUD) 操作。</span><span class="sxs-lookup"><span data-stu-id="2de55-106">It provides full create, read, update, and delete (CRUD) operations from Dataverse and Microsoft Power Platform.</span></span> <span data-ttu-id="2de55-107">虚拟表的数据未存储在 Dataverse 中，但存储在应用程序数据库中。</span><span class="sxs-lookup"><span data-stu-id="2de55-107">The data for virtual tables isn't stored in Dataverse, but in the application database.</span></span>

<span data-ttu-id="2de55-108">若要从 Dataverse 中对 Human Resources 实体启用 CRUD 操作，您必须将这些实体用作 Dataverse 中的虚拟表。</span><span class="sxs-lookup"><span data-stu-id="2de55-108">To enable CRUD operations on Human Resources entities from Dataverse, you must make the entities available as virtual tables in Dataverse.</span></span> <span data-ttu-id="2de55-109">这使您可以从 Dataverse 和 Microsoft Power Platform 中对 Human Resources 中的数据执行 CRUD 操作。</span><span class="sxs-lookup"><span data-stu-id="2de55-109">This lets you perform CRUD operations from Dataverse and Microsoft Power Platform on data that's in Human Resources.</span></span> <span data-ttu-id="2de55-110">这些操作还支持对 Human Resources 进行完整业务逻辑验证，以确保将数据写入实体时的数据完整性。</span><span class="sxs-lookup"><span data-stu-id="2de55-110">The operations also support the full business logic validations of Human Resources to ensure data integrity when writing data to the entities.</span></span>

> [!NOTE]
> <span data-ttu-id="2de55-111">Human Resources 实体与 Dataverse 表对应。</span><span class="sxs-lookup"><span data-stu-id="2de55-111">Human Resources entities correspond to Dataverse tables.</span></span> <span data-ttu-id="2de55-112">有关 Dataverse（以前的 Common Data Service）和术语更新的详细信息，请参阅[什么是 Microsoft Dataverse？](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)</span><span class="sxs-lookup"><span data-stu-id="2de55-112">For more information about Dataverse (formerly Common Data Service) and terminology updates, see [What is Microsoft Dataverse?](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)</span></span>

## <a name="available-virtual-tables-for-human-resources"></a><span data-ttu-id="2de55-113">Human Resources 的可用虚拟表</span><span class="sxs-lookup"><span data-stu-id="2de55-113">Available virtual tables for Human Resources</span></span>

<span data-ttu-id="2de55-114">Human Resources 中的所有 Open Data Protocol (OData) 实体都可用作 Dataverse 中的虚拟表。</span><span class="sxs-lookup"><span data-stu-id="2de55-114">All Open Data Protocol (OData) entities in Human Resources are available as virtual tables in Dataverse.</span></span> <span data-ttu-id="2de55-115">它们在 Power Platform 中也可用。</span><span class="sxs-lookup"><span data-stu-id="2de55-115">They're also available in Power Platform.</span></span> <span data-ttu-id="2de55-116">您现在可以直接使用具有完全 CRUD 功能的 Human Resources 中的数据构建应用和体验，而无需将数据复制或同步到 Dataverse。</span><span class="sxs-lookup"><span data-stu-id="2de55-116">You can now build apps and experiences with data directly from Human Resources with full CRUD capability, without copying or synchronizing data to Dataverse.</span></span> <span data-ttu-id="2de55-117">您可以使用 Power Apps 门户来构建面向外部的网站，以为 Human Resources 中的业务流程启用协作方案。</span><span class="sxs-lookup"><span data-stu-id="2de55-117">You can use Power Apps portals to build external-facing websites that enable collaboration scenarios for business processes in Human Resources.</span></span>

<span data-ttu-id="2de55-118">您可以查看在环境中启用的虚拟表列表，然后开始使用 **Dynamics 365 HR 虚拟表** 解决方案的 [Power Apps](https://make.powerapps.com) 中的表。</span><span class="sxs-lookup"><span data-stu-id="2de55-118">You can view the list of virtual tables enabled in the environment, and begin working with the tables in [Power Apps](https://make.powerapps.com), in the **Dynamics 365 HR Virtual Tables** solution.</span></span>

![Power Apps 中的 Dynamics 365 HR 虚拟表](./media/hr-admin-integration-virtual-entities-power-apps.jpg)

## <a name="virtual-tables-versus-native-tables"></a><span data-ttu-id="2de55-120">虚拟表与本地表</span><span class="sxs-lookup"><span data-stu-id="2de55-120">Virtual tables versus native tables</span></span>

<span data-ttu-id="2de55-121">Human Resources 的虚拟表与为 Human Resources 创建的 Dataverse 本地表不同。</span><span class="sxs-lookup"><span data-stu-id="2de55-121">Virtual tables for Human Resources aren't the same as the native Dataverse tables created for Human Resources.</span></span> 

<span data-ttu-id="2de55-122">Human Resources 的本地表单独生成，并在 Dataverse 的 HCM 通用解决方案中维护。</span><span class="sxs-lookup"><span data-stu-id="2de55-122">The native tables for Human Resources are generated separately and maintained in the HCM Common solution in Dataverse.</span></span> <span data-ttu-id="2de55-123">对于本地表，数据存储在 Dataverse 中并且需要与 Human Resources 应用程序数据库同步。</span><span class="sxs-lookup"><span data-stu-id="2de55-123">With native tables, the data is stored in Dataverse and requires synchronization with the Human Resources application database.</span></span>

> [!NOTE]
> <span data-ttu-id="2de55-124">要获取 Human Resources 的 Dataverse 本地表列表，请参阅 [Dataverse 表](https://docs.microsoft.com/dynamics365/human-resources/hr-developer-entities)。</span><span class="sxs-lookup"><span data-stu-id="2de55-124">For a list of the native Dataverse tables for Human Resources, see [Dataverse tables](https://docs.microsoft.com/dynamics365/human-resources/hr-developer-entities).</span></span>

## <a name="setup"></a><span data-ttu-id="2de55-125">设置</span><span class="sxs-lookup"><span data-stu-id="2de55-125">Setup</span></span>

<span data-ttu-id="2de55-126">请按照以下设置步骤在您的环境中启用虚拟表。</span><span class="sxs-lookup"><span data-stu-id="2de55-126">Follow these setup steps to enable virtual tables in your environment.</span></span>

### <a name="enable-virtual-tables-in-human-resources"></a><span data-ttu-id="2de55-127">在 Human Resources 中启用虚拟表</span><span class="sxs-lookup"><span data-stu-id="2de55-127">Enable virtual tables in Human Resources</span></span>

<span data-ttu-id="2de55-128">首先，您必须在 **功能管理** 工作区中启用虚拟表。</span><span class="sxs-lookup"><span data-stu-id="2de55-128">First, you must enable virtual tables in the **Feature management** workspace.</span></span>

1. <span data-ttu-id="2de55-129">在 Human Resources 中，选择 **系统管理**。</span><span class="sxs-lookup"><span data-stu-id="2de55-129">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="2de55-130">选择 **功能管理** 磁贴。</span><span class="sxs-lookup"><span data-stu-id="2de55-130">Select the **Feature management** tile.</span></span>

3. <span data-ttu-id="2de55-131">选择 **Dataverse 中的 HR 虚拟表支持**，然后选择 **启用**。</span><span class="sxs-lookup"><span data-stu-id="2de55-131">Select **Virtual table support for HR in Dataverse**, and then select **Enable**.</span></span>

<span data-ttu-id="2de55-132">有关启用和禁用功能的详细信息，请参阅[管理功能](hr-admin-manage-features.md)。</span><span class="sxs-lookup"><span data-stu-id="2de55-132">For more information about enabling and disabling features, see [Manage features](hr-admin-manage-features.md).</span></span>

### <a name="register-the-app-in-microsoft-azure"></a><span data-ttu-id="2de55-133">在 Microsoft Azure 中注册应用</span><span class="sxs-lookup"><span data-stu-id="2de55-133">Register the app in Microsoft Azure</span></span>

<span data-ttu-id="2de55-134">您必须在 Azure 门户中注册 Human Resources 实例，以便 Microsoft 标识平台可以为应用和用户提供身份验证和授权服务。</span><span class="sxs-lookup"><span data-stu-id="2de55-134">You must register your Human Resources instance in the Azure portal so the Microsoft identity platform can provide authentication and authorization services for the app and users.</span></span> <span data-ttu-id="2de55-135">有关在 Azure 中注册应用的详细信息，请参阅[快速入门：向 Microsoft 标识平台注册应用程序](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app)。</span><span class="sxs-lookup"><span data-stu-id="2de55-135">For more information about registering apps in Azure, see [Quickstart: Register an application with the Microsoft identity platform](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app).</span></span>

1. <span data-ttu-id="2de55-136">打开 [Microsoft Azure 门户](https://portal.azure.com)。</span><span class="sxs-lookup"><span data-stu-id="2de55-136">Open the [Microsoft Azure portal](https://portal.azure.com).</span></span>

2. <span data-ttu-id="2de55-137">在 Azure 服务中，选择 **应用注册**。</span><span class="sxs-lookup"><span data-stu-id="2de55-137">In the Azure services list, select **App registrations**.</span></span>

3. <span data-ttu-id="2de55-138">选择 **新注册**。</span><span class="sxs-lookup"><span data-stu-id="2de55-138">Select **New registration**.</span></span>

4. <span data-ttu-id="2de55-139">在 **名称** 字段中，输入应用的描述性名称。</span><span class="sxs-lookup"><span data-stu-id="2de55-139">In the **Name** field, enter a descriptive name for the app.</span></span> <span data-ttu-id="2de55-140">例如，**Dynamics 365 Human Resources 虚拟表**。</span><span class="sxs-lookup"><span data-stu-id="2de55-140">For example, **Dynamics 365 Human Resources Virtual Tables**.</span></span>

5. <span data-ttu-id="2de55-141">在 **重定向 URI** 字段中，输入 Human Resources 实例的命名空间 URL。</span><span class="sxs-lookup"><span data-stu-id="2de55-141">In the **Redirect URI** field, enter the namespace URL of your instance of Human Resources.</span></span>

6. <span data-ttu-id="2de55-142">选择 **注册**。</span><span class="sxs-lookup"><span data-stu-id="2de55-142">Select **Register**.</span></span>

7. <span data-ttu-id="2de55-143">注册完成后，Azure 门户显示应用注册的 **概述** 窗格，其中包括其 **应用程序（客户端）ID**。</span><span class="sxs-lookup"><span data-stu-id="2de55-143">When registration completes, the Azure portal displays the app registration's **Overview** pane, which includes its **Application (client) ID**.</span></span> <span data-ttu-id="2de55-144">此时，请记下 **应用程序（客户端）ID**。</span><span class="sxs-lookup"><span data-stu-id="2de55-144">Take note of the **Application (client) ID** at this time.</span></span> <span data-ttu-id="2de55-145">您将在[配置虚拟表数据源](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-table-data-source)时输入此信息。</span><span class="sxs-lookup"><span data-stu-id="2de55-145">You'll enter this information when you [Configure the virtual table data source](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-table-data-source).</span></span>

8. <span data-ttu-id="2de55-146">在左侧导航窗格中，选择 **证书和密码**。</span><span class="sxs-lookup"><span data-stu-id="2de55-146">In the left navigation pane, select **Certificates and secrets**.</span></span>

9. <span data-ttu-id="2de55-147">在页面的 **客户端密码** 部分中，选择 **新客户端密码**。</span><span class="sxs-lookup"><span data-stu-id="2de55-147">In the **Client secrets** section of the page, select **New client secret**.</span></span>

10. <span data-ttu-id="2de55-148">提供描述，选择持续时间，然后选择 **添加**。</span><span class="sxs-lookup"><span data-stu-id="2de55-148">Provide a description, select a duration, and select **Add**.</span></span>

11. <span data-ttu-id="2de55-149">记录密码的值。</span><span class="sxs-lookup"><span data-stu-id="2de55-149">Record the secret's value.</span></span> <span data-ttu-id="2de55-150">您将在[配置虚拟表数据源](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-table-data-source)时输入此信息。</span><span class="sxs-lookup"><span data-stu-id="2de55-150">You'll enter this information when you [Configure the virtual table data source](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-table-data-source).</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="2de55-151">请确保此时记下密码的值。</span><span class="sxs-lookup"><span data-stu-id="2de55-151">Be sure to take note of the secret's value at this time.</span></span> <span data-ttu-id="2de55-152">离开此页面后，密码将不再显示。</span><span class="sxs-lookup"><span data-stu-id="2de55-152">The secret is never displayed again after you leave this page.</span></span>

### <a name="install-the-dynamics-365-hr-virtual-table-app"></a><span data-ttu-id="2de55-153">安装 Dynamics 365 HR 虚拟表应用</span><span class="sxs-lookup"><span data-stu-id="2de55-153">Install the Dynamics 365 HR Virtual Table app</span></span>

<span data-ttu-id="2de55-154">在您的 Power Apps 环境中安装 Dynamics 365 HR 虚拟表应用以将虚拟表解决方案包部署到 Dataverse。</span><span class="sxs-lookup"><span data-stu-id="2de55-154">Install the Dynamics 365 HR Virtual Table app in your Power Apps environment to deploy the virtual table solution package to Dataverse.</span></span>

1. <span data-ttu-id="2de55-155">打开 [Power Platform 管理中心](https://admin.powerplatform.microsoft.com)。</span><span class="sxs-lookup"><span data-stu-id="2de55-155">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="2de55-156">在 **环境** 列表中，选择与您的 Human Resources 实例关联的 Power Apps 环境。</span><span class="sxs-lookup"><span data-stu-id="2de55-156">In the **Environments** list, select the Power Apps environment associated with your Human Resources instance.</span></span>

3. <span data-ttu-id="2de55-157">在页面的 **资源** 部分中，选择 **Dynamics 365 应用**。</span><span class="sxs-lookup"><span data-stu-id="2de55-157">In the **Resources** section of the page, select **Dynamics 365 apps**.</span></span>

4. <span data-ttu-id="2de55-158">选择 **安装应用** 操作。</span><span class="sxs-lookup"><span data-stu-id="2de55-158">Select the **Install app** action.</span></span>

5. <span data-ttu-id="2de55-159">选择 **Dynamics 365 HR 虚拟表**，然后选择 **下一步**。</span><span class="sxs-lookup"><span data-stu-id="2de55-159">Select **Dynamics 365 HR Virtual Table**, and select **Next**.</span></span>

6. <span data-ttu-id="2de55-160">审查并标记以同意服务条款。</span><span class="sxs-lookup"><span data-stu-id="2de55-160">Review and mark to agree to the terms of service.</span></span>

7. <span data-ttu-id="2de55-161">选择 **安装**。</span><span class="sxs-lookup"><span data-stu-id="2de55-161">Select **Install**.</span></span>

<span data-ttu-id="2de55-162">安装需要几分钟时间。</span><span class="sxs-lookup"><span data-stu-id="2de55-162">The install takes a few minutes.</span></span> <span data-ttu-id="2de55-163">完成后，请继续执行后续步骤。</span><span class="sxs-lookup"><span data-stu-id="2de55-163">When it completes, continue to the next steps.</span></span>

![从 Power Platform 管理中心安装 Dynamics 365 HR 虚拟表应用](./media/hr-admin-integration-virtual-entities-power-platform-install.jpg)

### <a name="configure-the-virtual-table-data-source"></a><span data-ttu-id="2de55-165">配置虚拟表数据源</span><span class="sxs-lookup"><span data-stu-id="2de55-165">Configure the virtual table data source</span></span> 

<span data-ttu-id="2de55-166">下一步是在 Power Apps 环境中配置虚拟表数据源。</span><span class="sxs-lookup"><span data-stu-id="2de55-166">The next step is to configure the virtual table data source in the Power Apps environment.</span></span> 

1. <span data-ttu-id="2de55-167">打开 [Power Platform 管理中心](https://admin.powerplatform.microsoft.com)。</span><span class="sxs-lookup"><span data-stu-id="2de55-167">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="2de55-168">在 **环境** 列表中，选择与您的 Human Resources 实例关联的 Power Apps 环境。</span><span class="sxs-lookup"><span data-stu-id="2de55-168">In the **Environments** list, select the Power Apps environment associated with your Human Resources instance.</span></span>

3. <span data-ttu-id="2de55-169">在页面的 **详细信息** 部分中选择 **环境 URL**。</span><span class="sxs-lookup"><span data-stu-id="2de55-169">Select the **Environment URL** in the **Details** section of the page.</span></span>

4. <span data-ttu-id="2de55-170">在 **解决方案运行状况中心** 中，选择应用程序页面右上角的 **高级查找** 图标。</span><span class="sxs-lookup"><span data-stu-id="2de55-170">In the **Solution Health Hub**, select the **Advanced Find** icon in the top right of the application page.</span></span>

5. <span data-ttu-id="2de55-171">在 **高级查找** 页面上的 **查找** 下拉列表中，选择 **Finance and Operations 虚拟数据源配置**。</span><span class="sxs-lookup"><span data-stu-id="2de55-171">On the **Advanced Find** page, in the **Look for** dropdown list, select **Finance and Operations Virtual Data Source Configurations**.</span></span>

6. <span data-ttu-id="2de55-172">选择 **结果**。</span><span class="sxs-lookup"><span data-stu-id="2de55-172">Select **Results**.</span></span>

7. <span data-ttu-id="2de55-173">选择 **Microsoft HR 数据源** 记录。</span><span class="sxs-lookup"><span data-stu-id="2de55-173">Select the **Microsoft HR Data Source** record.</span></span>

8. <span data-ttu-id="2de55-174">输入数据源配置所需的信息：</span><span class="sxs-lookup"><span data-stu-id="2de55-174">Enter the required information for the data source configuration:</span></span>

   - <span data-ttu-id="2de55-175">**目标 URL**：Human Resources 命名空间的 URL。</span><span class="sxs-lookup"><span data-stu-id="2de55-175">**Target URL**: The URL of your Human Resources namespace.</span></span> <span data-ttu-id="2de55-176">目标 URL 的格式为：</span><span class="sxs-lookup"><span data-stu-id="2de55-176">The format of the target URL is:</span></span>
     
     <span data-ttu-id="2de55-177">https://\<hostname\>.hr.talent.dynamics.com/namespaces/\<namespaceID\>/</span><span class="sxs-lookup"><span data-stu-id="2de55-177">https://\<hostname\>.hr.talent.dynamics.com/namespaces/\<namespaceID\>/</span></span>

     <span data-ttu-id="2de55-178">例如:</span><span class="sxs-lookup"><span data-stu-id="2de55-178">For example:</span></span>
     
     `https://aos.rts-sf-5ea54e35c68-westus2.hr.talent.dynamics.com/namespaces/49d24c565-8f4d-4891-b174-bf83d948ed0c/`

     >[!NOTE]
     ><span data-ttu-id="2de55-179">确保在 URL 的结尾包括“**/**”字符，以避免收到错误。</span><span class="sxs-lookup"><span data-stu-id="2de55-179">Be sure to include the "**/**" character at the end of the URL to avoid receiving an error.</span></span>

   - <span data-ttu-id="2de55-180">**租户 ID**：Azure Active Directory (Azure AD) 租户 ID。</span><span class="sxs-lookup"><span data-stu-id="2de55-180">**Tenant ID**: The Azure Active Directory (Azure AD) tenant ID.</span></span>

   - <span data-ttu-id="2de55-181">**AAD 应用程序 ID**：为在 Microsoft Azure 门户中注册的应用程序创建的应用程序（客户端）ID。</span><span class="sxs-lookup"><span data-stu-id="2de55-181">**AAD Application ID**: The application (client) ID created for the application registered in the Microsoft Azure portal.</span></span> <span data-ttu-id="2de55-182">您在步骤[在 Microsoft Azure 中注册应用](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure)的早期阶段就收到了此信息。</span><span class="sxs-lookup"><span data-stu-id="2de55-182">You received this information earlier during the step [Register the app in Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span></span>

   - <span data-ttu-id="2de55-183">**AAD 应用程序密码**：为在 Microsoft Azure 门户中注册的应用程序创建的客户端密码。</span><span class="sxs-lookup"><span data-stu-id="2de55-183">**AAD Application Secret**: The client secret created for the application registered in the Microsoft Azure portal.</span></span> <span data-ttu-id="2de55-184">您在步骤[在 Microsoft Azure 中注册应用](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure)的早期阶段就收到了此信息。</span><span class="sxs-lookup"><span data-stu-id="2de55-184">You received this information earlier during the step [Register the app in Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span></span>

   ![Microsoft HR 数据源](./media/hr-admin-integration-virtual-entities-hr-data-source.jpg)

9. <span data-ttu-id="2de55-186">选择 **保存并关闭**。</span><span class="sxs-lookup"><span data-stu-id="2de55-186">Select **Save & Close**.</span></span>

### <a name="grant-app-permissions-in-human-resources"></a><span data-ttu-id="2de55-187">在 Human Resources 中授予应用权限</span><span class="sxs-lookup"><span data-stu-id="2de55-187">Grant app permissions in Human Resources</span></span>

<span data-ttu-id="2de55-188">在 Human Resources 中为两个 Azure AD 应用程序授予权限：</span><span class="sxs-lookup"><span data-stu-id="2de55-188">Grant permissions for the two Azure AD applications in Human Resources:</span></span>

- <span data-ttu-id="2de55-189">在 Microsoft Azure 门户中为您的租户创建的应用</span><span class="sxs-lookup"><span data-stu-id="2de55-189">The app created for your tenant in the Microsoft Azure portal</span></span>
- <span data-ttu-id="2de55-190">在 Power Apps 环境中安装的 Dynamics 365 HR 虚拟表应用</span><span class="sxs-lookup"><span data-stu-id="2de55-190">The Dynamics 365 HR Virtual Table app installed in the Power Apps environment</span></span> 

1. <span data-ttu-id="2de55-191">在 Human Resources 中，打开 **Azure Active Directory 应用程序** 页面。</span><span class="sxs-lookup"><span data-stu-id="2de55-191">In Human Resources, open the **Azure Active Directory applications** page.</span></span>

2. <span data-ttu-id="2de55-192">选择 **新建** 以创建新的应用程序记录：</span><span class="sxs-lookup"><span data-stu-id="2de55-192">Select **New** to create a new application record:</span></span>

    - <span data-ttu-id="2de55-193">在 **客户端 ID** 字段中，输入您在 Microsoft Azure 门户中注册的应用的客户端 ID。</span><span class="sxs-lookup"><span data-stu-id="2de55-193">In the **Client ID** field, enter the client ID of the app you registered in the Microsoft Azure portal.</span></span>
    - <span data-ttu-id="2de55-194">在 **名称** 字段中，输入您在 Microsoft Azure 门户中注册的应用的名称。</span><span class="sxs-lookup"><span data-stu-id="2de55-194">In the **Name** field, enter the name of the app you registered in the Microsoft Azure portal.</span></span>
    - <span data-ttu-id="2de55-195">在 **用户 ID** 字段中，在 Human Resources 和 Power Apps 环境中选择具有管理员权限的用户的用户 ID。</span><span class="sxs-lookup"><span data-stu-id="2de55-195">In the **User ID** field, select the user ID of a user with admin permissions in Human Resources and the Power Apps environment.</span></span>

3. <span data-ttu-id="2de55-196">选择 **新建** 以创建第二个应用程序记录：</span><span class="sxs-lookup"><span data-stu-id="2de55-196">Select **New** to create a second application record:</span></span>

    - <span data-ttu-id="2de55-197">**客户端 ID**：f9be0c49-aa22-4ec6-911a-c5da515226ff</span><span class="sxs-lookup"><span data-stu-id="2de55-197">**Client Id**: f9be0c49-aa22-4ec6-911a-c5da515226ff</span></span>
    - <span data-ttu-id="2de55-198">**名称**：Dynamics 365 HR 虚拟表</span><span class="sxs-lookup"><span data-stu-id="2de55-198">**Name**: Dynamics 365 HR Virtual Table</span></span>
    - <span data-ttu-id="2de55-199">在 **用户 ID** 字段中，在 Human Resources 和 Power Apps 环境中选择具有管理员权限的用户的用户 ID。</span><span class="sxs-lookup"><span data-stu-id="2de55-199">In the **User ID** field, select the user ID of a user with admin permissions in Human Resources and the Power Apps environment.</span></span>

## <a name="generate-virtual-tables"></a><span data-ttu-id="2de55-200">生成虚拟表</span><span class="sxs-lookup"><span data-stu-id="2de55-200">Generate virtual tables</span></span>

<span data-ttu-id="2de55-201">设置完成后，您可以选择要在 Dataverse 实例中生成和启用的虚拟表。</span><span class="sxs-lookup"><span data-stu-id="2de55-201">When setup completes, you can select the virtual tables you want to generate and enable in your Dataverse instance.</span></span>

1. <span data-ttu-id="2de55-202">在 Human Resources 中，打开 **Dataverse 集成** 页面。</span><span class="sxs-lookup"><span data-stu-id="2de55-202">In Human Resources, open the **Dataverse integration** page.</span></span>

2. <span data-ttu-id="2de55-203">选择 **虚拟表** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="2de55-203">Select the **Virtual tables** tab.</span></span>

> [!NOTE]
> <span data-ttu-id="2de55-204">在完成所有所需的设置后，**启用虚拟表** 切换将自动设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="2de55-204">The **Enable virtual tables** toggle will be set to **Yes** automatically when all required setup has been completed.</span></span> <span data-ttu-id="2de55-205">如果切换设置为 **否**，请查看本文档前面部分中的步骤，以确保完成所有先决条件设置。</span><span class="sxs-lookup"><span data-stu-id="2de55-205">If the toggle is set to **No**, review the steps in previous sections of this document to ensure all prerequisite setup is completed.</span></span>

3. <span data-ttu-id="2de55-206">选择要在 Dataverse 中生成的一个或多个表。</span><span class="sxs-lookup"><span data-stu-id="2de55-206">Select the table or tables you want to generate in Dataverse.</span></span>

4. <span data-ttu-id="2de55-207">选择 **生成/刷新**。</span><span class="sxs-lookup"><span data-stu-id="2de55-207">Select **Generate/refresh**.</span></span>

![Dataverse 集成](./media/hr-admin-integration-common-data-service-integration.jpg)

## <a name="check-table-generation-status"></a><span data-ttu-id="2de55-209">检查表生成状态</span><span class="sxs-lookup"><span data-stu-id="2de55-209">Check table generation status</span></span>

<span data-ttu-id="2de55-210">虚拟表通过异步后台进程在 Dataverse 中生成。</span><span class="sxs-lookup"><span data-stu-id="2de55-210">Virtual tables are generated in Dataverse through an asynchronous background process.</span></span> <span data-ttu-id="2de55-211">有关进程的更新显示在操作中心中。</span><span class="sxs-lookup"><span data-stu-id="2de55-211">Updates on the process display in the action center.</span></span> <span data-ttu-id="2de55-212">有关进程的详细信息（包括错误日志）显示在 **进程自动化** 页面中。</span><span class="sxs-lookup"><span data-stu-id="2de55-212">Details on the process, including error logs, appear in the **Process automations** page.</span></span>

1. <span data-ttu-id="2de55-213">在 Human Resources 中，打开 **进程自动化** 页面。</span><span class="sxs-lookup"><span data-stu-id="2de55-213">In Human Resources, open the **Process automations** page.</span></span>

2. <span data-ttu-id="2de55-214">选择 **后台进程** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="2de55-214">Select the **Background processes** tab.</span></span>

3. <span data-ttu-id="2de55-215">选择 **虚拟表轮询异步操作后台进程**。</span><span class="sxs-lookup"><span data-stu-id="2de55-215">Select **Virtual table poll async operation background process**.</span></span>

4. <span data-ttu-id="2de55-216">选择 **查看最新结果**。</span><span class="sxs-lookup"><span data-stu-id="2de55-216">Select **View most recent results**.</span></span>

<span data-ttu-id="2de55-217">滑出窗格将显示该进程的最新执行结果。</span><span class="sxs-lookup"><span data-stu-id="2de55-217">The slideout pane displays the most recent execution results for the process.</span></span> <span data-ttu-id="2de55-218">您可以查看进程的日志，包括从 Dataverse 返回的任何错误。</span><span class="sxs-lookup"><span data-stu-id="2de55-218">You can view the log for the process, including any errors returned from Dataverse.</span></span>

## <a name="see-also"></a><span data-ttu-id="2de55-219">请参阅</span><span class="sxs-lookup"><span data-stu-id="2de55-219">See also</span></span>

[<span data-ttu-id="2de55-220">什么是 Dataverse？</span><span class="sxs-lookup"><span data-stu-id="2de55-220">What is Dataverse?</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro)<br>
[<span data-ttu-id="2de55-221">Dataverse 中的表</span><span class="sxs-lookup"><span data-stu-id="2de55-221">Tables in Dataverse</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/entity-overview)<br>
[<span data-ttu-id="2de55-222">表关系概述</span><span class="sxs-lookup"><span data-stu-id="2de55-222">Table relationships overview</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/relationships-overview)<br>
[<span data-ttu-id="2de55-223">创建和编辑包含来自外部数据源的数据的虚拟表</span><span class="sxs-lookup"><span data-stu-id="2de55-223">Create and edit virtual tables that contain data from an external data source</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/create-edit-virtual-entities)<br>
[<span data-ttu-id="2de55-224">什么是 Power Apps 门户？</span><span class="sxs-lookup"><span data-stu-id="2de55-224">What is Power Apps portals?</span></span>](https://docs.microsoft.com/powerapps/maker/portals/overview)<br>
[<span data-ttu-id="2de55-225">在 Power Apps 中创建应用概述</span><span class="sxs-lookup"><span data-stu-id="2de55-225">Overview of creating apps in Power Apps</span></span>](https://docs.microsoft.com/powerapps/maker/)


[!INCLUDE[footer-include](../includes/footer-banner.md)]