---
title: 使用自动发放销售订单发放到仓库时使用合并
description: 此主题提供以下方案：在同一个自动化发放到仓库定期过程中将多个订单发放到仓库。
author: GarmMSFT
manager: tfehr
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench, WHSFilterGroupTable, WHSShipmentConsolidation, WHSFilterGenerallyAvail
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: ac3ab25dc1355ee15e1209950ff0f3b3933b7095
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4423341"
---
# <a name="consolidate-shipments-when-they-are-released-to-the-warehouse-by-using-automatic-release-of-sales-orders"></a><span data-ttu-id="79dc1-103">使用自动发放销售订单发放到仓库时使用合并</span><span class="sxs-lookup"><span data-stu-id="79dc1-103">Consolidate shipments when they are released to the warehouse by using Automatic release of sales orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="79dc1-104">此主题提供以下方案：在同一个自动化发放到仓库定期过程中将多个订单发放到仓库。</span><span class="sxs-lookup"><span data-stu-id="79dc1-104">This topic presents a scenario where multiple orders are released to the warehouse in the same automated release-to-warehouse periodic procedure.</span></span> <span data-ttu-id="79dc1-105">将根据定义为装运合并策略的规则将订单自动合并到装运中。</span><span class="sxs-lookup"><span data-stu-id="79dc1-105">The orders will automatically be consolidated into shipments, based on rules that are defined as shipment consolidation policies.</span></span>

<span data-ttu-id="79dc1-106">在此方案中，将创建多组订单并将每组发放到仓库。</span><span class="sxs-lookup"><span data-stu-id="79dc1-106">During the scenario, you will create sets of sales orders and release each set to the warehouse.</span></span> <span data-ttu-id="79dc1-107">然后根据配置的策略查看装运合并期间创建或更新的装运。</span><span class="sxs-lookup"><span data-stu-id="79dc1-107">You will then review the shipments that are created or updated during shipment consolidation, based on the configured policies.</span></span>

## <a name="make-demo-data-available"></a><span data-ttu-id="79dc1-108">提供演示数据</span><span class="sxs-lookup"><span data-stu-id="79dc1-108">Make demo data available</span></span>

<span data-ttu-id="79dc1-109">此主题中的方案引用为 Microsoft Dynamics 365 Supply Chain Management 提供的标准演示数据中包含的值和记录。</span><span class="sxs-lookup"><span data-stu-id="79dc1-109">The scenario in this topic references values and records that are included in the standard demo data that is provided for Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="79dc1-110">如果要在进行此练习时使用此处提供的值，请务必在安装了演示数据的环境中操作，并且在开始前将法人设置为 **USMF**。</span><span class="sxs-lookup"><span data-stu-id="79dc1-110">If you want to use the values that are provided here as you do the exercises, be sure to work in an environment where the demo data is installed, and set the legal entity to **USMF** before you begin.</span></span>

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a><span data-ttu-id="79dc1-111">设置装运合并策略和产品筛选器</span><span class="sxs-lookup"><span data-stu-id="79dc1-111">Set up shipment consolidation policies and product filters</span></span>

<span data-ttu-id="79dc1-112">此处介绍的方案假设已经开启了此功能，完成了[配置装运合并策略](configure-shipment-consolidation-policies.md)中的练习，并创建了其中介绍的策略和其他记录。</span><span class="sxs-lookup"><span data-stu-id="79dc1-112">The scenario that is described here assumes that you've already turned on the feature, done the exercises in [Configure shipment consolidation policies](configure-shipment-consolidation-policies.md), and created the policies and other records that are described there.</span></span> <span data-ttu-id="79dc1-113">务必先完成这些练习，再继续完成此方案。</span><span class="sxs-lookup"><span data-stu-id="79dc1-113">Be sure to do those exercises before you continue with this scenario.</span></span>

## <a name="create-the-sales-orders-for-this-scenario"></a><span data-ttu-id="79dc1-114">为此方案创建销售订单</span><span class="sxs-lookup"><span data-stu-id="79dc1-114">Create the sales orders for this scenario</span></span>

<span data-ttu-id="79dc1-115">首先创建可以使用的销售订单的集合。</span><span class="sxs-lookup"><span data-stu-id="79dc1-115">Start by creating a collection of sales orders that you can work with.</span></span> <span data-ttu-id="79dc1-116">必须使用为高级仓库 (WMS) 流程启用的仓库。</span><span class="sxs-lookup"><span data-stu-id="79dc1-116">You must work with a warehouse that is enabled for advanced warehouse (WMS) processes.</span></span> <span data-ttu-id="79dc1-117">除非明确提及其他仓库，否则必须为下面的每组订单使用同一个仓库。</span><span class="sxs-lookup"><span data-stu-id="79dc1-117">Unless a different warehouse is explicitly mentioned, that same warehouse must be used for each of the following sets of orders.</span></span>

<span data-ttu-id="79dc1-118">转到 **应收帐款 \> 订单 \> 所有销售订单**，然后创建具有以下小节中介绍的设置的销售订单的集合。</span><span class="sxs-lookup"><span data-stu-id="79dc1-118">Go to **Accounts receivable \> Orders \> All sales orders**, and create a collection of sales orders that have the settings that are described in the following subsections.</span></span>

