---
title: 保函交易记录
description: 该过程简单介绍了保函的处理流程。
author: kweekley
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: Reasons, SalesTableListPage, SalesCreateOrder, SalesTable, BankLGRequestForm, BankLGRequestFormRequest, BankLGGuarantee, BankLGFormSubmitToBank, BankDocumentAgreementLineLookup, BankLGFormReceiveFromBank, LedgerJournalTable, LedgerJournalTransDaily, BankLGRequestFormGiveToBeneficiary, BankLGFormGiveToBeneficiary, BankLGRequestFormIncreaseValue, BankLGFormIncreaseValue, BankLGRequestFormLiquidate, BankLGFormLiquidate
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 089515287fc5706983b10614f69b4b1cd90178c5
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5834708"
---
# <a name="letter-of-guarantee-transaction"></a><span data-ttu-id="b5583-103">保函交易记录</span><span class="sxs-lookup"><span data-stu-id="b5583-103">Letter of guarantee transaction</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b5583-104">该过程简单介绍了保函的处理流程。</span><span class="sxs-lookup"><span data-stu-id="b5583-104">This procedure walks through the Letter of guarantee process.</span></span>



<span data-ttu-id="b5583-105">在完成该过程之前必须先完成以下任务：</span><span class="sxs-lookup"><span data-stu-id="b5583-105">The following tasks must be complete before completing this procedure:</span></span>

- <span data-ttu-id="b5583-106">设置银行设施和过帐保函模板。</span><span class="sxs-lookup"><span data-stu-id="b5583-106">Set up bank facilities and posting profiles for a letter of guarantee.</span></span>

- <span data-ttu-id="b5583-107">创建保函的银行信贷协议。</span><span class="sxs-lookup"><span data-stu-id="b5583-107">Create a bank facility agreement for a letter of guarantee.</span></span>



<span data-ttu-id="b5583-108">该程序适用于 USMF 演示公司。</span><span class="sxs-lookup"><span data-stu-id="b5583-108">This procedure uses the USMF demo company.</span></span>


## <a name="create-sales-order-with-letter-of-guarantee"></a><span data-ttu-id="b5583-109">创建“保函销售订单”</span><span class="sxs-lookup"><span data-stu-id="b5583-109">Create Sales Order with Letter of Guarantee</span></span>
1. <span data-ttu-id="b5583-110">转到应收帐项目>订单>所有销售订单。</span><span class="sxs-lookup"><span data-stu-id="b5583-110">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="b5583-111">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="b5583-111">Click New.</span></span>
3. <span data-ttu-id="b5583-112">在“客户帐户”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="b5583-112">In the Customer account field, enter or select a value.</span></span>
4. <span data-ttu-id="b5583-113">展开“常规”部分。</span><span class="sxs-lookup"><span data-stu-id="b5583-113">Expand the General section.</span></span>
5. <span data-ttu-id="b5583-114">在“站点”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="b5583-114">In the Site field, enter or select a value.</span></span>
6. <span data-ttu-id="b5583-115">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="b5583-115">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="b5583-116">在“仓库”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="b5583-116">In the Warehouse field, enter or select a value.</span></span>
8. <span data-ttu-id="b5583-117">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="b5583-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="b5583-118">在“银行文档类型”字段中，选择“保函”。</span><span class="sxs-lookup"><span data-stu-id="b5583-118">In the Bank document type field, select 'Letter of guarantee'.</span></span>
10. <span data-ttu-id="b5583-119">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="b5583-119">Click OK.</span></span>
11. <span data-ttu-id="b5583-120">在“物料编号”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="b5583-120">In the Item number field, enter or select a value.</span></span>
12. <span data-ttu-id="b5583-121">在“单位价格”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="b5583-121">In the Unit price field, enter a number.</span></span>
13. <span data-ttu-id="b5583-122">展开“行明细”部分。</span><span class="sxs-lookup"><span data-stu-id="b5583-122">Expand the Line details section.</span></span>
14. <span data-ttu-id="b5583-123">单击“交货”选项卡。</span><span class="sxs-lookup"><span data-stu-id="b5583-123">Click the Delivery tab.</span></span>
    * <span data-ttu-id="b5583-124">说明：选择“交货日期控制 = 无”</span><span class="sxs-lookup"><span data-stu-id="b5583-124">Note: Select Delivery date control = None</span></span>  
