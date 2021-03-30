---
title: 销售订单故障排除
description: 本主题介绍如何解决在使用销售订单时可能遇到的问题。
author: SmithaNataraj
manager: tfehr
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTable, SalesTableListPage, SalesTableListPage_SalesCancelOrder
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 346ebee598e282abfe01a399793cc259aff3c22d
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5232222"
---
# <a name="troubleshoot-sales-orders"></a><span data-ttu-id="7475d-103">销售订单故障排除</span><span class="sxs-lookup"><span data-stu-id="7475d-103">Troubleshoot sales orders</span></span>

<span data-ttu-id="7475d-104">本主题介绍如何解决在使用销售订单时可能遇到的问题。</span><span class="sxs-lookup"><span data-stu-id="7475d-104">This topic describes how to fix issues that you might encounter while you work with sales orders.</span></span>

## <a name="the-tax-information-isnt-updated-if-i-change-the-location-on-a-sales-order-header"></a><span data-ttu-id="7475d-105">如果更改销售订单标题上的位置，税务信息不会更新。</span><span class="sxs-lookup"><span data-stu-id="7475d-105">The tax information isn't updated if I change the location on a sales order header.</span></span>

### <a name="issue-description"></a><span data-ttu-id="7475d-106">问题描述</span><span class="sxs-lookup"><span data-stu-id="7475d-106">Issue description</span></span>

<span data-ttu-id="7475d-107">如果在销售订单标题或行级别更改了站点、仓库或交货地址，不会自动更新行的案例税务信息。</span><span class="sxs-lookup"><span data-stu-id="7475d-107">If the site, warehouse, or delivery address is changed either on a sales order header or at the line level, the case tax information isn't automatically updated for the lines.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="7475d-108">解决问题</span><span class="sxs-lookup"><span data-stu-id="7475d-108">Issue resolution</span></span>

<span data-ttu-id="7475d-109">此为有意行为。</span><span class="sxs-lookup"><span data-stu-id="7475d-109">This behavior is by design.</span></span> <span data-ttu-id="7475d-110">发生此问题是因为交货地址、站点和仓库也未在生级别自动更改。</span><span class="sxs-lookup"><span data-stu-id="7475d-110">The issue occurs because the delivery address, site, and warehouse aren't automatically changed at the line level either.</span></span> <span data-ttu-id="7475d-111">您必须手动更新它们。</span><span class="sxs-lookup"><span data-stu-id="7475d-111">You must update them manually.</span></span>

## <a name="if-there-are-two-trade-agreements-for-the-same-period-or-overlapping-periods-the-same-agreement-line-is-always-selected"></a><span data-ttu-id="7475d-112">如果在同一期间或重叠期间有两个贸易协议，将始终选择同一协议行。</span><span class="sxs-lookup"><span data-stu-id="7475d-112">If there are two trade agreements for the same period or overlapping periods, the same agreement line is always selected.</span></span>

### <a name="issue-description"></a><span data-ttu-id="7475d-113">问题描述</span><span class="sxs-lookup"><span data-stu-id="7475d-113">Issue description</span></span>

<span data-ttu-id="7475d-114">如果为同一期间或重叠期间定义了两个贸易协议，每次创建包含这些物料的销售订单行时，似乎会选择同一个贸易协议。</span><span class="sxs-lookup"><span data-stu-id="7475d-114">If two trade agreements are defined for the same period or overlapping periods, the same trade agreement seems to be selected every time when you create sales order lines that contain those items.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="7475d-115">解决问题</span><span class="sxs-lookup"><span data-stu-id="7475d-115">Issue resolution</span></span>

