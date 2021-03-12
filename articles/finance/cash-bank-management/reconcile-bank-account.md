---
title: 银行帐户对帐
description: 本主题介绍如何对银行帐户对帐。
author: panolte
manager: AnnBe
ms.date: 07/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: panolte
ms.search.validFrom:
- month/year of release that feature was introduced in
- in format yyyy-mm-dd
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 1abc86aa5c3863eba34f726b543792408a542383
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4976358"
---
# <a name="reconcile-a-bank-account"></a><span data-ttu-id="294e4-103">银行帐户对帐</span><span class="sxs-lookup"><span data-stu-id="294e4-103">Reconcile a bank account</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="294e4-104">当您收到银行对帐单时，应定期对帐法人银行交易记录与银行对帐单的交易记录。</span><span class="sxs-lookup"><span data-stu-id="294e4-104">When you receive a bank statement, you should periodically reconcile legal entity bank transactions with the transactions on the bank statement.</span></span>

<span data-ttu-id="294e4-105">如果在某一银行帐户对帐单上列出的任何支票或存款单付款当前具有状态 **待定取消**，您就不能将该对帐单与某一银行帐户进行对帐。</span><span class="sxs-lookup"><span data-stu-id="294e4-105">You cannot reconcile a bank statement with a bank account if any of the checks or deposit slip payments that are listed on the statement currently have a status of **Pending cancellation**.</span></span> <span data-ttu-id="294e4-106">在审核人过帐或拒绝某一支票冲销或存款单付款取消后，该状态将不再为 **待定取消**，并且您可以对该银行帐户进行对帐。</span><span class="sxs-lookup"><span data-stu-id="294e4-106">After a reviewer posts or rejects a check reversal or deposit slip payment cancellation, the status is no longer **Pending cancellation**, and you can reconcile the bank account.</span></span>

1.  <span data-ttu-id="294e4-107">转到 **现金和银行管理** \> **银行帐户** \> **银行帐户**。</span><span class="sxs-lookup"><span data-stu-id="294e4-107">Go to **Cash and bank management** \> **Bank Accounts** \> **Bank accounts**.</span></span> <span data-ttu-id="294e4-108">选择要使用银行对帐单对帐的用户帐户，然后选择 **对帐** > **帐户对帐**。</span><span class="sxs-lookup"><span data-stu-id="294e4-108">Select the bank account to reconcile with the bank statement and select **Reconcile** > **Account reconciliation**.</span></span>

2.  <span data-ttu-id="294e4-109">在 **银行对帐单日期** 和 **银行对帐单** 字段中输入信息。</span><span class="sxs-lookup"><span data-stu-id="294e4-109">Enter information in the **Bank statement date** and **Bank statement** fields.</span></span> <span data-ttu-id="294e4-110">在 **期末余额** 字段中，在出现在银行对帐单后，您可以输入该银行帐户的余额。</span><span class="sxs-lookup"><span data-stu-id="294e4-110">In the **Ending balance** field, you can enter the balance of the bank account as it appears on the bank statement.</span></span>

3.  <span data-ttu-id="294e4-111">选择 **交易** 打开 **帐户对帐** 页。</span><span class="sxs-lookup"><span data-stu-id="294e4-111">Select **Transactions** to open the **Account reconciliation** page.</span></span>

