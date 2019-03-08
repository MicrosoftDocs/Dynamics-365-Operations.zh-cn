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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 45bd4a3cc9f9b03c713d33638d6dc93aa696c581
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/29/2019
ms.locfileid: "358155"
---
# <a name="using-continuity-program"></a><span data-ttu-id="bb0bb-103">使用连续性计划</span><span class="sxs-lookup"><span data-stu-id="bb0bb-103">Using continuity program</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="bb0bb-104">此过程逐步演示如何销售连续性计划和如何处理相关销售订单。</span><span class="sxs-lookup"><span data-stu-id="bb0bb-104">This procedure walks through selling a continuity program and processing related sales orders.</span></span> <span data-ttu-id="bb0bb-105">若要完成此过程，必须将用户设置为呼叫中心用户。</span><span class="sxs-lookup"><span data-stu-id="bb0bb-105">To complete this procedure, the user has to be set up as a call center user.</span></span> <span data-ttu-id="bb0bb-106">此程序使用 USRT 演示数据公司。</span><span class="sxs-lookup"><span data-stu-id="bb0bb-106">This procedure uses the USRT demo data company.</span></span>

1. <span data-ttu-id="bb0bb-107">转至“零售和商业”>“客户”>“客户服务”。</span><span class="sxs-lookup"><span data-stu-id="bb0bb-107">Go to Retail and commerce > Customers > Customer service.</span></span>
2. <span data-ttu-id="bb0bb-108">在“SearchText”字段中，键入“Karen”，然后按 Tab 键。</span><span class="sxs-lookup"><span data-stu-id="bb0bb-108">In the SearchText field, type 'Karen' and then press the Tab key.</span></span>
    * <span data-ttu-id="bb0bb-109">应弹出高级搜索对话框。</span><span class="sxs-lookup"><span data-stu-id="bb0bb-109">The advanced search dialog should pop up.</span></span> <span data-ttu-id="bb0bb-110">如果不弹出，请单击此字段右侧的“搜索”。</span><span class="sxs-lookup"><span data-stu-id="bb0bb-110">If it doesn't, click Search to the right of this field.</span></span>  
3. <span data-ttu-id="bb0bb-111">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="bb0bb-111">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="bb0bb-112">应该只有一行在显示 Karen Berg。</span><span class="sxs-lookup"><span data-stu-id="bb0bb-112">There should be only one row with Karen Berg showing.</span></span> <span data-ttu-id="bb0bb-113">通过单击网格最左侧的复选标记列选中行。</span><span class="sxs-lookup"><span data-stu-id="bb0bb-113">Select the row by clicking on the checkmark column on the far left of the grid.</span></span>  
4. <span data-ttu-id="bb0bb-114">单击“选择”。</span><span class="sxs-lookup"><span data-stu-id="bb0bb-114">Click Select.</span></span>
5. <span data-ttu-id="bb0bb-115">单击“新建销售订单”。</span><span class="sxs-lookup"><span data-stu-id="bb0bb-115">Click New sales order.</span></span>
    * <span data-ttu-id="bb0bb-116">最好记下销售订单编号。</span><span class="sxs-lookup"><span data-stu-id="bb0bb-116">It's a good idea to note the sales order number.</span></span> <span data-ttu-id="bb0bb-117">此过程的后面需要该编号。</span><span class="sxs-lookup"><span data-stu-id="bb0bb-117">You'll need it later in this procedure.</span></span>  
6. <span data-ttu-id="bb0bb-118">在“物料编号”字段中，键入“88000”，然后按 Tab 键。</span><span class="sxs-lookup"><span data-stu-id="bb0bb-118">In the Item number field, type '88000' and then press the Tab key.</span></span>
    * <span data-ttu-id="bb0bb-119">这是 USRT 演示数据中的一个连续性物料。</span><span class="sxs-lookup"><span data-stu-id="bb0bb-119">This is a continuity item in the USRT demo data.</span></span>  
7. <span data-ttu-id="bb0bb-120">单击“完成”。</span><span class="sxs-lookup"><span data-stu-id="bb0bb-120">Click Complete.</span></span>
8. <span data-ttu-id="bb0bb-121">在“付款方式”字段中，输入“Visa”。</span><span class="sxs-lookup"><span data-stu-id="bb0bb-121">In the Payment method field, enter 'Visa'.</span></span>
9. <span data-ttu-id="bb0bb-122">单击“添加信用卡”。</span><span class="sxs-lookup"><span data-stu-id="bb0bb-122">Click Add credit card.</span></span>
    * <span data-ttu-id="bb0bb-123">在此页中输入所需信用卡信息。</span><span class="sxs-lookup"><span data-stu-id="bb0bb-123">Enter the required credit card information on this page.</span></span>  
