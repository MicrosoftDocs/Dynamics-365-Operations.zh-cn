---
title: 导出信用证
description: 这个流程帮助了解导出信用证的整个过程。
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustTable, CustBankAccounts, DefaultDashboard, SalesTableListPage, SalesCreateOrder, SalesTable, BankLCExport, SalesEditLines,  LedgerJournalTable, LedgerJournalTransCustPaym, CustOpenTrans
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3cd18320ca8505b1357ce505dfb4c94e81aaae91
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/18/2020
ms.locfileid: "3141641"
---
# <a name="export-letter-of-credit"></a><span data-ttu-id="24e42-103">导出信用证</span><span class="sxs-lookup"><span data-stu-id="24e42-103">Export letter of credit</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="24e42-104">这个流程帮助了解导出信用证的整个过程。</span><span class="sxs-lookup"><span data-stu-id="24e42-104">This procedure walks through the process of the Export letter of credit.</span></span>

<span data-ttu-id="24e42-105">信用证是银行签发的协议，在信用证中银行同意代表买家确认付款（如果满足了买家和卖家间的协议条款）。</span><span class="sxs-lookup"><span data-stu-id="24e42-105">A letter of credit is an agreement that is issued by a bank, in which the bank agrees to ensure payment on behalf of the buyer, if the terms of the agreement between the buyer and seller are met.</span></span>



<span data-ttu-id="24e42-106">在运行该过程之前，先运行“设置银行融资和过帐模板”和”信用证创建银行融资协议”过程。</span><span class="sxs-lookup"><span data-stu-id="24e42-106">Run the 'Set up bank facilities and posting profiles' procedure and the 'Letter of Credit_Create a bank facility agreement' procedure prior to this procedure.</span></span> <span data-ttu-id="24e42-107">请选择 USMF 演示公司以成功运行该过程。</span><span class="sxs-lookup"><span data-stu-id="24e42-107">The USMF demo company must be selected in order to run this procedure successfully.</span></span>




## <a name="create-sales-order-for-export-letter-of-credit"></a><span data-ttu-id="24e42-108">创建“导出信用证销售订单”</span><span class="sxs-lookup"><span data-stu-id="24e42-108">Create Sales Order for Export letter of credit</span></span>
1. <span data-ttu-id="24e42-109">转到应收帐项目>订单>所有销售订单。</span><span class="sxs-lookup"><span data-stu-id="24e42-109">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="24e42-110">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="24e42-110">Click New.</span></span>
3. <span data-ttu-id="24e42-111">在“客户帐户”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="24e42-111">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="24e42-112">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="24e42-112">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="24e42-113">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="24e42-113">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="24e42-114">展开或收起“常规”部分。</span><span class="sxs-lookup"><span data-stu-id="24e42-114">Expand or collapse the General section.</span></span>
7. <span data-ttu-id="24e42-115">在“位置”字段中，单击下拉按钮打开查询。</span><span class="sxs-lookup"><span data-stu-id="24e42-115">In the Site field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="24e42-116">选择进货物料的装运“站点”。</span><span class="sxs-lookup"><span data-stu-id="24e42-116">Select the Site where the item to be issued is stocked.</span></span>  
8. <span data-ttu-id="24e42-117">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="24e42-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="24e42-118">在“仓库”字段，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="24e42-118">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="24e42-119">选择进货物料的装运“仓库”。</span><span class="sxs-lookup"><span data-stu-id="24e42-119">Select the Warehouse where item to be issued is stocked.</span></span>  
10. <span data-ttu-id="24e42-120">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="24e42-120">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="24e42-121">说明：此“银行单据编号”字段应选择相关值“信用证”。</span><span class="sxs-lookup"><span data-stu-id="24e42-121">Note: The Bank document type field should be selected with the value 'Letter of credit'.</span></span>  
11. <span data-ttu-id="24e42-122">在“银行单据类型”字段中，选择“信用证”。</span><span class="sxs-lookup"><span data-stu-id="24e42-122">In the Bank document type field, select 'Letter of credit'.</span></span>
12. <span data-ttu-id="24e42-123">展开或折叠“交货”部分。</span><span class="sxs-lookup"><span data-stu-id="24e42-123">Expand or collapse the Delivery section.</span></span>
    * <span data-ttu-id="24e42-124">选择“交货日期管理 = 无”。</span><span class="sxs-lookup"><span data-stu-id="24e42-124">Select Delivery date control = None.</span></span>  
