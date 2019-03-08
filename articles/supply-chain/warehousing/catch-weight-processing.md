---
title: 使用仓库管理进行实际称重产品处理
description: 本主题介绍如何使用工作模板和库位指令确定在仓库中如何以及在哪里完成工作。
author: perlynne
manager: AnnBe
ms.date: 01/10/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSCatchWeightTag, WHSCatchWeightItemHandlingPolicy
ROBOTS: NOINDEX, NOFOLLOW
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-1-31
ms.dyn365.ops.version: 8.1.3
ms.openlocfilehash: 5161860e3b1c5b0ae795d109159268be085ec5af
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/29/2019
ms.locfileid: "334051"
---
# <a name="catch-weight-product-processing-with-warehouse-management"></a><span data-ttu-id="21a7d-103">使用仓库管理进行实际称重产品处理</span><span class="sxs-lookup"><span data-stu-id="21a7d-103">Catch weight product processing with warehouse management</span></span>
[!include [preview banner](../../includes/preview-banner.md)]
[!include [banner](../includes/banner.md)]

<span data-ttu-id="21a7d-104">**功能曝光**</span><span class="sxs-lookup"><span data-stu-id="21a7d-104">**Feature exposure**</span></span>

<span data-ttu-id="21a7d-105">若要使用仓库管理处理实际称重产品，必须使用许可证配置键打开功能。</span><span class="sxs-lookup"><span data-stu-id="21a7d-105">To use warehouse management to process catch weight products, you must use a license configuration key to turn on the functionality.</span></span> <span data-ttu-id="21a7d-106">（转到**系统管理 \> 设置 \> 许可证配置**。</span><span class="sxs-lookup"><span data-stu-id="21a7d-106">(Go to **System administration \> Setup \> License configuration**.</span></span> <span data-ttu-id="21a7d-107">然后，在**配置键**选项卡上，展开**贸易 \> 仓库和运输管理**，然后选择**面向仓库的实际称重**复选框）。</span><span class="sxs-lookup"><span data-stu-id="21a7d-107">Then, on the **Configuration keys** tab, expand **Trade \> Warehouse and Transportation management**, and select the check box for **Catch weight for warehouse**).</span></span>

> [!NOTE]
> <span data-ttu-id="21a7d-108">还必须打开**仓库和运输管理**许可证配置键和**流程分配实际称重**许可证配置键。</span><span class="sxs-lookup"><span data-stu-id="21a7d-108">Both the **Warehouse and Transportation management** license configuration key and the **Process distribution catch weight** license configuration keys must also be turned on.</span></span>

<span data-ttu-id="21a7d-109">在许可证配置键打开后，在您创建已发放产品时，您可以选择**实际称重**。</span><span class="sxs-lookup"><span data-stu-id="21a7d-109">After the license configuration key is turned on, when you create a released product, you can select **Catch weight**.</span></span> <span data-ttu-id="21a7d-110">您还可以将发放的产品与为其选择了**使用仓库管理流程**参数的存储维度组关联。</span><span class="sxs-lookup"><span data-stu-id="21a7d-110">You can also associate the released product with a storage dimension group that the **Use warehouse management processes** parameter is selected for.</span></span>

<span data-ttu-id="21a7d-111">您必须为实际称重进行某些基本产品的特定设置，然后才可以在“仓库管理”中使用产品：</span><span class="sxs-lookup"><span data-stu-id="21a7d-111">Before you can use the product in Warehouse management, you must do some basic product-specific setup for catch weight:</span></span>

- <span data-ttu-id="21a7d-112">在单位转换定义中定义实际称重单位（箱）和库存单位（千克）\[kg\] 之间的标称重量转换。</span><span class="sxs-lookup"><span data-stu-id="21a7d-112">Define the nominal weight conversion between the catch weight unit (box) and the inventory unit (kilogram \[kg\]) as part of a unit conversion definition.</span></span>
- <span data-ttu-id="21a7d-113">在实际称重单位设置中，定义最小和最大重量容差。</span><span class="sxs-lookup"><span data-stu-id="21a7d-113">Define the minimum and maximum weight tolerances as part of the catch weight unit setup.</span></span>
- <span data-ttu-id="21a7d-114">设置实际称重单位定义为最低库存单位 (SKU) 的单位序列组。</span><span class="sxs-lookup"><span data-stu-id="21a7d-114">Set up a unit sequence group where the catch weight unit is defined as the lowest stock keeping unit (SKU).</span></span>
- <span data-ttu-id="21a7d-115">设置实际称重物料处理策略。</span><span class="sxs-lookup"><span data-stu-id="21a7d-115">Set up a catch weight item handling policy.</span></span>

<span data-ttu-id="21a7d-116">有关详细信息，请参阅[设置和维护实际称重物料](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/setting-up-and-maintaining-catch-weight-items)。</span><span class="sxs-lookup"><span data-stu-id="21a7d-116">For more information, see [Setting up and maintaining catch weight items](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/setting-up-and-maintaining-catch-weight-items).</span></span>

