---
title: "结算余额"
description: "您可以通过将余额应用到会计科目来结算结算活动的剩余金额。"
author: mikefalkner
manager: aolson
ms.date: 10/16/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustOpenTrans, LedgerJournalTransCustPaym, LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2018-12-01
ms.dyn365.ops.version: 8.1.3
ms.translationtype: HT
ms.sourcegitcommit: 18eaadf417ce6d0aacf0b13b3e4f857e06031e66
ms.openlocfilehash: 408a36a7cf221463b38260bd8830b422e58ccb64
ms.contentlocale: zh-cn
ms.lasthandoff: 01/22/2019

---

# <a name="settle-remainder"></a><span data-ttu-id="5af50-103">结算余额</span><span class="sxs-lookup"><span data-stu-id="5af50-103">Settle remainder</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5af50-104">您可以通过将余额应用到会计科目或其他客户来结算结算活动的剩余金额。</span><span class="sxs-lookup"><span data-stu-id="5af50-104">You can settle the amount remaining from settlement activity by applying that amount to a ledger account or another customer.</span></span> <span data-ttu-id="5af50-105">您可以在结算输入到日记帐的金额时，或者在只结算未结交易记录时结算余额。</span><span class="sxs-lookup"><span data-stu-id="5af50-105">You can settle the remainder when you are settling amounts entered into a journal or when you are only settling open transactions.</span></span>

## <a name="setting-up-defaults"></a><span data-ttu-id="5af50-106">设置默认值</span><span class="sxs-lookup"><span data-stu-id="5af50-106">Setting up defaults</span></span> 
<span data-ttu-id="5af50-107">您必须先启用“结算余额”功能并设置默认设置，然后才能使用“结算余额”。</span><span class="sxs-lookup"><span data-stu-id="5af50-107">You must enable the Settle remainder feature and set up the default settings before you use Settle remainder</span></span>

1)  <span data-ttu-id="5af50-108">单击**应收帐款 > 参数 > 结算**或**应付帐款 > 参数 > 结算**</span><span class="sxs-lookup"><span data-stu-id="5af50-108">Click **Accounts receivable > Parameters > Settlements** or **Accounts payable > Parameters > Settlements**</span></span>
2)  <span data-ttu-id="5af50-109">选择**结算**选项卡并单击**启用结算余额**</span><span class="sxs-lookup"><span data-stu-id="5af50-109">Select the **Settlement** tab and click **Enable settle remainder**</span></span>
3)  <span data-ttu-id="5af50-110">在**默认原因代码**中，选择默认原因代码。</span><span class="sxs-lookup"><span data-stu-id="5af50-110">In **Default reason code**, select a default reason code.</span></span> <span data-ttu-id="5af50-111">必须已在**应收帐款 > 设置 > 客户勾销原因代码**或**应付帐款 > 设置 > 客户勾销原因代码**中设置原因代码。</span><span class="sxs-lookup"><span data-stu-id="5af50-111">The reason codes must have already been set up in **Accounts receivable > Setup > Customer write-off reason codes** or **Accounts payable > Setup > Customer write-off reason codes**.</span></span> <span data-ttu-id="5af50-112">**默认结算余额帐户**将默认为分配给勾销原因代码的帐户。</span><span class="sxs-lookup"><span data-stu-id="5af50-112">The **Default settle remainder account** will default to the account assigned to the write-off reason code.</span></span>
3)  <span data-ttu-id="5af50-113">根据需要更新**默认结算余额帐户**。</span><span class="sxs-lookup"><span data-stu-id="5af50-113">Update the **Default settle remainder account** as needed.</span></span>
4)  <span data-ttu-id="5af50-114">在**默认日记帐名称**中，如果您希望在仅结算未结交易记录时创建付款日记帐，请选择要使用的付款日记帐。</span><span class="sxs-lookup"><span data-stu-id="5af50-114">In the **Default journal name**, select a payment journal that will be used if you want to create a payment journal when you only settling open transactions.</span></span> <span data-ttu-id="5af50-115">如果您启用结算余额功能，您必须添加默认的日记帐名称。</span><span class="sxs-lookup"><span data-stu-id="5af50-115">If you enable the settle remainder feature, you must add a default journal name.</span></span>

