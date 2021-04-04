---
title: 处理催款单示例
description: 本主题详细介绍了一个示例，以显示创建、打印和过帐催款单的过程。
author: JodiChristiansen
manager: AnnBe
ms.date: 02/03/2021
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPosting, CustCollectionLetterNote
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-02-03
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: df4252513f9e3a02632561b4e465c98edc888ea7
ms.sourcegitcommit: 4ecc1bf82fbb04882d7ef5e1994ef3c07ef953dc
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/08/2021
ms.locfileid: "5558303"
---
# <a name="process-collection-letters-example"></a><span data-ttu-id="552b0-103">处理催款单示例</span><span class="sxs-lookup"><span data-stu-id="552b0-103">Process collection letters example</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="552b0-104">本主题详细介绍了一个示例，以显示创建、打印和过帐催款单的过程。</span><span class="sxs-lookup"><span data-stu-id="552b0-104">This topic goes through an example that shows the process of creating, printing, and posting collection letters.</span></span> <span data-ttu-id="552b0-105">该示例基于信用和收款中的 **忽略计算催款单代码时的付款及贷项通知单** 选项。</span><span class="sxs-lookup"><span data-stu-id="552b0-105">The example is based on the **Ignore payments and credit memos when calculating collection letter code** option in Credit and collections.</span></span> <span data-ttu-id="552b0-106">它使用 USMF 演示公司和新客户 US-045 中的数据。</span><span class="sxs-lookup"><span data-stu-id="552b0-106">It uses data in the USMF demo company and a new customer, US-045.</span></span>

<span data-ttu-id="552b0-107">首先，请转到 **应收账款 \> 客户 \> 所有客户**，选择 **新建**，然后输入所需的信息以创建客户 US-045。</span><span class="sxs-lookup"><span data-stu-id="552b0-107">To begin, go to **Accounts receivable \> Customers \> All customers**, select **New**, and then enter the required information to create customer US-045.</span></span>

<span data-ttu-id="552b0-108">在完成后，请执行下面的步骤。</span><span class="sxs-lookup"><span data-stu-id="552b0-108">When you've finished, follow these steps.</span></span>

1. <span data-ttu-id="552b0-109">转到 **信用和收款 \> 催款单 \> 设置催款单顺序**，然后设置分配给客户过帐配置文件的催款单顺序，如下表中所示。</span><span class="sxs-lookup"><span data-stu-id="552b0-109">Go to **Credit and collections \> Collection letter \> Setup collection letter sequence**, and set up the collection letter sequence as shown in the following table that is assigned to the customer posting profile.</span></span>

