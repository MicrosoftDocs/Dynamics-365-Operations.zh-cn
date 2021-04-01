---
title: 负荷构建和装运疑难解答
description: 此主题介绍如何解决在 Microsoft Dynamics 365 Supply Chain Management 中处理负荷构建和装运时可能遇到的常见问题。
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: c7dc9cc9de4d5089d497c36759931669ee2e9e55
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5259498"
---
# <a name="troubleshoot-load-building-and-shipments"></a><span data-ttu-id="e100e-103">负荷构建和装运疑难解答</span><span class="sxs-lookup"><span data-stu-id="e100e-103">Troubleshoot load building and shipments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e100e-104">此主题介绍如何解决在 Microsoft Dynamics 365 Supply Chain Management 中处理负荷构建和装运时可能遇到的常见问题。</span><span class="sxs-lookup"><span data-stu-id="e100e-104">This topic describes how to fix common issues that you might encounter while you work with load building and shipments in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-you-cant-create-a-load-line-for-this-order-line-because-it-contains-inventory-dimensions-that-are-invalid"></a><span data-ttu-id="e100e-105">我收到以下错误消息：“您无法为此订单行创建负荷行，因为它包含无效的库存维度...”</span><span class="sxs-lookup"><span data-stu-id="e100e-105">I receive the following error message: "You can't create a load line for this order line because it contains inventory dimensions that are invalid..."</span></span>

### <a name="issue-description"></a><span data-ttu-id="e100e-106">问题描述</span><span class="sxs-lookup"><span data-stu-id="e100e-106">Issue description</span></span>

<span data-ttu-id="e100e-107">当您尝试将退货销售订单下达到仓库时，您会收到以下错误消息：</span><span class="sxs-lookup"><span data-stu-id="e100e-107">You receive the following error message when you try to release a return sales order to the warehouse:</span></span>

> <span data-ttu-id="e100e-108">您无法为此订单行创建负荷行，因为它包含无效的库存维度。</span><span class="sxs-lookup"><span data-stu-id="e100e-108">You can't create a load line for this order line because it contains inventory dimensions that are invalid.</span></span> <span data-ttu-id="e100e-109">您无法引用位于预留层次结构中位置维度以下的库存维度。</span><span class="sxs-lookup"><span data-stu-id="e100e-109">You can't reference inventory dimensions that are located below the location dimension in the reservation hierarchy.</span></span> <span data-ttu-id="e100e-110">请从订单行中删除无效维度。</span><span class="sxs-lookup"><span data-stu-id="e100e-110">Remove the invalid dimensions from the order line.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="e100e-111">解决问题</span><span class="sxs-lookup"><span data-stu-id="e100e-111">Issue resolution</span></span>

<span data-ttu-id="e100e-112">很遗憾，此产品不支持销售退货流程的负荷处理。</span><span class="sxs-lookup"><span data-stu-id="e100e-112">Unfortunately, the product doesn't support load processing for a sales return process.</span></span> <span data-ttu-id="e100e-113">因此，您不能将退货销售订单下达到仓库。</span><span class="sxs-lookup"><span data-stu-id="e100e-113">Therefore, you can't release the return sales order to the warehouse.</span></span>

<span data-ttu-id="e100e-114">在销售订单交易中，您无法引用位于预留层次结构中 **位置** 维度以下的库存维度。</span><span class="sxs-lookup"><span data-stu-id="e100e-114">On sales order transactions, you can't reference inventory dimensions that are located below the **Location** dimension in the reservation hierarchy.</span></span> <span data-ttu-id="e100e-115">解决方法是从订单行中删除无效维度。</span><span class="sxs-lookup"><span data-stu-id="e100e-115">The resolution is to remove the invalid dimensions from the order line.</span></span>

## <a name="i-receive-the-following-error-message-one-of-the-lines-is-already-on-a-load-unable-to-release-to-warehouse"></a><span data-ttu-id="e100e-116">我收到以下错误消息：“其中一行已在负荷中。</span><span class="sxs-lookup"><span data-stu-id="e100e-116">I receive the following error message: "One of the lines is already on a load.</span></span> <span data-ttu-id="e100e-117">无法下达到仓库。”</span><span class="sxs-lookup"><span data-stu-id="e100e-117">Unable to release to warehouse."</span></span>

### <a name="issue-description"></a><span data-ttu-id="e100e-118">问题描述</span><span class="sxs-lookup"><span data-stu-id="e100e-118">Issue description</span></span>

