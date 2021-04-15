---
title: 零售商店中的财务对帐
description: 本主题介绍 POS for Microsoft Dynamics 365 Commerce 中的零售商店财务对帐。
author: anpurush
ms.date: 06/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-05-21
ms.dyn365.ops.version: ''
ms.openlocfilehash: 0f57f3119039337922dcd4035e1c4d64e6ae7295
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5792383"
---
# <a name="financial-reconciliation-in-retail-stores"></a><span data-ttu-id="a67e8-103">零售商店中的财务对帐</span><span class="sxs-lookup"><span data-stu-id="a67e8-103">Financial reconciliation in retail stores</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="a67e8-104">在 Microsoft Dynamics 365 Commerce 版本 10.0.10 及更低版本中，商店职员和商店经理可使用销售点 (POS) 客户端为零售商店中的日结流程提供的功能执行日结操作。</span><span class="sxs-lookup"><span data-stu-id="a67e8-104">In Microsoft Dynamics 365 Commerce version 10.0.10 and earlier, the functionality that the point of sale (POS) client provides for end-of-day processes in retail stores lets store clerks and store managers perform end-of-day operations.</span></span> <span data-ttu-id="a67e8-105">例如，可以进行点钞、直接结束班次，协调班次事务和结束班次。</span><span class="sxs-lookup"><span data-stu-id="a67e8-105">For example, they can do tender declarations, blind-close shifts, reconcile shift transactions, and close shifts.</span></span> <span data-ttu-id="a67e8-106">但是，在 POS 中不能完成班次的财务信息，因此可将其用于在 Commerce Headquarters 中过帐财务数据。</span><span class="sxs-lookup"><span data-stu-id="a67e8-106">However, there is no capability in POS to finalize the financial information for shifts, so that it can be used to post the financials in Commerce headquarters.</span></span> <span data-ttu-id="a67e8-107">通常由商店经理负责完成此任务。</span><span class="sxs-lookup"><span data-stu-id="a67e8-107">Typically, store managers are responsible for completing this task.</span></span> <span data-ttu-id="a67e8-108">他们必须先检查信息，进行必需的更正，然后完成班次的总计，才能注销班次。</span><span class="sxs-lookup"><span data-stu-id="a67e8-108">Before they can sign off on a shift, they must review the information, make any corrections that are required, and finalize the totals for that shift.</span></span> <span data-ttu-id="a67e8-109">然后应该在 Commerce Headquarters 中的财务模块内过帐完成的总计。</span><span class="sxs-lookup"><span data-stu-id="a67e8-109">The finalized totals should then be posted in financial modules in Commerce headquarters.</span></span>

<span data-ttu-id="a67e8-110">此外，在 Commerce version 10.0.10 及更低版本中，商店经理还可以在 Commerce Headquarters 中检查对帐单行并进行一些调整。</span><span class="sxs-lookup"><span data-stu-id="a67e8-110">Additionally, in Commerce version 10.0.10 and earlier, store managers can review and make some adjustments to statement lines in Commerce headquarters.</span></span> <span data-ttu-id="a67e8-111">但是，此功能受到限制，商店经理几乎不能访问 Commerce Headquarters 客户端。</span><span class="sxs-lookup"><span data-stu-id="a67e8-111">However, the capability is limited, and store managers rarely have access to the Commerce headquarters client.</span></span> <span data-ttu-id="a67e8-112">此外，仅当对帐单是在 Commerce Headquarters 中创建的，才能进行财务零售对帐单检查和调整。</span><span class="sxs-lookup"><span data-stu-id="a67e8-112">Moreover, financial retail statement review and adjustment can be done only when the statements are created in Commerce headquarters.</span></span> <span data-ttu-id="a67e8-113">不过，该流程通常在夜间进行。</span><span class="sxs-lookup"><span data-stu-id="a67e8-113">However, that process is typically a nightly process.</span></span> <span data-ttu-id="a67e8-114">因此，在 Commerce Headquarters 中创建财务零售对帐单时，商店经理必须等待班次注销。</span><span class="sxs-lookup"><span data-stu-id="a67e8-114">Therefore, store managers must wait for the shift sign-off when financial retail statements are created in Commerce headquarters.</span></span>

