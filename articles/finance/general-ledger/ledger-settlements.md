---
title: 分类帐结算
description: 本主题说明如何使用分类帐结算页面结算分类帐交易和冲销结算。
author: mikefalkner
manager: aolson
ms.date: 09/28/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerTransSettlement
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2018-11-30
ms.dyn365.ops.version: 8.1.1
ms.openlocfilehash: d41a69bed3d1340736cc7df35aa3ded032d4d79d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4440666"
---
# <a name="ledger-settlements"></a><span data-ttu-id="59307-103">分类帐结算</span><span class="sxs-lookup"><span data-stu-id="59307-103">Ledger settlements</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="59307-104">分类帐结算让您可以匹配总帐中的借方和贷方交易记录，并将其标记为已结算。</span><span class="sxs-lookup"><span data-stu-id="59307-104">Ledger settlements let you match debit and credit transactions in the general ledger, and mark them as settled.</span></span> <span data-ttu-id="59307-105">通过此方法，您可以确保清除相关的交易记录。</span><span class="sxs-lookup"><span data-stu-id="59307-105">In this way, you can make sure that related transactions have been cleared.</span></span> <span data-ttu-id="59307-106">您还可以冲销错误执行的结算。</span><span class="sxs-lookup"><span data-stu-id="59307-106">You can also reverse settlements if they were made by mistake.</span></span>

## <a name="enable-advanced-ledger-settlements"></a><span data-ttu-id="59307-107">启用高级分类帐结算</span><span class="sxs-lookup"><span data-stu-id="59307-107">Enable advanced ledger settlements</span></span>

<span data-ttu-id="59307-108">高级分类帐结算页面为筛选和选择交易记录提供其他功能。</span><span class="sxs-lookup"><span data-stu-id="59307-108">The advanced ledger settlements page provides additional capabilities for filtering and selecting transactions.</span></span> <span data-ttu-id="59307-109">若要启用高级分类帐结算页，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="59307-109">To enable advanced ledger settlements page, follow these steps.</span></span>

1. <span data-ttu-id="59307-110">选择 **总帐** \> **分类帐设置** \> **总帐参数**。</span><span class="sxs-lookup"><span data-stu-id="59307-110">Select **General ledger** \> **Ledger setup** \> **General ledger parameters**.</span></span> 
2. <span data-ttu-id="59307-111">在 **分类帐结算** 选项卡上，将 **高级分类帐结算** 选项设置为 **是** 以打开高级分类帐结算功能。</span><span class="sxs-lookup"><span data-stu-id="59307-111">On the **Ledger settlements** tab, set the **Advanced ledger settlement** option to **Yes** to turn on the advanced ledger settlement functionality.</span></span> <span data-ttu-id="59307-112">高级 **分类帐结算** 页将在您选择 **定期任务** 中的 **分类帐结算** 时使用。</span><span class="sxs-lookup"><span data-stu-id="59307-112">The advanced **Ledger settlements** page will be used when you select **Ledger settlements** in the **Periodic tasks**.</span></span> 
3. <span data-ttu-id="59307-113">您必须输入用于每个会计科目表的分类帐结算的科目列表。</span><span class="sxs-lookup"><span data-stu-id="59307-113">You must enter the list of accounts to use for ledger settlements for each chart of accounts.</span></span> <span data-ttu-id="59307-114">此列表用于筛选在 **分类帐结算** 页显示的交易记录的列表。</span><span class="sxs-lookup"><span data-stu-id="59307-114">This list is used to filter the list of transactions that appears on the **Ledger settlements** page.</span></span> <span data-ttu-id="59307-115">在 **会计科目表** 列表中，请选择会计科目表，然后选择 **新** 向列表添加新科目。</span><span class="sxs-lookup"><span data-stu-id="59307-115">In the **Chart of accounts** list, select a chart of accounts, and then select **New** to add new accounts to the list.</span></span>

## <a name="settle-transactions-by-using-the-advanced-ledger-settlements-page"></a><span data-ttu-id="59307-116">使用高级分类帐结算页结算交易记录</span><span class="sxs-lookup"><span data-stu-id="59307-116">Settle transactions by using the advanced ledger settlements page</span></span>

<span data-ttu-id="59307-117">若要结算分类帐交易，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="59307-117">To settle ledger transactions, follow these steps.</span></span>

