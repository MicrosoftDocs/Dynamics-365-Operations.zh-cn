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
ms.openlocfilehash: 23a517e7769dc86ebec30e4f17c62172a6ad8801
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938427"
---
# <a name="you-cant-confirm-a-shipment-because-items-havent-been-picked"></a><span data-ttu-id="319b8-103">您无法确认装运，因为物料尚未领取</span><span class="sxs-lookup"><span data-stu-id="319b8-103">You can't confirm a shipment because items haven't been picked</span></span>

<span data-ttu-id="319b8-104">错误代码：LoadNotPickedAndMovedToFinalShippingLocation</span><span class="sxs-lookup"><span data-stu-id="319b8-104">Error code: LoadNotPickedAndMovedToFinalShippingLocation</span></span>

## <a name="symptoms"></a><span data-ttu-id="319b8-105">故障特征</span><span class="sxs-lookup"><span data-stu-id="319b8-105">Symptoms</span></span>

<span data-ttu-id="319b8-106">当您尝试确认装运时，系统显示以下错误消息：</span><span class="sxs-lookup"><span data-stu-id="319b8-106">When you try to confirm a shipment, the system shows the following error message:</span></span>

> <span data-ttu-id="319b8-107">负荷 %1 所需的部分物料尚未领料并且已移至最终装运库位。</span><span class="sxs-lookup"><span data-stu-id="319b8-107">Some of the items that are needed for load %1 have not yet been picked and moved to the final shipping location.</span></span>

<span data-ttu-id="319b8-108">因此，您无法确认负荷的装运。</span><span class="sxs-lookup"><span data-stu-id="319b8-108">Therefore, you can't confirm the shipment for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="319b8-109">原因</span><span class="sxs-lookup"><span data-stu-id="319b8-109">Cause</span></span>

<span data-ttu-id="319b8-110">负荷或装运无法在其当前状态下确认，因为可能存在以下其中一种情况：</span><span class="sxs-lookup"><span data-stu-id="319b8-110">The load or shipment can't be confirmed in its current state because one of the following conditions might exist:</span></span>

- <span data-ttu-id="319b8-111">相关工作尚未领取并被移至最终装运位置。</span><span class="sxs-lookup"><span data-stu-id="319b8-111">The related work hasn't yet been picked and moved to the final shipping location.</span></span>
- <span data-ttu-id="319b8-112">领取的工作数量与负荷行上创建的工作数量不匹配。</span><span class="sxs-lookup"><span data-stu-id="319b8-112">The picked work quantity doesn't match the created work quantity on the load line.</span></span>

## <a name="resolution"></a><span data-ttu-id="319b8-113">解决方法</span><span class="sxs-lookup"><span data-stu-id="319b8-113">Resolution</span></span>

<span data-ttu-id="319b8-114">检查相关销售订单或转移单的负荷或装运。</span><span class="sxs-lookup"><span data-stu-id="319b8-114">Check the related sales orders or transfer orders for the load or shipment.</span></span> <span data-ttu-id="319b8-115">确保所有相关工作已在最终装运位置完成，并且数量匹配。</span><span class="sxs-lookup"><span data-stu-id="319b8-115">Make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>

1. <span data-ttu-id="319b8-116">转到 **仓库管理 \> 负荷 \> 所有负荷**。</span><span class="sxs-lookup"><span data-stu-id="319b8-116">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="319b8-117">选择无法确认装运的负荷。</span><span class="sxs-lookup"><span data-stu-id="319b8-117">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="319b8-118">在 **负荷行** 快速选项卡上，选择负荷行。</span><span class="sxs-lookup"><span data-stu-id="319b8-118">On the **Load lines** FastTab, select the load line.</span></span>
1. <span data-ttu-id="319b8-119">记下 **创建的工作数量** 字段的值。</span><span class="sxs-lookup"><span data-stu-id="319b8-119">Make a note of the value of the **Work created quantity** field.</span></span>
1. <span data-ttu-id="319b8-120">在操作窗格的 **负荷** 选项卡上的 **相关信息** 组中，选择 **工作**。</span><span class="sxs-lookup"><span data-stu-id="319b8-120">On the Action Pane, on the **Loads** tab, in the **Related information** group, select **Work**.</span></span>
1. <span data-ttu-id="319b8-121">验证工作已在最终装运位置完成，并且所领取的工作数量与负荷行上创建的工作数量匹配。</span><span class="sxs-lookup"><span data-stu-id="319b8-121">Verify that the work has been completed at the final shipping location, and that the picked work quantity matches the created work quantity on the load line.</span></span>
1. <span data-ttu-id="319b8-122">对所有负荷行重复此过程，确保满足所有条件。</span><span class="sxs-lookup"><span data-stu-id="319b8-122">Repeat this procedure for all load lines to make sure that all criteria are met.</span></span>
