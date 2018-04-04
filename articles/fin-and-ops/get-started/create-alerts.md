---
title: "创建预警"
description: "此主题提供有关预警的信息，并说明如何创建预警规则以通知您各个事件（例如到达的日期或发生的特定更改）。"
author: tjvass
manager: AnnBe
ms.date: 03/20/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EventCreateRule
audience: Application user
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2018-3-30
ms.dyn365.ops.version: Platform update 15
ms.translationtype: HT
ms.sourcegitcommit: 454368ab5a467002ebf973db97fd98e31885dfe0
ms.openlocfilehash: 5bcd02e08a4ce5b601615b39bf95362cf92d3fec
ms.contentlocale: zh-cn
ms.lasthandoff: 03/23/2018

---

# <a name="create-alerts"></a><span data-ttu-id="6718b-103">创建预警</span><span class="sxs-lookup"><span data-stu-id="6718b-103">Create alerts</span></span>

[!include[banner](../includes/banner.md)]

[!include[banner](../includes/pre-release.md)] 

## <a name="getting-started"></a><span data-ttu-id="6718b-104">入门</span><span class="sxs-lookup"><span data-stu-id="6718b-104">Getting started</span></span>
<span data-ttu-id="6718b-105">设置预警规则之前，请确定何时或在何种情况下您想要收到预警。</span><span class="sxs-lookup"><span data-stu-id="6718b-105">Before you set up an alert rule, decide when or in what situations you want to receive alerts.</span></span> <span data-ttu-id="6718b-106">当您确定要通知的事件时，在 Microsoft Dynamics 365 for Finance and Operations 中，找到出现引起该事件的数据的页面。</span><span class="sxs-lookup"><span data-stu-id="6718b-106">When you know which event you want to be notified about, in Microsoft Dynamics 365 for Finance and Operations find the page where the data that causes that event appears.</span></span> <span data-ttu-id="6718b-107">事件可以是即将来临的日期，也可以是发生的特定更改。</span><span class="sxs-lookup"><span data-stu-id="6718b-107">The event can be a date that arrives or a specific change that occurs.</span></span> <span data-ttu-id="6718b-108">因此，您必须找到指定此日期或者显示更改的字段或创建的新记录的页面。</span><span class="sxs-lookup"><span data-stu-id="6718b-108">Therefore, you must find the page where the date is specified, or where the field that changes or the new record that is created appears.</span></span> <span data-ttu-id="6718b-109">获得此信息之后，您便可以创建预警规则。</span><span class="sxs-lookup"><span data-stu-id="6718b-109">After you have this information, you can create the alert rule.</span></span>

<span data-ttu-id="6718b-110">创建预警规则时，您可以定义触发预警前必须满足的条件。</span><span class="sxs-lookup"><span data-stu-id="6718b-110">When you create an alert rule, you define the criteria that must be met before an alert is triggered.</span></span> <span data-ttu-id="6718b-111">可将条件视为事件发生与特定条件的满足之间的匹配。</span><span class="sxs-lookup"><span data-stu-id="6718b-111">You can think of criteria as a match between the occurrence of an event and the fulfillment of specific conditions.</span></span> <span data-ttu-id="6718b-112">发生事件时，系统将根据在 Finance and Operations 中设置的条件开始执行检查。</span><span class="sxs-lookup"><span data-stu-id="6718b-112">When an event occurs, the system starts to perform a check according to the conditions that are set up in Finance and Operations.</span></span>

## <a name="events"></a><span data-ttu-id="6718b-113">事件</span><span class="sxs-lookup"><span data-stu-id="6718b-113">Events</span></span>
<span data-ttu-id="6718b-114">触发预警规则的事件可以是即将来临的日期，也可以是发生的具体更改。</span><span class="sxs-lookup"><span data-stu-id="6718b-114">The event that triggers an alert rule can be a date that arrives or a specific change that occurs.</span></span> <span data-ttu-id="6718b-115">事件的触发器在**创建预警规则**对话框的**在以下情况下提示**快速选项卡上定义。</span><span class="sxs-lookup"><span data-stu-id="6718b-115">Triggers for events are defined on the **Alert me when** FastTab of the **Create alert rule** dialog box.</span></span> <span data-ttu-id="6718b-116">特定字段可用的事件，具体取决于选择的触发器。</span><span class="sxs-lookup"><span data-stu-id="6718b-116">The events that are available for a particular field depend on the trigger that is selected.</span></span>

