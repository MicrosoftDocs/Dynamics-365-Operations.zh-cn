--- 
title: "创建客户的勾销日记帐"
description: "此任务指南将为您展示在“收款”页、“未结客户发票”页和“客户”页如何设置勾销和勾销交易参数。"
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
ms.openlocfilehash: 19a816f04283ce4f200de7396617313e45e057db
ms.contentlocale: zh-cn
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-write-off-journal-for-a-customer"></a><span data-ttu-id="d945d-103">创建客户的勾销日记帐</span><span class="sxs-lookup"><span data-stu-id="d945d-103">Create a write-off journal for a customer</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d945d-104">此任务指南将为您展示在“收款”页、“未结客户发票”页和“客户”页如何设置勾销和勾销交易参数。</span><span class="sxs-lookup"><span data-stu-id="d945d-104">This task guide will show you how to set up the parameters for write-offs and then write off transactions from the Collections page, the Open customer invoices page, and the Customer page.</span></span> <span data-ttu-id="d945d-105">本任务使用 USMF 公司进行演示。</span><span class="sxs-lookup"><span data-stu-id="d945d-105">This task uses the USMF demo company.</span></span>


## <a name="set-up-the-write-off-parameters"></a><span data-ttu-id="d945d-106">设置勾销参数</span><span class="sxs-lookup"><span data-stu-id="d945d-106">Set up the write off parameters</span></span>
1. <span data-ttu-id="d945d-107">转至“信用和收款”>“设置”>“应收帐款参数”。</span><span class="sxs-lookup"><span data-stu-id="d945d-107">Go to Credit and collections > Setup > Accounts receivable parameters.</span></span>
2. <span data-ttu-id="d945d-108">单击“收款”选项卡。</span><span class="sxs-lookup"><span data-stu-id="d945d-108">Click the Collections tab.</span></span>
3. <span data-ttu-id="d945d-109">展开或折叠“勾销”部分。</span><span class="sxs-lookup"><span data-stu-id="d945d-109">Expand or collapse the Write-off section.</span></span>
    * <span data-ttu-id="d945d-110">此“勾销日记帐”是普通日记帐，它将持续勾销您创建的交易记录。</span><span class="sxs-lookup"><span data-stu-id="d945d-110">The Write-off journal is the general journal that will hold the write-off transactions that you create.</span></span>  
    * <span data-ttu-id="d945d-111">您可以为每次勾销附上一个原因代码。</span><span class="sxs-lookup"><span data-stu-id="d945d-111">You can attach a reason code to every write-off.</span></span> <span data-ttu-id="d945d-112">您可以在勾销时改写此默认值。</span><span class="sxs-lookup"><span data-stu-id="d945d-112">You can override this default at the time of the write-off.</span></span>  
    * <span data-ttu-id="d945d-113">如果你想在勾销的原始交易记录中分离销售税，请将其设置为“是”。</span><span class="sxs-lookup"><span data-stu-id="d945d-113">Set this to Yes if you want to separate the sales tax from the original transaction in the write-off.</span></span>  
4. <span data-ttu-id="d945d-114">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="d945d-114">Close the page.</span></span>
5. <span data-ttu-id="d945d-115">转到“信用征收”>“设置”>“客户过帐模板”。</span><span class="sxs-lookup"><span data-stu-id="d945d-115">Go to Credit and collections > Setup > Customer posting profiles.</span></span>
    * <span data-ttu-id="d945d-116">勾销帐户将用于普通日记帐的支出帐户或预留调整</span><span class="sxs-lookup"><span data-stu-id="d945d-116">The write-off account will be used as the expense account or reserve adjustment in the general journal</span></span>   
6. <span data-ttu-id="d945d-117">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="d945d-117">Close the page.</span></span>

