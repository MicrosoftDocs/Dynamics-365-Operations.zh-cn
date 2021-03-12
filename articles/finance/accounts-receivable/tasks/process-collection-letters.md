---
title: 处理催款单
description: 该主题说明如何创建、打印并过帐收款单。
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPosting, CustCollectionLetterNote
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2018-12-01
ms.dyn365.ops.version: 8.1.3
ms.openlocfilehash: a189bbdd360d07b2b5198fa357380fd9a89ac167
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4992956"
---
# <a name="process-collection-letters"></a><span data-ttu-id="fb7c8-103">处理催款单</span><span class="sxs-lookup"><span data-stu-id="fb7c8-103">Process collection letters</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="fb7c8-104">该主题说明如何创建、打印并过帐收款单。</span><span class="sxs-lookup"><span data-stu-id="fb7c8-104">This topic shows how to create, print, and post collection letters.</span></span> <span data-ttu-id="fb7c8-105">此任务使用 USMF 公司演示。</span><span class="sxs-lookup"><span data-stu-id="fb7c8-105">This task uses the USMF demo company.</span></span>

## <a name="set-up-a-collection-letter-sequence-on-the-posting-profile"></a><span data-ttu-id="fb7c8-106">在该过帐上设置收款单的排序</span><span class="sxs-lookup"><span data-stu-id="fb7c8-106">Set up a collection letter sequence on the posting profile</span></span>
1. <span data-ttu-id="fb7c8-107">转到 **导航窗格 > 模块 > 信用和收款 > 设置 > 客户过帐模板**。</span><span class="sxs-lookup"><span data-stu-id="fb7c8-107">Go to **Navigation pane > Modules > Credit and collections > Setup > Customer posting profiles**.</span></span>
2. <span data-ttu-id="fb7c8-108">单击 **编辑**。</span><span class="sxs-lookup"><span data-stu-id="fb7c8-108">Click **Edit**.</span></span>
3. <span data-ttu-id="fb7c8-109">从下拉列表中选择收款单排序。</span><span class="sxs-lookup"><span data-stu-id="fb7c8-109">Select a collection letter sequence from the drop-down list.</span></span> <span data-ttu-id="fb7c8-110">如果不希望使用该过帐模板生成交易收款单，则该字段保留空白。</span><span class="sxs-lookup"><span data-stu-id="fb7c8-110">If you do not want to generate collection letters for transactions using this posting profile, leave the field blank.</span></span>  
4. <span data-ttu-id="fb7c8-111">展开 **表限制** 选项卡可以更改处理收款单的方式。</span><span class="sxs-lookup"><span data-stu-id="fb7c8-111">Expand the **Table restrictions** tab to change the way that collection letters are processed.</span></span> <span data-ttu-id="fb7c8-112">如果此字段设置为 **是**，则将在此过帐模板创建收款单。</span><span class="sxs-lookup"><span data-stu-id="fb7c8-112">If this field is set to **Yes**, then collection letters will be created for this posting profile.</span></span>  

## <a name="create-collection-letters"></a><span data-ttu-id="fb7c8-113">创建催款单</span><span class="sxs-lookup"><span data-stu-id="fb7c8-113">Create collection letters</span></span>
1. <span data-ttu-id="fb7c8-114">转到 **导航窗格 > 模块 > 信用与收款 > 收款单 > 创建收款单**。</span><span class="sxs-lookup"><span data-stu-id="fb7c8-114">Go to **Navigation pane > Modules > Credit and collections > Collection letter > Create collection letters**.</span></span>
2. <span data-ttu-id="fb7c8-115">选择收款单的交易类型。</span><span class="sxs-lookup"><span data-stu-id="fb7c8-115">Select the transaction types for which you will collect letters.</span></span> <span data-ttu-id="fb7c8-116">此计算包含这些类型的所有开放交易。</span><span class="sxs-lookup"><span data-stu-id="fb7c8-116">All of the open transactions for these types will be included in the calculation.</span></span>  
3. <span data-ttu-id="fb7c8-117">在 **催款单** 字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="fb7c8-117">In the **Collection letter** field, select an option.</span></span>
4. <span data-ttu-id="fb7c8-118">在 **催款单日期** 字段中，输入催款单的日期。</span><span class="sxs-lookup"><span data-stu-id="fb7c8-118">In the **Collection letter date** field, enter the date of the collection letter.</span></span>
5. <span data-ttu-id="fb7c8-119">如果将 **使用过帐模板** 更改为 **选择**，则请选择一个过帐模板。</span><span class="sxs-lookup"><span data-stu-id="fb7c8-119">Select a posting profile if you changed **Use posting profile from** to **Select**.</span></span> <span data-ttu-id="fb7c8-120">具有两个过帐模板选项：</span><span class="sxs-lookup"><span data-stu-id="fb7c8-120">There are two posting profile options:</span></span>   

   - <span data-ttu-id="fb7c8-121">**帐户** – 使用分配给每个利息单的客户帐户的过帐模板。</span><span class="sxs-lookup"><span data-stu-id="fb7c8-121">**Account** – Use the posting profile that is assigned to the customer account for each interest note.</span></span>   
   - <span data-ttu-id="fb7c8-122">**选择** – 使用在 **过帐模板** 字段中选择的过帐模板。</span><span class="sxs-lookup"><span data-stu-id="fb7c8-122">**Select** – Use the posting profile that you select in the **Posting profile** field.</span></span>  

