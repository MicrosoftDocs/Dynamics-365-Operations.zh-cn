---
title: 灵活的仓库级维度预留策略
description: 本主题介绍一种库存预留策略，其允许销售批量跟踪产品并且以启用 WMS 的操作运行物流的企业为客户销售订单预留特定批次，即使与产品相关联的预留层次结构不允许预留特定批次。
author: perlynne
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSReservationHierarchy, WHSWorkTrans, WHSWorkInventTrans, WHSInventTableReservationHierarchy, WHSReservationHierarchyCreate, WHSInventTableReservationHierarchy
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-01-15
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 17ae3cc788c60917807acece2fc21f6c52d8ffe0
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5835670"
---
# <a name="flexible-warehouse-level-dimension-reservation-policy"></a><span data-ttu-id="84ca9-103">灵活的仓库级维度预留策略</span><span class="sxs-lookup"><span data-stu-id="84ca9-103">Flexible warehouse-level dimension reservation policy</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="84ca9-104">当 *Batch-below\[location\]* 类型的库存预留层次结构与产品关联时，销售批次跟踪产品并以启用 Microsoft Dynamics 365 仓库管理系统 (WMS) 的操作运行物流的企业不能为客户销售订单预留这些产品的特定批次。</span><span class="sxs-lookup"><span data-stu-id="84ca9-104">When an inventory reservation hierarchy of the *Batch-below\[location\]* type is associated with products, businesses that sell batch-tracked products and run their logistics as operations that are enabled for the Microsoft Dynamics 365 Warehouse Management System (WMS) can't reserve specific batches of those products for customer sales orders.</span></span>

<span data-ttu-id="84ca9-105">以类似的方式，当销售订单上的产品与默认预留层次结构关联时，不能为这些产品预留特定牌照。</span><span class="sxs-lookup"><span data-stu-id="84ca9-105">In a similar way, specific license plates can't be reserved for products on sales orders when those products are associated with the default reservation hierarchy.</span></span>

<span data-ttu-id="84ca9-106">本主题介绍一种库存预留策略，能够让这些企业预留特定批次或牌照，即使产品与 *Batch-below\[location\]* 预留层次结构关联。</span><span class="sxs-lookup"><span data-stu-id="84ca9-106">This topic describes the inventory reservation policy that lets these businesses reserve specific batches or license plates, even when the products are associated with a *Batch-below\[location\]* reservation hierarchy.</span></span>

## <a name="inventory-reservation-hierarchy"></a><span data-ttu-id="84ca9-107">库存预留层次结构</span><span class="sxs-lookup"><span data-stu-id="84ca9-107">Inventory reservation hierarchy</span></span>

<span data-ttu-id="84ca9-108">本节总结了现有的库存预留层次结构。</span><span class="sxs-lookup"><span data-stu-id="84ca9-108">This section summarizes the existing inventory reservation hierarchy.</span></span>

<span data-ttu-id="84ca9-109">库存预留层次结构指示，就存储维度而言，需求订单包含站点、仓库和库存状态的必需维度。</span><span class="sxs-lookup"><span data-stu-id="84ca9-109">The inventory reservation hierarchy dictates that, as far as storage dimensions are concerned, the demand order carries the mandatory dimensions of site, warehouse, and inventory status.</span></span> <span data-ttu-id="84ca9-110">换句话说，必需维度是预留层次结构中位于库位维度之上的所有维度，而仓库逻辑负责为请求的数量分配库位并预留库位。</span><span class="sxs-lookup"><span data-stu-id="84ca9-110">In other words, the mandatory dimensions are all the dimensions above the location dimension in the reservation hierarchy, while the warehouse logic is responsible for assigning a location to the requested quantities and reserving the location.</span></span> <span data-ttu-id="84ca9-111">在需求订单和仓库操作之间的交互中，需求订单应指示必须从何处装运（即哪个站点和仓库）。</span><span class="sxs-lookup"><span data-stu-id="84ca9-111">In the interactions between the demand order and the warehouse operations, the demand order is expected to indicate where the order must be shipped from (that is, what site and warehouse).</span></span> <span data-ttu-id="84ca9-112">然后，仓库依靠其逻辑在仓库货位查找所需的数量。</span><span class="sxs-lookup"><span data-stu-id="84ca9-112">The warehouse then relies on its logic to find the required quantity in the warehouse premises.</span></span>

<span data-ttu-id="84ca9-113">但是，为了反映业务的运营模型，跟踪维度（批号和序列号）需要具有更大的灵活性。</span><span class="sxs-lookup"><span data-stu-id="84ca9-113">However, to reflect the operational model of the business, tracking dimensions (batch and serial numbers) are subject to more flexibility.</span></span> <span data-ttu-id="84ca9-114">库存预留层次结构可以应对适用以下条件的场景：</span><span class="sxs-lookup"><span data-stu-id="84ca9-114">An inventory reservation hierarchy can accommodate scenarios where the following conditions apply:</span></span>

- <span data-ttu-id="84ca9-115">企业依靠其仓库操作来管理在仓库存储空间中找到具有批号或序列号的数量 *后*，领取这些数量。</span><span class="sxs-lookup"><span data-stu-id="84ca9-115">The business relies on its warehouse operations to manage picking of quantities that have batch or serial numbers *after* the quantities have been found in the warehousing storage space.</span></span> <span data-ttu-id="84ca9-116">此模型通常称为 *Batch-below\[location\]* 或 *Serial-below\[location\]*。</span><span class="sxs-lookup"><span data-stu-id="84ca9-116">This model is often referred to as *Batch-below\[location\]* or *Serial-below\[location\]*.</span></span> <span data-ttu-id="84ca9-117">它通常在产品的批号或序列号标识对向销售公司提出需求的客户不重要时使用。</span><span class="sxs-lookup"><span data-stu-id="84ca9-117">It's typically used when a product's batch or serial number identification isn't important to the customers who place the demand with the selling company.</span></span>
- <span data-ttu-id="84ca9-118">企业依靠其仓库操作来管理在仓库存储空间中找到具有批号或序列号的数量 *之前*，领取这些数量。</span><span class="sxs-lookup"><span data-stu-id="84ca9-118">The business relies on its warehouse operations to manage picking of quantities that have batch or serial numbers *before* the quantities have been found in the warehousing storage space.</span></span> <span data-ttu-id="84ca9-119">如果批号或序列号是客户订单说明的必要部分，并且记录在需求订单中，则在仓库中查找数量的仓库操作将不允许对其进行更改。</span><span class="sxs-lookup"><span data-stu-id="84ca9-119">If batch or serial numbers are necessary as part of a customer's order specification, they are recorded on the demand order, and the warehouse operations that find the quantities in the warehouse aren't allowed to change them.</span></span> <span data-ttu-id="84ca9-120">此模型称为 *Batch-above\[location\]* 或 *Serial-above\[location\]*。</span><span class="sxs-lookup"><span data-stu-id="84ca9-120">This model is referred to as *Batch-above\[location\]* or *Serial-above\[location\]*.</span></span> <span data-ttu-id="84ca9-121">由于库位之上的维度是必须满足的需求的特定要求，因此仓库逻辑不会分配它们。</span><span class="sxs-lookup"><span data-stu-id="84ca9-121">Because the dimensions above location are the specific requirements for the demands that must be fulfilled, the warehouse logic won't allocate them.</span></span> <span data-ttu-id="84ca9-122">**必须** 始终在需求订单上或在相关预留中指定这些维度。</span><span class="sxs-lookup"><span data-stu-id="84ca9-122">These dimensions **must** always be specified on the demand order or in the related reservations.</span></span>

<span data-ttu-id="84ca9-123">在这些场景中，挑战在于，只能为每个已发布的产品分配一个库存预留层次结构。</span><span class="sxs-lookup"><span data-stu-id="84ca9-123">In these scenarios, the challenge is that only one inventory reservation hierarchy can be assigned to each released product.</span></span> <span data-ttu-id="84ca9-124">因此，为使 WMS 处理跟踪物料，在层次结构分配确定应预留批号或序列号的时间之后（在接到需求订单时或在仓库领料工作期间），此时间不能作为特例更改。</span><span class="sxs-lookup"><span data-stu-id="84ca9-124">Therefore, for the WMS to handle tracked items, after the hierarchy assignment determines when the batch or serial number should be reserved (either when the demand order is taken or during the warehouse picking work), this timing can't be changed on an ad-hoc basis.</span></span>

## <a name="flexible-reservation-for-batch-tracked-items"></a><span data-ttu-id="84ca9-125">灵活地预留批次跟踪物料</span><span class="sxs-lookup"><span data-stu-id="84ca9-125">Flexible reservation for batch-tracked items</span></span>

### <a name="business-scenario"></a><span data-ttu-id="84ca9-126">业务方案</span><span class="sxs-lookup"><span data-stu-id="84ca9-126">Business scenario</span></span>

<span data-ttu-id="84ca9-127">在此场景中，公司使用按批号跟踪成品的库存策略。</span><span class="sxs-lookup"><span data-stu-id="84ca9-127">In this scenario, a company uses an inventory strategy where finished goods are tracked by batch numbers.</span></span> <span data-ttu-id="84ca9-128">该公司还使用 WMS 工作负载。</span><span class="sxs-lookup"><span data-stu-id="84ca9-128">This company also uses the WMS workload.</span></span> <span data-ttu-id="84ca9-129">因为此工作负荷具有用于计划和运行已启用批次的物料的仓库领料和装运操作的设备完善的逻辑，所以大多数成品物料都与 *Batch-below\[location\]* 库存预留层次结构相关联。</span><span class="sxs-lookup"><span data-stu-id="84ca9-129">Because this workload has well-equipped logic for planning and running warehouse picking and shipping operations for batch-enabled items, most of the finished items are associated with a *Batch-below\[location\]* inventory reservation hierarchy.</span></span> <span data-ttu-id="84ca9-130">这种类型的运营设置的优点在于，关于领取哪些批次以及将其放入仓库中哪个位置的决定（即有效的预留决定）被推迟到仓库领料操作开始时。</span><span class="sxs-lookup"><span data-stu-id="84ca9-130">The advantage of this type of operational setup is that decisions (which are effectively reservation decisions) about which batches to pick and where to put them in the warehouse are postponed until the warehouse picking operations start.</span></span> <span data-ttu-id="84ca9-131">而不会在客户下订单时作出。</span><span class="sxs-lookup"><span data-stu-id="84ca9-131">They aren't made when the customer's order is placed.</span></span>

<span data-ttu-id="84ca9-132">虽然 *Batch-below\[location\]* 预留层次结构很好地满足了公司的业务目标，但公司的许多老客户在重新订购产品时需要的都是以前购买的相同批次。</span><span class="sxs-lookup"><span data-stu-id="84ca9-132">Although the *Batch-below\[location\]* reservation hierarchy serves the company's business goals well, many of the company's established customers require the same batch that they previously purchased when they reorder products.</span></span> <span data-ttu-id="84ca9-133">因此，该公司正在寻求一种灵活的方式来处理批次预留规则，以便能够根据客户对同一物料的需求，执行以下行为：</span><span class="sxs-lookup"><span data-stu-id="84ca9-133">Therefore, the company is looking for flexibility in the way that the batch reservation rules are handled, so that, depending on the customers' demand for the same item, the following behaviors occur:</span></span>

- <span data-ttu-id="84ca9-134">当销售管理员接收订单时，可以记录并保留批号，并且批号在仓库操作期间不能更改和/或被其他需求获取。</span><span class="sxs-lookup"><span data-stu-id="84ca9-134">A batch number can be recorded and reserved when the order is taken by the sales processor, and it can't be changed during warehouse operations and/or taken by other demands.</span></span> <span data-ttu-id="84ca9-135">此行为有助于确保将订购的批号运送到客户。</span><span class="sxs-lookup"><span data-stu-id="84ca9-135">This behavior helps guarantee that the batch number that was ordered is shipped to the customer.</span></span>
- <span data-ttu-id="84ca9-136">如果批号对客户不重要，则在完成销售订单登记和预留后，仓库操作可以在领料工作期间确定批号。</span><span class="sxs-lookup"><span data-stu-id="84ca9-136">If the batch number isn't important to the customer, the warehouse operations can determine a batch number during picking work, after sales order registration and reservation have been done.</span></span>

### <a name="allowing-reservation-of-a-specific-batch-on-the-sales-order"></a><span data-ttu-id="84ca9-137">允许在销售订单上保留特定批次</span><span class="sxs-lookup"><span data-stu-id="84ca9-137">Allowing reservation of a specific batch on the sales order</span></span>

<span data-ttu-id="84ca9-138">为了适应与 *Batch-below\[location\]* 库存预留层次结构相关联的物料的批次预留行为的灵活性，库存管理员必须在 **库存预留层次结构** 页面上为 **批号** 级别选中 **允许在需求订单上预留** 复选框。</span><span class="sxs-lookup"><span data-stu-id="84ca9-138">To accommodate the desired flexibility in the batch reservation behavior for items that are associated with a *Batch-below\[location\]* inventory reservation hierarchy, inventory managers must select the **Allow reservation on demand order** check box for the **Batch number** level on the **Inventory reservation hierarchies** page.</span></span>

![使库存预留层次结构更灵活](media/Flexible-inventory-reservation-hierarchy.png)

<span data-ttu-id="84ca9-140">当在层次结构中选择了 **批号** 级别时，从该级别开始直至 **货位** 级别的所有维度都将被自动选择。</span><span class="sxs-lookup"><span data-stu-id="84ca9-140">When the **Batch number** level in the hierarchy is selected, all dimensions above that level and up through the **Location** level will be automatically selected.</span></span> <span data-ttu-id="84ca9-141">（默认情况下，会预先选择 **货位** 级别以上的所有维度。）此行为反映了这样的逻辑：在订单行上预留特定批号后，批号和货位之间的范围内的所有维度也会自动预留。</span><span class="sxs-lookup"><span data-stu-id="84ca9-141">(By default, all dimensions above the **Location** level are preselected.) This behavior reflects the logic where all dimensions in the range between the batch number and location are also automatically reserved after you reserve a specific batch number on the order line.</span></span>

> [!NOTE]
> <span data-ttu-id="84ca9-142">**允许在需求订单上预留** 复选框仅适用于仓库货位维度以下的预留层次结构级别。</span><span class="sxs-lookup"><span data-stu-id="84ca9-142">The **Allow reservation on demand order** check box applies only to reservation hierarchy levels that are below the warehouse location dimension.</span></span>
>
> <span data-ttu-id="84ca9-143">**批号** 和 **牌照** 是层次结构中唯一为灵活预留策略开放的级别。</span><span class="sxs-lookup"><span data-stu-id="84ca9-143">**Batch number** and **License plate** are the only levels in the hierarchy that are open for the flexible reservation policy.</span></span> <span data-ttu-id="84ca9-144">换言之，您无法为 **位置** 或 **序列号** 级别选择 **允许在需求订单上预留** 复选框。</span><span class="sxs-lookup"><span data-stu-id="84ca9-144">In other words, you can't select the **Allow reservation on demand order** check box for the **Location** or **Serial number** level.</span></span>
>
> <span data-ttu-id="84ca9-145">如果您的预留层次结构包含序列号维度（必须始终在 **批号** 级别以下），并且您已为批号打开了特定于批次的预留，系统将根据应用于 *Serial-below\[location\]* 预留策略的规则，继续处理序列号预留和领料操作。</span><span class="sxs-lookup"><span data-stu-id="84ca9-145">If your reservation hierarchy includes the serial number dimension (which must always be below the **Batch number** level), and if you've turned on batch-specific reservation for the batch number, the system will continue to handle serial number reservation and picking operations, based on the rules that apply to the *Serial-below\[location\]* reservation policy.</span></span>

<span data-ttu-id="84ca9-146">任何时候，您都可以允许为部署中现有的 *Batch-below\[location\]* 预留层次结构进行特定于批次的预留。</span><span class="sxs-lookup"><span data-stu-id="84ca9-146">At any point, you can allow batch-specific reservation for an existing *Batch-below\[location\]* reservation hierarchy in your deployment.</span></span> <span data-ttu-id="84ca9-147">此更改不会影响更改发生之前创建的任何预留和开放仓库工作。</span><span class="sxs-lookup"><span data-stu-id="84ca9-147">This change won't affect any reservations and open warehouse work that were created before the change occurred.</span></span> <span data-ttu-id="84ca9-148">但是，如果与该预留层次结构关联的一个或多个物料存在问题类型为 **订购预留**、**实际预留** 或 **已订购** 的库存交易记录，则不能清除 **允许在需求订单上预留** 复选框。</span><span class="sxs-lookup"><span data-stu-id="84ca9-148">However, the **Allow reservation on demand order** check box can't be cleared if inventory transactions of the **Reserved ordered**, **Reserved physical**, or **Ordered** issue type exist for one or more items that are associated with that reservation hierarchy.</span></span>

> [!NOTE]
> <span data-ttu-id="84ca9-149">如果物料的现有预留层次结构不允许订单上有批次说明，您可以将其重新分配到允许批次说明的预留层次结构，前提是两个层次结构的层次结构级别结构均相同。</span><span class="sxs-lookup"><span data-stu-id="84ca9-149">If an item's existing reservation hierarchy doesn't allow batch specification on the order, you can reassign it to a reservation hierarchy that does allow batch specification, provided that the hierarchy level structure is the same in both hierarchies.</span></span> <span data-ttu-id="84ca9-150">使用 **更改物料的预留层次结构** 功能来进行重新分配。</span><span class="sxs-lookup"><span data-stu-id="84ca9-150">Use the **Change reservation hierarchy for items** function to do the reassignment.</span></span> <span data-ttu-id="84ca9-151">当您要阻止为批次跟踪物料的其中一部分进行灵活的批次预留，但允许对其余的产品组合执行时，此更改可能很有用。</span><span class="sxs-lookup"><span data-stu-id="84ca9-151">This change might be relevant when you want to prevent flexible batch reservation for a subset of batch-tracked items but allow it for the rest of the product portfolio.</span></span>

<span data-ttu-id="84ca9-152">无论您是否选择了 **允许在需求订单上预留** 复选框，如果您不想为订单行上的物料预留特定的批号，仍会应用对 *Batch-below\[location\]* 预留层次结构有效的默认仓库操作逻辑。</span><span class="sxs-lookup"><span data-stu-id="84ca9-152">Regardless of whether you've selected the **Allow reservation on demand order** check box, if you don't want to reserve a specific batch number for the item on an order line, default warehouse operations logic that is valid for a *Batch-below\[location\]* reservation hierarchy will still apply.</span></span>

### <a name="reserve-a-specific-batch-number-for-a-customer-order"></a><span data-ttu-id="84ca9-153">为客户订单预留特定批号</span><span class="sxs-lookup"><span data-stu-id="84ca9-153">Reserve a specific batch number for a customer order</span></span>

