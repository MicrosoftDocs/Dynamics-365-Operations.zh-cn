---
title: Dynamics 365 Human Resources（2020 年 6 月 11 日）新增功能或更改
description: 此主题介绍了 2020 年 6 月 11 日 Microsoft Dynamics 365 Human Resources - Core HR 中的新增功能和更改的功能。
author: andreabichsel
ms.date: 06/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-06-11
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 9d75c4a27ff98f52fff6ec498aded4dfcc031931
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/04/2022
ms.locfileid: "8695779"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-june-11-2020"></a>Dynamics 365 Human Resources（2020 年 6 月 11 日）新增功能或更改

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

本文介绍 Dynamics 365 Human Resources 中的新增功能或更改的功能。 更改适用于内部版本号 8.1.3316。 某些标题中括号内的数字是 LCS 支持号码，供您参考。

## <a name="streamlined-employee-form-sometimes-causes-child-form-close-x-buttons-to-stop-working-442369"></a>简化的员工窗体有时导致子窗体关闭 (X) 按钮停止工作 (442369)

当新的 **工作人员** 窗体启用后，关闭 (**X**) 按钮有时对子窗体不起作用。 此问题是间歇性的。 您可以在离开然后返回窗体后关闭窗体。 例如，您可以选择左侧的菜单项，然后导航回 **工作人员** 窗体将其关闭。 本周的发布将解决此问题。 

## <a name="the-worker-personal-contact-person-entity-doesnt-export-personal-contacts-with-a-parent-relationship-type"></a>工作人员个人联系人实体不能导出具有父关系类型的个人联系人

通过此发布，**工作人员个人联系人** 实体可以导出所有关系类型。

## <a name="the-hcmpositionworkerassignmentv2entity-should-be-part-of-the-ceridian-payroll-integration-package-by-default-448506"></a>默认情况下，HcmPositionWorkerAssignmentV2Entity 应该是 Ceridian 工资单集成包的一部分 (448506)

通过此更改，**HcmPositionWorkerAssignmentV2Entity** 将包含在 Ceridian 工资单集成包中。

## <a name="in-preview"></a>预览模式

## <a name="database-logging"></a>数据库记录

数据库日志记录功能让您可以确定要监视哪些表和字段。 它还让您能够确定应该触发更改跟踪的事件。 您可以使用数据库日志记录功能来查看一段时间内的更改。 有关详细信息，请参阅[配置和管理数据库日志记录](hr-admin-database-logging.md)。

## <a name="human-resources-application-in-teams"></a>Teams 中的 Human Resources 应用程序

员工可以在 Microsoft Teams 中查看和请求离岗时间。 他们可以与机器人交互来创建休假请求。 有关详细信息，请参阅 [Teams 中的 Human Resources 应用](./hr-admin-teams-leave-app.md)。 

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

## <a name="new-platform-capabilities"></a>新平台功能 

您将可以通过使用个性化将字段设为必填字段。 此功能需要您启用 **已保存视图**。

## <a name="configure-the-name-of-employee-self-service"></a>配置员工自助服务的名称

人力资源参数中将提供一个新选项，可以将“员工自助服务”工作区的名称更新为“自助服务”。 

## <a name="see-also"></a>请参阅

[Human Resources 中新增或更改的功能](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2019 发布第 2 波概述](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[更新流程](hr-admin-setup-update-process.md)</br>
[管理功能](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]