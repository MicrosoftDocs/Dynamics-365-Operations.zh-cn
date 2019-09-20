---
title: Dynamics 365 for Talent（2019 年 6 月 4 日）新增功能或更改
description: 此主题介绍了 Microsoft Dynamics 365 for Talent 中的新增功能和更改的功能。
author: Darinkramer
manager: AnnBe
ms.date: 06/04/2019
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
ms.search.validFrom: 2019-06-04
ms.dyn365.ops.version: Talent
ms.openlocfilehash: e19e5d3f1cb2305e5a4153de3e4d0e8f4c7d31ac
ms.sourcegitcommit: 1bf6a8b2f872394a4f242f9ff13c67e8e1ae8f65
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/03/2019
ms.locfileid: "1856321"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-june-4-2019"></a>Dynamics 365 for Talent（2019 年 6 月 4 日）新增功能或更改

[!include [banner](includes/banner.md)]

此主题介绍了 Microsoft Dynamics 365 for Talent 中的新增功能和更改的功能。

## <a name="changes-in-attract"></a>Attract 中的更改

本版本中包含 Dynamics 365 for Talent: Attract 的小缺陷修复。

## <a name="coming-soon-in-attract"></a>Attract 中即将推出

### <a name="job-approvals-on-the-home-page"></a>主页中的工作审核

仪表板的**审核**部分中将显示审核。 审核人可在**已分配给你**下查看自己的审核。 此部分显示工作 ID、头衔、其他审核人和工作的分配日期。 提交待审核工作的用户可在**您请求的**下查看自己的工作。 此部分显示仍然必须审核所提交工作的审核人。

## <a name="changes-in-onboard"></a>Onboard 中的更改

本版本中包含 Dynamics 365 for Talent: Onboard 的小缺陷修复。

## <a name="changes-in-core-hr"></a>Core HR 中的更改

本部分中介绍的更改适用于内部版本号 8.1.2330。

### <a name="new-page-to-validate-position-hierarchy-data"></a>用于验证职位层次结构数据的新页面

人力资源 (HR) 员工和管理员可以验证管理层次结构以查找任何无意导入的循环引用。 可在**组织管理 \> 链接 \> 职位 \> 职位层次结构验证**中访问这个新页面。

### <a name="specify-reason-codes-on-leave-types"></a>指定休假类型的原因代码

组织可能需要有关休假请求的更多信息。 现在可指定休假类型的原因代码，并让员工在休假请求中选择原因代码。

### <a name="require-reason-codes-for-specific-leave-types-on-time-off-requests"></a>休假请求中的特定休假类型需要原因代码

组织可能会要求当员工提交休假请求时为特定休假类型设置原因代码。 可能因为公司政策或法规要求导致存在此项要求。 可以指定哪些休假类型需要原因代码，并且可以要求员工为自己的休假请求中的休假类型提供原因代码。

### <a name="provide-a-leave-and-absence-transaction-list-for-hr"></a>为 HR 提供休假和缺勤交易记录列表

跟踪员工休假和了解休假的计算方法这一功能不仅可以帮助 HR 解答员工的问题，还可以帮助确保员工的休假奖励精确无误。 HR 现在可以以新的视觉查看交易记录（授权、应计、调整和请求），这样 HR 人员就可以查看休假余额背后的原因。

### <a name="deleting-a-record-from-talent-doesnt-remove-the-record-from-common-data-service"></a>从 Talent 删除记录不会将该记录从 Common Data Service 删除

现在也会从 Common Data Service 删除从 Talent Core HR 删除的记录。

### <a name="variable-compensation-plan-valid-fromto-dates-arent-being-honored"></a>不遵循可变薪酬计划生效/失效日期

此版本中，如果开始日期在计划的开始日期的前面或结束日期在计划的结束日期后面，则不能在可变薪酬计划中登记员工。 

### <a name="performance-review-comments-are-removed-when-users-select-cancel"></a>用户选择“取消”时会删除绩效复查注释

此版本解决了以下问题：用户开始更改注释，然后选择**取消**，则会删除复查注释。 

## <a name="in-preview"></a>预览模式

### <a name="preview-features-are-enabled-only-in-sandbox-instances"></a>只有沙盒实例中才会启用预览功能

配置新的 Talent 实例时，可指定实例类型为**生产**还是**沙盒**。 **沙盒**类型的实例可用于提前测试新功能。 将把所有现有 Talent 实例更新为**生产**实例类型。 如果需要将现有实例之一更新为**沙盒**实例类型，请联系[支持](https://docs.microsoft.com/dynamics365/unified-operations/talent/talent-support)以发起更改请求。

有关如何发布更改的详细信息，请参阅[配置 Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent)。

### <a name="restrict-leave-types-in-time-off-requests"></a>限制请假中的休假类型

组织可以为员工提供多种不同的休假类型。 但是，可能不适合员工提交某些休假类型的请假。 可以改用 HR 管理这些休假类型。 在此版本中，可以配置员工可以提交哪些休假类型的请假。 

## <a name="coming-soon-in-core-hr"></a>Core HR 中即将推出

### <a name="view-extended-information-for-performance-in-manager-self-service"></a>在经理自助服务中查看绩效的更多信息

经理可通过一个新选项查看直接报表和扩展报表的绩效。 现在，职能经理可以分配和更新绩效目标和颁发新审核，与其员工一起管理。 此外，直属经理及其员工可维护和更新绩效日记帐，以帮助确保绩效复查流程顺利进行。 实施此更改后，除了直接报表，经理还可以查看和维护与其扩展报表的绩效有关的信息。 

### <a name="print-performance-reviews"></a>打印绩效复查

员工、经理和 HR 可以打印员工的绩效复查。
