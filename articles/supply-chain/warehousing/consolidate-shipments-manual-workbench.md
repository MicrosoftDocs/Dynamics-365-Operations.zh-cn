---
title: 使用装运合并工作台合并装运
description: 此主题提供以下方案：使用装运合并工作台将多个订单发放到仓库，以后再合并到装运中。
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
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 8320c8aab82a39a8a5565e6b3e805e1065c67453
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/10/2020
ms.locfileid: "3986807"
---
# <a name="consolidate-shipments-by-using-the-shipment-consolidation-workbench"></a><span data-ttu-id="52848-103">使用装运合并工作台合并装运</span><span class="sxs-lookup"><span data-stu-id="52848-103">Consolidate shipments by using the shipment consolidation workbench</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="52848-104">此主题提供以下方案：使用装运合并工作台将多个订单发放到仓库，以后再合并到装运中。</span><span class="sxs-lookup"><span data-stu-id="52848-104">This topic presents a scenario where multiple orders are released to the warehouse and then consolidated into shipments later by using the shipment consolidation workbench.</span></span>

## <a name="make-demo-data-available"></a><span data-ttu-id="52848-105">提供演示数据</span><span class="sxs-lookup"><span data-stu-id="52848-105">Make demo data available</span></span>

<span data-ttu-id="52848-106">此主题中的方案引用为 Microsoft Dynamics 365 Supply Chain Management 提供的标准演示数据中包含的值和记录。</span><span class="sxs-lookup"><span data-stu-id="52848-106">The scenario in this topic references values and records that are included in the standard demo data that is provided for Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="52848-107">如果要在进行此练习时使用此处提供的值，请务必在安装了演示数据的环境中操作，并且在开始前将法人设置为 **USMF**。</span><span class="sxs-lookup"><span data-stu-id="52848-107">If you want to use the values that are provided here as you do the exercises, be sure to work in an environment where the demo data is installed, and set the legal entity to **USMF** before you begin.</span></span>

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a><span data-ttu-id="52848-108">设置装运合并策略和产品筛选器</span><span class="sxs-lookup"><span data-stu-id="52848-108">Set up shipment consolidation policies and product filters</span></span>

<span data-ttu-id="52848-109">此处介绍的方案假设已经开启了此功能，完成了[配置装运合并策略](configure-shipment-consolidation-policies.md)中的练习，并创建了其中介绍的策略和其他记录。</span><span class="sxs-lookup"><span data-stu-id="52848-109">The scenario that is described here assumes that you've already turned on the feature, done the exercises in [Configure shipment consolidation policies](configure-shipment-consolidation-policies.md), and created the policies and other records that are described there.</span></span> <span data-ttu-id="52848-110">务必先完成这些练习，再继续完成此方案。</span><span class="sxs-lookup"><span data-stu-id="52848-110">Be sure to do those exercises before you continue with this scenario.</span></span>

## <a name="turn-on-the-manual-shipment-consolidation-feature"></a><span data-ttu-id="52848-111">开启手动合并装运功能</span><span class="sxs-lookup"><span data-stu-id="52848-111">Turn on the manual shipment consolidation feature</span></span>

<span data-ttu-id="52848-112">*手动合并装运*功能必须先在系统中开启，才能使用。</span><span class="sxs-lookup"><span data-stu-id="52848-112">Before you can use the *Manual shipment consolidation* feature, you must turn it on in your system.</span></span> <span data-ttu-id="52848-113">管理员可以使用[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)设置检查功能状态和开启功能。</span><span class="sxs-lookup"><span data-stu-id="52848-113">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="52848-114">在**功能管理**工作区中，此功能按照下面的方式列出：</span><span class="sxs-lookup"><span data-stu-id="52848-114">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="52848-115">**模块**：*仓库管理*</span><span class="sxs-lookup"><span data-stu-id="52848-115">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="52848-116">**功能名称**：*手动合并装运*</span><span class="sxs-lookup"><span data-stu-id="52848-116">**Feature name:** *Manual shipment consolidation*</span></span>

