---
title: 应计休假和缺勤计划
description: 您可以在 Dynamics 365 Human Resources 中累积多个或单个员工的休假和缺勤。
author: andreabichsel
manager: AnnBe
ms.date: 06/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
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
ms.openlocfilehash: 43c16c5d0de91bf1f433f4fde36e7d13775f44a0
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4417516"
---
# <a name="accrue-leave-and-absence-plans"></a><span data-ttu-id="e9a1a-103">应计休假和缺勤计划</span><span class="sxs-lookup"><span data-stu-id="e9a1a-103">Accrue leave and absence plans</span></span>

<span data-ttu-id="e9a1a-104">您可以在 Dynamics 365 Human Resources 中累积多个或单个员工的休假和缺勤。</span><span class="sxs-lookup"><span data-stu-id="e9a1a-104">You can accrue leave and absence in Dynamics 365 Human Resources for multiple employees or for an individual.</span></span>

## <a name="accrue-leave-and-absence-for-multiple-employees"></a><span data-ttu-id="e9a1a-105">累积多个员工的休假和缺勤</span><span class="sxs-lookup"><span data-stu-id="e9a1a-105">Accrue leave and absence for multiple employees</span></span>

1. <span data-ttu-id="e9a1a-106">在 **休假和缺勤** 页面，选择 **链接** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="e9a1a-106">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="e9a1a-107">在 **管理休假** 下，选择 **累积休假和缺勤计划**。</span><span class="sxs-lookup"><span data-stu-id="e9a1a-107">Under **Manage leave**, select **Accrue leave and absence plans**.</span></span>

3. <span data-ttu-id="e9a1a-108">将显示 **累积休假和缺勤计划** 对话框。</span><span class="sxs-lookup"><span data-stu-id="e9a1a-108">The **Accrue leave and absence plans** dialog box appears.</span></span> <span data-ttu-id="e9a1a-109">在 **累积截至** 中，选择 **今日日期**，或选择 **自定义日期** 并输入一个自定义日期。</span><span class="sxs-lookup"><span data-stu-id="e9a1a-109">In **Accrue as of**, either select **Today's date** or select **Custom date** and enter a custom date.</span></span>

4. <span data-ttu-id="e9a1a-110">如果要为所有公司运行应计，请选择 **所有公司**。</span><span class="sxs-lookup"><span data-stu-id="e9a1a-110">If you want to run accruals for all companies, select **All companies**.</span></span> <span data-ttu-id="e9a1a-111">如果要处理单个休假计划的应计，请为 **所有计划** 选择 **否**，然后选择 **休假计划**。</span><span class="sxs-lookup"><span data-stu-id="e9a1a-111">If you want to process accruals for a single leave plan, select **No** for **All plans**, and then select a **Leave plan**.</span></span> <span data-ttu-id="e9a1a-112">如果选择所有公司，则不能选择单个休假计划。</span><span class="sxs-lookup"><span data-stu-id="e9a1a-112">If you select all companies, you can't select an individual leave plan.</span></span> 

5. <span data-ttu-id="e9a1a-113">如果要在后台运行累积流程，请选择 **在后台运行** 并执行以下任务：</span><span class="sxs-lookup"><span data-stu-id="e9a1a-113">If you want to run the accrual process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="e9a1a-114">输入累积流程的信息。</span><span class="sxs-lookup"><span data-stu-id="e9a1a-114">Enter information for the accrual process.</span></span>

   2. <span data-ttu-id="e9a1a-115">要设置重复性作业，请选择 **重复**，输入重复信息，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="e9a1a-115">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="e9a1a-116">要设置作业预警，请选择 **预警**，选择要接收的预警，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="e9a1a-116">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="e9a1a-117">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="e9a1a-117">Select **OK**.</span></span> <span data-ttu-id="e9a1a-118">累积流程将使用您设置的参数运行。</span><span class="sxs-lookup"><span data-stu-id="e9a1a-118">The accrual process will run with the parameters you set.</span></span>

## <a name="accrue-leave-and-absence-for-an-employee"></a><span data-ttu-id="e9a1a-119">累积一个员工的休假和缺勤</span><span class="sxs-lookup"><span data-stu-id="e9a1a-119">Accrue leave and absence for an employee</span></span>

1. <span data-ttu-id="e9a1a-120">在员工的记录上，选择 **休假**。</span><span class="sxs-lookup"><span data-stu-id="e9a1a-120">On the employee's record, select **Leave**.</span></span>

