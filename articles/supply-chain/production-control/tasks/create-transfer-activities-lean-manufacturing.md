---
title: 创建 lean manufacturing 的转移活动
description: 创建 lean manufacturing 的转移活动。
author: cvocph
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityWizard, LeanWorkCellLookup, InventLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2411dc51dc1b85499edb30d9a580f396277a5bd9
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828866"
---
# <a name="create-transfer-activities-for-lean-manufacturing"></a><span data-ttu-id="da506-103">创建 lean manufacturing 的转移活动</span><span class="sxs-lookup"><span data-stu-id="da506-103">Create transfer activities for lean manufacturing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="da506-104">创建 lean manufacturing 的转移活动。</span><span class="sxs-lookup"><span data-stu-id="da506-104">Create a transfer activity for lean manufacturing.</span></span> 

<span data-ttu-id="da506-105">先决条件：</span><span class="sxs-lookup"><span data-stu-id="da506-105">Prerequisites:</span></span> 

1. <span data-ttu-id="da506-106">必须创建非活动的生产流和版本。</span><span class="sxs-lookup"><span data-stu-id="da506-106">A production flow and version that is not active must be created.</span></span>

2. <span data-ttu-id="da506-107">必须创建源和目标仓库和库位。</span><span class="sxs-lookup"><span data-stu-id="da506-107">The from and to warehouse and locations must be created.</span></span> <span data-ttu-id="da506-108">（可选）应创建补货或已补货工作单元。</span><span class="sxs-lookup"><span data-stu-id="da506-108">Optionally, the replenishing or the replenished work cell should be created.</span></span>


## <a name="find-the-production-flow-version"></a><span data-ttu-id="da506-109">找到生产流版本</span><span class="sxs-lookup"><span data-stu-id="da506-109">Find the production flow version</span></span>
1. <span data-ttu-id="da506-110">转到“生产控制”>“设置”>“精益生产流程”>“生产流程”。</span><span class="sxs-lookup"><span data-stu-id="da506-110">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="da506-111">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="da506-111">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="da506-112">请注意，生产流必须有状态为草稿的版本。</span><span class="sxs-lookup"><span data-stu-id="da506-112">Note that the production flow must have a version in draft status.</span></span>  
3. <span data-ttu-id="da506-113">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="da506-113">In the list, click the link in the selected row.</span></span>

## <a name="create-a-new-activity"></a><span data-ttu-id="da506-114">创建新的活动</span><span class="sxs-lookup"><span data-stu-id="da506-114">Create a new activity</span></span>
1. <span data-ttu-id="da506-115">单击“活动”。</span><span class="sxs-lookup"><span data-stu-id="da506-115">Click Activities.</span></span>
    * <span data-ttu-id="da506-116">确保所选生产流程具有草稿版本，并选中该版本。</span><span class="sxs-lookup"><span data-stu-id="da506-116">Ensure that the selected production flow has a version in draft and select that version.</span></span>  
2. <span data-ttu-id="da506-117">单击“创建新的计划活动”。</span><span class="sxs-lookup"><span data-stu-id="da506-117">Click Create new plan activity.</span></span>
3. <span data-ttu-id="da506-118">单击“下一步”。</span><span class="sxs-lookup"><span data-stu-id="da506-118">Click Next.</span></span>
4. <span data-ttu-id="da506-119">在“名称”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="da506-119">In the Name field, type a value.</span></span>
5. <span data-ttu-id="da506-120">在“活动类型”字段中，选择“转移”。</span><span class="sxs-lookup"><span data-stu-id="da506-120">In the Activity type field, select 'Transfer'.</span></span>
6. <span data-ttu-id="da506-121">在“流程数量”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="da506-121">In the Process quantity field, enter a number.</span></span>
7. <span data-ttu-id="da506-122">单击“下一步”。</span><span class="sxs-lookup"><span data-stu-id="da506-122">Click Next.</span></span>

## <a name="select-the-work-cells"></a><span data-ttu-id="da506-123">选择“工作单元”</span><span class="sxs-lookup"><span data-stu-id="da506-123">Select the Work cells</span></span>
1. <span data-ttu-id="da506-124">在“补货”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="da506-124">In the Replenishing field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="da506-125">若要将工作单元输出库位作为转移活动的源库位，则选择一个工作单元。</span><span class="sxs-lookup"><span data-stu-id="da506-125">To use the work cell output location as the from location in the transfer activity, select a work cell.</span></span> <span data-ttu-id="da506-126">补货工作单位可进行同样操作，此时设置转移活动的目标库位。</span><span class="sxs-lookup"><span data-stu-id="da506-126">The same can be done with the replenished work cell, which sets the target location of the transfer activity.</span></span>  
2. <span data-ttu-id="da506-127">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="da506-127">In the list, click the link in the selected row.</span></span>

