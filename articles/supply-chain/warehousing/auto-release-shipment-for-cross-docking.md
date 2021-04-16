---
title: 越库配送的自动下达装运
description: 本主题介绍越库配送策略，当提供需求数量的生产订单完工入库时，它让您可以自动将需求订单下达到仓库，以便将数量直接从生产输出位置移动到出库货位。
author: omulvad
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSCrossDockingTemplate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2019-10-1
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 1c831030659b38b52932e504f744d24d999958a5
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5831426"
---
# <a name="auto-release-shipment-for-cross-docking"></a><span data-ttu-id="0df37-103">越库配送的自动下达装运</span><span class="sxs-lookup"><span data-stu-id="0df37-103">Auto-release shipment for cross-docking</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0df37-104">本主题介绍越库配送策略，当提供需求数量的生产订单完工入库时，它让您可以自动将需求订单下达到仓库。</span><span class="sxs-lookup"><span data-stu-id="0df37-104">This topic describes a cross-docking strategy that lets you automatically release a demand order to the warehouse when the production order that supplies the demand quantity is reported as finished.</span></span> <span data-ttu-id="0df37-105">以此方式，履行需求订单所需的数量将直接从生产输出位置移动到出库货位。</span><span class="sxs-lookup"><span data-stu-id="0df37-105">In this way, the quantity that is required for fulfillment of the demand order is moved directly from the production output location to the outbound location.</span></span>

<span data-ttu-id="0df37-106">越库配送是一种仓库处理流程，其中履行出站订单所需的数量从接收入站订单的位置定向到订单的出库台或暂存区域。</span><span class="sxs-lookup"><span data-stu-id="0df37-106">Cross-docking is a warehouse handling flow where the quantity that is required to fulfill an outbound order is directed to the order's outbound dock or staging area from the location where the inbound order was received.</span></span> <span data-ttu-id="0df37-107">（入站订单可以是采购订单、转移单或生产订单。）而高级越库配送功能支持所有供应和需求订单，它需要在确定越库配送机会之前下达出站需求，自动下达装运功能具有以下特征：</span><span class="sxs-lookup"><span data-stu-id="0df37-107">(The inbound order can be a purchase order, a transfer order, or a production order.) Whereas the Advanced cross-docking feature supports all supply and demand orders, and it requires that the outbound demand be released before the cross-dock opportunity is identified, the Auto-release shipment feature has these characteristics:</span></span>

- <span data-ttu-id="0df37-108">它仅支持将生产订单作为供应，将销售订单和转移单作为需求。</span><span class="sxs-lookup"><span data-stu-id="0df37-108">It supports only production orders as supply, and only sales orders and transfer orders as demand.</span></span>
- <span data-ttu-id="0df37-109">即使在登记供应收货之前（即在生产完工入库之前）未将需求订单下达到仓库，也可以开始越库配送操作。</span><span class="sxs-lookup"><span data-stu-id="0df37-109">The cross-docking operation can be started even if the demand order wasn't released to the warehouse before the supply receipt was registered (that is, before the production was reported as finished).</span></span>

<span data-ttu-id="0df37-110">此越库配送功能具有两个优点：</span><span class="sxs-lookup"><span data-stu-id="0df37-110">This cross-docking functionality has two advantages:</span></span>

- <span data-ttu-id="0df37-111">如果只是再次提取这些数量的成品以履行出站订单，则仓库操作可以跳过将一定数量的成品入库到常规仓库存储区的步骤。</span><span class="sxs-lookup"><span data-stu-id="0df37-111">The warehouse operations can skip the step of putting away quantities of finished goods to the regular warehouse storage area if those quantities will just be picked up again to fulfill the outbound order.</span></span> <span data-ttu-id="0df37-112">取而代之的是，这些数量可以一次从输出位置移动到包装/运输位置。</span><span class="sxs-lookup"><span data-stu-id="0df37-112">Instead, the quantities can be moved one time, from the output location to a packing/shipping location.</span></span> <span data-ttu-id="0df37-113">这样，该功能有助于最大程度地减少存货的处理次数，并最终帮助最大限度地节省仓库车间的时间和空间。</span><span class="sxs-lookup"><span data-stu-id="0df37-113">In this way, the functionality helps minimize the number of times that stock is handled and, ultimately, helps maximize time and space savings on the warehouse shop floor.</span></span>
- <span data-ttu-id="0df37-114">仓库操作可以推迟销售订单的下达，并将订单转移到仓库，直到关联生产订单的成品输出已完工入库。</span><span class="sxs-lookup"><span data-stu-id="0df37-114">The warehouse operations can postpone the release of sales orders and transfer orders to the warehouse until the output of finished goods for the associated production order is reported as finished.</span></span> <span data-ttu-id="0df37-115">此优点在按订单生产环境中尤其重要，在这种环境中，制造提前期往往比按库存生产环境中的提前期要长。</span><span class="sxs-lookup"><span data-stu-id="0df37-115">This advantage might be especially relevant in make-to-order production environments, where manufacturing lead times tend to be longer than the lead times in make-to-stock environments.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="0df37-116">先决条件</span><span class="sxs-lookup"><span data-stu-id="0df37-116">Prerequisites</span></span>