## <a name="transaction-adjustments"></a><span data-ttu-id="21a7d-117">交易记录调整</span><span class="sxs-lookup"><span data-stu-id="21a7d-117">Transaction adjustments</span></span>

<span data-ttu-id="21a7d-118">由于库存重量在涉及到仓库时可能不同于库存从仓库发放时的重量，所以实际称重产品处理必须调整库存。</span><span class="sxs-lookup"><span data-stu-id="21a7d-118">Because the weight of inventory when it comes into a warehouse can differ from the weight when the inventory is issued out of the warehouse, the catch weight product processing must adjust the inventory.</span></span>

<span data-ttu-id="21a7d-119">**示例 1**</span><span class="sxs-lookup"><span data-stu-id="21a7d-119">**Example 1**</span></span>

<span data-ttu-id="21a7d-120">在**完工入库**生产流程中，包含八箱实际称重产品的牌照的进货重量捕获为 80.1 千克。</span><span class="sxs-lookup"><span data-stu-id="21a7d-120">During a **Report as finished** production process, the inbound weight of a license plate that contains eight boxes of a catch weight product is captured as 80.1 kg.</span></span> <span data-ttu-id="21a7d-121">牌照之后存储在成品区域，存储期间，部分重量在空气中流失。</span><span class="sxs-lookup"><span data-stu-id="21a7d-121">The license plate is then stored away in the finished goods area, and during the storage period, some weight is lost into the air.</span></span>

<span data-ttu-id="21a7d-122">之后，在销售订单领料流程中，同一个牌照的重量捕获为 79.8 千克。</span><span class="sxs-lookup"><span data-stu-id="21a7d-122">Later, as part of a sales order picking process, the weight of the same license plate is captured as 79.8 kg.</span></span> <span data-ttu-id="21a7d-123">因此，在系统中，您现在在物理维度设置中将有重量差异。</span><span class="sxs-lookup"><span data-stu-id="21a7d-123">Therefore, in the system, you now have a weight difference as part of the physical dimension set.</span></span>

<span data-ttu-id="21a7d-124">在这种情况下，系统将通过过帐缺少的 0.3 千克的交易记录来自动调整此差异。</span><span class="sxs-lookup"><span data-stu-id="21a7d-124">In this case, the system automatically adjusts the difference by posting a transaction for the missing 0.3 kg.</span></span>

<span data-ttu-id="21a7d-125">**示例 2**</span><span class="sxs-lookup"><span data-stu-id="21a7d-125">**Example 2**</span></span>

<span data-ttu-id="21a7d-126">在其定义中，产品被设置为最多允许**箱**实际称重单位的最小 8 千克重量、最大 12 千克重量。</span><span class="sxs-lookup"><span data-stu-id="21a7d-126">In its definition, a product is set up to tolerate a minimum weight of 8 kg and a maximum weight of 12 kg for the **Box** catch weight unit.</span></span>

<span data-ttu-id="21a7d-127">您有两箱产品，它们登记的重量为 16 千克。</span><span class="sxs-lookup"><span data-stu-id="21a7d-127">You have two boxes of the product, and they have a registered weight of 16 kg.</span></span> <span data-ttu-id="21a7d-128">如果仓库工作人员领取其中一箱并称重，重量捕获为 9 千克，另一箱重量将为 7 千克。</span><span class="sxs-lookup"><span data-stu-id="21a7d-128">If a warehouse worker picks and weighs one of the boxes, and the weight is captured as 9 kg, the remaining box will weigh 7 kg.</span></span> <span data-ttu-id="21a7d-129">但是，因为 7 千克低于最小重量，系统将执行自动调整，将现有库存重量增加 1 千克。</span><span class="sxs-lookup"><span data-stu-id="21a7d-129">However, because 7 kg is below the minimum weight, the system does an automatic adjustment to increase the weight of the on-hand inventory by 1 kg.</span></span>

<span data-ttu-id="21a7d-130">若要设置这些调整所过帐到的科目，请转到**成本管理 \> 分类帐集成策略设置 \> 过帐**。</span><span class="sxs-lookup"><span data-stu-id="21a7d-130">To set up the accounts that these adjustments are posted to, go to **Cost management \> Ledger integration policies setup \> Posting**.</span></span> <span data-ttu-id="21a7d-131">然后，在**库存**选项卡上，定义以下科目：</span><span class="sxs-lookup"><span data-stu-id="21a7d-131">Then, on the **Inventory** tab, define the following accounts:</span></span>

- <span data-ttu-id="21a7d-132">实际称重损失科目</span><span class="sxs-lookup"><span data-stu-id="21a7d-132">Catch weight loss account</span></span>
- <span data-ttu-id="21a7d-133">实际称重利润科目</span><span class="sxs-lookup"><span data-stu-id="21a7d-133">Catch weight profit account</span></span>

## <a name="catch-weight-item-handling-policy"></a><span data-ttu-id="21a7d-134">实际称重物料处理策略</span><span class="sxs-lookup"><span data-stu-id="21a7d-134">Catch weight item handling policy</span></span>

