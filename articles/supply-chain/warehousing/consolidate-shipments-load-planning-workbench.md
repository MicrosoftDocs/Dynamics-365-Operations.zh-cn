---
title: 使用装载计划工作台中的“发放到仓库”合并装运
description: 此主题提供以下方案：通过同一个装载将多个订单发放到仓库，然后将其合并到装运中。
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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: 2f1dd5c743664e638c043b600ae7b0f6bce5ddcd
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/10/2020
ms.locfileid: "3986832"
---
# <a name="consolidate-shipments-by-using-release-to-warehouse-from-the-load-planning-workbench"></a><span data-ttu-id="b5828-103">使用装载计划工作台中的“发放到仓库”合并装运</span><span class="sxs-lookup"><span data-stu-id="b5828-103">Consolidate shipments by using Release to warehouse from the load planning workbench</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b5828-104">此主题提供以下方案：通过同一个装载将多个订单发放到仓库，然后将其合并到装运中。</span><span class="sxs-lookup"><span data-stu-id="b5828-104">This topic presents a scenario where multiple orders are released to the warehouse in the same load and are then automatically consolidated into shipments.</span></span>

## <a name="make-demo-data-available"></a><span data-ttu-id="b5828-105">提供演示数据</span><span class="sxs-lookup"><span data-stu-id="b5828-105">Make demo data available</span></span>

<span data-ttu-id="b5828-106">此主题中的方案引用为 Microsoft Dynamics 365 Supply Chain Management 提供的标准演示数据中包含的值和记录。</span><span class="sxs-lookup"><span data-stu-id="b5828-106">The scenario in this topic references values and records that are included in the standard demo data that is provided for Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="b5828-107">如果要在进行此练习时使用此处提供的值，请务必在安装了演示数据的环境中操作，并且在开始前将法人设置为 **USMF**。</span><span class="sxs-lookup"><span data-stu-id="b5828-107">If you want to use the values that are provided here as you do the exercises, be sure to work in an environment where the demo data is installed, and set the legal entity to **USMF** before you begin.</span></span>

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a><span data-ttu-id="b5828-108">设置装运合并策略和产品筛选器</span><span class="sxs-lookup"><span data-stu-id="b5828-108">Set up shipment consolidation policies and product filters</span></span>

<span data-ttu-id="b5828-109">此处介绍的方案假设已经开启了此功能，完成了[配置装运合并策略](configure-shipment-consolidation-policies.md)中的练习，并创建了其中介绍的策略和其他记录。</span><span class="sxs-lookup"><span data-stu-id="b5828-109">The scenario that is described here assumes that you've already turned on the feature, done the exercises in [Configure shipment consolidation policies](configure-shipment-consolidation-policies.md), and created the policies and other records that are described there.</span></span> <span data-ttu-id="b5828-110">务必先完成这些练习，再继续完成此方案。</span><span class="sxs-lookup"><span data-stu-id="b5828-110">Be sure to do those exercises before you continue with this scenario.</span></span>

## <a name="create-the-sales-orders-for-this-scenario"></a><span data-ttu-id="b5828-111">为此方案创建销售订单</span><span class="sxs-lookup"><span data-stu-id="b5828-111">Create the sales orders for this scenario</span></span>

<span data-ttu-id="b5828-112">首先创建可以使用的销售订单的集合。</span><span class="sxs-lookup"><span data-stu-id="b5828-112">Start by creating a collection of sales orders that you can work with.</span></span> <span data-ttu-id="b5828-113">必须使用为高级仓库 (WMS) 流程启用的仓库。</span><span class="sxs-lookup"><span data-stu-id="b5828-113">You must work with a warehouse that is enabled for advanced warehouse (WMS) processes.</span></span> <span data-ttu-id="b5828-114">除非明确提及其他仓库，否则必须为下面的每组订单使用同一个仓库。</span><span class="sxs-lookup"><span data-stu-id="b5828-114">Unless a different warehouse is explicitly mentioned, that same warehouse must be used for each of the following sets of orders.</span></span>

<span data-ttu-id="b5828-115">转到**应收帐款 \> 订单 \> 所有销售订单**，然后创建具有以下小节中介绍的设置的销售订单的集合。</span><span class="sxs-lookup"><span data-stu-id="b5828-115">Go to **Accounts receivable \> Orders \> All sales orders**, and create a collection of sales orders that have the settings that are described in the following subsections.</span></span>

