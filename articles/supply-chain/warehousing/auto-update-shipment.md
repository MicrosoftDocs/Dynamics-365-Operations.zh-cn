---
title: 装运自动更新
description: 本主题概述了为装运提供自动更新的功能。
author: josaw1
manager: tfehr
ms.date: 11/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWaveTemplateTable,SalesTableListPage,SalesTable,WHSWaveTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 1f75e9421ab9cac0b62e1cdee17ecf74796783cc
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "5001216"
---
# <a name="shipment-auto-updates"></a><span data-ttu-id="8e91a-103">装运自动更新</span><span class="sxs-lookup"><span data-stu-id="8e91a-103">Shipment auto-updates</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8e91a-104">在将负荷发放到仓库后，自动更新装运功能会自动更新与装运关联的负荷行上的数量（增加和减少）。</span><span class="sxs-lookup"><span data-stu-id="8e91a-104">The auto-update shipment functionality automatically updates quantities (both increases and decreases) on a load line that is associated with a shipment, after the load has been released to a warehouse.</span></span> <span data-ttu-id="8e91a-105">此功能将保持打开状态，直到装运或负荷上的负荷行在波次中处理。</span><span class="sxs-lookup"><span data-stu-id="8e91a-105">This functionality remains turned on until the load line on the shipment or load is processed on a wave.</span></span> <span data-ttu-id="8e91a-106">使用此功能时，订单更新可以自动流过仓库，而无需手动干预，直到仓库工作已创建。</span><span class="sxs-lookup"><span data-stu-id="8e91a-106">When it's used, order updates can automatically flow through to the warehouse, without requiring manual intervention, until warehouse work is created.</span></span>

<span data-ttu-id="8e91a-107">当不使用自动更新装运功能时，只有数量减少会自动流过，直到仓库工作创建。</span><span class="sxs-lookup"><span data-stu-id="8e91a-107">When the auto-update shipment functionality isn't used, only quantity decreases automatically flow until warehouse work is created.</span></span> <span data-ttu-id="8e91a-108">用户必须手动更新或删除行，然后如果订单数量增加或添加了新订单行，则他们必须重新发放行。</span><span class="sxs-lookup"><span data-stu-id="8e91a-108">Users must manually update or delete lines, and they must then re-release lines if order quantities are increased or new order lines are added.</span></span> <span data-ttu-id="8e91a-109">通过使用自动更新装运功能，企业可以无缝地向仓库提供更新，而不必担心相关的装运和负荷不会反映出订单行更新。</span><span class="sxs-lookup"><span data-stu-id="8e91a-109">By using the auto-update shipment functionality, businesses can seamlessly provide updates to the warehouse without having to worry that related shipments and loads won't reflect order line updates.</span></span>

<span data-ttu-id="8e91a-110">自动更新装运功能适用于销售订单行和转移单行，其已为特定仓库打开。</span><span class="sxs-lookup"><span data-stu-id="8e91a-110">The auto-update shipment functionality applies to both sales order lines and transfer order lines, and it's turned on for a specific warehouse.</span></span> <span data-ttu-id="8e91a-111">因此，公司可以根据需要在仓库之间应用不同的自动更新装运策略。</span><span class="sxs-lookup"><span data-stu-id="8e91a-111">Therefore, companies can apply different auto-update shipment policies across warehouses, as they require.</span></span> <span data-ttu-id="8e91a-112">默认情况下，数量减少的自动更新装运策略适用于所有使用仓库管理流程的仓库。</span><span class="sxs-lookup"><span data-stu-id="8e91a-112">By default, the auto-update shipment policy for quantity decreases is applied for all warehouses that use warehouse management processes.</span></span> <span data-ttu-id="8e91a-113">使用此默认策略设置时，只有数量减少会自动流过装运和负荷，直到仓库工作创建为止。</span><span class="sxs-lookup"><span data-stu-id="8e91a-113">When this default policy setting is used, only quantity decreases automatically flow through to a shipment and load until warehouse work is created.</span></span> <span data-ttu-id="8e91a-114">此行为类似于在引入自动更新装运功能之前使用的行为。</span><span class="sxs-lookup"><span data-stu-id="8e91a-114">This behavior resembles the behavior that was used before the auto-update shipment functionality was introduced.</span></span>

