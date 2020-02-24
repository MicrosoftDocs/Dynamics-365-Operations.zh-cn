---
title: 管理功能
description: 了解如何在 Dynamics 365 Human Resources 中打开或关闭新功能。
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: FeatureManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 84ff11e8237ce0669f7f6ac70c5b4411c5d4b466
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008193"
---
# <a name="manage-features"></a>管理功能

在持续推出适用于 Microsoft Dynamics 365 Human Resources 的新功能时，我们希望让客户尽快体验新功能。 我们提供预览功能，这些功能几乎已针对普通使用准备就绪，并经过了大量测试。 我们正在征求最后一轮的客户反馈和验证，之后就会公开发布。

有关 Human Resources 中的新功能的详细信息，请参阅 [Human Resources 中的新增功能](hr-admin-whats-new.md)和 [Dynamics 365 和 Power Platform 版本计划](https://docs.microsoft.com/dynamics365/release-plans/#pivot=products&panel=products1)。

**功能管理**工作区提供了每个版本提供的功能列表。 默认情况下，新功能处于关闭状态。 可使用该工作区开启这些功能并查看其文档。 有关功能管理的更多信息，请参阅[功能管理概述](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview)。

所有新功能都会在预览阶段提供至少 30 天，通常为 30-60 天。 主要功能通常在预览期之后的每年 10 月和 4 月公开发布。 在**功能管理**工作区中看到新功能后，即可将其打开。 有些功能可能默认已启用。

某项功能公开发布后，即可以在生产环境中将其打开或关闭。 **功能管理**工作区指示何时将强制使用某项预览功能。 此日期通常是 10 月 1 日或 4 月 1 日，以与半年发布计划保持一致。 您无法关闭强制功能。 在强制使用之前，您可以在所有环境中打开和关闭功能。

## <a name="enable-or-disable-preview-features"></a>启用或禁用预览功能

若要访问预览功能，必须首先在您的环境中启用。 预览功能的启用或禁用特定于环境。

> [!IMPORTANT]
> 仅在**沙盒**环境中才能使用预览功能。 开启预览功能时，即对组织中该环境的所有用户启用了该预览功能。 关闭预览功能时，即禁用了该预览功能，并且您的用户不能访问该功能。 在 Human Resources 中，对预览功能的支持受限。 预览功能可以使用的隐私和安全措施更少，并且 Human Resources 服务级别协议 (SLA) 中不涵盖预览功能。 不应使用预览功能处理个人数据（即可能用于确认您的身份的所有信息），也不应处理其他与法律或法规遵从性要求有关的数据。

1. 在 Human Resources 中，选择**系统管理**。

2. 选择**功能管理**磁贴。

3. 要启用预览功能，请从列表中选择它，然后选择**启用**。 要禁用预览功能，请从列表中选择它，然后选择**禁用**。

## <a name="preview-feature-benefits-management"></a>预览功能：福利管理

福利管理为您提供了一个灵活的解决方案，它支持各种福利选项以及可以展示您的服务的易用的员工体验。 有关福利管理配置和使用的详细信息，请参阅[福利管理概述](hr-benefits-management-overview.md)。

福利管理取代了**福利**工作区中的功能。 启用“福利管理”预览功能后，您将无法再访问**福利**工作区的以下窗体：

- **福利**
- **福利元素**
- **缴纳计算比率**
- **福利登记结果**
- **福利到期和延期结果**
- **福利资格策略规则类型**
- **福利资格政策**
- **资格事件**

您可以以只读模式查看这些窗体中的信息。 如果要编辑信息，必须先禁用“福利管理”预览功能。

### <a name="benefits-management-known-issues"></a>福利管理已知问题

#### <a name="life-events"></a>生命事件

处理生命事件时，用户将收到错误：

覆盖范围开始日期必须在*计划期间开始*和*计划期间结束*期间。 

生命事件会继续按预期处理。

#### <a name="eligibility-processing"></a>资格处理

当运行使用 1-5X 薪金、薪金百分比和固定金额覆盖范围金额的福利的资格时，必须将福利详细信息日期设置为**工作经历**中的员工开始日期，其中包括工时数、付款频率和年度福利薪水金额。 如果工作人员存在固定薪酬，应输入工时数以及付款频率，然后将计算年度薪水金额。 如果员工是雇员，则不需要工时数。 我们建议在创建新工作人员时，首先输入固定薪酬。 更新福利详细信息记录：导航到**工作人员 > 工作人员历史记录 > 雇用详细信息**。 将日期调整为工作人员开始日期。

#### <a name="employee-self-service"></a>员工自助服务

员工可以选择自己没有资格享有的计划并签出。例如：某工作人员没有任何依赖方，但可以选择带有家庭覆盖范围选项的医疗计划。

更新人寿保险的覆盖范围金额时，不会计算员工金额。 例如，向员工提供人寿保险计划时，他们最多可以选择 50,000 美元的保额，每 1,000 美元保额费用为 0.36 美元。  当员工更新覆盖范围金额时，员工的关联成本保持为零。

对于仅允许单一选择该计划类型的福利计划，如果用户在选择计划后尝试放弃计划，将会收到错误。 例如，用户选择医疗计划并将其放在他们的购物车中。 然后，用户选择**放弃**另一个医疗计划。 用户将收到错误。

## <a name="preview-features-in-leave-and-absence"></a>休假和缺勤中的预览功能

休假和缺勤预览功能包括：

- **休假和缺勤日历** - 休假和缺勤参数将从**人力资源参数**转到一个名为**休假和缺勤参数**的新屏幕。 新屏幕包括一个新的**日历**选项卡。此预览仅启用一部分参数。 您可以从**休假和缺勤**工作区的**链接**选项卡访问新屏幕。 日历包括：
  - **公司日历** - 显示所有员工的休息时间请求。 具有**人力资源**角色的人员可以从**休假和缺勤**工作区的**链接**选项卡访问此日历。
  - **经理团队日历** - 显示所有直接下属的休息时间请求。 经理可以从**休假和缺勤**下员工自助服务中的**我的团队**选项卡访问此日历。 

- **休假和缺勤假日日历** - 休假类型包括新的**假日**选项，与工作时间日历结合使用。 在生成工作日时，由假日和歇业定义的天现在指定为**假日**。 处理应计时，将对分配到日历的员工进行调整，以考虑工作日的假日。

- **休假应计审计** - 一个新屏幕，您可以查看所有员工和单个员工何时处理和删除了应计。 您可以从**休假和缺勤**工作区的**链接**选项卡访问此新屏幕。

- **休假应计删除** - 您现在可以删除特定休假计划的应计记录。 您可以从**休假和缺勤**工作区的**链接**选项卡访问此新选项。 对于单独员工，此选项显示在员工资料中的**休假和缺勤**分组中。 

- **休假应计舍入** - **休假类型**定义应使用哪种类型的舍入应计，以及应计过程中舍入的小数精度的新选项。 处理应计时，将对应计记录应用此舍入和精度。 

- **在单个休假计划上配置多个休假类型** - 休假类型的休假应计计划中的新列，使您可以在具有不同应计计划的休假和缺勤计划上定义多个休假类型。 以前的**休假类型**字段已删除。 现在，在员工登记中，休假类型的余额显示在表中，而不是在屏幕顶部。

  > [!IMPORTANT]
  > 此功能启用后，将无法关闭。

- **使用员工的全职等效 (FTE) 进行应计** - 休假应计计划上的新列，允许使用 FTE 进行应计。 处理应计时，应用程序将使用员工的主要职位和定义的 FTE 来确定按比例分配的应计金额。

  > [!NOTE]
  > 此功能仅在启用**为每个休假计划配置多个休假类型**后可用。 

## <a name="feedback"></a>反馈

希望您提供有关预览功能的体验信息。 希望您在使用这些功能或其他功能时，定期在以下站点上发布反馈：

- [社区](https://community.dynamics.com/enterprise/f/759?pi53869=0&category=Talent) – 此站点是很好的资源，用户可在这里讨论使用案例，提问和获得社区帮助。
- 告知我们您希望在产品中看到的功能，或您认为我们应对现有功能进行的任何更改。 提出有关 [Human Resources 想法](https://powerusers.microsoft.com/t5/Ideas-for-Human-Resources/idb-p/HumanResources)的产品观点
    
请勿在提交反馈或产品评论时包含个人数据（可用于确认您的身份的任何信息）。 可能会对收集的信息进行更深入的分析，但在适用的隐私法律下不会用于回应申请。 在这些计划下单独收集的个人数据应遵守 [Microsoft 隐私声明](https://privacy.microsoft.com/privacystatement)。

## <a name="see-also"></a>请参阅

- [Human Resources 中的新增功能](hr-admin-whats-new.md)
- [Dynamics 365 和 Power Platform 版本计划](https://docs.microsoft.com/dynamics365/release-plans/#pivot=products&panel=products1)