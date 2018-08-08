---
title: "仓库配置"
description: "本文说明如何配置仓库。 它包含有关如何启用仓库布局和仓库流程的信息。"
author: perlynne
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventLocation, WHSLocation, WHSLocationBuild, WHSLocationProfile, WHSLocationType, WHSLocDirTable, WHSParameters, WHSWaveTemplateTable, WHSWorkPool, WHSWorkTemplateTable, WHSZone, WHSZoneGroup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 11554
ms.assetid: 262b7b88-2cce-44f7-9a5b-77c12af1be20
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 7e50d03718234748d9ad5092500b970216c40284
ms.contentlocale: zh-cn
ms.lasthandoff: 08/07/2018

---

# <a name="warehouse-configuration"></a><span data-ttu-id="70aea-104">仓库配置</span><span class="sxs-lookup"><span data-stu-id="70aea-104">Warehouse configuration</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="70aea-105">本文说明如何配置仓库。</span><span class="sxs-lookup"><span data-stu-id="70aea-105">This article explains how to configure a warehouse.</span></span> <span data-ttu-id="70aea-106">它包含有关如何启用仓库布局和仓库流程的信息。</span><span class="sxs-lookup"><span data-stu-id="70aea-106">It includes information about how to enable a warehouse layout and warehouse processes.</span></span>

<span data-ttu-id="70aea-107">**注释：** 本文适用于**仓库管理** 模块（高级仓库）中的功能。</span><span class="sxs-lookup"><span data-stu-id="70aea-107">**Note:** This article applies to features in the **Warehouse management** module (advanced warehousing).</span></span> <span data-ttu-id="70aea-108">它不适用于**库存管理**模块中的仓库功能。</span><span class="sxs-lookup"><span data-stu-id="70aea-108">It doesn't apply to warehouse features in the **Inventory management** module.</span></span>

## <a name="warehouse-layout"></a><span data-ttu-id="70aea-109">仓库布局</span><span class="sxs-lookup"><span data-stu-id="70aea-109">Warehouse layout</span></span>
<span data-ttu-id="70aea-110">Microsoft Dynamics 365 for Finance and Operations 中的仓库管理系统允许您以灵活方式定义您的仓库布局以适应不断变化的需要，因此，您可以实现最佳仓库效率。</span><span class="sxs-lookup"><span data-stu-id="70aea-110">The Warehouse management system in Microsoft Dynamics 365 for Finance and Operations gives you flexible ways to define your warehouse layout to meet changing needs, so that you can achieve optimal warehouse efficiency.</span></span>

-   <span data-ttu-id="70aea-111">您可以为货物的最佳位置建立高优先级和低优先级存储区域。</span><span class="sxs-lookup"><span data-stu-id="70aea-111">You can establish high-priority and low-priority storages areas for optimum placement of goods.</span></span>
-   <span data-ttu-id="70aea-112">您可以将您的仓库划分为区域以满足各种存储需要，例如温度要求或物料各种周转比率。</span><span class="sxs-lookup"><span data-stu-id="70aea-112">You can divide your warehouse into zones to accommodate various storage needs, such as temperature requirements, or various turnover rates for items.</span></span>
-   <span data-ttu-id="70aea-113">您可以在任何级别指定仓库位置（例如，站点、仓库、通道、货架、货位和储料箱位置）。</span><span class="sxs-lookup"><span data-stu-id="70aea-113">You can specify warehouse locations on any level (for example, site, warehouse, aisle, rack, shelf, and bin position).</span></span>
-   <span data-ttu-id="70aea-114">您可以通过使用实际容量约束设置来对位置进行分组。</span><span class="sxs-lookup"><span data-stu-id="70aea-114">You can group locations by using physical capacity constraint settings.</span></span>
-   <span data-ttu-id="70aea-115">您可以基于查询定义的规则来控制物料如何存储和领取。</span><span class="sxs-lookup"><span data-stu-id="70aea-115">You can control how items are stored and picked, based on query-defined rules.</span></span>

