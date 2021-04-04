---
title: Dynamics 365 Human Resources 的新增功能或更改，2021 年 1 月 21 日
description: 此主题介绍了 2021 年 1 月 21 日 Microsoft Dynamics 365 Human Resources - Core HR 中的新增功能和更改的功能。
author: marcelbf
manager: tfehr
ms.date: 01/21/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-01-21
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: fc3bb035686a46030514aca1f5ad03a2681845fd
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/17/2021
ms.locfileid: "5463518"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-january-21-2021"></a>Dynamics 365 Human Resources 的新增功能或更改，2021 年 1 月 21 日

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

本主题介绍了 Dynamics 365 Human Resources 中的新增、更改或即将推出的功能。

有关更新流程和计划的详细信息，请参阅[更新流程](hr-admin-setup-update-process.md)。

有关新功能及其预计的正式发布日期的详细信息，请参阅 [Dynamics 365 Human Resources 2020 年发布波次 2 概述](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/)。


## <a name="in-this-release"></a>在此发布中

此发布中包含以下新功能和缺陷修复。 更改适用于内部版本号 8.1.3866。

### <a name="new-features"></a>新功能

此发布通常提供以下功能。

| 功能 | 发布计划 | 文档 |
| --- | --- | --- |
| 平台更新 10.0.16(40) | -- | [针对 Finance and Operations 应用（2021 年 2 月）的版本 10.0.16 的平台更新](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-16) |
| 增强的工作流请求和审批 | [组织和人员管理工作流体验增强](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) | [用于定位“分配给我的工作项”列表的配置选项](https://docs.microsoft.com/dynamics365/human-resources/hr-whats-new-2020-09-03#configuration-option-to-position-work-items-assigned-to-me-list-477004) |
| 表单 1095-C、表单 1095-B 以及旧“福利”中电子报告的平价医疗法案 (ACA) 合规性更新 | -- | -- | 
| “福利管理”现在支持美国法人的 ACA 合规报告 | -- | [在“福利管理”中生成 ACA 报告](hr-benefits-management-aca-reports.md) |
| “福利管理”现在显示“福利比率层”和“福利比率双层”实体  | -- | -- |

### <a name="bug-fixes"></a>缺陷修复

此发布中包含以下缺陷修复。

> [!NOTE]
> 我们的目标是尽快为您提供此信息。 我们可能会更新本主题，以包含在最初发布本主题之后将其纳入内部版本的缺陷修复。

| 问题编号 | 签发 |  说明 |
| --- | --- | --- |
| 533079 | 尝试查看扣缴时出现导航错误“窗体被错误调用”。 | 修复了通过视图 **截止日期** 查看福利扣缴时出现的错误。 |
| 543641 | 电子报告中未填充邮政编码。  | 修复了当保险范围代码为 M 到 Q 时，邮政编码未在“福利管理”的 ACA 电子报告中出现的内部 bug。 |
| 542815 | 员工自助服务中的个人联系人屏幕允许员工查看其他人的个人联系人。 | 修复了以下错误：员工自助服务个人联系人的 **编辑** 窗体没有充分限制查询以保证只能检索到一个个人联系人，导致用户可以使用键盘快捷方式查看其他人的联系人。 |
| 536157 | 由于调用 IsVirtualEntityPackageInstalled()，无法在“系统管理”中打开 **Microsoft Dataverse 集成** 页。 | 问题阻止 **Microsoft Dataverse 集成** 页在 Human Resources 中加载。 |
| 533079 | 尝试查看扣缴时出现导航错误“窗体被错误调用”。 | 修复了查看 **截止日期** 时位于“福利管理”的 **扣缴** 窗体时出现的错误。 |
| 537264 | 应聘者记录中缺少 **个人信息** 快速选项卡。 | 应聘者的个人信息现在在应聘者记录中提供。 |
| 537267 | **专业经验** 未在内部应聘者记录中显示。 | **专业经验** 快速选项卡现在在内部应聘者记录中显示。 以前，如果应聘者是内部人员，**专业经验** 将替换为 **雇用历史记录**，这是应聘者在组织内的雇用历史记录。 两者都适用，并且必须显示给内部应聘者。 |
| 537067 | **允许联系雇主** 未显示。 | **允许联系雇主** 控件已添加到应聘者记录的 **编辑专业经验** 窗格。 |
| 525957 | 转移完成后 **应聘者状态** 未在内部应聘者中更新。 | 转移完成时（在 **将工作人员转移到新位置分配** 页选择了 **变更职位** 或 **继续** 按钮），应聘者记录上的 **状态** 应会更改为 **雇用**。 |
| 537051 | 印度卢比和土耳其里拉的货币符号未正确同步到 Dataverse | 印度卢比和土耳其里拉的符号现在将正确同步到 Dataverse。 |
| 534846 | 必须为“数据管理”启用招聘表。 | 为招聘请求和应聘者创建的新表现在已为“数据管理”启用。 这允许为表启用更改跟踪，从而可以在 Dataverse 虚拟表上启用 OData 更改跟踪。 |
| 533474 | 修复了缺少 Microsoft.SqlServer.XEvent.dll 引用的问题。 | Microsoft.SqlServer.XEvent.dll 的程序集加载异常阻止在某些环境中设置 Dataverse 虚拟表。 |
| 481122 | **人员** 工作区显示废弃职位。 | 废弃职位在 **人员** 工作区显示为空缺职位。 废弃职位不会再显示。 | 
| 541978 | 将主要电子邮件地址添加到 BaseWorker 实体。 | 此更改将工作人员的主要电子邮件地址添加到 HcmWorkerBaseEntity。 |

## <a name="in-preview"></a>预览模式

以下新功能处于预览状态。 有关打开或关闭功能的详细信息，请参阅[管理功能](hr-admin-manage-features.md)。

| 功能 | 发布计划 | 文档 |
| --- | --- | --- |
| Microsoft Teams 中的 Human Resources 应用 | [Microsoft Teams 中的员工休假和缺勤体验](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) | [Teams 中的 Human Resources 应用](https://go.microsoft.com/fwlink/?linkid=2127841)<br>[管理 Teams 中的休假申请](hr-teams-leave-app.md) |
| 与 LinkedIn Talent Hub 集成 | [与 LinkedIn Talent Hub 集成](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/integration-linkedin-talent-hub) | [与 LinkedIn Talent Hub 集成](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-integration-linkedin) |
| 经理跨公司查看休假 | [经理跨公司查看员工休假](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/cross-company-view-employee-leave-managers) | [配置休假和缺勤参数](https://docs.microsoft.com/dynamics365/human-resources/hr-leave-and-absence-parameters) |
|深入了解休假余额| [深入了解休假余额](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/provide-additional-insight-into-leave-balances) | [管理员工休假](https://docs.microsoft.com/dynamics365/human-resources/hr-leave-and-absence-manage-employee-leave) |
| 经理能够提交职位的招聘请求 | [经理可以提交空缺职位的招聘请求](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/manager-submit-request-recruit-open-positions) | [添加招聘请求](https://docs.microsoft.com/dynamics365/human-resources/hr-personnel-recruit#add-a-recruiting-request) |
| 人事管理中的增强应聘者个人资料 | [人事管理中的增强应聘者个人资料](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/enhanced-candidate-profile-personnel-management) | [添加或编辑应聘者个人资料](https://docs.microsoft.com/dynamics365/human-resources/hr-personnel-recruit#add-or-edit-a-candidate-profile) |
| 启用与招聘提供者的简化集成 | [启用与招聘提供者的简化集成](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/enable-simplified-integration-recruiting-providers) | [招聘工作应聘者](https://docs.microsoft.com/dynamics365/human-resources/hr-personnel-recruit) |

## <a name="coming-soon"></a>即将推出
| 功能 | 明细 |
| --- | --- |
| 福利登记的电子邮件确认 | 当员工从员工自助服务中的福利登记体验中签出时，此功能将提供向他们发送确认电子邮件的选项。 有关详细信息，请参阅[配置每个公司的福利管理参数](hr-benefits-setup-parameters-per-company.md)。 |
| 经理为员工输入的技能可以通过工作流自动审核 | 即将推出。 |

有关计划功能及其计划发布的完整列表，请参阅 [Dynamics 365 Human Resources 2020 年发布波次 2 概述](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/)。

## <a name="terminology-updates-for-microsoft-dataverse"></a>Microsoft Dataverse 术语更新

自 2020 年 11 月起，Common Data Service 已重命名为 [Microsoft Dataverse](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)。 请参阅 Power Apps 博客上的[正式公告](https://powerapps.microsoft.com/blog/reshape-the-future-of-work-with-microsoft-dataverse-for-teams-now-generally-available/)了解详细信息。 连同此名称更改一起，Dataverse 中的一些术语已经更新。 例如，*实体* 现在更新为 *表*，*字段* 现在更新为 *列*。 有关详细信息，请参阅[术语更新](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro#terminology-updates)。

在此版本中，与 Dynamics 365 Human Resources 和 Dataverse 集成相关的术语已在整个应用程序中进行了更新，以反映这些更改。 例如，**Common Data Service 集成** 窗体现在是 **Microsoft Dataverse 集成**。

要了解有关 Dynamics 365 Human Resources 与 Microsoft Dataverse 集成的详细信息，请参阅[配置 Microsoft Dataverse 集成](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-integration-common-data-service)和[配置 Microsoft Dataverse 虚拟表](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-integration-common-data-service-virtual-entities)。

## <a name="see-also"></a>请参阅

[Human Resources 中的新增功能或更改](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2020 发布第 2 波概述](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/)</br>
[更新流程](hr-admin-setup-update-process.md)</br>
[管理功能](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]