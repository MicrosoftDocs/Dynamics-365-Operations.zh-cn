--- 
title: "创建基准预测"
description: "生产规划员可通过使用时间序列预测模型或复制历史需求来创建基线预测。"
author: YuyuScheller
manager: AnnBe
ms.date: 111/02/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: bd3cf1118d848fe4f95ec92bee3f5d1abe3d3a7c
ms.contentlocale: zh-cn
ms.lasthandoff: 05/08/2018

---
# <a name="create-a-baseline-forecast"></a><span data-ttu-id="c0b42-103">创建基准预测</span><span class="sxs-lookup"><span data-stu-id="c0b42-103">Create a baseline forecast</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c0b42-104">生产规划员可通过使用时间序列预测模型或复制历史需求来创建基线预测。</span><span class="sxs-lookup"><span data-stu-id="c0b42-104">A production planner can create a baseline forecast either by using time series forecast models or by copying the historical demand.</span></span> <span data-ttu-id="c0b42-105">此过程显示如何复制历史需求以使用一个物料分配参数来创建所有产品的基线预测。</span><span class="sxs-lookup"><span data-stu-id="c0b42-105">This procedure shows how to copy the historical demand to create a baseline forecast for all products using one item allocation key.</span></span> 


## <a name="set-up-an-item-allocation-key"></a><span data-ttu-id="c0b42-106">设置物料分配参数</span><span class="sxs-lookup"><span data-stu-id="c0b42-106">Set up an item allocation key</span></span>
1. <span data-ttu-id="c0b42-107">转到“主计划”>“设置”>“内部公司计划组”。</span><span class="sxs-lookup"><span data-stu-id="c0b42-107">Go to Master planning > Setup > Intercompany planning groups.</span></span>
2. <span data-ttu-id="c0b42-108">使用“快速筛选器”以查找记录。</span><span class="sxs-lookup"><span data-stu-id="c0b42-108">Use the Quick Filter to find records.</span></span> <span data-ttu-id="c0b42-109">例如，使用值“10”在“名称”字段中进行筛选。</span><span class="sxs-lookup"><span data-stu-id="c0b42-109">For example, filter on the Name field with a value of '10'.</span></span>
    * <span data-ttu-id="c0b42-110">对法人运行需求预测。</span><span class="sxs-lookup"><span data-stu-id="c0b42-110">Demand forecasting runs across legal entities.</span></span> <span data-ttu-id="c0b42-111">因此您需要设置为其生成内部公司计划组预测的所有公司。</span><span class="sxs-lookup"><span data-stu-id="c0b42-111">That's why you need to set up all the companies for which you want to generate forecasts in one intercompany planning group.</span></span>  
3. <span data-ttu-id="c0b42-112">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="c0b42-112">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="c0b42-113">单击“物料分配参数”。</span><span class="sxs-lookup"><span data-stu-id="c0b42-113">Click Item allocation keys.</span></span>
    * <span data-ttu-id="c0b42-114">选择您想要创建预测的所有物料分配参数。</span><span class="sxs-lookup"><span data-stu-id="c0b42-114">Select all the item allocation keys for which you want to create forecasts.</span></span>  
5. <span data-ttu-id="c0b42-115">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="c0b42-115">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="c0b42-116">选择 D_Aloc 物料分配参数。</span><span class="sxs-lookup"><span data-stu-id="c0b42-116">Select D_Aloc item allocation key.</span></span>  
6. <span data-ttu-id="c0b42-117">单击 >。</span><span class="sxs-lookup"><span data-stu-id="c0b42-117">Click >.</span></span>
7. <span data-ttu-id="c0b42-118">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="c0b42-118">Close the page.</span></span>
8. <span data-ttu-id="c0b42-119">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="c0b42-119">Close the page.</span></span>

