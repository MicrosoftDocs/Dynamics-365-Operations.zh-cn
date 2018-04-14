--- 
title: "创建普通发票"
description: "此任务指南演示如何创建普通发票。"
author: mikefalkner
manager: AnnBe
ms.date: 10/26/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: ca7c0f46f0cab298580e37c236bd10e4325e011b
ms.contentlocale: zh-cn
ms.lasthandoff: 04/13/2018

---
# <a name="create-a-free-text-invoice"></a><span data-ttu-id="2aaae-103">创建普通发票</span><span class="sxs-lookup"><span data-stu-id="2aaae-103">Create a free text invoice</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2aaae-104">此任务指南演示如何创建普通发票。</span><span class="sxs-lookup"><span data-stu-id="2aaae-104">This task guide demonstrates creating a free text invoice.</span></span> <span data-ttu-id="2aaae-105">本任务使用 USMF 公司进行演示。</span><span class="sxs-lookup"><span data-stu-id="2aaae-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="2aaae-106">转到“应收账款”>“发票”>“所有普通发票”。</span><span class="sxs-lookup"><span data-stu-id="2aaae-106">Go to Accounts receivable > Invoices > All free text invoices.</span></span>
2. <span data-ttu-id="2aaae-107">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="2aaae-107">Click New.</span></span>
3. <span data-ttu-id="2aaae-108">在“客户帐户”字段中，选择一个值。</span><span class="sxs-lookup"><span data-stu-id="2aaae-108">In the Customer account field, select a value.</span></span>
    * <span data-ttu-id="2aaae-109">发票帐户将默认为用于客户帐户的同一帐户。</span><span class="sxs-lookup"><span data-stu-id="2aaae-109">The invoice account will default to the same account used for the customer account.</span></span>   
    * <span data-ttu-id="2aaae-110">如果发票未过帐，会计状态最开始为“进行中”。</span><span class="sxs-lookup"><span data-stu-id="2aaae-110">The accounting status starts with In process if the invoice is not posted.</span></span>   
    * <span data-ttu-id="2aaae-111">发票过帐后，将分配发票编号。</span><span class="sxs-lookup"><span data-stu-id="2aaae-111">The invoice number will be assigned when the invoice is posted.</span></span>  
    * <span data-ttu-id="2aaae-112">如果您使用 SEPA 授权，当您选择客户帐户时，直接借记授权将自动填充授权。</span><span class="sxs-lookup"><span data-stu-id="2aaae-112">If you are using SEPA mandates, the direct debit mandate will be automatically populated with a mandate when you select the customer account.</span></span>  
4. <span data-ttu-id="2aaae-113">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="2aaae-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="2aaae-114">在“主科目”字段中，指定没有维度的帐号。</span><span class="sxs-lookup"><span data-stu-id="2aaae-114">In the Main account field, specify an account number without dimensions.</span></span>
    * <span data-ttu-id="2aaae-115">您还可以为主科目输入一个或多个字符，并使用查找功能查找科目。</span><span class="sxs-lookup"><span data-stu-id="2aaae-115">You can also enter one or more characters for the main account and use the lookup to find your account.</span></span> <span data-ttu-id="2aaae-116">您稍后将在此指南输入维度。</span><span class="sxs-lookup"><span data-stu-id="2aaae-116">You will enter dimensions later on in this guide.</span></span>  
6. <span data-ttu-id="2aaae-117">展开“行明细”快速选项卡，以便您可以将维度添加到主科目。</span><span class="sxs-lookup"><span data-stu-id="2aaae-117">Expand the Line details fasttab so you can add dimensions to your main account.</span></span>
7. <span data-ttu-id="2aaae-118">单击“财务维度行”选项卡。</span><span class="sxs-lookup"><span data-stu-id="2aaae-118">Click the Financial dimensions line tab.</span></span>
    * <span data-ttu-id="2aaae-119">这些维度仅适用于所选行。</span><span class="sxs-lookup"><span data-stu-id="2aaae-119">The dimensions are for the selected line only.</span></span>    
    * <span data-ttu-id="2aaae-120">销售税组将从客户处填充信息。</span><span class="sxs-lookup"><span data-stu-id="2aaae-120">The sales tax group is populated from the customer.</span></span> <span data-ttu-id="2aaae-121">如果客户没有销售税组，则使用主科目的销售税组信息。</span><span class="sxs-lookup"><span data-stu-id="2aaae-121">If the customer does not have a sales tax group, the sales tax group from the main account is used.</span></span>  
    * <span data-ttu-id="2aaae-122">物料销售税组根据主科目填充。</span><span class="sxs-lookup"><span data-stu-id="2aaae-122">The items sales tax group is populated from the main account.</span></span> <span data-ttu-id="2aaae-123">如果主科目没有物料销售税组，则使用“总帐中销售税参数”中的物料销售税组。</span><span class="sxs-lookup"><span data-stu-id="2aaae-123">If the main account does not have an item sales tax group, then the item sales tax group in the General ledger sales tax parameters is used.</span></span>    
