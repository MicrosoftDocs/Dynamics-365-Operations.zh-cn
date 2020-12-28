---
title: 创建预警规则
description: 此主题提供有关预警的信息，并说明如何创建预警规则以通知您各个事件（例如到达的日期或发生的特定更改）。
author: tjvass
manager: AnnBe
ms.date: 10/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EventCreateRule
audience: Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2018-3-30
ms.dyn365.ops.version: Platform update 15
ms.openlocfilehash: 4fe97ca8e1eecdc064ad4d21d5acdeade9f33d9c
ms.sourcegitcommit: f5e31c34640add6d40308ac1365cc0ee60e60e24
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/08/2020
ms.locfileid: "4694487"
---
# <a name="create-alert-rules"></a><span data-ttu-id="18241-103">创建预警规则</span><span class="sxs-lookup"><span data-stu-id="18241-103">Create alert rules</span></span>

[!include [banner](../includes/banner.md)]

## <a name="getting-started"></a><span data-ttu-id="18241-104">入门</span><span class="sxs-lookup"><span data-stu-id="18241-104">Getting started</span></span>

<span data-ttu-id="18241-105">设置预警规则之前，请确定何时或在何种情况下您想要收到预警。</span><span class="sxs-lookup"><span data-stu-id="18241-105">Before you set up an alert rule, decide when or in what situations you want to receive alerts.</span></span> <span data-ttu-id="18241-106">当您确定要通知的事件时，找到出现引起该事件的数据的页面。</span><span class="sxs-lookup"><span data-stu-id="18241-106">When you know which event you want to be notified about, find the page where the data that causes that event appears.</span></span> <span data-ttu-id="18241-107">事件可以是即将来临的日期，也可以是发生的特定更改。</span><span class="sxs-lookup"><span data-stu-id="18241-107">The event can be a date that arrives or a specific change that occurs.</span></span> <span data-ttu-id="18241-108">因此，您必须找到指定此日期或者显示更改的字段或创建的新记录的页面。</span><span class="sxs-lookup"><span data-stu-id="18241-108">Therefore, you must find the page where the date is specified, or where the field that changes or the new record that is created appears.</span></span> <span data-ttu-id="18241-109">获得此信息之后，您便可以创建预警规则。</span><span class="sxs-lookup"><span data-stu-id="18241-109">After you have this information, you can create the alert rule.</span></span>

<span data-ttu-id="18241-110">创建预警规则时，您可以定义触发预警前必须满足的条件。</span><span class="sxs-lookup"><span data-stu-id="18241-110">When you create an alert rule, you define the criteria that must be met before an alert is triggered.</span></span> <span data-ttu-id="18241-111">条件基本是事件发生与特定条件的满足之间的匹配。</span><span class="sxs-lookup"><span data-stu-id="18241-111">Criteria is basically the match between the occurrence of an event and the fulfillment of specific conditions.</span></span> <span data-ttu-id="18241-112">发生事件时，系统将根据设置的条件开始执行检查。</span><span class="sxs-lookup"><span data-stu-id="18241-112">When an event occurs, the system starts to perform a check according to the conditions that are set up.</span></span>

## <a name="ensure-the-alert-batch-jobs-are-running"></a><span data-ttu-id="18241-113">确保预警批处理作业正在运行</span><span class="sxs-lookup"><span data-stu-id="18241-113">Ensure the alert batch jobs are running</span></span>

<span data-ttu-id="18241-114">需要运行数据变化和到期日期预警的批处理作业，才能处理预警条件和发送通知。</span><span class="sxs-lookup"><span data-stu-id="18241-114">The batch jobs for data change and due date alerts need to be running for the alert conditions to be processed and the notifications to be sent.</span></span> <span data-ttu-id="18241-115">若要运行批处理作业，请转到 **系统管理** > **定期任务** > **预警**，然后为 **基于变化的预警** 和/或 **到期日期预警** 添加新的批处理作业。</span><span class="sxs-lookup"><span data-stu-id="18241-115">To run batch jobs, go to **System administration** > **Periodic tasks** > **Alerts** and add a new batch job for **Change based alerts** and/or **Due date alerts**.</span></span> <span data-ttu-id="18241-116">如果需要频繁运行的长期批处理作业，请选择 **重复执行**，然后设置 **无结束日期**，并将 **重复执行模式** 设置为 **分钟**，将 **计数** 设置为 **1**。</span><span class="sxs-lookup"><span data-stu-id="18241-116">If a long and frequently running batch job is needed, select **Recurrence** and set **No end date** with a **Recurrence pattern** of **Minutes** and a **Count** of **1**.</span></span>

