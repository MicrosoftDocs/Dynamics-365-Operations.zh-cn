---
title: "内部公司会计设置"
description: "本主题说明如何设置内部公司会计，以便将内部公司日记帐用于分类帐分配和财务日记帐，如日常记帐、供应商发票日记帐和付款日记帐。"
author: kweekley
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerInterCompany
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 15761
ms.assetid: 1362297b-7a51-4930-b822-2b204a2e3c37
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 9c5e73d97f6f52a417cb71dc5bfb57658765aaa1
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---

# <a name="intercompany-accounting-setup"></a><span data-ttu-id="fd572-103">内部公司会计设置</span><span class="sxs-lookup"><span data-stu-id="fd572-103">Intercompany accounting setup</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="fd572-104">本主题说明如何设置内部公司会计，以便将内部公司日记帐用于分类帐分配和财务日记帐，如日常记帐、供应商发票日记帐和付款日记帐。</span><span class="sxs-lookup"><span data-stu-id="fd572-104">This topic explains how to set up intercompany accounting so that you can use intercompany journals for ledger allocations and financial journals, such as daily journals, vendor invoice journals, and payment journals.</span></span>

<span data-ttu-id="fd572-105">内部公司日记帐可以在不同方案创建，如为日常记帐、供应商发票日记帐、分类帐分配和集中付款。</span><span class="sxs-lookup"><span data-stu-id="fd572-105">Intercompany journals can be created in various scenarios, such as for daily journals, vendor invoice journals, ledger allocations, and centralized payments.</span></span> <span data-ttu-id="fd572-106">若要启用这些方案，必须设置内部公司会计。</span><span class="sxs-lookup"><span data-stu-id="fd572-106">To enable these scenarios, you must set up intercompany accounting.</span></span>

## <a name="define-main-accounts"></a><span data-ttu-id="fd572-107">定义主科目</span><span class="sxs-lookup"><span data-stu-id="fd572-107">Define main accounts</span></span>
<span data-ttu-id="fd572-108">首先，您必须创建内部公司主科目以用于“应付金额”和“应收金额”会计条目。</span><span class="sxs-lookup"><span data-stu-id="fd572-108">First, you must create the intercompany main accounts to use for the Due to and Due from accounting entries.</span></span> <span data-ttu-id="fd572-109">最好为每个公司使用唯一主科目，以便简化内部公司会计条目的对帐和清除。</span><span class="sxs-lookup"><span data-stu-id="fd572-109">It's a good idea to use unique main accounts for each company, to simplify the reconciliation and elimination of intercompany accounting entries.</span></span> <span data-ttu-id="fd572-110">如果您使用贸易伙伴或相似维度确定内部公司当事方，您可以定义此维度为在内部公司会计中定义的主科目的固定维度。</span><span class="sxs-lookup"><span data-stu-id="fd572-110">If you're using a trading partner or counterpart dimension to identify the intercompany party, you can define this dimension as a fixed dimension on the main account that is defined in Intercompany accounting.</span></span> <span data-ttu-id="fd572-111">在您设置主科目时，应将**主科目**页上的**主科目类型**字段设置为**资产负债表**。</span><span class="sxs-lookup"><span data-stu-id="fd572-111">When you set up the main accounts, you should set the **Main account type** field to **Balance sheet** on the **Main accounts** page.</span></span>

## <a name="define-journal-names"></a><span data-ttu-id="fd572-112">定义日记帐名称</span><span class="sxs-lookup"><span data-stu-id="fd572-112">Define journal names</span></span>
<span data-ttu-id="fd572-113">其次，必须定义日记帐名称。</span><span class="sxs-lookup"><span data-stu-id="fd572-113">Next, you must define a journal name.</span></span> <span data-ttu-id="fd572-114">将**日记帐名称**页上的**日记帐类型**字段设置为**日常**。</span><span class="sxs-lookup"><span data-stu-id="fd572-114">Set the **Journal type** field to **Daily** on the **Journal names** page.</span></span> <span data-ttu-id="fd572-115">最好为进行内部公司会计使用特定的日记帐名称。</span><span class="sxs-lookup"><span data-stu-id="fd572-115">It's a good idea to use a specific journal name for intercompany accounting.</span></span>