13. <span data-ttu-id="24e42-125">在“请求收货日期”字段中，输入一个日期。</span><span class="sxs-lookup"><span data-stu-id="24e42-125">In the Requested receipt date field, enter a date.</span></span>
14. <span data-ttu-id="24e42-126">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="24e42-126">Click OK.</span></span>
15. <span data-ttu-id="24e42-127">在“物料编号”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="24e42-127">In the Item number field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="24e42-128">选择所需的“装运/售出”物料。</span><span class="sxs-lookup"><span data-stu-id="24e42-128">Select the required item to be Issued/Sold.</span></span>  
16. <span data-ttu-id="24e42-129">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="24e42-129">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="24e42-130">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="24e42-130">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="24e42-131">在“单价”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="24e42-131">In the Unit price field, enter a number.</span></span>
19. <span data-ttu-id="24e42-132">展开或折叠“行详细信息”部分。</span><span class="sxs-lookup"><span data-stu-id="24e42-132">Expand or collapse the Line details section.</span></span>
20. <span data-ttu-id="24e42-133">单击“交货”选项卡。</span><span class="sxs-lookup"><span data-stu-id="24e42-133">Click the Delivery tab.</span></span>
21. <span data-ttu-id="24e42-134">在“请求装运日期”字段中，输入一个日期。</span><span class="sxs-lookup"><span data-stu-id="24e42-134">In the Requested ship date field, enter a date.</span></span>
22. <span data-ttu-id="24e42-135">在“确认装运日期”字段中，输入一个日期。</span><span class="sxs-lookup"><span data-stu-id="24e42-135">In the Confirmed ship date field, enter a date.</span></span>
23. <span data-ttu-id="24e42-136">在“操作窗格”上单击“管理”。</span><span class="sxs-lookup"><span data-stu-id="24e42-136">On the Action Pane, click Manage.</span></span>
24. <span data-ttu-id="24e42-137">单击“信用证”。</span><span class="sxs-lookup"><span data-stu-id="24e42-137">Click Letter of credit.</span></span>
25. <span data-ttu-id="24e42-138">在“银行单据编号”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="24e42-138">In the Bank document number field, type a value.</span></span>
26. <span data-ttu-id="24e42-139">在“到期日期”字段中，输入日期和时间。</span><span class="sxs-lookup"><span data-stu-id="24e42-139">In the Expiration date field, enter a date and time.</span></span>
27. <span data-ttu-id="24e42-140">展开或折叠“银行详细信息”部分。</span><span class="sxs-lookup"><span data-stu-id="24e42-140">Expand or collapse the Bank details section.</span></span>
28. <span data-ttu-id="24e42-141">在“开证银行”字段中，单击下拉按钮打开查找。</span><span class="sxs-lookup"><span data-stu-id="24e42-141">In the Issuing bank field, click the drop-down button to open the lookup.</span></span>
29. <span data-ttu-id="24e42-142">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="24e42-142">In the list, click the link in the selected row.</span></span>
30. <span data-ttu-id="24e42-143">在“通知银行”字段中，单击下拉按钮打开查找。</span><span class="sxs-lookup"><span data-stu-id="24e42-143">In the Advising bank field, click the drop-down button to open the lookup.</span></span>
31. <span data-ttu-id="24e42-144">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="24e42-144">In the list, find and select the desired record.</span></span>
32. <span data-ttu-id="24e42-145">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="24e42-145">In the list, click the link in the selected row.</span></span>
33. <span data-ttu-id="24e42-146">单击“提取订单装运”。</span><span class="sxs-lookup"><span data-stu-id="24e42-146">Click Fetch sales order shipments.</span></span>
34. <span data-ttu-id="24e42-147">单击“开证银行单据”。</span><span class="sxs-lookup"><span data-stu-id="24e42-147">Click Issue bank document.</span></span>
35. <span data-ttu-id="24e42-148">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="24e42-148">Close the page.</span></span>

