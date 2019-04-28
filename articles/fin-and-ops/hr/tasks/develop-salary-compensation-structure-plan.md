---
title: 制订薪水/薪酬结构和计划
description: 此任务指南将介绍创建固定薪酬计划的流程，以及通过资格规则筛选加入薪资计划的员工。
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, HcmCompensationWorkspace, HcmCompFixedPlansPart, HRMCompFixedPlanTable, HRMCompCreateGridDialog, HRCCompGridView, HRMCompEligibility,  HRCCompGrid
audience: Application User
ms.reviewer: anbichsea
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4e3b71e679539441b90f399a84ad8ef8d3decf19
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/19/2019
ms.locfileid: "859405"
---
# <a name="develop-salarycompensation-structure-and-plan"></a>制订薪水/薪酬结构和计划

[!include [task guide banner](../../includes/task-guide-banner.md)]

此任务指南将介绍创建固定薪酬计划的流程，以及通过资格规则筛选加入薪资计划的员工。 创建此任务的演示数据公司是 USMF，此任务专门面向薪酬和福利经理。


## <a name="create-fixed-compensation-plan"></a>创建固定薪酬计划
1. 单击“薪酬管理”。
2. 单击“固定薪酬计划”。
3. 单击“新建”。
4. 在“计划”字段中，输入一个值。
5. 在“描述”字段中，键入一个值。
6. 在“有效日期”字段中，输入日期。
7. 在“类型”字段中，选择固定薪酬计划为分段、级别还是步骤计划。
8. “推荐”允许复选框作为流程事件中添加到此计划的所有行动的默认值。  允许“推荐”让您在处理薪酬时覆盖计算出的指导性金额。
9. “容差范围”允许您决定如何处理，下降到给定薪酬结构范围之外的的薪酬金额。   “无容差范围”将允许使用任何薪酬金额。  若薪酬金额低于该等级的最小参考点金额，或高于该等级的最大参考点金额，“虚拟容差”将向用户发出警告。 用户可以忽略该警告并继续。  如果一员工的薪酬在该级别最低和最高参考范围之外，且在可用范围内自动调整员工薪酬失败，则“硬容差”将产生错误。
10. 若运行薪酬处理事件计算员工薪酬，则需使用“雇用规则”字段。   百分比雇用规则将计算，在雇佣周期内，工人增加时长比例。
11. 在“货币”字段中，键入一个值。
12. 在“付薪比率转换”字段中，输入或选择一个值。
13. 展开“幅度利用率矩阵”部分。
    * 或者，添加幅度利用记录，使员工可以快速获取中间值，但较慢获得最大范围。  
14. 此时，您在保存固定薪酬计划后，才可启用“设置薪酬”按钮，定义您的计划的薪酬结构。  单击“保存”。
15. 单击“设置薪酬”。
    * 创建薪酬结构有三种方法。 1：通过选择一组参考点并添加级别，创建一个您自己的全新的结构。 2：首先复制现有计划的薪酬结构并对其进行修改，已完成新的计划。 3：必须选择现有薪酬网格。 如果其他计划已使用薪酬网格，那么对网格进行更改，也将反映在其他计划中。  
16. 选中“根据现有薪酬矩阵创建新表格”选项。
17. 在“从网格复制”字段中，输入或选择一个值。
    * 或者您可以更改从所选网格复制而来的，新建的薪酬网格的名称。  
18. 单击“确定”。
19. 单击“批量更改”。
    * 批次更改允许您通过应用一个或更多级别和/或参考点的合并百分比或金额的增加，来维护薪酬矩阵金额。  
20. 在“调整金额”字段中，输入一个数值。
21. 在列表中，标记或取消标记所有行。
22. 单击“应用于网格”。
23. 关闭该页面。
    * 一旦薪酬结构被创建或选择，您将可以选择使用哪一个参考点作为固定薪酬计划的控制点。  控制点用于计算员工的比较比率。  
24. 在“控制点”字段中，输入或选择一个值。
25. 关闭该页面。

## <a name="create-an-eligibility-rule-for-the-new-fixed-compensation-plan"></a>为此新固定薪酬计划创建资格规则。
    * 只有在该计划已定义资格规则后，新固定薪酬计划才能分配给员工。  
1. 单击“资格规则”。
2. 单击“新建”。
3. 在“资格”字段中，输入一个值。
4. 在“描述”字段中，键入一个值。
5. 在“有效日期”字段中，输入日期。
    * 资格规则适用于固定薪酬计划和可变薪酬计划。  在“类型”字段中，选择此资格规则适用于哪种计划类型。  
6. 在“计划”字段中，输入或选择一个值。
    * 选择员工符合薪酬计划所需满足的条件。 标准包括部门、工会、位置（薪酬区域）、工作、职能、工作类型或薪酬水平。 员工必须满足所有指定条件才能符合薪酬计划。 如果未指定条件，则所有员工符合薪酬计划。 如果员工不满足指定的资格规则，或薪酬计划并未指定资格规则，那么在创建员工固定薪酬记录时，查找中将不会出现薪酬计划。  
7. 关闭该页面。
8. 关闭该页面。

