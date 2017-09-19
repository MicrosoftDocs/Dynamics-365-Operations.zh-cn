--- 
title: "设置最小-最大补货流程"
description: "此过程显示设置使用最小/最大补货战略的新补货流程。"
author: perlynne
manager: AnnBe
ms.date: 06/07/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 02af5d1beb2d4eb6a7162b47c42854725fbdbec2
ms.contentlocale: zh-cn
ms.lasthandoff: 08/29/2017

---
# <a name="set-up-a-min-max-replenishment-process"></a><span data-ttu-id="ef674-103">设置最小-最大补货流程</span><span class="sxs-lookup"><span data-stu-id="ef674-103">Set up a min-max replenishment process</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ef674-104">此过程显示设置使用最小/最大补货战略的新补货流程。</span><span class="sxs-lookup"><span data-stu-id="ef674-104">This procedure shows you how to set up a new replenishment process which uses the minimum/maximum replenishment strategy.</span></span> <span data-ttu-id="ef674-105">在库存低于最低水平时，将创建工作以在此位置补货。</span><span class="sxs-lookup"><span data-stu-id="ef674-105">When inventory falls below the minimum level, work will be created to replenish the location.</span></span> <span data-ttu-id="ef674-106">过程还显示如何使用固定领料位置以允许补货，即使库存低于最低水平，以及如何使用批处理作业使补货流程定期运行。</span><span class="sxs-lookup"><span data-stu-id="ef674-106">The procedure also shows how to use fixed picking locations to allow restocking even if inventory falls below the minimum level, and how to enable the replenishment process to run regularly using a batch job.</span></span> <span data-ttu-id="ef674-107">这些任务通常由仓库管理员完成。</span><span class="sxs-lookup"><span data-stu-id="ef674-107">These tasks would typically be carried out by a warehouse manager.</span></span> <span data-ttu-id="ef674-108">您可以使用注释中的示例值在 USMF 演示数据公司中运行此过程，或可以对您自己的数据运行它。</span><span class="sxs-lookup"><span data-stu-id="ef674-108">You can run this procedure in the USMF demo data company using the example values in the notes, or can run it on your own data.</span></span> <span data-ttu-id="ef674-109">如果您使用自己的数据，请确保您有为仓库管理流程启用的仓库。</span><span class="sxs-lookup"><span data-stu-id="ef674-109">If you’re using your own data, make sure that you have a warehouse that’s enabled for Warehouse management processes.</span></span>


## <a name="create-a-fixed-picking-location"></a><span data-ttu-id="ef674-110">创建固定领料库位</span><span class="sxs-lookup"><span data-stu-id="ef674-110">Create a fixed picking location</span></span>
1. <span data-ttu-id="ef674-111">转到“仓库管理”>“设置”>“仓库”>“固定货位”。</span><span class="sxs-lookup"><span data-stu-id="ef674-111">Go to Warehouse management > Setup > Warehouse > Fixed locations.</span></span>
    * <span data-ttu-id="ef674-112">这是最小-最大补货的可选任务，但是，如果您使用固定领料库位，这允许对存货进行补货，即使低于最低水平，因为系统可以确定哪些物料需要补货，即使没有任何剩余。</span><span class="sxs-lookup"><span data-stu-id="ef674-112">This is an optional task for min-max replenishment, but if you use fixed picking location, this allows stock to be replenished even if it falls below the minimum level, because the system can determine which items need to be replenished, even if there aren't any left.</span></span>  
2. <span data-ttu-id="ef674-113">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="ef674-113">Click New.</span></span>
3. <span data-ttu-id="ef674-114">在“物料编号”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="ef674-114">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="ef674-115">如果您正在使用 USMF，可以选择物料 A0001。</span><span class="sxs-lookup"><span data-stu-id="ef674-115">If you’re using USMF, you can select item A0001.</span></span>  
4. <span data-ttu-id="ef674-116">在“站点”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="ef674-116">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="ef674-117">如果您使用 USMF，您可以选择站点 2。</span><span class="sxs-lookup"><span data-stu-id="ef674-117">If you’re using USMF, you can select site 2.</span></span>  
5. <span data-ttu-id="ef674-118">在“仓库”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="ef674-118">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="ef674-119">如果您使用 USMF，您可以选择仓库 24。</span><span class="sxs-lookup"><span data-stu-id="ef674-119">If you’re using USMF, you can select warehouse 24.</span></span>  
6. <span data-ttu-id="ef674-120">在“位置”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="ef674-120">In the Location field, enter or select a value.</span></span>
    * <span data-ttu-id="ef674-121">如果您使用 USMF，您可以选择 CP-003。</span><span class="sxs-lookup"><span data-stu-id="ef674-121">If you’re using USMF, you can select CP-003.</span></span>  
