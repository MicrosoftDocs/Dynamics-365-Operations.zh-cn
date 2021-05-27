---
title: 物料处理设备接口 (MHAX)
description: 本主题介绍如何设置物料处理设备接口 (MHAX)，让您可以连接到外部物理物料处理 (MH) 系统。
author: Mirzaab
ms.date: 03/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WMHEParameters, WMHESubscription, WMHEQueueManagerWorkspace, WMHEInboundQueue, WMHEOutboundQueue
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-03-04
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 65c174896bbee07514285d4d19e1693c13dd9697
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021508"
---
# <a name="material-handling-equipment-interface-mhax"></a><span data-ttu-id="d661d-103">物料处理设备接口 (MHAX)</span><span class="sxs-lookup"><span data-stu-id="d661d-103">Material handling equipment interface (MHAX)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d661d-104">您可以使用 *物料处理设备接口* (MHAX) 将外部物理物料处理 (MH) 系统连接到由 Microsoft Dynamics 365 Supply Chain Management 中的高级仓库管理 (WMS) 管理的仓库。</span><span class="sxs-lookup"><span data-stu-id="d661d-104">You can use the *material handling equipment interface* (MHAX) to connect external physical material handling (MH) systems to a warehouse that is managed by advanced warehouse management (WMS) in Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="d661d-105">WMS 和 MH 系统之间的接口由两个队列组成：一个队列是出站事件（从 WMS 到 MH），另一个队列是入站事件（从 MH 到 WMS）。</span><span class="sxs-lookup"><span data-stu-id="d661d-105">The interface between the WMS and MH systems consists of two queues: one for outbound events (WMS to MH) and one for inbound events (MH to WMS).</span></span> <span data-ttu-id="d661d-106">WMS 系统基于在各个工作创建和执行流程中创建的工作行生成出站事件。</span><span class="sxs-lookup"><span data-stu-id="d661d-106">The WMS system generates outbound events based on work lines that are created during various work creation and execution processes.</span></span> <span data-ttu-id="d661d-107">然后，MH 系统会定期在 WMS 系统中轮询新事件并处理响应。</span><span class="sxs-lookup"><span data-stu-id="d661d-107">The MH system then regularly polls the WMS system for new events and processes the responses.</span></span> <span data-ttu-id="d661d-108">MH 系统按照工作说明完成事件处理后，将发送入站事件，如工作行完成和领料短缺。</span><span class="sxs-lookup"><span data-stu-id="d661d-108">After the MH system has finished handling the events in accordance with work instructions, it sends inbound events, such as work line completion and short picking.</span></span>

<span data-ttu-id="d661d-109">下图显示了使用 MHAX 集成时的各个元素以及流程发生的顺序。</span><span class="sxs-lookup"><span data-stu-id="d661d-109">The following illustration shows the various elements and the order that processes occur in when you use MHAX integration.</span></span>

<span data-ttu-id="d661d-110">![MHAX 组件和交互](media/mhax-components.png "MHAX 组件和交互")</span><span class="sxs-lookup"><span data-stu-id="d661d-110">![MHAX components and interactions](media/mhax-components.png "MHAX components and interactions")</span></span>

<span data-ttu-id="d661d-111">这是前图中所示的交互的说明：</span><span class="sxs-lookup"><span data-stu-id="d661d-111">Here is an explanation of the interactions that are shown in the previous illustration:</span></span>

1. <span data-ttu-id="d661d-112">在工作创建或工作执行期间，将在出站队列中创建出站事件。</span><span class="sxs-lookup"><span data-stu-id="d661d-112">During work creation or work execution, outbound events are created in the outbound queue.</span></span>
2. <span data-ttu-id="d661d-113">MH 设备连接到 MH 设备服务，轮询与之相关的任何新事件，并处理这些事件。</span><span class="sxs-lookup"><span data-stu-id="d661d-113">The MH equipment connects to the MH equipment service, polls for any new events that are relevant to it, and processes those events.</span></span>
3. <span data-ttu-id="d661d-114">当 MH 设备准备好进行报告时，它将再次连接到服务并提交入站事件。</span><span class="sxs-lookup"><span data-stu-id="d661d-114">When the MH equipment is ready to report back, it connects to the service again and submits inbound events.</span></span> <span data-ttu-id="d661d-115">这些事件将立即由队列处理器处理。</span><span class="sxs-lookup"><span data-stu-id="d661d-115">Those events are immediately processed by the queue processor.</span></span>
4. <span data-ttu-id="d661d-116">基于入站事件数据，队列处理器可以运行现有工作，对其进行修改或创建新工作。</span><span class="sxs-lookup"><span data-stu-id="d661d-116">Based on the inbound event data, the queue processor might run existing work, modify it, or create new work.</span></span>

## <a name="turn-on-the-mhax-feature"></a><span data-ttu-id="d661d-117">开启 MHAX 功能</span><span class="sxs-lookup"><span data-stu-id="d661d-117">Turn on the MHAX feature</span></span>

<span data-ttu-id="d661d-118">必须同时打开 MHAX 的功能和配置密钥，然后才能够使用 MHAX 功能。</span><span class="sxs-lookup"><span data-stu-id="d661d-118">Before you can use the MHAX feature, you must turn on both its feature and its configuration key.</span></span>

