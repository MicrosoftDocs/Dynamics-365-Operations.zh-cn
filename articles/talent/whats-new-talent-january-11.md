---
title: Dynamics 365 for Talent Core HR（2019 年 1 月 11 日）中的新增功能或更改
description: 此主题介绍了 Microsoft Dynamics 365 for Talent Core HR 中的新增功能和更改的功能。
author: Darinkramer
manager: AnnBe
ms.date: 01/11/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-01-11
ms.dyn365.ops.version: Talent
ms.openlocfilehash: e6a89ba455acbed9724da6826ac4d41c6a481490
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/19/2019
ms.locfileid: "856130"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-january-11-2019"></a>Dynamics 365 for Talent Core HR（2019 年 1 月 11 日）中的新增功能或更改

[!include [banner](includes/banner.md)]

**内部版本 8.1.2100**

此主题介绍了 Core HR 中的新增功能和更改的功能。

## <a name="changes"></a>更改

### <a name="validate-leave-requests-by-forecasting-available-balance"></a>通过预测可用余额验证休假请求
在此版本中所做的更改允许员工请求未来的休假，而不减少当前余额。 标准工作流将用于发起的所有未来请求。 有关详细信息，请阅读[根据工作时数累积休假时间](leave-accrue-hours-worked.md)。

### <a name="view-forecasted-leave-balance-in-ess-and-people"></a>查看 ESS 和“人员”中的预测休假余额
此功能支持按人力资源、经理和员工查看将来休假期间的余额。 员工可以在**员工自助服务**工作区中查看将来的余额，HR 有权使用**人员**工作区访问相同信息。

### <a name="notifications-for-changing-leave-balances"></a>更改休假余额的通知
休假余额将显示员工的当前余额。 将来余额可以通过输入“截止日期”计算预测余额在**员工自助服务**和**人员**工作区提供。

已在以下区域添加查看预测余额的导航：
  - **员工自助服务**工作区的**休假**卡。
  - **经理自助服务**工作区的**休假和缺勤**卡。
  - **人员**工作区的**休假和缺勤**页。

### <a name="allow-decimals-for-variable-compensation-plans-cash-plans"></a>允许可变薪酬计划（现金计划）有小数位
可变现金奖励和计划现在对有小数金额的值有更多的金额和覆盖灵活性。

### <a name="unable-to-change-the-dates-on-variable-comp-enrollments-after-the-plan-is-saved"></a>在保存计划后无法更改可变薪酬登记的日期
此更改允许在保存计划后更新计划结束日期（延长或到期）。 您仍然可以启用或停用与开始日期和结束日期无关的计划。

### <a name="payroll-information-available-when-assigned-the-payroll-admin-security-role"></a>工资单信息在分配了工资管理员安全角色时可用
工资管理员角色已更新，可以在请求过程中访问工资单信息。

### <a name="employee-self-service--position-hierarchy-drill-down-from-tile-fails-to-get-parent-node"></a>从磁贴深化的员工自助服务 | 职位层次结构无法获取父节点
已进行更改以清除在向新工作区添加职位层次结构和在组织结构内导航时发生的错误。

### <a name="new-validation-message-when-personnel-number-sequence-is-in-use"></a>人员编号规则正在使用时的新验证消息
已进行更改以澄清当您雇用员工且下一个人员编号正在使用时的问题。

### <a name="employee-self-service-workspace-selected-as-the-initial-startup-page"></a>选择作为初始启动页的员工自助服务工作区
在**员工自助服务**工作区被选择作为用户的初始启动页且该用户未被分配员工角色时，系统将重定向到默认仪表板。

### <a name="termination-reason-code-updates-position-assignment-record"></a>终止原因代码更新职位分配记录
终止原因代码现在将在终止雇用员工和结束职位时更新职位分配。 