### <a name="create-order-set-1"></a><span data-ttu-id="79dc1-119">创建订单集 1</span><span class="sxs-lookup"><span data-stu-id="79dc1-119">Create order set 1</span></span>

#### <a name="sales-order-1-1"></a><span data-ttu-id="79dc1-120">销售订单 1-1</span><span class="sxs-lookup"><span data-stu-id="79dc1-120">Sales order 1-1</span></span>

1. <span data-ttu-id="79dc1-121">创建具有以下设置的销售订单：</span><span class="sxs-lookup"><span data-stu-id="79dc1-121">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="79dc1-122">**客户帐户**：*US-001*</span><span class="sxs-lookup"><span data-stu-id="79dc1-122">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="79dc1-123">**交货方式**：*航空公司-航运*</span><span class="sxs-lookup"><span data-stu-id="79dc1-123">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="79dc1-124">添加具有以下设置的订单行：</span><span class="sxs-lookup"><span data-stu-id="79dc1-124">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="79dc1-125">**物料编号**：*A0001*（未为其分配 **代码 4** 筛选器的物料）</span><span class="sxs-lookup"><span data-stu-id="79dc1-125">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="79dc1-126">**数量：** *1.00*</span><span class="sxs-lookup"><span data-stu-id="79dc1-126">**Quantity:** *1.00*</span></span>

#### <a name="sales-order-1-2"></a><span data-ttu-id="79dc1-127">销售订单 1-2</span><span class="sxs-lookup"><span data-stu-id="79dc1-127">Sales order 1-2</span></span>

1. <span data-ttu-id="79dc1-128">创建具有以下设置的销售订单：</span><span class="sxs-lookup"><span data-stu-id="79dc1-128">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="79dc1-129">**客户帐户**：*US-001*</span><span class="sxs-lookup"><span data-stu-id="79dc1-129">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="79dc1-130">**交货方式**：*航空公司-航运*</span><span class="sxs-lookup"><span data-stu-id="79dc1-130">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="79dc1-131">添加具有以下设置的订单行：</span><span class="sxs-lookup"><span data-stu-id="79dc1-131">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="79dc1-132">**物料编号**：*A0001*（未为其分配 **代码 4** 筛选器的物料）</span><span class="sxs-lookup"><span data-stu-id="79dc1-132">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="79dc1-133">**数量：** *1.00*</span><span class="sxs-lookup"><span data-stu-id="79dc1-133">**Quantity:** *1.00*</span></span>

#### <a name="sales-order-1-3"></a><span data-ttu-id="79dc1-134">销售订单 1-3</span><span class="sxs-lookup"><span data-stu-id="79dc1-134">Sales order 1-3</span></span>

1. <span data-ttu-id="79dc1-135">创建具有以下设置的销售订单：</span><span class="sxs-lookup"><span data-stu-id="79dc1-135">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="79dc1-136">**客户帐户**：*US-001*</span><span class="sxs-lookup"><span data-stu-id="79dc1-136">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="79dc1-137">**交货方式**：*10*</span><span class="sxs-lookup"><span data-stu-id="79dc1-137">**Mode of delivery:** *10*</span></span>

1. <span data-ttu-id="79dc1-138">添加具有以下设置的订单行：</span><span class="sxs-lookup"><span data-stu-id="79dc1-138">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="79dc1-139">**物料编号**：*A0001*（未为其分配 **代码 4** 筛选器的物料）</span><span class="sxs-lookup"><span data-stu-id="79dc1-139">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="79dc1-140">**数量：** *1.00*</span><span class="sxs-lookup"><span data-stu-id="79dc1-140">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="79dc1-141">添加第二个具有以下设置的订单行：</span><span class="sxs-lookup"><span data-stu-id="79dc1-141">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="79dc1-142">**物料编号**：*A0002*（未为其分配 **代码 4** 筛选器的物料）</span><span class="sxs-lookup"><span data-stu-id="79dc1-142">**Item number:** *A0002* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="79dc1-143">**数量：** *1.00*</span><span class="sxs-lookup"><span data-stu-id="79dc1-143">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="79dc1-144">**交货方式**：*航空公司-航运*</span><span class="sxs-lookup"><span data-stu-id="79dc1-144">**Mode of delivery:** *Airwa-Air*</span></span>

### <a name="create-order-set-2"></a><span data-ttu-id="79dc1-145">创建订单集 2</span><span class="sxs-lookup"><span data-stu-id="79dc1-145">Create order set 2</span></span>

#### <a name="sales-orders-2-1-and-2-2"></a><span data-ttu-id="79dc1-146">销售订单 2-1 和 2-2</span><span class="sxs-lookup"><span data-stu-id="79dc1-146">Sales orders 2-1 and 2-2</span></span>

1. <span data-ttu-id="79dc1-147">创建具有以下设置的两个相同销售订单：</span><span class="sxs-lookup"><span data-stu-id="79dc1-147">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="79dc1-148">**客户帐户**：*US-002*</span><span class="sxs-lookup"><span data-stu-id="79dc1-148">**Customer account:** *US-002*</span></span>