<span data-ttu-id="e100e-119">如果您手动创建负荷，或者设置流程以在进行销售订单行输入之前负荷已经创建，系统将假定后续下达会手动完成，并将使用负荷中的路线和评级。</span><span class="sxs-lookup"><span data-stu-id="e100e-119">If you manually create loads, or if you set up the process so that loads are already created before sales order line entry occurs, the assumption is that the subsequent release will be done manually, and that the route and rating from the load will be used.</span></span>

<span data-ttu-id="e100e-120">在另一个可能的场景中，您尝试对仓库执行自动下达，但是波次流程无法创建工作。</span><span class="sxs-lookup"><span data-stu-id="e100e-120">In another possible scenario, you're trying to do an automatic release to the warehouse, but the wave process failed to create work.</span></span> <span data-ttu-id="e100e-121">因此，仍会创建未结装运或负荷。</span><span class="sxs-lookup"><span data-stu-id="e100e-121">Therefore, an open shipment or load is still created.</span></span> <span data-ttu-id="e100e-122">然后，此未结装运或负荷将阻止后续自动下达订单的尝试，直到您删除未结装运或负荷，或手动重新处理波次。</span><span class="sxs-lookup"><span data-stu-id="e100e-122">This open shipment or load then blocks subsequent attempts to automatically release the order until you either delete the open shipment or load, or manually reprocess the wave.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="e100e-123">解决问题</span><span class="sxs-lookup"><span data-stu-id="e100e-123">Issue resolution</span></span>

<span data-ttu-id="e100e-124">您可以从销售订单页下达，也可以从下达销售订单页自动下达，只要在下达仓库之前没有负荷。</span><span class="sxs-lookup"><span data-stu-id="e100e-124">You can release from the sales order page, or automatic release can be done from the release sales order page, only if no load exists before the release to the warehouse.</span></span> <span data-ttu-id="e100e-125">负荷将在波次被处理后自动创建。</span><span class="sxs-lookup"><span data-stu-id="e100e-125">The load will automatically be created after the wave is processed.</span></span>

## <a name="i-receive-the-following-error-message-the-delivery-note-correction-cant-be-processed-the-delivery-note-only-contains-items-that-are-subject-to-warehouse-management-processes-as-these-are-not-supported-by-delivery-note-correction"></a><span data-ttu-id="e100e-126">我收到以下错误消息：“无法处理交货通知更正。</span><span class="sxs-lookup"><span data-stu-id="e100e-126">I receive the following error message: "The delivery note correction can't be processed.</span></span> <span data-ttu-id="e100e-127">交货通知仅包含需要进入仓库管理流程的物料，因为交货通知更正不支持这些物料。”</span><span class="sxs-lookup"><span data-stu-id="e100e-127">The delivery note only contains items that are subject to warehouse management processes, as these are not supported by Delivery Note correction."</span></span>

### <a name="issue-description"></a><span data-ttu-id="e100e-128">问题描述</span><span class="sxs-lookup"><span data-stu-id="e100e-128">Issue description</span></span>

<span data-ttu-id="e100e-129">发布交货通知后，将无法取消，因为 **取消** 按钮不可用。</span><span class="sxs-lookup"><span data-stu-id="e100e-129">After you post a delivery note, you can't cancel it, because the **Cancel** button is unavailable.</span></span> <span data-ttu-id="e100e-130">您也无法更正交货通知。</span><span class="sxs-lookup"><span data-stu-id="e100e-130">You also can't correct the delivery note.</span></span> <span data-ttu-id="e100e-131">如果尝试更正，将收到此错误消息。</span><span class="sxs-lookup"><span data-stu-id="e100e-131">If you try, you receive this error message.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="e100e-132">解决问题</span><span class="sxs-lookup"><span data-stu-id="e100e-132">Issue resolution</span></span>

<span data-ttu-id="e100e-133">要更正已启用高级仓库管理 (WMS) 的物料的已过帐装箱单，必须从负荷而不是直接从订单进行过帐。</span><span class="sxs-lookup"><span data-stu-id="e100e-133">To correct posted packing slips for items that are enabled for advanced warehouse management (WMS), you must do the posting from the load, not directly from the order.</span></span>

## <a name="how-can-i-create-work-from-outbound-loads-instead-of-waves"></a><span data-ttu-id="e100e-134">如何从出站负荷而不是波次创建工作？</span><span class="sxs-lookup"><span data-stu-id="e100e-134">How can I create work from outbound loads instead of waves?</span></span>