|     <span data-ttu-id="552b0-110">催款单代码</span><span class="sxs-lookup"><span data-stu-id="552b0-110">Collection   letter code</span></span>      |     <span data-ttu-id="552b0-111">说明</span><span class="sxs-lookup"><span data-stu-id="552b0-111">Description</span></span>                           |     <span data-ttu-id="552b0-112">货币</span><span class="sxs-lookup"><span data-stu-id="552b0-112">Currency</span></span>      |     <span data-ttu-id="552b0-113">主帐户</span><span class="sxs-lookup"><span data-stu-id="552b0-113">Main   account</span></span>        |     <span data-ttu-id="552b0-114">用币种表示的费用</span><span class="sxs-lookup"><span data-stu-id="552b0-114">Fee   in currency</span></span>     |     <span data-ttu-id="552b0-115">高于以下值的最小金额</span><span class="sxs-lookup"><span data-stu-id="552b0-115">Minimum   over</span></span>        |     <span data-ttu-id="552b0-116">冻结天数</span><span class="sxs-lookup"><span data-stu-id="552b0-116">Days   Block</span></span>      |
|---------------------------------  |---------------------------------------    |-----------------  |-----------------------    |-------------------------- |-----------------------    |---------------------  |
|     <span data-ttu-id="552b0-117">催款单 1</span><span class="sxs-lookup"><span data-stu-id="552b0-117">Collection   letter 1</span></span>         |     <span data-ttu-id="552b0-118">第二次费用通知</span><span class="sxs-lookup"><span data-stu-id="552b0-118">Second   notification with fee</span></span>        |     <span data-ttu-id="552b0-119">USD</span><span class="sxs-lookup"><span data-stu-id="552b0-119">USD</span></span>           |                           |     <span data-ttu-id="552b0-120">0.00</span><span class="sxs-lookup"><span data-stu-id="552b0-120">0.00</span></span>                  |     <span data-ttu-id="552b0-121">0.00</span><span class="sxs-lookup"><span data-stu-id="552b0-121">0.00</span></span>                  |     <span data-ttu-id="552b0-122">2</span><span class="sxs-lookup"><span data-stu-id="552b0-122">2</span></span>                 |
|     <span data-ttu-id="552b0-123">催款单 2</span><span class="sxs-lookup"><span data-stu-id="552b0-123">Collection   letter 2</span></span>         |     <span data-ttu-id="552b0-124">第二次费用通知</span><span class="sxs-lookup"><span data-stu-id="552b0-124">Second   notification with fee</span></span>        |     <span data-ttu-id="552b0-125">USC</span><span class="sxs-lookup"><span data-stu-id="552b0-125">USC</span></span>           |     <span data-ttu-id="552b0-126">403150</span><span class="sxs-lookup"><span data-stu-id="552b0-126">403150</span></span>                |     <span data-ttu-id="552b0-127">20.00</span><span class="sxs-lookup"><span data-stu-id="552b0-127">20.00</span></span>                 |     <span data-ttu-id="552b0-128">10.00</span><span class="sxs-lookup"><span data-stu-id="552b0-128">10.00</span></span>                 |     <span data-ttu-id="552b0-129">3</span><span class="sxs-lookup"><span data-stu-id="552b0-129">3</span></span>                 |
|     <span data-ttu-id="552b0-130">收款</span><span class="sxs-lookup"><span data-stu-id="552b0-130">Collection</span></span>                    |     <span data-ttu-id="552b0-131">最后一次费用通知</span><span class="sxs-lookup"><span data-stu-id="552b0-131">Final   notification with fee</span></span>         |     <span data-ttu-id="552b0-132">USD</span><span class="sxs-lookup"><span data-stu-id="552b0-132">USD</span></span>           |     <span data-ttu-id="552b0-133">403150</span><span class="sxs-lookup"><span data-stu-id="552b0-133">403150</span></span>                |     <span data-ttu-id="552b0-134">50.00</span><span class="sxs-lookup"><span data-stu-id="552b0-134">50.00</span></span>                 |     <span data-ttu-id="552b0-135">100.00</span><span class="sxs-lookup"><span data-stu-id="552b0-135">100.00</span></span>                |     <span data-ttu-id="552b0-136">15</span><span class="sxs-lookup"><span data-stu-id="552b0-136">15</span></span>                |

<span data-ttu-id="552b0-137">下图显示了表格中的信息，该信息与 **催款单** 页上显示的信息完全一样。</span><span class="sxs-lookup"><span data-stu-id="552b0-137">The following illustration shows the information that's in the table as it would appear on the **Collection letters** page.</span></span> 

<span data-ttu-id="552b0-138">[![设置催款单序列](./media/Ignore-payments-creditmemos-1.PNG)](./media/Ignore-payments-creditmemos-1.PNG)</span><span class="sxs-lookup"><span data-stu-id="552b0-138">[![Setting up a collection letter sequence](./media/Ignore-payments-creditmemos-1.PNG)](./media/Ignore-payments-creditmemos-1.PNG)</span></span>

 <span data-ttu-id="552b0-139">现在，您必须设置此示例所需的两个参数。</span><span class="sxs-lookup"><span data-stu-id="552b0-139">You must now set the two parameters that are required for this example.</span></span>

2. <span data-ttu-id="552b0-140">转到 **信用和收款 \> 设置 \> 应收帐款参数**，然后按照以下步骤操作：</span><span class="sxs-lookup"><span data-stu-id="552b0-140">Go to **Credit and collections \> Setup \> Accounts receivable parameters**, and follow these steps:</span></span>

    1. <span data-ttu-id="552b0-141">在 **收款** 选项卡上，将 **忽略计算催款单代码时的付款及贷项通知单** 选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="552b0-141">On the **Collections** tab, set the **Ignore payments and credit memos when calculating collection letter code** option to **Yes**.</span></span>
    2. <span data-ttu-id="552b0-142">确保将 **依据以下条件创建催款单** 字段设置为 **客户**。</span><span class="sxs-lookup"><span data-stu-id="552b0-142">Make sure that the **Create collection letter per** field is set to **Customer**.</span></span>

    <span data-ttu-id="552b0-143">[![设置信用收款的应收帐款参数](./media/Ignore-payments-creditmemos-2.PNG)](./media/Ignore-payments-creditmemos-2.PNG)</span><span class="sxs-lookup"><span data-stu-id="552b0-143">[![Setting Accounts receivable parameters for Credit collections](./media/Ignore-payments-creditmemos-2.PNG)](./media/Ignore-payments-creditmemos-2.PNG)</span></span>

