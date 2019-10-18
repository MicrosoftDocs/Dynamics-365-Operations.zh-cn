---
title: 设定客户付款方式
description: 本主题说明如何为客户付款创建付款方式。
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/31/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPaymMode, BankAccountTableLookUp
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 22680a3033c1518735eb9edb4c6f22f310509aba
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/27/2019
ms.locfileid: "2188801"
---
# <a name="establish-customer-method-of-payment"></a><span data-ttu-id="fc708-103">设定客户付款方式</span><span class="sxs-lookup"><span data-stu-id="fc708-103">Establish customer method of payment</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="fc708-104">本主题说明如何为客户付款创建付款方式。</span><span class="sxs-lookup"><span data-stu-id="fc708-104">This topic explains how to create a method of payment for customer payments.</span></span> <span data-ttu-id="fc708-105">此任务使用 USMF 公司演示。</span><span class="sxs-lookup"><span data-stu-id="fc708-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="fc708-106">在导航窗格中，转到**模块 > 应收帐款 > 付款设置 > 付款方式**。</span><span class="sxs-lookup"><span data-stu-id="fc708-106">In the navigation pane, go to **Modules > Accounts receivable > Payments setup > Methods of payment**.</span></span>
2. <span data-ttu-id="fc708-107">选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="fc708-107">Select **New**.</span></span>
3. <span data-ttu-id="fc708-108">在**付款方式**字段中，为付款方式输入一个 ID。</span><span class="sxs-lookup"><span data-stu-id="fc708-108">In the **Method of payment** field, enter an ID for the method of payment.</span></span> <span data-ttu-id="fc708-109">付款方式 ID 将显示在发票和付款上，以便您足够清晰地了解正在记录的付款类型以及所使用的银行帐户。</span><span class="sxs-lookup"><span data-stu-id="fc708-109">The Method of payment ID is shown on invoices and payments, so make it descriptive enough to understand what type of payment is being recorded, and for what bank account.</span></span>  
4. <span data-ttu-id="fc708-110">在**描述**字段中，输入描述。</span><span class="sxs-lookup"><span data-stu-id="fc708-110">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="fc708-111">选择需要哪种付款状态才能过帐付款。</span><span class="sxs-lookup"><span data-stu-id="fc708-111">Select what payment status is required in order for payments to be posted.</span></span> <span data-ttu-id="fc708-112">在创建客户付款时，只有当付款状态与您在此处定义的付款状态匹配时才可以过帐。</span><span class="sxs-lookup"><span data-stu-id="fc708-112">When creating a customer payment, it can only be posted when the payment status matches the payment status you define here.</span></span>  
6. <span data-ttu-id="fc708-113">选择如何为发票创建客户付款。</span><span class="sxs-lookup"><span data-stu-id="fc708-113">Select how customers payments should be created for invoices.</span></span> <span data-ttu-id="fc708-114">仅当运行付款提议时才使用该选项。</span><span class="sxs-lookup"><span data-stu-id="fc708-114">This option is only used when running a payment proposal.</span></span> <span data-ttu-id="fc708-115">在进行直接借记和从客户的银行帐户收集资金时可以在客户付款中使用付款提议。</span><span class="sxs-lookup"><span data-stu-id="fc708-115">A payment proposal could be used for customer payments when doing direct debits, and pulling the funds from the customers' bank accounts.</span></span>  
7. <span data-ttu-id="fc708-116">选择付款类型。</span><span class="sxs-lookup"><span data-stu-id="fc708-116">Select the type of payment.</span></span> <span data-ttu-id="fc708-117">付款类型将有助于确定付款时是否会出现验证。</span><span class="sxs-lookup"><span data-stu-id="fc708-117">The payment type will help determine whether some validation will occur or not on the payment.</span></span>  
8. <span data-ttu-id="fc708-118">选择要过帐的付款的帐户类型。</span><span class="sxs-lookup"><span data-stu-id="fc708-118">Select what account type payments will post to.</span></span> <span data-ttu-id="fc708-119">通常为此选项选择“银行”。</span><span class="sxs-lookup"><span data-stu-id="fc708-119">Typically, Bank would be selected for this option.</span></span>  
9. <span data-ttu-id="fc708-120">选择该项付款将记录的银行帐户。</span><span class="sxs-lookup"><span data-stu-id="fc708-120">Select the bank account into which this payment will be recorded.</span></span>
10. <span data-ttu-id="fc708-121">输入“银行交易记录类型”以标识您的银行所使用的付款类型。</span><span class="sxs-lookup"><span data-stu-id="fc708-121">Enter the Bank transaction type to identify the type of payment used by your bank.</span></span> <span data-ttu-id="fc708-122">银行交易记录类型用于银行对帐过程，并且可以使对帐更容易。</span><span class="sxs-lookup"><span data-stu-id="fc708-122">The bank transaction type is used during the bank reconciliation process, and can make reconciliation easier.</span></span>  
11. <span data-ttu-id="fc708-123">选择此项旨在确定付款是否暂时过帐到过渡帐户。</span><span class="sxs-lookup"><span data-stu-id="fc708-123">Select whether this payment will temporarily post to a bridging account.</span></span> <span data-ttu-id="fc708-124">如果您想要尝试付款的浮动时间，以此来清除银行帐户，请使用“桥接”功能。</span><span class="sxs-lookup"><span data-stu-id="fc708-124">If you want to try the float time for a payment to clear the bank, use the Bridging functionality.</span></span> <span data-ttu-id="fc708-125">付款将暂时过帐到一个分类帐，直到其清除了银行帐户，此时，付款将会移到您在此处定义的银行帐户。</span><span class="sxs-lookup"><span data-stu-id="fc708-125">The payment will temporarily post to a Ledger account until it clears the bank, at which time the payment will move to the bank account you defined here.</span></span>  
12. <span data-ttu-id="fc708-126">输入过渡过帐的主要帐户。</span><span class="sxs-lookup"><span data-stu-id="fc708-126">Enter the main account used for the bridging posting.</span></span> <span data-ttu-id="fc708-127">这是使用桥接时付款将会被暂时过帐到其中的主要帐户。</span><span class="sxs-lookup"><span data-stu-id="fc708-127">This is the main account to which the payment will temporarily post if using bridging.</span></span>  
13. <span data-ttu-id="fc708-128">使用**文件格式**选项卡是为电子付款设置进行定义。</span><span class="sxs-lookup"><span data-stu-id="fc708-128">Use the **File format** tab to define setting for electronic payments.</span></span>
14. <span data-ttu-id="fc708-129">使用**付款控制**选项卡以定义必填字段。</span><span class="sxs-lookup"><span data-stu-id="fc708-129">Use the **Payment control** tab to define fields that are mandatory.</span></span> <span data-ttu-id="fc708-130">例如，如果您要求存入所有带该付款方式的付款，您可以在此选项卡上选择该选项。</span><span class="sxs-lookup"><span data-stu-id="fc708-130">For example, if you require all payments with this method of payment to be deposited, you can choose that option on this tab.</span></span>  
15. <span data-ttu-id="fc708-131">使用**付款属性**选项卡以定义您想针对此付款方式使用哪种付款属性。</span><span class="sxs-lookup"><span data-stu-id="fc708-131">Use the **Payment atrributes** tab to define which payment attributes you want to use for this method of payment.</span></span>
16. <span data-ttu-id="fc708-132">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="fc708-132">Select **Save**.</span></span>

