---
title: 定义周期盘点
description: 周期盘点是用于审计现有库存项目的仓库流程。
author: MarkusFogelberg
manager: AnnBe
ms.date: 06/23/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2832547f81b0153d42ac4664184f18bd66f1acdd
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/29/2019
ms.locfileid: "337294"
---
# <a name="define-cycle-counting"></a><span data-ttu-id="84f8d-103">定义周期盘点</span><span class="sxs-lookup"><span data-stu-id="84f8d-103">Define cycle counting</span></span> 

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="84f8d-104">周期盘点是用于审计现有库存项目的仓库流程。</span><span class="sxs-lookup"><span data-stu-id="84f8d-104">Cycle counting is a warehouse process that you can use to audit on-hand inventory items.</span></span> <span data-ttu-id="84f8d-105">该任务录制说明如何设置默认盘点工作优先级，如何启用移动设备菜单项处理选料和盘点操作，库位空置后如何启用盘点阀值触发器，以及如何在特定仓库中启用周期盘点计划。</span><span class="sxs-lookup"><span data-stu-id="84f8d-105">This task recording shows how to set up the default counting work priority, enable a mobile device menu item to process both picking and counting operations, enable a counting threshold trigger when a location becomes empty, and enable a cycle counting plan for a specific item in a specific warehouse.</span></span> <span data-ttu-id="84f8d-106">这些任务通常由仓库管理员执行。</span><span class="sxs-lookup"><span data-stu-id="84f8d-106">Typically, these tasks are performed by a warehouse manager.</span></span> <span data-ttu-id="84f8d-107">您可以在 USMF 演示数据公司或您自己的数据中了解该过程。</span><span class="sxs-lookup"><span data-stu-id="84f8d-107">You can go through this procedure in the USMF demo data company or in your own data.</span></span>


## <a name="set-the-priority-of-counting-work"></a><span data-ttu-id="84f8d-108">设置盘点工作优先级</span><span class="sxs-lookup"><span data-stu-id="84f8d-108">Set the priority of counting work</span></span>
1. <span data-ttu-id="84f8d-109">转到“仓库管理”>“设置”>“仓库管理参数”。</span><span class="sxs-lookup"><span data-stu-id="84f8d-109">Go to Warehouse management > Setup > Warehouse management parameters.</span></span>
2. <span data-ttu-id="84f8d-110">单击“周期盘点”选项卡。</span><span class="sxs-lookup"><span data-stu-id="84f8d-110">Click the Cycle counting tab.</span></span>
3. <span data-ttu-id="84f8d-111">在“默认周期盘点作业优先级”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="84f8d-111">In the Default cycle count work priority field, enter a number.</span></span>
    * <span data-ttu-id="84f8d-112">此步骤更改周期盘点工作相对窗口中其他工作类型的优先级。</span><span class="sxs-lookup"><span data-stu-id="84f8d-112">This step changes the priority of cycle counting work compared to other types of work in the warehouse.</span></span> <span data-ttu-id="84f8d-113">通过输入小于其他工作类型数量的数字，提升周期盘点作业的优先级。</span><span class="sxs-lookup"><span data-stu-id="84f8d-113">By entering a number that is lower than the number for other types of work, you raise the priority of the cycle counting work.</span></span>  
4. <span data-ttu-id="84f8d-114">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="84f8d-114">Click Save.</span></span>
5. <span data-ttu-id="84f8d-115">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="84f8d-115">Close the page.</span></span>

## <a name="enable-the-mobile-device"></a><span data-ttu-id="84f8d-116">启用移动设备</span><span class="sxs-lookup"><span data-stu-id="84f8d-116">Enable the mobile device</span></span>
1. <span data-ttu-id="84f8d-117">转到“仓库管理”>“设置”>“移动设备”>“移动设备菜单项”。</span><span class="sxs-lookup"><span data-stu-id="84f8d-117">Go to Warehouse management > Setup > Mobile device > Mobile device menu items.</span></span>
2. <span data-ttu-id="84f8d-118">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="84f8d-118">Click New.</span></span>
3. <span data-ttu-id="84f8d-119">在“菜单项名称”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="84f8d-119">In the Menu item name field, type a value.</span></span>
4. <span data-ttu-id="84f8d-120">在“标题”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="84f8d-120">In the Title field, type a value.</span></span>
5. <span data-ttu-id="84f8d-121">在“模式”字段中，选择“工作”。</span><span class="sxs-lookup"><span data-stu-id="84f8d-121">In the Mode field, select 'Work'.</span></span>
6. <span data-ttu-id="84f8d-122">将“使用现有工作”选项设置为“是”。</span><span class="sxs-lookup"><span data-stu-id="84f8d-122">Set the Use existing work option to Yes.</span></span>
    * <span data-ttu-id="84f8d-123">如果将此选项设置为“是”，使用移动设备菜单项时，系统将查找现有的作业。</span><span class="sxs-lookup"><span data-stu-id="84f8d-123">When you set this option to Yes, the system will look for existing work when the mobile device menu item is used.</span></span>  