<span data-ttu-id="52848-117">[配置装运合并策略](configure-shipment-consolidation-policies.md)中已说明，还必须先开启*合并装运*功能，才能创建策略。</span><span class="sxs-lookup"><span data-stu-id="52848-117">As was mentioned in [Configure shipment consolidation policies](configure-shipment-consolidation-policies.md), you must also turn on the *Consolidate shipment* feature before you can create policies.</span></span> <span data-ttu-id="52848-118">但是，您应该已经完成了该步骤。</span><span class="sxs-lookup"><span data-stu-id="52848-118">However, you should already have completed that step.</span></span>

## <a name="create-the-sales-orders-for-this-scenario"></a><span data-ttu-id="52848-119">为此方案创建销售订单</span><span class="sxs-lookup"><span data-stu-id="52848-119">Create the sales orders for this scenario</span></span>

<span data-ttu-id="52848-120">首先创建可以使用的销售订单的集合。</span><span class="sxs-lookup"><span data-stu-id="52848-120">Start by creating a collection of sales orders that you can work with.</span></span> <span data-ttu-id="52848-121">必须使用为高级仓库 (WMS) 流程启用的仓库。</span><span class="sxs-lookup"><span data-stu-id="52848-121">You must work with a warehouse that is enabled for advanced warehouse (WMS) processes.</span></span> <span data-ttu-id="52848-122">除非明确提及其他仓库，否则必须为下面的每组订单使用同一个仓库。</span><span class="sxs-lookup"><span data-stu-id="52848-122">Unless a different warehouse is explicitly mentioned, that same warehouse must be used for each of the following sets of orders.</span></span>

<span data-ttu-id="52848-123">转到**应收帐款 \> 订单 \> 所有销售订单**，然后创建具有以下小节中介绍的设置的销售订单的集合。</span><span class="sxs-lookup"><span data-stu-id="52848-123">Go to **Accounts receivable \> Orders \> All sales orders**, and create a collection of sales orders that have the settings that are described in the following subsections.</span></span>

### <a name="create-order-set-1"></a><span data-ttu-id="52848-124">创建订单集 1</span><span class="sxs-lookup"><span data-stu-id="52848-124">Create order set 1</span></span>

#### <a name="sales-orders-1-1-and-1-2"></a><span data-ttu-id="52848-125">销售订单 1-1 和 1-2</span><span class="sxs-lookup"><span data-stu-id="52848-125">Sales orders 1-1 and 1-2</span></span>

1. <span data-ttu-id="52848-126">创建具有以下设置的两个相同销售订单：</span><span class="sxs-lookup"><span data-stu-id="52848-126">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="52848-127">**客户帐户**：*US-001*</span><span class="sxs-lookup"><span data-stu-id="52848-127">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="52848-128">**交货方式**：*航空公司-航运*</span><span class="sxs-lookup"><span data-stu-id="52848-128">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="52848-129">添加具有以下设置的订单行：</span><span class="sxs-lookup"><span data-stu-id="52848-129">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="52848-130">**物料编号**：*A0001*（未为其分配**代码 4** 筛选器的物料）</span><span class="sxs-lookup"><span data-stu-id="52848-130">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="52848-131">**数量：** *1.00*</span><span class="sxs-lookup"><span data-stu-id="52848-131">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="52848-132">选择**库存 \> 预留**，然后在操作窗格上选择**预留批次**预留订单行。</span><span class="sxs-lookup"><span data-stu-id="52848-132">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-order-1-3"></a><span data-ttu-id="52848-133">销售订单 1-3</span><span class="sxs-lookup"><span data-stu-id="52848-133">Sales order 1-3</span></span>