## <a name="settle-remainder-from-a-journal"></a><span data-ttu-id="5af50-116">结算日记帐的余额</span><span class="sxs-lookup"><span data-stu-id="5af50-116">Settle remainder from a journal</span></span>
<span data-ttu-id="5af50-117">如果未启用**结算余额**功能，您仍可在日记帐中输入交易记录，然后对照它结算交易记录，因为您之前已经完成结算。</span><span class="sxs-lookup"><span data-stu-id="5af50-117">If you do not enable the **Settle remainder** feature, you can still enter a transaction in a journal and then settle transactions against it as you have done in the past.</span></span> <span data-ttu-id="5af50-118">在您单击**确定**按钮时，发票上的未结余额将减去此现金金额。</span><span class="sxs-lookup"><span data-stu-id="5af50-118">When you click the **OK** button, the open balance on the invoice is reduced by the cash amount.</span></span> <span data-ttu-id="5af50-119">如果现金未完全结算发票，发票将保持未结状态，包含要在以后结算的剩余金额。</span><span class="sxs-lookup"><span data-stu-id="5af50-119">If the cash does not fully settle the invoice, the invoice is left open with a remaining amount to be settled at a later time.</span></span>

<span data-ttu-id="5af50-120">在**结算余额**功能启用时，您可以将剩余金额结算到会计科目。</span><span class="sxs-lookup"><span data-stu-id="5af50-120">When the **Settle remainder** feature is enabled, you can settle the remaining amount to a ledger account.</span></span> <span data-ttu-id="5af50-121">您还可以将余额转移到其他其客户帐户（对于客户交易）或其他供应商（对于供应商交易），而不是将发票保留为未结状态。</span><span class="sxs-lookup"><span data-stu-id="5af50-121">You can also transfer the remainder to another customer account (for customer transactions) or another vendor (for vendor transactions) instead of leaving the invoices open.</span></span> 

<span data-ttu-id="5af50-122">要从**结算**页结算余额，请执行以下步骤：</span><span class="sxs-lookup"><span data-stu-id="5af50-122">To settle the remainder from the **Settlement** page, perform the following steps:</span></span>

