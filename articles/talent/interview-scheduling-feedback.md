---
title: 在 Attract 中计划面试
description: 此主题提供有关 Attract 中的面试计划和反馈活动的信息。
author: hasrivas
manager: AnnBe
ms.date: 04/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.search.region: Global
ms.author: shielas
ms.openlocfilehash: 33eba9796ca997fde4be9a46050207d313551bde
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4460477"
---
# <a name="schedule-interviews-in-attract"></a><span data-ttu-id="2ee55-103">在 Attract 中计划面试</span><span class="sxs-lookup"><span data-stu-id="2ee55-103">Schedule interviews in Attract</span></span>

[!include [banner](includes/banner.md)]

## <a name="scheduler-activity"></a><span data-ttu-id="2ee55-104">计划程序活动</span><span class="sxs-lookup"><span data-stu-id="2ee55-104">Scheduler activity</span></span>

<span data-ttu-id="2ee55-105">计划程序活动是可选的，有两个组件：应聘者可用日期请求和计划。</span><span class="sxs-lookup"><span data-stu-id="2ee55-105">The scheduler activity is optional and has two components: Candidate availability request and Schedule.</span></span> <span data-ttu-id="2ee55-106">应聘者可用日期组件允许您使用电子邮件请求应聘者的可用日期。</span><span class="sxs-lookup"><span data-stu-id="2ee55-106">The Candidate availability component lets you use email to request a candidate's availability.</span></span> <span data-ttu-id="2ee55-107">计划组件提供计划应聘者和招聘团队的面试的能力。</span><span class="sxs-lookup"><span data-stu-id="2ee55-107">The Schedule component provides the ability to schedule interviews with the candidate and the hiring team.</span></span>

<span data-ttu-id="2ee55-108">若要设置计划程序活动以包括或限制要安排的应聘者，请在 **要安排的对象** 字段中选择一个值。</span><span class="sxs-lookup"><span data-stu-id="2ee55-108">To set up the scheduler activity to include or limit the candidates to be scheduled, select a value in the **Who are you scheduling** field.</span></span> <span data-ttu-id="2ee55-109">可用选项为 **所有应聘者**、**外部应聘者** 和 **内部应聘者**。</span><span class="sxs-lookup"><span data-stu-id="2ee55-109">The available options are **All Candidates**, **External Candidates**, and **Internal Candidates**.</span></span> <span data-ttu-id="2ee55-110">例如，如果要在第一轮安排中跳过内部应聘者，可以通过将 **要安排的对象** 设置为 **外部应聘者**，将计划活动仅分配给外部应聘者。</span><span class="sxs-lookup"><span data-stu-id="2ee55-110">For example, if you want to skip internal candidates in the first round of scheduling, you can assign the schedule activity only to external candidates by setting **Who are you scheduling** to **External Candidates**.</span></span>

### <a name="candidate-availability-request"></a><span data-ttu-id="2ee55-111">应聘者可用日期请求</span><span class="sxs-lookup"><span data-stu-id="2ee55-111">Candidate availability request</span></span>

<span data-ttu-id="2ee55-112">要向请求其可用日期的应聘者发送电子邮件，请选择 **请求应聘者可用日期** 字段。</span><span class="sxs-lookup"><span data-stu-id="2ee55-112">To send an email to candidates requesting their availability, select the **Request candidate availability** field.</span></span> <span data-ttu-id="2ee55-113">如果未选择此字段，此步骤不会在工作的招聘流程中显示。</span><span class="sxs-lookup"><span data-stu-id="2ee55-113">If the field is not selected, this step won't be shown in the hiring process for the job.</span></span>

<span data-ttu-id="2ee55-114">若要发送可用日期请求，请单击 **发送请求**，选择可用日期和电子邮件模板，然后将邮件发送给应聘者。</span><span class="sxs-lookup"><span data-stu-id="2ee55-114">To send the availability request, click **Send request**, choose the available dates and an email template, and then send the mail to the candidate.</span></span>

<span data-ttu-id="2ee55-115">[![发送应聘者可用日期请求的 Attract 招聘人员视图](./media/scheduler-candidate-request.png)](./media/scheduler-candidate-request.png)</span><span class="sxs-lookup"><span data-stu-id="2ee55-115">[![Attract recruiter view to send candidate availability request](./media/scheduler-candidate-request.png)](./media/scheduler-candidate-request.png)</span></span>

