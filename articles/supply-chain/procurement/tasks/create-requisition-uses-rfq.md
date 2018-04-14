--- 
title: "创建使用询价的申请"
description: "此指南演示如何将价格和供应商信息添加到询价流程的采购申请。"
author: mkirknel
manager: AnnBe
ms.date: 08/25/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 2c2daad961ec5c47ca49b2e53a2118570caf6a58
ms.contentlocale: zh-cn
ms.lasthandoff: 04/13/2018

---
# <a name="create-a-requisition-that-uses-an-rfq"></a><span data-ttu-id="08659-103">创建使用询价的申请</span><span class="sxs-lookup"><span data-stu-id="08659-103">Create a requisition that uses an RFQ</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="08659-104">此指南演示如何将价格和供应商信息添加到询价流程的采购申请。</span><span class="sxs-lookup"><span data-stu-id="08659-104">This guide shows how to add price and vendor information to a purchase requisition from an RFQ process.</span></span> <span data-ttu-id="08659-105">可以在 USMF 演示数据公司中使用此指南中显示的示例，并且必须以 Admin 身份登录才能完成所有任务。</span><span class="sxs-lookup"><span data-stu-id="08659-105">The example shown in this guide can be used in the USMF demo data company, and you must be logged in as an Admin to complete all the steps.</span></span> <span data-ttu-id="08659-106">此指南中的任务通常由采购专业人员完成。</span><span class="sxs-lookup"><span data-stu-id="08659-106">The tasks in this guide would typically be done by procurement professionals.</span></span>


## <a name="create-a-requisition"></a><span data-ttu-id="08659-107">创建申请</span><span class="sxs-lookup"><span data-stu-id="08659-107">Create a requisition</span></span>
1. <span data-ttu-id="08659-108">转到“采购”>“采购申请”>“由我起草的采购申请”。</span><span class="sxs-lookup"><span data-stu-id="08659-108">Go to Procurement and sourcing > Purchase requisitions > Purchase requisitions prepared by me.</span></span>
2. <span data-ttu-id="08659-109">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="08659-109">Click New.</span></span>
3. <span data-ttu-id="08659-110">在“名称”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="08659-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="08659-111">在“请求日期”字段中，输入一个日期。</span><span class="sxs-lookup"><span data-stu-id="08659-111">In the Requested date field, enter a date.</span></span>
5. <span data-ttu-id="08659-112">在“会计结算日期”字段中，输入一个日期。</span><span class="sxs-lookup"><span data-stu-id="08659-112">In the Accounting date field, enter a date.</span></span>
6. <span data-ttu-id="08659-113">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="08659-113">Click OK.</span></span>
7. <span data-ttu-id="08659-114">在“原因”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="08659-114">In the Reason field, enter or select a value.</span></span>
8. <span data-ttu-id="08659-115">单击“添加行”。</span><span class="sxs-lookup"><span data-stu-id="08659-115">Click Add line.</span></span>
9. <span data-ttu-id="08659-116">在“采购类别”字段中，选择树中的类别，然后单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="08659-116">In the Procurement category field, select a category in the tree, and then click OK.</span></span>
10. <span data-ttu-id="08659-117">在“产品名称”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="08659-117">In the Product name field, type a value.</span></span>
11. <span data-ttu-id="08659-118">在“数量”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="08659-118">In the Quantity field, enter a number.</span></span>
12. <span data-ttu-id="08659-119">在“单位”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="08659-119">In the Unit field, enter or select a value.</span></span>
13. <span data-ttu-id="08659-120">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="08659-120">Click Save.</span></span>
14. <span data-ttu-id="08659-121">单击“工作流程”以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="08659-121">Click Workflow to open the drop dialog.</span></span>
15. <span data-ttu-id="08659-122">单击“提交”。</span><span class="sxs-lookup"><span data-stu-id="08659-122">Click Submit.</span></span>
16. <span data-ttu-id="08659-123">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="08659-123">Close the page.</span></span>
17. <span data-ttu-id="08659-124">单击“提交”。</span><span class="sxs-lookup"><span data-stu-id="08659-124">Click Submit.</span></span>

## <a name="reassign-a-workflow-task"></a><span data-ttu-id="08659-125">为工作流重新分配任务</span><span class="sxs-lookup"><span data-stu-id="08659-125">Reassign a workflow task</span></span>
    * <span data-ttu-id="08659-126">下一项任务是创建询价以获取供应商对产品的出价。</span><span class="sxs-lookup"><span data-stu-id="08659-126">The next task is to create an RFQ to get bids from vendors for the product.</span></span> <span data-ttu-id="08659-127">在 USMF 演示数据中，为申请工作流设置了规则，以便在未选择供应商或某行的单价为 0 时，为特定工作人员分配任务以创建询价。</span><span class="sxs-lookup"><span data-stu-id="08659-127">In USMF demo data, the requisition workflow is set up with a rule so that if a vendor is not selected, or the unit price is 0 for a line, a task is assigned to a specific worker to create an RFQ.</span></span> <span data-ttu-id="08659-128">要继续完成此指南，需要将该任务重新分配给其他用户（您自己）。</span><span class="sxs-lookup"><span data-stu-id="08659-128">To continue with this guide, you need to re-assign that task to another user (yourself).</span></span> <span data-ttu-id="08659-129">仅当您以 Admin 身份登录时，才能执行此操作。</span><span class="sxs-lookup"><span data-stu-id="08659-129">You can only do this if you are logged in as an Admin.</span></span>  
