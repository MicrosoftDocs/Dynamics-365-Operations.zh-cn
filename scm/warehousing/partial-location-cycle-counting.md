---
title: "部分库位周期盘点"
description: "周期盘点计划指导实际盘点操作。 您可以要求仅盘点特定的产品和产品变型，无需对库位中的所有现有库存进行盘点。"
author: perlynne
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
keywords: WHSCycleCountPlan, WHSWorkLineCycleCount, WHSWorkTemplateLineGroup, WHSWorkTemplateTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 2ee4de8eabc55271e272ca3026746787353f5fc3
ms.contentlocale: zh-cn
ms.lasthandoff: 07/18/2017

---

# <a name="partial-location-cycle-counting"></a><span data-ttu-id="1f479-105">部分库位周期盘点</span><span class="sxs-lookup"><span data-stu-id="1f479-105">Partial location cycle counting</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="1f479-106">周期盘点计划指导实际盘点操作。</span><span class="sxs-lookup"><span data-stu-id="1f479-106">Cycle count plans guide the actual counting operations.</span></span> <span data-ttu-id="1f479-107">您可以要求仅盘点特定的产品和产品变型，无需对库位中的所有现有库存进行盘点。</span><span class="sxs-lookup"><span data-stu-id="1f479-107">You can request that only specific products and product variants be counted instead of all on-hand inventory in a location.</span></span>

<span data-ttu-id="1f479-108">通过使用周期盘点计划创建盘点工作，您可以指导实际盘点操作。</span><span class="sxs-lookup"><span data-stu-id="1f479-108">By using cycle count plans to create counting work, you can guide the actual counting operations.</span></span> <span data-ttu-id="1f479-109">您可以要求仅盘点特定的产品和产品变型，无需对库位中的所有现有库存进行盘点。</span><span class="sxs-lookup"><span data-stu-id="1f479-109">You can request that only specific products and product variants be counted instead of all on-hand inventory in a location.</span></span> <span data-ttu-id="1f479-110">通过筛选特定产品，仓库经理可以降低审核开销，避免合并错误和节省时间。</span><span class="sxs-lookup"><span data-stu-id="1f479-110">By filtering on specific products, the warehouse manager can reduce review overhead, avoid consolidation mistakes, and save time.</span></span>

## <a name="how-to-configure-partial-location-cycle-counting"></a><span data-ttu-id="1f479-111">如何配置部分库位周期盘点</span><span class="sxs-lookup"><span data-stu-id="1f479-111">How to configure partial location cycle counting</span></span>
<span data-ttu-id="1f479-112">当您对盘点操作使用仓库工作流程时，为每个库位创建一个工作标题。</span><span class="sxs-lookup"><span data-stu-id="1f479-112">When you use the warehouse work process for counting operations, a work header is created for each location.</span></span> <span data-ttu-id="1f479-113">当您定义周期盘点计划时，可以使用**选择库位**查询以限制创建的周期盘点工作。</span><span class="sxs-lookup"><span data-stu-id="1f479-113">When you define the cycle count plan, you can use the **Select locations** query to limit the cycle counting work that is created.</span></span> <span data-ttu-id="1f479-114">为周期盘点计划选择产品时，可以同时选择产品和产品变型查询以细化盘点内容。</span><span class="sxs-lookup"><span data-stu-id="1f479-114">When you select products for the cycle count plan, you can select both product and product variant queries to refine what is counted.</span></span> 

<span data-ttu-id="1f479-115">您可以将**工作模板**与周期盘点计划相关联，以定义创建周期盘点工作的方式。</span><span class="sxs-lookup"><span data-stu-id="1f479-115">You can associate a **work template** with a cycle count plan to define how the cycle count work should be created.</span></span> <span data-ttu-id="1f479-116">用于盘点操作的工作模板从周期盘点计划中直接引用。</span><span class="sxs-lookup"><span data-stu-id="1f479-116">The work template for counting operations is directly referenced from the cycle count plan.</span></span> 

<span data-ttu-id="1f479-117">定义工作模板详细信息时，可以使用**工作换行符**选项以指定是否必须按照物料编号或产品变型编号对盘点工作行分组。</span><span class="sxs-lookup"><span data-stu-id="1f479-117">When you define the work template details, you can use the **Work line breaks** option to specify whether the counting work lines must be grouped by item number or product variant number.</span></span> <span data-ttu-id="1f479-118">如果您要仅对一个库位中的特定产品盘点现有库存，则必须进行此设置。</span><span class="sxs-lookup"><span data-stu-id="1f479-118">This setup is required if you want to count on-hand inventory only for specific products in a location.</span></span> <span data-ttu-id="1f479-119">创建的周期盘点工作行将具有您在此处定义的信息级别，并将基于此级别处理指导的盘点操作。</span><span class="sxs-lookup"><span data-stu-id="1f479-119">The cycle counting work lines that are created will have the level of information that you define here, and the guided counting operation will be handled based on this level.</span></span> 

