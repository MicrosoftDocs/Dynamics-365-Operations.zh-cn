--- 
title: "登记销售佣金"
description: "该过程显示如何计算和登记销售佣金。"
author: omulvad
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, SalesEditLines,  CustInvoiceJournal, CommissionTrans, LedgerTransVoucher
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 2c39b2fcf521106dfb58466bc45a316c0b506345
ms.contentlocale: zh-cn
ms.lasthandoff: 09/14/2018

---
# <a name="register-sales-commissions"></a><span data-ttu-id="e4a1c-103">登记销售佣金</span><span class="sxs-lookup"><span data-stu-id="e4a1c-103">Register sales commissions</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e4a1c-104">该过程显示如何计算和登记销售佣金。</span><span class="sxs-lookup"><span data-stu-id="e4a1c-104">This procedure shows you how sales commissions are calculated and registered.</span></span> <span data-ttu-id="e4a1c-105">您可以使用 USMF 公司演示数据，也可使用您自己的数据运行该过程。</span><span class="sxs-lookup"><span data-stu-id="e4a1c-105">You can run this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="e4a1c-106">在开始此指南前，运行名为“设置销售佣金规则”的指南，以确保您已设置好所有必要的佣金计算设置。</span><span class="sxs-lookup"><span data-stu-id="e4a1c-106">Before starting this guide, run the guide called "Set up sales commission rules" to make sure that you have all the necessary commission calculation setup.</span></span>

<span data-ttu-id="e4a1c-107">记录您为佣金过程选择的客户和物料编号，并在创建本指南的销售订单时使用。</span><span class="sxs-lookup"><span data-stu-id="e4a1c-107">Take note of the customer and item numbers that you have chosen for the commission process and use them when asked to create a sales order in this guide.</span></span>


## <a name="invoice-a-sales-order-that-qualifies-a-salesperson-for-a-commission"></a><span data-ttu-id="e4a1c-108">为销售人员符合佣金资格的销售订单开票</span><span class="sxs-lookup"><span data-stu-id="e4a1c-108">Invoice a sales order that qualifies a salesperson for a commission</span></span>
1. <span data-ttu-id="e4a1c-109">转至“销售和营销”>“销售订单”>“所有销售订单”。</span><span class="sxs-lookup"><span data-stu-id="e4a1c-109">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
2. <span data-ttu-id="e4a1c-110">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="e4a1c-110">Click New.</span></span>
3. <span data-ttu-id="e4a1c-111">在“客户帐户”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="e4a1c-111">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="e4a1c-112">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="e4a1c-112">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="e4a1c-113">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="e4a1c-113">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="e4a1c-114">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="e4a1c-114">Click OK.</span></span>
7. <span data-ttu-id="e4a1c-115">在“操作窗格”上，单击“选项”。</span><span class="sxs-lookup"><span data-stu-id="e4a1c-115">On the Action Pane, click Options.</span></span>
8. <span data-ttu-id="e4a1c-116">单击“更改”视图。</span><span class="sxs-lookup"><span data-stu-id="e4a1c-116">Click Change view.</span></span>
9. <span data-ttu-id="e4a1c-117">单击“标题”视图。</span><span class="sxs-lookup"><span data-stu-id="e4a1c-117">Click Header view.</span></span>
10. <span data-ttu-id="e4a1c-118">展开“设置”部分。</span><span class="sxs-lookup"><span data-stu-id="e4a1c-118">Expand the Setup section.</span></span>
    * <span data-ttu-id="e4a1c-119">“销售组”字段中的值代表有一名或多名指派的销售代表的组。</span><span class="sxs-lookup"><span data-stu-id="e4a1c-119">The value in the Sales group field represents a group with one or more sales representatives assigned to it.</span></span> <span data-ttu-id="e4a1c-120">组中的人员为在订单开票时以预定义的比率和分配规则接受佣金的人员。</span><span class="sxs-lookup"><span data-stu-id="e4a1c-120">The people in the group are the ones who will receive commissions when the order is invoiced, as per predefined rates and distribution.</span></span>   <span data-ttu-id="e4a1c-121">该值复制自客户卡，但如果您想更改则可以更改。</span><span class="sxs-lookup"><span data-stu-id="e4a1c-121">The value is copied from the Customer card, but you can change it if you wish.</span></span>  <span data-ttu-id="e4a1c-122">销售组还复制到销售订单行。</span><span class="sxs-lookup"><span data-stu-id="e4a1c-122">The Sales group is also copied to the sales order line.</span></span> <span data-ttu-id="e4a1c-123">您可以更改它，使其与标题和/或行之间的名称不同。</span><span class="sxs-lookup"><span data-stu-id="e4a1c-123">You can change it so that it can differ from the one in the header and/or between lines.</span></span>  
    * <span data-ttu-id="e4a1c-124">“佣金组”字段的值代表您出于跟踪佣金目的为一个或多个客户创建的组。</span><span class="sxs-lookup"><span data-stu-id="e4a1c-124">The value in the Commission group field represents a group that you have created for one or more customers with the purpose of tracking commissions.</span></span>   <span data-ttu-id="e4a1c-125">该值复制自客户卡，但如果您想更改则可以更改。</span><span class="sxs-lookup"><span data-stu-id="e4a1c-125">The value is copied from the Customer card, but you can change it if you wish.</span></span>   
