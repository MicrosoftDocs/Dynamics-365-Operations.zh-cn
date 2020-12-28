---
title: 仓库应用事件
description: 本主题介绍了作为批处理作业一部分的用于处理仓库应用事件消息的仓库应用事件处理。
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
ms.openlocfilehash: 210008c4a1366773f465c59b38eca30f11f0b38c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4422859"
---
# <a name="warehouse-app-event-processing"></a><span data-ttu-id="afc95-103">仓库应用事件处理</span><span class="sxs-lookup"><span data-stu-id="afc95-103">Warehouse app event processing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="afc95-104">在 Supply Chain Management 中运行的批处理作业可以使用队列中的数据来处理仓库应用发出的事件，以根据需要对发出信号的事件做出反应。</span><span class="sxs-lookup"><span data-stu-id="afc95-104">Batch jobs running in Supply Chain Management can use data from a queue for processing events issued by the warehouse app to react as needed to the signaled events.</span></span> <span data-ttu-id="afc95-105">此功能将相关事件添加到队列中，以响应工作人员使用该应用执行的某些类型的操作。</span><span class="sxs-lookup"><span data-stu-id="afc95-105">This feature add relevant events to the queue in response to certain types of actions taken by workers using the app.</span></span> <span data-ttu-id="afc95-106">例如，当使用 **通过仓库应用创建和处理转移单** 功能时，如果系统在运行 **处理仓库应用事件** 批处理作业，将在后端创建和更新转移单标题和行。</span><span class="sxs-lookup"><span data-stu-id="afc95-106">An example is when using the **Create and process transfer orders from the warehouse app** feature, the transfer order header and lines get created and updated in the back end when the system is running the **Process warehouse app events** batch job.</span></span>

## <a name="enable-the-process-warehouse-app-events-feature"></a><span data-ttu-id="afc95-107">启用处理仓库应用事件功能</span><span class="sxs-lookup"><span data-stu-id="afc95-107">Enable the Process warehouse app events feature</span></span>

<span data-ttu-id="afc95-108">此功能只有在系统中启用了之后才能使用。</span><span class="sxs-lookup"><span data-stu-id="afc95-108">Before you can use this feature, it must be enabled on your system.</span></span> <span data-ttu-id="afc95-109">管理员可以使用[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)页面检查功能状态，并在需要时启用。</span><span class="sxs-lookup"><span data-stu-id="afc95-109">Administrators can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) page to check the feature status and enable it if needed.</span></span> <span data-ttu-id="afc95-110">处理仓库应用事件功能列出为：</span><span class="sxs-lookup"><span data-stu-id="afc95-110">The Process warehouse app events feature is listed as:</span></span>

- <span data-ttu-id="afc95-111">**模块** - 仓库管理</span><span class="sxs-lookup"><span data-stu-id="afc95-111">**Module** - Warehouse management</span></span>
- <span data-ttu-id="afc95-112">**功能名称** - 处理仓库应用事件</span><span class="sxs-lookup"><span data-stu-id="afc95-112">**Feature name** - Process warehouse app events</span></span>

## <a name="set-up-a-batch-job-to-process-warehouse-app-events"></a><span data-ttu-id="afc95-113">设置批处理作业以处理仓库应用事件</span><span class="sxs-lookup"><span data-stu-id="afc95-113">Set up a batch job to process warehouse app events</span></span>

### <a name="process-warehouse-app-events"></a><span data-ttu-id="afc95-114">处理仓库应用事件</span><span class="sxs-lookup"><span data-stu-id="afc95-114">Process warehouse app events</span></span>

<span data-ttu-id="afc95-115">设置计划的批处理作业以处理用于转移单创建和行更新的仓库应用事件。</span><span class="sxs-lookup"><span data-stu-id="afc95-115">Set up a scheduled batch job to process the warehouse app events for the transfer order creation and line updates.</span></span>

