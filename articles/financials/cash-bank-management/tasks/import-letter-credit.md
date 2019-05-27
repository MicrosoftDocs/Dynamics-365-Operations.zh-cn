---
title: 导入信用证
description: 该过程介绍了导入信用证的流程。
author: kweekley
manager: AnnBe
ms.date: 02/28/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, VendBankAccounts, PurchTable, PurchCreateOrder, InventItemIdLookupPurchase, BankLCImport,  PurchEditLines, VendEditInvoice, SrsReportViewerForm, LedgerJournalTable, LedgerJournalTransVendPaym, VendOpenTrans, SysQueryForm, BankAccountTableLookUp
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3d5539fbd17c880d8bbadd47444c9cc53fce039c
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/15/2019
ms.locfileid: "1566286"
---
# <a name="import-letter-of-credit"></a><span data-ttu-id="faf6b-103">导入信用证</span><span class="sxs-lookup"><span data-stu-id="faf6b-103">Import letter of credit</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="faf6b-104">该过程介绍了导入信用证的流程。</span><span class="sxs-lookup"><span data-stu-id="faf6b-104">This procedure walks through the process of importing a letter of credit.</span></span> <span data-ttu-id="faf6b-105">在完成该过程前必须完成以下设置：银行贷款、过帐模板、银行贷款协议和供应商银行详细信息。</span><span class="sxs-lookup"><span data-stu-id="faf6b-105">The following must be set up before completing this procedure: bank facilities, posting profiles, a bank facility agreement and vendor bank details.</span></span>

<span data-ttu-id="faf6b-106">该程序适用于 USMF 演示公司。</span><span class="sxs-lookup"><span data-stu-id="faf6b-106">This procedure uses the USMF demo company.</span></span>


## <a name="create-a-purchase-order-with-letter-of-credit"></a><span data-ttu-id="faf6b-107">创建一个“信用证采购订单”</span><span class="sxs-lookup"><span data-stu-id="faf6b-107">Create a Purchase order with Letter of credit</span></span>
1. <span data-ttu-id="faf6b-108">转到“应付账款”>“采购订单”>“所有采购订单”。</span><span class="sxs-lookup"><span data-stu-id="faf6b-108">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="faf6b-109">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="faf6b-109">Click New.</span></span>
3. <span data-ttu-id="faf6b-110">在“供应商帐户”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="faf6b-110">In the Vendor account field, enter or select a value.</span></span>
4. <span data-ttu-id="faf6b-111">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="faf6b-111">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="faf6b-112">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="faf6b-112">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="faf6b-113">展开“常规”部分。</span><span class="sxs-lookup"><span data-stu-id="faf6b-113">Expand the General section.</span></span>
7. <span data-ttu-id="faf6b-114">在“站点”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="faf6b-114">In the Site field, enter or select a value.</span></span>
8. <span data-ttu-id="faf6b-115">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="faf6b-115">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="faf6b-116">在“仓库”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="faf6b-116">In the Warehouse field, enter or select a value.</span></span>
10. <span data-ttu-id="faf6b-117">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="faf6b-117">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="faf6b-118">在“会计结算日期”字段中，输入一个日期。</span><span class="sxs-lookup"><span data-stu-id="faf6b-118">In the Accounting date field, enter a date.</span></span>
12. <span data-ttu-id="faf6b-119">在“交货日期”字段中，输入一个日期。</span><span class="sxs-lookup"><span data-stu-id="faf6b-119">In the Delivery date field, enter a date.</span></span>
    * <span data-ttu-id="faf6b-120">说明：在“银行单据类型”字段中应选择相关值“信用证”。</span><span class="sxs-lookup"><span data-stu-id="faf6b-120">Note: The 'Bank document type' field should be selected with the value  'Letter of credit'.</span></span>  
