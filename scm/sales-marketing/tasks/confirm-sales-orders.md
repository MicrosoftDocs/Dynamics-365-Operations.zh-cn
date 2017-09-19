--- 
title: "确认销售订单"
description: "该过程说明了如何确认销售订单。"
author: omulvad
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 7cab69222c5004e6a62c632a9e85085403434ffd
ms.contentlocale: zh-cn
ms.lasthandoff: 08/29/2017

---
# <a name="confirm-sales-orders"></a><span data-ttu-id="6c94d-103">确认销售订单</span><span class="sxs-lookup"><span data-stu-id="6c94d-103">Confirm sales orders</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6c94d-104">该过程说明了如何确认销售订单。</span><span class="sxs-lookup"><span data-stu-id="6c94d-104">This procedure demonstrates how to confirm sales orders.</span></span> <span data-ttu-id="6c94d-105">将会向您显示如何确认单个订单，以及如何一次确认多个订单。</span><span class="sxs-lookup"><span data-stu-id="6c94d-105">You’ll be shown how to confirm a single order, and how to confirm multiple orders at once.</span></span> <span data-ttu-id="6c94d-106">这些任务通常由销售订单处理员完成。</span><span class="sxs-lookup"><span data-stu-id="6c94d-106">These tasks would typically be carried out by a sales order processor.</span></span> <span data-ttu-id="6c94d-107">您可以使用演示数据公司 USMF，也可使用您自己的数据运行该过程。</span><span class="sxs-lookup"><span data-stu-id="6c94d-107">You can use this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="6c94d-108">在您开始前，确保同一客户的若干未结销售订单可用。</span><span class="sxs-lookup"><span data-stu-id="6c94d-108">Before you start, make sure there are several open sales orders for the same customer.</span></span> <span data-ttu-id="6c94d-109">如果您正在使用 USMF，您可以使用客户 US-027。</span><span class="sxs-lookup"><span data-stu-id="6c94d-109">If you’re using USMF, you can use customer US-027.</span></span>


## <a name="confirm-a-single-sales-order"></a><span data-ttu-id="6c94d-110">确认单一销售订单</span><span class="sxs-lookup"><span data-stu-id="6c94d-110">Confirm a single sales order</span></span>
1. <span data-ttu-id="6c94d-111">转至“销售和营销”>“销售订单”>“所有销售订单”。</span><span class="sxs-lookup"><span data-stu-id="6c94d-111">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
2. <span data-ttu-id="6c94d-112">在列表中，查找并选择您想要确认的订单。</span><span class="sxs-lookup"><span data-stu-id="6c94d-112">In the list, find and select the order that you want to confirm.</span></span>
3. <span data-ttu-id="6c94d-113">单击销售订单编号上的链接，以打开选中的订单。</span><span class="sxs-lookup"><span data-stu-id="6c94d-113">Click the link on the sales order number to open the selected order.</span></span>
4. <span data-ttu-id="6c94d-114">在“操作窗格”上，单击“销售”。</span><span class="sxs-lookup"><span data-stu-id="6c94d-114">On the Action Pane, click Sell.</span></span>
5. <span data-ttu-id="6c94d-115">单击“确认销售订单”。</span><span class="sxs-lookup"><span data-stu-id="6c94d-115">Click Confirm sales order.</span></span>
6. <span data-ttu-id="6c94d-116">展开或收起“参数”部分。</span><span class="sxs-lookup"><span data-stu-id="6c94d-116">Expand or collapse the Parameters section.</span></span>
    * <span data-ttu-id="6c94d-117">确保“过帐是”字段有效。</span><span class="sxs-lookup"><span data-stu-id="6c94d-117">Make sure that the Posting Yes field is active.</span></span>  
7. <span data-ttu-id="6c94d-118">将“打印确认”选项设置为“是”。</span><span class="sxs-lookup"><span data-stu-id="6c94d-118">Set the Print confirmation option to Yes.</span></span>
    * <span data-ttu-id="6c94d-119">“检查信用额度”字段规定了用于计算客户的剩余信用额度的方法。</span><span class="sxs-lookup"><span data-stu-id="6c94d-119">The Check credit limit field specifies the method that’s used to calculate a customer's remaining credit.</span></span> <span data-ttu-id="6c94d-120">该选项默认从“应收帐款参数”页复制而来。</span><span class="sxs-lookup"><span data-stu-id="6c94d-120">By default, it’s copied from the Accounts receivable parameters page.</span></span> <span data-ttu-id="6c94d-121">如果在确认特定销售订单时，您想要跳过信用额度检查，可以将“检查信用额度”设置为“零”。</span><span class="sxs-lookup"><span data-stu-id="6c94d-121">If you want to skip the credit limit check when confirming a specific sales order, set the Check credit limit to None.</span></span> <span data-ttu-id="6c94d-122">但是，您应该清楚，即使此字段被设置为零，如果客户主数据中的强制信用额度选项被选中，信用额度检查仍将会执行。</span><span class="sxs-lookup"><span data-stu-id="6c94d-122">However, you should be aware that even with if this field is set to None, the credit limit check will still be performed if the Mandatory credit limit option is selected on the customer master data.</span></span>  