10. <span data-ttu-id="bb0bb-124">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="bb0bb-124">Click OK.</span></span>
11. <span data-ttu-id="bb0bb-125">展开付款窗口。</span><span class="sxs-lookup"><span data-stu-id="bb0bb-125">Expand the Payment section.</span></span>
    * <span data-ttu-id="bb0bb-126">若要提交呼叫中心订单，必须为该订单输入付款。</span><span class="sxs-lookup"><span data-stu-id="bb0bb-126">To submit a call center order, payments have to be entered for the order.</span></span>  
12. <span data-ttu-id="bb0bb-127">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="bb0bb-127">Click OK.</span></span>
13. <span data-ttu-id="bb0bb-128">单击“提交”。</span><span class="sxs-lookup"><span data-stu-id="bb0bb-128">Click Submit.</span></span>
    * <span data-ttu-id="bb0bb-129">您已创建完了新连续性订单。</span><span class="sxs-lookup"><span data-stu-id="bb0bb-129">You're done creating a new continuity order.</span></span> <span data-ttu-id="bb0bb-130">接下来，您将运行两个批处理流程，用于处理这些连续性订单。</span><span class="sxs-lookup"><span data-stu-id="bb0bb-130">Next, you'll run two batch processes that are used to process the continuity orders.</span></span>  
14. <span data-ttu-id="bb0bb-131">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="bb0bb-131">Close the page.</span></span>
15. <span data-ttu-id="bb0bb-132">转至“零售和商业”>"连续性">“处理连续性付款”。</span><span class="sxs-lookup"><span data-stu-id="bb0bb-132">Go to Retail and commerce > Continuity > Process continuity payments.</span></span>
16. <span data-ttu-id="bb0bb-133">在“连续性物料”字段中，键入“88000”，然后按 Tab 键。</span><span class="sxs-lookup"><span data-stu-id="bb0bb-133">In the Continuity item field, type '88000' and then press the Tab key.</span></span>
17. <span data-ttu-id="bb0bb-134">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="bb0bb-134">Click OK.</span></span>
18. <span data-ttu-id="bb0bb-135">转至“零售和商业”>"连续性">“创建连续性子订单”。</span><span class="sxs-lookup"><span data-stu-id="bb0bb-135">Go to Retail and commerce > Continuity > Create continuity child orders.</span></span>
    * <span data-ttu-id="bb0bb-136">此流程将基于您的连续性计划的设置创建新销售订单。</span><span class="sxs-lookup"><span data-stu-id="bb0bb-136">This process will create new sales orders based on the settings of your continuity programs.</span></span>  
19. <span data-ttu-id="bb0bb-137">在“连续性物料”字段中，键入“88000”，然后按 Tab 键。</span><span class="sxs-lookup"><span data-stu-id="bb0bb-137">In the Continuity item field, type '88000' and then press the Tab key.</span></span>
    * <span data-ttu-id="bb0bb-138">物料“88000”是 USRT 演示数据中的一个连续性物料。</span><span class="sxs-lookup"><span data-stu-id="bb0bb-138">Item '88000' is a continuity item in the USRT demo data.</span></span>  
20. <span data-ttu-id="bb0bb-139">在“销售订单”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="bb0bb-139">In the Sales order field, enter or select a value.</span></span>
    * <span data-ttu-id="bb0bb-140">输入您在此过程中前面记下的销售订单编号。</span><span class="sxs-lookup"><span data-stu-id="bb0bb-140">Enter the sales order number that you noted earlier in the procedure.</span></span> <span data-ttu-id="bb0bb-141">这将让此过程的处理时间降到最低。</span><span class="sxs-lookup"><span data-stu-id="bb0bb-141">This will keep the processing time to a minimal for this procedure.</span></span> <span data-ttu-id="bb0bb-142">“销售订单”字段为可选字段，您可以处理任一计划的所有订单。</span><span class="sxs-lookup"><span data-stu-id="bb0bb-142">The Sales order field field is optional--you could process all orders for any one program.</span></span>  
21. <span data-ttu-id="bb0bb-143">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="bb0bb-143">Click OK.</span></span>

