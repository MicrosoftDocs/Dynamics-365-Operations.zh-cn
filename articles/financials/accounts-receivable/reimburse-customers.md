---
title: "补偿客户"
description: "本文说明如何为一组客户创建偿还交易记录。 如果某一客户具有贷方余额，您可以为该客户偿还剩余的金额。"
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalTransCustPaym, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 14191
ms.assetid: 53533ee3-470e-458a-ac8b-3815aa4cb502
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 2d1a05ffe39c208748a316bd711d9442f1ed875a
ms.contentlocale: zh-cn
ms.lasthandoff: 04/13/2018

---

# <a name="reimburse-customers"></a><span data-ttu-id="2ebfc-104">补偿客户</span><span class="sxs-lookup"><span data-stu-id="2ebfc-104">Reimburse customers</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="2ebfc-105">本文说明如何为一组客户创建偿还交易记录。</span><span class="sxs-lookup"><span data-stu-id="2ebfc-105">This article explains how to create reimbursement transactions for a group of customers.</span></span> <span data-ttu-id="2ebfc-106">如果某一客户具有贷方余额，您可以为该客户偿还剩余的金额。</span><span class="sxs-lookup"><span data-stu-id="2ebfc-106">If a customer has a credit balance, you can reimburse the customer for the amount of the balance.</span></span> 

<span data-ttu-id="2ebfc-107">下表显示必须先就绪然后才能开始的先决条件。</span><span class="sxs-lookup"><span data-stu-id="2ebfc-107">The following table shows the prerequisites that must be in place before you start.</span></span>

| <span data-ttu-id="2ebfc-108">先决条件</span><span class="sxs-lookup"><span data-stu-id="2ebfc-108">Prerequisite</span></span>                                                            | <span data-ttu-id="2ebfc-109">描述</span><span class="sxs-lookup"><span data-stu-id="2ebfc-109">Description</span></span>                                                                                                                                                                                 |
|-------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ebfc-110">为法人指定最低偿还金额。</span><span class="sxs-lookup"><span data-stu-id="2ebfc-110">Specify the minimum reimbursement amount for the legal entity.</span></span>          | <span data-ttu-id="2ebfc-111">在**应收账款参数**页上，在**常规**区域中，在 **最低偿还额**字段中，输入可以偿还客户超额支付的最小金额。</span><span class="sxs-lookup"><span data-stu-id="2ebfc-111">On the **Accounts receivable parameters** page, in the **General** area, in the **Minimum reimbursement** field, enter the minimum amount that can be reimbursed for customer overpayments.</span></span> |
| <span data-ttu-id="2ebfc-112">可选：为每一个可获得偿还的客户添加一个供应商帐户。</span><span class="sxs-lookup"><span data-stu-id="2ebfc-112">Optional: Add a vendor account to each customer that can be reimbursed.</span></span> | <span data-ttu-id="2ebfc-113">在**客户**页，在**杂项详细信息**快速选项卡上，在**供应商帐户**字段中，选择客户的供应商帐户。</span><span class="sxs-lookup"><span data-stu-id="2ebfc-113">On the **Customers** page, on the **Miscellaneous details** FastTab, in the **Vendor account** field, select the vendor account for the customer.</span></span>                                           |

<span data-ttu-id="2ebfc-114">当您创建偿还交易记录时，将针对贷方余额创建供应商发票。</span><span class="sxs-lookup"><span data-stu-id="2ebfc-114">When you create reimbursement transactions, a vendor invoice is created for the amount of the credit balance.</span></span> <span data-ttu-id="2ebfc-115">偿还流程移除了客户帐户的贷方余额，并创建对应客户的供应商帐户结欠金额。</span><span class="sxs-lookup"><span data-stu-id="2ebfc-115">The reimbursement process removes the credit balance for the customer account and creates a balance due for the vendor account that corresponds to the customer.</span></span>

1.  <span data-ttu-id="2ebfc-116">在“应收账款”中，请运行**偿还**流程。</span><span class="sxs-lookup"><span data-stu-id="2ebfc-116">In Accounts receivable, run the **Reimbursement** process.</span></span>
2.  <span data-ttu-id="2ebfc-117">按以下步骤之一：</span><span class="sxs-lookup"><span data-stu-id="2ebfc-117">Follow one of these steps:</span></span>
    -   <span data-ttu-id="2ebfc-118">若要偿还特定的客户帐户，请单击**选择**，然后在查询中指定客户帐户。</span><span class="sxs-lookup"><span data-stu-id="2ebfc-118">To reimburse specific customer accounts, click **Select**, and specify the customer accounts in the query.</span></span>
    -   <span data-ttu-id="2ebfc-119">若要偿还所有客户帐户，请单击“**确定**”。</span><span class="sxs-lookup"><span data-stu-id="2ebfc-119">To reimburse all customer accounts, click **OK**.</span></span>

    <span data-ttu-id="2ebfc-120">贷方金额将转移到客户的供应商帐户，并且按一般的付款进行处理。</span><span class="sxs-lookup"><span data-stu-id="2ebfc-120">The credit amounts are transferred to the vendor accounts of the customers and are processed as ordinary payments.</span></span> <span data-ttu-id="2ebfc-121">如果某一客户不具有供应商帐户，则将自动为该客户创建零星供应商帐户。</span><span class="sxs-lookup"><span data-stu-id="2ebfc-121">If a customer doesn't have a vendor account, a one-time vendor account is automatically created for the customer.</span></span>
3.  <span data-ttu-id="2ebfc-122">若要查看创建的偿还交易记录，使用**偿还**页。</span><span class="sxs-lookup"><span data-stu-id="2ebfc-122">To view the reimbursement transactions that were created, use the **Reimbursement** page.</span></span>
4.  <span data-ttu-id="2ebfc-123">在应付账款中，为偿还流程创建的供应商发票创建付款。</span><span class="sxs-lookup"><span data-stu-id="2ebfc-123">In Accounts payable, create a payment for the vendor invoices that were created by the reimbursement process.</span></span>





