---
title: 采购订单故障排除
description: 本主题介绍如何解决在使用采购订单时可能遇到的问题。
author: SmithaNataraj
manager: tfehr
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 234458f865e37a2d962aee8ab218b9521847081d
ms.sourcegitcommit: e3f4dd2257a3255c2982f4fc7b72a1121275b88a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4018552"
---
# <a name="troubleshoot-purchase-orders"></a><span data-ttu-id="3497b-103">采购订单故障排除</span><span class="sxs-lookup"><span data-stu-id="3497b-103">Troubleshoot purchase orders</span></span>

<span data-ttu-id="3497b-104">本主题介绍如何解决在使用采购订单时可能遇到的问题。</span><span class="sxs-lookup"><span data-stu-id="3497b-104">This topic describes how to fix issues that you might encounter while you work with purchase orders.</span></span>

## <a name="an-action-can-be-completed-only-after-the-line-number-is-fully-distributed"></a><span data-ttu-id="3497b-105">仅在完全分配行号之后才能完成操作。</span><span class="sxs-lookup"><span data-stu-id="3497b-105">An action can be completed only after the line number is fully distributed.</span></span>

<span data-ttu-id="3497b-106">发生此问题可能是由于采购订单分配不一致。</span><span class="sxs-lookup"><span data-stu-id="3497b-106">This issue can occur because of inconsistency in purchase order distributions.</span></span>