## <a name="post-packing-slip"></a><span data-ttu-id="24e42-149">过帐“装箱单”</span><span class="sxs-lookup"><span data-stu-id="24e42-149">Post Packing slip</span></span>
1. <span data-ttu-id="24e42-150">在操作窗格中，单击“领料和装箱”。</span><span class="sxs-lookup"><span data-stu-id="24e42-150">On the Action Pane, click Pick and pack.</span></span>
2. <span data-ttu-id="24e42-151">单击“将装箱单过帐”。</span><span class="sxs-lookup"><span data-stu-id="24e42-151">Click Post packing slip.</span></span>
3. <span data-ttu-id="24e42-152">展开或收起“参数”部分。</span><span class="sxs-lookup"><span data-stu-id="24e42-152">Expand or collapse the Parameters section.</span></span>
4. <span data-ttu-id="24e42-153">在“数量”字段中，选择“所有”。</span><span class="sxs-lookup"><span data-stu-id="24e42-153">In the Quantity field, select 'All'.</span></span>
5. <span data-ttu-id="24e42-154">展开或折叠“设置”部分。</span><span class="sxs-lookup"><span data-stu-id="24e42-154">Expand or collapse the Setup section.</span></span>
6. <span data-ttu-id="24e42-155">在“装箱单日期”字段中，输入一个日期。</span><span class="sxs-lookup"><span data-stu-id="24e42-155">In the Packing slip date field, enter a date.</span></span>
7. <span data-ttu-id="24e42-156">选择“装运数”。</span><span class="sxs-lookup"><span data-stu-id="24e42-156">Select the Shipment number.</span></span>
8. <span data-ttu-id="24e42-157">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="24e42-157">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="24e42-158">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="24e42-158">Click OK.</span></span>
10. <span data-ttu-id="24e42-159">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="24e42-159">Click OK.</span></span>

## <a name="post-sales-invoice"></a><span data-ttu-id="24e42-160">过帐销售发票</span><span class="sxs-lookup"><span data-stu-id="24e42-160">Post sales invoice</span></span>
1. <span data-ttu-id="24e42-161">在操作窗格上，单击“发票”。</span><span class="sxs-lookup"><span data-stu-id="24e42-161">On the Action Pane, click Invoice.</span></span>
2. <span data-ttu-id="24e42-162">单击“发票”。</span><span class="sxs-lookup"><span data-stu-id="24e42-162">Click Invoice.</span></span>
3. <span data-ttu-id="24e42-163">展开或折叠“概述”部分。</span><span class="sxs-lookup"><span data-stu-id="24e42-163">Expand or collapse the Overview section.</span></span>
4. <span data-ttu-id="24e42-164">选择“装运数”。</span><span class="sxs-lookup"><span data-stu-id="24e42-164">Select the Shipment number.</span></span>
5. <span data-ttu-id="24e42-165">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="24e42-165">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="24e42-166">展开或折叠“设置”部分。</span><span class="sxs-lookup"><span data-stu-id="24e42-166">Expand or collapse the Setup section.</span></span>
7. <span data-ttu-id="24e42-167">在“发票日期”字段中，输入日期。</span><span class="sxs-lookup"><span data-stu-id="24e42-167">In the Invoice date field, enter a date.</span></span>
8. <span data-ttu-id="24e42-168">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="24e42-168">Click OK.</span></span>
9. <span data-ttu-id="24e42-169">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="24e42-169">Click OK.</span></span>

## <a name="shipment-document-submitted-status"></a><span data-ttu-id="24e42-170">装运单据的提交状态</span><span class="sxs-lookup"><span data-stu-id="24e42-170">Shipment document submitted status</span></span>
1. <span data-ttu-id="24e42-171">在“操作窗格”上单击“管理”。</span><span class="sxs-lookup"><span data-stu-id="24e42-171">On the Action Pane, click Manage.</span></span>
2. <span data-ttu-id="24e42-172">单击“信用证”。</span><span class="sxs-lookup"><span data-stu-id="24e42-172">Click Letter of credit.</span></span>
3. <span data-ttu-id="24e42-173">展开或折叠“行”部分。</span><span class="sxs-lookup"><span data-stu-id="24e42-173">Expand or collapse the Lines section.</span></span>
    * <span data-ttu-id="24e42-174">说明：“文件提交”字段应设置为“是”。</span><span class="sxs-lookup"><span data-stu-id="24e42-174">Note: The 'Document submitted' field should be set to 'Yes'.</span></span>  

