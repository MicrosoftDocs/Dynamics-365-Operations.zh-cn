---
title: 领料和打包疑难解答
description: 此主题介绍如何解决在 Microsoft Dynamics 365 Supply Chain Management 中领料和打包时可能遇到的常见问题。
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
ms.openlocfilehash: 01e33b63e09a035f5243bd57faf53b522737c987
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5223234"
---
# <a name="troubleshoot-picking-and-packing"></a><span data-ttu-id="e8509-103">领料和打包疑难解答</span><span class="sxs-lookup"><span data-stu-id="e8509-103">Troubleshoot picking and packing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e8509-104">此主题介绍如何解决在 Microsoft Dynamics 365 Supply Chain Management 中领料和打包时可能遇到的常见问题。</span><span class="sxs-lookup"><span data-stu-id="e8509-104">This topic describes how to fix common issues that you might encounter while you pick and pack in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-dimension-location-cant-be-left-blank-if-dimension-serial-number-is-set"></a><span data-ttu-id="e8509-105">我收到以下错误消息：“如果设置了维度序列号，维度位置不能保留为空。”</span><span class="sxs-lookup"><span data-stu-id="e8509-105">I receive the following error message: "Dimension location can't be left blank if dimension serial number is set."</span></span>

### <a name="issue-description"></a><span data-ttu-id="e8509-106">问题描述</span><span class="sxs-lookup"><span data-stu-id="e8509-106">Issue description</span></span>

<span data-ttu-id="e8509-107">如果您使用启用了高级仓库管理 (WMS) 的仓库为序列物料创建转移单，然后在工作完成后尝试确认装运，这时会收到此错误消息。</span><span class="sxs-lookup"><span data-stu-id="e8509-107">You receive this error message if you create a transfer order for a serial item by using a warehouse that is enabled for advanced warehouse management (WMS), and then, after the work is completed, you try to confirm the shipment.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="e8509-108">解决问题</span><span class="sxs-lookup"><span data-stu-id="e8509-108">Issue resolution</span></span>

<span data-ttu-id="e8509-109">**默认收货位置** 字段在“来源”仓库的中转仓库中是空白的。</span><span class="sxs-lookup"><span data-stu-id="e8509-109">The **Default receipt location** field is blank for a transit warehouse of the "from" warehouse.</span></span> <span data-ttu-id="e8509-110">要解决此问题，请在中转仓库中指定默认收货位置。</span><span class="sxs-lookup"><span data-stu-id="e8509-110">To fix this issue, specify a default receipt location in the transit warehouse.</span></span> <span data-ttu-id="e8509-111">请确保此位置是由牌照控制的。</span><span class="sxs-lookup"><span data-stu-id="e8509-111">Make sure that this location is license plate–controlled.</span></span>

## <a name="i-receive-the-following-error-message-invalid-license-plate"></a><span data-ttu-id="e8509-112">我收到以下错误消息：“无效牌照。”</span><span class="sxs-lookup"><span data-stu-id="e8509-112">I receive the following error message: "Invalid license plate."</span></span>

### <a name="issue-description"></a><span data-ttu-id="e8509-113">问题描述</span><span class="sxs-lookup"><span data-stu-id="e8509-113">Issue description</span></span>

<span data-ttu-id="e8509-114">当您扫描牌照 ID 时，会在仓库应用中收到此错误消息。</span><span class="sxs-lookup"><span data-stu-id="e8509-114">You receive this error message in the warehouse app when you scan a license plate ID.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="e8509-115">解决问题</span><span class="sxs-lookup"><span data-stu-id="e8509-115">Issue resolution</span></span>

