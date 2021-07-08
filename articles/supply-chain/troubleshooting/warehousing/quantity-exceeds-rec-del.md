---
title: 您尝试更新的数量超过收货/交货的数量。
description: 生成装箱单时，出站负荷包含的数量超过为销售订单领料和预留的工作数量。
author: GalynaFedorova
ms.date: 5/31/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSSalesPackingSlipPost,WHSLoadPlanningListPage_WHSSalesPackingSlipPost,WHSLoadPlanningWorkbench_WHSSalesPackingSlipPost
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 66d9cd80cc61e00d1d88ab4f59d03054d746cdd9
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/14/2021
ms.locfileid: "6249067"
---
# <a name="quantity-that-youre-trying-to-update-exceeds-the-receiveddelivered-quantity"></a><span data-ttu-id="25c4d-103">您尝试更新的数量超过收货/交货的数量</span><span class="sxs-lookup"><span data-stu-id="25c4d-103">Quantity that you're trying to update exceeds the received/delivered quantity</span></span>

<span data-ttu-id="25c4d-104">错误代码：SYS7676</span><span class="sxs-lookup"><span data-stu-id="25c4d-104">Error code: SYS7676</span></span>

## <a name="symptoms"></a><span data-ttu-id="25c4d-105">故障特征</span><span class="sxs-lookup"><span data-stu-id="25c4d-105">Symptoms</span></span>

<span data-ttu-id="25c4d-106">生成装箱单时，出站负荷包含的数量超过为销售订单领料和预留的工作数量。</span><span class="sxs-lookup"><span data-stu-id="25c4d-106">When you generate a packing slip, the outbound load contains a quantity that exceeds the work quantity that was picked and reserved for the sales order.</span></span>

<span data-ttu-id="25c4d-107">当您尝试生成装箱单时，系统显示以下错误消息：</span><span class="sxs-lookup"><span data-stu-id="25c4d-107">When you try to generate a packing slip, the system shows the following error message:</span></span>

> <span data-ttu-id="25c4d-108">您正尝试更新的数量超过了接收/交付的数量。</span><span class="sxs-lookup"><span data-stu-id="25c4d-108">The quantity that you are trying to update exceeds the quantity received/delivered.</span></span>

<span data-ttu-id="25c4d-109">因此，您无法为负荷生成装箱单。</span><span class="sxs-lookup"><span data-stu-id="25c4d-109">Therefore, you can't generate the packing slip for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="25c4d-110">原因</span><span class="sxs-lookup"><span data-stu-id="25c4d-110">Cause</span></span>

<span data-ttu-id="25c4d-111">领取的工作数量与负荷行上创建的工作数量不匹配。</span><span class="sxs-lookup"><span data-stu-id="25c4d-111">The picked work quantity doesn't match the created work quantity on the load line.</span></span> <span data-ttu-id="25c4d-112">例如，如果负荷行数量、工作创建数量或领料数量不准确，则可能会出现此问题。</span><span class="sxs-lookup"><span data-stu-id="25c4d-112">For example, this issue might occur if the load line quantity, work created quantity, or picked quantity isn't accurate.</span></span>

## <a name="resolution"></a><span data-ttu-id="25c4d-113">解决方法</span><span class="sxs-lookup"><span data-stu-id="25c4d-113">Resolution</span></span>

<span data-ttu-id="25c4d-114">负荷或装运当前处于装箱单生成失败的状态。</span><span class="sxs-lookup"><span data-stu-id="25c4d-114">The load or shipment is currently in a state where packing slip generation fails.</span></span> <span data-ttu-id="25c4d-115">要解决此问题，请完成以下任务之一：</span><span class="sxs-lookup"><span data-stu-id="25c4d-115">To fix this issue, complete one of the following tasks:</span></span>

- <span data-ttu-id="25c4d-116">查看您的负荷行，并确保所有相关工作已在最终装运库位完成，并且数量匹配。</span><span class="sxs-lookup"><span data-stu-id="25c4d-116">Review your load lines, and make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>
- <span data-ttu-id="25c4d-117">调整负荷行数量。</span><span class="sxs-lookup"><span data-stu-id="25c4d-117">Adjust the load line quantity.</span></span>
- <span data-ttu-id="25c4d-118">冲销所有领料登记，然后重新执行领料。</span><span class="sxs-lookup"><span data-stu-id="25c4d-118">Reverse all pick registrations, and redo picking.</span></span>

### <a name="review-your-load-lines-and-make-sure-that-all-the-related-work-has-been-completed-at-the-final-shipping-location-and-that-the-quantities-match"></a><span data-ttu-id="25c4d-119">查看您的负荷行，并确保所有相关工作已在最终装运库位完成，并且数量匹配</span><span class="sxs-lookup"><span data-stu-id="25c4d-119">Review your load lines, and make sure that all the related work has been completed at the final shipping location, and that the quantities match</span></span>

<span data-ttu-id="25c4d-120">使用以下过程查看您的负荷行，并确保所有相关工作已在最终装运库位完成，并且数量匹配。</span><span class="sxs-lookup"><span data-stu-id="25c4d-120">Use the following procedure to review your load lines and make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>

