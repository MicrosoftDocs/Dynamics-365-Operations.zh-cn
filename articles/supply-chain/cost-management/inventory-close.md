---
title: 库存结转
description: 作为结算具有收货交易记录的发货交易记录的流程的一部分，您还可以选择更新总帐以反映已进行的调整。
author: AndersGirke
manager: tfehr
ms.date: 04/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventClosing
audience: Application User
ms.reviewer: kamaybac
ms.custom: 61973
ms.assetid: c210c882-6849-4704-b78c-a777dd6cfdb6
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9fc06806c14539de913f2336f2adb7462f303f37
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5220864"
---
# <a name="inventory-close"></a><span data-ttu-id="750eb-103">库存结转</span><span class="sxs-lookup"><span data-stu-id="750eb-103">Inventory close</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="750eb-104">作为结算具有收货交易记录的发货交易记录的流程的一部分，您还可以选择更新总帐以反映已进行的调整。</span><span class="sxs-lookup"><span data-stu-id="750eb-104">As part of the process to settle issue transactions with receipt transactions, you can also choose to have the general ledger updated to reflect the adjustments that have been made.</span></span>

<span data-ttu-id="750eb-105">库存结转过程基于在物料的物料模型组中选择的库存评估方法将发货交易记录结算到收货交易记录。</span><span class="sxs-lookup"><span data-stu-id="750eb-105">The inventory close process settles issue transactions to receipt transactions, based on the inventory valuation method that is selected in the item’s item model group.</span></span> <span data-ttu-id="750eb-106">作为结算流程的一部分，您可以指定应更新总帐，以便它反映已进行的调整。</span><span class="sxs-lookup"><span data-stu-id="750eb-106">As part of the settlement process, you can specify that the general ledger should be updated, so that it reflects the adjustments that have been made.</span></span> <span data-ttu-id="750eb-107">但在运行库存结转或重新计算前， 将按计算的移动平均成本价过帐发货交易记录。</span><span class="sxs-lookup"><span data-stu-id="750eb-107">However, until inventory close or recalculation has been run, issue transactions are posted at the calculated running average cost price.</span></span> 

<span data-ttu-id="750eb-108">在库存结转后，无法再在您设置的库存结帐日期前的期间中过帐，除非您冲销已完成的库存结转过程。</span><span class="sxs-lookup"><span data-stu-id="750eb-108">After inventory close, you can no longer post in periods that are before the inventory closing date that you set, unless you reverse a completed inventory close process.</span></span> <span data-ttu-id="750eb-109">例如，如果，库存结转为 1 月 31 日结束的期间运行，您不能过帐具有早于 1 月 31 日的日期的交易记录。</span><span class="sxs-lookup"><span data-stu-id="750eb-109">For example, if inventory close is run for the period that ends on January 31, you can't post transactions that have a date that is earlier than January 31.</span></span> 

<span data-ttu-id="750eb-110">将库存中的物料分配至两个库存类型之一:物料或服务。</span><span class="sxs-lookup"><span data-stu-id="750eb-110">Items in inventory are assigned to one of two inventory types: item or service.</span></span> <span data-ttu-id="750eb-111">执行库存结转为这两种类型执行相同的功能。</span><span class="sxs-lookup"><span data-stu-id="750eb-111">Inventory close performs the same functions for both types.</span></span> <span data-ttu-id="750eb-112">但是，对于服务物料，库存结转仍将发货结算到收货。</span><span class="sxs-lookup"><span data-stu-id="750eb-112">However, for service items, inventory close still settles issues to receipts.</span></span> 

<span data-ttu-id="750eb-113">公司不同，执行库存结转的频率也有所不同。</span><span class="sxs-lookup"><span data-stu-id="750eb-113">How often the inventory close process is run varies by company.</span></span> <span data-ttu-id="750eb-114">但交易量将对您选择运行库存结转的频率产生影响。</span><span class="sxs-lookup"><span data-stu-id="750eb-114">However, transaction volume should help determine how often you decide to run inventory close.</span></span> <span data-ttu-id="750eb-115">通常，大多数公司将库存结转作为其月末结转和对帐过程的一部分运行。</span><span class="sxs-lookup"><span data-stu-id="750eb-115">In general, most companies run inventory close as part of their month-end close and reconciliation procedures.</span></span>

