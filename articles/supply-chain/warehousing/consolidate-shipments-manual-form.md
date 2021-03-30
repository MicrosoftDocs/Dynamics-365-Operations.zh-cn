---
title: 使用合并装运页面手动合并装运
description: 此主题提供以下方案：使用“合并装运”页将多个订单发放到仓库，以后再合并。
author: GarmMSFT
manager: tfehr
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: 6d9186fe242fa56b6a360d6a4e4284c0c3eac141
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5242197"
---
# <a name="consolidate-shipments-manually-by-using-the-consolidate-shipments-page"></a><span data-ttu-id="e65bb-103">使用合并装运页面手动合并装运</span><span class="sxs-lookup"><span data-stu-id="e65bb-103">Consolidate shipments manually by using the Consolidate shipments page</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e65bb-104">此主题提供以下方案：使用 **合并装运** 页将多个订单发放到仓库，以后再合并。</span><span class="sxs-lookup"><span data-stu-id="e65bb-104">This topic presents a scenario where multiple orders are released to the warehouse and then consolidated later by using the **Consolidate shipments** page.</span></span>

## <a name="make-demo-data-available"></a><span data-ttu-id="e65bb-105">提供演示数据</span><span class="sxs-lookup"><span data-stu-id="e65bb-105">Make demo data available</span></span>

<span data-ttu-id="e65bb-106">此主题中的方案引用为 Microsoft Dynamics 365 Supply Chain Management 提供的标准演示数据中包含的值和记录。</span><span class="sxs-lookup"><span data-stu-id="e65bb-106">The scenario in this topic references values and records that are included in the standard demo data that is provided for Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="e65bb-107">如果要在进行此练习时使用此处提供的值，请务必在安装了演示数据的环境中操作，并且在开始前将法人设置为 **USMF**。</span><span class="sxs-lookup"><span data-stu-id="e65bb-107">If you want to use the values that are provided here as you do the exercises, be sure to work in an environment where the demo data is installed, and set the legal entity to **USMF** before you begin.</span></span>

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a><span data-ttu-id="e65bb-108">设置装运合并策略和产品筛选器</span><span class="sxs-lookup"><span data-stu-id="e65bb-108">Set up shipment consolidation policies and product filters</span></span>

<span data-ttu-id="e65bb-109">此处介绍的方案假设已经开启了此功能，完成了[配置装运合并策略](configure-shipment-consolidation-policies.md)中的练习，并创建了其中介绍的策略和其他记录。</span><span class="sxs-lookup"><span data-stu-id="e65bb-109">The scenario that is described here assumes that you've already turned on the feature, done the exercises in [Configure shipment consolidation policies](configure-shipment-consolidation-policies.md), and created the policies and other records that are described there.</span></span> <span data-ttu-id="e65bb-110">务必先完成这些练习，再继续完成此方案。</span><span class="sxs-lookup"><span data-stu-id="e65bb-110">Be sure to do those exercises before you continue with this scenario.</span></span>

## <a name="create-the-sales-orders-for-this-scenario"></a><span data-ttu-id="e65bb-111">为此方案创建销售订单</span><span class="sxs-lookup"><span data-stu-id="e65bb-111">Create the sales orders for this scenario</span></span>

<span data-ttu-id="e65bb-112">首先创建可以使用的销售订单的集合。</span><span class="sxs-lookup"><span data-stu-id="e65bb-112">Start by creating a collection of sales orders that you can work with.</span></span> <span data-ttu-id="e65bb-113">必须使用为高级仓库 (WMS) 流程启用的仓库。</span><span class="sxs-lookup"><span data-stu-id="e65bb-113">You must work with a warehouse that is enabled for advanced warehouse (WMS) processes.</span></span> <span data-ttu-id="e65bb-114">除非明确提及其他仓库，否则必须为下面的每组订单使用同一个仓库。</span><span class="sxs-lookup"><span data-stu-id="e65bb-114">Unless a different warehouse is explicitly mentioned, that same warehouse must be used for each of the following sets of orders.</span></span>

<span data-ttu-id="e65bb-115">转到 **应收帐款 \> 订单 \> 所有销售订单**，然后创建具有以下小节中介绍的设置的销售订单的集合。</span><span class="sxs-lookup"><span data-stu-id="e65bb-115">Go to **Accounts receivable \> Orders \> All sales orders**, and create a collection of sales orders that have the settings that are described in the following subsections.</span></span>

