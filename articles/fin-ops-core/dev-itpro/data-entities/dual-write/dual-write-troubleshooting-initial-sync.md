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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: a2f0e0cbf0f8710dc020a48506775fa28df9c2d2
ms.sourcegitcommit: 7e1be696894731e1c58074d9b5e9c5b3acf7e52a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/17/2020
ms.locfileid: "4744629"
---
# <a name="troubleshoot-issues-during-initial-synchronization"></a>解决初始同步过程中的问题

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

本主题提供 Finance and Operations 应用与 Dataverse 之间的双写入集成的故障排除信息。 具体来说，提供可以帮助您解决初始同步期间可能发生的问题的信息。

> [!IMPORTANT]
> 本主题解决的某些问题可能需要系统管理员角色或 Microsoft Azure Active Directory (Azure AD) 租户管理员凭据。 介绍每个问题的每一节说明了是否需要特定角色或凭据。

## <a name="check-for-initial-synchronization-errors-in-a-finance-and-operations-app"></a>在 Finance and Operations 应用中检查初始同步错误

启用映射模板后，映射的状态应为 **正在运行**。 如果状态为 **未运行**，在初始同步期间将发生错误。 要查看错误，请选择 **双写入** 页面上的 **初始同步详细信息** 选项卡。

![初始同步详细信息选项卡上的错误](media/initial_sync_status.png)

## <a name="you-cant-complete-initial-synchronization-400-bad-request"></a>您无法完成初始同步：400 错误请求

**解决此问题所需的角色：** 系统管理员

当您尝试运行映射和初始同步时，您可能会收到以下错误消息：

*（\[错误请求\]，远程服务器返回错误：(400) 错误请求。），AX 导出遇到错误*

以下是完整错误消息的示例。

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

如果此错误持续发生，您无法完成初始同步，请按照以下步骤解决问题。

1. 登录到 Finance and Operations 应用的虚拟机 (VM)。
2. 打开微软管理终端程序。
3. 在 **服务** 窗格中，请确保 Microsoft Dynamics 365 数据导入导出框架服务正在运行。 如果已停止，请重新启动，因为初始同步需要它。

## <a name="initial-synchronization-error-403-forbidden"></a>初始同步错误：403 已禁止

在初始同步期间，您可能会收到以下错误消息：

*（\[已禁止\]，远程服务器返回错误：(403) 已禁止。），AX 导出遇到错误*

若要解决此问题，请按照以下步骤操作。

1. 登录到 Finance and Operations 应用。
2. 在 **Azure Active Directory 应用程序** 页面上，删除 **DtAppID** 客户端，然后再次添加。

![Azure AD 应用程序列表中的 DtAppID 客户端](media/aad_applications.png)

## <a name="self-reference-or-circular-reference-failures-during-initial-synchronization"></a>初始同步期间自引用或循环引用失败

如果您的任何映射都有自引用或循环引用，您可能会收到错误消息。 错误分为以下几类：

