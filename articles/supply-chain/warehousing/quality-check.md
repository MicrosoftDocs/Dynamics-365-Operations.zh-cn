---
title: 质量检查
description: 本主题提供有关质量检查功能的信息。 此功能使仓库工作人员在将物料接收到进货台区域时可以快速进行质量抽查。
author: mirzaab
manager: tfehr
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSQualityCheckTemplate,WHSWorkClass,WHSWorkTemplateTable.WHSLocDirTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 44a4694281f3dd53581c9d8245a0105b37b2b155
ms.sourcegitcommit: 7dc2ff9461c310324937bea2fc160ff056fefd8a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/11/2020
ms.locfileid: "3686349"
---
# <a name="quality-check"></a><span data-ttu-id="bde79-104">质量检查</span><span class="sxs-lookup"><span data-stu-id="bde79-104">Quality check</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bde79-105">*质量检查*功能使仓库工作人员在将物料接收到进货台区域时可以快速进行质量抽查。</span><span class="sxs-lookup"><span data-stu-id="bde79-105">The *Quality check* feature lets warehouse workers do quick spot checks for quality while they receive items to the inbound dock area.</span></span> <span data-ttu-id="bde79-106">当工作人员检查物料的包装或其他易于识别的物料部分时，这些抽查非常有用。</span><span class="sxs-lookup"><span data-stu-id="bde79-106">These spot checks are beneficial when workers inspect packaging or other easily recognizable parts of an item.</span></span> <span data-ttu-id="bde79-107">此功能可以指导工作人员快速查看库存是否有明显缺陷或损坏，然后再将库存存放到储存位置。</span><span class="sxs-lookup"><span data-stu-id="bde79-107">The feature guides workers to take a quick look to see whether anything is obviously faulty or damaged before they stock the inventory in its putaway location.</span></span>

<span data-ttu-id="bde79-108">此功能是标准质量检查流程的替代方法。</span><span class="sxs-lookup"><span data-stu-id="bde79-108">This feature is an alternative to the standard quality check process.</span></span> <span data-ttu-id="bde79-109">它提供更大的灵活性和更快的处理速度。</span><span class="sxs-lookup"><span data-stu-id="bde79-109">It offers more flexibility and faster processing.</span></span>

<span data-ttu-id="bde79-110">使用此功能时，到达和质量检查通过以下方式进行：</span><span class="sxs-lookup"><span data-stu-id="bde79-110">When you use this feature, the arrival and quality check occur in the following way:</span></span>

1. <span data-ttu-id="bde79-111">在装运到达时，仓库工作人员登记到达。</span><span class="sxs-lookup"><span data-stu-id="bde79-111">When a shipment arrives, a warehouse worker registers the arrival.</span></span> <span data-ttu-id="bde79-112">工作人员还将扫描牌照来登记位置。</span><span class="sxs-lookup"><span data-stu-id="bde79-112">The worker also scans a license plate to register the location.</span></span>
1. <span data-ttu-id="bde79-113">工作人员进行快速质量检查，并记录该牌照的结果（通过或未通过）。</span><span class="sxs-lookup"><span data-stu-id="bde79-113">The worker does a quick quality check and records the result (pass or fail) for that license plate.</span></span>
1. <span data-ttu-id="bde79-114">将进行以下操作之一：</span><span class="sxs-lookup"><span data-stu-id="bde79-114">One of the following actions occurs:</span></span>

    - <span data-ttu-id="bde79-115">如果通过了质量检查，将照常接受牌照并将其引导到接收位置。</span><span class="sxs-lookup"><span data-stu-id="bde79-115">If the quality check is passed, the license plate is accepted and guided to a receiving location, as usual.</span></span>
    - <span data-ttu-id="bde79-116">如果质量检查未通过，将拒绝牌照，并将其现有的储存工作重定向到另一个位置，以进行进一步检查。</span><span class="sxs-lookup"><span data-stu-id="bde79-116">If the quality check is failed, the license plate is rejected, and existing putaway work for it is redirected to an alternate location for further inspection.</span></span> <span data-ttu-id="bde79-117">新的质检订单将创建。</span><span class="sxs-lookup"><span data-stu-id="bde79-117">A new quality order is created.</span></span> <span data-ttu-id="bde79-118">要查看未通过质量检查时创建的质检订单，请转到**库存管理 \> 定期任务 \> 质量管理 \> 质检订单**。</span><span class="sxs-lookup"><span data-stu-id="bde79-118">To view the quality order that is created from the failed quality check, go to **Inventory management \> Periodic tasks \> Quality management \> Quality orders**.</span></span>

<span data-ttu-id="bde79-119">也可以对此流程进行设置，将所有扫描的牌照立即转移到质量检查位置。</span><span class="sxs-lookup"><span data-stu-id="bde79-119">This process can also be set up so that all scanned license plates are immediately diverted to the quality check location.</span></span>

## <a name="turn-on-the-quality-check-feature"></a><span data-ttu-id="bde79-120">开启“质量检查”功能</span><span class="sxs-lookup"><span data-stu-id="bde79-120">Turn on the Quality check feature</span></span>

<span data-ttu-id="bde79-121">*质量检查*功能只有在系统中开启之后才能使用。</span><span class="sxs-lookup"><span data-stu-id="bde79-121">Before you can use the *Quality check* feature, it must be turned on in your system.</span></span> <span data-ttu-id="bde79-122">管理员可以使用[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)设置检查功能状态和开启功能（如果需要）。</span><span class="sxs-lookup"><span data-stu-id="bde79-122">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="bde79-123">在**功能管理**工作区中，此功能按照下面的方式列出：</span><span class="sxs-lookup"><span data-stu-id="bde79-123">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="bde79-124">**模块**：*仓库管理*</span><span class="sxs-lookup"><span data-stu-id="bde79-124">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="bde79-125">**功能名称**：*质量检查*</span><span class="sxs-lookup"><span data-stu-id="bde79-125">**Feature name:** *Quality check*</span></span>

## <a name="set-up-the-feature-for-the-example-scenario"></a><span data-ttu-id="bde79-126">为示例方案设置此功能</span><span class="sxs-lookup"><span data-stu-id="bde79-126">Set up the feature for the example scenario</span></span>

<span data-ttu-id="bde79-127">本节提供指南和示例，演示如何设置*质量检查*功能，以及如何为本主题后面提供的示例方案准备示例数据。</span><span class="sxs-lookup"><span data-stu-id="bde79-127">This section provides guidelines and an example that shows how to set up the *Quality check* feature and prepare sample data for the example scenario that is provided later in this topic.</span></span>

### <a name="make-sample-data-available"></a><span data-ttu-id="bde79-128">提供示例数据</span><span class="sxs-lookup"><span data-stu-id="bde79-128">Make sample data available</span></span>