## <a name="inventory-recalculation-and-the-general-ledger"></a><span data-ttu-id="750eb-116">库存重新计算和总帐</span><span class="sxs-lookup"><span data-stu-id="750eb-116">Inventory recalculation and the general ledger</span></span>
<span data-ttu-id="750eb-117">如果在一个月或其他库存期间需要对库存和总帐进行调整，则您可以执行库存重新计算，而非库存结转。</span><span class="sxs-lookup"><span data-stu-id="750eb-117">If adjustments to inventory and the general ledger are required during a month or other inventory period, you can run inventory recalculation instead of inventory close.</span></span> <span data-ttu-id="750eb-118">库存重新计算会对库存交易记录进行调整，但不结算。</span><span class="sxs-lookup"><span data-stu-id="750eb-118">Inventory recalculation makes adjustments but doesn't make settlements to inventory transactions.</span></span> 

<span data-ttu-id="750eb-119">在库存重新计算时，调整现有库存量，调整库存交易记录，并且，运行库存重新计算和库存结转。</span><span class="sxs-lookup"><span data-stu-id="750eb-119">During inventory recalculation, on-hand inventory is adjusted, inventory transactions are adjusted, and inventory recalculations and inventory closes are run.</span></span> <span data-ttu-id="750eb-120">受这些任务影响的任何会计科目是那些链接到原始库存交易记录的会计科目。</span><span class="sxs-lookup"><span data-stu-id="750eb-120">These tasks affect any ledger account that is linked to the original inventory transaction.</span></span> 

<span data-ttu-id="750eb-121">**示例**</span><span class="sxs-lookup"><span data-stu-id="750eb-121">**Example**</span></span> 

<span data-ttu-id="750eb-122">在您从销售订单创建采购订单，总帐科目用于更新原始销售订单。</span><span class="sxs-lookup"><span data-stu-id="750eb-122">When you create a purchase order from a sales order, the general ledger accounts that are used for the original sales order are updated.</span></span> <span data-ttu-id="750eb-123">即使分配给此物料的物料组上的会计科目自从过帐销售订单后已更改，并且库存重新计算创建调整金额，该调整金额也仍将过帐到原始会计科目。</span><span class="sxs-lookup"><span data-stu-id="750eb-123">Even if the ledger accounts for the item group that is assigned to the item were changed after the sales order was posted, and an inventory recalculation created an adjustment amount, the adjustment amount is posted to the original ledger accounts.</span></span> <span data-ttu-id="750eb-124">调整的金额不过帐到分配给该物料的新会计科目。</span><span class="sxs-lookup"><span data-stu-id="750eb-124">The adjusted amount isn’t posted to the new ledger accounts that are assigned to the item.</span></span> 

<span data-ttu-id="750eb-125">在更新完成后，您可以查看由于其中某个任务而过帐的分类帐凭证。</span><span class="sxs-lookup"><span data-stu-id="750eb-125">After the update is completed, you can review the ledger voucher that is posted because of one of these tasks.</span></span>

1.  <span data-ttu-id="750eb-126">在 **结转与调整** 页上，在 **概览** 选项卡上，选中更新以进行审核。</span><span class="sxs-lookup"><span data-stu-id="750eb-126">On the **Closing and adjustment** page, on the **Overview** tab, select the update to review.</span></span>
2.  <span data-ttu-id="750eb-127">单击 **详细信息**，然后选择 **凭证**。</span><span class="sxs-lookup"><span data-stu-id="750eb-127">Click **Details**, and then select **Voucher**.</span></span>

## <a name="effects-of-the-inventory-close-process-on-the-general-ledger"></a><span data-ttu-id="750eb-128">总帐中库存结转流程的效果</span><span class="sxs-lookup"><span data-stu-id="750eb-128">Effects of the inventory close process on the general ledger</span></span>
<span data-ttu-id="750eb-129">您可以在 **结转与调整** 页中执行的若干任务将导致对总帐进行更新。</span><span class="sxs-lookup"><span data-stu-id="750eb-129">Several of the tasks that you can perform on the **Closing and adjustment** page cause an update to general ledger.</span></span> <span data-ttu-id="750eb-130">例如，当您进行现有库存量调整，进行库存交易记录调整，执行库存重新计算，以及执行库存结转时，将更新总帐。</span><span class="sxs-lookup"><span data-stu-id="750eb-130">For example, the general ledger is updated when you make inventory on-hand adjustments, make inventory transaction adjustments, run inventory recalculation, and run inventory close.</span></span> 