13. <span data-ttu-id="faf6b-121">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="faf6b-121">Click OK.</span></span>
14. <span data-ttu-id="faf6b-122">在“物料编号”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="faf6b-122">In the Item number field, enter or select a value.</span></span>
15. <span data-ttu-id="faf6b-123">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="faf6b-123">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="faf6b-124">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="faf6b-124">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="faf6b-125">展开“行详细信息”部分。</span><span class="sxs-lookup"><span data-stu-id="faf6b-125">Expand the Line details section.</span></span>
18. <span data-ttu-id="faf6b-126">单击“交货”选项卡。</span><span class="sxs-lookup"><span data-stu-id="faf6b-126">Click the Delivery tab.</span></span>
19. <span data-ttu-id="faf6b-127">在“交货日期”字段中，输入一个日期。</span><span class="sxs-lookup"><span data-stu-id="faf6b-127">In the Delivery date field, enter a date.</span></span>
20. <span data-ttu-id="faf6b-128">在“确认交货日期”字段中，输入一个日期。</span><span class="sxs-lookup"><span data-stu-id="faf6b-128">In the Confirmed delivery date field, enter a date.</span></span>
21. <span data-ttu-id="faf6b-129">在“单位价格”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="faf6b-129">In the Unit price field, enter a number.</span></span>
    * <span data-ttu-id="faf6b-130">定义信用证的详细信息。</span><span class="sxs-lookup"><span data-stu-id="faf6b-130">Define the Letter of credit details.</span></span>  
22. <span data-ttu-id="faf6b-131">在“操作窗格”上单击“管理”。</span><span class="sxs-lookup"><span data-stu-id="faf6b-131">On the Action Pane, click Manage.</span></span>
23. <span data-ttu-id="faf6b-132">单击“信用证/导入收款单”。</span><span class="sxs-lookup"><span data-stu-id="faf6b-132">Click Letter of credit / import collection.</span></span>
24. <span data-ttu-id="faf6b-133">在“申请日期”字段中，输入一个日期和时间。</span><span class="sxs-lookup"><span data-stu-id="faf6b-133">In the Application date field, enter a date and time.</span></span>
    * <span data-ttu-id="faf6b-134">核实“银行帐户”字段具有基于申请日期默认有效的银行帐户。</span><span class="sxs-lookup"><span data-stu-id="faf6b-134">Verify that the 'Bank account' field has the default active Bank account, which is based on the application date.</span></span>  
25. <span data-ttu-id="faf6b-135">在“银行单据编号”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="faf6b-135">In the Bank document number field, type a value.</span></span>
26. <span data-ttu-id="faf6b-136">在“收到日期”字段中，输入一个日期和时间。</span><span class="sxs-lookup"><span data-stu-id="faf6b-136">In the Date of receipt field, enter a date and time.</span></span>
27. <span data-ttu-id="faf6b-137">展开“银行单据”部分。</span><span class="sxs-lookup"><span data-stu-id="faf6b-137">Expand the Bank document section.</span></span>
28. <span data-ttu-id="faf6b-138">在“到期日期”字段中，输入日期和时间。</span><span class="sxs-lookup"><span data-stu-id="faf6b-138">In the Expiration date field, enter a date and time.</span></span>
29. <span data-ttu-id="faf6b-139">展开“银行详细信息”部分。</span><span class="sxs-lookup"><span data-stu-id="faf6b-139">Expand the Bank details section.</span></span>
30. <span data-ttu-id="faf6b-140">在“通知银行”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="faf6b-140">In the Advising bank field, enter or select a value.</span></span>
31. <span data-ttu-id="faf6b-141">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="faf6b-141">In the list, click the link in the selected row.</span></span>
32. <span data-ttu-id="faf6b-142">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="faf6b-142">Click Save.</span></span>
33. <span data-ttu-id="faf6b-143">单击“提取采购订单装运”。</span><span class="sxs-lookup"><span data-stu-id="faf6b-143">Click Fetch purchase order shipments.</span></span>
34. <span data-ttu-id="faf6b-144">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="faf6b-144">Close the page.</span></span>
35. <span data-ttu-id="faf6b-145">在操作窗格上，单击“采购”。</span><span class="sxs-lookup"><span data-stu-id="faf6b-145">On the Action Pane, click Purchase.</span></span>
36. <span data-ttu-id="faf6b-146">单击“确认”。</span><span class="sxs-lookup"><span data-stu-id="faf6b-146">Click Confirm.</span></span>
37. <span data-ttu-id="faf6b-147">在“操作窗格”上单击“管理”。</span><span class="sxs-lookup"><span data-stu-id="faf6b-147">On the Action Pane, click Manage.</span></span>
38. <span data-ttu-id="faf6b-148">单击“信用证/导入收款单”。</span><span class="sxs-lookup"><span data-stu-id="faf6b-148">Click Letter of credit / import collection.</span></span>
39. <span data-ttu-id="faf6b-149">单击“流程”。</span><span class="sxs-lookup"><span data-stu-id="faf6b-149">Click Process.</span></span>
40. <span data-ttu-id="faf6b-150">单击“确认”。</span><span class="sxs-lookup"><span data-stu-id="faf6b-150">Click Confirm.</span></span>
    * <span data-ttu-id="faf6b-151">核实该融资余额除去了采购订单金额。</span><span class="sxs-lookup"><span data-stu-id="faf6b-151">Verify that the Facility balance reduces the purchase order amount.</span></span>  <span data-ttu-id="faf6b-152">在此示例中，采购金额 = 500.00，融资限制 = 10000.00，因此，融资余额 = 9500.00。</span><span class="sxs-lookup"><span data-stu-id="faf6b-152">In this example, Purchase amount = 500.00,  Facility limit = 10000.00,  therefore, Facility balance = 9500.00.</span></span>  
