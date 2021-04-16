---
title: 使用发票池将发票数据键入 AP 系统
description: 此主题介绍如何使用发票登记簿创建发票。
author: abruer
ms.date: 07/31/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b9c54f610e45d288ed58fd209d290d73bfe1ff2f
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5820657"
---
# <a name="key-invoice-data-into-the-ap-system-using-invoice-pool"></a><span data-ttu-id="e48e4-103">使用发票池将发票数据键入 AP 系统</span><span class="sxs-lookup"><span data-stu-id="e48e4-103">Key invoice data into the AP system using invoice pool</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e48e4-104">此主题介绍如何使用发票登记簿创建发票。</span><span class="sxs-lookup"><span data-stu-id="e48e4-104">This topic describes how to use the invoice register to create invoices.</span></span> <span data-ttu-id="e48e4-105">然后使用发票池对发票与采购订单进行匹配，并在“供应商发票”页对费用进行关帐。</span><span class="sxs-lookup"><span data-stu-id="e48e4-105">Then use the invoice pool to match the invoice to a purchase order and finalize the expense in the vendor invoice page.</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="e48e4-106">创建采购订单</span><span class="sxs-lookup"><span data-stu-id="e48e4-106">Create a purchase order</span></span>
1. <span data-ttu-id="e48e4-107">在导航窗格中，转到 **模块 > 应付帐款 > 采购订单 > 采购订单**。</span><span class="sxs-lookup"><span data-stu-id="e48e4-107">In the navigation pane, go to **Modules > Accounts payable > Purchase orders > Purchase orders**.</span></span>
2. <span data-ttu-id="e48e4-108">选择 **新建** 以创建新的采购订单。</span><span class="sxs-lookup"><span data-stu-id="e48e4-108">Select **New** to create a purchase order.</span></span>
3. <span data-ttu-id="e48e4-109">在 **供应商帐户** 字段中，从下拉列表选择供应商。</span><span class="sxs-lookup"><span data-stu-id="e48e4-109">In the **Vendor account** field, select a vendor for the drop-down list.</span></span> <span data-ttu-id="e48e4-110">例如，选择供应商 **1001**。</span><span class="sxs-lookup"><span data-stu-id="e48e4-110">For example, select vendor **1001**.</span></span>
4. <span data-ttu-id="e48e4-111">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="e48e4-111">Select **OK**.</span></span>
5. <span data-ttu-id="e48e4-112">在 **物料编号** 字段中，在下拉列表中选择服务物料编号。</span><span class="sxs-lookup"><span data-stu-id="e48e4-112">In the **Item number** field, select the services item number in the drop-down list.</span></span> <span data-ttu-id="e48e4-113">例如，选择 **S0001**。</span><span class="sxs-lookup"><span data-stu-id="e48e4-113">For example, select **S0001**.</span></span> <span data-ttu-id="e48e4-114">净额为 75.00。</span><span class="sxs-lookup"><span data-stu-id="e48e4-114">The net amount is 75.00.</span></span>  <span data-ttu-id="e48e4-115">这是我们预期的发票金额。</span><span class="sxs-lookup"><span data-stu-id="e48e4-115">That is the amount that we will expect on the invoice.</span></span>  
6. <span data-ttu-id="e48e4-116">在操作窗格上，选择 **采购**。</span><span class="sxs-lookup"><span data-stu-id="e48e4-116">On the action pane, select **Purchase**.</span></span>
7. <span data-ttu-id="e48e4-117">选择 **确认**。</span><span class="sxs-lookup"><span data-stu-id="e48e4-117">Select **Confirm**.</span></span>

## <a name="create-and-post-and-invoice"></a><span data-ttu-id="e48e4-118">创建并过帐发票</span><span class="sxs-lookup"><span data-stu-id="e48e4-118">Create and post and invoice</span></span>
1. <span data-ttu-id="e48e4-119">在导航窗格中，转到 **模块 > 应付帐款 > 发票 > 发票登记簿**。</span><span class="sxs-lookup"><span data-stu-id="e48e4-119">In the navigation pane, go to **Modules > Accounts payable > Invoices > Invoice register**.</span></span>
2. <span data-ttu-id="e48e4-120">选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="e48e4-120">Select **New**.</span></span>
3. <span data-ttu-id="e48e4-121">打开查找以选择您想使用的发票登记簿的名称。</span><span class="sxs-lookup"><span data-stu-id="e48e4-121">Open the lookup to select the name of the invoice register that you want to use.</span></span>
4. <span data-ttu-id="e48e4-122">选择您想要使用的发票登记簿名称。</span><span class="sxs-lookup"><span data-stu-id="e48e4-122">Select the name of the invoice register that you want to use.</span></span>
5. <span data-ttu-id="e48e4-123">单击 **行**，以打开登记簿和输入费用行。</span><span class="sxs-lookup"><span data-stu-id="e48e4-123">Select **Lines** to open the register and enter expense lines.</span></span>
6. <span data-ttu-id="e48e4-124">在查找中，选择供应商。</span><span class="sxs-lookup"><span data-stu-id="e48e4-124">In the lookup, select a vendor.</span></span> <span data-ttu-id="e48e4-125">例如，选择供应商 **1001**。</span><span class="sxs-lookup"><span data-stu-id="e48e4-125">For example, select vendor **1001**.</span></span>
7. <span data-ttu-id="e48e4-126">在 **发票** 字段中，输入发票编号。</span><span class="sxs-lookup"><span data-stu-id="e48e4-126">In the **Invoice** field, enter the invoice number.</span></span>
8. <span data-ttu-id="e48e4-127">在 **描述** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="e48e4-127">In the **Description** field, type a value.</span></span>
9. <span data-ttu-id="e48e4-128">在 **信用** 字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="e48e4-128">In the **Credit** field, enter a number.</span></span>
10. <span data-ttu-id="e48e4-129">在 **采购订单** 字段中，打开下拉列表选择您之前创建的采购订单。</span><span class="sxs-lookup"><span data-stu-id="e48e4-129">In the **Purchase order** field, open the drop-down list to select the purchase order that you created earlier.</span></span>
11. <span data-ttu-id="e48e4-130">在 **审核人** 字段中，在下拉列表中突出显示一个审核人，然后单击 **选择** 选择该审核人。</span><span class="sxs-lookup"><span data-stu-id="e48e4-130">In the **Approved by** field, highlight an approver in the drop-down list and click **Select** to select that approver.</span></span>
12. <span data-ttu-id="e48e4-131">选择 **过帐**。</span><span class="sxs-lookup"><span data-stu-id="e48e4-131">Select **Post**.</span></span>

