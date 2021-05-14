---
title: 解决初始同步过程中的问题
description: 本主题提供故障排除信息，可以帮助您解决初始同步期间可能发生的问题。
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 709a3c332bb6d086910b257fee9cdec8d2bc81a2
ms.sourcegitcommit: a202bf67c3c2c054e2a47cb7b3145cb7c0ee635e
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/25/2021
ms.locfileid: "5941047"
---
# <a name="troubleshoot-issues-during-initial-synchronization"></a><span data-ttu-id="58f20-103">解决初始同步过程中的问题</span><span class="sxs-lookup"><span data-stu-id="58f20-103">Troubleshoot issues during initial synchronization</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="58f20-104">本主题提供 Finance and Operations 应用与 Dataverse 之间的双写入集成的故障排除信息。</span><span class="sxs-lookup"><span data-stu-id="58f20-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Dataverse.</span></span> <span data-ttu-id="58f20-105">具体来说，提供可以帮助您解决初始同步期间可能发生的问题的信息。</span><span class="sxs-lookup"><span data-stu-id="58f20-105">Specifically, it provides information that can help you fix issues that might occur during initial synchronization.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="58f20-106">本主题解决的某些问题可能需要系统管理员角色或 Microsoft Azure Active Directory (Azure AD) 租户管理员凭据。</span><span class="sxs-lookup"><span data-stu-id="58f20-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="58f20-107">介绍每个问题的每一节说明了是否需要特定角色或凭据。</span><span class="sxs-lookup"><span data-stu-id="58f20-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="check-for-initial-synchronization-errors-in-a-finance-and-operations-app"></a><span data-ttu-id="58f20-108">在 Finance and Operations 应用中检查初始同步错误</span><span class="sxs-lookup"><span data-stu-id="58f20-108">Check for initial synchronization errors in a Finance and Operations app</span></span>

<span data-ttu-id="58f20-109">启用映射模板后，映射的状态应为 **正在运行**。</span><span class="sxs-lookup"><span data-stu-id="58f20-109">After you enable the mapping templates, the status of the maps should be **Running**.</span></span> <span data-ttu-id="58f20-110">如果状态为 **未运行**，在初始同步期间将发生错误。</span><span class="sxs-lookup"><span data-stu-id="58f20-110">If the status is **Not running**, errors occurred during initial synchronization.</span></span> <span data-ttu-id="58f20-111">要查看错误，请选择 **双写入** 页面上的 **初始同步详细信息** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="58f20-111">To view the errors, select the **Initial sync details** tab on the **Dual-write** page.</span></span>

![初始同步详细信息选项卡上的错误](media/initial_sync_status.png)

## <a name="you-cant-complete-initial-synchronization-400-bad-request"></a><span data-ttu-id="58f20-113">您无法完成初始同步：400 错误请求</span><span class="sxs-lookup"><span data-stu-id="58f20-113">You can't complete initial synchronization: 400 Bad Request</span></span>

<span data-ttu-id="58f20-114">**解决此问题所需的角色：** 系统管理员</span><span class="sxs-lookup"><span data-stu-id="58f20-114">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="58f20-115">当您尝试运行映射和初始同步时，您可能会收到以下错误消息：</span><span class="sxs-lookup"><span data-stu-id="58f20-115">You might receive the following error message when you try to run the mapping and initial synchronization:</span></span>

<span data-ttu-id="58f20-116">*（\[错误请求\]，远程服务器返回错误：(400) 错误请求。），AX 导出遇到错误*</span><span class="sxs-lookup"><span data-stu-id="58f20-116">*(\[Bad Request\], The remote server returned an error: (400) Bad Request.), AX export encountered an error*</span></span>

<span data-ttu-id="58f20-117">以下是完整错误消息的示例。</span><span class="sxs-lookup"><span data-stu-id="58f20-117">Here is an example of the full error message.</span></span>

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

<span data-ttu-id="58f20-118">如果此错误持续发生，您无法完成初始同步，请按照以下步骤解决问题。</span><span class="sxs-lookup"><span data-stu-id="58f20-118">If this error occurs consistently, and you can't complete the initial synchronization, follow these steps to fix the issue.</span></span>

