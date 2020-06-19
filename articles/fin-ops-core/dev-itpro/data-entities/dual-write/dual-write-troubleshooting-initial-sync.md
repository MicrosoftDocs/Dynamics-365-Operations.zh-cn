---
title: 解决初始同步过程中的问题
description: 本主题提供故障排除信息，可以帮助您解决初始同步期间可能发生的问题。
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 10065039fce441d7f96f700ff826d959e96f2479
ms.sourcegitcommit: cecd97fd74ff7b31f1a677e8fdf3e233aa28ef5a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/28/2020
ms.locfileid: "3410073"
---
# <a name="troubleshoot-issues-during-initial-synchronization"></a><span data-ttu-id="508d3-103">解决初始同步过程中的问题</span><span class="sxs-lookup"><span data-stu-id="508d3-103">Troubleshoot issues during initial synchronization</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="508d3-104">本主题提供 Finance and Operations 应用与 Common Data Service 之间的双写入集成的故障排除信息。</span><span class="sxs-lookup"><span data-stu-id="508d3-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="508d3-105">具体来说，提供可以帮助您解决初始同步期间可能发生的问题的信息。</span><span class="sxs-lookup"><span data-stu-id="508d3-105">Specifically, it provides information that can help you fix issues that might occur during initial synchronization.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="508d3-106">本主题解决的某些问题可能需要系统管理员角色或 Microsoft Azure Active Directory (Azure AD) 租户管理员凭据。</span><span class="sxs-lookup"><span data-stu-id="508d3-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="508d3-107">介绍每个问题的每一节说明了是否需要特定角色或凭据。</span><span class="sxs-lookup"><span data-stu-id="508d3-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="check-for-initial-synchronization-errors-in-a-finance-and-operations-app"></a><span data-ttu-id="508d3-108">在 Finance and Operations 应用中检查初始同步错误</span><span class="sxs-lookup"><span data-stu-id="508d3-108">Check for initial synchronization errors in a Finance and Operations app</span></span>

<span data-ttu-id="508d3-109">启用映射模板后，映射的状态应为**正在运行**。</span><span class="sxs-lookup"><span data-stu-id="508d3-109">After you enable the mapping templates, the status of the maps should be **Running**.</span></span> <span data-ttu-id="508d3-110">如果状态为**未运行**，在初始同步期间将发生错误。</span><span class="sxs-lookup"><span data-stu-id="508d3-110">If the status is **Not running**, errors occurred during initial synchronization.</span></span> <span data-ttu-id="508d3-111">要查看错误，请选择**双写入**页面上的**初始同步详细信息**选项卡。</span><span class="sxs-lookup"><span data-stu-id="508d3-111">To view the errors, select the **Initial sync details** tab on the **Dual-write** page.</span></span>

![初始同步详细信息选项卡](media/initial_sync_status.png)

## <a name="you-cant-complete-initial-synchronization-400-bad-request"></a><span data-ttu-id="508d3-113">您无法完成初始同步：400 错误请求</span><span class="sxs-lookup"><span data-stu-id="508d3-113">You can't complete initial synchronization: 400 Bad Request</span></span>

<span data-ttu-id="508d3-114">**解决此问题所需的角色：** 系统管理员</span><span class="sxs-lookup"><span data-stu-id="508d3-114">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="508d3-115">当您尝试运行映射和初始同步时，您可能会收到以下错误消息：</span><span class="sxs-lookup"><span data-stu-id="508d3-115">You might receive the following error message when you try to run the mapping and initial synchronization:</span></span>

<span data-ttu-id="508d3-116">*远程服务器返回错误：(400) 错误请求。），AX 导出遇到错误*</span><span class="sxs-lookup"><span data-stu-id="508d3-116">*The remote server returned an error: (400) Bad Request.), AX export encountered an error*</span></span>

<span data-ttu-id="508d3-117">以下是完整错误消息的示例。</span><span class="sxs-lookup"><span data-stu-id="508d3-117">Here is an example of the full error message.</span></span>