| <span data-ttu-id="0df37-117">必备项</span><span class="sxs-lookup"><span data-stu-id="0df37-117">Prerequisite</span></span> | <span data-ttu-id="0df37-118">说明</span><span class="sxs-lookup"><span data-stu-id="0df37-118">Description</span></span> |
|---|---|
| <span data-ttu-id="0df37-119">项目</span><span class="sxs-lookup"><span data-stu-id="0df37-119">Item</span></span> | <span data-ttu-id="0df37-120">物料必须在仓库管理流程中启用。</span><span class="sxs-lookup"><span data-stu-id="0df37-120">The item must be enabled for warehouse management processes.</span></span><p><span data-ttu-id="0df37-121">**注意：** 启用实际称重的物料不能包含在越库配送流程中。</span><span class="sxs-lookup"><span data-stu-id="0df37-121">**Note:** Catch-weight-enabled items can't be included in the cross-docking processes.</span></span></p> |
| <span data-ttu-id="0df37-122">存放地点</span><span class="sxs-lookup"><span data-stu-id="0df37-122">Warehouse</span></span> | <span data-ttu-id="0df37-123">仓库必须在仓库管理流程中启用。</span><span class="sxs-lookup"><span data-stu-id="0df37-123">The warehouse must be enabled for warehouse management processes.</span></span> |
| <span data-ttu-id="0df37-124">越库配送模板</span><span class="sxs-lookup"><span data-stu-id="0df37-124">Cross-docking templates</span></span> | <span data-ttu-id="0df37-125">必须为指定仓库至少设置一个使用 **在供应收货时** 需求下达政策的越库配送模板。</span><span class="sxs-lookup"><span data-stu-id="0df37-125">At least one cross-docking template that uses the **At supply receipt** demand release policy must be set up for a given warehouse.</span></span> |
| <span data-ttu-id="0df37-126">工作类</span><span class="sxs-lookup"><span data-stu-id="0df37-126">Work class</span></span> | <span data-ttu-id="0df37-127">必须为 **越库配送** 工作订单类型创建越库配送工作类 ID。</span><span class="sxs-lookup"><span data-stu-id="0df37-127">A cross-docking work class ID must be created for the **Cross docking** work order type.</span></span> |
| <span data-ttu-id="0df37-128">工作模板</span><span class="sxs-lookup"><span data-stu-id="0df37-128">Work templates</span></span> | <span data-ttu-id="0df37-129">需要使用 **越库配送** 工作订单类型的工作模板才能创建越库配送领料和放置工作。</span><span class="sxs-lookup"><span data-stu-id="0df37-129">Work templates of the **Cross docking** work order type are required to create cross-docking pick and put work.</span></span> |
| <span data-ttu-id="0df37-130">位置指令</span><span class="sxs-lookup"><span data-stu-id="0df37-130">Location directives</span></span> | <span data-ttu-id="0df37-131">需要使用 **越库配送** 工作订单类型的位置指令，以指导将打包和装运批量销售订单的位置的放置工作。</span><span class="sxs-lookup"><span data-stu-id="0df37-131">Location directives of the **Cross docking** work order type are required to guide put work in the locations where sales order quantities will be packed and shipped.</span></span> |
| <span data-ttu-id="0df37-132">需求订单和生产订单之间的标记</span><span class="sxs-lookup"><span data-stu-id="0df37-132">Marking between a demand order and a production order</span></span> | <span data-ttu-id="0df37-133">仅当根据生产订单预留销售订单和转移单并进行标记时，仓库系统才可以触发出站订单装运的自动下达，并从输出位置按完工入库操作创建越库配送工作。</span><span class="sxs-lookup"><span data-stu-id="0df37-133">The warehouse system can trigger automatic release of the outbound order shipment and create cross-docking work from the output location at the report-as-finished action only if sales orders and transfer orders are reserved and marked against a production order.</span></span> |

## <a name="example-cross-docking-flow"></a><span data-ttu-id="0df37-134">越库配送流示例</span><span class="sxs-lookup"><span data-stu-id="0df37-134">Example cross-docking flow</span></span>