1. <span data-ttu-id="58f20-119">登录到 Finance and Operations 应用的虚拟机 (VM)。</span><span class="sxs-lookup"><span data-stu-id="58f20-119">Sign in to the virtual machine (VM) for the Finance and Operations app.</span></span>
2. <span data-ttu-id="58f20-120">打开微软管理终端程序。</span><span class="sxs-lookup"><span data-stu-id="58f20-120">Open Microsoft Management Console.</span></span>
3. <span data-ttu-id="58f20-121">在 **服务** 窗格中，请确保 Microsoft Dynamics 365 数据导入导出框架服务正在运行。</span><span class="sxs-lookup"><span data-stu-id="58f20-121">In the **Services** pane, make sure that the Microsoft Dynamics 365 Data import export framework service is running.</span></span> <span data-ttu-id="58f20-122">如果已停止，请重新启动，因为初始同步需要它。</span><span class="sxs-lookup"><span data-stu-id="58f20-122">Restart it if it has been stopped, because the initial synchronization requires it.</span></span>

## <a name="initial-synchronization-error-403-forbidden"></a><span data-ttu-id="58f20-123">初始同步错误：403 已禁止</span><span class="sxs-lookup"><span data-stu-id="58f20-123">Initial synchronization error: 403 Forbidden</span></span>

<span data-ttu-id="58f20-124">在初始同步期间，您可能会收到以下错误消息：</span><span class="sxs-lookup"><span data-stu-id="58f20-124">You might receive the following error message during initial synchronization:</span></span>

<span data-ttu-id="58f20-125">*（\[已禁止\]，远程服务器返回错误：(403) 已禁止。），AX 导出遇到错误*</span><span class="sxs-lookup"><span data-stu-id="58f20-125">*(\[Forbidden\], The remote server returned an error: (403) Forbidden.), AX export encountered an error*</span></span>

<span data-ttu-id="58f20-126">若要解决此问题，请按照以下步骤操作。</span><span class="sxs-lookup"><span data-stu-id="58f20-126">To fix the issue, follow these steps.</span></span>

1. <span data-ttu-id="58f20-127">登录到 Finance and Operations 应用。</span><span class="sxs-lookup"><span data-stu-id="58f20-127">Sign in to the Finance and Operations app.</span></span>
2. <span data-ttu-id="58f20-128">在 **Azure Active Directory 应用程序** 页面上，删除 **DtAppID** 客户端，然后再次添加。</span><span class="sxs-lookup"><span data-stu-id="58f20-128">On the **Azure Active Directory applications** page, delete the **DtAppID** client, and then add it again.</span></span>

![Azure AD 应用程序列表中的 DtAppID 客户端](media/aad_applications.png)

## <a name="self-reference-or-circular-reference-failures-during-initial-synchronization"></a><span data-ttu-id="58f20-130">初始同步期间自引用或循环引用失败</span><span class="sxs-lookup"><span data-stu-id="58f20-130">Self-reference or circular reference failures during initial synchronization</span></span>

<span data-ttu-id="58f20-131">如果您的任何映射都有自引用或循环引用，您可能会收到错误消息。</span><span class="sxs-lookup"><span data-stu-id="58f20-131">You might receive an error messages if any of your mappings have self-references or circular references.</span></span> <span data-ttu-id="58f20-132">错误分为以下几类：</span><span class="sxs-lookup"><span data-stu-id="58f20-132">The errors fall into these categories:</span></span>