7. <span data-ttu-id="ef674-122">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="ef674-122">Close the page.</span></span>

## <a name="create-a-replenishment-location-directive"></a><span data-ttu-id="ef674-123">创建补货位置指令</span><span class="sxs-lookup"><span data-stu-id="ef674-123">Create a replenishment location directive</span></span>
1. <span data-ttu-id="ef674-124">转到“库存管理”>“设置”>“位置指令”。</span><span class="sxs-lookup"><span data-stu-id="ef674-124">Go to Warehouse management > Setup > Location directives.</span></span>
    * <span data-ttu-id="ef674-125">库位指令用于确定在补货流程中应从哪里领料。</span><span class="sxs-lookup"><span data-stu-id="ef674-125">Location directives are used to determine where items should be picked from in the replenishment process.</span></span>  
2. <span data-ttu-id="ef674-126">在“工作订单类型”字段中，选择“补货”。</span><span class="sxs-lookup"><span data-stu-id="ef674-126">In the Work order type field, select 'Replenishment'.</span></span>
3. <span data-ttu-id="ef674-127">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="ef674-127">Click New.</span></span>
4. <span data-ttu-id="ef674-128">在“名称”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="ef674-128">In the Name field, type a value.</span></span>
5. <span data-ttu-id="ef674-129">在“工作类型”字段中，选择“领料”。</span><span class="sxs-lookup"><span data-stu-id="ef674-129">In the Work type field, select 'Pick'.</span></span>
6. <span data-ttu-id="ef674-130">在“站点”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="ef674-130">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="ef674-131">如果您使用 USMF，您可以选择站点 2。</span><span class="sxs-lookup"><span data-stu-id="ef674-131">If you’re using USMF, you can select site 2.</span></span>  
7. <span data-ttu-id="ef674-132">在“仓库”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="ef674-132">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="ef674-133">如果您使用 USMF，您可以选择仓库 24。</span><span class="sxs-lookup"><span data-stu-id="ef674-133">If you’re using USMF, you can select warehouse 24.</span></span>  
8. <span data-ttu-id="ef674-134">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="ef674-134">Click Save.</span></span>
9. <span data-ttu-id="ef674-135">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="ef674-135">Click New.</span></span>
10. <span data-ttu-id="ef674-136">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="ef674-136">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="ef674-137">在“截止数量”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="ef674-137">In the To quantity field, enter a number.</span></span>
    * <span data-ttu-id="ef674-138">例如，您可以将其设置为 9999。</span><span class="sxs-lookup"><span data-stu-id="ef674-138">For example, you can set it to 9999.</span></span>  
12. <span data-ttu-id="ef674-139">选中“允许拆分”复选框。</span><span class="sxs-lookup"><span data-stu-id="ef674-139">Select the Allow split check box.</span></span>
    * <span data-ttu-id="ef674-140">如果您选择此选项，工作创建流程将允许工作行数量跨多个位置分解。</span><span class="sxs-lookup"><span data-stu-id="ef674-140">If you select this option, the work creation process will allow work line quantities to be split across multiple locations.</span></span>  
