---
title: 配置休假和缺勤类型
description: 在 Dynamics 365 Human Resources 中设置员工可以申请的休假类型。
author: andreabichsel
manager: AnnBe
ms.date: 06/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6e6ca7d04b86232ba48474fcbe288a18995661ae
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4417431"
---
# <a name="configure-leave-and-absence-types"></a>配置休假和缺勤类型

Dynamics 365 Human Resources 中的休假类型定义员工可报告的各种缺勤类型。 您可以根据组织的需求定制休假类型。 休假类型的示例包括：

- 带薪休息时间 (PTO)
- 无薪假
- 带薪假
- 病假
- 医疗休假
- 探亲假
- 短期残障
- 丧亲假

## <a name="add-a-leave-type"></a>添加休假类型

1. 在 **休假和缺勤** 页面，选择 **链接** 选项卡。

2. 在 **设置** 下，选择 **休假和缺勤类型**。

3. 选择 **新建**。

4. 在 **类型** 下输入休假类型的名称，从 **工作流 ID** 中选择一个工作流，然后在 **说明** 下输入说明。

5. 在 **一般** 中，从 **类别** 下拉列表中选择 **无**、**计划** 或 **计划外**。

6. 从 **收入代码** 下拉列表中选择一个收入代码。

7. 在 **需要原因代码** 下，选择您是否希望提供原因代码。 如果您希望提供原因代码，可能需要添加原因代码。 在 **原因代码** 下，选择 **添加**，选择一个原因代码，然后选择它旁边的 **已启用** 复选框。

8. 在 **限制对选定角色的访问** 下，选择是否要限制访问。 然后在 **此休假类型的安全角色** 下选择安全角色。 安全角色在您在此过程前面在 **工作流 ID** 下选择的工作流程中定义。

9. 在 **日历颜色** 下，选择该请假类型在请假和缺勤日历上显示的颜色。 

10. 在 **暂停关系** 下，选择是否要让此休假类型暂停其他休假类型或被其他休假类型暂停。 当提交休假请求以暂停休假类型时，将自动为暂停的休假类型创建休假暂停。 

10. 选择 **保存**。

## <a name="configure-leave-type-rules"></a>配置请假类型规则

1. 设置休假类型的舍入选项。 选项包括 **无**、**向上**、**向下** 和 **最近**。 您还可以为休假类型设置舍入精度。

2. 为休假类型设置 **假日更正**。 选择此选项时，Human Resources 将使用工作日的假日数来确定如何累积休假类型的休息时间。 例如，如果圣诞节在星期一，Human Resources 在处理累积时将从休假类型中减去一天。

   在工作时间日历中设置假日。 有关详细信息，请参阅[创建工作时间日历](hr-leave-and-absence-working-time-calendar.md)
   
 3. 为休假类型设置 **结转休假类型**。 选择此选项时，任何结转余额都将转移到指定的休假类型。 结转休假类型也需要包括在休假和缺勤计划中。 
 
 4. 为休假类型定义 **到期规则**。 配置此选项时，可以选择天或月单位并设置有效期限。 您还可以设置到期规则的生效日期。 到期时存在的任何休假余额将从休假类型中减去，并反映在休假余额中。 
 
 
## <a name="see-also"></a>请参阅

- [休假和缺勤概览](hr-leave-and-absence-overview.md)
- [创建休假和缺勤计划](hr-leave-and-absence-plans.md)
- [创建工作时间日历](hr-leave-and-absence-working-time-calendar.md)
- [暂停休假](hr-leave-and-absence-suspend-leave.md)