## <a name="verify-export-letter-of-credit"></a><span data-ttu-id="24e42-175">核实“导出信用证”</span><span class="sxs-lookup"><span data-stu-id="24e42-175">Verify Export letter of credit</span></span>
1. <span data-ttu-id="24e42-176">转到现金和银行管理>信用证>导出信用证和导入催款</span><span class="sxs-lookup"><span data-stu-id="24e42-176">Go to Cash and bank management > Letters of credit > Export letter of credit and import collection.</span></span>
2. <span data-ttu-id="24e42-177">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="24e42-177">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="24e42-178">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="24e42-178">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="24e42-179">核实“导出信用证”的装运状态为“已开发票”。</span><span class="sxs-lookup"><span data-stu-id="24e42-179">Verify that the Export letter of credit has a Shipment status of 'Invoiced'.</span></span>  

## <a name="customer-payment"></a><span data-ttu-id="24e42-180">客户 - 付款</span><span class="sxs-lookup"><span data-stu-id="24e42-180">Customer payment</span></span>
1. <span data-ttu-id="24e42-181">转到“应收账款”>“付款”>“付款日记帐”。</span><span class="sxs-lookup"><span data-stu-id="24e42-181">Go to Accounts receivable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="24e42-182">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="24e42-182">Click New.</span></span>
3. <span data-ttu-id="24e42-183">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="24e42-183">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="24e42-184">在“名称”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="24e42-184">In the Name field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="24e42-185">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="24e42-185">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="24e42-186">单击“行”。</span><span class="sxs-lookup"><span data-stu-id="24e42-186">Click Lines.</span></span>
7. <span data-ttu-id="24e42-187">在“日期”字段中，输入一个日期。</span><span class="sxs-lookup"><span data-stu-id="24e42-187">In the Date field, enter a date.</span></span>
8. <span data-ttu-id="24e42-188">在“帐户”字段中，指定所需值。</span><span class="sxs-lookup"><span data-stu-id="24e42-188">In the Account field, specify the desired values.</span></span>
9. <span data-ttu-id="24e42-189">单击“结算”。</span><span class="sxs-lookup"><span data-stu-id="24e42-189">Click Settlement.</span></span>
10. <span data-ttu-id="24e42-190">选择“总计”标题上的复选框。</span><span class="sxs-lookup"><span data-stu-id="24e42-190">Select the check box on the header of Totals.</span></span>
    * <span data-ttu-id="24e42-191">说明：设置“显示”字段为“信用证”。</span><span class="sxs-lookup"><span data-stu-id="24e42-191">Note: Set the Show field to 'Letter of credit'.</span></span>  
11. <span data-ttu-id="24e42-192">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="24e42-192">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="24e42-193">选中或取消选择“标记”复选框。</span><span class="sxs-lookup"><span data-stu-id="24e42-193">Select or clear the Mark check box.</span></span>
13. <span data-ttu-id="24e42-194">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="24e42-194">Click OK.</span></span>
14. <span data-ttu-id="24e42-195">单击“付款”选项卡。</span><span class="sxs-lookup"><span data-stu-id="24e42-195">Click the Payment tab.</span></span>
    * <span data-ttu-id="24e42-196">核实“银行单据编号”和“装运数量”的详细信息</span><span class="sxs-lookup"><span data-stu-id="24e42-196">Verify Bank document number and Shipment number details</span></span>  
15. <span data-ttu-id="24e42-197">单击“过帐”。</span><span class="sxs-lookup"><span data-stu-id="24e42-197">Click Post.</span></span>

## <a name="verify-export-letter-of-credit-after-payment"></a><span data-ttu-id="24e42-198">在付款后核实“导出信用证”</span><span class="sxs-lookup"><span data-stu-id="24e42-198">Verify Export letter of credit after payment</span></span>
1. <span data-ttu-id="24e42-199">转到现金和银行管理>信用证>导出信用证和导入催款</span><span class="sxs-lookup"><span data-stu-id="24e42-199">Go to Cash and bank management > Letters of credit > Export letter of credit and import collection.</span></span>
2. <span data-ttu-id="24e42-200">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="24e42-200">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="24e42-201">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="24e42-201">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="24e42-202">核实装运状态 = 已收到付款和余额 = 0.00。</span><span class="sxs-lookup"><span data-stu-id="24e42-202">Verify Shipment status = Payment received and balance amount = 0.00.</span></span>  

