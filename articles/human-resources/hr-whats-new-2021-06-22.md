---
title: Dynamics 365 Human Resources（2021 年 6 月 22 日）中的新增功能或更改
description: 本文介绍 2021 年 6 月 22 日 Microsoft Dynamics 365 Human Resources 中的新增功能或更改的功能。
author: marcelbf
ms.date: 06/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-06-22
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: aacb605374d99a3c0bad3438c89e33a04a4d7faf
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8897768"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-june-22-2021"></a>Dynamics 365 Human Resources（2021 年 6 月 22 日）中的新增功能或更改

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

本文介绍 Dynamics 365 Human Resources 中的新增、更改或即将推出的功能。

有关更新流程和计划的详细信息，请参阅[更新流程](hr-admin-setup-update-process.md)。

有关新功能及其预计的正式发布日期的详细信息，请参阅 [Dynamics 365 Human Resources 2021 年发布波次 1 概述](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)。

## <a name="in-this-release"></a>在此发布中

此发布中包含以下新功能和缺陷修复。 更改适用于内部版本号 8.1.4258。

### <a name="new-features"></a>新功能

此发布通常提供以下功能。

| 功能 | 发布计划 | 文档 |
| --- | --- | --- |
| 通知用户“未雇用的工作人员”功能 - 当高级访问处于打开状态，并且 **查看所有未雇用的工作人员** 功能在功能管理中处于禁用状态时，“未雇用的工作人员”窗体中将显示一个横幅。 该横幅将指导用户打开 **查看所有未雇用的工作人员** 功能。 | 不适用| [未雇用的工作人员](/dynamics365/human-resources/hr-personnel-workers-without-employment)|
| 对福利管理资格规则的自定义字段支持 | [资格处理的自定义字段支持](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/custom-field-support-eligibility-processing) |[配置资格规则](/dynamics365/human-resources/hr-benefits-setup-eligibility-rules) |
| 休假应计交易记录审计 | 不适用 | [休假应计交易记录审计](hr-leave-and-absence-accrue.md)|
| 休假和缺勤工作流体验增强 | [休假和缺勤工作流体验增强](https://go.microsoft.com/fwlink/?linkid=2147528) | [申请休假](hr-employee-self-service-request-time-off.md)|

### <a name="bug-fixes"></a>缺陷修复

此发布中包含以下缺陷修复。

> [!NOTE]
> 我们的目标是尽快为您提供此信息。 我们可能会更新本文，以包含在最初发布本文之后将其纳入内部版本的缺陷修复。

| 问题编号 | 问题 |  Description |
| --- | --- | --- |
| 583052 | 收到反馈的用户可以编辑收到的反馈 | 当收到有关绩效日记帐的反馈的员工选择 **添加外部链接** 时，窗体变为可编辑，允许员工编辑他们收到的绩效反馈。 |
| 522281 | 在薪酬管理中的薪酬结构磁贴上选择员工数量会导致结果不正确| 当从薪酬工作区向下钻取到薪酬计划时，现在会显示正确的员工数量。 |
| 580683 | 分配给员工和经理角色的用户无法附加注释或更新绩效日记帐 | 分配给员工和经理角色的用户无法附加注释或更新绩效日记帐。 用户收到错误，“无法在绩效日记帐条目 (HcmPerfJournal) 中创建记录。 安全策略权限被拒绝。” |
| 583077 | 休假和缺勤公司日历中员工的出生日期显示不正确的日期 | 用户将能够在休假和缺勤公司日历中查看员工的正确出生日期。 |
| 586996 | 当访问仅限于单个公司时，跨公司休假视图功能会导致余额为空 | 启用跨公司休假视图时，用户可以正确查看员工的未来休假余额。 |
| 581014 | 启用跨公司休假和缺勤视图会导致在查看未来余额时出错 | 用户在启用跨公司休假视图的情况下查看未来休假余额时出现的错误已得到修复。 |
| 509404 | 部门人数分析未考虑部门之间的员工流动。 | 当员工从一个部门迁移到另一个部门时，如果该职位详细信息在当年已过期，则部门人数数据不会反映该员工从中迁出的旧部门。 |
| 584851 | 福利信贷分配规则“无”从不提供信贷 |弹性信贷分配规则“无”导致员工在福利期间收到零信贷，无论他们何时被雇用。 这已得到修复，因此如果员工在福利期间开始前被雇用，则应收到完整弹性信贷，如果在福利期间开始后被雇用，则没有。 |
| 584897 | 重复“使用基本外部功能”责任会导致错误 | 当尝试重复“使用基本外部功能”责任时，用户收到错误，“无法找到具有标识符 UserDefinedAppHostDialogView 的对象。” |
| 575692 | 累积休假和缺勤不可用于待定工作人员 | 当启用 **简化的员工输入** 时，可以在未来雇用时运行休假和缺勤累积。 |
| 580110 | 将公司添加到工资单集成会重置集成以使用所有实体，即使该选项设置为不刷新项目 | 如果客户已删除实体或已更改工资单集成的数据项目，并且具有设置为阻止项目自动刷新的选项，则向集成添加新公司将忽略该设置并刷新项目。  |
| 584518 |注册福利处理绩效问题 | 此 bug 解决了旧福利注册流程中的绩效问题。 |

## <a name="in-preview"></a>预览模式

以下新功能处于预览状态。 有关打开或关闭功能的详细信息，请参阅[管理功能](hr-admin-manage-features.md)。

| 功能 | 发布计划 | 文档 |
| --- | --- | --- |
| 福利管理工作区 | [福利管理工作区（预览）](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [福利管理工作区](hr-benefits-management-workspace.md) |
| 启用简化的工资单集成（工资单集成 API） | [启用与工资单提供商的简化集成](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-simplified-integration-payroll-providers) | [工资单集成 API](hr-admin-integration-payroll-api-introduction.md)|


## <a name="coming-soon"></a>即将推出

| 功能 | 明细 |
| --- | --- |
| 平台更新 10.0.19 (43) | 平台更新 10.0.19 计划于 2021 年 6 月 28 日在服务版本中开始推出。 有关详细信息，请参阅[财务和运营应用版本 10.0.19 的平台更新（2021 年 6 月）](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-19)。 |
|  服务年限显示切换 | 此功能提供使用不同日期计算在 **简化的员工输入** 窗体和 **人员** 窗体中显示的服务年限的选项。  这将在 Human Resources 参数中提供。 |
|  让缺勤管理人员能够管理休假 | [让缺勤管理人员能够管理休假](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-absence-manager-manage-leave) |
|  对特定休假类型的附件授权 | 利用此功能，管理员能够在提交特定休假类型的休假请求时对要添加的附件授权。 |
|  配置每个休假类型的休假单位 | 此功能使管理员能够为每个休假类型配置休假单位（小时或天）。  |
| 使员工能够标记为准备支付 | [使员工能够标记为准备支付](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-employees-be-marked-as-ready-pay) |

有关计划功能及其计划发布的完整列表，请参阅 [Dynamics 365 Human Resources 2021 年发布波次 1 概述](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)。

## <a name="see-also"></a>请参阅

[Human Resources 中的新增功能或更改](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2021 发布第 1 波概述](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[更新流程](hr-admin-setup-update-process.md)</br>
[管理功能](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