## <a name="events"></a><span data-ttu-id="18241-117">事件</span><span class="sxs-lookup"><span data-stu-id="18241-117">Events</span></span>

<span data-ttu-id="18241-118">触发预警规则的事件可以是即将来临的日期，也可以是发生的具体更改。</span><span class="sxs-lookup"><span data-stu-id="18241-118">The event that triggers an alert rule can be a date that arrives or a specific change that occurs.</span></span> <span data-ttu-id="18241-119">事件的触发器在 **创建预警规则** 对话框的 **在以下情况下提示** 快速选项卡上定义。</span><span class="sxs-lookup"><span data-stu-id="18241-119">Triggers for events are defined on the **Alert me when** FastTab of the **Create alert rule** dialog box.</span></span> <span data-ttu-id="18241-120">特定字段可用的事件，具体取决于选择的触发器。</span><span class="sxs-lookup"><span data-stu-id="18241-120">The events that are available for a particular field depend on the trigger that is selected.</span></span>

<span data-ttu-id="18241-121">例如，如果您在为 **开始日期** 字段设置预警规则，适用到期日期事件。</span><span class="sxs-lookup"><span data-stu-id="18241-121">For example, if you're setting up an alert rule for the **Start date** field, due date events are appropriate.</span></span> <span data-ttu-id="18241-122">因此，该字段可使用 **在以下范围内到期** 事件类型。</span><span class="sxs-lookup"><span data-stu-id="18241-122">Therefore, the **is due in** event type is available for that field.</span></span> <span data-ttu-id="18241-123">但是，对于 **成本中心** 等字段，到期日期事件不适用。</span><span class="sxs-lookup"><span data-stu-id="18241-123">However, for a field such as **Cost center**, a due date event isn't appropriate.</span></span> <span data-ttu-id="18241-124">因此，**在以下范围内到期** 事件类型不可用。</span><span class="sxs-lookup"><span data-stu-id="18241-124">Therefore, the **is due in** event type isn't available.</span></span> <span data-ttu-id="18241-125">而 **已更改** 事件类型可用。</span><span class="sxs-lookup"><span data-stu-id="18241-125">Instead, the **has changed** event type is available.</span></span>

## <a name="event-types"></a><span data-ttu-id="18241-126">事件类型</span><span class="sxs-lookup"><span data-stu-id="18241-126">Event types</span></span>

<span data-ttu-id="18241-127">可以发生三类事件：</span><span class="sxs-lookup"><span data-stu-id="18241-127">Three types of events can occur:</span></span>

- <span data-ttu-id="18241-128">**创建类型和删除类型的事件** – 这些事件在创建或删除记录时触发预警。</span><span class="sxs-lookup"><span data-stu-id="18241-128">**Create-type and delete-type events** – These events trigger an alert when a record is created or deleted.</span></span>
- <span data-ttu-id="18241-129">**更新类型事件** – 这些事件在特定字段的数据发生更改时触发预警。</span><span class="sxs-lookup"><span data-stu-id="18241-129">**Update-type events** – These events trigger an alert when the data in a specific field changes.</span></span>
- <span data-ttu-id="18241-130">**到期日期类型事件** – 达到某个日期时这些事件会触发预警。</span><span class="sxs-lookup"><span data-stu-id="18241-130">**Due date-type events** – These events trigger an alert when a date arrives.</span></span>
    
<span data-ttu-id="18241-131">发生的更改可由用户启动。</span><span class="sxs-lookup"><span data-stu-id="18241-131">Changes that occur can be initiated by a user.</span></span> <span data-ttu-id="18241-132">例如，用户更改采购订单的交货日期。</span><span class="sxs-lookup"><span data-stu-id="18241-132">For example, a user changes the delivery date of a purchase order.</span></span> <span data-ttu-id="18241-133">或者，更改可作为流程的一部分发生。</span><span class="sxs-lookup"><span data-stu-id="18241-133">Alternatively, changes can occur as part of a process.</span></span> <span data-ttu-id="18241-134">例如，某页面的 **状态** 字段发生更改，以反映系统中各个流程的生命周期。</span><span class="sxs-lookup"><span data-stu-id="18241-134">For example, the **Status** field on a page changes to reflect the life cycle of various processes in the system.</span></span>