<span data-ttu-id="0df37-135">典型的越库配送流包括以下主要步骤。</span><span class="sxs-lookup"><span data-stu-id="0df37-135">A typical cross-docking flow consists of the following main steps.</span></span>

1. <span data-ttu-id="0df37-136">销售订单接受者为按订单生产产品创建销售订单。</span><span class="sxs-lookup"><span data-stu-id="0df37-136">A sales order taker creates a sales order for a make-to-order product.</span></span> <span data-ttu-id="0df37-137">通常，请求数量并不是现有量，必须先进行生产。</span><span class="sxs-lookup"><span data-stu-id="0df37-137">Typically, the requested quantity isn't on hand and must first be produced.</span></span>
2. <span data-ttu-id="0df37-138">销售订单接受者直接从销售订单行创建生产订单。</span><span class="sxs-lookup"><span data-stu-id="0df37-138">The sales order taker creates a production order directly from the sales order line.</span></span> <span data-ttu-id="0df37-139">这样，销售订单接受者就可以根据生产订单数量预留和标记销售订单数量。</span><span class="sxs-lookup"><span data-stu-id="0df37-139">In this way, the sales order taker reserves and marks the sales order quantity against the production order quantity.</span></span> 

    <span data-ttu-id="0df37-140">或者，生产规划员指定在确认计划订单时必须更新标记。</span><span class="sxs-lookup"><span data-stu-id="0df37-140">Alternatively, a production planner specifies that the marking must be updated when planned orders are being firmed.</span></span>

3. <span data-ttu-id="0df37-141">生产订单执行以下步骤：</span><span class="sxs-lookup"><span data-stu-id="0df37-141">The production order goes through the following steps:</span></span>

    1. <span data-ttu-id="0df37-142">生产规划员评估并下达生产订单。</span><span class="sxs-lookup"><span data-stu-id="0df37-142">A production planner estimates and releases the production order.</span></span> <span data-ttu-id="0df37-143">（评估包括原材料预留，下达包括下达到仓库。）</span><span class="sxs-lookup"><span data-stu-id="0df37-143">(Estimation includes raw material reservation, and the release includes the release to a warehouse.)</span></span>
    2. <span data-ttu-id="0df37-144">仓库工作人员根据生产领料工作开始并完成从存储位置到生产输入位置的原材料领料。</span><span class="sxs-lookup"><span data-stu-id="0df37-144">A warehouse worker starts and completes raw material picking from the storage location to the production input location, according to the production pick work.</span></span>
    3. <span data-ttu-id="0df37-145">车间操作员开始生产订单。</span><span class="sxs-lookup"><span data-stu-id="0df37-145">A shop floor operator starts the production order.</span></span>
    4. <span data-ttu-id="0df37-146">在最后一项操作中，机器操作员使用移动设备报告生产订单已完工入库。</span><span class="sxs-lookup"><span data-stu-id="0df37-146">In the last operation, a machine operator uses the mobile device to report the production order as finished.</span></span>

4. <span data-ttu-id="0df37-147">系统使用设置来标识两个链接的订单的越库配送事件，然后完成以下任务：</span><span class="sxs-lookup"><span data-stu-id="0df37-147">The system uses the setup to identify the cross-docking event for the two linked orders and then completes these tasks:</span></span>

    1. <span data-ttu-id="0df37-148">自动将关联的销售订单下达到仓库以创建装运。</span><span class="sxs-lookup"><span data-stu-id="0df37-148">Automatically release the associated sales order to a warehouse to create a shipment.</span></span>
    2. <span data-ttu-id="0df37-149">自动创建越库配送工作，该工作具有从输出位置提取成品并将其移动到越库配送位置指令分配给销售订单的出库货位的说明。</span><span class="sxs-lookup"><span data-stu-id="0df37-149">Automatically create cross-docking work that has instructions to pick the finished goods from the output location and move them to the outbound location that the cross-docking location directives assigned to the sales order.</span></span>
    3. <span data-ttu-id="0df37-150">在生产订单已完工入库后，提示机器操作员立即完成越库配送工作。</span><span class="sxs-lookup"><span data-stu-id="0df37-150">Prompt a machine operator to complete the cross-docking work immediately after the production order is reported as finished.</span></span>

5. <span data-ttu-id="0df37-151">在越库配送工作完成并将数量装载到车辆上后，出库仓库规划员确认销售装运。</span><span class="sxs-lookup"><span data-stu-id="0df37-151">After the cross-docking work is completed, and quantities are loaded onto the vehicle, an outbound warehouse planner confirms the sales shipment.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="0df37-152">示例场景</span><span class="sxs-lookup"><span data-stu-id="0df37-152">Example scenario</span></span>

