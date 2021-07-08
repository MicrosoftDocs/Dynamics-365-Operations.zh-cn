---
title: 集装箱包装策略
description: 本主题介绍了集装箱包装策略之间的差异并提供了示例。
author: GalynaFedorova
ms.date: 06/11/2021
ms.topic: article
ms.search.form: WHSWaveTemplateTable, InventLocationIdLookup, WHSContainerType, WHSContainerGroup, WHSContainerizationTable, WHSContainerizationBreak, WHSCreateContainerBreak, WHSContainerStructure, WHSContainerTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-06-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: f481f6ca047ee0285fe0e81d8fa96665e9d27cee
ms.sourcegitcommit: 8e846b52763f90d2232ec7d427839f4722570bce
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/22/2021
ms.locfileid: "6292753"
---
# <a name="container-packing-strategies"></a><span data-ttu-id="c4ce0-103">集装箱包装策略</span><span class="sxs-lookup"><span data-stu-id="c4ce0-103">Container packing strategies</span></span>

<span data-ttu-id="c4ce0-104">*集装箱包装策略* 是一种可用于定义跨集装箱的物料分配的策略。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-104">A *container packing strategy* is a strategy that you can use to define item allocations across containers.</span></span> <span data-ttu-id="c4ce0-105">本主题说明了 *包装到所有开放集装箱* 和 *仅包装到当前集装箱* 策略之间的差异。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-105">This topic explains the differences between the *Pack into all open containers* and *Pack into current container only* strategies.</span></span>

- <span data-ttu-id="c4ce0-106">**包装到所有开放集装箱** – 系统必须检查已在集装化周期期间创建的所有开放集装箱，以确保该物料适合其中一个集装箱。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-106">**Pack into all open containers** – The system must check all open containers that have already been created during the containerization cycle, to make sure that the item will fit into one of them.</span></span> <span data-ttu-id="c4ce0-107">在包装期间，系统检查每个物料以确定它是否适合之前创建的任何集装箱。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-107">During packing, the system checks each item to determine whether it will fit into any of the previously created containers.</span></span> <span data-ttu-id="c4ce0-108">如果物料不适合现有集装箱，系统将创建一个新集装箱并继续，直到完成整个订单的包装。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-108">If the item won't fit into an existing container, the system creates a new container and continues until it has finished packing the whole order.</span></span>

    <span data-ttu-id="c4ce0-109">例如，*n* 个订购的物料需要集装化。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-109">For example, *n* ordered items require containerization.</span></span> <span data-ttu-id="c4ce0-110">最坏的情况是，每次系统处理不适合任何现有集装箱的物料时，总共将执行 (\[(*n* – 1) × (*n* + 1)\] ÷ 2) 个检查以评估该物料是否适合现有集装箱。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-110">In the worst case, every time that the system processes an item that doesn't fit into any existing container, it will do a total of (\[(*n* – 1) × (*n* + 1)\] ÷ 2) checks to evaluate whether the item fits into the existing containers.</span></span>

- <span data-ttu-id="c4ce0-111">**仅包装到当前集装箱** – 系统必须仅检查最近创建的集装箱，以确保该物料适合该集装箱。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-111">**Pack into current container only** – The system must check only the most recently created container to make sure that the item will fit into it.</span></span> <span data-ttu-id="c4ce0-112">在包装期间，系统检查每个物料以确定它是否适合最近创建的集装箱。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-112">During packing, the system checks each item to determine whether it will fit into the most recently created container.</span></span> <span data-ttu-id="c4ce0-113">如果物料不适合该集装箱，系统将创建一个新集装箱并继续，直到完成整个订单的包装。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-113">If the item won't fit into that container, the system creates a new container and continues until it has finished packing the whole order.</span></span>

    <span data-ttu-id="c4ce0-114">例如，*n* 个订购的物料需要集装化。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-114">For example, *n* ordered items require containerization.</span></span> <span data-ttu-id="c4ce0-115">最坏的情况是，系统总共将执行 (*n* – 1) 个检查以评估该物料是否适合集装箱。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-115">In the worst case, the system will do a total of (*n* – 1) checks to evaluate whether the item fits into the containers.</span></span>

## <a name="example-of-the-flow-for-container-packing-strategies"></a><span data-ttu-id="c4ce0-116">集装箱包装策略流的示例</span><span class="sxs-lookup"><span data-stu-id="c4ce0-116">Example of the flow for container packing strategies</span></span>

<span data-ttu-id="c4ce0-117">您设置以下物料进行集装化。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-117">You set up the following items for containerization.</span></span>

| <span data-ttu-id="c4ce0-118">物料</span><span class="sxs-lookup"><span data-stu-id="c4ce0-118">Item</span></span> | <span data-ttu-id="c4ce0-119">物理维度（宽 × 深 × 高）</span><span class="sxs-lookup"><span data-stu-id="c4ce0-119">Physical dimensions (width × depth × height)</span></span> | <span data-ttu-id="c4ce0-120">权重</span><span class="sxs-lookup"><span data-stu-id="c4ce0-120">Weight</span></span> |
|---|---|---|
| <span data-ttu-id="c4ce0-121">HDMI 电缆 6'</span><span class="sxs-lookup"><span data-stu-id="c4ce0-121">HDMI Cable 6'</span></span> | <span data-ttu-id="c4ce0-122">1 × 1 × 1</span><span class="sxs-lookup"><span data-stu-id="c4ce0-122">1 × 1 × 1</span></span> | <span data-ttu-id="c4ce0-123">1</span><span class="sxs-lookup"><span data-stu-id="c4ce0-123">1</span></span> |
| <span data-ttu-id="c4ce0-124">HDMI 电缆 12'</span><span class="sxs-lookup"><span data-stu-id="c4ce0-124">HDMI Cable 12'</span></span> | <span data-ttu-id="c4ce0-125">2 × 1 × 1</span><span class="sxs-lookup"><span data-stu-id="c4ce0-125">2 × 1 × 1</span></span> | <span data-ttu-id="c4ce0-126">1</span><span class="sxs-lookup"><span data-stu-id="c4ce0-126">1</span></span> |
| <span data-ttu-id="c4ce0-127">HDMI 电缆 18'</span><span class="sxs-lookup"><span data-stu-id="c4ce0-127">HDMI Cable 18'</span></span> | <span data-ttu-id="c4ce0-128">3 × 1 × 1</span><span class="sxs-lookup"><span data-stu-id="c4ce0-128">3 × 1 × 1</span></span> | <span data-ttu-id="c4ce0-129">2</span><span class="sxs-lookup"><span data-stu-id="c4ce0-129">2</span></span> |

<span data-ttu-id="c4ce0-130">您还设置了以下将用于包装的箱。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-130">You also set up the following box that will be used for packaging.</span></span>

| <span data-ttu-id="c4ce0-131">容器</span><span class="sxs-lookup"><span data-stu-id="c4ce0-131">Container</span></span> | <span data-ttu-id="c4ce0-132">物理维度（长 × 宽 × 高）</span><span class="sxs-lookup"><span data-stu-id="c4ce0-132">Physical dimensions (length × width × height)</span></span> | <span data-ttu-id="c4ce0-133">权重</span><span class="sxs-lookup"><span data-stu-id="c4ce0-133">Weight</span></span> | <span data-ttu-id="c4ce0-134">体积</span><span class="sxs-lookup"><span data-stu-id="c4ce0-134">Volume</span></span> |
|---|---|---|---|
| <span data-ttu-id="c4ce0-135">中等箱</span><span class="sxs-lookup"><span data-stu-id="c4ce0-135">Medium Box</span></span> | <span data-ttu-id="c4ce0-136">6 × 3 × 2</span><span class="sxs-lookup"><span data-stu-id="c4ce0-136">6 × 3 × 2</span></span> | <span data-ttu-id="c4ce0-137">10</span><span class="sxs-lookup"><span data-stu-id="c4ce0-137">10</span></span> | <span data-ttu-id="c4ce0-138">100</span><span class="sxs-lookup"><span data-stu-id="c4ce0-138">100</span></span> |

