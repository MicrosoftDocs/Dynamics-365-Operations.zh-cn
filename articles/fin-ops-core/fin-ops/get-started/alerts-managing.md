---
title: 预警的批处理
description: 此主题提供有关批处理预警的信息。
author: tjvass
manager: AnnBe
ms.date: 09/10/2010
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2018-3-30
ms.dyn365.ops.version: Platform update 15
ms.openlocfilehash: 57208e87dbbd0ae6fc05644229a8a9cf08da4249
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/09/2021
ms.locfileid: "5562402"
---
# <a name="batch-processing-of-alerts"></a><span data-ttu-id="a53aa-103">预警的批处理</span><span class="sxs-lookup"><span data-stu-id="a53aa-103">Batch processing of alerts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a53aa-104">预警由批处理功能来处理。</span><span class="sxs-lookup"><span data-stu-id="a53aa-104">Alerts are processed by the batch processing functionality.</span></span> <span data-ttu-id="a53aa-105">您必须首先设置批处理，然后才可以处理和发出预警。</span><span class="sxs-lookup"><span data-stu-id="a53aa-105">You must set up batch processing before the process and deliver alerts.</span></span>

<span data-ttu-id="a53aa-106">批处理功能支持两种类型的事件：</span><span class="sxs-lookup"><span data-stu-id="a53aa-106">Batch processing functionality supports two types of events:</span></span>

- <span data-ttu-id="a53aa-107">由基于更改的事件触发的事件。</span><span class="sxs-lookup"><span data-stu-id="a53aa-107">Events triggered by change-based events.</span></span> <span data-ttu-id="a53aa-108">这些事件也称作创建/删除和更新事件。</span><span class="sxs-lookup"><span data-stu-id="a53aa-108">These events are also referred to as create/delete and update events.</span></span>
- <span data-ttu-id="a53aa-109">由到期日期触发的事件。</span><span class="sxs-lookup"><span data-stu-id="a53aa-109">Events triggered by due dates.</span></span>

<span data-ttu-id="a53aa-110">您可以为各个事件类型设置批处理。</span><span class="sxs-lookup"><span data-stu-id="a53aa-110">You can set up batch processes for each type of event.</span></span>

## <a name="batch-processing-for-change-based-events"></a><span data-ttu-id="a53aa-111">基于变化的事件的批处理</span><span class="sxs-lookup"><span data-stu-id="a53aa-111">Batch processing for change-based events</span></span>

<span data-ttu-id="a53aa-112">系统读取自上次批处理运行以来出现的所有基于变化的事件。</span><span class="sxs-lookup"><span data-stu-id="a53aa-112">The system reads all change-based events that have occurred since batch processing was last run.</span></span> <span data-ttu-id="a53aa-113">基于变化的事件包括更新字段、删除记录和创建记录。</span><span class="sxs-lookup"><span data-stu-id="a53aa-113">Change-based events include updates to fields, the deletion of records, and the creation of records.</span></span> <span data-ttu-id="a53aa-114">这些事件与您在预警规则中设置的条件进行比较。</span><span class="sxs-lookup"><span data-stu-id="a53aa-114">These events are compared with the conditions that you set up in alert rules.</span></span> <span data-ttu-id="a53aa-115">事件与规则中的条件匹配时，批处理将生成预警。</span><span class="sxs-lookup"><span data-stu-id="a53aa-115">When an event matches the conditions in a rule, the batch process generates an alert.</span></span>

### <a name="frequency-for-change-based-events"></a><span data-ttu-id="a53aa-116">基于变化的事件的频率</span><span class="sxs-lookup"><span data-stu-id="a53aa-116">Frequency for change-based events</span></span>

<span data-ttu-id="a53aa-117">对于基于变化的事件，您可以设置一个批处理作业，在系统记录事件后立即触发对该事件的处理。</span><span class="sxs-lookup"><span data-stu-id="a53aa-117">For change-based events, you can set up a batch job that triggers the processing of an event soon after the system logs the event.</span></span> <span data-ttu-id="a53aa-118">如果您设置批处理作业以更高的频率重复，用户将在更改后很快收到其预警。</span><span class="sxs-lookup"><span data-stu-id="a53aa-118">If you set up the batch job to recur more often, users receive their alerts sooner after changes occur.</span></span> <span data-ttu-id="a53aa-119">但是，批处理的高频率可能冲销对系统性能的影响。</span><span class="sxs-lookup"><span data-stu-id="a53aa-119">However, a high frequency for batch processing might adversely affect system performance.</span></span>