6. <span data-ttu-id="fb7c8-123">扩展 **要包括的记录** 部分。</span><span class="sxs-lookup"><span data-stu-id="fb7c8-123">Expand the **Records to include** section.</span></span>
7. <span data-ttu-id="fb7c8-124">选择 **筛选器**。</span><span class="sxs-lookup"><span data-stu-id="fb7c8-124">Select **Filter**.</span></span>
8. <span data-ttu-id="fb7c8-125">在 **条件** 字段中，输入“客户 ID”。</span><span class="sxs-lookup"><span data-stu-id="fb7c8-125">In the **Criteria** field, enter a Customer ID.</span></span> <span data-ttu-id="fb7c8-126">例如，输入 'US-001'。</span><span class="sxs-lookup"><span data-stu-id="fb7c8-126">For example, enter 'US-001'.</span></span>
9. <span data-ttu-id="fb7c8-127">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="fb7c8-127">Select **OK**.</span></span>
10. <span data-ttu-id="fb7c8-128">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="fb7c8-128">Select **OK**.</span></span>

## <a name="print-collection-letters"></a><span data-ttu-id="fb7c8-129">打印收款单</span><span class="sxs-lookup"><span data-stu-id="fb7c8-129">Print collection letters</span></span>
1. <span data-ttu-id="fb7c8-130">转到 **导航窗格 > 模块 > 信用与收款 > 催款单 > 审核和处理催款单**。</span><span class="sxs-lookup"><span data-stu-id="fb7c8-130">Go to **navigation pane > Modules > Credit and collections > Collection letter > Review and process collection letters**.</span></span>
2. <span data-ttu-id="fb7c8-131">在 **状态** 字段中，选择 **创建**。</span><span class="sxs-lookup"><span data-stu-id="fb7c8-131">In the **Status** field, select **Created**.</span></span>
3. <span data-ttu-id="fb7c8-132">在 **打印** 字段中，选择 **不打印**。</span><span class="sxs-lookup"><span data-stu-id="fb7c8-132">In the **Printed** field, select **Not printed**.</span></span>
4. <span data-ttu-id="fb7c8-133">选择 **打印**。</span><span class="sxs-lookup"><span data-stu-id="fb7c8-133">Select **Print**.</span></span>
5. <span data-ttu-id="fb7c8-134">选择 **催款单**。</span><span class="sxs-lookup"><span data-stu-id="fb7c8-134">Select **Collection letter note**.</span></span>
6. <span data-ttu-id="fb7c8-135">在 **参数** 部分中，输入过帐的截止日期。</span><span class="sxs-lookup"><span data-stu-id="fb7c8-135">In the **Parameters** section, enter the cutoff date for postings.</span></span>
7. <span data-ttu-id="fb7c8-136">展开 **要包括的记录** 部分，然后输入催款单的详细信息。</span><span class="sxs-lookup"><span data-stu-id="fb7c8-136">Expand the **Records to include** section and enter the details of the Collection letter note.</span></span>
8. <span data-ttu-id="fb7c8-137">选择 **确定** 以打印催款单。</span><span class="sxs-lookup"><span data-stu-id="fb7c8-137">Select **OK** to print the collection letter.</span></span>
9. <span data-ttu-id="fb7c8-138">过帐收款单。</span><span class="sxs-lookup"><span data-stu-id="fb7c8-138">Post the collection letter.</span></span>

    1. <span data-ttu-id="fb7c8-139">选择 **过帐**。</span><span class="sxs-lookup"><span data-stu-id="fb7c8-139">Select **Post**.</span></span>
    1. <span data-ttu-id="fb7c8-140">输入该收款单的过帐日期</span><span class="sxs-lookup"><span data-stu-id="fb7c8-140">Enter the posting date for the collection letter.</span></span>
    1. <span data-ttu-id="fb7c8-141">扩展 **要包括的记录** 部分。</span><span class="sxs-lookup"><span data-stu-id="fb7c8-141">Expand the **Records to include** section.</span></span>
    1. <span data-ttu-id="fb7c8-142">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="fb7c8-142">Select **OK**.</span></span>
    1. <span data-ttu-id="fb7c8-143">在 **状态** 字段中，选择 **已过帐**。</span><span class="sxs-lookup"><span data-stu-id="fb7c8-143">In the **Status** field, select **Posted**.</span></span>
    1. <span data-ttu-id="fb7c8-144">在 **打印** 字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="fb7c8-144">In the **Printed** field, select an option.</span></span>

