---
title: 确认销售订单
description: 该过程说明了如何确认销售订单。
author: omulvad
ms.date: 06/26/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SalesTableListPage, SalesTable, SalesEditLines,  SrsReportViewerForm, CustConfirmJournal, SysQueryForm, SysQueryFieldLookUp, SysLookup, SalesParmIdLookup, SalesUnconfirmedOrdersPart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e681a822ae1ec628fd20931263a6115b998ffba9
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5836462"
---
# <a name="confirm-sales-orders"></a><span data-ttu-id="edbaf-103">确认销售订单</span><span class="sxs-lookup"><span data-stu-id="edbaf-103">Confirm sales orders</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="edbaf-104">该过程说明了如何确认销售订单。</span><span class="sxs-lookup"><span data-stu-id="edbaf-104">This procedure demonstrates how to confirm sales orders.</span></span> <span data-ttu-id="edbaf-105">将会向您显示如何确认单个订单，以及如何一次确认多个订单。</span><span class="sxs-lookup"><span data-stu-id="edbaf-105">You'll be shown how to confirm a single order, and how to confirm multiple orders at once.</span></span> <span data-ttu-id="edbaf-106">这些任务通常由销售订单处理员完成。</span><span class="sxs-lookup"><span data-stu-id="edbaf-106">These tasks would typically be carried out by a sales order processor.</span></span> <span data-ttu-id="edbaf-107">您可以使用演示数据公司 USMF，也可使用您自己的数据运行该过程。</span><span class="sxs-lookup"><span data-stu-id="edbaf-107">You can use this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="edbaf-108">在您开始前，确保同一客户的若干未结销售订单可用。</span><span class="sxs-lookup"><span data-stu-id="edbaf-108">Before you start, make sure there are several open sales orders for the same customer.</span></span> <span data-ttu-id="edbaf-109">如果您正在使用 USMF，您可以使用客户 US-027。</span><span class="sxs-lookup"><span data-stu-id="edbaf-109">If you're using USMF, you can use customer US-027.</span></span>