1. <span data-ttu-id="52848-134">创建具有以下设置的销售订单：</span><span class="sxs-lookup"><span data-stu-id="52848-134">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="52848-135">**客户帐户**：*US-001*</span><span class="sxs-lookup"><span data-stu-id="52848-135">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="52848-136">**交货方式**：*10*</span><span class="sxs-lookup"><span data-stu-id="52848-136">**Mode of delivery:** *10*</span></span>

1. <span data-ttu-id="52848-137">添加具有以下设置的订单行：</span><span class="sxs-lookup"><span data-stu-id="52848-137">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="52848-138">**物料编号**：*A0001*（未为其分配**代码 4** 筛选器的物料）</span><span class="sxs-lookup"><span data-stu-id="52848-138">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="52848-139">**数量：** *1.00*</span><span class="sxs-lookup"><span data-stu-id="52848-139">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="52848-140">选择**库存 \> 预留**，然后在操作窗格上选择**预留批次**预留订单行。</span><span class="sxs-lookup"><span data-stu-id="52848-140">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>
1. <span data-ttu-id="52848-141">添加第二个具有以下设置的订单行：</span><span class="sxs-lookup"><span data-stu-id="52848-141">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="52848-142">**物料编号**：*A0002*（未为其分配**代码 4** 筛选器的物料）</span><span class="sxs-lookup"><span data-stu-id="52848-142">**Item number:** *A0002* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="52848-143">**数量：** *1.00*</span><span class="sxs-lookup"><span data-stu-id="52848-143">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="52848-144">**交货方式**：*航空公司-航运*</span><span class="sxs-lookup"><span data-stu-id="52848-144">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="52848-145">选择**库存 \> 预留**，然后在操作窗格上选择**预留批次**预留第二个订单行。</span><span class="sxs-lookup"><span data-stu-id="52848-145">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the second order line.</span></span>

### <a name="create-order-set-2"></a><span data-ttu-id="52848-146">创建订单集 2</span><span class="sxs-lookup"><span data-stu-id="52848-146">Create order set 2</span></span>

#### <a name="sales-orders-2-1-and-2-2"></a><span data-ttu-id="52848-147">销售订单 2-1 和 2-2</span><span class="sxs-lookup"><span data-stu-id="52848-147">Sales orders 2-1 and 2-2</span></span>

1. <span data-ttu-id="52848-148">创建具有以下设置的两个相同销售订单：</span><span class="sxs-lookup"><span data-stu-id="52848-148">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="52848-149">**客户帐户**：*US-002*</span><span class="sxs-lookup"><span data-stu-id="52848-149">**Customer account:** *US-002*</span></span>
    - <span data-ttu-id="52848-150">**交货方式**：*航空公司-航运*</span><span class="sxs-lookup"><span data-stu-id="52848-150">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="52848-151">添加具有以下设置的订单行：</span><span class="sxs-lookup"><span data-stu-id="52848-151">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="52848-152">**物料编号**：*M9200*（其中的**代码 4** 筛选器设置为*易燃*的物料）</span><span class="sxs-lookup"><span data-stu-id="52848-152">**Item number:** *M9200* (an item where the **Code 4** filter is set to *Flammable*)</span></span>
    - <span data-ttu-id="52848-153">**数量：** *1.00*</span><span class="sxs-lookup"><span data-stu-id="52848-153">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="52848-154">选择**库存 \> 预留**，然后在操作窗格上选择**预留批次**预留订单行。</span><span class="sxs-lookup"><span data-stu-id="52848-154">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>
1. <span data-ttu-id="52848-155">添加第二个具有以下设置的订单行：</span><span class="sxs-lookup"><span data-stu-id="52848-155">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="52848-156">**物料编号**：*M9201*（其中的**代码 4** 筛选器设置为*易爆*的物料）</span><span class="sxs-lookup"><span data-stu-id="52848-156">**Item number:** *M9201* (an item where the **Code 4** filter is set to *Explosive*)</span></span>
    - <span data-ttu-id="52848-157">**数量：** *1.00*</span><span class="sxs-lookup"><span data-stu-id="52848-157">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="52848-158">**交货方式**：*航空公司-航运*</span><span class="sxs-lookup"><span data-stu-id="52848-158">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="52848-159">选择**库存 \> 预留**，然后在操作窗格上选择**预留批次**预留第二个订单行。</span><span class="sxs-lookup"><span data-stu-id="52848-159">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the second order line.</span></span>

