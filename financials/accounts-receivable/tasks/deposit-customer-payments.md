--- 
title: "存放客户付款"
description: "存入客户付款。"
author: ShivamPandey-msft
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
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: dbf21bd5df70cd80e4fe3f2f5d699aa82b62423b
ms.contentlocale: zh-cn
ms.lasthandoff: 08/29/2017

---
# <a name="deposit-customer-payments"></a><span data-ttu-id="2b811-103">存放客户付款</span><span class="sxs-lookup"><span data-stu-id="2b811-103">Deposit customer payments</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2b811-104">存入客户付款。</span><span class="sxs-lookup"><span data-stu-id="2b811-104">Deposit customer payments.</span></span> <span data-ttu-id="2b811-105">本任务使用 USMF 公司进行演示。</span><span class="sxs-lookup"><span data-stu-id="2b811-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="2b811-106">转到“应收帐款”>“付款”>“付款日记帐”。</span><span class="sxs-lookup"><span data-stu-id="2b811-106">Go to Accounts receivable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="2b811-107">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="2b811-107">Click New.</span></span>
3. <span data-ttu-id="2b811-108">在“名称”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="2b811-108">In the Name field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="2b811-109">选择付款日记帐。</span><span class="sxs-lookup"><span data-stu-id="2b811-109">Select the payment journal.</span></span> 
5. <span data-ttu-id="2b811-110">单击“行”。</span><span class="sxs-lookup"><span data-stu-id="2b811-110">Click Lines.</span></span>
6. <span data-ttu-id="2b811-111">在“帐户”字段中，选择记录付款的“客户”。</span><span class="sxs-lookup"><span data-stu-id="2b811-111">In the Account field, select the Customer for whom you are recording the payment.</span></span>
7. <span data-ttu-id="2b811-112">在“信用”字段，输入付款金额。</span><span class="sxs-lookup"><span data-stu-id="2b811-112">In the Credit field, enter the amount of the payment.</span></span>
    * <span data-ttu-id="2b811-113">您可以选择不填金额，由系统通过选择已经支付的发票计算出金额。</span><span class="sxs-lookup"><span data-stu-id="2b811-113">You can choose to leave the amount blank, and have the system calculate it by selecting the invoices which were paid.</span></span>  
8. <span data-ttu-id="2b811-114">在“付款参考”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="2b811-114">In the Payment reference field, type a value.</span></span>
    * <span data-ttu-id="2b811-115">付款参考可以是您输入的付款的支票编号。</span><span class="sxs-lookup"><span data-stu-id="2b811-115">The payment reference could be the check number for the payment you are entering.</span></span> <span data-ttu-id="2b811-116">填写付款参考是为了在存款单上添加付款。</span><span class="sxs-lookup"><span data-stu-id="2b811-116">The payment reference is required in order to include the payment on a deposit slip.</span></span>  
9. <span data-ttu-id="2b811-117">标记“使用存款单”框。</span><span class="sxs-lookup"><span data-stu-id="2b811-117">Mark the box Use a deposit slip.</span></span>
    * <span data-ttu-id="2b811-118">如果付款应该包含在存款中，请将此设置更改为“是”。</span><span class="sxs-lookup"><span data-stu-id="2b811-118">If the payment should be included in the deposit, change this setting to Yes.</span></span>  
10. <span data-ttu-id="2b811-119">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="2b811-119">Click New.</span></span>
11. <span data-ttu-id="2b811-120">在“帐户”字段中，选择下一付款的“客户”。</span><span class="sxs-lookup"><span data-stu-id="2b811-120">In the Account field, select the Customer for the next payment.</span></span>
12. <span data-ttu-id="2b811-121">在“信用”字段，输入付款金额。</span><span class="sxs-lookup"><span data-stu-id="2b811-121">In the Credit field, enter the payment amount.</span></span>
13. <span data-ttu-id="2b811-122">在“付款参考”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="2b811-122">In the Payment reference field, type a value.</span></span>
14. <span data-ttu-id="2b811-123">标记“使用存款单”框。</span><span class="sxs-lookup"><span data-stu-id="2b811-123">Mark the box Use a deposit slip.</span></span>
15. <span data-ttu-id="2b811-124">单击“过帐”。</span><span class="sxs-lookup"><span data-stu-id="2b811-124">Click Post.</span></span>
    * <span data-ttu-id="2b811-125">需在存款单生成之前，对付款过帐。</span><span class="sxs-lookup"><span data-stu-id="2b811-125">Payments must be posted before the deposit slip can be generated.</span></span> <span data-ttu-id="2b811-126">这是为了确保在存款单生成后付款不会发生更改。</span><span class="sxs-lookup"><span data-stu-id="2b811-126">This is to ensure that the payments don't change after the deposit slip is generated.</span></span>  
16. <span data-ttu-id="2b811-127">单击“功能”。</span><span class="sxs-lookup"><span data-stu-id="2b811-127">Click Functions.</span></span>
17. <span data-ttu-id="2b811-128">单击“存款单”。</span><span class="sxs-lookup"><span data-stu-id="2b811-128">Click Deposit slip.</span></span>
18. <span data-ttu-id="2b811-129">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="2b811-129">Click OK.</span></span>
    * <span data-ttu-id="2b811-130">第一页用于创建存款单。</span><span class="sxs-lookup"><span data-stu-id="2b811-130">The first page is used to create the deposit slip.</span></span>  
19. <span data-ttu-id="2b811-131">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="2b811-131">Click OK.</span></span>
    * <span data-ttu-id="2b811-132">第二步为打印存款单，此步骤非必填项。</span><span class="sxs-lookup"><span data-stu-id="2b811-132">The second step is to print the deposit slip, but this step is not required.</span></span>  


