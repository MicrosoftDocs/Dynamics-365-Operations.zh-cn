---
title: 应计休假和缺勤计划
description: 您可以在 Dynamics 365 Human Resources 中累积多个或单个员工的休假和缺勤。
author: andreabichsel
ms.date: 05/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ddd4c55f6ebfbe91fb949a92cb379f51d826c465
ms.sourcegitcommit: cee7887282d372c756c5c11f76684315f249bba5
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/24/2021
ms.locfileid: "6303456"
---
# <a name="accrue-leave-and-absence-plans"></a><span data-ttu-id="c705f-103">应计休假和缺勤计划</span><span class="sxs-lookup"><span data-stu-id="c705f-103">Accrue leave and absence plans</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="c705f-104">您可以在 Dynamics 365 Human Resources 中累积多个或单个员工的休假和缺勤。</span><span class="sxs-lookup"><span data-stu-id="c705f-104">You can accrue leave and absence in Dynamics 365 Human Resources for multiple employees or for an individual.</span></span>

## <a name="accrue-leave-and-absence-for-multiple-employees"></a><span data-ttu-id="c705f-105">累积多个员工的休假和缺勤</span><span class="sxs-lookup"><span data-stu-id="c705f-105">Accrue leave and absence for multiple employees</span></span>

1. <span data-ttu-id="c705f-106">在 **休假和缺勤** 页面，选择 **链接** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="c705f-106">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="c705f-107">在 **管理休假** 下，选择 **累积休假和缺勤计划**。</span><span class="sxs-lookup"><span data-stu-id="c705f-107">Under **Manage leave**, select **Accrue leave and absence plans**.</span></span>

3. <span data-ttu-id="c705f-108">将显示 **累积休假和缺勤计划** 对话框。</span><span class="sxs-lookup"><span data-stu-id="c705f-108">The **Accrue leave and absence plans** dialog box appears.</span></span> <span data-ttu-id="c705f-109">在 **累积截至** 中，选择 **今日日期**，或选择 **自定义日期** 并输入一个自定义日期。</span><span class="sxs-lookup"><span data-stu-id="c705f-109">In **Accrue as of**, either select **Today's date** or select **Custom date** and enter a custom date.</span></span>

4. <span data-ttu-id="c705f-110">如果要为所有公司运行应计，请选择 **所有公司**。</span><span class="sxs-lookup"><span data-stu-id="c705f-110">If you want to run accruals for all companies, select **All companies**.</span></span> <span data-ttu-id="c705f-111">如果要处理单个休假计划的应计，请为 **所有计划** 选择 **否**，然后选择 **休假计划**。</span><span class="sxs-lookup"><span data-stu-id="c705f-111">If you want to process accruals for a single leave plan, select **No** for **All plans**, and then select a **Leave plan**.</span></span> <span data-ttu-id="c705f-112">如果选择所有公司，则不能选择单个休假计划。</span><span class="sxs-lookup"><span data-stu-id="c705f-112">If you select all companies, you can't select an individual leave plan.</span></span>

5. <span data-ttu-id="c705f-113">如果要在后台运行累积流程，请选择 **在后台运行** 并执行以下任务：</span><span class="sxs-lookup"><span data-stu-id="c705f-113">If you want to run the accrual process in the background, select **Run in the background** and do the following tasks:</span></span>

    1. <span data-ttu-id="c705f-114">输入累积流程的信息。</span><span class="sxs-lookup"><span data-stu-id="c705f-114">Enter information for the accrual process.</span></span>
    2. <span data-ttu-id="c705f-115">要设置定期作业，选择 **定期**，输入定期信息，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="c705f-115">To set up a recurring job, select **Recurrence**, enter the recurrence information, and then select **OK**.</span></span>
    3. <span data-ttu-id="c705f-116">要设置作业预警，请选择 **预警**，选择要接收的预警，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="c705f-116">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>
    4. <span data-ttu-id="c705f-117">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="c705f-117">Select **OK**.</span></span> <span data-ttu-id="c705f-118">累积流程将使用您设置的参数运行。</span><span class="sxs-lookup"><span data-stu-id="c705f-118">The accrual process will run with the parameters you set.</span></span> 

