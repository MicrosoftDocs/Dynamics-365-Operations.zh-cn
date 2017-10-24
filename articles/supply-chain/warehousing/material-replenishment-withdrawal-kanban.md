---
title: "通过提领看板补货"
description: "此主题介绍如何使用提领看板进行物料补货用于制造活动。"
author: johanhoffmann
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: KanbanBoardTransferJob, KanbanFlow, KanbanRules
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 152b7908364db82481c5af4a05a9775fbabca042
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---

# <a name="replenishment-with-withdrawal-kanbans"></a><span data-ttu-id="9aeb7-103">通过提领看板补货</span><span class="sxs-lookup"><span data-stu-id="9aeb7-103">Replenishment with withdrawal kanbans</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="9aeb7-104">此主题介绍如何使用提领看板进行物料补货用于制造活动。</span><span class="sxs-lookup"><span data-stu-id="9aeb7-104">This topic describes how the withdrawal kanban is used for material replenishment for manufacturing activities.</span></span>

## <a name="workflow-for-material-replenishment-that-uses-the-withdrawal-kanban"></a><span data-ttu-id="9aeb7-105">使用提领看板进行物料补货的工作流</span><span class="sxs-lookup"><span data-stu-id="9aeb7-105">Workflow for material replenishment that uses the withdrawal kanban</span></span>
-------------------------------------------------------------------

<span data-ttu-id="9aeb7-106">提领看板可用于将单个物料的看板在仓库和使用物料的生产库位之间移动。</span><span class="sxs-lookup"><span data-stu-id="9aeb7-106">The withdrawal kanban can be used to move a kanban of a single item between warehouses and production locations where the material is consumed.</span></span> <span data-ttu-id="9aeb7-107">提领看板支持基于提取的物料补货解决方案，其中要求通过提取信号触发特定需求的供应。</span><span class="sxs-lookup"><span data-stu-id="9aeb7-107">The withdrawal kanban supports a pull-based solution for material replenishment, where a pull signal is required in order to trigger supply for a specific demand.</span></span> 

<span data-ttu-id="9aeb7-108">以下方案显示提取信号触发看板的创建以对生产流程进行物料补货的基于提取的补货系统。</span><span class="sxs-lookup"><span data-stu-id="9aeb7-108">The following scenario shows a pull-based replenishment system where a pull signal triggers the creation of a kanban to replenish material for a production process.</span></span> 

<span data-ttu-id="9aeb7-109">[![提取信号触发看板的创建以对生产流程进行物料补货](./media/material-replenishment-with-withdrawal-kanban.png)](./media/material-replenishment-with-withdrawal-kanban.png)</span><span class="sxs-lookup"><span data-stu-id="9aeb7-109">[![Pull signal triggers the creation of a kanban to replenish material for a production process](./media/material-replenishment-with-withdrawal-kanban.png)](./media/material-replenishment-with-withdrawal-kanban.png)</span></span>

1.  <span data-ttu-id="9aeb7-110">提领看板</span><span class="sxs-lookup"><span data-stu-id="9aeb7-110">Withdrawal kanban</span></span>
2.  <span data-ttu-id="9aeb7-111">看板“源”库位和用于仓库工作的入库库位</span><span class="sxs-lookup"><span data-stu-id="9aeb7-111">Kanban “from” location and put location for warehouse work</span></span>
3.  <span data-ttu-id="9aeb7-112">看板“至”库位和生产输入库位</span><span class="sxs-lookup"><span data-stu-id="9aeb7-112">Kanban “to” location and production input location</span></span>
4.  <span data-ttu-id="9aeb7-113">制造流程</span><span class="sxs-lookup"><span data-stu-id="9aeb7-113">Manufacturing process</span></span>
5.  <span data-ttu-id="9aeb7-114">仓库看板领料工作</span><span class="sxs-lookup"><span data-stu-id="9aeb7-114">Warehouse work for kanban picking</span></span>
6.  <span data-ttu-id="9aeb7-115">仓库原材料库位</span><span class="sxs-lookup"><span data-stu-id="9aeb7-115">Warehouse locations for raw material</span></span>
7.  <span data-ttu-id="9aeb7-116">物料仓库</span><span class="sxs-lookup"><span data-stu-id="9aeb7-116">Material warehouse</span></span>
8.  <span data-ttu-id="9aeb7-117">制造仓库</span><span class="sxs-lookup"><span data-stu-id="9aeb7-117">Manufacturing warehouse</span></span>