<span data-ttu-id="0df37-153">对于此情况，必须安装演示数据，并且必须使用 **USMF** 演示数据公司。</span><span class="sxs-lookup"><span data-stu-id="0df37-153">For this scenario, you must have demo data installed, and you must use the **USMF** demo data company.</span></span>

### <a name="set-up-cross-docking-that-uses-the-auto-release-shipment-feature"></a><span data-ttu-id="0df37-154">设置使用自动下达装运功能的越库配送</span><span class="sxs-lookup"><span data-stu-id="0df37-154">Set up cross-docking that uses the auto-release shipment feature</span></span>

#### <a name="cross-docking-template"></a><span data-ttu-id="0df37-155">越库配送模板</span><span class="sxs-lookup"><span data-stu-id="0df37-155">Cross-docking template</span></span>

1. <span data-ttu-id="0df37-156">转到 **仓库管理** \> **设置** \> **工作** \> **越库配送模板**。</span><span class="sxs-lookup"><span data-stu-id="0df37-156">Go to **Warehouse management** \> **Setup** \> **Work** \> **Cross docking templates**.</span></span>
2. <span data-ttu-id="0df37-157">选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="0df37-157">Select **New**.</span></span>
3. <span data-ttu-id="0df37-158">在 **序列号** 字段中，输入 **1**。</span><span class="sxs-lookup"><span data-stu-id="0df37-158">In the **Sequence number** field, enter **1**.</span></span>
4. <span data-ttu-id="0df37-159">在 **越库配送模板 ID** 字段中，输入名称，如 **XDock\_RAF**。</span><span class="sxs-lookup"><span data-stu-id="0df37-159">In the **Cross docking template ID** field, enter a name, such as **XDock\_RAF**.</span></span>
5. <span data-ttu-id="0df37-160">在 **需求下达政策** 字段中，选择 **在供应收货时**。</span><span class="sxs-lookup"><span data-stu-id="0df37-160">In the **Demand release policy** field, select **At supply receipt**.</span></span>
6. <span data-ttu-id="0df37-161">在 **仓库** 字段中，输入您要在其中设置越库配送流程的仓库的编号。</span><span class="sxs-lookup"><span data-stu-id="0df37-161">In the **Warehouse** field, enter the number of the warehouse where you want to set up the cross-docking process.</span></span> <span data-ttu-id="0df37-162">在这个例子中选择 **51**。</span><span class="sxs-lookup"><span data-stu-id="0df37-162">For this example, select **51**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="0df37-163">一旦选择 **在供应收货时** 作为模板的需求下达政策，页面上的所有其他字段将不可用。</span><span class="sxs-lookup"><span data-stu-id="0df37-163">As soon as you select **At supply receipt** as the demand release policy for the template, all other fields on the page become unavailable.</span></span> <span data-ttu-id="0df37-164">同样，您不能定义任何供应来源。</span><span class="sxs-lookup"><span data-stu-id="0df37-164">Likewise, you can't define any supply sources.</span></span> <span data-ttu-id="0df37-165">发生此行为的原因在于，使用自动下达装运功能的越库配送仅支持将生产订单作为供应来源，并且需要销售订单与生产订单之间存在标记。</span><span class="sxs-lookup"><span data-stu-id="0df37-165">This behavior occurs because cross-docking that uses the auto-release shipment feature supports only production orders as supply sources, and it requires that a marking exist between sales orders and production orders.</span></span> <span data-ttu-id="0df37-166">如果您选择 **在供应收货前** 作为需求下达政策，则 **计划** 和 **供应来源** 选项卡上的字段可用，并且可以进行编辑。</span><span class="sxs-lookup"><span data-stu-id="0df37-166">If you select **Before supply receipt** as the demand release policy, the fields on the **Planning** and **Supply sources** tabs are available and can be edited.</span></span>

#### <a name="work-classes"></a><span data-ttu-id="0df37-167">工作类</span><span class="sxs-lookup"><span data-stu-id="0df37-167">Work classes</span></span>

1. <span data-ttu-id="0df37-168">转到 **仓库管理** \> **设置** \> **工作** \> **工作类**。</span><span class="sxs-lookup"><span data-stu-id="0df37-168">Go to **Warehouse management** \> **Setup** \> **Work** \> **Work classes**.</span></span>
2. <span data-ttu-id="0df37-169">选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="0df37-169">Select **New**.</span></span>
3. <span data-ttu-id="0df37-170">在 **工作类 ID** 字段中，输入名称，如 **CrossDock**。</span><span class="sxs-lookup"><span data-stu-id="0df37-170">In the **Work class ID** field, enter a name, such as **CrossDock**.</span></span>
4. <span data-ttu-id="0df37-171">在 **工作订单类型** 字段中，选择 **越库配送**。</span><span class="sxs-lookup"><span data-stu-id="0df37-171">In the **Work order type** field, select **Cross docking**.</span></span>

