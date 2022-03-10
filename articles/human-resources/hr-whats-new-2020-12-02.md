---
title: Dynamics 365 Human Resources（2020 年 12 月 2 日）中的新增功能或更改
description: 本主题介绍 2020 年 12 月 2 日 Microsoft Dynamics 365 Human Resources 中的新增或更改的功能。
author: marcelbf
ms.date: 12/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2020-12-02
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6e02586ad3e6b4428f2ba826851db6ebc3172bdf1760b483032f5159e7864a81
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6782651"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-december-2-2020"></a>Dynamics 365 Human Resources（2020 年 12 月 2 日）中的新增功能或更改

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

本主题介绍了 Dynamics 365 Human Resources 中的新增、更改或即将推出的功能。

有关更新流程和计划的详细信息，请参阅[更新流程](hr-admin-setup-update-process.md)。

有关新功能及其预计的正式发布日期的详细信息，请参阅 [Dynamics 365 Human Resources 2020 年发布波次 2 概述](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/)。

## <a name="in-this-release"></a>在此发布中

此发布中包含以下新功能和缺陷修复。 更改适用于内部版本号 8.1.3788。

### <a name="new-features"></a>新功能

此发布通常提供以下功能。

| 功能 | 发布计划 | 文档 |
| --- | --- | --- |
| 经理能够提交职位的招聘请求 | [经理可以提交空缺职位的招聘请求](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/manager-submit-request-recruit-open-positions) | [添加招聘请求](./hr-personnel-recruit.md#add-a-recruiting-request) |
| 人事管理中的增强应聘者个人资料 | [人事管理中的增强应聘者个人资料](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/enhanced-candidate-profile-personnel-management) | [添加或编辑应聘者个人资料](./hr-personnel-recruit.md#add-or-edit-a-candidate-profile) |
| 启用与招聘提供者的简化集成 | [启用与招聘提供者的简化集成](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/enable-simplified-integration-recruiting-providers) | [招聘工作应聘者](./hr-personnel-recruit.md) |
| 经理自助服务中的自定义链接 | [经理自助服务中的自定义链接](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/custom-links-manager-self-service) | [经理自助服务中的自定义链接](./hr-employee-manager-self-service-custom-links.md) |


### <a name="bug-fixes"></a>缺陷修复

此发布中包含以下缺陷修复。

> [!NOTE]
> 我们的目标是尽快为您提供此信息。 我们可能会更新本主题，以包含在最初发布本主题之后将其纳入内部版本的缺陷修复。

| 问题编号 | 签发 | 说明 |
| --- | --- | --- |
| 514087 | BenefitEligibilityProcessResult 应包括在处理中使用的日期/时间。 | BenefitEligibity 处理结果现在包括上次处理的 datetimestamp，它在之前已丢失。 |
| 526903 | 当在 **Human Resources 共享参数** 中打开 **自动选择指定人员** 时，具有依赖方的计划的福利登记将失败。 | 修复了在为默认指定人员打开 **自动选择指定人员** 选项时依赖方的福利登记失败的问题。 |
| 521922 | **显示缺勤但不包含详细信息** 参数在团队缺勤日历中显示休假请求的详细信息。 | 当在 **休假和缺勤参数** 中 **显示缺勤但不包含详细信息** 设置为 **是** 时，在团队缺勤日历中显示休假类型、休假类型颜色和日期详细信息。 此问题已解决，现在不显示休假类型，并且团队缺勤日历上的所有休假类型均使用默认休假类型颜色（深蓝色）。 |
| 527316 | 工作、职位和工作人员通知的标题更改不同步。 | 之前已向工作、职位和工作人员实体添加了标题关联。 此关联的同步适用于从 Human Resources 到 Dataverse 的同步，但不适用于来自 Dataverse 的通知。 此问题已解决。 |
| 512275 | 从 **休假和缺勤参数** 中删除颜色选项。 | 现在，在休假类型上定义了颜色，**休假和缺勤参数** 中不再需要颜色选项，因此将其删除。 |
| 437112 | 员工职位分配期间的误导性错误消息文本。 | 在雇用工作人员并尝试将工作人员分配到不活动的职位时，更新了错误消息。 更新了消息 **从雇用开始日期开始，指定的职位不活动。请检查此职位的持续时间。** |
| 527816 | **休假** 页面的性能问题。 | 已在 **休假** 页面上改进性能。 |
| 523158 | BenefitPeriodMigrationUpgrade 和 BenefitPlanMigrationUpgrade 未执行。 | 修复了未正确执行与 **期间** 和 **计划** 相关的福利迁移工作。 |

## <a name="in-preview"></a>预览模式

以下新功能处于预览状态。 有关打开或关闭功能的详细信息，请参阅[管理功能](hr-admin-manage-features.md)。

| 功能 | 发布计划 | 文档 |
| --- | --- | --- |
| Microsoft Teams 中的 Human Resources 应用 | [Microsoft Teams 中的员工休假和缺勤体验](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) | [Teams 中的 Human Resources 应用](./hr-admin-teams-leave-app.md)<br>[管理 Teams 中的休假申请](hr-teams-leave-app.md) |
| 增强的工作流请求和审批 | [组织和人员管理工作流体验增强](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) | [用于定位“分配给我的工作项”列表的配置选项](./hr-whats-new-2020-09-03.md#configuration-option-to-position-work-items-assigned-to-me-list-477004) |
| 与 LinkedIn Talent Hub 集成 | [与 LinkedIn Talent Hub 集成](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/integration-linkedin-talent-hub) | [与 LinkedIn Talent Hub 集成](./hr-admin-integration-linkedin.md) |
|经理跨公司查看休假 | [经理跨公司查看员工休假](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/cross-company-view-employee-leave-managers) | [配置休假和缺勤参数](./hr-leave-and-absence-parameters.md) |
|深入了解休假余额| [深入了解休假余额](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/provide-additional-insight-into-leave-balances) | [管理员工休假](./hr-leave-and-absence-manage-employee-leave.md) |
| 经理能够提交职位的招聘请求 | [经理可以提交空缺职位的招聘请求](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/manager-submit-request-recruit-open-positions) | [添加招聘请求](./hr-personnel-recruit.md#add-a-recruiting-request) |
| 人事管理中的增强应聘者个人资料 | [人事管理中的增强应聘者个人资料](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/enhanced-candidate-profile-personnel-management) | [添加或编辑应聘者个人资料](./hr-personnel-recruit.md#add-or-edit-a-candidate-profile) |
| 启用与招聘提供者的简化集成 | [启用与招聘提供者的简化集成](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/enable-simplified-integration-recruiting-providers) | [招聘工作应聘者](./hr-personnel-recruit.md) |

## <a name="coming-soon"></a>即将推出

有关计划功能及其计划发布的完整列表，请参阅 [Dynamics 365 Human Resources 2020 年发布波次 2 概述](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/)。

## <a name="see-also"></a>请参阅

[Human Resources 中新增或更改的功能](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2020 发布第 2 波概述](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/)</br>
[更新流程](hr-admin-setup-update-process.md)</br>
[管理功能](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]