15. <span data-ttu-id="b5583-125">在“请求装运日期”字段中，输入一个日期。</span><span class="sxs-lookup"><span data-stu-id="b5583-125">In the Requested ship date field, enter a date.</span></span>
16. <span data-ttu-id="b5583-126">在“确认装运日期”字段中，输入一个日期。</span><span class="sxs-lookup"><span data-stu-id="b5583-126">In the Confirmed ship date field, enter a date.</span></span>

## <a name="process-letter-of-guarantee_request"></a><span data-ttu-id="b5583-127">处理保函_请求</span><span class="sxs-lookup"><span data-stu-id="b5583-127">Process letter of guarantee_Request</span></span>
1. <span data-ttu-id="b5583-128">在“操作窗格”上单击“管理”。</span><span class="sxs-lookup"><span data-stu-id="b5583-128">On the Action Pane, click Manage.</span></span>
2. <span data-ttu-id="b5583-129">单击“保函”。</span><span class="sxs-lookup"><span data-stu-id="b5583-129">Click Letter of guarantee.</span></span>
3. <span data-ttu-id="b5583-130">在“操作窗格”上单击“保函”。</span><span class="sxs-lookup"><span data-stu-id="b5583-130">On the Action Pane, click Letter of guarantee.</span></span>
4. <span data-ttu-id="b5583-131">单击“请求”打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="b5583-131">Click Request to open the drop dialog.</span></span>
5. <span data-ttu-id="b5583-132">在“类型”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="b5583-132">In the Type field, enter or select a value.</span></span>
6. <span data-ttu-id="b5583-133">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="b5583-133">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="b5583-134">在“值”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="b5583-134">In the Value field, enter a number.</span></span>
8. <span data-ttu-id="b5583-135">在“到期日期”字段中，输入日期和时间。</span><span class="sxs-lookup"><span data-stu-id="b5583-135">In the Expiration date field, enter a date and time.</span></span>
9. <span data-ttu-id="b5583-136">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="b5583-136">Click OK.</span></span>
10. <span data-ttu-id="b5583-137">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="b5583-137">Close the page.</span></span>

## <a name="process-letter-of-guarantee_submit-to-bank"></a><span data-ttu-id="b5583-138">处理保函_提交至银行</span><span class="sxs-lookup"><span data-stu-id="b5583-138">Process letter of guarantee_Submit to bank</span></span>
1. <span data-ttu-id="b5583-139">转到“现金和银行管理”>“保函”>“保函”。</span><span class="sxs-lookup"><span data-stu-id="b5583-139">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
2. <span data-ttu-id="b5583-140">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="b5583-140">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="b5583-141">单击“提交至银行”以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="b5583-141">Click Submit to bank to open the drop dialog.</span></span>
4. <span data-ttu-id="b5583-142">在“银行帐户”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="b5583-142">In the Bank account field, enter or select a value.</span></span>
5. <span data-ttu-id="b5583-143">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="b5583-143">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="b5583-144">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="b5583-144">Click OK.</span></span>

## <a name="process-letter-of-guarantee_receive-from-bank"></a><span data-ttu-id="b5583-145">处理保函_从银行处收到</span><span class="sxs-lookup"><span data-stu-id="b5583-145">Process letter of guarantee_Receive from bank</span></span>
1. <span data-ttu-id="b5583-146">单击“从银行处收到”以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="b5583-146">Click Receive from bank to open the drop dialog.</span></span>
2. <span data-ttu-id="b5583-147">在“银行号码”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="b5583-147">In the Bank number field, type a value.</span></span>
    * <span data-ttu-id="b5583-148">核实“毛利和费用”字段中所计算出的值。</span><span class="sxs-lookup"><span data-stu-id="b5583-148">Verify the values in the calculated Margin and Expense fields.</span></span>  
3. <span data-ttu-id="b5583-149">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="b5583-149">Click OK.</span></span>
4. <span data-ttu-id="b5583-150">展开“行为”部分。</span><span class="sxs-lookup"><span data-stu-id="b5583-150">Expand the Actions section.</span></span>
    * <span data-ttu-id="b5583-151">核实“从银行处收到”记录。</span><span class="sxs-lookup"><span data-stu-id="b5583-151">Verify the 'Receive from bank' record.</span></span>  
