---
title: 创建 lean manufacturing 的流程活动
description: 创建 lean manufacturing 的流程活动。
author: cvocph
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityWizard, LeanWorkCellLookup, InventLocationIdLookup, PlanActivityDetails, KanbanJobPickingListPart
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3cb096eb25fa449b521c370bcb1677e38e399658
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/10/2020
ms.locfileid: "3983389"
---
# <a name="create-process-activities-for-lean-manufacturing"></a><span data-ttu-id="766a6-103">创建 lean manufacturing 的流程活动</span><span class="sxs-lookup"><span data-stu-id="766a6-103">Create process activities for lean manufacturing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="766a6-104">创建 lean manufacturing 的流程活动。</span><span class="sxs-lookup"><span data-stu-id="766a6-104">Create a process activity for lean manufacturing.</span></span> 

<span data-ttu-id="766a6-105">先决条件：</span><span class="sxs-lookup"><span data-stu-id="766a6-105">Prerequisites:</span></span> 

1. <span data-ttu-id="766a6-106">必须创建非活动的生产流和版本。</span><span class="sxs-lookup"><span data-stu-id="766a6-106">A production flow and version that is not active must be created.</span></span>

2. <span data-ttu-id="766a6-107">必须创建工作单元。</span><span class="sxs-lookup"><span data-stu-id="766a6-107">A work cell must be created.</span></span>


## <a name="find-the-production-flow-version"></a><span data-ttu-id="766a6-108">找到生产流版本</span><span class="sxs-lookup"><span data-stu-id="766a6-108">Find the production flow version</span></span>
1. <span data-ttu-id="766a6-109">转到“生产控制”>“设置”>“精益生产流程”>“生产流程”。</span><span class="sxs-lookup"><span data-stu-id="766a6-109">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="766a6-110">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="766a6-110">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="766a6-111">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="766a6-111">In the list, click the link in the selected row.</span></span>

## <a name="create-a-new-activity"></a><span data-ttu-id="766a6-112">创建新的活动</span><span class="sxs-lookup"><span data-stu-id="766a6-112">Create a new activity</span></span>
1. <span data-ttu-id="766a6-113">单击“活动”。</span><span class="sxs-lookup"><span data-stu-id="766a6-113">Click Activities.</span></span>
    * <span data-ttu-id="766a6-114">确保所选生产流程具有草稿版本，并选中该版本。</span><span class="sxs-lookup"><span data-stu-id="766a6-114">Ensure that the selected production flow has a version in draft and select that version.</span></span>  
2. <span data-ttu-id="766a6-115">单击“创建新的计划活动”。</span><span class="sxs-lookup"><span data-stu-id="766a6-115">Click Create new plan activity.</span></span>
3. <span data-ttu-id="766a6-116">单击“下一步”。</span><span class="sxs-lookup"><span data-stu-id="766a6-116">Click Next.</span></span>
4. <span data-ttu-id="766a6-117">在“名称”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="766a6-117">In the Name field, type a value.</span></span>
5. <span data-ttu-id="766a6-118">在“名称”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="766a6-118">In the Name field, type a value.</span></span>
    * <span data-ttu-id="766a6-119">请注意，特定生产流的所有版本的名称是唯一的。</span><span class="sxs-lookup"><span data-stu-id="766a6-119">Note that the name must be unique for a given production flow for all versions.</span></span>  
6. <span data-ttu-id="766a6-120">在“流程数量”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="766a6-120">In the Process quantity field, enter a number.</span></span>
    * <span data-ttu-id="766a6-121">请注意，无论将处理的工作数量是多少，此为每一工作计算人工成本的最小数量。</span><span class="sxs-lookup"><span data-stu-id="766a6-121">Note that no matter what job quantity will be processed, this is the minimum quantity per job to calculate the labor cost.</span></span> <span data-ttu-id="766a6-122">如果工作数量与此数量有偏差，将会创建人工成本差异。</span><span class="sxs-lookup"><span data-stu-id="766a6-122">If job quantities deviate from this quantity, labor cost variance will be created.</span></span>  
7. <span data-ttu-id="766a6-123">单击“下一步”。</span><span class="sxs-lookup"><span data-stu-id="766a6-123">Click Next.</span></span>

## <a name="select-the-work-cell"></a><span data-ttu-id="766a6-124">选择工作单元</span><span class="sxs-lookup"><span data-stu-id="766a6-124">Select the work cell</span></span>
1. <span data-ttu-id="766a6-125">在“工作单元”字段中，单击下拉按钮打开查找。</span><span class="sxs-lookup"><span data-stu-id="766a6-125">In the Work cell field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="766a6-126">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="766a6-126">In the list, click the link in the selected row.</span></span>

## <a name="define-the-inventory-updates"></a><span data-ttu-id="766a6-127">定义库存更新</span><span class="sxs-lookup"><span data-stu-id="766a6-127">Define the inventory updates</span></span>
1. <span data-ttu-id="766a6-128">选择或取消选择“更新现有接收量”复选框。</span><span class="sxs-lookup"><span data-stu-id="766a6-128">Select or clear the Update on hand receipt check box.</span></span>
    * <span data-ttu-id="766a6-129">如果“现有更新=无”，您可定义活动，以接收半成品（活动未达到下一物料清单水平）。</span><span class="sxs-lookup"><span data-stu-id="766a6-129">If Update On hand = No, you can define the activity to receive a semi-finished product (the activity does not reach the next BOM level).</span></span>    <span data-ttu-id="766a6-130">您还可以选择消耗量半成品。</span><span class="sxs-lookup"><span data-stu-id="766a6-130">You can also select to consume semi-finished products.</span></span>  

