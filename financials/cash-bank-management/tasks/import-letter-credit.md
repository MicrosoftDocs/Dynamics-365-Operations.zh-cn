--- 
title: "导入信用证"
description: "该过程介绍了导入信用证的流程。"
author: kweekley
manager: AnnBe
ms.date: 02/26/2016
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
ms.openlocfilehash: e5bb7b8f285445ae9dc3e1d3cf09eecfc2167398
ms.contentlocale: zh-cn
ms.lasthandoff: 08/29/2017

---
# <a name="import-a-letter-of-credit"></a><span data-ttu-id="37637-103">导入信用证</span><span class="sxs-lookup"><span data-stu-id="37637-103">Import a letter of credit</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="37637-104">该过程介绍了导入信用证的流程。</span><span class="sxs-lookup"><span data-stu-id="37637-104">This procedure walks through the process of importing a letter of credit.</span></span> <span data-ttu-id="37637-105">在完成该过程前必须完成以下设置：银行贷款、过帐模板、银行贷款协议和供应商银行详细信息。</span><span class="sxs-lookup"><span data-stu-id="37637-105">The following must be set up before completing this procedure: bank facilities, posting profiles, a bank facility agreement and vendor bank details.</span></span>

<span data-ttu-id="37637-106">该程序适用于 USMF 演示公司。</span><span class="sxs-lookup"><span data-stu-id="37637-106">This procedure uses the USMF demo company.</span></span>


## <a name="create-a-purchase-order-with-letter-of-credit"></a><span data-ttu-id="37637-107">创建一个“信用证采购订单”</span><span class="sxs-lookup"><span data-stu-id="37637-107">Create a Purchase order with Letter of credit</span></span>
1. <span data-ttu-id="37637-108">转到“应付帐款”>“采购订单”>“所有采购订单”。</span><span class="sxs-lookup"><span data-stu-id="37637-108">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="37637-109">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="37637-109">Click New.</span></span>
3. <span data-ttu-id="37637-110">在“供应商帐户”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="37637-110">In the Vendor account field, enter or select a value.</span></span>
4. <span data-ttu-id="37637-111">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="37637-111">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="37637-112">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="37637-112">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="37637-113">展开“常规”部分。</span><span class="sxs-lookup"><span data-stu-id="37637-113">Expand the General section.</span></span>
7. <span data-ttu-id="37637-114">在“站点”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="37637-114">In the Site field, enter or select a value.</span></span>
8. <span data-ttu-id="37637-115">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="37637-115">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="37637-116">在“仓库”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="37637-116">In the Warehouse field, enter or select a value.</span></span>
10. <span data-ttu-id="37637-117">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="37637-117">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="37637-118">在“会计结算日期”字段中，输入一个日期。</span><span class="sxs-lookup"><span data-stu-id="37637-118">In the Accounting date field, enter a date.</span></span>
12. <span data-ttu-id="37637-119">在“交货日期”字段中，输入一个日期。</span><span class="sxs-lookup"><span data-stu-id="37637-119">In the Delivery date field, enter a date.</span></span>
    * <span data-ttu-id="37637-120">说明：在“银行单据类型”字段中应选择相关值“信用证”。</span><span class="sxs-lookup"><span data-stu-id="37637-120">Note: The 'Bank document type' field should be selected with the value  'Letter of credit'.</span></span>  
13. <span data-ttu-id="37637-121">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="37637-121">Click OK.</span></span>
14. <span data-ttu-id="37637-122">在“物料编号”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="37637-122">In the Item number field, enter or select a value.</span></span>
15. <span data-ttu-id="37637-123">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="37637-123">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="37637-124">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="37637-124">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="37637-125">展开“行详细信息”部分。</span><span class="sxs-lookup"><span data-stu-id="37637-125">Expand the Line details section.</span></span>
18. <span data-ttu-id="37637-126">单击“交货”选项卡。</span><span class="sxs-lookup"><span data-stu-id="37637-126">Click the Delivery tab.</span></span>
19. <span data-ttu-id="37637-127">在“交货日期”字段中，输入一个日期。</span><span class="sxs-lookup"><span data-stu-id="37637-127">In the Delivery date field, enter a date.</span></span>
20. <span data-ttu-id="37637-128">在“确认交货日期”字段中，输入一个日期。</span><span class="sxs-lookup"><span data-stu-id="37637-128">In the Confirmed delivery date field, enter a date.</span></span>
21. <span data-ttu-id="37637-129">在“单位价格”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="37637-129">In the Unit price field, enter a number.</span></span>
    * <span data-ttu-id="37637-130">定义信用证的详细信息。</span><span class="sxs-lookup"><span data-stu-id="37637-130">Define the Letter of credit details.</span></span>  
