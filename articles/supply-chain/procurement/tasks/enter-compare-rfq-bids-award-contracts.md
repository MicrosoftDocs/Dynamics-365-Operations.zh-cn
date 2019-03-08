---
title: 输入和比较询价出价并授予合同
description: 此过程显示您如何输入给询价的回复，以及如何对出价评分和比较出价，然后将出价授予某一供应商。
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchRFQCaseTableListPage, PurchRFQCaseTable, PurchRFQReplyTable, PurchRFQCompare, PurchRFQEditLines, PurchRFQEditLinesParameters, PurchTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7cd4876acfebcc9595abb358cfc9b355e93041d6
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/29/2019
ms.locfileid: "349990"
---
# <a name="enter-and-compare-rfq-bids-and-award-contracts"></a><span data-ttu-id="eafdf-103">输入和比较询价出价并授予合同</span><span class="sxs-lookup"><span data-stu-id="eafdf-103">Enter and compare RFQ bids, and award contracts</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="eafdf-104">此过程显示您如何输入给询价的回复，以及如何对出价评分和比较出价，然后将出价授予某一供应商。</span><span class="sxs-lookup"><span data-stu-id="eafdf-104">This procedure shows you how to enter replies to an RFQ, score and compare bids, and then award the bid to one of the vendors.</span></span> <span data-ttu-id="eafdf-105">您可以在演示数据公司 USMF 中使用此过程。</span><span class="sxs-lookup"><span data-stu-id="eafdf-105">You can use this procedure in demo data company USMF.</span></span> <span data-ttu-id="eafdf-106">在您开始前，您必须有具有至少发送给两个供应商的两个行的询价。</span><span class="sxs-lookup"><span data-stu-id="eafdf-106">Before you start, you must have an RFQ with two lines that has been sent to at least two vendors.</span></span> <span data-ttu-id="eafdf-107">您可以运行“创建询价”过程作为创建此询价的先决条件。</span><span class="sxs-lookup"><span data-stu-id="eafdf-107">You can run the "Create a request for quotation" procedure as a prerequisite to create this.</span></span> <span data-ttu-id="eafdf-108">您需要先设置计分条件才能运行此过程。</span><span class="sxs-lookup"><span data-stu-id="eafdf-108">You need to have set up scoring criteria before you can run this procedure.</span></span>


## <a name="enter-a-reply-from-a-vendor"></a><span data-ttu-id="eafdf-109">输入供应商的回复</span><span class="sxs-lookup"><span data-stu-id="eafdf-109">Enter a reply from a vendor</span></span>
1. <span data-ttu-id="eafdf-110">转到“采购”>“询价”>“所有询价”。</span><span class="sxs-lookup"><span data-stu-id="eafdf-110">Go to Procurement and sourcing > Requests for quotations > All requests for quotations.</span></span>
2. <span data-ttu-id="eafdf-111">选择具有“已发送”状态的询价，并单击询价案例编号上的链接。</span><span class="sxs-lookup"><span data-stu-id="eafdf-111">Select an RFQ that has a status of Sent and click the link on the Request for quotation case number.</span></span>
    * <span data-ttu-id="eafdf-112">应已发送询价到至少 2 个供应商。</span><span class="sxs-lookup"><span data-stu-id="eafdf-112">The RFQ should have been sent to at least 2 vendors.</span></span>  
3. <span data-ttu-id="eafdf-113">单击“抬头”转到供应商列表。</span><span class="sxs-lookup"><span data-stu-id="eafdf-113">Click Header to go to the list of vendors.</span></span>
4. <span data-ttu-id="eafdf-114">选择您要在询价中为其输入响应的供应商。</span><span class="sxs-lookup"><span data-stu-id="eafdf-114">Select the vendor for whom you want to enter a response on the RFQ.</span></span>
5. <span data-ttu-id="eafdf-115">单击“输入回复”。</span><span class="sxs-lookup"><span data-stu-id="eafdf-115">Click Enter reply.</span></span>
6. <span data-ttu-id="eafdf-116">在“操作”窗格上，单击“回复”。</span><span class="sxs-lookup"><span data-stu-id="eafdf-116">On the Action Pane, click Reply.</span></span>
7. <span data-ttu-id="eafdf-117">单击“将数据复制到回复”。</span><span class="sxs-lookup"><span data-stu-id="eafdf-117">Click Copy data to reply.</span></span>
    * <span data-ttu-id="eafdf-118">此操作将复制所选的数据，例如，从询价案例到询价回复的数量。</span><span class="sxs-lookup"><span data-stu-id="eafdf-118">This action will copy selected data, for example, the quantity from the RFQ case to the RFQ reply.</span></span> <span data-ttu-id="eafdf-119">您也可以跳过此操作，并在编辑回复时手动填写所有响应字段。</span><span class="sxs-lookup"><span data-stu-id="eafdf-119">Alternatively you can skip this action and fill in all the response fields manually when you edit the reply.</span></span>  
