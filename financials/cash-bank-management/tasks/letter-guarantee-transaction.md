--- 
title: "保函交易记录"
description: "该过程简单介绍了保函的处理流程。"
author: kweekley
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 21895bcda8f0fe46e9b7c4b2189ca8b13e0dc012
ms.contentlocale: zh-cn
ms.lasthandoff: 08/29/2017

---
# <a name="letter-of-guarantee-transaction"></a><span data-ttu-id="cea92-103">保函交易记录</span><span class="sxs-lookup"><span data-stu-id="cea92-103">Letter of guarantee transaction</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="cea92-104">该过程简单介绍了保函的处理流程。</span><span class="sxs-lookup"><span data-stu-id="cea92-104">This procedure walks through the Letter of guarantee process.</span></span>



<span data-ttu-id="cea92-105">在完成该过程之前必须先完成以下任务：</span><span class="sxs-lookup"><span data-stu-id="cea92-105">The following tasks must be complete before completing this procedure:</span></span>

- <span data-ttu-id="cea92-106">设置银行设施和过帐保函模板。</span><span class="sxs-lookup"><span data-stu-id="cea92-106">Set up bank facilities and posting profiles for a letter of guarantee.</span></span>

- <span data-ttu-id="cea92-107">创建保函的银行信贷协议。</span><span class="sxs-lookup"><span data-stu-id="cea92-107">Create a bank facility agreement for a letter of guarantee.</span></span>



<span data-ttu-id="cea92-108">该程序适用于 USMF 演示公司。</span><span class="sxs-lookup"><span data-stu-id="cea92-108">This procedure uses the USMF demo company.</span></span>


## <a name="create-sales-order-with-letter-of-guarantee"></a><span data-ttu-id="cea92-109">创建“保函销售订单”</span><span class="sxs-lookup"><span data-stu-id="cea92-109">Create Sales Order with Letter of Guarantee</span></span>
1. <span data-ttu-id="cea92-110">转到应收帐项目>订单>所有销售订单。</span><span class="sxs-lookup"><span data-stu-id="cea92-110">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="cea92-111">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="cea92-111">Click New.</span></span>
3. <span data-ttu-id="cea92-112">在“客户帐户”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="cea92-112">In the Customer account field, enter or select a value.</span></span>
4. <span data-ttu-id="cea92-113">展开“常规”部分。</span><span class="sxs-lookup"><span data-stu-id="cea92-113">Expand the General section.</span></span>
5. <span data-ttu-id="cea92-114">在“站点”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="cea92-114">In the Site field, enter or select a value.</span></span>
6. <span data-ttu-id="cea92-115">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="cea92-115">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="cea92-116">在“仓库”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="cea92-116">In the Warehouse field, enter or select a value.</span></span>
8. <span data-ttu-id="cea92-117">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="cea92-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="cea92-118">在“银行文档类型”字段中，选择“保函”。</span><span class="sxs-lookup"><span data-stu-id="cea92-118">In the Bank document type field, select 'Letter of guarantee'.</span></span>
10. <span data-ttu-id="cea92-119">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="cea92-119">Click OK.</span></span>
11. <span data-ttu-id="cea92-120">在“物料编号”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="cea92-120">In the Item number field, enter or select a value.</span></span>
12. <span data-ttu-id="cea92-121">在“单位价格”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="cea92-121">In the Unit price field, enter a number.</span></span>
13. <span data-ttu-id="cea92-122">展开“行明细”部分。</span><span class="sxs-lookup"><span data-stu-id="cea92-122">Expand the Line details section.</span></span>
14. <span data-ttu-id="cea92-123">单击“交货”选项卡。</span><span class="sxs-lookup"><span data-stu-id="cea92-123">Click the Delivery tab.</span></span>
    * <span data-ttu-id="cea92-124">说明：选择“交货日期控制 = 无”</span><span class="sxs-lookup"><span data-stu-id="cea92-124">Note: Select Delivery date control = None</span></span>  
15. <span data-ttu-id="cea92-125">在“请求装运日期”字段中，输入一个日期。</span><span class="sxs-lookup"><span data-stu-id="cea92-125">In the Requested ship date field, enter a date.</span></span>
16. <span data-ttu-id="cea92-126">在“确认装运日期”字段中，输入一个日期。</span><span class="sxs-lookup"><span data-stu-id="cea92-126">In the Confirmed ship date field, enter a date.</span></span>

