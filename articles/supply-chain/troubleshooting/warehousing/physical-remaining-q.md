---
title: 单位中的实际剩余数量不得为零
description: 当您生成装箱单时，向其提供的数据具有非零库存数量，但销售数量为零。
author: GalynaFedorova
ms.date: 5/31/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadPlanningListPage_WHSSalesPackingSlipPost, WHSLoadTable_WHSSalesPackingSlipPost
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: bfd381160bcfd1e6e5489e16cc22178b8a5142ee
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/14/2021
ms.locfileid: "6248768"
---
# <a name="physical-remaining-quantity-in-the-unit-must-not-be-zero"></a><span data-ttu-id="0e567-103">单位中的实际剩余数量不得为零</span><span class="sxs-lookup"><span data-stu-id="0e567-103">Physical remaining quantity in the unit must not be zero</span></span>

<span data-ttu-id="0e567-104">错误代码：SYS19591</span><span class="sxs-lookup"><span data-stu-id="0e567-104">Error code: SYS19591</span></span>

## <a name="symptoms"></a><span data-ttu-id="0e567-105">故障特征</span><span class="sxs-lookup"><span data-stu-id="0e567-105">Symptoms</span></span>

<span data-ttu-id="0e567-106">当您生成装箱单时，向其提供的数据具有非零库存数量，但销售数量为零。</span><span class="sxs-lookup"><span data-stu-id="0e567-106">When you generate a packing slip, the data that is supplied to it has a non-zero inventory quantity but a zero sales quantity.</span></span>

<span data-ttu-id="0e567-107">当您尝试生成装箱单时，系统显示以下错误消息：</span><span class="sxs-lookup"><span data-stu-id="0e567-107">When you try to generate the packing slip, the system shows the following error message:</span></span>

> <span data-ttu-id="0e567-108">用单位 %1 表示的实际剩余数量不能为零。</span><span class="sxs-lookup"><span data-stu-id="0e567-108">Physical remaining quantity in the unit %1 must be other than zero.</span></span>

<span data-ttu-id="0e567-109">因此，您无法为负荷生成装箱单。</span><span class="sxs-lookup"><span data-stu-id="0e567-109">Therefore, you can't generate the packing slip for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="0e567-110">原因</span><span class="sxs-lookup"><span data-stu-id="0e567-110">Cause</span></span>

<span data-ttu-id="0e567-111">系统评估库存单位中的实际剩余数量和装运单位中的实际剩余数量。</span><span class="sxs-lookup"><span data-stu-id="0e567-111">The system evaluates the physical remaining quantity in the inventory unit and the physical remaining quantity in the shipping unit.</span></span> <span data-ttu-id="0e567-112">如果系统发现装运单位中的实际剩余数量为 0（零），但库存单位中的实际剩余数量不为 0，则无法生成装箱单。</span><span class="sxs-lookup"><span data-stu-id="0e567-112">If the system finds that the physical remaining quantity in the shipping unit is 0 (zero), but the physical remaining quantity in the inventory unit isn't 0, you can't generate the packing slip.</span></span> <span data-ttu-id="0e567-113">例如，如果物料的销售单位和库存单位不同，并且单位之间的转换不准确，则可能会出现此问题。</span><span class="sxs-lookup"><span data-stu-id="0e567-113">For example, this issue might occur if the sales unit and inventory unit for the item differ, and the conversion between units isn't accurate.</span></span>

## <a name="resolution"></a><span data-ttu-id="0e567-114">解决方法</span><span class="sxs-lookup"><span data-stu-id="0e567-114">Resolution</span></span>

<span data-ttu-id="0e567-115">负荷或装运当前处于装箱单生成失败的状态。</span><span class="sxs-lookup"><span data-stu-id="0e567-115">The load or shipment is currently in a state where packing slip generation fails.</span></span> <span data-ttu-id="0e567-116">要解决此问题，请完成以下任务之一：</span><span class="sxs-lookup"><span data-stu-id="0e567-116">To fix this issue, complete one of the following tasks:</span></span>