8. <span data-ttu-id="eafdf-120">单击“编辑”。</span><span class="sxs-lookup"><span data-stu-id="eafdf-120">Click Edit.</span></span>
9. <span data-ttu-id="eafdf-121">在“单位价格”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="eafdf-121">In the Unit price field, enter a number.</span></span>
10. <span data-ttu-id="eafdf-122">选择其他报价单行。</span><span class="sxs-lookup"><span data-stu-id="eafdf-122">Choose the other quotation line.</span></span>
11. <span data-ttu-id="eafdf-123">在“单位价格”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="eafdf-123">In the Unit price field, enter a number.</span></span>

## <a name="score-the-bid"></a><span data-ttu-id="eafdf-124">为出价评分</span><span class="sxs-lookup"><span data-stu-id="eafdf-124">Score the bid</span></span>
1. <span data-ttu-id="eafdf-125">单击“抬头”转到出价评分。</span><span class="sxs-lookup"><span data-stu-id="eafdf-125">Click Header to go to the scoring of the bid.</span></span>
2. <span data-ttu-id="eafdf-126">扩展“出价评分”部分。</span><span class="sxs-lookup"><span data-stu-id="eafdf-126">Expand the Bid scoring section.</span></span>
3. <span data-ttu-id="eafdf-127">在“分数”字段中，为一个计分条件输入数字。</span><span class="sxs-lookup"><span data-stu-id="eafdf-127">In the Score field, enter a number for one of the scoring criteria.</span></span>
    * <span data-ttu-id="eafdf-128">如果您悬停在一个计分条件上，工具提示将显示您必须计分的范围。</span><span class="sxs-lookup"><span data-stu-id="eafdf-128">If you hover over one of the scoring criteria a tooltip shows the range that you have to score within.</span></span> <span data-ttu-id="eafdf-129">在此演示中，您可以添加 1 和 5 之间的数字到任何条件。</span><span class="sxs-lookup"><span data-stu-id="eafdf-129">In this demo you can add a number between 1 and 5 to any of the criteria.</span></span>  
4. <span data-ttu-id="eafdf-130">选择另一个计分条件。</span><span class="sxs-lookup"><span data-stu-id="eafdf-130">Select another scoring criterion.</span></span>
5. <span data-ttu-id="eafdf-131">在“分数”字段中输入数字。</span><span class="sxs-lookup"><span data-stu-id="eafdf-131">In the Score field, enter a number.</span></span>
6. <span data-ttu-id="eafdf-132">扩展“调查表”部分。</span><span class="sxs-lookup"><span data-stu-id="eafdf-132">Expand the Questionnaires section.</span></span>
    * <span data-ttu-id="eafdf-133">如果询价案例具有发送到供应商的调查表，您可以在调查表部分中输入他们的响应。</span><span class="sxs-lookup"><span data-stu-id="eafdf-133">If the RFQ case has a questionnaire that was sent to the vendors, you can enter their responses in the questionnaire section.</span></span>  
7. <span data-ttu-id="eafdf-134">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="eafdf-134">Close the page.</span></span>

