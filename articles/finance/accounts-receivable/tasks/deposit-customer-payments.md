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
ms.openlocfilehash: 1d903f557fbaeb720dd4a34dc1c772be0dcb56eb
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4440747"
---
# <a name="deposit-customer-payments"></a><span data-ttu-id="4e3fb-103">存放客户付款</span><span class="sxs-lookup"><span data-stu-id="4e3fb-103">Deposit customer payments</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4e3fb-104">存入客户付款。</span><span class="sxs-lookup"><span data-stu-id="4e3fb-104">Deposit customer payments.</span></span> <span data-ttu-id="4e3fb-105">此任务使用 USMF 公司演示。</span><span class="sxs-lookup"><span data-stu-id="4e3fb-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="4e3fb-106">转到 **导航窗格 > 模块 > 应收帐款 > 付款 > 付款日记帐**。</span><span class="sxs-lookup"><span data-stu-id="4e3fb-106">Go to **Navigation pane > Modules > Accounts receivable > Payments > Payment journal**.</span></span>
2. <span data-ttu-id="4e3fb-107">选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="4e3fb-107">Select **New**.</span></span>
3. <span data-ttu-id="4e3fb-108">在 **名称** 字段中，选择下拉菜单中的 **CustPay**。</span><span class="sxs-lookup"><span data-stu-id="4e3fb-108">In the **Name** field, select **CustPay** in the drop-down menu.</span></span>
4. <span data-ttu-id="4e3fb-109">选择 **行**。</span><span class="sxs-lookup"><span data-stu-id="4e3fb-109">Select **Lines**.</span></span>
5. <span data-ttu-id="4e3fb-110">在 **帐户** 字段中，选择记录付款的客户。</span><span class="sxs-lookup"><span data-stu-id="4e3fb-110">In the **Account** field, select the customer for whom you are recording the payment.</span></span>
6. <span data-ttu-id="4e3fb-111">在 **信用** 字段，输入付款金额。</span><span class="sxs-lookup"><span data-stu-id="4e3fb-111">In the **Credit** field, enter the amount of the payment.</span></span> <span data-ttu-id="4e3fb-112">您可以选择不填金额，由系统通过选择已经支付的发票计算出金额。</span><span class="sxs-lookup"><span data-stu-id="4e3fb-112">You can choose to leave the amount blank, and have the system calculate it by selecting the invoices which were paid.</span></span>  
7. <span data-ttu-id="4e3fb-113">在 **付款参考** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="4e3fb-113">In the **Payment reference** field, type a value.</span></span> <span data-ttu-id="4e3fb-114">付款参考可以是您输入的付款的支票编号。</span><span class="sxs-lookup"><span data-stu-id="4e3fb-114">The payment reference could be the check number for the payment you are entering.</span></span> <span data-ttu-id="4e3fb-115">填写付款参考是为了在存款单上添加付款。</span><span class="sxs-lookup"><span data-stu-id="4e3fb-115">The payment reference is required in order to include the payment on a deposit slip.</span></span>  
8. <span data-ttu-id="4e3fb-116">标记“使用存款单”框。</span><span class="sxs-lookup"><span data-stu-id="4e3fb-116">Mark the box Use a deposit slip.</span></span> <span data-ttu-id="4e3fb-117">如果付款应该包含在存款中，请将此设置更改为“是”。</span><span class="sxs-lookup"><span data-stu-id="4e3fb-117">If the payment should be included in the deposit, change this setting to Yes.</span></span>  
9. <span data-ttu-id="4e3fb-118">选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="4e3fb-118">Select **New**.</span></span>
10. <span data-ttu-id="4e3fb-119">在 **帐户** 字段中，选择下一付款的客户。</span><span class="sxs-lookup"><span data-stu-id="4e3fb-119">In the **Account** field, select the customer for the next payment.</span></span>
11. <span data-ttu-id="4e3fb-120">在 **信用** 字段，输入付款金额。</span><span class="sxs-lookup"><span data-stu-id="4e3fb-120">In the **Credit** field, enter the payment amount.</span></span>
12. <span data-ttu-id="4e3fb-121">在 **付款参考** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="4e3fb-121">In the **Payment reference** field, type a value.</span></span>
13. <span data-ttu-id="4e3fb-122">标记 **使用存款单** 框。</span><span class="sxs-lookup"><span data-stu-id="4e3fb-122">Mark the box **Use a deposit slip**.</span></span>
14. <span data-ttu-id="4e3fb-123">选择 **过帐**。</span><span class="sxs-lookup"><span data-stu-id="4e3fb-123">Select **Post**.</span></span> <span data-ttu-id="4e3fb-124">需在存款单生成之前，对付款过帐。</span><span class="sxs-lookup"><span data-stu-id="4e3fb-124">Payments must be posted before the deposit slip can be generated.</span></span> <span data-ttu-id="4e3fb-125">这是为了确保在存款单生成后付款不会发生更改。</span><span class="sxs-lookup"><span data-stu-id="4e3fb-125">This is to ensure that the payments don't change after the deposit slip is generated.</span></span>  
15. <span data-ttu-id="4e3fb-126">选择 **功能**。</span><span class="sxs-lookup"><span data-stu-id="4e3fb-126">Select **Functions**.</span></span>
16. <span data-ttu-id="4e3fb-127">选择 **存款单**。</span><span class="sxs-lookup"><span data-stu-id="4e3fb-127">Select **Deposit slip**.</span></span>
17. <span data-ttu-id="4e3fb-128">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="4e3fb-128">Select **OK**.</span></span> <span data-ttu-id="4e3fb-129">第一页用于创建存款单。</span><span class="sxs-lookup"><span data-stu-id="4e3fb-129">The first page is used to create the deposit slip.</span></span>  
18. <span data-ttu-id="4e3fb-130">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="4e3fb-130">Select **OK**.</span></span> <span data-ttu-id="4e3fb-131">第二步为打印存款单，此步骤非必填项。</span><span class="sxs-lookup"><span data-stu-id="4e3fb-131">The second step is to print the deposit slip, but this step is not required.</span></span>  

