---
title: 灵活的仓库级维度预留策略
description: 本主题介绍一种库存预留策略，其允许销售批量跟踪产品并且以启用 WMS 的操作运行物流的企业为客户销售订单预留特定批次，即使与产品相关联的预留层次结构不允许预留特定批次。
author: omulvad
manager: AnnBe
ms.date: 02/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSReservationHierarchy
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2020-01-15
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: cd6ec1013de757214db99ada02170bb6e2af96c0
ms.sourcegitcommit: f52ddcad105aac4ad2caef709751ff80caf363c0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/11/2020
ms.locfileid: "3036921"
---
# <a name="flexible-warehouse-level-dimension-reservation-policy"></a><span data-ttu-id="97bfe-103">灵活的仓库级维度预留策略</span><span class="sxs-lookup"><span data-stu-id="97bfe-103">Flexible warehouse-level dimension reservation policy</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="97bfe-104">当产品与“Batch-below\[location\]”类型的库存预留层次结构关联时，销售批次跟踪产品并以启用 Microsoft Dynamics 365 仓库管理系统 (WMS) 的操作运行物流的企业，不能为客户销售订单保留这些产品的特定批次。</span><span class="sxs-lookup"><span data-stu-id="97bfe-104">When an inventory reservation hierarchy of the "Batch-below\[location\]" type is associated with products, businesses that sell batch-tracked products and run their logistics as operations that are enabled for the Microsoft Dynamics 365 Warehouse Management System (WMS) can't reserve specific batches of those products for customer sales orders.</span></span> <span data-ttu-id="97bfe-105">本主题介绍一种库存预留策略，能够让这些企业预留特定批次，即使产品与“Batch-below\[location\]”预留层次结构关联。</span><span class="sxs-lookup"><span data-stu-id="97bfe-105">This topic describes the inventory reservation policy that lets these businesses reserve specific batches, even when the products are associated with a "Batch-below\[location\]" reservation hierarchy.</span></span>

## <a name="inventory-reservation-hierarchy"></a><span data-ttu-id="97bfe-106">库存预留层次结构</span><span class="sxs-lookup"><span data-stu-id="97bfe-106">Inventory reservation hierarchy</span></span>

<span data-ttu-id="97bfe-107">本节总结了现有的库存预留层次结构。</span><span class="sxs-lookup"><span data-stu-id="97bfe-107">This section summarizes the existing inventory reservation hierarchy.</span></span> <span data-ttu-id="97bfe-108">着重介绍批次跟踪和序列跟踪物料的处理方式。</span><span class="sxs-lookup"><span data-stu-id="97bfe-108">It focuses on the way that batch-tracked and serial-tracked items are handled.</span></span>

<span data-ttu-id="97bfe-109">库存预留层次结构指示，就存储维度而言，需求订单包含站点、仓库和库存状态的必需维度，而仓库逻辑负责为请求的数量分配库位并预留库位。</span><span class="sxs-lookup"><span data-stu-id="97bfe-109">The inventory reservation hierarchy dictates that, as far as storage dimensions are concerned, the demand order carries the mandatory dimensions of site, warehouse, and inventory status, whereas the warehouse logic is responsible for assigning a location to the requested quantities and reserving the location.</span></span> <span data-ttu-id="97bfe-110">换句话说，在需求订单和仓库操作之间的交互中，需求订单应指示必须从何处装运（即哪个站点和仓库）。</span><span class="sxs-lookup"><span data-stu-id="97bfe-110">In other words, in the interactions between the demand order and the warehouse operations, the demand order is expected to indicate where the order must be shipped from (that is, what site and warehouse).</span></span> <span data-ttu-id="97bfe-111">然后，仓库依靠其逻辑在仓库场所查找所需的数量。</span><span class="sxs-lookup"><span data-stu-id="97bfe-111">The warehouse then relies on its logic to find the required quantity in the warehouse premises.</span></span>

<span data-ttu-id="97bfe-112">但是，为了反映业务的运营模型，跟踪维度（批号和序列号）需要具有更大的灵活性。</span><span class="sxs-lookup"><span data-stu-id="97bfe-112">However, to reflect the operational model of the business, tracking dimensions (batch and serial numbers) are subject to more flexibility.</span></span> <span data-ttu-id="97bfe-113">库存预留层次结构可以应对适用以下条件的场景：</span><span class="sxs-lookup"><span data-stu-id="97bfe-113">An inventory reservation hierarchy can accommodate scenarios where the following conditions apply:</span></span>

- <span data-ttu-id="97bfe-114">企业依靠其仓库操作来管理在仓储存储空间中找到具有批号或序列号的数量后，领取这些数量。</span><span class="sxs-lookup"><span data-stu-id="97bfe-114">The business relies on its warehouse operations to manage picking of quantities that have batch or serial numbers after the quantities have been found in the warehousing storage space.</span></span> <span data-ttu-id="97bfe-115">此模型通常称为 *Batch-below\[location\]*。</span><span class="sxs-lookup"><span data-stu-id="97bfe-115">This model is often referred to as *Batch-below\[location\]*.</span></span> <span data-ttu-id="97bfe-116">它通常在产品的批号或序列号标识对向销售公司提出需求的客户不重要时使用。</span><span class="sxs-lookup"><span data-stu-id="97bfe-116">It's typically used when a product's batch or serial number identification isn't important to the customers who place the demand with the selling company.</span></span>
- <span data-ttu-id="97bfe-117">如果批号或序列号是客户订单说明的一部分，并且记录在需求订单中，则在仓库中查找数量的仓库操作将受特定的请求的编号约束，不允许对其进行更改。</span><span class="sxs-lookup"><span data-stu-id="97bfe-117">If batch or serial numbers are part of a customer's order specification, and they are recorded on the demand order, the warehouse operations that find the quantities in the warehouse are constrained by the specific requested numbers and aren't allowed to change them.</span></span> <span data-ttu-id="97bfe-118">此模型称为 *Batch-above\[location\]*。</span><span class="sxs-lookup"><span data-stu-id="97bfe-118">This model is referred to as *Batch-above\[location\]*.</span></span>

<span data-ttu-id="97bfe-119">在这些场景中，挑战在于，只能为每个已发布的产品分配一个库存预留层次结构。</span><span class="sxs-lookup"><span data-stu-id="97bfe-119">In these scenarios, the challenge is that only one inventory reservation hierarchy can be assigned to each released product.</span></span> <span data-ttu-id="97bfe-120">因此，为使 WMS 处理跟踪物料，在层次结构分配确定应预留批号或序列号的时间之后（在接到需求订单时或在仓库领料工作期间），此时间不能作为特例更改。</span><span class="sxs-lookup"><span data-stu-id="97bfe-120">Therefore, for the WMS to handle tracked items, after the hierarchy assignment determines when the batch or serial number should be reserved (either when the demand order is taken or during the warehouse picking work), this timing can't be changed on an ad-hoc basis.</span></span>

## <a name="flexible-reservation-for-batch-tracked-items"></a><span data-ttu-id="97bfe-121">灵活地预留批次跟踪物料</span><span class="sxs-lookup"><span data-stu-id="97bfe-121">Flexible reservation for batch-tracked items</span></span>

### <a name="business-scenario"></a><span data-ttu-id="97bfe-122">业务方案</span><span class="sxs-lookup"><span data-stu-id="97bfe-122">Business scenario</span></span>

<span data-ttu-id="97bfe-123">在此场景中，公司使用按批号跟踪成品的库存策略。</span><span class="sxs-lookup"><span data-stu-id="97bfe-123">In this scenario, a company uses an inventory strategy where finished goods are tracked by batch numbers.</span></span> <span data-ttu-id="97bfe-124">该公司还使用 WMS 工作负载。</span><span class="sxs-lookup"><span data-stu-id="97bfe-124">This company also uses the WMS workload.</span></span> <span data-ttu-id="97bfe-125">因为此工作负载具有用于计划和运行已启用批次的物料的仓库领料和装运操作的设备完善的逻辑，所以大多数成品物料都与“Batch-below\[location\]”库存预留层次结构相关联。</span><span class="sxs-lookup"><span data-stu-id="97bfe-125">Because this workload has well-equipped logic for planning and running warehouse picking and shipping operations for batch-enabled items, most of the finished items are associated with a "Batch-below\[location\]" inventory reservation hierarchy.</span></span> <span data-ttu-id="97bfe-126">这种类型的运营设置的优点在于，关于领取哪些批次以及将其放入仓库中哪个位置的决定（即有效的预留决定）被推迟到仓库领料操作开始时。</span><span class="sxs-lookup"><span data-stu-id="97bfe-126">The advantage of this type of operational setup is that decisions (which are effectively reservation decisions) about which batches to pick and where to put them in the warehouse are postponed until the warehouse picking operations start.</span></span> <span data-ttu-id="97bfe-127">而不会在客户下订单时作出。</span><span class="sxs-lookup"><span data-stu-id="97bfe-127">They aren't made when the customer's order is placed.</span></span>

<span data-ttu-id="97bfe-128">虽然“Batch-below\[location\]”预留层次结构很好地满足了公司的业务目标，但公司的许多老客户在重新订购产品时需要的都是以前购买的相同批次。</span><span class="sxs-lookup"><span data-stu-id="97bfe-128">Although the "Batch-below\[location\]" reservation hierarchy serves the company's business goals well, many of the company's established customers require the same batch that they previously purchased when they reorder products.</span></span> <span data-ttu-id="97bfe-129">因此，该公司正在寻求一种灵活的方式来处理批次预留规则，以便能够根据客户对同一物料的需求，执行以下行为：</span><span class="sxs-lookup"><span data-stu-id="97bfe-129">Therefore, the company is looking for flexibility in the way that the batch reservation rules are handled, so that, depending on the customers' demand for the same item, the following behaviors occur:</span></span>

- <span data-ttu-id="97bfe-130">当销售管理员接收订单时，可以记录并保留批号，并且批号在仓库操作期间不能更改和/或被其他需求获取。</span><span class="sxs-lookup"><span data-stu-id="97bfe-130">A batch number can be recorded and reserved when the order is taken by the sales processor, and it can't be changed during warehouse operations and/or taken by other demands.</span></span> <span data-ttu-id="97bfe-131">此行为有助于确保将订购的批号运送到客户。</span><span class="sxs-lookup"><span data-stu-id="97bfe-131">This behavior helps guarantee that the batch number that was ordered is shipped to the customer.</span></span>
- <span data-ttu-id="97bfe-132">如果批号对客户不重要，则在完成销售订单登记和预留后，仓库操作可以在领料工作期间确定批号。</span><span class="sxs-lookup"><span data-stu-id="97bfe-132">If the batch number isn't important to the customer, the warehouse operations can determine a batch number during picking work, after sales order registration and reservation have been done.</span></span>

### <a name="allowing-reservation-of-a-specific-batch-on-the-sales-order"></a><span data-ttu-id="97bfe-133">允许在销售订单上保留特定批次</span><span class="sxs-lookup"><span data-stu-id="97bfe-133">Allowing reservation of a specific batch on the sales order</span></span>

<span data-ttu-id="97bfe-134">为了适应与“Batch-below\[location\]”库存预留层次结构相关联的物料的批次预留行为的灵活性，库存管理员必须在**库存预留层次结构**页上为**批号**级别选择**允许在需求订单上预留**复选框。</span><span class="sxs-lookup"><span data-stu-id="97bfe-134">To accommodate the desired flexibility in the batch reservation behavior for items that are associated with a "Batch-below\[location\]" inventory reservation hierarchy, inventory managers must select the **Allow reservation on demand order** check box for the **Batch number** level on the **Inventory reservation hierarchies** page.</span></span>

![使库存预留层次结构更灵活](media/Flexible-inventory-reservation-hierarchy.png)

<span data-ttu-id="97bfe-136">当在层次结构中选择了**批号**级别时，从该级别开始直至**库位**级别的所有维度都将被自动选择。</span><span class="sxs-lookup"><span data-stu-id="97bfe-136">When the **Batch number** level in the hierarchy is selected, all dimensions above that level and up through the **Location** level will be automatically selected.</span></span> <span data-ttu-id="97bfe-137">（默认情况下，会预先选择**库位**级别以上的所有维度。）此行为反映了这样的逻辑：在订单行上预留特定批号后，批号和库位之间的范围内的所有维度也会自动预留。</span><span class="sxs-lookup"><span data-stu-id="97bfe-137">(By default, all dimensions above the **Location** level are preselected.) This behavior reflects the logic where all dimensions in the range between the batch number and location are also automatically reserved after you reserve a specific batch number on the order line.</span></span>

> [!NOTE]
> <span data-ttu-id="97bfe-138">**允许在需求订单上预留**复选框仅适用于仓库库位维度以下的预留层次结构级别。</span><span class="sxs-lookup"><span data-stu-id="97bfe-138">The **Allow reservation on demand order** check box applies only to reservation hierarchy levels that are below the warehouse location dimension.</span></span>
>
> <span data-ttu-id="97bfe-139">**批号**是层次结构中唯一为灵活预留策略开放的级别。</span><span class="sxs-lookup"><span data-stu-id="97bfe-139">**Batch number** is the only level in the hierarchy that is open for the flexible reservation policy.</span></span> <span data-ttu-id="97bfe-140">换句话说，您无法为**库位**，**牌照**或**序列号**级别选择**允许在需求订单上预留**复选框。</span><span class="sxs-lookup"><span data-stu-id="97bfe-140">In other words, you can't select the **Allow reservation on demand order** check box for the **Location**, **License plate**, or **Serial number** level.</span></span>
>
> <span data-ttu-id="97bfe-141">如果您的预留层次结构包含序列号维度（必须始终在**批号**级别以下），并且您已为批号打开了特定于批次的预留，系统将根据应用于“Serial-below\[location\]”预留策略的规则，继续处理序列号预留和领料操作。</span><span class="sxs-lookup"><span data-stu-id="97bfe-141">If your reservation hierarchy includes the serial number dimension (which must always be below the **Batch number** level), and if you've turned on batch-specific reservation for the batch number, the system will continue to handle serial number reservation and picking operations, based on the rules that apply to the "Serial-below\[location\]" reservation policy.</span></span>

