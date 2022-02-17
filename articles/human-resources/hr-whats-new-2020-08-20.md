---
title: Dynamics 365 Human Resources 的新增功能或更改（2020 年 8 月 20 日）
description: 此主题介绍了 2020 年 8 月 20 日 Microsoft Dynamics 365 Human Resources - Core HR 中的新增功能和更改的功能。
author: andreabichsel
ms.date: 08/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-08-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: a97997212a090f141c7280f7e48fd116a1f31481
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/31/2022
ms.locfileid: "8062153"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-august-20-2020"></a>Dynamics 365 Human Resources 的新增功能或更改（2020 年 8 月 20 日）

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



此主题介绍了 Dynamics 365 Human Resources 中的新增功能和更改的功能。 更改适用于内部版本号 8.1.3478。 某些标题中括号内的数字是 Lifecycle Services (LCS) 支持编号，以供参考。

## <a name="show-upcoming-and-pending-leave-of-absence-information-to-cards-in-people-workspace"></a>在“人员”工作区向卡显示即将发生和待处理休假信息

现在，待处理和即将发生的休假请求选项可在 **人员** 工作区中的休假和缺勤卡上找到。

## <a name="private-field-isnt-yes-by-default-for-employee-role-in-employee-self-service-477106"></a>默认情况下，“员工自助服务”中“员工”角色的“专用”字段不是“是” (477106)

现在，当员工通过“员工自助服务”中的 **个人信息** 页面添加新地址记录时，**专用** 字段将默认为 **是**。 

## <a name="candidates-to-hire-fasttab-in-personnel-management-shows-an-incorrect-count-of-candidates-470110"></a>“人事管理”中的“可雇用的应聘者”快速选项卡显示不正确的应聘者计数 (470110)

**人事管理** 页面现在可以准确显示要雇用的应聘者数量。 

## <a name="cant-enter-sickness-for-terminated-employee-when-accrual-is-set-to-zero-446195"></a>当应计设置为零时，无法为离职员工输入疾病 (446195)

现在允许将来离职员工的休假交易记录，应计将设置为零。 一直到员工的离职日期均可以输入休假交易记录。 

## <a name="adding-custom-fields-to-the-new-worker-form-disables-the-fields-in-the-action-pane-for-manage-leave-473314"></a>将自定义字段添加到新的工作人员窗体会禁用“管理休假”操作窗格中的字段 (473314)

如果已将自定义字段添加到新的 **工作人员** 窗体中，将不再禁用 **管理休假** 中新的 **工作人员** 窗体上的操作窗格选项。

## <a name="making-the-leave-comment-field-mandatory-allows-a-leave-request-to-be-submitted-when-no-comment-is-entered-473543"></a>将“休假注释”字段设为必填字段会允许在未输入注释时提交休假请求 (473543)

注释字段现在可以是必填字段，休假请求将遵循此设置。 必填字段是预览功能。

### <a name="dmf-entity-available-for-accrual-suspensions"></a>可用于暂停应计的 DMF 实体

DMF 实体现在可用于暂停应计。

## <a name="in-preview"></a>预览模式

### <a name="mandatory-fields"></a>必填字段

您可以使用 Human Resources 个性化功能将字段设置为必填字段。 此功能需要 **保存的视图**。 有关已保存视图的详细信息，请参阅：

- Dynamics 365 2020 年发行版本第 2 波计划中的[已保存视图 - 正式发布](/dynamics365-release-plan/2020wave2/finance-operations/finance-operations-crossapp-capabilities/saved-views--general-availability)
- [生成可充分利用已保存视图的窗体](../fin-ops-core/dev-itpro/user-interface/understanding-saved-views.md)

### <a name="human-resources-application-in-teams"></a>Teams 中的 Human Resources 应用程序

员工可以在 Microsoft Teams 中查看和请求离岗时间。 他们可以与机器人交互来创建休假请求。 有关详细信息，请参阅：

- Dynamics 365 2020 年发行版本第 1 波计划中的 [Microsoft Teams 中的员工休假和缺勤体验](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams)
- [Teams 中的 Human Resources 应用](./hr-admin-teams-leave-app.md)

## <a name="coming-soon"></a>即将到期

### <a name="human-resources-app-in-teams-preview-features"></a>Teams 中的 Human Resources 应用预览功能
 
-  **通知**：休假请求的提交者和审核人将在 Teams 中的 Human Resources 应用中收到通知。 审核人能够批准或拒绝休假请求，如果请求被批准或拒绝，将通知提交者。
 
- **经理休假日历**：经理可以在日历视图中查看其直接下属的已批准和待处理的休假。 通过此视图，可以轻松了解其团队成员的离岗时间。

### <a name="checklist-entities-included-in-dataverse"></a>Dataverse 中包含的核对清单实体

Dataverse 内很快将为入职、离职、转移和业务流程提供核对清单实体。

## <a name="known-issues"></a>已知问题

**功能管理** 工作区可能会显示正式发布时被作为预览功能禁用的功能。 以下是显示错误状态的正式发布功能的列表。 

- 福利管理
- 案例管理
- 数据库日志记录(审核)
- 单个公司或单个计划的休假假期额度
- 休假和缺勤假期额度记录暂停
- 余额调整原因代码和注释
- 购买和出售休假
- 休假和缺勤日历
- 休假结转规则
- 休假假期额度记录审核
- 休假假期额度记录删除
- 休假假期额度记录舍入
- 在单个休假计划上配置多个休假类型
- 更新请假增强功能
- 将员工的全职人力工时用于假期额度记录
- 跨公司薪酬视图
- 打印绩效复查
- 休假假期额度记录节假日更正

### <a name="benefit-plan-employee-entity"></a>福利计划员工实体 

我们最近发现了两个有关 **BenefitsPlanEmployee** 实体的问题。 导入工作人员登记时，**覆盖范围代码** 和 **计划类型代码** 设置不正确。 此问题导致员工福利计划在“员工自助服务”的 **工作人员福利计划** 窗体和 **开放登记** 窗体中显示不正确。 此问题还会影响员工在“员工自助服务”中选择计划的能力。 当前没有解决方法。 我们将此问题视为高优先级修复，将在我们的下一个版本中推出修复程序。

## <a name="see-also"></a>请参阅

[Human Resources 中新增或更改的功能](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2019 发布第 2 波概述](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[更新流程](hr-admin-setup-update-process.md)</br>
[管理功能](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]