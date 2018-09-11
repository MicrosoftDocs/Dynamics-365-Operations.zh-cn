--- 
title: "设置销售佣金规则"
description: "该过程显示如何设置和启用销售佣金计算和跟踪。"
author: omulvad
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CommissionCustomerGroup, CommissionItemGroup, CommissionSalesGroup, CommissionSalesMember, DirPartyLookup, CommissionCalc, InventPosting, CustTable, EcoResProductDetailsExtended
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: f7213341e012d0afc10c31edd2b850ee5e654f6a
ms.contentlocale: zh-cn
ms.lasthandoff: 09/11/2018

---
# <a name="set-up-sales-commission-rules"></a><span data-ttu-id="34543-103">设置销售佣金规则</span><span class="sxs-lookup"><span data-stu-id="34543-103">Set up sales commission rules</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="34543-104">该过程显示如何设置和启用销售佣金计算和跟踪。</span><span class="sxs-lookup"><span data-stu-id="34543-104">This procedure shows you how to set up and enable sales commission calculation and tracking.</span></span> <span data-ttu-id="34543-105">该过程显示如何创建客户和物料佣金组，以及如何链接选定客户和产品到各个组中。</span><span class="sxs-lookup"><span data-stu-id="34543-105">The procedure shows how to create both customer and item commission groups, and then how to link a selected customer and product to the respective groups.</span></span> <span data-ttu-id="34543-106">这些组将用于佣金计算设置中，以创建客户、物料和销售代表组合，这必须与销售订单匹配，以使销售人员有权获得佣金。</span><span class="sxs-lookup"><span data-stu-id="34543-106">Those groups are then used in the commission calculation setup to create a customer, item, and sales representatives combination that must be matched by the sales order to entitle the sales people to a commission.</span></span> <span data-ttu-id="34543-107">客户和物料佣金组的创建为可选项，因为还可为单个客户和/或物料计算佣金。</span><span class="sxs-lookup"><span data-stu-id="34543-107">Creating customer and item commission groups are optional, as the calculation of commission can also be done for an individual customer and/or item.</span></span> <span data-ttu-id="34543-108">您可以使用 USMF 公司演示数据，也可使用您自己的数据运行该过程。</span><span class="sxs-lookup"><span data-stu-id="34543-108">You can run this procedure in demo data company USMF or on your own data.</span></span>


## <a name="set-up-commission-groups-and-commission-rates"></a><span data-ttu-id="34543-109">设置佣金组和佣金比率</span><span class="sxs-lookup"><span data-stu-id="34543-109">Set up commission groups and commission rates</span></span>
1. <span data-ttu-id="34543-110">转到“销售和市场营销”>“佣金”>“佣金的客户组”。</span><span class="sxs-lookup"><span data-stu-id="34543-110">Go to Sales and marketing > Commissions > Customer groups for commission.</span></span>
2. <span data-ttu-id="34543-111">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="34543-111">Click New.</span></span>
3. <span data-ttu-id="34543-112">在“组”字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="34543-112">In the Group field, type a value.</span></span>
4. <span data-ttu-id="34543-113">在“名称”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="34543-113">In the Name field, type a value.</span></span>
5. <span data-ttu-id="34543-114">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="34543-114">Click Save.</span></span>
6. <span data-ttu-id="34543-115">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="34543-115">Close the page.</span></span>
7. <span data-ttu-id="34543-116">转到“销售和市场营销”>“佣金”>“物料组”。</span><span class="sxs-lookup"><span data-stu-id="34543-116">Go to Sales and marketing > Commissions > Item groups.</span></span>
8. <span data-ttu-id="34543-117">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="34543-117">Click New.</span></span>
9. <span data-ttu-id="34543-118">在“组”字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="34543-118">In the Group field, type a value.</span></span>
10. <span data-ttu-id="34543-119">在“名称”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="34543-119">In the Name field, type a value.</span></span>
11. <span data-ttu-id="34543-120">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="34543-120">Close the page.</span></span>
12. <span data-ttu-id="34543-121">转到“销售和市场营销”>“佣金”>“销售组”。</span><span class="sxs-lookup"><span data-stu-id="34543-121">Go to Sales and marketing > Commissions > Sales groups.</span></span>
    * <span data-ttu-id="34543-122">“佣金销售组”指定在与相关销售组相关的客户购买某些物料时，哪些销售代表能够接受佣金。</span><span class="sxs-lookup"><span data-stu-id="34543-122">A Commission sales group specifies the employees in sales representative roles who are eligible to receive a commission when a customer associated with the relevant sales group buys certain items.</span></span>  
    * <span data-ttu-id="34543-123">在演示数据公司 USMF 中，有称为“美国销售代表”的销售组。</span><span class="sxs-lookup"><span data-stu-id="34543-123">In the USMF demo data company, there is a sales group called "Sales reps US."</span></span>  