<span data-ttu-id="84ca9-154">在批次跟踪物料的 *Batch-below\[location\]* 库存预留层次结构设置为允许在销售订单上预留特定批号后，销售订单处理人员可以根据客户的请求，通过以下其中一种方式获取同一物料的客户订单：</span><span class="sxs-lookup"><span data-stu-id="84ca9-154">After a batch-tracked item's *Batch-below\[location\]* inventory reservation hierarchy is set up to allow reservation of specific batch numbers on sales orders, sales order processors can take customer orders for the same item in one of the following ways, depending on the customer's request:</span></span>

- <span data-ttu-id="84ca9-155">**输入订单详细信息但不指定批号** – 当产品的批次说明对客户不重要时，应使用此方法。</span><span class="sxs-lookup"><span data-stu-id="84ca9-155">**Enter order details without specifying a batch number** – This approach should be used when the product's batch specification isn't important to the customer.</span></span> <span data-ttu-id="84ca9-156">与处理系统中这种类型的订单相关联的所有现有流程均保持不变。</span><span class="sxs-lookup"><span data-stu-id="84ca9-156">All existing processes that are associated with handling an order of this type in the system remain unchanged.</span></span> <span data-ttu-id="84ca9-157">不需要对这部分用户作任何其他考虑。</span><span class="sxs-lookup"><span data-stu-id="84ca9-157">No additional considerations are required on the part of users.</span></span>
- <span data-ttu-id="84ca9-158">**输入订单详细信息并保留特定批号** – 当客户请求特定批次时，应使用此方法。</span><span class="sxs-lookup"><span data-stu-id="84ca9-158">**Enter order details and reserve a specific batch number** – This approach should be used when the customer requests a specific batch.</span></span> <span data-ttu-id="84ca9-159">通常，客户在重新订购之前购买的产品时会请求特定批次。</span><span class="sxs-lookup"><span data-stu-id="84ca9-159">Typically, customers will request a specific batch when they are reordering a product that they previously purchased.</span></span> <span data-ttu-id="84ca9-160">这种类型的批次特定预留称为 *订单承诺预留*。</span><span class="sxs-lookup"><span data-stu-id="84ca9-160">This type of batch-specific reservation is referred to as *order-committed reservation*.</span></span>

<span data-ttu-id="84ca9-161">当数量被处理并将批号提交到特定订单时，以下这组规则有效：</span><span class="sxs-lookup"><span data-stu-id="84ca9-161">The following set of rules is valid when quantities are processed, and a batch number is committed to a specific order:</span></span>

- <span data-ttu-id="84ca9-162">为了允许根据 *Batch-below\[location\]* 预留策略为物料预留特定批号，系统必须预留整个库位的所有维度。</span><span class="sxs-lookup"><span data-stu-id="84ca9-162">To allow reservation of a specific batch number for an item under the *Batch-below\[location\]* reservation policy, the system must reserve all dimensions up through location.</span></span> <span data-ttu-id="84ca9-163">这个范围通常包括牌照维度。</span><span class="sxs-lookup"><span data-stu-id="84ca9-163">This range typically includes the license plate dimension.</span></span>
- <span data-ttu-id="84ca9-164">在为使用订单承诺批次预留的销售订单行创建领料工作时，不使用货位指令。</span><span class="sxs-lookup"><span data-stu-id="84ca9-164">Location directives aren't used when picking work is created for a sales line that uses order-committed batch reservation.</span></span>
- <span data-ttu-id="84ca9-165">在订单承诺批次的仓库处理工作期间，用户和系统都不允许更改批号。</span><span class="sxs-lookup"><span data-stu-id="84ca9-165">During warehouse processing of work for order-committed batches, neither the user nor the system is allowed to change the batch number.</span></span> <span data-ttu-id="84ca9-166">（此处理包括异常处理。）</span><span class="sxs-lookup"><span data-stu-id="84ca9-166">(This processing includes exception handling.)</span></span>

<span data-ttu-id="84ca9-167">以下示例显示了端到端流。</span><span class="sxs-lookup"><span data-stu-id="84ca9-167">The following example shows the end-to-end flow.</span></span>

## <a name="example-scenario-batch-number-allocation"></a><span data-ttu-id="84ca9-168">示例方案：批号分配</span><span class="sxs-lookup"><span data-stu-id="84ca9-168">Example scenario: Batch number allocation</span></span>

<span data-ttu-id="84ca9-169">必须为此示例安装演示数据，并且必须使用 **USMF** 演示数据公司。</span><span class="sxs-lookup"><span data-stu-id="84ca9-169">For this example, demo data must be installed, and you must use the **USMF** demo data company.</span></span>

### <a name="set-up-an-inventory-reservation-hierarchy-to-allow-batch-specific-reservation"></a><a name="Example-batch-allocation"></a><span data-ttu-id="84ca9-170">设置库存预留层次结构以允许批次特定预留</span><span class="sxs-lookup"><span data-stu-id="84ca9-170">Set up an inventory reservation hierarchy to allow batch-specific reservation</span></span>

1. <span data-ttu-id="84ca9-171">转到 **仓库管理** \> **设置** \> **库存 \> 预留层次结构**。</span><span class="sxs-lookup"><span data-stu-id="84ca9-171">Go to **Warehouse management** \> **Setup** \> **Inventory \> Reservation hierarchy**.</span></span>
2. <span data-ttu-id="84ca9-172">选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="84ca9-172">Select **New**.</span></span>
3. <span data-ttu-id="84ca9-173">在 **名称** 字段中，输入名称（例如，**BatchFlex**）。</span><span class="sxs-lookup"><span data-stu-id="84ca9-173">In the **Name** field, enter a name (for example, **BatchFlex**).</span></span>
4. <span data-ttu-id="84ca9-174">在 **描述** 字段中，输入描述（例如，**批次以下灵活预留**）。</span><span class="sxs-lookup"><span data-stu-id="84ca9-174">In the **Description** field, enter a description (for example, **Batch below flexible**).</span></span>
5. <span data-ttu-id="84ca9-175">在 **已选** 字段中，选择 **序列号** 和 **所有者**，然后选择左箭头按钮将其移至 **可用** 字段。</span><span class="sxs-lookup"><span data-stu-id="84ca9-175">In the **Selected** field, select **Serial number** and **Owner**, and then select the left arrow button to move them to the **Available** field.</span></span>
6. <span data-ttu-id="84ca9-176">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="84ca9-176">Select **OK**.</span></span>
7. <span data-ttu-id="84ca9-177">在 **批号** 维度级别行中，选择 **允许在需求订单上预留** 复选框。</span><span class="sxs-lookup"><span data-stu-id="84ca9-177">In the row for the **Batch number** dimension level, select the **Allow reservation on demand order** check box.</span></span> <span data-ttu-id="84ca9-178">**牌照** 和 **货位** 级别将自动选择，您不能清除它们的复选框。</span><span class="sxs-lookup"><span data-stu-id="84ca9-178">The **License plate** and **Location** levels are automatically selected, and you can't clear the check boxes for them.</span></span>
8. <span data-ttu-id="84ca9-179">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="84ca9-179">Select **Save**.</span></span>

### <a name="create-a-new-released-product"></a><span data-ttu-id="84ca9-180">创建新的已发布产品</span><span class="sxs-lookup"><span data-stu-id="84ca9-180">Create a new released product</span></span>

1. <span data-ttu-id="84ca9-181">使用以下值设置产品的三个主数据参数：</span><span class="sxs-lookup"><span data-stu-id="84ca9-181">Set the product's three master data parameters by using these values:</span></span>

    - <span data-ttu-id="84ca9-182">在 **存储维度组** 字段中，选择 **Ware**。</span><span class="sxs-lookup"><span data-stu-id="84ca9-182">In the **Storage dimension group** field, select **Ware**.</span></span>
    - <span data-ttu-id="84ca9-183">在 **跟踪维度组** 字段中，选择 **Batch-Phy**。</span><span class="sxs-lookup"><span data-stu-id="84ca9-183">In the **Tracking dimension group** field, select **Batch-Phy**.</span></span>
    - <span data-ttu-id="84ca9-184">在 **预留层次结构** 字段中，选择 **BatchFlex**。</span><span class="sxs-lookup"><span data-stu-id="84ca9-184">In the **Reservation hierarchy** field, select **BatchFlex**.</span></span>

2. <span data-ttu-id="84ca9-185">创建两个批号，例如 **B11** 和 **B22**。</span><span class="sxs-lookup"><span data-stu-id="84ca9-185">Create two batch numbers, such as **B11** and **B22**.</span></span>
3. <span data-ttu-id="84ca9-186">使用以下值将物料数量添加到现有库存中。</span><span class="sxs-lookup"><span data-stu-id="84ca9-186">Add item quantities to on-hand stock by using the following values.</span></span>

    | <span data-ttu-id="84ca9-187">存放地点</span><span class="sxs-lookup"><span data-stu-id="84ca9-187">Warehouse</span></span> | <span data-ttu-id="84ca9-188">批号</span><span class="sxs-lookup"><span data-stu-id="84ca9-188">Batch number</span></span> | <span data-ttu-id="84ca9-189">货位</span><span class="sxs-lookup"><span data-stu-id="84ca9-189">Location</span></span> | <span data-ttu-id="84ca9-190">牌照</span><span class="sxs-lookup"><span data-stu-id="84ca9-190">License plate</span></span> | <span data-ttu-id="84ca9-191">数量</span><span class="sxs-lookup"><span data-stu-id="84ca9-191">Quantity</span></span> |
    |-----------|--------------|----------|---------------|----------|
    | <span data-ttu-id="84ca9-192">24</span><span class="sxs-lookup"><span data-stu-id="84ca9-192">24</span></span>        | <span data-ttu-id="84ca9-193">B11</span><span class="sxs-lookup"><span data-stu-id="84ca9-193">B11</span></span>          | <span data-ttu-id="84ca9-194">BULK-001</span><span class="sxs-lookup"><span data-stu-id="84ca9-194">BULK-001</span></span> | <span data-ttu-id="84ca9-195">否</span><span class="sxs-lookup"><span data-stu-id="84ca9-195">None</span></span>          | <span data-ttu-id="84ca9-196">10</span><span class="sxs-lookup"><span data-stu-id="84ca9-196">10</span></span>       |
    | <span data-ttu-id="84ca9-197">24</span><span class="sxs-lookup"><span data-stu-id="84ca9-197">24</span></span>        | <span data-ttu-id="84ca9-198">B11</span><span class="sxs-lookup"><span data-stu-id="84ca9-198">B11</span></span>          | <span data-ttu-id="84ca9-199">FL-001</span><span class="sxs-lookup"><span data-stu-id="84ca9-199">FL-001</span></span>   | <span data-ttu-id="84ca9-200">LP11</span><span class="sxs-lookup"><span data-stu-id="84ca9-200">LP11</span></span>          | <span data-ttu-id="84ca9-201">10</span><span class="sxs-lookup"><span data-stu-id="84ca9-201">10</span></span>       |
    | <span data-ttu-id="84ca9-202">24</span><span class="sxs-lookup"><span data-stu-id="84ca9-202">24</span></span>        | <span data-ttu-id="84ca9-203">B22</span><span class="sxs-lookup"><span data-stu-id="84ca9-203">B22</span></span>          | <span data-ttu-id="84ca9-204">FL-002</span><span class="sxs-lookup"><span data-stu-id="84ca9-204">FL-002</span></span>   | <span data-ttu-id="84ca9-205">LP22</span><span class="sxs-lookup"><span data-stu-id="84ca9-205">LP22</span></span>          | <span data-ttu-id="84ca9-206">10</span><span class="sxs-lookup"><span data-stu-id="84ca9-206">10</span></span>       |

### <a name="enter-sales-order-details"></a><a name="sales-order-details"></a><span data-ttu-id="84ca9-207">输入销售订单详细信息</span><span class="sxs-lookup"><span data-stu-id="84ca9-207">Enter sales order details</span></span>

1. <span data-ttu-id="84ca9-208">转到 **销售和营销** \> **销售订单** \> **所有销售订单**。</span><span class="sxs-lookup"><span data-stu-id="84ca9-208">Go to **Sales and marketing** \> **Sales orders** \> **All sales orders**.</span></span>
2. <span data-ttu-id="84ca9-209">选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="84ca9-209">Select **New**.</span></span>
3. <span data-ttu-id="84ca9-210">在销售订单抬头上，在 **客户帐户** 字段中，输入 **US-003**。</span><span class="sxs-lookup"><span data-stu-id="84ca9-210">On the sales order header, in the **Customer account** field, enter **US-003**.</span></span>
4. <span data-ttu-id="84ca9-211">为新物料添加一行，然后输入 **10** 作为数量。</span><span class="sxs-lookup"><span data-stu-id="84ca9-211">Add a line for the new item, and enter **10** as the quantity.</span></span> <span data-ttu-id="84ca9-212">请确保 **仓库** 字段设置为 **24**。</span><span class="sxs-lookup"><span data-stu-id="84ca9-212">Make sure that the **Warehouse** field is set to **24**.</span></span>
5. <span data-ttu-id="84ca9-213">在 **销售订单行** 快速选项卡上，选择 **库存**，然后在 **维护** 组中，选择 **批次预留**。</span><span class="sxs-lookup"><span data-stu-id="84ca9-213">On the **Sales order lines** FastTab, select **Inventory**, and then, in the **Maintain** group, select **Batch reservation**.</span></span> <span data-ttu-id="84ca9-214">**批次预留** 页面将显示可为订单行预留的批次的列表。</span><span class="sxs-lookup"><span data-stu-id="84ca9-214">The **Batch reservation** page shows a list of batches that are available for reservation for the order line.</span></span> <span data-ttu-id="84ca9-215">在此示例中，此页面显示批号 **B11** 的数量为 **20**，批号 **B22** 的数量为 **10**。</span><span class="sxs-lookup"><span data-stu-id="84ca9-215">For this example, it shows a quantity of **20** for batch number **B11** and a quantity of **10** for batch number **B22**.</span></span> <span data-ttu-id="84ca9-216">请注意，如果某行的物料与 *Batch-below\[location\]* 预留层次结构关联，则无法从该行访问 **批次预留** 页面，除非已将其设置为允许特定于批次的预留。</span><span class="sxs-lookup"><span data-stu-id="84ca9-216">Note that the **Batch reservation** page cannot be accessed from a line if the item on that line is associated with *Batch-below\[location\]* reservation hierarchy unless it is set up to allow batch-specific reservation.</span></span>

    > [!NOTE]
    > <span data-ttu-id="84ca9-217">要为销售订单预留特定批次，您必须使用 **批次预留** 页。</span><span class="sxs-lookup"><span data-stu-id="84ca9-217">To reserve a specific batch for a sales order, you must use the **Batch reservation** page.</span></span>
    >
    > <span data-ttu-id="84ca9-218">如果您直接在销售订单行上输入批号，系统行为将与您为遵守 *Batch-below\[location\]* 预留策略的物料输入特定批次值时一样。</span><span class="sxs-lookup"><span data-stu-id="84ca9-218">If you enter the batch number directly on the sales order line, the system will behave as though you entered a specific batch value for an item that is subject to the *Batch-below\[location\]* reservation policy.</span></span> <span data-ttu-id="84ca9-219">保存行时，您将收到一条警告消息。</span><span class="sxs-lookup"><span data-stu-id="84ca9-219">When you save the line, you will receive a warning message.</span></span> <span data-ttu-id="84ca9-220">如果您确认应直接在订单行上指定批号，该行将不会由常规仓库管理逻辑处理。</span><span class="sxs-lookup"><span data-stu-id="84ca9-220">If you confirm that the batch number should be specified directly on the order line, the line won't be handled by the regular warehouse management logic.</span></span>
    >
    > <span data-ttu-id="84ca9-221">如果您从 **预留** 页面预留数量，将不预留特定批次，并且该行的仓库操作的执行将遵循按照 *Batch-below\[location\]* 预留策略适用的规则。</span><span class="sxs-lookup"><span data-stu-id="84ca9-221">If you reserve the quantity from the **Reservation** page, no specific batch will be reserved, and the execution of warehouse operations for the line will follow the rules that are applicable under the *Batch-below\[location\]* reservation policy.</span></span>

    <span data-ttu-id="84ca9-222">通常，此页面的工作和交互方式与用于具有 *Batch-above\[location\]* 类型的关联预留层次结构的物料时相同。</span><span class="sxs-lookup"><span data-stu-id="84ca9-222">In general, this page works and is interacted with in the same way for items that have an associated reservation hierarchy of the *Batch-above\[location\]* type.</span></span> <span data-ttu-id="84ca9-223">但是，以下例外适用：</span><span class="sxs-lookup"><span data-stu-id="84ca9-223">However, the following exceptions apply:</span></span>

    - <span data-ttu-id="84ca9-224">**提交到源行的批号** 快速选项卡显示为订单行预留的批号。</span><span class="sxs-lookup"><span data-stu-id="84ca9-224">The **Batch numbers committed to source line** FastTab shows the batch numbers that are reserved for the order line.</span></span> <span data-ttu-id="84ca9-225">网格中的批次值将在订单行的整个履行周期内显示，包括仓库处理阶段。</span><span class="sxs-lookup"><span data-stu-id="84ca9-225">The batch values in the grid will be shown throughout the fulfillment cycle of the order line, including the warehouse processing stages.</span></span> <span data-ttu-id="84ca9-226">相比之下，在 **概览** 快速选项卡上，常规的订单行预留（即针对 **货位** 级别以上的维度进行的预留）显示在网格中，直到仓库工作创建为止。</span><span class="sxs-lookup"><span data-stu-id="84ca9-226">By contrast, on the **Overview** FastTab, regular order line reservation (that is, reservation that is done for the dimensions above the **Location** level) is shown in the grid up to the point when warehouse work is created.</span></span> <span data-ttu-id="84ca9-227">然后，工作实体接管行预留，行预留不再出现在页面上。</span><span class="sxs-lookup"><span data-stu-id="84ca9-227">The work entity then takes over the line reservation, and the line reservation no longer appears on the page.</span></span> <span data-ttu-id="84ca9-228">**提交到源行的批号** 快速选项卡帮助确保销售订单管理员可以查看，在客户订单生命周期的任何时间直到开票提交到该订单的批号。</span><span class="sxs-lookup"><span data-stu-id="84ca9-228">The **Batch numbers committed to source line** FastTab helps guarantee that the sales order processor can view the batch numbers that were committed to the customer's order at any point during its lifecycle, up through invoicing.</span></span>
    - <span data-ttu-id="84ca9-229">除了预留特定批次外，用户还可以手动选择批次的特定货位和牌照，而不是让系统自动选择。</span><span class="sxs-lookup"><span data-stu-id="84ca9-229">In addition to reserving a specific batch, a user can manually select the batch's specific location and license plate instead of letting the system automatically select them.</span></span> <span data-ttu-id="84ca9-230">此功能与订单承诺批次预留机制的设计有关。</span><span class="sxs-lookup"><span data-stu-id="84ca9-230">This capability is related to the design of the order-committed batch reservation mechanism.</span></span> <span data-ttu-id="84ca9-231">如前所述，当根据 *Batch-below\[location\]* 预留策略为物料预留批号时，系统必须预留整个库位的所有维度。</span><span class="sxs-lookup"><span data-stu-id="84ca9-231">As was mentioned earlier, when a batch number is reserved for an item under the *Batch-below\[location\]* reservation policy, the system must reserve all dimensions up through location.</span></span> <span data-ttu-id="84ca9-232">因此，仓库工作将包含与处理订单的用户预留的相同的存储维度，可能并不总是代表着对领料操作方便甚至可能的物料存储位置。</span><span class="sxs-lookup"><span data-stu-id="84ca9-232">Therefore, warehouse work will carry the same storage dimensions that were reserved by the users who worked with the orders, and it might not always represent the item storage placement that is convenient, or even possible, for picking operations.</span></span> <span data-ttu-id="84ca9-233">如果订单管理员知道仓库约束，他们可能希望在预留批次时手动选择特定货位和牌照。</span><span class="sxs-lookup"><span data-stu-id="84ca9-233">If order processors are aware of the warehouse constraints, they might want to manually select the specific locations and license plates when they reserve a batch.</span></span> <span data-ttu-id="84ca9-234">在这种情况下，用户必须使用页标题上的 **显示维度** 功能，并且必须在 **概览** 快速选项卡上的网格中添加货位和牌照。</span><span class="sxs-lookup"><span data-stu-id="84ca9-234">In this case, the user must use the **Display dimensions** functionality on the page header, and must add the location and license plate in the grid on the **Overview** FastTab.</span></span>

