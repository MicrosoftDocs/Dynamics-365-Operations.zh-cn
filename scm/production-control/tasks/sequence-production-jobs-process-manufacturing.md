--- 
title: "对流程制造的生产作业排序"
description: "此过程使用油漆产品作为示例显示如何根据颜色和包装大小的优先级排序计划订单。"
author: ChristianRytt
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: a25a4575ca1600b07b2dac5949c8775bcd162650
ms.contentlocale: zh-cn
ms.lasthandoff: 08/29/2017

---
# <a name="sequence-production-jobs-for-process-manufacturing"></a><span data-ttu-id="e3812-103">对流程制造的生产作业排序</span><span class="sxs-lookup"><span data-stu-id="e3812-103">Sequence production jobs for process manufacturing</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e3812-104">此过程使用油漆产品作为示例显示如何根据颜色和包装大小的优先级排序计划订单。</span><span class="sxs-lookup"><span data-stu-id="e3812-104">This procedure uses paint products as an example to show how to sequence planned orders according to the priority of color and package size.</span></span> <span data-ttu-id="e3812-105">创建此程序的演示数据公司是 USPI。</span><span class="sxs-lookup"><span data-stu-id="e3812-105">The demo data company used to create this procedure is USPI.</span></span> <span data-ttu-id="e3812-106">此程序是专为生产规划员设计的。</span><span class="sxs-lookup"><span data-stu-id="e3812-106">This procedure is intended for the production planner.</span></span>


## <a name="run-master-planning-for-uspi"></a><span data-ttu-id="e3812-107">运行 USPI 的主计划</span><span class="sxs-lookup"><span data-stu-id="e3812-107">Run master planning for USPI</span></span>
1. <span data-ttu-id="e3812-108">转到“主计划”>“主计划”>“运行”>“主计划”。</span><span class="sxs-lookup"><span data-stu-id="e3812-108">Go to Master planning > Master planning > Run > Master planning.</span></span>
2. <span data-ttu-id="e3812-109">在“主计划”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="e3812-109">In the Master plan field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="e3812-110">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="e3812-110">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="e3812-111">选择主计划。</span><span class="sxs-lookup"><span data-stu-id="e3812-111">Select MasterPlan.</span></span>  
4. <span data-ttu-id="e3812-112">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="e3812-112">Click OK.</span></span>
    * <span data-ttu-id="e3812-113">这将开始主计划，包括顺序流程。</span><span class="sxs-lookup"><span data-stu-id="e3812-113">This starts Master Planning, including the sequence process.</span></span> <span data-ttu-id="e3812-114">此流程可能需要几分钟的时间。</span><span class="sxs-lookup"><span data-stu-id="e3812-114">This process can take a few minutes.</span></span>  

## <a name="view-planned-orders-for-the-paint-products"></a><span data-ttu-id="e3812-115">查看油漆产品的计划订单</span><span class="sxs-lookup"><span data-stu-id="e3812-115">View planned orders for the paint products</span></span>
1. <span data-ttu-id="e3812-116">转到“主计划”>“主计划”>“计划订单”。</span><span class="sxs-lookup"><span data-stu-id="e3812-116">Go to Master planning > Master planning > Planned orders.</span></span>
2. <span data-ttu-id="e3812-117">展开“物料详细信息”速见表。</span><span class="sxs-lookup"><span data-stu-id="e3812-117">Expand the Item details FactBox.</span></span>
3. <span data-ttu-id="e3812-118">展开“计划详细信息”速见表。</span><span class="sxs-lookup"><span data-stu-id="e3812-118">Expand the Schedule details FactBox.</span></span>
4. <span data-ttu-id="e3812-119">在“计划”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="e3812-119">In the Plan field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="e3812-120">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="e3812-120">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="e3812-121">选择主计划。</span><span class="sxs-lookup"><span data-stu-id="e3812-121">Select MasterPlan.</span></span>  
6. <span data-ttu-id="e3812-122">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="e3812-122">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="e3812-123">使用“快速筛选”来筛选带有值“P300”的“物料编号”字段。</span><span class="sxs-lookup"><span data-stu-id="e3812-123">Use the Quick Filter to filter on the Item number field with a value of 'P300'.</span></span>
    * <span data-ttu-id="e3812-124">解锁以滚动到右侧查看订单日期和交货日期。</span><span class="sxs-lookup"><span data-stu-id="e3812-124">Unlock to scroll to the right to see the order date and delivery date.</span></span> <span data-ttu-id="e3812-125">请注意，这些物料具有“今天”订单日期，计划订单的交货日期没有在颜色和包装尺寸优先级后序列化，如产品名称中所示。</span><span class="sxs-lookup"><span data-stu-id="e3812-125">Notice that these items have an order date of Today and the delivery dates for the planned orders are not sequenced after the priority of color and package size, as shown in the product name.</span></span> <span data-ttu-id="e3812-126">您可以悬停到物料编号上查看产品名称和优先级。</span><span class="sxs-lookup"><span data-stu-id="e3812-126">You can hover over an item number to see the product name and priority.</span></span>  