3. <span data-ttu-id="552b0-144">转到 **应收帐款 \> 发票 \> 所有普通发票**，选择 **新建**，然后按照以下步骤执行操作：</span><span class="sxs-lookup"><span data-stu-id="552b0-144">Go to **Accounts receivable \> Invoices \> All free text invoices**, select **New**, and then follow these steps:</span></span>

    1. <span data-ttu-id="552b0-145">在 **客户帐户** 字段中选择 **US-045**。</span><span class="sxs-lookup"><span data-stu-id="552b0-145">In the **Customer account** field select **US-045**.</span></span>
    2. <span data-ttu-id="552b0-146">在 **发票日期** 字段中，输入 **1/15/2021**。</span><span class="sxs-lookup"><span data-stu-id="552b0-146">In the **Invoice date** field, enter **1/15/2021**.</span></span>
    3. <span data-ttu-id="552b0-147">在 **截止日期** 字段中，输入 **1/16/2021**。</span><span class="sxs-lookup"><span data-stu-id="552b0-147">In the **Due date** field, enter **1/16/2021**.</span></span>
    4. <span data-ttu-id="552b0-148">在 **发票行** 快速选项卡上的 **主帐户** 字段中，输入 **401100**。</span><span class="sxs-lookup"><span data-stu-id="552b0-148">On the **Invoice lines** FastTab, in the **Main account** field, enter **401100**.</span></span>
    5. <span data-ttu-id="552b0-149">在 **单位价格** 字段中，输入 **500.00**。</span><span class="sxs-lookup"><span data-stu-id="552b0-149">In the **Unit price** field, enter **500.00**.</span></span>
    6. <span data-ttu-id="552b0-150">选择 **过帐**。</span><span class="sxs-lookup"><span data-stu-id="552b0-150">Select **Post**.</span></span>

    <span data-ttu-id="552b0-151">现在，您必须为客户输入两个贷方通知单。</span><span class="sxs-lookup"><span data-stu-id="552b0-151">You must now enter two credit notes for the customer.</span></span>

4. <span data-ttu-id="552b0-152">选择 **新建**，然后按照以下步骤操作：</span><span class="sxs-lookup"><span data-stu-id="552b0-152">Select **New**, and then follow these steps:</span></span>

    1. <span data-ttu-id="552b0-153">在 **客户帐户** 字段中选择 **US-045**。</span><span class="sxs-lookup"><span data-stu-id="552b0-153">In the **Customer account** field, select **US-045**.</span></span>
    2. <span data-ttu-id="552b0-154">在 **发票日期** 字段中，输入 **1/15/2021**。</span><span class="sxs-lookup"><span data-stu-id="552b0-154">In the **Invoice date** field, enter **1/15/2021**.</span></span>
    3. <span data-ttu-id="552b0-155">在 **截止日期** 字段中，输入 **1/16/2021**。</span><span class="sxs-lookup"><span data-stu-id="552b0-155">In the **Due date** field, enter **1/16/2021**.</span></span>
    4. <span data-ttu-id="552b0-156">在 **发票行** 快速选项卡上的 **主帐户** 字段中，输入 **401100**。</span><span class="sxs-lookup"><span data-stu-id="552b0-156">On the **Invoice lines** FastTab, in the **Main account** field, enter **401100**.</span></span>
    5. <span data-ttu-id="552b0-157">在 **单价** 字段中，输入 **-100.00**。</span><span class="sxs-lookup"><span data-stu-id="552b0-157">In the **Unit price** field, enter **-100.00**.</span></span>
    6. <span data-ttu-id="552b0-158">选择 **过帐**。</span><span class="sxs-lookup"><span data-stu-id="552b0-158">Select **Post**.</span></span>