- [供应商 V2–to–msdyn_vendors 表映射中的错误](#error-vendor-map)
- [客户 V3–to–Accounts 表映射中的错误](#error-customer-map)

## <a name="resolve-errors-in-the-vendors-v2tomsdyn_vendors-table-mapping"></a><a id="error-vendor-map"></a>解决供应商 V2–to–msdyn_vendors 表映射中的错误

如果表具有在 **PrimaryContactPersonId** 和 **InvoiceVendorAccountNumber** 列中存在值的现有行，在将 **供应商 V2** 映射到 **msdyn\_vendors** 时，您可能会遇到初始同步错误。 发生这些错误是因为 **InvoiceVendorAccountNumber** 在供应商映射中是一个自引用列，**PrimaryContactPersonId** 是一个循环引用。

您收到的错误消息将为以下形式。

*无法解析字段的 GUID：\<field\>。未找到查找值：\<value\>。请尝试使用此 URL 检查引用数据是否存在：`https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>`*

下面举了一些示例加以说明：

- *无法解析字段的 GUID：msdyn\_vendorprimarycontactperson.msdyn\_contactpersonid。未找到查找值：000056。请尝试使用此 URL 检查引用数据是否存在：`https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'`*
- *无法解析字段的 GUID：msdyn\_invoicevendoraccountnumber.msdyn\_vendoraccountnumber。未找到查找值：V24-1。请尝试使用此 URL 检查引用数据是否存在：`https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/msdn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber eq 'V24-1'`*

如果供应商表中的任何行在 **PrimaryContactPersonId** 和 **InvoiceVendorAccountNumber** 列中都具有值，请按照以下步骤完成初始同步。

1. 在 Finance and Operations 应用中，从映射中删除 **PrimaryContactPersonId** 和 **InvoiceVendorAccountNumber** 列，然后保存映射。

    1. 在 **供应商 V2 (msdyn\_vendors)** 的双写入映射页面上，在 **表映射** 选项卡上，在左侧的筛选器中，选择 **Finance and Operations apps.Vendors V2**。 在右侧的筛选器中，选择 **Sales.Vendor**。
    2. 搜索 **primarycontactperson** 查找 **PrimaryContactPersonId** 源列。
    3. 选择 **操作**，然后选择 **删除**。

        ![删除 PrimaryContactPersonId 列](media/vend_selfref3.png)

    4. 重复这些步骤删除 **InvoiceVendorAccountNumber** 列。

        ![删除 InvoiceVendorAccountNumber 列](media/vend-selfref4.png)

    5. 将更改保存到映射。

2. 关闭 **供应商 V2** 表的更改跟踪。

    1. 在 **数据管理** 工作区中，选择 **数据表** 磁贴。
    2. 选择 **供应商 V2** 表。
    3. 在操作窗格上，选择 **选项**，然后选择 **更改跟踪**。

        ![选择更改跟踪选项](media/selfref_options.png)

    4. 选择 **禁用更改跟踪**。

        ![选择“禁用更改跟踪”](media/selfref_tracking.png)

3. 运行 **供应商 V2 (msdyn\_vendors)** 映射的初始同步。 初始同步应会成功运行，没有任何错误。
4. 运行 **CDS 联系人 V2 (contacts)** 映射的初始同步。 如果要同步供应商表上的主要联系人列，则必须同步此映射，因为还必须对联系人行进行初始同步。
5. 将 **PrimaryContactPersonId** 和 **InvoiceVendorAccountNumber** 列重新添加到 **供应商 V2 (msdyn\_vendors)** 映射，然后保存映射。
6. 再次运行 **供应商 V2 (msdyn\_vendors)** 映射的初始同步。 由于更改跟踪已关闭，所有行都将同步。
7. 重新打开 **供应商 V2** 表的更改跟踪。

## <a name="resolve-errors-in-the-customers-v3toaccounts-table-mapping"></a><a id="error-customer-map"></a>解决客户 V3–to–Accounts 表映射中的错误

如果表具有在 **ContactPersonID** 和 **InvoiceAccount** 列中存在值的现有行，在将 **客户 V3** 映射到 **客户** 时，您可能会遇到初始同步错误。 发生这些错误是因为 **InvoiceAccount** 在供应商映射中是一个自引用列，**ContactPersonID** 是一个循环引用。

您收到的错误消息将为以下形式。

*无法解析字段的 GUID：\<field\>。未找到查找值：\<value\>。请尝试使用此 URL 检查引用数据是否存在：`https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>`*

下面举了一些示例加以说明：

- *无法解析字段的 GUID：primarycontactid.msdyn\_contactpersonid。未找到查找值：000056。请尝试使用此 URL 检查引用数据是否存在：`https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'`*
- *无法解析字段的 GUID：msdyn\_billingaccount.accountnumber。未找到查找值：1206-1。请尝试使用此 URL 检查引用数据是否存在：`https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/accounts?$select=accountnumber.account&$filter=accountnumber eq '1206-1'`*

如果客户表中的任何行在 **ContactPersonID** 和 **InvoiceAccount** 列中都具有值，请按照以下步骤完成初始同步。 您可以对任何现成的表（如 **客户** 和 **联系人**）使用此方法。

1. 在 Finance and Operations 应用中，从 **客户 V3 (accounts)** 映射中删除 **ContactPersonID** 和 **InvoiceAccount** 列，然后保存映射。

    1. 在 **客户 V3 (accounts)** 的双写入映射页面，在 **表映射** 选项卡上，在左侧的筛选器中，选择 **Finance and Operations app.Customers V3**。 在右侧的筛选器中，选择 **Dataverse.Account**。
    2. 搜索 **contactperson** 查找 **ContactPersonID** 源列。
    3. 选择 **操作**，然后选择 **删除**。

        ![删除 ContactPersonID 列](media/cust_selfref3.png)

    4. 重复这些步骤删除 **InvoiceAccount** 列。

        ![删除 InvoiceAccount 列](media/cust_selfref4.png)

    5. 将更改保存到映射。

2. 关闭 **客户 V3** 表的更改跟踪。

    1. 在 **数据管理** 工作区中，选择 **数据表** 磁贴。
    2. 选择 **客户 V3** 表。
    3. 在操作窗格上，选择 **选项**，然后选择 **更改跟踪**。

        ![选择更改跟踪选项](media/selfref_options.png)

    4. 选择 **禁用更改跟踪**。

        ![选择“禁用更改跟踪”](media/selfref_tracking.png)

3. 运行 **客户 V3 (Accounts)** 映射的初始同步。 初始同步应会成功运行，没有任何错误。
4. 运行 **CDS 联系人 V2 (contacts)** 映射的初始同步。

    > [!NOTE]
    > 有两个名称相同的映射。 请确保在 **详细信息** 选项卡上选择具有以下描述的映射：**FO.CDS 供应商联系人 V2 与 CDS.Contacts 之间同步的双写入模板。需要新包 \[Dynamics365SupplyChainExtended\]。**

5. 将 **InvoiceAccount** 和 **ContactPersonId** 列重新添加到 **客户 V3 (Accounts)** 映射，然后保存映射。 **InvoiceAccount** 列和 **ContactPersonId** 列现在又成为了实时同步模式的一部分。 在下一步中，您将执行这些列的初始同步。
6. 再次运行 **客户 V3 (Accounts)** 映射的初始同步。 由于更改跟踪已关闭，Finance and Operations 应用中 **InvoiceAccount** 和 **ContactPersonId** 的数据将同步到 Dataverse。
7. 要将 **InvoiceAccount** 和 **ContactPersonId** 的数据从 Dataverse 同步到 Finance and Operations 应用，必须使用数据集成项目。

    1. 在 Power Apps 中，在 **Sales.Account** 和 **Finance and Operations apps.Customers V3** 表之间创建数据集成项目。 数据方向必须是从 Dataverse 到 Finance and Operations 应用。 因为 **InvoiceAccount** 是使用双写入的新属性，您可能需要跳过此属性的初始同步。 有关详细信息，请参阅[将数据集成到 Dataverse](https://docs.microsoft.com/power-platform/admin/data-integrator)。

        下图显示了一个更新 **CustomerAccount** 和 **ContactPersonId** 的项目。

        ![更新 CustomerAccount 和 ContactPersonId 的数据集成项目](media/cust_selfref6.png)

    2. 将公司条件添加到 Dataverse 一端的筛选器中，以仅让与筛选条件匹配的行在 Finance and Operations 应用中更新。 要添加筛选器，请选择筛选器按钮。 然后，在 **编辑查询** 对话框中，您可以添加筛选器查询，如 **\_msdyn\_company\_value eq '\<guid\>'**。 

        > [注意]如果筛选器按钮未出现，请创建支持票证，让数据集成团队在您的租户上启用筛选器功能。

        如果您没有为 **\_msdyn\_company\_value** 输入筛选器查询，那么所有行都将同步。

        ![添加筛选器查询](media/cust_selfref7.png)

    行的初始同步现已完成。

8. 在 Finance and Operations 应用中，为 **客户 V3** 表重新打开更改跟踪。


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]