41. <span data-ttu-id="faf6b-153">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="faf6b-153">Close the page.</span></span>
42. <span data-ttu-id="faf6b-154">在“单位价格”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="faf6b-154">In the Unit price field, enter a number.</span></span>
43. <span data-ttu-id="faf6b-155">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="faf6b-155">Click Save.</span></span>
44. <span data-ttu-id="faf6b-156">在操作窗格上，单击“采购”。</span><span class="sxs-lookup"><span data-stu-id="faf6b-156">On the Action Pane, click Purchase.</span></span>
45. <span data-ttu-id="faf6b-157">单击“确认”。</span><span class="sxs-lookup"><span data-stu-id="faf6b-157">Click Confirm.</span></span>
    * <span data-ttu-id="faf6b-158">根据“单价”的改变修正“信用证”。</span><span class="sxs-lookup"><span data-stu-id="faf6b-158">Amend the Letter of credit, due to the change in Unit price.</span></span>  
46. <span data-ttu-id="faf6b-159">在“操作窗格”上单击“管理”。</span><span class="sxs-lookup"><span data-stu-id="faf6b-159">On the Action Pane, click Manage.</span></span>
47. <span data-ttu-id="faf6b-160">单击“信用证/导入收款单”。</span><span class="sxs-lookup"><span data-stu-id="faf6b-160">Click Letter of credit / import collection.</span></span>
    * <span data-ttu-id="faf6b-161">根据“采购单价”的改变修正信用证。</span><span class="sxs-lookup"><span data-stu-id="faf6b-161">Amend the letter of credit, due to the change in Purchase unit price.</span></span>  
48. <span data-ttu-id="faf6b-162">单击“流程”。</span><span class="sxs-lookup"><span data-stu-id="faf6b-162">Click Process.</span></span>
49. <span data-ttu-id="faf6b-163">单击“修正”。</span><span class="sxs-lookup"><span data-stu-id="faf6b-163">Click Amend.</span></span>
50. <span data-ttu-id="faf6b-164">单击“移除”。</span><span class="sxs-lookup"><span data-stu-id="faf6b-164">Click Remove.</span></span>
51. <span data-ttu-id="faf6b-165">单击“是”。</span><span class="sxs-lookup"><span data-stu-id="faf6b-165">Click Yes.</span></span>
52. <span data-ttu-id="faf6b-166">单击“提取采购订单装运”。</span><span class="sxs-lookup"><span data-stu-id="faf6b-166">Click Fetch purchase order shipments.</span></span>
53. <span data-ttu-id="faf6b-167">单击“流程”。</span><span class="sxs-lookup"><span data-stu-id="faf6b-167">Click Process.</span></span>
54. <span data-ttu-id="faf6b-168">单击“确认”。</span><span class="sxs-lookup"><span data-stu-id="faf6b-168">Click Confirm.</span></span>
    * <span data-ttu-id="faf6b-169">核实该融资余额除去了采购订单金额。</span><span class="sxs-lookup"><span data-stu-id="faf6b-169">Verify that the Facility balance reduces the purchase order amount.</span></span>  <span data-ttu-id="faf6b-170">在此示例中，已编辑的采购金额 = 600.00，融资限制 = 10000.00，因此融资余额 = 9400.00。</span><span class="sxs-lookup"><span data-stu-id="faf6b-170">In this example, edited Purchase amount = 600.00,  Facility limit = 10000.00,  therefore, Facility balance = 9400.00.</span></span>  
55. <span data-ttu-id="faf6b-171">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="faf6b-171">Close the page.</span></span>