<span data-ttu-id="750eb-131">因为这些任务更新的会计科目链接到原始库存交易记录的会计科目。</span><span class="sxs-lookup"><span data-stu-id="750eb-131">The ledger accounts that are updated because of these tasks are linked to the original inventory transaction.</span></span> <span data-ttu-id="750eb-132">例如，如果某一销售订单结算到某一采购订单，则调整已用于原始销售订单的总帐科目。</span><span class="sxs-lookup"><span data-stu-id="750eb-132">For example, if a sales order is settled to a purchase order, the general ledger accounts that were used for the original sales order are adjusted.</span></span> <span data-ttu-id="750eb-133">即便分配给此物料的物料组的会计科目自过账销售订单后已更改也将发生此行为。</span><span class="sxs-lookup"><span data-stu-id="750eb-133">This behavior occurs even if the ledger accounts for the item group that is assigned to the item have changed since the sales order was posted.</span></span> <span data-ttu-id="750eb-134">在库存结转创建了一个结算金额后，该结算金额仍然会过帐到原始会计科目，而不是过帐到分配给物料的新会计科目。</span><span class="sxs-lookup"><span data-stu-id="750eb-134">After inventory close creates a settlement amount, the settlement amount is still posted to the original ledger accounts, not to the new ledger accounts that are assigned to the item.</span></span> <span data-ttu-id="750eb-135">如果您冲销库存结转，总帐也将更新。</span><span class="sxs-lookup"><span data-stu-id="750eb-135">The general ledger might also be updated if you reverse an inventory close.</span></span> 

> [!NOTE] 
> - <span data-ttu-id="750eb-136">对于除移动平均以外的所有库存模型，库存结转是月末结转过程中的必需步骤。</span><span class="sxs-lookup"><span data-stu-id="750eb-136">Inventory close is a required step in the month-end closing procedure for all inventory models except moving average.</span></span>  <span data-ttu-id="750eb-137">如果您尝试关闭财务期间而未在期间结束日期之前先执行库存结转操作，系统会警告您。</span><span class="sxs-lookup"><span data-stu-id="750eb-137">You will be warned if you try to close a financial period without first performing the inventory close as of the period end date.</span></span>
> - <span data-ttu-id="750eb-138">在运行结转过程前，您可以查看在更新期间无法结算的一组物料。</span><span class="sxs-lookup"><span data-stu-id="750eb-138">Before you run the closing procedure, you can view a list of items that can't be settled during the update.</span></span>
> - <span data-ttu-id="750eb-139">我们建议您在低谷时间执行库存结转，从而更平均地分配计算机资源。</span><span class="sxs-lookup"><span data-stu-id="750eb-139">We recommend that you run inventory close during off-peak hours, to distribute computing resources more evenly.</span></span>

## <a name="the-inventory-close-log"></a><span data-ttu-id="750eb-140">库存结转日志</span><span class="sxs-lookup"><span data-stu-id="750eb-140">The inventory close log</span></span>
<span data-ttu-id="750eb-141">在完成库存结转流程后，因为某一交易记录无法完全结算，消息中心的消息可能通知您成本价可能错误。</span><span class="sxs-lookup"><span data-stu-id="750eb-141">After the inventory close process has been completed, a message in the message center might inform you that a unit cost price might be incorrect because a transaction could not be fully settled.</span></span> 

<span data-ttu-id="750eb-142">在显示此消息前，此系统将报告物料编号和影响的交易记录。</span><span class="sxs-lookup"><span data-stu-id="750eb-142">Before this message is shown, the system reports the item number and the affected transaction.</span></span> <span data-ttu-id="750eb-143">此消息通知您由于库存结转用于此交易记录的成本额没有更新。</span><span class="sxs-lookup"><span data-stu-id="750eb-143">The message informs you that the cost amount that is used for this transaction wasn't updated because of the inventory close.</span></span> <span data-ttu-id="750eb-144">在无法结算某一发货类型交易记录时出现此消息。</span><span class="sxs-lookup"><span data-stu-id="750eb-144">This message appears when a transaction of the issue type can't be settled.</span></span> 