<span data-ttu-id="a67e8-115">在 Commerce 版本 10.0.11 及更高版本中，商店经理可以在 POS 客户端中执行检查、调整和完成自己的班次。</span><span class="sxs-lookup"><span data-stu-id="a67e8-115">In Commerce version 10.0.11 and later, store managers can review, adjust, and finalize their shifts in the POS client itself.</span></span> <span data-ttu-id="a67e8-116">然后使用这些数据在 Commerce Headquarters 中创建和过帐财务零售对帐单。</span><span class="sxs-lookup"><span data-stu-id="a67e8-116">That data is then used to create and post financial retail statements in Commerce headquarters.</span></span>

> [!NOTE]
> <span data-ttu-id="a67e8-117">仅当开启了基于缓慢馈送的订单创建功能，零售商店中才支持与财务对帐有关的功能。</span><span class="sxs-lookup"><span data-stu-id="a67e8-117">The functionality that is related to financial reconciliation in retail stores works only if trickle feed–based order creation is turned on.</span></span> <span data-ttu-id="a67e8-118">有关详细信息，请参阅[为零售商店交易记录创建基于缓慢馈送的订单](trickle-feed.md)。</span><span class="sxs-lookup"><span data-stu-id="a67e8-118">For more information, see [Trickle feed-based order creation for retail store transactions](trickle-feed.md).</span></span>

## <a name="set-up-financial-reconciliation"></a><span data-ttu-id="a67e8-119">设置财务对帐</span><span class="sxs-lookup"><span data-stu-id="a67e8-119">Set up financial reconciliation</span></span>

<span data-ttu-id="a67e8-120">请按照以下步骤使用财务对帐功能。</span><span class="sxs-lookup"><span data-stu-id="a67e8-120">Follow these steps to use the financial reconciliation functionality.</span></span>

1. <span data-ttu-id="a67e8-121">在 **功能管理** 工作区中，开启 **零售对帐单 - 缓慢馈送** 功能。</span><span class="sxs-lookup"><span data-stu-id="a67e8-121">In the **Feature management** workspace, turn on the **Retail statements - Trickle feed** feature.</span></span>
1. <span data-ttu-id="a67e8-122">在相应商店的 POS 功能配置文件中，将 **在商店中启用财务对帐** 选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="a67e8-122">In the POS functionality profile for the appropriate store, set the **Enable financial reconciliation in store** option to **Yes**.</span></span>

## <a name="more-information-about-financial-reconciliation"></a><span data-ttu-id="a67e8-123">有关财务对帐的详细信息</span><span class="sxs-lookup"><span data-stu-id="a67e8-123">More information about financial reconciliation</span></span>

<span data-ttu-id="a67e8-124">财务对帐功能开启后，将把 Commerce Headquarters 中 **零售商店** 页 **报表/结算** 快速选项卡上定义的部分参数同步到渠道数据库。</span><span class="sxs-lookup"><span data-stu-id="a67e8-124">When the financial reconciliation functionality is turned on, some of the parameters that are defined on the **Statement/closing** FastTab of the **Retail stores** page in Commerce headquarters are synced to the channel database.</span></span> <span data-ttu-id="a67e8-125">将实施用于零售对帐单的同一组计算条件和金额阈值。</span><span class="sxs-lookup"><span data-stu-id="a67e8-125">The same set of calculation criteria and amount thresholds that is used for retail statements is enforced.</span></span>

<span data-ttu-id="a67e8-126">调用 **结束班次** 操作时，系统将验证系统计算出的金额与申报金额是否匹配。</span><span class="sxs-lookup"><span data-stu-id="a67e8-126">When the **Close shift** operation is invoked, the system validates that the system-computed amounts and the declared amounts match.</span></span> <span data-ttu-id="a67e8-127">如果不同，并且差额超过了定义的阈值，将提示用户进行必要调整。</span><span class="sxs-lookup"><span data-stu-id="a67e8-127">If they differ, and the difference exceeds defined thresholds, the user is prompted and can make the required adjustments.</span></span>

<span data-ttu-id="a67e8-128">可以对每笔支付进行调整。</span><span class="sxs-lookup"><span data-stu-id="a67e8-128">Adjustments can be made for each tender.</span></span> <span data-ttu-id="a67e8-129">选择支付后，用户可以查看不同交易类型的总计和编辑特定交易类型的总计。</span><span class="sxs-lookup"><span data-stu-id="a67e8-129">When a tender is selected, the user can view the totals for different transaction types and edit the totals for a specific transaction type.</span></span> <span data-ttu-id="a67e8-130">编辑期间，系统将显示最初为该交易类型计算出的金额和替换成的金额。</span><span class="sxs-lookup"><span data-stu-id="a67e8-130">During editing, the system shows the original computed amount and the overridden amount for that transaction type.</span></span> <span data-ttu-id="a67e8-131">用户也可以在编辑过程中捕获通知单。</span><span class="sxs-lookup"><span data-stu-id="a67e8-131">The user can also capture notes as a part of the editing process.</span></span> <span data-ttu-id="a67e8-132">通知单可用于审核目的。</span><span class="sxs-lookup"><span data-stu-id="a67e8-132">Notes can be used for auditing purposes.</span></span>