<span data-ttu-id="7475d-116">如果给定日期有多个贸易协议，将始终选择价格最低的贸易协议。</span><span class="sxs-lookup"><span data-stu-id="7475d-116">If there is more than one trade agreement for a given date, the trade agreement that has the lowest price is always selected.</span></span> <span data-ttu-id="7475d-117">有关详细信息，请下载以下白皮书：[Microsoft Dynamics AX 2012 中的贸易协议](https://www.axug.com/HigherLogic/System/DownloadDocumentFile.ashx?DocumentFileKey=3396a3a8-1f48-4d85-8cd6-5fa982f62e90)。</span><span class="sxs-lookup"><span data-stu-id="7475d-117">For more information, download the following white paper: [Trade agreements in Microsoft Dynamics AX 2012](https://www.axug.com/HigherLogic/System/DownloadDocumentFile.ashx?DocumentFileKey=3396a3a8-1f48-4d85-8cd6-5fa982f62e90).</span></span>

## <a name="can-i-link-a-purchase-order-to-a-sales-order-to-fulfill-demand"></a><span data-ttu-id="7475d-118">我可以将采购订单链接到销售订单以满足需求吗？</span><span class="sxs-lookup"><span data-stu-id="7475d-118">Can I link a purchase order to a sales order to fulfill demand?</span></span>

<span data-ttu-id="7475d-119">您可以从销售订单创建采购订单。</span><span class="sxs-lookup"><span data-stu-id="7475d-119">You can create a purchase order from a sales order.</span></span> <span data-ttu-id="7475d-120">有关详细信息，请参阅[基于销售订单创建采购订单](tasks/create-purchase-order-sales-order.md)。</span><span class="sxs-lookup"><span data-stu-id="7475d-120">For more information, see [Create a purchase order from a sales order](tasks/create-purchase-order-sales-order.md).</span></span>

## <a name="i-cant-cancel-or-delete-a-return-order-or-a-sales-order"></a><span data-ttu-id="7475d-121">我无法取消或删除退货单或销售订单。</span><span class="sxs-lookup"><span data-stu-id="7475d-121">I can't cancel or delete a return order or a sales order.</span></span>

<span data-ttu-id="7475d-122">您只能取消处于 *已创建* 状态的销售订单和退货单。</span><span class="sxs-lookup"><span data-stu-id="7475d-122">You can cancel only sales orders and return orders that are in a *Created* state.</span></span> <span data-ttu-id="7475d-123">有关详细信息，请参阅[取消退货单](../service-management/cancel-return-order.md)。</span><span class="sxs-lookup"><span data-stu-id="7475d-123">For more information, see [Cancel a return order](../service-management/cancel-return-order.md).</span></span>

## <a name="when-i-try-to-cancel-a-sales-order-i-receive-a-reservations-cannot-be-removed-because-there-is-work-created-which-relies-on-the-reservations-error"></a><span data-ttu-id="7475d-124">当我尝试取消销售订单时，我收到“已创建了依赖预留的工作，因此无法删除这些预留”错误。</span><span class="sxs-lookup"><span data-stu-id="7475d-124">When I try to cancel a sales order, I receive a "Reservations cannot be removed because there is work created which relies on the reservations" error.</span></span>

<span data-ttu-id="7475d-125">错误代码：WAX4661</span><span class="sxs-lookup"><span data-stu-id="7475d-125">Error code: WAX4661</span></span>

<span data-ttu-id="7475d-126">如果工作与销售订单相关联，在取消和冲销工作之前，您不能取消销售订单。</span><span class="sxs-lookup"><span data-stu-id="7475d-126">If work is associated with a sales order, you can't cancel the sales order until the work is canceled and reversed.</span></span> <span data-ttu-id="7475d-127">即使与销售订单关联的工作已关闭，此要求也适用。</span><span class="sxs-lookup"><span data-stu-id="7475d-127">This requirement applies even if the work that is associated with the sales order is closed.</span></span>

<span data-ttu-id="7475d-128">若要解决此问题，请按照以下步骤操作。</span><span class="sxs-lookup"><span data-stu-id="7475d-128">To fix this issue, follow these steps.</span></span>

1. <span data-ttu-id="7475d-129">取消工作，然后将库存放回所需的位置。</span><span class="sxs-lookup"><span data-stu-id="7475d-129">Cancel the work, and put inventory back into the desired location.</span></span> <span data-ttu-id="7475d-130">转到销售订单的相关负荷，然后在负荷行上选择 **减少领料数量** 或在操作窗格上选择 **冲销工作**。</span><span class="sxs-lookup"><span data-stu-id="7475d-130">Go to the relevant load of the sales order, and select either **Reduce picked quantity** on the load line or **Reverse work** on the Action Pane.</span></span>

    <span data-ttu-id="7475d-131">现在，工作的状态为 *已取消*，并且已自动创建和处理新的库存变动工作，以在冲销时将库存放回到所述位置。</span><span class="sxs-lookup"><span data-stu-id="7475d-131">The work now has a status of *Canceled*, and new inventory movement work is automatically created and processed to put inventory back into the location that was described at the time of reversal.</span></span>

2. <span data-ttu-id="7475d-132">删除负荷。</span><span class="sxs-lookup"><span data-stu-id="7475d-132">Delete the load.</span></span> <span data-ttu-id="7475d-133">装运也会被删除。</span><span class="sxs-lookup"><span data-stu-id="7475d-133">The shipment is also deleted.</span></span>
3. <span data-ttu-id="7475d-134">您现在应该能够转到销售订单并取消订单。</span><span class="sxs-lookup"><span data-stu-id="7475d-134">You should now be able to go to the sales order and cancel it.</span></span>

## <a name="i-cant-cancel-an-intercompany-purchase-order-that-is-linked-to-a-sales-order"></a><span data-ttu-id="7475d-135">我无法取消链接到销售订单的内部公司采购订单。</span><span class="sxs-lookup"><span data-stu-id="7475d-135">I can't cancel an intercompany purchase order that is linked to a sales order.</span></span>

### <a name="issue-description"></a><span data-ttu-id="7475d-136">问题描述</span><span class="sxs-lookup"><span data-stu-id="7475d-136">Issue description</span></span>

<span data-ttu-id="7475d-137">如果您尝试取消链接到销售订单的内部公司采购订单，您可能会收到以下错误消息：“数量无法减少，因为剩余的更新数量会更改符号。”</span><span class="sxs-lookup"><span data-stu-id="7475d-137">If you try to cancel an intercompany purchase order that is linked to a sales order, you might receive the following error message: "Quantity cannot be reduced because the remaining update quantity changes sign."</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="7475d-138">解决问题</span><span class="sxs-lookup"><span data-stu-id="7475d-138">Issue resolution</span></span>

<span data-ttu-id="7475d-139">此问题已在 Microsoft Dynamics 365 Supply Chain Management 版本 10.0.13 中修复。</span><span class="sxs-lookup"><span data-stu-id="7475d-139">This issue was fixed in Microsoft Dynamics 365 Supply Chain Management version 10.0.13.</span></span> <span data-ttu-id="7475d-140">在该版本和更高版本中，您现在可以取消链接到销售订单的内部公司采购订单。</span><span class="sxs-lookup"><span data-stu-id="7475d-140">In that version and later versions, you can now cancel an intercompany purchase order that is linked to a sales order.</span></span>

## <a name="can-i-restore-an-invoiced-sales-order-that-was-deleted"></a><span data-ttu-id="7475d-141">我可以恢复删除的已开票销售订单吗？</span><span class="sxs-lookup"><span data-stu-id="7475d-141">Can I restore an invoiced sales order that was deleted?</span></span>

### <a name="issue-description"></a><span data-ttu-id="7475d-142">问题描述</span><span class="sxs-lookup"><span data-stu-id="7475d-142">Issue description</span></span>

<span data-ttu-id="7475d-143">开票的销售订单被误删除，您想要恢复它或查看它的详细信息。</span><span class="sxs-lookup"><span data-stu-id="7475d-143">An invoiced sales order was deleted by mistake, and you want to restore it or view its details.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="7475d-144">解决问题</span><span class="sxs-lookup"><span data-stu-id="7475d-144">Issue resolution</span></span>

<span data-ttu-id="7475d-145">如果删除的销售订单已开票，请转到 **客户帐户 \> 交易记录 \> 原始单据 \> 查看详细信息**。</span><span class="sxs-lookup"><span data-stu-id="7475d-145">If the deleted sales order has already been invoiced, go to **Customer account \> Transactions \> Original document \> View details**.</span></span> <span data-ttu-id="7475d-146">找到您要查找的发票，然后选择它查看详细信息。</span><span class="sxs-lookup"><span data-stu-id="7475d-146">Find the invoice that you're looking for, and select it to view its details.</span></span> <span data-ttu-id="7475d-147">这些详细信息包括销售订单引用。</span><span class="sxs-lookup"><span data-stu-id="7475d-147">These details include the sales order reference.</span></span> <span data-ttu-id="7475d-148">您还应该能够从该页面访问销售订单详细信息。</span><span class="sxs-lookup"><span data-stu-id="7475d-148">You should also be able to access the sales order details from that page.</span></span>

## <a name="the-deadline-of-a-sales-order-header-cant-be-found-in-the-salesorderheaderv2entity-data-entity"></a><span data-ttu-id="7475d-149">在 SalesOrderHeaderV2Entity 数据实体中找不到销售订单标题的截止日期。</span><span class="sxs-lookup"><span data-stu-id="7475d-149">The deadline of a sales order header can't be found in the SalesOrderHeaderV2Entity data entity.</span></span>

<span data-ttu-id="7475d-150">截止日期字段不在 *SalesOrderHeaderV2Entity* 实体中。</span><span class="sxs-lookup"><span data-stu-id="7475d-150">The deadline field doesn't exist on the *SalesOrderHeaderV2Entity* entity.</span></span>

## <a name="i-must-delete-orphaned-sales-order-records"></a><span data-ttu-id="7475d-151">我必须删除孤立的销售订单记录。</span><span class="sxs-lookup"><span data-stu-id="7475d-151">I must delete orphaned sales order records.</span></span>

<span data-ttu-id="7475d-152">要清除孤立的销售订单记录，请转到以下任一位置运行 *销售订单删除* 定期作业：</span><span class="sxs-lookup"><span data-stu-id="7475d-152">To clean up orphaned sales order records, run the *Sales order deletion* periodic job by going to either of the following places:</span></span>

- <span data-ttu-id="7475d-153">销售和市场营销 \> 定期任务 \> 清除 \> 删除销售订单</span><span class="sxs-lookup"><span data-stu-id="7475d-153">Sales and marketing \> Periodic tasks \> Clean up \> Delete sales orders</span></span>
- <span data-ttu-id="7475d-154">零售和商业 \> 零售和商业 IT \> 清除 \> 删除销售订单</span><span class="sxs-lookup"><span data-stu-id="7475d-154">Retail and commerce \> Retail and commerce IT \> Clean up \> Delete sales orders</span></span>

## <a name="is-there-a-way-to-calculate-commissions-on-invoices-that-have-already-been-posted"></a><span data-ttu-id="7475d-155">是否有方法可以计算已经过帐的发票上的佣金？</span><span class="sxs-lookup"><span data-stu-id="7475d-155">Is there a way to calculate commissions on invoices that have already been posted?</span></span>

<span data-ttu-id="7475d-156">Supply Chain Management 当前不支持已过帐发票的佣金计算。</span><span class="sxs-lookup"><span data-stu-id="7475d-156">Supply Chain Management doesn't currently support the calculation of commissions for posted invoices.</span></span>

## <a name="a-bundle-item-isnt-supported-in-an-intercompany-process"></a><span data-ttu-id="7475d-157">内部公司流程不支持捆绑物料。</span><span class="sxs-lookup"><span data-stu-id="7475d-157">A bundle item isn't supported in an intercompany process.</span></span>

<span data-ttu-id="7475d-158">捆绑物料不能用于采购订单，因为如果检查捆绑物料的销售订单行，您会注意到数量为 *0*（零），状态为 *已取消*。</span><span class="sxs-lookup"><span data-stu-id="7475d-158">The bundle item isn't available for the purchase order because, if you examine the sales order lines for the bundle item, you will notice that the quantity is *0* (zero) and the status is *Canceled*.</span></span> <span data-ttu-id="7475d-159">此为有意行为。</span><span class="sxs-lookup"><span data-stu-id="7475d-159">This behavior is by design.</span></span> <span data-ttu-id="7475d-160">销售订单仅购买捆绑物料的组件。</span><span class="sxs-lookup"><span data-stu-id="7475d-160">The sales order buys only the components of the bundle item.</span></span> <span data-ttu-id="7475d-161">不购买捆绑物料本身。</span><span class="sxs-lookup"><span data-stu-id="7475d-161">It doesn't buy the bundle item itself.</span></span>

<span data-ttu-id="7475d-162">如果必须购买捆绑，请考虑是否必须将其标记为捆绑物料，因为此功能是为收入确认场景设计的。</span><span class="sxs-lookup"><span data-stu-id="7475d-162">If you must buy a bundle, consider whether you have to mark it as bundle item, because this functionality is designed for revenue recognition scenarios.</span></span> <span data-ttu-id="7475d-163">有关捆绑物料的详细信息，请参阅[捆绑销售](../../finance/accounts-receivable/revenue-recognition-setup.md#bundles)。</span><span class="sxs-lookup"><span data-stu-id="7475d-163">For more information about bundle items, see [Bundles](../../finance/accounts-receivable/revenue-recognition-setup.md#bundles).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]