<span data-ttu-id="70aea-116">若要使用 Finance and Operations 中的仓库管理，您必须创建仓库并为更多高级或专业的仓库管理活动启用它。</span><span class="sxs-lookup"><span data-stu-id="70aea-116">To use warehouse management in Finance and Operations, you must create a warehouse and enable it for more advanced or specialized warehouse management activities.</span></span> <span data-ttu-id="70aea-117">在**仓库**页上，选择**使用仓库管理流程**选项。</span><span class="sxs-lookup"><span data-stu-id="70aea-117">On the **Warehouses** page, select the **Use warehouse management processes** option.</span></span>

### <a name="zone-groups-zones-location-types-and-locations"></a><span data-ttu-id="70aea-118">区域组、区域、位置类型和位置</span><span class="sxs-lookup"><span data-stu-id="70aea-118">Zone groups, zones, location types, and locations</span></span>

<span data-ttu-id="70aea-119">作为启用仓库布局的流程的一部分，您必须定义仓库区域组、区域、位置配置文件、位置类型和位置。</span><span class="sxs-lookup"><span data-stu-id="70aea-119">As part of the process for enabling a warehouse layout, you must define warehouse zone groups, and zones, location profiles, location types, and locations.</span></span>

-   <span data-ttu-id="70aea-120">**区域组** – 仓库内的一个逻辑或实际区域分组。</span><span class="sxs-lookup"><span data-stu-id="70aea-120">**Zone groups** – A logical or physical grouping of zones within a warehouse.</span></span>
-   <span data-ttu-id="70aea-121">**区域** – 仓库内的一个逻辑或实际位置分组。</span><span class="sxs-lookup"><span data-stu-id="70aea-121">**Zones** – A logical or physical grouping of locations within a warehouse.</span></span>
-   <span data-ttu-id="70aea-122">**位置配置文件** – 具有相同仓库位置流程策略的一个逻辑或实际位置分组（例如，不同物料编号的组合可以存储在那里，而且相同实际容量约束适用）。</span><span class="sxs-lookup"><span data-stu-id="70aea-122">**Location profiles** – A logical or physical grouping of locations that have the same warehouse location process policies (for example, a mix of different item numbers can be stored there, and the same physical capacity constraints apply).</span></span>
-   <span data-ttu-id="70aea-123">**区域类型** – 一个逻辑或实际仓库内位置分组。</span><span class="sxs-lookup"><span data-stu-id="70aea-123">**Locations types** – A logical or physical grouping of the warehouse locations.</span></span> <span data-ttu-id="70aea-124">例如，您可以创建所有暂存库位的库位类型。</span><span class="sxs-lookup"><span data-stu-id="70aea-124">For example, you can create a location type for all staging locations.</span></span> <span data-ttu-id="70aea-125">**仓库管理参数**页上的必需设置驱动定义暂存位置类型和最终交货位置类型的流程。</span><span class="sxs-lookup"><span data-stu-id="70aea-125">Mandatory settings on the **Warehouse management parameters** page drive the process of defining staging location types and the final shipping location type.</span></span>
-   <span data-ttu-id="70aea-126">**位置** – 最低级别的位置信息。</span><span class="sxs-lookup"><span data-stu-id="70aea-126">**Locations** – The lowest level of location information.</span></span> <span data-ttu-id="70aea-127">位置用于跟踪在仓库中的哪里存储和领取现有库存。</span><span class="sxs-lookup"><span data-stu-id="70aea-127">Locations are used to track where the on-hand inventory is stored and picked in a warehouse.</span></span>

