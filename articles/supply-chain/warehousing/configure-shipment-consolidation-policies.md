---
title: 配置装运合并策略
description: 此主题说明如何设置默认装运合并策略和自定义装运合并策略。
author: GarmMSFT
manager: tfehr
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench, WHSFilterGroupTable, TMSMode, WHSShipmentConsolidation, WHSFilterGenerallyAvail
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: 0d6ab6c034a5c341432f661cf1e729dfd3e5c239
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4996374"
---
# <a name="configure-shipment-consolidation-policies"></a><span data-ttu-id="14e84-103">配置装运合并策略</span><span class="sxs-lookup"><span data-stu-id="14e84-103">Configure shipment consolidation policies</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="14e84-104">在自动和手动发放到仓库期间，可通过使用装运合并策略的装运合并流程自动合并装运。</span><span class="sxs-lookup"><span data-stu-id="14e84-104">The shipment consolidation process that uses shipment consolidation policies allows for automated shipment consolidation during automated and manual release to the warehouse.</span></span> <span data-ttu-id="14e84-105">开启此功能后，必须配置初始策略。</span><span class="sxs-lookup"><span data-stu-id="14e84-105">After you turn on this feature, you must configure your initial policies.</span></span> <span data-ttu-id="14e84-106">如果不配置任何策略，每个销售行将生成有一个装载行的单独装运。</span><span class="sxs-lookup"><span data-stu-id="14e84-106">If no policies are configured, each sales line will generate a separate shipment that has a single load line.</span></span>

<span data-ttu-id="14e84-107">此主题中的方案显示如何设置默认装运合并策略和自定义装运合并策略。</span><span class="sxs-lookup"><span data-stu-id="14e84-107">The scenarios that are presented in this topic show how to set up default and custom shipment consolidation policies.</span></span>

## <a name="turn-on-the-shipment-consolidation-policies-feature"></a><span data-ttu-id="14e84-108">开启装运合并策略功能</span><span class="sxs-lookup"><span data-stu-id="14e84-108">Turn on the Shipment consolidation policies feature</span></span>