## <a name="accrue-leave-and-absence-for-an-employee"></a><span data-ttu-id="c705f-119">累积一个员工的休假和缺勤</span><span class="sxs-lookup"><span data-stu-id="c705f-119">Accrue leave and absence for an employee</span></span>

1. <span data-ttu-id="c705f-120">在员工的记录上，选择 **休假**。</span><span class="sxs-lookup"><span data-stu-id="c705f-120">On the employee's record, select **Leave**.</span></span>

2. <span data-ttu-id="c705f-121">选择 **累积休假和缺勤**。</span><span class="sxs-lookup"><span data-stu-id="c705f-121">Select **Accrue leave and absence**.</span></span>

3. <span data-ttu-id="c705f-122">将显示 **累积休假和缺勤计划** 对话框。</span><span class="sxs-lookup"><span data-stu-id="c705f-122">The **Accrue leave and absence plans** dialog box appears.</span></span> <span data-ttu-id="c705f-123">在 **累积截至** 中，选择 **今日日期**，或选择 **自定义日期** 并输入一个自定义日期。</span><span class="sxs-lookup"><span data-stu-id="c705f-123">In **Accrue as of**, either select **Today's date** or select **Custom date** and enter a custom date.</span></span>

4. <span data-ttu-id="c705f-124">如果要为所有公司运行应计，请选择 **所有公司**。</span><span class="sxs-lookup"><span data-stu-id="c705f-124">If you want to run accruals for all companies, select **All companies**.</span></span> <span data-ttu-id="c705f-125">如果要处理单个休假计划的应计，请为 **所有计划** 选择 **否**，然后选择 **休假计划**。</span><span class="sxs-lookup"><span data-stu-id="c705f-125">If you want to process accruals for a single leave plan, select **No** for **All plans**, and then select a **Leave plan**.</span></span> <span data-ttu-id="c705f-126">如果选择所有公司，则不能选择单个休假计划。</span><span class="sxs-lookup"><span data-stu-id="c705f-126">If you select all companies, you can't select an individual leave plan.</span></span>

5. <span data-ttu-id="c705f-127">如果要在后台运行累积流程，请选择 **在后台运行** 并执行以下任务：</span><span class="sxs-lookup"><span data-stu-id="c705f-127">If you want to run the accrual process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="c705f-128">输入累积流程的信息。</span><span class="sxs-lookup"><span data-stu-id="c705f-128">Enter information for the accrual process.</span></span>

   2. <span data-ttu-id="c705f-129">要设置重复性作业，请选择 **重复**，输入重复信息，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="c705f-129">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="c705f-130">要设置作业预警，请选择 **预警**，选择要接收的预警，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="c705f-130">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="c705f-131">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="c705f-131">Select **OK**.</span></span> <span data-ttu-id="c705f-132">累积流程将使用您设置的参数运行。</span><span class="sxs-lookup"><span data-stu-id="c705f-132">The accrual process will run with the parameters you set.</span></span>

## <a name="delete-leave-and-absence-accruals-for-multiple-employees"></a><span data-ttu-id="c705f-133">删除多个员工的休假和缺勤累积</span><span class="sxs-lookup"><span data-stu-id="c705f-133">Delete leave and absence accruals for multiple employees</span></span>

<span data-ttu-id="c705f-134">删除特定计划和日期范围的累积记录。</span><span class="sxs-lookup"><span data-stu-id="c705f-134">Delete accrual records for a specific plan and date range.</span></span> <span data-ttu-id="c705f-135">累积日期必须是今天或将来的日期。</span><span class="sxs-lookup"><span data-stu-id="c705f-135">Accrual dates must be dated today or in the future.</span></span>