## <a name="confirm-a-single-sales-order"></a><span data-ttu-id="edbaf-110">确认单一销售订单</span><span class="sxs-lookup"><span data-stu-id="edbaf-110">Confirm a single sales order</span></span>
1. <span data-ttu-id="edbaf-111">转到 **导航窗格 > 模块 > 销售和营销 > 销售订单 > 所有销售订单**。</span><span class="sxs-lookup"><span data-stu-id="edbaf-111">Go to **Navigation pane > Modules > Sales and marketing > Sales orders > All sales orders**.</span></span>
2. <span data-ttu-id="edbaf-112">在列表中，查找并选择您想要确认的订单。</span><span class="sxs-lookup"><span data-stu-id="edbaf-112">In the list, find and select the order that you want to confirm.</span></span>
3. <span data-ttu-id="edbaf-113">单击销售订单编号上的链接，以打开选中的订单。</span><span class="sxs-lookup"><span data-stu-id="edbaf-113">Click the link on the sales order number to open the selected order.</span></span>
4. <span data-ttu-id="edbaf-114">在 **操作窗格** 上，单击 **销售**。</span><span class="sxs-lookup"><span data-stu-id="edbaf-114">On the **Action Pane**, click **Sell**.</span></span>
5. <span data-ttu-id="edbaf-115">单击 **确认销售订单**。</span><span class="sxs-lookup"><span data-stu-id="edbaf-115">Click **Confirm sales order**.</span></span>
6. <span data-ttu-id="edbaf-116">展开 **参数** 部分。</span><span class="sxs-lookup"><span data-stu-id="edbaf-116">Expand the **Parameters** section.</span></span> <span data-ttu-id="edbaf-117">确保将 **过帐** 选项设置为“是”。</span><span class="sxs-lookup"><span data-stu-id="edbaf-117">Make sure that the **Posting** option is set to 'Yes'.</span></span>  
7. <span data-ttu-id="edbaf-118">将 **打印确认选项** 设置为“是”。</span><span class="sxs-lookup"><span data-stu-id="edbaf-118">Set the **Print confirmation option** to 'Yes'.</span></span> <span data-ttu-id="edbaf-119">**检查信用额度** 字段规定了用于计算客户的剩余信用额度的方法。</span><span class="sxs-lookup"><span data-stu-id="edbaf-119">The **Check credit limit** field specifies the method that's used to calculate a customer's remaining credit.</span></span> <span data-ttu-id="edbaf-120">该选项默认从“应收账款参数”页复制而来。</span><span class="sxs-lookup"><span data-stu-id="edbaf-120">By default, it's copied from the Accounts receivable parameters page.</span></span> <span data-ttu-id="edbaf-121">如果在确认特定销售订单时，您想要跳过信用额度检查，可以将 **检查信用额度** 设置为“无”。</span><span class="sxs-lookup"><span data-stu-id="edbaf-121">If you want to skip the credit limit check when confirming a specific sales order, set the **Check credit limit** to 'None'.</span></span> <span data-ttu-id="edbaf-122">但是，您应该清楚，即使此字段被设置为“无”，如果客户主数据中的 **强制信用额度** 选项被选中，信用额度检查仍将会执行。</span><span class="sxs-lookup"><span data-stu-id="edbaf-122">However, you should be aware that even with if this field is set to 'None', the credit limit check will still be performed if the **Mandatory credit limit** option is selected on the customer master data.</span></span> 
8. <span data-ttu-id="edbaf-123">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="edbaf-123">Click **OK**.</span></span>
9. <span data-ttu-id="edbaf-124">单击 **是**。</span><span class="sxs-lookup"><span data-stu-id="edbaf-124">Click **Yes**.</span></span>
10. <span data-ttu-id="edbaf-125">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="edbaf-125">Close the page.</span></span>
11. <span data-ttu-id="edbaf-126">在 **操作窗格** 上，单击 **选项**。</span><span class="sxs-lookup"><span data-stu-id="edbaf-126">On the **Action Pane**, click **Options**.</span></span>
12. <span data-ttu-id="edbaf-127">单击 **更改视图**。</span><span class="sxs-lookup"><span data-stu-id="edbaf-127">Click **Change view**.</span></span>
13. <span data-ttu-id="edbaf-128">单击 **标题视图**。</span><span class="sxs-lookup"><span data-stu-id="edbaf-128">Click **Header view**.</span></span> <span data-ttu-id="edbaf-129">在确认订单时，**文档状态** 设置为“确认”。</span><span class="sxs-lookup"><span data-stu-id="edbaf-129">When an order is confirmed, the **Document status** is set to 'Confirmation'.</span></span> 
14. <span data-ttu-id="edbaf-130">在 **操作窗格** 上，单击 **销售**。</span><span class="sxs-lookup"><span data-stu-id="edbaf-130">On the **Action Pane**, click **Sell**.</span></span>
15. <span data-ttu-id="edbaf-131">单击 **销售订单确认**。</span><span class="sxs-lookup"><span data-stu-id="edbaf-131">Click **Sales order confirmation**.</span></span>
16. <span data-ttu-id="edbaf-132">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="edbaf-132">Close the page.</span></span>