- <span data-ttu-id="0e567-117">查看您的负荷行，并确保所有相关工作已在最终装运库位完成，并且数量匹配。</span><span class="sxs-lookup"><span data-stu-id="0e567-117">Review your load lines, and make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>
- <span data-ttu-id="0e567-118">查看您的负荷行，并进行调整以确保可以干净地转换数量，而不会出现舍入问题。</span><span class="sxs-lookup"><span data-stu-id="0e567-118">Review your load lines, and make adjustments to ensure that the quantity can be cleanly converted without rounding issues.</span></span>
- <span data-ttu-id="0e567-119">查看您的负荷行，并进行调整以确保单位和数量与单位的小数精度一致。</span><span class="sxs-lookup"><span data-stu-id="0e567-119">Review your load lines, and make adjustments to ensure that the unit and quantity are aligned with the decimal precision of the unit.</span></span>
- <span data-ttu-id="0e567-120">确保库存度量单位小于销售度量单位。</span><span class="sxs-lookup"><span data-stu-id="0e567-120">Make sure that the inventory unit of measure is smaller than the sales unit of measure.</span></span>

### <a name="review-your-load-lines-and-make-sure-that-all-the-related-work-has-been-completed-at-the-final-shipping-location-and-that-the-quantities-match"></a><span data-ttu-id="0e567-121">查看您的负荷行，并确保所有相关工作已在最终装运库位完成，并且数量匹配</span><span class="sxs-lookup"><span data-stu-id="0e567-121">Review your load lines, and make sure that all the related work has been completed at the final shipping location, and that the quantities match</span></span>

<span data-ttu-id="0e567-122">使用以下过程查看您的负荷行，并确保所有相关工作已在最终装运库位完成，并且数量匹配。</span><span class="sxs-lookup"><span data-stu-id="0e567-122">Use the following procedure to review your load lines and make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>

1. <span data-ttu-id="0e567-123">转到 **仓库管理 \> 负荷 \> 所有负荷**。</span><span class="sxs-lookup"><span data-stu-id="0e567-123">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="0e567-124">选择无法确认装运的负荷。</span><span class="sxs-lookup"><span data-stu-id="0e567-124">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="0e567-125">在 **负荷行** 快速选项卡上，选择负荷行。</span><span class="sxs-lookup"><span data-stu-id="0e567-125">On the **Load lines** FastTab, select the load line.</span></span>
1. <span data-ttu-id="0e567-126">记下 **创建的工作数量** 字段的值。</span><span class="sxs-lookup"><span data-stu-id="0e567-126">Make a note of the value of the **Work created quantity** field.</span></span>
1. <span data-ttu-id="0e567-127">在操作窗格的 **负荷** 选项卡上的 **相关信息** 组中，选择 **工作**。</span><span class="sxs-lookup"><span data-stu-id="0e567-127">On the Action Pane, on the **Loads** tab, in the **Related information** group, select **Work**.</span></span>
1. <span data-ttu-id="0e567-128">验证工作已在最终装运位置完成，并且所领取的工作数量与负荷行上创建的工作数量匹配。</span><span class="sxs-lookup"><span data-stu-id="0e567-128">Verify that the work has been completed at the final shipping location, and that the picked work quantity matches the created work quantity on the load line.</span></span>
1. <span data-ttu-id="0e567-129">对所有负荷行重复此过程，确保满足所有条件。</span><span class="sxs-lookup"><span data-stu-id="0e567-129">Repeat this procedure for all load lines to make sure that all criteria are met.</span></span>

### <a name="review-your-load-lines-and-make-adjustments-to-ensure-that-the-quantity-can-be-cleanly-converted-without-rounding-issues"></a><span data-ttu-id="0e567-130">查看您的负荷行，并进行调整以确保可以干净地转换数量，而不会出现舍入问题</span><span class="sxs-lookup"><span data-stu-id="0e567-130">Review your load lines, and make adjustments to ensure that the quantity can be cleanly converted without rounding issues</span></span>

<span data-ttu-id="0e567-131">使用以下过程查看您的负荷行，并进行调整以确保可以干净地转换数量，而不会出现舍入问题。</span><span class="sxs-lookup"><span data-stu-id="0e567-131">Use the following procedure to review your load lines and make adjustments to ensure that the quantity can be cleanly converted without rounding issues.</span></span>

