---
title: Dynamics 365 Human Resources 的新增功能或更改（2020 年 8 月 6 日）
description: 此主题介绍了 2020 年 8 月 6 日 Microsoft Dynamics 365 Human Resources - Core HR 中的新增功能和更改的功能。
author: andreabichsel
ms.date: 08/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-08-06
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: a8058c1acdde20a1b48130fa1e8b75aa415bafce
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/04/2022
ms.locfileid: "8691965"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-august-06-2020"></a>Dynamics 365 Human Resources 的新增功能或更改（2020 年 8 月 6 日）

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



此主题介绍了 Dynamics 365 Human Resources 中的新增功能和更改的功能。 更改适用于内部版本号 8.1.3444。 某些标题中括号内的数字是 LCS 支持号码，供您参考。

## <a name="platform-update-1001236-is-now-available"></a>现已推出了平台更新 10.0.12(36)

有关详细信息，请参阅[财务和运营应用版本 10.0.12 的平台更新（2020 年 8 月）](../fin-ops-core/dev-itpro/get-started/whats-new-platform-update-10-0-12.md)。

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a>用于福利管理的数据管理框架 (DMF) 实体
 
福利管理实体即将发布。 DMF 实体允许导入和导出数据，以轻松配置福利管理。 福利管理模板可用于移动数据。 模板按顺序导出和导入数据，以保持数据依赖关系。 有关详细信息，请参阅：

- Dynamics 365 2020 年发行版本第 1 波计划中的 [DMF 实体支持](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/dmf-entity-support)
- [数据管理概览](../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md)


## <a name="claire-creates-a-workflow-for-buying-and-selling-leave-requests-446557"></a>Claire 创建用于买卖休假请求的工作流 (446557)

有关详细信息，请参阅：

