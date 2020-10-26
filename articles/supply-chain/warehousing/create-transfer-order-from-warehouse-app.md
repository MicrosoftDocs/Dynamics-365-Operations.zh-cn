---
title: 通过仓库应用创建转移单
description: 本主题描述了如何通过仓库应用功能创建和处理转移单
author: perlynne
manager: tfehr
ms.date: 09/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSMobileDeviceQueueEvent
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-09
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: c30b0e74053480a08f84f4d7579021084ded5799
ms.sourcegitcommit: 286786445f72db20e993d37a63df0b886f8f5e99
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/12/2020
ms.locfileid: "3988365"
---
# <a name="create-transfer-orders-from-the-warehouse-app"></a><span data-ttu-id="1cacf-103">通过仓库应用创建转移单</span><span class="sxs-lookup"><span data-stu-id="1cacf-103">Create transfer orders from the warehouse app</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1cacf-104">此功能允许仓库工作人员直接从仓库应用中创建和处理转移单。</span><span class="sxs-lookup"><span data-stu-id="1cacf-104">This feature lets warehouse workers create and process transfer orders directly from the warehouse app.</span></span> <span data-ttu-id="1cacf-105">仓库工作人员首先选择目标仓库，然后他们可以使用应用扫描一个或多个牌照来将牌照添加到转移单。</span><span class="sxs-lookup"><span data-stu-id="1cacf-105">The warehouse workers start by selecting the destination warehouse and then they can scan one or more license plates using the app to add license plates to the transfer order.</span></span> <span data-ttu-id="1cacf-106">当仓库工作人员选择**完成订单**时，批处理作业将根据为这些牌照登记的现有库存创建所需的转移单和订单行。</span><span class="sxs-lookup"><span data-stu-id="1cacf-106">When the warehouse worker selects  **Complete order**, a batch job will create the required transfer order and order lines based on the on-hand inventory registered for those license plates.</span></span>

## <a name="enable-the-create-transfer-orders-from-warehouse-app-feature"></a><a name="enable-create-transfer-order-from-warehouse-app"></a><span data-ttu-id="1cacf-107">启用通过仓库应用创建转移单功能</span><span class="sxs-lookup"><span data-stu-id="1cacf-107">Enable the create transfer orders from Warehouse app feature</span></span>

<span data-ttu-id="1cacf-108">只有在系统上启用了此功能及其先决条件后才能使用它。</span><span class="sxs-lookup"><span data-stu-id="1cacf-108">Before you can use this feature, both it and its prerequisites must be enabled on your system.</span></span> <span data-ttu-id="1cacf-109">管理员可以使用[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)页面检查功能状态，并在需要时启用。</span><span class="sxs-lookup"><span data-stu-id="1cacf-109">Administrators can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) page to check the feature status and enable it if needed.</span></span>

1. <span data-ttu-id="1cacf-110">首先启用[处理仓库应用事件](warehouse-app-events.md)功能，该功能在[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)中列出为：</span><span class="sxs-lookup"><span data-stu-id="1cacf-110">First enable the [Process warehouse app events](warehouse-app-events.md) feature, which is listed in [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) as:</span></span>
    - <span data-ttu-id="1cacf-111">**模块** - 仓库管理</span><span class="sxs-lookup"><span data-stu-id="1cacf-111">**Module** - Warehouse management</span></span>
    - <span data-ttu-id="1cacf-112">**功能名称** - 处理仓库应用事件</span><span class="sxs-lookup"><span data-stu-id="1cacf-112">**Feature name** - Process warehouse app events</span></span>
1. <span data-ttu-id="1cacf-113">然后，启用*通过仓库应用创建转移单*功能，该功能列出为：</span><span class="sxs-lookup"><span data-stu-id="1cacf-113">Then enable the *Create transfer orders from the warehouse app*  feature, which is listed as:</span></span>
    - <span data-ttu-id="1cacf-114">**模块** - 仓库管理</span><span class="sxs-lookup"><span data-stu-id="1cacf-114">**Module** - Warehouse management</span></span>
    - <span data-ttu-id="1cacf-115">**功能名称** - 通过仓库应用创建和处理转移单</span><span class="sxs-lookup"><span data-stu-id="1cacf-115">**Feature name** - Create and process transfer orders from the warehouse app</span></span>
1. <span data-ttu-id="1cacf-116">若要自动化出站装运的过程，您还必须启用[从批处理作业确认出站装运](confirm-outbound-shipments-from-batch-jobs.md)功能。</span><span class="sxs-lookup"><span data-stu-id="1cacf-116">To automate the processing of the outbound shipments, you must also enable the [Confirm outbound shipments from batch jobs](confirm-outbound-shipments-from-batch-jobs.md) feature.</span></span> <span data-ttu-id="1cacf-117">此功能列出为：</span><span class="sxs-lookup"><span data-stu-id="1cacf-117">This feature is listed as:</span></span>
    - <span data-ttu-id="1cacf-118">**模块** - 仓库管理</span><span class="sxs-lookup"><span data-stu-id="1cacf-118">**Module** - Warehouse management</span></span>
    - <span data-ttu-id="1cacf-119">**功能名称** - 从批处理作业确认出站装运</span><span class="sxs-lookup"><span data-stu-id="1cacf-119">**Feature name** - Confirm outbound shipments from batch jobs</span></span>

## <a name="set-up-a-mobile-device-menu-item-to-create-transfer-orders"></a><a name="setup-warehouse-app-menu"></a><span data-ttu-id="1cacf-120">设置用于创建转移单的移动设备菜单项</span><span class="sxs-lookup"><span data-stu-id="1cacf-120">Set up a mobile device menu item to create transfer orders</span></span>

<span data-ttu-id="1cacf-121">这是设置用于创建转移单的移动设备菜单项的一般准则。</span><span class="sxs-lookup"><span data-stu-id="1cacf-121">Here are general guidelines for setting up a mobile device menu item for creating a transfer order.</span></span> <span data-ttu-id="1cacf-122">根据要在用户从车间创建转移单时设置的自动化级别的业务需求，将启用不同的配置。</span><span class="sxs-lookup"><span data-stu-id="1cacf-122">Depending on your business requirements for the level of automation to be set when users create transfer orders from the floor, different configurations will be enabled.</span></span> <span data-ttu-id="1cacf-123">本文档中的方案将描述一种这样的配置。</span><span class="sxs-lookup"><span data-stu-id="1cacf-123">The scenario in this document will describe one such configuration.</span></span>

1. <span data-ttu-id="1cacf-124">转到**仓库管理 \> 设置 \> 移动设备 \> 移动设备菜单项**。</span><span class="sxs-lookup"><span data-stu-id="1cacf-124">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="1cacf-125">选择**新建**以添加新的菜单项。</span><span class="sxs-lookup"><span data-stu-id="1cacf-125">Select **New** to add a new menu item.</span></span> <span data-ttu-id="1cacf-126">然后，进行以下设置以开始使用：</span><span class="sxs-lookup"><span data-stu-id="1cacf-126">Then make the following settings to get started:</span></span>

    - <span data-ttu-id="1cacf-127">**菜单项名称** - 分配一个名称，因为它应该显示在 Supply Chain Management 中。</span><span class="sxs-lookup"><span data-stu-id="1cacf-127">**Menu item name** - Assign a name as it should appear in Supply Chain Management.</span></span>
    - <span data-ttu-id="1cacf-128">**标题** - 分配菜单名称，因为它应该在仓库应用中显示给工作人员。</span><span class="sxs-lookup"><span data-stu-id="1cacf-128">**Title** - Assign a menu name as it should be presented to workers in the warehouse app.</span></span>
    - <span data-ttu-id="1cacf-129">**模式** - 设置为*间接*（此仓库应用不会创建工作）。</span><span class="sxs-lookup"><span data-stu-id="1cacf-129">**Mode** - Set to *Indirect* (this warehouse app will not create work).</span></span>
    - <span data-ttu-id="1cacf-130">**活动代码** - 设置*通过牌照创建转移单*，以使仓库工人能够基于一个或多个扫描的牌照创建转移单。</span><span class="sxs-lookup"><span data-stu-id="1cacf-130">**Activity code** - Set to *Create transfer order from license plates* to enable the warehouse workers to create a transfer order based on one or more scanned license plates.</span></span>

1. <span data-ttu-id="1cacf-131">使用**转移单行创建策略**设置，以控制此菜单项将如何创建转移单行。</span><span class="sxs-lookup"><span data-stu-id="1cacf-131">Use the **Transfer order line creation policy** setting to control how transfer order lines will be created by this menu item.</span></span> <span data-ttu-id="1cacf-132">将根据针对扫描的牌照登记的现有库存创建/更新这些行。</span><span class="sxs-lookup"><span data-stu-id="1cacf-132">The lines will be created/updated based on the on-hand inventory registered for the scanned license plates.</span></span> <span data-ttu-id="1cacf-133">选择以下值之一：</span><span class="sxs-lookup"><span data-stu-id="1cacf-133">Choose one of the following values:</span></span>

    - <span data-ttu-id="1cacf-134">**没有预留** - 转移单行将不会预留。</span><span class="sxs-lookup"><span data-stu-id="1cacf-134">**No reservation** - The transfer order lines will not be reserved.</span></span>
    - <span data-ttu-id="1cacf-135">**牌照引导与行预留** – 转移单行将预留，并使用牌照引导策略选项，该选项存储与订单行关联的相关牌照 ID。</span><span class="sxs-lookup"><span data-stu-id="1cacf-135">**License plate guided with line reservation** – The transfer order lines will be reserved and use the License plate guided strategy option, which stores the relevant license plate IDs associated with the order lines.</span></span> <span data-ttu-id="1cacf-136">因此，可以在转移单行的工作创建过程中使用定位的牌照 ID 值。</span><span class="sxs-lookup"><span data-stu-id="1cacf-136">Located license plate ID values can therefore be used as part of the work creation process for the transfer order lines.</span></span>