- [<span data-ttu-id="58f20-133">供应商 V2–to–msdyn_vendors 表映射中的错误</span><span class="sxs-lookup"><span data-stu-id="58f20-133">Errors in the Vendors V2–to–msdyn_vendors table mapping</span></span>](#error-vendor-map)
- [<span data-ttu-id="58f20-134">客户 V3–to–Accounts 表映射中的错误</span><span class="sxs-lookup"><span data-stu-id="58f20-134">Errors in the Customers V3–to–Accounts table mapping</span></span>](#error-customer-map)

## <a name="resolve-errors-in-the-vendors-v2tomsdyn_vendors-table-mapping"></a><a id="error-vendor-map"></a><span data-ttu-id="58f20-135">解决供应商 V2–to–msdyn_vendors 表映射中的错误</span><span class="sxs-lookup"><span data-stu-id="58f20-135">Resolve errors in the Vendors V2–to–msdyn_vendors table mapping</span></span>

<span data-ttu-id="58f20-136">如果表具有在 **PrimaryContactPersonId** 和 **InvoiceVendorAccountNumber** 列中存在值的现有行，在将 **供应商 V2** 映射到 **msdyn\_vendors** 时，您可能会遇到初始同步错误。</span><span class="sxs-lookup"><span data-stu-id="58f20-136">You might encounter initial synchronization errors for the mapping of **Vendors V2** to **msdyn\_vendors** if the tables have existing rows where there are values in the **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** columns.</span></span> <span data-ttu-id="58f20-137">发生这些错误是因为 **InvoiceVendorAccountNumber** 在供应商映射中是一个自引用列，**PrimaryContactPersonId** 是一个循环引用。</span><span class="sxs-lookup"><span data-stu-id="58f20-137">These errors occur because **InvoiceVendorAccountNumber** is a self-referencing column, and **PrimaryContactPersonId** is a circular reference in the vendor mapping.</span></span>

<span data-ttu-id="58f20-138">您收到的错误消息将为以下形式。</span><span class="sxs-lookup"><span data-stu-id="58f20-138">The error messages that you receive will have the following form.</span></span>

<span data-ttu-id="58f20-139">*无法解析字段的 GUID：\<field\>。未找到查找值：\<value\>。请尝试使用此 URL 检查引用数据是否存在：`https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>`*</span><span class="sxs-lookup"><span data-stu-id="58f20-139">*Couldn't resolve the guid for the field: \<field\>. The lookup was not found: \<value\>. Try this URL(s) to check if the reference data exists: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>`*</span></span>

<span data-ttu-id="58f20-140">下面举了一些示例加以说明：</span><span class="sxs-lookup"><span data-stu-id="58f20-140">Here are some examples:</span></span>

- <span data-ttu-id="58f20-141">*无法解析字段的 GUID：msdyn\_vendorprimarycontactperson.msdyn\_contactpersonid。未找到查找值：000056。请尝试使用此 URL 检查引用数据是否存在：`https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'`*</span><span class="sxs-lookup"><span data-stu-id="58f20-141">*Couldn't resolve the guid for the field: msdyn\_vendorprimarycontactperson.msdyn\_contactpersonid. The lookup was not found: 000056. Try this URL(s) to check if the reference data exists: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'`*</span></span>
- <span data-ttu-id="58f20-142">*无法解析字段的 GUID：msdyn\_invoicevendoraccountnumber.msdyn\_vendoraccountnumber。未找到查找值：V24-1。请尝试使用此 URL 检查引用数据是否存在：`https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/msdn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber eq 'V24-1'`*</span><span class="sxs-lookup"><span data-stu-id="58f20-142">*Couldn't resolve the guid for the field: msdyn\_invoicevendoraccountnumber.msdyn\_vendoraccountnumber. The lookup was not found: V24-1. Try this URL(s) to check if the reference data exists: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/msdn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber eq 'V24-1'`*</span></span>

<span data-ttu-id="58f20-143">如果供应商表中的任何行在 **PrimaryContactPersonId** 和 **InvoiceVendorAccountNumber** 列中都具有值，请按照以下步骤完成初始同步。</span><span class="sxs-lookup"><span data-stu-id="58f20-143">If any rows in the vendor table have values in the **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** columns, follow these steps to complete the initial synchronization.</span></span>

1. <span data-ttu-id="58f20-144">在 Finance and Operations 应用中，从映射中删除 **PrimaryContactPersonId** 和 **InvoiceVendorAccountNumber** 列，然后保存映射。</span><span class="sxs-lookup"><span data-stu-id="58f20-144">In the Finance and Operations app, delete the **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** columns from the mapping, and then save the mapping.</span></span>

    1. <span data-ttu-id="58f20-145">在 **供应商 V2 (msdyn\_vendors)** 的双写入映射页面上，在 **表映射** 选项卡上，在左侧的筛选器中，选择 **Finance and Operations apps.Vendors V2**。</span><span class="sxs-lookup"><span data-stu-id="58f20-145">On the dual-write mapping page for **Vendors V2 (msdyn\_vendors)**, on the **Table mappings** tab, in the left filter, select **Finance and Operations apps.Vendors V2**.</span></span> <span data-ttu-id="58f20-146">在右侧的筛选器中，选择 **Sales.Vendor**。</span><span class="sxs-lookup"><span data-stu-id="58f20-146">In the right filter, select **Sales.Vendor**.</span></span>
    2. <span data-ttu-id="58f20-147">搜索 **primarycontactperson** 查找 **PrimaryContactPersonId** 源列。</span><span class="sxs-lookup"><span data-stu-id="58f20-147">Search for **primarycontactperson** to find the **PrimaryContactPersonId** source column.</span></span>
    3. <span data-ttu-id="58f20-148">选择 **操作**，然后选择 **删除**。</span><span class="sxs-lookup"><span data-stu-id="58f20-148">Select **Actions**, and then select **Delete**.</span></span>

        ![删除 PrimaryContactPersonId 列](media/vend_selfref3.png)

    4. <span data-ttu-id="58f20-150">重复这些步骤删除 **InvoiceVendorAccountNumber** 列。</span><span class="sxs-lookup"><span data-stu-id="58f20-150">Repeat these steps to delete the **InvoiceVendorAccountNumber** column.</span></span>

        ![删除 InvoiceVendorAccountNumber 列](media/vend-selfref4.png)

    5. <span data-ttu-id="58f20-152">将更改保存到映射。</span><span class="sxs-lookup"><span data-stu-id="58f20-152">Save your changes to the mapping.</span></span>

2. <span data-ttu-id="58f20-153">关闭 **供应商 V2** 表的更改跟踪。</span><span class="sxs-lookup"><span data-stu-id="58f20-153">Turn off change tracking for the **Vendors V2** table.</span></span>

    1. <span data-ttu-id="58f20-154">在 **数据管理** 工作区中，选择 **数据表** 磁贴。</span><span class="sxs-lookup"><span data-stu-id="58f20-154">In the **Data management** workspace, select the **Data tables** tile.</span></span>
    2. <span data-ttu-id="58f20-155">选择 **供应商 V2** 表。</span><span class="sxs-lookup"><span data-stu-id="58f20-155">Select the **Vendors V2** table.</span></span>
    3. <span data-ttu-id="58f20-156">在操作窗格上，选择 **选项**，然后选择 **更改跟踪**。</span><span class="sxs-lookup"><span data-stu-id="58f20-156">On the Action Pane, select **Options**, and then select **Change tracking**.</span></span>

        ![选择更改跟踪选项](media/selfref_options.png)

    4. <span data-ttu-id="58f20-158">选择 **禁用更改跟踪**。</span><span class="sxs-lookup"><span data-stu-id="58f20-158">Select **Disable Change Tracking**.</span></span>

        ![选择“禁用更改跟踪”](media/selfref_tracking.png)

3. <span data-ttu-id="58f20-160">运行 **供应商 V2 (msdyn\_vendors)** 映射的初始同步。</span><span class="sxs-lookup"><span data-stu-id="58f20-160">Run initial synchronization for the **Vendors V2 (msdyn\_vendors)** mapping.</span></span> <span data-ttu-id="58f20-161">初始同步应会成功运行，没有任何错误。</span><span class="sxs-lookup"><span data-stu-id="58f20-161">The initial synchronization should run successfully, without any errors.</span></span>
4. <span data-ttu-id="58f20-162">运行 **CDS 联系人 V2 (contacts)** 映射的初始同步。</span><span class="sxs-lookup"><span data-stu-id="58f20-162">Run initial synchronization for the **CDS Contacts V2 (contacts)** mapping.</span></span> <span data-ttu-id="58f20-163">如果要同步供应商表上的主要联系人列，则必须同步此映射，因为还必须对联系人行进行初始同步。</span><span class="sxs-lookup"><span data-stu-id="58f20-163">You must sync this mapping if you want to sync the primary contact column on the vendors table, because initial synchronization must also be done for the contact rows.</span></span>
5. <span data-ttu-id="58f20-164">将 **PrimaryContactPersonId** 和 **InvoiceVendorAccountNumber** 列重新添加到 **供应商 V2 (msdyn\_vendors)** 映射，然后保存映射。</span><span class="sxs-lookup"><span data-stu-id="58f20-164">Add the **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** columns back to the **Vendors V2 (msdyn\_vendors)** mapping, and then save the mapping.</span></span>
6. <span data-ttu-id="58f20-165">再次运行 **供应商 V2 (msdyn\_vendors)** 映射的初始同步。</span><span class="sxs-lookup"><span data-stu-id="58f20-165">Run initial synchronization again for the **Vendors V2 (msdyn\_vendors)** mapping.</span></span> <span data-ttu-id="58f20-166">由于更改跟踪已关闭，所有行都将同步。</span><span class="sxs-lookup"><span data-stu-id="58f20-166">Because change tracking is turned off, all the rows will be synced.</span></span>
7. <span data-ttu-id="58f20-167">重新打开 **供应商 V2** 表的更改跟踪。</span><span class="sxs-lookup"><span data-stu-id="58f20-167">Turn change tracking back on for the **Vendors V2** table.</span></span>

## <a name="resolve-errors-in-the-customers-v3toaccounts-table-mapping"></a><a id="error-customer-map"></a><span data-ttu-id="58f20-168">解决客户 V3–to–Accounts 表映射中的错误</span><span class="sxs-lookup"><span data-stu-id="58f20-168">Resolve errors in the Customers V3–to–Accounts table mapping</span></span>

<span data-ttu-id="58f20-169">如果表具有在 **ContactPersonID** 和 **InvoiceAccount** 列中存在值的现有行，在将 **客户 V3** 映射到 **客户** 时，您可能会遇到初始同步错误。</span><span class="sxs-lookup"><span data-stu-id="58f20-169">You might encounter initial synchronization errors for the mapping of **Customers V3** to **Accounts** if the tables have existing rows where there are values in the **ContactPersonID** and **InvoiceAccount** columns.</span></span> <span data-ttu-id="58f20-170">发生这些错误是因为 **InvoiceAccount** 在供应商映射中是一个自引用列，**ContactPersonID** 是一个循环引用。</span><span class="sxs-lookup"><span data-stu-id="58f20-170">These errors occur because **InvoiceAccount** is a self-referencing column, and **ContactPersonID** is a circular reference in the vendor mapping.</span></span>

<span data-ttu-id="58f20-171">您收到的错误消息将为以下形式。</span><span class="sxs-lookup"><span data-stu-id="58f20-171">The error messages that you receive will have the following form.</span></span>

<span data-ttu-id="58f20-172">*无法解析字段的 GUID：\<field\>。未找到查找值：\<value\>。请尝试使用此 URL 检查引用数据是否存在：`https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>`*</span><span class="sxs-lookup"><span data-stu-id="58f20-172">*Couldn't resolve the guid for the field: \<field\>. The lookup was not found: \<value\>. Try this URL(s) to check if the reference data exists: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>`*</span></span>

<span data-ttu-id="58f20-173">下面举了一些示例加以说明：</span><span class="sxs-lookup"><span data-stu-id="58f20-173">Here are some examples:</span></span>

- <span data-ttu-id="58f20-174">*无法解析字段的 GUID：primarycontactid.msdyn\_contactpersonid。未找到查找值：000056。请尝试使用此 URL 检查引用数据是否存在：`https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'`*</span><span class="sxs-lookup"><span data-stu-id="58f20-174">*Couldn't resolve the guid for the field: primarycontactid.msdyn\_contactpersonid. The lookup was not found: 000056. Try this URL(s) to check if the reference data exists: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'`*</span></span>
- <span data-ttu-id="58f20-175">*无法解析字段的 GUID：msdyn\_billingaccount.accountnumber。未找到查找值：1206-1。请尝试使用此 URL 检查引用数据是否存在：`https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/accounts?$select=accountnumber.account&$filter=accountnumber eq '1206-1'`*</span><span class="sxs-lookup"><span data-stu-id="58f20-175">*Couldn't resolve the guid for the field: msdyn\_billingaccount.accountnumber. The lookup was not found: 1206-1. Try this URL(s) to check if the reference data exists: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/accounts?$select=accountnumber.account&$filter=accountnumber eq '1206-1'`*</span></span>

<span data-ttu-id="58f20-176">如果客户表中的任何行在 **ContactPersonID** 和 **InvoiceAccount** 列中都具有值，请按照以下步骤完成初始同步。</span><span class="sxs-lookup"><span data-stu-id="58f20-176">If any rows in the customer table have values in the **ContactPersonID** and **InvoiceAccount** columns, follow these steps to complete the initial synchronization.</span></span> <span data-ttu-id="58f20-177">您可以对任何现成的表（如 **客户** 和 **联系人**）使用此方法。</span><span class="sxs-lookup"><span data-stu-id="58f20-177">You can use this approach for any out-of-box tables, such **Accounts** and **Contacts**.</span></span>

1. <span data-ttu-id="58f20-178">在 Finance and Operations 应用中，从 **客户 V3 (accounts)** 映射中删除 **ContactPersonID** 和 **InvoiceAccount** 列，然后保存映射。</span><span class="sxs-lookup"><span data-stu-id="58f20-178">In the Finance and Operations app, delete the **ContactPersonID** and **InvoiceAccount** columns from the **Customers V3 (accounts)** mapping, and then save the mapping.</span></span>

    1. <span data-ttu-id="58f20-179">在 **客户 V3 (accounts)** 的双写入映射页面，在 **表映射** 选项卡上，在左侧的筛选器中，选择 **Finance and Operations app.Customers V3**。</span><span class="sxs-lookup"><span data-stu-id="58f20-179">On the dual-write mapping page for **Customers V3 (accounts)**, on the **Table mappings** tab, in the left filter, select **Finance and Operations app.Customers V3**.</span></span> <span data-ttu-id="58f20-180">在右侧的筛选器中，选择 **Dataverse.Account**。</span><span class="sxs-lookup"><span data-stu-id="58f20-180">In the right filter, select **Dataverse.Account**.</span></span>
    2. <span data-ttu-id="58f20-181">搜索 **contactperson** 查找 **ContactPersonID** 源列。</span><span class="sxs-lookup"><span data-stu-id="58f20-181">Search for **contactperson** to find the **ContactPersonID** source column.</span></span>
    3. <span data-ttu-id="58f20-182">选择 **操作**，然后选择 **删除**。</span><span class="sxs-lookup"><span data-stu-id="58f20-182">Select **Actions**, and then select **Delete**.</span></span>

        ![删除 ContactPersonID 列](media/cust_selfref3.png)

    4. <span data-ttu-id="58f20-184">重复这些步骤删除 **InvoiceAccount** 列。</span><span class="sxs-lookup"><span data-stu-id="58f20-184">Repeat these steps to delete the **InvoiceAccount** column.</span></span>

        ![删除 InvoiceAccount 列](media/cust_selfref4.png)

    5. <span data-ttu-id="58f20-186">将更改保存到映射。</span><span class="sxs-lookup"><span data-stu-id="58f20-186">Save your changes to the mapping.</span></span>

2. <span data-ttu-id="58f20-187">关闭 **客户 V3** 表的更改跟踪。</span><span class="sxs-lookup"><span data-stu-id="58f20-187">Turn off change tracking for the **Customers V3** table.</span></span>

    1. <span data-ttu-id="58f20-188">在 **数据管理** 工作区中，选择 **数据表** 磁贴。</span><span class="sxs-lookup"><span data-stu-id="58f20-188">In the **Data management** workspace, select the **Data tables** tile.</span></span>
    2. <span data-ttu-id="58f20-189">选择 **客户 V3** 表。</span><span class="sxs-lookup"><span data-stu-id="58f20-189">Select the **Customers V3** table.</span></span>
    3. <span data-ttu-id="58f20-190">在操作窗格上，选择 **选项**，然后选择 **更改跟踪**。</span><span class="sxs-lookup"><span data-stu-id="58f20-190">On the Action Pane, select **Options**, and then select **Change tracking**.</span></span>

        ![选择更改跟踪选项](media/selfref_options.png)

    4. <span data-ttu-id="58f20-192">选择 **禁用更改跟踪**。</span><span class="sxs-lookup"><span data-stu-id="58f20-192">Select **Disable Change Tracking**.</span></span>

        ![选择“禁用更改跟踪”](media/selfref_tracking.png)

3. <span data-ttu-id="58f20-194">运行 **客户 V3 (Accounts)** 映射的初始同步。</span><span class="sxs-lookup"><span data-stu-id="58f20-194">Run initial synchronization for the **Customers V3 (Accounts)** mapping.</span></span> <span data-ttu-id="58f20-195">初始同步应会成功运行，没有任何错误。</span><span class="sxs-lookup"><span data-stu-id="58f20-195">The initial synchronization should run successfully, without any errors.</span></span>
4. <span data-ttu-id="58f20-196">运行 **CDS 联系人 V2 (contacts)** 映射的初始同步。</span><span class="sxs-lookup"><span data-stu-id="58f20-196">Run initial synchronization for the **CDS Contacts V2 (contacts)** mapping.</span></span>

    > [!NOTE]
    > <span data-ttu-id="58f20-197">有两个名称相同的映射。</span><span class="sxs-lookup"><span data-stu-id="58f20-197">There are two maps that have the same name.</span></span> <span data-ttu-id="58f20-198">请确保在 **详细信息** 选项卡上选择具有以下描述的映射：**FO.CDS 供应商联系人 V2 与 CDS.Contacts 之间同步的双写入模板。需要新包 \[Dynamics365SupplyChainExtended\]。**</span><span class="sxs-lookup"><span data-stu-id="58f20-198">Be sure to select the map that has the following description on the **Details** tab: **Dual-write template for sync between FO.CDS Vendor Contacts V2 to CDS.Contacts. Requires new package \[Dynamics365SupplyChainExtended\].**</span></span>

5. <span data-ttu-id="58f20-199">将 **InvoiceAccount** 和 **ContactPersonId** 列重新添加到 **客户 V3 (Accounts)** 映射，然后保存映射。</span><span class="sxs-lookup"><span data-stu-id="58f20-199">Add the **InvoiceAccount** and **ContactPersonId** columns back to the **Customers V3 (Accounts)** mapping, and then save the mapping.</span></span> <span data-ttu-id="58f20-200">**InvoiceAccount** 列和 **ContactPersonId** 列现在又成为了实时同步模式的一部分。</span><span class="sxs-lookup"><span data-stu-id="58f20-200">Both the **InvoiceAccount** column and the **ContactPersonId** column are now part of live synchronization mode again.</span></span> <span data-ttu-id="58f20-201">在下一步中，您将执行这些列的初始同步。</span><span class="sxs-lookup"><span data-stu-id="58f20-201">In the next step, you will do the initial synchronization for these columns.</span></span>
6. <span data-ttu-id="58f20-202">再次运行 **客户 V3 (Accounts)** 映射的初始同步。</span><span class="sxs-lookup"><span data-stu-id="58f20-202">Run initial synchronization again for the **Customers V3 (Accounts)** mapping.</span></span> <span data-ttu-id="58f20-203">由于更改跟踪已关闭，Finance and Operations 应用中 **InvoiceAccount** 和 **ContactPersonId** 的数据将同步到 Dataverse。</span><span class="sxs-lookup"><span data-stu-id="58f20-203">Because change tracking is turned off, the data for **InvoiceAccount** and **ContactPersonId** will be synced from the Finance and Operations app to Dataverse.</span></span>
7. <span data-ttu-id="58f20-204">要将 **InvoiceAccount** 和 **ContactPersonId** 的数据从 Dataverse 同步到 Finance and Operations 应用，必须使用数据集成项目。</span><span class="sxs-lookup"><span data-stu-id="58f20-204">To sync the data for **InvoiceAccount** and **ContactPersonId** from Dataverse to the Finance and Operations app, you must use a data integration project.</span></span>

    1. <span data-ttu-id="58f20-205">在 Power Apps 中，在 **Sales.Account** 和 **Finance and Operations apps.Customers V3** 表之间创建数据集成项目。</span><span class="sxs-lookup"><span data-stu-id="58f20-205">In Power Apps, create a data integration project between the **Sales.Account** and **Finance and Operations apps.Customers V3** tables.</span></span> <span data-ttu-id="58f20-206">数据方向必须是从 Dataverse 到 Finance and Operations 应用。</span><span class="sxs-lookup"><span data-stu-id="58f20-206">The data direction must be from Dataverse to the Finance and Operations app.</span></span> <span data-ttu-id="58f20-207">因为 **InvoiceAccount** 是使用双写入的新属性，您可能需要跳过此属性的初始同步。</span><span class="sxs-lookup"><span data-stu-id="58f20-207">Because **InvoiceAccount** is a new attribute in dual-write, you might want to skip initial synchronization for it.</span></span> <span data-ttu-id="58f20-208">有关详细信息，请参阅[将数据集成到 Dataverse](/power-platform/admin/data-integrator)。</span><span class="sxs-lookup"><span data-stu-id="58f20-208">For more information, see [Integrate data into Dataverse](/power-platform/admin/data-integrator).</span></span>

        <span data-ttu-id="58f20-209">下图显示了一个更新 **CustomerAccount** 和 **ContactPersonId** 的项目。</span><span class="sxs-lookup"><span data-stu-id="58f20-209">The following illustration shows a project that updates **CustomerAccount** and **ContactPersonId**.</span></span>

        ![更新 CustomerAccount 和 ContactPersonId 的数据集成项目](media/cust_selfref6.png)

    2. <span data-ttu-id="58f20-211">将公司条件添加到 Dataverse 一端的筛选器中，以仅让与筛选条件匹配的行在 Finance and Operations 应用中更新。</span><span class="sxs-lookup"><span data-stu-id="58f20-211">Add the company criteria in the filter on the Dataverse side, so that only rows that match the filter criteria will be updated in the Finance and Operations app.</span></span> <span data-ttu-id="58f20-212">要添加筛选器，请选择筛选器按钮。</span><span class="sxs-lookup"><span data-stu-id="58f20-212">To add a filter, select the filter button.</span></span> <span data-ttu-id="58f20-213">然后，在 **编辑查询** 对话框中，您可以添加筛选器查询，如 **\_msdyn\_company\_value eq '\<guid\>'**。</span><span class="sxs-lookup"><span data-stu-id="58f20-213">Then, in the **Edit query** dialog box, you can add a filter query such as **\_msdyn\_company\_value eq '\<guid\>'**.</span></span> 

        > <span data-ttu-id="58f20-214">[注意]如果筛选器按钮未出现，请创建支持票证，让数据集成团队在您的租户上启用筛选器功能。</span><span class="sxs-lookup"><span data-stu-id="58f20-214">[NOTE] If the filter button isn't present, create a support ticket to ask the data integration team to enable the filter capability on your tenant.</span></span>

        <span data-ttu-id="58f20-215">如果您没有为 **\_msdyn\_company\_value** 输入筛选器查询，那么所有行都将同步。</span><span class="sxs-lookup"><span data-stu-id="58f20-215">If you don't enter a filter query for **\_msdyn\_company\_value**, all the rows will be synced.</span></span>

        ![添加筛选器查询](media/cust_selfref7.png)

    <span data-ttu-id="58f20-217">行的初始同步现已完成。</span><span class="sxs-lookup"><span data-stu-id="58f20-217">The initial synchronization of the rows is now completed.</span></span>

8. <span data-ttu-id="58f20-218">在 Finance and Operations 应用中，为 **客户 V3** 表重新打开更改跟踪。</span><span class="sxs-lookup"><span data-stu-id="58f20-218">In the Finance and Operations app, turn change tracking back on for the **Customers V3** table.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]