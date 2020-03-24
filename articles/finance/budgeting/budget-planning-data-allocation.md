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
ms.search.scope: Core, Operations
ms.custom: 15191
ms.assetid: 89a918e8-59a4-4711-a2e9-b41989ddd0f1
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ceddeda5760d961568d58e7e4805955ea972c586
ms.sourcegitcommit: 8fad5a8c7ea5d0d0037669e61e2313f684bcae23
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/06/2020
ms.locfileid: "3106874"
---
# <a name="budget-planning-data-allocation"></a><span data-ttu-id="608d1-103">预算计划数据分配</span><span class="sxs-lookup"><span data-stu-id="608d1-103">Budget planning data allocation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="608d1-104">本主题介绍 Microsoft Dynamics 365 Finance 中可用的分配方法以及如何使用它们。</span><span class="sxs-lookup"><span data-stu-id="608d1-104">This topic describes the allocation methods that are available in Microsoft Dynamics 365 Finance and how they can be used.</span></span>  

<span data-ttu-id="608d1-105">您可以采用各种方式分配预算计划中的数据以准确地描述预计金额。</span><span class="sxs-lookup"><span data-stu-id="608d1-105">You can distribute the data in a budget plan in a number of ways to accurately portray the projected amounts.</span></span>

## <a name="allocation-methods"></a><span data-ttu-id="608d1-106">分配方法</span><span class="sxs-lookup"><span data-stu-id="608d1-106">Allocation methods</span></span>
<span data-ttu-id="608d1-107">三种分配方法（“跨期分配”、“分配到维度”和“使用分类帐分配规则”）可创建基于同一预算计划中的行的预算计划行。</span><span class="sxs-lookup"><span data-stu-id="608d1-107">Three allocation methods (Allocate across periods, Allocate to dimensions, and Use ledger allocation rules) can create budget plan lines that are based on lines in the same budget plan.</span></span> <span data-ttu-id="608d1-108">另外三种方法（“聚合”、“分配”和“从预算计划复制”）可创建其他预算计划中的预算计划行。</span><span class="sxs-lookup"><span data-stu-id="608d1-108">Three other methods (Aggregate, Distribute, and Copy from budget plan) can create budget plan lines in other budget plans.</span></span> <span data-ttu-id="608d1-109">对于所有六种分配方法，您指定目标方案。</span><span class="sxs-lookup"><span data-stu-id="608d1-109">For all six allocation methods, you specify the destination scenario.</span></span> <span data-ttu-id="608d1-110">目标方案可以是与源方案相同或不相同的方案。</span><span class="sxs-lookup"><span data-stu-id="608d1-110">The destination scenario can be either the same as the source scenario or different from the source scenario.</span></span> <span data-ttu-id="608d1-111">或者，您可以指定新行是否追加到预算计划或替换预算计划中的当前行。</span><span class="sxs-lookup"><span data-stu-id="608d1-111">Additionally, you can specify whether new lines are appended to the budget plan or replace the current lines in the budget plan.</span></span>

> [!NOTE] 
> <span data-ttu-id="608d1-112">应该对聚合使用不同于用于配送或父计划中之前执行的其他修改的方案的唯一方案。</span><span class="sxs-lookup"><span data-stu-id="608d1-112">A unique scenario should be used for aggregation that is different from the scenario that was used for distribution or other modifications that were previously performed  in the parent plan.</span></span>  

<span data-ttu-id="608d1-113">[![跨期分配分配方法](./media/allocateacrossperiods-300x259.png)](./media/allocateacrossperiods.png)
 **跨期分配** – 期间分配类别用于跨目标方案中的期间分配源预算计划方案中的预算计划行。</span><span class="sxs-lookup"><span data-stu-id="608d1-113">[![Allocate across Periods allocation method](./media/allocateacrossperiods-300x259.png)](./media/allocateacrossperiods.png)
**Allocate across periods** – A period allocation category is used to allocate the budget plan lines from the source budget plan scenario across periods in the destination scenario.</span></span> <span data-ttu-id="608d1-114">源金额将基于期间分配类别中定义的百分比和日期分配到目标方案中的多行。</span><span class="sxs-lookup"><span data-stu-id="608d1-114">The source amount is assigned to multiple lines in the destination scenario, based on the percentage and date that are defined in the period allocation category.</span></span>         

<span data-ttu-id="608d1-115">[![分配到维度分配方法](./media/allocatetodimensions.jpg)](./media/allocatetodimensions.jpg)
**分配到维度** – 预算计划行将基于所选预算期限中定义的百分比和财务维度从源预算计划方案中分配到目标方案中的一行或多行。</span><span class="sxs-lookup"><span data-stu-id="608d1-115">[![Allocate to Dimensions allocation method](./media/allocatetodimensions.jpg)](./media/allocatetodimensions.jpg)
**Allocate to dimensions** – The budget plan lines are allocated from the source budget planning scenario to one or more lines in the destination scenario, based on the percentages and financial dimensions that are defined in a selected budget allocation term.</span></span>           