## <a name="set-up-the-demand-forecasting-parameters"></a><span data-ttu-id="c0b42-120">设置需求预测参数</span><span class="sxs-lookup"><span data-stu-id="c0b42-120">Set up the demand forecasting parameters</span></span>
1. <span data-ttu-id="c0b42-121">转到“主计划”>“设置”>“需求预测”>“需求预测参数”。</span><span class="sxs-lookup"><span data-stu-id="c0b42-121">Go to Master planning > Setup > Demand forecasting > Demand forecasting parameters.</span></span>
2. <span data-ttu-id="c0b42-122">展开“预测算法参数”部分。</span><span class="sxs-lookup"><span data-stu-id="c0b42-122">Expand the Forecast algorithm parameters section.</span></span>
3. <span data-ttu-id="c0b42-123">在“预测生成策略”字段中，选择“复制历史需求”。</span><span class="sxs-lookup"><span data-stu-id="c0b42-123">In the Forecast generation strategy field, select 'Copy over historical demand'.</span></span>
4. <span data-ttu-id="c0b42-124">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="c0b42-124">Click Save.</span></span>

## <a name="create-a-baseline-forecast"></a><span data-ttu-id="c0b42-125">创建基准预测</span><span class="sxs-lookup"><span data-stu-id="c0b42-125">Create a baseline forecast</span></span>
1. <span data-ttu-id="c0b42-126">转到“主计划”>“预测”>“需求预测”>“生成统计基线预测”。</span><span class="sxs-lookup"><span data-stu-id="c0b42-126">Go to Master planning > Forecasting > Demand forecasting > Generate statistical baseline forecast.</span></span>
2. <span data-ttu-id="c0b42-127">在“开始日期”字段中输入日期。</span><span class="sxs-lookup"><span data-stu-id="c0b42-127">In the From date field, enter a date.</span></span>
    * <span data-ttu-id="c0b42-128">如果您有从 2015 年 1 月 1 日开始的销售订单，请输入此日期。</span><span class="sxs-lookup"><span data-stu-id="c0b42-128">If you have sales orders starting from January 1, 2015, enter this date.</span></span> <span data-ttu-id="c0b42-129">如果没有，则输入您销售订单的最早日期。</span><span class="sxs-lookup"><span data-stu-id="c0b42-129">If you don't, enter the earliest date of your sales orders.</span></span>  
3. <span data-ttu-id="c0b42-130">在“结束日期”字段中输入日期。</span><span class="sxs-lookup"><span data-stu-id="c0b42-130">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="c0b42-131">输入您的销售订单最后日期，例如 '2015-03-31'。</span><span class="sxs-lookup"><span data-stu-id="c0b42-131">Enter the last date of your sales orders, for example '2015-03-31'.</span></span>  
4. <span data-ttu-id="c0b42-132">在“开始日期”字段中输入日期。</span><span class="sxs-lookup"><span data-stu-id="c0b42-132">In the From date field, enter a date.</span></span>
    * <span data-ttu-id="c0b42-133">输入 '2015-04-01'。</span><span class="sxs-lookup"><span data-stu-id="c0b42-133">Enter '2015-04-01'.</span></span> <span data-ttu-id="c0b42-134">此日期将自动计算，作为下一预测时段的开始日期。</span><span class="sxs-lookup"><span data-stu-id="c0b42-134">This date will be automatically calculated as the start date of the next forecasting bucket.</span></span>  
