---
title: 从其他模块（如销售发票）过帐凭证
description: 可以从总帐、库存变动日记帐、销售发票和采购发票过帐中国式凭证。
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventJournalMovement, InventJournalCreate, InventItemIdLookupSimple, InventLocationIdLookup, InventProductDimensionLookup, DimensionLookup, InventTrans, SalesTableListPage, SalesCreateOrder, SalesTable, SalesEditLines,  CustInvoiceJournal, CustTrans
audience: Application User
ms.reviewer: kfend
ms.search.region: China (PRC)
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2bb172d595f7eb1b3c77b002e9f881182b385d49
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5820489"
---
# <a name="post-vouchers-from-other-modules-like-sales-invoices"></a><span data-ttu-id="91d0b-103">从其他模块（如销售发票）过帐凭证</span><span class="sxs-lookup"><span data-stu-id="91d0b-103">Post vouchers from other modules, like sales invoices</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="91d0b-104">可以从总帐、库存变动日记帐、销售发票和采购发票过帐中国式凭证。</span><span class="sxs-lookup"><span data-stu-id="91d0b-104">You can post Chinese vouchers from the general ledger, inventory movement journals, sales invoices, and purchase invoices.</span></span> <span data-ttu-id="91d0b-105">. 从这些源过帐时，将为这些财务凭证分配默认中国式凭证类型和中国式凭证号。</span><span class="sxs-lookup"><span data-stu-id="91d0b-105">When you post from these sources, the default Chinese voucher type and Chinese voucher number will be assigned to those financial vouchers.</span></span>
<span data-ttu-id="91d0b-106">此任务逐步演示如何从库存变动日记帐和从销售发票过帐中国式凭证。</span><span class="sxs-lookup"><span data-stu-id="91d0b-106">This task walks you through posting Chinese vouchers from the Inventory movement journal and from a sales invoice.</span></span>
<span data-ttu-id="91d0b-107">必须先向当前会计日历添加当前会计年度，才能完成此任务。</span><span class="sxs-lookup"><span data-stu-id="91d0b-107">Before you can complete this task, you must add the current fiscal year to the current fiscal calendar.</span></span> <span data-ttu-id="91d0b-108">用于创建此任务的演示数据公司是 CNMF。</span><span class="sxs-lookup"><span data-stu-id="91d0b-108">This task was created using the demo data company CNMF.</span></span> <span data-ttu-id="91d0b-109">此过程针对 Dynamics 365 for Operations 版本 1611 中增加的一项功能。</span><span class="sxs-lookup"><span data-stu-id="91d0b-109">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="post-chinese-vouchers-from-an-inventory-movement-journal"></a><span data-ttu-id="91d0b-110">从库存变动日记帐过帐中国式凭证</span><span class="sxs-lookup"><span data-stu-id="91d0b-110">Post Chinese vouchers from an inventory movement journal</span></span>
1. <span data-ttu-id="91d0b-111">转到“库存管理”>“日记帐条目”>“物料”>“移动”。</span><span class="sxs-lookup"><span data-stu-id="91d0b-111">Go to Inventory management > Journal entries > Items > Movement.</span></span>
2. <span data-ttu-id="91d0b-112">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="91d0b-112">Click New.</span></span>
3. <span data-ttu-id="91d0b-113">在“名称”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="91d0b-113">In the Name field, enter or select a value.</span></span>
4. <span data-ttu-id="91d0b-114">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="91d0b-114">Click OK.</span></span>
5. <span data-ttu-id="91d0b-115">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="91d0b-115">Click New.</span></span>
6. <span data-ttu-id="91d0b-116">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="91d0b-116">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="91d0b-117">在“日期”字段中，输入一个日期。</span><span class="sxs-lookup"><span data-stu-id="91d0b-117">In the Date field, enter a date.</span></span>
8. <span data-ttu-id="91d0b-118">在“物料编号”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="91d0b-118">In the Item number field, enter or select a value.</span></span>
9. <span data-ttu-id="91d0b-119">在“项目编号”字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="91d0b-119">In the Item number field, type a value.</span></span>
10. <span data-ttu-id="91d0b-120">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="91d0b-120">Close the page.</span></span>
11. <span data-ttu-id="91d0b-121">在“数量”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="91d0b-121">In the Quantity field, enter a number.</span></span>
12. <span data-ttu-id="91d0b-122">在“抵销帐户”字段中，指定所需值。</span><span class="sxs-lookup"><span data-stu-id="91d0b-122">In the Offset account field, specify the desired values.</span></span>
13. <span data-ttu-id="91d0b-123">在“抵销帐户”字段中，指定所需值。</span><span class="sxs-lookup"><span data-stu-id="91d0b-123">In the Offset account field, specify the desired values.</span></span>
14. <span data-ttu-id="91d0b-124">单击“库存维度”选项卡。</span><span class="sxs-lookup"><span data-stu-id="91d0b-124">Click the Inventory dimensions tab.</span></span>
15. <span data-ttu-id="91d0b-125">在“站点”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="91d0b-125">In the Site field, enter or select a value.</span></span>
16. <span data-ttu-id="91d0b-126">在“仓库”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="91d0b-126">In the Warehouse field, enter or select a value.</span></span>
17. <span data-ttu-id="91d0b-127">在“仓库”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="91d0b-127">In the Warehouse field, type a value.</span></span>
18. <span data-ttu-id="91d0b-128">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="91d0b-128">Close the page.</span></span>
19. <span data-ttu-id="91d0b-129">在“尺寸”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="91d0b-129">In the Size field, enter or select a value.</span></span>
20. <span data-ttu-id="91d0b-130">在“大小”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="91d0b-130">In the Size field, type a value.</span></span>
21. <span data-ttu-id="91d0b-131">单击“财务维度”选项卡。</span><span class="sxs-lookup"><span data-stu-id="91d0b-131">Click the Financial dimension tab.</span></span>
22. <span data-ttu-id="91d0b-132">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="91d0b-132">Close the page.</span></span>
23. <span data-ttu-id="91d0b-133">在“业务单位”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="91d0b-133">In the BusinessUnit field, enter or select a value.</span></span>
24. <span data-ttu-id="91d0b-134">在“CostCenter_CN”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="91d0b-134">In the CostCenter_CN field, enter or select a value.</span></span>
25. <span data-ttu-id="91d0b-135">在“Department_CN”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="91d0b-135">In the Department_CN field, enter or select a value.</span></span>
26. <span data-ttu-id="91d0b-136">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="91d0b-136">Click Save.</span></span>
27. <span data-ttu-id="91d0b-137">单击“验证”。</span><span class="sxs-lookup"><span data-stu-id="91d0b-137">Click Validate.</span></span>
28. <span data-ttu-id="91d0b-138">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="91d0b-138">Click OK.</span></span>
29. <span data-ttu-id="91d0b-139">单击“过帐”。</span><span class="sxs-lookup"><span data-stu-id="91d0b-139">Click Post.</span></span>
30. <span data-ttu-id="91d0b-140">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="91d0b-140">Click OK.</span></span>
31. <span data-ttu-id="91d0b-141">单击“库存”。</span><span class="sxs-lookup"><span data-stu-id="91d0b-141">Click Inventory.</span></span>
32. <span data-ttu-id="91d0b-142">单击“交易记录”。</span><span class="sxs-lookup"><span data-stu-id="91d0b-142">Click Transactions.</span></span>
33. <span data-ttu-id="91d0b-143">在操作窗格上，单击"分类帐"。</span><span class="sxs-lookup"><span data-stu-id="91d0b-143">On the Action Pane, click Ledger.</span></span>
34. <span data-ttu-id="91d0b-144">单击“财务凭证”。</span><span class="sxs-lookup"><span data-stu-id="91d0b-144">Click Financial voucher.</span></span>
    * <span data-ttu-id="91d0b-145">例如，为“中国式凭证类型”分配“交易”。</span><span class="sxs-lookup"><span data-stu-id="91d0b-145">For example, the Chinese voucher type Tran is assigned.</span></span>  