1. <span data-ttu-id="0e567-132">转到 **仓库管理 \> 负荷 \> 所有负荷**。</span><span class="sxs-lookup"><span data-stu-id="0e567-132">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="0e567-133">选择无法为其生成装箱单的负荷。</span><span class="sxs-lookup"><span data-stu-id="0e567-133">Select the load that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="0e567-134">在操作窗格上的 **装运和收货** 选项卡上，在 **冲销** 组中，选择 **冲销装运确认**。</span><span class="sxs-lookup"><span data-stu-id="0e567-134">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Reverse shipment confirmation**.</span></span>
1. <span data-ttu-id="0e567-135">在 **负荷行** 选项卡上，为超过超交的物料选择负荷行。</span><span class="sxs-lookup"><span data-stu-id="0e567-135">On the **Load lines** tab, select the load line for the item that exceeds the over-delivery.</span></span>
1. <span data-ttu-id="0e567-136">选择 **减少领料数量** 以调整领料数量。</span><span class="sxs-lookup"><span data-stu-id="0e567-136">Select **Reduce picked quantity** to adjust the picked quantity.</span></span>
1. <span data-ttu-id="0e567-137">在  **行详细信息** 选项卡上，选择 **订单**。</span><span class="sxs-lookup"><span data-stu-id="0e567-137">On the  **Line details** tab, select **Order**.</span></span>
1. <span data-ttu-id="0e567-138">将 **数量** 字段设置为领料数量（即，**工作创建数量** 字段的值），以便可以继续生成装箱单。</span><span class="sxs-lookup"><span data-stu-id="0e567-138">Set the **Quantity** field to the picked quantity (that is, the value of the **Work created quantity** field), so that packing slip generation can proceed.</span></span>

### <a name="review-your-load-lines-and-make-adjustments-to-ensure-that-the-unit-and-quantity-are-aligned-with-the-decimal-precision-of-the-unit"></a><span data-ttu-id="0e567-139">查看您的负荷行，并进行调整以确保单位和数量与单位的小数精度一致</span><span class="sxs-lookup"><span data-stu-id="0e567-139">Review your load lines, and make adjustments to ensure that the unit and quantity are aligned with the decimal precision of the unit</span></span>

<span data-ttu-id="0e567-140">使用以下过程查看您的负荷行，并进行调整以确保单位和数量与单位的小数精度一致。</span><span class="sxs-lookup"><span data-stu-id="0e567-140">Use the following procedure to review your load lines and make adjustments to ensure that the unit and quantity are aligned with the decimal precision of the unit.</span></span>

1. <span data-ttu-id="0e567-141">转到 **仓库管理 \> 负荷 \> 所有负荷**。</span><span class="sxs-lookup"><span data-stu-id="0e567-141">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="0e567-142">选择无法为其生成装箱单的负荷。</span><span class="sxs-lookup"><span data-stu-id="0e567-142">Select the load that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="0e567-143">在 **负荷行** 快速选项卡上，为导致问题的物料选择负荷行。</span><span class="sxs-lookup"><span data-stu-id="0e567-143">On the **Load lines** FastTab, select the load line for the item that causes an issue.</span></span> <span data-ttu-id="0e567-144">记下 **数量** 和 **单位** 字段的值。</span><span class="sxs-lookup"><span data-stu-id="0e567-144">Make a note of the value of the **Quantity** and **Unit** fields.</span></span>
1. <span data-ttu-id="0e567-145">转到 **组织管理 \> 单位 \> 单位**。</span><span class="sxs-lookup"><span data-stu-id="0e567-145">Go to **Organization administration \> Units \> Units**.</span></span>
1. <span data-ttu-id="0e567-146">选择无法为其生成装箱单的单位。</span><span class="sxs-lookup"><span data-stu-id="0e567-146">Select the unit that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="0e567-147">根据需要调整 **小数精度** 字段的值。</span><span class="sxs-lookup"><span data-stu-id="0e567-147">Adjust the value of the **Decimal precision** field as required.</span></span>

### <a name="make-sure-that-the-inventory-unit-of-measure-is-smaller-than-the-sales-unit-of-measure"></a><span data-ttu-id="0e567-148">确保库存度量单位小于销售度量单位</span><span class="sxs-lookup"><span data-stu-id="0e567-148">Make sure that the inventory unit of measure is smaller than the sales unit of measure</span></span>

<span data-ttu-id="0e567-149">确保库存度量单位小于销售度量单位。</span><span class="sxs-lookup"><span data-stu-id="0e567-149">Make sure that the inventory unit of measure is smaller than the sales unit of measure.</span></span> <span data-ttu-id="0e567-150">根据需要考虑重新配置物料的度量单位。</span><span class="sxs-lookup"><span data-stu-id="0e567-150">Consider reconfiguring the unit of measure for the item as required.</span></span>
