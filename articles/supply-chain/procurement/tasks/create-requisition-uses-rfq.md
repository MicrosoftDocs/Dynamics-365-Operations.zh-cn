---
title: 创建使用询价的申请
description: 此主题介绍如何将价格和供应商信息添加到询价流程的采购申请。
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchReqTableListPage, PurchReqCreate, PurchReqTable, PurchReqLineRelatedDocuments, EcoResCategorySingleLookup, PurchReqWorkflowDropDialog, WorkflowSubmitDialog, WorkflowStatus, WorkflowWorkItemActionDialog, WorkflowUserListLookup, PurchReqCopyRFQ, SysDataAreaSelectLookup, PurchRFQCaseTable, PurchRFQEditLines, PurchRFQReplyTable, UnitOfMeasureLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4429bda6efddbb4f1fa7da06e91e51d885919c05
ms.sourcegitcommit: e10491a2ff04f65d9f306ef6e068ee123213b23b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/21/2019
ms.locfileid: "1914946"
---
# <a name="create-a-requisition-that-uses-an-rfq"></a><span data-ttu-id="136aa-103">创建使用询价的申请</span><span class="sxs-lookup"><span data-stu-id="136aa-103">Create a requisition that uses an RFQ</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="136aa-104">此主题介绍如何将价格和供应商信息添加到询价流程的采购申请。</span><span class="sxs-lookup"><span data-stu-id="136aa-104">This topic explains how to add price and vendor information to a purchase requisition from an RFQ process.</span></span> <span data-ttu-id="136aa-105">可以在 USMF 演示数据公司中使用此指南中显示的示例，并且必须以 Admin 身份登录才能完成所有任务。</span><span class="sxs-lookup"><span data-stu-id="136aa-105">The example shown in this guide can be used in the USMF demo data company, and you must be logged in as an Admin to complete all the steps.</span></span> <span data-ttu-id="136aa-106">此指南中的任务通常由采购专业人员完成。</span><span class="sxs-lookup"><span data-stu-id="136aa-106">The tasks in this guide would typically be done by procurement professionals.</span></span>


## <a name="create-a-requisition"></a><span data-ttu-id="136aa-107">创建申请</span><span class="sxs-lookup"><span data-stu-id="136aa-107">Create a requisition</span></span>
1. <span data-ttu-id="136aa-108">在导航窗格中，转到**模块 > 采购 > 采购申请 > 由我准备的采购申请**。</span><span class="sxs-lookup"><span data-stu-id="136aa-108">In the navigation pane, go to **Modules > Procurement and sourcing > Purchase requisitions > Purchase requisitions prepared by me**.</span></span>
2. <span data-ttu-id="136aa-109">选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="136aa-109">Select **New**.</span></span>
3. <span data-ttu-id="136aa-110">在**名称**字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="136aa-110">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="136aa-111">在**请求日期**字段中，输入一个日期。</span><span class="sxs-lookup"><span data-stu-id="136aa-111">In the **Requested date** field, enter a date.</span></span>
5. <span data-ttu-id="136aa-112">在**会计结算日期**字段中，输入一个日期。</span><span class="sxs-lookup"><span data-stu-id="136aa-112">In the **Accounting date** field, enter a date.</span></span>
6. <span data-ttu-id="136aa-113">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="136aa-113">Select **OK**.</span></span>
7. <span data-ttu-id="136aa-114">在**原因**字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="136aa-114">In the **Reason** field, enter or select a value.</span></span>
8. <span data-ttu-id="136aa-115">选择**添加行**。</span><span class="sxs-lookup"><span data-stu-id="136aa-115">Select **Add line**.</span></span>
9. <span data-ttu-id="136aa-116">在**采购类别**字段中，选择树中的类别，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="136aa-116">In the **Procurement category** field, select a category in the tree, and then select **OK**.</span></span>
10. <span data-ttu-id="136aa-117">在**产品名称**字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="136aa-117">In the **Product name** field, type a value.</span></span>
11. <span data-ttu-id="136aa-118">在**数量**字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="136aa-118">In the **Quantity** field, enter a number.</span></span>
12. <span data-ttu-id="136aa-119">在**单位**字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="136aa-119">In the **Unit** field, enter or select a value.</span></span>
13. <span data-ttu-id="136aa-120">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="136aa-120">Select **Save**.</span></span>
14. <span data-ttu-id="136aa-121">选择**工作流**以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="136aa-121">Select **Workflow** to open the drop dialog.</span></span>
15. <span data-ttu-id="136aa-122">选择**提交**。</span><span class="sxs-lookup"><span data-stu-id="136aa-122">Select **Submit**.</span></span>
16. <span data-ttu-id="136aa-123">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="136aa-123">Close the page.</span></span>
17. <span data-ttu-id="136aa-124">选择**提交**。</span><span class="sxs-lookup"><span data-stu-id="136aa-124">Select **Submit**.</span></span>