1. <span data-ttu-id="c705f-136">在 **休假和缺勤** 页面，选择 **链接** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="c705f-136">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="c705f-137">在 **管理休假** 下，选择 **删除休假和缺勤计划应计项目**。</span><span class="sxs-lookup"><span data-stu-id="c705f-137">Under **Manage leave**, select **Delete leave and absence plan accruals**.</span></span>

3. <span data-ttu-id="c705f-138">在 **删除休假和缺勤计划应计项目** 对话框中，选择 **休假计划**。</span><span class="sxs-lookup"><span data-stu-id="c705f-138">In the **Delete leave and absence plan accruals** dialog box, select the **Leave plan**.</span></span>

4. <span data-ttu-id="c705f-139">如果适合，选择 **删除余额调整**。</span><span class="sxs-lookup"><span data-stu-id="c705f-139">If applicable, choose **Delete balance adjustments**.</span></span>

5. <span data-ttu-id="c705f-140">输入或选择一个 **休假应计日期**。</span><span class="sxs-lookup"><span data-stu-id="c705f-140">Enter or select a **Leave accrual date**.</span></span> <span data-ttu-id="c705f-141">这个日期必须是当天或在将来。</span><span class="sxs-lookup"><span data-stu-id="c705f-141">This date has to be either today or in the future.</span></span>

6. <span data-ttu-id="c705f-142">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="c705f-142">Select **OK**.</span></span> <span data-ttu-id="c705f-143">累积流程将使用您设置的参数删除累积。</span><span class="sxs-lookup"><span data-stu-id="c705f-143">The accrual process will delete accruals with the parameters you set.</span></span>

## <a name="delete-leave-and-absence-accruals-for-a-single-employee"></a><span data-ttu-id="c705f-144">删除一个员工的休假和缺勤累积</span><span class="sxs-lookup"><span data-stu-id="c705f-144">Delete leave and absence accruals for a single employee</span></span>

1. <span data-ttu-id="c705f-145">在员工的记录上，选择 **休假**。</span><span class="sxs-lookup"><span data-stu-id="c705f-145">On the employee's record, select **Leave**.</span></span>

2. <span data-ttu-id="c705f-146">选择 **删除休假和缺勤计划应计项目**。</span><span class="sxs-lookup"><span data-stu-id="c705f-146">Select **Delete leave and absence plan accruals**.</span></span>

3. <span data-ttu-id="c705f-147">在 **删除休假和缺勤计划应计项目** 对话框中，选择 **休假计划**。</span><span class="sxs-lookup"><span data-stu-id="c705f-147">In the **Delete leave and absence plan accruals** dialog box, select **Leave plan**.</span></span>

4. <span data-ttu-id="c705f-148">如果适合，选择 **删除余额调整**。</span><span class="sxs-lookup"><span data-stu-id="c705f-148">If applicable, choose **Delete balance adjustments**.</span></span>

5. <span data-ttu-id="c705f-149">输入或选择一个 **休假应计日期**。</span><span class="sxs-lookup"><span data-stu-id="c705f-149">Enter or select a **Leave accrual date**.</span></span> <span data-ttu-id="c705f-150">这个日期必须是当天或在将来。</span><span class="sxs-lookup"><span data-stu-id="c705f-150">This date must be either today or in the future.</span></span>

6. <span data-ttu-id="c705f-151">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="c705f-151">Select **OK**.</span></span> <span data-ttu-id="c705f-152">累积流程将使用您设置的参数删除累积。</span><span class="sxs-lookup"><span data-stu-id="c705f-152">The accrual process will delete accruals with the parameters you set.</span></span>

## <a name="review-leave-accrual-and-deletion-processes"></a><span data-ttu-id="c705f-153">检查休假累积和删除流程</span><span class="sxs-lookup"><span data-stu-id="c705f-153">Review leave accrual and deletion processes</span></span>

<span data-ttu-id="c705f-154">每次运行或删除一个或多个员工的累积时，都将显示 **休假累积审核**。</span><span class="sxs-lookup"><span data-stu-id="c705f-154">**Leave accrual audit** displays each time you run or delete an accrual for one or all employees.</span></span> <span data-ttu-id="c705f-155">还将显示执行操作的日期和人员。</span><span class="sxs-lookup"><span data-stu-id="c705f-155">The date and person who performed the action also displays.</span></span>

