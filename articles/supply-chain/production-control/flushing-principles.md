---
title: 耗用原则
description: 本主题描述为原材料消耗量使用的四个耗用原则。
author: johanhoffmann
manager: tfehr
ms.date: 04/04/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgShopSupervisorReleaseOrders
audience: Application User
ms.reviewer: kamaybac
ms.custom: 221264
ms.assetid: dde49743-1541-4353-a030-63ca3069cd7d
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 84be2a4646cfc18cd1f25a4ec969acdb62cb2856
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "5007233"
---
# <a name="flushing-principles"></a><span data-ttu-id="7f0cc-103">耗用原则</span><span class="sxs-lookup"><span data-stu-id="7f0cc-103">Flushing principles</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7f0cc-104">耗用原则反映用于生产流程中使用的原材料的不同的消耗策略。</span><span class="sxs-lookup"><span data-stu-id="7f0cc-104">The flushing principles reflect different consumption strategies for raw materials that are used in production processes.</span></span> <span data-ttu-id="7f0cc-105">消耗是从现有库存量中扣减物料并为生产订单和批次订单将已消耗物料的值设置为 **在制品** (WIP) 的流程。</span><span class="sxs-lookup"><span data-stu-id="7f0cc-105">Consumption is the process that deducts material from the on-hand inventory and sets the value of the consumed materials to **Work in progress** (WIP) for production orders and batch orders.</span></span> <span data-ttu-id="7f0cc-106">原材料通常从为使用物料的流程配置的位置使用。</span><span class="sxs-lookup"><span data-stu-id="7f0cc-106">Raw materials are usually consumed from a location that is configured for the process that consumes the material.</span></span> <span data-ttu-id="7f0cc-107">此位置称作生产输入位置。</span><span class="sxs-lookup"><span data-stu-id="7f0cc-107">This location is known as the production input location.</span></span>

<span data-ttu-id="7f0cc-108">在物料消耗前，物料移至输入位置。</span><span class="sxs-lookup"><span data-stu-id="7f0cc-108">Before material consumption, the materials are moved to the input location.</span></span> <span data-ttu-id="7f0cc-109">下图显示了此流程。</span><span class="sxs-lookup"><span data-stu-id="7f0cc-109">The following illustration shows the process.</span></span>

<span data-ttu-id="7f0cc-110">[![scenario4a](./media/scenario4a.png)](./media/scenario4a.png)</span><span class="sxs-lookup"><span data-stu-id="7f0cc-110">[![scenario4a](./media/scenario4a.png)](./media/scenario4a.png)</span></span>

1. <span data-ttu-id="7f0cc-111">物料仓库</span><span class="sxs-lookup"><span data-stu-id="7f0cc-111">Material warehouse</span></span>
2. <span data-ttu-id="7f0cc-112">原材料领取</span><span class="sxs-lookup"><span data-stu-id="7f0cc-112">Raw material picking</span></span>
3. <span data-ttu-id="7f0cc-113">生产输入地点</span><span class="sxs-lookup"><span data-stu-id="7f0cc-113">Production input location</span></span>
4. <span data-ttu-id="7f0cc-114">原材料消耗量</span><span class="sxs-lookup"><span data-stu-id="7f0cc-114">Raw material consumption</span></span>
5. <span data-ttu-id="7f0cc-115">生产流程</span><span class="sxs-lookup"><span data-stu-id="7f0cc-115">Production process</span></span>

<span data-ttu-id="7f0cc-116">原材料消耗量通过以下四个耗用原则进行控制：</span><span class="sxs-lookup"><span data-stu-id="7f0cc-116">Material consumption is controlled by the following four flushing principles:</span></span>

- <span data-ttu-id="7f0cc-117">手动</span><span class="sxs-lookup"><span data-stu-id="7f0cc-117">Manual</span></span>
- <span data-ttu-id="7f0cc-118">启动</span><span class="sxs-lookup"><span data-stu-id="7f0cc-118">Start</span></span>
- <span data-ttu-id="7f0cc-119">完成</span><span class="sxs-lookup"><span data-stu-id="7f0cc-119">Finish</span></span>
- <span data-ttu-id="7f0cc-120">在库位可用</span><span class="sxs-lookup"><span data-stu-id="7f0cc-120">Available at location</span></span>

