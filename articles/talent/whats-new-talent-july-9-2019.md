---
title: Dynamics 365 for Talent 的新增功能或更改（2019 年 7 月 9 日）
description: 此主题介绍了 Microsoft Dynamics 365 for Talent 中的新增功能和更改的功能。
author: Darinkramer
manager: AnnBe
ms.date: 07/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-07-09
ms.dyn365.ops.version: Talent
ms.openlocfilehash: e5bb02a7128cb920a79a5f04ac910be205aeed41
ms.sourcegitcommit: 1bf6a8b2f872394a4f242f9ff13c67e8e1ae8f65
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/03/2019
ms.locfileid: "1856369"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-july-9-2019"></a>Dynamics 365 for Talent 的新增功能或更改（2019 年 7 月 9 日）

[!include [banner](includes/banner.md)]

此主题介绍了 Dynamics 365 for Talent 中的新增功能和更改的功能。

## <a name="changes-in-attract"></a>Attract 中的更改

本版本中包含 Dynamics 365 Talent: Attract 的小缺陷修复。

### <a name="coming-soon-in-attract"></a>Attract 中即将推出
#### <a name="job-approvals-appear-on-the-home-page"></a>主页中显示工作审核

仪表板的**审核**部分中将显示审核。 审核人可以在**已分配给您**（其中显示工作 ID、工作头衔、其他审核人和作业的分配日期）下查看自己的审核。 提交待审核工作的用户可以在**您请求的**（其中显示仍然必须审核提交的工作的审核者）下查看自己的工作。

## <a name="changes-in-onboard"></a>Onboard 中的更改

本版本中包含 Dynamics 365 Talent: Onboard 的小缺陷修复。

## <a name="changes-in-core-hr"></a>Core HR 中的更改

本部分中的更改适用于内部版本号 8.1.2374。

### <a name="platform-update-28"></a>平台 update 28

有关平台更新 28 的其他详细信息，请参阅 [Dynamics 365 for Finance and Operations 平台更新 28（2019 年 7 月）中的预览功能](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-28)。

### <a name="entity-support-for-custom-fields-in-common-data-service"></a>Common Data Service 中自定义字段的实体支持 

以下实体支持自定义字段： 

- **薪酬固定计划**
- **薪酬参考点设置**
- **薪酬参考点设置行**
- **工资单收入代码**
- **付薪期间**
- **固定薪酬事件**
- **薪酬网格**

要查看 Talent 中所有更新的实体：

1. 选择**系统管理**，选择**链接**，然后选择 **Common data service 配置**。
2. 选择 **CDS 实体名称**下拉菜单。 列出的所有实体均为最新版本。 

###  <a name="full-name-added-to-worker-entity-in-common-data-service"></a>向 Common Data Service 中的工作人员实体添加了全名

**全名**字段已添加到**工作人员**实体。

### <a name="full-time-equivalent-higher-than-10"></a>全职等价高于 1.0

如果为某个职位的全职员工输入的值大于 1.0，则会显示警告。 

### <a name="a-warning-no-longer-displays-on-the-worker-page-when-there-is-no-future-dated-employment"></a>当没有将来日期的雇用时，工作人员页面上不再显示警告

当从**人事管理**工作区中的**离职员工**列表导航到**工作人员**页面时，您将不再收到指示存在未来雇用的消息。 

### <a name="unable-to-delete-a-business-process-in-talent"></a>无法删除 Talent 中的业务流程

您现在可以在**业务流程**工作区中删除业务流程。

### <a name="leave-balance-no-longer-displays-zero-for-plans-with-no-accruals-when-using-balance-as-of-accrual-period"></a>在使用截至应计期间的余额时，对于没有应计的计划，休假余额不再显示为零

在没有应计时设置的计划现在可以显示余额。

## <a name="in-preview"></a>预览模式

### <a name="preview-features-are-enabled-only-in-sandbox-instances"></a>只有沙盒实例中才会启用预览功能

配置新的 Talent 实例时，可指定实例类型为**生产**还是**沙盒**。 **沙盒**类型的实例可用于提前测试新功能。 将把所有现有 Talent 实例更新为**生产**实例类型。 如果需要将现有实例之一更新为**沙盒**实例类型，请联系[支持](https://docs.microsoft.com/dynamics365/unified-operations/talent/talent-support)以发起更改请求。

有关如何发布更改的详细信息，请参阅[配置 Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent)。

### <a name="restrict-leave-types-in-time-off-requests"></a>限制请假中的休假类型

组织可以为员工提供多种不同的休假类型。 但是，可能不适合员工提交某些休假类型的请假。 可以改用 HR 管理这些休假类型。 在此版本中，可以配置员工可以提交哪些休假类型的请假。 

## <a name="coming-soon-in-core-hr"></a>Core HR 中即将推出

### <a name="view-extended-information-for-performance-in-manager-self-service"></a>在经理自助服务中查看绩效的更多信息

经理可通过一个新选项查看直接报表和扩展报表的绩效。 现在，职能经理可以分配和更新绩效目标和颁发新审核，与其员工一起管理。 此外，直属经理及其员工可维护和更新绩效日记帐，以帮助确保绩效复查流程顺利进行。 实施此更改后，除了直接报表，经理还可以查看和维护与其扩展报表的绩效有关的信息。 

### <a name="entities-supporting-custom-fields"></a>实体支持自定义字段

将在 Common Data Service 中为自定义字段启用以下实体： 

- **休假类型**
- **工作人员银行帐户**
- **工作日历**