13. <span data-ttu-id="34543-124">在操作窗格上，单击“常规”。</span><span class="sxs-lookup"><span data-stu-id="34543-124">On the Action Pane, click General.</span></span>
14. <span data-ttu-id="34543-125">单击“销售代表”。</span><span class="sxs-lookup"><span data-stu-id="34543-125">Click Sales rep..</span></span>
    * <span data-ttu-id="34543-126">销售代表页显示与特定佣金组关联的公司销售人员的列表。</span><span class="sxs-lookup"><span data-stu-id="34543-126">The Sales rep. page displays a list of the company's sales people who are associated with a specific commission group.</span></span> <span data-ttu-id="34543-127">您可以将多个销售代表分配到同一组，并将其各自占总佣金的份额定义为百分比值。</span><span class="sxs-lookup"><span data-stu-id="34543-127">You can assign multiple sales representatives to the same group and define their respective share of the total commission fee as a percentage value.</span></span> <span data-ttu-id="34543-128">所有员工的总佣金份额不能超过 100。</span><span class="sxs-lookup"><span data-stu-id="34543-128">The total commission share across all employees must not exceed 100.</span></span>  
15. <span data-ttu-id="34543-129">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="34543-129">In the list, mark the selected row.</span></span>
16. <span data-ttu-id="34543-130">单击“编辑”。</span><span class="sxs-lookup"><span data-stu-id="34543-130">Click Edit.</span></span>
17. <span data-ttu-id="34543-131">设置“佣金份额”为“50”。</span><span class="sxs-lookup"><span data-stu-id="34543-131">Set Commission share to '50'.</span></span>
18. <span data-ttu-id="34543-132">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="34543-132">Click New.</span></span>
19. <span data-ttu-id="34543-133">在“名称”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="34543-133">In the Name field, click the drop-down button to open the lookup.</span></span>
20. <span data-ttu-id="34543-134">使用“快速筛选器”以查找记录。</span><span class="sxs-lookup"><span data-stu-id="34543-134">Use the Quick Filter to find records.</span></span> <span data-ttu-id="34543-135">例如，在“名称”字段中筛选数值“Susan Burk”。</span><span class="sxs-lookup"><span data-stu-id="34543-135">For example, filter on the Name field with a value of 'Susan Burk'.</span></span>
21. <span data-ttu-id="34543-136">单击“选择”。</span><span class="sxs-lookup"><span data-stu-id="34543-136">Click Select.</span></span>
22. <span data-ttu-id="34543-137">设置“佣金份额”为“50”。</span><span class="sxs-lookup"><span data-stu-id="34543-137">Set Commission share to '50'.</span></span>
23. <span data-ttu-id="34543-138">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="34543-138">Click Save.</span></span>
24. <span data-ttu-id="34543-139">转到“销售和市场营销”>“佣金”>“佣金计算”。</span><span class="sxs-lookup"><span data-stu-id="34543-139">Go to Sales and marketing > Commissions > Commission calculation.</span></span>
    * <span data-ttu-id="34543-140">在“佣金计算页”可定义在交易含有预设的客户和产品组合时，员工可接受销售交易的佣金比率。</span><span class="sxs-lookup"><span data-stu-id="34543-140">In the Commission calculation page you define the commission rate that the employee is to receive for a sales transaction when it contains the pre-set combination of customer and product.</span></span> <span data-ttu-id="34543-141">作为佣金比率设置的一部分，必须指定佣金计算基础，以及是否应包括或排除折扣。</span><span class="sxs-lookup"><span data-stu-id="34543-141">As part of the commission rate setup, you must specify the commission calculation basis and whether it should include or exclude discounts.</span></span> <span data-ttu-id="34543-142">您还可以输入佣金比率在此期间有效的有效期。</span><span class="sxs-lookup"><span data-stu-id="34543-142">You can also enter a validity period for when the commission rate is active.</span></span>  
