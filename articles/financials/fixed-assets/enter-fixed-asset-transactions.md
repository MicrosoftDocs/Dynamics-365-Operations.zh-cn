---
title: "固定资产交易记录选项"
description: "本文介绍可用来创建固定资产交易记录的不同方法。"
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetTable, PurchCreateOrder
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 23061
ms.assetid: 338c495b-a4d8-461e-b85b-a83faf673730
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 18352ad921c2e2d110a7535f979272685105662f
ms.contentlocale: zh-cn
ms.lasthandoff: 11/03/2017

---

# <a name="fixed-asset-transaction-options"></a><span data-ttu-id="98352-103">固定资产交易记录选项</span><span class="sxs-lookup"><span data-stu-id="98352-103">Fixed asset transaction options</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="98352-104">本文介绍可用来创建固定资产交易记录的不同方法。</span><span class="sxs-lookup"><span data-stu-id="98352-104">This article describes the different methods available to create fixed asset transactions.</span></span>

<span data-ttu-id="98352-105">您可以使用应收账款、应付账款、采购和源，以及总帐设置集成的固定资产。</span><span class="sxs-lookup"><span data-stu-id="98352-105">You can set up Fixed assets for integration with Accounts payable, Accounts receivable, Procurement and sourcing, and General ledger.</span></span> <span data-ttu-id="98352-106">如果您要在内部使用这些物料，您还可以将库存管理中的物料转移到固定资产。</span><span class="sxs-lookup"><span data-stu-id="98352-106">You can also transfer items in Inventory management to Fixed assets if you want to use those items internally.</span></span>

## <a name="accounts-payable"></a><span data-ttu-id="98352-107">应付账款</span><span class="sxs-lookup"><span data-stu-id="98352-107">Accounts payable</span></span>
<span data-ttu-id="98352-108">您可以在“日记帐凭证”页中输入固定资产交易记录。</span><span class="sxs-lookup"><span data-stu-id="98352-108">You can enter Fixed assets transactions in the Journal voucher page.</span></span> <span data-ttu-id="98352-109">此页可以从“发票日记帐”页中打开。</span><span class="sxs-lookup"><span data-stu-id="98352-109">This page can be opened from the Invoice journal page.</span></span> <span data-ttu-id="98352-110">您还可以从“发票审核日记帐”页中打开“日记帐凭证”页。</span><span class="sxs-lookup"><span data-stu-id="98352-110">You can also open the Journal voucher page from the Invoice approval journal page.</span></span> <span data-ttu-id="98352-111">在“对方科目类型”字段中，选择“固定资产”。</span><span class="sxs-lookup"><span data-stu-id="98352-111">In the Offset account type field, select Fixed assets.</span></span> <span data-ttu-id="98352-112">然后，在“对方科目”字段中，选择一个固定资产编号作。</span><span class="sxs-lookup"><span data-stu-id="98352-112">Then, in the Offset account field, select a fixed asset number.</span></span> <span data-ttu-id="98352-113">在“固定资产”选项卡上，在“交易记录类型”和“帐簿”字段中输入值。</span><span class="sxs-lookup"><span data-stu-id="98352-113">On the Fixed assets tab, enter values in the Transaction type and Book fields.</span></span>

## <a name="accounts-receivable"></a><span data-ttu-id="98352-114">应收账款</span><span class="sxs-lookup"><span data-stu-id="98352-114">Accounts receivable</span></span>
<span data-ttu-id="98352-115">您可以在“普通发票”页中输入固定资产交易记录。</span><span class="sxs-lookup"><span data-stu-id="98352-115">You can enter Fixed assets transactions in the Free text invoice page.</span></span>  <span data-ttu-id="98352-116">在“普通发票”页中的“发票行”窗格中，选择一个行项。</span><span class="sxs-lookup"><span data-stu-id="98352-116">In the Free text invoice page, in the Invoice lines grid, select a line item.</span></span> <span data-ttu-id="98352-117">单击“行明细”快速选项卡。</span><span class="sxs-lookup"><span data-stu-id="98352-117">Click the Line details FastTab.</span></span> <span data-ttu-id="98352-118">为处置交易记录输入固定资产编号和帐簿。</span><span class="sxs-lookup"><span data-stu-id="98352-118">Enter the fixed asset number and book for the disposal transaction.</span></span> <span data-ttu-id="98352-119">对于普通发票，固定资产交易记录的类型始终是“处置 - 出售”。</span><span class="sxs-lookup"><span data-stu-id="98352-119">For free text invoices, the fixed asset transaction type is always Disposal - sale.</span></span>