## <a name="conditions"></a><span data-ttu-id="18241-135">条件</span><span class="sxs-lookup"><span data-stu-id="18241-135">Conditions</span></span>

<span data-ttu-id="18241-136">在 **创建预警规则** 对话框的 **提示以下事项** 快速选项卡上，您可以使用条件来控制您什么时候收到与事件有关的预警。</span><span class="sxs-lookup"><span data-stu-id="18241-136">On the **Alert me for** FastTab in the **Create alert rule** dialog box, you can use conditions to control when you're alerted about events.</span></span>

<span data-ttu-id="18241-137">例如，您可以指定采购订单状态发生更改时系统应向您发出预警，但是仅在状态匹配一组特定条件的情况下。</span><span class="sxs-lookup"><span data-stu-id="18241-137">For example, you can specify that the system should alert you when the status of purchase orders changes, but only if the status matches a specific set of conditions.</span></span> <span data-ttu-id="18241-138">特别是当您要在采购订单的状态设置为 **已收到** 时收到预警的情况。</span><span class="sxs-lookup"><span data-stu-id="18241-138">Specifically, you want to be alerted when the status of a purchase order is set to **Received**.</span></span> <span data-ttu-id="18241-139">此状态更改是触发预警的事件。</span><span class="sxs-lookup"><span data-stu-id="18241-139">This change in status is the event that triggers the alert.</span></span>

<span data-ttu-id="18241-140">然后，您必须确定您要收到有关哪些采购订单的预警。</span><span class="sxs-lookup"><span data-stu-id="18241-140">Next, you must decide which purchase orders you want to be alerted about.</span></span> <span data-ttu-id="18241-141">例如，您可以选择以下选项之一：</span><span class="sxs-lookup"><span data-stu-id="18241-141">For example, you can select one of the following options.</span></span> <span data-ttu-id="18241-142">这些选项为预警规则定义了条件。</span><span class="sxs-lookup"><span data-stu-id="18241-142">These options define the conditions for the alert rule.</span></span>

- <span data-ttu-id="18241-143">**当前所选记录** – 您在特定采购订单的状态更改为 **已接收** 时收到预警。</span><span class="sxs-lookup"><span data-stu-id="18241-143">**Current selected record** – You receive an alert when the status of a specific purchase order changes to **Received**.</span></span>
- <span data-ttu-id="18241-144">**所有记录** – 当活动页视图中某个项目的采购订单状态更改时您将收到预警。</span><span class="sxs-lookup"><span data-stu-id="18241-144">**All records** – You receive an alert when the status of a purchase order is changed for an item in the active page view.</span></span> <span data-ttu-id="18241-145">您可以在页面上使用高级筛选为一组特定记录创建规则。</span><span class="sxs-lookup"><span data-stu-id="18241-145">You can use the advanced filtering that is available on the page to create rules for a specific set of records.</span></span> <span data-ttu-id="18241-146">例如，您可以创建为特定客户组中客户的所有采购订单触发的预警。</span><span class="sxs-lookup"><span data-stu-id="18241-146">For example, you can create an alert that is triggered for all purchase orders for the customers in a specific customer group.</span></span>
    
## <a name="expiry-of-rule"></a><span data-ttu-id="18241-147">规则到期</span><span class="sxs-lookup"><span data-stu-id="18241-147">Expiry of rule</span></span>

<span data-ttu-id="18241-148">在 **创建预警规则** 对话框的 **在以下时间之前提示** 快速选项卡上，可以指定预警规则应处于有效状态的时长。</span><span class="sxs-lookup"><span data-stu-id="18241-148">On the **Alert me until** FastTab of the **Create alert rule** dialog box, you can specify how long the alert rule should be active.</span></span>

## <a name="alert-contents"></a><span data-ttu-id="18241-149">预警内容</span><span class="sxs-lookup"><span data-stu-id="18241-149">Alert contents</span></span>