1. <span data-ttu-id="d661d-119">转到 **系统管理 \> 工作区 \> 功能管理**。</span><span class="sxs-lookup"><span data-stu-id="d661d-119">Go to **System administration \> Workspaces \> Feature management**.</span></span>
2. <span data-ttu-id="d661d-120">在 **[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** 工作区中，打开名为 *物料处理设备接口* 的功能。</span><span class="sxs-lookup"><span data-stu-id="d661d-120">In the **[Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** workspace, turn on the feature that is named *Material handling equipment interface*.</span></span>
3. <span data-ttu-id="d661d-121">将您的系统置于维护模式下，如[维护模式](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md)中所述。</span><span class="sxs-lookup"><span data-stu-id="d661d-121">Put your system into maintenance mode, as described in [Maintenance mode](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span></span>
4. <span data-ttu-id="d661d-122">转到 **系统管理 \> 设置 \> 许可证配置**。</span><span class="sxs-lookup"><span data-stu-id="d661d-122">Go to **System administration \> Setup \> License configuration**.</span></span>
5. <span data-ttu-id="d661d-123">展开 **贸易 \> 仓库和运输管理**，然后选中 **物料处理设备接口** 复选框。</span><span class="sxs-lookup"><span data-stu-id="d661d-123">Expand **Trade \> Warehouse and Transportation management**, and then select the **Material handling equipment interface** check box.</span></span>
6. <span data-ttu-id="d661d-124">关闭维护模式，如[维护模式](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md)中所述。</span><span class="sxs-lookup"><span data-stu-id="d661d-124">Turn off maintenance mode, as described in [Maintenance mode](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span></span>

## <a name="set-mhax-parameters"></a><span data-ttu-id="d661d-125">设置 MHAX 参数</span><span class="sxs-lookup"><span data-stu-id="d661d-125">Set MHAX parameters</span></span>

<span data-ttu-id="d661d-126">您必须在 **物料处理设备接口参数** 页上设置一些常规参数才能配置此功能。</span><span class="sxs-lookup"><span data-stu-id="d661d-126">You must set a few general parameters on the **Material handling equipment interface parameters** page to configure the feature.</span></span>

1. <span data-ttu-id="d661d-127">转到 **物料处理设备接口 \> 设置 \> 物料处理设备接口参数**。</span><span class="sxs-lookup"><span data-stu-id="d661d-127">Go to **Material handling equipment interface \> Setup \> Material handling equipment interface parameters**.</span></span>
2. <span data-ttu-id="d661d-128">在 **常规** 选项卡上，设置以下字段：</span><span class="sxs-lookup"><span data-stu-id="d661d-128">On the **General** tab, set the following fields:</span></span>

    - <span data-ttu-id="d661d-129">**用户 ID** – 选择一个工作人员。</span><span class="sxs-lookup"><span data-stu-id="d661d-129">**User ID** – Select a worker.</span></span> <span data-ttu-id="d661d-130">此工作人员将用于运行通过入站队列处理的所有工作操作（领料和放置）。</span><span class="sxs-lookup"><span data-stu-id="d661d-130">This worker will be used to run all work operations (picks and puts) that are processed through the inbound queue.</span></span>
    - <span data-ttu-id="d661d-131">**启用传入消息 ID** – 当此选项设置为 *是* 时，如果收到重复的传入消息 ID，该消息将被拒绝，并显示一条错误消息，指出该消息已存在。</span><span class="sxs-lookup"><span data-stu-id="d661d-131">**Enable inbound message ID** – When this option is set to *Yes*, if a duplicate inbound message ID is received, the message will be rejected, and an error message will state that the message already exists.</span></span> <span data-ttu-id="d661d-132">当此选项设置为 *否* 时，将允许重复的传入消息 ID。</span><span class="sxs-lookup"><span data-stu-id="d661d-132">When this option set to *No*, duplicate inbound message IDs will be allowed.</span></span>

3. <span data-ttu-id="d661d-133">在 **编号规则** 选项卡上，选择应用于为入站队列项、出站队列项和工作行对生成唯一 ID 的系统范围的编号规则。</span><span class="sxs-lookup"><span data-stu-id="d661d-133">On the **Number sequences** tab, select the system-wide number sequences that should be used to generate unique IDs for the inbound queue items, outbound queue items, and work line pairs.</span></span>

## <a name="outbound-events"></a><span data-ttu-id="d661d-134">出站事件</span><span class="sxs-lookup"><span data-stu-id="d661d-134">Outbound events</span></span>

<span data-ttu-id="d661d-135">在工作创建或工作执行期间的特定点，系统将确定是否必须生成要发送到 MH 系统的出站事件。</span><span class="sxs-lookup"><span data-stu-id="d661d-135">At specific points during work creation or work execution, the system determines whether it must generate outbound events to send to the MH system.</span></span> <span data-ttu-id="d661d-136">如果在仓库处理期间为特定点配置了预订，系统将根据预订的设置生成事件。</span><span class="sxs-lookup"><span data-stu-id="d661d-136">If a subscription is configured for a specific point during warehouse processing, the system generates the event according to the setup of the subscription.</span></span>

### <a name="structure-of-outbound-events"></a><span data-ttu-id="d661d-137">出站事件的结构</span><span class="sxs-lookup"><span data-stu-id="d661d-137">Structure of outbound events</span></span>

<span data-ttu-id="d661d-138">每个出站事件由出站队列 ID 唯一标识。</span><span class="sxs-lookup"><span data-stu-id="d661d-138">Each outbound event is uniquely identified by an outbound queue ID.</span></span> <span data-ttu-id="d661d-139">出站交易类型确定事件的类型。</span><span class="sxs-lookup"><span data-stu-id="d661d-139">The outbound transaction type determines the type of the event.</span></span> <span data-ttu-id="d661d-140">仓库和生成事件的预订的 ID 也会在事件中记录。</span><span class="sxs-lookup"><span data-stu-id="d661d-140">The warehouse and the ID of the subscription that generated the event are also recorded on the event.</span></span>

<span data-ttu-id="d661d-141">为了将数据传送到 MH 系统，出站事件包含 10 个数据字段（**data01** 到 **data10**）。</span><span class="sxs-lookup"><span data-stu-id="d661d-141">To carry data to the MH system, the outbound event contains 10 fields for data (**data01** through **data10**).</span></span> <span data-ttu-id="d661d-142">这些数据字段与现有数据库字段具有一对一 (1:1) 映射。</span><span class="sxs-lookup"><span data-stu-id="d661d-142">These data fields have a one-to-one (1:1) mapping to existing database fields.</span></span> <span data-ttu-id="d661d-143">具体而言，它们是从工作行表和工作标题表中的字段提取的。</span><span class="sxs-lookup"><span data-stu-id="d661d-143">Specifically, they are extracted from fields in the work line and work header tables.</span></span> <span data-ttu-id="d661d-144">这些字段可以自由选择。</span><span class="sxs-lookup"><span data-stu-id="d661d-144">The fields can be freely selected.</span></span> <span data-ttu-id="d661d-145">您在创建预订时设置它们。</span><span class="sxs-lookup"><span data-stu-id="d661d-145">You set them up when you create the subscription.</span></span>

<span data-ttu-id="d661d-146">除了与现有数据库字段有 1:1 映射的 10 个数据字段外，事件还可以包含称为 *有效负载* 的额外数据字段。</span><span class="sxs-lookup"><span data-stu-id="d661d-146">Besides the 10 data fields that have a 1:1 mapping to existing database fields, the event can contain an additional data field that is known as the *payload*.</span></span> <span data-ttu-id="d661d-147">此字段的内容由称为 *有效负载生成器* 的自定义 X++ 代码生成。</span><span class="sxs-lookup"><span data-stu-id="d661d-147">The contents of this field are generated by custom X++ code that is known as a *payload generator*.</span></span> <span data-ttu-id="d661d-148">应使用的任何有效负载生成器在预订中设置。</span><span class="sxs-lookup"><span data-stu-id="d661d-148">Any payload generator that should be used is set up in the subscription.</span></span>

<span data-ttu-id="d661d-149">为确保 MH 系统仅一次即可接收每个出站队列 ID，状态字段用于指定事件是否已准备好发送到外部系统或是否已经发送。</span><span class="sxs-lookup"><span data-stu-id="d661d-149">To ensure that the MH system receives each outbound queue ID only one time, a status field is used to specify whether an event is ready to be sent to the external system or whether it has already been sent.</span></span>

### <a name="outbound-queue-subscriptions"></a><span data-ttu-id="d661d-150">出站队列预订</span><span class="sxs-lookup"><span data-stu-id="d661d-150">Outbound queue subscriptions</span></span>

<span data-ttu-id="d661d-151">在生成任何事件之前，必须设置预订来告知 MHAX 功能是否以及如何生成事件。</span><span class="sxs-lookup"><span data-stu-id="d661d-151">Before any events are generated, a subscription must be set up to tell the MHAX feature whether and how to generate events.</span></span> <span data-ttu-id="d661d-152">生成的事件由预订标识符标记。</span><span class="sxs-lookup"><span data-stu-id="d661d-152">Generated events are tagged by the subscription identifier.</span></span> <span data-ttu-id="d661d-153">因此，多个 MH 系统可以连接到同一个 WMS 系统，但它们的事件保持分开。</span><span class="sxs-lookup"><span data-stu-id="d661d-153">Therefore, multiple MH systems can connect to the same WMS system but keep their events separate.</span></span> <span data-ttu-id="d661d-154">当轮询 MHAX 服务查询新事件时，预订是检索事件的可用选项之一。</span><span class="sxs-lookup"><span data-stu-id="d661d-154">When the MHAX service is polled for new events, a subscription is one of the available options for retrieving the events.</span></span>

<span data-ttu-id="d661d-155">要创建预订，转到 **物料处理设备接口 \> 设置 \> 预订**。</span><span class="sxs-lookup"><span data-stu-id="d661d-155">To create a subscription, go to **Material handling equipment interface \> Setup \> Subscriptions**.</span></span> <span data-ttu-id="d661d-156">对于每个预订，以下参数可用：</span><span class="sxs-lookup"><span data-stu-id="d661d-156">For each subscription, the following parameters are available:</span></span>

- <span data-ttu-id="d661d-157">**预订 ID** – 标识预订的唯一名称。</span><span class="sxs-lookup"><span data-stu-id="d661d-157">**Subscription ID** – A unique name that identifies the subscription.</span></span>
- <span data-ttu-id="d661d-158">**描述** – 预订的自由文本描述。</span><span class="sxs-lookup"><span data-stu-id="d661d-158">**Description** – A free-text description of the subscription.</span></span>
- <span data-ttu-id="d661d-159">**仓库** – 应按其筛选事件的特定仓库。</span><span class="sxs-lookup"><span data-stu-id="d661d-159">**Warehouse** – The specific warehouses that events should be filtered by.</span></span>
- <span data-ttu-id="d661d-160">**出站交易类型** – 预订应包含的事件类型。</span><span class="sxs-lookup"><span data-stu-id="d661d-160">**Outbound transaction type** – The type of events that the subscription should contain.</span></span>
- <span data-ttu-id="d661d-161">**有效负载生成器** – 可选代码扩展，可以在出站事件的 **有效负载** 字段中输入其他信息。</span><span class="sxs-lookup"><span data-stu-id="d661d-161">**Payload generator** – An optional code extension that can enter additional information in the **Payload** field of the outbound event.</span></span>

<span data-ttu-id="d661d-162">查询可以与每个预订关联。</span><span class="sxs-lookup"><span data-stu-id="d661d-162">A query can be associated with each subscription.</span></span> <span data-ttu-id="d661d-163">此查询筛选工作行和标题来进一步限制将使用预订生成事件的工作。</span><span class="sxs-lookup"><span data-stu-id="d661d-163">This query filters work lines and headers to further limit the work that will use the subscription to generate events.</span></span> <span data-ttu-id="d661d-164">要将查询添加到预订，在 **预订** 页上选中相关预订的 **运行查询** 复选框，然后在操作窗格上选择 **编辑查询**。</span><span class="sxs-lookup"><span data-stu-id="d661d-164">To add a query to a subscription, select the **Run query** check box for the relevant subscription on the **Subscriptions** page, and then select **Edit query** on the Action Pane.</span></span> <span data-ttu-id="d661d-165">标准 Supply Chain Management 查询编辑器将出现。</span><span class="sxs-lookup"><span data-stu-id="d661d-165">The standard Supply Chain Management query editor appears.</span></span>

<span data-ttu-id="d661d-166">此外，预订还包括一个 *预订映射*，可根据需要将工作标题或工作行中的字段映射到出站事件的 10 个空闲数据字段的其中一部分或全部。</span><span class="sxs-lookup"><span data-stu-id="d661d-166">In addition, the subscription includes a *subscription map* that maps fields from either the work header or the work line to some or all of the 10 free data fields of the outbound event, as required.</span></span> <span data-ttu-id="d661d-167">要将信息返回到 MHAX 服务，通常会包含工作行记录 ID 或 *工作行对 ID*。</span><span class="sxs-lookup"><span data-stu-id="d661d-167">To return information to the MHAX service, you will typically include the work line record ID or the *work line pair ID*.</span></span> <span data-ttu-id="d661d-168">（工作行对 ID 是一个新属性，让系统可以使用单个退回命令处理领料和放置行。）其余字段取决于用例。</span><span class="sxs-lookup"><span data-stu-id="d661d-168">(The work line pair ID is a new property that enables the system to use a single return command to process pick and put lines.) The remaining fields depend on the use case.</span></span> <span data-ttu-id="d661d-169">本主题后面提供了一些示例。</span><span class="sxs-lookup"><span data-stu-id="d661d-169">Some examples are provided later in this topic.</span></span>

<span data-ttu-id="d661d-170">要设置预订映射，在 **预订** 页上选择相关的预订，然后在操作窗格上选择 **预订映射**。</span><span class="sxs-lookup"><span data-stu-id="d661d-170">To set up a subscription map, select the relevant subscription on the **Subscriptions** page, and then select **Subscription map** on the Action Pane.</span></span> <span data-ttu-id="d661d-171">在在出现的 **预订映射** 对话框中，您可以根据需要为每个可用数据字段分配表和字段。</span><span class="sxs-lookup"><span data-stu-id="d661d-171">In the **Subscription map** dialog box that appears, you can assign a table and field for each available data field as you require.</span></span>

### <a name="outbound-event-types"></a><span data-ttu-id="d661d-172">出站事件类型</span><span class="sxs-lookup"><span data-stu-id="d661d-172">Outbound event types</span></span>

<span data-ttu-id="d661d-173">本节介绍各个可用的事件类型。</span><span class="sxs-lookup"><span data-stu-id="d661d-173">This section describes the various events types that are available.</span></span> <span data-ttu-id="d661d-174">（事件类型也称为 *交易类型*。）另外还说明了每个事件类型是何时在 WMS 系统中创建的。</span><span class="sxs-lookup"><span data-stu-id="d661d-174">(Event types are also known as *transaction types*.) It also explains when each type of event is created in the WMS system.</span></span>

#### <a name="work-creation-events"></a><span data-ttu-id="d661d-175">工作创作事件</span><span class="sxs-lookup"><span data-stu-id="d661d-175">Work creation events</span></span>

<span data-ttu-id="d661d-176">工作创建事件在应用程序生成工作后创建。</span><span class="sxs-lookup"><span data-stu-id="d661d-176">Work creation events are created after work is generated by the application.</span></span> <span data-ttu-id="d661d-177">此行为适用于大多数类型的工作创建流程，尤其是创建领料和补货工作。</span><span class="sxs-lookup"><span data-stu-id="d661d-177">This behavior applies to most types of work creation processes, most notably to the creation of picking and replenishment work.</span></span> <span data-ttu-id="d661d-178">通常，如果工作是在 *未结* 状态下创建的，这表明该工作已准备就绪，可以由工作人员运行，工作创建事件将生成。</span><span class="sxs-lookup"><span data-stu-id="d661d-178">In general, if work is created in an *Open* state, which indicates that the work is ready to be run by a worker, a work creation event will be generated.</span></span> <span data-ttu-id="d661d-179">此外，还会为基本移动工作（不是通过模板工作移动）生成工作创建事件，即使该工作没有作为未结工作创建。</span><span class="sxs-lookup"><span data-stu-id="d661d-179">In addition, work creation events will be generated for basic movement work (not movement by template work), even though that work isn't created as open work.</span></span>

<span data-ttu-id="d661d-180">此行为的一个明显例外是周期盘点工作，它当前不受支持。</span><span class="sxs-lookup"><span data-stu-id="d661d-180">A notable exception to this behavior is cycle counting work, which isn't currently supported.</span></span> <span data-ttu-id="d661d-181">MH 系统中的存货盘点不在 MHAX 范围内，盘点结果必须导入库存盘点日记帐。</span><span class="sxs-lookup"><span data-stu-id="d661d-181">Stock counts in the MH system are outside the scope of MHAX, and the results of counts must be imported into an inventory counting journal.</span></span>

<span data-ttu-id="d661d-182">创建工作后，MHAX 服务将处理所生成的工作行，并为每个工作标题的所有生成的工作行分配工作行对 ID。</span><span class="sxs-lookup"><span data-stu-id="d661d-182">After work has been created, the MHAX service processes the work lines that are generated and assigns a work line pair ID to all generated work lines for each work header.</span></span> <span data-ttu-id="d661d-183">目的是将所有领料工作行与连续的放置分组到一个工作行对 ID 下。</span><span class="sxs-lookup"><span data-stu-id="d661d-183">The objective is to group all the pick work lines with the successive puts under one work line pair ID.</span></span> <span data-ttu-id="d661d-184">（这些组对应于工作模板中的领料/放置对。）通过这种方式，可以使用一个 ID 来报告所有相关领料和放置行的工作完成。</span><span class="sxs-lookup"><span data-stu-id="d661d-184">(The groups correspond to pick/put pairs in work templates.) In this way, a single ID can be used to report work completion for all related pick and put lines.</span></span> <span data-ttu-id="d661d-185">分组流程从第一行开始，然后以相同的 ID 继续，直到遇到连续的放置/领料工作行对。</span><span class="sxs-lookup"><span data-stu-id="d661d-185">The grouping process starts with the first line and then continues with the same ID until it encounters a successive pair of put/pick work lines.</span></span> <span data-ttu-id="d661d-186">运行的 ID 将被分配到该对的放置行。</span><span class="sxs-lookup"><span data-stu-id="d661d-186">The running ID is assigned to the put line of that pair.</span></span> <span data-ttu-id="d661d-187">然后，新 ID 将用于之后该对的领料行。</span><span class="sxs-lookup"><span data-stu-id="d661d-187">A new ID it then used for the pick line of the pair onward.</span></span> <span data-ttu-id="d661d-188">此流程将一直持续到处理完所有属于工作标题的行为止。</span><span class="sxs-lookup"><span data-stu-id="d661d-188">This process continues until it has processed all lines that belong to the work header.</span></span>

<span data-ttu-id="d661d-189">作为工作创建事件的一项特殊功能，如果在工作标题上将 **锁定波次** 选项设置为 *是*，生成的事件的状态将为 *锁定*，而不是用于将它们发送到 MH 系统的通常的 *就绪* 状态。</span><span class="sxs-lookup"><span data-stu-id="d661d-189">As a special feature of work creation events, if the **Blocked wave** option is set to *Yes* on the work header, the events that are generated will have a status of *Blocked* instead of the usual status of *Ready* that is used to send them to the MH system.</span></span> <span data-ttu-id="d661d-190">工作标题上的 **锁定波次** 标记表示工作标题尚未准备好供工作人员运行，可能是由于补货工作未完成。</span><span class="sxs-lookup"><span data-stu-id="d661d-190">The **Blocked wave** flag on the work header indicates that the work header isn't yet ready for workers to run, perhaps because of unfinished replenishment work.</span></span> <span data-ttu-id="d661d-191">清除 **锁定波次** 标记后，已生成的事件将被解除锁定，可供 MH 系统从队列中检索。</span><span class="sxs-lookup"><span data-stu-id="d661d-191">When the **Blocked wave** flag is cleared, events that have already been generated are unblocked and are available for the MH system to retrieve from the queue.</span></span>

#### <a name="work-initiation-events"></a><span data-ttu-id="d661d-192">工作启动事件</span><span class="sxs-lookup"><span data-stu-id="d661d-192">Work initiation events</span></span>

<span data-ttu-id="d661d-193">工作启动事件在工作状态在工作更新期间从 *未结* 变为 *进行中* 时触发。</span><span class="sxs-lookup"><span data-stu-id="d661d-193">Work initiation events are triggered when the work status changes from *Open* to *In process* during work update.</span></span>

#### <a name="work-completion-events"></a><span data-ttu-id="d661d-194">工作完成事件</span><span class="sxs-lookup"><span data-stu-id="d661d-194">Work completion events</span></span>

<span data-ttu-id="d661d-195">工作完成事件在工作状态在工作更新期间从 *进行中* 变为 *已关闭* 时触发。</span><span class="sxs-lookup"><span data-stu-id="d661d-195">Work completion events are triggered when the work status changes from *In process* to *Closed* during work update.</span></span>

#### <a name="work-cancellation-events"></a><span data-ttu-id="d661d-196">工作取消事件</span><span class="sxs-lookup"><span data-stu-id="d661d-196">Work cancellation events</span></span>

<span data-ttu-id="d661d-197">工作取消事件在工作状态在工作更新期间从 *已取消* 以外的任何状态变为 *已取消* 时触发。</span><span class="sxs-lookup"><span data-stu-id="d661d-197">Work cancellation events are triggered when the work status changes from any status besides *Canceled* to *Canceled* during work update.</span></span> <span data-ttu-id="d661d-198">此外，与工作标题相关的所有其他事件将被从所有预订的队列中删除。</span><span class="sxs-lookup"><span data-stu-id="d661d-198">In addition, all other events that are related to the work header are deleted from the queue for all subscriptions.</span></span> <span data-ttu-id="d661d-199">这样，将阻止外部系统处理不需要的事件。</span><span class="sxs-lookup"><span data-stu-id="d661d-199">In this way, external systems are prevented from processing events that aren't required.</span></span>

#### <a name="pickput-completion-events"></a><span data-ttu-id="d661d-200">领料/放置完成事件</span><span class="sxs-lookup"><span data-stu-id="d661d-200">Pick/put completion events</span></span>

<span data-ttu-id="d661d-201">领料/放置完成事件在领料/放置行的状态在工作行更新期间从 *进行中* 变为 *已关闭* 时触发。</span><span class="sxs-lookup"><span data-stu-id="d661d-201">Pick/put completion events are triggered when the status of the pick/put line changes from *In process* to *Closed* during work line update.</span></span>

### <a name="monitor-the-outbound-queue"></a><span data-ttu-id="d661d-202">监视出站队列</span><span class="sxs-lookup"><span data-stu-id="d661d-202">Monitor the outbound queue</span></span>

<span data-ttu-id="d661d-203">要查看您的出站队列，请转到 **物料处理设备接口 \> 通用 \> 出站队列**。</span><span class="sxs-lookup"><span data-stu-id="d661d-203">To review your outbound queue, go to **Material handling equipment interface \> Common \> Outbound queue**.</span></span> <span data-ttu-id="d661d-204">**出站队列** 页列出每个出站队列项及其状态。</span><span class="sxs-lookup"><span data-stu-id="d661d-204">The **Outbound queue** page lists every outbound queue item and its status.</span></span> <span data-ttu-id="d661d-205">选择一个队列项来查看其详细信息。</span><span class="sxs-lookup"><span data-stu-id="d661d-205">Select a queue item to view its details.</span></span> <span data-ttu-id="d661d-206">这些详细信息包括项目的交易类型、它使用的预订，以及每个数据字段的值（**data01** 到 **data10**）和有效负载。</span><span class="sxs-lookup"><span data-stu-id="d661d-206">These details include the item's transaction type, the subscription that it used, and values for each data field (**data01** through **data10**) and the payload.</span></span>

### <a name="clean-up-the-outbound-queue"></a><span data-ttu-id="d661d-207">清理出站队列</span><span class="sxs-lookup"><span data-stu-id="d661d-207">Clean up the outbound queue</span></span>

<span data-ttu-id="d661d-208">最终，您的出站队列将开始充满已发送的队列项。</span><span class="sxs-lookup"><span data-stu-id="d661d-208">Eventually, your outbound queue will start to become full of queue items that have already been sent.</span></span> <span data-ttu-id="d661d-209">要删除这些项目，请转到 **物料处理设备接口 \> 定期任务 \> 清理 \> 出站队列清理**。</span><span class="sxs-lookup"><span data-stu-id="d661d-209">To remove these items, go to **Material handling equipment interface \> Periodic tasks \> Cleanup \> Outbound queue cleanup**.</span></span>

## <a name="inbound-events"></a><span data-ttu-id="d661d-210">入站事件</span><span class="sxs-lookup"><span data-stu-id="d661d-210">Inbound events</span></span>

<span data-ttu-id="d661d-211">本节介绍 MH 系统可以向 WMS 系统报告的各个类型的入站事件。</span><span class="sxs-lookup"><span data-stu-id="d661d-211">This section describes the various types of inbound events that the MH system can report back to the WMS system.</span></span> <span data-ttu-id="d661d-212">另外还说明了数据必须由 MH 系统提供，以及每个入站事件在 WMS 系统中的作用。</span><span class="sxs-lookup"><span data-stu-id="d661d-212">It also explains data must be supplied by the MH system, and what each inbound event does in the WMS system.</span></span>

### <a name="structure-of-inbound-events"></a><span data-ttu-id="d661d-213">入站事件的结构</span><span class="sxs-lookup"><span data-stu-id="d661d-213">Structure of inbound events</span></span>

<span data-ttu-id="d661d-214">提交入站事件时，外部系统必须提供入站交易类型以及最多 10 个参数（**data01** 到 **data10**）。</span><span class="sxs-lookup"><span data-stu-id="d661d-214">When an inbound event is submitted, the external system must supply the inbound transaction type together with up to 10 parameters (**data01** through **data10**).</span></span> <span data-ttu-id="d661d-215">可选验证可以确保 MHAX 服务没有多次收到同一个入站事件。</span><span class="sxs-lookup"><span data-stu-id="d661d-215">Optional validation can make sure that the MHAX service hasn't received the same inbound event more than one time.</span></span> <span data-ttu-id="d661d-216">要启用此验证，每个入站事件必须具有唯一的消息 ID。</span><span class="sxs-lookup"><span data-stu-id="d661d-216">To enable this validation, each inbound event must have a unique message ID.</span></span> <span data-ttu-id="d661d-217">如果收到重复的消息 ID，并且在 **物料处理设备接口参数** 页上 **启用入站消息 ID** 选项设置为 *是*，该消息将被拒绝。</span><span class="sxs-lookup"><span data-stu-id="d661d-217">If a duplicate message ID is received, and if the **Enable inbound message ID** option is set to *Yes* on the **Material handling equipment interface parameters** page, the message will be rejected.</span></span> <span data-ttu-id="d661d-218">错误消息将指出该消息已经存在。</span><span class="sxs-lookup"><span data-stu-id="d661d-218">An error message will state that the message already exists.</span></span>

<span data-ttu-id="d661d-219">除了传入数据字段外，系统还为事件分配唯一的入站队列 ID。</span><span class="sxs-lookup"><span data-stu-id="d661d-219">In addition to the incoming data fields, the system assigns a unique inbound queue ID to the event.</span></span>

### <a name="inbound-event-types"></a><span data-ttu-id="d661d-220">入站事件类型</span><span class="sxs-lookup"><span data-stu-id="d661d-220">Inbound event types</span></span>

<span data-ttu-id="d661d-221">本节介绍受支持的入站事件类型（交易类型）以及必须为要处理的事件提供的数据。</span><span class="sxs-lookup"><span data-stu-id="d661d-221">This section describes the inbound event types (transaction types) that are supported and the data that must be supplied for events to be processed.</span></span>

#### <a name="work-confirm-events"></a><span data-ttu-id="d661d-222">工作确认事件</span><span class="sxs-lookup"><span data-stu-id="d661d-222">Work-confirm events</span></span>

<span data-ttu-id="d661d-223">工作确认事件需要传入数据字段包括以下信息：</span><span class="sxs-lookup"><span data-stu-id="d661d-223">Work-confirm events require that the incoming data fields include the following information:</span></span>

- <span data-ttu-id="d661d-224">**data01** – 工作行对 ID。</span><span class="sxs-lookup"><span data-stu-id="d661d-224">**data01** – The work line pair ID.</span></span>
- <span data-ttu-id="d661d-225">**data02** – 工作行记录 ID（`RecId` 值）。</span><span class="sxs-lookup"><span data-stu-id="d661d-225">**data02** – The work line record ID (`RecId` value).</span></span>

    > [!NOTE]
    > <span data-ttu-id="d661d-226">**data01** 字段 *或* 者 **data02** 字段的 *其中一个* 必须存在。</span><span class="sxs-lookup"><span data-stu-id="d661d-226">*Either* the **data01** field *or* the **data02** field must be present.</span></span>

- <span data-ttu-id="d661d-227">**data03** – 从其领料的牌照的 ID。</span><span class="sxs-lookup"><span data-stu-id="d661d-227">**data03** – The ID of the license plate to pick from.</span></span>
- <span data-ttu-id="d661d-228">**data04** – 工作标题的目标牌照 ID。</span><span class="sxs-lookup"><span data-stu-id="d661d-228">**data04** – The work header's target license plate ID.</span></span>

<span data-ttu-id="d661d-229">如果提供了工作行对 ID，将按顺序运行由工作行对 ID 标记、状态为 *未结* 或 *进行中* 的所有领料、放置或自定义工作行。</span><span class="sxs-lookup"><span data-stu-id="d661d-229">If the work line pair ID is provided, all pick, put, or custom work lines that are marked by the work line pair ID, and that have a status of *Open* or *In process*, are run sequentially.</span></span> <span data-ttu-id="d661d-230">如果提供了工作行记录 ID（`RecId` 值），工作行必须是状态为 *未结* 或 *进行中* 的领料、放置或自定义工作行。</span><span class="sxs-lookup"><span data-stu-id="d661d-230">If a work line record ID (`RecId` value) is provided, the work line must be a pick, put, or custom work line that has a status of *Open* or *In process*.</span></span>

<span data-ttu-id="d661d-231">牌照控制的位置的领料行需要 **data03** 指定应从其领料的牌照，不论行是使用工作行记录 ID 还是工作行对 ID 标记。</span><span class="sxs-lookup"><span data-stu-id="d661d-231">Pick lines from license plate–controlled locations require that the **data03** specify the license plate that should be picked from, regardless of whether the lines are marked by the work line record ID or the work line pair ID.</span></span> <span data-ttu-id="d661d-232">**data04** 字段必须指定领料的工作标题的目标牌照。</span><span class="sxs-lookup"><span data-stu-id="d661d-232">The **data04** field must specify the work header's target license plate for the pick.</span></span>

<span data-ttu-id="d661d-233">放置行不接受其他信息。</span><span class="sxs-lookup"><span data-stu-id="d661d-233">Put lines don't accept further information.</span></span> <span data-ttu-id="d661d-234">它们仅基于当前工作行的位置和工作的目标牌照运行。</span><span class="sxs-lookup"><span data-stu-id="d661d-234">They are run based only on the current work line's location and the work's target license plate.</span></span> <span data-ttu-id="d661d-235">如果必须在其他位置进行放置，请按照本主题后面[替代事件](#override-events)一节中的介绍更改工作行的位置。</span><span class="sxs-lookup"><span data-stu-id="d661d-235">If the put must be done to a different location, change the location of the work line as described in the [Override events](#override-events) section later in this topic.</span></span>

<span data-ttu-id="d661d-236">自定义工作行在入站事件中不需要或支持任何其他信息。</span><span class="sxs-lookup"><span data-stu-id="d661d-236">Custom work lines don't require, or support, any additional information in the inbound event.</span></span>

#### <a name="short-pick-events"></a><span data-ttu-id="d661d-237">领料短缺事件</span><span class="sxs-lookup"><span data-stu-id="d661d-237">Short pick events</span></span>

<span data-ttu-id="d661d-238">领料短缺事件需要传入数据字段包括以下信息：</span><span class="sxs-lookup"><span data-stu-id="d661d-238">Short pick events require that the incoming data fields include the following information:</span></span>

- <span data-ttu-id="d661d-239">**data02** – 工作记录 ID（`RecId` 值）。</span><span class="sxs-lookup"><span data-stu-id="d661d-239">**data02** – The work record ID (`RecId` value).</span></span>
- <span data-ttu-id="d661d-240">**data03** – 从其领料的牌照的 ID。</span><span class="sxs-lookup"><span data-stu-id="d661d-240">**data03** – The ID of the license plate to pick from.</span></span>
- <span data-ttu-id="d661d-241">**data04** – 要领料的数量。</span><span class="sxs-lookup"><span data-stu-id="d661d-241">**data04** – The quantity to pick.</span></span>
- <span data-ttu-id="d661d-242">**data05** – 领料短缺异常代码。</span><span class="sxs-lookup"><span data-stu-id="d661d-242">**data05** – The short pick exception code.</span></span>
- <span data-ttu-id="d661d-243">**data06** – 工作标题的目标牌照 ID。</span><span class="sxs-lookup"><span data-stu-id="d661d-243">**data06** – The work header's target license plate ID.</span></span>

> [!NOTE]
> <span data-ttu-id="d661d-244">**data01** 字段不用于领料短缺事件。</span><span class="sxs-lookup"><span data-stu-id="d661d-244">The **data01** field isn't used for short pick events.</span></span>

<span data-ttu-id="d661d-245">此事件类似于工作确认事件，但仅应用于领料行。</span><span class="sxs-lookup"><span data-stu-id="d661d-245">This event resembles the work confirmation event, but it applies only to pick lines.</span></span>

#### <a name="override-events"></a><a id="override-events"></a><span data-ttu-id="d661d-246">替代事件</span><span class="sxs-lookup"><span data-stu-id="d661d-246">Override events</span></span>

<span data-ttu-id="d661d-247">替代事件需要传入数据字段包括以下信息：</span><span class="sxs-lookup"><span data-stu-id="d661d-247">Override events require that the incoming data fields include the following information:</span></span>

- <span data-ttu-id="d661d-248">**data01** – 工作记录 ID（`RecId` 值）。</span><span class="sxs-lookup"><span data-stu-id="d661d-248">**data01** – The work record ID (`RecId` value).</span></span>
- <span data-ttu-id="d661d-249">**data02** – 新位置 ID。</span><span class="sxs-lookup"><span data-stu-id="d661d-249">**data02** – The new location ID.</span></span>

<span data-ttu-id="d661d-250">工作行的状态必须为 *未结* 或 *进行中*，并且新位置必须存在。</span><span class="sxs-lookup"><span data-stu-id="d661d-250">The work line must have a status of either *Open* or *In process*, and the new location must exist.</span></span>

#### <a name="license-plate-receipt-events"></a><span data-ttu-id="d661d-251">牌照接收事件</span><span class="sxs-lookup"><span data-stu-id="d661d-251">License plate receipt events</span></span>

<span data-ttu-id="d661d-252">牌照接收事件需要传入数据字段包括以下信息：</span><span class="sxs-lookup"><span data-stu-id="d661d-252">License plate receipt events require that the incoming data fields include the following information:</span></span>

- <span data-ttu-id="d661d-253">**data01** – 要接收的入站牌照的 ID。</span><span class="sxs-lookup"><span data-stu-id="d661d-253">**data01** – The ID of the inbound license plate to receive.</span></span>

<span data-ttu-id="d661d-254">系统基于作为 **data01** 字段的值传入的牌照执行牌照接收操作。</span><span class="sxs-lookup"><span data-stu-id="d661d-254">The system performs a license plate receiving operation, based on the license plate that is passed in as the value of the **data01** field.</span></span>

### <a name="monitor-the-inbound-queue"></a><span data-ttu-id="d661d-255">监视入站队列</span><span class="sxs-lookup"><span data-stu-id="d661d-255">Monitor the inbound queue</span></span>

<span data-ttu-id="d661d-256">要查看您的入站队列，请转到 **物料处理设备接口 \> 通用 \> 入站队列**。</span><span class="sxs-lookup"><span data-stu-id="d661d-256">To review your inbound queue, go to **Material handling equipment interface \> Common \> Inbound queue**.</span></span> <span data-ttu-id="d661d-257">**入站队列** 页列出每个入站队列项及其状态。</span><span class="sxs-lookup"><span data-stu-id="d661d-257">The **Inbound queue** page lists every inbound queue item and its status.</span></span> <span data-ttu-id="d661d-258">选择一个队列项来查看其详细信息。</span><span class="sxs-lookup"><span data-stu-id="d661d-258">Select a queue item to view its details.</span></span> <span data-ttu-id="d661d-259">这些详细信息包括项目的交易类型、消息 ID，以及每个数据字段的值（**data01** 到 **data10**）。</span><span class="sxs-lookup"><span data-stu-id="d661d-259">These details include the item's transaction type, the message ID, and values for each data field (**data01** through **data10**).</span></span>

<span data-ttu-id="d661d-260">如果在处理入站事件时发生错误或其他类型的日志项，您可以通过在操作窗格上选择 **错误日志** 来检查日志。</span><span class="sxs-lookup"><span data-stu-id="d661d-260">If an error or another type of log item occurred while inbound events were processed, you can inspect the log by selecting **Error log** on the Action Pane.</span></span>

### <a name="inbound-event-processing"></a><span data-ttu-id="d661d-261">入站事件处理</span><span class="sxs-lookup"><span data-stu-id="d661d-261">Inbound event processing</span></span>

<span data-ttu-id="d661d-262">入站事件首先写入到数据库，然后立即（同步）运行。</span><span class="sxs-lookup"><span data-stu-id="d661d-262">Inbound events are first written to the database, and they are then immediately (synchronously) run.</span></span> <span data-ttu-id="d661d-263">如果在处理过程中发生错误，事件仍会写入到队列，但状态将设置为 *出错*。</span><span class="sxs-lookup"><span data-stu-id="d661d-263">If an error occurs during processing, the event is still written to the queue, but the status is set to *Errored*.</span></span> <span data-ttu-id="d661d-264">MHAX 服务将错误消息返回到 MH 系统，并将错误日志存储在入站事件记录中供以后调查。</span><span class="sxs-lookup"><span data-stu-id="d661d-264">The MHAX service returns an error message to the MH system and stores the error log in the inbound event record for later investigation.</span></span>

<span data-ttu-id="d661d-265">如果错误条件已修复，状态为 *出错* 的事件可以在以后重新处理。</span><span class="sxs-lookup"><span data-stu-id="d661d-265">Events that have a status of *Errored* can be reprocessed later if the error condition is fixed.</span></span> <span data-ttu-id="d661d-266">要重新处理，请按照下列步骤之一操作：</span><span class="sxs-lookup"><span data-stu-id="d661d-266">To reprocess them, follow one of these steps:</span></span>

- <span data-ttu-id="d661d-267">转到 **物料处理设备接口 \> 通用 \> 入站队列**。</span><span class="sxs-lookup"><span data-stu-id="d661d-267">Go to **Material handling equipment interface \> Common \> Inbound queue**.</span></span> <span data-ttu-id="d661d-268">选择相关的入站队列，然后在操作窗格上选择 **重新处理**。</span><span class="sxs-lookup"><span data-stu-id="d661d-268">Select the relevant inbound queue, and then select **Reprocess** on the Action Pane.</span></span>
- <span data-ttu-id="d661d-269">转到 **物料处理设备接口 \> 通用 \> 重新处理出错的入站队列**。</span><span class="sxs-lookup"><span data-stu-id="d661d-269">Go to **Material handling equipment interface \> Common \> Reprocess errored inbound queue**.</span></span> <span data-ttu-id="d661d-270">将出现一个标准批处理作业对话框。</span><span class="sxs-lookup"><span data-stu-id="d661d-270">A standard batch job dialog box appears.</span></span> <span data-ttu-id="d661d-271">在那里，您可以设置记录筛选器，并计划或运行批处理作业来重新处理队列。</span><span class="sxs-lookup"><span data-stu-id="d661d-271">There, you can set up a record filter, and schedule or run a batch job to reprocess the queue.</span></span>

<span data-ttu-id="d661d-272">所有工作操作（领料和放置）均使用在 **物料处理设备接口参数** 页上的 **用户 ID** 字段中选择的工作人员运行。</span><span class="sxs-lookup"><span data-stu-id="d661d-272">All work operations (picks and puts) are run by using the worker who is selected in the **User ID** field on the **Material handling equipment interface parameters** page.</span></span>

### <a name="clean-up-the-inbound-queue"></a><span data-ttu-id="d661d-273">清理入站队列</span><span class="sxs-lookup"><span data-stu-id="d661d-273">Clean up the inbound queue</span></span>

<span data-ttu-id="d661d-274">最终，您的入站队列将开始充满已处理的队列项。</span><span class="sxs-lookup"><span data-stu-id="d661d-274">Eventually, your inbound queue will start to become full of queue items that have already been processed.</span></span> <span data-ttu-id="d661d-275">要删除这些项目，请转到 **物料处理设备接口 \> 定期任务 \> 清理 \> 入站队列清理**。</span><span class="sxs-lookup"><span data-stu-id="d661d-275">To remove these items, go to **Material handling equipment interface \> Periodic tasks \> Cleanup \> Inbound queue cleanup**.</span></span>

## <a name="get-a-quick-overview-by-using-the-queue-manager"></a><span data-ttu-id="d661d-276">使用队列管理器快速概览</span><span class="sxs-lookup"><span data-stu-id="d661d-276">Get a quick overview by using the queue manager</span></span>

<span data-ttu-id="d661d-277">要快速概览与入站和出站队列相关的所有活动，请转到 **物料处理设备接口 \> 工作区 \> 队列管理器**。</span><span class="sxs-lookup"><span data-stu-id="d661d-277">To get a quick overview of all the activity that is related to your inbound and outbound queues, go to **Material handling equipment interface \> Workspaces \> Queue manager**.</span></span> <span data-ttu-id="d661d-278">**队列管理器** 页提供了一组选项卡和磁贴，可用于监视和浏览队列。</span><span class="sxs-lookup"><span data-stu-id="d661d-278">The **Queue manager** page provides a set of tabs and tiles that you can use to monitor and explore your queues.</span></span> <span data-ttu-id="d661d-279">另外还提供指向本主题中提到的其他大多数页面的有用链接。</span><span class="sxs-lookup"><span data-stu-id="d661d-279">It also provides useful links to most of the other pages that are mentioned in this topic.</span></span>

## <a name="connect-to-the-mhax-service"></a><span data-ttu-id="d661d-280">连接到 MHAX 服务</span><span class="sxs-lookup"><span data-stu-id="d661d-280">Connect to the MHAX service</span></span>

<span data-ttu-id="d661d-281">MHAX 作为自定义服务实现。</span><span class="sxs-lookup"><span data-stu-id="d661d-281">MHAX is implemented as a custom service.</span></span> <span data-ttu-id="d661d-282">因此，可以通过 SOAP 和 REST 调用对其进行访问。</span><span class="sxs-lookup"><span data-stu-id="d661d-282">Therefore, it's accessible via SOAP and REST calls.</span></span> <span data-ttu-id="d661d-283">以下是 SOAP 和 REST 终结点的地址：</span><span class="sxs-lookup"><span data-stu-id="d661d-283">Here are the addresses of the SOAP and REST endpoints:</span></span>

- <span data-ttu-id="d661d-284">**SOAP：**`https://base_environment_URL/soap/services/WMHEServices`</span><span class="sxs-lookup"><span data-stu-id="d661d-284">**SOAP:** `https://base_environment_URL/soap/services/WMHEServices`</span></span>
- <span data-ttu-id="d661d-285">**REST：**`https://base_environment_URL/api/services/WMHEServices/WMHEService`</span><span class="sxs-lookup"><span data-stu-id="d661d-285">**REST:** `https://base_environment_URL/api/services/WMHEServices/WMHEService`</span></span>

## <a name="retrieve-messages-from-the-outbound-queue"></a><span data-ttu-id="d661d-286">从出站队列检索消息</span><span class="sxs-lookup"><span data-stu-id="d661d-286">Retrieve messages from the outbound queue</span></span>

<span data-ttu-id="d661d-287">要从出站队列检索消息，请使用以下方法之一：</span><span class="sxs-lookup"><span data-stu-id="d661d-287">To retrieve messages from the outbound queue, use one of the following methods:</span></span>

- <span data-ttu-id="d661d-288">使用 `readOutboundSubscriptionQueue` 根据预订 ID 检索事件。</span><span class="sxs-lookup"><span data-stu-id="d661d-288">Use `readOutboundSubscriptionQueue` to retrieve the events based on the subscription ID.</span></span>
- <span data-ttu-id="d661d-289">使用 `readOutboundWarehouseQueue` 根据事件类型和仓库 ID 跨多个预订检索事件。</span><span class="sxs-lookup"><span data-stu-id="d661d-289">Use `readOutboundWarehouseQueue` to retrieve the events based on the event type and warehouse ID across multiple subscriptions.</span></span>