<span data-ttu-id="608d1-116">![聚合图表](./media/aggregatechart-300x230.png)
**聚合** - 预算计划行将从关联（子）预算计划中的源预算计划方案中聚合到父预算计划的目标方案。</span><span class="sxs-lookup"><span data-stu-id="608d1-116">![Aggregate chart](./media/aggregatechart-300x230.png)
**Aggregate** – The budget plan lines are aggregated from the source budget plan scenario in the associated (child) budget plans to the destination scenario in the parent budget plan.</span></span> <span data-ttu-id="608d1-117">此方法使得在组织中较低级别准备的预算金额在较高级别处合并。</span><span class="sxs-lookup"><span data-stu-id="608d1-117">This method enables budget amounts that are prepared at a lower level in the organization to be consolidated at a higher level.</span></span>          

<span data-ttu-id="608d1-118">[![分配图表](./media/distributechart-300x230.png)](./media/distributechart.png)
**分配** - 预算计划行将基于关联计划的组织单位的财务维度从父预算计划中的源预算计划方案分配到关联（子）预算计划中的目标方案。</span><span class="sxs-lookup"><span data-stu-id="608d1-118">[![Distribute chart](./media/distributechart-300x230.png)](./media/distributechart.png)
**Distribute** – The budget plan lines are distributed from the source budget planning scenario in the parent budget plan to the destination scenario in the associated (child) budget plans, based on the financial dimensions of the organization units of the associated plans.</span></span> <span data-ttu-id="608d1-119">此方法使得在组织中较高级别准备的预算金额进行分散以实现更本地化审核。</span><span class="sxs-lookup"><span data-stu-id="608d1-119">This method enables budget amounts that are prepared at a higher level in the organization to be spread out for more localized review.</span></span>           

<span data-ttu-id="608d1-120">[![分类帐分配规则](./media/ledgerallocationrules-300x202.png)](./media/ledgerallocationrules.png)
**使用分类帐分配规则** – 预算计划行将基于所选的分类帐分配规则从源预算计划方案中分配到目标方案。</span><span class="sxs-lookup"><span data-stu-id="608d1-120">[![Ledger allocation rules](./media/ledgerallocationrules-300x202.png)](./media/ledgerallocationrules.png)
**Use ledger allocation rules** – The budget plan lines are distributed from the source budget planning scenario to the destination scenario, based on the ledger allocation rule that is selected.</span></span> 

<span data-ttu-id="608d1-121">[![从预算计划复制](./media/copyfrombudgetplan-187x300.png)](./media/copyfrombudgetplan.png)
**从预算计划复制** – 正如“分配”分配方法中一样，预算计划行将基于相关预算计划中的行在目标方案中创建。</span><span class="sxs-lookup"><span data-stu-id="608d1-121">[![Copy from budget plan](./media/copyfrombudgetplan-187x300.png)](./media/copyfrombudgetplan.png)
**Copy from budget plan** – As in the Distribute allocation method, budget plan lines are created in the destination, based on lines in a related budget plan.</span></span> <span data-ttu-id="608d1-122">但是，对于此方法，源预算计划不必为父计划但可以是预算计划层次结构中的任何较高级别。</span><span class="sxs-lookup"><span data-stu-id="608d1-122">However, for this method, the source budget plan doesn't have to be the parent but can be at any higher level in the budget plan hierarchy.</span></span> <span data-ttu-id="608d1-123">此分配方法在以下情况下有用：合并的金额最初在非常高级别处进行预算，而且必须先转移到组织的较低级别以实现详细审核和调整，然后金额才能收到父审批。</span><span class="sxs-lookup"><span data-stu-id="608d1-123">This allocation method is useful if consolidated amounts are originally budgeted at a much higher level, and must be transferred to a lower level of the organization for detailed review and adjustment before they can receive upper-level approval.</span></span>          

## <a name="using-allocation-methods-in-a-budget-plan"></a><span data-ttu-id="608d1-124">在预算计划中使用分配方法</span><span class="sxs-lookup"><span data-stu-id="608d1-124">Using allocation methods in a budget plan</span></span>
<span data-ttu-id="608d1-125">要在预算计划页面上执行分配，请选择要分配的行，然后单击**分配预算**。</span><span class="sxs-lookup"><span data-stu-id="608d1-125">To perform allocations on the budget plan page, select the lines to allocate, and then click **Allocate budget**.</span></span>