<span data-ttu-id="21a7d-135">实际称重物料处理策略定义物料的两个主要仓库管理流程：何时捕获物料重量，以及如何捕获。</span><span class="sxs-lookup"><span data-stu-id="21a7d-135">The catch weight item handling policy defines two primary warehouse management flows for the items: when the weight of the items is captured, and how it's captured.</span></span>

<span data-ttu-id="21a7d-136">您可以定义什么时候为销售和转移单处理捕获重量。</span><span class="sxs-lookup"><span data-stu-id="21a7d-136">You can define when the weight is captured for sales and transfer order processing.</span></span> <span data-ttu-id="21a7d-137">重量可以在以下流程的任意一个流程期间捕获：</span><span class="sxs-lookup"><span data-stu-id="21a7d-137">The weight can be captured during either of the following processes:</span></span>

- <span data-ttu-id="21a7d-138">**领料** – 重量在订单工作的初始领料工作行期间捕获。</span><span class="sxs-lookup"><span data-stu-id="21a7d-138">**Picking** – The weight is captured during the initial pick work lines of order work.</span></span>
- <span data-ttu-id="21a7d-139">**装箱** – 重量在人工装箱期间捕获。</span><span class="sxs-lookup"><span data-stu-id="21a7d-139">**Packing** – The weight is captured during manual packing.</span></span> <span data-ttu-id="21a7d-140">（必须将物料发送到装箱工作站。）</span><span class="sxs-lookup"><span data-stu-id="21a7d-140">(You must send the items to a packing station.)</span></span>

<span data-ttu-id="21a7d-141">如果实际重量在集装箱装箱流程期间在装箱工作站捕获，在领料工作期间，将不提示仓库工作人员捕获重量。</span><span class="sxs-lookup"><span data-stu-id="21a7d-141">If the actual weight is captured at the packing station during the container packing processes, warehouse workers won't be prompted to capture the weight during picking work.</span></span> <span data-ttu-id="21a7d-142">物理库存的平均重量将被用作转到装箱区域的已领取库存的重量。</span><span class="sxs-lookup"><span data-stu-id="21a7d-142">Instead, the average weight of the physical inventory will be used as the weight of the picked inventory that goes to the packing area.</span></span>

<span data-ttu-id="21a7d-143">对于内部仓库管理流程，如盘点和调整更正，可以定义重量是否应捕获。</span><span class="sxs-lookup"><span data-stu-id="21a7d-143">For internal warehouse management processes like counting and adjustment corrections it is possible to define if the weight should be captured or not.</span></span> <span data-ttu-id="21a7d-144">如果未捕获，将使用标称重量。</span><span class="sxs-lookup"><span data-stu-id="21a7d-144">If not captured the nominal weight will be used.</span></span>

<span data-ttu-id="21a7d-145">您还可以定义如何捕获重量。</span><span class="sxs-lookup"><span data-stu-id="21a7d-145">You can also define how the weight is captured.</span></span> <span data-ttu-id="21a7d-146">在两个主要流之一，实际称重标记被跟踪并用于捕获重量。</span><span class="sxs-lookup"><span data-stu-id="21a7d-146">In one of the two main flows, catch weight tags are tracked and used to capture the weight.</span></span> <span data-ttu-id="21a7d-147">在另一个流中，不跟踪实际称重标记。</span><span class="sxs-lookup"><span data-stu-id="21a7d-147">In the other flow, catch weight tags aren't tracked.</span></span>

- <span data-ttu-id="21a7d-148">**是** – 物料使用实际称重标记。</span><span class="sxs-lookup"><span data-stu-id="21a7d-148">**Yes** – The item uses catch weight tags.</span></span> <span data-ttu-id="21a7d-149">每个标记编号表示一个实际称重单位（箱），重量以及其他信息与标记关联。</span><span class="sxs-lookup"><span data-stu-id="21a7d-149">Each tag number represents one catch weight unit (box), and a weight and other information are associated with the tag.</span></span> <span data-ttu-id="21a7d-150">对于出货流程，使用与标记关联的重量。</span><span class="sxs-lookup"><span data-stu-id="21a7d-150">For outbound processes, the weight that is associated with the tag is used.</span></span>
- <span data-ttu-id="21a7d-151">**否** – 物料不使用实际称重标记。</span><span class="sxs-lookup"><span data-stu-id="21a7d-151">**No** – The item doesn't use catch weight tags.</span></span> <span data-ttu-id="21a7d-152">进货和出货称重流程基于在每个流程中捕获的实际重量。</span><span class="sxs-lookup"><span data-stu-id="21a7d-152">The inbound and outbound weighing processes are based on the actual weight that is captured during each process.</span></span>

