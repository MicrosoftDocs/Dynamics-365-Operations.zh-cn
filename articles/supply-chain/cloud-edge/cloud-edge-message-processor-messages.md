---
title: 消息处理程序消息
description: 本主题提供有关缩放单元工作负荷的消息处理器消息功能的信息。
author: perlynne
ms.date: 04/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysMessageProcessorMessage, BusinessEventsWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: perlynne
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 03d8cad743ac2b2b1e7b2832b8272ca3dbf5a163
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021047"
---
# <a name="message-processor-messages"></a><span data-ttu-id="7b0df-103">消息处理程序消息</span><span class="sxs-lookup"><span data-stu-id="7b0df-103">Message processor messages</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="7b0df-104">当为[制造工作负荷](cloud-edge-workload-manufacturing.md)和[仓库管理工作负荷](cloud-edge-workload-warehousing.md)运行云和边缘缩放单元时，将使用消息处理器消息。</span><span class="sxs-lookup"><span data-stu-id="7b0df-104">Message processor messages are used when running cloud and edge scale units for [manufacturing workloads](cloud-edge-workload-manufacturing.md) and [warehouse management workloads](cloud-edge-workload-warehousing.md).</span></span>

<span data-ttu-id="7b0df-105">会有大量数据在中心和缩放单元部署环境之间进行交换以保持同步，但是 *消息处理器* 将仅处理其中的少数数据交换。</span><span class="sxs-lookup"><span data-stu-id="7b0df-105">A large amount of data is exchanged between the hub and scale unit deployment environments to keep them in sync, but only a few of these data exchanges will be processed by the *message processor*.</span></span> <span data-ttu-id="7b0df-106">您可以转到 **系统管理 > 消息处理器 > 消息处理器消息** 查看消息处理器处理的消息。</span><span class="sxs-lookup"><span data-stu-id="7b0df-106">You can view the messages processed by the message processor by going to **System administration > Message processor > Message processor messages**.</span></span>

## <a name="message-grid-columns-and-filters"></a><span data-ttu-id="7b0df-107">消息网格列和筛选器</span><span class="sxs-lookup"><span data-stu-id="7b0df-107">Message grid columns and filters</span></span>

<span data-ttu-id="7b0df-108">您可以使用 **消息处理器消息** 页顶部的字段帮助查找要查找的任何特定消息。</span><span class="sxs-lookup"><span data-stu-id="7b0df-108">You can use the fields at the top of the **Message processor messages** page to help find any particular messages you are looking for.</span></span> <span data-ttu-id="7b0df-109">这些筛选器中的大多数与消息网格中的列标题匹配。</span><span class="sxs-lookup"><span data-stu-id="7b0df-109">Most of these filters match the column headings in the message grid.</span></span> <span data-ttu-id="7b0df-110">提供以下筛选器和列标题：</span><span class="sxs-lookup"><span data-stu-id="7b0df-110">The following filters and column headings are available:</span></span>

- <span data-ttu-id="7b0df-111">**消息类型** – 指定消息的类型。</span><span class="sxs-lookup"><span data-stu-id="7b0df-111">**Message type** – Specifies the type of message.</span></span>
- <span data-ttu-id="7b0df-112">**消息队列** – 指定要处理其中的消息的队列的名称。</span><span class="sxs-lookup"><span data-stu-id="7b0df-112">**Message queue** – Specifies the name of the queue in which the message is to be processed.</span></span> <span data-ttu-id="7b0df-113">提供以下队列：</span><span class="sxs-lookup"><span data-stu-id="7b0df-113">The following queues are provided:</span></span>
  - <span data-ttu-id="7b0df-114">*缩放单元到中心*</span><span class="sxs-lookup"><span data-stu-id="7b0df-114">*Scale unit to hub*</span></span>
  - <span data-ttu-id="7b0df-115">*中心到仓库执行缩放单元*</span><span class="sxs-lookup"><span data-stu-id="7b0df-115">*Hub to warehouse execution scale unit*</span></span>
  - <span data-ttu-id="7b0df-116">*中心到制造执行缩放单元*</span><span class="sxs-lookup"><span data-stu-id="7b0df-116">*Hub to manufacturing execution scale unit*</span></span>