1. <span data-ttu-id="79dc1-149">添加具有以下设置的订单行：</span><span class="sxs-lookup"><span data-stu-id="79dc1-149">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="79dc1-150">**物料编号**：*M9200*（其中的 **代码 4** 筛选器设置为 *易燃* 的物料）</span><span class="sxs-lookup"><span data-stu-id="79dc1-150">**Item number:** *M9200* (an item where the **Code 4** filter is set to *Flammable*)</span></span>
    - <span data-ttu-id="79dc1-151">**数量：** *1.00*</span><span class="sxs-lookup"><span data-stu-id="79dc1-151">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="79dc1-152">添加第二个具有以下设置的订单行：</span><span class="sxs-lookup"><span data-stu-id="79dc1-152">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="79dc1-153">**物料编号**：*M9201*（其中的 **代码 4** 筛选器设置为 *易爆* 的物料）</span><span class="sxs-lookup"><span data-stu-id="79dc1-153">**Item number:** *M9201* (an item where the **Code 4** filter is set to *Explosive*)</span></span>
    - <span data-ttu-id="79dc1-154">**数量：** *1.00*</span><span class="sxs-lookup"><span data-stu-id="79dc1-154">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="79dc1-155">**交货方式**：*航空公司-航运*</span><span class="sxs-lookup"><span data-stu-id="79dc1-155">**Mode of delivery:** *Airwa-Air*</span></span>

### <a name="create-order-set-3"></a><span data-ttu-id="79dc1-156">创建订单集 3</span><span class="sxs-lookup"><span data-stu-id="79dc1-156">Create order set 3</span></span>

#### <a name="sales-order-3-1"></a><span data-ttu-id="79dc1-157">销售订单 3-1</span><span class="sxs-lookup"><span data-stu-id="79dc1-157">Sales order 3-1</span></span>

1. <span data-ttu-id="79dc1-158">创建具有以下设置的销售订单：</span><span class="sxs-lookup"><span data-stu-id="79dc1-158">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="79dc1-159">**客户帐户**：*US-002*</span><span class="sxs-lookup"><span data-stu-id="79dc1-159">**Customer account:** *US-002*</span></span>

1. <span data-ttu-id="79dc1-160">添加具有以下设置的订单行：</span><span class="sxs-lookup"><span data-stu-id="79dc1-160">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="79dc1-161">**物料编号**：*M9200*（其中的 **代码 4** 筛选器设置为 *易燃* 的物料）</span><span class="sxs-lookup"><span data-stu-id="79dc1-161">**Item number:** *M9200* (an item where the **Code 4** filter is set to *Flammable*)</span></span>
    - <span data-ttu-id="79dc1-162">**数量：** *1.00*</span><span class="sxs-lookup"><span data-stu-id="79dc1-162">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="79dc1-163">添加第二个具有以下设置的订单行：</span><span class="sxs-lookup"><span data-stu-id="79dc1-163">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="79dc1-164">**物料编号**：*M9201*（其中的 **代码 4** 筛选器设置为 *易爆* 的物料）</span><span class="sxs-lookup"><span data-stu-id="79dc1-164">**Item number:** *M9201* (an item where the **Code 4** filter is set to *Explosive*)</span></span>
    - <span data-ttu-id="79dc1-165">**数量：** *1.00*</span><span class="sxs-lookup"><span data-stu-id="79dc1-165">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="79dc1-166">**交货方式**：*航空公司-航运*</span><span class="sxs-lookup"><span data-stu-id="79dc1-166">**Mode of delivery:** *Airwa-Air*</span></span>

> [!NOTE]
> <span data-ttu-id="79dc1-167">此订单与为订单集 2 创建的两个订单相同。</span><span class="sxs-lookup"><span data-stu-id="79dc1-167">This order is identical to the two orders that you created for order set 2.</span></span> <span data-ttu-id="79dc1-168">但是，其作为自己的订单集列出，因为后面将在此方案中单独发放。</span><span class="sxs-lookup"><span data-stu-id="79dc1-168">However, it's listed as its own order set because you will release it separately later in this scenario.</span></span>

### <a name="create-order-set-4"></a><span data-ttu-id="79dc1-169">创建订单集 4</span><span class="sxs-lookup"><span data-stu-id="79dc1-169">Create order set 4</span></span>

#### <a name="sales-order-4-1"></a><span data-ttu-id="79dc1-170">销售订单 4-1</span><span class="sxs-lookup"><span data-stu-id="79dc1-170">Sales order 4-1</span></span>

1. <span data-ttu-id="79dc1-171">创建具有以下设置的销售订单：</span><span class="sxs-lookup"><span data-stu-id="79dc1-171">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="79dc1-172">**客户帐户**：*US-001*</span><span class="sxs-lookup"><span data-stu-id="79dc1-172">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="79dc1-173">**客户申请**：*1*</span><span class="sxs-lookup"><span data-stu-id="79dc1-173">**Customer requisition:** *1*</span></span>