11. <span data-ttu-id="e4a1c-126">在“操作窗格”上，单击“选项”。</span><span class="sxs-lookup"><span data-stu-id="e4a1c-126">On the Action Pane, click Options.</span></span>
12. <span data-ttu-id="e4a1c-127">单击“更改”视图。</span><span class="sxs-lookup"><span data-stu-id="e4a1c-127">Click Change view.</span></span>
13. <span data-ttu-id="e4a1c-128">单击“查看行”。</span><span class="sxs-lookup"><span data-stu-id="e4a1c-128">Click Line view.</span></span>
14. <span data-ttu-id="e4a1c-129">在“物料编号”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="e4a1c-129">In the Item number field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="e4a1c-130">在列表中，选择为佣金设置的物料。</span><span class="sxs-lookup"><span data-stu-id="e4a1c-130">In the list, select the item you have set up for commissions.</span></span> 
16. <span data-ttu-id="e4a1c-131">在“数量”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="e4a1c-131">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="e4a1c-132">记录行的净额。</span><span class="sxs-lookup"><span data-stu-id="e4a1c-132">Take note of the line's Net amount.</span></span> <span data-ttu-id="e4a1c-133">它代表销售收入，在此示例中它是佣金计算的基础。</span><span class="sxs-lookup"><span data-stu-id="e4a1c-133">It represents the sales revenue, which in this example is the basis for commission calculation.</span></span>  
17. <span data-ttu-id="e4a1c-134">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="e4a1c-134">Click Save.</span></span>
18. <span data-ttu-id="e4a1c-135">在操作窗格上，单击“发票”。</span><span class="sxs-lookup"><span data-stu-id="e4a1c-135">On the Action Pane, click Invoice.</span></span>
19. <span data-ttu-id="e4a1c-136">单击“发票”。</span><span class="sxs-lookup"><span data-stu-id="e4a1c-136">Click Invoice.</span></span>
20. <span data-ttu-id="e4a1c-137">展开“参数”部分。</span><span class="sxs-lookup"><span data-stu-id="e4a1c-137">Expand the Parameters section.</span></span>
21. <span data-ttu-id="e4a1c-138">在“数量”字段中，选择“所有”。</span><span class="sxs-lookup"><span data-stu-id="e4a1c-138">In the Quantity field, select 'All'.</span></span>
22. <span data-ttu-id="e4a1c-139">在“过帐”字段中选择“是”。</span><span class="sxs-lookup"><span data-stu-id="e4a1c-139">Select Yes in the Posting field.</span></span>
23. <span data-ttu-id="e4a1c-140">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="e4a1c-140">Click OK.</span></span>
24. <span data-ttu-id="e4a1c-141">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="e4a1c-141">Click OK.</span></span>
    * <span data-ttu-id="e4a1c-142">过帐交易记录可能需要大概一分钟。</span><span class="sxs-lookup"><span data-stu-id="e4a1c-142">It may take a minute or so to post the transaction.</span></span> <span data-ttu-id="e4a1c-143">允许完成处理，并且不关闭页面。</span><span class="sxs-lookup"><span data-stu-id="e4a1c-143">Allow the processing to complete and don’t close the page.</span></span>  

## <a name="review-the-registered-sales-commissions"></a><span data-ttu-id="e4a1c-144">查看登记的销售佣金</span><span class="sxs-lookup"><span data-stu-id="e4a1c-144">Review the registered sales commissions</span></span>
1. <span data-ttu-id="e4a1c-145">在操作窗格上，单击“发票”。</span><span class="sxs-lookup"><span data-stu-id="e4a1c-145">On the Action Pane, click Invoice.</span></span>
2. <span data-ttu-id="e4a1c-146">单击“发票”。</span><span class="sxs-lookup"><span data-stu-id="e4a1c-146">Click Invoice.</span></span>
3. <span data-ttu-id="e4a1c-147">在操作窗格上，单击“发票”。</span><span class="sxs-lookup"><span data-stu-id="e4a1c-147">On the Action Pane, click Invoice.</span></span>
4. <span data-ttu-id="e4a1c-148">单击“佣金交易记录”。</span><span class="sxs-lookup"><span data-stu-id="e4a1c-148">Click Commission transactions.</span></span>
    * <span data-ttu-id="e4a1c-149">概览选项卡显示应付给与开票的销售订单相关的销售人员的佣金金额行。</span><span class="sxs-lookup"><span data-stu-id="e4a1c-149">The Overview tab displays lines representing the commission amounts payable to sales representatives who are associated with the invoiced sales order.</span></span> <span data-ttu-id="e4a1c-150">我们现在查看详细信息。</span><span class="sxs-lookup"><span data-stu-id="e4a1c-150">Let's review the details.</span></span>     
    * <span data-ttu-id="e4a1c-151">如果您使用“设置销售佣金规则”指南来设置佣金销售组，将有两位销售人员接受销售佣金，并且两人平分佣金。</span><span class="sxs-lookup"><span data-stu-id="e4a1c-151">If you used the "Set up sales commission rules" guide to set up the Commission sales group, there are two sales people to receive a sales commissions, and the commission is split equally between them.</span></span>  
    * <span data-ttu-id="e4a1c-152">在此示例中，佣金的总金额计算为销售收入百分比（订单行的净额）。</span><span class="sxs-lookup"><span data-stu-id="e4a1c-152">In this example, the total amount of the commission is calculated as a percentage of the sales revenue (the net amount of order line).</span></span>   
5. <span data-ttu-id="e4a1c-153">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="e4a1c-153">Close the page.</span></span>
6. <span data-ttu-id="e4a1c-154">单击“凭证”。</span><span class="sxs-lookup"><span data-stu-id="e4a1c-154">Click Voucher.</span></span>
    * <span data-ttu-id="e4a1c-155">您可以在凭证交易记录中查看已过帐到预定义的佣金费用的佣金金额和应付佣金金额。</span><span class="sxs-lookup"><span data-stu-id="e4a1c-155">You can review the voucher transactions for the commission amounts that have been posted to the predefined commission expense and commission payable accounts.</span></span>  