## <a name="write-off-a-customer-balance-from-the-aged-balances-page"></a><span data-ttu-id="d945d-118">从帐龄余额页上勾销客户余额</span><span class="sxs-lookup"><span data-stu-id="d945d-118">Write off a customer balance from the aged balances page</span></span>
1. <span data-ttu-id="d945d-119">转到“贷记和收款”>“收款”>“帐龄余额”。</span><span class="sxs-lookup"><span data-stu-id="d945d-119">Go to Credit and collections > Collections > Aged balances.</span></span>
2. <span data-ttu-id="d945d-120">标记您要勾销客户所在的行。</span><span class="sxs-lookup"><span data-stu-id="d945d-120">Mark the row for the customer that you want to write off.</span></span> <span data-ttu-id="d945d-121">例如，标记 Birch 公司所在的行。</span><span class="sxs-lookup"><span data-stu-id="d945d-121">For example, mark the line with Birch Company on it.</span></span>
3. <span data-ttu-id="d945d-122">在“操作窗格”上，单击“收款”。</span><span class="sxs-lookup"><span data-stu-id="d945d-122">On the Action Pane, click Collect.</span></span>
4. <span data-ttu-id="d945d-123">单击“勾销”。</span><span class="sxs-lookup"><span data-stu-id="d945d-123">Click Write off.</span></span>
5. <span data-ttu-id="d945d-124">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="d945d-124">Click OK.</span></span>
6. <span data-ttu-id="d945d-125">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="d945d-125">Close the page.</span></span>
7. <span data-ttu-id="d945d-126">转到“总帐”>“日记帐条目”>“普通日记帐”。</span><span class="sxs-lookup"><span data-stu-id="d945d-126">Go to General ledger > Journal entries > General journals.</span></span>
8. <span data-ttu-id="d945d-127">选择包含您勾销条目的日记帐批号。</span><span class="sxs-lookup"><span data-stu-id="d945d-127">Select the journal batch number for the journal that contains your write-off.</span></span>
    * <span data-ttu-id="d945d-128">创建单行以预留客户余额。</span><span class="sxs-lookup"><span data-stu-id="d945d-128">One line is created to reverse the customer balance.</span></span> <span data-ttu-id="d945d-129">创建单行或多行以过帐勾销至勾销帐户。</span><span class="sxs-lookup"><span data-stu-id="d945d-129">One or more lines are created to post the write-off to the write-off account.</span></span>  
9. <span data-ttu-id="d945d-130">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="d945d-130">Close the page.</span></span>
10. <span data-ttu-id="d945d-131">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="d945d-131">Close the page.</span></span>

## <a name="write-off-transactions-from-the-collections-form"></a><span data-ttu-id="d945d-132">从收款窗体勾销交易。</span><span class="sxs-lookup"><span data-stu-id="d945d-132">Write off transactions from the collections form.</span></span>
1. <span data-ttu-id="d945d-133">转到“贷记和收款”>“收款”>“帐龄余额”。</span><span class="sxs-lookup"><span data-stu-id="d945d-133">Go to Credit and collections > Collections > Aged balances.</span></span>
2. <span data-ttu-id="d945d-134">选择您要勾销交易记录的客户的名称。</span><span class="sxs-lookup"><span data-stu-id="d945d-134">Select the name of the customer that has the transactions that you want to write off.</span></span> <span data-ttu-id="d945d-135">例如，选择 Cave Wholesales (US-004)。</span><span class="sxs-lookup"><span data-stu-id="d945d-135">For example, select Cave Wholesales (US-004).</span></span>
3. <span data-ttu-id="d945d-136">标记第一个交易行。</span><span class="sxs-lookup"><span data-stu-id="d945d-136">Mark the row for the first transaction.</span></span>
4. <span data-ttu-id="d945d-137">标记第二个交易行。</span><span class="sxs-lookup"><span data-stu-id="d945d-137">Mark the row for the second transaction.</span></span>
5. <span data-ttu-id="d945d-138">单击“勾销”。</span><span class="sxs-lookup"><span data-stu-id="d945d-138">Click Write off.</span></span>
6. <span data-ttu-id="d945d-139">在“原因注释”字段中，键入“坏帐”。</span><span class="sxs-lookup"><span data-stu-id="d945d-139">In the Reason comment field, type 'Bad debts'.</span></span>
7. <span data-ttu-id="d945d-140">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="d945d-140">Click OK.</span></span>
8. <span data-ttu-id="d945d-141">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="d945d-141">Close the page.</span></span>
9. <span data-ttu-id="d945d-142">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="d945d-142">Close the page.</span></span>
10. <span data-ttu-id="d945d-143">转到“总帐”>“日记帐条目”>“普通日记帐”。</span><span class="sxs-lookup"><span data-stu-id="d945d-143">Go to General ledger > Journal entries > General journals.</span></span>
11. <span data-ttu-id="d945d-144">选择包含您勾销条目的日记帐批号。</span><span class="sxs-lookup"><span data-stu-id="d945d-144">Select the journal batch number for the journal that contains your write-off.</span></span>
    * <span data-ttu-id="d945d-145">创建单行以预留客户余额。</span><span class="sxs-lookup"><span data-stu-id="d945d-145">One line is created to reverse the customer balance.</span></span> <span data-ttu-id="d945d-146">创建单行或多行以过帐勾销至勾销帐户。</span><span class="sxs-lookup"><span data-stu-id="d945d-146">One or more lines are created to post the write-off to the write-off account.</span></span>  