<span data-ttu-id="2ee55-116">在应聘者收到响应请求的电子邮件时，他们可以登录到其应聘者门户，选择与其可用日期匹配的日期，然后单击 **提交**。</span><span class="sxs-lookup"><span data-stu-id="2ee55-116">When the candidate receives an email to respond to the request, they can sign in to their candidate portal, choose the dates that match their availability, and click **Submit**.</span></span>

### <a name="schedule"></a><span data-ttu-id="2ee55-117">时间表</span><span class="sxs-lookup"><span data-stu-id="2ee55-117">Schedule</span></span>
<span data-ttu-id="2ee55-118">有多个配置可供面试安排人员使用、快速创建和将面试圈发送给面试官和应聘者。</span><span class="sxs-lookup"><span data-stu-id="2ee55-118">There are multiple configurations available for the interview scheduler to use and quickly create and send the interview loop to the interviewers and the candidate.</span></span>

1. <span data-ttu-id="2ee55-119">单击 **创建计划**，在 **添加面试官** 框中，列出进入面试圈中的所有面试官。</span><span class="sxs-lookup"><span data-stu-id="2ee55-119">Click **Create schedule**, and in the **Add interviewers** box, list all the interviewers that are going to be part of the interview loop.</span></span>
<span data-ttu-id="2ee55-120">[![开始计划面试圈的 Attract 招聘人员视图](./media/schedule-start-over.png)](./media/schedule-start-over.png) </span><span class="sxs-lookup"><span data-stu-id="2ee55-120">[![Attract recruiter view to start scheduling an interview loop](./media/schedule-start-over.png)](./media/schedule-start-over.png) </span></span>  
    <span data-ttu-id="2ee55-121">如果应聘者已响应面试请求可用性，**面试日期** 字段将预先填充其选择。</span><span class="sxs-lookup"><span data-stu-id="2ee55-121">If the candidate had responded to the interview request availability, the **Interview date** field will be pre-populated with their selection.</span></span> <span data-ttu-id="2ee55-122">您可以根据需要选择不同的日期。</span><span class="sxs-lookup"><span data-stu-id="2ee55-122">You can select a different date if needed.</span></span>
    
    <span data-ttu-id="2ee55-123">如果您选择 **将其设置为小组面试** 字段，左侧的面试官组将移到一个小组圈来创建面试。</span><span class="sxs-lookup"><span data-stu-id="2ee55-123">If you select the **Make this a panel interview** field, the group of interviewers on the left are moved in to a single panel loop to create the interview.</span></span> <span data-ttu-id="2ee55-124">然后您需要为面试定义特定顺序。</span><span class="sxs-lookup"><span data-stu-id="2ee55-124">You will then need to define a specific sequence for the interviews.</span></span>
    
    <span data-ttu-id="2ee55-125">应该安排面试计划以与参与者的可用日期最佳匹配。</span><span class="sxs-lookup"><span data-stu-id="2ee55-125">The interview schedule should be arranged to best match the participants’ availability.</span></span> <span data-ttu-id="2ee55-126">如果是内部应聘者，您可以将其可用日期包含在计划建议中。</span><span class="sxs-lookup"><span data-stu-id="2ee55-126">If it’s an internal candidate, you can include their availability as part of the schedule recommendation.</span></span>
    
    <span data-ttu-id="2ee55-127">若要召开联机会议，请选择 **添加 Skype 会议** 字段，每个面试事件将有一个可用的 **Skype for Business** 链接。</span><span class="sxs-lookup"><span data-stu-id="2ee55-127">To have an online meeting, select the **Add Skype meetings** field and each interview event will have a **Skype for Business** link available.</span></span>

2. <span data-ttu-id="2ee55-128">为每个面试事件选择面试持续时间，然后单击 **确定** 开始创建计划。</span><span class="sxs-lookup"><span data-stu-id="2ee55-128">Select the interview duration for each interview event, and then click **OK** to start creating the schedule.</span></span>

    <span data-ttu-id="2ee55-129">如果选择了 **建议**，将显示建议，面试网格将预填充。</span><span class="sxs-lookup"><span data-stu-id="2ee55-129">If **Recommendations** are selected, suggestions will be shown and the interview grid will be pre-populated.</span></span> <span data-ttu-id="2ee55-130">您可以查看所有选定的面试官当前的日历可用日期。</span><span class="sxs-lookup"><span data-stu-id="2ee55-130">You will be able to see the current calendar availability of all the selected interviewers.</span></span> <span data-ttu-id="2ee55-131">如果是内部应聘者，您还可以查看应聘者的日历。</span><span class="sxs-lookup"><span data-stu-id="2ee55-131">You will also be able to view the candidate’s calendar if they're an internal candidate.</span></span> <span data-ttu-id="2ee55-132">对于面试官和内部应聘者，您可以查看其忙时间段、工作时间、外出时间，还可以验证他们是否将自己的日历标记为特定时间段在其他地方工作。</span><span class="sxs-lookup"><span data-stu-id="2ee55-132">For the interviewers and internal candidates, you can view their busy time slots, their working hours, their out of office hours and also identify if they have marked their calendars as working elsewhere for specific time slots.</span></span> 