### <a name="create-order-set-1"></a><span data-ttu-id="b5828-116">创建订单集 1</span><span class="sxs-lookup"><span data-stu-id="b5828-116">Create order set 1</span></span>

#### <a name="sales-order-1-1"></a><span data-ttu-id="b5828-117">销售订单 1-1</span><span class="sxs-lookup"><span data-stu-id="b5828-117">Sales order 1-1</span></span>

1. <span data-ttu-id="b5828-118">创建具有以下设置的销售订单：</span><span class="sxs-lookup"><span data-stu-id="b5828-118">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="b5828-119">**客户帐户**：*US-001*</span><span class="sxs-lookup"><span data-stu-id="b5828-119">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="b5828-120">**交货方式**：*航空公司-航运*</span><span class="sxs-lookup"><span data-stu-id="b5828-120">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="b5828-121">添加具有以下设置的订单行：</span><span class="sxs-lookup"><span data-stu-id="b5828-121">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="b5828-122">**物料编号**：*A0001*（未为其分配**代码 4** 筛选器的物料）</span><span class="sxs-lookup"><span data-stu-id="b5828-122">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="b5828-123">**数量：** *1.00*</span><span class="sxs-lookup"><span data-stu-id="b5828-123">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="b5828-124">选择**库存 \> 预留**，然后在操作窗格上选择**预留批次**预留订单行。</span><span class="sxs-lookup"><span data-stu-id="b5828-124">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-order-1-2"></a><span data-ttu-id="b5828-125">销售订单 1-2</span><span class="sxs-lookup"><span data-stu-id="b5828-125">Sales order 1-2</span></span>

1. <span data-ttu-id="b5828-126">创建具有以下设置的销售订单：</span><span class="sxs-lookup"><span data-stu-id="b5828-126">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="b5828-127">**客户帐户**：*US-001*</span><span class="sxs-lookup"><span data-stu-id="b5828-127">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="b5828-128">**交货方式**：*航空公司-航运*</span><span class="sxs-lookup"><span data-stu-id="b5828-128">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="b5828-129">添加具有以下设置的订单行：</span><span class="sxs-lookup"><span data-stu-id="b5828-129">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="b5828-130">**物料编号**：*A0001*（未为其分配**代码 4** 筛选器的物料）</span><span class="sxs-lookup"><span data-stu-id="b5828-130">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="b5828-131">**数量：** *1.00*</span><span class="sxs-lookup"><span data-stu-id="b5828-131">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="b5828-132">选择**库存 \> 预留**，然后在操作窗格上选择**预留批次**预留订单行。</span><span class="sxs-lookup"><span data-stu-id="b5828-132">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-order-1-3"></a><span data-ttu-id="b5828-133">销售订单 1-3</span><span class="sxs-lookup"><span data-stu-id="b5828-133">Sales order 1-3</span></span>

1. <span data-ttu-id="b5828-134">创建具有以下设置的销售订单：</span><span class="sxs-lookup"><span data-stu-id="b5828-134">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="b5828-135">**客户帐户**：*US-001*</span><span class="sxs-lookup"><span data-stu-id="b5828-135">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="b5828-136">**交货方式**：*10*</span><span class="sxs-lookup"><span data-stu-id="b5828-136">**Mode of delivery:** *10*</span></span>

1. <span data-ttu-id="b5828-137">添加具有以下设置的订单行：</span><span class="sxs-lookup"><span data-stu-id="b5828-137">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="b5828-138">**物料编号**：*A0001*（未为其分配**代码 4** 筛选器的物料）</span><span class="sxs-lookup"><span data-stu-id="b5828-138">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="b5828-139">**数量：** *1.00*</span><span class="sxs-lookup"><span data-stu-id="b5828-139">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="b5828-140">选择**库存 \> 预留**，然后在操作窗格上选择**预留批次**预留订单行。</span><span class="sxs-lookup"><span data-stu-id="b5828-140">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>
1. <span data-ttu-id="b5828-141">添加第二个具有以下设置的订单行：</span><span class="sxs-lookup"><span data-stu-id="b5828-141">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="b5828-142">**物料编号**：*A0002*（未为其分配**代码 4** 筛选器的物料）</span><span class="sxs-lookup"><span data-stu-id="b5828-142">**Item number:** *A0002* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="b5828-143">**数量：** *1.00*</span><span class="sxs-lookup"><span data-stu-id="b5828-143">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="b5828-144">**交货方式**：*航空公司-航运*</span><span class="sxs-lookup"><span data-stu-id="b5828-144">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="b5828-145">选择**库存 \> 预留**，然后在操作窗格上选择**预留批次**预留第二个订单行。</span><span class="sxs-lookup"><span data-stu-id="b5828-145">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the second order line.</span></span>