<span data-ttu-id="a53aa-120">另一方面，在系统负载过低时，重复频率过低、安排的时间较短的批处理作业可能有助于提高系统性能。</span><span class="sxs-lookup"><span data-stu-id="a53aa-120">On the other hand, a batch job that recurs less often, and that you schedule for times when the system load is low, might help improve system performance.</span></span> <span data-ttu-id="a53aa-121">但是，批处理的频率过低可能不能及时满足用户对预警的需求。</span><span class="sxs-lookup"><span data-stu-id="a53aa-121">However, a low frequency for batch processing might not meet the users' demands for timely alerts.</span></span>

<span data-ttu-id="a53aa-122">因此，在为基于变化的事件设置批处理频率时，既要考虑预警的及时性，又要考虑整个系统的性能。</span><span class="sxs-lookup"><span data-stu-id="a53aa-122">Therefore, when you set up the frequency of batch processing for change-based events, consider the balance between the timeliness of alerts and the performance of the whole system.</span></span> <span data-ttu-id="a53aa-123">当创建预警规则的用户增多时，这些注意事项的相关性就会升高。</span><span class="sxs-lookup"><span data-stu-id="a53aa-123">These considerations become more relevant as the number of users who create alert rules increases.</span></span> <span data-ttu-id="a53aa-124">频率不影响系统处理的事件的数量。</span><span class="sxs-lookup"><span data-stu-id="a53aa-124">The frequency doesn't affect the number of events that the system processes.</span></span> <span data-ttu-id="a53aa-125">但是，如果创建规则的用户越多，流程将运行更多检查。</span><span class="sxs-lookup"><span data-stu-id="a53aa-125">However, if more users create rules, the process runs more checks.</span></span> <span data-ttu-id="a53aa-126">这类数据交换可能会影响系统性能。</span><span class="sxs-lookup"><span data-stu-id="a53aa-126">This type of data exchange might affect system performance.</span></span>

#### <a name="the-risks-of-low-batch-frequency"></a><span data-ttu-id="a53aa-127">低批处理频率的风险</span><span class="sxs-lookup"><span data-stu-id="a53aa-127">The risks of low batch frequency</span></span>

<span data-ttu-id="a53aa-128">如果为基于变化的事件的批处理设置了低频率，则与预警规则中的条件相关的数据可能在处理前发生更改。</span><span class="sxs-lookup"><span data-stu-id="a53aa-128">If you set up a low frequency for batch processing for change-based events, data that is relevant to the conditions in alert rules might change before processing.</span></span> <span data-ttu-id="a53aa-129">因此，您可能错过预警。</span><span class="sxs-lookup"><span data-stu-id="a53aa-129">Therefore, you might lose alerts.</span></span>

<span data-ttu-id="a53aa-130">例如，您创建要在事件为 **客户联系信息更改** 且条件为 **客户 = BB** 时触发的预警。</span><span class="sxs-lookup"><span data-stu-id="a53aa-130">For example, you create an alert to trigger when the event is **customer contact changes** and the condition is **customer = BB**.</span></span> <span data-ttu-id="a53aa-131">换言之，当客户 BB 的客户联系人更改时，流程将记录事件。</span><span class="sxs-lookup"><span data-stu-id="a53aa-131">In other words, when the customer contact for customer BB changes, the process logs the event.</span></span> <span data-ttu-id="a53aa-132">但是，对批处理系统进行设置，以便批处理出现的频率小于数据输入出现的频率。</span><span class="sxs-lookup"><span data-stu-id="a53aa-132">However, the batch processing system is set up so that batch processing occurs less often than data entry.</span></span> <span data-ttu-id="a53aa-133">如果事件处理之前客户名称从 **BB** 更改为 **AA**，那么数据库中的数据不再符合规则（**客户= BB**）中的条件。</span><span class="sxs-lookup"><span data-stu-id="a53aa-133">If the customer name changes from **BB** to **AA** before the event is processed, the data in the database no longer matches the condition in the rule, **customer = BB**.</span></span> <span data-ttu-id="a53aa-134">因此，最后在事件处理时，不会生成任何预警。</span><span class="sxs-lookup"><span data-stu-id="a53aa-134">Therefore, when the event is finally processed, no alert is generated.</span></span>