5. <span data-ttu-id="552b0-159">重复步骤 4，但在 **单价** 字段中输入 **-200.00**。</span><span class="sxs-lookup"><span data-stu-id="552b0-159">Repeat step 4, but enter **-200.00** in the **Unit price** field.</span></span>
6. <span data-ttu-id="552b0-160">转到 **应收帐款 \> 客户 \> 所有客户**，然后选择客户 **US-045**。</span><span class="sxs-lookup"><span data-stu-id="552b0-160">Go to **Accounts receivable \> Customers \> All customers**, and select customer **US-045**.</span></span> <span data-ttu-id="552b0-161">然后，在操作窗格上，选择 **交易 \> 交易** 以查看您先前过帐的客户交易。</span><span class="sxs-lookup"><span data-stu-id="552b0-161">Then, on the Action Pane, select **Transactions \> Transactions** to review the customer transactions that you posted earlier.</span></span>

    <span data-ttu-id="552b0-162">[![查看已过帐的客户交易](./media/Ignore-payments-creditmemos-3.PNG)](./media/Ignore-payments-creditmemos-3.PNG)</span><span class="sxs-lookup"><span data-stu-id="552b0-162">[![Reviewing the posted customer transactions](./media/Ignore-payments-creditmemos-3.PNG)](./media/Ignore-payments-creditmemos-3.PNG)</span></span>

    <span data-ttu-id="552b0-163">现在，您必须为客户 US-045 创建催款单。</span><span class="sxs-lookup"><span data-stu-id="552b0-163">You must now create collection letters for customer US-045.</span></span>

7. <span data-ttu-id="552b0-164">转到 **信用与收款 \> 催款单 \> 创建催款单**，然后按照以下步骤操作：</span><span class="sxs-lookup"><span data-stu-id="552b0-164">Go to **Credit and collections \> Collection letter \> Create collection letters**, and follow these steps:</span></span>

    1. <span data-ttu-id="552b0-165">将 **发票** 和 **贷方通知单** 选项设置 **是**。</span><span class="sxs-lookup"><span data-stu-id="552b0-165">Set the **Invoice** and **Credit note** options to **Yes**.</span></span>

        <span data-ttu-id="552b0-166">默认情况下，**催款单** 字段应设置为 **每个客户一个催款单**。</span><span class="sxs-lookup"><span data-stu-id="552b0-166">By default, the **Collection letter** field should be set to **Collection per customer**.</span></span>

    2. <span data-ttu-id="552b0-167">在 **催款单日期** 字段中，输入 **1/19/2021**。</span><span class="sxs-lookup"><span data-stu-id="552b0-167">In the **Collection letter date** field, enter **1/19/2021**.</span></span>
    3. <span data-ttu-id="552b0-168">在 **要包括的记录** 快速选项卡上，选择 **筛选**，然后在 **客户帐户** 字段中，添加客户 **US-045**。</span><span class="sxs-lookup"><span data-stu-id="552b0-168">On the **Records to include** FastTab, select **Filter**, and then, in the **Customer account** field, add customer **US-045**.</span></span>
    4. <span data-ttu-id="552b0-169">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="552b0-169">Select **OK**.</span></span>
    5. <span data-ttu-id="552b0-170">选择 **确定** 以创建催款单。</span><span class="sxs-lookup"><span data-stu-id="552b0-170">Select **OK** to create collection letters.</span></span>

8. <span data-ttu-id="552b0-171">转到 **信用与收款 \> 催款单 \> 查看和处理催款单**，然后按照以下步骤操作：</span><span class="sxs-lookup"><span data-stu-id="552b0-171">Go to **Credit and collections \> Collection letter \> Review and process collection letters**, and follow these steps:</span></span>

    1. <span data-ttu-id="552b0-172">请注意，抬头和交易行上的催款单代码均为 **催款单 1**，因为此催款单是序列中的第一个催款单。</span><span class="sxs-lookup"><span data-stu-id="552b0-172">Notice that the collection letter code on both the header and the transaction lines is **Collection letter 1**, because this collection letter is the first collection letter in the sequence.</span></span> <span data-ttu-id="552b0-173">（要查看交易行，您可能必须选择 **交易** 快速选项卡。）</span><span class="sxs-lookup"><span data-stu-id="552b0-173">(To view the transaction lines, you might have to select the **Transactions** FastTab.)</span></span>

   <span data-ttu-id="552b0-174">[![验证相同的催款单代码是否会出现在抬头和行上](./media/Ignore-payments-creditmemos-4.PNG)](./media/Ignore-payments-creditmemos-4.PNG)</span><span class="sxs-lookup"><span data-stu-id="552b0-174">[![Verifying that the same collection letter code appears on the header and the lines](./media/Ignore-payments-creditmemos-4.PNG)](./media/Ignore-payments-creditmemos-4.PNG)</span></span>

    2. <span data-ttu-id="552b0-175">在操作窗格上，选择 **过帐**。</span><span class="sxs-lookup"><span data-stu-id="552b0-175">On the Action Pane, select **Post**.</span></span>
    3. <span data-ttu-id="552b0-176">在 **过帐日期** 字段中，输入 **1/19/2021**。</span><span class="sxs-lookup"><span data-stu-id="552b0-176">In the **Posting date** field, enter **1/19/2021**.</span></span>

    <span data-ttu-id="552b0-177">现在，您必须再次为客户 US-045 创建收款单。</span><span class="sxs-lookup"><span data-stu-id="552b0-177">You must now create collection letters again for customer US-045.</span></span>

