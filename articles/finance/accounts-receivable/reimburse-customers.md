---
title: 补偿客户
description: 本文说明如何为一组客户创建偿还交易记录。 如果某一客户具有贷方余额，您可以为该客户偿还剩余的金额。
author: JodiChristiansen
manager: AnnBe
ms.date: 09/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTransCustPaym, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: roschlom
ms.custom: 14191
ms.assetid: 53533ee3-470e-458a-ac8b-3815aa4cb502
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ca087b5a39432eec6b2711cc4c4decf23932b611
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5251111"
---
# <a name="reimburse-customers"></a><span data-ttu-id="e48e9-104">补偿客户</span><span class="sxs-lookup"><span data-stu-id="e48e9-104">Reimburse customers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e48e9-105">本文说明如何为一组客户创建偿还交易记录。</span><span class="sxs-lookup"><span data-stu-id="e48e9-105">This article explains how to create reimbursement transactions for a group of customers.</span></span> <span data-ttu-id="e48e9-106">如果某一客户具有贷方余额，您可以为该客户偿还剩余的金额。</span><span class="sxs-lookup"><span data-stu-id="e48e9-106">If a customer has a credit balance, you can reimburse the customer for the amount of the balance.</span></span> 

<span data-ttu-id="e48e9-107">下表显示必须先就绪然后才能开始的先决条件。</span><span class="sxs-lookup"><span data-stu-id="e48e9-107">The following table shows the prerequisites that must be in place before you start.</span></span>

| <span data-ttu-id="e48e9-108">先决条件</span><span class="sxs-lookup"><span data-stu-id="e48e9-108">Prerequisite</span></span>                                                            | <span data-ttu-id="e48e9-109">描述</span><span class="sxs-lookup"><span data-stu-id="e48e9-109">Description</span></span> |
|-------------------------------------------------------------------------|-------------|
| <span data-ttu-id="e48e9-110">为法人指定最低偿还金额。</span><span class="sxs-lookup"><span data-stu-id="e48e9-110">Specify the minimum reimbursement amount for the legal entity.</span></span>          | <span data-ttu-id="e48e9-111">在 **应收帐款参数** 页上，在 **常规** 区域中，在 **最低偿还额** 字段中，输入可以偿还客户超额支付的最小金额。</span><span class="sxs-lookup"><span data-stu-id="e48e9-111">On the **Accounts receivable parameters** page, in the **General** area, in the **Minimum reimbursement** field, enter the minimum amount that can be reimbursed for customer overpayments.</span></span> |
| <span data-ttu-id="e48e9-112">可选：为每一个可获得偿还的客户添加一个供应商帐户。</span><span class="sxs-lookup"><span data-stu-id="e48e9-112">Optional: Add a vendor account to each customer that can be reimbursed.</span></span> | <span data-ttu-id="e48e9-113">在 **客户** 页，在 **杂项详细信息** 快速选项卡上，在 **供应商帐户** 字段中，选择客户的供应商帐户。</span><span class="sxs-lookup"><span data-stu-id="e48e9-113">On the **Customers** page, on the **Miscellaneous details** FastTab, in the **Vendor account** field, select the vendor account for the customer.</span></span> |

<span data-ttu-id="e48e9-114">当您创建偿还交易记录时，将针对贷方余额创建供应商发票。</span><span class="sxs-lookup"><span data-stu-id="e48e9-114">When you create reimbursement transactions, a vendor invoice is created for the amount of the credit balance.</span></span> <span data-ttu-id="e48e9-115">偿还流程移除了客户帐户的贷方余额，并创建对应客户的供应商帐户结欠金额。</span><span class="sxs-lookup"><span data-stu-id="e48e9-115">The reimbursement process removes the credit balance for the customer account and creates a balance due for the vendor account that corresponds to the customer.</span></span>

1. <span data-ttu-id="e48e9-116">在应收帐款中，运行 **偿还** 流程（**应收帐款 \> 定期任务 \> 偿还**）。</span><span class="sxs-lookup"><span data-stu-id="e48e9-116">In Accounts receivable, run the **Reimbursement** process (**Accounts receivable \> Periodic tasks \> Reimbursement**).</span></span>
2. <span data-ttu-id="e48e9-117">要对所有交易记录进行分组，而不考虑分类帐，请将 **汇总客户** 选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="e48e9-117">To group all transactions, regardless of ledger dimensions, set the **Summarize customer** option to **Yes**.</span></span> <span data-ttu-id="e48e9-118">要仅对具有类似分类帐维度的交易记录进行分组，请将此选项设置为 **否**。</span><span class="sxs-lookup"><span data-stu-id="e48e9-118">To group only transactions that have similar ledger dimensions, set the option to **No**.</span></span>
3. <span data-ttu-id="e48e9-119">选择 **包括具有未结借方交易记录的客户** 以选择具有未结算借方金额的客户。</span><span class="sxs-lookup"><span data-stu-id="e48e9-119">Select **Include customers with outstanding debit transactions** to select customers who have unsettled debit amounts.</span></span>
4. <span data-ttu-id="e48e9-120">要偿还特定的客户帐户，请在 **要包括的记录** 快速选项卡上选择 **筛选**，然后在查询中指定客户帐户。</span><span class="sxs-lookup"><span data-stu-id="e48e9-120">To reimburse specific customer accounts, on the **Records to include** FastTab, select **Filter**, and then specify the customer accounts in the query.</span></span>

    <span data-ttu-id="e48e9-121">贷方金额将转移到客户的供应商帐户，并且按一般的付款进行处理。</span><span class="sxs-lookup"><span data-stu-id="e48e9-121">The credit amounts are transferred to the vendor accounts of the customers and are processed as ordinary payments.</span></span> <span data-ttu-id="e48e9-122">如果某一客户不具有供应商帐户，则将自动为该客户创建零星供应商帐户。</span><span class="sxs-lookup"><span data-stu-id="e48e9-122">If a customer doesn't have a vendor account, a one-time vendor account is automatically created for the customer.</span></span>

5. <span data-ttu-id="e48e9-123">要查看创建的偿还交易记录，请使用 **偿还** 报表（**应收帐款 \> 查询和报表 \> 偿还报表**）。</span><span class="sxs-lookup"><span data-stu-id="e48e9-123">To view the reimbursement transactions that were created, use the **Reimbursement** report (**Accounts Receivable \> Inquiries and reports \> Reimbursement report**).</span></span>
6. <span data-ttu-id="e48e9-124">在应付帐款中，为偿还流程创建的供应商发票创建付款。</span><span class="sxs-lookup"><span data-stu-id="e48e9-124">In Accounts payable, create a payment for the vendor invoices that were created by the reimbursement process.</span></span> <span data-ttu-id="e48e9-125">有关如何向供应商付款的信息，请参阅[供应商付款概述](../accounts-payable/Vendor-payments-workspace.md)。</span><span class="sxs-lookup"><span data-stu-id="e48e9-125">For information about how to pay vendors, see [Vendor payment overview](../accounts-payable/Vendor-payments-workspace.md).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]