22. <span data-ttu-id="37637-131">在“操作窗格”上单击“管理”。</span><span class="sxs-lookup"><span data-stu-id="37637-131">On the Action Pane, click Manage.</span></span>
23. <span data-ttu-id="37637-132">单击“信用证/导入收款单”。</span><span class="sxs-lookup"><span data-stu-id="37637-132">Click Letter of credit / import collection.</span></span>
24. <span data-ttu-id="37637-133">在“申请日期”字段中，输入一个日期和时间。</span><span class="sxs-lookup"><span data-stu-id="37637-133">In the Application date field, enter a date and time.</span></span>
    * <span data-ttu-id="37637-134">核实“银行帐户”字段具有基于申请日期默认有效的银行帐户。</span><span class="sxs-lookup"><span data-stu-id="37637-134">Verify that the 'Bank account' field has the default active Bank account, which is based on the application date.</span></span>  
25. <span data-ttu-id="37637-135">在“银行单据编号”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="37637-135">In the Bank document number field, type a value.</span></span>
26. <span data-ttu-id="37637-136">在“收到日期”字段中，输入一个日期和时间。</span><span class="sxs-lookup"><span data-stu-id="37637-136">In the Date of receipt field, enter a date and time.</span></span>
27. <span data-ttu-id="37637-137">展开“银行单据”部分。</span><span class="sxs-lookup"><span data-stu-id="37637-137">Expand the Bank document section.</span></span>
28. <span data-ttu-id="37637-138">在“到期日期”字段中，输入日期和时间。</span><span class="sxs-lookup"><span data-stu-id="37637-138">In the Expiration date field, enter a date and time.</span></span>
29. <span data-ttu-id="37637-139">展开“银行详细信息”部分。</span><span class="sxs-lookup"><span data-stu-id="37637-139">Expand the Bank details section.</span></span>
30. <span data-ttu-id="37637-140">在“通知银行”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="37637-140">In the Advising bank field, enter or select a value.</span></span>
31. <span data-ttu-id="37637-141">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="37637-141">In the list, click the link in the selected row.</span></span>
32. <span data-ttu-id="37637-142">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="37637-142">Click Save.</span></span>
33. <span data-ttu-id="37637-143">单击“提取采购订单装运”。</span><span class="sxs-lookup"><span data-stu-id="37637-143">Click Fetch purchase order shipments.</span></span>
34. <span data-ttu-id="37637-144">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="37637-144">Close the page.</span></span>
35. <span data-ttu-id="37637-145">在操作窗格上，单击“采购”。</span><span class="sxs-lookup"><span data-stu-id="37637-145">On the Action Pane, click Purchase.</span></span>
36. <span data-ttu-id="37637-146">单击“确认”。</span><span class="sxs-lookup"><span data-stu-id="37637-146">Click Confirm.</span></span>
37. <span data-ttu-id="37637-147">在“操作窗格”上单击“管理”。</span><span class="sxs-lookup"><span data-stu-id="37637-147">On the Action Pane, click Manage.</span></span>
38. <span data-ttu-id="37637-148">单击“信用证/导入收款单”。</span><span class="sxs-lookup"><span data-stu-id="37637-148">Click Letter of credit / import collection.</span></span>
39. <span data-ttu-id="37637-149">单击“流程”。</span><span class="sxs-lookup"><span data-stu-id="37637-149">Click Process.</span></span>
40. <span data-ttu-id="37637-150">单击“确认”。</span><span class="sxs-lookup"><span data-stu-id="37637-150">Click Confirm.</span></span>
    * <span data-ttu-id="37637-151">核实该融资余额除去了采购订单金额。</span><span class="sxs-lookup"><span data-stu-id="37637-151">Verify that the Facility balance reduces the purchase order amount.</span></span>  <span data-ttu-id="37637-152">在此示例中，采购金额 = 500.00，融资限制 = 10000.00，因此，融资余额 = 9500.00。</span><span class="sxs-lookup"><span data-stu-id="37637-152">In this example, Purchase amount = 500.00,  Facility limit = 10000.00,  therefore, Facility balance = 9500.00.</span></span>  