<span data-ttu-id="c4ce0-139">最后，您设置具有以下产品和数量的订单。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-139">Finally, you set up an order that has the following products and quantities.</span></span>

| <span data-ttu-id="c4ce0-140">销售订单行</span><span class="sxs-lookup"><span data-stu-id="c4ce0-140">Sales order line</span></span> | <span data-ttu-id="c4ce0-141">数量</span><span class="sxs-lookup"><span data-stu-id="c4ce0-141">Quantity</span></span> |
|---|---|
| <span data-ttu-id="c4ce0-142">HDMI 电缆 12'</span><span class="sxs-lookup"><span data-stu-id="c4ce0-142">HDMI Cable 12'</span></span> | <span data-ttu-id="c4ce0-143">9</span><span class="sxs-lookup"><span data-stu-id="c4ce0-143">9</span></span> |
| <span data-ttu-id="c4ce0-144">HDMI 电缆 18'</span><span class="sxs-lookup"><span data-stu-id="c4ce0-144">HDMI Cable 18'</span></span> | <span data-ttu-id="c4ce0-145">8</span><span class="sxs-lookup"><span data-stu-id="c4ce0-145">8</span></span> |
| <span data-ttu-id="c4ce0-146">HDMI 电缆 6'</span><span class="sxs-lookup"><span data-stu-id="c4ce0-146">HDMI Cable 6'</span></span> | <span data-ttu-id="c4ce0-147">13</span><span class="sxs-lookup"><span data-stu-id="c4ce0-147">13</span></span> |

<span data-ttu-id="c4ce0-148">下表总结了集装化在使用 *包装到所有开放集装箱* 策略时以及使用 *仅包装到当前集装箱* 策略时的工作原理。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-148">The following table summarizes how containerization works when you use the *Pack into all open containers* strategy and when you use the *Pack into current container only* strategy.</span></span>

| <span data-ttu-id="c4ce0-149">装入所有打开的集装箱</span><span class="sxs-lookup"><span data-stu-id="c4ce0-149">Pack into all open containers</span></span> | <span data-ttu-id="c4ce0-150">包装到当前集装箱</span><span class="sxs-lookup"><span data-stu-id="c4ce0-150">Pack into current container</span></span> |
|---|---|
| <p><span data-ttu-id="c4ce0-151">HDMI 电缆 12'：</span><span class="sxs-lookup"><span data-stu-id="c4ce0-151">HDMI Cable 12':</span></span></p><ol><li><span data-ttu-id="c4ce0-152">创建一个新集装箱 CONT0001。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-152">Create a new container, CONT0001.</span></span></li><li><span data-ttu-id="c4ce0-153">将 9 个放入集装箱 CONT0001 中。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-153">Put 9 ea into container CONT0001.</span></span></li></ol> | <p><span data-ttu-id="c4ce0-154">HDMI 电缆 12'：</span><span class="sxs-lookup"><span data-stu-id="c4ce0-154">HDMI Cable 12':</span></span></p><ol><li><span data-ttu-id="c4ce0-155">创建一个新集装箱 CONT0001。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-155">Create a new container, CONT0001.</span></span></li><li><span data-ttu-id="c4ce0-156">将 9 个放入集装箱 CONT0001 中。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-156">Put 9 ea into container CONT0001.</span></span></li></ol> |
| <p><span data-ttu-id="c4ce0-157">HDMI 电缆 18'：</span><span class="sxs-lookup"><span data-stu-id="c4ce0-157">HDMI Cable 18':</span></span></p><ol><li><span data-ttu-id="c4ce0-158">检查物料是否适合集装箱 CONT0001。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-158">Check whether the item can fit into container CONT0001.</span></span></li><li><span data-ttu-id="c4ce0-159">创建一个新集装箱 CONT0002。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-159">Create a new container, CONT0002.</span></span></li><li><span data-ttu-id="c4ce0-160">将 5 个放入集装箱 CONT0002 中。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-160">Put 5 ea into container CONT0002.</span></span></li><li><span data-ttu-id="c4ce0-161">创建一个新集装箱 CONT0003。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-161">Create a new container, CONT0003.</span></span></li><li><span data-ttu-id="c4ce0-162">将 3 个放入集装箱 CONT0003 中。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-162">Put 3 ea into container CONT0003.</span></span></li></ol> | <p><span data-ttu-id="c4ce0-163">HDMI 电缆 18'：</span><span class="sxs-lookup"><span data-stu-id="c4ce0-163">HDMI Cable 18':</span></span></p><ol><li><span data-ttu-id="c4ce0-164">检查物料是否适合集装箱 CONT0001。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-164">Check whether the item can fit into container CONT0001.</span></span></li><li><span data-ttu-id="c4ce0-165">创建一个新集装箱 CONT0002。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-165">Create a new container, CONT0002.</span></span></li><li><span data-ttu-id="c4ce0-166">将 5 个放入集装箱 CONT0002 中。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-166">Put 5 ea into container CONT0002.</span></span></li><li><span data-ttu-id="c4ce0-167">创建一个新集装箱 CONT0003。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-167">Create a new container, CONT0003.</span></span></li><li><span data-ttu-id="c4ce0-168">将 3 个放入集装箱 CONT0003 中。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-168">Put 3 ea into container CONT0003.</span></span></li></ol> |
| <p><span data-ttu-id="c4ce0-169">HDMI 电缆 6'：</span><span class="sxs-lookup"><span data-stu-id="c4ce0-169">HDMI Cable 6':</span></span></p><ol><li><span data-ttu-id="c4ce0-170">检查物料是否适合集装箱 CONT0001。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-170">Check whether the item can fit into container CONT0001.</span></span></li><li><span data-ttu-id="c4ce0-171">将 1 个放入集装箱 CONT0001 中。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-171">Put 1 ea into container CONT0001.</span></span></li><li><span data-ttu-id="c4ce0-172">检查物料是否适合集装箱 CONT0002。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-172">Check whether the item can fit into container CONT0002.</span></span></li><li><span data-ttu-id="c4ce0-173">检查物料是否适合集装箱 CONT0003。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-173">Check whether the item can fit into container CONT0003.</span></span></li><li><span data-ttu-id="c4ce0-174">将 4 个放入集装箱 CONT0003 中。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-174">Put 4 ea into container CONT0003.</span></span></li><li><span data-ttu-id="c4ce0-175">创建一个新集装箱 CONT0004。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-175">Create a new container, CONT0004.</span></span></li><li><span data-ttu-id="c4ce0-176">将 8 个放入集装箱 CONT0004 中。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-176">Put 8 ea into container CONT0004.</span></span></li></ol> | <p><span data-ttu-id="c4ce0-177">HDMI 电缆 6'：</span><span class="sxs-lookup"><span data-stu-id="c4ce0-177">HDMI Cable 6':</span></span></p><ol><li><span data-ttu-id="c4ce0-178">检查物料是否适合集装箱 CONT0003。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-178">Check whether the item can fit into container CONT0003.</span></span></li><li><span data-ttu-id="c4ce0-179">将 4 个放入集装箱 CONT0003 中。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-179">Put 4 ea into container CONT0003.</span></span></li><li><span data-ttu-id="c4ce0-180">创建一个新集装箱 CONT0004。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-180">Create a new container, CONT0004.</span></span></li><li><span data-ttu-id="c4ce0-181">将 9 个放入集装箱 CONT0004 中。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-181">Put 9 ea into container CONT0004.</span></span></li></ol> |