<span data-ttu-id="9aeb7-118">在此方案中，制造流程 (4) 使用来自制造仓库 (8) 的生产输入库位 (3) 的物料。</span><span class="sxs-lookup"><span data-stu-id="9aeb7-118">In this scenario, a manufacturing process (4) consumes material from a production input location (3) in the manufacturing warehouse (8).</span></span> <span data-ttu-id="9aeb7-119">使用物料处理单元（看板）时，其登记为空。</span><span class="sxs-lookup"><span data-stu-id="9aeb7-119">When a handling unit of the material (kanban) is consumed, it’s registered as empty.</span></span> <span data-ttu-id="9aeb7-120">为物料来源创建补货信号，且创建新看板 (1)。</span><span class="sxs-lookup"><span data-stu-id="9aeb7-120">A replenishment signal is created for the item origin, and a new kanban (1) is created.</span></span> <span data-ttu-id="9aeb7-121">在这种情况下，物料来源包括物料仓库 (7) 中的库位。</span><span class="sxs-lookup"><span data-stu-id="9aeb7-121">In this case, the item origin consists of locations in the material warehouse (7).</span></span> <span data-ttu-id="9aeb7-122">看板物料领料并入库到相同仓库的库位 (2)。</span><span class="sxs-lookup"><span data-stu-id="9aeb7-122">The material for the kanban is picked and put to a location (2) in the same warehouse.</span></span> <span data-ttu-id="9aeb7-123">领取物料后，可以准备从库位 2 转移到制造仓库 (8) 中的生产输入库位 (3)。</span><span class="sxs-lookup"><span data-stu-id="9aeb7-123">When the material is picked, it’s ready to be transferred from location 2 to the production input location (3) in the manufacturing warehouse (8).</span></span>

## <a name="configure-warehouse-work-for-kanban-picking-for-the-withdrawal-kanban"></a><span data-ttu-id="9aeb7-124">为提领看板配置仓库看板领料工作</span><span class="sxs-lookup"><span data-stu-id="9aeb7-124">Configure warehouse work for kanban picking for the withdrawal kanban</span></span>

<span data-ttu-id="9aeb7-125">要启用提领看板的原材料领取，则为**看板领料**工作订单类型配置波次模板、工作模板和库位指令。</span><span class="sxs-lookup"><span data-stu-id="9aeb7-125">To enable raw material picking for the withdrawal kanban, configure wave templates, work templates, and location directives for the **Kanban picking** work order type.</span></span> <span data-ttu-id="9aeb7-126">此工作订单类型不仅支持提领看板的领料流程。</span><span class="sxs-lookup"><span data-stu-id="9aeb7-126">This work order type doesn’t just support the picking process for the withdrawal kanban.</span></span> <span data-ttu-id="9aeb7-127">它还支持制造看板的领料流程。</span><span class="sxs-lookup"><span data-stu-id="9aeb7-127">It also supports the picking process for the manufacturing kanban.</span></span> <span data-ttu-id="9aeb7-128">但是，您可以通过界定波次模板、工作模板和库位指令的方式为每种看板类型配置单独的领料流程。</span><span class="sxs-lookup"><span data-stu-id="9aeb7-128">However, you can configure a separate picking process for each type of kanban by separating the wave templates, work templates, and location directives.</span></span> <span data-ttu-id="9aeb7-129">要界定波次模板、工作模板和库位指令，请在这些实体的查询中对该活动类型（**流程**或**转移**）设置条件</span><span class="sxs-lookup"><span data-stu-id="9aeb7-129">To separate the wave templates, work templates, and location directives, set criteria on the activity type (**Process** or **Transfer**) in the queries for those entities.</span></span>

## <a name="configure-the-withdrawal-kanban"></a><span data-ttu-id="9aeb7-130">配置提领看板</span><span class="sxs-lookup"><span data-stu-id="9aeb7-130">Configure the withdrawal kanban</span></span>