- <span data-ttu-id="7b0df-117">**消息状态** – 指定消息的状态。</span><span class="sxs-lookup"><span data-stu-id="7b0df-117">**Message state** – Specifies the state of the message.</span></span> <span data-ttu-id="7b0df-118">存在以下状态：</span><span class="sxs-lookup"><span data-stu-id="7b0df-118">The following states exists:</span></span>
  - <span data-ttu-id="7b0df-119">*已排队* – 消息已准备好由消息处理器处理。</span><span class="sxs-lookup"><span data-stu-id="7b0df-119">*Queued* – The message is ready to be processed by the message processor.</span></span>
  - <span data-ttu-id="7b0df-120">*已处理* – 消息已由消息处理器成功处理。</span><span class="sxs-lookup"><span data-stu-id="7b0df-120">*Processed* – The message was successfully processed by the message processor.</span></span>
  - <span data-ttu-id="7b0df-121">*已取消* – 消息已处理，但处理失败。</span><span class="sxs-lookup"><span data-stu-id="7b0df-121">*Canceled* – The message was processed, but processing failed.</span></span>
- <span data-ttu-id="7b0df-122">**消息内容** – 此筛选器对消息内容进行全文搜索。</span><span class="sxs-lookup"><span data-stu-id="7b0df-122">**Message content** – This filter does a full-text search of message content.</span></span> <span data-ttu-id="7b0df-123">（消息内容未在网格中显示。）此筛选器将大多数特殊符号（例如“-”）视为空格，并将所有空格字符视为布尔 OR 运算符。</span><span class="sxs-lookup"><span data-stu-id="7b0df-123">(Message content is not shown in the grid.) The filter treats most special symbols (such as "-") as spaces, and treats all space characters as Boolean OR operators.</span></span> <span data-ttu-id="7b0df-124">T=例如，这意味着如果您搜索等于“USMF-123456”的特定 `journalid` 值，系统将查找所有包含“USMF”或“123456”的消息，这可能是一个很长的列表。</span><span class="sxs-lookup"><span data-stu-id="7b0df-124">T=For example, this means if you search for a specific `journalid` value equal "USMF-123456", the system will find all messages that contain "USMF" or "123456", which is likely to be a long list.</span></span> <span data-ttu-id="7b0df-125">因此，最好只输入“123456”，因为这样会返回更具体的结果。</span><span class="sxs-lookup"><span data-stu-id="7b0df-125">Therefore, it would be better to enter just "123456" alone because that will return more specific results.</span></span>

## <a name="example-message-type-request-inventory-adjustment-financial-update"></a><span data-ttu-id="7b0df-126">示例消息类型：请求库存调整财务更新</span><span class="sxs-lookup"><span data-stu-id="7b0df-126">Example message type: Request inventory adjustment financial update</span></span>

<span data-ttu-id="7b0df-127">例如，*请求库存调整财务更新* 这一 **消息类型** 用于在工作人员使用仓库应用在缩放单元仓库管理工作负荷上[登记库存调整](cloud-edge-warehouse-inventory-adjustment.md)时，在中心创建和过帐盘点日记帐。</span><span class="sxs-lookup"><span data-stu-id="7b0df-127">For example, the **Message type** *Request inventory adjustment financial update* is used to create and post a counting journal on the hub when a worker uses the warehouse app to [register an inventory adjustment](cloud-edge-warehouse-inventory-adjustment.md) on a scale unit warehouse management workload.</span></span> <span data-ttu-id="7b0df-128">由于此特定流程源自缩放单元，因此 **消息队列** 字段将显示值 *缩放单元到中心*。</span><span class="sxs-lookup"><span data-stu-id="7b0df-128">Because this specific process originates from a scale unit, the **Message queue** field will show the value *Scale unit to hub*.</span></span>