### <a name="create-order-set-2"></a><span data-ttu-id="b5828-146">创建订单集 2</span><span class="sxs-lookup"><span data-stu-id="b5828-146">Create order set 2</span></span>

#### <a name="sales-orders-2-1-and-2-2"></a><span data-ttu-id="b5828-147">销售订单 2-1 和 2-2</span><span class="sxs-lookup"><span data-stu-id="b5828-147">Sales orders 2-1 and 2-2</span></span>

1. <span data-ttu-id="b5828-148">创建具有以下设置的两个相同销售订单：</span><span class="sxs-lookup"><span data-stu-id="b5828-148">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="b5828-149">**客户帐户**：*US-002*</span><span class="sxs-lookup"><span data-stu-id="b5828-149">**Customer account:** *US-002*</span></span>

1. <span data-ttu-id="b5828-150">添加具有以下设置的订单行：</span><span class="sxs-lookup"><span data-stu-id="b5828-150">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="b5828-151">**物料编号**：*M9200*（其中的**代码 4** 筛选器设置为*易燃*的物料）</span><span class="sxs-lookup"><span data-stu-id="b5828-151">**Item number:** *M9200* (an item where the **Code 4** filter is set to *Flammable*)</span></span>
    - <span data-ttu-id="b5828-152">**数量：** *1.00*</span><span class="sxs-lookup"><span data-stu-id="b5828-152">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="b5828-153">选择**库存 \> 预留**，然后在操作窗格上选择**预留批次**预留订单行。</span><span class="sxs-lookup"><span data-stu-id="b5828-153">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>
1. <span data-ttu-id="b5828-154">添加第二个具有以下设置的订单行：</span><span class="sxs-lookup"><span data-stu-id="b5828-154">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="b5828-155">**物料编号**：*M9201*（其中的**代码 4** 筛选器设置为*易爆*的物料）</span><span class="sxs-lookup"><span data-stu-id="b5828-155">**Item number:** *M9201* (an item where the **Code 4** filter is set to *Explosive*)</span></span>
    - <span data-ttu-id="b5828-156">**数量：** *1.00*</span><span class="sxs-lookup"><span data-stu-id="b5828-156">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="b5828-157">**交货方式**：*航空公司-航运*</span><span class="sxs-lookup"><span data-stu-id="b5828-157">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="b5828-158">选择**库存 \> 预留**，然后在操作窗格上选择**预留批次**预留第二个订单行。</span><span class="sxs-lookup"><span data-stu-id="b5828-158">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the second order line.</span></span>

### <a name="create-order-set-3"></a><span data-ttu-id="b5828-159">创建订单集 3</span><span class="sxs-lookup"><span data-stu-id="b5828-159">Create order set 3</span></span>

#### <a name="sales-orders-3-1-and-3-2"></a><span data-ttu-id="b5828-160">销售订单 3-1 和 3-2</span><span class="sxs-lookup"><span data-stu-id="b5828-160">Sales orders 3-1 and 3-2</span></span>

1. <span data-ttu-id="b5828-161">创建具有以下设置的两个相同销售订单：</span><span class="sxs-lookup"><span data-stu-id="b5828-161">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="b5828-162">**客户帐户**：*US-001*</span><span class="sxs-lookup"><span data-stu-id="b5828-162">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="b5828-163">**客户申请**：*1*</span><span class="sxs-lookup"><span data-stu-id="b5828-163">**Customer requisition:** *1*</span></span>

