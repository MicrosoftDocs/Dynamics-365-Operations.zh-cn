---
title: Dynamics 365 Human Resources（2020 年 10 月 6 日）中的新增功能或更改
description: 本主题介绍了 2020 年 10 月 6 日 Microsoft Dynamics 365 Human Resources 中的新增或更改的功能。
author: jcart1106
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2020-10-06
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 090533a4391488f4ec0929dd4866e55a478ee6e639563ad37a6819592e91b23c
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6739195"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-october-6-2020"></a>Dynamics 365 Human Resources（2020 年 10 月 6 日）中的新增功能或更改

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

本主题介绍了 Dynamics 365 Human Resources 中的新增、更改或即将推出的功能。 有关更新流程和计划的详细信息，请参阅[更新流程](hr-admin-setup-update-process.md)。

有关新功能及其预计的正式发布日期的详细信息，请参阅 [Dynamics 365 Human Resources 2020 年发布波次 2 概述](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/)。

## <a name="in-this-release"></a>在此发布中

此发布中包含以下新功能和缺陷修复。 更改适用于内部版本号 8.1.3636。

### <a name="new-features"></a>新功能

此发布通常提供以下功能。

| 功能 | 发布计划 | 文档 |
| --- | --- | --- |
| 深入了解休假日历 | [深入了解休假日历视图](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/provide-additional-insight-leave-calendar-views) | [查看团队和公司日历](hr-employee-self-service-calendar.md) |

### <a name="bug-fixes"></a>缺陷修复

此发布中包含以下缺陷修复。

>[!NOTE]
> 我们的目标是尽快向您提供此信息。 本主题可能会进行更新，以包含在最初发布本主题之后将其纳入内部版本的缺陷修复。

| 问题编号 | 签发 | 说明 |
| --- | --- | --- |
| 448806 | 在 HCM 参数中，**默认标识类型** 导出为 **RecID** | 对 Human Resources 参数实体的此更改添加了一个其他列，该列显示 **默认标识类型**。 |
| 492923 | 任务录制未保存在 Lifecycle Services (LCS) 中 | 任务录制现在可以保存在 LCS 中。 |
| 429950 | 修复了在更改职位时薪酬不能正确到期的问题 | 当在 **转移工作人员** 页面上更改工作人员的职位时，结束薪酬日期设置在职位结束的前一天。 薪酬结束日期现在与职位结束日期相同。 |
| 467214 | 仅在 **付薪比率转换名称** 设置为 **年度** 时才显示 **按薪金分析** | 具有 **年度** 以外的名称的按薪金付薪比率未显示在薪酬分析中。 通过此更新，薪酬分析现在可以使用所有付薪比率转换。 在按 **小时** 或 **薪金** 运行报告时，使用小时以外的期间的任何付薪比率转换都包含在 **薪金** 筛选器中。 仅具有 **小时** 期间的付薪比率包含在 **小时** 筛选器中。 |
| 482464 | 在查看 **审核** 时，在应用筛选器后，**详细信息** 视图不会更改为网格视图 | 在应用筛选器后，审核网格将按预期显示。 |
| 483184 | 当您在 **休假登记** 记录中选择 **层基础** 作为 **调整后的开始日期** 时，Human Resources 不会生成休假应计 |在生成休假应计时，将填充并使用 **调整后的开始日期**。  |
| 509731 | 如果未来终止劳动的工作人员申请终止日期之后的休假，他们的休假请求将导致问题 | 现在，只要请求在终止日期之前，就可以为终止日期在未来的员工提交休假请求。 |
| 510716 | 针对 **男性平均时薪**，薪酬分析包括男性和女性员工 | 在薪酬分析中，**薪酬人口统计分析** 上的 **男性平均时薪** 包括女性平均薪酬。 现在，它只包括男性。 |
| 511348 | 福利自助服务应仅显示从今天到福利期间结束的有效福利计划 | 在 **福利登记** 页面上向员工显示了过期的福利计划。 此修复将删除这些计划。 |
| 512706 | 将以下字段设置为只读：<ul><li>BenefitPlanEmployeeEntity</li><li>EnrollmentConfirmed</li><li>EnrollmentConfirmedBy</li><li>EnrollmentConfirmedDateTime | 在完成操作后，未正确启用维度详细信息的 **添加** 和 **删除** 按钮。 对 **职位行动详细信息** 页面的此更新将使字段在操作完成后不可编辑。 |

## <a name="in-preview"></a>预览模式

以下新功能处于预览状态。 有关打开或关闭功能的详细信息，请参阅[管理功能](hr-admin-manage-features.md)。

| 功能 | 发布计划 | 文档 |
| --- | --- | --- |
| Microsoft Teams 中的 Human Resources 应用 | [Microsoft Teams 中的员工休假和缺勤体验](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) | [Teams 中的 Human Resources 应用](./hr-admin-teams-leave-app.md)<br>[管理 Teams 中的休假申请](hr-teams-leave-app.md) |
| 增强的工作流请求和审批 | [组织和人员管理工作流体验增强](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) | [用于定位“分配给我的工作项”列表的配置选项](./hr-whats-new-2020-09-03.md#configuration-option-to-position-work-items-assigned-to-me-list-477004) |
| 适用于 Human Resources 的 Dataverse 中的虚拟实体 | [在 Dataverse 中展开 Dynamics 365 Human Resources 核心数据](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/expand-dynamics-365-human-resources-core-data-common-data-service) | [配置 Dataverse 虚拟实体](hr-admin-integration-common-data-service-virtual-entities.md) |

## <a name="coming-soon"></a>即将推出

计划在将来的发布中添加以下新功能：

- **Dataverse 中包含的清单实体**：在 Dataverse 中很快将为入职、离职、转移和业务流程提供清单实体。

- **福利管理原因代码**：福利管理原因代码很快将与 Human Resources 中的现有原因代码合并。 如果在福利管理中创建了超过 15 个字符的原因代码，则必须在福利管理 **原因代码** 窗体中将该原因代码的名称更改为 15 个字符或更少。 更新名称后，该原因代码将在个人管理中现有原因代码窗体下显示。 此更改将在以后推出，不会影响现有功能。

- **经理自助服务中的自定义链接**：为了支持经理，我们正在扩展经理自助服务中的功能。 我们正在添加在 **我的团队** 选项卡上添加自定义链接的功能。此功能类似于员工自助服务中 **我的信息选项卡** 上的自定义链接功能。 有关详细信息，请参阅[经理自助服务中的自定义链接](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/custom-links-manager-self-service)。

有关计划功能及其计划发布的完整列表，请参阅 [Dynamics 365 Human Resources 2019 年发布波次 2 概述](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)。

## <a name="additional-resources"></a>其他资源

[Human Resources 中新增或更改的功能](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2020 发布第 2 波概述](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/)</br>
[更新流程](hr-admin-setup-update-process.md)</br>
[管理功能](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]