13. <span data-ttu-id="ef674-141">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="ef674-141">Click Save.</span></span>
14. <span data-ttu-id="ef674-142">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="ef674-142">Click New.</span></span>
15. <span data-ttu-id="ef674-143">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="ef674-143">In the list, mark the selected row.</span></span>
16. <span data-ttu-id="ef674-144">在“名称”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="ef674-144">In the Name field, type a value.</span></span>
17. <span data-ttu-id="ef674-145">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="ef674-145">Click Save.</span></span>
18. <span data-ttu-id="ef674-146">单击“编辑查询”。</span><span class="sxs-lookup"><span data-stu-id="ef674-146">Click Edit query.</span></span>
    * <span data-ttu-id="ef674-147">您可以编辑此查询来添加限制，限制在补货流程中可以从哪里选择库存。</span><span class="sxs-lookup"><span data-stu-id="ef674-147">You can edit this query to add restrictions where inventory can be selected from in the replenishment process.</span></span> <span data-ttu-id="ef674-148">例如，可以是仓库应只从仓库的堆放区使用。</span><span class="sxs-lookup"><span data-stu-id="ef674-148">For example, it could be that inventory should only be used from the Bulk area of the warehouse.</span></span>  
19. <span data-ttu-id="ef674-149">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="ef674-149">Click OK.</span></span>
20. <span data-ttu-id="ef674-150">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="ef674-150">Close the page.</span></span>

## <a name="create-a-replenishment-work-template"></a><span data-ttu-id="ef674-151">创建补货工作模板</span><span class="sxs-lookup"><span data-stu-id="ef674-151">Create a replenishment work template</span></span>
1. <span data-ttu-id="ef674-152">转到“仓库管理”>“设置”>“工作”>“工作模板”。</span><span class="sxs-lookup"><span data-stu-id="ef674-152">Go to Warehouse management > Setup > Work > Work templates.</span></span>
    * <span data-ttu-id="ef674-153">工作模板用于指导系统必须如何创建最小/最大补货工作。</span><span class="sxs-lookup"><span data-stu-id="ef674-153">The work template is use to guide the system as to how the min/max replenishment work must be created.</span></span> <span data-ttu-id="ef674-154">至少，必须具有用于领料和放置的工作模板行。</span><span class="sxs-lookup"><span data-stu-id="ef674-154">As a minimum, there must be a work template line for a pick and a put.</span></span> <span data-ttu-id="ef674-155">工作模板将显示无效，直到所有必要信息全部填充。</span><span class="sxs-lookup"><span data-stu-id="ef674-155">The work template will say that it’s Invalid until all the necessary information has been filled in.</span></span>  
2. <span data-ttu-id="ef674-156">在“工作订单类型”字段中，选择“补货”。</span><span class="sxs-lookup"><span data-stu-id="ef674-156">In the Work order type field, select 'Replenishment'.</span></span>
3. <span data-ttu-id="ef674-157">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="ef674-157">Click New.</span></span>
4. <span data-ttu-id="ef674-158">在“工作模板”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="ef674-158">In the Work template field, type a value.</span></span>
5. <span data-ttu-id="ef674-159">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="ef674-159">Click Save.</span></span>
6. <span data-ttu-id="ef674-160">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="ef674-160">Click New.</span></span>
7. <span data-ttu-id="ef674-161">在“工作类型”字段中，选择“领料”。</span><span class="sxs-lookup"><span data-stu-id="ef674-161">In the Work type field, select 'Pick'.</span></span>
8. <span data-ttu-id="ef674-162">在“工作类 ID”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="ef674-162">In the Work class ID field, enter or select a value.</span></span>
    * <span data-ttu-id="ef674-163">这应是与补货相关的工作类。</span><span class="sxs-lookup"><span data-stu-id="ef674-163">This should be a work class related to replenishment.</span></span> <span data-ttu-id="ef674-164">如果您正在使用 USMF，则选择“补货”。</span><span class="sxs-lookup"><span data-stu-id="ef674-164">If you’re using USMF, select Replenish.</span></span>  
9. <span data-ttu-id="ef674-165">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="ef674-165">Click New.</span></span>
10. <span data-ttu-id="ef674-166">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="ef674-166">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="ef674-167">在“工作类型”字段中，选择“放置”。</span><span class="sxs-lookup"><span data-stu-id="ef674-167">In the Work type field, select 'Put'.</span></span>
12. <span data-ttu-id="ef674-168">在“工作类 ID”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="ef674-168">In the Work class ID field, enter or select a value.</span></span>
13. <span data-ttu-id="ef674-169">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="ef674-169">Click Save.</span></span>
14. <span data-ttu-id="ef674-170">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="ef674-170">Close the page.</span></span>