3. <span data-ttu-id="2ee55-133">如果没有可用建议，在 **面试官** 列中，单击一个时间段，提供面试职位、详细信息，并根据需要填充位置详细信息。</span><span class="sxs-lookup"><span data-stu-id="2ee55-133">If there are no suggestions available, in the **Interviewers** column, click in a time slot, provide the interview title, details, and populate the location details, as necessary.</span></span> <span data-ttu-id="2ee55-134">您可以选择为面试包含 **Skype for Business** 链接。</span><span class="sxs-lookup"><span data-stu-id="2ee55-134">You can choose to include the **Skype for Business** link for the interview.</span></span>

4. <span data-ttu-id="2ee55-135">若要包括其他面试官，请单击 **添加面试** 网格列来选择一个或多个面试官。</span><span class="sxs-lookup"><span data-stu-id="2ee55-135">To include additional interviewers, click the **Add interview** grid column to select one or more interviewers.</span></span> <span data-ttu-id="2ee55-136">您可以使用省略号 (...) 选项来从圈中删除面试。</span><span class="sxs-lookup"><span data-stu-id="2ee55-136">You can use the ellipsis (...) option to remove an interview from the loop.</span></span>
    
5. <span data-ttu-id="2ee55-137">如果面试计划在不同时区，请从右上方的下拉列表中选择所需的城市/时区。</span><span class="sxs-lookup"><span data-stu-id="2ee55-137">If the interviews are scheduled in a different time-zone, pick the required city/time-zone from the drop-down list in the upper right.</span></span> <span data-ttu-id="2ee55-138">面试官可用日期网格将更新以反映新时区。</span><span class="sxs-lookup"><span data-stu-id="2ee55-138">The interviewer availability grid will be updated to reflect the new time zone.</span></span> <span data-ttu-id="2ee55-139">此时区选择现在还将在 **面试汇总** 视图中显示，其将与面试官和应聘者共享。</span><span class="sxs-lookup"><span data-stu-id="2ee55-139">This time-zone selection will now also display in the **Interview summary** view, which will be shared with the interviewers and the candidate.</span></span> 

6. <span data-ttu-id="2ee55-140">单击 **发送给面试官** 将会议邀请发送给涉及到的面试官。</span><span class="sxs-lookup"><span data-stu-id="2ee55-140">Click **Send to interviewers** to send the meeting invites to the interviewers involved.</span></span>

    <span data-ttu-id="2ee55-141">在面试请求发送给面试官后，他们可以直接从收到的电子邮件邀请响应。</span><span class="sxs-lookup"><span data-stu-id="2ee55-141">After the interview requests have been sent to the interviewers, they can respond directly from the email invite that they receive.</span></span>

    >[!NOTE]
    > <span data-ttu-id="2ee55-142">对于所有 1:1 面试，如果面试官尚未响应（接受或拒绝）请求，将每 24 小时向面试官发送提醒。</span><span class="sxs-lookup"><span data-stu-id="2ee55-142">For all 1:1 interviews, reminders are sent to the interviewers every 24 hours if the interviewer has not responded (accepted or declined) to the interview request.</span></span>

    > <span data-ttu-id="2ee55-143">对于所有小组面试，没有自动的面试请求提醒。</span><span class="sxs-lookup"><span data-stu-id="2ee55-143">For all panel interviews, there are no automated reminders for the interview request.</span></span> <span data-ttu-id="2ee55-144">若要手动触发提醒，请编辑面试并使用 **更新并发送** 选项将请求发送回面试官。</span><span class="sxs-lookup"><span data-stu-id="2ee55-144">To trigger a reminder manually, edit the interview and use the **Update & Send** option to send the request back to the interviewers.</span></span>

    <span data-ttu-id="2ee55-145">面试官响应在 Attract 中捕获和显示。</span><span class="sxs-lookup"><span data-stu-id="2ee55-145">Interviewer responses are captured and shown in Attract.</span></span> <span data-ttu-id="2ee55-146">如果面试官拒绝邀请，您将被通知进行更改。</span><span class="sxs-lookup"><span data-stu-id="2ee55-146">If an interviewer declines the invite, you will be notified to make a change.</span></span> <span data-ttu-id="2ee55-147">若要在 **计划程序** 网格视图中查看其响应，请单击气泡图标。</span><span class="sxs-lookup"><span data-stu-id="2ee55-147">To view their response in the **Scheduler** grid view, click the bubble icon.</span></span>