9. <span data-ttu-id="552b0-178">转到 **信用与收款 \> 催款单 \> 创建催款单**，然后按照以下步骤操作：</span><span class="sxs-lookup"><span data-stu-id="552b0-178">Go to **Credit and collections \> Collection letter \> Create collection letters**, and follow these steps:</span></span>

    1. <span data-ttu-id="552b0-179">将 **发票** 和 **贷方通知单** 选项设置 **是**。</span><span class="sxs-lookup"><span data-stu-id="552b0-179">Set the **Invoice** and **Credit note** options to **Yes**.</span></span>

        <span data-ttu-id="552b0-180">默认情况下，**催款单** 字段应设置为 **每个客户一个催款单**。</span><span class="sxs-lookup"><span data-stu-id="552b0-180">By default, the **Collection letter** field should be set to **Collection per customer**.</span></span>

    2. <span data-ttu-id="552b0-181">在 **催款单日期** 字段中，输入 **1/23/2021**。</span><span class="sxs-lookup"><span data-stu-id="552b0-181">In the **Collection letter date** field, enter **1/23/2021**.</span></span>
    3. <span data-ttu-id="552b0-182">在 **要包括的记录** 快速选项卡上，选择 **筛选**，然后在 **客户帐户** 字段中，添加客户 **US-045**。</span><span class="sxs-lookup"><span data-stu-id="552b0-182">On the **Records to include** FastTab, select **Filter**, and then, in the **Customer account** field, add customer **US-045**.</span></span>
    4. <span data-ttu-id="552b0-183">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="552b0-183">Select **OK**.</span></span>
    5. <span data-ttu-id="552b0-184">选择 **确定** 以创建催款单。</span><span class="sxs-lookup"><span data-stu-id="552b0-184">Select **OK** to create collection letters.</span></span>

10. <span data-ttu-id="552b0-185">转到 **信用与收款 \> 催款单 \> 查看和处理催款单**，然后按照以下步骤操作：</span><span class="sxs-lookup"><span data-stu-id="552b0-185">Go to **Credit and collections \> Collection letter \> Review and process collection letters**, and follow these steps:</span></span>

    1. <span data-ttu-id="552b0-186">请注意，抬头上的催款单代码为 **催款单 1**。</span><span class="sxs-lookup"><span data-stu-id="552b0-186">Notice that the collection letter code on the header is **Collection letter 1**.</span></span> <span data-ttu-id="552b0-187">但是，交易行上的代码是 **催款单 2**。</span><span class="sxs-lookup"><span data-stu-id="552b0-187">However, the code on the transaction lines is **Collection letter 2**.</span></span>

   <span data-ttu-id="552b0-188">[![验证不同的催款单代码是否会出现在抬头和行上](./media/Ignore-payments-creditmemos-5.PNG)](./media/Ignore-payments-creditmemos-5.PNG)</span><span class="sxs-lookup"><span data-stu-id="552b0-188">[![Verifies that different collection letter codes appear on the header and the lines](./media/Ignore-payments-creditmemos-5.PNG)](./media/Ignore-payments-creditmemos-5.PNG)</span></span>

  <span data-ttu-id="552b0-189">因为 **忽略计算催款单代码时的付款及贷项通知单** 选项设置为 **是**，所以代码不同。</span><span class="sxs-lookup"><span data-stu-id="552b0-189">The codes differ because the **Ignore payments and credit memos when calculating collection letter code** option is to **Yes**.</span></span>

  2. <span data-ttu-id="552b0-190">不过帐催款单。</span><span class="sxs-lookup"><span data-stu-id="552b0-190">Don't post this collection letter.</span></span>

