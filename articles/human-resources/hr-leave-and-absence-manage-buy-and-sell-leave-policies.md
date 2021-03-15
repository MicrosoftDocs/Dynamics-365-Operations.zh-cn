---
title: 管理购买和出售休假策略
description: 您可以在 Dynamics 365 Human Resources 中让员工可以购买和出售休假。
author: andreabichsel
manager: tfehr
ms.date: 08/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: LeaveBuySellPolicy, LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-06-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 89563204cf1423ddce47d7bacace8f14edf87005
ms.sourcegitcommit: 18e626c49ccfdb12c1484b985e3a275e51f61320
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/04/2021
ms.locfileid: "5115988"
---
# <a name="manage-buy-and-sell-leave-policies"></a>管理购买和出售休假策略

您可以通过创建购买和出售休假策略使员工能够购买和出售休假。 您可以配置这些策略来使用审批工作流、设置最大金额和费率以及设置购买和出售费率。 

## <a name="enable-employees-to-buy-and-sell-leave"></a>让员工可以购买和出售休假

1. 在 **休假和缺勤参数** 页面上，为 **允许员工购买休假** 和 **允许员工出售休假** 选择 **是**。

## <a name="create-a-buy-and-sell-leave-policy"></a>创建购买和出售休假策略

1. 在 **休假和缺勤** 页面，选择 **链接** 选项卡。 

2. 选择 **购买和出售休假策略**。

3. 选择 **新建**。

4. 在 **购买和出售休假策略** 下为策略输入 **名称** 和 **描述**。 

5. 选择 **策略类型**。 

   可用策略类型为 **金额** 和 **每周工时**。 选择 **金额** 为员工可以购买和出售的最大金额输入 **固定金额**。 如果选择 **每周工时**，在员工的分配工作时间日历中定义的工作时间用于确定策略的最大金额。 

6. 为策略选择 **开始日期** 和 **结束日期**。 购买和出售休假的请求只能在此时间范围内提交。 

7. 为策略选择一个 **工作流 ID**。 任何购买和出售请求都将使用此工作流进行审核和审批。 

8. 在 **购买策略** 下，选择 **全职等效** (FTE)，根据在员工职位中定义的 FTE 按比例分配最大金额。 如果策略类型是 **金额**，请输入 **最大固定金额**。 

9. 选择 **添加** 为员工购买休假添加休假类型。 您可以向策略添加多个休假类型。 

10. 为休假类型输入 **服务月数**，可以通过不同的服务月数确定员工可以购买的最大金额。 

11. 为休假类型输入 **最大金额**。 

12. 输入员工购买休假所使用的 **费率**。 

13. （可选）输入用于购买休假的 **收入代码**。 

14. （可选）设置是否使用 FTE 确定休假类型的最大金额。 

15. 要创建出售策略，请按照 **出售策略** 下的步骤 8 到 14 操作。 

## <a name="add-the-buy-and-sell-leave-policy-to-a-leave-and-absence-plan"></a>将购买和出售休假策略添加到休假和缺勤计划中

1. 在 **休假和缺勤** 页面上，选择一个休假和缺勤计划。

2. 在 **规则** 下，选择 **购买和出售休假策略**。

## <a name="see-also"></a>请参阅

[休假和缺勤概览](hr-leave-and-absence-overview.md)</br>
[配置休假和缺勤类型](hr-leave-and-absence-types.md)</br>
[应计休假和缺勤计划](hr-leave-and-absence-accrue.md)</br>
[购买和出售休假](hr-employee-self-service-buy-sell-leave.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]