## <a name="process-letter-of-guaranteerequest"></a><span data-ttu-id="cea92-127">处理保函_请求</span><span class="sxs-lookup"><span data-stu-id="cea92-127">Process letter of guarantee_Request</span></span>
1. <span data-ttu-id="cea92-128">在“操作窗格”上单击“管理”。</span><span class="sxs-lookup"><span data-stu-id="cea92-128">On the Action Pane, click Manage.</span></span>
2. <span data-ttu-id="cea92-129">单击“保函”。</span><span class="sxs-lookup"><span data-stu-id="cea92-129">Click Letter of guarantee.</span></span>
3. <span data-ttu-id="cea92-130">在“操作窗格”上单击“保函”。</span><span class="sxs-lookup"><span data-stu-id="cea92-130">On the Action Pane, click Letter of guarantee.</span></span>
4. <span data-ttu-id="cea92-131">单击“请求”打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="cea92-131">Click Request to open the drop dialog.</span></span>
5. <span data-ttu-id="cea92-132">在“类型”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="cea92-132">In the Type field, enter or select a value.</span></span>
6. <span data-ttu-id="cea92-133">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="cea92-133">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="cea92-134">在“值”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="cea92-134">In the Value field, enter a number.</span></span>
8. <span data-ttu-id="cea92-135">在“到期日期”字段中，输入日期和时间。</span><span class="sxs-lookup"><span data-stu-id="cea92-135">In the Expiration date field, enter a date and time.</span></span>
9. <span data-ttu-id="cea92-136">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="cea92-136">Click OK.</span></span>
10. <span data-ttu-id="cea92-137">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="cea92-137">Close the page.</span></span>

## <a name="process-letter-of-guaranteesubmit-to-bank"></a><span data-ttu-id="cea92-138">处理保函_提交至银行</span><span class="sxs-lookup"><span data-stu-id="cea92-138">Process letter of guarantee_Submit to bank</span></span>
1. <span data-ttu-id="cea92-139">转到“现金和银行管理”>“保函”>“保函”。</span><span class="sxs-lookup"><span data-stu-id="cea92-139">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
2. <span data-ttu-id="cea92-140">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="cea92-140">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="cea92-141">单击“提交至银行”以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="cea92-141">Click Submit to bank to open the drop dialog.</span></span>
4. <span data-ttu-id="cea92-142">在“银行帐户”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="cea92-142">In the Bank account field, enter or select a value.</span></span>
5. <span data-ttu-id="cea92-143">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="cea92-143">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="cea92-144">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="cea92-144">Click OK.</span></span>

## <a name="process-letter-of-guaranteereceive-from-bank"></a><span data-ttu-id="cea92-145">处理保函_从银行处收到</span><span class="sxs-lookup"><span data-stu-id="cea92-145">Process letter of guarantee_Receive from bank</span></span>
1. <span data-ttu-id="cea92-146">单击“从银行处收到”以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="cea92-146">Click Receive from bank to open the drop dialog.</span></span>
2. <span data-ttu-id="cea92-147">在“银行号码”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="cea92-147">In the Bank number field, type a value.</span></span>
    * <span data-ttu-id="cea92-148">核实“毛利和费用”字段中所计算出的值。</span><span class="sxs-lookup"><span data-stu-id="cea92-148">Verify the values in the calculated Margin and Expense fields.</span></span>  
3. <span data-ttu-id="cea92-149">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="cea92-149">Click OK.</span></span>
4. <span data-ttu-id="cea92-150">展开“行为”部分。</span><span class="sxs-lookup"><span data-stu-id="cea92-150">Expand the Actions section.</span></span>
    * <span data-ttu-id="cea92-151">核实“从银行处收到”记录。</span><span class="sxs-lookup"><span data-stu-id="cea92-151">Verify the 'Receive from bank' record.</span></span>  
