---
title: Dynamics 365 Human Resources 2020 年 10 月 22 日中的新增功能或更改
description: 本主题介绍了 2020 年 10 月 22 日 Microsoft Dynamics 365 Human Resources 中的新增或更改的功能。
author: jcart1106
ms.date: 10/22/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2020-10-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 27c34c36b0bf33c28f33f7ecd838a76c5e241cbb
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5802255"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-october-22-2020"></a>Dynamics 365 Human Resources 2020 年 10 月 22 日中的新增功能或更改

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

本主题介绍了 Dynamics 365 Human Resources 中的新增、更改或即将推出的功能。 有关更新流程和计划的详细信息，请参阅[更新流程](hr-admin-setup-update-process.md)。

有关新功能及其预计的正式发布日期的详细信息，请参阅 [Dynamics 365 Human Resources 2020 年发布波次 2 概述](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/)。

## <a name="in-this-release"></a>在此发布中

此发布中包含以下新功能和缺陷修复。 更改适用于内部版本号 8.1.3680。

### <a name="new-features"></a>新功能

此发布通常提供以下功能。

| 功能 | 发布计划 | 文档 |
| --- | --- | --- |
| 平台更新 10.0.14(38) | -- | [针对 Finance and Operations 应用（2020 年 11 月）的版本 10.0.14 的平台更新](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-14) |
| 组织和人员管理工作流体验增强 | [组织和人员管理工作流体验增强](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) | [用于定位“分配给我的工作项”列表的配置选项](https://docs.microsoft.com/dynamics365/human-resources/hr-whats-new-2020-09-03#configuration-option-to-position-work-items-assigned-to-me-list-477004) |


### <a name="bug-fixes"></a>缺陷修复

此发布中包含以下缺陷修复。

> [!NOTE]
> 我们的目标是尽快为您提供此信息。 我们可能会更新本主题，以包含在最初发布本主题之后将其纳入内部版本的缺陷修复。

| 问题编号| 签发  | 说明|
| --- | --- | --- |
| 437922 | 使用 DMF 实体导入 FMLA 小时数会导致只读错误。 | 使用 FMLA 小时数实体导入与 FMLA 案例相关的小时数失败。 我们添加了逻辑以确保导入的小时数不超过案例剩余的小时数。 |
| 512019 | 不正确的 **最后结转** 金额。 | 在 **休假** 页面上，将 **截止日期** 更改为下一个会计期间的第一天使 **年假** 类型的 **最后结转** 金额显示不正确。 现在，它显示正确的金额。 |
| 458639 | **工作人员联系人** 实体不支持更改跟踪模式。 | 我们更新了 **工作人员联系人** 实体，以便您可以在提供您自己的数据库 (BYOD) 方案中使用它。|
| 505347 | 启用简化的工作人员功能后，培训经理可以为员工提交休假请求。 | HR 助理和 HR 经理以外的角色均不得为员工提交休假请求。 |
| 513490 | 福利管理日志记录：为没有覆盖范围选项的计划添加日志记录。 | 我们为 **没有覆盖范围选项的计划** 启用了日志记录结果。 它们现在显示在 **流程结果** 表中并正确排序以显示在顶部。 |
| 517021 | 如果 **计划类型** 中每个类型都有一个登记，则无法选择具有相同 **计划类型** 代码的多个计划。 | 我们更改了选择仅允许一个登记的计划的限制。 现在，限制在 **计划类型代码** 级别上，而不是 **计划类型**。 这项更改允许 HSA 和 FSA 之类的计划，它们具有相同的类型，但是您可以向它们提供单独的 **计划类型代码**。 通过该方法，您可以在相同的登记期间选择二者。 |
| 444791 | 当在薪酬计划中打开 **限制访问** 时，无法在员工自助服务中查看薪酬。 | 在员工自助服务 **薪酬** 卡中，如果员工已在打开了 **限制访问** 的计划中登记并分配有特定角色，当前薪酬金额和增加百分比显示为“0”。 我们已解决此问题，因此员工和经理始终可以查看他们自己及其直接下属的薪酬详细信息。 |
| 457542 | 关闭课程后更新课程详细信息也不会为参加该课程的员工更新相同的信息。 | 现在，在关闭并重新打开课程后更改课程详细信息时，员工信息会正确更新。 |
| 515342 | 无法通过 **CDSLeaveRequestDetailEntity** 插入数据。 找不到公司或公司不存在。 | 您现在可以使用 **CDSLeaveRequestDetailEntity** 插入数据。 |
| 514743 | 使用 Microsoft Exchange 时 **电子邮件参数** 窗体中有错误。 | 当电子邮件提供商设置为 **Exchange** 时，**电子邮件参数** 页面中显示消息“无法加载文件或程序集...”。 此修复还允许 **电子邮件参数** 页面按预期加载并保存。 |


## <a name="in-preview"></a>预览模式

以下新功能处于预览状态。 有关打开或关闭功能的详细信息，请参阅[管理功能](hr-admin-manage-features.md)。

| 功能 | 发布计划 | 文档 |
| --- | --- | --- |
| Microsoft Teams 中的 Human Resources 应用 | [Microsoft Teams 中的员工休假和缺勤体验](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) | [Teams 中的 Human Resources 应用](https://go.microsoft.com/fwlink/?linkid=2127841)<br>[管理 Teams 中的休假申请](hr-teams-leave-app.md) |
| 增强的工作流请求和审批 | [组织和人员管理工作流体验增强](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) | [用于定位“分配给我的工作项”列表的配置选项](https://docs.microsoft.com/dynamics365/human-resources/hr-whats-new-2020-09-03#configuration-option-to-position-work-items-assigned-to-me-list-477004) |
| 适用于 Human Resources 的 Dataverse 中的虚拟实体 | [在 Dataverse 中展开 Dynamics 365 Human Resources 核心数据](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/expand-dynamics-365-human-resources-core-data-common-data-service) | [配置 Dataverse 虚拟实体](hr-admin-integration-common-data-service-virtual-entities.md) |
| 与 LinkedIn Talent Hub 集成 | [与 LinkedIn Talent Hub 集成](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/integration-linkedin-talent-hub) | [与 LinkedIn Talent Hub 集成](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-integration-linkedin) |
| 经理自助服务中的自定义链接 | [经理自助服务中的自定义链接](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/custom-links-manager-self-service) | [经理自助服务中的自定义链接](https://aka.ms/MSSCustomLinks) |

## <a name="coming-soon"></a>即将推出

有关计划功能及其计划发布的完整列表，请参阅 [Dynamics 365 Human Resources 2020 年发布波次 2 概述](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/)。


## <a name="see-also"></a>请参阅

[Human Resources 中新增或更改的功能](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2020 发布第 2 波概述](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/)</br>
[更新流程](hr-admin-setup-update-process.md)</br>
[管理功能](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]