## <a name="reassign-a-workflow-task"></a><span data-ttu-id="136aa-125">为工作流重新分配任务</span><span class="sxs-lookup"><span data-stu-id="136aa-125">Reassign a workflow task</span></span>
<span data-ttu-id="136aa-126">下一项任务是创建询价以获取供应商对产品的出价。</span><span class="sxs-lookup"><span data-stu-id="136aa-126">The next task is to create an RFQ to get bids from vendors for the product.</span></span> <span data-ttu-id="136aa-127">在 USMF 演示数据中，为申请工作流设置了规则，以便在未选择供应商或某行的单价为 0 时，为特定工作人员分配任务以创建询价。</span><span class="sxs-lookup"><span data-stu-id="136aa-127">In USMF demo data, the requisition workflow is set up with a rule so that if a vendor is not selected, or the unit price is 0 for a line, a task is assigned to a specific worker to create an RFQ.</span></span> <span data-ttu-id="136aa-128">要继续完成此指南，需要将该任务重新分配给其他用户（您自己）。</span><span class="sxs-lookup"><span data-stu-id="136aa-128">To continue with this guide, you need to re-assign that task to another user (yourself).</span></span> <span data-ttu-id="136aa-129">仅当您以 Admin 身份登录时，才能执行此操作。</span><span class="sxs-lookup"><span data-stu-id="136aa-129">You can only do this if you are logged in as an Admin.</span></span>  

1. <span data-ttu-id="136aa-130">选择**工作流**以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="136aa-130">Select **Workflow** to open the drop dialog.</span></span>
2. <span data-ttu-id="136aa-131">选择**查看历史记录**。</span><span class="sxs-lookup"><span data-stu-id="136aa-131">Select **View history**.</span></span>
3. <span data-ttu-id="136aa-132">刷新该页面。</span><span class="sxs-lookup"><span data-stu-id="136aa-132">Refresh the page.</span></span>
4. <span data-ttu-id="136aa-133">展开**跟踪详细信息**部分。</span><span class="sxs-lookup"><span data-stu-id="136aa-133">Expand the **Tracking details** section.</span></span>
5. <span data-ttu-id="136aa-134">在树中，请选择以“行工作流启用于”开始的行。</span><span class="sxs-lookup"><span data-stu-id="136aa-134">In the tree, select the line that starts with “Line workflow activated on”.</span></span>
6. <span data-ttu-id="136aa-135">选择**查看工作流详细信息**。</span><span class="sxs-lookup"><span data-stu-id="136aa-135">Select **View workflow details**.</span></span>
7. <span data-ttu-id="136aa-136">展开**工作项**部分。</span><span class="sxs-lookup"><span data-stu-id="136aa-136">Expand the **Work items** section.</span></span>
8. <span data-ttu-id="136aa-137">选择**重新分配**。</span><span class="sxs-lookup"><span data-stu-id="136aa-137">Select **Reassign**.</span></span>
9. <span data-ttu-id="136aa-138">在**用户**字段中，选择 **Admin**。</span><span class="sxs-lookup"><span data-stu-id="136aa-138">In the **User** field, select **Admin**.</span></span>
10. <span data-ttu-id="136aa-139">选择**重新分配**。</span><span class="sxs-lookup"><span data-stu-id="136aa-139">Select **Reassign**.</span></span>
11. <span data-ttu-id="136aa-140">关闭这两个页面。</span><span class="sxs-lookup"><span data-stu-id="136aa-140">Close the two pages.</span></span>

## <a name="create-an-rfq"></a><span data-ttu-id="136aa-141">创建询价</span><span class="sxs-lookup"><span data-stu-id="136aa-141">Create an RFQ</span></span>