### <a name="set-up-processing-for-change-based-alerts"></a><span data-ttu-id="a53aa-135">设置基于变化的预警的处理</span><span class="sxs-lookup"><span data-stu-id="a53aa-135">Set up processing for change-based alerts</span></span>

1. <span data-ttu-id="a53aa-136">转到 **系统管理** &gt; **定期任务** &gt; **预警** &gt; **基于变化的预警**。</span><span class="sxs-lookup"><span data-stu-id="a53aa-136">Go to **System administration** &gt; **Periodic tasks** &gt; **Alerts** &gt; **Change based alerts**.</span></span>
2. <span data-ttu-id="a53aa-137">在 **基于变化的预警** 对话框中，输入相应的信息。</span><span class="sxs-lookup"><span data-stu-id="a53aa-137">In the **Change based alerts** dialog box, enter the appropriate information.</span></span>

## <a name="batch-processing-for-due-date-events"></a><span data-ttu-id="a53aa-138">到期日期事件的批处理</span><span class="sxs-lookup"><span data-stu-id="a53aa-138">Batch processing for due-date events</span></span>

<span data-ttu-id="a53aa-139">系统会检测到所有由到期日期导致的事件，并将这些事件与预警规则中设置的条件进行比较。</span><span class="sxs-lookup"><span data-stu-id="a53aa-139">The system detects all events that are caused by due dates, and these events are compared with the conditions that are set up in alert rules.</span></span> <span data-ttu-id="a53aa-140">批处理在事件与规则中的条件匹配时生成预警。</span><span class="sxs-lookup"><span data-stu-id="a53aa-140">The batch process generates an alert when an event matches the conditions in a rule.</span></span>

### <a name="frequency-for-due-date-events"></a><span data-ttu-id="a53aa-141">到期日期事件的频率</span><span class="sxs-lookup"><span data-stu-id="a53aa-141">Frequency for due-date events</span></span>

<span data-ttu-id="a53aa-142">对于到期日期事件，您最好将批处理作业设置为在一天中的晚上或其他具体时间运行，以便平衡系统负荷。</span><span class="sxs-lookup"><span data-stu-id="a53aa-142">For due-date events, you might want to set up batch jobs that are run during the night or at specific times of the day, to balance the system load.</span></span> <span data-ttu-id="a53aa-143">我们建议您设置批处理作业，以使其每天至少运行一次。</span><span class="sxs-lookup"><span data-stu-id="a53aa-143">We recommend that you set up the batch job so that it's run at least one time per day.</span></span> <span data-ttu-id="a53aa-144">如果应尽可能早地发送预警，将批处理设置为在系统日期变化后立即进行。</span><span class="sxs-lookup"><span data-stu-id="a53aa-144">If alerts should be sent as early as possible, set up the batch processing to occur immediately after the system date changes.</span></span> <span data-ttu-id="a53aa-145">如果希望为在批处理作业已处理预警后发生的到期日期事件生成预警，则可以在同一天再次运行该批处理作业。</span><span class="sxs-lookup"><span data-stu-id="a53aa-145">If you want to generate alerts for due-date events that occur after a batch job has already processed alerts, you can run the batch job again on the same day.</span></span>

<span data-ttu-id="a53aa-146">例如，批处理作业已按特殊日旁运行。</span><span class="sxs-lookup"><span data-stu-id="a53aa-146">For example, a batch job has been run on a particular day.</span></span> <span data-ttu-id="a53aa-147">然后，您可以创建具有到期日期的采购订单，该日期应在同一天触发预警。</span><span class="sxs-lookup"><span data-stu-id="a53aa-147">You then create a purchase order that has a due date that should trigger an alert on that same day.</span></span> <span data-ttu-id="a53aa-148">要在该天接收预警，必须在创建采购订单后再次运行批处理作业。</span><span class="sxs-lookup"><span data-stu-id="a53aa-148">To receive the alert on that day, you must run the batch job again after the purchase order is created.</span></span> <span data-ttu-id="a53aa-149">不过，如果当天未再次运行该批处理作业，则第二天的批处理作业就会删除前几天未处理的任何到期日期事件。</span><span class="sxs-lookup"><span data-stu-id="a53aa-149">However, if you don't run the batch job again on that day, the next day's batch job detects any due-date events that weren't processed on previous days.</span></span>

