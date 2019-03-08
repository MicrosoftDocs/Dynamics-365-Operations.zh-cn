---
title: 设置集中的付款
description: 按照以下步骤可以代表您的组织中的其他法人准备一个法人的处理付款。
author: kweekley
manager: AnnBe
ms.date: 05/09/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerInterCompany
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 62243
ms.assetid: ffd17b5f-9aea-40e0-be49-d8702f615256
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bb0769d605b831da09046a1e7bf0c2a704dba398
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/29/2019
ms.locfileid: "361904"
---
# <a name="set-up-centralized-payments"></a><span data-ttu-id="05be6-103">设置集中的付款</span><span class="sxs-lookup"><span data-stu-id="05be6-103">Set up centralized payments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="05be6-104">按照以下步骤可以代表您的组织中的其他法人准备一个法人的处理付款。</span><span class="sxs-lookup"><span data-stu-id="05be6-104">Follow these steps to prepare to process payments in one legal entity on behalf of other legal entities in your organization.</span></span> <span data-ttu-id="05be6-105">在您开始前，必须完成以下设置：</span><span class="sxs-lookup"><span data-stu-id="05be6-105">Before you begin, the following setup must be completed:</span></span>

-   <span data-ttu-id="05be6-106">创建法人。</span><span class="sxs-lookup"><span data-stu-id="05be6-106">Create legal entities.</span></span>
-   <span data-ttu-id="05be6-107">设置总帐参数和会计科目表。</span><span class="sxs-lookup"><span data-stu-id="05be6-107">Set up General ledger parameters and charts of accounts.</span></span>
-   <span data-ttu-id="05be6-108">设置应付账款参数和应收账款参数（取决于使用集中付款的模块）。</span><span class="sxs-lookup"><span data-stu-id="05be6-108">Set up Accounts payable parameters and Accounts receivable parameters (depending on the modules that are using centralized payments).</span></span>
-   <span data-ttu-id="05be6-109">设置内部公司会计。</span><span class="sxs-lookup"><span data-stu-id="05be6-109">Set up intercompany accounting.</span></span>

## <a name="set-up-an-organizational-hierarchy-for-centralized-payments"></a><span data-ttu-id="05be6-110">为集中付款设置组织的层次结构。</span><span class="sxs-lookup"><span data-stu-id="05be6-110">Set up an organizational hierarchy for centralized payments</span></span>
<span data-ttu-id="05be6-111">您必须为集中付款设置组织的层次结构。</span><span class="sxs-lookup"><span data-stu-id="05be6-111">You must set up an organizational hierarchy for centralized payments.</span></span> <span data-ttu-id="05be6-112">将相同的组织层次结构用于处理集中的供应商付款和集中的客户付款。</span><span class="sxs-lookup"><span data-stu-id="05be6-112">The same organizational hierarchy is used to process centralized vendor payments and centralized customer payments.</span></span> <span data-ttu-id="05be6-113">**注意：** 对于集中付款，该层次结构的结构不会产生影响。</span><span class="sxs-lookup"><span data-stu-id="05be6-113">**Note:** For centralized payments, the structure of the hierarchy doesn't matter.</span></span> <span data-ttu-id="05be6-114">层次结构中的任何法人都将能代表层次结构中的任何其他法人处理付款。</span><span class="sxs-lookup"><span data-stu-id="05be6-114">Any legal entity in the hierarchy will be able to process payments on behalf of any other legal entity in the hierarchy.</span></span> <span data-ttu-id="05be6-115">在**组织层次结构**页上，您可以创建一个新的组织层次结构。</span><span class="sxs-lookup"><span data-stu-id="05be6-115">On the **Organization hierarchies** page, you can create a new organization hierarchy.</span></span> <span data-ttu-id="05be6-116">在**用途**字段中，必须选择**集中付款**。</span><span class="sxs-lookup"><span data-stu-id="05be6-116">In the **Purpose** field, you must select **Centralized payments**.</span></span> 