## <a name="control-collection-letters-at-the-customer-level"></a><span data-ttu-id="fb7c8-145">在客户级别控制催款单</span><span class="sxs-lookup"><span data-stu-id="fb7c8-145">Control collection letters at the customer level</span></span>
<span data-ttu-id="fb7c8-146">如果在交易记录级别设置催款单，则可以根据交易帐龄为一个客户生成多张催款单。</span><span class="sxs-lookup"><span data-stu-id="fb7c8-146">If collection letters are set up at the transaction level, multiple letters might be generated for a customer, based on transaction aging.</span></span> <span data-ttu-id="fb7c8-147">如果交易在不同催款单序列中显示，将为客户的每组逾期交易生成单独的催款单。</span><span class="sxs-lookup"><span data-stu-id="fb7c8-147">If transactions appear in different letter sequences, separate collection letters will be generated for each group of overdue transactions for the customer.</span></span> <span data-ttu-id="fb7c8-148">因此，可能会发生如下情况：一位客户可能会收到一张针对逾期 60 天的交易的催款单，以及另一张针对逾期 90 天的交易的催款单。</span><span class="sxs-lookup"><span data-stu-id="fb7c8-148">Therefore, an individual customer might receive, for example, one collection letter for transactions that are 60 days overdue and another collection letter for transactions that are 90 days overdue.</span></span> 

<span data-ttu-id="fb7c8-149">每张催款单还与一个催款单代码关联。</span><span class="sxs-lookup"><span data-stu-id="fb7c8-149">Each collection letter is also associated with a collection letter code.</span></span> <span data-ttu-id="fb7c8-150">催款单代码与单个交易关联，用于确定何时应该为每个交易生成下一张催款单。</span><span class="sxs-lookup"><span data-stu-id="fb7c8-150">The collection letter code is associated with individual transactions and is used to determine when the next collection letter should be generated for each transaction.</span></span> <span data-ttu-id="fb7c8-151">例如，如果一个交易预期超过 30 天，则催款单代码确定交易预期 60 天且尚未支付时，发送下一张催款单。</span><span class="sxs-lookup"><span data-stu-id="fb7c8-151">For example, if a transaction is more than 30 days overdue, the collection letter code determines that the next collection letter will be sent when the transaction becomes 60 days overdue, if it isn't paid before then.</span></span> 

<span data-ttu-id="fb7c8-152">也可以在客户级别设置催款单。</span><span class="sxs-lookup"><span data-stu-id="fb7c8-152">Collection letters can also be set up at the customer level.</span></span> <span data-ttu-id="fb7c8-153">在此情况下，将跟踪每个交易的催款单代码，但催款单处理将基于为客户存储的单个催款单级别。</span><span class="sxs-lookup"><span data-stu-id="fb7c8-153">In this case, the collection letter code for each transaction is tracked, but collection letter processing will be based on a single collection letter level that is stored for the customer.</span></span> <span data-ttu-id="fb7c8-154">单个催款单将包含对于客户已逾期的所有交易记录。</span><span class="sxs-lookup"><span data-stu-id="fb7c8-154">The single collection letter will contain all the transactions that are overdue for the customer.</span></span> <span data-ttu-id="fb7c8-155">由于宽限天数现在在客户级别跟踪，下一个催款单将在序列中下一个催款单经过的宽限天数后发送，即使交易记录在上一个催款单发送之后变为逾期。</span><span class="sxs-lookup"><span data-stu-id="fb7c8-155">Because the grace days are now tracked at the customer level, the next collection letter won't be sent until the number of grace days has passed for the next collection letter in the sequence, even though transactions became overdue after the last collection letter was sent.</span></span> <span data-ttu-id="fb7c8-156">此选项可帮助减少您必须向每个客户发送的催款单数量。</span><span class="sxs-lookup"><span data-stu-id="fb7c8-156">This option helps reduce the number of collection letters that you must send to each customer.</span></span>