1. <span data-ttu-id="25c4d-121">转到 **仓库管理 \> 负荷 \> 所有负荷**。</span><span class="sxs-lookup"><span data-stu-id="25c4d-121">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="25c4d-122">选择无法生成装运的负荷。</span><span class="sxs-lookup"><span data-stu-id="25c4d-122">Select the load that the shipment can't be generated for.</span></span>
1. <span data-ttu-id="25c4d-123">在 **负荷行** 快速选项卡上，选择负荷行。</span><span class="sxs-lookup"><span data-stu-id="25c4d-123">On the **Load lines** FastTab, select the load line.</span></span>
1. <span data-ttu-id="25c4d-124">记下 **创建的工作数量** 字段的值。</span><span class="sxs-lookup"><span data-stu-id="25c4d-124">Make a note of the value of the **Work created quantity** field.</span></span>
1. <span data-ttu-id="25c4d-125">在操作窗格的 **负荷** 选项卡上的 **相关信息** 组中，选择 **工作**。</span><span class="sxs-lookup"><span data-stu-id="25c4d-125">On the Action Pane, on the **Loads** tab, in the **Related information** group, select **Work**.</span></span>
1. <span data-ttu-id="25c4d-126">验证工作已在最终装运位置完成，并且所领取的工作数量与负荷行上创建的工作数量匹配。</span><span class="sxs-lookup"><span data-stu-id="25c4d-126">Verify that the work has been completed at the final shipping location, and that the picked work quantity matches the created work quantity on the load line.</span></span>
1. <span data-ttu-id="25c4d-127">对所有负荷行重复此过程，确保满足所有条件。</span><span class="sxs-lookup"><span data-stu-id="25c4d-127">Repeat this procedure for all load lines to make sure that all criteria are met.</span></span>

### <a name="adjust-the-load-line-quantity"></a><span data-ttu-id="25c4d-128">调整负荷行数量</span><span class="sxs-lookup"><span data-stu-id="25c4d-128">Adjust the load line quantity</span></span>

<span data-ttu-id="25c4d-129">使用以下过程调整负荷行数量。</span><span class="sxs-lookup"><span data-stu-id="25c4d-129">Use the following procedure to adjust the load line quantity.</span></span>

1. <span data-ttu-id="25c4d-130">转到 **仓库管理 \> 负荷 \> 所有负荷**。</span><span class="sxs-lookup"><span data-stu-id="25c4d-130">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="25c4d-131">选择无法为其生成装箱单的负荷。</span><span class="sxs-lookup"><span data-stu-id="25c4d-131">Select the load that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="25c4d-132">在操作窗格上的 **装运和收货** 选项卡上，在 **冲销** 组中，选择 **冲销装运确认**。</span><span class="sxs-lookup"><span data-stu-id="25c4d-132">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Reverse shipment confirmation**.</span></span>
1. <span data-ttu-id="25c4d-133">在 **负荷行** 选项卡上，为导致问题的物料选择负荷行。</span><span class="sxs-lookup"><span data-stu-id="25c4d-133">On the **Load lines** tab, select the load line for the item that causes an issue.</span></span>
1. <span data-ttu-id="25c4d-134">选择 **减少领料数量** 以调整领料数量。</span><span class="sxs-lookup"><span data-stu-id="25c4d-134">Select **Reduce picked quantity** to adjust the picked quantity.</span></span>
1. <span data-ttu-id="25c4d-135">设置 **减少负荷行** 字段以反映对负荷行的调整。</span><span class="sxs-lookup"><span data-stu-id="25c4d-135">Set the **Reduce load line** field to reflect adjustments on the load line.</span></span>

### <a name="reverse-all-pick-registrations-and-redo-picking"></a><span data-ttu-id="25c4d-136">冲销所有领料登记，然后重新执行领料</span><span class="sxs-lookup"><span data-stu-id="25c4d-136">Reverse all pick registrations, and redo picking</span></span>

<span data-ttu-id="25c4d-137">如果有人使用领料登记关闭没有工作的负荷行，则负荷行数量和领料数量之间可能会出现差异。</span><span class="sxs-lookup"><span data-stu-id="25c4d-137">If someone used pick registration to close a load line without work, a discrepancy can occur between the load line quantity and the picked quantity.</span></span> <span data-ttu-id="25c4d-138">在这种情况下，必须冲销手动领料登记，然后必须使用 Warehouse Management 移动应用完成领料。</span><span class="sxs-lookup"><span data-stu-id="25c4d-138">In this case, manual pick registration must be reversed, and picking must then be completed by using the Warehouse Management mobile app.</span></span>

<span data-ttu-id="25c4d-139">使用以下过程冲销领料登记。</span><span class="sxs-lookup"><span data-stu-id="25c4d-139">Use the following procedure to reverse the pick registration.</span></span>

1. <span data-ttu-id="25c4d-140">转到 **应收帐款 \> 订单 \> 所有订单**。</span><span class="sxs-lookup"><span data-stu-id="25c4d-140">Go to **Accounts receivable \> Orders \> All orders**.</span></span>
1. <span data-ttu-id="25c4d-141">选择无法为其过帐负荷的装箱单的销售订单。</span><span class="sxs-lookup"><span data-stu-id="25c4d-141">Select the sales order for which you can't post a packing slip for the load.</span></span>
1. <span data-ttu-id="25c4d-142">在 **销售订单行** 选项卡上，选择为其完成领料登记的销售订单行。</span><span class="sxs-lookup"><span data-stu-id="25c4d-142">On the **Sales order lines** tab, select the sales order line that pick registration was done for.</span></span>
1. <span data-ttu-id="25c4d-143">选择 **更新行 \> 领料** 以取消领料物料。</span><span class="sxs-lookup"><span data-stu-id="25c4d-143">Select **Update line \> Pick** to unpick the items.</span></span>