<span data-ttu-id="97bfe-142">任何时候，您都可以允许为部署中现有的“Batch-below\[location\]”预留层次结构进行批次特定预留。</span><span class="sxs-lookup"><span data-stu-id="97bfe-142">At any point, you can allow batch-specific reservation for an existing "Batch-below\[location\]" reservation hierarchy in your deployment.</span></span> <span data-ttu-id="97bfe-143">此更改不会影响更改发生之前创建的任何预留和开放仓库工作。</span><span class="sxs-lookup"><span data-stu-id="97bfe-143">This change won't affect any reservations and open warehouse work that were created before the change occurred.</span></span> <span data-ttu-id="97bfe-144">但是，如果与该预留层次结构关联的一个或多个物料存在问题类型为**订购预留**、**实际预留**或**已订购**的库存交易记录，则不能清除**允许在需求订单上预留**复选框。</span><span class="sxs-lookup"><span data-stu-id="97bfe-144">However, the **Allow reservation on demand order** check box can't be cleared if inventory transactions of the **Reserved ordered**, **Reserved physical**, or **Ordered** issue type exist for one or more items that are associated with that reservation hierarchy.</span></span>

> [!NOTE]
> <span data-ttu-id="97bfe-145">如果物料的现有预留层次结构不允许订单上有批次说明，您可以将其重新分配到允许批次说明的预留层次结构，前提是两个层次结构的层次结构级别结构均相同。</span><span class="sxs-lookup"><span data-stu-id="97bfe-145">If an item's existing reservation hierarchy doesn't allow batch specification on the order, you can reassign it to a reservation hierarchy that does allow batch specification, provided that the hierarchy level structure is the same in both hierarchies.</span></span> <span data-ttu-id="97bfe-146">使用**更改物料的预留层次结构**功能来进行重新分配。</span><span class="sxs-lookup"><span data-stu-id="97bfe-146">Use the **Change reservation hierarchy for items** function to do the reassignment.</span></span> <span data-ttu-id="97bfe-147">当您要阻止为批次跟踪物料的其中一部分进行灵活的批次预留，但允许对其余的产品组合执行时，此更改可能很有用。</span><span class="sxs-lookup"><span data-stu-id="97bfe-147">This change might be relevant when you want to prevent flexible batch reservation for a subset of batch-tracked items but allow it for the rest of the product portfolio.</span></span>

<span data-ttu-id="97bfe-148">无论您是否选择了**允许在需求订单上预留**复选框，如果您不想为订单行上的物料预留特定的批号，仍会应用对“Batch-below\[location\]”预留层次结构有效的默认仓库操作逻辑。</span><span class="sxs-lookup"><span data-stu-id="97bfe-148">Regardless of whether you've selected the **Allow reservation on demand order** check box, if you don't want to reserve a specific batch number for the item on an order line, default warehouse operations logic that is valid for a "Batch-below\[location\]" reservation hierarchy will still apply.</span></span>

### <a name="reserve-a-specific-batch-number-for-a-customer-order"></a><span data-ttu-id="97bfe-149">为客户订单预留特定批号</span><span class="sxs-lookup"><span data-stu-id="97bfe-149">Reserve a specific batch number for a customer order</span></span>

<span data-ttu-id="97bfe-150">在批次跟踪物料的“Batch-below\[location\]”库存预留层次结构设置为允许在销售订单上预留特定批号后，销售订单管理员可以根据客户的请求，通过以下其中一种方式获取同一物料的客户订单：</span><span class="sxs-lookup"><span data-stu-id="97bfe-150">After a batch-tracked item's "Batch-below\[location\]" inventory reservation hierarchy is set up to allow reservation of specific batch numbers on sales orders, sales order processors can take customer orders for the same item in one of the following ways, depending on the customer's request:</span></span>

- <span data-ttu-id="97bfe-151">**输入订单详细信息但不指定批号** – 当产品的批次说明对客户不重要时，应使用此方法。</span><span class="sxs-lookup"><span data-stu-id="97bfe-151">**Enter order details without specifying a batch number** – This approach should be used when the product's batch specification isn't important to the customer.</span></span> <span data-ttu-id="97bfe-152">与处理系统中这种类型的订单相关联的所有现有流程均保持不变。</span><span class="sxs-lookup"><span data-stu-id="97bfe-152">All existing processes that are associated with handling an order of this type in the system remain unchanged.</span></span> <span data-ttu-id="97bfe-153">不需要对这部分用户作任何其他考虑。</span><span class="sxs-lookup"><span data-stu-id="97bfe-153">No additional considerations are required on the part of users.</span></span>
- <span data-ttu-id="97bfe-154">**输入订单详细信息并保留特定批号** – 当客户请求特定批次时，应使用此方法。</span><span class="sxs-lookup"><span data-stu-id="97bfe-154">**Enter order details and reserve a specific batch number** – This approach should be used when the customer requests a specific batch.</span></span> <span data-ttu-id="97bfe-155">通常，客户在重新订购之前购买的产品时会请求特定批次。</span><span class="sxs-lookup"><span data-stu-id="97bfe-155">Typically, customers will request a specific batch when they are reordering a product that they previously purchased.</span></span> <span data-ttu-id="97bfe-156">这种类型的批次特定预留称为*订单承诺预留*。</span><span class="sxs-lookup"><span data-stu-id="97bfe-156">This type of batch-specific reservation is referred to as *order-committed reservation*.</span></span>

<span data-ttu-id="97bfe-157">当数量被处理并将批号提交到特定订单时，以下这组规则有效：</span><span class="sxs-lookup"><span data-stu-id="97bfe-157">The following set of rules is valid when quantities are processed, and a batch number is committed to a specific order:</span></span>

- <span data-ttu-id="97bfe-158">为了允许根据“Batch-below\[location\]”预留策略为物料预留特定批号，系统必须预留整个库位的所有维度。</span><span class="sxs-lookup"><span data-stu-id="97bfe-158">To allow reservation of a specific batch number for an item under the "Batch-below\[location\]" reservation policy, the system must reserve all dimensions up through location.</span></span> <span data-ttu-id="97bfe-159">这个范围通常包括牌照维度。</span><span class="sxs-lookup"><span data-stu-id="97bfe-159">This range typically includes the license plate dimension.</span></span>
- <span data-ttu-id="97bfe-160">在为使用订单承诺批次预留的销售订单行创建领料工作时，不使用库位指令。</span><span class="sxs-lookup"><span data-stu-id="97bfe-160">Location directives aren't used when picking work is created for a sales line that uses order-committed batch reservation.</span></span>
- <span data-ttu-id="97bfe-161">在订单承诺批次的仓库处理工作期间，用户和系统都不允许更改批号。</span><span class="sxs-lookup"><span data-stu-id="97bfe-161">During warehouse processing of work for order-committed batches, neither the user nor the system is allowed to change the batch number.</span></span> <span data-ttu-id="97bfe-162">（此处理包括异常处理。）</span><span class="sxs-lookup"><span data-stu-id="97bfe-162">(This processing includes exception handling.)</span></span>

<span data-ttu-id="97bfe-163">以下示例显示了端到端流。</span><span class="sxs-lookup"><span data-stu-id="97bfe-163">The following example shows the end-to-end flow.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="97bfe-164">示例场景</span><span class="sxs-lookup"><span data-stu-id="97bfe-164">Example scenario</span></span>

<span data-ttu-id="97bfe-165">必须为此示例安装演示数据，并且必须使用 **USMF** 演示数据公司。</span><span class="sxs-lookup"><span data-stu-id="97bfe-165">For this example, demo data must be installed, and you must use the **USMF** demo data company.</span></span>

### <a name="set-up-an-inventory-reservation-hierarchy-to-allow-batch-specific-reservation"></a><span data-ttu-id="97bfe-166">设置库存预留层次结构以允许批次特定预留</span><span class="sxs-lookup"><span data-stu-id="97bfe-166">Set up an inventory reservation hierarchy to allow batch-specific reservation</span></span>

1. <span data-ttu-id="97bfe-167">转到**仓库管理** \> **设置** \> **库存 \> 预留层次结构**。</span><span class="sxs-lookup"><span data-stu-id="97bfe-167">Go to **Warehouse management** \> **Setup** \> **Inventory \> Reservation hierarchy**.</span></span>
2. <span data-ttu-id="97bfe-168">选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="97bfe-168">Select **New**.</span></span>
3. <span data-ttu-id="97bfe-169">在**名称**字段中，输入名称（例如，**BatchFlex**）。</span><span class="sxs-lookup"><span data-stu-id="97bfe-169">In the **Name** field, enter a name (for example, **BatchFlex**).</span></span>
4. <span data-ttu-id="97bfe-170">在**描述**字段中，输入描述（例如，**批次以下灵活预留**）。</span><span class="sxs-lookup"><span data-stu-id="97bfe-170">In the **Description** field, enter a description (for example, **Batch below flexible**).</span></span>
5. <span data-ttu-id="97bfe-171">在**已选**字段中，选择**序列号**和**所有者**，然后选择左箭头按钮将其移至**可用**字段。</span><span class="sxs-lookup"><span data-stu-id="97bfe-171">In the **Selected** field, select **Serial number** and **Owner**, and then select the left arrow button to move them to the **Available** field.</span></span>
6. <span data-ttu-id="97bfe-172">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="97bfe-172">Select **OK**.</span></span>
7. <span data-ttu-id="97bfe-173">在**批号**维度级别行中，选择**允许在需求订单上预留**复选框。</span><span class="sxs-lookup"><span data-stu-id="97bfe-173">In the row for the **Batch number** dimension level, select the **Allow reservation on demand order** check box.</span></span> <span data-ttu-id="97bfe-174">**牌照**和**库位**级别将自动选择，您不能清除它们的复选框。</span><span class="sxs-lookup"><span data-stu-id="97bfe-174">The **License plate** and **Location** levels are automatically selected, and you can't clear the check boxes for them.</span></span>
8. <span data-ttu-id="97bfe-175">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="97bfe-175">Select **Save**.</span></span>

### <a name="create-a-new-released-product"></a><span data-ttu-id="97bfe-176">创建新的已发布产品</span><span class="sxs-lookup"><span data-stu-id="97bfe-176">Create a new released product</span></span>

1. <span data-ttu-id="97bfe-177">使用以下值设置产品的三个主数据参数：</span><span class="sxs-lookup"><span data-stu-id="97bfe-177">Set the product's three master data parameters by using these values:</span></span>

    - <span data-ttu-id="97bfe-178">在**存储维度组**字段中，选择 **Ware**。</span><span class="sxs-lookup"><span data-stu-id="97bfe-178">In the **Storage dimension group** field, select **Ware**.</span></span>
    - <span data-ttu-id="97bfe-179">在**跟踪维度组**字段中，选择 **Batch-Phy**。</span><span class="sxs-lookup"><span data-stu-id="97bfe-179">In the **Tracking dimension group** field, select **Batch-Phy**.</span></span>
    - <span data-ttu-id="97bfe-180">在**预留层次结构**字段中，选择 **BatchFlex**。</span><span class="sxs-lookup"><span data-stu-id="97bfe-180">In the **Reservation hierarchy** field, select **BatchFlex**.</span></span>

2. <span data-ttu-id="97bfe-181">创建两个批号，例如 **B11** 和 **B22**。</span><span class="sxs-lookup"><span data-stu-id="97bfe-181">Create two batch numbers, such as **B11** and **B22**.</span></span>
3. <span data-ttu-id="97bfe-182">使用以下值将物料数量添加到现有库存中。</span><span class="sxs-lookup"><span data-stu-id="97bfe-182">Add item quantities to on-hand stock by using the following values.</span></span>

    | <span data-ttu-id="97bfe-183">存放地点</span><span class="sxs-lookup"><span data-stu-id="97bfe-183">Warehouse</span></span> | <span data-ttu-id="97bfe-184">批号</span><span class="sxs-lookup"><span data-stu-id="97bfe-184">Batch number</span></span> | <span data-ttu-id="97bfe-185">场所</span><span class="sxs-lookup"><span data-stu-id="97bfe-185">Location</span></span> | <span data-ttu-id="97bfe-186">牌照</span><span class="sxs-lookup"><span data-stu-id="97bfe-186">License plate</span></span> | <span data-ttu-id="97bfe-187">数量</span><span class="sxs-lookup"><span data-stu-id="97bfe-187">Quantity</span></span> |
    |-----------|--------------|----------|---------------|----------|
    | <span data-ttu-id="97bfe-188">24</span><span class="sxs-lookup"><span data-stu-id="97bfe-188">24</span></span>        | <span data-ttu-id="97bfe-189">B11</span><span class="sxs-lookup"><span data-stu-id="97bfe-189">B11</span></span>          | <span data-ttu-id="97bfe-190">BULK-001</span><span class="sxs-lookup"><span data-stu-id="97bfe-190">BULK-001</span></span> | <span data-ttu-id="97bfe-191">否</span><span class="sxs-lookup"><span data-stu-id="97bfe-191">None</span></span>          | <span data-ttu-id="97bfe-192">10</span><span class="sxs-lookup"><span data-stu-id="97bfe-192">10</span></span>       |
    | <span data-ttu-id="97bfe-193">24</span><span class="sxs-lookup"><span data-stu-id="97bfe-193">24</span></span>        | <span data-ttu-id="97bfe-194">B11</span><span class="sxs-lookup"><span data-stu-id="97bfe-194">B11</span></span>          | <span data-ttu-id="97bfe-195">FL-001</span><span class="sxs-lookup"><span data-stu-id="97bfe-195">FL-001</span></span>   | <span data-ttu-id="97bfe-196">LP11</span><span class="sxs-lookup"><span data-stu-id="97bfe-196">LP11</span></span>          | <span data-ttu-id="97bfe-197">10</span><span class="sxs-lookup"><span data-stu-id="97bfe-197">10</span></span>       |
    | <span data-ttu-id="97bfe-198">24</span><span class="sxs-lookup"><span data-stu-id="97bfe-198">24</span></span>        | <span data-ttu-id="97bfe-199">B22</span><span class="sxs-lookup"><span data-stu-id="97bfe-199">B22</span></span>          | <span data-ttu-id="97bfe-200">FL-002</span><span class="sxs-lookup"><span data-stu-id="97bfe-200">FL-002</span></span>   | <span data-ttu-id="97bfe-201">LP22</span><span class="sxs-lookup"><span data-stu-id="97bfe-201">LP22</span></span>          | <span data-ttu-id="97bfe-202">10</span><span class="sxs-lookup"><span data-stu-id="97bfe-202">10</span></span>       |