### <a name="create-order-set-3"></a><span data-ttu-id="52848-160">创建订单集 3</span><span class="sxs-lookup"><span data-stu-id="52848-160">Create order set 3</span></span>

#### <a name="sales-orders-3-1-and-3-2"></a><span data-ttu-id="52848-161">销售订单 3-1 和 3-2</span><span class="sxs-lookup"><span data-stu-id="52848-161">Sales orders 3-1 and 3-2</span></span>

1. <span data-ttu-id="52848-162">创建具有以下设置的两个相同销售订单：</span><span class="sxs-lookup"><span data-stu-id="52848-162">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="52848-163">**客户帐户**：*US-001*</span><span class="sxs-lookup"><span data-stu-id="52848-163">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="52848-164">**客户申请**：*1*</span><span class="sxs-lookup"><span data-stu-id="52848-164">**Customer requisition:** *1*</span></span>

1. <span data-ttu-id="52848-165">添加具有以下设置的订单行：</span><span class="sxs-lookup"><span data-stu-id="52848-165">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="52848-166">**物料编号**：*A0001*（未为其分配**代码 4** 筛选器的物料）</span><span class="sxs-lookup"><span data-stu-id="52848-166">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="52848-167">**数量：** *1.00*</span><span class="sxs-lookup"><span data-stu-id="52848-167">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="52848-168">选择**库存 \> 预留**，然后在操作窗格上选择**预留批次**预留订单行。</span><span class="sxs-lookup"><span data-stu-id="52848-168">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-3-3-and-3-4"></a><span data-ttu-id="52848-169">销售订单 3-3 和 3-4</span><span class="sxs-lookup"><span data-stu-id="52848-169">Sales orders 3-3 and 3-4</span></span>

1. <span data-ttu-id="52848-170">创建具有以下设置的两个相同销售订单：</span><span class="sxs-lookup"><span data-stu-id="52848-170">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="52848-171">**客户帐户**：*US-001*</span><span class="sxs-lookup"><span data-stu-id="52848-171">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="52848-172">**客户申请**：*2*</span><span class="sxs-lookup"><span data-stu-id="52848-172">**Customer requisition:** *2*</span></span>

1. <span data-ttu-id="52848-173">添加具有以下设置的订单行：</span><span class="sxs-lookup"><span data-stu-id="52848-173">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="52848-174">**物料编号**：*A0001*（未为其分配**代码 4** 筛选器的物料）</span><span class="sxs-lookup"><span data-stu-id="52848-174">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="52848-175">**数量：** *1.00*</span><span class="sxs-lookup"><span data-stu-id="52848-175">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="52848-176">选择**库存 \> 预留**，然后在操作窗格上选择**预留批次**预留订单行。</span><span class="sxs-lookup"><span data-stu-id="52848-176">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

### <a name="create-order-set-4"></a><span data-ttu-id="52848-177">创建订单集 4</span><span class="sxs-lookup"><span data-stu-id="52848-177">Create order set 4</span></span>

#### <a name="sales-orders-4-1-and-4-2"></a><span data-ttu-id="52848-178">销售订单 4-1 和 4-2</span><span class="sxs-lookup"><span data-stu-id="52848-178">Sales orders 4-1 and 4-2</span></span>

1. <span data-ttu-id="52848-179">创建具有以下设置的两个相同销售订单：</span><span class="sxs-lookup"><span data-stu-id="52848-179">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="52848-180">**客户帐户**：*US-003*</span><span class="sxs-lookup"><span data-stu-id="52848-180">**Customer account:** *US-003*</span></span>