<span data-ttu-id="7f0cc-121">耗用原则在默认值层次结构中进行配置。</span><span class="sxs-lookup"><span data-stu-id="7f0cc-121">The flushing principles are configured in a hierarchy of default values.</span></span> <span data-ttu-id="7f0cc-122">层次结构从已发放的产品开始，此时耗用原则的值为 **开始**。</span><span class="sxs-lookup"><span data-stu-id="7f0cc-122">The hierarchy starts at the released product, where the flushing principle has the value **Start**.</span></span> <span data-ttu-id="7f0cc-123">在物料清单 (BOM) 或配方行上，可以覆盖来自产品的耗用原则。</span><span class="sxs-lookup"><span data-stu-id="7f0cc-123">On the bill of materials (BOM) or formula line, the flushing principle from the product can be overridden.</span></span> <span data-ttu-id="7f0cc-124">在生产 BOM 行或批次订单配方行上的默认耗用原则从产品或 BOM 或配方上被覆盖的值提取。</span><span class="sxs-lookup"><span data-stu-id="7f0cc-124">The default flushing principle on the production BOM lines or batch order formula lines is taken from the product or the overridden value on the BOM or formulas.</span></span>

## <a name="description-of-the-flushing-principles"></a><span data-ttu-id="7f0cc-125">耗用原则的描述</span><span class="sxs-lookup"><span data-stu-id="7f0cc-125">Description of the flushing principles</span></span>

### <a name="manual"></a><span data-ttu-id="7f0cc-126">手动</span><span class="sxs-lookup"><span data-stu-id="7f0cc-126">Manual</span></span>
<span data-ttu-id="7f0cc-127">手动耗用原则指示物料消耗量的登记由人工操作。</span><span class="sxs-lookup"><span data-stu-id="7f0cc-127">The Manual flushing principle indicates that the registration of material consumption is a manual operation.</span></span> <span data-ttu-id="7f0cc-128">例如，如果你希望能够跟踪时间，且因为跟踪目的而必须说明已使用的批号或序列号的数量，则与此原则有关。</span><span class="sxs-lookup"><span data-stu-id="7f0cc-128">This principle is relevant if, for example, you want to be able to track time, and the quantity of consumed batch numbers or serial numbers must be accounted for, for tracking purposes.</span></span> <span data-ttu-id="7f0cc-129">手动消耗量在生产领料单日志中登记。</span><span class="sxs-lookup"><span data-stu-id="7f0cc-129">Manual consumption is registered in a production picking list journal.</span></span> <span data-ttu-id="7f0cc-130">对于已启用高级仓库流程的物料，可以应用手持流。</span><span class="sxs-lookup"><span data-stu-id="7f0cc-130">For items that are enabled for advanced warehouse processes, a hand-held flow can be applied.</span></span>

### <a name="start"></a><span data-ttu-id="7f0cc-131">启动</span><span class="sxs-lookup"><span data-stu-id="7f0cc-131">Start</span></span>
<span data-ttu-id="7f0cc-132">“开始”耗用原则指示在开始执行生产订单时将自动使用物料。</span><span class="sxs-lookup"><span data-stu-id="7f0cc-132">The Start flushing principle indicates that material will be automatically consumed when the production order is started.</span></span> <span data-ttu-id="7f0cc-133">使用的物料量与开始的数量成比例。</span><span class="sxs-lookup"><span data-stu-id="7f0cc-133">The amount of material that is consumed is proportional to the quantity that is started.</span></span> <span data-ttu-id="7f0cc-134">当“开始”耗用原则与制造执行系统一起使用时，它也可以用于在开始操作或处理作业时耗用物料。</span><span class="sxs-lookup"><span data-stu-id="7f0cc-134">When the Start flushing principle is used together with the manufacturing execution system, it can also be used to flush materials when an operation or a process job is started.</span></span> <span data-ttu-id="7f0cc-135">例如，如果消耗量中的差异很小、物料为低价值物料、无跟踪需要或操作运行时间较短时，则与此原则有关。</span><span class="sxs-lookup"><span data-stu-id="7f0cc-135">This principle is relevant if, for example, the variance in the consumption is low, the materials are low-value materials, there are no tracking requirements, or there is a short run time on operations.</span></span> 