<span data-ttu-id="a67e8-133">用户可以忽略验证提示和消息，也可以继续结束班次。</span><span class="sxs-lookup"><span data-stu-id="a67e8-133">Users can ignore the validation prompts and messages, and can proceed to close the shift.</span></span> <span data-ttu-id="a67e8-134">但是，如果用户忽略验证提示，当班次在 Commerce Headquarters 中过帐财务对帐单时，将发生相同问题，并且必须解决这些问题。</span><span class="sxs-lookup"><span data-stu-id="a67e8-134">However, if a user ignores the validation prompts, the same issues will arise and will have to be fixed when the shift posts financial statements in Commerce headquarters.</span></span>

<span data-ttu-id="a67e8-135">POS 中的 **结束班次** 操作还会验证脱机数据库中的所有交易记录是否已同步到渠道数据库。</span><span class="sxs-lookup"><span data-stu-id="a67e8-135">The **Close shift** operation in POS also validates that all transactions in the offline database are synced to the channel database.</span></span> <span data-ttu-id="a67e8-136">如果未同步任何交易记录，用户将收到警告消息，因为这种情况可能导致系统计算出的金额不正确。</span><span class="sxs-lookup"><span data-stu-id="a67e8-136">If any transactions aren't synced, the user receives a warning message, because this situation can cause the system amounts to be incorrectly computed.</span></span> <span data-ttu-id="a67e8-137">在这种情况下，用户可以结束 **结束班次** 操作，并尝试将脱机交易记录同步到渠道数据库。</span><span class="sxs-lookup"><span data-stu-id="a67e8-137">In this situation, the user can end the **Close shift** operation and try to sync the offline transactions to the channel database.</span></span> <span data-ttu-id="a67e8-138">或者，用户也可以将系统计算出的金额手动调整为未同步的交易记录的金额，从而结束和过帐一组正确的财务数字。</span><span class="sxs-lookup"><span data-stu-id="a67e8-138">Alternatively, the user can manually adjust the system-computed amounts to account for the transactions that aren't synced, so that the correct set of financial numbers is finalized and posted.</span></span> 

<span data-ttu-id="a67e8-139">如果使用缓慢馈送对帐单过帐，从而使交易记录过帐与财务过帐分开，可以选择调整系统为缺少的脱机交易记录计算出的金额。</span><span class="sxs-lookup"><span data-stu-id="a67e8-139">When trickle feed statement posting is used, so that the posting of transactions is separated from the posting of financials, you can choose to adjust the system-computed amounts for missing offline transactions.</span></span> <span data-ttu-id="a67e8-140">这样就可以确保无论是否缺少交易记录，始终正确核算和过帐财务数据。</span><span class="sxs-lookup"><span data-stu-id="a67e8-140">In this way, you ensure that financials are always accounted and posted correctly, regardless of missing transactions.</span></span> <span data-ttu-id="a67e8-141">可以将脱机交易记录同步到渠道数据库和 Commerce Headquarters，之后再过帐，从而与财务过帐分开。</span><span class="sxs-lookup"><span data-stu-id="a67e8-141">Offline transactions can be synced to the channel database and Commerce headquarters, and then posted later, separately from the financial postings.</span></span>

<span data-ttu-id="a67e8-142">将使用 P 作业把班次的财务对帐详细信息同步到 Commerce Headquarters。</span><span class="sxs-lookup"><span data-stu-id="a67e8-142">Details of the financial reconciliation for a shift are synced to Commerce headquarters by using the P-job.</span></span>

<span data-ttu-id="a67e8-143">Commerce Headquarters 中的财务零售对帐单不会计算总计以在对帐单行中显示详细信息。</span><span class="sxs-lookup"><span data-stu-id="a67e8-143">Financial retail statements in Commerce headquarters don't compute totals to show the details on the statement lines.</span></span> <span data-ttu-id="a67e8-144">而是使用 POS 客户端中的最终金额创建和过帐财务零售对帐单。</span><span class="sxs-lookup"><span data-stu-id="a67e8-144">Instead, the finalized amounts in the POS client are used to create and post financial retail statements.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]