## <a name="post-packing-slip"></a><span data-ttu-id="faf6b-172">过帐“装箱单”</span><span class="sxs-lookup"><span data-stu-id="faf6b-172">Post Packing slip</span></span>
1. <span data-ttu-id="faf6b-173">在操作窗格上，单击“接收”。</span><span class="sxs-lookup"><span data-stu-id="faf6b-173">On the Action Pane, click Receive.</span></span>
2. <span data-ttu-id="faf6b-174">单击“产品收据”。</span><span class="sxs-lookup"><span data-stu-id="faf6b-174">Click Product receipt.</span></span>
3. <span data-ttu-id="faf6b-175">在“PurchParm 表格编号”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="faf6b-175">In the PurchParmTable_Num field, type a value.</span></span>
    * <span data-ttu-id="faf6b-176">选择“装运数量”创建相关“信用证”。</span><span class="sxs-lookup"><span data-stu-id="faf6b-176">Select the Shipment number created with reference to the Letter of credit.</span></span>  
4. <span data-ttu-id="faf6b-177">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="faf6b-177">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="faf6b-178">在“产品收货日期”字段中，输入一个日期。</span><span class="sxs-lookup"><span data-stu-id="faf6b-178">In the Product receipt date field, enter a date.</span></span>
6. <span data-ttu-id="faf6b-179">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="faf6b-179">Click OK.</span></span>
7. <span data-ttu-id="faf6b-180">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="faf6b-180">Close the page.</span></span>
8. <span data-ttu-id="faf6b-181">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="faf6b-181">Close the page.</span></span>

## <a name="verify-import-letter-of-credit-status"></a><span data-ttu-id="faf6b-182">核实“导入信用证”状态</span><span class="sxs-lookup"><span data-stu-id="faf6b-182">Verify Import letter of credit status</span></span>
1. <span data-ttu-id="faf6b-183">转到现金和银行管理>信用证>导出信用证和导入催款</span><span class="sxs-lookup"><span data-stu-id="faf6b-183">Go to Cash and bank management > Letters of credit > Import letter of credit and import collection.</span></span>
2. <span data-ttu-id="faf6b-184">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="faf6b-184">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="faf6b-185">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="faf6b-185">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="faf6b-186">核实“导入信用证”状态。</span><span class="sxs-lookup"><span data-stu-id="faf6b-186">Verify the Import letter of credit status.</span></span>     
4. <span data-ttu-id="faf6b-187">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="faf6b-187">Close the page.</span></span>
5. <span data-ttu-id="faf6b-188">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="faf6b-188">Close the page.</span></span>

## <a name="post-purchase-invoice"></a><span data-ttu-id="faf6b-189">过帐采购发票</span><span class="sxs-lookup"><span data-stu-id="faf6b-189">Post purchase invoice</span></span>
1. <span data-ttu-id="faf6b-190">转到“应付账款”>“采购订单”>“所有采购订单”。</span><span class="sxs-lookup"><span data-stu-id="faf6b-190">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
    * <span data-ttu-id="faf6b-191">选择此信用证创建的采购订单。</span><span class="sxs-lookup"><span data-stu-id="faf6b-191">Select the purchase order that was created with letter of credit.</span></span>  
2. <span data-ttu-id="faf6b-192">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="faf6b-192">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="faf6b-193">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="faf6b-193">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="faf6b-194">在操作窗格上，单击“发票”。</span><span class="sxs-lookup"><span data-stu-id="faf6b-194">On the Action Pane, click Invoice.</span></span>
5. <span data-ttu-id="faf6b-195">单击“发票”。</span><span class="sxs-lookup"><span data-stu-id="faf6b-195">Click Invoice.</span></span>
6. <span data-ttu-id="faf6b-196">在“编号”字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="faf6b-196">In the Number field, type a value.</span></span>
7. <span data-ttu-id="faf6b-197">在“装运数量”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="faf6b-197">In the Shipment number field, enter or select a value.</span></span>
8. <span data-ttu-id="faf6b-198">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="faf6b-198">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="faf6b-199">在“发票日期”字段中，输入日期。</span><span class="sxs-lookup"><span data-stu-id="faf6b-199">In the Invoice date field, enter a date.</span></span>
10. <span data-ttu-id="faf6b-200">单击“更新匹配状态”。</span><span class="sxs-lookup"><span data-stu-id="faf6b-200">Click Update match status.</span></span>
11. <span data-ttu-id="faf6b-201">单击“过帐”。</span><span class="sxs-lookup"><span data-stu-id="faf6b-201">Click Post.</span></span>
12. <span data-ttu-id="faf6b-202">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="faf6b-202">Close the page.</span></span>
13. <span data-ttu-id="faf6b-203">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="faf6b-203">Close the page.</span></span>