41. <span data-ttu-id="37637-153">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="37637-153">Close the page.</span></span>
42. <span data-ttu-id="37637-154">在“单位价格”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="37637-154">In the Unit price field, enter a number.</span></span>
43. <span data-ttu-id="37637-155">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="37637-155">Click Save.</span></span>
44. <span data-ttu-id="37637-156">在操作窗格上，单击“采购”。</span><span class="sxs-lookup"><span data-stu-id="37637-156">On the Action Pane, click Purchase.</span></span>
45. <span data-ttu-id="37637-157">单击“确认”。</span><span class="sxs-lookup"><span data-stu-id="37637-157">Click Confirm.</span></span>
    * <span data-ttu-id="37637-158">根据“单价”的改变修正“信用证”。</span><span class="sxs-lookup"><span data-stu-id="37637-158">Amend the Letter of credit, due to the change in Unit price.</span></span>  
46. <span data-ttu-id="37637-159">在“操作窗格”上单击“管理”。</span><span class="sxs-lookup"><span data-stu-id="37637-159">On the Action Pane, click Manage.</span></span>
47. <span data-ttu-id="37637-160">单击“信用证/导入收款单”。</span><span class="sxs-lookup"><span data-stu-id="37637-160">Click Letter of credit / import collection.</span></span>
    * <span data-ttu-id="37637-161">根据“采购单价”的改变修正信用证。</span><span class="sxs-lookup"><span data-stu-id="37637-161">Amend the letter of credit, due to the change in Purchase unit price.</span></span>  
48. <span data-ttu-id="37637-162">单击“流程”。</span><span class="sxs-lookup"><span data-stu-id="37637-162">Click Process.</span></span>
49. <span data-ttu-id="37637-163">单击“修正”。</span><span class="sxs-lookup"><span data-stu-id="37637-163">Click Amend.</span></span>
50. <span data-ttu-id="37637-164">单击“移除”。</span><span class="sxs-lookup"><span data-stu-id="37637-164">Click Remove.</span></span>
51. <span data-ttu-id="37637-165">单击“是”。</span><span class="sxs-lookup"><span data-stu-id="37637-165">Click Yes.</span></span>
52. <span data-ttu-id="37637-166">单击“提取采购订单装运”。</span><span class="sxs-lookup"><span data-stu-id="37637-166">Click Fetch purchase order shipments.</span></span>
53. <span data-ttu-id="37637-167">单击“流程”。</span><span class="sxs-lookup"><span data-stu-id="37637-167">Click Process.</span></span>
54. <span data-ttu-id="37637-168">单击“确认”。</span><span class="sxs-lookup"><span data-stu-id="37637-168">Click Confirm.</span></span>
    * <span data-ttu-id="37637-169">核实该融资余额除去了采购订单金额。</span><span class="sxs-lookup"><span data-stu-id="37637-169">Verify that the Facility balance reduces the purchase order amount.</span></span>  <span data-ttu-id="37637-170">在此示例中，已编辑的采购金额 = 600.00，融资限制 = 10000.00，因此融资余额 = 9400.00。</span><span class="sxs-lookup"><span data-stu-id="37637-170">In this example, edited Purchase amount = 600.00,  Facility limit = 10000.00,  therefore, Facility balance = 9400.00.</span></span>  
55. <span data-ttu-id="37637-171">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="37637-171">Close the page.</span></span>