<span data-ttu-id="7b0df-129">对于此消息类型，缩放单元工作负荷将消息记录为仓库应用库存调整操作的一部分。</span><span class="sxs-lookup"><span data-stu-id="7b0df-129">For this message type, a scale unit workload records the message as part of a warehouse app inventory adjustment operation.</span></span> <span data-ttu-id="7b0df-130">然后，消息数据将作为用于 [Commerce data exchange 体系结构](../../commerce/commerce-architecture.md)的同一流程的一部分转移到中心。</span><span class="sxs-lookup"><span data-stu-id="7b0df-130">The message data is then transferred to the hub as part of the same process used for the [Commerce data exchange architecture](../../commerce/commerce-architecture.md).</span></span> <span data-ttu-id="7b0df-131">消息将更新为 **消息状态** 显示 *已排队*。</span><span class="sxs-lookup"><span data-stu-id="7b0df-131">The message will be updated to show **Message state** as *Queued*.</span></span> <span data-ttu-id="7b0df-132">然后，消息处理器将尝试处理消息，如果成功，会将 **消息状态** 更新为 *已处理*，如果失败，则更新为 *已取消*。</span><span class="sxs-lookup"><span data-stu-id="7b0df-132">The message processor then attempts to process the message and updates the **Message state** to *Processed* on success, or *Canceled* on failure.</span></span>

## <a name="view-the-message-log-message-content-and-details"></a><span data-ttu-id="7b0df-133">查看消息日志、消息内容和详细信息</span><span class="sxs-lookup"><span data-stu-id="7b0df-133">View the message log, message content, and details</span></span>

<span data-ttu-id="7b0df-134">您可以通过以下方式查找有关消息的详细信息：在网格中选择该消息，然后打开消息网格下的 **日志** 或 **消息内容** 选项卡，其中会显示每个处理事件。</span><span class="sxs-lookup"><span data-stu-id="7b0df-134">You can find detailed information about a message by selecting it in the grid and then opening the **Log** or **Message content** tabs under the message grid, where each processing event is shown.</span></span>

<span data-ttu-id="7b0df-135">**消息内容** 取决于 **消息类型**，因此具有不同的文本长度。</span><span class="sxs-lookup"><span data-stu-id="7b0df-135">The **Message content** depends on the **Message type** and will therefore have different text length.</span></span> <span data-ttu-id="7b0df-136">典型的消息内容文本将以 **{** 开头，以 **}** 结尾，中间有字段名称（如 `journalId`），后跟 **:** 和一个值（如 *USMF-123456*）。</span><span class="sxs-lookup"><span data-stu-id="7b0df-136">A typical message content text will start with a **{** and end with a **}** and in between have field names such as `journalId` followed by a **:** and a value such as *USMF-123456*.</span></span>

<span data-ttu-id="7b0df-137">**日志** 选项卡上的工具栏包括以下按钮：</span><span class="sxs-lookup"><span data-stu-id="7b0df-137">The toolbar on the **Log** tab includes the following buttons:</span></span>

- <span data-ttu-id="7b0df-138">**日志** – 显示处理结果。</span><span class="sxs-lookup"><span data-stu-id="7b0df-138">**Log** – Displays the processing results.</span></span> <span data-ttu-id="7b0df-139">这对于理解 **处理结果** 为 *失败* 的消息为何处理失败的原因特别有用。</span><span class="sxs-lookup"><span data-stu-id="7b0df-139">This is especially helpful for understanding the reasons for a processing failure for messages having a **Processing result** of *Failed*.</span></span>
- <span data-ttu-id="7b0df-140">**捆绑** – 多个消息处理操作可以作为同一个批处理流程的一部分运行。</span><span class="sxs-lookup"><span data-stu-id="7b0df-140">**Bundle** – Multiple message processing operations can run as part of the same batch process.</span></span> <span data-ttu-id="7b0df-141">选择此按钮可以查看此详细数据。</span><span class="sxs-lookup"><span data-stu-id="7b0df-141">Select this button to view this detailed data.</span></span> <span data-ttu-id="7b0df-142">例如，您可以查看是否存在需要系统以特定顺序处理某些消息的依赖项。</span><span class="sxs-lookup"><span data-stu-id="7b0df-142">For example, you can see whether dependencies exist that require the system to process certain messages in a specific sequence.</span></span>