### <a name="set-up-the-customer-to-control-collection-letters-at-the-customer-level"></a><span data-ttu-id="fb7c8-157">将客户设置为在客户级别控制催款单</span><span class="sxs-lookup"><span data-stu-id="fb7c8-157">Set up the customer to control collection letters at the customer level</span></span>
1.  <span data-ttu-id="fb7c8-158">转到 **导航窗格 > 模块 > 信用和收款 > 设置 > 应收帐款参数**，然后选择 **收款** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="fb7c8-158">Go to **Navigation pane > Modules > Credit and collections > Setup > Accounts receivable parameters** and select the **Collections** tab.</span></span> 
2.  <span data-ttu-id="fb7c8-159">将 **依据以下条件创建催款单** 值更改为 **客户**。</span><span class="sxs-lookup"><span data-stu-id="fb7c8-159">Change the value of **Create collection letter per** to **Customer**.</span></span> 
3.  <span data-ttu-id="fb7c8-160">转到 **导航窗格 > 模块 > 信用与收款 > 催款单 > 审核和处理催款单**。</span><span class="sxs-lookup"><span data-stu-id="fb7c8-160">Go to **navigation pane > Modules > Credit and collections > Collection letter > Review and process collection letters**.</span></span> <span data-ttu-id="fb7c8-161">将只为客户生成一个催款单，其中包含所有逾期的交易记录。</span><span class="sxs-lookup"><span data-stu-id="fb7c8-161">Only one collection letter will be generated for a customer with all the overdue transactions.</span></span>

## <a name="ignore-payments-and-credit-memos-when-calculating-the-collection-letter-code"></a><span data-ttu-id="fb7c8-162">忽略计算催款单代码时的付款及贷项通知单</span><span class="sxs-lookup"><span data-stu-id="fb7c8-162">Ignore payments and credit memos when calculating the collection letter code</span></span>
<span data-ttu-id="fb7c8-163">如果您在将包含在催款单中的交易记录中包含付款及贷项通知单，您可能有将触发催款单的付款或贷项通知单。</span><span class="sxs-lookup"><span data-stu-id="fb7c8-163">If you include payments and credit memos in the transactions that will be included in the collection letters, you may have payments or credit memos that will trigger a collection letter.</span></span> <span data-ttu-id="fb7c8-164">您可以通过更改 **忽略计算催款单代码时的付款及贷项通知单** 参数来控制付款及贷项通知单如何控制催款单代码。</span><span class="sxs-lookup"><span data-stu-id="fb7c8-164">You can control how payments and credit memos control the collection letter code by changing the value of the **Ignore payments and credit memos when calculating the collection letter code** parameter.</span></span> 

<span data-ttu-id="fb7c8-165">若要忽略计算催款单代码时的付款及贷项通知单，请执行以下操作。</span><span class="sxs-lookup"><span data-stu-id="fb7c8-165">To ignore payments and credit memos when calculating the collection letter code, do the following.</span></span>

1. <span data-ttu-id="fb7c8-166">转到 **导航窗格 > 模块 > 信用和收款 > 设置 > 应收帐款参数**，然后单击 **收款** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="fb7c8-166">Go to **Navigation pane > Modules > Credit and collections > Setup > Accounts receivable parameters** and click the **Collections** tab.</span></span> 
2. <span data-ttu-id="fb7c8-167">将 **忽略计算催款单代码时的付款及贷项通知单** 的值更改为 **是**。</span><span class="sxs-lookup"><span data-stu-id="fb7c8-167">Change the value of **Ignore payments and credit memos when calculating the collection letter code** to **Yes**.</span></span>