## <a name="enter-a-reply-for-another-vendor"></a><span data-ttu-id="eafdf-135">输入其他供应商的回复</span><span class="sxs-lookup"><span data-stu-id="eafdf-135">Enter a reply for another vendor</span></span>
1. <span data-ttu-id="eafdf-136">通过清除您刚才为其输入回复的供应商，然后选择下一个供应商行来选择下一个供应商。</span><span class="sxs-lookup"><span data-stu-id="eafdf-136">Select the next vendor by clearing the vendor you have just entered the reply for and then selecting the row for the next vendor.</span></span>
2. <span data-ttu-id="eafdf-137">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="eafdf-137">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="eafdf-138">单击“输入回复”。</span><span class="sxs-lookup"><span data-stu-id="eafdf-138">Click Enter reply.</span></span>
4. <span data-ttu-id="eafdf-139">单击“将数据复制到回复”。</span><span class="sxs-lookup"><span data-stu-id="eafdf-139">Click Copy data to reply.</span></span>
5. <span data-ttu-id="eafdf-140">单击“编辑”。</span><span class="sxs-lookup"><span data-stu-id="eafdf-140">Click Edit.</span></span>
6. <span data-ttu-id="eafdf-141">在“单位价格”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="eafdf-141">In the Unit price field, enter a number.</span></span>
7. <span data-ttu-id="eafdf-142">选择其他报价单行。</span><span class="sxs-lookup"><span data-stu-id="eafdf-142">Choose the other quotation line.</span></span>
8. <span data-ttu-id="eafdf-143">在“单位价格”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="eafdf-143">In the Unit price field, enter a number.</span></span>

## <a name="score-the-second-bid"></a><span data-ttu-id="eafdf-144">为第二个出价评分</span><span class="sxs-lookup"><span data-stu-id="eafdf-144">Score the second bid</span></span>
1. <span data-ttu-id="eafdf-145">单击“抬头”转到出价评分。</span><span class="sxs-lookup"><span data-stu-id="eafdf-145">Click Header to go to scoring of the bid.</span></span>
2. <span data-ttu-id="eafdf-146">在“分数”字段中输入数字。</span><span class="sxs-lookup"><span data-stu-id="eafdf-146">In the Score field, enter a number.</span></span>
3. <span data-ttu-id="eafdf-147">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="eafdf-147">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="eafdf-148">在“分数”字段中输入数字。</span><span class="sxs-lookup"><span data-stu-id="eafdf-148">In the Score field, enter a number.</span></span>

## <a name="compare-the-replies"></a><span data-ttu-id="eafdf-149">比较回复</span><span class="sxs-lookup"><span data-stu-id="eafdf-149">Compare the replies</span></span>
1. <span data-ttu-id="eafdf-150">在操作窗格上，单击“常规”。</span><span class="sxs-lookup"><span data-stu-id="eafdf-150">On the Action Pane, click General.</span></span>
2. <span data-ttu-id="eafdf-151">单击“比较回复”。</span><span class="sxs-lookup"><span data-stu-id="eafdf-151">Click Compare replies.</span></span>
3. <span data-ttu-id="eafdf-152">在“排名”字段中输入数字。</span><span class="sxs-lookup"><span data-stu-id="eafdf-152">In the Rank field, enter a number.</span></span>
    * <span data-ttu-id="eafdf-153">此页显示具有标头和行的出价，以及标头级别的总分。</span><span class="sxs-lookup"><span data-stu-id="eafdf-153">This page shows the bids with the header and lines, and the total score on the header level.</span></span> <span data-ttu-id="eafdf-154">您可以通过在网格中排序对行进行比较，以便可比较的行相互相邻排列。</span><span class="sxs-lookup"><span data-stu-id="eafdf-154">You can compare the lines by sorting in the grid so that comparable lines are next to each other.</span></span> <span data-ttu-id="eafdf-155">信息还包括：数量：供应商报价的数量。</span><span class="sxs-lookup"><span data-stu-id="eafdf-155">The information also includes:   Quantity: The quantity quoted by the vendor.</span></span> <span data-ttu-id="eafdf-156">此数量可能不等于在 RFQ 中指定的数量。</span><span class="sxs-lookup"><span data-stu-id="eafdf-156">This might not equal the quantity specified in the RFQ.</span></span>   <span data-ttu-id="eafdf-157">净额：供应商的询价，在减去所有折扣后，针对行上的物料。</span><span class="sxs-lookup"><span data-stu-id="eafdf-157">Net amount: The price quoted by a vendor, after subtracting any discounts, for the items on the line.</span></span>   <span data-ttu-id="eafdf-158">偏差：投标标题或行的交货日期与询价标题或行所要求的交货日期之间偏差的天数。</span><span class="sxs-lookup"><span data-stu-id="eafdf-158">Deviation: The number of days that the delivery date in the bid header or line deviates from the requested delivery date in the RFQ header or RFQ line.</span></span>   <span data-ttu-id="eafdf-159">您可以为每个出价输入排名。</span><span class="sxs-lookup"><span data-stu-id="eafdf-159">You can enter a rank for each bid.</span></span>  
