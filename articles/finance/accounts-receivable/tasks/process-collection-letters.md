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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2018-12-01
ms.dyn365.ops.version: 8.1.3
ms.openlocfilehash: 326d9375670cb4f4990a4f7070bf923a28b2c025
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/27/2019
ms.locfileid: "2176640"
---
# <a name="process-collection-letters"></a><span data-ttu-id="54724-103">处理催款单</span><span class="sxs-lookup"><span data-stu-id="54724-103">Process collection letters</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="54724-104">该主题说明如何创建、打印并过帐收款单。</span><span class="sxs-lookup"><span data-stu-id="54724-104">This topic shows how to create, print, and post collection letters.</span></span> <span data-ttu-id="54724-105">此任务使用 USMF 公司演示。</span><span class="sxs-lookup"><span data-stu-id="54724-105">This task uses the USMF demo company.</span></span>

## <a name="set-up-a-collection-letter-sequence-on-the-posting-profile"></a><span data-ttu-id="54724-106">在该过帐上设置收款单的排序</span><span class="sxs-lookup"><span data-stu-id="54724-106">Set up a collection letter sequence on the posting profile</span></span>
1. <span data-ttu-id="54724-107">转到**导航窗格 > 模块 > 信用和收款 > 设置 > 客户过帐模板**。</span><span class="sxs-lookup"><span data-stu-id="54724-107">Go to **Navigation pane > Modules > Credit and collections > Setup > Customer posting profiles**.</span></span>
2. <span data-ttu-id="54724-108">单击**编辑**。</span><span class="sxs-lookup"><span data-stu-id="54724-108">Click **Edit**.</span></span>
3. <span data-ttu-id="54724-109">从下拉列表中选择收款单排序。</span><span class="sxs-lookup"><span data-stu-id="54724-109">Select a collection letter sequence from the drop-down list.</span></span> <span data-ttu-id="54724-110">如果不希望使用该过帐模板生成交易收款单，则该字段保留空白。</span><span class="sxs-lookup"><span data-stu-id="54724-110">If you do not want to generate collection letters for transactions using this posting profile, leave the field blank.</span></span>  
4. <span data-ttu-id="54724-111">展开**表限制**选项卡可以更改处理收款单的方式。</span><span class="sxs-lookup"><span data-stu-id="54724-111">Expand the **Table restrictions** tab to change the way that collection letters are processed.</span></span> <span data-ttu-id="54724-112">如果此字段设置为**是**，则将在此过帐模板创建收款单。</span><span class="sxs-lookup"><span data-stu-id="54724-112">If this field is set to **Yes**, then collection letters will be created for this posting profile.</span></span>  

## <a name="create-collection-letters"></a><span data-ttu-id="54724-113">创建催款单</span><span class="sxs-lookup"><span data-stu-id="54724-113">Create collection letters</span></span>
1. <span data-ttu-id="54724-114">转到**导航窗格 > 模块 > 信用与收款 > 收款单 > 创建收款单**。</span><span class="sxs-lookup"><span data-stu-id="54724-114">Go to **Navigation pane > Modules > Credit and collections > Collection letter > Create collection letters**.</span></span>
2. <span data-ttu-id="54724-115">选择收款单的交易类型。</span><span class="sxs-lookup"><span data-stu-id="54724-115">Select the transaction types for which you will collect letters.</span></span> <span data-ttu-id="54724-116">此计算包含这些类型的所有开放交易。</span><span class="sxs-lookup"><span data-stu-id="54724-116">All of the open transactions for these types will be included in the calculation.</span></span>  
3. <span data-ttu-id="54724-117">在**催款单**字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="54724-117">In the **Collection letter** field, select an option.</span></span>
4. <span data-ttu-id="54724-118">在**催款单日期**字段中，输入催款单的日期。</span><span class="sxs-lookup"><span data-stu-id="54724-118">In the **Collection letter date** field, enter the date of the collection letter.</span></span>
5. <span data-ttu-id="54724-119">如果将**使用过帐模板**更改为**选择**，则请选择一个过帐模板。</span><span class="sxs-lookup"><span data-stu-id="54724-119">Select a posting profile if you changed **Use posting profile from** to **Select**.</span></span> <span data-ttu-id="54724-120">具有两个过帐模板选项：</span><span class="sxs-lookup"><span data-stu-id="54724-120">There are two posting profile options:</span></span>   

   - <span data-ttu-id="54724-121">**帐户** – 使用分配给每个利息单的客户帐户的过帐模板。</span><span class="sxs-lookup"><span data-stu-id="54724-121">**Account** – Use the posting profile that is assigned to the customer account for each interest note.</span></span>   
   - <span data-ttu-id="54724-122">**选择** – 使用在**过帐模板**字段中选择的过帐模板。</span><span class="sxs-lookup"><span data-stu-id="54724-122">**Select** – Use the posting profile that you select in the **Posting profile** field.</span></span>  