4.  <span data-ttu-id="294e4-112">对于在银行帐户对帐单中包括的每个交易记录，选择 **已结** 复选框，前提是 Dynamics 365 Finance 中的金额与银行声明上的金额对应。</span><span class="sxs-lookup"><span data-stu-id="294e4-112">For each transaction that is included on the bank statement, select the **Cleared** check box if the amount in Dynamics 365 Finance corresponds to the amount on the bank statement.</span></span> <span data-ttu-id="294e4-113">您可以在 **银行交易记录类型** 字段中输入或修改该值。</span><span class="sxs-lookup"><span data-stu-id="294e4-113">You can also enter or modify the value in the **Bank transaction type** field.</span></span> <span data-ttu-id="294e4-114">这对于您的银行交易记录统计和某些报表十分重要。</span><span class="sxs-lookup"><span data-stu-id="294e4-114">This field value is important for bank transaction statistics and for some reports.</span></span>
    

    > [!NOTE]
    > <P><span data-ttu-id="294e4-115">对于未在银行帐户对帐单上的交易记录，不选中<STRONG>已结</STRONG>复选框。</span><span class="sxs-lookup"><span data-stu-id="294e4-115">Do not select the <STRONG>Cleared</STRONG> check box for transactions that are not on the bank statement.</span></span> <span data-ttu-id="294e4-116">这些交易记录继续出现在此页中，直到它们与将来的银行帐户对帐单对帐。</span><span class="sxs-lookup"><span data-stu-id="294e4-116">These transactions will continue to be displayed in on this page until they are reconciled with a future bank statement.</span></span></P>
    > <P><span data-ttu-id="294e4-117">如果该交易记录具有状态<STRONG>待定取消</STRONG>，则<STRONG>已结</STRONG>复选框不可用。</span><span class="sxs-lookup"><span data-stu-id="294e4-117">The <STRONG>Cleared</STRONG> check box is not available if the transaction has a status of <STRONG>Pending cancellation</STRONG>.</span></span> <span data-ttu-id="294e4-118">如果 Finance 设置为系统在过帐冲销或取消之前要求将其送交复核，交易记录就可能具有此状态。</span><span class="sxs-lookup"><span data-stu-id="294e4-118">Transactions might have this status if Finance is set up to require that reversals or cancellations be sent to review before they are posted.</span></span> <span data-ttu-id="294e4-119">在审核人过帐或拒绝该冲销或取消后，该状态将不再为<STRONG>待定取消</STRONG>，并且您可以对该帐户进行对帐。</span><span class="sxs-lookup"><span data-stu-id="294e4-119">After a reviewer posts or rejects the reversal or cancellation, the status is no longer <STRONG>Pending cancellation</STRONG>, and you can reconcile the bank account with the bank statement.</span></span></P>

    
    <span data-ttu-id="294e4-120">若要为所有在银行对帐单上显示的支票间隔选中 **已结** 复选框，请选择 **标记支票间隔**，然后指示该间隔。</span><span class="sxs-lookup"><span data-stu-id="294e4-120">To select the **Cleared** check box for an interval of checks that all are displayed on the bank statement, select **Mark check interval**, and then indicate the interval.</span></span>

5.  <span data-ttu-id="294e4-121">如果银行帐户交易记录金额与银行对帐单上的交易记录金额不对应，请在 **冲销金额** 字段中输入冲销金额。</span><span class="sxs-lookup"><span data-stu-id="294e4-121">If the amount for a bank account transaction does not correspond to the amount for the transaction on the bank statement, enter the amount of the correction in the **Correction amount** field.</span></span>
    

    > [!NOTE]
    > <P><span data-ttu-id="294e4-122">如果要更正的交易记录的会计期间已关闭，则<STRONG>冲销金额</STRONG>字段将无法使用。</span><span class="sxs-lookup"><span data-stu-id="294e4-122">If the fiscal period of the transaction to be corrected is closed, the <STRONG>Correction amount</STRONG> field cannot be used.</span></span> <span data-ttu-id="294e4-123">相反，请为具有交易记录日期位于此更正的一个启用会计期间的一行。</span><span class="sxs-lookup"><span data-stu-id="294e4-123">Instead, create a line that has a transaction date that is in an open fiscal period for the correction.</span></span> <span data-ttu-id="294e4-124">在此情况下，您必须添加在原始交易记录的财务维度，并且冲销主科目。</span><span class="sxs-lookup"><span data-stu-id="294e4-124">In this case, you must add the financial dimensions that were used on the original transaction, and also the offset main account.</span></span></P>



6.  <span data-ttu-id="294e4-125">为位于银行帐户对帐单上、但在 Finance 中未记录的分录（例如费用和利息）创建交易记录。</span><span class="sxs-lookup"><span data-stu-id="294e4-125">Create transactions for entries, such as fees and interest, that are on the bank statement but that are not recorded in Finance.</span></span> <span data-ttu-id="294e4-126">输入 **银行交易记录类型** 和相应的财务维度。</span><span class="sxs-lookup"><span data-stu-id="294e4-126">Enter the **Bank transaction type** and appropriate financial dimensions.</span></span>

7.  <span data-ttu-id="294e4-127">随着银行帐户对帐单上的交易记录标记为 **已结**，**未对帐** 字段中的金额（随着您进行更改将连续重新计算）将接近零。</span><span class="sxs-lookup"><span data-stu-id="294e4-127">As the transactions on the bank statement are marked as **Cleared**, the amount in the **Unreconciled** field, which is recalculated continuously as you make changes, approaches zero.</span></span> <span data-ttu-id="294e4-128">在其达到零时，选择 **对帐帐户** 过帐该对帐和交易记录以及您已创建的更正。</span><span class="sxs-lookup"><span data-stu-id="294e4-128">When it reaches zero, select **Reconcile account** to post the reconciliation, and the transactions and corrections that you have created.</span></span>
    
    <span data-ttu-id="294e4-129">在过帐对帐后，将无法进一步对已包括的交易记录进行修正或更正，并且它们不出现在任何将来的帐户对帐中。</span><span class="sxs-lookup"><span data-stu-id="294e4-129">After the reconciliation is posted, the transactions that have been included cannot be modified or corrected, and they are not displayed for future account reconciliation.</span></span>