1. <span data-ttu-id="59307-118">选择 **总帐** \> **定期任务** \> **分类帐结算**。</span><span class="sxs-lookup"><span data-stu-id="59307-118">Select **General ledger** \> **Periodic tasks** \> **Ledger settlements**.</span></span>
2. <span data-ttu-id="59307-119">设置页面顶部的筛选器：</span><span class="sxs-lookup"><span data-stu-id="59307-119">Set the filters at the top of the page:</span></span>

    - <span data-ttu-id="59307-120">选择一个日期范围或选择 **日期间隔代码** 自动填充日期范围。</span><span class="sxs-lookup"><span data-stu-id="59307-120">Select a date range, or select **Date interval code** to automatically fill in the date range.</span></span>
    - <span data-ttu-id="59307-121">根据需要更改过帐层。</span><span class="sxs-lookup"><span data-stu-id="59307-121">Change the posting layer as you require.</span></span>
    - <span data-ttu-id="59307-122">若要分别显示会计科目和维度，请选择财务维度集。</span><span class="sxs-lookup"><span data-stu-id="59307-122">To show the ledger account and dimensions separately, select a financial dimension set.</span></span>

3. <span data-ttu-id="59307-123">选择 **显示交易记录** 显示满足您设置的筛选器的所有交易记录，以及您在上一部分设置会计科目表时指定的科目列表。</span><span class="sxs-lookup"><span data-stu-id="59307-123">Select **Display transactions** to show all the transactions that match the filters that you set and the list of accounts that you specified when you set up the chart of accounts list in the previous section.</span></span> <span data-ttu-id="59307-124">如果您更改任何筛选器或维度集，则必须再次选择 **显示交易记录**。</span><span class="sxs-lookup"><span data-stu-id="59307-124">If you change any of the filters or the dimension sets, you must select **Display transactions** again.</span></span>
4. <span data-ttu-id="59307-125">选择您考虑要结算的一行或多行。</span><span class="sxs-lookup"><span data-stu-id="59307-125">Select one or more lines that you're considering for settlement.</span></span> <span data-ttu-id="59307-126">页面顶部的 **选定金额** 字段的值将按您选择的行中的总金额增加或减少。</span><span class="sxs-lookup"><span data-stu-id="59307-126">The value of the **Selected amount** field at the top of the page increases or decreases by the total amount on the lines that you selected.</span></span>
5. <span data-ttu-id="59307-127">完成选择交易记录后，请选择 **标记所选项**。</span><span class="sxs-lookup"><span data-stu-id="59307-127">After you've finished selecting transactions, select **Mark selected**.</span></span> <span data-ttu-id="59307-128">复选标记将在您选择的每个交易记录的 **已标记** 列中显示。</span><span class="sxs-lookup"><span data-stu-id="59307-128">A check mark appears in the **Marked** column for each transaction that you selected.</span></span> <span data-ttu-id="59307-129">此外，网格上方的 **标记金额** 字段的值将按您标记的行中的总金额增加或减少。</span><span class="sxs-lookup"><span data-stu-id="59307-129">Additionally, the value of the **Marked amount** field above the grid increases or decreases by the total amount on the lines that you marked.</span></span>
6. <span data-ttu-id="59307-130">在 **标记金额** 值是 **0**（零）时，请选择 **结算已标记的交易记录**。</span><span class="sxs-lookup"><span data-stu-id="59307-130">When the **Marked amount** value is **0** (zero), select **Settle marked transactions**.</span></span> <span data-ttu-id="59307-131">标记的交易记录的状态将更新为 **已结算**。</span><span class="sxs-lookup"><span data-stu-id="59307-131">The status of the marked transactions is updated to **Settled**.</span></span>

## <a name="make-transactions-easier-to-find"></a><span data-ttu-id="59307-132">让交易记录查找更加轻松</span><span class="sxs-lookup"><span data-stu-id="59307-132">Make transactions easier to find</span></span>

<span data-ttu-id="59307-133">**分类帐结算** 页包括更便于您查看结算交易记录所需的功能。</span><span class="sxs-lookup"><span data-stu-id="59307-133">The **Ledger settlements** page includes capabilities that make it easier to see the transactions that you need for settlement.</span></span>

- <span data-ttu-id="59307-134">**取消标记所选项** 按钮清除选择的所有行的 **已标记** 字段。</span><span class="sxs-lookup"><span data-stu-id="59307-134">The **Unmark selected** button clears the **Marked** field for all lines that are selected.</span></span>
- <span data-ttu-id="59307-135">**已标记** 筛选器允许您基于交易记录的 **已标记** 字段是选择还是清除来筛选交易记录。</span><span class="sxs-lookup"><span data-stu-id="59307-135">The **Marked** filter lets you filter transactions based on whether the **Marked** field for them is selected or cleared.</span></span>
- <span data-ttu-id="59307-136">**状态** 筛选器让您可以基于交易记录的状态是 **已结算** 还是 **未结算** 来筛选交易记录。</span><span class="sxs-lookup"><span data-stu-id="59307-136">The **Status** filter lets you filter transactions based on whether their status is **Settled** or **Not settled**.</span></span>
- <span data-ttu-id="59307-137">**按绝对金额排序** 按钮允许您按绝对值排序金额，以便您可以将具有相同金额的借方和贷方分组到一起。</span><span class="sxs-lookup"><span data-stu-id="59307-137">The **Sort by absolute amount** button lets you sort the amounts by absolute value, so that you can group together debits and credits that have the same amount.</span></span>