<span data-ttu-id="9aeb7-131">用于提领看板的转移活动配置为精益生产流中激活的活动计划的一部分。</span><span class="sxs-lookup"><span data-stu-id="9aeb7-131">The transfer activity that is used for the withdrawal kanban is configured as part of an activated activity plan in a Lean production flow.</span></span> <span data-ttu-id="9aeb7-132">作为配置转移活动的一部分，您指定转移的“自”和“到”库位。</span><span class="sxs-lookup"><span data-stu-id="9aeb7-132">As part of the configuration of the transfer activity, you specify the “from” and “to” locations for the transfer.</span></span> <span data-ttu-id="9aeb7-133">配置转移活动后，您可以将其分配到**提领**类型的看板规则。</span><span class="sxs-lookup"><span data-stu-id="9aeb7-133">After you configure the transfer activity, you can assign it to a kanban rule of the **Withdrawal** type.</span></span> <span data-ttu-id="9aeb7-134">看板规则设定提领看板的策略和配置。</span><span class="sxs-lookup"><span data-stu-id="9aeb7-134">The kanban rule sets the policies and configurations for the withdrawal kanban.</span></span> <span data-ttu-id="9aeb7-135">看板的数量定义看板在转移流程期间携带多少个物料处理单元。</span><span class="sxs-lookup"><span data-stu-id="9aeb7-135">The quantity of the kanban defines how many units of the handling unit the kanban carries during the transfer process.</span></span> <span data-ttu-id="9aeb7-136">选择固定补货策略时使用固定看板数量。</span><span class="sxs-lookup"><span data-stu-id="9aeb7-136">The fixed kanban quantity is used when the Fixed replenishment strategy is selected.</span></span> <span data-ttu-id="9aeb7-137">此数量定义为了防止存货或版本存货在需求源被耗尽所需的看板数量。</span><span class="sxs-lookup"><span data-stu-id="9aeb7-137">This quantity defines how many kanbans that are required in order to prevent stock or build inventory from running out at the source of demand.</span></span> <span data-ttu-id="9aeb7-138">固定数量可以基于实际需求、历史需求和服务级别进行计算。</span><span class="sxs-lookup"><span data-stu-id="9aeb7-138">The fixed quantity can be calculated based on actual demand, historical demand, and service levels.</span></span> <span data-ttu-id="9aeb7-139">以下两个方案介绍如何管理使用提领看板的物料补货。</span><span class="sxs-lookup"><span data-stu-id="9aeb7-139">The following two scenarios describe how you can manage material replenishment that uses the withdrawal kanban.</span></span>

## <a name="scenario-1-replenish-a-production-input-location-by-using-a-fixed-withdrawal-kanban"></a><span data-ttu-id="9aeb7-140">方案 1：使用固定提领看板对生产输入库位补货</span><span class="sxs-lookup"><span data-stu-id="9aeb7-140">Scenario 1: Replenish a production input location by using a fixed withdrawal kanban</span></span>

<span data-ttu-id="9aeb7-141">制造流程使用来自生产仓库中的生产输入库位的已购买的原材料。</span><span class="sxs-lookup"><span data-stu-id="9aeb7-141">A manufacturing process consumes a purchased raw material from a production input location that is in the production warehouse.</span></span> <span data-ttu-id="9aeb7-142">收到供应商提供的原材料后，存储到物料仓库的库位中。</span><span class="sxs-lookup"><span data-stu-id="9aeb7-142">When the raw material is received from the vendor, it’s stored in locations in the material warehouse.</span></span> <span data-ttu-id="9aeb7-143">由于对物料的需求在一段时间内被视为稳定，因为设置为在固定数量看板流中供应生产。</span><span class="sxs-lookup"><span data-stu-id="9aeb7-143">Because the demand for the material is considered stable over a period, it’s set up to supply the production in a fixed quantity kanban flow.</span></span> <span data-ttu-id="9aeb7-144">在生产输入库位使用看板时，将登记空信号，并在流中添加一个相同类型的新看板。</span><span class="sxs-lookup"><span data-stu-id="9aeb7-144">When a kanban is consumed at the production input location, an empty signal is registered, and a new kanban of the same type is added to the flow.</span></span> 