5. <span data-ttu-id="b5583-152">单击以访问“日记帐批号”字段中的链接。</span><span class="sxs-lookup"><span data-stu-id="b5583-152">Click to follow the link in the Journal batch number field.</span></span>
6. <span data-ttu-id="b5583-153">单击“行”。</span><span class="sxs-lookup"><span data-stu-id="b5583-153">Click Lines.</span></span>
    * <span data-ttu-id="b5583-154">核实日记帐条目的过帐信息。</span><span class="sxs-lookup"><span data-stu-id="b5583-154">Verify the posting of journal entries.</span></span>  
7. <span data-ttu-id="b5583-155">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="b5583-155">Close the page.</span></span>

## <a name="process-letter-of-guarantee_give-to-beneficiary"></a><span data-ttu-id="b5583-156">处理保函_给受益人</span><span class="sxs-lookup"><span data-stu-id="b5583-156">Process letter of guarantee_Give to beneficiary</span></span>
1. <span data-ttu-id="b5583-157">转到应收帐项目>订单>所有销售订单。</span><span class="sxs-lookup"><span data-stu-id="b5583-157">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="b5583-158">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="b5583-158">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="b5583-159">在“操作窗格”上单击“管理”。</span><span class="sxs-lookup"><span data-stu-id="b5583-159">On the Action Pane, click Manage.</span></span>
4. <span data-ttu-id="b5583-160">单击“保函”。</span><span class="sxs-lookup"><span data-stu-id="b5583-160">Click Letter of guarantee.</span></span>
5. <span data-ttu-id="b5583-161">在“操作窗格”上单击“保函”。</span><span class="sxs-lookup"><span data-stu-id="b5583-161">On the Action Pane, click Letter of guarantee.</span></span>
6. <span data-ttu-id="b5583-162">单击“给受益人”以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="b5583-162">Click Give to beneficiary to open the drop dialog.</span></span>
7. <span data-ttu-id="b5583-163">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="b5583-163">Click OK.</span></span>
8. <span data-ttu-id="b5583-164">转到“现金和银行管理”>“保函”>“保函”。</span><span class="sxs-lookup"><span data-stu-id="b5583-164">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
9. <span data-ttu-id="b5583-165">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="b5583-165">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="b5583-166">单击“给受益人”以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="b5583-166">Click Give to beneficiary to open the drop dialog.</span></span>
11. <span data-ttu-id="b5583-167">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="b5583-167">Click OK.</span></span>
12. <span data-ttu-id="b5583-168">展开“行为”部分。</span><span class="sxs-lookup"><span data-stu-id="b5583-168">Expand the Actions section.</span></span>
    * <span data-ttu-id="b5583-169">验证“给受益人”记录。</span><span class="sxs-lookup"><span data-stu-id="b5583-169">Validate the 'Give to beneficiary' record.</span></span>  

## <a name="process-letter-of-guarantee_increase-value"></a><span data-ttu-id="b5583-170">处理保函_增加值</span><span class="sxs-lookup"><span data-stu-id="b5583-170">Process letter of guarantee_Increase value</span></span>
1. <span data-ttu-id="b5583-171">转到应收帐项目>订单>所有销售订单。</span><span class="sxs-lookup"><span data-stu-id="b5583-171">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="b5583-172">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="b5583-172">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="b5583-173">在“操作窗格”上单击“管理”。</span><span class="sxs-lookup"><span data-stu-id="b5583-173">On the Action Pane, click Manage.</span></span>
4. <span data-ttu-id="b5583-174">单击“保函”。</span><span class="sxs-lookup"><span data-stu-id="b5583-174">Click Letter of guarantee.</span></span>
5. <span data-ttu-id="b5583-175">在“操作窗格”上单击“保函”。</span><span class="sxs-lookup"><span data-stu-id="b5583-175">On the Action Pane, click Letter of guarantee.</span></span>
6. <span data-ttu-id="b5583-176">单击“增加值”以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="b5583-176">Click Increase value to open the drop dialog.</span></span>
7. <span data-ttu-id="b5583-177">在“添加值”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="b5583-177">In the Value to add field, enter a number.</span></span>
8. <span data-ttu-id="b5583-178">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="b5583-178">Click OK.</span></span>
9. <span data-ttu-id="b5583-179">转到“现金和银行管理”>“保函”>“保函”。</span><span class="sxs-lookup"><span data-stu-id="b5583-179">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
10. <span data-ttu-id="b5583-180">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="b5583-180">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="b5583-181">单击“增加值”以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="b5583-181">Click Increase value to open the drop dialog.</span></span>
12. <span data-ttu-id="b5583-182">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="b5583-182">Click OK.</span></span>
13. <span data-ttu-id="b5583-183">展开“行为”部分。</span><span class="sxs-lookup"><span data-stu-id="b5583-183">Expand the Actions section.</span></span>
    * <span data-ttu-id="b5583-184">核实“增加值”记录。</span><span class="sxs-lookup"><span data-stu-id="b5583-184">Verify the 'Increase value' record.</span></span>  
