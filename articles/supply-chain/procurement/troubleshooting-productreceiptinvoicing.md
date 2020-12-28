---
title: 产品收货和开票故障排除
description: 本主题介绍如何解决使用产品收货和开票时可能遇到的问题。
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
ms.openlocfilehash: a89effb686d60dde9d11f99be51d4101897ad4ea
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4423423"
---
# <a name="troubleshoot-product-receipts-and-invoicing"></a><span data-ttu-id="70af4-103">产品收货和开票故障排除</span><span class="sxs-lookup"><span data-stu-id="70af4-103">Troubleshoot product receipts and invoicing</span></span>

<span data-ttu-id="70af4-104">本主题介绍如何解决使用产品收货和开票时可能遇到的问题。</span><span class="sxs-lookup"><span data-stu-id="70af4-104">This topic describes how to fix issues that you might encounter while you work with product receipts and invoicing.</span></span>

## <a name="i-cant-post-more-than-one-invoice-for-a-purchase-order-line-that-has-category-based-items"></a><span data-ttu-id="70af4-105">我无法为有基于类别的物料的采购订单行过帐多个发票。</span><span class="sxs-lookup"><span data-stu-id="70af4-105">I can't post more than one invoice for a purchase order line that has category-based items.</span></span>

<span data-ttu-id="70af4-106">如果要过帐发票，数量是必填项。</span><span class="sxs-lookup"><span data-stu-id="70af4-106">A quantity is mandatory if you want to post invoices.</span></span> <span data-ttu-id="70af4-107">因此，如果仅对一行的全部数量开具了部分金额的发票，您将无法为另一个发票上的其余金额开票。</span><span class="sxs-lookup"><span data-stu-id="70af4-107">Therefore, if the full quantity of a line has been invoiced for only a partial amount, you won't be able to invoice the remaining amount on another invoice.</span></span>

## <a name="i-receive-an-object-reference-not-set-error-during-purchase-order-confirmation-or-an-exception-has-been-thrown-by-the-target-of-an-invocation-exception-occurs-during-vendor-invoice-posting"></a><span data-ttu-id="70af4-108">我在采购订单确认期间收到“未设置对象引用”错误，或在供应商发票过帐期间发生了“调用目标引发异常”异常。</span><span class="sxs-lookup"><span data-stu-id="70af4-108">I receive an "Object reference not set" error during purchase order confirmation, or an "Exception has been thrown by the target of an invocation" exception occurs during vendor invoice posting.</span></span>

<span data-ttu-id="70af4-109">发生此问题可能是由于采购订单分配不一致。</span><span class="sxs-lookup"><span data-stu-id="70af4-109">This issue can occur because of inconsistency in purchase order distributions.</span></span>