<span data-ttu-id="3497b-107">要解决此问题并将采购订单重置为 *草稿* 状态，请转到 **采购 \> 定期任务 \> 清除 \> 采购订单分配重置** 。</span><span class="sxs-lookup"><span data-stu-id="3497b-107">To unblock this issue and reset the purchase order to a *Draft* state, go to **Procurement and sourcing \> Periodic tasks \> Clean up \> Purchase order distribution reset**.</span></span> <span data-ttu-id="3497b-108">有关详细信息，请参阅以下博客文章：[解决 Dynamics 365 Supply Chain Management 中的采购订单分配错误](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/)。</span><span class="sxs-lookup"><span data-stu-id="3497b-108">For more information, see the following blog post: [Resolve PO distribution errors in Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span></span>

## <a name="when-purchase-orders-are-imported-through-data-management-purchase-order-line-numbers-dont-follow-the-increment-that-defined-in-system-parameters"></a><span data-ttu-id="3497b-109">通过数据管理导入采购订单时，采购订单行号不遵循系统参数中定义的增量。</span><span class="sxs-lookup"><span data-stu-id="3497b-109">When purchase orders are imported through data management, purchase order line numbers don't follow the increment that defined in system parameters.</span></span>

### <a name="issue-description"></a><span data-ttu-id="3497b-110">问题描述</span><span class="sxs-lookup"><span data-stu-id="3497b-110">Issue description</span></span>

<span data-ttu-id="3497b-111">默认情况下，通过 *采购订单行 V2* 数据实体导入的采购订单行的自动生成的行号不使用系统参数中指定的系统行号增量。</span><span class="sxs-lookup"><span data-stu-id="3497b-111">By default, automatically generated line numbers for purchase order lines that are imported through the *Purchase order lines V2* data entity don't use the system line number increment that is specified in system parameters.</span></span> <span data-ttu-id="3497b-112">如果您手动创建采购订单并通过用户界面 (UI) 添加行，行号会正确递增。</span><span class="sxs-lookup"><span data-stu-id="3497b-112">If you manually create a purchase order and add lines through the user interface (UI), the line numbers are incremented correctly.</span></span> <span data-ttu-id="3497b-113">但是，如果您使用数据管理框架 (DMF)，则不会正确递增。</span><span class="sxs-lookup"><span data-stu-id="3497b-113">However, if you use the Data management framework (DMF), they aren't incremented correctly.</span></span>

<span data-ttu-id="3497b-114">发生此问题的原因是，当您通过 DMF 导入行时，如果在导入的实体中尚未分配行号，系统将使用 DMF 的方法进行分配。</span><span class="sxs-lookup"><span data-stu-id="3497b-114">This issue occurs because, when you import lines via DMF, if line numbers aren't already assigned in the imported entity, the system uses DMF's method for assigning them.</span></span> <span data-ttu-id="3497b-115">该方法始终将行号加 1。</span><span class="sxs-lookup"><span data-stu-id="3497b-115">That method always increments line numbers by one.</span></span>

### <a name="issue-workaround"></a><span data-ttu-id="3497b-116">问题解决方法</span><span class="sxs-lookup"><span data-stu-id="3497b-116">Issue workaround</span></span>

<span data-ttu-id="3497b-117">导入采购订单行时，请确保已在数据实体行号字段中提供了所需的行号。</span><span class="sxs-lookup"><span data-stu-id="3497b-117">Make sure that the desired line numbers are already given in the data entity line number fields when you import the purchase order lines.</span></span> <span data-ttu-id="3497b-118">在这种情况下，DMF 不会覆盖行号。</span><span class="sxs-lookup"><span data-stu-id="3497b-118">In this case, DMF won't overwrite the line numbers.</span></span>

## <a name="a-default-tax-group-and-a-default-cash-discount-arent-filled-in-from-the-invoice-account"></a><span data-ttu-id="3497b-119">未在发票帐户中填充默认税组和默认现金折扣。</span><span class="sxs-lookup"><span data-stu-id="3497b-119">A default tax group and a default cash discount aren't filled in from the invoice account.</span></span>

<span data-ttu-id="3497b-120">如果您使用与客户帐户不同的发票帐户，在创建采购订单时不会在发票帐户中填充默认税组和默认现金折扣。</span><span class="sxs-lookup"><span data-stu-id="3497b-120">If you're using an invoice account that differs from the customer account, a default tax group and a default cash discount aren't filled in from the invoice account when a purchase order is created.</span></span>

<span data-ttu-id="3497b-121">此为有意行为。</span><span class="sxs-lookup"><span data-stu-id="3497b-121">This behavior is by design.</span></span> <span data-ttu-id="3497b-122">税组、现金折扣和其他价格信息的默认值基于客户帐户，而不是发票帐户。</span><span class="sxs-lookup"><span data-stu-id="3497b-122">The default values for the tax group, cash discounts, and other price information are based on the customer account, not the invoice account.</span></span>

## <a name="i-receive-an-object-reference-not-set-error-during-purchase-order-confirmation-or-an-exception-has-been-thrown-by-the-target-of-an-invocation-exception-occurs-during-vendor-invoice-posting"></a><span data-ttu-id="3497b-123">我在采购订单确认期间收到“未设置对象引用”错误，或在供应商发票过帐期间发生了“调用目标引发异常”异常。</span><span class="sxs-lookup"><span data-stu-id="3497b-123">I receive an "Object reference not set" error during purchase order confirmation, or an "Exception has been thrown by the target of an invocation" exception occurs during vendor invoice posting.</span></span>

<span data-ttu-id="3497b-124">发生此问题可能是由于采购订单分配不一致。</span><span class="sxs-lookup"><span data-stu-id="3497b-124">This issue can occur because of inconsistency in purchase order distributions.</span></span>

<span data-ttu-id="3497b-125">要解决此问题并将采购订单重置为 *草稿* 状态，请转到 **采购 \> 定期任务 \> 清除 \> 采购订单分配重置** 。</span><span class="sxs-lookup"><span data-stu-id="3497b-125">To unblock this issue and reset the purchase order to a *Draft* state, go to **Procurement and sourcing \> Periodic tasks \> Clean up \> Purchase order distribution reset**.</span></span> <span data-ttu-id="3497b-126">有关详细信息，请参阅以下博客文章：[解决 Dynamics 365 Supply Chain Management 中的采购订单分配错误](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/)。</span><span class="sxs-lookup"><span data-stu-id="3497b-126">For more information, see the following blog post: [Resolve PO distribution errors in Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span></span>

## <a name="one-or-more-accounting-distributions-are-either-over-distributed-or-under-distributed"></a><span data-ttu-id="3497b-127">一个或多个会计分配分配过多或分配不足。</span><span class="sxs-lookup"><span data-stu-id="3497b-127">One or more accounting distributions are either over-distributed or under-distributed.</span></span>

### <a name="issue-description"></a><span data-ttu-id="3497b-128">问题描述</span><span class="sxs-lookup"><span data-stu-id="3497b-128">Issue description</span></span>

<span data-ttu-id="3497b-129">您收到以下错误：“一个或多个会计分配分配过多或分配不足。”</span><span class="sxs-lookup"><span data-stu-id="3497b-129">You receive the following error: "One or more accounting distributions is either over-distributed or under-distributed."</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="3497b-130">解决问题</span><span class="sxs-lookup"><span data-stu-id="3497b-130">Issue resolution</span></span>

<span data-ttu-id="3497b-131">发生此问题可能是由于采购订单分配不一致。</span><span class="sxs-lookup"><span data-stu-id="3497b-131">This issue can occur because of inconsistency in purchase order distributions.</span></span>

<span data-ttu-id="3497b-132">要解决此问题并将采购订单重置为 *草稿* 状态，请转到 **采购 \> 定期任务 \> 清除 \> 采购订单分配重置** 。</span><span class="sxs-lookup"><span data-stu-id="3497b-132">To unblock this issue and reset the purchase order to a *Draft* state, go to **Procurement and sourcing \> Periodic tasks \> Clean up \> Purchase order distribution reset**.</span></span> <span data-ttu-id="3497b-133">有关详细信息，请参阅以下博客文章：[解决 Dynamics 365 Supply Chain Management 中的采购订单分配错误](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/)。</span><span class="sxs-lookup"><span data-stu-id="3497b-133">For more information, see the following blog post: [Resolve PO distribution errors in Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span></span>

## <a name="can-i-show-only-purchase-orders-that-i-created"></a><span data-ttu-id="3497b-134">我可以只显示我创建的采购订单吗？</span><span class="sxs-lookup"><span data-stu-id="3497b-134">Can I show only purchase orders that I created?</span></span>

<span data-ttu-id="3497b-135">此功能当前不可用。</span><span class="sxs-lookup"><span data-stu-id="3497b-135">This functionality isn't currently available.</span></span>

## <a name="can-i-reserve-inventory-and-create-transactions-against-registered-inventory-on-a-purchase-order"></a><span data-ttu-id="3497b-136">我可以针对采购订单上的已登记库存预留库存和创建交易吗？</span><span class="sxs-lookup"><span data-stu-id="3497b-136">Can I reserve inventory and create transactions against registered inventory on a purchase order?</span></span>

### <a name="issue-description"></a><span data-ttu-id="3497b-137">问题描述</span><span class="sxs-lookup"><span data-stu-id="3497b-137">Issue description</span></span>

<span data-ttu-id="3497b-138">即使物料在采购订单上处于 *已登记* 状态，您仍然可以预留库存。</span><span class="sxs-lookup"><span data-stu-id="3497b-138">Even when items are in a *Registered* state on a purchase order, you can still reserve the inventory.</span></span> <span data-ttu-id="3497b-139">换言之，您可以针对已登记的库存创建交易记录。</span><span class="sxs-lookup"><span data-stu-id="3497b-139">In other words, you can create transactions against the registered inventory.</span></span>

### <a name="reproduce-the-issue"></a><span data-ttu-id="3497b-140">重现问题</span><span class="sxs-lookup"><span data-stu-id="3497b-140">Reproduce the issue</span></span>

<span data-ttu-id="3497b-141">以下过程显示了一种重现此问题的方法。</span><span class="sxs-lookup"><span data-stu-id="3497b-141">The following procedure shows one way to reproduce the issue.</span></span>

1. <span data-ttu-id="3497b-142">创建采购订单。</span><span class="sxs-lookup"><span data-stu-id="3497b-142">Create a purchase order.</span></span>
2. <span data-ttu-id="3497b-143">登记采购订单行。</span><span class="sxs-lookup"><span data-stu-id="3497b-143">Register the purchase order line.</span></span>
3. <span data-ttu-id="3497b-144">请注意，您可以针对已登记的库存生成预留或交易。</span><span class="sxs-lookup"><span data-stu-id="3497b-144">Notice that you can generate reservations or transactions against the registered inventory.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="3497b-145">解决问题</span><span class="sxs-lookup"><span data-stu-id="3497b-145">Issue resolution</span></span>

<span data-ttu-id="3497b-146">此为有意行为。</span><span class="sxs-lookup"><span data-stu-id="3497b-146">This behavior is by design.</span></span> <span data-ttu-id="3497b-147">预期是已登记的物料已实际到达仓库或库存，因此可以预留。</span><span class="sxs-lookup"><span data-stu-id="3497b-147">The expectation is that the registered items have physically arrived in the warehouse or inventory, and that they are therefore available for reservation.</span></span>

## <a name="purchase-orders-dont-reflect-the-language-settings-of-the-legal-entity"></a><span data-ttu-id="3497b-148">采购订单不反映法人的语言设置。</span><span class="sxs-lookup"><span data-stu-id="3497b-148">Purchase orders don't reflect the language settings of the legal entity.</span></span>

### <a name="issue-description"></a><span data-ttu-id="3497b-149">问题描述</span><span class="sxs-lookup"><span data-stu-id="3497b-149">Issue description</span></span>

<span data-ttu-id="3497b-150">采购订单上的产品名称以系统语言显示，而不是为创建采购订单的法人设置的语言。</span><span class="sxs-lookup"><span data-stu-id="3497b-150">The product name on a purchase order is shown in the system language instead of the language that is set for the legal entity where the purchase order was created.</span></span>

### <a name="reproduce-the-issue"></a><span data-ttu-id="3497b-151">重现问题</span><span class="sxs-lookup"><span data-stu-id="3497b-151">Reproduce the issue</span></span>

<span data-ttu-id="3497b-152">以下过程显示了一种重现此问题的方法。</span><span class="sxs-lookup"><span data-stu-id="3497b-152">The following procedure shows one way to reproduce the issue.</span></span>

1. <span data-ttu-id="3497b-153">将系统语言设置为 *EN-US* （美国英语）。</span><span class="sxs-lookup"><span data-stu-id="3497b-153">Set the system language to *EN-US* (US English).</span></span>
1. <span data-ttu-id="3497b-154">确保有一个产品保留了 *EN-US* 和 *DE* （德语）语言来翻译产品名称。</span><span class="sxs-lookup"><span data-stu-id="3497b-154">Make sure that there is a product where the *EN-US* and *DE* (German) languages are maintained for translations of the product name.</span></span>
1. <span data-ttu-id="3497b-155">将法人的语言更改为 *DE* 。</span><span class="sxs-lookup"><span data-stu-id="3497b-155">Change the language of a legal entity to *DE*.</span></span>
1. <span data-ttu-id="3497b-156">在将 *DE* 设置为语言的法人中，创建包含该产品的采购订单。</span><span class="sxs-lookup"><span data-stu-id="3497b-156">In the legal entity where *DE* is set as the language, create a purchase order that includes the product.</span></span>
1. <span data-ttu-id="3497b-157">请注意，产品名称仍以美国英语（系统语言）显示。</span><span class="sxs-lookup"><span data-stu-id="3497b-157">Notice that the product name is still shown in US English (the system language).</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="3497b-158">解决问题</span><span class="sxs-lookup"><span data-stu-id="3497b-158">Issue resolution</span></span>

<span data-ttu-id="3497b-159">此为有意行为。</span><span class="sxs-lookup"><span data-stu-id="3497b-159">This behavior is by design.</span></span> <span data-ttu-id="3497b-160">在采购订单上，产品始终以系统语言显示。</span><span class="sxs-lookup"><span data-stu-id="3497b-160">On purchase orders, the product is always shown in the system language.</span></span> <span data-ttu-id="3497b-161">创建确认日记帐时将使用采购订单语言。</span><span class="sxs-lookup"><span data-stu-id="3497b-161">The purchase order language is used when a confirmation journal is created.</span></span>

## <a name="the-approved-vendor-list-by-product-entity-doesnt-allow-the-effective-date-to-be-changed"></a><span data-ttu-id="3497b-162">按产品实体列出的核准供应商列表不允许更改生效日期。</span><span class="sxs-lookup"><span data-stu-id="3497b-162">The Approved vendor list by product entity doesn't allow the effective date to be changed.</span></span>

### <a name="issue-description"></a><span data-ttu-id="3497b-163">问题描述</span><span class="sxs-lookup"><span data-stu-id="3497b-163">Issue description</span></span>

<span data-ttu-id="3497b-164">例如，产品有生效日期为 2018 年 1 月 11 日 ( *01/11/2018* )，到期日期为 *从不* 的核准供应商。</span><span class="sxs-lookup"><span data-stu-id="3497b-164">A product has an approved vendor that has, for example, an effective date of January 11, 2018 ( *01/11/2018* ), and an expiration date of *Never*.</span></span> <span data-ttu-id="3497b-165">如果您尝试将生效日期更改为 2018 年 1 月 10 日 ( *01/10/2018* ) 或 2018 年 1 月 12 日 ( *01/12/2018* )，将收到以下错误：</span><span class="sxs-lookup"><span data-stu-id="3497b-165">If you try to change the effective date to January 10, 2018 ( *01/10/2018* ), or January 12, 2018 ( *01/12/2018* ), you receive the following error:</span></span>

> <span data-ttu-id="3497b-166">无法在核准供应商列表 (PdsApproveVendorList) 中创建记录。</span><span class="sxs-lookup"><span data-stu-id="3497b-166">Cannot create a record in Approved supplier list (PdsApproveVendorList).</span></span> <span data-ttu-id="3497b-167">“到期”值必须大于或等于“生效”值。</span><span class="sxs-lookup"><span data-stu-id="3497b-167">The 'Expiration' value needs to be greater than or equal to the 'Effective' value.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="3497b-168">解决问题</span><span class="sxs-lookup"><span data-stu-id="3497b-168">Issue resolution</span></span>

<span data-ttu-id="3497b-169">您只能延长供应商的核准期限。</span><span class="sxs-lookup"><span data-stu-id="3497b-169">You can only extend the period that the vendor is approved for.</span></span> <span data-ttu-id="3497b-170">下列规则适用：</span><span class="sxs-lookup"><span data-stu-id="3497b-170">The following rules apply:</span></span>

- <span data-ttu-id="3497b-171">要更改生效日期，使其早于物料供应商的任何现有记录（期限），新期间的到期日期必须早于现有记录中的所有到期日期。</span><span class="sxs-lookup"><span data-stu-id="3497b-171">To change the effective date so that it's earlier than any of the existing records (periods) for the item vendor, the expiration date of the new period must be before all the expiration dates in the existing records.</span></span>
- <span data-ttu-id="3497b-172">若要更改到期日期，使其晚于任何现有期限，生效日期必须在任何现有记录中的最新到期日期之后。</span><span class="sxs-lookup"><span data-stu-id="3497b-172">To change the expiration date so that it's later than any of the existing periods, the effective date must be after the latest expiration date in any existing record.</span></span>
- <span data-ttu-id="3497b-173">要减少供应商的总核准期限，必须删除或修改现有记录。</span><span class="sxs-lookup"><span data-stu-id="3497b-173">To reduce the overall period that the vendor is approved for, you must delete or modify existing records.</span></span> <span data-ttu-id="3497b-174">或者，您可以在导入期间使用 **截断** 切换。</span><span class="sxs-lookup"><span data-stu-id="3497b-174">Alternatively, you can use the **truncate** switch during import.</span></span> <span data-ttu-id="3497b-175">此切换按物料删除表中核准供应商的所有现有记录。</span><span class="sxs-lookup"><span data-stu-id="3497b-175">This switch deletes all existing records in the table for approved vendors by item.</span></span>

<span data-ttu-id="3497b-176">对于问题描述中描述的示例场景：记录的生效日期为 *01/11/2018* ，到期日期为 *从不* ，可以导入生效日期为 *01/10/2018* 、到期日期为 *从不* 的新记录。</span><span class="sxs-lookup"><span data-stu-id="3497b-176">For the example scenario that is described in the issue description, where a record has an effective date of *01/11/2018* and an expiration date of *Never* , you can import a new record that has an effective date of *01/10/2018* and an expiration date of *Never*.</span></span> <span data-ttu-id="3497b-177">但是，您无法通过数据管理缩短期限，让生效日期更新为 *01/12/2018* 。</span><span class="sxs-lookup"><span data-stu-id="3497b-177">However, you can't reduce the period so that the effective date is updated to *01/12/2018* via data management.</span></span> <span data-ttu-id="3497b-178">您必须通过 UI 进行此更改。</span><span class="sxs-lookup"><span data-stu-id="3497b-178">You must make this change through the UI.</span></span>

## <a name="after-i-change-the-delivery-address-on-a-purchase-order-header-the-delivery-nameisnt-synced"></a><span data-ttu-id="3497b-179">我更改采购订单标题上的交货地址后，交货名称没有同步。</span><span class="sxs-lookup"><span data-stu-id="3497b-179">After I change the delivery address on a purchase order header, the delivery name isn't synced.</span></span>

### <a name="issue-description"></a><span data-ttu-id="3497b-180">问题描述</span><span class="sxs-lookup"><span data-stu-id="3497b-180">Issue description</span></span>

<span data-ttu-id="3497b-181">采购订单标题上的地址将更新为不是交货地址的地址。</span><span class="sxs-lookup"><span data-stu-id="3497b-181">The address on the header of a purchase order is updated to an address that isn't a delivery address.</span></span> <span data-ttu-id="3497b-182">虽然地址在采购订单上已更新，但交货名称不会根据更新的地址进行更新。</span><span class="sxs-lookup"><span data-stu-id="3497b-182">Although the address is updated on the purchase order, the delivery name isn't updated based on the updated address.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="3497b-183">解决问题</span><span class="sxs-lookup"><span data-stu-id="3497b-183">Issue resolution</span></span>

<span data-ttu-id="3497b-184">此为有意行为。</span><span class="sxs-lookup"><span data-stu-id="3497b-184">This behavior is by design.</span></span> <span data-ttu-id="3497b-185">所选地址必须分类为交货地址。</span><span class="sxs-lookup"><span data-stu-id="3497b-185">The selected address must be classified as a delivery address.</span></span> <span data-ttu-id="3497b-186">否则，交货名称不会根据所选地址更新。</span><span class="sxs-lookup"><span data-stu-id="3497b-186">Otherwise, the delivery name isn't updated based on the selected address.</span></span>

## <a name="can-i-find-the-user-who-canceled-a-purchase-order"></a><span data-ttu-id="3497b-187">我可以找到取消采购订单的用户吗？</span><span class="sxs-lookup"><span data-stu-id="3497b-187">Can I find the user who canceled a purchase order?</span></span>

<span data-ttu-id="3497b-188">仅当采购订单接受更改管理时，才会跟踪此信息。</span><span class="sxs-lookup"><span data-stu-id="3497b-188">This information is tracked only if the purchase order is subject to change management.</span></span> <span data-ttu-id="3497b-189">如果使用更改管理，您可以查看谁提交了更改（取消）以及谁批准了更改。</span><span class="sxs-lookup"><span data-stu-id="3497b-189">If you use change management, you can see who submitted the change (the cancellation), and who approved it.</span></span>