<span data-ttu-id="6718b-117">例如，如果您在为**开始日期**字段设置预警规则，适用到期日期事件。</span><span class="sxs-lookup"><span data-stu-id="6718b-117">For example, if you're setting up an alert rule for the **Start date** field, due date events are appropriate.</span></span> <span data-ttu-id="6718b-118">因此，该字段可使用**在以下范围内到期**事件类型。</span><span class="sxs-lookup"><span data-stu-id="6718b-118">Therefore, the **is due in** event type is available for that field.</span></span> <span data-ttu-id="6718b-119">但是，对于**成本中心**等字段，到期日期事件不适用。</span><span class="sxs-lookup"><span data-stu-id="6718b-119">However, for a field such as **Cost center**, a due date event isn't appropriate.</span></span> <span data-ttu-id="6718b-120">因此，**在以下范围内到期**事件类型不可用。</span><span class="sxs-lookup"><span data-stu-id="6718b-120">Therefore, the **is due in** event type isn't available.</span></span> <span data-ttu-id="6718b-121">而**已更改**事件类型可用。</span><span class="sxs-lookup"><span data-stu-id="6718b-121">Instead, the **has changed** event type is available.</span></span>

## <a name="event-types"></a><span data-ttu-id="6718b-122">事件类型</span><span class="sxs-lookup"><span data-stu-id="6718b-122">Event types</span></span>
<span data-ttu-id="6718b-123">可以发生三类事件：</span><span class="sxs-lookup"><span data-stu-id="6718b-123">Three types of events can occur:</span></span>

- <span data-ttu-id="6718b-124">**创建类型和删除类型的事件** – 这些事件在创建或删除记录时触发预警。</span><span class="sxs-lookup"><span data-stu-id="6718b-124">**Create-type and delete-type events** – These events trigger an alert when a record is created or deleted.</span></span>
- <span data-ttu-id="6718b-125">**更新类型事件** – 这些事件在特定字段的数据发生更改时触发预警。</span><span class="sxs-lookup"><span data-stu-id="6718b-125">**Update-type events** – These events trigger an alert when the data in a specific field changes.</span></span>
- <span data-ttu-id="6718b-126">**到期日期类型事件** – 达到某个日期时这些事件会触发预警。</span><span class="sxs-lookup"><span data-stu-id="6718b-126">**Due date-type events** – These events trigger an alert when a date arrives.</span></span>
    
<span data-ttu-id="6718b-127">发生的更改可由用户启动。</span><span class="sxs-lookup"><span data-stu-id="6718b-127">Changes that occur can be initiated by a user.</span></span> <span data-ttu-id="6718b-128">例如，用户更改采购订单的交货日期。</span><span class="sxs-lookup"><span data-stu-id="6718b-128">For example, a user changes the delivery date of a purchase order.</span></span> <span data-ttu-id="6718b-129">或者，更改可作为流程的一部分发生。</span><span class="sxs-lookup"><span data-stu-id="6718b-129">Alternatively, changes can occur as part of a process.</span></span> <span data-ttu-id="6718b-130">例如，某页面的**状态**字段发生更改，以反映系统中各个流程的生命周期。</span><span class="sxs-lookup"><span data-stu-id="6718b-130">For example, the **Status** field on a page changes to reflect the life cycle of various processes in the system.</span></span>

