---
title: 定义 lean manufacturing 工作单元
description: 工作单元是可用于精益制造流程活动的特定形式的资源组。
author: cvocph
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WrkCtrResourceGroup, InventLocationIdLookup, UnitOfMeasureLookup, DimensionLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cfce85b43a4678bf94a5570f4df047249cf29d1e
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/01/2019
ms.locfileid: "1836280"
---
# <a name="define-lean-manufacturing-work-cells"></a><span data-ttu-id="b9f12-103">定义 lean manufacturing 工作单元</span><span class="sxs-lookup"><span data-stu-id="b9f12-103">Define lean manufacturing work cells</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b9f12-104">工作单元是可用于精益制造流程活动的特定形式的资源组。</span><span class="sxs-lookup"><span data-stu-id="b9f12-104">A work cell is a specific form of resource groups that can be used in lean manufacturing process activities.</span></span> <span data-ttu-id="b9f12-105">工作单元具有输入和输出位置以及基于生产流模型的产能定义。</span><span class="sxs-lookup"><span data-stu-id="b9f12-105">Work cells have input and output locations and a capacity definition based on a production flow model.</span></span> <span data-ttu-id="b9f12-106">若要了解有关精益制造工作单元和产能计算的基本概念，请参阅 Lean manufacturing 白皮书。</span><span class="sxs-lookup"><span data-stu-id="b9f12-106">To learn more about the basic concepts of lean manufacturing work cells and capacity calculations, see the white papers on Lean manufacturing.</span></span> <span data-ttu-id="b9f12-107">用于创建此过程的演示数据公司是 USMF。</span><span class="sxs-lookup"><span data-stu-id="b9f12-107">The demo data company used to create this procedure is USMF</span></span>


## <a name="create-a-work-cell"></a><span data-ttu-id="b9f12-108">创建工作单元。</span><span class="sxs-lookup"><span data-stu-id="b9f12-108">Create a work cell.</span></span> 
1. <span data-ttu-id="b9f12-109">转到“组织管理”>“资源”>“资源组”。</span><span class="sxs-lookup"><span data-stu-id="b9f12-109">Go to Organization administration > Resources > Resource groups.</span></span>
2. <span data-ttu-id="b9f12-110">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="b9f12-110">Click New.</span></span>
3. <span data-ttu-id="b9f12-111">在“资源组”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="b9f12-111">In the Resource group field, type a value.</span></span>
    * <span data-ttu-id="b9f12-112">工作单元 ID 通常是一个系统代码，且必须为该法人所独有。</span><span class="sxs-lookup"><span data-stu-id="b9f12-112">The work cell ID is typically a systematic code and has to be unique for the legal entity.</span></span>  
4. <span data-ttu-id="b9f12-113">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="b9f12-113">In the Description field, type a value.</span></span>
    * <span data-ttu-id="b9f12-114">描述包含工作单元的名称或标题。</span><span class="sxs-lookup"><span data-stu-id="b9f12-114">The description contains the name or title of the work cell.</span></span>  
5. <span data-ttu-id="b9f12-115">在“位置”字段中，单击下拉按钮打开查询。</span><span class="sxs-lookup"><span data-stu-id="b9f12-115">In the Site field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="b9f12-116">工作单元位于一个特定站点。</span><span class="sxs-lookup"><span data-stu-id="b9f12-116">A work cell is located at one specific site.</span></span> <span data-ttu-id="b9f12-117">输入与输出仓库以及工作单元的位置均位于此站点。</span><span class="sxs-lookup"><span data-stu-id="b9f12-117">Both input and output warehouse and location have to be located on this site.</span></span>  
6. <span data-ttu-id="b9f12-118">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="b9f12-118">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="b9f12-119">在“生产单位”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="b9f12-119">In the Production unit field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="b9f12-120">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="b9f12-120">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="b9f12-121">选择该工作单元所隶属的生产单位。</span><span class="sxs-lookup"><span data-stu-id="b9f12-121">Select a production unit that this work cell belongs to.</span></span>  
9. <span data-ttu-id="b9f12-122">选择“工作单元”复选框。</span><span class="sxs-lookup"><span data-stu-id="b9f12-122">Select the Work cell check box.</span></span>
    * <span data-ttu-id="b9f12-123">使用一个资源组作为精益工作单元，选择“工作单元”复选框。</span><span class="sxs-lookup"><span data-stu-id="b9f12-123">To use a resource group as a lean work cell, the Work cell check box has to be selected.</span></span>  <span data-ttu-id="b9f12-124">请注意，资源组创建后，此属性将无法更改。</span><span class="sxs-lookup"><span data-stu-id="b9f12-124">Note that this property cannot be changed after resource group is created.</span></span>  