<span data-ttu-id="608d1-126">[![分配预算按钮](./media/allocatebudgetbutton-300x84.png)](./media/allocatebudgetbutton.png)</span><span class="sxs-lookup"><span data-stu-id="608d1-126">[![Allocate budget button](./media/allocatebudgetbutton-300x84.png)](./media/allocatebudgetbutton.png)</span></span> 

<span data-ttu-id="608d1-127">接下来，选择分配方法。</span><span class="sxs-lookup"><span data-stu-id="608d1-127">Next, select an allocation method.</span></span> <span data-ttu-id="608d1-128">然后基于所选的方法设置剩余字段。</span><span class="sxs-lookup"><span data-stu-id="608d1-128">The remaining fields are then set, based on the method that you selected.</span></span> <span data-ttu-id="608d1-129">这些字段包含预算计划数据的源和目标以及一个选项，利用此选项，您可以在创建目标金额时用源乘以某个指定的系数，以便简化大量调整。</span><span class="sxs-lookup"><span data-stu-id="608d1-129">These fields include the source and destination of the budget plan data, and an option that lets you multiply the source by a specified factor when the destination amounts are created, to simplify bulk adjustment.</span></span> <span data-ttu-id="608d1-130">您还可以设置**追加到计划**选项。</span><span class="sxs-lookup"><span data-stu-id="608d1-130">You can also set the **Append to plan** option.</span></span> <span data-ttu-id="608d1-131">选择**否**替换现有预算计划行，或者选择**是**保留现有预算计划行并为分配的金额添加新行。</span><span class="sxs-lookup"><span data-stu-id="608d1-131">Select **No** to replace the existing budget plan lines, or select **Yes** to retain the existing budget plan lines and add new lines for the allocated amounts.</span></span>

## <a name="automating-allocations-during-a-workflow"></a><span data-ttu-id="608d1-132">自动工作流期间的分配</span><span class="sxs-lookup"><span data-stu-id="608d1-132">Automating allocations during a workflow</span></span>
<span data-ttu-id="608d1-133">一种强大的功能使得分配能够作为预算计划工作流中的一部分自动执行。</span><span class="sxs-lookup"><span data-stu-id="608d1-133">One powerful feature enables allocations to be performed automatically as part of a budget planning workflow.</span></span> <span data-ttu-id="608d1-134">由于预算计划在其工作流中移动，因此自动化任务可在某个指定预算计划阶段中调用分配。</span><span class="sxs-lookup"><span data-stu-id="608d1-134">As a budget plan moves through its workflow, automated tasks can invoke an allocation at a specified budget planning stage.</span></span> 

<span data-ttu-id="608d1-135">要设置自动化分配，您必须先在**预算计划配置**页面上创建分配计划。</span><span class="sxs-lookup"><span data-stu-id="608d1-135">To set up automated allocation, you must first create an allocation schedule on the **Budget planning configuration** page.</span></span> <span data-ttu-id="608d1-136">此分配计划定义在运行自动化分配时将使用的分配方法以及各种分配选项的值（请参阅上一部分中说明）。</span><span class="sxs-lookup"><span data-stu-id="608d1-136">The allocation schedule defines the allocation method that will be used when the automated allocation is run, and the values of the various allocation options (see the previous section for descriptions).</span></span> 

<span data-ttu-id="608d1-137">然后，在**预算计划配置**页面上创建阶段分配。</span><span class="sxs-lookup"><span data-stu-id="608d1-137">Next, you create a stage allocation on the **Budget planning configuration** page.</span></span> <span data-ttu-id="608d1-138">阶段分配会将分配计划分配到预算计划工作流和阶段。</span><span class="sxs-lookup"><span data-stu-id="608d1-138">The stage allocation assigns an allocation schedule to the budget planning workflow and stage.</span></span> 

<span data-ttu-id="608d1-139">最后，在所需的工作流阶段处为预算计划阶段分配添加自动化任务。</span><span class="sxs-lookup"><span data-stu-id="608d1-139">Finally, add an automated task for budget planning stage allocation at the desired workflow stage.</span></span> <span data-ttu-id="608d1-140">在以下示例中，两个预算计划阶段分配（用红色标出）已插入到工作流中。</span><span class="sxs-lookup"><span data-stu-id="608d1-140">In the following example, two budget planning stage allocations (outlined in red) have been inserted into the workflow.</span></span>

<span data-ttu-id="608d1-141">[![预算计划阶段分配](./media/budgetplanningstageallocations-300x300.png)](./media/budgetplanningstageallocations.png)</span><span class="sxs-lookup"><span data-stu-id="608d1-141">[![Budget planning stage allocations](./media/budgetplanningstageallocations-300x300.png)](./media/budgetplanningstageallocations.png)</span></span>