## <a name="procurement-and-sourcing"></a><span data-ttu-id="98352-120">采购</span><span class="sxs-lookup"><span data-stu-id="98352-120">Procurement and sourcing</span></span>
<span data-ttu-id="98352-121">您可以在“采购订单”页中输入固定资产交易记录。</span><span class="sxs-lookup"><span data-stu-id="98352-121">You can enter Fixed assets transactions in the Purchase order page.</span></span> <span data-ttu-id="98352-122">输入必需的信息创建采购订单，然后单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="98352-122">Enter the required information to create a purchase order, and then click OK.</span></span> <span data-ttu-id="98352-123">在“采购订单”页中，单击“行明细”快速选项卡。</span><span class="sxs-lookup"><span data-stu-id="98352-123">In the Purchase order page, click the Line details FastTab.</span></span> <span data-ttu-id="98352-124">然后，在“固定资产”选项卡上，输入有关固定资产的信息。</span><span class="sxs-lookup"><span data-stu-id="98352-124">Then, on the Fixed assets tab, enter information about the fixed asset.</span></span> 

<span data-ttu-id="98352-125">若要过帐现有固定资产的购置交易记录，请指定固定资产编号、帐簿和交易记录类型。</span><span class="sxs-lookup"><span data-stu-id="98352-125">To post an acquisition transaction for an existing fixed asset, specify the fixed asset number, book, and transaction type.</span></span> <span data-ttu-id="98352-126">如果缺少此信息中任何信息，则不能过帐固定资产。</span><span class="sxs-lookup"><span data-stu-id="98352-126">The fixed asset cannot be posted if any of this information is missing.</span></span> <span data-ttu-id="98352-127">若要过帐新的固定资产的购置交易记录，请选择“是否新建固定资产?”选项，然后选择要将新资产分配到的固定资产组。</span><span class="sxs-lookup"><span data-stu-id="98352-127">To post an acquisition transaction for a new fixed asset, select the New fixed asset? option, and then select the fixed asset group to assign the new asset to.</span></span> <span data-ttu-id="98352-128">但是，如果物料处于使用标准成本库存模型的库存模型组中，则对于某一行将没有固定资产字段可用。</span><span class="sxs-lookup"><span data-stu-id="98352-128">However, no fixed asset fields are available for a line if the item is in an inventory model group that uses a standard cost inventory model.</span></span> <span data-ttu-id="98352-129">此外，在“固定资产参数”页中定义的选项确定是否可以过帐来自采购模块的购置交易记录。</span><span class="sxs-lookup"><span data-stu-id="98352-129">Additionally, the options that are defined in the Fixed assets parameters page determine whether you can post acquisition transactions from the purchasing modules.</span></span> 

<span data-ttu-id="98352-130">将采购订单或存货转为固定资产日记帐用于购置固定资产时，将会影响库存成本。</span><span class="sxs-lookup"><span data-stu-id="98352-130">When a purchase order or the Inventory to fixed assets journal is used to acquire fixed assets, the inventory value is affected.</span></span>

## <a name="general-ledger"></a><span data-ttu-id="98352-131">总帐</span><span class="sxs-lookup"><span data-stu-id="98352-131">General ledger</span></span>
<span data-ttu-id="98352-132">任何一种固定资产交易记录类型都可以在“普通日记帐”页中过帐。</span><span class="sxs-lookup"><span data-stu-id="98352-132">Any fixed asset transaction type can be posted in the General journal page.</span></span> <span data-ttu-id="98352-133">您还可以在固定资产中使用日志过帐固定资产交易记录。</span><span class="sxs-lookup"><span data-stu-id="98352-133">You can also use journals in Fixed assets to post fixed asset transactions.</span></span>

## <a name="options-for-entering-fixed-asset-transaction-types"></a><span data-ttu-id="98352-134">用于输入固定资产交易记录类型的选项</span><span class="sxs-lookup"><span data-stu-id="98352-134">Options for entering fixed asset transaction types</span></span>