<span data-ttu-id="21a7d-153">跟踪实际称重标记的流程可以用于存储期间不会更改重量的物料。</span><span class="sxs-lookup"><span data-stu-id="21a7d-153">The process of tracking catch weight tags can be used for items that won't change weight during the storage period.</span></span> <span data-ttu-id="21a7d-154">重量将仅在进货仓库流程中捕获。</span><span class="sxs-lookup"><span data-stu-id="21a7d-154">The weight will be captured only during the inbound warehouse process.</span></span> <span data-ttu-id="21a7d-155">在出货流程中，将只扫描实际称重标记，与这些标记关联的重量将用于出货交易处理。</span><span class="sxs-lookup"><span data-stu-id="21a7d-155">During the outbound process, the catch weight tags will just be scanned, and the weights that are associated with the tags will be used for the outbound transactional processing.</span></span>

### <a name="how-to-capture-catch-weight"></a><span data-ttu-id="21a7d-156">如果捕获实际称重</span><span class="sxs-lookup"><span data-stu-id="21a7d-156">How to capture catch weight</span></span>

<span data-ttu-id="21a7d-157">在使用实际称重标记跟踪时，必须始终为收到的每个实际称重单位创建标记，并且每个标记必须始终与重量关联。</span><span class="sxs-lookup"><span data-stu-id="21a7d-157">When catch weight tag tracking is used, a tag must always be created for every catch weigh unit that is received, and every tag must always be associated with a weight.</span></span>

<span data-ttu-id="21a7d-158">例如，**箱**是实际称重单位，您将收到一个托盘（八箱）。</span><span class="sxs-lookup"><span data-stu-id="21a7d-158">For example, **Box** is the catch weight unit, and you receive one pallet of eight boxes.</span></span> <span data-ttu-id="21a7d-159">在这种情况下，必须创建八个唯一的实际称重标记，并且重量必须与每个标记关联。</span><span class="sxs-lookup"><span data-stu-id="21a7d-159">In this case, eight unique catch weight tags must be created, and a weight must be associated with each tag.</span></span> <span data-ttu-id="21a7d-160">根据进货实际称重标记，可以捕获全部八箱的重量，然后可以将平均重量分配到每箱，也可以为每箱捕获唯一重量。</span><span class="sxs-lookup"><span data-stu-id="21a7d-160">Depending on the inbound catch weight tag, either the weight of all eight boxes can be captured, and the average weight can then be distributed to each box, or a unique weight can be captured for each box.</span></span>

<span data-ttu-id="21a7d-161">在不使用实际称重标记跟踪时，可以针对每个维度集捕获重量（例如，对每个牌照和跟踪维度）。</span><span class="sxs-lookup"><span data-stu-id="21a7d-161">When catch weight tag tracking isn't used, the weight can be captured for each dimension set (for example, for each license plate and tracking dimension).</span></span> <span data-ttu-id="21a7d-162">或者，重量可以基于聚合级别捕获，如五个牌照（托盘）。</span><span class="sxs-lookup"><span data-stu-id="21a7d-162">Alternatively, the weight can be captured based on an aggregated level, such as five license plates (pallets).</span></span>

<span data-ttu-id="21a7d-163">对于捕获出货重量的方法，您可以定义是否为每个实际称重单位（即每箱）进行称重，或是否基于将要领取的数量（例如，三箱）捕获重量。</span><span class="sxs-lookup"><span data-stu-id="21a7d-163">For the methods for capturing outbound weight, you can define whether the weighing is done for each catch weight unit (that is, per box), or whether the weight is captured based on the quantity that will be picked (for example, three boxes).</span></span> <span data-ttu-id="21a7d-164">请注意，对于生产订单行领料流程，如果使用了**未捕获**选项，将使用平均重量。</span><span class="sxs-lookup"><span data-stu-id="21a7d-164">Note that for the production line picking process, the average weight will be used if the **Not captured** option is used.</span></span>

## <a name="supported-scenarios"></a><span data-ttu-id="21a7d-165">支持的方案</span><span class="sxs-lookup"><span data-stu-id="21a7d-165">Supported scenarios</span></span>

<span data-ttu-id="21a7d-166">并非所有工作流都支持使用仓库管理进行实际称重产品处理。</span><span class="sxs-lookup"><span data-stu-id="21a7d-166">Not all workflows support catch weight product processing with warehouse management.</span></span> <span data-ttu-id="21a7d-167">当前应用以下限制。</span><span class="sxs-lookup"><span data-stu-id="21a7d-167">The following restrictions currently apply.</span></span>
 
### <a name="configuring-catch-weight-products-for-warehouse-management-processes"></a><span data-ttu-id="21a7d-168">针对仓库管理流程配置实际称重产品</span><span class="sxs-lookup"><span data-stu-id="21a7d-168">Configuring catch weight products for warehouse management processes</span></span>