7. <span data-ttu-id="84f8d-124">在“指导”字段中，选择“系统指导”。</span><span class="sxs-lookup"><span data-stu-id="84f8d-124">In the Directed by field, select 'System directed'.</span></span>
    * <span data-ttu-id="84f8d-125">如果选择“系统导向的”，将指示仓库工作人员打开定义的工作类中的工作。</span><span class="sxs-lookup"><span data-stu-id="84f8d-125">When "System directed" is selected, the warehouse worker will be directed to open work that is in defined work classes.</span></span> <span data-ttu-id="84f8d-126">（接下来将创建这些工作类。）</span><span class="sxs-lookup"><span data-stu-id="84f8d-126">(We will create these work classes next.)</span></span>  
8. <span data-ttu-id="84f8d-127">展开或折叠“工作类”部分。</span><span class="sxs-lookup"><span data-stu-id="84f8d-127">Expand or collapse the Work classes section.</span></span>
    * <span data-ttu-id="84f8d-128">接下来将创建两个与该移动设备菜单项一起使用的工作类。</span><span class="sxs-lookup"><span data-stu-id="84f8d-128">Next, we will create two work classes that will be used with this mobile device menu item.</span></span> <span data-ttu-id="84f8d-129">在使用菜单项的同时，对这些工作类别进行查询，并向用户显示具有最高优先级的工作。</span><span class="sxs-lookup"><span data-stu-id="84f8d-129">When the menu item is used, these work classes will be queried, and the work that has the highest priority will be shown to the user.</span></span>  
9. <span data-ttu-id="84f8d-130">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="84f8d-130">Click New.</span></span>
10. <span data-ttu-id="84f8d-131">在“工作类别 ID”字段中，选择一个值。</span><span class="sxs-lookup"><span data-stu-id="84f8d-131">In the Work class ID field, select a value.</span></span>
11. <span data-ttu-id="84f8d-132">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="84f8d-132">Click New.</span></span>
12. <span data-ttu-id="84f8d-133">在“工作类别 ID”字段中，选择一个值。</span><span class="sxs-lookup"><span data-stu-id="84f8d-133">In the Work class ID field, select a value.</span></span>
13. <span data-ttu-id="84f8d-134">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="84f8d-134">Click Save.</span></span>
14. <span data-ttu-id="84f8d-135">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="84f8d-135">Close the page.</span></span>
15. <span data-ttu-id="84f8d-136">转到“仓库管理”>“设置”>“设置”>“移动设备菜单”。</span><span class="sxs-lookup"><span data-stu-id="84f8d-136">Go to Warehouse management > Setup > Mobile device > Mobile device menu.</span></span>
16. <span data-ttu-id="84f8d-137">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="84f8d-137">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="84f8d-138">在树中，选择您刚才创建的菜单项。</span><span class="sxs-lookup"><span data-stu-id="84f8d-138">In the tree, select 'the menu item that you just created'.</span></span>
18. <span data-ttu-id="84f8d-139">单击“编辑”。</span><span class="sxs-lookup"><span data-stu-id="84f8d-139">Click Edit.</span></span>
19. <span data-ttu-id="84f8d-140">单击箭头以将该菜单项添加到菜单中。</span><span class="sxs-lookup"><span data-stu-id="84f8d-140">Click the arrow to add the menu item to the menu.</span></span>
20. <span data-ttu-id="84f8d-141">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="84f8d-141">Click Save.</span></span>

## <a name="create-a-counting-threshold"></a><span data-ttu-id="84f8d-142">创建盘点阈值</span><span class="sxs-lookup"><span data-stu-id="84f8d-142">Create a counting threshold</span></span>
1. <span data-ttu-id="84f8d-143">转到“仓库管理”>“设置”>“周期盘点”>“周期盘点阈值”。</span><span class="sxs-lookup"><span data-stu-id="84f8d-143">Go to Warehouse management > Setup > Cycle counting > Cycle count thresholds.</span></span>
2. <span data-ttu-id="84f8d-144">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="84f8d-144">Click New.</span></span>
3. <span data-ttu-id="84f8d-145">在“周期盘点阈值 ID ”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="84f8d-145">In the Cycle counting threshold ID field, type a value.</span></span>
4. <span data-ttu-id="84f8d-146">设置“立即进行周期盘点”选项为“是”。</span><span class="sxs-lookup"><span data-stu-id="84f8d-146">Set the Process cycle counting immediately option to Yes.</span></span>
5. <span data-ttu-id="84f8d-147">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="84f8d-147">In the Description field, type a value.</span></span>
6. <span data-ttu-id="84f8d-148">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="84f8d-148">Click Save.</span></span>
7. <span data-ttu-id="84f8d-149">单击“选择库位”。</span><span class="sxs-lookup"><span data-stu-id="84f8d-149">Click Select locations.</span></span>
8. <span data-ttu-id="84f8d-150">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="84f8d-150">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="84f8d-151">在“条件”字段中，选择一个值。</span><span class="sxs-lookup"><span data-stu-id="84f8d-151">In the Criteria field, select a value.</span></span>
10. <span data-ttu-id="84f8d-152">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="84f8d-152">Click OK.</span></span>
11. <span data-ttu-id="84f8d-153">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="84f8d-153">Close the page.</span></span>

