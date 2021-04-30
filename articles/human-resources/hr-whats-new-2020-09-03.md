---
title: Dynamics 365 Human Resources（2020 年 9 月 3 日）中的新增功能或更改
description: 此主题介绍了 2020 年 9 月 3 日 Microsoft Dynamics 365 Human Resources - Core HR 中的新增功能和更改的功能。
author: andreabichsel
ms.date: 09/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-09-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 10978d8843e7bce2800d62b63e58152569be9631
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/13/2021
ms.locfileid: "5891761"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-september-3-2020"></a>Dynamics 365 Human Resources（2020 年 9 月 3 日）中的新增功能或更改

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

此主题介绍了 Dynamics 365 Human Resources 中的新增功能和更改的功能。 更改适用于内部版本号 8.1.3504。 某些标题中括号内的数字是 Lifecycle Services (LCS) 支持编号，以供参考。

有关 Human Resources 中即将推出的功能的详细信息，请参阅 [Dynamics 365 Human Resources 2019 发布波次 2 概述](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)。 有关 Human Resources 的更新流程的详细信息，请参阅[更新流程](hr-admin-setup-update-process.md)。

## <a name="in-this-release"></a>在此发布中

### <a name="new-default-financial-dimensions-grid-and-dialog-pattern-throughout-human-resources-469495"></a>Human Resources 中新的默认财务维度网格和对话框模式 (469495)

以下区域中现在提供财务维度的新模式：

- 位置操作（窗体：**HcmPositionActionDetail**）
- 工资单收入代码（窗体：**PayrollEarningCode**）

### <a name="entries-dont-appear-in-company-leave-calendar-if-leave-and-absence-calendar-enhancements-arent-enabled-484406"></a>如果未启用休假和缺勤日历增强，则公司休假日历中不显示条目 (484406)

此版本中解决了公司休假日历中不显示休假条目这一问题。 仅当未启用功能管理选项 **休假和缺勤日历增强** 时，才会出现此问题。

### <a name="benefitplanemployeeentity-issue-467597"></a>BenefitPlanEmployeeEntity 问题 (467597)

此版本解决了 **BenefitsPlanEmployee** 实体的问题。 导入工作人员登记时，现在 **覆盖范围代码** 和 **计划类型代码** 设置正确。 此问题导致了员工福利计划在“员工自助服务”的 **工作人员福利计划** 和 **开放登记** 窗体中显示不正确。

### <a name="electronic-file-1094-c-output-missing-letter-in-xml-435190"></a>XML 格式的电子文件 1094-C 输出中丢失字母 (435190)

此更改解决了在向 IRS 提交时 1094-C 输出文件丢失所需字符这一问题。

### <a name="employee-variable-compensation-table-mapped-to-fixed-compensation-form-476117"></a>“员工可变薪酬”表映射到固定薪酬窗体 (476117)

此更改已让固定薪酬字段与固定薪酬窗体一致。 现在只有可变薪酬窗体中才有可变薪酬字段。

### <a name="leave-requests-allowed-before-enrollment-if-that-leave-type-has-a-negative-minimum-balance-469917"></a>休假类型的最低余额为负时等记前允许休假请求 (469917)

此更改禁止在计划中等记之前输入休假请求，即使等记的最低余额为负。 只能在计划生效时输入或提交请求。

### <a name="document-templates-dont-download-457279"></a>无法下载文档模板 (457279)

通过此更改，现在可以下载所有文档模板。 

### <a name="data-displays-as-column-headers-instead-of-rows-for-the-pay-rate-field-in-the-compensation-plan-report-476077"></a>薪酬计划报表中的“付薪比率”字段的数据显示为列标题，而不是行 (476077)

此分析报表现在显示正确的 **付薪比率** 信息。

## <a name="in-preview"></a>预览模式

### <a name="human-resources-application-in-teams"></a>Teams 中的 Human Resources 应用程序