1. <span data-ttu-id="b5828-164">添加具有以下设置的订单行：</span><span class="sxs-lookup"><span data-stu-id="b5828-164">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="b5828-165">**物料编号**：*A0001*（未为其分配**代码 4** 筛选器的物料）</span><span class="sxs-lookup"><span data-stu-id="b5828-165">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="b5828-166">**数量：** *1.00*</span><span class="sxs-lookup"><span data-stu-id="b5828-166">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="b5828-167">选择**库存 \> 预留**，然后在操作窗格上选择**预留批次**预留订单行。</span><span class="sxs-lookup"><span data-stu-id="b5828-167">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-3-3-and-3-4"></a><span data-ttu-id="b5828-168">销售订单 3-3 和 3-4</span><span class="sxs-lookup"><span data-stu-id="b5828-168">Sales orders 3-3 and 3-4</span></span>

1. <span data-ttu-id="b5828-169">创建具有以下设置的两个相同销售订单：</span><span class="sxs-lookup"><span data-stu-id="b5828-169">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="b5828-170">**客户帐户**：*US-001*</span><span class="sxs-lookup"><span data-stu-id="b5828-170">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="b5828-171">**客户申请**：*2*</span><span class="sxs-lookup"><span data-stu-id="b5828-171">**Customer requisition:** *2*</span></span>

1. <span data-ttu-id="b5828-172">添加具有以下设置的订单行：</span><span class="sxs-lookup"><span data-stu-id="b5828-172">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="b5828-173">**物料编号**：*A0001*（未为其分配**代码 4** 筛选器的物料）</span><span class="sxs-lookup"><span data-stu-id="b5828-173">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="b5828-174">**数量：** *1.00*</span><span class="sxs-lookup"><span data-stu-id="b5828-174">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="b5828-175">选择**库存 \> 预留**，然后在操作窗格上选择**预留批次**预留订单行。</span><span class="sxs-lookup"><span data-stu-id="b5828-175">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

### <a name="create-order-set-4"></a><span data-ttu-id="b5828-176">创建订单集 4</span><span class="sxs-lookup"><span data-stu-id="b5828-176">Create order set 4</span></span>

#### <a name="sales-orders-4-1-and-4-2"></a><span data-ttu-id="b5828-177">销售订单 4-1 和 4-2</span><span class="sxs-lookup"><span data-stu-id="b5828-177">Sales orders 4-1 and 4-2</span></span>

1. <span data-ttu-id="b5828-178">创建具有以下设置的两个相同销售订单：</span><span class="sxs-lookup"><span data-stu-id="b5828-178">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="b5828-179">**客户帐户**：*US-003*</span><span class="sxs-lookup"><span data-stu-id="b5828-179">**Customer account:** *US-003*</span></span>

1. <span data-ttu-id="b5828-180">添加具有以下设置的订单行：</span><span class="sxs-lookup"><span data-stu-id="b5828-180">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="b5828-181">**物料编号**：*A0001*（未为其分配**代码 4** 筛选器的物料）</span><span class="sxs-lookup"><span data-stu-id="b5828-181">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="b5828-182">**数量：** *1.00*</span><span class="sxs-lookup"><span data-stu-id="b5828-182">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="b5828-183">选择**库存 \> 预留**，然后在操作窗格上选择**预留批次**预留订单行。</span><span class="sxs-lookup"><span data-stu-id="b5828-183">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-4-3-and-4-4"></a><span data-ttu-id="b5828-184">销售订单 4-3 和 4-4</span><span class="sxs-lookup"><span data-stu-id="b5828-184">Sales orders 4-3 and 4-4</span></span>

1. <span data-ttu-id="b5828-185">创建具有以下设置的两个相同销售订单：</span><span class="sxs-lookup"><span data-stu-id="b5828-185">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="b5828-186">**客户帐户**：*US-004*</span><span class="sxs-lookup"><span data-stu-id="b5828-186">**Customer account:** *US-004*</span></span>

1. <span data-ttu-id="b5828-187">添加具有以下设置的订单行：</span><span class="sxs-lookup"><span data-stu-id="b5828-187">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="b5828-188">**物料编号**：*A0001*（未为其分配**代码 4** 筛选器的物料）</span><span class="sxs-lookup"><span data-stu-id="b5828-188">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="b5828-189">**数量：** *1.00*</span><span class="sxs-lookup"><span data-stu-id="b5828-189">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="b5828-190">选择**库存 \> 预留**，然后在操作窗格上选择**预留批次**预留订单行。</span><span class="sxs-lookup"><span data-stu-id="b5828-190">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-4-5-and-4-6"></a><span data-ttu-id="b5828-191">销售订单 4-5 和 4-6</span><span class="sxs-lookup"><span data-stu-id="b5828-191">Sales orders 4-5 and 4-6</span></span>