- <span data-ttu-id="21a7d-169">对于实际称重产品，物料的存储维度组不能更改（以便仓库管理流程可用于它们）。</span><span class="sxs-lookup"><span data-stu-id="21a7d-169">For catch weight products, the storage dimension group for items can't be changed (so that warehouse management processes can be used for them).</span></span>
- <span data-ttu-id="21a7d-170">实际称重产品（不是物料清单）仅支持配方处理。</span><span class="sxs-lookup"><span data-stu-id="21a7d-170">Only formula processing is supported for catch weight products (not bill of materials).</span></span>
- <span data-ttu-id="21a7d-171">实际称重产品不能使用所有者维度与跟踪维度组关联。</span><span class="sxs-lookup"><span data-stu-id="21a7d-171">Catch weight products can't be associated with a tracking dimension group by using the Owner dimension.</span></span>
- <span data-ttu-id="21a7d-172">实际称重产品不能作为服务使用。</span><span class="sxs-lookup"><span data-stu-id="21a7d-172">Catch weight products can't be used as services.</span></span>
- <span data-ttu-id="21a7d-173">实际称重产品只能作为物料模型组的一部分用作“贮存产品”。</span><span class="sxs-lookup"><span data-stu-id="21a7d-173">Catch weight products can be used as "stocked products" only as part the item model group.</span></span>
- <span data-ttu-id="21a7d-174">实际称重产品不能与此功能一起用于跟踪“在销售流程中有效”。</span><span class="sxs-lookup"><span data-stu-id="21a7d-174">Catch weight products can't be used together with the functionality for tracking "Active in sales process."</span></span>
- <span data-ttu-id="21a7d-175">实际称重产品不能与此功能一起用于捕获序列号。</span><span class="sxs-lookup"><span data-stu-id="21a7d-175">Catch weight products can't be used together with the functionality for capturing serial numbers.</span></span> <span data-ttu-id="21a7d-176">因此，产品不能作为领料/装箱流程的一部分从“空白”转为序列号。</span><span class="sxs-lookup"><span data-stu-id="21a7d-176">Therefore, products can't be transferred from a "blank" to a serial number as part of the picking/packing process.</span></span>
- <span data-ttu-id="21a7d-177">实际称重产品不能与此功能一起用于在消耗前登记序列。</span><span class="sxs-lookup"><span data-stu-id="21a7d-177">Catch weight products can't be used together with the functionality for registering serials before consumption.</span></span>
- <span data-ttu-id="21a7d-178">启用变量的实际称重产品不能与此功能一起用于转换不同的度量单位。</span><span class="sxs-lookup"><span data-stu-id="21a7d-178">Catch weight products that are variant-enabled can't be used together with the functionality for converting variant units of measure.</span></span>
- <span data-ttu-id="21a7d-179">实际称重产品不能标记为零售“产品配套件”。</span><span class="sxs-lookup"><span data-stu-id="21a7d-179">Catch weight products can't be marked as a retail "product kit."</span></span>
- <span data-ttu-id="21a7d-180">实际称重产品只能与具有实际称重处理单位且将实际称重单位作为最低序列的单位序列组一起使用。</span><span class="sxs-lookup"><span data-stu-id="21a7d-180">Catch weight products can be used only with a unit sequence group that has catch weight handling units, and that has the catch weight unit as the lowest sequence.</span></span>
- <span data-ttu-id="21a7d-181">对于实际称重产品，只有当转换生成大于 1 的标准数量时，库存单位才可以转换为实际称重单位。</span><span class="sxs-lookup"><span data-stu-id="21a7d-181">For catch weight products, the inventory unit can be converted to the catch weight unit only if the conversion produces a nominal quantity that is more than 1.</span></span>
- <span data-ttu-id="21a7d-182">实际称重产品的条码设置不支持可变重量设置。</span><span class="sxs-lookup"><span data-stu-id="21a7d-182">The setup of bar codes for catch weight products doesn't support a variable weight setup.</span></span>
 
### <a name="order-processing"></a><span data-ttu-id="21a7d-183">订单处理</span><span class="sxs-lookup"><span data-stu-id="21a7d-183">Order processing</span></span>

- <span data-ttu-id="21a7d-184">不支持内部公司订单处理。</span><span class="sxs-lookup"><span data-stu-id="21a7d-184">Intercompany order processing isn't supported.</span></span>
- <span data-ttu-id="21a7d-185">发货通知（ASN/装箱结构）的创建不支持重量信息。</span><span class="sxs-lookup"><span data-stu-id="21a7d-185">The creation of advance ship notice (ASN/packing structures) doesn't support weight information.</span></span>
- <span data-ttu-id="21a7d-186">订单数量必须基于实际称重单位维护。</span><span class="sxs-lookup"><span data-stu-id="21a7d-186">The order quantity must be maintained based on the catch weight unit.</span></span>
 
### <a name="inbound-warehouse-processing"></a><span data-ttu-id="21a7d-187">进货仓库处理</span><span class="sxs-lookup"><span data-stu-id="21a7d-187">Inbound warehouse processing</span></span>

- <span data-ttu-id="21a7d-188">接收牌照需要重量在登记时分配，因为重量信息不支持作为发货通知的一部分。</span><span class="sxs-lookup"><span data-stu-id="21a7d-188">Receiving license plates requires that weights be assigned during registration, because weight information isn't supported as part of the advance ship notice.</span></span> <span data-ttu-id="21a7d-189">在使用实际称重标记流程时，标记编号必须按实际称重单位手动分配。</span><span class="sxs-lookup"><span data-stu-id="21a7d-189">When catch weight tag processes are used, the tag number must be manually assigned per catch weight unit.</span></span>
- <span data-ttu-id="21a7d-190">实际称重产品不支持接收混合牌照。</span><span class="sxs-lookup"><span data-stu-id="21a7d-190">Receiving mixed license plates isn't supports for catch weight products.</span></span>
 