### <a name="enter-sales-order-details"></a><span data-ttu-id="97bfe-203">输入销售订单详细信息</span><span class="sxs-lookup"><span data-stu-id="97bfe-203">Enter sales order details</span></span>

1. <span data-ttu-id="97bfe-204">转到**销售和营销** \> **销售订单** \> **所有销售订单**。</span><span class="sxs-lookup"><span data-stu-id="97bfe-204">Go to **Sales and marketing** \> **Sales orders** \> **All sales orders**.</span></span>
2. <span data-ttu-id="97bfe-205">选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="97bfe-205">Select **New**.</span></span>
3. <span data-ttu-id="97bfe-206">在销售订单抬头上，在**客户帐户**字段中，输入 **US-003**。</span><span class="sxs-lookup"><span data-stu-id="97bfe-206">On the sales order header, in the **Customer account** field, enter **US-003**.</span></span>
4. <span data-ttu-id="97bfe-207">为新物料添加一行，然后输入 **10** 作为数量。</span><span class="sxs-lookup"><span data-stu-id="97bfe-207">Add a line for the new item, and enter **10** as the quantity.</span></span> <span data-ttu-id="97bfe-208">请确保**仓库**字段设置为 **24**。</span><span class="sxs-lookup"><span data-stu-id="97bfe-208">Make sure that the **Warehouse** field is set to **24**.</span></span>
5. <span data-ttu-id="97bfe-209">在**销售订单行**快速选项卡上，选择**库存**，然后在**维护**组中，选择**批次预留**。</span><span class="sxs-lookup"><span data-stu-id="97bfe-209">On the **Sales order lines** FastTab, select **Inventory**, and then, in the **Maintain** group, select **Batch reservation**.</span></span> <span data-ttu-id="97bfe-210">**批次预留**页面将显示可为订单行预留的批次的列表。</span><span class="sxs-lookup"><span data-stu-id="97bfe-210">The **Batch reservation** page shows a list of batches that are available for reservation for the order line.</span></span> <span data-ttu-id="97bfe-211">在此示例中，此页面显示批号 **B11** 的数量为 **20**，批号 **B22** 的数量为 **10**。</span><span class="sxs-lookup"><span data-stu-id="97bfe-211">For this example, it shows a quantity of **20** for batch number **B11** and a quantity of **10** for batch number **B22**.</span></span> <span data-ttu-id="97bfe-212">请注意，如果某行的物料与“Batch-below\[location\]”预留层次结构关联，则无法从该行访问**批次预留**页面，除非已将其设置为允许批次特定预留。</span><span class="sxs-lookup"><span data-stu-id="97bfe-212">Note that the **Batch reservation** page cannot be accessed from a line if the item on that line is associated with "Batch-below\[location\]" reservation hierarchy unless it is set up to allow batch-specific reservation.</span></span>

    > [!NOTE]
    > <span data-ttu-id="97bfe-213">要为销售订单预留特定批次，您必须使用**批次预留**页。</span><span class="sxs-lookup"><span data-stu-id="97bfe-213">To reserve a specific batch for a sales order, you must use the **Batch reservation** page.</span></span>
    >
    > <span data-ttu-id="97bfe-214">如果您直接在销售订单行上输入批号，系统行为将与您为遵守“Batch-below\[location\]”预留策略的物料输入特定批次值时一样。</span><span class="sxs-lookup"><span data-stu-id="97bfe-214">If you enter the batch number directly on the sales order line, the system will behave as though you entered a specific batch value for an item that is subject to the "Batch-below\[location\]" reservation policy.</span></span> <span data-ttu-id="97bfe-215">保存行时，您将收到一条警告消息。</span><span class="sxs-lookup"><span data-stu-id="97bfe-215">When you save the line, you will receive a warning message.</span></span> <span data-ttu-id="97bfe-216">如果您确认应直接在订单行上指定批号，该行将不会由常规仓库管理逻辑处理。</span><span class="sxs-lookup"><span data-stu-id="97bfe-216">If you confirm that the batch number should be specified directly on the order line, the line won't be handled by the regular warehouse management logic.</span></span>
    >
    > <span data-ttu-id="97bfe-217">如果您从**预留**页预留数量，将不预留特定批次，并且该行的仓库操作的执行将遵循按照“Batch-below\[location\]”预留策略适用的规则。</span><span class="sxs-lookup"><span data-stu-id="97bfe-217">If you reserve the quantity from the **Reservation** page, no specific batch will be reserved, and the execution of warehouse operations for the line will follow the rules that are applicable under the "Batch-below\[location\]" reservation policy.</span></span>

    <span data-ttu-id="97bfe-218">通常，此页面的工作和交互方式与用于具有“Batch-above\[location\]”类型的关联预留层次结构的物料时相同。</span><span class="sxs-lookup"><span data-stu-id="97bfe-218">In general, this page works and is interacted with in the same way that it works and is interacted with for items that have an associated reservation hierarchy of the "Batch-above\[location\]" type.</span></span> <span data-ttu-id="97bfe-219">但是，以下例外适用：</span><span class="sxs-lookup"><span data-stu-id="97bfe-219">However, the following exceptions apply:</span></span>

    - <span data-ttu-id="97bfe-220">**提交到源行的批号**快速选项卡显示为订单行预留的批号。</span><span class="sxs-lookup"><span data-stu-id="97bfe-220">The **Batch numbers committed to source line** FastTab shows the batch numbers that are reserved for the order line.</span></span> <span data-ttu-id="97bfe-221">网格中的批次值将在订单行的整个履行周期内显示，包括仓库处理阶段。</span><span class="sxs-lookup"><span data-stu-id="97bfe-221">The batch values in the grid will be shown throughout the fulfilment cycle of the order line, including the warehouse processing stages.</span></span> <span data-ttu-id="97bfe-222">相比之下，在**概览**快速选项卡上，常规的订单行预留（即针对**库位**级别以上的维度进行的预留）显示在网格中，直到仓库工作创建为止。</span><span class="sxs-lookup"><span data-stu-id="97bfe-222">By contrast, on the **Overview** FastTab, regular order line reservation (that is, reservation that is done for the dimensions above the **Location** level) is shown in the grid up to the point when warehouse work is created.</span></span> <span data-ttu-id="97bfe-223">然后，工作实体接管行预留，行预留不再出现在页面上。</span><span class="sxs-lookup"><span data-stu-id="97bfe-223">The work entity then takes over the line reservation, and the line reservation no longer appears on the page.</span></span> <span data-ttu-id="97bfe-224">**提交到源行的批号**快速选项卡帮助确保销售订单管理员可以查看，在客户订单生命周期的任何时间直到开票提交到该订单的批号。</span><span class="sxs-lookup"><span data-stu-id="97bfe-224">The **Batch numbers committed to source line** FastTab helps guarantee that the sales order processor can view the batch numbers that were committed to the customer's order at any point during its lifecycle, up through invoicing.</span></span>
    - <span data-ttu-id="97bfe-225">除了预留特定批次外，用户还可以手动选择批次的特定库位和牌照，而不是让系统自动选择。</span><span class="sxs-lookup"><span data-stu-id="97bfe-225">In addition to reserving a specific batch, a user can manually select the batch's specific location and license plate instead of letting the system automatically select them.</span></span> <span data-ttu-id="97bfe-226">此功能与订单承诺批次预留机制的设计有关。</span><span class="sxs-lookup"><span data-stu-id="97bfe-226">This capability is related to the design of the order-committed batch reservation mechanism.</span></span> <span data-ttu-id="97bfe-227">如前所述，当根据“Batch-below\[location\]”预留策略为物料预留批号时，系统必须预留整个库位的所有维度。</span><span class="sxs-lookup"><span data-stu-id="97bfe-227">As was mentioned earlier, when a batch number is reserved for an item under the "Batch-below\[location\]" reservation policy, the system must reserve all dimensions up through location.</span></span> <span data-ttu-id="97bfe-228">因此，仓库工作将包含与处理订单的用户预留的相同的存储维度，可能并不总是代表着对领料操作方便甚至可能的物料存储位置。</span><span class="sxs-lookup"><span data-stu-id="97bfe-228">Therefore, warehouse work will carry the same storage dimensions that were reserved by the users who worked with the orders, and it might not always represent the item storage placement that is convenient, or even possible, for picking operations.</span></span> <span data-ttu-id="97bfe-229">如果订单管理员知道仓库约束，他们可能希望在预留批次时手动选择特定库位和牌照。</span><span class="sxs-lookup"><span data-stu-id="97bfe-229">If order processors are aware of the warehouse constraints, they might want to manually select the specific locations and license plates when they reserve a batch.</span></span> <span data-ttu-id="97bfe-230">在这种情况下，用户必须使用页标题上的**显示维度**功能，并且必须在**概览**快速选项卡上的网格中添加库位和牌照。</span><span class="sxs-lookup"><span data-stu-id="97bfe-230">In this case, the user must use the **Display dimensions** functionality on the page header, and must add the location and license plate in the grid on the **Overview** FastTab.</span></span>

6. <span data-ttu-id="97bfe-231">在**批次预留**页面上，选择 **B11** 这一行，然后选择**预留行**。</span><span class="sxs-lookup"><span data-stu-id="97bfe-231">On the **Batch reservation** page, select the line for batch **B11**, and then select **Reserve line**.</span></span> <span data-ttu-id="97bfe-232">在自动预留期间，没有用于分配库位和牌照的指定逻辑。</span><span class="sxs-lookup"><span data-stu-id="97bfe-232">There is no designated logic for assigning locations and license plates during automatic reservation.</span></span> <span data-ttu-id="97bfe-233">您可以在**预留**字段中手动输入数量。</span><span class="sxs-lookup"><span data-stu-id="97bfe-233">You can manually enter the quantity in the **Reservation** field.</span></span> <span data-ttu-id="97bfe-234">请注意，在**提交到源行的批号**快速选项卡上，批次 **B11** 将显示为**已提交**。</span><span class="sxs-lookup"><span data-stu-id="97bfe-234">Notice that, on the **Batch numbers committed to source line** FastTab, batch **B11** is shown as **Committed**.</span></span>

    ![在“批次预留”页面上向销售订单行提交特定批号](media/Batch-reservation-form-with-order-committed-reservation.png)

    > [!NOTE]
    > <span data-ttu-id="97bfe-236">可以跨多个批次在销售订单行上预留数量。</span><span class="sxs-lookup"><span data-stu-id="97bfe-236">Reservation of the quantity on a sales order line can be done across multiple batches.</span></span> <span data-ttu-id="97bfe-237">同样，可以针对多个库位和牌照进行同一批次的预留（如果已为库位启用了牌照）。</span><span class="sxs-lookup"><span data-stu-id="97bfe-237">Likewise, reservation of the same batch can be done against multiple locations and license plates (if license plates are enabled for the locations).</span></span>
    >
    > <span data-ttu-id="97bfe-238">在销售订单行上为数量预留特定批次也可以部分进行。</span><span class="sxs-lookup"><span data-stu-id="97bfe-238">Reservation of a specific batch for the quantity on a sales order line can also be partial.</span></span> <span data-ttu-id="97bfe-239">例如，可以预留 100 个单位的总数量，以向 20 个单位提交特定批次，而在站点和仓库级别为任何可用批次预留 80 个单位。</span><span class="sxs-lookup"><span data-stu-id="97bfe-239">For example, the total quantity of 100 units can be reserved so that a specific batch is committed to 20 units, whereas 80 units are reserved at the site and warehouse levels for any available batch.</span></span> <span data-ttu-id="97bfe-240">在这种情况下，WMS 将使用两个单独的工作行来处理领料操作。</span><span class="sxs-lookup"><span data-stu-id="97bfe-240">In this case, the WMS will handle picking operations by using two separate work lines.</span></span>

7. <span data-ttu-id="97bfe-241">转到**产品信息管理** \> **产品** \> **已发布产品**。</span><span class="sxs-lookup"><span data-stu-id="97bfe-241">Go to **Product information management** \> **Products** \> **Released products**.</span></span> <span data-ttu-id="97bfe-242">选择您的物料，然后选择**管理库存** \> **查看**\>**交易记录**。</span><span class="sxs-lookup"><span data-stu-id="97bfe-242">Select your item, and then select **Manage inventory** \> **View** \> **Transactions**.</span></span>

    ![将订单承诺预留作为库存交易记录类型](media/Inventory-transactions-for-order-committed-reservation.png)