1. <span data-ttu-id="b5828-192">创建具有以下设置的两个相同销售订单：</span><span class="sxs-lookup"><span data-stu-id="b5828-192">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="b5828-193">**客户帐户**：*US-007*</span><span class="sxs-lookup"><span data-stu-id="b5828-193">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="b5828-194">**站点**：*6*</span><span class="sxs-lookup"><span data-stu-id="b5828-194">**Site:** *6*</span></span>
    - <span data-ttu-id="b5828-195">**仓库**：*61*</span><span class="sxs-lookup"><span data-stu-id="b5828-195">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="b5828-196">**池**：*ShipCons*</span><span class="sxs-lookup"><span data-stu-id="b5828-196">**Pool:** *ShipCons*</span></span>

1. <span data-ttu-id="b5828-197">添加具有以下设置的订单行：</span><span class="sxs-lookup"><span data-stu-id="b5828-197">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="b5828-198">**物料编号**：*A0001*（未为其分配**代码 4** 筛选器的物料）</span><span class="sxs-lookup"><span data-stu-id="b5828-198">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="b5828-199">**数量：** *1.00*</span><span class="sxs-lookup"><span data-stu-id="b5828-199">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="b5828-200">选择**库存 \> 预留**，然后在操作窗格上选择**预留批次**预留订单行。</span><span class="sxs-lookup"><span data-stu-id="b5828-200">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-4-7-and-4-8"></a><span data-ttu-id="b5828-201">销售订单 4-7 和 4-8</span><span class="sxs-lookup"><span data-stu-id="b5828-201">Sales orders 4-7 and 4-8</span></span>

1. <span data-ttu-id="b5828-202">创建具有以下设置的两个相同销售订单：</span><span class="sxs-lookup"><span data-stu-id="b5828-202">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="b5828-203">**客户帐户**：*US-007*</span><span class="sxs-lookup"><span data-stu-id="b5828-203">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="b5828-204">**站点**：*6*</span><span class="sxs-lookup"><span data-stu-id="b5828-204">**Site:** *6*</span></span>
    - <span data-ttu-id="b5828-205">**仓库**：*61*</span><span class="sxs-lookup"><span data-stu-id="b5828-205">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="b5828-206">**池**：保持此字段为空。</span><span class="sxs-lookup"><span data-stu-id="b5828-206">**Pool:** Leave this field blank.</span></span>

1. <span data-ttu-id="b5828-207">添加具有以下设置的订单行：</span><span class="sxs-lookup"><span data-stu-id="b5828-207">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="b5828-208">**物料编号**：*A0001*（未为其分配**代码 4** 筛选器的物料）</span><span class="sxs-lookup"><span data-stu-id="b5828-208">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="b5828-209">**数量：** *1.00*</span><span class="sxs-lookup"><span data-stu-id="b5828-209">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="b5828-210">选择**库存 \> 预留**，然后在操作窗格上选择**预留批次**预留订单行。</span><span class="sxs-lookup"><span data-stu-id="b5828-210">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

## <a name="use-the-load-planning-workbench-to-create-loads-and-release-them-to-the-warehouse"></a><span data-ttu-id="b5828-211">使用装载计划工作台创建装载并将其发放到仓库</span><span class="sxs-lookup"><span data-stu-id="b5828-211">Use the load planning workbench to create loads and release them to the warehouse</span></span>

<span data-ttu-id="b5828-212">请按照以下步骤为您为此方案创建的每个订单集创建一个装载，然后将其发放到仓库。</span><span class="sxs-lookup"><span data-stu-id="b5828-212">Follow these steps to create a load for each order set that you created for this scenario and then release it to the warehouse.</span></span>