1. <span data-ttu-id="c705f-156">在 **休假和缺勤** 页面，选择 **链接** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="c705f-156">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="c705f-157">在 **管理休假** 下，选择 **删除休假累积审核**。</span><span class="sxs-lookup"><span data-stu-id="c705f-157">Under **Manage leave**, select **Delete leave accrual audit**.</span></span>

## <a name="leave-accrual-transaction-auditing"></a><span data-ttu-id="c705f-158">休假应计交易记录审计</span><span class="sxs-lookup"><span data-stu-id="c705f-158">Leave accrual transaction auditing</span></span>

<span data-ttu-id="c705f-159">此功能可帮助休假和缺勤管理人员了解与特定休假类型的员工休息时间余额相关的休假和缺勤应计交易。</span><span class="sxs-lookup"><span data-stu-id="c705f-159">This feature helps leave and absence managers understand the leave and absence accrual transactions related to an employee’s time off balances for a specific leave type.</span></span>

<span data-ttu-id="c705f-160">查看交易详细信息：</span><span class="sxs-lookup"><span data-stu-id="c705f-160">To view transaction details:</span></span>

1. <span data-ttu-id="c705f-161">在员工的记录上，选择 **休假**。</span><span class="sxs-lookup"><span data-stu-id="c705f-161">On the employee's record, select **Leave**.</span></span>

2. <span data-ttu-id="c705f-162">选择 **查看休息时间**，然后选择 **余额** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="c705f-162">Select **View time off**, and then select the **Balances** tab.</span></span>

<span data-ttu-id="c705f-163">要查看与特定休假类型相关的应计交易，选择 **当前余额** 列中的数值。</span><span class="sxs-lookup"><span data-stu-id="c705f-163">To view the accrual transactions related to a specific leave type, select the numerical value in the **Current balance** column.</span></span>

<span data-ttu-id="c705f-164">要查看特定应计金额的交易详细信息，选择一个应计行，打开右侧的 **相关信息** 面板，然后打开 **交易详细信息** 部分。</span><span class="sxs-lookup"><span data-stu-id="c705f-164">To view the transaction details for a specific accrual amount, select an accrual row, open the **Related information** panel on the right, and then open the **Transaction details** section.</span></span> <span data-ttu-id="c705f-165">“交易详细信息”部分显示：</span><span class="sxs-lookup"><span data-stu-id="c705f-165">The Transaction details section displays:</span></span>

- <span data-ttu-id="c705f-166">员工休假类型余额的更改</span><span class="sxs-lookup"><span data-stu-id="c705f-166">Changes to the employee’s leave type balance</span></span>
- <span data-ttu-id="c705f-167">指定应计期间的雇用详细信息</span><span class="sxs-lookup"><span data-stu-id="c705f-167">Employment details for that specified accrual period</span></span>
- <span data-ttu-id="c705f-168">有关应计期间和费率的详细信息</span><span class="sxs-lookup"><span data-stu-id="c705f-168">Details about the accrual period and rates</span></span>
- <span data-ttu-id="c705f-169">对休假计划配置所作的任何更改</span><span class="sxs-lookup"><span data-stu-id="c705f-169">Any changes made to leave plan configurations</span></span>

![显示休假应计交易审计](media/hr-leave-and-absence-accrue-audit.png)

## <a name="see-also"></a><span data-ttu-id="c705f-171">请参阅</span><span class="sxs-lookup"><span data-stu-id="c705f-171">See also</span></span>

[<span data-ttu-id="c705f-172">休假和缺勤概览</span><span class="sxs-lookup"><span data-stu-id="c705f-172">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)</br>
[<span data-ttu-id="c705f-173">创建休假和缺勤计划</span><span class="sxs-lookup"><span data-stu-id="c705f-173">Create a leave and absence plan</span></span>](hr-leave-and-absence-plans.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