### <a name="inventory-and-warehouse-operations"></a><span data-ttu-id="21a7d-191">库存和仓库操作</span><span class="sxs-lookup"><span data-stu-id="21a7d-191">Inventory and warehouse operations</span></span>

- <span data-ttu-id="21a7d-192">实际称重产品不支持手动创建检验单。</span><span class="sxs-lookup"><span data-stu-id="21a7d-192">Manual creation of quarantine orders isn't supported for catch weight products.</span></span>
- <span data-ttu-id="21a7d-193">实际称重产品不支持手动移动与工作相关的库存。</span><span class="sxs-lookup"><span data-stu-id="21a7d-193">Manual movement of inventory that is related to work isn't supported for catch weight products.</span></span>
- <span data-ttu-id="21a7d-194">实际称重产品不支持合并牌照。</span><span class="sxs-lookup"><span data-stu-id="21a7d-194">Consolidation of license plates isn't supported for catch weight products.</span></span>
- <span data-ttu-id="21a7d-195">实际称重产品不支持作为定期任务的一部分更改仓库库存状态。</span><span class="sxs-lookup"><span data-stu-id="21a7d-195">Changes to warehouse inventory status as part of a periodic task aren't supported for catch weight products.</span></span>
- <span data-ttu-id="21a7d-196">实际称重产品不支持对查询定义的库存状态进行更改。</span><span class="sxs-lookup"><span data-stu-id="21a7d-196">Changes to inventory status that are defined by a query aren't supported for catch weight products.</span></span> <span data-ttu-id="21a7d-197">（也不支持更改质检订单库存状态。）</span><span class="sxs-lookup"><span data-stu-id="21a7d-197">(Changes to quality order inventory status aren't supported either.)</span></span>
- <span data-ttu-id="21a7d-198">对于实际称重产品，不能从**按库位显示的现有量**页更改库存状态。</span><span class="sxs-lookup"><span data-stu-id="21a7d-198">For catch weight products, the inventory status can't be changed from the **On-hand by location** page.</span></span>
- <span data-ttu-id="21a7d-199">对于实际称重产品，不能作为仓库应用移动工作的一部分更改库存状态。</span><span class="sxs-lookup"><span data-stu-id="21a7d-199">For catch weight products, the inventory status can't be changed as part of warehouse app movement work.</span></span>
- <span data-ttu-id="21a7d-200">实际称重产品不支持加载来初始化仓库库存的牌照。</span><span class="sxs-lookup"><span data-stu-id="21a7d-200">License plate loading to initialize warehouse stock isn't supported for catch weight products.</span></span>
- <span data-ttu-id="21a7d-201">实际称重产品不支持批次平衡流程。</span><span class="sxs-lookup"><span data-stu-id="21a7d-201">Batch balancing processes aren't supported for catch weight products.</span></span>
- <span data-ttu-id="21a7d-202">实际称重产品不支持处理负实际库存。</span><span class="sxs-lookup"><span data-stu-id="21a7d-202">Handling of negative physical inventory isn't supported for catch weight products.</span></span>
- <span data-ttu-id="21a7d-203">库存标记不能用于实际称重产品。</span><span class="sxs-lookup"><span data-stu-id="21a7d-203">Inventory marking can't be used for catch weight products.</span></span>
 
### <a name="outbound-warehouse-processing"></a><span data-ttu-id="21a7d-204">出货仓库处理</span><span class="sxs-lookup"><span data-stu-id="21a7d-204">Outbound warehouse processing</span></span>

- <span data-ttu-id="21a7d-205">实际称重产品不支持群集领料功能。</span><span class="sxs-lookup"><span data-stu-id="21a7d-205">The functionality for cluster picking isn't supported for catch weight products.</span></span>
- <span data-ttu-id="21a7d-206">实际称重产品不支持领料和装箱仓库处理。</span><span class="sxs-lookup"><span data-stu-id="21a7d-206">Pick and pack warehouse processing isn't supported for catch weight products.</span></span>
- <span data-ttu-id="21a7d-207">对于实际称重产品，工作不能从**工作**页完成。</span><span class="sxs-lookup"><span data-stu-id="21a7d-207">For catch weight products, work can't be completed from the **Work** page.</span></span>
- <span data-ttu-id="21a7d-208">对于实际称重产品，在工作模板中定义的工作可以自动运行。</span><span class="sxs-lookup"><span data-stu-id="21a7d-208">For catch weight products, work that is defined in a work template can be run automatically.</span></span>
- <span data-ttu-id="21a7d-209">实际称重产品不支持冲销工作功能。</span><span class="sxs-lookup"><span data-stu-id="21a7d-209">The functionality for reversing work isn't supported for catch weight products.</span></span>
- <span data-ttu-id="21a7d-210">对于实际称重产品，不支持在集装箱关闭后创建工作的手动装箱工作站处理。</span><span class="sxs-lookup"><span data-stu-id="21a7d-210">For catch weight products, manual packing station processing where work is created after containers are closed isn't supported.</span></span>
- <span data-ttu-id="21a7d-211">实际称重产品不支持逐件扫描功能。</span><span class="sxs-lookup"><span data-stu-id="21a7d-211">The functionality for pcs-by-pcs scanning isn't supported for catch weight products.</span></span>
 