8. <span data-ttu-id="97bfe-244">查看与销售订单行预留相关的物料库存交易记录。</span><span class="sxs-lookup"><span data-stu-id="97bfe-244">Review the item's inventory transactions that are related to the sales order line reservation.</span></span>

    - <span data-ttu-id="97bfe-245">**参考**字段设置为**销售订单**且**发货**字段设置为**实际预留**的交易记录，表示**库位**级别以上的库存维度的订单行预留。</span><span class="sxs-lookup"><span data-stu-id="97bfe-245">A transaction where the **Reference** field is set to **Sales order** and the **Issue** field is set to **Reserved physical** represents the order line reservation for the inventory dimensions above the **Location** level.</span></span> <span data-ttu-id="97bfe-246">根据物料的库存预留层次结构，这些维度是站点、仓库和库存状态。</span><span class="sxs-lookup"><span data-stu-id="97bfe-246">According to the item's inventory reservation hierarchy, those dimensions are site, warehouse, and inventory status.</span></span>
    - <span data-ttu-id="97bfe-247">**参考**字段设置为**订单承诺预留**且**发货**字段设置为**实际预留**的交易记录，表示特定批次以及其以上所有库存维度的订单行预留。</span><span class="sxs-lookup"><span data-stu-id="97bfe-247">A transaction where the **Reference** field is set to **Order-committed reservation** and the **Issue** field is set to **Reserved physical** represents the order line reservation for the specific batch and all inventory dimensions above it.</span></span> <span data-ttu-id="97bfe-248">根据物料的库存预留层次结构，这些维度是批号和库位。</span><span class="sxs-lookup"><span data-stu-id="97bfe-248">According to the item's inventory reservation hierarchy, those dimensions are batch number and location.</span></span> <span data-ttu-id="97bfe-249">在此示例中，库位是 **Bulk-001**。</span><span class="sxs-lookup"><span data-stu-id="97bfe-249">In this example, the location is **Bulk-001**.</span></span>

9. <span data-ttu-id="97bfe-250">在销售订单抬头上，选择**仓库** \> **操作** \> **发放到仓库**。</span><span class="sxs-lookup"><span data-stu-id="97bfe-250">On the sales order header, select **Warehouse** \> **Actions** \> **Release to warehouse**.</span></span> <span data-ttu-id="97bfe-251">订单行现在已分波次，负荷和工作已创建。</span><span class="sxs-lookup"><span data-stu-id="97bfe-251">The order line is now waved, and a load and work are created.</span></span>

### <a name="review-and-process-warehouse-work-that-has-order-committed-batch-numbers"></a><span data-ttu-id="97bfe-252">审查和处理具有订单承诺批号的仓库工作</span><span class="sxs-lookup"><span data-stu-id="97bfe-252">Review and process warehouse work that has order-committed batch numbers</span></span>