8.  <span data-ttu-id="294e4-130">若要查看尚未对帐的银行交易记录，请使用 **未对帐的银行交易记录** 报表。</span><span class="sxs-lookup"><span data-stu-id="294e4-130">To view bank transactions that have not yet been reconciled, use the **Unreconciled bank transactions** report.</span></span> <span data-ttu-id="294e4-131">若要查看某一银行帐户的银行对帐单，请使用 **银行对帐单** 报表。</span><span class="sxs-lookup"><span data-stu-id="294e4-131">To view the bank statement for a bank account, use the **Bank statement** report.</span></span>

## <a name="cancel-bank-statement-reconciliation"></a><span data-ttu-id="294e4-132">取消银行对帐单对帐</span><span class="sxs-lookup"><span data-stu-id="294e4-132">Cancel bank statement reconciliation</span></span> 

<span data-ttu-id="294e4-133">可通过取消银行对帐单对帐功能取消银行对帐单对帐。</span><span class="sxs-lookup"><span data-stu-id="294e4-133">The Cancel bank statement reconciliation functionality enables you to cancel bank statement reconciliation.</span></span> <span data-ttu-id="294e4-134">若要使用此功能，请启用 **功能管理** 工作区中的 **取消银行对帐单对帐** 功能。</span><span class="sxs-lookup"><span data-stu-id="294e4-134">To use this feature, enable the **Cancel bank statement reconciliation** feature in the **Feature management** workspace.</span></span> <span data-ttu-id="294e4-135">还需要启用 **允许编辑银行对帐单** 参数。</span><span class="sxs-lookup"><span data-stu-id="294e4-135">You also need to enable the **Allow bank statement edit** parameter.</span></span> <span data-ttu-id="294e4-136">方法是，转到 **现金和银行管理 > 设置 > 现金和银行管理参数 > 银行对帐**。</span><span class="sxs-lookup"><span data-stu-id="294e4-136">To do this, go to **Cash and bank management > Setup > Cash and bank management parameters > Bank reconciliation**.</span></span>
 
<span data-ttu-id="294e4-137">银行对帐单对帐只能按照其输入时间顺序取消。</span><span class="sxs-lookup"><span data-stu-id="294e4-137">Bank statement reconciliations can only be canceled in the chronological order in which they were entered.</span></span> <span data-ttu-id="294e4-138">取消银行对帐单对帐时，将冲销新交易记录和冲销，并将其他所有交易记录标记为未对帐。</span><span class="sxs-lookup"><span data-stu-id="294e4-138">When a bank statement reconciliation is canceled, new transactions and corrections will be reversed and all other transactions will be marked as un-reconciled.</span></span>
 
<span data-ttu-id="294e4-139">若要取消银行对帐单对帐，请选择银行对帐单，然后选择 **银行对帐单 > 取消银行对帐**。</span><span class="sxs-lookup"><span data-stu-id="294e4-139">To cancel bank statement reconciliation, select the bank statement and select **Bank statement > Cancel bank reconciliation**.</span></span> <span data-ttu-id="294e4-140">在 **取消银行对帐** 页上，提供 **原因代码**、**原因注释** 和 **取消日期**。</span><span class="sxs-lookup"><span data-stu-id="294e4-140">On the **Cancel bank reconciliation** page, provide the **Reason code**, **Reason comment**, and **Cancellation date**.</span></span> <span data-ttu-id="294e4-141">选择 **确定** 开始取消。</span><span class="sxs-lookup"><span data-stu-id="294e4-141">Select **OK** to begin cancellation.</span></span> <span data-ttu-id="294e4-142">请注意，银行对帐单取消日期必须在银行对帐单日期当天或之后。</span><span class="sxs-lookup"><span data-stu-id="294e4-142">Note, the bank statement cancellation date must be on or after the bank statement date.</span></span> <span data-ttu-id="294e4-143">取消了银行对帐单对帐之后，将使用提供的 **取消日期** 更新银行对帐单的 **取消日期** 字段。</span><span class="sxs-lookup"><span data-stu-id="294e4-143">After the bank statement reconciliation has canceled, the **Cancellation date** field for the bank statement will be updated with the **Cancellation date** provided.</span></span> <span data-ttu-id="294e4-144">选择 **交易记录** 按钮查看取消了其对帐的交易记录。</span><span class="sxs-lookup"><span data-stu-id="294e4-144">Select the **Transactions** button to view the transactions for which the reconciliation was canceled.</span></span>
