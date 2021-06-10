---
title: 升级到当事方和全球通讯簿模型
description: 本主题介绍如何将双重写入数据升级到当事方和全球通讯簿模型。
author: RamaKrishnamoorthy
ms.date: 03/31/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-03-31
ms.openlocfilehash: 90ddbe704ab21d62752b581a813601e8986c2103
ms.sourcegitcommit: 180548e3c10459776cf199989d3753e0c1555912
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/28/2021
ms.locfileid: "6112665"
---
# <a name="upgrade-to-the-party-and-global-address-book-model"></a><span data-ttu-id="066ba-103">升级到当事方和全球通讯簿模型</span><span class="sxs-lookup"><span data-stu-id="066ba-103">Upgrade to the party and global address book model</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="066ba-104">[Microsoft Azure 数据工厂模板](https://aka.ms/dual-write-gab-adf)帮助您将采用双重写入的现有 **客户**、**联系人** 和 **供应商** 表数据升级到当事方和全球通讯薄模型。</span><span class="sxs-lookup"><span data-stu-id="066ba-104">The [Microsoft Azure Data Factory template](https://aka.ms/dual-write-gab-adf) helps you upgrade existing **Account**, **Contact**, and **Vendor** table data in dual-write to the party and global address book model.</span></span> <span data-ttu-id="066ba-105">模板将对帐 Finance and Operations 应用和 Customer Engagement 应用程序中的数据。</span><span class="sxs-lookup"><span data-stu-id="066ba-105">The template reconciles the data from both finance and operations apps and customer engagement applications.</span></span> <span data-ttu-id="066ba-106">在流程结束时，**当事方** 记录的 **当事方** 和 **联系人** 字段将创建，并与在 Customer Engagement 应用程序中的 **帐户**、**联系人** 和 **供应商** 记录相关联。</span><span class="sxs-lookup"><span data-stu-id="066ba-106">At the end of the process, **Party** and **Contact** fields for **Party** records will be created and associated with **Account**, **Contact**, and **Vendor** records in customer engagement applications.</span></span> <span data-ttu-id="066ba-107">将生成 .csv 文件 (`FONewParty.csv`) 以在 Finance and Operations 应用内创建新 **当事方** 记录。</span><span class="sxs-lookup"><span data-stu-id="066ba-107">A .csv file (`FONewParty.csv`) is generated to create new **Party** records inside the finance and operations app.</span></span> <span data-ttu-id="066ba-108">本主题提供如何使用数据工厂模板和升级数据的说明。</span><span class="sxs-lookup"><span data-stu-id="066ba-108">This topic provides instructions about how to use the Data Factory template and upgrade your data.</span></span>

<span data-ttu-id="066ba-109">如果没有任何自定义，可以按原样使用模板。</span><span class="sxs-lookup"><span data-stu-id="066ba-109">If you don’t have any customizations, you can use the template as is.</span></span> <span data-ttu-id="066ba-110">如果您有 **帐户**、**联系人** 和 **供应商** 的自定义，则必须使用以下说明修改模板。</span><span class="sxs-lookup"><span data-stu-id="066ba-110">If you have customizations for **Account**, **Contact**, and **Vendor** then you must modify the template using the following instructions.</span></span>

> [!NOTE]
> <span data-ttu-id="066ba-111">此模板仅升级 **当事方** 数据。</span><span class="sxs-lookup"><span data-stu-id="066ba-111">The template only upgrades the **Party** data.</span></span> <span data-ttu-id="066ba-112">在将来的版本中，将包括邮寄地址和电子地址。</span><span class="sxs-lookup"><span data-stu-id="066ba-112">In a future release, postal and electronic addresses will be included.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="066ba-113">先决条件</span><span class="sxs-lookup"><span data-stu-id="066ba-113">Prerequisites</span></span>

<span data-ttu-id="066ba-114">要升级到当事方和全球通讯簿模型，需要满足以下先决条件：</span><span class="sxs-lookup"><span data-stu-id="066ba-114">The following prerequisites are required to upgrade to the party and global address book model:</span></span>