1. <span data-ttu-id="1cacf-137">使用**出站装运策略**设置以根据需要向出站转移单装运过程添加更多自动化功能。</span><span class="sxs-lookup"><span data-stu-id="1cacf-137">Use the **Outbound shipment policy** setting to add more automation to the outbound transfer order shipment process, as needed.</span></span> <span data-ttu-id="1cacf-138">当工作人员选择**完成订单**按钮时，该应用将创建*完成订单*仓库应用事件，该事件将对当前转移单中的每个行保存您在**出站装运策略**字段中选择的值。</span><span class="sxs-lookup"><span data-stu-id="1cacf-138">When a worker selects the **Complete order** button, the app creates the *Complete order* warehouse app event, which will save the value you choose here in the **Outbound shipment policy** field for each line in the current transfer order.</span></span> <span data-ttu-id="1cacf-139">稍后，当批处理作业处理事件队列以创建转移单时，批处理作业可以读取此字段中存储的值，从而可以控制该作业如何处理每一行。</span><span class="sxs-lookup"><span data-stu-id="1cacf-139">Later, when the event queue is processed by a batch job to create the transfer order, the value stored in this field can be read by the batch job, and may therefore control how that job processes each line.</span></span> <span data-ttu-id="1cacf-140">选择以下各项之一：</span><span class="sxs-lookup"><span data-stu-id="1cacf-140">Choose one of the following:</span></span>

    - <span data-ttu-id="1cacf-141">**无** - 没有自动处理。</span><span class="sxs-lookup"><span data-stu-id="1cacf-141">**None** - No automated processing is done.</span></span>
    - <span data-ttu-id="1cacf-142">**发放到仓库** - 自动化发放到仓库的过程。</span><span class="sxs-lookup"><span data-stu-id="1cacf-142">**Release to warehouse** - Automates the release to warehouse process.</span></span>
    - <span data-ttu-id="1cacf-143">**装运确认** - 自动化装运确认的过程。</span><span class="sxs-lookup"><span data-stu-id="1cacf-143">**Ship confirm** - Automates the ship confirmation process.</span></span>
    - <span data-ttu-id="1cacf-144">**发放和装运确认** - 自动化发放到仓库和装运确认的过程。</span><span class="sxs-lookup"><span data-stu-id="1cacf-144">**Release and ship confirm** - Automates both the release to warehouse and ship confirmation processes.</span></span>

## <a name="add-the-mobile-device-menu-item-to-a-menu"></a><span data-ttu-id="1cacf-145">将移动设备菜单项添加到一个菜单</span><span class="sxs-lookup"><span data-stu-id="1cacf-145">Add the mobile device menu item to a menu</span></span>

1. <span data-ttu-id="1cacf-146">转到**仓库管理 \> 设置 \> 移动设备 \> 移动设备菜单**</span><span class="sxs-lookup"><span data-stu-id="1cacf-146">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**</span></span>
1. <span data-ttu-id="1cacf-147">选择**编辑**。</span><span class="sxs-lookup"><span data-stu-id="1cacf-147">Select **Edit**.</span></span>
1. <span data-ttu-id="1cacf-148">选择现有菜单，然后在**可用菜单和菜单项**下选择新菜单项。</span><span class="sxs-lookup"><span data-stu-id="1cacf-148">Select an existing menu following selection of the new menu item under **Available menus and menu items**.</span></span> <span data-ttu-id="1cacf-149">通过选择向右键按钮添加菜单项。</span><span class="sxs-lookup"><span data-stu-id="1cacf-149">Add the menu item by selecting the right-arrow button.</span></span>

## <a name="create-a-transfer-order-based-on-license-plates"></a><span data-ttu-id="1cacf-150">根据牌照创建转移单</span><span class="sxs-lookup"><span data-stu-id="1cacf-150">Create a transfer order based on license plates</span></span>

<span data-ttu-id="1cacf-151">仓库应用具有根据牌照创建转移单的简单过程。</span><span class="sxs-lookup"><span data-stu-id="1cacf-151">The warehouse app has a simple process for creating transfer orders based on license plates.</span></span> <span data-ttu-id="1cacf-152">为此，工作人员将使用仓库应用执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="1cacf-152">To do this, the worker does the following using the warehouse app:</span></span>

1. <span data-ttu-id="1cacf-153">创建转移单并确定目标仓库。</span><span class="sxs-lookup"><span data-stu-id="1cacf-153">Create the transfer order and identify the destination warehouse.</span></span>
1. <span data-ttu-id="1cacf-154">确定要装运的每个牌照。</span><span class="sxs-lookup"><span data-stu-id="1cacf-154">Identify each license plate to be shipped.</span></span>
1. <span data-ttu-id="1cacf-155">选择**完成订单**。</span><span class="sxs-lookup"><span data-stu-id="1cacf-155">Select **Complete order**.</span></span>