<span data-ttu-id="70aea-128">您创建用来定义仓库布局的实体在您在工作模板使用设置用于驱动仓库中的工作订单的查询中使用。</span><span class="sxs-lookup"><span data-stu-id="70aea-128">The entities that you create to define your warehouse layout are used in the queries that you set up in work templates to drive work orders in the warehouse.</span></span> <span data-ttu-id="70aea-129">因此，当您定义区域、位置类型等，请考虑仓库中的不同区域如何用于不同流程。</span><span class="sxs-lookup"><span data-stu-id="70aea-129">Therefore, when you define the zones, location types, and so on, consider how different areas in the warehouse are used for different processes.</span></span> <span data-ttu-id="70aea-130">此外，请考虑因素，例如一个特定区域的物理特征。</span><span class="sxs-lookup"><span data-stu-id="70aea-130">Additionally, consider factors such as the physical characteristics of a particular area.</span></span> <span data-ttu-id="70aea-131">例如，可能您在某些区域只能使用某一类型的铲车。</span><span class="sxs-lookup"><span data-stu-id="70aea-131">For example, there might be areas where you can use only a certain type of forklift truck.</span></span> <span data-ttu-id="70aea-132">或者，如果您的公司在同一设施内有生产和成品，您可能希望在 Finance and Operations 中创建单个仓库，但通过创建两个区域组将两个操作分开。</span><span class="sxs-lookup"><span data-stu-id="70aea-132">Or, if your company has both production and finished goods within the same facility, you might want to create a single warehouse in Finance and Operations but then separate the two operations by creating two zone groups.</span></span> <span data-ttu-id="70aea-133">为您的实体提供描述性名称，这样，当您在模板中查询时使用它们时容易识别它们。</span><span class="sxs-lookup"><span data-stu-id="70aea-133">Give your entities descriptive names, so that it's easy to identify them when you use them in template queries.</span></span>

### <a name="location-stocking-limits-location-profiles-and-fixed-picking-locations"></a><span data-ttu-id="70aea-134">位置储存限制、位置配置文件和固定领料位置</span><span class="sxs-lookup"><span data-stu-id="70aea-134">Location stocking limits, location profiles, and fixed picking locations</span></span>

<span data-ttu-id="70aea-135">必须考虑仓库的实际布局，从而确定存储容量（位置存储限制和位置配置文件）并且作为您的尝试的一部分实现最佳仓库流程。</span><span class="sxs-lookup"><span data-stu-id="70aea-135">You must consider the physical layout of the warehouse, both to determine storage capacities (location stocking limits and location profiles) and as part of your attempts to achieve optimal warehouse processes.</span></span> 

<span data-ttu-id="70aea-136">位置库存限制有助于确保不工作创建来请求将库存放入没有实际容量来容纳库存的位置。</span><span class="sxs-lookup"><span data-stu-id="70aea-136">Location stocking limits help guarantee that work isn't created to request that inventory be put in a location that doesn't have the physical capacity to carry the inventory.</span></span> <span data-ttu-id="70aea-137">例如，如果仓库内的某些位置只能为一个位置包含一个托盘，则可启用位置储存限制。</span><span class="sxs-lookup"><span data-stu-id="70aea-137">For example, if some locations within a warehouse can hold only one pallet per location, location stocking limits can be enabled.</span></span> <span data-ttu-id="70aea-138">在特定位置配置文件分组内，**数量**值可以设置为**1**，**单位**值可以设置为**PL**。</span><span class="sxs-lookup"><span data-stu-id="70aea-138">The **Quantity** value can be set to **1**, and the **Unit** value can be set to **PL** within a specific location profile grouping.</span></span> 

<span data-ttu-id="70aea-139">如果需要更多高级计算来控制位置容量限制，则可以使用位置配置文件设置。</span><span class="sxs-lookup"><span data-stu-id="70aea-139">If more advanced calculations are required to control the location capacity constraints, the location profile settings can be used.</span></span> <span data-ttu-id="70aea-140">在这种情况下，在完成计算容量后，会考虑重量和体积。</span><span class="sxs-lookup"><span data-stu-id="70aea-140">In this case, the weight and volume are considered when capacity calculations are done.</span></span> 

<span data-ttu-id="70aea-141">若要实现最佳出货流程，您应评估是否使用固定领料位置和/或包装位置。</span><span class="sxs-lookup"><span data-stu-id="70aea-141">To achieve optimal outbound processes, you should evaluate whether to use fixed picking locations and/or packing locations.</span></span> <span data-ttu-id="70aea-142">通常，最小/最大补货用于从堆放区到固定领料位置的补货流程，并且可以为产品变型在同一仓库内启用多个固定领料位置。</span><span class="sxs-lookup"><span data-stu-id="70aea-142">Often, minimum/maximum replenishment is used for replenishment processes from a bulk area to the fixed picking locations, and multiple fixed picking locations can be enabled within the same warehouse and for product variants.</span></span> <span data-ttu-id="70aea-143">考虑您可以通过启用专用需求补货溢出位置（仅用于波次/负荷补货处理）实现的灵活性。</span><span class="sxs-lookup"><span data-stu-id="70aea-143">Consider the flexibility that can you achieve by enabling dedicated demand replenishment overflow locations that are used only for wave/load replenishment processing.</span></span>

