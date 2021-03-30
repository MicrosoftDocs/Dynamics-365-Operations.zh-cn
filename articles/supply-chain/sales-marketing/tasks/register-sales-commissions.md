---
title: 登记销售佣金
description: 此主题介绍如何计算和登记销售佣金。
author: omulvad
manager: tfehr
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, SalesEditLines,  CustInvoiceJournal, CommissionTrans, LedgerTransVoucher, CustClassificationGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 82c8dc2f284923b5583bf983413a015b9ece8252
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5205921"
---
# <a name="register-sales-commissions"></a><span data-ttu-id="945a1-103">登记销售佣金</span><span class="sxs-lookup"><span data-stu-id="945a1-103">Register sales commissions</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="945a1-104">此主题介绍如何计算和登记销售佣金。</span><span class="sxs-lookup"><span data-stu-id="945a1-104">This topic explains how sales commissions are calculated and registered.</span></span> <span data-ttu-id="945a1-105">您可以使用 USMF 公司演示数据，也可使用您自己的数据运行该过程。</span><span class="sxs-lookup"><span data-stu-id="945a1-105">You can run this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="945a1-106">在开始此指南前，运行名为“设置销售佣金规则”的指南，以确保您已设置好所有必要的佣金计算设置。</span><span class="sxs-lookup"><span data-stu-id="945a1-106">Before starting this guide, run the guide called "Set up sales commission rules" to make sure that you have all the necessary commission calculation setup.</span></span>

<span data-ttu-id="945a1-107">记录您为佣金过程选择的客户和物料编号，并在创建本指南的销售订单时使用。</span><span class="sxs-lookup"><span data-stu-id="945a1-107">Take note of the customer and item numbers that you have chosen for the commission process and use them when asked to create a sales order in this guide.</span></span>


## <a name="invoice-a-sales-order-that-qualifies-a-salesperson-for-a-commission"></a><span data-ttu-id="945a1-108">为销售人员符合佣金资格的销售订单开票</span><span class="sxs-lookup"><span data-stu-id="945a1-108">Invoice a sales order that qualifies a salesperson for a commission</span></span>
1. <span data-ttu-id="945a1-109">在导航窗格中，转到 **模块 > 销售和营销 > 销售订单 > 所有销售订单**。</span><span class="sxs-lookup"><span data-stu-id="945a1-109">In the navigation pane, go to **Modules > Sales and marketing > Sales orders > All sales orders**.</span></span>
2. <span data-ttu-id="945a1-110">选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="945a1-110">Select **New**.</span></span>
3. <span data-ttu-id="945a1-111">在 **客户帐户** 字段中，从下拉菜单选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="945a1-111">In the **Customer account** field, select the desired record from the drop-down menu.</span></span>
4. <span data-ttu-id="945a1-112">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="945a1-112">Select **OK**.</span></span>
5. <span data-ttu-id="945a1-113">在操作窗格上，选择 **选项**。</span><span class="sxs-lookup"><span data-stu-id="945a1-113">On the Action Pane, select **Options**.</span></span>
6. <span data-ttu-id="945a1-114">选择 **更改视图**。</span><span class="sxs-lookup"><span data-stu-id="945a1-114">Select **Change view**.</span></span>
7. <span data-ttu-id="945a1-115">选择 **标题视图**。</span><span class="sxs-lookup"><span data-stu-id="945a1-115">Select **Header view**.</span></span>
8. <span data-ttu-id="945a1-116">展开 **设置** 部分。</span><span class="sxs-lookup"><span data-stu-id="945a1-116">Expand the **Setup** section.</span></span>

    - <span data-ttu-id="945a1-117">**销售组** 字段中的值代表有一名或多名指派的销售代表的组。</span><span class="sxs-lookup"><span data-stu-id="945a1-117">The value in the **Sales group** field represents a group with one or more sales representatives assigned to it.</span></span> <span data-ttu-id="945a1-118">组中的人员为在订单开票时以预定义的比率和分配规则接受佣金的人员。</span><span class="sxs-lookup"><span data-stu-id="945a1-118">The people in the group are the ones who will receive commissions when the order is invoiced, as per predefined rates and distribution.</span></span>   
    - <span data-ttu-id="945a1-119">该值复制自客户卡，但如果您想更改则可以更改。</span><span class="sxs-lookup"><span data-stu-id="945a1-119">The value is copied from the Customer card, but you can change it if you wish.</span></span>  
    - <span data-ttu-id="945a1-120">销售组还复制到销售订单行。</span><span class="sxs-lookup"><span data-stu-id="945a1-120">The Sales group is also copied to the sales order line.</span></span> <span data-ttu-id="945a1-121">您可以更改它，使其与标题和/或行之间的名称不同。</span><span class="sxs-lookup"><span data-stu-id="945a1-121">You can change it so that it can differ from the one in the header and/or between lines.</span></span>  
    - <span data-ttu-id="945a1-122">**佣金组** 字段的值代表您出于跟踪佣金目的为一个或多个客户创建的组。</span><span class="sxs-lookup"><span data-stu-id="945a1-122">The value in the **Commission group** field represents a group that you have created for one or more customers with the purpose of tracking commissions.</span></span>   
    - <span data-ttu-id="945a1-123">该值复制自客户卡，但如果您想更改则可以更改。</span><span class="sxs-lookup"><span data-stu-id="945a1-123">The value is copied from the Customer card, but you can change it if you wish.</span></span>   

