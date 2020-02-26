---
title: 概览
description: ''
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 9a36f6b6ba696fa926ab3d6298568dddfce43a57
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008264"
---
# <a name="overview"></a>概览

Dynamics 365 Human Resources 帮助您向工作人员提供出色的休假福利。 **休假和缺勤**工作区提供用于创建新休假计划的灵活框架、管理请求的工作流，以及供员工请求休息时间的直观自助服务页面。 分析可以帮助您的组织衡量和监控休假计划的休假余额和使用情况。

## <a name="set-up-leave-and-absence"></a>设置休假和缺勤

您需要先执行一些设置步骤，然后才能为员工创建休假计划：

- [配置休假和缺勤参数](hr-leave-and-absence-parameters.md)
- [创建工作时间日历](hr-leave-and-absence-working-time-calendar.md)
- [创建休假申请工作流](hr-leave-and-absence-workflow.md)

## <a name="create-and-manage-leave-plans"></a>创建和管理休假计划

在为员工创建休假计划之前，您需要创建休假和缺勤类型。 创建休假计划后，可以将工作人员登记到计划中。 您还可以运行累积流程、创建提醒以及查看计划的分析。

- [配置休假和缺勤类型](hr-leave-and-absence-types.md)
- [创建休假和缺勤计划](hr-leave-and-absence-plans.md)
- [将工作人员分配给休假计划](hr-leave-and-absence-enroll.md)
- [累积休假和缺勤计划](hr-leave-and-absence-accrue.md)
- [查看休假和缺勤分析](hr-leave-and-absence-analytics.md)

## <a name="request-time-off-and-manage-requests"></a>请求休息时间和管理请求

您的员工可以提交休息时间请求，您可以在**员工自助服务**工作区进行管理。

- [请求休息时间](hr-employee-self-service-request-time-off.md)
- [管理休假和缺勤请求](hr-employee-self-service-manage-requests.md)

## <a name="leave-and-absence-preview-features"></a>休假和缺勤预览功能

您可以在**沙盒**环境中试用新的休假和缺勤预览功能。 有关打开预览功能的信息，请参阅[管理功能](hr-admin-manage-features.md)。 预览功能包括：

- **休假和缺勤日历** - 休假和缺勤参数将从**人力资源参数**转到一个名为**休假和缺勤参数**的新屏幕。 新屏幕包括一个新的**日历**选项卡。此预览仅启用一部分参数。 您可以从**休假和缺勤**工作区的**链接**选项卡访问新屏幕。 日历包括：
  - **公司日历** - 显示所有员工的休息时间请求。 具有**人力资源**角色的人员可以从**休假和缺勤**工作区的**链接**选项卡访问此日历。
  - **经理团队日历** - 显示所有直接下属的休息时间请求。 经理可以从**休假和缺勤**下员工自助服务中的**我的团队**选项卡访问此日历。 

- **休假和缺勤假日日历** - 休假类型包括新的**假日**选项，与工作时间日历结合使用。 在生成工作日时，由假日和歇业定义的天现在指定为**假日**。 处理应计时，将对分配到日历的员工进行调整，以考虑工作日的假日。

- **休假应计审计** - 一个新屏幕，您可以查看所有员工和单个员工何时处理和删除了应计。 您可以从**休假和缺勤**工作区的**链接**选项卡访问此新屏幕。

- **休假应计删除** - 您现在可以删除特定休假计划的应计记录。 您可以从**休假和缺勤**工作区的**链接**选项卡访问此新选项。 对于单独员工，此选项显示在员工资料中的**休假和缺勤**分组中。 

- **休假应计舍入** - **休假类型**定义应使用哪种类型的舍入应计，以及应计过程中舍入的小数精度的新选项。 处理应计时，将对应计记录应用此舍入和精度。 

- **在单个休假计划上配置多个休假类型** - 休假类型的休假应计计划中的新列，使您可以在具有不同应计计划的休假和缺勤计划上定义多个休假类型。 以前的**休假类型**字段已删除。 现在，在员工登记中，休假类型的余额显示在表中，而不是在屏幕顶部。

  > [!IMPORTANT]
  > 此功能启用后，将无法关闭。

- **使用员工的全职等效 (FTE) 进行应计** - 休假应计计划上的新列，允许使用 FTE 进行应计。 处理应计时，应用程序将使用员工的主要职位和定义的 FTE 来确定按比例分配的应计金额。

  > [!NOTE]
  > 此功能仅在启用**为每个休假计划配置多个休假类型**后可用。 
