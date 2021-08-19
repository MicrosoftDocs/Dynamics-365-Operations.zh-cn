---
title: 配置休假和缺勤类型
description: 在 Dynamics 365 Human Resources 中设置员工可以申请的休假类型。
author: andreabichsel
ms.date: 07/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0ca474fe12867ae767db936ad0b2995c4437bdf0ee94831450fda825b9e075dc
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6730410"
---
# <a name="configure-leave-and-absence-types"></a>配置休假和缺勤类型

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

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
 
4. 为休假类型定义 **到期规则**。 配置此选项时，可以选择天或月单位并设置有效期限。 到期规则的生效日期用于确定何时开始运行处理休假到期或规则生效日期的批处理作业。 到期本身将始终发生在应计期间开始日期。 例如，如果应计期间开始日期为 2021 年 8 月 3 日，并且到期规则设置为 6 个月，则该规则将根据应计期间开始日期的到期偏移进行处理，因此它将在 2022 年 2 月 3 日执行。 到期时存在的任何休假余额将从休假类型中减去，并反映在休假余额中。
 
## <a name="configure-the-required-attachment-per-leave-type"></a>配置每个休假类型所需的附件

> [!NOTE]
> 要使用 **需要附件** 字段，您必须首先在功能管理中打开 **(预览)配置休假请求所需的附件** 功能。 有关如何打开预览功能的详细信息，请参阅[管理功能](hr-admin-manage-features.md)。

1. 在 **休假和缺勤** 页面，在 **链接** 选项卡上，在 **设置** 下，选择 **休假和缺勤类型**。

2. 在列表中选择休假和缺勤类型。 然后，在 **常规** 部分，使用 **需要附件** 字段指定当员工为所选休假类型提交新休假请求时是否必须上载附件。 

员工在提交假类型启用了 **需要附件** 字段的新休假请求时将需要上载附件。 要查看作为休假请求的一部分上载的附件，休假请求审批人可以对分配给他们的工作项使用 **附件** 选项。 如果使用 Microsoft Teams 中的 Human Resources 应用访问休假请求，可以使用休假请求的 **查看详细信息** 选项查看其详细信息和任何附件。

## <a name="configure-leave-units-hoursdays-per-leave-type"></a>配置每个休假类型的休假单位（小时/天）

> [!NOTE]
> 要使用每个休假类型的休假单位功能，您必须首先在功能管理中打开 **(预览)配置每个休假类型的休假单位** 功能。 有关如何打开预览功能的详细信息，请参阅[管理功能](hr-admin-manage-features.md)。

> [!IMPORTANT]
> 默认情况下，法人中的休假类型使用法人级别休假参数配置中的休假单位。
> 
> 仅当该休假类型没有休假交易时，才能修改休假和缺勤类型的休假单位。
> 
> 此功能打开后无法关闭。

1. 在 **休假和缺勤** 页面，在 **链接** 选项卡上，在 **设置** 下，选择 **休假和缺勤类型**。

2. 在列表中选择休假和缺勤类型。 然后，在 **常规** 部分，在 **单位** 字段中，选择休假单位。 您可以选择 **小时** 或 **天**。

3. 可选：如果您在 **单位** 字段中选择了 **小时**，您可以使用 **启用半天定义** 字段指定如果员工申请半天假期，是否可以选择上半天或下半天请假。

提交新休假请求的员工可以选择不同的休假类型来构建其休假请求。 但是，作为单个休假请求的一部分选择的所有休假类型应具有相同的休假单位。 员工可以在 **申请休假** 窗体中查看每个休假类型的休假单位。

## <a name="see-also"></a>请参阅

- [休假和缺勤概览](hr-leave-and-absence-overview.md)
- [创建休假和缺勤计划](hr-leave-and-absence-plans.md)
- [创建工作时间日历](hr-leave-and-absence-working-time-calendar.md)
- [暂停休假](hr-leave-and-absence-suspend-leave.md)
- [创建购买和出售休假请求工作流](hr-leave-and-absence-buy-sell-workflow.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