## <a name="create-a-new-replenishment-template"></a><span data-ttu-id="ef674-171">创建新的补货模板</span><span class="sxs-lookup"><span data-stu-id="ef674-171">Create a new replenishment template</span></span>
1. <span data-ttu-id="ef674-172">转到“仓库管理”>“设置”>“补货”>“补货模板”。</span><span class="sxs-lookup"><span data-stu-id="ef674-172">Go to Warehouse management > Setup > Replenishment > Replenishment templates.</span></span>
    * <span data-ttu-id="ef674-173">补货模板用于定义物料和数量以及补货位置。</span><span class="sxs-lookup"><span data-stu-id="ef674-173">The replenishment template is used to define the items and quantities, and the location to replenish.</span></span>  
2. <span data-ttu-id="ef674-174">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="ef674-174">Click New.</span></span>
3. <span data-ttu-id="ef674-175">在“补货模板”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="ef674-175">In the Replenish template field, type a value.</span></span>
    * <span data-ttu-id="ef674-176">为模板指定一个名称以指示它是用于最小/最大补货。</span><span class="sxs-lookup"><span data-stu-id="ef674-176">Give the template a name to indicate that it’s for min/max replenishment.</span></span>  
4. <span data-ttu-id="ef674-177">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="ef674-177">In the Description field, type a value.</span></span>
5. <span data-ttu-id="ef674-178">选择“允许波次需求使用未预留的数量”复选框。</span><span class="sxs-lookup"><span data-stu-id="ef674-178">Select the Allow wave demand to use unreserved quantities check box.</span></span>
    * <span data-ttu-id="ef674-179">如果选择此选项，将支持波次需求补货消耗与最小/最大补货相关的数量。</span><span class="sxs-lookup"><span data-stu-id="ef674-179">If you select this option, it enables wave demand replenishment to consume quantities that are related to min/max replenishment.</span></span> <span data-ttu-id="ef674-180">例如，如果最小/最大补货工作不立即处理，为了避免创建不必要的需求补货工作，这可能很有用。</span><span class="sxs-lookup"><span data-stu-id="ef674-180">For example, this might be useful if the min/max replenishment work isn’t processed immediately, to avoid unnecessary demand replenishment work from being created.</span></span>  
6. <span data-ttu-id="ef674-181">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="ef674-181">Click New.</span></span>
7. <span data-ttu-id="ef674-182">在“序列号”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="ef674-182">In the Sequence number field, enter a number.</span></span>
8. <span data-ttu-id="ef674-183">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="ef674-183">In the Description field, type a value.</span></span>
9. <span data-ttu-id="ef674-184">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="ef674-184">In the list, mark the selected row.</span></span>
10. <span data-ttu-id="ef674-185">在“补货单位”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="ef674-185">In the Replenishment unit field, enter or select a value.</span></span>
    * <span data-ttu-id="ef674-186">例如，选择 pcs。</span><span class="sxs-lookup"><span data-stu-id="ef674-186">For example, select pcs.</span></span> <span data-ttu-id="ef674-187">此设置是强制的。</span><span class="sxs-lookup"><span data-stu-id="ef674-187">This setting is mandatory.</span></span> <span data-ttu-id="ef674-188">它允许您对比在此模板中为最小和最大库存水平指定的单位，指定补货工作的不同度量单位。</span><span class="sxs-lookup"><span data-stu-id="ef674-188">It allows you to specify a different unit of measurement for replenishment work compared to the unit specified for the minimum and maximum stock levels in this template.</span></span>  
11. <span data-ttu-id="ef674-189">在“工作模板”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="ef674-189">In the Work template field, enter or select a value.</span></span>
    * <span data-ttu-id="ef674-190">选择您之前创建的工作模板。</span><span class="sxs-lookup"><span data-stu-id="ef674-190">Choose the work template that you created earlier.</span></span>  
