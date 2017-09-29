--- 
title: "定义薪酬流程并计算结果"
description: "薪酬流程用于确定在固定和可变薪酬计划中登记的员工的新的薪酬金额和奖励。"
author: kherr75
manager: AnnBe
ms.date: 06/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: ba28cf1fa6a8e9a4497d3bac1a2161098ec53db1
ms.contentlocale: zh-cn
ms.lasthandoff: 08/29/2017

---
# <a name="define-compensation-process-and-calculate-results"></a><span data-ttu-id="fc700-103">定义薪酬流程并计算结果</span><span class="sxs-lookup"><span data-stu-id="fc700-103">Define compensation process and calculate results</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="fc700-104">薪酬流程用于确定在固定和可变薪酬计划中登记的员工的新的薪酬金额和奖励。</span><span class="sxs-lookup"><span data-stu-id="fc700-104">Compensation processes are used to determine new compensation amounts and awards for employees enrolled in fixed and variable compensation plans.</span></span> <span data-ttu-id="fc700-105">薪酬流程可以运行多次以执行“假设”分析，从而验证所有的更改和设置都正确。</span><span class="sxs-lookup"><span data-stu-id="fc700-105">Compensation processes can be run multiple times to perform "what-if" analysis, to verify all changes and settings are correct.</span></span> <span data-ttu-id="fc700-106">该过程将创建薪酬流程，运行流程，并查看结果。</span><span class="sxs-lookup"><span data-stu-id="fc700-106">This procedure will create a compensation process, run the process, and view the results.</span></span> <span data-ttu-id="fc700-107">创建此程序的演示数据公司是 USMF。</span><span class="sxs-lookup"><span data-stu-id="fc700-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-compensation-process"></a><span data-ttu-id="fc700-108">创建薪酬流程</span><span class="sxs-lookup"><span data-stu-id="fc700-108">Create a compensation process</span></span>
1. <span data-ttu-id="fc700-109">转到“人力资源”>“薪酬”>“流程”>“薪酬流程”。</span><span class="sxs-lookup"><span data-stu-id="fc700-109">Go to Human resources > Compensation > Process > Compensation processes.</span></span>
2. <span data-ttu-id="fc700-110">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="fc700-110">Click New.</span></span>
3. <span data-ttu-id="fc700-111">在“流程”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="fc700-111">In the Process field, type a value.</span></span>
4. <span data-ttu-id="fc700-112">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="fc700-112">In the Description field, type a value.</span></span>
5. <span data-ttu-id="fc700-113">在“流程类型”字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="fc700-113">In the Process type field, select an option.</span></span>
    * <span data-ttu-id="fc700-114">周期指的是评估确定薪酬的时间周期。</span><span class="sxs-lookup"><span data-stu-id="fc700-114">A cycle specifies the time period evaluated to determine compensation.</span></span> <span data-ttu-id="fc700-115">评估会考虑到员工的职位、加入的哪些绩效评级、周期内员工受雇时间百分比的计算等。</span><span class="sxs-lookup"><span data-stu-id="fc700-115">The evaluation considers which positions were held by employees, which performance ratings to include, calculation of the percentage of time the employee was employed during the cycle, and more.</span></span> <span data-ttu-id="fc700-116">周期开始日期的示例可能是上一财政年度的第一天。</span><span class="sxs-lookup"><span data-stu-id="fc700-116">An example of a cycle start date might be the first day of the past fiscal year.</span></span>  
6. <span data-ttu-id="fc700-117">在“周期开始日期”字段中，输入日期。</span><span class="sxs-lookup"><span data-stu-id="fc700-117">In the Cycle start field, enter a date.</span></span>
    * <span data-ttu-id="fc700-118">周期结束日期十分重要，因为该日期用于确定哪些员工被主动雇用且被登记在一个或多个薪酬计划中。</span><span class="sxs-lookup"><span data-stu-id="fc700-118">The cycle end date is  important because it is the date used to determine which employees were actively employed and enrolled in one or more compensation plans.</span></span>  
7. <span data-ttu-id="fc700-119">在“周期结束”字段中，输入日期。</span><span class="sxs-lookup"><span data-stu-id="fc700-119">In the Cycle end field, enter a date.</span></span>
    * <span data-ttu-id="fc700-120">交易生效日期为新的薪酬费率的生效日期。</span><span class="sxs-lookup"><span data-stu-id="fc700-120">The transaction active date is the date the new compensation rates should take effect.</span></span> <span data-ttu-id="fc700-121">一些公司在周期结束日期和新的薪酬费用生效日期之间加入了几个月。</span><span class="sxs-lookup"><span data-stu-id="fc700-121">Many companies include a few months between their end of a cycle and the time the new compensation rates go into effect.</span></span> <span data-ttu-id="fc700-122">该额外时间用于处理和审查新的薪酬。</span><span class="sxs-lookup"><span data-stu-id="fc700-122">The additional time is used for processing and reviewing the new compensation.</span></span>  