<span data-ttu-id="0df37-172">要限制可以放置越库配送的成品的货位类型，您可以指定一种或多种有效的货位类型。</span><span class="sxs-lookup"><span data-stu-id="0df37-172">To limit the types of locations where cross-docked finished goods can be put, you can specify one or more valid location types.</span></span>

#### <a name="work-templates"></a><span data-ttu-id="0df37-173">工作模板</span><span class="sxs-lookup"><span data-stu-id="0df37-173">Work templates</span></span>

1. <span data-ttu-id="0df37-174">转到 **仓库管理** \> **设置** \> **工作** \> **工作模板**。</span><span class="sxs-lookup"><span data-stu-id="0df37-174">Go to **Warehouse management** \> **Setup** \> **Work** \> **Work templates**.</span></span>
2. <span data-ttu-id="0df37-175">在 **工作订单类型** 字段中，选择 **越库配送**。</span><span class="sxs-lookup"><span data-stu-id="0df37-175">In the **Work order type** field, select **Cross docking**.</span></span>
3. <span data-ttu-id="0df37-176">选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="0df37-176">Select **New**.</span></span>
4. <span data-ttu-id="0df37-177">在 **序列号** 字段中，输入 **1**。</span><span class="sxs-lookup"><span data-stu-id="0df37-177">In the **Sequence number** field, enter **1**.</span></span>
5. <span data-ttu-id="0df37-178">在 **工作模板** 字段中，输入名称，如 **CrossDock\_51**。</span><span class="sxs-lookup"><span data-stu-id="0df37-178">In the **Work template** field, enter a name, such as **CrossDock\_51**.</span></span>
6. <span data-ttu-id="0df37-179">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="0df37-179">Select **Save**.</span></span>
7. <span data-ttu-id="0df37-180">在 **工作模板详细信息** 部分，选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="0df37-180">In the **Work Template Details** section, select **New**.</span></span>
8. <span data-ttu-id="0df37-181">对于新行，在 **工作类型** 字段中，选择 **领料**。</span><span class="sxs-lookup"><span data-stu-id="0df37-181">For the new line, in the **Work type** field, select **Pick**.</span></span> <span data-ttu-id="0df37-182">在 **工作类 ID** 字段中，选择 **CrossDock**。</span><span class="sxs-lookup"><span data-stu-id="0df37-182">In the **Work class ID** field, select **CrossDock**.</span></span>
9. <span data-ttu-id="0df37-183">选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="0df37-183">Select **New**.</span></span>
10. <span data-ttu-id="0df37-184">对于新行，在 **工作类型** 字段中，选择 **放置**。</span><span class="sxs-lookup"><span data-stu-id="0df37-184">For the new line, in the **Work type** field, select **Put**.</span></span> <span data-ttu-id="0df37-185">在 **工作类 ID** 字段中，选择 **CrossDock**。</span><span class="sxs-lookup"><span data-stu-id="0df37-185">In the **Work class ID** field, select **CrossDock**.</span></span>

#### <a name="location-directives"></a><span data-ttu-id="0df37-186">位置指令</span><span class="sxs-lookup"><span data-stu-id="0df37-186">Location directives</span></span>

<span data-ttu-id="0df37-187">成品的标准储存流程需要 **放置** 位置指令，以指导将领料的生产数量移动到常规存储空间。</span><span class="sxs-lookup"><span data-stu-id="0df37-187">A standard put-away process for finished goods requires a **Put** location directive to guide the movement of picked production quantities to a regular storage space.</span></span> <span data-ttu-id="0df37-188">同样，您必须设置越库配送 **放置** 位置指令，以指示工作将完成的数量放置在供关联的销售订单的装运使用的指定出库货位。</span><span class="sxs-lookup"><span data-stu-id="0df37-188">Likewise, you must set up a cross-docking **Put** location directive to instruct the work to put the finished quantity in a designated outbound location that services the shipment of the associated sales order.</span></span>

<span data-ttu-id="0df37-189">对于越库配送，对于常规的成品储存，您不必为领料工作操作创建位置指令，因为已经指定了输出位置。</span><span class="sxs-lookup"><span data-stu-id="0df37-189">For cross-docking, as for regular put-away of finished goods, you don't have to create a location directive for the pick work action, because the output location is given.</span></span> <span data-ttu-id="0df37-190">此外，此输出位置应该设置为资源相关记录之一（即资源、资源组关系或资源组）上的默认输出位置，或者设置为仓库的默认生产成品位置。</span><span class="sxs-lookup"><span data-stu-id="0df37-190">Additionally, this output location is expected to be set up either as the default output location on one of the resource-related records (that is, the resource, resource group relation, or resource group) or as a default production finished goods location for a warehouse.</span></span>