## <a name="define-intercompany-accounting-setup"></a><span data-ttu-id="fd572-116">定义内部公司会计设置</span><span class="sxs-lookup"><span data-stu-id="fd572-116">Define intercompany accounting setup</span></span>
<span data-ttu-id="fd572-117">**内部公司会计**页用于创建可彼此交易的法人对。</span><span class="sxs-lookup"><span data-stu-id="fd572-117">The **Intercompany accounting** page is used to create the pairs of legal entities that can transact with each other.</span></span> <span data-ttu-id="fd572-118">内部公司会计设置是共享的，因此可从所有法人内查看此设置。</span><span class="sxs-lookup"><span data-stu-id="fd572-118">The Intercompany accounting setup is shared, so the setup is visible from within all legal entities.</span></span> <span data-ttu-id="fd572-119">在创建新的法人对时，请确保您知道哪个法人定义为源公司，哪个定义为目标公司。</span><span class="sxs-lookup"><span data-stu-id="fd572-119">When creating a new legal entity pair, ensure that you are aware of which legal entity is defined as the originating company versus the destination company.</span></span> <span data-ttu-id="fd572-120">在输入内部公司交易记录时，该交易记录确定哪个法人发起或创建了该交易记录。</span><span class="sxs-lookup"><span data-stu-id="fd572-120">When entering intercompany transactions, the transaction determines which legal entity is initiating or originating the transaction.</span></span> <span data-ttu-id="fd572-121">例如，内部公司会计是为 USMF（发起方）和 USSI（目标方）设置的。</span><span class="sxs-lookup"><span data-stu-id="fd572-121">For example, the intercompany accounting is setup for USMF (originating) and USSI (destination).</span></span> <span data-ttu-id="fd572-122">如果用户在 USSI 中处于活动状态，并输入了与 USMF 之间的内部公司交易记录，此交易记录将不过帐，因为内部公司会计是仅为充当发起方的 USMF 定义的。</span><span class="sxs-lookup"><span data-stu-id="fd572-122">If a user is active in USSI and enters an intercompany transaction with USMF, the transaction will not post because the intercompany accounting is only defined for USMF being the originator.</span></span> <span data-ttu-id="fd572-123">如果两个公司都可以发起交易记录，您需要为互惠设置再创建一个法人对。</span><span class="sxs-lookup"><span data-stu-id="fd572-123">If either company can originate a transaction, you will need to create a second legal entity pair for the reciprocal setup.</span></span> 

<span data-ttu-id="fd572-124">请为源和目标法人选择**借方科目(应收金额)**和**贷方科目(应付金额)**。</span><span class="sxs-lookup"><span data-stu-id="fd572-124">Select the **Debit account (Due from)** and **Credit account (Due to)** for both the originating and destination legal entity.</span></span> <span data-ttu-id="fd572-125">定义在目标公司中创建交易记录时使用哪个**日记帐名称**。</span><span class="sxs-lookup"><span data-stu-id="fd572-125">Define which **Journal name** will be used when the transaction is created in the destination company.</span></span> <span data-ttu-id="fd572-126">源公司的日记帐已知，因为是用户在创建内部公司交易记录时选择的。</span><span class="sxs-lookup"><span data-stu-id="fd572-126">The journal for the originating company is already known because it's selected by the user when creating the intercompany transaction.</span></span> 

<span data-ttu-id="fd572-127">最后，选择哪个法人将接收支持科目的会计，如集中付款的现金折扣或已有损益。</span><span class="sxs-lookup"><span data-stu-id="fd572-127">Finally, select which legal entity will receive the accounting for supporting amounts, such as cash discount or realized gains/losses for centralized payments.</span></span> 

<span data-ttu-id="fd572-128">可以通过在创建法人对后使用**创建互惠关系**按钮，在**内部公司会计**页中轻松设置互惠关系。</span><span class="sxs-lookup"><span data-stu-id="fd572-128">A reciprocal relationship can easily be set up on the **Intercompany accounting** page by using the **Create reciprocal relationship** button after the first legal entity pair is created.</span></span> <span data-ttu-id="fd572-129">创建互惠对后，将把目标公司的信息复制到源公司，反之亦然。</span><span class="sxs-lookup"><span data-stu-id="fd572-129">When the reciprocal pair is created, the information for the destination company is copied to the originating company and vice versa.</span></span> <span data-ttu-id="fd572-130">将保留为目标公司定义的日记帐。</span><span class="sxs-lookup"><span data-stu-id="fd572-130">The journal defined for the destination company will remain.</span></span> <span data-ttu-id="fd572-131">大多数组织为自己的日记帐名称使用相同的命名约定，因此日记帐名称相同。</span><span class="sxs-lookup"><span data-stu-id="fd572-131">Most organizations use the same naming convention for their journal names, so that the journal name is the same.</span></span> <span data-ttu-id="fd572-132">如果日记帐名称不同，将在字段中显示警告，通知您日记帐不存在，并且可以选择其他日记帐。</span><span class="sxs-lookup"><span data-stu-id="fd572-132">If the journal name is different, a warning will appear on the field to notify you that the journal doesn't exist and a different journal can be selected.</span></span>




