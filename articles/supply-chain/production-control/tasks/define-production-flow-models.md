---
title: 定义生产流模型
description: 生产流模型描述如何计算并维持精益制造工作单元的产能。
author: cvocph
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlowModel
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8267b18ea85b7a6ba7a1333b586f36ea8b6e8e30
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5257211"
---
# <a name="define-production-flow-models"></a><span data-ttu-id="a42d8-103">定义生产流模型</span><span class="sxs-lookup"><span data-stu-id="a42d8-103">Define production flow models</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a42d8-104">生产流模型描述如何计算并维持精益制造工作单元的产能。</span><span class="sxs-lookup"><span data-stu-id="a42d8-104">Production flow models describe how the capacity of lean manufacturing work cells is calculated and maintained.</span></span> <span data-ttu-id="a42d8-105">因此，定义生产流模型是定义工作单元的先决条件。</span><span class="sxs-lookup"><span data-stu-id="a42d8-105">Therefore the definition of a production flow model is a prerequisite of the definition of work cells.</span></span> <span data-ttu-id="a42d8-106">创建此程序的演示数据公司是 USMF。</span><span class="sxs-lookup"><span data-stu-id="a42d8-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="define-a-production-flow-model"></a><span data-ttu-id="a42d8-107">定义生产流模型。</span><span class="sxs-lookup"><span data-stu-id="a42d8-107">Define a production flow model.</span></span> 
1. <span data-ttu-id="a42d8-108">转到“生产管理”>“设置”>“精益生产流”>“生产流模型”。</span><span class="sxs-lookup"><span data-stu-id="a42d8-108">Go to Production control > Setup > Lean production flow > Production flow models.</span></span>
2. <span data-ttu-id="a42d8-109">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="a42d8-109">Click New.</span></span>
3. <span data-ttu-id="a42d8-110">在“生产流模型”字段中，输入生产流模型的 ID。</span><span class="sxs-lookup"><span data-stu-id="a42d8-110">In the Production flow model field, enter an ID for the production flow model.</span></span>
4. <span data-ttu-id="a42d8-111">在“模型类型”字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="a42d8-111">In the Model type field, select an option.</span></span>
    * <span data-ttu-id="a42d8-112">两个模型类型：吞吐量类型和工时类型。</span><span class="sxs-lookup"><span data-stu-id="a42d8-112">There are two model types: Throughput type and Hours type.</span></span> <span data-ttu-id="a42d8-113">对于使用吞吐量类型生产流模型的工作单元，其产能将通过产品数量进行描述和计算。</span><span class="sxs-lookup"><span data-stu-id="a42d8-113">For Throughput type, the capacity of work cells that use this production flow model will be expressed and calculated in product quantities.</span></span> <span data-ttu-id="a42d8-114">对于使用工时类型生产流模型的工作单元，其产能将通过工时数进行描述和计算。</span><span class="sxs-lookup"><span data-stu-id="a42d8-114">For Hours type, the capacity of work cells that uses this production flow model will be expressed and calculated in hours.</span></span> <span data-ttu-id="a42d8-115">请注意，现有生产流模型的属性无法更改。</span><span class="sxs-lookup"><span data-stu-id="a42d8-115">Note that this property can't be changed for an existing production flow model.</span></span> <span data-ttu-id="a42d8-116">工作单元具有产能预留后，其生产流模型将无法更改。</span><span class="sxs-lookup"><span data-stu-id="a42d8-116">After a work cell has capacity reservations, the production flow model type can't be changed.</span></span>  
5. <span data-ttu-id="a42d8-117">在“EPE 周期”字段中输入天数。</span><span class="sxs-lookup"><span data-stu-id="a42d8-117">Enter the number of days in the EPE Cycle.</span></span>
    * <span data-ttu-id="a42d8-118">间隔描述生产流或工作单元的每个部分将至少生产一次的周期。</span><span class="sxs-lookup"><span data-stu-id="a42d8-118">The interval describes the period when every part produced by a production flow or work cell will be produced at least once.</span></span> <span data-ttu-id="a42d8-119">EPE 循环时间越短，生产流就越灵活。</span><span class="sxs-lookup"><span data-stu-id="a42d8-119">The shorter the EPE cycle, the more flexible the production process is.</span></span> <span data-ttu-id="a42d8-120">如果 EPE 周期 = 0，则所有的需求量可在同一天生产出。</span><span class="sxs-lookup"><span data-stu-id="a42d8-120">If EPE Cycle = 0, all demand can be produced in the same day.</span></span> <span data-ttu-id="a42d8-121">EPE 周期用于安排精益流程作业计划。</span><span class="sxs-lookup"><span data-stu-id="a42d8-121">The EPE Cycle is used to schedule lean process jobs.</span></span> <span data-ttu-id="a42d8-122">如果采用 EPE 周期 = 5 计划工作单元中一项作业，则该计划流程将在到期日期 - EPE 周期（到期日期前 5 天）查询该工作单元的产能以确保该产品是否能在该周期内生产。</span><span class="sxs-lookup"><span data-stu-id="a42d8-122">When scheduling a job on a work cell with EPE Cycle = 5, the scheduling process will look for capacity on the work cell at Due date - EPE Cycle (5 days ahead of the due date) to ensure that the product can be produced in that cycle.</span></span> <span data-ttu-id="a42d8-123">产品的库存提前期通常等于或大于关联生产流的 EPE 周期。</span><span class="sxs-lookup"><span data-stu-id="a42d8-123">The inventory lead time of a product is usually equal to or greater than the EPE Cycle of the related production process.</span></span>  