1)  <span data-ttu-id="5af50-123">在**结算**页，标记要结算的发票或交易记录。</span><span class="sxs-lookup"><span data-stu-id="5af50-123">On the **Settlement** page, mark the invoices or transactions that you want to settle.</span></span>
2)  <span data-ttu-id="5af50-124">单击**结算余额**按钮。</span><span class="sxs-lookup"><span data-stu-id="5af50-124">Click the **Settle remainder** button.</span></span>
3)  <span data-ttu-id="5af50-125">将显示一个对话框，显示将针对会计科目结算的金额、将用于结算余额的日期、来自参数的默认原因代码，以及来自参数的默认帐户。</span><span class="sxs-lookup"><span data-stu-id="5af50-125">A dialog box will display, showing the amount that will be settled against a ledger account, the date that will be used to settle the remainder, the default reason code from the parameters, and the default account from the parameters.</span></span> 
4)  <span data-ttu-id="5af50-126">如果您希望更改默认原因，请选择一个新结算原因。</span><span class="sxs-lookup"><span data-stu-id="5af50-126">Select a new settlement reason if you want to change the default reason.</span></span> <span data-ttu-id="5af50-127">结算帐户将更改为与原因代码关联的帐户。</span><span class="sxs-lookup"><span data-stu-id="5af50-127">The settlement account will be changed to the account associated with the reason code.</span></span>
5)  <span data-ttu-id="5af50-128">如果您希望更改结算帐户，请对其进行编辑。</span><span class="sxs-lookup"><span data-stu-id="5af50-128">Edit the settlement account if you want to change it.</span></span>
6)  <span data-ttu-id="5af50-129">如果您正在结算客户交易记录，并且想要将余额转移到另一个客户，则选择**针对客户帐户的结算余额**中的客户。</span><span class="sxs-lookup"><span data-stu-id="5af50-129">If you are settling customer transactions and you want the remainder to be moved to another customer, then select a customer in the **Settle remainder against customer account**.</span></span> <span data-ttu-id="5af50-130">如果您正在结算供应商交易记录，并且想要将余额转移到另一个供应商，则选择**针对供应商帐户的结算余额**中的供应商。</span><span class="sxs-lookup"><span data-stu-id="5af50-130">If you are settling vendor transactions and you want the remainder to be moved to another vendor, then select a vendor in the **Settle remainder against vendor account**.</span></span>
6)  <span data-ttu-id="5af50-131">单击**结算余额**。</span><span class="sxs-lookup"><span data-stu-id="5af50-131">Click **Settle remainder**.</span></span>
7)  <span data-ttu-id="5af50-132">将显示**日记帐**页面。</span><span class="sxs-lookup"><span data-stu-id="5af50-132">The **Journal** page will display.</span></span> <span data-ttu-id="5af50-133">其他日记帐行将被添加到将结算余额作为此金额、将结算余额帐户作为抵销帐户的日记帐。</span><span class="sxs-lookup"><span data-stu-id="5af50-133">An additional journal line will be added to the journal with the settle remainder amount as the amount and with the settlement remainder account as the offset account.</span></span> <span data-ttu-id="5af50-134">如果您添加了某一客户或供应商，以便您可以将结算金额移动到另一客户或供应商，则其他行将被添加到日记帐以将结算金额移至该客户或供应商。</span><span class="sxs-lookup"><span data-stu-id="5af50-134">If you added a customer or vendor so that you can move the settlement amount to another customer or vendor, then an additional line will be added to the journal to move the settlement amount to that customer or vendor.</span></span>

<span data-ttu-id="5af50-135">在您过帐日记帐时，未结交易记录将完全结算。</span><span class="sxs-lookup"><span data-stu-id="5af50-135">When you post the journal, the open transaction will be fully settled.</span></span> 

## <a name="settle-remainder-when-you-are-only-settling-open-transactions"></a><span data-ttu-id="5af50-136">在您只结算未结交易记录时结算剩余</span><span class="sxs-lookup"><span data-stu-id="5af50-136">Settle remainder when you are only settling open transactions</span></span>
<span data-ttu-id="5af50-137">您也可以在不通过日记帐结算未结交易记录时结算余额。</span><span class="sxs-lookup"><span data-stu-id="5af50-137">You can also settle the remainder when you are settling open transactions without a journal.</span></span>

<span data-ttu-id="5af50-138">要结算余额，请执行以下步骤：</span><span class="sxs-lookup"><span data-stu-id="5af50-138">To settle the remainder, perform the following steps:</span></span>

