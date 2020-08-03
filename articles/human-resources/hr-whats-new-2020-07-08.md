---
title: Dynamics 365 Human Resources 的新增功能或更改（2020 年 7 月 8 日）
description: 此主题介绍了 Microsoft Dynamics 365 Human Resources 中的新增功能和更改的功能。
author: Darinkramer
manager: AnnBe
ms.date: 7/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8fe7bc33407bd5781d565f854c0f096766da5fc9
ms.sourcegitcommit: bd9ff0d28718d535356ffbe1cffaaf60310dd430
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/13/2020
ms.locfileid: "3555380"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-july-8-2020"></a>Dynamics 365 Human Resources 的新增功能或更改（2020 年 7 月 8 日）

此主题介绍了 Dynamics 365 Human Resources 中的新增功能和更改的功能。 更改适用于内部版本号 8.1.3382。 某些标题中括号内的数字是 LCS 支持号码，供您参考。

## <a name="database-logging"></a>数据库记录

数据库日志记录功能让您可以确定要监视哪些表和字段。 它还让您能够确定应该触发更改跟踪的事件。 您可以使用数据库日志记录功能来查看一段时间内的更改。 有关详细信息，请参阅[配置和管理数据库日志记录](hr-admin-database-logging.md)。

## <a name="configure-the-name-of-employee-self-service"></a>配置员工自助服务的名称

现在，在 **Human Resources 参数**中，您可以将**员工自助服务**工作区的名称更改为**自助服务**。 有关详细信息，请参阅[更改员工自助服务工作区名称](hr-employee-self-service-workspace-name.md)

## <a name="benefits-management-open-enrollment-access-outside-of-period"></a>在期间之外访问福利管理开放登记

此版本修复了员工可以在登记期间之外或在没有生活事件的情况下访问福利开放登记的问题。 因此，如果您需要在员工自助服务中演示开放登记，则必须将开放登记日期调整为今天（或更早）才能使用。 您可以在**福利管理 > 规则和选项期间**下更改此设置。

## <a name="email-employee-enrollment-confirmation"></a>电子邮件员工登记确认

您现在可以在员工完成福利选择后向他们发送电子邮件。 您可以发送默认消息，也可以使用组织电子邮件模板。 这些设置在 **Human resource 参数 > 福利管理**下。

## <a name="canceled-leave-still-appears-in-upcoming-time-off-on-people-workspace-441358"></a>已取消的休假仍然会在“人员”工作区上即将发生的休假中显示 (441358)

已取消休假不会再在**人员**工作区中的休假卡上显示为即将发生的休假。

## <a name="unable-to-use-the-department-entity-property-in-the-positionv2-entity-456486"></a>无法在 PositionV2 实体中使用部门实体属性 (456486)

现在，您可以添加部门而无需创建重复关系。

## <a name="payrollworkerenrolledbenefitdetailentity-should-only-use-calculated-field-for-retirement-plans-459779"></a>PayrollWorkerEnrolledBenefitDetailEntity 应该仅将计算字段用于退休计划 (459779)

导出 **PayrollWorkerEnrolledBenefitDetailEntity** 实体时，导出确定应使用基于比率表的计算字段还是使用后备表上的 **ContributionAmountCur** 字段。 数据实体使用的逻辑在应用程序通常不使用的情况下使用比率表。 此逻辑导致实体导出以为此列返回零值，因为没有计算比率表并且产品不允许客户指定比率表。
 
## <a name="confusing-translations-in-czech-language-in-personnel-management-and-employee-self-service-400276"></a>“人事管理”和“员工自助服务”中的捷克语翻译难以理解 (400276)

此版本更正了**公司目录**、**下一个注册的课程**、**工作**和**职位**的翻译。
 
## <a name="the-workcalendaremployment-table-doesnt-have-the-created-and-modified-system-fields-enabled-460171"></a>WorkCalendarEmployment 表未启用创建和修改的系统字段 (460171)

现在，在 Human Resources 中的 **WorkCalendarEmployment** 表中已启用创建和修改的系统字段。
 
## <a name="null-reference-exception-for-hire-and-add-details-for-future-employee-455475"></a>用于未来员工的“雇用并添加详细信息”的空引用异常 (455475)

此版本更正了当您使用**雇用并添加详细信息**选项雇用员工时，简化的员工输入中出现的错误（空引用）。

## <a name="changes-made-in-the-common-data-service-worker-entity-dont-reflect-in-human-resources-455652"></a>Common Data Service“工作人员”实体中所作的更改不反映在 Human Resources 中 (455652)

现在，在 Common Data Service 中对**工作人员**实体中的以下字段进行的更改将显示在 Human Resources 中：

- **在家办公**
- **受聘日期**
- **周年纪念日日期**
- **原始雇用日期**

## <a name="correct-compensation-level-doesnt-default-based-on-the-job-assigned-to-the-position-394136"></a>不能根据分配给职位的工作默认显示正确的薪酬级别 (394136)

进行此更改后，将根据**薪酬计划分配**的**职位详细信息**和**开始日期**的**生效日期**记录，默认显示正确的薪酬级别。

## <a name="in-preview"></a>预览模式

## <a name="mandatory-fields"></a>必填字段 

现在可使用 Human Resources 个性化功能将字段设置为必填字段。 此功能需要**保存的视图**。

## <a name="human-resources-application-in-teams"></a>Teams 中的 Human Resources 应用程序

员工可以在 Microsoft Teams 中查看和请求离岗时间。 他们可以与机器人交互来创建休假请求。 有关详细信息，请参阅 [Teams 中的 Human Resources 应用](https://go.microsoft.com/fwlink/?linkid=2127841)。 

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a>用于福利管理的数据管理框架 (DMF) 实体
 
福利管理实体即将发布。 DMF 实体允许导入和导出数据，以轻松配置福利管理。 福利管理模板可用于移动数据。 模板按顺序导出和导入数据，以保持数据依赖关系。

## <a name="buy-and-sell-leave"></a>购买和出售休假 

一些组织提供允许员工购买和出售其休假的福利。 此流程通常通过手动管理。 此功能可自动管理人力资源部门的策略和请求。 它将简化休假管理流程，并帮助消除错误。 有关详细信息，请参阅：

- [管理购买和出售休假策略](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [购买和出售休假](hr-employee-self-service-buy-sell-leave.md)

## <a name="leave-accrual-for-a-single-company-or-single-plan"></a>单个公司或单个计划的休假假期额度

客户可以处理单个公司或单个休假和缺勤计划的应计项目。 此功能为具有不同休假年限或休假应计政策的客户提供清晰的应计流程。 有关详细信息，请参阅[按公司或按休假计划累积休假](hr-leave-and-absence-accrue.md#accrue-leave-per-company-or-per-leave-plan)。

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

## <a name="checklist-entities-included-in-common-data-service"></a>Common Data Service 中包含的核对清单实体

Common Data Service 内很快将为入职、离职、转移和业务流程提供核对清单实体。

## <a name="see-also"></a>请参阅

[Human Resources 中新增或更改的功能](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2019 发布第 2 波概述](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[更新流程](hr-admin-setup-update-process.md)</br>
[管理功能](hr-admin-manage-features.md)
