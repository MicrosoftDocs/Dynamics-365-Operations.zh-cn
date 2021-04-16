---
title: Dynamics 365 Human Resources（2020 年 5 月 28 日）中的新增功能或更改
description: 此主题介绍了 2020 年 5 月 28 日 Microsoft Dynamics 365 Human Resources - Core HR 中的新增功能和更改的功能。
author: andreabichsel
ms.date: 05/28/2020
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
ms.search.validFrom: 2020-05-28
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0e15891a2cb75851d195e08b87bbfc9efb78e66e
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5803385"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-may-28-2020"></a>Dynamics 365 Human Resources（2020 年 5 月 28 日）中的新增功能或更改

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

此主题介绍了 Dynamics 365 Human Resources 中的新增功能和更改的功能。 更改适用于内部版本号 8.1.3287。 某些标题中括号内的数字是 LCS 支持号码，供您参考。

## <a name="leaverequest-entity-doesnt-work-when-you-enable-multiple-types-per-leave-plan-447498"></a>在每个休假计划中启用多种类型时，LeaveRequest 实体不起作用 (447498)

通过此更改，**LeaveEnrollmentV2Entity** 现在可用于更正启用多个休假类型时发生的错误。

## <a name="batch-contention-reduction-feature-preview-446619"></a>批处理争用缩减功能（预览）(446619)

启用此功能后，可以减少选择任务和完成作业时对批处理框架表的阻碍。

## <a name="updateconflict-while-saving-worker-prevents-editing-a-record-in-people-427915"></a>保存工作人员时发生的 UpdateConflict 阻止在“人员”中编辑记录 (427915)

此更改更正添加新工作人员、更新地址信息和更改语言首选项时出现的错误。 在此特殊情况下，显示的错误指示无法更新记录。 

## <a name="unable-to-add-an-attachment-to-an-approved-leave-request-to-resubmit-425407"></a>无法向批准的请假添加附件以重新提交 (425407)

此更改现在允许附件添加到批准的休假请求中。

## <a name="user-can-enter-compensation-for-an-employee-in-a-different-legal-entity-form-409529"></a>用户可以在其他法人窗体中为员工输入薪酬 (409529)

此更改禁用了薪酬选项，以防止为错误的法人误输入薪酬条目。

## <a name="error-when-you-transfer-an-employee-and-the-worker-position-assignment-date-is-before-the-position-duration-429402"></a>当您转移员工并且工作人员职位分配日期早于职位期限时发生错误 (429402)

在此情况下转移员工时显示的错误消息已更新，以更好地描述更正问题所需的更改。

## <a name="attachments-capabilities-in-employee-self-service-benefits-enrollment"></a>员工自助服务福利登记中的附件功能
 
现在，您可以在福利登记流程中为员工登记的每个计划添加附件。 然后，您可以在 **工作人员登记福利** 窗体中查看附件。

## <a name="in-preview"></a>预览模式

## <a name="human-resources-application-in-teams"></a>Teams 中的 Human Resources 应用程序

员工可以在 Microsoft Teams 中查看和请求离岗时间。 他们可以与机器人交互来创建休假请求。 有关详细信息，请参阅 [Teams 中的 Human Resources 应用](https://go.microsoft.com/fwlink/?linkid=2127841)。 

## <a name="leave-suspension"></a>休假暂停

可在 Human Resources 中暂停员工的休假和缺勤。 暂停休假将停止所选休假类型的休假应计。 如果处理了应计后发生暂停，暂停休假将为员工的休假余额创建按比例调整。 有关详细信息，请参阅[暂停休假](hr-leave-and-absence-suspend-leave.md)。

## <a name="update-user-experience-to-indicate-that-accrual-is-suspended-429550"></a>更新用户体验以表明应计已暂停 (429550)

用户体验现在表明计划已暂停应计。

## <a name="coming-soon"></a>即将到期

## <a name="database-logging-in-preview-in-june"></a>数据库日志记录（6 月预览）

数据库日志记录功能让您可以确定应该监视哪些表和字段。 它还让您能够确定应该触发更改跟踪的事件。 查询功能可用于查看一段时间内发生的更改。

## <a name="buy-and-sell-leave-in-preview-june-1"></a>购买和出售休假（6 月 1 日预览）

一些组织提供允许员工购买和出售其休假的福利。 此流程通常通过手动管理。 此功能提供了一种更加自动化的方法来管理人力资源部门的政策和请求，它可以帮助消除错误并简化休假管理流程。 有关详细信息，请参阅：

- [管理购买和出售休假策略](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [购买和出售休假](hr-employee-self-service-buy-sell-leave.md)

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a>用于福利管理的数据管理框架 (DMF) 实体
 
福利管理实体即将发布。 DMF 实体允许导入和导出数据，以轻松配置福利管理。 福利管理模板也可用于移动数据。 模板以顺序方式导出和导入数据，以保持数据依赖关系。

## <a name="add-reason-code-to-accrual-suspensions-june-1"></a>将原因代码添加到应计暂停（6 月 1 日）

原因代码已添加到应计暂停。

## <a name="carry-forward-rules-june-1"></a>结转规则（6 月 1 日）

可为转移了结转调整的结转余额指定结转休假类型。 例如，如果员工结转 10 天，则可为这 10 天选择其他休假类型。 有关详细信息，请参阅[配置休假和缺勤类型](hr-leave-and-absence-types.md)。

## <a name="suspend-leave-accrual-for-specified-leave-types-june-1"></a>暂停指定休假类型的休假应计（6 月 1 日）

在此版本中，HR 可以创建一个规则，以针对输入了无薪假休假请求的员工暂停休假应计。 无薪假可以是一种类型，但不是必须的。 您可以根据其他休假类型暂停任何休假。

## <a name="dmf-entity-available-for-accrual-suspensions-june-1"></a>可用于暂停应计的 DMF 实体（6 月 1 日）

DMF 实体现在可用于暂停应计。

## <a name="see-also"></a>请参阅

[Human Resources 中新增或更改的功能](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2019 发布第 2 波概述](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[更新流程](hr-admin-setup-update-process.md)</br>
[管理功能](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]