<span data-ttu-id="e8509-116">请确保牌照表中存在该牌照 ID，并且牌照上的物料和数量均可用（换言之，它们没有被锁定）。</span><span class="sxs-lookup"><span data-stu-id="e8509-116">Make sure that the license plate ID exists in the license plates table, and that the items and quantities on the license plate are available (in other words, they aren't blocked).</span></span>

## <a name="i-receive-the-following-error-message-field-load-weight-1-can-only-contain-positive-numbers-update-has-been-canceled"></a><span data-ttu-id="e8509-117">我收到以下错误消息：“字段 'Load weight'(=-%1) 只能包含正数。</span><span class="sxs-lookup"><span data-stu-id="e8509-117">I receive the following error message: "Field 'Load weight'(=-%1) can only contain positive numbers.</span></span> <span data-ttu-id="e8509-118">已取消更新。”</span><span class="sxs-lookup"><span data-stu-id="e8509-118">Update has been canceled."</span></span>

### <a name="issue-description"></a><span data-ttu-id="e8509-119">问题描述</span><span class="sxs-lookup"><span data-stu-id="e8509-119">Issue description</span></span>

<span data-ttu-id="e8509-120">当您处理从打包位置到暂存位置，或从暂存位置到停靠位置的工作时，如果有未结工作，将会收到此错误消息。</span><span class="sxs-lookup"><span data-stu-id="e8509-120">You receive this error message if there is open work when you process work from packing locations to staging locations, or from staging locations to dock locations.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="e8509-121">解决问题</span><span class="sxs-lookup"><span data-stu-id="e8509-121">Issue resolution</span></span>

<span data-ttu-id="e8509-122">要解决此问题，请转到 **系统管理 \> 定期任务 \> 数据库 \> 一致性检查**，运行 **仓库负荷重量一致性检查** 流程。</span><span class="sxs-lookup"><span data-stu-id="e8509-122">To fix this issue, go to **System administration \> Periodic tasks \> Database \> Consistency check**, and run the process for **Warehouse load weight consistency check**.</span></span>

## <a name="i-receive-the-following-error-message-the-quantity-is-not-valid-for-unit-1"></a><span data-ttu-id="e8509-123">我收到以下错误消息：“数量对于单位 %1 无效。”</span><span class="sxs-lookup"><span data-stu-id="e8509-123">I receive the following error message: "The quantity is not valid for unit %1."</span></span>

### <a name="issue-description"></a><span data-ttu-id="e8509-124">问题描述</span><span class="sxs-lookup"><span data-stu-id="e8509-124">Issue description</span></span>

<span data-ttu-id="e8509-125">当您尝试跨多个批次执行 *拆分领料* 时，会收到此错误消息。</span><span class="sxs-lookup"><span data-stu-id="e8509-125">You receive this error message when you try to perform a *split pick* across multiple batches.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="e8509-126">解决问题</span><span class="sxs-lookup"><span data-stu-id="e8509-126">Issue resolution</span></span>

<span data-ttu-id="e8509-127">仓库工作人员必须在仓库应用中使用 *领料短缺* 流程。</span><span class="sxs-lookup"><span data-stu-id="e8509-127">The warehouse worker must use the *Short picking* process in the warehouse app.</span></span> <span data-ttu-id="e8509-128">如果您尝试从同一位置为多个批次领料，还可以在仓库应用中使用 **完全** 选项。</span><span class="sxs-lookup"><span data-stu-id="e8509-128">If you're trying to pick multiple batches from the same location, you can also use the **Full** option in the warehouse app.</span></span>

## <a name="i-cant-move-inventory-to-a-location-that-is-license-platecontrolled"></a><span data-ttu-id="e8509-129">我无法将库存移动到牌照控制的位置。</span><span class="sxs-lookup"><span data-stu-id="e8509-129">I can't move inventory to a location that is license plate–controlled.</span></span>

### <a name="issue-description"></a><span data-ttu-id="e8509-130">问题描述</span><span class="sxs-lookup"><span data-stu-id="e8509-130">Issue description</span></span>

<span data-ttu-id="e8509-131">您不能减少负荷上的已领料数量。</span><span class="sxs-lookup"><span data-stu-id="e8509-131">You can't reduce picked quantities on a load.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="e8509-132">解决问题</span><span class="sxs-lookup"><span data-stu-id="e8509-132">Issue resolution</span></span>

<span data-ttu-id="e8509-133">在早期版本中，您不能减少负荷上的已领料数量。</span><span class="sxs-lookup"><span data-stu-id="e8509-133">In earlier versions, you can't reduce picked quantities on a load.</span></span> <span data-ttu-id="e8509-134">但是，现在您可以取消牌照控制的位置的领料。</span><span class="sxs-lookup"><span data-stu-id="e8509-134">However, you can now unpick to a license plate–controlled location.</span></span> <span data-ttu-id="e8509-135">您必须在 **减少领料数量** 页上为负荷行指定 **位置** 值和 **牌照** 值。</span><span class="sxs-lookup"><span data-stu-id="e8509-135">You must specify both a **Location** value and a **License plate** value for the load line on the **Reduce picked quantity** page.</span></span>

## <a name="can-i-print-a-delivery-note-or-packing-content-by-warehouse"></a><span data-ttu-id="e8509-136">我可以按仓库打印交货通知或打包内容吗？</span><span class="sxs-lookup"><span data-stu-id="e8509-136">Can I print a delivery note or packing content by warehouse?</span></span>

### <a name="issue-description"></a><span data-ttu-id="e8509-137">问题描述</span><span class="sxs-lookup"><span data-stu-id="e8509-137">Issue description</span></span>

<span data-ttu-id="e8509-138">您要在 **工作审计模板行更新** 页上按仓库或站点打印交货通知或打包内容。</span><span class="sxs-lookup"><span data-stu-id="e8509-138">You want to print a delivery note or packing content by warehouse or site on the **Work audit template line update** page.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="e8509-139">解决问题</span><span class="sxs-lookup"><span data-stu-id="e8509-139">Issue resolution</span></span>

<span data-ttu-id="e8509-140">使用“打印管理”设置打印文档时，请通过“打印管理”限制范围（站点/仓库），而不要在 **工作审计模板行更新** 页上选择 **编辑打印设置**。</span><span class="sxs-lookup"><span data-stu-id="e8509-140">When you print a document by using Print management settings, limit the scope (site/warehouse) through Print management instead of by selecting **Edit print settings** on the **Work audit template line update** page.</span></span>

## <a name="i-cant-cancel-a-packing-slip-after-its-posted-from-a-sales-order"></a><span data-ttu-id="e8509-141">装箱单从销售订单过帐后，我无法取消。</span><span class="sxs-lookup"><span data-stu-id="e8509-141">I can't cancel a packing slip after it's posted from a sales order.</span></span>

### <a name="issue-description"></a><span data-ttu-id="e8509-142">问题描述</span><span class="sxs-lookup"><span data-stu-id="e8509-142">Issue description</span></span>

<span data-ttu-id="e8509-143">为 WMS 启用了领料和装运流程后，无法取消从销售订单过帐的装箱单。</span><span class="sxs-lookup"><span data-stu-id="e8509-143">When picking and shipping processes are enabled for WMS, you can't cancel a packing slip after it's posted from a sales order.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="e8509-144">解决问题</span><span class="sxs-lookup"><span data-stu-id="e8509-144">Issue resolution</span></span>

<span data-ttu-id="e8509-145">要更正已启用 WMS 的物料的已过帐装箱单，必须从负荷而不是从订单进行过帐。</span><span class="sxs-lookup"><span data-stu-id="e8509-145">To correct posted packing slips for items that are enabled for WMS, the posting must occur from the load, not from the order.</span></span> <span data-ttu-id="e8509-146">Microsoft 已评估此问题，确定了这是一项功能限制。</span><span class="sxs-lookup"><span data-stu-id="e8509-146">Microsoft has evaluated this issue and has determined that it's a feature limitation.</span></span> <span data-ttu-id="e8509-147">通常，通过仓库管理流程领料和装运的销售订单可以从负荷或装运以及销售订单文档本身更新装箱单。</span><span class="sxs-lookup"><span data-stu-id="e8509-147">In general, a sales order that has been picked and shipped through warehouse management processes can be packing slip–updated from the load or shipment and the sales order document itself.</span></span> <span data-ttu-id="e8509-148">但是，如果从销售订单文档对销售订单进行装箱单更新，装箱单冲销仍然无法从负荷或销售订单进行。</span><span class="sxs-lookup"><span data-stu-id="e8509-148">However, if you packing slip–update the sales order from the sales order document, packing slip reversal still can't be done from the load or sales order.</span></span> <span data-ttu-id="e8509-149">因此，我们建议您从负荷使用装箱单过帐。</span><span class="sxs-lookup"><span data-stu-id="e8509-149">Therefore, we recommend that you use the packing slip posting from the load.</span></span> <span data-ttu-id="e8509-150">在这种情况下，将启用必须从负荷进行的冲销。</span><span class="sxs-lookup"><span data-stu-id="e8509-150">In this case, the reversal that must be done from the load will be enabled.</span></span>

## <a name="i-receive-the-following-error-message-not-enough-work-can-be-found-for-cluster"></a><span data-ttu-id="e8509-151">我收到以下错误消息：“找不到足够的工作来建立群集。”</span><span class="sxs-lookup"><span data-stu-id="e8509-151">I receive the following error message: "Not enough work can be found for cluster."</span></span>

### <a name="issue-description"></a><span data-ttu-id="e8509-152">问题描述</span><span class="sxs-lookup"><span data-stu-id="e8509-152">Issue description</span></span>

<span data-ttu-id="e8509-153">当您使用 *系统导向的群集领料* 流程时，如果您配置了一个群集配置文件，例如可以在配置文件中为 10 个位置领料，那么当有足够的工作可以为 10 个位置领料时，该流程将按计划运行。</span><span class="sxs-lookup"><span data-stu-id="e8509-153">When you use the *System directed cluster picking* process, if you configure a cluster profile where, for example, 10 positions can be picked, the process works as planned when there is enough work to pick to 10 positions.</span></span> <span data-ttu-id="e8509-154">但是，如果只有八个位置要领料，您会收到此错误消息，因为一个群集的工作不足。</span><span class="sxs-lookup"><span data-stu-id="e8509-154">However, if there are only eight positions to pick, you receive this error message, because there isn't enough work for one cluster.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="e8509-155">解决问题</span><span class="sxs-lookup"><span data-stu-id="e8509-155">Issue resolution</span></span>

<span data-ttu-id="e8509-156">要解决此问题，请编辑群集配置文件，将 **激活位置** 选项设置为 *否*。</span><span class="sxs-lookup"><span data-stu-id="e8509-156">To fix this issue, edit the cluster profile, and set the **Activate positions** option to *No*.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]