> [!NOTE]
> <span data-ttu-id="a53aa-150">即使在批处理运行的频率超过一天一次时，也不会为同一到期日期事件和条件重复预警。</span><span class="sxs-lookup"><span data-stu-id="a53aa-150">Even when the batch process is run more than one time per day, alerts aren't duplicated for the same due-date event and conditions.</span></span> <span data-ttu-id="a53aa-151">仅当日期因系统在上次批处理作业运行后发生了更改而到期时，才会为之生成预警。</span><span class="sxs-lookup"><span data-stu-id="a53aa-151">Alerts are generated only for dates that have become due because of changes that occurred in the system after the last batch job was run.</span></span>

### <a name="batch-processing-window"></a><span data-ttu-id="a53aa-152">批处理时间范围</span><span class="sxs-lookup"><span data-stu-id="a53aa-152">Batch processing window</span></span>

<span data-ttu-id="a53aa-153">公司中预警规则的处理停止原因可有很多种。</span><span class="sxs-lookup"><span data-stu-id="a53aa-153">The processing of alert rules in a company can be stopped for several reasons.</span></span> <span data-ttu-id="a53aa-154">这些原因包括假期、系统错误，或者阻止批处理作业在一段时间内运行的其他问题。</span><span class="sxs-lookup"><span data-stu-id="a53aa-154">These reasons include vacations, system errors, or other issues that prevent the batch jobs from being run for some time.</span></span>

<span data-ttu-id="a53aa-155">为了防止到期日期预警因为批处理作业数天未运行而过时，您可以设置批处理窗口。</span><span class="sxs-lookup"><span data-stu-id="a53aa-155">To prevent due-date alerts from becoming obsolete because the batch job hasn't been run for several days, you can set up a batch processing window.</span></span> <span data-ttu-id="a53aa-156">批处理窗口可以用于阻止批处理作业在指定的运行天数内运行。</span><span class="sxs-lookup"><span data-stu-id="a53aa-156">A batch processing window can be used to prevent a batch job from being run for a specified number of days.</span></span>

<span data-ttu-id="a53aa-157">如果设置批处理窗口，预警在预警规则处理时发送，即使预警超过了到期日期条件中定义的时间限制。</span><span class="sxs-lookup"><span data-stu-id="a53aa-157">If you set up a batch processing window, an alert is sent when the alert rule is processed, even if the alert exceeds the time limit that is defined in the due-date criteria.</span></span> <span data-ttu-id="a53aa-158">只要由此时间限制和批处理窗口定义的期间未超过，预警就会继续被发送。</span><span class="sxs-lookup"><span data-stu-id="a53aa-158">An alert continues to be sent for as long as the period that is defined by this time limit plus the batch processing window isn't exceeded.</span></span> <span data-ttu-id="a53aa-159">但是，当期间超过时间限制和批处理窗口定义的值时，不再发送预警。</span><span class="sxs-lookup"><span data-stu-id="a53aa-159">However, when the period exceeds the value defined by the time limit plus the batch processing window, an alert is no longer sent.</span></span>

### <a name="set-up-processing-for-due-date-alerts"></a><span data-ttu-id="a53aa-160">设置到期日期预警的处理</span><span class="sxs-lookup"><span data-stu-id="a53aa-160">Set up processing for due-date alerts</span></span>

1. <span data-ttu-id="a53aa-161">转到 **系统管理** &gt; **定期任务** &gt; **预警** &gt; **到期日期预警**。</span><span class="sxs-lookup"><span data-stu-id="a53aa-161">Go to **System administration** &gt; **Periodic tasks** &gt; **Alerts** &gt; **Due date alerts**.</span></span>
2. <span data-ttu-id="a53aa-162">在 **到期日期预警** 对话框中，输入相应的信息。</span><span class="sxs-lookup"><span data-stu-id="a53aa-162">In the **Due date alerts** dialog box, enter the appropriate information.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]