1. <span data-ttu-id="0df37-191">转到 **仓库管理** \> **设置** \> **货位指令**。</span><span class="sxs-lookup"><span data-stu-id="0df37-191">Go to **Warehouse management** \> **Setup** \> **Location directives**.</span></span>
2. <span data-ttu-id="0df37-192">在 **工作订单类型** 字段中，选择 **越库配送**。</span><span class="sxs-lookup"><span data-stu-id="0df37-192">In the **Work order type** field, select **Cross docking**.</span></span>
3. <span data-ttu-id="0df37-193">选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="0df37-193">Select **New**.</span></span>
4. <span data-ttu-id="0df37-194">在 **序列号** 字段中，输入 **1**。</span><span class="sxs-lookup"><span data-stu-id="0df37-194">In the **Sequence number** field, enter **1**.</span></span>
5. <span data-ttu-id="0df37-195">在 **名称** 字段中，输入名称，如 **Baydoor**。</span><span class="sxs-lookup"><span data-stu-id="0df37-195">In the **Name** field, enter a name, such as **Baydoor**.</span></span>
6. <span data-ttu-id="0df37-196">在 **工作类型** 字段中，选择 **放置**。</span><span class="sxs-lookup"><span data-stu-id="0df37-196">In the **Work type** field, select **Put**.</span></span>
7. <span data-ttu-id="0df37-197">在 **站点** 字段中，选择 **5**。</span><span class="sxs-lookup"><span data-stu-id="0df37-197">In the **Site** field, select **5**.</span></span>
8. <span data-ttu-id="0df37-198">在 **仓库** 字段中，选择 **51**。</span><span class="sxs-lookup"><span data-stu-id="0df37-198">In the **Warehouse** field, select **51**.</span></span>
9. <span data-ttu-id="0df37-199">在 **行** 快速选项卡上，选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="0df37-199">On the **Lines** FastTab, select **New**.</span></span>
10. <span data-ttu-id="0df37-200">在 **目标数量** 字段中，输入范围的最大数量，如 **1000000**。</span><span class="sxs-lookup"><span data-stu-id="0df37-200">In the **To quantity** field, enter the maximum quantity of the range, such as **1000000**.</span></span>
11. <span data-ttu-id="0df37-201">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="0df37-201">Select **Save**.</span></span>
12. <span data-ttu-id="0df37-202">在 **位置指令操作** 快速选项卡上，选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="0df37-202">On the **Location Directives Actions** FastTab, select **New**.</span></span>
13. <span data-ttu-id="0df37-203">在 **名称** 字段中，输入名称，如 **Baydoor**。</span><span class="sxs-lookup"><span data-stu-id="0df37-203">In the **Name** field, enter a name, such as **Baydoor**.</span></span>
14. <span data-ttu-id="0df37-204">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="0df37-204">Select **Save**.</span></span>
15. <span data-ttu-id="0df37-205">您可以使用标准查询工具将放置位置限制为一个或多个特定位置。</span><span class="sxs-lookup"><span data-stu-id="0df37-205">You can use the standard query facility to limit put locations to one or more specific locations.</span></span> <span data-ttu-id="0df37-206">选择 **编辑查询**，然后在 **位置** 表中选择 **51** 作为 **仓库** 字段的条件。</span><span class="sxs-lookup"><span data-stu-id="0df37-206">Select **Edit query**, and select **51** as the criterion for the **Warehouse** field in the **Locations** table.</span></span>

### <a name="cross-dock-finished-goods-to-the-outbound-location"></a><span data-ttu-id="0df37-207">将成品越库配送到出库货位</span><span class="sxs-lookup"><span data-stu-id="0df37-207">Cross-dock finished goods to the outbound location</span></span>

<span data-ttu-id="0df37-208">要将成品数量越库配送到关联的销售订单的出库货位，请按照以下步骤操作。</span><span class="sxs-lookup"><span data-stu-id="0df37-208">To cross-dock the quantity of finished goods to the outbound location of the associated sales order, follow these steps.</span></span>

