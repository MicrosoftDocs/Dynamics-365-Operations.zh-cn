---
title: 在装箱单生成期间领料数量不足
description: 当生成装箱单时，出站负荷包含的领料数量与负荷行上创建的工作数量不匹配。
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
ms.openlocfilehash: fa6054dc26e4306ec16e37b0e6c320342ed40fe0
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/14/2021
ms.locfileid: "6249066"
---
# <a name="picked-quantity-isnt-sufficient-during-packing-slip-generation"></a><span data-ttu-id="74d6c-103">在装箱单生成期间领料数量不足</span><span class="sxs-lookup"><span data-stu-id="74d6c-103">Picked quantity isn't sufficient during packing slip generation</span></span>

<span data-ttu-id="74d6c-104">错误代码：SYS54073</span><span class="sxs-lookup"><span data-stu-id="74d6c-104">Error code: SYS54073</span></span>

## <a name="symptoms"></a><span data-ttu-id="74d6c-105">故障特征</span><span class="sxs-lookup"><span data-stu-id="74d6c-105">Symptoms</span></span>

<span data-ttu-id="74d6c-106">当生成装箱单时，出站负荷包含的领料数量与负荷行上创建的工作数量不匹配。</span><span class="sxs-lookup"><span data-stu-id="74d6c-106">When you generate a packing slip, the outbound load contains a picked quantity that doesn't match the created work quantity on the load line.</span></span>

<span data-ttu-id="74d6c-107">当您尝试生成装箱单时，系统显示以下错误消息：</span><span class="sxs-lookup"><span data-stu-id="74d6c-107">When you try to generate a packing slip, the system shows the following error message:</span></span>

> <span data-ttu-id="74d6c-108">由于已领取 %1，如果后面的余额必须是 %3，则不足以更新 %2。</span><span class="sxs-lookup"><span data-stu-id="74d6c-108">As %1 have been picked, it is not sufficient to update %2, when, subsequently, the remainder must be %3.</span></span>

<span data-ttu-id="74d6c-109">因此，您无法为负荷生成装箱单。</span><span class="sxs-lookup"><span data-stu-id="74d6c-109">Therefore, you can't generate the packing slip for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="74d6c-110">原因</span><span class="sxs-lookup"><span data-stu-id="74d6c-110">Cause</span></span>

<span data-ttu-id="74d6c-111">装箱单无法在其当前状态下生成，因为可能存在以下一种情况：</span><span class="sxs-lookup"><span data-stu-id="74d6c-111">The packing slip can't be generated in its current state because one of the following conditions might exist:</span></span>

- <span data-ttu-id="74d6c-112">相关工作尚未领取并被移至最终装运位置。</span><span class="sxs-lookup"><span data-stu-id="74d6c-112">The related work hasn't yet been picked and moved to the final shipping location.</span></span>
- <span data-ttu-id="74d6c-113">领取的工作数量与负荷行上创建的工作数量不匹配。</span><span class="sxs-lookup"><span data-stu-id="74d6c-113">The picked work quantity doesn't match the created work quantity on the load line.</span></span>
- <span data-ttu-id="74d6c-114">负荷行数量、工作创建数量和领料数量不匹配。</span><span class="sxs-lookup"><span data-stu-id="74d6c-114">The load line quantity, work created quantity, and picked quantity don't match.</span></span>

## <a name="resolution"></a><span data-ttu-id="74d6c-115">解决方法</span><span class="sxs-lookup"><span data-stu-id="74d6c-115">Resolution</span></span>

<span data-ttu-id="74d6c-116">负荷或装运当前处于装箱单生成失败的状态。</span><span class="sxs-lookup"><span data-stu-id="74d6c-116">The load or shipment is currently in a state where packing slip generation fails.</span></span> <span data-ttu-id="74d6c-117">要解决此问题，请完成以下任务之一：</span><span class="sxs-lookup"><span data-stu-id="74d6c-117">To fix this issue, complete one of the following tasks:</span></span>

- <span data-ttu-id="74d6c-118">查看您的负荷行，并确保所有相关工作已在最终装运库位完成，并且数量匹配。</span><span class="sxs-lookup"><span data-stu-id="74d6c-118">Review your load lines, and make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>
- <span data-ttu-id="74d6c-119">调整负荷行数量。</span><span class="sxs-lookup"><span data-stu-id="74d6c-119">Adjust the load line quantity.</span></span>
- <span data-ttu-id="74d6c-120">冲销所有领料登记，然后重新执行领料。</span><span class="sxs-lookup"><span data-stu-id="74d6c-120">Reverse all pick registrations, and redo picking.</span></span>

### <a name="review-your-load-lines-and-make-sure-that-all-the-related-work-has-been-completed-at-the-final-shipping-location-and-that-the-quantities-match"></a><span data-ttu-id="74d6c-121">查看您的负荷行，并确保所有相关工作已在最终装运库位完成，并且数量匹配</span><span class="sxs-lookup"><span data-stu-id="74d6c-121">Review your load lines, and make sure that all the related work has been completed at the final shipping location, and that the quantities match</span></span>

<span data-ttu-id="74d6c-122">使用以下过程查看您的负荷行，并确保所有相关工作已在最终装运库位完成，并且数量匹配。</span><span class="sxs-lookup"><span data-stu-id="74d6c-122">Use the following procedure to review your load lines and make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>

