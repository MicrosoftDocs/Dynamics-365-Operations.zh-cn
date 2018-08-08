---
title: "部分库位周期盘点"
description: "周期盘点计划指导实际盘点操作。 您可以要求仅盘点特定的产品和产品变型，无需对库位中的所有现有库存进行盘点。"
author: perlynne
manager: AnnBe
ms.date: 11/02/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSCycleCountPlan, WHSWorkLineCycleCount, WHSWorkTemplateLineGroup, WHSWorkTemplateTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: cd7cb8b35023ed63af191545d01c60c2c7cc8ef5
ms.contentlocale: zh-cn
ms.lasthandoff: 08/07/2018

---

# <a name="partial-location-cycle-counting"></a><span data-ttu-id="7cdab-104">部分库位周期盘点</span><span class="sxs-lookup"><span data-stu-id="7cdab-104">Partial location cycle counting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7cdab-105">周期盘点计划指导实际盘点操作。</span><span class="sxs-lookup"><span data-stu-id="7cdab-105">Cycle count plans guide the actual counting operations.</span></span> <span data-ttu-id="7cdab-106">您可以要求仅盘点特定的产品和产品变型，无需对库位中的所有现有库存进行盘点。</span><span class="sxs-lookup"><span data-stu-id="7cdab-106">You can request that only specific products and product variants be counted instead of all on-hand inventory in a location.</span></span>

<span data-ttu-id="7cdab-107">通过使用周期盘点计划创建盘点工作，您可以指导实际盘点操作。</span><span class="sxs-lookup"><span data-stu-id="7cdab-107">By using cycle count plans to create counting work, you can guide the actual counting operations.</span></span> <span data-ttu-id="7cdab-108">您可以要求仅盘点特定的产品和产品变型，无需对库位中的所有现有库存进行盘点。</span><span class="sxs-lookup"><span data-stu-id="7cdab-108">You can request that only specific products and product variants be counted instead of all on-hand inventory in a location.</span></span> <span data-ttu-id="7cdab-109">通过筛选特定产品，仓库经理可以降低审核开销，避免合并错误和节省时间。</span><span class="sxs-lookup"><span data-stu-id="7cdab-109">By filtering on specific products, the warehouse manager can reduce review overhead, avoid consolidation mistakes, and save time.</span></span>

## <a name="how-to-configure-partial-location-cycle-counting"></a><span data-ttu-id="7cdab-110">如何配置部分库位周期盘点</span><span class="sxs-lookup"><span data-stu-id="7cdab-110">How to configure partial location cycle counting</span></span>
<span data-ttu-id="7cdab-111">当您对盘点操作使用仓库工作流程时，为每个库位创建一个工作标题。</span><span class="sxs-lookup"><span data-stu-id="7cdab-111">When you use the warehouse work process for counting operations, a work header is created for each location.</span></span> <span data-ttu-id="7cdab-112">当您定义周期盘点计划时，可以使用**选择库位**查询以限制创建的周期盘点工作。</span><span class="sxs-lookup"><span data-stu-id="7cdab-112">When you define the cycle count plan, you can use the **Select locations** query to limit the cycle counting work that is created.</span></span> <span data-ttu-id="7cdab-113">为周期盘点计划选择产品时，可以同时选择产品和产品变型查询以细化盘点内容。</span><span class="sxs-lookup"><span data-stu-id="7cdab-113">When you select products for the cycle count plan, you can select both product and product variant queries to refine what is counted.</span></span> 

<span data-ttu-id="7cdab-114">您可以将**工作模板**与周期盘点计划相关联，以定义创建周期盘点工作的方式。</span><span class="sxs-lookup"><span data-stu-id="7cdab-114">You can associate a **work template** with a cycle count plan to define how the cycle count work should be created.</span></span> <span data-ttu-id="7cdab-115">用于盘点操作的工作模板从周期盘点计划中直接引用。</span><span class="sxs-lookup"><span data-stu-id="7cdab-115">The work template for counting operations is directly referenced from the cycle count plan.</span></span> 

<span data-ttu-id="7cdab-116">定义工作模板详细信息时，可以使用**工作换行符**选项以指定是否必须按照物料编号或产品变型编号对盘点工作行分组。</span><span class="sxs-lookup"><span data-stu-id="7cdab-116">When you define the work template details, you can use the **Work line breaks** option to specify whether the counting work lines must be grouped by item number or product variant number.</span></span> <span data-ttu-id="7cdab-117">如果您要仅对一个库位中的特定产品盘点现有库存，则必须进行此设置。</span><span class="sxs-lookup"><span data-stu-id="7cdab-117">This setup is required if you want to count on-hand inventory only for specific products in a location.</span></span> <span data-ttu-id="7cdab-118">创建的周期盘点工作行将具有您在此处定义的信息级别，并将基于此级别处理指导的盘点操作。</span><span class="sxs-lookup"><span data-stu-id="7cdab-118">The cycle counting work lines that are created will have the level of information that you define here, and the guided counting operation will be handled based on this level.</span></span> 