## <a name="create-a-cycle-count-plan"></a><span data-ttu-id="84f8d-154">创建周期盘点计划</span><span class="sxs-lookup"><span data-stu-id="84f8d-154">Create a cycle count plan</span></span>
1. <span data-ttu-id="84f8d-155">转到“仓库管理”>“设置”>“周期盘点”>“周期盘点计划”。</span><span class="sxs-lookup"><span data-stu-id="84f8d-155">Go to Warehouse management > Setup > Cycle counting > Cycle count plans.</span></span>
2. <span data-ttu-id="84f8d-156">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="84f8d-156">Click New.</span></span>
3. <span data-ttu-id="84f8d-157">在“周期盘点计划 ID ”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="84f8d-157">In the Cycle counting plan ID field, type a value.</span></span>
4. <span data-ttu-id="84f8d-158">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="84f8d-158">In the Description field, type a value.</span></span>
5. <span data-ttu-id="84f8d-159">在“周期盘点最大数”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="84f8d-159">In the Maximum number of cycle counts field, enter a number.</span></span>
6. <span data-ttu-id="84f8d-160">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="84f8d-160">Click Save.</span></span>
7. <span data-ttu-id="84f8d-161">单击“选择库位”。</span><span class="sxs-lookup"><span data-stu-id="84f8d-161">Click Select locations.</span></span>
8. <span data-ttu-id="84f8d-162">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="84f8d-162">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="84f8d-163">在“条件”字段中，选择一个值。</span><span class="sxs-lookup"><span data-stu-id="84f8d-163">In the Criteria field, select a value.</span></span>
10. <span data-ttu-id="84f8d-164">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="84f8d-164">Click OK.</span></span>
11. <span data-ttu-id="84f8d-165">在“周期盘点天数”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="84f8d-165">In the Days between cycle counting field, enter a number.</span></span>
    * <span data-ttu-id="84f8d-166">例如，如果“周期盘点之间的天数”字段设置为 5，则周期盘点作业每五天创建一次。</span><span class="sxs-lookup"><span data-stu-id="84f8d-166">For example, if the Days between cycle counting field is set to 5, cycle counting work will be created every five days.</span></span> <span data-ttu-id="84f8d-167">但是，如果在第三天处理周期盘点工作，则下一个周期盘点工作将在处理完最后的周期盘点之后的第五天被创建，即第八天。</span><span class="sxs-lookup"><span data-stu-id="84f8d-167">However, if cycle counting work is processed on day three, the next cycle counting work will be created five days after the last cycle counting was processed, on day 8.</span></span>  
12. <span data-ttu-id="84f8d-168">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="84f8d-168">Click Save.</span></span>
13. <span data-ttu-id="84f8d-169">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="84f8d-169">Click New.</span></span>
14. <span data-ttu-id="84f8d-170">在“序列号”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="84f8d-170">In the Sequence number field, enter a number.</span></span>
    * <span data-ttu-id="84f8d-171">排序是从最小数字到最大数字。</span><span class="sxs-lookup"><span data-stu-id="84f8d-171">The sort is from the smallest number to the largest number.</span></span> <span data-ttu-id="84f8d-172">值必须大于 0（零）。</span><span class="sxs-lookup"><span data-stu-id="84f8d-172">The value must be more than 0 (zero).</span></span>  
15. <span data-ttu-id="84f8d-173">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="84f8d-173">In the list, mark the selected row.</span></span>
16. <span data-ttu-id="84f8d-174">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="84f8d-174">In the Description field, type a value.</span></span>
17. <span data-ttu-id="84f8d-175">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="84f8d-175">Click Save.</span></span>
18. <span data-ttu-id="84f8d-176">单击“定义产品查询”。</span><span class="sxs-lookup"><span data-stu-id="84f8d-176">Click Define product query.</span></span>
19. <span data-ttu-id="84f8d-177">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="84f8d-177">In the list, mark the selected row.</span></span>
20. <span data-ttu-id="84f8d-178">在“标准”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="84f8d-178">In the Criteria field, enter or select a value.</span></span>
21. <span data-ttu-id="84f8d-179">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="84f8d-179">Click OK.</span></span>
22. <span data-ttu-id="84f8d-180">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="84f8d-180">Close the page.</span></span>