<span data-ttu-id="70af4-110">要解决此问题并将采购订单重置为 *草稿* 状态，请转到 **采购 \> 定期任务 \> 清除 \> 采购订单分配重置**。</span><span class="sxs-lookup"><span data-stu-id="70af4-110">To unblock this issue and reset the purchase order to a *Draft* state, go to **Procurement and sourcing \> Periodic tasks \> Clean up \> Purchase order distribution reset**.</span></span> <span data-ttu-id="70af4-111">有关详细信息，请参阅以下博客文章：[解决 Dynamics 365 Supply Chain Management 中的采购订单分配错误](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/)。</span><span class="sxs-lookup"><span data-stu-id="70af4-111">For more information, see the following blog post: [Resolve PO distribution errors in Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span></span>

## <a name="i-cant-consolidate-multiple-product-receipts-into-a-single-purchase-order"></a><span data-ttu-id="70af4-112">我无法将多个产品收货合并到一个采购订单中。</span><span class="sxs-lookup"><span data-stu-id="70af4-112">I can't consolidate multiple product receipts into a single purchase order.</span></span>

<span data-ttu-id="70af4-113">如果不同的产品收货行具有不同的会计日期，则不能将多个产品收货合并到一个采购订单中。</span><span class="sxs-lookup"><span data-stu-id="70af4-113">You can't consolidate multiple product receipts into a single purchase order if the different product receipt lines have different accounting dates.</span></span>

<span data-ttu-id="70af4-114">在早期版本的 Microsoft Dynamics 365 Supply Chain Management 中，这种情况允许合并。</span><span class="sxs-lookup"><span data-stu-id="70af4-114">In earlier versions of Microsoft Dynamics 365 Supply Chain Management, consolidation was allowed in this situation.</span></span> <span data-ttu-id="70af4-115">但是，这种做法很容易出错。</span><span class="sxs-lookup"><span data-stu-id="70af4-115">However, the practice is prone to error.</span></span> <span data-ttu-id="70af4-116">创建的采购订单行上的会计日期应与从其创建这些采购订单行的产品收货行上的会计日期相同。</span><span class="sxs-lookup"><span data-stu-id="70af4-116">The accounting date on the purchase order lines that are created should not differ from the accounting date on the product receipt lines that those purchase order lines were created from.</span></span> <span data-ttu-id="70af4-117">（采购订单行上的会计日期与采购订单标题上的会计日期匹配。）因此，不再允许将多个产品收货合并到一个采购订单中。</span><span class="sxs-lookup"><span data-stu-id="70af4-117">(The accounting date on the purchase order lines matches the accounting date on the purchase order header.) Therefore, the consolidation of multiple product receipts into a single purchase orders is no longer allowed.</span></span>

<span data-ttu-id="70af4-118">例如，会计日期会用于预算预留和保留款。</span><span class="sxs-lookup"><span data-stu-id="70af4-118">The accounting date is used, for example, for budget reservations and encumbrance.</span></span> <span data-ttu-id="70af4-119">因此，应在从产品收货到采购订单的转换期间保留此信息。</span><span class="sxs-lookup"><span data-stu-id="70af4-119">Therefore, it should be kept during the transition from product receipt to purchase order.</span></span>

## <a name="when-product-receipts-are-canceled-transactions-can-be-posted-to-a-suspended-ledger-account"></a><span data-ttu-id="70af4-120">取消产品收货后，可以将交易记录过帐到已暂停的会计科目中。</span><span class="sxs-lookup"><span data-stu-id="70af4-120">When product receipts are canceled, transactions can be posted to a suspended ledger account.</span></span>

### <a name="issue-description"></a><span data-ttu-id="70af4-121">问题描述</span><span class="sxs-lookup"><span data-stu-id="70af4-121">Issue description</span></span>

<span data-ttu-id="70af4-122">如果取消了产品收货，系统将允许将交易记录过帐到已暂停的会计科目中，即使主科目已暂停。</span><span class="sxs-lookup"><span data-stu-id="70af4-122">If a product receipt is canceled, the system allows transactions to be posted to suspended ledger accounts, even though the main accounts are suspended.</span></span>

### <a name="reproduce-the-issue"></a><span data-ttu-id="70af4-123">重现问题</span><span class="sxs-lookup"><span data-stu-id="70af4-123">Reproduce the issue</span></span>

<span data-ttu-id="70af4-124">以下过程显示了一种重现此问题的方法。</span><span class="sxs-lookup"><span data-stu-id="70af4-124">The following procedure shows one way to reproduce the issue.</span></span>

1. <span data-ttu-id="70af4-125">在 **应付帐款参数** 页上的 **常规** 选项卡上，确保将 **在分类帐中对产品收货过帐** 选项设置为 *是*。</span><span class="sxs-lookup"><span data-stu-id="70af4-125">On the **Accounts payable parameters** page, on the **General** tab, make sure that the **Post product receipt in ledger** option is set to *Yes*.</span></span>
1. <span data-ttu-id="70af4-126">创建一个采购订单，并添加产品数量为 *1,000* 的订单行。</span><span class="sxs-lookup"><span data-stu-id="70af4-126">Create a purchase order, and add an order line that has a quantity of *1,000* for a product.</span></span>
1. <span data-ttu-id="70af4-127">确认采购订单。</span><span class="sxs-lookup"><span data-stu-id="70af4-127">Confirm the purchase order.</span></span>
1. <span data-ttu-id="70af4-128">过帐产品收货，并检查凭证。</span><span class="sxs-lookup"><span data-stu-id="70af4-128">Post the product receipt, and check the vouchers.</span></span>
1. <span data-ttu-id="70af4-129">暂停相关的主科目 *200140* 和 *140200*。</span><span class="sxs-lookup"><span data-stu-id="70af4-129">Suspend the relevant main accounts, *200140* and *140200*.</span></span>
1. <span data-ttu-id="70af4-130">取消已过帐的产品收货。</span><span class="sxs-lookup"><span data-stu-id="70af4-130">Cancel the posted product receipt.</span></span>
1. <span data-ttu-id="70af4-131">请注意，可以将交易记录过帐到暂停的会计科目中。</span><span class="sxs-lookup"><span data-stu-id="70af4-131">Notice that transactions can be posted to the suspended leger accounts.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="70af4-132">解决问题</span><span class="sxs-lookup"><span data-stu-id="70af4-132">Issue resolution</span></span>

<span data-ttu-id="70af4-133">取消产品收货后，可以将交易记录过帐到已暂停的会计科目中，因为此行为可进行正确过帐。</span><span class="sxs-lookup"><span data-stu-id="70af4-133">Transactions can be posted to the suspended leger accounts when product receipts are canceled, because this behavior allows for correct postings.</span></span>

## <a name="a-product-receipt-voucher-number-is-consumed-even-if-no-financial-voucher-is-generated-during-product-receipt"></a><span data-ttu-id="70af4-134">即使产品收货期间未生成财务凭证，也会使用产品收货凭证号。</span><span class="sxs-lookup"><span data-stu-id="70af4-134">A product receipt voucher number is consumed even if no financial voucher is generated during product receipt.</span></span>

<span data-ttu-id="70af4-135">如果物料模型组的 **产品收货上的应计负债** 选项设置为 *否*，将不会过帐到总帐。</span><span class="sxs-lookup"><span data-stu-id="70af4-135">If the **Accrue liability on product receipt** option is set to *No* for the item model group, no postings to the general ledger will occur.</span></span> <span data-ttu-id="70af4-136">但是，将在子分类帐中为会计目的记录物理事件，该事件需要凭证号。</span><span class="sxs-lookup"><span data-stu-id="70af4-136">However, a physical event will be recorded for the purpose of accounting in a subledger, and that event requires a voucher number.</span></span> <span data-ttu-id="70af4-137">此凭证号是库存交易记录中引用的凭证号。</span><span class="sxs-lookup"><span data-stu-id="70af4-137">This voucher number is the voucher number that is referenced in the inventory transactions.</span></span>

<span data-ttu-id="70af4-138">我们建议您将 **产品收货上的应计负债** 选项设置为 *是*，如以下博客文章所述：[在产品收货时过帐杂项费用](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/11/11/post-misc-charges-at-time-of-product-receipt/)。</span><span class="sxs-lookup"><span data-stu-id="70af4-138">We recommend that you set the **Accrue liability on product receipt** option to *Yes*, as described in the following blog post: [Post Misc. charges at time of product receipt](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/11/11/post-misc-charges-at-time-of-product-receipt/).</span></span>

## <a name="the-post-to-charge-account-in-ledger-setting-isnt-turned-on"></a><span data-ttu-id="70af4-139">不能打开“过帐到分类帐中的费用帐户”设置。</span><span class="sxs-lookup"><span data-stu-id="70af4-139">The Post to charge account in ledger setting isn't turned on.</span></span>

### <a name="issue-description"></a><span data-ttu-id="70af4-140">问题描述</span><span class="sxs-lookup"><span data-stu-id="70af4-140">Issue description</span></span>

<span data-ttu-id="70af4-141">为采购订单开票时，如果将 **应付帐款参数** 的 **发票** 选项卡上的 **过帐到分类帐中的费用帐户** 选项设置为 *是*，将发生此问题。</span><span class="sxs-lookup"><span data-stu-id="70af4-141">This issue occurs when a purchase order is invoiced, if the **Post to charge account in ledger** option is set to *Yes* on the **Invoice** tab of the **Accounts payable parameters** page.</span></span>

### <a name="reproduce-the-issue"></a><span data-ttu-id="70af4-142">重现问题</span><span class="sxs-lookup"><span data-stu-id="70af4-142">Reproduce the issue</span></span>

<span data-ttu-id="70af4-143">以下过程显示了一种重现此问题的方法。</span><span class="sxs-lookup"><span data-stu-id="70af4-143">The following procedure shows one way to reproduce the issue.</span></span>

1. <span data-ttu-id="70af4-144">转到 **应付帐款 \>设置 \> 应付帐款参数**。</span><span class="sxs-lookup"><span data-stu-id="70af4-144">Go to **Accounts payable \> Setup \> Accounts payable parameters**.</span></span>
1. <span data-ttu-id="70af4-145">在 **发票** 选项卡上，将 **过帐到分类帐中的费用帐户** 选项设置为 *是*。</span><span class="sxs-lookup"><span data-stu-id="70af4-145">On the **Invoice** tab, set the **Post to charge account in ledger** option to *Yes*.</span></span>
1. <span data-ttu-id="70af4-146">转到 **库存管理 \> 设置 \> 过帐 \> 过帐**。</span><span class="sxs-lookup"><span data-stu-id="70af4-146">Go to **Inventory management \> Setup \> Posting \> Posting**.</span></span>
1. <span data-ttu-id="70af4-147">在 **采购订单** 选项卡上，确保已删除产品的采购支出中的所有行。</span><span class="sxs-lookup"><span data-stu-id="70af4-147">On the **Purchase order** tab, make sure that you've deleted all the lines in the purchase expenditure for the product.</span></span>
1. <span data-ttu-id="70af4-148">转到 **应付帐款 \> 采购订单 \> 所有采购订单**。</span><span class="sxs-lookup"><span data-stu-id="70af4-148">Go to **Accounts payable \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="70af4-149">创建采购订单。</span><span class="sxs-lookup"><span data-stu-id="70af4-149">Create a purchase order.</span></span> <span data-ttu-id="70af4-150">在 **供应商帐户** 字段中，选择 *1001 Acme 办公设备*。</span><span class="sxs-lookup"><span data-stu-id="70af4-150">In the **Vendor account** field, select *1001 Acme Office Supplies*.</span></span>
1. <span data-ttu-id="70af4-151">添加具有以下设置的采购订单行：</span><span class="sxs-lookup"><span data-stu-id="70af4-151">Add a purchase order line that has the following settings:</span></span>

    - <span data-ttu-id="70af4-152">**物料编号**：*D0011 激光投影仪*</span><span class="sxs-lookup"><span data-stu-id="70af4-152">**Item number:** *D0011 Laser Projector*</span></span>
    - <span data-ttu-id="70af4-153">**站点**：*1*</span><span class="sxs-lookup"><span data-stu-id="70af4-153">**Site:** *1*</span></span>
    - <span data-ttu-id="70af4-154">**仓库**：*11*</span><span class="sxs-lookup"><span data-stu-id="70af4-154">**Warehouse:** *11*</span></span>
    - <span data-ttu-id="70af4-155">**数量：** *4*</span><span class="sxs-lookup"><span data-stu-id="70af4-155">**Quantity:** *4*</span></span>

1. <span data-ttu-id="70af4-156">在操作窗格的 **采购** 选项卡上，在 **操作** 组中，选择 **确认**。</span><span class="sxs-lookup"><span data-stu-id="70af4-156">On the Action Pane, on the **Purchase** tab, in the **Action** group, select **Confirm**.</span></span>
1. <span data-ttu-id="70af4-157">在操作窗格的 **接收** 选项卡上，在 **生成** 组中，选择 **产品收货**。</span><span class="sxs-lookup"><span data-stu-id="70af4-157">On the Action Pane, on the **Receive** tab, in the **Generate** group, select **Product receipt**.</span></span>
1. <span data-ttu-id="70af4-158">在 **过帐产品收货** 对话框中的 **产品收货** 字段中，输入任意数字，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="70af4-158">In the **Posting product receipt** dialog box, in the **Product receipt** field, enter an arbitrary number, and then select **OK**.</span></span>
1. <span data-ttu-id="70af4-159">在操作窗格 **发票** 选项卡的 **常规** 组中，选择 **发票**。</span><span class="sxs-lookup"><span data-stu-id="70af4-159">On the Action Pane, on the **Invoice** tab, in the **Generate** group, select **Invoice**.</span></span>
1. <span data-ttu-id="70af4-160">在 **编号** 字段中，输入任意数字作为发票编号。</span><span class="sxs-lookup"><span data-stu-id="70af4-160">In the **Number** field, enter an arbitrary number as the invoice number.</span></span>
1. <span data-ttu-id="70af4-161">更新匹配状态，然后过帐。</span><span class="sxs-lookup"><span data-stu-id="70af4-161">Update the match status, and post.</span></span>
1. <span data-ttu-id="70af4-162">请注意，现在从采购订单生成发票时会收到以下错误：“产品的“采购支出”交易类型的科目编号不存在。”</span><span class="sxs-lookup"><span data-stu-id="70af4-162">Notice that you now receive the following error when you generate an invoice from a purchase order: "Account number for transaction type Purchase expenditure for product does not exist."</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="70af4-163">解决问题</span><span class="sxs-lookup"><span data-stu-id="70af4-163">Issue resolution</span></span>

<span data-ttu-id="70af4-164">这取决于发票和发票组的参数设置。</span><span class="sxs-lookup"><span data-stu-id="70af4-164">This depends on the parameter settings for invoices and invoice groups.</span></span> <span data-ttu-id="70af4-165">有关详细信息，请参阅以下博客文章：[采购费用和库存变化的会计](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/12/15/accounting-for-purchase-charge-and-stock-variation/)。</span><span class="sxs-lookup"><span data-stu-id="70af4-165">For more information, see the following blog post: [Accounting for Purchase charge and Stock variation](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/12/15/accounting-for-purchase-charge-and-stock-variation/).</span></span>
