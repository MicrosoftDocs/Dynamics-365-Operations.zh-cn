---
title: "薪酬计划"
description: "薪酬和福利经理可以使用薪酬管理来维护和处理组织的员工的固定薪酬计划和可变薪酬计划。"
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: HcmCompensationLevel, HRCCompGrid, HRMCompFixedAction, HRMCompFixedBudget, HRMCompFixedPlanTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: a6db69bcf9a26706174e56136696e970ec54ca8b
ms.contentlocale: zh-cn
ms.lasthandoff: 04/25/2017


---

# <a name="compensation-plans"></a>薪酬计划

[!include[banner](includes/banner.md)]


薪酬和福利经理可以使用薪酬管理来维护和处理组织的员工的固定薪酬计划和可变薪酬计划。

### <a name="introduction"></a>简介

薪酬管理用于控制基本工资和奖励的发放。 员工的固定基本工资和业绩调薪是通过固定薪酬计划控制的。 激励性的付款，例如额外津贴、绩效奖、股票期权和赠与以及一次性奖励，是通过可变薪酬计划控制的。 

员工可登记一个或多个这两种类型的计划。 员工必须满足以下要求以便符合在薪酬计划中登记的条件：
-   员工必须具有有效职位分配。
-   员工必须满足由薪酬计划资格规则定义的条件。

## <a name="compensation-setup"></a>薪酬设置
下表列出可整体设置贵公司的薪酬计划的薪酬过程的组成。

<table>
<thead>
<tr class="header">
<th>组件</th>
<th>更多信息…</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>固定薪酬操作</td>
<td>固定薪酬操作实现两个目的：
<ul>
<li>操作可以指定在员工薪酬更改时必须记录的信息种类。 例如，您可以要求记录更改（例如晋升或降级）的原因。</li>
<li>操作可以确保在处理固定薪酬计划时应用计算。  例如，类型“权益”的操作会将员工付薪与员工所在级别的最小参考点进行比较，并确保员工的工资至少为最小值。</li>
</ul></td>
</tr>
<tr class="even">
<td>级别</td>
<td>级别与工作以及作业引用有关的所有职位关联。 您可以为三个薪酬计划类型创建独立的级别：等级、分段或步幅。</td>
</tr>
<tr class="odd">
<td>幅度利用率矩阵</td>
<td>幅度利用率矩阵帮助您员工转移到其作业的控制点。 您还可以使用幅度利用率来控制公司内的付薪比率公正性，而与单独员工的绩效或公司的整体绩效无关。 例如，在其幅度内薪资低的员工比薪资高的员工获得更高的增长率。 以此种方式，您可以系统化地抵消股本差异。 按如下公式计算幅度利用率：（固定付薪比率 - 最小幅度）÷（最大幅度 - 最小幅度）。</td>
</tr>
<tr class="even">
<td>参考点设置</td>
<td>参考点设置包括在矩阵表中构成工资幅度的一组参考点。 每个幅度均可以与付薪比率关联。 例如，等级计划通常将具有最小、中间和最大参考点。</td>
</tr>
<tr class="odd">
<td>薪酬矩阵</td>
<td>薪酬矩阵是用于创建薪酬结构的一组参考点和级别。</td>
</tr>
<tr class="even">
<td>薪酬结构</td>
<td>薪酬结构是一个薪酬矩阵，其付薪比率与每个级别的参考点关联。</td>
</tr>
<tr class="odd">
<td>资格规则</td>
<td>资格规则用于标识特定作业、作业职能、作业类型、部门、工会或由特定薪酬计划覆盖的薪酬地区的员工。 您必须为可变和固定薪酬计划创建资格规则，以便在计划中登记员工。 指定薪酬计划的资格规则后，可以定义将要应用于计划所覆盖的工作的一组级别。</td>
</tr>
<tr class="even">
<td>付薪频率</td>
<td>付薪频率用于定义指定薪酬的时段。  例如，付薪频率帮助您理解薪酬金额是否指定为年薪与付薪比率。 付薪频率还用于设置换算系数以便将薪酬金额从按月、周、小时的付薪频率转换为按年的付薪频率。</td>
</tr>
<tr class="odd">
<td>薪酬地区</td>
<td>付薪区域基于工作地点的位置用于指定员工薪酬。</td>
</tr>
<tr class="even">
<td>控制点</td>
<td>该控制点定义您认为处于某一薪酬水平的所有员工的理想付薪比率是什么。 对于等级计划结构，控制点通常是范围的中点。 分段结构很少用于控制点。 您可以在“固定薪酬计划”窗体中指定固定薪酬计划的控制点。</td>
</tr>
<tr class="odd">
<td>工作职能</td>
<td>工作职能用于分类和筛选针对特定工作的薪酬计划。</td>
</tr>
<tr class="even">
<td>工作类型</td>
<td>工作类型用于分类和筛选针对特定工作的薪酬计划。</td>
</tr>
<tr class="odd">
<td>可变薪酬类型</td>
<td>在可变薪酬计划中设置可变薪酬类型（如股票奖励或现金奖励）。</td>
</tr>
<tr class="even">
<td>薪酬网格</td>
<td>薪酬网格包含薪酬结构。  薪酬网格可以由一个或多个薪酬计划使用。</td>
</tr>
<tr class="odd">
<td>绩效计划</td>
<td>绩效计划用于蒋性能与分配矩阵表进行关联，以便以按绩效付薪策略使用此计划。</td>
</tr>
<tr class="even">
<td>绩效等级</td>
<td>薪酬等级用于绩效计划中，以确定优异奖或绩效奖的金额。</td>
</tr>
</tbody>
</table>

## <a name="process-events"></a>流程事件
流程事件是用于计算特定期间在一个或多个固定或可变薪酬计划中登记的所有员工的薪酬信息。 可以重复运行流程事件以便测试或更新薪酬结果。

<a name="compensation-events"></a>薪酬事件
-------------------

每次运行流程事件时，都会创建一个薪酬事件。  薪酬事件包含该流程事件中包括的每个员工的薪酬流程的结果。  当计算正确时，您可以加载薪酬事件以更新受流程事件影响的员工的薪酬记录。

## <a name="recommendations"></a>建议
在运行流程事件后，可以建议基于流程事件的计算所得指导性对员工的调薪或奖励金额的调整。 若要向员工的建议，必须在您设置了薪酬计划或设置流程事件时启用建议。