+ [<span data-ttu-id="066ba-115">Azure 预订</span><span class="sxs-lookup"><span data-stu-id="066ba-115">Azure subscription</span></span>](https://portal.azure.com/)
+ [<span data-ttu-id="066ba-116">模板访问权限</span><span class="sxs-lookup"><span data-stu-id="066ba-116">Access to the template</span></span>](https://aka.ms/dual-write-gab-adf)
+ <span data-ttu-id="066ba-117">您必须是现有的双写入客户。</span><span class="sxs-lookup"><span data-stu-id="066ba-117">You must be an existing dual-write customer.</span></span>

## <a name="prepare-for-the-upgrade"></a><span data-ttu-id="066ba-118">准备升级</span><span class="sxs-lookup"><span data-stu-id="066ba-118">Prepare for the upgrade</span></span>
<span data-ttu-id="066ba-119">需要进行以下活动来为升级作准备：</span><span class="sxs-lookup"><span data-stu-id="066ba-119">The following activities are needed to prepare for the upgrade:</span></span>

+ <span data-ttu-id="066ba-120">**完全同步**：两种环境对于 **客户**、**联系人** 和 **供应商** 均处于完全同步状态。</span><span class="sxs-lookup"><span data-stu-id="066ba-120">**Fully synced**: Both environments are in a fully synced state for **Account (Customer)**, **Contact**, and **Vendor**.</span></span>
+ <span data-ttu-id="066ba-121">**集成密钥**：Customer Engagement 应用中的 **帐户(客户)**、**联系人** 和 **供应商** 表使用现成提供的集成密钥。</span><span class="sxs-lookup"><span data-stu-id="066ba-121">**Integration keys**: **Account (Customer)**, **Contact**, and **Vendor** tables in customer engagement apps are using the integration keys that shipped out-of-the-box.</span></span> <span data-ttu-id="066ba-122">如果已自定义集成密钥，必须自定义模板。</span><span class="sxs-lookup"><span data-stu-id="066ba-122">If you customized the integration keys, you must customize the template.</span></span>
+ <span data-ttu-id="066ba-123">**当事方编号**：将升级的所有 **帐户(客户)**、**联系人** 和 **供应商** 记录都具有 **当事方** 编号。</span><span class="sxs-lookup"><span data-stu-id="066ba-123">**Party number**: All **Account (Customer)**, **Contact**, and **Vendor** records that will be upgraded have a **Party** number.</span></span> <span data-ttu-id="066ba-124">将忽略没有 **当事方** 编号的记录。</span><span class="sxs-lookup"><span data-stu-id="066ba-124">Records without a **Party** number will be ignored.</span></span> <span data-ttu-id="066ba-125">如果要升级这些记录，请在开始升级流程之前，向其添加 **当事方** 编号。</span><span class="sxs-lookup"><span data-stu-id="066ba-125">If you want to upgrade those records, add a **Party** number to them before you start the upgrade process.</span></span>
+ <span data-ttu-id="066ba-126">**系统中断**：在升级流程期间，您必须使 Finance and Operations 和 Customer Engagement 环境脱机。</span><span class="sxs-lookup"><span data-stu-id="066ba-126">**System outage**: During the upgrade process, you will have to take both the finance and operations and customer engagement environments offline.</span></span>
+ <span data-ttu-id="066ba-127">**快照**：拍摄 Finance and Operations 和 Customer Engagement 应用的快照。</span><span class="sxs-lookup"><span data-stu-id="066ba-127">**Snapshot**: Take snapshots of both the finance and operations apps and customer engagement apps.</span></span> <span data-ttu-id="066ba-128">如果需要，使用快照还原以前的状态。</span><span class="sxs-lookup"><span data-stu-id="066ba-128">Use the snapshots to restore the previous state if you need to.</span></span>

## <a name="deployment"></a><span data-ttu-id="066ba-129">部署</span><span class="sxs-lookup"><span data-stu-id="066ba-129">Deployment</span></span>

1. <span data-ttu-id="066ba-130">从 [Dynamics-365-FastTrack-Implementation-Assets](https://aka.ms/dual-write-gab-adf) 下载模板。</span><span class="sxs-lookup"><span data-stu-id="066ba-130">Download the template from [Dynamics-365-FastTrack-Implementation-Assets](https://aka.ms/dual-write-gab-adf).</span></span>

2. <span data-ttu-id="066ba-131">登录到 [Microsoft Azure](https://portal.azure.com/)。</span><span class="sxs-lookup"><span data-stu-id="066ba-131">Sign in to [Microsoft Azure](https://portal.azure.com/).</span></span>

3. <span data-ttu-id="066ba-132">创建[资源组](/azure/azure-resource-manager/management/manage-resource-groups-portal)。</span><span class="sxs-lookup"><span data-stu-id="066ba-132">Create a [resource group](/azure/azure-resource-manager/management/manage-resource-groups-portal).</span></span>

4. <span data-ttu-id="066ba-133">在创建的资源组中创建[存储帐户](/azure/storage/common/storage-account-create?tabs=azure-portal)。</span><span class="sxs-lookup"><span data-stu-id="066ba-133">Create a [storage account](/azure/storage/common/storage-account-create?tabs=azure-portal) in the resource group that you created.</span></span>

5. <span data-ttu-id="066ba-134">在创建的上述资源组中创建[数据工厂](/azure/data-factory/quickstart-create-data-factory-portal)。</span><span class="sxs-lookup"><span data-stu-id="066ba-134">Create a [data factory](/azure/data-factory/quickstart-create-data-factory-portal) in above resource group that you created.</span></span>

6. <span data-ttu-id="066ba-135">打开数据工厂，然后选择 **创作和监视** 磁贴。</span><span class="sxs-lookup"><span data-stu-id="066ba-135">Open the data factory and select the **Author & Monitor** tile.</span></span>

7. <span data-ttu-id="066ba-136">在 **管理** 选项卡上，选择 **ARM 模板**。</span><span class="sxs-lookup"><span data-stu-id="066ba-136">On the **Manage** tab, select **ARM template**.</span></span>

8. <span data-ttu-id="066ba-137">选择 **导入 ARM 模板** 以导入 **当事方** 模板。</span><span class="sxs-lookup"><span data-stu-id="066ba-137">Select the **Import ARM template** to import the **Party** template.</span></span>

9. <span data-ttu-id="066ba-138">将模板导入到数据工厂中。</span><span class="sxs-lookup"><span data-stu-id="066ba-138">Import the template into the data factory.</span></span> <span data-ttu-id="066ba-139">为 **项目详细信息** 和 **实例详细信息** 输入以下值。</span><span class="sxs-lookup"><span data-stu-id="066ba-139">Enter the following values for **Project details** and **Instance details**.</span></span>

    <span data-ttu-id="066ba-140">字段</span><span class="sxs-lookup"><span data-stu-id="066ba-140">Field</span></span> | <span data-ttu-id="066ba-141">值</span><span class="sxs-lookup"><span data-stu-id="066ba-141">Value</span></span>
    ---|---
    <span data-ttu-id="066ba-142">预订</span><span class="sxs-lookup"><span data-stu-id="066ba-142">Subscription</span></span> | <span data-ttu-id="066ba-143">Azure 预订</span><span class="sxs-lookup"><span data-stu-id="066ba-143">Azure subscription</span></span>
    <span data-ttu-id="066ba-144">资源组</span><span class="sxs-lookup"><span data-stu-id="066ba-144">Resource group</span></span> | <span data-ttu-id="066ba-145">提供在其下创建存储帐户的相同资源。</span><span class="sxs-lookup"><span data-stu-id="066ba-145">Provide same resource under which storage account is created.</span></span>
    <span data-ttu-id="066ba-146">区域</span><span class="sxs-lookup"><span data-stu-id="066ba-146">Region</span></span> | <span data-ttu-id="066ba-147">指定区域。</span><span class="sxs-lookup"><span data-stu-id="066ba-147">Specify region.</span></span>
    <span data-ttu-id="066ba-148">工厂名称</span><span class="sxs-lookup"><span data-stu-id="066ba-148">Factory Name</span></span> | <span data-ttu-id="066ba-149">指定工厂名称。</span><span class="sxs-lookup"><span data-stu-id="066ba-149">Specify factory name.</span></span>
    <span data-ttu-id="066ba-150">FO Linked Service_service Principal Key</span><span class="sxs-lookup"><span data-stu-id="066ba-150">FO Linked Service_service Principal Key</span></span> | <span data-ttu-id="066ba-151">指定应用程序的密钥。</span><span class="sxs-lookup"><span data-stu-id="066ba-151">Specify the application's key.</span></span>
    <span data-ttu-id="066ba-152">Azure Blob Storage_connection String</span><span class="sxs-lookup"><span data-stu-id="066ba-152">Azure Blob Storage_connection String</span></span> | <span data-ttu-id="066ba-153">Azure Blob 存储连接字符串。</span><span class="sxs-lookup"><span data-stu-id="066ba-153">Azure Blob storage connection string.</span></span>
    <span data-ttu-id="066ba-154">Dynamics Crm Linked Service_password</span><span class="sxs-lookup"><span data-stu-id="066ba-154">Dynamics Crm Linked Service_password</span></span> | <span data-ttu-id="066ba-155">您指定为用户名的用户帐户的密码。</span><span class="sxs-lookup"><span data-stu-id="066ba-155">The password for the user account you specified as the username.</span></span>
    <span data-ttu-id="066ba-156">FO Linked Service_properties_type Properties_url</span><span class="sxs-lookup"><span data-stu-id="066ba-156">FO Linked Service_properties_type Properties_url</span></span>  | `https://sampledynamics.sandbox-operationsdynamics.com/data`
    <span data-ttu-id="066ba-157">FO Linked Service_properties_type Properties_tenant</span><span class="sxs-lookup"><span data-stu-id="066ba-157">FO Linked Service_properties_type Properties_tenant</span></span> | <span data-ttu-id="066ba-158">指定您的应用程序所在的租户信息（域名或租户 ID）。</span><span class="sxs-lookup"><span data-stu-id="066ba-158">Specify the tenant information (domain name or tenant ID) under which your application resides.</span></span>
    <span data-ttu-id="066ba-159">FO Linked Service_properties_type Properties_aad Resource Id</span><span class="sxs-lookup"><span data-stu-id="066ba-159">FO Linked Service_properties_type Properties_aad Resource Id</span></span> | `https://sampledynamics.sandboxoperationsdynamics.com`
    <span data-ttu-id="066ba-160">FO Linked Service_properties_type Properties_service Principal Id</span><span class="sxs-lookup"><span data-stu-id="066ba-160">FO Linked Service_properties_type Properties_service Principal Id</span></span> | <span data-ttu-id="066ba-161">指定应用程序的客户端 ID。</span><span class="sxs-lookup"><span data-stu-id="066ba-161">Specify the application's client ID.</span></span>
    <span data-ttu-id="066ba-162">Dynamics Crm Linked Service_properties_type Properties_username</span><span class="sxs-lookup"><span data-stu-id="066ba-162">Dynamics Crm Linked Service_properties_type Properties_username</span></span> | <span data-ttu-id="066ba-163">连接到 Dynamics 365 的用户名。</span><span class="sxs-lookup"><span data-stu-id="066ba-163">The username to connect to Dynamics 365.</span></span>

    <span data-ttu-id="066ba-164">有关其他信息，请参阅以下主题：</span><span class="sxs-lookup"><span data-stu-id="066ba-164">For additional information, refer to the following topics:</span></span> 
    
    - [<span data-ttu-id="066ba-165">手动提升每个环境的资源管理器模板</span><span class="sxs-lookup"><span data-stu-id="066ba-165">Manually promote a Resource Manager template for each environment</span></span>](/azure/data-factory/continuous-integration-deployment#manually-promote-a-resource-manager-template-for-each-environment)
    - [<span data-ttu-id="066ba-166">链接服务属性</span><span class="sxs-lookup"><span data-stu-id="066ba-166">Linked service properties</span></span>](/azure/data-factory/connector-dynamics-ax#linked-service-properties)
    - [<span data-ttu-id="066ba-167">使用 Azure 数据工厂复制数据</span><span class="sxs-lookup"><span data-stu-id="066ba-167">Copy data using Azure Data Factory</span></span>](/azure/data-factory/connector-dynamics-crm-office-365#dynamics-365-and-dynamics-crm-online)

10. <span data-ttu-id="066ba-168">部署后，验证数据工厂的数据集、数据流和链接服务。</span><span class="sxs-lookup"><span data-stu-id="066ba-168">After deployment, validate the datasets, data flow, and linked service of the data factory.</span></span>

   ![数据集、数据流和链接服务](media/data-factory-validate.png)

11. <span data-ttu-id="066ba-170">导航到 **管理**。</span><span class="sxs-lookup"><span data-stu-id="066ba-170">Navigate to **Manage**.</span></span> <span data-ttu-id="066ba-171">在 **连接** 下，选择 **链接服务**。</span><span class="sxs-lookup"><span data-stu-id="066ba-171">Under **Connections**, select **Linked Service**.</span></span> <span data-ttu-id="066ba-172">选择 **DynamicsCrmLinkedService**。</span><span class="sxs-lookup"><span data-stu-id="066ba-172">Select **DynamicsCrmLinkedService**.</span></span> <span data-ttu-id="066ba-173">在 **编辑链接服务 (Dynamics CRM)** 窗体中，输入以下值。</span><span class="sxs-lookup"><span data-stu-id="066ba-173">In the **Edit linked service (Dynamics CRM)** form, enter the following values.</span></span>

    <span data-ttu-id="066ba-174">字段</span><span class="sxs-lookup"><span data-stu-id="066ba-174">Field</span></span> | <span data-ttu-id="066ba-175">值</span><span class="sxs-lookup"><span data-stu-id="066ba-175">Value</span></span>
    ---|---
    <span data-ttu-id="066ba-176">姓名</span><span class="sxs-lookup"><span data-stu-id="066ba-176">Name</span></span> | <span data-ttu-id="066ba-177">DynamicsCrmLinkedService</span><span class="sxs-lookup"><span data-stu-id="066ba-177">DynamicsCrmLinkedService</span></span>
    <span data-ttu-id="066ba-178">说明</span><span class="sxs-lookup"><span data-stu-id="066ba-178">Description</span></span> | <span data-ttu-id="066ba-179">要与 CRM 实例连接以提取实体数据的链接服务</span><span class="sxs-lookup"><span data-stu-id="066ba-179">Linked services to connect with CRM instance to fetch entities data</span></span>
    <span data-ttu-id="066ba-180">通过集成运行时连接</span><span class="sxs-lookup"><span data-stu-id="066ba-180">Connect via integration runtime</span></span> | <span data-ttu-id="066ba-181">AutoResolvelntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="066ba-181">AutoResolvelntegrationRuntime</span></span>
    <span data-ttu-id="066ba-182">部署类型</span><span class="sxs-lookup"><span data-stu-id="066ba-182">Deployment type</span></span> | <span data-ttu-id="066ba-183">联机</span><span class="sxs-lookup"><span data-stu-id="066ba-183">Online</span></span>
    <span data-ttu-id="066ba-184">服务 URI</span><span class="sxs-lookup"><span data-stu-id="066ba-184">Service Uri</span></span> | `https://<organization-name>.crm[x].dynamics.com`
    <span data-ttu-id="066ba-185">身份验证类型</span><span class="sxs-lookup"><span data-stu-id="066ba-185">Authentication type</span></span> | <span data-ttu-id="066ba-186">Office365</span><span class="sxs-lookup"><span data-stu-id="066ba-186">Office365</span></span>
    <span data-ttu-id="066ba-187">用户名</span><span class="sxs-lookup"><span data-stu-id="066ba-187">User name</span></span> |
    <span data-ttu-id="066ba-188">密码或 Azure 密钥保管库</span><span class="sxs-lookup"><span data-stu-id="066ba-188">Password or Azure Key Vault</span></span> | <span data-ttu-id="066ba-189">密码</span><span class="sxs-lookup"><span data-stu-id="066ba-189">Password</span></span>
    <span data-ttu-id="066ba-190">密码</span><span class="sxs-lookup"><span data-stu-id="066ba-190">Password</span></span> |

## <a name="run-the-template"></a><span data-ttu-id="066ba-191">运行模板</span><span class="sxs-lookup"><span data-stu-id="066ba-191">Run the template</span></span>

1. <span data-ttu-id="066ba-192">使用 Finance and Operations 应用停止以下 **客户**、**联系人** 和 **供应商** 双写入映射。</span><span class="sxs-lookup"><span data-stu-id="066ba-192">Stop the following **Account**, **Contact**, and **Vendor** dual-write maps using the Finance and Operations app.</span></span>

    + <span data-ttu-id="066ba-193">客户 V3 (accounts)</span><span class="sxs-lookup"><span data-stu-id="066ba-193">Customers V3(accounts)</span></span>
    + <span data-ttu-id="066ba-194">客户 V3（联系人）</span><span class="sxs-lookup"><span data-stu-id="066ba-194">Customers V3(contacts)</span></span>
    + <span data-ttu-id="066ba-195">CDS 联系人 V2（联系人）</span><span class="sxs-lookup"><span data-stu-id="066ba-195">CDS Contacts V2(contacts)</span></span>
    + <span data-ttu-id="066ba-196">CDS 联系人 V2（联系人）</span><span class="sxs-lookup"><span data-stu-id="066ba-196">CDS Contacts V2(contacts)</span></span>
    + <span data-ttu-id="066ba-197">供应商 V2 (msdyn_vendor)</span><span class="sxs-lookup"><span data-stu-id="066ba-197">Vendor V2 (msdyn_vendor)</span></span>

2. <span data-ttu-id="066ba-198">确保从 Dataverse 的 `msdy_dualwriteruntimeconfig` 表中删除地图。</span><span class="sxs-lookup"><span data-stu-id="066ba-198">Make sure the maps are removed from the `msdy_dualwriteruntimeconfig` table in Dataverse.</span></span>

3. <span data-ttu-id="066ba-199">从 AppSource 中安装[双重写入当事方和全球通讯簿解决方案](https://aka.ms/dual-write-gab)。</span><span class="sxs-lookup"><span data-stu-id="066ba-199">Install [Dual-write Party and Global Address Book Solutions](https://aka.ms/dual-write-gab) from AppSource.</span></span>

4. <span data-ttu-id="066ba-200">在 Finance and Operations 应用中，如果以下表包含数据，则针对它们 **运行初始同步**。</span><span class="sxs-lookup"><span data-stu-id="066ba-200">In the finance and operations app, if the following tables contain data, then run **Initial Sync** for them.</span></span>

    + <span data-ttu-id="066ba-201">称呼</span><span class="sxs-lookup"><span data-stu-id="066ba-201">Salutations</span></span>
    + <span data-ttu-id="066ba-202">人员特点类型</span><span class="sxs-lookup"><span data-stu-id="066ba-202">Personal character types</span></span>
    + <span data-ttu-id="066ba-203">结束语</span><span class="sxs-lookup"><span data-stu-id="066ba-203">Complimentary closing</span></span>
    + <span data-ttu-id="066ba-204">联系人职务</span><span class="sxs-lookup"><span data-stu-id="066ba-204">Contact person titles</span></span>
    + <span data-ttu-id="066ba-205">决策角色</span><span class="sxs-lookup"><span data-stu-id="066ba-205">Decision making roles</span></span>
    + <span data-ttu-id="066ba-206">忠诚度级别</span><span class="sxs-lookup"><span data-stu-id="066ba-206">Loyalty levels</span></span>

5. <span data-ttu-id="066ba-207">在 Customer Engagement 应用中，禁用以下插件步骤。</span><span class="sxs-lookup"><span data-stu-id="066ba-207">In the customer engagement app, disable the following plug-in steps.</span></span>

    + <span data-ttu-id="066ba-208">帐户更新</span><span class="sxs-lookup"><span data-stu-id="066ba-208">Account Update</span></span>
         + <span data-ttu-id="066ba-209">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity：帐户的更新</span><span class="sxs-lookup"><span data-stu-id="066ba-209">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Update of account</span></span>
         + <span data-ttu-id="066ba-210">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes：帐户的更新</span><span class="sxs-lookup"><span data-stu-id="066ba-210">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Update of account</span></span>
    + <span data-ttu-id="066ba-211">联系人更新</span><span class="sxs-lookup"><span data-stu-id="066ba-211">Contact Update</span></span>
         + <span data-ttu-id="066ba-212">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity：联系人的更新</span><span class="sxs-lookup"><span data-stu-id="066ba-212">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Update of contact</span></span>
         + <span data-ttu-id="066ba-213">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact：联系人的更新</span><span class="sxs-lookup"><span data-stu-id="066ba-213">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Update of contact</span></span>
    + <span data-ttu-id="066ba-214">msdyn_party 更新</span><span class="sxs-lookup"><span data-stu-id="066ba-214">msdyn_party Update</span></span>
         + <span data-ttu-id="066ba-215">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity：msdyn_party 的更新</span><span class="sxs-lookup"><span data-stu-id="066ba-215">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: Update of msdyn_party</span></span>
    + <span data-ttu-id="066ba-216">msdyn_vendor 更新</span><span class="sxs-lookup"><span data-stu-id="066ba-216">msdyn_vendor Update</span></span>
         + <span data-ttu-id="066ba-217">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity：msdyn_vendor 的更新</span><span class="sxs-lookup"><span data-stu-id="066ba-217">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: Update of msdyn_vendor</span></span>

6. <span data-ttu-id="066ba-218">在 Customer Engagement 应用中，禁用以下工作流：</span><span class="sxs-lookup"><span data-stu-id="066ba-218">In the customer engagement app, disable the following workflows:</span></span>

    + <span data-ttu-id="066ba-219">在“客户”表中创建供应商</span><span class="sxs-lookup"><span data-stu-id="066ba-219">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="066ba-220">在“客户”表中创建供应商</span><span class="sxs-lookup"><span data-stu-id="066ba-220">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="066ba-221">在“联系人”表中创建个人类型的供应商</span><span class="sxs-lookup"><span data-stu-id="066ba-221">Create Vendors of type person in Contacts Table</span></span>
    + <span data-ttu-id="066ba-222">在“供应商”表中创建“个人”类型的供应商</span><span class="sxs-lookup"><span data-stu-id="066ba-222">Create Vendors of type Person in Vendors Table</span></span>
    + <span data-ttu-id="066ba-223">在“客户”表中更新供应商</span><span class="sxs-lookup"><span data-stu-id="066ba-223">Update Vendors in Accounts Table</span></span>
    + <span data-ttu-id="066ba-224">在“供应商”表中更新供应商</span><span class="sxs-lookup"><span data-stu-id="066ba-224">Update Vendors in Vendors Table</span></span>
    + <span data-ttu-id="066ba-225">在“联系人”表中更新“个人”类型的供应商</span><span class="sxs-lookup"><span data-stu-id="066ba-225">Update Vendors of type Person in Contacts Table</span></span>
    + <span data-ttu-id="066ba-226">在“供应商”表中更新“个人”类型的供应商</span><span class="sxs-lookup"><span data-stu-id="066ba-226">Update Vendors of type Person in Vendors Table</span></span>

7. <span data-ttu-id="066ba-227">在数据工厂中，通过选择 **立即触发** 运行模板，如下图所示。</span><span class="sxs-lookup"><span data-stu-id="066ba-227">In the data factory, run the template by selecting **Trigger now** as shown in the following image.</span></span> <span data-ttu-id="066ba-228">根据数据量，此流程可能需要几个小时才能完成。</span><span class="sxs-lookup"><span data-stu-id="066ba-228">This process might take a few hours to complete based on the data volume.</span></span>

    ![触发器运行](media/data-factory-trigger.png)

    > [!NOTE]
    > <span data-ttu-id="066ba-230">如果您有 **客户**、**联系人** 和 **供应商** 的自定义，则需要修改模板。</span><span class="sxs-lookup"><span data-stu-id="066ba-230">If you have customizations for **Account**, **Contact**, and **Vendor**, then you need to modify the template.</span></span>

8. <span data-ttu-id="066ba-231">在 Finance and Operations 应用中导入新 **当事方** 记录。</span><span class="sxs-lookup"><span data-stu-id="066ba-231">Import the new **Party** records in the Finance and Operations app.</span></span>

    + <span data-ttu-id="066ba-232">从 Azure Blob 存储中下载 `FONewParty.csv` 文件。</span><span class="sxs-lookup"><span data-stu-id="066ba-232">Download the `FONewParty.csv` file from Azure blob storage.</span></span> <span data-ttu-id="066ba-233">路径为 `partybootstrapping/output/FONewParty.csv`。</span><span class="sxs-lookup"><span data-stu-id="066ba-233">The path is `partybootstrapping/output/FONewParty.csv`.</span></span>
    + <span data-ttu-id="066ba-234">将 `FONewParty.csv` 文件转换为 Excel 文件并将 Excel 文件导入到 Finance and Operations 应用中。</span><span class="sxs-lookup"><span data-stu-id="066ba-234">Convert the `FONewParty.csv` file into an Excel file and import the Excel file into the finance and operations app.</span></span> <span data-ttu-id="066ba-235">如果 csv 导入适合您，您可以直接导入 csv 文件。</span><span class="sxs-lookup"><span data-stu-id="066ba-235">If the csv import works for you, you can import the csv file directly.</span></span> <span data-ttu-id="066ba-236">导入可能需要几个小时才能运行，具体取决于数据量。</span><span class="sxs-lookup"><span data-stu-id="066ba-236">The import could take a few hours to run, depending on the data volume.</span></span> <span data-ttu-id="066ba-237">有关详细信息，请参阅[数据导入和导出作业概述](../data-import-export-job.md)。</span><span class="sxs-lookup"><span data-stu-id="066ba-237">For more information, see [Data import and export jobs overview](../data-import-export-job.md).</span></span>

    ![导入 Datavers 当事方记录](media/data-factory-import-party.png)

9. <span data-ttu-id="066ba-239">在 Customer Engagement 应用中，启用以下插件步骤：</span><span class="sxs-lookup"><span data-stu-id="066ba-239">In the customer engagement apps, enable the following plug-in steps:</span></span>

    + <span data-ttu-id="066ba-240">帐户更新</span><span class="sxs-lookup"><span data-stu-id="066ba-240">Account Update</span></span>
         + <span data-ttu-id="066ba-241">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity：帐户的更新</span><span class="sxs-lookup"><span data-stu-id="066ba-241">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Update of account</span></span>
         + <span data-ttu-id="066ba-242">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes：帐户的更新</span><span class="sxs-lookup"><span data-stu-id="066ba-242">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Update of account</span></span>
    + <span data-ttu-id="066ba-243">联系人更新</span><span class="sxs-lookup"><span data-stu-id="066ba-243">Contact Update</span></span>
         + <span data-ttu-id="066ba-244">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity：联系人的更新</span><span class="sxs-lookup"><span data-stu-id="066ba-244">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Update of contact</span></span>
         + <span data-ttu-id="066ba-245">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact：联系人的更新</span><span class="sxs-lookup"><span data-stu-id="066ba-245">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Update of contact</span></span>
    + <span data-ttu-id="066ba-246">msdyn_party 更新</span><span class="sxs-lookup"><span data-stu-id="066ba-246">msdyn_party Update</span></span>
         + <span data-ttu-id="066ba-247">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity：msdyn_party 的更新</span><span class="sxs-lookup"><span data-stu-id="066ba-247">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: Update of msdyn_party</span></span>
    + <span data-ttu-id="066ba-248">msdyn_vendor 更新</span><span class="sxs-lookup"><span data-stu-id="066ba-248">msdyn_vendor Update</span></span>
         + <span data-ttu-id="066ba-249">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity：msdyn_vendor 的更新</span><span class="sxs-lookup"><span data-stu-id="066ba-249">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: Update of msdyn_vendor</span></span>

10. <span data-ttu-id="066ba-250">在 Customer Engagement 应用中，如果您在前面的步骤中停用了以下工作流，请激活它们：</span><span class="sxs-lookup"><span data-stu-id="066ba-250">In the customer engagement apps, activate the following workflows if you deactivated them in previous steps:</span></span>

    + <span data-ttu-id="066ba-251">在“客户”表中创建供应商</span><span class="sxs-lookup"><span data-stu-id="066ba-251">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="066ba-252">在“客户”表中创建供应商</span><span class="sxs-lookup"><span data-stu-id="066ba-252">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="066ba-253">在“联系人”表中创建个人类型的供应商</span><span class="sxs-lookup"><span data-stu-id="066ba-253">Create Vendors of type person in Contacts Table</span></span>
    + <span data-ttu-id="066ba-254">在“供应商”表中创建“个人”类型的供应商</span><span class="sxs-lookup"><span data-stu-id="066ba-254">Create Vendors of type Person in Vendors Table</span></span>
    + <span data-ttu-id="066ba-255">在“客户”表中更新供应商</span><span class="sxs-lookup"><span data-stu-id="066ba-255">Update Vendors in Accounts Table</span></span>
    + <span data-ttu-id="066ba-256">在“供应商”表中更新供应商</span><span class="sxs-lookup"><span data-stu-id="066ba-256">Update Vendors in Vendors Table</span></span>
    + <span data-ttu-id="066ba-257">在“联系人”表中更新“个人”类型的供应商</span><span class="sxs-lookup"><span data-stu-id="066ba-257">Update Vendors of type Person in Contacts Table</span></span>
    + <span data-ttu-id="066ba-258">在“供应商”表中更新“个人”类型的供应商</span><span class="sxs-lookup"><span data-stu-id="066ba-258">Update Vendors of type Person in Vendors Table</span></span>

11. <span data-ttu-id="066ba-259">运行与 **当事方** 相关的地图，如[当事方和全球通讯簿](party-gab.md)中所示。</span><span class="sxs-lookup"><span data-stu-id="066ba-259">Run the **Party**-related maps as instructed in [Party and global address book](party-gab.md).</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="066ba-260">疑难解答</span><span class="sxs-lookup"><span data-stu-id="066ba-260">Troubleshooting</span></span>

1. <span data-ttu-id="066ba-261">如果流程失败，从失败的活动开始重新运行数据工厂。</span><span class="sxs-lookup"><span data-stu-id="066ba-261">If the process fails, rerun the data factory starting from the failed activity.</span></span>
2. <span data-ttu-id="066ba-262">某些文件由可用于数据验证目的的数据工厂生成。</span><span class="sxs-lookup"><span data-stu-id="066ba-262">Some files are generated by the data factory that you can use for data validation purpose.</span></span>
3. <span data-ttu-id="066ba-263">基于以逗号分隔的 csv 文件运行数据工厂。</span><span class="sxs-lookup"><span data-stu-id="066ba-263">The data factory runs based on csv files that are comma-delimited.</span></span> <span data-ttu-id="066ba-264">如果字段值带有逗号，则可能会干扰结果。</span><span class="sxs-lookup"><span data-stu-id="066ba-264">If there is a field value that has a comma, it may interfere with the results.</span></span> <span data-ttu-id="066ba-265">您需要删除逗号。</span><span class="sxs-lookup"><span data-stu-id="066ba-265">You need to remove the commas.</span></span>
4. <span data-ttu-id="066ba-266">**监视** 选项卡提供有关所有步骤和已处理的数据的信息。</span><span class="sxs-lookup"><span data-stu-id="066ba-266">The **Monitoring** tab provides information about all steps and data processed.</span></span> <span data-ttu-id="066ba-267">选择特定步骤以对其进行调试。</span><span class="sxs-lookup"><span data-stu-id="066ba-267">Select a specific step to debug it.</span></span>

    ![监视选项卡](media/data-factory-monitor.png)

## <a name="learn-more-about-the-template"></a><span data-ttu-id="066ba-269">了解有关模板的详细信息</span><span class="sxs-lookup"><span data-stu-id="066ba-269">Learn more about the template</span></span>

<span data-ttu-id="066ba-270">您可以在 [Azure 数据工厂模板自述文件注释](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/readme.md)中找到有关模板的其他信息。</span><span class="sxs-lookup"><span data-stu-id="066ba-270">You can find additional information about the template in [Comments for Azure Data Factory template readme](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/readme.md).</span></span>