1. <span data-ttu-id="52848-181">添加具有以下设置的订单行：</span><span class="sxs-lookup"><span data-stu-id="52848-181">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="52848-182">**物料编号**：*A0001*（未为其分配**代码 4** 筛选器的物料）</span><span class="sxs-lookup"><span data-stu-id="52848-182">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="52848-183">**数量：** *1.00*</span><span class="sxs-lookup"><span data-stu-id="52848-183">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="52848-184">选择**库存 \> 预留**，然后在操作窗格上选择**预留批次**预留订单行。</span><span class="sxs-lookup"><span data-stu-id="52848-184">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-4-3-and-4-4"></a><span data-ttu-id="52848-185">销售订单 4-3 和 4-4</span><span class="sxs-lookup"><span data-stu-id="52848-185">Sales orders 4-3 and 4-4</span></span>

1. <span data-ttu-id="52848-186">创建具有以下设置的两个相同销售订单：</span><span class="sxs-lookup"><span data-stu-id="52848-186">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="52848-187">**客户帐户**：*US-004*</span><span class="sxs-lookup"><span data-stu-id="52848-187">**Customer account:** *US-004*</span></span>

1. <span data-ttu-id="52848-188">添加具有以下设置的订单行：</span><span class="sxs-lookup"><span data-stu-id="52848-188">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="52848-189">**物料编号**：*A0001*（未为其分配**代码 4** 筛选器的物料）</span><span class="sxs-lookup"><span data-stu-id="52848-189">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="52848-190">**数量：** *1.00*</span><span class="sxs-lookup"><span data-stu-id="52848-190">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="52848-191">选择**库存 \> 预留**，然后在操作窗格上选择**预留批次**预留订单行。</span><span class="sxs-lookup"><span data-stu-id="52848-191">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-4-5-and-4-6"></a><span data-ttu-id="52848-192">销售订单 4-5 和 4-6</span><span class="sxs-lookup"><span data-stu-id="52848-192">Sales orders 4-5 and 4-6</span></span>

1. <span data-ttu-id="52848-193">创建具有以下设置的两个相同销售订单：</span><span class="sxs-lookup"><span data-stu-id="52848-193">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="52848-194">**客户帐户**：*US-007*</span><span class="sxs-lookup"><span data-stu-id="52848-194">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="52848-195">**站点**：*6*</span><span class="sxs-lookup"><span data-stu-id="52848-195">**Site:** *6*</span></span>
    - <span data-ttu-id="52848-196">**仓库**：*61*</span><span class="sxs-lookup"><span data-stu-id="52848-196">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="52848-197">**池**：*ShipCons*</span><span class="sxs-lookup"><span data-stu-id="52848-197">**Pool:** *ShipCons*</span></span>

1. <span data-ttu-id="52848-198">添加具有以下设置的订单行：</span><span class="sxs-lookup"><span data-stu-id="52848-198">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="52848-199">**物料编号**：*A0001*（未为其分配**代码 4** 筛选器的物料）</span><span class="sxs-lookup"><span data-stu-id="52848-199">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="52848-200">**数量：** *1.00*</span><span class="sxs-lookup"><span data-stu-id="52848-200">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="52848-201">选择**库存 \> 预留**，然后在操作窗格上选择**预留批次**预留订单行。</span><span class="sxs-lookup"><span data-stu-id="52848-201">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-4-7-and-4-8"></a><span data-ttu-id="52848-202">销售订单 4-7 和 4-8</span><span class="sxs-lookup"><span data-stu-id="52848-202">Sales orders 4-7 and 4-8</span></span>