<span data-ttu-id="18241-150">在 **创建预警规则** 对话框的 **提示以下内容** 快速选项卡上，可以指定预警消息应使用的主题文本和消息。</span><span class="sxs-lookup"><span data-stu-id="18241-150">On the **Alert me with** FastTab of the **Create alert rule** dialog box, you can specify the subject text and message text that the alert messages should use.</span></span>

## <a name="user-id"></a><span data-ttu-id="18241-151">用户 ID</span><span class="sxs-lookup"><span data-stu-id="18241-151">User ID</span></span>

<span data-ttu-id="18241-152">在 **创建预警规则** 对话框的 **提示以下内容** 快速选项卡上，可以指定应接收预警消息的用户。</span><span class="sxs-lookup"><span data-stu-id="18241-152">On the **Alert me with** FastTab of the **Create alert rule** dialog box, you can specify which user should receive the alert messages.</span></span> <span data-ttu-id="18241-153">默认状态下，将选择您的用户 ID。</span><span class="sxs-lookup"><span data-stu-id="18241-153">By default, your user ID is selected.</span></span> <span data-ttu-id="18241-154">只有组织管理员才能更改用户是否可接收预警。</span><span class="sxs-lookup"><span data-stu-id="18241-154">The ability to change the user receiving the alert is restricted to organization administrators.</span></span>

## <a name="alerts-as-business-events"></a><span data-ttu-id="18241-155">业务事件预警</span><span class="sxs-lookup"><span data-stu-id="18241-155">Alerts as business events</span></span>

<span data-ttu-id="18241-156">可以使用业务事件框架在外部发送预警。</span><span class="sxs-lookup"><span data-stu-id="18241-156">Alerts can be sent externally using the business events framework.</span></span> <span data-ttu-id="18241-157">创建预警时，将 **组织范围** 设置为 **否**，将 **外部发送** 设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="18241-157">When creating an alert, set **Organization-wide** to **No** and set **Send externally** to **Yes**.</span></span> <span data-ttu-id="18241-158">设置了用于触发业务事件的预警之后，可以使用 Finance and Operations 连接器中的 **当业务事件发生时** 触发器触发 Power Automate 中内置的流，或通过 **业务事件对话框** 将事件显式发送给业务事件终结点。</span><span class="sxs-lookup"><span data-stu-id="18241-158">After you have the alert triggering the business event, you can trigger a flow built in Power Automate using the **When a business event occurs** trigger on the Finance and Operations connector, or explicitly send the event to a business events endpoint via the **Business events catalog**.</span></span>

## <a name="create-an-alert-rule"></a><span data-ttu-id="18241-159">创建预警规则</span><span class="sxs-lookup"><span data-stu-id="18241-159">Create an alert rule</span></span>