```console
Dual write Initial Sync completed with status: Error. Following are the details:
Executed leg: From AX Financial dimensions to CRM msdyn_dimensionattributes
with exported records count: 0, ImportRecordsErrorCount: 0,
ImportRecordsInsertedCount: 0 and ImportRecordsUpdatedCount: 0
ErrorsDetails:
Dual write Initial sync failed
Message: ([Bad Request], The remote server returned an error: (400) Bad Request.), AX export encountered an error
Stacktrace: at
Microsoft.Dynamics.Integrator.QueryGenerator.AxClient.\<ExportAxPackage\>d__16.MoveNext()
in X:\\bt\\1024532\\repo\\src\\Core\\QueryGenerator\\AxClient.cs:line 265
\--- End of stack trace from previous location where exception was thrown ---
at System.Runtime.ExceptionServices.ExceptionDispatchInfo.Throw()
at System.Runtime.CompilerServices.TaskAwaiter.HandleNonSuccessAndDebuggerNotification(Task task)
at Microsoft.D365.ServicePlatform.Context.ServiceContext.Activity.\<ExecuteAsync\>d__11\`2.MoveNext()
\--- End of stack trace from previous location where exception was thrown ---
```

<span data-ttu-id="508d3-118">如果此错误持续发生，您无法完成初始同步，请按照以下步骤解决问题。</span><span class="sxs-lookup"><span data-stu-id="508d3-118">If this error occurs consistently, and you can't complete the initial synchronization, follow these steps to fix the issue.</span></span>

1. <span data-ttu-id="508d3-119">登录到 Finance and Operations 应用的虚拟机 (VM)。</span><span class="sxs-lookup"><span data-stu-id="508d3-119">Sign in to the virtual machine (VM) for the Finance and Operations app.</span></span>
2. <span data-ttu-id="508d3-120">打开微软管理终端程序。</span><span class="sxs-lookup"><span data-stu-id="508d3-120">Open Microsoft Management Console.</span></span>
3. <span data-ttu-id="508d3-121">在**服务**窗格中，请确保 Microsoft Dynamics 365 数据导入导出框架服务正在运行。</span><span class="sxs-lookup"><span data-stu-id="508d3-121">In the **Services** pane, make sure that the Microsoft Dynamics 365 Data import export framework service is running.</span></span> <span data-ttu-id="508d3-122">如果已停止，请重新启动，因为初始同步需要它。</span><span class="sxs-lookup"><span data-stu-id="508d3-122">Restart it if it has been stopped, because the initial synchronization requires it.</span></span>

## <a name="initial-synchronization-error-403-forbidden"></a><span data-ttu-id="508d3-123">初始同步错误：403 已禁止</span><span class="sxs-lookup"><span data-stu-id="508d3-123">Initial synchronization error: 403 Forbidden</span></span>

<span data-ttu-id="508d3-124">在初始同步期间，您可能会收到以下错误消息：</span><span class="sxs-lookup"><span data-stu-id="508d3-124">You might receive the following error message during initial synchronization:</span></span>

<span data-ttu-id="508d3-125">*（\[已禁止\]，远程服务器返回错误：(403) 已禁止。），AX 导出遇到错误*</span><span class="sxs-lookup"><span data-stu-id="508d3-125">*(\[Forbidden\], The remote server returned an error: (403) Forbidden.), AX export encountered an error*</span></span>

<span data-ttu-id="508d3-126">若要解决此问题，请按照以下步骤操作。</span><span class="sxs-lookup"><span data-stu-id="508d3-126">To fix the issue, follow these steps.</span></span>

1. <span data-ttu-id="508d3-127">登录到 Finance and Operations 应用。</span><span class="sxs-lookup"><span data-stu-id="508d3-127">Sign in to the Finance and Operations app.</span></span>
2. <span data-ttu-id="508d3-128">在 **Azure Active Directory 应用程序**页面上，删除 **DtAppID** 客户端，然后再次添加。</span><span class="sxs-lookup"><span data-stu-id="508d3-128">On the **Azure Active Directory applications** page, delete the **DtAppID** client, and then add it again.</span></span>

![Azure AD 应用程序列表](media/aad_applications.png)