1. <span data-ttu-id="97bfe-253">在**销售订单行**快速选项卡上，选择**仓库** \> **工作详细信息**。</span><span class="sxs-lookup"><span data-stu-id="97bfe-253">On the **Sales order lines** FastTab, select **Warehouse** \> **Work details**.</span></span>

    <span data-ttu-id="97bfe-254">处理提交给销售订单行的批次数量的领料操作的工作具有以下特征：</span><span class="sxs-lookup"><span data-stu-id="97bfe-254">The work that handles the picking operation for batch quantities that are committed to the sales order line has the following characteristics:</span></span>

    - <span data-ttu-id="97bfe-255">为了创建工作，系统使用工作模板，而不是库位指令。</span><span class="sxs-lookup"><span data-stu-id="97bfe-255">To create work, the system uses work templates but not location directives.</span></span> <span data-ttu-id="97bfe-256">为工作模板定义的所有标准设置（例如，最大领料行数或特定度量单位）将应用来确定何时应创建新工作。</span><span class="sxs-lookup"><span data-stu-id="97bfe-256">All the standard settings that are defined for work templates, such as a maximum number of pick lines or a specific unit of measure, will be applied to determine when new work should be created.</span></span> <span data-ttu-id="97bfe-257">但是，不考虑与用于识别领料库位的库位指令相关联的规则，因为订单承诺预留已经指定了所有库存维度。</span><span class="sxs-lookup"><span data-stu-id="97bfe-257">However, the rules that are associated with location directives for identifying pick locations aren't considered, because the order-committed reservation already specifies all the inventory dimensions.</span></span> <span data-ttu-id="97bfe-258">这些库存维度包括仓库存储级别的维度。</span><span class="sxs-lookup"><span data-stu-id="97bfe-258">Those inventory dimensions include the dimensions at the warehouse storage level.</span></span> <span data-ttu-id="97bfe-259">因此，作品将继承这些维度，而不必参考库位指令。</span><span class="sxs-lookup"><span data-stu-id="97bfe-259">Therefore, the work inherits those dimensions without having to consult location directives.</span></span>
    - <span data-ttu-id="97bfe-260">批号不显示在领料行上（对于为具有关联的“Batch-above\[location\]”预留层次结构的物料创建的工作行就是这种情况。）而“源”批号和所有其他存储维度将显示在工作行的工作库存交易记录中，该交易记录是从关联的库存交易记录引用的。</span><span class="sxs-lookup"><span data-stu-id="97bfe-260">The batch number isn't shown on the pick line (as is the case for the work line that is created for an item that has an associated "Batch-above\[location\]" reservation hierarchy.) Instead, the "from" batch number and all other storage dimensions are shown on the work line's work inventory transaction that is referenced from the associated inventory transactions.</span></span>

        ![源自订单承诺预留的工作的仓库库存交易记录](media/Work-inventory-transactions-for-order-committed-reservation.png)

    - <span data-ttu-id="97bfe-262">创建工作后，**参考**字段设置为**订单承诺预留**的物料的库存交易记录将删除。</span><span class="sxs-lookup"><span data-stu-id="97bfe-262">After work is created, the item's inventory transaction where the **Reference** field is set to **Order-committed reservation** is removed.</span></span> <span data-ttu-id="97bfe-263">**参考**字段设置为**工作**的库存交易记录现在在所有数量的库存维度中保留实际预留。</span><span class="sxs-lookup"><span data-stu-id="97bfe-263">The inventory transaction where the **Reference** field is set to **Work** now holds the physical reservation on all the quantity's inventory dimensions.</span></span>

        <span data-ttu-id="97bfe-264">仓库操作可以以通常的方式继续处理工作的执行。</span><span class="sxs-lookup"><span data-stu-id="97bfe-264">Warehouse operations can proceed to handle execution of the work in the usual manner.</span></span> <span data-ttu-id="97bfe-265">但是，移动设备上的指令将指示工作人员领取特定的批号。</span><span class="sxs-lookup"><span data-stu-id="97bfe-265">However, the instructions on the mobile device will instruct the worker to pick a specific batch number.</span></span> <span data-ttu-id="97bfe-266">在库位由牌照控制的仓库环境中，当工作人员到达将同一批次存储在多个牌照中的库位后，他或她可以从尚未预留的任何牌照领料（例如，通过另一个订单承诺预留或源自该类型预留的工作。）</span><span class="sxs-lookup"><span data-stu-id="97bfe-266">In warehouse environments where locations are license plate–controlled, after a worker reaches a location that stores the same batch on multiple license plates, he or she can pick from any license plate that isn't already reserved (for example, by another order-committed reservation or work that originates from a reservation of that type.)</span></span>

        <span data-ttu-id="97bfe-267">如果发现从工作行上指定的库位领料不切实际，仓库操作员可以使用以下操作之一重定向来从更方便的库位领取特定批次：</span><span class="sxs-lookup"><span data-stu-id="97bfe-267">If it turns out to be impractical to pick from the location that is specified on the work line, the warehouse operators can use one of the following actions to redirect picking of the specific batch from a more convenient location:</span></span>

        - <span data-ttu-id="97bfe-268">移动设备上的标准**覆盖库位**操作（前提是仓库工作人员的**允许领料库位覆盖**设置已启用）</span><span class="sxs-lookup"><span data-stu-id="97bfe-268">The standard **Override location** action on a mobile device (provided that the warehouse worker's **Allow pick location override** setting is enabled)</span></span>
        - <span data-ttu-id="97bfe-269">**工作列表详细信息**页的**更改库位**操作。</span><span class="sxs-lookup"><span data-stu-id="97bfe-269">The **Change location** action on the **Work list details** page.</span></span> 

2. <span data-ttu-id="97bfe-270">在移动设备上，完成领料并放入工作。</span><span class="sxs-lookup"><span data-stu-id="97bfe-270">On the mobile device, finish picking and putting the work.</span></span>

    <span data-ttu-id="97bfe-271">批号 **B11** 的数量 **10** 现在已为销售订单行领取，并放入 **Baydoor** 库位。</span><span class="sxs-lookup"><span data-stu-id="97bfe-271">The quantity of **10** for batch number **B11** is now picked for the sales order line and put in the **Baydoor** location.</span></span> <span data-ttu-id="97bfe-272">此时，可以将其装载到卡车上并发往客户地址了。</span><span class="sxs-lookup"><span data-stu-id="97bfe-272">At this point, it's ready to be loaded onto the truck and dispatched to the customer's address.</span></span>

## <a name="exception-handling-of-warehouse-work-thas-has-order-committed-batch-numbers"></a><span data-ttu-id="97bfe-273">具有订单承诺批号的仓库工作的异常处理</span><span class="sxs-lookup"><span data-stu-id="97bfe-273">Exception handling of warehouse work thas has order-committed batch numbers</span></span>

<span data-ttu-id="97bfe-274">领取订单承诺批号的仓库工作与常规工作一样，都要接受相同的标准仓库异常处理和操作。</span><span class="sxs-lookup"><span data-stu-id="97bfe-274">Warehouse work for picking order-committed batch numbers is subject to the same standard warehouse exception handling and actions as regular work.</span></span> <span data-ttu-id="97bfe-275">通常，未结工作或工作行可以被取消，可以因为用户库位已满而中断，可以存在领料短缺，并可以由于移动而更新。</span><span class="sxs-lookup"><span data-stu-id="97bfe-275">In general, the open work or work line can be canceled, it can be interrupted because a user location is full, it can be short-picked, and it can be updated because of a movement.</span></span> <span data-ttu-id="97bfe-276">同样，已领取的已完成工作的数量可以减少，或工作可以冲销。</span><span class="sxs-lookup"><span data-stu-id="97bfe-276">Likewise, the picked quantity of work that has already been completed can be reduced, or the work can be reversed.</span></span>

<span data-ttu-id="97bfe-277">以下关键规则应用于所有这些异常处理操作：为客户预留的批号永远不能替换为其他批号，但是可以通过用户手动更新或系统自动更新来更改其存储维度（库位和牌照）。</span><span class="sxs-lookup"><span data-stu-id="97bfe-277">The following key rule is applied to all these exception handling actions: the batch number that was reserved for the customer can never be replaced with a different batch number, but its storage dimensions (location and license plate) can be changed through either a manual update by the user or an automatic update by the system.</span></span> <span data-ttu-id="97bfe-278">自动更新基于对存储维度的随机分配，其与在自动预留特定批次但未指定存储维度时应用的方法相同。</span><span class="sxs-lookup"><span data-stu-id="97bfe-278">The automatic update is based on the same random assignment of storage dimensions that applied when a specific batch was automatically reserved but no storage dimensions were specified.</span></span>

### <a name="example-scenario"></a><span data-ttu-id="97bfe-279">示例场景</span><span class="sxs-lookup"><span data-stu-id="97bfe-279">Example scenario</span></span>

<span data-ttu-id="97bfe-280">这种情形的一个示例是：之前完成的工作未通过使用**减少领料数量**功能领取。</span><span class="sxs-lookup"><span data-stu-id="97bfe-280">An example of this scenario is a situation where previously completed work is being unpicked by using the **Reduce picked quantity** function.</span></span> <span data-ttu-id="97bfe-281">此示例继续本主题中的上一个示例。</span><span class="sxs-lookup"><span data-stu-id="97bfe-281">This example continues the previous example in this topic.</span></span>

1. <span data-ttu-id="97bfe-282">转到**仓库管理** \> **负荷** \> **有效负荷**。</span><span class="sxs-lookup"><span data-stu-id="97bfe-282">Go to **Warehouse management** \> **Loads** \> **Active loads**.</span></span>
2. <span data-ttu-id="97bfe-283">选择创建的与销售订单的装运相关的负荷。</span><span class="sxs-lookup"><span data-stu-id="97bfe-283">Select the load that was created in connection with the shipment of your sales order.</span></span>
3. <span data-ttu-id="97bfe-284">从**负荷订单行**快速选项卡，选择**减少领料数量**。</span><span class="sxs-lookup"><span data-stu-id="97bfe-284">From the **Load order lines** FastTab, select **Reduce picked quantity**.</span></span>
4. <span data-ttu-id="97bfe-285">在**减少领料数量**页面，在**移到库位**字段中，选择 **FL-001**。</span><span class="sxs-lookup"><span data-stu-id="97bfe-285">On the **Reduce picked quantity** page, in the **Move to location** field, select **FL-001**.</span></span>
5. <span data-ttu-id="97bfe-286">在**移到牌照**字段中，选择 **LP33**。</span><span class="sxs-lookup"><span data-stu-id="97bfe-286">In the **Move to license plate** field, select **LP33**.</span></span>
6. <span data-ttu-id="97bfe-287">在网格中，在**要取消领料的库存数量**字段中，输入 **10**。</span><span class="sxs-lookup"><span data-stu-id="97bfe-287">In the grid, in the **Inventory quantity to unpick** field, enter **10**.</span></span>
7. <span data-ttu-id="97bfe-288">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="97bfe-288">Select **OK**.</span></span>

<span data-ttu-id="97bfe-289">这是取消领料操作的结果：</span><span class="sxs-lookup"><span data-stu-id="97bfe-289">Here are the results of the unpicking action:</span></span>

- <span data-ttu-id="97bfe-290">先前结束的工作的状态设置为**已取消**。</span><span class="sxs-lookup"><span data-stu-id="97bfe-290">The status of the previously closed work is set to **Canceled**.</span></span>
- <span data-ttu-id="97bfe-291">为批号 **B11** 的取消领料的数量 **10** 创建了**库存变动**类型的新工作。</span><span class="sxs-lookup"><span data-stu-id="97bfe-291">New work of the **Inventory movement** type is created for the unpicked quantity of **10** for batch number **B11**.</span></span> <span data-ttu-id="97bfe-292">此工作代表从 **Baydoor** 库位到 **FL-001** 库位中的牌照 **LP33** 的移动。</span><span class="sxs-lookup"><span data-stu-id="97bfe-292">This work represents the movement from the **Baydoor** location to license plate **LP33** in location **FL-001**.</span></span> <span data-ttu-id="97bfe-293">状态设置为**已结束**。</span><span class="sxs-lookup"><span data-stu-id="97bfe-293">The status is set to **Closed**.</span></span>
- <span data-ttu-id="97bfe-294">系统将重新预留最初订购的批号，并分配库位和牌照 ID。</span><span class="sxs-lookup"><span data-stu-id="97bfe-294">The system re-reserves the batch number that was originally ordered, and assigns the location and license plate IDs.</span></span> <span data-ttu-id="97bfe-295">（此流程等效于为给定批号的订单行运行**预留行**功能）。</span><span class="sxs-lookup"><span data-stu-id="97bfe-295">(This process is equivalent to running the **Reserve line** function for the order line for a given batch number).</span></span> <span data-ttu-id="97bfe-296">结果是，批次 **B11** 在**批次预留**页的**提交到源行的批号**快速选项卡上显示为已提交，**预留**字段包含批号 **B11** 的数量 **10**。</span><span class="sxs-lookup"><span data-stu-id="97bfe-296">As a result, batch **B11** is shown as committed on the **Batch numbers committed to source line** FastTab of the **Batch reservation** page, and the **Reservation** field contains a quantity of **10** for batch number **B11**.</span></span> <span data-ttu-id="97bfe-297">此外，**库位**字段设置为 **FL-001**，**牌照**字段设置为 **LP11**。</span><span class="sxs-lookup"><span data-stu-id="97bfe-297">Additionally, the **Location** field is set to **FL-001**, and the **License plate** field is set to **LP11**.</span></span> <span data-ttu-id="97bfe-298">（如果这些字段不可见，您可以将它们添加到网格中。）</span><span class="sxs-lookup"><span data-stu-id="97bfe-298">(You can add these fields to the grid if they aren't visible.)</span></span>

<span data-ttu-id="97bfe-299">下表提供了显示系统如何处理特定仓库操作的订单承诺批次预留的概览。</span><span class="sxs-lookup"><span data-stu-id="97bfe-299">The following tables provide an overview that shows how the system handles order-committed batch reservation for specific warehouse actions.</span></span> <span data-ttu-id="97bfe-300">为了解释表中的内容，假定每个仓库操作都在源于订单承诺批次预留的现有仓库工作的上下文中运行，或者每个仓库操作的执行都会影响该类型的工作。</span><span class="sxs-lookup"><span data-stu-id="97bfe-300">To interpret the content in the tables, assume that each warehouse action is run in the context of existing warehouse work that originates from an order-committed batch reservation, or that execution of each warehouse action affects work of that type.</span></span>

> [!NOTE]
> <span data-ttu-id="97bfe-301">在这些表中，“批次数量可用”列指示，除为当前的订单承诺预留已预留的数量，或由源于该类型预留的仓库工作已预留的数量之外，批次数量是否可用。</span><span class="sxs-lookup"><span data-stu-id="97bfe-301">In these tables, the "Batch quantity is available" column indicates whether a batch quantity is available in addition to the quantity that is either already reserved for the current order-committed reservations or already reserved by the warehouse work that originates from reservations of that type.</span></span>

#### <a name="override-the-pick-location-on-the-open-work"></a><span data-ttu-id="97bfe-302">覆盖未结工作上的领料库位</span><span class="sxs-lookup"><span data-stu-id="97bfe-302">Override the pick location on the open work</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="97bfe-303">关键设置参数</span><span class="sxs-lookup"><span data-stu-id="97bfe-303">Key setup parameter</span></span></th>
<th><span data-ttu-id="97bfe-304">批次数量可用</span><span class="sxs-lookup"><span data-stu-id="97bfe-304">Batch quantity is available</span></span></th>
<th><span data-ttu-id="97bfe-305">关键用户步骤</span><span class="sxs-lookup"><span data-stu-id="97bfe-305">Key user steps</span></span></th>
<th><span data-ttu-id="97bfe-306">仓库工作</span><span class="sxs-lookup"><span data-stu-id="97bfe-306">Warehouse work</span></span></th>
<th><span data-ttu-id="97bfe-307">订单承诺批次预留</span><span class="sxs-lookup"><span data-stu-id="97bfe-307">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="97bfe-308"><strong>允许领料库位覆盖</strong>在工作人员上已启用。</span><span class="sxs-lookup"><span data-stu-id="97bfe-308">The <strong>Allow pick location override</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="97bfe-309">是</span><span class="sxs-lookup"><span data-stu-id="97bfe-309">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="97bfe-310">开始领料工作时，在 Warehouse Mmobile App (WMA) 上选择<strong>覆盖库位</strong>菜单项。</span><span class="sxs-lookup"><span data-stu-id="97bfe-310">Select the <strong>Override location</strong> menu item on the Warehouse Mmobile App (WMA) when you start picking work.</span></span></li>
<li><span data-ttu-id="97bfe-311">选择<strong>建议</strong>。</span><span class="sxs-lookup"><span data-stu-id="97bfe-311">Select <strong>Suggest</strong>.</span></span></li>
<li><span data-ttu-id="97bfe-312">根据批次数量的可用性确认建议的新库位。</span><span class="sxs-lookup"><span data-stu-id="97bfe-312">Confirm the new location that is suggested based on batch quantity availability.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="97bfe-313">在当前工作上，将发生以下操作：</span><span class="sxs-lookup"><span data-stu-id="97bfe-313">On the current work, the following actions occur:</span></span>
<ul>
<li><span data-ttu-id="97bfe-314">领料行上的库位已更新为新库位。</span><span class="sxs-lookup"><span data-stu-id="97bfe-314">The location on the pick line is updated to the new location.</span></span> <span data-ttu-id="97bfe-315">（如果库位是由牌照控制的，将为工作库存交易记录分配一个随机牌照，工作人员可以从任何具有可用数量的牌照领料。）</span><span class="sxs-lookup"><span data-stu-id="97bfe-315">(If the location is license plate–controlled, a random license plate is assigned to the work inventory transaction, and the worker can pick from any license plate that has available quantity.)</span></span></li>
<li><span data-ttu-id="97bfe-316">如果在新库位的一个以上牌照中找到数量，原始领料行将拆分成多行以匹配每个牌照。</span><span class="sxs-lookup"><span data-stu-id="97bfe-316">If the quantity is found on more than one license plate in the new location, the original pick line is split into multiple lines to match each license plate.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="97bfe-317">不适用</span><span class="sxs-lookup"><span data-stu-id="97bfe-317">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="97bfe-318">否</span><span class="sxs-lookup"><span data-stu-id="97bfe-318">No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="97bfe-319">开始领料工作时，在 WMA 上选择<strong>覆盖库位</strong>菜单项。</span><span class="sxs-lookup"><span data-stu-id="97bfe-319">Select the <strong>Override location</strong> menu item on the WMA when you start picking work.</span></span></li>
<li><span data-ttu-id="97bfe-320">手动输入库位。</span><span class="sxs-lookup"><span data-stu-id="97bfe-320">Manually enter a location.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="97bfe-321"><strong>覆盖库位</strong>操作无法执行。</span><span class="sxs-lookup"><span data-stu-id="97bfe-321">The <strong>Override location</strong> action isn't possible.</span></span> <span data-ttu-id="97bfe-322">操作失败，并引发错误。</span><span class="sxs-lookup"><span data-stu-id="97bfe-322">It fails, and an error is thrown.</span></span></td>
<td><span data-ttu-id="97bfe-323">不适用</span><span class="sxs-lookup"><span data-stu-id="97bfe-323">Not applicable</span></span></td>
</tr>
</tbody>
</table>

#### <a name="full-button--split-a-work-line-because-of-overflow-on-the-user-location"></a><span data-ttu-id="97bfe-324">“全部”按钮 – 工作行由于用户库位存在溢出被拆分</span><span class="sxs-lookup"><span data-stu-id="97bfe-324">Full button – Split a work line because of overflow on the user location</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="97bfe-325">关键设置参数</span><span class="sxs-lookup"><span data-stu-id="97bfe-325">Key setup parameter</span></span></th>
<th><span data-ttu-id="97bfe-326">批次数量可用</span><span class="sxs-lookup"><span data-stu-id="97bfe-326">Batch quantity is available</span></span></th>
<th><span data-ttu-id="97bfe-327">关键用户步骤</span><span class="sxs-lookup"><span data-stu-id="97bfe-327">Key user steps</span></span></th>
<th><span data-ttu-id="97bfe-328">仓库工作</span><span class="sxs-lookup"><span data-stu-id="97bfe-328">Warehouse work</span></span></th>
<th><span data-ttu-id="97bfe-329">订单承诺批次预留</span><span class="sxs-lookup"><span data-stu-id="97bfe-329">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="97bfe-330"><strong>允许拆分工作</strong>选项在移动设备菜单项上启用。</span><span class="sxs-lookup"><span data-stu-id="97bfe-330">The <strong>Allow splitting of work</strong> option is enabled on the mobile device menu item.</span></span></td>
<td><span data-ttu-id="97bfe-331">不适用</span><span class="sxs-lookup"><span data-stu-id="97bfe-331">Not applicable</span></span></td>
<td>
<ol>
<li><span data-ttu-id="97bfe-332">处理领料工作时，在 WMA 上选择<strong>全部</strong>菜单项。</span><span class="sxs-lookup"><span data-stu-id="97bfe-332">Select the <strong>Full</strong> menu item on the WMA when you process picking work.</span></span></li>
<li><span data-ttu-id="97bfe-333">在<strong>领料数量</strong>字段中，输入需要领料的部分数量来指示全部产能。</span><span class="sxs-lookup"><span data-stu-id="97bfe-333">In the <strong>Pick Qty</strong> field, enter a partial quantity of the required pick to indicate the full capacity.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="97bfe-334">在当前工作上，数量更新为必须领料的剩余数量。</span><span class="sxs-lookup"><span data-stu-id="97bfe-334">On the current work, the quantity is updated to the remaining quantity that must be picked.</span></span></li>
<li><span data-ttu-id="97bfe-335">领料数量的新工作已创建并结束。</span><span class="sxs-lookup"><span data-stu-id="97bfe-335">New work for the picked quantity is created and closed.</span></span></li>
</ul></td>
<td><span data-ttu-id="97bfe-336">不适用</span><span class="sxs-lookup"><span data-stu-id="97bfe-336">Not applicable</span></span></td>
</tr>
</tbody>
</table>

#### <a name="reduce-the-picked-quantity-of-completed-work-from-a-load"></a><span data-ttu-id="97bfe-337">减少已完成工作的领料数量（从负荷）</span><span class="sxs-lookup"><span data-stu-id="97bfe-337">Reduce the picked quantity of completed work (from a load)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="97bfe-338">关键设置参数</span><span class="sxs-lookup"><span data-stu-id="97bfe-338">Key setup parameter</span></span></th>
<th><span data-ttu-id="97bfe-339">批次数量可用</span><span class="sxs-lookup"><span data-stu-id="97bfe-339">Batch quantity is available</span></span></th>
<th><span data-ttu-id="97bfe-340">关键用户步骤</span><span class="sxs-lookup"><span data-stu-id="97bfe-340">Key user steps</span></span></th>
<th><span data-ttu-id="97bfe-341">仓库工作</span><span class="sxs-lookup"><span data-stu-id="97bfe-341">Warehouse work</span></span></th>
<th><span data-ttu-id="97bfe-342">订单承诺批次预留</span><span class="sxs-lookup"><span data-stu-id="97bfe-342">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="97bfe-343">不适用</span><span class="sxs-lookup"><span data-stu-id="97bfe-343">Not applicable</span></span></td>
<td><span data-ttu-id="97bfe-344">是</span><span class="sxs-lookup"><span data-stu-id="97bfe-344">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="97bfe-345">从负荷行打开<strong>减少领料数量</strong>页面。</span><span class="sxs-lookup"><span data-stu-id="97bfe-345">Open the <strong>Reduce picked quantity</strong> page from the load line.</span></span></li>
<li><span data-ttu-id="97bfe-346">输入要取消领料的全部数量。</span><span class="sxs-lookup"><span data-stu-id="97bfe-346">Enter the full quantity to unpick.</span></span></li>
<li><span data-ttu-id="97bfe-347">选择“移至”库位/牌照。</span><span class="sxs-lookup"><span data-stu-id="97bfe-347">Select a "move to" location/license plate.</span></span></li>
</ol>
</td>
<td>
<ul> 
<li><span data-ttu-id="97bfe-348">与负荷行关联的工作被取消。</span><span class="sxs-lookup"><span data-stu-id="97bfe-348">Work that is associated with the load line is canceled.</span></span></li>
<li><span data-ttu-id="97bfe-349">库存变动的新工作已创建并结束。</span><span class="sxs-lookup"><span data-stu-id="97bfe-349">New work for the inventory movement is created and closed.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="97bfe-350">为同一批次重新预留了数量。</span><span class="sxs-lookup"><span data-stu-id="97bfe-350">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="97bfe-351">系统随机分配数量可用的库位和牌照（如果库位是由牌照控制的）。</span><span class="sxs-lookup"><span data-stu-id="97bfe-351">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="97bfe-352">否</span><span class="sxs-lookup"><span data-stu-id="97bfe-352">No</span></span></td>
<td><span data-ttu-id="97bfe-353">查看上一行。</span><span class="sxs-lookup"><span data-stu-id="97bfe-353">See the previous row.</span></span></td>
<td><span data-ttu-id="97bfe-354">查看上一行。</span><span class="sxs-lookup"><span data-stu-id="97bfe-354">See the previous row.</span></span></td>
<td><span data-ttu-id="97bfe-355">已为同一批次，以及取消领料期间输入的同一库位和牌照（如果库位是由牌照控制的）重新预留了数量。</span><span class="sxs-lookup"><span data-stu-id="97bfe-355">The quantity is re-reserved for the same batch, and for the same location and license plate (if the location is license plate–controlled) that were entered during unpicking.</span></span></td>
</tr>
</tbody>
</table>

#### <a name="move-an-item-within-a-warehouse"></a><span data-ttu-id="97bfe-356">在仓库内移动物料</span><span class="sxs-lookup"><span data-stu-id="97bfe-356">Move an item within a warehouse</span></span>

> [!NOTE]
> <span data-ttu-id="97bfe-357">此仓库操作仅适用于**工作创建流程**类型的移动，不适用于模板移动。</span><span class="sxs-lookup"><span data-stu-id="97bfe-357">This warehouse action is applicable only to movement of the **Work creation process** type, not to movement by template.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="97bfe-358">关键设置参数</span><span class="sxs-lookup"><span data-stu-id="97bfe-358">Key setup parameter</span></span></th>
<th><span data-ttu-id="97bfe-359">批次数量可用</span><span class="sxs-lookup"><span data-stu-id="97bfe-359">Batch quantity is available</span></span></th>
<th><span data-ttu-id="97bfe-360">关键用户步骤</span><span class="sxs-lookup"><span data-stu-id="97bfe-360">Key user steps</span></span></th>
<th><span data-ttu-id="97bfe-361">仓库工作</span><span class="sxs-lookup"><span data-stu-id="97bfe-361">Warehouse work</span></span></th>
<th><span data-ttu-id="97bfe-362">订单承诺批次预留</span><span class="sxs-lookup"><span data-stu-id="97bfe-362">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="97bfe-363"><strong>允许包含关联工作的库存移动</strong>选项在工作人员上启用。</span><span class="sxs-lookup"><span data-stu-id="97bfe-363">The <strong>Allow movement of inventory with associated work</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="97bfe-364">是</span><span class="sxs-lookup"><span data-stu-id="97bfe-364">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="97bfe-365">在 WMA 上开始移动。</span><span class="sxs-lookup"><span data-stu-id="97bfe-365">Start a movement on the WMA.</span></span></li>
<li><span data-ttu-id="97bfe-366">输入“起始”和“目标”库位。</span><span class="sxs-lookup"><span data-stu-id="97bfe-366">Enter "from" and "to" locations.</span></span></li>
</ol></td>
<td>
<ul>
<li><span data-ttu-id="97bfe-367">在受移动影响的所有现有工作上，领料库位将更新为新的“目标”库位。</span><span class="sxs-lookup"><span data-stu-id="97bfe-367">On all existing work that is affected by the move, the pick location is updated to the new "to" location.</span></span></li>
<li><span data-ttu-id="97bfe-368">库存变动的新工作已创建并结束。</span><span class="sxs-lookup"><span data-stu-id="97bfe-368">New work for the inventory movement is created and closed.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="97bfe-369">受从给定库位的数量移动影响的所有现有预留已为同一批次重新预留。</span><span class="sxs-lookup"><span data-stu-id="97bfe-369">All existing reservations that are affected by the quantity movement from the given location are re-reserved for the same batch.</span></span> <span data-ttu-id="97bfe-370">系统随机分配数量可用的库位和牌照（如果库位是由牌照控制的）。</span><span class="sxs-lookup"><span data-stu-id="97bfe-370">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="97bfe-371">否</span><span class="sxs-lookup"><span data-stu-id="97bfe-371">No</span></span></td>
<td><span data-ttu-id="97bfe-372">查看上一行。</span><span class="sxs-lookup"><span data-stu-id="97bfe-372">See the previous row.</span></span></td>
<td><span data-ttu-id="97bfe-373">查看上一行。</span><span class="sxs-lookup"><span data-stu-id="97bfe-373">See the previous row.</span></span></td>
<td><span data-ttu-id="97bfe-374">受从给定库位的数量移动影响的所有现有预留已为同一批次，以及新的“目标”库位和牌照（如果库位是由牌照控制的）重新预留。</span><span class="sxs-lookup"><span data-stu-id="97bfe-374">All existing reservations that are affected by the quantity movement from the given location are re-reserved for the same batch, and for the new "to" location and license plate (if the location is license plate–controlled).</span></span></td>
</tr>
</tbody>
</table>

#### <a name="reverse-the-picked-quantity-of-completed-work-from-a-load-or-a-wave"></a><span data-ttu-id="97bfe-375">冲销已完成工作的领料数量（从负荷或波次）</span><span class="sxs-lookup"><span data-stu-id="97bfe-375">Reverse the picked quantity of completed work (from a load or a wave)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="97bfe-376">关键设置参数</span><span class="sxs-lookup"><span data-stu-id="97bfe-376">Key setup parameter</span></span></th>
<th><span data-ttu-id="97bfe-377">批次数量可用</span><span class="sxs-lookup"><span data-stu-id="97bfe-377">Batch quantity is available</span></span></th>
<th><span data-ttu-id="97bfe-378">关键用户步骤</span><span class="sxs-lookup"><span data-stu-id="97bfe-378">Key user steps</span></span></th>
<th><span data-ttu-id="97bfe-379">仓库工作</span><span class="sxs-lookup"><span data-stu-id="97bfe-379">Warehouse work</span></span></th>
<th><span data-ttu-id="97bfe-380">订单承诺批次预留</span><span class="sxs-lookup"><span data-stu-id="97bfe-380">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='6'><span data-ttu-id="97bfe-381">不适用</span><span class="sxs-lookup"><span data-stu-id="97bfe-381">Not applicable</span></span></td>
<td><span data-ttu-id="97bfe-382">是</span><span class="sxs-lookup"><span data-stu-id="97bfe-382">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="97bfe-383">打开<strong>冲销工作</strong>页面。</span><span class="sxs-lookup"><span data-stu-id="97bfe-383">Open the <strong>Reverse work</strong> page.</span></span></li>
<li><span data-ttu-id="97bfe-384">在请求页面上，选择<strong>将物料留在当前库位</strong>选项。</span><span class="sxs-lookup"><span data-stu-id="97bfe-384">On the request page, select the <strong>Leave items at current location</strong> option.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="97bfe-385">与负荷关联的所有工作被取消。</span><span class="sxs-lookup"><span data-stu-id="97bfe-385">All work that is associated with the load is canceled.</span></span></td>
<td><span data-ttu-id="97bfe-386">为同一批次重新预留了数量。</span><span class="sxs-lookup"><span data-stu-id="97bfe-386">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="97bfe-387">系统随机分配数量可用的库位和牌照（如果库位是由牌照控制的）。</span><span class="sxs-lookup"><span data-stu-id="97bfe-387">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="97bfe-388">否</span><span class="sxs-lookup"><span data-stu-id="97bfe-388">No</span></span></td>
<td><span data-ttu-id="97bfe-389">查看上一行。</span><span class="sxs-lookup"><span data-stu-id="97bfe-389">See the previous row.</span></span></td>
<td><span data-ttu-id="97bfe-390">查看上一行。</span><span class="sxs-lookup"><span data-stu-id="97bfe-390">See the previous row.</span></span></td>
<td><span data-ttu-id="97bfe-391">数量已为同一批次以及在冲销后保留数量的库位和牌照重新预留。</span><span class="sxs-lookup"><span data-stu-id="97bfe-391">The quantity is re-reserved for the same batch, and for the location and license plate where the quantity was left upon reversal.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="97bfe-392">是</span><span class="sxs-lookup"><span data-stu-id="97bfe-392">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="97bfe-393">打开<strong>冲销工作</strong>页面。</span><span class="sxs-lookup"><span data-stu-id="97bfe-393">Open the <strong>Reverse work</strong> page.</span></span></li>
<li><span data-ttu-id="97bfe-394">在请求页面上，选择<strong>将物料分配给此库位</strong>选项。</span><span class="sxs-lookup"><span data-stu-id="97bfe-394">On the request page, select the <strong>Assign items to this location</strong> option.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="97bfe-395">当前工作被取消。</span><span class="sxs-lookup"><span data-stu-id="97bfe-395">The current work is canceled.</span></span></li>
<li><span data-ttu-id="97bfe-396">库存变动的新工作已创建并结束。</span><span class="sxs-lookup"><span data-stu-id="97bfe-396">New work for the inventory movement is created and closed.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="97bfe-397">为同一批次重新预留了数量。</span><span class="sxs-lookup"><span data-stu-id="97bfe-397">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="97bfe-398">系统随机分配数量可用的库位和牌照（如果库位是由牌照控制的）。</span><span class="sxs-lookup"><span data-stu-id="97bfe-398">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="97bfe-399">否</span><span class="sxs-lookup"><span data-stu-id="97bfe-399">No</span></span></td>
<td><span data-ttu-id="97bfe-400">查看上一行。</span><span class="sxs-lookup"><span data-stu-id="97bfe-400">See the previous row.</span></span></td>
<td><span data-ttu-id="97bfe-401">查看上一行。</span><span class="sxs-lookup"><span data-stu-id="97bfe-401">See the previous row.</span></span></td>
<td><span data-ttu-id="97bfe-402">数量已为同一批次以及在冲销后向其分配数量的库位和牌照重新预留。</span><span class="sxs-lookup"><span data-stu-id="97bfe-402">The quantity is re-reserved for the same batch, and for the location and license plate that the quantity was assigned to upon reversal.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="97bfe-403">是/否</span><span class="sxs-lookup"><span data-stu-id="97bfe-403">Yes/No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="97bfe-404">打开<strong>冲销工作</strong>页面。</span><span class="sxs-lookup"><span data-stu-id="97bfe-404">Open the <strong>Reverse work</strong> page.</span></span></li>
<li><span data-ttu-id="97bfe-405">在请求页面上，选择<strong>将物料移到此库位</strong>选项。</span><span class="sxs-lookup"><span data-stu-id="97bfe-405">On the request page, select the <strong>Move items to this location</strong> option.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="97bfe-406">不支持冲销。</span><span class="sxs-lookup"><span data-stu-id="97bfe-406">Reversal isn't supported.</span></span></td>
<td><span data-ttu-id="97bfe-407">不适用</span><span class="sxs-lookup"><span data-stu-id="97bfe-407">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="97bfe-408">是/否</span><span class="sxs-lookup"><span data-stu-id="97bfe-408">Yes/No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="97bfe-409">打开<strong>冲销工作</strong>页面。</span><span class="sxs-lookup"><span data-stu-id="97bfe-409">Open the <strong>Reverse work</strong> page.</span></span></li>
<li><span data-ttu-id="97bfe-410">在请求页面上，选择<strong>根据库位指令移动物料</strong>选项。</span><span class="sxs-lookup"><span data-stu-id="97bfe-410">On the request page, select the <strong>Move items based on location directives</strong> option.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="97bfe-411">不支持冲销。</span><span class="sxs-lookup"><span data-stu-id="97bfe-411">Reversal isn't supported.</span></span> </td>
<td><span data-ttu-id="97bfe-412">不适用</span><span class="sxs-lookup"><span data-stu-id="97bfe-412">Not applicable</span></span></td>
</tr>
</tbody>
</table>

#### <a name="short-pick-a-quantity--register-the-quantity-as-physically-not-found-at-the-locationlicense-plate-while-you-perform-picking-work"></a><span data-ttu-id="97bfe-413">领料短缺数量 – 登记在执行领料工作时，在库位/牌照上实际未找到的数量</span><span class="sxs-lookup"><span data-stu-id="97bfe-413">Short-pick a quantity – Register the quantity as physically not found at the location/license plate while you perform picking work</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="97bfe-414">关键设置参数</span><span class="sxs-lookup"><span data-stu-id="97bfe-414">Key setup parameter</span></span></th>
<th><span data-ttu-id="97bfe-415">批次数量可用</span><span class="sxs-lookup"><span data-stu-id="97bfe-415">Batch quantity is available</span></span></th>
<th><span data-ttu-id="97bfe-416">关键用户步骤</span><span class="sxs-lookup"><span data-stu-id="97bfe-416">Key user steps</span></span></th>
<th><span data-ttu-id="97bfe-417">仓库工作</span><span class="sxs-lookup"><span data-stu-id="97bfe-417">Warehouse work</span></span></th>
<th><span data-ttu-id="97bfe-418">订单承诺批次预留</span><span class="sxs-lookup"><span data-stu-id="97bfe-418">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="97bfe-419">设置<strong>领料短缺</strong>类型的工作异常，其中，<strong>物料重新分配</strong> = <strong>无</strong>，<strong>调整库存</strong> = <strong>是</strong>，<strong>删除预留</strong> = <strong>否</strong>。</span><span class="sxs-lookup"><span data-stu-id="97bfe-419">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>None</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>No</strong>.</span></span></td>
<td><span data-ttu-id="97bfe-420">是</span><span class="sxs-lookup"><span data-stu-id="97bfe-420">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="97bfe-421">运行领料工作时，在 WMA 上选择<strong>ShortPick</strong>菜单项。</span><span class="sxs-lookup"><span data-stu-id="97bfe-421">Select the <strong>Shortpick</strong> menu item on the WMA when you run picking work.</span></span></li>
<li><span data-ttu-id="97bfe-422">在<strong>领料数量</strong>字段中，输入<strong>0</strong>（零）。</span><span class="sxs-lookup"><span data-stu-id="97bfe-422">In the <strong>Pick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="97bfe-423">在<strong>原因</strong>字段中，输入<strong>未重新分配</strong>。</span><span class="sxs-lookup"><span data-stu-id="97bfe-423">In the <strong>Reason</strong> field, enter <strong>No reallocation</strong>.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="97bfe-424">当前工作已结束，领料数量为 0（零）。</span><span class="sxs-lookup"><span data-stu-id="97bfe-424">The current work is closed, and the picked quantity is 0 (zero).</span></span></li>
<li><span data-ttu-id="97bfe-425"><strong>盘点</strong>类型和<strong>已售出</strong>发货类型的库存交易记录已创建来表示调整。</span><span class="sxs-lookup"><span data-stu-id="97bfe-425">An inventory transaction of the <strong>Counting</strong> type and the <strong>Sold</strong> issue type is created to represent the adjustment.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="97bfe-426">为同一批次重新预留了数量。</span><span class="sxs-lookup"><span data-stu-id="97bfe-426">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="97bfe-427">系统随机分配数量可用的库位和牌照（如果库位是由牌照控制的）。</span><span class="sxs-lookup"><span data-stu-id="97bfe-427">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="97bfe-428">否</span><span class="sxs-lookup"><span data-stu-id="97bfe-428">No</span></span></td>
<td><span data-ttu-id="97bfe-429">查看上一行。</span><span class="sxs-lookup"><span data-stu-id="97bfe-429">See the previous row.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="97bfe-430">领料短缺操作失败，并引发错误。</span><span class="sxs-lookup"><span data-stu-id="97bfe-430">The short-picking action fails, and an error is thrown.</span></span></li>
<li><span data-ttu-id="97bfe-431">当前工作保持未结状态。</span><span class="sxs-lookup"><span data-stu-id="97bfe-431">The current work remains open.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="97bfe-432">不适用</span><span class="sxs-lookup"><span data-stu-id="97bfe-432">Not applicable</span></span></td>
</tr>
<tr>
<td rowspan='2'><span data-ttu-id="97bfe-433">设置<strong>领料短缺</strong>类型的工作异常，其中，<strong>物料重新分配</strong> = <strong>无</strong>，<strong>调整库存</strong> = <strong>是</strong>，<strong>删除预留</strong> = <strong>是</strong>。</span><span class="sxs-lookup"><span data-stu-id="97bfe-433">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>None</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>Yes</strong>.</span></span></td>
<td><span data-ttu-id="97bfe-434">是</span><span class="sxs-lookup"><span data-stu-id="97bfe-434">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="97bfe-435">运行领料工作时，在 WMA 上选择<strong>ShortPick</strong>菜单项。</span><span class="sxs-lookup"><span data-stu-id="97bfe-435">Select the <strong>Shortpick</strong> menu item on the WMA when you run picking work.</span></span></li>
<li><span data-ttu-id="97bfe-436">在<strong>领料数量</strong>字段中，输入<strong>0</strong>（零）。</span><span class="sxs-lookup"><span data-stu-id="97bfe-436">In the <strong>Pick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="97bfe-437">在<strong>原因</strong>字段中，输入<strong>未重新分配</strong>。</span><span class="sxs-lookup"><span data-stu-id="97bfe-437">In the <strong>Reason</strong> field, enter <strong>No reallocation</strong>.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="97bfe-438">当前工作已结束，领料数量为 0（零）。</span><span class="sxs-lookup"><span data-stu-id="97bfe-438">The current work is closed, and the picked quantity is 0 (zero).</span></span></li>
<li><span data-ttu-id="97bfe-439"><strong>盘点</strong>类型和<strong>已售出</strong>发货类型的库存交易记录已创建来表示调整。</span><span class="sxs-lookup"><span data-stu-id="97bfe-439">An inventory transaction of the <strong>Counting</strong> type and the <strong>Sold</strong> issue type is created to represent the adjustment.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="97bfe-440">受领料短缺库位的数量调整影响的所有现有预留已为同一批次重新预留。</span><span class="sxs-lookup"><span data-stu-id="97bfe-440">All existing reservations that are affected by the quantity adjustment in the short-picked location are re-reserved for the same batch.</span></span> <span data-ttu-id="97bfe-441">系统随机分配数量可用的库位和牌照（如果库位是由牌照控制的）。</span><span class="sxs-lookup"><span data-stu-id="97bfe-441">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="97bfe-442">否</span><span class="sxs-lookup"><span data-stu-id="97bfe-442">No</span></span></td>
<td><span data-ttu-id="97bfe-443">查看上一行。</span><span class="sxs-lookup"><span data-stu-id="97bfe-443">See the previous row.</span></span></td>
<td><span data-ttu-id="97bfe-444">查看上一行。</span><span class="sxs-lookup"><span data-stu-id="97bfe-444">See the previous row.</span></span></td>
<td><span data-ttu-id="97bfe-445">受领料短缺库位的数量调整影响的所有现有预留已删除。</span><span class="sxs-lookup"><span data-stu-id="97bfe-445">All existing reservations that are affected by the quantity adjustment in the short-picked location are removed.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="97bfe-446">设置<strong>领料短缺</strong>类型的工作异常，其中，<strong>物料重新分配</strong> = <strong>手动</strong>，<strong>调整库存</strong> = <strong>是</strong>，<strong>删除预留</strong> = <strong>否/是</strong>。</span><span class="sxs-lookup"><span data-stu-id="97bfe-446">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>Manual</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>No/Yes</strong>.</span></span> <span data-ttu-id="97bfe-447">此外，<strong>允许手动重新分配物料</strong>选项在工作人员上启用。</span><span class="sxs-lookup"><span data-stu-id="97bfe-447">Additionally, the <strong>Allow manual item reallocation</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="97bfe-448">是</span><span class="sxs-lookup"><span data-stu-id="97bfe-448">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="97bfe-449">运行领料工作时，在 WMA 上选择<strong>ShortPick</strong>菜单项。</span><span class="sxs-lookup"><span data-stu-id="97bfe-449">Select the <strong>Shortpick</strong> menu item on the WMA when you run picking work.</span></span></li>
<li><span data-ttu-id="97bfe-450">在<strong>领料短缺数量</strong>字段中，输入<strong>0</strong>（零）。</span><span class="sxs-lookup"><span data-stu-id="97bfe-450">In the <strong>Shortpick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="97bfe-451">在<strong>原因</strong>字段中，选择<strong>手动重新分配领料短缺</strong>。</span><span class="sxs-lookup"><span data-stu-id="97bfe-451">In the <strong>Reason</strong> field, select <strong>Short Picking with manual reallocation</strong>.</span></span></li>
<li><span data-ttu-id="97bfe-452">在列表中选择库位/牌照。</span><span class="sxs-lookup"><span data-stu-id="97bfe-452">Select the location/license plate in the list.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="97bfe-453">在当前工作上，将发生以下操作：</span><span class="sxs-lookup"><span data-stu-id="97bfe-453">On the current work, the following actions occur:</span></span>
<ul>
<li><span data-ttu-id="97bfe-454">领料行已关闭，领料数量为 0（零）。</span><span class="sxs-lookup"><span data-stu-id="97bfe-454">The pick line is closed, and the picked quantity is 0 (zero).</span></span></li>
<li><span data-ttu-id="97bfe-455">放置行被取消。</span><span class="sxs-lookup"><span data-stu-id="97bfe-455">The put line is canceled.</span></span></li>
<li><span data-ttu-id="97bfe-456">新领料行创建。</span><span class="sxs-lookup"><span data-stu-id="97bfe-456">A new pick line is created.</span></span> <span data-ttu-id="97bfe-457">它使用用户选择的库位/牌照。</span><span class="sxs-lookup"><span data-stu-id="97bfe-457">It uses the location/license plate that the user selected.</span></span></li>
<li><span data-ttu-id="97bfe-458">新放置行创建。</span><span class="sxs-lookup"><span data-stu-id="97bfe-458">A new put line is created.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="97bfe-459"><strong>盘点</strong>类型和<strong>已售出</strong>发货类型的库存交易记录已创建来表示调整。</span><span class="sxs-lookup"><span data-stu-id="97bfe-459">An inventory transaction of the <strong>Counting</strong> type and the <strong>Sold</strong> issue type is created to represent the adjustment.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="97bfe-460">不适用</span><span class="sxs-lookup"><span data-stu-id="97bfe-460">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="97bfe-461">设置<strong>领料短缺</strong>类型的工作异常，其中，<strong>物料重新分配</strong> = <strong>手动</strong>，<strong>调整库存</strong> = <strong>是</strong>，<strong>删除预留</strong> = <strong>否</strong>。</span><span class="sxs-lookup"><span data-stu-id="97bfe-461">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>Manual</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>No</strong>.</span></span> <span data-ttu-id="97bfe-462">此外，<strong>允许手动重新分配物料</strong>选项在工作人员上启用。</span><span class="sxs-lookup"><span data-stu-id="97bfe-462">Additionally, the <strong>Allow manual item reallocation</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="97bfe-463">否</span><span class="sxs-lookup"><span data-stu-id="97bfe-463">No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="97bfe-464">运行领料工作时，在 WMA 上选择<strong>ShortPick</strong>菜单项。</span><span class="sxs-lookup"><span data-stu-id="97bfe-464">Select the <strong>Shortpick</strong> menu item on the WMA when you run picking work.</span></span></li>
<li><span data-ttu-id="97bfe-465">在<strong>领料短缺数量</strong>字段中，输入<strong>0</strong>（零）。</span><span class="sxs-lookup"><span data-stu-id="97bfe-465">In the <strong>Shortpick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="97bfe-466">在<strong>原因</strong>字段中，选择<strong>手动重新分配领料短缺</strong>。</span><span class="sxs-lookup"><span data-stu-id="97bfe-466">In the <strong>Reason</strong> field, select <strong>Short Picking with manual reallocation</strong>.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="97bfe-467">领料短缺操作失败，并引发错误。</span><span class="sxs-lookup"><span data-stu-id="97bfe-467">The short-picking action fails, and an error is thrown.</span></span></td>
<td><span data-ttu-id="97bfe-468">不适用</span><span class="sxs-lookup"><span data-stu-id="97bfe-468">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="97bfe-469">设置<strong>领料短缺</strong>类型的工作异常，其中，<strong>物料重新分配</strong> = <strong>手动</strong>，<strong>调整库存</strong> = <strong>是</strong>，<strong>删除预留</strong> = <strong>是</strong>。</span><span class="sxs-lookup"><span data-stu-id="97bfe-469">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>Manual</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>Yes</strong>.</span></span> <span data-ttu-id="97bfe-470">此外，<strong>允许手动重新分配物料</strong>选项在工作人员上启用。</span><span class="sxs-lookup"><span data-stu-id="97bfe-470">Additionally, the <strong>Allow manual item reallocation</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="97bfe-471">否</span><span class="sxs-lookup"><span data-stu-id="97bfe-471">No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="97bfe-472">运行领料工作时，在 WMA 上选择<strong>ShortPick</strong>菜单项。</span><span class="sxs-lookup"><span data-stu-id="97bfe-472">Select the <strong>Shortpick</strong> menu item on the WMA when you run picking work.</span></span></li>
<li><span data-ttu-id="97bfe-473">在<strong>领料短缺数量</strong>字段中，输入<strong>0</strong>（零）。</span><span class="sxs-lookup"><span data-stu-id="97bfe-473">In the <strong>Shortpick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="97bfe-474">在<strong>原因</strong>字段中，选择<strong>手动重新分配领料短缺</strong>。</span><span class="sxs-lookup"><span data-stu-id="97bfe-474">In the <strong>Reason</strong> field, select <strong>Short Picking with manual reallocation</strong>.</span></span></li>
<li><span data-ttu-id="97bfe-475">在列表中选择库位/牌照。</span><span class="sxs-lookup"><span data-stu-id="97bfe-475">Select the location/license plate in the list.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="97bfe-476">在当前工作上，将发生以下操作：</span><span class="sxs-lookup"><span data-stu-id="97bfe-476">On the current work, the following actions occur:</span></span>
<ul>
<li><span data-ttu-id="97bfe-477">领料行已关闭，领料数量为 0（零）。</span><span class="sxs-lookup"><span data-stu-id="97bfe-477">The pick line is closed, and the picked quantity is 0 (zero).</span></span></li>
<li><span data-ttu-id="97bfe-478">放置行被取消。</span><span class="sxs-lookup"><span data-stu-id="97bfe-478">The put line is canceled.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="97bfe-479"><strong>盘点</strong>类型和<strong>已售出</strong>发货类型的库存交易记录已创建来表示调整。</span><span class="sxs-lookup"><span data-stu-id="97bfe-479">An inventory transaction of the <strong>Counting</strong> type and the <strong>Sold</strong> issue type is created to represent the adjustment.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="97bfe-480">受领料短缺库位/牌照的数量调整影响的所有现有预留已删除。</span><span class="sxs-lookup"><span data-stu-id="97bfe-480">All existing reservations that are affected by the quantity adjustment in the short-picked location/license plate are removed.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="97bfe-481">设置<strong>领料短缺</strong>类型的工作异常，其中，<strong>物料重新分配</strong> = <strong>自动</strong>，<strong>调整库存</strong> = <strong>是/否</strong>，<strong>删除预留</strong> = <strong>是/否</strong>。</span><span class="sxs-lookup"><span data-stu-id="97bfe-481">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>Automatic</strong>, <strong>Adjust inventory</strong> = <strong>Yes/No</strong>, and <strong>Remove reservations</strong> = <strong>Yes/No</strong>.</span></span></td>
<td><span data-ttu-id="97bfe-482">不适用</span><span class="sxs-lookup"><span data-stu-id="97bfe-482">Not applicable</span></span></td>
<td>
<ol>
<li><span data-ttu-id="97bfe-483">运行领料工作时，在 WMA 上选择<strong>ShortPick</strong>菜单项。</span><span class="sxs-lookup"><span data-stu-id="97bfe-483">Select the <strong>Shortpick</strong> menu item on the WMA when you run picking work.</span></span></li>
<li><span data-ttu-id="97bfe-484">在<strong>领料短缺数量</strong>字段中，输入<strong>0</strong>（零）。</span><span class="sxs-lookup"><span data-stu-id="97bfe-484">In the <strong>Shortpick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="97bfe-485">在<strong>原因</strong>字段中，选择<strong>自动重新分配领料短缺</strong>。</span><span class="sxs-lookup"><span data-stu-id="97bfe-485">In the <strong>Reason</strong> field, select <strong>Short Picking with automatic reallocation</strong>.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="97bfe-486">不支持涉及自动重新分配的领料短缺。</span><span class="sxs-lookup"><span data-stu-id="97bfe-486">Short-picking that involves automatic reallocation isn't supported.</span></span></td>
<td><span data-ttu-id="97bfe-487">不支持涉及自动重新分配的领料短缺。</span><span class="sxs-lookup"><span data-stu-id="97bfe-487">Short-picking that involves automatic reallocation isn't supported.</span></span></td>
</tr>
</tbody>
</table>

#### <a name="change-the-inventory-status"></a><span data-ttu-id="97bfe-488">更改库存状态</span><span class="sxs-lookup"><span data-stu-id="97bfe-488">Change the inventory status</span></span>

> [!NOTE]
> <span data-ttu-id="97bfe-489">可以从多个入口点执行此仓库操作。</span><span class="sxs-lookup"><span data-stu-id="97bfe-489">This warehouse action can be performed from multiple entry points.</span></span> <span data-ttu-id="97bfe-490">此处显示的示例使用**按库位显示的现有量**页面的**库存状态更改**操作。</span><span class="sxs-lookup"><span data-stu-id="97bfe-490">The example that is shown here uses **Inventory status change** action on the **On-hand by location** page.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="97bfe-491">关键设置参数</span><span class="sxs-lookup"><span data-stu-id="97bfe-491">Key setup parameter</span></span></th>
<th><span data-ttu-id="97bfe-492">批次数量可用</span><span class="sxs-lookup"><span data-stu-id="97bfe-492">Batch quantity is available</span></span></th>
<th><span data-ttu-id="97bfe-493">关键用户步骤</span><span class="sxs-lookup"><span data-stu-id="97bfe-493">Key user steps</span></span></th>
<th><span data-ttu-id="97bfe-494">仓库工作</span><span class="sxs-lookup"><span data-stu-id="97bfe-494">Warehouse work</span></span></th>
<th><span data-ttu-id="97bfe-495">订单承诺批次预留</span><span class="sxs-lookup"><span data-stu-id="97bfe-495">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="97bfe-496">在<strong>仓库</strong>选项卡上，在<strong>仓库</strong>记录中，<strong>删除预留和标记</strong>字段设置为<strong>预留</strong>或<strong>标记和预留</strong>。</span><span class="sxs-lookup"><span data-stu-id="97bfe-496">On the <strong>Warehouse</strong> tab, in the <strong>Warehouse</strong> record, the <strong>Remove reservations and markings</strong> field is set to <strong>Reservations</strong> or <strong>Markings and reservations</strong>.</span></span></td>
<td><span data-ttu-id="97bfe-497">是</span><span class="sxs-lookup"><span data-stu-id="97bfe-497">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="97bfe-498">选择特定位置。</span><span class="sxs-lookup"><span data-stu-id="97bfe-498">Select a specific location.</span></span></li>
<li><span data-ttu-id="97bfe-499">选择具有特定物料、库位和牌照的行（如果库位是由牌照控制的）。</span><span class="sxs-lookup"><span data-stu-id="97bfe-499">Select a line that has a specific item, location, and license plate (if the location is license plate–controlled).</span></span></li>
<li><span data-ttu-id="97bfe-500">选择<strong>库存状态更改</strong>。</span><span class="sxs-lookup"><span data-stu-id="97bfe-500">Select <strong>Inventory status change</strong>.</span></span></li>
<li><span data-ttu-id="97bfe-501">将<strong>库存状态</strong>字段设置为<strong>锁定</strong>。</span><span class="sxs-lookup"><span data-stu-id="97bfe-501">Set the <strong>Inventory status</strong> field to <strong>Blocking</strong>.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="97bfe-502">为工作预留的数量不允许库存状态更改。</span><span class="sxs-lookup"><span data-stu-id="97bfe-502">Inventory status changes aren't allowed for quantities that are reserved for work.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="97bfe-503">为同一批次重新预留了数量。</span><span class="sxs-lookup"><span data-stu-id="97bfe-503">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="97bfe-504">系统随机分配数量可用的库位和牌照（如果库位是由牌照控制的）。</span><span class="sxs-lookup"><span data-stu-id="97bfe-504">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></li>
<li><span data-ttu-id="97bfe-505"><strong>库存状态更改</strong>的两个库存交易记录已创建，来表示库存状态维度的更改。</span><span class="sxs-lookup"><span data-stu-id="97bfe-505">Two inventory transactions of the <strong>Inventory status change</strong> type are created to represent the change in the inventory status dimension.</span></span></li>
<li><span data-ttu-id="97bfe-506"><strong>库存锁定</strong>类型和<strong>实际预留</strong>发货类型的库存交易记录已创建，来表示锁定数量的预留。</span><span class="sxs-lookup"><span data-stu-id="97bfe-506">An inventory transaction of the <strong>Inventory blocking</strong> type and the <strong>Reserved physical</strong> issue type is created to represent the reservation of the blocked quantity.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="97bfe-507">否</span><span class="sxs-lookup"><span data-stu-id="97bfe-507">No</span></span></td>
<td><span data-ttu-id="97bfe-508">查看上一行。</span><span class="sxs-lookup"><span data-stu-id="97bfe-508">See the previous row.</span></span></td>
<td><span data-ttu-id="97bfe-509">为工作预留的数量不允许库存状态更改。</span><span class="sxs-lookup"><span data-stu-id="97bfe-509">Inventory status changes aren't allowed for quantities that are reserved for work.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="97bfe-510">预留被删除。</span><span class="sxs-lookup"><span data-stu-id="97bfe-510">The reservation is removed.</span></span></li>
<li><span data-ttu-id="97bfe-511"><strong>库存状态更改</strong>的两个库存交易记录已创建，来表示库存状态维度的更改。</span><span class="sxs-lookup"><span data-stu-id="97bfe-511">Two inventory transactions of the <strong>Inventory status change</strong> type are created to represent the change in the inventory status dimension.</span></span></li>
<li><span data-ttu-id="97bfe-512"><strong>库存锁定</strong>类型和<strong>实际预留</strong>发货类型的库存交易记录已创建，来表示锁定数量的预留。</span><span class="sxs-lookup"><span data-stu-id="97bfe-512">An inventory transaction of the <strong>Inventory blocking</strong> type and the <strong>Reserved physical</strong> issue type is created to represent the reservation of the blocked quantity.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td rowspan='2'><span data-ttu-id="97bfe-513">在<strong>仓库</strong>选项卡上，在<strong>仓库</strong>记录中，<strong>删除预留和标记</strong>字段设置为<strong>无</strong>。</span><span class="sxs-lookup"><span data-stu-id="97bfe-513">On the <strong>Warehouse</strong> tab, in the <strong>Warehouse</strong> record, the <strong>Remove reservations and markings</strong> field is set to <strong>None</strong>.</span></span></td>
<td><span data-ttu-id="97bfe-514">是</span><span class="sxs-lookup"><span data-stu-id="97bfe-514">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="97bfe-515">选择特定位置。</span><span class="sxs-lookup"><span data-stu-id="97bfe-515">Select a specific location.</span></span></li>
<li><span data-ttu-id="97bfe-516">选择具有特定物料、库位和牌照的行（如果库位是由牌照控制的）。</span><span class="sxs-lookup"><span data-stu-id="97bfe-516">Select a line that has a specific item, location, and license plate (if the location is license plate–controlled).</span></span></li>
<li><span data-ttu-id="97bfe-517">选择<strong>库存状态更改</strong>。</span><span class="sxs-lookup"><span data-stu-id="97bfe-517">Select <strong>Inventory status change</strong>.</span></span></li>
<li><span data-ttu-id="97bfe-518">将<strong>库存状态</strong>字段设置为<strong>锁定</strong>。</span><span class="sxs-lookup"><span data-stu-id="97bfe-518">Set the <strong>Inventory status</strong> field to <strong>Blocking</strong>.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="97bfe-519">为工作预留的数量不允许库存状态更改。</span><span class="sxs-lookup"><span data-stu-id="97bfe-519">Inventory status changes aren't allowed for quantities that are reserved for work.</span></span></td>
<td><span data-ttu-id="97bfe-520">为同一批次重新预留了数量。</span><span class="sxs-lookup"><span data-stu-id="97bfe-520">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="97bfe-521">系统随机分配数量可用的库位和牌照（如果库位是由牌照控制的）。</span><span class="sxs-lookup"><span data-stu-id="97bfe-521">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="97bfe-522">否</span><span class="sxs-lookup"><span data-stu-id="97bfe-522">No</span></span></td>
<td><span data-ttu-id="97bfe-523">查看上一行。</span><span class="sxs-lookup"><span data-stu-id="97bfe-523">See the previous row.</span></span></td>
<td><span data-ttu-id="97bfe-524">为工作预留的数量不允许库存状态更改。</span><span class="sxs-lookup"><span data-stu-id="97bfe-524">Inventory status changes aren't allowed for quantities that are reserved for work.</span></span></td>
<td><span data-ttu-id="97bfe-525">不允许库存状态更改。</span><span class="sxs-lookup"><span data-stu-id="97bfe-525">Inventory status changes aren't allowed.</span></span></td>
</tr>
</tbody>
</table>

## <a name="limitations"></a><span data-ttu-id="97bfe-526">限制</span><span class="sxs-lookup"><span data-stu-id="97bfe-526">Limitations</span></span>

- <span data-ttu-id="97bfe-527">灵活的仓库级维度预留功能不支持以下功能：</span><span class="sxs-lookup"><span data-stu-id="97bfe-527">The flexible warehouse-level dimension reservation functionality doesn't support the following features:</span></span>

    - <span data-ttu-id="97bfe-528">实际称重管理</span><span class="sxs-lookup"><span data-stu-id="97bfe-528">Catch weight management</span></span>
    - <span data-ttu-id="97bfe-529">允许实际负库存</span><span class="sxs-lookup"><span data-stu-id="97bfe-529">Physical negative inventory</span></span>
    - <span data-ttu-id="97bfe-530">按订购的供应预留</span><span class="sxs-lookup"><span data-stu-id="97bfe-530">Reservation against ordered supply</span></span>
    - <span data-ttu-id="97bfe-531">转移单和原材料领料</span><span class="sxs-lookup"><span data-stu-id="97bfe-531">Transfer orders and raw material picking</span></span>

- <span data-ttu-id="97bfe-532">按指令单位包装的集装箱合并规则有局限性。</span><span class="sxs-lookup"><span data-stu-id="97bfe-532">The container consolidation rule for packing by directive unit has limitations.</span></span> <span data-ttu-id="97bfe-533">对于订单承诺预留，我们建议您不要在**按指令单位包装**字段已启用的情况下使用集装箱生成模板。</span><span class="sxs-lookup"><span data-stu-id="97bfe-533">For order-committed reservations, we recommend that you not use container build templates where the **Pack by directive unit** field is enabled.</span></span> <span data-ttu-id="97bfe-534">在当前的设计中，创建仓库工作时不使用库位指令。</span><span class="sxs-lookup"><span data-stu-id="97bfe-534">In the current design, location directives aren't used when warehouse work is created.</span></span> <span data-ttu-id="97bfe-535">因此，在集装化波次步骤期间，仅应用单位序列组中的最低单位（库存单位）。</span><span class="sxs-lookup"><span data-stu-id="97bfe-535">Therefore, only the lowest unit in the unit sequence group (the inventory unit) is applied during the containerization wave step.</span></span>