5. <span data-ttu-id="cea92-152">单击以访问“日记帐批号”字段中的链接。</span><span class="sxs-lookup"><span data-stu-id="cea92-152">Click to follow the link in the Journal batch number field.</span></span>
6. <span data-ttu-id="cea92-153">单击“行”。</span><span class="sxs-lookup"><span data-stu-id="cea92-153">Click Lines.</span></span>
    * <span data-ttu-id="cea92-154">核实日记帐条目的过帐信息。</span><span class="sxs-lookup"><span data-stu-id="cea92-154">Verify the posting of journal entries.</span></span>  
7. <span data-ttu-id="cea92-155">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="cea92-155">Close the page.</span></span>

## <a name="process-letter-of-guaranteegive-to-beneficiary"></a><span data-ttu-id="cea92-156">处理保函_给受益人</span><span class="sxs-lookup"><span data-stu-id="cea92-156">Process letter of guarantee_Give to beneficiary</span></span>
1. <span data-ttu-id="cea92-157">转到应收帐项目>订单>所有销售订单。</span><span class="sxs-lookup"><span data-stu-id="cea92-157">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="cea92-158">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="cea92-158">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="cea92-159">在“操作窗格”上单击“管理”。</span><span class="sxs-lookup"><span data-stu-id="cea92-159">On the Action Pane, click Manage.</span></span>
4. <span data-ttu-id="cea92-160">单击“保函”。</span><span class="sxs-lookup"><span data-stu-id="cea92-160">Click Letter of guarantee.</span></span>
5. <span data-ttu-id="cea92-161">在“操作窗格”上单击“保函”。</span><span class="sxs-lookup"><span data-stu-id="cea92-161">On the Action Pane, click Letter of guarantee.</span></span>
6. <span data-ttu-id="cea92-162">单击“给受益人”以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="cea92-162">Click Give to beneficiary to open the drop dialog.</span></span>
7. <span data-ttu-id="cea92-163">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="cea92-163">Click OK.</span></span>
8. <span data-ttu-id="cea92-164">转到“现金和银行管理”>“保函”>“保函”。</span><span class="sxs-lookup"><span data-stu-id="cea92-164">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
9. <span data-ttu-id="cea92-165">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="cea92-165">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="cea92-166">单击“给受益人”以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="cea92-166">Click Give to beneficiary to open the drop dialog.</span></span>
11. <span data-ttu-id="cea92-167">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="cea92-167">Click OK.</span></span>
12. <span data-ttu-id="cea92-168">展开“行为”部分。</span><span class="sxs-lookup"><span data-stu-id="cea92-168">Expand the Actions section.</span></span>
    * <span data-ttu-id="cea92-169">验证“给受益人”记录。</span><span class="sxs-lookup"><span data-stu-id="cea92-169">Validate the 'Give to beneficiary' record.</span></span>  

## <a name="process-letter-of-guaranteeincrease-value"></a><span data-ttu-id="cea92-170">处理保函_增加值</span><span class="sxs-lookup"><span data-stu-id="cea92-170">Process letter of guarantee_Increase value</span></span>
1. <span data-ttu-id="cea92-171">转到应收帐项目>订单>所有销售订单。</span><span class="sxs-lookup"><span data-stu-id="cea92-171">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="cea92-172">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="cea92-172">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="cea92-173">在“操作窗格”上单击“管理”。</span><span class="sxs-lookup"><span data-stu-id="cea92-173">On the Action Pane, click Manage.</span></span>
4. <span data-ttu-id="cea92-174">单击“保函”。</span><span class="sxs-lookup"><span data-stu-id="cea92-174">Click Letter of guarantee.</span></span>
5. <span data-ttu-id="cea92-175">在“操作窗格”上单击“保函”。</span><span class="sxs-lookup"><span data-stu-id="cea92-175">On the Action Pane, click Letter of guarantee.</span></span>
6. <span data-ttu-id="cea92-176">单击“增加值”以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="cea92-176">Click Increase value to open the drop dialog.</span></span>
7. <span data-ttu-id="cea92-177">在“添加值”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="cea92-177">In the Value to add field, enter a number.</span></span>
8. <span data-ttu-id="cea92-178">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="cea92-178">Click OK.</span></span>
9. <span data-ttu-id="cea92-179">转到“现金和银行管理”>“保函”>“保函”。</span><span class="sxs-lookup"><span data-stu-id="cea92-179">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
10. <span data-ttu-id="cea92-180">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="cea92-180">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="cea92-181">单击“增加值”以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="cea92-181">Click Increase value to open the drop dialog.</span></span>
12. <span data-ttu-id="cea92-182">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="cea92-182">Click OK.</span></span>
13. <span data-ttu-id="cea92-183">展开“行为”部分。</span><span class="sxs-lookup"><span data-stu-id="cea92-183">Expand the Actions section.</span></span>
    * <span data-ttu-id="cea92-184">核实“增加值”记录。</span><span class="sxs-lookup"><span data-stu-id="cea92-184">Verify the 'Increase value' record.</span></span>  