## <a name="post-packing-slip"></a><span data-ttu-id="37637-172">过帐“装箱单”</span><span class="sxs-lookup"><span data-stu-id="37637-172">Post Packing slip</span></span>
1. <span data-ttu-id="37637-173">在操作窗格上，单击“接收”。</span><span class="sxs-lookup"><span data-stu-id="37637-173">On the Action Pane, click Receive.</span></span>
2. <span data-ttu-id="37637-174">单击“产品收据”。</span><span class="sxs-lookup"><span data-stu-id="37637-174">Click Product receipt.</span></span>
3. <span data-ttu-id="37637-175">在“PurchParm 表格编号”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="37637-175">In the PurchParmTable_Num field, type a value.</span></span>
    * <span data-ttu-id="37637-176">选择“装运数量”创建相关“信用证”。</span><span class="sxs-lookup"><span data-stu-id="37637-176">Select the Shipment number created with reference to the Letter of credit.</span></span>  
4. <span data-ttu-id="37637-177">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="37637-177">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="37637-178">在“产品收货日期”字段中，输入一个日期。</span><span class="sxs-lookup"><span data-stu-id="37637-178">In the Product receipt date field, enter a date.</span></span>
6. <span data-ttu-id="37637-179">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="37637-179">Click OK.</span></span>
7. <span data-ttu-id="37637-180">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="37637-180">Close the page.</span></span>
8. <span data-ttu-id="37637-181">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="37637-181">Close the page.</span></span>

## <a name="verify-import-letter-of-credit-status"></a><span data-ttu-id="37637-182">核实“导入信用证”状态</span><span class="sxs-lookup"><span data-stu-id="37637-182">Verify Import letter of credit status</span></span>
1. <span data-ttu-id="37637-183">转到现金和银行管理>信用证>导出信用证和导入催款</span><span class="sxs-lookup"><span data-stu-id="37637-183">Go to Cash and bank management > Letters of credit > Import letter of credit and import collection.</span></span>
2. <span data-ttu-id="37637-184">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="37637-184">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="37637-185">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="37637-185">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="37637-186">核实“导入信用证”状态。</span><span class="sxs-lookup"><span data-stu-id="37637-186">Verify the Import letter of credit status.</span></span>  
4. <span data-ttu-id="37637-187">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="37637-187">Close the page.</span></span>
5. <span data-ttu-id="37637-188">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="37637-188">Close the page.</span></span>

## <a name="post-purchase-invoice"></a><span data-ttu-id="37637-189">过帐采购发票</span><span class="sxs-lookup"><span data-stu-id="37637-189">Post purchase invoice</span></span>
1. <span data-ttu-id="37637-190">转到“应付帐款”>“采购订单”>“所有采购订单”。</span><span class="sxs-lookup"><span data-stu-id="37637-190">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
    * <span data-ttu-id="37637-191">选择此信用证创建的采购订单。</span><span class="sxs-lookup"><span data-stu-id="37637-191">Select the purchase order that was created with letter of credit.</span></span>  
2. <span data-ttu-id="37637-192">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="37637-192">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="37637-193">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="37637-193">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="37637-194">在操作窗格上，单击“发票”。</span><span class="sxs-lookup"><span data-stu-id="37637-194">On the Action Pane, click Invoice.</span></span>
5. <span data-ttu-id="37637-195">单击“发票”。</span><span class="sxs-lookup"><span data-stu-id="37637-195">Click Invoice.</span></span>
6. <span data-ttu-id="37637-196">在“编号”字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="37637-196">In the Number field, type a value.</span></span>
7. <span data-ttu-id="37637-197">在“装运数量”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="37637-197">In the Shipment number field, enter or select a value.</span></span>
8. <span data-ttu-id="37637-198">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="37637-198">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="37637-199">在“发票日期”字段中，输入日期。</span><span class="sxs-lookup"><span data-stu-id="37637-199">In the Invoice date field, enter a date.</span></span>
10. <span data-ttu-id="37637-200">单击“更新匹配状态”。</span><span class="sxs-lookup"><span data-stu-id="37637-200">Click Update match status.</span></span>
11. <span data-ttu-id="37637-201">单击“过帐”。</span><span class="sxs-lookup"><span data-stu-id="37637-201">Click Post.</span></span>
12. <span data-ttu-id="37637-202">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="37637-202">Close the page.</span></span>
13. <span data-ttu-id="37637-203">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="37637-203">Close the page.</span></span>