## <a name="example-scenario-pack-single-orders-per-container"></a><span data-ttu-id="c4ce0-182">示例场景：每个集装箱包装单个订单</span><span class="sxs-lookup"><span data-stu-id="c4ce0-182">Example scenario: Pack single orders per container</span></span>

<span data-ttu-id="c4ce0-183">本部分显示一个场景，其中系统设置为将多个订单合并到一个装运中。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-183">This section presents a scenario where the system is set up to consolidate multiple orders into one shipment.</span></span> <span data-ttu-id="c4ce0-184">因此，从销售订单完成集装化，以确保包含多个产品的每个订单都包装到自己的集装箱中。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-184">Therefore, containerization will be done from the sales order to ensure that every order that contains multiple products is packed into its own container.</span></span>

<span data-ttu-id="c4ce0-185">此功能可让您处理必须仅将一个销售订单包装到每个集装箱的场景，以便配送中心可以在零售商店之间越库配送满载的集装箱。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-185">This functionality lets you handle scenarios where you must pack only one sales order into each container, so that the distribution center can cross-dock full containers between retail stores.</span></span> <span data-ttu-id="c4ce0-186">除了零售场景（每个零售商店的订单和装运到配送中心以进行越库配送）之外，此技术也常用于精益供应链（每个即时生产线的销售订单）。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-186">In addition to the retail scenarios (order per retail store and shipping to a distribution center for cross-docking) this technique is also commonly used in lean supply chains (sales order per just-in-time production line).</span></span>

<span data-ttu-id="c4ce0-187">此场景显示您可以如何使用 *仅包装到当前集装箱* 策略进行集装化来减少包装期间评估的集装箱数。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-187">This scenario shows how you can decrease the number of containers that are evaluated during packing by using the *Pack into current container only* strategy for containerization.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="c4ce0-188">先决条件</span><span class="sxs-lookup"><span data-stu-id="c4ce0-188">Prerequisites</span></span>

#### <a name="turn-on-the-consolidate-shipments-feature-in-your-system"></a><span data-ttu-id="c4ce0-189">在您的系统中打开合并装运功能</span><span class="sxs-lookup"><span data-stu-id="c4ce0-189">Turn on the Consolidate shipments feature in your system</span></span>

<span data-ttu-id="c4ce0-190">该场景使用 *合并装运* 功能。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-190">This scenario uses the *Consolidate shipments* feature.</span></span> <span data-ttu-id="c4ce0-191">如果该功能在您的系统中尚不可用，您必须使用[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)打开它。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-191">If that feature isn't already available in your system, you must turn it on by using [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>

#### <a name="make-demo-data-available"></a><span data-ttu-id="c4ce0-192">提供演示数据</span><span class="sxs-lookup"><span data-stu-id="c4ce0-192">Make demo data available</span></span>

<span data-ttu-id="c4ce0-193">此场景引用为 Microsoft Dynamics 365 Supply Chain Management 提供的标准演示数据中包含的值和记录。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-193">This scenario references values and records that are included in the standard demo data that is provided for Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="c4ce0-194">如果要在进行此练习时使用此处提供的值，请务必在安装了演示数据的环境中操作，并且在开始前将法人设置为 **USMF**。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-194">If you want to use the values that are provided here as you do the exercises, be sure to work in an environment where the demo data is installed, and set the legal entity to **USMF** before you begin.</span></span>

### <a name="inspect-or-create-container-types"></a><span data-ttu-id="c4ce0-195">检查或创建集装箱类型</span><span class="sxs-lookup"><span data-stu-id="c4ce0-195">Inspect or create container types</span></span>

<span data-ttu-id="c4ce0-196">若要检查您的集装箱类型，或根据需要创建新的集装箱类型，请按照以下步骤操作。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-196">To inspect your container types, or to create new container types if they are required, follow these steps.</span></span>

1. <span data-ttu-id="c4ce0-197">转到 **仓库管理** \> **设置** \> **集装箱** \> **集装箱类型**。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-197">Go to **Warehouse management** \> **Setup** \> **Containers** \> **Container types**.</span></span>
1. <span data-ttu-id="c4ce0-198">确保以下每种集装箱类型在您的演示数据中可用。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-198">Make sure that each of the following container types is available in your demo data.</span></span> <span data-ttu-id="c4ce0-199">根据需要编辑或创建集装箱类型。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-199">Edit or create container types as required.</span></span>

    - <span data-ttu-id="c4ce0-200">集装箱类型 1：</span><span class="sxs-lookup"><span data-stu-id="c4ce0-200">Container type 1:</span></span>

        - <span data-ttu-id="c4ce0-201">**集装箱类型代码**：*大箱*</span><span class="sxs-lookup"><span data-stu-id="c4ce0-201">**Container type code:** *Box-Large*</span></span>
        - <span data-ttu-id="c4ce0-202">**描述**：*大箱*</span><span class="sxs-lookup"><span data-stu-id="c4ce0-202">**Description:** *Large Box*</span></span>
        - <span data-ttu-id="c4ce0-203">**最大净重**：*100*</span><span class="sxs-lookup"><span data-stu-id="c4ce0-203">**Maximum net weight:** *100*</span></span>
        - <span data-ttu-id="c4ce0-204">**体积**：*400*</span><span class="sxs-lookup"><span data-stu-id="c4ce0-204">**Volume:** *400*</span></span>
        - <span data-ttu-id="c4ce0-205">**长度**：*4*</span><span class="sxs-lookup"><span data-stu-id="c4ce0-205">**Length:** *4*</span></span>
        - <span data-ttu-id="c4ce0-206">**宽度**：*10*</span><span class="sxs-lookup"><span data-stu-id="c4ce0-206">**Width:** *10*</span></span>
        - <span data-ttu-id="c4ce0-207">**高度**：*10*</span><span class="sxs-lookup"><span data-stu-id="c4ce0-207">**Height:** *10*</span></span>

    - <span data-ttu-id="c4ce0-208">集装箱类型 2：</span><span class="sxs-lookup"><span data-stu-id="c4ce0-208">Container type 2:</span></span>

        - <span data-ttu-id="c4ce0-209">**集装箱类型代码**：*中等箱*</span><span class="sxs-lookup"><span data-stu-id="c4ce0-209">**Container type code:** *Box-Medium*</span></span>
        - <span data-ttu-id="c4ce0-210">**描述**：*中等箱*</span><span class="sxs-lookup"><span data-stu-id="c4ce0-210">**Description:** *Medium Box*</span></span>
        - <span data-ttu-id="c4ce0-211">**最大净重**：*50*</span><span class="sxs-lookup"><span data-stu-id="c4ce0-211">**Maximum net weight:** *50*</span></span>
        - <span data-ttu-id="c4ce0-212">**体积**：*200*</span><span class="sxs-lookup"><span data-stu-id="c4ce0-212">**Volume:** *200*</span></span>
        - <span data-ttu-id="c4ce0-213">**长度**：*2*</span><span class="sxs-lookup"><span data-stu-id="c4ce0-213">**Length:** *2*</span></span>
        - <span data-ttu-id="c4ce0-214">**宽度**：*10*</span><span class="sxs-lookup"><span data-stu-id="c4ce0-214">**Width:** *10*</span></span>
        - <span data-ttu-id="c4ce0-215">**高度**：*10*</span><span class="sxs-lookup"><span data-stu-id="c4ce0-215">**Height:** *10*</span></span>

    - <span data-ttu-id="c4ce0-216">集装箱类型 3：</span><span class="sxs-lookup"><span data-stu-id="c4ce0-216">Container type 3:</span></span>

        - <span data-ttu-id="c4ce0-217">**集装箱类型代码**：*小箱*</span><span class="sxs-lookup"><span data-stu-id="c4ce0-217">**Container type code:** *Box-Small*</span></span>
        - <span data-ttu-id="c4ce0-218">**描述**：*小箱*</span><span class="sxs-lookup"><span data-stu-id="c4ce0-218">**Description:** *Small Box*</span></span>
        - <span data-ttu-id="c4ce0-219">**最大净重**：*20*</span><span class="sxs-lookup"><span data-stu-id="c4ce0-219">**Maximum net weight:** *20*</span></span>
        - <span data-ttu-id="c4ce0-220">**体积**：*100*</span><span class="sxs-lookup"><span data-stu-id="c4ce0-220">**Volume:** *100*</span></span>
        - <span data-ttu-id="c4ce0-221">**长度**：*1*</span><span class="sxs-lookup"><span data-stu-id="c4ce0-221">**Length:** *1*</span></span>
        - <span data-ttu-id="c4ce0-222">**宽度**：*10*</span><span class="sxs-lookup"><span data-stu-id="c4ce0-222">**Width:** *10*</span></span>
        - <span data-ttu-id="c4ce0-223">**高度**：*10*</span><span class="sxs-lookup"><span data-stu-id="c4ce0-223">**Height:** *10*</span></span>

