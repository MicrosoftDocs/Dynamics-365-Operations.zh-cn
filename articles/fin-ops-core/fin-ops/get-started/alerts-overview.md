---
title: 预警概览
description: 本主题提供了有关预警的一般信息。 您可以使用预警保持了解有关您想要在工作日期间跟踪的事件。
author: tjvass
manager: AnnBe
ms.date: 09/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EventCreateRule
audience: Application user
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2018-3-30
ms.dyn365.ops.version: Platform update 15
ms.openlocfilehash: 755181e956a3d93d87e9e5d57622283ff7bf4944
ms.sourcegitcommit: f62c2151be477acfaeace73878471abb9b1b832d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/17/2020
ms.locfileid: "3602521"
---
# <a name="alerts-overview"></a><span data-ttu-id="0a4d1-104">预警概览</span><span class="sxs-lookup"><span data-stu-id="0a4d1-104">Alerts overview</span></span>

[!include [banner](../includes/banner.md)]

## <a name="about-alerts"></a><span data-ttu-id="0a4d1-105">关于预警</span><span class="sxs-lookup"><span data-stu-id="0a4d1-105">About alerts</span></span>
<span data-ttu-id="0a4d1-106">预警形成系统中重要事件的通知系统。</span><span class="sxs-lookup"><span data-stu-id="0a4d1-106">Alerts form a notification system for critical events in the system.</span></span> <span data-ttu-id="0a4d1-107">您可以使用预警保持了解有关您想要在工作日期间跟踪的事件。</span><span class="sxs-lookup"><span data-stu-id="0a4d1-107">You can use alerts to stay informed about events that you want to track during the workday.</span></span> <span data-ttu-id="0a4d1-108">您可轻松创建自己的一套预警规则，以便获得有关逾期交货、删除订单、价格更改或其他必须响应的事件的预警。</span><span class="sxs-lookup"><span data-stu-id="0a4d1-108">You can easily create your own set of alert rules so that you're alerted about deliveries that are overdue, orders that are deleted, prices that change, or other events that you must respond to.</span></span>

<span data-ttu-id="0a4d1-109">在企业资源规划 (ERP) 中，有多个典型场景可以使用预警功能。</span><span class="sxs-lookup"><span data-stu-id="0a4d1-109">In enterprise resource planning (ERP), there are several typical scenarios where the alerts feature can be used.</span></span> <span data-ttu-id="0a4d1-110">下面举了一些示例加以说明。</span><span class="sxs-lookup"><span data-stu-id="0a4d1-110">Here are some examples.</span></span>

### <a name="scenario-1-create-an-alert-rule-for-new-sales-orders"></a><span data-ttu-id="0a4d1-111">场景 1：为新销售订单创建预警规则</span><span class="sxs-lookup"><span data-stu-id="0a4d1-111">Scenario 1: Create an alert rule for new sales orders</span></span>

1. <span data-ttu-id="0a4d1-112">打开**所有销售订单**页。</span><span class="sxs-lookup"><span data-stu-id="0a4d1-112">Open the **All sales orders** page.</span></span>
2. <span data-ttu-id="0a4d1-113">在操作窗格上，在**选项**选项卡，在**共享**组中，选择**创建自定义预警**。</span><span class="sxs-lookup"><span data-stu-id="0a4d1-113">On the Action Pane, on the **Options** tab, in the **Share** group, select **Create a custom alert**.</span></span>
3. <span data-ttu-id="0a4d1-114">在**创建预警规则**对话框，在**在以下情况下提示**快速选项卡上，在**事件**字段中，选择**记录已创建**。</span><span class="sxs-lookup"><span data-stu-id="0a4d1-114">In the **Create alert rule** dialog box, on the **Alert me when** FastTab, in the **Event** field, select **Record has been created**.</span></span>

### <a name="scenario-2-create-an-alert-rule-for-postponement-of-a-delivery-date"></a><span data-ttu-id="0a4d1-115">场景 2：为交货日期延期创建预警规则</span><span class="sxs-lookup"><span data-stu-id="0a4d1-115">Scenario 2: Create an alert rule for postponement of a delivery date</span></span>