1. <span data-ttu-id="0df37-209">转到 **销售和营销** \> **销售订单** \> **所有销售订单**。</span><span class="sxs-lookup"><span data-stu-id="0df37-209">Go to **Sales and marketing** \> **Sales orders** \> **All sales orders**.</span></span>
2. <span data-ttu-id="0df37-210">选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="0df37-210">Select **New**.</span></span>
3. <span data-ttu-id="0df37-211">对于销售订单抬头，选择客户帐户 **US-001** 以及为使用自动下达装运功能的越库配送设置的仓库。</span><span class="sxs-lookup"><span data-stu-id="0df37-211">For the sales order header, select customer account **US-001** and a warehouse that is set up for cross-docking that uses the auto-release shipment feature.</span></span>
4. <span data-ttu-id="0df37-212">为成品添加一行，然后输入 **10** 作为数量。</span><span class="sxs-lookup"><span data-stu-id="0df37-212">Add a line for a finished product, and enter **10** as the quantity.</span></span>
5. <span data-ttu-id="0df37-213">在 **销售订单行** 部分，选择 **产品和供应** \> **生产订单**。</span><span class="sxs-lookup"><span data-stu-id="0df37-213">In the **Sales order lines** section, select **Product and supply** \> **Production order**.</span></span>
6. <span data-ttu-id="0df37-214">在 **创建生产订单** 对话框中，查看默认值，然后选择 **创建**。</span><span class="sxs-lookup"><span data-stu-id="0df37-214">In the **Create production order** dialog box, review the default values, and then select **Create**.</span></span> <span data-ttu-id="0df37-215">新生产订单已创建并链接到销售订单（即其已预留并标记）。</span><span class="sxs-lookup"><span data-stu-id="0df37-215">A new production order is created and linked to the sales order (that is, it's reserved and marked).</span></span>
7. <span data-ttu-id="0df37-216">可选：更改 **数量** 字段的值，使其大于履行销售订单所需的值。</span><span class="sxs-lookup"><span data-stu-id="0df37-216">Optional: Change the value of the **Quantity** field so that it's more than the value that is required to fulfill the sales order.</span></span> <span data-ttu-id="0df37-217">当生产数量已完工入库时，系统将根据处理成品储存的常规过程为标记的数量创建越库配送工作，并为剩余数量创建储存工作。</span><span class="sxs-lookup"><span data-stu-id="0df37-217">When the production quantity is reported as finished, the system will create cross-docking work for the marked quantity and put-away work for the remaining quantity, according to the regular procedure for handling the put-away of finished goods.</span></span>

    <span data-ttu-id="0df37-218">如前所述，销售订单和生产订单之间必须存在标记。</span><span class="sxs-lookup"><span data-stu-id="0df37-218">As was mentioned earlier, a marking must exist between the sales order and the production order.</span></span> <span data-ttu-id="0df37-219">否则，越库配送将无法运行。</span><span class="sxs-lookup"><span data-stu-id="0df37-219">Otherwise, the cross-docking won't work.</span></span> <span data-ttu-id="0df37-220">可以通过多种方式创建标记：</span><span class="sxs-lookup"><span data-stu-id="0df37-220">A marking can be created in the multiple ways:</span></span>

    - <span data-ttu-id="0df37-221">在以下情况下，系统可以自动创建标记：</span><span class="sxs-lookup"><span data-stu-id="0df37-221">The system can automatically create the marking in the following situations:</span></span>

        - <span data-ttu-id="0df37-222">生产订单直接从销售订单行手动创建（请参见步骤 6）。</span><span class="sxs-lookup"><span data-stu-id="0df37-222">The production order is manually created directly from the sales order line (see step 6).</span></span>
        - <span data-ttu-id="0df37-223">计划生产订单已确认，并且 **更新标记** 字段设置为 **标准**。</span><span class="sxs-lookup"><span data-stu-id="0df37-223">Planned production orders are firmed, and the **Update marking** field is set to **Standard**.</span></span>

    - <span data-ttu-id="0df37-224">用户可以通过从需求订单行打开 **标记** 页面来手动创建标记。</span><span class="sxs-lookup"><span data-stu-id="0df37-224">The user can manually create the marking by opening the **Marking** page from the demand order line.</span></span>

    > [!NOTE]
    > <span data-ttu-id="0df37-225">无法为设置为使用标准和加权平均作为库存模型的物料手动创建标记。</span><span class="sxs-lookup"><span data-stu-id="0df37-225">A marking can't be manually created for items that are set up to use standard and weighted average as inventory models.</span></span>

8. <span data-ttu-id="0df37-226">在 **生产订单** 页面上的“操作”窗格上，在 **生产订单** 选项卡上的 **流程** 组中，选择 **评估**，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="0df37-226">On the **Production order** page, on the Action Pane, on the **Production order** tab, in the **Process** group, select **Estimate**, and then select **OK**.</span></span> <span data-ttu-id="0df37-227">订单已评估，并为生产预留了原材料数量。</span><span class="sxs-lookup"><span data-stu-id="0df37-227">The order is estimated, and the raw material quantity is reserved for the production.</span></span>
9. <span data-ttu-id="0df37-228">在“操作”窗格上，在 **生产订单** 选项卡上的 **流程** 组中，选择评估，选择 **下达**，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="0df37-228">On the Action Pane, on the **Production order** tab, in the **Process** group, select **Release**, and then select **OK**.</span></span> <span data-ttu-id="0df37-229">将为原材料创建仓库领料工作。</span><span class="sxs-lookup"><span data-stu-id="0df37-229">Warehouse pick work is created for the raw materials.</span></span>
10. <span data-ttu-id="0df37-230">打开并查看工作。</span><span class="sxs-lookup"><span data-stu-id="0df37-230">Open and review the work.</span></span> <span data-ttu-id="0df37-231">在“操作”窗格的 **仓库** 选项卡上，在 **常规** 组中，选择 **工作详细信息**。</span><span class="sxs-lookup"><span data-stu-id="0df37-231">On the Action Pane, on the **Warehouse** tab, in the **General** group, select **Work details**.</span></span> <span data-ttu-id="0df37-232">记录工作 ID。</span><span class="sxs-lookup"><span data-stu-id="0df37-232">Make a note of the work ID.</span></span>
11. <span data-ttu-id="0df37-233">登录到仓库管理移动应用以在仓库 51 中运行工作。</span><span class="sxs-lookup"><span data-stu-id="0df37-233">Sign in to the Warehouse Management mobile app to run work in warehouse 51.</span></span>
12. <span data-ttu-id="0df37-234">转到 **生产** \> **生产领料**。</span><span class="sxs-lookup"><span data-stu-id="0df37-234">Go to **Production** \> **Production pick**.</span></span>
13. <span data-ttu-id="0df37-235">输入工作 ID 以开始并完成原材料领料。</span><span class="sxs-lookup"><span data-stu-id="0df37-235">Enter the work ID to start and complete the raw material picking.</span></span> 

    <span data-ttu-id="0df37-236">在工作完工入库后，将在生产输入位置（USMF 演示数据中的 **005**）提供原材料的数量，然后可以开始执行生产订单。</span><span class="sxs-lookup"><span data-stu-id="0df37-236">After the work is reported as finished, the quantity of raw materials is available in the production input location (**005** in USMF demo data), and execution of the production order can start.</span></span>

14. <span data-ttu-id="0df37-237">在 **生产订单** 页面上的“操作”窗格上，在 **生产订单** 选项卡上的 **流程** 组中，选择 **开始**，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="0df37-237">On the **Production order** page, on the Action Pane, on the **Production order** tab, in the **Process** group, select **Start**, and then select **OK**.</span></span>
15. <span data-ttu-id="0df37-238">在应用中，转到 **生产** \> **RAF 和储存**。</span><span class="sxs-lookup"><span data-stu-id="0df37-238">In the app, go to **Production** \> **RAF and put away**.</span></span>
16. <span data-ttu-id="0df37-239">在 **生产 ID** 字段中，输入生产订单编号和其他必填详细信息，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="0df37-239">In the **Prod ID** field, enter the production order number and other mandatory details, and then select **OK**.</span></span>

<span data-ttu-id="0df37-240">请注意，将发生以下事件：</span><span class="sxs-lookup"><span data-stu-id="0df37-240">Notice that the following events occur:</span></span>

- <span data-ttu-id="0df37-241">为链接的销售订单触发下达到仓库。</span><span class="sxs-lookup"><span data-stu-id="0df37-241">The release to a warehouse is triggered for the linked sales order.</span></span>
- <span data-ttu-id="0df37-242">根据下达，装运和越库配送工作将创建。</span><span class="sxs-lookup"><span data-stu-id="0df37-242">Based on the release, shipment and cross-docking work is created.</span></span> <span data-ttu-id="0df37-243">此工作指示仓库操作员领取履行销售订单行所需的数量，并将它们放入越库配送位置指令中指定的出库货位。</span><span class="sxs-lookup"><span data-stu-id="0df37-243">This work instructs the warehouse operator to pick the quantities that are required to fulfill the sales order line and put them in the outbound location that specified in the cross-docking location directive.</span></span>
- <span data-ttu-id="0df37-244">如果生产订单数量大于销售订单所需的数量，则会创建常规储存工作。</span><span class="sxs-lookup"><span data-stu-id="0df37-244">If the production order quantity is more than the quantity that is required by the sales order, regular put-away work is created.</span></span> <span data-ttu-id="0df37-245">此工作指示仓库操作员根据位置指令，领取越库配送后剩余的成品数量，并将其移至常规存储。</span><span class="sxs-lookup"><span data-stu-id="0df37-245">This work instructs the warehouse operator to pick the quantity of finished goods that remains after cross-docking and move it to regular storage, according to the location directive.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]