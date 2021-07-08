---
title: 在装箱单生成期间数量超过超交百分比
description: 生成装箱单时，出站负荷包含的数量超过超交百分比。
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
ms.openlocfilehash: 1106322cc3772c1b671b7fa82fb74039c028ba35
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/14/2021
ms.locfileid: "6249064"
---
# <a name="quantity-exceeds-over-delivery-percentage-during-packing-slip-generation"></a><span data-ttu-id="4473f-103">在装箱单生成期间数量超过超交百分比</span><span class="sxs-lookup"><span data-stu-id="4473f-103">Quantity exceeds over-delivery percentage during packing slip generation</span></span>

<span data-ttu-id="4473f-104">错误代码：SYS24920</span><span class="sxs-lookup"><span data-stu-id="4473f-104">Error code: SYS24920</span></span>

## <a name="symptoms"></a><span data-ttu-id="4473f-105">故障特征</span><span class="sxs-lookup"><span data-stu-id="4473f-105">Symptoms</span></span>

<span data-ttu-id="4473f-106">生成装箱单时，出站负荷包含的数量超过超交百分比。</span><span class="sxs-lookup"><span data-stu-id="4473f-106">When you generate a packing slip, the outbound load contains a quantity that exceeds the over-delivery percentage.</span></span>

<span data-ttu-id="4473f-107">当您尝试生成装箱单时，系统显示以下错误消息：</span><span class="sxs-lookup"><span data-stu-id="4473f-107">When you try to generate a packing slip, the system shows the following error message:</span></span>

> <span data-ttu-id="4473f-108">行超交百分比是 %1，但允许的超交百分比只有 %2。</span><span class="sxs-lookup"><span data-stu-id="4473f-108">Overdelivery of line is %1 percent, but the allowed overdelivery is only %2 percent.</span></span>

<span data-ttu-id="4473f-109">因此，您无法为负荷生成装箱单。</span><span class="sxs-lookup"><span data-stu-id="4473f-109">Therefore, you can't generate the packing slip for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="4473f-110">原因</span><span class="sxs-lookup"><span data-stu-id="4473f-110">Cause</span></span>

<span data-ttu-id="4473f-111">负荷或装运的领料数量大于订购数量且不在超交百分比的范围内。</span><span class="sxs-lookup"><span data-stu-id="4473f-111">The picked quantity for the load or shipment is more than the ordered quantity and isn't within the range of the over-delivery percentage.</span></span>

## <a name="resolution"></a><span data-ttu-id="4473f-112">解决方法</span><span class="sxs-lookup"><span data-stu-id="4473f-112">Resolution</span></span>

<span data-ttu-id="4473f-113">负荷或装运当前处于装箱单生成失败的状态。</span><span class="sxs-lookup"><span data-stu-id="4473f-113">The load or shipment is currently in a state where packing slip generation fails.</span></span> <span data-ttu-id="4473f-114">要解决此问题，请完成以下任务之一：</span><span class="sxs-lookup"><span data-stu-id="4473f-114">To fix this issue, complete one of the following tasks:</span></span>

- <span data-ttu-id="4473f-115">调整负荷行数量。</span><span class="sxs-lookup"><span data-stu-id="4473f-115">Adjust the load line quantity.</span></span>
- <span data-ttu-id="4473f-116">调整超交百分比。</span><span class="sxs-lookup"><span data-stu-id="4473f-116">Adjust the over-delivery percentage.</span></span>
- <span data-ttu-id="4473f-117">冲销并进行调整。</span><span class="sxs-lookup"><span data-stu-id="4473f-117">Reverse and make adjustments.</span></span>

### <a name="adjust-the-load-line-quantity"></a><span data-ttu-id="4473f-118">调整负荷行数量</span><span class="sxs-lookup"><span data-stu-id="4473f-118">Adjust the load line quantity</span></span>

<span data-ttu-id="4473f-119">使用以下过程调整负荷行数量。</span><span class="sxs-lookup"><span data-stu-id="4473f-119">Use the following procedure to adjust the load line quantity.</span></span>

1. <span data-ttu-id="4473f-120">转到 **仓库管理 \> 负荷 \> 所有负荷**。</span><span class="sxs-lookup"><span data-stu-id="4473f-120">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="4473f-121">选择无法为其生成装箱单的负荷。</span><span class="sxs-lookup"><span data-stu-id="4473f-121">Select the load that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="4473f-122">在操作窗格上的 **装运和收货** 选项卡上，在 **冲销** 组中，选择 **冲销装运确认**。</span><span class="sxs-lookup"><span data-stu-id="4473f-122">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Reverse shipment confirmation**.</span></span>
1. <span data-ttu-id="4473f-123">在 **负荷行** 选项卡上，为超过超交百分比的物料选择负荷行。</span><span class="sxs-lookup"><span data-stu-id="4473f-123">On the **Load lines** tab, select the load line for the item that exceeds the over-delivery percentage.</span></span>
1. <span data-ttu-id="4473f-124">选择 **减少领料数量** 以调整领料数量。</span><span class="sxs-lookup"><span data-stu-id="4473f-124">Select **Reduce picked quantity** to adjust the picked quantity.</span></span>
1. <span data-ttu-id="4473f-125">在  **行详细信息** 选项卡上，选择 **订单**。</span><span class="sxs-lookup"><span data-stu-id="4473f-125">On the  **Line details** tab, select **Order**.</span></span>
1. <span data-ttu-id="4473f-126">将 **数量** 字段设置为领料数量（即，**工作创建数量** 字段的值），以便可以继续生成装箱单。</span><span class="sxs-lookup"><span data-stu-id="4473f-126">Set the **Quantity** field to the picked quantity (that is, the value of the **Work created quantity** field), so that packing slip generation can proceed.</span></span>