## <a name="verify-import-letter-of-credit-status"></a><span data-ttu-id="faf6b-204">核实“导入信用证”状态</span><span class="sxs-lookup"><span data-stu-id="faf6b-204">Verify Import letter of credit status</span></span>
1. <span data-ttu-id="faf6b-205">转到现金和银行管理>信用证>导出信用证和导入催款</span><span class="sxs-lookup"><span data-stu-id="faf6b-205">Go to Cash and bank management > Letters of credit > Import letter of credit and import collection.</span></span>
2. <span data-ttu-id="faf6b-206">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="faf6b-206">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="faf6b-207">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="faf6b-207">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="faf6b-208">核实“导入信用证2”。</span><span class="sxs-lookup"><span data-stu-id="faf6b-208">Verify the Import letter of credit2.</span></span>  
    * <span data-ttu-id="faf6b-209">验证：装运状态 = 开具发票的银行融资的详细信息</span><span class="sxs-lookup"><span data-stu-id="faf6b-209">Validate :  Shipment status = Invoiced  Bank facility details</span></span>  
4. <span data-ttu-id="faf6b-210">单击“查看”。</span><span class="sxs-lookup"><span data-stu-id="faf6b-210">Click View.</span></span>
5. <span data-ttu-id="faf6b-211">单击“打印申请”。</span><span class="sxs-lookup"><span data-stu-id="faf6b-211">Click Print application.</span></span>
6. <span data-ttu-id="faf6b-212">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="faf6b-212">Click OK.</span></span>
    * <span data-ttu-id="faf6b-213">核实该“信用证”申请已打印。</span><span class="sxs-lookup"><span data-stu-id="faf6b-213">Verify that the Letter of credit application gets printed.</span></span>  
7. <span data-ttu-id="faf6b-214">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="faf6b-214">Close the page.</span></span>
8. <span data-ttu-id="faf6b-215">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="faf6b-215">Close the page.</span></span>
9. <span data-ttu-id="faf6b-216">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="faf6b-216">Close the page.</span></span>

## <a name="post-vendor-payment-journal-for-the-created-purchase-invoice-with-letter-of-credit"></a><span data-ttu-id="faf6b-217">为创建信用证采购发票过帐“供应商”付款日记帐</span><span class="sxs-lookup"><span data-stu-id="faf6b-217">Post Vendor payment journal for the created purchase invoice with letter of credit</span></span>
1. <span data-ttu-id="faf6b-218">转至“应付账款”>“付款”>“付款日记帐”。</span><span class="sxs-lookup"><span data-stu-id="faf6b-218">Go to Accounts payable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="faf6b-219">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="faf6b-219">Click New.</span></span>
3. <span data-ttu-id="faf6b-220">在“名称”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="faf6b-220">In the Name field, enter or select a value.</span></span>
4. <span data-ttu-id="faf6b-221">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="faf6b-221">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="faf6b-222">单击“行”。</span><span class="sxs-lookup"><span data-stu-id="faf6b-222">Click Lines.</span></span>
6. <span data-ttu-id="faf6b-223">在“日期”字段中，输入一个日期。</span><span class="sxs-lookup"><span data-stu-id="faf6b-223">In the Date field, enter a date.</span></span>
7. <span data-ttu-id="faf6b-224">在“帐户”字段中，指定所需值。</span><span class="sxs-lookup"><span data-stu-id="faf6b-224">In the Account field, specify the desired values.</span></span>
8. <span data-ttu-id="faf6b-225">单击“结算交易记录”。</span><span class="sxs-lookup"><span data-stu-id="faf6b-225">Click Settle transactions.</span></span>
9. <span data-ttu-id="faf6b-226">展开“总计”部分。</span><span class="sxs-lookup"><span data-stu-id="faf6b-226">Expand the Totals section.</span></span>
10. <span data-ttu-id="faf6b-227">在“显示”字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="faf6b-227">In the Show field, select an option.</span></span>
    * <span data-ttu-id="faf6b-228">核实“银行单据编号和装运数量”字段内容已更新。</span><span class="sxs-lookup"><span data-stu-id="faf6b-228">Verify that the Bank document number and Shipment number fields have been updated.</span></span>  
