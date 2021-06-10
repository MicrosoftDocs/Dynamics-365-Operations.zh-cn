---
title: 为 Warehouse Management 移动应用分配步骤图标和标题
description: 本主题介绍如何为 Warehouse Management 移动应用的新任务流或自定义任务流分配步骤图标和标题。
author: MarkusFogelberg
ms.date: 05/17/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2021-05-17
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 9523492d766669e6c38579fba7b5ddd6b3d282fc
ms.sourcegitcommit: c53de2c09b9296b41653e739178edf29f79e0679
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/17/2021
ms.locfileid: "6049356"
---
# <a name="assign-step-icons-and-titles-for-the-warehouse-management-mobile-app"></a><span data-ttu-id="b66b9-103">为 Warehouse Management 移动应用分配步骤图标和标题</span><span class="sxs-lookup"><span data-stu-id="b66b9-103">Assign step icons and titles for the Warehouse Management mobile app</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b66b9-104">本主题介绍如何为 Warehouse Management 移动应用的新任务流或自定义任务流分配步骤图标和步骤标题。</span><span class="sxs-lookup"><span data-stu-id="b66b9-104">This topic describes how to assign step icons and step titles for new or customized task flows for the Warehouse Management mobile app.</span></span>

<span data-ttu-id="b66b9-105">下图显示了 Warehouse Management 移动应用中步骤图标和标题的显示方式。</span><span class="sxs-lookup"><span data-stu-id="b66b9-105">The following illustrations shows how step icons and titles appear in the Warehouse Management mobile app.</span></span>

<span data-ttu-id="b66b9-106">![Warehouse Management 移动应用中步骤图标和步骤标题的示例](media/step-icon-example.png "Warehouse Management 移动应用中步骤图标和步骤标题的示例")</span><span class="sxs-lookup"><span data-stu-id="b66b9-106">![Example of a step icon and a step title in the Warehouse Management mobile app](media/step-icon-example.png "Example of a step icon and a step title in the Warehouse Management mobile app")</span></span>

## <a name="turn-on-this-feature-in-your-system"></a><span data-ttu-id="b66b9-107">在系统中开启此功能</span><span class="sxs-lookup"><span data-stu-id="b66b9-107">Turn on this feature in your system</span></span>

<span data-ttu-id="b66b9-108">此功能只有在系统中开启之后才能使用。</span><span class="sxs-lookup"><span data-stu-id="b66b9-108">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="b66b9-109">管理员可以使用[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)设置以检查功能状态和打开功能。</span><span class="sxs-lookup"><span data-stu-id="b66b9-109">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="b66b9-110">在 **功能管理** 工作区中，此功能按照下面的方式列出：</span><span class="sxs-lookup"><span data-stu-id="b66b9-110">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="b66b9-111">**模块**：*仓库管理*</span><span class="sxs-lookup"><span data-stu-id="b66b9-111">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="b66b9-112">**功能名称**：*新仓库应用的用户设置、图标和步骤标题*</span><span class="sxs-lookup"><span data-stu-id="b66b9-112">**Feature name:** *User settings, icons, and step titles for the new warehouse app*</span></span>

## <a name="standard-step-ids-classes-and-icons"></a><span data-ttu-id="b66b9-113">标准步骤 ID、类和图标</span><span class="sxs-lookup"><span data-stu-id="b66b9-113">Standard step IDs, classes, and icons</span></span>

<span data-ttu-id="b66b9-114">任务流中的每个步骤由一个步骤 ID 标识，每个步骤 ID 有对应的步骤类。</span><span class="sxs-lookup"><span data-stu-id="b66b9-114">Each step in a task flow is identified by a step ID, and each step ID has a corresponding step class.</span></span> <span data-ttu-id="b66b9-115">在每个步骤类中指定步骤图标和标题。</span><span class="sxs-lookup"><span data-stu-id="b66b9-115">The step icon and title are specified in each step class.</span></span>

### <a name="step-ids-and-step-classes"></a><a name="step-ids-classes"></a><span data-ttu-id="b66b9-116">步骤 ID 和步骤类</span><span class="sxs-lookup"><span data-stu-id="b66b9-116">Step IDs and step classes</span></span>

<span data-ttu-id="b66b9-117">下表列出了当前可用的每个步骤 ID，以及对应的步骤类。</span><span class="sxs-lookup"><span data-stu-id="b66b9-117">The following table lists every step ID that is currently available, and its corresponding step class.</span></span> <span data-ttu-id="b66b9-118">主输入字段的控件名称用作步骤 ID。</span><span class="sxs-lookup"><span data-stu-id="b66b9-118">The control name of the primary input field is used as the step ID.</span></span>

