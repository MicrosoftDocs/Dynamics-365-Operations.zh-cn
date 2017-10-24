--- 
title: "创建 lean manufacturing 的流程活动"
description: "创建 lean manufacturing 的流程活动。"
author: cvocph
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
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: dd77c20b622fd8a14e1cdf77883043699f9a6317
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---
# <a name="create-process-activities-for-lean-manufacturing"></a><span data-ttu-id="d5345-103">创建 lean manufacturing 的流程活动</span><span class="sxs-lookup"><span data-stu-id="d5345-103">Create process activities for lean manufacturing</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d5345-104">创建 lean manufacturing 的流程活动。</span><span class="sxs-lookup"><span data-stu-id="d5345-104">Create a process activity for lean manufacturing.</span></span> 

<span data-ttu-id="d5345-105">先决条件：</span><span class="sxs-lookup"><span data-stu-id="d5345-105">Prerequisites:</span></span> 

1. <span data-ttu-id="d5345-106">必须创建非活动的生产流和版本。</span><span class="sxs-lookup"><span data-stu-id="d5345-106">A production flow and version that is not active must be created.</span></span>

2. <span data-ttu-id="d5345-107">必须创建工作单元。</span><span class="sxs-lookup"><span data-stu-id="d5345-107">A work cell must be created.</span></span>


## <a name="find-the-production-flow-version"></a><span data-ttu-id="d5345-108">找到生产流版本</span><span class="sxs-lookup"><span data-stu-id="d5345-108">Find the production flow version</span></span>
1. <span data-ttu-id="d5345-109">转到“生产控制”>“设置”>“精益生产流程”>“生产流程”。</span><span class="sxs-lookup"><span data-stu-id="d5345-109">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="d5345-110">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="d5345-110">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="d5345-111">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="d5345-111">In the list, click the link in the selected row.</span></span>

## <a name="create-a-new-activity"></a><span data-ttu-id="d5345-112">创建新的活动</span><span class="sxs-lookup"><span data-stu-id="d5345-112">Create a new activity</span></span>
1. <span data-ttu-id="d5345-113">单击“活动”。</span><span class="sxs-lookup"><span data-stu-id="d5345-113">Click Activities.</span></span>
    * <span data-ttu-id="d5345-114">确保所选生产流程具有草稿版本，并选中该版本。</span><span class="sxs-lookup"><span data-stu-id="d5345-114">Ensure that the selected production flow has a version in draft and select that version.</span></span>  
2. <span data-ttu-id="d5345-115">单击“创建新的计划活动”。</span><span class="sxs-lookup"><span data-stu-id="d5345-115">Click Create new plan activity.</span></span>
3. <span data-ttu-id="d5345-116">单击“下一步”。</span><span class="sxs-lookup"><span data-stu-id="d5345-116">Click Next.</span></span>
4. <span data-ttu-id="d5345-117">在“名称”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="d5345-117">In the Name field, type a value.</span></span>
5. <span data-ttu-id="d5345-118">在“名称”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="d5345-118">In the Name field, type a value.</span></span>
    * <span data-ttu-id="d5345-119">请注意，特定生产流的所有版本的名称是唯一的。</span><span class="sxs-lookup"><span data-stu-id="d5345-119">Note that the name must be unique for a given production flow for all versions.</span></span>  
6. <span data-ttu-id="d5345-120">在“流程数量”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="d5345-120">In the Process quantity field, enter a number.</span></span>
    * <span data-ttu-id="d5345-121">请注意，无论将处理的工作数量是多少，此为每一工作计算人工成本的最小数量。</span><span class="sxs-lookup"><span data-stu-id="d5345-121">Note that no matter what job quantity will be processed, this is the minimum quantity per job to calculate the labor cost.</span></span> <span data-ttu-id="d5345-122">如果工作数量与此数量有偏差，将会创建人工成本差异。</span><span class="sxs-lookup"><span data-stu-id="d5345-122">If job quantities deviate from this quantity, labor cost variance will be created.</span></span>  
7. <span data-ttu-id="d5345-123">单击“下一步”。</span><span class="sxs-lookup"><span data-stu-id="d5345-123">Click Next.</span></span>

## <a name="select-the-work-cell"></a><span data-ttu-id="d5345-124">选择工作单元</span><span class="sxs-lookup"><span data-stu-id="d5345-124">Select the work cell</span></span>
1. <span data-ttu-id="d5345-125">在“工作单元”字段中，单击下拉按钮打开查找。</span><span class="sxs-lookup"><span data-stu-id="d5345-125">In the Work cell field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="d5345-126">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="d5345-126">In the list, click the link in the selected row.</span></span>

## <a name="define-the-inventory-updates"></a><span data-ttu-id="d5345-127">定义库存更新</span><span class="sxs-lookup"><span data-stu-id="d5345-127">Define the inventory updates</span></span>
1. <span data-ttu-id="d5345-128">选择或取消选择“更新现有接收量”复选框。</span><span class="sxs-lookup"><span data-stu-id="d5345-128">Select or clear the Update on hand receipt check box.</span></span>
    * <span data-ttu-id="d5345-129">如果“现有更新=无”，您可定义活动，以接收半成品（活动未达到下一物料清单水平）。</span><span class="sxs-lookup"><span data-stu-id="d5345-129">If Update On hand = No, you can define the activity to receive a semi-finished product (the activity does not reach the next BOM level).</span></span>    <span data-ttu-id="d5345-130">您还可以选择消耗量半成品。</span><span class="sxs-lookup"><span data-stu-id="d5345-130">You can also select to consume semi-finished products.</span></span>  