11. <span data-ttu-id="faf6b-229">选择“标记”复选框。</span><span class="sxs-lookup"><span data-stu-id="faf6b-229">Select the Mark check box.</span></span>
12. <span data-ttu-id="faf6b-230">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="faf6b-230">Click OK.</span></span>
13. <span data-ttu-id="faf6b-231">单击“付款”选项卡。</span><span class="sxs-lookup"><span data-stu-id="faf6b-231">Click the Payment tab.</span></span>
    * <span data-ttu-id="faf6b-232">核实“银行单据编号和装运数量”字段内容已更新。</span><span class="sxs-lookup"><span data-stu-id="faf6b-232">Verify that the Bank document number and Shipment number fields have been updated.</span></span>  
14. <span data-ttu-id="faf6b-233">单击“过帐”。</span><span class="sxs-lookup"><span data-stu-id="faf6b-233">Click Post.</span></span>
15. <span data-ttu-id="faf6b-234">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="faf6b-234">Close the page.</span></span>
16. <span data-ttu-id="faf6b-235">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="faf6b-235">Close the page.</span></span>

## <a name="verify-import-letter-of-credit-status-after-invoice-paid"></a><span data-ttu-id="faf6b-236">核实“导入信用证”状态为“发票支付”</span><span class="sxs-lookup"><span data-stu-id="faf6b-236">Verify Import letter of credit status after Invoice paid</span></span>
1. <span data-ttu-id="faf6b-237">转到现金和银行管理>信用证>导出信用证和导入催款</span><span class="sxs-lookup"><span data-stu-id="faf6b-237">Go to Cash and bank management > Letters of credit > Import letter of credit and import collection.</span></span>
2. <span data-ttu-id="faf6b-238">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="faf6b-238">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="faf6b-239">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="faf6b-239">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="faf6b-240">核实“导入信用证”状态。</span><span class="sxs-lookup"><span data-stu-id="faf6b-240">Verify the Import letter of credit status.</span></span>   
4. <span data-ttu-id="faf6b-241">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="faf6b-241">Close the page.</span></span>

## <a name="verify-the-bank-facility-limit-and-utilization-report"></a><span data-ttu-id="faf6b-242">核实“银行融资限制与利用率报告”</span><span class="sxs-lookup"><span data-stu-id="faf6b-242">Verify the Bank facility limit and utilization report</span></span>
1. <span data-ttu-id="faf6b-243">转到现金和银行管理>查询与报告>信用证或担保人</span><span class="sxs-lookup"><span data-stu-id="faf6b-243">Go to Cash and bank management > Inquiries and reports > Letters of credit or guarantee > Bank facilities and utilization report.</span></span>
2. <span data-ttu-id="faf6b-244">扩展“要包括的记录”部分。</span><span class="sxs-lookup"><span data-stu-id="faf6b-244">Expand the Records to include section.</span></span>
3. <span data-ttu-id="faf6b-245">单击“筛选器”。</span><span class="sxs-lookup"><span data-stu-id="faf6b-245">Click Filter.</span></span>
    * <span data-ttu-id="faf6b-246">用所需银行账户定义“条件”字段。</span><span class="sxs-lookup"><span data-stu-id="faf6b-246">Define the Criteria field with the required bank account.</span></span>  
4. <span data-ttu-id="faf6b-247">在“标准”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="faf6b-247">In the Criteria field, enter or select a value.</span></span>
5. <span data-ttu-id="faf6b-248">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="faf6b-248">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="faf6b-249">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="faf6b-249">Click OK.</span></span>
7. <span data-ttu-id="faf6b-250">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="faf6b-250">Click OK.</span></span>
    * <span data-ttu-id="faf6b-251">核实列出交易记录的报表。</span><span class="sxs-lookup"><span data-stu-id="faf6b-251">Verify the report which lists the transactions.</span></span>  
    * <span data-ttu-id="faf6b-252">核实该报告列出的交易记录，包括“银行单据编号”、“融资限制”、已使用金额和融资余额。</span><span class="sxs-lookup"><span data-stu-id="faf6b-252">Verify the report lists the transactions with Bank document number, Facility limit, utilized amount and the facility balance amount.</span></span>  
8. <span data-ttu-id="faf6b-253">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="faf6b-253">Close the page.</span></span>