8. <span data-ttu-id="fc700-123">在“事务有效日期”字段中，输入日期。</span><span class="sxs-lookup"><span data-stu-id="fc700-123">In the Transaction active date field, enter a date.</span></span>
    * <span data-ttu-id="fc700-124">时间点日期用于可变的薪酬计划中，该计划基于员工在该时间点的薪酬费率来决定员工的奖励金额。</span><span class="sxs-lookup"><span data-stu-id="fc700-124">The point-in-time date is used for variable compensation plans that determine an employee's award amount based on their compensation rate at this point in time.</span></span>  
    * <span data-ttu-id="fc700-125">固定薪酬按比例分配雇用日期，其用于具有“百分比”的雇用规则的固定薪酬计划。</span><span class="sxs-lookup"><span data-stu-id="fc700-125">The fixed pay pro rated hire date is used with fixed compensation plans with a hire rule of Percent.</span></span>  <span data-ttu-id="fc700-126"> 在周期开始日期和固定薪酬按比例分配的雇用日期之间，受雇用的雇员将得到他们所计算的薪酬增加的 100%，而不是按比例分摊百分比。</span><span class="sxs-lookup"><span data-stu-id="fc700-126">Employees who are hired between the cycle start and the fixed pay pro rated hire date will receive 100% of their calculated compensation increase, instead of pro-rated percentage.</span></span>  
9. <span data-ttu-id="fc700-127">在“固定薪酬按比例分配雇用日期”字段中，输入日期。</span><span class="sxs-lookup"><span data-stu-id="fc700-127">In the Fixed pay pro rated hire date field, enter a date.</span></span>
    * <span data-ttu-id="fc700-128">审查截止日期是指所有流程结果审查完后的日期，以便可以在交易生效日期之前将结果载入员工的薪酬记录。</span><span class="sxs-lookup"><span data-stu-id="fc700-128">The review deadline is the date by which all process results should be reviewed so that they can be loaded into an employee's compensation record before the transaction active date.</span></span> <span data-ttu-id="fc700-129">该字段仅用于提供信息。</span><span class="sxs-lookup"><span data-stu-id="fc700-129">This field is informational only.</span></span>  
10. <span data-ttu-id="fc700-130">在“审查截止日期”字段中，输入日期。</span><span class="sxs-lookup"><span data-stu-id="fc700-130">In the Review deadline field, enter a date.</span></span>
11. <span data-ttu-id="fc700-131">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="fc700-131">Click Save.</span></span>

## <a name="setup-the-compensation-plans-and-actions-for-a-compensation-process"></a><span data-ttu-id="fc700-132">为薪酬流程设置薪酬计划和操作</span><span class="sxs-lookup"><span data-stu-id="fc700-132">Setup the compensation plans and actions for a compensation process</span></span>
1. <span data-ttu-id="fc700-133">单击“设置”。</span><span class="sxs-lookup"><span data-stu-id="fc700-133">Click Setup.</span></span>
    * <span data-ttu-id="fc700-134">“设置”页用于选择：作为此薪酬流程的一部分，应处理哪一计划，以及针对每个计划需要采取哪些行动。</span><span class="sxs-lookup"><span data-stu-id="fc700-134">The Setup page is used to select which plans to process as part of this compensation process, as well as which actions should be taken against each plan.</span></span>  
2. <span data-ttu-id="fc700-135">在“计划”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="fc700-135">In the Plan field, enter or select a value.</span></span>
3. <span data-ttu-id="fc700-136">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="fc700-136">Click Save.</span></span>
4. <span data-ttu-id="fc700-137">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="fc700-137">Click Add.</span></span>
5. <span data-ttu-id="fc700-138">在“行为”字段中，选择“行为的权益类型”。</span><span class="sxs-lookup"><span data-stu-id="fc700-138">In the Action field, select an Equity type of action.</span></span>
6. <span data-ttu-id="fc700-139">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="fc700-139">Click Add.</span></span>
7. <span data-ttu-id="fc700-140">在“行为”字段中，选择“行为的绩效类型”。</span><span class="sxs-lookup"><span data-stu-id="fc700-140">In the Action field, select a Merit type of action.</span></span>
    * <span data-ttu-id="fc700-141">可以通过使用“使用上一结果”字段表明所选操作是否应使用员工的基本工资或先前操作结果作为此操作的计算起点，将薪酬操作“链接”在一起。</span><span class="sxs-lookup"><span data-stu-id="fc700-141">Compensation actions can be "chained" together using the Use previous result field to indicate whether the selected action should use the employees base pay or the result of the previous action as the starting point for this action's calculation.</span></span>  