12. <span data-ttu-id="ef674-191">在“最小数量”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="ef674-191">In the Minimum quantity field, enter a number.</span></span>
    * <span data-ttu-id="ef674-192">选择应触发补货的最小数量。</span><span class="sxs-lookup"><span data-stu-id="ef674-192">Select the minimum quantity that should trigger the replenishment.</span></span> <span data-ttu-id="ef674-193">例如，设置此数量为 50。</span><span class="sxs-lookup"><span data-stu-id="ef674-193">For example, set this to 50.</span></span> <span data-ttu-id="ef674-194">如果您在固定位置补货，且“仅对空的固定货位补货”选项设置为“是”，可以将此设置保留为零。</span><span class="sxs-lookup"><span data-stu-id="ef674-194">It is possible to leave this set to zero, if you’re replenishing a fixed location and the Replenish empty fixed locations option is set to Yes.</span></span> <span data-ttu-id="ef674-195">我们还建议您出于绩效原因选择“仅对固定货位补货”选项。</span><span class="sxs-lookup"><span data-stu-id="ef674-195">We also recommend that you select the Replenish only fixed locations option for performance reasons.</span></span>  
13. <span data-ttu-id="ef674-196">在“最大数量”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="ef674-196">In the Maximum quantity field, enter a number.</span></span>
    * <span data-ttu-id="ef674-197">例如，则此设置为 100。</span><span class="sxs-lookup"><span data-stu-id="ef674-197">For example, set this to 100.</span></span>  
14. <span data-ttu-id="ef674-198">在“单位”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="ef674-198">In the Unit field, enter or select a value.</span></span>
    * <span data-ttu-id="ef674-199">为最小和最大数量分配单位。</span><span class="sxs-lookup"><span data-stu-id="ef674-199">Assign the unit for the minimum and maximum quantities.</span></span> <span data-ttu-id="ef674-200">例如，设置此数量为 pcs。</span><span class="sxs-lookup"><span data-stu-id="ef674-200">For example, set this to pcs.</span></span>  
15. <span data-ttu-id="ef674-201">选择“仅对空的固定货位补货”复选框。</span><span class="sxs-lookup"><span data-stu-id="ef674-201">Select the Replenish empty fixed locations check box.</span></span>
    * <span data-ttu-id="ef674-202">选择此复选框以对固定位置为空时补货。</span><span class="sxs-lookup"><span data-stu-id="ef674-202">Select this check box to replenish fixed locations when they are empty.</span></span> <span data-ttu-id="ef674-203">否则，只有具有现有数量的位置进行补货。</span><span class="sxs-lookup"><span data-stu-id="ef674-203">Otherwise, only the locations where there is a quantity on hand will be replenished.</span></span>  
16. <span data-ttu-id="ef674-204">选择“仅对固定货位补货”复选框。</span><span class="sxs-lookup"><span data-stu-id="ef674-204">Select the Replenish only fixed locations check box.</span></span>
17. <span data-ttu-id="ef674-205">单击“选择产品”。</span><span class="sxs-lookup"><span data-stu-id="ef674-205">Click Select products.</span></span>
    * <span data-ttu-id="ef674-206">这是定义应补货哪些产品的位置。</span><span class="sxs-lookup"><span data-stu-id="ef674-206">This is the place to define which products should be replenished.</span></span> <span data-ttu-id="ef674-207">如果选择“固定领料位置”选项，还需要在此查询中定义位置。</span><span class="sxs-lookup"><span data-stu-id="ef674-207">If the Fixed picking locations option is selected, you also need to define the locations in this query.</span></span> <span data-ttu-id="ef674-208">变型特定查询可用，产品特定查询也可用。</span><span class="sxs-lookup"><span data-stu-id="ef674-208">Variant-specific queries are available as well product-specific queries.</span></span>  