### <a name="production-processing"></a><span data-ttu-id="21a7d-212">生产处理</span><span class="sxs-lookup"><span data-stu-id="21a7d-212">Production processing</span></span>

- <span data-ttu-id="21a7d-213">对于实际称重产品，仅支持配方产品的批次订单。</span><span class="sxs-lookup"><span data-stu-id="21a7d-213">For catch weight products, only batch orders for formula products are supported.</span></span>
- <span data-ttu-id="21a7d-214">实际称重产品不支持看板功能。</span><span class="sxs-lookup"><span data-stu-id="21a7d-214">Kanban functionality isn't supported for catch weight products.</span></span>
- <span data-ttu-id="21a7d-215">对于实际称重产品，序列号不能在消耗前登记。</span><span class="sxs-lookup"><span data-stu-id="21a7d-215">For catch weight products, serial numbers can't be registered before consumption.</span></span>
- <span data-ttu-id="21a7d-216">实际称重产品不支持冲销牌照功能。</span><span class="sxs-lookup"><span data-stu-id="21a7d-216">The functionality for reversing license plates isn't supported for catch weight products.</span></span>
- <span data-ttu-id="21a7d-217">对于实际称重产品，完工入库可通过序列号注册。</span><span class="sxs-lookup"><span data-stu-id="21a7d-217">For catch weight products, reporting as finished can be registered by serial number.</span></span>

### <a name="transportation-management-processing"></a><span data-ttu-id="21a7d-218">运输管理处理</span><span class="sxs-lookup"><span data-stu-id="21a7d-218">Transportation management processing</span></span>

- <span data-ttu-id="21a7d-219">实际称重产品不支持装载计划工作台处理。</span><span class="sxs-lookup"><span data-stu-id="21a7d-219">Load building workbench processing isn't supported for catch weight products.</span></span>
- <span data-ttu-id="21a7d-220">实际称重产品不支持运输请求行。</span><span class="sxs-lookup"><span data-stu-id="21a7d-220">Transport request lines aren't supported for catch weight products.</span></span>
 
### <a name="other-restrictions-and-behaviors-for-catch-weight-product-processing-with-warehouse-management"></a><span data-ttu-id="21a7d-221">使用仓库管理的实际称重产品处理的其他限制和行为</span><span class="sxs-lookup"><span data-stu-id="21a7d-221">Other restrictions and behaviors for catch weight product processing with warehouse management</span></span>

- <span data-ttu-id="21a7d-222">在实际称重标记作为仓库应用处理的一部分捕获时，用户不能在工作流外取消。</span><span class="sxs-lookup"><span data-stu-id="21a7d-222">When catch weight tags are captured as part of warehouse app processing, the user can't cancel out of the workflow.</span></span>
- <span data-ttu-id="21a7d-223">在没有提示用户标识跟踪维度的领料流程中，重量分配基于平均重量进行。</span><span class="sxs-lookup"><span data-stu-id="21a7d-223">During picking processes where the user isn't prompted to identify tracking dimensions, the weight assignment is done based on the average weight.</span></span> <span data-ttu-id="21a7d-224">例如，此行为在以下情况下发生：在同一位置使用跟踪维度组合，并且在用户处理领料后，该位置只剩一个跟踪维度值。</span><span class="sxs-lookup"><span data-stu-id="21a7d-224">This behavior occurs when, for example, a combination of tracking dimensions is used in the same location and, after a user processes picking, only one tracking dimension value is left in the location.</span></span>
- <span data-ttu-id="21a7d-225">在库存为针对仓库管理流程配置的实际称重产品预留时，预留将基于定义的最小重量进行，即使此数量是现有的最后一个处理数量。</span><span class="sxs-lookup"><span data-stu-id="21a7d-225">When inventory is reserved for a catch weight product that is configured for warehouse management processes, the reservation is done based on the minimum weight that is defined, even if this quantity is the on-hand last handling quantity.</span></span> <span data-ttu-id="21a7d-226">此行为与未为仓库管理流程配置的物料的行为不同。</span><span class="sxs-lookup"><span data-stu-id="21a7d-226">This behavior differs from the behavior for items that aren't configured for warehouse management processes.</span></span>
- <span data-ttu-id="21a7d-227">将重量作为产能计算（波次阈值、工作最大休息时间、集装箱最大数、库位负荷产能等）的一部分使用的流程不使用库存的实际重量。</span><span class="sxs-lookup"><span data-stu-id="21a7d-227">Processes that use the weight as part of capacity calculations (wave thresholds, work maximum breaks, container maximums, location load capacities, and so on) don't use the actual weight of the inventory.</span></span> <span data-ttu-id="21a7d-228">流程基于为产品定义的实际处理重量。</span><span class="sxs-lookup"><span data-stu-id="21a7d-228">Instead, the processes are based on the physical handling weight that is defined for the product.</span></span>
- <span data-ttu-id="21a7d-229">通常，实际称重产品不支持零售功能。</span><span class="sxs-lookup"><span data-stu-id="21a7d-229">In general, Retail functionality isn't supported for catch weight products.</span></span>
 