8. <span data-ttu-id="fc700-142">在“使用先前结果”字段中，选择“是”。</span><span class="sxs-lookup"><span data-stu-id="fc700-142">Select Yes in the Use previous result field.</span></span>
9. <span data-ttu-id="fc700-143">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="fc700-143">Click Add.</span></span>
10. <span data-ttu-id="fc700-144">在“行为”字段中，选择“行为的常规类型”。</span><span class="sxs-lookup"><span data-stu-id="fc700-144">In the Action field, select a General type of Action.</span></span>
    * <span data-ttu-id="fc700-145">不同的薪酬操作类型启用不同的字段。</span><span class="sxs-lookup"><span data-stu-id="fc700-145">Different compensation action types enable different fields.</span></span> <span data-ttu-id="fc700-146">对于“通用薪酬操作类型”，可指定增加百分比或金额。</span><span class="sxs-lookup"><span data-stu-id="fc700-146">For a General compensation action type, an increase percent or increase amount can be specified.</span></span>  
11. <span data-ttu-id="fc700-147">选择“选择增加金额”选项。</span><span class="sxs-lookup"><span data-stu-id="fc700-147">Select the Select increase amount option.</span></span>
12. <span data-ttu-id="fc700-148">在“增加金额”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="fc700-148">In the Increase amount field, enter a number.</span></span>
13. <span data-ttu-id="fc700-149">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="fc700-149">Click Add.</span></span>
14. <span data-ttu-id="fc700-150">在“行为”字段中，选择“行为的促销类型”。</span><span class="sxs-lookup"><span data-stu-id="fc700-150">In the Action field, select a Promotion type of Action.</span></span>
    * <span data-ttu-id="fc700-151">“促销”和“其他级别的更改操作类型”可以让用户手动调整员工薪酬。</span><span class="sxs-lookup"><span data-stu-id="fc700-151">Promotion and Other level change action types enable users to make manual adjustments to employee compensation.</span></span> <span data-ttu-id="fc700-152">对于这些操作类型可以启用建议，同时其他操作类型则需要输入员工的新建议薪酬。</span><span class="sxs-lookup"><span data-stu-id="fc700-152">Recommendations can be enabled for these action types, as well as other action types to enable you to enter a new recommended compensation value for an employee.</span></span>  
15. <span data-ttu-id="fc700-153">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="fc700-153">Click Add.</span></span>
16. <span data-ttu-id="fc700-154">在“类型”字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="fc700-154">In the Type field, select an option.</span></span>
    * <span data-ttu-id="fc700-155">固定和可变薪酬计划可在同一薪酬流程中运行。</span><span class="sxs-lookup"><span data-stu-id="fc700-155">Fixed and variable compensation plans can be run in the same compensation process.</span></span>  
17. <span data-ttu-id="fc700-156">在“计划”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="fc700-156">In the Plan field, enter or select a value.</span></span>
    * <span data-ttu-id="fc700-157">使用“启用绩效薪酬”复选框，确定是否基于员工的绩效等级调整固定和可变薪酬金额。</span><span class="sxs-lookup"><span data-stu-id="fc700-157">Use the Enable pay for performance check box to determined whether fixed and variable compensation amounts should be adjusted based on the employee's performance rating.</span></span>  
    * <span data-ttu-id="fc700-158">在可变薪酬计划中可以替换杠杆作用。</span><span class="sxs-lookup"><span data-stu-id="fc700-158">Leverage can be overridden on variable compensation plans.</span></span>  
18. <span data-ttu-id="fc700-159">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="fc700-159">Click Save.</span></span>
19. <span data-ttu-id="fc700-160">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="fc700-160">Click Add.</span></span>
20. <span data-ttu-id="fc700-161">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="fc700-161">Close the page.</span></span>