6. <span data-ttu-id="84ca9-235">在 **批次预留** 页面上，选择 **B11** 这一行，然后选择 **预留行**。</span><span class="sxs-lookup"><span data-stu-id="84ca9-235">On the **Batch reservation** page, select the line for batch **B11**, and then select **Reserve line**.</span></span> <span data-ttu-id="84ca9-236">在自动预留期间，没有用于分配货位和牌照的指定逻辑。</span><span class="sxs-lookup"><span data-stu-id="84ca9-236">There is no designated logic for assigning locations and license plates during automatic reservation.</span></span> <span data-ttu-id="84ca9-237">您可以在 **预留** 字段中手动输入数量。</span><span class="sxs-lookup"><span data-stu-id="84ca9-237">You can manually enter the quantity in the **Reservation** field.</span></span> <span data-ttu-id="84ca9-238">请注意，在 **提交到源行的批号** 快速选项卡上，批次 **B11** 将显示为 **已提交**。</span><span class="sxs-lookup"><span data-stu-id="84ca9-238">Notice that, on the **Batch numbers committed to source line** FastTab, batch **B11** is shown as **Committed**.</span></span>

    ![在“批次预留”页面上向销售订单行提交特定批号](media/Batch-reservation-form-with-order-committed-reservation.png)

    > [!NOTE]
    > <span data-ttu-id="84ca9-240">可以跨多个批次在销售订单行上预留数量。</span><span class="sxs-lookup"><span data-stu-id="84ca9-240">Reservation of the quantity on a sales order line can be done across multiple batches.</span></span> <span data-ttu-id="84ca9-241">同样，可以针对多个货位和牌照进行同一批次的预留（如果已为货位启用了牌照）。</span><span class="sxs-lookup"><span data-stu-id="84ca9-241">Likewise, reservation of the same batch can be done against multiple locations and license plates (if license plates are enabled for the locations).</span></span>
    >
    > <span data-ttu-id="84ca9-242">在销售订单行上为数量预留特定批次也可以部分进行。</span><span class="sxs-lookup"><span data-stu-id="84ca9-242">Reservation of a specific batch for the quantity on a sales order line can also be partial.</span></span> <span data-ttu-id="84ca9-243">例如，可以预留 100 个单位的总数量，以向 20 个单位提交特定批次，而在站点和仓库级别为任何可用批次预留 80 个单位。</span><span class="sxs-lookup"><span data-stu-id="84ca9-243">For example, the total quantity of 100 units can be reserved so that a specific batch is committed to 20 units, whereas 80 units are reserved at the site and warehouse levels for any available batch.</span></span> <span data-ttu-id="84ca9-244">在这种情况下，WMS 将使用两个单独的工作行来处理领料操作。</span><span class="sxs-lookup"><span data-stu-id="84ca9-244">In this case, the WMS will handle picking operations by using two separate work lines.</span></span>

7. <span data-ttu-id="84ca9-245">转到 **产品信息管理** \> **产品** \> **已发布产品**。</span><span class="sxs-lookup"><span data-stu-id="84ca9-245">Go to **Product information management** \> **Products** \> **Released products**.</span></span> <span data-ttu-id="84ca9-246">选择您的物料，然后选择 **管理库存** \> **查看**\>**交易记录**。</span><span class="sxs-lookup"><span data-stu-id="84ca9-246">Select your item, and then select **Manage inventory** \> **View** \> **Transactions**.</span></span>

    ![将订单承诺预留作为库存交易记录类型](media/Inventory-transactions-for-order-committed-reservation.png)

8. <span data-ttu-id="84ca9-248">查看与销售订单行预留相关的物料库存交易记录。</span><span class="sxs-lookup"><span data-stu-id="84ca9-248">Review the item's inventory transactions that are related to the sales order line reservation.</span></span>

    - <span data-ttu-id="84ca9-249">**参考** 字段设置为 **销售订单** 且 **发货** 字段设置为 **实际预留** 的交易记录，表示 **货位** 级别以上的库存维度的订单行预留。</span><span class="sxs-lookup"><span data-stu-id="84ca9-249">A transaction where the **Reference** field is set to **Sales order** and the **Issue** field is set to **Reserved physical** represents the order line reservation for the inventory dimensions above the **Location** level.</span></span> <span data-ttu-id="84ca9-250">根据物料的库存预留层次结构，这些维度是站点、仓库和库存状态。</span><span class="sxs-lookup"><span data-stu-id="84ca9-250">According to the item's inventory reservation hierarchy, those dimensions are site, warehouse, and inventory status.</span></span>
    - <span data-ttu-id="84ca9-251">**参考** 字段设置为 **订单承诺预留** 且 **发货** 字段设置为 **实际预留** 的交易记录，表示特定批次以及其以上所有库存维度的订单行预留。</span><span class="sxs-lookup"><span data-stu-id="84ca9-251">A transaction where the **Reference** field is set to **Order-committed reservation** and the **Issue** field is set to **Reserved physical** represents the order line reservation for the specific batch and all inventory dimensions above it.</span></span> <span data-ttu-id="84ca9-252">根据物料的库存预留层次结构，这些维度是批号和货位。</span><span class="sxs-lookup"><span data-stu-id="84ca9-252">According to the item's inventory reservation hierarchy, those dimensions are batch number and location.</span></span> <span data-ttu-id="84ca9-253">在此示例中，货位是 **Bulk-001**。</span><span class="sxs-lookup"><span data-stu-id="84ca9-253">In this example, the location is **Bulk-001**.</span></span>

9. <span data-ttu-id="84ca9-254">在销售订单抬头上，选择 **仓库** \> **操作** \> **发放到仓库**。</span><span class="sxs-lookup"><span data-stu-id="84ca9-254">On the sales order header, select **Warehouse** \> **Actions** \> **Release to warehouse**.</span></span> <span data-ttu-id="84ca9-255">订单行现在已分波次，负荷和工作已创建。</span><span class="sxs-lookup"><span data-stu-id="84ca9-255">The order line is now waved, and a load and work are created.</span></span>

### <a name="review-and-process-warehouse-work-that-has-order-committed-batch-numbers"></a><span data-ttu-id="84ca9-256">审查和处理具有订单承诺批号的仓库工作</span><span class="sxs-lookup"><span data-stu-id="84ca9-256">Review and process warehouse work that has order-committed batch numbers</span></span>

