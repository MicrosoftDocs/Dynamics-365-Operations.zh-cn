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
ms.openlocfilehash: d51b547093825a6e7730b5fdfcfb1c081776c63c
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172706"
---
# <a name="troubleshoot-issues-during-initial-synchronization"></a>解决初始同步过程中的问题

[!include [banner](../../includes/banner.md)]



本主题提供 Finance and Operations 应用与 Common Data Service 之间的双写入集成的故障排除信息。 具体来说，提供可以帮助您解决初始同步期间可能发生的问题的信息。 

> [!IMPORTANT]
> 本主题解决的某些问题可能需要系统管理员角色或 Microsoft Azure Active Directory (Azure AD) 租户管理员凭据。 介绍每个问题的每一节说明了是否需要特定角色或凭据。

## <a name="check-for-initial-synchronization-errors-in-a-finance-and-operations-app"></a>在 Finance and Operations 应用中检查初始同步错误

启用映射模板后，映射的状态应为**正在运行**。 如果状态为**未运行**，在初始同步期间将发生错误。 要查看错误，请选择**双写入**页面上的**初始同步详细信息**选项卡。

![初始同步详细信息选项卡](media/initial_sync_status.png)

## <a name="you-cant-complete-initial-synchronization-400-bad-request"></a>您无法完成初始同步：400 错误请求

**解决此问题所需的角色：** 系统管理员

当您尝试运行映射和初始同步时，您可能会收到以下错误消息：

*远程服务器返回错误：(400) 错误请求。），AX 导出遇到错误*

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
3. 在**服务**窗格中，请确保 Microsoft Dynamics 365 数据导入导出框架服务正在运行。 如果已停止，请重新启动，因为初始同步需要它。

## <a name="initial-synchronization-error-403-forbidden"></a>初始同步错误：403 已禁止

在初始同步期间，您可能会收到以下错误消息：

*（\[已禁止\]，远程服务器返回错误：(403) 已禁止。），AX 导出遇到错误*

若要解决此问题，请按照以下步骤操作。

1. 登录到 Finance and Operations 应用。
2. 在 **Azure Active Directory 应用程序**页面上，删除 **DtAppID** 客户端，然后再次添加。

![Azure AD 应用程序列表](media/aad_applications.png)

## <a name="self-reference-failures-during-initial-synchronization"></a>初始同步期间自引用失败

如果您的任何映射都有自引用，您可能会收到类似于以下示例的错误消息：

*在“供应商 V2”上，以下错误：记录 ID：新记录，错误消息：无法解析字段的 GUID：msdyn\_invoicevendoraccountnumber.msdyn\_vendoraccountnumber。未找到查找值：CN-001。尝试使用此 URL 检查引用数据是否存在：`https://sampleorg.crm.dynamics.com/api/data/v9.0/msdyn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber` eq 'CN-001'*

在具有自引用的映射的初始同步期间，将发生此类错误。 在前面的示例中，字段“账单帐户”引用了供应商实体。

若要解决此问题，您可能必须先运行两次映射，才能成功进行初始同步。