### <a name="inspect-or-create-container-groups"></a><span data-ttu-id="c4ce0-224">检查或创建集装箱组</span><span class="sxs-lookup"><span data-stu-id="c4ce0-224">Inspect or create container groups</span></span>

<span data-ttu-id="c4ce0-225">若要检查您的集装箱组，或根据需要创建新的集装箱组，请按照以下步骤操作。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-225">To inspect your container groups, or to create new container groups if they are required, follow these steps.</span></span>

1. <span data-ttu-id="c4ce0-226">转到 **仓库管理** \> **设置** \> **集装箱** \> **集装箱组**。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-226">Go to **Warehouse management** \> **Setup** \> **Containers** \> **Container groups**.</span></span>
1. <span data-ttu-id="c4ce0-227">确保以下集装箱组在您的演示数据中可用。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-227">Make sure that the following container group is available in your demo data.</span></span> <span data-ttu-id="c4ce0-228">如果不可用，请选择 **新建** 创建它。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-228">If it isn't available, select **New** to create it.</span></span>

    - <span data-ttu-id="c4ce0-229">**集装箱组 ID**：*箱*</span><span class="sxs-lookup"><span data-stu-id="c4ce0-229">**Container group ID:** *Boxes*</span></span>
    - <span data-ttu-id="c4ce0-230">**描述**：*箱大小*</span><span class="sxs-lookup"><span data-stu-id="c4ce0-230">**Description:** *Box sizes*</span></span>

1. <span data-ttu-id="c4ce0-231">在 *箱* 集装箱组的 **详细信息** 快速选项卡上，确保存在以下行。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-231">On the **Details** FastTab for the *Boxes* container group, make sure that the following lines exist.</span></span> <span data-ttu-id="c4ce0-232">如果不存在，请选择 **新建** 添加它们。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-232">If they don't, select **New** to add them.</span></span>

    - <span data-ttu-id="c4ce0-233">行 1：</span><span class="sxs-lookup"><span data-stu-id="c4ce0-233">Line 1:</span></span>

        - <span data-ttu-id="c4ce0-234">**序列号**：*1*</span><span class="sxs-lookup"><span data-stu-id="c4ce0-234">**Sequence number:** *1*</span></span>
        - <span data-ttu-id="c4ce0-235">**集装箱类型**：*大箱*</span><span class="sxs-lookup"><span data-stu-id="c4ce0-235">**Container type:** *Box-Large*</span></span>
        - <span data-ttu-id="c4ce0-236">**集装箱利用率百分比**：*100*</span><span class="sxs-lookup"><span data-stu-id="c4ce0-236">**Container utilization percentage:** *100*</span></span>

    - <span data-ttu-id="c4ce0-237">行 2：</span><span class="sxs-lookup"><span data-stu-id="c4ce0-237">Line 2:</span></span>

        - <span data-ttu-id="c4ce0-238">**序列号**：*2*</span><span class="sxs-lookup"><span data-stu-id="c4ce0-238">**Sequence number:** *2*</span></span>
        - <span data-ttu-id="c4ce0-239">**集装箱类型**：*中等箱*</span><span class="sxs-lookup"><span data-stu-id="c4ce0-239">**Container type:** *Box-Medium*</span></span>
        - <span data-ttu-id="c4ce0-240">**集装箱利用率百分比**：*100*</span><span class="sxs-lookup"><span data-stu-id="c4ce0-240">**Container utilization percentage:** *100*</span></span>

    - <span data-ttu-id="c4ce0-241">行 3：</span><span class="sxs-lookup"><span data-stu-id="c4ce0-241">Line 3:</span></span>

        - <span data-ttu-id="c4ce0-242">**序列号**：*3*</span><span class="sxs-lookup"><span data-stu-id="c4ce0-242">**Sequence number:** *3*</span></span>
        - <span data-ttu-id="c4ce0-243">**集装箱类型**：*小箱*</span><span class="sxs-lookup"><span data-stu-id="c4ce0-243">**Container type:** *Box-Small*</span></span>
        - <span data-ttu-id="c4ce0-244">**集装箱利用率百分比**：*100*</span><span class="sxs-lookup"><span data-stu-id="c4ce0-244">**Container utilization percentage:** *100*</span></span>

### <a name="create-a-new-container-build-template"></a><span data-ttu-id="c4ce0-245">创建新的集装箱生成模板</span><span class="sxs-lookup"><span data-stu-id="c4ce0-245">Create a new container build template</span></span>

<span data-ttu-id="c4ce0-246">若要创建新的集装箱生成模板，请按照以下步骤操作。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-246">To create a new container build template, follow these steps.</span></span>

