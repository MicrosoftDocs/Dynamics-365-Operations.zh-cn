--- 
title: "使用发票池将发票数据键入 AP 系统"
description: "此任务向导将向您展示如何使用发票登记簿创建发票。"
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
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 96040b1c1ba130f773ba0defbf7bf1dcebedfc13
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---
# <a name="key-invoice-data-into-the-ap-system-using-invoice-pool"></a><span data-ttu-id="b87d0-103">使用发票池将发票数据键入 AP 系统</span><span class="sxs-lookup"><span data-stu-id="b87d0-103">Key invoice data into the AP system using invoice pool</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b87d0-104">此任务向导将向您展示如何使用发票登记簿创建发票。</span><span class="sxs-lookup"><span data-stu-id="b87d0-104">This task guide will show you how to use the invoice register to create invoices.</span></span>  <span data-ttu-id="b87d0-105">然后使用发票池对发票与采购订单进行匹配，并在“供应商发票”页对费用进行关帐。</span><span class="sxs-lookup"><span data-stu-id="b87d0-105">Then use the invoice pool to match the invoice to a purchase order and finalize the expense in the vendor invoice page.</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="b87d0-106">创建采购订单</span><span class="sxs-lookup"><span data-stu-id="b87d0-106">Create a purchase order</span></span>
1. <span data-ttu-id="b87d0-107">转到“应付账款”>“采购订单”>“采购订单”。</span><span class="sxs-lookup"><span data-stu-id="b87d0-107">Go to Accounts payable > Purchase orders > Purchase orders.</span></span>
2. <span data-ttu-id="b87d0-108">单击“新建”以创建新的采购订单。</span><span class="sxs-lookup"><span data-stu-id="b87d0-108">Click New to create a purchase order.</span></span>
3. <span data-ttu-id="b87d0-109">在“供应商帐户”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="b87d0-109">In the Vendor account field, click the drop down button to open the lookup.</span></span>
4. <span data-ttu-id="b87d0-110">从列表中选择供应商。</span><span class="sxs-lookup"><span data-stu-id="b87d0-110">Select the vendor from the list.</span></span> <span data-ttu-id="b87d0-111">例如，供应商 1001。</span><span class="sxs-lookup"><span data-stu-id="b87d0-111">For example, vendor 1001.</span></span>
5. <span data-ttu-id="b87d0-112">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="b87d0-112">Click OK.</span></span>
6. <span data-ttu-id="b87d0-113">在“物料编号”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="b87d0-113">In the Item number field, click the drop down button to open the lookup.</span></span>
7. <span data-ttu-id="b87d0-114">在该列表中查找服务物料编号。</span><span class="sxs-lookup"><span data-stu-id="b87d0-114">Find the services item number in the list.</span></span> <span data-ttu-id="b87d0-115">例如，选择 S0001。</span><span class="sxs-lookup"><span data-stu-id="b87d0-115">For example, select S0001.</span></span>
8. <span data-ttu-id="b87d0-116">单击物料编号并选择它。</span><span class="sxs-lookup"><span data-stu-id="b87d0-116">Click on the item number and select it.</span></span>
    * <span data-ttu-id="b87d0-117">净额为 75.00。</span><span class="sxs-lookup"><span data-stu-id="b87d0-117">The net amount is 75.00.</span></span>  <span data-ttu-id="b87d0-118">这是我们预期的发票金额。</span><span class="sxs-lookup"><span data-stu-id="b87d0-118">That is the amount that we will expect on the invoice.</span></span>  
9. <span data-ttu-id="b87d0-119">在操作窗格上，单击“采购”。</span><span class="sxs-lookup"><span data-stu-id="b87d0-119">On the action pane, click Purchase.</span></span>
10. <span data-ttu-id="b87d0-120">单击“确认”。</span><span class="sxs-lookup"><span data-stu-id="b87d0-120">Click Confirm.</span></span>