4. <span data-ttu-id="eafdf-160">选择要排名的其他出价的抬头行。</span><span class="sxs-lookup"><span data-stu-id="eafdf-160">Select the header line for the other bid that you want to rank.</span></span>
5. <span data-ttu-id="eafdf-161">在“排名”字段中输入数字。</span><span class="sxs-lookup"><span data-stu-id="eafdf-161">In the Rank field, enter a number.</span></span>
6. <span data-ttu-id="eafdf-162">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="eafdf-162">Click Save.</span></span>

## <a name="reject-a-bid"></a><span data-ttu-id="eafdf-163">拒绝出价</span><span class="sxs-lookup"><span data-stu-id="eafdf-163">Reject a bid</span></span>
1. <span data-ttu-id="eafdf-164">选择要拒绝的出价的抬头行。</span><span class="sxs-lookup"><span data-stu-id="eafdf-164">Select the header line for the bid that you want to reject.</span></span>
    * <span data-ttu-id="eafdf-165">每次每个出价内只能接受、拒绝或返回一个出价或行。</span><span class="sxs-lookup"><span data-stu-id="eafdf-165">You can only accept, reject, or return one bid or lines within one bid at a time.</span></span>  
2. <span data-ttu-id="eafdf-166">选择“标记”复选框。</span><span class="sxs-lookup"><span data-stu-id="eafdf-166">Select the Mark check box.</span></span>
    * <span data-ttu-id="eafdf-167">如果您在出价的抬头上选中“标记”复选框，那么所有行也将被标记。</span><span class="sxs-lookup"><span data-stu-id="eafdf-167">If you select the Mark check box on the Header of the bid then all the lines will be marked as well.</span></span> <span data-ttu-id="eafdf-168">您还可以选择标记出价内行的子集以拒绝或接受它们。</span><span class="sxs-lookup"><span data-stu-id="eafdf-168">You could also choose to mark a subset of the lines within the bid to reject or accept those.</span></span> <span data-ttu-id="eafdf-169">您可以接受询价的有些行的一个供应商出价，然后将其他询价行授予不同的供应商，但是，您需要在 2 个步骤中执行此操作，一次一个出价。</span><span class="sxs-lookup"><span data-stu-id="eafdf-169">It’s possible to accept one vendor’s bid for some lines of an RFQ, and then award other RFQ lines to a different vendor, however you need to do this in 2 steps, one bid at a time.</span></span> <span data-ttu-id="eafdf-170">如果存在替换行，则您可以只接受原始投标行或替换行，但不能同时接受两个。</span><span class="sxs-lookup"><span data-stu-id="eafdf-170">If alternate lines are present, you can only accept either the original bid line or its alternate, but not both.</span></span>  
3. <span data-ttu-id="eafdf-171">单击“拒绝”。</span><span class="sxs-lookup"><span data-stu-id="eafdf-171">Click Reject.</span></span>
4. <span data-ttu-id="eafdf-172">单击“参数”以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="eafdf-172">Click Parameters to open the drop dialog.</span></span>
5. <span data-ttu-id="eafdf-173">在“拒绝原因”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="eafdf-173">In the Reason reject field, enter or select a value.</span></span>
    * <span data-ttu-id="eafdf-174">拒绝原因将存储在回复中。</span><span class="sxs-lookup"><span data-stu-id="eafdf-174">The reason for rejection will be stored on the reply.</span></span>  
6. <span data-ttu-id="eafdf-175">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="eafdf-175">Click OK.</span></span>
7. <span data-ttu-id="eafdf-176">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="eafdf-176">Click OK.</span></span>
8. <span data-ttu-id="eafdf-177">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="eafdf-177">Close the page.</span></span>
9. <span data-ttu-id="eafdf-178">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="eafdf-178">Close the page.</span></span>
10. <span data-ttu-id="eafdf-179">刷新该页面。</span><span class="sxs-lookup"><span data-stu-id="eafdf-179">Refresh the page.</span></span>