## <a name="conditions"></a><span data-ttu-id="6718b-131">条件</span><span class="sxs-lookup"><span data-stu-id="6718b-131">Conditions</span></span>
<span data-ttu-id="6718b-132">在**创建预警规则**对话框的**提示以下事项**快速选项卡上，您可以使用条件来控制您什么时候收到与事件有关的预警。</span><span class="sxs-lookup"><span data-stu-id="6718b-132">On the **Alert me for** FastTab of the **Create alert rule** dialog box, you can use conditions to control when you're alerted about events.</span></span>

<span data-ttu-id="6718b-133">例如，您可以指定采购订单状态发生更改时系统应向您发出预警，但是仅在状态匹配一组特定条件的情况下。</span><span class="sxs-lookup"><span data-stu-id="6718b-133">For example, you can specify that the system should alert you when the status of purchase orders changes, but only if the status matches a specific set of conditions.</span></span> <span data-ttu-id="6718b-134">特别是当您要在采购订单的状态设置为**已收到**时收到预警的情况。</span><span class="sxs-lookup"><span data-stu-id="6718b-134">Specifically, you want to be alerted when the status of a purchase order is set to **Received**.</span></span> <span data-ttu-id="6718b-135">此状态更改是触发预警的事件。</span><span class="sxs-lookup"><span data-stu-id="6718b-135">This change in status is the event that triggers the alert.</span></span>

<span data-ttu-id="6718b-136">然后，您必须确定您要收到有关哪些采购订单的预警。</span><span class="sxs-lookup"><span data-stu-id="6718b-136">Next, you must decide which purchase orders you want to be alerted about.</span></span> <span data-ttu-id="6718b-137">例如，您可以选择以下选项之一：</span><span class="sxs-lookup"><span data-stu-id="6718b-137">For example, you can select one of the following options.</span></span> <span data-ttu-id="6718b-138">这些选项为预警规则定义了条件。</span><span class="sxs-lookup"><span data-stu-id="6718b-138">These options define the conditions for the alert rule.</span></span>

- <span data-ttu-id="6718b-139">**当前所选记录** – 您在特定采购订单的状态更改为**已接收**时收到预警。</span><span class="sxs-lookup"><span data-stu-id="6718b-139">**Current selected record** – You receive an alert when the status of a specific purchase order changes to **Received**.</span></span>
- <span data-ttu-id="6718b-140">**所有记录** – 当活动页视图中某个项目的采购订单状态更改时您将收到预警。</span><span class="sxs-lookup"><span data-stu-id="6718b-140">**All records** – You receive an alert when the status of a purchase order is changed for an item in the active page view.</span></span> <span data-ttu-id="6718b-141">您可以在页面上使用高级筛选为一组特定记录创建规则。</span><span class="sxs-lookup"><span data-stu-id="6718b-141">You can use the advanced filtering that is available on the page to create rules for a specific set of records.</span></span> <span data-ttu-id="6718b-142">例如，您可以创建为特定客户组中客户的所有采购订单触发的预警。</span><span class="sxs-lookup"><span data-stu-id="6718b-142">For example, you can create an alert that is triggered for all purchase orders for the customers in a specific customer group.</span></span>
    
## <a name="expiry-of-rule"></a><span data-ttu-id="6718b-143">规则到期</span><span class="sxs-lookup"><span data-stu-id="6718b-143">Expiry of rule</span></span>
<span data-ttu-id="6718b-144">在**创建预警规则**对话框的**在以下时间之前提示**快速选项卡上，可以指定预警规则应处于有效状态的时长。</span><span class="sxs-lookup"><span data-stu-id="6718b-144">On the **Alert me until** FastTab of the **Create alert rule** dialog box, you can specify how long the alert rule should be active.</span></span>

## <a name="alert-contents"></a><span data-ttu-id="6718b-145">预警内容</span><span class="sxs-lookup"><span data-stu-id="6718b-145">Alert contents</span></span>
<span data-ttu-id="6718b-146">在**创建预警规则**对话框的**提示以下内容**快速选项卡上，可以指定预警消息应使用的主题文本和消息。</span><span class="sxs-lookup"><span data-stu-id="6718b-146">On the **Alert me with** FastTab of the **Create alert rule** dialog box, you can specify the subject text and message text that the alert messages should use.</span></span>