1. <span data-ttu-id="08659-130">单击“工作流程”以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="08659-130">Click Workflow to open the drop dialog.</span></span>
2. <span data-ttu-id="08659-131">单击“查看历史记录”。</span><span class="sxs-lookup"><span data-stu-id="08659-131">Click View history.</span></span>
3. <span data-ttu-id="08659-132">刷新该页面。</span><span class="sxs-lookup"><span data-stu-id="08659-132">Refresh the page.</span></span>
4. <span data-ttu-id="08659-133">展开“跟踪详细信息”部分。</span><span class="sxs-lookup"><span data-stu-id="08659-133">Expand the Tracking details section.</span></span>
5. <span data-ttu-id="08659-134">在树中，请选择以“行工作流启用于”开始的行。</span><span class="sxs-lookup"><span data-stu-id="08659-134">In the tree, select 'the line that starts with “Line workflow activated on”'.</span></span>
6. <span data-ttu-id="08659-135">单击“查看工作流详细信息”。</span><span class="sxs-lookup"><span data-stu-id="08659-135">Click View workflow details.</span></span>
7. <span data-ttu-id="08659-136">展开“工作项”部分。</span><span class="sxs-lookup"><span data-stu-id="08659-136">Expand the Work items section.</span></span>
8. <span data-ttu-id="08659-137">单击“重新分配”。</span><span class="sxs-lookup"><span data-stu-id="08659-137">Click Reassign.</span></span>
9. <span data-ttu-id="08659-138">在“用户”字段中，选择“Admin”。</span><span class="sxs-lookup"><span data-stu-id="08659-138">In the User field, select Admin.</span></span>
10. <span data-ttu-id="08659-139">单击“重新分配”。</span><span class="sxs-lookup"><span data-stu-id="08659-139">Click Reassign.</span></span>
11. <span data-ttu-id="08659-140">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="08659-140">Close the page.</span></span>
12. <span data-ttu-id="08659-141">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="08659-141">Close the page.</span></span>

## <a name="create-an-rfq"></a><span data-ttu-id="08659-142">创建询价</span><span class="sxs-lookup"><span data-stu-id="08659-142">Create an RFQ</span></span>
1. <span data-ttu-id="08659-143">刷新该页面。</span><span class="sxs-lookup"><span data-stu-id="08659-143">Refresh the page.</span></span>
2. <span data-ttu-id="08659-144">单击“询价”。</span><span class="sxs-lookup"><span data-stu-id="08659-144">Click Request for quotation.</span></span>
3. <span data-ttu-id="08659-145">在“购买法人”字段中，选择 USMF。</span><span class="sxs-lookup"><span data-stu-id="08659-145">In the Buying legal entity field, select USMF.</span></span>
    * <span data-ttu-id="08659-146">必须选择位于申请行中的同一个法人。</span><span class="sxs-lookup"><span data-stu-id="08659-146">You must select the same legal entity that’s on the requisition line.</span></span>  
4. <span data-ttu-id="08659-147">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="08659-147">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="08659-148">如果采购申请中有多行，请选择要添加到询价的所有行。</span><span class="sxs-lookup"><span data-stu-id="08659-148">If you had multiple lines on your purchase requisition, select all the lines that you want to add to the RFQ.</span></span>  
5. <span data-ttu-id="08659-149">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="08659-149">Click OK.</span></span>
6. <span data-ttu-id="08659-150">刷新该页面。</span><span class="sxs-lookup"><span data-stu-id="08659-150">Refresh the page.</span></span>
7. <span data-ttu-id="08659-151">打开速见表，然后展开“相关单据”部分。</span><span class="sxs-lookup"><span data-stu-id="08659-151">Open the FactBox and then expand the Related documents section.</span></span>
    * <span data-ttu-id="08659-152">您可能已经打开了该速见表。</span><span class="sxs-lookup"><span data-stu-id="08659-152">You may already have the FactBox open.</span></span> <span data-ttu-id="08659-153">在“行/标题”切换按钮右侧找到带箭头的图标。</span><span class="sxs-lookup"><span data-stu-id="08659-153">Look for the icon with an arrow on it, to the right of the Lines/Header toggle buttons.</span></span> <span data-ttu-id="08659-154">如果箭头指向右侧，说明速见表已打开。</span><span class="sxs-lookup"><span data-stu-id="08659-154">If the arrow is pointing to the right, the FactBox is already open.</span></span> <span data-ttu-id="08659-155">如果箭头指向左侧，请单击该箭头打开速见表。</span><span class="sxs-lookup"><span data-stu-id="08659-155">If the arrow points to the left, click it to open the FactBox.</span></span>  