1. <span data-ttu-id="c4ce0-247">转到 **仓库管理** \> **设置** \> **集装箱** \> **集装箱生成模板**。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-247">Go to **Warehouse management** \> **Setup** \> **Containers** \> **Container build template**.</span></span>
1. <span data-ttu-id="c4ce0-248">选择 **新建** 创建具有以下设置的集装箱生成模板：</span><span class="sxs-lookup"><span data-stu-id="c4ce0-248">Select **New** to create a container build template that has the following settings:</span></span>

    - <span data-ttu-id="c4ce0-249">**序列号**：*1*</span><span class="sxs-lookup"><span data-stu-id="c4ce0-249">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="c4ce0-250">**集装箱模板 ID**：*箱*</span><span class="sxs-lookup"><span data-stu-id="c4ce0-250">**Container template ID:** *Box*</span></span>
    - <span data-ttu-id="c4ce0-251">**集装箱组 ID**：*箱*</span><span class="sxs-lookup"><span data-stu-id="c4ce0-251">**Container group ID:** *Boxes*</span></span>
    - <span data-ttu-id="c4ce0-252">**基本查询类型**：*销售分配行*</span><span class="sxs-lookup"><span data-stu-id="c4ce0-252">**Base query types:** *Sales allocation line*</span></span>
    - <span data-ttu-id="c4ce0-253">**波次步骤代码**：*234*</span><span class="sxs-lookup"><span data-stu-id="c4ce0-253">**Wave step code:** *234*</span></span>
    - <span data-ttu-id="c4ce0-254">**允许拆分领料**：*是*</span><span class="sxs-lookup"><span data-stu-id="c4ce0-254">**Allow split picks:** *Yes*</span></span>
    - <span data-ttu-id="c4ce0-255">**集装箱包装策略**：*仅包装到当前集装箱*</span><span class="sxs-lookup"><span data-stu-id="c4ce0-255">**Container packing strategy:** *Pack into current container only*</span></span>
    - <span data-ttu-id="c4ce0-256">**按指令单位包装**：*否*</span><span class="sxs-lookup"><span data-stu-id="c4ce0-256">**Pack by directive unit:** *No*</span></span>

1. <span data-ttu-id="c4ce0-257">在仍选择新模板行的同时，在操作窗格上选择 **编辑查询**。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-257">While the row for the new template is still selected, select **Edit query** on the Action Pane.</span></span>
1. <span data-ttu-id="c4ce0-258">将显示标准查询编辑器对话框。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-258">A standard query editor dialog box appears.</span></span> <span data-ttu-id="c4ce0-259">在 **排序** 选项卡上，选择 **添加** 以添加具有以下设置的行：</span><span class="sxs-lookup"><span data-stu-id="c4ce0-259">On the **Sorting** tab, select **Add** to add a row that has the following settings:</span></span>

    - <span data-ttu-id="c4ce0-260">**表**：*临时工作事务*</span><span class="sxs-lookup"><span data-stu-id="c4ce0-260">**Table:** *Temporary work transactions*</span></span>
    - <span data-ttu-id="c4ce0-261">**派生表**：*临时工作事务*</span><span class="sxs-lookup"><span data-stu-id="c4ce0-261">**Derived table:** *Temporary work transactions*</span></span>
    - <span data-ttu-id="c4ce0-262">**字段**：*订单编号*</span><span class="sxs-lookup"><span data-stu-id="c4ce0-262">**Field:** *Order number*</span></span>
    - <span data-ttu-id="c4ce0-263">**搜索方向**：*升序*</span><span class="sxs-lookup"><span data-stu-id="c4ce0-263">**Search direction:** *Ascending*</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="c4ce0-264">若要避免循环检查所有其他开放的集装箱，并通过一次检查一个集装箱来加快流程，除了按订单编号排序外，请使用 *仅包装到当前集装箱* 策略。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-264">To avoid cycling over all the other open containers, and to speed up the process by checking one container at a time, use the *Pack into current container only* strategy in addition to sorting by order number.</span></span> <span data-ttu-id="c4ce0-265">此组合将像工作模板上的工作分解一样工作。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-265">This combination will work like a work break on a work template.</span></span>

1. <span data-ttu-id="c4ce0-266">选择 **确定** 关闭查询编辑器对话框。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-266">Select **OK** to close the query editor dialog box.</span></span>
1. <span data-ttu-id="c4ce0-267">在仍选择新模板行的同时，在操作窗格上选择 **集装箱混合约束**。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-267">While the row for the new template is still selected, select **Container mixing constraints** on the Action Pane.</span></span>

    <span data-ttu-id="c4ce0-268">现在，您将添加一个约束，将单个订单中的物料放入单个集装箱中。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-268">You will now add a constraint that puts items from a single order into a single container.</span></span> <span data-ttu-id="c4ce0-269">来自任何其他订单的物料将放入单独的集装箱中。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-269">Items from any other order will be put into a separate container.</span></span>

1. <span data-ttu-id="c4ce0-270">选择 **新建** 创建具有以下设置的混合约束：</span><span class="sxs-lookup"><span data-stu-id="c4ce0-270">Select **New** to create a mixing constraint that has the following settings:</span></span>

    - <span data-ttu-id="c4ce0-271">**表**：*销售订单*</span><span class="sxs-lookup"><span data-stu-id="c4ce0-271">**Table:** *Sales orders*</span></span>
    - <span data-ttu-id="c4ce0-272">**字段选择**：*SalesId*（该字段在网格中将显示为 *销售订单*。）</span><span class="sxs-lookup"><span data-stu-id="c4ce0-272">**Field select:** *SalesId* (The field will appear as *Sales order* in the grid.)</span></span>

1. <span data-ttu-id="c4ce0-273">选择 **确定** 以添加约束。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-273">Select **OK** to add the constraint.</span></span>
1. <span data-ttu-id="c4ce0-274">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-274">Close the page.</span></span>

### <a name="set-up-a-wave-template-for-containerization"></a><span data-ttu-id="c4ce0-275">为集装化设置波次模板</span><span class="sxs-lookup"><span data-stu-id="c4ce0-275">Set up a wave template for containerization</span></span>

<span data-ttu-id="c4ce0-276">若要设置波次模板，请按照以下步骤操作。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-276">To set up a wave template, follow these steps.</span></span>

1. <span data-ttu-id="c4ce0-277">转到 **仓库管理 \> 设置 \> 波次 \> 波次模板**。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-277">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="c4ce0-278">在列表窗格中，将 **波次模板类型** 字段设置为 *装运*。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-278">In the list pane, set the **Wave template type** field to *Shipping*.</span></span>
1. <span data-ttu-id="c4ce0-279">在列表中选择 **63 集装化** 模板。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-279">Select the **63 Containerization** template in the list.</span></span>
1. <span data-ttu-id="c4ce0-280">在操作窗格上，选择 **编辑**。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-280">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="c4ce0-281">在 **方法** 快速选项卡上，在 **选定方法** 列中，找到以下行：</span><span class="sxs-lookup"><span data-stu-id="c4ce0-281">On the **Methods** FastTab, in the **Selected methods** column, find the following line:</span></span>

    - <span data-ttu-id="c4ce0-282">**方法名称**：*集装化*</span><span class="sxs-lookup"><span data-stu-id="c4ce0-282">**Method name:** *containerization*</span></span>
    - <span data-ttu-id="c4ce0-283">**名称**：*集装化*</span><span class="sxs-lookup"><span data-stu-id="c4ce0-283">**Name:** *Containerization*</span></span>

1. <span data-ttu-id="c4ce0-284">将行的 **波次步骤代码** 字段设置为 *234*。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-284">Set the **Wave step code** field for the line to *234*.</span></span>

### <a name="set-up-a-work-template"></a><span data-ttu-id="c4ce0-285">设置工作模板</span><span class="sxs-lookup"><span data-stu-id="c4ce0-285">Set up a work template</span></span>

<span data-ttu-id="c4ce0-286">若要设置工作模板，请按照以下步骤操作。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-286">To set up a work template, follow these steps.</span></span>