25. <span data-ttu-id="34543-143">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="34543-143">Click New.</span></span>
26. <span data-ttu-id="34543-144">在“物料代码”字段中，选择“组”。</span><span class="sxs-lookup"><span data-stu-id="34543-144">In the Item code field, select 'Group'.</span></span>
27. <span data-ttu-id="34543-145">在“物料关系”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="34543-145">In the Item relation field, click the drop-down button to open the lookup.</span></span>
28. <span data-ttu-id="34543-146">在列表中，查找并选择您先前创建的组。</span><span class="sxs-lookup"><span data-stu-id="34543-146">In the list, find and select the group that you created earlier.</span></span>
29. <span data-ttu-id="34543-147">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="34543-147">In the list, click the link in the selected row.</span></span>
30. <span data-ttu-id="34543-148">在“客户代码”字段中，选择“组”。</span><span class="sxs-lookup"><span data-stu-id="34543-148">In the Customer code field, select 'Group'.</span></span>
31. <span data-ttu-id="34543-149">在“客户关系”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="34543-149">In the Customer relation field, click the drop-down button to open the lookup.</span></span>
32. <span data-ttu-id="34543-150">在列表中，查找并选择您先前设置的组。</span><span class="sxs-lookup"><span data-stu-id="34543-150">In the list, select the group that you set up earlier.</span></span>
33. <span data-ttu-id="34543-151">在“销售代表 关系”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="34543-151">In the Sales rep. relation field, click the drop-down button to open the lookup.</span></span>
34. <span data-ttu-id="34543-152">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="34543-152">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="34543-153">保持勾选“单行折扣前”选项。</span><span class="sxs-lookup"><span data-stu-id="34543-153">Keep the "Before line discount" option.</span></span>  
    * <span data-ttu-id="34543-154">保持勾选“收入”选项作为佣金值计算的基础。</span><span class="sxs-lookup"><span data-stu-id="34543-154">Keep the "Revenue" option as the basis for commission value calculation.</span></span>    
35. <span data-ttu-id="34543-155">在“佣金百分比”字段中，输入数字。</span><span class="sxs-lookup"><span data-stu-id="34543-155">In the Commission percentage field, enter a number.</span></span>
36. <span data-ttu-id="34543-156">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="34543-156">Click Save.</span></span>