1. <span data-ttu-id="0a4d1-116">打开**所有采购订单**页。</span><span class="sxs-lookup"><span data-stu-id="0a4d1-116">Open the **All purchase orders** page.</span></span>
2. <span data-ttu-id="0a4d1-117">选择采购订单 ID 以访问采购订单详细信息。</span><span class="sxs-lookup"><span data-stu-id="0a4d1-117">Select a purchase order ID to access the purchase order details.</span></span>
3. <span data-ttu-id="0a4d1-118">展开**采购订单头**快速选项卡。</span><span class="sxs-lookup"><span data-stu-id="0a4d1-118">Expand the **Purchase order header** FastTab.</span></span>
4. <span data-ttu-id="0a4d1-119">在操作窗格上，在**选项**选项卡，在**共享**组中，选择**创建自定义预警**。</span><span class="sxs-lookup"><span data-stu-id="0a4d1-119">On the Action Pane, on the **Options** tab, in the **Share** group, select **Create a custom alert**.</span></span>
5. <span data-ttu-id="0a4d1-120">在**创建预警规则**对话框，在**在以下情况下提示**快速选项卡上，在**字段**字段中，选择**交货日期**。</span><span class="sxs-lookup"><span data-stu-id="0a4d1-120">In the **Create alert rule** dialog box, on the **Alert me when** FastTab, in the **Field** field, select **Delivery date**.</span></span>
6. <span data-ttu-id="0a4d1-121">在**事件**字段，选择**已延迟**。</span><span class="sxs-lookup"><span data-stu-id="0a4d1-121">In the **Event** field, select **has been postponed**.</span></span>
    
<span data-ttu-id="0a4d1-122">关闭**创建预警规则**对话框后，您的规则将出现在**管理预警规则**页。</span><span class="sxs-lookup"><span data-stu-id="0a4d1-122">After you close the **Create alert rule** dialog box, your rule appears on the **Manage alert rules** page.</span></span> <span data-ttu-id="0a4d1-123">您可以使用**管理预警规则**页更新您现有的预警规则。</span><span class="sxs-lookup"><span data-stu-id="0a4d1-123">You can use the **Manage alert rules** page to update your existing alert rules.</span></span> <span data-ttu-id="0a4d1-124">例如，您可以修改事件触发器、更新事件通知、更新到期日期。</span><span class="sxs-lookup"><span data-stu-id="0a4d1-124">For example, you can modify event triggers, update event notifications, and update expiration dates.</span></span> <span data-ttu-id="0a4d1-125">若要打开**管理预警规则**页，使用操作窗格的**选项**选项卡上的**提示我**按钮。</span><span class="sxs-lookup"><span data-stu-id="0a4d1-125">To open the **Manage alert rules** page, use the **Alert me** button on the **Options** tab of the Action Pane.</span></span>

## <a name="what-occurs-when-an-alert-rule-is-created"></a><span data-ttu-id="0a4d1-126">创建预警规则时会发生什么情况？</span><span class="sxs-lookup"><span data-stu-id="0a4d1-126">What occurs when an alert rule is created?</span></span>

<span data-ttu-id="0a4d1-127">在您创建预警规则时，可以将预定义的事件与一个特定字段关联。</span><span class="sxs-lookup"><span data-stu-id="0a4d1-127">When you create alert rules, you can associate a predefined event with a specific field.</span></span> <span data-ttu-id="0a4d1-128">例如，到达字段中指定的日期时，或者字段的内容更改时。</span><span class="sxs-lookup"><span data-stu-id="0a4d1-128">For example, the date that is specified in the field arrives, or the contents of the field change.</span></span> <span data-ttu-id="0a4d1-129">或者，您可以将某一事件与特定页面中的记录关联。</span><span class="sxs-lookup"><span data-stu-id="0a4d1-129">Alternatively, you can associate an event with the records on a specific page.</span></span> <span data-ttu-id="0a4d1-130">例如，创建记录或删除记录。</span><span class="sxs-lookup"><span data-stu-id="0a4d1-130">For example, a record is created, or a record is deleted.</span></span>

