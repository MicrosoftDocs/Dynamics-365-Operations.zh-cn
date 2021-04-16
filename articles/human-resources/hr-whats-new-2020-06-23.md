---
title: Dynamics 365 Human Resources（2020 年 6 月 25 日）新增功能或更改
description: 此主题介绍了 2020 年 6 月 23 日 Microsoft Dynamics 365 Human Resources - Core HR 中的新增功能和更改的功能。
author: andreabichsel
ms.date: 06/25/2020
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
ms.search.validFrom: 2020-06-25
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 49853eaaf9d4e0fa44c22b3f0927ae4ab034cf8e
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5802303"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-june-23-2020"></a>Dynamics 365 Human Resources（2020 年 6 月 23 日）新增功能或更改

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

此主题介绍了 Dynamics 365 Human Resources 中的新增功能和更改的功能。 更改适用于内部版本号 8.1.3347。 某些标题中括号内的数字是 LCS 支持号码，供您参考。

## <a name="when-an-enrollment-is-expired-for-a-terminated-employee-the-leave-type-balance-and-amount-are-all-cleared-in-the-leave-enrollment-form-444867"></a>当已离职员工的等记到期时，将彻底清除休假等记表中的休假类型、余额和数量 (444867)

现在在进行此项选择之后，将保留 **休假类型**、**余额** 和 **数量** 中的值，而不是清除。

## <a name="incorrect-forecasted-balance-when-new-feature-leave-accrual-for-a-single-company-or-a-single-plan-is-enabled-456553"></a>启用了新功能（单个公司或单个计划的休假应计）时，预测余额不正确 (456553)

已经启用了单个公司或单个计划的休假应计时，现在显示正确的预测余额。

## <a name="entities-with-relations-that-result-in-duplicate-navigation-properties-456486"></a>多个实体具有将导致重复导航属性的关系 (456486)

此版本解决了多个实体的导航属性（关系）问题。 可以检测到重复关系。 这些情况都已得到纠正。
 
## <a name="cross-company-comments-on-performance-review-455536"></a>审查性能时的跨公司注释 (455536)

安装此修补程序之后，性能审查时会显示跨公司注释。 此更改更正了审查者在不同公司为同一项性能审查输入的注释的视图。
 
## <a name="inconsistency-in-showing-compensation-management-data-432562"></a>薪酬管理数据显示不一致 (432562)

现在经理自助服务中薪酬数据的视图保持一致。 薪酬数据现在可以按照您导航到工作人员 **薪酬详细信息** 的方式一致地对经理显示。
 
## <a name="fixed-compensation-plans-effective-date-defaults-to-todays-date-411994"></a>固定薪酬计划的生效日期默认为当天日期 (411994)

薪酬开始日期现在基于为员工分配的职位的开始日期。

## <a name="leave-and-absence-form-enable-half-day-definition-is-disabled-when-form-opens-452607"></a>休假和缺勤窗体打开时禁用该窗体的“启用半天定义” (452607)

进行此更改之后，将启用 **启用半天定义**，直到出现新的休假事务。 

## <a name="unable-to-publish-to-hcmdiscussionentity-via-excel-totalratingscore-field-error-453899"></a>无法通过 Excel 发布到 HcmDiscussionEntity；TotalRatingScore 字段错误 (453899)

现在可在 Excel 工作簿设计器中使用 **HCMDiscussionEntity** 更新 **TotalRatingScore** 字段。

## <a name="in-preview"></a>预览模式

## <a name="database-logging"></a>数据库记录

数据库日志记录功能让您可以确定要监视哪些表和字段。 它还让您能够确定应该触发更改跟踪的事件。 您可以使用数据库日志记录功能来查看一段时间内的更改。 有关详细信息，请参阅[配置和管理数据库日志记录](hr-admin-database-logging.md)。

## <a name="mandatory-fields"></a>必填字段 

现在可使用 Human Resources 个性化功能将字段设置为必填字段。 此功能需要 **保存的视图**。

## <a name="human-resources-application-in-teams"></a>Teams 中的 Human Resources 应用程序

员工可以在 Microsoft Teams 中查看和请求离岗时间。 他们可以与机器人交互来创建休假请求。 有关详细信息，请参阅 [Teams 中的 Human Resources 应用](https://go.microsoft.com/fwlink/?linkid=2127841)。 

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a>用于福利管理的数据管理框架 (DMF) 实体
 
福利管理实体即将发布。 DMF 实体允许导入和导出数据，以轻松配置福利管理。 福利管理模板可用于移动数据。 模板按顺序导出和导入数据，以保持数据依赖关系。

## <a name="buy-and-sell-leave"></a>购买和出售休假 

一些组织提供允许员工购买和出售其休假的福利。 此流程通常通过手动管理。 此功能可自动管理人力资源部门的策略和请求。 它将简化休假管理流程，并帮助消除错误。 有关详细信息，请参阅：

- [管理购买和出售休假策略](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [购买和出售休假](hr-employee-self-service-buy-sell-leave.md)

## <a name="leave-accrual-for-a-single-company-or-single-plan"></a>单个公司或单个计划的休假假期额度

客户可以处理单个公司或单个休假和缺勤计划的应计项目。 此功能为具有不同休假年限或休假应计政策的客户提供清晰的应计流程。 有关详细信息，请参阅[按公司或按休假计划累积休假](hr-leave-and-absence-accrue.md)。

## <a name="add-attachments-to-time-off-requests"></a>将附件添加到休假请求

在当前的 COVID-19 环境中，向批准的休假请求添加附件的功能至关重要。 员工现在可以添加这些附件。 他们还将对休假请求进行了怎样的更新有更多了解。 有关详细信息，请参阅[将附件添加到现有请求](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request)。

## <a name="add-reason-code-to-accrual-suspensions"></a>将原因代码添加到应计暂停 

原因代码已添加到应计暂停。

## <a name="carry-forward-rules"></a>结转规则 

可为转移了结转调整的结转余额指定结转休假类型。 例如，如果员工结转 10 天，则可为这 10 天选择其他休假类型。 有关详细信息，请参阅[配置休假和缺勤类型](hr-leave-and-absence-types.md)。

## <a name="suspend-leave-accrual-for-specified-leave-types"></a>暂停指定休假类型的休假应计

您可以创建一个规则，以针对输入了无薪假休假请求的员工暂停休假应计。 无薪假可以是一种类型，但不是必须的。 您可以根据其他休假类型暂停任何休假。

## <a name="dmf-entity-available-for-accrual-suspensions"></a>可用于暂停应计的 DMF 实体 

DMF 实体现在可用于暂停应计。

## <a name="coming-soon"></a>即将到期

## <a name="configure-the-name-of-employee-self-service"></a>配置员工自助服务的名称

**人力资源参数** 中将提供一个新选项，可以将“员工自助服务”工作区的名称更新为“自助服务”。

## <a name="checklist-entities-included-in-dataverse"></a>Dataverse 中包含的核对清单实体

Dataverse 内很快将为入职、离职、转移和业务流程提供核对清单实体。

## <a name="see-also"></a>请参阅

[Human Resources 中新增或更改的功能](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2019 发布第 2 波概述](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[更新流程](hr-admin-setup-update-process.md)</br>
[管理功能](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]