1. <span data-ttu-id="52848-203">创建具有以下设置的两个相同销售订单：</span><span class="sxs-lookup"><span data-stu-id="52848-203">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="52848-204">**客户帐户**：*US-007*</span><span class="sxs-lookup"><span data-stu-id="52848-204">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="52848-205">**站点**：*6*</span><span class="sxs-lookup"><span data-stu-id="52848-205">**Site:** *6*</span></span>
    - <span data-ttu-id="52848-206">**仓库**：*61*</span><span class="sxs-lookup"><span data-stu-id="52848-206">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="52848-207">**池**：保持此字段为空。</span><span class="sxs-lookup"><span data-stu-id="52848-207">**Pool:** Leave this field blank.</span></span>

1. <span data-ttu-id="52848-208">添加具有以下设置的订单行：</span><span class="sxs-lookup"><span data-stu-id="52848-208">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="52848-209">**物料编号**：*A0001*（未为其分配**代码 4** 筛选器的物料）</span><span class="sxs-lookup"><span data-stu-id="52848-209">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="52848-210">**数量：** *1.00*</span><span class="sxs-lookup"><span data-stu-id="52848-210">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="52848-211">选择**库存 \> 预留**，然后在操作窗格上选择**预留批次**预留订单行。</span><span class="sxs-lookup"><span data-stu-id="52848-211">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

## <a name="release-the-orders-to-the-warehouse"></a><span data-ttu-id="52848-212">将订单发放到仓库</span><span class="sxs-lookup"><span data-stu-id="52848-212">Release the orders to the warehouse</span></span>

<span data-ttu-id="52848-213">请按照以下步骤将您为此方案创建的每个销售订单发放到仓库。</span><span class="sxs-lookup"><span data-stu-id="52848-213">Follow these steps to release each sales order that you created for this scenario to the warehouse.</span></span>

1. <span data-ttu-id="52848-214">转到**应收帐款 \> 订单 \> 全部采购订单**。</span><span class="sxs-lookup"><span data-stu-id="52848-214">Go to **Accounts receivable \> Orders \> All sales orders**.</span></span>
1. <span data-ttu-id="52848-215">查找并选择要发放的销售订单。</span><span class="sxs-lookup"><span data-stu-id="52848-215">Find and select the sales order to release.</span></span>
1. <span data-ttu-id="52848-216">在“操作窗格”上的**仓库**选项卡上，选择**操作 \> 发放到仓库**发放所选销售订单。</span><span class="sxs-lookup"><span data-stu-id="52848-216">On the Action Pane, on the **Warehouse** tab, select **Actions \> Release to warehouse** to release the selected sales order.</span></span>
1. <span data-ttu-id="52848-217">对为此方案创建的其他每个销售订单集重复此过程。</span><span class="sxs-lookup"><span data-stu-id="52848-217">Repeat this procedure for every other sales order that you created for this scenario.</span></span>

## <a name="consolidate-the-shipments-by-using-the-shipment-consolidation-workbench"></a><span data-ttu-id="52848-218">使用装运合并工作台合并装运</span><span class="sxs-lookup"><span data-stu-id="52848-218">Consolidate the shipments by using the shipment consolidation workbench</span></span>

1. <span data-ttu-id="52848-219">转到**仓库管理 \> 发放到仓库 \> 装运合并工作台**。</span><span class="sxs-lookup"><span data-stu-id="52848-219">Go to **Warehouse management \> Release to warehouse \> Shipment consolidation workbench**.</span></span>
1. <span data-ttu-id="52848-220">在操作窗格上，选择**编辑查询**。</span><span class="sxs-lookup"><span data-stu-id="52848-220">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="52848-221">在查询编辑器对话框中**范围**选项卡上，选择**添加**向网格添加具有以下设置的行：</span><span class="sxs-lookup"><span data-stu-id="52848-221">In the query editor dialog box, on the **Range** tab, select **Add** to add a row that has the following settings to the grid:</span></span>

    - <span data-ttu-id="52848-222">**表**：*销售订单*</span><span class="sxs-lookup"><span data-stu-id="52848-222">**Table:** *Sales orders*</span></span>
    - <span data-ttu-id="52848-223">**字段**：*销售订单*</span><span class="sxs-lookup"><span data-stu-id="52848-223">**Field:** *Sales order*</span></span>
    - <span data-ttu-id="52848-224">**条件：** 输入为此方案创建的每个订单集以逗号分隔的销售订单编号列表。</span><span class="sxs-lookup"><span data-stu-id="52848-224">**Criteria:** Enter a comma-separated list of the sales order numbers for each order set that you created for this scenario.</span></span>