12. <span data-ttu-id="d945d-147">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="d945d-147">Close the page.</span></span>
13. <span data-ttu-id="d945d-148">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="d945d-148">Close the page.</span></span>

## <a name="write-off-an-invoice-from-the-open-customers-invoices-page"></a><span data-ttu-id="d945d-149">从“未结客户发票”页勾销发票</span><span class="sxs-lookup"><span data-stu-id="d945d-149">Write off an invoice from the Open customers invoices page</span></span>
1. <span data-ttu-id="d945d-150">转至“应收帐款”>“发票”>“未结客户发票”。</span><span class="sxs-lookup"><span data-stu-id="d945d-150">Go to Accounts receivable > Invoices > Open customer invoices.</span></span>
2. <span data-ttu-id="d945d-151">标记发票行。</span><span class="sxs-lookup"><span data-stu-id="d945d-151">Mark the line for an invoice.</span></span> <span data-ttu-id="d945d-152">例如，标记 CIV-000667 所在行。</span><span class="sxs-lookup"><span data-stu-id="d945d-152">For example, mark the line for CIV-000667.</span></span>
3. <span data-ttu-id="d945d-153">在操作窗格上，单击“发票”。</span><span class="sxs-lookup"><span data-stu-id="d945d-153">On the Action Pane, click Invoice.</span></span>
4. <span data-ttu-id="d945d-154">单击“勾销”。</span><span class="sxs-lookup"><span data-stu-id="d945d-154">Click Write off.</span></span>
5. <span data-ttu-id="d945d-155">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="d945d-155">Click OK.</span></span>
6. <span data-ttu-id="d945d-156">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="d945d-156">Close the page.</span></span>

## <a name="write-off-a-customer-balance-from-the-customer-page"></a><span data-ttu-id="d945d-157">从“客户”页勾销客户余额</span><span class="sxs-lookup"><span data-stu-id="d945d-157">Write off a customer balance from the customer page</span></span>
1. <span data-ttu-id="d945d-158">转到“应付帐款”>“客户”>“所有客户”。</span><span class="sxs-lookup"><span data-stu-id="d945d-158">Go to Accounts receivable > Customers > All customers.</span></span>
2. <span data-ttu-id="d945d-159">选择客户帐户。</span><span class="sxs-lookup"><span data-stu-id="d945d-159">Select a customer account.</span></span> <span data-ttu-id="d945d-160">例如，选择 US-001 (Contoso Retail San Diego)。</span><span class="sxs-lookup"><span data-stu-id="d945d-160">For example, select US-001 (Contoso Retail San Diego).</span></span>
3. <span data-ttu-id="d945d-161">在“操作窗格”上，单击“收款”。</span><span class="sxs-lookup"><span data-stu-id="d945d-161">On the Action Pane, click Collect.</span></span>
4. <span data-ttu-id="d945d-162">单击“勾销”。</span><span class="sxs-lookup"><span data-stu-id="d945d-162">Click Write off.</span></span>
5. <span data-ttu-id="d945d-163">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="d945d-163">Click OK.</span></span>
6. <span data-ttu-id="d945d-164">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="d945d-164">Close the page.</span></span>