### <a name="create-sales-orders-1-and-2"></a><span data-ttu-id="e65bb-116">创建销售订单 1 和 2</span><span class="sxs-lookup"><span data-stu-id="e65bb-116">Create sales orders 1 and 2</span></span>

1. <span data-ttu-id="e65bb-117">创建具有以下设置的两个相同销售订单：</span><span class="sxs-lookup"><span data-stu-id="e65bb-117">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="e65bb-118">**客户帐户**：*US-007*</span><span class="sxs-lookup"><span data-stu-id="e65bb-118">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="e65bb-119">**池**：*ShipCons*</span><span class="sxs-lookup"><span data-stu-id="e65bb-119">**Pool:** *ShipCons*</span></span>

1. <span data-ttu-id="e65bb-120">添加具有以下设置的订单行：</span><span class="sxs-lookup"><span data-stu-id="e65bb-120">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="e65bb-121">**物料编号**：*A0001*（未为其分配 **代码 4** 筛选器的物料）</span><span class="sxs-lookup"><span data-stu-id="e65bb-121">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="e65bb-122">**数量：** *1.00*</span><span class="sxs-lookup"><span data-stu-id="e65bb-122">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="e65bb-123">选择 **库存 \> 预留**，然后在操作窗格上选择 **预留批次** 预留订单行。</span><span class="sxs-lookup"><span data-stu-id="e65bb-123">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

### <a name="create-sales-orders-3-and-4"></a><span data-ttu-id="e65bb-124">创建销售订单 3 和 4</span><span class="sxs-lookup"><span data-stu-id="e65bb-124">Create sales orders 3 and 4</span></span>

1. <span data-ttu-id="e65bb-125">创建具有以下设置的两个相同销售订单：</span><span class="sxs-lookup"><span data-stu-id="e65bb-125">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="e65bb-126">**客户帐户**：*US-007*</span><span class="sxs-lookup"><span data-stu-id="e65bb-126">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="e65bb-127">**池**：保持此字段为空。</span><span class="sxs-lookup"><span data-stu-id="e65bb-127">**Pool:** Leave this field blank.</span></span>

1. <span data-ttu-id="e65bb-128">添加具有以下设置的订单行：</span><span class="sxs-lookup"><span data-stu-id="e65bb-128">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="e65bb-129">**物料编号**：*A0001*（未为其分配 **代码 4** 筛选器的物料）</span><span class="sxs-lookup"><span data-stu-id="e65bb-129">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="e65bb-130">**数量：** *1.00*</span><span class="sxs-lookup"><span data-stu-id="e65bb-130">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="e65bb-131">选择 **库存 \> 预留**，然后在操作窗格上选择 **预留批次** 预留订单行。</span><span class="sxs-lookup"><span data-stu-id="e65bb-131">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

## <a name="release-the-orders-to-the-warehouse"></a><span data-ttu-id="e65bb-132">将订单发放到仓库</span><span class="sxs-lookup"><span data-stu-id="e65bb-132">Release the orders to the warehouse</span></span>

<span data-ttu-id="e65bb-133">请按照以下步骤将您为此方案创建的每个销售订单发放到仓库。</span><span class="sxs-lookup"><span data-stu-id="e65bb-133">Follow these steps to release each sales order that you created for this scenario to the warehouse.</span></span>

1. <span data-ttu-id="e65bb-134">转到 **应收帐款 \> 订单 \> 全部采购订单**。</span><span class="sxs-lookup"><span data-stu-id="e65bb-134">Go to **Accounts receivable \> Orders \> All sales orders**.</span></span>
1. <span data-ttu-id="e65bb-135">查找并选择要发放的销售订单。</span><span class="sxs-lookup"><span data-stu-id="e65bb-135">Find and select the sales order to release.</span></span>
1. <span data-ttu-id="e65bb-136">在“操作窗格”上的 **仓库** 选项卡上，选择 **操作 \> 发放到仓库** 发放所选销售订单。</span><span class="sxs-lookup"><span data-stu-id="e65bb-136">On the Action Pane, on the **Warehouse** tab, select **Actions \> Release to warehouse** to release the selected sales order.</span></span>
1. <span data-ttu-id="e65bb-137">对为此方案创建的其他每个销售订单集重复此过程。</span><span class="sxs-lookup"><span data-stu-id="e65bb-137">Repeat this procedure for every other sales order that you created for this scenario.</span></span>

## <a name="consolidate-shipments"></a><span data-ttu-id="e65bb-138">合并装运</span><span class="sxs-lookup"><span data-stu-id="e65bb-138">Consolidate shipments</span></span>