1. <span data-ttu-id="79dc1-174">添加具有以下设置的订单行：</span><span class="sxs-lookup"><span data-stu-id="79dc1-174">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="79dc1-175">**物料编号**：*A0001*（未为其分配 **代码 4** 筛选器的物料）</span><span class="sxs-lookup"><span data-stu-id="79dc1-175">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="79dc1-176">**数量：** *1.00*</span><span class="sxs-lookup"><span data-stu-id="79dc1-176">**Quantity:** *1.00*</span></span>

### <a name="create-order-set-5"></a><span data-ttu-id="79dc1-177">创建订单集 5</span><span class="sxs-lookup"><span data-stu-id="79dc1-177">Create order set 5</span></span>

#### <a name="sales-orders-5-1-and-5-2"></a><span data-ttu-id="79dc1-178">销售订单 5-1 和 5-2</span><span class="sxs-lookup"><span data-stu-id="79dc1-178">Sales orders 5-1 and 5-2</span></span>

1. <span data-ttu-id="79dc1-179">创建具有以下设置的两个相同销售订单：</span><span class="sxs-lookup"><span data-stu-id="79dc1-179">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="79dc1-180">**客户帐户**：*US-001*</span><span class="sxs-lookup"><span data-stu-id="79dc1-180">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="79dc1-181">**客户申请**：*2*</span><span class="sxs-lookup"><span data-stu-id="79dc1-181">**Customer requisition:** *2*</span></span>

1. <span data-ttu-id="79dc1-182">添加具有以下设置的订单行：</span><span class="sxs-lookup"><span data-stu-id="79dc1-182">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="79dc1-183">**物料编号**：*A0001*（未为其分配 **代码 4** 筛选器的物料）</span><span class="sxs-lookup"><span data-stu-id="79dc1-183">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="79dc1-184">**数量：** *1.00*</span><span class="sxs-lookup"><span data-stu-id="79dc1-184">**Quantity:** *1.00*</span></span>

#### <a name="sales-order-5-3"></a><span data-ttu-id="79dc1-185">销售订单 5-3</span><span class="sxs-lookup"><span data-stu-id="79dc1-185">Sales order 5-3</span></span>

1. <span data-ttu-id="79dc1-186">创建具有以下设置的销售订单：</span><span class="sxs-lookup"><span data-stu-id="79dc1-186">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="79dc1-187">**客户帐户**：*US-001*</span><span class="sxs-lookup"><span data-stu-id="79dc1-187">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="79dc1-188">**客户申请**：*1*</span><span class="sxs-lookup"><span data-stu-id="79dc1-188">**Customer requisition:** *1*</span></span>

1. <span data-ttu-id="79dc1-189">添加具有以下设置的订单行：</span><span class="sxs-lookup"><span data-stu-id="79dc1-189">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="79dc1-190">**物料编号**：*A0001*（未为其分配 **代码 4** 筛选器的物料）</span><span class="sxs-lookup"><span data-stu-id="79dc1-190">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="79dc1-191">**数量：** *1.00*</span><span class="sxs-lookup"><span data-stu-id="79dc1-191">**Quantity:** *1.00*</span></span>

### <a name="create-order-set-6"></a><span data-ttu-id="79dc1-192">创建订单集 6</span><span class="sxs-lookup"><span data-stu-id="79dc1-192">Create order set 6</span></span>

#### <a name="sales-orders-6-1-and-6-2"></a><span data-ttu-id="79dc1-193">销售订单 6-1 和 6-2</span><span class="sxs-lookup"><span data-stu-id="79dc1-193">Sales orders 6-1 and 6-2</span></span>

1. <span data-ttu-id="79dc1-194">创建具有以下设置的两个相同销售订单：</span><span class="sxs-lookup"><span data-stu-id="79dc1-194">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="79dc1-195">**客户帐户**：*US-003*</span><span class="sxs-lookup"><span data-stu-id="79dc1-195">**Customer account:** *US-003*</span></span>
    - <span data-ttu-id="79dc1-196">**客户申请**：*2*</span><span class="sxs-lookup"><span data-stu-id="79dc1-196">**Customer requisition:** *2*</span></span>

1. <span data-ttu-id="79dc1-197">添加具有以下设置的订单行：</span><span class="sxs-lookup"><span data-stu-id="79dc1-197">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="79dc1-198">**物料编号**：*A0001*（未为其分配 **代码 4** 筛选器的物料）</span><span class="sxs-lookup"><span data-stu-id="79dc1-198">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="79dc1-199">**数量：** *1.00*</span><span class="sxs-lookup"><span data-stu-id="79dc1-199">**Quantity:** *1.00*</span></span>

#### <a name="sales-orders-6-3-and-6-4"></a><span data-ttu-id="79dc1-200">销售订单 6-3 和 6-4</span><span class="sxs-lookup"><span data-stu-id="79dc1-200">Sales orders 6-3 and 6-4</span></span>

1. <span data-ttu-id="79dc1-201">创建具有以下设置的两个相同销售订单：</span><span class="sxs-lookup"><span data-stu-id="79dc1-201">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="79dc1-202">**客户帐户**：*US-004*</span><span class="sxs-lookup"><span data-stu-id="79dc1-202">**Customer account:** *US-004*</span></span>
    - <span data-ttu-id="79dc1-203">**客户申请**：*1*</span><span class="sxs-lookup"><span data-stu-id="79dc1-203">**Customer requisition:** *1*</span></span>