- Dynamics 365 2020 年发行版本第 2 波计划中的[允许员工买卖休假](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/allow-employees-buy-sell-leave)
- [管理购买和出售休假策略](./hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [购买和出售休假](./hr-employee-self-service-buy-sell-leave.md)


## <a name="worker-postal-addresses-v2-entity-has-access-across-legal-entities-with-restricted-access-459126"></a>工作人员邮寄地址 V2 实体可以访问访问受限的法人实体 (459126)

通过此更改，**工作人员邮寄地址 V2** 实体将基于授予用户的法人访问权限受到限制。

## <a name="workflow-email-hyperlink-fails-to-open-relevant-reviews-437398"></a>工作流电子邮件超链接无法打开相关审核 (437398)

当您使用占位符在审核工作流中打开绩效审核时，电子邮件中生成的超链接现在会打开所选记录。

## <a name="new-entities-for-buying-and-selling-leave-473180"></a>可以买卖休假的新实体 (473180)

数据管理框架实体现在可用于买卖休假。 有关详细信息，请参阅[数据管理概述](../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md)。

## <a name="when-viewing-record-information-and-using-advanced-filters-a-user-could-gain-access-to-other-employees-records-472490"></a>查看记录信息和使用高级筛选器时，用户可以访问其他员工的记录 (472490)

通过此更改，员工自助服务用户只能在使用员工自助服务时访问自己的记录。 在更改筛选选项时查看记录信息将不再公开其他数据。

## <a name="personnel-management-analytics-include-exited-worker-records-382893"></a>人事管理分析包含已离职工作人员的记录 (382893)

在此版本中，人事管理分析现在仅包括有效工作人员。 
 
## <a name="unable-to-process-a-merit-increase-for-an-employee-473125"></a>无法处理员工的业绩调薪 (473125)

此更改使您可以在更改新业绩调薪的生效日期时输入业绩调薪。

## <a name="review-workflow-can-be-started-more-than-once-467541"></a>审核工作流可能多次开始 (467541)

进行此更改后，您只能开始一次绩效审核工作流。 经理的状态不再显示开始审核的选项。

## <a name="leave-request-work-flow-ends-in-error-when-canceling-an-approved-leave-request-472063"></a>取消批准的休假请求时，休假请求工作流会错误地结束 (472063)

在此版本中，当您取消批准的休假请求时，请求的状态将不再保持批准状态，工作流将继续。

## <a name="system-suggests-exited-workers-when-creating-a-new-review-form-the-template-460624"></a>从模板创建新审核窗体时系统建议已离职的工作人员 (460624)

通过此更改，从模板创建新审核时，离职工作人员将不再可用。 您无法为雇用日期之外的员工创建审核。

## <a name="position-hierarchy-circular-reference-detection-415879"></a>职位层次结构循环引用检测 (415879)

通过此更改，职位层次结构循环引用检测仅限于单个时间点。 您可以针对不同日期运行循环引用检测，以验证报告结构中没有任何循环引用。

## <a name="buy-and-sell-leave"></a>购买和出售休假 

一些组织提供允许员工购买和出售其休假的福利。 此流程通常通过手动管理。 此功能可自动管理人力资源部门的策略和请求。 它将简化休假管理流程，并帮助消除错误。 有关详细信息，请参阅：

- Dynamics 365 2020 年发行版本第 2 波计划中的[允许员工买卖休假](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/allow-employees-buy-sell-leave)
- [管理购买和出售休假策略](./hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [购买和出售休假](./hr-employee-self-service-buy-sell-leave.md)

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

## <a name="in-preview"></a>预览模式

### <a name="mandatory-fields"></a>必填字段

您可以使用 Human Resources 个性化功能将字段设置为必填字段。 此功能需要 **保存的视图**。 有关已保存视图的详细信息，请参阅：

- Dynamics 365 2020 年发行版本第 2 波计划中的[已保存视图 - 正式发布](/dynamics365-release-plan/2020wave2/finance-operations/finance-operations-crossapp-capabilities/saved-views--general-availability)
- [生成可充分利用已保存视图的窗体](../fin-ops-core/dev-itpro/user-interface/understanding-saved-views.md)

### <a name="human-resources-application-in-teams"></a>Teams 中的 Human Resources 应用程序

员工可以在 Microsoft Teams 中查看和请求离岗时间。 他们可以与机器人交互来创建休假请求。 有关详细信息，请参阅：

- Dynamics 365 2020 年发行版本第 1 波计划中的 [Microsoft Teams 中的员工休假和缺勤体验](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams)
- [Teams 中的 Human Resources 应用](./hr-admin-teams-leave-app.md)

### <a name="dmf-entity-available-for-accrual-suspensions"></a>可用于暂停应计的 DMF 实体

DMF 实体现在可用于暂停应计。

## <a name="coming-soon"></a>即将到期

## <a name="checklist-entities-included-in-dataverse"></a>Dataverse 中包含的核对清单实体

Dataverse 内很快将为入职、离职、转移和业务流程提供核对清单实体。

## <a name="known-issues"></a>已知问题

**功能管理** 工作区可能会显示正式发布时被作为预览功能禁用的功能。 以下是显示错误状态的正式发布功能的列表。 

1.  福利管理
2.  案例管理
3.  数据库日志记录(审核)
4.  单个公司或单个计划的休假假期额度
5.  休假和缺勤假期额度记录暂停
6.  余额调整原因代码和注释
7.  购买和出售休假
8.  休假和缺勤日历
9.  休假结转规则
10. 休假假期额度记录审核
11. 休假假期额度记录删除
12. 休假假期额度记录舍入
13. 在单个休假计划上配置多个休假类型
14. 更新请假增强功能
15. 将员工的全职人力工时用于假期额度记录
16. 跨公司薪酬视图
17. 打印绩效复查
18. 休假假期额度记录节假日更正

## <a name="see-also"></a>请参阅

[Human Resources 中新增或更改的功能](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2019 发布第 2 波概述](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[更新流程](hr-admin-setup-update-process.md)</br>
[管理功能](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]