2. <span data-ttu-id="e9a1a-121">选择 **累积休假和缺勤**。</span><span class="sxs-lookup"><span data-stu-id="e9a1a-121">Select **Accrue leave and absence**.</span></span>

3. <span data-ttu-id="e9a1a-122">将显示 **累积休假和缺勤计划** 对话框。</span><span class="sxs-lookup"><span data-stu-id="e9a1a-122">The **Accrue leave and absence plans** dialog box appears.</span></span> <span data-ttu-id="e9a1a-123">在 **累积截至** 中，选择 **今日日期**，或选择 **自定义日期** 并输入一个自定义日期。</span><span class="sxs-lookup"><span data-stu-id="e9a1a-123">In **Accrue as of**, either select **Today's date** or select **Custom date** and enter a custom date.</span></span>

4. <span data-ttu-id="e9a1a-124">如果要为所有公司运行应计，请选择 **所有公司**。</span><span class="sxs-lookup"><span data-stu-id="e9a1a-124">If you want to run accruals for all companies, select **All companies**.</span></span> <span data-ttu-id="e9a1a-125">如果要处理单个休假计划的应计，请为 **所有计划** 选择 **否**，然后选择 **休假计划**。</span><span class="sxs-lookup"><span data-stu-id="e9a1a-125">If you want to process accruals for a single leave plan, select **No** for **All plans**, and then select a **Leave plan**.</span></span> <span data-ttu-id="e9a1a-126">如果选择所有公司，则不能选择单个休假计划。</span><span class="sxs-lookup"><span data-stu-id="e9a1a-126">If you select all companies, you can't select an individual leave plan.</span></span> 

5. <span data-ttu-id="e9a1a-127">如果要在后台运行累积流程，请选择 **在后台运行** 并执行以下任务：</span><span class="sxs-lookup"><span data-stu-id="e9a1a-127">If you want to run the accrual process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="e9a1a-128">输入累积流程的信息。</span><span class="sxs-lookup"><span data-stu-id="e9a1a-128">Enter information for the accrual process.</span></span>

   2. <span data-ttu-id="e9a1a-129">要设置重复性作业，请选择 **重复**，输入重复信息，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="e9a1a-129">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="e9a1a-130">要设置作业预警，请选择 **预警**，选择要接收的预警，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="e9a1a-130">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="e9a1a-131">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="e9a1a-131">Select **OK**.</span></span> <span data-ttu-id="e9a1a-132">累积流程将使用您设置的参数运行。</span><span class="sxs-lookup"><span data-stu-id="e9a1a-132">The accrual process will run with the parameters you set.</span></span>

## <a name="delete-leave-and-absence-accruals-for-multiple-employees"></a><span data-ttu-id="e9a1a-133">删除多个员工的休假和缺勤累积</span><span class="sxs-lookup"><span data-stu-id="e9a1a-133">Delete leave and absence accruals for multiple employees</span></span>

<span data-ttu-id="e9a1a-134">删除特定计划和日期范围的累积记录。</span><span class="sxs-lookup"><span data-stu-id="e9a1a-134">Delete accrual records for a specific plan and date range.</span></span> <span data-ttu-id="e9a1a-135">累积日期必须是今天或将来的日期。</span><span class="sxs-lookup"><span data-stu-id="e9a1a-135">Accrual dates must be dated today or in the future.</span></span>

1. <span data-ttu-id="e9a1a-136">在 **休假和缺勤** 页面，选择 **链接** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="e9a1a-136">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="e9a1a-137">在 **管理休假** 下，选择 **删除休假和缺勤计划应计项目**。</span><span class="sxs-lookup"><span data-stu-id="e9a1a-137">Under **Manage leave**, select **Delete leave and absence plan accruals**.</span></span>

3. <span data-ttu-id="e9a1a-138">在 **删除休假和缺勤计划应计项目** 对话框中，选择 **休假计划**。</span><span class="sxs-lookup"><span data-stu-id="e9a1a-138">In the **Delete leave and absence plan accruals** dialog box, select the **Leave plan**.</span></span> 

4. <span data-ttu-id="e9a1a-139">如果适合，选择 **删除余额调整**。</span><span class="sxs-lookup"><span data-stu-id="e9a1a-139">If applicable, choose **Delete balance adjustments**.</span></span>