8. <span data-ttu-id="6c94d-123">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="6c94d-123">Click OK.</span></span>
9. <span data-ttu-id="6c94d-124">单击“是”。</span><span class="sxs-lookup"><span data-stu-id="6c94d-124">Click Yes.</span></span>
10. <span data-ttu-id="6c94d-125">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="6c94d-125">Close the page.</span></span>
11. <span data-ttu-id="6c94d-126">在“操作窗格”上，单击“选项”。</span><span class="sxs-lookup"><span data-stu-id="6c94d-126">On the Action Pane, click Options.</span></span>
12. <span data-ttu-id="6c94d-127">单击“更改”视图。</span><span class="sxs-lookup"><span data-stu-id="6c94d-127">Click Change view.</span></span>
13. <span data-ttu-id="6c94d-128">单击“标题”视图。</span><span class="sxs-lookup"><span data-stu-id="6c94d-128">Click Header view.</span></span>
    * <span data-ttu-id="6c94d-129">在确认订单时，“文档状态”设置为“确认”。</span><span class="sxs-lookup"><span data-stu-id="6c94d-129">When an order is confirmed, the Document status is set to Confirmation.</span></span>  
14. <span data-ttu-id="6c94d-130">在“操作窗格”上，单击“销售”。</span><span class="sxs-lookup"><span data-stu-id="6c94d-130">On the Action Pane, click Sell.</span></span>
15. <span data-ttu-id="6c94d-131">单击“销售订单确认”。</span><span class="sxs-lookup"><span data-stu-id="6c94d-131">Click Sales order confirmation.</span></span>
16. <span data-ttu-id="6c94d-132">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="6c94d-132">Close the page.</span></span>

## <a name="confirm-multiple-sales-orders-at-once"></a><span data-ttu-id="6c94d-133">一次确认多个销售订单</span><span class="sxs-lookup"><span data-stu-id="6c94d-133">Confirm multiple sales orders at once</span></span>
1. <span data-ttu-id="6c94d-134">转到“销售和营销”>“销售订单”>“订单确认”>“确认销售订单”。</span><span class="sxs-lookup"><span data-stu-id="6c94d-134">Go to Sales and marketing > Sales orders > Order confirmation > Confirm sales order.</span></span>
2. <span data-ttu-id="6c94d-135">单击“选择”。</span><span class="sxs-lookup"><span data-stu-id="6c94d-135">Click Select.</span></span>
3. <span data-ttu-id="6c94d-136">在“范围”选项卡的列表中，查找并选择引用“客户帐户”字段的记录。</span><span class="sxs-lookup"><span data-stu-id="6c94d-136">In the list on the Range tab, find and select the record that references the Customer account field.</span></span>
4. <span data-ttu-id="6c94d-137">在“标准”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="6c94d-137">In the Criteria field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="6c94d-138">在列表中，查找并选择拥有您想要批量确认的多个订单的客户帐户。</span><span class="sxs-lookup"><span data-stu-id="6c94d-138">In the list, find and select the customer account that has multiple orders which you want to mass confirm.</span></span>
    * <span data-ttu-id="6c94d-139">如果正在使用 USMF，您可以选择帐户 US-027。</span><span class="sxs-lookup"><span data-stu-id="6c94d-139">If you’re using USMF, you can select account US-027.</span></span>  
6. <span data-ttu-id="6c94d-140">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="6c94d-140">Click OK.</span></span>
    * <span data-ttu-id="6c94d-141">“概述”选项卡会显示与查询条件匹配的订单列表。</span><span class="sxs-lookup"><span data-stu-id="6c94d-141">The Overview tab displays a list of the orders that match the query criteria.</span></span> <span data-ttu-id="6c94d-142">这些将包括在确认中。</span><span class="sxs-lookup"><span data-stu-id="6c94d-142">These will be included in the confirmation.</span></span>  
    * <span data-ttu-id="6c94d-143">“汇总更新”字段规定了将多个订单汇总到一个确认文件所需的参数。</span><span class="sxs-lookup"><span data-stu-id="6c94d-143">The Summary update for field specifies the parameter by which multiple orders are to be summarized into one confirmation document.</span></span> <span data-ttu-id="6c94d-144">该选项默认从“应收帐款参数”页中汇总更新设置的“默认值”复制而来。</span><span class="sxs-lookup"><span data-stu-id="6c94d-144">By default, the option is copied from the Default values for summary update setting on the Accounts receivable parameters page.</span></span>  
7. <span data-ttu-id="6c94d-145">在“汇总更新“字段中，选择“订单”。</span><span class="sxs-lookup"><span data-stu-id="6c94d-145">In the Summary update for field, select 'Order'.</span></span>
    * <span data-ttu-id="6c94d-146">创建汇总更新所需的最少参数是发票帐户和币种。</span><span class="sxs-lookup"><span data-stu-id="6c94d-146">The minimum parameters that are required to create summary updates are Invoice account and Currency.</span></span> <span data-ttu-id="6c94d-147">这意味着不允许汇总更新拥有不同的发票帐户和不同的币种。</span><span class="sxs-lookup"><span data-stu-id="6c94d-147">This means that summary updates that have different invoice accounts and different currencies are not allowed.</span></span> <span data-ttu-id="6c94d-148">附加参数可以在“汇总更新参数”页内设置，并且“汇总更新参数”页可以从“应收帐款参数”页访问。</span><span class="sxs-lookup"><span data-stu-id="6c94d-148">Additional parameters can be set up in the Summary update parameters page which is accessible from the Accounts receivable parameters page.</span></span>  
8. <span data-ttu-id="6c94d-149">在“销售订单”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="6c94d-149">In the Sales order field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="6c94d-150">在列表中，选择您想将其纳入汇总订单的销售订单。</span><span class="sxs-lookup"><span data-stu-id="6c94d-150">In the list, select the order number that you want to be the summary order.</span></span>
10. <span data-ttu-id="6c94d-151">单击“排列”。</span><span class="sxs-lookup"><span data-stu-id="6c94d-151">Click Arrange.</span></span>
11. <span data-ttu-id="6c94d-152">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="6c94d-152">Click OK.</span></span>
12. <span data-ttu-id="6c94d-153">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="6c94d-153">Click OK.</span></span>