### <a name="catch-weight-tags"></a><span data-ttu-id="21a7d-230">实际称重标记</span><span class="sxs-lookup"><span data-stu-id="21a7d-230">Catch weight tags</span></span>

<span data-ttu-id="21a7d-231">目前，实际称重标记的功能仅作为以下方案的一部分支持：</span><span class="sxs-lookup"><span data-stu-id="21a7d-231">Currently, the functionality for catch weight tags is supported only as part of the following scenarios:</span></span>

- <span data-ttu-id="21a7d-232">当处理采购订单仓库应用接收时。</span><span class="sxs-lookup"><span data-stu-id="21a7d-232">When processing purchase order warehouse app receiving.</span></span>
- <span data-ttu-id="21a7d-233">当通过仓库应用处理负荷接收时。</span><span class="sxs-lookup"><span data-stu-id="21a7d-233">When processing load receiving via warehouse app.</span></span>
- <span data-ttu-id="21a7d-234">对于与采购订单负荷相关的牌照接收，重量分配在接收流程中请求。</span><span class="sxs-lookup"><span data-stu-id="21a7d-234">For license plate receiving that is related to a purchase order load, weight assignment is requested during the receiving process.</span></span> <span data-ttu-id="21a7d-235">相对而言，对于转移单接收，将使用转移单的装运数据中的重量。</span><span class="sxs-lookup"><span data-stu-id="21a7d-235">By contrast, for transfer order receiving, the weight from the shipment data for the transfer order is used.</span></span>
- <span data-ttu-id="21a7d-236">对于来自非仓库管理流程仓库的转移单物料和行接收。</span><span class="sxs-lookup"><span data-stu-id="21a7d-236">For transfer order item and line receiving that comes from a non-warehouse management process warehouse.</span></span>
- <span data-ttu-id="21a7d-237">销售退货单接收的处理可以记录实际称重标记，但如果标记是最初为特定销售订单行装运的相同标记，则不会验证处理。</span><span class="sxs-lookup"><span data-stu-id="21a7d-237">The processing of sales return order receiving can record catch weight tags, but the processing won't be validated if the tags are the same tags that were originally shipped for a particular sales order line.</span></span>
- <span data-ttu-id="21a7d-238">在使用仓库应用处理更改的库存状态时。</span><span class="sxs-lookup"><span data-stu-id="21a7d-238">When processing a inventory status changed by using the warehouse app.</span></span>
- <span data-ttu-id="21a7d-239">在使用仓库应用完成仓库转移时。</span><span class="sxs-lookup"><span data-stu-id="21a7d-239">When a warehouse transfer is done by using the warehouse app.</span></span>
- <span data-ttu-id="21a7d-240">在通过仓库应用处理调入和调出时。</span><span class="sxs-lookup"><span data-stu-id="21a7d-240">When processing adjustment in and out via the warehouse app.</span></span>
- <span data-ttu-id="21a7d-241">在为销售订单和转移单处理领料工作时。</span><span class="sxs-lookup"><span data-stu-id="21a7d-241">When picking work is processed for sales and transfer orders.</span></span> <span data-ttu-id="21a7d-242">（请注意，实际称重标记不能为生产组件领料记录。）</span><span class="sxs-lookup"><span data-stu-id="21a7d-242">(Note that catch weight tags can't be recorded for production component picking.)</span></span>
- <span data-ttu-id="21a7d-243">在减少负荷行的领料数量时（不管是否使用集装箱）。</span><span class="sxs-lookup"><span data-stu-id="21a7d-243">When picked quantities are reduced from load lines, regardless of whether containers are used.</span></span>
- <span data-ttu-id="21a7d-244">当产品在装箱工作站装入集装箱时。</span><span class="sxs-lookup"><span data-stu-id="21a7d-244">When products are packed into containers at a packing station.</span></span>
- <span data-ttu-id="21a7d-245">在重新打开集装箱时。</span><span class="sxs-lookup"><span data-stu-id="21a7d-245">When containers are reopened.</span></span>
- <span data-ttu-id="21a7d-246">当配方产品使用仓库应用完工入库时。</span><span class="sxs-lookup"><span data-stu-id="21a7d-246">When formula products are reported as finished by using the warehouse app.</span></span>
- <span data-ttu-id="21a7d-247">在使用仓库应用处理运输负荷时。</span><span class="sxs-lookup"><span data-stu-id="21a7d-247">When transport loads are processed by using the warehouse app.</span></span>
