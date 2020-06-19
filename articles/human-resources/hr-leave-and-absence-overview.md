---
title: 概览
description: 在 Dynamics 365 Human Resources 中，休假和缺勤工作区提供用于创建新休假计划的灵活框架、管理请求的工作流，以及供员工请求休息时间的直观自助服务页面。
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
ms.openlocfilehash: ec72d2d741f7f8428a7daa97bb982e9fc00b8c3f
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/04/2020
ms.locfileid: "3428959"
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

- [申请休假](hr-employee-self-service-request-time-off.md)
- [管理休假和缺勤申请](hr-employee-self-service-manage-requests.md)

## <a name="leave-and-absence-known-issues"></a>休假和缺勤已知问题

### <a name="rounding-precision"></a>舍入精度

设置**化整类型**时不能设置**化整精度**。 只能通过使用**休假和缺勤类型**实体设置**化整精度**。 

1. 从**休假和缺勤类型**选择**在 Excel 中打开**以打开**休假和缺勤类型**实体。

2. 打开并启用文件后，选择**设计**。

3. 在**休假和缺勤类型**表中，选择铅笔选项进行编辑。

4. 选择**化整精度**和**化整类型**，然后选择**添加**添加到字段列表。

5. 选择**更新**，然后选择**完成**。

6. 为各种休假类型输入或选择**化整类型**（如果尚未设置）。 

7. 为相应类型输入**化整精度**。

8. 选择**发布**将更改推送到 Human Resources 中。

## <a name="leave-and-absence-preview-features"></a>休假和缺勤预览功能

您可以在**沙盒**环境中试用新的休假和缺勤预览功能。 有关打开预览功能的信息，请参阅[管理功能](hr-admin-manage-features.md)。 

[!include [banner](includes/preview-feature.md)]

预览功能包括：

- **按公司或计划的休假应计** - 您可以对所有公司或单个公司运行应计流程。 您还可以对特定公司的特定休假和缺勤计划运行应计流程。 

- **购买休假** - 您可以为员工提交购买请求启用和创建购买休假政策。 员工可以提交购买请求，并让余额自动更新来反映请求。  

- **向批准的休假请求添加附件** - 您可以将附件添加到已经批准的休假请求中。 

