---
title: 采购工作流故障排除
description: 本主题介绍如何解决使用采购工作流时可能遇到的问题。
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
ms.openlocfilehash: cdedc45b8f057310801f134104156a732fb58d86
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4423424"
---
# <a name="troubleshoot-procurement-and-sourcing-workflows"></a><span data-ttu-id="c8c10-103">采购工作流故障排除</span><span class="sxs-lookup"><span data-stu-id="c8c10-103">Troubleshoot procurement and sourcing workflows</span></span>

<span data-ttu-id="c8c10-104">本主题介绍如何解决使用采购工作流时可能遇到的问题。</span><span class="sxs-lookup"><span data-stu-id="c8c10-104">This topic describes how to fix issues that you might encounter while you work with procurement and sourcing workflows.</span></span>

## <a name="error-when-re-submitting-a-purchase-order-to-the-workflow-after-a-change-changes-to-purchase-order-x-are-allowed-only-in-a-draft-state-when-change-management-is-activated"></a><span data-ttu-id="c8c10-105">更改后将采购订单重新提交到工作流时出错：“激活更改管理后，仅允许在“草稿”状态下对采购订单 X 进行更改”</span><span class="sxs-lookup"><span data-stu-id="c8c10-105">Error when re-submitting a purchase order to the workflow after a change: "Changes to purchase order X are allowed only in a Draft state when change management is activated"</span></span>

<span data-ttu-id="c8c10-106">仅当在您请求更改之前采购订单处于 *已确认* 状态时，才会发生此问题。</span><span class="sxs-lookup"><span data-stu-id="c8c10-106">This issue occurs only if the purchase order was in a *Confirmed* state before you requested changes.</span></span> <span data-ttu-id="c8c10-107">如果您在采购订单处于 *已批准* 状态时请求更改，工作流可以成功处理。</span><span class="sxs-lookup"><span data-stu-id="c8c10-107">If you request changes while the purchase order is in an *Approved* state, the workflow can be processed successfully.</span></span>

### <a name="error-description"></a><span data-ttu-id="c8c10-108">错误描述</span><span class="sxs-lookup"><span data-stu-id="c8c10-108">Error description</span></span>

<span data-ttu-id="c8c10-109">更改后重新提交采购订单时，工作流中发生以下错误：</span><span class="sxs-lookup"><span data-stu-id="c8c10-109">The following error occurs in the workflow when a purchase order is resubmitted after a change:</span></span>

> <span data-ttu-id="c8c10-110">已停止(错误): X++ 异常：在以下位置激活更改管理时，仅允许在“草稿”状态下对采购订单 PO0000569 进行更改</span><span class="sxs-lookup"><span data-stu-id="c8c10-110">Stopped (error): X++ Exception: Changes to purchase order PO0000569 are only allowed in state Draft when change management is activated at</span></span><br>
<span data-ttu-id="c8c10-111">SysWorkflowParticipantProvider-resolve</span><span class="sxs-lookup"><span data-stu-id="c8c10-111">SysWorkflowParticipantProvider-resolve</span></span><br>
<span data-ttu-id="c8c10-112">SysWorkflowParticipantProvider-resolveParticipants</span><span class="sxs-lookup"><span data-stu-id="c8c10-112">SysWorkflowParticipantProvider-resolveParticipants</span></span><br>
<span data-ttu-id="c8c10-113">SysWorkflowServiceProvider-resolveParticipant</span><span class="sxs-lookup"><span data-stu-id="c8c10-113">SysWorkflowServiceProvider-resolveParticipant</span></span><br>
<span data-ttu-id="c8c10-114">SysWorkflowQueue-resume</span><span class="sxs-lookup"><span data-stu-id="c8c10-114">SysWorkflowQueue-resume</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="c8c10-115">解决问题</span><span class="sxs-lookup"><span data-stu-id="c8c10-115">Issue resolution</span></span>