## <a name="open-an-invoice-from-the-pool-and-match-it-to-a-purchase-order-to-complete-the-invoice-process"></a><span data-ttu-id="e48e4-132">从发票池中打开发票并与采购订单进行匹配以此完成发票流程</span><span class="sxs-lookup"><span data-stu-id="e48e4-132">Open an invoice from the pool and match it to a purchase order to complete the invoice process</span></span>
1. <span data-ttu-id="e48e4-133">在导航窗格中，转到 **模块 > 应付帐款 > 发票 > 发票池**。</span><span class="sxs-lookup"><span data-stu-id="e48e4-133">In the navigation pane, go to **Modules > Accounts payable > Invoices > Invoice pool**.</span></span>
2. <span data-ttu-id="e48e4-134">选择 **采购订单** 以从池中的发票中创建供应商发票。</span><span class="sxs-lookup"><span data-stu-id="e48e4-134">Select **Purchase order** to create a vendor invoice from the invoice in the pool.</span></span>
3. <span data-ttu-id="e48e4-135">选择您想要查看的发票。</span><span class="sxs-lookup"><span data-stu-id="e48e4-135">Select the invoice that you want to review.</span></span>
4. <span data-ttu-id="e48e4-136">选择 **更新匹配状态** 以完成匹配。</span><span class="sxs-lookup"><span data-stu-id="e48e4-136">Select **Update match status** to complete the matching.</span></span>
5. <span data-ttu-id="e48e4-137">在操作窗格上，选择 **选项**。</span><span class="sxs-lookup"><span data-stu-id="e48e4-137">On the action pane, select **Options**.</span></span>
6. <span data-ttu-id="e48e4-138">选择 **更改视图**。</span><span class="sxs-lookup"><span data-stu-id="e48e4-138">Select **Change view**.</span></span>
7. <span data-ttu-id="e48e4-139">选择 **网格视图**。</span><span class="sxs-lookup"><span data-stu-id="e48e4-139">Select **Grid view**.</span></span>
8. <span data-ttu-id="e48e4-140">选择 **过帐**。</span><span class="sxs-lookup"><span data-stu-id="e48e4-140">Select **Post**.</span></span>
9. <span data-ttu-id="e48e4-141">关闭窗体。</span><span class="sxs-lookup"><span data-stu-id="e48e4-141">Close the form.</span></span>
10. <span data-ttu-id="e48e4-142">在导航窗格中，转到 **模块 > 应付帐款 > 供应商 > 供应商**。</span><span class="sxs-lookup"><span data-stu-id="e48e4-142">In the navigation pane, go to **Modules > Accounts payable > Vendors > Vendors**.</span></span>
11. <span data-ttu-id="e48e4-143">选择采购订单上的供应商。</span><span class="sxs-lookup"><span data-stu-id="e48e4-143">Select the vendor that was on the purchase order.</span></span> <span data-ttu-id="e48e4-144">例如，选择供应商 **1001**。</span><span class="sxs-lookup"><span data-stu-id="e48e4-144">For example, select vendor **1001**.</span></span>
12. <span data-ttu-id="e48e4-145">在操作窗格上，选择 **供应商**。</span><span class="sxs-lookup"><span data-stu-id="e48e4-145">On the action pane, select **Vendor**.</span></span>
13. <span data-ttu-id="e48e4-146">选择 **交易记录**。</span><span class="sxs-lookup"><span data-stu-id="e48e4-146">Select **Transactions**.</span></span>
14. <span data-ttu-id="e48e4-147">选择您创建的发票。</span><span class="sxs-lookup"><span data-stu-id="e48e4-147">Select the invoice that you created.</span></span> <span data-ttu-id="e48e4-148">发票登记簿应计项目被冲销并被过帐到相应的费用帐户。</span><span class="sxs-lookup"><span data-stu-id="e48e4-148">The invoice register accrual was reversed and posted to the appropriate expense account.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]