14. <span data-ttu-id="b5583-185">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="b5583-185">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="b5583-186">单击以访问“日记帐批号”字段中的链接。</span><span class="sxs-lookup"><span data-stu-id="b5583-186">Click to follow the link in the Journal batch number field.</span></span>
16. <span data-ttu-id="b5583-187">单击“行”。</span><span class="sxs-lookup"><span data-stu-id="b5583-187">Click Lines.</span></span>
    * <span data-ttu-id="b5583-188">核实已过帐的日记帐条目。</span><span class="sxs-lookup"><span data-stu-id="b5583-188">Verify the posted journal entries.</span></span>  

## <a name="process-letter-of-guarantee_liquidate"></a><span data-ttu-id="b5583-189">处理保函_清算</span><span class="sxs-lookup"><span data-stu-id="b5583-189">Process letter of guarantee_Liquidate</span></span>
1. <span data-ttu-id="b5583-190">转到应收帐项目>订单>所有销售订单。</span><span class="sxs-lookup"><span data-stu-id="b5583-190">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="b5583-191">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="b5583-191">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="b5583-192">在“操作窗格”上单击“管理”。</span><span class="sxs-lookup"><span data-stu-id="b5583-192">On the Action Pane, click Manage.</span></span>
4. <span data-ttu-id="b5583-193">单击“保函”。</span><span class="sxs-lookup"><span data-stu-id="b5583-193">Click Letter of guarantee.</span></span>
5. <span data-ttu-id="b5583-194">在“操作窗格”上单击“保函”。</span><span class="sxs-lookup"><span data-stu-id="b5583-194">On the Action Pane, click Letter of guarantee.</span></span>
6. <span data-ttu-id="b5583-195">单击“清算”以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="b5583-195">Click Liquidate to open the drop dialog.</span></span>
7. <span data-ttu-id="b5583-196">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="b5583-196">Click OK.</span></span>
8. <span data-ttu-id="b5583-197">转到“现金和银行管理”>“保函”>“保函”。</span><span class="sxs-lookup"><span data-stu-id="b5583-197">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
9. <span data-ttu-id="b5583-198">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="b5583-198">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="b5583-199">单击“清算”以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="b5583-199">Click Liquidate to open the drop dialog.</span></span>
11. <span data-ttu-id="b5583-200">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="b5583-200">Click OK.</span></span>
12. <span data-ttu-id="b5583-201">展开“行为”部分。</span><span class="sxs-lookup"><span data-stu-id="b5583-201">Expand the Actions section.</span></span>
    * <span data-ttu-id="b5583-202">核实“清算”记录。</span><span class="sxs-lookup"><span data-stu-id="b5583-202">Verify the 'Liquidate' record.</span></span>  
13. <span data-ttu-id="b5583-203">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="b5583-203">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="b5583-204">单击以访问“日记帐批号”字段中的链接。</span><span class="sxs-lookup"><span data-stu-id="b5583-204">Click to follow the link in the Journal batch number field.</span></span>
15. <span data-ttu-id="b5583-205">单击“行”。</span><span class="sxs-lookup"><span data-stu-id="b5583-205">Click Lines.</span></span>
    * <span data-ttu-id="b5583-206">核实已过帐的日记帐条目。</span><span class="sxs-lookup"><span data-stu-id="b5583-206">Verify the posted journal entries.</span></span>  
16. <span data-ttu-id="b5583-207">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="b5583-207">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]