>[!NOTE]
> <span data-ttu-id="1cacf-156">多个工作人员可以通过使用**选择转移单**按钮从仓库应用事件队列中选择未处理的现有转移单号，为同一转移单分配牌照。</span><span class="sxs-lookup"><span data-stu-id="1cacf-156">It is possible for multiple workers to assign license plates intended for the same transfer order by using the **Select transfer order** button to select an existing, unprocessed, transfer order number from the warehouse app event queue.</span></span> <span data-ttu-id="1cacf-157">有关如何查找转移单号的值的信息，请参见[查询仓库应用事件](#inquire-the-warehouse-app-events)。</span><span class="sxs-lookup"><span data-stu-id="1cacf-157">For information about how to find the transfer order number values, see [Inquire the warehouse app events](#inquire-the-warehouse-app-events).</span></span>

## <a name="example-scenario"></a><span data-ttu-id="1cacf-158">示例场景</span><span class="sxs-lookup"><span data-stu-id="1cacf-158">Example scenario</span></span>

<span data-ttu-id="1cacf-159">此方案概述了获取根据已登记所选牌照的现有库存创建和自动处理的转移单的过程。</span><span class="sxs-lookup"><span data-stu-id="1cacf-159">This scenario provides an overview of the process for getting transfer orders created and automatically processed based on the on-hand inventory registered on the selected license plates.</span></span>

<span data-ttu-id="1cacf-160">若要使用建议的值完成此方案，必须在安装了演示数据的系统上工作，然后选择 *USMF* 法人，然后再开始。</span><span class="sxs-lookup"><span data-stu-id="1cacf-160">To work through this scenario using the values suggested, you must work on a system with demo data installed and select the *USMF* legal entity before you begin.</span></span>

<span data-ttu-id="1cacf-161">此方案假设您已经启用了[通过仓库应用创建和处理转移单功能](#enable-create-transfer-order-from-warehouse-app)和[仓库应用事件处理](warehouse-app-events.md)功能。</span><span class="sxs-lookup"><span data-stu-id="1cacf-161">This scenario assumes that you have already enabled both the [Create and process transfer orders from the warehouse app feature](#enable-create-transfer-order-from-warehouse-app), and the [warehouse app event processing](warehouse-app-events.md) capability.</span></span>

<span data-ttu-id="1cacf-162">除了在移动设备菜单项中设置创建转移单外，还必须设置并启用其他模板、位置指令和批处理作业。</span><span class="sxs-lookup"><span data-stu-id="1cacf-162">In addition to setting up the create transfer order in the mobile device menu items, additional templates, location directives, and batch jobs must also be set up and enabled.</span></span>

### <a name="example-scenario-blueprint"></a><span data-ttu-id="1cacf-163">示例方案蓝图</span><span class="sxs-lookup"><span data-stu-id="1cacf-163">Example Scenario blueprint</span></span>

<span data-ttu-id="1cacf-164">您是零售商，拥有多个牌照，每个牌照包含物料组合，这些物料放在您的一个仓库（*仓库 51*）中的特定位置。</span><span class="sxs-lookup"><span data-stu-id="1cacf-164">You are a retailer and have multiple license plates, each containing a mix of items placed at a specific location within one of your warehouses (*Warehouse 51*).</span></span> <span data-ttu-id="1cacf-165">您想要启用允许工作人员创建到另一个仓库（*仓库 61*）的转移单以收集扫描的牌照的过程。</span><span class="sxs-lookup"><span data-stu-id="1cacf-165">You would like to enable the process that allows workers to create a transfer order to another warehouse (*Warehouse 61*) for a collection of scanned license plates.</span></span> <span data-ttu-id="1cacf-166">一旦确定了该订单的最后一个牌照，您将自动装运/更新转移单。</span><span class="sxs-lookup"><span data-stu-id="1cacf-166">You will automatically ship-update the transfer order as soon as the last license plate for the order has been identified.</span></span>

<span data-ttu-id="1cacf-167">![自动化转移单过程示例](media/create-transfer-order-from-app-example.png "自动化转移单过程示例")</span><span class="sxs-lookup"><span data-stu-id="1cacf-167">![Automated transfer order process example](media/create-transfer-order-from-app-example.png "Automated transfer order process example")</span></span>

### <a name="create-a-mobile-device-menu-item-for-creating-transfer-orders"></a><span data-ttu-id="1cacf-168">创建用于创建转移单的移动设备菜单项</span><span class="sxs-lookup"><span data-stu-id="1cacf-168">Create a mobile device menu item for creating transfer orders</span></span>

<span data-ttu-id="1cacf-169">此部分说明了如何创建用于创建转移单的新移动设备菜单项。</span><span class="sxs-lookup"><span data-stu-id="1cacf-169">This section explains how to create a new mobile device menu item for creating transfer orders.</span></span> <span data-ttu-id="1cacf-170">将**模式**设置为*间接*，并将**活动代码**设置为*通过牌照创建转移单*。</span><span class="sxs-lookup"><span data-stu-id="1cacf-170">Set the **Mode** to *Indirect* and the **Activity code** to *Create transfer order from license plates*.</span></span>

1. <span data-ttu-id="1cacf-171">转到**仓库管理 \> 设置 \> 移动设备 \> 移动设备菜单项**。</span><span class="sxs-lookup"><span data-stu-id="1cacf-171">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="1cacf-172">选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="1cacf-172">Select **New**.</span></span>
1. <span data-ttu-id="1cacf-173">在**菜单项名称**字段中，输入名称*创建到*。</span><span class="sxs-lookup"><span data-stu-id="1cacf-173">In the **Menu item name** field, enter the name *Create TO*.</span></span>
1. <span data-ttu-id="1cacf-174">在**标题**字段中，输入说明*创建到*。</span><span class="sxs-lookup"><span data-stu-id="1cacf-174">In the **Title** field, enter the description *Create TO*.</span></span>
1. <span data-ttu-id="1cacf-175">在**模式**字段中，选择*间接*。</span><span class="sxs-lookup"><span data-stu-id="1cacf-175">In the **Mode** field, select *Indirect*.</span></span>
1. <span data-ttu-id="1cacf-176">在**活动代码**中，选择*通过牌照创建转移单*</span><span class="sxs-lookup"><span data-stu-id="1cacf-176">In the **Activity code**, select *Create transfer order from license plates*</span></span>
1. <span data-ttu-id="1cacf-177">在**订单行创建策略**中，选择*牌照引导与行预留*。</span><span class="sxs-lookup"><span data-stu-id="1cacf-177">In the **Order line creation policy**, select *License plate guided with line reservation*.</span></span>
1. <span data-ttu-id="1cacf-178">在**出站装运策略**中，选择*发放和装运确认*。</span><span class="sxs-lookup"><span data-stu-id="1cacf-178">In the **Outbound shipment policy**, select *Release and ship confirm*.</span></span>
1. <span data-ttu-id="1cacf-179">转到**仓库管理 \> 设置 \> 移动设备 \> 移动设备菜单**。</span><span class="sxs-lookup"><span data-stu-id="1cacf-179">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span>
1. <span data-ttu-id="1cacf-180">选择**编辑**。</span><span class="sxs-lookup"><span data-stu-id="1cacf-180">Select **Edit**.</span></span>
1. <span data-ttu-id="1cacf-181">选择现有**库存**菜单，然后在**可用菜单和菜单项**下选择新菜单项。</span><span class="sxs-lookup"><span data-stu-id="1cacf-181">Select the existing **Inventory** menu and then select the new menu item under **Available menus and menu items**.</span></span> <span data-ttu-id="1cacf-182">通过选择向右键按钮将菜单项添加到**库存**菜单。</span><span class="sxs-lookup"><span data-stu-id="1cacf-182">Add the menu item into to **Inventory** menu by selecting the right-arrow button.</span></span>

### <a name="set-up-work-templates-to-auto-process-and-break-work-by-located-license-plate"></a><span data-ttu-id="1cacf-183">设置工作模板以按定位的牌照自动处理和分解工作</span><span class="sxs-lookup"><span data-stu-id="1cacf-183">Set up work templates to auto process and break work by located license plate</span></span>

<span data-ttu-id="1cacf-184">此部分说明了如何在发放波次时使工作模板自动处理由模板创建的工作。</span><span class="sxs-lookup"><span data-stu-id="1cacf-184">This section explains how to enable a work template to automatically process the work created by the template when a wave is released.</span></span>

1. <span data-ttu-id="1cacf-185">转到**仓库管理 \> 设置 \> 工作 \> 工作模板**。</span><span class="sxs-lookup"><span data-stu-id="1cacf-185">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="1cacf-186">在**工作订单类型**字段中，选择*转移发放*。</span><span class="sxs-lookup"><span data-stu-id="1cacf-186">In the **Work order type** field, select *Transfer issue*.</span></span>
1. <span data-ttu-id="1cacf-187">选择**新建**创建新的工作模板。</span><span class="sxs-lookup"><span data-stu-id="1cacf-187">Select **New** to create a new work template.</span></span>
1. <span data-ttu-id="1cacf-188">在**工作模板**字段中，输入 *51 自动处理 LP*。</span><span class="sxs-lookup"><span data-stu-id="1cacf-188">In the **Work template** field, enter *51 Auto process LP*.</span></span>
1. <span data-ttu-id="1cacf-189">在**工作模板说明**字段中，输入 *51 自动处理 LP*。</span><span class="sxs-lookup"><span data-stu-id="1cacf-189">In the **Work template description** field, enter *51 Auto process LP*.</span></span>
1. <span data-ttu-id="1cacf-190">选择**自动处理**复选框。</span><span class="sxs-lookup"><span data-stu-id="1cacf-190">Select the **Automatically process** check box.</span></span> <span data-ttu-id="1cacf-191">必须选择此项才能处理任何自动化步骤。</span><span class="sxs-lookup"><span data-stu-id="1cacf-191">This must be selected in order for any automation steps to be processed.</span></span>
1. <span data-ttu-id="1cacf-192">在演示数据中，已经存在一个工作模板 *51 转移*，编辑**序列号**字段，以便新工作模板的序列号比现有工作模板 *51 转移*的序列号低。</span><span class="sxs-lookup"><span data-stu-id="1cacf-192">In the demo data, there already exists a work template *51 Transfer*, edit the **Sequence number** field so that the new work template has a lower sequence number than the existing work template *51 Transfer*.</span></span>
1. <span data-ttu-id="1cacf-193">在工具栏中选择**保存**以启用**工作模板详细信息**快速选项卡。</span><span class="sxs-lookup"><span data-stu-id="1cacf-193">Select **Save** in the toolbar to enable the **Work Template Details** FastTab.</span></span>
1. <span data-ttu-id="1cacf-194">在**工作模板详细信息**快速选项卡中，在工具栏中选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="1cacf-194">In the **Work Template Details** FastTab, select **New** in the toolbar.</span></span> <span data-ttu-id="1cacf-195">您将添加两行。</span><span class="sxs-lookup"><span data-stu-id="1cacf-195">You will add two lines.</span></span>
1. <span data-ttu-id="1cacf-196">在**工作类型**字段中，选择*领料*。</span><span class="sxs-lookup"><span data-stu-id="1cacf-196">In the **Work type** field, select *Pick*.</span></span>
1. <span data-ttu-id="1cacf-197">在**工作类 ID** 字段中，选择 *TransfOut*。</span><span class="sxs-lookup"><span data-stu-id="1cacf-197">In the **Work class ID** field, select *TransfOut*.</span></span>
1. <span data-ttu-id="1cacf-198">在**工作模板详细信息**工具栏中选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="1cacf-198">Select **New** in the **Work Template Details** toolbar.</span></span>
1. <span data-ttu-id="1cacf-199">在**工作类型**字段中，选择*放置*。</span><span class="sxs-lookup"><span data-stu-id="1cacf-199">In the **Work type** field, select *Put*.</span></span>
1. <span data-ttu-id="1cacf-200">在**工作类 ID** 字段中，选择 *TransfOut*。</span><span class="sxs-lookup"><span data-stu-id="1cacf-200">In the **Work class ID** field, select *TransfOut*.</span></span>
1. <span data-ttu-id="1cacf-201">选择**保存**以启用**指令代码**字段。</span><span class="sxs-lookup"><span data-stu-id="1cacf-201">Select **Save** to enable the **Directive code** field.</span></span>
1. <span data-ttu-id="1cacf-202">在**工作类型**和*放置*行上，依次选择**指令代码**和*货架门*。</span><span class="sxs-lookup"><span data-stu-id="1cacf-202">On the **Work type** *Put* line, select **Directive code** *Baydoor*.</span></span> <span data-ttu-id="1cacf-203">确保此新的工作模板获取最低的**序列号**。</span><span class="sxs-lookup"><span data-stu-id="1cacf-203">Make sure this new work template gets the lowest **Sequence number**.</span></span>
1. <span data-ttu-id="1cacf-204">在工具栏中，选择**编辑查询**以打开查询编辑器。</span><span class="sxs-lookup"><span data-stu-id="1cacf-204">In the toolbar, select **Edit query** to open the query editor.</span></span>
1. <span data-ttu-id="1cacf-205">在**范围**选项卡中，选择**添加**。</span><span class="sxs-lookup"><span data-stu-id="1cacf-205">In the **Range** tab, select **Add**.</span></span>
1. <span data-ttu-id="1cacf-206">在添加的行上，在**字段**中选择*仓库*。</span><span class="sxs-lookup"><span data-stu-id="1cacf-206">On the line added, in **Field** select *Warehouse*.</span></span>
1. <span data-ttu-id="1cacf-207">在**条件**字段中，选择 *51*。</span><span class="sxs-lookup"><span data-stu-id="1cacf-207">In the **Criteria** field, select *51*.</span></span>
1. <span data-ttu-id="1cacf-208">选择**排序**选项卡。</span><span class="sxs-lookup"><span data-stu-id="1cacf-208">Select the **Sorting** tab.</span></span>
1. <span data-ttu-id="1cacf-209">选择**添加**，并将**字段**设置为*定位的牌照 ID*。</span><span class="sxs-lookup"><span data-stu-id="1cacf-209">Select **Add** and set **Field** to *Located license plate ID*.</span></span> <span data-ttu-id="1cacf-210">选择此字段将启用工具栏按钮**工作标题分解**。</span><span class="sxs-lookup"><span data-stu-id="1cacf-210">Selecting this field will enable the toolbar button **Work header breaks**.</span></span>
1. <span data-ttu-id="1cacf-211">依次选择**确定**和**是**以重置分组，然后返回到**工作模板**页面。</span><span class="sxs-lookup"><span data-stu-id="1cacf-211">Select **OK** followed by **Yes** to reset the grouping and return to the **Work templates** page.</span></span>
1. <span data-ttu-id="1cacf-212">选择**工作标题分解**并为**定位的牌照 ID** 启用**按此字段分组**，然后关闭。</span><span class="sxs-lookup"><span data-stu-id="1cacf-212">Select **Work header breaks** and enable the **Group by this field** for the **Located license plate ID** and close.</span></span>

> [!NOTE]
> <span data-ttu-id="1cacf-213">并非所有设置都可以自动处理，例如，实际称重物料和使用混合的跟踪维度。</span><span class="sxs-lookup"><span data-stu-id="1cacf-213">Not all setup can be auto processed, for example, catch weight items and the use of mixed tracking dimensions.</span></span>

### <a name="set-up-location-directives-for-the-license-plate-guided-strategy"></a><span data-ttu-id="1cacf-214">为牌照引导策略设置位置指令</span><span class="sxs-lookup"><span data-stu-id="1cacf-214">Set up location directives for the license plate guided strategy</span></span>

<span data-ttu-id="1cacf-215">此部分说明了如何设置位置指令领料过程以使用**牌照引导**策略。</span><span class="sxs-lookup"><span data-stu-id="1cacf-215">This section explains how to set up a location directive pick process to use the **License plate guided** strategy.</span></span>

1. <span data-ttu-id="1cacf-216">转到**库存管理 \> 设置 \> 位置指令**。</span><span class="sxs-lookup"><span data-stu-id="1cacf-216">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="1cacf-217">选择**编辑**。</span><span class="sxs-lookup"><span data-stu-id="1cacf-217">Select **Edit**.</span></span>
1. <span data-ttu-id="1cacf-218">在导航列表标题中，依次选择**工作订单类型**和*转移发放*。</span><span class="sxs-lookup"><span data-stu-id="1cacf-218">In the navigation list header, select the **Work order type** *Transfer issue*.</span></span>
1. <span data-ttu-id="1cacf-219">在导航列表中，选择现有的位置指令 **51 领料**。</span><span class="sxs-lookup"><span data-stu-id="1cacf-219">In the navigation list, select the existing location directive **51 TO Pick**.</span></span>
1. <span data-ttu-id="1cacf-220">在**行**快速选项卡中，选择**允许拆分**复选框。</span><span class="sxs-lookup"><span data-stu-id="1cacf-220">In the **Lines** FastTab, select the **Allow split** checkbox.</span></span>
1. <span data-ttu-id="1cacf-221">在**位置指令操作**快速选项卡中，选择**新建**以添加新操作行。</span><span class="sxs-lookup"><span data-stu-id="1cacf-221">In the **Location Directive Actions** FastTab select **New** to add a new action line.</span></span>
1. <span data-ttu-id="1cacf-222">在**名称**字段中，输入*LP 引导*。</span><span class="sxs-lookup"><span data-stu-id="1cacf-222">In the **Name** field, enter *LP Guided*.</span></span>
1. <span data-ttu-id="1cacf-223">在**战略**字段中，选择*牌照引导*。</span><span class="sxs-lookup"><span data-stu-id="1cacf-223">In the **Strategy** field, select *License plate guided*.</span></span> <span data-ttu-id="1cacf-224">此操作需要最低的序列号。</span><span class="sxs-lookup"><span data-stu-id="1cacf-224">This action needs the lowest sequence number.</span></span>
1. <span data-ttu-id="1cacf-225">在工具栏中选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="1cacf-225">Select **Save** in the toolbar.</span></span>
1. <span data-ttu-id="1cacf-226">从工具栏中选择**刷新**页面图标。</span><span class="sxs-lookup"><span data-stu-id="1cacf-226">Select  the **Refresh** page icon from the toolbar.</span></span>
1. <span data-ttu-id="1cacf-227">在**位置指令操作**快速选项卡中，选择行*领料*。</span><span class="sxs-lookup"><span data-stu-id="1cacf-227">In the **Location Directive Actions** FastTab, select the line *TOPick*.</span></span>
1. <span data-ttu-id="1cacf-228">在**位置指令操作**工具栏中，选择**下移**以将序列号更改为大于刚创建的 *LP 引导*操作的序列号。</span><span class="sxs-lookup"><span data-stu-id="1cacf-228">In the **Location Directive Actions** toolbar, select **Move down** to change the sequence number to be greater than the sequence number for the *LP Guided* action just created.</span></span>

> [!NOTE]
> <span data-ttu-id="1cacf-229">牌照引导策略将尝试在具有与转移单行关联的所请求牌照的位置上预留和创建领料工作。</span><span class="sxs-lookup"><span data-stu-id="1cacf-229">The License plate guided strategy will try to reserve and create picking work against the locations holding the requested license plates that have been associated with the transfer order lines.</span></span> <span data-ttu-id="1cacf-230">但是，如果这不可行，并且您仍想创建领料工作，则应回退到另一种位置指令操作策略，可能还要根据业务流程的需要在仓库的另一个区域中搜索库存。</span><span class="sxs-lookup"><span data-stu-id="1cacf-230">But if this isn't possible and you still would like to create picking work, you should fall back to another location directive action strategy, and perhaps also search for inventory in another area of the warehouse, depending on your business process needs.</span></span>

### <a name="set-up-a-batch-job-to-process-warehouse-app-events"></a><span data-ttu-id="1cacf-231">设置批处理作业以处理仓库应用事件</span><span class="sxs-lookup"><span data-stu-id="1cacf-231">Set up a batch job to process warehouse app events</span></span>

<span data-ttu-id="1cacf-232">此部分说明了如何设置计划的批处理作业以处理仓库应用事件。</span><span class="sxs-lookup"><span data-stu-id="1cacf-232">This section explains how to set up a scheduled batch job to process warehouse app events.</span></span>

1. <span data-ttu-id="1cacf-233">转到**仓库管理 \> 定期任务 \> 处理仓库应用事件**。</span><span class="sxs-lookup"><span data-stu-id="1cacf-233">Go to **Warehouse management \> Periodic tasks \> Process warehouse app events**.</span></span>
2. <span data-ttu-id="1cacf-234">在对话框中，启用**在后台运行**部分下的**批处理**。</span><span class="sxs-lookup"><span data-stu-id="1cacf-234">In the dialog box, enable **Batch processing** under the **Run in background** section.</span></span>
3. <span data-ttu-id="1cacf-235">选择**定期**并根据您的业务所需的时间间隔设置要处理的批处理作业。</span><span class="sxs-lookup"><span data-stu-id="1cacf-235">Select **Recurrence** and set up the batch job to process based on the interval needed for your business.</span></span>
4. <span data-ttu-id="1cacf-236">选择**确定**以返回到主对话框。</span><span class="sxs-lookup"><span data-stu-id="1cacf-236">Select **OK** to return to the main dialog.</span></span>
5. <span data-ttu-id="1cacf-237">在主对话框中选择**确定**以将作业添加到批处理队列。</span><span class="sxs-lookup"><span data-stu-id="1cacf-237">Select **OK** in the main dialog to add the job to the batch queue.</span></span>

### <a name="set-up-a-batch-job-to-release-transfer-orders-automatically"></a><span data-ttu-id="1cacf-238">设置批处理作业以自动发放转移单</span><span class="sxs-lookup"><span data-stu-id="1cacf-238">Set up a batch job to release transfer orders automatically</span></span>

<span data-ttu-id="1cacf-239">此部分说明了如何设置计划的批处理作业以发放已标记为“准备发放”的转移单。</span><span class="sxs-lookup"><span data-stu-id="1cacf-239">This section explains how to set up a scheduled batch job to release the transfer orders that have been marked as "ready to release".</span></span>

1. <span data-ttu-id="1cacf-240">转到**仓库管理 \> 发放到仓库 \> 自动发放转移单**。</span><span class="sxs-lookup"><span data-stu-id="1cacf-240">Go to **Warehouse management \> Release to warehouse \> Automatic release of transfer orders**.</span></span>
1. <span data-ttu-id="1cacf-241">在对话框中，展开**要包括的记录**部分。</span><span class="sxs-lookup"><span data-stu-id="1cacf-241">In the dialog box, expand the **Records to include** section.</span></span>
1. <span data-ttu-id="1cacf-242">在**要包括的记录**部分下，选择**筛选器**。</span><span class="sxs-lookup"><span data-stu-id="1cacf-242">Select **Filter** under the **Records to include** section.</span></span>
1. <span data-ttu-id="1cacf-243">在 **WHSTransferAutoRTWQuery** 查询页面中，在**范围**选项卡中，选择**添加**以向查询添加一个新行。</span><span class="sxs-lookup"><span data-stu-id="1cacf-243">In the **WHSTransferAutoRTWQuery** query page, **Range** tab, select **Add** to add a new line to the query.</span></span>
1. <span data-ttu-id="1cacf-244">在新行**表**字段中，选择下拉菜单并选择表**转移行发放到仓库**。</span><span class="sxs-lookup"><span data-stu-id="1cacf-244">In the new line **Table** field, select the drop-down menu and select the table **Transfer line release to warehouse**.</span></span>
1. <span data-ttu-id="1cacf-245">在**字段**下拉菜单中，选择**出站装运策略**。</span><span class="sxs-lookup"><span data-stu-id="1cacf-245">In the **Field** drop-down menu, select **Outbound shipment policy**.</span></span>
1. <span data-ttu-id="1cacf-246">在**条件**字段中，选择**发放和装运确认**。</span><span class="sxs-lookup"><span data-stu-id="1cacf-246">In the **Criteria** field, select **Release and ship confirm**.</span></span>
1. <span data-ttu-id="1cacf-247">在**字段**设置为*从仓库*的行中，在**条件**字段中，选择 *51*。</span><span class="sxs-lookup"><span data-stu-id="1cacf-247">In the line where **Field** is set to *From warehouse*, in the **Criteria** field, select *51*.</span></span>
1. <span data-ttu-id="1cacf-248">选择**确定**以返回到主对话框。</span><span class="sxs-lookup"><span data-stu-id="1cacf-248">Select **OK** to return to the main dialog box.</span></span>
1. <span data-ttu-id="1cacf-249">展开**在后台运行**部分以设置批处理。</span><span class="sxs-lookup"><span data-stu-id="1cacf-249">Expand the **Run in the background** section to set up batch processing.</span></span>
1. <span data-ttu-id="1cacf-250">启用**在后台运行**部分下的**批处理**。</span><span class="sxs-lookup"><span data-stu-id="1cacf-250">Enable **Batch processing** under the **Run in background** section.</span></span>
1. <span data-ttu-id="1cacf-251">选择**定期**并根据您的业务所需的时间间隔设置要处理的批处理作业。</span><span class="sxs-lookup"><span data-stu-id="1cacf-251">Select **Recurrence** and set up the batch job to process based on interval needed for your business.</span></span>
1. <span data-ttu-id="1cacf-252">选择**确定**以返回到主对话框。</span><span class="sxs-lookup"><span data-stu-id="1cacf-252">Select **OK** to return to the main dialog.</span></span>
1. <span data-ttu-id="1cacf-253">在主对话框中选择**确定**以将批处理作业添加到批处理队列。</span><span class="sxs-lookup"><span data-stu-id="1cacf-253">Select **OK** in the main dialog to have the batch job added to the batch queue.</span></span>

### <a name="set-up-the-process-outbound-shipment-batch-job"></a><span data-ttu-id="1cacf-254">设置“处理出站装运”批处理作业</span><span class="sxs-lookup"><span data-stu-id="1cacf-254">Set up the "Process outbound shipment" batch job</span></span>

<span data-ttu-id="1cacf-255">此部分说明了如何设置计划的批处理作业，以为与“准备装运”的转移单相关的准备装运的负载运行出站装运确认。</span><span class="sxs-lookup"><span data-stu-id="1cacf-255">This section explains how to set up a scheduled batch job to run the outbound shipment confirmation for loads ready to ship related to transfer order lines that are "ready to ship".</span></span>

1. <span data-ttu-id="1cacf-256">转到**仓库管理 \> 定期任务 \> 处理出站装运**。</span><span class="sxs-lookup"><span data-stu-id="1cacf-256">Go to **Warehouse management \> Periodic tasks \> Process outbound shipments**.</span></span>
1. <span data-ttu-id="1cacf-257">扩展**要包括的记录**部分。</span><span class="sxs-lookup"><span data-stu-id="1cacf-257">Expand the **Records to include** section.</span></span>
1. <span data-ttu-id="1cacf-258">选择**筛选器**。</span><span class="sxs-lookup"><span data-stu-id="1cacf-258">Select **Filter**.</span></span>
1. <span data-ttu-id="1cacf-259">在 **WHSLoadShipConfirm** 查询中，选择**联接**选项卡。</span><span class="sxs-lookup"><span data-stu-id="1cacf-259">In the **WHSLoadShipConfirm** query, select the **Joins** tab.</span></span>
1. <span data-ttu-id="1cacf-260">展开表层次结构，以便已展开**负载**和**负载详细信息**。</span><span class="sxs-lookup"><span data-stu-id="1cacf-260">Expand the table hierarchy so that **Loads** and **Load details** have been expanded.</span></span>
1. <span data-ttu-id="1cacf-261">选择**负载详细信息**表。</span><span class="sxs-lookup"><span data-stu-id="1cacf-261">Select the **Load details** table.</span></span>
1. <span data-ttu-id="1cacf-262">选择**添加表联接**按钮。</span><span class="sxs-lookup"><span data-stu-id="1cacf-262">Select the **Add table join** button.</span></span>
1. <span data-ttu-id="1cacf-263">在表关系的列表中，筛选或搜索*转移单行（引用）* 的**关系**列。</span><span class="sxs-lookup"><span data-stu-id="1cacf-263">In the list of table relations, filter or search on the **Relation** column for *Transfer order lines (Reference)*.</span></span>
1. <span data-ttu-id="1cacf-264">关注列表中的表关系，然后按**选择**按钮。</span><span class="sxs-lookup"><span data-stu-id="1cacf-264">Focus on the table relation in the list then press the **Select** button.</span></span>
1. <span data-ttu-id="1cacf-265">选择**转移单行**表。</span><span class="sxs-lookup"><span data-stu-id="1cacf-265">Select the **Transfer order lines** table.</span></span>
1. <span data-ttu-id="1cacf-266">选择**添加表联接**按钮。</span><span class="sxs-lookup"><span data-stu-id="1cacf-266">Select the **Add table join** button.</span></span>
1. <span data-ttu-id="1cacf-267">在表关系的列表中，筛选或搜索*库存转移附加字段（记录 ID）* 的**关系**列。</span><span class="sxs-lookup"><span data-stu-id="1cacf-267">In the list of table relations, filter or search on the **Relation** column for *Invent Transfer Additional Fields (Record-ID)*.</span></span>
1. <span data-ttu-id="1cacf-268">关注列表中的表关系，然后按**选择**按钮。</span><span class="sxs-lookup"><span data-stu-id="1cacf-268">Focus on the table relation in the list then press the **Select** button.</span></span>
1. <span data-ttu-id="1cacf-269">选择**范围**选项卡。</span><span class="sxs-lookup"><span data-stu-id="1cacf-269">Select the **Range** tab.</span></span>
1. <span data-ttu-id="1cacf-270">在**范围**查询表中，您将设置三个查询条件范围。</span><span class="sxs-lookup"><span data-stu-id="1cacf-270">In the **Range** query tables, you will set up three query criteria ranges.</span></span> <span data-ttu-id="1cacf-271">选择**添加**按钮添加一行。</span><span class="sxs-lookup"><span data-stu-id="1cacf-271">Select the **Add** button to add a line.</span></span>
1. <span data-ttu-id="1cacf-272">为表**负载**添加范围。</span><span class="sxs-lookup"><span data-stu-id="1cacf-272">Add a range for the table **Loads**.</span></span> <span data-ttu-id="1cacf-273">将**字段**设置为*负载状态*并将**条件**设置为*已负载*。</span><span class="sxs-lookup"><span data-stu-id="1cacf-273">Set **Field** to *Load status* and set **Criteria** to *Loaded*.</span></span>
1. <span data-ttu-id="1cacf-274">为表**库存转移附加字段**添加另一个范围。</span><span class="sxs-lookup"><span data-stu-id="1cacf-274">Add another range for the table **Invent Transfer Additional Fields**.</span></span> <span data-ttu-id="1cacf-275">将**字段**设置为*出站装运策略*并将**条件**设置为*发放和装运确认*。</span><span class="sxs-lookup"><span data-stu-id="1cacf-275">Set **Field** to *Outbound shipment policy* and set **Criteria** to *Release and ship confirm*.</span></span>
1. <span data-ttu-id="1cacf-276">为表**负载详细信息**添加另一个范围。</span><span class="sxs-lookup"><span data-stu-id="1cacf-276">Add another range for the table **Load details**.</span></span> <span data-ttu-id="1cacf-277">将**字段**设置为*引用*并将**条件**设置为*转移单装运*。</span><span class="sxs-lookup"><span data-stu-id="1cacf-277">Set **Field** to *Reference* and set **Criteria** to *Transfer order shipment*.</span></span>
1. <span data-ttu-id="1cacf-278">选择**确定**以返回到主对话框。</span><span class="sxs-lookup"><span data-stu-id="1cacf-278">Select **OK** to return to the main dialog box.</span></span>
1. <span data-ttu-id="1cacf-279">展开**后台运行**部分。</span><span class="sxs-lookup"><span data-stu-id="1cacf-279">Expand the **Run in the background** section.</span></span>
1. <span data-ttu-id="1cacf-280">启用**批处理**。</span><span class="sxs-lookup"><span data-stu-id="1cacf-280">Enable **Batch processing**.</span></span>
1. <span data-ttu-id="1cacf-281">选择**定期**并根据您的业务所需的时间间隔设置要处理的批处理作业。</span><span class="sxs-lookup"><span data-stu-id="1cacf-281">Select **Recurrence** and set up the batch job to process based on interval needed for your business.</span></span>
1. <span data-ttu-id="1cacf-282">选择**确定**以返回到主对话框。</span><span class="sxs-lookup"><span data-stu-id="1cacf-282">Select **OK** to return to the main dialog.</span></span>
1. <span data-ttu-id="1cacf-283">在主对话框中选择**确定**以将批处理作业添加到批处理队列。</span><span class="sxs-lookup"><span data-stu-id="1cacf-283">Select **OK** in the main dialog to have the batch job added to the batch queue.</span></span>

> [!NOTE]
> <span data-ttu-id="1cacf-284">有关详细信息，请参阅[从批处理作业确认出站装运](confirm-outbound-shipments-from-batch-jobs.md)。</span><span class="sxs-lookup"><span data-stu-id="1cacf-284">For more information, see [Confirm outbound shipments from batch jobs](confirm-outbound-shipments-from-batch-jobs.md).</span></span>

## <a name="processing-the-example-for-create-transfer-order-from-the-warehouse-app"></a><span data-ttu-id="1cacf-285">处理“通过仓库应用创建转移单”的示例</span><span class="sxs-lookup"><span data-stu-id="1cacf-285">Processing the example for "Create transfer order from the warehouse app"</span></span>

### <a name="add-on-hand-on-a-license-plate"></a><span data-ttu-id="1cacf-286">在牌照上添加现有库存</span><span class="sxs-lookup"><span data-stu-id="1cacf-286">Add on-hand on a license plate</span></span>

<span data-ttu-id="1cacf-287">在此方案中，首先您将需要具有包含实际可用的现有库存的牌照。</span><span class="sxs-lookup"><span data-stu-id="1cacf-287">As a starting point for this scenario you will need to have a license plate containing physical available inventory on hand.</span></span>

| <span data-ttu-id="1cacf-288">物料</span><span class="sxs-lookup"><span data-stu-id="1cacf-288">Item</span></span> | <span data-ttu-id="1cacf-289">存放地点</span><span class="sxs-lookup"><span data-stu-id="1cacf-289">Warehouse</span></span> | <span data-ttu-id="1cacf-290">库存状态</span><span class="sxs-lookup"><span data-stu-id="1cacf-290">Inventory status</span></span> | <span data-ttu-id="1cacf-291">库位</span><span class="sxs-lookup"><span data-stu-id="1cacf-291">Location</span></span> | <span data-ttu-id="1cacf-292">牌照</span><span class="sxs-lookup"><span data-stu-id="1cacf-292">License plate</span></span> | <span data-ttu-id="1cacf-293">数量</span><span class="sxs-lookup"><span data-stu-id="1cacf-293">Quantity</span></span> |
| --- | --- | --- | --- | --- | --- |
| <span data-ttu-id="1cacf-294">A0001</span><span class="sxs-lookup"><span data-stu-id="1cacf-294">A0001</span></span> | <span data-ttu-id="1cacf-295">51</span><span class="sxs-lookup"><span data-stu-id="1cacf-295">51</span></span> | <span data-ttu-id="1cacf-296">可用值</span><span class="sxs-lookup"><span data-stu-id="1cacf-296">Available</span></span> | <span data-ttu-id="1cacf-297">LP-010</span><span class="sxs-lookup"><span data-stu-id="1cacf-297">LP-010</span></span> | <span data-ttu-id="1cacf-298">LP10</span><span class="sxs-lookup"><span data-stu-id="1cacf-298">LP10</span></span> | <span data-ttu-id="1cacf-299">1</span><span class="sxs-lookup"><span data-stu-id="1cacf-299">1</span></span> |
| <span data-ttu-id="1cacf-300">A0002</span><span class="sxs-lookup"><span data-stu-id="1cacf-300">A0002</span></span> | <span data-ttu-id="1cacf-301">51</span><span class="sxs-lookup"><span data-stu-id="1cacf-301">51</span></span> | <span data-ttu-id="1cacf-302">可用值</span><span class="sxs-lookup"><span data-stu-id="1cacf-302">Available</span></span> | <span data-ttu-id="1cacf-303">LP-010</span><span class="sxs-lookup"><span data-stu-id="1cacf-303">LP-010</span></span> | <span data-ttu-id="1cacf-304">LP10</span><span class="sxs-lookup"><span data-stu-id="1cacf-304">LP10</span></span> | <span data-ttu-id="1cacf-305">2</span><span class="sxs-lookup"><span data-stu-id="1cacf-305">2</span></span> |

<span data-ttu-id="1cacf-306">使用以下值添加实际的现有库存数量：</span><span class="sxs-lookup"><span data-stu-id="1cacf-306">Add physical inventory on hand quantities by using the following values:</span></span>

> [!NOTE]
> <span data-ttu-id="1cacf-307">您将需要创建牌照并使用允许您具有混合物料的位置，例如 LP-010。</span><span class="sxs-lookup"><span data-stu-id="1cacf-307">You will need to create the license plate and use locations that allow you to carry mixed items, like LP-010.</span></span>

### <a name="create-and-process-transfer-orders-from-the-warehouse-app"></a><span data-ttu-id="1cacf-308">通过仓库应用创建和处理转移单</span><span class="sxs-lookup"><span data-stu-id="1cacf-308">Create and process transfer orders from the warehouse app</span></span>

1. <span data-ttu-id="1cacf-309">打开应用并以用户 *51* 身份登录。</span><span class="sxs-lookup"><span data-stu-id="1cacf-309">Open the app and sign in as user *51*.</span></span> <span data-ttu-id="1cacf-310">当前用户仓库将为 51。</span><span class="sxs-lookup"><span data-stu-id="1cacf-310">Current user warehouse will be 51.</span></span>
1. <span data-ttu-id="1cacf-311">从您在设置过程中将其添加到的菜单位置选择菜单项**创建到**。</span><span class="sxs-lookup"><span data-stu-id="1cacf-311">Select the menu item **Create TO** from the menu location you added it to during setup.</span></span>
1. <span data-ttu-id="1cacf-312">通过在**仓库**字段中输入目标仓库（至仓库）开始创建转移单，输入 *61*。</span><span class="sxs-lookup"><span data-stu-id="1cacf-312">Start the creation of a transfer order by entering the destination warehouse (To warehouse) in the **Warehouse** field, enter *61*.</span></span> <span data-ttu-id="1cacf-313">新的转移单将从当前仓库 51（从仓库）转到目标仓库 *61*。</span><span class="sxs-lookup"><span data-stu-id="1cacf-313">The new transfer order will be going from current warehouse 51 (From warehouse) to the destination warehouse *61*.</span></span>
1. <span data-ttu-id="1cacf-314">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="1cacf-314">Select **OK**.</span></span>
1. <span data-ttu-id="1cacf-315">在**牌照**字段中扫描牌照 ID。</span><span class="sxs-lookup"><span data-stu-id="1cacf-315">Scan a license plate ID in the **License plate** field.</span></span> <span data-ttu-id="1cacf-316">输入在上一步骤中添加的库存的牌照 *LP10*。</span><span class="sxs-lookup"><span data-stu-id="1cacf-316">Enter the license plate of the inventory added in an earlier step, *LP10*.</span></span>
1. <span data-ttu-id="1cacf-317">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="1cacf-317">Select **OK**.</span></span>
1. <span data-ttu-id="1cacf-318">选择菜单按钮，然后选择**完成订单**完成仓库应用转移单创建。</span><span class="sxs-lookup"><span data-stu-id="1cacf-318">Select the menu button and then select **Complete order** to finalize the warehouse app transfer order creation.</span></span>

<span data-ttu-id="1cacf-319">对于上述示例，使用两个**仓库应用事件**（*创建转移单*和*完成转移单*）。</span><span class="sxs-lookup"><span data-stu-id="1cacf-319">For the mentioned example, two **Warehouse app events** (*Create transfer order* and *Complete transfer order*) are used.</span></span>

### <a name="inquire-the-warehouse-app-events"></a><a name="#inquire-the-warehouse-app-events"></a><span data-ttu-id="1cacf-320">查询仓库应用事件</span><span class="sxs-lookup"><span data-stu-id="1cacf-320">Inquire the warehouse app events</span></span>

<span data-ttu-id="1cacf-321">您可以通过转到**仓库管理 \> 查询和报表 \> 移动设备日志 \> 仓库应用事件**查看仓库应用生成的事件队列和事件消息。</span><span class="sxs-lookup"><span data-stu-id="1cacf-321">You can view the event queue and events messages generated by the warehouse app by going to **Warehouse management \> Inquiries and reports \> Mobile device logs \> Warehouse app events**.</span></span>

<span data-ttu-id="1cacf-322">*创建转移单*事件消息将收到状态*等待*，这意味着**处理仓库应用事件**批处理作业将不会接收并处理事件消息。</span><span class="sxs-lookup"><span data-stu-id="1cacf-322">The *Create transfer order* event messages will receive the status *Waiting*, which means that the **Process warehouse app events** batch job will not pick up and process the event messages.</span></span> <span data-ttu-id="1cacf-323">一旦事件消息更新为状态*已排队*，批处理作业将处理事件。</span><span class="sxs-lookup"><span data-stu-id="1cacf-323">As soon as the event message updates to status *Queued*, the batch job will process the events.</span></span> <span data-ttu-id="1cacf-324">这将与创建*完成转移单*事件（当工作人员在仓库应用上选择**完成订单**按钮时）同时发生。</span><span class="sxs-lookup"><span data-stu-id="1cacf-324">This will happen at the same time as the creation of the *Complete transfer order* event (when a worker selects the**Complete order** button on the warehouse app).</span></span> <span data-ttu-id="1cacf-325">当*创建转移单*事件消息已处理时，状态将更新为*已完成*或*失败*。</span><span class="sxs-lookup"><span data-stu-id="1cacf-325">When the *Create transfer order* event messages has been processed, the status is updated to *Completed* or *Failed*.</span></span> <span data-ttu-id="1cacf-326">当*完成转移单*状态更新为*已完成*时，所有相关事件将从队列中删除。</span><span class="sxs-lookup"><span data-stu-id="1cacf-326">When the *Complete transfer order* status is updated to *Completed*, all the related events are deleted from the queue.</span></span>

<span data-ttu-id="1cacf-327">因为在消息更新为状态*已排队*之前，批处理作业将不会处理创建转移单数据**仓库应用事件**，因此您将需要查找请求的转移单号作为**标识符**字段的一部分。</span><span class="sxs-lookup"><span data-stu-id="1cacf-327">Because the **Warehouse app events** for the creation of transfer order data will not be processed by the batch job before the messages iss updated to status *Queued*, you will need to look up the requested transfer order numbers as part of the **Identifier** field.</span></span> <span data-ttu-id="1cacf-328">**标识符**字段位于**仓库应用事件**页面的顶部。</span><span class="sxs-lookup"><span data-stu-id="1cacf-328">The **Identifier** field is in the header of the **Warehouse app events** page.</span></span>

<span data-ttu-id="1cacf-329">作为仓库事件处理的一部分，创建转移单行可能会失败。</span><span class="sxs-lookup"><span data-stu-id="1cacf-329">As part of the warehouse event processing, the creation of the transfer order line might fail.</span></span> <span data-ttu-id="1cacf-330">在这种情况下，事件消息的状态将更新为*失败*，您可以使用**批处理日志**信息了解原因并采取措施纠正任何问题。</span><span class="sxs-lookup"><span data-stu-id="1cacf-330">In this case, the state of the event message is updated to *Failed* and you can use the **Batch log** information to learn why and take action to correct any problems.</span></span>

<span data-ttu-id="1cacf-331">典型的问题可能与缺少过程设置有关，例如缺少*创建转移单*事件的中转仓库。</span><span class="sxs-lookup"><span data-stu-id="1cacf-331">Typical issues could be related to missing setup for the process, like a missing transit warehouse for the *Create transfer order* event.</span></span> <span data-ttu-id="1cacf-332">在这样的示例中，您可以将中转仓库添加到装运仓库，并使用**重置**选项将所有仓库应用事件消息从*失败*更改为*已排队*，这意味着批处理作业将在更正设置数据后再次处理事件消息。</span><span class="sxs-lookup"><span data-stu-id="1cacf-332">In an example like this, you would add a transit warehouse to the shipping warehouse and use the **Reset** option to change the status for all the warehouse app event messages from *Failed* to *Queued*, which means that the batch job will process the event messages again after the correction of the setup data.</span></span>

<span data-ttu-id="1cacf-333">在生产环境中，异常与过程的相关性更高，例如拥有请求的牌照，该牌照在批处理作业处理时为空，因此不会创建转移单行。</span><span class="sxs-lookup"><span data-stu-id="1cacf-333">Within production environments, the exceptions would be more process related, such as having a requested license plate, which at the batch job processing time is empty and thereby no transfer order lines are created.</span></span> <span data-ttu-id="1cacf-334">可以使用**删除**选项删除此失败的事件消息，或者您可以在牌照上添加所需的实际现有库存并针对所有相关的事件消息使用**重置**选项。</span><span class="sxs-lookup"><span data-stu-id="1cacf-334">This failed event message can either be removed by using the **Delete** option or you can add the needed physical on-hand on the license plate and use the **Reset** option for all the related event messages.</span></span>

<span data-ttu-id="1cacf-335">有关详细信息，请参阅[仓库应用事件处理](warehouse-app-events.md)。</span><span class="sxs-lookup"><span data-stu-id="1cacf-335">For more information, see [Warehouse app event processing](warehouse-app-events.md).</span></span>

### <a name="follow-up-on-the-example-scenario-processing"></a><span data-ttu-id="1cacf-336">跟进示例方案处理</span><span class="sxs-lookup"><span data-stu-id="1cacf-336">Follow up on the example scenario processing</span></span>

<span data-ttu-id="1cacf-337">在此方案中，将发生以下事件：</span><span class="sxs-lookup"><span data-stu-id="1cacf-337">During this scenario, the following occurred:</span></span>

1. <span data-ttu-id="1cacf-338">您使用仓库应用选择了一个使用活动代码**通过牌照创建转移单**的菜单项。</span><span class="sxs-lookup"><span data-stu-id="1cacf-338">Using the warehouse app, you selected a menu item that uses the activity code **Create transfer order from license plates**.</span></span>
1. <span data-ttu-id="1cacf-339">该应用提示您选择转移单的目标仓库。</span><span class="sxs-lookup"><span data-stu-id="1cacf-339">The app prompted you to select the destination warehouse for the transfer order.</span></span> <span data-ttu-id="1cacf-340">源仓库始终是您当前以工作人员身份登录的仓库。</span><span class="sxs-lookup"><span data-stu-id="1cacf-340">The source warehouse is always the one you currently are signed into as a Worker.</span></span>
1. <span data-ttu-id="1cacf-341">在选择目标仓库时，系统将为即将生成的转移单预留一个 ID 号（基于在您的系统上定义的转移单号顺序），但尚未创建转移单。</span><span class="sxs-lookup"><span data-stu-id="1cacf-341">On the selection of the destination warehouse, the system reserved an ID number for the upcoming transfer order (based on the transfer-order number sequence defined on your system) but didn't create the transfer order yet.</span></span>
1. <span data-ttu-id="1cacf-342">当您扫描包含应移至新仓库的现有库存的牌照 *LP10* 时，**仓库应用事件**已添加到事件队列中，以便稍后处理。</span><span class="sxs-lookup"><span data-stu-id="1cacf-342">When you scanned the license plate *LP10* containing on-hand inventory that should be moved to the new warehouse, a **Warehouse app event** was added to the events queue to be processed later.</span></span> <span data-ttu-id="1cacf-343">仓库事件包含有关扫描的消息详细信息，包括预期的转移单号。</span><span class="sxs-lookup"><span data-stu-id="1cacf-343">The warehouse event contained message details about the scan, including the intended transfer-order number.</span></span>
1. <span data-ttu-id="1cacf-344">在仓库应用上，当选择**完成订单**按钮时，将创建一个新的仓库应用事件**完成转移单**，并将相关现有事件**创建转移单**的状态更改为**已排队**。</span><span class="sxs-lookup"><span data-stu-id="1cacf-344">On the warehouse app when the **Complete order** button is selected, a new warehouse app event, **Complete transfer order**, is created and the related existing event, **Create transfer order**, changed status to **Queued**.</span></span>
1. <span data-ttu-id="1cacf-345">在后端，**处理仓库应用事件批处理作业**接收**已排队**事件，并收集与扫描的牌照相关的现有库存。</span><span class="sxs-lookup"><span data-stu-id="1cacf-345">On the back end, the **Process warehouse app events batch job** picked up the **Queued** event and collected the on-hand related to the scanned license plate.</span></span> <span data-ttu-id="1cacf-346">根据现有库存创建实际转移单记录和关联的行。</span><span class="sxs-lookup"><span data-stu-id="1cacf-346">Based on the on-hand the actual transfer order record and associated lines got created.</span></span> <span data-ttu-id="1cacf-347">在配置*发放和装运确认*并针对**牌照引导**战略的行链接牌照后，该作业还使用值填充了转移单的**出站装运策略**字段。</span><span class="sxs-lookup"><span data-stu-id="1cacf-347">The job also populated the **Outbound shipment policy** field for the transfer order with the value based to configured *Release and ship confirm* and linked the license plate against the lines for the **License plate guided** strategy.</span></span>
1. <span data-ttu-id="1cacf-348">根据转移单行**出站装运策略**字段值，**自动发放转移单批处理作业**查询现在将转移单发放到装运仓库。</span><span class="sxs-lookup"><span data-stu-id="1cacf-348">Based on the transfer order line **Outbound shipment policy** field value the **Automatic release of transfer orders batch job** query now resulted in releasing the transfer order to the shipping warehouse.</span></span> <span data-ttu-id="1cacf-349">由于使用的**波次模板**、**工作模板**和**位置指令**设置，工作会自动处理，**负载状态**会更新为*已负载*。</span><span class="sxs-lookup"><span data-stu-id="1cacf-349">And due to the setup for the used **Wave template**, **Work template**, and **Location directives** the work got auto processes resulting on the **Load status** got updated to *Loaded*.</span></span>
1. <span data-ttu-id="1cacf-350">将针对负载执行**处理出站装运批处理作业**，从而装运转移单并生成装运前通知 (ASN)。</span><span class="sxs-lookup"><span data-stu-id="1cacf-350">The **Process outbound shipment batch job** is executed for the load, resulting in the transfer order being shipped and the Advance Shipment Notice (ASN) is generated.</span></span>
1. <span data-ttu-id="1cacf-351">所有这些事件的发生时间取决于创建的批处理作业的**定期**设置。</span><span class="sxs-lookup"><span data-stu-id="1cacf-351">The timing of all these events is dependent on the **Recurrence** settings for the batch jobs created.</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="1cacf-352">常见问题</span><span class="sxs-lookup"><span data-stu-id="1cacf-352">Frequently asked questions</span></span>

### <a name="mobile-device-menu-item-setup"></a><span data-ttu-id="1cacf-353">移动设备菜单项设置</span><span class="sxs-lookup"><span data-stu-id="1cacf-353">Mobile device menu item setup</span></span>

#### <a name="why-cant-i-see-create-transfer-order-from-license-plate-in-the-menu-item-work-activity-drop-down-list"></a><span data-ttu-id="1cacf-354">为什么在菜单项工作活动下拉列表中看不到“通过牌照创建转移单”？</span><span class="sxs-lookup"><span data-stu-id="1cacf-354">Why can’t I see "Create transfer order from license plate" in the menu item work activity drop-down list?</span></span>

<span data-ttu-id="1cacf-355">必须启用功能*通过仓库应用创建和处理转移单*。</span><span class="sxs-lookup"><span data-stu-id="1cacf-355">The feature *Create and process transfer orders from the warehouse app* must be enabled.</span></span> <span data-ttu-id="1cacf-356">有关详细信息，请参阅[启用通过仓库应用创建转移单](#enable-create-transfer-order-from-warehouse-app)。</span><span class="sxs-lookup"><span data-stu-id="1cacf-356">For more information, see [Enable the create transfer orders from Warehouse app](#enable-create-transfer-order-from-warehouse-app).</span></span>

### <a name="warehouse-app-processes"></a><span data-ttu-id="1cacf-357">仓库应用过程</span><span class="sxs-lookup"><span data-stu-id="1cacf-357">Warehouse app processes</span></span>

#### <a name="why-cant-i-see-the-menu-button-complete-order"></a><span data-ttu-id="1cacf-358">为什么看不到菜单按钮“完成订单”？</span><span class="sxs-lookup"><span data-stu-id="1cacf-358">Why can’t I see the menu button "Complete order"?</span></span>

<span data-ttu-id="1cacf-359">您必须为转移单分配至少一个牌照。</span><span class="sxs-lookup"><span data-stu-id="1cacf-359">You must have at least one license plate assigned to the transfer order.</span></span>

#### <a name="can-several-warehouse-app-users-add-license-plates-to-the-same-transfer-order-at-the-same-time"></a><span data-ttu-id="1cacf-360">多个仓库应用用户是否可以同时向同一转移单添加牌照？</span><span class="sxs-lookup"><span data-stu-id="1cacf-360">Can several warehouse app users add license plates to the same transfer order at the same time?</span></span>

<span data-ttu-id="1cacf-361">是，多个仓库工作人员可以将牌照扫描到同一转移单中。</span><span class="sxs-lookup"><span data-stu-id="1cacf-361">Yes, several warehouse workers can scan license plates into the same transfer order.</span></span>

#### <a name="can-the-same-license-plate-be-added-to-different-transfer-orders"></a><span data-ttu-id="1cacf-362">同一牌照是否可以添加到不同的转移单？</span><span class="sxs-lookup"><span data-stu-id="1cacf-362">Can the same license plate be added to different transfer orders?</span></span>

<span data-ttu-id="1cacf-363">否，一次只能向一个转移单添加一个牌照。</span><span class="sxs-lookup"><span data-stu-id="1cacf-363">No, a license plate can only be added to one transfer order at the time.</span></span>

#### <a name="after-having-selected-the-complete-order-button-can-i-then-add-more-license-plates-for-that-transfer-order"></a><span data-ttu-id="1cacf-364">选择“完成订单”按钮后，是否可以为该转移单添加更多牌照？</span><span class="sxs-lookup"><span data-stu-id="1cacf-364">After having selected the "Complete order" button, can I then add more license plates for that transfer order?</span></span>

<span data-ttu-id="1cacf-365">否，您不能向具有**完成转移单**仓库应用事件的转移单添加更多牌照。</span><span class="sxs-lookup"><span data-stu-id="1cacf-365">No, you can't add more license plates to a transfer order that has a **Complete transfer order** warehouse app event.</span></span>

#### <a name="how-can-i-find-existing-transfer-orders-to-be-used-via-the-select-transfer-order-button-in-the-warehouse-app-if-the-order-has-not-yet-been-created-in-the-backend-system"></a><span data-ttu-id="1cacf-366">如果尚未在后端系统中创建订单，如何通过仓库应用中的“选择转移单”按钮找到要使用的现有转移单？</span><span class="sxs-lookup"><span data-stu-id="1cacf-366">How can I find existing transfer orders to be used via the "Select transfer order" button in the warehouse app, if the order has not yet been created in the backend system?</span></span>

<span data-ttu-id="1cacf-367">目前，您无法在应用中查找转移单，但可以在**仓库应用事件**页面上找到转移单号。</span><span class="sxs-lookup"><span data-stu-id="1cacf-367">Currently, you can't look up transfer orders in the app, but you can find the transfer order numbers on the **Warehouse app events** page.</span></span> <span data-ttu-id="1cacf-368">有关详细信息，请参阅[查询仓库应用事件](#inquire-the-warehouse-app-events)。</span><span class="sxs-lookup"><span data-stu-id="1cacf-368">For more information, see [Inquire the warehouse app events](#inquire-the-warehouse-app-events).</span></span>

#### <a name="can-i-manually-select-the-transfer-order-number-to-be-used-from-the-warehouse-app"></a><span data-ttu-id="1cacf-369">我是否可以从仓库应用中手动选择要使用的转移单号？</span><span class="sxs-lookup"><span data-stu-id="1cacf-369">Can I manually select the transfer order number to be used from the warehouse app?</span></span>

<span data-ttu-id="1cacf-370">仅支持通过编号规则自动生成的转移单号。</span><span class="sxs-lookup"><span data-stu-id="1cacf-370">Only autogenerated transfer order numbers via number sequences are supported.</span></span>

### <a name="background-processing"></a><span data-ttu-id="1cacf-371">后台处理</span><span class="sxs-lookup"><span data-stu-id="1cacf-371">Background processing</span></span>

#### <a name="how-should-i-clean-up-records-in-my-warehouse-app-events-queue-message-tables"></a><span data-ttu-id="1cacf-372">我应该如何清理仓库应用事件队列消息表中的记录？</span><span class="sxs-lookup"><span data-stu-id="1cacf-372">How should I clean up records in my warehouse app events queue message tables?</span></span>

<span data-ttu-id="1cacf-373">您可以在**仓库应用事件**页面上查看和维护记录。</span><span class="sxs-lookup"><span data-stu-id="1cacf-373">You can view and maintain this on the **Warehouse app events** page.</span></span> <span data-ttu-id="1cacf-374">有关详细信息，请参阅[查询仓库应用事件](#inquire-the-warehouse-app-events)。</span><span class="sxs-lookup"><span data-stu-id="1cacf-374">For more information, see [Inquire the warehouse app events](#inquire-the-warehouse-app-events).</span></span>

#### <a name="why-is-the-transfer-order-receipt-date-not-updated-according-to-my-delivery-date-control-setup"></a><span data-ttu-id="1cacf-375">为什么未根据我的“交货日期控制”设置更新转移单“收货日期”？</span><span class="sxs-lookup"><span data-stu-id="1cacf-375">Why is the transfer order "Receipt date" not updated according to my "Delivery date control" setup?</span></span>

<span data-ttu-id="1cacf-376">转移单不是使用**交货日期控制**功能创建的。</span><span class="sxs-lookup"><span data-stu-id="1cacf-376">The transfer orders are created without using the **Delivery date control** capabilities.</span></span>

#### <a name="can-i-use-a-license-plate-having-physical-negative-inventory-on-hand"></a><span data-ttu-id="1cacf-377">我是否可以使用实际的现有库存为负的牌照？</span><span class="sxs-lookup"><span data-stu-id="1cacf-377">Can I use a license plate having physical negative inventory on hand?</span></span>

<span data-ttu-id="1cacf-378">该功能仅支持数量为正的实际现有库存。</span><span class="sxs-lookup"><span data-stu-id="1cacf-378">The feature only supports positive physical on-hand quantities.</span></span> <span data-ttu-id="1cacf-379">在将牌照分配给转移单之前，请确保仓库和库存状态级别上的实际现有库存数量为正。</span><span class="sxs-lookup"><span data-stu-id="1cacf-379">Make sure that you have positive physical on-hand quantities at the warehouse and inventory status level before assigning license plates to a transfer order.</span></span>