## <a name="verify-import-letter-of-credit-status"></a><span data-ttu-id="37637-204">核实“导入信用证”状态</span><span class="sxs-lookup"><span data-stu-id="37637-204">Verify Import letter of credit status</span></span>
1. <span data-ttu-id="37637-205">转到现金和银行管理>信用证>导出信用证和导入催款</span><span class="sxs-lookup"><span data-stu-id="37637-205">Go to Cash and bank management > Letters of credit > Import letter of credit and import collection.</span></span>
2. <span data-ttu-id="37637-206">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="37637-206">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="37637-207">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="37637-207">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="37637-208">核实“导入信用证2”。</span><span class="sxs-lookup"><span data-stu-id="37637-208">Verify the Import letter of credit2.</span></span>  
    * <span data-ttu-id="37637-209">验证：装运状态 = 开具发票的银行融资的详细信息</span><span class="sxs-lookup"><span data-stu-id="37637-209">Validate :  Shipment status = Invoiced  Bank facility details</span></span>  
4. <span data-ttu-id="37637-210">单击“查看”。</span><span class="sxs-lookup"><span data-stu-id="37637-210">Click View.</span></span>
5. <span data-ttu-id="37637-211">单击“打印申请”。</span><span class="sxs-lookup"><span data-stu-id="37637-211">Click Print application.</span></span>
6. <span data-ttu-id="37637-212">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="37637-212">Click OK.</span></span>
    * <span data-ttu-id="37637-213">核实该“信用证”申请已打印。</span><span class="sxs-lookup"><span data-stu-id="37637-213">Verify that the Letter of credit application gets printed.</span></span>  
7. <span data-ttu-id="37637-214">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="37637-214">Close the page.</span></span>
8. <span data-ttu-id="37637-215">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="37637-215">Close the page.</span></span>
9. <span data-ttu-id="37637-216">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="37637-216">Close the page.</span></span>

## <a name="post-vendor-payment-journal-for-the-created-purchase-invoice-with-letter-of-credit"></a><span data-ttu-id="37637-217">为创建信用证采购发票过帐“供应商”付款日记帐</span><span class="sxs-lookup"><span data-stu-id="37637-217">Post Vendor payment journal for the created purchase invoice with letter of credit</span></span>
1. <span data-ttu-id="37637-218">转至“应付帐款”>“付款”>“付款日记帐”。</span><span class="sxs-lookup"><span data-stu-id="37637-218">Go to Accounts payable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="37637-219">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="37637-219">Click New.</span></span>
3. <span data-ttu-id="37637-220">在“名称”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="37637-220">In the Name field, enter or select a value.</span></span>
4. <span data-ttu-id="37637-221">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="37637-221">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="37637-222">单击“行”。</span><span class="sxs-lookup"><span data-stu-id="37637-222">Click Lines.</span></span>
6. <span data-ttu-id="37637-223">在“日期”字段中，输入一个日期。</span><span class="sxs-lookup"><span data-stu-id="37637-223">In the Date field, enter a date.</span></span>
7. <span data-ttu-id="37637-224">在“帐户”字段中，指定所需值。</span><span class="sxs-lookup"><span data-stu-id="37637-224">In the Account field, specify the desired values.</span></span>
8. <span data-ttu-id="37637-225">单击“结算交易记录”。</span><span class="sxs-lookup"><span data-stu-id="37637-225">Click Settle transactions.</span></span>
9. <span data-ttu-id="37637-226">展开“总计”部分。</span><span class="sxs-lookup"><span data-stu-id="37637-226">Expand the Totals section.</span></span>
10. <span data-ttu-id="37637-227">在“显示”字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="37637-227">In the Show field, select an option.</span></span>
    * <span data-ttu-id="37637-228">核实“银行单据编号和装运数量”字段内容已更新。</span><span class="sxs-lookup"><span data-stu-id="37637-228">Verify that the Bank document number and Shipment number fields have been updated.</span></span>  