<span data-ttu-id="0a4d1-131">该字段或该页面中的记录发生所选事件时，向您发送预警。</span><span class="sxs-lookup"><span data-stu-id="0a4d1-131">When the selected event occurs for the field or for a record on the page, an alert is sent to you.</span></span> <span data-ttu-id="0a4d1-132">例如，您创建规则将特定采购订单行的**交货日期**字段与**在此时间量之前到期**事件关联。</span><span class="sxs-lookup"><span data-stu-id="0a4d1-132">For example, you create a rule where you associate the **Delivery date** field on a specific purchase order line with the **was due this amount of time ago** event.</span></span> <span data-ttu-id="0a4d1-133">您将时间范围设置为五天。</span><span class="sxs-lookup"><span data-stu-id="0a4d1-133">You set the time frame to five days.</span></span> <span data-ttu-id="0a4d1-134">在此案例中，在该采购订单行的交付日期五天后发送预警。</span><span class="sxs-lookup"><span data-stu-id="0a4d1-134">In this case, an alert is sent five days after the delivery date of that purchase order line.</span></span>

<span data-ttu-id="0a4d1-135">此外，您可以通过设置条件来细化预警规则。</span><span class="sxs-lookup"><span data-stu-id="0a4d1-135">Additionally, you can refine alert rules by setting conditions.</span></span> <span data-ttu-id="0a4d1-136">例如，您可以获得为特定供应商帐户创建新的采购订单的预警。</span><span class="sxs-lookup"><span data-stu-id="0a4d1-136">For example, you can be alerted about new purchase orders that are created for specific vendor accounts.</span></span>

## <a name="preparing-for-an-alert"></a><span data-ttu-id="0a4d1-137">准备预警</span><span class="sxs-lookup"><span data-stu-id="0a4d1-137">Preparing for an alert</span></span>

<span data-ttu-id="0a4d1-138">设置预警规则之前，请确定何时或在何种情况下您想要收到预警。</span><span class="sxs-lookup"><span data-stu-id="0a4d1-138">Before you set up an alert rule, decide when or in what situations you want to receive alerts.</span></span> <span data-ttu-id="0a4d1-139">当您确定要通知的事件时，找到出现引起该事件的数据的页面。</span><span class="sxs-lookup"><span data-stu-id="0a4d1-139">When you know which event you want to be notified about, find the page where the data that causes that event appears.</span></span> <span data-ttu-id="0a4d1-140">事件可以是即将来临的日期，也可以是发生的特定更改。</span><span class="sxs-lookup"><span data-stu-id="0a4d1-140">The event can be a date that arrives or a specific change that occurs.</span></span> <span data-ttu-id="0a4d1-141">因此，您必须找到指定此日期或者显示更改的字段或创建的新记录的页面。</span><span class="sxs-lookup"><span data-stu-id="0a4d1-141">Therefore, you must find the page where the date is specified, or where the field that changes or the new record that is created appears.</span></span> <span data-ttu-id="0a4d1-142">获得此信息之后，您便可以创建预警规则。</span><span class="sxs-lookup"><span data-stu-id="0a4d1-142">After you have this information, you can create the alert rule.</span></span>

## <a name="components-of-an-alert-rule"></a><span data-ttu-id="0a4d1-143">预警规则的组件</span><span class="sxs-lookup"><span data-stu-id="0a4d1-143">Components of an alert rule</span></span>

<span data-ttu-id="0a4d1-144">预警规则有五个组件：</span><span class="sxs-lookup"><span data-stu-id="0a4d1-144">An alert rule has five components:</span></span>