1)  <span data-ttu-id="5af50-139">在**结算**页，标记要结算的发票或交易记录</span><span class="sxs-lookup"><span data-stu-id="5af50-139">On the **Settlement** page, mark the invoices or transactions that you want to settle</span></span>
2)  <span data-ttu-id="5af50-140">单击**结算余额**</span><span class="sxs-lookup"><span data-stu-id="5af50-140">Click on **Settle remainder**</span></span>
3)  <span data-ttu-id="5af50-141">将显示一个对话框，显示将针对会计科目结算的金额、将用于结算余额的日期、来自参数的默认原因代码，以及来自参数的默认帐户。</span><span class="sxs-lookup"><span data-stu-id="5af50-141">A dialog box will display, showinh the amount that will be settled against a ledger account, the date that will be used to settle the remainder, the default reason code from the parameters, and the default account from the parameters.</span></span> 
4)  <span data-ttu-id="5af50-142">如果您希望更改默认原因，请选择一个新结算原因。</span><span class="sxs-lookup"><span data-stu-id="5af50-142">Select a new settlement reason if you want to change the default reason.</span></span> <span data-ttu-id="5af50-143">结算帐户将更改为与原因代码关联的帐户。</span><span class="sxs-lookup"><span data-stu-id="5af50-143">The settlement account will be changed to the account associated with the reason code.</span></span>
5)  <span data-ttu-id="5af50-144">如果您希望更改**结算帐户**，请对其进行编辑。</span><span class="sxs-lookup"><span data-stu-id="5af50-144">Edit the **settlement account** if you want to change it.</span></span>
6)  <span data-ttu-id="5af50-145">如果您正在结算客户交易记录，并且想要将余额转移到另一个客户，则选择**针对客户帐户的结算余额**中的客户。</span><span class="sxs-lookup"><span data-stu-id="5af50-145">If you are settling customer transactions and you want the remainder to be moved to another customer, then select a customer in the **Settle remainder against customer account**.</span></span> <span data-ttu-id="5af50-146">如果您正在结算供应商交易记录，并且想要将余额转移到另一个供应商，则选择**针对供应商帐户的结算余额**中的供应商</span><span class="sxs-lookup"><span data-stu-id="5af50-146">If you are settling vendor transactions and you want the remainder to be moved to another vendor, then select a vendor in the **Settle remainder against vendor account**</span></span>
7)  <span data-ttu-id="5af50-147">您也可以选择创建包含结算余额的付款日记帐，或只是过帐结算余额，而不通过日记帐。</span><span class="sxs-lookup"><span data-stu-id="5af50-147">You can also choose to create a payment journal with the settlement remainder or just post it without a journal.</span></span> <span data-ttu-id="5af50-148">为**在日记帐中编辑**选择**是**来创建付款日记帐。</span><span class="sxs-lookup"><span data-stu-id="5af50-148">Select **Yes** for **Edit in journal** to create a payment journal.</span></span> <span data-ttu-id="5af50-149">您可以编辑您创建的付款日记帐。</span><span class="sxs-lookup"><span data-stu-id="5af50-149">You will be able to edit the payment journal that you create.</span></span>
8)  <span data-ttu-id="5af50-150">单击**结算余额**。</span><span class="sxs-lookup"><span data-stu-id="5af50-150">Click **Settle remainder**.</span></span> <span data-ttu-id="5af50-151">如果您选择创建日记帐，按钮将更改为**创建日记帐**。</span><span class="sxs-lookup"><span data-stu-id="5af50-151">If you chose to create a journal, the button will change to **Create journal**.</span></span> <span data-ttu-id="5af50-152">单击**创建日记帐**。</span><span class="sxs-lookup"><span data-stu-id="5af50-152">Click **Create journal** instead.</span></span>
9)  <span data-ttu-id="5af50-153">如果您创建了付款日记帐，日记帐页面将在单击**结算余额**后打开。</span><span class="sxs-lookup"><span data-stu-id="5af50-153">If you created a payment journal, the journal page will open after you click **Settle remainder**.</span></span> <span data-ttu-id="5af50-154">日记帐行将被添加到将结算余额作为此金额、将结算余额帐户作为抵销帐户的日记帐。</span><span class="sxs-lookup"><span data-stu-id="5af50-154">A journal line will be added to the journal with the settle remainder amount as the amount and with the settlement remainder account as the offset account.</span></span> <span data-ttu-id="5af50-155">如果您添加了某一客户或供应商，以便您可以将结算金额移动到另一客户或供应商，则其他行将被添加到日记帐以将结算金额移至该客户或供应商。</span><span class="sxs-lookup"><span data-stu-id="5af50-155">If you added a customer or vendor so that you can move the settlement amount to another customer or vendor, then an additional line will be added to the journal to move the settlement amount to that customer or vendor.</span></span>