5. <span data-ttu-id="e9a1a-140">输入或选择一个 **休假应计日期**。</span><span class="sxs-lookup"><span data-stu-id="e9a1a-140">Enter or select a **Leave accrual date**.</span></span> <span data-ttu-id="e9a1a-141">这个日期必须是当天或在将来。</span><span class="sxs-lookup"><span data-stu-id="e9a1a-141">This date has to be either today or in the future.</span></span> 

6. <span data-ttu-id="e9a1a-142">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="e9a1a-142">Select **OK**.</span></span> <span data-ttu-id="e9a1a-143">累积流程将使用您设置的参数删除累积。</span><span class="sxs-lookup"><span data-stu-id="e9a1a-143">The accrual process will delete accruals with the parameters you set.</span></span> 

## <a name="delete-leave-and-absence-accruals-for-a-single-employee"></a><span data-ttu-id="e9a1a-144">删除一个员工的休假和缺勤累积</span><span class="sxs-lookup"><span data-stu-id="e9a1a-144">Delete leave and absence accruals for a single employee</span></span>

1. <span data-ttu-id="e9a1a-145">在员工的记录上，选择 **休假**。</span><span class="sxs-lookup"><span data-stu-id="e9a1a-145">On the employee's record, select **Leave**.</span></span>

2. <span data-ttu-id="e9a1a-146">选择 **删除休假和缺勤计划应计项目**。</span><span class="sxs-lookup"><span data-stu-id="e9a1a-146">Select **Delete leave and absence plan accruals**.</span></span>

3. <span data-ttu-id="e9a1a-147">在 **删除休假和缺勤计划应计项目** 对话框中，选择 **休假计划**。</span><span class="sxs-lookup"><span data-stu-id="e9a1a-147">In the **Delete leave and absence plan accruals** dialog box, select **Leave plan**.</span></span> 

4. <span data-ttu-id="e9a1a-148">如果适合，选择 **删除余额调整**。</span><span class="sxs-lookup"><span data-stu-id="e9a1a-148">If applicable, choose **Delete balance adjustments**.</span></span>

5. <span data-ttu-id="e9a1a-149">输入或选择一个 **休假应计日期**。</span><span class="sxs-lookup"><span data-stu-id="e9a1a-149">Enter or select a **Leave accrual date**.</span></span> <span data-ttu-id="e9a1a-150">这个日期必须是当天或在将来。</span><span class="sxs-lookup"><span data-stu-id="e9a1a-150">This date must be either today or in the future.</span></span> 

6. <span data-ttu-id="e9a1a-151">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="e9a1a-151">Select **OK**.</span></span> <span data-ttu-id="e9a1a-152">累积流程将使用您设置的参数删除累积。</span><span class="sxs-lookup"><span data-stu-id="e9a1a-152">The accrual process will delete accruals with the parameters you set.</span></span> 

## <a name="review-leave-accrual-and-deletion-processes"></a><span data-ttu-id="e9a1a-153">检查休假累积和删除流程</span><span class="sxs-lookup"><span data-stu-id="e9a1a-153">Review leave accrual and deletion processes</span></span>

<span data-ttu-id="e9a1a-154">每次运行或删除一个或多个员工的累积时，都将显示 **休假累积审核**。</span><span class="sxs-lookup"><span data-stu-id="e9a1a-154">**Leave accrual audit** displays each time you run or delete an accrual for one or all employees.</span></span> <span data-ttu-id="e9a1a-155">还将显示执行操作的日期和人员。</span><span class="sxs-lookup"><span data-stu-id="e9a1a-155">The date and person who performed the action also displays.</span></span>

1. <span data-ttu-id="e9a1a-156">在 **休假和缺勤** 页面，选择 **链接** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="e9a1a-156">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="e9a1a-157">在 **管理休假** 下，选择 **删除休假累积审核**。</span><span class="sxs-lookup"><span data-stu-id="e9a1a-157">Under **Manage leave**, select **Delete leave accrual audit**.</span></span>

## <a name="see-also"></a><span data-ttu-id="e9a1a-158">请参阅</span><span class="sxs-lookup"><span data-stu-id="e9a1a-158">See also</span></span>

[<span data-ttu-id="e9a1a-159">休假和缺勤概览</span><span class="sxs-lookup"><span data-stu-id="e9a1a-159">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)</br>
[<span data-ttu-id="e9a1a-160">创建休假和缺勤计划</span><span class="sxs-lookup"><span data-stu-id="e9a1a-160">Create a leave and absence plan</span></span>](hr-leave-and-absence-plans.md)