- <span data-ttu-id="0a4d1-145">**事件** – 触发预警规则的事件可以是即将来临的日期，也可以是发生的具体更改。</span><span class="sxs-lookup"><span data-stu-id="0a4d1-145">**Event** – The event that triggers an alert rule can be a date that arrives or a specific change that occurs.</span></span> <span data-ttu-id="0a4d1-146">您在**创建预警规则**对话框的**发送有关作业状态更改的电子邮件预警**快速选项卡上定义事件。</span><span class="sxs-lookup"><span data-stu-id="0a4d1-146">You define events on the **Send email alerts for job status changes** FastTab of the **Create alert rule** dialog box.</span></span>
- <span data-ttu-id="0a4d1-147">**条件** – 在**创建预警规则**对话框的**提示以下事项**快速选项卡上，您可以选择条件的作用域，来控制您什么时候收到与事件有关的预警。</span><span class="sxs-lookup"><span data-stu-id="0a4d1-147">**Condition** – On the **Alert me for** FastTab of the **Create alert rule** dialog box, you can select the scope of the condition, to control when you're alerted about events.</span></span> <span data-ttu-id="0a4d1-148">您可以只将这个规则应用到当前记录或应用到页面上的所有可见记录。</span><span class="sxs-lookup"><span data-stu-id="0a4d1-148">You can apply the rule either to the current record only or to all visible records on the page.</span></span> <span data-ttu-id="0a4d1-149">如果在多个法人中应用规则，则您可以将**组织范围**选项设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="0a4d1-149">If the rule applies across legal entities, you can set the **Organization-wide** option to **Yes**.</span></span>
- <span data-ttu-id="0a4d1-150">**规则到期** – 在**创建预警规则**对话框的**在以下时间之前提示**快速选项卡上，可以指定预警规则应处于有效状态的时长。</span><span class="sxs-lookup"><span data-stu-id="0a4d1-150">**Expiry of rule** – On the **Alert me until** FastTab of the **Create alert rule** dialog box, you can specify how long the alert rule should be active.</span></span>
- <span data-ttu-id="0a4d1-151">**内容** – 在**创建预警规则**对话框的**提示以下内容**快速选项卡上，可以指定预警消息应使用的主题文本和消息。</span><span class="sxs-lookup"><span data-stu-id="0a4d1-151">**Contents** – On the **Alert me with** FastTab of the **Create alert rule** dialog box, you can specify the subject text and message text that the alert messages should use.</span></span>
- <span data-ttu-id="0a4d1-152">**用户** – 在**创建预警规则**对话框的**被警告者**快速选项卡上，可以指定应接收预警消息的用户。</span><span class="sxs-lookup"><span data-stu-id="0a4d1-152">**User** – On the **Alert who** FastTab of the **Create alert rule** dialog box, you can specify which user should receive the alert messages.</span></span> <span data-ttu-id="0a4d1-153">默认状态下，将选择您的用户 ID。</span><span class="sxs-lookup"><span data-stu-id="0a4d1-153">By default, your user ID is selected.</span></span>

    > [!NOTE]
    > <span data-ttu-id="0a4d1-154">此选项仅限组织管理员使用。</span><span class="sxs-lookup"><span data-stu-id="0a4d1-154">This option is restricted to organization administrators.</span></span>

## <a name="videos"></a><span data-ttu-id="0a4d1-155">视频</span><span class="sxs-lookup"><span data-stu-id="0a4d1-155">Videos</span></span>

### <a name="how-to-use-alerts-to-monitor-filtered-data"></a><span data-ttu-id="0a4d1-156">如何使用预警监控筛选数据</span><span class="sxs-lookup"><span data-stu-id="0a4d1-156">How to use alerts to monitor filtered data</span></span>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE3DWZ3]

<span data-ttu-id="0a4d1-157">YouTube 上的 [Finance and Operations 播放列表](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW)中包含[如何使用预警监控筛选数据](https://youtu.be/ZYKMcv6kl9s)视频（上面所示）。</span><span class="sxs-lookup"><span data-stu-id="0a4d1-157">The [How to use alerts to monitor filtered data](https://youtu.be/ZYKMcv6kl9s) video (shown above) is included in the [Finance and Operations playlist](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) available on YouTube.</span></span>

### <a name="alert-rule-options"></a><span data-ttu-id="0a4d1-158">预警规则选项</span><span class="sxs-lookup"><span data-stu-id="0a4d1-158">Alert rule options</span></span>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE3E4PV]

<span data-ttu-id="0a4d1-159">YouTube 上的 [Finance and Operations 播放列表](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW)中包含[预警规则选项](https://youtu.be/cpzimwOjicM)视频（上面所示）。</span><span class="sxs-lookup"><span data-stu-id="0a4d1-159">The [Alert rule options](https://youtu.be/cpzimwOjicM) video (shown above) is included in the [Finance and Operations playlist](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) available on YouTube.</span></span>