## <a name="setting-up-commission-posting"></a><span data-ttu-id="34543-157">设置佣金过帐</span><span class="sxs-lookup"><span data-stu-id="34543-157">Setting up commission posting</span></span>
1. <span data-ttu-id="34543-158">转到“销售和市场营销”>“佣金”>“佣金过帐”。</span><span class="sxs-lookup"><span data-stu-id="34543-158">Go to Sales and marketing > Commissions > Commission posting.</span></span>
    * <span data-ttu-id="34543-159">佣金为应付给员工的费用，且必须设置，以确保正确过帐到总帐的相应帐户中。</span><span class="sxs-lookup"><span data-stu-id="34543-159">Commission fees are payable to the employees and must therefore be set up to ensure correct financial posting to the appropriate accounts in the General ledger.</span></span> <span data-ttu-id="34543-160">这在“佣金过帐”页完成。</span><span class="sxs-lookup"><span data-stu-id="34543-160">This is done in the Commission posting page.</span></span> <span data-ttu-id="34543-161">查看当前公司可用的设置。</span><span class="sxs-lookup"><span data-stu-id="34543-161">Review the setup that is available for the current company.</span></span> <span data-ttu-id="34543-162">通常，佣金金额将过帐到专门的支出帐户以及经专门的应付账款抵消。</span><span class="sxs-lookup"><span data-stu-id="34543-162">Typically, the commission amounts are posted to a dedicated expense account and are offset to a dedicated payable account.</span></span> <span data-ttu-id="34543-163">如果没有设置佣金过帐规则，系统将无法对有资格获得佣金的销售订单开具发票。</span><span class="sxs-lookup"><span data-stu-id="34543-163">If you don't have the commission posting rules set up, the system will fail to complete invoicing of a sales order which has eligible commissions.</span></span>  
2. <span data-ttu-id="34543-164">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="34543-164">Close the page.</span></span>

## <a name="assign-a-commission-group-to-a-customer-and-a-product"></a><span data-ttu-id="34543-165">分配佣金组给客户和产品</span><span class="sxs-lookup"><span data-stu-id="34543-165">Assign a commission group to a customer and a product</span></span>
1. <span data-ttu-id="34543-166">转到“销售和市场营销”>“客户”>“所有客户”。</span><span class="sxs-lookup"><span data-stu-id="34543-166">Go to Sales and marketing > Customers > All customers.</span></span>
2. <span data-ttu-id="34543-167">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="34543-167">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="34543-168">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="34543-168">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="34543-169">单击“编辑”。</span><span class="sxs-lookup"><span data-stu-id="34543-169">Click Edit.</span></span>
5. <span data-ttu-id="34543-170">展开“销售订单默认值”部分。</span><span class="sxs-lookup"><span data-stu-id="34543-170">Expand the Sales order defaults section.</span></span>
6. <span data-ttu-id="34543-171">在“佣金组”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="34543-171">In the Commission group field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="34543-172">在列表中，选择在先前创建的组。</span><span class="sxs-lookup"><span data-stu-id="34543-172">In the list, select the group that you created earlier.</span></span>
8. <span data-ttu-id="34543-173">在“销售组”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="34543-173">In the Sales group field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="34543-174">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="34543-174">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="34543-175">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="34543-175">Click Save.</span></span>
11. <span data-ttu-id="34543-176">转到“产品信息管理”>“产品”>“已发布产品”。</span><span class="sxs-lookup"><span data-stu-id="34543-176">Go to Product information management > Products > Released products.</span></span>
12. <span data-ttu-id="34543-177">使用“快速筛选器”以查找记录。</span><span class="sxs-lookup"><span data-stu-id="34543-177">Use the Quick Filter to find records.</span></span> <span data-ttu-id="34543-178">例如，在“物料编号”字段中筛选数值“T0020”。</span><span class="sxs-lookup"><span data-stu-id="34543-178">For example, filter on the Item number field with a value of 'T0020 '.</span></span>
13. <span data-ttu-id="34543-179">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="34543-179">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="34543-180">单击“编辑”。</span><span class="sxs-lookup"><span data-stu-id="34543-180">Click Edit.</span></span>
15. <span data-ttu-id="34543-181">展开“销售”部分。</span><span class="sxs-lookup"><span data-stu-id="34543-181">Expand the Sell section.</span></span>
16. <span data-ttu-id="34543-182">在“佣金组”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="34543-182">In the Commission group field, click the drop-down button to open the lookup.</span></span>
17. <span data-ttu-id="34543-183">在列表中，选择您先前设置的佣金组。</span><span class="sxs-lookup"><span data-stu-id="34543-183">In the list, select the commission group that you created earlier.</span></span>