1. <span data-ttu-id="c4ce0-287">转到 **仓库管理 \> 设置 \> 工作 \> 工作模板**。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-287">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="c4ce0-288">将 **工作订单类型** 字段设置为 *销售订单*。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-288">Set the **Work order type** field to *Sales orders*.</span></span>
1. <span data-ttu-id="c4ce0-289">在 **概述** 网格中，找到并选择应该用于针对每个集装箱包装单个订单的工作模板。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-289">In the **Overview** grid, find and select the work template that should be used for packing single orders per container.</span></span> <span data-ttu-id="c4ce0-290">对于此场景，选择 **63 领料到集装箱** 模板。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-290">For this scenario, select the **63 Pick to container** template.</span></span>
1. <span data-ttu-id="c4ce0-291">在操作窗格上，选择 **编辑查询**。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-291">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="c4ce0-292">将显示标准查询编辑器对话框。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-292">A standard query editor dialog box appears.</span></span> <span data-ttu-id="c4ce0-293">在 **排序** 选项卡上，添加以下行：</span><span class="sxs-lookup"><span data-stu-id="c4ce0-293">On the **Sorting** tab, add the following lines:</span></span>

    - <span data-ttu-id="c4ce0-294">行 1：</span><span class="sxs-lookup"><span data-stu-id="c4ce0-294">Line 1:</span></span>

        - <span data-ttu-id="c4ce0-295">**表**：*临时工作事务*</span><span class="sxs-lookup"><span data-stu-id="c4ce0-295">**Table:** *Temporary work transactions*</span></span>
        - <span data-ttu-id="c4ce0-296">**派生表**：*临时工作事务*</span><span class="sxs-lookup"><span data-stu-id="c4ce0-296">**Derived table:** *Temporary work transactions*</span></span>
        - <span data-ttu-id="c4ce0-297">**字段**：*装运 ID*</span><span class="sxs-lookup"><span data-stu-id="c4ce0-297">**Field:** *Shipment ID*</span></span>
        - <span data-ttu-id="c4ce0-298">**搜索方向**：*升序*</span><span class="sxs-lookup"><span data-stu-id="c4ce0-298">**Search direction:** *Ascending*</span></span>

    - <span data-ttu-id="c4ce0-299">行 2：</span><span class="sxs-lookup"><span data-stu-id="c4ce0-299">Line 2:</span></span>

        - <span data-ttu-id="c4ce0-300">**表**：*临时工作事务*</span><span class="sxs-lookup"><span data-stu-id="c4ce0-300">**Table:** *Temporary work transactions*</span></span>
        - <span data-ttu-id="c4ce0-301">**派生表**：*临时工作事务*</span><span class="sxs-lookup"><span data-stu-id="c4ce0-301">**Derived table:** *Temporary work transactions*</span></span>
        - <span data-ttu-id="c4ce0-302">**字段**：*订单编号*</span><span class="sxs-lookup"><span data-stu-id="c4ce0-302">**Field:** *Order number*</span></span>
        - <span data-ttu-id="c4ce0-303">**搜索方向**：*升序*</span><span class="sxs-lookup"><span data-stu-id="c4ce0-303">**Search direction:** *Ascending*</span></span>

    - <span data-ttu-id="c4ce0-304">行 3：</span><span class="sxs-lookup"><span data-stu-id="c4ce0-304">Line 3:</span></span>

        - <span data-ttu-id="c4ce0-305">**表**：*临时工作事务*</span><span class="sxs-lookup"><span data-stu-id="c4ce0-305">**Table:** *Temporary work transactions*</span></span>
        - <span data-ttu-id="c4ce0-306">**派生表**：*临时工作事务*</span><span class="sxs-lookup"><span data-stu-id="c4ce0-306">**Derived table:** *Temporary work transactions*</span></span>
        - <span data-ttu-id="c4ce0-307">**字段**：*集装箱 ID*</span><span class="sxs-lookup"><span data-stu-id="c4ce0-307">**Field:** *Container ID*</span></span>
        - <span data-ttu-id="c4ce0-308">**搜索方向**：*升序*</span><span class="sxs-lookup"><span data-stu-id="c4ce0-308">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="c4ce0-309">选择 **确定** 关闭查询编辑器对话框。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-309">Select **OK** to close the query editor dialog box.</span></span>
1. <span data-ttu-id="c4ce0-310">您将收到以下消息：“分组将重置，是否继续？”</span><span class="sxs-lookup"><span data-stu-id="c4ce0-310">You receive the following message: "Grouping will be reset, continue?"</span></span> <span data-ttu-id="c4ce0-311">选择 **是** 继续。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-311">Select **Yes** to continue.</span></span>
1. <span data-ttu-id="c4ce0-312">在仍选择 **63 领料到集装箱** 模板的同时，在操作窗格上选择 **工作标题分解**。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-312">While the **63 Pick to container** template is still selected, select **Work header breaks** on the Action Pane.</span></span>

    <span data-ttu-id="c4ce0-313">现在，您将应用设置以分解工作，以便订单中的每个集装箱都链接到一个工作订单。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-313">You will now apply settings to break the work so that each container in the order is linked to one work order.</span></span>

1. <span data-ttu-id="c4ce0-314">在 **工作标题分解** 页面上为每一行选中 **按此字段分组** 复选框（**装运 ID**、**订单编号** 和 **集装箱 ID**）。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-314">Select the **Group by this field** checkbox for each row on the **Work header breaks** page (**Shipment ID**, **Order number**, and **Container ID**).</span></span>
1. <span data-ttu-id="c4ce0-315">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-315">Close the page.</span></span>

### <a name="set-up-shipment-consolidation-policies"></a><span data-ttu-id="c4ce0-316">设置装运合并策略</span><span class="sxs-lookup"><span data-stu-id="c4ce0-316">Set up shipment consolidation policies</span></span>

<span data-ttu-id="c4ce0-317">若要设置装运合并策略，请按照以下步骤操作。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-317">To set up a shipment consolidation policy, follow these steps.</span></span>

1. <span data-ttu-id="c4ce0-318">转到 **仓库管理 \> 设置 \> 发放到仓库 \> 装运合并策略**。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-318">Go to **Warehouse management \> Setup \> Release to warehouse \> Shipment consolidation policies**.</span></span>
1. <span data-ttu-id="c4ce0-319">在列表窗格中，将 **策略类型** 字段设置为 *销售订单*。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-319">In the list pane, set the **Policy type** field to *Sales orders*.</span></span>
1. <span data-ttu-id="c4ce0-320">在列表中选择 **默认** 策略。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-320">Select the **Default** policy in the list.</span></span>
1. <span data-ttu-id="c4ce0-321">在操作窗格上，选择 **编辑**。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-321">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="c4ce0-322">在 **合并字段** 快速选项卡上的 **选定字段** 列表中，选择 **字段名称** 字段设置为 *订单编号* 的行。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-322">On the **Consolidation fields** FastTab, in the **Selected fields** list, select the row where the **Field name** field is set to *Order number*.</span></span>
1. <span data-ttu-id="c4ce0-323">选择 **删除** 按钮 ![向左箭头](media/backward-button.png) 将字段移到 **其余字段** 列表中。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-323">Select the **Remove** button ![Left arrow](media/backward-button.png) to move the field to the **Remaining fields** list.</span></span>
1. <span data-ttu-id="c4ce0-324">在操作窗格上，选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-324">On the Action Pane, select **Save**.</span></span>

### <a name="set-up-physical-dimensions-for-the-product"></a><span data-ttu-id="c4ce0-325">为产品设置物理维度</span><span class="sxs-lookup"><span data-stu-id="c4ce0-325">Set up physical dimensions for the product</span></span>

<span data-ttu-id="c4ce0-326">若要为将在此场景中使用的产品设置物理维度，请按照以下步骤操作。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-326">To set up physical dimensions for the products that will be used in this scenario, follow these steps.</span></span>

