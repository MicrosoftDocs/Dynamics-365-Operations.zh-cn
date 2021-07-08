---
title: 您无法确认装运，因为物料尚未领取
description: 您无法确认装运，因为物料尚未领取
author: perlynne
ms.date: 04/21/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: lbc
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: f3ebd47ffc85d4ca257b404579d60d679f7929b6
ms.sourcegitcommit: f9b145ef4a81cec81f420871b4130b05db4f4500
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/23/2021
ms.locfileid: "6301297"
---
# <a name="you-cant-confirm-a-shipment-because-items-havent-been-picked"></a><span data-ttu-id="d479e-103">您无法确认装运，因为物料尚未领取</span><span class="sxs-lookup"><span data-stu-id="d479e-103">You can't confirm a shipment because items haven't been picked</span></span>

<span data-ttu-id="d479e-104">错误代码：LoadNotPickedAndMovedToFinalShippingLocation</span><span class="sxs-lookup"><span data-stu-id="d479e-104">Error code: LoadNotPickedAndMovedToFinalShippingLocation</span></span>

## <a name="symptoms"></a><span data-ttu-id="d479e-105">故障特征</span><span class="sxs-lookup"><span data-stu-id="d479e-105">Symptoms</span></span>

<span data-ttu-id="d479e-106">当您尝试确认装运时，系统显示以下错误消息：</span><span class="sxs-lookup"><span data-stu-id="d479e-106">When you try to confirm a shipment, the system shows the following error message:</span></span>

> <span data-ttu-id="d479e-107">负荷 %1 所需的部分物料尚未领料并且已移至最终装运库位。</span><span class="sxs-lookup"><span data-stu-id="d479e-107">Some of the items that are needed for load %1 have not yet been picked and moved to the final shipping location.</span></span>

<span data-ttu-id="d479e-108">因此，您无法确认负荷的装运。</span><span class="sxs-lookup"><span data-stu-id="d479e-108">Therefore, you can't confirm the shipment for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="d479e-109">原因</span><span class="sxs-lookup"><span data-stu-id="d479e-109">Cause</span></span>

<span data-ttu-id="d479e-110">负荷或装运无法在其当前状态下确认，因为可能存在以下其中一种情况：</span><span class="sxs-lookup"><span data-stu-id="d479e-110">The load or shipment can't be confirmed in its current state because one of the following conditions might exist:</span></span>

- <span data-ttu-id="d479e-111">相关工作尚未领取并被移至最终装运位置。</span><span class="sxs-lookup"><span data-stu-id="d479e-111">The related work hasn't yet been picked and moved to the final shipping location.</span></span>
- <span data-ttu-id="d479e-112">领取的工作数量与负荷行上创建的工作数量不匹配。</span><span class="sxs-lookup"><span data-stu-id="d479e-112">The picked work quantity doesn't match the created work quantity on the load line.</span></span>
- <span data-ttu-id="d479e-113">在使用波次模板集装化时，库位指令已配置为作为最终装运库位的包装库位。</span><span class="sxs-lookup"><span data-stu-id="d479e-113">The location directive has been configured with packing location as the final shipping location while using Wave template containerization.</span></span>

## <a name="resolution"></a><span data-ttu-id="d479e-114">解决方法</span><span class="sxs-lookup"><span data-stu-id="d479e-114">Resolution</span></span>

<span data-ttu-id="d479e-115">负荷或装运当前处于装运确认失败的状态。</span><span class="sxs-lookup"><span data-stu-id="d479e-115">The load or shipment is currently in a state where shipment confirmation fails.</span></span> <span data-ttu-id="d479e-116">要解决此问题，请完成以下任务之一：</span><span class="sxs-lookup"><span data-stu-id="d479e-116">To fix this issue, complete one of the following tasks:</span></span>

- <span data-ttu-id="d479e-117">查看您的负荷行并确保所有相关工作已在最终装运库位完成，并且数量匹配。</span><span class="sxs-lookup"><span data-stu-id="d479e-117">Review your load lines and make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>
- <span data-ttu-id="d479e-118">取消使用包装库位作为最终装运库位创建的工作 ID，重新配置库位指令，并重新发放负荷。</span><span class="sxs-lookup"><span data-stu-id="d479e-118">Cancel the work IDs that have been created with the packing location as the final shipping location, reconfigure the location directive, and rerelease the load.</span></span>