1. <span data-ttu-id="afc95-116">转到 **仓库管理 \> 定期任务 \> 处理仓库应用事件**。</span><span class="sxs-lookup"><span data-stu-id="afc95-116">Go to **Warehouse management \> Periodic tasks \> Process warehouse app events**.</span></span>
1. <span data-ttu-id="afc95-117">“处理仓库应用事件”对话框将打开。</span><span class="sxs-lookup"><span data-stu-id="afc95-117">The Process warehouse app events dialog box opens.</span></span> <span data-ttu-id="afc95-118">展开 **在后台运行** 快速选项卡并将 **批处理** 设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="afc95-118">Expand the **Run in background** FastTab and set **Batch processing** to **Yes**.</span></span>
1. <span data-ttu-id="afc95-119">在 **在后台运行** 快速选项卡上，选择 **重复执行**。</span><span class="sxs-lookup"><span data-stu-id="afc95-119">On the **Run in the background** FastTab, select **Recurrence**.</span></span>
1. <span data-ttu-id="afc95-120">**定义重复执行** 对话框将打开。</span><span class="sxs-lookup"><span data-stu-id="afc95-120">The **Define recurrence** dialog box opens.</span></span> <span data-ttu-id="afc95-121">根据业务需要设置运行计划。</span><span class="sxs-lookup"><span data-stu-id="afc95-121">Set the run schedule as needed for your business.</span></span>
1. <span data-ttu-id="afc95-122">选择 **确定** 以返回到 **处理仓库应用事件** 对话框。</span><span class="sxs-lookup"><span data-stu-id="afc95-122">Select **OK** to return to the **Process warehouse app events** dialog box.</span></span>
1. <span data-ttu-id="afc95-123">在 **处理仓库应用事件** 对话框中选择 **确定**，将批处理作业添加到批处理队列中。</span><span class="sxs-lookup"><span data-stu-id="afc95-123">Select **OK** in the **Process warehouse app events** dialog box to add the batch job to the batch queue.</span></span>

## <a name="query-warehouse-app-events"></a><span data-ttu-id="afc95-124">查询仓库应用事件</span><span class="sxs-lookup"><span data-stu-id="afc95-124">Query warehouse app events</span></span>

<span data-ttu-id="afc95-125">您可以通过转到 **仓库管理 \> 查询和报表 \> 移动设备日志 \> 仓库应用事件** 查看仓库应用生成的事件队列和事件消息。</span><span class="sxs-lookup"><span data-stu-id="afc95-125">You can view the event queue and events messages generated by the warehouse app by going to **Warehouse management \> Inquiries and reports \> Mobile device logs \> Warehouse app events**.</span></span>

## <a name="the-standard-event-queue-process"></a><span data-ttu-id="afc95-126">标准事件队列流程</span><span class="sxs-lookup"><span data-stu-id="afc95-126">The standard event queue process</span></span>

<span data-ttu-id="afc95-127">仓库应用事件队列通常将与下面描述的流一起使用：</span><span class="sxs-lookup"><span data-stu-id="afc95-127">The warehouse apps events queue will typically be used with the following described flow:</span></span>

1. <span data-ttu-id="afc95-128">一个事件随事件消息一起添加到队列中。</span><span class="sxs-lookup"><span data-stu-id="afc95-128">An event gets added to the queue  with an event message.</span></span> <span data-ttu-id="afc95-129">新消息最初的事件状态为 **等待**，这意味着 **处理仓库应用事件** 批处理作业将不会接收并处理此消息。</span><span class="sxs-lookup"><span data-stu-id="afc95-129">The new message initially has an Event state of **Waiting**, which means that the **Process warehouse app events** batch job will not pick up and process this message.</span></span>
1. <span data-ttu-id="afc95-130">一旦消息状态更新为 **已排队**，**流程仓库应用** 事件批处理作业将会接收并处理事件。</span><span class="sxs-lookup"><span data-stu-id="afc95-130">As soon as the message state is updated to **Queued**, the **Process warehouse app** events batch job will pick up and process the event.</span></span>
1. <span data-ttu-id="afc95-131">批处理作业将事件状态更新为 **已完成** 或 **失败**，具体取决于请求的流程是否可行。</span><span class="sxs-lookup"><span data-stu-id="afc95-131">The batch job updates the event states to either **Completed** or **Failed**, depending on whether the requested process was possible.</span></span>
1. <span data-ttu-id="afc95-132">当所有相关事件消息都是 **已完成** 时，该事件将从队列中删除。</span><span class="sxs-lookup"><span data-stu-id="afc95-132">When all the related event messages are **Completed**, the event is deleted from the queue.</span></span>

 <span data-ttu-id="afc95-133">有关详细示例，请参阅[通过仓库应用创建转移单流程](create-transfer-order-from-warehouse-app.md)。</span><span class="sxs-lookup"><span data-stu-id="afc95-133">For a detailed example, see [Create transfer order from warehouse app process](create-transfer-order-from-warehouse-app.md).</span></span>