1. <span data-ttu-id="c4ce0-327">转到 **产品信息管理 \> 产品 \> 已发布产品**。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-327">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="c4ce0-328">选择 **物料编号** 字段设置为 *A0001* 的产品。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-328">Select the product where the **Item number** field is set to *A0001*.</span></span>
1. <span data-ttu-id="c4ce0-329">在“操作窗格”上的 **管理库存** 选项卡上，在 **仓库** 组中，选择 **物理维度**。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-329">On the Action Pane, on the **Manage inventory** tab, in the **Warehouse** group, select **Physical dimensions**.</span></span>
1. <span data-ttu-id="c4ce0-330">在 **物理维度** 页面上，您应该在网格中看到以下行：</span><span class="sxs-lookup"><span data-stu-id="c4ce0-330">On the **Physical dimensions** page, you should see the following line in the grid:</span></span>

    - <span data-ttu-id="c4ce0-331">**单位**：*件*</span><span class="sxs-lookup"><span data-stu-id="c4ce0-331">**Unit:** *pcs*</span></span>
    - <span data-ttu-id="c4ce0-332">**毛重**：*3.00*</span><span class="sxs-lookup"><span data-stu-id="c4ce0-332">**Gross weight:** *3.00*</span></span>
    - <span data-ttu-id="c4ce0-333">**宽度**：*2.00*</span><span class="sxs-lookup"><span data-stu-id="c4ce0-333">**Width:** *2.00*</span></span>
    - <span data-ttu-id="c4ce0-334">**深度**：*2.00*</span><span class="sxs-lookup"><span data-stu-id="c4ce0-334">**Depth:** *2.00*</span></span>
    - <span data-ttu-id="c4ce0-335">**高度**：*4.00*</span><span class="sxs-lookup"><span data-stu-id="c4ce0-335">**Height:** *4.00*</span></span>
    - <span data-ttu-id="c4ce0-336">**体积**：*16.00*</span><span class="sxs-lookup"><span data-stu-id="c4ce0-336">**Volume:** *16.00*</span></span>

1. <span data-ttu-id="c4ce0-337">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-337">Close the page.</span></span>
1. <span data-ttu-id="c4ce0-338">选择 **物料编号** 字段设置为 *A0002* 的产品。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-338">Select the product where the **Item number** field is set to *A0002*.</span></span>
1. <span data-ttu-id="c4ce0-339">在“操作窗格”上的 **管理库存** 选项卡上，在 **仓库** 组中，选择 **物理维度**。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-339">On the Action Pane, on the **Manage inventory** tab, in the **Warehouse** group, select **Physical dimensions**.</span></span>
1. <span data-ttu-id="c4ce0-340">在 **物理维度** 页面上，您应该在网格中看到以下行：</span><span class="sxs-lookup"><span data-stu-id="c4ce0-340">On the **Physical dimensions** page, you should see the following line in the grid:</span></span>

    - <span data-ttu-id="c4ce0-341">**单位**：*件*</span><span class="sxs-lookup"><span data-stu-id="c4ce0-341">**Unit:** *pcs*</span></span>
    - <span data-ttu-id="c4ce0-342">**毛重**：*4.00*</span><span class="sxs-lookup"><span data-stu-id="c4ce0-342">**Gross weight:** *4.00*</span></span>
    - <span data-ttu-id="c4ce0-343">**宽度**：*3.00*</span><span class="sxs-lookup"><span data-stu-id="c4ce0-343">**Width:** *3.00*</span></span>
    - <span data-ttu-id="c4ce0-344">**深度**：*1.00*</span><span class="sxs-lookup"><span data-stu-id="c4ce0-344">**Depth:** *1.00*</span></span>
    - <span data-ttu-id="c4ce0-345">**高度**：*3.00*</span><span class="sxs-lookup"><span data-stu-id="c4ce0-345">**Height:** *3.00*</span></span>
    - <span data-ttu-id="c4ce0-346">**体积**：*9.00*</span><span class="sxs-lookup"><span data-stu-id="c4ce0-346">**Volume:** *9.00*</span></span>

### <a name="create-sales-order-1"></a><span data-ttu-id="c4ce0-347">创建销售订单 1</span><span class="sxs-lookup"><span data-stu-id="c4ce0-347">Create sales order 1</span></span>

<span data-ttu-id="c4ce0-348">要创建销售订单，请按照下面的步骤操作。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-348">To create a sales order, follow these steps.</span></span>

1. <span data-ttu-id="c4ce0-349">转到 **销售和营销 \> 销售订单 \> 所有销售订单**。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-349">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="c4ce0-350">在操作窗格上，选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-350">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="c4ce0-351">显示用于创建新销售订单的对话框。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-351">A dialog box for creating a new sales order appears.</span></span> <span data-ttu-id="c4ce0-352">设置以下值：</span><span class="sxs-lookup"><span data-stu-id="c4ce0-352">Set the following values:</span></span>

    - <span data-ttu-id="c4ce0-353">**客户帐户**：*US-001*</span><span class="sxs-lookup"><span data-stu-id="c4ce0-353">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="c4ce0-354">**仓库**：*63*</span><span class="sxs-lookup"><span data-stu-id="c4ce0-354">**Warehouse:** *63*</span></span>

1. <span data-ttu-id="c4ce0-355">选择 **确定** 创建销售订单，然后关闭对话框。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-355">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="c4ce0-356">将打开新销售订单。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-356">The new sales order is opened.</span></span> <span data-ttu-id="c4ce0-357">在 **销售订单行** 快速选项卡上，添加以下销售行：</span><span class="sxs-lookup"><span data-stu-id="c4ce0-357">On the **Sales order lines** FastTab, add the following sales lines:</span></span>

    - <span data-ttu-id="c4ce0-358">行 1：</span><span class="sxs-lookup"><span data-stu-id="c4ce0-358">Line 1:</span></span>

        - <span data-ttu-id="c4ce0-359">\**物料编号：\*\*\*A0001*</span><span class="sxs-lookup"><span data-stu-id="c4ce0-359">**Item number:** *A0001*</span></span>
        - <span data-ttu-id="c4ce0-360">**数量：** *2*</span><span class="sxs-lookup"><span data-stu-id="c4ce0-360">**Quantity:** *2*</span></span>

    - <span data-ttu-id="c4ce0-361">行 2：</span><span class="sxs-lookup"><span data-stu-id="c4ce0-361">Line 2:</span></span>

        - <span data-ttu-id="c4ce0-362">\**物料编号：\*\*\*A0002*</span><span class="sxs-lookup"><span data-stu-id="c4ce0-362">**Item number:** *A0002*</span></span>
        - <span data-ttu-id="c4ce0-363">**数量：** *2*</span><span class="sxs-lookup"><span data-stu-id="c4ce0-363">**Quantity:** *2*</span></span>

1. <span data-ttu-id="c4ce0-364">选择第一行，然后选择 **库存 \> 预留**。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-364">Select the first line, and then select **Inventory \> Reservation**.</span></span>
1. <span data-ttu-id="c4ce0-365">在 **预留** 页上，选择 **预留批次**。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-365">On the **Reservation** page, select **Reserve lot**.</span></span> <span data-ttu-id="c4ce0-366">然后关闭页面。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-366">Then close the page.</span></span>
1. <span data-ttu-id="c4ce0-367">对第二行重复前两个步骤。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-367">Repeat the previous two steps for the second line.</span></span>
1. <span data-ttu-id="c4ce0-368">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-368">Close the page.</span></span>

### <a name="create-sales-order-2"></a><span data-ttu-id="c4ce0-369">创建销售订单 2</span><span class="sxs-lookup"><span data-stu-id="c4ce0-369">Create sales order 2</span></span>