## <a name="message-processor-batch-job"></a><span data-ttu-id="7b0df-143">消息处理器批处理作业</span><span class="sxs-lookup"><span data-stu-id="7b0df-143">Message processor batch job</span></span>

<span data-ttu-id="7b0df-144">在运行云和边缘部署时，在创建新消息以进行处理时，将自动引发 *消息处理器* 批处理作业，因此，您应该无需手动计划此作业。</span><span class="sxs-lookup"><span data-stu-id="7b0df-144">When running a cloud and edge deployment, the *Message processor* batch job will automatically be evoked when a new message is created for processing, so you should not need to schedule this job manually.</span></span>

<span data-ttu-id="7b0df-145">如有必要，您可以转到 **系统管理 > 消息处理器 > 消息处理器** 来访问此批处理作业。</span><span class="sxs-lookup"><span data-stu-id="7b0df-145">If necessary, you can access the batch job by going to **System administration > Message  processor > Message processor**.</span></span>

## <a name="manually-process-or-cancel-a-message"></a><span data-ttu-id="7b0df-146">手动处理或取消消息</span><span class="sxs-lookup"><span data-stu-id="7b0df-146">Manually process or cancel a message</span></span>

<span data-ttu-id="7b0df-147">如果需要，您可以根据消息的当前状态手动处理或取消消息。</span><span class="sxs-lookup"><span data-stu-id="7b0df-147">If needed, you can manually process or cancel a message, depending on its current state.</span></span> <span data-ttu-id="7b0df-148">要执行此操作，在网格中选择消息，然后在操作窗格上选择 **处理** 或 **取消**</span><span class="sxs-lookup"><span data-stu-id="7b0df-148">To do so, select the message in the grid and then select **Process** or **Cancel** on the Action Pane</span></span>

## <a name="set-up-business-events-to-deliver-alerts-for-failed-processing-results"></a><span data-ttu-id="7b0df-149">设置业务事件以为失败的处理结果发送警报</span><span class="sxs-lookup"><span data-stu-id="7b0df-149">Set up business events to deliver alerts for failed processing results</span></span>

<span data-ttu-id="7b0df-150">除了筛选 **消息状态** 值 *已取消* 来查询失败的消息外，您还可以在中心设置[业务事件](../../fin-ops-core/dev-itpro/business-events/home-page.md)，来提醒您处理结果失败。</span><span class="sxs-lookup"><span data-stu-id="7b0df-150">In addition to filtering on the **Message state** value *Canceled* to inquire for failed messages, you can set up [Business events](../../fin-ops-core/dev-itpro/business-events/home-page.md) on the hub to alert you to failed processing results.</span></span> <span data-ttu-id="7b0df-151">要执行此操作，在 **业务事件目录** 页（**系统管理 > 设置 > 业务事件 > 业务事件目录**）上激活名为 *消息处理器消息已处理* 的业务事件。</span><span class="sxs-lookup"><span data-stu-id="7b0df-151">To do so, activate the business event named *Message processor message processed*  on the **Business events catalog** page (**System administration > Setup > Business events > Business events catalog**).</span></span>

<span data-ttu-id="7b0df-152">作为激活流程的一部分，系统将指导您指定事件是特定于一个还是所有法人，并提供必须首先定义的 **终结点名称**。</span><span class="sxs-lookup"><span data-stu-id="7b0df-152">As part of the activation process, you will be guided to specify whether the event is specific to one or all legal entities and provide an **Endpoint name**, which must be defined first.</span></span>

>[!NOTE]
> <span data-ttu-id="7b0df-153">如果将 **当业务事件发生时** 设置为 *Microsoft Power Automate*（比如不是 *HTTPS*），将基于 *Microsoft Power Automate* 设置在 Supply Chain Management 中自动创建 **终结点名称**。</span><span class="sxs-lookup"><span data-stu-id="7b0df-153">If **When a Business Event occurs** is set to *Microsoft Power Automate* (rather than *HTTPS*, for example), the **Endpoint name** will automatically be created in Supply Chain Management based on the *Microsoft Power Automate* setup.</span></span>