1. <span data-ttu-id="52848-225">选择**确定**保存查询并关闭对话框。</span><span class="sxs-lookup"><span data-stu-id="52848-225">Select **OK** to save your query and close the dialog box.</span></span>
1. <span data-ttu-id="52848-226">在操作窗格上选择**合并装运**。</span><span class="sxs-lookup"><span data-stu-id="52848-226">On the Action Pane, select **Consolidate shipments**.</span></span>
1. <span data-ttu-id="52848-227">选择所有装运，然后在操作窗格上选择**合并**。</span><span class="sxs-lookup"><span data-stu-id="52848-227">Select all the shipments, and then, on the Action Pane, select **Consolidate**.</span></span>

## <a name="verify-the-shipments"></a><span data-ttu-id="52848-228">验证装运</span><span class="sxs-lookup"><span data-stu-id="52848-228">Verify the shipments</span></span>

<span data-ttu-id="52848-229">以下过程用于验证装运合并导致已创建或更新的装运。</span><span class="sxs-lookup"><span data-stu-id="52848-229">The following procedure lets you verify the shipments that have been created or updated as a result of shipment consolidation.</span></span> <span data-ttu-id="52848-230">将其用于查看您为此方案创建的每个订单集，然后查看后面的小节以确保获取了预期结果。</span><span class="sxs-lookup"><span data-stu-id="52848-230">Use it to review each order set that you created for this scenario, and then review the subsections that follow to make sure that you've obtained the expected results.</span></span>

1. <span data-ttu-id="52848-231">转到**仓库管理 \> 装运 \> 所有装运**。</span><span class="sxs-lookup"><span data-stu-id="52848-231">Go to **Warehouse management \> Shipments \> All shipments**.</span></span>
1. <span data-ttu-id="52848-232">找到并选择所需装运。</span><span class="sxs-lookup"><span data-stu-id="52848-232">Find and select the required shipment.</span></span>
1. <span data-ttu-id="52848-233">如果创建或更新装运时使用了合并策略，应该可以在**装运合并策略**字段中看到此策略。</span><span class="sxs-lookup"><span data-stu-id="52848-233">If a consolidation policy was used when the shipment was created or updated, you should see it in the **Shipment consolidation policy** field.</span></span>

### <a name="related-shipments-for-order-set-1"></a><span data-ttu-id="52848-234">订单集 1 的相关装运</span><span class="sxs-lookup"><span data-stu-id="52848-234">Related shipments for order set 1</span></span>

<span data-ttu-id="52848-235">应该已经创建了两个装运：</span><span class="sxs-lookup"><span data-stu-id="52848-235">Two shipments should have been created:</span></span>

- <span data-ttu-id="52848-236">第一个装运中包含三行，该装运是使用 *CustomerMode* 装运合并策略创建的。</span><span class="sxs-lookup"><span data-stu-id="52848-236">The first shipment contains three lines and was created by using the *CustomerMode* shipment consolidation policy.</span></span>
- <span data-ttu-id="52848-237">第二个装运（该装运不使用*航空公司*交装运输方式）是使用 *CustomerOrderNo* 装运合并策略创建的。</span><span class="sxs-lookup"><span data-stu-id="52848-237">The second shipment, which doesn't use the *Airways* transportation mode of delivery, was created by using the *CustomerOrderNo* shipment consolidation policy.</span></span>