### <a name="finish"></a><span data-ttu-id="7f0cc-136">完成</span><span class="sxs-lookup"><span data-stu-id="7f0cc-136">Finish</span></span>
<span data-ttu-id="7f0cc-137">“完成”耗用原则指示当生产订单报告完工入库时，或当设置为使用物料的操作登记为已完成时将自动使用物料。</span><span class="sxs-lookup"><span data-stu-id="7f0cc-137">The Finish flushing principle indicates that material will be automatically consumed when the production order is reported as finished, or when an operation that is set up to consume the materials is registered as completed.</span></span> <span data-ttu-id="7f0cc-138">使用的物料量与报告完工入库的数量成比例。</span><span class="sxs-lookup"><span data-stu-id="7f0cc-138">The amount of material that is consumed is proportional to the quantity that is reported as finished.</span></span> <span data-ttu-id="7f0cc-139">当“完成”耗用原则与制造执行系统一起使用时，它也可以用于在完成操作或处理作业时耗用物料。</span><span class="sxs-lookup"><span data-stu-id="7f0cc-139">When the Finish flushing principle is used together with the manufacturing execution system, it can also be used to flush materials when an operation or a process job is completed.</span></span> <span data-ttu-id="7f0cc-140">此原则的适用情况与“开始”原则相同。</span><span class="sxs-lookup"><span data-stu-id="7f0cc-140">This principle is relevant in the same situations as the Start principle.</span></span> <span data-ttu-id="7f0cc-141">但是，“完成”原则适用于运行时间更长，且在操作完成前不应将物料设置为 WIP 的操作。</span><span class="sxs-lookup"><span data-stu-id="7f0cc-141">However, the Finish principle is for operations that have a longer run time, where materials should not be set to WIP before the operation is completed.</span></span> 

### <a name="available-at-location"></a><span data-ttu-id="7f0cc-142">在库位可用</span><span class="sxs-lookup"><span data-stu-id="7f0cc-142">Available at location</span></span>
<span data-ttu-id="7f0cc-143">“在库位可用”耗用原则指示当物料登记为生产领料时自动使用物料。</span><span class="sxs-lookup"><span data-stu-id="7f0cc-143">The Available at location flushing principle indicates that the material will be automatically consumed when it's registered as picked for production.</span></span> <span data-ttu-id="7f0cc-144">当原材料领料工作完成时，或当物料在生产输入库位可用且物料行被发放到仓库时，该物料登记为从库位领料。</span><span class="sxs-lookup"><span data-stu-id="7f0cc-144">The material is registered as picked from location when work for the raw material picking is completed, or when material is available on the production input location and the material line is released to the warehouse.</span></span> <span data-ttu-id="7f0cc-145">在批处理作业中对流程进行过帐期间生成领料单。</span><span class="sxs-lookup"><span data-stu-id="7f0cc-145">The picking list that is generated during the process is posted in a batch job.</span></span> <span data-ttu-id="7f0cc-146">例如，如果一个生产订单有多个领料活动，则与此原则有关。</span><span class="sxs-lookup"><span data-stu-id="7f0cc-146">This principle is relevant if, for example, you have many picking activities against one production order.</span></span> <span data-ttu-id="7f0cc-147">在这种情况下，你不必手动更新领料单，而且可以获得 WIP 余额的当前视图。</span><span class="sxs-lookup"><span data-stu-id="7f0cc-147">In this case, you don't have to update the picking list manually, and you can get a current view of the WIP balance.</span></span>