## <a name="handle-event-errors"></a><span data-ttu-id="afc95-134">处理事件错误</span><span class="sxs-lookup"><span data-stu-id="afc95-134">Handle event errors</span></span>

<span data-ttu-id="afc95-135">作为仓库事件处理的一部分，所请求的消息活动可能未从批处理作业接收流程。</span><span class="sxs-lookup"><span data-stu-id="afc95-135">As part of the warehouse event processing, the requested message activity may not receive processes from the batch job.</span></span> <span data-ttu-id="afc95-136">在这种情况下，事件消息将更改为 **失败**。</span><span class="sxs-lookup"><span data-stu-id="afc95-136">In this case, the event message will change to **Failed**.</span></span> <span data-ttu-id="afc95-137">您可以使用 **批处理日志** 信息以了解原因并采取必要的措施纠正任何问题。</span><span class="sxs-lookup"><span data-stu-id="afc95-137">You can use the **Batch log** information to learn why and take needed action to correct any problems.</span></span>

<span data-ttu-id="afc95-138">有关详细示例，请参阅[通过仓库应用创建转移单](create-transfer-order-from-warehouse-app.md)。</span><span class="sxs-lookup"><span data-stu-id="afc95-138">For a detailed example, see [Create transfer order from warehouse app](create-transfer-order-from-warehouse-app.md).</span></span>

<span data-ttu-id="afc95-139">若要重置失败的仓库应用事件消息：</span><span class="sxs-lookup"><span data-stu-id="afc95-139">To reset a failed warehouse app event message:</span></span>

1. <span data-ttu-id="afc95-140">转到 **仓库管理 \> 查询和报表 \> 移动设备日志 \> 仓库应用事件**。</span><span class="sxs-lookup"><span data-stu-id="afc95-140">Go to **Warehouse management \> Inquiries and reports \> Mobile device logs \> Warehouse app events**.</span></span>
1. <span data-ttu-id="afc95-141">在 **仓库应用事件消息** 快速选项卡上，找到并选择在 **事件状态** 列中显示 **失败** 的相关事件。</span><span class="sxs-lookup"><span data-stu-id="afc95-141">On the **Warehouse app event messages** FastTab, find and select a relevant event that is showing **Failed** in the **Event state** column.</span></span>
1. <span data-ttu-id="afc95-142">从 **仓库应用事件消息** 工具栏中选择 **重置**。</span><span class="sxs-lookup"><span data-stu-id="afc95-142">Select **Reset** from the **Warehouse app event messages** toolbar.</span></span>
1. <span data-ttu-id="afc95-143">继续工作，直到所有相关消息都已重置。</span><span class="sxs-lookup"><span data-stu-id="afc95-143">Continue working until all relevant messages are reset.</span></span>

<span data-ttu-id="afc95-144">您也可以通过使用 **仓库应用事件消息** 工具栏上的 **删除** 选项删除 **失败** 事件消息。</span><span class="sxs-lookup"><span data-stu-id="afc95-144">You can also remove a **Failed** event message by using the **Delete** option on the **Warehouse app event messages** toolbar.</span></span>
