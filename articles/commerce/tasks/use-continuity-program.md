---
title: 使用连续性计划
description: 此过程逐步演示如何销售连续性计划和如何处理相关销售订单。
author: scott-tucker
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MCRCustomerService, MCRCustSearch, SalesTable, MCRContinuityCustInfo, MCRCustPaymLookup, CreditCardTokenization, CreditCardLookup, MCRSalesOrderRecap
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5b641fb6ba5edf359a2f1f2de7b5095d73b497cf
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "5003620"
---
# <a name="using-continuity-program"></a><span data-ttu-id="1ff77-103">使用连续性计划</span><span class="sxs-lookup"><span data-stu-id="1ff77-103">Using continuity program</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1ff77-104">此过程逐步演示如何销售连续性计划和如何处理相关销售订单。</span><span class="sxs-lookup"><span data-stu-id="1ff77-104">This procedure walks through selling a continuity program and processing related sales orders.</span></span> <span data-ttu-id="1ff77-105">若要完成此过程，必须将用户设置为呼叫中心用户。</span><span class="sxs-lookup"><span data-stu-id="1ff77-105">To complete this procedure, the user has to be set up as a call center user.</span></span> <span data-ttu-id="1ff77-106">此程序使用 USRT 演示数据公司。</span><span class="sxs-lookup"><span data-stu-id="1ff77-106">This procedure uses the USRT demo data company.</span></span>

1. <span data-ttu-id="1ff77-107">转至“Retail 和 Commerce”>“客户”>“客户服务”。</span><span class="sxs-lookup"><span data-stu-id="1ff77-107">Go to Retail and Commerce > Customers > Customer service.</span></span>
2. <span data-ttu-id="1ff77-108">在“SearchText”字段中，键入“Karen”，然后按 Tab 键。</span><span class="sxs-lookup"><span data-stu-id="1ff77-108">In the SearchText field, type 'Karen' and then press the Tab key.</span></span>
    * <span data-ttu-id="1ff77-109">应弹出高级搜索对话框。</span><span class="sxs-lookup"><span data-stu-id="1ff77-109">The advanced search dialog should pop up.</span></span> <span data-ttu-id="1ff77-110">如果不弹出，请单击此字段右侧的“搜索”。</span><span class="sxs-lookup"><span data-stu-id="1ff77-110">If it doesn't, click Search to the right of this field.</span></span>  
3. <span data-ttu-id="1ff77-111">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="1ff77-111">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="1ff77-112">应该只有一行在显示 Karen Berg。</span><span class="sxs-lookup"><span data-stu-id="1ff77-112">There should be only one row with Karen Berg showing.</span></span> <span data-ttu-id="1ff77-113">通过单击网格最左侧的复选标记列选中行。</span><span class="sxs-lookup"><span data-stu-id="1ff77-113">Select the row by clicking on the checkmark column on the far left of the grid.</span></span>  
4. <span data-ttu-id="1ff77-114">单击“选择”。</span><span class="sxs-lookup"><span data-stu-id="1ff77-114">Click Select.</span></span>
5. <span data-ttu-id="1ff77-115">单击“新建销售订单”。</span><span class="sxs-lookup"><span data-stu-id="1ff77-115">Click New sales order.</span></span>
    * <span data-ttu-id="1ff77-116">最好记下销售订单编号。</span><span class="sxs-lookup"><span data-stu-id="1ff77-116">It's a good idea to note the sales order number.</span></span> <span data-ttu-id="1ff77-117">此过程的后面需要该编号。</span><span class="sxs-lookup"><span data-stu-id="1ff77-117">You'll need it later in this procedure.</span></span>  
6. <span data-ttu-id="1ff77-118">在“物料编号”字段中，键入“88000”，然后按 Tab 键。</span><span class="sxs-lookup"><span data-stu-id="1ff77-118">In the Item number field, type '88000' and then press the Tab key.</span></span>
    * <span data-ttu-id="1ff77-119">这是 USRT 演示数据中的一个连续性物料。</span><span class="sxs-lookup"><span data-stu-id="1ff77-119">This is a continuity item in the USRT demo data.</span></span>  
