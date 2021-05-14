---
title: 延期处理手动库存变动
description: 本主题介绍如何在 Microsoft Dynamics 365 Supply Chain Management 中使用延期处理手动库存变动。
author: Mirzaab
ms.date: 04/27/2021
ms.topic: article
ms.search.form: WHSWorkProcessingPolicy, WHSWorkDeferredPutProcessingTask
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: Mirzaab
ms.search.validFrom: 2021-04-27
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 54a202b7e6728bc83022851c901d3c5db17510bf
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956559"
---
# <a name="deferred-processing-of-manual-inventory-movement"></a><span data-ttu-id="47225-103">延期处理手动库存变动</span><span class="sxs-lookup"><span data-stu-id="47225-103">Deferred processing of manual inventory movement</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="47225-104">本主题介绍如何在 Microsoft Dynamics 365 Supply Chain Management 中使用延期处理手动库存变动。</span><span class="sxs-lookup"><span data-stu-id="47225-104">This topic describes how to use deferred processing of manual inventory movement in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="47225-105">延期处理让仓库工作人员可以在后台处理放置操作期间继续执行其他工作。</span><span class="sxs-lookup"><span data-stu-id="47225-105">Deferred processing lets warehouse workers continue to do other work while a put operation is processed in the background.</span></span> <span data-ttu-id="47225-106">当服务器的处理时间临时或意外增加，并且增加的处理时间可能影响工作人员的生产率时，延期处理非常有用。</span><span class="sxs-lookup"><span data-stu-id="47225-106">Deferred processing is useful when the server can have occasional or unplanned increases in processing time, and the increased processing time might affect worker productivity.</span></span> <span data-ttu-id="47225-107">*库存变动* 工作类型现已添加到此功能支持的工作类型集中。</span><span class="sxs-lookup"><span data-stu-id="47225-107">The *Inventory movement* work type has now been added to the set of work types that this feature supports.</span></span>

<span data-ttu-id="47225-108">后台处理通过使用[处理仓库应用事件功能](warehouse-app-events.md)实现。</span><span class="sxs-lookup"><span data-stu-id="47225-108">Background processing is achieved by using the [Process warehouse app events feature](warehouse-app-events.md).</span></span>

## <a name="turn-on-this-feature-for-your-system"></a><span data-ttu-id="47225-109">为您的系统启用此功能</span><span class="sxs-lookup"><span data-stu-id="47225-109">Turn on this feature for your system</span></span>