### <a name="review-your-load-lines-and-make-sure-that-all-the-related-work-has-been-completed-at-the-final-shipping-location-and-that-the-quantities-match"></a><span data-ttu-id="d479e-119">查看您的负荷行并确保所有相关工作已在最终装运库位完成，并且数量匹配</span><span class="sxs-lookup"><span data-stu-id="d479e-119">Review your load lines and make sure that all the related work has been completed at the final shipping location, and that the quantities match</span></span>

<span data-ttu-id="d479e-120">使用以下过程查看您的负荷行，并确保所有相关工作已在最终装运库位完成，并且数量匹配。</span><span class="sxs-lookup"><span data-stu-id="d479e-120">Use the following procedure to review your load lines and make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>

1. <span data-ttu-id="d479e-121">转到 **仓库管理 \> 负荷 \> 所有负荷**。</span><span class="sxs-lookup"><span data-stu-id="d479e-121">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="d479e-122">选择无法确认装运的负荷。</span><span class="sxs-lookup"><span data-stu-id="d479e-122">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="d479e-123">在 **负荷行** 快速选项卡上，选择负荷行。</span><span class="sxs-lookup"><span data-stu-id="d479e-123">On the **Load lines** FastTab, select the load line.</span></span>
1. <span data-ttu-id="d479e-124">记下 **创建的工作数量** 字段的值。</span><span class="sxs-lookup"><span data-stu-id="d479e-124">Make a note of the value of the **Work created quantity** field.</span></span>
1. <span data-ttu-id="d479e-125">在操作窗格的 **负荷** 选项卡上的 **相关信息** 组中，选择 **工作**。</span><span class="sxs-lookup"><span data-stu-id="d479e-125">On the Action Pane, on the **Loads** tab, in the **Related information** group, select **Work**.</span></span>
1. <span data-ttu-id="d479e-126">验证工作已在最终装运位置完成，并且所领取的工作数量与负荷行上创建的工作数量匹配。</span><span class="sxs-lookup"><span data-stu-id="d479e-126">Verify that the work has been completed at the final shipping location, and that the picked work quantity matches the created work quantity on the load line.</span></span>
1. <span data-ttu-id="d479e-127">对所有负荷行重复此过程，确保满足所有条件。</span><span class="sxs-lookup"><span data-stu-id="d479e-127">Repeat this procedure for all load lines to make sure that all criteria are met.</span></span>

### <a name="cancel-the-work-ids-that-have-been-created-with-the-packing-location-as-the-final-shipping-location-reconfigure-the-location-directive-and-rerelease-the-load"></a><span data-ttu-id="d479e-128">取消使用包装库位作为最终装运库位创建的工作 ID，重新配置库位指令，并重新发放负荷</span><span class="sxs-lookup"><span data-stu-id="d479e-128">Cancel the work IDs that have been created with the packing location as the final shipping location, reconfigure the location directive, and rerelease the load</span></span>

<span data-ttu-id="d479e-129">使用以下过程取消使用包装库位作为最终放置库位并采用自动集装化的工作 ID。</span><span class="sxs-lookup"><span data-stu-id="d479e-129">Use the following procedure to cancel the work IDs that have the packing location as the final put location with automated containerization in place.</span></span>

1. <span data-ttu-id="d479e-130">转到 **仓库管理 \> 定期任务 \> 清理 \> 取消工作**。</span><span class="sxs-lookup"><span data-stu-id="d479e-130">Go to **Warehouse management \> Periodic tasks \> Clean up \> Cancel work**.</span></span>
1. <span data-ttu-id="d479e-131">将打开 **取消工作** 对话框。</span><span class="sxs-lookup"><span data-stu-id="d479e-131">The **Cancel work** dialog opens.</span></span> <span data-ttu-id="d479e-132">在 **工作 ID** 字段中，指定要取消的工作的 ID。</span><span class="sxs-lookup"><span data-stu-id="d479e-132">In the **Work ID** field, specify the ID of the work that you want to cancel.</span></span> <span data-ttu-id="d479e-133">选定的工作 ID 必须具有 *打开*、*进行中*、*已取消*、*已合并* 或 *已关闭* 的 **工作状态** 值。</span><span class="sxs-lookup"><span data-stu-id="d479e-133">The selected work ID must have a **Work status** value of *Open*, *In progress*, *Canceled*, *Combined*, or *Closed*.</span></span>
1. <span data-ttu-id="d479e-134">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="d479e-134">Select **OK**.</span></span>
1. <span data-ttu-id="d479e-135">选择 **是** 确认要取消该工作。</span><span class="sxs-lookup"><span data-stu-id="d479e-135">Select **Yes** to confirm that you want to cancel the work.</span></span>
1. <span data-ttu-id="d479e-136">根据需要对其他工作 ID 重复此过程。</span><span class="sxs-lookup"><span data-stu-id="d479e-136">Repeat this procedure for the other work IDs as needed.</span></span>