## <a name="sequence-planned-orders-for-paint"></a><span data-ttu-id="e3812-127">排序油漆产品的计划订单</span><span class="sxs-lookup"><span data-stu-id="e3812-127">Sequence planned orders for paint</span></span>
1. <span data-ttu-id="e3812-128">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="e3812-128">Close the page.</span></span>
2. <span data-ttu-id="e3812-129">转到“主计划”>“主计划”>“序列化计划订单”。</span><span class="sxs-lookup"><span data-stu-id="e3812-129">Go to Master planning > Master planning > Sequenced planned orders.</span></span>
3. <span data-ttu-id="e3812-130">展开“物料详细信息”速见表。</span><span class="sxs-lookup"><span data-stu-id="e3812-130">Expand the Item details FactBox.</span></span>
4. <span data-ttu-id="e3812-131">展开“计划详细信息”速见表。</span><span class="sxs-lookup"><span data-stu-id="e3812-131">Expand the Schedule details FactBox.</span></span>
    * <span data-ttu-id="e3812-132">注意：这里您看到计划订单的开始日期/时间根据 28 计算时段内的颜色和包装尺寸排序。</span><span class="sxs-lookup"><span data-stu-id="e3812-132">Note: Here you see that the Start date/time for the planned orders are sequenced according to color and package size within a bucket period of 28 days.</span></span> <span data-ttu-id="e3812-133">这些期间由字段“市场活动”中的数字定义。</span><span class="sxs-lookup"><span data-stu-id="e3812-133">These periods are defined by a number in the field Campaign.</span></span> <span data-ttu-id="e3812-134">“序列化计划订单”窗体类似于典型的计划订单窗体，生产规划员可以在此确定计划订单。</span><span class="sxs-lookup"><span data-stu-id="e3812-134">The sequenced planned order form acts like the typical planned order form, and the production planner can firm the planned orders here.</span></span>  
5. <span data-ttu-id="e3812-135">标记所有行。</span><span class="sxs-lookup"><span data-stu-id="e3812-135">Mark all rows.</span></span>
6. <span data-ttu-id="e3812-136">单击“接受”。</span><span class="sxs-lookup"><span data-stu-id="e3812-136">Click Accept.</span></span>
    * <span data-ttu-id="e3812-137">这将使用所选的“延期”或“提前”顺序操作更新计划订单。</span><span class="sxs-lookup"><span data-stu-id="e3812-137">This will update the planned orders with the selected sequence action of either Postpone or Advance.</span></span>  

## <a name="verify-the-sequence-of-the-planned-orders"></a><span data-ttu-id="e3812-138">确认计划订单的顺序</span><span class="sxs-lookup"><span data-stu-id="e3812-138">Verify the sequence of the planned orders</span></span>
1. <span data-ttu-id="e3812-139">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="e3812-139">Close the page.</span></span>
2. <span data-ttu-id="e3812-140">转到“主计划”>“主计划”>“计划订单”。</span><span class="sxs-lookup"><span data-stu-id="e3812-140">Go to Master planning > Master planning > Planned orders.</span></span>
3. <span data-ttu-id="e3812-141">展开“物料详细信息”速见表。</span><span class="sxs-lookup"><span data-stu-id="e3812-141">Expand the Item details FactBox.</span></span>
4. <span data-ttu-id="e3812-142">展开“计划详细信息”速见表。</span><span class="sxs-lookup"><span data-stu-id="e3812-142">Expand the Schedule details FactBox.</span></span>
5. <span data-ttu-id="e3812-143">在“计划”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="e3812-143">In the Plan field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="e3812-144">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="e3812-144">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="e3812-145">选择主计划。</span><span class="sxs-lookup"><span data-stu-id="e3812-145">Select MasterPlan.</span></span>  
7. <span data-ttu-id="e3812-146">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="e3812-146">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="e3812-147">使用“快速筛选”来筛选带有值“P300”的“物料编号”字段。</span><span class="sxs-lookup"><span data-stu-id="e3812-147">Use the Quick Filter to filter on the Item number field with a value of 'P300'.</span></span>
    * <span data-ttu-id="e3812-148">请注意，订单现在根据颜色和尺寸的优先级排序，计划订单从最早订单日期和交货日期开始。</span><span class="sxs-lookup"><span data-stu-id="e3812-148">Notice that the orders now are sequenced according to the priority of color and size and the planned orders start at the earliest order date and delivery date.</span></span> <span data-ttu-id="e3812-149">验证“计划详细信息”速见表中的订单日期列或开始日期。</span><span class="sxs-lookup"><span data-stu-id="e3812-149">Validate the Order date column or the Start date in the Schedule details FactBbox.</span></span>  