## <a name="define-the-picking-activities"></a><span data-ttu-id="766a6-131">定义领料活动</span><span class="sxs-lookup"><span data-stu-id="766a6-131">Define the picking activities</span></span>
1. <span data-ttu-id="766a6-132">单击“下一步”。</span><span class="sxs-lookup"><span data-stu-id="766a6-132">Click Next.</span></span>
2. <span data-ttu-id="766a6-133">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="766a6-133">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="766a6-134">为所选工作单元的输入库位创建默认领料活动。</span><span class="sxs-lookup"><span data-stu-id="766a6-134">A default picking activity is created for the input location of the selected work cell.</span></span>  
3. <span data-ttu-id="766a6-135">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="766a6-135">Click Add.</span></span>
    * <span data-ttu-id="766a6-136">您可以为不暂存于工作单元输入库位的特定产品创建额外的领料活动。</span><span class="sxs-lookup"><span data-stu-id="766a6-136">You can create additional picking activities for specific products, that are not staged at the work cell input activity.</span></span>  
4. <span data-ttu-id="766a6-137">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="766a6-137">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="766a6-138">在“项目编号”字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="766a6-138">In the Item number field, type a value.</span></span>
6. <span data-ttu-id="766a6-139">在“仓库”字段，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="766a6-139">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="766a6-140">根据此定义，活动消耗的所有物料领自默认输入仓库和库位，除非物料在第二各领料活动中有定义。</span><span class="sxs-lookup"><span data-stu-id="766a6-140">With this definition, all materials consumed in the activity are picked from the default input warehouse and location except the item that is defined in the second picking activity.</span></span> <span data-ttu-id="766a6-141">此物料将从不同的仓库和库位领取。</span><span class="sxs-lookup"><span data-stu-id="766a6-141">This item will be picked from a different warehouse and location.</span></span>  
7. <span data-ttu-id="766a6-142">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="766a6-142">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="766a6-143">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="766a6-143">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="766a6-144">选择或取消选择“登记废料”复选框。</span><span class="sxs-lookup"><span data-stu-id="766a6-144">Select or clear the Register scrap check box.</span></span>
10. <span data-ttu-id="766a6-145">单击“下一步”。</span><span class="sxs-lookup"><span data-stu-id="766a6-145">Click Next.</span></span>

## <a name="define-the-activity-times"></a><span data-ttu-id="766a6-146">定义活动时间</span><span class="sxs-lookup"><span data-stu-id="766a6-146">Define the activity times</span></span>
1. <span data-ttu-id="766a6-147">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="766a6-147">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="766a6-148">需要定义运行时间。</span><span class="sxs-lookup"><span data-stu-id="766a6-148">The definition of a Runtime is required.</span></span> <span data-ttu-id="766a6-149">“运行时间”用于计算看板作业的成本和吞吐时间。</span><span class="sxs-lookup"><span data-stu-id="766a6-149">The Runtime is used to calculate costs and the throughput times of the kanban jobs.</span></span> <span data-ttu-id="766a6-150">运行时间不用于计算产能负荷以及消耗量，两者按周期时间计算，周期根据生产流版本任务确定。</span><span class="sxs-lookup"><span data-stu-id="766a6-150">Runtimes are not used to calculate capacity load and consumption, this is calculated by cycle time, derived from the production flow version task.</span></span>  
2. <span data-ttu-id="766a6-151">在“时间”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="766a6-151">In the Time field, enter a number.</span></span>
3. <span data-ttu-id="766a6-152">在“单位”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="766a6-152">In the Unit field, type a value.</span></span>
4. <span data-ttu-id="766a6-153">选择“时间单位”。</span><span class="sxs-lookup"><span data-stu-id="766a6-153">Select the Time unit.</span></span>
5. <span data-ttu-id="766a6-154">在“单位数量”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="766a6-154">In the Per quantity field, enter a number.</span></span>
6. <span data-ttu-id="766a6-155">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="766a6-155">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="766a6-156">排队时间为可选项。</span><span class="sxs-lookup"><span data-stu-id="766a6-156">Queue times are optional.</span></span>  
7. <span data-ttu-id="766a6-157">在“时间”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="766a6-157">In the Time field, enter a number.</span></span>
8. <span data-ttu-id="766a6-158">在“单位”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="766a6-158">In the Unit field, type a value.</span></span>
9. <span data-ttu-id="766a6-159">选择“时间单位”。</span><span class="sxs-lookup"><span data-stu-id="766a6-159">Select the Time unit.</span></span>
10. <span data-ttu-id="766a6-160">在“单位数量”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="766a6-160">In the Per quantity field, enter a number.</span></span>
11. <span data-ttu-id="766a6-161">单击“下一步”。</span><span class="sxs-lookup"><span data-stu-id="766a6-161">Click Next.</span></span>
12. <span data-ttu-id="766a6-162">单击“完成”。</span><span class="sxs-lookup"><span data-stu-id="766a6-162">Click Finish.</span></span>
13. <span data-ttu-id="766a6-163">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="766a6-163">Close the page.</span></span>