<span data-ttu-id="d479e-137">有关详细信息，请参阅[取消要进行异常处理的仓库工作](../../warehousing/cancel-warehouse-work.md)。</span><span class="sxs-lookup"><span data-stu-id="d479e-137">For more information, see [Cancel warehouse work for exception handling](../../warehousing/cancel-warehouse-work.md).</span></span>

<span data-ttu-id="d479e-138">使用以下过程重新配置库位指令，以便在为波次模板设置自动集装化时不会使用包装库位作为最终装运库位。</span><span class="sxs-lookup"><span data-stu-id="d479e-138">Use the following procedure to reconfigure the location directive so it won't use the packing location as the final shipping location when automated containerization is set up for the wave template.</span></span>

1. <span data-ttu-id="d479e-139">转到 **库存管理 \> 设置 \> 位置指令**。</span><span class="sxs-lookup"><span data-stu-id="d479e-139">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="d479e-140">在 **工作订单类型** 字段中，选择 *销售订单*。</span><span class="sxs-lookup"><span data-stu-id="d479e-140">In the **Work order type** field, select *Sales orders*.</span></span>
1. <span data-ttu-id="d479e-141">选择用于自动集装化的库位指令。</span><span class="sxs-lookup"><span data-stu-id="d479e-141">Select the location directive you are using for automated containerization.</span></span>
1. <span data-ttu-id="d479e-142">在 **库位指令操作** 快速选项卡工具栏上，选择 **编辑查询**。</span><span class="sxs-lookup"><span data-stu-id="d479e-142">On the **Location Directive Actions** FastTab toolbar, select **Edit query**.</span></span>
1. <span data-ttu-id="d479e-143">在查询编辑器对话框中的 **范围** 选项卡上，找到 **字段** 设置为 *库位配置文件* 的行，验证该行的 **条件** 字段未设置为 **库位类型** 为 *包装* 的库位配置文件。</span><span class="sxs-lookup"><span data-stu-id="d479e-143">In the query editor dialog, on the **Range** tab, find the row where **Field** is set to *Location profile*, and verify that the **Criteria** field for that row is not set to a location profile that has a **Location type** of *Packing*.</span></span> <span data-ttu-id="d479e-144">调整 **条件** 字段以更正最终放置库位。</span><span class="sxs-lookup"><span data-stu-id="d479e-144">Adjust the **Criteria** field to correct the final put location.</span></span>

<span data-ttu-id="d479e-145">使用以下过程重新发放负荷并创建具有正确最终装运库位的工作 ID。</span><span class="sxs-lookup"><span data-stu-id="d479e-145">Use the following procedure to rerelease the load and create work IDs with the correct final shipping location.</span></span>

1. <span data-ttu-id="d479e-146">转到 **仓库管理 \> 装载 \> 装载计划工作台**。</span><span class="sxs-lookup"><span data-stu-id="d479e-146">Go to **Warehouse management \> Loads \> Load planning workbench**.</span></span>
1. <span data-ttu-id="d479e-147">在 **负荷** 部分中，查找需要发放的负荷。</span><span class="sxs-lookup"><span data-stu-id="d479e-147">In the **Loads** section, find the load that needs to be released.</span></span>
1. <span data-ttu-id="d479e-148">在 **负荷** 部分工具栏上，选择 **发放 \> 发放到仓库** 以将选定负荷发放到仓库。</span><span class="sxs-lookup"><span data-stu-id="d479e-148">On the **Loads** section toolbar, select **Release \> Release to warehouse** to release the selected load to the warehouse.</span></span>
1. <span data-ttu-id="d479e-149">根据需要对其他负荷重复此过程。</span><span class="sxs-lookup"><span data-stu-id="d479e-149">Repeat this procedure for the other loads as needed.</span></span>