11. <span data-ttu-id="37637-229">选择“标记”复选框。</span><span class="sxs-lookup"><span data-stu-id="37637-229">Select the Mark check box.</span></span>
12. <span data-ttu-id="37637-230">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="37637-230">Click OK.</span></span>
13. <span data-ttu-id="37637-231">单击“付款”选项卡。</span><span class="sxs-lookup"><span data-stu-id="37637-231">Click the Payment tab.</span></span>
    * <span data-ttu-id="37637-232">核实“银行单据编号和装运数量”字段内容已更新。</span><span class="sxs-lookup"><span data-stu-id="37637-232">Verify that the Bank document number and Shipment number fields have been updated.</span></span>  
14. <span data-ttu-id="37637-233">单击“过帐”。</span><span class="sxs-lookup"><span data-stu-id="37637-233">Click Post.</span></span>
15. <span data-ttu-id="37637-234">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="37637-234">Close the page.</span></span>
16. <span data-ttu-id="37637-235">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="37637-235">Close the page.</span></span>

## <a name="verify-import-letter-of-credit-status-after-invoice-paid"></a><span data-ttu-id="37637-236">核实“导入信用证”状态为“发票支付”</span><span class="sxs-lookup"><span data-stu-id="37637-236">Verify Import letter of credit status after Invoice paid</span></span>
1. <span data-ttu-id="37637-237">转到现金和银行管理>信用证>导出信用证和导入催款</span><span class="sxs-lookup"><span data-stu-id="37637-237">Go to Cash and bank management > Letters of credit > Import letter of credit and import collection.</span></span>
2. <span data-ttu-id="37637-238">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="37637-238">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="37637-239">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="37637-239">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="37637-240">核实“导入信用证”状态。</span><span class="sxs-lookup"><span data-stu-id="37637-240">Verify the Import letter of credit status.</span></span>   
4. <span data-ttu-id="37637-241">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="37637-241">Close the page.</span></span>

## <a name="verify-the-bank-facility-limit-and-utilization-report"></a><span data-ttu-id="37637-242">核实“银行融资限制与利用率报告”</span><span class="sxs-lookup"><span data-stu-id="37637-242">Verify the Bank facility limit and utilization report</span></span>
1. <span data-ttu-id="37637-243">转到现金和银行管理>查询与报告>信用证或担保人</span><span class="sxs-lookup"><span data-stu-id="37637-243">Go to Cash and bank management > Inquiries and reports > Letters of credit or guarantee > Bank facilities and utilization report.</span></span>
2. <span data-ttu-id="37637-244">扩展“要包括的记录”部分。</span><span class="sxs-lookup"><span data-stu-id="37637-244">Expand the Records to include section.</span></span>
3. <span data-ttu-id="37637-245">单击“筛选器”。</span><span class="sxs-lookup"><span data-stu-id="37637-245">Click Filter.</span></span>
    * <span data-ttu-id="37637-246">用所需银行账户定义“条件”字段。</span><span class="sxs-lookup"><span data-stu-id="37637-246">Define the Criteria field with the required bank account.</span></span>  
4. <span data-ttu-id="37637-247">在“标准”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="37637-247">In the Criteria field, enter or select a value.</span></span>
5. <span data-ttu-id="37637-248">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="37637-248">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="37637-249">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="37637-249">Click OK.</span></span>
7. <span data-ttu-id="37637-250">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="37637-250">Click OK.</span></span>
    * <span data-ttu-id="37637-251">核实列出交易记录的报表。</span><span class="sxs-lookup"><span data-stu-id="37637-251">Verify the report which lists the transactions.</span></span>  
    * <span data-ttu-id="37637-252">核实该报告列出的交易记录，包括“银行单据编号”、“融资限制”、已使用金额和融资余额。</span><span class="sxs-lookup"><span data-stu-id="37637-252">Verify the report lists the transactions with Bank document number, Facility limit, utilized amount and the facility balance amount.</span></span>  
8. <span data-ttu-id="37637-253">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="37637-253">Close the page.</span></span>