10. <span data-ttu-id="b9f12-125">在“输入仓库”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="b9f12-125">In the Input warehouse field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="b9f12-126">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="b9f12-126">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="b9f12-127">为核算和管理物料，车间内的物料通常会分配给一个特定的虚拟仓库。</span><span class="sxs-lookup"><span data-stu-id="b9f12-127">For accounting and material control, the material staged on the shop floor is typically allocated to a specific virtual warehouse.</span></span> <span data-ttu-id="b9f12-128">但是，如果希望使用仓库作业补充某位置的物料，则该位置必须属于可接收原材料的仓库。</span><span class="sxs-lookup"><span data-stu-id="b9f12-128">However, if you want to replenish the locations using warehouse work, they must be part of the receptive raw material warehouse.</span></span>  
12. <span data-ttu-id="b9f12-129">在“输入位置”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="b9f12-129">In the Input location field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="b9f12-130">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="b9f12-130">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="b9f12-131">请注意，流程活动（或特定产品或产品变型）的输入位置一般可以通过定义给该流程活动送料的装货活动而重写。</span><span class="sxs-lookup"><span data-stu-id="b9f12-131">Note that for a process activity, the input location can by overwritten in general or for a specific product or product variant by defining picking activities that feed to the process activity.</span></span> <span data-ttu-id="b9f12-132">工作单元的输入位置不受牌照控制。</span><span class="sxs-lookup"><span data-stu-id="b9f12-132">The input locations of a work cell cannot be license plate controlled.</span></span>  
14. <span data-ttu-id="b9f12-133">在“输出仓库”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="b9f12-133">In the Output warehouse field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="b9f12-134">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="b9f12-134">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="b9f12-135">在多个活动生产流或生产行中，这通常是生产流后产品一般会转移到的下一个工作单元、销售点或中转仓库的输入仓库。</span><span class="sxs-lookup"><span data-stu-id="b9f12-135">In multiple activity production flows or production lines, this is often the input warehouse of the next work cell or the sales or transit warehouse where a product is typically transferred to after the production process.</span></span> <span data-ttu-id="b9f12-136">请记住，模拟精益制造流程时，通常不需要运输，因为这是报告形式的运输。</span><span class="sxs-lookup"><span data-stu-id="b9f12-136">Remember when modeling lean manufacturing processes, transport is usually waste, as is reporting transport.</span></span>  
16. <span data-ttu-id="b9f12-137">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="b9f12-137">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="b9f12-138">在“输出位置”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="b9f12-138">In the Output location field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="b9f12-139">在具有多个流程活动的生产流中，这通常是下一个工作单元的输入位置。</span><span class="sxs-lookup"><span data-stu-id="b9f12-139">In a production flow with multiple process activites this if often the input location of the next work cell.</span></span>  
18. <span data-ttu-id="b9f12-140">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="b9f12-140">In the list, find and select the desired record.</span></span>
19. <span data-ttu-id="b9f12-141">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="b9f12-141">In the list, click the link in the selected row.</span></span>
20. <span data-ttu-id="b9f12-142">展开或折叠“运营”部分。</span><span class="sxs-lookup"><span data-stu-id="b9f12-142">Expand or collapse the Operation section.</span></span>
    * <span data-ttu-id="b9f12-143">要计算精益看板作业的成本并处理精益看板作业，必须提供“运行时间”类别。</span><span class="sxs-lookup"><span data-stu-id="b9f12-143">A Run time category must be provided to enable cost calculation and processing of lean kanban jobs.</span></span>  