## <a name="run-the-compensation-process"></a><span data-ttu-id="fc700-162">运行薪酬流程</span><span class="sxs-lookup"><span data-stu-id="fc700-162">Run the compensation process</span></span>
1. <span data-ttu-id="fc700-163">单击“运行流程“。</span><span class="sxs-lookup"><span data-stu-id="fc700-163">Click Run process.</span></span>
    * <span data-ttu-id="fc700-164">“显示处理结果”可在处理完成后，查看完整的薪酬流程的处理消息。</span><span class="sxs-lookup"><span data-stu-id="fc700-164">The Show processing results control lets you view processing messages for the complete compensation process when processing has finished.</span></span>  
2. <span data-ttu-id="fc700-165">在“显示处理结果”字段中，选择“是”。</span><span class="sxs-lookup"><span data-stu-id="fc700-165">Select Yes in the Show processing results field.</span></span>
3. <span data-ttu-id="fc700-166">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="fc700-166">Click OK.</span></span>

## <a name="view-the-results"></a><span data-ttu-id="fc700-167">查看结果</span><span class="sxs-lookup"><span data-stu-id="fc700-167">View the results</span></span>
1. <span data-ttu-id="fc700-168">单击“流程结果”。</span><span class="sxs-lookup"><span data-stu-id="fc700-168">Click Process results.</span></span>
2. <span data-ttu-id="fc700-169">单击“员工结果”。</span><span class="sxs-lookup"><span data-stu-id="fc700-169">Click Employee results.</span></span>
3. <span data-ttu-id="fc700-170">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="fc700-170">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="fc700-171">展开“固定薪酬”部分。</span><span class="sxs-lookup"><span data-stu-id="fc700-171">Expand the Fixed compensation section.</span></span>
    * <span data-ttu-id="fc700-172">展开快速选项卡以查看流程结果。</span><span class="sxs-lookup"><span data-stu-id="fc700-172">Expand the FastTabs to view the results of the process.</span></span> <span data-ttu-id="fc700-173">如果已标记薪酬操作为“启用建议”，则可为该操作启用“建议”字段。</span><span class="sxs-lookup"><span data-stu-id="fc700-173">If Enable recommendations was marked for a compensation action, the Recommendation fields will be enabled for that action.</span></span>  
5. <span data-ttu-id="fc700-174">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="fc700-174">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="fc700-175">可以通过单击“查看结果”按钮查看单个员工的薪酬结果。</span><span class="sxs-lookup"><span data-stu-id="fc700-175">The results for a single employee can be viewed by clicking the View results button.</span></span>  
    * <span data-ttu-id="fc700-176">您可以通过在“建议”字段调整百分比或增加金额以重写计算的薪资金额。</span><span class="sxs-lookup"><span data-stu-id="fc700-176">You can overwrite the calculated compensation amount by adjusting the percent or the increase amount in the Recommendation fields.</span></span>  
6. <span data-ttu-id="fc700-177">在“建议百分比”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="fc700-177">In the percent recommended field, enter a number.</span></span>
7. <span data-ttu-id="fc700-178">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="fc700-178">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="fc700-179">在“建议百分比”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="fc700-179">In the percent recommended field, enter a number.</span></span>
    * <span data-ttu-id="fc700-180">重新计算可用于忽略现有记录中的任何更改，并记录和生成所选员工的新的薪酬结果。</span><span class="sxs-lookup"><span data-stu-id="fc700-180">Recalculate can be used to ignore any changes made to the existing record and generate a new compensation result for the selected employee.</span></span>  
    * <span data-ttu-id="fc700-181">当完成一个员工的所有更改后，则将状态更改为“已核准”。</span><span class="sxs-lookup"><span data-stu-id="fc700-181">When all changes are complete for an employee, change the status to Approved.</span></span>  
9. <span data-ttu-id="fc700-182">单击“更改状态”。</span><span class="sxs-lookup"><span data-stu-id="fc700-182">Click Change status.</span></span>
10. <span data-ttu-id="fc700-183">单击“核准”。</span><span class="sxs-lookup"><span data-stu-id="fc700-183">Click Approved.</span></span>
    * <span data-ttu-id="fc700-184">核准完该记录后，将其加载到员工的正式薪酬记录中。</span><span class="sxs-lookup"><span data-stu-id="fc700-184">After the record has been approved it can be loaded to the employee's official compensation record.</span></span> <span data-ttu-id="fc700-185">新的薪酬将在薪酬流程设置的交易记录日期内均有效。</span><span class="sxs-lookup"><span data-stu-id="fc700-185">The new compensation will be effective as of the transaction date set on the compensation process.</span></span>  