11. <span data-ttu-id="552b0-191">转到 **信用和收款 \> 设置 \> 应收帐款参数**，然后在 **收款** 选项卡上，将 **忽略计算催款单代码时的付款及贷项通知单** 选项设置为 **否**。</span><span class="sxs-lookup"><span data-stu-id="552b0-191">Go to **Credit and collections \> Setup \> Accounts receivable parameters**, and then, on the **Collections** tab, set the **Ignore payments and credit memos when calculating collection letter code** option to **No**.</span></span>

    <span data-ttu-id="552b0-192">[![将“忽略计算催款单代码时的付款及贷项通知单”选项设置为“否”](./media/Ignore-payments-creditmemos-6.PNG)](./media/Ignore-payments-creditmemos-6.PNG)</span><span class="sxs-lookup"><span data-stu-id="552b0-192">[![Setting the Ignore payments and credit memos when calculating collection letter code option to No](./media/Ignore-payments-creditmemos-6.PNG)](./media/Ignore-payments-creditmemos-6.PNG)</span></span>

    <span data-ttu-id="552b0-193">现在，您必须再次为客户 US-045 创建收款单。</span><span class="sxs-lookup"><span data-stu-id="552b0-193">You must now create collection letters again for customer US-045.</span></span>

12. <span data-ttu-id="552b0-194">转到 **信用与收款 \> 催款单 \> 创建催款单**，然后按照以下步骤操作：</span><span class="sxs-lookup"><span data-stu-id="552b0-194">Go to **Credit and collections \> Collection letter \> Create collection letters**, and follow these steps:</span></span>

    1. <span data-ttu-id="552b0-195">将 **发票** 和 **贷方通知单** 选项设置 **是**。</span><span class="sxs-lookup"><span data-stu-id="552b0-195">Set the **Invoice** and **Credit note** options to **Yes**.</span></span>

        <span data-ttu-id="552b0-196">默认情况下，**催款单** 字段应设置为 **每个客户一个催款单**。</span><span class="sxs-lookup"><span data-stu-id="552b0-196">By default, the **Collection letter** field should be set to **Collection per customer**.</span></span>

    2. <span data-ttu-id="552b0-197">在 **催款单日期** 字段中，输入 **1/23/2021**。</span><span class="sxs-lookup"><span data-stu-id="552b0-197">In the **Collection letter date** field, enter **1/23/2021**.</span></span>
    3. <span data-ttu-id="552b0-198">在 **要包括的记录** 快速选项卡上，选择 **筛选**，然后在 **客户帐户** 字段中，添加客户 **US-045**。</span><span class="sxs-lookup"><span data-stu-id="552b0-198">On the **Records to include** FastTab, select **Filter**, and then, in the **Customer account** field, add customer **US-045**.</span></span>
    4. <span data-ttu-id="552b0-199">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="552b0-199">Select **OK**.</span></span>
    5. <span data-ttu-id="552b0-200">选择 **确定** 以创建催款单。</span><span class="sxs-lookup"><span data-stu-id="552b0-200">Select **OK** to create collection letters.</span></span>

13. <span data-ttu-id="552b0-201">转到 **信用和收款 \> 催款单 \> 查看并处理催款单**，请注意，抬头和交易行上的催款单代码均为 **催款单 2**。</span><span class="sxs-lookup"><span data-stu-id="552b0-201">Go to **Credit and collections \> Collection letter \> Review and process collection letters**, and notice that the collection letter code on both the header and the transaction lines is **Collection letter 2**.</span></span>

    <span data-ttu-id="552b0-202">[![再次显示相同的催款单代码会出现在抬头和行上](./media/Ignore-payments-creditmemos-7.PNG)](./media/Ignore-payments-creditmemos-7.PNG)</span><span class="sxs-lookup"><span data-stu-id="552b0-202">[![Showing again that the same collection letter code appears on the header and the lines](./media/Ignore-payments-creditmemos-7.PNG)](./media/Ignore-payments-creditmemos-7.PNG)</span></span>

    <span data-ttu-id="552b0-203">因为 **忽略计算催款单代码时的付款及贷项通知单** 选项现在设置为 **是**，所以这两个位置会出现相同的代码。</span><span class="sxs-lookup"><span data-stu-id="552b0-203">The same code appears in both places because the **Ignore payments and credit memos when calculating collection letter code** option is now set to **No**.</span></span>