## <a name="reverse-a-settlement"></a><span data-ttu-id="59307-138">冲销结算</span><span class="sxs-lookup"><span data-stu-id="59307-138">Reverse a settlement</span></span>

<span data-ttu-id="59307-139">您可以冲销错误进行的结算。</span><span class="sxs-lookup"><span data-stu-id="59307-139">You can reverse a settlement that was made by mistake.</span></span>

1. <span data-ttu-id="59307-140">请按照“使用高级分类帐结算页结算交易记录”部分中的第 1 步到第 3 步显示您要查找的交易记录。</span><span class="sxs-lookup"><span data-stu-id="59307-140">Follow steps 1 through 3 in the "Settle transactions by using advanced ledger settlements page" section to show the transactions that you're looking for.</span></span>
2. <span data-ttu-id="59307-141">在 **状态** 筛选器中，选择 **已结算**。</span><span class="sxs-lookup"><span data-stu-id="59307-141">In the **Status** filter, select **Settled**.</span></span>
3. <span data-ttu-id="59307-142">选择您考虑要冲销的一行或多行。</span><span class="sxs-lookup"><span data-stu-id="59307-142">Select one or more lines that you're considering for reversal.</span></span> <span data-ttu-id="59307-143">页面顶部的 **选定金额** 字段的值将按您选择的行中的总金额增加或减少。</span><span class="sxs-lookup"><span data-stu-id="59307-143">The value of the **Selected amount** field at the top of the page increases or decreases by the total amount on the lines that you selected.</span></span>
4. <span data-ttu-id="59307-144">完成选择交易记录后，请选择 **标记所选项**。</span><span class="sxs-lookup"><span data-stu-id="59307-144">After you've finished selecting transactions, select **Mark selected**.</span></span> <span data-ttu-id="59307-145">复选标记将在您选择的每个交易记录的 **已标记** 列中显示。</span><span class="sxs-lookup"><span data-stu-id="59307-145">A check mark appears in the **Marked** column for each transaction that you selected.</span></span> <span data-ttu-id="59307-146">此外，页面顶部的 **标记金额** 字段的值将按您标记的行中的总金额增加或减少。</span><span class="sxs-lookup"><span data-stu-id="59307-146">Additionally, the value of the **Marked amount** field at the top of the page increases or decreases by the total amount on the lines that you marked.</span></span>
5. <span data-ttu-id="59307-147">在 **标记金额** 值是 **0**（零）时，请选择 **冲销已标记的交易记录**。</span><span class="sxs-lookup"><span data-stu-id="59307-147">When the **Marked amount** value is **0** (zero), select **Reverse marked transactions**.</span></span> <span data-ttu-id="59307-148">标记的交易记录的状态将更新为 **未结算**。</span><span class="sxs-lookup"><span data-stu-id="59307-148">The status of the marked transactions is updated to **Not settled**.</span></span>

## <a name="update-the-list-of-accounts-that-are-included-in-the-list-of-transactions"></a><span data-ttu-id="59307-149">更新交易记录列表中包括的科目列表</span><span class="sxs-lookup"><span data-stu-id="59307-149">Update the list of accounts that are included in the list of transactions</span></span>

<span data-ttu-id="59307-150">选择 **分类帐结算科目** 打开您可以编辑交易记录列表中包括的科目的对话框。</span><span class="sxs-lookup"><span data-stu-id="59307-150">Select **Ledger settlement accounts** to open a dialog box where you can edit the accounts that are included in the list of transactions.</span></span> <span data-ttu-id="59307-151">选择 **新** 向列表添加新科目。</span><span class="sxs-lookup"><span data-stu-id="59307-151">Select **New** to add new accounts to the list.</span></span> <span data-ttu-id="59307-152">此列表用于筛选在 **分类帐结算** 页显示的交易记录的列表。</span><span class="sxs-lookup"><span data-stu-id="59307-152">This list is used to filter the list of transactions that appears on the **Ledger settlements** page.</span></span>