9. <span data-ttu-id="945a1-124">在操作窗格上，选择 **选项**。</span><span class="sxs-lookup"><span data-stu-id="945a1-124">On the Action Pane, select **Options**.</span></span>
10. <span data-ttu-id="945a1-125">选择 **更改视图**。</span><span class="sxs-lookup"><span data-stu-id="945a1-125">Select **Change view**.</span></span>
11. <span data-ttu-id="945a1-126">选择 **行视图**。</span><span class="sxs-lookup"><span data-stu-id="945a1-126">Select **Line view**.</span></span>
12. <span data-ttu-id="945a1-127">在 **物料编号** 字段的下拉菜单中，选择已为其设置了佣金的物料。</span><span class="sxs-lookup"><span data-stu-id="945a1-127">In the drop down menu of the **Item number** field, select the item you have set up for commissions.</span></span> 
13. <span data-ttu-id="945a1-128">在 **数量** 字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="945a1-128">In the **Quantity** field, enter a number.</span></span> <span data-ttu-id="945a1-129">记录行的净额。</span><span class="sxs-lookup"><span data-stu-id="945a1-129">Take note of the line's Net amount.</span></span> <span data-ttu-id="945a1-130">它代表销售收入，在此示例中它是佣金计算的基础。</span><span class="sxs-lookup"><span data-stu-id="945a1-130">It represents the sales revenue, which in this example is the basis for commission calculation.</span></span>  
14. <span data-ttu-id="945a1-131">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="945a1-131">Select **Save**.</span></span>
15. <span data-ttu-id="945a1-132">在操作窗格上，选择 **发票**。</span><span class="sxs-lookup"><span data-stu-id="945a1-132">On the Action Pane, select **Invoice**.</span></span>
16. <span data-ttu-id="945a1-133">选择 **发票**。</span><span class="sxs-lookup"><span data-stu-id="945a1-133">Select **Invoice**.</span></span>
17. <span data-ttu-id="945a1-134">展开 **参数** 部分。</span><span class="sxs-lookup"><span data-stu-id="945a1-134">Expand the **Parameters** section.</span></span>
18. <span data-ttu-id="945a1-135">在 **数量** 字段中，选择 **全部**。</span><span class="sxs-lookup"><span data-stu-id="945a1-135">In the **Quantity** field, select **All**.</span></span>
19. <span data-ttu-id="945a1-136">在 **过帐** 字段中选择 **是**。</span><span class="sxs-lookup"><span data-stu-id="945a1-136">Select **Yes** in the **Posting** field.</span></span>
20. <span data-ttu-id="945a1-137">选择 **确定**，然后在下一个窗格中选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="945a1-137">Select **OK**, then select **OK** in the next pane.</span></span> <span data-ttu-id="945a1-138">过帐交易记录可能需要大概一分钟。</span><span class="sxs-lookup"><span data-stu-id="945a1-138">It may take a minute or so to post the transaction.</span></span> <span data-ttu-id="945a1-139">允许完成处理，并且不关闭页面。</span><span class="sxs-lookup"><span data-stu-id="945a1-139">Allow the processing to complete and don't close the page.</span></span>  

## <a name="review-the-registered-sales-commissions"></a><span data-ttu-id="945a1-140">查看登记的销售佣金</span><span class="sxs-lookup"><span data-stu-id="945a1-140">Review the registered sales commissions</span></span>
1. <span data-ttu-id="945a1-141">在操作窗格上，选择 **发票**，然后再次选择 **发票**。</span><span class="sxs-lookup"><span data-stu-id="945a1-141">On the Action Pane, select **Invoice**, then select **Invoice** again.</span></span>
2. <span data-ttu-id="945a1-142">在操作窗格上，选择 **发票**，然后选择 **佣金交易记录**。</span><span class="sxs-lookup"><span data-stu-id="945a1-142">On the Action Pane, select **Invoice**, then select **Commission transactions**.</span></span>

    - <span data-ttu-id="945a1-143">**概览** 选项卡显示应付给与开票的销售订单相关的销售人员的佣金金额行。</span><span class="sxs-lookup"><span data-stu-id="945a1-143">The **Overview** tab displays lines representing the commission amounts payable to sales representatives who are associated with the invoiced sales order.</span></span> <span data-ttu-id="945a1-144">我们现在查看详细信息。</span><span class="sxs-lookup"><span data-stu-id="945a1-144">Let's review the details.</span></span>  
    - <span data-ttu-id="945a1-145">如果您使用“设置销售佣金规则”指南来设置 **佣金销售** 组，将有两位销售人员接受销售佣金，并且两人平分佣金。</span><span class="sxs-lookup"><span data-stu-id="945a1-145">If you used the "Set up sales commission rules" guide to set up the **Commission sales** group, there are two sales people to receive a sales commissions, and the commission is split equally between them.</span></span>  
    - <span data-ttu-id="945a1-146">在此示例中，佣金的总金额计算为销售收入百分比（订单行的净额）。</span><span class="sxs-lookup"><span data-stu-id="945a1-146">In this example, the total amount of the commission is calculated as a percentage of the sales revenue (the net amount of order line).</span></span>  
3. <span data-ttu-id="945a1-147">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="945a1-147">Close the page.</span></span>
4. <span data-ttu-id="945a1-148">选择 **凭证**。</span><span class="sxs-lookup"><span data-stu-id="945a1-148">Select **Voucher**.</span></span> <span data-ttu-id="945a1-149">您可以在凭证交易记录中查看已过帐到预定义的佣金费用的佣金金额和应付佣金金额。</span><span class="sxs-lookup"><span data-stu-id="945a1-149">You can review the voucher transactions for the commission amounts that have been posted to the predefined commission expense and commission payable accounts.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]