<span data-ttu-id="9aeb7-145">空信号可以配置为在完成看板时自动发生。</span><span class="sxs-lookup"><span data-stu-id="9aeb7-145">The empty signal can be configured to occur automatically when a kanban is completed.</span></span> <span data-ttu-id="9aeb7-146">或者，空信号可以设置为从看板转移面板或手持设备上的菜单提供的手动交互。</span><span class="sxs-lookup"><span data-stu-id="9aeb7-146">Alternatively, the empty signal can be set up as a manual interaction that is given either from the Kanban transfer board or from a menu on the hand-held device.</span></span> <span data-ttu-id="9aeb7-147">看板转移面板是管理看板生命周期中的所有活动的工作区。</span><span class="sxs-lookup"><span data-stu-id="9aeb7-147">The Kanban transfer board is the workspace where all activities in the kanban life cycle are managed.</span></span> 

<span data-ttu-id="9aeb7-148">创建看板后，原材料的波次行被添加到物料仓库的看板波次。</span><span class="sxs-lookup"><span data-stu-id="9aeb7-148">When the kanban is created, a wave line for the raw material is added to a kanban wave for the material warehouse.</span></span> <span data-ttu-id="9aeb7-149">在看板转移面板的领料单部分，可以监控从波次创建到工作创建的物料和相关仓库流程的状态，直到物料在“转移自”库位中现有且已准备好随时被转移到生产输入库位。</span><span class="sxs-lookup"><span data-stu-id="9aeb7-149">In the picking list section of the Kanban transfer board, the status of the material and related warehouse processes can be monitored from wave creation to work creation, until the material is on-hand in the “transfer from” location and is ready to be transferred to the production input locations.</span></span> <span data-ttu-id="9aeb7-150">可以从看板转移模板或从手持设备的菜单完成看板。</span><span class="sxs-lookup"><span data-stu-id="9aeb7-150">The kanban can be completed either from the Kanban transfer board or from a menu on the hand-held device.</span></span> 

<span data-ttu-id="9aeb7-151">在此方案中，物料仓库中的领料单被作为一个活动进行处理。</span><span class="sxs-lookup"><span data-stu-id="9aeb7-151">In this scenario, the picking work in the material warehouse is processed as one activity.</span></span> <span data-ttu-id="9aeb7-152">物料仓库与生产仓库之间的转移活动被作为一个单独的活动进行处理。</span><span class="sxs-lookup"><span data-stu-id="9aeb7-152">The transfer activity between the material warehouse and the production warehouse is processed as a separate activity.</span></span> <span data-ttu-id="9aeb7-153">此方法可能很有用，例如如果两个仓库之间的实际距离较大时。</span><span class="sxs-lookup"><span data-stu-id="9aeb7-153">This approach can be useful if, for example, there is a large physical distance between the two warehouses.</span></span> <span data-ttu-id="9aeb7-154">在这种情况下，看板转移活动可以表示卡车负荷。</span><span class="sxs-lookup"><span data-stu-id="9aeb7-154">In this case, the kanban transfer activity can represent a truck load.</span></span> 

<span data-ttu-id="9aeb7-155">如果仓库库位与生产输入库位之间的距离较短，则将转移活动包括在领料流程中可能更有效。</span><span class="sxs-lookup"><span data-stu-id="9aeb7-155">If the distance between the warehouse locations and the production input location is small, it might be more efficient to include the transfer activity in the picking process.</span></span> <span data-ttu-id="9aeb7-156">物料领料后，可以直接入库到生产输入库位。</span><span class="sxs-lookup"><span data-stu-id="9aeb7-156">Then, after the material is picked, it can be put directly to the production input location.</span></span> <span data-ttu-id="9aeb7-157">为了支持此流程，您将转移活动配置为处理提领看板的领料工作时自动完成。</span><span class="sxs-lookup"><span data-stu-id="9aeb7-157">To support this process, you configure the transfer activity so that it’s automatically completed when the pick work of the withdrawal kanban is processed.</span></span>