0. <span data-ttu-id="18241-160">确保预警批处理作业正在运行（参见上文）。</span><span class="sxs-lookup"><span data-stu-id="18241-160">Ensure the alert batch jobs are running (see above).</span></span>
1. <span data-ttu-id="18241-161">打开包含要监控的数据的页面。</span><span class="sxs-lookup"><span data-stu-id="18241-161">Open the page that contains the data to monitor.</span></span>
2. <span data-ttu-id="18241-162">在操作窗格上，在 **选项** 选项卡，在 **共享** 组中，选择 **创建预警规则**。</span><span class="sxs-lookup"><span data-stu-id="18241-162">On the Action Pane, on the **Options** tab, in the **Share** group, select **Create alert rule**.</span></span>
3. <span data-ttu-id="18241-163">在 **创建预警规则** 对话框中，在 **字段** 字段中，选择要监控的字段。</span><span class="sxs-lookup"><span data-stu-id="18241-163">In the **Create alert rule** dialog box, in the **Field** field, select the field to monitor.</span></span>
4. <span data-ttu-id="18241-164">在 **事件** 字段中，选择事件的类型。</span><span class="sxs-lookup"><span data-stu-id="18241-164">In the **Event** field, select the type of event.</span></span>
5. <span data-ttu-id="18241-165">在 **提示以下事项** 快速选项卡上，选择所需选项。</span><span class="sxs-lookup"><span data-stu-id="18241-165">On the **Alert me for** FastTab, select the desired option.</span></span> <span data-ttu-id="18241-166">如果要将预警作为业务事件发送，请确保 **组织范围** 设置为 **否**。</span><span class="sxs-lookup"><span data-stu-id="18241-166">If you want to send the alert as a business event, ensure that **Organization-wide** is set to **No**.</span></span>
6. <span data-ttu-id="18241-167">如果预警规则应在特定日期失效，则在 **在以下时间之前提示** 快速选项卡上选择某一结束日期。</span><span class="sxs-lookup"><span data-stu-id="18241-167">If the alert rule should become inactive on a specific date, on the **Alert me until** FastTab, select an end date.</span></span>
7. <span data-ttu-id="18241-168">在 **提示以下内容** 快速选项卡上，在 **主题** 字段中，接受默认的电子邮件主题标题或输入新的主题。</span><span class="sxs-lookup"><span data-stu-id="18241-168">On the **Alert me with** FastTab, in the **Subject** field, accept the default subject heading for the email message, or enter a new subject.</span></span> <span data-ttu-id="18241-169">文本用作触发预警时所收到电子邮件的主题标题。</span><span class="sxs-lookup"><span data-stu-id="18241-169">The text is used as the subject heading for the email message that you receive when an alert is triggered.</span></span> <span data-ttu-id="18241-170">如果要将预警作为业务事件发送，请将 **外部发送** 设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="18241-170">If you want to send the alert as a business event, set **Send externally** to **Yes**.</span></span>
8. <span data-ttu-id="18241-171">在 **消息** 字段中，输入可选消息</span><span class="sxs-lookup"><span data-stu-id="18241-171">In the **Message** field, enter an optional message.</span></span> <span data-ttu-id="18241-172">文本用作触发预警时收到的消息。</span><span class="sxs-lookup"><span data-stu-id="18241-172">The text is used as the message that you receive when an alert is triggered.</span></span>
9. <span data-ttu-id="18241-173">选择 **确定** 保存设置和创建预警规则。</span><span class="sxs-lookup"><span data-stu-id="18241-173">Select **OK** to save the settings and create the alert rule.</span></span>

## <a name="limitations-and-workarounds"></a><span data-ttu-id="18241-174">限制和解决方法</span><span class="sxs-lookup"><span data-stu-id="18241-174">Limitations and workarounds</span></span>

### <a name="workaround-for-creating-alerts-for-the-secondary-data-sources-of-a-form"></a><span data-ttu-id="18241-175">为窗体的辅助数据源创建预警的解决方法</span><span class="sxs-lookup"><span data-stu-id="18241-175">Workaround for creating alerts for the secondary data sources of a form</span></span>
<span data-ttu-id="18241-176">无法为窗体上的某些辅助数据源创建预警。</span><span class="sxs-lookup"><span data-stu-id="18241-176">Alerts can't be created for some secondary data sources on forms.</span></span> <span data-ttu-id="18241-177">例如，当在客户或供应商过帐配置文件窗体上创建预警时，仅标题（客户分类帐或供应商分类帐）上的字段可用，而维度帐户不可用。</span><span class="sxs-lookup"><span data-stu-id="18241-177">For example, when creating alerts on the customer or vendor posting profiles form, only the fields on the header (CustLedger or VendLedger) are available and not the dimension accounts.</span></span> <span data-ttu-id="18241-178">此限制的解决方法是使用 **SysTableBrowser** 打开该表作为主要数据源。</span><span class="sxs-lookup"><span data-stu-id="18241-178">The workaround for this limitation is to use **SysTableBrowser** to open that table as primary data source.</span></span> 
1. <span data-ttu-id="18241-179">在 **SysTableBrowser** 窗体中打开该表。</span><span class="sxs-lookup"><span data-stu-id="18241-179">Open the table in the **SysTableBrowser** form.</span></span>
    ```
        https://<EnvironmentURL>/?cmp=USMF&mi=SysTableBrowser&TableName=<TableName>
    ```
2. <span data-ttu-id="18241-180">从 SysTableBrowser 窗体创建预警。</span><span class="sxs-lookup"><span data-stu-id="18241-180">Create an alert from the SysTableBrowser form.</span></span>