1. <span data-ttu-id="b5828-213">转到**仓库管理 \> 装载 \> 装载计划工作台**。</span><span class="sxs-lookup"><span data-stu-id="b5828-213">Go to **Warehouse management \> Loads \> Load planning workbench**.</span></span>
1. <span data-ttu-id="b5828-214">在**销售行**选项卡上，找到并选择为此方案创建的一个订单集中的所有销售订单行。</span><span class="sxs-lookup"><span data-stu-id="b5828-214">On the **Sales lines** tab, find and select all the sales order lines from one of the order sets that you created for this scenario.</span></span>
1. <span data-ttu-id="b5828-215">在操作窗格上的**供应与需求**选项卡中，选择**添加 \> 至新装载**将所选订单行添加到新装载。</span><span class="sxs-lookup"><span data-stu-id="b5828-215">On the Action Pane, on the **Supply and demand** tab, select **Add \> To new load** to add the selected order lines to a new Load.</span></span>
1. <span data-ttu-id="b5828-216">在**装载模板分配**对话框的**装载模板 ID** 字段中，选择一个装载模板，如*标准装载模板*。</span><span class="sxs-lookup"><span data-stu-id="b5828-216">In the **Load template assignment** dialog box, in the **Load template ID** field, select a load template, such as *Stnd Load Template*.</span></span>
1. <span data-ttu-id="b5828-217">选择**确定**关闭对话框。</span><span class="sxs-lookup"><span data-stu-id="b5828-217">Select **OK** to close the dialog box.</span></span> 
1. <span data-ttu-id="b5828-218">在**装载**部分中，找到并选择刚才创建的装载。</span><span class="sxs-lookup"><span data-stu-id="b5828-218">In the **Loads** section, find and select the load that you just created.</span></span>
1. <span data-ttu-id="b5828-219">选择**发放 \> 发放到仓库**将所选装载发放到仓库。</span><span class="sxs-lookup"><span data-stu-id="b5828-219">Select **Release \> Release to warehouse** to release the selected load to the warehouse.</span></span>
1. <span data-ttu-id="b5828-220">对为此方案创建的其他三个订单集重复此过程。</span><span class="sxs-lookup"><span data-stu-id="b5828-220">Repeat this procedure for the other three order sets that you created for this scenario.</span></span>

## <a name="verify-the-shipments"></a><span data-ttu-id="b5828-221">验证装运</span><span class="sxs-lookup"><span data-stu-id="b5828-221">Verify the shipments</span></span>

<span data-ttu-id="b5828-222">以下过程用于验证装运合并导致已创建或更新的装运。</span><span class="sxs-lookup"><span data-stu-id="b5828-222">The following procedure lets you verify the shipments that have been created or updated as a result of shipment consolidation.</span></span> <span data-ttu-id="b5828-223">将其用于查看您为此方案创建的每个订单集，然后查看后面的小节以确保获取了预期结果。</span><span class="sxs-lookup"><span data-stu-id="b5828-223">Use it to review each order set that you created for this scenario, and then review the subsections that follow to make sure that you've obtained the expected results.</span></span>

1. <span data-ttu-id="b5828-224">转到**仓库管理 \> 装运 \> 所有装运**。</span><span class="sxs-lookup"><span data-stu-id="b5828-224">Go to **Warehouse management \> Shipments \> All shipments**.</span></span>
1. <span data-ttu-id="b5828-225">找到并选择所需装运。</span><span class="sxs-lookup"><span data-stu-id="b5828-225">Find and select the required shipment.</span></span>
1. <span data-ttu-id="b5828-226">如果创建或更新装运时使用了合并策略，应该可以在**装运合并策略**字段中看到此策略。</span><span class="sxs-lookup"><span data-stu-id="b5828-226">If a consolidation policy was used when the shipment was created or updated, you should see it in the **Shipment consolidation policy** field.</span></span>

### <a name="release-order-set-1-in-one-load"></a><span data-ttu-id="b5828-227">通过一个装载发放订单集 1</span><span class="sxs-lookup"><span data-stu-id="b5828-227">Release order set 1 in one load</span></span>

<span data-ttu-id="b5828-228">应该已经创建了两个装运：</span><span class="sxs-lookup"><span data-stu-id="b5828-228">Two shipments should have been created:</span></span>

- <span data-ttu-id="b5828-229">第一个装运中包含三行，该装运是使用 *CustomerMode* 装运合并策略创建的。</span><span class="sxs-lookup"><span data-stu-id="b5828-229">The first shipment contains three lines and was created by using the *CustomerMode* shipment consolidation policy.</span></span>
- <span data-ttu-id="b5828-230">第二个装运（该装运不使用*航空公司*交装运输方式）是使用 *CustomerOrderNo* 装运合并策略创建的。</span><span class="sxs-lookup"><span data-stu-id="b5828-230">The second shipment, which doesn't use the *Airways* transportation mode of delivery, was created by using the *CustomerOrderNo* shipment consolidation policy.</span></span>