## <a name="self-reference-or-circular-reference-failures-during-initial-synchronization"></a><span data-ttu-id="508d3-130">初始同步期间自引用或循环引用失败</span><span class="sxs-lookup"><span data-stu-id="508d3-130">Self-reference or circular-reference failures during initial synchronization</span></span>

<span data-ttu-id="508d3-131">如果您的任何映射都有自引用或循环引用，您可能会收到错误消息。</span><span class="sxs-lookup"><span data-stu-id="508d3-131">You might receive an error messages if any of your mappings have self-references or circular references.</span></span> <span data-ttu-id="508d3-132">错误分为以下几类：</span><span class="sxs-lookup"><span data-stu-id="508d3-132">The errors fall into these categories:</span></span>

- [<span data-ttu-id="508d3-133">供应商 V2 到 msdyn_vendors 实体映射</span><span class="sxs-lookup"><span data-stu-id="508d3-133">Vendors V2 to msdyn_vendors entity mapping</span></span>](#error-vendor-map)
- [<span data-ttu-id="508d3-134">客户 V3 到客户实体映射</span><span class="sxs-lookup"><span data-stu-id="508d3-134">Customers V3 to Accounts entity mapping</span></span>](#error-customer-map)

## <a name="resolve-an-error-in-vendors-v2-to-msdyn_vendors-entity-mapping"></a><a id="error-vendor-map"></a><span data-ttu-id="508d3-135">解决供应商 V2 到 msdyn_vendors 实体映射中的错误</span><span class="sxs-lookup"><span data-stu-id="508d3-135">Resolve an error in Vendors V2 to msdyn_vendors entity mapping</span></span>

<span data-ttu-id="508d3-136">如果实体具有 **PrimaryContactPersonId** 和 **InvoiceVendorAccountNumber** 字段中有值的现有记录，您可能在**供应商 V2** 到 **msdyn_vendors** 映射上遇到以下初始同步错误。</span><span class="sxs-lookup"><span data-stu-id="508d3-136">You might run into the following initial sync errors on the **Vendors V2** to **msdyn_vendors** mapping if the entities have existing records with values in the **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** fields.</span></span> <span data-ttu-id="508d3-137">这是因为 **InvoiceVendorAccountNumber** 在供应商映射中是一个自引用字段，**PrimaryContactPersonId** 是一个循环引用。</span><span class="sxs-lookup"><span data-stu-id="508d3-137">This because **InvoiceVendorAccountNumber** is a self-referencing field, and **PrimaryContactPersonId** is a circular reference in the vendor mapping.</span></span>

<span data-ttu-id="508d3-138">*无法解析字段的 GUID：<field>。未找到查找值：<value>。请尝试使用此 URL 检查引用数据是否存在：https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>*</span><span class="sxs-lookup"><span data-stu-id="508d3-138">*Couldn't resolve the guid for the field: <field>. The lookup was not found: <value>. Try this URL(s) to check if the reference data exists: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>*</span></span>

<span data-ttu-id="508d3-139">以下是几个示例：</span><span class="sxs-lookup"><span data-stu-id="508d3-139">Here are a couple of examples:</span></span>

- <span data-ttu-id="508d3-140">*无法解析字段的 GUID：msdyn_vendorprimarycontactperson.msdyn_contactpersonid。未找到查找值：000056。请尝试使用此 URL 检查引用数据是否存在：https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'*</span><span class="sxs-lookup"><span data-stu-id="508d3-140">*Couldn't resolve the guid for the field: msdyn_vendorprimarycontactperson.msdyn_contactpersonid. The lookup was not found: 000056. Try this URL(s) to check if the reference data exists: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'*</span></span>
- <span data-ttu-id="508d3-141">*无法解析字段的 GUID：msdyn_invoicevendoraccountnumber.msdyn_vendoraccountnumber。未找到查找值：V24-1。请尝试使用此 URL 检查引用数据是否存在：https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/msdn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber eq 'V24-1'*</span><span class="sxs-lookup"><span data-stu-id="508d3-141">*Couldn't resolve the guid for the field: msdyn_invoicevendoraccountnumber.msdyn_vendoraccountnumber. The lookup was not found: V24-1. Try this URL(s) to check if the reference data exists: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/msdn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber eq 'V24-1'*</span></span>

<span data-ttu-id="508d3-142">如果您有记录在供应商实体中的这些字段中有值，请按照以下一节中的步骤成功完成初始同步。</span><span class="sxs-lookup"><span data-stu-id="508d3-142">If you have records with values in these fields in the vendor entity follow the steps in the below section to complete initial sync successfully.</span></span>

1. <span data-ttu-id="508d3-143">在 Finance and Operations 应用中，从映射中删除 **PrimaryContactPersonId** 和 **InvoiceVendorAccountNumber** 字段，然后保存更改。</span><span class="sxs-lookup"><span data-stu-id="508d3-143">In the Finance and Operations app, delete the **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** fields from the mapping and save the changes.</span></span>

    1. <span data-ttu-id="508d3-144">导航至**供应商 V2 (msdyn_vendors)** 的双写入映射页面，选择**实体映射**选项卡。在左侧的筛选器中，选择 **Finance and Operations apps.Vendors V2**。</span><span class="sxs-lookup"><span data-stu-id="508d3-144">Navigate to the dual-write mapping page for **Vendors V2 (msdyn_vendors)**, and select the **Entity mappings** tab. In the left filter, select **Finance and Operations apps.Vendors V2**.</span></span> <span data-ttu-id="508d3-145">在右侧的筛选器中，选择 **Sales.Vendor**。</span><span class="sxs-lookup"><span data-stu-id="508d3-145">In the right filter, select **Sales.Vendor**.</span></span>

    2. <span data-ttu-id="508d3-146">搜索 **primarycontactperson** 查找源字段 **PrimaryContactPersonId**。</span><span class="sxs-lookup"><span data-stu-id="508d3-146">Search for **primarycontactperson** to find the source field **PrimaryContactPersonId**.</span></span>
    
    3. <span data-ttu-id="508d3-147">单击**操作**按钮，选择**删除**。</span><span class="sxs-lookup"><span data-stu-id="508d3-147">Click the **Actions** button, and select **Delete**.</span></span>
    
        ![自引用或循环引用 3](media/vend_selfref3.png)
    
    4. <span data-ttu-id="508d3-149">重复此步骤删除 **InvoiceVendorAccountNumber** 字段。</span><span class="sxs-lookup"><span data-stu-id="508d3-149">Repeat to delete the **InvoiceVendorAccountNumber** field.</span></span>
    
        ![自引用或循环引用 4](media/vend-selfref4.png)
    
    5. <span data-ttu-id="508d3-151">保存映射更改。</span><span class="sxs-lookup"><span data-stu-id="508d3-151">Save the mapping changes.</span></span>

2. <span data-ttu-id="508d3-152">禁用**供应商 V2** 实体的更改跟踪。</span><span class="sxs-lookup"><span data-stu-id="508d3-152">Disable the change tracking for the **Vendors V2** entity.</span></span>

    1. <span data-ttu-id="508d3-153">导航到**数据管理 \> 数据实体**。</span><span class="sxs-lookup"><span data-stu-id="508d3-153">Navigate to **Data management \> Data Entities**.</span></span>
    
    2. <span data-ttu-id="508d3-154">选择**供应商 V2** 实体。</span><span class="sxs-lookup"><span data-stu-id="508d3-154">Select the **Vendors V2** entity.</span></span>
    
    3. <span data-ttu-id="508d3-155">单击菜单栏中的**选项**，然后单击**更改跟踪**。</span><span class="sxs-lookup"><span data-stu-id="508d3-155">Click **Options** from the menu bar, and then **Change tracking**.</span></span>
    
        ![自引用或循环引用 5](media/selfref_options.png)
    
    4. <span data-ttu-id="508d3-157">单击**禁用更改跟踪**。</span><span class="sxs-lookup"><span data-stu-id="508d3-157">Click **Disable Change Tracking**.</span></span>
    
        ![自引用或循环引用 6](media/selfref_tracking.png)

3. <span data-ttu-id="508d3-159">运行**供应商 V2 (msdyn_vendors)** 映射的初始同步。</span><span class="sxs-lookup"><span data-stu-id="508d3-159">Run the initial sync of **Vendors V2 (msdyn_vendors)** mapping.</span></span> <span data-ttu-id="508d3-160">初始同步应会成功运行，没有任何错误。</span><span class="sxs-lookup"><span data-stu-id="508d3-160">The initial sync should run successfully without any errors.</span></span>

4. <span data-ttu-id="508d3-161">运行 **CDS 联系人 V2 (contacts)** 映射的初始同步。</span><span class="sxs-lookup"><span data-stu-id="508d3-161">Run the initial sync for the **CDS Contacts V2 (contacts)** mapping.</span></span> <span data-ttu-id="508d3-162">如果要同步供应商实体上的主要联系人字段，则必须同步此映射，因为联系人记录也需要进行初始同步。</span><span class="sxs-lookup"><span data-stu-id="508d3-162">You must sync this mapping if you want to sync primary contact field on vendors entity as the contacts records also need to be initial synced.</span></span>

5. <span data-ttu-id="508d3-163">将字段 **PrimaryContactPersonId** 和 **InvoiceVendorAccountNumber** 重新添加到**供应商 V2 (msdyn_vendors)** 映射，然后保存映射。</span><span class="sxs-lookup"><span data-stu-id="508d3-163">Add the fields **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** back to the **Vendors V2 (msdyn_vendors)** mapping and save the mapping.</span></span>

6. <span data-ttu-id="508d3-164">再次运行**供应商 V2 (msdyn_vendors)** 映射的初始同步。</span><span class="sxs-lookup"><span data-stu-id="508d3-164">Run the initial sync again for the **Vendors V2 (msdyn_vendors)** mapping.</span></span> <span data-ttu-id="508d3-165">所有记录都将同步，因为更改跟踪已禁用。</span><span class="sxs-lookup"><span data-stu-id="508d3-165">All the records will be synced, because change tracking is disabled.</span></span>

7. <span data-ttu-id="508d3-166">启用**供应商 V2** 实体的更改跟踪。</span><span class="sxs-lookup"><span data-stu-id="508d3-166">Enable change tracking for the **Vendors V2** entity.</span></span>

## <a name="resolve-an-error-in-customers-v3-to-accounts-entity-mapping"></a><a id="error-customer-map"></a><span data-ttu-id="508d3-167">解决客户 V3 到客户实体映射中的错误</span><span class="sxs-lookup"><span data-stu-id="508d3-167">Resolve an error in Customers V3 to Accounts entity mapping</span></span>

<span data-ttu-id="508d3-168">如果实体具有 **ContactPersonID** 和 **InvoiceAccount** 字段中有值的现有记录，您可能在**客户 V3** 到**客户**映射上遇到以下初始同步错误。</span><span class="sxs-lookup"><span data-stu-id="508d3-168">You might run into the following initial sync errors on the **Customers V3** to **Accounts** mapping if the entities have existing records with values in the **ContactPersonID** and **InvoiceAccount** fields.</span></span> <span data-ttu-id="508d3-169">这是因为 **InvoiceAccount** 在供应商映射中是一个自引用字段，**ContactPersonID** 是一个循环引用。</span><span class="sxs-lookup"><span data-stu-id="508d3-169">This because **InvoiceAccount** is a self-referencing field, and **ContactPersonID** is a circular reference in the vendor mapping.</span></span>

<span data-ttu-id="508d3-170">*无法解析字段的 GUID：<field>。未找到查找值：<value>。请尝试使用此 URL 检查引用数据是否存在：https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>*</span><span class="sxs-lookup"><span data-stu-id="508d3-170">*Couldn't resolve the guid for the field: <field>. The lookup was not found: <value>. Try this URL(s) to check if the reference data exists: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>*</span></span>

- <span data-ttu-id="508d3-171">*无法解析字段的 GUID：primarycontactid.msdyn_contactpersonid。未找到查找值：000056。请尝试使用此 URL 检查引用数据是否存在：https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'*</span><span class="sxs-lookup"><span data-stu-id="508d3-171">*Couldn't resolve the guid for the field: primarycontactid.msdyn_contactpersonid. The lookup was not found: 000056. Try this URL(s) to check if the reference data exists: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'*</span></span>
- <span data-ttu-id="508d3-172">*无法解析字段的 GUID：msdyn_billingaccount.accountnumber。未找到查找值：1206-1。请尝试使用此 URL 检查引用数据是否存在：https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/accounts?$select=accountnumber.account&$filter=accountnumber eq '1206-1'*</span><span class="sxs-lookup"><span data-stu-id="508d3-172">*Couldn't resolve the guid for the field: msdyn_billingaccount.accountnumber. The lookup was not found: 1206-1. Try this URL(s) to check if the reference data exists: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/accounts?$select=accountnumber.account&$filter=accountnumber eq '1206-1'*</span></span>

<span data-ttu-id="508d3-173">如果您有记录在客户实体中的这些字段中有值，请按照以下一节中的步骤成功完成初始同步。</span><span class="sxs-lookup"><span data-stu-id="508d3-173">If you have records with values in these fields in the customer entity follow the steps in the below section to complete initial sync successfully.</span></span> <span data-ttu-id="508d3-174">您可以对任何现成的实体（如客户和联系人）使用此方法。</span><span class="sxs-lookup"><span data-stu-id="508d3-174">You can use this approach for any out-of-the-box entities such Accounts and Contacts.</span></span>

1. <span data-ttu-id="508d3-175">在 Finance and Operations 应用中，从**客户 V3 (accounts)** 映射中删除字段 **ContactPersonID** 和 **InvoiceAccount**，然后保存映射。</span><span class="sxs-lookup"><span data-stu-id="508d3-175">In the Finance and Operations app, delete the fields **ContactPersonID** and **InvoiceAccount** from the **Customers V3 (accounts)** mapping and save the mapping.</span></span>

    1. <span data-ttu-id="508d3-176">导航至**客户 V3 (accounts)** 的双写入映射页面，选择**实体映射**选项卡。在左侧的筛选器中，选择 **Finance and Operations app.Customers V3**。</span><span class="sxs-lookup"><span data-stu-id="508d3-176">Navigate to the dual-write mapping page for **Customers V3 (accounts)**, select the **Entity mappings** tab. In the left filter, select **Finance and Operations app.Customers V3**.</span></span> <span data-ttu-id="508d3-177">在右侧的筛选器中，选择 **Common Data Service.Account**。</span><span class="sxs-lookup"><span data-stu-id="508d3-177">In the right filter, select **Common Data Service.Account**.</span></span>

    2. <span data-ttu-id="508d3-178">搜索 **contactperson** 查找源字段 **ContactPersonID**。</span><span class="sxs-lookup"><span data-stu-id="508d3-178">Search for **contactperson** to find the source field **ContactPersonID**.</span></span>
    
    3. <span data-ttu-id="508d3-179">单击**操作**按钮，选择**删除**。</span><span class="sxs-lookup"><span data-stu-id="508d3-179">Click the **Actions** button, and select **Delete**.</span></span>
    
        ![自引用或循环引用 3](media/cust_selfref3.png)
    
    4. <span data-ttu-id="508d3-181">重复此步骤删除 **InvoiceAccount** 字段。</span><span class="sxs-lookup"><span data-stu-id="508d3-181">Repeat to delete the **InvoiceAccount** field.</span></span>
    
        ![自引用或循环引用](media/cust_selfref4.png)
    
    5. <span data-ttu-id="508d3-183">保存映射更改。</span><span class="sxs-lookup"><span data-stu-id="508d3-183">Save the mapping changes.</span></span>

2. <span data-ttu-id="508d3-184">禁用**客户 V3** 实体的更改跟踪。</span><span class="sxs-lookup"><span data-stu-id="508d3-184">Disable the change tracking for the **Customers V3** entity.</span></span>

    1. <span data-ttu-id="508d3-185">导航到**数据管理 \> 数据实体**。</span><span class="sxs-lookup"><span data-stu-id="508d3-185">Navigate to **Data management \> Data Entities**.</span></span>
    
    2. <span data-ttu-id="508d3-186">选择**客户 V3** 实体。</span><span class="sxs-lookup"><span data-stu-id="508d3-186">Select the **Customers V3** entity.</span></span>
    
    3. <span data-ttu-id="508d3-187">单击菜单栏中的**选项**，然后单击**更改跟踪**。</span><span class="sxs-lookup"><span data-stu-id="508d3-187">Click **Options** from the menu bar, and then **Change tracking**.</span></span>
    
        ![自引用或循环引用 5](media/selfref_options.png)
    
    4. <span data-ttu-id="508d3-189">单击**禁用更改跟踪**。</span><span class="sxs-lookup"><span data-stu-id="508d3-189">Click **Disable Change Tracking**.</span></span>
    
        ![自引用或循环引用 6](media/selfref_tracking.png)

3. <span data-ttu-id="508d3-191">运行**客户 V3 (Accounts)** 映射的初始同步。</span><span class="sxs-lookup"><span data-stu-id="508d3-191">Run the initial sync for the **Customers V3 (Accounts)** mapping.</span></span> <span data-ttu-id="508d3-192">初始同步应会成功运行，没有任何错误。</span><span class="sxs-lookup"><span data-stu-id="508d3-192">The initial sync should run successfully without any errors.</span></span>

4. <span data-ttu-id="508d3-193">运行 **CDS 联系人 V2 (contacts)** 映射的初始同步。</span><span class="sxs-lookup"><span data-stu-id="508d3-193">Run the initial sync for the **CDS Contacts V2 (contacts)** mapping.</span></span> <span data-ttu-id="508d3-194">有 2 个名称相同的映射。</span><span class="sxs-lookup"><span data-stu-id="508d3-194">There are 2 maps with the same name.</span></span> <span data-ttu-id="508d3-195">选择描述为**用于在 FO.CDS 供应商联系人 V2 与 CDS.Contacts 之间同步的双写入模板。需要新包 \[Dynamics365SupplyChainExtended\]。** 的那个。</span><span class="sxs-lookup"><span data-stu-id="508d3-195">Select the one with the description **Dual-write template for sync between FO.CDS Vendor Contacts V2 to CDS.Contacts. Requires new package \[Dynamics365SupplyChainExtended\].**</span></span> <span data-ttu-id="508d3-196">在映射的**详细信息**选项卡上。</span><span class="sxs-lookup"><span data-stu-id="508d3-196">on the **Details** tab of the map.</span></span>

5. <span data-ttu-id="508d3-197">将字段 **InvoiceAccount** 和 **ContactPersonId** 重新添加到**客户 V3 (Accounts)** 映射，然后保存映射。</span><span class="sxs-lookup"><span data-stu-id="508d3-197">Add the fields **InvoiceAccount** and **ContactPersonId** back to the **Customers V3 (Accounts)** mapping and save the mapping.</span></span> <span data-ttu-id="508d3-198">现在，**InvoiceAccount** 字段和 **ContactPersonId** 字段又成为了实时同步模式的一部分。</span><span class="sxs-lookup"><span data-stu-id="508d3-198">Now, both the **InvoiceAccount** field and the **ContactPersonId** field are again part of live sync mode.</span></span> <span data-ttu-id="508d3-199">在下一步中，您将完成这些字段的初始同步。</span><span class="sxs-lookup"><span data-stu-id="508d3-199">In the next step, you complete the initial sync for these fields.</span></span>

6. <span data-ttu-id="508d3-200">再次运行**客户 V3 (Accounts)** 映射的初始同步。</span><span class="sxs-lookup"><span data-stu-id="508d3-200">Run the initial sync again for the **Customers V3 (Accounts)** mapping.</span></span> <span data-ttu-id="508d3-201">由于更改跟踪已禁用，因此运行同步会将 Finance and Operations 应用中 **InvoiceAccount** 和 **ContactPersonId** 的数据同步到 Common Data Service。</span><span class="sxs-lookup"><span data-stu-id="508d3-201">Because change tracking is disabled, running the sync will sync the data for **InvoiceAccount** and **ContactPersonId** from the Finance and Operations app to Common Data Service.</span></span>

7. <span data-ttu-id="508d3-202">要将 **InvoiceAccount** 和 **ContactPersonId** 的数据从 Common Data Service 同步到 Finance and Operations，将使用数据集成项目。</span><span class="sxs-lookup"><span data-stu-id="508d3-202">To sync the data for **InvoiceAccount** and **ContactPersonId** from Common Data Service to the Finance and Operations, you use a data integration project.</span></span>

    1. <span data-ttu-id="508d3-203">在 Power Apps 中，在 **Sales.Account** 和 **Finance and Operations apps.Customers V3** 实体之间创建数据集成项目。</span><span class="sxs-lookup"><span data-stu-id="508d3-203">In Power Apps, create a data integration project between the **Sales.Account** and **Finance and Operations apps.Customers V3** entities.</span></span> <span data-ttu-id="508d3-204">数据方向必须是从 Common Data Service 到 Finance and Operations 应用。</span><span class="sxs-lookup"><span data-stu-id="508d3-204">The data direction must be from Common Data Service to the Finance and Operations app.</span></span>  <span data-ttu-id="508d3-205">因为 **InvoiceAccount** 是使用双写入的新属性，您可能需要跳过此属性的初始同步。</span><span class="sxs-lookup"><span data-stu-id="508d3-205">Because **InvoiceAccount** is a new attribute in dual-write, you may want to skip initial sync for this attribute.</span></span> <span data-ttu-id="508d3-206">有关详细信息，请参阅[将数据集成到 Common Data Service](https://docs.microsoft.com/power-platform/admin/data-integrator)。</span><span class="sxs-lookup"><span data-stu-id="508d3-206">For more information, see [Integrate data into Common Data Service](https://docs.microsoft.com/power-platform/admin/data-integrator).</span></span>

        <span data-ttu-id="508d3-207">下图显示了一个更新 **CustomerAccount** 和 **ContactPersonId** 的项目。</span><span class="sxs-lookup"><span data-stu-id="508d3-207">The following image shows a project that updates **CustomerAccount** and **ContactPersonId**.</span></span>

        ![自引用或循环引用](media/cust_selfref6.png)

    2. <span data-ttu-id="508d3-209">将公司条件添加到 Common Data Service 一端的筛选器中，因为只有与筛选条件匹配的记录会在 Finance and Operations 应用中更新。</span><span class="sxs-lookup"><span data-stu-id="508d3-209">Add the company criteria in the filter on Common Data Service side, because only the records that match filter criteria will be updated in the Finance and Operations app.</span></span> <span data-ttu-id="508d3-210">要添加筛选器，请单击筛选器图标。</span><span class="sxs-lookup"><span data-stu-id="508d3-210">To add a filter, click the filter icon.</span></span> <span data-ttu-id="508d3-211">在**编辑查询**对话框中，您可以添加像 **_msdyn_company_value eq '\<guid\>'** 这样的筛选器查询。</span><span class="sxs-lookup"><span data-stu-id="508d3-211">In the **Edit query** dialog, you can add a filter query like **_msdyn_company_value eq '\<guid\>'**.</span></span> <span data-ttu-id="508d3-212">如果筛选器图标未出现，请创建支持票证，让数据集成团队在您的租户上启用筛选器功能。</span><span class="sxs-lookup"><span data-stu-id="508d3-212">If the filter icon is not present, create a support ticket to ask the data integration team to enable the filter capability on your tenant.</span></span> <span data-ttu-id="508d3-213">如果您没有为 **_msdyn_company_value** 输入筛选器查询，那么所有记录都将同步。</span><span class="sxs-lookup"><span data-stu-id="508d3-213">If you do not enter a filter query for **_msdyn_company_value**, then all the records are synced.</span></span>

        ![自引用或循环引用](media/cust_selfref7.png)

        <span data-ttu-id="508d3-215">这将完成记录的初始同步。</span><span class="sxs-lookup"><span data-stu-id="508d3-215">This completes the initial sync of the records.</span></span>

8. <span data-ttu-id="508d3-216">在 Finance and Operations 应用中为**客户 V3** 实体启用更改跟踪。</span><span class="sxs-lookup"><span data-stu-id="508d3-216">Enable change tracking for the **Customers V3** entity in the Finance and Operations app.</span></span>