## <a name="set-up-an-intercompany-account-for-centralized-payments"></a><span data-ttu-id="05be6-117">为集中付款设置内部公司帐户</span><span class="sxs-lookup"><span data-stu-id="05be6-117">Set up an intercompany account for centralized payments</span></span>
<span data-ttu-id="05be6-118">在对照其他法人中的发票结算当前法人中的付款交易记录时，将为每个法人创建相应的应付和应收交易记录。</span><span class="sxs-lookup"><span data-stu-id="05be6-118">When payment transactions in the current legal entity are settled against invoices in other legal entities, the appropriate due-to and due-from transactions are created for each legal entity.</span></span> <span data-ttu-id="05be6-119">您必须指定过帐任何适用现金折扣和已有损益金额的法人。</span><span class="sxs-lookup"><span data-stu-id="05be6-119">You must specify the legal entity where any applicable cash discounts and realized gain or loss amounts are posted.</span></span> <span data-ttu-id="05be6-120">在开始前，确定您将使用哪一法人处理供应商和客户付款。</span><span class="sxs-lookup"><span data-stu-id="05be6-120">Before you begin, decide which legal entity you will use to process vendor and customer payments.</span></span> <span data-ttu-id="05be6-121">如果一个法人处理供应商付款，另一个法人处理客户付款，您必须切换到各法人。</span><span class="sxs-lookup"><span data-stu-id="05be6-121">If one legal entity processes vendor payments but another legal entity processes customer payments, you will have to switch to each legal entity.</span></span> <span data-ttu-id="05be6-122">在**内部公司会计**页上，可以为将代表其处理付款的法人选择内部公司关系记录。</span><span class="sxs-lookup"><span data-stu-id="05be6-122">On the **Intercompany accounting** page, you can select an intercompany relationship record for a legal entity that you will process payments on behalf of.</span></span> 

<span data-ttu-id="05be6-123">在**集中付款**选项卡上，您可以选择是将现金折扣过帐到付款（或减少供应商帐户余额的其他交易记录）法人还是发票（或增加供应商帐户余额的其他交易记录）法人。</span><span class="sxs-lookup"><span data-stu-id="05be6-123">On the **Centralized payments** tab, you can select whether to post cash discounts to the legal entity of the payment (or other transaction that decreases the balance of the vendor account) or the legal entity of the invoice (or other transaction that increases the balance of the vendor account).</span></span> <span data-ttu-id="05be6-124">此选择与**应付账款参数**和**应收账款参数**页的**现金折扣管理**字段一起工作。</span><span class="sxs-lookup"><span data-stu-id="05be6-124">This selection works together with the **Cash discount administration** field on the **Accounts payable parameters** and **Accounts receivable parameters** pages.</span></span> <span data-ttu-id="05be6-125">对于超额付款和尾差容差，使用付款的法人中的设置。</span><span class="sxs-lookup"><span data-stu-id="05be6-125">For overpayments and penny difference tolerances, the setting in the legal entity of the payment is used.</span></span> <span data-ttu-id="05be6-126">对于支付不足和尾差容差，使用发票的法人中的设置。</span><span class="sxs-lookup"><span data-stu-id="05be6-126">For underpayments and penny difference tolerances, the setting in the legal entity of the invoice is used.</span></span>

## <a name="map-vendor-accounts-across-legal-entities"></a><span data-ttu-id="05be6-127">映射跨法人的供应商账户</span><span class="sxs-lookup"><span data-stu-id="05be6-127">Map vendor accounts across legal entities</span></span>
<span data-ttu-id="05be6-128">当您支付某个法人的供应商并且您想选择其他法人中的供应商的发票时，您必须确保每个法人中的相应的供应商账户都使用相同的地址簿 ID。</span><span class="sxs-lookup"><span data-stu-id="05be6-128">If you pay a vendor from one legal entity and want to select invoices for that vendor in other legal entities, you must make sure that all the corresponding vendor accounts in each legal entity use the same address book ID.</span></span> <span data-ttu-id="05be6-129">如果您接收来自在多个法人中支付发票的客户的付款，则必须确保每个法人中的相应客户帐户全都使用相同的通讯簿 ID。</span><span class="sxs-lookup"><span data-stu-id="05be6-129">If you receive a payment from a customer that pays invoices in more than one legal entity, you must make sure that all the corresponding customer accounts in each legal entity use the same address book ID.</span></span>