6. <span data-ttu-id="54724-123">扩展**要包括的记录**部分。</span><span class="sxs-lookup"><span data-stu-id="54724-123">Expand the **Records to include** section.</span></span>
7. <span data-ttu-id="54724-124">选择**筛选器**。</span><span class="sxs-lookup"><span data-stu-id="54724-124">Select **Filter**.</span></span>
8. <span data-ttu-id="54724-125">在**条件**字段中，输入“客户 ID”。</span><span class="sxs-lookup"><span data-stu-id="54724-125">In the **Criteria** field, enter a Customer ID.</span></span> <span data-ttu-id="54724-126">例如，输入 'US-001'。</span><span class="sxs-lookup"><span data-stu-id="54724-126">For example, enter 'US-001'.</span></span>
9. <span data-ttu-id="54724-127">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="54724-127">Select **OK**.</span></span>
10. <span data-ttu-id="54724-128">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="54724-128">Select **OK**.</span></span>

## <a name="print-collection-letters"></a><span data-ttu-id="54724-129">打印收款单</span><span class="sxs-lookup"><span data-stu-id="54724-129">Print collection letters</span></span>
1. <span data-ttu-id="54724-130">转到**导航窗格 > 模块 > 信用与收款 > 催款单 > 审核和处理催款单**。</span><span class="sxs-lookup"><span data-stu-id="54724-130">Go to **navigation pane > Modules > Credit and collections > Collection letter > Review and process collection letters**.</span></span>
2. <span data-ttu-id="54724-131">在**状态**字段中，选择**创建**。</span><span class="sxs-lookup"><span data-stu-id="54724-131">In the **Status** field, select **Created**.</span></span>
3. <span data-ttu-id="54724-132">在**打印**字段中，选择**不打印**。</span><span class="sxs-lookup"><span data-stu-id="54724-132">In the **Printed** field, select **Not printed**.</span></span>
4. <span data-ttu-id="54724-133">选择**打印**。</span><span class="sxs-lookup"><span data-stu-id="54724-133">Select **Print**.</span></span>
5. <span data-ttu-id="54724-134">选择**催款单**。</span><span class="sxs-lookup"><span data-stu-id="54724-134">Select **Collection letter note**.</span></span>
6. <span data-ttu-id="54724-135">在**参数**部分中，输入过帐的截止日期。</span><span class="sxs-lookup"><span data-stu-id="54724-135">In the **Parameters** section, enter the cutoff date for postings.</span></span>
7. <span data-ttu-id="54724-136">展开**要包括的记录**部分，然后输入催款单的详细信息。</span><span class="sxs-lookup"><span data-stu-id="54724-136">Expand the **Records to include** section and enter the details of the Collection letter note.</span></span>
8. <span data-ttu-id="54724-137">选择**确定**以打印催款单。</span><span class="sxs-lookup"><span data-stu-id="54724-137">Select **OK** to print the collection letter.</span></span>
9. <span data-ttu-id="54724-138">过帐收款单。</span><span class="sxs-lookup"><span data-stu-id="54724-138">Post the collection letter.</span></span>

    1. <span data-ttu-id="54724-139">选择**过帐**。</span><span class="sxs-lookup"><span data-stu-id="54724-139">Select **Post**.</span></span>
    1. <span data-ttu-id="54724-140">输入该收款单的过帐日期</span><span class="sxs-lookup"><span data-stu-id="54724-140">Enter the posting date for the collection letter.</span></span>
    1. <span data-ttu-id="54724-141">扩展**要包括的记录**部分。</span><span class="sxs-lookup"><span data-stu-id="54724-141">Expand the **Records to include** section.</span></span>
    1. <span data-ttu-id="54724-142">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="54724-142">Select **OK**.</span></span>
    1. <span data-ttu-id="54724-143">在**状态**字段中，选择**已过帐**。</span><span class="sxs-lookup"><span data-stu-id="54724-143">In the **Status** field, select **Posted**.</span></span>
    1. <span data-ttu-id="54724-144">在**打印**字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="54724-144">In the **Printed** field, select an option.</span></span>