1. <span data-ttu-id="79dc1-204">添加具有以下设置的订单行：</span><span class="sxs-lookup"><span data-stu-id="79dc1-204">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="79dc1-205">**物料编号**：*A0001*（未为其分配 **代码 4** 筛选器的物料）</span><span class="sxs-lookup"><span data-stu-id="79dc1-205">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="79dc1-206">**数量：** *1.00*</span><span class="sxs-lookup"><span data-stu-id="79dc1-206">**Quantity:** *1.00*</span></span>

#### <a name="sales-orders-6-5-and-6-6"></a><span data-ttu-id="79dc1-207">销售订单 6-5 和 6-6</span><span class="sxs-lookup"><span data-stu-id="79dc1-207">Sales orders 6-5 and 6-6</span></span>

1. <span data-ttu-id="79dc1-208">创建具有以下设置的两个相同销售订单：</span><span class="sxs-lookup"><span data-stu-id="79dc1-208">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="79dc1-209">**客户帐户**：*US-007*</span><span class="sxs-lookup"><span data-stu-id="79dc1-209">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="79dc1-210">**站点**：*6*</span><span class="sxs-lookup"><span data-stu-id="79dc1-210">**Site:** *6*</span></span>
    - <span data-ttu-id="79dc1-211">**仓库**：*61*</span><span class="sxs-lookup"><span data-stu-id="79dc1-211">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="79dc1-212">**池**：*ShipCons*</span><span class="sxs-lookup"><span data-stu-id="79dc1-212">**Pool:** *ShipCons*</span></span>

1. <span data-ttu-id="79dc1-213">添加具有以下设置的订单行：</span><span class="sxs-lookup"><span data-stu-id="79dc1-213">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="79dc1-214">**物料编号**：*A0001*（未为其分配 **代码 4** 筛选器的物料）</span><span class="sxs-lookup"><span data-stu-id="79dc1-214">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="79dc1-215">**数量：** *1.00*</span><span class="sxs-lookup"><span data-stu-id="79dc1-215">**Quantity:** *1.00*</span></span>

#### <a name="sales-orders-6-7-and-6-8"></a><span data-ttu-id="79dc1-216">销售订单 6-7 和 6-8</span><span class="sxs-lookup"><span data-stu-id="79dc1-216">Sales orders 6-7 and 6-8</span></span>

1. <span data-ttu-id="79dc1-217">创建具有以下设置的两个相同销售订单：</span><span class="sxs-lookup"><span data-stu-id="79dc1-217">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="79dc1-218">**客户帐户**：*US-007*</span><span class="sxs-lookup"><span data-stu-id="79dc1-218">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="79dc1-219">**站点**：*6*</span><span class="sxs-lookup"><span data-stu-id="79dc1-219">**Site:** *6*</span></span>
    - <span data-ttu-id="79dc1-220">**仓库**：*61*</span><span class="sxs-lookup"><span data-stu-id="79dc1-220">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="79dc1-221">**池**：保持此字段为空。</span><span class="sxs-lookup"><span data-stu-id="79dc1-221">**Pool:** Leave this field blank.</span></span>

1. <span data-ttu-id="79dc1-222">添加具有以下设置的订单行：</span><span class="sxs-lookup"><span data-stu-id="79dc1-222">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="79dc1-223">**物料编号**：*A0001*（未为其分配 **代码 4** 筛选器的物料）</span><span class="sxs-lookup"><span data-stu-id="79dc1-223">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="79dc1-224">**数量：** *1.00*</span><span class="sxs-lookup"><span data-stu-id="79dc1-224">**Quantity:** *1.00*</span></span>

## <a name="automatic-release-of-sales-orders-to-the-warehouse"></a><span data-ttu-id="79dc1-225">将销售订单自动发放到仓库</span><span class="sxs-lookup"><span data-stu-id="79dc1-225">Automatic release of sales orders to the warehouse</span></span>