## <a name="set-up-posting-profiles-for-centralized-payments"></a><span data-ttu-id="05be6-130">为集中付款设置过帐模板</span><span class="sxs-lookup"><span data-stu-id="05be6-130">Set up posting profiles for centralized payments</span></span>
<span data-ttu-id="05be6-131">当您在结算另一个法人的发票的法人中创建了付款，过帐模板 ID 在这两个法人中必须相同。</span><span class="sxs-lookup"><span data-stu-id="05be6-131">When you create a payment in one legal entity that settles invoices in other legal entities, the posting profile IDs must be the same in both legal entities.</span></span> <span data-ttu-id="05be6-132">为了帮助确保正确创建付款，在发票的每个法人中，设置与付款法人中使用的过帐模板相对应的过帐模板。</span><span class="sxs-lookup"><span data-stu-id="05be6-132">To help guarantee that payments are created correctly, in each legal entity of the invoice, set up a posting profile that corresponds to the posting profiles that are used in the legal entity of the payment.</span></span> <span data-ttu-id="05be6-133">切换到发票的第一个法人，然后，在**供应商过帐模板**页上，您可以创建一个新的过帐模板或编辑现有的过帐模板。</span><span class="sxs-lookup"><span data-stu-id="05be6-133">Switch to the first legal entity of the invoice, and then, on the **Vendor posting profiles** page, you can create a new posting profile or edit an existing posting profile.</span></span> <span data-ttu-id="05be6-134">在发票的法人中为过帐模板所做的选择不必与付款法人中过帐模板的设置匹配。</span><span class="sxs-lookup"><span data-stu-id="05be6-134">The selections that you make for the posting profile in the legal entity of the invoice don't have to match the setup of the posting profile in the legal entity of the payment.</span></span>

## <a name="set-up-methods-of-payment-for-centralized-payments"></a><span data-ttu-id="05be6-135">设置集中付款的付款方式</span><span class="sxs-lookup"><span data-stu-id="05be6-135">Set up methods of payment for centralized payments</span></span>
<span data-ttu-id="05be6-136">当您在结算另一个法人的发票的法人中的创建了付款，付款方法 ID 在这两个法人中必须相同。</span><span class="sxs-lookup"><span data-stu-id="05be6-136">When you create a payment in one legal entity that settles invoices in other legal entities, the method of payment IDs must be the same in both legal entities.</span></span> <span data-ttu-id="05be6-137">为了帮助确保正确创建付款，在发票的各个法人中，设置与付款法人中使用的付款方式相符的付款方式。</span><span class="sxs-lookup"><span data-stu-id="05be6-137">To help guarantee that payments are created correctly, in each legal entity of the invoice, set up a method of payment that corresponds to the methods of payment that are used in the legal entity of the payment.</span></span> <span data-ttu-id="05be6-138">切换到发票的第一个法人，然后，在**付款方法**页，可以创建新的付款方法或编辑现有的付款方法。</span><span class="sxs-lookup"><span data-stu-id="05be6-138">Switch to the first legal entity of the invoice, and then, on the **Methods of payment** page, you can create a new method of payment or edit an existing method of payment.</span></span> <span data-ttu-id="05be6-139">您在发票法人中为付款方法进行的选择不必与在付款法人中付款方法的设置相匹配。</span><span class="sxs-lookup"><span data-stu-id="05be6-139">The selections that you make for the method of payment in the legal entity of the invoice don't have to match the setup of the method of payment in the legal entity of the payment.</span></span>

## <a name="set-up-default-descriptions"></a><span data-ttu-id="05be6-140">设置默认描述</span><span class="sxs-lookup"><span data-stu-id="05be6-140">Set up default descriptions</span></span>
<span data-ttu-id="05be6-141">您可为内部公司结算凭证定义默认描述。</span><span class="sxs-lookup"><span data-stu-id="05be6-141">You can define default descriptions for intercompany settlement vouchers.</span></span> <span data-ttu-id="05be6-142">该默认描述包括在跨公司结算过程中的应付和应收交易记录上。</span><span class="sxs-lookup"><span data-stu-id="05be6-142">The default description is included on the due-to and due-from transactions during the cross-company settlement process.</span></span> <span data-ttu-id="05be6-143">在**默认描述**页上，您可以为**内部公司客户结算**和**内部公司供应商结算**创建新的描述，方法是通过选择语言然后输入文本。</span><span class="sxs-lookup"><span data-stu-id="05be6-143">On the **Default descriptions** page, you can create new descriptions for both **Intercompany customer settlement** and **Intercompany vendor settlement** by selecting a language and then entering text.</span></span>