### <a name="adjust-the-over-delivery-percentage"></a><span data-ttu-id="4473f-127">调整超交百分比</span><span class="sxs-lookup"><span data-stu-id="4473f-127">Adjust the over-delivery percentage</span></span>

<span data-ttu-id="4473f-128">使用以下过程调整超交百分比。</span><span class="sxs-lookup"><span data-stu-id="4473f-128">Use the following procedure to adjust the over-delivery percentage.</span></span>

1. <span data-ttu-id="4473f-129">转到 **应收帐款 \> 订单 \> 所有订单**。</span><span class="sxs-lookup"><span data-stu-id="4473f-129">Go to **Accounts receivable \> Orders \> All orders**.</span></span>
1. <span data-ttu-id="4473f-130">选择无法为其过帐负荷的装箱单的销售订单。</span><span class="sxs-lookup"><span data-stu-id="4473f-130">Select the sales order for which you can't post a packing slip for the load.</span></span>
1. <span data-ttu-id="4473f-131">在 **销售订单行** 选项卡上，为超过超交百分比的物料选择销售订单行。</span><span class="sxs-lookup"><span data-stu-id="4473f-131">On the **Sales order lines** tab, select the sales order line for the item that exceeds the over-delivery percentage.</span></span>
1. <span data-ttu-id="4473f-132">在  **行详细信息** 选项卡上，选择 **交货**。</span><span class="sxs-lookup"><span data-stu-id="4473f-132">On the  **Line details** tab, select **Delivery**.</span></span>
1. <span data-ttu-id="4473f-133">将 **超交** 字段设置为可接受根据负荷数量领料的数量的更大百分比，以便可以继续生成装箱单。</span><span class="sxs-lookup"><span data-stu-id="4473f-133">Set the **Overdelivery** field to a larger percentage that accommodates the quantity that was picked against the load quantity, so that packing slip generation can proceed.</span></span>

### <a name="reverse-and-make-adjustments"></a><span data-ttu-id="4473f-134">冲销并进行调整</span><span class="sxs-lookup"><span data-stu-id="4473f-134">Reverse and make adjustments</span></span>

<span data-ttu-id="4473f-135">冲销已为负荷过帐的所有内容（例如，装箱单、装运确认和工作），进行销售订单调整，将订单重新发放到仓库，并完成装运过程。</span><span class="sxs-lookup"><span data-stu-id="4473f-135">Reverse everything that has been posted for the load (for example, the packing slip, shipment confirmation, and work), make sales order adjustments, re-release the order to the warehouse, and complete the shipment procedure.</span></span>

<span data-ttu-id="4473f-136">使用以下过程取消装箱单。</span><span class="sxs-lookup"><span data-stu-id="4473f-136">Use the following procedure to cancel a packing slip.</span></span>

1. <span data-ttu-id="4473f-137">转到 **仓库管理 \> 负荷 \> 所有负荷**。</span><span class="sxs-lookup"><span data-stu-id="4473f-137">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="4473f-138">在操作窗格上的 **装运和收货** 选项卡上，在 **冲销** 组中，选择 **取消装箱单**。</span><span class="sxs-lookup"><span data-stu-id="4473f-138">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Cancel packing slips**.</span></span>

<span data-ttu-id="4473f-139">使用以下过程冲销装运确认。</span><span class="sxs-lookup"><span data-stu-id="4473f-139">Use the following procedure to reverse a shipment confirmation.</span></span>

1. <span data-ttu-id="4473f-140">转到 **仓库管理 \> 负荷 \> 所有负荷**。</span><span class="sxs-lookup"><span data-stu-id="4473f-140">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="4473f-141">在操作窗格上的 **装运和收货** 选项卡上，在 **冲销** 组中，选择 **冲销装运确认**。</span><span class="sxs-lookup"><span data-stu-id="4473f-141">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Reverse shipment confirmation**.</span></span>

<span data-ttu-id="4473f-142">使用以下过程来冲销工作。</span><span class="sxs-lookup"><span data-stu-id="4473f-142">Use the following procedure to reverse work.</span></span>

1. <span data-ttu-id="4473f-143">转到 **仓库管理 \> 负荷 \> 所有负荷**。</span><span class="sxs-lookup"><span data-stu-id="4473f-143">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="4473f-144">在操作窗格上的 **负荷** 选项卡上，在 **工作** 组中，选择 **冲销工作**。</span><span class="sxs-lookup"><span data-stu-id="4473f-144">On the Action Pane, on the **Loads** tab, in the **Work** group, select **Reverse work**.</span></span>