<span data-ttu-id="2ee55-148">[![面试官响应的 Attract 招聘人员视图](./media/schedule-interviewer-response2.png)](./media/schedule-interviewer-response2.png)</span><span class="sxs-lookup"><span data-stu-id="2ee55-148">[![Attract recruiter view of an interviewer's response](./media/schedule-interviewer-response2.png)](./media/schedule-interviewer-response2.png)</span></span>

7. <span data-ttu-id="2ee55-149">在面试计划可以与应聘者共享后，请单击 **发送给应聘者**。</span><span class="sxs-lookup"><span data-stu-id="2ee55-149">After the interview schedule is ready to be shared with the candidate, click **Send to candidate**.</span></span> <span data-ttu-id="2ee55-150">您可以选择隐藏或显示应聘者的面试官姓名和时间段。</span><span class="sxs-lookup"><span data-stu-id="2ee55-150">You can choose to hide or show the interviewer names and slots with the candidate.</span></span>

8. <span data-ttu-id="2ee55-151">选择一个电子邮件模板并将面试汇总发送给应聘者。</span><span class="sxs-lookup"><span data-stu-id="2ee55-151">Select an email template and send the interview summary to the candidate.</span></span> <span data-ttu-id="2ee55-152">应聘者可以在其电子邮件以及其应聘者门户中查看此信息。</span><span class="sxs-lookup"><span data-stu-id="2ee55-152">The candidate can view this information in their email as well as on their candidate portal.</span></span>
    
>[!NOTE] 
> <span data-ttu-id="2ee55-153">只有当应聘者是内部应聘者时，应聘者的日历可用日期才会显示。</span><span class="sxs-lookup"><span data-stu-id="2ee55-153">The calendar availability of a candidate is shown only if the candidate is internal.</span></span> <span data-ttu-id="2ee55-154">同样，仅内部应聘者可以用于增强面试计划建议。</span><span class="sxs-lookup"><span data-stu-id="2ee55-154">Similarly, only an internal candidates can be used to enhance interview schedule recommendations.</span></span> <span data-ttu-id="2ee55-155">目前，应聘者（外部或内部）不接收电子邮件会议邀请，而只接收面试汇总。</span><span class="sxs-lookup"><span data-stu-id="2ee55-155">Currently, candidates (external or internal) don't receive an email meeting invite, instead the candidate receives only a summary of the interviews.</span></span>

<span data-ttu-id="2ee55-156">应聘者将收到该电子邮件，其中汇总了其面试圈。</span><span class="sxs-lookup"><span data-stu-id="2ee55-156">Candidates will receive the email summarizing their interview loop.</span></span> <span data-ttu-id="2ee55-157">此电子邮件中包含一个 .ics 文件，可将该文件保存到个人日历，以便更容易访问，还包含有关面试的通知。</span><span class="sxs-lookup"><span data-stu-id="2ee55-157">The emails contain an .ics file which can be saved to their personal calendars for easier access and notfications about the interview.</span></span>

>[!TIP] 
> <span data-ttu-id="2ee55-158">如果重新将面试计划发送给应聘者，应聘者将再次收到一个 .ics 文件附件。</span><span class="sxs-lookup"><span data-stu-id="2ee55-158">In case you re-send the interview schedule to the candidate, they will receive another .ics file attachment.</span></span> <span data-ttu-id="2ee55-159">我们建议更新应聘者面试摘要的电子邮件模板，以确保应聘者删除以前添加的面试事件，这样就不会在日历中看到重复项。</span><span class="sxs-lookup"><span data-stu-id="2ee55-159">We recommend updating the email templates for the candidate's interview summary to ensure candidates delete the previously added interview events and do not see duplicates on their calendar.</span></span> 

## <a name="feedback-activity"></a><span data-ttu-id="2ee55-160">反馈活动</span><span class="sxs-lookup"><span data-stu-id="2ee55-160">Feedback activity</span></span>

<span data-ttu-id="2ee55-161">反馈活动在工作模板中是可选的。</span><span class="sxs-lookup"><span data-stu-id="2ee55-161">The feedback activity is optional in a job template.</span></span> <span data-ttu-id="2ee55-162">此活动允许面试参与者为申请人输入建议或反馈注释。</span><span class="sxs-lookup"><span data-stu-id="2ee55-162">This activity lets interview participants enter recommendations or feedback comments for an applicant.</span></span> 

<span data-ttu-id="2ee55-163">若要包括或限制应提供有关哪些应聘者的反馈，请在 **面试官应提供的反馈所属对象** 字段中选择一个值。</span><span class="sxs-lookup"><span data-stu-id="2ee55-163">To include or limit the candidates to provide feedback on, select a value in the **Who should interviewers provide feedback on** field.</span></span>  <span data-ttu-id="2ee55-164">可用选项为 **所有应聘者**、**外部应聘者** 和 **内部应聘者**。</span><span class="sxs-lookup"><span data-stu-id="2ee55-164">The available options are **All Candidates**, **External Candidates**, and **Internal Candidates**.</span></span> <span data-ttu-id="2ee55-165">例如，如果要在第一轮安排中跳过内部应聘者，请将 **面试官应提供的反馈所属对象** 设置为 **外部应聘者**。</span><span class="sxs-lookup"><span data-stu-id="2ee55-165">For example, if you want to skip internal candidates in the first round of scheduling, set **Who should interviewers provide feedback on** to **External Candidates**.</span></span>

<span data-ttu-id="2ee55-166">如果选择 **继承来自招聘团队的反馈参与者** 字段，招聘人员、招聘经理和面试官将自动进入反馈活动。</span><span class="sxs-lookup"><span data-stu-id="2ee55-166">If you select the **Inherit feedback participants from Hiring Team** field, the recruiter, hiring manager, and interviewers are automatically entered in the feedback activity.</span></span> <span data-ttu-id="2ee55-167">组织可以允许面试官在提交他们自己的反馈前查看其他人员的反馈。</span><span class="sxs-lookup"><span data-stu-id="2ee55-167">Organizations can allow interviewers to view the feedback of other people before they submit their own feedback.</span></span> <span data-ttu-id="2ee55-168">组织还可以允许面试官在提交反馈后编辑反馈。</span><span class="sxs-lookup"><span data-stu-id="2ee55-168">Organizations can also allow interviewers to edit their feedback after they submit it.</span></span> <span data-ttu-id="2ee55-169">面试官被提醒为其最近根据工作模板中的预设配置进行的面试提交反馈。</span><span class="sxs-lookup"><span data-stu-id="2ee55-169">Interviewers are reminded to submit feedback for the interviews they have recently conducted based on the preset configuration as part of the job template.</span></span> <span data-ttu-id="2ee55-170">工作中的招聘经理或招聘人员还可以选择手动提醒面试官提交反馈。</span><span class="sxs-lookup"><span data-stu-id="2ee55-170">The hiring manager or a recruiter on the job can also choose to manually remind an interviewer to submit feedback.</span></span>

## <a name="interview-activity"></a><span data-ttu-id="2ee55-171">面试活动</span><span class="sxs-lookup"><span data-stu-id="2ee55-171">Interview activity</span></span>

<span data-ttu-id="2ee55-172">面试活动是具有三个组件的可选活动：**应聘者可用日期请求**、**计划** 和 **反馈**。</span><span class="sxs-lookup"><span data-stu-id="2ee55-172">The interview activity is an optional activity with three components: **Candidate availability request**, **Schedule**, and **Feedback**.</span></span> <span data-ttu-id="2ee55-173">如果您在流程中需要应聘者的所有可用日期请求、计划和反馈，而不是单独使用，应在工作模板中使用面试活动。</span><span class="sxs-lookup"><span data-stu-id="2ee55-173">Use the interview activity in the job template if you want all of the candidate’s availability request, schedule, and feedback as part of the process instead of using them individually.</span></span>

<span data-ttu-id="2ee55-174">若要包括或限制要面试的应聘者，请在 **要面试的对象** 字段中选择一个值。</span><span class="sxs-lookup"><span data-stu-id="2ee55-174">To include or limit the candidates to be interviewed, select a value in the **Who are you interviewing** field.</span></span> <span data-ttu-id="2ee55-175">可用选项为 **所有应聘者**、**外部应聘者** 和 **内部应聘者**。</span><span class="sxs-lookup"><span data-stu-id="2ee55-175">The available options are **All Candidates**, **External Candidates**, and **Internal Candidates**.</span></span> <span data-ttu-id="2ee55-176">例如，如果要在第一轮面试中跳过内部应聘者，请将 **要面试的对象** 设置为 **外部应聘者**。</span><span class="sxs-lookup"><span data-stu-id="2ee55-176">For example, if you want to skip internal candidates in the first round of interviewing, set **Who are you interviewing** to **External Candidates**.</span></span>