## <a name="define-the-inventory-updates"></a><span data-ttu-id="da506-128">定义库存更新</span><span class="sxs-lookup"><span data-stu-id="da506-128">Define the inventory updates</span></span>
1. <span data-ttu-id="da506-129">在“产品类型”字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="da506-129">In the Product type field, select an option.</span></span>
    * <span data-ttu-id="da506-130">请注意，转移并不改变产品类型。</span><span class="sxs-lookup"><span data-stu-id="da506-130">Note that a transfer does not change the type of product.</span></span> <span data-ttu-id="da506-131">您可以转移成品或半成品（在一个生产流以及可能的一个看板流的两个活动之间转移）。</span><span class="sxs-lookup"><span data-stu-id="da506-131">You can transfer finished products or semi-finished products (transfer between two activities of a production flow and possibly a kanban flow).</span></span>     <span data-ttu-id="da506-132"> 在转移成品时，您可以选择“领取或接收是否产生库存交易记录”。</span><span class="sxs-lookup"><span data-stu-id="da506-132">When transferring finished products, you can select if picking or receiving results in an inventory transaction.</span></span>  

## <a name="define-the-transfer-locations"></a><span data-ttu-id="da506-133">定义转移库位</span><span class="sxs-lookup"><span data-stu-id="da506-133">Define the transfer locations</span></span>
1. <span data-ttu-id="da506-134">单击“下一步”。</span><span class="sxs-lookup"><span data-stu-id="da506-134">Click Next.</span></span>
2. <span data-ttu-id="da506-135">在“仓库”字段，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="da506-135">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="da506-136">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="da506-136">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="da506-137">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="da506-137">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="da506-138">在“地点”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="da506-138">In the Location field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="da506-139">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="da506-139">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="da506-140">在“货运服务提供方”字段中，选择“发货人”。</span><span class="sxs-lookup"><span data-stu-id="da506-140">In the Freighted by field, select 'Shipper'.</span></span>
    * <span data-ttu-id="da506-141">可选项包括：发货人-装运仓库物料的组织、接收人-接收仓库物料的组织、承运人-第三方供应商。</span><span class="sxs-lookup"><span data-stu-id="da506-141">Options include: Shipper - the organization operating the shipping warehouse, Recipient -  the organization operating the receiving warehouse, Carrier - a third party vendor.</span></span> <span data-ttu-id="da506-142">如果运行机构为供应商，转移活动需要转包协议。</span><span class="sxs-lookup"><span data-stu-id="da506-142">If the operating organization is a vendor, the transfer activity requires a subcontracting agreement.</span></span>  
8. <span data-ttu-id="da506-143">单击“下一步”。</span><span class="sxs-lookup"><span data-stu-id="da506-143">Click Next.</span></span>

## <a name="define-the-activity-times"></a><span data-ttu-id="da506-144">定义活动时间</span><span class="sxs-lookup"><span data-stu-id="da506-144">Define the activity times</span></span>
1. <span data-ttu-id="da506-145">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="da506-145">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="da506-146">需要定义运行时间。</span><span class="sxs-lookup"><span data-stu-id="da506-146">The definition of a Runtime is required.</span></span> <span data-ttu-id="da506-147">“运行时间”用于计算看板作业的成本和吞吐时间。</span><span class="sxs-lookup"><span data-stu-id="da506-147">The Runtime is used to calculate cost and the throughput times of the kanban jobs.</span></span> <span data-ttu-id="da506-148">“运行时间”不用于计算产能负荷以及消耗量，两者按周期时间计算，周期根据生产流版本任务确定。</span><span class="sxs-lookup"><span data-stu-id="da506-148">Runtimes are not used to calculate capacity load and consumption, which is calculated by cycle time, derived from the production flow version task.</span></span>  
2. <span data-ttu-id="da506-149">在“时间”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="da506-149">In the Time field, enter a number.</span></span>
3. <span data-ttu-id="da506-150">在“单位”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="da506-150">In the Unit field, type a value.</span></span>
4. <span data-ttu-id="da506-151">选择“时间单位”。</span><span class="sxs-lookup"><span data-stu-id="da506-151">Select the Time unit.</span></span>
5. <span data-ttu-id="da506-152">在“单位数量”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="da506-152">In the Per quantity field, enter a number.</span></span>
6. <span data-ttu-id="da506-153">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="da506-153">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="da506-154">排队时间为可选项。</span><span class="sxs-lookup"><span data-stu-id="da506-154">Queue times are optional.</span></span>  
7. <span data-ttu-id="da506-155">在“时间”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="da506-155">In the Time field, enter a number.</span></span>
8. <span data-ttu-id="da506-156">在“单位”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="da506-156">In the Unit field, type a value.</span></span>
9. <span data-ttu-id="da506-157">选择“时间单位”。</span><span class="sxs-lookup"><span data-stu-id="da506-157">Select the Time unit.</span></span>
10. <span data-ttu-id="da506-158">在“单位数量”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="da506-158">In the Per quantity field, enter a number.</span></span>
11. <span data-ttu-id="da506-159">单击“下一步”。</span><span class="sxs-lookup"><span data-stu-id="da506-159">Click Next.</span></span>
12. <span data-ttu-id="da506-160">单击“完成”。</span><span class="sxs-lookup"><span data-stu-id="da506-160">Click Finish.</span></span>
13. <span data-ttu-id="da506-161">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="da506-161">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]