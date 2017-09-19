--- 
title: "使用供应商发票将发票数据键入应付帐款"
description: "本任务指南将帮助您根据采购订单创建供应商发票，并查看采购订单、收据和发票的匹配结果（三向匹配）。"
author: abruer
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 48535a283cbdfdc7343a20105b139c527cac85f4
ms.contentlocale: zh-cn
ms.lasthandoff: 08/29/2017

---
# <a name="key-invoice-data-into-accounts-payable-using-a-vendor-invoice"></a><span data-ttu-id="e6d0c-103">使用供应商发票将发票数据键入应付帐款</span><span class="sxs-lookup"><span data-stu-id="e6d0c-103">Key invoice data into accounts payable using a vendor invoice</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e6d0c-104">本任务指南将帮助您根据采购订单创建供应商发票，并查看采购订单、收据和发票的匹配结果（三向匹配）。</span><span class="sxs-lookup"><span data-stu-id="e6d0c-104">This task guide will help you create a vendor invoice from a purchase order and view the results of matching the purchase order, receipt, and invoice (3 way matching).</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="e6d0c-105">创建采购订单</span><span class="sxs-lookup"><span data-stu-id="e6d0c-105">Create a purchase order</span></span>
1. <span data-ttu-id="e6d0c-106">转到“应付帐款”>“采购订单”>“所有采购订单”。</span><span class="sxs-lookup"><span data-stu-id="e6d0c-106">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="e6d0c-107">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="e6d0c-107">Click New.</span></span>
3. <span data-ttu-id="e6d0c-108">在“供应商帐户”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="e6d0c-108">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="e6d0c-109">查找并选择一个供应商。</span><span class="sxs-lookup"><span data-stu-id="e6d0c-109">Find a vendor to select.</span></span> <span data-ttu-id="e6d0c-110">例如，滚动到 US-104。</span><span class="sxs-lookup"><span data-stu-id="e6d0c-110">For example, scroll down to US-104.</span></span>
5. <span data-ttu-id="e6d0c-111">选择供应商 US-104。</span><span class="sxs-lookup"><span data-stu-id="e6d0c-111">Select vendor US-104.</span></span>
6. <span data-ttu-id="e6d0c-112">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="e6d0c-112">Click OK.</span></span>
7. <span data-ttu-id="e6d0c-113">在“物料编号”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="e6d0c-113">In the Item number field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="e6d0c-114">选择一个库存物料。</span><span class="sxs-lookup"><span data-stu-id="e6d0c-114">Select an inventory item.</span></span> <span data-ttu-id="e6d0c-115">例如，选择物料编号 1000。</span><span class="sxs-lookup"><span data-stu-id="e6d0c-115">For example, select item number 1000.</span></span>
9. <span data-ttu-id="e6d0c-116">展开或折叠“行详细信息”部分。</span><span class="sxs-lookup"><span data-stu-id="e6d0c-116">Expand or collapse the Line details section.</span></span>
10. <span data-ttu-id="e6d0c-117">单击“设置”选项卡。</span><span class="sxs-lookup"><span data-stu-id="e6d0c-117">Click the Setup tab.</span></span>
    * <span data-ttu-id="e6d0c-118">您可以覆盖匹配政策，改为使用不匹配、双向匹配或三向匹配。</span><span class="sxs-lookup"><span data-stu-id="e6d0c-118">You can override the matching policy to use no matching, 2-way matching, or 3-way matching.</span></span>  
11. <span data-ttu-id="e6d0c-119">展开或折叠“行详细信息”部分。</span><span class="sxs-lookup"><span data-stu-id="e6d0c-119">Expand or collapse the Line details section.</span></span>
12. <span data-ttu-id="e6d0c-120">在操作窗格上，单击“采购”。</span><span class="sxs-lookup"><span data-stu-id="e6d0c-120">On the Action Pane, click Purchase.</span></span>
13. <span data-ttu-id="e6d0c-121">单击“确认”。</span><span class="sxs-lookup"><span data-stu-id="e6d0c-121">Click Confirm.</span></span>

## <a name="receive-the-products"></a><span data-ttu-id="e6d0c-122">接收产品</span><span class="sxs-lookup"><span data-stu-id="e6d0c-122">Receive the products</span></span>
1. <span data-ttu-id="e6d0c-123">在操作窗格上，单击“接收”。</span><span class="sxs-lookup"><span data-stu-id="e6d0c-123">On the Action Pane, click Receive.</span></span>
2. <span data-ttu-id="e6d0c-124">单击“产品收据”。</span><span class="sxs-lookup"><span data-stu-id="e6d0c-124">Click Product receipt.</span></span>
3. <span data-ttu-id="e6d0c-125">在“产品收据”字段中，输入产品收据编号。</span><span class="sxs-lookup"><span data-stu-id="e6d0c-125">In the Product receipt field, enter the product receipt number.</span></span> <span data-ttu-id="e6d0c-126">例如，输入 PR123。</span><span class="sxs-lookup"><span data-stu-id="e6d0c-126">For example, enter PR123.</span></span>
4. <span data-ttu-id="e6d0c-127">单击“确定”过帐产品收据。</span><span class="sxs-lookup"><span data-stu-id="e6d0c-127">Click OK to post the product receipt.</span></span>
5. <span data-ttu-id="e6d0c-128">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="e6d0c-128">Close the page.</span></span>