### <a name="issue-description"></a><span data-ttu-id="e100e-135">问题描述</span><span class="sxs-lookup"><span data-stu-id="e100e-135">Issue description</span></span>

<span data-ttu-id="e100e-136">这里是重现此问题的一种方法。</span><span class="sxs-lookup"><span data-stu-id="e100e-136">Here is one way to reproduce this issue.</span></span>

1. <span data-ttu-id="e100e-137">使用销售订单或转移单创建出站负荷。</span><span class="sxs-lookup"><span data-stu-id="e100e-137">Create an outbound load by using a sales order or transfer order.</span></span>
2. <span data-ttu-id="e100e-138">将负荷发放到仓库。</span><span class="sxs-lookup"><span data-stu-id="e100e-138">Release the load to the warehouse.</span></span>
3. <span data-ttu-id="e100e-139">请注意，尚未生成任何领料工作。</span><span class="sxs-lookup"><span data-stu-id="e100e-139">Notice that no picking work has yet been generated.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="e100e-140">解决问题</span><span class="sxs-lookup"><span data-stu-id="e100e-140">Issue resolution</span></span>

<span data-ttu-id="e100e-141">如果必须在发放负荷时立即生成工作，您必须相应地配置波次模板。</span><span class="sxs-lookup"><span data-stu-id="e100e-141">If work must be generated immediately when the load is released, you must configure the wave template accordingly.</span></span> <span data-ttu-id="e100e-142">在波次模板上，将以下选项设置为 *是*：</span><span class="sxs-lookup"><span data-stu-id="e100e-142">On the wave template, set the following options to *Yes*:</span></span>

- <span data-ttu-id="e100e-143">自动波次创建</span><span class="sxs-lookup"><span data-stu-id="e100e-143">Automate wave creation</span></span>
- <span data-ttu-id="e100e-144">在发放到仓库时处理波次</span><span class="sxs-lookup"><span data-stu-id="e100e-144">Process wave at release to warehouse</span></span>
- <span data-ttu-id="e100e-145">自动发出波次</span><span class="sxs-lookup"><span data-stu-id="e100e-145">Automate wave release</span></span>

## <a name="i-cant-re-release-a-partially-shipped-load"></a><span data-ttu-id="e100e-146">我无法重新发放部分装运的负荷。</span><span class="sxs-lookup"><span data-stu-id="e100e-146">I can't re-release a partially shipped load.</span></span>

### <a name="issue-description"></a><span data-ttu-id="e100e-147">问题描述</span><span class="sxs-lookup"><span data-stu-id="e100e-147">Issue description</span></span>

<span data-ttu-id="e100e-148">您不能将部分装运的负荷发放到仓库。</span><span class="sxs-lookup"><span data-stu-id="e100e-148">You can't release a partially shipped load to the warehouse.</span></span> <span data-ttu-id="e100e-149">当您对仓库执行发放时，会出现“操作完成”消息，但是不会发生任何变化，也不会为剩余数量创建工作。</span><span class="sxs-lookup"><span data-stu-id="e100e-149">When you do the release to the warehouse, an "Operation complete" message appears, but nothing happens, and no work is created for the remaining quantity.</span></span> <span data-ttu-id="e100e-150">当您使用运输负荷功能并且有未完成的预留时，会发生此问题。</span><span class="sxs-lookup"><span data-stu-id="e100e-150">This issue occurs when you use transport load functionality and there is an incomplete reservation.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="e100e-151">解决问题</span><span class="sxs-lookup"><span data-stu-id="e100e-151">Issue resolution</span></span>

<span data-ttu-id="e100e-152">[KB 问题 470069](https://fix.lcs.dynamics.com/Issue/Details?kb=4574490&bugId=470069&dbType=3&qc=84ce1e09d7032d8b8ef86f5a0c68b86badf3dfaf29686c5ebbe97c53c0957b5f)（“部分装运的负荷可以重新加入波次和重新处理”）在[版本 10.0.15](../get-started/whats-new-scm-10-0-15.md) 中已修复。</span><span class="sxs-lookup"><span data-stu-id="e100e-152">[KB issue 470069](https://fix.lcs.dynamics.com/Issue/Details?kb=4574490&bugId=470069&dbType=3&qc=84ce1e09d7032d8b8ef86f5a0c68b86badf3dfaf29686c5ebbe97c53c0957b5f) ("Partially shipped loads can be re-waved and re-processed") is fixed in [release 10.0.15](../get-started/whats-new-scm-10-0-15.md).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]