6. <span data-ttu-id="a42d8-124">在“计划周期类型”字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="a42d8-124">In the Planning period type field, select an option.</span></span>
    * <span data-ttu-id="a42d8-125">工作单元具有产能预留后，其生产流模型将无法更改。</span><span class="sxs-lookup"><span data-stu-id="a42d8-125">After a work cell has capacity reservations, the planning period type cannot by changed.</span></span> <span data-ttu-id="a42d8-126">对于此特定工作单元，只能选择与其具有相同周期类型的生产流模型。</span><span class="sxs-lookup"><span data-stu-id="a42d8-126">You can only select production flow models with the same period type for this given work cell.</span></span>  
7. <span data-ttu-id="a42d8-127">在“计划时限”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="a42d8-127">In the Planning time fence field, enter a number.</span></span>
    * <span data-ttu-id="a42d8-128">计划产能时限描述可为相关工作单元提供的产能预留天数。</span><span class="sxs-lookup"><span data-stu-id="a42d8-128">The planning time fence describes the number of days where capacity reservations can be made for the related work cells.</span></span> <span data-ttu-id="a42d8-129">在“计划时限”中，输入天数。</span><span class="sxs-lookup"><span data-stu-id="a42d8-129">In the Planning time fence, enter the number of days.</span></span>   <span data-ttu-id="a42d8-130">将不通过自动计划规划不在此期间的看板处理作业。</span><span class="sxs-lookup"><span data-stu-id="a42d8-130">Kanban process jobs that fall outside of this period are not planned with automatic planning.</span></span> <span data-ttu-id="a42d8-131">计划时限通常是生产流或工作单元内所生产产品的平均库存提前期的两倍。</span><span class="sxs-lookup"><span data-stu-id="a42d8-131">The planning time fence is typically two times the average inventory lead time of the products produced in a production flow or work cell.</span></span> <span data-ttu-id="a42d8-132">EPE 周期不应超过计划时隙的一半。</span><span class="sxs-lookup"><span data-stu-id="a42d8-132">The EPE Cycle should not be more than half the planning time fence.</span></span>     
8. <span data-ttu-id="a42d8-133">在“产能短缺反应”字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="a42d8-133">In the Capacity shortage reaction field, select an option.</span></span>
    * <span data-ttu-id="a42d8-134">选项包括：延期 - 将该计划事件的饱和需求量延期至下一个吞吐量的可用生产日。</span><span class="sxs-lookup"><span data-stu-id="a42d8-134">The options include:   Postpone - Postponing the full demand of the scheduling event on the next available production day, with available throughput.</span></span> <span data-ttu-id="a42d8-135">取消 - 终止该计划事件的自动计划作业，并取消其关联的作业计划。</span><span class="sxs-lookup"><span data-stu-id="a42d8-135">Cancel - End the automatic planning for the scheduling event and leave the related jobs unplanned.</span></span>   <span data-ttu-id="a42d8-136">添加到所要求的日期 - 将其要求的作业安排到所要求的期间内。</span><span class="sxs-lookup"><span data-stu-id="a42d8-136">Add to requested day - Plan the requested jobs for the requested period.</span></span> <span data-ttu-id="a42d8-137">这超过当天该工作单元的负荷并需要计划员进行检查和手动交互。</span><span class="sxs-lookup"><span data-stu-id="a42d8-137">This overloads the cell for this day and requires the planner to review and to a manual interaction .</span></span>   <span data-ttu-id="a42d8-138">分配到可用期间 - 从第一个可用生产日开始为该计划事件的所有不同作业分配可用生产日。</span><span class="sxs-lookup"><span data-stu-id="a42d8-138">Distribute to available periods - Distribute the different jobs of the scheduling event to all available production days, beginning from the first available day.</span></span> <span data-ttu-id="a42d8-139">此最小分配数量就是该看板作业的数量。</span><span class="sxs-lookup"><span data-stu-id="a42d8-139">The minimum distribution quantity is the kanban job quantity.</span></span> <span data-ttu-id="a42d8-140">每天分配给最小计划数量（看板作业数量）充足可用的吞吐量。</span><span class="sxs-lookup"><span data-stu-id="a42d8-140">The distribution assigns the minimum planning quantity (kanban quantity) to every day with enough available throughput.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]