---
title: Dynamics 365 Human Resources（2020 年 9 月 16 日）中的新增功能或更改
description: 此主题介绍了 2020 年 9 月 16 日 Microsoft Dynamics 365 Human Resources 中的新增功能和更改的功能。
author: jcart1106
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2020-09-16
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: b1386cca9fd39c2cf021e87fcc33da2bbda89630
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/06/2021
ms.locfileid: "6353582"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-september-16-2020"></a>Dynamics 365 Human Resources（2020 年 9 月 16 日）中的新增功能或更改

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

此主题介绍了 Dynamics 365 Human Resources 中的新增功能和更改的功能。 更改适用于内部版本号 8.1.3557。 部分功能旁边括号内的数字是 Lifecycle Services (LCS) 支持编号，以供参考。

## <a name="included-in-this-release"></a>此版本中包含的功能

-  [已保存视图 - 正式发布](/dynamics365-release-plan/2020wave2/finance-operations/finance-operations-crossapp-capabilities/saved-views--general-availability)<br>- 有关详细信息，请参阅[已保存视图](../fin-ops-core/fin-ops/get-started/saved-views.md)。 

- **职位操作** 窗体具有更新的维度网格和新对话框 (469495)。

- 如果您在 **Human Resources 共享参数** 的 **高级访问** 中将 **限制访问工作人员信息** 设置为“是”，福利窗体现在仅显示适当的工作人员 (393384)。

- **WorkCalendar** 实体中的新日历生成选项 (477055)：<br>- 默认结束时间<br>- 默认开始时间<br>- 星期五工作日<br>- 星期一工作日<br>- 星期六工作日<br>- 星期日工作日<br>- 星期四工作日<br>- 星期二工作日<br>- 星期三工作日<br>- 工作日历假日 ID

- **LeaveBankTransactionV1** 实体现在包含原因码 (477823)。

- 现在，您可以保存任务录制 (492923)。

- 数据现在已成功从 **HCMWorkerContactEntity** 发布 (427620)。

- 现在，在 **工作人员操作** 窗体中为合同工工作人员类型显示 **薪酬** 快速选项卡 (482494)。

- 现在，如果您设置了 **固定薪酬**，**级别** 和 **计划** 是必填字段。 如果将这些字段保留为空白，将显示错误消息 (482497)。

- 现在，**福利** 中的 **计划类型** 字段是一个下拉列表 (488768)。

- 如果从 Human Resources 中删除了自定义字段，系统管理员现在会收到通知 (481408)。

- 在终止聘用员工流程中，Human Resources 可以正常工作，不会在好像锁定后更改所选公司(479877)。 

- 经理无法再通过个性化设置添加编号列 (485317)。

- 经理无法再从到期的标识号中删除数据范围筛选器 (485321)。

- 当 **报告** 字段为空时，将鼠标悬停在职位上仍会显示职位详细信息 (433328)。

- 员工现在可以在员工自助服务中查看福利计划信息 (481676)。

- 员工现在可以查看所有已注册的课程 (429048)。

- 现在，您可以限制 **专业证书** 页的查看选项。 您可以按工作人员状态和工作人员类型将查看选项限制为当前法人 (451501)。 


## <a name="in-preview"></a>预览模式

### <a name="human-resources-app-in-teams"></a>Teams 中的 Human Resources 应用

员工可以在 Microsoft Teams 中查看和请求离岗时间。 他们可以与机器人交互来创建休假请求。 有关详细信息，请参阅：

- Dynamics 365 2020 年发行版本第 1 波计划中的 [Microsoft Teams 中的员工休假和缺勤体验](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams)
- Human Resources 文档中的 [Teams 中的 Human Resources 应用](./hr-admin-teams-leave-app.md)

### <a name="human-resources-app-in-teams-preview-features"></a>Teams 中的 Human Resources 应用预览功能
 
-  **通知**：休假请求的提交者和审核人将在 Teams 中的 Human Resources 应用中收到通知。 审批者可以批准或拒绝休假请求。 将通知提交者，说明批准还是拒绝了请求。 有关详细信息，请参阅：
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

![分配给我的工作项。](./media/hr-workflow-work-items-assigned-to-me.png)

![工作流项快速访问。](./media/hr-workflow-quick-access.png)

### <a name="leave-and-absence-calendar"></a>休假和缺勤日历

此版本包括休假和缺勤日历的其他日历选项。 有关详细信息，请参阅[查看团队和公司日历](./hr-employee-self-service-calendar.md)。

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