21. <span data-ttu-id="b9f12-144">在“运行时间类别”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="b9f12-144">In the Run time category field, click the drop-down button to open the lookup.</span></span>
22. <span data-ttu-id="b9f12-145">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="b9f12-145">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="b9f12-146">运行时间的成本类别用于标准成本计算和倒冲成本计算。</span><span class="sxs-lookup"><span data-stu-id="b9f12-146">The run time cost category is used in standard cost calculation and on backflush costing.</span></span>  
23. <span data-ttu-id="b9f12-147">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="b9f12-147">In the list, click the link in the selected row.</span></span>
24. <span data-ttu-id="b9f12-148">展开或折叠“日历”部分。</span><span class="sxs-lookup"><span data-stu-id="b9f12-148">Expand or collapse the Calendars section.</span></span>
25. <span data-ttu-id="b9f12-149">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="b9f12-149">Click Add.</span></span>
26. <span data-ttu-id="b9f12-150">在“日历”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="b9f12-150">In the Calendar field, click the drop-down button to open the lookup.</span></span>
27. <span data-ttu-id="b9f12-151">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="b9f12-151">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="b9f12-152">给定站点的工作单元通常使用相同的工作时间日历。</span><span class="sxs-lookup"><span data-stu-id="b9f12-152">Typically work cells of a given site use the same working time calendar.</span></span> <span data-ttu-id="b9f12-153">如果工作单元具有单独的工作时间，则可能需要为此工作单元创建特定的工作时间日历。</span><span class="sxs-lookup"><span data-stu-id="b9f12-153">If work cells can have individual working times, you might need to create a specific working time calendar for the work cell.</span></span> <span data-ttu-id="b9f12-154">请注意，当用于精益工作单元时，此日历应该具有标准工作时间，因为产能定义通常与工作日的标准工作时间相关。</span><span class="sxs-lookup"><span data-stu-id="b9f12-154">Note that the calendar should have a standard working time defined when used for a lean work cell, because the capacity definition is usually related to the standard working time of a work day.</span></span>  
28. <span data-ttu-id="b9f12-155">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="b9f12-155">In the list, click the link in the selected row.</span></span>
29. <span data-ttu-id="b9f12-156">展开或折叠“工作单元产能”部分。</span><span class="sxs-lookup"><span data-stu-id="b9f12-156">Expand or collapse the Work cell capacity section.</span></span>
30. <span data-ttu-id="b9f12-157">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="b9f12-157">Click Add.</span></span>
31. <span data-ttu-id="b9f12-158">在“生产流模型”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="b9f12-158">In the Production flow model field, click the drop-down button to open the lookup.</span></span>
32. <span data-ttu-id="b9f12-159">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="b9f12-159">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="b9f12-160">该过程需要将生产流模型类型设为吞吐量类型，以显示吞吐量产能的定义。</span><span class="sxs-lookup"><span data-stu-id="b9f12-160">This procedures requires production flow model type Throughput, to show the definition of throughput capacity.</span></span>  
33. <span data-ttu-id="b9f12-161">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="b9f12-161">In the list, click the link in the selected row.</span></span>
34. <span data-ttu-id="b9f12-162">在“产能期间”字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="b9f12-162">In the Capacity period field, select an option.</span></span>
    * <span data-ttu-id="b9f12-163">选项包括：标准工作日 - 以工作单元工作时间日历标准工作日的长度表示产能。</span><span class="sxs-lookup"><span data-stu-id="b9f12-163">The options include:   Standard workday - The capacity is expressed by the length of the standard workday of the working time calendar for the work cell.</span></span> <span data-ttu-id="b9f12-164">该日历决定了每天的实际工作时间，同时据此计算有效可用产能。</span><span class="sxs-lookup"><span data-stu-id="b9f12-164">For each day, the actual working time is determined from the calendar and the effective available capacity is calculated based on that.</span></span>   <span data-ttu-id="b9f12-165">周 - 允许每周产能。</span><span class="sxs-lookup"><span data-stu-id="b9f12-165">Week - Allows a weekly capacity.</span></span> <span data-ttu-id="b9f12-166">未根据实际工作时间进行调整。</span><span class="sxs-lookup"><span data-stu-id="b9f12-166">There is no adjustment done by the actual working time.</span></span>   <span data-ttu-id="b9f12-167">月 - 允许每月产能。</span><span class="sxs-lookup"><span data-stu-id="b9f12-167">Month - Allows a monthly capacity.</span></span> <span data-ttu-id="b9f12-168">未根据实际产能进行调整。</span><span class="sxs-lookup"><span data-stu-id="b9f12-168">There is no adjustment done by the actual capacity.</span></span>   <span data-ttu-id="b9f12-169">标准工作日通常用于每日期间，周产能用于每周产能期间。</span><span class="sxs-lookup"><span data-stu-id="b9f12-169">Typically, the standard workday is used for daily periods and the weekly capacity is used for weekly capacity periods.</span></span>  