### <a name="microsoft-power-automate-example"></a><span data-ttu-id="7b0df-154">Microsoft Power Automate 示例</span><span class="sxs-lookup"><span data-stu-id="7b0df-154">Microsoft Power Automate example</span></span>

<span data-ttu-id="7b0df-155">在此示例中，将 **当业务事件发生时** 与 *Microsoft Power Automate* 配合使用，来发送包含信息日志消息和超链接的电子邮件，以打开中心部署中特定失败消息的 **消息处理器消息** 页。</span><span class="sxs-lookup"><span data-stu-id="7b0df-155">In this example, use **When a Business Event occurs** with *Microsoft Power Automate* sends emails containing InfoLog messages and hyperlinks to open the **Message processor messages** page for a specific failed message on the hub deployment.</span></span> <span data-ttu-id="7b0df-156">如果需要，您可以添加额外的逻辑来使用不同的渠道并行发送通知，并根据事件数据控制收件人。</span><span class="sxs-lookup"><span data-stu-id="7b0df-156">If needed, you can add extra logic to send the notifications in parallel using different channels and control the recipients based on the event data.</span></span>

1. <span data-ttu-id="7b0df-157">在 [Power Automate](https://preview.flow.microsoft.com) 中，为流触发器 **当业务事件发生时 - Fin & Ops App (Dynamics 365)** 创建一个新的自动化云端流，后跟 **分析 JSON** 和 **发送电子邮件** 步骤，如下图所示。</span><span class="sxs-lookup"><span data-stu-id="7b0df-157">In [Power Automate](https://preview.flow.microsoft.com), create a new automated cloud flow for the flow trigger **When a Business Event occurs - Fin & Ops App (Dynamics 365)** followed by the **Parse JSON** and **Send an email** steps, as shown in the following illustration.</span></span>

    :::image type="content" source="./media/cloud-edge-power-automate-example1.png" alt-text="Power Automate自动化云端流":::

1. <span data-ttu-id="7b0df-159">在 **当业务事件发生时** 步骤中，您可以查找或输入中心 **实例**，之后是 **类别**，然后是 \**业务事件\*\*\*消息处理器消息已处理*，如下图所示。</span><span class="sxs-lookup"><span data-stu-id="7b0df-159">In the **When a Business Event occurs** step, you can look up or enter the hub **Instance** following the **Category** and then the **Business event** *Message processor message processed*, as shown in the following illustration.</span></span>

    :::image type="content" source="./media/cloud-edge-power-automate-example2.png" alt-text="Power Automate 当业务事件发生时步骤":::

1. <span data-ttu-id="7b0df-161">对于 **分析 JSON** 步骤，输入定义扩展字段的 **架构**。</span><span class="sxs-lookup"><span data-stu-id="7b0df-161">For the **Parse JSON** step, enter a **Schema** that defines the extended fields.</span></span> <span data-ttu-id="7b0df-162">您可以使用 Supply Chain Management 中 **业务事件目录** 页上的 *下载架构* 选项，也可以从粘贴示例架构文本开始。</span><span class="sxs-lookup"><span data-stu-id="7b0df-162">You can use the *Download schema* option on the **Business events catalog** page in Supply Chain Management or start by pasting in the example schema text.</span></span> <span data-ttu-id="7b0df-163">下图之后提供了此示例文本。</span><span class="sxs-lookup"><span data-stu-id="7b0df-163">This example text is provided after the following illustration.</span></span>

    :::image type="content" source="./media/cloud-edge-power-automate-example3.png" alt-text="Power Automate 分析 JSON步骤":::

    ```json
    {
        "properties": {
            "BusinessEventId": {
                "type": "string"
            },
            "ControlNumber": {
                "type": "integer"
            },
            "EventId": {
                "type": "string"
            },
            "EventTime": {
                "type": "string"
            },
            "MajorVersion": {
                "type": "integer"
            },
            "MessageContent": {
                "type": "string"
            },
            "MessageDestinationCompanyId": {
                "type": "string"
            },
            "MessageDestinationOperationalSiteId": {
                "type": "string"
            },
            "MessageDestinationWarehouseId": {
                "type": "string"
            },
            "MessageDestinationWorkloadName": {
                "type": "string"
            },
            "MessageInfolog": {
                "type": "string"
            },
            "MessageProcessingResult": {
                "type": "string"
            },
            "MessageProcessingResultLabel": {
                "type": "string"
            },
            "MessageProcessorMessagePageUrl": {
                "type": "string"
            },
            "MessageQueue": {
                "type": "string"
            },
            "MessageQueueLabel": {
                "type": "string"
            },
            "MessageSourceCompanyId": {
                "type": "string"
            },
            "MessageSourceOperationalSiteId": {
                "type": "string"
            },
            "MessageSourceWarehouseId": {
                "type": "string"
            },
            "MessageSourceWorkloadName": {
                "type": "string"
            },
            "MessageState": {
                "type": "string"
            },
            "MessageStateLabel": {
                "type": "string"
            },
            "MessageType": {
                "type": "string"
            },
            "MessageTypeLabel": {
                "type": "string"
            },
            "MinorVersion": {
                "type": "integer"
            }
        },
        "type": "object"
    }
    ```

1. <span data-ttu-id="7b0df-165">在 **发送电子邮件** 步骤中，您可以选择各个字段，也可以从将电子邮件正文示例粘贴到 **正文** 字段中开始。</span><span class="sxs-lookup"><span data-stu-id="7b0df-165">In the **Send an email** step, you can select the individual fields or start by pasting the email body example into the **Body** field.</span></span> <span data-ttu-id="7b0df-166">下图之后提供了此示例。</span><span class="sxs-lookup"><span data-stu-id="7b0df-166">This example is provided after the following illustration.</span></span>

    :::image type="content" source="./media/cloud-edge-power-automate-example4.png" alt-text="Power Automate 发送电子邮件步骤":::

    ```plaintext
    Message queue: @{body('Parse_JSON')?['MessageQueue']}
    Message queue label: @{body('Parse_JSON')?['MessageQueueLabel']}
    Message type: @{body('Parse_JSON')?['MessageQueueType']}
    Message type label: @{body('Parse_JSON')?['MessageQueueTypeLabel']}
    Message content: @{body('Parse_JSON')?['MessageContent']}
    Message state: @{body('Parse_JSON')?['MessageState']}
    Message state label: @{body('Parse_JSON')?['MessageStateLabel']}
    Message processing result: @{body('Parse_JSON')?['MessageProcessingResult']}
    Message processing result label: @{body('Parse_JSON')?['MessageProcessingResultLabel']}
    Message infolog: @{body('Parse_JSON')?['MessageInfolog']}
    Message source company ID: @{body('Parse_JSON')?['MessageSourceCompanyId']}
    Message source workload name: @{body('Parse_JSON')?['MessageSourceWorkloadName']}
    Message source site ID: @{body('Parse_JSON')?['MessageSourceOperationalSiteId']}
    Message source warehouse ID: @{body('Parse_JSON')?['MessageSourceWarehouseId']}
    Message destination company ID: @{body('Parse_JSON')?['MessageDestinationCompanyId']}
    Message destination workload name: @{body('Parse_JSON')?['MessageDestinationWorkloadName']}
    Message destination site ID: @{body('Parse_JSON')?['MessageDestinationOperationalSiteId']}
    Message destination warehouse ID: @{body('Parse_JSON')?['MessageDestinationWarehouseId']}
    Message processor message page URL: @{body('Parse_JSON')?['MessageProcessorMessagePageUrl']}
    ```

1. <span data-ttu-id="7b0df-168">保存业务事件时，它将自动被激活，可以用作 Supply Chain Management 的一部分。</span><span class="sxs-lookup"><span data-stu-id="7b0df-168">When you save the business event, it will automatically be activated and ready to use as part of Supply Chain Management.</span></span>