## <a name="confirm-multiple-sales-orders-at-once"></a><span data-ttu-id="edbaf-133">一次确认多个销售订单</span><span class="sxs-lookup"><span data-stu-id="edbaf-133">Confirm multiple sales orders at once</span></span>
1. <span data-ttu-id="edbaf-134">转到 **销售和营销 > 销售订单 > 订单确认 > 确认销售订单**。</span><span class="sxs-lookup"><span data-stu-id="edbaf-134">Go to **Sales and marketing > Sales orders > Order confirmation > Confirm sales order**.</span></span>
2. <span data-ttu-id="edbaf-135">单击 **选择**。</span><span class="sxs-lookup"><span data-stu-id="edbaf-135">Click **Select**.</span></span>
3. <span data-ttu-id="edbaf-136">在 **范围** 选项卡的列表中，查找并选择引用 **客户帐户** 字段的记录。</span><span class="sxs-lookup"><span data-stu-id="edbaf-136">In the list on the **Range** tab, find and select the record that references the **Customer account** field.</span></span>
4. <span data-ttu-id="edbaf-137">在 **标准** 字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="edbaf-137">In the **Criteria** field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="edbaf-138">在列表中，查找并选择拥有您想要批量确认的多个订单的客户帐户。</span><span class="sxs-lookup"><span data-stu-id="edbaf-138">In the list, find and select the customer account that has multiple orders which you want to mass confirm.</span></span> <span data-ttu-id="edbaf-139">如果正在使用 USMF，您可以选择帐户 US-027。</span><span class="sxs-lookup"><span data-stu-id="edbaf-139">If you're using USMF, you can select account US-027.</span></span>  
6. <span data-ttu-id="edbaf-140">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="edbaf-140">Click **OK**.</span></span>
    - <span data-ttu-id="edbaf-141">**概述** 选项卡会显示与查询条件匹配的订单列表。</span><span class="sxs-lookup"><span data-stu-id="edbaf-141">The **Overview** tab displays a list of the orders that match the query criteria.</span></span> <span data-ttu-id="edbaf-142">这些将包括在确认中。</span><span class="sxs-lookup"><span data-stu-id="edbaf-142">These will be included in the confirmation.</span></span>  
    - <span data-ttu-id="edbaf-143">**参数** 部分的 **汇总更新** 字段规定了将多个订单汇总到一个确认文件所需的参数。</span><span class="sxs-lookup"><span data-stu-id="edbaf-143">The **Summary update for** field in the **Parameters** section specifies the parameter by which multiple orders are to be summarized into one confirmation document.</span></span> <span data-ttu-id="edbaf-144">该选项默认从 **应收账款参数** 页中 **汇总更新设置的默认值** 复制而来。</span><span class="sxs-lookup"><span data-stu-id="edbaf-144">By default, the option is copied from the D **efault values for summary update setting** on the **Accounts receivable parameters** page.</span></span>  
7. <span data-ttu-id="edbaf-145">在 **汇总更新** 字段中，选择“订单”。</span><span class="sxs-lookup"><span data-stu-id="edbaf-145">In the **Summary update for** field, select 'Order'.</span></span> <span data-ttu-id="edbaf-146">创建汇总更新所需的最少参数是 **发票帐户** 和 **币种**。</span><span class="sxs-lookup"><span data-stu-id="edbaf-146">The minimum parameters that are required to create summary updates are **Invoice account** and **Currency**.</span></span> <span data-ttu-id="edbaf-147">这意味着不允许汇总更新拥有不同的发票帐户和不同的币种。</span><span class="sxs-lookup"><span data-stu-id="edbaf-147">This means that summary updates that have different invoice accounts and different currencies are not allowed.</span></span> <span data-ttu-id="edbaf-148">附加参数可以在“汇总更新参数”页内设置，并且 **汇总更新参数** 页可以从 **应收账款参数** 页访问。</span><span class="sxs-lookup"><span data-stu-id="edbaf-148">Additional parameters can be set up in the **Summary update parameters** page which is accessible from the **Accounts receivable parameters** page.</span></span> 
8. <span data-ttu-id="edbaf-149">在 **销售订单** 字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="edbaf-149">In the **Sales order** field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="edbaf-150">在列表中，选择您想将其纳入汇总订单的销售订单。</span><span class="sxs-lookup"><span data-stu-id="edbaf-150">In the list, select the order number that you want to be the summary order.</span></span>
10. <span data-ttu-id="edbaf-151">单击 **排列**。</span><span class="sxs-lookup"><span data-stu-id="edbaf-151">Click **Arrange**.</span></span>
11. <span data-ttu-id="edbaf-152">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="edbaf-152">Click **OK**.</span></span>
12. <span data-ttu-id="edbaf-153">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="edbaf-153">Click **OK**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]