8. <span data-ttu-id="08659-156">单击“询价”字段中的链接打开刚才创建的询价。</span><span class="sxs-lookup"><span data-stu-id="08659-156">Click the link in the Request for quotation field to open the RFQ that was just created.</span></span>
9. <span data-ttu-id="08659-157">单击“单头”。</span><span class="sxs-lookup"><span data-stu-id="08659-157">Click Header.</span></span>
10. <span data-ttu-id="08659-158">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="08659-158">Click Add.</span></span>
11. <span data-ttu-id="08659-159">在“供应商帐户”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="08659-159">In the Vendor account field, enter or select a value.</span></span>
12. <span data-ttu-id="08659-160">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="08659-160">Click Add.</span></span>
13. <span data-ttu-id="08659-161">在“供应商帐户”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="08659-161">In the Vendor account field, enter or select a value.</span></span>
14. <span data-ttu-id="08659-162">单击“发送”。</span><span class="sxs-lookup"><span data-stu-id="08659-162">Click Send.</span></span>
15. <span data-ttu-id="08659-163">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="08659-163">Click OK.</span></span>
16. <span data-ttu-id="08659-164">单击“输入回复”。</span><span class="sxs-lookup"><span data-stu-id="08659-164">Click Enter reply.</span></span>
17. <span data-ttu-id="08659-165">在“操作”窗格上，单击“回复”。</span><span class="sxs-lookup"><span data-stu-id="08659-165">On the Action Pane, click Reply.</span></span>
18. <span data-ttu-id="08659-166">单击“将数据复制到回复”。</span><span class="sxs-lookup"><span data-stu-id="08659-166">Click Copy data to reply.</span></span>
    * <span data-ttu-id="08659-167">这将把数量和日期之类数据从询价复制到回复。</span><span class="sxs-lookup"><span data-stu-id="08659-167">This copies data, such as the quantity and dates, from the RFQ to the reply .</span></span>  
19. <span data-ttu-id="08659-168">在“单位价格”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="08659-168">In the Unit price field, enter a number.</span></span>
    * <span data-ttu-id="08659-169">这是您从供应商处收到的价格。</span><span class="sxs-lookup"><span data-stu-id="08659-169">This is the price that you’ve received from the vendor.</span></span> <span data-ttu-id="08659-170">您可能还希望输入供应商提供的其他信息。</span><span class="sxs-lookup"><span data-stu-id="08659-170">You might also want to enter additional information from the vendor.</span></span>  
20. <span data-ttu-id="08659-171">单击“接受”。</span><span class="sxs-lookup"><span data-stu-id="08659-171">Click Accept.</span></span>
21. <span data-ttu-id="08659-172">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="08659-172">Click OK.</span></span>

## <a name="verify-that-vendor-and-price-have-been-transferred-to-the-requisition"></a><span data-ttu-id="08659-173">验证是否已将供应商和价格转移到申请</span><span class="sxs-lookup"><span data-stu-id="08659-173">Verify that vendor and price have been transferred to the requisition</span></span>
1. <span data-ttu-id="08659-174">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="08659-174">Close the page.</span></span>
2. <span data-ttu-id="08659-175">单击“行”。</span><span class="sxs-lookup"><span data-stu-id="08659-175">Click Lines.</span></span>
3. <span data-ttu-id="08659-176">单击“相关信息”。</span><span class="sxs-lookup"><span data-stu-id="08659-176">Click Related information.</span></span>
4. <span data-ttu-id="08659-177">单击“采购申请”。</span><span class="sxs-lookup"><span data-stu-id="08659-177">Click Purchase requisition.</span></span>
5. <span data-ttu-id="08659-178">选择已转移到询价的行。</span><span class="sxs-lookup"><span data-stu-id="08659-178">Select the line that was transferred to the RFQ.</span></span>
    * <span data-ttu-id="08659-179">验证是否已将价格和供应商复制到申请。</span><span class="sxs-lookup"><span data-stu-id="08659-179">Verify that the price and vendor have been copied to the requisition.</span></span>  
6. <span data-ttu-id="08659-180">单击“工作流程”以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="08659-180">Click Workflow to open the drop dialog.</span></span>
7. <span data-ttu-id="08659-181">单击“完成”。</span><span class="sxs-lookup"><span data-stu-id="08659-181">Click Complete.</span></span>
8. <span data-ttu-id="08659-182">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="08659-182">Close the page.</span></span>
9. <span data-ttu-id="08659-183">单击“完成”。</span><span class="sxs-lookup"><span data-stu-id="08659-183">Click Complete.</span></span>