1. <span data-ttu-id="136aa-142">刷新该页面。</span><span class="sxs-lookup"><span data-stu-id="136aa-142">Refresh the page.</span></span>
2. <span data-ttu-id="136aa-143">选择**询价**。</span><span class="sxs-lookup"><span data-stu-id="136aa-143">Select **Request for quotation**.</span></span>
3. <span data-ttu-id="136aa-144">在**购买法人**字段中，选择 **USMF**。</span><span class="sxs-lookup"><span data-stu-id="136aa-144">In the **Buying legal entity** field, select **USMF**.</span></span> <span data-ttu-id="136aa-145">必须选择位于申请行中的同一个法人。</span><span class="sxs-lookup"><span data-stu-id="136aa-145">You must select the same legal entity that’s on the requisition line.</span></span>  
4. <span data-ttu-id="136aa-146">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="136aa-146">In the list, mark the selected row.</span></span> <span data-ttu-id="136aa-147">如果采购申请中有多行，请选择要添加到询价的所有行。</span><span class="sxs-lookup"><span data-stu-id="136aa-147">If you had multiple lines on your purchase requisition, select all the lines that you want to add to the RFQ.</span></span>  
5. <span data-ttu-id="136aa-148">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="136aa-148">Select **OK**.</span></span>
6. <span data-ttu-id="136aa-149">刷新该页面。</span><span class="sxs-lookup"><span data-stu-id="136aa-149">Refresh the page.</span></span>
7. <span data-ttu-id="136aa-150">确保此速见表已打开，然后展开**相关单据**部分。</span><span class="sxs-lookup"><span data-stu-id="136aa-150">Ensure that the FactBox is open, then expand the **Related documents** section.</span></span>
8. <span data-ttu-id="136aa-151">选择**询价**字段中的链接打开刚才创建的询价。</span><span class="sxs-lookup"><span data-stu-id="136aa-151">Select the link in the **Request for quotation** field to open the RFQ that was just created.</span></span>
9. <span data-ttu-id="136aa-152">选择**标题**。</span><span class="sxs-lookup"><span data-stu-id="136aa-152">Select **Header**.</span></span>
10. <span data-ttu-id="136aa-153">选择**添加**。</span><span class="sxs-lookup"><span data-stu-id="136aa-153">Select **Add**.</span></span>
11. <span data-ttu-id="136aa-154">在**供应商帐户**字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="136aa-154">In the **Vendor account** field, enter or select a value.</span></span>
12. <span data-ttu-id="136aa-155">选择**添加**。</span><span class="sxs-lookup"><span data-stu-id="136aa-155">Select **Add**.</span></span>
13. <span data-ttu-id="136aa-156">在**供应商帐户**字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="136aa-156">In the **Vendor account** field, enter or select a value.</span></span>
14. <span data-ttu-id="136aa-157">选择**发送**。</span><span class="sxs-lookup"><span data-stu-id="136aa-157">Select **Send**.</span></span>
15. <span data-ttu-id="136aa-158">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="136aa-158">Select **OK**.</span></span>
16. <span data-ttu-id="136aa-159">选择**输入回复**。</span><span class="sxs-lookup"><span data-stu-id="136aa-159">Select **Enter reply**.</span></span>
17. <span data-ttu-id="136aa-160">在操作窗格上，选择**回复**。</span><span class="sxs-lookup"><span data-stu-id="136aa-160">On the Action Pane, select **Reply**.</span></span>
18. <span data-ttu-id="136aa-161">选择**将数据复制到回复**。</span><span class="sxs-lookup"><span data-stu-id="136aa-161">Select **Copy data to reply**.</span></span> <span data-ttu-id="136aa-162">这将把数量和日期之类数据从询价复制到回复。</span><span class="sxs-lookup"><span data-stu-id="136aa-162">This copies data, such as the quantity and dates, from the RFQ to the reply.</span></span>  
19. <span data-ttu-id="136aa-163">在**单价**字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="136aa-163">In the **Unit price** field, enter a number.</span></span> <span data-ttu-id="136aa-164">这是您从供应商处收到的价格。</span><span class="sxs-lookup"><span data-stu-id="136aa-164">This is the price that you’ve received from the vendor.</span></span> <span data-ttu-id="136aa-165">您可能还希望输入供应商提供的其他信息。</span><span class="sxs-lookup"><span data-stu-id="136aa-165">You might also want to enter additional information from the vendor.</span></span>  
20. <span data-ttu-id="136aa-166">选择**接受**。</span><span class="sxs-lookup"><span data-stu-id="136aa-166">Select **Accept**.</span></span>
21. <span data-ttu-id="136aa-167">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="136aa-167">Select **OK**.</span></span>

## <a name="verify-that-vendor-and-price-have-been-transferred-to-the-requisition"></a><span data-ttu-id="136aa-168">验证是否已将供应商和价格转移到申请</span><span class="sxs-lookup"><span data-stu-id="136aa-168">Verify that vendor and price have been transferred to the requisition</span></span>
1. <span data-ttu-id="136aa-169">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="136aa-169">Close the page.</span></span>
2. <span data-ttu-id="136aa-170">选择**行**。</span><span class="sxs-lookup"><span data-stu-id="136aa-170">Select **Lines**.</span></span>
3. <span data-ttu-id="136aa-171">选择**相关信息**。</span><span class="sxs-lookup"><span data-stu-id="136aa-171">Select **Related information**.</span></span>
4. <span data-ttu-id="136aa-172">选择**采购申请**。</span><span class="sxs-lookup"><span data-stu-id="136aa-172">Select **Purchase requisition**.</span></span>
5. <span data-ttu-id="136aa-173">选择已转移到询价的行。</span><span class="sxs-lookup"><span data-stu-id="136aa-173">Select the line that was transferred to the RFQ.</span></span> <span data-ttu-id="136aa-174">验证是否已将价格和供应商复制到申请。</span><span class="sxs-lookup"><span data-stu-id="136aa-174">Verify that the price and vendor have been copied to the requisition.</span></span>  
6. <span data-ttu-id="136aa-175">选择**工作流**以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="136aa-175">Select **Workflow** to open the drop dialog.</span></span>
7. <span data-ttu-id="136aa-176">选择“完成”。</span><span class="sxs-lookup"><span data-stu-id="136aa-176">Select Complete.</span></span>
8. <span data-ttu-id="136aa-177">选择此页面。</span><span class="sxs-lookup"><span data-stu-id="136aa-177">Select the page.</span></span>
9. <span data-ttu-id="136aa-178">选择“完成”。</span><span class="sxs-lookup"><span data-stu-id="136aa-178">Select Complete.</span></span>