<span data-ttu-id="7cdab-119">如果您使用**工作换行符**选项将周期盘点计划与工作模板相关联，则为创建的周期盘点工作选择**部分周期盘点**字段，并将基于工作模板的定义创建多个周期盘点工作行。</span><span class="sxs-lookup"><span data-stu-id="7cdab-119">If you associate cycle count plans with work templates by using the **Work lines breaks** option, the **Partial cycle count** field is selected for the cycle counting work that is created, and multiple cycle counting work lines will be created based on the definition of the work template.</span></span> 

<span data-ttu-id="7cdab-120">可以处理部分周期盘点工作前，您必须至少为移动设备菜单项选择**显示物料编号**作为周期盘点设置的一部分。</span><span class="sxs-lookup"><span data-stu-id="7cdab-120">Before partial cycle count work can be processed, you must, at a minimum, select **Display item number** for the mobile device menu item as part of the cycle counting setup.</span></span> <span data-ttu-id="7cdab-121">系统将要求仓库操作员仅记录与盘点行相关联的盘点信息（物料编号和产品维度）。</span><span class="sxs-lookup"><span data-stu-id="7cdab-121">The warehouse operator will be asked to record only counting information that is related to the counting lines (item numbers and product dimensions).</span></span> <span data-ttu-id="7cdab-122">此盘点流程将忽略所有其他现有库存。</span><span class="sxs-lookup"><span data-stu-id="7cdab-122">All other on-hand inventory will be ignored for this counting process.</span></span> 

<span data-ttu-id="7cdab-123">对于部分周期盘点流程，不会更新此库位的**上一次周期盘点**日期/时间。</span><span class="sxs-lookup"><span data-stu-id="7cdab-123">For the partial cycle count process, the **Last cycle count** date/time won’t be updated for the location.</span></span>

## <a name="example"></a><span data-ttu-id="7cdab-124">示例</span><span class="sxs-lookup"><span data-stu-id="7cdab-124">Example</span></span>
<span data-ttu-id="7cdab-125">在此示例中，仅须盘点仓库 61 中的物料编号 A0001。</span><span class="sxs-lookup"><span data-stu-id="7cdab-125">For this example, only item number A0001 must be counted in warehouse 61.</span></span>

1.  <span data-ttu-id="7cdab-126">为周期盘点创建新的工作模板。</span><span class="sxs-lookup"><span data-stu-id="7cdab-126">A new work template for cycle counting is created.</span></span> <span data-ttu-id="7cdab-127">**工作换行符**选项用于按物料编号对盘点工作行分组。</span><span class="sxs-lookup"><span data-stu-id="7cdab-127">The **Work line breaks** option is used to group counting work lines by item number.</span></span> <span data-ttu-id="7cdab-128">因此，创建的周期盘点工作的每个物料编号有多行。</span><span class="sxs-lookup"><span data-stu-id="7cdab-128">Therefore, the cycle counting work that is created will have lines per item number.</span></span> <span data-ttu-id="7cdab-129">您还可以按产品变型编号对行分组。</span><span class="sxs-lookup"><span data-stu-id="7cdab-129">You can also group the lines by product variant number.</span></span>
2.  <span data-ttu-id="7cdab-130">创建引用新建工作模板的新周期盘点计划。</span><span class="sxs-lookup"><span data-stu-id="7cdab-130">A new cycle counting plan is created that references the newly created work template.</span></span> <span data-ttu-id="7cdab-131">周期盘点计划包括拥有物料编号 A0001 库存的仓库 61 中的所有库位（**选择库位**查询）。</span><span class="sxs-lookup"><span data-stu-id="7cdab-131">The cycle counting plan includes all locations in warehouse 61 (**Select locations** query) that hold inventory for item number A0001.</span></span> <span data-ttu-id="7cdab-132">特定产品的选择在**周期盘点产品选择**部分定义。</span><span class="sxs-lookup"><span data-stu-id="7cdab-132">The selection of specific products is defined in the **Cycle count product selections** section.</span></span>
3.  <span data-ttu-id="7cdab-133">您可以通过将**空库位**字段设置为**排除空库位**来为周期盘点计划选择产品。</span><span class="sxs-lookup"><span data-stu-id="7cdab-133">You can select products for cycle counting plans by setting the **Empty locations** field to **Exclude empty**.</span></span> <span data-ttu-id="7cdab-134">在处理周期盘点计划时，物料编号 A0001 的部分周期盘点工作将创建。</span><span class="sxs-lookup"><span data-stu-id="7cdab-134">When the cycle counting plan is processed, partial cycle count work for item number A0001 is created.</span></span> <span data-ttu-id="7cdab-135">使用用于指导的周期盘点的移动设备菜单项可以执行实际盘点流程。</span><span class="sxs-lookup"><span data-stu-id="7cdab-135">The actual counting process can be performed by using a mobile device menu item for guided cycle counting.</span></span>



<a name="additional-resources"></a><span data-ttu-id="7cdab-136">其他资源</span><span class="sxs-lookup"><span data-stu-id="7cdab-136">Additional resources</span></span>
--------

[<span data-ttu-id="7cdab-137">周期盘点</span><span class="sxs-lookup"><span data-stu-id="7cdab-137">Cycle counting</span></span>](cycle-counting.md)