<span data-ttu-id="79dc1-226">将为之前创建的每组销售订单完成自动发放到仓库过程。</span><span class="sxs-lookup"><span data-stu-id="79dc1-226">For each set of sales orders that you created earlier, you will complete a procedure for automatic release to the warehouse.</span></span> <span data-ttu-id="79dc1-227">在每个示例中，将完成此处提供的[发放到仓库基本过程](#release-procedure)。</span><span class="sxs-lookup"><span data-stu-id="79dc1-227">In each case, you will work through the [basic release-to-warehouse procedure](#release-procedure) that is provided here.</span></span>

### <a name="basic-release-to-warehouse-procedure"></a><a name="release-procedure"></a><span data-ttu-id="79dc1-228">发放到仓库基本过程</span><span class="sxs-lookup"><span data-stu-id="79dc1-228">Basic release-to-warehouse procedure</span></span>

<span data-ttu-id="79dc1-229">为之前创建的每组销售订单完成以下小节中概述的三个过程。</span><span class="sxs-lookup"><span data-stu-id="79dc1-229">For each set of sales orders that you created earlier, you will complete the three procedures that are outlined in the following subsections.</span></span>

#### <a name="update-the-wave-template-that-will-be-used-during-release"></a><span data-ttu-id="79dc1-230">更新发放期间将使用的波次模板</span><span class="sxs-lookup"><span data-stu-id="79dc1-230">Update the wave template that will be used during release</span></span>

1. <span data-ttu-id="79dc1-231">转到 **仓库管理 \> 设置 \> 波次 \> 波次模板**。</span><span class="sxs-lookup"><span data-stu-id="79dc1-231">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="79dc1-232">将 **波次模板类型** 字段设置为 *装运*。</span><span class="sxs-lookup"><span data-stu-id="79dc1-232">Set the **Wave template type** field to *Shipping*.</span></span>
1. <span data-ttu-id="79dc1-233">找到并选择与为此方案创建的订单集中所用仓库关联的波次模板。</span><span class="sxs-lookup"><span data-stu-id="79dc1-233">Find and select the wave template that is associated with the warehouse that you used in the order sets that you created for this scenario.</span></span> <span data-ttu-id="79dc1-234">例如，如果使用了仓库 *24*，请选择 **24 装运默认值** 波次模板。</span><span class="sxs-lookup"><span data-stu-id="79dc1-234">For example, if you used warehouse *24*, select the **24 Shipping Default** wave template.</span></span> <span data-ttu-id="79dc1-235">如果使用了仓库 *61*，请选择 **61 装运** 波次模板。</span><span class="sxs-lookup"><span data-stu-id="79dc1-235">If you used warehouse *61*, select the **61 Shipping** wave template.</span></span>
1. <span data-ttu-id="79dc1-236">在操作窗格上，选择 **编辑**。</span><span class="sxs-lookup"><span data-stu-id="79dc1-236">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="79dc1-237">设置 **在发放到仓库时处理波次** 选项为 *否*。</span><span class="sxs-lookup"><span data-stu-id="79dc1-237">Set the **Process wave at release to warehouse** option to *No*.</span></span>

#### <a name="release-to-the-warehouse"></a><span data-ttu-id="79dc1-238">发放到仓库</span><span class="sxs-lookup"><span data-stu-id="79dc1-238">Release to the warehouse</span></span>

1. <span data-ttu-id="79dc1-239">转到 **仓库管理 \> 发放到仓库 \> 自动发放销售订单**。</span><span class="sxs-lookup"><span data-stu-id="79dc1-239">Go to **Warehouse management \> Release to warehouse \> Automatic release of sales orders**.</span></span>
1. <span data-ttu-id="79dc1-240">将 **要发放的数量** 字段设置为 *全部*。</span><span class="sxs-lookup"><span data-stu-id="79dc1-240">Set the **Quantity to release** field to *All*.</span></span>
1. <span data-ttu-id="79dc1-241">在 **要包括的记录** 快速选项卡上，选择 **筛选器** 打开查询对话框。</span><span class="sxs-lookup"><span data-stu-id="79dc1-241">On the **Records to include** FastTab, select **Filter** to open the query dialog box.</span></span>
1. <span data-ttu-id="79dc1-242">在 **范围** 选项卡上，选择 **添加** 向网格添加具有以下设置的行：</span><span class="sxs-lookup"><span data-stu-id="79dc1-242">On the **Range** tab, select **Add** to add a row that has the following settings to the grid:</span></span>

    - <span data-ttu-id="79dc1-243">**表**：*销售订单*</span><span class="sxs-lookup"><span data-stu-id="79dc1-243">**Table:** *Sales order*</span></span>
    - <span data-ttu-id="79dc1-244">**派生表**：*销售订单*</span><span class="sxs-lookup"><span data-stu-id="79dc1-244">**Derived table:** *Sales order*</span></span>
    - <span data-ttu-id="79dc1-245">**字段**：*销售订单*</span><span class="sxs-lookup"><span data-stu-id="79dc1-245">**Field:** *Sales order*</span></span>
    - <span data-ttu-id="79dc1-246">**条件：** 输入所需订单集中的销售订单编号以逗号分隔的列表。</span><span class="sxs-lookup"><span data-stu-id="79dc1-246">**Criteria:** Enter a comma-separated list of the sales order numbers from the desired order set.</span></span>

1. <span data-ttu-id="79dc1-247">选择 **确定** 保存您的查询。</span><span class="sxs-lookup"><span data-stu-id="79dc1-247">Select **OK** to save your query.</span></span>
1. <span data-ttu-id="79dc1-248">选择 **确定** 开始 *自动发放到仓库* 过程。</span><span class="sxs-lookup"><span data-stu-id="79dc1-248">Select **OK** to start the *Automatic release to warehouse* procedure.</span></span>

#### <a name="review-the-shipment-that-is-created-or-updated"></a><span data-ttu-id="79dc1-249">查看创建或更新的装运</span><span class="sxs-lookup"><span data-stu-id="79dc1-249">Review the shipment that is created or updated</span></span>

1. <span data-ttu-id="79dc1-250">转到 **仓库管理 \> 装运 \> 所有装运**。</span><span class="sxs-lookup"><span data-stu-id="79dc1-250">Go to **Warehouse management \> Shipments \> All shipments**.</span></span>
1. <span data-ttu-id="79dc1-251">找到并选择所需装运。</span><span class="sxs-lookup"><span data-stu-id="79dc1-251">Find and select the required shipment.</span></span>
1. <span data-ttu-id="79dc1-252">如果创建或更新装运时使用了合并策略，应该可以在 **装运合并策略** 字段中看到此策略。</span><span class="sxs-lookup"><span data-stu-id="79dc1-252">If a consolidation policy was used when the shipment was created or updated, you should see it in the **Shipment consolidation policy** field.</span></span>

### <a name="release-sales-orders-from-order-set-1"></a><span data-ttu-id="79dc1-253">发放订单集 1 中的销售订单</span><span class="sxs-lookup"><span data-stu-id="79dc1-253">Release sales orders from order set 1</span></span>

<span data-ttu-id="79dc1-254">执行[发放到仓库基本过程](#release-procedure)发放订单集 1 中的销售订单。</span><span class="sxs-lookup"><span data-stu-id="79dc1-254">Follow the [basic release-to-warehouse procedure](#release-procedure) to release the sales orders from order set 1.</span></span>

<span data-ttu-id="79dc1-255">完成后，您应该可以看到创建了下面两个装运：</span><span class="sxs-lookup"><span data-stu-id="79dc1-255">When you've finished, you should see that two shipments were created:</span></span>

- <span data-ttu-id="79dc1-256">第一个装运中包含三行，该装运是使用 *CustomerMode* 装运合并策略创建的。</span><span class="sxs-lookup"><span data-stu-id="79dc1-256">The first shipment contains three lines and was created by using the *CustomerMode* shipment consolidation policy.</span></span>
- <span data-ttu-id="79dc1-257">第二个装运（该装运不使用 *航空公司* 交装运输方式）是使用 *CustomerOrderNo* 装运合并策略创建的。</span><span class="sxs-lookup"><span data-stu-id="79dc1-257">The second shipment, which doesn't use the *Airways* transportation mode of delivery, was created by using the *CustomerOrderNo* shipment consolidation policy.</span></span>

### <a name="release-sales-orders-from-order-set-2"></a><span data-ttu-id="79dc1-258">发放订单集 2 中的销售订单</span><span class="sxs-lookup"><span data-stu-id="79dc1-258">Release sales orders from order set 2</span></span>

<span data-ttu-id="79dc1-259">执行[发放到仓库基本过程](#release-procedure)发放订单集 2 中的销售订单。</span><span class="sxs-lookup"><span data-stu-id="79dc1-259">Follow the [basic release-to-warehouse procedure](#release-procedure) to release the sales orders from order set 2.</span></span>

<span data-ttu-id="79dc1-260">完成后，您应该可以看到创建了下面三个装运：</span><span class="sxs-lookup"><span data-stu-id="79dc1-260">When you've finished, you should see that three shipments were created:</span></span>

- <span data-ttu-id="79dc1-261">第一个装运中包含 *易燃* 物品。</span><span class="sxs-lookup"><span data-stu-id="79dc1-261">The first shipment contains *Flammable* items.</span></span>
- <span data-ttu-id="79dc1-262">其他两个装运每个包含一行，该行有 *易爆* 物品。</span><span class="sxs-lookup"><span data-stu-id="79dc1-262">Each of the other two shipments contains one line that has the *Explosive* item.</span></span>

### <a name="release-sales-orders-from-order-set-3"></a><span data-ttu-id="79dc1-263">发放订单集 3 中的销售订单</span><span class="sxs-lookup"><span data-stu-id="79dc1-263">Release sales orders from order set 3</span></span>

<span data-ttu-id="79dc1-264">执行[发放到仓库基本过程](#release-procedure)发放订单集 3 中的销售订单。</span><span class="sxs-lookup"><span data-stu-id="79dc1-264">Follow the [basic release-to-warehouse procedure](#release-procedure) to release the sales orders from order set 3.</span></span>

<span data-ttu-id="79dc1-265">完成后，应该可以看到发生了以下操作：</span><span class="sxs-lookup"><span data-stu-id="79dc1-265">When you've finished, you should see that the following actions occurred:</span></span>

- <span data-ttu-id="79dc1-266">更新了一个现有装运（订单集 2 发放到仓库时创建的装运）。</span><span class="sxs-lookup"><span data-stu-id="79dc1-266">One existing shipment (the shipment that was created when order set 2 was released to the warehouse) was updated.</span></span> <span data-ttu-id="79dc1-267">添加了一个具有 *易燃* 物品的行。</span><span class="sxs-lookup"><span data-stu-id="79dc1-267">A line that has the *Flammable* item was added.</span></span>
- <span data-ttu-id="79dc1-268">创建了一个包含 *易爆* 物品的新装运。</span><span class="sxs-lookup"><span data-stu-id="79dc1-268">One new shipment was created that contains the *Explosive* item.</span></span>

### <a name="release-sales-orders-from-order-set-4"></a><span data-ttu-id="79dc1-269">发放订单集 4 中的销售订单</span><span class="sxs-lookup"><span data-stu-id="79dc1-269">Release sales orders from order set 4</span></span>

<span data-ttu-id="79dc1-270">执行[发放到仓库基本过程](#release-procedure)发放订单集 4 中的销售订单。</span><span class="sxs-lookup"><span data-stu-id="79dc1-270">Follow the [basic release-to-warehouse procedure](#release-procedure) to release the sales orders from order set 4.</span></span>

<span data-ttu-id="79dc1-271">完成后，应该可以看到更新了一个现有装运（其中的 **客户申请** 字段设置为 *1*）。</span><span class="sxs-lookup"><span data-stu-id="79dc1-271">When you've finished, you should see that one existing shipment (where the **Customer requisition** field is set to *1*) was updated.</span></span> <span data-ttu-id="79dc1-272">向其添加了一个新行。</span><span class="sxs-lookup"><span data-stu-id="79dc1-272">One new line was added to it.</span></span>

### <a name="release-sales-orders-from-order-set-5"></a><span data-ttu-id="79dc1-273">发放订单集 5 中的销售订单</span><span class="sxs-lookup"><span data-stu-id="79dc1-273">Release sales orders from order set 5</span></span>

<span data-ttu-id="79dc1-274">执行[发放到仓库基本过程](#release-procedure)发放订单集 5 中的销售订单。</span><span class="sxs-lookup"><span data-stu-id="79dc1-274">Follow the [basic release-to-warehouse procedure](#release-procedure) to release the sales orders from order set 5.</span></span>

<span data-ttu-id="79dc1-275">完成后，应该可以看到发生了以下操作：</span><span class="sxs-lookup"><span data-stu-id="79dc1-275">When you've finished, you should see that the following actions occurred:</span></span>

- <span data-ttu-id="79dc1-276">更新了一个现有装运（其中的 **客户申请** 字段设置为 *1*）。</span><span class="sxs-lookup"><span data-stu-id="79dc1-276">One existing shipment (where the **Customer requisition** field is set to *1*) was updated.</span></span> <span data-ttu-id="79dc1-277">向其添加了销售订单 5-3（其中的 **客户申请** 字段设置为 *1*）中的一行。</span><span class="sxs-lookup"><span data-stu-id="79dc1-277">A line from sales order 5-3 (where the **Customer requisition** field is set to *1*) was added to it.</span></span>
- <span data-ttu-id="79dc1-278">创建了一个新装运，其中销售订单 5-1 和 5-2 的行合并为一个装运。</span><span class="sxs-lookup"><span data-stu-id="79dc1-278">One new shipment was created, where lines from sales orders 5-1 and 5-2 are grouped into one shipment.</span></span>

### <a name="release-sales-orders-from-order-set-6"></a><span data-ttu-id="79dc1-279">发放订单集 6 中的销售订单</span><span class="sxs-lookup"><span data-stu-id="79dc1-279">Release sales orders from order set 6</span></span>

<span data-ttu-id="79dc1-280">执行[发放到仓库基本过程](#release-procedure)发放订单集 6 中的销售订单。</span><span class="sxs-lookup"><span data-stu-id="79dc1-280">Follow the [basic release-to-warehouse procedure](#release-procedure) to release the sales orders from order set 6.</span></span>

<span data-ttu-id="79dc1-281">完成后，您应该可以看到创建了下面四个装运：</span><span class="sxs-lookup"><span data-stu-id="79dc1-281">When you've finished, you should see that four shipments were created:</span></span>

- <span data-ttu-id="79dc1-282">使用 *订单池* 装运合并策略将客户 *US-003* 的两个订单的行合并到了一个装运中。</span><span class="sxs-lookup"><span data-stu-id="79dc1-282">Lines from two orders for customer *US-003* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="79dc1-283">使用 *订单池* 装运合并策略将客户 *US-004* 的两个订单的行合并到了一个装运中。</span><span class="sxs-lookup"><span data-stu-id="79dc1-283">Lines from two orders for customer *US-004* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="79dc1-284">使用 *订单池* 装运合并策略将客户 *US-007* 的销售订单 6-5 和 6-6 的行合并到了一个装运中。</span><span class="sxs-lookup"><span data-stu-id="79dc1-284">Lines from sales orders 6-5 and 6-6 for customer *US-007* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="79dc1-285">使用 *交叉订单* 装运合并策略将客户 *US-007* 的销售订单 6-7 和 6-8 的行合并到了一个装运中。</span><span class="sxs-lookup"><span data-stu-id="79dc1-285">Lines from sales orders 6-7 and 6-8 for customer *US-007* were grouped into one shipment by using the *CrossOrder* shipment consolidation policy.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="79dc1-286">其他资源</span><span class="sxs-lookup"><span data-stu-id="79dc1-286">Additional resources</span></span>

- [<span data-ttu-id="79dc1-287">装运合并政策</span><span class="sxs-lookup"><span data-stu-id="79dc1-287">Shipment consolidation policies</span></span>](about-shipment-consolidation-policies.md)
- [<span data-ttu-id="79dc1-288">配置装运合并策略</span><span class="sxs-lookup"><span data-stu-id="79dc1-288">Configure shipment consolidation policies</span></span>](configure-shipment-consolidation-policies.md)