14. <span data-ttu-id="cea92-185">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="cea92-185">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="cea92-186">单击以访问“日记帐批号”字段中的链接。</span><span class="sxs-lookup"><span data-stu-id="cea92-186">Click to follow the link in the Journal batch number field.</span></span>
16. <span data-ttu-id="cea92-187">单击“行”。</span><span class="sxs-lookup"><span data-stu-id="cea92-187">Click Lines.</span></span>
    * <span data-ttu-id="cea92-188">核实已过帐的日记帐条目。</span><span class="sxs-lookup"><span data-stu-id="cea92-188">Verify the posted journal entries.</span></span>  

## <a name="process-letter-of-guaranteeliquidate"></a><span data-ttu-id="cea92-189">处理保函_清算</span><span class="sxs-lookup"><span data-stu-id="cea92-189">Process letter of guarantee_Liquidate</span></span>
1. <span data-ttu-id="cea92-190">转到应收帐项目>订单>所有销售订单。</span><span class="sxs-lookup"><span data-stu-id="cea92-190">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="cea92-191">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="cea92-191">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="cea92-192">在“操作窗格”上单击“管理”。</span><span class="sxs-lookup"><span data-stu-id="cea92-192">On the Action Pane, click Manage.</span></span>
4. <span data-ttu-id="cea92-193">单击“保函”。</span><span class="sxs-lookup"><span data-stu-id="cea92-193">Click Letter of guarantee.</span></span>
5. <span data-ttu-id="cea92-194">在“操作窗格”上单击“保函”。</span><span class="sxs-lookup"><span data-stu-id="cea92-194">On the Action Pane, click Letter of guarantee.</span></span>
6. <span data-ttu-id="cea92-195">单击“清算”以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="cea92-195">Click Liquidate to open the drop dialog.</span></span>
7. <span data-ttu-id="cea92-196">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="cea92-196">Click OK.</span></span>
8. <span data-ttu-id="cea92-197">转到“现金和银行管理”>“保函”>“保函”。</span><span class="sxs-lookup"><span data-stu-id="cea92-197">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
9. <span data-ttu-id="cea92-198">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="cea92-198">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="cea92-199">单击“清算”以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="cea92-199">Click Liquidate to open the drop dialog.</span></span>
11. <span data-ttu-id="cea92-200">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="cea92-200">Click OK.</span></span>
12. <span data-ttu-id="cea92-201">展开“行为”部分。</span><span class="sxs-lookup"><span data-stu-id="cea92-201">Expand the Actions section.</span></span>
    * <span data-ttu-id="cea92-202">核实“清算”记录。</span><span class="sxs-lookup"><span data-stu-id="cea92-202">Verify the 'Liquidate' record.</span></span>  
13. <span data-ttu-id="cea92-203">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="cea92-203">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="cea92-204">单击以访问“日记帐批号”字段中的链接。</span><span class="sxs-lookup"><span data-stu-id="cea92-204">Click to follow the link in the Journal batch number field.</span></span>
15. <span data-ttu-id="cea92-205">单击“行”。</span><span class="sxs-lookup"><span data-stu-id="cea92-205">Click Lines.</span></span>
    * <span data-ttu-id="cea92-206">核实已过帐的日记帐条目。</span><span class="sxs-lookup"><span data-stu-id="cea92-206">Verify the posted journal entries.</span></span>  
16. <span data-ttu-id="cea92-207">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="cea92-207">Close the page.</span></span>


