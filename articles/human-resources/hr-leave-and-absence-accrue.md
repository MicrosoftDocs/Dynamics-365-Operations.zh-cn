---
title: 应计休假和缺勤计划
description: 您可以在 Dynamics 365 Human Resources 中累积多个或单个员工的休假和缺勤。
author: andreabichsel
ms.date: 06/01/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 53c089da64f6b5f950a92afb9246454fb9a9686d
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5800253"
---
# <a name="accrue-leave-and-absence-plans"></a>应计休假和缺勤计划

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

您可以在 Dynamics 365 Human Resources 中累积多个或单个员工的休假和缺勤。

## <a name="accrue-leave-and-absence-for-multiple-employees"></a>累积多个员工的休假和缺勤

1. 在 **休假和缺勤** 页面，选择 **链接** 选项卡。

2. 在 **管理休假** 下，选择 **累积休假和缺勤计划**。

3. 将显示 **累积休假和缺勤计划** 对话框。 在 **累积截至** 中，选择 **今日日期**，或选择 **自定义日期** 并输入一个自定义日期。

4. 如果要为所有公司运行应计，请选择 **所有公司**。 如果要处理单个休假计划的应计，请为 **所有计划** 选择 **否**，然后选择 **休假计划**。 如果选择所有公司，则不能选择单个休假计划。 

5. 如果要在后台运行累积流程，请选择 **在后台运行** 并执行以下任务：

   1. 输入累积流程的信息。

   2. 要设置重复性作业，请选择 **重复**，输入重复信息，然后选择 **确定**。

   3. 要设置作业预警，请选择 **预警**，选择要接收的预警，然后选择 **确定**。

   4. 选择 **确定**。 累积流程将使用您设置的参数运行。

## <a name="accrue-leave-and-absence-for-an-employee"></a>累积一个员工的休假和缺勤

1. 在员工的记录上，选择 **休假**。

2. 选择 **累积休假和缺勤**。

3. 将显示 **累积休假和缺勤计划** 对话框。 在 **累积截至** 中，选择 **今日日期**，或选择 **自定义日期** 并输入一个自定义日期。

4. 如果要为所有公司运行应计，请选择 **所有公司**。 如果要处理单个休假计划的应计，请为 **所有计划** 选择 **否**，然后选择 **休假计划**。 如果选择所有公司，则不能选择单个休假计划。 

5. 如果要在后台运行累积流程，请选择 **在后台运行** 并执行以下任务：

   1. 输入累积流程的信息。

   2. 要设置重复性作业，请选择 **重复**，输入重复信息，然后选择 **确定**。

   3. 要设置作业预警，请选择 **预警**，选择要接收的预警，然后选择 **确定**。

   4. 选择 **确定**。 累积流程将使用您设置的参数运行。

## <a name="delete-leave-and-absence-accruals-for-multiple-employees"></a>删除多个员工的休假和缺勤累积

删除特定计划和日期范围的累积记录。 累积日期必须是今天或将来的日期。

1. 在 **休假和缺勤** 页面，选择 **链接** 选项卡。

2. 在 **管理休假** 下，选择 **删除休假和缺勤计划应计项目**。

3. 在 **删除休假和缺勤计划应计项目** 对话框中，选择 **休假计划**。 

4. 如果适合，选择 **删除余额调整**。

5. 输入或选择一个 **休假应计日期**。 这个日期必须是当天或在将来。 

6. 选择 **确定**。 累积流程将使用您设置的参数删除累积。 

## <a name="delete-leave-and-absence-accruals-for-a-single-employee"></a>删除一个员工的休假和缺勤累积

1. 在员工的记录上，选择 **休假**。

2. 选择 **删除休假和缺勤计划应计项目**。

3. 在 **删除休假和缺勤计划应计项目** 对话框中，选择 **休假计划**。 

4. 如果适合，选择 **删除余额调整**。

5. 输入或选择一个 **休假应计日期**。 这个日期必须是当天或在将来。 

6. 选择 **确定**。 累积流程将使用您设置的参数删除累积。 

## <a name="review-leave-accrual-and-deletion-processes"></a>检查休假累积和删除流程

每次运行或删除一个或多个员工的累积时，都将显示 **休假累积审核**。 还将显示执行操作的日期和人员。

1. 在 **休假和缺勤** 页面，选择 **链接** 选项卡。

2. 在 **管理休假** 下，选择 **删除休假累积审核**。

## <a name="see-also"></a>请参阅

[休假和缺勤概览](hr-leave-and-absence-overview.md)</br>
[创建休假和缺勤计划](hr-leave-and-absence-plans.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]