> [!IMPORTANT]
> <span data-ttu-id="14e84-109">在此主题中介绍的[第一个方案](#scenario-1)中，首先设置仓库，使其使用之前的装运合并功能。</span><span class="sxs-lookup"><span data-stu-id="14e84-109">In the [first scenario](#scenario-1) that is described in this topic, you will first set up a warehouse so that it uses the earlier shipment consolidation feature.</span></span> <span data-ttu-id="14e84-110">然后启用装运合并策略。</span><span class="sxs-lookup"><span data-stu-id="14e84-110">You will then make shipment consolidation policies available.</span></span> <span data-ttu-id="14e84-111">这样就可以体验升级方案如何工作。</span><span class="sxs-lookup"><span data-stu-id="14e84-111">In this way, you can experience how the upgrade scenario works.</span></span> <span data-ttu-id="14e84-112">如果计划使用演示数据环境完成第一个方案，请勿在使用进行此方案之前开启该功能。</span><span class="sxs-lookup"><span data-stu-id="14e84-112">If you plan to use a demo data environment to go through the first scenario, don't turn on the feature before you do the scenario.</span></span>

<span data-ttu-id="14e84-113">*装运合并策略* 功能必须先在系统中开启，才能使用。</span><span class="sxs-lookup"><span data-stu-id="14e84-113">Before you can use the *Shipment consolidation policies* feature, you must turn it on in your system.</span></span> <span data-ttu-id="14e84-114">管理员可以使用[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)设置检查功能状态和开启功能。</span><span class="sxs-lookup"><span data-stu-id="14e84-114">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="14e84-115">在 **功能管理** 工作区中，此功能按照下面的方式列出：</span><span class="sxs-lookup"><span data-stu-id="14e84-115">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="14e84-116">**模块**：*仓库管理*</span><span class="sxs-lookup"><span data-stu-id="14e84-116">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="14e84-117">**功能名称**：*合并装运*</span><span class="sxs-lookup"><span data-stu-id="14e84-117">**Feature name:** *Consolidate shipment*</span></span>

## <a name="make-demo-data-available"></a><span data-ttu-id="14e84-118">提供演示数据</span><span class="sxs-lookup"><span data-stu-id="14e84-118">Make demo data available</span></span>

<span data-ttu-id="14e84-119">此主题中的每个方案都引用为 Microsoft Dynamics 365 Supply Chain Management 提供的标准演示数据中包含的值和记录。</span><span class="sxs-lookup"><span data-stu-id="14e84-119">Each scenario in this topic references values and records that are included in the standard demo data that is provided for Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="14e84-120">如果要在进行此练习时使用此处提供的值，请务必在安装了演示数据的环境中操作，并且在开始前将法人设置为 **USMF**。</span><span class="sxs-lookup"><span data-stu-id="14e84-120">If you want to use the values that are provided here as you do the exercises, be sure to work in an environment where the demo data is installed, and set the legal entity to **USMF** before you begin.</span></span>

## <a name="scenario-1-configure-default-shipment-consolidation-policies"></a><a name="scenario-1"></a><span data-ttu-id="14e84-121">方案 1：配置默认装运合并策略</span><span class="sxs-lookup"><span data-stu-id="14e84-121">Scenario 1: Configure default shipment consolidation policies</span></span>

<span data-ttu-id="14e84-122">有两种情况必须在开启 *装运合并策略* 功能之后配置最小默认策略数量：</span><span class="sxs-lookup"><span data-stu-id="14e84-122">There are two situations where you must configure the minimum number of default policies after you turn on the *Shipment consolidation policies* feature:</span></span>

- <span data-ttu-id="14e84-123">升级已包含数据的环境。</span><span class="sxs-lookup"><span data-stu-id="14e84-123">You're upgrading an environment that already contains data.</span></span>
- <span data-ttu-id="14e84-124">设置全新环境。</span><span class="sxs-lookup"><span data-stu-id="14e84-124">You're setting up a completely new environment.</span></span>

### <a name="upgrade-an-environment-where-warehouses-are-already-configured-for-cross-order-consolidation"></a><span data-ttu-id="14e84-125">升级已经为跨订单合并配置了仓库的环境</span><span class="sxs-lookup"><span data-stu-id="14e84-125">Upgrade an environment where warehouses are already configured for cross-order consolidation</span></span>

<span data-ttu-id="14e84-126">开始此过程时，应该关闭 *装运合并策略* 功能，以模拟已使用了基本跨订单合并功能的环境。</span><span class="sxs-lookup"><span data-stu-id="14e84-126">When you start this procedure, the *Shipment consolidation policies* feature should be turned off, to simulate an environment where the basic cross-order consolidation feature was already used.</span></span> <span data-ttu-id="14e84-127">然后使用功能管理开启此功能，从而可以了解如何在升级后设置装运合并策略。</span><span class="sxs-lookup"><span data-stu-id="14e84-127">You will then use feature management to turn on the feature, so that you can learn how to set up shipment consolidation policies after the upgrade.</span></span>

<span data-ttu-id="14e84-128">请执行以下步骤在已经为跨订单合并配置了仓库的环境中设置默认装运合并策略。</span><span class="sxs-lookup"><span data-stu-id="14e84-128">Follow these steps to set up default shipment consolidation policies in an environment where warehouses have already been configured for cross-order consolidation.</span></span>

1. <span data-ttu-id="14e84-129">转到 **仓库管理 \> 设置 \> 仓库 \> 仓库**。</span><span class="sxs-lookup"><span data-stu-id="14e84-129">Go to **Warehouse management \> Setup \> Warehouse \> Warehouses**.</span></span>
1. <span data-ttu-id="14e84-130">在列表中，找到并打开所需仓库记录（例如，**USMF** 演示数据中的仓库 *24*）。</span><span class="sxs-lookup"><span data-stu-id="14e84-130">In the list, find and open the desired warehouse record (for example, warehouse *24* in the **USMF** demo data).</span></span>
1. <span data-ttu-id="14e84-131">在操作窗格上，选择 **编辑**。</span><span class="sxs-lookup"><span data-stu-id="14e84-131">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="14e84-132">在 **仓库** 快速选项卡上，将 **在发放到仓库时合并装运** 选项设置为 *是*。</span><span class="sxs-lookup"><span data-stu-id="14e84-132">On the **Warehouse** FastTab, set the **Consolidate shipment at release to warehouse** option to *Yes*.</span></span>
1. <span data-ttu-id="14e84-133">对需要进行合并的其他所有仓库重复步骤 2 到 4。</span><span class="sxs-lookup"><span data-stu-id="14e84-133">Repeat steps 2 through 4 for all other warehouses where consolidation is required.</span></span>
1. <span data-ttu-id="14e84-134">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="14e84-134">Close the page.</span></span>
1. <span data-ttu-id="14e84-135">使用 [功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)开启 *装运合并策略* 功能。</span><span class="sxs-lookup"><span data-stu-id="14e84-135">Use [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) to turn on the *Shipment consolidation policies* feature.</span></span> <span data-ttu-id="14e84-136">在 **功能管理** 工作区中，此功能的名称为 *合并装运*。</span><span class="sxs-lookup"><span data-stu-id="14e84-136">In the **Feature management** workspace, the feature is named *Consolidate shipment*.</span></span>
1. <span data-ttu-id="14e84-137">转到 **仓库管理 \> 设置 \> 发放到仓库 \> 装运合并策略**。</span><span class="sxs-lookup"><span data-stu-id="14e84-137">Go to **Warehouse management \> Setup \> Release to warehouse \> Shipment consolidation policies**.</span></span> <span data-ttu-id="14e84-138">开启此功能之后，可能必须刷新浏览器才能查看新的 **装运合并策略** 菜单项。</span><span class="sxs-lookup"><span data-stu-id="14e84-138">You might have to refresh your browser to see the new **Shipment consolidation policies** menu item after you turn on the feature.</span></span>
1. <span data-ttu-id="14e84-139">在操作窗格上，选择 **创建默认设置** 创建以下策略：</span><span class="sxs-lookup"><span data-stu-id="14e84-139">On the Action Pane, select **Create default setup** to create the following policies:</span></span>

    - <span data-ttu-id="14e84-140">适用于 *销售订单* 策略类型的 **CrossOrder** 策略（前提是您有至少一个仓库设置为使用前面的合并功能）</span><span class="sxs-lookup"><span data-stu-id="14e84-140">A **CrossOrder** policy for the *Sales orders* policy type (provided that you have at least one warehouse that is set up to use the earlier consolidation feature)</span></span>
    - <span data-ttu-id="14e84-141">适用于 *销售订单* 策略类型的 **默认** 策略</span><span class="sxs-lookup"><span data-stu-id="14e84-141">A **Default** policy for the *Sales orders* policy type</span></span>
    - <span data-ttu-id="14e84-142">适用于 *转移问题* 策略类型的 **默认** 策略</span><span class="sxs-lookup"><span data-stu-id="14e84-142">A **Default** policy for the *Transfer issue* policy type</span></span>
    - <span data-ttu-id="14e84-143">适用于 *转移问题* 策略类型的 **CrossOrder** 策略（前提是您有至少一个仓库设置为使用前面的合并功能）</span><span class="sxs-lookup"><span data-stu-id="14e84-143">A **CrossOrder** policy for the *Transfer issue* policy type (provided you have at least one warehouse that is set up to use the earlier consolidation feature)</span></span>

    > [!NOTE]
    > - <span data-ttu-id="14e84-144">两种 **CrossOrder** 策略都将同一组字段视为之前的逻辑，但订单编号的字段除外。</span><span class="sxs-lookup"><span data-stu-id="14e84-144">Both **CrossOrder** policies consider the same set of fields as the earlier logic, except for the field for the order number.</span></span> <span data-ttu-id="14e84-145">（此字段用于根据仓库、交装运输方式和地址等元素将行合并为装运。）</span><span class="sxs-lookup"><span data-stu-id="14e84-145">(That field is used to consolidate lines into shipments, based on factors such as the warehouse, transportation mode of delivery, and address.)</span></span>
    > - <span data-ttu-id="14e84-146">两种 **默认** 策略都将同一组字段视为之前的逻辑，包括订单编号的字段。</span><span class="sxs-lookup"><span data-stu-id="14e84-146">Both **Default** policies consider the same set of fields as the earlier logic, including the field for the order number.</span></span> <span data-ttu-id="14e84-147">（此字段用于根据订单编号、仓库、交货的运输方式和地址等元素将行合并为装运。）</span><span class="sxs-lookup"><span data-stu-id="14e84-147">(That field is used to consolidate lines into shipments, based on factors such as the order number, warehouse, transportation mode of delivery, and address.)</span></span>

1. <span data-ttu-id="14e84-148">为 *销售订单* 策略类型选择 **CrossOrder**，然后在操作窗格上选择 **编辑查询**。</span><span class="sxs-lookup"><span data-stu-id="14e84-148">Select the **CrossOrder** policy for the *Sales orders* policy type, and then, on the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="14e84-149">请注意，查询编辑器对话框中列出了其 **在发放到仓库时合并装运** 选项设置为 *是* 的仓库。</span><span class="sxs-lookup"><span data-stu-id="14e84-149">In the query editor dialog box, notice that warehouses where the **Consolidate shipment at release to warehouse** option is set to *Yes* are listed.</span></span> <span data-ttu-id="14e84-150">因此，查询中包含它们。</span><span class="sxs-lookup"><span data-stu-id="14e84-150">Therefore, they are included in the query.</span></span>

### <a name="create-default-policies-for-a-new-environment"></a><span data-ttu-id="14e84-151">为新环境创建默认策略</span><span class="sxs-lookup"><span data-stu-id="14e84-151">Create default policies for a new environment</span></span>

<span data-ttu-id="14e84-152">请执行以下步骤在全新环境中设置默认装运合并策略。</span><span class="sxs-lookup"><span data-stu-id="14e84-152">Follow these steps to set up default shipment consolidation policies in a brand-new environment.</span></span>

1. <span data-ttu-id="14e84-153">如果尚未开启 *装运合并策略* 功能，请使用[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)开启此功能。</span><span class="sxs-lookup"><span data-stu-id="14e84-153">Use [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) to turn on the *Shipment consolidation policies* feature, if you haven't already turned it on.</span></span> <span data-ttu-id="14e84-154">在 **功能管理** 工作区中，此功能的名称为 *合并装运*。</span><span class="sxs-lookup"><span data-stu-id="14e84-154">In the **Feature management** workspace, the feature is named *Consolidate shipment*.</span></span>
1. <span data-ttu-id="14e84-155">转到 **仓库管理 \> 设置 \> 发放到仓库 \> 装运合并策略**。</span><span class="sxs-lookup"><span data-stu-id="14e84-155">Go to **Warehouse management \> Setup \> Release to warehouse \> Shipment consolidation policies**.</span></span>
1. <span data-ttu-id="14e84-156">在操作窗格上，选择 **创建默认设置** 创建以下策略：</span><span class="sxs-lookup"><span data-stu-id="14e84-156">On the Action Pane, select **Create default setup** to create the following policies:</span></span>

    - <span data-ttu-id="14e84-157">适用于 *销售订单* 策略类型的 **默认** 策略</span><span class="sxs-lookup"><span data-stu-id="14e84-157">A **Default** policy for the *Sales orders* policy type</span></span>
    - <span data-ttu-id="14e84-158">适用于 *转移问题* 策略类型的 **默认** 策略</span><span class="sxs-lookup"><span data-stu-id="14e84-158">A **Default** policy for the *Transfer issue* policy type</span></span>

    > [!NOTE]
    > <span data-ttu-id="14e84-159">两种 **默认** 策略都将同一组字段视为之前的逻辑，包括订单编号的字段。</span><span class="sxs-lookup"><span data-stu-id="14e84-159">Both **Default** policies consider the same set of fields as the earlier logic, including the field for the order number.</span></span> <span data-ttu-id="14e84-160">（此字段用于根据订单编号、仓库、交货的运输方式和地址等元素将行合并为装运。）</span><span class="sxs-lookup"><span data-stu-id="14e84-160">(That field is used to consolidate lines into shipments, based on factors such as the order number, warehouse, transportation mode of delivery, and address.)</span></span>

## <a name="scenario-2-configure-custom-shipment-consolidation-policies"></a><span data-ttu-id="14e84-161">方案 2：配置自定义装运合并策略</span><span class="sxs-lookup"><span data-stu-id="14e84-161">Scenario 2: Configure custom shipment consolidation policies</span></span>

<span data-ttu-id="14e84-162">此业务情景显示了如何设置自定义装运合并策略。</span><span class="sxs-lookup"><span data-stu-id="14e84-162">This scenario shows how to set up custom shipment consolidation policies.</span></span> <span data-ttu-id="14e84-163">自定义策略可以支持装运合并取决于多个条件的复杂业务要求。</span><span class="sxs-lookup"><span data-stu-id="14e84-163">Custom policies can support complex business requirements where shipment consolidation depends on several conditions.</span></span> <span data-ttu-id="14e84-164">此方案中后面的每个示例策略中包含业务案例的简短说明。</span><span class="sxs-lookup"><span data-stu-id="14e84-164">For each example policy later in this scenario, a short description of the business case is included.</span></span> <span data-ttu-id="14e84-165">应该按照可确保金字塔式评估查询的顺序设置这些示例策略。</span><span class="sxs-lookup"><span data-stu-id="14e84-165">These example policies should be set up in a sequence that ensures a pyramid-like evaluation of the queries.</span></span> <span data-ttu-id="14e84-166">（换句话说，应该将条件最多的策略作为优先级最高进行评估。）</span><span class="sxs-lookup"><span data-stu-id="14e84-166">(In other words, the policies that have the most conditions should be evaluated as having the highest priority.)</span></span>

### <a name="turn-on-the-feature-and-prepare-master-data-for-this-scenario"></a><span data-ttu-id="14e84-167">为此方案开启此功能和准备主数据</span><span class="sxs-lookup"><span data-stu-id="14e84-167">Turn on the feature and prepare master data for this scenario</span></span>

<span data-ttu-id="14e84-168">必须先按照下面的小节中的说明开启此功能并准备执行筛选所需主数据，然后才能完成此方案中的练习。</span><span class="sxs-lookup"><span data-stu-id="14e84-168">Before you can go through the exercises in this scenario, you must turn on the feature and prepare the master data that is required to do the filtering, as described in the following subsections.</span></span> <span data-ttu-id="14e84-169">（这些先决条件也适用于[有关如何使用装运合并策略的示例方案](#example-scenarios)中列出的方案。）</span><span class="sxs-lookup"><span data-stu-id="14e84-169">(These prerequisites also apply to the scenarios listed in [Example scenarios of how to use shipment consolidation policies](#example-scenarios).)</span></span>

#### <a name="turn-on-the-feature-and-create-the-default-policies"></a><span data-ttu-id="14e84-170">开启功能和创建默认策略</span><span class="sxs-lookup"><span data-stu-id="14e84-170">Turn on the feature and create the default policies</span></span>

<span data-ttu-id="14e84-171">如果尚未开启此功能，请使用功能管理开启，然后创建[方案 1](#scenario-1) 中介绍的默认合并策略。</span><span class="sxs-lookup"><span data-stu-id="14e84-171">Use feature management to turn on the feature, if you haven't already turned it on, and create the default consolidation polices that are described in [scenario 1](#scenario-1).</span></span>

#### <a name="create-two-new-product-filter-codes"></a><span data-ttu-id="14e84-172">创建两个新产品筛选器代码</span><span class="sxs-lookup"><span data-stu-id="14e84-172">Create two new product filter codes</span></span>

1. <span data-ttu-id="14e84-173">转到 **仓库管理 \> 设置 \> 产品筛选器 \> 产品筛选器**，然后添加两个产品筛选器：</span><span class="sxs-lookup"><span data-stu-id="14e84-173">Go to **Warehouse management \> Setup \> Product filters \> Product filters**, and add two product filters:</span></span>

    - <span data-ttu-id="14e84-174">产品筛选器 1：</span><span class="sxs-lookup"><span data-stu-id="14e84-174">Product filter 1:</span></span>

        - <span data-ttu-id="14e84-175">**过滤器代码**：*易燃*</span><span class="sxs-lookup"><span data-stu-id="14e84-175">**Filter code:** *Flammable*</span></span>
        - <span data-ttu-id="14e84-176">**过滤器标题**：*代码 4*</span><span class="sxs-lookup"><span data-stu-id="14e84-176">**Filter title:** *Code 4*</span></span>

    - <span data-ttu-id="14e84-177">产品筛选器 2：</span><span class="sxs-lookup"><span data-stu-id="14e84-177">Product filter 2:</span></span>

        - <span data-ttu-id="14e84-178">**过滤器代码**：*易爆*</span><span class="sxs-lookup"><span data-stu-id="14e84-178">**Filter code:** *Explosive*</span></span>
        - <span data-ttu-id="14e84-179">**过滤器标题**：*代码 4*</span><span class="sxs-lookup"><span data-stu-id="14e84-179">**Filter title:** *Code 4*</span></span>

1. <span data-ttu-id="14e84-180">转到 **产品信息管理 \> 产品 \> 已发布产品**。</span><span class="sxs-lookup"><span data-stu-id="14e84-180">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="14e84-181">打开物料编号为 *M9200* 的产品。</span><span class="sxs-lookup"><span data-stu-id="14e84-181">Open the product that has item number *M9200*.</span></span> <span data-ttu-id="14e84-182">（必须为高级仓库 \[WMS\] 流程启用所选产品，而 **USMF** 演示数据中则已为 WMS 流程预先启用了此产品。）</span><span class="sxs-lookup"><span data-stu-id="14e84-182">(The product that you select must be enabled for advanced warehouse \[WMS\] processes, and this product is pre-enabled for WMS processes in the **USMF** demo data.)</span></span>
1. <span data-ttu-id="14e84-183">在 **仓库** 快速选项卡上，将 **代码 4** 字段设置为 *易燃*。</span><span class="sxs-lookup"><span data-stu-id="14e84-183">On the **Warehouse** FastTab, set the **Code 4** field to *Flammable*.</span></span>
1. <span data-ttu-id="14e84-184">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="14e84-184">Close the page.</span></span>
1. <span data-ttu-id="14e84-185">打开物料编号为 *M9201* 的产品。</span><span class="sxs-lookup"><span data-stu-id="14e84-185">Open the product that has item number *M9201*.</span></span> <span data-ttu-id="14e84-186">（已在 **USMF** 演示数据中为 WMS 流程预先启用了此产品。）</span><span class="sxs-lookup"><span data-stu-id="14e84-186">(This product is also pre-enabled for WMS processes in the in the **USMF** demo data.)</span></span>
1. <span data-ttu-id="14e84-187">在 **仓库** 快速选项卡上，将 **代码 4** 字段设置为 *易爆*。</span><span class="sxs-lookup"><span data-stu-id="14e84-187">On the **Warehouse** FastTab, set the **Code 4** field to *Explosive*.</span></span>
1. <span data-ttu-id="14e84-188">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="14e84-188">Close the page.</span></span>

#### <a name="create-a-new-transportation-mode-of-delivery"></a><span data-ttu-id="14e84-189">创建新交装运输方式</span><span class="sxs-lookup"><span data-stu-id="14e84-189">Create a new transportation mode of delivery</span></span>

1. <span data-ttu-id="14e84-190">转到 **运输管理 \> 设置 \> 承运人 \> 方式**。</span><span class="sxs-lookup"><span data-stu-id="14e84-190">Go to **Transportation management \> Setup \> Carriers \> Mode**.</span></span>
1. <span data-ttu-id="14e84-191">创建合并查询中将使用的运输方式，然后将其命名为 *航空公司*。</span><span class="sxs-lookup"><span data-stu-id="14e84-191">Create a transportation mode that will be used in consolidation queries, and name it *Airways*.</span></span>
1. <span data-ttu-id="14e84-192">转到 **运输管理 \> 设置 \> 承运人 \> 装运承运人**。</span><span class="sxs-lookup"><span data-stu-id="14e84-192">Go to **Transportation management \> Setup \> Carriers \> Shipping carriers**.</span></span>
1. <span data-ttu-id="14e84-193">创建具有以下设置的承运人：</span><span class="sxs-lookup"><span data-stu-id="14e84-193">Create a carrier that has the following settings:</span></span>

    - <span data-ttu-id="14e84-194">**装运承运人**：*航空公司*</span><span class="sxs-lookup"><span data-stu-id="14e84-194">**Shipping carrier:** *Airways*</span></span>
    - <span data-ttu-id="14e84-195">**名称**：*航空公司*</span><span class="sxs-lookup"><span data-stu-id="14e84-195">**Name:** *Airways*</span></span>
    - <span data-ttu-id="14e84-196">**模式**：*航空公司*</span><span class="sxs-lookup"><span data-stu-id="14e84-196">**Mode:** *Airways*</span></span>

1. <span data-ttu-id="14e84-197">在新承运人的 **服务** 快速选项卡上，添加一个具有以下设置的行：</span><span class="sxs-lookup"><span data-stu-id="14e84-197">On the **Services** FastTab for the new carrier, add a row that has the following settings:</span></span>

    - <span data-ttu-id="14e84-198">**承运人服务**：*航运*</span><span class="sxs-lookup"><span data-stu-id="14e84-198">**Carrier service:** *Air*</span></span>
    - <span data-ttu-id="14e84-199">**运输方式**：*航运*</span><span class="sxs-lookup"><span data-stu-id="14e84-199">**Transportation method:** *Air*</span></span>

1. <span data-ttu-id="14e84-200">在操作窗格上，选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="14e84-200">On the Action Pane, select **Save**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="14e84-201">保存新承运人时，**服务** 网格中新行的 **交货方式** 字段将自动设置为 *航空公司-航运*。</span><span class="sxs-lookup"><span data-stu-id="14e84-201">When you save the new carrier, the **Mode of delivery** field for the new row in the **Services** grid is automatically set to *Airwa-Air*.</span></span> <span data-ttu-id="14e84-202">为销售订单使用 *航空公司-航运* 交货方式时，将为相关装运使用 *航空公司* 运输方式。</span><span class="sxs-lookup"><span data-stu-id="14e84-202">When you use the *Airwa-Air* mode of delivery for a sales order, the *Airways* transportation mode will be used for related shipments.</span></span>

#### <a name="create-an-order-pool"></a><span data-ttu-id="14e84-203">创建订单池</span><span class="sxs-lookup"><span data-stu-id="14e84-203">Create an order pool</span></span>

1. <span data-ttu-id="14e84-204">转到 **销售和营销 \> 设置 \> 销售订单 \> 订单池**。</span><span class="sxs-lookup"><span data-stu-id="14e84-204">Go to **Sales and marketing \> Setup \> Sales orders \> Order pools**.</span></span>
1. <span data-ttu-id="14e84-205">创建将用于合并查询的订单池。</span><span class="sxs-lookup"><span data-stu-id="14e84-205">Create an order pool that will be used for the consolidation query.</span></span> <span data-ttu-id="14e84-206">此订单池将具有以下设置：</span><span class="sxs-lookup"><span data-stu-id="14e84-206">This order pool should have the following settings:</span></span>

    - <span data-ttu-id="14e84-207">**池：** 输入其他任何池尚未使用的整数。</span><span class="sxs-lookup"><span data-stu-id="14e84-207">**Pool:** Enter an integer that isn't already used by any other pool.</span></span>
    - <span data-ttu-id="14e84-208">**名称**：*ShipCons*</span><span class="sxs-lookup"><span data-stu-id="14e84-208">**Name:** *ShipCons*</span></span>

1. <span data-ttu-id="14e84-209">转到 **销售和市场营销 \> 客户 \> 所有客户**。</span><span class="sxs-lookup"><span data-stu-id="14e84-209">Go to **Sales and marketing \> Customers \> All customers**.</span></span>
1. <span data-ttu-id="14e84-210">打开客户编号为 *US-003* 的客户。</span><span class="sxs-lookup"><span data-stu-id="14e84-210">Open the customer that has account number *US-003*.</span></span>
1. <span data-ttu-id="14e84-211">在 **销售订单默认值** 快速选项卡上，将 **销售订单池** 字段设置为刚才创建的订单池。</span><span class="sxs-lookup"><span data-stu-id="14e84-211">On the **Sales order defaults** FastTab, set the **Sales order pool** field to the order pool that you just created.</span></span>
1. <span data-ttu-id="14e84-212">关闭页面，然后为帐户编号为 *US-004* 的客户重复步骤 4 和 5。</span><span class="sxs-lookup"><span data-stu-id="14e84-212">Close the page, and then repeat the steps 4 and 5 for the customer that has account number *US-004*.</span></span>

### <a name="create-example-policy-1"></a><span data-ttu-id="14e84-213">创建示例策略 1</span><span class="sxs-lookup"><span data-stu-id="14e84-213">Create example policy 1</span></span>

<span data-ttu-id="14e84-214">在此示例中，将创建可用于以下业务案例的 *客户 + 方式* 策略。</span><span class="sxs-lookup"><span data-stu-id="14e84-214">In this example, you will create a *Customer+Mode* policy that can be used for the following business case:</span></span>

- <span data-ttu-id="14e84-215">此策略将查询特定客户帐户 (*US-001*) 和特定交货方式（*航空公司-航运*）。</span><span class="sxs-lookup"><span data-stu-id="14e84-215">The policy will query for a specific customer account (*US-001*) and a specific mode of delivery (*Airwa-Air*).</span></span>
- <span data-ttu-id="14e84-216">已关闭与未结装运合并。</span><span class="sxs-lookup"><span data-stu-id="14e84-216">Consolidation with open shipments is turned off.</span></span>
- <span data-ttu-id="14e84-217">合并按订单 ID 进行。</span><span class="sxs-lookup"><span data-stu-id="14e84-217">Consolidation is done per order ID.</span></span> <span data-ttu-id="14e84-218">（换句话说，每个订单、仓库等都将有单独的装运。）</span><span class="sxs-lookup"><span data-stu-id="14e84-218">(In other words, there will be separate shipments per order, warehouse, and so on.)</span></span>

<span data-ttu-id="14e84-219">执行以下步骤为此业务案例创建装运合并策略。</span><span class="sxs-lookup"><span data-stu-id="14e84-219">Follow these steps to create the shipment consolidation policy for this business case.</span></span>

1. <span data-ttu-id="14e84-220">转到 **仓库管理 \> 设置 \> 发放到仓库 \> 装运合并策略**。</span><span class="sxs-lookup"><span data-stu-id="14e84-220">Go to **Warehouse management \> Setup \> Release to warehouse \> Shipment consolidation policies**.</span></span>
1. <span data-ttu-id="14e84-221">将 **策略类型** 字段设置为 *销售订单*。</span><span class="sxs-lookup"><span data-stu-id="14e84-221">Set the **Policy type** field to *Sales orders*.</span></span>
1. <span data-ttu-id="14e84-222">在操作窗格上，选择 **新建** 创建具有以下设置的策略：</span><span class="sxs-lookup"><span data-stu-id="14e84-222">On the Action Pane, select **New** to create a policy that has the following settings:</span></span>

    - <span data-ttu-id="14e84-223">**策略名称**：*CustomerMode*</span><span class="sxs-lookup"><span data-stu-id="14e84-223">**Policy name:** *CustomerMode*</span></span>
    - <span data-ttu-id="14e84-224">**策略说明**：*客户帐户和交货方式*</span><span class="sxs-lookup"><span data-stu-id="14e84-224">**Policy description:** *Customer account and mode of delivery*</span></span>

1. <span data-ttu-id="14e84-225">让 **与未结装运合并** 选项继续设置为 *否*。</span><span class="sxs-lookup"><span data-stu-id="14e84-225">Leave the **Consolidate with open shipments** option set to *No*.</span></span>
1. <span data-ttu-id="14e84-226">在操作窗格上，选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="14e84-226">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="14e84-227">在 **合并字段** 快速选项卡上 **其余字段** 列表中，选择其中的 **字段名称** 字段设置为 *交货方式* 的行。</span><span class="sxs-lookup"><span data-stu-id="14e84-227">On the **Consolidation fields** FastTab, in the **Remaining fields** list, select the row where the **Field name** field is set to *Mode of delivery*.</span></span>
1. <span data-ttu-id="14e84-228">选择 **添加** 按钮 ![向右箭头](media/forward-button.png) 将字段移到 **所选字段** 列表中。</span><span class="sxs-lookup"><span data-stu-id="14e84-228">Select the **Add** button ![Right arrow](media/forward-button.png) to move the field to the **Selected fields** list.</span></span>
1. <span data-ttu-id="14e84-229">在操作窗格上，选择 **编辑查询**。</span><span class="sxs-lookup"><span data-stu-id="14e84-229">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="14e84-230">在查询编辑器对话框中 **范围** 选项卡上网格内，找到其中的 **字段** 字段设置为 *客户帐户* 的行，然后将该行的 **条件** 字段设置为 *US-001*。</span><span class="sxs-lookup"><span data-stu-id="14e84-230">In the query editor dialog box, on the **Range** tab, in the grid, find the row where the **Field** field is set to *Customer account*, and set the **Criteria** field for that row to *US-001*.</span></span>
1. <span data-ttu-id="14e84-231">选择 **添加** 向网格添加具有以下设置的行：</span><span class="sxs-lookup"><span data-stu-id="14e84-231">Select **Add** to add a row that has the following settings to the grid:</span></span>

    - <span data-ttu-id="14e84-232">**表**：*订单行*</span><span class="sxs-lookup"><span data-stu-id="14e84-232">**Table:** *Order lines*</span></span>
    - <span data-ttu-id="14e84-233">**派生表**：*订单行*</span><span class="sxs-lookup"><span data-stu-id="14e84-233">**Derived table:** *Order lines*</span></span>
    - <span data-ttu-id="14e84-234">**字段**：*交货方式*</span><span class="sxs-lookup"><span data-stu-id="14e84-234">**Field:** *Mode of delivery*</span></span>
    - <span data-ttu-id="14e84-235">**条件**：*航空公司-航运*</span><span class="sxs-lookup"><span data-stu-id="14e84-235">**Criteria:** *Airwa-Air*</span></span>

1. <span data-ttu-id="14e84-236">选择 **确定** 关闭对话框。</span><span class="sxs-lookup"><span data-stu-id="14e84-236">Select **OK** to close the dialog box.</span></span>

> [!NOTE]
> <span data-ttu-id="14e84-237">对于此业务案例，将不合并多个订单的使用 *航空公司-航运* 交货方式的客户 *US-001* 的订单行。</span><span class="sxs-lookup"><span data-stu-id="14e84-237">For this business case, order lines for customer *US-001* that use the *Airwa-Air* mode of delivery won't be consolidated across orders.</span></span> <span data-ttu-id="14e84-238">如果为此客户合并其他所有交货方式的装运，应该首先在序列中使用此策略。</span><span class="sxs-lookup"><span data-stu-id="14e84-238">This policy is intended to be used first in a sequence, in cases where shipments for all other modes of delivery are consolidated for this customer.</span></span>

### <a name="create-example-policy-2"></a><span data-ttu-id="14e84-239">创建示例策略 2</span><span class="sxs-lookup"><span data-stu-id="14e84-239">Create example policy 2</span></span>

<span data-ttu-id="14e84-240">在此示例中，将创建可用于以下业务案例的 *危险货物* 策略。</span><span class="sxs-lookup"><span data-stu-id="14e84-240">In this example, you will create a *Hazardous goods* policy that can be used for the following business case:</span></span>

- <span data-ttu-id="14e84-241">此策略将查询特定筛选器代码（*危险*）和特定交货方式（*航空公司-航运*）。</span><span class="sxs-lookup"><span data-stu-id="14e84-241">The policy will query for a specific filter code (*hazardous*) and a specific mode of delivery (*Airwa-Air*).</span></span>
- <span data-ttu-id="14e84-242">已开启与未结装运合并。</span><span class="sxs-lookup"><span data-stu-id="14e84-242">Consolidation with open shipments is turned on.</span></span>
- <span data-ttu-id="14e84-243">将跨订单进行合并。</span><span class="sxs-lookup"><span data-stu-id="14e84-243">Consolidation is done across orders.</span></span> <span data-ttu-id="14e84-244">（换句话说，每个帐户、仓库等有单独的装运，但是只在查询中指定的物料组内。）</span><span class="sxs-lookup"><span data-stu-id="14e84-244">(In other words, there will be separate shipments per account, warehouse, and so on, but only within the item group that is specified in the query.)</span></span>

<span data-ttu-id="14e84-245">执行以下步骤为此业务案例创建装运合并策略。</span><span class="sxs-lookup"><span data-stu-id="14e84-245">Follow these steps to create the shipment consolidation policy for this business case.</span></span>

1. <span data-ttu-id="14e84-246">转到 **仓库管理 \> 设置 \> 发放到仓库 \> 装运合并策略**。</span><span class="sxs-lookup"><span data-stu-id="14e84-246">Go to **Warehouse management \> Setup \> Release to warehouse \> Shipment consolidation policies**.</span></span>
1. <span data-ttu-id="14e84-247">将 **策略类型** 字段设置为 *销售订单*。</span><span class="sxs-lookup"><span data-stu-id="14e84-247">Set the **Policy type** field to *Sales orders*.</span></span>
1. <span data-ttu-id="14e84-248">在操作窗格上，选择 **新建** 创建具有以下设置的策略：</span><span class="sxs-lookup"><span data-stu-id="14e84-248">On the Action Pane, select **New** to create a policy that has the following settings:</span></span>

    - <span data-ttu-id="14e84-249">**策略名称**：*物料类型*</span><span class="sxs-lookup"><span data-stu-id="14e84-249">**Policy name:** *Item type*</span></span>
    - <span data-ttu-id="14e84-250">**策略说明**：*跨订单合并类型相同的物料*</span><span class="sxs-lookup"><span data-stu-id="14e84-250">**Policy description:** *Consolidate the same type of item across orders*</span></span>

1. <span data-ttu-id="14e84-251">将 **与未结装运合并** 选项设置为 *是*。</span><span class="sxs-lookup"><span data-stu-id="14e84-251">Set the **Consolidate with open shipments** option to *Yes*.</span></span>
1. <span data-ttu-id="14e84-252">在操作窗格上，选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="14e84-252">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="14e84-253">在 **合并字段** 快速选项卡上 **其余字段** 列表中，选择其中的 **字段名称** 字段设置为 *交货方式* 的行。</span><span class="sxs-lookup"><span data-stu-id="14e84-253">On the **Consolidation fields** FastTab, in the **Remaining fields** list, select the row where the **Field name** field is set to *Mode of delivery*.</span></span>
1. <span data-ttu-id="14e84-254">选择 **添加** 按钮 ![向右箭头](media/forward-button.png) 将字段移到 **所选字段** 列表中。</span><span class="sxs-lookup"><span data-stu-id="14e84-254">Select the **Add** button ![Right arrow](media/forward-button.png) to move the field to the **Selected fields** list.</span></span>
1. <span data-ttu-id="14e84-255">在操作窗格上，选择 **编辑查询**。</span><span class="sxs-lookup"><span data-stu-id="14e84-255">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="14e84-256">在查询编辑器对话框中 **联接** 选项卡上，展开并选择树中的 **表 \> 负荷详细信息**。</span><span class="sxs-lookup"><span data-stu-id="14e84-256">In the query editor dialog box, on the **Joins** tab, expand and select **Tables \> Load details** in the tree.</span></span>
1. <span data-ttu-id="14e84-257">选择 **添加表联接**。</span><span class="sxs-lookup"><span data-stu-id="14e84-257">Select **Add table join**.</span></span>
1. <span data-ttu-id="14e84-258">在显示的关系网格中，找到并选择其中的 **关系** 字段设置为 *仓库物料包含（物料编号）* 的行，然后选择 **选择**。</span><span class="sxs-lookup"><span data-stu-id="14e84-258">In the grid of relations that appears, find and select the row where the **Relation** field is set to *Warehouse item number (Item number)*, and then select **Select**.</span></span> 
1. <span data-ttu-id="14e84-259">在 **范围** 选项卡上，选择 **添加** 向网格添加具有以下设置的行：</span><span class="sxs-lookup"><span data-stu-id="14e84-259">On the **Range** tab, select **Add** to add a row that has the following settings to the grid:</span></span>

    - <span data-ttu-id="14e84-260">**表**：*仓库物料编号*</span><span class="sxs-lookup"><span data-stu-id="14e84-260">**Table:** *Warehouse item number*</span></span>
    - <span data-ttu-id="14e84-261">**派生表**：*仓库物料编号*</span><span class="sxs-lookup"><span data-stu-id="14e84-261">**Derived table:** *Warehouse item number*</span></span>
    - <span data-ttu-id="14e84-262">**字段**：*代码 4*</span><span class="sxs-lookup"><span data-stu-id="14e84-262">**Field:** *Code 4*</span></span>
    - <span data-ttu-id="14e84-263">**条件**：*易燃*</span><span class="sxs-lookup"><span data-stu-id="14e84-263">**Criteria:** *Flammable*</span></span>

1. <span data-ttu-id="14e84-264">选择 **确定** 关闭对话框。</span><span class="sxs-lookup"><span data-stu-id="14e84-264">Select **OK** to close the dialog box.</span></span>

> [!NOTE]
> <span data-ttu-id="14e84-265">对于此业务案例，其中的物料具有特定筛选器代码（即其中的 **代码 4** 字段设置为 *易燃* 的筛选器代码）的所有订单行将跨订单与同一种类型的其他物料合并。</span><span class="sxs-lookup"><span data-stu-id="14e84-265">For this business case, all order lines where items have a specific filter code (that is, the filter code where the **Code 4** field is set to *Flammable*) will be consolidated with other items of the same type across orders.</span></span> <span data-ttu-id="14e84-266">如果同一个帐户、仓库和物料组有未结装运，将为其附加新行。</span><span class="sxs-lookup"><span data-stu-id="14e84-266">If there is an open shipment for the same account, warehouse, and group of items, the new lines will be attached to it.</span></span>

### <a name="create-example-policy-3"></a><span data-ttu-id="14e84-267">创建示例策略 3</span><span class="sxs-lookup"><span data-stu-id="14e84-267">Create example policy 3</span></span>

<span data-ttu-id="14e84-268">在此示例中，将创建可用于以下业务案例的 *客户要求* 策略。</span><span class="sxs-lookup"><span data-stu-id="14e84-268">In this example, you will create a *Customers' requirements* policy that can be used for the following business case:</span></span>

- <span data-ttu-id="14e84-269">此策略将查询特定客户帐户。</span><span class="sxs-lookup"><span data-stu-id="14e84-269">The policy will query for a specific customer account.</span></span>
- <span data-ttu-id="14e84-270">已开启与未结装运合并。</span><span class="sxs-lookup"><span data-stu-id="14e84-270">Consolidation with open shipments is turned on.</span></span>
- <span data-ttu-id="14e84-271">将跨订单但基于客户申请进行合并。</span><span class="sxs-lookup"><span data-stu-id="14e84-271">Consolidation is done across orders but is based on customer requisitions.</span></span> <span data-ttu-id="14e84-272">（换句话说，将根据相同客户申请编号和仓库把多个订单组合为装运。）</span><span class="sxs-lookup"><span data-stu-id="14e84-272">(In other words, multiple orders will be grouped into shipments, based on the same customer requisition number and warehouse.)</span></span>

<span data-ttu-id="14e84-273">执行以下步骤为此业务案例创建装运合并策略。</span><span class="sxs-lookup"><span data-stu-id="14e84-273">Follow these steps to create the shipment consolidation policy for this business case.</span></span>

1. <span data-ttu-id="14e84-274">转到 **仓库管理 \> 设置 \> 发放到仓库 \> 装运合并策略**。</span><span class="sxs-lookup"><span data-stu-id="14e84-274">Go to **Warehouse management \> Setup \> Release to warehouse \> Shipment consolidation policies**.</span></span>
1. <span data-ttu-id="14e84-275">将 **策略类型** 字段设置为 *销售订单*。</span><span class="sxs-lookup"><span data-stu-id="14e84-275">Set the **Policy type** field to *Sales orders*.</span></span>
1. <span data-ttu-id="14e84-276">在操作窗格上，选择 **新建** 创建具有以下设置的策略：</span><span class="sxs-lookup"><span data-stu-id="14e84-276">On the Action Pane, select **New** to create a policy that has the following settings:</span></span>

    - <span data-ttu-id="14e84-277">**策略名称**：*CustomerOrderNo*</span><span class="sxs-lookup"><span data-stu-id="14e84-277">**Policy name:** *CustomerOrderNo*</span></span>
    - <span data-ttu-id="14e84-278">**策略说明**：*根据客户 PO 合并行*</span><span class="sxs-lookup"><span data-stu-id="14e84-278">**Policy description:** *Consolidate lines based on customer PO*</span></span>

1. <span data-ttu-id="14e84-279">将 **与未结装运合并** 选项设置为 *是*。</span><span class="sxs-lookup"><span data-stu-id="14e84-279">Set the **Consolidate with open shipments** option to *Yes*.</span></span>
1. <span data-ttu-id="14e84-280">在操作窗格上，选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="14e84-280">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="14e84-281">在 **合并字段** 快速选项卡上 **其余字段** 列表中，选择其中的 **字段名称** 字段设置为 *客户申请* 的行。</span><span class="sxs-lookup"><span data-stu-id="14e84-281">On the **Consolidation fields** FastTab, in the **Remaining fields** list, select the row where the **Field name** field is set to *Customer requisition*.</span></span>
1. <span data-ttu-id="14e84-282">选择 **添加** 按钮 ![向右箭头](media/forward-button.png) 将字段移到 **所选字段** 列表中。</span><span class="sxs-lookup"><span data-stu-id="14e84-282">Select the **Add** button ![Right arrow](media/forward-button.png) to move the field to the **Selected fields** list.</span></span>
1. <span data-ttu-id="14e84-283">在 **其余字段** 列表中，选择其中的 **字段名称** 字段设置为 *交货方式* 的行。</span><span class="sxs-lookup"><span data-stu-id="14e84-283">In the **Remaining fields** list, select the row where the **Field name** field is set to *Mode of delivery*.</span></span>
1. <span data-ttu-id="14e84-284">选择 **添加** 按钮 ![向右箭头](media/forward-button.png) 将字段移到 **所选字段** 列表中。</span><span class="sxs-lookup"><span data-stu-id="14e84-284">Select the **Add** button ![Right arrow](media/forward-button.png) to move the field to the **Selected fields** list.</span></span>
1. <span data-ttu-id="14e84-285">在操作窗格上，选择 **编辑查询**。</span><span class="sxs-lookup"><span data-stu-id="14e84-285">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="14e84-286">在查询编辑器对话框中 **范围** 选项卡上，找到其中的 **字段** 字段设置为 *客户帐户* 的行，然后将该行的 **条件** 字段设置为 *US-001*。</span><span class="sxs-lookup"><span data-stu-id="14e84-286">In the query editor dialog box, on the **Range** tab, find the row where the **Field** field is set to *Customer account*, and set the **Criteria** field for that row to *US-001*.</span></span>
1. <span data-ttu-id="14e84-287">选择 **确定** 关闭对话框。</span><span class="sxs-lookup"><span data-stu-id="14e84-287">Select **OK** to close the dialog box.</span></span>

> [!NOTE]
> <span data-ttu-id="14e84-288">对于此业务案例，无论销售订单编号是什么，都将把其中的销售订单的客户申请编号相同的所有订单行合并为一个装运。</span><span class="sxs-lookup"><span data-stu-id="14e84-288">For this business case, all order lines where sales orders have the same customer requisition number will be consolidated into one shipment, regardless of the sales order number.</span></span> <span data-ttu-id="14e84-289">（客户申请编号用作客户的采购订单 \[PO\] 编号。）如果同一个帐户、仓库和客户申请有未结装运，将为其附加新行。</span><span class="sxs-lookup"><span data-stu-id="14e84-289">(The customer requisition number is used as the customer's purchase order \[PO\] number.) If there is an open shipment for the same account, warehouse, and customer requisition, the new lines will be attached to it.</span></span> <span data-ttu-id="14e84-290">如果一天内客户多次添加具有相同 PO 编号的更多订单行，并且希望将所有行合并为一个装运，可使用此策略。</span><span class="sxs-lookup"><span data-stu-id="14e84-290">This policy can be used if the customer sends additional order lines that have the same PO number several times during a day and wants all the lines to be grouped into one shipment.</span></span> <span data-ttu-id="14e84-291">（换句话说，将有一份提货单和一份装箱单。）</span><span class="sxs-lookup"><span data-stu-id="14e84-291">(In other words, there will be one bill of lading and one packing slip.)</span></span>

### <a name="create-example-policy-4"></a><span data-ttu-id="14e84-292">创建示例策略 4</span><span class="sxs-lookup"><span data-stu-id="14e84-292">Create example policy 4</span></span>

<span data-ttu-id="14e84-293">在此示例中，将创建可用于以下业务案例的 *客户允许合并* 策略。</span><span class="sxs-lookup"><span data-stu-id="14e84-293">In this example, you will create a *Customers allowing consolidation* policy that can be used for the following business case:</span></span>

- <span data-ttu-id="14e84-294">此策略将查询特定订单池以识别接受合并的装运的客户。</span><span class="sxs-lookup"><span data-stu-id="14e84-294">The policy will query for a specific order pool to identify customers who accept consolidated shipments.</span></span>
- <span data-ttu-id="14e84-295">已关闭与未结装运合并。</span><span class="sxs-lookup"><span data-stu-id="14e84-295">Consolidation with open shipments is turned off.</span></span>
- <span data-ttu-id="14e84-296">将使用默认 CrossOrder 策略选择的字段跨订单进行合并（以复制之前的 **在发放到仓库时合并装运** 复选框）。</span><span class="sxs-lookup"><span data-stu-id="14e84-296">Consolidation is done across orders using the fields selected by default CrossOrder policy (to replicate the previous **Consolidate shipment at release to warehouse** check box).</span></span>

- <span data-ttu-id="14e84-297">可以通过选择其他订单池覆盖销售订单中的规则。</span><span class="sxs-lookup"><span data-stu-id="14e84-297">You can override the rule on a sales order by selecting a different order pool.</span></span>

<span data-ttu-id="14e84-298">执行以下步骤为此业务案例创建装运合并策略。</span><span class="sxs-lookup"><span data-stu-id="14e84-298">Follow these steps to create the shipment consolidation policy for this business case.</span></span>

1. <span data-ttu-id="14e84-299">转到 **仓库管理 \> 设置 \> 发放到仓库 \> 装运合并策略**。</span><span class="sxs-lookup"><span data-stu-id="14e84-299">Go to **Warehouse management \> Setup \> Release to warehouse \> Shipment consolidation policies**.</span></span>
1. <span data-ttu-id="14e84-300">将 **策略类型** 字段设置为 *销售订单*。</span><span class="sxs-lookup"><span data-stu-id="14e84-300">Set the **Policy type** field to *Sales orders*.</span></span>
1. <span data-ttu-id="14e84-301">在操作窗格上，选择 **新建** 创建具有以下设置的策略：</span><span class="sxs-lookup"><span data-stu-id="14e84-301">On the Action Pane, select **New** to create a policy that has the following settings:</span></span>

    - <span data-ttu-id="14e84-302">**策略名称**：*订单池*</span><span class="sxs-lookup"><span data-stu-id="14e84-302">**Policy name:** *Order pool*</span></span>
    - <span data-ttu-id="14e84-303">**策略说明**：*根据订单池跨订单合并*</span><span class="sxs-lookup"><span data-stu-id="14e84-303">**Policy description:** *Consolidate across orders based on order pool*</span></span>

1. <span data-ttu-id="14e84-304">让 **与未结装运合并** 选项继续设置为 *否*。</span><span class="sxs-lookup"><span data-stu-id="14e84-304">Leave the **Consolidate with open shipments** option set to *No*.</span></span>
1. <span data-ttu-id="14e84-305">在操作窗格上，选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="14e84-305">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="14e84-306">在 **合并字段** 快速选项卡上 **其余字段** 列表中，选择其中的 **字段名称** 字段设置为 *交货方式* 的行。</span><span class="sxs-lookup"><span data-stu-id="14e84-306">On the **Consolidation fields** FastTab, in the **Remaining fields** list, select the row where the **Field name** field is set to *Mode of delivery*.</span></span>
1. <span data-ttu-id="14e84-307">选择 **添加** 按钮 ![向右箭头](media/forward-button.png) 将字段移到 **所选字段** 列表中。</span><span class="sxs-lookup"><span data-stu-id="14e84-307">Select the **Add** button ![Right arrow](media/forward-button.png) to move the field to the **Selected fields** list.</span></span>
1. <span data-ttu-id="14e84-308">在操作窗格上，选择 **编辑查询**。</span><span class="sxs-lookup"><span data-stu-id="14e84-308">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="14e84-309">在查询编辑器对话框中 **范围** 选项卡上，选择 **添加** 向网格添加具有以下设置的行：</span><span class="sxs-lookup"><span data-stu-id="14e84-309">In the query editor dialog box, on the **Range** tab, select **Add** to add a row that has the following settings to the grid:</span></span>

    - <span data-ttu-id="14e84-310">**表**：*销售订单*</span><span class="sxs-lookup"><span data-stu-id="14e84-310">**Table:** *Sales orders*</span></span>
    - <span data-ttu-id="14e84-311">**派生表**：*销售订单*</span><span class="sxs-lookup"><span data-stu-id="14e84-311">**Derived table:** *Sales orders*</span></span>
    - <span data-ttu-id="14e84-312">**字段**：*池*</span><span class="sxs-lookup"><span data-stu-id="14e84-312">**Field:** *Pool*</span></span>
    - <span data-ttu-id="14e84-313">**条件**：*ShipCons*</span><span class="sxs-lookup"><span data-stu-id="14e84-313">**Criteria:** *ShipCons*</span></span>

1. <span data-ttu-id="14e84-314">选择 **确定** 关闭对话框。</span><span class="sxs-lookup"><span data-stu-id="14e84-314">Select **OK** to close the dialog box.</span></span>

> [!NOTE]
> <span data-ttu-id="14e84-315">对于此业务案例，其中的销售订单属于同一个订单池的所有订单行将跨同一个帐户、仓库和交装运输方式的销售订单合并为一个装运。</span><span class="sxs-lookup"><span data-stu-id="14e84-315">For this business case, all order lines where sales orders belong to the same order pool will be consolidated into one shipment across sales orders for the same account, warehouse, and transportation mode of delivery.</span></span> <span data-ttu-id="14e84-316">可以使用其他任何字段而不是订单池区分一组客户，并默认使用销售订单标题。</span><span class="sxs-lookup"><span data-stu-id="14e84-316">Instead of the order pool, you can use any other field to distinguish a group of customers and use the sales order header by default.</span></span> <span data-ttu-id="14e84-317">如果客户而不是仓库推动了对合并的需要，可使用这种方法。</span><span class="sxs-lookup"><span data-stu-id="14e84-317">You can use this approach if the customer, not the warehouse, is driving the need for consolidation.</span></span> <span data-ttu-id="14e84-318">（在之前的合并策略中，推动合并需要的是仓库。）</span><span class="sxs-lookup"><span data-stu-id="14e84-318">(In the earlier consolidation logic, the warehouse drove the need for consolidation.)</span></span>

### <a name="create-example-policy-5"></a><span data-ttu-id="14e84-319">创建示例策略 5</span><span class="sxs-lookup"><span data-stu-id="14e84-319">Create example policy 5</span></span>

<span data-ttu-id="14e84-320">在此示例中，将创建可用于以下业务案例的 *仓库允许合并* 策略。</span><span class="sxs-lookup"><span data-stu-id="14e84-320">In this example, you will create a *Warehouses allowing consolidation* policy that can be used for the following business case:</span></span>

- <span data-ttu-id="14e84-321">此策略将查询特定订单池以识别可合并装运的仓库。</span><span class="sxs-lookup"><span data-stu-id="14e84-321">The policy will query for a specific order pool to identify warehouses that can consolidate shipments.</span></span>
- <span data-ttu-id="14e84-322">已关闭与未结装运合并。</span><span class="sxs-lookup"><span data-stu-id="14e84-322">Consolidation with open shipments is turned off.</span></span>
- <span data-ttu-id="14e84-323">将使用默认 CrossOrder 策略选择的字段跨订单进行合并（以复制之前的 **在发放到仓库时合并装运** 复选框）。</span><span class="sxs-lookup"><span data-stu-id="14e84-323">Consolidation is done across orders using the fields selected by default CrossOrder policy (to replicate the previous **Consolidate shipment at release to warehouse** check box).</span></span>

<span data-ttu-id="14e84-324">通常可使用在[方案 1](#scenario-1) 中创建的默认策略解决此业务案例。</span><span class="sxs-lookup"><span data-stu-id="14e84-324">Typically, this business case can be addressed by using the default policies that you created in [scenario 1](#scenario-1).</span></span> <span data-ttu-id="14e84-325">但是，也可以执行以下步骤手动创建类似策略。</span><span class="sxs-lookup"><span data-stu-id="14e84-325">However, you can also manually create similar policies by following these steps.</span></span>

1. <span data-ttu-id="14e84-326">转到 **仓库管理 \> 设置 \> 发放到仓库 \> 装运合并策略**。</span><span class="sxs-lookup"><span data-stu-id="14e84-326">Go to **Warehouse management \> Setup \> Release to warehouse \> Shipment consolidation policies**.</span></span>
1. <span data-ttu-id="14e84-327">将 **策略类型** 字段设置为 *销售订单*。</span><span class="sxs-lookup"><span data-stu-id="14e84-327">Set the **Policy type** field to *Sales orders*.</span></span>
1. <span data-ttu-id="14e84-328">在操作窗格上，选择 **新建** 创建具有以下设置的策略：</span><span class="sxs-lookup"><span data-stu-id="14e84-328">On the Action Pane, select **New** to create a policy that has the following settings:</span></span>

    - <span data-ttu-id="14e84-329">**策略名称**：*Cross-order*</span><span class="sxs-lookup"><span data-stu-id="14e84-329">**Policy name:** *Cross-order*</span></span>
    - <span data-ttu-id="14e84-330">**策略说明**：*跨订单合并特定仓库*</span><span class="sxs-lookup"><span data-stu-id="14e84-330">**Policy description:** *Cross-order consolidation for specific warehouses*</span></span>

1. <span data-ttu-id="14e84-331">让 **与未结装运合并** 选项继续设置为 *否*。</span><span class="sxs-lookup"><span data-stu-id="14e84-331">Leave the **Consolidate with open shipments** option set to *No*.</span></span>
1. <span data-ttu-id="14e84-332">在操作窗格上，选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="14e84-332">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="14e84-333">在 **合并字段** 快速选项卡上 **其余字段** 字段中，选择其中的 **字段名称** 字段设置为 *交货方式* 的行。</span><span class="sxs-lookup"><span data-stu-id="14e84-333">On the **Consolidation fields** FastTab, in the **Remaining fields** field, select the row where the **Field name** field is set to *Mode of delivery*.</span></span>
1. <span data-ttu-id="14e84-334">选择 **添加** 按钮 ![向右箭头](media/forward-button.png) 将字段移到 **所选字段** 列表中。</span><span class="sxs-lookup"><span data-stu-id="14e84-334">Select the **Add** button ![Right arrow](media/forward-button.png) to move the field to the **Selected fields** list.</span></span>
1. <span data-ttu-id="14e84-335">在操作窗格上，选择 **编辑查询**。</span><span class="sxs-lookup"><span data-stu-id="14e84-335">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="14e84-336">在查询编辑器对话框中 **范围** 选项卡上，找到其中的 **字段** 字段设置为 *仓库* 的行，然后将该行的 **条件** 字段设置为 *61, 63*。</span><span class="sxs-lookup"><span data-stu-id="14e84-336">In the query editor dialog box, on the **Range** tab, find the row where the **Field** field is set to *Warehouse*, and set the **Criteria** field for that row to *61, 63*.</span></span>
1. <span data-ttu-id="14e84-337">选择 **确定** 关闭对话框。</span><span class="sxs-lookup"><span data-stu-id="14e84-337">Select **OK** to close the dialog box.</span></span>

### <a name="set-the-order"></a><span data-ttu-id="14e84-338">设置顺序</span><span class="sxs-lookup"><span data-stu-id="14e84-338">Set the order</span></span>

<span data-ttu-id="14e84-339">鉴于已经创建了所有策略，现在必须建立这些策略将采用的顺序。</span><span class="sxs-lookup"><span data-stu-id="14e84-339">Now that you've created all your policies, you must establish the order that they will be applied in.</span></span> <span data-ttu-id="14e84-340">若要使用金字塔式方法（其中条件最多的策略评估为优先级最高），请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="14e84-340">To use a pyramid-like approach, where the policies that have the most conditions are evaluated as having the highest priority, follow these steps.</span></span>

1. <span data-ttu-id="14e84-341">转到 **仓库管理 \> 设置 \> 发放到仓库 \> 装运合并策略**。</span><span class="sxs-lookup"><span data-stu-id="14e84-341">Go to **Warehouse management \> Setup \> Release to warehouse \> Shipment consolidation policies**.</span></span>
1. <span data-ttu-id="14e84-342">将 **策略类型** 字段设置为 *销售订单*。</span><span class="sxs-lookup"><span data-stu-id="14e84-342">Set the **Policy type** field to *Sales orders*.</span></span>
1. <span data-ttu-id="14e84-343">选择左列中列出的每个策略，然后使用操作窗格中的 **上移** 和 **下移** 按钮按照以下顺序排列策略：</span><span class="sxs-lookup"><span data-stu-id="14e84-343">Select each policy that is listed in the left column, and then use the **Move up** and **Move down** buttons on the Action Pane to arrange the policies in the following order:</span></span>

    1. <span data-ttu-id="14e84-344">CustomerMode</span><span class="sxs-lookup"><span data-stu-id="14e84-344">CustomerMode</span></span>
    1. <span data-ttu-id="14e84-345">物料类型</span><span class="sxs-lookup"><span data-stu-id="14e84-345">Item type</span></span>
    1. <span data-ttu-id="14e84-346">CustomerOrderNo</span><span class="sxs-lookup"><span data-stu-id="14e84-346">CustomerOrderNo</span></span>
    1. <span data-ttu-id="14e84-347">订单池</span><span class="sxs-lookup"><span data-stu-id="14e84-347">Order pool</span></span>
    1. <span data-ttu-id="14e84-348">Cross-order</span><span class="sxs-lookup"><span data-stu-id="14e84-348">Cross-order</span></span>
    1. <span data-ttu-id="14e84-349">默认值</span><span class="sxs-lookup"><span data-stu-id="14e84-349">Default</span></span>

## <a name="example-scenarios-of-how-to-use-shipment-consolidation-policies"></a><a name="example-scenarios"></a> <span data-ttu-id="14e84-350">有关如何使用装运合并策略的示例方案</span><span class="sxs-lookup"><span data-stu-id="14e84-350">Example scenarios of how to use shipment consolidation policies</span></span>

<span data-ttu-id="14e84-351">以下方案说明如何在阅读本主题的同时使用创建的装运合并策略。</span><span class="sxs-lookup"><span data-stu-id="14e84-351">The following scenarios illustrate how you could use the shipment consolidation policies that you created while reading this topic.</span></span> <span data-ttu-id="14e84-352">每个方案将引导您完成装运合并流程，此流程在自动或手动发放到仓库期间使用装运合并策略：</span><span class="sxs-lookup"><span data-stu-id="14e84-352">Each scenario walks you through a shipment consolidation process that uses shipment consolidation policies during automated or manual release to the warehouse:</span></span>

- <span data-ttu-id="14e84-353">方案 1：[使用自动发放销售订单发放到仓库时使用合并](../warehousing/consolidate-shipments-automatic.md)</span><span class="sxs-lookup"><span data-stu-id="14e84-353">Scenario 1: [Consolidate shipments when they are released to the warehouse by using Automatic release of sales orders](../warehousing/consolidate-shipments-automatic.md)</span></span>
- <span data-ttu-id="14e84-354">方案 2：[覆盖了装运合并策略时从“发放到仓库”页合并装运](../warehousing/consolidate-shipments-release-to-warehouse-override.md)</span><span class="sxs-lookup"><span data-stu-id="14e84-354">Scenario 2: [Consolidate shipments when the shipment consolidation policy is overridden from the Release to warehouse page](../warehousing/consolidate-shipments-release-to-warehouse-override.md)</span></span>
- <span data-ttu-id="14e84-355">方案 3：[使用装载计划工作台中的“发放到仓库”合并装运](../warehousing/consolidate-shipments-load-planning-workbench.md)</span><span class="sxs-lookup"><span data-stu-id="14e84-355">Scenario 3: [Consolidate shipments by using Release to warehouse from the load planning workbench](../warehousing/consolidate-shipments-load-planning-workbench.md)</span></span>
- <span data-ttu-id="14e84-356">方案 4：[使用装运合并工作台合并装运](../warehousing/consolidate-shipments-manual-workbench.md)</span><span class="sxs-lookup"><span data-stu-id="14e84-356">Scenario 4: [Consolidate shipments by using the shipment consolidation workbench](../warehousing/consolidate-shipments-manual-workbench.md)</span></span>
- <span data-ttu-id="14e84-357">方案 5：[使用合并装运页面手动合并装运](../warehousing/consolidate-shipments-manual-form.md)</span><span class="sxs-lookup"><span data-stu-id="14e84-357">Scenario 5: [Consolidate shipments manually by using the Consolidate shipments page](../warehousing/consolidate-shipments-manual-form.md)</span></span>


## <a name="additional-resources"></a><span data-ttu-id="14e84-358">其他资源</span><span class="sxs-lookup"><span data-stu-id="14e84-358">Additional resources</span></span>

- [<span data-ttu-id="14e84-359">装运合并政策</span><span class="sxs-lookup"><span data-stu-id="14e84-359">Shipment consolidation policies</span></span>](about-shipment-consolidation-policies.md)