18. <span data-ttu-id="ef674-209">选择“物料行”。</span><span class="sxs-lookup"><span data-stu-id="ef674-209">Select the Items row.</span></span>
19. <span data-ttu-id="ef674-210">在“标准”字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="ef674-210">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="ef674-211">选择应在固定位置补货的物料。</span><span class="sxs-lookup"><span data-stu-id="ef674-211">Select the items that should be replenished at the fixed locations.</span></span> <span data-ttu-id="ef674-212">例如，键入 A* 可以选择所有以 A 开头的物料编号。</span><span class="sxs-lookup"><span data-stu-id="ef674-212">For example, type A* to select all item numbers beginning with A.</span></span>  
20. <span data-ttu-id="ef674-213">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="ef674-213">Click Add.</span></span>
    * <span data-ttu-id="ef674-214">添加位置实体（除非已经存在）可以将补货工作限制到特定仓库区域内的固定领料库位。</span><span class="sxs-lookup"><span data-stu-id="ef674-214">Add the Location entity (unless it already exists) to be able to restrict the replenishment work to the fixed picking locations within a specific area of the warehouse.</span></span>  
21. <span data-ttu-id="ef674-215">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="ef674-215">In the list, mark the selected row.</span></span>
22. <span data-ttu-id="ef674-216">将“表”字段设置为“位置”。</span><span class="sxs-lookup"><span data-stu-id="ef674-216">Set the Table field to Locations.</span></span>
23. <span data-ttu-id="ef674-217">在“字段”字段中，选择“位置模板 ID”。</span><span class="sxs-lookup"><span data-stu-id="ef674-217">In the Field field, select Location profile ID.</span></span>
24. <span data-ttu-id="ef674-218">在“标准”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="ef674-218">In the Criteria field, enter or select a value.</span></span>
25. <span data-ttu-id="ef674-219">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="ef674-219">Click OK.</span></span>
26. <span data-ttu-id="ef674-220">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="ef674-220">Close the page.</span></span>

## <a name="set-the-replenishment-process-to-run-as-a-batch-job"></a><span data-ttu-id="ef674-221">设置补货流程以将其作为批处理作业运行</span><span class="sxs-lookup"><span data-stu-id="ef674-221">Set the replenishment process to run as a batch job</span></span>
1. <span data-ttu-id="ef674-222">转到“仓库管理”>“补货”>“补货”。</span><span class="sxs-lookup"><span data-stu-id="ef674-222">Go to Warehouse management > Replenishment > Replenishments.</span></span>
    * <span data-ttu-id="ef674-223">补货页允许您设置补货作为批处理作业运行，或者要求手动开始。</span><span class="sxs-lookup"><span data-stu-id="ef674-223">The Replenishments page allows you to set up replenishment to run as a batch job, or to require that it’s started manually.</span></span>  
2. <span data-ttu-id="ef674-224">单击“筛选器”。</span><span class="sxs-lookup"><span data-stu-id="ef674-224">Click Filter.</span></span>
3. <span data-ttu-id="ef674-225">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="ef674-225">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="ef674-226">在“标准”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="ef674-226">In the Criteria field, enter or select a value.</span></span>
5. <span data-ttu-id="ef674-227">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="ef674-227">Click OK.</span></span>
6. <span data-ttu-id="ef674-228">展开“后台运行”部分。</span><span class="sxs-lookup"><span data-stu-id="ef674-228">Expand the Run in the background section.</span></span>
7. <span data-ttu-id="ef674-229">设置“批处理”选项为“是”。</span><span class="sxs-lookup"><span data-stu-id="ef674-229">Set the Batch processing option to Yes.</span></span>
8. <span data-ttu-id="ef674-230">单击“重复执行”。</span><span class="sxs-lookup"><span data-stu-id="ef674-230">Click Recurrence.</span></span>
9. <span data-ttu-id="ef674-231">选择“无结束日期”选项。</span><span class="sxs-lookup"><span data-stu-id="ef674-231">Select the No end date option.</span></span>
10. <span data-ttu-id="ef674-232">设置重复执行模式。</span><span class="sxs-lookup"><span data-stu-id="ef674-232">Set the Recurrance pattern.</span></span>
    * <span data-ttu-id="ef674-233">例如，选择“天”。</span><span class="sxs-lookup"><span data-stu-id="ef674-233">For example, select Days.</span></span>  
11. <span data-ttu-id="ef674-234">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="ef674-234">Click OK.</span></span>
12. <span data-ttu-id="ef674-235">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="ef674-235">Click OK.</span></span>