<span data-ttu-id="47225-110">若要使此功能可用，请在[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)中打开以下功能。</span><span class="sxs-lookup"><span data-stu-id="47225-110">To make this feature available, turn on the following features in [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span> <span data-ttu-id="47225-111">您必须按以下顺序打开它们：</span><span class="sxs-lookup"><span data-stu-id="47225-111">You must turn them on in this order:</span></span>

1. <span data-ttu-id="47225-112">组织范围内的工作阻止</span><span class="sxs-lookup"><span data-stu-id="47225-112">Organization-wide work blocking</span></span>
1. <span data-ttu-id="47225-113">处理仓库应用事件</span><span class="sxs-lookup"><span data-stu-id="47225-113">Process warehouse app events</span></span>
1. <span data-ttu-id="47225-114">延迟 PUT 操作</span><span class="sxs-lookup"><span data-stu-id="47225-114">Deferred put operations</span></span>
1. <span data-ttu-id="47225-115">延迟处理手动库存变动操作</span><span class="sxs-lookup"><span data-stu-id="47225-115">Deferred processing of manual inventory movement operation</span></span>

## <a name="configure-the-work-processing-policies"></a><span data-ttu-id="47225-116">配置工作处理策略</span><span class="sxs-lookup"><span data-stu-id="47225-116">Configure the work processing policies</span></span>

<span data-ttu-id="47225-117">若要使用推迟处理，必须设置并使用工作处理策略。</span><span class="sxs-lookup"><span data-stu-id="47225-117">To use deferred processing, you must set up and use a work processing policy.</span></span> <span data-ttu-id="47225-118">对于延期放置处理，[延期处理仓库工作功能](deferred-put.md)支持以下工作类型：*销售订单*、*转移单发货* 和 *补货*。</span><span class="sxs-lookup"><span data-stu-id="47225-118">For deferred put processing, the [Deferred processing of warehouse work feature](deferred-put.md) supports the following work types: *Sales order*, *Transfer order issue*, and *Replenishment*.</span></span> <span data-ttu-id="47225-119">*延期处理手动库存变动操作* 功能添加了新的工作类型：*库存变动*。</span><span class="sxs-lookup"><span data-stu-id="47225-119">The *Deferred processing of manual inventory movement operation* features adds a new work type: *Inventory movement*.</span></span>

<span data-ttu-id="47225-120">要设置工作处理策略，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="47225-120">To set up a work processing policy, follow these steps.</span></span>

1. <span data-ttu-id="47225-121">转到 **仓库管理 \> 设置 \> 工作 \> 工作处理策略**。</span><span class="sxs-lookup"><span data-stu-id="47225-121">Go to **Warehouse management \> Setup \> Work \> Work processing policies**.</span></span>
1. <span data-ttu-id="47225-122">在列表中选择一个现有策略，或者在操作窗格上选择 **新建** 创建一个新策略。</span><span class="sxs-lookup"><span data-stu-id="47225-122">Either select an existing policy in the list, or create a new policy by selecting **New** on the Action Pane.</span></span> <span data-ttu-id="47225-123">每个策略的标头都有以下字段：</span><span class="sxs-lookup"><span data-stu-id="47225-123">The header of every policy has the following fields:</span></span>

    - <span data-ttu-id="47225-124">**工作处理策略名称** – 工作处理策略的名称。</span><span class="sxs-lookup"><span data-stu-id="47225-124">**Work processing policy name** – The name of the work processing policy.</span></span>
    - <span data-ttu-id="47225-125">**描述** – 工作处理策略的描述。</span><span class="sxs-lookup"><span data-stu-id="47225-125">**Description** – A description of the work processing policy.</span></span>

1. <span data-ttu-id="47225-126">在 **处理规则** 快速选项卡上，设置将应用策略的规则集合。</span><span class="sxs-lookup"><span data-stu-id="47225-126">On the **Processing rules** FastTab, set up the collection of rules that the policy will apply.</span></span> <span data-ttu-id="47225-127">使用工具栏上的按钮可以根据需要添加或删除规则。</span><span class="sxs-lookup"><span data-stu-id="47225-127">Use the buttons on the toolbar to add or remove rules as you require.</span></span> <span data-ttu-id="47225-128">对于每个规则，设置以下字段：</span><span class="sxs-lookup"><span data-stu-id="47225-128">For each rule, set the following fields:</span></span>

    - <span data-ttu-id="47225-129">**工作订单类型** – 选择策略应用的工作类型。</span><span class="sxs-lookup"><span data-stu-id="47225-129">**Work order type** – Select the work type that the policy applies to.</span></span>
    - <span data-ttu-id="47225-130">**操作** – 选择策略用于处理的操作。</span><span class="sxs-lookup"><span data-stu-id="47225-130">**Operation** – Select the operation that the policy is used to process.</span></span> <span data-ttu-id="47225-131">如果您在 **工作订单类型** 字段中选择了 *库存变动*，则不必设置此字段，因为领料操作和放置操作都将作为单个事件处理。</span><span class="sxs-lookup"><span data-stu-id="47225-131">If you selected *Inventory movement* in the **Work order type** field, you don't have to set this field, because both pick operations and put operations are processed as a single event.</span></span>
    - <span data-ttu-id="47225-132">**工作处理方法** – 选择用于处理工作行的方法。</span><span class="sxs-lookup"><span data-stu-id="47225-132">**Work processing method** – Select the method that is used to process the work line.</span></span> <span data-ttu-id="47225-133">如果选择 *立即*，行为类似未使用任何工作处理策略来处理行时的行为。</span><span class="sxs-lookup"><span data-stu-id="47225-133">If you select *Immediate*, the behavior resembles the behavior when no work processing policies are used to process the line.</span></span> <span data-ttu-id="47225-134">如果选择 *延期*，系统将应用使用批处理框架的延期处理。</span><span class="sxs-lookup"><span data-stu-id="47225-134">If you select *Deferred*, the system will apply deferred processing that uses the batch framework.</span></span>
    - <span data-ttu-id="47225-135">**延期处理阈值** – 如果将此字段设置为 *0*（零），将没有阈值。</span><span class="sxs-lookup"><span data-stu-id="47225-135">**Deferred processing threshold** – If you set this field to *0* (zero), there is no threshold.</span></span> <span data-ttu-id="47225-136">在这种情况下，如果可能，会使用 *延期* 处理方法。</span><span class="sxs-lookup"><span data-stu-id="47225-136">In this case, the *Deferred* processing method is used if possible.</span></span> <span data-ttu-id="47225-137">如果阈值的具体计算结果低于阈值，则使用 *立即* 方法。</span><span class="sxs-lookup"><span data-stu-id="47225-137">If the specific threshold calculation is below the threshold, the *Immediate* method is used.</span></span> <span data-ttu-id="47225-138">否则，如果可能，则使用 *延期* 方法。</span><span class="sxs-lookup"><span data-stu-id="47225-138">Otherwise, the *Deferred* method is used if possible.</span></span> <span data-ttu-id="47225-139">对于与销售和运输有关的工作，计算出的阈值是正在为工作处理的关联源负荷行的数量。</span><span class="sxs-lookup"><span data-stu-id="47225-139">For sales and transfer-related work, the threshold is calculated as the number of associated source load lines that are being processed for the work.</span></span> <span data-ttu-id="47225-140">对于补货工作，计算出的阈值是工作正在补货的工作行的数量。</span><span class="sxs-lookup"><span data-stu-id="47225-140">For replenishment work, the threshold is calculated as the number of work lines that are being replenished by the work.</span></span> <span data-ttu-id="47225-141">例如，如果将销售的阈值设置为 *5*，您将确保初始源负荷行少于五个的较小工作不使用延期处理，但是大量工作则会使用。</span><span class="sxs-lookup"><span data-stu-id="47225-141">By setting a threshold of, for example, *5* for sales, you ensure that smaller works that have fewer than five initial source load lines won't use deferred processing, but larger works will use it.</span></span> <span data-ttu-id="47225-142">仅当 **工作处理方法** 字段设置为 *延期* 时，此阈值才有效。</span><span class="sxs-lookup"><span data-stu-id="47225-142">The threshold has an effect only if the **Work processing method** field is set to *Deferred*.</span></span>
    - <span data-ttu-id="47225-143">**延期处理批处理组** – 指定用于处理的批处理组。</span><span class="sxs-lookup"><span data-stu-id="47225-143">**Deferred processing batch group** – Specify the batch group that is used for processing.</span></span> <span data-ttu-id="47225-144">如果您在 **工作订单类型** 字段中选择了 *库存变动*，则不必设置此字段，因为已在 **处理仓库应用事件** 对话框中选择了批处理组。</span><span class="sxs-lookup"><span data-stu-id="47225-144">If you selected *Inventory movement* in the **Work order type** field, you don't have to set this field, because the batch group is selected in the **Process warehouse app events** dialog box.</span></span>

## <a name="assign-the-work-creation-policy"></a><span data-ttu-id="47225-145">分配工作创建策略</span><span class="sxs-lookup"><span data-stu-id="47225-145">Assign the work creation policy</span></span>

<span data-ttu-id="47225-146">有关如何分配作品创建策略的详细信息，请参阅[延期处理仓库工作](deferred-put.md)。</span><span class="sxs-lookup"><span data-stu-id="47225-146">For details about how to assign a work creation policy, see [Deferred processing of warehouse work](deferred-put.md).</span></span>

## <a name="set-up-a-batch-job-to-process-warehouse-app-events"></a><span data-ttu-id="47225-147">设置批处理作业以处理仓库应用事件</span><span class="sxs-lookup"><span data-stu-id="47225-147">Set up a batch job to process warehouse app events</span></span>

<span data-ttu-id="47225-148">要使用 *延期处理手动库存变动操作* 流程，需要设置计划的批处理作业。</span><span class="sxs-lookup"><span data-stu-id="47225-148">To use the *Deferred processing of manual inventory movement operation* process, set up a scheduled batch job.</span></span>

1. <span data-ttu-id="47225-149">转到 **仓库管理 \> 定期任务 \> 处理仓库应用事件**。</span><span class="sxs-lookup"><span data-stu-id="47225-149">Go to **Warehouse management \> Periodic tasks \> Process warehouse app events**.</span></span>
1. <span data-ttu-id="47225-150">在 **处理仓库应用事件** 对话框中，在 **在后台运行** 快速选项卡上，将 **批处理** 选项设置为 *是*。</span><span class="sxs-lookup"><span data-stu-id="47225-150">In the **Process warehouse app events** dialog box, on the **Run in background** FastTab, set the **Batch processing** option to *Yes*.</span></span>
1. <span data-ttu-id="47225-151">选择 **定期**，设置符合您的业务要求的运行计划。</span><span class="sxs-lookup"><span data-stu-id="47225-151">Select **Recurrence**, and set up a run schedule that meets the requirements of your business.</span></span>
1. <span data-ttu-id="47225-152">在每个对话框中选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="47225-152">Select **OK** in each dialog box.</span></span>

## <a name="inquire-about-the-warehouse-app-events"></a><span data-ttu-id="47225-153">查询仓库应用事件</span><span class="sxs-lookup"><span data-stu-id="47225-153">Inquire about the warehouse app events</span></span>

<span data-ttu-id="47225-154">您可以通过转到 **仓库管理 \> 查询和报表 \> 移动设备日志 \> 仓库应用事件** 查看仓库应用生成的事件队列和事件消息。</span><span class="sxs-lookup"><span data-stu-id="47225-154">You can view the event queue and event messages that the warehouse app generates by going to **Warehouse management \> Inquiries and reports \> Mobile device logs \> Warehouse app events**.</span></span>

<span data-ttu-id="47225-155">首次创建时，*库存变动* 事件消息的状态为 *已排队*。</span><span class="sxs-lookup"><span data-stu-id="47225-155">The *Inventory movement* event messages will have a status of *Queued* when they are first created.</span></span> <span data-ttu-id="47225-156">此状态指示 **处理仓库应用事件** 批处理作业将选取事件消息并进行处理。</span><span class="sxs-lookup"><span data-stu-id="47225-156">This status indicates that the **Process warehouse app events** batch job will pick up the event messages and process them.</span></span> <span data-ttu-id="47225-157">当状态更新为 *已完成* 时，所有相关事件将从队列中删除。</span><span class="sxs-lookup"><span data-stu-id="47225-157">When the status is updated to *Completed*, all the related events are deleted from the queue.</span></span>

<span data-ttu-id="47225-158">所有 *库存变动* 事件按事件类型和仓库在一个集合下累积。</span><span class="sxs-lookup"><span data-stu-id="47225-158">All the *Inventory movement* events are accumulated under one collection per event type and warehouse.</span></span>

<span data-ttu-id="47225-159">批处理作业将根据在 **处理仓库应用事件** 对话框中设置的定期处理仓库应用事件。</span><span class="sxs-lookup"><span data-stu-id="47225-159">The batch job will process the warehouse app events according to the recurrence that is set up in the **Process warehouse app events** dialog box.</span></span> <span data-ttu-id="47225-160">因此，在消息被处理之前，您可以通过在 **标识符** 字段中查找来查找仓库 ID。</span><span class="sxs-lookup"><span data-stu-id="47225-160">Therefore, until a message is processed, you can find the warehouse ID by looking in the **Identifier** field.</span></span>

<span data-ttu-id="47225-161">消息的详细信息包含变动详细信息（例如，“起始”和“目标”位置）。</span><span class="sxs-lookup"><span data-stu-id="47225-161">The details of the message contain the details of the movement (for example, the "from" and "to" locations).</span></span>

<span data-ttu-id="47225-162">有关详细信息，请参阅[仓库应用事件处理](warehouse-app-events.md)。</span><span class="sxs-lookup"><span data-stu-id="47225-162">For more information, see [Warehouse app event processing](warehouse-app-events.md).</span></span>

## <a name="configure-the-mobile-device-menu-to-skip-the-deferred-processing-policy"></a><span data-ttu-id="47225-163">配置移动设备菜单以跳过推迟处理策略</span><span class="sxs-lookup"><span data-stu-id="47225-163">Configure the mobile device menu to skip the deferred processing policy</span></span>

<span data-ttu-id="47225-164">有关如何配置移动设备菜单以跳过延期处理策略的详细信息，请参阅[延期处理仓库工作](deferred-put.md)。</span><span class="sxs-lookup"><span data-stu-id="47225-164">For details about how to configure the mobile device menu to skip the deferred processing policy, see [Deferred processing of warehouse work](deferred-put.md).</span></span>

## <a name="impact-on-closed-work-dates"></a><span data-ttu-id="47225-165">对工作关闭日期的影响</span><span class="sxs-lookup"><span data-stu-id="47225-165">Impact on closed work dates</span></span>

<span data-ttu-id="47225-166">有关对已关闭工作日期的影响的详细信息，请参阅[延期处理仓库工作](deferred-put.md)。</span><span class="sxs-lookup"><span data-stu-id="47225-166">For details about the impact on closed work dates, see [Deferred processing of warehouse work](deferred-put.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="47225-167">其他资源</span><span class="sxs-lookup"><span data-stu-id="47225-167">Additional resources</span></span>

- [<span data-ttu-id="47225-168">仓库工作延期处理</span><span class="sxs-lookup"><span data-stu-id="47225-168">Deferred processing of warehouse work</span></span>](deferred-put.md)
- [<span data-ttu-id="47225-169">仓库应用事件处理</span><span class="sxs-lookup"><span data-stu-id="47225-169">Warehouse app event processing</span></span>](warehouse-app-events.md)
- [<span data-ttu-id="47225-170">设置移动设备以执行仓库工作</span><span class="sxs-lookup"><span data-stu-id="47225-170">Set up mobile devices for warehouse work</span></span>](configure-mobile-devices-warehouse.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