| <span data-ttu-id="98352-135">交易记录类型</span><span class="sxs-lookup"><span data-stu-id="98352-135">Transaction type</span></span>                    | <span data-ttu-id="98352-136">模块</span><span class="sxs-lookup"><span data-stu-id="98352-136">Module</span></span>                   | <span data-ttu-id="98352-137">期权</span><span class="sxs-lookup"><span data-stu-id="98352-137">Options</span></span>                                   |
|-------------------------------------|--------------------------|-------------------------------------------|
| <span data-ttu-id="98352-138">购置、购置调整</span><span class="sxs-lookup"><span data-stu-id="98352-138">Acquisition, Acquisition adjustment</span></span> | <span data-ttu-id="98352-139">固定资产</span><span class="sxs-lookup"><span data-stu-id="98352-139">Fixed assets</span></span>             | <span data-ttu-id="98352-140">固定资产、库存转为固定资产</span><span class="sxs-lookup"><span data-stu-id="98352-140">Fixed assets, Inventory to fixed assets</span></span>   |
|                                     | <span data-ttu-id="98352-141">总帐</span><span class="sxs-lookup"><span data-stu-id="98352-141">General ledger</span></span>           | <span data-ttu-id="98352-142">普通日记帐</span><span class="sxs-lookup"><span data-stu-id="98352-142">General journal</span></span>                           |
|                                     | <span data-ttu-id="98352-143">应付账款</span><span class="sxs-lookup"><span data-stu-id="98352-143">Accounts payable</span></span>         | <span data-ttu-id="98352-144">发票日记帐、发票审核日记帐</span><span class="sxs-lookup"><span data-stu-id="98352-144">Invoice journal, Invoice approval journal</span></span> |
|                                     | <span data-ttu-id="98352-145">采购</span><span class="sxs-lookup"><span data-stu-id="98352-145">Procurement and sourcing</span></span> | <span data-ttu-id="98352-146">采购订单</span><span class="sxs-lookup"><span data-stu-id="98352-146">Purchase order</span></span>                            |
| <span data-ttu-id="98352-147">折旧</span><span class="sxs-lookup"><span data-stu-id="98352-147">Depreciation</span></span>                        | <span data-ttu-id="98352-148">固定资产</span><span class="sxs-lookup"><span data-stu-id="98352-148">Fixed assets</span></span>             | <span data-ttu-id="98352-149">固定资产</span><span class="sxs-lookup"><span data-stu-id="98352-149">Fixed assets</span></span>                              |
|                                     | <span data-ttu-id="98352-150">总帐</span><span class="sxs-lookup"><span data-stu-id="98352-150">General ledger</span></span>           | <span data-ttu-id="98352-151">普通日记帐</span><span class="sxs-lookup"><span data-stu-id="98352-151">General journal</span></span>                           |
| <span data-ttu-id="98352-152">处置</span><span class="sxs-lookup"><span data-stu-id="98352-152">Disposal</span></span>                            | <span data-ttu-id="98352-153">固定资产</span><span class="sxs-lookup"><span data-stu-id="98352-153">Fixed assets</span></span>             | <span data-ttu-id="98352-154">固定资产</span><span class="sxs-lookup"><span data-stu-id="98352-154">Fixed assets</span></span>                              |
| <span data-ttu-id="98352-155">** **</span><span class="sxs-lookup"><span data-stu-id="98352-155">** **</span></span>                               | <span data-ttu-id="98352-156">总帐</span><span class="sxs-lookup"><span data-stu-id="98352-156">General ledger</span></span>           | <span data-ttu-id="98352-157">普通日记帐</span><span class="sxs-lookup"><span data-stu-id="98352-157">General journal</span></span>                           |
| <span data-ttu-id="98352-158">** **</span><span class="sxs-lookup"><span data-stu-id="98352-158">** **</span></span>                               | <span data-ttu-id="98352-159">应收账款</span><span class="sxs-lookup"><span data-stu-id="98352-159">Accounts receivable</span></span>      | <span data-ttu-id="98352-160">普通发票</span><span class="sxs-lookup"><span data-stu-id="98352-160">Free text invoice</span></span>                         |



<span data-ttu-id="98352-161">有关详细信息，请参阅[固定资产集成](fixed-asset-integration.md)。</span><span class="sxs-lookup"><span data-stu-id="98352-161">For more information, see [Fixed assets integration](fixed-asset-integration.md).</span></span>