5. <span data-ttu-id="c0b42-135">扩展“要包括的记录”部分。</span><span class="sxs-lookup"><span data-stu-id="c0b42-135">Expand the Records to include section.</span></span>
6. <span data-ttu-id="c0b42-136">单击“筛选器”。</span><span class="sxs-lookup"><span data-stu-id="c0b42-136">Click Filter.</span></span>
7. <span data-ttu-id="c0b42-137">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="c0b42-137">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="c0b42-138">标记字段=内部公司计划组的行。</span><span class="sxs-lookup"><span data-stu-id="c0b42-138">Mark the row where Field = Intercompany planning group.</span></span>  
8. <span data-ttu-id="c0b42-139">在“标准”字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="c0b42-139">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="c0b42-140">键入内部公司计划组，例如您在第一个任务所使用的 10。</span><span class="sxs-lookup"><span data-stu-id="c0b42-140">Type the intercompany planning group, for example, 10, that you used in the first task.</span></span>  
9. <span data-ttu-id="c0b42-141">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="c0b42-141">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="c0b42-142">选择字段=物料分配参数的行。</span><span class="sxs-lookup"><span data-stu-id="c0b42-142">Select the row where Field = Item allocation key.</span></span>  
10. <span data-ttu-id="c0b42-143">在“标准”字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="c0b42-143">In the Criteria field, type a value.</span></span>
11. <span data-ttu-id="c0b42-144">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="c0b42-144">Click OK.</span></span>
12. <span data-ttu-id="c0b42-145">展开“高级参数”部分。</span><span class="sxs-lookup"><span data-stu-id="c0b42-145">Expand the Advanced parameters section.</span></span>
13. <span data-ttu-id="c0b42-146">在“预测时段”字段中，选择“月份”。</span><span class="sxs-lookup"><span data-stu-id="c0b42-146">In the Forecast bucket field, select 'Month'.</span></span>
14. <span data-ttu-id="c0b42-147">在“预测区间”字段中，输入“3”。</span><span class="sxs-lookup"><span data-stu-id="c0b42-147">In the Forecast horizon field, enter '3'.</span></span>
15. <span data-ttu-id="c0b42-148">输入“锁定时限”字段中，输入“1”。</span><span class="sxs-lookup"><span data-stu-id="c0b42-148">In the Freeze time fence field, enter '1'.</span></span>
16. <span data-ttu-id="c0b42-149">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="c0b42-149">Click OK.</span></span>

## <a name="visualize-the-demand-forecast"></a><span data-ttu-id="c0b42-150">使需求预测可视化</span><span class="sxs-lookup"><span data-stu-id="c0b42-150">Visualize the demand forecast</span></span>
1. <span data-ttu-id="c0b42-151">转到“主计划”>“预测”>“需求预测”>“调整后的需求预测”。</span><span class="sxs-lookup"><span data-stu-id="c0b42-151">Go to Master planning > Forecasting > Demand forecasting > Adjusted demand forecast.</span></span>
2. <span data-ttu-id="c0b42-152">在聚合视图表中，选择位于第 1 行、第 2 列的单元格。</span><span class="sxs-lookup"><span data-stu-id="c0b42-152">In the aggregated view table, select the cell in row 1, column 2.</span></span> <span data-ttu-id="c0b42-153">这是您为其创建预测的第二个月。</span><span class="sxs-lookup"><span data-stu-id="c0b42-153">This is the second month for which you have created forecast.</span></span>
3. <span data-ttu-id="c0b42-154">设置数量单元格 (QtyCell) 为“400”。</span><span class="sxs-lookup"><span data-stu-id="c0b42-154">Set QtyCell to '400'.</span></span>
    * <span data-ttu-id="c0b42-155">在单元格中，输入不同于预测值的数字，例如 400。</span><span class="sxs-lookup"><span data-stu-id="c0b42-155">In the cell, enter a different number than the one that was forecasted, for example, 400.</span></span>  
4. <span data-ttu-id="c0b42-156">您已手动调整预测。</span><span class="sxs-lookup"><span data-stu-id="c0b42-156">You have made a manual adjustment to the forecast.</span></span> <span data-ttu-id="c0b42-157">请注意在下一步的图形指示。</span><span class="sxs-lookup"><span data-stu-id="c0b42-157">Notice the graphical indication in the next step.</span></span>
5. <span data-ttu-id="c0b42-158">单击“预测行详细信息”。</span><span class="sxs-lookup"><span data-stu-id="c0b42-158">Click Forecast line details.</span></span>
    * <span data-ttu-id="c0b42-159">在此页面中，您可以查看准确值、历史需求和预测。</span><span class="sxs-lookup"><span data-stu-id="c0b42-159">On this page, you can see the accuracy values, historical demand, and forecast.</span></span> <span data-ttu-id="c0b42-160">您还可以对预测进行更改。</span><span class="sxs-lookup"><span data-stu-id="c0b42-160">You can make changes to the forecast as well.</span></span>  


