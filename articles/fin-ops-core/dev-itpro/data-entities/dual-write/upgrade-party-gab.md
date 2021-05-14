---
title: 升级到当事方和全球通讯簿模型
description: 本主题介绍如何将双重写入数据升级到当事方和全球通讯簿模型。
author: RamaKrishnamoorthy
ms.date: 03/31/2021
ms.topic: article
ms.service: dynamics-ax-applications
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-03-31
ms.openlocfilehash: 32128d48bfac195530d70b60e67cfd4921fc001e
ms.sourcegitcommit: a202bf67c3c2c054e2a47cb7b3145cb7c0ee635e
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/25/2021
ms.locfileid: "5941075"
---
# <a name="upgrade-to-the-party-and-global-address-book-model"></a><span data-ttu-id="4d292-103">升级到当事方和全球通讯簿模型</span><span class="sxs-lookup"><span data-stu-id="4d292-103">Upgrade to the party and global address book model</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="4d292-104">[Azure 数据工厂模板](https://aka.ms/dual-write-gab-adf)帮助您将采用双重写入的现有 **帐户**、**联系人** 和 **供应商** 表数据升级到当事方和全球通讯薄模型。</span><span class="sxs-lookup"><span data-stu-id="4d292-104">The [Azure Data Factory template](https://aka.ms/dual-write-gab-adf) helps you upgrade existing **Account**, **Contact**, and **Vendor** table data in dual-write to the party and global address book model.</span></span> <span data-ttu-id="4d292-105">模板将对帐 Finance and Operations 应用和 Customer Engagement 应用程序中的数据。</span><span class="sxs-lookup"><span data-stu-id="4d292-105">The template reconciles the data from both Finance and Operations apps and customer engagement applications.</span></span> <span data-ttu-id="4d292-106">在流程结束时，**当事方** 记录的 **当事方** 和 **联系人** 字段将创建，并与在 Customer Engagement 应用程序中的 **帐户**、**联系人** 和 **供应商** 记录相关联。</span><span class="sxs-lookup"><span data-stu-id="4d292-106">At the end of the process, **Party** and **Contact** fields for **Party** records will be created and associated with **Account**, **Contact**, and **Vendor** records in customer engagement applications.</span></span> <span data-ttu-id="4d292-107">将生成 .csv 文件 (`FONewParty.csv`) 以在 Finance and Operations 应用内创建新 **当事方** 记录。</span><span class="sxs-lookup"><span data-stu-id="4d292-107">A .csv file (`FONewParty.csv`) is generated to create new **Party** records inside the Finance and Operations app.</span></span> <span data-ttu-id="4d292-108">本主题提供使用数据工厂模板和升级数据的说明。</span><span class="sxs-lookup"><span data-stu-id="4d292-108">This topic provides the instructions to use the Data Factory template and upgrade your data.</span></span>

<span data-ttu-id="4d292-109">如果没有任何自定义，可以按原样使用模板。</span><span class="sxs-lookup"><span data-stu-id="4d292-109">If you don’t have any customizations, you can use the template as-is.</span></span> <span data-ttu-id="4d292-110">如果您有 **帐户**、**联系人** 和 **供应商** 的自定义，则必须使用以下说明修改模板。</span><span class="sxs-lookup"><span data-stu-id="4d292-110">If you have customizations for **Account**, **Contact**, and **Vendor** then you must modify the template using the following instructions.</span></span>

> [!Note]
> <span data-ttu-id="4d292-111">该模板可帮助仅升级 **当事方** 数据。</span><span class="sxs-lookup"><span data-stu-id="4d292-111">The template helps to upgrade only the **Party** data.</span></span> <span data-ttu-id="4d292-112">在将来的版本中，将包括邮寄地址和电子地址。</span><span class="sxs-lookup"><span data-stu-id="4d292-112">In a future release, postal and electronic addresses will be included.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="4d292-113">先决条件</span><span class="sxs-lookup"><span data-stu-id="4d292-113">Prerequisites</span></span>

<span data-ttu-id="4d292-114">需要以下先决条件：</span><span class="sxs-lookup"><span data-stu-id="4d292-114">These prerequisites are required:</span></span>