1. <span data-ttu-id="74d6c-123">转到 **仓库管理 \> 负荷 \> 所有负荷**。</span><span class="sxs-lookup"><span data-stu-id="74d6c-123">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="74d6c-124">选择无法为其生成装箱单的负荷。</span><span class="sxs-lookup"><span data-stu-id="74d6c-124">Select the load that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="74d6c-125">在 **负荷行** 快速选项卡上，选择负荷行。</span><span class="sxs-lookup"><span data-stu-id="74d6c-125">On the **Load lines** FastTab, select the load line.</span></span>
1. <span data-ttu-id="74d6c-126">记下 **创建的工作数量** 字段的值。</span><span class="sxs-lookup"><span data-stu-id="74d6c-126">Make a note of the value of the **Work created quantity** field.</span></span>
1. <span data-ttu-id="74d6c-127">在操作窗格的 **负荷** 选项卡上的 **相关信息** 组中，选择 **工作**。</span><span class="sxs-lookup"><span data-stu-id="74d6c-127">On the Action Pane, on the **Loads** tab, in the **Related information** group, select **Work**.</span></span>
1. <span data-ttu-id="74d6c-128">验证工作已在最终装运位置完成，并且所领取的工作数量与负荷行上创建的工作数量匹配。</span><span class="sxs-lookup"><span data-stu-id="74d6c-128">Verify that the work has been completed at the final shipping location, and that the picked work quantity matches the created work quantity on the load line.</span></span>
1. <span data-ttu-id="74d6c-129">对所有负荷行重复此过程，确保满足所有条件。</span><span class="sxs-lookup"><span data-stu-id="74d6c-129">Repeat this procedure for all load lines to make sure that all criteria are met.</span></span>

### <a name="adjust-the-load-line-quantity"></a><span data-ttu-id="74d6c-130">调整负荷行数量</span><span class="sxs-lookup"><span data-stu-id="74d6c-130">Adjust the load line quantity</span></span>

<span data-ttu-id="74d6c-131">使用以下过程调整负荷行数量。</span><span class="sxs-lookup"><span data-stu-id="74d6c-131">Use the following procedure to adjust the load line quantity.</span></span>

1. <span data-ttu-id="74d6c-132">转到 **仓库管理 \> 负荷 \> 所有负荷**。</span><span class="sxs-lookup"><span data-stu-id="74d6c-132">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="74d6c-133">选择无法为其生成装箱单的负荷。</span><span class="sxs-lookup"><span data-stu-id="74d6c-133">Select the load that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="74d6c-134">在操作窗格上的 **装运和收货** 选项卡上，在 **冲销** 组中，选择 **冲销装运确认**。</span><span class="sxs-lookup"><span data-stu-id="74d6c-134">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Reverse shipment confirmation**.</span></span>
1. <span data-ttu-id="74d6c-135">在 **负荷行** 选项卡上，为导致问题的物料选择负荷行。</span><span class="sxs-lookup"><span data-stu-id="74d6c-135">On the **Load lines** tab, select the load line for the item that causes an issue.</span></span>
1. <span data-ttu-id="74d6c-136">选择 **减少领料数量** 以调整领料数量。</span><span class="sxs-lookup"><span data-stu-id="74d6c-136">Select **Reduce picked quantity** to adjust the picked quantity.</span></span>
1. <span data-ttu-id="74d6c-137">设置 **减少负荷行** 字段以反映对负荷行的调整。</span><span class="sxs-lookup"><span data-stu-id="74d6c-137">Set the **Reduce load line** field to reflect adjustments on the load line.</span></span>

### <a name="reverse-all-pick-registrations-and-redo-picking"></a><span data-ttu-id="74d6c-138">冲销所有领料登记，然后重新执行领料</span><span class="sxs-lookup"><span data-stu-id="74d6c-138">Reverse all pick registrations, and redo picking</span></span>

<span data-ttu-id="74d6c-139">因为有人使用了领料登记关闭没有工作的负荷行，因此可能会出现此问题。</span><span class="sxs-lookup"><span data-stu-id="74d6c-139">The issue might occur because someone used pick registration to close a load line without work.</span></span> <span data-ttu-id="74d6c-140">在这种情况下，必须冲销手动领料登记，然后必须使用 Warehouse Management 移动应用完成领料。</span><span class="sxs-lookup"><span data-stu-id="74d6c-140">In this case, manual pick registration must be reversed, and picking must then be completed by using the Warehouse Management mobile app.</span></span>

<span data-ttu-id="74d6c-141">使用以下过程冲销领料登记。</span><span class="sxs-lookup"><span data-stu-id="74d6c-141">Use the following procedure to reverse the pick registration.</span></span>

1. <span data-ttu-id="74d6c-142">转到 **应收帐款 \> 订单 \> 所有订单**。</span><span class="sxs-lookup"><span data-stu-id="74d6c-142">Go to **Accounts receivable \> Orders \> All orders**.</span></span>
1. <span data-ttu-id="74d6c-143">选择无法为其过帐负荷的装箱单的销售订单。</span><span class="sxs-lookup"><span data-stu-id="74d6c-143">Select the sales order for which you can't post a packing slip for the load.</span></span>
1. <span data-ttu-id="74d6c-144">在 **销售订单行** 选项卡上，选择为其完成领料登记的销售订单行。</span><span class="sxs-lookup"><span data-stu-id="74d6c-144">On the **Sales order lines** tab, select the sales order line that pick registration was done for.</span></span>
1. <span data-ttu-id="74d6c-145">选择 **更新行 \> 领料** 以取消领料物料。</span><span class="sxs-lookup"><span data-stu-id="74d6c-145">Select **Update line \> Pick** to unpick the items.</span></span>