## <a name="post-chinese-vouchers-from-a-sales-invoice"></a><span data-ttu-id="91d0b-146">从销售发票过帐中国式凭证</span><span class="sxs-lookup"><span data-stu-id="91d0b-146">Post Chinese vouchers from a sales invoice</span></span>
1. <span data-ttu-id="91d0b-147">转到应收帐项目>订单>所有销售订单。</span><span class="sxs-lookup"><span data-stu-id="91d0b-147">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="91d0b-148">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="91d0b-148">Click New.</span></span>
3. <span data-ttu-id="91d0b-149">在“客户帐户”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="91d0b-149">In the Customer account field, enter or select a value.</span></span>
4. <span data-ttu-id="91d0b-150">展开“常规”部分。</span><span class="sxs-lookup"><span data-stu-id="91d0b-150">Expand the General section.</span></span>
5. <span data-ttu-id="91d0b-151">展开“管理”部分。</span><span class="sxs-lookup"><span data-stu-id="91d0b-151">Expand the Administration section.</span></span>
6. <span data-ttu-id="91d0b-152">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="91d0b-152">Click OK.</span></span>
7. <span data-ttu-id="91d0b-153">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="91d0b-153">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="91d0b-154">在“物料编号”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="91d0b-154">In the Item number field, enter or select a value.</span></span>
9. <span data-ttu-id="91d0b-155">在“项目编号”字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="91d0b-155">In the Item number field, type a value.</span></span>
10. <span data-ttu-id="91d0b-156">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="91d0b-156">Close the page.</span></span>
11. <span data-ttu-id="91d0b-157">展开“行明细”部分。</span><span class="sxs-lookup"><span data-stu-id="91d0b-157">Expand the Line details section.</span></span>
12. <span data-ttu-id="91d0b-158">单击“设置”选项卡。</span><span class="sxs-lookup"><span data-stu-id="91d0b-158">Click the Setup tab.</span></span>
13. <span data-ttu-id="91d0b-159">单击“产品”选项卡。</span><span class="sxs-lookup"><span data-stu-id="91d0b-159">Click the Product tab.</span></span>
14. <span data-ttu-id="91d0b-160">在“尺寸”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="91d0b-160">In the Size field, enter or select a value.</span></span>
15. <span data-ttu-id="91d0b-161">在“站点”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="91d0b-161">In the Site field, enter or select a value.</span></span>
16. <span data-ttu-id="91d0b-162">在“站点”字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="91d0b-162">In the Site field, type a value.</span></span>
17. <span data-ttu-id="91d0b-163">在“仓库”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="91d0b-163">In the Warehouse field, type a value.</span></span>
18. <span data-ttu-id="91d0b-164">在“仓库”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="91d0b-164">In the Warehouse field, enter or select a value.</span></span>
19. <span data-ttu-id="91d0b-165">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="91d0b-165">Close the page.</span></span>
20. <span data-ttu-id="91d0b-166">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="91d0b-166">Close the page.</span></span>
21. <span data-ttu-id="91d0b-167">单击"价格和折扣"选项卡。</span><span class="sxs-lookup"><span data-stu-id="91d0b-167">Click the Price and discount tab.</span></span>
22. <span data-ttu-id="91d0b-168">单击“财务维度”选项卡。</span><span class="sxs-lookup"><span data-stu-id="91d0b-168">Click the Financial dimensions tab.</span></span>
23. <span data-ttu-id="91d0b-169">在“数量”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="91d0b-169">In the Quantity field, enter a number.</span></span>
24. <span data-ttu-id="91d0b-170">在“单价”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="91d0b-170">In the Unit price field, enter a number.</span></span>
25. <span data-ttu-id="91d0b-171">在“当前交货量”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="91d0b-171">In the Deliver now field, enter a number.</span></span>
26. <span data-ttu-id="91d0b-172">在“当前交货量”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="91d0b-172">In the Deliver now field, enter a number.</span></span>
27. <span data-ttu-id="91d0b-173">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="91d0b-173">Click Save.</span></span>
28. <span data-ttu-id="91d0b-174">在操作窗格上，单击“发票”。</span><span class="sxs-lookup"><span data-stu-id="91d0b-174">On the Action Pane, click Invoice.</span></span>
29. <span data-ttu-id="91d0b-175">单击“发票”。</span><span class="sxs-lookup"><span data-stu-id="91d0b-175">Click Invoice.</span></span>
30. <span data-ttu-id="91d0b-176">展开“参数”部分。</span><span class="sxs-lookup"><span data-stu-id="91d0b-176">Expand the Parameters section.</span></span>
31. <span data-ttu-id="91d0b-177">在数量字段，挑一选项。</span><span class="sxs-lookup"><span data-stu-id="91d0b-177">In the Quantity field, select an option.</span></span>
32. <span data-ttu-id="91d0b-178">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="91d0b-178">Click OK.</span></span>
33. <span data-ttu-id="91d0b-179">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="91d0b-179">Click OK.</span></span>
34. <span data-ttu-id="91d0b-180">单击“发票”。</span><span class="sxs-lookup"><span data-stu-id="91d0b-180">Click Invoice.</span></span>
35. <span data-ttu-id="91d0b-181">单击“交易记录”。</span><span class="sxs-lookup"><span data-stu-id="91d0b-181">Click Transactions.</span></span>
36. <span data-ttu-id="91d0b-182">单击“凭证”。</span><span class="sxs-lookup"><span data-stu-id="91d0b-182">Click Voucher.</span></span>
    * <span data-ttu-id="91d0b-183">例如，可以看到为“中国式凭证类型”分配了“交易”。</span><span class="sxs-lookup"><span data-stu-id="91d0b-183">For example, you can see that the Chinese voucher type Tran has been assigned.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]