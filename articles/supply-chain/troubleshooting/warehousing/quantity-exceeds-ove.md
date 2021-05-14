---
title: 您无法确认装运，因为数量超过了超交百分比
description: 您无法确认装运，因为数量超过了超交百分比
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
ms.openlocfilehash: c9b5ba8dedb927ee049d7e53e9a666902f563f49
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938430"
---
# <a name="you-cant-confirm-a-shipment-because-the-quantity-exceeds-the-overdelivery-percentage"></a><span data-ttu-id="3c700-103">您无法确认装运，因为数量超过了超交百分比</span><span class="sxs-lookup"><span data-stu-id="3c700-103">You can't confirm a shipment because the quantity exceeds the overdelivery percentage</span></span>

<span data-ttu-id="3c700-104">错误代码：WAX1687</span><span class="sxs-lookup"><span data-stu-id="3c700-104">Error code: WAX1687</span></span>

## <a name="symptoms"></a><span data-ttu-id="3c700-105">故障特征</span><span class="sxs-lookup"><span data-stu-id="3c700-105">Symptoms</span></span>

<span data-ttu-id="3c700-106">当您尝试确认装运时，系统显示以下错误消息：</span><span class="sxs-lookup"><span data-stu-id="3c700-106">When you try to confirm a shipment, the system shows the following error message:</span></span>

> <span data-ttu-id="3c700-107">负荷 %1 的装运无法确认，因为物料 %2 的数量超出了为超交定义的百分比。</span><span class="sxs-lookup"><span data-stu-id="3c700-107">The shipment for load %1 could not be confirmed because the quantity for item %2 exceeds the percentage that is defined for overdelivery.</span></span>

<span data-ttu-id="3c700-108">因此，您无法确认负荷的装运。</span><span class="sxs-lookup"><span data-stu-id="3c700-108">Therefore, you can't confirm the shipment for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="3c700-109">原因</span><span class="sxs-lookup"><span data-stu-id="3c700-109">Cause</span></span>

<span data-ttu-id="3c700-110">负荷或装运的数量仅部分领取。</span><span class="sxs-lookup"><span data-stu-id="3c700-110">The quantity of the load or shipment has been only partially picked.</span></span> <span data-ttu-id="3c700-111">数量当前超出领料数量的百分比数超过了允许的超交百分比。</span><span class="sxs-lookup"><span data-stu-id="3c700-111">The quantity currently exceeds the picked quantity by a percentage that is outside the allowed overdelivery percentage.</span></span>

## <a name="resolution"></a><span data-ttu-id="3c700-112">解决方法</span><span class="sxs-lookup"><span data-stu-id="3c700-112">Resolution</span></span>

<span data-ttu-id="3c700-113">要解决此问题，请完成以下任务之一：</span><span class="sxs-lookup"><span data-stu-id="3c700-113">To fix this issue, complete one of the following tasks:</span></span>

- <span data-ttu-id="3c700-114">设置负荷行数量。</span><span class="sxs-lookup"><span data-stu-id="3c700-114">Set the load line quantity.</span></span>
- <span data-ttu-id="3c700-115">设置超交百分比。</span><span class="sxs-lookup"><span data-stu-id="3c700-115">Set the overdelivery percentage.</span></span>

### <a name="set-the-load-line-quantity"></a><span data-ttu-id="3c700-116">设置负荷行数量</span><span class="sxs-lookup"><span data-stu-id="3c700-116">Set the load line quantity</span></span>

<span data-ttu-id="3c700-117">要设置负荷行数量，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="3c700-117">To set the load line quantity, follow these steps.</span></span>

1. <span data-ttu-id="3c700-118">转到 **仓库管理 \> 负荷 \> 所有负荷**。</span><span class="sxs-lookup"><span data-stu-id="3c700-118">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="3c700-119">选择无法确认装运的负荷。</span><span class="sxs-lookup"><span data-stu-id="3c700-119">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="3c700-120">在 **负荷行** 快速选项卡上，为超出超交百分比的物料选择负荷行。</span><span class="sxs-lookup"><span data-stu-id="3c700-120">On the **Load lines** FastTab, select the load line for the item that exceeds the overdelivery percentage.</span></span>
1. <span data-ttu-id="3c700-121">在 **行详细信息** 快速选项卡上，选择 **订单**。</span><span class="sxs-lookup"><span data-stu-id="3c700-121">On the **Line details** FastTab, select **Order**.</span></span>
1. <span data-ttu-id="3c700-122">在 **数量** 字段中，将值设置为领料数量（即设置为 **创建的工作数量** 值），以可以进行装运确认。</span><span class="sxs-lookup"><span data-stu-id="3c700-122">In the **Quantity** field, set the value to the picked quantity (that is, to the **Work created quantity** value), so that shipment confirmation can occur.</span></span>

### <a name="set-the-overdelivery-percentage"></a><span data-ttu-id="3c700-123">设置超交百分比</span><span class="sxs-lookup"><span data-stu-id="3c700-123">Set the overdelivery percentage</span></span>

<span data-ttu-id="3c700-124">要设置欠交百分比，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="3c700-124">To set the underdelivery percentage, follow these steps.</span></span>

1. <span data-ttu-id="3c700-125">转到 **仓库管理 \> 负荷 \> 所有负荷**。</span><span class="sxs-lookup"><span data-stu-id="3c700-125">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="3c700-126">选择无法确认装运的负荷。</span><span class="sxs-lookup"><span data-stu-id="3c700-126">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="3c700-127">在 **负荷行** 快速选项卡上，为超出超交百分比的物料选择负荷行。</span><span class="sxs-lookup"><span data-stu-id="3c700-127">On the **Load lines** FastTab, select the load line for the item that exceeds the overdelivery percentage.</span></span>
1. <span data-ttu-id="3c700-128">在 **行详细信息** 快速选项卡上，选择 **常规**。</span><span class="sxs-lookup"><span data-stu-id="3c700-128">On the **Line details** FastTab, select **General**.</span></span>
1. <span data-ttu-id="3c700-129">在 **超交** 字段中，将值设置为可接受根据负荷数量领取的数量的更大百分比，以可以进行装运确认。</span><span class="sxs-lookup"><span data-stu-id="3c700-129">In the **Overdelivery** field, set the value to a larger percentage that accommodates the quantity that has been picked against the load quantity, so that shipment confirmation can occur.</span></span>