<span data-ttu-id="bde79-129">若要使用此处指定的示例记录和值演练[示例方案](#example-scenario)，使用的系统中必须已安装标准[演示数据](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md)。</span><span class="sxs-lookup"><span data-stu-id="bde79-129">To work through the [example scenario](#example-scenario) by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="bde79-130">此外，开始前，还必须选择 **USMF** 法人。</span><span class="sxs-lookup"><span data-stu-id="bde79-130">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

### <a name="quality-check-template"></a><a name="quality-template"></a><span data-ttu-id="bde79-131">质量检查模板</span><span class="sxs-lookup"><span data-stu-id="bde79-131">Quality check template</span></span>

<span data-ttu-id="bde79-132">质量检查模板定义了在接收时进行快速质量抽查的规则。</span><span class="sxs-lookup"><span data-stu-id="bde79-132">The quality check template defines the rules for doing quick spot checks for quality at the time of receiving.</span></span>

1. <span data-ttu-id="bde79-133">转到**仓库管理 \> 设置 \> 工作 \> 质量检查模板**。</span><span class="sxs-lookup"><span data-stu-id="bde79-133">Go to **Warehouse management \> Setup \> Work \> Quality check template**.</span></span>
1. <span data-ttu-id="bde79-134">选择**新建**向网格添加模板。</span><span class="sxs-lookup"><span data-stu-id="bde79-134">Select **New** to add a template to the grid.</span></span>
1. <span data-ttu-id="bde79-135">设置以下值来定义新模板：</span><span class="sxs-lookup"><span data-stu-id="bde79-135">Set the following values to define the new template:</span></span>

    - <span data-ttu-id="bde79-136">**质量检查模板名称**：*货台检查*</span><span class="sxs-lookup"><span data-stu-id="bde79-136">**Quality check template name:** *Dock check*</span></span>

        <span data-ttu-id="bde79-137">输入标识用于此模板的策略的名称。</span><span class="sxs-lookup"><span data-stu-id="bde79-137">Enter a name that identifies the policies applied for this template.</span></span>

    - <span data-ttu-id="bde79-138">**接受策略**：*提示用户*</span><span class="sxs-lookup"><span data-stu-id="bde79-138">**Acceptance policy:** *Prompt user*</span></span>

        <span data-ttu-id="bde79-139">指定用户在处理工作时是否应提示用户接受或拒绝库存质量，或是否应自动拒绝质量。</span><span class="sxs-lookup"><span data-stu-id="bde79-139">Specify whether users should be prompted to accept or reject the quality of the inventory while they process the work, or whether the quality should automatically be rejected.</span></span> <span data-ttu-id="bde79-140">可用选项有*自动拒绝*和*提示用户*。</span><span class="sxs-lookup"><span data-stu-id="bde79-140">The available options are *Auto reject* and *Prompt user*.</span></span>

    - <span data-ttu-id="bde79-141">**质量处理策略**：*创建质检订单*</span><span class="sxs-lookup"><span data-stu-id="bde79-141">**Quality processing policy:** *Create quality order*</span></span>

        <span data-ttu-id="bde79-142">选择在拒绝库存质量时应使用的策略。</span><span class="sxs-lookup"><span data-stu-id="bde79-142">Select the policy that should be used when the quality of the inventory is rejected.</span></span> <span data-ttu-id="bde79-143">选项如下：</span><span class="sxs-lookup"><span data-stu-id="bde79-143">The following options are available:</span></span>

        - <span data-ttu-id="bde79-144">*仅创建工作* – 仅创建工作来推进库存移动。</span><span class="sxs-lookup"><span data-stu-id="bde79-144">*Create work only* – Just create work to facilitate inventory movement.</span></span>
        - <span data-ttu-id="bde79-145">*创建质检订单* – 创建质检订单来推进质量测试。</span><span class="sxs-lookup"><span data-stu-id="bde79-145">*Create quality order* – Create a quality order to facilitate quality tests.</span></span>

    - <span data-ttu-id="bde79-146">**测试组：** *机箱*</span><span class="sxs-lookup"><span data-stu-id="bde79-146">**Test group:** *Enclosure*</span></span>

        <span data-ttu-id="bde79-147">指定应该在创建的质检订单中使用的测试组。</span><span class="sxs-lookup"><span data-stu-id="bde79-147">Specify the test group that should be used in the quality order that is created.</span></span> <span data-ttu-id="bde79-148">测试组在**库存管理**模块中设置。</span><span class="sxs-lookup"><span data-stu-id="bde79-148">Test groups are set up in the **Inventory management** module.</span></span>

        <span data-ttu-id="bde79-149">保持测试组的**破坏性测试**选项为关闭状态。</span><span class="sxs-lookup"><span data-stu-id="bde79-149">Leave the **Destructive text** option turned off for the test group.</span></span> <span data-ttu-id="bde79-150">此选项定义是否将样品作为测试组中测试的一部分销毁。</span><span class="sxs-lookup"><span data-stu-id="bde79-150">This option defines whether the sample will be destroyed as part of the tests in the test group.</span></span> <span data-ttu-id="bde79-151">如果使用破坏性测试，在为物料创建质检订单时，系统会生成库存交易记录。</span><span class="sxs-lookup"><span data-stu-id="bde79-151">If a destructive test is used, the system generates an inventory transaction when a quality order is created for an item.</span></span> <span data-ttu-id="bde79-152">新的库存交易记录预测测试数量的库存减少。</span><span class="sxs-lookup"><span data-stu-id="bde79-152">The new inventory transaction predicts the inventory reduction for the test quantity.</span></span> <span data-ttu-id="bde79-153">通过验证步骤完成质检订单后，将出现库存减少。</span><span class="sxs-lookup"><span data-stu-id="bde79-153">The inventory reduction occurs when the quality order is completed through the validation step.</span></span> <span data-ttu-id="bde79-154">库存交易记录标识为质检订单。</span><span class="sxs-lookup"><span data-stu-id="bde79-154">The inventory transaction is identified as a quality order.</span></span>

### <a name="work-class--quality-check"></a><a name="work-class"></a><span data-ttu-id="bde79-155">工作类 – 质量检查</span><span class="sxs-lookup"><span data-stu-id="bde79-155">Work class – Quality check</span></span>

<span data-ttu-id="bde79-156">工作类用于处理和/或限制工作指令行的类型，以便仓库工作人员可以在移动设备上进行处理。</span><span class="sxs-lookup"><span data-stu-id="bde79-156">Work classes are used to direct and/or limit the type of work order lines that warehouse workers can process on a mobile device.</span></span>

1. <span data-ttu-id="bde79-157">转到**仓库管理 \> 设置 \> 工作 \> 工作类**。</span><span class="sxs-lookup"><span data-stu-id="bde79-157">Go to **Warehouse management \> Setup \> Work \> Work classes**.</span></span>
1. <span data-ttu-id="bde79-158">选择**新建**创建工作类。</span><span class="sxs-lookup"><span data-stu-id="bde79-158">Select **New** to create a work class.</span></span>
1. <span data-ttu-id="bde79-159">在标题中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="bde79-159">In the header, set the following values:</span></span>

    - <span data-ttu-id="bde79-160">**工作类 ID**：*QC Check*</span><span class="sxs-lookup"><span data-stu-id="bde79-160">**Work class ID:** *QC Check*</span></span>

        <span data-ttu-id="bde79-161">输入标识工作类的名称。</span><span class="sxs-lookup"><span data-stu-id="bde79-161">Enter a name that identifies the work class.</span></span>

    - <span data-ttu-id="bde79-162">**描述**：*质检*</span><span class="sxs-lookup"><span data-stu-id="bde79-162">**Description:** *QC Check*</span></span>

        <span data-ttu-id="bde79-163">输入说明工作类的用途的简短描述。</span><span class="sxs-lookup"><span data-stu-id="bde79-163">Enter a short description that indicates what the work class is used for.</span></span>

    - <span data-ttu-id="bde79-164">**工作订单类型**：*质量检查质量*</span><span class="sxs-lookup"><span data-stu-id="bde79-164">**Work order type:** *Quality in quality check*</span></span>

        <span data-ttu-id="bde79-165">选择工作类创建的工作订单类型。</span><span class="sxs-lookup"><span data-stu-id="bde79-165">Select the type of work order that is created by the work class.</span></span> <span data-ttu-id="bde79-166">设置质量控制工作时，请始终选择*质量检查质量*。</span><span class="sxs-lookup"><span data-stu-id="bde79-166">When you set up quality control work, always select *Quality in quality check*.</span></span>

1. <span data-ttu-id="bde79-167">在**有效放置位置类型**快速选项卡上，保留**位置类型**字段为空。</span><span class="sxs-lookup"><span data-stu-id="bde79-167">On the **Valid put location types** FastTab, leave the **Location type** field blank.</span></span>

    <span data-ttu-id="bde79-168">如果选择位置类型，应限制在物料领取后可以放置物料的位置。</span><span class="sxs-lookup"><span data-stu-id="bde79-168">If you select a location type, you limit the locations where items can be put after they are picked.</span></span> <span data-ttu-id="bde79-169">在位置指令尝试决定位置，或者当仓库工作人员手动指定移动设备菜单项的位置时，将使用此字段。</span><span class="sxs-lookup"><span data-stu-id="bde79-169">This field is used when a location directive tries to resolve the location, or when a warehouse worker manually specifies the location for the mobile device menu item.</span></span>

<span data-ttu-id="bde79-170">有关工作类以及如何创建工作类的详细信息，请参阅[创建工作类](tasks/create-work-class.md)。</span><span class="sxs-lookup"><span data-stu-id="bde79-170">For more information about work classes and how to create them, see [Create a work class](tasks/create-work-class.md).</span></span>

### <a name="work-template"></a><span data-ttu-id="bde79-171">工作模板</span><span class="sxs-lookup"><span data-stu-id="bde79-171">Work template</span></span>

<span data-ttu-id="bde79-172">工作模板可以定义必须在仓库中执行的工作操作。</span><span class="sxs-lookup"><span data-stu-id="bde79-172">Work templates let you define the work operations that must be performed in the warehouse.</span></span> <span data-ttu-id="bde79-173">通常，仓库工作操作包括一个对操作：仓库工作人员在一个库位领取现有库存量，然后将领取的库存放到另一个位置。</span><span class="sxs-lookup"><span data-stu-id="bde79-173">Typically, warehouse work operations consist of a pair of actions: a warehouse worker picks on-hand inventory up in one location and then puts the picked inventory down in another location.</span></span> <span data-ttu-id="bde79-174">用于质量控制的工作模板定义用于进行质量检查的工作操作。</span><span class="sxs-lookup"><span data-stu-id="bde79-174">A work template for quality control defines the work operations for doing quality checks.</span></span>

#### <a name="purchase-orders"></a><span data-ttu-id="bde79-175">采购订单</span><span class="sxs-lookup"><span data-stu-id="bde79-175">Purchase orders</span></span>

1. <span data-ttu-id="bde79-176">转到**仓库管理 \> 设置 \> 工作 \> 工作模板**。</span><span class="sxs-lookup"><span data-stu-id="bde79-176">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="bde79-177">在标题中，将**工作订单类型**字段设置为*采购订单*。</span><span class="sxs-lookup"><span data-stu-id="bde79-177">In the header, set the **Work order type** field to *Purchase orders*.</span></span>
1. <span data-ttu-id="bde79-178">在操作窗格上，选择**编辑**。</span><span class="sxs-lookup"><span data-stu-id="bde79-178">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="bde79-179">选择一个应包含质量检查步骤的工作模板。</span><span class="sxs-lookup"><span data-stu-id="bde79-179">Select a work template that should include a quality check step.</span></span> <span data-ttu-id="bde79-180">在**概览**部分，在**工作模板**字段中，选择 *51 采购订单收据*。</span><span class="sxs-lookup"><span data-stu-id="bde79-180">In the **Overview** section, in the **Work template** field, select *51 PO Receipt*.</span></span>
1. <span data-ttu-id="bde79-181">在**工作模板详细信息**部分，注意此网格有两个现有行：一个是*领料*，一个是*放置*。</span><span class="sxs-lookup"><span data-stu-id="bde79-181">In the **Work template details** section, notice that the grid has two existing lines: one for *Pick* and one for *Put*.</span></span>
1. <span data-ttu-id="bde79-182">在**工作模板详细信息**部分，选择**新建**在网格中为质量控制添加一行。</span><span class="sxs-lookup"><span data-stu-id="bde79-182">In the **Work template details** section, select **New** to add a row for quality control to the grid.</span></span> <span data-ttu-id="bde79-183">注意新行的**行号**字段将设置为 *3*。</span><span class="sxs-lookup"><span data-stu-id="bde79-183">Notice that the **Line number** field for the new line is set to *3*.</span></span>
1. <span data-ttu-id="bde79-184">在新行中，设置以下值。</span><span class="sxs-lookup"><span data-stu-id="bde79-184">On the new line, set the following values.</span></span> <span data-ttu-id="bde79-185">其余字段接受默认值。</span><span class="sxs-lookup"><span data-stu-id="bde79-185">Accept the default values for the remaining fields.</span></span>

    - <span data-ttu-id="bde79-186">**工作类型**：*质量检查*</span><span class="sxs-lookup"><span data-stu-id="bde79-186">**Work type:** *Quality check*</span></span>
    - <span data-ttu-id="bde79-187">**工作类 ID**：*Purchase*</span><span class="sxs-lookup"><span data-stu-id="bde79-187">**Work class ID:** *Purchase*</span></span>
    - <span data-ttu-id="bde79-188">**质量检查模板名称**：*货台检查*</span><span class="sxs-lookup"><span data-stu-id="bde79-188">**Quality check template name:** *Dock check*</span></span>

        <span data-ttu-id="bde79-189">为工作类选择唯一 ID。</span><span class="sxs-lookup"><span data-stu-id="bde79-189">Select the unique ID for the work class.</span></span> <span data-ttu-id="bde79-190">您使用此值配置移动设备上的菜单项和这些菜单项可以处理的工作类型。</span><span class="sxs-lookup"><span data-stu-id="bde79-190">You use this value to configure the menu items on the mobile device and the types of work that those menu items can process.</span></span>

1. <span data-ttu-id="bde79-191">在操作窗格上，选择**保存**保存您到目前为止的工作。</span><span class="sxs-lookup"><span data-stu-id="bde79-191">On the Action Pane, select **Save** to save your work so far.</span></span>

    <span data-ttu-id="bde79-192">您收到一条信息性消息，显示“无效 - 质量检查必须在领料后立即进行。”</span><span class="sxs-lookup"><span data-stu-id="bde79-192">You receive an informational message that states, "Invalid - Quality check must come directly after a pick."</span></span> <span data-ttu-id="bde79-193">因此，您必须为刚添加的行更改**行号**值。</span><span class="sxs-lookup"><span data-stu-id="bde79-193">Therefore, you must change the **Line number** value for the line that you just added.</span></span>

1. <span data-ttu-id="bde79-194">请按照以下步骤更改新行的**行号**值：</span><span class="sxs-lookup"><span data-stu-id="bde79-194">Follow these steps to change the **Line number** value for the new line:</span></span>

    1. <span data-ttu-id="bde79-195">在**工作模板详细信息**部分，选择**工作类型**字段设置为*质量检查*的行。</span><span class="sxs-lookup"><span data-stu-id="bde79-195">In the **Work template details** section, select the line where the **Work type** field is set to *Quality check*.</span></span>
    2. <span data-ttu-id="bde79-196">选择**上移**或**下移**按钮移动*质量检查*行，使其位于*领料*行之后。</span><span class="sxs-lookup"><span data-stu-id="bde79-196">Select the **Move up** or **Move down** button to move the *Quality check* line so that it's after the *Pick* line.</span></span>

1. <span data-ttu-id="bde79-197">在操作窗格上，选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="bde79-197">On the Action Pane, select **Save**.</span></span>

#### <a name="quality-in-quality-check"></a><span data-ttu-id="bde79-198">质量检查中的质量</span><span class="sxs-lookup"><span data-stu-id="bde79-198">Quality in quality check</span></span>

<span data-ttu-id="bde79-199">接下来，创建用于质量检查的工作模板。</span><span class="sxs-lookup"><span data-stu-id="bde79-199">Next, create a work template for the quality check.</span></span>

1. <span data-ttu-id="bde79-200">在**工作模板**页面的标题中，将**工作订单类型**字段的值更改为*质量检查质量*。</span><span class="sxs-lookup"><span data-stu-id="bde79-200">In the header of the **Work templates** page, change the value of the **Work order type** field to *Quality in quality check*.</span></span>
1. <span data-ttu-id="bde79-201">在操作窗格上，选择**新建**向**概览**部分的网格添加一行。</span><span class="sxs-lookup"><span data-stu-id="bde79-201">On the Action Pane, select **New** to add a row to the grid in the **Overview** section.</span></span>
1. <span data-ttu-id="bde79-202">在新行中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="bde79-202">In the new row, set the following values:</span></span>

    - <span data-ttu-id="bde79-203">**工作模板**：*51 质量检查*</span><span class="sxs-lookup"><span data-stu-id="bde79-203">**Work template:** *51 Quality Check*</span></span>

        <span data-ttu-id="bde79-204">输入模板的名称。</span><span class="sxs-lookup"><span data-stu-id="bde79-204">Enter a name for the template.</span></span>

    - <span data-ttu-id="bde79-205">**工作模板描述**：*51 质量检查*</span><span class="sxs-lookup"><span data-stu-id="bde79-205">**Work template description:** *51 Quality Check*</span></span>

1. <span data-ttu-id="bde79-206">在操作窗格上，选择**保存**使**工作模板详细信息**部分可用。</span><span class="sxs-lookup"><span data-stu-id="bde79-206">On the Action Pane, select **Save** to make the **Work template details** section available.</span></span>
1. <span data-ttu-id="bde79-207">在**概览**部分仍然选择新模板时，在**工作模板详细信息**部分选择**新建**向那里的网格添加一行。</span><span class="sxs-lookup"><span data-stu-id="bde79-207">While the new template is still selected in the **Overview** section, select **New** in the **Work template details** section to add a row to the grid there.</span></span>
1. <span data-ttu-id="bde79-208">在新行中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="bde79-208">In the new row, set the following values:</span></span>

    - <span data-ttu-id="bde79-209">**工作类型：** *领料*</span><span class="sxs-lookup"><span data-stu-id="bde79-209">**Work type:** *Pick*</span></span>
    - <span data-ttu-id="bde79-210">**工作类 ID**：*QC Check*</span><span class="sxs-lookup"><span data-stu-id="bde79-210">**Work class ID:** *QC Check*</span></span>

        <span data-ttu-id="bde79-211">选择您先前为质量控制工作创建的[工作类](#work-class)的名称。</span><span class="sxs-lookup"><span data-stu-id="bde79-211">Select the name of the [work class](#work-class) that you created earlier for quality control work.</span></span>

1. <span data-ttu-id="bde79-212">在**工作模板详细信息**部分，再次选择**新建**添加另一行。</span><span class="sxs-lookup"><span data-stu-id="bde79-212">In the **Work template details** section, select **New** again to add another row.</span></span>
1. <span data-ttu-id="bde79-213">在新行中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="bde79-213">In the new row, set the following values:</span></span>

    - <span data-ttu-id="bde79-214">**工作类型：** *放入*</span><span class="sxs-lookup"><span data-stu-id="bde79-214">**Work type:** *Put*</span></span>
    - <span data-ttu-id="bde79-215">**工作类 ID**：*QC Check*</span><span class="sxs-lookup"><span data-stu-id="bde79-215">**Work class ID:** *QC Check*</span></span>

        <span data-ttu-id="bde79-216">选择您先前为质量控制工作创建的[工作类](#work-class)的名称。</span><span class="sxs-lookup"><span data-stu-id="bde79-216">Select the name of the [work class](#work-class) that you created earlier for quality control work.</span></span>

1. <span data-ttu-id="bde79-217">在操作窗格上，选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="bde79-217">On the Action Pane, select **Save**.</span></span>

<span data-ttu-id="bde79-218">有关工作模板的详细信息，请参阅[使用工作模板和位置指令控制仓库工作](control-warehouse-location-directives.md)</span><span class="sxs-lookup"><span data-stu-id="bde79-218">For more information about work templates, see [Control warehouse work by using work templates and location directives](control-warehouse-location-directives.md)</span></span>

### <a name="location-directive--quality-failures"></a><span data-ttu-id="bde79-219">位置指令 – 质检未通过</span><span class="sxs-lookup"><span data-stu-id="bde79-219">Location directive – Quality failures</span></span>

<span data-ttu-id="bde79-220">库位指令是帮助标识领料和使位置用于库存移动的规则。</span><span class="sxs-lookup"><span data-stu-id="bde79-220">Location directives are rules that help identify pick and put locations for inventory movement.</span></span> <span data-ttu-id="bde79-221">例如，在销售订单交易记录中，位置指令决定在何处领取物料，及将领取的物料放置在何处。</span><span class="sxs-lookup"><span data-stu-id="bde79-221">For example, in a sales order transaction, a location directive determines where the items will be picked and where the picked items will be put.</span></span> <span data-ttu-id="bde79-222">您必须配置位置指令规则来定义如何处理未通过的质量检查。</span><span class="sxs-lookup"><span data-stu-id="bde79-222">You must configure a location directive rule to define how failed quality checks will be handled.</span></span>

1. <span data-ttu-id="bde79-223">转到**库存管理 \> 设置 \> 位置指令**。</span><span class="sxs-lookup"><span data-stu-id="bde79-223">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="bde79-224">在左窗格中，将**工作订单类型**字段设置为*采购订单*来使用该类型的位置指令。</span><span class="sxs-lookup"><span data-stu-id="bde79-224">In the left pane, set the **Work order type** field to *Purchase orders* to work with location directives of that type.</span></span>
1. <span data-ttu-id="bde79-225">在操作窗格上，选择**新建**创建用于质量检查的位置指令。</span><span class="sxs-lookup"><span data-stu-id="bde79-225">On the Action Pane, select **New** to create a location directive for quality checks.</span></span>
1. <span data-ttu-id="bde79-226">在标题中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="bde79-226">In the header, set the following values:</span></span>

    - <span data-ttu-id="bde79-227">**序列号：** 接受默认值。</span><span class="sxs-lookup"><span data-stu-id="bde79-227">**Sequence number:** Accept the default value.</span></span>
    - <span data-ttu-id="bde79-228">**名称**：*51 到质量*</span><span class="sxs-lookup"><span data-stu-id="bde79-228">**Name:** *51 To Quality*</span></span>

1. <span data-ttu-id="bde79-229">在**货位指令**快速选项卡上，设置以下值。</span><span class="sxs-lookup"><span data-stu-id="bde79-229">On the **Location directives** FastTab, set the following values.</span></span> <span data-ttu-id="bde79-230">其余字段接受默认值。</span><span class="sxs-lookup"><span data-stu-id="bde79-230">Accept the default values for the remaining fields.</span></span>

    - <span data-ttu-id="bde79-231">**工作类型：** *放入*</span><span class="sxs-lookup"><span data-stu-id="bde79-231">**Work type:** *Put*</span></span>
    - <span data-ttu-id="bde79-232">**站点：** *5*</span><span class="sxs-lookup"><span data-stu-id="bde79-232">**Site:** *5*</span></span>
    - <span data-ttu-id="bde79-233">**仓库：** *51*</span><span class="sxs-lookup"><span data-stu-id="bde79-233">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="bde79-234">在操作窗格上，选择**保存**保存指令，使**行**快速选项卡可用。</span><span class="sxs-lookup"><span data-stu-id="bde79-234">On the Action Pane select **Save** to save your directive and make the **Lines** FastTab available.</span></span>
1. <span data-ttu-id="bde79-235">在**行**快速选项卡上，选择**新建**向网格添加一行。</span><span class="sxs-lookup"><span data-stu-id="bde79-235">On the **Lines** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="bde79-236">在新行中，设置以下值。</span><span class="sxs-lookup"><span data-stu-id="bde79-236">On the new line, set the following values.</span></span> <span data-ttu-id="bde79-237">其余字段接受默认值。</span><span class="sxs-lookup"><span data-stu-id="bde79-237">Accept the default values for the remaining fields.</span></span>

    - <span data-ttu-id="bde79-238">**起始数量：** *1*</span><span class="sxs-lookup"><span data-stu-id="bde79-238">**From quantity:** *1*</span></span>
    - <span data-ttu-id="bde79-239">**目标数量：** *1000000*</span><span class="sxs-lookup"><span data-stu-id="bde79-239">**To quantity:** *1000000*</span></span>

1. <span data-ttu-id="bde79-240">在操作窗格上，选择**保存**保存新行，使**位置指令操作**快速选项卡可用。</span><span class="sxs-lookup"><span data-stu-id="bde79-240">On the Action Pane, select **Save** to save the new line and make the **Location directive actions** FastTab available.</span></span>
1. <span data-ttu-id="bde79-241">当**行**快速选项卡上仍选择新行时，在**位置指令操作**快速选项卡上选择**新建**向那里的网格添加一行，以可以为该行设置操作。</span><span class="sxs-lookup"><span data-stu-id="bde79-241">While the new line is still selected on the **Lines** FastTab, select **New** on the **Location directive actions** FastTab to add a row to the grid there, so that you can set up an action for the line.</span></span>
1. <span data-ttu-id="bde79-242">在新行中，将**名称**字段设置为*质量*。</span><span class="sxs-lookup"><span data-stu-id="bde79-242">In the new row, set the **Name** field to *Quality*.</span></span> <span data-ttu-id="bde79-243">其余字段接受默认值。</span><span class="sxs-lookup"><span data-stu-id="bde79-243">Accept the default values for the remaining fields.</span></span>
1. <span data-ttu-id="bde79-244">在操作窗格上，选择**保存**让**位置指令操作**快速选项卡上的**编辑查询**按钮可用。</span><span class="sxs-lookup"><span data-stu-id="bde79-244">On the Action Pane, select **Save** to make the **Edit query** button on the **Location directive actions** FastTab available.</span></span>
1. <span data-ttu-id="bde79-245">在**位置指令操作**快速选项卡上仍然选择您刚刚添加的行时，选择**编辑查询**打开一个对话框，您可以在其中编辑操作的查询。</span><span class="sxs-lookup"><span data-stu-id="bde79-245">While the line that you just added is still selected on the **Location directive actions** FastTab, select **Edit query** to open a dialog box where you can edit the query for the action.</span></span>
1. <span data-ttu-id="bde79-246">在**范围**选项卡中，选择**添加**向查询添加一行。</span><span class="sxs-lookup"><span data-stu-id="bde79-246">On the **Range** tab, select **Add** to add a row to the query.</span></span>
1. <span data-ttu-id="bde79-247">在新行中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="bde79-247">In the new row, set the following values:</span></span>

    - <span data-ttu-id="bde79-248">**表：** *位置*</span><span class="sxs-lookup"><span data-stu-id="bde79-248">**Table:** *Locations*</span></span>
    - <span data-ttu-id="bde79-249">**派生表**：*货位*</span><span class="sxs-lookup"><span data-stu-id="bde79-249">**Derived table:** *Locations*</span></span>
    - <span data-ttu-id="bde79-250">**字段**：*货位*</span><span class="sxs-lookup"><span data-stu-id="bde79-250">**Field:** *Location*</span></span>
    - <span data-ttu-id="bde79-251">**条件：** *QMS*</span><span class="sxs-lookup"><span data-stu-id="bde79-251">**Criteria:** *QMS*</span></span>

    <span data-ttu-id="bde79-252">*QMS* 位置是质检的仓库位置。</span><span class="sxs-lookup"><span data-stu-id="bde79-252">The *QMS* location is a warehouse location for quality.</span></span>

1. <span data-ttu-id="bde79-253">选择**确定**关闭对话框。</span><span class="sxs-lookup"><span data-stu-id="bde79-253">Select **OK** to close the dialog box.</span></span>
1. <span data-ttu-id="bde79-254">现在，您必须更改仓库 *51* 的采购订单位置指令的顺序。</span><span class="sxs-lookup"><span data-stu-id="bde79-254">You must now change the sequence of purchase order location directives for warehouse *51*.</span></span> <span data-ttu-id="bde79-255">保存新的 *51 到质量*位置指令，刷新页面，然后在列表中选择此位置指令。</span><span class="sxs-lookup"><span data-stu-id="bde79-255">Save the new *51 To Quality* location directive, refresh the page, and select the location directive in the list.</span></span> <span data-ttu-id="bde79-256">然后使用操作窗格上的**上移**和**下移**按钮，按以下顺序放置仓库 *51* 的位置指令。</span><span class="sxs-lookup"><span data-stu-id="bde79-256">Then use the **Move up** and **Move down** buttons on the Action Pane to put the location directive for warehouse *51* in the following order.</span></span> <span data-ttu-id="bde79-257">（选择**上移**或**下移**之前，必须在列表中选择一个位置指令。）</span><span class="sxs-lookup"><span data-stu-id="bde79-257">(Before you select **Move up** or **Move down**, you must select a location directive in the list.)</span></span>

    1. <span data-ttu-id="bde79-258">51 到质量</span><span class="sxs-lookup"><span data-stu-id="bde79-258">51 To Quality</span></span>
    2. <span data-ttu-id="bde79-259">51 采购订单直接</span><span class="sxs-lookup"><span data-stu-id="bde79-259">51 PO Direct</span></span>
    3. <span data-ttu-id="bde79-260">51 QMS</span><span class="sxs-lookup"><span data-stu-id="bde79-260">51 QMS</span></span>

### <a name="mobile-device-menu-items"></a><span data-ttu-id="bde79-261">移动设备菜单项</span><span class="sxs-lookup"><span data-stu-id="bde79-261">Mobile device menu items</span></span>

<span data-ttu-id="bde79-262">配置菜单项，让移动设备可以执行**质量检查**功能。</span><span class="sxs-lookup"><span data-stu-id="bde79-262">Configure a menu item so that mobile devices can perform the **Quality Check** function.</span></span>

#### <a name="purchase-putaway"></a><span data-ttu-id="bde79-263">购买储存</span><span class="sxs-lookup"><span data-stu-id="bde79-263">Purchase putaway</span></span>

1. <span data-ttu-id="bde79-264">转到**仓库管理 \> 设置 \> 移动设备 \> 移动设备菜单项**。</span><span class="sxs-lookup"><span data-stu-id="bde79-264">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="bde79-265">在列表中，选择**购买储存**菜单项。</span><span class="sxs-lookup"><span data-stu-id="bde79-265">In the list, select the **Purchase put-away** menu item.</span></span>
1. <span data-ttu-id="bde79-266">在操作窗格上，选择**编辑**。</span><span class="sxs-lookup"><span data-stu-id="bde79-266">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="bde79-267">在**工作类**部分，选择**新建**向网格添加一行。</span><span class="sxs-lookup"><span data-stu-id="bde79-267">In the **Work classes** section, select **New** to add a row to the grid.</span></span>
1. <span data-ttu-id="bde79-268">在新行中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="bde79-268">In the new row, set the following values:</span></span>

    - <span data-ttu-id="bde79-269">**工作类 ID**：*QC Check*</span><span class="sxs-lookup"><span data-stu-id="bde79-269">**Work class ID:** *QC Check*</span></span>

        <span data-ttu-id="bde79-270">输入您先前为质量控制工作创建的[工作类](#work-class)的名称。</span><span class="sxs-lookup"><span data-stu-id="bde79-270">Enter the name of the [work class](#work-class) that you created earlier for quality control work.</span></span>

    - <span data-ttu-id="bde79-271">**工作订单类型**：*质量检查质量*</span><span class="sxs-lookup"><span data-stu-id="bde79-271">**Work order type:** *Quality in quality check*</span></span>

1. <span data-ttu-id="bde79-272">在操作窗格上，选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="bde79-272">On the Action Pane, select **Save**.</span></span>

#### <a name="purchase-order-line-receiving"></a><span data-ttu-id="bde79-273">采购订单行接收</span><span class="sxs-lookup"><span data-stu-id="bde79-273">Purchase order line receiving</span></span>

1. <span data-ttu-id="bde79-274">转到**仓库管理 \> 设置 \> 移动设备 \> 移动设备菜单项**。</span><span class="sxs-lookup"><span data-stu-id="bde79-274">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="bde79-275">在操作窗格上，选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="bde79-275">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="bde79-276">在标题中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="bde79-276">In the header, set the following values:</span></span>

    - <span data-ttu-id="bde79-277">**菜单项名称**：*PO 行收货*</span><span class="sxs-lookup"><span data-stu-id="bde79-277">**Menu item name:** *PO line receiving*</span></span>
    - <span data-ttu-id="bde79-278">**标题**：*PO 行收货*</span><span class="sxs-lookup"><span data-stu-id="bde79-278">**Title:** *PO line receiving*</span></span>
    - <span data-ttu-id="bde79-279">\**模式：\*\*\*工作*</span><span class="sxs-lookup"><span data-stu-id="bde79-279">**Mode:** *Work*</span></span>
    - <span data-ttu-id="bde79-280">**使用现有工作**：*否*</span><span class="sxs-lookup"><span data-stu-id="bde79-280">**Use existing work:** *No*</span></span>

1. <span data-ttu-id="bde79-281">在**常规**快速选项卡上，设置以下值。</span><span class="sxs-lookup"><span data-stu-id="bde79-281">On the **General** FastTab, set the following values.</span></span> <span data-ttu-id="bde79-282">其余字段接受默认值。</span><span class="sxs-lookup"><span data-stu-id="bde79-282">Accept the default values for the remaining fields.</span></span>

    - <span data-ttu-id="bde79-283">**工作创建流程**：*采购订单行收货和储存*</span><span class="sxs-lookup"><span data-stu-id="bde79-283">**Work creation process:** *Purchase order line receiving and put away*</span></span>
    - <span data-ttu-id="bde79-284">\**生成牌照：\*\*\*是*</span><span class="sxs-lookup"><span data-stu-id="bde79-284">**Generate license plate:** *Yes*</span></span>
    - <span data-ttu-id="bde79-285">**工作模板**：*51 采购订单收据*</span><span class="sxs-lookup"><span data-stu-id="bde79-285">**Work template:** *51 PO Receipt*</span></span>

1. <span data-ttu-id="bde79-286">在操作窗格上，选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="bde79-286">On the Action Pane, select **Save**.</span></span>

#### <a name="add-the-menu-item-to-a-mobile-device-menu"></a><span data-ttu-id="bde79-287">添加菜单项到一个移动设备菜单</span><span class="sxs-lookup"><span data-stu-id="bde79-287">Add the menu item to a mobile device menu</span></span>

1. <span data-ttu-id="bde79-288">转到**仓库管理 \> 设置 \> 移动设备 \> 移动设备菜单**。</span><span class="sxs-lookup"><span data-stu-id="bde79-288">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span>
1. <span data-ttu-id="bde79-289">在左侧窗格中，选择**入站**菜单。</span><span class="sxs-lookup"><span data-stu-id="bde79-289">In the left pane, select the **Inbound** menu.</span></span>
1. <span data-ttu-id="bde79-290">在操作窗格上，选择**编辑**。</span><span class="sxs-lookup"><span data-stu-id="bde79-290">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="bde79-291">在**可用菜单和菜单项**列中，选择新的**采购订单行收货**菜单项。</span><span class="sxs-lookup"><span data-stu-id="bde79-291">In the **Available menus and menu items** column, select the new **PO line receiving** menu item.</span></span>
1. <span data-ttu-id="bde79-292">选择向右箭头按钮，将**采购订单行收货**移至**菜单结构**列。</span><span class="sxs-lookup"><span data-stu-id="bde79-292">Select the right arrow button to move **PO line receiving** to the **Menu structure** column.</span></span>
1. <span data-ttu-id="bde79-293">在**菜单结构**列中，选择**采购订单行收货**，然后选择向上箭头或向下箭头按钮将菜单项移到移动设备菜单上的所需位置。</span><span class="sxs-lookup"><span data-stu-id="bde79-293">In the **Menu structure** column, select **PO line receiving**, and then select the up arrow or down arrow button to move the menu item to the desired position on the mobile device menu.</span></span>
1. <span data-ttu-id="bde79-294">在操作窗格上，选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="bde79-294">On the Action Pane, select **Save**.</span></span>

## <a name="example-scenario"></a><a name="example-scenario"></a><span data-ttu-id="bde79-295">示例场景</span><span class="sxs-lookup"><span data-stu-id="bde79-295">Example scenario</span></span>

<span data-ttu-id="bde79-296">在使所有前面描述的示例数据可用并进行设置之后，您可以演练此方案来试用*质量检查*功能了。</span><span class="sxs-lookup"><span data-stu-id="bde79-296">After you've made all the previously described sample data available and set it up, you can work through this scenario to try out the *Quality check* feature.</span></span> <span data-ttu-id="bde79-297">此方案中显示的值假设您使用的是标准演示数据，选择了 **USMF** 法人，并且您准备了本主题前面介绍的示例记录。</span><span class="sxs-lookup"><span data-stu-id="bde79-297">The values that are shown in this scenario assume that you're working with the standard demo data, that you selected the **USMF** legal entity, and that you prepared the sample records that are described earlier in this topic.</span></span> <span data-ttu-id="bde79-298">此方案还可以用作说明如何在生产设置中使用此功能的示例。</span><span class="sxs-lookup"><span data-stu-id="bde79-298">This scenario also serves as an example that shows how the feature can be used in a production setting.</span></span>

### <a name="create-a-purchase-order"></a><span data-ttu-id="bde79-299">创建采购订单</span><span class="sxs-lookup"><span data-stu-id="bde79-299">Create a purchase order</span></span>

1. <span data-ttu-id="bde79-300">转到**采购 \> 采购订单 \> 所有采购订单**。</span><span class="sxs-lookup"><span data-stu-id="bde79-300">Go to **Procurement and sourcing \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="bde79-301">在操作窗格上，选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="bde79-301">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="bde79-302">在**创建采购订单**对话框中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="bde79-302">In the **Create purchase order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="bde79-303">**供应商帐户**：*104*</span><span class="sxs-lookup"><span data-stu-id="bde79-303">**Vendor account:** *104*</span></span>
    - <span data-ttu-id="bde79-304">**仓库：** *51*</span><span class="sxs-lookup"><span data-stu-id="bde79-304">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="bde79-305">选择**确定**关闭对话框并打开新的采购订单。</span><span class="sxs-lookup"><span data-stu-id="bde79-305">Select **OK** to close the dialog box and open the new purchase order.</span></span>
1. <span data-ttu-id="bde79-306">在**采购订单行**快速选项卡上，网格包含一个新的空白行。</span><span class="sxs-lookup"><span data-stu-id="bde79-306">On the **Purchase order lines** FastTab, the grid contains a new, blank line.</span></span> <span data-ttu-id="bde79-307">在这个行中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="bde79-307">On this line, set the following values:</span></span>

    - <span data-ttu-id="bde79-308">\**物料编号：\*\*\*M9203*</span><span class="sxs-lookup"><span data-stu-id="bde79-308">**Item number:** *M9203*</span></span>
    - <span data-ttu-id="bde79-309">**数量：** *3*</span><span class="sxs-lookup"><span data-stu-id="bde79-309">**Quantity:** *3*</span></span>
    - <span data-ttu-id="bde79-310">**单位**：*PL*</span><span class="sxs-lookup"><span data-stu-id="bde79-310">**Unit:** *PL*</span></span>

1. <span data-ttu-id="bde79-311">在操作窗格上，选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="bde79-311">On the Action Pane, select **Save**.</span></span>

### <a name="process-quality-check-receiving"></a><span data-ttu-id="bde79-312">处理质量检查收货</span><span class="sxs-lookup"><span data-stu-id="bde79-312">Process quality check receiving</span></span>

<span data-ttu-id="bde79-313">创建采购订单后，可以使用**采购订单行收货**菜单项和*质量检查*功能接收采购订单。</span><span class="sxs-lookup"><span data-stu-id="bde79-313">After the purchase order has been created, it can be received by using the **PO line receiving** menu item and the functionality of the *Quality check* feature.</span></span>

#### <a name="receive-pallet-1"></a><span data-ttu-id="bde79-314">接收托盘 1</span><span class="sxs-lookup"><span data-stu-id="bde79-314">Receive pallet 1</span></span>

1. <span data-ttu-id="bde79-315">以仓库 *51* 用户身份登录仓库应用。</span><span class="sxs-lookup"><span data-stu-id="bde79-315">Sign in to the warehouse app as a user for warehouse *51*.</span></span> <span data-ttu-id="bde79-316">（用户 ID 输入 *51*，密码输入 *1*。）</span><span class="sxs-lookup"><span data-stu-id="bde79-316">(Enter *51* as the user ID and *1* as the password.)</span></span>
1. <span data-ttu-id="bde79-317">转到**入站 \> 采购订单行收货**。</span><span class="sxs-lookup"><span data-stu-id="bde79-317">Go to **Inbound \> PO line receiving**.</span></span>
1. <span data-ttu-id="bde79-318">在 **PONUM** 字段中，输入采购订单编号。</span><span class="sxs-lookup"><span data-stu-id="bde79-318">In the **PONUM** field, enter the purchase order number.</span></span>
1. <span data-ttu-id="bde79-319">确认采购订单编号。</span><span class="sxs-lookup"><span data-stu-id="bde79-319">Confirm the purchase order number.</span></span>
1. <span data-ttu-id="bde79-320">在 **LINENUM** 字段中，输入要接收的采购订单行的编号。</span><span class="sxs-lookup"><span data-stu-id="bde79-320">In the **LINENUM** field, enter the number of the purchase order line that is being received.</span></span> <span data-ttu-id="bde79-321">因为在此方案中订单只有一行，所以您将在每个接收步骤的 **LINENUM** 字段中输入 *1*。</span><span class="sxs-lookup"><span data-stu-id="bde79-321">Because the order has only one line in this scenario, you will enter *1* in the **LINENUM** field for each receiving step.</span></span>
1. <span data-ttu-id="bde79-322">确认行号。</span><span class="sxs-lookup"><span data-stu-id="bde79-322">Confirm the line number.</span></span>
1. <span data-ttu-id="bde79-323">在 **QTY** 字段中，输入要接收的数量。</span><span class="sxs-lookup"><span data-stu-id="bde79-323">In the **QTY** field, enter the quantity to receive.</span></span> <span data-ttu-id="bde79-324">因为在此方案中采购订单针对三个托盘 (*PL*)，并且有三个接收步骤，所以您将在每个接收步骤的 **QTY** 字段中输入 *1*。</span><span class="sxs-lookup"><span data-stu-id="bde79-324">Because the purchase order is for three pallets (*PL*) in this scenario, and there are three receiving steps, you will enter *1* in the **QTY** field for each receiving step.</span></span>
1. <span data-ttu-id="bde79-325">确认数量。</span><span class="sxs-lookup"><span data-stu-id="bde79-325">Confirm the quantity.</span></span>

    <span data-ttu-id="bde79-326">出现的**质量检查**页面没有输入字段。</span><span class="sxs-lookup"><span data-stu-id="bde79-326">The **Quality check** page that appears has no entry fields.</span></span> <span data-ttu-id="bde79-327">它只在底部有一个确认（复选标记）按钮，在顶部有一个菜单按钮 (**≡**)。</span><span class="sxs-lookup"><span data-stu-id="bde79-327">It has only the confirmation (check mark) button at the bottom and the Menu button (**≡**) at the top.</span></span> <span data-ttu-id="bde79-328">（菜单按钮有时称为汉堡包或汉堡包按钮。）为了加快质量检查流程，当托盘通过质量检查时，用户只需确认**质量检查**页。</span><span class="sxs-lookup"><span data-stu-id="bde79-328">(The Menu button is sometimes referred to as the hamburger or the hamburger button.) To expedite the quality check process, when the pallet passes the quality check, the user just confirms the **Quality check** page.</span></span>

    <span data-ttu-id="bde79-329">![质量检查页面](media/quality-check.png "质量检查页面")</span><span class="sxs-lookup"><span data-stu-id="bde79-329">![Quality check page](media/quality-check.png "Quality check page")</span></span>

1. <span data-ttu-id="bde79-330">选择确认按钮通过行 1 的托盘 1 的质量检查。</span><span class="sxs-lookup"><span data-stu-id="bde79-330">Select the confirmation button to pass the quality check for pallet 1 from line 1.</span></span>

    <span data-ttu-id="bde79-331">出现的**采购订单：放置**页面将显示放置工作的详细信息：</span><span class="sxs-lookup"><span data-stu-id="bde79-331">The **Purchase orders: Put** page that appears shows details of the put work:</span></span>

    - <span data-ttu-id="bde79-332">**位置：** 系统确定的位置</span><span class="sxs-lookup"><span data-stu-id="bde79-332">**LOC:** The system determined location</span></span>

        <span data-ttu-id="bde79-333">此位置是采购订单接收的指定储存位置。</span><span class="sxs-lookup"><span data-stu-id="bde79-333">This location is the designated putaway location for purchase order receiving.</span></span>

    - <span data-ttu-id="bde79-334">**牌照：** 系统生成的牌照 ID</span><span class="sxs-lookup"><span data-stu-id="bde79-334">**LP:** The system-generated License plate ID</span></span>
    - <span data-ttu-id="bde79-335">\**物料：\*\*\*M9203*</span><span class="sxs-lookup"><span data-stu-id="bde79-335">**Item:** *M9203*</span></span>
    - <span data-ttu-id="bde79-336">**数量**：*1 托盘：100 个*</span><span class="sxs-lookup"><span data-stu-id="bde79-336">**Qty:** *1 PL: 100 ea*</span></span>

    <span data-ttu-id="bde79-337">还会显示物料描述。</span><span class="sxs-lookup"><span data-stu-id="bde79-337">The item description is also shown.</span></span>

1. <span data-ttu-id="bde79-338">确认储存工作。</span><span class="sxs-lookup"><span data-stu-id="bde79-338">Confirm the putaway work.</span></span>

    <span data-ttu-id="bde79-339">在采购订单行接收的**任务**页面上，您将收到“工作已完成”消息。</span><span class="sxs-lookup"><span data-stu-id="bde79-339">On the **Task** page for purchase order line receiving, you receive a "Work Completed" message.</span></span> <span data-ttu-id="bde79-340">**LINENUM** 字段可用，让您可以开始接收下一个托盘。</span><span class="sxs-lookup"><span data-stu-id="bde79-340">The **LINENUM** field is available so that you can start to receive the next pallet.</span></span>

#### <a name="receive-pallet-2"></a><span data-ttu-id="bde79-341">接收托盘 2</span><span class="sxs-lookup"><span data-stu-id="bde79-341">Receive pallet 2</span></span>

<span data-ttu-id="bde79-342">在此方案中，将拒绝托盘 2。</span><span class="sxs-lookup"><span data-stu-id="bde79-342">For this scenario, pallet 2 will be rejected.</span></span>

1. <span data-ttu-id="bde79-343">在 **LINENUM** 字段中，输入 *1*，确认行号。</span><span class="sxs-lookup"><span data-stu-id="bde79-343">In the **LINENUM** field, enter *1*, and confirm the line number.</span></span>
1. <span data-ttu-id="bde79-344">**QTY** 字段现在可用。</span><span class="sxs-lookup"><span data-stu-id="bde79-344">The **QTY** field is now available.</span></span> <span data-ttu-id="bde79-345">输入 *1*，确认数量。</span><span class="sxs-lookup"><span data-stu-id="bde79-345">Enter *1*, and confirm the quantity.</span></span>

    <span data-ttu-id="bde79-346">**质量检查**页面将出现。</span><span class="sxs-lookup"><span data-stu-id="bde79-346">The **Quality check** page appears.</span></span> <span data-ttu-id="bde79-347">对于此接收，托盘将被质检拒绝，并被放入 *QMS* 质检位置。</span><span class="sxs-lookup"><span data-stu-id="bde79-347">For this receipt, the pallet will be rejected for quality, and it will be put into the *QMS* quality location.</span></span>

1. <span data-ttu-id="bde79-348">选择页面顶部的菜单按钮 (**≡**)，然后在菜单上选择**拒绝**。</span><span class="sxs-lookup"><span data-stu-id="bde79-348">Select the Menu button (**≡**) at the top of the page, and then, on the menu, select **Reject**.</span></span>
1. <span data-ttu-id="bde79-349">在出现的**任务**页面上，输入 **QMS** 作为为进一步检查将托盘发送到的*放置*位置。</span><span class="sxs-lookup"><span data-stu-id="bde79-349">On the **Task** page that appears, enter **QMS** as the *Put* location to send the pallet to for further inspection.</span></span>

    <span data-ttu-id="bde79-350">出现的**质量检查质量：放置**页面将显示放置工作的详细信息：</span><span class="sxs-lookup"><span data-stu-id="bde79-350">The **Quality in quality check: Put** page that appears shows details of the put work:</span></span>

    - <span data-ttu-id="bde79-351">**位置**：*QMS*</span><span class="sxs-lookup"><span data-stu-id="bde79-351">**LOC:** *QMS*</span></span>

        <span data-ttu-id="bde79-352">此位置是被拒绝的质量接收的指定储存位置。</span><span class="sxs-lookup"><span data-stu-id="bde79-352">This location is the designated putaway location for rejected quality receiving.</span></span>

    - <span data-ttu-id="bde79-353">**牌照：** 系统生成的牌照 ID</span><span class="sxs-lookup"><span data-stu-id="bde79-353">**LP:** The system-generated License plate ID</span></span>
    - <span data-ttu-id="bde79-354">\**物料：\*\*\*M9203*</span><span class="sxs-lookup"><span data-stu-id="bde79-354">**Item:** *M9203*</span></span>
    - <span data-ttu-id="bde79-355">**数量**：*1 托盘：100 个*</span><span class="sxs-lookup"><span data-stu-id="bde79-355">**Qty:** *1 PL: 100 ea*</span></span>

    <span data-ttu-id="bde79-356">还会显示物料描述。</span><span class="sxs-lookup"><span data-stu-id="bde79-356">The item description is also shown.</span></span>

1. <span data-ttu-id="bde79-357">确认储存工作。</span><span class="sxs-lookup"><span data-stu-id="bde79-357">Confirm the putaway work.</span></span>

    <span data-ttu-id="bde79-358">在采购订单行接收的**任务**页面上，您将收到“工作已完成”消息。</span><span class="sxs-lookup"><span data-stu-id="bde79-358">On the **Task** page for purchase order line receiving, you receive a "Work Completed" message.</span></span> <span data-ttu-id="bde79-359">**LINENUM** 字段可用，让您可以开始接收下一个托盘。</span><span class="sxs-lookup"><span data-stu-id="bde79-359">The **LINENUM** field is available so that you can start to receive the next pallet.</span></span>

<span data-ttu-id="bde79-360">现在，您已经完成了质量检查并为被拒绝的托盘创建了质检订单。</span><span class="sxs-lookup"><span data-stu-id="bde79-360">You've now completed the quality check and created a quality order for the rejected pallet.</span></span> <span data-ttu-id="bde79-361">要查看创建的订单，请转到**库存管理 \> 定期任务 \> 质量管理 \> 质检订单**。</span><span class="sxs-lookup"><span data-stu-id="bde79-361">To view the order that was created, go to **Inventory management \> Periodic tasks \> Quality management \> Quality orders**.</span></span>

<span data-ttu-id="bde79-362">现在可以处理质检订单测试了。</span><span class="sxs-lookup"><span data-stu-id="bde79-362">Quality order testing can now be processed.</span></span> <span data-ttu-id="bde79-363">本主题不包含质检测试。</span><span class="sxs-lookup"><span data-stu-id="bde79-363">Quality testing isn't covered in this topic.</span></span>

<span data-ttu-id="bde79-364">有关质量管理的详细信息，请参阅[质量管理概述](../inventory/enable-quality-management.md)</span><span class="sxs-lookup"><span data-stu-id="bde79-364">For more information about quality management, see [Quality management overview](../inventory/enable-quality-management.md)</span></span>

#### <a name="receive-pallet-3"></a><span data-ttu-id="bde79-365">接收托盘 3</span><span class="sxs-lookup"><span data-stu-id="bde79-365">Receive pallet 3</span></span>

<span data-ttu-id="bde79-366">在此方案中，将接受托盘 3。</span><span class="sxs-lookup"><span data-stu-id="bde79-366">For this scenario, pallet 3 will be accepted.</span></span>

1. <span data-ttu-id="bde79-367">在 **LINENUM** 字段中，输入 *1*，确认行号。</span><span class="sxs-lookup"><span data-stu-id="bde79-367">In the **LINENUM** field, enter *1*, and confirm the line number.</span></span>
1. <span data-ttu-id="bde79-368">**QTY** 字段现在可用。</span><span class="sxs-lookup"><span data-stu-id="bde79-368">The **QTY** field is now available.</span></span> <span data-ttu-id="bde79-369">输入 *1*，确认数量。</span><span class="sxs-lookup"><span data-stu-id="bde79-369">Enter *1*, and confirm the quantity.</span></span>

    <span data-ttu-id="bde79-370">**质量检查**页面将出现。</span><span class="sxs-lookup"><span data-stu-id="bde79-370">The **Quality check** page appears.</span></span> <span data-ttu-id="bde79-371">对于此接收，托盘将被质检接受，并被放入批量储存位置。</span><span class="sxs-lookup"><span data-stu-id="bde79-371">For this receipt, the pallet will be accepted for quality, and it will be put into a bulk putaway location.</span></span>

1. <span data-ttu-id="bde79-372">选择确认按钮通过质量检查。</span><span class="sxs-lookup"><span data-stu-id="bde79-372">Select the confirmation button to pass the quality check.</span></span>

    <span data-ttu-id="bde79-373">出现的**采购订单：放置**页面将显示放置工作的详细信息：</span><span class="sxs-lookup"><span data-stu-id="bde79-373">The **Purchase orders: Put** page that appears shows details of the put work:</span></span>

    - <span data-ttu-id="bde79-374">**位置：** 系统确定的位置</span><span class="sxs-lookup"><span data-stu-id="bde79-374">**LOC:** The system determined location</span></span>

        <span data-ttu-id="bde79-375">此位置是采购订单接收的指定储存位置。</span><span class="sxs-lookup"><span data-stu-id="bde79-375">This location is the designated putaway location for purchase order receiving.</span></span>

    - <span data-ttu-id="bde79-376">**牌照：** 系统生成的牌照 ID</span><span class="sxs-lookup"><span data-stu-id="bde79-376">**LP:** The system-generated License plate ID</span></span>
    - <span data-ttu-id="bde79-377">\**物料：\*\*\*M9203*</span><span class="sxs-lookup"><span data-stu-id="bde79-377">**Item:** *M9203*</span></span>
    - <span data-ttu-id="bde79-378">**数量**：*1 托盘：100 个*</span><span class="sxs-lookup"><span data-stu-id="bde79-378">**Qty:** *1 PL: 100 ea*</span></span>

    <span data-ttu-id="bde79-379">还会显示物料描述。</span><span class="sxs-lookup"><span data-stu-id="bde79-379">The item description is also shown.</span></span>

1. <span data-ttu-id="bde79-380">确认储存工作。</span><span class="sxs-lookup"><span data-stu-id="bde79-380">Confirm the putaway work.</span></span>

    <span data-ttu-id="bde79-381">在采购订单行接收的**任务**页面上，您将收到“工作已完成”消息。</span><span class="sxs-lookup"><span data-stu-id="bde79-381">On the **Task** page for purchase order line receiving, you receive a "Work Completed" message.</span></span> <span data-ttu-id="bde79-382">**LINENUM** 字段可用，让您可以开始接收下一个托盘。</span><span class="sxs-lookup"><span data-stu-id="bde79-382">The **LINENUM** field is available so that you can start to receive the next pallet.</span></span>

1. <span data-ttu-id="bde79-383">选择页面顶部的菜单按钮 (**≡**)，然后在菜单上选择**取消**返回菜单。</span><span class="sxs-lookup"><span data-stu-id="bde79-383">Select the Menu button (**≡**) at the top of the page, and then, on the menu, select **Cancel** to return to the menu.</span></span>

<span data-ttu-id="bde79-384">您现在可以关闭移动应用了。</span><span class="sxs-lookup"><span data-stu-id="bde79-384">You can now close the mobile app.</span></span>