+ [<span data-ttu-id="4d292-115">Azure 预订</span><span class="sxs-lookup"><span data-stu-id="4d292-115">Azure subscription</span></span>](https://portal.azure.com/)
+ [<span data-ttu-id="4d292-116">模板访问权限</span><span class="sxs-lookup"><span data-stu-id="4d292-116">Access to the template</span></span>](https://aka.ms/dual-write-gab-adf)
+ <span data-ttu-id="4d292-117">您是现有的双重写入客户。</span><span class="sxs-lookup"><span data-stu-id="4d292-117">You are an existing dual-write customer.</span></span>

## <a name="prepare-for-the-upgrade"></a><span data-ttu-id="4d292-118">准备升级</span><span class="sxs-lookup"><span data-stu-id="4d292-118">Prepare for the upgrade</span></span>

+ <span data-ttu-id="4d292-119">**完全同步**：两种环境对于 **帐户(客户)**、**联系人** 和 **供应商** 均处于完全同步状态。</span><span class="sxs-lookup"><span data-stu-id="4d292-119">**Fully synched**: Both environments are fully synched state for **Account (Customer)**, **Contact**, and **Vendor**.</span></span>
+ <span data-ttu-id="4d292-120">**集成密钥**：Customer Engagement 应用中的 **帐户(客户)**、**联系人** 和 **供应商** 表使用现成提供的集成密钥。</span><span class="sxs-lookup"><span data-stu-id="4d292-120">**Integration keys**: **Account (Customer)**, **Contact**, and **Vendor** tables in customer engagement apps are using the integration keys that shipped out-of-the-box.</span></span> <span data-ttu-id="4d292-121">如果已自定义集成密钥，必须自定义模板。</span><span class="sxs-lookup"><span data-stu-id="4d292-121">If you customized the integration keys, you must customize the template.</span></span>
+ <span data-ttu-id="4d292-122">**当事方编号**：将升级的所有 **帐户(客户)**、**联系人** 和 **供应商** 记录都具有 **当事方** 编号。</span><span class="sxs-lookup"><span data-stu-id="4d292-122">**Party number**: All **Account (Customer)**, **Contact**, and **Vendor** records that will be upgraded have a **Party** number.</span></span> <span data-ttu-id="4d292-123">将忽略没有 **当事方** 编号的记录。</span><span class="sxs-lookup"><span data-stu-id="4d292-123">Records without a **Party** number will be ignored.</span></span> <span data-ttu-id="4d292-124">如果要升级这些记录，请在开始升级流程之前，向其添加 **当事方** 编号。</span><span class="sxs-lookup"><span data-stu-id="4d292-124">If you want to upgrade those records, add a **Party** number to them before you start the upgrade process.</span></span>
+ <span data-ttu-id="4d292-125">**系统中断**：在升级流程期间，您必须使 Finance and Operations 和 Customer Engagement 环境脱机。</span><span class="sxs-lookup"><span data-stu-id="4d292-125">**System outage**: During the upgrade process, you will have to take both the Finance and Operations and customer engagement environments offline.</span></span>
+ <span data-ttu-id="4d292-126">**快照**：拍摄 Finance and Operations 和 Customer Engagement 应用的快照。</span><span class="sxs-lookup"><span data-stu-id="4d292-126">**Snapshot**: Take snapshots of both the Finance and Operations and customer engagement apps.</span></span> <span data-ttu-id="4d292-127">如果需要，使用快照还原以前的状态。</span><span class="sxs-lookup"><span data-stu-id="4d292-127">Use the snapshots to restore the previous state if you need to.</span></span>

## <a name="deployment"></a><span data-ttu-id="4d292-128">部署</span><span class="sxs-lookup"><span data-stu-id="4d292-128">Deployment</span></span>

1. <span data-ttu-id="4d292-129">从 [Dynamics-365-FastTrack-Implementation-Assets](https://aka.ms/dual-write-gab-adf) 下载模板。</span><span class="sxs-lookup"><span data-stu-id="4d292-129">Download the template from [Dynamics-365-FastTrack-Implementation-Assets](https://aka.ms/dual-write-gab-adf).</span></span>

2. <span data-ttu-id="4d292-130">登录到 [Microsoft Azure](https://portal.azure.com/)。</span><span class="sxs-lookup"><span data-stu-id="4d292-130">Sign in to [Microsoft Azure](https://portal.azure.com/).</span></span>

3. <span data-ttu-id="4d292-131">创建[资源组](/azure/azure-resource-manager/management/manage-resource-groups-portal)。</span><span class="sxs-lookup"><span data-stu-id="4d292-131">Create a [resource group](/azure/azure-resource-manager/management/manage-resource-groups-portal).</span></span>

4. <span data-ttu-id="4d292-132">在创建的资源组中创建[存储帐户](/azure/storage/common/storage-account-create?tabs=azure-portal)。</span><span class="sxs-lookup"><span data-stu-id="4d292-132">Create a [storage account](/azure/storage/common/storage-account-create?tabs=azure-portal) in the resource group that you created.</span></span>

5. <span data-ttu-id="4d292-133">在创建的上述资源组中创建[数据工厂](/azure/data-factory/quickstart-create-data-factory-portal)。</span><span class="sxs-lookup"><span data-stu-id="4d292-133">Create a [data factory](/azure/data-factory/quickstart-create-data-factory-portal) in above resource group that you created.</span></span>

6. <span data-ttu-id="4d292-134">打开数据工厂，然后选择 **创作和监视** 磁贴。</span><span class="sxs-lookup"><span data-stu-id="4d292-134">Open the data factory and select the **Author & Monitor** tile.</span></span>

7. <span data-ttu-id="4d292-135">在 **管理** 选项卡上，选择 **ARM 模板**。</span><span class="sxs-lookup"><span data-stu-id="4d292-135">On the **Manage** tab, select **ARM template**.</span></span>

8. <span data-ttu-id="4d292-136">选择 **导入 ARM 模板** 以导入 **当事方** 模板。</span><span class="sxs-lookup"><span data-stu-id="4d292-136">Select the **Import ARM template** to import the **Party** template.</span></span>

9. <span data-ttu-id="4d292-137">将模板导入到数据工厂中。</span><span class="sxs-lookup"><span data-stu-id="4d292-137">Import the template into the data factory.</span></span> <span data-ttu-id="4d292-138">为 **项目详细信息** 和 **实例详细信息** 输入以下值。</span><span class="sxs-lookup"><span data-stu-id="4d292-138">Enter the following values for **Project details** and **Instance details**.</span></span>

    <span data-ttu-id="4d292-139">字段</span><span class="sxs-lookup"><span data-stu-id="4d292-139">Field</span></span> | <span data-ttu-id="4d292-140">值</span><span class="sxs-lookup"><span data-stu-id="4d292-140">Value</span></span>
    ---|---
    <span data-ttu-id="4d292-141">预订</span><span class="sxs-lookup"><span data-stu-id="4d292-141">Subscription</span></span> | <span data-ttu-id="4d292-142">Azure 预订</span><span class="sxs-lookup"><span data-stu-id="4d292-142">Azure subscription</span></span>
    <span data-ttu-id="4d292-143">资源组</span><span class="sxs-lookup"><span data-stu-id="4d292-143">Resource group</span></span> | <span data-ttu-id="4d292-144">提供在其下创建存储帐户的相同资源。</span><span class="sxs-lookup"><span data-stu-id="4d292-144">Provide same resource under which storage account is created.</span></span>
    <span data-ttu-id="4d292-145">区域</span><span class="sxs-lookup"><span data-stu-id="4d292-145">Region</span></span> | <span data-ttu-id="4d292-146">指定区域。</span><span class="sxs-lookup"><span data-stu-id="4d292-146">Specify region.</span></span>
    <span data-ttu-id="4d292-147">工厂名称</span><span class="sxs-lookup"><span data-stu-id="4d292-147">Factory Name</span></span> | <span data-ttu-id="4d292-148">指定工厂名称。</span><span class="sxs-lookup"><span data-stu-id="4d292-148">Specify factory name.</span></span>
    <span data-ttu-id="4d292-149">FO Linked Service_service Principal Key</span><span class="sxs-lookup"><span data-stu-id="4d292-149">FO Linked Service_service Principal Key</span></span> | <span data-ttu-id="4d292-150">指定应用程序的密钥。</span><span class="sxs-lookup"><span data-stu-id="4d292-150">Specify the application's key.</span></span>
    <span data-ttu-id="4d292-151">Azure Blob Storage_connection String</span><span class="sxs-lookup"><span data-stu-id="4d292-151">Azure Blob Storage_connection String</span></span> | <span data-ttu-id="4d292-152">Azure Blob 存储连接字符串。</span><span class="sxs-lookup"><span data-stu-id="4d292-152">Azure Blob storage connection string.</span></span>
    <span data-ttu-id="4d292-153">Dynamics Crm Linked Service_password</span><span class="sxs-lookup"><span data-stu-id="4d292-153">Dynamics Crm Linked Service_password</span></span> | <span data-ttu-id="4d292-154">您指定为用户名的用户帐户的密码。</span><span class="sxs-lookup"><span data-stu-id="4d292-154">The password for the user account you specified as the username.</span></span>
    <span data-ttu-id="4d292-155">FO Linked Service_properties_type Properties_url</span><span class="sxs-lookup"><span data-stu-id="4d292-155">FO Linked Service_properties_type Properties_url</span></span>  | `https://sampledynamics.sandbox-operationsdynamics.com/data`
    <span data-ttu-id="4d292-156">FO Linked Service_properties_type Properties_tenant</span><span class="sxs-lookup"><span data-stu-id="4d292-156">FO Linked Service_properties_type Properties_tenant</span></span> | <span data-ttu-id="4d292-157">指定您的应用程序所在的租户信息（域名或租户 ID）。</span><span class="sxs-lookup"><span data-stu-id="4d292-157">Specify the tenant information (domain name or tenant ID) under which your application resides.</span></span>
    <span data-ttu-id="4d292-158">FO Linked Service_properties_type Properties_aad Resource Id</span><span class="sxs-lookup"><span data-stu-id="4d292-158">FO Linked Service_properties_type Properties_aad Resource Id</span></span> | `https://sampledynamics.sandboxoperationsdynamics.com`
    <span data-ttu-id="4d292-159">FO Linked Service_properties_type Properties_service Principal Id</span><span class="sxs-lookup"><span data-stu-id="4d292-159">FO Linked Service_properties_type Properties_service Principal Id</span></span> | <span data-ttu-id="4d292-160">指定应用程序的客户端 ID。</span><span class="sxs-lookup"><span data-stu-id="4d292-160">Specify the application's client ID.</span></span>
    <span data-ttu-id="4d292-161">Dynamics Crm Linked Service_properties_type Properties_username</span><span class="sxs-lookup"><span data-stu-id="4d292-161">Dynamics Crm Linked Service_properties_type Properties_username</span></span> | <span data-ttu-id="4d292-162">连接到 Dynamics 的用户名。</span><span class="sxs-lookup"><span data-stu-id="4d292-162">The username to connect to Dynamics.</span></span>

    <span data-ttu-id="4d292-163">有关详细信息，请参阅[手动提升每个环境的资源管理器模板](/azure/data-factory/continuous-integration-deployment#manually-promote-a-resource-manager-template-for-each-environment)、[链接服务属性](/azure/data-factory/connector-dynamics-ax#linked-service-properties)和[使用 Azure 数据工厂复制数据](/azure/data-factory/connector-dynamics-crm-office-365#dynamics-365-and-dynamics-crm-online)</span><span class="sxs-lookup"><span data-stu-id="4d292-163">For more information, see [Manually promote a Resource Manager template for each environment](/azure/data-factory/continuous-integration-deployment#manually-promote-a-resource-manager-template-for-each-environment), [Linked service properties](/azure/data-factory/connector-dynamics-ax#linked-service-properties), and [Copy data using Azure Data Factory](/azure/data-factory/connector-dynamics-crm-office-365#dynamics-365-and-dynamics-crm-online)</span></span>

10. <span data-ttu-id="4d292-164">部署后，验证数据工厂的数据集、数据流和链接服务。</span><span class="sxs-lookup"><span data-stu-id="4d292-164">After deployment, validate the datasets, data flow, and linked service of the data factory.</span></span>

   ![数据集、数据流和链接服务](media/data-factory-validate.png)

11. <span data-ttu-id="4d292-166">导航到 **管理**。</span><span class="sxs-lookup"><span data-stu-id="4d292-166">Navigate to **Manage**.</span></span> <span data-ttu-id="4d292-167">在 **连接** 下，选择 **链接服务**。</span><span class="sxs-lookup"><span data-stu-id="4d292-167">Under **Connections**, select **Linked Service**.</span></span> <span data-ttu-id="4d292-168">选择 **DynamicsCrmLinkedService**。</span><span class="sxs-lookup"><span data-stu-id="4d292-168">Select **DynamicsCrmLinkedService**.</span></span> <span data-ttu-id="4d292-169">在 **编辑链接服务 (Dynamics CRM)** 窗体中，输入以下值：</span><span class="sxs-lookup"><span data-stu-id="4d292-169">In the **Edit linked service (Dynamics CRM)** form, enter the following values:</span></span>

    <span data-ttu-id="4d292-170">字段</span><span class="sxs-lookup"><span data-stu-id="4d292-170">Field</span></span> | <span data-ttu-id="4d292-171">值</span><span class="sxs-lookup"><span data-stu-id="4d292-171">Value</span></span>
    ---|---
    <span data-ttu-id="4d292-172">姓名</span><span class="sxs-lookup"><span data-stu-id="4d292-172">Name</span></span> | <span data-ttu-id="4d292-173">DynamicsCrmLinkedService</span><span class="sxs-lookup"><span data-stu-id="4d292-173">DynamicsCrmLinkedService</span></span>
    <span data-ttu-id="4d292-174">说明</span><span class="sxs-lookup"><span data-stu-id="4d292-174">Description</span></span> | <span data-ttu-id="4d292-175">要与 CRM 实例连接以提取实体数据的链接服务</span><span class="sxs-lookup"><span data-stu-id="4d292-175">Linked services to connect with CRM instance to fetch entities data</span></span>
    <span data-ttu-id="4d292-176">通过集成运行时连接</span><span class="sxs-lookup"><span data-stu-id="4d292-176">Connect via integration runtime</span></span> | <span data-ttu-id="4d292-177">AutoResolvelntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="4d292-177">AutoResolvelntegrationRuntime</span></span>
    <span data-ttu-id="4d292-178">部署类型</span><span class="sxs-lookup"><span data-stu-id="4d292-178">Deployment type</span></span> | <span data-ttu-id="4d292-179">联机</span><span class="sxs-lookup"><span data-stu-id="4d292-179">Online</span></span>
    <span data-ttu-id="4d292-180">服务 URI</span><span class="sxs-lookup"><span data-stu-id="4d292-180">Service Uri</span></span> | `https://<organization-name>.crm[x].dynamics.com`
    <span data-ttu-id="4d292-181">身份验证类型</span><span class="sxs-lookup"><span data-stu-id="4d292-181">Authentication type</span></span> | <span data-ttu-id="4d292-182">Office365</span><span class="sxs-lookup"><span data-stu-id="4d292-182">Office365</span></span>
    <span data-ttu-id="4d292-183">用户名</span><span class="sxs-lookup"><span data-stu-id="4d292-183">User name</span></span> |
    <span data-ttu-id="4d292-184">密码或 Azure 密钥保管库</span><span class="sxs-lookup"><span data-stu-id="4d292-184">Password or Azure Key Vault</span></span> | <span data-ttu-id="4d292-185">密码</span><span class="sxs-lookup"><span data-stu-id="4d292-185">Password</span></span>
    <span data-ttu-id="4d292-186">密码</span><span class="sxs-lookup"><span data-stu-id="4d292-186">Password</span></span> |

## <a name="run-the-template"></a><span data-ttu-id="4d292-187">运行模板</span><span class="sxs-lookup"><span data-stu-id="4d292-187">Run the template</span></span>

1. <span data-ttu-id="4d292-188">使用 Finance and Operations 应用停止以下 **帐户**、**联系人** 和 **供应商** 双重写入。</span><span class="sxs-lookup"><span data-stu-id="4d292-188">Stop the following **Account**, **Contact**, and **Vendor** dual-write using the Finance and Operations app.</span></span>

    + <span data-ttu-id="4d292-189">客户 V3 (accounts)</span><span class="sxs-lookup"><span data-stu-id="4d292-189">Customers V3(accounts)</span></span>
    + <span data-ttu-id="4d292-190">客户 V3（联系人）</span><span class="sxs-lookup"><span data-stu-id="4d292-190">Customers V3(contacts)</span></span>
    + <span data-ttu-id="4d292-191">CDS 联系人 V2（联系人）</span><span class="sxs-lookup"><span data-stu-id="4d292-191">CDS Contacts V2(contacts)</span></span>
    + <span data-ttu-id="4d292-192">CDS 联系人 V2（联系人）</span><span class="sxs-lookup"><span data-stu-id="4d292-192">CDS Contacts V2(contacts)</span></span>
    + <span data-ttu-id="4d292-193">供应商 V2 (msdyn_vendor)</span><span class="sxs-lookup"><span data-stu-id="4d292-193">Vendor V2 (msdyn_vendor)</span></span>

2. <span data-ttu-id="4d292-194">确保从 Dataverse 的 `msdy_dualwriteruntimeconfig` 表中删除地图。</span><span class="sxs-lookup"><span data-stu-id="4d292-194">Make sure the maps are removed from the `msdy_dualwriteruntimeconfig` table in Dataverse.</span></span>

3. <span data-ttu-id="4d292-195">从 AppSource 中安装[双重写入当事方和全球通讯簿解决方案](https://aka.ms/dual-write-gab)。</span><span class="sxs-lookup"><span data-stu-id="4d292-195">Install [Dual-write Party and Global Address Book Solutions](https://aka.ms/dual-write-gab) from AppSource.</span></span>

4. <span data-ttu-id="4d292-196">在 Finance and Operations 应用中，如果以下表包含数据，则针对它们运行 **初始同步**。</span><span class="sxs-lookup"><span data-stu-id="4d292-196">In the Finance and Operations app, if the following tables contain data, then run **Initial Sync** for them.</span></span>

    + <span data-ttu-id="4d292-197">称呼</span><span class="sxs-lookup"><span data-stu-id="4d292-197">Salutations</span></span>
    + <span data-ttu-id="4d292-198">人员特点类型</span><span class="sxs-lookup"><span data-stu-id="4d292-198">Personal character types</span></span>
    + <span data-ttu-id="4d292-199">结束语</span><span class="sxs-lookup"><span data-stu-id="4d292-199">Complimentary closing</span></span>
    + <span data-ttu-id="4d292-200">联系人职务</span><span class="sxs-lookup"><span data-stu-id="4d292-200">Contact person titles</span></span>
    + <span data-ttu-id="4d292-201">决策角色</span><span class="sxs-lookup"><span data-stu-id="4d292-201">Decision making roles</span></span>
    + <span data-ttu-id="4d292-202">忠诚度级别</span><span class="sxs-lookup"><span data-stu-id="4d292-202">Loyalty levels</span></span>

5. <span data-ttu-id="4d292-203">在 Customer Engagement 应用中，禁用以下插件步骤。</span><span class="sxs-lookup"><span data-stu-id="4d292-203">In the customer engagement app, disable the following plugin steps.</span></span>

    + <span data-ttu-id="4d292-204">帐户更新</span><span class="sxs-lookup"><span data-stu-id="4d292-204">Account Update</span></span>
         + <span data-ttu-id="4d292-205">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity：帐户的更新</span><span class="sxs-lookup"><span data-stu-id="4d292-205">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Update of account</span></span>
         + <span data-ttu-id="4d292-206">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes：帐户的更新</span><span class="sxs-lookup"><span data-stu-id="4d292-206">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Update of account</span></span>
    + <span data-ttu-id="4d292-207">联系人更新</span><span class="sxs-lookup"><span data-stu-id="4d292-207">Contact Update</span></span>
         + <span data-ttu-id="4d292-208">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity：联系人的更新</span><span class="sxs-lookup"><span data-stu-id="4d292-208">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Update of contact</span></span>
         + <span data-ttu-id="4d292-209">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact：联系人的更新</span><span class="sxs-lookup"><span data-stu-id="4d292-209">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Update of contact</span></span>
    + <span data-ttu-id="4d292-210">msdyn_party 更新</span><span class="sxs-lookup"><span data-stu-id="4d292-210">msdyn_party Update</span></span>
         + <span data-ttu-id="4d292-211">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity：msdyn_party 的更新</span><span class="sxs-lookup"><span data-stu-id="4d292-211">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: Update of msdyn_party</span></span>
    + <span data-ttu-id="4d292-212">msdyn_vendor 更新</span><span class="sxs-lookup"><span data-stu-id="4d292-212">msdyn_vendor Update</span></span>
         + <span data-ttu-id="4d292-213">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity：msdyn_vendor 的更新</span><span class="sxs-lookup"><span data-stu-id="4d292-213">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: Update of msdyn_vendor</span></span>

6. <span data-ttu-id="4d292-214">在 Customer Engagement 应用中，禁用以下工作流：</span><span class="sxs-lookup"><span data-stu-id="4d292-214">In the customer engagement app, disable the following workflows:</span></span>

    + <span data-ttu-id="4d292-215">在“客户”表中创建供应商</span><span class="sxs-lookup"><span data-stu-id="4d292-215">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="4d292-216">在“客户”表中创建供应商</span><span class="sxs-lookup"><span data-stu-id="4d292-216">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="4d292-217">在“联系人”表中创建个人类型的供应商</span><span class="sxs-lookup"><span data-stu-id="4d292-217">Create Vendors of type person in Contacts Table</span></span>
    + <span data-ttu-id="4d292-218">在“供应商”表中创建“个人”类型的供应商</span><span class="sxs-lookup"><span data-stu-id="4d292-218">Create Vendors of type Person in Vendors Table</span></span>
    + <span data-ttu-id="4d292-219">在“客户”表中更新供应商</span><span class="sxs-lookup"><span data-stu-id="4d292-219">Update Vendors in Accounts Table</span></span>
    + <span data-ttu-id="4d292-220">在“供应商”表中更新供应商</span><span class="sxs-lookup"><span data-stu-id="4d292-220">Update Vendors in Vendors Table</span></span>
    + <span data-ttu-id="4d292-221">在“联系人”表中更新“个人”类型的供应商</span><span class="sxs-lookup"><span data-stu-id="4d292-221">Update Vendors of type Person in Contacts Table</span></span>
    + <span data-ttu-id="4d292-222">在“供应商”表中更新“个人”类型的供应商</span><span class="sxs-lookup"><span data-stu-id="4d292-222">Update Vendors of type Person in Vendors Table</span></span>

7. <span data-ttu-id="4d292-223">在数据工厂中，通过选择 **立即触发** 运行模板，如下图所示。</span><span class="sxs-lookup"><span data-stu-id="4d292-223">In the data factory, run the template by selecting **Trigger now** as shown in the following image.</span></span> <span data-ttu-id="4d292-224">根据数据量，此流程可能需要几个小时才能完成。</span><span class="sxs-lookup"><span data-stu-id="4d292-224">This process might take a few hours to complete based on the data volume.</span></span>

    ![触发器运行](media/data-factory-trigger.png)

    > [!NOTE]
    > <span data-ttu-id="4d292-226">如果您有 **帐户**、**联系人** 和 **供应商** 的自定义，则必须修改模板。</span><span class="sxs-lookup"><span data-stu-id="4d292-226">If you have customizations for **Account**, **Contact**, and **Vendor** then you must modify the template.</span></span>

8. <span data-ttu-id="4d292-227">在 Finance and Operations 应用中导入新 **当事方** 记录。</span><span class="sxs-lookup"><span data-stu-id="4d292-227">Import the new **Party** records in the Finance and Operations app.</span></span>

    + <span data-ttu-id="4d292-228">从 Azure Blob 存储中下载 `FONewParty.csv` 文件。</span><span class="sxs-lookup"><span data-stu-id="4d292-228">Download the `FONewParty.csv` file from Azure blob storage.</span></span> <span data-ttu-id="4d292-229">路径为 `partybootstrapping/output/FONewParty.csv`。</span><span class="sxs-lookup"><span data-stu-id="4d292-229">The path is `partybootstrapping/output/FONewParty.csv`.</span></span>
    + <span data-ttu-id="4d292-230">将 `FONewParty.csv` 文件转换为 Excel 文件并将 Excel 文件导入到 Finance and Operations 应用中。</span><span class="sxs-lookup"><span data-stu-id="4d292-230">Convert the `FONewParty.csv` file into an Excel file and import the Excel file into the Finance and Operations app.</span></span>  <span data-ttu-id="4d292-231">如果 csv 导入适合您，您可以直接导入 csv 文件。</span><span class="sxs-lookup"><span data-stu-id="4d292-231">If the csv import works for you, you can import csv file directly.</span></span> <span data-ttu-id="4d292-232">导入可能需要几个小时才能运行，具体取决于数据量。</span><span class="sxs-lookup"><span data-stu-id="4d292-232">The import could take a few hours to run, depending on the data volume.</span></span> <span data-ttu-id="4d292-233">有关详细信息，请参阅[数据导入和导出作业概述](../data-import-export-job.md)。</span><span class="sxs-lookup"><span data-stu-id="4d292-233">For more information, see [Data import and export jobs overview](../data-import-export-job.md).</span></span>

    ![导入 Datavers 当事方记录](media/data-factory-import-party.png)

9. <span data-ttu-id="4d292-235">在 Customer Engagement 应用中，启用以下插件步骤：</span><span class="sxs-lookup"><span data-stu-id="4d292-235">In the customer engagement apps, enable the following plugin steps:</span></span>

    + <span data-ttu-id="4d292-236">帐户更新</span><span class="sxs-lookup"><span data-stu-id="4d292-236">Account Update</span></span>
         + <span data-ttu-id="4d292-237">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity：帐户的更新</span><span class="sxs-lookup"><span data-stu-id="4d292-237">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Update of account</span></span>
         + <span data-ttu-id="4d292-238">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes：帐户的更新</span><span class="sxs-lookup"><span data-stu-id="4d292-238">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Update of account</span></span>
    + <span data-ttu-id="4d292-239">联系人更新</span><span class="sxs-lookup"><span data-stu-id="4d292-239">Contact Update</span></span>
         + <span data-ttu-id="4d292-240">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity：联系人的更新</span><span class="sxs-lookup"><span data-stu-id="4d292-240">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Update of contact</span></span>
         + <span data-ttu-id="4d292-241">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact：联系人的更新</span><span class="sxs-lookup"><span data-stu-id="4d292-241">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Update of contact</span></span>
    + <span data-ttu-id="4d292-242">msdyn_party 更新</span><span class="sxs-lookup"><span data-stu-id="4d292-242">msdyn_party Update</span></span>
         + <span data-ttu-id="4d292-243">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity：msdyn_party 的更新</span><span class="sxs-lookup"><span data-stu-id="4d292-243">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: Update of msdyn_party</span></span>
    + <span data-ttu-id="4d292-244">msdyn_vendor 更新</span><span class="sxs-lookup"><span data-stu-id="4d292-244">msdyn_vendor Update</span></span>
         + <span data-ttu-id="4d292-245">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity：msdyn_vendor 的更新</span><span class="sxs-lookup"><span data-stu-id="4d292-245">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: Update of msdyn_vendor</span></span>

10. <span data-ttu-id="4d292-246">在 Customer Engagement 应用中，如果您在前面的步骤中停用了以下工作流，请激活它们：</span><span class="sxs-lookup"><span data-stu-id="4d292-246">In the customer engagement apps, activate the following workflows if you deactivated them in previous steps:</span></span>

    + <span data-ttu-id="4d292-247">在“客户”表中创建供应商</span><span class="sxs-lookup"><span data-stu-id="4d292-247">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="4d292-248">在“客户”表中创建供应商</span><span class="sxs-lookup"><span data-stu-id="4d292-248">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="4d292-249">在“联系人”表中创建个人类型的供应商</span><span class="sxs-lookup"><span data-stu-id="4d292-249">Create Vendors of type person in Contacts Table</span></span>
    + <span data-ttu-id="4d292-250">在“供应商”表中创建“个人”类型的供应商</span><span class="sxs-lookup"><span data-stu-id="4d292-250">Create Vendors of type Person in Vendors Table</span></span>
    + <span data-ttu-id="4d292-251">在“客户”表中更新供应商</span><span class="sxs-lookup"><span data-stu-id="4d292-251">Update Vendors in Accounts Table</span></span>
    + <span data-ttu-id="4d292-252">在“供应商”表中更新供应商</span><span class="sxs-lookup"><span data-stu-id="4d292-252">Update Vendors in Vendors Table</span></span>
    + <span data-ttu-id="4d292-253">在“联系人”表中更新“个人”类型的供应商</span><span class="sxs-lookup"><span data-stu-id="4d292-253">Update Vendors of type Person in Contacts Table</span></span>
    + <span data-ttu-id="4d292-254">在“供应商”表中更新“个人”类型的供应商</span><span class="sxs-lookup"><span data-stu-id="4d292-254">Update Vendors of type Person in Vendors Table</span></span>

11. <span data-ttu-id="4d292-255">运行与 **当事方** 相关的地图，如[当事方和全球通讯簿](party-gab.md)中所示。</span><span class="sxs-lookup"><span data-stu-id="4d292-255">Run the **Party**-related maps as instructed in [Party and global address book](party-gab.md).</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="4d292-256">疑难解答</span><span class="sxs-lookup"><span data-stu-id="4d292-256">Troubleshooting</span></span>

1. <span data-ttu-id="4d292-257">如果流程失败，从失败的活动开始重新运行数据工厂。</span><span class="sxs-lookup"><span data-stu-id="4d292-257">In the process fails, rerun the data factory starting from the failed activity.</span></span>
2. <span data-ttu-id="4d292-258">某些文件由可用于数据验证目的的数据工厂生成。</span><span class="sxs-lookup"><span data-stu-id="4d292-258">Some files are generated by the data factory that you can use for data validation purpose.</span></span>
3. <span data-ttu-id="4d292-259">基于以逗号分隔的 csv 文件运行数据工厂。</span><span class="sxs-lookup"><span data-stu-id="4d292-259">The data factory runs based on csv files that are comma-delimited.</span></span> <span data-ttu-id="4d292-260">如果字段值带有逗号，则可能会干扰结果。</span><span class="sxs-lookup"><span data-stu-id="4d292-260">If there is a field value that has a comma, it may interfere with the results.</span></span> <span data-ttu-id="4d292-261">您需要删除逗号。</span><span class="sxs-lookup"><span data-stu-id="4d292-261">You need to remove the commas.</span></span>
4. <span data-ttu-id="4d292-262">**监视** 选项卡提供有关所有步骤和已处理的数据的信息。</span><span class="sxs-lookup"><span data-stu-id="4d292-262">The **Monitoring** tab provides information about all steps and data processed.</span></span> <span data-ttu-id="4d292-263">选择特定步骤以对其进行调试。</span><span class="sxs-lookup"><span data-stu-id="4d292-263">Select a specific step to debug it.</span></span>

    ![监视选项卡](media/data-factory-monitor.png)

## <a name="learn-more-about-the-template"></a><span data-ttu-id="4d292-265">了解有关模板的详细信息</span><span class="sxs-lookup"><span data-stu-id="4d292-265">Learn more about the template</span></span>

<span data-ttu-id="4d292-266">您可以在 [readme.md](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/readme.md) 文件中找到模板的注释。</span><span class="sxs-lookup"><span data-stu-id="4d292-266">You can find comments for the template the [readme.md](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/readme.md) file.</span></span>