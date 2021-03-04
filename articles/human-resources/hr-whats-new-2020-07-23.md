---
title: Dynamics 365 Human Resources 的新增功能或更改（2020 年 7 月 23 日）
description: 此主题介绍了 2020 年 7 月 23 日 Microsoft Dynamics 365 Human Resources - Core HR 中的新增功能和更改的功能。
author: Darinkramer
manager: AnnBe
ms.date: 07/23/2020
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
ms.search.validFrom: 2020-07-23
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d0672e3039f54a4591db49eee00d69bf5e4278fd
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/17/2020
ms.locfileid: "4528441"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-july-23-2020"></a>Dynamics 365 Human Resources 的新增功能或更改（2020 年 7 月 23 日）

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

此主题介绍了 Dynamics 365 Human Resources 中的新增功能和更改的功能。 更改适用于内部版本号 8.1.3416。 某些标题中括号内的数字是 LCS 支持号码，供您参考。

## <a name="deleting-financial-dimensions-on-a-position-doesnt-work-as-expected-445476"></a>在位置上删除财务维度不能按预期进行 (445476)

现在，从某个位置删除维度会从 Common Data Service 中删除这些相同的位置。

## <a name="positions-not-in-hierarchy-show-inactive-positions-397257"></a>不在层次结构中的位置显示无效职位 (397257)

无效的位置（持续时间已过）将不再在位置层次结构中显示为 **不在层次结构中的位置**。 

## <a name="validation-occurring-between-leaveenrollmententity-and-hcmworkerentity-on-data-management-framework-dmf-import-causes-slow-data-loads-442324"></a>在数据管理框架 (DMF) 导入时在 LeaveEnrollmentEntity 和 HcmWorkerEntity 之间进行的验证导致数据加载缓慢 (442324)

此版本中的更改提高了 **LeaveEnrollmentEntity** 的性能。

## <a name="unable-to-personalize-in-organization-administration-447490"></a>无法在“组织管理”中个性化 (447490)

进行此更改后，您现在可以在 **组织管理** 中个性化链接。

## <a name="in-preview"></a>预览模式

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

## <a name="checklist-entities-included-in-common-data-service"></a>Common Data Service 中包含的核对清单实体

Common Data Service 内很快将为入职、离职、转移和业务流程提供核对清单实体。

## <a name="platform-changes"></a>平台变更

平台更新 10.0.12 (36)

## <a name="see-also"></a>请参阅

[Human Resources 中新增或更改的功能](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2019 发布第 2 波概述](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[更新流程](hr-admin-setup-update-process.md)</br>
[管理功能](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]