<span data-ttu-id="b66b9-119">有关演示如何使用这些步骤 ID 和类的示例，请参阅本主题后面[示例：为自定义流分配步骤图标和标题](#example)一节中的 `WHSMobileAppStepInfoBuilder.stepId()` 方法的实现。</span><span class="sxs-lookup"><span data-stu-id="b66b9-119">For an example that shows how these step IDs and classes are used, see the implementation of the `WHSMobileAppStepInfoBuilder.stepId()` method in the [Example: Assign step icons and titles for a custom flow](#example) section later in this topic.</span></span>

| <span data-ttu-id="b66b9-120">步骤 ID</span><span class="sxs-lookup"><span data-stu-id="b66b9-120">Step ID</span></span> | <span data-ttu-id="b66b9-121">步骤类</span><span class="sxs-lookup"><span data-stu-id="b66b9-121">Step Class</span></span> |
|-|-|
| <span data-ttu-id="b66b9-122">BatchDisposition</span><span class="sxs-lookup"><span data-stu-id="b66b9-122">BatchDisposition</span></span> | <span data-ttu-id="b66b9-123">WHSMobileAppStepBatchDisposition</span><span class="sxs-lookup"><span data-stu-id="b66b9-123">WHSMobileAppStepBatchDisposition</span></span> |
| <span data-ttu-id="b66b9-124">承运人</span><span class="sxs-lookup"><span data-stu-id="b66b9-124">Carrier</span></span> | <span data-ttu-id="b66b9-125">WHSMobileAppStepCarrier</span><span class="sxs-lookup"><span data-stu-id="b66b9-125">WHSMobileAppStepCarrier</span></span> |
| <span data-ttu-id="b66b9-126">CatchWeight</span><span class="sxs-lookup"><span data-stu-id="b66b9-126">CatchWeight</span></span> | <span data-ttu-id="b66b9-127">WHSMobileAppStepCatchWeight</span><span class="sxs-lookup"><span data-stu-id="b66b9-127">WHSMobileAppStepCatchWeight</span></span> |
| <span data-ttu-id="b66b9-128">CatchWeightQtyOutboundWeight</span><span class="sxs-lookup"><span data-stu-id="b66b9-128">CatchWeightQtyOutboundWeight</span></span> | <span data-ttu-id="b66b9-129">WHSMobileAppStepCatchWeight</span><span class="sxs-lookup"><span data-stu-id="b66b9-129">WHSMobileAppStepCatchWeight</span></span> |
| <span data-ttu-id="b66b9-130">CatchWeightTag</span><span class="sxs-lookup"><span data-stu-id="b66b9-130">CatchWeightTag</span></span> | <span data-ttu-id="b66b9-131">WHSMobileAppStepCatchWeightTag</span><span class="sxs-lookup"><span data-stu-id="b66b9-131">WHSMobileAppStepCatchWeightTag</span></span> |
| <span data-ttu-id="b66b9-132">CatchWeightTagWeight</span><span class="sxs-lookup"><span data-stu-id="b66b9-132">CatchWeightTagWeight</span></span> | <span data-ttu-id="b66b9-133">WHSMobileAppStepCatchWeightTagWeight</span><span class="sxs-lookup"><span data-stu-id="b66b9-133">WHSMobileAppStepCatchWeightTagWeight</span></span> |
| <span data-ttu-id="b66b9-134">ChangeWarehouseSuccess</span><span class="sxs-lookup"><span data-stu-id="b66b9-134">ChangeWarehouseSuccess</span></span> | <span data-ttu-id="b66b9-135">WHSMobileAppStepChangeWarehouseSuccess</span><span class="sxs-lookup"><span data-stu-id="b66b9-135">WHSMobileAppStepChangeWarehouseSuccess</span></span> |
| <span data-ttu-id="b66b9-136">CheckDigit</span><span class="sxs-lookup"><span data-stu-id="b66b9-136">CheckDigit</span></span> | <span data-ttu-id="b66b9-137">WHSMobileAppStepCheckDigit</span><span class="sxs-lookup"><span data-stu-id="b66b9-137">WHSMobileAppStepCheckDigit</span></span> |
| <span data-ttu-id="b66b9-138">ClusterId</span><span class="sxs-lookup"><span data-stu-id="b66b9-138">ClusterId</span></span> | <span data-ttu-id="b66b9-139">WHSMobileAppStepClusterId</span><span class="sxs-lookup"><span data-stu-id="b66b9-139">WHSMobileAppStepClusterId</span></span> |
| <span data-ttu-id="b66b9-140">ClusterPickQtyVerification</span><span class="sxs-lookup"><span data-stu-id="b66b9-140">ClusterPickQtyVerification</span></span> | <span data-ttu-id="b66b9-141">WHSMobileAppStepQtyVerification</span><span class="sxs-lookup"><span data-stu-id="b66b9-141">WHSMobileAppStepQtyVerification</span></span> |
| <span data-ttu-id="b66b9-142">ClusterPosition</span><span class="sxs-lookup"><span data-stu-id="b66b9-142">ClusterPosition</span></span> | <span data-ttu-id="b66b9-143">WHSMobileAppStepClusterPosition</span><span class="sxs-lookup"><span data-stu-id="b66b9-143">WHSMobileAppStepClusterPosition</span></span> |
| <span data-ttu-id="b66b9-144">ConfigId</span><span class="sxs-lookup"><span data-stu-id="b66b9-144">ConfigId</span></span> | <span data-ttu-id="b66b9-145">WHSMobileAppStepConfigId</span><span class="sxs-lookup"><span data-stu-id="b66b9-145">WHSMobileAppStepConfigId</span></span> |
| <span data-ttu-id="b66b9-146">确认单</span><span class="sxs-lookup"><span data-stu-id="b66b9-146">Confirmation</span></span> | <span data-ttu-id="b66b9-147">WHSMobileAppStepConfirmation</span><span class="sxs-lookup"><span data-stu-id="b66b9-147">WHSMobileAppStepConfirmation</span></span> |
| <span data-ttu-id="b66b9-148">ConsolidateFromLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="b66b9-148">ConsolidateFromLicensePlateId</span></span> | <span data-ttu-id="b66b9-149">WHSMobileAppStepConsolidateFromLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="b66b9-149">WHSMobileAppStepConsolidateFromLicensePlateId</span></span> |
| <span data-ttu-id="b66b9-150">ConsolidateLPConfirmation</span><span class="sxs-lookup"><span data-stu-id="b66b9-150">ConsolidateLPConfirmation</span></span> | <span data-ttu-id="b66b9-151">WHSMobileAppStepConsolidateLPConfirmation</span><span class="sxs-lookup"><span data-stu-id="b66b9-151">WHSMobileAppStepConsolidateLPConfirmation</span></span> |
| <span data-ttu-id="b66b9-152">ConsolidateToLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="b66b9-152">ConsolidateToLicensePlateId</span></span> | <span data-ttu-id="b66b9-153">WHSMobileAppStepConsolidateToLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="b66b9-153">WHSMobileAppStepConsolidateToLicensePlateId</span></span> |
| <span data-ttu-id="b66b9-154">ContainerType</span><span class="sxs-lookup"><span data-stu-id="b66b9-154">ContainerType</span></span> | <span data-ttu-id="b66b9-155">WHSMobileAppStepContainerType</span><span class="sxs-lookup"><span data-stu-id="b66b9-155">WHSMobileAppStepContainerType</span></span> |
| <span data-ttu-id="b66b9-156">CountingReasonCode</span><span class="sxs-lookup"><span data-stu-id="b66b9-156">CountingReasonCode</span></span> | <span data-ttu-id="b66b9-157">WHSMobileAppStepCountingReasonCode</span><span class="sxs-lookup"><span data-stu-id="b66b9-157">WHSMobileAppStepCountingReasonCode</span></span> |
| <span data-ttu-id="b66b9-158">CycleCountingAddLPOrFinish</span><span class="sxs-lookup"><span data-stu-id="b66b9-158">CycleCountingAddLPOrFinish</span></span> | <span data-ttu-id="b66b9-159">WHSMobileAppStepCycleCountingAddLPOrFinish</span><span class="sxs-lookup"><span data-stu-id="b66b9-159">WHSMobileAppStepCycleCountingAddLPOrFinish</span></span> |
| <span data-ttu-id="b66b9-160">CycleCountQty1</span><span class="sxs-lookup"><span data-stu-id="b66b9-160">CycleCountQty1</span></span> | <span data-ttu-id="b66b9-161">WHSMobileAppStepCycleCountQty</span><span class="sxs-lookup"><span data-stu-id="b66b9-161">WHSMobileAppStepCycleCountQty</span></span> |
| <span data-ttu-id="b66b9-162">CycleCountQty2</span><span class="sxs-lookup"><span data-stu-id="b66b9-162">CycleCountQty2</span></span> | <span data-ttu-id="b66b9-163">WHSMobileAppStepCycleCountQty</span><span class="sxs-lookup"><span data-stu-id="b66b9-163">WHSMobileAppStepCycleCountQty</span></span> |
| <span data-ttu-id="b66b9-164">CycleCountQty3</span><span class="sxs-lookup"><span data-stu-id="b66b9-164">CycleCountQty3</span></span> | <span data-ttu-id="b66b9-165">WHSMobileAppStepCycleCountQty</span><span class="sxs-lookup"><span data-stu-id="b66b9-165">WHSMobileAppStepCycleCountQty</span></span> |
| <span data-ttu-id="b66b9-166">CycleCountQty4</span><span class="sxs-lookup"><span data-stu-id="b66b9-166">CycleCountQty4</span></span> | <span data-ttu-id="b66b9-167">WHSMobileAppStepCycleCountQty</span><span class="sxs-lookup"><span data-stu-id="b66b9-167">WHSMobileAppStepCycleCountQty</span></span> |
| <span data-ttu-id="b66b9-168">Disposition</span><span class="sxs-lookup"><span data-stu-id="b66b9-168">Disposition</span></span> | <span data-ttu-id="b66b9-169">WHSMobileAppStepDisposition</span><span class="sxs-lookup"><span data-stu-id="b66b9-169">WHSMobileAppStepDisposition</span></span> |
| <span data-ttu-id="b66b9-170">DriverCheckInConfirmation</span><span class="sxs-lookup"><span data-stu-id="b66b9-170">DriverCheckInConfirmation</span></span> | <span data-ttu-id="b66b9-171">WHSMobileAppStepDriverCheckInConfirmation</span><span class="sxs-lookup"><span data-stu-id="b66b9-171">WHSMobileAppStepDriverCheckInConfirmation</span></span> |
| <span data-ttu-id="b66b9-172">DriverCheckInId</span><span class="sxs-lookup"><span data-stu-id="b66b9-172">DriverCheckInId</span></span> | <span data-ttu-id="b66b9-173">WHSMobileAppStepDriverCheckInId</span><span class="sxs-lookup"><span data-stu-id="b66b9-173">WHSMobileAppStepDriverCheckInId</span></span> |
| <span data-ttu-id="b66b9-174">DriverCheckOutConfirmation</span><span class="sxs-lookup"><span data-stu-id="b66b9-174">DriverCheckOutConfirmation</span></span> | <span data-ttu-id="b66b9-175">WHSMobileAppStepDriverCheckOutConfirmation</span><span class="sxs-lookup"><span data-stu-id="b66b9-175">WHSMobileAppStepDriverCheckOutConfirmation</span></span> |
| <span data-ttu-id="b66b9-176">DriverCheckOutId</span><span class="sxs-lookup"><span data-stu-id="b66b9-176">DriverCheckOutId</span></span> | <span data-ttu-id="b66b9-177">WHSMobileAppStepDriverCheckOutId</span><span class="sxs-lookup"><span data-stu-id="b66b9-177">WHSMobileAppStepDriverCheckOutId</span></span> |
| <span data-ttu-id="b66b9-178">ExpDate</span><span class="sxs-lookup"><span data-stu-id="b66b9-178">ExpDate</span></span> | <span data-ttu-id="b66b9-179">WHSMobileAppStepExpDate</span><span class="sxs-lookup"><span data-stu-id="b66b9-179">WHSMobileAppStepExpDate</span></span> |
| <span data-ttu-id="b66b9-180">FromBatchDisposition</span><span class="sxs-lookup"><span data-stu-id="b66b9-180">FromBatchDisposition</span></span> | <span data-ttu-id="b66b9-181">WHSMobileAppStepFromBatchDisposition</span><span class="sxs-lookup"><span data-stu-id="b66b9-181">WHSMobileAppStepFromBatchDisposition</span></span> |
| <span data-ttu-id="b66b9-182">FromInventoryStatus</span><span class="sxs-lookup"><span data-stu-id="b66b9-182">FromInventoryStatus</span></span> | <span data-ttu-id="b66b9-183">WHSMobileAppStepInventoryStatusFrom</span><span class="sxs-lookup"><span data-stu-id="b66b9-183">WHSMobileAppStepInventoryStatusFrom</span></span> |
| <span data-ttu-id="b66b9-184">FullQty</span><span class="sxs-lookup"><span data-stu-id="b66b9-184">FullQty</span></span> | <span data-ttu-id="b66b9-185">WHSMobileAppStepFullQty</span><span class="sxs-lookup"><span data-stu-id="b66b9-185">WHSMobileAppStepFullQty</span></span> |
| <span data-ttu-id="b66b9-186">InboundPut</span><span class="sxs-lookup"><span data-stu-id="b66b9-186">InboundPut</span></span> | <span data-ttu-id="b66b9-187">WHSMobileAppStepInboundPut</span><span class="sxs-lookup"><span data-stu-id="b66b9-187">WHSMobileAppStepInboundPut</span></span> |
| <span data-ttu-id="b66b9-188">InventBatchId</span><span class="sxs-lookup"><span data-stu-id="b66b9-188">InventBatchId</span></span> | <span data-ttu-id="b66b9-189">WHSMobileAppStepBatch</span><span class="sxs-lookup"><span data-stu-id="b66b9-189">WHSMobileAppStepBatch</span></span> |
| <span data-ttu-id="b66b9-190">InventColorId</span><span class="sxs-lookup"><span data-stu-id="b66b9-190">InventColorId</span></span> | <span data-ttu-id="b66b9-191">WHSMobileAppStepInventColorId</span><span class="sxs-lookup"><span data-stu-id="b66b9-191">WHSMobileAppStepInventColorId</span></span> |
| <span data-ttu-id="b66b9-192">InventLocation</span><span class="sxs-lookup"><span data-stu-id="b66b9-192">InventLocation</span></span> | <span data-ttu-id="b66b9-193">WHSMobileAppStepInventLocation</span><span class="sxs-lookup"><span data-stu-id="b66b9-193">WHSMobileAppStepInventLocation</span></span> |
| <span data-ttu-id="b66b9-194">InventLocationId</span><span class="sxs-lookup"><span data-stu-id="b66b9-194">InventLocationId</span></span> | <span data-ttu-id="b66b9-195">WHSMobileAppStepWarehouse</span><span class="sxs-lookup"><span data-stu-id="b66b9-195">WHSMobileAppStepWarehouse</span></span> |
| <span data-ttu-id="b66b9-196">InventSerialId</span><span class="sxs-lookup"><span data-stu-id="b66b9-196">InventSerialId</span></span> | <span data-ttu-id="b66b9-197">WHSMobileAppStepInventSerialId</span><span class="sxs-lookup"><span data-stu-id="b66b9-197">WHSMobileAppStepInventSerialId</span></span> |
| <span data-ttu-id="b66b9-198">InventSizeId</span><span class="sxs-lookup"><span data-stu-id="b66b9-198">InventSizeId</span></span> | <span data-ttu-id="b66b9-199">WHSMobileAppStepInventSizeId</span><span class="sxs-lookup"><span data-stu-id="b66b9-199">WHSMobileAppStepInventSizeId</span></span> |
| <span data-ttu-id="b66b9-200">InventStatusId</span><span class="sxs-lookup"><span data-stu-id="b66b9-200">InventStatusId</span></span> | <span data-ttu-id="b66b9-201">WHSMobileAppStepInventStatus</span><span class="sxs-lookup"><span data-stu-id="b66b9-201">WHSMobileAppStepInventStatus</span></span> |
| <span data-ttu-id="b66b9-202">InventStyleId</span><span class="sxs-lookup"><span data-stu-id="b66b9-202">InventStyleId</span></span> | <span data-ttu-id="b66b9-203">WHSMobileAppStepInventStyleId</span><span class="sxs-lookup"><span data-stu-id="b66b9-203">WHSMobileAppStepInventStyleId</span></span> |
| <span data-ttu-id="b66b9-204">InventVersionId</span><span class="sxs-lookup"><span data-stu-id="b66b9-204">InventVersionId</span></span> | <span data-ttu-id="b66b9-205">WHSMobileAppStepInventVersionId</span><span class="sxs-lookup"><span data-stu-id="b66b9-205">WHSMobileAppStepInventVersionId</span></span> |
| <span data-ttu-id="b66b9-206">ItemId</span><span class="sxs-lookup"><span data-stu-id="b66b9-206">ItemId</span></span> | <span data-ttu-id="b66b9-207">WHSMobileAppStepItem</span><span class="sxs-lookup"><span data-stu-id="b66b9-207">WHSMobileAppStepItem</span></span> |
| <span data-ttu-id="b66b9-208">ITMContainerID</span><span class="sxs-lookup"><span data-stu-id="b66b9-208">ITMContainerID</span></span> | <span data-ttu-id="b66b9-209">ITMMobileAppStepContainerId</span><span class="sxs-lookup"><span data-stu-id="b66b9-209">ITMMobileAppStepContainerId</span></span> |
| <span data-ttu-id="b66b9-210">ITMShipmentID</span><span class="sxs-lookup"><span data-stu-id="b66b9-210">ITMShipmentID</span></span> | <span data-ttu-id="b66b9-211">ITMMobileAppStepShipmentId</span><span class="sxs-lookup"><span data-stu-id="b66b9-211">ITMMobileAppStepShipmentId</span></span> |
| <span data-ttu-id="b66b9-212">KanbanCardId</span><span class="sxs-lookup"><span data-stu-id="b66b9-212">KanbanCardId</span></span> | <span data-ttu-id="b66b9-213">WHSMobileAppStepKanbanCard</span><span class="sxs-lookup"><span data-stu-id="b66b9-213">WHSMobileAppStepKanbanCard</span></span> |
| <span data-ttu-id="b66b9-214">KanbanCardToEmpty</span><span class="sxs-lookup"><span data-stu-id="b66b9-214">KanbanCardToEmpty</span></span> | <span data-ttu-id="b66b9-215">WHSMobileAppStepKanbanCardToEmpty</span><span class="sxs-lookup"><span data-stu-id="b66b9-215">WHSMobileAppStepKanbanCardToEmpty</span></span> |
| <span data-ttu-id="b66b9-216">KanbanOrCardId</span><span class="sxs-lookup"><span data-stu-id="b66b9-216">KanbanOrCardId</span></span> | <span data-ttu-id="b66b9-217">WHSMobileAppStepKanbanCard</span><span class="sxs-lookup"><span data-stu-id="b66b9-217">WHSMobileAppStepKanbanCard</span></span> |
| <span data-ttu-id="b66b9-218">LicensePlateId</span><span class="sxs-lookup"><span data-stu-id="b66b9-218">LicensePlateId</span></span> | <span data-ttu-id="b66b9-219">WHSMobileAppStepLicensePlate</span><span class="sxs-lookup"><span data-stu-id="b66b9-219">WHSMobileAppStepLicensePlate</span></span> |
| <span data-ttu-id="b66b9-220">LoadId</span><span class="sxs-lookup"><span data-stu-id="b66b9-220">LoadId</span></span> | <span data-ttu-id="b66b9-221">WHSMobileAppStepLoadId</span><span class="sxs-lookup"><span data-stu-id="b66b9-221">WHSMobileAppStepLoadId</span></span> |
| <span data-ttu-id="b66b9-222">LocationLicensePlatePosition</span><span class="sxs-lookup"><span data-stu-id="b66b9-222">LocationLicensePlatePosition</span></span> | <span data-ttu-id="b66b9-223">WHSMobileAppStepLocationLicensePlatePosition</span><span class="sxs-lookup"><span data-stu-id="b66b9-223">WHSMobileAppStepLocationLicensePlatePosition</span></span> |
| <span data-ttu-id="b66b9-224">LocOrLP</span><span class="sxs-lookup"><span data-stu-id="b66b9-224">LocOrLP</span></span> | <span data-ttu-id="b66b9-225">WHSMobileAppStepLocOrLP</span><span class="sxs-lookup"><span data-stu-id="b66b9-225">WHSMobileAppStepLocOrLP</span></span> |
| <span data-ttu-id="b66b9-226">LocOrLP_From</span><span class="sxs-lookup"><span data-stu-id="b66b9-226">LocOrLP_From</span></span> | <span data-ttu-id="b66b9-227">WHSMobileAppStepLocOrLPFrom</span><span class="sxs-lookup"><span data-stu-id="b66b9-227">WHSMobileAppStepLocOrLPFrom</span></span> |
| <span data-ttu-id="b66b9-228">LocOrLP_To</span><span class="sxs-lookup"><span data-stu-id="b66b9-228">LocOrLP_To</span></span> | <span data-ttu-id="b66b9-229">WHSMobileAppStepLocOrLPTo</span><span class="sxs-lookup"><span data-stu-id="b66b9-229">WHSMobileAppStepLocOrLPTo</span></span> |
| <span data-ttu-id="b66b9-230">LocOrLPCheck</span><span class="sxs-lookup"><span data-stu-id="b66b9-230">LocOrLPCheck</span></span> | <span data-ttu-id="b66b9-231">WHSMobileAppStepLocOrLPCheck</span><span class="sxs-lookup"><span data-stu-id="b66b9-231">WHSMobileAppStepLocOrLPCheck</span></span> |
| <span data-ttu-id="b66b9-232">LocVerification</span><span class="sxs-lookup"><span data-stu-id="b66b9-232">LocVerification</span></span> | <span data-ttu-id="b66b9-233">WHSMobileAppStepLocVerification</span><span class="sxs-lookup"><span data-stu-id="b66b9-233">WHSMobileAppStepLocVerification</span></span> |
| <span data-ttu-id="b66b9-234">LPAdjustIn</span><span class="sxs-lookup"><span data-stu-id="b66b9-234">LPAdjustIn</span></span> | <span data-ttu-id="b66b9-235">WHSMobileAppStepLPAdjustIn</span><span class="sxs-lookup"><span data-stu-id="b66b9-235">WHSMobileAppStepLPAdjustIn</span></span> |
| <span data-ttu-id="b66b9-236">LPBreakChildLP</span><span class="sxs-lookup"><span data-stu-id="b66b9-236">LPBreakChildLP</span></span> | <span data-ttu-id="b66b9-237">WHSMobileAppStepLPBreakChildLP</span><span class="sxs-lookup"><span data-stu-id="b66b9-237">WHSMobileAppStepLPBreakChildLP</span></span> |
| <span data-ttu-id="b66b9-238">LPBreakParentLP</span><span class="sxs-lookup"><span data-stu-id="b66b9-238">LPBreakParentLP</span></span> | <span data-ttu-id="b66b9-239">WHSMobileAppStepLPBreakParentLP</span><span class="sxs-lookup"><span data-stu-id="b66b9-239">WHSMobileAppStepLPBreakParentLP</span></span> |
| <span data-ttu-id="b66b9-240">LPBuildChildLP</span><span class="sxs-lookup"><span data-stu-id="b66b9-240">LPBuildChildLP</span></span> | <span data-ttu-id="b66b9-241">WHSMobileAppStepLPBuildChildLP</span><span class="sxs-lookup"><span data-stu-id="b66b9-241">WHSMobileAppStepLPBuildChildLP</span></span> |
| <span data-ttu-id="b66b9-242">LPBuildParentLP</span><span class="sxs-lookup"><span data-stu-id="b66b9-242">LPBuildParentLP</span></span> | <span data-ttu-id="b66b9-243">WHSMobileAppStepLPBuildParentLP</span><span class="sxs-lookup"><span data-stu-id="b66b9-243">WHSMobileAppStepLPBuildParentLP</span></span> |
| <span data-ttu-id="b66b9-244">LPVerification</span><span class="sxs-lookup"><span data-stu-id="b66b9-244">LPVerification</span></span> | <span data-ttu-id="b66b9-245">WHSMobileAppStepLPVerification</span><span class="sxs-lookup"><span data-stu-id="b66b9-245">WHSMobileAppStepLPVerification</span></span> |
| <span data-ttu-id="b66b9-246">MergeContainerId</span><span class="sxs-lookup"><span data-stu-id="b66b9-246">MergeContainerId</span></span> | <span data-ttu-id="b66b9-247">WHSMobileAppStepMergeContainerId</span><span class="sxs-lookup"><span data-stu-id="b66b9-247">WHSMobileAppStepMergeContainerId</span></span> |
| <span data-ttu-id="b66b9-248">MixedLPLineNum</span><span class="sxs-lookup"><span data-stu-id="b66b9-248">MixedLPLineNum</span></span> | <span data-ttu-id="b66b9-249">WHSMobileAppStepMixedLPLineNum</span><span class="sxs-lookup"><span data-stu-id="b66b9-249">WHSMobileAppStepMixedLPLineNum</span></span> |
| <span data-ttu-id="b66b9-250">MobileDeviceQueueMessageCollectionIdentifierId</span><span class="sxs-lookup"><span data-stu-id="b66b9-250">MobileDeviceQueueMessageCollectionIdentifierId</span></span> | <span data-ttu-id="b66b9-251">WHSMobileAppStepSelectOrder</span><span class="sxs-lookup"><span data-stu-id="b66b9-251">WHSMobileAppStepSelectOrder</span></span> |
| <span data-ttu-id="b66b9-252">MovementConfirmCancel</span><span class="sxs-lookup"><span data-stu-id="b66b9-252">MovementConfirmCancel</span></span> | <span data-ttu-id="b66b9-253">WHSMobileAppStepMovementConfirmCancel</span><span class="sxs-lookup"><span data-stu-id="b66b9-253">WHSMobileAppStepMovementConfirmCancel</span></span> |
| <span data-ttu-id="b66b9-254">NewCaptureWeight</span><span class="sxs-lookup"><span data-stu-id="b66b9-254">NewCaptureWeight</span></span> | <span data-ttu-id="b66b9-255">WHSMobileAppStepCatchWeight</span><span class="sxs-lookup"><span data-stu-id="b66b9-255">WHSMobileAppStepCatchWeight</span></span> |
| <span data-ttu-id="b66b9-256">NewQty</span><span class="sxs-lookup"><span data-stu-id="b66b9-256">NewQty</span></span> | <span data-ttu-id="b66b9-257">WHSMobileAppStepNewQty</span><span class="sxs-lookup"><span data-stu-id="b66b9-257">WHSMobileAppStepNewQty</span></span> |
| <span data-ttu-id="b66b9-258">OutboundCatchWeightTag</span><span class="sxs-lookup"><span data-stu-id="b66b9-258">OutboundCatchWeightTag</span></span> | <span data-ttu-id="b66b9-259">WHSMobileAppStepCatchWeightTag</span><span class="sxs-lookup"><span data-stu-id="b66b9-259">WHSMobileAppStepCatchWeightTag</span></span> |
| <span data-ttu-id="b66b9-260">OutboundPut</span><span class="sxs-lookup"><span data-stu-id="b66b9-260">OutboundPut</span></span> | <span data-ttu-id="b66b9-261">WHSMobileAppStepOutboundPut</span><span class="sxs-lookup"><span data-stu-id="b66b9-261">WHSMobileAppStepOutboundPut</span></span> |
| <span data-ttu-id="b66b9-262">OutboundWeight</span><span class="sxs-lookup"><span data-stu-id="b66b9-262">OutboundWeight</span></span> | <span data-ttu-id="b66b9-263">WHSMobileAppStepCatchWeight</span><span class="sxs-lookup"><span data-stu-id="b66b9-263">WHSMobileAppStepCatchWeight</span></span> |
| <span data-ttu-id="b66b9-264">OverridePutNewLocation</span><span class="sxs-lookup"><span data-stu-id="b66b9-264">OverridePutNewLocation</span></span> | <span data-ttu-id="b66b9-265">WHSMobileAppStepOverridePutNewLocation</span><span class="sxs-lookup"><span data-stu-id="b66b9-265">WHSMobileAppStepOverridePutNewLocation</span></span> |
| <span data-ttu-id="b66b9-266">PieceByPieceConfirmation</span><span class="sxs-lookup"><span data-stu-id="b66b9-266">PieceByPieceConfirmation</span></span> | <span data-ttu-id="b66b9-267">WHSMobileAppStepQtyVerification</span><span class="sxs-lookup"><span data-stu-id="b66b9-267">WHSMobileAppStepQtyVerification</span></span> |
| <span data-ttu-id="b66b9-268">POLineNum</span><span class="sxs-lookup"><span data-stu-id="b66b9-268">POLineNum</span></span> | <span data-ttu-id="b66b9-269">WHSMobileAppStepPOLineNum</span><span class="sxs-lookup"><span data-stu-id="b66b9-269">WHSMobileAppStepPOLineNum</span></span> |
| <span data-ttu-id="b66b9-270">采购订单编号</span><span class="sxs-lookup"><span data-stu-id="b66b9-270">PONum</span></span> | <span data-ttu-id="b66b9-271">WHSMobileAppStepPONum</span><span class="sxs-lookup"><span data-stu-id="b66b9-271">WHSMobileAppStepPONum</span></span> |
| <span data-ttu-id="b66b9-272">PositionFull</span><span class="sxs-lookup"><span data-stu-id="b66b9-272">PositionFull</span></span> | <span data-ttu-id="b66b9-273">WHSMobileAppStepPositionFull</span><span class="sxs-lookup"><span data-stu-id="b66b9-273">WHSMobileAppStepPositionFull</span></span> |
| <span data-ttu-id="b66b9-274">PositionFullQty</span><span class="sxs-lookup"><span data-stu-id="b66b9-274">PositionFullQty</span></span> | <span data-ttu-id="b66b9-275">WHSMobileAppStepPositionFullQty</span><span class="sxs-lookup"><span data-stu-id="b66b9-275">WHSMobileAppStepPositionFullQty</span></span> |
| <span data-ttu-id="b66b9-276">含量</span><span class="sxs-lookup"><span data-stu-id="b66b9-276">Potency</span></span> | <span data-ttu-id="b66b9-277">WHSMobileAppStepPotency</span><span class="sxs-lookup"><span data-stu-id="b66b9-277">WHSMobileAppStepPotency</span></span> |
| <span data-ttu-id="b66b9-278">PrinterName</span><span class="sxs-lookup"><span data-stu-id="b66b9-278">PrinterName</span></span> | <span data-ttu-id="b66b9-279">WHSMobileAppStepPrinterName</span><span class="sxs-lookup"><span data-stu-id="b66b9-279">WHSMobileAppStepPrinterName</span></span> |
| <span data-ttu-id="b66b9-280">ProdId</span><span class="sxs-lookup"><span data-stu-id="b66b9-280">ProdId</span></span> | <span data-ttu-id="b66b9-281">WHSMobileAppStepProdId</span><span class="sxs-lookup"><span data-stu-id="b66b9-281">WHSMobileAppStepProdId</span></span> |
| <span data-ttu-id="b66b9-282">ProdLastPalletConfirmation</span><span class="sxs-lookup"><span data-stu-id="b66b9-282">ProdLastPalletConfirmation</span></span> | <span data-ttu-id="b66b9-283">WHSMobileAppStepProdLastPalletConfirmation</span><span class="sxs-lookup"><span data-stu-id="b66b9-283">WHSMobileAppStepProdLastPalletConfirmation</span></span> |
| <span data-ttu-id="b66b9-284">ProductConfirmation</span><span class="sxs-lookup"><span data-stu-id="b66b9-284">ProductConfirmation</span></span> | <span data-ttu-id="b66b9-285">WHSMobileAppStepProductConfirmation</span><span class="sxs-lookup"><span data-stu-id="b66b9-285">WHSMobileAppStepProductConfirmation</span></span> |
| <span data-ttu-id="b66b9-286">ProductionScrapConfirmation</span><span class="sxs-lookup"><span data-stu-id="b66b9-286">ProductionScrapConfirmation</span></span> | <span data-ttu-id="b66b9-287">WHSMobileAppStepProductionScrapConfirmation</span><span class="sxs-lookup"><span data-stu-id="b66b9-287">WHSMobileAppStepProductionScrapConfirmation</span></span> |
| <span data-ttu-id="b66b9-288">放入</span><span class="sxs-lookup"><span data-stu-id="b66b9-288">Put</span></span> | <span data-ttu-id="b66b9-289">WHSMobileAppStepPut</span><span class="sxs-lookup"><span data-stu-id="b66b9-289">WHSMobileAppStepPut</span></span> |
| <span data-ttu-id="b66b9-290">PutawayClusterId</span><span class="sxs-lookup"><span data-stu-id="b66b9-290">PutawayClusterId</span></span> | <span data-ttu-id="b66b9-291">WHSMobileAppStepPutawayClusterId</span><span class="sxs-lookup"><span data-stu-id="b66b9-291">WHSMobileAppStepPutawayClusterId</span></span> |
| <span data-ttu-id="b66b9-292">数量</span><span class="sxs-lookup"><span data-stu-id="b66b9-292">Qty</span></span> | <span data-ttu-id="b66b9-293">WHSMobileAppStepQty</span><span class="sxs-lookup"><span data-stu-id="b66b9-293">WHSMobileAppStepQty</span></span> |
| <span data-ttu-id="b66b9-294">QtyAdjust</span><span class="sxs-lookup"><span data-stu-id="b66b9-294">QtyAdjust</span></span> | <span data-ttu-id="b66b9-295">WHSMobileAppStepQtyAdjust</span><span class="sxs-lookup"><span data-stu-id="b66b9-295">WHSMobileAppStepQtyAdjust</span></span> |
| <span data-ttu-id="b66b9-296">QtyShort</span><span class="sxs-lookup"><span data-stu-id="b66b9-296">QtyShort</span></span> | <span data-ttu-id="b66b9-297">WHSMobileAppStepQtyShort</span><span class="sxs-lookup"><span data-stu-id="b66b9-297">WHSMobileAppStepQtyShort</span></span> |
| <span data-ttu-id="b66b9-298">QtyToConsume</span><span class="sxs-lookup"><span data-stu-id="b66b9-298">QtyToConsume</span></span> | <span data-ttu-id="b66b9-299">WHSMobileAppStepQtyToConsume</span><span class="sxs-lookup"><span data-stu-id="b66b9-299">WHSMobileAppStepQtyToConsume</span></span> |
| <span data-ttu-id="b66b9-300">QtyToPick</span><span class="sxs-lookup"><span data-stu-id="b66b9-300">QtyToPick</span></span> | <span data-ttu-id="b66b9-301">WHSMobileAppStepQtyToPick</span><span class="sxs-lookup"><span data-stu-id="b66b9-301">WHSMobileAppStepQtyToPick</span></span> |
| <span data-ttu-id="b66b9-302">QtyToPut</span><span class="sxs-lookup"><span data-stu-id="b66b9-302">QtyToPut</span></span> | <span data-ttu-id="b66b9-303">WHSMobileAppStepQtyToPut</span><span class="sxs-lookup"><span data-stu-id="b66b9-303">WHSMobileAppStepQtyToPut</span></span> |
| <span data-ttu-id="b66b9-304">QtyToScrap</span><span class="sxs-lookup"><span data-stu-id="b66b9-304">QtyToScrap</span></span> | <span data-ttu-id="b66b9-305">WHSMobileAppStepQtyToScrap</span><span class="sxs-lookup"><span data-stu-id="b66b9-305">WHSMobileAppStepQtyToScrap</span></span> |
| <span data-ttu-id="b66b9-306">QtyVerification</span><span class="sxs-lookup"><span data-stu-id="b66b9-306">QtyVerification</span></span> | <span data-ttu-id="b66b9-307">WHSMobileAppStepQtyVerification</span><span class="sxs-lookup"><span data-stu-id="b66b9-307">WHSMobileAppStepQtyVerification</span></span> |
| <span data-ttu-id="b66b9-308">QtyWithScanningLimit</span><span class="sxs-lookup"><span data-stu-id="b66b9-308">QtyWithScanningLimit</span></span> | <span data-ttu-id="b66b9-309">WHSMobileAppStepQtyAdjust</span><span class="sxs-lookup"><span data-stu-id="b66b9-309">WHSMobileAppStepQtyAdjust</span></span> |
| <span data-ttu-id="b66b9-310">ReasonString</span><span class="sxs-lookup"><span data-stu-id="b66b9-310">ReasonString</span></span> | <span data-ttu-id="b66b9-311">WHSMobileAppStepReasonString</span><span class="sxs-lookup"><span data-stu-id="b66b9-311">WHSMobileAppStepReasonString</span></span> |
| <span data-ttu-id="b66b9-312">RecvLocationId</span><span class="sxs-lookup"><span data-stu-id="b66b9-312">RecvLocationId</span></span> | <span data-ttu-id="b66b9-313">WHSMobileAppStepRecvLocationId</span><span class="sxs-lookup"><span data-stu-id="b66b9-313">WHSMobileAppStepRecvLocationId</span></span> |
| <span data-ttu-id="b66b9-314">RemoveContainerId</span><span class="sxs-lookup"><span data-stu-id="b66b9-314">RemoveContainerId</span></span> | <span data-ttu-id="b66b9-315">WHSMobileAppStepRemoveContainerId</span><span class="sxs-lookup"><span data-stu-id="b66b9-315">WHSMobileAppStepRemoveContainerId</span></span> |
| <span data-ttu-id="b66b9-316">ReprintLabelConfirmation</span><span class="sxs-lookup"><span data-stu-id="b66b9-316">ReprintLabelConfirmation</span></span> | <span data-ttu-id="b66b9-317">WHSMobileAppStepReprintLabelConfirmation</span><span class="sxs-lookup"><span data-stu-id="b66b9-317">WHSMobileAppStepReprintLabelConfirmation</span></span> |
| <span data-ttu-id="b66b9-318">RMANum</span><span class="sxs-lookup"><span data-stu-id="b66b9-318">RMANum</span></span> | <span data-ttu-id="b66b9-319">WHSMobileAppStepRMANum</span><span class="sxs-lookup"><span data-stu-id="b66b9-319">WHSMobileAppStepRMANum</span></span> |
| <span data-ttu-id="b66b9-320">ShortPickReason</span><span class="sxs-lookup"><span data-stu-id="b66b9-320">ShortPickReason</span></span> | <span data-ttu-id="b66b9-321">WHSMobileAppStepShortPickReason</span><span class="sxs-lookup"><span data-stu-id="b66b9-321">WHSMobileAppStepShortPickReason</span></span> |
| <span data-ttu-id="b66b9-322">SortConOrLP</span><span class="sxs-lookup"><span data-stu-id="b66b9-322">SortConOrLP</span></span> | <span data-ttu-id="b66b9-323">WHSMobileAppStepSortConOrLP</span><span class="sxs-lookup"><span data-stu-id="b66b9-323">WHSMobileAppStepSortConOrLP</span></span> |
| <span data-ttu-id="b66b9-324">SortLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="b66b9-324">SortLicensePlateId</span></span> | <span data-ttu-id="b66b9-325">WHSMobileAppStepSortLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="b66b9-325">WHSMobileAppStepSortLicensePlateId</span></span> |
| <span data-ttu-id="b66b9-326">SortPositionId</span><span class="sxs-lookup"><span data-stu-id="b66b9-326">SortPositionId</span></span> | <span data-ttu-id="b66b9-327">WHSMobileAppStepSortPositionId</span><span class="sxs-lookup"><span data-stu-id="b66b9-327">WHSMobileAppStepSortPositionId</span></span> |
| <span data-ttu-id="b66b9-328">SortVerification</span><span class="sxs-lookup"><span data-stu-id="b66b9-328">SortVerification</span></span> | <span data-ttu-id="b66b9-329">WHSMobileAppStepSortVerification</span><span class="sxs-lookup"><span data-stu-id="b66b9-329">WHSMobileAppStepSortVerification</span></span> |
| <span data-ttu-id="b66b9-330">StartLocationId</span><span class="sxs-lookup"><span data-stu-id="b66b9-330">StartLocationId</span></span> | <span data-ttu-id="b66b9-331">WHSMobileAppStepStartLocationId</span><span class="sxs-lookup"><span data-stu-id="b66b9-331">WHSMobileAppStepStartLocationId</span></span> |
| <span data-ttu-id="b66b9-332">StartProdOrderConfirmation</span><span class="sxs-lookup"><span data-stu-id="b66b9-332">StartProdOrderConfirmation</span></span> | <span data-ttu-id="b66b9-333">WHSMobileAppStepStartProdOrderConfirmation</span><span class="sxs-lookup"><span data-stu-id="b66b9-333">WHSMobileAppStepStartProdOrderConfirmation</span></span> |
| <span data-ttu-id="b66b9-334">TargetLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="b66b9-334">TargetLicensePlateId</span></span> | <span data-ttu-id="b66b9-335">WHSMobileAppStepTargetLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="b66b9-335">WHSMobileAppStepTargetLicensePlateId</span></span> |
| <span data-ttu-id="b66b9-336">TOLineNum</span><span class="sxs-lookup"><span data-stu-id="b66b9-336">TOLineNum</span></span> | <span data-ttu-id="b66b9-337">WHSMobileAppStepTOLineNum</span><span class="sxs-lookup"><span data-stu-id="b66b9-337">WHSMobileAppStepTOLineNum</span></span> |
| <span data-ttu-id="b66b9-338">ToLocation</span><span class="sxs-lookup"><span data-stu-id="b66b9-338">ToLocation</span></span> | <span data-ttu-id="b66b9-339">WHSMobileAppStepToLocation</span><span class="sxs-lookup"><span data-stu-id="b66b9-339">WHSMobileAppStepToLocation</span></span> |
| <span data-ttu-id="b66b9-340">转移订单编号</span><span class="sxs-lookup"><span data-stu-id="b66b9-340">TONum</span></span> | <span data-ttu-id="b66b9-341">WHSMobileAppStepTONum</span><span class="sxs-lookup"><span data-stu-id="b66b9-341">WHSMobileAppStepTONum</span></span> |
| <span data-ttu-id="b66b9-342">ToWarehouse</span><span class="sxs-lookup"><span data-stu-id="b66b9-342">ToWarehouse</span></span> | <span data-ttu-id="b66b9-343">WHSMobileAppStepWarehouseTo</span><span class="sxs-lookup"><span data-stu-id="b66b9-343">WHSMobileAppStepWarehouseTo</span></span> |
| <span data-ttu-id="b66b9-344">TransportLoadId</span><span class="sxs-lookup"><span data-stu-id="b66b9-344">TransportLoadId</span></span> | <span data-ttu-id="b66b9-345">WHSMobileAppStepTransportLoadId</span><span class="sxs-lookup"><span data-stu-id="b66b9-345">WHSMobileAppStepTransportLoadId</span></span> |
| <span data-ttu-id="b66b9-346">WaveLabelId</span><span class="sxs-lookup"><span data-stu-id="b66b9-346">WaveLabelId</span></span> | <span data-ttu-id="b66b9-347">WHSMobileAppStepWaveLabelId</span><span class="sxs-lookup"><span data-stu-id="b66b9-347">WHSMobileAppStepWaveLabelId</span></span> |
| <span data-ttu-id="b66b9-348">WaveLblQty</span><span class="sxs-lookup"><span data-stu-id="b66b9-348">WaveLblQty</span></span> | <span data-ttu-id="b66b9-349">WHSMobileAppStepWaveLblQty</span><span class="sxs-lookup"><span data-stu-id="b66b9-349">WHSMobileAppStepWaveLblQty</span></span> |
| <span data-ttu-id="b66b9-350">权重</span><span class="sxs-lookup"><span data-stu-id="b66b9-350">Weight</span></span> | <span data-ttu-id="b66b9-351">WHSMobileAppStepWeight</span><span class="sxs-lookup"><span data-stu-id="b66b9-351">WHSMobileAppStepWeight</span></span> |
| <span data-ttu-id="b66b9-352">WeightToConsume</span><span class="sxs-lookup"><span data-stu-id="b66b9-352">WeightToConsume</span></span> | <span data-ttu-id="b66b9-353">WHSMobileAppStepWeightToConsume</span><span class="sxs-lookup"><span data-stu-id="b66b9-353">WHSMobileAppStepWeightToConsume</span></span> |
| <span data-ttu-id="b66b9-354">WHSAdjustmentType</span><span class="sxs-lookup"><span data-stu-id="b66b9-354">WHSAdjustmentType</span></span> | <span data-ttu-id="b66b9-355">WHSMobileAppStepWHSAdjustmentType</span><span class="sxs-lookup"><span data-stu-id="b66b9-355">WHSMobileAppStepWHSAdjustmentType</span></span> |
| <span data-ttu-id="b66b9-356">WHSReceivingException</span><span class="sxs-lookup"><span data-stu-id="b66b9-356">WHSReceivingException</span></span> | <span data-ttu-id="b66b9-357">WHSMobileAppStepWHSReceivingException</span><span class="sxs-lookup"><span data-stu-id="b66b9-357">WHSMobileAppStepWHSReceivingException</span></span> |
| <span data-ttu-id="b66b9-358">WHSWorkException</span><span class="sxs-lookup"><span data-stu-id="b66b9-358">WHSWorkException</span></span> | <span data-ttu-id="b66b9-359">WHSMobileAppStepWHSWorkException</span><span class="sxs-lookup"><span data-stu-id="b66b9-359">WHSMobileAppStepWHSWorkException</span></span> |
| <span data-ttu-id="b66b9-360">WHSWorkLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="b66b9-360">WHSWorkLicensePlateId</span></span> | <span data-ttu-id="b66b9-361">WHSMobileAppStepWorkLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="b66b9-361">WHSMobileAppStepWorkLicensePlateId</span></span> |
| <span data-ttu-id="b66b9-362">WMSLocationId</span><span class="sxs-lookup"><span data-stu-id="b66b9-362">WMSLocationId</span></span> | <span data-ttu-id="b66b9-363">WHSMobileAppStepLocation</span><span class="sxs-lookup"><span data-stu-id="b66b9-363">WHSMobileAppStepLocation</span></span> |
| <span data-ttu-id="b66b9-364">WorkId</span><span class="sxs-lookup"><span data-stu-id="b66b9-364">WorkId</span></span> | <span data-ttu-id="b66b9-365">WHSMobileAppStepWorkId</span><span class="sxs-lookup"><span data-stu-id="b66b9-365">WHSMobileAppStepWorkId</span></span> |
| <span data-ttu-id="b66b9-366">WorkIdToCancel</span><span class="sxs-lookup"><span data-stu-id="b66b9-366">WorkIdToCancel</span></span> | <span data-ttu-id="b66b9-367">WHSMobileAppStepWorkIdToCancel</span><span class="sxs-lookup"><span data-stu-id="b66b9-367">WHSMobileAppStepWorkIdToCancel</span></span> |
| <span data-ttu-id="b66b9-368">WorkLPIdPutawayCluster</span><span class="sxs-lookup"><span data-stu-id="b66b9-368">WorkLPIdPutawayCluster</span></span> | <span data-ttu-id="b66b9-369">WHSMobileAppStepWorkLPIdPutawayCluster</span><span class="sxs-lookup"><span data-stu-id="b66b9-369">WHSMobileAppStepWorkLPIdPutawayCluster</span></span> |
| <span data-ttu-id="b66b9-370">WorkPoolId</span><span class="sxs-lookup"><span data-stu-id="b66b9-370">WorkPoolId</span></span> | <span data-ttu-id="b66b9-371">WHSMobileAppStepWorkPoolId</span><span class="sxs-lookup"><span data-stu-id="b66b9-371">WHSMobileAppStepWorkPoolId</span></span> |
| <span data-ttu-id="b66b9-372">ZoneId</span><span class="sxs-lookup"><span data-stu-id="b66b9-372">ZoneId</span></span> | <span data-ttu-id="b66b9-373">WHSMobileAppStepZoneId</span><span class="sxs-lookup"><span data-stu-id="b66b9-373">WHSMobileAppStepZoneId</span></span> |

### <a name="available-step-icons"></a><a name="step-icons"></a><span data-ttu-id="b66b9-374">可用步骤图标</span><span class="sxs-lookup"><span data-stu-id="b66b9-374">Available step icons</span></span>

<span data-ttu-id="b66b9-375">系统包括标准步骤图标的集合，您也可以将其用于自定义步骤。</span><span class="sxs-lookup"><span data-stu-id="b66b9-375">The system includes a collection of standard step icons that you can also use for your custom steps.</span></span> <span data-ttu-id="b66b9-376">目前无法上载自定义步骤图标。</span><span class="sxs-lookup"><span data-stu-id="b66b9-376">You can't currently upload custom step icons.</span></span> <span data-ttu-id="b66b9-377">因此，您必须始终选择其中一个标准步骤图标。</span><span class="sxs-lookup"><span data-stu-id="b66b9-377">Therefore, you must always select one of the standard step icons.</span></span>

<span data-ttu-id="b66b9-378">下表显示了当前可用的每个标准步骤图标及其名称。</span><span class="sxs-lookup"><span data-stu-id="b66b9-378">The following table shows every standard step icon that is currently available, and its name.</span></span>

<table>
<tbody>
<tr>
<td><img src="media/step-icons-about.png" alt="About step icon" title="关于步骤图标"><br><span data-ttu-id="b66b9-380">关于</span><span class="sxs-lookup"><span data-stu-id="b66b9-380">About</span></span></td>
<td><img src="media/step-icons-add-lp.png" alt="Add license plate or item step icon" title="添加牌照或物料步骤图标"><br><span data-ttu-id="b66b9-382">AddLpOrItem</span><span class="sxs-lookup"><span data-stu-id="b66b9-382">AddLpOrItem</span></span></td>
<td><img src="media/step-icons-batch-disposition.png" alt="Batch disposition step icon" title="批处置步骤图标"><br><span data-ttu-id="b66b9-384">BatchDisposition</span><span class="sxs-lookup"><span data-stu-id="b66b9-384">BatchDisposition</span></span></td>
<td><img src="media/step-icons-carrier.png" alt="Carrier step icon" title="承运人步骤图标"><br><span data-ttu-id="b66b9-386">承运人</span><span class="sxs-lookup"><span data-stu-id="b66b9-386">Carrier</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-cw-tag.png" alt="Catch weight tag step icon" title="实际称重标记步骤图标"><br><span data-ttu-id="b66b9-388">CatchWeightTag</span><span class="sxs-lookup"><span data-stu-id="b66b9-388">CatchWeightTag</span></span></td>
<td><img src="media/step-icons-cw-tag-weight.png" alt="Catch weight tag weight step icon" title="实际称重标记重量步骤图标"><br><span data-ttu-id="b66b9-390">CatchWeightTagWeight</span><span class="sxs-lookup"><span data-stu-id="b66b9-390">CatchWeightTagWeight</span></span></td>
<td><img src="media/step-icons-check-digit.png" alt="Check digit step icon" title="校验位步骤图标"><br><span data-ttu-id="b66b9-392">CheckDigit</span><span class="sxs-lookup"><span data-stu-id="b66b9-392">CheckDigit</span></span></td>
<td><img src="media/step-icons-check-in-out.png" alt="Check in or out ID step icon" title="签入或签出 ID 步骤图标"><br><span data-ttu-id="b66b9-394">CheckInOutId</span><span class="sxs-lookup"><span data-stu-id="b66b9-394">CheckInOutId</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-child-lp.png" alt="Child license plate step icon" title="子牌照步骤图标"><br><span data-ttu-id="b66b9-396">ChildLP</span><span class="sxs-lookup"><span data-stu-id="b66b9-396">ChildLP</span></span></td>
<td><img src="media/step-icons-cluster-id.png" alt="Cluster ID step icon" title="群集 ID 步骤图标"><br><span data-ttu-id="b66b9-398">ClusterId</span><span class="sxs-lookup"><span data-stu-id="b66b9-398">ClusterId</span></span></td>
<td><img src="media/step-icons-cluster-position.png" alt="Cluster position step icon" title="群集位置步骤图标"><br><span data-ttu-id="b66b9-400">ClusterPosition</span><span class="sxs-lookup"><span data-stu-id="b66b9-400">ClusterPosition</span></span></td>
<td><img src="media/step-icons-config-id.png" alt="Config ID step icon" title="配置 ID 步骤图标"><br><span data-ttu-id="b66b9-402">ConfigId</span><span class="sxs-lookup"><span data-stu-id="b66b9-402">ConfigId</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-configured-field.png" alt="Configured field step icon" title="已配置字段步骤图标"><br><span data-ttu-id="b66b9-404">ConfiguredField</span><span class="sxs-lookup"><span data-stu-id="b66b9-404">ConfiguredField</span></span></td>
<td><img src="media/step-icons-con-lp.png" alt="Con or LP step icon" title="集装箱或牌照步骤图标"><br><span data-ttu-id="b66b9-406">ConOrLP</span><span class="sxs-lookup"><span data-stu-id="b66b9-406">ConOrLP</span></span></td>
<td><img src="media/step-icons-consolidate-from-LP.png" alt="Consolidate from license plate ID step icon" title="从牌照 ID 合并步骤图标"><br><span data-ttu-id="b66b9-408">ConsolidateFromLicensePlateID</span><span class="sxs-lookup"><span data-stu-id="b66b9-408">ConsolidateFromLicensePlateID</span></span></td>
<td><img src="media/step-icons-consolidate-to-LP.png" alt="Consolidate to license plate ID step icon" title="合并到牌照 ID 步骤图标"><br><span data-ttu-id="b66b9-410">ConsolidateToLicensePlateID</span><span class="sxs-lookup"><span data-stu-id="b66b9-410">ConsolidateToLicensePlateID</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-container-type.png" alt="Container type step icon" title="集装箱类型步骤图标"><br><span data-ttu-id="b66b9-412">ContainerType</span><span class="sxs-lookup"><span data-stu-id="b66b9-412">ContainerType</span></span></td>
<td><img src="media/step-icons-counting.png" alt="Counting step icon" title="盘点步骤图标"><br><span data-ttu-id="b66b9-414">盘点</span><span class="sxs-lookup"><span data-stu-id="b66b9-414">Counting</span></span></td>
<td><img src="media/step-icons-counting-reason.png" alt="Counting reason code step icon" title="盘点原因代码步骤图标"><br><span data-ttu-id="b66b9-416">CountingReasonCode</span><span class="sxs-lookup"><span data-stu-id="b66b9-416">CountingReasonCode</span></span></td>
<td><img src="media/step-icons-country-origin.png" alt="Country of origin code step icon" title="原产国家/地区代码步骤图标"><br><span data-ttu-id="b66b9-418">CountryOfOrigin</span><span class="sxs-lookup"><span data-stu-id="b66b9-418">CountryOfOrigin</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-disposition.png" alt="Disposition step icon" title="处置步骤图标"><br><span data-ttu-id="b66b9-420">Disposition</span><span class="sxs-lookup"><span data-stu-id="b66b9-420">Disposition</span></span></td>
<td><img src="media/step-icons-done.png" alt="Done step icon" title="完成步骤图标"><br><span data-ttu-id="b66b9-422">已完成</span><span class="sxs-lookup"><span data-stu-id="b66b9-422">Done</span></span></td>
<td><img src="media/step-icons-driver-check-in-confirmation.png" alt="Driver check in confirmation step icon" title="驾驶员签入确认步骤图标"><br><span data-ttu-id="b66b9-424">DriverCheckInConfirmation</span><span class="sxs-lookup"><span data-stu-id="b66b9-424">DriverCheckInConfirmation</span></span></td>
<td><img src="media/step-icons-driver-check-in-id.png" alt="Driver check in ID step icon" title="驾驶员签入 ID 步骤图标"><br><span data-ttu-id="b66b9-426">DriverCheckInId</span><span class="sxs-lookup"><span data-stu-id="b66b9-426">DriverCheckInId</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-driver-check-out-id.png" alt="Driver check out ID step icon" title="驾驶员签出 ID 步骤图标"><br><span data-ttu-id="b66b9-428">DriverCheckOutId</span><span class="sxs-lookup"><span data-stu-id="b66b9-428">DriverCheckOutId</span></span></td>
<td><img src="media/step-icons-exp-date.png" alt="Expiration date step icon" title="到期日期步骤图标"><br><span data-ttu-id="b66b9-430">ExpDate</span><span class="sxs-lookup"><span data-stu-id="b66b9-430">ExpDate</span></span></td>
<td><img src="media/step-icons-field.png" alt="Field step icon" title="字段步骤图标"><br><span data-ttu-id="b66b9-432">字段</span><span class="sxs-lookup"><span data-stu-id="b66b9-432">Field</span></span></td>
<td><img src="media/step-icons-from-batch.png" alt="From batch disposition step icon" title="从批处置步骤图标"><br><span data-ttu-id="b66b9-434">FromBatchDisposition</span><span class="sxs-lookup"><span data-stu-id="b66b9-434">FromBatchDisposition</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-from-inventory-status.png" alt="From inventory status step icon" title="从库存状态步骤图标"><br><span data-ttu-id="b66b9-436">FromInventoryStatus</span><span class="sxs-lookup"><span data-stu-id="b66b9-436">FromInventoryStatus</span></span></td>
<td><img src="media/step-icons-id-attribute.png" alt="ID attribute step icon" title="ID 属性步骤图标"><br><span data-ttu-id="b66b9-438">IdAttribute</span><span class="sxs-lookup"><span data-stu-id="b66b9-438">IdAttribute</span></span></td>
<td><img src="media/step-icons-invent-batch-id.png" alt="Inventory batch ID step icon" title="库存批处理 ID 步骤图标"><br><span data-ttu-id="b66b9-440">InventBatchID</span><span class="sxs-lookup"><span data-stu-id="b66b9-440">InventBatchID</span></span></td>
<td><img src="media/step-icons-invent-color-id.png" alt="Inventory color ID step icon" title="库存颜色 ID 步骤图标"><br><span data-ttu-id="b66b9-442">InventColorID</span><span class="sxs-lookup"><span data-stu-id="b66b9-442">InventColorID</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-invent-location.png" alt="Inventory location step icon" title="库存位置 ID 步骤图标"><br><span data-ttu-id="b66b9-444">InventLocation</span><span class="sxs-lookup"><span data-stu-id="b66b9-444">InventLocation</span></span></td>
<td><img src="media/step-icons-invent-serial-id.png" alt="Inventory serial ID step icon" title="库存序列 ID 步骤图标"><br><span data-ttu-id="b66b9-446">InventSerialID</span><span class="sxs-lookup"><span data-stu-id="b66b9-446">InventSerialID</span></span></td>
<td><img src="media/step-icons-invent-size-id.png" alt="Inventory size ID step icon" title="库存尺寸 ID 步骤图标"><br><span data-ttu-id="b66b9-448">InventSizeID</span><span class="sxs-lookup"><span data-stu-id="b66b9-448">InventSizeID</span></span></td>
<td><img src="media/step-icons-invent-status-id.png" alt="Inventory status ID step icon" title="库存状态 ID 步骤图标"><br><span data-ttu-id="b66b9-450">InventStatusID</span><span class="sxs-lookup"><span data-stu-id="b66b9-450">InventStatusID</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-invent-style-id.png" alt="Inventory style ID step icon" title="库存样式 ID 步骤图标"><br><span data-ttu-id="b66b9-452">InventStyleID</span><span class="sxs-lookup"><span data-stu-id="b66b9-452">InventStyleID</span></span></td>
<td><img src="media/step-icons-invent-version-id.png" alt="Inventory version ID step icon" title="库存版本 ID 步骤图标"><br><span data-ttu-id="b66b9-454">InventVersionID</span><span class="sxs-lookup"><span data-stu-id="b66b9-454">InventVersionID</span></span></td>
<td><img src="media/step-icons-item-id.png" alt="Item ID step icon" title="物料 ID 步骤图标"><br><span data-ttu-id="b66b9-456">ItemID</span><span class="sxs-lookup"><span data-stu-id="b66b9-456">ItemID</span></span></td>
<td><img src="media/step-icons-itm-contianer-id.png" alt="ITM container ID step icon" title="ITM 集装箱 ID 步骤图标"><br><span data-ttu-id="b66b9-458">ITMContainerID</span><span class="sxs-lookup"><span data-stu-id="b66b9-458">ITMContainerID</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-itm-shipment-id.png" alt="ITM shipment ID step icon" title="ITM 装运 ID 步骤图标"><br><span data-ttu-id="b66b9-460">ITMShipmentID</span><span class="sxs-lookup"><span data-stu-id="b66b9-460">ITMShipmentID</span></span></td>
<td><img src="media/step-icons-kanban-card-id.png" alt="Kanban card ID step icon" title="看板卡 ID 步骤图标"><br><span data-ttu-id="b66b9-462">KanbanCardID</span><span class="sxs-lookup"><span data-stu-id="b66b9-462">KanbanCardID</span></span></td>
<td><img src="media/step-icons-kanban-or-card-id.png" alt="Kanban or card ID step icon" title="看板或卡 ID 步骤图标"><br><span data-ttu-id="b66b9-464">KanbanOrCardID</span><span class="sxs-lookup"><span data-stu-id="b66b9-464">KanbanOrCardID</span></span></td>
<td><img src="media/step-icons-license-plate-id.png" alt="License plate ID step icon" title="牌照 ID 步骤图标"><br><span data-ttu-id="b66b9-466">LicensePlateID</span><span class="sxs-lookup"><span data-stu-id="b66b9-466">LicensePlateID</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-load-id.png" alt="Load ID step icon" title="负荷 ID 步骤图标"><br><span data-ttu-id="b66b9-468">LoadId</span><span class="sxs-lookup"><span data-stu-id="b66b9-468">LoadId</span></span></td>
<td><img src="media/step-icons-location-lp-pos.png" alt="Location license plate position step icon" title="位置牌照位置步骤图标"><br><span data-ttu-id="b66b9-470">LocationLicensePlatePosition</span><span class="sxs-lookup"><span data-stu-id="b66b9-470">LocationLicensePlatePosition</span></span></td>
<td><img src="media/step-icons-location-or-lp.png" alt="Location or license plate step icon" title="位置或牌照步骤图标"><br><span data-ttu-id="b66b9-472">LocOrLP</span><span class="sxs-lookup"><span data-stu-id="b66b9-472">LocOrLP</span></span></td>
<td><img src="media/step-icons-location-or-lp-check.png" alt="Location or license plate check step icon" title="位置或牌照检查步骤图标"><br><span data-ttu-id="b66b9-474">LocOrLPCheck</span><span class="sxs-lookup"><span data-stu-id="b66b9-474">LocOrLPCheck</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-location-or-lp-from.png" alt="Location or license plate from step icon" title="源位置或牌照步骤图标"><br><span data-ttu-id="b66b9-476">LocOrLPFrom</span><span class="sxs-lookup"><span data-stu-id="b66b9-476">LocOrLPFrom</span></span></td>
<td><img src="media/step-icons-location-or-lp-to.png" alt="Location or license plate to step icon" title="目标位置或牌照步骤图标"><br><span data-ttu-id="b66b9-478">LocOrLPTo</span><span class="sxs-lookup"><span data-stu-id="b66b9-478">LocOrLPTo</span></span></td>
<td><img src="media/step-icons-long-process-complete.png" alt="Long process completed step icon" title="长流程已完成步骤图标"><br><span data-ttu-id="b66b9-480">LongProcessCompleted</span><span class="sxs-lookup"><span data-stu-id="b66b9-480">LongProcessCompleted</span></span></td>
<td><img src="media/step-icons-lp-break-parent.png" alt="LP break parent LP step icon" title="牌照中断父牌照步骤图标"><br><span data-ttu-id="b66b9-482">LPBreakParentLP</span><span class="sxs-lookup"><span data-stu-id="b66b9-482">LPBreakParentLP</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-merge-container.png" alt="Merge container ID step icon" title="合并集装箱 ID 步骤图标"><br><span data-ttu-id="b66b9-484">MergeContainerId</span><span class="sxs-lookup"><span data-stu-id="b66b9-484">MergeContainerId</span></span></td>
<td><img src="media/step-icons-mixed-lp-line.png" alt="Mixed license plate line number step icon" title="混合牌照行编号步骤图标"><br><span data-ttu-id="b66b9-486">MixedLPLineNum</span><span class="sxs-lookup"><span data-stu-id="b66b9-486">MixedLPLineNum</span></span></td>
<td><img src="media/step-icons-outbound-weight.png" alt="Outbound weight step icon" title="出库重量步骤图标"><br><span data-ttu-id="b66b9-488">OutboundWeight</span><span class="sxs-lookup"><span data-stu-id="b66b9-488">OutboundWeight</span></span></td>
<td><img src="media/step-icons-owner.png" alt="Owner step icon" title="负责人步骤图标"><br><span data-ttu-id="b66b9-490">负责人</span><span class="sxs-lookup"><span data-stu-id="b66b9-490">Owner</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-parent-lp.png" alt="Parent license plate step icon" title="父牌照步骤图标"><br><span data-ttu-id="b66b9-492">ParentLP</span><span class="sxs-lookup"><span data-stu-id="b66b9-492">ParentLP</span></span></td>
<td><img src="media/step-icons-please-confirm.png" alt="Please confirm step icon" title="请确认步骤图标"><br><span data-ttu-id="b66b9-494">PleaseConfirm</span><span class="sxs-lookup"><span data-stu-id="b66b9-494">PleaseConfirm</span></span></td>
<td><img src="media/step-icons-po-line-num.png" alt="Purchase order line number step icon" title="采购订单行编号步骤图标"><br><span data-ttu-id="b66b9-496">POLineNum</span><span class="sxs-lookup"><span data-stu-id="b66b9-496">POLineNum</span></span></td>
<td><img src="media/step-icons-po-num.png" alt="Purchase order number step icon" title="采购订单编号步骤图标"><br><span data-ttu-id="b66b9-498">采购订单编号</span><span class="sxs-lookup"><span data-stu-id="b66b9-498">PONum</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-position-full.png" alt="Position full step icon" title="位置已满步骤图标"><br><span data-ttu-id="b66b9-500">PositionFull</span><span class="sxs-lookup"><span data-stu-id="b66b9-500">PositionFull</span></span></td>
<td><img src="media/step-icons-potency.png" alt="Potency step icon" title="含量步骤图标"><br><span data-ttu-id="b66b9-502">含量</span><span class="sxs-lookup"><span data-stu-id="b66b9-502">Potency</span></span></td>
<td><img src="media/step-icons-printer-name.png" alt="Printer name step icon" title="打印机名称步骤图标"><br><span data-ttu-id="b66b9-504">PrinterName</span><span class="sxs-lookup"><span data-stu-id="b66b9-504">PrinterName</span></span></td>
<td><img src="media/step-icons-prod-id.png" alt="Prod ID step icon" title="生产 ID 步骤图标"><br><span data-ttu-id="b66b9-506">ProdId</span><span class="sxs-lookup"><span data-stu-id="b66b9-506">ProdId</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-product-confirm.png" alt="Product confirmation step icon" title="产品确认步骤图标"><br><span data-ttu-id="b66b9-508">ProductConfirmation</span><span class="sxs-lookup"><span data-stu-id="b66b9-508">ProductConfirmation</span></span></td>
<td><img src="media/step-icons-put.png" alt="Put step icon" title="放置步骤图标"><br><span data-ttu-id="b66b9-510">放入</span><span class="sxs-lookup"><span data-stu-id="b66b9-510">Put</span></span></td>
<td><img src="media/step-icons-putaway-cluster-id.png" alt="Putaway cluster ID step icon" title="储存群集 ID 步骤图标"><br><span data-ttu-id="b66b9-512">PutawayClusterId</span><span class="sxs-lookup"><span data-stu-id="b66b9-512">PutawayClusterId</span></span></td>
<td><img src="media/step-icons-qty.png" alt="Quantity step icon" title="数量步骤图标"><br><span data-ttu-id="b66b9-514">数量</span><span class="sxs-lookup"><span data-stu-id="b66b9-514">Qty</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-qty-adjust-in.png" alt="Quantity adjust in step icon" title="数量调整步骤图标"><br><span data-ttu-id="b66b9-516">QtyAdjustIn</span><span class="sxs-lookup"><span data-stu-id="b66b9-516">QtyAdjustIn</span></span></td>
<td><img src="media/step-icons-qty-short.png" alt="Quantity short step icon" title="数量短缺步骤图标"><br><span data-ttu-id="b66b9-518">QtyShort</span><span class="sxs-lookup"><span data-stu-id="b66b9-518">QtyShort</span></span></td>
<td><img src="media/step-icons-qty-to-consume.png" alt="Quantity to consume step icon" title="要消耗的数量步骤图标"><br><span data-ttu-id="b66b9-520">QtyToConsume</span><span class="sxs-lookup"><span data-stu-id="b66b9-520">QtyToConsume</span></span></td>
<td><img src="media/step-icons-qty-to-put.png" alt="Quantity to put step icon" title="要放置的数量步骤图标"><br><span data-ttu-id="b66b9-522">QtyToPut</span><span class="sxs-lookup"><span data-stu-id="b66b9-522">QtyToPut</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-qty-to-scrap.png" alt="Quantity to scrap step icon" title="要报废的数量步骤图标"><br><span data-ttu-id="b66b9-524">QtyToScrap</span><span class="sxs-lookup"><span data-stu-id="b66b9-524">QtyToScrap</span></span></td>
<td><img src="media/step-icons-qty-confirmation.png" alt="Quantity confirmation step icon" title="数量确认步骤图标"><br><span data-ttu-id="b66b9-526">QuantityConfirmation</span><span class="sxs-lookup"><span data-stu-id="b66b9-526">QuantityConfirmation</span></span></td>
<td><img src="media/step-icons-raf-end-job.png" alt="Report as finished end job step icon" title="报告为完工入库结束作业步骤图标"><br><span data-ttu-id="b66b9-528">RAFEndJob</span><span class="sxs-lookup"><span data-stu-id="b66b9-528">RAFEndJob</span></span></td>
<td><img src="media/step-icons-recv-loc-id.png" alt="Receive location ID step icon" title="接收位置 ID 步骤图标"><br><span data-ttu-id="b66b9-530">RecvLocationID</span><span class="sxs-lookup"><span data-stu-id="b66b9-530">RecvLocationID</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-remove-container-id.png" alt="Remove container ID step icon" title="删除集装箱 ID 步骤图标"><br><span data-ttu-id="b66b9-532">RemoveContainerID</span><span class="sxs-lookup"><span data-stu-id="b66b9-532">RemoveContainerID</span></span></td>
<td><img src="media/step-icons-rma-no.png" alt="RMA number step icon" title="RMA 编号步骤图标"><br><span data-ttu-id="b66b9-534">RMANum</span><span class="sxs-lookup"><span data-stu-id="b66b9-534">RMANum</span></span></td>
<td><img src="media/step-icons-select-order.png" alt="Select order step icon" title="选择订单步骤图标"><br><span data-ttu-id="b66b9-536">SelectOrder</span><span class="sxs-lookup"><span data-stu-id="b66b9-536">SelectOrder</span></span></td>
<td><img src="media/step-icons-short-pick-reason.png" alt="Short pick reason step icon" title="领料短缺原因步骤图标"><br><span data-ttu-id="b66b9-538">ShortPickReason</span><span class="sxs-lookup"><span data-stu-id="b66b9-538">ShortPickReason</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-sort-position-id.png" alt="Sort position ID step icon" title="分类位置 ID 步骤图标"><br><span data-ttu-id="b66b9-540">SortPositionId</span><span class="sxs-lookup"><span data-stu-id="b66b9-540">SortPositionId</span></span></td>
<td><img src="media/step-icons-target-lp-id.png" alt="Target license plate ID step icon" title="目标牌照 ID 步骤图标"><br><span data-ttu-id="b66b9-542">TargetLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="b66b9-542">TargetLicensePlateId</span></span></td>
<td><img src="media/step-icons-to-line-no.png" alt="To line number step icon" title="目标行号步骤图标"><br><span data-ttu-id="b66b9-544">ToLineNum</span><span class="sxs-lookup"><span data-stu-id="b66b9-544">ToLineNum</span></span></td>
<td><img src="media/step-icons-to-location.png" alt="To location step icon" title="目标位置步骤图标"><br><span data-ttu-id="b66b9-546">ToLocation</span><span class="sxs-lookup"><span data-stu-id="b66b9-546">ToLocation</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-to-number.png" alt="To number step icon" title="目标编号步骤图标"><br><span data-ttu-id="b66b9-548">ToNum</span><span class="sxs-lookup"><span data-stu-id="b66b9-548">ToNum</span></span></td>
<td><img src="media/step-icons-to-warehouse.png" alt="To warehouse step icon" title="目标仓库步骤图标"><br><span data-ttu-id="b66b9-550">ToWarehouse</span><span class="sxs-lookup"><span data-stu-id="b66b9-550">ToWarehouse</span></span></td>
<td><img src="media/step-icons-tranport-load-id.png" alt="Transport load ID step icon" title="运输负荷 ID 步骤图标"><br><span data-ttu-id="b66b9-552">TransportLoadId</span><span class="sxs-lookup"><span data-stu-id="b66b9-552">TransportLoadId</span></span></td>
<td><img src="media/step-icons-vendor-batch-id.png" alt="Vendor batch ID step icon" title="供应商批处理 ID 步骤图标"><br><span data-ttu-id="b66b9-554">VendBatchId</span><span class="sxs-lookup"><span data-stu-id="b66b9-554">VendBatchId</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-wave-label-id.png" alt="Wave label ID step icon" title="波次标签 ID 步骤图标"><br><span data-ttu-id="b66b9-556">WaveLabelId</span><span class="sxs-lookup"><span data-stu-id="b66b9-556">WaveLabelId</span></span></td>
<td><img src="media/step-icons-wave-label-qty.png" alt="Wave label quantity step icon" title="波次标签数量步骤图标"><br><span data-ttu-id="b66b9-558">WaveLblQty</span><span class="sxs-lookup"><span data-stu-id="b66b9-558">WaveLblQty</span></span></td>
<td><img src="media/step-icons-weight.png" alt="Weight step icon" title="重量步骤图标"><br><span data-ttu-id="b66b9-560">权重</span><span class="sxs-lookup"><span data-stu-id="b66b9-560">Weight</span></span></td>
<td><img src="media/step-icons-weight-to-consume.png" alt="Weight to consume step icon" title="要消耗的重量步骤图标"><br><span data-ttu-id="b66b9-562">WeightToConsume</span><span class="sxs-lookup"><span data-stu-id="b66b9-562">WeightToConsume</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-whs-adjustment-type.png" alt="WHS adjustment type step icon" title="WHS 调整类型步骤图标"><br><span data-ttu-id="b66b9-564">WHSAdjustmentType</span><span class="sxs-lookup"><span data-stu-id="b66b9-564">WHSAdjustmentType</span></span></td>
<td><img src="media/step-icons-whs-receiving-exception.png" alt="WHS receiving exception step icon" title="WHS 接收例外步骤图标"><br><span data-ttu-id="b66b9-566">WHSReceivingException</span><span class="sxs-lookup"><span data-stu-id="b66b9-566">WHSReceivingException</span></span></td>
<td><img src="media/step-icons-wms-location-id.png" alt="WMS location ID step icon" title="WMS 位置 ID 步骤图标"><br><span data-ttu-id="b66b9-568">WMSLocationID</span><span class="sxs-lookup"><span data-stu-id="b66b9-568">WMSLocationID</span></span></td>
<td><img src="media/step-icons-work-id.png" alt="Work ID step icon" title="工作 ID 步骤图标"><br><span data-ttu-id="b66b9-570">WorkId</span><span class="sxs-lookup"><span data-stu-id="b66b9-570">WorkId</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-work-id-to-cancel.png" alt="Work ID to cancel step icon" title="要取消的工作 ID 步骤图标"><br><span data-ttu-id="b66b9-572">WorkIdToCancel</span><span class="sxs-lookup"><span data-stu-id="b66b9-572">WorkIdToCancel</span></span></td>
<td><img src="media/step-icons-work-lp-id.png" alt="Work license plate ID step icon" title="工作牌照 ID 步骤图标"><br><span data-ttu-id="b66b9-574">WorkLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="b66b9-574">WorkLicensePlateId</span></span></td>
<td><img src="media/step-icons-work-lp-putaway-cluster.png" alt="Work license plate ID putaway cluster step icon" title="工作牌照 ID 储存群集步骤图标"><br><span data-ttu-id="b66b9-576">WorkLPIDPutawayCluster</span><span class="sxs-lookup"><span data-stu-id="b66b9-576">WorkLPIDPutawayCluster</span></span></td>
<td><img src="media/step-icons-work-pool-id.png" alt="Work pool ID step icon" title="工作池 ID 步骤图标"><br><span data-ttu-id="b66b9-578">WorkPoolID</span><span class="sxs-lookup"><span data-stu-id="b66b9-578">WorkPoolID</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-zone-pool-id.png" alt="Zone ID step icon" title="区域 ID 步骤图标"><br><span data-ttu-id="b66b9-580">ZoneID</span><span class="sxs-lookup"><span data-stu-id="b66b9-580">ZoneID</span></span></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

## <a name="example-assign-step-icons-and-titles-for-a-custom-flow"></a><a name="example"></a><span data-ttu-id="b66b9-581">示例：为自定义流分配步骤图标和标题</span><span class="sxs-lookup"><span data-stu-id="b66b9-581">Example: Assign step icons and titles for a custom flow</span></span>

<span data-ttu-id="b66b9-582">此示例说明如何为自定义任务流设置步骤图标和标题。</span><span class="sxs-lookup"><span data-stu-id="b66b9-582">This example explains how to set up step icons and titles for a custom task flow.</span></span> <span data-ttu-id="b66b9-583">场景基于一个自定义任务流的示例建立，该流在以下博客文章中进行了更详细地演示和探索：[自定义 Warehousing Mobile App](https://cloudblogs.microsoft.com/dynamics365/it/2017/07/06/customizing-the-warehousing-mobile-app)。</span><span class="sxs-lookup"><span data-stu-id="b66b9-583">The scenario is built on an example of a custom task flow that is presented and explored in more detail in the following blog post: [Customizing the Warehousing Mobile App](https://cloudblogs.microsoft.com/dynamics365/it/2017/07/06/customizing-the-warehousing-mobile-app).</span></span> <span data-ttu-id="b66b9-584">此任务流按以下方式工作：</span><span class="sxs-lookup"><span data-stu-id="b66b9-584">The task flow works in the following way:</span></span>

1. <span data-ttu-id="b66b9-585">应用显示一个页面，提示工作人员提供集装箱 ID（例如，通过扫描条码）。</span><span class="sxs-lookup"><span data-stu-id="b66b9-585">The app shows a page that prompts the worker to provide a container ID (for example, by scanning a bar code).</span></span>
1. <span data-ttu-id="b66b9-586">如果集装箱 ID 有效，应用会打开一个新页面，提示工作人员输入重量。</span><span class="sxs-lookup"><span data-stu-id="b66b9-586">If the container ID is valid, the app opens a new page that prompts the worker for the weight.</span></span> <span data-ttu-id="b66b9-587">（如果集装箱 ID 无效，工作人员将返回到第一页。）</span><span class="sxs-lookup"><span data-stu-id="b66b9-587">(If the container ID isn't valid, the worker is returned to the first page.)</span></span>
1. <span data-ttu-id="b66b9-588">当工作人员输入有效重量时，系统将存储该重量并将工作人员返回到第一页。</span><span class="sxs-lookup"><span data-stu-id="b66b9-588">When the worker enters a valid weight, the system stores the weight and returns the worker to the first page.</span></span>

<span data-ttu-id="b66b9-589">下图显示了此任务流。</span><span class="sxs-lookup"><span data-stu-id="b66b9-589">The following illustration shows this task flow.</span></span>

<span data-ttu-id="b66b9-590">![任务流图](media/step-icons-example-task-flow.png "任务流图")</span><span class="sxs-lookup"><span data-stu-id="b66b9-590">![Task flow diagram](media/step-icons-example-task-flow.png "Task flow diagram")</span></span>

### <a name="create-a-step-class-for-the-container-input-page"></a><span data-ttu-id="b66b9-591">为集装箱输入页面创建步骤类</span><span class="sxs-lookup"><span data-stu-id="b66b9-591">Create a step class for the container input page</span></span>

<span data-ttu-id="b66b9-592">通过集装箱输入页面，工作人员可以扫描或输入集装箱 ID。</span><span class="sxs-lookup"><span data-stu-id="b66b9-592">The container input page lets the worker scan or enter a container ID.</span></span>

<span data-ttu-id="b66b9-593">![集装箱输入页面](media/step-icons-example-container-input.png "集装箱输入页面")</span><span class="sxs-lookup"><span data-stu-id="b66b9-593">![Container input page](media/step-icons-example-container-input.png "Container input page")</span></span>

<span data-ttu-id="b66b9-594">在集装箱输入页面上，输入字段的控件名称为 `ContainerId`。</span><span class="sxs-lookup"><span data-stu-id="b66b9-594">On the container input page, the control name of the input field is `ContainerId`.</span></span> <span data-ttu-id="b66b9-595">由于此控件名称不在[步骤 ID 列表](#step-ids-classes)中，所以您找不到基于它的现有步骤。</span><span class="sxs-lookup"><span data-stu-id="b66b9-595">Because this control name isn't in the [list of step IDs](#step-ids-classes), you won't find an existing step that is based on it.</span></span> <span data-ttu-id="b66b9-596">因此，您必须创建一个表示该步骤的步骤类。</span><span class="sxs-lookup"><span data-stu-id="b66b9-596">Therefore, you must create a step class that represents the step.</span></span> <span data-ttu-id="b66b9-597">下面是一个示例。</span><span class="sxs-lookup"><span data-stu-id="b66b9-597">Here is an example.</span></span>

```xpp
[WHSMobileAppStepId('ContainerId')]
final internal class WHSMobileAppStepContainerId extends WHSMobileAppStep
{
    private const WHSMobileAppStepIcon PopulationIcon = 'InventBatchID';
    private const WHSMobileAppStepTitle InputNotFilledTitle = "@WAX:WHSMobileAppStepContainerID_InputNotFilled"; //Scan a container
    protected void initValues()
    {
        defaultStepIcon = PopulationIcon;
        defaultStepTitle = InputNotFilledTitle;
    }
}
```

<span data-ttu-id="b66b9-598">步骤图标的标识符存储在 `defaultStepIcon` 类成员中，步骤标题存储在 `defaultStepTitle` 类成员中。</span><span class="sxs-lookup"><span data-stu-id="b66b9-598">The identifier of the step icon is stored in the `defaultStepIcon` class member, and the step title is stored in the `defaultStepTitle` class member.</span></span>

<span data-ttu-id="b66b9-599">要分配步骤图标，将 `defaultStepIcon` 设置为本主题前面[可用步骤图标](#step-icons)一节中列出的图标 ID 之一。</span><span class="sxs-lookup"><span data-stu-id="b66b9-599">To assign a step icon, set `defaultStepIcon` to one of the icon IDs that are listed in the [Available step icons](#step-icons) section earlier in this topic.</span></span>

### <a name="use-a-standard-or-custom-step-icon-and-title-for-the-weight-input"></a><span data-ttu-id="b66b9-600">为重量输入使用标准或自定义步骤图标和标题</span><span class="sxs-lookup"><span data-stu-id="b66b9-600">Use a standard or custom step icon and title for the weight input</span></span>

<span data-ttu-id="b66b9-601">重量输入页面让工作人员可以输入重量。</span><span class="sxs-lookup"><span data-stu-id="b66b9-601">The weight input page lets the worker enter a weight.</span></span>

<span data-ttu-id="b66b9-602">![重量输入页面](media/step-icons-example-weight-input.png "重量输入页面")</span><span class="sxs-lookup"><span data-stu-id="b66b9-602">![Weight input page](media/step-icons-example-weight-input.png "Weight input page")</span></span>

<span data-ttu-id="b66b9-603">在重量输入页面上，输入字段的控件名称为 `Weight`，在[步骤 ID 列表](#step-ids-classes)中。</span><span class="sxs-lookup"><span data-stu-id="b66b9-603">On the weight input page, the control name of the input field is `Weight`, which is in the [list of step IDs](#step-ids-classes).</span></span> <span data-ttu-id="b66b9-604">因此，如果您可以接受在 `WHSMobileAppStepWeight` 类中定义的步骤图标和标题，则无需为此步骤进行更改任何。</span><span class="sxs-lookup"><span data-stu-id="b66b9-604">Therefore, if the step icon and title that are defined in the `WHSMobileAppStepWeight` class are acceptable to you, you don't have to change anything for this step.</span></span>

<span data-ttu-id="b66b9-605">但是，如果您更倾向于在此步骤中使用不同的图标或标题，您可以替代构建器类中的 `stepId()` 方法或 `stepInfo()` 方法。</span><span class="sxs-lookup"><span data-stu-id="b66b9-605">However, if you prefer to use a different icon or title for this step, you can override either the `stepId()` method or the `stepInfo()` method in the builder class.</span></span> <span data-ttu-id="b66b9-606">每个任务流都有自己的步骤信息构建器。</span><span class="sxs-lookup"><span data-stu-id="b66b9-606">Each task flow has its own step info builder.</span></span>

#### <a name="override-the-stepid-method"></a><span data-ttu-id="b66b9-607">替代 stepId() 方法</span><span class="sxs-lookup"><span data-stu-id="b66b9-607">Override the stepId() method</span></span>

<span data-ttu-id="b66b9-608">以下示例显示了一种可以通过替代 `stepId()` 方法来修改构建器类的方法。</span><span class="sxs-lookup"><span data-stu-id="b66b9-608">The following example shows one way that you can modify a builder class by overriding the `stepId()` method.</span></span>

```xpp
[WHSWorkExecuteMode(WHSWorkExecuteMode:: WeighContainer)]
public class WHSMobileAppStepInfoBuilderWeighContainer extends WHSMobileAppStepInfoBuilder
{
    protected WHSMobileAppStepId stepId()
    {
        WHSMobileAppStepId stepIdLocal = super();
        if (stepIdLocal == 'Weight')
        {
            return 'NewWeight';
        }
        return stepIdLocal;
    }
}
```

<span data-ttu-id="b66b9-609">然后您将为 `NewWeight` 步骤创建一个步骤类。</span><span class="sxs-lookup"><span data-stu-id="b66b9-609">You then create a step class for the `NewWeight` step.</span></span> <span data-ttu-id="b66b9-610">代码应类似于本主题前面显示的 `ContainerId` 示例的代码。</span><span class="sxs-lookup"><span data-stu-id="b66b9-610">The code should resemble the code for the `ContainerId` example that was shown earlier in this topic.</span></span>

#### <a name="override-the-stepinfo-method"></a><span data-ttu-id="b66b9-611">替代 stepInfo() 方法</span><span class="sxs-lookup"><span data-stu-id="b66b9-611">Override the stepInfo() method</span></span>

<span data-ttu-id="b66b9-612">以下示例显示了一种可以通过替代 `stepInfo()` 方法来修改构建器类的方法。</span><span class="sxs-lookup"><span data-stu-id="b66b9-612">The following example shows one way that you can modify a builder class by overriding the `stepInfo()` method.</span></span>

```xpp
[WHSWorkExecuteMode(WHSWorkExecuteMode:: WeighContainer)]
public class WHSMobileAppStepInfoBuilderWeighContainer extends WHSMobileAppStepInfoBuilder
{
    protected WHSMobileAppStepInfo stepInfo()
    {
        if (stepId != 'Weight')
        {
            return super();
        }
        WHSMobileAppStepInfo stepInfo = WHSMobileAppStepInfo::construct();
        stepInfo.parmStepIcon('NewIcon');
        stepInfo.parmStepTitle('NewTitle');
        return stepInfo;
    }
}
```

<span data-ttu-id="b66b9-613">然后，您将构造一个 `WHSMobileAppStepInfo` 对象，并直接设置图标和/或标题。</span><span class="sxs-lookup"><span data-stu-id="b66b9-613">You then construct a `WHSMobileAppStepInfo` object, and set the icon and/or title directly.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b66b9-614">其他资源</span><span class="sxs-lookup"><span data-stu-id="b66b9-614">Additional resources</span></span>

- [<span data-ttu-id="b66b9-615">安装和连接仓库管理移动应用</span><span class="sxs-lookup"><span data-stu-id="b66b9-615">Install and connect the Warehouse Management mobile app</span></span>](install-configure-warehouse-management-app.md)
- [<span data-ttu-id="b66b9-616">移动设备用户设置</span><span class="sxs-lookup"><span data-stu-id="b66b9-616">Mobile device user settings</span></span>](mobile-device-user-settings.md)