## <a name="control-collection-letters-at-the-customer-level"></a><span data-ttu-id="54724-145">在客户级别控制催款单</span><span class="sxs-lookup"><span data-stu-id="54724-145">Control collection letters at the customer level</span></span>
<span data-ttu-id="54724-146">您还可以在客户级别设置催款单，以便跟踪每个交易记录的催款单代码，但催款单处理将基于为客户存储的单个催款单级别。</span><span class="sxs-lookup"><span data-stu-id="54724-146">You can also set up collection letters at the customer level so that the collection letter code for each transaction is tracked, but the collection letter processing will be based on a single collection letter level that is stored for the customer.</span></span> <span data-ttu-id="54724-147">单个催款单将包含对于客户已逾期的所有交易记录。</span><span class="sxs-lookup"><span data-stu-id="54724-147">The single collection letter will contain all transactions that are overdue for the customer.</span></span> <span data-ttu-id="54724-148">由于宽限天数现在在客户级别跟踪，下一个催款单将在序列中下一个催款单经过的宽限天数后发送，即使交易记录在上一个催款单发送之后变为逾期。</span><span class="sxs-lookup"><span data-stu-id="54724-148">Because the grace days are now tracked on the customer level, the next collection letter will not be sent until the number of grace days has passed for the next collection letter in the sequence, even though transactions become overdue after the last collection letter was sent.</span></span> <span data-ttu-id="54724-149">此选项将减少您按客户发送的催款单数量。</span><span class="sxs-lookup"><span data-stu-id="54724-149">This option reduces the number of collection letters you will send per customer.</span></span> 

### <a name="set-up-the-customer-to-control-collection-letters-at-the-customer-level"></a><span data-ttu-id="54724-150">将客户设置为在客户级别控制催款单</span><span class="sxs-lookup"><span data-stu-id="54724-150">Set up the customer to control collection letters at the customer level</span></span>
1.  <span data-ttu-id="54724-151">转到**导航窗格 > 模块 > 信用和收款 > 设置 > 应收帐款参数**，然后选择**收款**选项卡。</span><span class="sxs-lookup"><span data-stu-id="54724-151">Go to **Navigation pane > Modules > Credit and collections > Setup > Accounts receivable parameters** and select the **Collections** tab.</span></span> 
2.  <span data-ttu-id="54724-152">将**依据以下条件创建催款单**值更改为**客户**。</span><span class="sxs-lookup"><span data-stu-id="54724-152">Change the value of **Create collection letter per** to **Customer**.</span></span> 
3.  <span data-ttu-id="54724-153">转到**导航窗格 > 模块 > 信用与收款 > 催款单 > 审核和处理催款单**。</span><span class="sxs-lookup"><span data-stu-id="54724-153">Go to **navigation pane > Modules > Credit and collections > Collection letter > Review and process collection letters**.</span></span> <span data-ttu-id="54724-154">将只为客户生成一个催款单，其中包含所有逾期的交易记录。</span><span class="sxs-lookup"><span data-stu-id="54724-154">Only one collection letter will be generated for a customer with all the overdue transactions.</span></span>

## <a name="ignore-payments-and-credit-memos-when-calculating-the-collection-letter-code"></a><span data-ttu-id="54724-155">忽略计算催款单代码时的付款及贷项通知单</span><span class="sxs-lookup"><span data-stu-id="54724-155">Ignore payments and credit memos when calculating the collection letter code</span></span>
<span data-ttu-id="54724-156">如果您在将包含在催款单中的交易记录中包含付款及贷项通知单，您可能有将触发催款单的付款或贷项通知单。</span><span class="sxs-lookup"><span data-stu-id="54724-156">If you include payments and credit memos in the transactions that will be included in the collection letters, you may have payments or credit memos that will trigger a collection letter.</span></span> <span data-ttu-id="54724-157">您可以通过更改**忽略计算催款单代码时的付款及贷项通知单**参数来控制付款及贷项通知单如何控制催款单代码。</span><span class="sxs-lookup"><span data-stu-id="54724-157">You can control how payments and credit memos control the collection letter code by changing the value of the **Ignore payments and credit memos when calculating the collection letter code** parameter.</span></span> 

<span data-ttu-id="54724-158">若要忽略计算催款单代码时的付款及贷项通知单，请执行以下操作。</span><span class="sxs-lookup"><span data-stu-id="54724-158">To ignore payments and credit memos when calculating the collection letter code, do the following.</span></span>

1. <span data-ttu-id="54724-159">转到**导航窗格 > 模块 > 信用和收款 > 设置 > 应收帐款参数**，然后单击**收款**选项卡。</span><span class="sxs-lookup"><span data-stu-id="54724-159">Go to **Navigation pane > Modules > Credit and collections > Setup > Accounts receivable parameters** and click the **Collections** tab.</span></span> 
2. <span data-ttu-id="54724-160">将**忽略计算催款单代码时的付款及贷项通知单**的值更改为**是**。</span><span class="sxs-lookup"><span data-stu-id="54724-160">Change the value of **Ignore payments and credit memos when calculating the collection letter code** to **Yes**.</span></span>
