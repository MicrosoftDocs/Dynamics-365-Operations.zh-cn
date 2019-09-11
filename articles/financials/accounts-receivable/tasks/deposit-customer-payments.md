---
title: 存放客户付款
description: 存入客户付款。
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/18/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransCustPaym, CustTableLookup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 595d1b609ae83af8f1581caeff9ef7d3892a6207
ms.sourcegitcommit: a368682f9cf3897347d155f1a2d4b33e555cc2c4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/08/2019
ms.locfileid: "1867766"
---
# <a name="deposit-customer-payments"></a><span data-ttu-id="aa119-103">存放客户付款</span><span class="sxs-lookup"><span data-stu-id="aa119-103">Deposit customer payments</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="aa119-104">存入客户付款。</span><span class="sxs-lookup"><span data-stu-id="aa119-104">Deposit customer payments.</span></span> <span data-ttu-id="aa119-105">此任务使用 USMF 公司演示。</span><span class="sxs-lookup"><span data-stu-id="aa119-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="aa119-106">转到**导航窗格 > 模块 > 应收帐款 > 付款 > 付款日记帐**。</span><span class="sxs-lookup"><span data-stu-id="aa119-106">Go to **Navigation pane > Modules > Accounts receivable > Payments > Payment journal**.</span></span>
2. <span data-ttu-id="aa119-107">选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="aa119-107">Select **New**.</span></span>
3. <span data-ttu-id="aa119-108">在**名称**字段中，选择下拉菜单中的 **CustPay**。</span><span class="sxs-lookup"><span data-stu-id="aa119-108">In the **Name** field, select **CustPay** in the drop-down menu.</span></span>
4. <span data-ttu-id="aa119-109">选择**行**。</span><span class="sxs-lookup"><span data-stu-id="aa119-109">Select **Lines**.</span></span>
5. <span data-ttu-id="aa119-110">在**帐户**字段中，选择记录付款的客户。</span><span class="sxs-lookup"><span data-stu-id="aa119-110">In the **Account** field, select the customer for whom you are recording the payment.</span></span>
6. <span data-ttu-id="aa119-111">在**信用**字段，输入付款金额。</span><span class="sxs-lookup"><span data-stu-id="aa119-111">In the **Credit** field, enter the amount of the payment.</span></span> <span data-ttu-id="aa119-112">您可以选择不填金额，由系统通过选择已经支付的发票计算出金额。</span><span class="sxs-lookup"><span data-stu-id="aa119-112">You can choose to leave the amount blank, and have the system calculate it by selecting the invoices which were paid.</span></span>  
7. <span data-ttu-id="aa119-113">在**付款参考**字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="aa119-113">In the **Payment reference** field, type a value.</span></span> <span data-ttu-id="aa119-114">付款参考可以是您输入的付款的支票编号。</span><span class="sxs-lookup"><span data-stu-id="aa119-114">The payment reference could be the check number for the payment you are entering.</span></span> <span data-ttu-id="aa119-115">填写付款参考是为了在存款单上添加付款。</span><span class="sxs-lookup"><span data-stu-id="aa119-115">The payment reference is required in order to include the payment on a deposit slip.</span></span>  
8. <span data-ttu-id="aa119-116">标记“使用存款单”框。</span><span class="sxs-lookup"><span data-stu-id="aa119-116">Mark the box Use a deposit slip.</span></span> <span data-ttu-id="aa119-117">如果付款应该包含在存款中，请将此设置更改为“是”。</span><span class="sxs-lookup"><span data-stu-id="aa119-117">If the payment should be included in the deposit, change this setting to Yes.</span></span>  
9. <span data-ttu-id="aa119-118">选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="aa119-118">Select **New**.</span></span>
10. <span data-ttu-id="aa119-119">在**帐户**字段中，选择下一付款的客户。</span><span class="sxs-lookup"><span data-stu-id="aa119-119">In the **Account** field, select the customer for the next payment.</span></span>
11. <span data-ttu-id="aa119-120">在**信用**字段，输入付款金额。</span><span class="sxs-lookup"><span data-stu-id="aa119-120">In the **Credit** field, enter the payment amount.</span></span>
12. <span data-ttu-id="aa119-121">在**付款参考**字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="aa119-121">In the **Payment reference** field, type a value.</span></span>
13. <span data-ttu-id="aa119-122">标记**使用存款单**框。</span><span class="sxs-lookup"><span data-stu-id="aa119-122">Mark the box **Use a deposit slip**.</span></span>
14. <span data-ttu-id="aa119-123">选择**过帐**。</span><span class="sxs-lookup"><span data-stu-id="aa119-123">Select **Post**.</span></span> <span data-ttu-id="aa119-124">需在存款单生成之前，对付款过帐。</span><span class="sxs-lookup"><span data-stu-id="aa119-124">Payments must be posted before the deposit slip can be generated.</span></span> <span data-ttu-id="aa119-125">这是为了确保在存款单生成后付款不会发生更改。</span><span class="sxs-lookup"><span data-stu-id="aa119-125">This is to ensure that the payments don't change after the deposit slip is generated.</span></span>  
15. <span data-ttu-id="aa119-126">选择**功能**。</span><span class="sxs-lookup"><span data-stu-id="aa119-126">Select **Functions**.</span></span>
16. <span data-ttu-id="aa119-127">选择**存款单**。</span><span class="sxs-lookup"><span data-stu-id="aa119-127">Select **Deposit slip**.</span></span>
17. <span data-ttu-id="aa119-128">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="aa119-128">Select **OK**.</span></span> <span data-ttu-id="aa119-129">第一页用于创建存款单。</span><span class="sxs-lookup"><span data-stu-id="aa119-129">The first page is used to create the deposit slip.</span></span>  
18. <span data-ttu-id="aa119-130">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="aa119-130">Select **OK**.</span></span> <span data-ttu-id="aa119-131">第二步为打印存款单，此步骤非必填项。</span><span class="sxs-lookup"><span data-stu-id="aa119-131">The second step is to print the deposit slip, but this step is not required.</span></span>  