## <a name="main-elements-of-the-functionality"></a><span data-ttu-id="8e91a-115">功能的主要元素</span><span class="sxs-lookup"><span data-stu-id="8e91a-115">Main elements of the functionality</span></span>

<span data-ttu-id="8e91a-116">自动更新装运功能主要依靠装运状态来确定在销售订单行或转移单行上进行更改时是否应更改负荷行上的数量。</span><span class="sxs-lookup"><span data-stu-id="8e91a-116">The auto-update shipment functionality relies primarily on the shipment status to determine whether the quantity on a load line should be changed when a change is made on a sales order line or transfer order line.</span></span> <span data-ttu-id="8e91a-117">它还主要依靠装运状态来确定何时应将新负荷行自动添加到现有负荷中。</span><span class="sxs-lookup"><span data-stu-id="8e91a-117">It also relies primarily on the shipment status to determine when a new load line should automatically be added to an existing load.</span></span> <span data-ttu-id="8e91a-118">当装运状态为 **已分波次** 或更高时，不会发生自动更新。</span><span class="sxs-lookup"><span data-stu-id="8e91a-118">When the shipment status is **Waved** or higher, no automatic update occurs.</span></span>

<span data-ttu-id="8e91a-119">自动更新也会考虑波次状态。</span><span class="sxs-lookup"><span data-stu-id="8e91a-119">Wave status is also considered for automatic updates.</span></span> <span data-ttu-id="8e91a-120">当与负荷行相关的波次的状态为 **已持有**、**正在执行**、**已发放**、**已领料**、或 **已装运** 时，如果用户尝试减少负荷行上的数量（通过销售订单行或转移单行上的数量减少），则会显示以下错误消息：“已创建了依赖预留的工作，因此无法删除这些预留。”</span><span class="sxs-lookup"><span data-stu-id="8e91a-120">When the wave that is related to the load line has a status of **Held**, **Executing**, **Released**, **Picked**, or **Shipped**, if a user tries to reduce the quantity on a load line (via a quantity decrease on the sales order line or transfer order line), the following error message is shown: "Reservations cannot be removed because there is work created which relies on the reservations."</span></span> <span data-ttu-id="8e91a-121">此外，当波次具有上述波次状态之一时，如果用户尝试通过增加销售订单行或转移单行上的数量来间接增加负荷行数量，负荷行上的数量不会自动增加。</span><span class="sxs-lookup"><span data-stu-id="8e91a-121">Additionally, when the wave has one of the previously mentioned wave statuses, if a user tries to indirectly increase the load line quantity by increasing the quantity on the sales order line or transfer order line, the quantity on the load line isn't automatically increased.</span></span> <span data-ttu-id="8e91a-122">在这种情况下，必须手动更新负荷行。</span><span class="sxs-lookup"><span data-stu-id="8e91a-122">In this case, the load line must be manually updated.</span></span>

## <a name="scenarios"></a><span data-ttu-id="8e91a-123">方案</span><span class="sxs-lookup"><span data-stu-id="8e91a-123">Scenarios</span></span>

<span data-ttu-id="8e91a-124">自动更新装运功能支持四个场景：添加新订单行、增加订单行上的数量、减少订单行上的数量以及删除订单行。</span><span class="sxs-lookup"><span data-stu-id="8e91a-124">The auto-update shipment functionality supports four scenarios: adding a new order line, increasing the quantity on an order line, decreasing the quantity on an order line, and removing an order line.</span></span>