## <a name="accept-a-bid"></a><span data-ttu-id="eafdf-180">接受出价</span><span class="sxs-lookup"><span data-stu-id="eafdf-180">Accept a bid</span></span>
1. <span data-ttu-id="eafdf-181">选择要接受的出价，然后单击“询价”字段中的链接。</span><span class="sxs-lookup"><span data-stu-id="eafdf-181">Select the bid that you want to accept and then click the link in the Request for quotation field.</span></span>
2. <span data-ttu-id="eafdf-182">在“操作”窗格上，单击“回复”。</span><span class="sxs-lookup"><span data-stu-id="eafdf-182">On the Action Pane, click Reply.</span></span>
3. <span data-ttu-id="eafdf-183">单击“接受”。</span><span class="sxs-lookup"><span data-stu-id="eafdf-183">Click Accept.</span></span>
    * <span data-ttu-id="eafdf-184">如果标记了特定行而不是其他行，那么接受操作将只包括标记的行。</span><span class="sxs-lookup"><span data-stu-id="eafdf-184">If you have marked specific lines and not others then the accept action will only include the marked lines.</span></span> <span data-ttu-id="eafdf-185">如果要接受出价的所有行，那么您不必标记这些行。</span><span class="sxs-lookup"><span data-stu-id="eafdf-185">If you want to accept all lines on the bid then you do not have to mark the lines.</span></span>  
4. <span data-ttu-id="eafdf-186">单击“参数”以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="eafdf-186">Click Parameters to open the drop dialog.</span></span>
    * <span data-ttu-id="eafdf-187">这允许您记录接受出价的原因。</span><span class="sxs-lookup"><span data-stu-id="eafdf-187">This allows you to record a reason for accepting the bid.</span></span> <span data-ttu-id="eafdf-188">原因将存储在出价中。</span><span class="sxs-lookup"><span data-stu-id="eafdf-188">The reason will be stored on the bid.</span></span>  
5. <span data-ttu-id="eafdf-189">在“接受原因”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="eafdf-189">In the Reason accept field, enter or select a value.</span></span>
6. <span data-ttu-id="eafdf-190">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="eafdf-190">Click OK.</span></span>
7. <span data-ttu-id="eafdf-191">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="eafdf-191">Click OK.</span></span>
    * <span data-ttu-id="eafdf-192">在单击“确定”后，这将基于在询价接受中包括的行生成采购订单。</span><span class="sxs-lookup"><span data-stu-id="eafdf-192">When you click OK this generates a purchase order based on the lines that are included in the RFQ acceptance.</span></span> <span data-ttu-id="eafdf-193">如果存在其他尚未处理的出价（已接受、已拒绝或已返回），那么系统将提示您拒绝其余出价。</span><span class="sxs-lookup"><span data-stu-id="eafdf-193">If there are other bids that have not been processed (accepted, rejected, or returned) then the system will prompt you to reject the remaining bids.</span></span>  

## <a name="view-the-purchase-order-thats-been-generated"></a><span data-ttu-id="eafdf-194">查看已生成的采购订单</span><span class="sxs-lookup"><span data-stu-id="eafdf-194">View the purchase order that's been generated</span></span>
1. <span data-ttu-id="eafdf-195">在操作窗格上，单击“常规”。</span><span class="sxs-lookup"><span data-stu-id="eafdf-195">On the Action Pane, click General.</span></span>
2. <span data-ttu-id="eafdf-196">单击“采购订单”。</span><span class="sxs-lookup"><span data-stu-id="eafdf-196">Click Purchase order.</span></span>
    * <span data-ttu-id="eafdf-197">在这里您可以查看接受出价时生成的采购订单。</span><span class="sxs-lookup"><span data-stu-id="eafdf-197">Here you can see the purchase order that was generated when you accepted the bid.</span></span>  
3. <span data-ttu-id="eafdf-198">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="eafdf-198">Close the page.</span></span>
4. <span data-ttu-id="eafdf-199">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="eafdf-199">Close the page.</span></span>
5. <span data-ttu-id="eafdf-200">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="eafdf-200">Close the page.</span></span>
6. <span data-ttu-id="eafdf-201">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="eafdf-201">Close the page.</span></span>