员工可以在 Microsoft Teams 中查看和请求离岗时间。 他们可以与机器人交互来创建休假请求。 有关详细信息，请参阅：

- Dynamics 365 2020 年发行版本第 1 波计划中的 [Microsoft Teams 中的员工休假和缺勤体验](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams)
- Human Resources 文档中的 [Teams 中的 Human Resources 应用](./hr-admin-teams-leave-app.md)

### <a name="human-resources-app-in-teams-preview-features"></a>Teams 中的 Human Resources 应用预览功能
 
-  **通知**：休假请求的提交者和审核人将在 Teams 中的 Human Resources 应用中收到通知。 审批者将可以审批或拒绝休假请求。 将通知提交者，说明批准还是拒绝了请求。 有关详细信息，请参阅：
   - Dynamics 365 2020 年发行版本第 2 波计划中的 [Microsoft Teams 中的员工休假和缺勤体验](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams)
   - Human Resources 文档中的 [为 Teams 中的 Human Resources 应用启用通知](./hr-admin-teams-leave-app.md#enable-notifications-for-the-human-resources-app-in-teams)
   - Human Resources 文档中的[为单个用户打开或关闭 Teams 通知](./hr-admin-teams-leave-app.md#turn-teams-notifications-on-or-off-for-individual-users)
   - Human Resources 文档中的 [Teams 通知](./hr-teams-leave-app.md#respond-to-teams-notifications)
   - Human Resources 文档中的[查看团队的休假日历](./hr-teams-leave-app.md#view-your-teams-leave-calendar)
 
- **经理休假日历**：经理可以在日历视图中查看其直接下属的已批准和待处理的休假。 通过此视图，可以轻松了解其团队成员的离岗时间。 有关详细信息，请参阅：
   - Dynamics 365 2020 年发行版本第 2 波计划中的 [Microsoft Teams 中的员工休假和缺勤体验](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams)
   - Human Resources 文档中的[查看团队的休假日历](./hr-teams-leave-app.md#view-your-teams-leave-calendar)

### <a name="configuration-option-to-position-work-items-assigned-to-me-list-477004"></a>用于定位“分配给我的工作项”列表的配置选项 (477004)

现在在仪表板右侧列中提供了一个新的选项，用于定位 **分配给我的工作项** 列表。 通过此更改，所有工作项和待办事宜列表在同一个区域显示。 请通过在功能管理中打开 **预览 - 工作流体验增强** 启用此功能。 有关打开预览功能的详细信息，请参阅[管理功能](hr-admin-manage-features.md)。

此功能还可以用于升级个人操作窗体中显示的工作流选项。 工作流选项还在操作快速选项卡上方显示，以便加快访问速度。 有关详细信息，请参阅： 

- Dynamics 365 2020 发行波次 2 计划中的[组织和个人管理工作流体验增强](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements)

![分配给我的工作项](./media/hr-workflow-work-items-assigned-to-me.png)

![工作流项快速访问](./media/hr-workflow-quick-access.png)

## <a name="coming-soon"></a>即将推出

### <a name="checklist-entities-included-in-dataverse"></a>Dataverse 中包含的核对清单实体

Dataverse 内很快将为入职、离职、转移和业务流程提供核对清单实体。

### <a name="benefits-management-reason-codes"></a>福利管理原因代码

福利管理原因代码很快将与 Human Resources 中的现有原因代码合并。 如果在福利管理中创建了超过 15 个字符的原因代码，则必须在福利管理 **原因代码** 窗体中将该原因代码的名称更改为 15 个字符或更少。 更新名称后，该原因代码将在个人管理中现有原因代码窗体下显示。 此更改将在以后推出，不会影响现有功能。

## <a name="see-also"></a>请参阅

[Human Resources 中新增或更改的功能](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2019 发布第 2 波概述](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[更新流程](hr-admin-setup-update-process.md)</br>
[管理功能](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