### <a name="location-setup-wizard"></a><span data-ttu-id="70aea-144">库位设置向导</span><span class="sxs-lookup"><span data-stu-id="70aea-144">Location setup wizard</span></span>

<span data-ttu-id="70aea-145">若要快速在仓库内创建位置，您可以使用**设置位置**向导。</span><span class="sxs-lookup"><span data-stu-id="70aea-145">To quickly create the locations within a warehouse, you can use the **Location setup** wizard.</span></span> <span data-ttu-id="70aea-146">作为此流程的一部分，您可以轻松地维护位置名称的格式。</span><span class="sxs-lookup"><span data-stu-id="70aea-146">As part of this process, you can easily maintain the format of the location names.</span></span>

## <a name="warehouse-processes"></a><span data-ttu-id="70aea-147">仓库流程</span><span class="sxs-lookup"><span data-stu-id="70aea-147">Warehouse processes</span></span>
<span data-ttu-id="70aea-148">作为仓库部署的一部分，您一定要根据业务要求启用仓库流程。</span><span class="sxs-lookup"><span data-stu-id="70aea-148">As part of the configuration of the warehouse, it's important that you enable warehouse processes according to business requirements.</span></span> <span data-ttu-id="70aea-149">必须配置的最重要组件是通知波次模板、工作模板、工作池和位置指令。</span><span class="sxs-lookup"><span data-stu-id="70aea-149">The most important components that you must configure are wave templates, work templates, work pools, and location directives.</span></span>

### <a name="wave-templates"></a><span data-ttu-id="70aea-150">波动模板</span><span class="sxs-lookup"><span data-stu-id="70aea-150">Wave templates</span></span>

<span data-ttu-id="70aea-151">波次模板可帮助启用传出版本“发放到仓库”流程。</span><span class="sxs-lookup"><span data-stu-id="70aea-151">Wave templates help enable the outbound "Release to warehouse" process.</span></span> <span data-ttu-id="70aea-152">在下达订单行（直接从源文档、通过批处理作业流程，或者通过已经创建的负载）后，会使用波次模板功能。</span><span class="sxs-lookup"><span data-stu-id="70aea-152">As soon as order lines are released (either directly from source documents, via batch job processes, or via loads that have already been created), the wave template functionality is used.</span></span> 

<span data-ttu-id="70aea-153">您可以创建三类波次模板：</span><span class="sxs-lookup"><span data-stu-id="70aea-153">You can create three types of wave templates:</span></span> 
-   <span data-ttu-id="70aea-154">**装运**</span><span class="sxs-lookup"><span data-stu-id="70aea-154">**Shipping**</span></span>
-   <span data-ttu-id="70aea-155">**生产订单**</span><span class="sxs-lookup"><span data-stu-id="70aea-155">**Production order**</span></span>
-   <span data-ttu-id="70aea-156">**看板**</span><span class="sxs-lookup"><span data-stu-id="70aea-156">**Kanban**</span></span> 