<span data-ttu-id="c4ce0-370">若要创建第二个销售订单，请按照以下步骤操作。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-370">To create a second sales order, follow these steps.</span></span>

1. <span data-ttu-id="c4ce0-371">转到 **销售和营销 \> 销售订单 \> 所有销售订单**。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-371">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="c4ce0-372">在操作窗格上，选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-372">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="c4ce0-373">显示用于创建新销售订单的对话框。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-373">A dialog box for creating a new sales order appears.</span></span> <span data-ttu-id="c4ce0-374">设置以下值：</span><span class="sxs-lookup"><span data-stu-id="c4ce0-374">Set the following values:</span></span>

    - <span data-ttu-id="c4ce0-375">**客户帐户**：*US-001*</span><span class="sxs-lookup"><span data-stu-id="c4ce0-375">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="c4ce0-376">**仓库**：*63*</span><span class="sxs-lookup"><span data-stu-id="c4ce0-376">**Warehouse:** *63*</span></span>

1. <span data-ttu-id="c4ce0-377">选择 **确定** 创建销售订单，然后关闭对话框。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-377">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="c4ce0-378">将打开新销售订单。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-378">The new sales order is opened.</span></span> <span data-ttu-id="c4ce0-379">在 **销售订单行** 快速选项卡上，添加以下销售行：</span><span class="sxs-lookup"><span data-stu-id="c4ce0-379">On the **Sales order lines** FastTab, add the following sales lines:</span></span>

    - <span data-ttu-id="c4ce0-380">行 1：</span><span class="sxs-lookup"><span data-stu-id="c4ce0-380">Line 1:</span></span>

        - <span data-ttu-id="c4ce0-381">\**物料编号：\*\*\*A0001*</span><span class="sxs-lookup"><span data-stu-id="c4ce0-381">**Item number:** *A0001*</span></span>
        - <span data-ttu-id="c4ce0-382">**数量：** *4*</span><span class="sxs-lookup"><span data-stu-id="c4ce0-382">**Quantity:** *4*</span></span>

    - <span data-ttu-id="c4ce0-383">行 2：</span><span class="sxs-lookup"><span data-stu-id="c4ce0-383">Line 2:</span></span>

        - <span data-ttu-id="c4ce0-384">\**物料编号：\*\*\*A0002*</span><span class="sxs-lookup"><span data-stu-id="c4ce0-384">**Item number:** *A0002*</span></span>
        - <span data-ttu-id="c4ce0-385">**数量：** *4*</span><span class="sxs-lookup"><span data-stu-id="c4ce0-385">**Quantity:** *4*</span></span>

1. <span data-ttu-id="c4ce0-386">选择第一行，然后选择 **库存 \> 预留**。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-386">Select the first line, and then select **Inventory \> Reservation**.</span></span>
1. <span data-ttu-id="c4ce0-387">在 **预留** 页上，选择 **预留批次**。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-387">On the **Reservation** page, select **Reserve lot**.</span></span> <span data-ttu-id="c4ce0-388">然后关闭页面。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-388">Then close the page.</span></span>
1. <span data-ttu-id="c4ce0-389">对第二行重复前两个步骤。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-389">Repeat the previous two steps for the second line.</span></span>
1. <span data-ttu-id="c4ce0-390">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-390">Close the page.</span></span>

### <a name="create-the-load"></a><span data-ttu-id="c4ce0-391">创建负荷</span><span class="sxs-lookup"><span data-stu-id="c4ce0-391">Create the load</span></span>

<span data-ttu-id="c4ce0-392">若要为您为此场景创建的每个订单创建负荷，然后将其发放到仓库，请按照以下步骤操作。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-392">To create a load for each order that you created for this scenario and then release it to the warehouse, follow these steps.</span></span>

1. <span data-ttu-id="c4ce0-393">转到 **仓库管理 \> 装载 \> 装载计划工作台**。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-393">Go to **Warehouse management \> Loads \> Load planning workbench**.</span></span>
1. <span data-ttu-id="c4ce0-394">在 **销售行** 选项卡上，找到并选择为此场景创建的销售订单中的所有销售订单行。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-394">On the **Sales lines** tab, find and select all the sales order lines from the sales orders that you created for this scenario.</span></span>
1. <span data-ttu-id="c4ce0-395">在操作窗格上 **供应与需求** 选项卡上 **添加** 组中，选择 **至新负荷**。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-395">On the Action Pane, on the **Supply and demand** tab, in the **Add** group, select **To new load**.</span></span> <span data-ttu-id="c4ce0-396">选定订单行将添加到新负荷中。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-396">The selected order lines are added to a new load.</span></span>
1. <span data-ttu-id="c4ce0-397">在 **负荷模板分配** 对话框的 **负荷模板 ID** 字段中，选择负荷模板，例如 *40' 集装箱*。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-397">In the **Load template assignment** dialog box, in the **Load template ID** field, select a load template, such as *40' Container*.</span></span>
1. <span data-ttu-id="c4ce0-398">选择 **确定** 关闭对话框。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-398">Select **OK** to close the dialog box.</span></span>
1. <span data-ttu-id="c4ce0-399">在 **装载** 部分中，找到并选择刚才创建的装载。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-399">In the **Loads** section, find and select the load that you just created.</span></span>
1. <span data-ttu-id="c4ce0-400">选择 **发放 \> 发放到仓库**。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-400">Select **Release \> Release to warehouse**.</span></span>
1. <span data-ttu-id="c4ce0-401">在 **发放到仓库** 对话框中，选择 **确定** 以将选定负荷发放到仓库。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-401">In the **Release to warehouse** dialog box, select **OK** to release the selected load to the warehouse.</span></span>

### <a name="verify-the-shipments-and-containers"></a><span data-ttu-id="c4ce0-402">验证装运和集装箱</span><span class="sxs-lookup"><span data-stu-id="c4ce0-402">Verify the shipments and containers</span></span>

<span data-ttu-id="c4ce0-403">以下过程可让您验证已创建的装运。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-403">The following procedure lets you verify the shipments that have been created.</span></span> <span data-ttu-id="c4ce0-404">使用它查看您为此场景创建的订单，以确保您获得了预期的结果。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-404">Use it to review the order that you created for this scenario, to make sure that you've obtained the expected results.</span></span>

1. <span data-ttu-id="c4ce0-405">转到 **仓库管理 \> 装运 \> 所有装运**。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-405">Go to **Warehouse management \> Shipments \> All shipments**.</span></span>
1. <span data-ttu-id="c4ce0-406">查找并选择已为刚发放的负荷创建的装运。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-406">Find and select the shipment that was created for the load that you just released.</span></span>
1. <span data-ttu-id="c4ce0-407">在操作窗格上的 **运输** 选项卡上，选择 **查看集装箱**。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-407">On the Action Pane, on the **Transportation** tab, select **View containers**.</span></span>
1. <span data-ttu-id="c4ce0-408">确认销售订单中的物料已集装化到两个不同的集装箱中。</span><span class="sxs-lookup"><span data-stu-id="c4ce0-408">Confirm that the items from the sales orders were containerized into two different containers.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c4ce0-409">其他资源</span><span class="sxs-lookup"><span data-stu-id="c4ce0-409">Additional resources</span></span>

- [<span data-ttu-id="c4ce0-410">集装化</span><span class="sxs-lookup"><span data-stu-id="c4ce0-410">Containerization</span></span>](wave-containerization.md)