- <span data-ttu-id="8e91a-125">**添加新订单行** – 当 **仓库** 页的 **仓库** 快速选项卡上的 **自动更新装运** 字段（**仓库管理 \> 设置 \> 仓库 \> 仓库**）设置为 **始终** 时，如果订单存在装运，并且在为销售订单创建了负荷之后新订单行已添加到销售订单或转移单中，现有负荷不会更新。</span><span class="sxs-lookup"><span data-stu-id="8e91a-125">**Add a new order line** – When the **Auto update shipment** field on the **Warehouse** FastTab of the **Warehouses** page (**Warehouse management \> Setup \> Warehouse \> Warehouses**) is set to **Always**, if a shipment exists for the order, and a new order line is added to a sales order or transfer order after a load has already been created for the sales order, the existing load isn't updated.</span></span> <span data-ttu-id="8e91a-126">将创建一个不引用现有负荷的新负荷行，并将其与现有装运关联。</span><span class="sxs-lookup"><span data-stu-id="8e91a-126">A new load line that has no reference to the existing load is created and associated with the existing shipment.</span></span> <span data-ttu-id="8e91a-127">新行将添加到负荷中并发放。</span><span class="sxs-lookup"><span data-stu-id="8e91a-127">The new line is added to the load and released.</span></span>
- <span data-ttu-id="8e91a-128">**增加订单行上的数量** – 当 **自动更新装运** 字段设置为 **始终** 时，如果订单存在装运，并且在为销售订单创建负荷后，现有销售订单行或转移单行上的数量已增加，负荷行将增加与订单行相同的数量。</span><span class="sxs-lookup"><span data-stu-id="8e91a-128">**Increase the quantity on an order line** – When the **Auto update shipment** field is set to **Always**, if a shipment exists for the order, and the quantity on an existing sales order line or transfer order line is increased after a load has already been created for the sales order, the load line is increased by the same quantity as the order line.</span></span> <span data-ttu-id="8e91a-129">如果负荷已发放，但未创建任何工作，则负荷行将增加与订单行相同的数量。</span><span class="sxs-lookup"><span data-stu-id="8e91a-129">If the load was released, but no work was created, the load line is increased by the same quantity as the order line.</span></span>
- <span data-ttu-id="8e91a-130">**减少订单行上的数量** – 当 **自动更新装运** 字段设置为 **始终** 或 **在数量减少时**，如果订单存在装运，并且现有销售订单行或转移单行上的数量在为销售订单创建了负荷之后减少，关联的负荷行上的数量将更新以匹配，除非该负荷行上的数量已经等于或小于订单行上的新数量。</span><span class="sxs-lookup"><span data-stu-id="8e91a-130">**Decrease the quantity on an order line** – When the **Auto update shipment** field is set to **Always** or **On quantity decrease**, if a shipment exists for the order, and the quantity on an existing sales order line or transfer order line is decreased after a load has already been created for the sales order, the quantity on the associated load line is updated to match, unless the quantity on that load line already equals or is less than the new quantity on the order line.</span></span> <span data-ttu-id="8e91a-131">在这种情况下，负荷行不受影响。</span><span class="sxs-lookup"><span data-stu-id="8e91a-131">In that case, the load line isn't affected.</span></span> <span data-ttu-id="8e91a-132">如果负荷已发放，但未创建任何工作，关联的负荷行上的数量将更新以匹配，除非该负荷行上的数量已经等于或小于订单行上的新数量。</span><span class="sxs-lookup"><span data-stu-id="8e91a-132">If the load was released, but no work was created, the quantity on the associated load line is updated to match, unless the quantity on the load line already equals or is less than the new quantity on the order line.</span></span> <span data-ttu-id="8e91a-133">在这种情况下，负荷行不受影响。</span><span class="sxs-lookup"><span data-stu-id="8e91a-133">In that case, the load line is affected.</span></span>
- <span data-ttu-id="8e91a-134">**删除订单行** – 当 **自动更新装运** 字段设置为 **始终** 或 **在数量减少时**，如果用户尝试删除负荷行存在的订单行，则会显示一条错误消息。</span><span class="sxs-lookup"><span data-stu-id="8e91a-134">**Remove an order line** – When the **Auto update shipment** field is set to **Always** or **On quantity decrease**, if the user tries to remove an order line that a load line exists for, an error message is shown.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="8e91a-135">示例场景</span><span class="sxs-lookup"><span data-stu-id="8e91a-135">Example scenario</span></span>