1. <span data-ttu-id="e65bb-139">转到 **仓库管理 \> 装运 \> 所有装运**。</span><span class="sxs-lookup"><span data-stu-id="e65bb-139">Go to **Warehouse management \> Shipments \> All shipments**.</span></span>
1. <span data-ttu-id="e65bb-140">找到并选择将销售订单 1 发放到仓库时创建的装运。</span><span class="sxs-lookup"><span data-stu-id="e65bb-140">Find and select a shipment that was created when sales order 1 was released to the warehouse.</span></span> <span data-ttu-id="e65bb-141">（其 **装运合并策略** 字段应设置为 *订单池*。）</span><span class="sxs-lookup"><span data-stu-id="e65bb-141">(Its **Shipment consolidation policy** field should be set to *Order pool*.)</span></span>
1. <span data-ttu-id="e65bb-142">在“操作”窗格上的 **装运** 选项卡中，选择 **装运 \> 合并装运**。</span><span class="sxs-lookup"><span data-stu-id="e65bb-142">On the Action Pane, on the **Shipments** tab, select **Shipments \> Consolidate shipments**.</span></span>
1. <span data-ttu-id="e65bb-143">验证建议合并的装运。</span><span class="sxs-lookup"><span data-stu-id="e65bb-143">Verify the shipments that are suggested for consolidation.</span></span> <span data-ttu-id="e65bb-144">只应建议合并策略相同的一个装运。</span><span class="sxs-lookup"><span data-stu-id="e65bb-144">Only one shipment that has the same policy should be suggested for consolidation.</span></span>
1. <span data-ttu-id="e65bb-145">关闭 **装运合并** 页。</span><span class="sxs-lookup"><span data-stu-id="e65bb-145">Close the **Shipment consolidation** page.</span></span>
1. <span data-ttu-id="e65bb-146">找到并选择将销售订单 3 发放到仓库时创建的装运。</span><span class="sxs-lookup"><span data-stu-id="e65bb-146">Find and select a shipment that was created when sales order 3 was released to the warehouse.</span></span> <span data-ttu-id="e65bb-147">（其 **装运合并策略** 字段应设置为 *默认*。）</span><span class="sxs-lookup"><span data-stu-id="e65bb-147">(Its **Shipment consolidation policy** field should be set to *Default*.)</span></span>
1. <span data-ttu-id="e65bb-148">在“操作”窗格上的 **装运** 选项卡中，选择 **装运 \> 合并装运**。</span><span class="sxs-lookup"><span data-stu-id="e65bb-148">On the Action Pane, on the **Shipments** tab, select **Shipments \> Consolidate shipments**.</span></span>
1. <span data-ttu-id="e65bb-149">验证没有建议要合并的装运。</span><span class="sxs-lookup"><span data-stu-id="e65bb-149">Verify that no shipments are suggested for consolidation.</span></span>
1. <span data-ttu-id="e65bb-150">选择 **显示筛选器**。</span><span class="sxs-lookup"><span data-stu-id="e65bb-150">Select **Show filters**.</span></span>
1. <span data-ttu-id="e65bb-151">在 **筛选器** 窗格中，移除 **订单编号** 筛选器，然后选择 **应用**。</span><span class="sxs-lookup"><span data-stu-id="e65bb-151">In the **Filters** pane, remove the **Order number** filter, and then select **Apply**.</span></span>
1. <span data-ttu-id="e65bb-152">验证建议合并的装运。</span><span class="sxs-lookup"><span data-stu-id="e65bb-152">Verify the shipments that are suggested for consolidation.</span></span> <span data-ttu-id="e65bb-153">只应建议合并策略相同的一个装运。</span><span class="sxs-lookup"><span data-stu-id="e65bb-153">Only one shipment that has the same policy should be suggested for consolidation.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e65bb-154">其他资源</span><span class="sxs-lookup"><span data-stu-id="e65bb-154">Additional resources</span></span>

- [<span data-ttu-id="e65bb-155">装运合并政策</span><span class="sxs-lookup"><span data-stu-id="e65bb-155">Shipment consolidation policies</span></span>](about-shipment-consolidation-policies.md)
- [<span data-ttu-id="e65bb-156">配置装运合并策略</span><span class="sxs-lookup"><span data-stu-id="e65bb-156">Configure shipment consolidation policies</span></span>](configure-shipment-consolidation-policies.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]