## <a name="define-the-picking-activities"></a><span data-ttu-id="d5345-131">定义领料活动</span><span class="sxs-lookup"><span data-stu-id="d5345-131">Define the picking activities</span></span>
1. <span data-ttu-id="d5345-132">单击“下一步”。</span><span class="sxs-lookup"><span data-stu-id="d5345-132">Click Next.</span></span>
2. <span data-ttu-id="d5345-133">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="d5345-133">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="d5345-134">为所选工作单元的输入库位创建默认领料活动。</span><span class="sxs-lookup"><span data-stu-id="d5345-134">A default picking activity is created for the input location of the selected work cell.</span></span>  
3. <span data-ttu-id="d5345-135">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="d5345-135">Click Add.</span></span>
    * <span data-ttu-id="d5345-136">您可以为不暂存于工作单元输入库位的特定产品创建额外的领料活动。</span><span class="sxs-lookup"><span data-stu-id="d5345-136">You can create additional picking activities for specific products, that are not staged at the work cell input activity.</span></span>  
4. <span data-ttu-id="d5345-137">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="d5345-137">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="d5345-138">在“项目编号”字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="d5345-138">In the Item number field, type a value.</span></span>
6. <span data-ttu-id="d5345-139">在“仓库”字段，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="d5345-139">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="d5345-140">根据此定义，活动消耗的所有物料领自默认输入仓库和库位，除非物料在第二各领料活动中有定义。</span><span class="sxs-lookup"><span data-stu-id="d5345-140">With this definition, all materials consumed in the activity are picked from the default input warehouse and location except the item that is defined in the second picking activity.</span></span> <span data-ttu-id="d5345-141">此物料将从不同的仓库和库位领取。</span><span class="sxs-lookup"><span data-stu-id="d5345-141">This item will be picked from a different warehouse and location.</span></span>  
7. <span data-ttu-id="d5345-142">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="d5345-142">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="d5345-143">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="d5345-143">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="d5345-144">选择或取消选择“登记废料”复选框。</span><span class="sxs-lookup"><span data-stu-id="d5345-144">Select or clear the Register scrap check box.</span></span>
10. <span data-ttu-id="d5345-145">单击“下一步”。</span><span class="sxs-lookup"><span data-stu-id="d5345-145">Click Next.</span></span>

## <a name="define-the-activity-times"></a><span data-ttu-id="d5345-146">定义活动时间</span><span class="sxs-lookup"><span data-stu-id="d5345-146">Define the activity times</span></span>
1. <span data-ttu-id="d5345-147">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="d5345-147">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="d5345-148">需要定义运行时间。</span><span class="sxs-lookup"><span data-stu-id="d5345-148">The definition of a Runtime is required.</span></span> <span data-ttu-id="d5345-149">“运行时间”用于计算看板作业的成本和吞吐时间。</span><span class="sxs-lookup"><span data-stu-id="d5345-149">The Runtime is used to calculate costs and the throughput times of the kanban jobs.</span></span> <span data-ttu-id="d5345-150">运行时间不用于计算产能负荷以及消耗量，两者按周期时间计算，周期根据生产流版本任务确定。</span><span class="sxs-lookup"><span data-stu-id="d5345-150">Runtimes are not used to calculate capacity load and consumption, this is calculated by cycle time, derived from the production flow version task.</span></span>  
2. <span data-ttu-id="d5345-151">在“时间”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="d5345-151">In the Time field, enter a number.</span></span>
3. <span data-ttu-id="d5345-152">在“单位”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="d5345-152">In the Unit field, type a value.</span></span>
4. <span data-ttu-id="d5345-153">选择“时间单位”。</span><span class="sxs-lookup"><span data-stu-id="d5345-153">Select the Time unit.</span></span>
5. <span data-ttu-id="d5345-154">在“单位数量”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="d5345-154">In the Per quantity field, enter a number.</span></span>
6. <span data-ttu-id="d5345-155">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="d5345-155">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="d5345-156">排队时间为可选项。</span><span class="sxs-lookup"><span data-stu-id="d5345-156">Queue times are optional.</span></span>  
7. <span data-ttu-id="d5345-157">在“时间”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="d5345-157">In the Time field, enter a number.</span></span>
8. <span data-ttu-id="d5345-158">在“单位”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="d5345-158">In the Unit field, type a value.</span></span>
9. <span data-ttu-id="d5345-159">选择“时间单位”。</span><span class="sxs-lookup"><span data-stu-id="d5345-159">Select the Time unit.</span></span>
10. <span data-ttu-id="d5345-160">在“单位数量”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="d5345-160">In the Per quantity field, enter a number.</span></span>
11. <span data-ttu-id="d5345-161">单击“下一步”。</span><span class="sxs-lookup"><span data-stu-id="d5345-161">Click Next.</span></span>
12. <span data-ttu-id="d5345-162">单击“完成”。</span><span class="sxs-lookup"><span data-stu-id="d5345-162">Click Finish.</span></span>
13. <span data-ttu-id="d5345-163">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="d5345-163">Close the page.</span></span>