1. <span data-ttu-id="84ca9-257">在 **销售订单行** 快速选项卡上，选择 **仓库** \> **工作详细信息**。</span><span class="sxs-lookup"><span data-stu-id="84ca9-257">On the **Sales order lines** FastTab, select **Warehouse** \> **Work details**.</span></span>

    <span data-ttu-id="84ca9-258">处理提交给销售订单行的批次数量的领料操作的工作具有以下特征：</span><span class="sxs-lookup"><span data-stu-id="84ca9-258">The work that handles the picking operation for batch quantities that are committed to the sales order line has the following characteristics:</span></span>

    - <span data-ttu-id="84ca9-259">为了创建工作，系统使用工作模板，而不是货位指令。</span><span class="sxs-lookup"><span data-stu-id="84ca9-259">To create work, the system uses work templates but not location directives.</span></span> <span data-ttu-id="84ca9-260">为工作模板定义的所有标准设置（例如，最大领料行数或特定度量单位）将应用来确定何时应创建新工作。</span><span class="sxs-lookup"><span data-stu-id="84ca9-260">All the standard settings that are defined for work templates, such as a maximum number of pick lines or a specific unit of measure, will be applied to determine when new work should be created.</span></span> <span data-ttu-id="84ca9-261">但是，不考虑与用于识别领料货位的货位指令相关联的规则，因为订单承诺预留已经指定了所有库存维度。</span><span class="sxs-lookup"><span data-stu-id="84ca9-261">However, the rules that are associated with location directives for identifying pick locations aren't considered, because the order-committed reservation already specifies all the inventory dimensions.</span></span> <span data-ttu-id="84ca9-262">这些库存维度包括仓库存储级别的维度。</span><span class="sxs-lookup"><span data-stu-id="84ca9-262">Those inventory dimensions include the dimensions at the warehouse storage level.</span></span> <span data-ttu-id="84ca9-263">因此，作品将继承这些维度，而不必参考货位指令。</span><span class="sxs-lookup"><span data-stu-id="84ca9-263">Therefore, the work inherits those dimensions without having to consult location directives.</span></span>
    - <span data-ttu-id="84ca9-264">批号不显示在领料行上（对于为具有关联的 *Batch-above\[location\]* 预留层次结构的物料创建的工作行就是这种情况。）而“源”批号和所有其他存储维度将显示在工作行的工作库存交易记录中，该交易记录是从关联的库存交易记录引用的。</span><span class="sxs-lookup"><span data-stu-id="84ca9-264">The batch number isn't shown on the pick line (as is the case for the work line that is created for an item that has an associated *Batch-above\[location\]* reservation hierarchy.) Instead, the "from" batch number and all other storage dimensions are shown on the work line's work inventory transaction that is referenced from the associated inventory transactions.</span></span>

        ![源自订单承诺预留的工作的仓库库存交易记录](media/Work-inventory-transactions-for-order-committed-reservation.png)

    - <span data-ttu-id="84ca9-266">创建工作后，**参考** 字段设置为 **订单承诺预留** 的物料的库存交易记录将删除。</span><span class="sxs-lookup"><span data-stu-id="84ca9-266">After work is created, the item's inventory transaction where the **Reference** field is set to **Order-committed reservation** is removed.</span></span> <span data-ttu-id="84ca9-267">**参考** 字段设置为 **工作** 的库存交易记录现在在所有数量的库存维度中保留实际预留。</span><span class="sxs-lookup"><span data-stu-id="84ca9-267">The inventory transaction where the **Reference** field is set to **Work** now holds the physical reservation on all the quantity's inventory dimensions.</span></span>

        <span data-ttu-id="84ca9-268">仓库操作可以以通常的方式继续处理工作的执行。</span><span class="sxs-lookup"><span data-stu-id="84ca9-268">Warehouse operations can proceed to handle execution of the work in the usual manner.</span></span> <span data-ttu-id="84ca9-269">但是，移动设备上的指令将指示工作人员领取特定的批号。</span><span class="sxs-lookup"><span data-stu-id="84ca9-269">However, the instructions on the mobile device will instruct the worker to pick a specific batch number.</span></span> <span data-ttu-id="84ca9-270">在货位由牌照控制的仓库环境中，当工作人员到达将同一批次存储在多个牌照中的货位后，他或她可以从尚未预留的任何牌照领料（例如，通过另一个订单承诺预留或源自该类型预留的工作。）</span><span class="sxs-lookup"><span data-stu-id="84ca9-270">In warehouse environments where locations are license plate–controlled, after a worker reaches a location that stores the same batch on multiple license plates, he or she can pick from any license plate that isn't already reserved (for example, by another order-committed reservation or work that originates from a reservation of that type.)</span></span>

        <span data-ttu-id="84ca9-271">如果发现从工作行上指定的货位领料不切实际，仓库操作员可以使用以下操作之一重定向来从更方便的货位领取特定批次：</span><span class="sxs-lookup"><span data-stu-id="84ca9-271">If it turns out to be impractical to pick from the location that is specified on the work line, the warehouse operators can use one of the following actions to redirect picking of the specific batch from a more convenient location:</span></span>

        - <span data-ttu-id="84ca9-272">移动设备上的标准 **覆盖货位** 操作（前提是仓库工作人员的 **允许领料货位覆盖** 设置已启用）</span><span class="sxs-lookup"><span data-stu-id="84ca9-272">The standard **Override location** action on a mobile device (provided that the warehouse worker's **Allow pick location override** setting is enabled)</span></span>
        - <span data-ttu-id="84ca9-273">**工作列表详细信息** 页的 **更改货位** 操作。</span><span class="sxs-lookup"><span data-stu-id="84ca9-273">The **Change location** action on the **Work list details** page.</span></span> 

2. <span data-ttu-id="84ca9-274">在移动设备上，完成领料并放入工作。</span><span class="sxs-lookup"><span data-stu-id="84ca9-274">On the mobile device, finish picking and putting the work.</span></span>

    <span data-ttu-id="84ca9-275">批号 **B11** 的数量 **10** 现在已为销售订单行领取，并放入 **Baydoor** 货位。</span><span class="sxs-lookup"><span data-stu-id="84ca9-275">The quantity of **10** for batch number **B11** is now picked for the sales order line and put in the **Baydoor** location.</span></span> <span data-ttu-id="84ca9-276">此时，可以将其装载到卡车上并发往客户地址了。</span><span class="sxs-lookup"><span data-stu-id="84ca9-276">At this point, it's ready to be loaded onto the truck and dispatched to the customer's address.</span></span>

## <a name="flexible-license-plate-reservation"></a><span data-ttu-id="84ca9-277">灵活牌照预留</span><span class="sxs-lookup"><span data-stu-id="84ca9-277">Flexible license plate reservation</span></span>

### <a name="business-scenario"></a><span data-ttu-id="84ca9-278">业务方案</span><span class="sxs-lookup"><span data-stu-id="84ca9-278">Business scenario</span></span>

<span data-ttu-id="84ca9-279">在此方案中，某公司使用仓库管理和工作处理，在创建工作之前在 Supply Chain Management 外部的单个托盘/容器级别处理装载计划。</span><span class="sxs-lookup"><span data-stu-id="84ca9-279">In this scenario, a company uses warehouse management and work processing, and handles load planning at the level of individual pallets/containers outside Supply Chain Management before work is created.</span></span> <span data-ttu-id="84ca9-280">这些容器由库存维度中的牌照表示。</span><span class="sxs-lookup"><span data-stu-id="84ca9-280">These containers are represented by license plates in the inventory dimensions.</span></span> <span data-ttu-id="84ca9-281">因此，对于这种方法，必须在完成领料工作之前将特定牌照预先分配给销售订单行。</span><span class="sxs-lookup"><span data-stu-id="84ca9-281">Therefore, for this approach, specific license plates must be pre-assigned to sales order lines before picking work is done.</span></span> <span data-ttu-id="84ca9-282">该公司正在寻求一种灵活的方式来处理牌照预留规则，以执行以下行为：</span><span class="sxs-lookup"><span data-stu-id="84ca9-282">The company is looking for flexibility in the way that the license plate reservation rules are handled, so that the following behaviors occur:</span></span>

- <span data-ttu-id="84ca9-283">当销售管理员接收订单时，可以记录并预留牌照，并且牌照不能被其他需求获取。</span><span class="sxs-lookup"><span data-stu-id="84ca9-283">A license plate can be recorded and reserved when the order is taken by the sales processor, and it can't be taken by other demands.</span></span> <span data-ttu-id="84ca9-284">此行为有助于确保将计划的牌照运送到客户。</span><span class="sxs-lookup"><span data-stu-id="84ca9-284">This behavior helps guarantee that the license plate that was planned is shipped to the customer.</span></span>
- <span data-ttu-id="84ca9-285">如果尚未将牌照分配给销售订单行，仓库人员可以在销售订单登记和预留完成后在领料工作中选择牌照。</span><span class="sxs-lookup"><span data-stu-id="84ca9-285">If the license plate isn't already assigned to a sales order line, warehouse personnel can select a license plate during picking work, after sales order registration and reservation are completed.</span></span>

### <a name="turn-on-flexible-license-plate-reservation"></a><span data-ttu-id="84ca9-286">开启“灵活牌照预留”</span><span class="sxs-lookup"><span data-stu-id="84ca9-286">Turn on flexible license plate reservation</span></span>

<span data-ttu-id="84ca9-287">必须在系统中开启两项功能，才能够使用灵活牌照预留。</span><span class="sxs-lookup"><span data-stu-id="84ca9-287">Before you can use flexible license plate reservation, two features must be turned on in your system.</span></span> <span data-ttu-id="84ca9-288">管理员可以使用[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)设置检查这些功能的状态，并在需要这些功能时将其开启。</span><span class="sxs-lookup"><span data-stu-id="84ca9-288">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the features and turn them on if they are required.</span></span> <span data-ttu-id="84ca9-289">您必须按以下顺序开启功能：</span><span class="sxs-lookup"><span data-stu-id="84ca9-289">You must turn on the features in the following order:</span></span>

1. <span data-ttu-id="84ca9-290">**功能名称**：*灵活的仓库级维度预留*</span><span class="sxs-lookup"><span data-stu-id="84ca9-290">**Feature name:** *Flexible warehouse-level dimension reservation*</span></span>
1. <span data-ttu-id="84ca9-291">**功能名称**：*灵活的订单承诺牌照预留*</span><span class="sxs-lookup"><span data-stu-id="84ca9-291">**Feature name:** *Flexible order-committed license plate reservation*</span></span>

### <a name="reserve-a-specific-license-plate-on-the-sales-order"></a><span data-ttu-id="84ca9-292">在销售订单上预留特定牌照</span><span class="sxs-lookup"><span data-stu-id="84ca9-292">Reserve a specific license plate on the sales order</span></span>

<span data-ttu-id="84ca9-293">要在订单上启用牌照预留，您必须在与相关物料关联的层次结构的 **库存预留层次结构** 页，选中 **牌照** 级别的 **允许在需求订单上预留** 复选框。</span><span class="sxs-lookup"><span data-stu-id="84ca9-293">To enable license plate reservation on an order, you must select the **Allow reservation on demand order** check box for the **License plate** level on the **Inventory reservation hierarchies** page for the hierarchy that is associated with the relevant item.</span></span>

![灵活牌照预留层次结构的“库存预留层次结构”页面](media/Flexible-LP-reservation-hierarchy.png)

<span data-ttu-id="84ca9-295">您可以在部署中的任何时候在订单上启用牌照预留。</span><span class="sxs-lookup"><span data-stu-id="84ca9-295">You can enable license plate reservation on the order at any point in your deployment.</span></span> <span data-ttu-id="84ca9-296">此更改不会影响更改发生之前创建的任何预留或开放仓库工作。</span><span class="sxs-lookup"><span data-stu-id="84ca9-296">This change won't affect any reservations or open warehouse work that were created before the change occurred.</span></span> <span data-ttu-id="84ca9-297">但是，如果与该预订层次结构关联的一个或多个物料存在状态为 *在单*、*订购预留* 或 *实际预留* 的未结出站库存交易记录，则无法清除 **允许在需求订单上预留** 复选框。</span><span class="sxs-lookup"><span data-stu-id="84ca9-297">However, you can't clear the **Allow reservation on demand order** check box if open outbound inventory transactions that have an issue status of *On order*, *Reserved ordered*, or *Reserved physical* exist for one or more items that are associated with that reservation hierarchy.</span></span>

<span data-ttu-id="84ca9-298">即使为 **牌照** 级别选中了 **允许在需求订单上预留** 复选框，仍然可以 *不* 在订单上预留特定牌照。</span><span class="sxs-lookup"><span data-stu-id="84ca9-298">Even if the **Allow reservation on demand order** check box is selected for the **License plate** level, it's still possible *not* to reserve a specific license plate on the order.</span></span> <span data-ttu-id="84ca9-299">在这种情况下，应用对预留层次结构有效的默认仓库操作逻辑。</span><span class="sxs-lookup"><span data-stu-id="84ca9-299">In this case, the default warehouse operations logic that is valid for the reservation hierarchy applies.</span></span>

<span data-ttu-id="84ca9-300">若要预留特定牌照，您必须使用 [Open Data Protocol (OData)](../../fin-ops-core/dev-itpro/data-entities/odata.md) 流程。</span><span class="sxs-lookup"><span data-stu-id="84ca9-300">To reserve a specific license plate, you must use an [Open Data Protocol (OData)](../../fin-ops-core/dev-itpro/data-entities/odata.md) process.</span></span> <span data-ttu-id="84ca9-301">在应用程序中，您可以使用 **在 Excel 中打开** 命令的 **每个牌照的订单承诺预留** 选项直接从销售订单中执行此预留。</span><span class="sxs-lookup"><span data-stu-id="84ca9-301">In the application, you can do this reservation directly from a sales order by using the **Order-committed reservations per license plate** option of the **Open in Excel** command.</span></span> <span data-ttu-id="84ca9-302">在 Excel 加载项中打开的实体数据中，您必须输入以下与预留相关的数据，然后选择 **发布** 将数据发送回 Supply Chain Management：</span><span class="sxs-lookup"><span data-stu-id="84ca9-302">In the entity data that is opened in the Excel add-in, you must enter the following reservation-related data and then select **Publish** to send the data back to Supply Chain Management:</span></span>

- <span data-ttu-id="84ca9-303">引用（仅支持 *销售订单* 值。）</span><span class="sxs-lookup"><span data-stu-id="84ca9-303">Reference (Only the *Sales order* value is supported.)</span></span>
- <span data-ttu-id="84ca9-304">订单编号（此值可以从批次派生。）</span><span class="sxs-lookup"><span data-stu-id="84ca9-304">Order number (The value can be derived from the lot.)</span></span>
- <span data-ttu-id="84ca9-305">批次 ID</span><span class="sxs-lookup"><span data-stu-id="84ca9-305">Lot ID</span></span>
- <span data-ttu-id="84ca9-306">牌照</span><span class="sxs-lookup"><span data-stu-id="84ca9-306">License plate</span></span>
- <span data-ttu-id="84ca9-307">数量</span><span class="sxs-lookup"><span data-stu-id="84ca9-307">Quantity</span></span>

<span data-ttu-id="84ca9-308">如果必须为批量跟踪物料预留特定牌照，请使用 **批次预留** 页面，如[输入销售订单详细信息](#sales-order-details)一节所述。</span><span class="sxs-lookup"><span data-stu-id="84ca9-308">If you must reserve a specific license plate for a batch-tracked item, use the **Batch reservation** page, as described in the [Enter sales order details](#sales-order-details) section.</span></span>

<span data-ttu-id="84ca9-309">当使用订单承诺牌照预留的销售订单行由仓库操作处理时，将不使用位置指令。</span><span class="sxs-lookup"><span data-stu-id="84ca9-309">When the sales order line that uses an order-committed license plate reservation is processed by warehouse operations, location directives aren't used.</span></span>

<span data-ttu-id="84ca9-310">如果仓库工作项由等同于一个完整托盘的行组成，并且具有牌照承诺数量，您可以使用移动设备菜单项（**按牌照处理** 选项设置为 *是*）来优化领料流程。</span><span class="sxs-lookup"><span data-stu-id="84ca9-310">If a warehouse work item consists of lines that equal a complete pallet and have license plate–committed quantities, you can optimize the picking process by using a mobile device menu item where the **Handle by license plate** option is set to *Yes*.</span></span> <span data-ttu-id="84ca9-311">然后，仓库工作人员可以扫描牌照来完成领料，而不必在工作中逐个扫描物料。</span><span class="sxs-lookup"><span data-stu-id="84ca9-311">A warehouse worker can then scan a license plate to complete a pick instead of having to scan the items from the work one by one.</span></span>

![“按牌照处理”选项设置为“是”的移动设备菜单项](media/Handle-by-LP-menu-item.png)

<span data-ttu-id="84ca9-313">由于 **按牌照处理** 功能不支持包含多个托盘的工作，因此最好为不同的牌照使用单独的工作项。</span><span class="sxs-lookup"><span data-stu-id="84ca9-313">Because the **Handle by license plate** functionality doesn't support work that covers multiple pallets, it's better to have a separate work item for different license plates.</span></span> <span data-ttu-id="84ca9-314">要使用此方法，请在 **工作模板** 页面上添加 **订单承诺牌照 ID** 字段作为工作标题分行符。</span><span class="sxs-lookup"><span data-stu-id="84ca9-314">To use this approach, add the **Order-committed license plate ID** field as a work header break on the **Work template** page.</span></span>

> [!NOTE]
> <span data-ttu-id="84ca9-315">对于订单承诺工作创建过程，“订单承诺库存维度”值将分配给领料工作行，并且无法直接查看牌照值。</span><span class="sxs-lookup"><span data-stu-id="84ca9-315">For the order-committed work creation process, an "order-committed inventory dimension" value will be assigned to the picking work lines, and it won't be possible to view the license plate value directly.</span></span> <span data-ttu-id="84ca9-316">在设置移动设备菜单项时，仅支持 *用户导向* 过程。</span><span class="sxs-lookup"><span data-stu-id="84ca9-316">Only the *User directed* process is supported when setting up a mobile device menu item.</span></span>

## <a name="example-scenario-set-up-and-process-an-order-committed-license-plate-reservation"></a><span data-ttu-id="84ca9-317">示例方案：设置和处理订单承诺牌照预留</span><span class="sxs-lookup"><span data-stu-id="84ca9-317">Example scenario: Set up and process an order-committed license plate reservation</span></span>

<span data-ttu-id="84ca9-318">此方案演示如何设置和处理订单承诺牌照预留。</span><span class="sxs-lookup"><span data-stu-id="84ca9-318">This scenario shows how to set up and process an order-committed license plate reservation.</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="84ca9-319">提供演示数据</span><span class="sxs-lookup"><span data-stu-id="84ca9-319">Make demo data available</span></span>

<span data-ttu-id="84ca9-320">此方案引用为 Supply Chain Management 提供的标准演示数据中包含的值和记录。</span><span class="sxs-lookup"><span data-stu-id="84ca9-320">This scenario refers to values and records that are included in the standard demo data that is provided for Supply Chain Management.</span></span> <span data-ttu-id="84ca9-321">如果要使用此处提供的值来演练此方案，请确保在安装了演示数据的环境中工作。</span><span class="sxs-lookup"><span data-stu-id="84ca9-321">If you want to work through the scenario by using the values that are provided here, be sure to work on an environment where the demo data is installed.</span></span> <span data-ttu-id="84ca9-322">此外，在开始前，将法人设置为 **USMF**。</span><span class="sxs-lookup"><span data-stu-id="84ca9-322">Additionally, set the legal entity to **USMF** before you begin.</span></span>

### <a name="create-an-inventory-reservation-hierarchy-that-allows-for-license-plate-reservation"></a><span data-ttu-id="84ca9-323">创建允许牌照预留的库存预留层次结构</span><span class="sxs-lookup"><span data-stu-id="84ca9-323">Create an inventory reservation hierarchy that allows for license plate reservation</span></span>

1. <span data-ttu-id="84ca9-324">转到 **仓库管理 \> 设置 \> 库存 \> 预留层次结构**。</span><span class="sxs-lookup"><span data-stu-id="84ca9-324">Go to **Warehouse management \> Setup \> Inventory \> Reservation hierarchy**.</span></span>
1. <span data-ttu-id="84ca9-325">选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="84ca9-325">Select **New**.</span></span>
1. <span data-ttu-id="84ca9-326">在 **名称** 字段中，输入值（例如，*FlexibleLP*）。</span><span class="sxs-lookup"><span data-stu-id="84ca9-326">In the **Name** field, enter a value (for example, *FlexibleLP*).</span></span>
1. <span data-ttu-id="84ca9-327">在 **描述** 字段中，输入值（例如，*灵活牌照预留*）。</span><span class="sxs-lookup"><span data-stu-id="84ca9-327">In the **Description** field, enter a value (for example, *Flexible LP reservation*).</span></span>
1. <span data-ttu-id="84ca9-328">在 **选定** 列表中，选择 **批号**、**序列号** 和 **所有者**。</span><span class="sxs-lookup"><span data-stu-id="84ca9-328">In the **Selected** list, select **Batch number**, **Serial number**, and **Owner**.</span></span>
1. <span data-ttu-id="84ca9-329">选择 **删除** 按钮 ![向后箭头](media/backward-button.png) 将选定记录移到 **可用** 列表中。</span><span class="sxs-lookup"><span data-stu-id="84ca9-329">Select the **Remove** button ![backward arrow](media/backward-button.png) to move the selected records to the **Available** list.</span></span>
1. <span data-ttu-id="84ca9-330">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="84ca9-330">Select **OK**.</span></span>
1. <span data-ttu-id="84ca9-331">在 **牌照** 维度级别行中，选择 **允许在需求订单上预留** 复选框。</span><span class="sxs-lookup"><span data-stu-id="84ca9-331">In the row for the **License plate** dimension level, select the **Allow reservation on demand order** check box.</span></span> <span data-ttu-id="84ca9-332">**位置** 级别将自动选择，您不能清除它的复选框。</span><span class="sxs-lookup"><span data-stu-id="84ca9-332">The **Location** level is automatically selected, and you can't clear the check box for it.</span></span>
1. <span data-ttu-id="84ca9-333">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="84ca9-333">Select **Save**.</span></span>

### <a name="create-two-released-products"></a><span data-ttu-id="84ca9-334">创建两个已发布产品</span><span class="sxs-lookup"><span data-stu-id="84ca9-334">Create two released products</span></span>

1. <span data-ttu-id="84ca9-335">转到 **产品信息管理 \> 产品 \> 已发布产品**。</span><span class="sxs-lookup"><span data-stu-id="84ca9-335">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="84ca9-336">在操作窗格上，选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="84ca9-336">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="84ca9-337">在 **新建已发布产品** 对话框中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="84ca9-337">In the **New released product** dialog box, set the following values:</span></span>

    - <span data-ttu-id="84ca9-338">**产品编号**：*Item1*</span><span class="sxs-lookup"><span data-stu-id="84ca9-338">**Product number:** *Item1*</span></span>
    - <span data-ttu-id="84ca9-339">**物料编号**：*Item1*</span><span class="sxs-lookup"><span data-stu-id="84ca9-339">**Item number:** *Item1*</span></span>
    - <span data-ttu-id="84ca9-340">**物料模型组**：*先进先出*</span><span class="sxs-lookup"><span data-stu-id="84ca9-340">**Item model group:** *FIFO*</span></span>
    - <span data-ttu-id="84ca9-341">**物料组**：*音频*</span><span class="sxs-lookup"><span data-stu-id="84ca9-341">**Item group:** *Audio*</span></span>
    - <span data-ttu-id="84ca9-342">**存储维度组**：*仓库*</span><span class="sxs-lookup"><span data-stu-id="84ca9-342">**Storage dimension group:** *Ware*</span></span>
    - <span data-ttu-id="84ca9-343">**跟踪维度组**：*无*</span><span class="sxs-lookup"><span data-stu-id="84ca9-343">**Tracking dimension group:** *None*</span></span>
    - <span data-ttu-id="84ca9-344">**预留层次结构**：*FlexibleLP*</span><span class="sxs-lookup"><span data-stu-id="84ca9-344">**Reservation hierarchy:** *FlexibleLP*</span></span>

1. <span data-ttu-id="84ca9-345">选择 **确定** 创建产品，然后关闭对话框。</span><span class="sxs-lookup"><span data-stu-id="84ca9-345">Select **OK** to create the product and close the dialog box.</span></span>
1. <span data-ttu-id="84ca9-346">新产品将打开。</span><span class="sxs-lookup"><span data-stu-id="84ca9-346">The new product is opened.</span></span> <span data-ttu-id="84ca9-347">在 **仓库** 快速选项卡上，将 **单位序列组 ID** 字段设置为 *ea*。</span><span class="sxs-lookup"><span data-stu-id="84ca9-347">On the **Warehouse** FastTab, set the **Unit sequence group ID** field to *ea*.</span></span>
1. <span data-ttu-id="84ca9-348">重复上述步骤，创建具有相同设置的第二个产品，但是将 **产品编号** 和 **物料编号** 字段设置为 *Item2*。</span><span class="sxs-lookup"><span data-stu-id="84ca9-348">Repeat the previous steps to create a second product that has the same settings, but set the **Product number** and **Item number** fields to *Item2*.</span></span>
1. <span data-ttu-id="84ca9-349">在操作窗格上的 **管理库存** 选项卡上，在 **视图** 组中，选择 **现有库存量**。</span><span class="sxs-lookup"><span data-stu-id="84ca9-349">On the Action Pane, on the **Manage inventory** tab, in the **View** group, select **On-hand inventory**.</span></span> <span data-ttu-id="84ca9-350">然后选择 **数量调整**。</span><span class="sxs-lookup"><span data-stu-id="84ca9-350">Then select **Quantity adjustment**.</span></span>
1. <span data-ttu-id="84ca9-351">调整下表中指定的新物料的现有库存量。</span><span class="sxs-lookup"><span data-stu-id="84ca9-351">Adjust the on-hand inventory of the new items as specified in the following table.</span></span>

    | <span data-ttu-id="84ca9-352">物料</span><span class="sxs-lookup"><span data-stu-id="84ca9-352">Item</span></span>  | <span data-ttu-id="84ca9-353">存放地点</span><span class="sxs-lookup"><span data-stu-id="84ca9-353">Warehouse</span></span> | <span data-ttu-id="84ca9-354">库位</span><span class="sxs-lookup"><span data-stu-id="84ca9-354">Location</span></span> | <span data-ttu-id="84ca9-355">牌照</span><span class="sxs-lookup"><span data-stu-id="84ca9-355">License plate</span></span> | <span data-ttu-id="84ca9-356">数量</span><span class="sxs-lookup"><span data-stu-id="84ca9-356">Quantity</span></span> |
    |-------|-----------|----------|---------------|----------|
    | <span data-ttu-id="84ca9-357">Item1</span><span class="sxs-lookup"><span data-stu-id="84ca9-357">Item1</span></span> | <span data-ttu-id="84ca9-358">24</span><span class="sxs-lookup"><span data-stu-id="84ca9-358">24</span></span>        | <span data-ttu-id="84ca9-359">FL-010</span><span class="sxs-lookup"><span data-stu-id="84ca9-359">FL-010</span></span>   | <span data-ttu-id="84ca9-360">LP01</span><span class="sxs-lookup"><span data-stu-id="84ca9-360">LP01</span></span>          | <span data-ttu-id="84ca9-361">10</span><span class="sxs-lookup"><span data-stu-id="84ca9-361">10</span></span>       |
    | <span data-ttu-id="84ca9-362">Item1</span><span class="sxs-lookup"><span data-stu-id="84ca9-362">Item1</span></span> | <span data-ttu-id="84ca9-363">24</span><span class="sxs-lookup"><span data-stu-id="84ca9-363">24</span></span>        | <span data-ttu-id="84ca9-364">FL-011</span><span class="sxs-lookup"><span data-stu-id="84ca9-364">FL-011</span></span>   | <span data-ttu-id="84ca9-365">LP02</span><span class="sxs-lookup"><span data-stu-id="84ca9-365">LP02</span></span>          | <span data-ttu-id="84ca9-366">10</span><span class="sxs-lookup"><span data-stu-id="84ca9-366">10</span></span>       |
    | <span data-ttu-id="84ca9-367">Item2</span><span class="sxs-lookup"><span data-stu-id="84ca9-367">Item2</span></span> | <span data-ttu-id="84ca9-368">24</span><span class="sxs-lookup"><span data-stu-id="84ca9-368">24</span></span>        | <span data-ttu-id="84ca9-369">FL-010</span><span class="sxs-lookup"><span data-stu-id="84ca9-369">FL-010</span></span>   | <span data-ttu-id="84ca9-370">LP01</span><span class="sxs-lookup"><span data-stu-id="84ca9-370">LP01</span></span>          | <span data-ttu-id="84ca9-371">5</span><span class="sxs-lookup"><span data-stu-id="84ca9-371">5</span></span>        |
    | <span data-ttu-id="84ca9-372">Item2</span><span class="sxs-lookup"><span data-stu-id="84ca9-372">Item2</span></span> | <span data-ttu-id="84ca9-373">24</span><span class="sxs-lookup"><span data-stu-id="84ca9-373">24</span></span>        | <span data-ttu-id="84ca9-374">FL-011</span><span class="sxs-lookup"><span data-stu-id="84ca9-374">FL-011</span></span>   | <span data-ttu-id="84ca9-375">LP02</span><span class="sxs-lookup"><span data-stu-id="84ca9-375">LP02</span></span>          | <span data-ttu-id="84ca9-376">5</span><span class="sxs-lookup"><span data-stu-id="84ca9-376">5</span></span>        |

    > [!NOTE]
    > <span data-ttu-id="84ca9-377">您必须创建两个牌照并使用允许混合物料的位置，如 *FL-010* 和 *FL-011*。</span><span class="sxs-lookup"><span data-stu-id="84ca9-377">You must create the two license plates and use locations that allow for mixed items, such as *FL-010* and *FL-011*.</span></span>

### <a name="create-a-sales-order-and-reserve-a-specific-license-plate"></a><span data-ttu-id="84ca9-378">创建销售订单并预留特定牌照</span><span class="sxs-lookup"><span data-stu-id="84ca9-378">Create a sales order and reserve a specific license plate</span></span>

1. <span data-ttu-id="84ca9-379">转到 **销售和营销 \> 销售订单 \> 所有销售订单**。</span><span class="sxs-lookup"><span data-stu-id="84ca9-379">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="84ca9-380">选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="84ca9-380">Select **New**.</span></span>
1. <span data-ttu-id="84ca9-381">在 **创建销售订单** 对话框中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="84ca9-381">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="84ca9-382">**客户帐户**：*US-001*</span><span class="sxs-lookup"><span data-stu-id="84ca9-382">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="84ca9-383">**仓库**：*24*</span><span class="sxs-lookup"><span data-stu-id="84ca9-383">**Warehouse:** *24*</span></span>

1. <span data-ttu-id="84ca9-384">选择 **确定** 关闭 **创建销售订单** 对话框并打开新销售订单。</span><span class="sxs-lookup"><span data-stu-id="84ca9-384">Select **OK** to close the **Create sales order** dialog box and open the new sales order.</span></span>
1. <span data-ttu-id="84ca9-385">在 **销售订单行** 快速选项卡上，添加具有以下设置的行：</span><span class="sxs-lookup"><span data-stu-id="84ca9-385">On the **Sales order lines** FastTab, add a line that has the following settings:</span></span>

    - <span data-ttu-id="84ca9-386">**物料编号**：*Item1*</span><span class="sxs-lookup"><span data-stu-id="84ca9-386">**Item number:** *Item1*</span></span>
    - <span data-ttu-id="84ca9-387">**数量：** *10*</span><span class="sxs-lookup"><span data-stu-id="84ca9-387">**Quantity:** *10*</span></span>

1. <span data-ttu-id="84ca9-388">添加第二个具有以下设置的销售订单行：</span><span class="sxs-lookup"><span data-stu-id="84ca9-388">Add a second sales order line that has the following settings:</span></span>

    - <span data-ttu-id="84ca9-389">**物料编号**：*Item2*</span><span class="sxs-lookup"><span data-stu-id="84ca9-389">**Item number:** *Item2*</span></span>
    - <span data-ttu-id="84ca9-390">**数量：** *5*</span><span class="sxs-lookup"><span data-stu-id="84ca9-390">**Quantity:** *5*</span></span>

1. <span data-ttu-id="84ca9-391">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="84ca9-391">Select **Save**.</span></span>
1. <span data-ttu-id="84ca9-392">在 **行详细信息** 快速选项卡上，在 **设置** 选项卡上，记下每行的 **批次 ID** 值。</span><span class="sxs-lookup"><span data-stu-id="84ca9-392">On the **Line details** FastTab, on the **Setup** tab, make a note of the **Lot ID** value for each line.</span></span> <span data-ttu-id="84ca9-393">在预留特定牌照期间将需要这些值。</span><span class="sxs-lookup"><span data-stu-id="84ca9-393">These values will be required during reservation of specific license plates.</span></span>

    > [!NOTE]
    > <span data-ttu-id="84ca9-394">要预留特定牌照，您必须使用 **每个牌照的订单承诺预留** 数据实体。</span><span class="sxs-lookup"><span data-stu-id="84ca9-394">To reserve a specific license plate, you must use the **Order-committed reservations per license plate** data entity.</span></span> <span data-ttu-id="84ca9-395">要在特定牌照上预留批量跟踪物料，您还可以使用 **批次预留** 页面，如[输入销售订单详细信息](#sales-order-details)一节所述。</span><span class="sxs-lookup"><span data-stu-id="84ca9-395">To reserve a batch-tracked item on a specific license plate, you can also use the **Batch reservation** page, as described in the [Enter sales order details](#sales-order-details) section.</span></span>
    >
    > <span data-ttu-id="84ca9-396">如果直接在销售订单行上输入牌照并向系统确认，该行将不使用仓库管理处理。</span><span class="sxs-lookup"><span data-stu-id="84ca9-396">If you enter the license plate directly on the sales order line and confirm it to the system, warehouse management processing won't be used for the line.</span></span>

1. <span data-ttu-id="84ca9-397">选择 **在 Microsoft Office 中打开**，选择 **每个牌照的订单承诺预留**，然后下载文件。</span><span class="sxs-lookup"><span data-stu-id="84ca9-397">Select **Open in Microsoft Office**, select **Order-committed reservations per license plate**, and download the file.</span></span>
1. <span data-ttu-id="84ca9-398">在 Excel 中打开下载的文件，选择 **启用编辑** 启用要运行的 Excel 加载项。</span><span class="sxs-lookup"><span data-stu-id="84ca9-398">Open the downloaded file in Excel, and select **Enable editing** to enable the Excel add-in to run.</span></span>
1. <span data-ttu-id="84ca9-399">如果首次运行此 Excel 加载项，则选择 **信任此加载项**。</span><span class="sxs-lookup"><span data-stu-id="84ca9-399">If you're running the Excel add-in for the first time, select **Trust this Add-in**.</span></span>
1. <span data-ttu-id="84ca9-400">如果系统提示您登录，选择 **登录**，然后使用用于登录 Supply Chain Management 的相同凭据登录。</span><span class="sxs-lookup"><span data-stu-id="84ca9-400">If you're prompted to sign in, select **Sign in**, and then sign in by using the same credentials that you used to sign in to Supply Chain Management.</span></span>
1. <span data-ttu-id="84ca9-401">要在特定牌照上预留物料，在 Excel 加载项中，选择 **新建** 添加预留行，然后设置以下值：</span><span class="sxs-lookup"><span data-stu-id="84ca9-401">To reserve an item on a specific license plate, in the Excel add-in, select **New** to add a reservation line, and then set the following values:</span></span>

    - <span data-ttu-id="84ca9-402">**批次 ID：** 输入您找到的 *Item1* 的销售订单行的 **批次 ID** 值。</span><span class="sxs-lookup"><span data-stu-id="84ca9-402">**Lot ID:** Enter the **Lot ID** value that you found for the sales order line for *Item1*.</span></span>
    - <span data-ttu-id="84ca9-403">**牌照**：*LP02*</span><span class="sxs-lookup"><span data-stu-id="84ca9-403">**License plate:** *LP02*</span></span>
    - <span data-ttu-id="84ca9-404">**预留库存数量**：*10*</span><span class="sxs-lookup"><span data-stu-id="84ca9-404">**ReservedInventoryQuantity:** *10*</span></span>

1. <span data-ttu-id="84ca9-405">选择 **新建** 再添加一个预留行，然后设置以下值：</span><span class="sxs-lookup"><span data-stu-id="84ca9-405">Select **New** to add another reservation line, and set the following values:</span></span>

    - <span data-ttu-id="84ca9-406">**批次 ID：** 输入您找到的 *Item2* 的销售订单行的 **批次 ID** 值。</span><span class="sxs-lookup"><span data-stu-id="84ca9-406">**Lot ID:** Enter the **Lot ID** value you found for the sales order line for *Item2*.</span></span>
    - <span data-ttu-id="84ca9-407">**牌照**：*LP02*</span><span class="sxs-lookup"><span data-stu-id="84ca9-407">**License plate:** *LP02*</span></span>
    - <span data-ttu-id="84ca9-408">**预留库存数量**：*5*</span><span class="sxs-lookup"><span data-stu-id="84ca9-408">**ReservedInventoryQuantity:** *5*</span></span>

1. <span data-ttu-id="84ca9-409">在 Excel 加载项中，选择 **发布** 将数据发送回 Supply Chain Management。</span><span class="sxs-lookup"><span data-stu-id="84ca9-409">In the Excel add-in, select **Publish** to send the data back to Supply Chain Management.</span></span>

    > [!NOTE]
    > <span data-ttu-id="84ca9-410">仅当发布完成且没有错误时，预留行才会出现在系统中。</span><span class="sxs-lookup"><span data-stu-id="84ca9-410">The reservation line will appear in the system only if publishing is completed without errors.</span></span>

1. <span data-ttu-id="84ca9-411">返回 Supply Chain Management。</span><span class="sxs-lookup"><span data-stu-id="84ca9-411">Go back to Supply Chain Management.</span></span> 
1. <span data-ttu-id="84ca9-412">要查看物料的预留，在 **销售订单行** 快速选项卡上，在 **库存** 菜单上，选择 **维护 \> 预留**。</span><span class="sxs-lookup"><span data-stu-id="84ca9-412">To review the item's reservation, on the **Sales order lines** FastTab, on the **Inventory** menu, select **Maintain \> Reservation**.</span></span> <span data-ttu-id="84ca9-413">请注意，在 *Item1* 的销售订单行上，预留了 *10* 库存，在 *Item2* 的销售订单行上，预留了 *5* 库存。</span><span class="sxs-lookup"><span data-stu-id="84ca9-413">Notice that, for the sales order line for *Item1*, inventory of *10* is reserved, and for the sales order line for *Item2*, inventory of *5* is reserved.</span></span>
1. <span data-ttu-id="84ca9-414">要查看与销售订单行预留相关的库存交易记录，在 **销售订单行** 快速选项卡上，在 **库存** 菜单上，选择 **视图 \> 交易记录**。</span><span class="sxs-lookup"><span data-stu-id="84ca9-414">To review inventory transactions that are related to the sales order line reservation, on the **Sales order lines** FastTab, on the **Inventory** menu, select **View \> Transactions**.</span></span> <span data-ttu-id="84ca9-415">请注意，有两条与预留相关的交易记录：一条的 **引用** 字段设置为 *销售订单*，另一条的 **引用** 字段设置为 *订单承诺预留*。</span><span class="sxs-lookup"><span data-stu-id="84ca9-415">Notice that there are two transactions that are related to the reservation: one where the **Reference** field is set to *Sales order* and one where the **Reference** field is set to *Order-committed reservation*.</span></span>

    > [!NOTE]
    > <span data-ttu-id="84ca9-416">**引用** 字段设置为 *销售订单* 的交易记录，表示 **位置** 级别以上（站点、仓库和库存状态）的库存维度的订单行预留。</span><span class="sxs-lookup"><span data-stu-id="84ca9-416">A transaction where the **Reference** field is set to *Sales order* represents the order line reservation for inventory dimensions that are above the **Location** level (site, warehouse, and inventory status).</span></span> <span data-ttu-id="84ca9-417">**引用** 字段设置为 *订单承诺预留* 的交易记录表示特定牌照和位置的订单行预留。</span><span class="sxs-lookup"><span data-stu-id="84ca9-417">A transaction where the **Reference** field is set to *Order-committed reservation* represents the order line reservation for the specific license plate and location.</span></span>

1. <span data-ttu-id="84ca9-418">要发放销售订单，在操作窗格上，在 **仓库** 选项卡上的 **操作** 组中，选择 **发放到仓库**。</span><span class="sxs-lookup"><span data-stu-id="84ca9-418">To release the sales order, on the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>

### <a name="review-and-process-warehouse-work-with-order-committed-license-plates-assigned"></a><span data-ttu-id="84ca9-419">查看和处理分配了订单承诺牌照的仓库工作</span><span class="sxs-lookup"><span data-stu-id="84ca9-419">Review and process warehouse work with order-committed license plates assigned</span></span>

1. <span data-ttu-id="84ca9-420">在 **销售订单行** 快速选项卡上的 **仓库** 菜单中，选择 **工作详细信息**。</span><span class="sxs-lookup"><span data-stu-id="84ca9-420">On the **Sales order lines** FastTab, on the **Warehouse** menu, select **Work details**.</span></span>

    <span data-ttu-id="84ca9-421">与为特定批次完成预留时一样，系统在为使用牌照预留的销售订单创建工作时不使用位置指令。</span><span class="sxs-lookup"><span data-stu-id="84ca9-421">As when reservation is done for a specific batch, the system doesn't use location directives when it creates the work for the sales order that uses license plate reservation.</span></span> <span data-ttu-id="84ca9-422">由于订单承诺预留指定所有库存维度，包括位置，因此不必使用位置指令，因为这些库存维度仅在工作中输入。</span><span class="sxs-lookup"><span data-stu-id="84ca9-422">Because the order-committed reservation specifies all the inventory dimensions, including the location, location directives don't have to be used, because those inventory dimensions are just entered in the work.</span></span> <span data-ttu-id="84ca9-423">它们将显示在 **工作库存交易记录** 页面的 **来自库存维度** 部分。</span><span class="sxs-lookup"><span data-stu-id="84ca9-423">They are shown in the **From inventory dimensions** section on the **Work inventory transactions** page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="84ca9-424">创建工作后，**引用** 字段设置为 *订单承诺预留* 的物料的库存交易记录将删除。</span><span class="sxs-lookup"><span data-stu-id="84ca9-424">After the work is created, the item's inventory transaction where the **Reference** field is set to *Order-committed reservation* is removed.</span></span> <span data-ttu-id="84ca9-425">**引用** 字段设置为 *工作* 的库存交易记录现在保留所有数量的库存维度的实际预留。</span><span class="sxs-lookup"><span data-stu-id="84ca9-425">The inventory transaction where the **Reference** field is set to *Work* now holds the physical reservation for all the quantity's inventory dimensions.</span></span>

1. <span data-ttu-id="84ca9-426">在移动设备上，使用已选中 **按牌照处理** 复选框的菜单项完成领料和放置工作。</span><span class="sxs-lookup"><span data-stu-id="84ca9-426">On the mobile device, finish picking and putting the work by using a menu item where the **Handle by license plate** check box is selected.</span></span>

    > [!NOTE]
    > <span data-ttu-id="84ca9-427">**按牌照处理** 功能可帮助您处理整个牌照。</span><span class="sxs-lookup"><span data-stu-id="84ca9-427">The **Handle by license plate** functionality helps you process the whole license plate.</span></span> <span data-ttu-id="84ca9-428">如果必须处理牌照的一部分，则无法使用此功能。</span><span class="sxs-lookup"><span data-stu-id="84ca9-428">If you must process part of the license plate, you can't use this functionality.</span></span>
    >
    > <span data-ttu-id="84ca9-429">我们建议您为每个牌照生成单独的工作。</span><span class="sxs-lookup"><span data-stu-id="84ca9-429">We recommend that you have separate work generated for each license plate.</span></span> <span data-ttu-id="84ca9-430">要达到此目的，使用 **工作模板** 页上的 **工作标题分行符** 功能。</span><span class="sxs-lookup"><span data-stu-id="84ca9-430">To achieve this result, use the **Work header breaks** feature on the **Work template** page.</span></span>

    <span data-ttu-id="84ca9-431">牌照 *LP02* 现在已为销售订单行领取，并放到 *货架门* 位置。</span><span class="sxs-lookup"><span data-stu-id="84ca9-431">License plate *LP02* is now picked for sales order lines and put to the *Baydoor* location.</span></span> <span data-ttu-id="84ca9-432">此时，可以将其装载并发往客户。</span><span class="sxs-lookup"><span data-stu-id="84ca9-432">At this point, it's ready to be loaded and dispatched to the customer.</span></span>

## <a name="exception-handling-of-warehouse-work-that-has-order-committed-batch-numbers"></a><span data-ttu-id="84ca9-433">具有订单承诺批号的仓库工作的异常处理</span><span class="sxs-lookup"><span data-stu-id="84ca9-433">Exception handling of warehouse work that has order-committed batch numbers</span></span>

<span data-ttu-id="84ca9-434">领取订单承诺批号的仓库工作与常规工作一样，都要接受相同的标准仓库异常处理和操作。</span><span class="sxs-lookup"><span data-stu-id="84ca9-434">Warehouse work for picking order-committed batch numbers is subject to the same standard warehouse exception handling and actions as regular work.</span></span> <span data-ttu-id="84ca9-435">通常，未结工作或工作行可以被取消，可以因为用户货位已满而中断，可以存在领料短缺，并可以由于移动而更新。</span><span class="sxs-lookup"><span data-stu-id="84ca9-435">In general, the open work or work line can be canceled, it can be interrupted because a user location is full, it can be short-picked, and it can be updated because of a movement.</span></span> <span data-ttu-id="84ca9-436">同样，已领取的已完成工作的数量可以减少，或工作可以冲销。</span><span class="sxs-lookup"><span data-stu-id="84ca9-436">Likewise, the picked quantity of work that has already been completed can be reduced, or the work can be reversed.</span></span>

<span data-ttu-id="84ca9-437">以下关键规则应用于所有这些异常处理操作：为客户预留的批号永远不能替换为其他批号，但是可以通过用户手动更新或系统自动更新来更改其存储维度（货位和牌照）。</span><span class="sxs-lookup"><span data-stu-id="84ca9-437">The following key rule is applied to all these exception handling actions: the batch number that was reserved for the customer can never be replaced with a different batch number, but its storage dimensions (location and license plate) can be changed through either a manual update by the user or an automatic update by the system.</span></span> <span data-ttu-id="84ca9-438">自动更新基于对存储维度的随机分配，其与在自动预留特定批次但未指定存储维度时应用的方法相同。</span><span class="sxs-lookup"><span data-stu-id="84ca9-438">The automatic update is based on the same random assignment of storage dimensions that applied when a specific batch was automatically reserved but no storage dimensions were specified.</span></span>

### <a name="example-scenario"></a><span data-ttu-id="84ca9-439">示例场景</span><span class="sxs-lookup"><span data-stu-id="84ca9-439">Example scenario</span></span>

<span data-ttu-id="84ca9-440">这种情形的一个示例是：之前完成的工作未通过使用 **减少领料数量** 功能领取。</span><span class="sxs-lookup"><span data-stu-id="84ca9-440">An example of this scenario is a situation where previously completed work is being unpicked by using the **Reduce picked quantity** function.</span></span> <span data-ttu-id="84ca9-441">本示例假定您已经完成[示例方案：批号分配](#Example-batch-allocation)中所述的步骤。</span><span class="sxs-lookup"><span data-stu-id="84ca9-441">This example assumes that you've already completed the steps that are described in [Example scenario: Batch number allocation](#Example-batch-allocation).</span></span> <span data-ttu-id="84ca9-442">与该示例具有连续性。</span><span class="sxs-lookup"><span data-stu-id="84ca9-442">It continues from that example.</span></span>

1. <span data-ttu-id="84ca9-443">转到 **仓库管理** \> **负荷** \> **有效负荷**。</span><span class="sxs-lookup"><span data-stu-id="84ca9-443">Go to **Warehouse management** \> **Loads** \> **Active loads**.</span></span>
2. <span data-ttu-id="84ca9-444">选择创建的与销售订单的装运相关的负荷。</span><span class="sxs-lookup"><span data-stu-id="84ca9-444">Select the load that was created in connection with the shipment of your sales order.</span></span>
3. <span data-ttu-id="84ca9-445">从 **负荷订单行** 快速选项卡，选择 **减少领料数量**。</span><span class="sxs-lookup"><span data-stu-id="84ca9-445">From the **Load order lines** FastTab, select **Reduce picked quantity**.</span></span>
4. <span data-ttu-id="84ca9-446">在 **减少领料数量** 页面，在 **移到货位** 字段中，选择 **FL-001**。</span><span class="sxs-lookup"><span data-stu-id="84ca9-446">On the **Reduce picked quantity** page, in the **Move to location** field, select **FL-001**.</span></span>
5. <span data-ttu-id="84ca9-447">在 **移到牌照** 字段中，选择 **LP33**。</span><span class="sxs-lookup"><span data-stu-id="84ca9-447">In the **Move to license plate** field, select **LP33**.</span></span>
6. <span data-ttu-id="84ca9-448">在网格中，在 **要取消领料的库存数量** 字段中，输入 **10**。</span><span class="sxs-lookup"><span data-stu-id="84ca9-448">In the grid, in the **Inventory quantity to unpick** field, enter **10**.</span></span>
7. <span data-ttu-id="84ca9-449">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="84ca9-449">Select **OK**.</span></span>

<span data-ttu-id="84ca9-450">这是取消领料操作的结果：</span><span class="sxs-lookup"><span data-stu-id="84ca9-450">Here are the results of the unpicking action:</span></span>

- <span data-ttu-id="84ca9-451">先前结束的工作的状态设置为 **已取消**。</span><span class="sxs-lookup"><span data-stu-id="84ca9-451">The status of the previously closed work is set to **Canceled**.</span></span>
- <span data-ttu-id="84ca9-452">为批号 **B11** 的取消领料的数量 **10** 创建了 **库存变动** 类型的新工作。</span><span class="sxs-lookup"><span data-stu-id="84ca9-452">New work of the **Inventory movement** type is created for the unpicked quantity of **10** for batch number **B11**.</span></span> <span data-ttu-id="84ca9-453">此工作代表从 **Baydoor** 货位到 **FL-001** 货位中的牌照 **LP33** 的移动。</span><span class="sxs-lookup"><span data-stu-id="84ca9-453">This work represents the movement from the **Baydoor** location to license plate **LP33** in location **FL-001**.</span></span> <span data-ttu-id="84ca9-454">状态设置为 **已结束**。</span><span class="sxs-lookup"><span data-stu-id="84ca9-454">The status is set to **Closed**.</span></span>
- <span data-ttu-id="84ca9-455">系统将重新预留最初订购的批号，并分配货位和牌照 ID。</span><span class="sxs-lookup"><span data-stu-id="84ca9-455">The system re-reserves the batch number that was originally ordered, and assigns the location and license plate IDs.</span></span> <span data-ttu-id="84ca9-456">（此流程等效于为给定批号的订单行运行 **预留行** 功能）。</span><span class="sxs-lookup"><span data-stu-id="84ca9-456">(This process is equivalent to running the **Reserve line** function for the order line for a given batch number).</span></span> <span data-ttu-id="84ca9-457">结果是，批次 **B11** 在 **批次预留** 页的 **提交到源行的批号** 快速选项卡上显示为已提交，**预留** 字段包含批号 **B11** 的数量 **10**。</span><span class="sxs-lookup"><span data-stu-id="84ca9-457">As a result, batch **B11** is shown as committed on the **Batch numbers committed to source line** FastTab of the **Batch reservation** page, and the **Reservation** field contains a quantity of **10** for batch number **B11**.</span></span> <span data-ttu-id="84ca9-458">此外，**货位** 字段设置为 **FL-001**，**牌照** 字段设置为 **LP11**。</span><span class="sxs-lookup"><span data-stu-id="84ca9-458">Additionally, the **Location** field is set to **FL-001**, and the **License plate** field is set to **LP11**.</span></span> <span data-ttu-id="84ca9-459">（如果这些字段不可见，您可以将它们添加到网格中。）</span><span class="sxs-lookup"><span data-stu-id="84ca9-459">(You can add these fields to the grid if they aren't visible.)</span></span>

<span data-ttu-id="84ca9-460">下表提供了显示系统如何处理特定仓库操作的订单承诺批次预留的概览。</span><span class="sxs-lookup"><span data-stu-id="84ca9-460">The following tables provide an overview that shows how the system handles order-committed batch reservation for specific warehouse actions.</span></span> <span data-ttu-id="84ca9-461">为了解释表中的内容，假定每个仓库操作都在源于订单承诺批次预留的现有仓库工作的上下文中运行，或者每个仓库操作的执行都会影响该类型的工作。</span><span class="sxs-lookup"><span data-stu-id="84ca9-461">To interpret the content in the tables, assume that each warehouse action is run in the context of existing warehouse work that originates from an order-committed batch reservation, or that execution of each warehouse action affects work of that type.</span></span>

> [!NOTE]
> <span data-ttu-id="84ca9-462">在这些表中，“批次数量可用”列指示，除为当前的订单承诺预留已预留的数量，或由源于该类型预留的仓库工作已预留的数量之外，批次数量是否可用。</span><span class="sxs-lookup"><span data-stu-id="84ca9-462">In these tables, the "Batch quantity is available" column indicates whether a batch quantity is available in addition to the quantity that is either already reserved for the current order-committed reservations or already reserved by the warehouse work that originates from reservations of that type.</span></span>

#### <a name="override-the-pick-location-on-the-open-work"></a><span data-ttu-id="84ca9-463">覆盖未结工作上的领料货位</span><span class="sxs-lookup"><span data-stu-id="84ca9-463">Override the pick location on the open work</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="84ca9-464">关键设置参数</span><span class="sxs-lookup"><span data-stu-id="84ca9-464">Key setup parameter</span></span></th>
<th><span data-ttu-id="84ca9-465">批次数量可用</span><span class="sxs-lookup"><span data-stu-id="84ca9-465">Batch quantity is available</span></span></th>
<th><span data-ttu-id="84ca9-466">关键用户步骤</span><span class="sxs-lookup"><span data-stu-id="84ca9-466">Key user steps</span></span></th>
<th><span data-ttu-id="84ca9-467">仓库工作</span><span class="sxs-lookup"><span data-stu-id="84ca9-467">Warehouse work</span></span></th>
<th><span data-ttu-id="84ca9-468">订单承诺批次预留</span><span class="sxs-lookup"><span data-stu-id="84ca9-468">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="84ca9-469"><strong>允许领料库位覆盖</strong>在工作人员上已启用。</span><span class="sxs-lookup"><span data-stu-id="84ca9-469">The <strong>Allow pick location override</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="84ca9-470">是</span><span class="sxs-lookup"><span data-stu-id="84ca9-470">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="84ca9-471">开始领料工作时，在仓库管理移动应用上选择<strong>替代库位</strong>菜单项。</span><span class="sxs-lookup"><span data-stu-id="84ca9-471">Select the <strong>Override location</strong> menu item on the Warehouse Management mobile app when you start picking work.</span></span></li>
<li><span data-ttu-id="84ca9-472">选择<strong>建议</strong>。</span><span class="sxs-lookup"><span data-stu-id="84ca9-472">Select <strong>Suggest</strong>.</span></span></li>
<li><span data-ttu-id="84ca9-473">根据批次数量的可用性确认建议的新货位。</span><span class="sxs-lookup"><span data-stu-id="84ca9-473">Confirm the new location that is suggested based on batch quantity availability.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="84ca9-474">在当前工作上，将发生以下操作：</span><span class="sxs-lookup"><span data-stu-id="84ca9-474">On the current work, the following actions occur:</span></span>
<ul>
<li><span data-ttu-id="84ca9-475">领料行上的货位已更新为新货位。</span><span class="sxs-lookup"><span data-stu-id="84ca9-475">The location on the pick line is updated to the new location.</span></span> <span data-ttu-id="84ca9-476">（如果货位是由牌照控制的，将为工作库存交易记录分配一个随机牌照，工作人员可以从任何具有可用数量的牌照领料。）</span><span class="sxs-lookup"><span data-stu-id="84ca9-476">(If the location is license plate–controlled, a random license plate is assigned to the work inventory transaction, and the worker can pick from any license plate that has available quantity.)</span></span></li>
<li><span data-ttu-id="84ca9-477">如果在新货位的一个以上牌照中找到数量，原始领料行将拆分成多行以匹配每个牌照。</span><span class="sxs-lookup"><span data-stu-id="84ca9-477">If the quantity is found on more than one license plate in the new location, the original pick line is split into multiple lines to match each license plate.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="84ca9-478">不适用</span><span class="sxs-lookup"><span data-stu-id="84ca9-478">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="84ca9-479">无</span><span class="sxs-lookup"><span data-stu-id="84ca9-479">No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="84ca9-480">开始领料工作时，在仓库管理移动应用上选择<strong>替代库位</strong>菜单项。</span><span class="sxs-lookup"><span data-stu-id="84ca9-480">Select the <strong>Override location</strong> menu item on the Warehouse Management mobile app when you start picking work.</span></span></li>
<li><span data-ttu-id="84ca9-481">手动输入货位。</span><span class="sxs-lookup"><span data-stu-id="84ca9-481">Manually enter a location.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="84ca9-482"><strong>覆盖货位</strong>操作无法执行。</span><span class="sxs-lookup"><span data-stu-id="84ca9-482">The <strong>Override location</strong> action isn't possible.</span></span> <span data-ttu-id="84ca9-483">操作失败，并引发错误。</span><span class="sxs-lookup"><span data-stu-id="84ca9-483">It fails, and an error is thrown.</span></span></td>
<td><span data-ttu-id="84ca9-484">不适用</span><span class="sxs-lookup"><span data-stu-id="84ca9-484">Not applicable</span></span></td>
</tr>
</tbody>
</table>

#### <a name="full-button--split-a-work-line-because-of-overflow-on-the-user-location"></a><span data-ttu-id="84ca9-485">“全部”按钮 – 工作行由于用户货位存在溢出被拆分</span><span class="sxs-lookup"><span data-stu-id="84ca9-485">Full button – Split a work line because of overflow on the user location</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="84ca9-486">关键设置参数</span><span class="sxs-lookup"><span data-stu-id="84ca9-486">Key setup parameter</span></span></th>
<th><span data-ttu-id="84ca9-487">批次数量可用</span><span class="sxs-lookup"><span data-stu-id="84ca9-487">Batch quantity is available</span></span></th>
<th><span data-ttu-id="84ca9-488">关键用户步骤</span><span class="sxs-lookup"><span data-stu-id="84ca9-488">Key user steps</span></span></th>
<th><span data-ttu-id="84ca9-489">仓库工作</span><span class="sxs-lookup"><span data-stu-id="84ca9-489">Warehouse work</span></span></th>
<th><span data-ttu-id="84ca9-490">订单承诺批次预留</span><span class="sxs-lookup"><span data-stu-id="84ca9-490">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="84ca9-491"><strong>允许拆分工作</strong>选项在移动设备菜单项上启用。</span><span class="sxs-lookup"><span data-stu-id="84ca9-491">The <strong>Allow splitting of work</strong> option is enabled on the mobile device menu item.</span></span></td>
<td><span data-ttu-id="84ca9-492">不适用</span><span class="sxs-lookup"><span data-stu-id="84ca9-492">Not applicable</span></span></td>
<td>
<ol>
<li><span data-ttu-id="84ca9-493">处理领料工作时，在仓库管理移动应用上选择<strong>完全</strong>菜单项。</span><span class="sxs-lookup"><span data-stu-id="84ca9-493">Select the <strong>Full</strong> menu item on the Warehouse Management mobile app when you process picking work.</span></span></li>
<li><span data-ttu-id="84ca9-494">在<strong>领料数量</strong>字段中，输入需要领料的部分数量来指示全部产能。</span><span class="sxs-lookup"><span data-stu-id="84ca9-494">In the <strong>Pick Qty</strong> field, enter a partial quantity of the required pick to indicate the full capacity.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="84ca9-495">在当前工作上，数量更新为必须领料的剩余数量。</span><span class="sxs-lookup"><span data-stu-id="84ca9-495">On the current work, the quantity is updated to the remaining quantity that must be picked.</span></span></li>
<li><span data-ttu-id="84ca9-496">领料数量的新工作已创建并结束。</span><span class="sxs-lookup"><span data-stu-id="84ca9-496">New work for the picked quantity is created and closed.</span></span></li>
</ul></td>
<td><span data-ttu-id="84ca9-497">不适用</span><span class="sxs-lookup"><span data-stu-id="84ca9-497">Not applicable</span></span></td>
</tr>
</tbody>
</table>

#### <a name="reduce-the-picked-quantity-of-completed-work-from-a-load"></a><span data-ttu-id="84ca9-498">减少已完成工作的领料数量（从负荷）</span><span class="sxs-lookup"><span data-stu-id="84ca9-498">Reduce the picked quantity of completed work (from a load)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="84ca9-499">关键设置参数</span><span class="sxs-lookup"><span data-stu-id="84ca9-499">Key setup parameter</span></span></th>
<th><span data-ttu-id="84ca9-500">批次数量可用</span><span class="sxs-lookup"><span data-stu-id="84ca9-500">Batch quantity is available</span></span></th>
<th><span data-ttu-id="84ca9-501">关键用户步骤</span><span class="sxs-lookup"><span data-stu-id="84ca9-501">Key user steps</span></span></th>
<th><span data-ttu-id="84ca9-502">仓库工作</span><span class="sxs-lookup"><span data-stu-id="84ca9-502">Warehouse work</span></span></th>
<th><span data-ttu-id="84ca9-503">订单承诺批次预留</span><span class="sxs-lookup"><span data-stu-id="84ca9-503">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="84ca9-504">不适用</span><span class="sxs-lookup"><span data-stu-id="84ca9-504">Not applicable</span></span></td>
<td><span data-ttu-id="84ca9-505">是</span><span class="sxs-lookup"><span data-stu-id="84ca9-505">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="84ca9-506">从负荷行打开<strong>减少领料数量</strong>页面。</span><span class="sxs-lookup"><span data-stu-id="84ca9-506">Open the <strong>Reduce picked quantity</strong> page from the load line.</span></span></li>
<li><span data-ttu-id="84ca9-507">输入要取消领料的全部数量。</span><span class="sxs-lookup"><span data-stu-id="84ca9-507">Enter the full quantity to unpick.</span></span></li>
<li><span data-ttu-id="84ca9-508">选择“移至”货位/牌照。</span><span class="sxs-lookup"><span data-stu-id="84ca9-508">Select a "move to" location/license plate.</span></span></li>
</ol>
</td>
<td>
<ul> 
<li><span data-ttu-id="84ca9-509">与负荷行关联的工作被取消。</span><span class="sxs-lookup"><span data-stu-id="84ca9-509">Work that is associated with the load line is canceled.</span></span></li>
<li><span data-ttu-id="84ca9-510">库存变动的新工作已创建并结束。</span><span class="sxs-lookup"><span data-stu-id="84ca9-510">New work for the inventory movement is created and closed.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="84ca9-511">为同一批次重新预留了数量。</span><span class="sxs-lookup"><span data-stu-id="84ca9-511">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="84ca9-512">系统随机分配数量可用的货位和牌照（如果货位是由牌照控制的）。</span><span class="sxs-lookup"><span data-stu-id="84ca9-512">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="84ca9-513">否</span><span class="sxs-lookup"><span data-stu-id="84ca9-513">No</span></span></td>
<td><span data-ttu-id="84ca9-514">查看上一行。</span><span class="sxs-lookup"><span data-stu-id="84ca9-514">See the previous row.</span></span></td>
<td><span data-ttu-id="84ca9-515">查看上一行。</span><span class="sxs-lookup"><span data-stu-id="84ca9-515">See the previous row.</span></span></td>
<td><span data-ttu-id="84ca9-516">已为同一批次，以及取消领料期间输入的同一货位和牌照（如果货位是由牌照控制的）重新预留了数量。</span><span class="sxs-lookup"><span data-stu-id="84ca9-516">The quantity is re-reserved for the same batch, and for the same location and license plate (if the location is license plate–controlled) that were entered during unpicking.</span></span></td>
</tr>
</tbody>
</table>

#### <a name="move-an-item-within-a-warehouse"></a><span data-ttu-id="84ca9-517">在仓库内移动物料</span><span class="sxs-lookup"><span data-stu-id="84ca9-517">Move an item within a warehouse</span></span>

> [!NOTE]
> <span data-ttu-id="84ca9-518">此仓库操作仅适用于 **工作创建流程** 类型的移动，不适用于模板移动。</span><span class="sxs-lookup"><span data-stu-id="84ca9-518">This warehouse action is applicable only to movement of the **Work creation process** type, not to movement by template.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="84ca9-519">关键设置参数</span><span class="sxs-lookup"><span data-stu-id="84ca9-519">Key setup parameter</span></span></th>
<th><span data-ttu-id="84ca9-520">批次数量可用</span><span class="sxs-lookup"><span data-stu-id="84ca9-520">Batch quantity is available</span></span></th>
<th><span data-ttu-id="84ca9-521">关键用户步骤</span><span class="sxs-lookup"><span data-stu-id="84ca9-521">Key user steps</span></span></th>
<th><span data-ttu-id="84ca9-522">仓库工作</span><span class="sxs-lookup"><span data-stu-id="84ca9-522">Warehouse work</span></span></th>
<th><span data-ttu-id="84ca9-523">订单承诺批次预留</span><span class="sxs-lookup"><span data-stu-id="84ca9-523">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="84ca9-524"><strong>允许包含关联工作的库存移动</strong>选项在工作人员上启用。</span><span class="sxs-lookup"><span data-stu-id="84ca9-524">The <strong>Allow movement of inventory with associated work</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="84ca9-525">是</span><span class="sxs-lookup"><span data-stu-id="84ca9-525">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="84ca9-526">在仓库管理移动应用上开始移动。</span><span class="sxs-lookup"><span data-stu-id="84ca9-526">Start a movement on the Warehouse Management mobile app.</span></span></li>
<li><span data-ttu-id="84ca9-527">输入“起始”和“目标”货位。</span><span class="sxs-lookup"><span data-stu-id="84ca9-527">Enter "from" and "to" locations.</span></span></li>
</ol></td>
<td>
<ul>
<li><span data-ttu-id="84ca9-528">在受移动影响的所有现有工作上，领料货位将更新为新的“目标”货位。</span><span class="sxs-lookup"><span data-stu-id="84ca9-528">On all existing work that is affected by the move, the pick location is updated to the new "to" location.</span></span></li>
<li><span data-ttu-id="84ca9-529">库存变动的新工作已创建并结束。</span><span class="sxs-lookup"><span data-stu-id="84ca9-529">New work for the inventory movement is created and closed.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="84ca9-530">受从给定货位的数量移动影响的所有现有预留已为同一批次重新预留。</span><span class="sxs-lookup"><span data-stu-id="84ca9-530">All existing reservations that are affected by the quantity movement from the given location are re-reserved for the same batch.</span></span> <span data-ttu-id="84ca9-531">系统随机分配数量可用的货位和牌照（如果货位是由牌照控制的）。</span><span class="sxs-lookup"><span data-stu-id="84ca9-531">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="84ca9-532">否</span><span class="sxs-lookup"><span data-stu-id="84ca9-532">No</span></span></td>
<td><span data-ttu-id="84ca9-533">查看上一行。</span><span class="sxs-lookup"><span data-stu-id="84ca9-533">See the previous row.</span></span></td>
<td><span data-ttu-id="84ca9-534">查看上一行。</span><span class="sxs-lookup"><span data-stu-id="84ca9-534">See the previous row.</span></span></td>
<td><span data-ttu-id="84ca9-535">受从给定货位的数量移动影响的所有现有预留已为同一批次，以及新的“目标”货位和牌照（如果货位是由牌照控制的）重新预留。</span><span class="sxs-lookup"><span data-stu-id="84ca9-535">All existing reservations that are affected by the quantity movement from the given location are re-reserved for the same batch, and for the new "to" location and license plate (if the location is license plate–controlled).</span></span></td>
</tr>
</tbody>
</table>

#### <a name="reverse-the-picked-quantity-of-completed-work-from-a-load-or-a-wave"></a><span data-ttu-id="84ca9-536">冲销已完成工作的领料数量（从负荷或波次）</span><span class="sxs-lookup"><span data-stu-id="84ca9-536">Reverse the picked quantity of completed work (from a load or a wave)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="84ca9-537">关键设置参数</span><span class="sxs-lookup"><span data-stu-id="84ca9-537">Key setup parameter</span></span></th>
<th><span data-ttu-id="84ca9-538">批次数量可用</span><span class="sxs-lookup"><span data-stu-id="84ca9-538">Batch quantity is available</span></span></th>
<th><span data-ttu-id="84ca9-539">关键用户步骤</span><span class="sxs-lookup"><span data-stu-id="84ca9-539">Key user steps</span></span></th>
<th><span data-ttu-id="84ca9-540">仓库工作</span><span class="sxs-lookup"><span data-stu-id="84ca9-540">Warehouse work</span></span></th>
<th><span data-ttu-id="84ca9-541">订单承诺批次预留</span><span class="sxs-lookup"><span data-stu-id="84ca9-541">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='6'><span data-ttu-id="84ca9-542">不适用</span><span class="sxs-lookup"><span data-stu-id="84ca9-542">Not applicable</span></span></td>
<td><span data-ttu-id="84ca9-543">是</span><span class="sxs-lookup"><span data-stu-id="84ca9-543">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="84ca9-544">打开<strong>冲销工作</strong>页面。</span><span class="sxs-lookup"><span data-stu-id="84ca9-544">Open the <strong>Reverse work</strong> page.</span></span></li>
<li><span data-ttu-id="84ca9-545">在请求页面上，选择<strong>将物料留在当前货位</strong>选项。</span><span class="sxs-lookup"><span data-stu-id="84ca9-545">On the request page, select the <strong>Leave items at current location</strong> option.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="84ca9-546">与负荷关联的所有工作被取消。</span><span class="sxs-lookup"><span data-stu-id="84ca9-546">All work that is associated with the load is canceled.</span></span></td>
<td><span data-ttu-id="84ca9-547">为同一批次重新预留了数量。</span><span class="sxs-lookup"><span data-stu-id="84ca9-547">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="84ca9-548">系统随机分配数量可用的货位和牌照（如果货位是由牌照控制的）。</span><span class="sxs-lookup"><span data-stu-id="84ca9-548">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="84ca9-549">否</span><span class="sxs-lookup"><span data-stu-id="84ca9-549">No</span></span></td>
<td><span data-ttu-id="84ca9-550">查看上一行。</span><span class="sxs-lookup"><span data-stu-id="84ca9-550">See the previous row.</span></span></td>
<td><span data-ttu-id="84ca9-551">查看上一行。</span><span class="sxs-lookup"><span data-stu-id="84ca9-551">See the previous row.</span></span></td>
<td><span data-ttu-id="84ca9-552">数量已为同一批次以及在冲销后保留数量的货位和牌照重新预留。</span><span class="sxs-lookup"><span data-stu-id="84ca9-552">The quantity is re-reserved for the same batch, and for the location and license plate where the quantity was left upon reversal.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="84ca9-553">是</span><span class="sxs-lookup"><span data-stu-id="84ca9-553">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="84ca9-554">打开<strong>冲销工作</strong>页面。</span><span class="sxs-lookup"><span data-stu-id="84ca9-554">Open the <strong>Reverse work</strong> page.</span></span></li>
<li><span data-ttu-id="84ca9-555">在请求页面上，选择<strong>将物料分配给此货位</strong>选项。</span><span class="sxs-lookup"><span data-stu-id="84ca9-555">On the request page, select the <strong>Assign items to this location</strong> option.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="84ca9-556">当前工作被取消。</span><span class="sxs-lookup"><span data-stu-id="84ca9-556">The current work is canceled.</span></span></li>
<li><span data-ttu-id="84ca9-557">库存变动的新工作已创建并结束。</span><span class="sxs-lookup"><span data-stu-id="84ca9-557">New work for the inventory movement is created and closed.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="84ca9-558">为同一批次重新预留了数量。</span><span class="sxs-lookup"><span data-stu-id="84ca9-558">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="84ca9-559">系统随机分配数量可用的货位和牌照（如果货位是由牌照控制的）。</span><span class="sxs-lookup"><span data-stu-id="84ca9-559">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="84ca9-560">否</span><span class="sxs-lookup"><span data-stu-id="84ca9-560">No</span></span></td>
<td><span data-ttu-id="84ca9-561">查看上一行。</span><span class="sxs-lookup"><span data-stu-id="84ca9-561">See the previous row.</span></span></td>
<td><span data-ttu-id="84ca9-562">查看上一行。</span><span class="sxs-lookup"><span data-stu-id="84ca9-562">See the previous row.</span></span></td>
<td><span data-ttu-id="84ca9-563">数量已为同一批次以及在冲销后向其分配数量的货位和牌照重新预留。</span><span class="sxs-lookup"><span data-stu-id="84ca9-563">The quantity is re-reserved for the same batch, and for the location and license plate that the quantity was assigned to upon reversal.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="84ca9-564">是/否</span><span class="sxs-lookup"><span data-stu-id="84ca9-564">Yes/No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="84ca9-565">打开<strong>冲销工作</strong>页面。</span><span class="sxs-lookup"><span data-stu-id="84ca9-565">Open the <strong>Reverse work</strong> page.</span></span></li>
<li><span data-ttu-id="84ca9-566">在请求页面上，选择<strong>将物料移到此货位</strong>选项。</span><span class="sxs-lookup"><span data-stu-id="84ca9-566">On the request page, select the <strong>Move items to this location</strong> option.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="84ca9-567">不支持冲销。</span><span class="sxs-lookup"><span data-stu-id="84ca9-567">Reversal isn't supported.</span></span></td>
<td><span data-ttu-id="84ca9-568">不适用</span><span class="sxs-lookup"><span data-stu-id="84ca9-568">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="84ca9-569">是/否</span><span class="sxs-lookup"><span data-stu-id="84ca9-569">Yes/No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="84ca9-570">打开<strong>冲销工作</strong>页面。</span><span class="sxs-lookup"><span data-stu-id="84ca9-570">Open the <strong>Reverse work</strong> page.</span></span></li>
<li><span data-ttu-id="84ca9-571">在请求页面上，选择<strong>根据货位指令移动物料</strong>选项。</span><span class="sxs-lookup"><span data-stu-id="84ca9-571">On the request page, select the <strong>Move items based on location directives</strong> option.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="84ca9-572">不支持冲销。</span><span class="sxs-lookup"><span data-stu-id="84ca9-572">Reversal isn't supported.</span></span> </td>
<td><span data-ttu-id="84ca9-573">不适用</span><span class="sxs-lookup"><span data-stu-id="84ca9-573">Not applicable</span></span></td>
</tr>
</tbody>
</table>

#### <a name="short-pick-a-quantity--register-the-quantity-as-physically-not-found-at-the-locationlicense-plate-while-you-perform-picking-work"></a><span data-ttu-id="84ca9-574">领料短缺数量 – 登记在执行领料工作时，在货位/牌照上实际未找到的数量</span><span class="sxs-lookup"><span data-stu-id="84ca9-574">Short-pick a quantity – Register the quantity as physically not found at the location/license plate while you perform picking work</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="84ca9-575">关键设置参数</span><span class="sxs-lookup"><span data-stu-id="84ca9-575">Key setup parameter</span></span></th>
<th><span data-ttu-id="84ca9-576">批次数量可用</span><span class="sxs-lookup"><span data-stu-id="84ca9-576">Batch quantity is available</span></span></th>
<th><span data-ttu-id="84ca9-577">关键用户步骤</span><span class="sxs-lookup"><span data-stu-id="84ca9-577">Key user steps</span></span></th>
<th><span data-ttu-id="84ca9-578">仓库工作</span><span class="sxs-lookup"><span data-stu-id="84ca9-578">Warehouse work</span></span></th>
<th><span data-ttu-id="84ca9-579">订单承诺批次预留</span><span class="sxs-lookup"><span data-stu-id="84ca9-579">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="84ca9-580">设置<strong>领料短缺</strong>类型的工作异常，其中，<strong>物料重新分配</strong> = <strong>无</strong>，<strong>调整库存</strong> = <strong>是</strong>，<strong>删除预留</strong> = <strong>否</strong>。</span><span class="sxs-lookup"><span data-stu-id="84ca9-580">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>None</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>No</strong>.</span></span></td>
<td><span data-ttu-id="84ca9-581">是</span><span class="sxs-lookup"><span data-stu-id="84ca9-581">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="84ca9-582">运行领料工作时，在仓库管理移动应用上选择<strong>领料不足</strong>菜单项。</span><span class="sxs-lookup"><span data-stu-id="84ca9-582">Select the <strong>Shortpick</strong> menu item on the Warehouse Management mobile app when you run picking work.</span></span></li>
<li><span data-ttu-id="84ca9-583">在<strong>领料数量</strong>字段中，输入<strong>0</strong>（零）。</span><span class="sxs-lookup"><span data-stu-id="84ca9-583">In the <strong>Pick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="84ca9-584">在<strong>原因</strong>字段中，输入<strong>未重新分配</strong>。</span><span class="sxs-lookup"><span data-stu-id="84ca9-584">In the <strong>Reason</strong> field, enter <strong>No reallocation</strong>.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="84ca9-585">当前工作已结束，领料数量为 0（零）。</span><span class="sxs-lookup"><span data-stu-id="84ca9-585">The current work is closed, and the picked quantity is 0 (zero).</span></span></li>
<li><span data-ttu-id="84ca9-586"><strong>盘点</strong>类型和<strong>已售出</strong>发货类型的库存交易记录已创建来表示调整。</span><span class="sxs-lookup"><span data-stu-id="84ca9-586">An inventory transaction of the <strong>Counting</strong> type and the <strong>Sold</strong> issue type is created to represent the adjustment.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="84ca9-587">为同一批次重新预留了数量。</span><span class="sxs-lookup"><span data-stu-id="84ca9-587">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="84ca9-588">系统随机分配数量可用的货位和牌照（如果货位是由牌照控制的）。</span><span class="sxs-lookup"><span data-stu-id="84ca9-588">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="84ca9-589">否</span><span class="sxs-lookup"><span data-stu-id="84ca9-589">No</span></span></td>
<td><span data-ttu-id="84ca9-590">查看上一行。</span><span class="sxs-lookup"><span data-stu-id="84ca9-590">See the previous row.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="84ca9-591">领料短缺操作失败，并引发错误。</span><span class="sxs-lookup"><span data-stu-id="84ca9-591">The short-picking action fails, and an error is thrown.</span></span></li>
<li><span data-ttu-id="84ca9-592">当前工作保持未结状态。</span><span class="sxs-lookup"><span data-stu-id="84ca9-592">The current work remains open.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="84ca9-593">不适用</span><span class="sxs-lookup"><span data-stu-id="84ca9-593">Not applicable</span></span></td>
</tr>
<tr>
<td rowspan='2'><span data-ttu-id="84ca9-594">设置<strong>领料短缺</strong>类型的工作异常，其中，<strong>物料重新分配</strong> = <strong>无</strong>，<strong>调整库存</strong> = <strong>是</strong>，<strong>删除预留</strong> = <strong>是</strong>。</span><span class="sxs-lookup"><span data-stu-id="84ca9-594">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>None</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>Yes</strong>.</span></span></td>
<td><span data-ttu-id="84ca9-595">是</span><span class="sxs-lookup"><span data-stu-id="84ca9-595">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="84ca9-596">运行领料工作时，在仓库管理移动应用上选择<strong>领料不足</strong>菜单项。</span><span class="sxs-lookup"><span data-stu-id="84ca9-596">Select the <strong>Shortpick</strong> menu item on the Warehouse Management mobile app when you run picking work.</span></span></li>
<li><span data-ttu-id="84ca9-597">在<strong>领料数量</strong>字段中，输入<strong>0</strong>（零）。</span><span class="sxs-lookup"><span data-stu-id="84ca9-597">In the <strong>Pick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="84ca9-598">在<strong>原因</strong>字段中，输入<strong>未重新分配</strong>。</span><span class="sxs-lookup"><span data-stu-id="84ca9-598">In the <strong>Reason</strong> field, enter <strong>No reallocation</strong>.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="84ca9-599">当前工作已结束，领料数量为 0（零）。</span><span class="sxs-lookup"><span data-stu-id="84ca9-599">The current work is closed, and the picked quantity is 0 (zero).</span></span></li>
<li><span data-ttu-id="84ca9-600"><strong>盘点</strong>类型和<strong>已售出</strong>发货类型的库存交易记录已创建来表示调整。</span><span class="sxs-lookup"><span data-stu-id="84ca9-600">An inventory transaction of the <strong>Counting</strong> type and the <strong>Sold</strong> issue type is created to represent the adjustment.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="84ca9-601">受领料短缺货位的数量调整影响的所有现有预留已为同一批次重新预留。</span><span class="sxs-lookup"><span data-stu-id="84ca9-601">All existing reservations that are affected by the quantity adjustment in the short-picked location are re-reserved for the same batch.</span></span> <span data-ttu-id="84ca9-602">系统随机分配数量可用的货位和牌照（如果货位是由牌照控制的）。</span><span class="sxs-lookup"><span data-stu-id="84ca9-602">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="84ca9-603">否</span><span class="sxs-lookup"><span data-stu-id="84ca9-603">No</span></span></td>
<td><span data-ttu-id="84ca9-604">查看上一行。</span><span class="sxs-lookup"><span data-stu-id="84ca9-604">See the previous row.</span></span></td>
<td><span data-ttu-id="84ca9-605">查看上一行。</span><span class="sxs-lookup"><span data-stu-id="84ca9-605">See the previous row.</span></span></td>
<td><span data-ttu-id="84ca9-606">受领料短缺货位的数量调整影响的所有现有预留已删除。</span><span class="sxs-lookup"><span data-stu-id="84ca9-606">All existing reservations that are affected by the quantity adjustment in the short-picked location are removed.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="84ca9-607">设置<strong>领料短缺</strong>类型的工作异常，其中，<strong>物料重新分配</strong> = <strong>手动</strong>，<strong>调整库存</strong> = <strong>是</strong>，<strong>删除预留</strong> = <strong>否/是</strong>。</span><span class="sxs-lookup"><span data-stu-id="84ca9-607">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>Manual</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>No/Yes</strong>.</span></span> <span data-ttu-id="84ca9-608">此外，<strong>允许手动重新分配物料</strong>选项在工作人员上启用。</span><span class="sxs-lookup"><span data-stu-id="84ca9-608">Additionally, the <strong>Allow manual item reallocation</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="84ca9-609">是</span><span class="sxs-lookup"><span data-stu-id="84ca9-609">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="84ca9-610">运行领料工作时，在仓库管理移动应用上选择<strong>领料不足</strong>菜单项。</span><span class="sxs-lookup"><span data-stu-id="84ca9-610">Select the <strong>Shortpick</strong> menu item on the Warehouse Management mobile app when you run picking work.</span></span></li>
<li><span data-ttu-id="84ca9-611">在<strong>领料短缺数量</strong>字段中，输入<strong>0</strong>（零）。</span><span class="sxs-lookup"><span data-stu-id="84ca9-611">In the <strong>Shortpick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="84ca9-612">在<strong>原因</strong>字段中，选择<strong>手动重新分配领料短缺</strong>。</span><span class="sxs-lookup"><span data-stu-id="84ca9-612">In the <strong>Reason</strong> field, select <strong>Short Picking with manual reallocation</strong>.</span></span></li>
<li><span data-ttu-id="84ca9-613">在列表中选择货位/牌照。</span><span class="sxs-lookup"><span data-stu-id="84ca9-613">Select the location/license plate in the list.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="84ca9-614">在当前工作上，将发生以下操作：</span><span class="sxs-lookup"><span data-stu-id="84ca9-614">On the current work, the following actions occur:</span></span>
<ul>
<li><span data-ttu-id="84ca9-615">领料行已关闭，领料数量为 0（零）。</span><span class="sxs-lookup"><span data-stu-id="84ca9-615">The pick line is closed, and the picked quantity is 0 (zero).</span></span></li>
<li><span data-ttu-id="84ca9-616">放置行被取消。</span><span class="sxs-lookup"><span data-stu-id="84ca9-616">The put line is canceled.</span></span></li>
<li><span data-ttu-id="84ca9-617">新领料行创建。</span><span class="sxs-lookup"><span data-stu-id="84ca9-617">A new pick line is created.</span></span> <span data-ttu-id="84ca9-618">它使用用户选择的货位/牌照。</span><span class="sxs-lookup"><span data-stu-id="84ca9-618">It uses the location/license plate that the user selected.</span></span></li>
<li><span data-ttu-id="84ca9-619">新放置行创建。</span><span class="sxs-lookup"><span data-stu-id="84ca9-619">A new put line is created.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="84ca9-620"><strong>盘点</strong>类型和<strong>已售出</strong>发货类型的库存交易记录已创建来表示调整。</span><span class="sxs-lookup"><span data-stu-id="84ca9-620">An inventory transaction of the <strong>Counting</strong> type and the <strong>Sold</strong> issue type is created to represent the adjustment.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="84ca9-621">不适用</span><span class="sxs-lookup"><span data-stu-id="84ca9-621">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="84ca9-622">设置<strong>领料短缺</strong>类型的工作异常，其中，<strong>物料重新分配</strong> = <strong>手动</strong>，<strong>调整库存</strong> = <strong>是</strong>，<strong>删除预留</strong> = <strong>否</strong>。</span><span class="sxs-lookup"><span data-stu-id="84ca9-622">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>Manual</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>No</strong>.</span></span> <span data-ttu-id="84ca9-623">此外，<strong>允许手动重新分配物料</strong>选项在工作人员上启用。</span><span class="sxs-lookup"><span data-stu-id="84ca9-623">Additionally, the <strong>Allow manual item reallocation</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="84ca9-624">无</span><span class="sxs-lookup"><span data-stu-id="84ca9-624">No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="84ca9-625">运行领料工作时，在仓库管理移动应用上选择<strong>领料不足</strong>菜单项。</span><span class="sxs-lookup"><span data-stu-id="84ca9-625">Select the <strong>Shortpick</strong> menu item on the Warehouse Management mobile app when you run picking work.</span></span></li>
<li><span data-ttu-id="84ca9-626">在<strong>领料短缺数量</strong>字段中，输入<strong>0</strong>（零）。</span><span class="sxs-lookup"><span data-stu-id="84ca9-626">In the <strong>Shortpick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="84ca9-627">在<strong>原因</strong>字段中，选择<strong>手动重新分配领料短缺</strong>。</span><span class="sxs-lookup"><span data-stu-id="84ca9-627">In the <strong>Reason</strong> field, select <strong>Short Picking with manual reallocation</strong>.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="84ca9-628">领料短缺操作失败，并引发错误。</span><span class="sxs-lookup"><span data-stu-id="84ca9-628">The short-picking action fails, and an error is thrown.</span></span></td>
<td><span data-ttu-id="84ca9-629">不适用</span><span class="sxs-lookup"><span data-stu-id="84ca9-629">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="84ca9-630">设置<strong>领料短缺</strong>类型的工作异常，其中，<strong>物料重新分配</strong> = <strong>手动</strong>，<strong>调整库存</strong> = <strong>是</strong>，<strong>删除预留</strong> = <strong>是</strong>。</span><span class="sxs-lookup"><span data-stu-id="84ca9-630">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>Manual</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>Yes</strong>.</span></span> <span data-ttu-id="84ca9-631">此外，<strong>允许手动重新分配物料</strong>选项在工作人员上启用。</span><span class="sxs-lookup"><span data-stu-id="84ca9-631">Additionally, the <strong>Allow manual item reallocation</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="84ca9-632">无</span><span class="sxs-lookup"><span data-stu-id="84ca9-632">No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="84ca9-633">运行领料工作时，在仓库管理移动应用上选择<strong>领料不足</strong>菜单项。</span><span class="sxs-lookup"><span data-stu-id="84ca9-633">Select the <strong>Shortpick</strong> menu item on the Warehouse Management mobile app when you run picking work.</span></span></li>
<li><span data-ttu-id="84ca9-634">在<strong>领料短缺数量</strong>字段中，输入<strong>0</strong>（零）。</span><span class="sxs-lookup"><span data-stu-id="84ca9-634">In the <strong>Shortpick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="84ca9-635">在<strong>原因</strong>字段中，选择<strong>手动重新分配领料短缺</strong>。</span><span class="sxs-lookup"><span data-stu-id="84ca9-635">In the <strong>Reason</strong> field, select <strong>Short Picking with manual reallocation</strong>.</span></span></li>
<li><span data-ttu-id="84ca9-636">在列表中选择货位/牌照。</span><span class="sxs-lookup"><span data-stu-id="84ca9-636">Select the location/license plate in the list.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="84ca9-637">在当前工作上，将发生以下操作：</span><span class="sxs-lookup"><span data-stu-id="84ca9-637">On the current work, the following actions occur:</span></span>
<ul>
<li><span data-ttu-id="84ca9-638">领料行已关闭，领料数量为 0（零）。</span><span class="sxs-lookup"><span data-stu-id="84ca9-638">The pick line is closed, and the picked quantity is 0 (zero).</span></span></li>
<li><span data-ttu-id="84ca9-639">放置行被取消。</span><span class="sxs-lookup"><span data-stu-id="84ca9-639">The put line is canceled.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="84ca9-640"><strong>盘点</strong>类型和<strong>已售出</strong>发货类型的库存交易记录已创建来表示调整。</span><span class="sxs-lookup"><span data-stu-id="84ca9-640">An inventory transaction of the <strong>Counting</strong> type and the <strong>Sold</strong> issue type is created to represent the adjustment.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="84ca9-641">受领料短缺货位/牌照的数量调整影响的所有现有预留已删除。</span><span class="sxs-lookup"><span data-stu-id="84ca9-641">All existing reservations that are affected by the quantity adjustment in the short-picked location/license plate are removed.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="84ca9-642">设置<strong>领料短缺</strong>类型的工作异常，其中，<strong>物料重新分配</strong> = <strong>自动</strong>，<strong>调整库存</strong> = <strong>是/否</strong>，<strong>删除预留</strong> = <strong>是/否</strong>。</span><span class="sxs-lookup"><span data-stu-id="84ca9-642">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>Automatic</strong>, <strong>Adjust inventory</strong> = <strong>Yes/No</strong>, and <strong>Remove reservations</strong> = <strong>Yes/No</strong>.</span></span></td>
<td><span data-ttu-id="84ca9-643">不适用</span><span class="sxs-lookup"><span data-stu-id="84ca9-643">Not applicable</span></span></td>
<td>
<ol>
<li><span data-ttu-id="84ca9-644">运行领料工作时，在仓库管理移动应用上选择<strong>领料不足</strong>菜单项。</span><span class="sxs-lookup"><span data-stu-id="84ca9-644">Select the <strong>Shortpick</strong> menu item on the Warehouse Management mobile app when you run picking work.</span></span></li>
<li><span data-ttu-id="84ca9-645">在<strong>领料短缺数量</strong>字段中，输入<strong>0</strong>（零）。</span><span class="sxs-lookup"><span data-stu-id="84ca9-645">In the <strong>Shortpick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="84ca9-646">在<strong>原因</strong>字段中，选择<strong>自动重新分配领料短缺</strong>。</span><span class="sxs-lookup"><span data-stu-id="84ca9-646">In the <strong>Reason</strong> field, select <strong>Short Picking with automatic reallocation</strong>.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="84ca9-647">不支持涉及自动重新分配的领料短缺。</span><span class="sxs-lookup"><span data-stu-id="84ca9-647">Short-picking that involves automatic reallocation isn't supported.</span></span></td>
<td><span data-ttu-id="84ca9-648">不支持涉及自动重新分配的领料短缺。</span><span class="sxs-lookup"><span data-stu-id="84ca9-648">Short-picking that involves automatic reallocation isn't supported.</span></span></td>
</tr>
</tbody>
</table>

#### <a name="change-the-inventory-status"></a><span data-ttu-id="84ca9-649">更改库存状态</span><span class="sxs-lookup"><span data-stu-id="84ca9-649">Change the inventory status</span></span>

> [!NOTE]
> <span data-ttu-id="84ca9-650">可以从多个入口点执行此仓库操作。</span><span class="sxs-lookup"><span data-stu-id="84ca9-650">This warehouse action can be performed from multiple entry points.</span></span> <span data-ttu-id="84ca9-651">此处显示的示例使用 **按货位显示的现有量** 页面的 **库存状态更改** 操作。</span><span class="sxs-lookup"><span data-stu-id="84ca9-651">The example that is shown here uses **Inventory status change** action on the **On-hand by location** page.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="84ca9-652">关键设置参数</span><span class="sxs-lookup"><span data-stu-id="84ca9-652">Key setup parameter</span></span></th>
<th><span data-ttu-id="84ca9-653">批次数量可用</span><span class="sxs-lookup"><span data-stu-id="84ca9-653">Batch quantity is available</span></span></th>
<th><span data-ttu-id="84ca9-654">关键用户步骤</span><span class="sxs-lookup"><span data-stu-id="84ca9-654">Key user steps</span></span></th>
<th><span data-ttu-id="84ca9-655">仓库工作</span><span class="sxs-lookup"><span data-stu-id="84ca9-655">Warehouse work</span></span></th>
<th><span data-ttu-id="84ca9-656">订单承诺批次预留</span><span class="sxs-lookup"><span data-stu-id="84ca9-656">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="84ca9-657">在<strong>仓库</strong>选项卡上，在<strong>仓库</strong>记录中，<strong>删除预留和标记</strong>字段设置为<strong>预留</strong>或<strong>标记和预留</strong>。</span><span class="sxs-lookup"><span data-stu-id="84ca9-657">On the <strong>Warehouse</strong> tab, in the <strong>Warehouse</strong> record, the <strong>Remove reservations and markings</strong> field is set to <strong>Reservations</strong> or <strong>Markings and reservations</strong>.</span></span></td>
<td><span data-ttu-id="84ca9-658">是</span><span class="sxs-lookup"><span data-stu-id="84ca9-658">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="84ca9-659">选择特定位置。</span><span class="sxs-lookup"><span data-stu-id="84ca9-659">Select a specific location.</span></span></li>
<li><span data-ttu-id="84ca9-660">选择具有特定物料、货位和牌照的行（如果货位是由牌照控制的）。</span><span class="sxs-lookup"><span data-stu-id="84ca9-660">Select a line that has a specific item, location, and license plate (if the location is license plate–controlled).</span></span></li>
<li><span data-ttu-id="84ca9-661">选择<strong>库存状态更改</strong>。</span><span class="sxs-lookup"><span data-stu-id="84ca9-661">Select <strong>Inventory status change</strong>.</span></span></li>
<li><span data-ttu-id="84ca9-662">将<strong>库存状态</strong>字段设置为<strong>锁定</strong>。</span><span class="sxs-lookup"><span data-stu-id="84ca9-662">Set the <strong>Inventory status</strong> field to <strong>Blocking</strong>.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="84ca9-663">为工作预留的数量不允许库存状态更改。</span><span class="sxs-lookup"><span data-stu-id="84ca9-663">Inventory status changes aren't allowed for quantities that are reserved for work.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="84ca9-664">为同一批次重新预留了数量。</span><span class="sxs-lookup"><span data-stu-id="84ca9-664">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="84ca9-665">系统随机分配数量可用的货位和牌照（如果货位是由牌照控制的）。</span><span class="sxs-lookup"><span data-stu-id="84ca9-665">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></li>
<li><span data-ttu-id="84ca9-666"><strong>库存状态更改</strong>的两个库存交易记录已创建，来表示库存状态维度的更改。</span><span class="sxs-lookup"><span data-stu-id="84ca9-666">Two inventory transactions of the <strong>Inventory status change</strong> type are created to represent the change in the inventory status dimension.</span></span></li>
<li><span data-ttu-id="84ca9-667"><strong>库存锁定</strong>类型和<strong>实际预留</strong>发货类型的库存交易记录已创建，来表示锁定数量的预留。</span><span class="sxs-lookup"><span data-stu-id="84ca9-667">An inventory transaction of the <strong>Inventory blocking</strong> type and the <strong>Reserved physical</strong> issue type is created to represent the reservation of the blocked quantity.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="84ca9-668">否</span><span class="sxs-lookup"><span data-stu-id="84ca9-668">No</span></span></td>
<td><span data-ttu-id="84ca9-669">查看上一行。</span><span class="sxs-lookup"><span data-stu-id="84ca9-669">See the previous row.</span></span></td>
<td><span data-ttu-id="84ca9-670">为工作预留的数量不允许库存状态更改。</span><span class="sxs-lookup"><span data-stu-id="84ca9-670">Inventory status changes aren't allowed for quantities that are reserved for work.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="84ca9-671">预留被删除。</span><span class="sxs-lookup"><span data-stu-id="84ca9-671">The reservation is removed.</span></span></li>
<li><span data-ttu-id="84ca9-672"><strong>库存状态更改</strong>的两个库存交易记录已创建，来表示库存状态维度的更改。</span><span class="sxs-lookup"><span data-stu-id="84ca9-672">Two inventory transactions of the <strong>Inventory status change</strong> type are created to represent the change in the inventory status dimension.</span></span></li>
<li><span data-ttu-id="84ca9-673"><strong>库存锁定</strong>类型和<strong>实际预留</strong>发货类型的库存交易记录已创建，来表示锁定数量的预留。</span><span class="sxs-lookup"><span data-stu-id="84ca9-673">An inventory transaction of the <strong>Inventory blocking</strong> type and the <strong>Reserved physical</strong> issue type is created to represent the reservation of the blocked quantity.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td rowspan='2'><span data-ttu-id="84ca9-674">在<strong>仓库</strong>选项卡上，在<strong>仓库</strong>记录中，<strong>删除预留和标记</strong>字段设置为<strong>无</strong>。</span><span class="sxs-lookup"><span data-stu-id="84ca9-674">On the <strong>Warehouse</strong> tab, in the <strong>Warehouse</strong> record, the <strong>Remove reservations and markings</strong> field is set to <strong>None</strong>.</span></span></td>
<td><span data-ttu-id="84ca9-675">是</span><span class="sxs-lookup"><span data-stu-id="84ca9-675">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="84ca9-676">选择特定位置。</span><span class="sxs-lookup"><span data-stu-id="84ca9-676">Select a specific location.</span></span></li>
<li><span data-ttu-id="84ca9-677">选择具有特定物料、货位和牌照的行（如果货位是由牌照控制的）。</span><span class="sxs-lookup"><span data-stu-id="84ca9-677">Select a line that has a specific item, location, and license plate (if the location is license plate–controlled).</span></span></li>
<li><span data-ttu-id="84ca9-678">选择<strong>库存状态更改</strong>。</span><span class="sxs-lookup"><span data-stu-id="84ca9-678">Select <strong>Inventory status change</strong>.</span></span></li>
<li><span data-ttu-id="84ca9-679">将<strong>库存状态</strong>字段设置为<strong>锁定</strong>。</span><span class="sxs-lookup"><span data-stu-id="84ca9-679">Set the <strong>Inventory status</strong> field to <strong>Blocking</strong>.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="84ca9-680">为工作预留的数量不允许库存状态更改。</span><span class="sxs-lookup"><span data-stu-id="84ca9-680">Inventory status changes aren't allowed for quantities that are reserved for work.</span></span></td>
<td><span data-ttu-id="84ca9-681">为同一批次重新预留了数量。</span><span class="sxs-lookup"><span data-stu-id="84ca9-681">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="84ca9-682">系统随机分配数量可用的货位和牌照（如果货位是由牌照控制的）。</span><span class="sxs-lookup"><span data-stu-id="84ca9-682">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="84ca9-683">否</span><span class="sxs-lookup"><span data-stu-id="84ca9-683">No</span></span></td>
<td><span data-ttu-id="84ca9-684">查看上一行。</span><span class="sxs-lookup"><span data-stu-id="84ca9-684">See the previous row.</span></span></td>
<td><span data-ttu-id="84ca9-685">为工作预留的数量不允许库存状态更改。</span><span class="sxs-lookup"><span data-stu-id="84ca9-685">Inventory status changes aren't allowed for quantities that are reserved for work.</span></span></td>
<td><span data-ttu-id="84ca9-686">不允许库存状态更改。</span><span class="sxs-lookup"><span data-stu-id="84ca9-686">Inventory status changes aren't allowed.</span></span></td>
</tr>
</tbody>
</table>

## <a name="limitations"></a><span data-ttu-id="84ca9-687">限制</span><span class="sxs-lookup"><span data-stu-id="84ca9-687">Limitations</span></span>

- <span data-ttu-id="84ca9-688">灵活的仓库级维度预留功能不支持以下功能：</span><span class="sxs-lookup"><span data-stu-id="84ca9-688">The flexible warehouse-level dimension reservation functionality doesn't support the following features:</span></span>

    - <span data-ttu-id="84ca9-689">实际称重管理</span><span class="sxs-lookup"><span data-stu-id="84ca9-689">Catch weight management</span></span>
    - <span data-ttu-id="84ca9-690">允许实际负库存</span><span class="sxs-lookup"><span data-stu-id="84ca9-690">Physical negative inventory</span></span>
    - <span data-ttu-id="84ca9-691">按订购的供应预留</span><span class="sxs-lookup"><span data-stu-id="84ca9-691">Reservation against ordered supply</span></span>
    - <span data-ttu-id="84ca9-692">转移单和原材料领料</span><span class="sxs-lookup"><span data-stu-id="84ca9-692">Transfer orders and raw material picking</span></span>

- <span data-ttu-id="84ca9-693">按指令单位包装的集装箱合并规则有局限性。</span><span class="sxs-lookup"><span data-stu-id="84ca9-693">The container consolidation rule for packing by directive unit has limitations.</span></span> <span data-ttu-id="84ca9-694">对于订单承诺预留，我们建议您不要在 **按指令单位包装** 字段已启用的情况下使用集装箱生成模板。</span><span class="sxs-lookup"><span data-stu-id="84ca9-694">For order-committed reservations, we recommend that you not use container build templates where the **Pack by directive unit** field is enabled.</span></span> <span data-ttu-id="84ca9-695">在当前的设计中，创建仓库工作时不使用货位指令。</span><span class="sxs-lookup"><span data-stu-id="84ca9-695">In the current design, location directives aren't used when warehouse work is created.</span></span> <span data-ttu-id="84ca9-696">因此，在集装化波次步骤期间，仅应用单位序列组中的最低单位（库存单位）。</span><span class="sxs-lookup"><span data-stu-id="84ca9-696">Therefore, only the lowest unit in the unit sequence group (the inventory unit) is applied during the containerization wave step.</span></span>

## <a name="see-also"></a><span data-ttu-id="84ca9-697">请参阅</span><span class="sxs-lookup"><span data-stu-id="84ca9-697">See also</span></span>

- [<span data-ttu-id="84ca9-698">仓库管理中的批号</span><span class="sxs-lookup"><span data-stu-id="84ca9-698">Batch numbers in Warehouse management</span></span>](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/batch-numbers-in-warehouse-management)
- [<span data-ttu-id="84ca9-699">为销售订单预留相同的批次</span><span class="sxs-lookup"><span data-stu-id="84ca9-699">Reserve the same batch for a sales order</span></span>](../sales-marketing/reserve-same-batch-sales-order.md)
- [<span data-ttu-id="84ca9-700">在移动设备上领取最早的批次</span><span class="sxs-lookup"><span data-stu-id="84ca9-700">Pick oldest batch on a mobile device</span></span>](pick-oldest-batch.md)
- [<span data-ttu-id="84ca9-701">批次和牌照确认</span><span class="sxs-lookup"><span data-stu-id="84ca9-701">Batch and license plate confirmation</span></span>](batch-and-license-plate-confirmation.md)
- [<span data-ttu-id="84ca9-702">仓库管理中的预留疑难解答</span><span class="sxs-lookup"><span data-stu-id="84ca9-702">Troubleshoot reservations in warehouse management</span></span>](troubleshoot-warehouse-reservations.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