35. <span data-ttu-id="b9f12-170">在“平均吞吐量”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="b9f12-170">In the Average throughput quantity field, enter a number.</span></span>
    * <span data-ttu-id="b9f12-171">请注意，精益操作绝不可设置为理想环境下的最大可能产能。</span><span class="sxs-lookup"><span data-stu-id="b9f12-171">Note that a lean operation is never set up for the maximum possible capacity in an ideal environment.</span></span> <span data-ttu-id="b9f12-172">产能应始终根据一般情景下的操作运行进行定义。</span><span class="sxs-lookup"><span data-stu-id="b9f12-172">Instead the capacity should always be defined for operations running under typical circumstances.</span></span>  
36. <span data-ttu-id="b9f12-173">在“单位”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="b9f12-173">In the Unit field, click the drop-down button to open the lookup.</span></span>
37. <span data-ttu-id="b9f12-174">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="b9f12-174">In the list, click the link in the selected row.</span></span>
38. <span data-ttu-id="b9f12-175">ResolveChanges 单位。</span><span class="sxs-lookup"><span data-stu-id="b9f12-175">ResolveChanges the Unit.</span></span>

## <a name="add-a-financial-dimension"></a><span data-ttu-id="b9f12-176">添加财务维度</span><span class="sxs-lookup"><span data-stu-id="b9f12-176">Add a financial dimension</span></span>
1. <span data-ttu-id="b9f12-177">展开或折叠“财务维度”部分。</span><span class="sxs-lookup"><span data-stu-id="b9f12-177">Expand or collapse the Financial dimensions section.</span></span>
    * <span data-ttu-id="b9f12-178">请注意，根据生产流定义的财务维度会覆盖给定工作单元的财务维度。</span><span class="sxs-lookup"><span data-stu-id="b9f12-178">Note that financial dimensions defined on the production flow override the financial dimension of a given work cell.</span></span>    <span data-ttu-id="b9f12-179">可以选择的财务维度取决于您系统的财务维度配置。</span><span class="sxs-lookup"><span data-stu-id="b9f12-179">The financial dimensions that can be selected depend on the configuration of the financial dimensions of your system.</span></span> <span data-ttu-id="b9f12-180">以下步骤与 USMF 公司的演示数据设定相对应。</span><span class="sxs-lookup"><span data-stu-id="b9f12-180">The following steps correspond to the Demo data set in company USMF.</span></span> <span data-ttu-id="b9f12-181">如果使用不同数据，这些步骤可能不适用。</span><span class="sxs-lookup"><span data-stu-id="b9f12-181">When using different data, the steps might not be applicable.</span></span>  
2. <span data-ttu-id="b9f12-182">在“成本中心”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="b9f12-182">In the CostCenter field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="b9f12-183">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="b9f12-183">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="b9f12-184">需要在精益工作单元中选择的维度取决于特定法人会计模型中实施的财务维度。</span><span class="sxs-lookup"><span data-stu-id="b9f12-184">The dimensions that need to be selected on lean work cells depend on the implementation of financial dimensions in the accounting model for a specific legal entity.</span></span>  
4. <span data-ttu-id="b9f12-185">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="b9f12-185">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="b9f12-186">在“物料组”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="b9f12-186">In the ItemGroup field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="b9f12-187">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="b9f12-187">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="b9f12-188">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="b9f12-188">In the list, click the link in the selected row.</span></span>

## <a name="save"></a><span data-ttu-id="b9f12-189">保存</span><span class="sxs-lookup"><span data-stu-id="b9f12-189">Save</span></span>
1. <span data-ttu-id="b9f12-190">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="b9f12-190">Click Save.</span></span>

