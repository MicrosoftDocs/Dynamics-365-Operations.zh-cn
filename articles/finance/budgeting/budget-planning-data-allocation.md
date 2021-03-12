---
title: 预算计划数据分配
description: 本主题介绍 Microsoft Dynamics 365 Finance 中可用的分配方法以及如何使用它们。
author: ShylaThompson
manager: AnnBe
ms.date: 03/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BudgetPlanningConfiguration
audience: Application User
ms.reviewer: roschlom
ms.custom: 15191
ms.assetid: 89a918e8-59a4-4711-a2e9-b41989ddd0f1
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b07a0f59dfba1cc38133f0cc8ea02e0515f43443
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4971245"
---
# <a name="budget-planning-data-allocation"></a>预算计划数据分配

[!include [banner](../includes/banner.md)]

本主题介绍 Microsoft Dynamics 365 Finance 中可用的分配方法以及如何使用它们。  

您可以采用各种方式分配预算计划中的数据以准确地描述预计金额。

## <a name="allocation-methods"></a>分配方法
三种分配方法（“跨期分配”、“分配到维度”和“使用分类帐分配规则”）可创建基于同一预算计划中的行的预算计划行。 另外三种方法（“聚合”、“分配”和“从预算计划复制”）可创建其他预算计划中的预算计划行。 对于所有六种分配方法，您指定目标方案。 目标方案可以是与源方案相同或不相同的方案。 或者，您可以指定新行是否追加到预算计划或替换预算计划中的当前行。

> [!NOTE] 
> 应该对聚合使用不同于用于配送或父计划中之前执行的其他修改的方案的唯一方案。  

[![跨期分配分配方法](./media/allocateacrossperiods-300x259.png)](./media/allocateacrossperiods.png)
 **跨期分配** – 期间分配类别用于跨目标方案中的期间分配源预算计划方案中的预算计划行。 源金额将基于期间分配类别中定义的百分比和日期分配到目标方案中的多行。         

[![分配到维度分配方法](./media/allocatetodimensions.jpg)](./media/allocatetodimensions.jpg)
**分配到维度** – 预算计划行将基于所选预算期限中定义的百分比和财务维度从源预算计划方案中分配到目标方案中的一行或多行。           

![聚合图表](./media/aggregatechart-300x230.png)
**聚合** - 预算计划行将从关联（子）预算计划中的源预算计划方案中聚合到父预算计划的目标方案。 此方法使得在组织中较低级别准备的预算金额在较高级别处合并。          

[![分配图表](./media/distributechart-300x230.png)](./media/distributechart.png)
**分配** - 预算计划行将基于关联计划的组织单位的财务维度从父预算计划中的源预算计划方案分配到关联（子）预算计划中的目标方案。 此方法使得在组织中较高级别准备的预算金额进行分散以实现更本地化审核。           

[![分类帐分配规则](./media/ledgerallocationrules-300x202.png)](./media/ledgerallocationrules.png)
**使用分类帐分配规则** – 预算计划行将基于所选的分类帐分配规则从源预算计划方案中分配到目标方案。 

[![从预算计划复制](./media/copyfrombudgetplan-187x300.png)](./media/copyfrombudgetplan.png)
**从预算计划复制** – 正如“分配”分配方法中一样，预算计划行将基于相关预算计划中的行在目标方案中创建。 但是，对于此方法，源预算计划不必为父计划但可以是预算计划层次结构中的任何较高级别。 此分配方法在以下情况下有用：合并的金额最初在非常高级别处进行预算，而且必须先转移到组织的较低级别以实现详细审核和调整，然后金额才能收到父审批。          

## <a name="using-allocation-methods-in-a-budget-plan"></a>在预算计划中使用分配方法
要在预算计划页面上执行分配，请选择要分配的行，然后单击 **分配预算**。

[![分配预算按钮](./media/allocatebudgetbutton-300x84.png)](./media/allocatebudgetbutton.png) 

接下来，选择分配方法。 然后基于所选的方法设置剩余字段。 这些字段包含预算计划数据的源和目标以及一个选项，利用此选项，您可以在创建目标金额时用源乘以某个指定的系数，以便简化大量调整。 您还可以设置 **追加到计划** 选项。 选择 **否** 替换现有预算计划行，或者选择 **是** 保留现有预算计划行并为分配的金额添加新行。

## <a name="automating-allocations-during-a-workflow"></a>自动工作流期间的分配
一种强大的功能使得分配能够作为预算计划工作流中的一部分自动执行。 由于预算计划在其工作流中移动，因此自动化任务可在某个指定预算计划阶段中调用分配。 

要设置自动化分配，您必须先在 **预算计划配置** 页面上创建分配计划。 此分配计划定义在运行自动化分配时将使用的分配方法以及各种分配选项的值（请参阅上一部分中说明）。 

然后，在 **预算计划配置** 页面上创建阶段分配。 阶段分配会将分配计划分配到预算计划工作流和阶段。 

最后，在所需的工作流阶段处为预算计划阶段分配添加自动化任务。 在以下示例中，两个预算计划阶段分配（用红色标出）已插入到工作流中。

[![预算计划阶段分配](./media/budgetplanningstageallocations-300x300.png)](./media/budgetplanningstageallocations.png)