<span data-ttu-id="70aea-157">参数用于定义系统在传出工作处理中应自动运行的程度。</span><span class="sxs-lookup"><span data-stu-id="70aea-157">Parameters are used to define how far the system should automatically go in the outbound work processing.</span></span> <span data-ttu-id="70aea-158">波次模板是基于在模板中指定的波次模板顺序和标准而选择的。</span><span class="sxs-lookup"><span data-stu-id="70aea-158">A wave template is selected based on the wave template sequence and criteria that are specified in the template.</span></span> <span data-ttu-id="70aea-159">如果模板列在该序列的顶部，则首先检查该模板中的条件。</span><span class="sxs-lookup"><span data-stu-id="70aea-159">If a template is listed at the top of the sequence, the criteria in that template are checked first.</span></span> <span data-ttu-id="70aea-160">如果可以满足条件，则会处理波次模板。</span><span class="sxs-lookup"><span data-stu-id="70aea-160">If the criteria can be met, the wave template is processed.</span></span> <span data-ttu-id="70aea-161">否则，会检查下一个模板中的条件，等等。</span><span class="sxs-lookup"><span data-stu-id="70aea-161">Otherwise, the criteria in the next template are checked, and so on.</span></span> <span data-ttu-id="70aea-162">因此，最好将具有最具体条件的模板放在波次模板顺序列表顶部，因此，它会首先被处理。</span><span class="sxs-lookup"><span data-stu-id="70aea-162">Therefore, it's a good idea to put the template that has the most specific criteria at the top of the wave template sequence list, so that it's processed first.</span></span> <span data-ttu-id="70aea-163">例如，如果您要处理今天特定承运人的所有工作并临时延迟处理其他承运人的工作。</span><span class="sxs-lookup"><span data-stu-id="70aea-163">For example, you want to process all the work for a specific carrier today and temporarily delay processing of the work for other carriers.</span></span> <span data-ttu-id="70aea-164">在这种情况下，为该承运人选择工作的波次模板应列在序列中比其他模板更高的位置。</span><span class="sxs-lookup"><span data-stu-id="70aea-164">In this case, the wave template that selects work for that carrier should be listed higher in the sequence than other templates.</span></span> <span data-ttu-id="70aea-165">否则，其他承运人的工作可能在该承运人的工作完成前处理。</span><span class="sxs-lookup"><span data-stu-id="70aea-165">Otherwise, the work for other carriers might be processed before the work for that carrier is completed.</span></span> 

<span data-ttu-id="70aea-166">您必须在每个波次模板中指定波次流程方法。</span><span class="sxs-lookup"><span data-stu-id="70aea-166">You must specify the wave process methods in each wave template.</span></span> <span data-ttu-id="70aea-167">可用的方法根据波次模板类型而不同。</span><span class="sxs-lookup"><span data-stu-id="70aea-167">The methods that are available vary, depending on the wave template type.</span></span>

### <a name="work-templates"></a><span data-ttu-id="70aea-168">工作模板</span><span class="sxs-lookup"><span data-stu-id="70aea-168">Work templates</span></span>

<span data-ttu-id="70aea-169">工作模板定义在仓库管理工作流程的定义中扮演重要角色。</span><span class="sxs-lookup"><span data-stu-id="70aea-169">Work template definitions play an important role in the definition of warehouse management work processes.</span></span> <span data-ttu-id="70aea-170">它们定义执行哪些工作，以及该工作如何完成。</span><span class="sxs-lookup"><span data-stu-id="70aea-170">They define what work is performed, and how the work is done.</span></span> <span data-ttu-id="70aea-171">模板还可以包含一个指令代码，链接到一个位置指令来确定在哪里执行工作。</span><span class="sxs-lookup"><span data-stu-id="70aea-171">Templates can also contain a directive code that links to a location directive to determine where work is performed.</span></span> <span data-ttu-id="70aea-172">工作模板包括为该工作指定条件的查询。</span><span class="sxs-lookup"><span data-stu-id="70aea-172">Work templates include a query that specifies the criteria for the work.</span></span> <span data-ttu-id="70aea-173">每个模板必须包含至少一个领料工序和一个放入工序，才能将转移现有库存的基本工作工序从一个位置转移到另一个位置。</span><span class="sxs-lookup"><span data-stu-id="70aea-173">Each template must include at least one Pick operation and one Put operation to drive the basic work operation of transferring on-hand inventory from one location to another.</span></span> 

<span data-ttu-id="70aea-174">如果多个工作人员必须能够为某些仓库工序处理工作，您可能希望对库存使用 *“暂存”* 概念并将工作执行分开到不同的工作类中。</span><span class="sxs-lookup"><span data-stu-id="70aea-174">If multiple workers must be able to process work for some of your warehouse operations, you might want to use the concept of *staging* for the inventory and separate the work execution into different work classes.</span></span>

### <a name="work-pools"></a><span data-ttu-id="70aea-175">工作池</span><span class="sxs-lookup"><span data-stu-id="70aea-175">Work pools</span></span>