<span data-ttu-id="1f479-120">如果您使用**工作换行符**选项将周期盘点计划与工作模板相关联，则为创建的周期盘点工作选择**部分周期盘点**字段，并将基于工作模板的定义创建多个周期盘点工作行。</span><span class="sxs-lookup"><span data-stu-id="1f479-120">If you associate cycle count plans with work templates by using the **Work lines breaks** option, the **Partial cycle count** field is selected for the cycle counting work that is created, and multiple cycle counting work lines will be created based on the definition of the work template.</span></span> 

<span data-ttu-id="1f479-121">可以处理部分周期盘点工作前，您必须至少为移动设备菜单项选择**显示物料编号**作为周期盘点设置的一部分。</span><span class="sxs-lookup"><span data-stu-id="1f479-121">Before partial cycle count work can be processed, you must, at a minimum, select **Display item number** for the mobile device menu item as part of the cycle counting setup.</span></span> <span data-ttu-id="1f479-122">系统将要求仓库操作员仅记录与盘点行相关联的盘点信息（物料编号和产品维度）。</span><span class="sxs-lookup"><span data-stu-id="1f479-122">The warehouse operator will be asked to record only counting information that is related to the counting lines (item numbers and product dimensions).</span></span> <span data-ttu-id="1f479-123">此盘点流程将忽略所有其他现有库存。</span><span class="sxs-lookup"><span data-stu-id="1f479-123">All other on-hand inventory will be ignored for this counting process.</span></span> 

<span data-ttu-id="1f479-124">对于部分周期盘点流程，不会更新此库位的**上一次周期盘点**日期/时间。</span><span class="sxs-lookup"><span data-stu-id="1f479-124">For the partial cycle count process, the **Last cycle count** date/time won’t be updated for the location.</span></span>

## <a name="example"></a><span data-ttu-id="1f479-125">示例</span><span class="sxs-lookup"><span data-stu-id="1f479-125">Example</span></span>
<span data-ttu-id="1f479-126">在此示例中，仅须盘点仓库 61 中的物料编号 A0001。</span><span class="sxs-lookup"><span data-stu-id="1f479-126">For this example, only item number A0001 must be counted in warehouse 61.</span></span>

1.  <span data-ttu-id="1f479-127">为周期盘点创建新的工作模板。</span><span class="sxs-lookup"><span data-stu-id="1f479-127">A new work template for cycle counting is created.</span></span> <span data-ttu-id="1f479-128">**工作换行符**选项用于按物料编号对盘点工作行分组。</span><span class="sxs-lookup"><span data-stu-id="1f479-128">The **Work line breaks** option is used to group counting work lines by item number.</span></span> <span data-ttu-id="1f479-129">因此，创建的周期盘点工作的每个物料编号有多行。</span><span class="sxs-lookup"><span data-stu-id="1f479-129">Therefore, the cycle counting work that is created will have lines per item number.</span></span> <span data-ttu-id="1f479-130">您还可以按产品变型编号对行分组。</span><span class="sxs-lookup"><span data-stu-id="1f479-130">You can also group the lines by product variant number.</span></span>
2.  <span data-ttu-id="1f479-131">创建引用新建工作模板的新周期盘点计划。</span><span class="sxs-lookup"><span data-stu-id="1f479-131">A new cycle counting plan is created that references the newly created work template.</span></span> <span data-ttu-id="1f479-132">周期盘点计划包括拥有物料编号 A0001 库存的仓库 61 中的所有库位（**选择库位**查询）。</span><span class="sxs-lookup"><span data-stu-id="1f479-132">The cycle counting plan includes all locations in warehouse 61 (**Select locations** query) that hold inventory for item number A0001.</span></span> <span data-ttu-id="1f479-133">特定产品的选择在**周期盘点产品选择**部分定义。</span><span class="sxs-lookup"><span data-stu-id="1f479-133">The selection of specific products is defined in the **Cycle count product selections** section.</span></span>
3.  <span data-ttu-id="1f479-134">您可以通过将**空库位**字段设置为**排除空库位**的方式为周期盘点计划选择产品。处理周期盘点计划时，为物料 A0001 创建部分周期盘点工作。</span><span class="sxs-lookup"><span data-stu-id="1f479-134">You can select products for cycle counting plans by setting the **Empty locations** field to **Exclude empty**.When the cycle counting plan is processed, partial cycle count work for item number A0001 is created.</span></span> <span data-ttu-id="1f479-135">使用用于指导的周期盘点的移动设备菜单项可以执行实际盘点流程。</span><span class="sxs-lookup"><span data-stu-id="1f479-135">The actual counting process can be performed by using a mobile device menu item for guided cycle counting.</span></span>



<a name="see-also"></a><span data-ttu-id="1f479-136">请参阅</span><span class="sxs-lookup"><span data-stu-id="1f479-136">See also</span></span>
--------

[<span data-ttu-id="1f479-137">周期盘点</span><span class="sxs-lookup"><span data-stu-id="1f479-137">Cycle counting</span></span>](cycle-counting.md)


