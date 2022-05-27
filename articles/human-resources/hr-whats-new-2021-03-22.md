---
title: Dynamics 365 Human Resources 中的新增功能或更改（2021 年 3 月 22 日）
description: 本主题介绍 2021 年 3 月 22 日 Microsoft Dynamics 365 Human Resources 中的新增功能或更改的功能。
author: marcelbf
ms.date: 03/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-03-22
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 13520ca55c98fb1acb6185af393550b12fbc2072
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/04/2022
ms.locfileid: "8693519"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-march-22-2021"></a>Dynamics 365 Human Resources 中的新增功能或更改（2021 年 3 月 22 日）

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

本主题介绍了 Dynamics 365 Human Resources 中的新增、更改或即将推出的功能。

有关更新流程和计划的详细信息，请参阅[更新流程](hr-admin-setup-update-process.md)。

有关新功能及其预计的正式发布日期的详细信息，请参阅 [Dynamics 365 Human Resources 2021 年发布波次 1 概述](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)。

## <a name="in-this-release"></a>在此发布中

此发布中包含以下新功能和缺陷修复。 更改适用于内部版本号 8.1.4049。

### <a name="new-features"></a>新功能

此发布通常提供以下功能。

| 功能 | 发布计划 | 文档 |
| --- | --- | --- |
| 强制取消和重置卡住的批处理作业的选项 (560976) | NA | [重置卡住的批处理作业](./hr-admin-troubleshooting-batch-execution.md) |
| 用于创建新福利计划的次要 UX 更新 (419941) | NA | [创建福利计划](hr-benefits-plans-setup.md) |

### <a name="bug-fixes"></a>缺陷修复

此发布中包含以下缺陷修复。

> [!NOTE]
> 我们的目标是尽快为您提供此信息。 我们可能会更新本主题，以包含在最初发布本主题之后将其纳入内部版本的缺陷修复。

| 问题编号 | 签发 |  说明 |
| --- | --- | --- |
| 554239 | 与 **BusinessProcessTaskAssignment** 表相关的实体的性能改进 | 通过向表添加建议的索引来改进与 **BusinessProcessTaskAssignment** 表相关的实体的性能。 |
| 566061 | 从每晚同步中删除 V2 实体回退代码 | 删除每晚 Dataverse 同步的 V2 回退代码。不再需要回退，它可以防止筛选的同步按预期工作。 该更改增强了 Dataverse 数据同步的一致性。 |
| 538024 | 工作人员福利计划 > 删除结帐引发错误 | 修复了删除“工作人员福利”窗体中“福利计划”选项的结帐时的错误。 |
| 557965 | **福利** 工作区：**有效的生命事件** 链接在 **链接** 部分中应始终可见 | 修复了 **有效的生命事件** 链接在 **链接** 部分中可见，但在不启用 **(预览)福利管理工作区** 功能的情况下尝试导航时引发错误的问题。 有关启用工作区的详细信息，请参阅[福利管理工作区](hr-benefits-management-workspace.md)。 |
| 556672 | 当在功能管理中启用 **简化的员工输入** 时，无法处理已离职员工的应计 | 当在功能管理中启用 **简化的员工输入** 时，用于应计休假和缺勤计划的选项已添加到员工的 **工作历史记录** 下的 **更多选项**。 |
| 562656 | **SysRecordChangeLogValidTimeState** 菜单项应包括在安全特权和 **SystemExternalBasicMaintain** 安全责任的扩展中 | 非系统管理员角色缺少日期管理器窗体上的 **查看更改** 按钮。 |
| 505989 | 生命事件处理：由于使用的日期，未正确处理资格的更改 | 修复了资格处理中的更改依赖于职位开始日期，而不仅是当前职位的问题。 |
| 562286 | 解雇工作人员将多个更新发送到 Dataverse | 解雇工作人员后，将向 Dataverse 发送多个更新操作，导致同一更改有两个更新通知。 如果 Power Automate 流配置为从操作触发，这可能导致多个触发。 |
| 527340 | 当打开休假和缺勤登记时，将显示“不可再现日期/时间”错误 | 当选择休假和缺勤登记时，该错误不再显示。 |
| 561663 | 增加群集预配的等待时间间隔 | 通过群集配置更新来提高基础结构稳定性和预配一致性。 |
| 486129 | 无法在 **职位 > 管理更改** 中编辑自定义字段 | 修复了无法在 **职位** 的 **管理更改** 选项卡中编辑自定义字段的问题。 |

## <a name="in-preview"></a>预览模式

以下新功能处于预览状态。 有关打开或关闭功能的详细信息，请参阅[管理功能](hr-admin-manage-features.md)。

| 功能 | 发布计划 | 文档 |
| --- | --- | --- |
| 福利管理工作区 | [福利管理工作区（预览）](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [福利管理工作区](hr-benefits-management-workspace.md) |
| 限制员工编辑业务联系人详细信息 | [限制员工编辑业务联系人详细信息](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/restrict-employees-editing-business-contact-details) | [限制对个人信息的编辑](hr-employee-self-service-restrict-editing.md)|

## <a name="coming-soon"></a>即将推出

| 功能 | 明细 |
| --- | --- |
| 经理为员工输入的技能可以通过工作流自动审核 | 即将推出。 |

有关计划功能及其计划发布的完整列表，请参阅 [Dynamics 365 Human Resources 2021 年发布波次 1 概述](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)。

## <a name="see-also"></a>请参阅

[Human Resources 中的新增功能或更改](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2021 发布第 1 波概述](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[更新流程](hr-admin-setup-update-process.md)</br>
[管理功能](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]