8. <span data-ttu-id="2aaae-124">在“数量”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="2aaae-124">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="2aaae-125">数量为可选项。</span><span class="sxs-lookup"><span data-stu-id="2aaae-125">The quantity is optional.</span></span>  
9. <span data-ttu-id="2aaae-126">在“单位价格”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="2aaae-126">In the Unit price field, enter a number.</span></span>
    * <span data-ttu-id="2aaae-127">单位价格为可选项。</span><span class="sxs-lookup"><span data-stu-id="2aaae-127">The unit price is optional.</span></span>  
    * <span data-ttu-id="2aaae-128">此金额计算为数量乘以单位价格。</span><span class="sxs-lookup"><span data-stu-id="2aaae-128">The amount is calculated as the quantity times the unit price.</span></span> <span data-ttu-id="2aaae-129">不过，您可以覆盖计算值，另外输入一个金额。</span><span class="sxs-lookup"><span data-stu-id="2aaae-129">However, you can override that calculation and enter an amount.</span></span>  
10. <span data-ttu-id="2aaae-130">单击“销售税”查看为您的发票计算的销售税。</span><span class="sxs-lookup"><span data-stu-id="2aaae-130">Click on Sales tax to view the sales tax calculated for your invoice.</span></span>
    * <span data-ttu-id="2aaae-131">在此页查看销售税金额，您也可以在“调整”选项卡上覆盖这些金额。</span><span class="sxs-lookup"><span data-stu-id="2aaae-131">View the sales tax amounts in this page or you can override the amounts on the Adjustment tab.</span></span>  
11. <span data-ttu-id="2aaae-132">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="2aaae-132">Click OK.</span></span>
12. <span data-ttu-id="2aaae-133">单击“费用”，以添加费用到您的发票中。</span><span class="sxs-lookup"><span data-stu-id="2aaae-133">Click Charges to add a charge to your invoice.</span></span> 
13. <span data-ttu-id="2aaae-134">在“费用代码”字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="2aaae-134">In the Charges code field, type a value.</span></span>
14. <span data-ttu-id="2aaae-135">在“费用数值”字段中，输入一个数目。</span><span class="sxs-lookup"><span data-stu-id="2aaae-135">In the Charges value field, enter a number.</span></span>
15. <span data-ttu-id="2aaae-136">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="2aaae-136">Close the page.</span></span>
16. <span data-ttu-id="2aaae-137">单击“总计”查看汇总的发票详细信息和总计。</span><span class="sxs-lookup"><span data-stu-id="2aaae-137">Click Totals to view the summary invoice details and totals.</span></span>
17. <span data-ttu-id="2aaae-138">单击“关闭”。</span><span class="sxs-lookup"><span data-stu-id="2aaae-138">Click Close.</span></span>
18. <span data-ttu-id="2aaae-139">单击“过帐”过帐该发票。</span><span class="sxs-lookup"><span data-stu-id="2aaae-139">Click Post to post the invoice.</span></span> <span data-ttu-id="2aaae-140">在过帐前，您可以取消。</span><span class="sxs-lookup"><span data-stu-id="2aaae-140">You will be able to cancel before you post.</span></span>
    * <span data-ttu-id="2aaae-141">更改发票打印时的时间：选择“当前”（各发票更新后即打印），或选择“之后”（在更新所有发票后打印）。</span><span class="sxs-lookup"><span data-stu-id="2aaae-141">To change the timing of your invoice printing:  Select Current to print each invoice as it is updated   or  Select After to print after all invoices have been updated.</span></span>  
    * <span data-ttu-id="2aaae-142">如果要更改过帐前客户信用额度的检查方式，则更改“信用额度”类型。</span><span class="sxs-lookup"><span data-stu-id="2aaae-142">If you want to change how the customer's credit limit is checked before posting, change the Credit limit type.</span></span>  
    * <span data-ttu-id="2aaae-143">如果您要打印发票，则选择“是”。</span><span class="sxs-lookup"><span data-stu-id="2aaae-143">If you want to print the invoice, select Yes.</span></span>  
    * <span data-ttu-id="2aaae-144">如果您要将发票过帐，则选择“是”。</span><span class="sxs-lookup"><span data-stu-id="2aaae-144">If you want to post the invoice, select Yes.</span></span> <span data-ttu-id="2aaae-145">您可以打印未过帐发票。</span><span class="sxs-lookup"><span data-stu-id="2aaae-145">You can print the invoice without posting.</span></span>  
19. <span data-ttu-id="2aaae-146">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="2aaae-146">Click OK.</span></span>


