---
title: 应计休假和缺勤计划
description: 您可以在 Dynamics 365 Human Resources 中累积多个或单个员工的休假和缺勤。
author: andreabichsel
ms.date: 05/04/2020
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
ms.openlocfilehash: 8c0ab67517d9efdc59f3d1b1ea9405f08dbab5c636322758cab761ecd5481681
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6755442"
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
    2. 要设置定期作业，选择 **定期**，输入定期信息，然后选择 **确定**。
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

## <a name="leave-accrual-transaction-auditing"></a>休假应计交易记录审计

此功能可帮助休假和缺勤管理人员了解与特定休假类型的员工休息时间余额相关的休假和缺勤应计交易。

查看交易详细信息：

1. 在员工的记录上，选择 **休假**。

2. 选择 **查看休息时间**，然后选择 **余额** 选项卡。

要查看与特定休假类型相关的应计交易，选择 **当前余额** 列中的数值。

要查看特定应计金额的交易详细信息，选择一个应计行，打开右侧的 **相关信息** 面板，然后打开 **交易详细信息** 部分。 “交易详细信息”部分显示：

- 员工休假类型余额的更改
- 指定应计期间的雇用详细信息
- 有关应计期间和费率的详细信息
- 对休假计划配置所作的任何更改

![显示休假应计交易审计。](media/hr-leave-and-absence-accrue-audit.png)

## <a name="see-also"></a>请参阅

[休假和缺勤概览](hr-leave-and-absence-overview.md)</br>
[创建休假和缺勤计划](hr-leave-and-absence-plans.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