7. <span data-ttu-id="1ff77-120">单击“完成”。</span><span class="sxs-lookup"><span data-stu-id="1ff77-120">Click Complete.</span></span>
8. <span data-ttu-id="1ff77-121">在“付款方式”字段中，输入“Visa”。</span><span class="sxs-lookup"><span data-stu-id="1ff77-121">In the Payment method field, enter 'Visa'.</span></span>
9. <span data-ttu-id="1ff77-122">单击“添加信用卡”。</span><span class="sxs-lookup"><span data-stu-id="1ff77-122">Click Add credit card.</span></span>
    * <span data-ttu-id="1ff77-123">在此页中输入所需信用卡信息。</span><span class="sxs-lookup"><span data-stu-id="1ff77-123">Enter the required credit card information on this page.</span></span>  
10. <span data-ttu-id="1ff77-124">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="1ff77-124">Click OK.</span></span>
11. <span data-ttu-id="1ff77-125">展开付款窗口。</span><span class="sxs-lookup"><span data-stu-id="1ff77-125">Expand the Payment section.</span></span>
    * <span data-ttu-id="1ff77-126">若要提交呼叫中心订单，必须为该订单输入付款。</span><span class="sxs-lookup"><span data-stu-id="1ff77-126">To submit a call center order, payments have to be entered for the order.</span></span>  
12. <span data-ttu-id="1ff77-127">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="1ff77-127">Click OK.</span></span>
13. <span data-ttu-id="1ff77-128">单击“提交”。</span><span class="sxs-lookup"><span data-stu-id="1ff77-128">Click Submit.</span></span>
    * <span data-ttu-id="1ff77-129">您已创建完了新连续性订单。</span><span class="sxs-lookup"><span data-stu-id="1ff77-129">You're done creating a new continuity order.</span></span> <span data-ttu-id="1ff77-130">接下来，您将运行两个批处理流程，用于处理这些连续性订单。</span><span class="sxs-lookup"><span data-stu-id="1ff77-130">Next, you'll run two batch processes that are used to process the continuity orders.</span></span>  
14. <span data-ttu-id="1ff77-131">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="1ff77-131">Close the page.</span></span>
15. <span data-ttu-id="1ff77-132">转至“Retail 和 Commerce”>“连续性”>“处理连续性付款”。</span><span class="sxs-lookup"><span data-stu-id="1ff77-132">Go to Retail and Commerce > Continuity > Process continuity payments.</span></span>
16. <span data-ttu-id="1ff77-133">在“连续性物料”字段中，键入“88000”，然后按 Tab 键。</span><span class="sxs-lookup"><span data-stu-id="1ff77-133">In the Continuity item field, type '88000' and then press the Tab key.</span></span>
17. <span data-ttu-id="1ff77-134">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="1ff77-134">Click OK.</span></span>
18. <span data-ttu-id="1ff77-135">转至“Retail 和 Commerce”>“连续性”>“创建连续性子订单”。</span><span class="sxs-lookup"><span data-stu-id="1ff77-135">Go to Retail and Commerce > Continuity > Create continuity child orders.</span></span>
    * <span data-ttu-id="1ff77-136">此流程将基于您的连续性计划的设置创建新销售订单。</span><span class="sxs-lookup"><span data-stu-id="1ff77-136">This process will create new sales orders based on the settings of your continuity programs.</span></span>  
19. <span data-ttu-id="1ff77-137">在“连续性物料”字段中，键入“88000”，然后按 Tab 键。</span><span class="sxs-lookup"><span data-stu-id="1ff77-137">In the Continuity item field, type '88000' and then press the Tab key.</span></span>
    * <span data-ttu-id="1ff77-138">物料“88000”是 USRT 演示数据中的一个连续性物料。</span><span class="sxs-lookup"><span data-stu-id="1ff77-138">Item '88000' is a continuity item in the USRT demo data.</span></span>  
20. <span data-ttu-id="1ff77-139">在“销售订单”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="1ff77-139">In the Sales order field, enter or select a value.</span></span>
    * <span data-ttu-id="1ff77-140">输入您在此过程中前面记下的销售订单编号。</span><span class="sxs-lookup"><span data-stu-id="1ff77-140">Enter the sales order number that you noted earlier in the procedure.</span></span> <span data-ttu-id="1ff77-141">这将让此过程的处理时间降到最低。</span><span class="sxs-lookup"><span data-stu-id="1ff77-141">This will keep the processing time to a minimal for this procedure.</span></span> <span data-ttu-id="1ff77-142">“销售订单”字段为可选字段，您可以处理任一计划的所有订单。</span><span class="sxs-lookup"><span data-stu-id="1ff77-142">The Sales order field field is optional--you could process all orders for any one program.</span></span>  
21. <span data-ttu-id="1ff77-143">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="1ff77-143">Click OK.</span></span>