<span data-ttu-id="8e91a-136">对于此情况，必须安装演示数据，并且必须使用 **USMF** 演示数据公司。</span><span class="sxs-lookup"><span data-stu-id="8e91a-136">For this scenario, you must have demo data installed, and you must use the **USMF** demo data company.</span></span>

### <a name="turn-on-the-auto-update-shipment-functionality"></a><span data-ttu-id="8e91a-137">打开自动更新装运功能</span><span class="sxs-lookup"><span data-stu-id="8e91a-137">Turn on the auto-update shipment functionality</span></span>

<span data-ttu-id="8e91a-138">要打开自动更新装运功能，请按照以下步骤操作。</span><span class="sxs-lookup"><span data-stu-id="8e91a-138">To turn on the auto-update shipment functionality, follow these steps.</span></span>

1. <span data-ttu-id="8e91a-139">转到 **仓库管理 \> 设置 \> 仓库 \> 仓库**。</span><span class="sxs-lookup"><span data-stu-id="8e91a-139">Go to **Warehouse management \> Setup \> Warehouse \> Warehouses**.</span></span>
2. <span data-ttu-id="8e91a-140">选择仓库 **24**。</span><span class="sxs-lookup"><span data-stu-id="8e91a-140">Select warehouse **24**.</span></span>
3. <span data-ttu-id="8e91a-141">在 **仓库** 快速选项卡上的 **自动更新装运** 字段中，将值从 **在数量减少时** 更改为 **始终**。</span><span class="sxs-lookup"><span data-stu-id="8e91a-141">On the **Warehouse** FastTab, in the **Auto update shipment** field, change the value from **On quantity decrease** to **Always**.</span></span>

<span data-ttu-id="8e91a-142">将值更改为 **始终** 后，销售订单行和转移单行上数量的任何增加或减少，以及新行的任何增加，都会反映在选定仓库的装运和负荷上（假定是前面所述的更新约束）。</span><span class="sxs-lookup"><span data-stu-id="8e91a-142">After you change the value to **Always**, any increases or decreases in the quantities on sales order lines and transfer order lines, and any additions of new lines, are reflected on shipments and loads for the selected warehouse, given the previously mentioned update constraints.</span></span>

### <a name="change-the-wave-template-so-that-load-lines-arent-automatically-processed"></a><span data-ttu-id="8e91a-143">更改波次模板，以使负荷行不会自动处理</span><span class="sxs-lookup"><span data-stu-id="8e91a-143">Change the wave template so that load lines aren't automatically processed</span></span>

<span data-ttu-id="8e91a-144">要配置波次模板，使其不自动处理负荷行，请按照以下步骤操作。</span><span class="sxs-lookup"><span data-stu-id="8e91a-144">To configure the wave template so that it doesn't automatically process load lines, follow these steps.</span></span>

1. <span data-ttu-id="8e91a-145">转到 **仓库管理 \> 设置 \> 波次 \> 波次模板**。</span><span class="sxs-lookup"><span data-stu-id="8e91a-145">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
2. <span data-ttu-id="8e91a-146">选择波次模板 **24 装运默认**。</span><span class="sxs-lookup"><span data-stu-id="8e91a-146">Select wave template **24 Shipping default**.</span></span>
3. <span data-ttu-id="8e91a-147">选择 **编辑**。</span><span class="sxs-lookup"><span data-stu-id="8e91a-147">Select **Edit**.</span></span>
4. <span data-ttu-id="8e91a-148">在 **常规** 快速选项卡上，将 **自动波次创建** 选项设置为 **是**，并确保将所有其他选项设置为 **否**。</span><span class="sxs-lookup"><span data-stu-id="8e91a-148">On the **General** FastTab, set the **Automate wave creation** option to **Yes**, and make sure that all other options are set to **No**.</span></span>