### <a name="release-order-set-2-in-one-load"></a><span data-ttu-id="b5828-231">通过一个装载发放订单集 2</span><span class="sxs-lookup"><span data-stu-id="b5828-231">Release order set 2 in one load</span></span>

<span data-ttu-id="b5828-232">应该已经创建了三个装运：</span><span class="sxs-lookup"><span data-stu-id="b5828-232">Three shipments should have been created:</span></span>

- <span data-ttu-id="b5828-233">第一个装运中包含*易燃*物品。</span><span class="sxs-lookup"><span data-stu-id="b5828-233">The first shipment contains the *Flammable* items.</span></span>
- <span data-ttu-id="b5828-234">其他两个装运每个包含一行，该行有*易爆*物品。</span><span class="sxs-lookup"><span data-stu-id="b5828-234">Each of the other two shipments contains one line that has the *Explosive* item.</span></span>

### <a name="release-order-set-3-in-one-load"></a><span data-ttu-id="b5828-235">通过一个装载发放订单集 3</span><span class="sxs-lookup"><span data-stu-id="b5828-235">Release order set 3 in one load</span></span>

<span data-ttu-id="b5828-236">应该已经创建了两个装运：</span><span class="sxs-lookup"><span data-stu-id="b5828-236">Two shipments should have been created:</span></span>

- <span data-ttu-id="b5828-237">第一个装运中包含其中的**客户申请**字段设置为 *1* 的销售订单中的订单行。</span><span class="sxs-lookup"><span data-stu-id="b5828-237">The first shipment contains order lines from the sales order where the **Customer requisition** field is set to *1*.</span></span>
- <span data-ttu-id="b5828-238">第二个装运中包含其中的**客户申请**字段设置为 *2* 的销售订单中的订单行。</span><span class="sxs-lookup"><span data-stu-id="b5828-238">The second shipment contains order lines from sales order where the **Customer requisition** field is set to *2*.</span></span>

### <a name="release-order-set-4-in-one-load"></a><span data-ttu-id="b5828-239">通过一个装载发放订单集 4</span><span class="sxs-lookup"><span data-stu-id="b5828-239">Release order set 4 in one load</span></span>

<span data-ttu-id="b5828-240">应该已经创建了四个装运：</span><span class="sxs-lookup"><span data-stu-id="b5828-240">Four shipments should have been created:</span></span>

- <span data-ttu-id="b5828-241">使用*订单池*装运合并策略将客户帐户 *US-003* 的两个订单的行合并到了一个装运中。</span><span class="sxs-lookup"><span data-stu-id="b5828-241">Lines from two orders for customer account *US-003* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="b5828-242">使用*订单池*装运合并策略将客户帐户 *US-004* 的两个订单的行合并到了一个装运中。</span><span class="sxs-lookup"><span data-stu-id="b5828-242">Lines from two orders for customer account *US-004* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="b5828-243">使用*订单池*装运合并策略将客户帐户 *US-007* 的销售订单 4-5 和 4-6 的行合并到了一个装运中。</span><span class="sxs-lookup"><span data-stu-id="b5828-243">Lines from sales orders 4-5 and 4-6 for customer account *US-007* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="b5828-244">使用*交叉订单*装运合并策略将客户帐户 *US-007* 的销售订单 4-7 和 4-8 的行合并到了一个装运中。</span><span class="sxs-lookup"><span data-stu-id="b5828-244">Lines from sales orders 4-7 and 4-8 for customer account *US-007* were grouped into one shipment by using the *CrossOrder* shipment consolidation policy.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b5828-245">其他资源</span><span class="sxs-lookup"><span data-stu-id="b5828-245">Additional resources</span></span>

- [<span data-ttu-id="b5828-246">装运合并政策</span><span class="sxs-lookup"><span data-stu-id="b5828-246">Shipment consolidation policies</span></span>](about-shipment-consolidation-policies.md)
- [<span data-ttu-id="b5828-247">配置装运合并策略</span><span class="sxs-lookup"><span data-stu-id="b5828-247">Configure shipment consolidation policies</span></span>](configure-shipment-consolidation-policies.md)