## <a name="create-a-vendor-invoice"></a><span data-ttu-id="e6d0c-129">创建供应商发票</span><span class="sxs-lookup"><span data-stu-id="e6d0c-129">Create a vendor invoice</span></span>
1. <span data-ttu-id="e6d0c-130">转到“应付帐款”>“采购订单”>“已接收但未开票采购订单”。</span><span class="sxs-lookup"><span data-stu-id="e6d0c-130">Go to Accounts payable > Purchase orders > Purchase orders received but not invoiced.</span></span>
2. <span data-ttu-id="e6d0c-131">选择您创建的采购订单。</span><span class="sxs-lookup"><span data-stu-id="e6d0c-131">Select the purchase order that you created.</span></span>
3. <span data-ttu-id="e6d0c-132">在“操作窗格”中，单击“发票”。</span><span class="sxs-lookup"><span data-stu-id="e6d0c-132">On the Action Pane, click Invoice.</span></span>
4. <span data-ttu-id="e6d0c-133">单击“发票”。</span><span class="sxs-lookup"><span data-stu-id="e6d0c-133">Click Invoice.</span></span>
5. <span data-ttu-id="e6d0c-134">在“编号”字段中，输入发票编号。</span><span class="sxs-lookup"><span data-stu-id="e6d0c-134">In the Number field, enter the invoice number.</span></span>
6. <span data-ttu-id="e6d0c-135">在“发票描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="e6d0c-135">In the Invoice description field, type a value.</span></span>
7. <span data-ttu-id="e6d0c-136">在“发票日期”字段中，输入日期。</span><span class="sxs-lookup"><span data-stu-id="e6d0c-136">In the Invoice date field, enter a date.</span></span>
8. <span data-ttu-id="e6d0c-137">在“单价”字段中，输入 1200。</span><span class="sxs-lookup"><span data-stu-id="e6d0c-137">In the Unit price field, enter 1200.</span></span>
9. <span data-ttu-id="e6d0c-138">单击“添加行”。</span><span class="sxs-lookup"><span data-stu-id="e6d0c-138">Click Add line.</span></span>
10. <span data-ttu-id="e6d0c-139">在“物料编号”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="e6d0c-139">In the Item number field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="e6d0c-140">在列表中，找到安装费用项目编号。</span><span class="sxs-lookup"><span data-stu-id="e6d0c-140">In the list, find the installation charge item number.</span></span> <span data-ttu-id="e6d0c-141">例如：S0001</span><span class="sxs-lookup"><span data-stu-id="e6d0c-141">For example, S0001</span></span>
12. <span data-ttu-id="e6d0c-142">选择安装费用项目编号。</span><span class="sxs-lookup"><span data-stu-id="e6d0c-142">Select the installation charge item number.</span></span>
    * <span data-ttu-id="e6d0c-143">请注意，自您作出更改后，尚未执行匹配。</span><span class="sxs-lookup"><span data-stu-id="e6d0c-143">Note that matching has not been performed since you made the changes.</span></span>  
13. <span data-ttu-id="e6d0c-144">单击“更新匹配状态”。</span><span class="sxs-lookup"><span data-stu-id="e6d0c-144">Click Update match status.</span></span>
14. <span data-ttu-id="e6d0c-145">在操作窗格上，单击“审核”。</span><span class="sxs-lookup"><span data-stu-id="e6d0c-145">On the Action Pane, click Review.</span></span>
15. <span data-ttu-id="e6d0c-146">单击“匹配详细信息”。</span><span class="sxs-lookup"><span data-stu-id="e6d0c-146">Click Matching details.</span></span>
    * <span data-ttu-id="e6d0c-147">列有服务的新行并不需要匹配，因此状态仍为“不执行”。</span><span class="sxs-lookup"><span data-stu-id="e6d0c-147">The new line with services does not need to be matched so the status stays "Not performed".</span></span>  
16. <span data-ttu-id="e6d0c-148">为您接收的库存物料选择产品收据。</span><span class="sxs-lookup"><span data-stu-id="e6d0c-148">Select the product receipt for the inventory item that you received.</span></span>
    * <span data-ttu-id="e6d0c-149">已就产品收据匹配行，但数量或价格不匹配，所以匹配失败。</span><span class="sxs-lookup"><span data-stu-id="e6d0c-149">The line with the product receipt was matched but there is a mismatch of quantity or price so it fails.</span></span>  
17. <span data-ttu-id="e6d0c-150">在“单位价格”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="e6d0c-150">In the Unit price field, enter a number.</span></span>
    * <span data-ttu-id="e6d0c-151">由于单位价格匹配，因而状态更新为“已通过”。</span><span class="sxs-lookup"><span data-stu-id="e6d0c-151">Now that the unit price matches, the status is updated to Passed.</span></span> <span data-ttu-id="e6d0c-152">如果您的政策允许有差异，或匹配只是一个警告，您仍然可以过帐发票。</span><span class="sxs-lookup"><span data-stu-id="e6d0c-152">If your policy allows discrepancies or if matching is only a warning, you can still post the invoice.</span></span>  
18. <span data-ttu-id="e6d0c-153">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="e6d0c-153">Close the page.</span></span>
19. <span data-ttu-id="e6d0c-154">单击“过帐”。</span><span class="sxs-lookup"><span data-stu-id="e6d0c-154">Click Post.</span></span>
20. <span data-ttu-id="e6d0c-155">关闭窗体。</span><span class="sxs-lookup"><span data-stu-id="e6d0c-155">Close the form.</span></span>
    * <span data-ttu-id="e6d0c-156">请注意，采购订单不再列为“已接收但未开票”。</span><span class="sxs-lookup"><span data-stu-id="e6d0c-156">Note that the purchase order is no longer listed as received but not invoiced.</span></span>  