<span data-ttu-id="8e91a-149">在波次创建过程中，不自动创建和发放任何工作，这一点很重要。</span><span class="sxs-lookup"><span data-stu-id="8e91a-149">It's important that no work be automatically created and released as part of the wave creation process.</span></span> <span data-ttu-id="8e91a-150">在创建与为销售订单行创建的负荷行相关的工作之后，如果更改了销售订单行上的数量，则负荷行将不再自动更新。</span><span class="sxs-lookup"><span data-stu-id="8e91a-150">After work is created that is related to the load line that was created for the sales order line, the load line is no longer automatically updated if the quantity on the sales order line is changed.</span></span>

### <a name="create-a-sales-order"></a><span data-ttu-id="8e91a-151">创建销售订单</span><span class="sxs-lookup"><span data-stu-id="8e91a-151">Create a sales order</span></span>

<span data-ttu-id="8e91a-152">要创建销售订单，请按照下面的步骤操作。</span><span class="sxs-lookup"><span data-stu-id="8e91a-152">To create a sales order, follow these steps.</span></span>

1. <span data-ttu-id="8e91a-153">转到 **销售和营销 \> 销售订单 \> 所有销售订单**。</span><span class="sxs-lookup"><span data-stu-id="8e91a-153">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
2. <span data-ttu-id="8e91a-154">选择客户 **US-003**。</span><span class="sxs-lookup"><span data-stu-id="8e91a-154">Select customer **US-003**.</span></span>
3. <span data-ttu-id="8e91a-155">为物料编号 **A0001** 创建一行。</span><span class="sxs-lookup"><span data-stu-id="8e91a-155">Create a line for item number **A0001**.</span></span>
4. <span data-ttu-id="8e91a-156">输入数量 **10**。</span><span class="sxs-lookup"><span data-stu-id="8e91a-156">Enter a quantity of **10**.</span></span> <span data-ttu-id="8e91a-157">（确保您使用的是仓库 **24**。）</span><span class="sxs-lookup"><span data-stu-id="8e91a-157">(Make sure that you're using warehouse **24**.)</span></span>
5. <span data-ttu-id="8e91a-158">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="8e91a-158">Select **Save**.</span></span>
6. <span data-ttu-id="8e91a-159">在“操作窗格”上的 **仓库** 选项卡上，在 **操作** 组中，选择 **发放到仓库**。</span><span class="sxs-lookup"><span data-stu-id="8e91a-159">On the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span> <span data-ttu-id="8e91a-160">装运和波次已创建。</span><span class="sxs-lookup"><span data-stu-id="8e91a-160">A shipment and a wave are created.</span></span>

<span data-ttu-id="8e91a-161">由于您在上一过程中更改了波次模板，因此不会创建任何负荷或工作。</span><span class="sxs-lookup"><span data-stu-id="8e91a-161">Because you changed the wave template in the previous procedure, no load or work is created.</span></span> <span data-ttu-id="8e91a-162">装运状态为 **打开**，波次状态为 **已创建**。</span><span class="sxs-lookup"><span data-stu-id="8e91a-162">The shipment status is **Open**, and the wave status is **Created**.</span></span>

### <a name="decrease-the-quantity-on-a-sales-order-line"></a><span data-ttu-id="8e91a-163">减少销售订单行上的数量</span><span class="sxs-lookup"><span data-stu-id="8e91a-163">Decrease the quantity on a sales order line</span></span>

<span data-ttu-id="8e91a-164">要减少销售订单行上的数量，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="8e91a-164">To decrease the quantity on a sales order line, follow these steps.</span></span>

1. <span data-ttu-id="8e91a-165">转到 **销售和营销 \> 销售订单 \> 所有销售订单**。</span><span class="sxs-lookup"><span data-stu-id="8e91a-165">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
2. <span data-ttu-id="8e91a-166">选择您刚刚发放到仓库的销售订单。</span><span class="sxs-lookup"><span data-stu-id="8e91a-166">Select the sales order that you just released to the warehouse.</span></span>
3. <span data-ttu-id="8e91a-167">选择销售订单行。</span><span class="sxs-lookup"><span data-stu-id="8e91a-167">Select the sales order line.</span></span> <span data-ttu-id="8e91a-168">在 **数量** 字段中，将值从 **10** 更改为 **8**。</span><span class="sxs-lookup"><span data-stu-id="8e91a-168">In the **Quantity** field, change the value from **10** to **8**.</span></span>
4. <span data-ttu-id="8e91a-169">在销售订单行中，选择 **仓库 \> 装运详细信息**。</span><span class="sxs-lookup"><span data-stu-id="8e91a-169">From the sales order line, select **Warehouse \> Shipment details**.</span></span> <span data-ttu-id="8e91a-170">在 **装运详细信息** 页面上的 **负荷行** 快速选项卡上，数量反映了销售订单行上的更改。</span><span class="sxs-lookup"><span data-stu-id="8e91a-170">On the **Shipment details** page, on the **Load lines** FastTab, the quantity reflects the change on the sales order line.</span></span>

### <a name="increase-the-quantity-on-a-sales-order-line"></a><span data-ttu-id="8e91a-171">增加销售订单行上的数量</span><span class="sxs-lookup"><span data-stu-id="8e91a-171">Increase the quantity on a sales order line</span></span>

<span data-ttu-id="8e91a-172">要增加销售订单行上的数量，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="8e91a-172">To increase the quantity on a sales order line, follow these steps.</span></span>

1. <span data-ttu-id="8e91a-173">转到 **销售和营销 \> 销售订单 \> 所有销售订单**。</span><span class="sxs-lookup"><span data-stu-id="8e91a-173">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
2. <span data-ttu-id="8e91a-174">选择您之前发放到仓库的销售订单。</span><span class="sxs-lookup"><span data-stu-id="8e91a-174">Select the sales order that you previously released to the warehouse.</span></span>
3. <span data-ttu-id="8e91a-175">将行数量从 **8** 改为 **12**。</span><span class="sxs-lookup"><span data-stu-id="8e91a-175">Change the line quantity from **8** to **12**.</span></span>
4. <span data-ttu-id="8e91a-176">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="8e91a-176">Select **Save**.</span></span>
5. <span data-ttu-id="8e91a-177">返回 **所有销售订单** 页，两次选择该销售订单。</span><span class="sxs-lookup"><span data-stu-id="8e91a-177">Go back to the **All sales orders** page, and select the sales order again.</span></span>
5. <span data-ttu-id="8e91a-178">在“操作窗格”的 **仓库** 选项卡上的 **相关信息** 组中，选择 **装运详细信息**。</span><span class="sxs-lookup"><span data-stu-id="8e91a-178">On the Action Pane, on the **Warehouse** tab, in the **Related information** group, select **Shipment details**.</span></span> <span data-ttu-id="8e91a-179">在 **装运详细信息** 页面上的 **负荷行** 快速选项卡上，数量反映了销售订单行上的更改。</span><span class="sxs-lookup"><span data-stu-id="8e91a-179">On the **Shipment details** page, on the **Load lines** FastTab, the quantity reflects the change on the sales order line.</span></span>

<span data-ttu-id="8e91a-180">尽管负荷行上的数量从 8 增加到了 12，但除非打开了自动预留功能，否则只有八个物料会预留。</span><span class="sxs-lookup"><span data-stu-id="8e91a-180">Although the quantity on the load line was increased from 8 to 12, only eight items remain reserved, unless automatic reservation is turned on.</span></span> <span data-ttu-id="8e91a-181">由于尚未预留添加到现有装运的数量，因此，如果此时在未预留的情况下处理波次，则仅为已预留的数量创建工作。</span><span class="sxs-lookup"><span data-stu-id="8e91a-181">Because the quantity that was added to the existing shipment hasn't been reserved, if the wave is processed at this point, without reservation, work is created only for the quantity that has already been reserved.</span></span>

> [!NOTE]
> <span data-ttu-id="8e91a-182">当订单行上的数量减少时，如果负荷行上的数量已经等于或小于订单行上的新数量，则此数量不会受到影响。</span><span class="sxs-lookup"><span data-stu-id="8e91a-182">When the quantity on an order line is decreased, the quantity on the load line isn't affected if it already equals or is less than the new quantity on the order line.</span></span> <span data-ttu-id="8e91a-183">当增加订单行上的数量时，负荷行将增加与订单行相同的数量。</span><span class="sxs-lookup"><span data-stu-id="8e91a-183">When the quantity on an order line is increased, the load line is increased by the same quantity as the order line.</span></span> <span data-ttu-id="8e91a-184">如果订单行上的数量与负荷行上的数量不同，差额将保持不变。</span><span class="sxs-lookup"><span data-stu-id="8e91a-184">If the quantity on the order line differs from the quantity on the load line, the difference remains.</span></span>

### <a name="add-a-sales-order-line"></a><span data-ttu-id="8e91a-185">添加销售订单行</span><span class="sxs-lookup"><span data-stu-id="8e91a-185">Add a sales order line</span></span>

<span data-ttu-id="8e91a-186">若要添加销售订单行，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="8e91a-186">To add a sales order line, follow these steps.</span></span>

1. <span data-ttu-id="8e91a-187">转到 **销售和营销 \> 销售订单 \> 所有销售订单**。</span><span class="sxs-lookup"><span data-stu-id="8e91a-187">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
2. <span data-ttu-id="8e91a-188">选择您之前发放到仓库的销售订单。</span><span class="sxs-lookup"><span data-stu-id="8e91a-188">Select the sales order that you previously released to the warehouse.</span></span>
3. <span data-ttu-id="8e91a-189">为物料编号 **A0002** 创建一行。</span><span class="sxs-lookup"><span data-stu-id="8e91a-189">Create a line for item number **A0002**.</span></span>
4. <span data-ttu-id="8e91a-190">在 **数量** 字段中，输入 **10**。</span><span class="sxs-lookup"><span data-stu-id="8e91a-190">In the **Quantity** field, enter **10**.</span></span> <span data-ttu-id="8e91a-191">（请确保您使用的是仓库 **24**。）新行将自动添加到现有装运中。</span><span class="sxs-lookup"><span data-stu-id="8e91a-191">(Make sure that you're using warehouse **24**.) The new line is automatically added to the existing shipment.</span></span>
5. <span data-ttu-id="8e91a-192">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="8e91a-192">Select **Save**.</span></span>
6. <span data-ttu-id="8e91a-193">返回 **所有销售订单** 页，两次选择该销售订单。</span><span class="sxs-lookup"><span data-stu-id="8e91a-193">Go back to the **All sales orders** page, and select the sales order again.</span></span>
7. <span data-ttu-id="8e91a-194">在“操作窗格”的 **仓库** 选项卡上的 **相关信息** 组中，选择 **装运详细信息**。</span><span class="sxs-lookup"><span data-stu-id="8e91a-194">On the Action Pane, on the **Warehouse** tab, in the **Related information** group, select **Shipment details**.</span></span> <span data-ttu-id="8e91a-195">在 **装运详细信息** 页面上的 **负荷行** 快速选项卡上，注意第二个负荷行。</span><span class="sxs-lookup"><span data-stu-id="8e91a-195">On the **Shipment details** page, on the **Load lines** FastTab, notice the second load line.</span></span>

<span data-ttu-id="8e91a-196">由于尚未预留刚刚添加到现有装运的销售订单行，因此，如果此时处理了波次，则仅为第一个销售订单行和第一个负荷行上的数量创建工作。</span><span class="sxs-lookup"><span data-stu-id="8e91a-196">Because the sales order line that you just added to the existing shipment hasn't been reserved, if the wave is processed at this point, work is created only for the quantity on the first sales order line and the first load line.</span></span>

### <a name="process-a-wave"></a><span data-ttu-id="8e91a-197">处理波次</span><span class="sxs-lookup"><span data-stu-id="8e91a-197">Process a wave</span></span>

<span data-ttu-id="8e91a-198">若要处理波次，请遵循以下步骤。</span><span class="sxs-lookup"><span data-stu-id="8e91a-198">To process the wave, follow these steps.</span></span>

1. <span data-ttu-id="8e91a-199">转到 **仓库管理 \> 出站波次 \> 装运波次 \> 所有波次**。</span><span class="sxs-lookup"><span data-stu-id="8e91a-199">Go to **Warehouse management \> Outbound waves \> Shipment waves \> All waves**.</span></span>
2. <span data-ttu-id="8e91a-200">选择您之前创建的波次。</span><span class="sxs-lookup"><span data-stu-id="8e91a-200">Select the wave that you previously created.</span></span>
3. <span data-ttu-id="8e91a-201">在“操作窗格”的 **波次** 选项卡的 **波次** 组中，选择 **处理**。</span><span class="sxs-lookup"><span data-stu-id="8e91a-201">On the Action Pane, on the **Wave** tab, in the **Wave** group, select **Process**.</span></span>

<span data-ttu-id="8e91a-202">波次将被处理，并为负荷行上的预留数量创建工作。</span><span class="sxs-lookup"><span data-stu-id="8e91a-202">The wave is processed and creates work for the reserved quantities on the load lines.</span></span> <span data-ttu-id="8e91a-203">装运状态将从 **打开** 更新为 **已分波次**。</span><span class="sxs-lookup"><span data-stu-id="8e91a-203">The shipment status is updated from **Open** to **Waved**.</span></span> <span data-ttu-id="8e91a-204">当装运状态更新为 **已分波次** 时，发生的任何更改（例如行数量减少或增加，或向销售订单添加新行）都不会影响与已分波次装运关联的现有负荷行。</span><span class="sxs-lookup"><span data-stu-id="8e91a-204">As the shipment status is updated to **Waved**, any changes that occur, such as decreases or increases in line quantities, or the addition of new lines to the sales order, don't affect the existing load lines that are associated with the waved shipment.</span></span>

<span data-ttu-id="8e91a-205">如果装运的状态为 **已分波次** 或更高，则不会在与该装运关联的负荷行上反映或根据其验证销售订单行上的数量更新。</span><span class="sxs-lookup"><span data-stu-id="8e91a-205">If a shipment has a status of **Waved** or higher, updates to the quantity on a sales order line aren't reflected on or validated against a load line that is associated with the shipment.</span></span> <span data-ttu-id="8e91a-206">必须直接在负荷行上更改负荷行上的数量。</span><span class="sxs-lookup"><span data-stu-id="8e91a-206">Changes to the quantity on a load line must be made directly on the load line.</span></span>

<span data-ttu-id="8e91a-207">验证将在为负荷行创建工作并进行预留之后进行。</span><span class="sxs-lookup"><span data-stu-id="8e91a-207">Validation is done after work has been created for the load line and a reservation has been made.</span></span> <span data-ttu-id="8e91a-208">然后，根据工作行预留验证销售订单行上数量的减少。</span><span class="sxs-lookup"><span data-stu-id="8e91a-208">A decrease in the quantity on the sales order line is then validated against the work line reservation.</span></span>