### <a name="related-shipments-for-order-set-2"></a><span data-ttu-id="52848-238">订单集 2 的相关装运</span><span class="sxs-lookup"><span data-stu-id="52848-238">Related shipments for order set 2</span></span>

<span data-ttu-id="52848-239">应该已经创建了三个装运：</span><span class="sxs-lookup"><span data-stu-id="52848-239">Three shipments should have been created:</span></span>

- <span data-ttu-id="52848-240">第一个装运中包含*易燃*物品。</span><span class="sxs-lookup"><span data-stu-id="52848-240">The first shipment contains *Flammable* items.</span></span>
- <span data-ttu-id="52848-241">其他两个装运每个包含一行，该行有*易爆*物品。</span><span class="sxs-lookup"><span data-stu-id="52848-241">Each of the other two shipments contains one line that has the *Explosive* item.</span></span>

### <a name="related-shipments-for-order-set-3"></a><span data-ttu-id="52848-242">订单集 3 的相关装运</span><span class="sxs-lookup"><span data-stu-id="52848-242">Related shipments for order set 3</span></span>

<span data-ttu-id="52848-243">应该已经创建了两个装运：</span><span class="sxs-lookup"><span data-stu-id="52848-243">Two shipments should have been created:</span></span>

- <span data-ttu-id="52848-244">第一个装运中包含其中的**客户申请**字段设置为 *1* 的销售订单中的订单行。</span><span class="sxs-lookup"><span data-stu-id="52848-244">The first shipment contains order lines from the sales order where the **Customer requisition** field is set to *1*.</span></span>
- <span data-ttu-id="52848-245">第二个装运中包含其中的**客户申请**字段设置为 *2* 的销售订单中的订单行。</span><span class="sxs-lookup"><span data-stu-id="52848-245">The second shipment contains order lines from sales order where the **Customer requisition** field is set to *2*.</span></span>

### <a name="related-shipments-for-order-set-4"></a><span data-ttu-id="52848-246">订单集 4 的相关装运</span><span class="sxs-lookup"><span data-stu-id="52848-246">Related shipments for order set 4</span></span>

<span data-ttu-id="52848-247">应该已经创建了四个装运：</span><span class="sxs-lookup"><span data-stu-id="52848-247">Four shipments should have been created:</span></span>

- <span data-ttu-id="52848-248">使用*订单池*装运合并策略将客户 *US-003* 的两个订单的行合并到了一个装运中。</span><span class="sxs-lookup"><span data-stu-id="52848-248">Lines from two orders for customer *US-003* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="52848-249">使用*订单池*装运合并策略将客户 *US-004* 的两个订单的行合并到了一个装运中。</span><span class="sxs-lookup"><span data-stu-id="52848-249">Lines from two orders for customer *US-004* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="52848-250">使用*订单池*装运合并策略将客户 *US-007* 的销售订单 4-5 和 4-6 的行合并到了一个装运中。</span><span class="sxs-lookup"><span data-stu-id="52848-250">Lines from sales orders 4-5 and 4-6 for customer *US-007* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="52848-251">使用*交叉订单*装运合并策略将客户 *US-007* 的销售订单 4-7 和 4-8 的行合并到了一个装运中。</span><span class="sxs-lookup"><span data-stu-id="52848-251">Lines from sales orders 4-7 and 4-8 for customer *US-007* were grouped into one shipment by using the *CrossOrder* shipment consolidation policy.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="52848-252">其他资源</span><span class="sxs-lookup"><span data-stu-id="52848-252">Additional resources</span></span>

- [<span data-ttu-id="52848-253">装运合并政策</span><span class="sxs-lookup"><span data-stu-id="52848-253">Shipment consolidation policies</span></span>](about-shipment-consolidation-policies.md)
- [<span data-ttu-id="52848-254">配置装运合并策略</span><span class="sxs-lookup"><span data-stu-id="52848-254">Configure shipment consolidation policies</span></span>](configure-shipment-consolidation-policies.md)