<span data-ttu-id="70aea-176">工作池用于将工作组织到组。</span><span class="sxs-lookup"><span data-stu-id="70aea-176">Work pools are used to organize work into groups.</span></span> <span data-ttu-id="70aea-177">例如，您可以创建工作池以为在特定仓库库位进行的工作分类。</span><span class="sxs-lookup"><span data-stu-id="70aea-177">For example, you can create a work pool to classify work that occurs in a particular warehouse location.</span></span> <span data-ttu-id="70aea-178">对于所有工作类型（除了盘点），您可以将工作池分配给工作模板。</span><span class="sxs-lookup"><span data-stu-id="70aea-178">For all work types except counting, you can assign a work pool to a work template.</span></span> <span data-ttu-id="70aea-179">对于周期盘点，您可以在以下页面上分配工作池：</span><span class="sxs-lookup"><span data-stu-id="70aea-179">For cycle counting, you can assign a work pool on the following pages:</span></span>

-   <span data-ttu-id="70aea-180">周期盘点计划</span><span class="sxs-lookup"><span data-stu-id="70aea-180">Cycle count plans</span></span>
-   <span data-ttu-id="70aea-181">周期盘点阈值</span><span class="sxs-lookup"><span data-stu-id="70aea-181">Cycle count thresholds</span></span>
-   <span data-ttu-id="70aea-182">按位置分类的周期盘点工作</span><span class="sxs-lookup"><span data-stu-id="70aea-182">Cycle count work by location</span></span>
-   <span data-ttu-id="70aea-183">按物料分类的周期盘点工作</span><span class="sxs-lookup"><span data-stu-id="70aea-183">Cycle count work by item</span></span>

<span data-ttu-id="70aea-184">在您使用工作模板创建工作时，工作池会被自动分配给该工作。</span><span class="sxs-lookup"><span data-stu-id="70aea-184">When you use work templates to create work, the work pool is automatically assigned to the work.</span></span> 

<span data-ttu-id="70aea-185">工作池 ID 还可用于限制导向给特定仓库工作人员的工作类型，前提条件是在相关移动设备菜单项上配置了该功能。</span><span class="sxs-lookup"><span data-stu-id="70aea-185">Work pool IDs can also be used to limit the type of work that is directed to a particular warehouse worker, provided that this functionality is configured on the relevant mobile device menu item.</span></span>

### <a name="location-directives"></a><span data-ttu-id="70aea-186">位置指令</span><span class="sxs-lookup"><span data-stu-id="70aea-186">Location directives</span></span>

<span data-ttu-id="70aea-187">如名称所提示的那样，位置指令用于将工作交易记录导向到仓库中正确的位置。</span><span class="sxs-lookup"><span data-stu-id="70aea-187">As the name suggests, location directives are used to direct the work transactions to the appropriate locations in the warehouse.</span></span> <span data-ttu-id="70aea-188">换言之，它们定义在哪里领料和放入。</span><span class="sxs-lookup"><span data-stu-id="70aea-188">In other words, they define where to pick and put.</span></span> 

<span data-ttu-id="70aea-189">为了更方便、更快地定义与每个位置指示行关联的操作，请使用一个预定义策略。</span><span class="sxs-lookup"><span data-stu-id="70aea-189">To make it easier and quicker to define the actions that are associated with each location directive line, use one of the predefined strategies.</span></span> <span data-ttu-id="70aea-190">例如，您可以使用**没有传入工作的空库位**策略搜索仓库中的可用位置，或者为传出销售领料使用**先过期先出批次预留**策略。</span><span class="sxs-lookup"><span data-stu-id="70aea-190">For example, you can use the **Empty location with no incoming work** strategy to search for free locations in a warehouse, or you can use **FEFO batch reservation** strategy for outbound sales picking.</span></span>

<a name="additional-resources"></a><span data-ttu-id="70aea-191">其他资源</span><span class="sxs-lookup"><span data-stu-id="70aea-191">Additional resources</span></span>
--------

[<span data-ttu-id="70aea-192">在启用 WMS 的仓库中配置位置（任务指南）</span><span class="sxs-lookup"><span data-stu-id="70aea-192">Configure locations in a WMS-enabled warehouse (Task guide)</span></span>](tasks/configure-locations-wms-enabled-warehouse.md)