## <a name="scenario-2-automatically-complete-the-transfer-activity-when-kanban-picking-work-is-processed"></a><span data-ttu-id="9aeb7-158">方案 2：处理看板领料工作时自动完成转移活动</span><span class="sxs-lookup"><span data-stu-id="9aeb7-158">Scenario 2: Automatically complete the transfer activity when kanban picking work is processed</span></span>

<span data-ttu-id="9aeb7-159">在以下方案中，提领看板的转移活动配置为在同一仓库的两个库位之间转移。</span><span class="sxs-lookup"><span data-stu-id="9aeb7-159">In the following scenario, the transfer activity of the withdrawal kanban is configured to transfer between two locations in the same warehouse.</span></span> <span data-ttu-id="9aeb7-160">提领看板的转移活动设置为自动完成。</span><span class="sxs-lookup"><span data-stu-id="9aeb7-160">The transfer activity of the withdrawal kanban is set up so that it’s completed automatically.</span></span> 

<span data-ttu-id="9aeb7-161">[![处理看板领料工作时自动完成转移活动](./media/transfer-activities-when-processing-kanban-picking.png)](./media/transfer-activities-when-processing-kanban-picking.png)</span><span class="sxs-lookup"><span data-stu-id="9aeb7-161">[![Transfer activity is automatically completed when kanban picking work is processed](./media/transfer-activities-when-processing-kanban-picking.png)](./media/transfer-activities-when-processing-kanban-picking.png)</span></span>

1.  <span data-ttu-id="9aeb7-162">原材料和生产的共享仓库</span><span class="sxs-lookup"><span data-stu-id="9aeb7-162">Shared warehouse for raw materials and production</span></span>
2.  <span data-ttu-id="9aeb7-163">原材料的仓库库位</span><span class="sxs-lookup"><span data-stu-id="9aeb7-163">Warehouse locations for raw materials</span></span>
3.  <span data-ttu-id="9aeb7-164">看板“源”库位和用于仓库工作的入库库位</span><span class="sxs-lookup"><span data-stu-id="9aeb7-164">Kanban “from” location and put location for warehouse work</span></span>
4.  <span data-ttu-id="9aeb7-165">提领看板</span><span class="sxs-lookup"><span data-stu-id="9aeb7-165">Withdrawal kanban</span></span>
5.  <span data-ttu-id="9aeb7-166">生产输入地点</span><span class="sxs-lookup"><span data-stu-id="9aeb7-166">Production input location</span></span>
6.  <span data-ttu-id="9aeb7-167">制造流程</span><span class="sxs-lookup"><span data-stu-id="9aeb7-167">Manufacturing process</span></span>

<span data-ttu-id="9aeb7-168">在生产输入库位使用看板后，看板报告为空，并在流中添加一个新看板。</span><span class="sxs-lookup"><span data-stu-id="9aeb7-168">After a kanban is consumed at the production input location, the kanban is reported as empty, and a new kanban is added to the flow.</span></span> <span data-ttu-id="9aeb7-169">创建看板后，在看板波次中添加一个波次行。</span><span class="sxs-lookup"><span data-stu-id="9aeb7-169">When the kanban is created, a wave line is added to a kanban wave.</span></span> <span data-ttu-id="9aeb7-170">处理看板波次后，创建看板领料的仓库工作。</span><span class="sxs-lookup"><span data-stu-id="9aeb7-170">When the kanban wave is processed, warehouse work for kanban picking is created.</span></span> <span data-ttu-id="9aeb7-171">仓库工作人员处理看板领料工作，并按照工作的指示在仓库库位中领取看板物料。</span><span class="sxs-lookup"><span data-stu-id="9aeb7-171">The warehouse worker processes the work for kanban picking and is directed by the work to pick the material for the kanban in a warehouse location.</span></span> <span data-ttu-id="9aeb7-172">在此仓库工作人员确认领料后，看板自动完成，并指导仓库工作人员将物料入库到生产输入库位。</span><span class="sxs-lookup"><span data-stu-id="9aeb7-172">As this warehouse worker confirms the pick, the kanban is automatically completed, and the warehouse worker is guided to the put the material to the production input location.</span></span>