## <a name="user-id"></a><span data-ttu-id="6718b-147">用户 ID</span><span class="sxs-lookup"><span data-stu-id="6718b-147">User ID</span></span>
<span data-ttu-id="6718b-148">在**创建预警规则**对话框的**提示以下内容**快速选项卡上，可以指定应接收预警消息的用户。</span><span class="sxs-lookup"><span data-stu-id="6718b-148">On the **Alert me with** FastTab of the **Create alert rule** dialog box, you can specify which user should receive the alert messages.</span></span> <span data-ttu-id="6718b-149">默认状态下，将选择您的用户 ID。</span><span class="sxs-lookup"><span data-stu-id="6718b-149">By default, your user ID is selected.</span></span> <span data-ttu-id="6718b-150">此选项仅限组织管理员使用。</span><span class="sxs-lookup"><span data-stu-id="6718b-150">This option is restricted to organization administrators.</span></span>

## <a name="create-an-alert-rule"></a><span data-ttu-id="6718b-151">创建预警规则</span><span class="sxs-lookup"><span data-stu-id="6718b-151">Create an alert rule</span></span>
1. <span data-ttu-id="6718b-152">打开包含要监控的数据的页面。</span><span class="sxs-lookup"><span data-stu-id="6718b-152">Open the page that contains the data to monitor.</span></span>
2. <span data-ttu-id="6718b-153">在操作窗格上，在**选项**选项卡，在**共享**组中，选择**创建预警规则**。</span><span class="sxs-lookup"><span data-stu-id="6718b-153">On the Action Pane, on the **Options** tab, in the **Share** group, select **Create alert rule**.</span></span>
3. <span data-ttu-id="6718b-154">在**创建预警规则**对话框中，在**字段**字段中，选择要监控的字段。</span><span class="sxs-lookup"><span data-stu-id="6718b-154">In the **Create alert rule** dialog box, in the **Field** field, select the field to monitor.</span></span>
4. <span data-ttu-id="6718b-155">在**事件**字段中，选择事件的类型。</span><span class="sxs-lookup"><span data-stu-id="6718b-155">In the **Event** field, select the type of event.</span></span>
5. <span data-ttu-id="6718b-156">在**提示以下事项**快速选项卡上，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="6718b-156">On the **Alert me for** FastTab, select an option.</span></span>
6. <span data-ttu-id="6718b-157">如果预警规则应在特定日期失效，则在**在以下时间之前提示**快速选项卡上选择某一结束日期。</span><span class="sxs-lookup"><span data-stu-id="6718b-157">If the alert rule should become inactive on a specific date, on the **Alert me until** FastTab, select an end date.</span></span>
7. <span data-ttu-id="6718b-158">在**提示以下内容**快速选项卡上，在**主题**字段中，接受默认的电子邮件主题标题或输入新的主题。</span><span class="sxs-lookup"><span data-stu-id="6718b-158">On the **Alert me with** FastTab, in the **Subject** field, accept the default subject heading for the email message, or enter a new subject.</span></span> <span data-ttu-id="6718b-159">文本用作触发预警时所收到电子邮件的主题标题。</span><span class="sxs-lookup"><span data-stu-id="6718b-159">The text is used as the subject heading for the email message that you receive when an alert is triggered.</span></span>
8. <span data-ttu-id="6718b-160">在**消息**字段中，输入可选消息</span><span class="sxs-lookup"><span data-stu-id="6718b-160">In the **Message** field, enter an optional message.</span></span> <span data-ttu-id="6718b-161">文本用作触发预警时收到的消息。</span><span class="sxs-lookup"><span data-stu-id="6718b-161">The text is used as the message that you receive when an alert is triggered.</span></span>
9. <span data-ttu-id="6718b-162">选择**确定**保存设置和创建预警规则。</span><span class="sxs-lookup"><span data-stu-id="6718b-162">Select **OK** to save the settings and create the alert rule.</span></span>