<span data-ttu-id="750eb-145">在库存结转过程中，系统检查每个财务维度以了解是否存在发货超过收货的情况，截至指定结转日期。</span><span class="sxs-lookup"><span data-stu-id="750eb-145">During the inventory close process, the system checks each financial dimension to see whether there are more issues than receipts up to the specified closing date.</span></span> <span data-ttu-id="750eb-146">因为尚未接收供应商发票，或者因为在更高级别上的生产中包括的物料清单分项未在财务上过帐，未完全从财务上过帐来自采购订单的库存交易记录时不平衡的类型可以发生。</span><span class="sxs-lookup"><span data-stu-id="750eb-146">This type of imbalance can occur when an inventory transaction from a purchase order isn't fully posted financially, either because the vendor invoice hasn't been received, or because bill of materials (BOM) components that are included in a production on a higher level aren't financially posted.</span></span> <span data-ttu-id="750eb-147">（子生产不是计算的成本。）在这种情况下，则随后的结转不会将所有发货都调整到正确的成本价，因为未提供足够的收货信息。</span><span class="sxs-lookup"><span data-stu-id="750eb-147">(The sub-production isn't cost-calculated.) In this case, the subsequent close won't adjust all issues to the correct cost price, because not enough receipt information is available.</span></span> 

<span data-ttu-id="750eb-148">对于每个结转过程的运行，系统指示是否存储并且可以查看包含警告的日志。</span><span class="sxs-lookup"><span data-stu-id="750eb-148">For each run of the closing procedure, the system indicates whether a log that contains the warnings is stored and can be viewed.</span></span> 

<span data-ttu-id="750eb-149">如果在消息中您收到许多警告，则我们建议您采取以下措施：</span><span class="sxs-lookup"><span data-stu-id="750eb-149">If you receive many warnings in the message, we recommend that you perform the following actions:</span></span>

-   <span data-ttu-id="750eb-150">从财务上更新收货。</span><span class="sxs-lookup"><span data-stu-id="750eb-150">Update receipts financially.</span></span>
-   <span data-ttu-id="750eb-151">将结转日期提前。</span><span class="sxs-lookup"><span data-stu-id="750eb-151">Advance the closing date.</span></span>
-   <span data-ttu-id="750eb-152">重估业务流程。</span><span class="sxs-lookup"><span data-stu-id="750eb-152">Reevaluate the business procedures.</span></span>

<span data-ttu-id="750eb-153">在某些环境中，可能您不能执行有关警告的任何操作。</span><span class="sxs-lookup"><span data-stu-id="750eb-153">In some circumstances, you might not be able to do anything about the warnings.</span></span> <span data-ttu-id="750eb-154">例如，如果使用标记，且标记的采购订单具有的财务日期处于结转日期之后，无法更改结转日期。</span><span class="sxs-lookup"><span data-stu-id="750eb-154">For example, if marking is used, and the marked purchase order has a financial date that is after the closing date, the closing date can't be changed.</span></span>

## <a name="reversing-a-completed-inventory-close"></a><span data-ttu-id="750eb-155">冲销已完成的库存结转</span><span class="sxs-lookup"><span data-stu-id="750eb-155">Reversing a completed inventory close</span></span>
<span data-ttu-id="750eb-156">您偶尔可能必须冲销已完成的库存结转，以将结算返回到执行调整前的状态。</span><span class="sxs-lookup"><span data-stu-id="750eb-156">Occasionally, you might have to reverse a completed inventory close to return settlements to the state that they had before adjustments were made.</span></span> <span data-ttu-id="750eb-157">在您冲销已完成的库存结转时，库存还会重新打开，以可以在库存转结涵盖期间中过帐。</span><span class="sxs-lookup"><span data-stu-id="750eb-157">When you reverse a completed inventory close, inventory is reopened to enable posting in the period that the inventory close covers.</span></span> <span data-ttu-id="750eb-158">也可能在总账中进行相关的更改。</span><span class="sxs-lookup"><span data-stu-id="750eb-158">Related changes might also be made in the general ledger.</span></span> <span data-ttu-id="750eb-159">在完成调整后，您可以为您正在使用的期间再次运行库存结转。</span><span class="sxs-lookup"><span data-stu-id="750eb-159">After you've finished making adjustments, you can run inventory close again for the period that you're working with.</span></span> 

> [!NOTE] 
> <span data-ttu-id="750eb-160">只有最后关闭的库存期间可以重新打开。</span><span class="sxs-lookup"><span data-stu-id="750eb-160">Only the last inventory period that was closed can be reopened.</span></span> <span data-ttu-id="750eb-161">若要冲销更早的库存结转，必须一次冲销一个后续库存，从最近的结转开始。</span><span class="sxs-lookup"><span data-stu-id="750eb-161">To reverse an earlier inventory close, you must reverse each subsequent inventory close one at a time, starting with the most recent close.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]