## <a name="create-and-post-and-invoice"></a><span data-ttu-id="b87d0-121">创建并过帐发票</span><span class="sxs-lookup"><span data-stu-id="b87d0-121">Create and post and invoice</span></span>
1. <span data-ttu-id="b87d0-122">转到“应付账款”>“发票”>“发票登记簿”。</span><span class="sxs-lookup"><span data-stu-id="b87d0-122">Go to Accounts payable > Invoices > Invoice register.</span></span>
2. <span data-ttu-id="b87d0-123">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="b87d0-123">Click New.</span></span>
3. <span data-ttu-id="b87d0-124">打开查找以选择您想使用的发票登记簿的名称。</span><span class="sxs-lookup"><span data-stu-id="b87d0-124">Open the lookup to select the name of the invoice register that you want to use.</span></span>
4. <span data-ttu-id="b87d0-125">选择您想要使用的发票登记簿名称。</span><span class="sxs-lookup"><span data-stu-id="b87d0-125">Select the name of the invoice register that you want to use.</span></span>
5. <span data-ttu-id="b87d0-126">单击“行”，以打开登记簿和输入费用行。</span><span class="sxs-lookup"><span data-stu-id="b87d0-126">Click on Lines to open the register and enter expense lines.</span></span>
6. <span data-ttu-id="b87d0-127">在查找中，选择供应商。</span><span class="sxs-lookup"><span data-stu-id="b87d0-127">In the lookup, select a vendor.</span></span> <span data-ttu-id="b87d0-128">例如，单击供应商 1001 。</span><span class="sxs-lookup"><span data-stu-id="b87d0-128">For example, click on vendor 1001.</span></span>
7. <span data-ttu-id="b87d0-129">在“发票”字段中，输入发票编号。</span><span class="sxs-lookup"><span data-stu-id="b87d0-129">In the Invoice field, enter the invoice number.</span></span>
8. <span data-ttu-id="b87d0-130">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="b87d0-130">In the Description field, type a value.</span></span>
9. <span data-ttu-id="b87d0-131">在“信用”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="b87d0-131">In the Credit field, enter a number.</span></span>
10. <span data-ttu-id="b87d0-132">在“采购订单”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="b87d0-132">In the Purchase order field, click the drop down button to open the lookup.</span></span>
11. <span data-ttu-id="b87d0-133">选择您之前创建的采购订单。</span><span class="sxs-lookup"><span data-stu-id="b87d0-133">Select the purchase order that you created earlier.</span></span>
12. <span data-ttu-id="b87d0-134">在“审核人”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="b87d0-134">In the Approved by field, click the drop down button to open the lookup.</span></span>
13. <span data-ttu-id="b87d0-135">突出显示一个审核人，然后单击“选择”以选择该审核人。</span><span class="sxs-lookup"><span data-stu-id="b87d0-135">Highlight an approver and click Select to select that approver.</span></span>
14. <span data-ttu-id="b87d0-136">单击“过帐”。</span><span class="sxs-lookup"><span data-stu-id="b87d0-136">Click Post.</span></span>
15. <span data-ttu-id="b87d0-137">关闭窗体。</span><span class="sxs-lookup"><span data-stu-id="b87d0-137">Close the form.</span></span>
16. <span data-ttu-id="b87d0-138">关闭窗体。</span><span class="sxs-lookup"><span data-stu-id="b87d0-138">Close the form.</span></span>

## <a name="open-an-invoice-from-the-pool-and-match-it-to-a-purchase-order-to-complete-the-invoice-process"></a><span data-ttu-id="b87d0-139">从发票池中打开发票并与采购订单进行匹配以此完成发票流程</span><span class="sxs-lookup"><span data-stu-id="b87d0-139">Open an invoice from the pool and match it to a purchase order to complete the invoice process</span></span>
1. <span data-ttu-id="b87d0-140">转到“应付账款”>“发票”>“发票池”。</span><span class="sxs-lookup"><span data-stu-id="b87d0-140">Go to Accounts payable > Invoices > Invoice pool.</span></span>
2. <span data-ttu-id="b87d0-141">单击“采购订单”以从发票池中的发票中创建供应商发票。</span><span class="sxs-lookup"><span data-stu-id="b87d0-141">Click Purchase order to create a vendor invoice from the invoice in the pool.</span></span>
3. <span data-ttu-id="b87d0-142">选择您想要查看的发票。</span><span class="sxs-lookup"><span data-stu-id="b87d0-142">Select the invoice that you want to review.</span></span>
4. <span data-ttu-id="b87d0-143">单击“更新匹配状态”以完成匹配。</span><span class="sxs-lookup"><span data-stu-id="b87d0-143">Click Update match status to complete the matching.</span></span>
5. <span data-ttu-id="b87d0-144">在操作窗格上，单击“选项”。</span><span class="sxs-lookup"><span data-stu-id="b87d0-144">On the action pane, click Options.</span></span>
6. <span data-ttu-id="b87d0-145">单击“更改”视图。</span><span class="sxs-lookup"><span data-stu-id="b87d0-145">Click Change view.</span></span>
7. <span data-ttu-id="b87d0-146">单击“网格”视图。</span><span class="sxs-lookup"><span data-stu-id="b87d0-146">Click Grid view.</span></span>
8. <span data-ttu-id="b87d0-147">单击“过帐”。</span><span class="sxs-lookup"><span data-stu-id="b87d0-147">Click Post.</span></span>
9. <span data-ttu-id="b87d0-148">关闭窗体。</span><span class="sxs-lookup"><span data-stu-id="b87d0-148">Close the form.</span></span>
10. <span data-ttu-id="b87d0-149">转到“应付账款”>“供应商”>“供应商”。</span><span class="sxs-lookup"><span data-stu-id="b87d0-149">Go to Accounts payable > Vendors > Vendors.</span></span>
11. <span data-ttu-id="b87d0-150">选择采购订单上的供应商。</span><span class="sxs-lookup"><span data-stu-id="b87d0-150">Select the vendor that was on the purchase order.</span></span> <span data-ttu-id="b87d0-151">例如，选择供应商 1001。</span><span class="sxs-lookup"><span data-stu-id="b87d0-151">For example, select vendor 1001.</span></span>
12. <span data-ttu-id="b87d0-152">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="b87d0-152">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="b87d0-153">在操作窗格上，单击“供应商”。</span><span class="sxs-lookup"><span data-stu-id="b87d0-153">On the action pane, click Vendor.</span></span>
14. <span data-ttu-id="b87d0-154">单击“交易记录”。</span><span class="sxs-lookup"><span data-stu-id="b87d0-154">Click Transactions.</span></span>
15. <span data-ttu-id="b87d0-155">选择您创建的发票。</span><span class="sxs-lookup"><span data-stu-id="b87d0-155">Select the invoice that you created.</span></span>
    * <span data-ttu-id="b87d0-156">发票登记簿应计项目被冲销并被过帐到相应的费用帐户。</span><span class="sxs-lookup"><span data-stu-id="b87d0-156">The invoice register accrual was reversed and posted to the appropriate expense account.</span></span>  