<span data-ttu-id="c8c10-116">发生此问题可能是由于采购订单分配不一致。</span><span class="sxs-lookup"><span data-stu-id="c8c10-116">This issue can occur because of inconsistency in purchase order distributions.</span></span>

<span data-ttu-id="c8c10-117">要解决此问题并将采购订单重置为 *草稿* 状态，请转到 **采购 \> 定期任务 \> 清除 \> 采购订单分配重置**。</span><span class="sxs-lookup"><span data-stu-id="c8c10-117">To unblock this issue and reset the purchase order to a *Draft* state, go to **Procurement and sourcing \> Periodic tasks \> Clean up \> Purchase order distribution reset**.</span></span> <span data-ttu-id="c8c10-118">有关详细信息，请参阅以下博客文章：[解决 Dynamics 365 Supply Chain Management 中的采购订单分配错误](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/)。</span><span class="sxs-lookup"><span data-stu-id="c8c10-118">For more information, see the following blog post: [Resolve PO distribution errors in Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span></span>

<span data-ttu-id="c8c10-119">此问题将通过[此 Microsoft 知识库 (KB) 文章](https://msdyneng.visualstudio.com/FinOps/_workitems/edit/467138)解决。</span><span class="sxs-lookup"><span data-stu-id="c8c10-119">The issue will be fixed through [this Microsoft Knowledge Base (KB) article](https://msdyneng.visualstudio.com/FinOps/_workitems/edit/467138).</span></span>

## <a name="one-or-more-accounting-distributions-are-either-over-distributed-or-under-distributed"></a><span data-ttu-id="c8c10-120">一个或多个会计分配分配过多或分配不足。</span><span class="sxs-lookup"><span data-stu-id="c8c10-120">One or more accounting distributions are either over-distributed or under-distributed.</span></span>

<span data-ttu-id="c8c10-121">发生此问题可能是由于采购订单分配不一致。</span><span class="sxs-lookup"><span data-stu-id="c8c10-121">This issue can occur because of inconsistency in purchase order distributions.</span></span>

<span data-ttu-id="c8c10-122">要解决此问题并将采购订单重置为 *草稿* 状态，请转到 **采购 \> 定期任务 \> 清除 \> 采购订单分配重置**。</span><span class="sxs-lookup"><span data-stu-id="c8c10-122">To unblock this issue and reset the purchase order to a *Draft* state, go to **Procurement and sourcing \> Periodic tasks \> Clean up \> Purchase order distribution reset**.</span></span> <span data-ttu-id="c8c10-123">有关详细信息，请参阅以下博客文章：[解决 Dynamics 365 Supply Chain Management 中的采购订单分配错误](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/)。</span><span class="sxs-lookup"><span data-stu-id="c8c10-123">For more information, see the following blog post: [Resolve PO distribution errors in Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span></span>

## <a name="if-a-delivery-remainder-is-canceled-on-a-purchase-order-where-change-management-is-turned-on-the-purchase-order-goes-to-a-confirmed-state"></a><span data-ttu-id="c8c10-124">如果在打开了更改管理的采购订单上取消了剩余交货量，采购订单将进入“已确认”状态。</span><span class="sxs-lookup"><span data-stu-id="c8c10-124">If a delivery remainder is canceled on a purchase order where change management is turned on, the purchase order goes to a Confirmed state.</span></span>

### <a name="issue-description"></a><span data-ttu-id="c8c10-125">问题描述</span><span class="sxs-lookup"><span data-stu-id="c8c10-125">Issue description</span></span>

<span data-ttu-id="c8c10-126">对于需要接受更改管理的采购订单，如果请求的唯一更改是取消一个或多个行上的剩余交货量，该采购订单在获得批准后将直接进入 *已确认* 状态，不会创建日记帐。</span><span class="sxs-lookup"><span data-stu-id="c8c10-126">For a purchase order that is subject to change management, if the only change that is requested is the cancellation of a delivery remainder on one or more of the lines, the purchase order will go directly to a *Confirmed* state when it's approved, and no journal will be created.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="c8c10-127">解决问题</span><span class="sxs-lookup"><span data-stu-id="c8c10-127">Issue resolution</span></span>

<span data-ttu-id="c8c10-128">取消剩余交货量不会影响确认日记帐的内容。</span><span class="sxs-lookup"><span data-stu-id="c8c10-128">Cancellation of a delivery remainder doesn't affect the contents of the confirmation journal.</span></span> <span data-ttu-id="c8c10-129">此功能应在部分接收行时使用，剩余数量应在与供应商确认采购订单后，在流程步骤中取消。</span><span class="sxs-lookup"><span data-stu-id="c8c10-129">This functionality should be used when the line has been partially received, and the remainder quality should be canceled in the process step after the purchase order has been confirmed with the vendor.</span></span>

<span data-ttu-id="c8c10-130">如果这应该反映在采购订单确认中，数量应在采购订单行上调整，以要求进行确认。</span><span class="sxs-lookup"><span data-stu-id="c8c10-130">If this should be reflected on the purchase order confirmation, the quantity should be adjusted on the purchase order line so that the confirmation will be required.</span></span> <span data-ttu-id="c8c10-131">或者，如果行上未进行任何接收，可以删除数量。</span><span class="sxs-lookup"><span data-stu-id="c8c10-131">Alternatively, if nothing has been received on the line, the quantity can be removed.</span></span> <span data-ttu-id="c8c10-132">在这种情况下，将需要重新确认。</span><span class="sxs-lookup"><span data-stu-id="c8c10-132">In this case, reconfirmation will be required.</span></span>

## <a name="canceled-purchase-orders-appear-in-the-draft-list-in-the-purchase-order-preparation-workspace"></a><span data-ttu-id="c8c10-133">取消的采购订单将显示在“采购订单准备”工作区的草稿列表中。</span><span class="sxs-lookup"><span data-stu-id="c8c10-133">Canceled purchase orders appear in the draft list in the Purchase order preparation workspace.</span></span>

### <a name="issue-description"></a><span data-ttu-id="c8c10-134">问题描述</span><span class="sxs-lookup"><span data-stu-id="c8c10-134">Issue description</span></span>

<span data-ttu-id="c8c10-135">取消处于 *已确认* 状态的采购订单后，取消的采购订单仍会出现在 **采购订单准备** 工作区中的草稿采购订单列表中。</span><span class="sxs-lookup"><span data-stu-id="c8c10-135">After you cancel purchase orders that were in a *Confirmed* state, the canceled purchase orders still appear in the list of draft purchase orders in the **Purchase order preparation** workspace.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="c8c10-136">解决问题</span><span class="sxs-lookup"><span data-stu-id="c8c10-136">Issue resolution</span></span>

<span data-ttu-id="c8c10-137">仅需要接受更改管理的采购订单会发生此问题。</span><span class="sxs-lookup"><span data-stu-id="c8c10-137">This issue occurs only for purchase orders that are subject to change management.</span></span> <span data-ttu-id="c8c10-138">发生这种情况是因为取消被认为是必须进行审批的更改。</span><span class="sxs-lookup"><span data-stu-id="c8c10-138">It occurs because the cancellation is considered a change that must be approved.</span></span> <span data-ttu-id="c8c10-139">审批可以由系统自动完成。</span><span class="sxs-lookup"><span data-stu-id="c8c10-139">The approval can be done automatically by the system.</span></span> <span data-ttu-id="c8c10-140">因此，流程是将取消的采购订单提交到审批工作流，让它可以进入 *已批准* 状态。</span><span class="sxs-lookup"><span data-stu-id="c8c10-140">Therefore, the process is to submit the canceled purchase order to the approval workflow so that it can go to an *Approved* state.</span></span> <span data-ttu-id="c8c10-141">此时，采购订单将不再出现在 **采购订单准备** 工作区中的草稿采购订单列表中。</span><span class="sxs-lookup"><span data-stu-id="c8c10-141">At that point, the purchase order will no longer appear in the list of draft purchase orders in the **Purchase order preparation** workspace.</span></span>

